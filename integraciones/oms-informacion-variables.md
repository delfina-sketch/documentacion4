---
icon: puzzle-piece
---

# OMS - Información variables

## Variables

Son datos dinámicos que se muestran en los mails. Es muy importante que se incluyan estas variables en los mails para que el cliente pueda recibir la información correspondiente a cada tipo de mail.

{% hint style="danger" %}
Estas variables NO deben ser modificadas. Siempre se encuentran entre < >.
{% endhint %}

### Listado

* ID de la orden: <%= decorated\_order.id %>
* Datos de envío:
  * Nombre: <%= decorated\_bill.full\_name %>
  * Dirección: <%= @order.choice.decorate.full\_address %
* Método de envío: <%= decorated\_order.shipping\_method %>
* Facturación:
  * Nombre: <%= decorated\_bill.full\_name %>
  * Dirección: <%= decorated\_bill.full\_address %>
  * Dirección: <%= decorated\_bill.location %>
  * País: <%= decorated\_bill.country\_name %>
* Método de pago: <%= decorated\_order.payment\_method %>
* Nombre de la marca: <%= Setting.first.brand\_name %> (Tomará el nombre de la marca cargado en el backoffice)
* Número de seguimiento: <%= decorated\_order.shipping\_code %>
* Botón rastrear pedido: <%= decorated\_choice.shipping\_url %>
* Datos del cliente
  * Nombre: <%= @order.choice.first\_name %>
  * Apellido: <%= @order.choice.last\_name %>
  * Dirección: <%= decorated\_choice.address %>
* Nombre de la sucursal: <%= nom\_suc %>
* Foto del producto: = <%=entry.decorate.entry\_variant\_image%>
* Nombre del producto: <%= entry.decorate.title %>
* Color y talle: <%= property.display %>
* Cantidad: <%= entry.decorate.quantity %>
* Precio con descuento: <%= decorated\_order.discount %>
* Full price: <%= entry.decorate.price %>
* Subtotal: <%= decorated\_order.subtotal %>
* Envío: <%= decorated\_order.shipping\_rate %>
* Total: <%= decorated\_order.price %>
