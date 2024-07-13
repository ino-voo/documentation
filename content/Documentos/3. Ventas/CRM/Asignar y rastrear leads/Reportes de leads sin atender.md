_Los leads sin atender_ son leads que tienen actividades programadas que se deben hacer pronto o que ya no se hicieron a tiempo. Siempre que se programe una actividad, Odoo rastrea la fecha final y envía correos de recordatorios a los usuarios a los que se les asignó la actividad.

Un _reporte de leads sin atender_ junta todos los leads activos en el flujo que tienen actividades que se deben hacer pronto o que ya no se hicieron a tiempo, lo cual permite que el gerente de ventas identifique cuáles oportunidades requieren atención inmediata.

Al realizar un reporte de leads sin atender cada día, los gerentes de ventas pueden recordarle a sus equipos que tienen que realizar sus actividades pendientes antes de que pase la fecha límite. De esta forma evitará que se olviden leads y fomentará una actitud proactiva de parte de sus vendedores.

 Example

> Un gerente de ventas empieza el día viendo el reporte de leads sin atender y verá lo siguiente al cambiar a la vista de lista:
> 
> ![Vista de lista de un reporte de Leads sin atender con las actividades resaltadas.](https://www.odoo.com/documentation/17.0/es/_images/unattended-leads-example.png)

Mitchell, uno de los miembros del equipo, tiene dos leads en la etapa _propuesta_ y debe hacer algunas actividades.

El icono amarillo 📞 (teléfono) indica que el lead `Espacio abierto moderno` tiene una actividad de llamada programada para hoy. El icono rojo ✉️ (sobre) indica que el lead `5 VP Chairs` (5 sillas) tiene una actividad de correo electrónico programada que ya venció.

El gerente hace clic en el lead `5 VP Chairs` (5 sillas) para ver el registro del lead y ver el chatter. Pueden ver que un correo electrónico se programó para enviarse hace 2 días, pero Mitchell nunca marcó la actividad como hecha.

![Ejemplo de una notificación de actividad retrasada en el chatter de un lead.](https://www.odoo.com/documentation/17.0/es/_images/overdue-activities-email.png)

 Importante

Para poder generar un reporte de leads sin atender, el equipo de ventas **debe** utilizar la actividad en el flujo de _CRM_ de forma regular, en tarjetas de leads y oportunidades diferentes.

**No** es posible recopilar un reporte completo si las personas de ventas no están utilizando la función _Actividades_ en el _chatter_

Para más información consulte [Actividades](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html)

## Crear un reporte de leads sin atender[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#create-an-unattended-leads-report "Enlazar permanentemente con este título")

Para crear un reporte de leads sin atender, vaya primero a la aplicación CRM ‣ Reportes ‣ Flujo para abrir el tablero Análisis de flujo. Haga clic en la barra Búsqueda… en la parte superior de la página para eliminar todos los filtros predeterminados.

 Nota

El filtro Creado el puede mantenerse activo, ya que puede ser util incluir esta variante en el reporte.

Para agregar filtros personalizados haga clic en el icono 🔻(triángulo apuntando hacia abajo) ubicado a la derecha de la barra de búsqueda, esta acción abrirá el menú desplegable que incluye las columnas :guilabel:`Filtros, Agrupar por y Favoritos. En la columna Filtros, haga clic en Agregar filtro personalizado para abrir la ventana emergente Agregar filtro personalizado.

La ventana emergente Agregar filtro personalizado permite crear filtros más específicos.

### Añadir filtros personalizados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#add-custom-filters "Enlazar permanentemente con este título")

Para poder generar un reporte de leads sin atender, debe crear filtros para seguir las siguientes condiciones:

> - [Actividades pasadas por realizar](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#unattended-leads-report-past-due): limita los resultados para que solo incluya leads que tengan actividades asignadas de las que ya pasó la fecha límite. Esto se puede modificar para incluir actividades faltantes que deban ocurrir en la fecha en la que el reporte también se genera.
>     
> - [Leads no asignados](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#unattended-leads-report-exclude-unassigned): excluye leads que no se le han asignado a una persona del equipo de ventas.
>     
> - [Equipos de venta específicos](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#unattended-leads-report-sales-team): limita los resultados para que solo incluyan leads asignados a uno o más equipos de ventas. Este filtro es opcional, no lo incluya si el reporte está dirigido a toda la empresa.
>     

#### Agregar un filtro para actividades pendientes pasadas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#add-filter-for-past-due-activities "Enlazar permanentemente con este título")

Haga clic en el primer campo para la nueva regla y escriba `Actividades` en la barra Buscar… o deslícese hacia abajo para buscar por la lista. Después, a un lado de Actividades haga clic en > (signo de mayor que) para abrir un menú desplegable con condiciones secundarias.

Escriba `Fecha de vencimiento` en la barra Buscar… o deslícese hacia abajo para buscar por la lista. Haga clic en Fecha de vencimiento para agregarla a la regla.

> ![Filtro emergente personalizado en el que se resalta las opciones para actividades y fecha de vencimiento.](https://www.odoo.com/documentation/17.0/es/_images/activities-due.png)

Después, haga clic en el siguiente campo y seleccione <= del menú desplegable. Seleccione este operador para incluir todas las actividades con una fecha de vencimiento, incluyendo y hasta la fecha que se seleccione en el siguiente campo.

En el tercer campo se puede dejar la fecha de hoy o se puede ajustar como se necesite.

#### Excluir leads no asignados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#exclude-unassigned-leads "Enlazar permanentemente con este título")

Después de filtrar por actividades, agregue una Nueva regla. Haga clic en el primer campo de la nueva regla y escriba `Vendedor` en la barra Buscar… o deslícese por la lista para encontrarlo.

En el segundo campo de la regla, seleccione está establecido desde el menú desplegable. Seleccionar este operador excluye todos los leads no asignados a una persona de ventas específica.

#### Agregar un equipo de ventas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#add-a-sales-team "Enlazar permanentemente con este título")

 Nota

Este filtro es opcional. Para ver los resultados de toda la empresa, **no** añada este filtro y continúe en [Ver resultados](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#unattended-leads-report-view-results).

Para limitar los resultados del informe a uno o más equipos de ventas, haga clic en Nueva regla. A continuación, haga clic en el primer campo de la nueva regla y escriba «Equipo de ventas» en la barra Buscar… o desplácese por la lista para localizarlo.

En el segundo campo de la regla, seleccione está en en el menú desplegable. La selección de este operador limita los resultados a los equipos de ventas seleccionados en el campo siguiente.

Finalmente, en el tercer campo, seleccione el equipo de ventas deseado del menú desplegable. Puede agregar varios equipos de venta en este campo, donde cada parámetro se trata con un operado «or» (por ejemplo, «any») en la lógica de búsqueda.

![Un ejemplo de una ventana emergente para el filtro personalizado con todas las reglas configuradas.](https://www.odoo.com/documentation/17.0/es/_images/configured-custom-rules1.png)

Un ejemplo de una ventana emergente para **agregar un filtro personalizado** con todas las reglas configuradas.[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#id1 "Enlace permanente a esta imagen")

## Ver resultados[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#view-results "Enlazar permanentemente con este título")

En la parte superior del formulario Agregar filtro personalizado hay una opción para que coincida con cualquiera de las reglas o con todas ellas. Para ejecutar el reporte de forma correcta solo debe incluir los registros que coincidan con **todos** los siguientes filtros. Antes de agregar los filtros asegúrese de que la opción Todos está seleccionada en este campo.

![Ejemplo de una notificación de actividad retrasada en el chatter de un lead.](https://www.odoo.com/documentation/17.0/es/_images/all-custom-filter.png)

Después de que se configuren todos los filtros, haga clic en Agregar. El reporte resultante mostrará todos los leads asignados a una persona de ventas donde una actividad ya venció, o vencerá en la fecha de hoy. El modo de visualización predeterminado es un gráfico de barras, donde los leads se agrupan por _etapa_.

Para agrupar los resultados por vendedor, haga clic en el icono 🔻(triángulo apuntando hacia abajo) situado a la derecha de la barra Buscar… para abrir el menú desplegable que contiene las columnas Filtros, Agrupar por y Favoritos. En el encabezado Agrupar por seleccione una persona de ventas.

 Nota

La opción para agrupar por Equipos de ventas también está disponible en el encabezado Agrupar por.

Para cambiar a una vista de _lista_, haga clic en el icono ≣ (lista) en la esquina superior derecha de la pantalla.

 Truco

> Al hacer clic en el icono (toggle) se abrirá un menú desplegable de columnas adicionales que se pueden agregar al reporte.
> 
> Algunas de las opciones que pueden beneficiar al reporte incluyen:
> 
> - Actividades: el resumen de las actividades más recientes para este lead.
>     
> - Cierre esperado: la fecha estimada en la que se ganará el lead.
>     
> - Probabilidad: tasa estimada de éxito según la etapa.
>     

![Filtro emergente personalizado en el que se resalta las opciones para actividades y fecha de vencimiento.](https://www.odoo.com/documentation/17.0/es/_images/additional-options.png)

 Ver también

[Actividades](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html)

 [Edit on GitHub](https://github.com/odoo/documentation/edit/17.0/content/applications/sales/crm/track_leads/unattended_leads_report.rst)

##### EN ESTA PÁGINA

- - [Crear un reporte de leads sin atender](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#create-an-unattended-leads-report)
        
    - [Ver resultados](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/unattended_leads_report.html#view-results)