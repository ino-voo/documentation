Ya que haya configurado sus suscripciones y estén funcionando, es importante mantenerse al día de los clientes. Es eficiente usar la automatización para evitar tener que pasar por la lista de suscriptores y ver cómo van las cosas. Aquí es donde la función de _reglas de automatización_ son muy útiles.

La aplicación _Suscripciones_ de Odoo permite que los usuarios configuren correos electrónicos automáticos, creen tareas para las personas de ventas e incluso envíen cuestionarios de satisfacción para que los suscriptores evalúen su experiencia.

## Cree reglas de automatización[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/automatic_alerts.html#create-automation-rules "Enlazar permanentemente con este título")

Para crear una regla automatizada vaya a la aplicación Suscripciones ‣ Configuración ‣ Reglas de automatización. Aquí podrá encontrar todas las reglas de automatización para las suscripciones.

La página Reglas de automatización muestra el page Nombre de cada regla, la Acción a realizar, Activar en, y la Empresa a la que se aplicará esta regla.

Para ver o modificar cualquier regla de automatización existente, solo haga clic en la regla deseada que se encuentre en esta página.

 Nota

Al modificar una regla de automatización existente Odoo «atenuará» la sección Acción del formulario y le muestra la siguiente advertencia: _Para evitar comportamientos inesperados, no es posible actualizar los datos de acción. Mejor cree una nueva acción._

Para crear una nueva regla de automatización, haga clic en Nuevo.

![La página de Reglas de automatización en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/automation-rules-page.png)

Al hacer clic en Nuevo se mostrará un formulario de Reglas de automatización en blanco con varios campos numéricos por configurar.

![Un formulario de reglas de automatización de ejemplo en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/automation-rules-form.png)

### Campos de las reglas de automatización[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/automatic_alerts.html#automation-rule-form-fields "Enlazar permanentemente con este título")

- Nombre de la acción: título de la regla de acción automatizada.
    

#### Sección Aplicar en[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/automatic_alerts.html#apply-on-section "Enlazar permanentemente con este título")

La sección aplicar en indica a qué órdenes o clientes se aplicará esta acción automatizada.

- MRR entre: designar un rango de ingresos recurrentes mensuales al que dirigirse.
    
- Aumento de MRR: designar un cambio de ingresos recurrentes mensuales al objetivo, en porcentaje o unidad de moneda.
    
- Periodo: seleccione un periodo durante el que se calcularán los KPI (indicadores de rendimiento clave).
    
- Calificación de satisfacción: designe un nivel de satisfacción como mayor que o menor que un porcentaje.
    
- Estado: seleccione el estado de las suscripciones que se tienen que incluir en esta regla de automatización. Las opciones son Cotización, Cotización enviada, Orden de venta, and Cancelar.
    
- Etapa pasa de: designa cuándo se debe activar la regla de automatización mediante dos campos que representan dos diferentes etapas de la suscripción.
    
- Planes de suscripción: seleccione los planes de suscripción que serán el objetivo de la regla de automatización.
    
- Productos: seleccione productos específicos que serán el objetivo de la regla de automatización.
    
- Clientes: seleccione clientes específicos que serán el objetivo de esta regla de automatización.
    
- Empresa: en un entorno multiempresa, seleccione información específica de la empresa que sea el objetivo de esta regla de automatización.
    
- Equipos de venta: seleccione los datos de equipos de venta específicos que sean objetivo de la regla de automatización.
    

 Nota

Si cualquier campo se deja en blanco, la regla aplica a todas las suscripciones que no tengan esa designación específica.

 Truco

El número de suscripciones que coinciden con los criterios configurados de la regla de automatización personalizada se muestran hasta abajo del campo Aplicar en.

Si se hace clic en ese enlace verde de suscripciones, Odoo mostrará una página separada en la que se pueden ver todas las suscripciones que coinciden con los criterios de la regla de automatización.

#### Sección de Acción[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/automatic_alerts.html#action-section "Enlazar permanentemente con este título")

La sección Acción indica qué acción debe ocurrir cuando se activa una regla de automatización.

En el campo Acciones por hacer seleccione la acción que se realizará una vez que se active la regla de automatización. Al hacer clic, las siguientes opciones estarán disponibles en el menú desplegable:

