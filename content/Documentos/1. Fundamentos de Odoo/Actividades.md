Las _Actividades_ son tareas de seguimiento vinculadas a un registro en una base de datos de Odoo.

El icono que se usa para mostrar las actividades depende del [tipo de actividad](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-types):

- Icono  (reloj): icono predeterminado para las actividades.
    
- Icono  (teléfono): hay una llamada telefónica programada.
    
- Icono  (sobre): hay un correo electrónico programado.
    
- Icono  (marca de verificación): hay una actividad pendiente programada.
    
- Icono  (varias personas): hay una reunión programada.
    
- Icono  (subir): hay un documento que se debe subir.
    
- Icono  (solicitud de firma): hay una solicitud de firma programada.
    

## Planear actividades[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#schedule-activities "Enlazar permanentemente con este título")

Las actividades se pueden programar en cualquier página de la base de datos que contenga un hilo de [chatter](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-chatter), una [vista de kanban](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-kanban), [lista de vista](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-list), o [vista de actividades](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-activity) de una aplicación.

### Chatter[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#chatter "Enlazar permanentemente con este título")

Las actividades se pueden crear desde el chatter de cualquier registro.

Para programar una actividad, haga clic en el botón Actividades ubicado en la parte superior del chatter de cualquier registro. En la ventana emergente Programar actividad, [llene el formulario para programar una actividad](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-form).

