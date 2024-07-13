En el menú Reportes de la mayoría de las aplicaciones puede encontrar varios reportes que le permiten analizar y visualizar los datos de sus registros.

## Seleccionar una vista[](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#selecting-a-view "Enlazar permanentemente con este título")

Dependiendo del reporte, Odoo puede mostrar los datos de varias formas. Algunas veces está disponible una vista única personalizada por completo al reporte, mientras que varias vistas están disponibles para otros. Sin embargo, hay dos vistas genéricas específicas para los reportes: las vistas de gráfico y tabla dinámica.

### Vista de gráfico[](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#graph-view "Enlazar permanentemente con este título")

La [vista de gráfico](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#reporting-using-graph) se utiliza para visualizar los datos de sus registros, esta le ayudará a identificar patrones y tendencias. A menudo puede encontrar esta vista en el menú reportes de las aplicaciones, pero también puede encontrarla en otros lugares. Para acceder a ella, haga clic en el **botón de vista de gráfico** que se ubica en la parte superior derecha de la página.

![Seleccionar la vista de gráfico](https://www.odoo.com/documentation/17.0/es/_images/graph-button.png)

### Vista de tabla dinámica[](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#pivot-view "Enlazar permanentemente con este título")

La [vista de tabla dinámica](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#reporting-using-pivot) se utiliza para agregar los datos de sus registros y desglosarlos para su análisis. Puede encontrar esta vista en el menú reportes de las aplicaciones, pero también puede encontrarla en otros lugares. Para acceder a ella, haga clic en el **botón de vista de tabla dinámica** que se ubica en la parte superior derecha de la página.

![Selección de la vista de tabla dinámica](https://www.odoo.com/documentation/17.0/es/_images/pivot-button.png)

## Elegir medidas[](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#choosing-measures "Enlazar permanentemente con este título")

Tras seleccionar una vista, debe asegurarse de que solo se [filtran](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html) los registros relevantes. A continuación, debe elegir lo que se medirá. Siempre hay una medida seleccionada de forma predeterminada, si desea editarla haga clic en medidas y elija una, o varias en el caso de las tablas dinámicas.

 Nota

Cuando selecciona una medida, Odoo agrega los valores registrados en ese campo para los registros filtrados. Solo se pueden medir los campos numéricos [enteros](https://www.odoo.com/documentation/17.0/es/applications/studio/fields.html#studio-fields-simple-fields-integer), [decimales](https://www.odoo.com/documentation/17.0/es/applications/studio/fields.html#studio-fields-simple-fields-decimal) y [monetarios](https://www.odoo.com/documentation/17.0/es/applications/studio/fields.html#studio-fields-simple-fields-monetary). Además, la opción «número» se utiliza para contar el número total de registros filtrados.

Después de elegir qué desea medir, puede definir cómo se deben [agrupar](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-group) los datos según la dimensión que desea analizar. De forma predeterminada, los datos se agrupan por _Fecha > Mes_ para analizar la evolución de las medidas a lo largo de los meses.

 Truco

Cuando filtra un solo periodo de tiempo, se habilita la opción de compararlo con otro.

![Uso de la opción de comparación](https://www.odoo.com/documentation/17.0/es/_images/comparison.png)

 Example

Select measuresGroup measures

Entre otras medidas, puede agregar las medidas de margen y número al reporte de análisis de ventas. De forma predeterminada, se selecciona la medida importe sin impuestos.

![Selección de distintas medidas en el reporte de análisis de ventas](https://www.odoo.com/documentation/17.0/es/_images/measures.png)

## Utilizar la vista de tabla dinámica[](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#using-the-pivot-view "Enlazar permanentemente con este título")

Agrupar datos es esencial para la vista de tabla dinámica pues le permite desglosar los datos para obtener información más detallada. Aunque puede usar la opción Agrupar por para agregar con rapidez un grupo en el nivel de las filas, como se muestra en el ejemplo anterior. También puede hacer clic en el botón con el signo de más (➕) junto al encabezado de total en el nivel de las filas _y_ columnas, y luego seleccionar uno de los **grupos preconfigurados**. Para eliminar uno, haga clic en el botón con el signo de menos (➖).

Una vez que agregue un grupo, puede agregar nuevos en el eje opuesto o en los subgrupos recién creados.

 Example

Puede dividir aún más las medidas en el ejemplo anterior del reporte de análisis de ventas mediante el grupo vendedor en el nivel de columnas y el grupo Fecha de orden > Mes en la categoría de producto Todos / Se pueden vender / Muebles de oficina.

![Agregar varios grupos a un reporte de análisis de ventas](https://www.odoo.com/documentation/17.0/es/_images/multiple-groups.png)

 Truco

- Puede cambiar los grupos de las filas y columnas al hacer clic en el botón «girar eje» (⇄).
    
- Puede hacer clic en la etiqueta de una medida para ordenar los valores en orden ascendente (⏶) o descendente (⏷).
    
- Puede descargar una versión `.xlsx` de la tabla dinámica al hacer clic en el botón de descarga (⭳).
    

## Utilizar la vista de gráfico[](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#using-the-graph-view "Enlazar permanentemente con este título")

Hay tres gráficos disponibles: de barras, de líneas y circular.

Los **gráficos de barras** se utilizan para mostrar la distribución o una comparación de varias categorías. Son bastante útiles, ya que pueden trabajar con conjuntos grandes de datos.

Los **gráficos de líneas** son útiles para mostrar los cambios en series temporales y tendencias a lo largo del tiempo.

Los **gráficos circulares** se utilizan para mostrar la distribución o comparación de un pequeño número de categorías cuando son parte de un conjunto significativo.

Bar chartLine chartPie chart

![Vista del reporte de análisis de ventas como gráfico de barras](https://www.odoo.com/documentation/17.0/es/_images/bar.png)

 Truco

Para los gráficos de **barras** y **líneas** puede usar la opción de apilado cuando tiene al menos dos grupos, aparecerán uno encima del otro en lugar de uno junto al otro.

Stacked bar chartRegular bar chartStacked line chartRegular line chart

![Ejemplo de gráfico de barras apilado](https://www.odoo.com/documentation/17.0/es/_images/stacked-bar.png)

Para los gráficos de **líneas** puede usar la opción de acumulativo para sumar valores, resulta bastante útil para mostrar el cambio en el crecimiento durante un período de tiempo.

Cumulative line chartRegular line chart

![Ejemplo de gráfico de líneas acumulativo](https://www.odoo.com/documentation/17.0/es/_images/cumulative.png)

 [Edit on GitHub](https://github.com/odoo/documentation/edit/17.0/content/applications/essentials/reporting.rst)

##### EN ESTA PÁGINA

- - [Seleccionar una vista](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#selecting-a-view)
        
    - [Elegir medidas](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#choosing-measures)
    - [Utilizar la vista de tabla dinámica](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#using-the-pivot-view)
    - [Utilizar la vista de gráfico](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html#using-the-graph-view)