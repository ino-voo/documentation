La aplicación _Evaluaciones_ de Odoo lleva seguimiento de dos métricas a medida que completa evaluaciones: un [análisis de evaluación](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/reporting.html#appraisals-analysis-report) y una [evolución de habilidades](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/reporting.html#appraisals-skills-report).

## Análisis de evaluaciones[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/reporting.html#appraisal-analysis "Enlazar permanentemente con este título")

Para acceder al reporte de _análisis de evaluaciones_, vaya a Evaluaciones ‣ Reportes ‣ Análisis de evaluaciones.

En la página de análisis de evaluaciones hay un reporte de todas las evaluaciones en la base de datos y su estado aparece representado por distintos colores.

Las evaluaciones en amarillo están _completas_, las que están en naranja están en progreso (es decir, la _evaluación ha sido enviada_, pero no está completada), las que están en rojo fueron _canceladas_ y las que aparecen en gris están _programadas_ (según los [Planes de evaluación](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals.html#appraisals-appraisal-plan)), pero aún no han sido confirmadas.

El reporte muestra el año actual en vista de Gantt de forma predeterminada y está agrupado por departamento.

Para cambiar el periodo que aparece de forma predeterminada deberá cambiar los ajustes de fecha ubicados en la parte superior izquierda del reporte. Las opciones de visualización son Día, Semana, Mes y Año. Utilice las flechas para avanzar o retroceder en el tiempo.

En cualquier momento puede hacer clic en el botón Hoy para que la vista de Gantt incluya la fecha actual.

El reporte puede tener otros [filtros](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-filters) y [grupos](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-group) establecidos en la barra de búsqueda que se encuentra en la parte superior.

![Un reporte que muestra todas las evaluaciones para el reporte de Análisis de evaluación.](https://www.odoo.com/documentation/17.0/es/_images/analysis.png)

 Example

Las evaluaciones canceladas aparecen en color rojo en el reporte de análisis de evaluaciones, pero no hay un filtro preconfigurado para que solo las evaluaciones canceladas sean visibles.

Para ver solo las evaluaciones canceladas, haga clic en el icono  (flecha hacia abajo) en la barra de búsqueda.

Después haga clic en Agregar filtro personalizado en la sección :guilabel:[`](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/reporting.html#id1)Filtros. Esta acción abrirá la ventana emergente correspondiente.

Con el menú desplegable, seleccione Estado en el primero y luego seleccione Cancelado en el tercero. Haga clic en el botón Agregar y solo aparecerán las evaluaciones canceladas.

![La ventana emergente de filtro personalizado con los parámetros configurados para que solo aparezcan las evaluaciones canceladas.](https://www.odoo.com/documentation/17.0/es/_images/custom-filter.png)

## Evolución de las habilidades[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/reporting.html#skills-evolution "Enlazar permanentemente con este título")

Para acceder al reporte de _evolución de habilidades_, vaya a Evaluación ‣ Reportes ‣ Evolución de las habilidades. La página del reporte de las habilidades evaluadas incluye un reporte con todas estas agrupadas por empleado.

Los niveles de habilidad **solo** se actualizan después de marcar una evaluación como completada. Cualquier cambio en los niveles de habilidad correspondiente a las evaluaciones activas que **no** han sido finalizadas **no** se incluyen en este reporte.

Todas las líneas del reporte están ocultas de forma predeterminada. Haga clic en cualquier parte de la línea para abrir los datos y ver sus detalles.

Cada habilidad cuenta con la siguiente información:

- Empleado: el nombre del empleado.
    
- Tipo de habilidad: la categoría a la que pertenece la habilidad.
    
- Habilidad: la habilidad específica e individual.
    
- Nivel de habilidad anterior: el nivel que el empleado había alcanzado con anterioridad en la habilidad.
    
- Progreso anterior de la habilidad: el porcentaje anterior de dominio alcanzado para la habilidad (según el nivel de habilidad).
    
- Nivel actual de la habilidad: el nivel actual que el empleado tiene en esa habilidad.
    
- Progreso actual de la habilidad: el porcentaje actual de dominio alcanzado para la habilidad.
    
- Justificación: cualquier nota proporcionada en la habilidad que explique el progreso.
    

El color del texto de la habilidad indica los cambios que han ocurrido desde la evaluación anterior. Los niveles que han aumentado aparecen color en verde como _Mejora_, los que no han cambiado aparecen en color negro como _Sin cambio_ y los que han disminuido aparecen en color rojo como _Retroceso_.

![Un reporte que muestra todas las habilidades agrupadas por empleado.](https://www.odoo.com/documentation/17.0/es/_images/skills-report.png)

El reporte puede tener otros [filtros](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-filters) y [grupos](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-group) establecidos en la barra de búsqueda que se encuentra en la parte superior.

 Example

El reporte de habilidades de evaluación organiza todas las habilidades por empleado y puede que sea difícil encontrar empleados con una habilidad específica en un nivel en particular, así que es necesario utilizar un filtro personalizado para encontrarlos.

Primero elimine cualquier filtro activo en la :guilabel:` barra de búsqueda` para ver solo a los empleados que tienen el nivel experto en la habilidad de Javascript.

Haga clic en el icono  (flecha hacia abajo) en la barra de búsqueda, luego haga clic en Agregar filtro personalizado en la sección de Filtros para abrir la ventana emergente correspondiente.

Con el menú desplegable seleccione Habilidad en el primer campo y seleccione Javascript para el tercero.

Después haga clic en el botón Nueva regla, aparecerá otra línea en la que deberá seleccionar el nivel de habilidad actual en el primer menú desplegable. También seleccione Experto en el tercer campo de menú desplegable.

Después de hacer clic en el botón Nueva regla, la palabra cualquiera de la frase Coincidir con cualquiera de las siguientes reglas: cambia de texto normal a un menú desplegable. Haga clic en el icono  (flecha hacia abajo) después de la palabra cualquiera y seleccione todas.

Por último haga clic en el botón Agregar. Solo aparecerán los empleados que tengan el nivel experto en la habilidad Javascript.

![La ventana emergente de filtro personalizado con los parámetros configurados para que solo aparezcan empleados con nivel experto en la habilidad JavaScript.](https://www.odoo.com/documentation/17.0/es/_images/javascript.png)

 Ver también

- [Fundamentos de los reportes de Odoo](https://www.odoo.com/documentation/17.0/es/applications/essentials/reporting.html)
    
- [Buscar, filtrar y agrupar registros](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html)