Los **descuentos de efectivo** son reducciones al importe que un cliente debe pagar por un bien o servicio; por lo general se ofrecen para incentivar al cliente a pagar una factura de inmediato. Con frecuencia, los descuentos son un porcentaje del importe total de la factura y se aplican solo si el cliente paga en un plazo específico. Los descuentos de efectivo ayudan a que las empresas mantengan un flujo de efectivo constante.

 Example

Crea una factura de €100 el primero de enero. El pago total se tiene que hacer dentro de los siguientes 30 días, pero también ofrece un descuento del 2% si el cliente paga dentro de los primeros 7 días.

El cliente puede pagar €98 hasta el 8 de enero. Después de esta fecha, tendrá que pagar €100 antes del 31 de enero.

También se puede aplicar una [reducción de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#cash-discounts-tax-reductions) dependiendo del país o la región.

 Ver también

- [Términos de pago y planes de pago a plazos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/payment_terms.html)
    
- [Pagos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html)
    

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#configuration "Enlazar permanentemente con este título")

Para otorgar descuentos de efectivo a los clientes, primero debe verificar las [cuentas de ganancias y pérdidas](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#cash-discounts-gain-loss-accounts). Después, configure los [términos de pago](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#cash-discounts-payment-terms) y agregue un descuento en efectivo, para esto debe seleccionar la casilla Descuento anticipado y completar los campos de porcentaje de descuento, días de descuento y de [reducción de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#cash-discounts-tax-reductions).

### Cuentas de ganancias o pérdidas por descuentos de efectivo[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#cash-discount-gain-loss-accounts "Enlazar permanentemente con este título")

Con un descuento de efectivo, la cantidad que gana depende de cuánto se beneficia el cliente o no del descuento. Esto siempre lleva a pérdidas o ganancias, que se registran en cuentas predeterminadas.

Para modificar estas cuentas vaya a Contabilidad ‣ Configuración ‣ Ajustes. En la sección Cuentas predeterminadas seleccione las cuentas que desea usar para la Cuenta de ganancia por descuento de efectivo y la Cuenta de pérdida por descuento de efectivo.

### Términos de Pago[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#payment-terms "Enlazar permanentemente con este título")

Los descuentos de efectivo se definen en los [términos de pago](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/payment_terms.html). Para configurarlos según sus necesidades, vaya a Contabilidad ‣ Configuración ‣ Términos de pago y asegúrese de completar los campos de porcentaje de descuento, días de descuento y de [reducción de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#cash-discounts-tax-reductions).

![Configuración de los términos de pago llamados "2/7 neto 30". El campo "Descripción en las facturas" dice: "Términos de pago: 30 días, 2% de descuento por pago anticipado antes de 7 días".](https://www.odoo.com/documentation/17.0/es/_images/payment-terms.png)

### Reducciones de impuestos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#tax-reductions "Enlazar permanentemente con este título")

Según el país o región, el importe base que se utiliza para calcular el impuesto puede variar, lo que puede resultar en una **reducción de impuestos**. Dado que las reducciones de impuestos se establecen en términos de pago individuales, cada término puede usar una reducción de impuestos específica.

Para configurar cómo se aplica la reducción de impuestos, vaya a un término de pago con la casilla Descuento anticipado habilitada y seleccione una de las tres opciones siguientes:

- Siempre (en la factura)
    
    El impuesto siempre se reduce. La cantidad de base que se usa para calcular el impuesto es la cantidad de diferencia, no importa si el cliente obtiene algún beneficio o no.
    
- En pago anticipado
    
    El impuesto se reduce solo si el cliente paga antes. La cantidad de base que se usa para calcular el impuesto es la misma que la venta: si el cliente obtiene un beneficio de la reducción, entonces se reduce el impuesto. Esto significa que la cantidad de los impuestos puede variar después de enviar la factura, dependiendo del cliente.
    
- Nunca
    
    El impuesto no se reduce. La cantidad de base que se usa para calcular el impuesto es la cantidad total, no importa si el cliente se beneficia o no del descuento.
    

 Example

Supongamos que usted crea una factura de €100 (libre de impuestos) con una tasa tributaria del 21%, el 1 de enero. El pago completo se debe de realizar dentro de los próximos 30 días y también ofrece un descuento del 2% si su cliente paga dentro de los próximos 7 días.

Always (upon invoice)On early paymentNever

|Fecha límite|Importe total sin pagar|Cálculo|
|---|---|---|
|8 de enero|€118.58|$98 + (21% de $98)|
|31 de enero|€120.58|$100 + (21% de $98)|

 Nota

- [Las tablas de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/tax_returns.html#tax-returns-tax-grids), que se usan para el reporte de impuestos, se calculan de manera correcta según el [tipo de reducción de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#cash-discounts-tax-reductions) que configuró.
    
- El **tipo de reducción de impuestos por diferencia de efectivo** puede preconfigurarse de manera correcta dependiendo del [paquete de localización fiscal](https://www.odoo.com/documentation/17.0/es/applications/finance/fiscal_localizations.html#fiscal-localizations-packages) con el que cuenta.
    

## Aplicar un descuento en efectivo a una factura[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#apply-a-cash-discount-to-a-customer-invoice "Enlazar permanentemente con este título")

Para aplicar un descuento de efectivo a una factura de cliente seleccione los [términos de pago que usted creó](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#cash-discounts-payment-terms). Odoo calculará de manera automática los importes correctos, los impuestos, las fechas de vencimiento y los registros contables.

En la pestaña asientos de diario puede mostrar los detalles del descuento. Para hacerlo tiene que hacer clic en el botón de «alternar» y agregar las columnas Fecha de descuento e Importe del descuento.

![Una factura por €100.00 en la que se seleccionó "2/7 neto 30" como término de pago. La pestaña de "asientos de diario" está abierta, y se muestran las columnas de "Fecha de descuento" e "Importe de descuento".](https://www.odoo.com/documentation/17.0/es/_images/invoice-journal-entry.png)

El importe del descuento y la fecha de vencimiento también se muestran en el reporte de la factura generada que se envía al cliente si la opción Mostrar fechas de las cuotas está seleccionada en los términos de pago.

![Una factura de $100.00 con el siguiente texto escrito dentro de los términos y condiciones: "30 días, 2% de descuento por pago anticipado antes de 7 días. El total es de $118.58 si se paga antes del 01/08/2023."](https://www.odoo.com/documentation/17.0/es/_images/invoice-print.png)

### Conciliación de pagos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/cash_discounts.html#payment-reconciliation "Enlazar permanentemente con este título")

Cuando registra un [pago](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html) o [concilia sus transacciones bancarias](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html), Odoo toma en cuenta la fecha del pago del cliente para definir si se puede beneficiar del descuento de efectivo o no.

 Nota

Si su cliente paga el importe del descuento _después_ de la fecha límite para obtener el descuento, usted decide si indica si la factura está pagada en su totalidad con una cancelación o si indica que está parcialmente pagada.