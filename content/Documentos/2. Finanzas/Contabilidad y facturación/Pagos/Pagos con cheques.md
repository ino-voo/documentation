Una vez que decida pagar la factura de su proveedor, puede pagar con cheque. Después puede imprimir todos los pagos que se registraron por cheque. Finalmente, el proceso de conciliación bancaria vinculará los cheques que usted le envía a los proveedores con los estados bancarios.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/pay_checks.html#configuration "Enlazar permanentemente con este título")

### Activar métodos de pago con cheque[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/pay_checks.html#activate-checks-payment-methods "Enlazar permanentemente con este título")

Para activar el método de pago con cheques, vaya a Contabilidad ‣ Configuración ‣ Ajustes y baje a la sección Pagos de proveedor. Ahí debe activar el método de pago, además de que debe configurar el Diseño del cheque.

 Nota

- Ya que haya activado la opción Cheques, el método de pago **por cheques** se configura de manera automática en las pestañas Pagos salientes del diario **bancario**.
    
- Algunos países necesitan módulos específicos del país para imprimir cheques, es posible que estos módulos ya estén instalados. Por ejemplo, el módulo U.S. Checks Layout es necesario para imprimir cheques en los Estados Unidos.
    

## Material compatible para la impresión de cheques[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/pay_checks.html#compatible-check-stationery-for-printing-checks "Enlazar permanentemente con este título")

### Estados Unidos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/pay_checks.html#united-states "Enlazar permanentemente con este título")

Para los Estados Unidos, Odoo es compatible de forma predeterminada con los siguientes formatos de cheques:

- **Quickbooks y Quicken**: cheque en la parte superior, talón en el centro y en la parte inferior.
    
- **Peachtree**: cheque en el medio, talón en la parte superior e inferior.
    
- **ADP**: cheque en la parte inferior, y talón en la parte superior.
    

## Pagar una factura de proveedor con un cheque[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/pay_checks.html#pay-a-supplier-bill-with-a-check "Enlazar permanentemente con este título")

El pago a un proveedor con un cheque se realiza en tres pasos:

1. registrar un pago
    
2. Imprimir cheques en lote para todos los pagos registrados.
    
3. conciliación de estados bancarios
    

### Registrar un pago con cheque[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/pay_checks.html#register-a-payment-by-check "Enlazar permanentemente con este título")

Para registrar un pago, abra cualquier factura de proveedor desde el menú Compras ‣ Facturas de proveedor. Puede registrar un pago una vez que se validó una factura de proveedor. Configure el método de pago como Cheques y valide el pago.

### Imprimir cheques[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/pay_checks.html#print-checks "Enlazar permanentemente con este título")

En su tablero de Contabilidad vaya al diario banco puede ver el número de cheques que están registrados. Al hacer clic en Cheques por imprimir puede imprimir los cheques conciliados.

Para imprimir todos los cheques por lote, seleccione todos los pagos desde la vista de lista y haga clic en Imprimir.