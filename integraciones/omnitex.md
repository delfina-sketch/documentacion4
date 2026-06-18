---
hidden: true
---

# 🧩 Omnitex

## **Descripción**

**Omnitex** es una solución de Pow para la asignación de pedidos Omnicanales de Vtex. Este producto reemplaza a la Arquitectura de Franquicias de Vtex, disponibilizando el total del stock (Depósito Central + Locales) en el sitio web.

Esta solución permite garantizar mayor agilidad en el envío, además de eficientizar los costos logísticos, minimizar inmovilizaciones de stock y mejorar el servicio al cliente.

## Funcionamiento

<figure><img src="https://lh7-us.googleusercontent.com/4B1UNxJ10Y7km1zNDRi1-Mlb-aZUpZrAVMCPVn7v37OLcXvSKkyBXi8aAR2bB9h79PYXnym4vW0C7rWfOzbYppuzQTQWN6QwtLaPtFe3TWkCRv0Rxz-t0sIKRZKTztgddMhJigyI95gRqWERNGG1TMc" alt="" width="375"><figcaption></figcaption></figure>

1. NEO informa el Stock del Depósito Central + Locales a Link Up
2. Link Up Informa el total de stock a Vtex (Depósito Central + Locales)
3. Vtex informa el ingreso de órdenes a Link Up
4. Link Up informa órdenes que ingresan de Vtex a “Omnitex”
5. Omnitex asigna un depósito a c/ítem de la orden y lo informa a Link Up
6. Link Up informa las órdenes que ingresan a NEO (con la asignación de pedidos)

## Consideraciones

* Disponibiliza el stock de los locales que queremos que ofrezcan su stock para la venta omnicanal.
* Presenta una lógica para asignar depósitos a los distintos ítems que componen una orden. Esta lógica está definida por criterios previamente definidos:
  * Generar la menor cantidad de envíos posibles→ Por ejemplo: una orden tiene 2 ítems A y B. El ítem A se encuentra solo en el Depósito Central y el B en el Depósito Central y también en el Local 1. Omnitex priorizará llevar a cabo un sólo envío, abasteciendo A y B desde el Depósito Central, y no enviando un ítem de cada depósito.
  * Ante igualdad de envíos posibles se prioriza el Depósito Central → Si todas las opciones para completar la orden generan la misma cantidad de envíos, se prioriza utilizar el stock que se encuentra en Depósito Central.

## Accesos a Link Up - Pantalla “Omnicanalidad”

Dentro de Link Up existe una pantalla destinada a “Omnicanalidad”. Se puede acceder a la misma con los siguientes usuarios:

**Usuario con acceso a todas las funcionalidades de Link Up:**

