# 🛒 Transacciones

## Descripción

Al momento en que, luego de completar los datos en el checkout, se hace click en comprar, VTEX dispara cuatro eventos en simultáneo que harán una serie de comprobaciones para aprobar o desestimar la compra.

Si alguno de esos cuatro eventos falla, la transacción será rechazada, pero esto no quiere decir que haya un problema con VTEX o la pasarela, si no que simplemente el pago no pudo realizarse. Datos erróneos como código de seguridad o falta de fondos son los principales inconvenientes que rechazarán la transacción.&#x20;

## Visualización

Desde el módulo de **Pedidos ->Transacciones** es posible consultar sobre el estado de una transacción en particular.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.01.37 p. m..png" alt=""><figcaption></figcaption></figure>

Para emparejar la orden con su respectiva transacción, debemos tomar el número de clave que se encuentra entre paréntesis en el detalle de la orden o al final del número de orden dentro del listado de detalle de todos los pedidos:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.03.56 p. m..png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.05.24 p. m..png" alt=""><figcaption></figcaption></figure>

De esta forma, podremos emparejar la orden con su correspondiente transacción:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.07.00 p. m..png" alt=""><figcaption></figcaption></figure>

Dentro de la transacción encontraremos todos los datos respecto del intercambio de información entre VTEX y la pasarela de pago, y tanto si fue aceptado como si fue rechazado.

## Transacciones

### Elementos relevantes de la transacción

* **TID:** Transaction ID, en caso de tener algún inconveniente con el medio de pago (ej Mercado Pago), este número servirá como referencia para poder identificar qué sucedió con esa transacción.
* **Acquirer:** Será el medio de pago, la afiliación dentro de VTEX con la que se hizo el pago (Mercado Pago, MODO, Go Cuotas, etc)
* **AuthID:** Dato de autorización que devuelve el medio de pago
* **Message:** Siempre dirá "pending\_capture" porque quedará pendiente de captura al crearse. En caso de cancelarse, dirá por qué se canceló.
* **CardHolder:** Nombre del titular de la tarjeta con la que se intentó hacer el pago
* **ExpiryMonth y ExpiryYear**: Datos de los vencimientos de tarjeta
* **Adress:** Dirección que se está cargando para la compra, datos erróneos o vagos pueden activar el antifraude y trabar el pago.

### Lista de rechazos comunes

* **unauthorized\_use\_of\_live\_credentials:** Esto significa que las credenciales de la cuenta de Mercado Pago no están activadas. Debes ir a la página de credenciales y activarlas.
* **invalid\_installments:** Se está intentando procesar el pago con una tasa que no está habilitada.
* **Invalid\_users:** Se está intentando pagar con el mismo usuario al que se le está cobrando.
* **Cannot infer payment method:** Se está intentando pagar con una tarjeta que no es del tipo seleccionado (ej seleccionar crédito visa y querer usar con débito visa).
* **Invalid users involved:** Sucede cuando credenciales de prueba se utilizan en entornos productivos o viceversa.
* **High risk:** Está siendo rechazado por el antifraude de Mercado Pago.
* **Other reason:** Está siendo rechazado por el banco y no se proveyó ningún motivo.
* **Black list:** Tarjeta denunciada como robada o perdida.
