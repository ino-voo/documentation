En Odoo, los plazos entrega se utilizan para predecir cuánto tiempo lleva completar una acción específica. Por ejemplo, es posible establecer un _plazo de entrega_ para un producto comprado, este especifica el número de días que suele tomarle al proveedor del producto entregárselo a la empresa que lo compró.

Si se trata de productos subcontratados, es posible configurar plazos de entrega que consideren el tiempo necesario para que el subcontratista fabrique el producto. De esta manera, la empresa contratante puede planificar mejor las fechas de entrega de estos productos.

Algunos productos subcontratados necesitan que la empresa contratante le proporcione los componentes de fabricación al subcontratista. En este caso es posible utilizar un _plazo de fabricación_ y el plazo de entrega para generar la fecha en la que el subcontratista debe recibir los componentes necesarios para fabricar el producto y entregarlo a tiempo.

En los casos en que los componentes se envían directo al subcontratista es posible establecer un plazo de entrega adicional para cada componente. Este debe ajustarse al tiempo que el proveedor tarda en entregar los componentes al subcontratista.

Después de establecer el tiempo de entrega para un componente, las órdenes de triangulación de ese componente muestran la fecha límite para confirmar la orden, de modo que pueda enviarse directo al subcontratista para la fecha en la que debe comenzar la fabricación.

 Importante

Como todos los plazos de entrega en Odoo, los plazos de entrega para los productos subcontratados solo son una estimación y están basados el tiempo que se _espera_ que tome realizar las acciones.

Hay circunstancias imprevistas que pueden afectar que estas acciones se lleven a cabo, así que los plazos de entrega no están garantizados.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/dropship_subcontracting_lead_times.html#configuration "Enlazar permanentemente con este título")

Al utilizar la ruta [Enviar al subcontratista al ordenar](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html), la empresa es responsable de comprar los componentes necesarios a un proveedor y enviárselos directamente al subcontratista.

Es decir, además del tiempo que le toma al subcontratista fabricar y entregar el producto, también es necesario considerar el tiempo que le toma al proveedor de componentes enviarle los componentes al subcontratista.

Al asignar un _plazo de entrega_ al subcontratista de un producto, especificar un _plazo de fabricación_ en la lista de materiales correspondiente y asignar al proveedor de los componentes un _plazo de entrega adicional_, la fecha límite para confirmar una orden triangulada para enviar los componentes al subcontratista aparece en las órdenes de _envío directo_ para los componentes del producto.

### Plazo de entrega de productos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/dropship_subcontracting_lead_times.html#product-delivery-lead-time "Enlazar permanentemente con este título")

Para configurar el plazo de entrega para el subcontratista de un producto, vaya a Inventario –> Productos –> Productos y seleccione uno de estos productos.

Después vaya a la pestaña Compras de la página del producto. Si aún no hay ningún proveedor como subcontratista, haga clic en Agregar una línea y selecciónelo en la columna Proveedor.

Luego de agregar al subcontratista, escriba la cantidad de días que le toma fabricar y entregar el producto en la columna Plazo de entrega.

