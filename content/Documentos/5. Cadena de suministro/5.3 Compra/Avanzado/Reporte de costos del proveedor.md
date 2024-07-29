La aplicación _Compra_ permite que los usuarios puedan monitores la fluctuación de los costos de los proveedores a lo largo del tiempo. Esto les ayuda a identificar los proveedores que tienen precios más caros y a llevar seguimiento de los cambios en cada temporada.

## Crear reportes de costos del proveedor[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/advanced/vendor_costs_report.html#create-vendor-costs-reports "Enlazar permanentemente con este título")

Para elaborar un reporte de costos de proveedores, primero vaya a Compra ‣ Reportes ‣ Compras para abrir el tablero de Análisis de compra. En este tablero aparece de forma predeterminada una vista general con un gráfico de líneas del total sin impuestos de las órdenes de compra con fecha de confirmación del mes actual o de las solicitudes de cotización en estado de _borrador_, _enviadas_ o _canceladas_.

### Agregar filtros y grupos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/advanced/vendor_costs_report.html#add-filters-and-groups "Enlazar permanentemente con este título")

Haga clic en el ícono  (tabla dinámica) en la parte superior derecha para cambiar a la vista correspondiente.

Elimine cualquier filtro predeterminado de la barra de búsqueda. Haga clic en  (down) icon para abrir el menú desplegable que contiene las columnas Filtros, Agrupar por y Favoritos.

 Nota

A menos que especifique lo contrario, el reporte muestra la información de las solicitudes de cotización y de las órdenes de compra. Para cambiarlo, seleccione Solicitudes de cotización u Órdenes de compra en la columna Filtros.

Seleccione un intervalo de fechas para usarlo en la columna Filtros. El reporte se puede filtrar por fecha de la orden o fecha de confirmación. Elija una opción de la lista y haga clic en  (down) icon para especificar el periodo, por ejemplo, mes, trimestre o año.

Seleccione Proveedor en la columna Agrupar por y después elija Producto, también se encuentra en la misma columna.

 Nota

Seleccionar un producto **no** es obligatorio para este reporte, pero le recomendamos que lo haga porque proporciona información adicional sobre el rendimiento de cada proveedor. También es posible elegir otras opciones en el encabezado Agrupar por, como Categoría de producto, Estado y Representante de compras.

Verifique que Proveedor sea la **primera** opción seleccionada en la columna Agrupar por para asegurar que el reporte se genere correctamente.

Seleccione alguna de las opciones disponibles en la sección Comparación, estas aparecen solo después de elegir un rango de fechas en la columna Filtros y varían según el mismo. La opción Periodo anterior agrega una comparación con algún periodo anterior, como el mes o trimestre pasado, mientras que Año anterior compara el mismo periodo del año anterior.

 Nota

Es posible agregar varios filtros relacionados con el tiempo a la vez, pero solo puede seleccionar una comparación.

![El menú desplegable de las opciones filtros, agrupar por y comparación para el reporte de costos de proveedor.](https://www.odoo.com/documentation/17.0/es/_images/filters-groups1.png)

### Agregar medidas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/advanced/vendor_costs_report.html#add-measures "Enlazar permanentemente con este título")

Haga clic fuera del menú desplegable luego de seleccionar los ajustes de Filtros, Agrupar por y Comparación.

El reporte aparece de forma predeterminada con las siguientes medidas: Orden, Total, Total sin impuestos y Cantidad. Haga clic en el botón Medidas ubicado en la parte superior izquierda para abrir la lista desplegable de medidas disponibles. Haga clic en Costo promedio para agregarlo al reporte. Seleccione cualquier medida adicional para agregarla o, si lo desea, haga clic en cualquiera de las medidas ya seleccionadas para eliminarlas.

 Truco

Le recomendamos que elabore el reporte con las opciones Costo promedio, Total o Total sin impuestos seleccionadas en la lista de medidas. Es posible agregar otras medidas como Días para recibir para obtener información detallada.

## Ver resultados[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/advanced/vendor_costs_report.html#view-results "Enlazar permanentemente con este título")

El reporte se genera en la vista de tabla dinámica luego de seleccionar todos los [filtros y medidas](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/advanced/vendor_costs_report.html#purchase-vender-cost-report-filters). Haga clic en Insertar en hoja de cálculo para agregar esta vista a un formato de hoja de cálculo editable dentro de la aplicación _Documentos_.

 Importante

La opción Insertar en hoja de cálculo solo está disponible si el módulo _Documentos de hoja de cálculo_ está instalado.

![Un ejemplo del reporte de costos de proveedor con las medidas establecidas como costos totales y promedio.](https://www.odoo.com/documentation/17.0/es/_images/sample-vendor-report.png)

 Nota

El reporte de costos del proveedor también está disponible en la vista de _gráfico_. Haga clic en el icono  (gráfico de áreas) para cambiar a la vista de gráfico. Haga clic en el icono correspondiente ubicado en la parte superior del reporte para cambiar a un  (gráfico de barras),  (gráfico de líneas) o  (gráfico circular).

 Ver también

Consulte [Favoritos](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-favorites) para guardar este reporte como _favorito_.