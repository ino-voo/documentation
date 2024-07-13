[Buckaroo](https://www.buckaroo.eu/) es una empresa neerlandesa que ofrece varias posibilidades de pago en línea.

## Configuración en Buckaroo Plaza[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/buckaroo.html#configuration-on-buckaroo-plaza "Enlazar permanentemente con este título")

1. Inicie sesión en [Buckaroo Plaza](https://plaza.buckaroo.nl/), vaya a Mi Buckaroo ‣ Sitios web y seleccione la pestaña Configuraciones push.
    
2. Seleccione la casilla Permitir la respuesta push en la sección Respuestas atrasadas y push.
    
3. Ingrese la URL de su base de datos de Odoo, seguido de `/payment/buckaroo/webhook` en los campos de texto Hacer push en URI de éxito/pendiente y en Hacer push en el fallo URI. Por ejemplo: `https://yourcompany.odoo.com/payment/buckaroo/webhook`.
    
4. Deje los demás campos como están y haga clic en Guardar.
    
5. En la pestaña de General, copie la Clave (la clave que se usa únicamente para identificar su sitio web con Buckaroo) de su sitio web y guárdela para después.
    
6. Vaya a Configuración ‣ Seguridad ‣ Clave secreta, ingrese o Genere una Clave secreta y haga clic en Guardar. Guarde la clave para después.
    

## Configuración en Odoo[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/buckaroo.html#configuration-on-odoo "Enlazar permanentemente con este título")

1. [Vaya al proveedor de pago Buckaroo](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-add-new) y cambie su estado a Habilitado.
    
2. En la pestaña Credenciales, llene los campos Clave del sitio web y Clave secreta con los valores que guardo en el paso [Configuración en Buckaroo Plaza](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/buckaroo.html#payment-providers-buckaroo-configure-dashboard).
    
3. Configure el resto de las opciones como guste.
    

 Ver también

[Pagos en línea](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html)