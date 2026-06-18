# 👕 Sinónimos

## Descripción

La funcionalidad sinónimos de **Intelligent Search** permite registrar palabras con significados similares a un término de búsqueda específico, lo que aumenta las posibilidades de éxito de la búsqueda. Esta herramienta permite crear reglas de relación entre las palabras buscadas y las palabras contenidas en el registro de productos.

Por ejemplo: en una tienda, los productos se registran con el nombre **televisión**, pero es común que los clientes busquen **tv**. Puedes configurar un sinónimo para determinar que cuando se busque el término **tv**, también se muestren los resultados de televisión.

### Cómo funciona <a href="#como-funciona" id="como-funciona"></a>

Durante la búsqueda, Intelligent Search recibe el término buscado por el cliente y verifica las reglas de sinónimos registradas. Si se encuentra un sinónimo que coincida con el término, Intelligent Search incluye en los resultados de la búsqueda los ítems que coinciden con el sinónimo.

De este modo, aunque el cliente no busque la palabra registrada en el producto, podrá obtener resultados relevantes, lo que aumenta las posibilidades de éxito de la búsqueda y reduce la posibilidad de obtener resultados vacíos.

El uso de sinónimos también complementa los informes de búsquedas sin resultados. A partir de este análisis, el retailer puede identificar las búsquedas que no arrojaron resultados y determinar qué términos necesitan sinónimos registrados.

### Tipos de sinónimos <a href="#tipos-de-sinonimos" id="tipos-de-sinonimos"></a>

Pueden crearse dos tipos de sinónimos: unidireccional y bidireccional. Consulta a continuación las características de cada uno:

| Tipo           | Descripción                                                                                                                                                                                                                                                       | Ejemplo                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| -------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Unidireccional | <p>Dos o más palabras tienen significados similares, pero no se consideran equivalentes en todos los contextos.<br>Esta configuración se elige estratégicamente para que la coincidencia funcione en una dirección específica.</p>                                | <p><mark style="background-color:purple;">smartphone → iphone</mark><br>Al buscar el término "smartphone", los resultados incluirán productos etiquetados como "iphone". Sin embargo, al buscar "iphone" no se mostrarán resultados de "smartphone".</p>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| Bidireccional  | <p>Dos o más palabras tienen sentidos y significados equivalentes, lo que permite que la correspondencia funcione en ambas direcciones.<br>Esta configuración facilita la búsqueda de productos que pueden tener nombres distintos según el país o la región.</p> | <p><mark style="background-color:purple;">diet ⇄ cero azúcar ⇄ sin azúcar</mark><br>Al buscar productos "diet" se incluirán productos definidos como "cero azúcar" y "sin azúcar". Del mismo modo, al buscar "cero azúcar", los resultados incluirán productos "diet" y "sin azúcar". Los resultados de "sin azúcar" también incluirán productos "cero azúcar" y "diet".<br><br><mark style="background-color:purple;">pomelo ⇄ toronja ⇄ pamplemusa</mark><br>En distintos países en los que se habla español, los términos "pomelo", "toronja" y "pamplemusa" se refieren a la misma fruta. Con sinónimos bidireccionales para cada término, no será necesario repetir cada palabra en la descripción del producto, ya que se mostrarán todos los resultados.</p> |

Una vez registrado o modificado un sinónimo, puede tardar hasta dos horas en reflejarse en la tienda.

### Buenas prácticas <a href="#buenas-practicas" id="buenas-practicas"></a>

No utilices las palabras sustitutas para optimizar las búsquedas de productos y SKU en el Catálogo con Intelligent Search. Usa únicamente la funcionalidad de sinónimos, ya que permite una gestión más escalable de términos por producto.

#### Clasificación de los resultados <a href="#clasificacion-de-los-resultados" id="clasificacion-de-los-resultados"></a>

Al crear un sinónimo bidireccional, no hay diferenciación entre los dos términos en la clasificación de los resultados de búsqueda. \
Por ejemplo, si existe un sinónimo bidireccional como <mark style="background-color:purple;">tempra ⇄ paracetamol</mark>, al buscar tempra, los resultados de este medicamento no necesariamente aparecerán antes que los resultados de paracetamol. Para determinar la estrategia de clasificación, es necesario utilizar una **regla de merchandising**.

#### Palabras agregadas individualmente <a href="#palabras-agregadas-individualmente" id="palabras-agregadas-individualmente"></a>

Cuando se crea un sinónimo con más de una palabra, ambos términos deben añadirse individualmente al producto. Por ejemplo, si hay un sinónimo <mark style="background-color:purple;">zapatillas running ⇄ tenis running</mark> y alguien busca el término running, los resultados de tenis running y de zapatillas running se incluirán en los resultados de la búsqueda.

#### Recursividad <a href="#recursividad" id="recursividad"></a>

Los sinónimos son recursivos, es decir, los resultados son acumulativos. Por ejemplo, al crear un sinónimo <mark style="background-color:purple;">tempra ⇄ paracetamol</mark> y otro sinónimo <mark style="background-color:purple;">paracetamol ⇄ dolor de cabeza</mark>, en una búsqueda de tempra, considera que también se mostrarán los resultados de dolor de cabeza.

#### Autocorrección en Intelligent Search <a href="#autocorreccion-en-intelligent-search" id="autocorreccion-en-intelligent-search"></a>

Los sinónimos no deben utilizarse para resolver errores ortográficos, variaciones de singular y plural, pronombres, artículos o preposiciones en los términos de búsqueda. En estos casos, Intelligent Search es capaz de interpretar, aprender y corregir automáticamente a través de Autocorrección.

