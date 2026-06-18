# Integración vía FTP

{% hint style="info" %}
Actualmente presentan este tipo de integración activo, pero a futuro se migrará al uso de la API de NEO
{% endhint %}

1. **Información de Stock y Precios a Link Up**

Para realizar esta integración se habilitó un FTP en el cual Neo Retail deja 2 archivos (archivo de stock y archivo de precios) para realizar actualizaciones. Link-Up se encarga de procesar los archivos para luego impactarlos en Vtex.

_Tiempo de actualización de stock y precios:_ actualmente se actualizan cada 40 min en ambos casos.

_Precios:_ Se actualiza únicamente el precio Full Price.

{% hint style="success" %}
El FTP donde NEO deja los archivos de Stock y Precios es **propiedad de Pow**
{% endhint %}

2. **Actualización de Stock y Precios en Vtex**

Una vez procesados los CSV, Link-Up comienza a impactar mediante API a Vtex las actualizaciones indicadas en el CSV para cada SKU.

Es importante saber que los artículos que no estén catalogados en VTEX no serán procesados.

3. **Búsqueda de órdenes en Vtex**

Link-Up es el responsable de buscar las nuevas órdenes que generan en VTEX para que luego sean normalizadas para su futuro procesamiento, al ser informadas al ERP (Neo Retail). Esta integración está realizada por API, haciendo llamadas a las APIs de Vtex.

_Tiempo de actualización: Online._

4. **Informe de órdenes a NEO**

Link-Up luego de tener procesada una venta en VTEX, normaliza la información y la adapta para que pueda ser procesada por Neo Retail. Se generan 2 archivos por cada venta tal como fue requerido por el ERP (un archivo con info de pagos y otra con info del pedido)

_Tiempo de actualización: Online, por cada venta.Los pedidos que ingresan a Vtex se informan al:_

* OMS inmediatamente, es decir con Pago Pendiente también, sin esperar la aprobación del pago

<figure><img src="../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

* A la PL (central y locales) únicamente cuando el pago ya se encuentra aprobado y el estado del pedido es "Listo para preparación" en Vtex > Ready for Handling
