En Odoo, la aplicación _Evaluación_ se puede usar para evaluar el rendimiento de un empleado de forma regular. Los gerentes pueden evaluar el rendimiento de sus empleados y también pueden permitir que los empleados hagan una autoevaluación. Las evaluaciones se pueden personalizar y se pueden realizar en cualquier momento.

Las evaluaciones le brindan a los empleados una valiosa retroalimentación, incluyendo las metas que debe lograr, así como habilidades que se puedan medir y que se deban mejorar. Además, las evaluaciones pueden ser la base para aumentos, promociones y otros beneficios.

Las evaluaciones regulares son buenas tanto para los empleados como para la empresa. De esta forma se puede medir correctamente el rendimiento según los objetivos de la empresa y los empleados pueden ver qué es lo que necesitan mejorar.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals.html#configuration "Enlazar permanentemente con este título")

El menú de Configuración de la aplicación _Evaluaciones_ es donde se pueden realizar los ajustes, editar las plantillas de retroalimentación, configurar la frecuencia de retroalimentación, gestionar las escalas de evaluación, almacenar información para retroalimentación 360 y crear o ver las etiquetas de objetivos.

### Ajustes[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals.html#settings "Enlazar permanentemente con este título")

Para acceder al menú de _Ajustes_ vaya a la aplicación Evaluaciones ‣ Configuración ‣ Ajustes.

#### Plantillas de retroalimentación[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals.html#feedback-templates "Enlazar permanentemente con este título")

Las plantillas de retroalimentación son un esquema de formulario que se usa durante la evaluación de un empleado. Las ediciones que se hagan a la plantilla se reflejarán en la valoración que se le envíe a los empleados.

Hoy dos plantillas preconfiguradas en la aplicación _Evaluación_ de Odoo: una para la retroalimentación del empleado y otra para la retroalimentación del gerente. Cada una contiene varias secciones junto con sus preguntas y breves explicaciones sobre cómo responder las preguntas

La Plantilla de retroalimentación del empleado tiene las siguientes secciones: Mi trabajo, Mi futuro, and Mis sentimientos.

La Plantilla de retroalimentación del gerente tiene las siguientes secciones: Retroalimentación, Evaluación y Mejoras.

Cualquier cambio que se quiera hacer a las plantillas de retroalimentación se pueden hacer directamente en cada plantilla.

#### Valoraciones[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals.html#id1 "Enlazar permanentemente con este título")

La sección Evaluaciones del menú de ajustes determina la frecuencia con la que se realizarán las evaluaciones y si es posible solicitar retroalimentación adicional.

