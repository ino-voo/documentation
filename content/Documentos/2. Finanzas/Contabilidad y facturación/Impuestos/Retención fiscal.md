Una **retención de impuestos** fuerza a la persona que pague una factura de cliente a deducir el impuesto del pago y remitirlo al gobierno. Normalmente, un impuesto se incluye en el subtotal para calcular la cantidad total pagada, mientras que los impuestos retenidos se quitan directamente del pago.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/retention.html#configuration "Enlazar permanentemente con este título")

En Odoo, para definir un impuesto retenido debe crear un impuesto negativo en Contabilidad ‣ Configuración ‣ Impuestos y, en el campo Cantidad, ingrese una cantidad negativa.

![cantidad negativa de impuestos en el campo](https://www.odoo.com/documentation/17.0/es/_images/negative-amount.png)

Después, vaya a la pestaña Opciones avanzadas y cree un Gupo de impuestos de retención.

![grupo de impuestos para impuesto de retención.](https://www.odoo.com/documentation/17.0/es/_images/tax-group.png)

 Truco

Si la retención es un porcentaje de un impuesto regular, cree un Impuesto cuyo Cálculo de impuestos sea Grupo de impuestos. Después, configure tanto el impuesto normal como el de retención en la pestaña Definición.

## Retención de impuestos en facturas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/retention.html#retention-taxes-on-invoices "Enlazar permanentemente con este título")

Una vez que haya creado el impuesto de retención podrá usarlo en formularios de clientes, órdenes de ventas y facturas. Puede aplicar varios impuestos en una sola línea de factura.

![líneas de facturas con impuestos](https://www.odoo.com/documentation/17.0/es/_images/invoice-tax.png)

 Ver también

[Impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html)