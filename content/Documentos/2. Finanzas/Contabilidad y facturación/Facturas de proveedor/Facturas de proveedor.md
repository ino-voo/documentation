En Odoo podemos registrar las facturas de proveedores de forma **manual** o **automática**, mientras que el **reporte de cuentas por pagar pendientes** proporciona una visión general de todas las facturas pendientes para ayudarnos a pagar las cantidades correctas a tiempo.

 Ver también

- Tutorial [Registrar una factura de proveedor](https://www.odoo.com/slides/slide/registering-a-vendor-bill-1683?fullscreen=1)
    
- [Gestionar facturas de proveedor](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html)
    

## Creación de factura[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills.html#bill-creation "Enlazar permanentemente con este título")

### Manualmente[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills.html#manually "Enlazar permanentemente con este título")

Para crear una factura de proveedor de forma manual, vaya a Contabilidad ‣ Proveedores ‣ Facturas y haga clic en Crear.

### Automáticamente[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills.html#automatically "Enlazar permanentemente con este título")

Se pueden crear de forma automática las facturas de proveedores, solo se debe **enviar un correo electrónico** a un [seudónimo de correo electrónico](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/invoice_digitization.html#invoice-digitization-email-alias) vinculado al diario de compras, o **subir un PDF** en Contabilidad ‣ Proveedores ‣ Facturas y, luego, hacer clic en subir.

## Finalización de la factura[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills.html#bill-completion "Enlazar permanentemente con este título")

Aunque la factura se cree de forma manual o automática, debe asegurarse de que los siguientes campos se hayan completado correctamente:

- Proveedor: Odoo completa la información registrada en órdenes de compra o facturas del proveedor.
    
- Referencia de factura: añade la referencia de la orden de venta y se usa para hacer la [conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html#payments-matching) al recibir los productos.
    
- Autocompletar: seleccione una factura u orden de compra para que el documento se complete de forma automática. Debe haber completado el campo de proveedor antes de este campo.
    
- Fecha de factura: es la fecha de la emisión de la factura.
    
- Fecha contable: es la fecha en la cuál se registra el documento en su contabilidad.
    
- Referencia de pago: se indica automáticamente en el campo Memo al registrar un pago.
    
- Banco destinatario: indica el número de cuenta al que se tiene que hacer el pago.
    
- Fecha de vencimiento o Términos de la factura a pagar.
    
- Diario: selecciona el diario en el cuál se registrará la factura y su [divisa](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/multi_currency.html).
    

![factura de proveedor](https://www.odoo.com/documentation/17.0/es/_images/bill-completion.png)

 Nota

- Las facturas se pueden [digitalizar](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/invoice_digitization.html) para agilizar la completación automática, solo debe hacer clic en Enviar para digitalización.
    
- Si carga la factura verá el PDF de lado derecho, de esta manera podrá ver mejor su información.
    

## Confirmación de la factura[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills.html#bill-confirmation "Enlazar permanentemente con este título")

Haga clic en confirmar cuando termine un documento. El estado de su documento cambiará a Publicado y se creará un asiento de diario según la configuración de la factura.

 Nota

Una vez que se confirme no podrá editarlo. Si desea hacer algún cambio, tendrá que hacer clic Restablecer a borrador.

## Pago de la factura[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills.html#bill-payment "Enlazar permanentemente con este título")

Una vez pagada la factura del proveedor, haga clic en Registrar pago, esto hará que aparezca una nueva ventana.

Seleccione el diario, el método de pago, el importe a pagar (completo o parcial), y la divisa. Odoo completa el campo Memo de manera automática si la referencia de pago se estableció correctamente en la factura de proveedor; se recomienda que seleccione el número de factura de proveedor como referencia.

Una vez confirmada aparecerá un banner con el lema en proceso de pago hasta que se [concilia](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html) la factura.

## Reporte de cuentas antiguas por pagar[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills.html#aged-payable-report "Enlazar permanentemente con este título")

Si desea obtener una vista general de sus facturas de proveedor pendientes y sus fechas de vencimiento correspondientes, use el **reporte de cuentas antiguas por pagar**. Vaya a Contabilidad ‣ Reportes ‣ Reportes de contacto: Cuenta antigua por pagar.

Haga clic en el nombre de un proveedor para ver la información de todas las facturas con pagos pendientes, su importe, fechas de vencimiento, etc.

 Nota

- Si hace clic en el botón Guardar podrá exportar toda la información disponible como archivo PDF o XLSX y guardarlo en sus documentos.
    
- Si su proveedor tiene órdenes parciales y le envía facturas cada que envía productos, es posible que reciba varias facturas.