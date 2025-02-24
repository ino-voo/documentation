Hay dos maneras de gestionar pagos que se recibieron en Odoo, ya sea desde [las cuentas por cobrar](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#checks-outstanding-account) o si [evita el proceso de conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#checks-reconciliation-bypass).

**Recomendamos que use cuentas pendientes** ya que su cuenta bancaria se mantiene al día y correcta solo cuando puede tomar en cuenta cheques que no se han cambiado.

 Nota

Al final del proceso ambos métodos producen los mismos datos en su contabilidad. Sin embargo, si tiene cheques que no ha cambiado, el método **Cuentas por cobrar** registra estos cheques en la cuenta **Recibos por cobrar**. De igual manera, los fondos aparecen en su cuenta bancaria sin importar si se conciliaron o no, ya que el valor del banco se refleja en el momento que recibe su estado de cuenta bancaria.

 Ver también

- [Cuentas pendientes](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#bank-outstanding-accounts)
    
- [Conciliación bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/cheat_sheet.html#accounting-reconciliation)
    

## Método 1: cuentas pendientes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#method-1-outstanding-account "Enlazar permanentemente con este título")

Cuando recibe un cheque, usted [registra el pago](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html) mediante un cheque en la factura. Después, cuando a su cuenta bancaria se le abone la cantidad del cheque, usted reconcilia el pago y el estado de cuenta para que la cantidad se mueva de la cuenta **Pagos pendientes** a la cuenta **Banco**.

 Truco

Puede crear un nuevo método de pago llamado _Cheques_ si desea identificar este tipo de pagos con facilidad. Para hacerlo, vaya a Contabilidad ‣ Configuración ‣ Diarios ‣ Banco, haga clic en la pestaña Pagos entrantes y agregue una línea. Como Método de pago seleccione Manual y escriba `Cheques` como nombre.

## Método 2: ignorar la conciliación[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#method-2-reconciliation-bypass "Enlazar permanentemente con este título")

Cuando recibe un cheque, usted [registra un pago](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html) en la factura relacionada. Después, la cantidad se mueve de **Cuenta por cobrar** a la cuenta **Banco**, lo cual se salta el proceso de conciliación y crea solo **un asiento contable**.

Para lograrlo, usted _debe_ realizar la misma configuración que le presentamos a continuación. Vaya a Contabilidad ‣ Configuración ‣ Diarios ‣ Banco. Haga clic en la pestaña Pagos entrantes y después Agregue una línea. Seleccione Manual como Método de pago, e ingrese `Cheques` como el Nambre. Haga clic en el botón para alternar el menú, seleccione Cuenta de recibos pendientes, y en la columna Cuenta de recibos pendientes seleccione la cuenta Banco para el método de pago **Cheques**.

![Use la cuenta Banco para ignorar la cuenta de recibos pendientes.](https://www.odoo.com/documentation/17.0/es/_images/outstanding-payment-accounts.png)

## Registro de pagos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#payment-registration "Enlazar permanentemente con este título")

 Nota

De forma predeterminada hay dos maneras de registrar pagos hechos con cheque:

- **Manual**: para cheques únicos, y
    
- **Por lote**: para varios cheques a la vez.
    

Esta documentación está enfocada en pagos para **cheques únicos**. Para **depósitos por lotes**, consulte la [documentación de pagos por lotes](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/batch.html).

Una vez que reciba el cheque de un cliente, vaya a la factura relacionada (Contabilidad ‣ Cliente ‣ Facturas), y haga clic en Registrar pago. Llene la información de pago:

- Diario: Banco;
    
- Método de pago: Manual (o **Cheques** si creó un método de pago específico);
    
- Memorando: ingrese el número de cheque;
    
- Haga clic en Crear pago.
    

![Revise la información de pago](https://www.odoo.com/documentation/17.0/es/_images/payment-checks.png)

Los asientos bancarios generados serán diferentes según el método de registro de pago que se eligió.

## Asientos contables[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#journal-entries "Enlazar permanentemente con este título")

### Cuentas pendientes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#outstanding-account "Enlazar permanentemente con este título")

La factura se marca como En proceso de pago tan pronto como se registra el pago. Esta operación producirá el siguiente **asiento de diario**:

|Cuenta|Conciliación de estados de cuenta bancarios|Débito|Crédito|
|---|---|---|---|
|Cuenta a cobrar|||100.00|
|Recibos pendientes||100.00||

Después, ya que reciba los estados de cuenta bancarios, vincule ese estado de cuenta con el cheque que está en la cuenta de **Recibos pendientes**, lo que producirá el siguiente **asiento de diario**:

|Cuenta|Conciliación de estados de cuenta bancarios|Débito|Crédito|
|---|---|---|---|
|Recibos pendientes|X||100.00|
|Banco||100.00||

Si elige este enfoque para gestionar los cheques recibidos, obtendrá la lista de cheques que no se han cambiado en la cuenta **Recibos pendientes** (a la que puede entrar desde el libro mayor general, por ejemplo).

### Ignorar el paso de conciliación[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#reconciliation-bypass "Enlazar permanentemente con este título")

La factura se marca como Pagado tan pronto como se registre el cheque.

Con este enfoque, no se tendrá que usar la cuenta de **recibos pendientes**, lo que significa que solo obtendrá un asiento de diario en sus libros y se saltará el paso de conciliación:

|Cuenta|Conciliación de estados de cuenta bancarios|Débito|Crédito|
|---|---|---|---|
|Cuenta a cobrar|X||100.00|
|Banco||100.00||

 [Edit on GitHub](https://github.com/odoo/documentation/edit/17.0/content/applications/finance/accounting/payments/checks.rst)

##### EN ESTA PÁGINA

- - [Método 1: cuentas pendientes](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#method-1-outstanding-account)
    - [Método 2: ignorar la conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#method-2-reconciliation-bypass)
    - [Registro de pagos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#payment-registration)
    - [Asientos contables](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html#journal-entries)