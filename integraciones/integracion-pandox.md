---
hidden: true
---

# 🧩 Integración Pandox

## **Descripción**

Pandox crea soluciones innovadoras en ingeniería de datos impulsadas por inteligencia artificial, especialmente diseñadas para empresas del sector retail.

Actualmente la tienda de Vtex de 47 Street se encuentra integrado con Pandox a través de Link Up.

## Funcionamiento

* Link up diariamente envía un CSV a Pandox a través de un sistema de Storage (S3 AWS-Amazon).
* A través de un job llamado "pandox\_job" cada 20 minutos se crea el CSV con las nuevas ventas ingresadas y las mismas se informan a Pandox
* Se especifica dentro del CSV el medio de pago involucrado en la compra. En el campo "**TarjetaTipo"** del CSV se aclara qué medio de pago se utilizó

{% hint style="info" %}
En este archivo se listas los posibles medios de pago que puede tomar ese campo [listado de opciones para informar en el campo TarjetaTipo](https://drive.google.com/file/d/1QH3Yt26LjUicbyfQPL4LgiRsTyXCk_ab/view?usp=drive_link)
{% endhint %}

* Link Up saca los parámetros encriptados que envía Vtex dentro de los mails de los usuarios. De esta manera un mail recibido así desde Vtex > <mark style="color:blue;">vanesaroma@hotmail.com231601826415b.ct.vtex.com.br</mark> , es "procesado" por Link up, para informarlo limpio a Pandox > [vanesa-roma@hotmail.com](mailto:vanesa-roma@hotmail.com-231601826415b.ct.vtex.com.br)
* En caso de que algún campo del pedido deba viajar vacío es importante colocar desde Link Up un guión "-". Caso contrario Pandox no puede procesar los pedidos
* El proceso de informe de órdenes está **formato de transaccion** por lo que si una orden no se escribe tira error y vuelve a reintentar y vuelve a escribir la misma orden sucesivamente. Además en Link Up se marcan como exportados de a uno los pedidos, a medida que se van informando correctamente a Pandox.

### Ventas Canceladas no se informan a Pandox

Se trabajó un desarrollo en Link Up para que **no se informen** las ventas canceladas de ninguno de los canales de ventas a Pandox.

Al estar informándolas anteriormente se restaban del total de la facturación de cada día y les generaba diferencias respecto a lo que informan en archivos internos.

### Información de ventas de PACTO (Moda Circular Shopify) a Pandox

Con motivo del nuevo proyecto 47 Circular, 47 Street incorporó un sitio en Shopify gestionado por PACTO, donde se venden productos reacondicionados bajo la modalidad de moda circular.

#### Contexto del flujo de negocio

* Los usuarios podrán llevar prendas usadas a sucursales adheridas de la marca para canjearlas por puntos en la app 47 Club.
* Dichas prendas se reacondicionan y se ponen a la venta en la tienda **Shopify de PACTO**.
* Todos los pedidos que ingresen en este canal también deben ser informados a **Pandox** mediante el conector Link Up.

#### Reglas específicas para el envío a Pandox

1. **Origen de pedidos:** Todos los pedidos provenientes de Shopify (PACTO) deben informarse a Pandox.
2. **ID de sucursal (columna B):** siempre debe enviarse con el valor **"PACTO"**.
3. **Medio de pago:** el campo de medio de pago debe informarse con el valor **"PACTO"**.

#### Resumen

Este ajuste asegura que Pandox pueda diferenciar las ventas de **Moda Circular (PACTO)** de las ventas regulares de 47 Street, manteniendo la trazabilidad del proyecto dentro de sus reportes y sistemas de gestión.

<br>
