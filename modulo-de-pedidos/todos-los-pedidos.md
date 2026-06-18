# 🛒 Todos los pedidos

## Descripción

Dentro de Pedidos ->Todos los pedidos, podremos tener una vista general de los últimos pedidos de nuestra tienda.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 8.22.28 p. m..png" alt=""><figcaption></figcaption></figure>

En la parte superior, los primeros datos disponibilizados serán las métricas de los pedidos que vemos actualmente.&#x20;

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 8.38.39 p. m..png" alt=""><figcaption></figcaption></figure>

Un dato importante a tener en cuenta es que las métricas son en función a los filtros que tengamos activados. Esto quiere decir que no necesariamente son los pedidos reales, ya que como se desarrolla en Status del pedido, algunos pedidos podrían estar pendientes de pago o directamente cancelados.

Como una persona puede tener varios pedidos cancelados, es posible que sin filtros, las métricas nos darán números no acertados y no serían reflejo fiel del que poder sacar referencias para toma de decisiones. Por ello, si se quiere tener un reflejo más fiel de la cantidad real de pedidos válidos, es necesario aplicar filtros.

En esta vista, podemos ver las métricas y la cantidad de pedidos que están aceptados (listos para preparar) y la cantidad que están cancelados.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 8.24.59 p. m..png" alt=""><figcaption></figcaption></figure>

Los pedidos cancelados no pasaron las comprobaciones necesarias para constituirse como un pedido para despachar, y a mayor flujo de pedidos, se aumentan las posibilidades de tener una mayor cantidad de cancelados (porque el cliente no pagó, puso mal datos, la pasarela rechazó el pago, etcétera) por lo que es necesario poder filtrar esos pedidos cancelados para que no interfieran con los pedidos que sí merecen nuestra atención.&#x20;

Para ello, hacemos click en "Filtrar por status" y nos enfocaremos en los que requieren nuestra atención, que son los "Listos para preparación".

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 8.39.34 p. m..png" alt=""><figcaption></figcaption></figure>

Así, podremos notar que las métricas de la parte superior se actualizaron y muestran ahora un número más acertado, contando únicamente los pedidos en el status indicado.

El otro filtro que debe considerarse para evitar inconvenientes, es el de Fecha. Es importante corroborar tener el filtro en hoy, últimos 7 días, mes actual o últimos 30 días. De esta forma, los últimos pedidos estarán disponibilizados en la lista.

Si utilizamos el filtro ayer o una personalización por fecha, podríamos no estar viendo los pedidos de hoy que requieren nuestra atención. Por otro lado, la ventana de fecha personalizada más larga que podremos tener, es de 6 meses. Si queremos ver pedidos más antiguos, tendremos que ir haciéndolo por rangos de 6 meses ya que VTEX no permite la vista completa de rangos más amplios por cuestión de rendimiento del administrador.

Si hacemos click en "Filtros" podremos observar toda la cantidad de filtros que nos permite aplicar VTEX para casos puntuales en los que necesitemos aplicar filtros específicos en las órdenes:

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 8.43.44 p. m..png" alt=""><figcaption></figcaption></figure>

Una vez tenemos la lista de órdenes según nuestras necesidades, tendremos disponible el listado de las órdenes que cumplan con esos criterios, algunos datos generales como status, cliente, cantidad de SKUs y valor de la órden, y además tendremos la posibilidad de ver la información del pedido haciendo click en el ID del pedido.

<figure><img src="../.gitbook/assets/Captura de pantalla 2024-04-07 a la(s) 8.44.26 p. m..png" alt=""><figcaption></figcaption></figure>
