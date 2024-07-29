Los envíos entrantes y salientes están configurados de forma predeterminada para procesarse en un solo paso en la aplicación _Inventario_ de Odoo. Es decir, las compras se recibirán directo en el inventario y las entregas se trasladarán a las existencias de los clientes.

 Truco

**No** es necesario que configure los envíos entrantes y salientes con el mismo número de pasos.

Por ejemplo, puede configurar los ajustes de un almacén para recibir los productos en un solo paso y entregarlos en tres pasos (recolección + empaquetado + envío).

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#configuration "Enlazar permanentemente con este título")

Vaya a Inventario ‣ Configuración ‣ Almacenes para configurar recepciones y entregas en un solo paso y seleccione el almacén que desea editar.

En la pestaña Configuración del almacén, configure Envíos entrantes en Recibir artículos directamente (1 paso) y configure Envíos salientes en Entregar artículos directamente (1 paso).

![Envíos entrantes y salientes configurados con un solo paso en el formulario de almacén.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-one-step-warehouse-settings.png)

 Nota

En Odoo, la recepción y entrega en un solo paso es la opción predeterminada para los envíos entrantes y salientes, así que la función _Rutas multietapa_ _no_ es necesaria.

Sin embargo, la función **debe** estar habilitada para que los ajustes de envíos aparezcan en el formulario del almacén.

Vaya a Inventario ‣ Configuración ‣ Ajustes para activar la función _Rutas multietapa_. Diríjase a la sección Almacén, seleccione la casilla junto a Rutas multietapa y haga clic en Guardar. Esta acción también habilita la función Ubicaciones de almacenamiento.

## Recibir bienes directamente (1 paso)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#receive-goods-directly-1-step "Enlazar permanentemente con este título")

Al recibir los productos en un solo paso, estos se trasladarán de la ubicación del proveedor a las existencias de almacén en la base de datos de forma inmediata después de validar una orden de compra.

### Crear una orden de compra[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#create-purchase-order "Enlazar permanentemente con este título")

Vaya a la aplicación Compra para crear una orden de compra y haga clic en Nuevo. Esta acción abrirá un formulario vacío para una solicitud de cotización.

Agregue el proveedor en el campo correspondiente y complete los campos de la solicitud de cotización según sea necesario.

![Una nueva solicitud de cotización con su formulario completo.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-one-step-new-rfq.png)

En la pestaña Productos, haga clic en Agregar un producto y seleccione el que desea añadir a la solicitud de cotización.

Una vez que haya terminado, haga clic en Confirmar orden. Esta acción mueve la solicitud de cotización a la etapa de Orden de compra.

El botón inteligente Recepción aparece en la parte superior del formulario después de confirmar la orden de compra. Al hacer clic en él, se abre el formulario de recepción de almacén (WH/IN).

![Botón inteligente de recepción en el formulario de una orden de compra confirmada.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-one-step-receipt-smart-button.png)

### Procesar una recepción[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#process-receipt "Enlazar permanentemente con este título")

Desde el formulario de recepción de almacén puede recibir los productos ordenados. Para recibirlos, haga clic en Validar, después la recepción pasa a la etapa Hecho.

![Recibo de almacén validado en la etapa Hecho.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-one-step-done-receipt.png)

Regrese a la orden de compra (con las migas de pan ubicadas en la parte superior del formulario) para ver su formulario. En la línea del producto, la cantidad en la columna Recibido ahora coincide con la cantidad ordenada.

## Entregar bienes directamente (1 paso)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#deliver-goods-directly-1-step "Enlazar permanentemente con este título")

Al entregar los productos un solo paso, estos se trasladarán del almacén a la ubicación del cliente en la base de datos justo después de validar una orden de venta.

### Crear una orden de venta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#create-sales-order "Enlazar permanentemente con este título")

Vaya a la aplicación Ventas para crear una orden de venta y haga clic en Nuevo. Esta acción abrirá un formulario vacío para una cotización de venta.

Agregue el cliente en el campo correspondiente y complete los campos de cotización de venta según sea necesario.

![Una nueva cotización de venta con su formulario completo.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-one-step-new-sales-order.png)

En la pestaña Productos, haga clic en Agregar un producto y seleccione el que desea añadir a la cotización de la orden de venta.

Una vez que haya terminado, haga clic en Confirmar orden. Esta acción mueve la cotización a la etapa de Orden de venta.

El botón inteligente Recepción aparece en la parte superior del formulario después de confirmar la orden de venta. Al hacer clic en él, se abre el formulario de recepción de almacén (WH/OUT).

![Botón inteligente de entrega en el formulario de una orden de venta confirmada.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-one-step-delivery-button.png)

### Procesar una entrega[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#process-delivery "Enlazar permanentemente con este título")

Los productos que el cliente ordenó se pueden entregar desde el almacén desde el formulario de entrega del almacén. Para ello, cambie el valor en el campo Cantidad para que coincida con la cantidad ordenada en el campo Demanda.

Una vez que haya terminado, haga clic en Validar. Después de esto la orden de entrega se mueve a la etapa Hecho.

![Orden de entrega validada en la etapa Hecho.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-one-step-done-delivery.png)

Regrese a la orden de venta (con las migas de pan ubicadas en la parte superior del formulario) para ver su formulario. En la línea del producto, la cantidad en la columna Entregado ahora coincide con la cantidad ordenada.

 Ver también

[Envíos entrantes y órdenes de entrega](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/shipments_deliveries.html)