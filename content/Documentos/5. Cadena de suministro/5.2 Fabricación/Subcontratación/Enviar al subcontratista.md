En fabricación, la subcontratación es el proceso que una empresa lleva a cabo cuando contrata a un fabricante externo, o subcontratista, para que fabrique los productos que luego venderá la empresa contratante.

En Odoo, la ruta _Enviar al subcontratista al ordenar_ se utiliza para comprar los componentes necesarios para un producto subcontratado a un proveedor y que este se los entregue al subcontratista cuando se confirma una orden de compra con ese producto.

El subcontratista utiliza los componentes para fabricar el producto deseado antes de enviarlo de vuelta a la empresa contratante.

 Importante

Es necesario entender las diferencias entre las rutas _Triangular_ y _Enviar al subcontratista al ordenar_. Ambas rutas implican envío directo, pero se utilizan con distintos propósitos.

La ruta _Triangular_ se utiliza para comprar productos a un proveedor y que este se encargue de enviarlos al consumidor final.

La ruta _Enviar al subcontratista al ordenar_ se utiliza para comprar componentes a un proveedor y que este los envíe directo a un subcontratista. De forma predeterminada, el subcontratista envía los productos terminados a la empresa contratante.

Sin embargo, es posible combinar las rutas _Triangular_ y _Enviar al subcontratista al ordenar_ para utilizarlas en el mismo producto. En este flujo de trabajo, los componentes se envían directo al subcontratista y este envía el producto terminado directo al consumidor final.

