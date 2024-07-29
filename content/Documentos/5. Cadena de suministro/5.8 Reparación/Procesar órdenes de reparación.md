A veces, los productos que los clientes reciben pueden romperse o dañarse durante el trayecto y deben devolverlos para obtener un reembolso, un reemplazo o para que los reparen.

La aplicación _Reparación_ de Odoo permite llevar seguimiento de las reparaciones de los productos que devuelven los clientes. Una vez reparados, es posible volver a entregar los productos al cliente.

El proceso de devolución y reparación de productos dañados con frecuencia sigue estos pasos:

1. [Procesar la orden de devolución de un producto dañado](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/repairs/repair_orders.html#repairs-repair-orders-return-order)
    
2. [Crear una orden de reparación para un producto devuelto](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/repairs/repair_orders.html#repairs-repair-orders-repair)
    
3. [Devolver el producto reparado al cliente](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/repairs/repair_orders.html#repairs-repair-orders-return-customer)
    

## Devolución de órdenes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/repairs/repair_orders.html#return-order "Enlazar permanentemente con este título")

Las devoluciones se pueden procesar en Odoo con _traslados inversos_ que se crean directo desde las órdenes de venta después de que un cliente recibió sus productos.

Para crear una devolución, vaya a la aplicación Ventas y haga clic en una orden de venta de la cual deba devolver un producto. En el formulario de la orden de venta haga clic en el botón inteligente Entrega, esta acción abrirá el formulario de la orden de entrega.

Haga clic en Devolver en el formulario, esta acción abre la ventana emergente Revertir traslado.

![Ventana emergente de traslado inverso en el formulario de la orden de entrega.](https://www.odoo.com/documentation/17.0/es/_images/repair-orders-reverse-transfer.png)

Esta ventana emergente muestra el producto incluido en la orden, la cantidad entregada al cliente y la unidad de medida en la que se encontraba el producto.

Haga clic en el valor en el campo Cantidad para modificar la cantidad del producto a devolver en caso de que sea necesario.

Haga clic en el icono 🗑️ (papelera) ubicado del lado derecho al final de la línea del producto para eliminarlo de la devolución en caso de que sea necesario.

Luego haga clic en Devolver para confirmar la devolución. Esto crea una nueva recepción para los productos devueltos.

Una vez que el producto se encuentre en el almacén podrá registrar la recepción de la devolución en la base de datos al hacer clic en Validar desde el formulario de reversión del traslado.

 Truco

El valor en la columna Entregado en la orden de venta original se actualiza luego de validar un traslado inverso de una devolución para reflejar la diferencia entre la cantidad que se ordenó al inicio y la cantidad devuelta por el cliente.

![Las columnas Entregado y Cantidad en la orden de venta luego de una devolución.](https://www.odoo.com/documentation/17.0/es/_images/repair-orders-quantity-delivered.png)

## Crear una orden de reparación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/repairs/repair_orders.html#create-repair-order "Enlazar permanentemente con este título")

Luego de devolver los productos, es posible llevar seguimiento de sus reparaciones al crear una orden de reparación.

Vaya a la aplicación Reparación para crear una nueva orden de reparación y haga clic en Nuevo. Esta acción abrirá un formulario vacío de orden de reparación.

![Lado izquierdo del formulario de la orden de reparación en blanco.](https://www.odoo.com/documentation/17.0/es/_images/repair-orders-left-hand-form.png)

Seleccione un cliente en el formulario. Debe seleccionar al cliente al que le facturará y entregará la orden.

En el campo Producto a reparar, haga clic en el menú desplegable y seleccione el producto que necesita reparación. Si es necesario, haga clic en Buscar más… para abrir la ventana emergente Buscar: Producto a reparar y visualizar todos los productos en la base de datos.

Luego de seleccionar un producto a reparar, el nuevo campo Cantidad de producto aparece abajo. Ahí escriba la cantidad (en formato `0.00`) del producto que necesita reparación.

A la derecha de ese valor, haga clic en la lista desplegable para seleccionar la unidad de medida (UdM) del producto.

Haga clic en el menú desplegable del campo Devolver y seleccione la orden de devolución de la cual proviene el producto a reparar.

Seleccione la casilla Bajo garantía si la reparación del producto está cubierta por una garantía. Al seleccionarla, el cliente no deberá pagar las piezas utilizadas en la orden de reparación.

En el campo Fecha programada, haga clic en la fecha para abrir un calendario emergente. Ahí seleccione la fecha para la reparación y haga clic en Aplicar.

![Lado derecho del formulario de la orden de reparación en blanco.](https://www.odoo.com/documentation/17.0/es/_images/repair-orders-completed-repair-form.png)

En el campo Responsable haga clic en el menú desplegable y seleccione al usuario que será responsable de la reparación.

Si está en un entorno multiempresa, en el campo Empresa seleccione a qué empresa pertenece esta orden de reparación.

En el campo Etiquetas haga clic en el menú desplegable y seleccione las etiquetas que deben aplicarse a esta orden de reparación.

### Pestaña de piezas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/repairs/repair_orders.html#parts-tab "Enlazar permanentemente con este título")

Agregue, elimine o recicle piezas en la pestaña con el mismo nombre. Para ello, haga clic en Agregar una línea en la parte inferior del formulario.

Haga clic en la columna Tipo, esto hará que aparezcan tres opciones: Agregar (seleccionada de forma predeterminada), Eliminar y Reciclar.

![Opciones de la columna Tipo o nueva pieza en la pestaña Piezas.](https://www.odoo.com/documentation/17.0/es/_images/repair-orders-type-column.png)

Seleccionar Agregar añade esta pieza a la orden de reparación, es decir, agregar piezas enumera los componentes que se usarán en la reparación. Si los componentes son utilizados, el usuario que completa la reparación puede registrarlos. En caso contrario, el usuario también puede indicarlo y guardar los componentes para otro uso.

Seleccionar Eliminar quita esta parte de la orden de reparación, es decir, eliminar piezas enumera los componentes que debe retirar del producto durante el proceso de reparación. Si las piezas son eliminadas, el usuario que completa la reparación puede indicar que fueron retiradas.

Seleccionar Reciclar recicla esta parte de la orden de reparación para que pueda usarla después o para que la reutilice con otro propósito en el almacén.

En la columna Producto seleccione el producto (pieza) que se debe agregar, quitar o reciclar. En la columna Demanda cambie la cantidad, si es necesario, para indicar qué cantidad de esta pieza se debe utilizar en el proceso de reparación.

Cambie el valor (en formato `0.00`) en la columna Hecho después de que haya agregado, eliminado o reciclado la pieza con éxito.

Seleccione la unidad de medida de la pieza en la columna con el mismo nombre.

Por último, seleccione la casilla en la columna Utilizado después de haber usado la pieza en el proceso de reparación.

Haga clic en el icono (menú para mostrar u ocultar columnas opcionales) ubicado en el extremo derecho de la fila de encabezado para agregar columnas adicionales a la línea. Seleccione las opciones que desee agregar a la línea.

![Opciones adicionales opcionales a agregar a una línea de pieza.](https://www.odoo.com/documentation/17.0/es/_images/repair-orders-additional-options.png)

### Pestañas de notas de reparación y varios[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/repairs/repair_orders.html#repair-notes-and-miscellaneous-tabs "Enlazar permanentemente con este título")

Haga clic en la pestaña Notas de reparación para agregar notas internas sobre esta orden en específico y cualquier otra información que el usuario que realice la reparación deba conocer.

Haga clic en el campo de texto vacío para escribir notas.

Haga clic en la pestaña Varios para ver el tipo de operación de esta reparación. De forma predeterminada, esta está establecido como SuEmpresa: Reparaciones, lo que indica que se trata de una operación de tipo reparación.

Haga clic en Confirmar reparación después de que haya realizado todas las configuraciones deseadas en el formulario de la orden de reparación. Esta acción mueve la orden de reparación a la etapa Confirmada y reserva los componentes necesarios para la reparación.

La nueva columna Pronosticado aparece en las líneas de productos de la pestaña Piezas y muestra la disponibilidad de todos los componentes necesarios para la reparación.

Una vez listo, haga clic en Iniciar reparación. Esta acción mueve la orden de reparación a la etapa En reparación (en la esquina superior derecha). Haga clic en Cancelar reparación si necesita cancelarla.

La orden de reparación se completa luego de que todos los productos hayan sido reparados con éxito. Para registrar esto en la base de datos, haga clic en Finalizar reparación.

 Nota

Si no utilizó todas las piezas agregadas a la orden de reparación, al hacer clic en Finalizar reparación aparecerá la ventana emergente Movimientos incompletos.

![Ventana emergente de movimientos incompletos para las piezas sin utilizar.](https://www.odoo.com/documentation/17.0/es/_images/repair-orders-uncomplete-moves.png)

La ventana emergente le informará al usuario que hay una diferencia entre la demanda inicial y la cantidad real que se utilizó en la orden.

Haga clic en Descartar o cierre la ventana emergente si debe cambiar la cantidad utilizada. Haga clic en Validar si debe confirmar la orden.

Esta acción mueve la orden de reparación a la etapa Reparado y también aparece el botón inteligente Movimientos de producto arriba del formulario.

Haga clic en el botón inteligente Movimientos de producto para ver el historial de movimientos del producto durante y después del proceso de reparación.

![Historial de movimiento del producto incluido en la orden de reparación.](https://www.odoo.com/documentation/17.0/es/_images/repair-orders-product-moves.png)

### Devolver el producto al cliente[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/repairs/repair_orders.html#return-product-to-customer "Enlazar permanentemente con este título")

#### El producto se encuentra bajo garantía[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/repairs/repair_orders.html#product-is-under-warranty "Enlazar permanentemente con este título")

Después de que reparó el producto con éxito puede devolvérselo al cliente.

#### El producto ya no tiene garantía[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/repairs/repair_orders.html#product-is-not-under-warranty "Enlazar permanentemente con este título")

Haga clic en Crear cotización si el producto no se encuentra en garantía o si el cliente debe pagar los costos de reparación. Esta acción abrirá un nuevo formulario de orden de venta que estará completado con las piezas utilizadas en la orden de reparación y el costo total de la reparación calculado.

![Nueva cotización precompletada para las piezas incluidas en la orden de reparación.](https://www.odoo.com/documentation/17.0/es/_images/repair-orders-new-quotation.png)

Si es necesario enviar esta orden de venta al cliente, haga clic en Confirmar y proceda a facturar al cliente por la reparación.

 Truco

Si necesita que el cliente pague el servicio de reparación puede crear un producto de tipo servicio y agregarlo a la orden de venta de un producto reparado.

Para devolver el producto al cliente, vaya a la aplicación Ventas y seleccione la orden de venta original desde la cual se procesó la devolución inicial. Haga clic en el botón inteligente Entrega.

De la lista resultante de operaciones, haga clic en el traslado revertido señalado por el documento fuente, que debería ser `Devolución de WH/OUT/XXXXX`.

Esta acción abre el formulario de devolución. En la parte superior de este formulario ahora aparece el botón inteligente Órdenes de reparación que vincula esta devolución a la orden de reparación completada.

Haga clic en Devolver en la parte superior del formulario para abrir la ventana emergente Revertir traslado.

![Ventana emergente de traslado inverso en el formulario de la orden de entrega.](https://www.odoo.com/documentation/17.0/es/_images/repair-orders-reverse-transfer.png)

Esta ventana emergente muestra el producto incluido en la orden, la cantidad entregada al cliente y la unidad de medida en la que se encontraba el producto.

Haga clic en el valor en el campo Cantidad para modificar la cantidad del producto a devolver en caso de que sea necesario.

Haga clic en el icono 🗑️ (papelera) ubicado del lado derecho al final de la línea del producto para eliminarlo de la devolución en caso de que sea necesario.

Luego haga clic en Devolver para confirmar la devolución. Esto crea una nueva entrega para los productos devueltos.

Después de procesar la entrega y devolver el producto al cliente, haga clic en Validar para validarla.

 Ver también

[Devoluciones y reembolsos](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/returns.html)