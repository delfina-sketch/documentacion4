---
hidden: true
---

# 🧩 Integración Shopify (PACTO – Moda Circular)

### Introducción al proyecto "47 Circular"

47 Street lanza un nuevo proyecto de moda circular, con el objetivo de fomentar la sustentabilidad y ofrecer una experiencia innovadora a sus clientes.

El flujo de negocio es el siguiente:

* Los usuarios llevan sus prendas usadas a **sucursales adheridas**.
* A cambio, reciben **puntos en la app 47 Club**.
* Las prendas se reacondicionan y se ponen a la venta en una tienda online **Shopify**, gestionada por **PACTO**.

Este proyecto requiere integrar la tienda Shopify con los sistemas actuales de 47 Street para que los pedidos y la gestión de stock estén alineados en el ecosistema de **Link Up + OMS + NEO**.

### Alcance de la integración

La integración contempla:

* Conexión del **sitio Shopify (PACTO)** con **Link Up**.
* Envío de pedidos hacia **OMS** y **NEO**

{% hint style="warning" %}
Particularidad: **no interviene la PL (Picking List)** ya que el picking y preparación de pedidos se realiza directamente desde **PACTO**.
{% endhint %}

### Reglas y configuraciones específicas

#### Identificación de pedidos

* Todos los pedidos de Shopify (PACTO) que tengan pago aprobado deben ser informados al **OMS** y a **NEO**.
* El **código externo** para identificar estas órdenes en NEO es siempre: **`PACTO`**.

#### Archivo CSV de stock al informar pedidos a NEO

* La configuración será similar a la de MERCADOLIBRE FULL.
* Diferencia clave: en lugar de utilizar el código de depósito REPRO, se debe enviar el código de depósito **DC**.
* Este ajuste aplica **únicamente en los productos**.
* El ítem de **envío** no debe ser modificado.

Ejemplo:

<figure><img src="../.gitbook/assets/image - 2025-10-03T101329.333.png" alt=""><figcaption></figcaption></figure>

* El ítem **envío** en este archivo debe informarse siempre **debajo de los productos** dentro del pedido.
* Esto es necesario para que el flujo de facturación en NEO se procese correctamente.
