
Al final de una conversación de _Chat en vivo_, los clientes tienen la oportunidad de evaluar la calidad del soporte que recibieron del _operador_ de esta aplicación. Los clientes proporcionan calificaciones tan pronto como cierran la conversación, esto permite que los operadores reciban retroalimentación inmediata sobre su desempeño. Además, los clientes también tienen la oportunidad de compartir cualquier comentario final antes de salir de la ventana de chat.

## Calificar conversaciones del Chat en vivo[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/ratings.html#rate-live-chat-conversations "Enlazar permanentemente con este título")

Los clientes pueden finalizar una conversación de _Chat en vivo_ si hacen clic en la X que se encuentra ubicada en la esquina superior derecha de la ventana de chat. Después, se les solicita que seleccionen un icono que coincida con su nivel de satisfacción, cada uno representa una de las siguientes calificaciones:

> - **Satisfecho** - _carita feliz verde_
>     
> - **Neutral** - _carita neutral amarilla_
>     
> - **Inconforme** - _carita enojada roja_
>     

![Vista de la ventana de chat desde el lado del usuario en el Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/live-chat-ratings-faces.png)

 Nota

Cuando los clientes terminan una conversación, el campo marcado como Recibir una copia de esta conversación aparece debajo de los iconos de _calificación_. Los clientes pueden escribir su correo antes o después de enviar una calificación.

Si el cliente selecciona el icono relacionado a satisfecho (carita feliz), recibirán un mensaje de agradecimiento y un enlace para cerrar la conversación.

