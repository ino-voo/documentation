Importar transacciones desde sus estados de cuenta bancarios permite hacer un seguimiento de las transacciones de la cuenta bancaria y conciliarlas con las registradas en su contabilidad.

La [sincronización bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html) automatiza el proceso. Sin embargo, si no desea utilizarlo o si su banco aún no es compatible, existen otras opciones:

- [Importar transacciones bancarias](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html#transactions-import) proporcionadas por su banco;
    
- [Registrar transacciones bancarias](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html#transactions-register) de forma manual.
    

 Nota

La [agrupación de transacciones por estado de cuenta](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html#transactions-statements) es opcional.

## Importar transacciones[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html#import-transactions "Enlazar permanentemente con este título")

Odoo admite múltiples formatos de archivo para importar transacciones:

- Formato de gestión de efectivo recomendado por SEPA (CAMT.053);
    
- Valores separados por coma (.CSV);
    
- Open Financial Exchange (.OFX);
    
- Quicken Interchange Format (.QIF);
    
- Bélgica: Coded Statement of Account (.CODA).
    

Para importar un archivo vaya al **tablero de Contabilidad** y en el diario Banco haga clic en Importar archivo.

 Truco

También puede:

- hacer clic en ⋮ en el diario Banco y después seleccionar Importar archivo.
    
- Acceda a la lista de transacciones con el icono ⋮ en el diario Banco y seleccione Transacciones. Haga clic en el icono de engranaje (⚙) y seleccione Importar registros.
    
    ![Importe transacciones bancarias desde el diario de banco](https://www.odoo.com/documentation/17.0/es/_images/import-transactions.png)
    

Después, seleccione al archivo y súbalo.

Después de configurar las opciones de formato necesarias y mapear las columnas del archivo con los campos relacionados en Odoo, puede correr una prueba e import sus transacciones bancarias.

 Ver también

[Exportar e importar datos](https://www.odoo.com/documentation/17.0/es/applications/essentials/export_import_data.html)

## Registrar transacciones bancarias manualmente[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html#register-bank-transactions-manually "Enlazar permanentemente con este título")

También puede registrar sus transacciones bancarias de manera manual. Para hacerlo, vaya al tablero de contabilidad, haga clic en el diario bancario y después en Nuevo. Asegúrese de llenar los campos partner y etiqueta para facilitar el proceso de conciliación.

## Estados de cuenta[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html#statements "Enlazar permanentemente con este título")

Un **estado bancario** es un documento que un banco o una institución financiera crean en el que se enlistan las transacciones que se realizaron en una cuenta bancaria en particular durante un periodo específico.

En nuestra aplicación de Contabilidad es opcional agrupar las transacciones según el estado de cuenta en el que aparecen, pero dependiendo del flujo de su negocio, puede que quiera registrarlas para llevar un buen control de dichas transacciones.

 Importante

Si quiere comparar los balances finales de sus estados bancarios con los de sus registros financieros, _no se le olvide crear una transacción de apertura_ para registrar el balance de su cuenta de banco desde la fecha en la que empezó a sincronizar o importar transacciones. Este paso es necesario para que su contabilidad sea correcta.

Para acceder a la lista de estados, vaya al tablero de contabilidad, haga clic en los tres puntos (⋮) junto al diario de banco o efectivo que quiere revisar y después vaya a Estados de cuenta.

### Creación de estados de cuenta desde la vista de kanban[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html#statement-creation-from-the-kanban-view "Enlazar permanentemente con este título")

Haga clic en el nombre del diario de banco para abrir la vista de conciliación bancaria. Identifique la transacción correspondiente a la última transacción en su estado bancario. Haga clic en el botón ESTADO DE CUENTA que aparece al pasar el ratón encima de la línea de separación superior.

![Al colocar el cursor arriba de la línea que separa dos transacciones podrá ver un botón "ESTADO DE CUENTA".](https://www.odoo.com/documentation/17.0/es/_images/statements-kanban.png)

Llene los detalles del estado de cuenta y guárdelos. El estado de cuenta que se acaba de crear incluye las transacciones previas desde el último estado de cuenta.

### Creación de estado de cuenta desde la vista de lista[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html#statement-creation-from-the-list-view "Enlazar permanentemente con este título")

Haga clic en el nombre del diario de banco para abrir la lista de transacciones y cambie a la vista de lista. Seleccione todas las transacciones correspondientes al estado de cuenta bancario y en la columna Estado de cuenta seleccione un estado existente o escriba una referencia y cree uno nuevo en Crear y editar…, donde tendrá que llenar los detalles del estado de cuenta para después guardarlos