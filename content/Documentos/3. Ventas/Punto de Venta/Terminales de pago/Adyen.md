Si conecta su **terminal de pago Adyen** podrá ofrecer a sus clientes un flujo de pago eficaz y facilitar el trabajo a sus cajeros.

 Importante

- Las terminales de pago Adyen no necesitan una [caja IoT](https://www.odoo.com/documentation/17.0/es/applications/general/iot.html).
    
- Las terminales Adyen se pueden utilizar en muchos países, pero no en todo el mundo. Consulte la [lista de países compatibles con Adyen](https://docs.adyen.com/point-of-sale/what-we-support/supported-languages/).
    
- Adyen funciona solo con empresas que procesan más de **10 millones anuales** o que facturan mínimo **1000 transacciones al mes**.
    

 Ver también

- [Lista de métodos de pago compatibles con Adyen](https://docs.adyen.com/point-of-sale/what-we-support/payment-methods/)
    
- [Lista de terminales Adyen](https://docs.adyen.com/point-of-sale/what-we-support/select-your-terminals/)
    

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/adyen.html#configuration "Enlazar permanentemente con este título")

Primero cree su cuenta de Adyen en el [sitio web de Adyen](https://www.adyen.com/). Después, siga los pasos que se muestran en la pantalla de su terminal para activarla.

 Ver también

[Documentación de Adyen - Guías de inicio rápido para las terminales de pago](https://docs.adyen.com/point-of-sale/user-manuals)

### Generar una clave API de Adyen[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/adyen.html#generate-an-adyen-api-key "Enlazar permanentemente con este título")

La **clave API de Adyen** se utiliza para autenticar las solicitudes de su terminal de Adyen. Para generar una clave API, vaya a su cuenta de Adyen ‣ Desarrolladores ‣ Credenciales de API y **cree** nuevas credenciales o seleccione las que ya **existen**. Haga clic en Generar una clave API y guarde la clave para pegarla en el campo Clave API de Adyen de Odoo al [crear el método de pago](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/adyen.html#adyen-method-creation).

 Ver también

- [Documentos de Adyen - Credenciales API](https://docs.adyen.com/development-resources/api-credentials#generate-api-key).
    

### Ubicar el identificador de terminal Adyen[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/adyen.html#locate-the-adyen-terminal-identifier "Enlazar permanentemente con este título")

El **identificador de terminal de Adyen** es el número de serie de la terminal y se utiliza para identificar el hardware.

Para encontrar este número, vaya a su cuenta de Adyen ‣ Punto de Venta ‣ Terminales, seleccione la terminal que vinculará y guarde su número de serie, después lo pegará en el campo Identificador de terminal de Adyen de Odoo al [crear el método de pago](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/adyen.html#adyen-method-creation).

### Configurar las URL del evento[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/adyen.html#set-the-event-urls "Enlazar permanentemente con este título")

Para que Odoo sepa cuándo se realizó un pago, debe configurar las **URL de eventos** de la terminal. Para ello:

1. Inicie sesión en el [sitio web de Adyen](https://www.adyen.com/).
    
2. Vaya al tablero de Adyen ‣ Punto de venta ‣ Terminales y seleccione la terminal conectada.
    
3. Desde los ajustes de la terminal, haga clic en Integraciones.
    
4. Establezca el campo Cambiar a modo descifrado para editar esta configuración en Descifrado.
    
5. Haga clic en el **icono de lápiz** y escriba la dirección de su servidor, seguida por `/pos_adyen/notification` en el campo URL de eventos.
    
6. Haga clic en Guardar en la parte inferior de la pantalla para guardar los cambios.
    

### Configure el método de pago[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/adyen.html#configure-the-payment-method "Enlazar permanentemente con este título")

Habilite la terminal de pago en los [ajustes de la aplicación](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration.html#configuration-settings) y [cree el método de pago relacionado](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods.html). Establezca el tipo de diario como Banco y seleccione Adyen en el campo Usar una terminal de pago.

Por último, complete los campos obligatorios con su [clave API de Adyen](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/adyen.html#adyen-api), [identificador de terminal de Adyen](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/adyen.html#adyen-identifier) y cuenta de comerciante de Adyen.

![../../../../../_images/payment-method1.png](https://www.odoo.com/documentation/17.0/es/_images/payment-method1.png)

Ya que haya creado el método de pago, puede seleccionarlo en sus ajustes del Punto de venta. Para hacerlo, vaya a los [ajustes del punto de venta](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration.html#configuration-settings), haga clic en Editar y agregue el método de pago en la sección de Pagos.

## Pagar con una terminal de pago[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/adyen.html#pay-with-a-payment-terminal "Enlazar permanentemente con este título")

Al procesar un pago, seleccione Adyen como método de pago. Revise el importe y haga clic en Enviar. En cuanto se realice el pago, el estado cambia a Pago exitoso.

 Nota

- En caso de que haya problemas de conexión entre Odoo y la terminal de pago, puede forzar el pago al hacer clic en forzar hecho, lo que le permite validar la orden.
    
    Esta opción solo está disponible después de recibir un mensaje de error que le informa que la conexión falló.
    
- Para cancelar la solicitud de pago, haga clic en cancelar.