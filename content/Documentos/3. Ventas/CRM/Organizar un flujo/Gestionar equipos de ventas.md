La función _Equipos de Ventas_ de la aplicación _CRM_ de Odoo permite crear y gestionar varios equipos de ventas, cada uno con sus propias reglas de asignación, objetivos de facturación y lista de vendedores.

## Crear un equipo de ventas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/manage_sales_teams.html#create-a-sales-team "Enlazar permanentemente con este título")

Para crear un nuevo equipo de ventas, vaya a CRM ‣ Configuración ‣ Equipos de venta y haga clic en Nuevo.

En el formulario vacío del equipo de ventas, asígnele un nombre en el campo Equipo de ventas.

Seleccione un líder del equipo en la lista desplegable.

Configure un seudónimo de correo electrónico para generar leads u oportunidades en automático para este equipo de ventas cada que reciba un mensaje en esa dirección. Elija si desea aceptar correos electrónicos de todos, contactos autenticados, solo seguidores o empleados autenticados.

Seleccione una Empresa del menú desplegable para asignarle este equipo.

 Nota

El campo Empresa solo aparece en bases de datos multiempresa y no es obligatorio.

![La página de ajustes de un nuevo equipo de ventas.](https://www.odoo.com/documentation/17.0/es/_images/sales-team-creation.png)

 Nota

En el formulario del equipo de ventas aparece el campo Objetivo de facturación si la aplicación _Ventas_ está instalada en la base de datos. Este es el objetivo de ingresos para el mes actual. La cantidad ingresada en este campo se utiliza para completar la barra de progreso de facturación en el [tablero del equipo de ventas](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/manage_sales_teams.html#crm-sales-team-dashboard).

### Agregar miembros al equipo de ventas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/manage_sales_teams.html#add-sales-team-members "Enlazar permanentemente con este título")

Haga clic en Agregar en la pestaña Miembros al editar la página de configuración del equipo de ventas para añadir miembros al equipo. Esta acción abre la ventana emergente Crear miembros del equipo de ventas.

 Nota

Si la función Asignación por reglas **no** está habilitada en la página de _ajustes_ de la aplicación _CRM_, al hacer clic en Agregar en la pestaña Miembros se abrirá la ventana emergente Agregar: Vendedores. Seleccione la casilla ubicada del lado izquierdo del vendedor que desea agregar al equipo y luego haga clic en Seleccionar.

![La ventana emergente "Agregar: Vendedores" en un nuevo equipo de ventas.](https://www.odoo.com/documentation/17.0/es/_images/add-salespersons.png)

Seleccione un usuario de la lista desplegable Vendedor para agregarlo al equipo. Para evitar que reciba oportunidades de forma automática, seleccione la casilla Omitir durante la asignación automática. En caso de que esta función esté activada, aún podrá asignarle oportunidades de forma manual.

![La ventana emergente para crear miembros del equipo de ventas.](https://www.odoo.com/documentation/17.0/es/_images/create-sales-team-members.png)

El campo Leads (30 días) lleva seguimiento de los leads que se le han asignado al vendedor en los últimos treinta días en este equipo, así como el número máximo de leads que se le deben asignar. Para editar el número máximo de leads que este vendedor puede recibir, escriba la cantidad en el campo Leads (30 días).

 Truco

Las [reglas de asignación](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/lead_scoring.html) se pueden configurar para cada vendedor con la sección Dominio.

Haga clic en Guardar y cerrar cuando haya terminado o en Guardar y crear nuevo para agregar otros miembros.

## Habilitar varios equipos[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/manage_sales_teams.html#enable-multi-teams "Enlazar permanentemente con este título")

Para permitir que los vendedores puedan formar parte de más de un equipo de ventas es necesario habilitar la función _Varios equipos_. Primero vaya a CRM ‣ Configuración ‣ Ajustes. En la sección CRM, seleccione la casilla con el nombre Varios equipos y luego haga clic en el botón Guardar ubicado en la parte superior izquierda de la página.

![La página de ajustes de la aplicación CRM con la función Varios equipos habilitada.](https://www.odoo.com/documentation/17.0/es/_images/enable-multi-teams.png)

## Tablero del equipo de ventas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/manage_sales_teams.html#sales-team-dashboard "Enlazar permanentemente con este título")

Para ver el tablero del equipo de ventas, vaya a CRM ‣ Ventas ‣ Equipos. Todos los equipos en los que el usuario es miembro aparecerán en el tablero.

![El tablero del equipo de ventas en la aplicación CRM.](https://www.odoo.com/documentation/17.0/es/_images/sales-teams-dashboard.png)

Cada tarjeta de kanban ofrece un resumen sobre las oportunidades abiertas, cotizaciones, órdenes de venta y ingresos esperados del equipo de ventas, así como un gráfico de barras con las nuevas oportunidades por semana y una barra de progreso de facturación.

Haga clic en el botón Flujo para ir directamente al flujo de _CRM_ del equipo.

Haga clic en el icono  (puntos verticales) ubicado en la esquina superior derecha de la tarjeta de kanban para abrir el menú desplegable. Haga clic en Configuración para ver o editar la configuración del equipo.

 Ver también

- [Utilizar actividades para los equipos de ventas](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html)
    
- [Asignación de leads con la puntuación predictiva de leads](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/lead_scoring.html)