In the Odoo _Live Chat_ application, _commands_ allow the user to perform specific actions both inside the chat window, and through other Odoo applications. The _Live Chat_ app also includes _canned responses_. These are customized, preconfigured substitutions that allow users to replace shortcut entries in place of longer, well-thought out responses to some of the most common questions and comments.

Tanto los comandos como las respuestas predeterminadas ahorran tiempo y permiten que los usuarios mantengan un nivel de consistencia en sus conversaciones.

## Ejecutar un comando[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#execute-a-command "Enlazar permanentemente con este título")

Live chat _commands_ are keywords that trigger preconfigured actions. When a live chat _operator_ is participating in a conversation with a customer or website visitor, they can execute a command by typing `/`, followed by the command.

Commands, and the resulting actions, are only visible in the conversation window for the live chat operator. A customer does not see any commands that an operator uses in a conversation from their view of the chat.

 Example

During a conversation with a customer, a live chat operator executes the command to [create a ticket](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#live-chat-ticket). After entering the command, `/ticket`, the system automatically creates a ticket with the information from the conversation. It also includes a link to the new ticket, so the operator can go there directly to add any additional information, if necessary.

![Vista de la ventana de chat con un ticket del servicio de asistencia creado mediante la aplicación Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/responses-ticket-link.png)

A continuación encontrará más información sobre los comandos disponibles.

### Ayuda[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#help "Enlazar permanentemente con este título")

Si un operador escribe `/ayuda` en la ventana del chat, aparecerá un mensaje con información que incluye los tipos de entrada potenciales que puede hacer.

- Escriba `@nombre_de_usuario` para mencionar a un usuario en la conversación. Ese usuario recibirá una notificación en su bandeja de entrada o correo electrónico, según la configuración de sus notificaciones.
    
- Escriba `#canal` para mencionar un canal de _Conversaciones_.
    
- Escriba `/comando` para ejecutar un comando.
    
- Escriba `:atajo` para insertar una [respuesta predefinida](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#live-chat-canned-responses).
    

![Vista del mensaje que se generó mediante el comando /ayuda en la aplicación Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/responses-help.png)

 Ver también

- [Conversaciones](https://www.odoo.com/documentation/17.0/es/applications/productivity/discuss.html)
    
- [Uso de canales para la comunicación en equipo](https://www.odoo.com/documentation/17.0/es/applications/productivity/discuss/team_communication.html)
    

### Ticket & search tickets[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#ticket-search-tickets "Enlazar permanentemente con este título")

The `/ticket` and `/search_tickets` commands allow operators to create helpdesk tickets directly from a conversation, and search through existing tickets by keyword or ticket number.

 Importante

The `/ticket` and `/search_tickets` commands can **only** be used if the _Helpdesk_ app has been installed, and _Live Chat_ has been activated on a _Helpdesk_ team. To activate _Live Chat_, go to Helpdesk app ‣ Configuration ‣ Helpdesk Teams, and select a team. Scroll to the Channels section, and check the box labeled, Live Chat.

#### Crear un ticket desde un chat en vivo[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#create-a-ticket-from-a-live-chat "Enlazar permanentemente con este título")

If an operator types `/ticket` in the chat window, the conversation is used to create a _Helpdesk_ ticket.

After entering the `/ticket` command, type a title for the ticket into the chat window, then press `Enter`.

![Vista de los resultados de una búsqueda en el servicio de asistencia en una conversación de chat en vivo.](https://www.odoo.com/documentation/17.0/es/_images/helpdesk.png)

El equipo de _Servicio de asistencia_ con el chat en vivo habilitado recibirá el ticket recién creado. Si más de un equipo tiene esta función habilitada, entonces se asignará en automático según la prioridad del equipo.

La transcripción de la conversación se agregará al nuevo ticket, en la pestaña Descripción.

To access the new ticket, click on the link in the chat window, or go to the Helpdesk app, and click the Tickets button on the Kanban card for the appropriate team.

#### Buscar un ticket desde un chat en vivo[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#search-for-a-ticket-from-a-live-chat "Enlazar permanentemente con este título")

If an operator types `/search_tickets` in the chat window, they can search through _Helpdesk_ tickets, either by ticket number or keyword.

After entering the `/search_tickets` command, type a keyword or ticket number, then press Enter. If one or more related tickets are found, a list of links is generated in the conversation window.

![Vista de los resultados de una búsqueda en el servicio de asistencia en una conversación de chat en vivo.](https://www.odoo.com/documentation/17.0/es/_images/helpdesk-search.png)

 Nota

Solo el operador podrá ver los resultados del comando de búsqueda, el cliente no.

### Historial[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#history "Enlazar permanentemente con este título")

Typing `/history` in the chat window generates a list of the most recent pages the visitor has viewed on the website (up to fifteen pages).

![Vista de los resultados del comando /historial en una conversación de chat en vivo.](https://www.odoo.com/documentation/17.0/es/_images/responses-history.png)

### Iniciativa[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#lead "Enlazar permanentemente con este título")

Si un operador escribe `/lead` en la ventana de chat, creará un _lead_ en la aplicación _CRM_.

![Vista de los resultados de un comando /lead en una conversación de chat en vivo.](https://www.odoo.com/documentation/17.0/es/_images/responses-lead.png)

 Importante

Solo puede utilizar el comando `/lead` si instaló la aplicación _CRM_.

Después de escribir `/lead`, proporcione un título para este lead y luego presione `Enter`. Aparecerá un enlace con el título del lead, haga clic en él o vaya a la aplicación CRM para ver el flujo.

 Nota

Solo el operador puede ver y acceder al enlace del lead, el cliente no.

Se agregará la transcripción de esa conversación en específico (donde se creó el lead) de chat en vivo a la pestaña Notas internas del formulario de lead.

En la pestaña Información adicional del formulario del lead, aparecerá Chat en vivo como fuente.

### Ausencia[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#leave "Enlazar permanentemente con este título")

Un operador puede salir de la conversación si escribe `/leave` en la ventana de chat. Este comando no hace que el cliente salga de la conversación o que esta termine de forma automática.

 Ver también

- [Obtener leads](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads.html)
    
- [Servicio de asistencia](https://www.odoo.com/documentation/17.0/es/applications/services/helpdesk.html)
    

## Respuestas predefinidas[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#canned-responses "Enlazar permanentemente con este título")

_Canned responses_ are customizable inputs, where a typed shortcut populates a longer response. A user enters a keyword _shortcut_, which is then automatically replaced by the expanded _substitution_ response. The shortcut is the keyword or key phrase that is to be replaced. The substitution is the longer message that replaces the shortcut.

### Crear respuestas predefinidas[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#create-canned-responses "Enlazar permanentemente con este título")

Para crear una nueva respuesta predefinida, vaya a la aplicación Chat en vivo ‣ Configuración ‣ Respuestas predefinidas ‣ Nuevo.

Type a shortcut command in the Shortcut field. Next, click the Substitution field, and type the message that should replace the shortcut.

 Truco

Try to connect the shortcut to the topic of the substitution. Not only does this make it easier to use the responses, it prevents the list of responses from becoming disorganized and overwhelming.

In the Description field, add any information that provides context for this response, such as guidelines for when it should or should not be used.

The Last Used field keeps track of the date and time each response was most recently used. This field **cannot** be edited.

### Usar respuestas predefinidas en una conversación de chat en vivo[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html#use-canned-responses-in-a-live-chat-conversation "Enlazar permanentemente con este título")

Para usar una respuesta predefinida durante una conversación de chat en vivo, escriba dos puntos (`:`) en la ventana de chat y luego el atajo.

 Example

Un operador se encuentra conversando con un visitante. Al escribir `:` tendrá acceso a una lista de respuestas disponibles y podrá seleccionar una de la lista o continuar escribiendo. Si desea usar la respuesta predefinida `'Lamento escuchar eso.'`, deberá escribir `:disculpa`.

![Vista de una ventana de chat y el uso de una respuesta predefinida en la aplicación Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/canned-responses.png)

 Truco

Cuando escribe `:` en una ventana de chat se genera la lista de respuestas predefinidas disponibles. Además del uso de accesos rápidos, también puede seleccionar manualmente las respuestas de esta lista.

![Vista de una ventana de chat y la lista de respuestas predefinidas disponibles.](https://www.odoo.com/documentation/17.0/es/_images/response-list.png)