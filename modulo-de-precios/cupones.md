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

# 💸 Cupones

{% hint style="warning" %}
Desde Pow aconsejamos ante la habilitación del modulo Cupones, el exhaustivo, minucioso y periódico control de este bloque dado que la creación de un Cupón es estar creando dinero para utilizar en la web. Asimismo recomendamos la revisión de los perfiles y sus roles asignados para evitar y/o disminuir acciones que comprometan la integridad del sitio tanto como acciones mal intencionadas de terceros.

Lo aconsejable en este punto es que **solo un grupo muy reducido de perfiles** cuenten con acceso a este nuevo módulo.
{% endhint %}

### Cupones <a href="#cupones" id="cupones"></a>

Para crear un cupón de descuento, es necesario dirigirse al módulo Promociones -> Cupones. Una vez allí, tendremos un listado de los cupones actuales y la opción de "Crear cupón". Le haremos click.

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FrLPg4GeNC1P9kxp9zFfV%252F2.png%3Falt%3Dmedia%26token%3D5461b7d5-4bd9-45d2-b248-129a550da826&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=9c4e3497&#x26;sv=2" alt=""><figcaption></figcaption></figure>

### Uso del cupón y promociones asociadas <a href="#uso-del-cupon-y-promociones-asociadas" id="uso-del-cupon-y-promociones-asociadas"></a>

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252F6Amw3KkwFLNiC82zbSbB%252F3.png%3Falt%3Dmedia%26token%3D93f445f6-2d8f-4902-841c-4d12a27a8b75&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=f9bf6594&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Desde esta sección podremos ver tanto la cantidad de veces que se utilizó este cupón, como la cantidad y las promociones que están asociadas a este cupón.

