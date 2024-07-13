[Stripe](https://stripe.com/) es un proveedor de soluciones de pago en línea con sede en Estados Unidos con el que las empresas pueden aceptar **tarjetas de crédito** y otros métodos de pago.

 Ver también

- [Lista de países compatibles con Stripe](https://stripe.com/global)
    
- [Lista de métodos de pago compatibles con Stripe](https://stripe.com/payments/payment-methods)
    

## Cree su cuenta de Stripe con Odoo[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/stripe.html#create-your-stripe-account-with-odoo "Enlazar permanentemente con este título")

El método para obtener sus credenciales depende de su tipo de alojamiento:

Odoo OnlineOdoo.sh or On-premise

1. [Vaya al proveedor de pago Stripe](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-supported-providers) y haga clic en Conectar Stripe.
    
2. Siga el proceso de configuración y confirme su dirección de correo cuando Stripe le envíe un correo de confirmación.
    
3. Al final del proceso, haga clic en Agree and submit (estoy de acuerdo y enviar). Si se envió toda la información solicitada regresará a Odoo y se activará su proveedor de pago.
    

 Truco

- Para usar una cuenta de Stripe existente, [active el modo desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode) y [active Stripe manualmente](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-add-new). Entonces podrá completar sus credenciales, [generar un webhook](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/stripe.html#stripe-webhook) y establecer su proveedor de pago.
    
- También puede probar Stripe con el [Modo de prueba](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-test-mode) (modo de prueba de proveedores de pago). Para hacerlo, primero [inicie sesión en su tablero de Stripe](https://dashboard.stripe.com/dashboard) y cambie al **modo de prueba**. Después en Odoo [active el modo de Desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode), [vaya al proveedor de pago Stripe](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-supported-providers), [llene las credenciales de su API](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/stripe.html#stripe-api-keys) con las claves de prueba y configure elm:guilabel:`Estado` como Modo de prueba.
    

### Introduzca sus credenciales[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/stripe.html#fill-in-your-credentials "Enlazar permanentemente con este título")

Si necesita sus **credenciales API** para conectar con su cuenta de Stripe, haga lo siguiente:

1. Vaya a [la página de claves API de Stripe](https://dashboard.stripe.com/account/apikeys), o inicie sesión en su tablero de Stripe y vaya a Desarrolladores ‣ Claves API.
    
2. En la sección Standard keys (claves estándar) copie la Publishable key (clave que se puede publicar) y la Secret key (clave secreta) y guárdelas para que pueda usarlas después.
    
3. En Odoo [vaya al proveedor de pago de Stripe](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-supported-providers).
    
4. En la pestaña Credenciales llene los campos Clave pública y Clave secreta con los valores que guardó antes.
    

### Genere un webhook[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/stripe.html#generate-a-webhook "Enlazar permanentemente con este título")

Si necesita su **secreto de implementación Webhook** para conectarse con su cuenta de Stripe, puede crear un webhook de manera automática o manual.

Create the webhook automaticallyCreate the webhook manually

Asegúrese de haber completado la información de sus [Claves publicables y secretas](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/stripe.html#stripe-api-keys), luego haga clic en el botón Generar su webhook.

## Habilitar Apple Pay[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/stripe.html#enable-apple-pay "Enlazar permanentemente con este título")

Para permitir que los clientes usen el botón de pago de Apple Pay para pagar sus órdenes de comercio electrónico, vaya a la pestaña Configuración, active Permitir el pago rápido y haga clic en Habilitar Apple Pay.

 Ver también

- [Pago exprés y Google Pay](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-express-checkout)
    
- [Pagos en línea](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html)
    
- [Usar Stripe como terminal de pago en el punto de venta](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/stripe.html)