Use el reporte de existencias de la aplicación _Inventario_ para consultar una lista detallada con todos los productos almacenados entre los que se encuentran los que están reservados, los que fueron comprados y los que están en tránsito, además de los que ya fueron entregados a los clientes.

 Nota

Solo los usuarios con [acceso de administrador](https://www.odoo.com/documentation/17.0/es/applications/general/users/access_rights.html) pueden acceder a las funciones de reportes.

Vaya a Inventario ‣ Reportes ‣ Existencias para consultar el reporte correspondiente.

![Imagen de la lista de reporte de existencias que se encuentra en Inventario > Reportes > Existencias.](https://www.odoo.com/documentation/17.0/es/_images/stock-report1.png)

## Explorar el reporte de existencias[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/stock.html#navigate-the-stock-report "Enlazar permanentemente con este título")

La barra lateral izquierda del reporte de existencias incluye varios grupos para filtrar lo que aparece. Los grupos predeterminados son Almacenes, que filtra productos por almacenes específicos, y Categoría, que muestra productos dentro de la categoría seleccionada.

 Nota

The Warehouse grouping is only available when there are multiple warehouses in the database. Refer to the [Warehouses](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/warehouses.html) documentation for more details.

En el reporte aparecen las siguientes columnas para representar la siguiente información:

- Producto: nombre del producto.
    
- Costo unitario: valoración promedio del inventario por unidad, ajustada según el costo de compra o fabricación del producto.
    
- Valor total: valoración total del inventario del producto, calculada al multiplicar el costo unitario por la cantidad disponible.
    
     Ver también
    
    - [Calcular el costo promedio por unidad de la valuación de inventario](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/avg_price_valuation.html#inventory-avg-cost-formula)
        
    - [Métodos de valuación de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html)
        
    
- Disponible: cantidad actual de productos. Haga clic en el icono  (pencil) para [modificar la cantidad disponible](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/count_products.html).
    
- Disponible para uso: cantidad disponible que **no** está reservada para órdenes de entrega o fabricación y que está disponible para vender o utilizar.
    
- Entrante: artículos que se espera su llegada al almacén. El número de productos está basado en la cantidad de las órdenes de compra confirmadas.
    
- Saliente: artículos que se espera que salgan del almacén o se consuman en las órdenes de fabricación. El número de productos está basado en la cantidad de las órdenes de venta o fabricación confirmadas.
    

Haga clic en los botones ubicados a la derecha de cada elemento de la fila para consultar información adicional:

- Historial: acceda al historial de movimiento de existencias del producto. Aparece la información relacionada con la cantidad y el motivo por el que un producto se trasladó de un lugar a otro.
    
- Reabastecimiento: acceda a la página de [reglas de reordenamiento](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html) del producto para crear o gestionar métodos de reabastecimiento.
    
- Ubicaciones: desglose de la cantidad disponible en distintas ubicaciones de almacenamiento. Solo está disponible cuando el producto está almacenado en varias ubicaciones.
    
- Pronóstico: consulte el reporte de pronóstico para visualizar la cantidad disponible, entrante y saliente. El reporte también incluye enlaces a órdenes de compra, venta o fabricación confirmadas. Solo está disponible cuando el producto tiene alguna de las órdenes antes mencionadas confirmadas.
    

### Opciones de búsqueda[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/stock.html#search-options "Enlazar permanentemente con este título")

FiltersGroup ByFavorites

La sección de Filtros permite que los usuarios busquen entre filtros predefinidos y personalizados para encontrar registros específicos de las existencias.

- Publicado: muestra los productos publicados en el sitio web. Solo está disponible si la aplicación _Sitio web_ está instalada.
    
- Disponible en PdV: mostrar productos disponibles a través de la aplicación _Punto de venta_.
    
- Disponible en auto: muestra productos disponibles en autopedido mediante la aplicación _Punto de venta_. Aparece en la búsqueda porque la casilla Disponible en auto está seleccionada en la sección Punto de venta de la pestaña Ventas del formulario del producto. La opción solo está disponible si la casilla Disponible en PdV está seleccionada.
    
    ![La función *Disponible en autopedido* en la pestaña Compra del formulario de un producto.](https://www.odoo.com/documentation/17.0/es/_images/available-in-self-order.png)
    
- No disponible en auto: mostrar productos disponibles en el _PdV_, pero que no están disponibles en autopedido.
    

 Ver también

[Configurar productos para el punto de venta](https://youtu.be/REbA3TBhFa4)

- Se puede vender: muestra productos que se pueden vender a los clientes. Aparece en la búsqueda porque la casilla Se puede vender está seleccionada en el formulario del producto.
    
- Se puede comprar: muestra productos que se pueden comprar a los proveedores. Aparece en la búsqueda porque la casilla Se puede comprar está seleccionada en el formulario del producto.
    
- Puede ser recurrente: muestra productos de suscripción que tienen la casilla Recurrente seleccionada en su formulario de producto. Solo está disponible si la aplicación _Suscripciones_ está activada.
    
- Se puede alquilar: muestra productos que se pueden alquilar a clientes durante un periodo predeterminado. Aparece en la búsqueda porque la casilla Se puede alquilar está seleccionada en el formulario del producto. Solo está disponible si la aplicación _Alquiler_ está instalada.
    
- Se puede subcontratar: muestra productos que un [fabricante externo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html) puede fabricar. Solo está disponible si la aplicación _Fabricación_ está instalada.
    
- Puede ser un gasto: muestra elementos que se pueden contabilizar como gastos. Solo está disponible si la aplicación _Gastos_ está instalada.
    

 Ver también

[Tipo de producto](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html)

 Ver también

[Buscar, filtrar y agrupar registros](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html)