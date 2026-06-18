---
description: >-
  Para realizar la carga de productos existen dos formas, dependiendo del
  volumen y la disponibilidad/comodidad de los datos: manual o masivo.
---

# 👕 Carga de Productos y Skus

{% hint style="info" %}
Para más información sobre todas las cargas masivas, es recomendable revisar primero el documento de [Importación/Exportación](importacion-exportacion.md)
{% endhint %}

## Producto o SKU

Antes de comenzar, es importante dejar clara la diferencia entre producto y SKU.

**Producto** es como se le llama a un artículo que, por sus características, puede o no tener distintas variantes de sí mismo. Por ejemplo, Sweater Nova

**SKU** por el otro lado, es la variante específica de un producto, normalmente asociada al talle o al color. Retomando el ejemplo anterior, si Swater Nova es un producto, su variante Negra talle M sería el SKU.

Un producto podrá estar compuesto de uno o más SKUs, pero un SKU estará siempre ligado solo a un único producto. Tanto producto como SKU tienen sus códigos identificatorios propios, por lo que es importante diferenciar a la hora de hablar de los códigos asignados por VTEX (ID de Producto e ID de SKU) o de los asignados por nosotros mismos (Product Ref ID y SKU Ref ID).

Por esto mismo, el Short Best negro talle 00 podría tener hasta 4 códigos de identificación distintos (sin contar el EAN/UPC), como por ejemplo sería:

* Product ID: 6169
* SKU ID: 39607
* Código de referencia de producto: 39N1344041
* Código de referencia de SKU: 39N1344041\_02\_00

{% hint style="warning" %}
Confundir ID de Producto con ID de SKU podría traer inconvenientes a la hora de ejecutar tareas operativas diarias, como por ejemplo en la carga de promociones, de colecciones, cambio de precios, etcétera. Siempre es mejor asegurarse de con qué tipo de código se estará trabajando.
{% endhint %}

### Carga manual

Para realizar la carga manual de producto, nos debemos dirigir al administrador e ingresar a **Catálogo > Productos y SKUs**<br>

<figure><img src="../.gitbook/assets/1 (4).png" alt=""><figcaption></figcaption></figure>

Allí nos saldrá la lista de productos y SKUs cargados actualmente, y a la derecha tendremos el botón para **agregar nuevos productos**. Le hacemos click.

Al ingresar, podremos ingresar a través de dos pestañas: Producto y SKUs. Ingresamos por Producto y tendremos algunos campos a completar:<br>

<figure><img src="../.gitbook/assets/image (74).png" alt=""><figcaption></figcaption></figure>

*   **Información general:** Información básica que debes completar para empezar a vender tu producto.

    * **Nombre**: Obligatorio, el nombre con el que se mostrará nuestro producto, será visible para el usuario.
    * **Descripción del producto**: Campo para volcar la información general relacionada al producto.
    * D**escripción adicional:** Permite agregar una descripción corta para poder mostrarlo desde página de producto o listado de ser deseado. En caso de seleccionar esta opción se habilitará un campo adicional.

    <figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FUTqHEUCbbovExBofUd3P%252Fimage.png%3Falt%3Dmedia%26token%3Da4374211-1c88-4473-80c3-bcccdf0d79d8&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=e45b6dd4&#x26;sv=2" alt=""><figcaption></figcaption></figure>

    * **Marca:** Marca del producto, debe estar previamente registrada ya que debe elegirse de un desplegable.
    * **Categoría:** Categoría del propio árbol de categorías del producto, también debe estar previamente registrada.
    * **Políticas comerciales:** Política comercial a la que aplica. La misma debe estar previamente registrada.

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FN2EdnfLrtCcFSGSOBwmq%252Fimage.png%3Falt%3Dmedia%26token%3D52f15e5d-94bf-4046-8a96-b662a37d35b4&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=a59b0913&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* **SEO**: Estos campos influyen en el ranking del producto en motores de búsqueda como Google y Bing.
  * **Categoría global de VTEX**: Categoría del árbol predefinido de VTEX. Si bien no es obligatorio, es recomendable registrarla para una buena integración con Google Shopping o Marketplaces.
  * **URL**: Será el que dictamine la URL de nuestro producto, si bien no tiene un lugar llamativo, será visible para el usuario en cuanto a la vista del navegador.
  * **Título de página:** Texto de la pestaña del navegador (importante para SEO)
  *   **Metadescripción:** Muy breve descripción del producto, utilizado para SEO y para la información de los motores de búsqueda. La misma no debe excederse de 160 caracteres.



      <figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FPDbhlCS6r2RJZb6ci2JV%252Fimage.png%3Falt%3Dmedia%26token%3D5be8ca97-a8dc-429d-b87f-e0e120c0193e&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=ad6d0306&#x26;sv=2" alt=""><figcaption></figcaption></figure>
