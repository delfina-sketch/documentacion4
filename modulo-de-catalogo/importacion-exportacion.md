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

# 👕 Importación/exportación

El módulo de Importación/exportación es muy útil para poder realizar de forma masiva tareas diarias relacionadas al catálogo. Saber dominarlo nos será muy beneficioso para simplificar y acortar tiempos de trabajo.

{% hint style="info" %}
Para no romper el exportador, nunca es recomendable exportar más de 10.000 líneas. El límite de excel de filas es 65.000, por lo que exportar más registros que esos directamente hará que no nos exporte toda la información requerida.
{% endhint %}

## Todos los productos

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.26.13 p. m..png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Para referencias sobre la edición de la planilla, remitirse a [**Carga masiva** ](carga-de-productos-y-skus.md#carga-masiva)dentro de [**Carga de producto y SKU**.](carga-de-productos-y-skus.md)
{% endhint %}

Dentro de la pestaña, tendremos en primer lugar la posibilidad de **filtrar los resultados**: esto es importante porque de esta forma podemos mantenernos dentro de los límites de líneas ideales para no romper el exportador. Los filtros funcionan exactamente igual que en la página de Productos.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.28.04 p. m..png" alt=""><figcaption></figcaption></figure>

También, si queremos reducir el tiempo de exportación porque requerimos unos pocos datos, podemos elegir los campos a exportar. Menos campos significarán menos tiempo de exportación:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.29.23 p. m..png" alt=""><figcaption></figcaption></figure>

Y por último, estará el botón de Exportación/Importación.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.31.35 p. m..png" alt=""><figcaption></figcaption></figure>

En ambos casos, para exportar o para importar, tendremos que proporcionar nuestro correo para recibir la información del resumen de la importación o exportación a nuestro correo.

De todas formas, debajo de ello tenemos la lista de productos que estamos viendo y que se exportará. Es una fila por SKU, por lo que como podemos ver, actualmente al exportar estaríamos exportando 4225 filas:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.34.01 p. m..png" alt=""><figcaption></figcaption></figure>

No es un número exagerado, podríamos exportarlo sin problemas. Pero si quisiéramos, y de repente sólo necesitáramos exportar la categoría accesorios, directamente podríamos filtrar y el número de SKUs se reduciría drásticamente:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.36.50 p. m..png" alt=""><figcaption></figcaption></figure>

Seleccionamos en accesorios

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.38.27 p. m..png" alt=""><figcaption></figcaption></figure>

Y en vez de requerir una exportación de casi 4.225 filas, pasamos a una exportación de 518 filas.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.39.48 p. m..png" alt=""><figcaption></figcaption></figure>

En el caso de importación, tenemos la posibilidad de descargar la planilla modelo. Una vez con el archivo correcto, lo seleccionamos y le damos a importar.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.46.24 p. m..png" alt=""><figcaption></figcaption></figure>

## Especificaciones del producto y especificaciones del sku

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.48.21 p. m..png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Para referencias sobre la edición de la planilla, remitirse a [**Carga masiva**](especificaciones.md#carga-masiva) dentro de [**Especificaciones**](especificaciones.md).
{% endhint %}

Dentro de Especificaciones de Producto y Especificaciones de SKU, podremos descargar la planilla de especificaciones del departamento, categoría o subcategoría que deseemos.

Por ejemplo, para descargar la planilla de Collection, vamos y podemos exportar seleccionando "Exportar" al hacer clic derecho:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.51.31 p. m..png" alt=""><figcaption></figcaption></figure>

Una vez lista la planilla, más abajo seleccionamos el archivo y lo subimos con **"**&#x49;mporta&#x72;**"**:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.55.09 p. m..png" alt=""><figcaption></figcaption></figure>

## Importar imágenes

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.57.54 p. m..png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Para referencias sobre la edición de la planilla, remitirse a [**Carga masiva** ](carga-de-imagenes.md#carga-masiva)dentro de [**Carga de imágenes.**](carga-de-imagenes.md)
{% endhint %}

Principalmente en esta pestaña podremos descargar la planilla de ejemplo y cargar el archivo:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.59.51 p. m..png" alt=""><figcaption></figcaption></figure>

## Exportar imágenes

En este módulo se podrá exportar la lista de imágenes actual de todos los productos.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-05 a la(s) 12.01.32 a. m..png" alt=""><figcaption></figcaption></figure>

Si bien no hay posibilidad de discriminar por categoría, sí se puede filtrar por algunos campos para no tener una exportación tan pesada en caso de superar los 10.000 registros:

<figure><img src="https://lh7-us.googleusercontent.com/X8iphx3jSZRiPoybU_B-k-JAqg8C595bLFBRBo9MNx4Nd9UPLK3MwAo5aoq7Q7wsV4SzTbrkjC98_-_3aap2EtGQ7IICTTKUKpzY_G0iTXEqeetANwG_LUfkNNrSjm1Ztf-lJyKpGWfoJAYbPxAk9l0" alt=""><figcaption></figcaption></figure>

Una vez filtrado de ser necesario, simplemente le damos a exportar a Excel:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-05 a la(s) 12.03.36 a. m..png" alt=""><figcaption></figcaption></figure>

## Exportación de comentarios de productos

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-05 a la(s) 12.06.04 a. m..png" alt=""><figcaption></figcaption></figure>

Si bien no suele utilizarse, también se podrían exportar los comentarios de productos. \
Al igual que especificaciones, funciona haciendo click derecho en la categoría objetivo y clickeando **"**&#x45;xporta&#x72;**".**

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-05 a la(s) 12.06.43 a. m..png" alt=""><figcaption></figcaption></figure>
