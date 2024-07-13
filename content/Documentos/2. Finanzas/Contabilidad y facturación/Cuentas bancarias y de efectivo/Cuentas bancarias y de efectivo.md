En su base de datos puede administrar todas las cuentas bancarias o de efectivo que necesite. Si las configura de la manera adecuada, podrá tener toda su información bancaria al día y lista para la [conciliación](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/reconciliation.html) con sus asientos contables.

En Contabilidad de Odoo cada cuenta bancaria tiene un diario exclusivo para registrar todas las entradas en una cuenta específica. Tanto el diario como la cuenta se crean y configuran de forma automática cuando se agrega una cuenta bancaria.

 Nota

Los diarios y cuentas de efectivo deben configurarse manualmente.

Los diarios bancarios aparecen de forma predeterminada en el tablero de Contabilidad en forma de tarjetas que incluyen botones de acción.

![Los diarios bancarios aparecen en el tablero Contabilidad y contienen botones de acción.](https://www.odoo.com/documentation/17.0/es/_images/card.png)

## Administre sus cuentas bancarias y de efectivo.[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#manage-your-bank-and-cash-accounts "Enlazar permanentemente con este título")

### Conecte su banco para la sincronización automática.[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#connect-your-bank-for-automatic-synchronization "Enlazar permanentemente con este título")

Para conectar su cuenta bancaria a su base de datos, vaya a «Contabilidad -> Configuración -> Bancos: Agregar una cuenta bancaria», seleccione su banco en la lista, haga clic en «Conectar» y siga las instrucciones.

 Ver también

[Sincronización bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html)

### Crear una cuenta bancaria[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#create-a-bank-account "Enlazar permanentemente con este título")

Si su institución bancaria no está disponible en Odoo, o si no desea conectar su cuenta bancaria a su base de datos, puede configurar su cuenta bancaria de forma manual.

Para agregar de forma manual una cuenta bancaria, vaya a «Contabilidad -> Configuración -> Bancos: Agregar una cuenta bancaria», haga clic en «Crear» (en la parte inferior derecha) y complete el formulario.

 Nota

- Odoo detecta en automático el tipo de cuenta bancaria (por ejemplo, IBAN) y, por consiguiente, habilita algunas funciones.
    
- Hay disponible un diario bancario predeterminado que se puede utilizar para configurar su cuenta bancaria yendo a «Contabilidad -> Configuración -> Contabilidad: Diarios -> Bancos». Ábralo y edite los diferentes campos para que coincidan con la información de su cuenta bancaria.
    

### Crear un diario de efectivo[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#create-a-cash-journal "Enlazar permanentemente con este título")

Para crear un nuevo diario de efectivo, vaya a Contabilidad ‣ Configuración ‣ Contabilidad: Diarios, haga clic en Crear y seleccione Efectivo en el campo Tipo.

Para obtener más información sobre los campos de información contable, lea la sección [Configuración](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#bank-accounts-configuration) de esta página.

 Nota

Un diario de efectivo predeterminado está disponible y se puede utilizar de inmediato. Puede revisarlo yendo a Contabilidad ‣ Configuración ‣ Contabilidad: Diarios ‣ Efectivo.

### Editar un diario bancario o de efectivo existente[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#edit-an-existing-bank-or-cash-journal "Enlazar permanentemente con este título")

Para editar un diario bancario existente, vaya a Contabilidad ‣ Configuración ‣ Contabilidad: Diarios y escoja el diario que desea modificar.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#configuration "Enlazar permanentemente con este título")

Puede editar la información contable y el número de cuenta bancaria de acuerdo con sus necesidades.

![Configure manualmente su información bancaria](https://www.odoo.com/documentation/17.0/es/_images/bank-journal-config.png)

 Ver también

- [Sistema multidivisa](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/multi_currency.html)
    
- [Transacciones](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html)
    

### Cuenta transitoria[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#suspense-account "Enlazar permanentemente con este título")

Las transacciones del extracto bancario se registran en la :guilabel:[`](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#id1)Cuenta transitoria hasta que la conciliación final permita encontrar la cuenta correcta.

### Cuentas del estado de resultados[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#profit-and-loss-accounts "Enlazar permanentemente con este título")

La Cuenta de ganancias se utiliza para registrar una ganancia cuando el saldo final de una caja registradora difiere del que el sistema calcula, mientras que la Cuenta de pérdidas se utiliza para registrar una pérdida cuando el saldo final de una caja registradora difiere del que el sistema calcula.

### Moneda[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#currency "Enlazar permanentemente con este título")

Puede editar la moneda utilizada para ingresar los extractos.

 Ver también

[Sistema multidivisa](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/multi_currency.html)

### Número de cuenta[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#account-number "Enlazar permanentemente con este título")

Si necesita **editar los detalles de su cuenta bancaria**, haga clic en la flecha de enlace externo junto a su Número de cuenta. En la nueva página, haga clic en la flecha de enlace externo junto a su Banco y actualice tu información bancaria como corresponda. Estos detalles se utilizan al registrar los pagos.

![Edite su información bancaria](https://www.odoo.com/documentation/17.0/es/_images/bank-account-number.png)

### Conexiones bancarias[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#bank-feeds "Enlazar permanentemente con este título")

Conexiones bancarias define cómo se registran los estados de cuenta bancarios. Hay tres opciones disponibles:

- Aún no definido, debe seleccionarse cuando aún no se sabe si se sincronizará o no la cuenta bancaria con la base de datos.
    
- Importar (CAMT, CODA, CSV, OFX, QIF), debe seleccionarse si se desea importar el estado de cuenta bancario utilizando un formato diferente.
    
- Sincronización bancaria automatizada, debe seleccionarse si su banco está sincronizado con la base de datos.
    

 Ver también

- [Sincronización bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html)
    
- [Transacciones](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html)
    

## Cuentas pendientes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#outstanding-accounts "Enlazar permanentemente con este título")

De forma predeterminada, los pagos se registran a través de cuentas transitorias llamadas **cuentas pendientes** antes de registrarlos en su cuenta bancaria.

- Una **cuenta de pagos pendientes** es donde se registran los pagos salientes hasta que se vinculan con un retiro de su estado de cuenta bancario.
    
- Una **cuenta de cobros pendientes** es donde se registran los pagos entrantes hasta que se vinculan con un depósito en su estado de cuenta bancario.
    

Estas cuentas deben ser del [tipo](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/chart_of_accounts.html#chart-of-account-type) Activos corrientes.

 Nota

El movimiento desde una cuenta pendiente a una cuenta bancaria se realiza automáticamente cuando concilia la cuenta bancaria con un estado de cuenta bancario.

### Configuración predeterminada de cuentas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#default-accounts-configuration "Enlazar permanentemente con este título")

Las cuentas pendientes se definen de manera predeterminada. Si es necesario, puede actualizarlas yendo a Contabilidad ‣ Configuración ‣ Configuración ‣ Cuentas predeterminadas y actualizar su Cuenta de cobros pendientes y Cuenta de pagos pendientes.

### Configuración de diarios bancarios y en efectivo[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html#bank-and-cash-journals-configuration "Enlazar permanentemente con este título")

También puede establecer cuentas pendientes específicas para cualquier diario del [tipo](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/chart_of_accounts.html#chart-of-account-type) Banco o Efectivo.

Desde el Tablero de control de Contabilidad, haga clic en la selección de menú ⋮ del diario que desea configurar, y haga clic en Configuración, luego abra la pestaña Pagos entrantes/salientes. Para mostrar la columna de cuentas pendientes, haga clic en el botón de alternancia y marque la casilla de Cuentas de cobros/pagos pendientes, luego actualice la cuenta.

![Seleccione el botón de alternancia y haga clic en Cuentas pendientes](https://www.odoo.com/documentation/17.0/es/_images/toggle-button1.png)

 Nota

- Si no especifica una cuenta de pagos pendientes o una cuenta de cobros pendientes para un diario específico, Odoo utilizará las cuentas pendientes predeterminadas.
    
- Si su cuenta bancaria principal se agrega como una cuenta de cobros pendientes o una cuenta de pagos pendientes, cuando se registra un pago, el estado de la factura o el recibo se establece directamente en Pagado.