Para que el cupón funcione, sí o sí debe estar asociado a una promoción. Para ello, se puede crear directamente la promoción o asociarla manualmente. Para más información revisar[ Asociar cupón a promoción.](https://pow-ecommerce.gitbook.io/vtex-clientes/modulo-de-precios/cupones#asociar-cupon-a-promocion)

### General <a href="#general" id="general"></a>

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FQVhQReLdvC1Ertdkn0FZ%252F4.png%3Falt%3Dmedia%26token%3D52a9fc5e-4817-4ca1-be46-f5558cf7b3fa&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=4a830c05&#x26;sv=2" alt=""><figcaption></figcaption></figure>

En las configuraciones generales, tendremos en principio el código del cupón. Este código será el que tenga que ingresar el cliente, por lo que debe reflejar la intención del cupón. En el caso de generarse cupones en lote, será el prefijo de todos los códigos.

Ejemplo, si nuestro código del cupón es "Cupónprueba" y generamos en lote, los códigos podrán ser "Cupónprueba-15sgds56fa", "Cupónprueba-542fds54" y así.

Fuente UTM y Campaña UTM son parámetros de la URL para poder rastrear el alcance del cupón. Si bien no se necesitan ambas, es obligatorio tener al menos una configurada.

* **utm\_source:** el origen del tráfico, es decir, de qué sitio, anunciante o publicación vino el usuario.
* **utm\_campaign:** el nombre de la campaña que define determinado contexto de marketing (ejemplos: natal, lanzamiento, promo01).

La generación de cupones en lote permitirá que podamos tener distintos subcupones para el mismo cupón, y así poder diferenciar de repente dentro de un mismo cupón general, cual sí se usó y cual no, o poder repartir varios cupones que puedan utilizarse una sola vez. 1000 es el máximo permitido.

Al habilitar restricciones, estaremos limitando el uso de cada cupón.

### Restricciones <a href="#restricciones" id="restricciones"></a>

Al habilitar restricciones, estaremos limitando el uso de cada cupón.

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FLCCRVOX1qfFnjdYZi8FI%252Fimage.png%3Falt%3Dmedia%26token%3D2908472c-fc48-4cb3-984e-dd11830d20d5&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=faccf9ce&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Si se generan cupones en lote, la restricción aplica a cada subcupón de forma individual. Esto quiere decir que, si generamos 5 cupones en lote y asignamos una restricción de 2 usos máximos, cada cupón se podrá usar 2 veces, dando un total de 10 usos (Por ejemplo: 5 cupones X cada 2 usos = 10 total // 5 x 2 = 10).

Normalmente si se quiere generar un lote y que se utilice 1 vez cada uno, esta opción de restricción quedará en 1 máximo.

### Cupón generado <a href="#cupon-generado" id="cupon-generado"></a>

Una vez generado el cupón, en caso de haber activado la generación en lote, podremos entrar al cupón mismo y tendremos la posibilidad de copiar o exportar la **lista de cupones generados con su correspondiente código aleatorio.**

### Asociar cupón a promoción <a href="#asociar-cupon-a-promocion" id="asociar-cupon-a-promocion"></a>

Para que el cupón esté activo, es necesario asignarlo a una promoción existente o crear una. Para ello existen varias formas:

#### Asociar a promoción existente <a href="#asociar-a-promocion-existente" id="asociar-a-promocion-existente"></a>

Si la promoción ya existe, vamos directamente a la promoción y asignamos el mismo UTM que hayamos aplicado en el cupón. Si por ejemplo, nosotros configuramos el UTM de campaña "promoprueba", vamos a la promoción que queramos asignar y colocamos el mismo UTM.

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2Flh7-us.googleusercontent.com%2FYlWyE3IexShn3y-iHSgOmsRtiC42g6HfGI0BRWA1deTJuI5XyRmR6pTmf7-DcGRSdaRWoyW-mWU89LpSY3U__Rr2-jAkzusbeo-Ids355ieSyLA4eR4Vwv7A6c4WFuOCAaabvJETk9-cD7-BjZDhAeg&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=bc632d94&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Al ir a la promoción y asignar el mismo UTM y tipo (no confundir UTM source y UTM campaign) ya nos dará la lista de códigos a las que aplica:

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252Fqfx8VW6EMKkIf3n8JtS8%252Fimage.png%3Falt%3Dmedia%26token%3Dd57d642a-dc05-48e6-96eb-86967f501a73&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=de558414&#x26;sv=2" alt=""><figcaption></figcaption></figure>

#### Crear promoción en base al cupón <a href="#crear-promocion-en-base-al-cupon" id="crear-promocion-en-base-al-cupon"></a>

Si no tenemos la promoción creada, desde el recuadro "-- promociones asociadas" podremos directamente crear la promoción:

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FFemflEwWlT14nByWwNBJ%252F5.png%3Falt%3Dmedia%26token%3D74140231-3acd-4406-8fd7-ed1c84ec3c47&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=e5da1d3&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Desde esta misma opción podremos crear directamente la promoción en base a nuestras necesidades para ese cupón especifico:

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FVf5mjP9gq2B0WPNp5hgR%252F6.png%3Falt%3Dmedia%26token%3Df89689ac-918a-407d-82bd-3bb017caf020&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=decc6f14&#x26;sv=2" alt=""><figcaption></figcaption></figure>

#### Crear cupón en base a la promoción <a href="#crear-cupon-en-base-a-la-promocion" id="crear-cupon-en-base-a-la-promocion"></a>

Si ya tenemos la promoción pero aún no tenemos el cupón, desde la misma pantalla de Promociones podremos crear un cupón en base a la UTM seleccionada.

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FP3GVirkLERMjY3M8pQzX%252F7.png%3Falt%3Dmedia%26token%3D7a46269f-1934-4510-9135-84f1a418ca3e&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=c67c47f3&#x26;sv=2" alt=""><figcaption></figcaption></figure>

De esta forma nos llevará directamente a la creación del cupón en base al UTM o los UTMs seleccionados en la configuración de la promoción.

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252F7hUvGzbtnUbtzs7uVKoy%252Fimage.png%3Falt%3Dmedia%26token%3D6d7753ef-66f7-4475-83f0-634237690af1&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=bdfc8c33&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Es posible utilizar en un cupón un utm source y un utm campaign al mismo tiempo.

Lo que NO es posible es no utilizar ninguno, ya que requiere al menos uno.
