# 👕 Categorías

## Descripción

Antes de la creación de productos, es necesario tener registrado un árbol de categorías en donde ubicar dichos productos. Para ello, se debe ir al módulo **Catálogo -> Categorías.**

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-05 a la(s) 5.45.17 p. m..png" alt=""><figcaption></figcaption></figure>

Para poder crear un correcto árbol de categorías, es importante considerar hacer como máximo tres niveles, acorde a las recomendaciones de VTEX. Si bien no es obligatorio, es lo recomendado. Estos niveles corresponderán a:

* Departamento (Nivel 1)
  * Categoría (Nivel 2)
    * Subcategoría (Nivel 3)

Siguiendo estas consideraciones, el orden del árbol debería quedar, por ejemplo, de esta forma:

* Departamento
* Departamento
  * Categoría
* Departamento
  * Categoría
  * Categoría
    * Subcategoría
    * Subcategoría
  * Categoría
* Departamento

Un buen ejemplo sería el siguiente:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-05 a la(s) 5.50.44 p. m..png" alt="" width="178"><figcaption></figcaption></figure>

{% hint style="info" %}
Los números que aparecen antes de cada categoría son el ID de categoría. Estos se asignan por VTEX de forma automática, por lo que no se debe agregarlos al nombre de la categoría.

**Por ejemplo:** El departamento Accesorios tiene el ID 31.  El nombre del Departamento es **"Accesorios"**. El número 31 es un indicador de VTEX, no forma parte del nombre de categoría.

![](<../.gitbook/assets/Captura de pantalla 2024-04-05 a la(s) 5.51.04 p. m..png>)
{% endhint %}

## Crear categoría

En el caso que se quiera crear un nuevo Departamento, es necesario hacer click sobre la categoría llamada **"Categorías"**. Esa es la categoría raíz o categoría madre. Si por otro lado se quiere crear una categoría o subcategoría, se debe hacer click en el departamento o en la categoría en que la nueva categoría vaya a estar anidada.

Hecho eso, se mostrará una opción a la derecha. Se debe clickear en el desplegable **"Acciones"** y dar click a **"Incluir".**

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-06 a la(s) 10.08.46 p. m..png" alt=""><figcaption></figcaption></figure>

En la ventana de creación de categoría aparecerán los siguientes campos:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-06 a la(s) 10.25.55 p. m..png" alt=""><figcaption></figcaption></figure>

* **Nombre:** Será el nombre del departamento/categoría/subcategoría. Es visible y se verá en la URL de la categoría y en el título de la PLP.
* **Palabras similares:** Sirve para indicar a VTEX palabras similares o sinónimos de la categoría.
* **Título de página de la categoría:** Es el título de la pestaña, útil para SEO.
* **Descripción de categoría:** Descripción de la categoría para motores de búsqueda. Se recomienda no más de 150 caracteres, útil para SEO.
* **Código de AdWords y Lomadee**: Útil para poner, en caso de tener, código de AdWords o Lomadee que correspondan a esa categoría.
* **Categoría principal:** Es el departamento o la categoría en la que estará anidada la nueva categoría. Si se hizo sobre "Categorías" para crear un nuevo departamento, estará en blanco.
* **Categoría global VTEX:** Es la categoría del árbol de VTEX que más se parezca a la categoría nueva. Esto es porque VTEX utilizará esta categoría global VTEX para match de información con Google Shopping, Marketplaces y demás integraciones.
* **Menú:** Normalmente va destildado ya que el menú y menú lateral se modifican directamente desde Site Editor.
* **Activo:** Debe estar tildado para que la categoría sea usable y esté activa.
* **Menú con link activo:** Debe estar tildado para que la categoría tenga su página activa.
* **Filtro de marca:** Normalmente va destildado, ya que hay una única marca en cada sitio.
* **Puntuación:** En caso de utilizar sistema de Score para ordenar la sábana, se puede utilizar este campo. Actualmente no está en uso.
* **Modo de visualización de productos:** Normalmente será "Sigue la definición de la especificación de SKU".

Una vez completada toda la información necesaria, se le debe dar click a Guardar.

## Editar categoría

En caso que se desee editar una categoría ya creada, se le debe dar click a la categoría, y en el desplegable de la derecha se debe hacer click en **"Acciones"** y **"Editar"**.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-06 a la(s) 10.27.13 p. m..png" alt=""><figcaption></figcaption></figure>

Los campos a editar serán los mismos que al crear una categoría.

## **Consideraciones**

{% hint style="danger" %}
* No se recomienda bajo ningún concepto hacer cambios en la categoría raíz (como por ejemplo, agregar campos).
* No se debe utilizar ninguna de las siguientes palabras reservadas para el nombre de la categoría:
  * a
  * meta
  * api
  * admin
* No es posible eliminar categorías desde el Admin. Para evitar inconvenientes, es viable cambiar el nombre a **"no usar"** y destildar la opción de **"Activo"**. Asegurarse también que no haya ningún producto catalogado bajo esa categoría.
{% endhint %}

{% hint style="warning" %}
Algunas herramientas como **Intelligent Search** no se guían por el ID de categoría, sino por el nombre de la misma. Es recomendable asignar nombres claros para evitar confusiones.
{% endhint %}
