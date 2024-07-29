Los usuarios pueden monitorear los gastos de aprovisionamiento a lo largo del tiempo con la aplicación _Compra_. Este reporte es útil para que las empresas monitoreen y analicen los gastos, identifiquen oportunidades para ahorrar costos y garanticen una gestión eficiente del presupuesto.

## Crear reportes de gastos de aprovisionamiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/advanced/procurement_expenses_report.html#create-procurement-expenses-report "Enlazar permanentemente con este título")

Para crear un reporte de ingresos esperados, primero vaya a CRM ‣ Reportes ‣ Compra. Esta acción abrirá el tablero de Análisis de compra.

El tablero muestra de forma predeterminada un resumen en forma de gráfico de líneas del total sin Impuestos de las órdenes de compra con fecha de confirmación del mes actual o de las solicitudes de cotización en estado de _Borrador_, _Enviado_ o _Cancelado_.

### Agregar filtros y grupos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/advanced/procurement_expenses_report.html#add-filters-and-groups "Enlazar permanentemente con este título")

Haga clic en el ícono  (tabla dinámica) en la parte superior derecha para cambiar a la vista correspondiente.

 Truco

Es posible [visualizar](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/advanced/procurement_expenses_report.html#purchase-view-results) el reporte como un  (gráfico de barras),  (gráfico de líneas) o  (gráfico circular), pero la vista de tabla dinámica proporciona la vista más detallada de los datos la recomendamos como punto de partida.

Elimine cualquier filtro predeterminado de la barra de búsqueda. Haga clic en  (down) icon para abrir el menú desplegable que contiene las columnas Filtros, Agrupar por y Favoritos.

 Nota

A menos que especifique lo contrario, el reporte muestra la información de las solicitudes de cotización y de las órdenes de compra. Para cambiarlo, seleccione Solicitudes de cotización u Órdenes de compra en la columna Filtros.

Seleccione un plazo para usarlo en la columna Filtros. El reporte se puede filtrar por fecha de la orden o fecha de confirmación. Elija una opción de la lista y haga clic en  (down) icon para especificar el periodo, por ejemplo, mes, trimestre o año.

Seleccione Proveedor en la columna Agrupar por y después elija Categoría de producto, también se encuentra en la misma columna.

 Nota

Es posible modificar las opciones en el encabezado Agrupar por según las necesidades de cada empresa. Por ejemplo, seleccionar Producto en lugar de Categoría de producto proporciona un análisis más detallado acerca del rendimiento de algunos artículos en específico en lugar de una categoría completa.

Seleccione alguna de las opciones disponibles en la sección Comparación, estas aparecen solo después de elegir un rango de fechas en la columna Filtros y varían según el mismo. La opción Periodo anterior agrega una comparación con algún periodo anterior, como el mes o trimestre pasado, mientras que Año anterior compara el mismo periodo del año anterior.

 Nota

Es posible agregar varios filtros relacionados con el tiempo a la vez, pero solo puede seleccionar una comparación.

![El menú desplegable de las opciones filtros, agrupar por y comparación para el reporte de gastos de aprovisionamiento.](https://www.odoo.com/documentation/17.0/es/_images/filters-groups.png)

El filtro para el segundo trimestre, la comparación para el **periodo anterior** y el grupo por **Proveedor** y **Categoría de producto** están seleccionados.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/advanced/procurement_expenses_report.html#id1 "Enlace permanente a esta imagen")

### Agregar medidas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/advanced/procurement_expenses_report.html#add-measures "Enlazar permanentemente con este título")

Haga clic fuera del menú desplegable luego de seleccionar los ajustes de Filtros, Agrupar por y Comparación.

El reporte muestra la información de forma predeterminada con las siguientes medidas: Orden, Total, Total sin impuestos y Cantidad. Haga clic en Medidas en la parte superior izquierda para abrir la lista desplegable con las medidas disponibles.

Haga clic en las siguientes medidas para incluir otras columnas en el reporte de gastos de aprovisionamiento:

- Total y Subtotal: puede incluir una o ambas medidas. Estas se incluyen para realizar un análisis general del gasto.
    
- Costo promedio: se incluye para evaluar la rentabilidad.
    
- Dias para confirmar y Días para recibir: se usan para evaluar el rendimiento del proveedor.
    
- Cantidad ordenada y Cantidad recibida: se usa para entender la eficiencia de la orden.
    
- Cantidad facturada y Cantidad a facturar: se usa para entender la exactitud de la orden.
    

 Truco

Si lo desea puede incluir otras medidas en el reporte para proporcionar más información. Por ejemplo, puede incluir Peso bruto y Volumen para realizar un análisis adicional de logística y gestión.

Haga clic fuera del menú desplegable después de seleccionar todas las medidas necesarias.

## Ver resultados[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/advanced/procurement_expenses_report.html#view-results "Enlazar permanentemente con este título")

El reporte se genera en la vista seleccionada después de seleccionar todos los filtros y medidas correspondientes.

![Una versión de muestra del reporte de gastos de aprovisionamiento.](https://www.odoo.com/documentation/17.0/es/_images/sample-per-report.png)

Haga clic en Insertar en hoja de cálculo para agregar la vista de tabla dinámica a un formato de hoja de cálculo editable en la aplicación _Documentos_.

 Importante

La opción Insertar en hoja de cálculo **solo** está disponible si el módulo _Documentos de hoja de cálculo_ está instalado.

 Nota

El reporte también está disponible en la vista de gráfico. Haga clic en el icono  (gráfico de áreas) para cambiar a la vista de gráfico. Haga clic en el icono correspondiente ubicado en la parte superior del reporte para cambiar a un  (gráfico de barras),  (gráfico de líneas) o  (gráfico circular).

 Ver también

Consulte [Favoritos](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-favorites) para guardar este reporte como _favorito_.