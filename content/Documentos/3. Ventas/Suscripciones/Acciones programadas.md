_Las acciones programadas_ son procesos preconfigurados que permiten que los usuarios automaticen algunas tareas dentro de la base de datos según un horario designado o un número de ocurrencias. Estas tareas pueden ser enviar correos electrónicos, generar facturas, limpieza de datos y muchas más.

En Odoo algunas acciones programadas están activas de manera predeterminada para asegurar que algunas funciones se activan de manera automática. Sin embargo, _también_ hay varias opciones de acciones programadas que aparecen en la base de datos y _no_ están activas de forma predeterminada.

En la aplicacipon _Suscripciones_ de Odoo hay dos acciones programadas que inician el proceso de facturación para activar suscripciones recurrentes, así como cuándo se debe detener la facturación debido a que una suscripción ya no está activa.

Están activas de forma predeterminada y se pueden desactivar en cualquier momento para gestionar suscripciones de forma manual

## Acceder a las acciones programadas[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/scheduled_actions.html#access-scheduled-actions "Enlazar permanentemente con este título")

 Importante

Para poder acceder a acciones programadas **debe** activar el [modo de desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode).

Con el modo de desarrollador activado, vaya a los Ajustes ‣ Técnicos ‣ Acciones programadas.

![La opción de acciones programadas en el menú técnico de los Ajustes de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/scheduled-actions-technical-settings-page.png)

Al hacerlo se mostrará un tablero de Acciones programadas . En esta página hay una lista completa de acciones programadas para toda la base de datos.

Escriba `Suscripción` en la barra de búsqueda. Al hacerlo se mostrarán resultados específicos de la suscripción. La siguiente documentación se centra en los últimos dos resultados de la lista:

- Suscripción de venta: Generar pagos y facturas recurrentes
    
- Suscripción de venta: Vencimiento de suscripciones
    

![Los resultados relacionados a las suscripciones en la página de acciones programadas en los ajustes de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/scheduled-actions-page-subscription-results.png)

Para determinar si una acción programada está activa busque en la columna Activo en la hilera correspondiente en el tablero de Acciones programadas hasta que encuentre una casilla de verificación marcada. Si la casilla de verificación está en verde con una marca de comprobación, la acción programada está activa.

Si la acción programada se debe activar, haga clic en la acción programada que quiera activar de la lista.

![La acción programada desde los Ajustes de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/scheduled-action-form.png)

Después, desde el formulario de acción programada, cambie el activador que se encuentra en el campo Activo de la derecha. Al hacerlo se convertirá a verde, lo cual indica que la acción programada ahora está `Activa`.

También puede programar la frecuencia con la que se activa una acción programada desde el formulario de acción, en el campo Ejecutar cada.

 Importante

La acción programada **no** funciona correctamente si el tiempo de ejecución es menor a cinco minutos. Esta es una regla general para todas las acciones programadas.

