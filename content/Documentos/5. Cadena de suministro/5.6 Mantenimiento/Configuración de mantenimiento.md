La aplicación _Mantenimiento_ de Odoo ayuda a las empresas a programar el mantenimiento correctivo y preventivo del equipo que usan en su almacén. Esto es útil para que eviten averías en sus equipos, bloqueos en sus centros de trabajo y gastos de reparación de emergencia.

## Equipos de mantenimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_setup.html#maintenance-teams "Enlazar permanentemente con este título")

Es posible asignar un _equipo de mantenimiento_ al crear solicitudes para que sean responsables de gestionarla.

Vaya a Mantenimiento ‣ Configuración ‣ Equipos de mantenimiento para consultar los equipos existentes.

En la página de Equipos aparece una lista con todos los existentes (si los hay) e incluye el nombre del equipo, los miembros del equipo y la empresa de forma predeterminada.

![Lista de equipos en la página de equipos de mantenimiento.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-setup-teams-list.png)

Haga clic en Nuevo para agregar un nuevo equipo, esta acción agrega una línea vacía al final de la lista de equipos. En el campo que aparece abajo de la columna Nombre del equipo asígnele un nombre al nuevo equipo de mantenimiento.

En la columna Miembros del equipo, haga clic en el campo para abrir un menú desplegable con los usuarios existentes en la base de datos. Seleccione a los usuarios pertenecientes al nuevo equipo de mantenimiento.

Haga clic en Buscar más… para abrir la ventana emergente Buscar: Miembros del equipo. Allí busque a los usuarios que **no** aparecen en el menú desplegable inicial.

![Ventana emergente Buscar: Miembros del equipo.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-setup-search-team-members.png)

En la columna Empresa, si se encuentra en un entorno multiempresa, haga clic en el menú desplegable para seleccionar la empresa en la base de datos a la que pertenece este nuevo equipo.

Una vez que esté listo, haga clic en Guardar para guardar los cambios.

 Truco

A los miembros del equipo asignados a los equipos de mantenimiento también se les llama **técnicos** en el calendario de mantenimiento.

Vaya a menuselection:`Mantenimiento --> Mantenimiento --> Calendario de mantenimiento` y haga clic en una solicitud existente. En la ventana emergente que aparece busque el campo Técnico, el nombre que aparece en ese campo es el miembro del equipo y es el usuario responsable de esa solicitud en particular.

![Ventana emergente de solicitud de mantenimiento, el campo Técnico aparece dentro de un recuadro rojo.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-setup-popover-technician.png)

En el lado derecho de la página hay una columna lateral con un calendario minimizado establecido en la fecha de hoy y una lista de técnicos en la que aparecen todos los técnicos (o miembros del equipo) que en ese momento tienen solicitudes abiertas.

## Equipo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_setup.html#equipment "Enlazar permanentemente con este título")

En la aplicación _Mantenimiento_ de Odoo, el _equipo_ son las máquinas y herramientas que se utilizan de forma interna en los centros de trabajo de almacén. El equipo puede incluir computadoras o tabletas, herramientas eléctricas, máquinas utilizadas para la fabricación y más.

### Categorías de equipo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_setup.html#equipment-categories "Enlazar permanentemente con este título")

Cada pieza de equipo pertenece a una _categoría de equipo_. Antes de agregar equipo nuevo, asegúrese de crear una categoría correspondiente a este equipo.

Para agregar una nueva categoría, vaya a Mantenimiento ‣ Configuración ‣ Categorías del equipo y haga clic en Nuevo. Esta acción abre un formulario vacío de categoría de equipo.

![Formulario de categoría de equipo con información completada.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-setup-category-form.png)

En el formulario vacío, asígnele un nombre en el campo Nombre de categoría.

