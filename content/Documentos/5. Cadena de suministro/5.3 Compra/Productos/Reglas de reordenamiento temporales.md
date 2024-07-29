Varios negocios necesitan que siempre haya una cantidad minima de existencias disponibles para algunos productos en cualquier momento. En Odoo, las empresas pueden crear _reglas de reordenamiento_ para evitar que las existencias se encuentren por debajo de las necesarias y automatizar las órdenes de compras para productos en específico.

Las reglas de reordenamiento mantienen los niveles de existencias previstos por arriba de cierto umbral sin necesidad de exceder el límite establecido o la cantidad máxima deseada. Odoo genera una orden con la _ruta_ seleccionada (por ejemplo, _comprar_ o _fabricar_) para reabastecer las existencias cuando un producto con reglas de reordenamiento se encuentra por debajo de la cantidad establecida.

En algunos casos, los negocios podrían preferir usar _reglas de reordenamiento temporales_ cuando no desean reabastecer de forma automática algunos productos en específico.

En Odoo, se crea una regla de reordenamiento «temporal» en el tablero de reabastecimiento cuando un producto:

1. Está configurado con la ruta _Comprar_.
    
2. No tiene ninguna regla de reordenamiento configurada.
    
3. Tiene la cantidad `0` en sus existencias.
    
4. Está incluido en una orden de venta.
    

Esta regla se elimina después de confirmar la orden de compra que se generó para el producto.

 Ver también

- [Reglas de reabastecimiento](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html)
    
- [Configurar reglas de reordenamiento](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/products/reordering.html)
    

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/products/temporary_reordering.html#configuration "Enlazar permanentemente con este título")

Para configurar que un producto active reglas de reordenamiento temporales en cuanto sus existencias lleguen a `0`, primero vaya a Inventario ‣ Productos ‣ Productos y haga clic en Nuevo.

 Nota

También puede configurarlas en un producto que ya existe, solo vaya a Inventario ‣ Productos ‣ Productos y seleccione uno.

En el formulario de producto, escriba el nombre del producto y asegúrese de que las opciones Se puede vender y Se puede comprar que están ubicadas debajo del campo Nombre del producto estén seleccionadas.

Después, en la pestaña Información general, seleccione `Producto almacenable` como Tipo de producto.

A continuación, vaya a la pestaña Compra y en la sección Proveedor haga clic en Agregar una línea para seleccionar uno del menú desplegable. Después, establezca un precio de compra en el campo Precio.

 Importante

**Debe** haber un proveedor establecido para que las reglas de reordenamiento temporales funcionen. Si bien es posible crear una orden de compra de forma automática, cuando intente reabastecer el producto desde el tablero Reabastecimiento en la aplicación _Inventario_ aparecerá una advertencia que le solicitará que agregue un proveedor al formulario del producto.

![Ventana emergente de advertencia que aparece después de hacer clic en reabastecer producto cuando no hay un proveedor establecido.](https://www.odoo.com/documentation/17.0/es/_images/temporary-reordering-warning-popup.png)

Antes de crear una orden de venta para el producto, asegúrese de que en el botón inteligente Disponible de su formulario aparezca `0.00 Unidades`. Después, verifique que el botón inteligente Reglas de reordenamiento diga `0`, lo que indica que no hay ninguna regla aplicada a ese producto.

![Botones inteligentes en el formulario del producto, corresponden a Disponible y Reglas de reordenamiento.](https://www.odoo.com/documentation/17.0/es/_images/temporary-reordering-smart-buttons.png)

## Activar una regla de reordenamiento temporal[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/products/temporary_reordering.html#trigger-temporary-reordering-rule "Enlazar permanentemente con este título")

Para activar una regla de reordenamiento temporal, cree una orden de venta para un producto desde la aplicación Ventas ‣ Nuevo.

Después, agregue un cliente en el campo correspondiente. Vaya a la pestaña Líneas de la orden, haga clic en Agregar un producto en la columna Producto y seleccione uno en el menú desplegable. Por último, confirme la orden de venta.

![Orden de venta para un producto que no tiene reglas de reordenamiento configuradas.](https://www.odoo.com/documentation/17.0/es/_images/temporary-reordering-sales-order.png)

## Verificar el reporte de reabastecimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/products/temporary_reordering.html#check-replenishment-report "Enlazar permanentemente con este título")

Para visualizar la regla de reordenamiento temporal que se creó para el producto sin existencias incluido en la orden de venta, vaya a Inventario ‣ Operaciones ‣ Reabastecimiento. Esta acción abre el tablero Reabastecimiento.

Busque el producto para el que creó la regla de reabastecimiento temporal en este tablero. En la línea del producto podrá visualizar la cantidad disponible, la cantidad pronosticada negativa, la ruta _Comprar_ y la cantidad por ordenar para reabastecer.

Además, en el extremo derecho de la fila hay dos opciones de reabastecimiento: Ordenar una vez y Automatizar.

![El reporte de reabastecimiento con reglas de reordenamiento temporales y otras opciones.](https://www.odoo.com/documentation/17.0/es/_images/temporary-reordering-replenishment-dashboard.png)

Haga clic en Ordenar una vez para usar la regla de reordenamiento temporal una sola vez. Esta acción hace que aparezca una ventana emergente en la esquina superior derecha con el mensaje Se generó la siguiente orden de reabastecimiento y el número de la nueva orden de compra.

 Truco

Después de que hizo clic en Ordenar una vez y se generó la orden de compra, actualice la página. Ka regla de reordenamiento temporal del producto ya no aparecerá en el tablero Reabastecimiento.

## Completar una orden de compra[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/products/temporary_reordering.html#complete-purchase-order "Enlazar permanentemente con este título")

Vaya a la aplicación Compra para visualizar la orden de compra que se creó desde el tablero Reabastecimiento. Seleccione la orden de compra generada desde la vista general de solicitudes de cotización.

Una vez allí, haga clic en Confirmar orden y después en Recibir productos. Por último, haga clic en Validar para completar la orden de compra.

![Orden de compra para un producto ordenado mediante una regla de reordenamiento temporal.](https://www.odoo.com/documentation/17.0/es/_images/temporary-reordering-purchase-order.png)

Ahora podrá entregar y facturar la orden de venta original.

 Nota

Asegúrese de que no haya reglas de reordenamiento en el formulario del producto después de que haya entregado y facturado la orden de venta.

Vaya a Inventario ‣ Productos ‣ Productos, seleccione el producto y verifique que la cantidad en el botón inteligente Reglas de reordenamiento es `0`.