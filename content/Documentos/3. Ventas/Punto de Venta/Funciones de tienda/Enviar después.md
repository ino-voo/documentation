La función **Enviar después** le permite vender productos y programar la entrega en una fecha posterior. Es útil, por ejemplo, cuando un producto está agotado o es tan voluminoso que ya necesita enviarlo, también en caso de que por cualquier motivo, el cliente necesite recibir su orden después, etc.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/ship_later.html#configuration "Enlazar permanentemente con este título")

[Vaya a los ajustes del PdV](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration.html#configuration-settings), diríjase a la sección Inventario y habilite Permitir enviar después.

![Ajustes para habilitar y configurar la función Enviar después.](https://www.odoo.com/documentation/17.0/es/_images/settings3.png)

Una vez que haya habilitado esta función podrá:

- Seleccionar un almacén para elegir la ubicación desde donde se enviarán los productos.
    
- Definir una ruta específica o dejar ese campo vacío para usar la ruta predeterminada.
    
- Defina la Política de envío. Si los productos pueden entregarse por separado seleccione guilabel:`Lo antes posible` o Cuando todos los productos estén listos si desea enviar todos los productos al mismo tiempo.
    

 Ver también

- [Métodos de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/delivery_method.html)
    
- [Gestionar almacenes y ubicaciones](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/warehouses_locations.html)
    

## Aplicación práctica[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/ship_later.html#practical-application "Enlazar permanentemente con este título")

1. [Abrir una sesión](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#pos-session-start) y realizar una venta.
    
2. Seleccione un cliente en la pantalla de pago y seleccione Enviar después.
    
3. En la ventana emergente, establezca una fecha de envío y haga clic en Confirmar para ir a la pantalla de pago.
    

![Seleccionar enviar después al pagar.](https://www.odoo.com/documentation/17.0/es/_images/payment.png)

De forma instantánea, el sistema crea una orden de entrega del almacén a la dirección de envío.

 Nota

El cliente seleccionado debe tener una dirección establecida para poder enviar los productos.