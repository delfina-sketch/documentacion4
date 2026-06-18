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

# 👕 Especificaciones

## Descripción

Las especificaciones son campos útiles que nos permiten establecer distintos campos de información para un departamento, categoría o subcategoría a fin de sumar información o asignar características particulares propias de ciertos grupos de productos.

Por ejemplo, si quisiéramos establecer un filtro que discrimine productos según su material, VTEX no tiene de forma nativa un campo en el SKU o Producto que nos permita asignar la característica material, bien, para ello se puede crear una especificación llamada Material, a la que nosotros previamente podremos cargar una lista determinada de materiales, y que a la hora de catalogar simplemente se seleccione el o los materiales que correspondan.

De misma forma se hace con los campos color y talle, ya que son especificaciones de SKU y que se deben configurar en cada SKU en particular a la hora de crearlos.

## **Tipos de especificación**

Existen dos tipos de especificación: de producto y de SKU. Dependiendo de lo que necesitemos, es el tipo de especificación que debemos crear a la categoría.

Si se trata, por ejemplo, de una especificación llamada "material", casi siempre el material es común en todos los SKUs de un mismo producto, por lo que podría ir cargado como una especificación de producto.

Si por el otro lado, se trata de una especificación como la que hablamos anteriormente que sea color o talle, al ser distinto entre SKUs de un mismo producto, nos convendrá configurarlas como especificación de SKU.

## **Configuración de especificación**

Antes de la carga, debemos realizar la configuración de las especificaciones. La configuración se puede hacer únicamente a través del administrador, por lo que debemos dirigirnos a Categorías.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 10.20.24 p. m..png" alt=""><figcaption></figcaption></figure>

Una vez ahí, debemos determinar en qué nivel del árbol nos conviene crear la especificación, y para ello hay que hacer un análisis de la especificación que crearemos.

Por ejemplo: Si la especificación que deseamos crear es específica de medias, nos conviene crearla directamente en Medias. Si la creamos en "Invisible", no la tendremos disponible en productos catalogados en "Media caña" o en "soquete". Si por el otro lado la creamos en "Accesorios", tendremos en "Ojotas" y en "Pantuflas" esa misma especificación que sólo era necesaria para "Medias".

Por ello, siempre es recomendado crear la especificación en la categoría justa a la que alcanza la especificación.

{% hint style="danger" %}
No se recomienda jamás crear especificaciones sobre la categoría raíz (llamada "Categorías", la que engloba a todos los departamentos categorías y subcategorías) ya que ello implica algunos malos funcionamientos propios de VTEX.

En el caso, por ejemplo, de la especificación "Color" que es común a todo el sitio, es recomendable crear una especificación por cada departamento. No es recomendable nunca crear una especificación sobre la raíz.
{% endhint %}

Para crear una especificación de producto en medias por ejemplo, hacemos click en "AW24" y luego en el desplegable de la derecha seleccionamos "Campo (producto)". En el caso que lo que se desee sea crear una especificación de SKU, deberíamos clickear sobre "Campo (SKU)".

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 10.30.36 p. m..png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Si al querer ingresar a las especificaciones te devuelve a la vista de categorías, es normal, es un mal funcionamiento de VTEX. Simplemente vuelve a intentar.
{% endhint %}

En el caso de tener especificaciones ya creadas en ese orden, podremos editarlas y verlas en el panel. Si lo que queremos es crear una nueva, simplemente debemos hacer click en "Nuevo campo".

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 10.32.22 p. m..png" alt=""><figcaption></figcaption></figure>

En la próxima vista tendremos toda la información respecto de la configuración de la especificación de producto.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 10.34.52 p. m..png" alt=""><figcaption></figcaption></figure>

