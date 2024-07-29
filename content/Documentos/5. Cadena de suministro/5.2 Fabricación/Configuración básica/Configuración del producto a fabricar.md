Para fabricar un producto con la aplicación _Fabricación_ de Odoo, el producto debe estar configurado de forma correcta. Esto consiste en habilitar la ruta _Fabricación_ y configurar una lista de materiales (LdM) para el producto. Una vez que haya completado estos pasos, puede seleccionar el producto al crear una nueva orden de fabricación.

## Activar la ruta de fabricación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/configure_manufacturing_product.html#activate-the-manufacture-route "Enlazar permanentemente con este título")

La ruta de fabricación se activa para cada producto desde su propia página. Vaya a Fabricación ‣ Productos ‣ Productos y seleccione un producto existente o cree uno nuevo con el botón correspondiente.

En la página del producto, seleccione la pestaña Inventario y active la casilla Fabricación en la sección Rutas. Esto le indica a Odoo que el producto se puede fabricar.

![La ruta de fabricación en la pestaña Inventario en la página de un producto.](https://www.odoo.com/documentation/17.0/es/_images/manufacturing-route.png)

### Seguimiento por número de serie o lote[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/configure_manufacturing_product.html#lot-serial-number-tracking "Enlazar permanentemente con este título")

No es obligatorio asignar números de serie o lotes a los productos recién fabricados. Para [asignar estos números](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html) de forma opcional, vaya a la sección Trazabilidad en la pestaña Inventario. En el campo Seguimiento, seleccione Por número de serie único o Por lotes.

Esto habilita el campo _Número de lote o serie_ en una orden de fabricación o la instrucción _Registrar producción_ en una tarjeta de orden de trabajo en la aplicación _Taller_.

![Campo "Número de serie o lote" en la orden de fabricación.](https://www.odoo.com/documentation/17.0/es/_images/lot-number-field.png)

Campo **Número de serie o lote** en la orden de fabricación.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/configure_manufacturing_product.html#id1 "Enlace permanente a esta imagen")

![La opción **Registrar producción* para generar el número de serie o lote en una tarjeta de orden de trabajo.](https://www.odoo.com/documentation/17.0/es/_images/register-production.png)

La opción [**](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/configure_manufacturing_product.html#id1)Registrar producción* para generar el número de serie o lote en una tarjeta de orden de trabajo.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/configure_manufacturing_product.html#id2 "Enlace permanente a esta imagen")

## Configurar una lista de materiales (LdM)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/configure_manufacturing_product.html#configure-a-bill-of-materials-bom "Enlazar permanentemente con este título")

A continuación, debe configurar una lista de materiales (LdM) para el producto para que Odoo sepa cómo se fabrica. Una LdM es una lista de los componentes y operaciones que se necesitan para fabricar un producto.

Para crear una LdM para un producto específico, vaya a Fabricación ‣ Productos ‣ Productos y seleccione el producto. En la página del producto, haga clic en el botón inteligente Lista de materiales en la parte superior de la página, luego seleccione Nuevo para configurar una nueva LdM.

![El botón inteligente de lista de materiales en la página de un producto.](https://www.odoo.com/documentation/17.0/es/_images/bom-smart-button1.png)

En [|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/configure_manufacturing_product.html#id1)a LdM, el campo Producto se completa en automático. Especifique el número de unidades que produce la LdM en el campo Cantidad.

Para agregar un componente a la LdM seleccione la pestaña Componentes y haga clic en Agregar una línea, elija un componente del menú desplegable Componente y escriba la cantidad en el campo correspondiente. Continúe agregando componentes en nuevas líneas hasta que haya terminado de incluir todos.

![La pestaña Componentes en una lista de materiales.](https://www.odoo.com/documentation/17.0/es/_images/components-tab.png)

A continuación, seleccione la pestaña Operaciones, haga clic en Agregar una línea y aparecerá la ventana emergente Crear operaciones. Especifique el nombre de la operación a agregar (por ejemplo, ensamblaje, corte, etc.) en el campo correspondiente y, en el menú desplegable Centro de trabajo, seleccione el lugar donde se realizará la operación. Por último, haga clic en Guardar y cerrar para terminar de agregar operaciones o en Guardar y crear nuevo para agregar más.

 Importante

La pestaña Operaciones solo aparece si la función Órdenes de trabajo está activada. Vaya a Fabricación ‣ Configuración ‣ Ajustes y seleccione la casilla Órdenes de trabajo.

![La pestaña Operaciones en una lista de materiales.](https://www.odoo.com/documentation/17.0/es/_images/operations-tab1.png)

 Más información

La sección anterior proporciona instrucciones para crear una lista de materiales básica que permita fabricar un producto en Odoo. Sin embargo, no es un resumen exhaustivo de todas las opciones de configuración disponibles. Para obtener más información sobre las listas de materiales, consulte la documentación sobre cómo [crear una lista de materiales](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html).