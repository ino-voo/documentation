El tablero de _ubicaciones_ de la aplicación _Inventario_ proporciona información general sobre las ubicaciones de almacenamiento disponibles para los productos de la empresa. Utilice este reporte para ver dónde se almacenan las existencias, identificar [artículos extraviados](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/locations.html#inventory-warehouse-storage-stranded) o consultar el inventario anterior para conocer la ubicación de ciertos productos en fechas específicas.

 Nota

Solo los usuarios con [acceso de administrador](https://www.odoo.com/documentation/17.0/es/applications/general/users/access_rights.html) pueden acceder al menú _Reportes_ en la aplicación _Inventario_.

La función _Ubicaciones de almacenamiento_ debe estar habilitada para acceder a este reporte. Para ello, vaya a Inventario ‣ Configuración ‣ Ajustes. Diríjase a la sección Almacén, seleccione la casilla Ubicaciones de almacenamiento y haga clic en Guardar, después vaya al tablero de ubicaciones desde Inventario ‣ Reportes ‣ Ubicaciones.

## Explorar el tablero de ubicaciones[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/locations.html#navigate-the-locations-dashboard "Enlazar permanentemente con este título")

En el tablero de ubicaciones aparecen todos los productos disponibles (en la columna Producto) de forma predeterminada con la siguiente información:

- Ubicación: la ubicación actual de almacenamiento. Si un producto está almacenado en `Estante 1` y `Estante 2`, este aparece dos veces y muestra la cantidad en cada ubicación.
    
- Paquete: el paquete en el que se almacena el producto, en caso de que haya uno.
    
- Número de serie o lote: el número de serie o lote se especifica aquí en caso de que tenga uno.
    
- Cantidad disponible: cantidad actual de productos. Haga clic en el icono  (pencil) para [modificar la cantidad disponible](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/count_products.html).
    
- Cantidad reservada: cantidad disponible reservada para operaciones como recolección, órdenes de entrega o fabricación.
    
- Unidad: la unidad de medida del producto.
    

Haga clic en los botones ubicados a la derecha de cada elemento de la fila para consultar información adicional:

-  Historial: acceda al historial de movimiento de existencias del producto. Aparece la información relacionada con la cantidad y el motivo por el que un producto se trasladó de un lugar a otro.
    
     Truco
    
    Haga clic en el botón  Historial ubicado en el extremo derecho de la línea del producto para ver para qué está reservado.
    
    Elimine el filtro  Hecho en la página Historial de movimientos y después haga clic en el icono  (caret down) ubicado a la derecha de la barra de búsqueda para abrir las opciones de filtro. Seleccione el filtro Por hacer.
    
    ![Mostrar la página *Historial de movimientos* de las entregas pendientes que reservaron el producto.](https://www.odoo.com/documentation/17.0/es/_images/reserved-products.png)
    
-  Reabastecimiento: acceda a la página de [reglas de reordenamiento](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html) para reabastecer productos en alguna ubicación específica.
    

En la esquina superior izquierda de la página, haga clic en el botón Nuevo para realizar un [ajuste de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/count_products.html) y registrar las cantidades de un producto específico en una ubicación determinada.

Para ver los productos, además de su cantidad y ubicación en una fecha específica, haga clic en el botón Inventario a la fecha (también está ubicado en la esquina superior izquierda de la página). Seleccione una fecha y una hora en el campo Inventario a la fecha y después haga clic en Confirmar.

## Generar reportes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/locations.html#generate-reports "Enlazar permanentemente con este título")

Después de aprender cómo [explorar por el tablero de ubicaciones](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/locations.html#inventory-warehouses-storage-locations-report), puede utilizarlo para elaborar y compartir diferentes reportes.

A continuación detallamos algunos reportes comunes que se pueden crear con el tablero de ubicaciones.

### Reporte de existencias remanentes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/locations.html#dead-stock-report "Enlazar permanentemente con este título")

Siga estos pasos para obtener la lista de artículos caducados, también conocidos como _existencias remanentes_:

1. Vaya a Inventario ‣ Reportes ‣ Ubicaciones.
    
2. Luego, haga clic en el icono  (caret down) ubicado a la derecha de la barra de búsqueda para abrir el menú desplegable con las opciones Filtros, Agrupar por y Favoritos.
    
3. Habilite las opciones Ubicaciones internas y Alertas de caducidad en la sección Filtros.
    

El reporte mostrará una lista de productos caducados.

 Nota

También es posible generar este reporte desde la página de [Números de lote y serie](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/expiration_dates.html#inventory-product-management-expiration-alerts). Puede acceder desde Inventario ‣ Productos ‣ Números de serie/lote.

![Mostrar una lista de productos con las fechas de caducidad después del día de hoy.](https://www.odoo.com/documentation/17.0/es/_images/dead-stock.png)

### Reporte de inventario varado[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/locations.html#stranded-inventory-report "Enlazar permanentemente con este título")

Es posible que las empresas que utilizan flujos de varios pasos en las aplicaciones _Inventario_ o _Fabricación_ cuenten con productos _varados_, es decir, productos que no están en la ubicación adecuada debido a errores humanos. Use este reporte para verificar de vez en cuando las ubicaciones de traslados (por ejemplo, _WH/Entrada_, _WH/Preprocesamiento_) y asegurarse de que los productos sean trasladados a las ubicaciones previstas y se registren de forma adecuada en la base de datos.

Siga estos pasos para obtener una lista de elementos que podrían estar detenidos en el almacenamiento:

1. Vaya a Inventario ‣ Reportes ‣ Ubicaciones.
    
2. En la barra de búsqueda escriba el nombre de la ubicación a la que desea mover los productos, como `WH/Entrada` o `WH/Embalaje`.
    
3. Seleccione la opción Buscar ubicación para: [nombre de la ubicación] en el menú desplegable que aparece abajo de la barra de búsqueda.
    
    ![Mostrar resultado de búsqueda de la ubicación.](https://www.odoo.com/documentation/17.0/es/_images/search-input-location.png)
    

En el reporte ahora aparece una lista de productos que se encuentran en la ubicación de tránsito.

 Example

Al buscar `Entrada` en la ubicación aparece una lista de productos en la ubicación _WH/Entrada_.

La lista muestra `500` unidades de `Pollo`, un número alarmante si estas no se refrigeran poco después de recibirlas. El reporte de inventario varado ayuda a identificar los artículos que han estado detenidos en ubicaciones que no son de almacenamiento.

![Visualización de artículos almacenados en una ubicación específica.](https://www.odoo.com/documentation/17.0/es/_images/stranded-inventory.png)

### Reporte de discrepancias de inventario[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/locations.html#inventory-discrepancy-report "Enlazar permanentemente con este título")

Siga estas instrucciones para generar un reporte de los elementos que se han movido desde la última [auditoría de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/cycle_counts.html):

1. Vaya a Inventario ‣ Reportes ‣ Ubicaciones.
    
2. Luego, haga clic en el icono  (caret down) ubicado a la derecha de la barra de búsqueda para abrir el menú desplegable con las opciones Filtros, Agrupar por y Favoritos.
    
3. Habilite las opciones Ubicaciones internas y Conflictos en la sección Filtros.
    
4. El reporte ahora mostrará aquellos elementos que cambiaron en cantidad desde el último conteo de ciclo.
    
    ![Visualización de los artículos del filtro *Conflictos* del reporte.](https://www.odoo.com/documentation/17.0/es/_images/discrepancy.png)
    
5. Haga clic en el botón  Historial para ver los traslados de inventario, incluyendo las recepciones y las entregas, que han ocurrido desde el ajuste correspondiente.
    
    ![Visualización del *historial de movimientos*, aparece una entrega que ocurrió después de un ajuste de inventario.](https://www.odoo.com/documentation/17.0/es/_images/history1.png)