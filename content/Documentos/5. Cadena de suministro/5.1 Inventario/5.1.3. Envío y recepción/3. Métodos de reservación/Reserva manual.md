Al contrario del método de reservación _en la confirmación_, el método de reservación _manual_ **no** reserva los productos de forma automática.

En su lugar, una vez que se confirma la orden de venta, la disponibilidad de un producto se **debe** revisar de manera manual y la cantidad necesaria se **debe** revertir de forma manual.

 Ver también

[Métodos de reservación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods.html)

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/manually.html#configuration "Enlazar permanentemente con este título")

Para configurar el método de reservación a _Manual_ navegue a la aplicación Inventario ‣ Configuración ‣ Tipos de operaciones. Después, seleccione el Tipo de operación que configurará, o cree uno nuevo haciendo clic en Nuevo.

En la pestaña General localice el campo Método de reserva y seleccione Manual.

![El campo de método de reserva en el formulario de tipo de operación orden de envío.](https://www.odoo.com/documentation/17.0/es/_images/manually-operations-type.png)

 Nota

Cuando el Tipo de operación se cambia a Recepción en un formulario de Tipos de operación, los métodos de reservación **no** están disponibles.

## Flujo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/manually.html#workflow "Enlazar permanentemente con este título")

Para ver cómo funciona el método de reservación _Manual_ cree una [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/manually.html#id1) nueva desde la aplicación de Ventas ‣ Nuevo.

Agregue un client en el campo Cliente. Luego, en la pestaña Líneas de la orden haga clic en Agregar un producto y desde el menú desplegable seleccione un producto que agregar a la cotización. Finalmente, en la columna Cantidad ajuste la cantidad que quiere vender del producto.

Cuando esté listo, confirme la orden de venta.

Haga clic en el icono verde 📈 (gráfico) que se encuntra en la línea del producto para mostrar la información sobre la Disponibilidad. Esta herramienta muestra el número de unidades reservadas para esta orden. Ya que el método de reservación es _manual_, la cantidad Reservada será `0 Unidades`.

Sin embargo, debajo de esa cantidad se leerá `Existencias disponibles`. Esto se debe a que la cantidad está disponible, pero se debe reservar de forma manual.

 Nota

Si **no** hay suficiente cantidad de existencias de un producto que aparece en una [|orden de ventas|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/manually.html#id3), el icono de 📈 (gráfico) aparecerá rojo en lugar de verde.

En lugar de mostrar el número reservado de unidades para una orden, la disponibilidad se lee como Reservado y muestra el número de unidades disponibles (por ejemplo, `0 unidades`).

Además, a no ser de que haya un reabastecimiento o una recepción programada, también leerá No hay disponibilidad futura, en texto rojo.

![Orden de venta confirmada con la disponibilidad seleccionada.](https://www.odoo.com/documentation/17.0/es/_images/manually-availability-tooltip.png)

Una vez que haya confirmado la orden de venta vaya a Inventario y busque la tarjeta Órdenes de entrega en la página Información general de Inventario.

La tarjeta órdenes de entrega muestra el estado actual de las órdenes , incluyendo aquellas que están en el estado En espera. Las órdenes con este estado indican que los productos en esas órdenes no se han reservado todavía o todavía no están en existencia.

![Hoja de ruta de órdenes de entrega con órdenes de estado de espera.](https://www.odoo.com/documentation/17.0/es/_images/manually-delivery-orders-card.png)

Para ver la [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/manually.html#id5) previamente creada, haga clic en el botón (#) En espera en la tarjeta (en este caso , `8 en espera`).

Ubique la orden de entrega vinculada a la [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/manually.html#id7) que se creó previamente y haga clic en la línea para verla.

En el formulario de la orden de entrega, el estado en el campo Disponibilidad del producto se muestra como `Disponible` en texto amarillo en lugar de verde. Esto es porque hay suficientes existencias a la mano para esta orden, pero todavía no se ha reservado nada.

En la pestaña Operaciones, en la línea Producto los números en la columna Demanda y la columna Cantidad no coinciden.

En este caso, la columna Demanda muestra `10.00`, mientras que la columna Cantidad muestra `0`.

![El formulario de la orden de entrega con la disponibilidad de producto y cantidad reservada.](https://www.odoo.com/documentation/17.0/es/_images/manually-delivery-order-form.png)

Para reservar manualmente la cantidad especificada del producto para esta orden, haga clic en el botón Comprobar disponibilidad en la parte superior del formulario. Al hacerlo, el estado `Disponible` del campo Disponibilidad del producto se vuelve verde y cambia el número de la columna Cantidad para que coincida con la columna Demanda.

Esto se debe a que hay cantidad suficiente de existencias para reservar para la orden.

Una vez que esté listo, haga clic en Validar.

 Truco

Puede reservar varias órdenes con el estado _En espera_ al mismo tiempo y se pueden configurar al estado _Listo_.

Para hacerlo, abra la aplicación Inventario, la cual muestra la página Resumen de inventario. También puede acceder a la página Resumen de inventario en la aplicación Inventario ‣ Resumen.

Desde la página Resumen de inventario haga clic en el botón (#) En espera en la tarjeta de la Orden de entrega.

Después, marque todas las casillas de verificación a la izquierda de cada orden deseada, o marque la casilla de verificación en la hilera de encabezado para seleccionar todas las órdenes de una página al mismo tiempo.

Después, haga clic en el botón Comprobar disponibilidad en la parte superior de la página.

Si los productos incluidos en cada orden seleccionada tienen suficientes existencias disponibles, se reservan los productos y la orden pasa al estado Listo. Al recibir el estado Listo, el pedido desaparece de la lista En espera.

SI _no_ hay suficiente cantidad de existencias a la mano, la orden mantiene su estado actual y se queda en la lista.

![Lista de órdenes en el estado en espera y el botón de revisar disponibilidad.](https://www.odoo.com/documentation/17.0/es/_images/manually-check-availability.png)

 Ver también

- [En la confirmación de la reserva](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/at_confirmation.html)
    
- [Antes de la fecha programada](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/before_scheduled_date.html)