---
layout:
  width: default
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
  metadata:
    visible: true
  tags:
    visible: true
  actions:
    visible: true
---

# 💸 Gift Card



{% hint style="warning" %}
Desde Pow aconsejamos ante la habilitación del módulo para crear Gift Cards, el exhaustivo, minucioso y periódico control de este bloque dado que la creación de una Gift Card es estar creando dinero para utilizar en la web.&#x20;

Asimismo recomendamos la revisión de los perfiles y sus roles asignados para evitar y/o disminuir acciones que comprometan la integridad del sitio tanto como acciones mal intencionadas de terceros.

Lo aconsejable en este punto es que solo un grupo muy reducido de perfiles cuenten con acceso a este nuevo módulo.
{% endhint %}

En VTEX, la Gift Card es considerada un medio de pago más, y como tal, debe ser activado como medio de pago. Si no se activa como medio de pago, por más que se configuren Gift Cards, no podrán ser usadas ya que los clientes no tendrán un campo donde ingresar el código de la Gift Card.

Es importante diferenciar entre Gift Card y cupón de descuento, ya que son cosas distintas y VTEX los procesa distintos (la Gift Card debe ingresarse en la forma de pago al final del Checkout, mientras que el cupón de descuento puede ingresarse al principio del Checkout)

## Creación de Gift Card

Para crear una Gift Card, deberemos ingresar al admin dentro del bloque de Promociones, en la sección Tarjetas de regalo.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.22.18 p. m..png" alt="" width="189"><figcaption></figcaption></figure>

Una vez dentro del módulo, daremos click en el botón azul ubicado en la derecha llamado **"Nuevo Vale"**

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.22.54 p. m..png" alt=""><figcaption></figcaption></figure>

Procederemos a configurar los campos que se desean y que nos permite VTEX para la Gift Card. Los campos con los que contaremos son:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.24.00 p. m..png" alt=""><figcaption></figcaption></figure>

* **Valor:** Este expresará el valor en pesos que le adjudicaremos a la GC (Giftcard)
* **Fecha de vencimiento:** si quisiéramos que la misma tuviese una fecha límite para su utilización
* **Doc de identificación:** Dni con el cual se asociará la tarjeta de regalo (este campo no es obligatorio pero aconsejamos utilizarlo para así tener mayor control sobre la Gift card y solo quien sepa el dni podrá utilizar el medio de pago)
* **Colección:** Este campo no es obligatorio, sirve para indicar si queremos limitar la utilización de la Gift a una única colección
* **Restringido:** al tildar esta opción limitaremos el uso de la GC al dni asociado en los campos previos, es decir, para que la misma funcione correctamente, deberá cargarse en el checkout el mismo dni que se configuró previamente desde el back a la GC.
* **Recargable:** Tildando esta opción, indicaremos que la Gift Card que estamos configurando podrá ser recargable, es decir, podremos volver a generarle monto disponible para utilizar en la tienda
* **Reutilizable:** Indicará que la Gift Card que estamos configurando no será de un solo uso, sino que podrá ser utilizable hasta agotarse su saldo, en caso de no tildar esta opción la gift quedará limitada a un solo uso más allá de que quede saldo restante en ella.

Una vez configurados todos los campos de la Gift Card, le damos a guardar y ya tendremos la misma lista para ser utilizada en la web.

{% hint style="danger" %}
Se aconseja siempre asociar una Gift Card con un número de DNI y tildar el campo restringido para así garantizar la integridad del proceso. Con estos pasos podremos evitar el uso indebido de un tercero de la Gift Card. Solo podrá ser utilizado por quienes conozcan el numero de dni asociado y el nombre de la Gift
{% endhint %}

## Gift Card y Oh Gift Card

### Gift Card Vtex

La Gift Card que solemos llamar "nativa" es la creada en VTEX  y la misma se utiliza para cambios o para realizar compras de prueba en el sitio.&#x20;

Para abonar con esta opción, se deberá seleccionar en el checkout(en el paso 3) la opción Gift Card 47 (Cambios)

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-11 a la(s) 4.40.08 p. m..png" alt=""><figcaption></figcaption></figure>

### Oh Gift Card

La [Oh Gift Card](https://www.ohgiftcard.com.ar/) es externa a VTEX y se utiliza para que los usuarios puedan regalarlas, y luego para que los usuarios puedan abonar un pedido con las mismas. Las mismas deben generarse y administrarse desde la plataforma propia de Oh Gift Card.

Para abonar con esta opción, se deberá seleccionar en el checkout(en el paso 3) la opción Oh Gift Card  (Regalo)

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-11 a la(s) 4.38.34 p. m..png" alt=""><figcaption></figcaption></figure>

## Utilización de Gift Card

El método de pago Gift Card aparece en las opciones de pago en el 3 paso del proceso de compra.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.33.29 p. m. (1).png" alt=""><figcaption></figcaption></figure>

Una vez que se selecciona el medio de pago Gift card, aparece la caja de texto para introducir el código de la Gift card según corresponda:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-11 a la(s) 4.58.09 p. m..png" alt=""><figcaption></figcaption></figure>

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-11 a la(s) 5.03.30 p. m..png" alt=""><figcaption></figcaption></figure>
