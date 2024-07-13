Usar un lector de códigos de barras para procesar las órdenes de su punto de venta aumenta la eficiencia a la hora de ofrecer un servicio al cliente más rápido. Puede usar un lector de código de barras tanto para escanear productos como para registrar a empleados en una sesión de PdV.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/barcode.html#configuration "Enlazar permanentemente con este título")

Para usar un lector de códigos de barras, primero debe habilitar la función en la aplicación Inventario. Vaya a Inventario ‣ Configuración ‣ Ajustes y en la sección código de barras seleccione la opción lector de código de barras y guarde.

![Ajustes de códigos de barras en la aplicación Inventario](https://www.odoo.com/documentation/17.0/es/_images/barcode-inventory.png)

 Ver también

- [Configurar un lector de código de barras](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html)
    
- [Activar lectores de códigos de barra](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/software.html)
    

Una vez que habilite la función de códigos de barras en **Inventario**, puede usarla en la aplicación **Punto de venta** con productos que tengan un número de código de barras asignado.

## Asignar códigos de barras[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/barcode.html#assign-barcodes "Enlazar permanentemente con este título")

### A productos[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/barcode.html#to-your-products "Enlazar permanentemente con este título")

Para poder usar esta función en PdV sus productos deben tener códigos de barras asignados. Para hacerlo, vaya a Punto de venta ‣ Productos ‣ Productos y abra el **formulario de un producto**. Agregue un número de código de barras en el campo código de barras en la pestaña información general.

### A empleados[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/barcode.html#to-your-employees "Enlazar permanentemente con este título")

Para asignarle un número de identificación a un empleado, vaya a la aplicación **Empleados** y abra el **formulario del empleado**. Elija un número de identificación para el empleado y complete el campo código NIP en la pestaña ajustes de RR. HH..

## Usar códigos de barras[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/barcode.html#use-barcodes "Enlazar permanentemente con este título")

### Escanear productos[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/barcode.html#scan-products "Enlazar permanentemente con este título")

Escanee el código de barras de un producto con un lector de códigos de barras. Hacer esto agrega el producto directamente al carrito. Para cambiar la cantidad, escanee un producto las veces que sea necesario, o haga clic en cant. e introduzca el número de productos mediante el teclado.

También puede introducir de forma manual el código de barras en la barra de búsqueda para buscar el producto. Solo haga clic en él para agregarlo al carrito.

### Registrar empleados[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/barcode.html#log-employees "Enlazar permanentemente con este título")

También puede utilizar un lector de códigos de barras para registrar a sus empleados. Para hacerlo, [restrinja el acceso](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/employee_login.html#employee-login-configuration) al PdV y [utilice los códigos de barras para que sus empleados inicien sesión](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/employee_login.html#employee-login-badge) en su PdV.