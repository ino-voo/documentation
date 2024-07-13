Trabajar con **números de serie** y **lotes** le permite rastrear los movimientos de sus productos. Cuando los productos se rastrean, el sistema identifica su ubicación según su último movimiento.

Para habilitar la trazabilidad, vaya a Punto de venta ‣ Productos ‣ Productos. Posteriormente, seleccione un producto y marque la casilla de Rastreo por número de serie único o la de Rastreo por lotes en la pestaña de Inventario.

![Habilitar los ajustes de trazabilidad](https://www.odoo.com/documentation/17.0/es/_images/product-form-traceability.png)

## Importación de números de serie y lotes[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/serial_numbers.html#serial-numbers-and-lots-importation "Enlazar permanentemente con este título")

Puede importar números de serie en la aplicación Punto de venta. Para hacerlo, seleccione una **orden de venta** o una **cotización** que contenga productos a los que se les lleva seguimiento. Posteriormente, acceda a cargar los **Números de lote o de serie** vinculados a la orden de venta.

![Ventana emergente para importación de números de serie](https://www.odoo.com/documentation/17.0/es/_images/importing-sn.png)

Los números de rastreo importados aparecen debajo de los productos rastreados. Puede modificarlos al hacer clic en botón de vista de lista junto a los productos.

![Ventana emergente para importación de números de serie](https://www.odoo.com/documentation/17.0/es/_images/pos-sn-imported.png)

 Ver también

- [Orden de venta](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/sales_order.html)
    

## Creación de números de serie y lotes[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/serial_numbers.html#serial-numbers-and-lots-creation "Enlazar permanentemente con este título")

Si un producto rastreado está disponible en su PdV, agregarlo al carrito abre una venta emergente en la que puede escribir o escanear el número de serie o de lote del producto. Para agregar más de uno del mismo producto rastreado, haga clic en **ingresar** para validar y empezar una nueva línea.

![Agregar nuevos números de serie y de lote](https://www.odoo.com/documentation/17.0/es/_images/create-change-sn.png)

 Nota

- Cambiar la cantidad de un producto rastreado mediante el teclado numérico cambia el color del botón de lista de vista a rojo. Hacer clic en él agrega los números de serie y de lote faltantes.
    
- Los números de lote y de serie son necesarios en los productos rastreados, pero no son obligatorios. Esto significa que el no atribuir alguno o ninguno **no** inhabilita completar la venta.
    

 Ver también

- [Usar números de serie para rastrear productos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/serial_numbers.html)
    
- [Números de lote](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html)