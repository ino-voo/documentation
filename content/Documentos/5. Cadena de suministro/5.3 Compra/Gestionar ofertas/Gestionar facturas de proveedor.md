Una _factura de proveedor_ es una factura que se recibe para bienes y/o servicios que una empresa adquiere de un proveedor. Estas facturas registran todo lo que llega de los proveedores que se debe pagar y puede incluir importes adeudados por lo bienes y/o servicios adquiridos, impuestos sobre las ventas, cargos de transporte, envíos y mucho más.

En Odoo, una factura de proveedor se puede crear en diferentes puntos del proceso de compra, dependinedo de la política de _control de facturas_ configruada en los ajustes de la aplicación _Compra_.

## Políticas de control de facturación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#bill-control-policies "Enlazar permanentemente con este título")

Para configurar las políticas de control, vaya a Aplicación de compra ‣ Configuración ‣ Ajustes y baje hasta la sección de Facturación.

La función Control de facturas le brinda dos opciones de políticas: Cantidades ordenadas y Cantidades recibidas.

La que selecciona será la que se use de forma predeterminada por cada producto creado. Cada política actúa de la siguiente manera:

- Cantidades ordenadas: crea una factura de proveedor en cuanto se confirma una orden de compra. Los productos y cantidades en la orden de compra se usan para generar un borrador de factura.
    
- Cantidades recibidas: se crea una factura solamente **después** de que el total (o una parte) de la orden se recibió. Los productos y cantidades **recibidos** se usan para generar un borrador de factura.
    

