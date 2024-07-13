[AsiaPay](https://www.asiapay.com/) es un proveedor de pago en línea establecido en Hong Kong y cubre varios países asiáticos y métodos de pago.

## Configuración en el tablero de AsiaPay[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/asiapay.html#configuration-on-asiapay-dashboard "Enlazar permanentemente con este título")

1. Inicie sesión en el tablero de AsiaPay según la cuenta que le dieron.
    
    - [PayDollar](https://www.paydollar.com/b2c2/eng/merchant/index.jsp): para mercados de HK, CN, MO, TW, SG, MY, IN, VN, NZ y AU.
        
    - [PesoPay](https://www.pesopay.com/b2c2/eng/merchant/index.jsp): para el mercado de PH
        
    - [SiamPay](https://www.siampay.com/b2c2/eng/merchant/index.jsp): para mercado de TH
        
    - [BimoPay](https://www.bimopay.com/b2c2/eng/merchant/index.jsp): para mercado de ID
        
2. Vaya a Perfil ‣ Información de la cuenta. Copia los valores de los campos Divisa y Hash seguro y guárdelos para más tarde.
    
3. Vaya a Perfil ‣ Configuración de pago de la cuenta y active la opción Enlace del valor de retorno (Datefeed)
    
    Ingrese la URL de su base de datos de Odoo, seguido de `/payment/asiapay/webhook` en los campos de texto Enlace del valor de retorno (Datafeed). Por ejemplo: `https://yourcompany.odoo.com/payment/asiapay/webhook`;
    
    Haga clic en Probar para comprobar que el webhook está funcionando correctamente.
    
4. Haga clic en Actualizar para finalizar con la configuración.
    

## Configuración en Odoo[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/asiapay.html#configuration-on-odoo "Enlazar permanentemente con este título")

1. [Vaya al proveedor de pago AsiaPay](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-add-new) y cambie su estado a Habilitado.
    
2. En la pestaña de Credenciales seleccione la Marca de su cuenta de Asiapay. Después, llene identificación de comerciantes, el Secreto de hash seguro y la Divisa en la pestaña de Configuración con los valores que guardaste en el paso [Configuración en el tablero de AsiaPay](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/asiapay.html#payment-providers-asiapay-configure-dashboard);
    
    De manera predeterminada, el proveedor de pago AsiaPay está configurado para verificar el hash secreto con la función hash `SHA1`. Si una función diferente está [establecida en su cuenta](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/asiapay.html#payment-providers-asiapay-configure-dashboard), active el [modo desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode) y establezca el mismo valor en el campo Función hash segura en la pestaña de Credenciales.
    
3. Configure el resto de las opciones como guste.
    

 Ver también

- [Pagos en línea](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html)