* **Nombre:** Será el nombre por el que identificaremos a la especificación.
* **Texto:** Es un texto que nos permite profundizar un poco más sobre qué es la especificación.
*   **Tipo:** Esta es la configuración más importante, ya que nos permitirá elegir el tipo de especificación que estamos por configurar.

    * Texto
    * Texto grande
    * Número
    * Combo
    * Radio
    * Checkbox
    * Texto indexado
    * Texto grande indexado

    Normalmente, los tipos que se recomiendan son combo y checkbox. **Combo** es muy útil para elegir talle o tamaño. **Checkbox** sirve para especificaciones con posibles valores múltiples, como material, de esta forma, se estandarizan los posibles valores de esa especificación y simplemente se debe chequear o deschequear la o las casillas de esos valores en el producto para indicar que pertenece.

{% hint style="info" %}
Cabe mencionar que no hay una regla general para el tipo de campo que corresponde a cada especificación. Siempre dependerá de lo que necesitemos y queramos hacer, por lo que ante la duda a la hora de configurar una nueva especificación, siempre es recomendable consultar la documentación para estar seguros de qué tipo de campo se adapta más a la especificación.
{% endhint %}

* **Grupo:** Las especificaciones tienen un grupo, por defecto caerá en **"Especificaciones-\[nombre categoría]"**, no es necesario modificarlo.
* **Filtro:** En caso que se desee activar para filtro dentro de la navegación del sitio, chequearlo.
* **Obligatorio:** Si lo marcamos, todos los productos o SKUs que no tengan completa la especificación quedarán desactivados hasta que sean completados, y aquellos que vayan a crearse en un futuro vía admin no permitirá avanzar hasta ser completada la especificación. Si se crean vía masivo, tampoco quedarán activos hasta que se completen las especificaciones correctas.
* **Muestra especificación:** Si está tildado, el campo se mostrará en la pantalla del producto o SKU en el área de especificación.
* **Link en el menú superior/lateral:** Normalmente no se utiliza y van destildados.
* **Activo:** Define si la especificación está activa o inactiva. Si la queremos utilizar, debemos tildarla. De todas formas, si elegimos tipos de campo como **"Checkbox"** o **"Combo"**, al no tener valores cargados, la especificación se apagará automáticamente hasta que tenga al menos 1 valor cargado.

Una vez cargada la especificación, si es del tipo **"Combo"** o **"Checkbox"** debemos cargar los valores que permitiremos sean elegidos a la hora de modificar especificaciones.

Para ello, vamos a la ventana de los campos de la categoría y en la flecha hacemos click en "Valores":

<figure><img src="https://lh7-us.googleusercontent.com/6zhJkxr6FurGQuq1KuU6rG0kaYBdwwcf3h9sbmR32-MLforVHjb4l9X6mPxi8gQhv_1YdmB1JlNXnvCC_-l8Vj2Pv4zTa_vRy4s4sxpFnyzocrg3hcikzeVtcYAyIQoEo3xIgtM88etKqHhMSsQ2prk" alt=""><figcaption></figcaption></figure>

Allí nos aparecerán los valores ya cargados, o ninguno si no hay ninguno cargado.\
Para cargar nuevos valores, hacemos click en "**Nuevo valor**"

<figure><img src="https://lh7-us.googleusercontent.com/KVvnQ_7TaRl0F2UChh4KJnFKljvmI9yDf7-7L6kD_Rbn_Wx3OaaGUqD_5EtacEUfarH1zjJSHkb84PlOVJWJzKMccr8PigXbYq0GbdNO83RIzqeWuX4JYsvETltCWXBn_qx4qIeXKbsRJKMMsCHXrn4" alt=""><figcaption></figcaption></figure>

Cada fila que agreguemos será un valor nuevo, por lo que si necesitamos agregar, por ejemplo, diez colores distintos, no hace falta que lo hagamos uno a uno. Agregamos cada color separando por línea de esta forma:

<figure><img src="https://lh7-us.googleusercontent.com/Imza4_ygCeK99sXVvY4bxjlLLhgZfZpC0XHCPTP3zmYTjbrq90wPHaMYWX-n5K8Sd7CbDgqt9gTZ4I5e9ImRFug1UoIVZOeUjOO13C5F7dL9ui7eyQvrvcHkRywd30amMj_inpI7JdDWoz-85vZ6rU4" alt=""><figcaption></figcaption></figure>

