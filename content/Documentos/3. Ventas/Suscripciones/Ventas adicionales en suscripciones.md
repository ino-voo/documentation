Las suscripciones son recurrentes y continúan durante un tiempo indefinido, así que es posible que en algún momento los clientes deseen modificarlas. Por lo tanto, es indispensable poder adaptar los precios o cambiar las cantidades para satisfacer cualquier necesidad. Es en este contexto donde surge la oportunidad de realizar una venta adicional en una suscripción.

Una venta adicional podría ser buena para los siguientes tipos de clientes:

1. _Clientes leales_
    
    Estos son los clientes que ya confían en su empresa o marca y, como ya cuentan con un patrón de pago establecido para ciertos productos o servicios, existe mayor confianza durante el momento en que intente venderles un producto o servicio más caro.
    
2. _Nuevos clientes_
    
    Estos son los clientes nuevos que no están familiarizados con su empresa o marca, así que debe emplear una táctica nueva y llamativa para persuadirles a comprar un producto o servicio más caro.
    
    > Los descuentos pueden ser útiles en un caso como este. Por lo general, las suscripciones terminan después de cierto tiempo.
    > 
    > Entonces, si ofrece productos o servicios más costosos a los nuevos clientes con un descuento, es posible que logre venderlos y que al mismo tiempo establezca una fuerte sensación de confianza entre el cliente y su empresa o marca. Además, esto puede aumentar la retención de clientes, ya que con el paso del tiempo se sentirán más cómodos y tendrán más confianza.
    

## Configuración de descuentos[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/upselling.html#discount-configuration "Enlazar permanentemente con este título")

Para poder realizar ventas adicionales con descuentos en una suscripción para un nuevo cliente **debe** habilitar la función _Descuentos_.

Vaya a la aplicación Ventas ‣ Configuración ‣ Ajustes para activar la función de _descuentos_. Diríjase a la sección Precios, seleccione la casilla junto a Descuentos y haga clic en Guardar.

![Activación de la opción de descuento en la aplicación Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/configuration-to-upsell-a-subscription.png)

Una vez que haya habilitado esa función podrá proporcionar descuentos en las líneas de las órdenes de ventas.

### Ventas adicionales en suscripciones[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/upselling.html#id1 "Enlazar permanentemente con este título")

Antes de realizar una venta adicional para una suscripción, consulte nuestra documentación sobre cómo [crear una cotización](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions.html) con productos de suscripción.

Al confirmar una cotización con una suscripción, esta se convierte en una orden de venta y se crea una nueva suscripción en la aplicación _Suscripciones_ de Odoo.

 Nota

**Debe** facturar la orden de venta de la suscripción _antes_ de poder realizar una venta adicional.

Al abrir la orden de venta de la suscripción, ya sea desde la aplicación _Ventas_ o _Suscripciones_, puede realizar una venta adicional para esa suscripción con el botón Venta adicional ubicado en la parte superior de la orden de venta.

![El botón "Venta adicional" en la orden de venta de la suscripción en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/upsell-your-subscription.png)

Al hacer clic en el botón Venta adicional aparece un nuevo formulario de cotización con el indicador de estado Venta adicional en la esquina superior derecha. El producto de suscripción inicial ya se encuentra en la pestaña Líneas de la orden.

Debajo del producto de suscripción inicial en la pestaña Líneas de la orden también aparece una advertencia para recordarle al usuario que los productos recurrentes tienen descuentos según el periodo prorrateado.

 Importante

El importe prorrateado **solo** se aplica a los tipos de productos _Servicio_ y **no** aplica a los tipos de productos _Consumible_ o _Almacenables_, incluso si aparece el mensaje.

Agregue nuevos productos de suscripción en la pestaña Líneas de la orden del nuevo formulario de cotización de venta adicional. Haga clic en Agregar un producto y seleccione el producto de suscripción deseado.

![Agregar productos a su suscripción a través de la opción de venta adicional en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/use-of-the-upsell-button-in-odoo-sales.png)

Una vez que haya agregado los productos de suscripción adicionales correspondientes puede enviárselos al cliente para que los apruebe, solo haga clic en el botón Enviar por correo electrónico.

 Importante

Cuando los clientes confirman la cotización, los productos de venta adicional se agregan a la suscripción inicial. Los precios de las cotizaciones se reparten entre el tiempo restante del periodo de facturación actual.

 Nota

Antes de enviar la nueva cotización al cliente puede aplicar el precio unitario, los impuestos e incluso el descuento.

Después de que el cliente haya realizado la aprobación, haga clic en el botón Confirmar en la cotización para convertirla en una orden de venta. Después de realizar esa acción, aparece el botón inteligente Historial de ventas que muestra cuántas órdenes de venta están vinculadas a esta orden de suscripción inicial.

Al hacer clic en el botón inteligente Historial de ventas, Odoo abre una página que incluye la lista de las órdenes de venta relacionadas y su respectivo estado de suscripción.

![La orden de venta relacionada visible desde el botón inteligente Historial de ventas en la aplicación Suscripciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/sales-history-smartbutton.png)

 Ver también

- [Suscripciones](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions.html)
    
- [Planes de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/plans.html)
    
- [Productos de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/products.html)
