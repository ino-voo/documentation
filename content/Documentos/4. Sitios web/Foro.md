La aplicación **Foro de Odoo** es un foro de preguntas y respuestas diseñado para proporcionar soporte al cliente. Agregar un foro a un sitio web le permite construir una comunidad, fomentar la participación y compartir información.

## Crear un foro[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#create-a-forum "Enlazar permanentemente con este título")

Para crear o editar un foro, vaya a Sitio web ‣ Configuración ‣ Foro: Foros. Haga clic en Nuevo o seleccione un foro existente y configure los siguientes elementos.

Nombre del foro: agregue el nombre del foro.

Modo: seleccione Preguntas para permitir marcar una respuesta como la mejor, esto significa que las preguntas aparecen como _resueltas_. Si selecciona Conversaciones entonces la función no es necesaria.

 Nota

Sin importar el modo que haya seleccionado, solo se permite **una respuesta** por usuario en una publicación. Sin embargo, es posible comentar varias veces.

Clasificación predeterminada: elija cómo se ordenan de forma predeterminada las preguntas.

> - Más reciente: por la fecha de publicación más reciente de una pregunta.
>     
> - Última actualización: por la fecha de actividad más reciente (se incluyen las respuestas y los comentarios).
>     
> - Más votada: por la cantidad más alta de votos.
>     
> - Relevancia: por la relevancia de la publicación (se determina por una fórmula).
>     
> - Respondida: por la probabilidad de recibir una respuesta (se determina por una fórmula).
>     

 Nota

Los usuarios tienen varias opciones de clasificación (respuestas totales, vistas totales, última actividad) en el frontend del foro.

Privacidad: seleccione Público para que cualquier persona pueda ver el foro, Inició sesión para que sea visible solo para los usuarios que iniciaron sesión o Algunos usuarios para que sea visible solo para un grupo de acceso de usuarios específicos si elige un grupo autorizado.

A continuación, configure las [ganancias de karma](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-karma-gains) y los [derechos relacionados con el karma](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-karma-related-rights).

### Puntos de karma[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#karma-points "Enlazar permanentemente con este título")

Los usuarios pueden recibir puntos de karma según sus diferentes interacciones en el foro y se pueden usar para determinar a qué funcionalidades del foro pueden acceder, desde poder votar en las publicaciones hasta obtener permisos de moderador. Además, se utilizan para establecer los [ranks](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-ranks) del usuario.

 Importante

- Los puntos de karma de un usuario se comparten entre todos los foros, cursos y otro contenido de un único sitio web de Odoo.
    
