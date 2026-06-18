# Banner de categorías (top banner)

## Descripción

Los banner de categoría son piezas gráficas que nos permiten darle a ciertas páginas de listado de productos un agregado visual.

Es la imagen que se visualiza al inicio de una sábana de producto (si está maquetado por IT).

{% hint style="warning" %}
Es importante aclarar que esta funcionalidad de Banner de categorías **no aplica para landings custom**. Si se desea agregar un top banner en ese tipo de landings, se deben hacer por código y maquetarlas con la intervención del equipo de IT.
{% endhint %}

## Cambio de banners

Para hacer uso del sistema de gestión de contenido, debemos ir al administrador de VTEX y buscar el módulo llamado **Storefront**. Allí, ingresaremos a la opción de **Multimedia**.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.15.18 a. m..png" alt=""><figcaption></figcaption></figure>

Si ya tenemos cargada la imagen por la cual queremos hacer el cambio, haremos click en los 3 puntitos de la imagen y seleccionaremos la opción de **Copiar URL**

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.17.32 a. m..png" alt=""><figcaption></figcaption></figure>

En cambio, si aún no hemos cargado la imagen, ingresaremos por **Agregar nuevo** y subiremos la imagen desde nuestro dispositivo.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.18.35 a. m..png" alt=""><figcaption></figcaption></figure>

Una vez subida la imagen, copiaremos la URL como  se indicó en el paso anterior.&#x20;

Luego, nos dirigiremos a **Storefront -> Banners.** Allí visualizaremos que ya tenemos creados los bloques de banners para las categorías principales.&#x20;

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.19.49 a. m..png" alt=""><figcaption></figcaption></figure>

Para modificar el banner de alguna de estas categorías, debemos ingresar por los 3 puntitos que se encuentran en la columna **Acciones** y seleccionar la opción **Editar.**

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.20.27 a. m..png" alt=""><figcaption></figcaption></figure>

Cuando ingresemos, debemos dirigirnos al bloque de HTML donde copiaremos la URL a modificar.&#x20;

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.27.52 a. m..png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Tener en cuenta que si optamos ingresar por la opción Imagen, se cargará la misma imagen para todas las resoluciones (desktop y mobile)
{% endhint %}

Una vez allí debemos reemplazar las imágenes existentes por las URLs que copiamos anteriormente.&#x20;

Por ej: Para el caso de Ropa de cama, vamos a encontrarnos este pedazo de código:

```html
<div class="banner-cat">
    <picture>
     <source srcset=https://street47.vteximg.com.br/arquivos/banner-testing.jpg media="(min-width: 720px)">
     <source srcset=https://street47.vteximg.com.br/arquivos/banner-testing.jpg media="(max-width: 720px)">
    <img class="banner-cat-image" src=https://street47.vteximg.com.br/arquivos/banner-testing.jpg  alt="Test"/>
    </picture>
    </div>
    <style>.banner-cat{position: relative;width: 100%;}.banner-cat-image{width: 100%;}@media screen and (max-width:720px){.banner-cat,.banner-cat-image{width: 100%;}}</style>
    [...] el código sigue
```

Dónde:

1. La primer etiqueta source, tendrá la URL de la imagen para desktop.&#x20;
2. La segunda etiqueta source, tendrá la URL de la imagen para mobile
3. La etiqueta image, tendrá también la URL de la imagen para desktop (imagen por default).&#x20;

Es importante que únicamente editen el tramo que dice **srcset=**"URL de la imagen".&#x20;

## Eliminar banners

Para esto debe tenerse en cuenta que si eliminamos un banner, estaremos eliminando el bloque y no solamente la imagen.&#x20;

Nos dirigiremos a **Storefront -> Banners**, haremos click en los tres puntitos del banner que queremos eliminar y seleccionamos la opción **"Eliminar".**

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 10.29.07 a. m..png" alt=""><figcaption></figcaption></figure>

Hecho eso, el banner dejará de visualizarse.

## Crear un banner

Para crear un banner, debe insertarse un código en HTML para ajustar la posición y los estilos de la categoría. Recomendamos solicitarlo al equipo de IT de Pow. para evitar inconvenientes, pero en caso que quisieran crearlo, pueden copiar el código HTML de alguna de las otras categorías ya creadas por Pow.

Al momento de realizada esta documentación, el código HTML es el siguiente:

```
<div class="banner-cat">
    <picture>
     <source srcset=https://street47.vteximg.com.br/arquivos/banner-testing.jpg media="(min-width: 720px)">
     <source srcset=https://street47.vteximg.com.br/arquivos/banner-testing.jpg media="(max-width: 720px)">
    <img class="banner-cat-image" src=https://street47.vteximg.com.br/arquivos/banner-testing.jpg  alt="Test"/>
    </picture>
    </div>
    <style>.banner-cat{position: relative;width: 100%;}.banner-cat-image{width: 100%;}@media screen and (max-width:720px){.banner-cat,.banner-cat-image{width: 100%;}}</style>

```

## Medidas

* **Desktop:** 2880x510
* **Mobile**: 750x258

{% hint style="info" %}
VTEX requiere de aproximadamente 30 minutos para que impacte el cambio correctamente, es normal que no se vea al instante.
{% endhint %}
