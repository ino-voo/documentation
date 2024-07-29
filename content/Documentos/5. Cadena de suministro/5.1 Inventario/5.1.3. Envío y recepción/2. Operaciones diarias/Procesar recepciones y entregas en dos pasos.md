Es posible que, según las necesidades de una empresa, recibir y enviar productos dentro y fuera del almacén requiera de operaciones de varios pasos. Es posible hacer esto en la aplicación _Inventario_ con las _rutas multietapa_.

En el proceso de recepción de dos pasos, los productos se reciben en un área de entrada y después se trasladan a las existencias. Este tipo de proceso para envíos entrantes podría ser útil para los almacenes que tienen ubicaciones de almacenamiento específicas, como congeladores, refrigeradores, áreas cerradas con llave y pasillos o estantes especiales.

Puede organizar los productos de acuerdo al lugar en donde se guardarán y los empleados pueden almacenar todos los productos en una ubicación en específico. Los productos _no_ estarán disponibles para ningún otro proceso hasta después de que los trasladen a las existencias.

Durante el proceso de entrega de dos pasos, primero es necesario recolectar los productos desde la ubicación correspondiente en el almacén para luego trasladarlos a la ubicación de salida antes de enviárselos al cliente.

Este puede ser útil para las empresas que usan las estrategias de remoción conocidas como primeras entradas, primeras salidas (PEPS), últimas entradas, primeras salidas (UEPS) o primero en expirar, primero en salir (FEFO).

 Truco

**No** es necesario que configure los envíos entrantes y salientes con el mismo número de pasos.

Por ejemplo, puede configurar los ajustes de un almacén para recibir los productos en dos pasos (entrada + existencias) y entregarlos en tres pasos (recolección + empaquetado + envío).

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html#configuration "Enlazar permanentemente con este título")

Los envíos entrantes y salientes están configurados de forma predeterminada para procesarse en un solo paso en la aplicación _Inventario_ de Odoo. Para cambiar estos ajustes es necesario que habilite la función _Rutas multietapa_.

Vaya a Inventario ‣ Configuración ‣ Ajustes para activar la función _Rutas multietapa_. Diríjase a la sección Almacén, seleccione la casilla junto a Rutas multietapa y haga clic en Guardar. Esta acción también habilita la función Ubicaciones de almacenamiento.

![La función Rutas multietapa habilitada en los ajustes de la aplicación Inventario.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-two-steps-settings.png)

Vaya a Inventario ‣ Configuración ‣ Almacenes para configurar recepciones y entregas en dos pasos en un almacén y seleccione el que desea editar.

En la pestaña Configuración del almacén, configure Envíos entrantes en Recibir artículos en la ubicación de entrada y luego llevar a existencias (2 pasos) y configure Envíos salientes en Enviar artículos a ubicación de salida y entregar (2 pasos).

![Envíos entrantes y salientes configurados con dos pasos en el formulario de almacén.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-two-steps-shipments.png)

 Nota

Seleccionar recepciones y entregas en dos pasos crea dos nuevas ubicaciones de almacén, _Entrada_ y _Salida_, en la base de datos en automático con los nombres `WH/Entrada` y `WH/Salida` según corresponde.

Para renombrar o editar estas ubicaciones, vaya a Inventario ‣ Configuración ‣ Ubicaciones y seleccione la ubicación correspondiente.

En el formulario de la ubicación, modifique el nombre de la ubicación y haga cualquier otro cambio necesario.

## Procesar una recepción en dos pasos (entrada + inventario)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html#process-receipt-in-two-steps-input-stock "Enlazar permanentemente con este título")

Al recibir los productos en dos pasos, primero se mueven de la ubicación del proveedor a una ubicación de entrada, después se trasladan de la ubicación de entrada al almacén en la base de datos luego de validar la orden de compra y el traslado interno.

### Crear una orden de compra[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html#create-purchase-order "Enlazar permanentemente con este título")

Vaya a la aplicación Compra para crear una orden de compra y haga clic en Nuevo. Esta acción abrirá un formulario vacío para una solicitud de cotización.

Agregue el proveedor en el campo correspondiente y complete los campos de la solicitud de cotización según sea necesario.

![Una nueva solicitud de cotización completada del proveedor.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-two-steps-new-rfq.png)

En la pestaña Productos, haga clic en Agregar un producto y seleccione el que desea añadir a la solicitud de cotización.

Una vez que haya terminado, haga clic en Confirmar orden. Esta acción mueve la solicitud de cotización a la etapa de Orden de compra.

El botón inteligente Recepción aparece en la parte superior del formulario después de confirmar la orden de compra. Al hacer clic en él, se abre el formulario de recepción de almacén (WH/IN).

![Botón inteligente de entrega para una orden de compra validada.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-two-steps-smart-button.png)

 Truco

Si se trata de una empresa que tiene varios almacenes con distintas configuraciones de pasos, **debe** especificar la _ubicación de entrada_ correcta vinculada al almacén de dos pasos en el campo Entregar a del formulario de la orden de compra.

