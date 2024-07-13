La aplicación _Suscripciones_ de Odoo le proporciona flexibilidad a los negocios para que decidan si los clientes pueden autogestionar sus suscripciones o restringir esa capacidad por completo.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/closing.html#configuration "Enlazar permanentemente con este título")

Primero vaya a la aplicación de Suscripción ‣ Configuración ‣ Planes recurrentes. Desde ahí, puede crear un nuevo plan si hace clic en Nuevo o seleccione una existente para modificarla.

Una vez que esté en el formulario de Planes recurrentes active la opción Se puede cerrar en la sección Autoservicio para que los clientes puedan cerrar sus propias suscripciones mediante el portal del cliente.

![La opción se puede cerrar en un plan recurrente en Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/recurring-plans-closable-option.png)

 Ver también

[Configurar planes recurrentes](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/plans.html)

## Cancelar una suscripción[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/closing.html#close-a-subscription "Enlazar permanentemente con este título")

### Vista de administrador[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/closing.html#administrator-view "Enlazar permanentemente con este título")

Después de que se haya confirmado la cotización para un producto de suscripción, se convierte en una orden de ventas y el estado de la suscripción cambia a En progreso.

En ese momento, es posible cerrar la suscripción con el botón Cerrar ubicado en la parte superior de la orden de suscripción, cerca de la fila que incluye la etapa En progreso y algunas otras. Esta opción también está disponible después de haber facturado y registrado el pago.

![Cerrar la suscripción desde el punto de vista de un administrador con Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/close-subscriptions-administrator.png)

Al hacer clic en el botón Cerrar aparecerá una ventana emergente llamada Motivo de la cancelación. Aquí el administrador podrá indicar el motivo por el cual se canceló la suscripción, o elegir desde el menú desplegable de opciones en el campo Razón.

![La ventana emergente de motivo de cancelación cuando se hace clic al botón Cerrar en suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/close-reason-popup.png)

Cuando se ingrese el Motivo haga clic en el botón Enviar.

Al hacer clic en Enviar en la ventana emergente de Motivo de la cancelación se actualiza el pedido de venta de suscripción para mostrar la etiqueta de estado Cancelado, junto con el Motivo de la cancelación especificado.

![Una orden de ventas cancelada para una suscripción en Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/churned-sales-order.png)

El mismo motivo de cierre se puede encontrar en el _Chatter_ de la orden de ventas también.

![El chatter de una orden de venta cancelada para una suscripción cancelada en Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/churned-sales-order-chatter.png)

### Vista del cliente[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/closing.html#customer-view "Enlazar permanentemente con este título")

 Nota

Como administrador, la posibilidad de ver lo que los clientes ven al gestionar sus suscripciones es posible a través del botón Vista previa ubicado en la parte superior de la orden de venta.

Desde el punto de venta del cliente en el portal del cliente, el botón Cancelar suscripción se ubica en el lado izquierdo de la orden de venta.

![Botón para cancelar la suscripción desde la vista de un cliente de una orden de ventas en las Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/close-subscription-button-customer-view.png)

Cuando el cliente hace clic en el botón Cerrar suscripción, aparece una ventana emergente Cerrar suscripción en la que el cliente debe elegir entre una lista de razones por las que decide cerrar la suscripción.

![La ventana emergente de cerrar suscripción que ve el cliente al cerrar la suscripción.](https://www.odoo.com/documentation/17.0/es/_images/close-subscription-customer-pov.png)

 Nota

Los clientes _solo_ pueden elegir un motivo preconfigurado por el que cierran su suscripción. _No_ pueden escribir un motivo personalizado desde el portal del cliente. Ajuste estas opciones desde Suscripciones ‣ Configuración ‣ Motivos de cierre.

Una vez que el cliente haya seleccionado un motivo de cierre, podrán hacer clic en el botón Enviar en la ventana emergente.

Después del cierre, la orden de la suscripción en el portal del cliente se etiqueta como Cerrada.

Además, la etiqueta Motivo de la cancelación especificada aparece en el pedido de suscripción en la aplicación _Suscripciones_ del backend (vista del administrador).

 Ver también

- [Suscripciones](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions.html)
    
- [Planes de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/plans.html)
    
- [Productos de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/products.html)