Al enviar productos a los clientes, el costo en destino es el precio total de un producto o envío. Este incluye todos los gastos asociados con el envío del producto.

En Odoo, la función _Costos en destino_ se utiliza para tomar en cuenta costos adicionales al calcular la valoración de un producto, como el costo de envío, seguro, impuestos aduaneros, impuestos generales y otros cargos.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/integrating_landed_costs.html#configuration "Enlazar permanentemente con este título")

La función _Costos en destino_ debe estar activada para poder agregarlos a los productos. Vaya a Inventario ‣ Configuración ‣ Ajustes y diríjase a la sección Valoración.

Seleccione la casilla junto a la opción Costos en destino y haga clic en Guardar.

La página se actualizará y aparecerá un nuevo campo, Diario predeterminado, abajo de la función Costos en destino en la sección Valoración.

Haga clic en el menú desplegable Diario predeterminado para abrir la lista de diarios contables. Seleccione el diario en el que se registrarán todos los asientos relacionados con los costos en destino.

![La función de costos en destino y el campo de diario predeterminado que aparece en los ajustes de Inventario.](https://www.odoo.com/documentation/17.0/es/_images/integrating-landed-costs-enabled-setting.png)

## Crear un producto de costo en destino[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/integrating_landed_costs.html#create-landed-cost-product "Enlazar permanentemente con este título")

Cuando se trata de cargos que se agregan como costos en destino con frecuencia, entonces debe crear un producto de costo en destino en Odoo. De esta forma, podrá agregar el producto de costo en destino con rapidez a la factura de proveedor como una línea en la factura en lugar de tener que agregar esta información cada que cree una.

Cree un nuevo producto desde Inventario ‣ Productos ‣ Productos, allí haga clic en Nuevo.

Asigne un nombre al producto de costo en destino en el campo Nombre del producto (por ejemplo, `Envíos internacionales`). En el campo Tipo de producto, haga clic en el menú desplegable y seleccione Servicio como Tipo de producto.

 Importante

Los productos de costo en destino **deben** estar configurados con servicio como tipo de producto.

Haga clic en la pestaña Compra y seleccione la casilla ubicada junto a Es un costo en destino que se encuentra en la sección Facturas de proveedores. Después de seleccionarla aparece el campo Método de división predeterminado abajo. Al hacer clic en ese menú desplegable aparecen las siguientes opciones:

- Igual: divide el costo por igual entre cada producto incluido en el recibo, independientemente de la cantidad de cada uno.
    
- Por cantidad: divide el costo entre las unidades de todos los productos en el recibo.
    
- Por costo actual: divide el costo de acuerdo con el costo de cada unidad de producto. Un producto con un costo más alto recibe una mayor proporción del costo en destino.
    
- Por peso: divide el costo de acuerdo con el peso de los productos en el recibo.
    
- Por volumen: divide el costo de acuerdo con el volumen de los productos en el recibo.
    

![La casilla Es un costo en destino y el método de división predeterminado en el formulario de un producto de tipo servicio.](https://www.odoo.com/documentation/17.0/es/_images/integrating-landed-costs-landed-cost-product.png)

Al crear nuevas facturas de proveedores es posible agregar este producto como una línea de factura que corresponda a un costo en destino.

 Importante

Para aplicar un costo en destino a una factura de proveedor, los productos incluidos en la [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/integrating_landed_costs.html#id1) **deben** pertenecer a la _Categoría del producto_ con la _Estrategia de remoción forzada_ configurada como FIFO. El _método de costo_ puede ser [|Costo promedio (ACVO)|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/integrating_landed_costs.html#id3) o FIFO y el método de valoración puede ser [manual](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/using_inventory_valuation.html) o [automático](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html).

## Crear una orden de compra[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/integrating_landed_costs.html#create-purchase-order "Enlazar permanentemente con este título")

Vaya a Compra ‣ Nuevo para crear una nueva solicitud de cotización. En el campo Proveedor, agregue el proveedor al que le ordenará los productos y después haga clic en Agregar un producto en la pestaña Productos para agregarlos a la solicitud correspondiente.

Cuando haya terminado, haga clic en Confirmar orden para confirmarla, después haga clic en Recibir productos una vez que hayan sido recibidos y por último, haga clic en Validar.

### Crear una factura de proveedor[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/integrating_landed_costs.html#create-vendor-bill "Enlazar permanentemente con este título")

Una vez que el proveedor cumpla con la orden de compra y envíe la factura, podrá crear la factura de proveedor desde la orden de compra en Odoo.

Vaya a Compra, haga clic en la orden de compra de la que se debe crear la factura de proveedor y luego haga clic en Crear factura. Esto abrirá una nueva factura de proveedor en la etapa de borrador.

En el campo Fecha de la factura, haga clic en la línea para abrir un menú emergente de calendario y seleccione la fecha en la que se debe facturar este borrador.

Después, en la pestaña Líneas de factura, haga clic en Agregar una línea y en el menú desplegable de la columna Producto seleccione el producto de costo en destino que creó con anterioridad. Haga clic en el icono  (nube con una flecha) para guardar de forma manual y actualizar la factura que se encuentra en borrador.

![Las casillas de la columna de costos en destino para el producto y el costo en destino.](https://www.odoo.com/documentation/17.0/es/_images/integrating-landed-costs-checkboxes.png)

En la columna Costos en destino, el producto que le ordenó al proveedor **no** tiene su casilla seleccionada, mientras que la casilla del producto de costo en destino **sí** lo está. Esto diferencia los costos en destino de todos los demás que aparecen en la factura.

Además, el botón Crear costos en destino aparece en la parte superior del formulario.

![El botón para crear costos en destino en una factura de proveedor.](https://www.odoo.com/documentation/17.0/es/_images/integrating-landed-costs-create-button.png)

## Agregar costos en destino[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/integrating_landed_costs.html#add-landed-cost "Enlazar permanentemente con este título")

Haga clic en el botón Crear costos en destino ubicado en la parte superior del formulario después de agregar uno a la factura de proveedor.

Esto creará en automático un registro de costo en destino con uno completado con anterioridad en la línea del producto en la pestaña Costos adicionales.

En el formulario de costo en destino haga clic en el menú desplegable Traslado y seleccione a cuál traslado pertenece este costo.

![Formulario de costo en destino con un traslado de recepción seleccionado.](https://www.odoo.com/documentation/17.0/es/_images/integrating-landed-costs-transfers-menu.png)

 Truco

Además de crear costos en destino desde una factura de proveedor, también puede crear los registros de estos costos desde Inventario ‣ Operaciones ‣ Costos en destino, luego haga clic en Nuevo.

Luego de configurar la recolección con el menú desplegable Traslados, haga clic en Calcular (se encuentra en la parte inferior del formulario, abajo del costo total).

Haga clic en la pestaña Ajustes de valoración para ver cómo influyeron los costos en destino. En la columna Valor original aparece el precio original de la orden de compra, la columna Costo en destino adicional muestra el costo en destino y la columna Nuevo valor muestra la suma de ambos, para el costo total de la orden.

Después haga clic en Validar para registrar el asiento del costo en destino en el diario contable.

Esta acción hace que el botón inteligente Valoración aparezca en la parte superior del formulario. Haga clic en él para abrir la página de valoración de existencias que incluye la valoración actualizada del producto.

 Nota

Para que el botón inteligente Valuación aparezca luego de esto, es **necesario** que el tipo de producto sea almacenable.

Vaya a Inventario ‣ Reportes ‣ Valoración para ver la valoración de _todos_ los productos, entre ellos, los de costo en destino.

 Nota

Cada asiento creado para un costo en destino en una factura de proveedor es visible en la aplicación _Contabilidad_.

Para localizar estos asientos contables, vaya a Contabilidad ‣ Contabilidad ‣ Asientos contables y busque el asiento correspondiente por número (por ejemplo, `PBNK1/2024/XXXXX`).

Haga clic en el asiento contable para visualizar los apuntes contables y otra información relacionada.

![Formulario de asiento contable para el costo en destino creado a partir de la factura del proveedor.](https://www.odoo.com/documentation/17.0/es/_images/integrating-landed-costs-journal-entry.png)