*   **Storefront:**

    * **Mostrar en el sitio web:** Activa o desactiva su visibilidad en la tienda.
    * **Mostrar producto agotado:** Habilita poder mostrar el producto aún cuando este esté agotado (esta característica también dependerá de nuestras configuraciones de tienda)
    * **Fecha de release:** Permite establecer una fecha de lanzamiento. También es útil para poder ordenar en el listado de productos por los más nuevos primero.
    * **Palabras sustitutas**: Sirve para que podamos indicar a VTEX qué palabras son reemplazo del nombre de nuestro producto en cuanto a búsquedas. De esta forma, ambos resultados darán con nuestro producto. Límite: 8000 caracteres.
    * **Categorías similares: P**ermite que un producto se muestre en más de una categoría, sin necesidad de duplicar la información del producto.
    * **Prioridad en el orden de búsqueda:** Permite **d**eterminar mayor o menor relevancia a los productos a la hora de hacer activaciones con la búsqueda inteligente. Mayor puntuación = mayor visibilidad.



    <figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FBeDancoE0M2TbwGqYkfp%252Fimage.png%3Falt%3Dmedia%26token%3Da0510001-e611-47d5-8bfe-79764132ed09&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=72106106&#x26;sv=2" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Las tiendas VTEX IO utilizan el buscador inteligente de VTEX el cual utiliza la creación de [sinónimos ](https://pow-ecommerce.gitbook.io/vtex-clientes/modulo-de-catalogo/sinonimos)para las búsquedas en lugar del campo **Palabras sustitutas.**
{% endhint %}

{% hint style="info" %}
**Consideraciones:**

Sustituir los espacios por guiones (-).

Máximo 50 caracteres.

No usar caracteres especiales como `! ñ . * ' ( ) ; : @ & = + $ , / ? % # [ ] |` o acentos como `´ ¨ ^ ~`.

Tampoco deben usarse las siguientes palabras reservadas:

* a
* meta
* api
* admin
{% endhint %}

* **Identificadores:**
  * **Código de referencia de producto**: Campo que nos permite agregar nuestro propio código de referencia interno.
  *   **Código fiscal**: Número de identificación fiscal, normalmente no se utiliza.



      <figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FHHlfIDLdtQ33BqgDZfEF%252Fimage.png%3Falt%3Dmedia%26token%3D839c3fba-9500-4f58-b31f-a2e2626f5acc&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=e19bfc51&#x26;sv=2" alt=""><figcaption></figcaption></figure>
*   **Especificaciones:** En caso de haber creado especificaciones de producto, se listarán en este apartado con sus opciones para seleccionar:



    <figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FGGwBDkQcm3KrNPUvAUAK%252Fimage.png%3Falt%3Dmedia%26token%3Dadec32e1-366d-4cc4-86be-bc4a5aac7816&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=f85b4fb6&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Ahora pasando a la pestaña de SKUs, encontraremos otros campos relevantes para la configuración de variantes. Desde el + podremos agregar la cantidad de SKUs que necesitemos:<br>

<figure><img src="../.gitbook/assets/image (75).png" alt=""><figcaption></figcaption></figure>

* **Nombre:** Será el nombre específico de esa variante. Ejemplo: Si el nombre de producto (autocompletado) es Short Best, el del SKU sería Negro - Talle 00.
* **Activo:** Nos dirá si la variante está o no activo.
*   **Especificaciones:** Desde esta pestaña, vamos a visualizar las especificaciones creadas para este SKU desde la categoría y podremos asignarle los valores correspondientes. Para este ejemplo, tenemos creadas las especificaciones de Talle y Color.<br>

    <figure><img src="../.gitbook/assets/image (76).png" alt=""><figcaption></figcaption></figure>
* **Contenido multimedia:** En este apartado podemos subir los archivos que serán relevantes para este SKU como:
  * **Imágenes:** Desde el icono de la imagen debemos subir los archivos.
  *   **Videos:** Desde el **+Agregar,** nos abrirá un modal para completar la URL.<br>

      <figure><img src="../.gitbook/assets/2 (5).png" alt=""><figcaption></figcaption></figure>

<figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FOxEZD2Clm4kFPVToXtHZ%252Fimage.png%3Falt%3Dmedia%26token%3D9f05a76b-20fc-4a52-8dd1-d9c489593801&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=5fe197b&#x26;sv=2" alt=""><figcaption></figcaption></figure>

* **Identificadores:**
  * **Código de referencia:** Es el código interno de nuestra organización para esa variante específica.
  * **EAN/UPC:** Sirve para completar con nuestro EAN/UPC en caso de ser necesario.
  *   **Código del Fabricante:** proporcionado por el fabricante para identificar su producto. Si algún producto tiene un código específico, este campo debe rellenarse.



      <figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FhR96V0fSj6AdM8l6Y1Pa%252Fimage.png%3Falt%3Dmedia%26token%3D06a88ef2-0892-4e83-93cf-cc795d79bfa3&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=45e4823e&#x26;sv=2" alt=""><figcaption></figcaption></figure>
* **Logística:**
  * **Modal (opcional):** En caso de haber activado este modal para logística, nos aparecerán las opciones que hayamos configurado. Más información: [Modal logística](https://help.vtex.com/es/tutorial/como-se-maneja-el-modal--tutorials_125)
  * **Peso, altura, anchura y longitud para envío**: Son obligatorias, la única considerada en inventario y envío es peso, pero es necesario ser consistente con los datos.
  * **Peso, altura, anchura y longitud real:** Sirve para indicar las características del producto una vez sacados del empaque del envío.
  * **Medidas de stock:** Esta información se utiliza para especificar la unidad de medida que se empleará para contabilizar el ítem en el stock.
    * **Unidad de Medida:** utilizada apenas en casos en los que es necesario convertir la unidad de medida para la venta. En este caso, un (de unidad).
    *   **Multiplicador de Unidad:** unidad numérica que multiplica la cantidad seleccionada del producto cuando se agrega al carrito. En este caso, 1.



        <figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252F7cj6VqOU0xX95gyJ16xf%252Fimage.png%3Falt%3Dmedia%26token%3D8ffc2867-f5db-41ca-ad8d-18105b17d600&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=b958d056&#x26;sv=2" alt=""><figcaption></figcaption></figure>
* **Estrategia comercial:**
  * **Condición Comercial:** utilizado para definir promociones/reglas de pago en cuotas específicas para SKUs. En este caso, siempre "Padräo".
  * **Valor de fidelidad:** Se utiliza para sistemas de fidelidad.
  * **Fecha de preventa:** Sirve para registrar el SKU como preventa (de estar configurado).
  *   **Generar crédito en tarjeta de regalo?:**



      <figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252FqyWweMCI5JonRiyO1LUQ%252Fimage.png%3Falt%3Dmedia%26token%3D05c3fd24-cbfb-4360-9d9e-af4924bb1fcb&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=f33aa51e&#x26;sv=2" alt=""><figcaption></figcaption></figure>
* **Personalizaciones:** Podremos agregar anexos o servicios adicionales para este producto.
* **Recomendaciones de cross-sell y up-sell:** Nos permite cargar otros productos como recomendaciones. Pueden ser de 4 tipos distintos:
  * **Similares (Productos Sustitutos):** tiene la función de mostrar en la página del producto otras opciones que son similares al mismo. Límite de 50.
  * **Accesorios:** añade nuevos SKUs al SKU que se está registrando. Si está registrando un vestido, coloca un cinturón como accesorio. Tiene como particularidad generar un checkbox donde el cliente puede hacer clic y ya hacer la compra de ambos ítems.
  * **Sugeridos:** sugiere nuevos SKUs al SKU que se está registrando. Si está registrando un vestido, coloca un cinturón como sugerencia. Sin embargo, el cliente no puede comprarlos juntos. Es necesario entrar en la página de cada uno de los ítems que quiere comprar.
  *   **Mostrar Junto:** muestra los SKUs de los productos sugeridos para su compra en conjunto.<br>

      <figure><img src="../.gitbook/assets/image (77).png" alt=""><figcaption></figcaption></figure>
*   **Atributos:** Nos permite crear y asignar un atributo determinado y aplicar a todos los SKUs de ese producto.



    <figure><img src="https://pow-ecommerce.gitbook.io/vtex-clientes/~gitbook/image?url=https%3A%2F%2F3709566463-files.gitbook.io%2F%7E%2Ffiles%2Fv0%2Fb%2Fgitbook-x-prod.appspot.com%2Fo%2Fspaces%252F72B6lE7Nn0jKtcyB10gI%252Fuploads%252F5ZbHMtaZlKpOYEOkXG8v%252Fimage.png%3Falt%3Dmedia%26token%3D7fd60985-1faa-449c-8d0f-0fd3b601be6c&#x26;width=768&#x26;dpr=4&#x26;quality=100&#x26;sign=3d73a740&#x26;sv=2" alt=""><figcaption></figcaption></figure>

Al ser un tema amplio, **especificaciones se abordará en la siguiente documentación:** [**Especificaciones**](https://pow-ecommerce.gitbook.io/vtex-clientes/modulo-de-catalogo/importacion-exportacion)

Una vez hayamos completado toda la información de nuestro SKU, le damos a "Guardar" y ¡listo! Ya con el SKU guardado, podremos repetir el proceso cuantas veces sea necesario para registrar cada una de las variantes posibles de ese producto.<br>

<figure><img src="../.gitbook/assets/3 (2).png" alt=""><figcaption></figcaption></figure>

### Carga masiva

En caso de tener que cargar muchos productos, o de tener los datos en otro sistema del que los podemos extraer y plasmar en cantidad y fácil, podremos optar para la carga masiva.

{% hint style="info" %}
Es recomendable revisar la documentación [Importación/Exportación](importacion-exportacion.md) antes de proseguir con la carga masiva.
{% endhint %}

Una vez teniendo la planilla de importación masiva, la abrimos y nos encontraremos con las siguientes columnas:

<figure><img src="../.gitbook/assets/Captura de Pantalla 2024-02-03 a la(s) 16.49.02.png" alt=""><figcaption></figcaption></figure>

Si bien hay un ejemplo, **no debemos olvidar eliminarlo** para evitar importarlo y crearlo por accidente.

* **\_IDSKU (Não alterável):** Si es un producto nuevo lo dejaremos vacío. Si es un producto que ya existe, no debemos modificarlo.
* **\_NomeSKU:** Es el nombre del SKU, es decir de la VARIANTE del producto, no del producto en sí. Es decir, al revés que la creación manual que primero nos pide nombre de producto.
* **\_AtivarSKUSePossível:** Activará el SKU en caso de cumplir todos los requisitos para estar activo. Únicos valores aceptados: `SÍ`o`NO` (nótese que el "SÍ" lleva tilde en la i)
* **\_SKUAtivo (Não alterável)**: este campo no permite ningún cambio, solo se utiliza para consulta.
* **\_EANSKU**: código único de identificación de SKU (código de barras). Acepta hasta 13 caracteres numéricos. Si se ha rellenado el campo CodigoReferenciaSKU, este campo deja de ser obligatorio.
* **\_Altura:** Altura calculada para flete, obligatorio.&#x20;
* **\_AlturaReal**: La altura real del producto.
* **\_Largura**: Ancho para flete, obligatorio.
* **\_LarguraReal**: Ancho real del producto.
* **\_Comprimento**: Largo para flete, obligatorio.
* **\_ComprimentoReal**: Largo real del producto.
* **\_Peso**: Peso para flete, obligatorio.
* **\_PesoReal**: Peso real del producto.
* **\_UnidadeMedida**: Siempre "un", ya que son unidades.
* **\_MultiplicadorUnidade**: Siempre 1, para indicar que se suma de a 1 unidad.
* **\_CodigoReferenciaSKU**: Código de referencia interno de nuestra empresa para ese SKU.
* **\_ValorFidelidade**: Valor para sistema de fidelidad, no es utilizado por el momento.
* **\_DataPrevisaoChegada**: en caso de preventa, introducir la fecha prevista de llegada del producto, en el formato dd/mm/aaaa.
* **\_CodigoFabricante**: código proporcionado por el fabricante para identificar su producto.
* **\_IDProduto**: Es el ID del producto ahora, al igual que en IdSKU, si está completo NO se modifica. Si es un producto nuevo, lo dejamos vacío.
* **\_NomeProduto**: Es el campo del nombre de producto, visible para el cliente.
* **\_BreveDescricaoProduto**: Sirve para insertar la descripción corta del producto.
* **\_ProdutoAtivo**: No es editable por planilla, debe dejarse vacío.
* **\_CodigoReferenciaProduto**: Código interno de nuestra organización para ese producto.
* **\_MostrarNoSite**: Activará el producto en caso de cumplir todos los requisitos para estar activo. Únicos valores aceptados: `SÍ`o`NO` (nótese que el "SÍ" lleva tilde en la i)
* **\_LinkTexto (Não alterável)**: Será el que dictamine la URL de nuestro producto, si bien no tiene un lugar llamativo, será visible para el usuario en cuanto a la vista del navegador.

{% hint style="danger" %}
**Consideraciones:**

Sustituir los espacios por guiones (-).

Máximo 50 caracteres.

No usar caracteres especiales como `! ñ . * ' ( ) ; : @ & = + $ , / ? % # [ ] |` o acentos como `´ ¨ ^ ~`.

Tampoco deben usarse las siguientes palabras reservadas:

* a
* meta
* api
* admin
{% endhint %}

* **\_DescricaoProduto**: Campo para volcar la información general relacionada al producto.&#x20;
* **\_DataLancamentoProduto**: Permite establecer una fecha de lanzamiento. También es útil para poder ordenar en el listado de productos por los más nuevos primero, formato _dd/mm/aaaa_.
* **\_PalavrasChave**: Sirve para que podamos indicar a VTEX qué palabras son reemplazo del nombre de nuestro producto en cuanto a búsquedas. De esta forma, ambos resultados darán con nuestro producto. Límite: 8000 caracteres.
* **\_TituloSite**: Texto de la pestaña del navegador (importante para SEO)
* **\_DescricaoMetaTag**: Muy breve descripción del producto, utilizado para SEO y para la información de los motores de búsqueda. Es recomendable no pasa los 150 caracteres.
* **\_IDFornecedor**: campo obsoleto. Este campo no es utilizado por el sistema y se recomienda mantenerlo vacío.
* **\_MostrarSemEstoque**: Habilita poder mostrar el producto aún cuando este esté agotado (esta característica también dependerá de nuestras configuraciones de tienda)
* **\_Kit (Não alterável)**: define si el SKU del producto en cuestión forma parte de un [Kit](https://help.vtex.com/es/tutorial/o-que-e-um-kit--5ov5s3eHM4AqAAgqWwoc28). No es posible editar este campo a través de la plantilla. Si se trata de un nuevo SKU, dejar el campo vacío.
* **\_IDDepartamento**: número único de identificación de la categoría de mayor nivel jerárquico del producto. No es posible editar este campo a través de la plantilla. Si se trata de un nuevo producto, dejar el campo vacío.
* **\_NomeDepartamento**: nombre relacionado con la categoría de mayor nivel jerárquico del producto. Si se trata de un nuevo producto, dejar el campo vacío.
* **\_IDCategoria**: ID de la categoría, el mismo podrá ser sacado del módulo "Categorías" revisando nuestro árbol de categoría.
* **\_NomeCategoria**: nombre relacionado con la categoría de menor nivel jerárquico del producto. No es posible editar este campo una vez rellenado.
* **\_IDMarca**: ID de la marca, el mismo podrá ser sacado del módulo "Marcas" revisando nuestras marcas registradas. Normalmente será 2000000.
* **\_Marca**: nombre dado a la marca del producto. No es posible editar este campo una vez rellenado.
* **\_PesoCubico**: campo obsoleto. Este campo no es utilizado por el sistema y se recomienda mantenerlo vacío.
* **\_CondicaoComercial**: El nombre de nuestra condición comercial, normalmente Padrão.
* **\_Lojas**: El ID de la política comercial, en este caso 1.
* **\_Acessorios**: Normalmente se deja vacío.
* **\_Similares**: Normalmente se deja vacío.
* **\_Sugestoes**: Normalmente se deja vacío.
* **\_ShowTogether**: Normalmente se deja vacío.
* **\_Anexos**: Normalmente se deja vacío.

Una vez terminado de editar, se debe subir el archivo y se crearán los nuevos productos.

{% hint style="info" %}
**Sugerencia:** Para evitar confusiones, es sugerible al momento de crear productos, descargarse una exportación de productos para poder seguir el mismo estilo y formato que los anteriores productos y SKUs. Además, así podrás asegurarte que no estarás ingresando información en una columna incorrecta.
{% endhint %}

## Consideraciones

Para que un SKU sea visible, requiere de las siguientes características:

* El producto y SKU deben estar registrados con todos sus elementos obligatorios.
* El SKU debe tener al menos una imagen cargada.
* Debe tener precio registrado.
* Debe tener stock cargado.
* Toda la configuración logística, desde el muelle, transportadora, almacén hasta el peso y tamaño debe estar correctamente cargada.
* Debe estar marcado como activar de ser posible.
* Marca y categoría deben ser válidas y estar activas.
* Debe estar asociado a una política comercial.
* Mostrar en el sitio web y Producto activo deben estar tildados como SÍ.
* Las especificaciones obligatorias deben ser cargadas.
