El método de reservación _en la confirmación_ reserva los productos **solo** cuando se confirma una orden de venta **y** si hay suficientes existencias de los productos incluidos en la [|orden de ventas|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/at_confirmation.html#id1) que ya están disponibles.

 Ver también

[Métodos de reservación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods.html)

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/at_confirmation.html#configuration "Enlazar permanentemente con este título")

Para configurar el método de reservación a _en la confirmación_ navegue a la aplicación Inventario ‣ Configuración ‣ Tipos de operaciones. Después, seleccione el Tipo de operación que quiere configurar, o cree uno nuevo haciendo clic en Nuevo.

En la pestaña General del formulario de tipo de operación, localice la opción Método de Reserva, y seleccione en la confirmación.

![El campo de método de reserva en el formulario de tipo de operación orden de envío.](https://www.odoo.com/documentation/17.0/es/_images/at-confirmation-operations-type.png)

## Flujo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/at_confirmation.html#workflow "Enlazar permanentemente con este título")

Para ver cómo funciona el método de reservación _en la confirmación_ cree una [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/at_confirmation.html#id3) nueva desde la aplicación de Ventas ‣ Nuevo.

Agregue un client en el campo Cliente. Luego, en la pestaña Líneas de la orden haga clic en Agregar un producto y desde el menú desplegable seleccione un producto que agregar a la cotización. Finalmente, en la columna Cantidad ajuste la cantidad que quiere vender del producto.

Cuando esté listo, confirme la orden de venta.

Haga clic en el icono 📈 (gráfico) que se encuentra en la línea de producto para mostrar la disponibilidad del producto, que muestra el número de unidades Reservadas para esta orden.

 Nota

Si **no** hay suficiente cantidad de existencias de un producto que aparece en una [|orden de ventas|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/at_confirmation.html#id5), el icono de 📈 (gráfico) aparecerá rojo en lugar de verde.

En lugar de mostrar el número reservado de unidades para una orden, la disponibilidad se lee como Disponible y muestra el número de unidades disponibles (por ejemplo, `0 unidades`).

![Orden de venta confirmada con la disponibilidad seleccionada.](https://www.odoo.com/documentation/17.0/es/_images/at-confirmation-availability-tooltip.png)

 Reporte pronosticado

Para ver todos los factores que afectan la reservación de productos, haga clic en el enlace interno Ver pronóstico en forma de flecha para ver el tablero Reporte pronosticado.

El Informe de previsión muestra información de previsión sobre el producto o productos incluidos en el pedido de venta; es decir, cualquier recepción en vivo del producto y cualquier pedido de venta activo, que se enumeran en la columna Usado por. Vea cómo se ha cumplido cada pedido en la columna Reabastecimiento.

Además, la cantidad pronosticada se calcula en la parte superior de la página. Para hacerlo se suman las cantidades a la mano y entrantes y se restará la cantidad saliente, como se muestra a continuación:

![La ecuación para obtener la cantidad pronosticada desde la página Reporte pronosticado.](https://www.odoo.com/documentation/17.0/es/_images/at-confirmation-forecasted-equation.png)

Si se le debe dar prioridad a una orden sobre la otra, haga clic en el botón Anular reserva en la línea de orden correspondiente en la columna Reabastecimiento.

Para entregar los productos, haga clic en el botón inteligente Entrega en la parte superior del formulario de la orden de venta. Para confirmar que la reserva funcionó como debía, asegúrese de que el campo Disponibilidad del producto sea `Disponible` (en texto verde) y que los números de las columnas Demanda y Cantidad coincidan (en este caso, ambos deberían ser `100.00`).

![La orden de entrega para el producto que se incluye en la orden de venta con una reserva "en la confirmación".](https://www.odoo.com/documentation/17.0/es/_images/at-confirmation-delivery-order.png)

Una vez que esté listo, haga clic en Validar.

 Ver también

- [Reservación manual](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/manually.html)
    
- [Antes de la fecha programada](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/before_scheduled_date.html)