En Odoo, hay dos estrategias para reabastecer automáticamente el inventario: _reglas de reordenamiento_ y la ruta _fabricación sobre pedido (MTO)_. Aunque estas estrategias difieren ligeramente, ambas tienen consecuencias similares: desencadenar la creación automática de una [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id2) u [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id4). La elección de la estrategia a utilizar depende de los procesos de fabricación y entrega de la empresa.

## Terminología[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#terminology "Enlazar permanentemente con este título")

### Reporte de reabastecimiento y reglas de reordenamiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#replenishment-report-and-reordering-rules "Enlazar permanentemente con este título")

El reporte de reabastecimiento es una lista de todos los productos que tienen una cantidad de pronóstico negativa.

_Las reglas de reordenamiento_ son usadas para asegurar que siempre hay una cantidad mínima de un producto en existencias, para poder fabricar productos y/o cumplir con ordenes de venta. Cuando el nivel de existencias de un producto alcanza su cantidad mínima, Odoo genera automáticamente una orden de compra con la cantidad necesaria para alcanzar el nivel máximo de existencias.

Puede crear y gestionar reglas de reordenamiento en el reporte de reabastecimiento, o desde el formulario de producto.

### Fabricación sobre pedido[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#make-to-order "Enlazar permanentemente con este título")

_Fabricación sobre pedido (MTO)_ es una ruta de aprovisionamiento que crea un proyecto de orden de compra (u orden de fabricación) cada vez que se confirma una orden de venta, **sin tener en cuenta el nivel actual de existencias**.

A diferencia de los productos reabastecidos mediante reglas de reordenamiento, Odoo vincula automáticamente la orden de venta a la [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id6) u [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id8) generada por la ruta MTO.

Otra diferencia entre las reglas de reordenamiento y MTO es que con MTO Odoo genera un borrador de [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id10) u [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id12) inmediatamente después de que se confirme una [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id14). Mientras que con las reglas de reordenamiento, Odoo genera un borrador de [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id16) o MO cuando las existencias pronosticadas del producto están por debajo de la cantidad mínima establecida.

Además, Odoo añade automáticamente cantidades a la [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id18) u [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id20) cuando cambia el pronóstico, siempre que la [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id22) u [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id24) no esté confirmada.

La ruta MTO es la mejor estrategia de reabastecimiento para productos que son personalizados o para productos que no tienen existencias disponibles.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#configuration "Enlazar permanentemente con este título")

### Reporte de reabastecimiento y reglas de reordenamiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id1 "Enlazar permanentemente con este título")

Para acceder al reporte de reabastecimiento, vaya a la aplicación Inventario ‣ Operaciones ‣ Reabastecimiento.

De forma predeterminada, el tablero de reporte de reabastecimiento muestra cada producto que se debe reordenar manualmente. Si no hay una regla específica para un producto, Odoo asume que las existencias mínimas y máximas son ambas `0.00`.

 Nota

Para los productos que no cuentan con una regla de reorden establecida, Odoo calcula el pronóstico según las órdenes de venta confirmadas, las entregas y los recibos. En el caso de productos con una regla de reorden establecida, Odoo calcula el pronóstico con normalidad, pero también tiene en cuenta el tiempo de espera de compra/fabricación y el tiempo de espera de seguridad.

 Importante

Antes de crear una nueva regla de reordenación, asegúrese de que el producto tiene un _proveedor_ o una _lista de materiales_ definidos en el formulario del producto. Para comprobarlo, vaya a la aplicación :menuselection:` Inventario –> Productos –> Productos`, y seleccione el producto para abrir su formulario de producto. Si se estableció, el proveedor aparecerá en la pestaña Compra, y si se estableció la lista de materiales, aparecerá en el botón inteligente Lista de materiales en la parte superior del formulario.

El tipo de producto, ubicado en la pestaña información general en el formulario del producto, se **debe** definir como producto consumible. Por definición, no se lleva un control de los niveles de inventario de un producto consumible, por lo que Odoo no puede incluir un producto consumible en el reporte de reabastecimiento.

