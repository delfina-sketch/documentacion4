---
hidden: true
---

# 🧩 Integración Vtex | Link Up | NEO

Esta integración se utiliza para actualizar el stock y precio de los diferentes productos así como también informar las pedidos creados en Vtex a Neo Retail.

#### Flujo de integración <a href="#flujo-de-integracion" id="flujo-de-integracion"></a>

<figure><img src="../../.gitbook/assets/image (10).png" alt="" width="563"><figcaption></figcaption></figure>

#### Datos de Acceso a Link up

* Usuario:  [47street@pow.la](mailto:47street@pow.la)
* Password: 111111
* Url: [http://52.34.10.130/admins/sign\_in](http://52.34.10.130/admins/sign_in)



1. **Actualización de Stock y Precios**

Para realizar esta integración se habilitó un FTP en el cual Neo Retail deja 1 archivo (Archivo de Stock) para realizar actualizaciones. Link-Up se encarga de procesar los archivos para luego impactarlos.&#x20;

_Tiempo de actualización de stock:_ actualmente se actualizan cada 40 min en ambos casos.

_Actualización de precios:_ Actualmente la actualización de precios, 47 ST la hace de manera manual (Link-up no hace nada)

2. **Actualización de Stock y Precios en Vtex**

Una vez procesados los CSV, Link-Up comienza a impactar mediante API a Vtex las actualizaciones indicadas en el CSV para cada SKU.

Es importante saber que los artículos que no estén catalogados en VTEX no serán procesados.

3. **Buscar Órdenes en Vtex**

Link-Up es el responsable de buscar las nuevas órdenes que generan en VTEX para que luego sean normalizadas para su futuro procesamiento al ser informadas al ERP (Neo Retail). Esta integración está realizada por API, haciendo llamadas a las APIs de Vtex.

_Tiempo de actualización: Online._&#x20;

4. **Informar Ventas**

Link-Up luego de tener procesada una venta en VTEX, normaliza la información y la adapta para que pueda ser procesada por Neo Retail. Se generan 2 archivos por cada venta tal como fue requerido por el ERP.\
&#xNAN;_&#x54;iempo de actualización: Online, por cada venta._

### ¿Cómo prender y apagar integración?

A continuación vamos a explicar cómo se pueden prender y apagar los servicios de integración en el Middleware ERP que utilizamos para realizar la integración de precios, stock y upload de facturas.

1. Ir a la sección Clientes -> URL: [http://52.34.10.130/clients](http://52.34.10.130/clients)

<figure><img src="../../.gitbook/assets/Captura de Pantalla 2024-03-25 a la(s) 16.43.53.png" alt=""><figcaption></figcaption></figure>

2. Hacer clic en “Activar Servicios” -> URL: [http://52.34.10.130/clients/2](http://52.34.10.130/clients/2)

<figure><img src="../../.gitbook/assets/Captura de Pantalla 2024-03-25 a la(s) 16.45.23.png" alt=""><figcaption></figcaption></figure>

3. Hacer clic en “Micro Servicios” -> URL: [http://52.34.10.130/clients/2/micro\_services](http://52.34.10.130/clients/2/micro_services)

<figure><img src="../../.gitbook/assets/Captura de Pantalla 2024-03-25 a la(s) 16.47.00.png" alt=""><figcaption></figcaption></figure>

4. En la imagen a continuación se puede ver que todos los servicios se encuentran encendidos.

<figure><img src="../../.gitbook/assets/Captura de Pantalla 2024-03-25 a la(s) 17.04.22.png" alt=""><figcaption></figcaption></figure>

5. Para desactivar algún servicio se debe hacer clic en el botón de pausa en la columna acciones.

<figure><img src="../../.gitbook/assets/Captura de Pantalla 2024-03-25 a la(s) 17.12.26.png" alt=""><figcaption></figcaption></figure>

#### **Listado de servicios:**

El siguiente listado detalla la funcionalidad de cada servicio. Dependiendo de la acción deseada se debe escoger el servicio adecuado.

1. Sync orders from Vtex to FTP NEO → Sirve para informar las órdenes a NEO.
2. Sync DAFITI WITH Vtex → Sirve para aprender o apagar la integración con Dafiti(Actualmente la integración con Dafiti no está en funcionamiento).
3. Sync Invoices NEO → Sirve para bajar del FTP las facturas y las impacta en NEO.
4. Download Stock/Price from FTP → Neo deja un archivo en el FTP. Se baja el archivo y se procesa cada 3 horas.

### **¿Cómo se configura el FTP?**

Para poder configurar el FTP debemos ingresar a “Activar Servicios” → Configuración FTP

<figure><img src="https://lh7-us.googleusercontent.com/tnQK5k4i_U3iRZBWG9LqLbuUjmrlxtuDfDjSAeJTISMo0OZgh2-mfAHRhFmvn4hEv7zYFg3bn4u_wcVcd6eCG8w28Yxp3RY7YtXh7Pc-am581EOmLwKk-j64xnTbTvzLRPSsPdOI4_Moc2-b1lJPd58" alt=""><figcaption></figcaption></figure>

Una vez que seleccionamos “Configuración FTP”, visualizaremos la siguiente pantalla donde debemos completar todos los datos requeridos para configurar el FTP.<br>

<figure><img src="https://lh7-us.googleusercontent.com/8bpCReaiGuk9fv-0ktlZ6scXWQBESLpTzeLogUVYv-MPUB5PcReDB-zsqvQgfaVO2oSdlJiy56mX513G1ZsvESbe2DbB6ZU0WFGZhcPZjygDqIQju51ZgeqVlgIDwWqaAKp34xepRbFpDhxfTsIiL6I" alt=""><figcaption></figcaption></figure>

Una vez que seleccionamos “Configuración FTP”, visualizaremos la siguiente pantalla donde debemos completar todos los datos requeridos para configurar el FTP.

<figure><img src="https://lh7-us.googleusercontent.com/h3FdOOGuSL-Az7o8L4bbIzFdE2U2JwLA8CVSn-5-vbIikls2kIVscusop8FQovpnJ30gu2H57Jn0wuQbQLsIW-NUc15azTao7HFG8A9OB6qS-bT0uMLfAaVklrEI8_ZNjaUTZR-XQsFU1sYEWXk8Mh4" alt=""><figcaption></figcaption></figure>
