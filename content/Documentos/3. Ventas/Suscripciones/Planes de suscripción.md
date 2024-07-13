Los _Planes de suscripción_ son [plantillas de cotización](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/quote_template.html) que se usan para pre-configurar cotizaciones con los productos de suscripción. Use los planes de suscripción para crear rápidamente órdenes de suscripción.

## Configure planes de suscripción[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/plans.html#configure-subscription-plans "Enlazar permanentemente con este título")

Para configurar planes de suscripción, vaya a Suscripciones ‣ Configuración ‣ Planes. Luego, haga clic en Nuevo para crear un nuevo plan o seleccionar uno ya existente para editarlo.

Puesto que la aplicación _Suscripciones_ de Odoo está estrechamente integrada con la aplicación _Ventas_, los planes de suscripción usan el mismo formulario como plantillas de cotización.

![Configuración del formulario del plan de suscripción (plantilla de cotización)](https://www.odoo.com/documentation/17.0/es/_images/subplan-quotation-template.png)

El formulario del plan de suscripción incluye las siguientes opciones:

- Nombre: introduzca un nombre para el plan de suscripción en la aparte superior de la página.
    
- La cotización vence después de: introduzca el número de días después de los cuales la cotización vence, comenzando desde el día en que envía la cotización al cliente. Deje este campo en cero para que la cotización no tenga fecha de vencimiento.
    
- Confirmación en línea: seleccione las casillas junto a Firma o Pago para permitir que el cliente confirme su orden de suscripción al firmar o pagar la cotización. Active ambos campos para que el cliente pueda escoger una opción. Deje ambos en blanco para confirmar la cotización solo desde el backend.
    
- Correo de confirmación: seleccione una [plantilla de correo electrónico](https://www.odoo.com/documentation/17.0/es/applications/general/companies/email_template.html) para el correo de confirmación que se enviará de forma automática al cliente después de confirmar la cotización. Deje este campo vacío para no enviar nada.
    
    - Para crear una nueva plantilla de correo electrónico, introduzca un nombre para la plantilla, luego haga clic Crear y editar.
        
    - Para editar una plantilla de correo que ya existe, seleccione una del menú desplegable, luego haga clic en la flecha del enlace interno al final de la línea.
        
- Recurrencia: seleccione el periodo recurrente que usará el plan. Los periodos recurrentes que están disponibles aquí son los mismos que están configurados en Suscripciones ‣ Configuración ‣ Periodos Recurrentes.
    

Seleccionar una recurrencia convierte la plantilla de cotización en un plan de suscripción y activa las siguientes opciones adicionales:

- Duración: elija si el plan de suscripción no tiene fecha de finalización (para siempre) o una duración fija.
    
    - Si establece la duración como para siempre, entonces el plan de suscripción se renovará hasta que el cliente o la empresa finalicen manualmente la suscripción.
        
    - Si establece la duración como fija, entonces introduzca una fecha de terminar después de , lo que determina la cantidad de tiempo tras la cual la suscripción terminará automáticamente.
        
- Autocancelable: seleccione esta casilla para permitir que el cliente cancele su suscripción desde el [portal de cliente](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/customer_accounts.html).
    
- Cancelación automática: introduzca el número de días tras los cuales las suscripciones _pendientes de pago_ que _pasaron_ la fecha límite de pago se cancelan automáticamente.
    
- Diario contable: seleccione el diario contable en el cual se registrarán las facturas para este plan de suscripción. Deje este campo en blanco para usar el diario de ventas con la secuencia más baja.
    

![Plan de suscripción con Recurrencia seleccionada](https://www.odoo.com/documentation/17.0/es/_images/subplan-recurrence.png)

En la pestaña Líneas, cree las líneas de la orden para la cotización. Haga clic en Agregar un producto, selecciones un producto para incluir el plan, y luego introduzca la cantidad y la unidad de medida. Agregue tantos productos como quiera a las líneas de la orden.

En la pestaña Productos opcionales , introduzca cualquiera de los productos opcionales que el cliente pueda añadir a su cotización antes de confirmar la orden.

Si el plan de suscripción tiene términos y condiciones, especiales, agreguelos en la pestaña Términos y Condiciones. Si los términos y condiciones están especificados en un plan, se usarán estos en lugar de los términos y condiciones predeterminados establecidos en los ajustes de la aplicación _Ventas_.

![Pestaña de Términos y Condiciones del plan de suscripción](https://www.odoo.com/documentation/17.0/es/_images/subplan-terms-conditions.png)

## Use los planes de suscripción en las cotizaciones[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/plans.html#use-subscription-plans-on-quotations "Enlazar permanentemente con este título")

Lac cotizaciones para los productos de suscripción se pueden crear tanto en la aplicación _Suscripciones_ como en [*](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/plans.html#id1)Ventas.

Desde el tablero de Suscripciones, haga clic en Nuevo para crear una nueva cotización. Luego, seleccione un plan de suscripción en el campo Plan de suscripción.

La recurrencia, los productos y otros campos del plan se llenan automáticamente. La cotización se puede modificar después si es necesario.

Desde el tablero de Ventas , haga clic en Nuevo para crear una nueva cotización. Luego, seleccione un plan de suscripción en el campo Plantilla de cotización.

Todas las órdenes de suscripción aparecerán en el tablero de Suscripciones sin importar si se crearon en la aplicación _Suscripciones_ or _Ventas_.