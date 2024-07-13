Al dirigir una empresa tal vez necesite aplicar distintos impuestos y registrar transacciones en varias cuentas según la ubicación y el tipo de negocio de sus clientes y proveedores.

La función **posiciones fiscales** le permite establecer reglas que seleccionan de forma automática los impuestos y cuentas correctas que se utilizarán en cada transacción.

 Ver también

- [Posiciones fiscales (mapeo de impuestos y cuentas)](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/fiscal_positions.html)
    
- [Impuestos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes.html)
    

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/fiscal_position.html#configuration "Enlazar permanentemente con este título")

Para habilitar la función, vaya a Punto de venta ‣ Configuración ‣ Ajustes, baje a la sección Contabilidad y habilite la función impuestos flexibles.

Después, en el campo predeterminado establezca una posición fiscal predeterminada que se debería aplicar a todas las ventas en el PdV seleccionado. También puede agregar más posiciones fiscales para seleccionar en el campo permitido.

![../../../../_images/flexible-taxes-setting.png](https://www.odoo.com/documentation/17.0/es/_images/flexible-taxes-setting.png)

Según el [paquete de localización fiscal](https://www.odoo.com/documentation/17.0/es/applications/finance/fiscal_localizations.html) que activó, hay varias posiciones fiscales preconfiguradas que se pueden establecer y utilizar en PdV. Sin embargo, también puede [crear nuevas posiciones fiscales](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/fiscal_positions.html#fiscal-positions-mapping).

 Nota

Si no establece una posición fiscal, el impuesto permanece como se definió en el campo **impuestos de cliente** en el formulario del producto.

## Usar posiciones fiscales[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/fiscal_position.html#use-fiscal-positions "Enlazar permanentemente con este título")

Abra una [sesión de PdV](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#pos-session-start) para utilizar una de las posiciones fiscales permitidas. Luego, haga clic en el botón impuesto a lado del icono con forma de **libro** y seleccione una posición fiscal de la lista. Hacer esto aplica las reglas definidas de forma automática a todos los productos sometidos a las regulaciones de la posición fiscal elegida.

![../../../../_images/set-tax.png](https://www.odoo.com/documentation/17.0/es/_images/set-tax.png)

 Nota

Si se establece una posición fiscal predeterminada, el botón «impuesto» muestra el nombre de la posición fiscal.

 Ver también

[Posiciones fiscales (mapeo de impuestos y cuentas)](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/fiscal_positions.html)