* Usuario: [47street@pow.la](mailto:47street@pow.la)
* Contraseña:&#x20;
* URL: [http://52.34.10.130/admins/sign\_in](http://52.34.10.130/admins/sign_in)

**Usuario con único acceso a la pantalla de Omnicanalidad (para ATC):**

* Usuario : 47street\_atc@pow.la
* Contraseña :
* URL: [http://52.34.10.130/admins/sign\_in](http://52.34.10.130/admins/sign_in)

## Pantalla “Omnicanalidad”

### Acceso con Usuario [47street@pow.la](mailto:47street@pow.la):

1. Dirigirse al siguiente link [http://52.34.10.130/admins/sign\_in](http://52.34.10.130/admins/sign_in) y completar los datos correspondientes para loguearse:

<figure><img src="https://lh7-us.googleusercontent.com/SJI11zNdV9cr40iMNGtkxqZqaHTFIHf6i5E_VHOaVmjuKyryjmca25s5b34BbvwQHJeR50GAzt4NMXTeDPe_icNUdySP6vwIuiYrMUdEGyB5Gh3a5Ljf1Fz9Y6ab62IlPIV-rE0vtBVvrUXfRumYfQc" alt="" width="375"><figcaption></figcaption></figure>

2. Hacer clic en “Activar Servicios”

<figure><img src="https://lh7-us.googleusercontent.com/nd5FG5MtUm9fZjLIoapMsdxA3r1DcuUmKGahkOe_Ov6BC0c31GxOFpe1zj0HPxXJjhk0z4iInc9HFMejZXG44YqCGzQW2bsh0MI7ih_x1bFvaS_dpQQAlGX56dYhDFirWbSXbh-IerTmKnlO5iRI8oM" alt="" width="563"><figcaption></figcaption></figure>

3. Hacer clic en “Omnicanalidad”

<figure><img src="https://lh7-us.googleusercontent.com/_sukMr6TYLe8sicPa4sp6S-Oti3kgMHEkPwblXUDpMxcy2GZ97Afq4giIrqUooxcfGvObPG-TrdkU_VnQlzkm4apbXmKNDU5wXnkrV50l7H-9bpVxEIIfajxAjazDuchvZy-LB9SL2hX2Dntg69iV2M" alt="" width="563"><figcaption></figcaption></figure>

4. Para descargar un CSV con el detalle de órdenes informadas a NEO, se debe seleccionar el rango de fecha deseado (Desde - Hasta) y hacer clic en el botón “Descargar CSV”

<figure><img src="https://lh7-us.googleusercontent.com/7Yf9-ZqJUhgQ0N3ujdnEpuoMzqiirp66lznk5KF-oFDji6dOZtSd_H2fc8S5cpuzr6VNPT_uyaG8tBDlZrRVy9uund-qi4biZCIRfyCLITMCq_3G9QbJfoAXTuWUs7FUf27w_Ky76NZ3GtU5bH0gkJo" alt="" width="563"><figcaption></figcaption></figure>

El CSV descargado presenta el listado de órdenes que Link Up informó a NEO, con el siguiente formato (similar a como al export obtenido en Vtex)

<figure><img src="https://lh7-us.googleusercontent.com/T7T7-3LRkyZ6epAvGHBKp5xgRtlMek8-Ux2JrU-7QjSJ4LDd7-sWRHeTJRzkoXpzNCFCEZ8ndJ8AvFDjHXdoC8pRY4smAhvPuJPTnEaoWkTyXeo92fjVtH6Bv9eIGxk8VYJu6Ufk5geC0XprIYQCfjE" alt=""><figcaption></figcaption></figure>

5. Para observar el detalle de una orden y a qué depósito se asignó cada uno de sus ítems, se puede filtrar el pedido en el buscador.

Se puede hacer la búsqueda por Nº largo de orden (Ej: 1370970773366-01) o por Nº corto (Ej: 773366). Al completar con el Nº de pedido, hacer clic en “Buscar”

<figure><img src="https://lh7-us.googleusercontent.com/r6PBIBxruZYs4oiJwieSYwicA8_yKoc8Z2cuc7c_KRSuQvigZHew7NKZbwW8w2ZVO-XfWg8ov1QZEtgq-hyXkutlCSdGA9HXSn0kCH7sFhhA1Pw98qCGoowIvJ28zL3cVbAkKvW0EJ4Q0hx8008zNcU" alt="" width="563"><figcaption></figcaption></figure>

Al desplegarse el detalle de la orden se puede visualizar la siguiente información:

* SKU/s que componen el pedido
* Producto → Descripción del SKU
* Precio Unitario
* Precio con descuento → Precio al que queda el ítem con el descuento aplicado, en caso de tenerlo.
* Cantidad → Unidades de ese ítem.
* Depósito → Depósito al que fue asignado el ítem.

<figure><img src="https://lh7-us.googleusercontent.com/XaWeNuvHz1TbyH_KaYlIL5KB-WkJ2T8Zrrq1FraiGctQ2By2jj0d2MhVJ55guSkLZYb1lge0l5w821AVWnw4rncfkzkxUmt9UmN3uB2Hw3mSBciHelx8mKWBBUz0LaghHYrkhNq8k7Q4B3lem2EJsZY" alt="" width="563"><figcaption></figcaption></figure>

### Acceso con Usuario [47street\_atc@pow.la](mailto:47street_atc@pow.la):

1. Dirigirse al siguiente link [http://52.34.10.130/admins/sign\_in](http://52.34.10.130/admins/sign_in) y completar los datos correspondientes para loguearse:

<figure><img src="https://lh7-us.googleusercontent.com/wEkRunTRpj5-rWgRfZjiFWg0uBT25lQXvG6nXwScYlJv0oz1jPgnMln6WG_77LeXQtySg8y_qRbMD8qQLXkwZrQ8AuGgPDjLIUUt1kEJhlw967vc-coyIIByt7OOuLGDzEgQZSokLephtAde83CSmi8" alt="" width="375"><figcaption></figcaption></figure>

Al iniciar sesión se abre automáticamente la pantalla de “Omnicanalidad”.

2. Para descargar un CSV con el detalle de órdenes informadas a NEO, se debe seleccionar el rango de fecha deseado (Desde - Hasta) y hacer clic en el botón “Descargar CSV”.

<figure><img src="https://lh7-us.googleusercontent.com/7Yf9-ZqJUhgQ0N3ujdnEpuoMzqiirp66lznk5KF-oFDji6dOZtSd_H2fc8S5cpuzr6VNPT_uyaG8tBDlZrRVy9uund-qi4biZCIRfyCLITMCq_3G9QbJfoAXTuWUs7FUf27w_Ky76NZ3GtU5bH0gkJo" alt=""><figcaption></figcaption></figure>

El CSV descargado presenta el listado de órdenes que Link Up informó a NEO, con el siguiente formato (similar a como al export obtenido en Vtex)

<figure><img src="https://lh7-us.googleusercontent.com/T7T7-3LRkyZ6epAvGHBKp5xgRtlMek8-Ux2JrU-7QjSJ4LDd7-sWRHeTJRzkoXpzNCFCEZ8ndJ8AvFDjHXdoC8pRY4smAhvPuJPTnEaoWkTyXeo92fjVtH6Bv9eIGxk8VYJu6Ufk5geC0XprIYQCfjE" alt=""><figcaption></figcaption></figure>

3. Para observar el detalle de una orden y a qué depósito se asignó cada uno de sus ítems, se puede filtrar el pedido en el buscador.

Se puede hacer la búsqueda por Nº largo de orden (Ej: 1370970773366-01) o por Nº corto (Ej: 773366).&#x20;

Al completar con el Nº de pedido, hacer clic en “Buscar”

<figure><img src="https://lh7-us.googleusercontent.com/r6PBIBxruZYs4oiJwieSYwicA8_yKoc8Z2cuc7c_KRSuQvigZHew7NKZbwW8w2ZVO-XfWg8ov1QZEtgq-hyXkutlCSdGA9HXSn0kCH7sFhhA1Pw98qCGoowIvJ28zL3cVbAkKvW0EJ4Q0hx8008zNcU" alt="" width="563"><figcaption></figcaption></figure>

Al desplegarse el detalle de la orden se puede visualizar la siguiente información:

* SKU/s que componen el pedido
* Producto → Descripción del SKU
* Precio Unitario
* Precio con descuento → Precio al que queda el ítem con el descuento aplicado, en caso de tenerlo.
* Cantidad → Unidades de ese ítem.
* Depósito → Depósito al que fue asignado el ítem.

<figure><img src="https://lh7-us.googleusercontent.com/XaWeNuvHz1TbyH_KaYlIL5KB-WkJ2T8Zrrq1FraiGctQ2By2jj0d2MhVJ55guSkLZYb1lge0l5w821AVWnw4rncfkzkxUmt9UmN3uB2Hw3mSBciHelx8mKWBBUz0LaghHYrkhNq8k7Q4B3lem2EJsZY" alt="" width="563"><figcaption></figcaption></figure>