![Vista de la ventana de chat en vivo desde la percepción del cliente con un mensaje de agradecimiento.](https://www.odoo.com/documentation/17.0/es/_images/live-chat-thank-you.png)

Si el cliente selecciona el icono relacionado a neutral (carita amarilla) o a inconforme (carita triste), aparecerá un cuadro de texto. En esa sección, los clientes pueden agregar comentarios para explicar el motivo de su calificación. El operador de chat en vivo recibirá este mensaje junto con el icono de calificación.

![Vista de una ventana de chat desde la perspectiva del operador, se resalta una calificación en la aplicación Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/live-chat-ratings-operator-window.png)

## Publicar las calificaciones de los clientes[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/ratings.html#publish-customer-ratings "Enlazar permanentemente con este título")

Para publicar las calificaciones de un canal en el sitio web, primero diríjase al registro de un canal de chat en vivo. Vaya a la aplicación Chat en vivo y haga clic en la tarjeta kanban de ese equipo, después haga clic en el botón inteligente Ir al sitio web. Esta acción abrirá la página de estadísticas del canal de chat en vivo.

En la esquina superior derecha de la página, haga clic en el interruptor Sin publicar, este cambiará del estado anterior a Publicado.

![Vista de las calificaciones publicadas en portal para el Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/live-chat-ratings-unpublished.png)

 Nota

Las notas que el cliente envió con su calificación _no_ se publicarán en el sitio web, son para uso interno. En el sitio web solo aparece información general estadística sobre el desempeño de los operadores del _canal_.

### Agregar una página de calificaciones al sitio[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/ratings.html#add-ratings-page-to-site "Enlazar permanentemente con este título")

Una vez que se ha publicado la página de calificaciones, se tiene que agregar manualmente al sitio web. Para hacerlo, vaya al tablero principal de Odoo y abra la aplicación _Sitio web_ y luego :menuselection: Sitio –> Contenido –> Páginas`, y haga clic en Nuevo.

Esto abrirá una ventana emergente de Nueva página. En el campo Titulo de la página, escriba `livechat`. Esto será como la URL para la página web publicada.

 Importante

La URL _debe_ tener el nombre de `livechat` para que la base de datos lo reconozca y conecte la página de calificaciones. Después de que se publico la página, puede cambiar el título de la página después en el Menú de editor.

Haga clic en Crear y se abrirá una página web recién creada. El Editor de la página web aparecerá en el panel derecho.

La página mostrará los nombres de los Canales de chat en vivo cuyas páginas de calificación se han publicado. Del lado izquierdo del nombre del canal aparecerá un icono de una burbuja de diálogo, el cual podrán utilizar los usuarios para ir a la página de calificaciones para sus respectivos canales.

![Vista de la página web para las calificaciones del chat en vivo haciendo énfasis en el icono del canal.](https://www.odoo.com/documentation/17.0/es/_images/live-chat-published-icon.png)

Haga los cambio o adiciones que desee a la página y luego haga clic en Guardar ubicado en la esquina superior derecha del editor de la página. El panel lateral de editor se cerrará y la página web permanecerá en la pantalla.

Para publicar la página web de `livechat`, regrese a la lista de páginas web en Sitio ‣ Contenido ‣ Páginas. Haga clic en la casilla ubicada del lado izquierdo de `livechat` en la lista de páginas para seleccionar la página y resaltar la línea. Luego, haga clic en la casilla debajo de la columna llamada Publicado. Este campo con la casilla está resaltado en color blanco. Haga clic en la casilla una segunda vez para activar la casilla Publicado. La página web ya estará publicada.

![Vista de la lista de página de un sitio web con la casilla 'publicado' resaltada.](https://www.odoo.com/documentation/17.0/es/_images/live-chat-is-published.png)

Una vez que la página se añadió al sitio, las calificaciones están listas para publicarse de manera predeterminada. Sin embargo, las calificaciones manuales se pueden seleccionar manualmente para que el público no las vea. La calificación aún estará incluida en los reportes internos y los equipos internos todavía la podrá ver. Sin embargo, los visitantes del sitio web público y los usuarios del portal no tendrán acceso a ella.

Consulte la página [Ocultar calificaciones individuales](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/ratings.html#livechat-overview-hide-ratings) para obtener más información.

## Reporte de calificaciones del cliente[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/ratings.html#customer-ratings-report "Enlazar permanentemente con este título")

El reporte Calificaciones de los clientes (Chat en vivo ‣ Reportes ‣ Calificaciones de los clientes) muestra un resumen de las calificaciones recibidas en los tickets de soporte individuales, así como cualquier comentario adicional enviado junto a la calificación.

![Vista del reporte de calificaciones de cliente en la aplicación Chat en vivo de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/live-chat-ratings-report.png)

El reporte tiene la vista kanban de forma predeterminada, cada calificación está representada por una tarjeta diferente. Para cambiar de vista, haga clic en uno de los iconos de la esquina superior derecha de la pantalla. El reporte está disponible en vista de _lista_, _tabla dinámica_ y _gráfico_.

Haz clic en una calificación individual para consultar información adicional sobre la conversación y la calificación.

### Ocultar calificaciones individuales[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/ratings.html#hide-individual-ratings "Enlazar permanentemente con este título")

Las calificaciones están listas para publicarse de manera predeterminada. Sin embargo, las calificaciones manuales se pueden seleccionar manualmente para que el público no las vea. La calificación aún estará incluida en los reportes internos y los equipos internos todavía la podrá ver. Sin embargo, los visitantes del sitio web público y los usuarios del portal no tendrán acceso a ella.

Si desea ocultar una calificación, vaya a la aplicación Chat en vivo ‣ Reportes ‣ Calificaciones de clientes y haga clic en la tarjeta kanban de la calificación que desea ocultar. En la página de detalles de la calificación individual, marque la casilla Visible solo de forma interna.

![Vista de la página de detalles de una calificación individual con la opción 'visible solo de forma interna' marcada.](https://www.odoo.com/documentation/17.0/es/_images/live-chat-ratings-visible-internally.png)

 Ver también

- [Chat en vivo](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat.html)
    
- [Comandos y respuestas predefinidas](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/responses.html)
    
- [Sitio web](https://www.odoo.com/documentation/17.0/es/applications/websites/website.html)