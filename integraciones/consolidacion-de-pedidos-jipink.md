---
hidden: true
---

# 🧩 Consolidación de pedidos Jipink

### Descripción

Jipink es una transportadora y operador logístico que brinda soluciones de distribución para ecommerce y retail.

Se especializa en:

* Distribución nacional de pedidos online.
* Servicios de envíos estándar, cambios y devoluciones.
* Integración vía API con sistemas de gestión de pedidos (OMS) para automatizar la logística.

En nuestro ecosistema, Jipink permite gestionar despachos de forma unificada, generar etiquetas y obtener tracking para los clientes finales.

### Método adicional: Armado de Paquetes y Consolidación Omnicanal

Además de los métodos tradicionales, Jipink fue integrado en 47 Street con la funcionalidad de consolidación de pedidos omnicanales.

#### Objetivo

Permitir unificar múltiples paquetes de un mismo pedido (spliteado en varios depósitos/locales) en un solo envío, de manera que se emita un único número de seguimiento para el cliente.

#### Flujo de creación y consolidación

#### Caso omnicanal (pedido dividido en varias órdenes)

1. **Primera orden que ingresa al MS OOLL**
   * Se crea un **envío padre** (envío general) → genera un **tracking padre** y un **ID de envío**
   * Este tracking **no se asocia al pedido**.
   * Inmediatamente se debe crear un **paquete hijo** (con `tipo_paquete: true` y sin `id_externo`).
   * El tracking de este paquete hijo será el que represente a la primera orden.
2. **Órdenes siguientes (segunda, tercera, …)**
   * Para cada orden, se crean **nuevos paquetes hijos** dentro del mismo envío padre.
   * Se envía `tipo_paquete: true` + `id_externo` con el **ID del envío padre**.
   * Cada paquete hijo genera su propio **tracking secundario**.
3. **Consolidación en Jipink**
   * Cada depósito/local imprime y despacha la **etiqueta de su paquete hijo**.
   * Jipink recolecta los paquetes y los consolida.
   * En ese momento imprime la **etiqueta del envío padre** (tracking principal consolidado).
   * Este tracking padre es el que se usa para:
     * El **mail transaccional único al cliente**.
     * La **visualización del detalle de la orden en el OMS** como tracking principal.

***

#### Generación e impresión de etiquetas

* **Tracking padre:**
  * Se genera en el MS OOLL, pero no se asocia a ningún pedido.
  * Solo se imprime en la planta Jipink una vez consolidado el envío.
  * Se usa como tracking principal en el transaccional y en el OMS.
* **Trackings hijos:**
  * Cada paquete hijo tiene su propia etiqueta y número de tracking (`numeroDeEnvioPaquete`).
  * Estos trackings se usan para preparar pedidos en PL y figuran en las picking lists.
  * Están vinculados automáticamente al tracking padre.

#### Beneficios del nuevo flujo

* Mejor experiencia de cliente: recibe un único tracking consolidado aunque su pedido se haya preparado en múltiples depósitos/locales.
* Menos costos operativos: reducción de etiquetas y envíos duplicados.
* Automatización completa: la lógica se resuelve desde OMS + MS OOLL + PL sin intervención manual.
* Escalabilidad: mismo flujo aplicable a cualquier marca que use Jipink en omnicanalidad.

### Aclaraciones técnicas:

1. **Envío convencional (sin paquetes):**
   * Si no se envía `tipo_paquete`, el envío se crea como **envío padre estándar**.
2. **Primer paquete hijo (primer orden):**
   * Se envía `tipo_paquete: "true"`, sin `id_externo`.
   * Se debe enviar también `bultos.numeroPaquete` con el valor `1`.
   * El sistema crea automáticamente el envío padre y el primer paquete hijo.
3. **Paquetes hijos adicionales (órdenes siguientes):**
   * Se envía `tipo_paquete: "true"` y `id_externo` con el **ID del envío padre**.
   * Se debe enviar `bultos.numeroPaquete` con el número correlativo de paquete.

#### Ejemplo de response (envío con paquetes hijos)

```json
{
    "response": "Success",
    "providerStatus": "Package added",
    "numeroDeEnvioPaquete": "S2RP7",  // tracking hijo
    "numeroDeEnvio": "S3YLB",         // tracking padre
    "idPadre": 1136,
    "idPaquete": 1138,
    "package": {
        "package_number": 2
    },
    "sucursalDeDistribucion": {
        "id": null,
        "descripcion": ""
    },
    "sucursalDeRendicion": null,
    "sucursalDeImposicion": null,
    "numeroDePermisionaria": null,
    "descripcionServicio": null,
    "etiqueta": ""
}
```

📌 En este response:

* `numeroDeEnvio` = tracking padre consolidado.
* `numeroDeEnvioPaquete` = tracking del paquete hijo.
* `idPadre` = ID del envío general.
* `idPaquete` = ID del paquete hijo.