![Formulario para un nuevo tipo de actividad.](https://www.odoo.com/documentation/17.0/es/_images/chatter.png)

### Vista de kanban[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#kanban-view "Enlazar permanentemente con este título")

Las actividades también se pueden crear desde la vista de kanban .

Para ello, haga clic en el icono de reloj ubicado en la parte inferior de un registro.

Haga clic en + Programar una actividad y después [llene el formulario de Actividad programada](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-form).

![Vista kanban de un flujo de CRM y la opción para planear una actividad.](https://www.odoo.com/documentation/17.0/es/_images/schedule-kanban-activity.png)

 Nota

Si un registro ya tiene una actividad programada, el icono con forma de reloj cambiará por un icono que represente a la actividad que se programó. Para programar otra solo haga clic en el icono del tipo de actividad.

### Vista de lista[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#list-view "Enlazar permanentemente con este título")

Las actividades también se pueden crear desde la vista de lista .

Si la columna Actividades está oculta haga clic en el icono  (ajustes) ubicado en la parte derecha de la fila superior para abrirla.

Después, haga clic en el icono de [|reloj|](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#id1) del registro al que agregará la actividad, después en + Programar una actividad y [complete el formulario correspondiente](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-form) que aparece.

 Nota

Si un registro ya tiene una actividad programada, el icono con forma de reloj cambiará por un icono que represente a la actividad que se programó. Para programar otra solo haga clic en el icono del tipo de actividad.

![Vista de lista de un flujo de CRM y la opción de planear una actividad.](https://www.odoo.com/documentation/17.0/es/_images/schedule-list-activity.png)

### Vista de actividad[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activity-view "Enlazar permanentemente con este título")

La mayoría de las aplicaciones en Odoo tienen una vista de _actividades_ disponible. Si está disponible, aparecerá un [|reloj|](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#id3) en la esquina superior derecha de la barra de menú principal junto con los otros iconos de opciones de vista.

Haga clic en el [|reloj|](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#id5) para abrir la vista de actividad.

![Menú superior derecho con el icono de actividades sobresaltado.](https://www.odoo.com/documentation/17.0/es/_images/activities.png)

En esta vista todas las actividades disponibles se enlistan en las columnas, mientras que las entradas horizontales representan los registros individuales.

Las actividades que aparecen en verde se deben realizar en una fecha en el futuro, las actividades que aparecen en naranja se deben realizar hoy y las actividades que aparecen en rojo son actividades retrasadas.

La barra de colores en cada columna representa registros de los tipos específicos de actividad y muestran un número en el que se indica cuántas actividades están programadas para ese tipo.

Si se programan varios tipos de actividades para un registro, un número aparece en la caja en el que se indica el número total de actividades programadas.

 Nota

Los colores de las actividades y la relación que tienen con la fecha limite se mantendrán igual en toda la base de datos de Odoo sin importar el tipo de actividad o de vista.

Para programar una actividad para un registro pase el cursor sobre el campo correspondiente, haga clic en el icono  (más) que aparece y [complete el formulario para programarla](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-form).

![Vista de actividad de un flujo de CRM y la opción de planear una actividad.](https://www.odoo.com/documentation/17.0/es/_images/activity-view.png)

### Formulario para programar actividad[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#schedule-activity-form "Enlazar permanentemente con este título")

Las actividades se pueden programar desde diferentes lugares, como el [chatter](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-chatter) de un registro, o desde una de varias vistas en una aplicación cuando estén disponibles: the [kanban](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-kanban), [lista](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-list), o [actividad](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-activity).

En el formulario ingrese:

- Tipo de actividad: seleccione el tipo de actividad con el menú desplegable. Las opciones predeterminadas son: Correo, Llamada, Reunión, o Por hacer. Es posible que tenga otras opciones disponibles dependiendo de las aplicaciones instaladas.
    
- Resumen: ingrese una descripción corta de la actividad, como `hablar sobre la propuesta`.
    
- Fecha de vencimiento: con la ventana emergente de calendario, seleccione la fecha límite de la actividad.
    
- Asignado a: este campo se llenará con el nombre del usuario actual por defecto. Para asignar a un usuario diferente para la actividad, selecciónelo con el menú desplegable.
    
- Notas: agregue cualquier información para la actividad en este campo.
    

Cuando termine de llenar la ventana emergente Programa actividad haga clic en uno de los siguientes botones:

- Abrir calendario: abre el calendario del usuario para agregar y programar la actividad.
    
    Haga clic en la fecha y la hora deseadas para la actividad y aparecerá una ventana emergente Nuevo evento. El resumen de la ventana emergente _Programar actividad_ llena el campo Título.
    
    Ingrese la información en la ventana emergente Nuevo evento, después haga clic en Guardar y cerrar para programarla. Una vez que la programe, la actividad se agrega al chatter en la sección actividades planeadas.
    
     Importante
    
    El botón Abrir calendario **solo** aparece si tipo de actividad está configurado a llamada o Reunión.
    
- Planear: programa la actividad y agrega la actividad al chatter en Actividades planeadas.
    
- Marcar como hecho: agrega los detalles de la actividad al chatter en la sección Hoy. La actividad no se planea y se marca automáticamente como hecha.
    
- ¡Hecho! Prepare el siguiente: agrega los detalles de la actividad al chatter en la sección Hoy. La actividad no se planea, sino que se marca automáticamente como hecha y aparece una nueva ventana emergente Programar actividad.
    
- Cancellar: descarta cualquier cambio hecho en la ventana emergente Programar actividad.
    

![Vista de los leads en CRM y la opción para planear una actividad.](https://www.odoo.com/documentation/17.0/es/_images/schedule-pop-up.png)

## Todas las actividades programadas[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#all-scheduled-activities "Enlazar permanentemente con este título")

Para ver la lista completa de las actividades organizadas por aplicación, haga clic en el icono de reloj ubicado en la esquina superior derecha en el menú del encabezado.

El número de actividades programadas aparecerá dentro de una burbuja roja en el icono de reloj.

Todas las actividades para cada aplicación se dividen más entre secciones secundarias para indicar dónde en la aplicación se debe completar la actividad. Cada sección secundaria enlista el número de actividades programadas que están Retrasadas, se deben hacer hoy, y están programadas para el Futuro.

 Example

En la aplicación _Tiempo personal_ una actividad se programa para hacerse en el tablero de _Todo el tiempo personal_ y seis actividades están programadas para hacerse en el tablero _asignaciones_.

Estas solicitudes aparecerán en dos listas separadas en el menú desplegable de todas las actividades: una se llamará `Tiempo personal` y la otra `Asignación de tiempo personal`.

![La lista de actividades que se puede acceder desde la barra de menú principal. Dos entradas para la aplicación Tiempo libre están resaltadas.](https://www.odoo.com/documentation/17.0/es/_images/activities-menu.png)

### Solicitar un documento[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#request-a-document "Enlazar permanentemente con este título")

La opción para Solicitar un documento está disponible en la parte inferior de la lita de [todas las actividades programadas](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-all), la opción para Solicitar un documento aparece. Haga clic en Solicitar un documento y aparecerá una ventana emergente de Solicitar un archivo.

En el formulario ingrese:

- Nombre del documento: eingrese el nombre del documento que está solicitando.
    
- Solicitar a: en el menú desplegable seleccione el usuario al que se le solicitará el documento.
    
- Fecha de vencimiento en: ingrese el valor numérico para indicar cuándo se debe entregar el documento. A un lado de este campo encontrará el campo Días, esta es la opción predeterminada, haga clic en ella para mostrar un menú desplegable. Desde la lista que aparezca podrá seleccionar la opción de tiempo que quiera desde la lista, estas opciones son Días, Semanas, o Meses.
    
- Espacio de trabajo: seleccione el [espacio de trabajo](https://www.odoo.com/documentation/17.0/es/applications/productivity/documents.html#documents-workspaces) específico al que se subirá el documento en el menú desplegable.
    
- Etiquetas: seleccione cualquier etiqueta que quiera del menú desplegable. Las etiquetas disponibles que se muestran dependen de las etiquetas configuradas para el Espacio de trabajo seleccionado.
    
- Mensaje: ingrese el mensaje para describir la solicitud de documento en este campo.
    

Cuando complete todos los campos, haga clic en Solicitar para enviar la solicitud de documento.

![El formulario para la solicitud de un archivo, con todos los campos llenos para solicitar un contrato.](https://www.odoo.com/documentation/17.0/es/_images/request-doc.png)

## Tipos de actividades[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activity-types "Enlazar permanentemente con este título")

Para ver los tipos de actividades que están configurados en la base de datos, vaya a la aplicación Ajustes ‣ sección de Conversaciones ‣ Actividades ‣ Tipo de actividades.

![Botón de tipo de actividades en la aplicación Ajustes en la sección Conversaciones.](https://www.odoo.com/documentation/17.0/es/_images/settings-activities-types.png)

Esto mostrará la página Tipos de actividad, donde podrá encontrar los tipos de actividad existentes.

 Truco

Las aplicaciones individuales tienen una lista de _tipos de actividad_ específicas para esta aplicación. Por ejemplo, para ver y editar las actividades disponibles en la aplicación _CRM_ debe ir a CRM ‣ Configuración ‣ Tipos de actividad.

![La lista de los tipos de actividades que ya están configurados y disponibles.](https://www.odoo.com/documentation/17.0/es/_images/activity-list.png)

### Editar tipos de actividades[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#edit-activity-types "Enlazar permanentemente con este título")

Para editar un [tipo de actividad](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-types) existente, haga clic en el tipo de actividad para cargar el formulario del tipo de actividad.

Haga los cambios deseados en el formulario del tipo de actividad. El formulario se guardará en automático, pero también puede guardarlo de forma manual en cualquier momento si hace clic en la opción Guardar de forma manual, que encontrará con el icono  (subir a la nube) que está en la esquina superior izquierda de la página.

### Cree un nuevo tipo de actividad[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#create-new-activity-types "Enlazar permanentemente con este título")

Para crear un nuevo [tipo de actividad](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-types) haga clic en Nuevo desde la página de Tipos de actividad para cargar un formulario en blanco de tipo de actividad.

Ingrese el Nombre para el tipo de actividad en la parte superior del formulario y después ingrese la siguiente información en el formulario.

#### Sección de ajustes de actividad[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activity-settings-section "Enlazar permanentemente con este título")

- Acción: seleccione una acción relacionada con este nuevo tipo de actividad desde el menú desplegable. Algunas acciones activarán comportamientos específicos después de que se programe una actividad, como:
    
    - Subir documento: si selecciona esta opción se agregará un enlace para subir un documento directamente a la actividad planeada en el chatter.
        
    - Llamada o Junta: si selecciona esta opción los usuarios tendrán la opción de abrir su calendario para seleccionar una fecha y hora para esta actividad.
        
    - Solicitar firma: si selecciona esta opción, se agregará de forma automática un enlace para abrir una ventana emergente de firma a la actividad del chatter. Esta opción necesita que se instale la aplicación _Firma electrónica_ de Odoo.
        
    
     Nota
    
    Los tipos de actividades disponibles dependen de las aplicaciones que tenga instaladas en la base de datos.
    
- Carpeta: seleccione una carpeta específica del [espacio de trabajo](https://www.odoo.com/documentation/17.0/es/applications/productivity/documents.html#documents-workspaces) en la que se debe de guardar el documento. Este campo **solo** aparece si selecciona como Acción la opción Subir documento.
    
    Seleccione la carpeta en la que se debe de guardar el documento con el menú desplegable.
    
- Usuario predeterminado: en el menú desplegable seleccione un usuario al que se le asignará de forma automática esta actividad cuando se programe este tipo de actividad. Si deja este campo en blanco, la actividad se le asignará al usuario que la cree.
    
- Resumen predeterminado: incluya una nota que se deba incluir siempre que se cree este tipo de actividad.
    
     Nota
    
    La información en los campos Usuario predeterminado y Resumen predeterminado se incluye en la actividad creada, pero puede alterar estos campos antes de que la actividad se programe o se guarde.
    
- Mantener como Hecho: marque esta casilla si quiere que las actividades que se marquen como `Hechas` sigan visibles en la [vista de actividades](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#activities-activity).
    
- Nota predeterminada: ingrese cualquier nota que deba aparecer con la actividad.
    

#### Sección de siguiente actividad[](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html#next-activity-section "Enlazar permanentemente con este título")

Es posible que se sugiera o incluso active otra oportunidad. Para hacerlo debe configurar la sección Siguiente actividad.

- Tipo de encadenamiento: desde el menú desplegable puede seleccionar ya sea Sugerir siguiente actividad o Activar la siguiente actividad. Dependiendo de la opción que seleccione, se mostrará ya sea el campo Sugerir o Activar.
    
     Nota
    
    El campo Tipo de encadenamiento **no** aparecerá si selecciona Subir documento en el campo Acción.
    
- Sugerir/Activar: este campo será Sugeror o Activar, según lo que seleccione en el Tipo de encadenamiento. Seleccione la actividad a recomendar o programar como seguimiento después del tipo de actividad desde el menú desplegable.
    
- Programar: configure cuándo se sugerirá o activará la siguiente actividad.
    
    Primero, ingrese el valor numérico en el que se indique cuándo se sugerirá o activará la siguiente actividad.
    
    A un lado de este campo encontrará el campo Días, esta es la opción predeterminada, haga clic en ella para mostrar un menú desplegable. Desde la lista que aparezca podrá seleccionar la opción de tiempo que quiera desde la lista, estas opciones son Días, Semanas, o Meses.
    
    Finalmente, con el menú desplegable seleccione si una actividad se programará o activará ya sea :guilabel:` después de la fecha límite de la actividad anterior` o :guilabel:` después de la fecha de finalización`.
    

![Un formulario de nueva Actividad con todos los campos llenos.](https://www.odoo.com/documentation/17.0/es/_images/new-activity.png)

 Ver también

- [Conversaciones](https://www.odoo.com/documentation/17.0/es/applications/productivity/discuss.html)
    
- [Uso de canales para la comunicación en equipo](https://www.odoo.com/documentation/17.0/es/applications/productivity/discuss/team_communication.html)
    
- [Utilizar actividades para los equipos de ventas](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html)