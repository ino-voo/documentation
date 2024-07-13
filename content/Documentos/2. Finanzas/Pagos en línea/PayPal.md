[Paypal](https://www.paypal.com/) es un proveedor de pago en líne estadounidense disponible en todo el mundo y es uno de los pocos que no cobran un cargo por suscripción.

 Nota

Aunque PayPal está disponible en [más de 200 países y regiones](https://www.paypal.com/webapps/mpp/country-worldwide), solo [unas cuantas divisas son compatibles](https://developer.paypal.com/docs/reports/reference/paypal-supported-currencies).

## Configuración en PayPal[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#settings-in-paypal "Enlazar permanentemente con este título")

Para acceder a los ajustes de su cuenta de PayPal, inicie sesión en PayPal, abra los Ajustes de la cuenta y abra el menú Pagos en el sitio web.

![Menú de la cuenta de PayPal](https://www.odoo.com/documentation/17.0/es/_images/paypal-account.png)

 Importante

Tenga en cuenta que para que PayPal funcione **en Odoo**, las opciones [retorno automático](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#paypal-auto-return) y [PDT](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#paypal-pdt) **deben** estar activadas.

### Retorno automático[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#auto-return "Enlazar permanentemente con este título")

La función de **Retorno automático** redirige automáticamente a los clientes a Odoo una vez que se procesó el pago.

Desde Pagos en el sitio web, vaya a Preferencias del sitio web ‣ Actualizar ‣ Retorno automático para pagos en el sitio web ‣ Retorno automático y seleccione Activado. Introduzca la dirección de su base de datos de Odoo (por ejemplo, `https://yourcompany.odoo.com`) en el campo URL de retorno y luego haga clic en Guardar.

 Nota

Cualquier URL funciona. Odoo solo necesita que la opción esté activada pues usa otra URL.

### Transferencia de datos de pago (PDT)[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#payment-data-transfer-pdt "Enlazar permanentemente con este título")

La PDT le permite recibir las confirmaciones de los pagos, muestra el estado del pago a sus clientes y verifica la autenticidad de los mismos. Desde Preferencias del sitio web ‣ Actualizar, baje hasta encontrar Transferencia de datos de pago y seleccione Activar.

 Truco

PayPal le muestra su **Token de identificación PDT** tan pronto como estén activadas las opciones [Retorno automático](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#paypal-auto-return) y [Transferencia de datos de pago (PDT)](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#paypal-pdt). Si necesita el **Token de identificación PDT**, desactive y reactive la Transferencia de datos de pago para mostrar el token de nuevo.

### Cuenta opcional PayPal[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#paypal-account-optional "Enlazar permanentemente con este título")

Le recomendamos no pedirle a sus clientes que inicien sesión con su cuenta de Paypal en el momento del pago. Es mejor y más accesible que paguen con una tarjeta de crédito o débito. Para evitar que inicien sesión vaya a Ajustes de la cuenta ‣ Pagos en el sitio web ‣ Actualizar y seleccionarlo como Activado para la Cuenta opcional PayPal.

### Formato de mensajes de pago[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#payment-messages-format "Enlazar permanentemente con este título")

Si uso caracteres acentuados (o algo más que caracteres latinos básicos) para el nombre de sus clientes o direcciones, entonces **debe** configurar el formato de codificación de la solicitud de pago que envia Odoo a PayPal. Si no lo hace, algunas transacciones fallarán sin notificarle.

Para hacerlo, vaya a su [cuenta de producción](https://www.paypal.com/cgi-bin/customerprofileweb?cmd=_profile-language-encoding). Luego, haga clic en Más Opciones y establezca los dos formatos de codificación como UTF-8.

 Truco

- Para pagos encriptados en sitio web y errores EWP_SETTINGS, revise la [documentación de Paypal](https://developer.paypal.com/docs/online/).
    
- Configure su [Cuenta de Paypal Sandbox](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#paypal-testing), luego entre a este [enlace](https://sandbox.paypal.com/cgi-bin/customerprofileweb?cmd=_profile-language-encoding) para configurar el formato de codificación en un entorno de prueba.
    

## Ajustes en Odoo[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#settings-in-odoo "Enlazar permanentemente con este título")

 Ver también

[Activar un proveedor de pago](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-add-new)

Odoo necesita sus **Credenciales API** para conectarse con su cuenta de PayPal. Para hacerlo, vaya a Contabilidad ‣ Configuración ‣ Proveedores de pago y Active PayPal. Luego, introduzca las credenciales de su cuenta de PayPal en la pestaña de Credenciales:

- Correo electrónico: la dirección de correo electrónico para iniciar sesión en Paypal;
    
- Token de identidad: la clave que se usa para verificar la autenticidad de las transacciones.
    

## Entorno de prueba[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#test-environment "Enlazar permanentemente con este título")

### Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/paypal.html#configuration "Enlazar permanentemente con este título")

Gracias a las cuentas sandbox de PayPal, puede probar el flujo de pago completo en Odoo.

Inicie sesión en el [Sitio de desarrolladro de PayPal](https://developer.paypal.com/) usando sus credenciales de PayPal, lo que crea dos cuentas sandbox:

- Una cuenta de negocios (para usar como comerciante, por ejemplo [pp.merch01-facilitator@example.com](mailto:pp.merch01-facilitator%40example.com));
    
- Una cuenta personal predeterminada (para usarla como comprador, por ejemplo, [pp.merch01-buyer@example.com](mailto:pp.merch01-buyer%40example.com)).
    

Inicie sesión en sandbox de PayPal usando la cuenta de comerciante y siga las mismas instrucciones de configuración. Introduzca sus credenciales sanbox en Odoo (Contabilidad ‣ Configuración ‣ Proveedores de pago‣ PayPal en la pestaña de Credenciales, y asegúrese de que el estado esté en Modo de prueba.

Ejecute una transacción de prueba desde Odoo con la cuenta sandbox personal.

 Ver también

- [Pagos en línea](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html)