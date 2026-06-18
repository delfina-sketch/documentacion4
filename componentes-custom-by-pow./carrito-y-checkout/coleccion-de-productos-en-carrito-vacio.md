# 📌 Colección de productos en carrito vacío

## Descripción

Este componente permite mostrar en el carrito desplegable, una colección de productos que permita aumentar el agregado al carrito. Esto se mostrará únicamente cuando no haya productos agregados.&#x20;

<figure><img src="../../.gitbook/assets/47 (1).gif" alt=""><figcaption></figcaption></figure>

### Pasos para la configuración

1.  Ingresar por el **administrador de VTEX > Configuración de la tienda > Storefront > Checkout > Código** y hacer click en el archivo **minicart-context.json.**<br>

    <figure><img src="../../.gitbook/assets/1 (3).png" alt=""><figcaption></figcaption></figure>


2. Al ingresar al archivo, contaremos con estos campos para editar:

```json
{
    "MiniCartProductGrid":{
      "showComponent":true,
      "collectionID": "447",
      "collectionName": "New In",
      "maxItemsProducts": 10,
      "title": "Tu carrito está vacio",
      "subTitle": "Llenalo con estos items:"
	}
}
```

#### Campos

* **"showComponent":** se podrá con las opciones <mark style="color:blue;">true</mark> (para que se muestre el componente) o <mark style="color:red;">false</mark> (para que no se muestre).&#x20;
* **"collectionID":** se completará el ID de la colección a mostrar entre comillas. Por ej: <mark style="color:blue;">"447"</mark>
* **"collectionName":** se completará entre comillas el nombre que queremos que se muestre como título de la colección. Por ej: <mark style="color:blue;">"New In"</mark>
* **"maxItemsProducts":** se completará el número máximo de productos a mostrar. Por ej: <mark style="color:blue;">10</mark>.
* **"title":** se completará entre comillas el nombre que queremos que se muestre como título del carrito. Por ej: <mark style="color:blue;">"Tu carrito está vacio"</mark>
* **"subTitle":** se completará entre comillas el nombre que queremos que se muestre como subtítulo del carrito. Por ej: <mark style="color:blue;">"Llenalo con estos items:"</mark>

3.  Al finalizar los cambios, recordar hacer click en **Guardar** para que impacten en producción. <br>

    <figure><img src="../../.gitbook/assets/2 (4).png" alt=""><figcaption></figcaption></figure>





