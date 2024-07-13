Un _bot de chat_ es un programa diseñado para imitar una conversación con un humano y funciona con un guion que debe seguir con pasos escritos previamente. Los guiones están diseñados para pronosticar la respuesta de un visitante y guiarlo mediante una serie de preguntas y respuestas de la misma manera que lo haría algún miembro del equipo.

Puede personalizar los bots de chat para que desempeñen varias funciones como proporcionar atención al cliente o crear leads y recopilar información de contacto. El objetivo del bot de chat depende de varios criterios, como la página de sitio web que se les asigne y la información que captura.

![Vista de la ventana de chat con un ticket del servicio de asistencia creado mediante la aplicación Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/chatbot-visitor-view.png)

## Crear un bot de chat[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#build-a-chatbot "Enlazar permanentemente con este título")

Antes de crear un nuevo bot de chat debe instalar la aplicación _Chat en vivo_ en la base de datos, puede instalarla desde el menú de Aplicaciones. Busque `Chat en vivo` en la barra de búsqueda y haga clic en Instalar.

Una vez que haya instalado la aplicación _chat en vivo_, vaya a Chat en vivo ‣ Configuración ‣ Bots de chat.

 Nota

Cuando instala la aplicación _Chat en vivo_, se crea un bot de chat de muestra con el nombre _Bot de bienvenida_. Este bot tiene un guion preconfigurado con algunos pasos básicos, como preguntar por el correo electrónico de un visitante o enviar esa conversación a un operador.

Puede utilizar el _Bot de bienvenida_ como base, ya que puede editar o eliminar los pasos existentes. También puede agregar nuevos pasos para personalizar el guion según sus necesidades.

Puede eliminar o archivar el _Bot de bienvenida_ si lo considera necesario.

![Vista del guion del bot de bienvenida en el Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/chatbot-welcome-bot.png)

Para crear un nuevo bot de chat, vaya a la página de bots de chat (aplicación Chat en vivo ‣ Configuración ‣ Bots de chat) y haga clic en Nuevo. Se abrirá una página con detalles para el bot de chat en blanco.

En la página de detalles para el bot de chat a completar, escriba la información correspondiente en el nombre del bot de chat y haga clic en el icono editar imagen en la esquina superior derecha del formulario para agregar una imagen.

### Guion para el bot de chat[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#chatbot-scripts "Enlazar permanentemente con este título")

Una vez que creó y nombró al bot de chat, debe crear un guion. Las conversaciones del bot de chat siguen el guion adjunto compuesto por líneas de diálogo, las cuales están diseñadas para proporcionar u obtener información.

Para crear un guion de bot de chat, haga clic en Agregar una línea en la pestaña Guion de la página de detalles del bot de chat. Se abrirá una ventana emergente de Pasos del guion.

Debe llenar este formulario para **cada** línea de texto (diálogo) que el bot de chat podría proporcionar durante la conversación.

Primero, escriba el contenido del mensaje en el campo Mensaje y luego seleccione una opción en los menús desplegables Tipos de paso y Solo si.

#### Tipos de paso[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#step-types "Enlazar permanentemente con este título")

El tipo de paso seleccionado depende del propósito que tenga el mensaje. Las opciones disponibles en el menú desplegable Tipo de paso se encuentran a continuación:

##### Texto[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#text "Enlazar permanentemente con este título")

Este paso se utiliza para los mensajes donde no se espera o no es necesaria una respuesta. Puede usar los pasos de texto para enviar un saludo, para proporcionar información como documentación, o para enviar enlaces a páginas web específicas.

 Importante

Los tipos de pasos de _texto_ solo tienen como objetivo proporcionar información, pues no permiten que los visitantes escriban una respuesta. Por lo tanto, **necesitan** pasos adicionales para poder continuar con la conversación.

##### Pregunta[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#question "Enlazar permanentemente con este título")

Este paso hace una pregunta y proporciona un conjunto de respuestas. El visitante hace clic en una respuesta y como resultado crea un nuevo paso en la conversación, también puede proporcionar un enlace opcional a una nueva página web.

Ingrese la pregunta en el campo Mensaje. Después, en el encabezado Respuesta haga clic en Agregar una línea para crear una línea de respuesta en blanco.