![La sección de retroalimentaciones con una línea de tiempo completa en una retroalimentación 360 activada.](https://www.odoo.com/documentation/17.0/es/_images/appraisals-setting.png)

##### Planes de evaluación[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals.html#appraisals-plans "Enlazar permanentemente con este título")

La configuración automática de las evaluaciones es que se creen seis meses después de que se contrata al empleado, con una segunda evaluación seis meses después de la primera.

Una de esas dos evaluaciones iniciales se completan durante el primer año del empleado, las siguientes evaluaciones solo se crean una vez al año (cada doce meses).

Para modificar la frecuenta, cambie el número de meses en los campos en blanco que hay en la sección Planes de valoración.

 Importante

Si la sección Planes de valoración se modifica, también se modifican **todas** las siguientes fechas de evaluación para **todos** los empleados.

##### Retroalimentación 360[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals.html#feedback "Enlazar permanentemente con este título")

Puede activar la opción retroalimentación 360 para permitir que los gerentes soliciten retroalimentación de otros empleados usando un formulario de encuesta, en cualquier momento, sin importar el calendario de evaluaciones.

Usualmente los gerentes piden retroalimentación de otras personas que trabajan con uno de los empleados bajo su mando. Esto incluye los diferentes gerentes del empleado, sus compañeros de trabajo y las personas que le reportan directamente a esta persona.

Para ver la encuesta retroalimentación 360 haga clic en el icono → enlace interno al final del campo Plantilla predeterminada. La encuesta retroalimentación 360 se cargará y podrá hacer cualquier cambio que desee.

Para más información sobre cómo editar una encuesta, vea el documento [Crear encuestas](https://www.odoo.com/documentation/17.0/es/applications/marketing/surveys/create.html).

 Importante

El formulario retroalimentación 360 es una encuesta preconfigurada dentro de la aplicación _Encuestas_. **Debe** instalar la aplicación _Encuestas_ para poder usar y editar la opción retroalimentación 360.

### Escala de evaluación[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals.html#evaluation-scale "Enlazar permanentemente con este título")

En el formulario de evaluación de cada empleado aparecen opciones para una calificación final de forma predeterminada. Para poder ver y editar estas opciones, vaya a Evaluación ‣ Configuración ‣ Escala de evaluación. Esta acción despliega las evaluaciones en vista de lista.

Las calificaciones preconfiguradas son Necesita mejorar, Cumple las expectativas, Supera las expectativas y Supera las expectativas. Para agregar otra calificación, haga clic en el botón Nuevo.

Cuando se hace clic en el botón Nuevo en la página Escala de evaluación aparecerá una línea en blanco en la parte inferior de la lista. Ingrese el nombre de la calificación en el campo.

Para cambiar el orden de las calificaciones, haga clic en el icono (seis cuadros grises pequeños) en la izquierda de la calificación y arrastre la calificación a la posición deseada de la lista.

![Imagen de la escala de evaluación donde se resaltan el botón nuevo y los iconos para arrastrar y soltar.](https://www.odoo.com/documentation/17.0/es/_images/evaluation-scale.png)

### Retroalimentación 360[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals.html#id2 "Enlazar permanentemente con este título")

La sección retroalimentación 360 muestra información para todas las encuestas configuradas en la aplicación _Evaluaciones_. Para ver las encuestas y sus estadísticas, vaya a la aplicación Evaluación ‣ Configuración ‣ Retroalimentación 360.

![Una vista de lista de todas las encuestas disponibles en la aplicación Evaluación.](https://www.odoo.com/documentation/17.0/es/_images/survey-list.png)

Cada evaluación (o encuesta) se presenta en su propia línea en la página retroalimentación 360, así como mucha información relacionada a esa evaluación en particular.

Cada evaluación incluye la siguiente información:

- Nombre de la encuesta: el nombre de esa encuesta en específico.
    
- Responsable: el empleado responsable de la encuesta, incluyendo el mes y el año en el que se les dio esa responsabilidad.
    
- Preguntas: el número de preguntas en esa encuesta en particular.
    
- Duración promedio: el tiempo promedio que le toma a un usuario completar la encuesta.
    
- Registrado: el número de personas a las que se les envió esta encuesta.
    
- Completado: el número de personas que completaron esta encuesta.
    

Cada evaluación también tiene dos botones al final de cada línea: a un botón para probar y un botón para ver los resultados.

Para ver cómo se ve una evaluación para el usuario final (es decir, para el empleado), haga clic en el botón probar y la evaluación se cargará en una nueva pestaña de su navegador. Se cargará la evaluación completa y podrá navegar por ella sin tener que responder ninguna de las preguntas.

Para salir, cierre la pestaña. También puede hacer clic en Esta es una encuesta de prueba. → Editar encuesta en la parte superior de la página para ir a un formulario de detalle para una encuesta en particular.

Para ver los resultados de todas las personas que han completado una evaluación, haga clic en el botón Ver resultados. Esto le mostrará todas las respuestas de la encuesta en una pestaña nueva. Cada pregunta brinda información sobre cuántas personas ha respondido una pregunta y cuántas personas se la saltaron. Podrá ver todas las respuestas a cada pregunta.

Para salir, cierre la pestaña. También puede hacer clic en → Editar encuesta en la parte superior de la página para ir a un formulario de detalle para una encuesta en particular.

Además de ver las respuestas a evaluaciones y encuestas pasadas, también puede crear nuevas encuestas desde la página retroalimentación 360. Solo haga clic en el botón Nuevo en la parte superior izquierda de la página para crear una encuesta nueva.

Para más información sobre cómo crear una encuesta, vea el documento [Crear encuestas](https://www.odoo.com/documentation/17.0/es/applications/marketing/surveys/create.html).

 Nota

En versiones previas de Odoo esta sección se llamaba Encuestas.

 Ver también

- [New appraisals](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/new_appraisals.html)
    
- [Metas](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/goals.html)
    
- [Reportes](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/reporting.html)