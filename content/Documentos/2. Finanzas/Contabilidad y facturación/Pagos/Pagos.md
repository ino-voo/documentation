En Odoo, los pagos se pueden vincular de manera automática con una factura o se pueden dejar como registros separados que se usarán en otra fecha.

- Si un pago está **vinculado a una factura** entonces la cantidad por pagar de la factura se reducirá o liquidará. Puede tener muchos pagos relacionados a la misma factura.
    
- Si un pago **no está ligado a una factura**. el cliente tendrá un crédito pendiente con su empresa, o su empresa tendrá un crédito pendiente con un proveedor. Puede usar esas cantidades pendientes para reducir o liquidar facturas sin pagar.
    

 Ver también

- [Transferencias internas](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/internal_transfers.html)
    
- [Conciliación bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html)
    
- [Tutoriales de Odoo: configuración bancaria](https://www.odoo.com/slides/slide/bank-configuration-1880)
    

## Registrar un pago para una factura[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html#registering-payment-from-an-invoice-or-bill "Enlazar permanentemente con este título")

Cuando haga clic en el botón Registrar pago que aparece en una factura, se genera un asiento contable y se cambia la cantidad que se debe según la cantidad que se pagó. La contrapartida se refleja en la cuenta de **recibos** o **pagos** [pendientes](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#bank-outstanding-accounts). En este momento es cuando se marca la factura como En proceso de pago. Después, cuando la cuenta pendiente se concilie con la línea del estado de cuenta bancario, la factura cambiará al estado Pagado.

El icono de información en la línea de pago muestra más información sobre el pago. Para ver información adicional. como el diario relacionado, haga clic en Vista.

![Ver información de pago detallada.](https://www.odoo.com/documentation/17.0/es/_images/information-icon.png)

 Nota

- Para poder registrar el pago la factura debe estar en el estado Publicado.
    
- Si quita la conciliación de un pago seguirá apareciendo en sus libros pero ya no estará ligado a ninguna factura.
    
- Si concilia o quita la conciliación de un pago en una divisa diferente, se crea un asiento de diario de manera automática para publicar la cantidad de pérdidas y ganancias tras el cambio de divisas.
    
- Si concilia o quita la conciliación de un pago y una factura si tiene impuestos con base en efectivo, se crea un asiento de diario de manera automática para publicar la cantidad de impuestos con base en efectivo.
    

 Truco

- Si su cuenta bancaria principal está configurada como [Cuenta pendiente](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#bank-outstanding-accounts) y el pago se registra en Odoo (no a través de una cuenta bancaria relacionada), entonces las facturas se registran de manera automática con el estado Pagado.
    

## Registrar pagos que no están ligados a una factura[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html#registering-payments-not-tied-to-an-invoice-or-bill "Enlazar permanentemente con este título")

Cuando se registra un nuevo pago a través del menú Clientes / Proveedores ‣ Pagos, este pago no se vinculará de inmediato a una factura. En su lugar, las cuentas por pagar o las cuentas por cobrar se concilian con las **cuentas pendientes** hasta que se concilien de manera manual con la factura relacionada.

### Vincular facturas con pagos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html#matching-invoices-and-bills-with-payments "Enlazar permanentemente con este título")

Cuando valida una nueva factura y hay un **pago pendiente** (ya sea que el cliente no haya pagado o usted no haya pagado al proveedor) aparecerá una cinta azul. Para vincular la factura solo haga clic en Añadir en Créditos pendientes o Débitos pendientes.

![Muestra la opción AGREGAR para conciliar una factura con un pago.](https://www.odoo.com/documentation/17.0/es/_images/add-option.png)

La factura ahora se marca como En proceso de pago hasta que se haya conciliado con el extracto bancario correspondiente.

### Pago en lote[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html#batch-payment "Enlazar permanentemente con este título")

Los pagos en lote le permiten agrupar varios pagos para facilitar la [conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html). También ayudan mucho cuando hay que depositar [cheques](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/checks.html) en el banco o para [pagos SEPA](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/pay_sepa.html). Para crear pagos en lote vaya a Contabilidad ‣ Clientes ‣ Pagos por lote o Contabilidad ‣ Proveedores ‣ Pagos por lote. En la vista de lista de los pagos puede seleccionarlos y agruparlos en lote, haga clie en Acción ‣ Crear pago por lotes.

 Ver también

- [Pagos por lote para depósitos bancarios](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/batch.html)
    
- [Pagos por lotes: domiciliación bancaria SEPA (SDD)](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments/batch_sdd.html)
    

### Emparejamiento de pagos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html#payments-matching "Enlazar permanentemente con este título")

La herramienta Emparejamiento de pagos abre todas las facturas sin conciliar y podrá procesar todas individualmente, ya que podrá vincular los pagos con las facturas a la vez en un mismo lugar. Para usar esta herramienta vaya al Tablero de contabilidad ‣ Facturas de cliente y de proveedor, haga clic en el menú desplegable ⋮ y seleccione Emparejamiento de pagos, o en Contabilidad ‣ Conciliación.

![Menú de conciliación de pagos en el menú desplegable.](https://www.odoo.com/documentation/17.0/es/_images/payments-journal.png)

 Nota

Durante la [conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html), si la suma de los cargos y los abonos no cuadra queda el balance restante. Este balance se tiene que conciliar después o se tiene que borrar.

### Conciliación de pagos por lote[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html#batch-payments-matching "Enlazar permanentemente con este título")

Puede usar la **función de conciliación bancaria por lotes** para conciliar varios pagos o facturas pendientes de forma simultánea para un cliente o proveedor específico. Vaya al **tablero de Contabilidad** y abra su **diario bancario**. En la vista **conciliación bancaria** seleccione una **transacción** y haga clic en la pestaña Pagos por lotes, allí podrá conciliar sus pagos por lotes <payments/batch> con sus pagos o facturas pendientes.

![La opción para conciliar el pago en lote](https://www.odoo.com/documentation/17.0/es/_images/reconcile-option.png)

## Registrar un pago parcial[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html#registering-a-partial-payment "Enlazar permanentemente con este título")

Para registrar un **pago parcial**, haga clic en Registrar pago en la factura relacionada e ingrese el importe recibido o pagado. Al ingresar el importe aparecerá un mensaje que le pedirá que decida si Mantener abierta la factura o Marcar como pagado en su totalidad. Seleccione Mantener abierta y haga clic en Crear pago y la factura se marcará como Parcial. Seleccione Marcar como pagado en su totalidad si desea saldar la factura con una diferencia en el importe.

![Pago parcial de una factura.](https://www.odoo.com/documentation/17.0/es/_images/payment-difference.png)

## Conciliar pagos con estados de cuenta bancarios[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html#reconciling-payments-with-bank-statements "Enlazar permanentemente con este título")

Después de registrar el pago, el estado de la factura será En proceso de pago. Después, [concilie](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html) el pago con la línea del estado de cuenta bancario relacionado para finalizar la transacción y hacer que la factura se marque como Pagado.