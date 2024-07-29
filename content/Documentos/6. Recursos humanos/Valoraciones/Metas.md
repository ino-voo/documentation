La aplicación _Evaluación_ de Odoo permite que los gerentes impongan metas a sus empleados. De esta forma, los empleados saben a qué objetivo deben llegar antes de su siguiente evaluación.

Para visualizar todas las metas, vaya a Evaluación ‣ Metas. Allí aparecerán todas las metas de cada empleado en una vista de kanban predeterminada.

Cada tarjeta de meta incluye la siguiente información:

- Meta: el nombre de la meta.
    
- Empleado: el empleado al que se le asigna la meta.
    
- Icono  (reloj): muestra el [icono de actividad](https://www.odoo.com/documentation/17.0/es/applications/essentials/activities.html) correspondiente para el registro. Si no hay actividades programadas, el icono predeterminado es  (reloj). Si se programó cualquier actividad, el icono representará la actividad más cercana que se haya programado.
    
- Fecha límite: la fecha de vencimiento de la meta.
    
- Progreso: qué tan completada está la meta en porcentaje. Las opciones son 0%, 25%, 50%, 75%, o 100%.
    
- Icono de empleado: el icono de perfil del empleado al que se le asigna la meta.
    

Si la meta se ha cumplido aparece el mensaje Hecho en la esquina superior derecha de su tarjeta.

![La vista de kanban de las metas, aparecen nueve tarjetas.](https://www.odoo.com/documentation/17.0/es/_images/goals.png)

 Nota

Cada meta individual requiere su propio registro para cada empleado. Si varios empleados tienen la misma meta, en la lista aparecerá una tarjeta de meta diferente para cada empleado.

Por ejemplo, si Bob y Sara tienen la misma meta de `Teclear`, aparecerán dos tarjetas en la vista kanban: una meta `Teclear` para Bob y otra meta `Teclear` para Sara.

## Nueva meta[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/goals.html#new-goal "Enlazar permanentemente con este título")

Para crear una nueva meta, vaya a Evaluación ‣ Metas y haga clic en Nuevo que se encuentra en la esquina superior izquierda para abrir un formulario de meta vacío.

Ingrese la información sobre la meta, el empleado, el progreso, y la Fecha de vencimiento, en la tarjeta de meta, como se explicó en la sección [tarjeta de meta](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/goals.html#appraisals-goal-card) de este documento.

La información necesaria es la misma que aparece en la tarjeta de meta en la vista de kanban, solo que ahora incluye el campo Etiquetas y la pestaña Descripción.

 Truco

La aplicación _Evaluaciones_ **no** tiene etiquetas preconfiguradas, así que debe agregar todas las etiquetas. Para agregar una etiqueta, ingrese el nombre de la etiqueta en la línea y después haga clic en Crear «(etiqueta)». Repita este proceso por todas las etiquetas que deba agregar.

El usuario actual completa en automático el campo Empleado de forma predeterminada y el campo Gerente se completa con el gerente establecido en el perfil del empleado.

Haga los cambios necesarios en el formulario y agregue cualquier nota que pueda ser útil para explicar la meta en la pestaña Descripción.

![Un formulario de meta completado para la habilidad "Python", establecido en un 50% de dominio.](https://www.odoo.com/documentation/17.0/es/_images/new-goal.png)

## Metas completadas[](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals/goals.html#completed-goals "Enlazar permanentemente con este título")

Al cumplir una meta es importante actualizar el registro. Las metas se pueden marcar como `hechas` de dos formas, ya sea desde el tablero principal de Metas o desde su respectiva tarjeta.

Para marcar una meta como `hecha` desde el tablero principal de Metas, haga clic en el icono  (tres puntos verticales) que está ubicado en la esquina superior derecha de una tarjeta de objetivo.

 Nota

El icono  (tres puntos verticales) **solo** aparece al pasar el cursor sobre la esquina superior derecha de una tarjeta de meta.

Después, haga clic en la opción Marcar como hecho que se encuentra en el menú desplegable. En la esquina superior derecha de la tarjeta aparecerá el mensaje Hecha en una cinta verde.

Para marcar una meta como `hecha` desde su tarjeta, haga clic en una tarjeta de meta para abrir su formulario correspondiente. Haga clic en el botón Marcar como hecho ubicado en la esquina superior izquierda del formulario. Después, en la esquina superior derecha del formulario del objetivo aparecerá una cinta verde con el mensaje Hecha.