Las _estrategias de remoción_ son bastante útiles para las empresas con almacenes ya que les permiten determinar **qué** productos se toman del almacén y **cuándo**. Por ejemplo, en el caso de los productos perecederos, priorizar la recolección de bienes con la fecha de caducidad más cercana ayuda a minimizar el desperdicio de alimentos.

Las columnas de la siguiente tabla enumeran las estrategias de remoción disponibles en Odoo y detallan cómo se determinan las recolecciones junto con su orden. Utilice estas estrategias de remoción para que Odoo seleccione de forma automática los productos para las órdenes:

||[PEPS](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fifo.html)|[UEPS](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/lifo.html)|[FEFO](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fefo.html)|[Ubicación más cercana](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/closest_location.html)|[Menos paquetes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/least_packages.html)|
|---|---|---|---|---|---|
|Basado en|[Fecha de llegada](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fifo.html#inventory-warehouses-storage-arrival-date)|[Fecha de llegada](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fifo.html#inventory-warehouses-storage-arrival-date)|[Fecha de remoción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fefo.html#inventory-warehouses-storage-removal-date)|[Secuencia de ubicación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/closest_location.html#inventory-warehouses-storage-sequence)|[Cantidad de paquetes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/least_packages.html#inventory-warehouses-storage-pkg-qty)|
|Orden de selección|Primero en entrar|Último en entrar|[Primero en expirar](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fefo.html#inventory-warehouses-storage-exp-date)|[Nombre alfanumérico de la ubicación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/closest_location.html#inventory-warehouses-storage-location-name)|Cantidad más cercana a cumplir con la demanda|

Consulte cada página de la documentación correspondiente por separado para obtener ejemplos detallados sobre cómo usar cada estrategia de remoción.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#configuration "Enlazar permanentemente con este título")

Las estrategias de remoción pueden configurarse en las categorías de producto o en las ubicaciones de almacenamiento.

![Cambiar la estrategia de remoción forzada en las categorías de los productos o en las ubicaciones.](https://www.odoo.com/documentation/17.0/es/_images/navigate-location-category.png)

Configure las estrategias de remoción para ubicación desde Inventario ‣ Configuración ‣ Ubicaciones y seleccione una. En el formulario de ubicación elija alguna de las opciones en el menú desplegable Estrategia de remoción.

 Importante

Las funciones Ubicaciones de almacenamiento y Rutas multietapa **deben** estar habilitadas para poder establecer una estrategia de remoción en una ubicación. Vaya a Inventario ‣ Configuración ‣ Ajustes.

Estas funciones **solo** son necesarias si desea establecer una estrategia de remoción en una ubicación.

Configure las estrategias de remoción para las categorías de producto desde Inventario ‣ Configuración ‣ Categorías de productos y seleccione una. Después, elija una de las opciones del menú desplegable Estrategia de remoción forzada.

 Importante

El valor establecido en el campo Estrategia de remoción forzada de un formulario de categoría de producto se considera prioritario si hay distintas estrategias de remoción aplicadas tanto en una ubicación como una la categoría de producto.

## Funciones necesarias[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#required-features "Enlazar permanentemente con este título")

Aunque algunas estrategias de remoción están disponibles de forma predeterminada, **debe** habilitar algunas funciones adicionales en Inventario ‣ Configuración ‣ Ajustes para que las opciones aparezcan en el menú desplegable del campo Estrategia de remoción forzada o Estrategia de remoción.

Consulte la siguiente tabla para obtener un resumen de las funciones necesarias. De lo contrario, consulte la sección relacionada a una estrategia de remoción específica para obtener más detalles sobre los requisitos y uso.

||PEPS|UEPS|FEFO|Ubicación más cercana|Menos paquetes|
|---|---|---|---|---|---|
|Funciones necesarias|Números de serie y lotes|Números de serie y lotes|Números de serie y lotes, fechas de vencimiento|Ubicaciones de almacenamiento, rutas multietapa|Paquetes|

### Números de lote y de serie[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#lots-and-serial-numbers "Enlazar permanentemente con este título")

Los números de lote y de serie diferencian productos idénticos y llevan seguimiento de información como fechas de llegada o de vencimiento. Para habilitar esta función, vaya a Inventario ‣ Configuración ‣ Ajustes. En la sección de Trazabilidad marque la casilla junto a Números de lote y de serie para habilitar la función.

![Habilitar números de lote y de serie.](https://www.odoo.com/documentation/17.0/es/_images/enable-lots.png)

Asegúrese de que el producto esté rastreado por lotes o números de serie. Vaya al formulario del producto a través de Inventario ‣ Productos ‣ Productos y selecciónelo. En el formulario del producto, vaya a la pestaña Inventario y, en el campo Seguimiento, elija las opciones Por número de serie único o Por lotes.

Después de habilitar estas funciones es importante que asigne números de serie o lotes a los productos mediante un [ajuste de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/count_products.html) o durante la [recepción de productos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#inventory-product-management-assign-lots).

### Ubicaciones y rutas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#locations-and-routes "Enlazar permanentemente con este título")

Las **ubicaciones de almacenamiento** y las **rutas multietapa** son necesarias para configurar **todos** los tipos de estrategias de remoción en una ubicación. Sin embargo, estas funciones son específicamente necesarias para la estrategia de remoción de ubicación más cercana, ya que solo se aplica a nivel de ubicación.

Para habilitar estas funciones, vaya a Inventario ‣ Configuración ‣ Ajustes. En la sección Almacén podrá activar las funciones Ubicaciones de almacenamiento y Rutas multietapa.

![Habilitar las funciones de ubicación y rutas.](https://www.odoo.com/documentation/17.0/es/_images/enable-location1.png)

### Fecha de vencimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#expiration-date "Enlazar permanentemente con este título")

Habilite la función de **fechas de vencimiento** para llevar seguimiento de las fechas de expiración, fechas de consumo preferente, fechas de remoción y fechas de alerta en un número de serie o de lote. Vaya a Inventario ‣ Configuración ‣ Ajustes.

Asegúrese de que la función Números de lote y de serie esté seleccionada en la sección Trazabilidad y luego marque la casilla de Fechas de vencimiento para habilitar la función.

![Habilitar la función de fechas de vencimiento para la estrategia FEFO.](https://www.odoo.com/documentation/17.0/es/_images/enable-expiration.png)

### Paquetes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#packages "Enlazar permanentemente con este título")

La función _Paquetes_ se utiliza para agrupar productos y es necesaria para la estrategia de remoción de menos paquetes.

Vaya a Inventario ‣ Configuración ‣ Ajustes y seleccione la casilla Paquetes para habilitar la función correspondiente.

![Habilitar la función Paquetes.](https://www.odoo.com/documentation/17.0/es/_images/enable-pack1.png)

 Ver también

- [Paquetes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/package.html)
    
- [Entrega en dos pasos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html)
    
- [Entrega en tres pasos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/delivery_three_steps.html)