- Los usuarios de eLearning pueden recibir puntos de karma al [interactuar con el curso](https://www.odoo.com/documentation/17.0/es/applications/websites/elearning.html#elearning-karma) y por [completar pruebas](https://www.odoo.com/documentation/17.0/es/applications/websites/elearning.html#elearning-quiz).
    

#### Ganancias de karma[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#karma-gains "Enlazar permanentemente con este título")

Varias interacciones en el foro pueden sumar o restar puntos de karma.

|Interacción|Descripción|Ganancia de karma predeterminada|
|---|---|---|
|Hacer pregunta|Publicación de una pregunta.|2|
|Pregunta votada a favor|Otro usuario vota a favor de la pregunta que publicó.|5|
|Pregunta votada en contra|Otro usuario vota en contra de la pregunta que publicó.|-2|
|Respuesta votada a favor|Otro usuario vota a favor de la respuesta que publicó.|10|
|Respuesta votada en contra|Otro usuario vota en contra de la respuesta que publicó.|-2|
|Acepta una respuesta|Selecciona una respuesta publicada por otro usuario como la mejor.|2|
|Respuesta aceptada|Otro usuario selecciona la respuesta que publicó como la mejor.|15|
|Respuesta reportada|Otro usuario indica que alguna pregunta o respuesta que haya publicado está [reportada como ofensiva](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-moderation).|-100|

 Nota

Los nuevos usuarios reciben **tres puntos** al validar su dirección de correo electrónico.

Para modificar los valores predeterminados, vaya a Sitio web ‣ Configuración ‣ Foro: Foros, seleccione uno y vaya a la pestaña Ganancias de karma. Después, seleccione un valor para editarlo.

Si el valor es positivo (por ejemplo, `5`), el usuario recibirá ese número de puntos en su cuenta cada vez que la interacción ocurra en el foro seleccionado. En cambio, si el valor es negativo (por ejemplo, `-5`), el número de puntos disminuirá. Use `0` si una interacción no debe afectar las recompensas del usuario.

#### Derechos relacionados con el karma[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#karma-related-rights "Enlazar permanentemente con este título")

Para configurar el número de puntos de karma necesarios para acceder a las diferentes funcionalidades del foro, vaya a Sitio web ‣ Configuración ‣ Foro: Foros, seleccione uno y vaya a la pestaña Derechos relacionados con el karma. Después, seleccione un valor para editarlo.

 Advertencia

Debe tener cuidado al modificar algunas funcionalidades, como Editar todas las publicaciones, Bloquear todas las publicaciones, Eliminar todas las publicaciones, Moderar publicaciones y Desvincular todos los comentarios. Asegúrese de comprender las consecuencias de proporcionar acceso a _cualquier_ usuario que cumpla con los requisitos de karma establecidos.

|Funcionalidad|Descripción|Requisitos de karma predeterminados|
|---|---|---|
|Hacer preguntas|Publicar preguntas.|3|
|Responder preguntas|Publicar respuestas en preguntas.|3|
|Voto a favor|Votar a favor en preguntas o respuestas.|5|
|Voto en contra|Votar en contra de preguntas o respuestas.|50|
|Editar publicaciones propias|Editar sus preguntas o respuestas.|1|
|Editar cualquier tipo de publicación|Editar cualquier pregunta o respuesta.|300|
|Bloquear mis publicaciones|Cerrar sus preguntas o respuestas.|100|
|Bloquear cualquier tipo de publicación|Cerrar cualquier pregunta o respuesta.|500|
|Eliminar publicaciones propias|Eliminar sus preguntas o respuestas.|500|
|Eliminar cualquier tipo de publicación|Eliminar cualquier pregunta o respuesta.|1,000|
|Enlaces Nofollow|Si se encuentra por debajo del karma necesario, el atributo _nofollow_ indica a los motores de búsqueda que ignoren los enlaces que publica.|500|
|Aceptar una respuesta para sus propias preguntas|Seleccionar una respuesta como la mejor en las preguntas que publicó.|20|
|Aceptar una respuesta para todas las preguntas|Seleccionar una respuesta como la mejor en cualquier pregunta.|500|
|Funciones del editor: imagen y enlaces|Agregar enlaces e imágenes a sus publicaciones.|30|
|Comentar sus publicaciones|Publicar comentarios en sus preguntas o respuestas.|1|
|Comentar todo tipo de publicaciones|Publicar comentarios en cualquier pregunta o respuesta.|1|
|Convertir las respuestas propias en comentarios y viceversa|Convertir los comentarios que publicó a respuestas.|50|
|Convertir respuestas en comentarios y viceversa|Convertir cualquier comentario en respuesta.|500|
|Desvincular sus propios comentarios|Eliminar sus comentarios.|50|
|Desvincular todos los comentarios|Eliminar cualquier comentario.|500|
|Hacer preguntas sin validación|No es necesario [validar](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-moderation) primero las preguntas que publique.|100|
|Marcar una publicación como ofensiva|Marcar una pregunta o respuesta como ofensiva.|500|
|Moderar publicaciones|Acceder a todas las [herramientas de moderación](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-moderation).|1,000|
|Cambiar las etiquetas de la pregunta|Cambiar las [etiquetas](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-tags) de las preguntas publicadas (si tiene permisos de edición).|75|
|Crear nuevas etiquetas|Crear nuevas [etiquetas](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-tags) al publicar preguntas.|30|
|Mostrar biografía detallada del usuario|Cuando un usuario pasa el ratón sobre su avatar o nombre de usuario, un cuadro emergente mostrará sus puntos de karma, biografía y número de [insignias](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-badges) por nivel.|750|

 Truco

Lleve seguimiento de las actividades relacionadas con el karma y agregue o elimine karma manualmente al [activar el modo de desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode). Vaya a Ajustes ‣ Herramientas de ludificación ‣ Rastreo del karma.

### Gamificación[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#gamification "Enlazar permanentemente con este título")

Los rangos e insignias son útiles para fomentar la participación. Los rangos toman en cuenta el total de los [puntos de karma](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-karma), mientras que las insignias se pueden otorgar manual o automáticamente al completar los desafíos.

#### Rangos[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#ranks "Enlazar permanentemente con este título")

Para crear nuevos rangos o modificar los predeterminados, vaya a Sitio web ‣ Configuración ‣ Foro: Rangos y haga clic en Nuevo o seleccione uno que ya existe.

Agregue el nombre de rango, el karma necesario para pertenecer a él, su descripción, un mensaje motivacional para animar a los usuarios a alcanzarlo y una imagen.

![Rangos predeterminados en el foro](https://www.odoo.com/documentation/17.0/es/_images/ranks.png)

#### Insignias[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#badges "Enlazar permanentemente con este título")

Para crear nuevas insignias o modificar las predeterminadas, vaya a Sitio web ‣ Configuración ‣ Foro: Insignias y haga clic en Nuevo o seleccione una que ya existe.

Escriba el nombre y la descripción de la insignia, agregue una imagen y configúrela.

##### Asignar de forma manual[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#assign-manually "Enlazar permanentemente con este título")

Si la insignia se debe otorgar manualmente, seleccione qué usuarios pueden otorgarla. Seleccione una de las siguientes opciones para la concesión a otorgar:

- Todos: todas aquellas personas que no utilizan el portal (puesto que las insignias se otorgan desde el backend).
    
- Una lista de usuarios seleccionados: los usuarios seleccionados con Usuarios autorizados.
    
- Personas que tienen algunas insignias: los usuarios a quienes se les ha otorgado una insignia en Insignias requeridas.
    

Tiene la opción de restringir la cantidad de veces al mes en las que cada usuario puede otorgar una insignia al activar la opción Aportación mensual limitada a y escribiendo un Número de limitación.

##### Asignar de forma automática[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#assign-automatically "Enlazar permanentemente con este título")

Si la insignia debe otorgarse de manera **automática** cuando se cumplen ciertas condiciones, seleccione la opción Nadie, se asigna mediante los desafíos en Concesión a otorgar.

Después, determine cómo debe otorgarse la insignia haciendo clic en Agregar en la sección Recompensas de desafíos. Seleccione un desafío para agregarla o cree uno haciendo clic en Nuevo.

 Truco

Puede darle a la insignia un Nivel de insignia del foro (Bronce, Plata, Oro) para darle más o menos importancia.

![Insignias predeterminadas del foro](https://www.odoo.com/documentation/17.0/es/_images/badges.png)

### Etiquetas[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#tags "Enlazar permanentemente con este título")

Los usuarios pueden usar etiquetas para filtrar las publicaciones del foro.

Para gestionar las etiquetas, vaya a Sitio web ‣ Configuración ‣ Foro: Etiquetas. Haga clic en Nuevo para crear una etiqueta y seleccionar el Foro relacionado.

 Truco

- Use la sección de Etiquetas en la barra lateral de foro para filtrar todas las preguntas asignadas a la etiqueta seleccionada. Haga clic en Ver todo para mostrar todas las etiquetas.
    
- Puede crear nuevas etiquetas al publicar un mensaje nuevo, si es que el usuario tiene suficientes [puntos de karma](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-karma-related-rights).
    

## Usar un foro[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#use-a-forum "Enlazar permanentemente con este título")

 Nota

El acceso a varias funciones depende de los [puntos de karma](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-karma-related-rights) que tenga un usuario.

### Publicar preguntas[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#post-questions "Enlazar permanentemente con este título")

Para crear una nueva publicación, acceda al foro desde el frontend, haga clic en Nueva publicación y complete la siguiente información:

- Título: agregue una pregunta o el tema de la publicación.
    
- Descripción: agregue una descripción para la pregunta.
    
- Etiquetas: agregue hasta cinco [etiquetas](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#forum-tags).
    

Haga clic en Publicar pregunta.

### Interactuar con las publicaciones[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#interact-with-posts "Enlazar permanentemente con este título")

Puede aplicar diferentes acciones en una publicación.

- Marque una pregunta como **favorita** haciendo clic en el botón de estrella (☆).
    
- Sigua una publicación y reciba **notificaciones** (por correo o dentro de Odoo) cuando alguien responda, haciendo clic en el botón de campana (🔔).
    
- **Vote** **a favor** (flecha hacia arriba ▲) o **en contra** (flecha hacia abajo ▼) de una pregunta o respuesta.
    
- Marque una respuesta como la **mejor** haciendo clic en el botón de la palomita (✔). Esta opción solo está disponible si el Modo del foro está establecido en Preguntas.
    
- Responder una pregunta.
    
- **Comente** una pregunta o respuesta haciendo clic en el botón de la burbuja de conversación (💬).
    
- **Comparta** una pregunta en Facebook, Twitter o LinkedIn haciendo clic en el botón de _compartir nodos*_.
    

Haga clic en el botón de elipsis (…) para:

> - Editar una pregunta o respuesta.
>     
> - Cerrar una pregunta.
>     
> - Eliminar una pregunta, respuesta o comentario. Puede Deshacer la acción de eliminar la pregunta después.
>     
> - Marcar una pregunta o respuesta como ofensiva.
>     
> - Convertir un comentario en respuesta.
>     
> - Ver el [Ticket de soporte](https://www.odoo.com/documentation/17.0/es/applications/services/helpdesk/overview/help_center.html#helpdesk-forum), relacionado, si es que existe.
>     

![Acciones de las publicaciones](https://www.odoo.com/documentation/17.0/es/_images/post-actions.png)

 Nota

De manera predeterminada, se requieren de 150 puntos de karma para ver el perfil de otro usuario. Este valor se puede configurar al crear un nuevo sitio web.

## Moderar un foro[](https://www.odoo.com/documentation/17.0/es/applications/websites/forum.html#moderate-a-forum "Enlazar permanentemente con este título")

Desde el frontend del foro, la sección Herramientas de moderación de la barra lateral, reúne todas las funciones esenciales para moderar.

![Herramientas de moderación de la barra lateral del foro](https://www.odoo.com/documentation/17.0/es/_images/moderation-tools.png)

Por validar: acceda a todas las preguntas y respuestas que esperan validación antes de que aparezcan en la pantalla de los no moderadores.

![Preguntas por validar](https://www.odoo.com/documentation/17.0/es/_images/to-validate.png)

 Nota

Una pregunta está pendiente de validarse si un usuario no tiene el karma requerido. El usuario no podrá publicar preguntas o respuestas mientras espera la validación. Solo se permite una pregunta pendiente de validación por usuario por foro.

Marcado: acceda a todas las preguntas y respuestas que se marcaron como ofensivas. Haga clic en Aceptar para quitar la bandera de ofensivo o en Ofensivo para confirmarlo. Luego seleccione una razón y haga clic en Marcar como ofensivo. Los usuarios que no tengan derechos de moderador no podrán ver la publicación y se le restarán 100 puntos de karma al conteo del usuario que lo publicó.

![Selección de la razón ofensiva](https://www.odoo.com/documentation/17.0/es/_images/offensive-reason.png)

Cerrada: acceda a todas las preguntas que se cerraron. Puede Eliminar o Reabrir las preguntas que desee. Para cerrar una pregunta, ábrala y haga clic en el botón de elipsis (…), luego en Cerrar, seleccione una Razón de cierre y haga clic en Cerrar publicación. La publicación ya no será visible para los usuarios que no tengan derechos de moderador.

 Nota

Si selecciona Es spam o publicidad o Es ofensiva o malintencionada como la razón de cierre, se le restarán 100 puntos de karma al conteo de la persona que hizo la publicación.

 Truco

- Cree o edite las razones de cierre en Sitio web ‣ Configuración ‣ Foro: Razones de cierre de la publicación. Seleccione Básico como Tipo de razón si la razón debe usarse al cerrar una pregunta y Ofensivo si debe usarse para marcar publicaciones.
    
- Gestione todas las publicaciones en Sitio web ‣ Configuración ‣ Foro: Foros, seleccione el foro y haga clic en el botón inteligente de Publicaciones. Al hacer clic en el botón de Acciones, puede Exportar, Archivar, Desarchivar, o Eliminar una o varias publicaciones.