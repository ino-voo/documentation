Un cliente potencial de _calidad_ es un cliente potencial que tiene probabilidades de convertirse en una venta. Debe ajustarse a las características que más comúnmente se cree que ayudan a los vendedores a cerrar un trato, además de a criterios más precisos específicos de cada organización.

 Nota

Los criterios específicos para definir a un _lead de calidad_ cambian dependiendo de la organización. Para obtener más información, vea [Definir leads de calidad](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#track-links-define-a-lead).

Un _reporte_ de leads de calidad compara cuántos clientes potenciales de calidad ha recibido cada vendedor en un periodo de tiempo determinado, por ejemplo, en los últimos 30 días. Los jefes de ventas pueden utilizar este informe para tomar decisiones más informadas a la hora de asignar nuevos clientes potenciales a su equipo.

 Example

> Un gerente de ventas realiza un reporte de leads de calidad con los criterios específicos de su empresa:
> 
> - Los leads deben un número de teléfono y una dirección de correo.
>     
> - La dirección de correo debe tener un dominio profesional.
>     
> - La fuente del lead debe ser de una conversación de chat en vivo o una junta con una persona de ventas.
>     

Luego de elaborar el reporte, el gerente puede ver que, aunque la capacidad de cada colaborador para cerrar un trato ha variado, algunos miembros del equipo han recibido un mayor número de leads de calidad que otros.

> ![Un ejemplo de reporte de leads de calidad en la aplicación CRM de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/example-report.png)
> 
> Con esta información, el gerente de ventas puede decidir si asignar más leads de calidad a personas del equipo de ventas que estén en la parte de abajo, así se balanceará la distribución de leads de calidad.

## Crear un reporte de leads de calidad[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#create-a-quality-leads-report "Enlazar permanentemente con este título")

Para crear un reporte de leads de calidad, primero vaya a CRM ‣ Reportes ‣ Flujo para abrir el tablero Análisis de flujo. Haga clic en la barra de búsqueda ubicada en la parte superior de la página y elimine los filtros activos.

Haga clic en el icono 🔻(triángulo apuntando hacia abajo) situado a la derecha de la barra Buscar… para abrir el menú desplegable que contiene las columnas Filtros, Agrupar por y Favoritos. Haga clic en Añadir filtro personalizado, que abre una ventana emergente Añadir filtro personalizado.

La ventana emergente Agregar filtro personalizado permite crear filtros más específicos.

### Añadir filtros personalizados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#add-custom-filters "Enlazar permanentemente con este título")

Para poder generar un reporte de leads de calidad, debe crear filtros para seguir las siguientes condiciones:

- [Fecha de inicio](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#quality-leads-report-starting-date): limita los resultados a los creados dentro de un marco temporal específico.
    
- [Equipos de venta](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#quality-leads-report-sales-team): limita los resultados para que solo incluyan leads asignados a uno o más equipos de ventas. Este filtro es opcional y no debe incluirse si el reporte está destinado a toda la empresa.
    
- [Excluir leads sin asignar](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#quality-leads-report-unassigned-leads): excluye leads sin vendedor asignado.
    
- [Incluir leads archivados](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#quality-leads-report-archived-leads): asegura que tanto los leads activos como inactivos se incluyan en los resultados.
    
- [Agregar reglas para leads de calidad](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#quality-leads-report-add-quality-rules): incluye o excluye resultados según los criterios para el equipo de ventas de esa empresa en específico.
    

![Un ejemplo de una ventana emergente para el filtro personalizado con todas las reglas configuradas.](https://www.odoo.com/documentation/17.0/es/_images/configured-custom-rules.png)

Un ejemplo de una ventana emergente para el _filtro personalizado_ con todas las reglas predeterminadas configuradas.[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#id1 "Enlace permanente a esta imagen")

#### Agregar un filtro de fecha inicial[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#add-a-starting-date-filter "Enlazar permanentemente con este título")

Empiece por definir primero el parámetro de la regla con un intervalo de fechas, haciendo clic en el primer campo, a la izquierda de la fila, y escribiendo `Creado el` en la barra Buscar…, o desplazándose por la lista del menú para localizarlo.

En el menú desplegable de reglas de operador, defina aún más el parámetro seleccionando:

- >= (mayor que o igual a) para especificar una fecha de inicio e incluir todas las entradas _después_ de esa fecha de inicio (así como el propio valor inicial); o bien
    
- está entre para definir con mayor precisión un marco temporal con una fecha de inicio y fin. Todas las entradas que coincidan y que se ajusten a las fechas de inicio y fin definidas se incluirán en el reporte.
    

Con cualquiera de las opciones, use el calendario emergente para seleccionar un día y una hora en el campo de la derecha para definir el rango de fecha respectivo. Configurar estos valores es todo lo que tiene que hacer para crear la primera regla.

#### Agregar un filtro de equipo de ventas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#add-a-sales-team-filter "Enlazar permanentemente con este título")

 Nota

Este filtro es opcional, **no** lo agregue si desea visualizar los resultados de toda la empresa.

Para limitar los resultados del informe a uno o más equipos de ventas, haga clic en Nueva regla. A continuación, haga clic en el primer campo de la nueva regla y escriba «Equipo de ventas» en la barra Buscar… o desplácese por la lista para localizarlo.

En el segundo campo de la regla, seleccione está en en el menú desplegable. La selección de este operador limita los resultados a los equipos de ventas seleccionados en el campo siguiente.

Finalmente, en el tercer campo, seleccione el equipo de ventas deseado del menú desplegable. Puede agregar varios equipos de venta en este campo, donde cada parámetro se trata con un operado «or» (por ejemplo, «any») en la lógica de búsqueda.

#### Excluir leads no asignados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#exclude-unassigned-leads "Enlazar permanentemente con este título")

Después agregue una nueva regla. Haga clic en el primer campo de la nueva regla y escriba `Vendedor` en la barra de búsqueda o búsquelo en la lista.

En el segundo campo de la regla, seleccione está establecido desde el menú desplegable. Seleccionar este operador excluye todos los leads no asignados a una persona de ventas específica.

#### Incluir leads archivados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#include-archived-leads "Enlazar permanentemente con este título")

 Truco

Este filtro también es opcional. Agrega leads archivados (inactivos) al reporte, pero le recomendamos que lo incluya porque obtiene _todos_ los leads asignados y los coloca en el reporte sin importar su estado. Esto garantiza que la representación de los leads asignados más acertada. **No** active esta función si quiere generar un reporte que solo incluya leads activos.

Después, en la esquina superior derecha de la ventana emergente Agregar filtro personalizado, presione el botón Incluir archivados para activar la selección correspondiente.

![La ventana emergente para agregar un filtro personalizado. El botón "Incluir archivados" aparece destacado.](https://www.odoo.com/documentation/17.0/es/_images/include-archived.png)

Habilitar esta función agrega leads archivados (es decir, inactivos) al reporte.

#### Agregar reglas para leads de calidad[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#add-rules-for-quality-leads "Enlazar permanentemente con este título")

Los filtros agregados en este paso varían según cómo una organización define un _filtro de calidad_.

##### Definir un filtro de calidad[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#define-a-quality-lead "Enlazar permanentemente con este título")

Como se definió antes, un _lead de calidad_ es un lead que es muy probable que resulte en una oportunidad ganada. Aunque los criterios para un lead de calidad varían dependiendo de la organización, comúnmente son una combinación de factures que se atribuyen a los resultados de ventas positivos, además de los factores importantes para cada organización.

Además de los filtros básicos y opciones de agrupación mostrados en el [Reporte de la hoja de trabajo de calidad](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#track-links-create-quality-leads-report), considere los siguientes filtros al definir un lead de calidad:

- Correo electrónico o Teléfono: la información en estos campos le puede ayudar a determinar si un lead es un contacto profesional.
    
- Fuente: este campo junta los esfuerzos de marketing y generación de leads de todas las aplicaciones de Odoo, incluyendo _Chat en vivo_, _Marketing social_ y _Marketing por correo electrónico_.
    
- Etapa: este filtro se puede usar para eliminar o abordar leads que estén en una etapa específica.
    
- Medio: la fuente de un lead puede indicar su nivel de calidad, ya que varios canales tienen diferentes tasas de ganados y ganancias esperadas.
    
- Campaña: agregar este filtro le ayuda a rastrear el éxito de diferentes campañas de marketing que buscan obtener leads de mayor calidad.
    
- Motivo de pérdida: excluir los leads que pueden parecer de calidad según varios criterios, pero que se marcaron como _perdidos_ por razones específicas.
    
- Etiquetas: incluir o excluir resultados según una o más etiquetas personalizadas.
    

 Truco

Al agregar reglas a un filtro personalizado, tenga en cuenta las afirmaciones que preceden a cada regla. Las afirmaciones arriba de las reglas determinan si un resultado de búsqueda coincide con **todas** las listas debajo de la afirmación, o con **cualquiera** de las reglas debajo de la afirmación.

![Imagen de las opciones de coincidence de reglas en una ventana emergente para agregar un filtro personalizado.](https://www.odoo.com/documentation/17.0/es/_images/match-all-match-any.png)

## Ver el reporte[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/quality_leads_report.html#view-the-report "Enlazar permanentemente con este título")

 Importante

En la parte superior del formulario Agregar filtro personalizado hay una opción para que coincida con cualquiera de las reglas o con todas ellas. Para ejecutar el reporte de forma correcta solo debe incluir los registros que coincidan con **todos** los siguientes filtros. Antes de agregar los filtros asegúrese de que la opción Todos está seleccionada en este campo.

![Imagen de la opción para coincidir todas las reglas en la ventana emergente para agregar un filtro personalizado.](https://www.odoo.com/documentation/17.0/es/_images/match-all-rules.png)

Después de que se configuren los filtros, haga clic en Agregar. El método de visualización predeterminado para el reporte es el gráfico de barras, donde los leads se agrupan por _etapa_.

Para agrupar los resultados por vendedor, haga clic en el icono 🔻(triángulo apuntando hacia abajo) ubicado del lado derecho de la barra de búsqueda para abrir el mega menú desplegable. Abajo del encabezado Agrupar por seleccione un Vendedor. En la misma columna, abajo de Agrupar por, haga clic en Agregar grupo personalizado y después seleccione Activo en el menú desplegable para agregar el _estado_ al grupo principal de Vendedor.

El reporte ahora muestra el conteo total de _leads de calidad_ que cada vendedor ha recibido en el periodo designado. Como hay varios filtros de Agrupar por , los leads agrupados también tienen un código de color para identificar si están _activos_ o si se _marcaron como perdidos_.

 Truco

Para guardar esta búsqueda para después, haga clic en el icono de 🔻(triángulo apuntando hacia abajo) que se encuentra a un lado de la barra Buscar… para abrir el menú desplegable. En el encabezado de Favoritos haga clic en Guardar búsqueda actual.

En el menú desplegable, cambie el nombre del reporte de `Flujo` a `Leads de calidad` y después haga clic en Guardar.