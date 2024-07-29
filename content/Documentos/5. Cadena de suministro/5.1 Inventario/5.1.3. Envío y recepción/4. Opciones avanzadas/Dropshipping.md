La triangulación de envíos es una estrategia de cumplimiento de pedidos que permite que los vendedores envíen artículos directo de los proveedores a los clientes. Por lo general, un vendedor le compra un producto a un proveedor, lo almacena en su inventario y lo envía al cliente final una vez que se realiza un pedido. Mediante la triangulación de envíos, el proveedor es responsable de almacenar y enviar el artículo. Esto beneficia al vendedor al reducir los costos de inventario, incluido el precio de los almacenes operativos.

## Configurar productos para realizar una triangulación de envío[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/dropshipping.html#configure-products-to-be-dropshipped "Enlazar permanentemente con este título")

Para usar la triangulación como estrategia de cumplimiento, vaya a la aplicación Compra y seleccione Configuración ‣ Ajustes. En el encabezado Logística haga clic en la casilla Triangular y guarde para finalizar.

Luego, vaya a la aplicación Ventas, haga clic en Productos ‣ Productos y elija uno que ya existe o seleccione Nuevo para configurar uno. En la página del producto asegúrese de que las casillas Se puede vender y Se puede comprar están habilitadas.

![Habilitar las casillas de verificación "Se puede vender" y "Se puede comprar" en el formulario del producto.](https://www.odoo.com/documentation/17.0/es/_images/sold-purchased-checkboxes.png)

Haga clic en la pestaña Compra y especifique un proveedor y el precio al que venden el producto. Puede agregar varios proveedores, pero el que se encuentre en la parte superior de la lista será el que se seleccione de forma automática para las órdenes de compra.

![El formulario de producto con un proveedor especificado.](https://www.odoo.com/documentation/17.0/es/_images/product-vendor-config.png)

Por último, seleccione la pestaña Inventario y habilite la casilla Triangular en la sección Rutas.

![Habilitar la opción Triangular en la pestaña de inventario del producto.](https://www.odoo.com/documentation/17.0/es/_images/enable-dropship-route.png)

 Nota

Aunque no es necesario activar la ruta comprar además de la ruta triangulación de pedidos, si lo hace podrá hacer triangulación del pedido con el producto, o comprarlo directamente.

## Completar órdenes mediante el uso de triangulación de envíos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/dropshipping.html#fulfill-orders-using-dropshipping "Enlazar permanentemente con este título")

Una solicitud de cotización asociada para comprar el producto al proveedor se genera en automático al crear una orden de venta para un producto de envío directo. Puede ver las órdenes de venta en la aplicación Ventas si selecciona Órdenes ‣ Órdenes. Haga clic en el botón inteligente Compra ubicado en la parte superior derecha de una orden de venta para ver la solicitud de cotización asociada.

![Una orden de venta triangulada con el botón inteligente Compra en la esquina superior derecha.](https://www.odoo.com/documentation/17.0/es/_images/dropship-sales-order.png)

Al confirmar la solicitud de cotización, esta se convierte en una orden de compra, se crea un recibo de triangulación y se vincula. El recibo se puede ver al hacer clic en el botón inteligente Triangular en la esquina superior derecha del formulario de la orden de compra.

![Una orden de compra triangulada con el botón inteligente Recepción en la esquina superior derecha.](https://www.odoo.com/documentation/17.0/es/_images/dropship-purchase-order.png)

El recibo de la triangulación mostrará al Proveedor o contactos en la sección Ubicación de origen y al Cliente o contacto en la sección Ubicación de destino. Después de que el cliente reciba el producto, haga clic en el botón Validar en la parte superior izquierda del recibo de triangulación para confirmar la cantidad entregada.

![Validar el recibo de triangulación después de la entrega.](https://www.odoo.com/documentation/17.0/es/_images/validate-dropship-receipt.png)

Para ver todas las órdenes trianguladas, vaya al tablero de información general en Inventario y haga clic en el botón turquesa con el número por procesar en la tarjeta de triangulación.

![Haga clic en el botón verde de la tarjeta de triangulación para ver todas las órdenes trianguladas.](https://www.odoo.com/documentation/17.0/es/_images/view-all-dropship-orders.png)