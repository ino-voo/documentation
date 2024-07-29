To create a new appraisal for an employee, first navigate to the main _Appraisals_ dashboard by opening the Appraisals app. The Appraisals dashboard is the default view.

## Appraisals dashboard[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#appraisals-dashboard "Enlazar permanentemente con este título")

All appraisals are displayed on the dashboard in a default Kanban view, with a list of groupings on the left side of the dashboard, including COMPANY, DEPARTMENT, and STATUS.

Haga clic en cualquier opción de agrupamiento para ver evaluaciones **solo** de la selección que hizo.

 Nota

Only groupings with multiple selections appear in the list. For example, if a database only has one company, the COMPANY grouping does **not** appear, since there is no other company to select.

Cada tarjeta de evaluación muestra la siguiente información:

- **Name**: the employee’s name.
    
- **Department**: the department the employee is associated with.
    
- **Company**: the company the employee works for. This only appears in a multi-company database.
    
- **Date**: the date the appraisal was requested, or is scheduled for in the future.
    
- **Activities**: any [activities](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html) that are scheduled for the appraisal, such as _Meetings_ or _Phone Calls_.
    
- **Manager**: the employee’s manager, indicated by the profile icon in the bottom-right corner of an appraisal card.
    
- **Status banner**: the status of the appraisal. A banner appears if an appraisal is marked as either _Canceled_ or _Done_. If no banner is present, that means the appraisal has not happened, or has not been scheduled yet.
    

Para ver los detalles de cualquier evaluación, haga clic en la tarjeta para abrir el formulario de evaluación.

