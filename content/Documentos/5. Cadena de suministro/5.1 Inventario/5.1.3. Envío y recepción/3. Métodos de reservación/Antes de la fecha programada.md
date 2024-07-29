El método de reservación _antes de la fecha programada_ permite que los usuarios seleccionen un número específico de días para que sean el número máximo de días **antes** de una fecha de entrega programada cuando los productos incluidos en la orden de venta deben de reservarse.

 Ver también

[Métodos de reservación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods.html)

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/before_scheduled_date.html#configuration "Enlazar permanentemente con este título")

Para configurar el método de reservación a _antes de la fecha programada_ navegue a la aplicación Inventario ‣ Configuración ‣ Tipos de operaciones. Después, seleccione el Tipo de operación que quiere configurar, o cree uno nuevo haciendo clic en Nuevo.

En la pestaña General localice el campo Método de reserva y seleccione antes de la fecha programada.

![El campo de método de reserva en el formulario de tipo de operación orden de envío.](https://www.odoo.com/documentation/17.0/es/_images/before-scheduled-date-configuration.png)

 Nota

Cuando el Tipo de operación se cambia a Recepción en un formulario de Tipos de operación, los métodos de reservación **no** están disponibles.

Una vez que lo seleccione, aparecerá un nuevo campo abajo, Reservar antes de la fecha programada. En este campo puede cambiar el número de días antes y días antes de que se destacó de el número predeterminado, `0`, al que usted prefiera.

Si cambia el valor días antes también cambiará el número máximo de días antes de la fecha programada en los que se debe reservar productos.

Si cambia el valor días antes de que se destacó también cambiará el número máximo de días antes de la fecha programada en los que se debe reservar productos si las transferencias se marcan como favoritas.

 Example

Aquí el valor días antes se configura como `2` días antes y el valor días antes de que se destacó se configura como `3`.

Esto significa que los productos se reservan dos días antes de la fecha de entrega prevista para los pedidos normales, y tres días antes de la fecha de entrega prevista para las transferencias con estrella (favoritas).

![Campo reservar antes de la fecha programada con valores numéricos configurados.](https://www.odoo.com/documentation/17.0/es/_images/before-scheduled-date-days-before.png)

Esta es la configuración que se aplica para el flujo de trabajo que se encuentra a continuación.

### Editar formulario del producto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/before_scheduled_date.html#edit-product-form "Enlazar permanentemente con este título")

Antes de que pueda usar el método de reservación _antes de la fecha programada_ asegúrese de que se agregó un _tiempo de espera del cliente_ a los productos que planea vender con ese método.

Para hacerlo, vaya a la aplicación Inventario ‣ Productos ‣ Productos y seleccione el producto que quiere configurar.

En el formulario del producto haga clic en la pestaña Inventario y, en la sección Logística, cambie el valor en el campo Tiempo de espera del cliente.

Para este flujo de trabajo de ejemplo, cámbielo a `5` días.

Esto programa la fecha de entrega de un producto específico a cinco días después de la fecha de creación de la orden de venta.

![Formulario del producto con el tiempo de espera del cliente configurado en la pestaña Inventario](https://www.odoo.com/documentation/17.0/es/_images/before-scheduled-date-customer-lead-time.png)

## Flujo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/before_scheduled_date.html#workflow "Enlazar permanentemente con este título")

Para ver cómo funciona el método de reservación _antes de la fecha programada_ cree una [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/before_scheduled_date.html#id1) nueva desde la aplicación de Ventas ‣ Nuevo.

Agregue un client en el campo Cliente. Luego, en la pestaña Líneas de la orden haga clic en Agregar un producto y seleccione un producto desde el menú desplegable que tiene un _tiempo de espera del cliente_ programado, para agregar un formulario de cotización.

Finalmente, en la columna Cantidad ajuste la cantidad que quiere vender de un producto.

Para este flujo de trabajo de ejemplo, configure la Cantidad a `10`.

Cuando esté listo, confirme la orden de venta.

Haga clic en el icono verde 📈 (gráfico) que se encuntra en la línea del producto para mostrar la información sobre la Disponibilidad. Esta herramienta muestra el número de unidades reservadas para esta orden. Ya que el método de reservación es _antes de la fecha programada_, la cantidad Reservada será `0 Unidades`.

Sin embargo, debajo de esa cantidad se leerá `Existencias disponibles`. Esto se debe a que la cantidad está disponible, pero la fecha programada para este flujo de trabajo de ejemplo es 5 días después de la fecha de la orden.

Como la reserva no es sino hasta dos días antes de la fecha programada los productos no se reservarán antes de ese momento.

 Nota

Si **no** hay suficiente cantidad de existencias de un producto que aparece en una [|orden de ventas|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/before_scheduled_date.html#id3), el icono de 📈 (gráfico) aparecerá rojo en lugar de verde.

En lugar de mostrar el número reservado de unidades para una orden, la disponibilidad se lee como Reservado y muestra el número de unidades disponibles (por ejemplo, `0 unidades`).

Además, a no ser de que haya un reabastecimiento o una recepción programada, también leerá No hay disponibilidad futura, en texto rojo.

![Orden de venta confirmada con la disponibilidad seleccionada.](https://www.odoo.com/documentation/17.0/es/_images/before-scheduled-date-availability-tooltip.png)

Haga clic en el botón inteligente Reserva para ver el formulario de la orden de reserva.

En el formulario de la orden de entrega, el estado en el campo Disponibilidad del producto se muestra como `Disponible` en texto amarillo en lugar de verde. Esto es porque hay suficientes existencias a la mano para esta orden, pero todavía no se ha reservado nada.

Note que el campo Fecha programada, arriba del campo Disponibilidad del producto muestra la fecha cinco días a partir de la orden de creación. Esto indica que los productos no se reservarán hasta tres días después de la fecha de hoy (dos días antes de la fecha de entrega programada).

![El formulario de la orden de entrega con la disponibilidad de producto y cantidad reservada.](https://www.odoo.com/documentation/17.0/es/_images/before-scheduled-date-delivery-order-form.png)

En la pestaña Operaciones en la línea de producto los números en la columna Demanda y la columna Cantidad no ocinciden (en este caso, la columna Demanda muestra `10.00` y la columna Cantidad enlista `0`.).

La columna Cantidad muestra `0` porque los productos no se reservan sino hasta dos días _antes_ de la fecha de entrega. Odoo reserva de forma automática los productos una vez que la fecha programada llega, que es cuando las columnas Demanda y Cantidad coincidirán.

 Truco

Si los productos en la [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/before_scheduled_date.html#id5) se deben reservar _antes_ de la fecha programada de reservación, puede hacerlo de forma manual. Para reservar productos de forma manual antes de lo programado, haga clic en Revisar disponibilidad en la parte superior del formualrio

Esto hace que el estado sea `Disponible` en el campo verde Disponibilidad del producto y cambia el número en la columna Cantidad para que coincida con la columna Demanda.

Una vez que esté listo, haga clic en Validar.

 Ver también

- [Reservación manual](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/manually.html)
    
- [En la confirmación de la reserva](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/at_confirmation.html)