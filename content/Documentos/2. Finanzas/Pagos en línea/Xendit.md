[Xendit](https://www.xendit.co/) es un proveedor de soluciones de pago con sede en Indonesia que abarca varios países del sudeste asiático. Este proveedor permite que las empresas acepten tarjetas de crédito, así como otros métodos de pago locales.

## Configuración en el tablero de Xendit[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/xendit.html#configuration-on-the-xendit-dashboard "Enlazar permanentemente con este título")

1. Si es necesario, cree una cuenta de Xendit e inicie sesión en el [tablero de Xendit](https://dashboard.xendit.co/).
    
2. Verifique el modo de su cuenta, este se ubica en la esquina superior izquierda de la página. Utilice el Modo de prueba para probar la integración sin realizar cobros a sus clientes. Cambie al Modo en directo una vez que todo esté listo para aceptar pagos.
    
3. Vaya a Configuración: Ajustes en la parte izquierda de la página de la aplicación. Haga clic en [Claves API](https://dashboard.xendit.co/settings/developers#api-keys) en la sección Desarrolladores.
    
4. Haga clic en Generar clave secreta. En el cuadro emergente escriba cualquier nombre de clave API, seleccione Escribir en el permiso Productos de entrada de dinero y Ninguno para todos los demás permisos, haga clic en Generar clave.
    
5. Confirme su contraseña para visualizar su clave API. Copie o descargue la clave y **almacene esta información de forma segura para después**. Esta es la única vez que podrá visualizar o descargar la clave API.
    
6. Una vez que haya terminado, vaya a la parte inferior de la página y busque la sección [Webhooks](https://dashboard.xendit.co/settings/developers#webhooks) para generar el token del webhook.
    
7. En Token de verificación del webhook, haga clic en Ver token de verificación del webhook y después confirme su contraseña para consultar el token. Guárdelo para usarlo después.
    
8. En la sección URL del webhook escriba la URL de su base de datos de Odoo y después agregue `/payment/xendit/webhook` (por ejemplo, `https://ejemplo.odoo.com/payment/xendit/webhook`) en el campo Facturas pagadas. Haga clic en el botón Probar y guardar.
    

## Configuración en Odoo[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/xendit.html#configuration-on-odoo "Enlazar permanentemente con este título")

1. [Vaya al proveedor de pago Xendit](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-add-new) y cambie su estado a Habilitado.
    
2. Complete los campos Clave secreta y Token de webhook con la información que almacenó en el paso de [Configuración en el tablero de Xendit](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/xendit.html#payment-providers-xendit-configure-dashboard).
    
3. Configure el resto de las opciones como guste.
    

 Ver también

[Pagos en línea](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html)