![Reporte de reabastecimiento que enumera todos los artículos que se deben comprar para cubrir las necesidades actuales.](https://www.odoo.com/documentation/17.0/es/_images/replenishment-report-dashboard.png)

Si desea crear una nueva regla de reabastecimiento desde el reporte de reabastecimiento, vaya a la aplicación Inventario ‣ Operaciones ‣ Reabastecimiento, haga clic en Crear, y seleccione el producto deseado en el menú desplegable de la columna Producto. Si lo necesita, también puede establecer una cantidad mínima y una cantidad máxima en las columnas correspondientes de la página del reporte de reabastecimiento.

Para crear una nueva regla de reordenamiento desde el formulario de producto, vaya a la aplicación Inventario ‣ Productos ‣ Productos, y seleccione un producto para abrir su formulario de producto. Haga clic en el botón inteligente Reglas de reordenamiento, haga clic en Crear y complete los campos.

#### Campos del reporte de reabastecimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#replenishment-report-fields "Enlazar permanentemente con este título")

Los siguientes campos se encuentran en el reporte de reabastecimiento. Si alguno de estos campos no está visible, haga clic en el icono ⋮ (opciones adicionales) situado en el extremo derecho del reporte y haga clic en la casilla de verificación situada junto al campo para hacerlo visible.

- Producto: el producto que se debe reabastecer.
    
- Ubicación: la ubicación específica donde se almacena el producto.
    
- Almacén: el almacén donde se almacena el producto.
    
- Disponible: la cantidad de producto disponible.
    
- Pronóstico: la cantidad de producto disponible después de considerar todas las órdenes actuales (ventas, fabricación, compra, etc).
    
- Ruta preferida: cómo se adquiere el producto, puede ser por Compra, Fabricación, Envío directo, etc.
    
- Proveedor: la empresa de la cual se adquiere el producto.
    
- Lista de materiales: la lista de materiales del producto (si está configurada).
    
- Activador: cómo se crea el reaprovisionamiento, ya sea de forma Automática (una vez que la cantidad :guilabel: `a la mano` es inferior a la :guilabel: `cantidad mínima`) o :guilabel: `manual` (solo cuando se solicita el reaprovisionamiento).
    
- Grupo de aprovisionamiento: el número de referencia de cómo se adquiere el producto, puede ser por una orden de cliente, una orden de compra o una orden de fabricación.
    
- Cantidad mínima: la cantidad mínima de producto que debe estar disponible. Cuando los niveles de inventario son inferiores a esta cantidad, se activa el reabastecimiento.
    
- Cantidad máxima: la cantidad de producto que debe quedar disponible tras el reabastecimiento del producto.
    
- Cantidad múltiple: si el producto debe pedirse en cantidades específicas, introduzca el número que debe pedirse. Por ejemplo, si Cantidad múltiple se establece en `5`, y solo se necesitan 3, se repondrán 5 productos.
    
- Por ordenar: la cantidad de producto que se necesita actualmente y que se pedirá si hace clic en el botón Ordenar una vez o Automatizar órdenes.
    
- UdM: la unidad de medida utilizada para adquirir el producto.
    
- Empresa: la empresa para la que se adquiere el producto.
    

De forma predeterminada, la cantidad del campo Por ordenar es la cantidad necesaria para alcanzar la cantidad máxima establecida. Sin embargo, la cantidad por ordenar puede ajustarse haciendo clic en el campo y cambiando el valor. Para reabastecer un producto de forma manual, haga clic en Ordenar una vez.

Para automatizar un reabastecimiento desde la página Reabastecimiento, haga clic en Automatizar órdenes en la parte derecha de la línea, representada por el icono 🔄 (flecha circular).

Cuando se hace clic en este botón, Odoo generará automáticamente un borrador de [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id26)/[|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id28) cada vez que el nivel de existencias pronosticado caiga por debajo de la cantidad mínima de la regla de reordenamiento.

En la página Reabastecimiento, se puede desactivar temporalmente una regla de reordenamiento o un reabastecimiento manual durante un periodo determinado, solo debe hacer clic en el icono 🔕 (posponer) ubicado en el extremo derecho de la línea.

![Las opciones para posponer permiten desactivar las notificaciones de reordenamiento durante un periodo de tiempo.](https://www.odoo.com/documentation/17.0/es/_images/reordering-rule-snooze-settings.png)

Una [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id30) u [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id32) creada por un reabastecimiento manual tiene un Reporte de reabastecimiento como documento de origen. Una [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id34) u [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id36) creada por una regla de reordenamiento automatizada tiene el número de referencia [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#id38) que activó la regla como documento de origen.

![La lista de solicitudes de cotización muestra qué cotizaciones provienen directamente del reporte de reabastecimiento.](https://www.odoo.com/documentation/17.0/es/_images/rfq-source-document.png)

## Ruta de fabricación sobre pedido (MTO)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#make-to-order-mto-route "Enlazar permanentemente con este título")

Dado que la ruta MTO se recomienda para productos personalizados, la ruta está oculta de forma predeterminada.

Para activar la ruta MTO en Odoo:

1. Vaya a la aplicación Inventario ‣ Configuración ‣ Ajustes.
    
2. Active la opción Rutas multietapa, ubicada en la sección Almacén, y haga clic en Guardar.
    
3. Luego, vaya a la aplicación Inventario ‣ Configuración ‣ Rutas.
    
4. Haga clic en Filtros ‣ Archivado para mostrar las rutas archivadas.
    
5. Seleccione la casilla junto a Reabastecer sobre pedido (MTO), y haga clic en Acción ‣ Desarchivar.
    

 Nota

Al activar la configuración de las Rutas multietapa también se activan ubicaciones de almacenamiento. Si el almacén no utiliza estas funciones, desactívelas después de desarchivar la ruta MTO.

Para establecer la ruta de aprovisionamiento de un producto a MTO, vaya a la aplicación Inventario ‣ Productos ‣ Productos y haga clic en el producto deseado para abrir su formulario.

Luego, haga clic en la pestaña Inventario y en la sección Rutas de las opciones, seleccione Reabastecer sobre pedido (MTO).

Asegúrese de seleccionar la ruta Comprar para los productos que compra directamente a un proveedor, además de la ruta Reabastecer sobre pedido (MTO). También asegúrese de que un proveedor esté configurado en la pestaña Compra del formulario de producto.

Para los productos que fabrica de forma interna, asegúrese de seleccionar la ruta Fabricación, además de la ruta Reabastecer sobre pedido (MTO). También asegúrese de configurar una lista de materiales para el producto, puede acceder mediante el botón inteligente Lista de materiales en el formulario del producto.

 Nota

La ruta MTO **solo** funciona si también selecciona la ruta Fabricación o Comprar.

![La ruta "Reabastecer sobre pedido" seleccionada en el formulario del producto.](https://www.odoo.com/documentation/17.0/es/_images/acoustic-block-screen-replenish.png)

 [Edit on GitHub](https://github.com/odoo/documentation/edit/17.0/content/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.rst)

##### En esta página

- - [Terminología](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#terminology)
        
    - [Configuración](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#configuration)
        
    - [Ruta de fabricación sobre pedido (MTO)](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html#make-to-order-mto-route)