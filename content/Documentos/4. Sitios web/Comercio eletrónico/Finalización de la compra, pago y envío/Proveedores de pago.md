Odoo acepta una serie de [proveedores de pago](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html) en línea para su sitio web, lo que permite que sus clientes paguen con sus métodos de pago preferidos.

 Ver también

- [Usar monederos electrónicos y tarjetas de regalo](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/ewallets_giftcards.html)
    
- [Proceso de pago](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/checkout.html)
    

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/payments.html#configuration "Enlazar permanentemente con este título")

Para configurar proveedores de pago en la aplicación de comercio electrónico vaya a Sitio web ‣ Configuración ‣ Proveedores de pago. Desde aquí, Active los proveedores de pago que desea habilitar en su tienda y configúrelos según sus necesidades.

También puede acceder a los **proveedores de pago** a través de Sitio web ‣ Configuración ‣ Ajustes. En la sección Tienda - Pago puede configurar la domiciliación bancaria SEPA en caso de que desee usarla, además podrá ver otros proveedores. Si utiliza el proveedor de pago Authorize.net puede configurar el [método de captura de pago](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-manual-capture) desde el mismo menú.

Si está usando [PayPal](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html), también es posible activarlo y configurarlo desde aquí.

### Opciones de pago[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/payments.html#checkout-payment-options "Enlazar permanentemente con este título")

Una vez que usted active esto, los clientes podrán elegir el proveedor de pago de su elección durante el **proceso de pago** al llegar al paso Confirmar orden.

![Selección de proveedor de pago al momento de realizar el pago](https://www.odoo.com/documentation/17.0/es/_images/payments-checkout.png)

## Monederos electrónicos y tarjetas de regalo[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/payments.html#ewallets-and-gift-cards "Enlazar permanentemente con este título")

Al realizar el pago, los clientes pueden pagar con un monedero electrónico o con tarjetas de regalo. Para permitir esta opción, vaya a Sitio web ‣ Configuración ‣ Ajustes y en la sección Tienda - Productos active la opción Descuentos y tarjetas de lealtad y regalo.

Una vez que usted active esta opción, los clientes podrán ingresar el **código** de su tarjeta de regalo o pagar con su monedero electrónico al momento de realizar el pago.

![Ingrese el código de la tarjeta de regalo para procesar el pago.](https://www.odoo.com/documentation/17.0/es/_images/payments-ewallets-giftcards.png)

 Ver también

[Usar monederos electrónicos y tarjetas de regalo](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/ewallets_giftcards.html)