La función **pantalla del cliente** le brinda a los clientes actualizaciones del proceso de pago en tiempo real en una pantalla secundaria.

![pantalla del cliente](https://www.odoo.com/documentation/17.0/es/_images/display.png)

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/customer_display.html#configuration "Enlazar permanentemente con este título")

Según la configuración de su Punto de venta las funciones se pueden mostrar [en la pantalla principal o en una secundaria](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/customer_display.html#customer-display-local) o en [otro monitor que esté conectado a una caja IoT](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/customer_display.html#customer-display-iot).

Para activar la función, vaya a los ajustes del PdV, busque la sección Dispositivos conectados y seleccione la casilla Pantalla del cliente.

![Casilla de la función Pantalla del cliente.](https://www.odoo.com/documentation/17.0/es/_images/feature-setting.png)

### Local[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/customer_display.html#local "Enlazar permanentemente con este título")

Conecte una segunda pantalla a su PdV y [abra una sesión de PdV](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#pos-session-start). Haga clic en Pantalla del cliente para abrir una nueva ventana, deberá arrastrarla y soltarla en la segunda pantalla.

### Caja IoT[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/customer_display.html#iot-box "Enlazar permanentemente con este título")

Conecte una caja IoT a su base de datos y la segunda pantalla a la caja IoT. Después, vaya a Punto de Venta ‣ Configuración ‣ Ajustes, diríjase a la sección Dispositivos conectados, seleccione la casilla Caja IoT y elija el segundo monitor en el campo Pantalla del cliente.

![Función de la caja IoT para conectar una pantalla del cliente.](https://www.odoo.com/documentation/17.0/es/_images/iot-setting.png)

 Nota

Ambos dispositivos deben estar conectados a la misma red local.

 Ver también

[Utilizar una caja IoT con un PdV](https://www.odoo.com/documentation/17.0/es/applications/general/iot/config/pos.html)