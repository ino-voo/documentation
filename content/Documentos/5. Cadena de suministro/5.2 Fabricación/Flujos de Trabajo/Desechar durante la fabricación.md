Es posible que durante el proceso de fabricación sea necesario desechar componentes o productos ya terminados si estos están dañados o no son usables por cualquier otra razón.

De manera predeterminada, al desechar un componente o un producto terminado, se elimina del inventario físico y se coloca en una ubicación virtual llamada _Ubicaciones virtuales/Desechos_. Una ubicación virtual **no** es un espacio físico, sino un lugar asignado en Odoo que se usa para rastrear elementos que ya no existen en el inventario físico.

 Ver también

For more information, see the documentation about the different types of [locations](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management.html).

Los componentes se pueden desechar desde la aplicación _Fabricación_ o el módulo _Taller_ antes de que la orden de fabricación relacionada se cierre. Los productos terminados solo se pueden desechar desde la aplicación _Fabricación_ y únicamente después de cerrar la orden de fabricación asociada.

 Truco

Puede ver las órdenes de desecho en Inventario ‣ Operaciones ‣ Desechar. Cada orden de desecho muestra la fecha y la hora en la que se creó la orden, junto con el producto y la cantidad desechada.

Para ver la cantidad total de cada elemento desechado vaya a Inventario ‣ Configuración ‣ Ubicaciones y luego elimine el filtro de Interno de la barra de Buscar… para mostrar todas las ubicaciones virtuales. Desde la lista, seleccione la ubicación llamada Ubicaciones virtuales/Desechos.

## Ventana emergente para desechar[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/scrap_manufacturing.html#scrap-pop-up-window "Enlazar permanentemente con este título")

La función de la ventana emergente Desechar es desechar componentes y productos terminados. Puede acceder a esta ventana desde una orden de fabricación en el backend o desde el módulo _Taller_.

### Desechar un componente desde Fabricación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/scrap_manufacturing.html#scrap-component-from-manufacturing "Enlazar permanentemente con este título")

Para desechar un componente de una orden de fabricación, primero vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y seleccione una. Haga clic en el botón Desechar ubicado en la parte superior de la orden de fabricación para abrir la ventana emergente Desechar.

### Desechar un producto terminado desde Fabricación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/scrap_manufacturing.html#scrap-finished-product-from-manufacturing "Enlazar permanentemente con este título")

Para desechar un producto terminado desde una orden de fabricación, primero vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y seleccione una que esté abierta, después haga clic en el botón Producir todo para cerrarla.

Para seleccionar una orden de fabricación que ya está cerrada, vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación, elimine el filtro Por hacer de la barra de búsqueda y busque la orden de fabricación deseada.

Una vez que esté cerrada, haga clic en el botón guilabel:`Desechar` ubicado en la parte superior de la orden de fabricación para abrir la ventana emergente guilabel:`Desechar`.

### Desechar un componente desde Taller[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/scrap_manufacturing.html#scrap-component-from-shop-floor "Enlazar permanentemente con este título")

Para desechar un componente desde el módulo _Taller_, primero vaya a Taller. Después, haga clic en en el botón ⋮ (tres puntos verticales) de alguna tarjeta de orden de trabajo o seleccione un centro de trabajo ubicado en la parte superior de la página y haga clic en el botón ⋮ (tres puntos verticales) de la tarjeta de una orden de trabajo.

Ambos métodos abrirán la ventana emergente ¿Qué desea hacer?, allí haga clic en el botón Desechar para abrir la ventana emergente Desechar.

## Ventana emergente para desechar[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/scrap_manufacturing.html#id1 "Enlazar permanentemente con este título")

Después de abrir la ventana emergente Desechar con alguno de los métodos [descritos con anterioridad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/scrap_manufacturing.html#manufacturing-management-scrap-window) seleccione el componente o producto terminado a desechar en el menú desplegable Producto.

Escriba la cantidad que desechará en el campo Cantidad.

De forma predeterminada, el campo Ubicación de origen tiene la ubicación de preproducción del almacén establecida, mientras que el campo Ubicación de desecho tiene la ubicación Ubicaciones virtuales/Desechos. Si necesita cambiar la ubicación de origen o de desecho, puede seleccionar una distinta desde los menús desplegables correspondientes.

Seleccione la casilla Reabastecer cantidades desechadas si es necesario crear una orden de recolección para reemplazar los componentes desechados después de confirmar la orden de desecho. Esta opción solo se debería habilitar en los almacenes con fabricación [en dos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/two_step_manufacturing.html) o [en tres pasos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/three_step_manufacturing.html), ya que los componentes no se recolectan como parte del proceso de fabricación [en un paso](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html).

![La ventana emergente de desechar.](https://www.odoo.com/documentation/17.0/es/_images/scrap-window.png)

Haga clic en el botón Desechar para desechar el componente elegido. El botón inteligente Desechos aparece en la parte superior de la pantalla después de crear una o más órdenes de desecho, haga clic allí para ver una lista con todas las órdenes de desecho de la orden de fabricación.

Si se creó una orden de recolección para reabastecer los componentes desechados, podrá acceder a ella si abre la aplicación Inventario. Haga clic en el botón Número por procesar ubicado en la tarjeta Elegir componentes y seleccione la orden.