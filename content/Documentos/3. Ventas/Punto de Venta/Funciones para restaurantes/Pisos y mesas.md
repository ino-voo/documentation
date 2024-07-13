La **vista de plano del piso** le permite gestionar los pisos del restaurante, cómo están acomodadas las meses y monitorear el estado de las mesas en tiempo real, incluyendo las que están ocupadas, las que tienen reservaciones y las órdenes de cocina.

 Example

![ejemplo de la vista de plano del piso con claves visuales para poder entenderlo.](https://www.odoo.com/documentation/17.0/es/_images/plan-understand.png)

- Mesa 1: se realizó una orden y se envió a la cocina.
    
- Mesa 3: se realizó una orden de cuatro artículos que se debe enviar a la cocina.
    
- Mesas 2, 4 y 5: estas mesas están disponibles.
    
- Mesas 2, 4 y 5: la capacidad total de estas mesas es 2, 4 y 8 respectivamente.
    
- Mesa 1: la mesa de dos está llena.
    
- Mesa 3: la mesa de cuatro la está ocupando una persona.
    
- Mesa 5: «Juan Pérez» tiene una reservación de 8 personas a las 12:00.
    

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant/floors_tables.html#configuration "Enlazar permanentemente con este título")

### Desde el backend del Punto de venta[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant/floors_tables.html#from-the-pos-backend "Enlazar permanentemente con este título")

Para crear pisos y mesas desde el backend, vaya a Punto de venta ‣ Configuración ‣ Diseño del piso y haga clic en Nuevo para crear un piso. Póngale un nombre, seleccione los puntos de venta relacionados y haga clic en Agregar una línea para crear una tabla. Póngale nombre a la tabla, asigne un número de asientos y, si quiere que se pueda reservar la mesa, debe vincularla a un recurso de cita. Una vez que esté listo, haga clic en Guardar y cerrar o en Guardar y crear nuevo.

![ventana para crear una mesa desde el backend del punto de venta](https://www.odoo.com/documentation/17.0/es/_images/table-creation-backend.png)

 Nota

El punto de venta debe estar abierto y [se debe editar desde el frontend](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant/floors_tables.html#floors-tables-frontend) para poder crear un mapa de su restaurante o bar que refleje su plano del visto actual.

 Truco

Puede crear pisos a instante: [ingrese a sus ajustes del punto de venta](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration.html#configuration-settings), ingrese el nombre de su piso en el campo Piso de la categoría Mapa de pisos y mesas y presione _enter_.

![ajuste para crear pisos desde los ajustes del Punto de venta](https://www.odoo.com/documentation/17.0/es/_images/floor-creation-backend.png)

### Desde el frontend del Punto de venta[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant/floors_tables.html#from-the-pos-frontend "Enlazar permanentemente con este título")

Para crear pisos y meses desde el frontend [abra una sesión de punto de venta](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#pos-session-start), haga clic en el icono de las tres rayas ≡ en la esquina superior derecha y después en Editar plan para ingresar en el **modo de edición**.

Haga clic en + Agregar un piso para agregar un piso y después ingrese el nombre en una ventana emergente.

Una vez que se haya creado el piso haga clic en + MESA para agregar una mesa. Para moverla, selecciónela y arrástrela. También puede editar los atributos de la mesa seleccionada, como el número de asientos si hace clic en ASIENTOS, la forma de la mesa si hace clic en FORMA, el color de la mesa si hace clic en RELLENO, o el nombre de de la mesa si hace clic en RENOMBRAR. Si quiere duplicar una mesa existente, selecciónela y haga clic en COPIAR y haga clic en BORRAR si quiere borrarla.

Después de hacer todas las modificaciones necesarias haga clic en CERRAR para guardar.

![la vista del plano del piso en modo edición.](https://www.odoo.com/documentation/17.0/es/_images/floor-map.png)

 Nota

Si no se selecciona ninguna mesa, las modificaciones se aplicarán al piso.

 Advertencia

No se puede deshacer la acción de borrar una besa o un piso.

## Tomar órdenes[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant/floors_tables.html#take-orders "Enlazar permanentemente con este título")

Haga clic en una mesa para acceder a la interfaz del punto de venta y comenzar a tomar la orden de su cliente. El sistema asocia las órdenes a la mesa de forma automática, lo cual le permitirá agregar más artículos después y generar una factura específica para las órdenes de esa mesa.

Una vez que haya tomado la orden haga clic en Cambiar mesa para regresar a la vista del plano del piso.

 Nota

Tan pronto como haga clic a la mesa, el número de invitados automáticamente será uno. Si selecciona una mesa por error, haga clic en Liberar mesa para liberarla o [transferir al cliente](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant/floors_tables.html#floors-tables-transfer) a otra mesa.

## Transferir una mesa[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant/floors_tables.html#table-transfer "Enlazar permanentemente con este título")

Para mover clientes de una mesa a otra, seleccione una mesa y haga clic en → Transferir en la interfaz del punto de venta. Esto le redirige a la vista de plano de planta, donde puede elegir la nueva mesa a la que desea transferir los clientes.

Cuando transfiere clientes, todas las órdenes que se realicen y estén vinculadas a la mesa original también se transfieren.