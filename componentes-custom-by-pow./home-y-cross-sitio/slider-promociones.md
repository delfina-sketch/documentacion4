# 📌 Slider promociones

## Descripción

Se realizó un componente custom para la visualización de un slide de promociones que se encuentra en Home y sábana.

Podrán configurar tanto promociones bancarias como las promociones que planteen tener en la web y configurar redirects.

<figure><img src="../../.gitbook/assets/image (60).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../.gitbook/assets/image (61).png" alt=""><figcaption></figcaption></figure>

## **Pasos para la configuración**

1. Acceder al administrador de VTEX.
2. Ingresar por **Storefront** → **Site Editor**.
3.  Al ingresar, debemos localizar el bloque llamado Slider Promotions.<br>

    <figure><img src="../../.gitbook/assets/image (62).png" alt=""><figcaption></figcaption></figure>
4.  Una vez adentro, vamos a visualizar un switch que nos indicará si el componente se encuentra o no visible. En caso que el switch esté en color **AZUL** se encontrará activo. Lo mismo para activar la transición del carrusel.

    <figure><img src="../../.gitbook/assets/image (64).png" alt="" width="251"><figcaption></figcaption></figure>

* Tendrán para completar:
  * Velocidad de transición (en ms): 800 ms es lo recomendable por defoul. Es la velocidad con la que se pasa a la card.
  * Retardo entre transiciones de diapositivas (en ms): no deberán completarlo.
  * Función de temporización. (omitir): no deberán completarlo.
  * Tiempo de espera (en ms) entre cada diapositiva: es el tiempo de espera que tarda en pasar a otra diapositiva.

5.  Luego tendran el switch para Determina si la reproducción automática debe detenerse cuando los usuarios pasan el cursor sobre el slide -> que es para que se detenga el slide si el usuario se posiciona en cima.

    <figure><img src="../../.gitbook/assets/image (65).png" alt="" width="245"><figcaption></figcaption></figure>
6.  Y por último les va a figurar para cargar todos los "Items del Carrusel" y los "Items del Modal":

    <figure><img src="../../.gitbook/assets/image (67).png" alt="" width="246"><figcaption></figcaption></figure>

    * "Items del Carrusel": deberán cargar todos los items que quieran que aparezcan en el Slider. Tendrán que configurar:
      * Título identificador: Título para identificarlo en el admin.
      * Texto Principal: texto que aparecerá en el Slider primero.
      * Grosor de la tipografia: grosor de este texto.
      *   Color del texto: el color que deseen.

          <figure><img src="../../.gitbook/assets/image (68).png" alt="" width="124"><figcaption></figcaption></figure>
      * Texto link: texto que tendrá que seleccionar el usuario para que ejecute la acción que configuren.
      * Grosor de la tipografia: grosor de este texto.
      * Color del texto: el color que deseen.
      * Y tienen dos opciones de las cuales deben encender una de las dos:
        * Encender si requiere que abra el modal, sino omitir -> si quieren que abra modal.
        *   URL de la redireccion (Omitir si abre el modal) -> si quieren que el usuario se redirija a otra URL.

            <figure><img src="../../.gitbook/assets/image (69).png" alt="" width="124"><figcaption></figcaption></figure>

*   "Items del Modal": deberán cargar todos los items que quieran que aparezcan en el Modal/Pop Up. Tendrán que configurar:

    * Título identificador: Título para identificarlo en el admin.
    * Imagen - logo: cargar la imagen.
    * Texto alternativo (alt) de la imagen.
    * Texto Principal: texto que aparecerá en el Slider primero.
    * Grosor de la tipografia: grosor de este texto.
    *   Color del texto: el color que deseen.

        <figure><img src="../../.gitbook/assets/image (70).png" alt="" width="111"><figcaption></figcaption></figure>



    * Texto Secundario: texto que aparecerá abajo del texto principal. En caso de que quieran que aparezca un link deberán ponerlo en el texto de la siguiente forma: \<a href ="/blabla"> www.onelink/blabla \</a >
    * Grosor de la tipografia: grosor de este texto.
    * Color del texto: el color que deseen.
    * Texto Opcional: texto que aparecerá abajo del texto Secundario.
    * Grosor de la tipografia: grosor de este texto.
    *   Color del texto: el color que deseen.

        <figure><img src="../../.gitbook/assets/image (71).png" alt="" width="105"><figcaption></figcaption></figure>
* Luego tendrán el switch opcional que podrán poner contenido más extenso -> Desea mostrar el contenido despleable? En caso de activarlo deberán completar el texto, Grosor y color. Y el mismo mostrará un "Ver mas" el cual usuario deberá seleccionar para ver el texto.

<figure><img src="../../.gitbook/assets/image (72).png" alt="" width="215"><figcaption></figcaption></figure>

##





