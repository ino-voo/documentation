La base de cualquier modelo de negocio de suscripción son los pagos recurrentes. Los clientes pagan puntualmente un cantidad regular en intervalos específicos a cambio de obtener acceso a un producto o servicio de suscripción.

La renovación de una suscripción es el proceso que se lleva a cabo después de que los clientes, de forma voluntaria, deciden continuar usando (y pagando) un producto o servicio de suscripción.

El proceso de renovación de las suscripciones puede ocurrir en distintos intervalos, como semanal, mensual, anual y otros según la duración del contrato acordado.

La mayoría de las empresas que ofrecen suscripciones prefieren automatizar el proceso de renovación para los clientes, pero en algunos casos, todavía utilizan procesos manuales de renovación.

Con la aplicación _Suscripciones_ de Odoo, una empresa puede gestionar todas sus suscripciones desde un solo lugar. Pueden procesar las renovaciones de forma automática o manual, incluir productos adicionales o ventas adicionales en cada orden de renovación. También pueden procesarlas en vistas por lotes para localizar con rapidez a los clientes que necesitan renovarlas.

## Renovación de suscripciones[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/renewals.html#subscription-renewals "Enlazar permanentemente con este título")

Para renovar una suscripción **debe** confirmar una cotización con un producto de suscripción que cuente con un plan recurrente configurado, esto la convertirá en una orden de venta.

 Nota

- Solo es necesario un producto en particular.
    
- Un servicio de suscripción sigue siendo un producto (aunque sea digital o recurrente).
    

Luego deberá confirmar esa orden de venta. También deberá facturar y registrar el pago del cliente por la suscripción inicial.

Una vez que haya completado esos pasos, aparecerá la etiqueta En progreso en el formulario de la orden de venta y también una serie de botones en la parte superior de la orden de venta, incluido un botón con el texto Renovar.

![El botón "Renovar" en la orden de venta de la suscripción en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/renew-button.png)

Cuando hace clic en el botón Renovar, Odoo presenta una nueva cotización de renovación de forma instantánea y está completa con la etiqueta de Cotización de la renovación.

![Cotización de la renovación en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/renewal-quotation.png)

A partir de este punto puede realizar un flujo de ventas estándar para confirmar la cotización. Haga clic en Enviar por correo electrónico, de esta forma el cliente recibirá una copia de la cotización para que la confirme y, eventualmente, la pague.

 Nota

En el _chatter_ de la cotización de renovación se menciona que esta suscripción es la renovación de la suscripción de la orden de venta original.

Una vez que confirma la cotización de renovación, esta se convierte en una orden de venta y aparece el botón inteligente Historial de ventas en la parte superior de la página.

![Botón inteligente "Historial de ventas" en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/sales-history-smart-button.png)

Al hacer clic en el botón inteligente Historial de ventas, Odoo abre una página que muestra las distintas órdenes de venta adjuntas a esta suscripción y su respectivo estado.

![Cotización de la renovación en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/sales-history-page.png)

Además, una vez que haya confirmado la cotización de renovación, también aparece el botón inteligente MRR en la parte superior de la orden de venta.

![Botón inteligente "MRR" en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/mrr-smart-button.png)

Una vez que hace clic, Odoo abre la página de Análisis de MRR. Allí se detallan los ingresos recurrentes mensuales relacionados con esta suscripción en específico.

 Ver también

- [Suscripciones](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions.html)
    
- [Planes de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/plans.html)
    
- [Productos de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/products.html)