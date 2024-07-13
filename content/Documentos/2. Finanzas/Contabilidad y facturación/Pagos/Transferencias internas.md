Puede gestionar trasferencias de dinero internas desde Odoo. Necesita al menos dos cuentas bancarias para realizar transferencias internas.

 Ver también

[Cómo agregar una cuenta bancaria adicional](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html)

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/internal_transfers.html#configuration "Enlazar permanentemente con este título")

Una cuenta de transferencia interna se crea de manera automática en su base de datos en función de la localización de su empresa y de la legislación de su país. Para modificar la cuenta predeterminada de Transferencia interna vaya a la:menuselection:`Aplicación Contabilidad --> Configuración --> Configuración` en la sección de Cuentas predeterminadas.

## Registrar una transferencia interna de un banco a otro[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/internal_transfers.html#register-an-internal-transfer-from-one-bank-to-another "Enlazar permanentemente con este título")

Si quiere transferir dinero de un banco a otro, vaya al tablero de Contabilidad, haga clic en el botón de selección expandible (⋮) en el formulario del banco al que quiere hacer la transferencia. Después, haga clic en Pagos y seleccione o cree un pago, marque la casilla Transferencia interna y seleccione Diario de destino antes de que vaya a Confirmar la transferencia interna.

El dinero ahora estará registrado en la cuenta de transferencia y se creará otro pago de forma automática en el diario de destino.

 Example

- Diario bancario (Banco A)
    
    |**Cuenta**|**Debe**|**Haber**|
    |---|---|---|
    |Cuenta de pagos pendientes||$1,000|
    |**Cuenta de transferencia interna**|**$1,000**||
    
- Diario bancario (Banco B)
    
    |**Cuenta**|**Debe**|**Haber**|
    |---|---|---|
    |Cuenta de cobros pendientes|$1,000||
    |**Cuenta de transferencia interna**||**$1,000**|
    

Hay **un pago pendiente** y **un cobro pendiente** en los dos diarios de cuentas bancarias, porque aún no se ha registrado el extracto bancario que confirma el envío y la recepción del dinero.

Una vez que haya hecho esto, puede registrar y conciliar las líneas de diario bancario como siempre.

 Ver también

[Conciliación bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html)