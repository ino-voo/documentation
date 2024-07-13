_Los ingresos esperados_ es el valor total de efectivo de los leads que se espera recibir en una fecha en específico, usualmente al final del mes en curso.

Un _reporte de ingresos esperados_ recopila todos los leads activos en una cartera de ventas que tienen una fecha de cierre esperada establecida, y compara el rendimiento de los equipos de ventas en un plazo determinado.

![Imagen con acercamiento de la fecha prevista de cierre de un cliente potencial en la aplicación CRM.](https://www.odoo.com/documentation/17.0/es/_images/expected-revenue-closing.png)

Al elaborar un reporte mensual de ingresos previstos, los gerentes de ventas pueden ver qué miembros del equipo están alcanzando sus objetivos y quiénes pueden necesitar ayuda adicional para cerrar buenos tratos.

## Crear un reporte de ingresos esperados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html#create-an-expected-revenue-report "Enlazar permanentemente con este título")

Para crear un reporte de ingresos esperados, primero vaya a aplicación CRM ‣ Reportes ‣ Flujo. Esto abrirá el tablero de Análisis del flujo.

 Importante

El tablero de _Análisis de flujo_ incluye varios filtros en la barra de búsqueda de forma predeterminada, elimínelos antes de agregar más filtros personalizados.

Haga clic en Medidas en la parte superior izquierda del reporte y luego seleccione Ingresos esperados en el menú desplegable.

En la parte superior de la página, haga clic en el icono 🔻(triángulo apuntando hacia abajo) situado a la derecha de la barra Buscar… para abrir el menú desplegable que contiene las columnas Filtros, Agrupar por y Favoritos. Bajo la columna Filtros, haga clic en Añadir filtro personalizado, que abre una ventana emergente Añadir filtro personalizado.

### Añadir filtros personalizados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html#add-custom-filters "Enlazar permanentemente con este título")

Para poder generar un reporte de ingresos esperados, debe crear filtros para seguir las siguientes condiciones:

> - [Fecha de cierre prevista](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html#expected-revenue-report-closing-date): limita los resultados para que sólo incluyan los clientes potenciales que se espera que se cierren dentro de un plazo específico.
>     
> - [Número de leads sin asignar](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html#expected-revenue-report-unassigned-leads): excluye leads sin vendedor asignado.
>     
> - [Equipos de venta específicos](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html#expected-revenue-report-sales-team): limita los resultados para que solo incluyan leads asignados a uno o más equipos de ventas. Este filtro es opcional, no lo incluya si el reporte está dirigido a toda la empresa.
>     

#### Agregar filtro para fecha de cierre prevista[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html#add-filter-for-expected-closing-date "Enlazar permanentemente con este título")

En la ventana emergente Agregar filtro personalizado, haga clic en el primer campo de la nueva regla. Escriba `Cierre esperado` en la barra Buscar…, o desplácese para seleccionarlo de la lista. Haga clic en el segundo campo y seleccione está establecido. Esto limita los resultados para que sólo incluyan clientes potenciales en los que aparezca una fecha de cierre estimada.

Después haga clic en el símbolo ➕ (más) a la derecha de la regla para duplicarla.

 Truco

Con el símbolo de ➕ (más) es más fácil agregar varias reglas basadas en el mismo filtro.

En el segundo campo de la nueva regla, seleccione es entre en el menú desplegable. De este modo se crea un intervalo de tiempo durante el cual debe producirse la fecha de cierre prevista para que los clientes potenciales se incluyan en los resultados.

Haga clic en cada campo de fecha, de uno en uno, y utilice la ventana emergente del calendario para añadir una fecha de inicio y otra de fin a la regla. Normalmente se trata del inicio y el final del mes o trimestre fiscal en curso.

#### Excluir leads no asignados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html#exclude-unassigned-leads "Enlazar permanentemente con este título")

Después de filtrar por la fecha de cierre esperada, agregue una nueva regla. Haga clic en el primer campo de la nueva regla y escriba `Vendedor` en la barra de búsqueda o busque en la lista para seleccionarlo. Haga clic en el segundo campo de la regla y en el menú desplegable seleccione está establecido, esto excluirá cualquier resultado que no tenga un vendedor asignado.

#### Agregar un filtro para equipos de ventas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html#add-a-filter-for-sales-teams "Enlazar permanentemente con este título")

 Nota

Este filtro es opcional. Para ver los resultados de toda la empresa, **no** añada este filtro y continúe en [Ver resultados](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html#expected-revenue-report-view-results).

Para limitar los resultados del informe a uno o más equipos de ventas, haga clic en Nueva regla. A continuación, haga clic en el primer campo de la nueva regla y escriba «Equipo de ventas» en la barra Buscar… o desplácese por la lista para localizarlo.

En el segundo campo de la regla, seleccione está en en el menú desplegable. La selección de este operador limita los resultados a los equipos de ventas indicados en el campo siguiente.

Por último, haga clic en el tercer campo y, o bien realice una selección de la lista completa que aparece en el menú emergente, o bien escriba los primeros caracteres del título del equipo de ventas específico para encontrarlo rápidamente y seleccionarlo como parámetro.

 Truco

Se pueden añadir varios equipos a la regla «Equipo de ventas», donde cada parámetro se trata con un operador «o» (por ejemplo, «cualquiera») en la lógica de búsqueda.

![Ventana emergente para agregar filtros personalizados con filtros personalizados configurados para el reporte de ingresos esperados.](https://www.odoo.com/documentation/17.0/es/_images/custom-filters.png)

## Ver resultados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html#view-results "Enlazar permanentemente con este título")

En la parte superior del formulario Agregar filtro personalizado hay una opción para que coincida con cualquiera de las reglas o con todas ellas. Para ejecutar el reporte de forma correcta solo debe incluir los registros que coincidan con **todos** los siguientes filtros. Antes de agregar los filtros asegúrese de que la opción Todos está seleccionada en este campo.

![Haga hincapié en la opción coincidir con todos los filtros de la ventana emergente Añadir filtro personalizado.](https://www.odoo.com/documentation/17.0/es/_images/match-all-filters.png)

En la parte inferior del formulario Agregar un filtro personalizado haga clic en Agregar.

### Ver opciones[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html#view-options "Enlazar permanentemente con este título")

El informe de ingresos previstos se beneficia de la utilización de múltiples vistas. La vista de gráfico predeterminada puede utilizarse para identificar qué vendedores se espera que generen más ingresos, mientras que la vista de lista y la vista pivotante proporcionan más detalles sobre acuerdos específicos.

Graph viewList viewPivot view

La vista _gráfica_ se utiliza para visualizar datos, y es beneficiosa para identificar patrones y tendencias.

_Los gráficos de barras_ se utilizan para mostrar la distribución de los datos entre varias categorías o entre varios vendedores.

_Los gráficos de líneas_ son útiles para mostrar tendencias cambiantes a lo largo de un periodo de tiempo.

_Los gráficos circulares_ son útiles para mostrar la distribución, o comparación, de datos entre un pequeño número de categorías o vendedores, concretamente cómo forman la parte significativa de una imagen completa.

La vista predeterminada del reporte de ingresos previstos es el gráfico de barras apilado. Para usar una vista de gráfico diferente, haga clic en uno de los iconos ubicados en la parte superior izquierda del reporte. El gráfico de líneas y el de barras están disponibles en vista apilada, pero el gráfico circular no.

![Vista de cerca de los iconos de gráfico en el reporte de análisis de flujo en la aplicación CRM.](https://www.odoo.com/documentation/17.0/es/_images/graph-view-icons.png)

Iconos de vista de gráfico en orden: barras, línea, circular, apilados.