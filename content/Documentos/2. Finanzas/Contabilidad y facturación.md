La aplicación **Facturación de Odoo** es una aplicación autónoma para crear facturas, enviárselas a sus clientes y gestionar pagos.

**Contabilidad de Odoo** es una aplicación con funciones de contabilidad completas. La productividad contable es el enfoque al desarrollar las diferentes funciones, como facturas reconocidas por inteligencia artificial, sincronización con sus cuentas bancarias, coincidencias inteligentemente sugeridas, etc.

 Ver también

[Tutoriales de Odoo: Contabilidad](https://www.odoo.com/slides/accounting-19)

[

#### Get started

Basic concepts of accounting and initial setup of your accounting



](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started.html)[

#### Taxes

Taxes, fiscal positions, and integrations



](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html)[

#### Customer invoices

Customer invoices, payment terms, and electronic invoicing



](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices.html)[

#### Vendor bills

Vendor bills, assets, and invoice digitization (OCR)



](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills.html)[

#### Payments

Invoices and bills payments (online, checks, batches) and follow-up on invoices



](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/payments.html)[

#### Bank and cash accounts

Bank synchronization, reconciliation, and cash registers



](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html)[

#### Reporting

Reporting, declarations, and analytic accounting



](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting.html)

## Contabilidad de doble entrada[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#double-entry-bookkeeping "Enlazar permanentemente con este título")

Odoo crea de manera automática todos los asientos de diarios de todas las transacciones de contabilidad, como facturas, órdenes del punto de venta, gastos, valoraciones del inventario, etc.

Odoo usa el sistema de partida doble, donde cada asiento requiere una contraparte en una cuenta diferente, con una cuenta de débito y otra de crédito. De esta manera nos aseguramos de que todas las transacciones se registran debidamente y de que todas las cuentas siempre están balanceadas.

 Ver también

[Hoja de referencia de contabilidad](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/cheat_sheet.html)

## Base de devengo y efectivo[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#accrual-and-cash-basis "Enlazar permanentemente con este título")

En Odoo es posible llevar la contabilidad con base de devengo y de efectivo. De esta manera podrá reportar un ingreso y un gasto ya sea cuando ocurra una transacción (base de devengo) o cuando se reciba un pago (base de efectivo).

 Ver también

[Base de efectivo](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/cash_basis.html)

## Multiempresa[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#multi-company "Enlazar permanentemente con este título")

Es posible gestionar varias empresas dentro de una misma base de datos de Odoo. Cada empresa tiene su propio [plan de cuentas](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/chart_of_accounts.html), que también es útil para generar reportes de consolidación. Los usuarios tienen acceso a varias empresas, pero solo pueden trabajar en la contabilidad de una empresa a la vez.

## Entorno multidivisa[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#multi-currency-environment "Enlazar permanentemente con este título")

En Odoo está disponible un entorno [multidivisa](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/multi_currency.html) con una tasa de cambio automática que facilita las transacciones internacionales. Cada transacción se registra de forma automática en la divisa de la empresa. Para las transacciones que se realizan en otra divisa, Odoo almacena el valor tanto en la divisa que se usa en la empresa como la divisa de la transacción en sí. Además, genera las ganancias y pérdidas de la divisa después de conciliar los apuntes contables.

 Ver también

[Gestionar un banco en una divisa extranjera](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/foreign_currency.html)

## Administración de sucursales[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#branch-management "Enlazar permanentemente con este título")

Puede gestionar varias sucursales gracias a las jerarquías multiempresa. Esto le permite publicar asientos contables en cada sucursal así como configurar una fecha de bloqueo administrada por la empresa principal.

## Estándares internacionales[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#international-standards "Enlazar permanentemente con este título")

Es posible utilizar Contabilidad de Odoo en más de 70 países. La aplicación contiene los mecanismos y estándares que son comunes en todas las naciones. Además, gracias a que es posible instalar módulos específicos para cada país, es fácil cumplir con todos los requisitos locales. Las posiciones fiscales existen para poder gestionar cuestiones específicas de cada región, como lo es el plan de cuentas, los impuestos y cualquier otro requerimiento.

 Ver también

[Paquetes de localización fiscal](https://www.odoo.com/documentation/17.0/es/applications/finance/fiscal_localizations.html)

## Cuentas por pagar y por cobrar[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#accounts-receivable-and-payable "Enlazar permanentemente con este título")

De forma predeterminada, hay una sola cuenta para los asientos de cuentas por cobrar y otra para los asientos de cuentas por pagar. Como las transacciones están vinculadas a sus **contactos**, puede realizar un reporte por cliente, proveedor o distribuidor.

El reporte del **libro mayor de la empresa** muestra el balance de sus clientes y proveedores. Lo puede encontrar en Contabilidad ‣ Reportes ‣ Libro mayor de la empresa.

## Reportes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#reporting "Enlazar permanentemente con este título")

Estos [reportes financieros](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting.html) están disponibles y se actualizan en tiempo real:

|Reportes financieros|   |
|---|---|
|Estado de cuenta|Balance general|
|Estado de resultados|
|Estado de flujo de efectivo|
|Reporte de impuestos|
|Declaración recapitulativa de operaciones intracomunitarias|
|Auditar|Libro mayor|
|Balanza de comprobación|
|Reporte de diario|
|Reporte Intrastat|
|Registro de caja|
|Contacto|Libro mayor de la empresa|
|Cuenta antigua por cobrar|
|Cuenta antigua por pagar|
|Administración|Análisis de factura|
|Ganancias/pérdidas de divisa no realizadas|
|Programa de depreciación|
|Gastos rechazados|
|Análisis de presupuesto|
|Márgenes de producto|
|Reporte 1099|

 Truco

[Cree y personalice reportes](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/customize.html) con el motor de reportes de Odoo.

### Reporte de impuestos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#tax-report "Enlazar permanentemente con este título")

Odoo calcula todas las transacciones de contabilidad del periodo fiscal específico y usa los totales para calcular las obligaciones relativas a los impuestos.

 Importante

Una vez que se crea el reporte de impuestos para un periodo, Odoo lo bloquea y evita que se creen nuevos asientos que incluyan IVA. Si necesita corregir cualquier factura, lo tendrá que hacer en el siguiente periodo.

 Nota

Dependiendo de la localización del país, es posible generar una versión XML del reporte de impuestos para poder subirla a la plataforma de IVA de la autoridad fiscal correspondiente.

## Sincronización bancaria[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#bank-synchronization "Enlazar permanentemente con este título")

El sistema de sincronización bancaria se conecta directamente a su institución bancaria, de esta forma puede importar todas las transacciones directamente a su base de datos. Podrá obtener un resumen de su flujo de efectivo sin tener que iniciar sesión en su sistema de banca en línea y sin tener que esperar a que le entreguen sus estados de cuenta físicos.

 Ver también

[Sincronización bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html)

## Valuación de inventario[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#inventory-valuation "Enlazar permanentemente con este título")

En Odoo se pueden realizar tanto valuaciones de inventario de forma periódica (manuales) o permanente (automáticas). Los métodos disponibles son precio estándar, precio promedio, UEPS y FIFO.

 Ver también

[Valoración automática de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html)

## Ganancias retenidas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#retained-earnings "Enlazar permanentemente con este título")

Las ganancias retenidas son la porción de los ingresos que un negocio retiene. Odoo calcula las ganancias del año actual en tiempo real, así que no se necesita un diario de final de año ni renovación. El estado de resultados se reporta de manera automática en el reporte del balance general.

 Ver también

[Hoja de referencia de contabilidad](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/cheat_sheet.html)

## Fiduciarias[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#fiduciaries "Enlazar permanentemente con este título")

El modo de empresas de contabilidad se puede activar desde Contabilidad ‣ Configuración ‣ Ajustes ‣ Modo de empresas de contabilidad. Cuando lo active:

- Es posible editar la secuencia del documento en cada uno de ellos.
    
- Aparecerá un nuevo campo llamado Total (impuestos incluidos) con el que será posible acelerar y controlar la codificación, ya que las líneas se crearán de inmediato con la cuenta y el impuesto correctos;
    
- Al codificar una transacción, el campo Fecha de la factura se llena de manera predeterminada.
    
- La opción de Codificación rápida está disponible en sus facturas.