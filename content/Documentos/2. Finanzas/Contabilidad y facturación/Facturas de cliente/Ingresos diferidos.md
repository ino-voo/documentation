Los **ingresos diferidos**, **ingresos no generados**, son facturas que se hacen a los clientes por bienes que todavía no se entregan o servicios que todavía no se han prestado.

La empresa no puede reportarlos en el **reporte o estado de resultados** actual, ya que los bienes y servicios se entregarán, o prestarán, en el futuro.

Estos ingresos futuros deben diferirse en el saldo de la empresa, junto con los pasivos actuales hasta que se puedan **reconocer**, al mismo tiempo o a lo largo de un periodo definido, en el estado de resultados.

Por ejemplo, digamos que una empresa vende una licencia de software de 1 año en $1,200. La factura al cliente se realiza de inmediato, pero todavía no se puede considerar como ganancia porque los meses futuros de la licencia no se han entregado. Por lo tanto, publican este nuevo ingreso en una cuenta de ingresos no generados y se reconoce todos los meses; durante los siguientes 12 meses se reconocerá como un ingreso de $100 cada mes.

La aplicación Contabilidad de Odoo distribuye los ingresos diferidos en varios asientos que se contabilizan de forma periódica.

 Nota

El servidor revisa una vez al día si un asiento debe contabilizarse. Pueden pasar hasta 24 horas antes de que vea el cambio de Borrador a Publicado.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/deferred_revenues.html#configuration "Enlazar permanentemente con este título")

Asegúrese de que los ajustes predeterminados están bien configurados para su negocio. Para hacerlo, vaya a Contabilidad ‣ Configuración ‣ Ajustes. Las opciones disponibles:

Diario

Los asientos diferidos se publican en este diario.

Cuenta de gastos diferidos

Los gastos en la cuenta de activos actual están diferidos hasta que se reconozcan.

Cuenta de ingresos diferidos

Los ingresos en la cuenta de activos actual están diferidos hasta que se reconozcan.

Generar asientos

