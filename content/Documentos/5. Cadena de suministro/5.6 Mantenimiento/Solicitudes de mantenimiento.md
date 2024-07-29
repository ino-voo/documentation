Para que los equipos y los centros de trabajo funcionen correctamente, a menudo es necesario realizar tareas de mantenimiento en ellos. Esto puede incluir el mantenimiento preventivo, destinado a evitar que los equipos se averíen, o el mantenimiento correctivo, que se utiliza para arreglar equipos averiados o inutilizables por cualquier otro motivo.

En la aplicación _Mantenimiento_ de Odoo los usuarios pueden crear _solicitudes de mantenimiento_ para programar y rastrear el progreso de equipos y mantenimiento del centro de trabajo.

## Crear solicitudes de mantenimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_requests.html#create-maintenance-request "Enlazar permanentemente con este título")

Para crear una nueva solicitud de mantenimiento, vaya a aplicación de Mantenimiento ‣ Mantenimiento ‣ Solicitudes de mantenimiento y haga clic en Nuevo.

Llene el formulario con un título descriptivo en el campo Solicitud (por ejemplo, `El taladro no funciona`).

El campo Creado por se llena automáticamente con el usuario que crea la solicitud, pero se puede seleccionar otro usuario haciendo clic en el menú desplegable.

En el menú desplegable Para, seleccione Equipo si la solucitud de mantenimiento se crea desde una pieza de equipo, o Centro de trabajo si se crea para un centro de trabajo.

Dependiendo de la opción seleccionada en el campo Para, el siguiente campo se titula ya sea Equipo o Centro de trabajo. Con el menú desplegable para cualquiera de los campos, seleccione una pieza de equipo o un centro de trabajo.

Si la opción _Hojas de trabajo personalizadas de mantenimiento_ está activada en la configuración de la aplicación _Mantenimiento_, aparecerá un campo Plantilla de hoja de trabajo debajo del campo Equipo o Centro de trabajo. Si es necesario, utilice este campo para seleccionar una hoja de trabajo que rellenará el empleado que realiza el mantenimiento.

El siguiente campo es Fecha de solicitud y la fecha que aparece de forma predeterminada es la fecha de creación de la solicitud de mantenimiento. El usuario no puede cambiarla.

En el campo Tipo de mantenimiento seleccione la opción Correctivo si la solicitud es para solucionar un problema existente, o la opción Preventivo si la solicitud es para prevenir que ocurran problemas en el futuro.

Si la solicitud se crea para solucionar un problema que surgió durante una orden de fabricación específica, selecciónelo en el campo Orden de fabricación.

Si se seleccionó una [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_requests.html#id1) en el campo Orden de fabricación, aparecerá un campo de orden de trabajo debajo. Si un problema surge durante una orden de trabajo específica, dígalo en este campo.

En el campo Equipo especifique el equipo de mantenimiento responsable de gestionar la solicitud. Si un miembro específico del equipo es el responsable, selecciónelo en el campo Responsable.

El campo Fecha programada se usa para especificar la fecha en la que se debe llevar a cabo un mantenimiento y la hora en la que debe empezar. Para seleccionar una fecha haga clic en el campo para abrir un calendario en una ventana emergente y después seleccione un día en el calendario. Ingrese la hora y los minutos en los dos campos debajo del calendario y haga clic en Aplicar para guardar la fecha y la hora.

El campo Duración se utiliza para especificar el tiempo que se tarda en completar la solicitud de mantenimiento. Utilice el campo de entrada de texto para introducir la hora en formato `00:00`.

Si se selecciona Centro de trabajo en el campo para, aparecerá una casilla de verificación Bloquear centro de trabajo debajo del campo Duración. Active la casilla de verificación para evitar que se programen órdenes de trabajo u otro tipo de mantenimiento en el centro de trabajo especificado mientras se procesa la solicitud de mantenimiento.

El campo Prioridad se utiliza para comunicar la importancia (o urgencia) de la solicitud de mantenimiento. Asigne a la solicitud una prioridad entre cero y tres ⭐⭐⭐ (estrellas), haciendo clic en el número de estrella deseado. Las solicitudes a las que se asigna una prioridad más alta aparecen por encima de las que tienen una prioridad más baja, en el tablero Kanban utilizado para seguir la progresión de las solicitudes de mantenimiento.

En la pestaña Notas de la parte inferior del formulario, introduzca cualquier detalle relevante sobre la solicitud de mantenimiento (por qué surgió el problema de mantenimiento, cuándo se produjo, etc.).

La pestaña Instrucciones se utiliza para incluir instrucciones sobre cómo debe realizarse el mantenimiento. Seleccione una de las tres opciones y después incluya las instrucciones como se detalla a continuación:

- PDF: haga clic en el botón Subir el archivo para abrir el gestor de archivos y después seleccione un archivo para subir.
    
- Google Slid: ingrese el enlace a Google Slide en el campo de entrada de texto que aparece después de que se selecciona la opción.
    
- Texto: ingrese las instrucciones en el campo de entrada de texto que aparece después de que se selecciona la opción.
    

![Un formulario de solicitud de mantenimiento llenado para una pieza de equipo.](https://www.odoo.com/documentation/17.0/es/_images/request-form.png)

## Procesar una solicitud de mantenimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_requests.html#process-maintenance-request "Enlazar permanentemente con este título")

Una vez que se ha creado una solicitud de mantenimiento aparecerá en la etapa _Nueva solicitud_ de la página _Solicitudes de mantenimiento_, a la que puede ingresar desde la aplicación Mantenimiento ‣ Mantenimiento ‣ Solicitudes de mantenimiento.

Las solicitudes de mantenimiento se pueden mover a etapas diferentes, solo tiene que arrastrarlas y soltarlas. También puede hacer clic en una solicitud para abrirla en una nueva página, después seleccione la etapa deseada en la barra de indicador ubicada en la esquina superior derecha del formulario de solicitud.

Las solicitudes de mantenimiento exitosas deberían moverse a la etapa Reparado, para indicar que el equipo o el centro de trabajo ya se reparó.

Las solicitudes de mantenimiento falladas se deberían mover a la etapa Desechar, para indicar que el equipo o centro de trabajo no pudo repararse, por lo que debe desecharse.