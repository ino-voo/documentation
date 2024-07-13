La **conciliación bancaria** es el proceso de conciliar sus [transacciones bancarias](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html) con los registros de su empresa, como las [facturas de clientes](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices.html), [de proveedores](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills.html) y [pagos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html). No solo es obligatorio para la mayoría de las empresas, sino que también ofrece varias ventajas, como la reducción del riesgo de errores en los reportes financieros, la detección de actividades fraudulentas y la mejora de la gestión del flujo de caja.

Gracias a los modelos de [conciliación bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation_models.html), Odoo preselecciona los asientos a conciliar de forma automática.

 Ver también

- [Tutoriales de Odoo: conciliación bancaria](https://www.odoo.com/slides/slide/bank-reconciliation-2724)
    
- [Sincronización bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html)
    
- transacciones
    

## Vista de conciliación bancaria[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#bank-reconciliation-view "Enlazar permanentemente con este título")

Para acceder a la **vista de conciliación** de un diario bancario, vaya al tablero de Contabilidad y:

- haga clic en el nombre del diario (por ejemplo, banco) para mostrar todas las transacciones, incluidas las que ya están conciliadas, o
    
- haga clic en el botón Conciliar apuntes para mostrar todas las transacciones preseleccionadas por Odoo para la conciliación. Puede eliminar el filtro no conciliadas de la barra de búsqueda para incluir transacciones ya conciliadas.
    

![Imagen donde se muestra cómo acceder a la herramienta de conciliación bancaria desde el tablero de la aplicación Contabilidad.](https://www.odoo.com/documentation/17.0/es/_images/bank-card.png)

La vista de la conciliación bancaria se estructura en tres secciones diferentes: transacciones, asientos de contrapartida y el asiento resultante.

![La interfaz del usuario de la vista de una conciliación en un diario bancario.](https://www.odoo.com/documentation/17.0/es/_images/user-interface.png)

Transacciones

La sección de transacciones que se encuentra a la izquierda muestra todas las transacciones bancarias y la más reciente aparece primero. Haga clic en una transacción para seleccionarla.

Asientos de contrapartida

La sección de asientos de contrapartida que se encuentra en la parte inferior derecha muestra las opciones para conciliar la transacción bancaria seleccionada. Están disponibles varias pestañas, entre las que se encuentran [Conciliar asientos existentes](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-existing-entries), [Pagos por lotes](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-batch-payments), [Operaciones manuales](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-manual-operations) y Conversaciones, en esta última encontrará el chatter de la transacción bancaria seleccionada.

Asiento resultante

La sección de asiento resultante en la parte superior derecha muestra la transacción bancaria seleccionada con los asientos de contrapartida e incluye cualquier cargo o abono restante. En esta sección, puede validar la conciliación o marcarla como por revisar. Todos los [botones de los modelos de conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-button) también están disponibles en la sección del asiento resultante.

## Conciliar transacciones[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconcile-transactions "Enlazar permanentemente con este título")

Las transacciones se pueden conciliar de forma automática con el uso de [los modelos de conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation_models.html), o se pueden conciliar con [asientos existentes](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-existing-entries), [pagos por lote](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-batch-payments), [operaciones manuales](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-manual-operations) y [botones de modelo de conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-button).

1. Seleccione una transacción de entre varias transacciones bancarias no conciliadas.
    
2. Defina la contrapartida. Hay varias opciones para esto, incluyendo [conciliar asientos existentes](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-existing-entries), [operaciones manuales](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-manual-operations), [pagos por lote](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-batch-payments), y [botones del modelo de conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-button).
    
3. Si el asiento resultante no está saldado en su totalidad, puede agregar un asiento de contrapartida existente o anularlo mediante una [operación manual](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-manual-operations).
    
4. Haga clic en el botón Validar para confirmar la conciliación y seguir con la siguiente transacción.
    

 Truco

Si no está seguro de cómo conciliar una transacción en particular y quiere trabajar con ella después, use el botón por revisar. Todas las transacciones que marque como por revisar aparecen si elige el filtro por revisar.

 Nota

Las transacciones bancarias se registran en la **cuenta transitoria del diario** hasta que se concilien. En este momento, la conciliación modifica el asiento contable de la transacción. Para hacerlo, se reemplaza la cuenta transitoria del banco con la cuenta por cobrar, por pagar o pendiente correspondiente.

### Conciliar asientos existentes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#match-existing-entries "Enlazar permanentemente con este título")

Esta pestaña contiene los asientos conciliados que Odoo selecciona de manera automática según los modelos de conciliación. El orden del asiento se basa en los modelos de conciliación, pero los asientos sugeridos aparecerán primero.

 Truco

La barra de búsqueda dentro de la pestaña conciliar asientos existentes le permite buscar apuntes contables específicos.

### Pagos por lotes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#batch-payments "Enlazar permanentemente con este título")

Con [los pagos por lote](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/payments/batch-payments) podrá agrupar diferentes pagos para facilitar la conciliación. Use la pestaña pagos por lote para encontrar los pagos por lote de clientes y proveedores. Así como la pestaña emparejar asientos existentes la pestaña pagos por lote tiene una barra de búsqueda que le permite buscar pagos por lotes específicos.

### Operaciones manuales[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#manual-operations "Enlazar permanentemente con este título")

Si no hay un asiento existente para conciliar con la transacción seleccionada, puede hacerlo de forma manual, solo tiene que seleccionar la cuenta y el importe correcto. Después, complete todos los campos opcionales que sean necesarios.

 Truco

Puede usar la opción totalmente pagado para conciliar un pago, incluso si solo ha recibido un pago parcial. Aparecerá una nueva línea en la sección del asiento resultante para que mostrará el saldo pendiente que se registró en la cuenta por cobrar de forma predeterminada. Para elegir otra cuenta haga clic en la línea nueva que se encuentra en la sección del asiento resultante y seleccione la Cuenta para registrar este saldo.

 Nota

Las líneas se concilian de forma automática a menos que se requiera un asiento de cancelación, lo que inicia las acciones del asistente de reconciliación.

![Haga clic en marcar como totalmente pagado para que la facture se marque como pagada.](https://www.odoo.com/documentation/17.0/es/_images/fully-paid.png)

### Botones del modelo de conciliación[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html#reconciliation-model-buttons "Enlazar permanentemente con este título")

Use el [botón del modelo de conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation_models.html) para operaciones manuales que se usan con frecuencia. Estos botones personalizados le permitirán conciliar transacciones bancarias de manera eficaz y manual, además de que se pueden usar con asientos ya existentes.