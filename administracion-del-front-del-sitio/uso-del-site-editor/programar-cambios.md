# Programar cambios

## ¿Qué son las versiones de contenido?

La versión de un bloque es una copia de su contenido en un momento determinado. Por ejemplo, un Carrusel puede tener versiones predefinidas para futuras campañas de marketing, como Black Friday y San Valentín, con banners de contenido específico.

Con la función Versiones, puedes crear, programar y probar diferentes contenidos para un bloque determinado sin comprometer la versión publicada de tu tienda. Cada bloque disponible en el Site Editor puede tener múltiples versiones.

## Programar cambios

Esta documentación se desprende de la documentación [**Site Editor**](../site-editor.md), por lo que es recomendable primero leer dicha documentación y posteriormente referirse a la documentación de programación de cambios.

Una vez ya se está en el site editor, es necesario localizar el bloque que se desee programar. Por ejemplo, en este caso tomaremos el Layout del slider de la home de 47 Street

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.07.17 a. m..png" alt=""><figcaption></figcaption></figure>

Al hacer click sobre el bloque a editar, hay una sección en la parte superior derecha que indica VERSIONES. Le damos click.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.07.39 a. m..png" alt=""><figcaption></figcaption></figure>

Al hacerle click, VTEX mostrará todas las versiones que existen de ese mismo bloque. En este caso, hay una única versión que indica algunas características VITALES de la versión:

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.09.47 a. m..png" alt=""><figcaption></figcaption></figure>

* **ACTIVO:** Significa que es la versión que está visible en el sitio actualmente, esa versión es la que todos los usuarios que navegan el sitio están viendo.
* **Contenido sin título:** En caso  de que la versión tenga un título, se mostrará aquí. Simplemente es una nomenclatura para poder identificarla. Es administrable y puede ser cambiado a gusto por el administrador, y no es visible por el usuario.
* **Guardado en el template:** Esto quiere decir que este cambio está guardado en la plantilla de esa página. En el caso de la home no tiene mucho sentido ya que sólo hay una única página utilizando la plantilla y es la home, pero en el caso del menú por ejemplo, se podría hacer una versión sólo para una URL. Por el contrario, si se quiere versionar algo en el menú para todo el sitio, debería ser en la plantilla del menú y no en la URL. Ya se verá a profundidad en la edición de versiones, pero es importante este dato para que podamos ver a simple vista qué versión afecta al template y cual no (si no está guardado en el template no dirá nada).
* **Creado por street47.store-theme:** Esto indica que es la versión ORIGINAL de ese bloque. Ello significa que esa versión puede ser modificada o pueden ser creadas otras versiones, pero esa versión original no puede ser borrada, sólo restaurada. Ya retomaremos este tema a profundidad también cuando hayamos creado una versión, pero es importante para saber que esta versión no se podrá borrar y es la original de ese bloque.

Ahora, para crear una nueva versión, se debe dar click a **Nueva versión.**

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-08 a la(s) 4.26.42 p. m..png" alt="" width="205"><figcaption></figcaption></figure>

Al crear una nueva versión, tendremos los mismos campos que en el bloque original, con la salvedad de que habrá un apartado adicional al final que se llama **Visibilidad**.

<figure><img src="../../.gitbook/assets/versiones5 (1).png" alt="" width="188"><figcaption></figcaption></figure>

{% hint style="info" %}
Es importante asegurarse de replicar tal cual las configuraciones del bloque, para evitar que al activarse se vea de alguna forma que no sea la indicada.&#x20;
{% endhint %}

La primera opción es de cuándo se activará:

* **Activar ahora:** Activa la versión en el momento en el que se guarda y pasa a ser la versión visible para todos. Si se activa, no se puede programar fecha de inicio.
* **Programar una fecha de inicio:** Activa la versión en el momento indicado que se haya configurado en esa versión. Si se activa, no se puede tildar activar ahora.
* **Programar una fecha de fin:** Esta es la forma de indicar que en determinada fecha la versión debe apagarse. Esto es porque la versión original no tiene programación de inicio, por lo que con esta opción se controla cuándo debe volver a la versión original.

Por buenas práctica se recomienda siempre programar fecha de fin, incluso cuando la versión vaya a ser reemplazada por otra versión y no la original, se programa la versión 1 con fecha de fin y la versión 2 que lo reemplazará con fecha de inicio ambas en la misma fecha y hora.

Y las segunda opción corresponde a si se activará en el template o en la url.

* **Esta URL:** Se aplicará la versión únicamente en la URL en la que se está actualmente y en ninguna otra más, por lo que si es una página con una misma plantilla en varias páginas (como sucede por ejemplo en la página de Producto, o en el Menú) el cambio será visible únicamente en esa URL.
* **Este template:** El cambio se activará en toda la plantilla, por lo que se verá en todas las URLs que utilicen esa plantilla. Por defecto, las versiones originales del bloque se activan en template, por lo que no es posible aplicar una versión original a una sola URL.

En el caso de este primer ejemplo, al tratarse de una modificación hecha en la home y siendo que sólo se tiene una home en el sitio, aplicarlo al template o a la URL será exactamente lo mismo.

Una vez guardemos la versión, podremos observar las dos versiones que están configuradas para ese bloque.&#x20;

<figure><img src="../../.gitbook/assets/veeriones6 (1).png" alt=""><figcaption></figcaption></figure>

En el caso de que la versión no deba ser publicada o por cualquier razón se quiera eliminar, en los tres puntos es posible hacer click en ELIMINAR, opción que como ya establecimos, no tiene la versión original ya que la versión original no puede eliminarse, sólo restablecerse al contenido predeterminado del bloque (el mismo que sale por defecto al crear una nueva versión).

<figure><img src="../../.gitbook/assets/versiones6 (1).png" alt=""><figcaption></figcaption></figure>

### **Consideraciones**

1. No se recomienda almacenar versiones antiguas. La recomendación es que luego de un evento o de un cambio, la versión que se antigua sea borrada, de forma que a lo sumo esté la versión original, y las versiones que estén activas o programadas para activarse. De esta forma se mantendrá un orden y no habrá versiones antiguas que puedan llevar a publicar algo viejo que no corresponde.
2. Siempre programar fecha de fin, aún si lo que se programa luego es otra versión y no la original, para evitar errores de publicación de versiones.
3. No todos los elementos son aptos para versionar, ya que algunos bloques vienen específicamente configurados desde código y tienen elementos no editables. En este caso, esas modificaciones deberán seguir haciéndose de forma manual.
