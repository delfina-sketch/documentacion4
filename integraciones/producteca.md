---
hidden: true
---

# 🧩 Producteca

Se integra Producteca con Link Up para enviar las órdenes de MELI a NEO y PL sin la necesidad de pasar por Vtex.

Esta integración sólo tiene en cuenta las órdenes. La secuencia es:

1. Se envía la orden de Producteca a Link Up
2. Link Up se la envía a NEO y a la PL

{% hint style="info" %}
Se mantiene la integración Vtex <> Producteca para todo lo que es productos.
{% endhint %}

### Flujo de integración

<figure><img src="../.gitbook/assets/image (87).png" alt="" width="557"><figcaption></figcaption></figure>

1.  **Recepción de pedidos de Producteca**

    Producteca envía a Link Up, a través un endpoint (propio de Pow que les habilitamos), las notificaciones de creación de orden y cancelación. Link Up toma y guarda esa info y actualizaciones.
2. **Envío de pedidos a NEO y Picking List**

Link Up informa a:

* &#x20;NEO las órdenes de Producteca como una orden normal de Vtex

{% hint style="info" %}
Modificación > las órdenes que informa Producteca, ya no se informan a NEO con la identificación “**MLC-**&#x31;08362009” ya que era info de Vtex. Actualmente las órdenes se informan con el número de orden de Producteca, ejemplo: 108362009.
{% endhint %}

* Picking List con el sufijo **MLC** como lo informaba anteriormente Vtex.

3. **Informe de cambio de estado a Link Up**

La Picking List cuando despacha un pedido le informa a Link Up este cambio de estado.

4. **Informe de cambio de estado a Producteca**

Link Up le informa a Producteca este cambio de estado y el pedido pasa de “Por Enviar” a “En tránsito”

{% hint style="success" %}
**Etiquetas:** Si bien Link Up tiene integración con Producteca, las etiquetas las solicita el MSOOLL directamente a la API de Meli
{% endhint %}

{% hint style="warning" %}
Actualmente las compras realizadas en Mercado Libre Full, Link Up las filtra para que no ingresen en la Picking List, ya que estas son despachadas por el deposito de MELI.
{% endhint %}

## Worker creado para buscar órdenes que Producteca no informa

Debido a que Producteca por algún error no informa el total de órdenes que Link Up debe informar a la PL y NEO, y tampoco informa novedades con cambio de estado de órdenes, se desarrolló un worker en Link Up que busca órdenes en Producteca con los siguientes estados, para tomarlas, guardarlas en la base de datos de Link Up e informarlas a la PL y NEO.

#### Horarios agendados en los que se ejecuta el worker:

* 7hs
* 19hs

#### Estados que se consideran al ejecutar el worker:

**DeliverStatus** [**(Documentación)**](https://app.swaggerhub.com/apis-docs/product19/api-external/1.0.0#/DeliveryStatus) **- Estado de Entrega**

Tiene que tomar las órdenes en "PickingPending"

<figure><img src="../.gitbook/assets/image (88).png" alt=""><figcaption></figcaption></figure>

**PaymentStatus** [**(Documentación)**](https://app.swaggerhub.com/apis-docs/product19/api-external/1.0.0#/PaymentStatus) **- Estado de pago**

<figure><img src="../.gitbook/assets/image (89).png" alt=""><figcaption></figcaption></figure>

**Estado de etiqueta** [**(Documentación)**](https://app.swaggerhub.com/apis-docs/product19/api-external/1.0.0#/Shipment)

Toma las órdenes con estado "ReadyToPrint"

<figure><img src="../.gitbook/assets/image (90).png" alt=""><figcaption></figcaption></figure>

#### Otros puntos a tener en cuenta:

* El worker de Link Up busca 7 días para atrás en Producteca las órdenes que Producteca no informó.
* Se fija que si corresponden a Envío Full no pasan a la PL, pero a NEO sí se informan estas órdenes.
* Se fija que el pago esté "Approved", y si la orden se cancela, esto se informa como novedad a la PL para que la orden desaparezca.
* Se fija que la etiqueta no esté en "CreatingLabel" y si la misma cambia a "ReadyToPrint" Link Up la toma y si la informará.
