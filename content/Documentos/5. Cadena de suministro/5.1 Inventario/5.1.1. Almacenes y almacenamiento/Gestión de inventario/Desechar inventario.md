En algunas ocasiones, los productos en el almacén de una empresa pueden estar dañados o tener defectos que no se pueden reparar. En caso de que no sea posible reparar el producto o devolvérselo a un proveedor, puede desecharlo.

La aplicación _Inventario_ permite que los usuarios desechen parte de su inventario y designen bienes o materiales que ya no se pueden utilizar o vender para deshacerse de ellos (o reciclarlos).

Desechar inventario en una base de datos ayuda a mantener la precisión en los conteos, ya que elimina estos productos del inventario físico y los coloca en una ubicación virtual de desecho (_Ubicaciones virtuales/Desecho_).

 Nota

Las _ubicaciones virtuales_ en Odoo **no** son espacios físicos reales en un almacén, sino que son ubicaciones en una base de datos que proporcionan seguimiento de los artículos que no deben contarse en un inventario físico.

For more information about virtual locations, see the documentation about the different types of [location types](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management.html#inventory-warehouses-storage-location-type).

## Desechar de las existencias[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/scrap_inventory.html#scrap-from-stock "Enlazar permanentemente con este título")

Vaya a Inventario ‣ Operaciones ‣ Desechar y haga clic en Nuevo para crear una nueva orden de desecho para un producto en existencia. Esta acción abrirá un nuevo formulario para esta orden.

Haga clic en el menú desplegable del campo Producto y seleccione el producto a desechar del inventario. En el campo Cantidad cambie el valor a la cantidad correspondiente (este valor es `1.00` de forma predeterminada).

![Formulario completado de la nueva orden de desecho con los detalles del producto.](https://www.odoo.com/documentation/17.0/es/_images/scrap-inventory-new-scrap-order.png)

El valor predeterminado en la ubicación de origen es la ubicación donde se almacena el producto en ese momento y el valor predeterminado de la ubicación de deshecho es la designada para los mismos (Ubicaciones virtuales/Desechos). Es posible cambiar cualquiera de estas si selecciona una ubicación distinta desde sus menús desplegables.

Si el desecho está relacionado con una operación específica existente, especifíquela en el campo Documento origen.

En el campo Empresa aparece la que es propietaria del almacén de este producto. Si hay una regla de reabastecimiento configurada para el producto a desechar y se debe reabastecer, seleccione la casilla de Reabastecer cantidades.

Al terminar, haga clic en Validar para completar la nueva orden de desecho. Luego de validarla aparece el botón inteligente Movimientos de producto en la parte superior del formulario, haga clic en él para ver los detalles de la operación correspondiente.

![Botón inteligente Movimientos de producto en el formulario de una nueva orden de desecho.](https://www.odoo.com/documentation/17.0/es/_images/scrap-inventory-product-moves-button.png)

 Truco

Para visualizar el número completo de artículos desechados vaya a Inventario ‣ Configuración ‣ Ubicaciones. Haga clic en el botón x (eliminar) en el filtro Interno en la barra de búsqueda para mostrar las ubicaciones virtuales.

Seleccione la ubicación Ubicaciones virtuales/Desecho. En el formulario de la ubicación Desecho, haga clic en el botón inteligente Existencias actuales ubicado en la parte superior del formulario.

Aparece una lista con todos los productos desechados y la cantidad correspondiente.

![Lista de existencias actuales de todos los productos desechados en la ubicación virtual correspondiente.](https://www.odoo.com/documentation/17.0/es/_images/scrap-inventory-current-stock.png)

## Desechar desde una operación existente[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/scrap_inventory.html#scrap-from-an-existing-operation "Enlazar permanentemente con este título")

_También_ es posible crear órdenes de desecho a partir de operaciones existentes, como recepciones, órdenes de entrega y traslados internos, antes de ingresarlas o retirarlas del inventario para una operación.

Vaya a Inventario para desechar un producto durante una operación. Desde la información general de Inventario, haga clic en el botón # por procesar en la tarjeta correspondiente a la tarea de la operación (es decir, la tarjeta de recepciones).

![El botón "# por procesar" en la tarjeta de tareas de recepciones en la página Resumen de inventario.](https://www.odoo.com/documentation/17.0/es/_images/scrap-inventory-receipts-task-card.png)

Después seleccione una operación para procesar de la lista de órdenes existentes, esta acción abre el formulario de esa operación.

Haga clic en el icono  (engranaje), y seleccione Desechar en el menú desplegable. Esta acción abrirá la ventana emergente Desechar productos.

![La ventana emergente "Desechar productos" en el formulario de la operación.](https://www.odoo.com/documentation/17.0/es/_images/scrap-inventory-popup-window.png)

En esta ventana emergente, haga clic en el menú desplegable del campo Producto y seleccione los productos a desechar de la operación. Ajuste el valor en el campo Cantidad en caso de que sea necesario.

Si el producto seleccionado se rastrea con un número de lote o de serie aparecerá el campo correspondiente, especifique el número de rastreo allí.

Es posible cambiar la ubicación de origen y la ubicación de desecho si es necesario. Si hay una regla de reabastecimiento configurada para el producto a desechar y se debe reabastecer, seleccione la casilla de Reabastecer cantidades.

Al terminar, haga clic en Desechar productos. Aparecerá el botón inteligente Desechos en la parte superior del formulario de la operación, haga clic en él para ver los detalles de todas las órdenes creadas a partir de esta operación en específico.

![Botón inteligente "Desechos" que muestra todas las ordenes correspondientes de la operación.](https://www.odoo.com/documentation/17.0/es/_images/scrap-inventory-scraps-smart-button.png)