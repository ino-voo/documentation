En fabricación, la subcontratación es el proceso que una empresa lleva a cabo cuando contrata a un fabricante externo, o subcontratista, para que fabrique los productos que luego venderá la empresa contratante.

En la subcontratación básica, el subcontratista es responsable de adquirir los componentes necesarios. Es decir, la empresa contratante solo tiene que preocuparse por lo que sucede con los productos subcontratados luego de su fabricación.

El flujo de trabajo para comprar un producto fabricado mediante subcontratación básica es similar al que utiliza con un proveedor cuando le compra un producto no subcontratado. La principal diferencia es la forma en que se configuran los productos subcontratados, además de que el proveedor tarda más en enviar los productos subcontratados porque primero debe fabricarlos.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#configuration "Enlazar permanentemente con este título")

Para usar subcontratación en Odoo, vaya a Fabricación ‣ Configuración ‣ Ajustes y, en la sección Operaciones, seleccione la casilla ubicada junto a Subcontratación. Haga clic en Guardar.

Luego de habilitar la función de subcontratación también es necesario configurar de manera adecuada el producto subcontratado y su lista de materiales.

### Configurar productos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#configure-product "Enlazar permanentemente con este título")

Para configurar un producto para la subcontratación básica, vaya a Inventario ‣ Productos ‣ Productos y seleccione uno o créelo con el botón Nuevo.

En el formulario del producto, vaya a la pestaña Compra y agregue al subcontratista de los productos como proveedor. Haga clic en Agregar una línea, seleccione al subcontratista en el menú desplegable Proveedor y escriba el precio en el campo Precio.

Después, haga clic en la pestaña Inventario y use el campo Rutas para configurar la ruta que determine qué ocurrirá con el producto terminado una vez que el subcontratista lo haya fabricado.

Asegúrese de que la ruta Comprar esté seleccionada si el producto terminado se devuelve a la empresa contratista. Además, seleccione la ruta Reabastecer sobre pedido (MTO) para crear una orden de compra en automático para el producto al confirmar una orden de venta, a menos que haya suficientes existencias para cumplir con la orden de compra.

Asegúrese de seleccionar **solo** la ruta triangulación si el subcontratista envía el producto terminado al cliente.

### Configurar listas de materiales[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#configure-bom "Enlazar permanentemente con este título")

Para configurar una lista de materiales para subcontratación básica, haga clic en el botón inteligente Lista de Materiales en el formulario del producto y seleccione la LdM deseada.

Como alternativa, vaya a Fabricación ‣ Productos ‣ Listas de materiales y seleccione la lista de materiales para el producto subcontratado.

 Ver también

Consulte la documentación de [lista de materiales](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html) para obtener información completa sobre su configuración.

En el campo Tipo de LdM seleccione la opción Subcontratación y después agregue uno o más subcontratistas en el campo Subcontratistas que aparece abajo.

