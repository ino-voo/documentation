Los _leads_ son un paso adicional de calificación antes de que se cree la oportunidad. Esto permite que se cuente con más tiempo para revisar el potencial y evaluar la viabilidad antes de asignarle la oportunidad a un vendedor.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/convert.html#configuration "Enlazar permanentemente con este título")

Para activar la función de _leads_, vaya a aplicación CRM ‣ Configuración ‣ Ajustes, seleccione la casilla con el nombre Leads y luego haga clic en Guardar.

![Ajustes de leads en la página de configuración de CRM.](https://www.odoo.com/documentation/17.0/es/_images/convert-leads-leads-setting.png)

Al activar esta función aparece una nueva opción en el menú, Leads, en la barra ubicada en la parte superior de la pantalla.

![Menú de leads en la aplicación CRM.](https://www.odoo.com/documentation/17.0/es/_images/convert-leads-leads-menu.png)

Una vez habilitó la función de _leads_, esta se aplica de forma predeterminada a todos los equipos de ventas. Para desactivar los leads en un equipo específico, vaya a la aplicación CRM ‣ Configuración ‣ Equipos de ventas. Seleccione un equipo de la lista para abrir su ágina de configuración, desmarque la casilla Leads ubicada abajo del campo Equipo de ventas y luego haga clic en Guardar.

![Menú de leads en la aplicación CRM.](https://www.odoo.com/documentation/17.0/es/_images/convert-leads-leads-button.png)

## Convierta un lead en una oportunidad[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/convert.html#convert-a-lead-into-an-opportunity "Enlazar permanentemente con este título")

Para convertir un lead en una oportunidad, vaya a la aplicación CRM ‣ Leads y haga clic en un lead de la lista para abrirlo.

 Advertencia

Si aparece un botón inteligente de Leads similares en la parte superior de la página del lead quiere decir que hay un lead o una oportunidad similar existente en la base de datos. Antes de convertir este lead, haga clic en el botón inteligente para verificar si lo mejor sería fusionar los leads.

![Imagen de un lead con el botón inteligente Leads similares resaltado.](https://www.odoo.com/documentation/17.0/es/_images/similar-leads-smart-button.png)

Haga clic en el botón Convertir a oportunidad ubicado en la parte superior izquierda de la página.

![Botón para crear oportunidad en el registro de un lead.](https://www.odoo.com/documentation/17.0/es/_images/convert-leads-convert-opp-button.png)

Esto abrirá un modal emergente Convertir a oportunidad. Aquí, en el campo Acciones de conversión, seleccione la opción Convertir a oportunidad.

 Nota

Para fusionar este lead con un lead u oportunidad existente similar, en el campo Acciones de conversión seleccione la opción Fusionar con oportunidades existentes. Esto generará una lista de lead u oportunidades similares que se pueden fusionar.

Al fusionar, Odoo prioriza el lead u oportunidad que se creó primero en el sistema y fusiona la información en donde se creó primero. Si fusiona un lead y una oportunidad el registro resultante se denomina oportunidad, sin importar que se creó primero.

Después, seleccione un Vendedor y un Equipo de ventas a los que se les debe asignar la oportunidad. Ninguno de los campos es obligatorio, aunque si hace una selección en el campo Vendedor, el campo Equipo de ventas se llenará en automático según cuál sea el equipo del vendedor.

Estos campos se completarán de forma automática con la información correspondiente si el lead ya estaba asignado a un vendedor o a un equipo.

![Ventana emergente para convertir a oportunidad.](https://www.odoo.com/documentation/17.0/es/_images/convert-leads-conversion-action.png)

Elija alguna de las siguientes opciones en la sección Cliente:

- Crear un nuevo cliente: elija esta opción para usar la información del lead para crear un nuevo registro de cliente.
    
- Vincular a un cliente existente: para vincular esta oportunidad al registro de un cliente existente elija esta opción y luego seleccione uno del menú desplegable.
    
- No vincular a un cliente: elija esta opción para convertir el lead, pero no vincularlo a un cliente nuevo o existente.
    

Por último, al completar todas las configuraciones, haga clic en Crear oportunidad.

Para ver la oportunidad que acaba de crear, vaya a la aplicación CRM ‣ Mi flujo.

 Nota

Es posible que deba quitar algunos filtros de la barra Buscar… en la página del Flujo para ver todas las oportunidades.