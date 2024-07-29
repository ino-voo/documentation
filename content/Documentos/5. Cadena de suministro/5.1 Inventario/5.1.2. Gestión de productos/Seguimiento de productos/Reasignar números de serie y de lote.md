Cambiar los ajustes de seguimiento de un producto para usar lotes o números de serie _después_ de almacenar productos en Odoo sin ellos podría ocasionar registros inconsistentes. Siga las instrucciones en esta documentación para aprender a usar un ajuste de inventario para asignar los números correspondientes a los productos que no tenían asignado uno.

![Mensaje de advertencia: los productos en existencia no tienen número de lote o serie.](https://www.odoo.com/documentation/17.0/es/_images/warning.png)

 Nota

Esta documentación describe el proceso de usar dos ajustes de inventario: uno para eliminar registros incorrectos _sin_ números de lote y otro para guardar la cantidad indicada _con_ los números de lote.

 Ver también

- [Configurar y usar números de lote](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html)
    
- [Configurar números de lote](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html)
    
- [Usar números de serie](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/serial_numbers.html)
    

## Cambiar la cantidad disponible a cero[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/reassign.html#change-on-hand-quantity-to-zero "Enlazar permanentemente con este título")

Para cambiar los ajustes de un producto y rastrearlo por números de serie o lote, vaya a Inventario ‣ Productos ‣ Productos y seleccione uno.

Después, haga clic en el botón inteligente Disponible para abrir la página Actualizar cantidad. Cambie el valor a cero en la columna Cantidad disponible.

 Nota

Si almacena el producto en varias ubicaciones, asegúrese de que la cantidad **total** disponible en **todas** ubicaciones sea cero.

![Visualización del modelo de Ajustes de inventario, el campo "Cantidad disponible". aparece dentro de un recuadro rojo.](https://www.odoo.com/documentation/17.0/es/_images/remove-quant.png)

## Cambiar los ajustes de trazabilidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/reassign.html#change-traceability-setting "Enlazar permanentemente con este título")

Regrese al formulario del producto (Inventario ‣ Productos ‣ Productos) y vaya a la pestaña Inventario. En la sección Trazabilidad, cambie la opción :guilabel:`Seguimiento a Por lotes o a Por número de serie único.

 Ver también

[Fechas de vencimiento](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/expiration_dates.html)

![Habilitar números de lote y de serie.](https://www.odoo.com/documentation/17.0/es/_images/tracking.png)

## Restablecer la cantidad disponible[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/reassign.html#restore-on-hand-quantity "Enlazar permanentemente con este título")

Después de cambiar la cantidad disponible a cero y los ajustes de seguimiento a lotes o números de serie, haga clic en el botón inteligente Disponible del formulario de producto correspondiente para restaurar la cantidad adecuada.

Como había cambiado la cantidad disponible a cero con anterioridad, en la página Actualizar cantidad aparece la advertencia Sin existencias disponibles. Desde aquí, haga clic en el botón Nuevo ubicado en la esquina superior izquierda, esta acción abre una nueva línea modificable en la misma página. Escriba el número de lote deseado en el campo Número de serie o lote y ajuste la cantidad disponible a su valor original.

 Ver también

[Ajustes de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/count_products.html)

![Complete los campos "Número de serie/lote" y "Cantidad disponible".](https://www.odoo.com/documentation/17.0/es/_images/update-quantity.png)

 Truco

Haga clic en el  (lápiz) en la columna Cantidad disponible después de asignar un nuevo lote o número de serie para encontrar la cantidad original y ajustar la cantidad disponible según corresponda. Después haga clic en el botón  Historial ubicado en el extremo derecho.

![Visualización del botón "Historial" en la página Ajuste de inventario.](https://www.odoo.com/documentation/17.0/es/_images/adjustment.png)

El ajuste de inventario que modificó la cantidad disponible a cero aparece en el campo Cantidad.

> ![Visualización del historial de entradas.](https://www.odoo.com/documentation/17.0/es/_images/history.png)