# Administrar estáticas

## Descripción

{% hint style="success" %}
Para llevar a cabo los procesos descritos en esta documentación, es necesario haber aprehendido en principio los procesos de la documentación [**Site editor**](../site-editor.md), ya que para administrar páginas estáticas, se da por sentado que se tienen al menos conocimientos básicos en el uso del site editor.
{% endhint %}

Hay dos pasos para administrar una página estática:

1. Crear una página nueva
2. Editar una página ya existente

De forma que, dependiendo de la tarea que requieras hacer, podrías empezar la documentación desde el inicio o tomarla directamente desde el punto 2.&#x20;

## Crear una página nueva&#x20;

Para crear una página nueva es necesario dirigirse, dentro del administrador, a la sección **Storefront -> Páginas**

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-11-11 a la(s) 4.03.51 p. m..png" alt=""><figcaption></figcaption></figure>

Dentro del módulo de páginas, se debe dar click al botón **Crear nueva**.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-11-11 a la(s) 4.04.50 p. m..png" alt=""><figcaption></figcaption></figure>

Ese botón habilitará la siguiente ventana:

<figure><img src="../../.gitbook/assets/Captura de Pantalla 2024-02-03 a la(s) 20.21.39.png" alt=""><figcaption></figcaption></figure>

* <mark style="background-color:blue;">**Titulo:**</mark>**&#x20;Será** el nombre de la página, que a su vez saldrá también en la pestaña del navegador, por lo que es necesario ser prolijos y conscientes en que el nombre ingresado en este campo, será visible también para el cliente.
* <mark style="background-color:blue;">**URL:**</mark> Es la URL que llevará a dicha página. Debe ingresarse la URL relativa, es decir, sin el dominio completo.
  * Ejemplo: Si se quiere crear una página llamada Preguntas frecuentes, se debe ingresar como url `/preguntas-frecuentes`
* **Requiere autenticación**: Por defecto dejarlo desactivado.
* **Descripción**: Permite agregar una descripción a la página que aparecerá en los resultados de los motores de búsqueda.
* **Palabras clave**: Palabras o temas que definen el contenido de la página, ayudando con el SEO.
* <mark style="background-color:blue;">**Templates:**</mark> Para páginas estáticas, debe elegirse **específicamente el template llamado XXXXX** Esta es la plantilla que le dará el estilo de **página estática** a esta nueva página.

Los campos <mark style="background-color:blue;">sombreados en azul</mark> **son obligatorios**.

Una vez completados todos los campos necesarios, hay que dar click en **Guardar** para que la página se guarde correctamente. En este caso, se creó una página llamada **Estática** para utilizar de ejemplo en la documentación.

Hecho esto, ya está creada la página y se puede proceder con el siguiente paso.

## Editar una página ya existente

Cuando la página ya está creada, ya se puede utilizar el site editor para personalizar toda la información necesaria. Para ello, acudimos directamente a la URL de la página que se desea editar, en este caso, para el ejemplo de la documentación utilizaremos la URL de la página 47club, /47club.

Hay un único bloque en el que se editará y plasmará todo el texto, y es el que se encuentra en el bloque de Fila, llamado Texto RTF.

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 11.10.26 a. m..png" alt=""><figcaption></figcaption></figure>

Este bloque es sólo un bloque de texto, pero tiene múltiples posibilidades de dar formato, con los siguientes caracteres de formato:

* Título principal: `# + espacio + texto` (Es un numeral, un espacio y el texto del título).
* Título secundario: `## + espacio + texto` (Es 2 numerales, un espacio y el texto del título).&#x20;
* Texto en negrita: `**texto**` (Es 2 asteriscos, el texto que se quiere resaltar sin espacios y 2 asteriscos).
* Texto itálica: `*texto*` (Es 1 asterisco, el texto que se quiere resaltar sin espacios y 1 asterisco).
* Negrita e itálica: `***texto***` (Es 3 asteriscos, el texto que se quiere resaltar sin espacios y 3 asteriscos).
* Listas numeradas: `1. +espacio Texto 2. +espacio Texto 3. +espacio Texto` (Es número, punto, un espacio y el texto). Se tiene que escribir uno solo por linea.
* Listas no numeradas: `- +espacio Texto - +espacio Texto - +espacio Texto` (Es guión medio, un espacio y el texto) Se tiene que escribir uno solo por linea.&#x20;
* Email: Cuando se escribe un texto que incluye un @ automaticamente se va a transformar en un email (destacandolo con texto celeste) y agregando el link al mail sin tener que hacer nada adicional.&#x20;
* Link: Cuando se escribe un texto que incluye un www y .com, .ar o cualquier dominio, automaticamente se va a transformar en un CTA (destacandolo con texto celeste) y agregando el link a la web sin tener que hacer nada adicional.
