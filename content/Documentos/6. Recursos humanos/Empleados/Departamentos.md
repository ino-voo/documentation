Todos los empleados en la aplicación _Empleados_ pertenecen a departamentos específicos dentro de la empresa.

## Crear nuevos departamentos[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/departments.html#create-new-departments "Enlazar permanentemente con este título")

Para crear un nuevo departamento, vaya a Empleados ‣ Departamentos y después haga clic en Nuevo en la parte superior izquierda para mostrar un formulario de departamento en blanco. Llene la siguiente información en el formulario del departamento:

![Un formulario de departamento con todos los campos llenos.](https://www.odoo.com/documentation/17.0/es/_images/department-form.png)

- Nombre del departamento: ingrese el nombre del departamento.
    
- Gerente: seleccione el gerente del departamento desde el menú desplegable.
    
- Departamento principal: si el nuevo departamento pertenece a otro departamento (tiene un departamento principal) seleccione cuál es departamento principal desde el menú desplegable.
    
- Plantillas de evaluaciones personalizadas: si un empleado de este departamento requiere un formulario de evaluación específico que es diferente al automático, marque esta casilla. Si activa esta opción, aparecerá una pestaña de Plantillas de evaluación abajo del formulario. Este campo **solo** aparece si tiene instalada la aplicación _Evaluaciones_.
    
- Empresa: seleccione la empresa a la que pertenece este departamento en el menú desplegable.
    
- :guilabel:` Encuesta de evaluación`: en este menú desplegable seleccione la encuesta predeterminada que se usará para el departamento cuando se solicite retroalimentación de los empleados. Este campo **solo** aparece si la aplicación _Evaluaciones_ está instalada **y** la opción _Evaluación de desempeño 360°_ se activó en los ajustes.
    
- Color: seleccione un color para el departamento. Haga clic en la caja de color blanco para mostrar todas las opciones de colores. Haga clic en un color para seleccionarlo.
    
- Pestaña plantilla de evaluación: esta pestaña **solo** aparece si activó la opción Plantillas de evaluaciones personalizadas en el formulario. Haga todos los cambios que quiera al formulario de valoración, este formulario se usará para las valoraciones de todos los empleados de este departamento.
    

Después de completar el formulario, haga clic en el icono  (subir a la nube) para guardar los cambios de forma manual. Al guardarlos, aparecerá un gráfico de Organización del departamento en la parte superior derecha de la tarjeta del departamento.

 Nota

El formulario se guarda de forma automática cuando ingresa información, sin embargo el gráfico de Organización del departamento aparecerá **solo** hasta que guarde el formulario de forma manual. Si el formulario no se guarda, el gráfico de Organización del departamento se puede ver al abrir la tarjeta del departamento desde el tablero Departamentos.

 Ver también

Consulte la documentación sobre [Valoraciones](https://www.odoo.com/documentation/17.0/es/applications/hr/appraisals.html) para más información.

## Tablero de departamentos[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/departments.html#departments-dashboard "Enlazar permanentemente con este título")

Para ver los departamentos configurados, vaya a Empleados ‣ Departamentos. Todos los departamentos aparecen en vista kanban por defecto y se enlistan en orden alfabético.

![La vista de tablero de departamentos, con todas las tarjetas de departamento en una vista kanban.](https://www.odoo.com/documentation/17.0/es/_images/departments.png)

### Vista de kanban[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/departments.html#kanban-view "Enlazar permanentemente con este título")

Cada departamento tiene su propia tarjeta de kanban en la vista  (Kanban) del tablero de Departamentos. En estas tarjetas encontrará la información siguiente:

- Nombre del departamento: ingrese el nombre del departamento.
    
- Empresa: la empresa a la que pertenece el departamento.
    
- Empleados: el número de empleados que pertenecen al departamento.
    
- Evaluaciones: el número de evaluaciones programadas para los empleados de este departamento.
    
- Solicitudes de tiempo personal: el número de solicitudes de tiempo personal sin aprobar para empleados dentro del departamento [en espera de aprobación](https://www.odoo.com/documentation/17.0/es/applications/hr/time_off/management.html#time-off-manage-time-off) . Esto **solo** aparece si hay solicitudes por aprobar.
    
- Solicitudes de asignación: el número de solicitudes de asignación sin aprobar para empleados dentro del departamento [en espera de aprobación](https://www.odoo.com/documentation/17.0/es/applications/hr/time_off/management.html#time-off-manage-allocations) . Esto **solo** aparece si hay solicitudes por aprobar.
    
- Nuevos candidatos: el número de [nuevos candidatos](https://www.odoo.com/documentation/17.0/es/applications/hr/recruitment/recruitment-flow.html#recruitment-new) que hay para un puesto en este departamento. Esto **solo** aparece si hay nuevos candidatos.
    
- Reportes de gastos: el número de empleados en este departamento que tienen [reportes de gastos abiertos por aprobar](https://www.odoo.com/documentation/17.0/es/applications/finance/expenses.html#expenses-approve). Esto **solo** aparece si hay reportes de gastos por aprobar.
    
- Ausencia: el número de ausencias para el día de hoy.
    
- Barra de color: el color seleccionado para el departamento aparece como una barra vertical en el lado izquierdo de la tarjeta de departamento.
    

 Nota

Haga clic en una alerta en la tarjeta del departamento, como Solicitudes de tiempo personal para mostrar las solicitudes por aprobar. Esta lista incluye **todas** las solicitudes abiertas por aprobar, no solo las del departamento en específico.

La vista predeterminada para el tablero de Departamentos es la vista kanban. Es posible ver los departamentos de dos otras formas: una vista de lista y una lista de jerarquía.

### Vista de lista[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/departments.html#list-view "Enlazar permanentemente con este título")

Para ver los departamentos en una vista de lista, haga clic en el icono  (lista) ubicado en la esquina superior derecha. Los departamentos aparecen en una vista de lista, en la que podrá ver el Nombre de departamento, Empresa, Gerente, Empleados, Departamento principal y Color de cada departamento.

Por defecto, los departamentos se acomodan en orden alfabético por Nombre de departamento.

![Los departamentos se muestran en vista de lista.](https://www.odoo.com/documentation/17.0/es/_images/list2.png)

 Truco

Cuando se encuentre en vista de lista, podrá gestionar los departamentos en lote si selecciona uno o varios registros con las casillas de verificación. Después seleccione el botón  Acciones para mostrar un menú desplegable de acciones.

### Vista de jerarquía[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/departments.html#hierarchy-view "Enlazar permanentemente con este título")

Para ver los departamentos en vista de jerarquía, haga clic en el icono  (jerarquía) en la esquina superior derecha. Los departamentos aparecen en formato de organigrama, en la parte superior aparecerá el departamento de mayor nivel (usualmente será la Gerencia) y todos los otros departamentos aparecerán abajo de este. Todos los departamentos secundarios del departamento principal estarán plegados.

Cada tarjeta de departamento muestra el Nombre del departamento, el Gerente (y su imagen de perfil), el Número de empleados en el departamento y la posibilidad de expandir el departamento (Desplegar) si el departamento tiene departamentos secundarios.

Haga clic en el botón Desplegar en la tarjeta del departamento para expandirlo. Una vez que lo haga, el botón Desplegar cambiará a ser un botón Plegar. Para colapsar el departamento, haga clic en el botón Plegar. Solo puede desplegar **un** departamento _por hilera_ a la vez.

Haga clic en cualquier parte dentro de una tarjeta de departamento para abrir el formulario de departamento. Haga clic en el botón inteligente (#) Empleados para ver una lista de todos los empleados en ese departamento, incluyendo todos los empleados en los departamentos secundarios debajo, organizados por departamento individual.

 Example

> En la vista de jerarquía, si hace clic en el botón (2) Empleados en la tarjeta Gestión (la tarjeta de departamento con mayor nivel) **todos** los empleados aparecerán en la vista de lista agrupados por departamentos. Esto se debe a que **todos** los departamentos son departamentos secundarios del departamento Gestión.
> 
> Si se hace clic en el botón (3) Empleados en la tarjeta de departamento Ventas aparecerán en la lista los empleados del departamento Ventas así como los de los dos departamentos secundarios (Territorio de la costa este y Territorio de la costa oesta).

![Los departamentos mostrados en vista de jerarquía.](https://www.odoo.com/documentation/17.0/es/_images/hierarchy.png)![La vista de lista de empleados para el departamento al que se hizo clic, incluyendo todos los departamentos secundarios.](https://www.odoo.com/documentation/17.0/es/_images/employee-list.png)