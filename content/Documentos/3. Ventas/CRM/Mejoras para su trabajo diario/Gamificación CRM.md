En la aplicación _CRM_ de Odoo, las _herramientas de ludificación_ permiten evaluar y motificar a los usuarios mediante retos, metas y recompensas que se pueden personalizar. Las metas se crean para acciones dentro de la aplicación _CRM_, además, pueden monitorearse y los equipos de venta pueden recibir recompensas en automático.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/gamification.html#configuration "Enlazar permanentemente con este título")

Para instalar el módulo de * Ludificación CRM* vaya a Aplicaciones, haga clic en la barra Buscar… en la parte superior de la página y quite el filtro Aplicaciones. Escriba ` Ludificación CRM` en la barra de búsqueda.

En el módulo Ludificación CRM haga clic en Instalar. Este módulo incluye las metas y los retos relacionados a las aplicaciones _CRM_ y _Ventas_.

![Vista de un módulo de gamificación que se está instalando en Odoo.](https://www.odoo.com/documentation/17.0/es/_images/gamification-module-install.png)

 Nota

Si tiene instalada **tanto** la aplicación _CRM_ como la aplicación _Ventas_, el módulo _Ludificación CRM_ se instala de manera automática en la base de datos.

Para acceder al menú _Herramientas de ludificación_ primero deberá activar modo de desarrollador.

Después, vaya a Ajustes ‣ Herramientas de ludificación.

![Vista del menú de herramientas de gamificación en los ajustes de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/gamification-tools-menu.png)

## Crear insignias[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/gamification.html#create-badges "Enlazar permanentemente con este título")

Las _insignias_ se le dan a los usuarios cuando completaron un reto. Se pueden premiar diferentes insignias según el tipo de tarea completada y se pueden brindar a más de un usuario, según el tiempo que les tome lograr una meta.

Para ver las insignias existentes, cree una nueva en Ajustes ‣ Herramientas de ludifiación ‣ Insignias.

![Vista de la página de insignias en Odoo.](https://www.odoo.com/documentation/17.0/es/_images/badges1.png)

 Nota

Algunas insignias también se pueden premiar fuera de retos. Seleccione la tarjeta de kanban para la insignia deseada y después haga clic en Otorgar, lo cual hará que se abra la ventana emergente Otorgar insignia. Finalmente, seleccione un usuario en el campo ¿A quién desea recompensar?.

Agregue cualquier información adicional sobre por qué este usuario está recibiendo esta insignia en el campo de abajo y luego haga clic en Otorgar insignia.

Para crear una insignia nueva, haga clic en Nuevo en la parte superior derecha de la página para abrir un formulario en blanco. Ingrese el nombre de la Insignia y luego escriba una descripción.

El campo Concesión a otorgar determina cuándo y quién puede otorgar la insignia:

- Todos: esta insignia se puede otorgar de forma manual a cualquier usuario
    
- Una lista de usuarios seleccionados: esta insignia solo la puede otorgar un grupo específico de usuarios. Si se selecciona esta opción, se generará un nuevo campo de Usuarios autorizados donde podrá a seleccionar a los usuarios apropiados desde la lista desplegable.
    
- Personas que tienen algunas insignias: esta insignia solo la pueden otorgar usuarios que ya tengan una insignia específica. Si selecciona esta opción se generará un campo nuevo de Insignias requeridas. En la lista desplegable de este campo seleccione las insignias que un usuario debe tener antes de poder otorgar esta insignia a otros usuarios.
    
- Nadie, se asignó mediante los desafíos: esta insifnia no se puede otrogar de forma manual, solo se puede ganar mediante retos.
    

Para limitar el número de insignias que un usuario puede enviar, marque la casilla de verificación Aportación mensual limitada a. Esto impondrá un límite en las veces que un usuario puede otorgar esta insignia. En el campo Número de limitación ingrese el número máximo de veces que esta insignia se puede enviar por mes, por persona.

![La página de detalles para una nueva insignia.](https://www.odoo.com/documentation/17.0/es/_images/create-badge.png)

## Cree un reto[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/gamification.html#create-a-challenge "Enlazar permanentemente con este título")

Para crear un reto, vaya a Ajustes ‣ Herramientas de ludificación ‣ Retos. Haga clic en Nuevo en la esquina superior izquierda para abrir un formulario de reto en blanco.

En la parte superior del formulario, ingrese el Nombre del desafío.

### Crear reglas de asignación[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/gamification.html#create-assignment-rules "Enlazar permanentemente con este título")

Para asignarle el reto a usuarios en específico, primero debe utilizar una o más reglas de asignación.

Haga clic en el primer campo debajo de Asignar desafío a y seleccione un parámetro desde la lista desplegable para definir la regla. Después, haga clic en el campo a un lado para definir el operador de la regla. Si es necesario, haga clic en el tercer campo para definir aún más el parámetro de la regla.

 Truco

Cree una regla con los siguientes parámetros para incluir a todos los usuarios con permisos en la aplicación _Ventas_:

- Grupos
    
- está en
    
- `Ventas/Usuario: solo mostrar documentos propios`
    

![Imagen de la sección de reglas de asignación de un formulario de reto.](https://www.odoo.com/documentation/17.0/es/_images/assignation-rule.png)

En el campo Periodicidad seleccione un periodo en las que las metas se deben evaluar de manera automática.

### Agregar metas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/gamification.html#add-goals "Enlazar permanentemente con este título")

Los retos se basan en una única meta, o pueden incluir varias metas con diferentes objetivos. Para agregar una meta a un reto, haga clic en Agregar una línea en la pestaña Metas.

En el campo Definición de la meta seleccione una meta de la lista desplegable. El campo Condición se actualiza para recibir la condición que esté configurada en la definición de la meta.

 Truco

El módulo _Ludificación CRM_ contiene algunas metas preconfiguradas para equipos de venta:

- Leads nuevos
    
- Tiempo para calificar un lead
    
- Días para cerrar un trato
    
- Nuevas oportunidades
    
- Nuevas órdenes de venta
    

Ingrese un Objetivo para la meta según el Sufijo.

Repita estos pasos para cada meta adicional.

![La pestaña de metas de un formulario de reto.](https://www.odoo.com/documentation/17.0/es/_images/challenge-goals.png)

### Agregar recompensas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/gamification.html#add-rewards "Enlazar permanentemente con este título")

Después, haga clic en la pestaña Recompensa. Seleccione la [insignia](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/optimize/gamification.html#crm-create-rewards) que se debe otorgar Para el primer usuario y Para todos los usuarios exitosos desde la lista desplegable.

 Nota

Las insignias se otorgan cuando se finaliza un reto. Esto pasa al final de un periodo, en la última fecha del reto, o cuando el reto se cierra de forma manual.

Después de que se completa la configuración, haga clic en Iniciar reto en la parte superior izquierda de la página para iniciar el reto.