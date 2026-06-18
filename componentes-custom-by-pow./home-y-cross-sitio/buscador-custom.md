# 📌 Buscador custom

## Descripción

Este componente permite mejorar la visualización de las búsquedas y productos recomendados en el buscador. Tanto los tabs de "Lo más buscado" como el carrusel de productos que se muestra , son configurables desde un archivo del checkout.&#x20;

<figure><img src="../../.gitbook/assets/47-buscador.gif" alt=""><figcaption></figcaption></figure>

### Pasos para la configuración

1. Acceder al administrador de VTEX.
2.  Ingresar por Configuración de la tienda > Storefront > Checkout<br>

    <figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>
3.  Al ingresar, debemos hacer click en la ruedita que se encuentra junto al nombre de la tienda<br>

    <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-09-24 a la(s) 12.49.53 p. m..png" alt="" width="308"><figcaption></figcaption></figure>
4.  Una vez allí, hacemos click en la pestaña **Código** y en el archivo llamado **search\_context.json**<br>

    <figure><img src="../../.gitbook/assets/search1.png" alt=""><figcaption></figcaption></figure>
5.  Al abrir el archivo, nos encontramos con los campos a editar:<br>

    <figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

    * **customTopSearches:** Dentro de este campo se deben configurar los tabs que se mostrarán por debajo del título "Lo más buscado". Para modificarlo, deben editar los valores que se encuentran entre comillas en los campos "term" y "url". Por ej:\
      `{ "term": "Calzado", "url": "/calzado" },`
    * **suggestedProductsCollection:** Dentro de este campo se debe configurar el ID de la colección que se mostrará como recomendación de productos. Para modificarla, deben editar el valor que se encuentran entre comillas. Por ej:\
      `"suggestedProductsCollection": "111",`
    * **suggestedProductsTitle:** Dentro de este campo se debe configurar el título que se mostrará por encima de de los productos recomendados. Para modificarlo, deben editar el valor que se encuentran entre comillas. Por ej:\
      `"suggestedProductsTitle": "Recomendado para vos",`
    * **maxSuggestedProducts**: Dentro de este campo se debe configurar el máximo de productos de la colección que se mostrará en el bloque de los productos recomendados. Para modificarlo, deben editar el valor que se encuentra en el archivo (no sumar comillas). Por ej:\
      `"maxSuggestedProducts": 12`
