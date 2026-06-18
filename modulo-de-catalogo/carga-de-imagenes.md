---
description: >-
  Para realizar la carga de imágenes existen dos formas, dependiendo del volumen
  y la disponibilidad/comodidad de los datos: manual o masivo.
---

# 👕 Carga de imágenes

## Consideraciones

La carga de imágenes se hace únicamente por SKU. Los productos no tienen carga de imágenes, por lo que es necesario que el producto tenga al menos un SKU para poder realizar la carga.

## Carga manual

Para hacer la carga manual, posterior a la [carga de productos y skus](carga-de-productos-y-skus.md), nos dirigimos al SKU al que le queremos cargar las imágenes:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.12.37 p. m..png" alt=""><figcaption></figcaption></figure>

Una vez ahí, nos dirigimos a la pestaña llamada **imágenes**.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.14.39 p. m..png" alt=""><figcaption></figcaption></figure>

Ahí, veremos varias imágenes: en principio, se puede distinguir la imagen principal de ese SKU porque hay una opción que permite seleccionar la **imagen principal:**

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.16.34 p. m..png" alt=""><figcaption></figcaption></figure>

Para agregar una nueva imagen, haremos click en "**Insertar**"

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.17.59 p. m..png" alt=""><figcaption></figcaption></figure>

Ahí, seleccionaremos la imagen. Por otro lado, texto no es obligatorio y etiqueta lo utilizaremos únicamente en casos particulares.

Una vez completado, hacemos click en "**Enviar**", y una vez tengamos todas las imágenes necesarias cargadas, click en "**Guardar**" para guardar los cambios en ese SKU.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.19.09 p. m..png" alt=""><figcaption></figcaption></figure>

## Carga masiva

En caso de tener que cargar muchas imágenes, o de tener los datos en otro sistema del que los podemos extraer y plasmar en cantidad, podremos optar para la carga masiva.

{% hint style="info" %}
Es recomendable revisar la documentación[ Importación/Exportación](importacion-exportacion.md) antes de proseguir con la carga masiva.
{% endhint %}

Una vez teniendo la planilla de importación masiva, la abrimos y nos encontraremos con las siguientes columnas:

<figure><img src="../.gitbook/assets/Captura de Pantalla 2024-01-28 a la(s) 00.35.51.png" alt=""><figcaption></figcaption></figure>

Si bien hay ejemplos, no debemos olvidar eliminarlos para evitar importarlo y crearlo por accidente.

* **URL**: Es el enlace en el que VTEX irá a buscar la imagen para alojarla en su servidor. Esto quiere decir que la imagen que se muestre no quedará alojada en el servidor donde la tengamos alojada inicialmente, simplemente VTEX la tomará de ese servidor y la subirá al suyo propio, de esta forma aseguramos la disponibilidad de la imagen aún cuando el servidor primitivo donde estuvo alojada se caiga. La URL debe comenzar, sin excepción, con el identificador de protocolo HTTPS (https://) y terminar con la extensión del archivo (.jpg, .png o .gif). Ejemplo: [http://www.urltest.com/image/imagen1.jpg](http://www.urltest.com/image/imagen1.jpg)
* **NomeImagem**: Este campo es obligatorio. No está permitido usar caracteres especiales, tildes o espacios en blanco. El nombre es lo que viene luego de la última / en la URL de la imagen, incluyendo su extensión. Es decir que, teniendo en cuenta el ejemplo anterior, el nombre sería imagen1.jpg
* **TextoImagem**: En este campo irá el texto relacionado a la imagen. No está permitido usar caracteres especiales ni tildes, ni es obligatorio.
* **Label**: Acá irá la etiqueta del producto en caso de requerirse. No está permitido usar caracteres especiales ni tildes, ni es obligatorio.
* **IdSku**: Este campo es obligatorio. El ID informado debe corresponderse con el ID de un SKU ya existente en el Catálogo.
* **CodigoreferenciaSku**: Este campo es obligatorio. El código de referencia del SKU es el código que consta en el registro del SKU en el campo Código de referencia.

Una vez terminados con los registros necesarios, guardamos la planilla y la subimos al gestor de exportación/importación masiva.

## Requerimientos de imágenes de producto

Medidas: 708x1060 px

Formato: JPG

Nombre: El nombre del archivo no debe contener espacios o caracteres especiales, tampoco ya que se considera un caracter especial.

## Buenas prácticas sugeridas por VTEX

* El nombre de los archivos de las imágenes no debe contener espacios. Si es necesario, se recomienda que los caracteres se separen por guión.
* No utilizar caracteres especiales en los nombres de las imágenes. Seguir un patrón alfanumérico.
* La extensión recomendada para los archivos es .JPG (y no .JPEG).
* Recomendamos las portadas tengan fondo blanco.
* Las imágenes no deben tener menos de 600 píxeles.
* Las imágenes pueden tener hasta 3200 x 3200 píxeles.
* Para que el zoom de las imágenes funcione correctamente, se recomienda que las imágenes tengan como mínimo 1000 píxeles. Si posible, se puede obtener un resultado aún mejor en el zoom con imágenes de 1500 a 2000 píxeles.
* Recomendamos que las imágenes no tengan más de 300 kb de peso.
* No recomendamos estirar las imágenes para no afectar su calidad.
