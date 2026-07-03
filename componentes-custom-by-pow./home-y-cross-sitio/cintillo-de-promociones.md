# 📌 Cintillo de promociones

## Descripción

Este componente permite cargar varias leyendas en un cintillo dinámico que va mostrando los mensajes en loop.&#x20;

Este componente permite editar el color de los textos, fondo, espaciado entre textos, configurar links, cantidad de mensajes y la posibilidad de mostrar u ocultar mensajes dentro del componente.&#x20;

<figure><img src="../../.gitbook/assets/image (96).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Se deberá cargar una configuración para el sitio en general como para la landing de Mich
{% endhint %}

<figure><img src="../../.gitbook/assets/image (97).png" alt=""><figcaption></figcaption></figure>

#### Pasos para la configuración

1.  Acceder al administrador de VTEX y abrir la sección de **Apps** y hacer click en **Aplicaciones instaladas** la que se llama **Cintillo Promocional.**<br>

    <figure><img src="../../.gitbook/assets/47-1 (2).png" alt=""><figcaption></figcaption></figure>
2. Al ingresar, contaremos con dos tabs: General y Mich, donde podremos cargar los estilos para cada caso de forma individual.&#x20;
3. Si ingresamos por General o Mich, podremos configurar los estilos para cada caso:
   1. **Mostrar cintillo?:** Permite activar o desactivar el componente.
   2. **Color de fondo:** Permite configurar el color de fondo del cintillo en formato hexadecimal o rgba.
   3. **Color del texto:** Permite configurar el color del texto del cintillo en formato hexadecimal o rgba.
   4. **Opacidad del fondo:** Permite configurar la opacidad del fondo en un número comprendido entre 0 y 1.
   5. **Espaciado vertical:** Permite asignar en px el espaciado arriba y abajo del texto del cintillo promocional.
   6. **Espaciado horizontal entre mensajes:** Permite asignar en px el espaciado entre cada texto del cintillo promocional.
   7.  **Pausar al pasar el mouse:** Si esta opción se encuentra activa, al pasar el mouse sobre el cintillo, la animación se detendrá (aplica desktop).<br>

       <figure><img src="../../.gitbook/assets/image (106).png" alt=""><figcaption></figcaption></figure>
4. Luego, únicamente desde la pantalla de General, tendremos la sección **Mensajes** que nos permitirá cargar los mensajes que se mostrarán en el cintillo y desde el CTA +Agregar mensajes se podrán cargar cada uno de los mensajes con sus respectivas configuraciones:
   1. **Titulo:** Podemos completar con un título para identificar cada uno de los mensajes desde el componente del site editor (no se mostrará en el cintillo).&#x20;
   2.  **Texto del mensaje:** Se debe completar con el mensaje que se mostrará en el cintillo. En caso de querer agregar un link, se deberá completar entre corchetes "\[]" la palabra que contendrá el link y entre paréntesis "()" el link. Por ej: PICK UP EN STORES.<br>

       <figure><img src="../../.gitbook/assets/image (107).png" alt=""><figcaption></figcaption></figure>
5. También contamos con la configuración del Pop-up de promociones donde podremos establecer tanto en el tab de General como en Mich:
   1. **Activar pop-up de promociones:** Permite administrar la visibilidad del pop-up en Mich y en el resto del sitio de forma individual
   2.  **Mostrar en dos columnas:** Permite activar esta funcionalidad en desktop de forma individual para Mich y el resto del sitio. <br>

       <figure><img src="../../.gitbook/assets/image (108).png" alt=""><figcaption></figcaption></figure>
6. Por último, para configurar la información que se mostrará en el pop-up, sólo debemos cargarla desde la pestaña General modificando o agregando nuevos items:
   1. **Título del modal:** Será el título que se muestre al abrirse el modal
   2. **Título identificador (admin):** Es un título identificatorio de la promoción dentro del cintillo (no se mostrará en el front).&#x20;
   3. **Imagen:** Se puede cargar una imagen que acompañe a la promoción, subiendo un archivo de imagen o completando la URL donde se encuentra alojada.
   4.  **Texto alternativo (alt):** Permite cargar un texto alternativo para la imagen para facilitar su accesibilidad.&#x20;

       <figure><img src="../../.gitbook/assets/image (109).png" alt=""><figcaption></figcaption></figure>
   5. **Título (texto):** Será el título de la promoción
   6. **Grosor:** Se puede elegir el peso de la fuente del título entre Normal (400), Medium (500) o Bold (700).&#x20;
   7.  **Color:** Deberá configurarse el color del título.&#x20;

       <figure><img src="../../.gitbook/assets/image (110).png" alt=""><figcaption></figcaption></figure>
   8. **Subtítulo (texto):** Se deberá completar con la información de la promoción o condiciones que quieran comunicarse.&#x20;
   9. **Grosor:** Se puede elegir el peso de la fuente del subtítulo entre Normal (400), Medium (500) o Bold (700).&#x20;
   10. **Color:** Deberá configurarse el color del subtítulo.&#x20;

       <figure><img src="../../.gitbook/assets/image (111).png" alt=""><figcaption></figcaption></figure>
   11. **Texto opcional (texto):** Sólo completar en caso de querer sumar alguna información opcional.&#x20;
   12. **Grosor:** Se puede elegir el peso de la fuente del texto opcional entre Normal (400), Medium (500) o Bold (700).&#x20;
   13. **Color:** Deberá configurarse el color del texto opcional. <br>

       <figure><img src="../../.gitbook/assets/image (112).png" alt=""><figcaption></figcaption></figure>
   14. **Desplegable:** En caso de activar esta opción, se mostrará el contenido cuando el cliente haga click en "Ver más" con el texto que se configure más abajo
   15. **Texto desglegable (texto):** Sólo completar en caso de querer mostrar un texto desplegable.&#x20;
   16. **Grosor:** Se puede elegir el peso de la fuente del texto desplegable entre Normal (400), Medium (500) o Bold (700).&#x20;
   17. **Color:** Deberá configurarse el color del texto desplegable. <br>

       <figure><img src="../../.gitbook/assets/image (113).png" alt=""><figcaption></figcaption></figure>
7.  Por último, tendremos dos CTA para **"Eliminar item"** o **"Agregar Item"** según corresponda y al finalizar hacemos click en **"Guardar Pop-up"** para guardar todos los cambios. <br>

    <figure><img src="../../.gitbook/assets/image (114).png" alt=""><figcaption></figcaption></figure>
