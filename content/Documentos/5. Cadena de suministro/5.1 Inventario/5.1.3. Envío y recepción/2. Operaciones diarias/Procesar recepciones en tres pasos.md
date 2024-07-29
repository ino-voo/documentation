# Procesar recepciones en tres pasos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_three_steps.html#process-receipts-in-three-steps "Enlazar permanentemente con este título")

Algunas empresas requieren de un proceso de control de calidad antes de recibir los bienes de los proveedores. Para hacerlo, Odoo cuenta con un proceso de tres pasos.

En el proceso de recepción en tres pasos, se reciben los productos en un área de entrada y luego se transfieren a un área de calidad para su inspección. Los productos que pasan la inspección de calidad se transfieren a las existencias. Los productos no se podrán procesar hasta que salgan del área de calidad y se muevan a las existencias.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_three_steps.html#configuration "Enlazar permanentemente con este título")

Odoo está configurado para [recibir y enviar bienes en un paso](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#inventory-receipts-delivery-one-step) de manera predeterminada, entonces deberá cambiar la configuración para utilizar las recepciones en tres pasos. Primero, asegúrese de que la opción _Rutas multietapa_ esté habilitada en Inventario ‣ Configuración ‣ Ajustes ‣ Almacén. Tenga en cuenta que al activar las Rutas multietapa también activará las _ubicaciones de almacenamiento_.

![Active las rutas multietapas y las ubicaciones de almacenamiento en los ajustes de Inventario.](https://www.odoo.com/documentation/17.0/es/_images/receipts-three-steps-multi-step-routes.png)

A continuación, es necesario configurar el almacén para las recepciones en tres etapas. Para ello, vaya a la aplicación de inventario ‣ Configuración ‣ Almacenes, y seleccione el almacén que desea editar. Al hacerlo, aparecerá el formulario de detalle de ese almacén en concreto.

En esa página de formulario de Almacén seleccione Recibir artículos en la ubicación de entrada, trasladar a control de calidad y luego llevar a existencias (3 pasos) para Envíos a recibir.

![Establezca los envíos entrantes a recibir en tres pasos.](https://www.odoo.com/documentation/17.0/es/_images/receipts-three-steps-incoming-shipments.png)

Activar la recepción y entrega en tres pasos crea dos nuevas ubicaciones internas: _Entrada_ (WH/Entrada) y un _Control de calidad_ (WH/Control de calidad). Para cambiar el nombre de estas ubicaciones, vaya a la aplicación Inventario ‣ Configuración ‣ Ubicaciones, haga clic en la ubicación para la que desea modificar (o actualizar) el nombre.

## Recibir en 3 pasos (entrada + control de calidad + existencias)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_three_steps.html#receive-in-three-steps-input-quality-stock "Enlazar permanentemente con este título")

### Crear una orden de compra[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_three_steps.html#create-a-purchase-order "Enlazar permanentemente con este título")

Para crear una nueva cotización, vaya a la aplicación Ventas ‣ Nuevo, se abrirá una página con un formulario de cotización en blanco. Una vez allí, seleccione un cliente, agregue un producto almacenable y haga clic en Confirmar orden.

Aparecerá un botón inteligente de Recepción en la parte superior derecha, estará asociada a una orden de compra. Al hacer clic en el botón inteligente de Recepción, aparecerá la orden de recepción.

![Después de confirmar una orden de compra, aparecerá un botón inteligente de recepción.](https://www.odoo.com/documentation/17.0/es/_images/receipts-three-steps-smart-button.png)

### Procesar una recepción[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_three_steps.html#process-a-receipt "Enlazar permanentemente con este título")

Una vez que se confirma la orden de compra, se genera una operación de recepción (`WH/Entrada`) lista para procesar.

Es posible confirmar la recepción desde el formulario de compra original o puede acceder desde la aplicación Inventario, ahí deberá buscar la tarjeta de las tareas de recepción.

Haga clic en el botón # por procesar para abrir todas las recepciones por procesar, después haga clic en la recepción asociada con la orden de compra anterior.

Haga clic en Validar para validar la recepción y mover el producto a la ubicación de destino que es WH/Entrada.

![Operación de recepción para el movimiento de un producto a la ubicación WH/Entrada.](https://www.odoo.com/documentation/17.0/es/_images/receipts-three-steps-receipt-form.png)

### Procesar un traslado a Control de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_three_steps.html#process-a-transfer-to-quality-control "Enlazar permanentemente con este título")

La operación de traslado interno para mover el producto a control de calidad estará lista para procesarla una vez que valide la recepción.

Regrese al tablero de Información general de Inventario con las migas de pan y busque la tarjeta de las tareas de traslados internos.

Seleccione el botón # por procesar para abrir todos los traslados internos por procesar, después seleccione el traslado interno relacionado con el recibo validado.

Después haga clic en Validar para completar el traslado y mover el producto de WH/Entrada a WH/Control de calidad.

![Traslado interno del producto a la zona de control de calidad.](https://www.odoo.com/documentation/17.0/es/_images/receipts-three-steps-internal-transfer.png)

## Procesar un traslado a existencias[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_three_steps.html#process-a-transfer-to-stock "Enlazar permanentemente con este título")

Otra operación de traslado interno para mover el producto a las existencias del almacén estará lista para procesarla una vez que valide el traslado interno para moverlo a control de calidad.

Haga clic en SuEmpresa: traslados internos de las migas de pan para abrir la lista con todos los traslados internos a procesar. Después, seleccione el nuevo traslado interno para mover el producto de `WH/Control de calidad` a `WH/Existencias`.

Después haga clic en Validar para completar el traslado y mover el producto de WH/Control de calidad a WH/Existencias.

![Traslado interno del producto a las existencias del almacén.](https://www.odoo.com/documentation/17.0/es/_images/receipts-three-steps-second-transfer.png)