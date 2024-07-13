Hay varios tipos de **impuestos**, y su uso varía mucho, esto depende principalmente de la ubicación de su empresa. Para asegurarse de que se registran correctamente, el sistema de impuestos de Odoo es compatible con todo tipo de usos y cálculos.

## Impuestos predeterminados[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#default-taxes "Enlazar permanentemente con este título")

Los **impuestos predeterminados** definen qué impuestos se seleccionan de forma automática al crear un nuevo producto. También se utilizan para completar el campo Impuestos al agregar una nueva línea en una factura en el modo de [empresas de contabilidad](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting.html#fiduciaries).

![Odoo completa el campo "impuestos" de forma automática según los impuestos predeterminados](https://www.odoo.com/documentation/17.0/es/_images/default-configuration.png)

Para cambiar los **impuestos predeterminados**, vaya a menuselection:`Contabilidad --> Configuración --> Ajustes --> Impuestos --> Impuestos predeterminados`, seleccione los impuestos adecuados para sus impuestos de venta y compra y haga clic en Guardar.

![Defina qué impuestos se utilizan de forma predeterminada en Odoo](https://www.odoo.com/documentation/17.0/es/_images/default-taxes.png)

 Nota

Los **impuestos predeterminados** se configurar de manera automática según el país que se haya seleccionado al momento de crear la base de datos, o cuando configure el [paquete de localización fiscal](https://www.odoo.com/documentation/17.0/es/applications/finance/fiscal_localizations.html#fiscal-localizations-packages) de su empresa.

## Activar los impuestos de venta desde la vista de lista[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#activate-sales-taxes-from-the-list-view "Enlazar permanentemente con este título")

La mayoría de sus impuestos de venta ya están preconfigurados en su base de datos gracias a su [paquete de localización fiscal](https://www.odoo.com/documentation/17.0/es/applications/finance/fiscal_localizations.html#fiscal-localizations-packages); sin embargo, solo algunos de los impuestos se activan de forma automática. Para activar los impuestos relevantes para su empresa, vaya a Contabilidad ‣ Configuración ‣ Impuestos y active el botón de opción en la columna Activo.

![Impuestos preconfigurados activos en la aplicación Contabilidad de Odoo](https://www.odoo.com/documentation/17.0/es/_images/list1.png)

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#configuration "Enlazar permanentemente con este título")

Para editar o crear un **impuesto** vaya a Contabilidad ‣ Configuración ‣ Impuestos y abra un impuesto o haga clic en Nuevo.

![Modo de edición de un impuesto en la aplicación Contabilidad de Odoo](https://www.odoo.com/documentation/17.0/es/_images/edit.png)

### Opciones principales[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#basic-options "Enlazar permanentemente con este título")

#### Nombre del impuesto[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#tax-name "Enlazar permanentemente con este título")

El **nombre del impuesto** es para que los usuarios del backend lo puedan leer en el campo impuestos de las [órdenes de venta](https://www.odoo.com/documentation/17.0/es/applications/sales/sales.html), [facturas](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices.html), formularios de los productos, etc.

#### Cálculo de impuestos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#tax-computation "Enlazar permanentemente con este título")

- **Grupos de impuestos**
    
    El impuesto es una combinación de varios subimpuestos. Puede agregar tantos impuestos como quiera y en el orden en el que quiera.
    
     Importante
    
    Asegúrese de que la secuencia de impuestos es correcta, ya su orden puede afectar al cálculo de los importes de los impuestos, en especial si uno de los impuestos [afecta a la base de los siguientes](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#taxes-base-subsequent).
    
- **Fijo**
    
    El impuesto será de una cantidad fija en la divisa. La cantidad será la misma sin importar el precio de venta.
    

 Example

Un producto tiene un precio de venta de $1000, y aplicamos un impuesto fijo de $10. El resultado es:

|Precio de venta del producto|Precio sin impuestos|Impuesto|Total|
|---|---|---|---|
|1,000|1,000|10|1,010.00|

- **Porcentaje del precio**
    
    El _precio de venta_ es la base del impuesto: el importe del impuesto se calcula multiplicando el precio de venta por el porcentaje del impuesto.
    

 Example

Un producto tiene un precio de venta de $1000, y aplicamos un impuesto del _10% del precio_. El resultado es:

|Precio de venta del producto|Precio sin impuestos|Impuesto|Total|
|---|---|---|---|
|1,000|1,000|100|1,100.00|

- **Porcentaje del precio con impuestos incluidos**
    
    El _total_ es el saldo con el impuesto: el importe del impuesto es un porcentaje del total.
    

 Example

Un producto tiene un precio de venta de $1000 y aplicamos un impuesto de _10% de impuesto incluido en el precio_. Entonces, tenemos:

|Precio de venta del producto|Precio sin impuestos|Impuesto|Total|
|---|---|---|---|
|1,000|1,000|111.11|1,111.11|

- **Código Python**
    
    Un impuesto definido como **código Python** consta de dos fragmentos de código Python que están excluidos en un entorno local y contienen datos como el precio unitario, el producto o el contacto. El código python define la cantidad del impuesto y el Código aplicable define si el impuesto se debe de aplicar. La fórmula se encuentra al final de la pestaña Definición.
    

 Example

Código Python: `resultado = price_unit * 0.10` Código aplicable: `resultado = true`

#### Activo[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#active "Enlazar permanentemente con este título")

Solo los impuestos **activos** se pueden agregar a nuevos documentos.

 Importante

No es posible eliminar los impuestos que ya se han utilizado. En su lugar, puede desactivarlos para evitar su uso en el futuro.

 Nota

Este campo se puede modificar desde la [vista de lista](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#taxes-list-activation).

#### Tipo de impuesto[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#tax-type "Enlazar permanentemente con este título")

El tipo de impuesto determina cómo se aplica el impuesto, lo cual también limita su visualización.

- **Ventas**: facturas de clientes, impuestos de productos para clientes, etc.
    
- **Compra**: facturas de proveedor, impuestos de productos de los proveedores, etc.
    
- **Ninguno**
    

 Truco

Puede utilizar la opción ninguno para los impuestos que desee incluir en un [grupo de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#taxes-computation), pero que no quiera incluir en la lista junto con los otros impuestos de venta o compra.

#### Ámbito del impuesto[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#tax-scope "Enlazar permanentemente con este título")

El ámbito del impuesto restringe el uso de impuestos a un tipo de producto, ya sea un **bien** o un **servicio**.

### Pestaña de definición[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#definition-tab "Enlazar permanentemente con este título")

Asigne el importe de la base del impuesto o los porcentajes del impuesto calculado a varias cuentas y tablas de impuestos.

![Asignación de importes de impuestos en las cuentas y tablas de impuestos correctas](https://www.odoo.com/documentation/17.0/es/_images/definition.png)

- **Basado en**:
    
    - Base: el precio en la línea de impuestos
        
    - % de impuesto: un porcentaje del impuesto calculado.
        
- **Cuenta**: si se define, se registrará un apunte contable adicional.
    
- **Tablas de impuestos**: se usan para generar [reportes de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/tax_returns.html) de forma automática, de acuerdo a las normativas de su país.
    

### Pestaña de opciones avanzadas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#advanced-options-tab "Enlazar permanentemente con este título")

#### Etiqueta en las facturas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#label-on-invoices "Enlazar permanentemente con este título")

La etiqueta de impuesto se muestra en cada línea de impuesto en la columna Impuestos. Los usuarios del frontend pueden ver esto en el portal del cliente, etc.

![La etiqueta en las facturas se muestra en cada línea de la factura.](https://www.odoo.com/documentation/17.0/es/_images/invoice-label.png)

#### Grupo de impuestos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#tax-group "Enlazar permanentemente con este título")

Seleccione a qué **grupo de impuestos** pertenece el impuesto. El nombre del grupo de impuestos se muestra arriba de la línea **total** en los impuestos exportados y en los portales del cliente.

Los grupos de impuesto incluyen diferentes iteraciones del mismo impuesto. Esto puede ser útil cuando tenga que registrar el mismo impuesto de otra manera según las [posiciones fiscales](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/fiscal_positions.html).

 Example

![El nombre del grupo de impuestos es distinto al de la etiqueta en las facturas](https://www.odoo.com/documentation/17.0/es/_images/invoice-tax-group.png)

En el ejemplo anterior, el impuesto 0% EU S para clientes de la comunidad en Europa registra la cantidad en cuentas específicas y tablas de impuestos; sin embargo, se mantendrá a 0% como impuesto para el cliente. Es por esto que la etiqueta indica 0% EU S y el nombre del grupo de impuestos arriba de la línea de Total indica VAT 0%.

 Importante

Los impuestos tienen tres etiquetas diferentes, cada una con un uso específico. Consulte la siguiente tabla para ver en qué lugar aparecen.

|[Nombre del impuesto](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#taxes-name)|[Etiqueta en la factura](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#taxes-label-invoices)|[Grupo de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#taxes-tax-group)|
|---|---|---|
|Salir (sin cerrar sesión)|La columna impuestos en los impuestos exportados|Arriba de la línea de Total en los impuestos exportados|

#### Incluido en costo analítico[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#include-in-analytic-cost "Enlazar permanentemente con este título")

Si activa esta opción, el importe del impuesto se asigna a la misma **cuenta analítica** que la línea de factura.

#### Incluido en el precio[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#included-in-price "Enlazar permanentemente con este título")

Si activa esta opción, el total (con impuestos incluidos) es igual al **precio de venta**.

`Total = Precio de venta = Precio calculado sin impuestos incluidos + Impuesto`

 Example

Un producto tiene un precio de venta de $1,000 y aplicamos el impuesto de _10% del precio_, que se _incluye en el precio_. Entonces tenemos:

|Precio de venta del producto|Precio sin impuestos|Impuesto|Total|
|---|---|---|---|
|1,000|900.10|90.9|1,000.00|

 Nota

Si necesita definir los precios con precisión, tanto con o sin impuestos, consulte la siguiente documentación: [Precios B2B (impuestos no incluidos) y B2C (impuestos incluidos)](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/B2B_B2C.html).

 Nota

La columna Impuestos excluidos solo aparece en facturas de forma predeterminada. Para mostrar la columna Impuestos incluidos, haga clic en el botón **de opción para desplegarla** y seleccione Impuestos incluidos.

![../../../_images/toggle-button.png](https://www.odoo.com/documentation/17.0/es/_images/toggle-button.png)

#### Afecta la base de los impuestos subsecuentes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#affect-base-of-subsequent-taxes "Enlazar permanentemente con este título")

Con esta opción, el total de impuestos incluidos se convierte en la base del impuesto de los demás impuestos aplicados al mismo producto.

Puede configurar un nuevo [grupo de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#taxes-computation) que incluya este impuesto o agregarlo directo a la línea del producto.

![El impuesto se considera como base del IVA del 21%](https://www.odoo.com/documentation/17.0/es/_images/subsequent-line.png)

 Advertencia

El orden en el que se añaden los impuestos en una línea de producto no tiene ningún efecto sobre el cálculo de los importes. Si añade los impuestos directamente en una línea de producto, solo la secuencia de impuestos determina el orden en que se aplican.

Para reorganizar la secuencia, vaya a Contabilidad ‣ Configuración ‣ Impuestos, y arrastre y suelte las líneas junto a los nombres de los impuestos.

![La secuencia de los impuestos en Odoo determina qué impuestos se aplican primero](https://www.odoo.com/documentation/17.0/es/_images/list-sequence.png)

## Impuestos adicionales[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#extra-taxes "Enlazar permanentemente con este título")

Los «impuestos adicionales» es un término muy amplia que embarca los impuestos más allá de los básicos impuestos por el gobierno. Estos impuestos adicionales pueden ser impuestos de **lujo**, **ambientales**, de **importación**, **exportación**, etc.

 Nota

El método para calcular estos impuestos depende del país. Le recomendamos consultar las regulaciones de su país para entender cómo calcular estos impuestos dentro de su empresa.

Para calcular un impuesto adicional en Odoo [cree un impuesto](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#taxes-configuration), ingrese el nombre del impuesto, seleccione un [cálculo de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html#taxes-configuration), configure una Cantidad y en la pestaña opciones avanzadas seleccione Afecta la base de los impuestos subsecuentes `. Después, arrastre y suelte los impuestos en el :ref:`orden en el que se tienen que calcular <taxes/base-subsequent>.

 Example

- En Bélgica, la fórmula para calcular un impuesto ambiental es: `(precio del producto + impuesto ambiental) x impuesto de venta`. Por lo tanto, nuestro impuesto ambiental debe venir _antes_ que el impuesto de la venta en la secuencia de cálculo.
    
- En nuestro caso, creamos un impuesto ambiental (Ecotax) del 5% y lo pusimos _antes_ que el impuesto belga base del 21%.
    

![Secuencia de impuesto ambiental en Bélgica.](https://www.odoo.com/documentation/17.0/es/_images/ecotax.png)

 Ver también

- [Posiciones fiscales (mapeo de impuestos y cuentas)](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/fiscal_positions.html)
    
- [Precios B2B (impuestos no incluidos) y B2C (impuestos incluidos)](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/B2B_B2C.html)
    
- [Integración con TaxCloud](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/taxcloud.html)
    
- [Declaración de impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/tax_returns.html)