![Política de control de facturas en los ajustes de la aplicación Compra.](https://www.odoo.com/documentation/17.0/es/_images/manage-configuration-settings.png)

Un vez que seleccionó una política, haga clic en Guardar para guardar todos los cambios.

 Truco

Si un producto necesita una política de control diferente a la que está configurada en la aplicación _Compra_, puede sobrescribir la política de esa producto en la pestaña Compra en el formulario del producto. Seleccione la política deseada en el campo Política de control.

![Campo de control de políticas en el formulario del producto.](https://www.odoo.com/documentation/17.0/es/_images/manage-product-form.png)

### Conciliación de tres vías[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#way-matching "Enlazar permanentemente con este título")

La política de _conciliación de tres vías_ asegura que las facturas solo se paguen una vez que reciba una parte de (o todos) los productos incluidos en la orden de compra.

Para activar la conciliación de tres vías, vaya a Aplicación de compra ‣ Configuración ‣ Ajustes y baje hasta la sección de Facturación.

Marque la casilla de verificación a un lado de Conciliación de tres vías y haga clic en Guardar.

 Importante

La función de conciliación de tres vías **solo** tiene el propósito de funcionar con la política de control de facturas correspondiente a Cantidades recibidas.

## Crear y gestionar facturas de proveedor al recibir productos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#create-and-manage-vendor-bills-on-receipts "Enlazar permanentemente con este título")

Cuando se reciben productos en el almacén de una empresa, también se crean los recibos. Una vez que la empresa procese las cantidades recibidas, pueden elegir crear una factura de proveedor directamente desde el formulario de recepción de almacén.

Dependiendo de la política de control de la factura que seleccionó en ajustes, la creación de factura de proveedor se crea en diferentes pasos del proceso de abastecimiento.

### Cantidades pedidas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#ordered-quantities "Enlazar permanentemente con este título")

Para crear y gestionar facturas de proveedor para recibos cuando la política de _control de factura_ es _cantidades ordenadas_, primero vaya a la aplicación Compra y haga clic en Nuevo en el tablero de Solicitud de cotización.

Al hacer esto, se abrirá un formulario de solicitud de cotización. En este formulario en blanco de [|solicitud de cotización|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id1) agregue un Proveedor y haga clic en Agregar una línea en la pestaña Producto para agregar productos a la orden.

En la línea de producto seleccione un producto desde el menú desplegable en el campo Producto e ingrese la cantidad a ordenar en el campo Cantidad.

Cuando esté listo, haga clic en Confirmar orden para confirmar [|la solicitud de cotización|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id3) y convertirla a la [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id5).

Después, haga clic en Crear factura para crear una factura de proveedor. Esto abre una Factura de proveedor en estado de Borrador. Desde ahí, agregue una fecha en el campo Fecha de factura.

Cuando esté listo, haga clic en Confirmar en la página Factura de proveedor.

 Truco

Puesto que la política de control de facturas está establecida en _cantidades ordenadas_, el borrador de factura se puede confirmar tan pronto como se crea antes de que haya recibido los productos.

Una vez que se haya recibido el pago, haga clic en Registrar pago en la parte superior de la factura para registrarla.

Al hacer esto aparecerá una ventana emergente para Registrar pago en la que podrá seleccionar el diario de pago y el método de pago para elegir.

Además, el total, fecha de pago y el memo (Número de referencia) de la factura se puede editar en esta ventana emergente, si es necesario.

Una vez que esté listo, haga clic en Crear pago para terminar de crear la Factura de proveedor. Al hacerlo se mostrará un listón verde que dice Pagado en el formulario de la [|solicitud de facturación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id7).

![Formluario de la factura de proveedor para la política de control sobre cantidades ordenadas.](https://www.odoo.com/documentation/17.0/es/_images/manage-draft-vendor-bill.png)

### Cantidades recibidas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#received-quantities "Enlazar permanentemente con este título")

Para crear y gestionar facturas de proveedor para recibos cuando la política de control de factura es _cantidades ordenadas_, primero vaya a la aplicación Compra y haga clic en Nuevo.

Al hacer esto, se abrirá una [|solicitud de cotización|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id9) nueva. En este formulario en blanco de [|solicitud de cotización|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id11) agregue un Proveedor y haga clic en Agregar una línea en la pestaña Producto para agregar productos a la orden.

En la línea de producto seleccione un producto desde el menú desplegable en el campo Producto e ingrese la cantidad a ordenar en el campo Cantidad.

Cuando esté listo, haga clic en Confirmar orden para confirmar [|la solicitud de cotización|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id13) y convertirla a la [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id15).

 Importante

Al usar la política de control _cantidades recibidas_ si hace clic en Crear factura antes de que se reciba cualquier producto causará que aparezca una ventana emergente Operación no válida.

En Odoo es necesario incluir al menos cantidades parcial de los artículos en la recepción de la [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id17) para poder crear una factura de proveedor.

![Ventana emergente con el mensaje de error de usuario para la política de control sobre cantidades recibidas.](https://www.odoo.com/documentation/17.0/es/_images/manage-user-error-popup.png)

En la [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id19) haga clic en el botón inteligente de Recepción para ver el formulario de recepción del almacén.

Haga clic en Validar para registrar las cantidades Hechas (recibidas).

Después, regrese a la [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id21) usando las migas de pan y después haga clic en Crear factura.

Esto abre un formulario de factura de proveedor en estado Borrador. Aquí, agregue una fecha en el campo Fecha de la factura. Una vez que esté listo, haga clic en Confirmar en la parte superior de la factura para confirmar la factura.

Una vez que se haya recibido el pago, haga clic en Registrar pago en la parte superior de la factura para registrarla.

Al hacer esto aparecerá una ventana emergente para Registrar pago en la que podrá seleccionar el diario de pago y el método de pago para elegir.

Además, el total, fecha de pago y el memo (Número de referencia) de la factura se puede editar en esta ventana emergente, si es necesario.

Una vez que esté listo, haga clic en Crear pago para terminar de crear la Factura de proveedor. Al hacerlo se mostrará un listón verde que dice Pagado en el formulario de la [|solicitud de facturación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id23).

## Gestionar las facturas de proveedores en Contabilidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#manage-vendor-bills-in-accounting "Enlazar permanentemente con este título")

Las facturas de proveedores también se pueden crear en la aplicación _Contabilidad_, sin tener que crear una orden de compra primero.

Vaya a Contabilidad ‣ Proveedores ‣ Facturas y haga clic en Nuevo para abrir un formulario en blanco de Factura de proveedor.

Agregue un proveedor en el campo Proveedor. Después, en la pestaña Líneas de factura haga clic en Agregar una línea para agregar productos.

Seleccione un producto del menú desplegable que se encuentra en el campo Producto e ingrese la cantidad por ordenar en el campo Cantidad.

Seleccionar una Fecha de factura y configure cualquier otra información necesaria. Finalmente haga clic en Confirmar para confirmar la plantilla.

Una vez confirmada, haga clic en la pestaña de Apuntes contables para ver los diarios de las Cuentas que se llenan según la configuración correspondiente de los formularios de Proveedor y Producto.

Si es necesario, haga clic en Nota de crédito para agregar una nota de crédito a la factura. Además, puede agregar un número de Referencia de la factura.

Una vez hecho, haga clic en Registrar pago, luego en Crear pago y complete la Factura de proveedor.

 Truco

Para vincular una factura en borrador a una orden de compra existente haga clic en el menú desplegable aun lado de Autocompletar _antes_ de hacer clic en Confirmar y seleccione una [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#id25) del menú.

La factura se completa en automático con la información de la orden de compra seleccionada.

![Lista desplegable de autocompletado en el borrador de la factura de proveedor.](https://www.odoo.com/documentation/17.0/es/_images/manage-auto-complete.png)

## Facturación por lotes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html#batch-billing "Enlazar permanentemente con este título")

Las facturas de proveedor se pueden procesar y gestionar por lotes desde la aplicación _Contabilidad_.

Vaya a Contabilidad ‣ Proveedores ‣ Facturas. Después, haga clic en la casilla de verificación en la esquina superior izquierda a un lado de la columna Número abajo del botón Nuevo.

Así se seleccionarán todas las facturas de proveedor existentes con un Estado de Publicada o Borrador.

Haga clic en el botón  Imprimir para imprimir las facturas seleccionadas.

Haga clic en Registrar pago para crear y procesar pagos para varios proveedores al mismo tiempo.

 Nota

Los pagos en línea que tengan Estado de Publicado pueden facturarse en lotes. Los pagos en la etapa Borrador **deben** publicarse antes de que se puedan incluir en una facturación por lotes.

Al hacer clic en Registrar pago se abrirá una ventana emergente del mismo nombre. En esta ventana podrá seleccionar el Diario en el que se debe publicar la factura, la Fecha de pago y el Método de pago

Desde esta ventana también tiene la opción de Agrupar pagos. Si se marca esta casilla de verificación, solo se creará un pago el lugar de un pago por factura. Esta opción solo aparece si la función _Pagos por lote_ está activada en los ajustes de la aplicación Contabilidad

Cuando esté listo, haga clic en el botón de Crear pago, el cual crea una lista de asientos contables en una página por separado. Todos los asientos contables en esta lista estarán vinculados a sus facturas de proveedor correspondientes.

![Ventana emergente de registro de facturación por lotes.](https://www.odoo.com/documentation/17.0/es/_images/manage-batch-billing.png)

 Ver también

[Políticas de control de facturación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/control_bills.html)