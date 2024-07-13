La aplicación _Chat en vivo_ de Odoo incluye varios reportes que permiten monitorear el rendimiento del operador e identificar las tendencias en las conversaciones de los clientes.

## Reportes disponibles[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#available-reports "Enlazar permanentemente con este título")

Los siguientes reportes se incluyen en la aplicación _Chat en vivo_:

- [Historial de sesiones](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#livechat-sessions-history)
    
- [Estadísticas de sesión](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#livechat-session-statistics)
    
- [Análisis de operador](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#livechat-operator-analysis)
    

 Nota

También puede acceder al _reporte de calificaciones del Chat en vivo_ a través del menú Reportes. Para más información sobre este reporte, y sobre el proceso de calificación del _Chat en vivo_, vea [Calificaciones del Chat en vivo](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/ratings.html).

Para acceder al menú desplegable con todos los reportes disponibles, vaya a la aplicación Chat en vivo ‣ Reportes.

### Historial de sesiones[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#sessions-history "Enlazar permanentemente con este título")

El reporte de _Historial de sesiones_ muestra un resumen de las sesiones del chat en vivo, incluyendo sus fechas, el nombre y país de los participantes, la duración de la sesión, el número de mensajes y la calificación. También brinda acceso a las transcripciones completas de las sesiones del chat en vivo.

Para acceder a este reporte, vaya a la aplicación Chat en vivo ‣ Reporte ‣ Historial de sesiones.

![Ejemplo de un reporte de Historial de sesiones desde la aplicación Chat en vivo.](https://www.odoo.com/documentation/17.0/es/_images/sessions-history.png)

Puede exportar la información de este reporte, o la puede insertar en una hoja de cálculo.

Haga clic en el icono ⚙️ (engranaje) en la página Historial, en la esquina superior derecha. Esto mostrará un menú desplegable.

Desde el menú desplegable, haga clic en Exportar todo para exportar todas las sesiones a una hoja de cálculo, o Insertar la lista en la hoja de cálculo para insertar en una hoja de cálculo nueva o existente.

Para solo exportar algunas sesiones, desde la vista de lista haga clic en la casilla de verificación a la izquierda de cada sesión individual para seleccionar las sesiones que desea exportar. Cuando haya seleccionado las sesiones, haga clic en el icono ⚙️ (engranaje) de acciones en la parte superior central de la página. Después, haga clic en Exportar o Insertar la lista en la hoja de cálculo.

Para ver la transcripción de una conversación individual, haga clic en cualquier parte de la línea de entrada. Esto abrirá un hilo de _Conversaciones_.

En el hilo de _Conversaciones_ se mostrará la transcripción completa de la conversación. En la parte superior de la conversación hay una lista de páginas web que el visitante vio antes de empezar la sesión de chat, además de las marcaciones de hora correspondientes. Si el visitante dejó una calificación, esta se incluirá al final de la transcripción.

![Imagen de la transcripción del chan en la aplicación Conversaciones.](https://www.odoo.com/documentation/17.0/es/_images/chat-transcript.png)

### Estadísticas de sesión[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#session-statistics "Enlazar permanentemente con este título")

El reporte _Estadísticas de sesión_ brinda un resumen estadístico sobre las sesiones del chat. La vista predeterminada para este reporte muestra las sesiones de chat en vivo agrupadas por fecha de creación.

Para acceder a este reporte, vaya a la aplicación Chat en vivo ‣ Reportes ‣ Estadísticas de sesión.

![Ejemplo de un reporte de Estadísticas de sesión desde la aplicación Chat en vivo.](https://www.odoo.com/documentation/17.0/es/_images/sessions-statistics.png)

La vista de gráfico de barras apiladas del reporte _Estadísticas de sesión_, con los resultados agrupados por Fecha de creación (hora) y, después, por calificación.[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#id1 "Enlace permanente a esta imagen")

Para ver una medida distinta, haga clic en el menú desplegable Medidas ubicado en la parte superior izquierda del reporte. Las medidas disponibles para este son:

- Número de participantes: número de participantes en una conversación.
    
- Días de actividad: número de días desde la primera sesión del operador.
    
- Duración de la sesión (min): la duración de una conversación en minutos.
    
- ¿El visitante es anónimo?: indica si el participante de la sesión es anónimo.
    
- Mensajes por sesión: el número total de mensajes que se envían a una conversación. Esta medida se incluye en la vista predeterminada.
    
- Calificación: la calificación que un operador recibió al final de una sesión, si es que el participante dejó una.
    
- Sesión sin calificar: indica si la sesión **no** recibió ninguna calificación al finalizar la conversación.
    
- Tiempo de respuesta (seg): el tiempo promedio, en segundos, que le lleva a un operador responder a una solicitud de chat.
    
- El visitante está satisfecho: muestra si la calificación fue positiva. Si el visitante dio una calificación dio una respuesta negativa o neutral, se considerarán como _insatisfechos_.
    
- Número: el número total de sesiones.
    

### Análisis de operador[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#operator-analysis "Enlazar permanentemente con este título")

El reporte de _Análisis de operador_ se usa para monitorear el rendimiento de operadores de chat en vivo individuales.

Para acceder a este reporte, vaya a la aplicación Chat en vivo ‣ Reportes ‣ Análisis de operador.

La vista predeterminada para este reporte es un gráfico de barras, que solo muestra conversaciones del mes actual, como lo indica el filtro de búsqueda predeterminado Este mes. Las conversaciones se agrupan por operador.

Para ver una medida distinta, haga clic en el menú desplegable Medidas ubicado en la parte superior izquierda del reporte. Las medidas disponibles para este son:

- Número de sesiones: el número de sesiones en las que un operador ha participado. Esta medida está incluida de forma predeterminada.
    
- Duración promedio: el promedio de cuánto dura una conversación en segundos
    
- Calificación promedio: la calificación promedio que recibe un operador.
    
- Tiempo de respuesta: el tiempo promedio antes de que un operador responsa una solicitud de chat, en segundos.
    
- Número: el número total de sesiones.
    

![Ejemplo de un reporte de Análisis de operador en la aplicación Chat en vivo.](https://www.odoo.com/documentation/17.0/es/_images/operator-analysis.png)

## Visualizar y filtrar opciones[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#view-and-filter-options "Enlazar permanentemente con este título")

En cualquier reporte de Odoo, las opciones de visualización y filtrado varían según los datos que se están analizando, midiendo y agrupando. A continuación encontrará más información sobre las vistas disponibles para los reportes del _Chat en vivo_.

 Nota

El reporte [Historial de sesiones](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#livechat-sessions-history) **solo** está disponible en vista de lista.

### Vista de tabla dinámica[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#pivot-view "Enlazar permanentemente con este título")

La vista _tabla dinámica_ presenta los datos de forma interactiva. Los reportes [Estadísticas de sesión](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#livechat-session-statistics) y [Análisis de operador](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#livechat-operator-analysis) están disponibles en esta vista.

Puede acceder a la vista de tabla dinámica en cualquier reporte, haga clic en el icono de tabla en la parte superior derecha de la pantalla.

Para agregar un grupo a una fila o columna, haga clic en el ➕ (signo más) junto a Total y luego seleccione uno de los grupos del menú desplegable que aparece. Para eliminar uno, haga clic en ➖ (signo menos) y desmarque la opción apropiada.

### Vista de gráfico[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#graph-view "Enlazar permanentemente con este título")

La vista de _gráfico_ muestra los datos en un gráfico de _barras_, _líneas_ o _circular_. Los reportes [Estadísticas de sesión](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#livechat-session-statistics) y [Análisis de operador](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#livechat-operator-analysis) están disponibles en esta vista.

Cambie a la vista de gráfico seleccionando el gráfico de líneas en la parte superior derecha de la pantalla. Para cambiar entre los diferentes gráficos, seleccione el icono que corresponde a la lista deseada en la parte superior izquierda del gráfico mientras se encuentra en esta vista.

 Truco

Tanto el gráfico de barras como el gráfico de líneas pueden utilizar la opción de _vista apilada_, esta presenta dos (o más) grupos de datos uno encima del otro, en lugar de uno junto al otro, facilitando así la comparación de datos.

### Guardar y compartir una búsqueda de favoritos[](https://www.odoo.com/documentation/17.0/es/applications/websites/livechat/reports.html#save-and-share-a-favorite-search "Enlazar permanentemente con este título")

La función de _Favoritos_ en los reportes permite que los usuarios guarden sus filtros más utilizados sin tener que reconstruirlos cada vez que los necesitan.

Para crear y guardar un filtro en la sección _Favoritos_ en el menú desplegable de la barra de búsqueda, siga los siguientes pasos:

1. Establezca los parámetros necesarios utilizando las opciones Filtros y Agrupar por disponibles en el menú desplegable de la barra de búsqueda y en el menú desplegable Medidas de la parte superior izquierda del reporte.
    
2. Haga clic en el icono 🔻(triángulo apuntando hacia abajo) situado junto a la barra de búsqueda para abrir el menú desplegable.
    
3. En el encabezado Favoritos , haga clic en Guardar búsqueda actual.
    
4. Renombre la búsqueda.
    
5. Seleccione Filtro predeterminado para que estos ajustes de filtro se muestren de forma automática cuando se abra el reporte. De lo contrario, no seleccione la casilla.
    
6. Seleccione Compartido para que este filtro esté disponible para los demás usuarios de la base de datos. Si esta casilla no está seleccionada, el filtro solo estará disponible para el usuario que la creó.
    
7. Haga clic en Guardar para conservar la configuración para su uso posterior.