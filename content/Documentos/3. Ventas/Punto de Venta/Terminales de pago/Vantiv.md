Conectar una terminal de pago Vantiv le permite ofrecerle a sus clientes un flujo de pago ágil y facilitar el trabajo de sus cajeros.

 Nota

Tome en cuenta que MercuryPay solo funciona con bancos de Estados Unidos y Canadá, lo que hace que este procedimiento sea adecuado solo para empresas norteamericanas.

 Advertencia

Si va a usar los lectores de tarjetas de Vantiv, los debe comprar directamente de Vantiv, ya que muchas terminales de Vantiv que se compran por Amazon no incluyen la encriptación correcta necesaria para que se puedan utilizar con una base de datos de Odoo.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/vantiv.html#configuration "Enlazar permanentemente con este título")

### Configure el método de pago[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/vantiv.html#configure-the-payment-method "Enlazar permanentemente con este título")

Active la terminal de pago en la sección Terminales de pago de [los ajustes de la aplicación](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration.html#configuration-settings).

Después vaya a Punto de venta ‣ Configuración ‣ Métodos de pago y [cree el método de pago relacionado](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods.html). Establezca el tipo de diario como Banco y seleccione Vantiv en el campo Usar una terminal de pago.

Ingrese el nombre que le quiere dear a las Credenciales Vantiv y haga clic en Crear y editar. Ingrese su ID de comerciante y su Contraseña de comerciante y después haga clic en Guardar y cerrar.

![Método de pago Vantiv](https://www.odoo.com/documentation/17.0/es/_images/vantiv-method.png)

Ya que haya creado el método de pago, puede seleccionarlo en sus ajustes del punto de venta. Para hacerlo, vaya a los [ajustes del punto de venta](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration.html#configuration-settings) y agregue el método de pago en la sección Pago.

## Pagar con una terminal de pago[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/vantiv.html#pay-with-a-payment-terminal "Enlazar permanentemente con este título")

Al procesar un pago, seleccione el método de pago relacionado. Revise el importe y haga clic en Enviar. En cuanto se realice el pago, el estado cambia a Pago exitoso.