![El campo "Tipo de LdM" en una lista de materiales configurada para fabricar el producto mediante subcontratación.](https://www.odoo.com/documentation/17.0/es/_images/bom-type.png)

Por último, haga clic en la pestaña Varios. En el campo Plazo de fabricación escriba el número de días que el subcontratista tarda en fabricar el producto. Este número sirve para calcular la fecha prevista de llegada del producto.

 Nota

Cuando se trata de subcontratación básica no es necesario enumerar los componentes en la pestaña Componentes de la lista de materiales, pues el subcontratista gestiona los componentes necesarios para la fabricación y la forma en que se adquieren.

## Flujo de subcontratación básica[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#basic-subcontracting-workflow "Enlazar permanentemente con este título")

El flujo de trabajo de subcontratación básica consta de hasta cuatro pasos:

1. Crear una orden de venta para el producto subcontratado, esto creará una orden de compra para adquirir el producto del subcontratista.
    
2. Confirmar la orden de compra creada en el paso anterior o crear una nueva. Esto creará una orden de recepción o de triangulación.
    
3. Procesar la recepción después de que el subcontratista haya terminado de fabricar el producto subcontratado y lo envíe de vuelta a la empresa contratante **o** procesar la orden de triangulación para enviar el producto al cliente.
    
4. Si el flujo de trabajo se inició creando una orden de venta y el producto terminado no se envía directo al cliente final, procese la orden de entrega una vez que envíe el producto al cliente.
    

El número específico de pasos depende del motivo por el que le compra el producto subcontratado al subcontratista.

Si el motivo es cumplir con la orden específica del cliente, el proceso comienza con la creación de una orden de venta y termina con la entrega del producto al cliente o con el subcontratista enviándolo de forma directa.

Si el motivo es aumentar la cantidad de existencias disponibles, el proceso comienza con la creación de una orden de compra y termina con la recepción del producto en el inventario.

### Crear una orden de venta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#create-so "Enlazar permanentemente con este título")

Solo es necesario completar este paso si le compra el producto se compra al subcontratista para cumplir con alguna de las necesidades del cliente. Diríjase al siguiente paso si compra el producto para aumentar la cantidad disponible.

Para crear una nueva orden de venta, vaya a Ventas ‣ Órdenes ‣ Órdenes y haga clic en Nuevo.

Seleccione al cliente en el menú desplegable correspondiente. Después, haga clic en Agregar un producto en la pestaña Líneas de orden, seleccione un producto subcontratado en el menú desplegable Producto y escriba el número adecuado en el campo Cantidad.

Haga clic en el botón correspondiente para confirmar la orden de venta, en ese momento aparecerá el botón inteligente Compra en la parte superior de la página. Este botón abre la orden de compra creada para adquirir el producto subcontratado del subcontratista.

 Nota

Una orden de venta para el producto solo crea una orden de compra si la ruta _Reabastecer bajo pedido (MTO)_ está habilitada en el formulario del producto **y** el producto no tiene suficientes existencias para cumplir con la orden de venta.

Si hay suficientes existencias disponibles, confirmar una orden de venta para el producto creará una orden de entrega porque Odoo asume que la orden de venta se cumple con las existencias en el almacén.

No ocurre lo mismo con los productos subcontratados que se envían directo al cliente final. En ese caso **siempre** se crea una orden de compra, incluso si hay suficientes existencias.

### Procesar una orden de compra[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#process-po "Enlazar permanentemente con este título")

Si creó una orden de compra en el paso anterior, vaya a ella con el botón inteligente Compra ubicado en la parte superior de la orden o vaya a Compras –> Órdenes –> Órdenes de compra y selecciónela. Después, haga clic en Confirmar orden para confirmarla y pasar al siguiente paso.

Si no creó una orden de compra en el paso anterior, vaya a Compra ‣ Órdenes ‣ Órdenes de compra y haga clic en Nueva.

Comience a completar la orden de compra y seleccione a un subcontratista con el menú desplegable Proveedor. En la pestaña Productos, haga clic en Agregar un producto para crear una nueva línea de productos. En el campo Producto elija un producto subcontratado e ingrese la cantidad en el campo Cantidad. Por último, haga clic en Confirmar orden para confirmar la orden de compra.

Al confirmar una orden de compra para un producto que se fabrica mediante subcontratación básica, entonces se crea una orden de recepción o triangulación de forma automática a la que puede acceder con el botón inteligente Recibo o Triangular que aparece en la parte superior de la orden de compra.

![Una orden de compra para un producto de subcontratación básica, el botón inteligente Recepción aparece en la parte superior de la página.](https://www.odoo.com/documentation/17.0/es/_images/subcontractor-po.png)

Una orden de compra para un producto de subcontratación básica, el botón inteligente Recepción aparece en la parte superior de la página.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#id1 "Enlace permanente a esta imagen")

### Procesar una recepción o una orden de envío directo (triangulación)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#process-receipt-or-dropship-order "Enlazar permanentemente con este título")

Después de que el subcontratista terminó de fabricar el producto deberá enviarlo a la empresa contratante o al consumidor final, esto depende de la [configuración](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#manufacturing-workflows-subcontracting-basic-product-config) del producto.

#### Procesar una recepción[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#process-receipt "Enlazar permanentemente con este título")

Si el subcontratista envía el producto terminado a la empresa contratante, vaya a Compra ‣ Órdenes ‣ Órdenes de compra después de que se haya recibido y seleccione la orden de compra.

Haga clic en el botón Recibir productos que está ubicado en la parte superior de la orden de compra o en el botón inteligente Recibo que se encuentra en la parte superior de la página para abrir la recepción. Después, haga clic en Validar en la parte superior del recibo para ingresar el producto al inventario.

#### Procesar una orden de envío directo (triangulación)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#process-dropship-order "Enlazar permanentemente con este título")

Si el subcontratista envía el producto directo al cliente final, vaya a Compra ‣ Órdenes ‣ Órdenes de compra una vez que lo haya enviado y seleccione la orden de compra.

Seleccione el botón inteligente Triangular ubicado en la parte superior de la página para abrir la orden de envío directo y después haga clic en Validar en la parte superior de la orden para confirmar que ya le enviaron el producto al cliente.

### Procesar una orden de entrega[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html#process-delivery-order "Enlazar permanentemente con este título")

Si el flujo de trabajo de subcontratación fue iniciado por una orden de venta del cliente y el producto terminado **no** fue enviado de forma directa al cliente, sino que lo recibió la empresa contratante, es necesario enviar el producto al cliente y procesar la orden de entrega.

Una vez que haya enviado el producto al cliente, vaya a la aplicación Ventas y seleccione la orden de venta. Presione el botón inteligente Entrega ubicado en la parte superior de la página para abrir la orden de entrega, luego haga clic en Validar en la orden para confirmar que el producto ha sido enviado.