Para más información, lea la documentación [Preguntas técnicas más frecuentes](https://www.odoo.com/documentation/17.0/es/administration/odoo_sh/advanced/frequent_technical_questions.html).

## Generar facturas y pagos recurrentes[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/scheduled_actions.html#generate-recurring-invoices-and-payments "Enlazar permanentemente con este título")

Para que la acción programada Venta de suscripción: generar facturas y pagos recurrentes genere facturas y pagos en suscripciones de forma adecuada, las cuentas _Gastos diferidos_ e _Ingresos diferidos_ **deben** configurarse para que Odoo pueda procesar varias facturas y pagos relacionados a la suscripción.

Para configurar las cuentas de _Gastos diferidos_ e _Ingresos diferidos_, vaya a la aplicación Contabilidad ‣ Configuración ‣ Ajustes. Ambas cuentas se pueden configurar en la sección Cuentas predeterminadas.

![Los ajustes necesarios de la cuenta diferida en la página de ajustes de Contabilidad de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/deferred-settings-accounting.png)

Una vez que las cuentas correctas se ingresaron en los campos desplegables Gastos diferidos e Ingresos diferidos, haga clic en Guardar en la esquina superior izquierda.

### Crear factura[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/scheduled_actions.html#create-invoice "Enlazar permanentemente con este título")

Los elementos relacionados a la acción programada Venta de suscripción: generar facturas y pagos recurrentes se pueden encontrar en órdenes de venta de suscripciones confirmadas.

Para examinar estos elementos, abra cualquier orden de venta confirmada en la aplicación _Suscripciones_ para mostrar el formulario de la orden de venta de suscripción.

En un formulario de orden de venta de suscripción confirmado, fíjese en los campos Plan recurrente y Fecha de la siguiente factura.

![Una orden de venta de suscripción confirmada en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/confirmed-subscription-sales-order-fields.png)

La acción programada crea una factura cuando la fecha de hoy es la misma que la Fecha de la siguiente factura.

Odoo usa la información en el campo Plan recurrente para actualizar la fecha de la siguiente factura.

 Advertencia

Si no hay un proveedor de pagos configurado, Odoo **no** creará una factura y no se le cobrará al cliente. Lo que ocurrirá es que la suscripción se procesará como un producto recurrente gratuito y así aparecerá en el _chatter_ de la orden de venta de la suscripción. El mensaje `Renovación automática exitosa. Suscripción sin costo. Siguiente factura: [fecha]. No se envió un correo electrónico` aparecerá cuando esto ocurra.

Ya que se cree la factura para la orden de venta de la suscripción, podrá ver la factura si hace clic en el botón inteligente Facturas que aparece en la parte superior de la orden ce venta.

Se le envía un correo electrónico al cliente en el que se le notifica el cargo de la suscripción recurrente _si_ hay un Token de pago en la cuenta.

Para revisar si hay un Token de pago abra la pestaña Otra información y busque el campo Token de pago bajo la sección Suscripción.

![El campo de Token de pago bajo la pestaña Otra información en un formulario de orden de venta de suscripción.](https://www.odoo.com/documentation/17.0/es/_images/payment-token-field.png)

Si no hay un token de pago (es decir, si el proveedor de pago es `Transferencia bancaria`), la factura se crea y se le envía al cliente. El pago **debe** registrarse de forma manual en este caso.

### Cerrar facturas[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/scheduled_actions.html#closing-invoices "Enlazar permanentemente con este título")

La acción programada Venta de suscripción: generar facturas y pagos recurrentes también le permite cerrar una suscripción si se cumplen con las siguientes condiciones:

- Si la suscripción no tiene un token de pago, cree y publique la factura.
    
- Si la suscripción tiene un token de pago, haga un cambio.
    
    > - Si el cambio se realiza con éxito, cree y publique la factura.
    >     
    > - Si el cambio falla, envíe recordatorios de manera periódica.
    >     
    >     > - Si el cambio sigue fallando por más de catorce días, cierre la suscripción.
    >     >     
    >     
    

## Vencimiento de las suscripciones[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/scheduled_actions.html#subscriptions-expiration "Enlazar permanentemente con este título")

La acción programada Venta de suscripción: vencimiento de la suscripción revisa todas las condiciones que pueden hacer que una suscripción se cierre de forma automática. Si se cumple alguna condición, la acción programada cerrará esa suscripción.

Primero, la acción Venta de suscripción: vencimiento de la suscripción revisa si la fecha de vencimiento ya pasó. Esta fecha está configurada en la orden de venta de suscripción.

![La fecha de vencimiento en una orden de venta de suscripción en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/subscription-expiration-date.png)

Después, la acción programada Venta de suscripción: vencimiento de la suscripción revisa si la factura no se ha pagado antes de la fecha límite de los términos de pago

Para acceder a las facturas adjuntas a una suscripción, acceda a la orden de ventas para el producto de suscripción y haga clic en el botón inteligente Facturas. Después, vea la columna Fecha de facturación.

![La columna Fecha de facturación en la página de facturas de las suscripciones en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/invoices-invoice-date-column.png)

Las suscripciones sin pagar con una Fecha de factura que ya pasó el número determinado de días en el campo Cierre automático de un Plan recurrente se cierran de manera automática con la acción programada Suscripción de venta: Vencimiento de suscripciones.

![El campo de cierre automático en un formulario de plan recurrente en suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/automatic-closing-field.png)

Por ejemplo, si la fecha de la siguiente factura es el 1 de julio y el Cierre automático está configurado a “30 días”, la acción programada cerrará la suscripción el 1 de agosto.

 Ver también

- [Suscripciones](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions.html)
    
- [Planes de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/plans.html)
    
- [Productos de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/products.html)
    
- [Reglas de automatización](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/automatic_alerts.html)