Esto es posible al seleccionar el almacén del menú desplegable que incluye la etiqueta `Recepciones` al final de su nombre.

### Procesar una recepción[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html#process-receipt "Enlazar permanentemente con este título")

Desde el formulario de recepción de almacén puede recibir los productos ordenados. Para recibirlos, haga clic en Validar, después la recepción pasa a la etapa Hecho y los productos se mueven a la ubicación WH/Entrada.

![Formulario de recepción para los productos ordenados a un proveedor.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-two-steps-receipt-form.png)

Regrese a la orden de compra (con las migas de pan ubicadas en la parte superior del formulario) para ver su formulario. En la línea del producto, la cantidad en la columna Recibido ahora coincide con la cantidad ordenada.

### Procesar traslados internos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html#process-internal-transfer "Enlazar permanentemente con este título")

El traslado interno se creará y estará listo para validarlo una vez que valide la recepción.

Vaya a Inventario y busque la tarjeta de la tarea Traslados internos, luego busque el traslado correspondiente.

Haga clic en el botón # por procesar en la tarjeta de la tarea para abrir una lista con todos los traslados internos por procesar y seleccione el traslado relacionado al recibo validado con anterioridad.

Después haga clic en Validar para completar el traslado y mover el producto de WH/Entrada a WH/Existencias.

Después de validar el traslado, los productos entran al inventario y están disponible para entregárselos al cliente o usarlos en órdenes de fabricación.

![Formulario de traslado interno  para los productos ordenados a un proveedor.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-two-steps-internal-transfer.png)

## Procesar una orden de envío en dos pasos (recolección + envío)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html#process-delivery-order-in-two-steps-pick-ship "Enlazar permanentemente con este título")

Al entregar los productos en dos pasos, estos se mueven del almacén a una ubicación de salida, después se mueven de la ubicación de salida a una ubicación de cliente en la base de datos luego de validar la orden de recolección y de entrega.

### Crear una orden de venta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html#create-sales-order "Enlazar permanentemente con este título")

Vaya a la aplicación Ventas para crear una orden de venta y haga clic en Nuevo. Esta acción abrirá un formulario vacío para una cotización de venta.

Agregue el cliente en el campo correspondiente y complete los campos de cotización de venta según sea necesario.

![Un formulario completado de una nueva orden de venta.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-two-steps-new-sales-order.png)

En la pestaña Líneas de la orden, haga clic en Agregar un producto y seleccione el que desea añadir a la cotización de la orden de venta.

Una vez que haya terminado, haga clic en Confirmar orden. Esta acción mueve la cotización a la etapa de Orden de venta.

El botón inteligente Recepción aparece en la parte superior del formulario después de confirmar la orden de venta. Al hacer clic en él, se abre el formulario de recepción de almacén (WH/OUT).

![Botón inteligente de entrega en el formulario de una orden de venta validada.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-two-steps-delivery-button.png)

### Procesar recolecciones[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html#process-picking "Enlazar permanentemente con este título")

Una vez que se confirma la orden de venta, se genera una orden de recolección lista para procesar.

Para completar la recolección, vaya a Inventario y busque la tarjeta de la tarea Recolección en el tablero Información general. También es posible acceder a la orden de recolección desde el botón inteligente Entrega ubicado en la pate superior del formulario de la orden de venta.

Una vez en la página Resumen de inventario, haga clic en el botón # por procesar en la tarjeta de la tarea Recolección. Esta acción abre una lista con todas las recolecciones por procesar.

Haga clic en la operación de recolección (WH/RECOLECCIÓN) asociada con la orden de venta para abrirla.

![Formulario de orden de recolección para los productos incluidos en la orden de venta.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-two-steps-picking-form.png)

Configure la cantidad de forma manual, cambié el valor en la columna Cantidad para que coincida con el de la columna Demanda.

Después haga clic en Validar para completar la recolección y mover el producto de WH/Existencias a WH/Salida.

### Procesar una entrega[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html#process-delivery "Enlazar permanentemente con este título")

Después de validar la recolección, se crea una orden de entrega lista para procesar. Al hacer clic en el botón inteligente Entrega del formulario de la orden de venta abre la nueva orden creada.

También es posible ir a la página del resumen de Inventario con las migas de pan para ver la orden de entrega. Busque la tarjeta de la tarea Órdenes de entrega.

Haga clic en el botón # por procesar para abrir una lista con todas las órdenes de entrega por procesar y seleccione la orden relacionada a la recolección validada con anterioridad.

![Formulario de orden de entrega para los productos ordenados por el cliente.](https://www.odoo.com/documentation/17.0/es/_images/receipts-delivery-two-steps-delivery-order.png)

Para entregar los productos, cambie el valor en el campo Cantidad para que coincida con la cantidad ordenada en el campo Demanda.

Una vez que haya terminado, haga clic en Validar. Después de esto la orden de entrega se mueve a la etapa Hecho.

 Ver también

[Envíos entrantes y órdenes de entrega](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/shipments_deliveries.html)