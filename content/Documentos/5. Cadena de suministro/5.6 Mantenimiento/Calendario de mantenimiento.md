Es necesario que el equipo reciba mantenimiento de forma constante para evitar que los equipos tengan averías y causen bloqueos en los centros de trabajo. El mantenimiento correctivo oportuno para máquinas y herramientas que pueden descomponerse de manera inesperada, así como el mantenimiento preventivo para garantizar que se eviten estos problemas, son esenciales para que las operaciones en el almacén no se detengan y continúen sin problemas.

En la aplicación _Mantenimiento_ de Odoo, los usuarios pueden acceder al _calendario de mantenimiento_ para crear, programar y editar solicitudes de mantenimiento correctivo y preventivo. Esto les permitirá mantenerse al tanto de los equipos y centros de trabajo.

## Crear solicitudes de mantenimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_calendar.html#create-maintenance-request "Enlazar permanentemente con este título")

Es posible crear solicitudes de mantenimiento desde el _calendario de mantenimiento_. Para acceder al calendario, vaya a Mantenimiento ‣ Mantenimiento ‣ Calendario de mantenimiento.

Haga clic en cualquier parte del calendario para crear una nueva solicitud, esto abrirá la ventana emergente Nuevo evento. En el campo Nombre: deberá asignarle un título a la nueva solicitud.

![La ventana emergente de creación de nuevos eventos.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-new-event-popup.png)

Al hacer clic en el botón Crear de la ventana emergente se guarda la nueva solicitud sin tener que agregar detalles adicionales. Si desea cancelar la creación de la solicitud, haga clic en el botón correspondiente.

Haga clic en Editar para agregar más detalles y programar la solicitud en una fecha y hora específica.

Al hacer clic en Editar se abre un formulario de solicitud de mantenimiento vacío en el que podrá completar varios detalles sobre la solicitud.

### Editar las solicitudes de mantenimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_calendar.html#edit-maintenance-request "Enlazar permanentemente con este título")

En el campo Solicitud deberá asignarle un título. En el campo Creado por, con el menú despegable, seleccione al usuario que creó la solicitud. De forma predeterminada, este campo se completa en automático con el usuario que está creando la solicitud.

![Formulario para crear una nueva solicitud de mantenimiento.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-new-request-form.png)

En el campo Para, con el menú desplegable, seleccione si esta solicitud es para un equipo o un centro de trabajo.

 Nota

Si en el campo Para selecciona Centro de trabajo aparecerán otros dos campos en el formulario: Centro de trabajo y Bloquear centro de trabajo.

En el campo Centro de trabajo seleccione a qué centro de trabajo del almacén se aplicará esta solicitud de mantenimiento.

Si la casilla de la opción Bloquear centro de trabajo está seleccionada no podrá planificar órdenes de trabajo u otras solicitudes de mantenimiento en este centro de trabajo mientras esta solicitud esté activa.

Si en el campo Para selecciona Equipo, que es la opción predeterminada, seleccione la máquina o herramienta que necesita mantenimiento en el campo Equipo. Luego de seleccionar una pieza específica aparece el campo Categoría en color gris, allí aparece la _categoría de equipo_ a la que pertenece.

En el campo Plantilla de hoja de trabajo, haga clic en el menú desplegable para seleccionar una plantilla en caso de que sea necesaria. Estas plantillas están personalizadas y el empleado que realiza el mantenimiento podrá completarlas.

Abajo del campo Categoría aparece el campo Fecha de solicitud que muestra la fecha solicitada para el mantenimiento.

El campo Tipo de mantenimiento cuenta con dos botones de opción para seleccionar entre mantenimiento correctivo o preventivo.

El mantenimiento correctivo es para solicitudes que surgen de las necesidades que deben atenderse de inmediato (por ejemplo, equipo averiado), mientras que el mantenimiento preventivo es para solicitudes planificadas que evitarán averías en el futuro.

Si la solicitud está relacionada a una orden de fabricación específica, selecciónela en el campo Orden de fabricación.

Con el menú desplegable del campo Equipo seleccione el equipo de mantenimiento que realizará esta acción y en el campo Responsable seleccione al técnico responsable de la solicitud.

![Detalles completados del formulario de solicitud de mantenimiento.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-filled-out-form.png)

En el campo Fecha programada, haga clic en la fecha para abrir un calendario emergente. Ahí seleccione la fecha planificada del mantenimiento y haga clic en Aplicar para guardarla.

En el campo Duración escriba la cantidad de horas (en formato `00:00`) que está planeado que dure el mantenimiento.