Algunos ejemplos de configuración de sinónimos:



| Sinónimos                                                                        | Tipo           | Comentario                                                                                             |
| -------------------------------------------------------------------------------- | -------------- | ------------------------------------------------------------------------------------------------------ |
| <mark style="background-color:purple;">loción ⇄ crema</mark>                     | Bidireccional  | ✔️ Configuración adecuada. Cuando alguien busca crema, se añaden los resultados de loción y viceversa. |
| <mark style="background-color:purple;">pantalón → jeans</mark>                   | Unidireccional | ✔️ Configuración adecuada. Cuando alguien busca pantalón, se añaden los resultados de jeans.           |
| <mark style="background-color:purple;">sueter → sweater</mark>                   | Unidireccional | ❌ Configuración redundante. Intelligent Search corrige automáticamente casos como este.                |
| <mark style="background-color:purple;">pantalón ⇄ pantalones</mark>              | Bidireccional  | ❌ Configuración redundante. Intelligent Search corrige automáticamente casos como este.                |
| <mark style="background-color:purple;">pantalón jeans ⇄ pantalón de jeans</mark> | Bidireccional  | ❌ Configuración redundante. Intelligent Search corrige automáticamente casos como este.                |

La funcionalidad **Sinónimos** genera recomendaciones de términos para registrar sinónimos, además de la configuración manual.&#x20;

## Crear sinónimos

{% hint style="info" %}
Recomendamos usar **Sinónimos** en lugar de **Palabras sustitutas** para asociar palabras con productos, ya que los sinónimos permiten gestionar los términos por producto de una forma más escalable.&#x20;
{% endhint %}

Hay dos formas de configurar sinónimos en VTEX Admin: **individualmente** o **importando una hoja de cálculo en formato CSV.** Si necesita registrar sinónimos en bloque, le recomendamos que utilice la hoja de cálculo.&#x20;

<mark style="background-color:purple;">La configuración de sinónimos funciona de forma recursiva. Esto significa que cuando agrega un segundo sinónimo a uno existente, también se convertirá en sinónimo del primero.</mark>

### Crear sinónimos individualmente <a href="#crear-sinonimos-individualmente" id="crear-sinonimos-individualmente"></a>

#### Pasos

1. En el Admin VTEX, ingresa a **Storefront**, o escribe **Storefront** en la barra de búsqueda en la parte superior de la página.
2. En **Intelligent Search**, haga clic en **Sinónimos**.
3. Haga clic en Crear sinónimo.
4. Rellene los campos referentes al sinónimo:
   * **Tipo:** define el tipo de sinónimo.&#x20;
   * **Términos:** palabras o expresiones que se definirán como sinónimos. Es necesario pulsar **Enter** después de cada término para insertar otro término.
   * **Idiomas:** idiomas en los que se aplicará el sinónimo. **Campo solo disponible para tiendas que utilizan configuración multidioma (beta)**.
   * **Status:** define si el sinónimo estará activo o inactivo.
5. Para terminar, haga clic en Publicar.

La alteración puede tardar hasta dos horas en aplicarse.

### Importar CSV <a href="#importar-csv" id="importar-csv"></a>

Si existen muchos sinónimos para registrar, puedes hacer un archivo .csv y luego importarlo en el Admin.

#### Pasos

1. Cree un archivo CSV en el formato indicado en Plantilla de sinónimos.
2. En el Admin VTEX, acceda a **Storefront**, o escribe **Storefront** en la barra de búsqueda en la parte superior de la página.
3. En **Intelligent Search**, haga clic en **Sinónimos**.
4. Haga clic en  Importar.
5. Arrastre el archivo CSV al área delimitada o haga clic en selecciona un archivo para seleccionar el archivo de su dispositivo.
6. Haga clic en Importar.

### Plantilla de sinónimos <a href="#plantilla-de-sinonimos" id="plantilla-de-sinonimos"></a>

El fichero debe contener el siguiente formato, según los **tipos de sinónimos** elegidos:

*   **Unidireccional:** <mark style="background-color:purple;">{términos separados por una coma};{término equivalente};{status}</mark>

    **Ejemplos:**

    * <mark style="background-color:purple;">smartphone;iphone;true</mark>: al buscar por <mark style="background-color:purple;">smartphone</mark>, se mostrarán los resultados para <mark style="background-color:purple;">iphone</mark>. Sin embargo, al buscar por <mark style="background-color:purple;">iphone</mark>, los resultados para <mark style="background-color:purple;">smartphone</mark> no se mostrarán.
    * <mark style="background-color:purple;">tablet;ipad;true</mark>: al buscar por <mark style="background-color:purple;">tablet</mark>, se mostrarán los resultados para <mark style="background-color:purple;">ipad</mark>. Sin embargo, al buscar por <mark style="background-color:purple;">ipad</mark>, los resultados para <mark style="background-color:purple;">tablet</mark> no se mostrarán.
*   **Bidireccional:** <mark style="background-color:purple;">{términos separados por una coma};{status}</mark>

    **Ejemplos:**

    * <mark style="background-color:purple;">tv,televisión,televisor;true</mark>: al buscar por cualquiera de los términos, el producto que contenga uno de estos será devuelto.
    * <mark style="background-color:purple;">monitor,pantalla,display;true</mark>: al buscar por cualquiera de los términos, el producto que contenga uno de estos será devuelto.
