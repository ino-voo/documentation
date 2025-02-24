La aplicación **Ventas** de Odoo permite que los clientes confirmen sus órdenes con una firma electrónica desde la orden de venta. Una vez que el cliente firma de manera electrónica la orden de venta, el vendedor asignado a la orden recibe una notificación al instante sobre la confirmación de esa orden de venta.

## Activar la firma en línea[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/get_signature_to_validate.html#activate-online-signatures "Enlazar permanentemente con este título")

La función _Firma en línea_ **debe** estar habilitada para que los clientes puedan confirmar sus órdenes mediante una firma en línea.

Para activar la función para _firmar en línea_, vaya a aplicación Ventas ‣ Configuración ‣ Ajustes, baje hasta la sección de Cotizaciones y órdenes y active la función de Firma en línea haciendo clic en la casilla de a lado.

![La opción de la función de firma en línea en los ajustes de la aplicación Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/signature-setting.png)

Luego, haga clic en Guardar que se ubica en la parte superior izquierda.

 Nota

Al hacer una plantilla de cotización, la función de firma en línea es la opción de firma que se ubica en el campo confirmación en línea del formulario de la plantilla de cotización.

![La opción de firma de confirmación en línea que se encuentra en cada plantilla de cotización de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/signature-feature-quotation-template.png)

En plantillas de cotización estándar, la función de firma en línea es la opción Firma que se ubica en la pestaña Otra información en el formulario de la cotización.

![La opción firma de confirmación en línea en la pestaña Otra información en un formulario de cotización en Odoo.](https://www.odoo.com/documentation/17.0/es/_images/signature-other-info-tab.png)

## Confirmaciones de órdenes con firmas en línea[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/get_signature_to_validate.html#order-confirmations-with-online-signatures "Enlazar permanentemente con este título")

Cuando un cliente accede a una cotización en línea a través de su portal de cliente, podrá ver un botón para Firmar y pagar directamente en la cotización.

![El botón Firmar y pagar presente en las cotizaciones en línea de Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/sign-and-pay-button.png)

Al hacer clic sobre él, aparecerá una ventana emergente para validar la orden. El campo Nombre completo se completa de manera automática según la información de contacto en la base de datos.

![La ventana emergente para Validar la orden para firmas en línea en Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/validate-order-popup.png)

Después, los clientes tienen la opción de firmar en línea con cualquiera de las siguientes opciones: automático, trazar, o subir.

Automático permite que Odoo genere de manera automática una firma electrónica según la información que aparece en el campo Nombre completo. Trazar le permite al cliente usar el cursor para crear una firma personalizada directamente desde la ventana emergente. Subir deja que el cliente suba un archivo de una firma ya creada desde su computadora.

Después de que el cliente haya elegido una de las tres opciones anteriores para firmar (automático, trazar, o subir), deberán hacer clic en Aceptar y firmar.

Al hacerlo, aparecerán los diferentes métodos de pago disponibles de entre los que podrán elegir el que prefieran (solo si la opción _pago en línea_ aplica para esta cotización).

Cuando la cotización esté pagada y confirmada, se creará de manera automática una orden de envío (si está instalada la aplicación _Inventario_ de Odoo).

 Ver también

- [Plantillas de cotización](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/quote_template.html)
    
- [Confirmación de orden de pago en línea](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/get_paid_to_validate.html)