Al completar órdenes de ventas o comprar componentes para órdenes de fabricación, a veces es necesario darle prioridad a una orden de compra o una orden de fabricación. En situaciones donde no hay suficientes existencias a la mano para cumplir con todas las órdenes de venta o de fabricación, es importante asegurarse que los productos y componentes están reservados para las órdenes que son prioritarias.

En _Fabricación_ de Odoo, los reportes de asignación se usan en [|órdenes de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id1) para asignar productos a [|órdenes de ventas|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id3), o componentes a [|órdenes de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id5) específicas. Así nos aseguramos de que los productos o componentes estarán disponibles para esas órdenes y no los usuramos por error.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#configuration "Enlazar permanentemente con este título")

Para usar reportes de asignación, la función _Reporte de asignación para órdenes de fabricación_ **debe** estar activa. Para activarla, vaya a la aplicación Fabriación ‣ Configuración ‣ Ajustes, marque la casilla de verificación a un lado de Reporte de asignación para órdenes de fabricación y haga clic en guardar.

también es necesario configurar los productos que se venden para poderlos incluir en las órdenes de venta. Vaya a Inventario ‣ Productos ‣ Productos y seleccione uno, busque el campo Nombre del producto en el formulario del producto y asegúrese de que la casilla Se puede vender esté seleccionada.

## Asignar productos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#allocate-products "Enlazar permanentemente con este título")

Para asignar productos o componentes de una [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id7) a una [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id9), o a una [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id11) diferente, primero vaya a la aplicación Fabricación‣ Operaciones ‣ Órdenes de fabricación. Haga clic en Nuevo para crear una [|orden de fabriación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id13) nueva.

En el formulario de [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id15), seleccione un producto en el campo Producto y especifique la cantidad del producto que se debe producir en el campo Cantidad. Finalmente haga clic en Confirmar para confirmar la [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id17).

El resto del flujo de asignación depende de la cantidad a la mano actual del producto que se está fabricando y si hay [|órdenes de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id19) o [|de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id21) que requieran este producto, pero que todavía no tengan unidades asignadas.

Si **hay** órdenes de venta y de fabricación que necesitan el producto **y** hay pocas unidades del producto disponibles para cumplir con esas órdenes, entonces el botón inteligente  Asignación aparece en la parte superior de la página tan pronto como se confirme la [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id23).

Si **hay** órdenes de venta y de fabricación que necesitan el producto **y** hay suficientes unidades del producto disponibles para cumplir con esas órdenes, entonces el botón inteligente  Asignación solo aparece en la parte superior de la página después de marcar la orden de fabricación como completada al hacer clic en Producir todo.

![El botón inteligente de asignación en la parte superior de una orden de fabricación.](https://www.odoo.com/documentation/17.0/es/_images/allocation-button.png)

 Nota

Si **no hay** [|órdenes de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id25) y [|de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id27) existentes que requieran el producto, el botón inteligente  Asignación no aparecerá, aunque la [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id29) se marque como terminada.

Haga clic en el botón inteligente  Asignación para abrir el Reporte de recepción de planeación de recursos de fabricación para la [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id31). Este reporte enlista órdenes de entrega o de [|fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id33) en curso, dependiendo del tipo de producto que se produjo en la [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id35) original.

### Asignar a la orden de entrega[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#allocate-to-delivery-order "Enlazar permanentemente con este título")

Si la [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id37) contiene un producto terminado, el reporte enlista todas las ordenes de envío activas para las que la cantidad del producto no se ha reservado.

 Example

Se crea una orden de fabricación para producir tres unidades de una _mecedora_. Al hacer clic en el botón inteligente Asignación en la orden de fabricación se abre un reporte de asignación que incluye las órdenes de entrega abiertas que necesitan una o más mecedoras.

Haga clic en el botón Asignar todos a la derecha de una orden específica para asignar productos para cada cantidad requerida para cumplir con esa orden.

 Example

Si una orden requiere una cantidad de cuatro unidades del producto, y una cantidad de una unidad del producto, si hace clic en Asignar todos asignará cinco unidades del producto para cumplir con ambas cantidades.

También si hace clic en Asignar a un lado de una cantidad específica para solo asignar productos a esa cantidad, y no a ningún otro producto en esa orden.

 Example

Si una orden requiere una cantidad de cuatro unidades de un producto, y una cantidad de una unidad del producto, si hace clic en Asignar a un lado de la cantidad de una unidad, se asignará un producto a esa cantidad, pero la cantidad de cuatro unidades se quedará sin producto asignado.

![El Reporte de recepción de planeación de recursos de fabricación para una orden de fabricación que contiene productos terminados.](https://www.odoo.com/documentation/17.0/es/_images/product-reception-report.png)

### Asignar a orden de fabricación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#allocate-to-mo "Enlazar permanentemente con este título")

Si la [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id39) contiene un componente, el reporte enlista cualquier [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id41) abierta para el que las cantidades del componente no se han reservado.

 Example

Se crea una orden de fabricación para producir tres unidades de _madera_ que se utiliza como componente para el producto _Mecedora_. Al hacer clic en el botón inteligente Asignación en la orden de fabricación se abre un reporte de asignación que incluye las órdenes de fabricación abiertas de mecedoras que necesitan una o más piezas de madera.

Haga clic en el botón Asignar todos o Asignar a la derecha de una [|orden de fabricación específica|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id43) para asignarle componentes.

![El Reporte de recepción de planeación de recursos de fabricación para una orden de fabricación que contiene componentes.](https://www.odoo.com/documentation/17.0/es/_images/component-reception-report.png)

### Eliminar asignación de productos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#unassign-products "Enlazar permanentemente con este título")

Después de asignar productos a una cantidad dentro de la orden de entrega, o componentes a una [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#id45), el botón Asignar se convertirá en Desasignar, en el que puede hacer clic si quiere cancelar la reserva de los productos asignados de esa cantidad y así estarán disponibles para otras cantidades.

### Imprimir etiquetas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/allocation.html#print-labels "Enlazar permanentemente con este título")

Después de hacer clic en Asignar todo o Asignar, el botón Imprimir etiquetas o Imprimir etiqueta a la derecha de cualquier botón se volverá seleccionable. Si selecciona cualquiera de los botones se descargará un documento PDF por cada producto asignado. Estas etiquetas se usar para designar cada producto como reservado para esa orden en específico.

![Las etiquetas de asignación que se generaron al hacer clic en imprimir etiquetas o imprimir etiqueta.](https://www.odoo.com/documentation/17.0/es/_images/assigned-labels.png)