![El tablero de la aplicación Evaluación con cada evaluación en su propia caja.](https://www.odoo.com/documentation/17.0/es/_images/dashboard.png)

## Create an appraisal[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#create-an-appraisal "Enlazar permanentemente con este título")

To create a new appraisal, click the New button in the upper-left corner of the Appraisals dashboard. Doing so reveals a blank appraisal form. After entering a name in the first blank field, proceed to enter the following information on the form:

- Manager: select the employee’s manager from the drop-down menu. The manager is responsible for completing the _Manager’s Feedback_ section of the appraisal. This field auto-populates after the employee is selected, if they have a manager set on their employee profile.
    
- Appraisal Date: the current date is automatically entered in this field. This field is automatically updated once the appraisal is completed or cancelled, with the corresponding date of completion or cancellation.
    
- Departamento: seleccione el departamento al que pertenece el empleado desde el menú desplegable. Este campo se llena de forma automática después de que se seleccione el empleado, si tienen configurado un departamento en el perfil.
    
- Empresa: seleccione la empresa a la que pertenece el empleado desde el menú desplegable. Este campo se llena de forma automática después de que se seleccione el empleado, si tienen configurado una empresa en el perfil.
    

 Nota

The only required fields for the appraisal form are the employee’s name, the Manager, and the Company.

Una vez que haya completado el formulario, haga clic en el botón Confirmar para confirmar la solicitud de evaluación.

Una vez que se haya confirmado, el empleado recibirá un correo electrónico en el que se indicará que se solicitó una evaluación y después se le pide que elija una fecha para la misma.

El estado cambiará a Confirmadp y la sección Retroalimentación del empleado de la pestaña Evaluación aparecerá atenuada. La información en esta sección solo aparecerá una vez que el empleado termine su autoevaluación. El campo Calificación final solo aparece cuando la solicitud de evaluación se confirma.

Si hay evaluaciones existentes del empleado, aparecerá un botón inteligente de Evaluación en la parte superior de la página, donde se enlista el número total de evaluaciones que hay para el empleado.

### Solicitar retroalimentación[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#ask-for-feedback "Enlazar permanentemente con este título")

Como parte del proceso de evaluación, el gerente puede pedirle a cualquier persona de la empresa retroalimentación de un empleado. La retroalimentación usualmente se pide a compañeros de trabajo y otras personas con las que el empleado interactúa o trabaja. Esto se hace con el objetivo de obtener una vista más completa del empleado y ayudar a que el gerente pueda hacer una evaluación completa.

Para solicitar retroalimentación **debe** confirmar la evaluación. Una vez que se confirme, aparecerá el botón Solicitar retroalimentación en la parte superior del formulario.

Cuando se hace clic en el botón Solicitar retroalimentación aparecerá un formulario emergente de correo electrónico con la plantilla Evaluación: solicitar retroalimentación, que envía la encuesta retroalimentación 360.

En el campo Destinatarios ingrese los empleados a los que les pedirá que completen la encuesta. Puede seleccionar a varios empleados.

La plantilla de correo electrónico tiene marcadores de posición dinámicos para personalizar el mensaje y tiene la posibilidad de agregar cualquier texto adicional al correo en caso de que así lo desee.

Puede agregar una fecha límite para responder en caso de que sea necesaria.

If any attachments are needed, click the  Attachments button, and a file explorer window appears. Navigate to the file(s), select them, then click Open.

Una vez que el correo electrónico esté listo para su envío, haga clic en Enviar.

![La ventana emergente de correo electrónico en donde se solicitan los comentarios de otros empleados.](https://www.odoo.com/documentation/17.0/es/_images/ask-feedback.png)

### Formulario de evaluación[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#appraisal-form "Enlazar permanentemente con este título")

Once an appraisal is confirmed, the next steps require the employee to fill out the self-assessment, after which the manager completes their assessment.

#### Retroalimentación del empleado[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#employee-s-feedback "Enlazar permanentemente con este título")

Los empleados deben dirigirse al tablero principal de la aplicación Evaluación para completar su retroalimentación. Allí las únicas entradas visibles son las evaluaciones del empleado, es decir, las propias y las de cualquier persona a la que supervise y deba proporcionar retroalimentación como gerente.

Haga clic en la evaluación para abrir su formulario y escriba las respuestas en la sección Retroalimentación del empleado que se encuentra en la pestaña Evaluación.

Una vez que la sección esté completada, haga clic en No es visible para el gerente (es el ajuste predeterminado luego de confirmar una evaluación). Al hacer clic cambiará a Es visible para el gerente.

![La sección de retroalimentación para el empleado con el interruptor correspondiente en un recuadro rojo.](https://www.odoo.com/documentation/17.0/es/_images/employee-feedback.png)

#### Retroalimentación del gerente[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#manager-s-feedback "Enlazar permanentemente con este título")

Después de que el empleado haya completado la sección Retroalimentación del empleado ubicada en la pestaña Evaluación, el gerente deberá completar la sección Retroalimentación del gerente.

El gerente deberá escribir sus respuestas en los campos [igual que el empleado](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#appraisals-employee-feedback).

Una vez que la sección de retroalimentación haya sido completada, haga clic en No es visible para el empleado (es el ajuste predeterminado luego de confirmar una evaluación). Al hacer clic cambiará a Es visible para el empleado.

![La sección de retroalimentación para los empleados y los gerentes. Los botones aparecen en un recuadro rojo.](https://www.odoo.com/documentation/17.0/es/_images/manager-feedback.png)

#### Pestaña de habilidades[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#skills-tab "Enlazar permanentemente con este título")

Part of an appraisal is evaluating an employee’s skills, and tracking their progress over time. The Skills tab of the appraisal form auto-populates with the skills from the [employee form](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#employees-skills), once an appraisal is confirmed.

Cada habilidad está agrupada con habilidades similares. Además, aparece el Nivel de habilidad, Progreso y Justificación para cada una de ellas.

En la pestaña Habilidades puede actualizar cualquier habilidad o agregar nuevas.

Si el nivel de habilidad aumentó puede proporcionar el motivo por el que la calificación mejoró en el campo Justificación, por ejemplo, `realizó un examen de fluidez de cierto idioma` o `recibió una certificación de JavaScript`.

 Ver también

Consulte la documentación sobre cómo [crear un nuevo empleado](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#employees-skills) para obtener instrucciones detalladas relacionadas con agregar o actualizar una habilidad.

Después de completar una evaluación y de actualizar las habilidades, las habilidades actualizadas aparecerán en la pestaña Habilidades la próxima vez que se confirme una evaluación.

![La pestaña de habilidades de un formulario de evaluación con la información completa.](https://www.odoo.com/documentation/17.0/es/_images/skills.png)

 Nota

The Skills tab can be modified **after** the employee and their manager have met and discussed the employee’s appraisal.

This is a common situation as the manager may not have all the necessary information to properly assess and update the employee’s skills before meeting.

#### Private Note tab[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#private-note-tab "Enlazar permanentemente con este título")

If managers want to leave notes that are only visible to other managers, they can be entered in the Private Note tab. This can be done before or after meeting with the employee to discuss the appraisal.

The employee being evaluated does **not** have access to this tab, and the tab does **not** appear on their appraisal.

### Agendar una reunión[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#schedule-a-meeting "Enlazar permanentemente con este título")

El empleado y el gerente deberán reunirse para hablar sobre su evaluación una vez que ambas partes de la evaluación estén completas (es decir, las secciones de [retroalimentación del empleado](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#appraisals-employee-feedback) y [retroalimentación del gerente](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#appraisals-manager-feedback)).

Es posible programar una reunión de dos formas, desde el tablero de la aplicación _Evaluación_ o desde una tarjeta de evaluación individual.

To schedule an appraisal from the dashboard of the _Appraisals_ application, first navigate to Appraisals app ‣ Appraisals.

Click the  (clock) icon, beneath the appraisal date on the desired appraisal card, and a pop-up window appears. Then, click  Schedule an activity to create an activity from a Schedule Activity pop-up form that appears.

En el menú desplegable de Tipo de actividad seleccione Reunión. El formulario cambiará y solo aparecerán los campos Tipo de actividad y Resumen.

Enter a brief description in the Summary field of the Schedule Activity pop-up form, such as `Annual Appraisal for (Employee)`.

Después haga clic en el botón Abrir calendario. Aparecerá la página del calendario, desde allí vaya a (y haga doble clic en) la fecha y hora deseadas para la reunión.

Doing so opens a New Event pop-up form. From this pop-up form, make any desired modifications, such as designating a Start time, or modifying the default Title to the meeting.

Add the appraisee in the Attendees section, and include anyone else who should also be in the meeting, if necessary.

To make the meeting a video call, instead of an in-person meeting, click  Odoo meeting, and a Videocall URL link appears in the field.

Haga clic en Guardar y cerrar después de realizar todos los cambios necesarios.

La reunión ahora aparece en el calendario y todos los invitados reciben un aviso por correo electrónico.

![El formulario de reunión con toda la información correspondiente para la evaluación anual de Ronnie Hart.](https://www.odoo.com/documentation/17.0/es/_images/meeting.png)

The other way to schedule a meeting is from the individual appraisal form. To do this, navigate to the Appraisal app dashboard, then click on an appraisal card.

Next, click on the  Meeting smart button, and the calendar loads. Follow the same directions above to create the meeting.

For more detailed information on how to schedule activities, refer to the [activities](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html) documentation.

 Nota

Si no hay reuniones programadas, en el botón inteligente Reunión aparecerá Sin reuniones.

## Complete an appraisal[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html#complete-an-appraisal "Enlazar permanentemente con este título")

After the appraisal is complete, and both the manager and employee have met to discuss the appraisal, the appraisal can be marked as _Done_. When completed, click the Mark as Done button on the appraisal form, located in the top-left corner.

Once the appraisal is marked as _Done_, the Mark as Done button disappears, and a Reopen button appears.

 Truco

Modifications are **not** possible once the appraisal is marked as done.

To make any changes to an appraisal that is marked as _Done_, click the Reopen button.

Then, click the Confirm button that appears, and make any modifications needed. Once all modifications are complete, click the the Mark as Done button again.

 Ver también

- [Metas](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/goals.html)
    
- [Reportes](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/reporting.html)