En el campo Prioridad elija una que se encuentre entre una y tres ⭐⭐⭐ (estrellas), estas indican la importancia de la solicitud de mantenimiento.

Si se encuentra en un entorno multiempresa, en el campo Empresa, seleccione con el menú desplegable la empresa a la que pertenece esta solicitud de mantenimiento.

En la parte inferior del formulario hay dos pestañas: Notas e Instrucciones.

En la pestaña Notas escriba las notas internas, en caso de que sean necesarias, para el equipo o técnico asignado a la solicitud.

En la pestaña Instrucciones, en caso de que sean necesarias, seleccione alguno de los tres botones de opción para proporcionar instrucciones de mantenimiento al equipo o técnico asignado. Los métodos disponibles para esto son a través de PDF, Presentaciones de Google o texto.

![Opciones de la pestaña de instrucciones del formulario de solicitud de mantenimiento.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-instructions-tab.png)

## Elementos del calendario[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_calendar.html#calendar-elements "Enlazar permanentemente con este título")

El _calendario de mantenimiento_ proporciona varias vistas, funciones de búsqueda y filtros que ayudan a llevar seguimiento del progreso de solicitudes de mantenimiento que se encuentran activas y las que están programadas.

Las siguientes secciones describen los elementos presentes en varias vistas del calendario.

### Filtros y favoritos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_calendar.html#filters-and-favorites "Enlazar permanentemente con este título")

Para acceder al calendario, vaya a Mantenimiento ‣ Mantenimiento ‣ Calendario de mantenimiento.

Para agregar o eliminar filtros para ordenar la información en el _calendario de mantenimiento_, haga clic en el icono 🔻 (triángulo apuntando hacia abajo) que se encuentra del lado derecho de la barra de búsqueda ubicada en la parte superior de la página.

En el lado izquierdo del menú desplegable aparecen todos los filtros que los usuarios pueden utilizar. Los filtros Por hacer y Activo están seleccionados de forma predeterminada para que aparezcan todas las solicitudes abiertas.

 Truco

Para agregar un filtro predeterminado al calendario de mantenimiento haga clic en Agregar filtro personalizado en la sección Filtros del menú desplegable. Esta acción abrirá la ventana desplegable para agregar un filtro personalizado.

En esta ventana emergente configure las propiedades de la nueva regla para el filtro y una vez que haya terminado haga clic en Agregar.

En el lado derecho del menú desplegable aparecen los favoritos y las búsquedas que haya guardado como favoritas para consultarlas después.

![Sección de filtros favoritos en el menú desplegable.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-favorites-popover.png)

Para almacenar una búsqueda como favorita, primero deberá seleccionar los filtros correspondientes y luego haga clic en Guardar búsqueda actual. En el campo que aparece abajo del botón anterior deberá asignar un nombre para la búsqueda.

Abajo del nombre asignado aparecen dos opciones, puede guardar la búsqueda como el filtro predeterminado o como un filtro compartido.

Si selecciona Filtro predeterminado, esta búsqueda aparecerá de forma predeterminada cuando abra la vista de calendario.

Otros usuarios podrán usar el filtro si selecciona la opción Compartido.

Haga clic en Guardar cuando haya terminado. Al hacer clic, el filtro favorito aparecerá en la columna Favoritos y también aparecerá el icono ⭐ (estrella dorada) junto al nombre del filtro en la barra de búsqueda.

### Vistas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_calendar.html#views "Enlazar permanentemente con este título")

El calendario de mantenimiento está disponible en seis vistas distintas: calendario (es la vista predeterminada), kanban, lista, tabla dinámica, gráfico y actividad.

![Iconos de los distintos tipos de vista del calendario de mantenimiento.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-view-type-icons.png)

#### Vista de calendario[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_calendar.html#calendar-view "Enlazar permanentemente con este título")

La vista predeterminada al abrir el calendario de mantenimiento es la de calendario, pero hay varias opciones disponibles en este tipo de vista para ordenar y agrupar la información de las solicitudes de mantenimiento.

En la esquina superior izquierda de la página hay un menú desplegable configurado de forma predeterminada con semana. Al hacer clic en él aparecen diferentes periodos para visualizar el calendario, como día, mes y año. La opción Mostrar fines de semana también está seleccionada de forma predeterminada, si la desmarca no aparecerán en el calendario.

![Opciones de periodo en el menú desplegable del calendario.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-period-dropdown.png)

A la izquierda de este menú se encuentran los iconos ⬅️ (flecha izquierda) y ➡️ (flecha derecha) y al hacer clic en ellos, el calendario se mueve hacia atrás o hacia adelante según corresponda.

