En Odoo, los plazos entrega se utilizan para predecir cuánto tiempo lleva completar una acción específica. Por ejemplo, es posible establecer un _plazo de entrega_ para un producto comprado, este especifica el número de días que suele tomarle al proveedor del producto entregárselo a la empresa que lo compró.

Si se trata de productos subcontratados, es posible configurar plazos de entrega que consideren el tiempo necesario para que el subcontratista fabrique el producto. De esta manera, la empresa contratante puede planificar mejor las fechas de entrega de estos productos.

Algunos productos subcontratados necesitan que la empresa contratante le proporcione los componentes de fabricación al subcontratista. En este caso es posible utilizar un _plazo de fabricación_ y el plazo de entrega para generar la fecha en la que el subcontratista debe recibir los componentes necesarios para fabricar el producto y entregarlo a tiempo.

 Importante

Como todos los plazos de entrega en Odoo, los plazos de entrega para los productos subcontratados solo son una estimación y están basados el tiempo que se _espera_ que tome realizar las acciones.

Hay circunstancias imprevistas que pueden afectar que estas acciones se lleven a cabo, así que los plazos de entrega **no** están garantizados.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/resupply_subcontracting_lead_times.html#configuration "Enlazar permanentemente con este título")

Al utilizar la ruta [Reabastecer al subcontratista al ordenar](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html), la empresa es responsable de suministrarle los componentes necesarios al subcontratista, entonces el subcontratista no puede comenzar a fabricar los productos hasta que haya recibido los componentes.

Es decir, además del tiempo que el subcontratista tarda en fabricar y entregar el producto, también es necesario considerar la fecha en que recibe los componentes.

Al asignar un plazo de entrega al subcontratista de un producto y especificar un plazo de fabricación en la lista de materiales (LdM) correspondiente, las órdenes de _reabastecimiento al Subcontratista_ para los componentes del producto muestran la fecha límite para que el subcontratista reciba los componentes.

### Plazo de entrega de productos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/resupply_subcontracting_lead_times.html#product-delivery-lead-time "Enlazar permanentemente con este título")

Para configurar el plazo de entrega para el subcontratista de un producto, vaya a Inventario ‣ Productos ‣ Productos y seleccione uno de estos productos.

Después vaya a la pestaña Compras de la página del producto. Si aún no hay ningún proveedor como subcontratista, haga clic en Agregar una línea y selecciónelo en el campo Proveedor.

Luego de agregar al subcontratista, escriba la cantidad de días que le toma fabricar y entregar el producto en la columna Plazo de entrega.

