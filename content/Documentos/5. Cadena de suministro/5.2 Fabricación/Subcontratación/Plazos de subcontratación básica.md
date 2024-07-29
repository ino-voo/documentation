En Odoo, los plazos entrega se utilizan para predecir cuánto tiempo lleva completar una acción específica. Por ejemplo, es posible establecer un _plazo de entrega_ para un producto comprado, este especifica el número de días que suele tomarle al proveedor del producto entregárselo a la empresa que lo compró.

Si se trata de productos subcontratados, es posible configurar plazos de entrega que consideren el tiempo necesario para que el subcontratista fabrique el producto. De esta manera, la empresa contratante puede planificar mejor las fechas de entrega de estos productos.

 Importante

Como todos los plazos de entrega en Odoo, los plazos de entrega para los productos subcontratados solo son una estimación y están basados el tiempo que se _espera_ que tome realizar las acciones.

Hay circunstancias imprevistas que pueden afectar que estas acciones se lleven a cabo, así que los plazos de entrega no están garantizados.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/basic_subcontracting_lead_times.html#configuration "Enlazar permanentemente con este título")

Al utilizar el flujo de trabajo [básico de subcontratación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html) para fabricar un producto, la empresa no es responsable de suministrarle los componentes necesarios al subcontratista. Esto significa que los únicos factores que influyen en la fecha de entrega del producto son el tiempo que lleva al subcontratista fabricarlo y entregarlo.

Al asignar un plazo de entrega a un subcontratista de un producto que considere ambos factores, la fecha de _entrega esperada_ que aparece en las órdenes de compra del producto refleja con mayor precisión el tiempo necesario para fabricar y entregar.

### Plazo de entrega de productos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/basic_subcontracting_lead_times.html#product-delivery-lead-time "Enlazar permanentemente con este título")

Para configurar el plazo de entrega para el subcontratista de un producto, vaya a Inventario ‣ Productos ‣ Productos y seleccione uno de estos productos.

Después vaya a la pestaña Compras de la página del producto. Si aún no hay ningún proveedor como subcontratista, haga clic en Agregar una línea y selecciónelo en la columna Proveedor.

Luego de agregar al subcontratista, escriba la cantidad de días que le toma fabricar y entregar el producto en la columna Plazo de entrega.

![El campo Plazo de entrega para un subcontratista, en la pestaña Compra de la página de un producto.](https://www.odoo.com/documentation/17.0/es/_images/delivery-lead-time.png)

 Nota

Es posible agregar varios subcontratistas en la pestaña Compras en la página de un producto y también puede establecer un tiempo de entrega distinto para cada uno.

## Flujo de trabajo de plazos de entrega[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/basic_subcontracting_lead_times.html#lead-time-workflow "Enlazar permanentemente con este título")

Cree una solicitud de cotización luego de establecer un plazo de entrega para un proveedor de un producto. Vaya a Compra ‣ Órdenes ‣ Órdenes de compra y haga clic en Nuevo.

Especifique al subcontratista en el campo Proveedor y agregue el producto en la pestaña Productos. Haga clic en Agregar un producto, seleccione el producto en la columna correspondiente y escriba la cantidad.

Después de agregar un producto, el campo Entrega esperada en la solicitud de cotización se completa en automático con una fecha que muestra el plazo de entrega del proveedor tal como se especifica en la página del producto.

Haga clic en el campo Entrega esperada si necesita ajustar la fecha, esto abrirá un calendario emergente donde podrá seleccionar la fecha deseada. Asegúrese de no elegir una fecha anterior a la que se completó de forma automática a menos que el subcontratista haya confirmado que puede entregar el producto para esa fecha.

Por último, haga clic en Confirmar orden en la solicitud de cotización para convertirla en una orden de compra. En ese momento el subcontratista debería comenzar a fabricar el producto subcontratado antes de entregárselo a la empresa contratante.

 Example

El distribuidor _Las bicicletas de Miguel_ trabaja con un subcontratista, _Amigos ciclistas_, para producir unidades de su producto _Triciclo_.

Amigos ciclistas necesita tres días en promedio para fabricar un triciclo y a eso hay que sumar dos días más para que se lo entreguen a Las bicicletas de Miguel.

Como resultado, Las bicicletas de Miguel establece un plazo de entrega de cinco días para los triciclos fabricados por Amigos ciclistas: tres días para la fabricación y dos días para la entrega.

Las bicicletas de Miguel confirma una orden de compra el 3 de mayo para adquirir un triciclo en Amigos ciclistas.

La fecha de llegada esperada que aparece en la orden de compra es el 8 de mayo, cinco días después de la fecha de confirmación.

![La fecha de entrega esperada en un orden de compra para un producto subcontratado.](https://www.odoo.com/documentation/17.0/es/_images/expected-arrival.png)

Amigos ciclistas comienza a fabricar el triciclo el 3 de mayo (el mismo día que se confirma la orden de compra) y termina el 6 de mayo, tres días después.

Envían el triciclo a Las bicicletas de Miguel el mismo día y la empresa lo recibe dos días después, es decir, el 8 de mayo.