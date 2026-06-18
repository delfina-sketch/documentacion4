---
hidden: true
---

# 📌 Landing - Navegador de categorías

## Descripción

Landing en la que se podrá mostrar categorías como tabs. Las mismas van a cumplir la función de filtro, es decir, que si se selecciona una categoría que cambie la sábana pero sigan figurando las demás para elegir, y a su vez, se va a resaltar la categoría que se elija.&#x20;

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-05-29 a la(s) 10.20.27 a. m..png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/PASAR-A-GIFFF.gif" alt=""><figcaption></figcaption></figure>

## **Pasos para la configuración**

1. Acceder al administrador de VTEX.
2. Ingresar por **Storefront** → **Site Editor**.
3. Una vez en el sitio, se deberá ingresar en la sábana que se desee agregar este componente.
4.  Una vez que ingresamos en la sábana, vamos a resultado de busqueda flexible -> Navegador de categorías:

    <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-05-29 a la(s) 10.30.24 a. m. (1).png" alt=""><figcaption></figcaption></figure>
5. Adentro del componente hay dos cosas a configurar:
   * Mostrar el componente: que es para activar o desactivar el componente.
   *   Mostrar en Colecciones: que también tienen que tener activo para que se muestre el componente. En caso de que se lo desactiven lo que va a ocurrir es que cuando seleccionen una colección, no va a aparecer el componente, es decir, con esto desactivo, el componente solo aparece en la landing y no en las colecciones, por lo que para que al usuario le vuelva a aparecer tiene que volver a ingresar en la landing.

       <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-05-29 a la(s) 10.33.41 a. m..png" alt=""><figcaption></figcaption></figure>
6. Después entramos en Ítem y empezamos a configurar todas las colecciones que queremos que aparezcan:
   *   Ingresamos en Ítem:

       <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-05-29 a la(s) 10.50.46 a. m..png" alt=""><figcaption></figcaption></figure>
   * Lista de ids de las Colecciones en las que aparecerán los tabs en sabana: son todos los id de las colecciones en los que se quiere que aparezcan los tabs.
   *   Lista de tabs: son los tabs a configurar

       * En caso de que quieran que aparezca en todas las colecciones que colocan en los tabs, deberán coincidir las colecciones que ponen en ambos.

       <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-05-29 a la(s) 12.22.21 p. m..png" alt=""><figcaption></figcaption></figure>
7. En **Lista de tabs tendrán que configurar:**
   * **Título:** título para identificar el tab
   * Id de la colección: id de la colección a la que pertenecerá el tab
   * Nombre: Nombre que se mostrará en el tab
   * URL a la que te redirige: deben poner la url de la coleccion que pusieron el id.
   * Target de la ancla: siempre debe estar en \_self, ya que _\__&#x62;lank es para que al seleccionarla abra en otra pestaña.
   *   Color del tab cuando se activa: es el color del tab: deben moverlo de negro y volver a ponerlo en negro ya que a veces no lo toma (esto es un bug de VTEX que sabe que el selector no funciona correctamente)

       <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-05-29 a la(s) 11.13.40 a. m..png" alt=""><figcaption></figcaption></figure>


8.  Debe configurarse en Mobile y en Desktop:

    <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-05-29 a la(s) 11.25.20 a. m..png" alt=""><figcaption></figcaption></figure>

Consideraciones:

* Solo se pueden poner colecciones y categorías. No se puede en landings custom, como por ejemplo lo es /mich.
