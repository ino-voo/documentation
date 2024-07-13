[Flutterwave](https://flutterwave.com/) es un proveedor de pago en línea establecido en Nigeria y cubre varios países africanos y métodos de pago.

## Configuración en el tablero de Flutterwave[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/flutterwave.html#configuration-on-flutterwave-dashboard "Enlazar permanentemente con este título")

1. Inicie sesión en [el tablero de Flutterwave](https://dashboard.flutterwave.com/) y vaya a Configuración ‣ API. Copie los valores de los campos Clave pública y Clave secreta y guárdelos para después.
    
2. Vaya a Configuración ‣ Webhooks e ingrese la URL de su base de datos de Odoo seguido de `/payment/flutterwave/webhook` en el campo de texto URL.
    
    Por ejemplo: `https://yourcompany.odoo.com/payment/flutterwave/webhook`.
    
3. Llena los campos Hash secreto con una contraseña que usted cree y guarde su valor para después.
    
4. Asegúrese de que _todas_ las demás casillas estén seleccionadas.
    
5. Haga clic en **Guardar** para finalizar con la configuración.
    

![Ajustes de Flutterwave](https://www.odoo.com/documentation/17.0/es/_images/flutterwave-settings.png)

## Configuración en Odoo[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/flutterwave.html#configuration-on-odoo "Enlazar permanentemente con este título")

1. [Vaya al proveedor de pago Flutterwave](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-add-new) y cambie su estado a Habilitado.
    
2. En la pestaña Credenciales, llene los campos Clave pública, Clave secreta y Webhook secreto con los valores que guardo en el paso [Configuración en el tablero de Flutterwave](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/flutterwave.html#payment-providers-flutterwave-configure-dashboard).
    
3. Configure el resto de las opciones como guste.
    
     Importante
    
    Si elige permitir que se guarden los métodos de pago, se le recomienda que solo active pagos con tarjeta desde el tablero de Flutterwarve, pues solo las tarjetas se pueden guardar como tokens de pago. Para hacerlo, vaya a su tablero de Flutterwave y luego a Configuración ‣ Configuración de la cuenta.
    

 Ver también

- [Pagos en línea](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html)