De esta forma, se crearán esos 10 nuevos valores de forma distinta. Así, ya podremos activar la especificación y empezar a configurarla en cada producto o SKU particular.

## **Carga de especificación en producto/SKU**

### **Carga manual**

Para cargar de forma manual una especificación, debemos dirigirnos al producto o SKU que queremos cargar desde catálogo - Todos los productos, por ejemplo, el SKU ID 91.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 10.47.09 p. m..png" alt=""><figcaption></figcaption></figure>

Allí nos dirigimos a la pestaña "**Especificaciones**"

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 10.49.27 p. m..png" alt=""><figcaption></figcaption></figure>

En este caso, al ser ambas especificaciones del tipo **Combo**, nos aparecerá como de una única opción de selección. También, al ser obligatoria tendrá un asterisco y no nos dejará guardar el SKU hasta que ambas estén completas.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 10.52.04 p. m..png" alt=""><figcaption></figcaption></figure>

Si fueran del tipo checkbox, las especificaciones se verían de esta forma:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 10.55.58 p. m..png" alt="" width="375"><figcaption></figcaption></figure>

Una vez terminada la configuración de las especificaciones en el producto o SKU, simplemente se debe guardar y estará listo.

### Carga masiva

{% hint style="info" %}
Para más información sobre todas las cargas masivas, es recomendable revisar primero el documento [Importación/exportación](importacion-exportacion.md)
{% endhint %}

La carga masiva se hace directamente desde el módulo de Importación/Exportación. Para ello habrá dos pestañas, según lo que tengamos que modificar, que serán Especificaciones de Producto o Especificaciones de SKU:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 10.58.41 p. m..png" alt=""><figcaption></figcaption></figure>

En este caso lo haremos con las especificaciones del SKU ya que no hay cargadas especificaciones de producto, pero el modo de trabajo es exactamente el mismo, lo único que cambiará son los campos que nos salgan para completar.

Suponiendo que necesitamos realizar la asignación en Final Sale.&#x20;

Simplemente damos click derecho sobre ese departamento, y le damos a "**Exportar**".

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.01.15 p. m..png" alt=""><figcaption></figcaption></figure>

Una vez terminada la exportación, se enviará por correo electrónico y nos mostrará el siguiente mensaje:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.04.48 p. m..png" alt=""><figcaption></figcaption></figure>

La descargamos y la abrimos, y tendremos la siguiente visión:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-04 a la(s) 11.08.46 p. m..png" alt=""><figcaption></figcaption></figure>

* **Columna A, IDSKU**: Es el ID del SKU. Si notamos, están todos 2 veces, ya que es una línea por cada especificación que tengamos. Como tenemos 2 (talle y color) cada SKU saldrá dos veces, uno para talle y otro para color.
* **Columna B, NombreSKU:** Por si no estamos familiarizados con el IdSKU o el Código de referencia, también tendremos el nombre del SKU.
* **Columna D NombreCampo:** Nos indicará la especificación de que trata la línea, como son dos, hay dos por cada SKU, talle y color, y se van repitiendo por cada SKU en la categoría.
* **Columna G, NombreValorCampo:** Es la lista de todos los valores válidos para la especificación, ya que se trata de campos del tipo Combo, por lo que ya están predefinidas.
* **Columna I, ValorEspecificación:** Es donde debemos ingresar el valor de la especificación. Si no va nada, deben quedar las tres líneas "---"
* **Columna J, CodigoReferenciaSKU:** Sirve para tener de referencia el código del SKU, más allá del nombre y el ID.

Entonces si quisiéramos asignar colores y talles, lo haríamos en la columna I teniendo en cuenta los valores de la columna G.

En resumen, la única columna que debemos modificar en esta planilla será la columna I.

Una vez terminada la planilla, la guardamos y la subimos al importador.

{% hint style="info" %}
Para más información sobre todas las cargas masivas, es recomendable revisar primero el documento [**Importación/exportación.**](importacion-exportacion.md)<br>
{% endhint %}
