El reporte de antigüedad del inventario evalúa todos los artículos en existencia y proporciona información sobre los costos de compra potencialmente irrecuperables y los retrasos en la rentabilidad.

Cree tablas dinámicas personalizadas para analizar el producto, los tipos de operación, el mes o los desgloses de la empresa. Estas le ayudan a identificar los productos en sus existencias que se aproximan a sus fechas de vencimiento o viabilidad, además de aquellos casos de podredumbre o descomposición si se trata de artículos que vencen con rapidez.

 Nota

Solo los usuarios con [acceso de administrador](https://www.odoo.com/documentation/17.0/es/applications/general/users/access_rights.html) pueden acceder al menú _Reportes_ en la aplicación _Inventario_.

Vaya a Inventario ‣ Reportes ‣ Antigüedad del inventario para consultar el reporte correspondiente.

## Explorar el reporte de antigüedad del inventario[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/aging.html#navigate-the-inventory-aging-report "Enlazar permanentemente con este título")

El reporte de antigüedad del inventario muestra una tabla dinámica de forma predeterminada con los meses en las columnas y las categorías de producto en las filas. Los filtros predeterminados, Entrante y Tiene cantidad restante, solo muestran los productos de las recepciones y que están disponibles.

Cant. restante muestra el número de artículos disponibles y Valor restante muestra el costo total de comprarlos.

Al hacer clic en el icono  (más) de cada columna o fila aparecen otras opciones para expandir la tabla dinámica y mostrar un desglose detallado de cantidad restante y valor restante por producto, categoría de producto, fecha o empresa. Al hacer clic en el icono  (menos) esta se reduce de nuevo al estado anterior.

![Reporte de antigüedad del inventario.](https://www.odoo.com/documentation/17.0/es/_images/inventory-aging.png)

Reporte de antigüedad del inventario con los **productos** en las filas y las **fechas de recepción** en las columnas. Esto ayuda a monitorear mejor los productos con fechas de vencimiento próximas. Cada fila muestra la cantidad total disponible y la valoración del inventario de los artículos comprados en cada día.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/aging.html#id1 "Enlace permanente a esta imagen")

 Nota

Los registros en el reporte de antigüedad de inventario son las _capas de valoración de existencias_ (SVL), estas representan los movimientos de productos que influyen en la valoración del inventario.

Los ajustes de inventario **no** crean _capas de valoración de existencias_ (SVL), solo los artículos comprados a proveedores.

## Generar reportes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/aging.html#generate-reports "Enlazar permanentemente con este título")

Después de aprender cómo [explorar por el reporte de antigüedad del inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/aging.html#inventory-warehouses-storage-aging-report), puede utilizarlo para elaborar y compartir diferentes reportes.

A continuación detallamos algunos reportes comunes que puede crear con el reporte de antigüedad del inventario.

### Reporte de rotación de existencias[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/aging.html#rotating-stock-report "Enlazar permanentemente con este título")

Siga estos pasos para crear un reporte para identificar los artículos que han estado en sus existencias durante algún tiempo:

1. Vaya a Inventario ‣ Reportes ‣ Antigüedad del inventario.
    
2. En el reporte de antigüedad del inventario, haga clic en el icono  (flecha hacia abajo) en la barra de búsqueda para abrir una lista desplegable con las opciones Filtros, Agrupar por y Favoritos.
    
3. Seleccione Producto en la sección Agrupar por. Esta acción abrirá la tabla dinámica para mostrar un producto en cada fila.
    
4. Haga clic en el icono  (más) ubicado a la izquierda de la columna de fechas. Pase el cursor por encima de Fecha en el menú desplegable y elija Año, Trimestre, Mes, Semana o Día. Al hacer esto aparecerán las columnas para mostrar la cantidad restante y el valor restante según el periodo seleccionado.
    
     Truco
    
    Si se trata de productos que tienen mayor vida útil, elija periodos más largos como Mes o Trimestre al expandir las columnas por Fecha.
    
    ![Tabla dinámica, resaltando el icono "más" para expandir las columnas.](https://www.odoo.com/documentation/17.0/es/_images/column-expand-icon.png)
    
5. El reporte ahora muestra el inventario de artículos disponibles y su costo total de compra para cada periodo.
    
     Example
    
    La siguiente imagen ejemplifica un reporte de antigüedad de inventario con la opción Agrupar por: Producto seleccionada y con la columna Fecha configurada en Día. Proporciona información sobre cuántos productos de sashimi de pescado crudo se compraron cada día y cuánto costaron. Esta información es útil para que los propietarios del negocio sepan cuántas existencias por día podrían descomponerse en el almacén.
    
    ![Reporte de antigüedad de inventario. Aparecen las filas de productos y columnas de días.](https://www.odoo.com/documentation/17.0/es/_images/inventory-aging.png)