- Crear siguiente actividad: crea la siguiente actividad que debe ocurrir, la cual se configura en la sección Actividad que aparece al fondo del formulario de reglas de automatización.
    
- Enviar un correo electrónico al cliente: se le envía un correo electrónico al cliente que coincida con los criterios de la regla de automatización.
    
- Enviar un mensaje de texto SMS al cliente: envía un mensaje SMS al cliente que coincida con los criterios de la regla de automatización.
    
- Establecer el valor de la salud del contrato: configurar el valor de la salud del contrato de suscripción.
    

Si se selecciona Enviar un correo electrónico al cliente en el campo Acción a realizar, aparecerá el siguiente campo:

- Plantilla de correo electrónico: cree (y edite) una nueva plantilla de correo electrónico _o_ seleccione una desde una lista de plantillas de correo electrónico preconfiguradas para enviársela a los clientes.
    

Si selecciona Enviar un mensaje de texto SMS al cliente en el campo Acción a realizar, aparecerá el siguiente campo:

- Plantilla de SMS: cree (y edite) una nueva plantilla de SMS _o_ seleccione una desde una lista de plantillas SMS preconfiguradas para enviársela a los clientes.
    

Si se selecciona Establecer el valor de la salud del contrato en el campo Acción a realizar, aparecerá el siguiente campo:

- Salud: para designar la salud de la suscripción tiene que elegir entre: Neutral, Bueno, o Malo.
    

En el campo Activar en se debe decidir si la regla de automatización se debe activar en una Modificación o Condición de tiempo.

 Nota

Aparecerá el botón Activar ahora en la parte superior de la regla de automatización _solo_ cuando configuró una forma de activar la regla.

 Advertencia

Cuando se hace clic en Activar ahora Odoo activará la acción vinculada a _todas_ las suscripciones, sin importar las condiciones de tiempo posibles.

 Nota

Para enviar un mensaje de texto SMS en Odoo es necesario que cuente con créditos o tokens de compras dentro de la aplicación (IAP). Para obtener más información sobre IAP, visite [Compras dentro de la aplicación (IAP, por sus siglas en inglés)](https://www.odoo.com/documentation/17.0/es/applications/essentials/in_app_purchase.html). Para obtener más información sobre el envío de mensajes SMS, visite [Fundamentos de SMS](https://www.odoo.com/documentation/17.0/es/applications/marketing/sms_marketing/essentials/sms_essentials.html).

Si se selecciona Condición de tiempo en el campo Activar en, aparecerá el siguiente campo:

- Fecha de activación: representa cuándo se debe activar la condición. Si se deja en blanco, la acción se creará cuando se cree _y_ actualice la suscripción.
    
- Retraso después de la activación: seleccionar una cantidad de tiempo de retraso en (Minutos, Horas, Días, o Meses) que Odoo debe esperar antes de que se active una acción configurada. Si se ingresa un número negativo, el «retraso» ocurrirá _antes_ de la Fecha de activación.
    

##### Sección de Actividad[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/automatic_alerts.html#activity-section "Enlazar permanentemente con este título")

Si se selecciona Crear siguiente actividad en el campo Acción por hacer aparecerá una sección de Actividad en la parte inferior del formulario.

- Tipo de actividad: seleccione un tipo de actividad preconfigurado desde el menú desplegable.
    
- Título: ingrese un título personalizado de la actividad elegida.
    
- Nota: deje una nota para el empleado al que se le haya asignado la actividad.
    
- Fecha de vencimiento en: ingrese la cantidad en días dentro de los que se debe de completar la actividad.
    
- Asignar a: puede elegir asignar una actividad específica ya sea a: Persona de venta de la suscripción, Líder del equipo de ventas, o Usuarios específicos.
    

 Nota

Si se selecciona Usuarios específicos en la opción Asignar a aparecerá un campo de Usuarios específicos debajo de él, donde puede seleccionar a usuarios específicos a los que asignarles la actividad configurada.

 Ver también

- [Suscripciones](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions.html)
    
- [Planes de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/plans.html)
    
- [Productos de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/products.html)
    
- [Compras dentro de la aplicación (IAP, por sus siglas en inglés)](https://www.odoo.com/documentation/17.0/es/applications/essentials/in_app_purchase.html)