De forma predeterminada, en el menú desplegable está establecida la opción Semana y del lado derecho aparece el botón Hoy. Al hacer clic en el botón anterior restablecerá el calendario para ver la fecha actual.

En el lado derecho de la página hay una columna lateral con un calendario minimizado establecido en la fecha de hoy y una lista de técnicos en la que aparecen todos los _técnicos_ que en ese momento tienen solicitudes abiertas. Haga clic en el icono (panel) ubicado en la parte superior de esta barra lateral para abrirla o cerrarla.

 Nota

La lista de técnicos solo muestra si los técnicos están asignados a las solicitudes abiertas y, además, los técnicos solo aparecen si están configurados como los responsables en al menos **un** formulario de solicitud de mantenimiento.

#### Vista de kanban[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_calendar.html#kanban-view "Enlazar permanentemente con este título")

En la vista de kanban, todas las solicitudes de mantenimiento abiertas aparecen en columnas correspondientes a sus respectivas etapas del proceso de mantenimiento.

Cada solicitud de mantenimiento aparece en la respectiva tarjeta de su tarea y estas se pueden arrastrar y soltar en otras etapas del flujo de kanban.

Cada columna tiene su nombre (por ejemplo, En progreso) y al pasar el cursor por encima aparece el icono ⚙️ (engranaje). Al hacer clic en el icono ⚙️ (engranaje) abrirá una lista de opciones para esa columna: Plegar, Editar, Automatizaciones y Eliminar.

![Opciones de columna para la etapa en la vista de kanban.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-kanban-column.png)

Hacer clic en Plegar oculta la columna y su contenido.

Hacer clic en Editar abre la ventana desplegable Editar: (nombre de la etapa) con el nombre de etapa correspondiente y ahí puede editar los detalles de la columna. Las siguientes son las opciones que puede editar:

![Ventana emergente para editar la columna En progreso.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-edit-stage-popup.png)

- Nombre: el nombre de la etapa en el flujo de kanban.
    
- Plegada en el flujo de mantenimiento: cuando está seleccionada, la columna de esta etapa se pliega de forma predeterminada en el tipo de vista de kanban.
    
- Solicitud confirmada: cuando esta casilla no está seleccionada y el tipo de solicitud de mantenimiento es _Centro de trabajo_, entonces no se crea ninguna pausa en el respectivo centro de trabajo al crear una solicitud de mantenimiento. Si la casilla está seleccionada, el centro de trabajo se bloquea en automático por el tiempo establecido, ya sea en la fecha configurada o tan pronto como sea posible si el centro de trabajo no está disponible.
    
- Secuencia: el orden en el proceso de mantenimiento en el que aparece esta etapa.
    
- Solicitud lista: si esa casilla está seleccionada, indica que esta etapa es el paso final del proceso de mantenimiento. Las solicitudes que se mueven a esta etapa están cerradas.
    

Una vez que haya terminado haga clic en Guardar y cerrar. Si no hizo ningún cambio, haga clic en Desscartar o en el icono X para cerrar la ventana emergente.

#### Vista de lista[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_calendar.html#list-view "Enlazar permanentemente con este título")

La vista de lista muestra todas las solicitudes de mantenimiento abiertas en una lista con información sobre cada una en la fila correspondiente.

Las columnas de información que aparecen en este tipo de vista son las siguientes:

- Mantenimientos: el nombre asignado a la solicitud de mantenimiento.
    
- Empleado: el empleado que creó la solicitud de mantenimiento.
    
- Técnico: el técnico responsable de la solicitud de mantenimiento.
    
- Categoría: la categoría a la que pertenece el equipo que se está reparando.
    
- Etapa: la etapa del proceso de mantenimiento en que se encuentra la solicitud.
    
- Empresa: si se encuentra en un entorno multiempresa, la empresa de la base de datos a la que se asigna la solicitud.
    

#### Vista de tabla dinámica[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_calendar.html#pivot-view "Enlazar permanentemente con este título")

La vista de tabla dinámica muestra las solicitudes en una tabla y puede personalizarla para que aparezcan varias métricas.

Para agregar más datos a la tabla dinámica haga clic en el botón Medidas, esta acción abrirá un menú desplegable. La opción Número esta seleccionada de forma predeterminada. Las opciones adicionales para agregar a la tabla son Pausas adicionales por planear, Duración, y Repetir cada.

![Opciones de medidas en la página de la vista de tabla dinámica.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-measures-menu.png)

