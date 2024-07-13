Puede agregar leads a la aplicación _CRM_ con seudónimos de correo personalizados o creando registros nuevos de forma manual. Esto es además de los leads y oportunidades que se crearon en la aplicación a través del [formulario de contacto del sitio web](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/opportunities_form.html).

Primero vaya a CRM ‣ Configuración ‣ Ajustes para asegurarse de que la función _Leads_ esté activa. Marque la casilla de verificación Leads y después haga clic en Guardar.

## Configurar seudónimos de correo[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/email_manual.html#configure-email-aliases "Enlazar permanentemente con este título")

Cada equipo de ventas puede crear y utilizar su propio seudónimo de correo. Cuando se envíen mensajes a esta dirección de correo, se creará un lead (u oportunidad) con la información del mensaje.

Para crear o actualizar los seudónimos de correos de un equipo de ventas, vaya a CRM ‣ Configuración ‣ Equipos de ventas. Haga clic en un equipo de la lista para abrir la página de detalles de ese equipo.

![La página de detalles del equipo de ventas, con el enfoque en la sección de seudónimos de correo.](https://www.odoo.com/documentation/17.0/es/_images/email-alias.png)

En el campo :guilabel:` Seudónimo de correo electrónico` ingrese el nombre del seudónimo de correo electrónico o edite el nombre existente. En el campo Aceptar correos electrónicos de use el menú desplegbale para seleccionar quién puede enviar mensajes a este seudónimo de correo electrónico:

- Todos: cualquier dirección de correo electrónico puede enviar mensajes.
    
- Contactos autenticados: solo acepta mensajes de correos electrónicos asociados con un registro de contacto o cliente.
    
- Solo seguidores: solo se aceptan mensajes de personas que están siguiendo un registro relacionado al equipo, como un lead o una oportunidad. También se reciben mensajes de miembros del equipo.
    
- Empleados autenticados: solo se aceptan mensajes de direcciones de correo que estén vinculadas a algún registro de la aplicación _Empleados_.
    

### Leads creados desde un correo[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/email_manual.html#leads-created-from-email "Enlazar permanentemente con este título")

Los leads que se creen de mensajes a seudónimos de correo se pueden ver en CRM ‣ Leads. Haga clic en un lead de la lista para abrirlo y ver los detalles.

El correo que se haya recibido en el alias se agregará al hilo del _chatter_ para el lead. El asunto del mensaje se agregará al campo de título y el campo Correo se actualizará con la dirección de correo del contacto.

![El hilo de chatter de un lead recién creado en la aplicación CRM.](https://www.odoo.com/documentation/17.0/es/_images/chatter-message.png)

 Nota

Si la función _leads_ **no** está activa en la base de datos, los mensajes que se envíen al seudónimo de correo se agregarán a la base de datos como oportunidades.

 Ver también

[Enviar y recibir correos electrónicos en Odoo con un servidor de correo electrónico](https://www.odoo.com/documentation/17.0/es/applications/general/email_communication/email_servers.html)

## Crear leads de forma manual[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/email_manual.html#manually-create-leads "Enlazar permanentemente con este título")

Puede agregar leads a la aplicación _CRM_ directamente, solo debe crear un nuevo registro de forma manual. Vaya a CRM ‣ Leads para ver una lista de leads existentes.

 Truco

También puede agregar leads con el botón [Generar leads](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/lead_mining.html).

En la parte superior izquierda de la lista, haga clic en Nuevo para abrir un formulario en blanco de Leads.

En el primer campo del formulario nuevo ingrese el título para el lead nuevo. Luego, ingrese un Nombre de contacto y un Nombre de empresa.

 Nota

Si un lead se [convierte a oportunidad](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/convert.html) el campo Nombre de la empresa se usa ya sea para vincular esta oportunidad a un cliente existente o para crear un cliente nuevo.

### Crear oportunidades de forma manual[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/email_manual.html#manually-create-opportunities "Enlazar permanentemente con este título")

Para crear una oportunidad de forma manual vaya a CRM ‣ Ventas ‣ Mi flujo. En la parte superior izquierda de la página haga clic en Nuevo para crear una tarjeta kanban nueva de oportunidad. En el campo Organización/contacto ingrese el nombre de la empresa para la que es la oportunidad.

Seleccione un nombre y póngalo en el campo Oportunidad, _el cual es un campo obligatorio._ Al crear una oportunidad de forma manual, lo mejor es ponerle un nombre que se relacione a los detalles de la oportunidad.

 Example

En el ejemplo a continuación, la oportunidad se llama `5 sillas`. Esto identifica el producto que le interesa al cliente, además de la cantidad potencial que quiere comprar.

![Un ejemplo de una oportunidad en el flujo CRM.](https://www.odoo.com/documentation/17.0/es/_images/opportunity-example.png)

Ingrese la información de contacto para la oportunidad en los campos Correo y Teléfono.

En el campo Ingreso esperado ingrese el valor estimado para la oportunidad.

 Nota

La información en el campo Ingreso esperado y los campos prioritarios se puede usar para monitorear el rendimiento de vendedores individuales y del equipo en sí. Vea [Reporte de ingresos esperados](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/expected_revenue_report.html) y [Asignación de leads con la puntuación predictiva de leads](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/lead_scoring.html) para más información.

Después, use los iconos de  (estrella) para asignar la prioridad.

-   : prioridad baja
    
-   : prioridad media
    
-   : prioridad alta
    
-   : la prioridad más alta
    

 Nota

El asignar una prioridad hará que cambie el orden en el que los leads se ven en la vista Kanban, los leads con la prioridad más alta se mostrarán primero.

Haga clic en Agregar una vez que haya agregado toda la información necesaria.

![El flujo de CRM con una oportunidad recién creada.](https://www.odoo.com/documentation/17.0/es/_images/create-opportunities.png)