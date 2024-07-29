Algunas empresas procesan altas cantidades de entregas todos los días y muchas de ellas incluyen varios productos o necesitan un embalaje especial. Para que este proceso sea eficiente, se necesita un paso de embalaje antes de enviar los productos. Odoo tiene un proceso de tres pasos para entregar los productos.

En el proceso de entrega de tres pasos predeterminado, los productos que forman parte de una orden de entrega se recolectan en el almacén según su estrategia de remoción y se llevan a una zona de empaquetado. Después de que los artículos se empaquetaron en dentro de los distintos envíos en la zona correspondiente, se llevan a una ubicación de salida antes de enviarlos. Es posible modificar estos pasos si no se ajustan a las necesidades del negocio.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/delivery_three_steps.html#configuration "Enlazar permanentemente con este título")

Odoo está configurado de forma predeterminada para [recibir y enviar bienes en un solo paso](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#inventory-receipts-delivery-one-step), así que deberá modificar los ajustes para utilizar las recepciones en tres pasos. Primero, asegúrese de que la opción _Rutas multietapa_ se encuentra habilitada en Inventario ‣ Configuración ‣ Ajustes ‣ Almacén. Tenga en cuenta que al activar las rutas multietapa también activará las _ubicaciones de almacenamiento_.

![Activar las rutas multietapa y las ubicaciones de almacenamiento en los ajustes de la aplicación Inventario.](https://www.odoo.com/documentation/17.0/es/_images/delivery-three-steps-multi-step-routes.png)

Después, debe configurar el almacén para las entregas en tres pasos. Vaya a la aplicación Inventario ‣ Configuración ‣ Almacenes y haga clic en el almacén que desee. Luego, seleccione Empaquetar artículos, enviar productos a ubicación de salida y enviar (3 pasos) para los envíos salientes.

![Establecer la opción de envío saliente para entregar en tres pasos.](https://www.odoo.com/documentation/17.0/es/_images/delivery-three-steps-outgoing-shipments.png)

Activar la recepción y entrega en tres pasos crea dos nuevas ubicaciones internas: una _zona de empaquetado_ (WH/Zona de empaquetado) y una de _salida_ (WH/Salida). Para cambiar el nombre de estas ubicaciones, vaya a la aplicación Inventario ‣ Configuración ‣ Ubicaciones, haga clic en la ubicación que desea modificar y actualice el nombre.

## Entregar en 3 pasos (recolección, empaquetado y envío)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/delivery_three_steps.html#deliver-in-three-steps-pick-pack-ship "Enlazar permanentemente con este título")

### Crear una orden de venta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/delivery_three_steps.html#create-a-sales-order "Enlazar permanentemente con este título")

Para crear una nueva cotización, vaya a la aplicación Ventas ‣ Nuevo, se abrirá un formulario de cotización en blanco. Una vez allí, seleccione un cliente, agregue un producto almacenable y haga clic en Confirmar.

El botón inteligente Entrega aparece en la parte superior derecha del formulario de cotización. Al hacer clic en él se abrirá la orden de recolección para mover el producto de `WH/Existencias` a `WH/Zona de embalaje`.

![Después de confirmar la orden de venta, aparece el botón inteligente de entrega que muestra sus tres artículos  relacionados.](https://www.odoo.com/documentation/17.0/es/_images/delivery-three-steps-smart-button.png)

### Procesar una recolección[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/delivery_three_steps.html#process-a-picking "Enlazar permanentemente con este título")

La orden de recolección se creará luego de confirmar la orden de venta. Para visualizar la recolección, vaya a Inventario y busque la tarjeta de tarea Recolección en el tablero de Información general de Inventario.

Haga clic en el botón # por procesar, este abrirá la orden de recolección generada a partir de la orden de venta confirmada con anterioridad.

Haga clic en la recolección para procesarla. Si hay existencias del producto, Odoo lo reservará en automático. Haga clic en Validar para marcar la recolección como completada y completar el traslado a la zona de embalaje.

![Operación de recolección de órdenes en la que aparece la ubicación de origen y de destino.](https://www.odoo.com/documentation/17.0/es/_images/delivery-three-steps-picking-order.png)

### Procesar un empaquetado[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/delivery_three_steps.html#process-a-packing "Enlazar permanentemente con este título")

La orden de embalaje estará lista para su procesamiento después de validar la recolección. Haga clic en Información general de Inventario y busque la tarjeta de las tareas de empaquetado en el tablero.

Haga clic en el botón # por procesar (en este caso, 1 por procesar), este abrirá la orden de empaquetado generada a partir de la orden de venta confirmada con anterioridad.

Haga clic en la orden de empaquetado asociada a la orden de ventas, luego haga clic en Validar para completar el empaquetado.

![Operación de embalaje de órdenes en la que aparece la ubicación de origen y de destino.](https://www.odoo.com/documentation/17.0/es/_images/delivery-three-steps-packing-order.png)

Una vez validada la orden de empaquetada, el producto deja la ubicación de WH/Zona de empaquetado y se mueve a la ubicación de WH/Ubicación de salida. Luego, el estado del documento cambiará a Hecho.

### Procesar una entrega[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/delivery_three_steps.html#process-a-delivery "Enlazar permanentemente con este título")

La orden de entrega estará lista para su procesamiento después de validar la orden de embalaje. Regrese a la orden de venta original para procesar la entrega, vaya a Ventas y seleccione la orden de venta creada con anterioridad.

 Truco

_También_ es posible acceder a las órdenes de entrega desde Inventario ‣ Operaciones ‣ Entregas.

El botón inteligente Entrega ahora indica que hay 3 traslados, no solo uno. Al hacer clic en Entrega aparecerán las tres operaciones relacionadas con la orden de ventas: la recolección, el embalaje y la entrega.

Haga clic en el traslado de entrega (WH/SALIDA) para abrir la orden correspondiente y luego haga clic en Validar.

![Haga clic en validar en la orden de entrega para transferir el producto de la ubicación de salida a la ubicación del cliente.](https://www.odoo.com/documentation/17.0/es/_images/delivery-three-steps-delivery-order.png)

Una vez validada la orden de entrega, el producto deja la WH/Ubicación de salida y se dirige a la ubicación de los Partners/Clientes. Luego, el estado del documento cambiará a Hecho.