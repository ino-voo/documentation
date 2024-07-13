Las _actividades_ son tareas de seguimiento vinculadas a un registro en una base de datos de _Odoo_. Estas se pueden programar desde cualquier página de la base de datos que tenga un hilo del chatter, una vista de kanban, una vista de lista o una vista de actividades de una aplicación.

![Información general de las actividades para leads y oportunidades en una base de datos de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/activities-view.png)

Actividades planificadas para leads y oportunidades.[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#id1 "Enlace permanente a esta imagen")

## Tipos de actividades[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#activity-types "Enlazar permanentemente con este título")

La aplicación _CRM_ cuenta con un varios tipos de actividad preconfigurados, para ver la lista vaya a CRM ‣ Configuración ‣ Tipos de actividad.

 Nota

Hay otros tipos de actividad disponibles en la base de datos y puede utilizarlos en diferentes aplicaciones. Para acceder a la lista completa de tipos de actividad, vaya a Ajustes, diríjase a la sección Conversaciones y haga clic en Tipos de actividad.

Los tipos de actividad preconfigurados para la aplicación _CRM_ son los siguientes:

> - Correo electrónico: agrega un recordatorio al chatter para indicarle al vendedor que debe enviar un correo electrónico.
>     
> - Llamada: abre un enlace de calendario donde el vendedor puede programar una hora para llamar al contacto.
>     
> - Reunión: abre un enlace de calendario donde el vendedor puede programar una hora para reunirse con el contacto.
>     
> - Por hacer: agrega una tarea de recordatorio general al chatter.
>     
> - Subir documento: agrega un enlace en la actividad donde es posible subir un documento externo. Tenga en cuenta que la aplicación _Documentos_ **no** es necesaria para utilizar este tipo de actividad.
>     

 Nota

Si instala otras aplicaciones, como _Ventas_ o _Contabilidad_, habrá otros tipos de actividad disponibles en la aplicación _CRM_.

### Crear un nuevo tipo de actividad[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#create-a-new-activity-type "Enlazar permanentemente con este título")

Para crear un nuevo tipo de actividad haga clic en el botón Nuevo ubicado en la parte superior izquierda de la página, esta acción abrirá un formulario vacío.

Primero, en la parte superior del formulario, elija un nombre para el nuevo tipo de actividad.

#### Ajustes de actividad[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#activity-settings "Enlazar permanentemente con este título")

##### Acción[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#action "Enlazar permanentemente con este título")

El campo _Acción_ especifica el propósito de la actividad. Algunas acciones activarán comportamientos específicos después de programar una actividad.

- Si selecciona Subir documento. se agregará un enlace para subir un documento directamente a la actividad planeada en el chatter.
    
- Si selecciona Llamada o Junta los usuarios tendrán la opción de abrir su calendario para agendar esta actividad.
    
- Si selecciona Solicitar firma se agregará un enlace en el chatter de la actividad planeada. Al hacer clic en este enlace se abrirá una ventana emergente para solicitar la firma.
    

![Los ajustes de la actividad de un nuevo tipo de actividad. El campo Acción aparece dentro de un recuadro rojo.](https://www.odoo.com/documentation/17.0/es/_images/action-field.png)

 Nota

Las acciones disponibles que puede seleccionar en el tipo de actividad varían dependiendo de las aplicaciones que tienen en la base de datos.

##### Usuario predeterminado[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#default-user "Enlazar permanentemente con este título")

Para asignar esta actividad a un usuario específico de manera automática al programar este tipo de actividad, seleccione un nombre desde el menú desplegable Usuario predeterminado. Si este campo se deja en blanco, se asignará una actividad al usuario que cree la actividad.

##### Resumen predeterminado[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#default-summary "Enlazar permanentemente con este título")

Para incluir notas al crear este tipo de actividad debe ingresarlas en el campo Resumen predeterminado.

 Nota

La información en los campos Usuario predeterminado y Resumen predeterminado se incluye en la actividad creada, pero puede alterar estos campos antes de que la actividad se programe o se guarde.

#### Siguiente actividad[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#next-activity "Enlazar permanentemente con este título")

Para sugerir o activar una actividad de manera automática después de que una actividad se marca como completada, se debe configurar el Tipo de encadenamiento.

##### Sugerir la siguiente actividad[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#suggest-next-activity "Enlazar permanentemente con este título")

En el campo Tipo de encadenamiento seleccione Sugerir siguiente actividad. Al hacerlo, el campo de abajo cambiará a Sugerir. Haga clic en este campo para seleccionar las actividades que recomienda como actividades que le sigan a este tipo de actividad.

![La sección Siguiente actividad en un formulario de nuevo tipo de actividad.](https://www.odoo.com/documentation/17.0/es/_images/next-activity.png)

En el campo Horario seleccione una fecha límite predeterminada para estas actividades. Para hacerlo, configure un número específico de Días, Semanas, o Meses. Después, decida si debe pasar después de la fecha de finalización o después de la fecha límite de actividad anterior.

Puede alterar la información del campo Horario antes de agendar la actividad.

Al completar todas las configuraciones, haga clic en Guardar.

 Nota

Si una actividad tiene el Tipo de encadenamiento configurado como Sugerir siguiente actividad y tiene actividades enlistadas en el campo Sugerir, los usuarios obtendrán recomendaciones de actividades que pueden ser el siguiente paso.

![Una ventana emergente de actividades programadas. Las actividades recomendadas aparecen dentro de un recuadro rojo.](https://www.odoo.com/documentation/17.0/es/_images/suggest-next-activity.png)

##### Activar la siguiente actividad[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#trigger-next-activity "Enlazar permanentemente con este título")

Si configura el Tipo de encadenamiento a Activar siguiente actividad hara que la siguiente actividad se active de inmediato una vez que la actividad previa se termine.

Si selecciona Activar la siguiente actividad en el campo Tipo de encadenamiento, el campo de abajo cambiará a Activador. Desde el menú desplegable del campo Activador seleccione la actividad que se debería iniciar una vez que esta actividad se complete.

En el campo Horario seleccione una fecha límite predeterminada para estas actividades. Para hacerlo, configure un número específico de Días, Semanas, o Meses. Después, decida si debe pasar después de la fecha de finalización o después de la fecha límite de actividad anterior.

Puede alterar la información del campo Horario antes de agendar la actividad.

Al completar todas las configuraciones, haga clic en Guardar.

 Nota

Cuando el tipo de encadenamiento de una actividad es Activar la siguiente actividad, al marcar la actividad como _Lista_, la siguiente actividad que aparece en el campo Activar iniciará de inmediato.

## Seguimiento de actividades[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#activity-tracking "Enlazar permanentemente con este título")

Para mantener el flujo actualizado con la vista más precisa del estado de las actividades, tan pronto como se interactúe con un lead, es necesario que marque la actividad asociada como _Hecho_. Esto garantiza que pueda programar la siguiente actividad según sea necesario y también evita que el flujo se sature con actividades vencidas.

El flujo es más efectivo cuando está actualizado y en orden con las interacciones que está rastreando.

## Planes de actividades[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#activity-plans "Enlazar permanentemente con este título")

Los _Planes de actividad_ son secuencias de actividades preconfiguradas. Cuando un plan de actividad inicia, toda actividad en la secuencia se programa de forma automática.

Para crear un nuevo plan, vaya a la aplicación CRM ‣ Configuración ‣ Plan de actividad. Haga clic en Nuevo en la parte superior izquierda de la página para abrir un formulario de Planes de leads en blanco.

En el campo Nombre del plan ingrese el nombre para el plan nuevo. En la pestaña Actividades por crear haga clic en Agregar una línea para agregar una actividad nueva.

Seleccione un Tipo de actividad desde el menú desplegable. Haga clic en Buscar más para ver la lista completa de tipos de actividades disponibles, o para crear [uno nuevo](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#crm-create-new-activity-type).

Después, en el campo Resumen ingrese varios detalles para describir los específicos de una actividad, incluyendo las instrucciones para el vendedor o la información que se debe dar al completar la actividad. El contenido de este campo se incluyen con la actividad programada y los puede editar cuando quiera.

En el campo Asignación seleccione una de las siguientes opciones:

> - Preguntar en el lanzamiento: las actividades se asignan a un usuario cuando el plan se programe.
>     
> - Usuario predeterminado: las actividades siempre se asignan a un usuario en específico.
>     

Si selecciona Usuario predeterminado en el campo Asignación, seleccione un usuario en el campo Asignado a.

 Truco

> Los planes de actividades pueden incluir actividades asignadas a un usuario predeterminado y usuarios que se indican al lanzamiento.

![Un formulario de plan de led con actividades programadas.](https://www.odoo.com/documentation/17.0/es/_images/create-activity-plan.png)

Después, configure la línea de tiempo de la actividad. Las actividades se pueden programar para que sucedan ya sea antes o después de la fecha de planeación. Use los campos Intervalo y Unidades para configurar una fecha límite para esta actividad. Finalmente, en el campo Activar seleccione si la actividad debe suceder antes o después de la fecha planeada.

 Example

Un plan de actividad se crea sobre todo para gestionar leads de alta prioridad, específicamente, leads a los que se debería contactar rápido y se debe planear una junta dentro de los próximos días para el primer contacto. El plan se configura con las siguientes actividades:

- Enviar correo electrónico dos días **antes** de la fecha planeada.
    
- Junta cero días **antes** de la fecha pleneada
    
- Hacer una cotización tres días **después** de la fecha planeada
    
- Subir documento tres días **después** de la fecha planeada
    
- Dar seguimiento cinco días **después** de la fecha planeada
    

Esto hará que la _fecha planeada_ sea la fecha límite de una junta, que es el objetivo del plan. Antes de esa fecha, hay un tiempo de tolerancia para contactar al cliente y preparar la junta. Después de esa fecha, el vendedor tiene tiempo para crear una cotización, subir el documento y hacer el seguimiento.

Repita estos pasos para cada actividad que se incluya en el plan.

### Iniciar un plan de actividad[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#launch-an-activity-plan "Enlazar permanentemente con este título")

Para iniciar un plan de actividad en una oportunidad de _CRM_ vaya a la aplicación CRM y haga clic en la tarjeta de kanban de la oportunidad para abrirla.

En la parte superior derecha del chatter, haga clic en Actividades para abrir la ventana emergente de Planear actividad.

En el campo Plan, seleccione el plan de actividad que quiere iniciar, así generará un Resumen del plan en el cual se enlistarán las actividades que se incluyen en el plan. Seleccione una Fecha del plan usando el calendario que se muestra para actualizar el Resumen del plan con las fechas límites según los intervalos configurados en el [plan de actividad.](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/utilize_activities.html#crm-activity-plans).

Seleccione un usuario en el campo Asignado a. A este usuario se le asignará cualquiera de las actividades en el plan que esté configurado con Preguntar en el lanzamiento en el campo Asignación.

![La ventana emergente para programar una actividad con el plan de actividad seleccionado.](https://www.odoo.com/documentation/17.0/es/_images/schedule-activity-plan.png)

Haga clic en Programar.

Además de que los detalles del plan se agregarán a cada una de las actividades, también se agregarán al chatter.

![El hilo de chatter de una oportunidad CRM con un plan de actividad iniciado.](https://www.odoo.com/documentation/17.0/es/_images/activity-plan-chatter.png)

 Ver también

- [Actividades](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html)