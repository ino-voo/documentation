El _Chat en vivo_ de Odoo le permite a los visitantes de un sitio web comunicarse dentro del mismo en tiempo real. Con el _Chat en vivo_, puede calificar a los leads de acuerdo a su potencial de ventas, ayudar a que la respuesta a las preguntas sea más rápida y que los equipos apropiados puedan atender e investigar (o dar seguimiento) acerca de los problemas que puedan surgir. El _Chat en vivo_ también brinda la oportunidad de recibir retroalimentación inmediata de parte de los clientes.

## Habilitar chat en vivo[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#enable-live-chat "Enlazar permanentemente con este título")

La aplicación _Chat en vivo_ puede instalarse de varias formas:

- Vaya a Aplicaciones ‣ Chat en vivo y haga clic en Instalar.
    
- Vaya a la vista de lista en Servicio de asistencia ‣ Configuración ‣ Equipos de servicio de asistencia, seleccione un equipo y en la página de ajustes de equipo marque la casilla de verificación a un lado de Chat en vivo, en la sección Canales.
    
- En la aplicación Sitio web, vaya a Configuración ‣ Ajustes, baje hasta la sección de Correo electrónico y Marketing, seleccione la casilla que esta junto a Chat en vivo y haga clic en Guardar.
    
    ![Vista de la página de ajustes y de la función de chat en vivo para Chat en vivo en Odoo.](https://www.odoo.com/documentation/17.0/es/_images/enable-setting.png)
    

 Nota

Después de que se haya instalado la aplicación _Chat en vivo_, se creará un _canal_ de chat en vivo de forma predeterminada.

## Crear canales de chat en vivo[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#create-live-chat-channels "Enlazar permanentemente con este título")

Para crear un nuevo _Canal_ de chat en vivo, vaya a la aplicación Chat en vivo ‣ Nuevo”. Esto abrirá un formulario de detalles en blanco para un canal. Escriba el nombre del nuevo canal en el campo :guilabel:`Nombre del canal.

![Vista de un formulario de canal de chat en vivo en la aplicación Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/open-channel.png)

Para configurar las pestañas restantes en el formulario de detalles del canal ([Operadores](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#livechat-operators-tab), [Opciones](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#livechat-options-tab), [Reglas del canal](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#livechat-channel-rules-tab) y [Widget](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#livechat-widget-tab)), siga los pasos a continuación.

 Truco

The channel detail form for any channel can be accessed by navigating back to the Website Live Chat Channels dashboard, via the breadcrumbs. Find the Kanban card for the appropriate live chat channel, hover over it, and then click on the  (vertical ellipsis) icon to open the drop-down menu. Click Configure Channel to open the channel detail form.

### Pestaña de los operadores[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#operators-tab "Enlazar permanentemente con este título")

Los _operadores_ son usuarios que pueden funcionar como agentes y responder solicitudes de los clientes del chat en vivo. Cuando un usuario se agrega como operador en un canal del chat en vivo, podrán recibir chats desde los visitantes del sitio web sin importar donde estén en su base de datos. Las ventanas de chat se abrirán en la parte inferior derecha de la pantalla.

![Vista de una ventana emergente de chat en vivo en una base de datos de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/pop-up1.png)

Haga clic en la pestaña Operadores del formulario de detalles del canal. El usuario que creó el canal de chat en vivo aparecerá como operador de forma predeterminada.

 Nota

Puede editar (o eliminar) a los operadores actuales haciendo clic en sus respectivas casillas en la pestaña de Operadores, la cual muestra una ventana emergente adicional de Abrir: Operadores. En esa ventana, edite la información que necesite y haga clic en Guardar o haga clic en Eliminar para eliminar a ese operador del canal.

Haga click en Agregar para mostrar una ventana emergente de Operadores.

En la ventana emergente, deslícese hacia abajo hasta encontrar los usuarios deseados, ingrese su nombre en la barra de búsqueda. Después, marque la casilla de verificación a un lado de los usuarios para agregarlos y haga clic en Seleccionar.

Puede crear nuevos operadores y agregarlos a la lista directamente desde esta ventana emergente haciendo clic en Nuevo y llenando el formulario emergente de Crear operadores. Cuando el formulario esté completo, haga clic en guilabel:`Guardar y cerrar`, o en Guardar y nuevo para crear varios registros.

 Peligro

Crear un nuevo usuario puede cambiar el estado de una suscripción de Odoo, ya que el número total de usuarios en una base de datos se toma en cuenta para calcular el precio; piénselo bien antes de crear un usuario nuevo. Si el usuario ya existe y lo agrega como operador **no** afectará la suscripción ni el precio de la base de datos.

### Pestaña de opciones[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#options-tab "Enlazar permanentemente con este título")

La pestaña de opciones en el formulario de detalles del canal de chat en vivo contiene los ajustes visuales y de texto para la ventana de chat en vivo.

#### Botón de chat en vivo[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#livechat-button "Enlazar permanentemente con este título")

El _botón de chat en vivo_ es el icono que aparece en la esquina inferior del sitio web.

![Vista de un sitio web en Odoo, se resalta el botón de chat en vivo.](https://www.odoo.com/documentation/17.0/es/_images/chat-button.png)

Cambie el texto en el campo Texto de la notificación para actualizar el texto que se mostrará en la burbuja de texto cuando el botón de chat en vivo aparezca en el sitio web.

The Livechat Button Color alters the color of the live chat button as it appears on the website. To change the color, click on a color bubble to open the color selection window, then click and drag the circle along the color gradient. Click out of the selection window once complete. Click the  (refresh) icon to the right of the color bubbles to reset the colors to the default selection.

 Truco

Puede elegir un color para el botón o encabezado manualmente con el selector, también puede escribir el código de color RGB, HSL o HEX en la ventana emergente de selección de color que aparece cuando hace clic en cualquiera de las burbujas. Hay distintas opciones disponibles según el sistema operativo que utilice.

#### Ventana de chat en vivo[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#livechat-window "Enlazar permanentemente con este título")

La _ventana de chat en vivo_ es el espacio donde se lleva a cabo la conversación con los visitantes del sitio web.

Edite el mensaje de bienvenida para cambiar el mensaje que recibe el visitante al iniciar una nueva sesión de chat. Este mensaje simula que lo envió un operador de chat en vivo, debe funcionar como un saludo e incitar a seguir conversando.

Edite el marcador de posición de entrada de texto del chat para modificar el texto que aparece en el cuadro donde los visitantes escriben sus respuestas. Este mensaje incita a que el visitante inicie a chatear.

El _encabezado del canal_ es la barra de color en la parte superior de la ventana de chat y puede cambiar el color del encabezado del canal si sigue los mismos pasos que realizó para el [Botón de chat en vivo](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#livechat-livechat-button).

![../../_images/chat-window.png](https://www.odoo.com/documentation/17.0/es/_images/chat-window.png)

La ventana de chat en vivo con un encabezado de canal morado y un texto de marcador de posición que dice «Diga algo…»[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#id1 "Enlace permanente a esta imagen")

### Pestaña de reglas del canal[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#channel-rules-tab "Enlazar permanentemente con este título")

La pestaña Reglas del canal en el formulario de detalles del canal de chat en vivo determina cuando se abre la ventana de chat en vivo en el sitio web. Para esto, debe configurar cuando se activa una acción regex de URL, como una visita a la página.

Para crear una nueva regla de canal haga clic en Agregar una línea. Esto hará que se abra la ventana emergente Crear reglas.

![Vista de un formulario de reglas de un canal en la aplicación Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/create-rules.png)

#### Crear nuevas reglas[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#create-new-rules "Enlazar permanentemente con este título")

Complete los campos en la ventana emergente Crear reglas como se indica a continuación y luego haga clic en Guardar y cerrar.

Live Chat ButtonChatbotURL RegexOpen automatically timerCountry

El _botón de Chat en vivo_ es el icono que aparece en la esquina inferior del sitio web. Seleccione una de las siguientes opciones de visualización:

- Mostrar: muestra el botón de chat en las páginas.
    
- Mostrar con notificación: muestra el botón de chat y una burbuja de texto que flota junto al botón.
    
- Abrir de forma automática: muestra el botón y abre la ventana de chat en automático después de una cantidad específica de tiempo (esta se define en el campo Temporizador para abrir de forma automática, que se muestra al seleccionar esta opción).
    
- Ocultar: oculta el botón de chat en las páginas.
    

 Nota

Para poder rastrear la ubicación geográfica de los visitantes debe instalar _GeoIP_ en su base de datos. Esta función se instala de forma predeterminada en based datos de _Odoo en línea_, pero en las bases de datos _locales_ debe realizar algunos [pasos de configuración](https://www.odoo.com/documentation/17.0/es/administration/on_premise/geo_ip.html).

### Pestaña de widget[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html#widget-tab "Enlazar permanentemente con este título")

La pestaña Widget en el formulario de detalles del canal de chat en vivo proporciona el código para un widget de sitio web. Puede agregar este código a un sitio web para proporcionar acceso a una ventana de chat en vivo.

 Truco

Puede agregar el widget de chat en vivo a sitios web creados con Odoo. Vaya a Sitio web ‣ Configuración ‣ Ajustes. Después, baje hasta la sección Correo electrónico y marketing. En el campo Canal seleccione el canal que quiere agregar al sitio y después haga clic en Guardar.

Si desea agregar el widget a un sitio web que creó en una plataforma externa, solo haga clic en el primer botón de COPIAR en la pestaña Widget y pegue el código en la etiqueta `<head>` del sitio.

Del mismo modo, para enviar una sesión de chat en vivo a un cliente, haga clic en el segundo botón de COPIAR en la pestaña Widget. Puede enviar este enlace a un cliente y una vez que haga clic, se abrirá una nueva ventana de chat.

![Vista de la pestaña "widget" en la aplicación Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/widget-code.png)

 Ver también

- [Conversaciones](https://www.odoo.com/documentation/17.0/es/applications/productivity/discuss.html)
    
- [Comandos y respuestas predefinidas](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html)
    
- [Valoraciones](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/ratings.html)
    
- [Bots de chat](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html)
    
- [Participate in live chat](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/participate.html)