Ingrese la respuesta como deba aparecerle al visitante. Para que la respuesta sea un enlace que se abra cuando el visitante lo seleccione, agregue la URL a la línea de respuesta en el encabezado Enlace opcional.

Repita estos pasos para cada respuesta a la pregunta que se deba incluir.

Haga clic en Guardar y cerrar o Guardar y crear nuevo.

 Truco

Es útil agregar una respuesta general (por ejemplo, `Algo más`) a los pasos de preguntas. Esto ayuda a los visitantes a continuar la conversación, incluso si lo que necesitan no coincide exactamente con ninguna de las otras respuestas.

##### Correo electrónico[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#email "Enlazar permanentemente con este título")

Este paso solicita a los visitantes que proporcionen su dirección de correo electrónico, esta se almacena y los miembros del equipo podrán utilizarla después para realizar un seguimiento con información adicional.

Las **únicas** entradas aceptadas para este tipo de paso son las direcciones de correo electrónico con un formato válido. Si un visitante intenta escribir otra cosa, el bot de chat responderá que no reconoce la información enviada.

![Vista de un bot de chat que responde a un correo electrónico no válido.](https://www.odoo.com/documentation/17.0/es/_images/chatbot-invalid-email.png)

##### Teléfono[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#phone "Enlazar permanentemente con este título")

Al igual que el correo electrónico, este tipo de paso le pide al visitante que proporcione su número de teléfono. Este se podrá utilizar después para hacer un seguimiento con información adicional o para agendar demostraciones y otras actividades.

 Advertencia

Debido a la gran cantidad de formatos que tienen los números telefónicos en todo el mundo, en este tipo de paso **no** se valida el formato de las respuestas, que pueden incluir tanto números como caracteres especiales.

##### Reenviar al operador[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#forward-to-operator "Enlazar permanentemente con este título")

Este paso envía la conversación a un operador de chat en vivo activo para que pueda seguir ayudando al visitante. La transcripción de la conversación se transfiere al operador, y este podrá continuar donde se quedó el bot de chat. Esto no solo ahorra tiempo para todas las partes involucradas, también puede ayudar a calificar las conversaciones antes de que lleguen a los operadores.

 Nota

Si ningún operador está activo en el canal, el bot de chat seguirá la conversación con el visitante. Por lo tanto, los pasos adicionales se deben agregar después de este para asegurarse de que la conversación no se terminará de forma abrupta. Los pasos adicionales pueden servir para indicarle a los visitantes que por ahora no hay operadores disponibles (por ejemplo, `Lo sentimos, al parecer ninguno de nuestros operadores está disponible`) y para continuar la conversación (por ejemplo `¿Por qué no deja su correo electrónico?`).

![Vista de mensajes de seguimiento de un bot de chat cuando ningún operador de chat en vivo está disponible.](https://www.odoo.com/documentation/17.0/es/_images/chatbot-no-operator.png)

##### Entrada libre o multilínea[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#free-input-multi-line "Enlazar permanentemente con este título")

El paso denominado _entrada libre_ permite que los visitantes respondan a las preguntas sin proporcionar respuestas predefinidas. La información proporcionada en estas respuestas se almacena en las transcripciones del chat.

Elija entre Entrada libre y Entrada libre (multilínea) según el tipo y la cantidad de información que el visitante deba proporcionar.

##### Crear lead[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#create-lead "Enlazar permanentemente con este título")

Este paso crea un lead en la aplicación _CRM_. Seleccione una opción del menú desplegable Equipo de ventas para asignar el lead que se creó a un equipo específico.

 Nota

Este paso **solo** está disponible si la aplicación _CRM_ se instala en la base de datos.

##### Crear ticket[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#create-ticket "Enlazar permanentemente con este título")

Este paso creará un [ticket](https://www.odoo.com/documentation/17.0/es/applications/services/helpdesk/overview/receiving_tickets.html) en la aplicación _Servicio de asistencia_. Seleccione una opción desde el campo desplegable Equipo de Servicio de asistencia que aparece para asignar el ticket creado a un equipo específico.

 Nota

Este paso **solo** está disponible si la aplicación _Servicio de asistencia_ se instala en la base de datos.

#### Solo si[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#only-if "Enlazar permanentemente con este título")

Los guiones del bot de chat trabajan con una base «si - entonces», es decir, la siguiente pregunta que se le hará al visitante está determinada por la respuesta que proporcionó a la pregunta anterior.

Para continuar con la conversación, el formulario para crear pasos del guión contiene un campo etiquetado Solo si. En este campo se define la progresión de las preguntas.

Puede dejar vacío este campo si espera que un paso siga todos los mensajes anteriores. Sin embargo, si un mensaje **solo** debe enviarse de forma condicional, según las respuestas anteriores, entonces **debe** agregar esas respuestas a este campo.

 Importante

Si se hace cualquier selección en el campo Solo si, debe hacer **todas** las selecciones durante la conversación _antes_ de incluir este paso. Solo incluya selecciones en este campo si son necesarias para mostrar este paso.

 Example

En el guion del _bot de bienvenida_, un visitante puede preguntar sobre los precios. Si el visitante selecciona esta respuesta, se incluye un paso para enviar la conversación a un operador. El bot de chat primero envía un mensaje que le informa al visitante que está en búsqueda de un operador disponible para chatear.

Sin embargo, este mensaje **solo** se debe enviar si el visitante solicita información de precios. En ese caso, la conversación sería la siguiente:

- Bot de bienvenida: «_¿Qué está buscando?_»
    
- Visitante: «**Tengo una pregunta sobre los precios.**»
    
- Bot de bienvenida: «_Mmmm, déjeme revisar si puedo encontrar a alguien que pueda ayudarle con eso…_»
    

En el formulario de detalles del paso de tipo texto se seleccionó la respuesta _Tengo una pregunta sobre los precios_ en el campo Solo si. Este paso **solo** aparece en las conversaciones donde se seleccionó esa respuesta.

![Vista del formulario de nuevo mensaje, se resalta el campo Solo si.](https://www.odoo.com/documentation/17.0/es/_images/chatbot-only-if.png)

### Pruebas con el guion[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#script-testing "Enlazar permanentemente con este título")

Para garantizar que todos los visitantes tengan una experiencia satisfactoria con el bot de chat, cada mensaje debe tener un desenlace natural. Debe probar los guiones del bot de chat para verificar que los mensajes proporcionan soluciones adecuadas y para comprender lo que el visitante ve cuando interactúa con el bot.

 Importante

Si el visitante da una respuesta o entrada de texto que **no** tiene asignada una respuesta para continuar, la conversación se detiene. Como el visitante no puede volver a activar el bot de chat, tendrá que actualizar la ventana de chat o el navegador para iniciar la conversación de nuevo.

Para probar el rendimiento de un bot de chat, primero haga clic en Probar en la parte superior izquierda de la página del guion del bot de chat. Se le redirigirá a la pantalla de prueba, responda las preguntas del bot de chat como lo haría un visitante potencial del sitio.

Cuando el guion ya no tiene más mensajes para mostrar, en la parte inferior de la ventana de chat aparece el mensaje _La conversación terminó… Reiniciar_. Para iniciar una conversación con el primer mensaje del guion, haga clic en Reiniciar. Para volver a la página del guion, haga clic en Volver al modo de edición en la parte superior de la página.

## Agregar un bot de chat a un canal[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/chatbots.html#add-chatbot-to-a-channel "Enlazar permanentemente con este título")

Después de crear y probar su bot conversacional, debe agregarlo a un canal de chat en vivo.

Primero, abra la aplicación Chat en vivo y encuentre la tarjeta de kanban del canal de chat en vivo que desea, pase el cursor por encima y haga clic en el icono ⋮ (kebab) para abrir el menú desplegable. Haga clic en Configurar canal para abrir el formulario de detalles del canal.

 Nota

Para crear un nuevo canal de chat en vivo, abra la aplicación Chat en vivo y haga clic en Nuevo. Vea [Chat en vivo](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html) para más información.

Haga clic en la pestaña Reglas del canal. Después, abra una regla existente o cree una nueva haciendo clic en Agregar una línea.

En la ventana emergente Crear reglas seleccione un bot de chat apropiado en el campo bot de chat.

Si el bot conversacional **solo** debe estar activo si no hay operadores de chat en vivo disponibles, marque la casilla con el nombre Habilitado solo si no hay un operador.

![Vista de las reglas del canal, se resalta el campo Bot de chat.](https://www.odoo.com/documentation/17.0/es/_images/chatbot-add-to-channel.png)

 Ver también

[Reglas del canal de chat en vivo](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html)