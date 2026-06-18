# 🛒 Información del pedido

## Descripción

Al ingresar al detalle de la orden, tendremos toda la información relacionada ordenada por distintos bloques.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.46.56 p. m..png" alt=""><figcaption></figcaption></figure>

## Cliente y entrega

Tendremos los principales datos del cliente: nombre, DNI, dirección, destinatario, correo, etcétera. De estos campos saldrán los datos para la factura y para el envío/retiro.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.47.36 p. m..png" alt=""><figcaption></figcaption></figure>

## Valor total del pedido

Es el detalle final de lo que pagó el cliente, contando impuestos, descuentos y envío.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.48.25 p. m..png" alt=""><figcaption></figcaption></figure>

## Pago

En este bloque se disponibilizará toda la información relevante del pago: método de pago, cuotas, time-stamp del pago, ID y un hipervínculo para ver toda la información desde el módulo transacciones para ver toda la información respecto de la transacción.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.49.32 p. m..png" alt=""><figcaption></figcaption></figure>

## Estado del pedido

Al ingresar un pedido, hay una serie de pasos por los que pasará y que hará que el pedido termine en alguno de estos dos estados: cancelado o facturado.

{% hint style="warning" %}
Es importante que los pedidos no queden en instancias previas, y que lleguen al status final de cancelado o de facturado. Si no, al quedar abierto el pedido, podrían cancelarse o darse problemas con la orden. Por ello, es importante que todo pedido correcto sea marcado como facturado.
{% endhint %}

Desde la vista general, podemos observar el flujo simplificado del pedido:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.50.06 p. m..png" alt=""><figcaption></figcaption></figure>

Ahora, si hacemos click en "Ver flujo completo", podremos observar la totalidad de los status y todo el flujo con sus únicos dos status finales:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.50.53 p. m..png" alt=""><figcaption></figcaption></figure>

El pedido, al estar aprobado y pasar la ventana de cancelación, pasará a "Listo para preparar". En ese momento se visualizará en la Picking List para preparar y despachar el pedido. Luego, una vez que se despache el pedido, el estado en Vtex cambiará a "Facturado".

Lo correcto es que el producto se facture una vez esté preparado el envío, de esta forma se evitan inconvenientes con stock o reservas excesivas de stock que desencadenen en un stock negativo (cuando en realidad, físicamente podría haber exceso de stock, pero VTEX asume, al no estar facturadas las órdenes, que hay cierta cantidad de productos reservados aún no facturados).



## Artículos para facturar

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.52.13 p. m..png" alt=""><figcaption></figcaption></figure>

Desde esta sección podremos ver la totalidad de items de la orden, tanto para la factura como para el envío.

Cada artículo tendrá, además de su precio, su cantidad, almacén y SKU propio (Referencia) de forma que podremos tomar ese valor y tener precisión sobre de qué SKU específico se trata.

Además, tendremos la transportadora elegida por el cliente y la entrega estimada calculada en base a las configuraciones de dicha transportadora.

{% hint style="info" %}
Tené en cuenta que este número no refleja el total a facturar, únicamente considera la facturación de productos. Recordá que en la parte superior se encuentra la caja llamada valor total del pedido, que contempla además el valor del envío.
{% endhint %}

## Historial de pedidos

Desde el historial de pedidos podremos ver **todo el historial de cambios** que sufrió el pedido desde su creación.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.53.25 p. m..png" alt="" width="299"><figcaption></figcaption></figure>

Además, podremos tener una vista de los correos transaccionales que le fueron enviados al cliente por esa orden.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.54.06 p. m..png" alt="" width="323"><figcaption></figcaption></figure>

## Comentarios

Es posible dejar comentarios de la orden dentro de la misma, en el caso de que se necesite dejar asentado algo particular o para comunicar algo a cualquier otro colaborador que ingrese a la misma. **Este comentario es interno, por lo que el cliente no podrá verlo.**

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.54.44 p. m..png" alt=""><figcaption></figcaption></figure>

## Cancelar pedido

En el caso que la orden se encuentre abierta, en la parte superior derecha tendremos disponible el botón de "Cancelar pedido", del que podremos hacer uso.&#x20;

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.55.45 p. m..png" alt=""><figcaption></figcaption></figure>

{% hint style="danger" %}
Esta acción es irreversible. Una vez que se canceló el pedido, no tendremos forma de dar marcha atrás. Si el cliente se arrepiente de la cancelación, deberá realizar la compra nuevamente.
{% endhint %}

Una vez cancelado, el pedido no podrá ser preparado o facturado y no tendremos más acciones para poder realizar en VTEX.

## Factura

Junto al botón de Cancelar pedido, tendremos el botón de Factura.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 9.56.44 p. m..png" alt=""><figcaption></figcaption></figure>

Ese botón nos llevará a una ventana que nos dará tres opciones posibles:

* **Enviar la factura con la referencia de los items:** Permite subir facturas en función a los productos. Si se emitieron dos facturas separadas correspondientes cada una a cada artículo, podrían subirse manualmente de esta forma.
* **Enviar una sola factura:** Permite enviar una factura por la orden, ya sea por el monto total o por un monto menor. Es importante saber que en caso de marcar que la factura es un valor parcial, la orden no pasará a Facturado. Es necesario facturar el total de la orden para que la orden pase al estado Facturado.
* **Solicitar factura:** En caso de trabajar con un ERP, es posible utilizar esta opción para cualquier cuestión que no haya permitido que la factura se emita correctamente.

{% hint style="warning" %}
Es importante que los pedidos queden facturados para que se pueda liberar el stock reservado en Vtex.

Cuando los pedidos son despachados desde la Picking List, los mismos cambian de estado de "Listo para preparación" a "Facturado" y se le impone un número de factura aleatorio.
{% endhint %}