![El campo Plazo de entrega para un subcontratista, en la pestaña Compra de la página de un producto.](https://www.odoo.com/documentation/17.0/es/_images/delivery-lead-time2.png)

### Plazos de fabricación de productos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/resupply_subcontracting_lead_times.html#product-manufacturing-lead-time "Enlazar permanentemente con este título")

Vaya a la lista de materiales del producto. Haga clic en el botón inteligente Lista de materiales ubicado en la parte superior de la página del producto y seleccione una de las LdM de la lista.

Diríjase a la pestaña Varios de la LdM. En el campo Plazo de fabricación escriba el mismo número de días que ingresó en el campo Plazo de entrega del producto de la lista de materiales.

![El campo Plazo de fabricación en la LdM de un producto.](https://www.odoo.com/documentation/17.0/es/_images/manufacturing-lead-time1.png)

Aunque en realidad el subcontratista no utiliza todos estos días para fabricar el producto, establecer el mismo número de días en cada campo le indica a Odoo que el subcontratista debe recibir los componentes y comenzar la producción cuando el plazo de entrega del producto inicie. Esto le proporciona suficiente tiempo al subcontratista para fabricar y entregar el producto.

### Flujo de reabastecimiento al subcontratista[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/resupply_subcontracting_lead_times.html#resupply-subcontracting-workflow "Enlazar permanentemente con este título")

Para crear una solicitud de cotización para el producto, vaya a Compra ‣ Órdenes ‣ Solicitudes de cotización y haga clic en Nuevo.

Especifique al subcontratista en el campo Proveedor y agregue el producto en la pestaña Productos. Haga clic en Agregar un producto, seleccione el producto en la columna correspondiente y especifique la cantidad.

En el campo Entrega esperada ingrese una fecha que proporcione suficiente tiempo para que el subcontratista reciba los componentes, fabrique el producto y se lo entregue a la empresa de subcontratación.

 Importante

Al agregar un producto a una solicitud de cotización, el campo Entrega esperada se completa en automático la fecha correspondiente a la fecha de hoy más el tiempo de entrega del producto. Sin embargo, este **no** considera el tiempo que toma enviar los componentes al subcontratista.

Al comprar un producto subcontratado con la ruta _Reabastecer al subcontratista al ordenar_ es necesario ajustar la fecha para tomar en cuenta el tiempo adicional necesario para enviar los componentes al subcontratista.

Como la producción no comienza hasta recibir los componentes, dejar la fecha tal como está ocasiona que el producto terminado llegue _después_ de la fecha indicada en la solicitud de cotización.

Haga clic en Confirmar orden para convertir la solicitud de cotización en una orden de compra. Esta acción hace que aparezca el botón inteligente Reabastecer en la parte superior de la página.

Haga clic en el botón inteligente Reabastecer para abrir la orden de reabastecimiento al subcontratista, esta es la orden creada para enviarle los componentes al subcontratista.

El campo Fecha límite en la orden correspondiente muestra la fecha indicada para que el subcontratista reciba los componentes, así tendrá suficiente tiempo para fabricar y entregar el producto terminado para la fecha de entrega esperada.

El campo Fecha programada debe mostrar la última fecha en la que es posible enviar los componentes y que aún lleguen al subcontratista antes de la fecha límite. Sin embargo, la fecha que aparece de forma predeterminada es la misma que la fecha del campo Fecha límite y debe actualizarse para tener en cuenta el tiempo necesario para el envío.

Haga clic en el campo Fecha programada para abrir el calendario emergente donde podrá seleccionar una fecha. Elija una que permita entregar los componentes antes de la fecha límite especificada en la orden de reabastecimiento al subcontratista.

Haga clic en el botón Validar ubicado en la parte superior de la orden luego de enviar los componentes para confirmar su envío al subcontratista.

Cuando el el subcontratista recibe los materiales entonces comienzan a fabricar el componente antes de entregárselo a la empresa contratante.

 Example

El distribuidor _Las bicicletas de Miguel_ trabaja con un subcontratista, _Amigos ciclistas_, para producir unidades de su producto _Uniciclo_.

Las bicicletas de Miguel le debe proporcionar los componentes necesarios a Amigos ciclistas para que fabriquen los monociclos.

Amigos ciclistas tarda tres días en promedio en fabricar cada monociclo y a eso hay que sumar dos días más para que en Las bicicletas de Miguel reciban el producto.

Como resultado, Las bicicletas de Miguel establece un plazo de entrega de cinco días para los monociclos fabricados por Amigos ciclistas: tres días para la fabricación y dos días para la entrega.

Agregan un tiempo de producción de cinco días a la lista de materiales del monociclo para poder recordar la fecha en que deben entregar los componentes al subcontratista.

Confirman una orden de compra para un monociclo con fecha de llegada estimada para el 30 de mayo.

La orden de reabastecimiento al subcontratista para enviarle los componentes muestra el 25 de mayo como _fecha límite_. El subcontratista debe recibir los componentes durante o antes de esta fecha para poder fabricar el monociclo a tiempo y entregarlo antes del 30 de mayo.

Las bicicletas de Miguel tardan dos días en entregar los componentes y actualizan el campo _Fecha programada_ en la orden de reabastecimiento al subcontratista hasta el 23 de mayo, dos días antes de la fecha límite.

![Los campos Fecha programada y Fecha límite en una orden de reabastecimiento al contratista.](https://www.odoo.com/documentation/17.0/es/_images/scheduled-deadline.png)

Las bicicletas de Miguel envía los componentes a Amigos ciclistas el día programado, es decir, el 23 de mayo, y estos llegan el día de la fecha límite, es decir, el 25 de mayo. Esto le da suficiente tiempo a Amigos ciclistas para fabricar el monociclo y enviárselo a Las bicicletas de Miguel para la fecha de llegada esperada del 30 de mayo.