Del lado derecho del botón Medidas se encuentra el botón Insertar en hoja de cálculo. Al hacer clic en este botón abrirá la ventana emergente titulada Seleccione una hoja de cálculo para insertar su tabla dinámica.

Hay dos pestañas en esta ventana emergente, Hojas de cálculo y Tableros. Haga clic en una de ellas y seleccione una hoja de cálculo o un tablero de la base de datos para agregar esta tabla dinámica y después haga clic en Confirmar. Si no es necesario agregar esta tabla a una hoja de cálculo o un tablero haga clic en Cancelar o en el icono X para cerrar la ventana emergente.

Del lado derecho del botón Insertar en hoja de cálculo hay otros tres botones:

- Girar eje: gira los ejes x e y de la tabla dinámica.
    
- Expandir todo: todas las filas y columnas disponibles para la información de tabla dinámica se muestran por completo.
    
- Descargar xlsx: la información de la tabla dinámica se descarga como un archivo .xlsx
    

#### Vista de gráfico[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_calendar.html#graph-view "Enlazar permanentemente con este título")

Con la vista de gráfico seleccionada, aparecen las siguientes opciones entre la barra de búsqueda y la representación visual de los datos. Estas opciones específicas del gráfico se encuentran a la derecha de los botones Medidas e Insertar en hoja de cálculo.

![Iconos de tipo de gráfico en la página de la vista de gráfico.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-graph-view-icons.png)

Hay tres tipos distintos de gráficos disponibles para que los usuarios puedan ver los datos:

- Gráfico de barras: la información aparece en un gráfico de barras.
    
- Gráfico de líneas: la información aparece en un gráfico de líneas.
    
- Gráfico circular: la información aparece en un gráfico circular.
    

Al ver los datos en un gráfico de barras es posible darles el siguiente formato:

- Apilado: la información aparece apilada en el gráfico.
    
- Descendente: la información aparece en orden descendente.
    
- Ascendente: la información aparece en orden ascendente.
    

Al ver los datos en un gráfico de líneas es posible darles el siguiente formato:

- Apilado: la información aparece apilada en el gráfico.
    
- Acumulativo: los datos se acumulan de forma creciente.
    
- Descendente: la información aparece en orden descendente.
    
- Ascendente: la información aparece en orden ascendente.
    

Al ver los datos en un gráfico circular, todos los datos pertinentes aparecen forma predeterminada y no hay opciones de formato adicionales disponibles.

#### Vista de actividad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_calendar.html#activity-view "Enlazar permanentemente con este título")

En la vista de actividad todas las solicitudes de mantenimiento abiertas aparecen en su propia fila y es posible programar actividades relacionadas con ellas.

![Solicitudes de mantenimiento en la vista de actividad.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-activity-view-type.png)

Las solicitudes de mantenimiento aparecen en la columna Solicitud de mantenimiento como actividades. Al hacer clic en una solicitud abrirá la ventana emergente Solicitud de mantenimiento que indica el estado de la solicitud y el técnico responsable. Para programar una actividad desde ahí, haga clic en ➕ Programar actividad, esto abrirá la ventana emergente correspondiente.

En la ventana emergente, elija el tipo de actividad, proporcione un resumen, programe una fecha límite y elija el usuario responsable en el campo Asignada a.

![Ventana emergente para programar una actividad.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-schedule-activity-popover.png)

Escriba cualquier nota adicional para la nueva actividad en el espacio vacío dentro del campo Registre una nota… que aparece en gris. Al hacer clic, el mensaje cambia a Escriba «/» para acceder a los comandos.

Una vez que haya terminado, haga clic en Programar para programar la actividad. También puede hacer clic en Programar y marcar como hecho para cerrar la actividad, Hecho y programar siguiente para cerrar la actividad y abrir una nueva o en Cancelar para cancelarla.

La vista de actividad muestra los tipos de actividad disponibles en su propia columna al programar una. Estas columnas son Correo electrónico, Llamada, Reunión, Solicitud de mantenimiento, Actividades pendientes, Subir documento, Solicitar firma y Conceder aprobación.

Para programar una actividad con ese tipo en específico, haga clic en cualquier cuadro vacío de la fila correspondiente para la solicitud de mantenimiento deseada y haga clic en el icono ➕ (más). Esta acción abre la ventana emergente de Odoo en donde podrá programar la actividad.

![Ventana emergente Odoo para programar una actividad.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-calendar-odoo-activity-popup.png)

 Ver también

- [Solicitudes de mantenimiento](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_requests.html)
    
- [Agregar equipo nuevo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/add_new_equipment.html)