En el campo Responsable asigne a un usuario para que se encargue del equipo en esta categoría, si es necesario. De forma predeterminada, el usuario que crea la categoría está seleccionado como :guilabel:[`](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_setup.html#id1)responsable.

Si se encuentra en un entorno multiempresa, haga clic en el campo Empresa y con el menú desplegable seleccione la empresa de la base de datos a la que pertenece el equipo en esta categoría.

En el campo Seudónimo de correo electrónico asigne un seudónimo de correo a esta categoría, si es necesario.

En el campo Comentarios escriba cualquier comentario o nota para que, en caso de que sea necesario, los usuarios internos hagan referencia con esta categoría.

 Nota

Luego de crear una nueva categoría de equipo, todos los equipos pertenecientes a ella, así como cualquier solicitud de mantenimiento anterior o actual, están disponibles en el formulario correspondiente.

Vaya a Mantenimiento ‣ Configuración ‣ Categorías del equipo y seleccione una para visualizarla. En la parte superior del formulario aparecerán dos botones inteligentes: Equipo y Mantenimiento.

![Los botones Equipo y Mantenimiento en el formulario de categoría del equipo.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-setup-smart-buttons.png)

Haga clic en el botón inteligente Equipo para ver todos los equipos que pertenecen a esta categoría y haga clic en el botón Mantenimiento para ver cualquier solicitud de mantenimiento anterior o actual.

### Máquinas y herramientas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_setup.html#machines-tools "Enlazar permanentemente con este título")

Para agregar equipo nuevo, vaya a Mantenimiento ‣ Equipo ‣ Maquinas y herramientas y haga clic en Nuevo.

Asígnele un nombre al nuevo equipo en el campo Nombre. En el campo Categoría del equipo, haga clic en el menú desplegable y seleccione a qué categoría debe pertenecer este nuevo equipo.

Si se encuentra en un entorno multiempresa, haga clic en el campo Empresa y con el menú desplegable seleccione la empresa de la base de datos a la que pertenece el nuevo equipo.

En el campo Usado por seleccione uno de los tres botones de opción: Departamento, Empleado u Otro.

![Lado izquierdo de los campos de información en el formulario del nuevo equipo.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-setup-new-equipment-left-side.png)

Si selecciona Departamento, el campo Departamento aparece abajo del campo Usado por. Haga clic en el menú desplegable y seleccione el departamento que utiliza este equipo.

Si selecciona Empleado, el campo Empleado aparece abajo del campo Usado por. Haga clic en el menú desplegable y seleccione al empleado que utiliza este equipo.

Si selecciona la opción Otro, abajo del campo :guilabel:`Usado por aparecen los campos Departamento y Empleado. Haga clic en los menús desplegables de los respectivos campos y elija qué departamento y empleado utilizan este equipo.

En el campo Equipo de mantenimiento seleccione al equipo responsable de este equipo y en el campo Técnico seleccione al miembro del equipo o usuario responsable del equipo.

![Lado derecho de los campos de información en el formulario del nuevo equipo.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-setup-new-equipment-right-side.png)

En el campo Usado en la ubicación proporcione la ubicación correspondiente si este equipo no se utilizará en un centro de trabajo interno (por ejemplo, en una oficina).

En el campo Centro de trabajo haga clic en el menú desplegable y seleccione en qué centro de trabajo se utilizará este equipo.

En el espacio vacío disponible en la pestaña Descripción que se encuentra en la parte inferior del formulario podrá agregar cualquier información relevante que describa el equipo.

#### Pestaña de información del producto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_setup.html#product-information-tab "Enlazar permanentemente con este título")

Haga clic en la pestaña Información del producto del formulario de equipo para agregar cualquier información relevante al crear un nuevo equipo.

![La pestaña información del producto con sus campos disponibles.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-setup-product-information.png)

En el campo Proveedor agregue el proveedor del que adquirió el equipo y, en caso de que sea necesario, en el campo Referencia de proveedor agregue el número de referencia del producto que le proporcionó el proveedor.

En el campo Modelo especifique el modelo de este equipo en caso de que sea necesario. Si el equipo está seriado, agregue un número de serie en el campo Número de serie.

Haga clic en la fecha del campo Fecha efectiva para abrir un calendario emergente y seleccione una fecha. Esta fecha indica cuándo se puso en uso este equipo por primera vez y se utilizará para calcular el tiempo medio entre fallos (MTBF) en la pestaña Mantenimiento del equipo.

En el campo Costo especifique cuánto cuesta adquirir el equipo, si aplica.

Si el equipo cuenta con una garantía, seleccione una fecha en el campo Fecha de vencimiento de la garantía para especificar cuándo termina.

#### Pestaña de mantenimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_setup.html#maintenance-tab "Enlazar permanentemente con este título")

Varias de las métricas de mantenimiento que están disponibles en cada equipo se calculan en automático según el mantenimiento correctivo y el mantenimiento preventivo planificado.

Haga clic en la pestaña Mantenimiento para visualizar las métricas de mantenimiento de un equipo en específico.

![La pestaña de mantenimiento en el formulario del equipo. Aparecen los campos con las métricas calculadas.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-setup-metrics.png)

La acción anterior hace que aparezcan los siguientes campos:

- Tiempo medio estimado entre fallos: la cantidad de tiempo (en días) antes de esperar el siguiente fallo. Este es el **único** campo que no está en gris y el **único** campo que los usuarios pueden editar.
    
- Tiempo medio entre fallos: la cantidad de tiempo (en días) entre los fallos notificados. Este valor se calcula con los mantenimientos correctivos completados.
    
- Próximo fallo estimado: la fecha en la que se espera el siguiente fallo. Esta fecha se calcula con la última fecha de fallo y el tiempo medio entre fallos.
    
- Último fallo: la fecha del último fallo. El valor en este campo se actualiza cuando notifica un fallo para este equipo.
    
- Tiempo medio de reparación: la cantidad de tiempo (en días) necesaria para reparar este equipo en caso de fallo. Este valor se actualiza al completar una solicitud de mantenimiento para este equipo.
    

## Centros de trabajo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_setup.html#work-centers "Enlazar permanentemente con este título")

Para ver los centros de trabajo donde se está utilizando el equipo y cómo se utiliza, vaya a Mantenimiento ‣ Equipo ‣ Centros de trabajo y haga clic en uno.

Esta acción abrirá el formulario del centro de trabajo correspondiente. Haga clic en la pestaña Equipo para ver todas las máquinas y herramientas que se utilizan en ese centro de trabajo.

Cada equipo aparece con información relacionada, como el nombre del equipo, el técnico responsable, la categoría del equipo a la que pertenece y algunas métricas de mantenimiento importantes como su tiempo medio entre fallos, Tiempo medio de reparación y la fecha del próximo fallo esperado.

![Lista de los equipos incluidos en un centro de trabajo.](https://www.odoo.com/documentation/17.0/es/_images/maintenance-setup-work-center.png)

 Truco

Para agregar nuevos equipos a un centro de trabajo desde el formulario del centro de trabajo, haga clic en Agregar una línea en la pestaña Equipo. Esta acción abre la ventana emergente Agregar: Equipo de mantenimiento.

En la ventana emergente, seleccione el equipo que debe agregar al centro de trabajo y haga clic en Seleccionar.

 Ver también

[Agregar equipo nuevo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/add_new_equipment.html)