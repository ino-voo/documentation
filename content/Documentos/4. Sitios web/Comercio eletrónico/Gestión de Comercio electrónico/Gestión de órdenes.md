Cuando un cliente realiza una orden en su sitio web hay **tres** tipos de registro que se necesitan gestionar en Odoo:

- [Órdenes de venta](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/order_handling.html#handling-sales);
    
- [Órdenes de entrega](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/order_handling.html#handling-delivery);
    
- [Facturas y requisitos legales](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/order_handling.html#handling-legal).
    

## Orden de venta[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/order_handling.html#sales-orders "Enlazar permanentemente con este título")

### Estado de la orden y del pago[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/order_handling.html#order-and-payment-status "Enlazar permanentemente con este título")

El primer paso después de que un cliente agrega un producto a su carrito es la creación de una cotización. Las órdenes se pueden gestionar ya sea desde el **sitio web** o desde la aplicación [Ventas](https://www.odoo.com/documentation/17.0/es/applications/sales/sales.html). Para que las órdenes del comercio electrónico se asignen a un equipo de ventas en específico primero vaya a Sitio web ‣ Configuración ‣ Ajustes. En la sección **Tienda - Proceso de pago** seleccione un Equipo de ventas o un Vendedor que gestione las órdenes del comercio electrónico.

![Asignación de las órdenes en línea a equipos de venta o a un vendedor](https://www.odoo.com/documentation/17.0/es/_images/handling-salesteam.png)

Puede encontrar las órdenes en Sitio web ‣ Comercio electrónico ‣ Órdenes sin pagar. Cada orden tiene un estado diferente:

- **Cotización**: se agrega un nuevo producto al carrito, pero el cliente _no_ ha pasado por el proceso de cambio todavía;
    
- **Cotización enviada**: el cliente ya pasó el proceso de pago y confirmó la orden, pero el pago no se ha confirmado todavía;
    
- **Orden**: el cliente ya pasó por el proceso de pago, ya confirmó la orden y el pago se recibió.
    

![Estados de las órdenes del comercio electrónico](https://www.odoo.com/documentation/17.0/es/_images/handling-status.png)

### Carrito abandonado[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/order_handling.html#abandoned-cart "Enlazar permanentemente con este título")

Un **carrtio abandonado** representa una orden para la cual el cliente **no terminó** el proceso de confirmación de pago. Para estas órdenes es posible enviar un **correo de recordatorio** al cliente. Para activar esta función vaya a Sitio web ‣ Configuración ‣ Ajustes y en la sección Marketing por correo electrónico active Envío automático de correos electrónicos de pagos abandonados. Una vez que active esta opción, podrá configurar **cuánto tiempo** después se debe enviar el correo, además de que podrá personalizar la **plantilla de correo** que se use.

 Nota

Para correos de carritos abandonados, el cliente deben haber ingresado sus detalles de contacto durante el proceso de pago, o debe haber iniciado sesión cuando agregó el producto a su carrito.

## Órdenes de entrega[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/order_handling.html#delivery-orders "Enlazar permanentemente con este título")

### Flujo de entrega[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/order_handling.html#delivery-flow "Enlazar permanentemente con este título")

Una vez que se confirmó la cotización, se creará una orden de entrega de manera automática. El siguiente paso es procesar la entrega.

Empacar las órdenes del comercio electrónico usualmente requiere recolectar el producto, preparar el empaquetado, imprimir la (o las) etiqueta de envío y enviar el producto al cliente. Dependiendo del número de órdenes, la estrategia o los recursos, estos pasos se pueden considerar como una o varias acciones dentro de Odoo.

Se le puede enviar un correo electrónico automático al cliente cuando el estado de transferencia en Odoo sea «listo». Para hacerlo, active la función en los ajustes de la aplicación [Inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory.html).

 Nota

Si los clientes pueden realizar su pago al recoger su orden en tiendas o por transferencia bancaria, la cotización **no** se confirmará y el inventario **no** se reservará. Las órdenes se deben confirmar de manera manual para reservar los productos en el inventario.

 Ver también

- [Facturación del costo de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/invoicing.html)
    
- [Imprimir etiquetas de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html)
    
- [Envío en varios paquetes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/multipack.html)
    

### Devoluciones y reembolsos[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/order_handling.html#returns-and-refunds "Enlazar permanentemente con este título")

Los clientes solo pueden realizar la devolución de una orden mediante un formulario en línea. Es posible que no puedan regresar los productos según la estrategia de devolución o el tipo de producto.

Los reembolsos completos se pueden enviar directamente a los clientes desde la interfaz de la orden. Primero debe activar un proveedor de pago que sea compatible con el reembolso.

 Ver también

- [Devoluciones y reembolsos](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/returns.html)
    
- [Servicios posventa](https://www.odoo.com/documentation/17.0/es/applications/services/helpdesk/advanced/after_sales.html)
    
- [Pagos en línea](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html)
    

## Facturación y requerimientos legales[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/order_handling.html#invoice-and-legal-requirements "Enlazar permanentemente con este título")

El paso final de una orden de comercio electrónico es generar una factura y enviarla al cliente. Dependiendo del tipo de negocio (B2B o B2C) es posible generar una factura de manera automática (B2B) o cuando el cliente la pida (B2C). Este proceso se puede automatizar si (y cuándo) el pago en línea se [confirme](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/order_handling.html#handling-sales).

Para automatizar la facturación vaya a Sitio web ‣ Configuración ‣ Ajustes y en la sección Facturación active la opción Factura automática.