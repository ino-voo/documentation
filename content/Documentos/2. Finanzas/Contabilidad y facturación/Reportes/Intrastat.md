Intrastat es el sistema de recopilación de datos y elaboración de estadísticas sobre los bienes comercializados entre los Estados miembros de la UE. Recopila datos sobre:

- Transacciones comerciales de bienes para su uso, consumo, inversión o reventa con traspaso de propiedad;
    
- Movimientos de bienes sin traspaso de propiedad (por ejemplo, traslados de existencias o movimientos de bienes antes o después de la producción o tratamiento externos, y después del mantenimiento o reparación);
    
- Devolución de bienes
    

 Nota

Aunque se sigue utilizando el sistema Intrastat, el término Intrastat no se emplea en la [última legislación](http://data.europa.eu/eli/reg/2019/2152/2022-01-01), en su lugar se usa el término _estadísticas del comercio de bienes dentro de la Unión_.

 Ver también

Explicación de las estadísticas de Eurostat - Glosario: Intrastat <[https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Glossary:Intrastat](https://ec.europa.eu/eurostat/statistics-explained/index.php?title=Glossary:Intrastat)>`_

## Configuración general[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#general-configuration "Enlazar permanentemente con este título")

Active el reporte Intrastat en Contabilidad ‣ Configuración ‣ Ajustes. Seleccione Intrastat en la sección Facturas de clientes y, por último, Guardar.

### Códigos predeterminados de transacción: facturación y reembolsos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#default-transaction-codes-invoice-and-refund "Enlazar permanentemente con este título")

Puede establecer un [código de transacción](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-transaction-code) predeterminado para todas las transacciones de factura y reembolso. Para hacer esto, vaya a Contabilidad ‣ Configuración ‣ Ajustes, seleccione un código de transacción de factura predeterminado o un código de transacción de reembolso predeterminado y luego haga clic en guardar. El código se establecerá de forma automática en todas las líneas de factura respectivas.

### Código regional[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#region-code "Enlazar permanentemente con este título")

El código regional **solo se usa para las empresas belgas**. Para usarlo, vaya a Contabilidad ‣ Configuración ‣ Ajustes, seleccione la región intrastat de la empresa en la que se encuentra la empresa y haga clic en guardar.

 Truco

Si tiene almacenes en más de una región, puede definir el código de región en cada almacén. Para ello, vaya a Inventario ‣ Configuración ‣ Almacenes, seleccione un almacén, defina su región intrastat y haga clic en guardar.

![Se añade la región intrastat a un almacén](https://www.odoo.com/documentation/17.0/es/_images/warehouse-region.png)

## Configuración de productos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#product-configuration "Enlazar permanentemente con este título")

Para que los productos se añadan correctamente a un reporte intrastat deben estar bien configurados.

### Código de mercancía[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#commodity-code "Enlazar permanentemente con este título")

Los códigos de mercancía son números de referencia reconocidos en todo el mundo que se usan para clasificar los bienes según sus **características**. El código intrastat usa la [nomenclatura combinada](https://taxation-customs.ec.europa.eu/customs-4/calculation-customs-duties/customs-tariff/combined-nomenclature_en).

Si desea añadir un código de mercancía, vaya a Contabilidad ‣ Clientes ‣ Productos y seleccione un producto, luego, en la pestaña contabilidad, establezca el código de mercancía del producto.

 Ver también

[Códigos intrastat de mercancía - Banco Nacional de Bélgica](https://www.nbb.be/en/statistics/foreign-trade/nomenclature-and-codes)

### Cantidad: peso y unidades suplementarias[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#quantity-weight-and-supplementary-unit "Enlazar permanentemente con este título")

De acuerdo con las características de la mercancía, a veces es necesario indicar el peso en kilos (sin contar el paquete) o las unidades suplementarias del producto, esto se debe indicar en metros cuadrados (`m2`), número de unidades (`p/st`), litros (`l`), o gramos (`g`).

Si desea añadir el peso de un producto o una unidad suplementaria, vaya a Contabilidad ‣ Clientes ‣ Productos y seleccione un producto. Introduzca el peso o las unidades suplementarias del producto en la pestaña contabilidad.

### País de origen[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#country-of-origin "Enlazar permanentemente con este título")

Si desea establecer el país de origen de un producto, vaya a Contabilidad ‣ Clientes ‣ Productos y seleccione un producto. Establezca el país de origen en la pestaña contabilidad.

## Configuración de las facturas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#invoices-and-bills-configuration "Enlazar permanentemente con este título")

Una vez que haya configurado correctamente los productos, deberá definir varios valores en las facturas y recibos que cree.

### Código de transacción[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#transaction-code "Enlazar permanentemente con este título")

Los códigos de transacción sirven para identificar el tipo de transacción. Pude establecer [códigos de transacción predeterminados](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-default-transaction-codes) para las transacciones de facturas y reembolsos.

Si desea establecer un código de transacción en una línea de factura debe crear una factura, hacer clic en el botón de selección de columnas, seleccionar intrastat, y usar esta nueva columna para seleccionar un código de transacción.

![Se añade la columna intrastat en una factura](https://www.odoo.com/documentation/17.0/es/_images/intrastat-column.png)

 Ver también

[Intrastat: características de las transacciones desde enero 2022 - Banco Nacional de Bélgica](https://www.nbb.be/doc/dd/onegate/data/new_natures_of_transaction_2022_en.pdf)

### País del contacto[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#partner-country "Enlazar permanentemente con este título")

El país del contacto representa el país del proveedor y del cliente para las facturas. Se completa de forma automática según el país establecido en el campo País del contacto.

Si desea editar el país del contacto de forma manual debe crear una factura, hacer clic en la pestaña Más información y seleccionar el país intrastat.

### Código de transporte[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#transport-code "Enlazar permanentemente con este título")

El código de transporte identifica el presunto **modo de transporte** a usar para transportar los bienes (llegada o expedición).

Si desea añadir el código de transporte debe crear una factura, hacer clic en la pestaña Más información y seleccionar el modo de transporte intrastat.

### Valor de los bienes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#value-of-the-goods "Enlazar permanentemente con este título")

El valor de un bien es el subtotal (precio multiplicado por la cantidad) de una línea de factura.

## Configuración de contacto[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#partner-configuration "Enlazar permanentemente con este título")

Intrastat utiliza dos campos del formulario de contacto: NIF y país. Puede establecer [el país](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-partner-country) en la factura de forma manual.

## Generar el reporte intrastat[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#generate-the-intrastat-report "Enlazar permanentemente con este título")

Para generar el reporte, vaya a Contabilidad ‣ Reportes ‣ Reportes de auditoría: reporte intrastat. Se calcula de forma automática según la [configuración predeterminada](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-general-configuration) y la información que se encuentra en los [productos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-product-configuration), [facturas](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-invoice-bill-configuration), y [contactos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-partner).

Exporte el reporte en formato PDF, XLSX o XML y envíelo a su administración legal.

Cada línea del reporte corresponde a una sola línea de la factura y contiene la siguiente información:

- Número de referencia de la factura;
    
- Sistema, consiste en un código generado automáticamente para indicar si el documento es una factura (expedición) o un recibo (llegada);
    
- [País](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-partner-country); el país del proveedor para las llegadas y el país del cliente para los envíos;
    
- [Código de transacción](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-transaction-code);
    
- Si su empresa está ubicada en Bélgica, [código regional](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-region-code);
    
- [Código de mercancía](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-commodity-code);
    
- [País de origen](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-origin-country);
    
- [NIF del contacto](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-partner);
    
- [Código de transporte](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-transport-code);
    
- [Código incoterm](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/incoterms.html);
    
- [Peso](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-quantity);
    
- [Unidades suplementarias](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-quantity);
    
- [Valor](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html#intrastat-value), expresado siempre en euros, aunque en la factura original se haya utilizado otra divisa.