Para ello debe seguir los pasos uno a cinco en la [sección de flujo de trabajo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#manufacturing-workflows-subcontracting-dropship) de este documento.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#configuration "Enlazar permanentemente con este título")

Para utilizar la ruta _Enviar al subcontratista al ordenar_, vaya a Fabricación ‣ Configuración ‣ Ajustes y, en la sección Operaciones, seleccione la casilla ubicada junto a Subcontratación.

Luego de habilitar la función de _subcontratación_ también es necesario configurar de manera adecuada el producto subcontratado, la lista de materiales del producto y los componentes que forman parte de ella.

### Configurar productos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#configure-product "Enlazar permanentemente con este título")

Para configurar un producto para la ruta _Enviar al subcontratista al ordenar_, vaya a Inventario ‣ Productos ‣ Productos y seleccione uno o créelo con el botón Nuevo.

Seleccione la pestaña Compra y agregue al subcontratista de los productos como proveedor. Haga clic en Agregar una línea, seleccione al subcontratista en el menú desplegable Proveedor y escriba el precio en el campo Precio.

Después, haga clic en la pestaña Inventario para configurar la ruta que determine qué ocurrirá con el producto terminado una vez que el subcontratista lo haya fabricado.

Asegúrese de que la ruta Comprar esté seleccionada si el producto terminado se devuelve a la empresa contratista. Además, seleccione la ruta Reabastecer sobre pedido (MTO) para crear una orden de compra en automático para el producto al confirmar una orden de venta, a menos que haya suficientes existencias para cumplir con la orden de compra.

Asegúrese de seleccionar solo la ruta triangulación si el subcontratista envía el producto terminado al cliente.

### Configurar listas de materiales[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#configure-bill-of-materials "Enlazar permanentemente con este título")

Para configurar una lista de materiales para la ruta _Enviar al subcontratista al ordenar_, haga clic en el botón inteligente Lista de Materiales en la página del producto y seleccione la LdM.

Como alternativa, vaya a Fabricación ‣ Productos ‣ Listas de materiales y seleccione la lista de materiales para el producto subcontratado.

 Ver también

Consulte la documentación de [lista de materiales](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html) para obtener información completa sobre su configuración.

En el campo Tipo de LdM seleccione la opción Subcontratación y después agregue uno o más subcontratistas en el campo Subcontratistas que aparece abajo.

![El campo "Tipo de LdM" en una lista de materiales configurada para fabricar el producto mediante subcontratación.](https://www.odoo.com/documentation/17.0/es/_images/bom-type1.png)

Por último, asegúrese de que todos los componentes necesarios están presentes en la pestaña Componentes. Para agregar un nuevo componente, haga clic en Agregar una línea, después, en el menú desplegable Componente seleccione el necesario y especifique la cantidad requerida en el campo correspondiente.

### Configurar componentes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#configure-components "Enlazar permanentemente con este título")

Para configurar los componentes para la ruta _Enviar al subcontratista al ordenar_, vaya a cada componente desde la lista de materiales y seleccione el nombre del componente en la pestaña Componentes, haga clic en el botón ➡️ (flecha derecha) que está del lado derecho del nombre.

Como alternativa también puede ir a cada componente desde Inventario ‣ Productos ‣ Productos y elegirlo.

En el formulario del producto de componente, seleccione la pestaña Compra y agregue un proveedor con el botón Agregar una línea, seleccione el proveedor en el campo Proveedor y agregue el precio al que venden el producto en el campo Precio. Este es el proveedor que envía los componentes al subcontratista después de comprarlos.

Después, seleccione la pestaña Inventario y elija Enviar al subcontratista al ordenar en la sección Rutas.

Repita este proceso en todos los componentes que se deben enviar al subcontratista de forma directa.

## Flujo de trabajo de la ruta Enviar al subcontratista al ordenar[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#dropship-subcontractor-on-order-workflow "Enlazar permanentemente con este título")

El flujo de trabajo de la ruta Enviar al subcontratista al ordenar consta de hasta seis pasos:

1. Crear una orden de venta para el producto subcontratado, esto creará una orden de compra del _subcontratista_ para adquirir su producto.
    
2. Confirmar la orden de compra creada en el paso anterior o crear una nueva. Esto crea una solicitud de cotización para comprar los componentes al proveedor, así como una orden de recepción o de triangulación.
    
3. Confirmar la solicitud de cotización para convertirla en una segunda orden de compra (_orden de compra_ del proveedor). Esto crea una orden de _envío directo al subcontratista_.
    
4. Procesar la orden de _triangulación al subcontratista_ una vez que el proveedor le envió los componentes al subcontratista.
    
5. Procesar la recepción después de que el subcontratista haya terminado de fabricar el producto subcontratado y lo envíe de vuelta a la empresa contratante **o** procesar la orden de triangulación para enviar el producto al cliente.
    
6. Si el flujo de trabajo se inició creando una orden de venta y el producto terminado no se envía directo al cliente final, procese la orden de entrega una vez que el producto haya sido enviado al cliente.
    

El número específico de pasos depende del motivo por el que le compra el producto subcontratado al subcontratista.

Si el motivo es cumplir con la orden específica del cliente, el proceso comienza con la creación de una orden de venta y termina con la entrega del producto al cliente o con el subcontratista enviándolo de forma directa.

Si el motivo es aumentar la cantidad de existencias disponibles, el proceso comienza con la creación de una orden de compra y termina con la recepción del producto en el inventario.

### Crear una orden de venta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#create-an-so "Enlazar permanentemente con este título")

Solo es necesario completar este paso si le compra el producto se compra al subcontratista para cumplir con alguna de las necesidades del cliente. Diríjase al siguiente paso si compra el producto para aumentar la cantidad disponible.

Para crear una nueva orden de venta, vaya a Ventas ‣ Órdenes ‣ Órdenes y haga clic en Nuevo.

Seleccione al cliente en el menú desplegable correspondiente. Después, haga clic en Agregar un producto en la pestaña Líneas de orden, seleccione el producto en el menú desplegable Producto y escriba el número adecuado en el campo Cantidad.

Haga clic en el botón correspondiente para confirmar la orden de venta, en ese momento aparecerá el botón inteligente Compra en la parte superior de la página. Esta es la orden de compra del _subcontratista_ o la orden de compra creada para adquirir el producto subcontratado del subcontratista.

 Nota

Una orden de venta para el producto solo crea una orden de compra de _subcontratista_ si la ruta _Reabastecer bajo pedido (MTO)_ está habilitada en la página del producto **y** el producto no tiene suficiente disponibilidad.

Si hay existencias disponibles, confirmar una orden de venta para el producto creará una orden de entrega porque Odoo asume que la orden de venta se cumple con las existencias en el almacén.

No ocurre lo mismo con los productos subcontratados que se envían directo al cliente final. En ese caso **siempre** se crea una orden de compra de _subcontratista_, incluso si hay disponibilidad.

### Procesar una orden de compra del subcontratista[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#process-subcontractor-po "Enlazar permanentemente con este título")

Si no creó una orden de compra de _subcontratista_ en el paso anterior, vaya a Compras ‣ Órdenes ‣ Órdenes de compra y haga clic en Nueva.

Complete la orden de compra, primero seleccione un subcontratista con el menú desplegable Proveedor.

En la pestaña Productos, haga clic en Agregar un producto para crear una nueva línea, después seleccione un producto fabricado por el subcontratista en el campo Producto y escriba el número correspondiente en el campo Cantidad.

Por último, haga clic en Confirmar orden para confirmar la orden de compra del _subcontratista_.

Al confirmar una orden de compra para un producto que necesita que envíe componentes a un subcontratista, entonces se crea una orden de recepción o triangulación de forma automática a la que puede acceder con el botón inteligente Recibo o Triangular que aparece en la parte superior de la orden de compra.

![Una orden de compra del subcontratista para un producto con ruta *Enviar al subcontratista al ordenar*, con el botón inteligente Recepción en la parte superior de la página.](https://www.odoo.com/documentation/17.0/es/_images/subcontractor-po1.png)

Además, se crea una solicitud de cotización para los componentes que se compran al proveedor y se envían al subcontratista. Sin embargo, esta solicitud **NO** se vincula en automático a la orden de compra del _subcontratista_.

Cuando la solicitud de cotización está confirmada y se convierte en una orden de compra del _proveedor_, se crea una orden de para _enviar al subcontratista_. Esta orden está vinculada tanto a la orden de compra del _proveedor_ como a la orden de compra del _subcontratista_.

### Confirmar solicitudes de cotización de los proveedores[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#confirm-vendor-rfq "Enlazar permanentemente con este título")

Vaya a Compra ‣ Órdenes ‣ Solicitudes de cotización para acceder a la solicitud de cotización creada al confirmar la _orden de compra_ del subcontratista. Seleccione la orden de cotización en la que aparece el proveedor correcto en el campo Proveedor y el número de referencia del recibo que se creó después de confirmar la orden de compra del subcontratista en el campo Documento origen.

En la solicitud de cotización, el campo Entregar a menciona Subcontratista de triangulación y en el campo Dirección de entrega aparece el nombre del subcontratista que recibirá los componentes.

Haga clic en Confirmar orden para convertir la solicitud de cotización en una _orden de compra_ de proveedor y confirmar la compra de componentes al proveedor. Después de esto aparecerá el botón inteligente Triangular en la parte superior de la _orden de compra_ del proveedor y el botón inteligente Reabastecer en la parte superior de la orden de compra* del subcontratista.

![Una orden de compra del proveedor para un producto con ruta *Enviar al subcontratista al ordenar*, con el botón inteligente Triangular en la parte superior de la página.](https://www.odoo.com/documentation/17.0/es/_images/vendor-po.png)

### Procesar la orden para enviar al subcontratista[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#process-dropship-subcontractor-order "Enlazar permanentemente con este título")

Una vez que el subcontratista haya recibido los componentes, vaya a Compra ‣ Órdenes ‣ Órdenes de compra, seleccione la orden de compra del proveedor o del subcontratista y haga clic en el botón inteligente Triangular o en el botón inteligente Reabastecer según corresponda.

Al hacer clic en cualquiera de los botones abrirá la orden para _enviar al subcontratista_. Haga clic en el botón Validar ubicado en la parte superior de la orden para confirmar que el subcontratista recibió los componentes.

### Procesar una recepción o una orden de envío directo (triangulación)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#process-receipt-or-dropship-order "Enlazar permanentemente con este título")

Una vez que el subcontratista haya fabricado el producto terminado, vaya a Compra ‣ Órdenes ‣ Órdenes de compra y seleccione la orden de compra del _subcontratista_.

Si es necesario recibir el producto subcontratado en el inventario, en cuanto llegue haga clic en el botón Recibir productos que está ubicado en la parte superior de la orden de compra del _subcontratista_ para abrir la recepción. Después, haga clic en Validar en la parte superior del recibo para registrar el producto en el inventario.

También puede seleccionar el botón inteligente Recibo ubicado en la parte superior de la orden de compra del _subcontratista_ y hacer clic en Validar en la parte superior de la recepción.

Si el proveedor debe enviar el producto subcontratado, seleccione el botón Triangular que se ubica en la parte superior de la página para abrir la orden correspondiente. Haga clic en Validar después de que el subcontratista haya enviado el producto al cliente.

### Procesar una orden de entrega[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html#process-delivery-order "Enlazar permanentemente con este título")

Si el flujo de trabajo de subcontratación fue iniciado por una orden de venta del cliente y el producto terminado **no** fue enviado de forma directa al cliente, sino que lo recibió la empresa contratante, es necesario enviar el producto al cliente y procesar la orden de entrega.

Una vez que haya enviado el producto al cliente, vaya a la aplicación Ventas y seleccione la orden de venta. Presione el botón inteligente Entrega ubicado en la parte superior de la página para abrir la orden de entrega, luego haga clic en Validar para confirmar que envió el producto al cliente.