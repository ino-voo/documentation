El reporte de _pronóstico_ de la aplicación _CRM_ permite que los usuarios vean las próximas oportunidades y elaboren un pronóstico de posibles ventas. Las oportunidades se agrupan por el mes de fecha de cierre esperada y se pueden arrastrar y soltar para ajustar el plazo límite.

Para acceder al reporte de _pronóstico_, vaya a CRM ‣ Reportes ‣ Pronóstico.

## Explorar el reporte de pronóstico[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/forecast_report.html#navigate-the-forecast-report "Enlazar permanentemente con este título")

El reporte de pronóstico predeterminado incluye las oportunidades asignadas al flujo del usuario actual y que se espera que se cierren en los próximos cuatro meses. También muestra las oportunidades sin una fecha esperada de cierre asignada. Las oportunidades están agrupadas por mes en una vista de  (kanban).

![Una versión de muestra del reporte de pronóstico en la aplicación CRM.](https://www.odoo.com/documentation/17.0/es/_images/sample-report.png)

### Fecha de cierre prevista[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/forecast_report.html#expected-closing-date "Enlazar permanentemente con este título")

Las oportunidades se agrupan por la fecha asignada en el campo _Cierre esperado_ en el formulario de oportunidad. Para cambiar esta fecha desde la página Pronóstico, seleccione la tarjeta de kanban de la oportunidad deseada, luego haga clic en ella y arrástrela a la columna correspondiente.

 Nota

El plazo predeterminado para el pronóstico es [*](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/forecast_report.html#id1)mes y puede cambiarlo al hacer clic en  (down) icon junto a la barra de búsqueda ubicada en la parte superior del reporte. En el encabezado Agrupar por del menú desplegable, haga clic en Cierre esperado para abrir la lista con opciones disponibles y seleccionar el periodo deseado.

Después de agregar una oportunidad a un nuevo mes, el campo _Cierre esperado_ del formulario de la oportunidad se actualiza a la _última_ fecha del mes antes mencionado.

 Truco

El campo _Cierre esperado_ también se puede actualizar de forma manual en la tarjeta de la oportunidad. Para hacerlo, haga clic en la tarjeta de kanban correspondiente en la página Pronóstico para abrir su formulario de detalles, después haga clic en el campo Cierre esperado y use el calendario emergente para seleccionar una nueva fecha de cierre.

### Ingreso prorrateado[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/forecast_report.html#prorated-revenue "Enlazar permanentemente con este título")

En la parte superior de la columna de cada mes en la página del reporte de pronóstico, del lado derecho de la barra de progreso, está la suma de los ingresos prorrateados para ese periodo.

El ingreso prorrateado se calcula con la siguiente fórmula:

Ingreso esperado×Probabilidad=Ingreso prorrateado

Al mover las oportunidades de una columna a otra, el ingreso esta se actualiza en automático para reflejar el cambio.

 Example

El reporte de pronóstico del mes de junio incluye dos oportunidades:

La primera oportunidad, `Global Solutions`, tiene un ingreso esperado de `$3,800` y una probabilidad del `90%`. Como resultado, el ingreso prorrateado es de `$3,420`.

La segunda oportunidad, `Cotización por 600 sillas`, tiene un ingreso esperado de `$22,500` y una probabilidad del `20%`. Como resultado, el ingreso prorrateado es de `$4,500`.

El ingreso prorrateado combinado de las oportunidades es de `$7,920` y aparece en la parte superior de la columna del mes.

![Un ejemplo de los ingresos prorrateados para un mes del reporte de pronóstico.](https://www.odoo.com/documentation/17.0/es/_images/example-revenue.png)

 Ver también

Consulte [Asignación de leads con la puntuación predictiva de leads](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/lead_scoring.html) para obtener más información sobre la asignación de probabilidad a las oportunidades.

## Ver resultados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/forecast_report.html#view-results "Enlazar permanentemente con este título")

Haga clic en el icono  (gráfico de áreas) para cambiar a la vista de gráfico. Haga clic en el icono correspondiente ubicado en la parte superior del reporte para cambiar a un  (gráfico de barras),  (gráfico de líneas), o  (gráfico circular).

![Una vista de gráfico circular del reporte de pronóstico.](https://www.odoo.com/documentation/17.0/es/_images/pie-chart-view.png)

Haga clic en  (pivot) icon para cambiar a la vista de tabla dinámica o en  (list) icon para cambiar a la vista de lista.

 Truco

La [vista de tabla dinámica](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#reporting-using-pivot) es útil para ver y analizar datos con mayor detalle. Es posible seleccionar varias medidas, así como visualizar los datos por mes y por etapa de la oportunidad.

![Una muestra del reporte de pronóstico en la vista de tabla dinámica.](https://www.odoo.com/documentation/17.0/es/_images/pivot-view1.png)

 Ver también

Consulte [Favoritos](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-favorites) para guardar este reporte como _favorito_.