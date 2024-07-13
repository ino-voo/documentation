En Odoo, cada transacción se registra en la divisa predeterminada de la empresa y los reportes están basados en ella. Odoo almacena dos valores para cada transacción cuando tiene una cuenta bancaria en una divisa extranjera:

- El débito y crédito en la divisa de la _empresa_.
    
- El débito y crédito en la divisa de la _cuenta bancaria_.
    

Las tasas de cambio se actualizan en automático con los servicios web de una institución bancaria. Odoo usa los servicios web del Banco Central Europeo de forma predeterminada, pero hay otras opciones disponibles.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/foreign_currency.html#configuration "Enlazar permanentemente con este título")

### Activar multidivisas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/foreign_currency.html#activate-multi-currencies "Enlazar permanentemente con este título")

Para trabajar con varias divisas, vaya a Contabilidad ‣ Configuración ‣ Configuración ‣ Divisas y seleccione Multidivisas. Luego, en Registrar diferencias de cambio en:, indique un diario, una cuenta de ganancias, una cuenta de pérdidas y luego haga clic en Guardar.

### Configurar divisas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/foreign_currency.html#configure-currencies "Enlazar permanentemente con este título")

Una vez que configuró Odoo para que sea compatible con varias divisas, todas se crean de forma predeterminada, pero eso no significa que están activas. Para activar las nuevas divisas, haga clic en Activar otras divisas en la configuración de Multidivisas o vaya a Contabilidad ‣ Configuración ‣ Contabilidad: Divisas.

Al activar las divisas puede elegir **automatizar** la actualización de las tasas de cambio o dejarla en modo **manual**. Para configurar la actualización de tasas, regrese a Contabilidad ‣ Configuración ‣ Configuración ‣ Divisas, seleccione la opción Tasas de cambio automáticas, establezca el intervalo según la frecuencia que necesite y luego haga clic en Guardar. También puede elegir el servicio del cual desea obtener las tasas de cambio.

Haga clic en el botón Actualizar ahora (🔄) junto al campo Siguiente ejecución para actualizar las tasas de cambio de forma manual.

### Crear una nueva cuenta bancaria[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/foreign_currency.html#create-a-new-bank-account "Enlazar permanentemente con este título")

En la aplicación Contabilidad, vaya a Contabilidad ‣ Configuración ‣ Diarios y cree uno nuevo. Ingrese un Nombre del diario y establezca el Tipo como `Banco`. En la pestaña Asientos contables, ingrese un **código corto**, una **divisa** y, por último, haga clic en el campo Cuenta bancaria para crear una cuenta nueva. En la ventana emergente de creación de cuenta, ingrese un nombre, un código (por ejemplo: 550007), establezca su tipo como `Banco y efectivo`, elija un tipo de divisa y guarde los cambios. Cuando esté de nuevo en el **diario**, haga clic en el campo Número de cuenta y en la ventana emergente, complete el Número de cuenta, el Banco de su cuenta y guarde los cambios.

![Ejemplo de un diario bancario creado.](https://www.odoo.com/documentation/17.0/es/_images/foreign-journal.png)

Después de crear el diario, Odoo vincula de manera automática la cuenta bancaria. Puede encontrarlo en Contabilidad ‣ Configuración ‣ Contabilidad: Plan de cuentas.

## Factura de proveedor en divisa extranjera[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/foreign_currency.html#vendor-bill-in-a-foreign-currency "Enlazar permanentemente con este título")

Para pagar una factura en divisa extranjera, solo seleccione la divisa junto al campo Diario y registre el pago. Odoo crea y contabiliza de manera automática la **ganancia o pérdida de cambio** como un nuevo asiento contable.

![Cómo establecer la divisa de una factura.](https://www.odoo.com/documentation/17.0/es/_images/foreign-bill-currency.png)

 Nota

Tenga en cuenta que puede pagar una factura extranjera con otra divisa. En ese caso, Odoo realiza la conversión entre ambas divisas de forma automática.

## Reporte de ganancias y pérdidas cambiarias no realizadas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/foreign_currency.html#unrealized-currency-gains-losses-report "Enlazar permanentemente con este título")

Este reporte le proporciona un resumen de todos los montos no realizados en una divisa extranjera en su balance general y le permite ajustar un asiento o establecer una tasa de cambio de forma manual. Para acceder a este reporte, vaya a Reportes‣ Gestión: Ganancias/pérdidas de divisa no realizadas. Desde allí podrá acceder a todos los asientos abiertos de su **balance general**.

![Vista del diario de ganancias/pérdidas no realizadas.](https://www.odoo.com/documentation/17.0/es/_images/foreign-gains-losses.png)

Si desea utilizar una tasa de cambio distinta a la establecida vaya a Contabilidad ‣ Configuración ‣ Ajustes ‣ Divisas, haga clic en el botón Tasas de cambio y modifique la tasa de las divisas extranjeras en el reporte.

![Menú para cambiar de forma manual las tasas de cambio.](https://www.odoo.com/documentation/17.0/es/_images/foreign-exchange-rates.png)

Cuando cambie las **tasas de cambio** de forma manual, aparecerá un recuadro amarillo que le permitirá restablecer la tasa de cambio de Odoo. Para ello, solo haga clic en Restablecer a la tasa de Odoo.

![Recuadro para restablecer las tasas de cambio de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/foreign-reset-rates.png)

Para actualizar su **balance general** con el importe de la columna ajuste, haga clic en el botón Asiento de ajuste. En la ventana emergente, seleccione un Diario, una Cuenta de gastos y una Cuenta de ingresos para calcular y procesar las **ganancias y pérdidas no realizadas**.

Puede establecer la fecha del reporte en el campo Fecha. De forma automática, Odoo revertirá el asiento contable a la fecha establecida en Fecha de reversión.

Una vez contabilizado, la columna ajuste debería indicar `0.00`, lo que significa que todas las **ganancias/pérdidas no realizadas** han sido ajustadas.

![Reporte de ganancias/pérdidas de cambio no realizadas una vez ajustado.](https://www.odoo.com/documentation/17.0/es/_images/foreign-adjustment.png)