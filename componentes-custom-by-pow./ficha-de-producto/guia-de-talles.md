# 📌 Guía de Talles

## Descripción

Se realizó un componente custom para la visualización de la guía de talles que se encuentra en la ficha de producto. A través de este, se puede ver las medidas de cada uno de los talles, cómo debe medirse el usuario, y también agregar al carrito desde la misma guía de talles.

Este desarrollo se trabajó de acuerdo a los modelos de indumentaria solicitados: tops, bottoms y calzado. <br>

<figure><img src="../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

{% hint style="info" %}
Cada uno de estos modelos: tops, bottoms y calzado, tienen una imagen y detalle de como medirse distinta. Esta información se modifica vía JSON
{% endhint %}

## Configuración

Para configurar la tabla de talles, se debe agregar el modelo de tabla de talle correspondiente a el/los productos que se deseen y crear un JSON.

### Paso a paso para agregar la tabla de talles

1.  Acceder a Catálogo -> Productos y Skus

    <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-07-19 a la(s) 8.55.01 a. m..png" alt=""><figcaption></figcaption></figure>
2.  Ingresar en el producto el modelo de la tabla que necesiten:

    <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-07-19 a la(s) 8.56.10 a. m..png" alt=""><figcaption></figcaption></figure>

Los productos que se mostrarán con la guía de talles serán los que tengan configurado los modelos:

* Tops
* Bottoms
* Calzado

{% hint style="info" %}
Cuando agreguen un nuevo modelo a la Guía de talles deberán solicitar&#x20;
{% endhint %}

### **Cómo crear el JSON**

1. Ingresar en configuración de la tienda -> Storefront -> Checkout.
2. Ingresar a apartado de "Código" -> customSize.json

<figure><img src="../../.gitbook/assets/Captura de pantalla 2024-07-19 a la(s) 9.14.02 a. m..png" alt=""><figcaption></figcaption></figure>

### Las partes del JSON que se pueden editar son:

* JSON de ejemplo:

<pre class="language-json"><code class="lang-json">    "tipoTalles": [
        {
            "tipo": <a data-footnote-ref href="#user-content-fn-1">"tops",</a>
            "imagenRef": "https://street47.vtexassets.com/assets/vtex.file-manager-graphql/images/44252fbc-f2a3-4fed-a1da-42c6aa1e79b4___48d42a42bf0711ebba7b219230e05539.png",
            "referencia": [
                {
                    "name": "Contorno de pecho",
                    "value": "Con una cinta métrica, medi alrededor de la parte más ancha de tu pecho."
                },
                {
                    "name": "Contorno de cintura",
                    "value": "Colocá la cinta alrededor de la parte más estrecha entre tu pecho y cadera."
                },
                {
                    "name": "Contorno de cadera",
                    "value": "Con los pies juntos, medí con la cinta la parte más ancha de tu cadera."
                }
            ],
            "talles": [
                {
                    "valorTalle": "00",
                    "medidas": [
                        {
                            "item":"Contorno de pecho",
                            "value": "82/85"
                        },
                        {
                            "item":"Contorno de cintura",
                            "value": "61/64"
                        },
                        {
                            "item":"Contorno de cadera",
                            "value": "90/93"
                        }
                    ]
                },
                {
                    "valorTalle": "01",
                    "medidas": [
                        {
                            "item": "Contorno de pecho",
                            "value": "86/89"
                        },
                        {
                            "item": "Contorno de cintura",
                            "value": "65/68"
                        },
                        {
                            "item": "Contorno de cadera",
                            "value": "94/97"
                        }
                    ]
                },
                {
                    "valorTalle": "02",
                    "medidas": [
                        {
                            "item": "Contorno de pecho",
                            "value": "90/93"
                        },
                        {
                            "item": "Contorno de cintura",
                            "value": "69/72"
                        },
                        {
                            "item": "Contorno de cadera",
                            "value": "98/101"
                        }
                    ]
                },
                {
                    "valorTalle": "03",
                    "medidas": [
                        {
                            "item": "Contorno de pecho",
                            "value": "94/97"
                        },
                        {
                            "item": "Contorno de cintura",
                            "value": "73/76"
                        },
                        {
                            "item": "Contorno de cadera",
                            "value": "102/105"
                        }
                    ]
                },
                {
                    "valorTalle": "04",
                    "medidas": [
                        {
                            "item": "Contorno de pecho",
                            "value": "98/101"
                        },
                        {
                            "item": "Contorno de cintura",
                            "value": "77/80"
                        },
                        {
                            "item": "Contorno de cadera",
                            "value": "106/109"
                        }
                    ]
                }
            ]
        }
    ]
}
</code></pre>

* <mark style="color:blue;">"tipo"</mark>: "<mark style="background-color:purple;">tops</mark>", : deben ponerlo de acuerdo al modelo que quieran traer.
* <mark style="color:blue;">"imagenRef"</mark>: en la que deben poner la imagen que corresponda al tipo que está arriba, por ejemplo: "<mark style="background-color:purple;">https://street47.vtexassets.com/assets/vtex.file-manager-graphql/images/44252fbc-f2a3-4fed-a1da-42c6aa1e79b4\_\_\_48d42a42bf0711ebba7b219230e05539.png</mark>",
* <mark style="color:blue;">"name"</mark>: Pueden modificarlo: "<mark style="background-color:purple;">Contorno de pecho</mark>",&#x20;
* <mark style="color:blue;">"value"</mark>: Pueden modificarlo: "<mark style="background-color:purple;">Con una cinta métrica, medi alrededor de la parte más ancha de tu pecho.</mark>"
* En <mark style="color:blue;">"talles"</mark> pueden modificar <mark style="color:blue;">"valorTalle"</mark>: "<mark style="background-color:purple;">00</mark>", y por dentro: <mark style="color:blue;">"item"</mark>: "<mark style="background-color:purple;">Contorno de cadera</mark>", y <mark style="color:blue;">"value"</mark>: "<mark style="background-color:purple;">82/85</mark>" para modificar las medidas de cada talle.

{% hint style="info" %}
Lo resaltado con <mark style="background-color:purple;">violeta</mark> es lo que pueden editar
{% endhint %}

### **Cómo crear un nuevo modelo**

Cada vez que quieran agregar una nueva tabla de talles, podrán hacerlo sin bajar el requerimiento.

Para  crearlo deberán:

1. Crear un nuevo modelo con el nombre que deseen.
2. Cargar los productos que necesiten con ese modelo.
3. Crear en el JSON esa nueva tabla de talles, para el cual tendrán que copiar desde <mark style="color:blue;">"tipo": "tops"</mark>, al que le deberán poner el mismo nombre que el modelo. Y luego cargar lo restante del código que se menciona arriba.

{% hint style="info" %}
Recuerden, que antes de empezar a editar el JSON, copienlo en un word aparte para tener el respaldo por si se rompe.
{% endhint %}



[^1]: 
