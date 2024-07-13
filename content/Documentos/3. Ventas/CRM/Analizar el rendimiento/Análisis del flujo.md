La aplicación _CRM_ gestiona el proceso de ventas a medida que los clientes potenciales/oportunidades avanzan de etapa en etapa, desde el origen hasta la venta (**ganada**) o el archivo (**perdida**).

Después de organizar el flujo de trabajo, utilice las opciones de búsqueda y reportes disponibles en la página _análisis del flujo de ventas_ para obtener información sobre la eficacia del flujo de trabajo y sus usuarios.

Si desea acceder a la página _análisis del flujo de trabajo_, vaya a la aplicación CRM ‣ Reportes ‣ Flujo de trabajo.

![Abra la aplicación CRM y haga clic en la pestaña de reportes en la parte superior, luego haga clic en 'flujos de trabajo'.](https://www.odoo.com/documentation/17.0/es/_images/reporting-tab-and-pipeline-view.png)

## Cómo navegar la página de análisis del flujo de trabajo[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#navigate-the-pipeline-analysis-page "Enlazar permanentemente con este título")

Cuando acceda a la página análisis del flujo de ventas, se generará automáticamente un gráfico de barras que muestra los clientes potenciales del año pasado. Las barras representan la cantidad de clientes potenciales en cada etapa del proceso de ventas, organizadas por colores para mostrar el mes en que el cliente potencial alcanzó esa etapa.

![El estado predeterminado de la página de análisis del flujo de ventas es un gráfico, con muchas opciones para modificarlo.](https://www.odoo.com/documentation/17.0/es/_images/pipeline-analysis-page.png)

Los elementos interactivos de la página análisis del flujo de trabajo modifican el gráfico para reportar diferentes métricas en varias vistas. De izquierda a derecha, de arriba a abajo, los elementos incluyen:

- Acciones: representadas por el icono ⚙️ (engranaje), ubicado junto al título de la página análisis del flujo de ventas. Al hacer clic, aparecerá un menú desplegable con tres opciones, cada una con su propio submenú: conocimiento, tablero, hoja de cálculo. (Consulte [guardar y compartir reportes](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#win-loss-save-reports) para obtener más información)
    
    - La opción información sirve para vincular o insertar el gráfico en un artículo de la aplicación _Información_.
        
    - La opción tablero sirve para agregar el gráfico a un tablero en la aplicación _Tablero_.
        
    - La opción hoja de cálculo sirve para vincular el gráfico a una hoja de cálculo en la aplicación _Documentos_.
        
- Barra buscar…: muestra los filtros y agrupaciones que se aplican actualmente al gráfico. Si desea agregar nuevos filtros/grupos, escríbalos en la barra de búsqueda o haga clic en el icono ⬇️ (flecha hacia abajo), al final de la barra, para abrir un menú desplegable de opciones. (Consulte [opciones de búsqueda](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#win-loss-search) para obtener más información).
    

En la esquina superior derecha verá opciones de vista representadas por diferentes iconos. (Consulte [opciones de vista](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#win-loss-view) para más información).

- Vista de gráfico: muestra los datos en un gráfico de barras. Esta es la vista predeterminada.
    
- Vista Pivot: muestra los datos en una tabla de métricas personalizable y con categorías.
    
- Vista cohorte: muestra y organiza datos según la semana (predeterminado), día, mes o año de creado en y fecha de cierre.
    
- Vista de lista: muestra los datos en una lista.
    

En el lado izquierdo de la página, debajo del título de la página análisis del flujo de trabajo verá más opciones de filtros y vistas configurables.

- Medidas: abre un menú desplegable con diferentes opciones de medidas que puede visualizar en una gráfica, una tabla dinámica o en vista cohorte. El menú desplegable de medidas no está disponible para la vista de lista. (Consulte la página sobre [opciones de medidas](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#win-loss-measure) para obtener más información)
    
- Insertar en hoja de cálculo: abre una ventana emergente con opciones para abrir un gráfico o una tabla dinámica en una hoja de cálculo en la aplicación _Documentos_. Esta opción no está disponible para la vista cohorte o de lista.
    

Si selecciona la vista de gráfico, tendrá disponibles las siguientes opciones:

- Gráfico de barras: cambia el gráfico por un gráfico de barras.
    
- Gráfico de línea: cambia el gráfico por un gráfico de línea.
    
- Gráfico circular: cambia el gráfico por un gráfico circular.
    
- Apilado: al seleccionar esta opción, los resultados de cada etapa del gráfico se apilan uno encima del otro. Si no lo selecciona, los resultados de cada etapa se muestran como barras individuales.
    
- Descendiente: reordena las etapas del gráfico de manera descendiente de izquierda a derecha. Haga clic en el icono una segunda vez para quitar la opción. Es posible que esta opción no esté disponible dependiendo de sus criterios de búsqueda.
    
- Ascendiente: reordena las etapas del gráfico de manera ascendiente de izquierda a derecha. Haga clic en el icono una segunda vez para quitar la opción. Es posible que esta opción no esté disponible dependiendo de sus criterios de búsqueda.
    

Si selecciona la vista de tabla dinámica, tendrá disponibles las siguientes opciones:

- Girar eje: gira los ejes X e Y de toda la tabla.
    
- Expandir todo: al seleccionar agrupaciones adicionales con el icono ➕ (signo de más), este botón abre dichos grupos debajo de cada fila.
    
- Descargar xlsx: descarga la tabla como un archivo de Excel.
    

### Opciones de búsqueda[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#search-options "Enlazar permanentemente con este título")

La página del guilabel:`análisis de flujo` se puede personalizar con varias opciones de filtros y de agrupaciones.

Para añadir nuevos criterios de búsqueda, escriba lo que desee en la barra de búsqueda, o haga clic en el icono ⬇️ (flecha hacia abajo) que se encuentra junto a la barra de búsqueda, para abrir un menú desplegable con todas las opciones. Consulte las secciones de abajo para obtener más información acerca de lo que hace cada opción.

![Al hacer clic en la flecha hacia abajo que se encuentra junto a la barra de búsqueda, se abrirá un menú de filtros para el análisis.](https://www.odoo.com/documentation/17.0/es/_images/search-panel-filters-and-group-by-options.png)

FiltersGroup ByComparisonFavorites

La sección de filtros le permite a los usuarios agregar filtros ya existentes o personalizados para buscar sus criterios. Puede agregar varios filtros a una sola búsqueda.

- Mi flujo de ventas: muestra los leads asignados al usuario actual.
    
- Oportunidades: muestra los leads calificados como oportunidades.
    
- Leads: muestra los leads que están por calificarse como oportunidades.
    
- Activo: muestra los leads activos.
    
- Inactivos: muestra los leads inactivos.
    
- Ganado: muestra los leads marcados como **ganados**.
    
- Perdido: muestra los leads marcados como **perdidos**.
    
- Creado el: muestra los leads que se crearon durante un periodo específico de tiempo. De manera predeterminada, el rango es el año pasado, pero se puede ajustar como lo desee, o bien, puede quitarlo por completo.
    
- Cierre esperado: muestra los leads para los que se espera un cierre (que se marquen como **ganados**) durante un periodo específico de tiempo.
    
- Fecha de cierre: muestra los leads que se cerraron (marcados como **ganados**) durante un periodo específico de tiempo.
    
- Archivado: muestra los leads que se han archivado (marcados como **perdidos**).
    
- Agregar filtro personalizado: le permite al usuario crear un filtro personalizado con varias opciones. (Consulte la página de [agregar filtros y grupos personalizados](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#win-loss-custom-filters) para obtener más información)
    

#### Agregar filtros y grupos personalizados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#add-custom-filters-and-groups "Enlazar permanentemente con este título")

Además de las opciones ya existentes en la barra de búsqueda, la página de análisis de flujo también puede utilizar filtros y grupos personalizados.

Los filtros personalizados con reglas complejas que personalizan aún más los resultados de la búsqueda, mientras que los grupos personalizados muestran la información de manera más organizada.

**Para agregar un filtro personalizado:**

1. En la página de análisis de flujo, haga clic en el icono de la flecha hacia abajo que se encuentra junto a la barra de Buscar….
    
2. En el menú desplegable, haga clic en Agregar filtro personalizado.
    
3. Aparecerá la ventana emergente para agregar un filtro personalizado con una regla predeterminada (El país está en _____) compuesto de tres campos únicos. Puede editar estos campos para crear la regla personalizada, y puede agregar varias reglas a un solo filtro personalizado.
    
4. Para editar una regla, haga clic en el primer campo (País) y seleccione una opción del menú desplegable. El primer campo determina el contenido primario del la regla.
    
5. Luego, haga clic en el segundo campo y seleccione una opción del menú desplegable. El segundo campo determina la relación entre el primer y tercer campo, y generalmente **es** o **no es** una afirmación, aunque también pueden ser enunciados de **es más o menos que**, y más.
    
6. Finalmente, haga clic en el tercer campo y seleccione una opción del menú desplegable. El tercer campo determina el contenido secundario de la regla.
    
7. La regla estará completa un vez que estén seleccionados los tres campos.
    
    - **Para agregar más reglas:** haga clic en Nueva regla y repita los reglas 4-7, según lo necesite.
        
    - **Para eliminar una regla:** haga clic en el icono de 🗑️ (papelera) del lado derecho de la regla.
        
    - **Para duplicar una regla existente:** haga clic en el icono ➕ (signo de más) del lado derecho de la regla.
        
    - **Para crear reglas más complejas:** haga clic en el icono de agregar rama del lado derecho de la regla. Esto agrega otro modificador debajo de la regla para agregar un enunciado «todo de» o «cualquiera de».
        

![La función de agregar rama le permite crear enunciados más complejos de todo de o cualquiera de para las reglas.](https://www.odoo.com/documentation/17.0/es/_images/custom-filter-add-branch.png)

8. Una vez que agregó todas las reglas, haga clic en Agregar para agregar el filtro personalizado para los criterios de búsqueda.
    
    - **Para eliminar un filtro personalizado:** haga clic en el icono de ✖️ (x) junto al filtro en la barra de búsqueda.
        

**Para agregar un grupo personalizado:**

1. En la página de análisis de flujo, haga clic en el icono de la flecha hacia abajo que se encuentra en la barra de búsqueda.
    
2. En el menú desplegable que aparece, haga clic en Agregar un grupo personalizado.
    
3. Busque entre las opciones del menú y seleccione uno o más grupos.
    
    - **Para eliminar un grupo personalizado:** haga clic en el icono ✖️ (x) que se encuentra en el grupo personalizado en la barra de búsqueda.
        

### Opciones de medidas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#measurement-options "Enlazar permanentemente con este título")

De manera predeterminada, la página de análisis de flujo mide el número total de leads que coincidan con los criterios de búsqueda, pero los puede cambiar para medir otros elementos de su interés.

Para cambiar la medida seleccionada, haga clic en el botón de Medidas que se encuentra en la parte superior izquierda de la página y seleccione una de las siguientes opciones del menú desplegable:

- Días por asignar: mide el número de días que tardó un lead en ser asignado después de su creación.
    
- Días para el cierre: mide el número de días que tardó el lead en cerrarse (que marcará como **ganado**).
    
- Días para convertir: mide el número de días que tardó un lead en convertirse en oportunidad.
    
- Días de cierre excedidos: mide el número de días que excede un lead de su fecha de cierre esperada.
    
- MRR esperado: mide el ingreso mensual recurrente esperado de un lead.
    
- Ingreso esperado: mide el ingreso esperado de un lead.
    
- MRR prorrateado: mide el ingreso mensual recurrente prorrateado de un lead.
    
- Ingresos recurrentes prorrateados: mide los ingresos recurrentes prorrateados de un lead.
    
- Ingreso prorrateado: mide el ingreso prorrateado de un lead.
    
- Ingresos recurrentes: mide el ingreso recurrente de un lead.
    
- Número total: mide el número total de leads que coinciden con los criterios de búsqueda.
    

### Ver opciones[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#view-options "Enlazar permanentemente con este título")

Después de configurar los filtros, los grupos y las medidas, la página de análisis de flujo puede mostrar los datos de muchas maneras. La página usa la vista de gráfico de forma predeterminada, pero puede usar la vista de tabla dinámica, de cohorte o de lista.

Para cambiar la vista del flujo, haga clic en uno de los cuatro iconos que se ubican en la parte superior derecha de la página de análisis de flujo.

Graph ViewPivot ViewCohort ViewList View

La vista de gráfico está seleccionada de manera predeterminada en la página de análisis de flujo. Muestra el análisis ya sea en un gráfico de barras de línea o circular.

Esta opción de vista es útil para tener una visualización rápida y comparar relaciones simples, como el número total de leads en cada etapa, o los leads asignados a cada vendedor.

De manera predeterminada, el gráfico mide el número total de leads en cada grupo, pero puede cambiarlo si hace clic en el botón Medidas y [selecciona otra opción](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#win-loss-measure) del menú desplegable que aparece.

![La vista de gráfico muestra el análisis como un gráfico de barras, de línea o circular.](https://www.odoo.com/documentation/17.0/es/_images/graph-view.png)

 Truco

Le recomendamos que desactive la opción Apilado al utilizar un gráfico de barras en esta vista para hacer que el desglose de los resultados sea más legible.

## Crear reportes[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#create-reports "Enlazar permanentemente con este título")

Después de comprender cómo [navegar por la página de análisis del flujo](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#win-loss-pipeline) puede utilizarla para crear y compartir diferentes reportes. Puede crear casi cualquier combinación posible gracias a las opciones predefinidas, los filtros y los agrupamientos personalizados.

Una vez que haya creado los reportes, puede [guardarlos como favoritos, compartirlos con otros usuarios o agregarlos a tableros y hojas de cálculo](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#win-loss-save-reports).

A continuación detallamos algunos reportes comunes que puede crear en la página de análisis del flujo.

### Reporte de perdidos y ganados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#win-loss-win-loss "Enlazar permanentemente con este título")

El cálculo de ganados y perdidos corresponde al cálculo de los leads activos o que solían estar activos en un flujo y que se marcaron como **ganados** o **perdidos** en un período específico de tiempo. Al calcular las oportunidades ganadas sobre las perdidas, los equipos pueden especificar los indicadores clave de rendimiento (KPI) que convierten leads en ventas, por ejemplo, los equipos o miembros específicos del equipo, determinados medios o campañas de marketing, entre otros.

ó𝑅𝑎𝑧ó𝑛 𝑑𝑒 𝑝𝑒𝑟𝑑𝑖𝑑𝑜𝑠 𝑦 𝑔𝑎𝑛𝑎𝑑𝑜𝑠=𝑂𝑝𝑜𝑟𝑡𝑢𝑛𝑖𝑑𝑎𝑑𝑒𝑠 𝑔𝑎𝑛𝑎𝑑𝑎𝑠𝑂𝑝𝑜𝑟𝑡𝑢𝑛𝑖𝑑𝑎𝑑𝑒𝑠 𝑝𝑒𝑟𝑑𝑖𝑑𝑎𝑠

El reporte de ganados y perdidos filtra los leads del año pasado, sin importar si fueron ganados o perdidos, y agrupa los resultados por su etapa en el flujo. Para poder crear este reporte necesita un filtro personalizado y agrupar los resultados por Etapa.

![Los criterios de búsqueda para los reportes de ganados y perdidos son "Creado el", "Etapa" y "Activo es verdadero y falso".](https://www.odoo.com/documentation/17.0/es/_images/search-criteria-for-basic-win-loss.png)

Siga los pasos que se describen a continuación para crear un reporte de ganados y perdidos:

1. Vaya a la aplicación CRM ‣ Reportes ‣ Flujo.
    
2. En la página de análisis de flujo, haga clic en el icono ⬇️ (flecha hacia abajo) que está ubicado junto a la barra de búsqueda para abrir un menú desplegable de filtros y grupos.
    
    ![El menú de búsqueda que contiene los filtros para un reporte básico de ganados y perdidos.](https://www.odoo.com/documentation/17.0/es/_images/filters-for-basic-win-loss-report.png)
    
3. Haga clic en Etapa en el menú desplegable de la sección Agrupar por.
    
4. Vaya a la sección Filtros y haga clic en Agregar filtro personalizado para abrir otro menú emergente.
    
5. En el menú emergente Agregar filtro personalizado, haga clic en el primer campo de la sección Conciliar cualquiera de las siguientes reglas:. Este campo muestra País de forma predeterminada.
    
6. Al hacer clic en ese primer campo abrirá un submenú que le permitirá elegir alguna de las opciones disponibles. Busque y seleccione la opción Activo, después de esto los campos restantes se completarán en automático.
    
    El primer campo dice Activo, el segundo campo dice es y, por último, el tercer campo dice establecido.
    
    La regla completa dice: Activo es establecido.
    
7. Haga clic en Nueva regla, cambie el primer campo a Activo y el último a no establecido. La regla completa dice Activo no es establecido.
    
8. Haga clic en Agregar.
    

![El menú Agregar filtro personalizado muestra dos reglas: (1) Activo es establecido y (2) Activo no es establecido.](https://www.odoo.com/documentation/17.0/es/_images/add-custom-active-filter.png)

El reporte ahora muestra el total de leads, tanto «ganados» como «perdidos», agrupados por su etapa en el flujo del CRM. Pase el cursor sobre una sección del reporte para visualizar el número de prospectos en esa etapa.

![Un reporte básico de ganados y perdidos que muestra todos los leads agrupados por etapa, sin importar si fueron ganados o perdidos.](https://www.odoo.com/documentation/17.0/es/_images/basic-win-loss-report.png)

#### Personalizar los reportes de ganados y perdidos[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#customize-win-loss-reports "Enlazar permanentemente con este título")

Después de [crear un reporte de ganados y perdidos](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#win-loss-win-loss) puede utilizar las siguientes opciones para personalizar el reporte según lo que necesite.

 Example

Un gerente de ventas podría agrupar los leads ganados y perdidos por vendedor o equipo de ventas para ver quién tiene la mejor tasa de conversión. Un equipo de marketing podría agrupar por fuentes o medios para saber dónde ha sido más exitosa su publicidad.

Filters and groupsPivot ViewList View

Para agregar más filtros y grupos haga clic en el icono ⬇️ (flecha hacia abajo) que está ubicado junto a la barra de búsqueda. Seleccione una o más opciones del menú desplegable.

Estas son algunas de las opciones más útiles:

- Creado en: si ajusta este filtro a un periodo distinto, por ejemplo, los últimos 30 días o el último trimestre, puede proporcionar resultados más recientes.
    
- Agregar filtro personalizado: si hace clic en esta opción y navega por las diversas opciones en el menú desplegable podrá abrir criterios de búsqueda adicionales, por ejemplo, la última actualización de la etapa o el motivo de pérdida.
    
- Agregar grupo personalizado > Activo: al hacer clic en Agregar grupo personalizado ‣ Activo los resultados se dividen en **ganados** (verdadero) o **perdidos** (falso). Esto muestra en qué etapa marcan los leads como **ganados** o **perdidos**.
    
- Varios grupos: puede seleccionar Agrupar por varias veces para dividir los resultados en fragmentos más relevantes y gestionables.
    
    - Si agrega Vendedor o Equipo de ventas dividirá el número total de leads en cada Etapa.
        
    - Si agrega Medio o Fuente puede saber qué herramientas de marketing generan más ventas.
        

![El menú de búsqueda abierto y con los filtros de ganados y perdidos resaltados.](https://www.odoo.com/documentation/17.0/es/_images/search-panel-filters-and-group-by-options.png)

## Guardar y compartir reportes[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#save-and-share-reports "Enlazar permanentemente con este título")

Después de [crear un reporte](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html#win-loss-reports), los criterios de búsqueda se pueden guardar, así el reporte no se necesita crear de nuevo en el futuro. Los resultados de las búsquedas guardadas se actualizan cada vez que se abre el reporte.

Además, los reportes se pueden compartir con otros, o se pueden agregar a las hojas de cálculo o tableros para personalizarlos más y con mayor facilidad.

Save to FavoritesAdd to a SpreadsheetAdd to a Dashboard

Para guardar un reporte para más tarde:

1. En la página de análisis de flujo, haga clic en el icono ⬇️ (flecha hacia abajo) que está ubicado junto a la barra de búsqueda.
    
2. En el menú desplegable que aparece bajo el encabezado Favoritos , haga clic en Guardar búsqueda actual.
    
3. En el siguiente menú desplegable que aparece ingrese el nombre del reporte.
    
    - Si marca la caja Filtro predeterminado este reporte será el análisis predeterminado al acceder a la página Análisis del flujo.
        
    - Si marca la caja Compartido otros usuarios podrán acceder a este reporte.
        
4. Finalmente, haga clic en Guardar para que el reporte se guarde en el encabezado Favoritos
    

![En el encabezado Favoritos, haga clic en Guardar la búsqueda actual y guarde el reporte para más tarde.](https://www.odoo.com/documentation/17.0/es/_images/save-to-favorites.png)

 Ver también

- [Convertir leads en oportunidades](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/convert.html)
    
- [Crear y enviar cotizaciones](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/send_quotes.html)
    
- [Gestión de oportunidades perdidas](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html)