Para asegurarse de que los clientes paguen sus facturas a tiempo es necesario especificar todas las condiciones en los **términos de pago**.

Los términos de pago generalmente se definen en documentos como las órdenes de venta y las facturas. Estos términos cubren:

- La o las fechas límite
    
- Descuentos por pago anticipado
    
- Cualquier otra condición del pago.
    

Un **plan de cuotas** permite a los clientes pagar una factura en partes con los importes y fechas definidas previamente por el proveedor.

 Example

Pago inmediato

Se debe pagar la totalidad de la factura el día de su emisión.

15 días (o 15 días netos)

Se debe pagar la totalidad de la factura 15 días después de su fecha de emisión.

el día 21 del mes siguiente a la factura

Se debe pagar la totalidad de la factura antes del día 21 del siguiente mes a la fecha de su emisión.

30% Anticipo - Restante Al Fin del Mes Siguiente

Se debe pagar el 30% el día en el que se emita la factura. El balance restante se debe pagar al final del mes siguiente.

2% día 10, neto a 30 días a final de mes

Un [descuento por pronto pago](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html) del 2% si el pago se recibe en un periodo de diez días. En caso contrario, se debe realizar el pago completo al final del mes siguiente a la fecha de la factura.

 Nota

- No hay que confundir los términos de pago con [las facturas a plazos](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html). Si para una orden en específico usted emite varias facturas a su cliente, entonces estamos hablando de una política de facturación, no de un término de pago ni de un plan de pago a plazos.
    
- En esta página hablamos sobre la función _términos de pago_ no de los [términos y condiciones](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/terms_conditions.html), que se usan para declarar obligaciones contractuales sobre uso de contenido, políticas de devoluciones y otras políticas sobre la venta de bienes y servicios.
    

 Ver también

- [Tutoriales de Odoo: términos de pago](https://www.odoo.com/slides/slide/payment-terms-1679)
    
- [Descuentos en efectivo y reducción de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html)
    

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/payment_terms.html#configuration "Enlazar permanentemente con este título")

Para crear nuevos términos de pago, siga los siguientes pasos:

1. Vaya a Contabilidad ‣ Configuración ‣ Términos de pago y haga clic en Nuevo.
    
2. Ingrese un nombre en el campo Términos de pago. Este campo es el nombre que aparecerá en la base de datos, el cliente no puede visualizarlo.
    
3. Seleccione la casilla Descuento anticipado y complete los campos de porcentaje de descuento, días de descuento y [reducción de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#cash-discounts-tax-reductions) para agregar un [descuento en efectivo](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html), si así lo desea.
    
4. En la sección Términos debidos agregue las reglas (términos) para definir lo que se debe pagar y las fechas correspondientes. Al definir los términos, las fechas límite de pago se calculan de forma automática, lo cual es muy útil al gestionar **pagos a plazos** (términos de pago con varios términos).
    
    Para agregar un término, haga clic en Agregar una línea, defina el valor del descuento y complete los campos Debido y Después para determinar la fecha de vencimiento.
    
5. Escriba el texto que aparecerá en el documento (orden de venta, factura, etc.) en el cuadro de texto gris que se ubica en la columna Vista previa.
    
6. Seleccione la opción Mostrar fechas de las cuotas para que en el reporte de la factura aparezca un resumen de cada pago y la fecha en la que se debe realizar, si es necesario.
    

 Truco

Si desea especificar un número de días _antes del fin de mes_, use un valor negativo en el campo Después.

Para comprobar que sus términos de pago están configurados de forma correcta, ingrese una fecha de facturación en la línea de ejemplo para generar los pagos que se deben realizar y las fechas límite que se muestran según estos términos de pago.

 Importante

Los términos se calcula en el orden de sus fechas límite.

 Example

En el siguiente ejemplo, se debe pagar el 30% el día en que se emite la factura y el 70% restante al final del mes siguiente.

![Ejemplo de un término de pago. En la primera línea se menciona que se debe pagar el 30% de inmediato. En la segunda línea se menciona que  el 70% restante se debe pagar al final del mes siguiente.](https://www.odoo.com/documentation/17.0/es/_images/configuration.png)

## Usar términos de pago[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/payment_terms.html#using-payment-terms "Enlazar permanentemente con este título")

Para definir los términos de pago puede usar el campo términos de pago en:

- **Contactos:** para configurar de manera automática términos de pago en las órdenes de venta y facturas de un contacto. Esto se puede modificar en el formulario del contacto, en la pestaña Venta y compra
    
- **Cotizaciones/Órdenes de venta:** para que de manera automática se configure un término de pago en todas las facturas que se generan de una cotización u orden de venta.
    

Para definir los términos de pago use el campo Fecha límite, com la lista desplegable Términos en:

- **Facturas de los clientes**: para configurar términos de pago específicos en una factura.
    
- **Facturas de los proveedores:** para configurar términos de pago específicos en una factura.
    

 Truco

Configurar términos de pago para proveedores es útil sobre todo cuando es necesario gestionar términos de pago de proveedores con diferentes plazos o descuentos de efectivo. De lo contrario, puede solo configurar una **fecha límite** de manera manual. Si los términos de pago ya están definidos, vacíe el campo para seleccionar una fecha.

## Asientos contables[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/payment_terms.html#journal-entries "Enlazar permanentemente con este título")

Las facturas con términos de pago específicos generan diferentes _asientos de diario_. Cada _fecha límite_ que se calculó tiene un _apunte de diario_.

Esto facilita los procesos de [seguimiento](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/follow_up.html) y [conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html) ya que Odoo toma en cuenta cada fecha límite y no solo el balance de la fecha límite. Esto también ayuda a obtener un reporte de [cuentas antiguas por cobrar](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices.html#customer-invoices-aging-report) correcto.

 Example

![La cantidad que se abonó a las cuentas por cobrar se divide en dos apuntes de diario con fechas límite diferentes.](https://www.odoo.com/documentation/17.0/es/_images/journal-entry.png)

En este ejemplo se emitió una factura de $1000 con los siguientes términos de pago: _El 30% debe pagarse el día de la emisión y el 70% restante al final del siguiente mes._

|Cuenta|Fecha límite|Débito|Crédito|
|---|---|---|---|
|Cuenta a cobrar|21 de febrero|300||
|Cuenta a cobrar|31 de marzo|700||
|Venta de productos|||1000|

Los $1000 que se abonaron a las cuentas por cobrar se divide en dos apuntes de diario distintos. Ambos tendrán su propia fecha límite.