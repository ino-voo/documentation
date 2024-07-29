Integrar Odoo con [transportistas de terceros](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html) para imprimir etiquetas de envío que incluyan precio, dirección de destino, números de rastreo y códigos de barra.

 Ver también

[Imprimir etiquetas de transportista de forma automática](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-carrier-labels)

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html#configuration "Enlazar permanentemente con este título")

Para generar etiquetas para transportistas de terceros, primero [instale el conector del transportista externo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html). Después, configure y active el [método de entrega](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-delivery-method), asegúrese de configurar el Nivel de integración a Obtener tarifas y crear envíos para generar etiquetas de envío. Finalmente, ingrese la [dirección de origen](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-source-address) de la empresa y [el peso de los productos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-weight).

 Ver también

[Transportistas externos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html)

![Configure la opción "Obtener tarifas y crear envíos".](https://www.odoo.com/documentation/17.0/es/_images/integration-level.png)

### Etiquetas para operaciones multietapa[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html#labels-for-multi-step "Enlazar permanentemente con este título")

Para las empresas que utilizan [entrega en dos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html) o en [tres pasos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/delivery_three_steps.html) es posible configurar la impresión de las etiquetas después de validar la operación de recolección o empaque. Vaya a Inventario ‣ Configuración ‣ Tipos de operaciones y elija la operación correspondiente.

Seleccione la casilla Imprimir etiqueta en la página de configuración del tipo de operación. Habilitar la función asegura que la etiqueta de envío externo se imprima al validar esta operación.

 Example

Para la [entrega en dos pasos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html), donde los productos se colocan directo en los paquetes durante la recolección, las empresas pueden imprimir las etiquetas de envío durante la recolección en lugar de durante la entrega. Además, Odoo tiene la flexibilidad de permitir que los usuarios habiliten la función Imprimir etiqueta durante la operación de `recolección`.

![Habilitar la función "Imprimir etiqueta".](https://www.odoo.com/documentation/17.0/es/_images/pick-print-label.png)

## Imprimir etiquetas de envío[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html#print-tracking-labels "Enlazar permanentemente con este título")

Las etiquetas de seguimiento se imprimen al validar ciertas operaciones. Por ejemplo, validar una orden de entrega genera una etiqueta de seguimiento en el chatter de forma predeterminada.

 Nota

Si se trata de empresas que utilizan la entrega en dos o tres pasos, consulte la sección relacionada con la [impresión de etiquetas para operaciones multietapa](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html#inventory-shipping-receiving-picking-config) para obtener más información sobre cómo imprimir la etiqueta luego de validar una operación de recolección o empaque.

Si tiene instaladas las aplicaciones _Ventas_ e _Inventario_, primero vaya a Ventas y abra la cotización u orden de venta correspondiente. Una vez allí [agregue el costo de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html#inventory-shipping-receiving-add-shipping-quote) a la orden. Después vaya a la orden de entrega relacionada (u otro tipo de operación si usa entrega multietapa) para validar la operación e imprimir la etiqueta.

Si solo tiene la aplicación _Inventario_ instalada, cree las órdenes de envío desde la aplicación Inventario, [agregue al transportista externo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html#inventory-shipping-receiving-validate-print-label) en el campo Transportista y valide la orden de entrega.

### Agregar el envío a la cotización[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html#add-shipping-on-quotation "Enlazar permanentemente con este título")

Para generar una etiqueta de rastreo para una orden, primero cree una cotización en Ventas ‣ Órdenes ‣ Cotizaciones, haga clic en Nuevo y llene el formulario de cotización. Después, haga clic en Agregar envío en la esquina inferior derecha de la cotización.

![Visualización el botón "Agregar envío" en la cotización.](https://www.odoo.com/documentation/17.0/es/_images/add-shipping-button.png)

Esta acción abrirá una ventana emergente, seleccione el transportista deseado en el menú desplegable Método de envío. El campo Peso total de la orden se completa en automático con el [peso de los productos en ella](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-weight). Modifique este campo para sobrescribir el peso previsto y úselo para estimar el costo de envío.

Después, haga clic en Obtener tarifa para visualizar el monto que pagará el cliente al transportista externo por el envío en el campo Costo.

 Importante

Si al hacer clic en Obtener tarifa aparece un error, asegúrese de que la [dirección del almacén](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-source-address) y el [peso de los productos de la orden](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-weight) estén bien configurados.

Haga clic en Agregar para agregar los costos a la cotización, que está enlistada como [producto de entrega configurado](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/delivery_method.html#inventory-shipping-receiving-delivery-product). Finalmente, haga clic en Confirmar en la cotización y haga clic en el botón inteligente Entrega para ingresar a la [|orden de envío|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html#id2).

![Visualización de la ventana emergente "Obtener tarifa".](https://www.odoo.com/documentation/17.0/es/_images/get-rate.png)

 Truco

Si no cuenta con la aplicación _Ventas_ instalada, especifique el transportista. Vaya a Inventario, diríjase a la orden de entrega y haga clic en la pestaña Información adicional.

![Mostrar la pestaña "información adicional" de la orden de entrega.](https://www.odoo.com/documentation/17.0/es/_images/additional-info-tab.png)

### Validar la orden de entrega[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html#validate-delivery-order "Enlazar permanentemente con este título")

En un formulario de orden de entrega, vaya a la pestaña Información adicional para asegurarse de que el transportista externo se agregó al campo Transportista.

 Importante

Si la aplicación _Ventas_ no está instalada, el transportista se configura en el campo Transportista.

Después de que los artículos en la orden se hayan empaquetado, haga clic en Validar para obtener el número de rastreo y generar una etiqueta de envío.

 Nota

Cree o seleccione una orden de envío existente en la aplicación Inventario y seleccione la tarjeta órdenes de envío.

El número Referencia de rastreo se genera en la pestaña Información adicional de la orden de entrega. Haga clic en el botón inteligente Seguimiento para acceder al enlace de seguimiento del sitio web del transportista.

La etiqueta de rastreo se encuentra en formato PDF en el chatter.

![Visualización de la etiqueta de envío generada en el chatter.](https://www.odoo.com/documentation/17.0/es/_images/shipping-label.png)

 Nota

Para envío de múltiples paquetes, se genera una etiqueta por paquete. Cada etiqueta aparece en el chatter.

![Etiqueta de ejemplo generada desde el conector de envío de Odoo con FedEx.](https://www.odoo.com/documentation/17.0/es/_images/sample-label.png)

Etiqueta de ejemplo generada desde el conector de envío de Odoo con FedEx.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html#id1 "Enlace permanente a esta imagen")

 Ver también

- [Facturación del costo de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/invoicing.html)
    
- [Envío en varios paquetes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/multipack.html)