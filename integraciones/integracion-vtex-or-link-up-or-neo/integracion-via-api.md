---
hidden: true
---

# Integración vía API

Actualmente desde Link Up se encuentran trabajando en la migración de la integración con el ERP a través de la nueva API que cuenta NEO.&#x20;

Una vez que se finalice este trabajo, los detalles de la integración serán los siguientes:

* Quedará registrado en Link Up si el proceso de actualización corrió correctamente o no. Hay logs que se guardan por SKU actualizado, y se puede ver el historial del JOB en sidekiq StreetStockJob.
* De esta manera si la marca requiere saber si la actualización de stock y precios se llevó a cabo exitosamente o arrojó algún error, es posible verificarlo.

1. **Información de Stock y Precios a Link Up**

Para realizar esta integración Link Up consulta a NEO por API, para obtener actualizaciones de Stock y Precios:

* **Stock >** Las temporadas que utilizamos son la 10, 33, 34, 35 y 36. Para que estén al tanto la temporada 10 es en la cuál unificamos los productos de temporadas pasadas. Los códigos son "10", "33", "34", "35" y "36". Entonces quedaría de esta manera:

{

&#x20;   "TipoDeItem": "ProductoTerminado",

&#x20;   "DepositoCodigo": "2",

&#x20;   "TemporadaCodigo": "10"

}

* **Precio >** Las listas de precio que vamos a utilizar son: "público" y "acuerdo". Acuerdo es el full price y público el precio con descuento.

1. PÚBLICO: "LISTA 1"
2. ACUERDO: "LISTA 2"

{% hint style="info" %}
La actualización será 40 min en ambos casos (los tiempos de actualización quedan iguales a como estaban con la actualización por FTP)
{% endhint %}

2. **Actualización de Stock y Precios en Vtex**

Una vez que Link Up hace la consulta por API a NEO, comienza a impactar en Vtex, también mediante API las actualizaciones correspondientes.

_Para actualizar stock y precio Link Up usa el job “StreetStockJob” (mismo para stock y precio)_

3. **Búsqueda de órdenes en Vtex**

Vtex envía la notificación a Link Up cuando ingresa un nuevo pedido, y lo hace informando únicamente el ID de la orden.

Link-Up es el responsable de buscar por API en Vtex con ese ID recibido, para guardarla en la base de datos e informarla posteriormente (según el estado de la orden)

_Esta actualización se realiza de forma online._

{% hint style="success" %}
Los estados que se consideran son los siguientes:

"status": \[

* "payment-approved",
* "ready-for-handling",
* "cancel"
{% endhint %}

4. **Informe de ventas a NEO**

Link-Up luego de tener procesada una venta en VTEX, normaliza la información y la adapta para que pueda ser procesada por Neo Retail. Esta información se hace también vía API

_Esta actualización se realiza de forma online._

### **Registro de errores al informar pedidos a NEO**

Con el objetivo de tener conocimiento sobre los errores y motivos de pedidos que no pasan a NEO correctamente.

Se crea una pantalla en el front de Link Up donde se disponibiliza el nº de pedido y la respuesta/error arrojado por NEO.

#### ¿Cómo revisar y visualizar esta información?

1. Ingresar a la cuenta de Link up
2. Seleccionar **“Activar Microservicios”**

<figure><img src="../../.gitbook/assets/image (13).png" alt="" width="563"><figcaption></figcaption></figure>

\
3\. Entrar en Microservicios y seleccionar el link de **“Revisar errores API”**

<figure><img src="../../.gitbook/assets/image (14).png" alt="" width="563"><figcaption></figcaption></figure>

4. Al ingresar se verán 2 filtros:

* **Por fecha:** se debe colocar fecha de inicio a fin, y al buscar en la tabla inferior aparecerán todos los pedidos que la API de NEO arrojó error y no se informaron correctamente dentro del periodo seleccionado
* **Por nº de pedido:** Se puede buscar una orden en particular y buscar. En la tabla aparecerá el detalle correspondiente al pedido filtrado

<figure><img src="../../.gitbook/assets/image (15).png" alt="" width="563"><figcaption></figcaption></figure>

5. La información disponibilizada es la siguiente:

* Nº de pedido
* Mensaje de error arrojado por NEO

<figure><img src="../../.gitbook/assets/image (86).png" alt=""><figcaption></figcaption></figure>

### Worker para reinformar pedidos a la API y reinforme manual

Con el objetivo de contar con un mecanismo que permita **reintentar el envío de pedidos a la API de NEO** cuando por algún motivo no se hayan informado en el primer intento (por error, caída de servicio, timeout, etc) se disponen de dos frentes de ejecución complementarios:

**1) Re-intento Automático**\
Se desarrolló un worker que se ejecuta de forma periódica **(frecuencia de ejecución: cada 6 horas)** que:

* identifica pedidos que quedaron sin informar o con error
* reprocesa y reinforma esos pedidos a la API de NEO sin intervención manual

Este proceso automático asegura cobertura general y evita la necesidad de monitoreo humano constante.

**2) Re-intento Manual**\
Adicionalmente y como refuerzo, la marca mantiene la capacidad de informar pedidos puntuales de forma manual, ingresando el número de pedido directamente (como hacen hoy desde la pantalla actual de LinkUp).\
Este mecanismo funciona como “método de contingencia rápida”, para poder reintentar un pedido aislado sin esperar la próxima ejecución del worker automático.

<figure><img src="../../.gitbook/assets/image (8).png" alt="" width="361"><figcaption></figcaption></figure>

**Los pasos a seguir para utilizar esta pantalla son los siguientes:**

1. Iniciar sesión en Link Up
2. Activar microservicios
3. Seleccionar del menú izquierdo la solapa "Microservicios"
4. Dentro de la primer línea de la tabla seleccionar "Reinformar órdenes"

<figure><img src="../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>