![El campo Plazo de entrega para un subcontratista, en la pestaña Compra de la página de un producto.](https://www.odoo.com/documentation/17.0/es/_images/delivery-lead-time1.png)

### Plazos de fabricación de productos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/dropship_subcontracting_lead_times.html#product-manufacturing-lead-time "Enlazar permanentemente con este título")

Vaya a la lista de materiales del producto. Haga clic en el botón inteligente Lista de materiales ubicado en la parte superior de la página del producto y seleccione una de las LdM de la lista.

Diríjase a la pestaña Varios de la LdM. En el campo Plazo de fabricación escriba el mismo número de días que ingresó en el campo Plazo de entrega del producto de la lista de materiales.

![El campo Plazo de fabricación en la LdM de un producto.](https://www.odoo.com/documentation/17.0/es/_images/manufacturing-lead-time.png)

Aunque en realidad el subcontratista no utiliza todos estos días para fabricar el producto, establecer el mismo número de días en cada campo le indica a Odoo que el subcontratista debe recibir los componentes y comenzar la producción cuando el plazo de entrega del producto inicie. Esto le proporciona suficiente tiempo al subcontratista para fabricar y entregar el producto.

### Plazo de entrega de componentes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/dropship_subcontracting_lead_times.html#component-delivery-lead-time "Enlazar permanentemente con este título")

Vaya a cada componente en la lista de materiales (LdM) del producto. Haga clic en el componente en la pestaña Componentes y luego haga clic en el botón  (flecha apuntando hacia la derecha) ubicado junto al componente.

Vaya a la pestaña Compra en la página del producto de cada componente. Si aún no hay ningún proveedor, haga clic en Agregar una línea y seleccione al subcontratista en la columna Proveedor.

Luego de agregar al proveedor, escriba la cantidad de días que le toma enviar el producto al subcontratista en la columna Plazo de entrega.

## Flujo de trabajo de subcontratación por envío directo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/dropship_subcontracting_lead_times.html#dropship-subcontracting-workflow "Enlazar permanentemente con este título")

Para crear una solicitud de cotización para el producto, vaya a Compra ‣ Órdenes ‣ Solicitudes de cotización y haga clic en Nuevo.

Especifique al subcontratista en el campo Proveedor y agregue el producto en la pestaña Productos. Haga clic en Agregar un producto, seleccione el producto en la columna correspondiente y especifique la cantidad.

En el campo Entrega esperada ingrese una fecha que proporcione suficiente tiempo para que el proveedor de componentes los envíe y el subcontratista fabrique y entregue el producto.

 Importante

Al agregar un producto a una solicitud de cotización, el campo Entrega esperada se completa en automático la fecha correspondiente a la fecha de hoy más el tiempo de entrega del producto. Sin embargo, este no considera el tiempo que toma triangular los componentes al subcontratista.

Al comprar un producto subcontratado con la ruta _Enviar al subcontratista al ordenar_ es necesario ajustar la fecha para tomar en cuenta el tiempo adicional necesario para que el subcontratista reciba los componentes.

Como la producción no comienza hasta recibir los componentes, dejar la fecha tal como está ocasiona que el producto terminado llegue _después_ de la fecha indicada en la solicitud de cotización.

Haga clic en Confirmar orden para convertir la solicitud de cotización en una orden de compra. Esta acción crea otra solicitud de cotización para adquirir los componentes con el proveedor encargado del envío directo y enviárselos al subcontratista.

Vaya a Compra ‣ Órdenes ‣ Solicitudes de Cotización y seleccione la solicitud en la que aparece el proveedor encargado del envío directo en la columna Proveedor.

En la solicitud de cotización, el campo Entrega esperada muestra la fecha en la cual el subcontratista debe recibir los componentes para poder entregar el producto terminado para la fecha de _llegada esperada_ indicada en la orden de compra del subcontratista.

El campo Fecha límite de la orden indica la última fecha en la que se puede confirmar la solicitud de cotización para que el proveedor pueda entregar los componentes al subcontratista y así cumplir con la fecha de entrega esperada.

Haga clic en Confirmar orden para convertir la solicitud de cotización en una orden de compra y confirmar la compra de los componentes al proveedor encargado del envío directo. Esta acción hace que aparezca el botón inteligente Triangular en la parte superior de la página.

Haga clic en el botón inteligente Triangular para abrir la orden corrrespondiente, también puede acceder a ella con el botón inteligente Reabastecer que aparece en la orden de compra del subcontratista.

Después de la empresa correspondiente haya entregado los componentes al subcontratista, haga clic en el botón Validar en la parte superior de la orden para confirmar que el subcontratista los recibió.

Cuando el el subcontratista recibe los materiales entonces comienzan a fabricar el componente antes de entregárselo a la empresa contratante.

 Example

El distribuidor _Las bicicletas de Miguel_ trabaja con un subcontratista, _Amigos ciclistas_, para producir unidades de su producto _Bicicleta_.

Las bicicletas de Miguel debe comprar los componentes necesarios del distribuidor El Mundo de las Bicis y luego hacer el envío directo a Amigos ciclistas.

Amigos ciclistas tarda tres días en promedio en fabricar cada bicicleta y a eso hay que sumar dos días más para que en Las bicicletas de Miguel reciban el producto.

Como resultado, Las bicicletas de Miguel establece un plazo de entrega de cinco días para las bicicletas fabricadas por Amigos ciclistas: tres días para la fabricación y dos días para la entrega.

Agregan un tiempo de producción de cinco días a la lista de materiales de la bicicleta para poder recordar la fecha en que deben entregar los componentes al subcontratista.

Le asignan un tiempo de entrega de dos días a El Mundo de las Bicis en las páginas de producto de cada uno de los componentes de la bicicleta, este es el tiempo que necesitan para enviar cada componente al subcontratista.

El 10 de mayo, Las bicicletas de Miguel confirma una orden de compra para una bicicleta con fecha de entrega estimada para el 17 de mayo.

La solicitud de cotización para la compra de los componentes a El Mundo de las Bicis y su envío directo a Amigos ciclistas tiene una fecha de llegada esperada del 12 de mayo y la fecha límite es el 10 de mayo. La solicitud se debe confirmar antes de la fecha límite para que Amigos ciclistas reciba los componentes antes de la fecha de llegada esperada, dándoles suficiente tiempo para entregar la bicicleta terminada a Las bicicletas de Miguel para el 17 de mayo.

![La fecha límite de una orden y las fechas de entrega esperada en una orden de triangulación.](https://www.odoo.com/documentation/17.0/es/_images/deadline-arrival.png)

Las bicicletas de Miguel confirma la solicitud de cotización el 10 de mayo y El Mundo de las Bicis entrega los componentes a Amigos ciclistas el 12 de mayo. Amigos ciclistas fabrica la bicicleta y la entrega a Las bicicletas de Miguel el 17 de mayo.