Odoo [genera en automático](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/deferred_revenues.html#customer-invoices-deferred-generate-on-validation) y de forma predeterminada los asientos diferidos cuando registra la factura de un cliente. Sin embargo, si desea [generarlos de forma manual](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/deferred_revenues.html#customer-invoices-deferred-generate-manually) debe seleccionar la opción Manual y agrupados.

Cálculo de importe

Supongamos que una factura de $1,200 debe deferirse en 12 meses. El cálculo de Igual por mes cuenta $100 al mes, mientras que el cálculo Según los días cuenta las diferentes cantidades según el número de días de cada mes.

## Genere asientos diferidos al validarlos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/deferred_revenues.html#generate-deferral-entries-on-validation "Enlazar permanentemente con este título")

 Truco

Asegúrese de que los campos de Fecha de inicio y la Fecha de finalización sean visibles en la pestaña Líneas de la factura. En la mayoría de los casos, la Fecha de inicio debe ser el mismo mes que la Fecha de factura. Los asientos de ingresos diferidos se registran con la fecha de la factura y aparecen en el reporte tal como corresponden.

Para cada línea de la factura que se debe diferir, especifique las fechas de inicio y finalización del periodo para diferir.

Si el campo Generar asientos en los **Ajustes** está configurado como Validación en la factura, Odoo genera de forma automática los asientos diferidos al validar la factura. Haga clic en el botón inteligente Asiento diferido para verlos.

Un asiento, con fecha del mismo día que la fecha contable de la factura, mueve las cantidades facturadas de la cuenta de ingresos a la cuenta de diferidos. Los otros asientos son asientos diferidos que cada mes mueven las cantidades facturadas de la cuenta de diferidos a la cuenta de ingresos para reconocer el ingreso.

 Example

Puede diferir una factura de enero por $1,200 a lo largo de 12 meses, solo debe especificar la fecha de inicio en 01/01/2023 y la fecha de finalización en 31/12/2023. Al final de agosto, se habrán reconocido $800 como ingreso, mientras que los otros $400 se quedarán en la cuenta de diferidos.

## Reportes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/deferred_revenues.html#reporting "Enlazar permanentemente con este título")

El reporte de ingresos diferidos calcula un resumen de los asientos diferidos para cada cuenta. Para acceder a este reporte, vaya a Contabilidad ‣ Reportes ‣ Ingresos diferidos.

Para ver los apuntes de diario de cada cuenta, haga clic en el nombre de la cuenta y después en Apuntes de diario.

![Reporte de ingresos diferidos](https://www.odoo.com/documentation/17.0/es/_images/deferred_revenue_report.png)

 Nota

Solo se tomarán en cuenta las facturas cuya fecha de entrega sea antes del final del periodo del reporte.

## Genere asientos diferidos agrupados de forma manual[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/deferred_revenues.html#generate-grouped-deferral-entries-manually "Enlazar permanentemente con este título")

Si tiene muchos ingresos diferidos y quiere reducir el número de asientos de diario generados, puede generar asientos de diario diferidos de forma manual. Para hacerlo, configure el campo Generar asientos en los **Ajustes** como Manual y agrupados. Odoo entonces agrega las cantidades diferidas a un solo asiento.

Al final de cada mes, vaya a Contabilidad ‣ Reportes ‣ Ingresos diferidos y haga clic en el botón Generar asientos. Esto genera dos asientos diferidos:

- El primer asiento tiene la fecha del final de cada mes, que agrega todas las cantidades diferidas de ese mes para cada cuenta. Esto significa que una parte de los ingresos diferidos se reconoce al final de ese periodo.
    
- La anulación de este asiento creado, con fecha del siguiente día (es decir, el primer día del siguiente mes), para cancelar el asiento previo.
    

 Example

Hay dos facturas:

- Factura A: $1,200 a diferir de 01/01/2023 a 31/12/2023
    
- Factura B: $600 a diferir de 01/01/2023 a 31/12/2023
    

En enero

Al final de enero, después de hacer clic en Generar asientos, verá los siguientes asientos:

- Asiento 1 con fecha del 31 de enero:
    
    - Línea 1: cuenta de gastos -1,200 -600 = **-1,800** (lo cual cancela el total de ambas facturas)
        
    - Línea 2: cuenta de gastos 100 + 50 = **150** (el cual reconoce 1/12 de factura A y factura B)
        
    - Línea 3: cuenta diferida $1,800 - 150 =**1,650** (cantidad que todavía se tiene que diferir después)
        
- Asiento 2 con fecha del 1 de febrero, la cancelación del asiento previo:
    
    - Línea 1: cuenta de gastos **1,800**
        
    - Línea 2: cuenta diferidos **-150**
        
    - Línea 3: cuenta de gastos **-1,650**
        

En febrero

Al final de febrero, después de hacer clic en Generar asientos, verá los siguientes asientos:

- Asiento 1 con fecha del 28 de febrero:
    
    - Línea 1: cuenta de gastos -1,200 -600 = **-1,800** (lo cual cancela el total de ambas facturas)
        
    - Línea 2: cuenta de gastos 200 + 100 = **300** (el cual reconoce 1/12 de factura A y factura B)
        
    - Línea 3: cuenta diferida $1,800 - 300 =**1,500** (cantidad que todavía se tiene que diferir después)
        
- Asiento 2 con fecha del 1 de marzo, la cancelación del asiento previo.
    

De marzo a octubre

Se hace el mismo cálculo por cada mes hasta octubre.

En noviembre

Al final de noviembre, después de hacer clic en Generar asientos, verá los siguientes asientos:

- Asiento 1 con fecha del 30 de noviembre:
    
    - Línea 1: cuenta de gastos -1,200 -600 = **-1,800** (lo cual cancela el total de ambas facturas)
        
    - Línea 2: cuenta de gastos 1,100 + 550 = **1,650** (el cual reconoce 1/12 de factura A y factura B)
        
    - Línea 3: cuenta diferida $1,800 - 1,650 =**150** (cantidad que todavía se tiene que diferir después)
        
- Asiento 2 con fecha del 1 de diciembre, la cancelación del asiento previo.
    

En diciembre

No hay necesidad de generar asientos en diciembre. Si hacemos el cálculo en diciembre, la cantidad que se debe diferir es 0.

En total

Si sumamos todo, tendríamos:

- factura A y factura B
    
- dos asientos (una para los asientos diferidos y otro para la cancelación) para cada mes de enero a noviembre
    

Por lo tanto, al final de diciembre, las facturas A y B se reconocen como ingresos solo una vez a pesar de todos los asientos creados gracias al mecanismo de cancelación.