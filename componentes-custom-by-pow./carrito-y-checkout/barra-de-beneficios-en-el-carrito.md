# 📌 Barra de beneficios en el carrito

## Descripción

Este componente permite mostrar de forma rápida en el carrito, los beneficios alcanzados por el cliente según el monto agregado al carrito. \
La cantidad de beneficios, íconos, leyendas y montos mínimos para alcanzar los beneficios son autoadministrables por la marca desde un archivo json en el checkout.&#x20;

{% hint style="info" %}
_Todos los beneficios se encontrarán a la misma distancia entre ellos, a pesar de la diferencia de montos que existan entre ellos. Por esto, la barra de desplazamiento no se completará (o pintará) hasta alcanzar el monto del próximo beneficio._
{% endhint %}

## Pasos para la configuración

1. Acceder al administrador de VTEX.
2.  Ingresar por Configuración de la tienda > Storefront > Checkout<br>

    <figure><img src="../../.gitbook/assets/image (43).png" alt=""><figcaption></figcaption></figure>
3.  Al ingresar, debemos hacer click en la ruedita que se encuentra junto al nombre de la tienda<br>

    <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-09-24 a la(s) 12.49.53 p. m..png" alt="" width="308"><figcaption></figcaption></figure>
4.  Una vez allí, hacemos click en la pestaña Código y en el archivo llamado context-components.json



    <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-09-24 a la(s) 12.51.40 p. m..png" alt=""><figcaption></figcaption></figure>
5. Aquí debemos ubicarnos en esta porción de código

```json
"benefitsContext":{
    "PRICE_BENEFIT":200000,
    "isActive":true,
    "props":[
      {
        "beneficio_1":{
          "title":"Retiro gratis en tienda",
          "imageUrl":"/arquivos/icon-trash-equus.svg",
          "price":0
        }
      },
      {
        "beneficio_2":{
        "title":"Envío 100% gratis",
        "imageUrl":"/arquivos/icon-trash-equus.svg",
        "price":30000
        }
      },
      {
        "beneficio_3":{
          "title":"9 cuotas sin interés",
          "imageUrl":"/arquivos/icon-trash-equus.svg",
          "price":60000
        }
      },
      {
        "beneficio_4":{
          "title":"12 cuotas sin interés",
          "imageUrl":"/arquivos/icon-trash-equus.svg",
          "price":90000
                  }
      },
      }
    ]
  }
```

## **Campos:**

* **PRICE\_BENEFIT:** Valor máximo para alcanzar todos los beneficios.&#x20;
* "isActive": se debe completar con "true", para que se encuentre activa la funcionalidad, y "false" para apagar la funcionalidad.
* **beneficio\_1, beneficio\_2, \[...]:** cantidad de beneficios que se ofrecerán en el checkout. En caso de querer agregar más beneficios, deberá agregarse el objeto completo, asegurándonos de colocar una coma antes de colocar el siguiente objeto y que el nuevo beneficio quede por dentro de los \[ ], como en el archivo de ejemplo.&#x20;
* **title:** Leyenda que indica el beneficio a mostrar. Por ej: Retiro gratis en tienda
* **imageUrl:** Ícono que acompañará a cada beneficio.&#x20;
* **price:** Precio mínimo para alcanzar el beneficio. Por ejemplo, para el caso de Retiro gratis en tienda, el mismo siempre está disponible por lo que el precio mínimo es 0.&#x20;

6.  Una vez completados todos los campos, hacemos click en Guardar para que impacten los cambios<br>

    <figure><img src="../../.gitbook/assets/Captura de pantalla 2024-09-24 a la(s) 12.53.33 p. m..png" alt=""><figcaption></figcaption></figure>
7. En caso de querer agregar un nuevo beneficio, debemos colocar una coma en el último elemento, siguiendo la misma estructura como en este ejemplo:

`"benefitsContext":{`&#x20;

`"PRICE_BENEFIT":200000,`&#x20;

`"isActive":true,`

`"props":[`&#x20;

`{`&#x20;

`"beneficio_1":{`

`"title":"Retiro gratis en tienda",`&#x20;

`"imageUrl":"/arquivos/icon-trash-equus.svg",`&#x20;

`"price":0`&#x20;

`}`&#x20;

`},`

`{`&#x20;

`"beneficio_2":{`&#x20;

`"title":"Envío 100% gratis",`&#x20;

`"imageUrl":"/arquivos/icon-trash-equus.svg",`&#x20;

`"price":30000 }`&#x20;

`},`

`{`

`"beneficio_3":{`&#x20;

`"title":"9 cuotas sin interés",`&#x20;

`"imageUrl":"/arquivos/icon-trash-equus.svg",`&#x20;

`"price":60000`&#x20;

`}`&#x20;

`},`&#x20;

`{`&#x20;

`"beneficio_4":{`&#x20;

`"title":"12 cuotas sin interés",`&#x20;

`"imageUrl":"/arquivos/icon-trash-equus.svg",`&#x20;

`"price":90000`&#x20;

`}`&#x20;

`}`<mark style="background-color:green;">`,`</mark>&#x20;

<mark style="background-color:green;">`{`</mark>&#x20;

<mark style="background-color:green;">`"beneficio_5":{`</mark>&#x20;

<mark style="background-color:green;">`"title":"15 cuotas sin interés",`</mark>&#x20;

<mark style="background-color:green;">`"imageUrl":"/arquivos/icon-trash-equus.svg",`</mark>&#x20;

<mark style="background-color:green;">`"price":120000`</mark>&#x20;

<mark style="background-color:green;">`}`</mark>&#x20;

<mark style="background-color:green;">`},`</mark>&#x20;

<mark style="background-color:green;">`{`</mark>&#x20;

<mark style="background-color:green;">`"beneficio_6":{`</mark>&#x20;

<mark style="background-color:green;">`"title":"18 cuotas sin interés",`</mark>&#x20;

<mark style="background-color:green;">`"imageUrl":"/arquivos/icon-trash-equus.svg",`</mark>&#x20;

<mark style="background-color:green;">`"price":200000`</mark>

<mark style="background-color:green;">`}`</mark>&#x20;

`}`&#x20;

`] }`

{% hint style="info" %}
El primer beneficio siempre será en $0.
{% endhint %}



