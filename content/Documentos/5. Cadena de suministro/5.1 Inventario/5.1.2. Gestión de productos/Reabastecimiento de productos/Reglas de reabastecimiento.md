Las _reglas de reordenamiento_ se utilizan para mantener los niveles de existencias previstos sin sobrepasar un límite especificado. Esto se consigue especificando una cantidad mínima por debajo de la cual no deben descender las existencias y una cantidad máxima que no deben superar.

Puede configurar las reglas de reordenamiento para cada producto en función de la ruta utilizada para reabastecerlo. Si un producto utiliza la ruta _Comprar_, se crea una cotización cuando se activa la regla de reordenamiento. Si un producto utiliza la ruta _Fabricación_, se crea una orden de fabricación. Esto es así independientemente de la ruta de reabastecimiento seleccionada.

 Ver también

- [Tutoriales de Odoo: Reglas de reordenamiento automáticas](https://www.youtube.com/watch?v=XEJZrCjoXaU)
    
- [Tutoriales de Odoo: Reglas de reordenamiento manuales](https://www.youtube.com/watch?v=deIREJ1FFj4)
    

## Configurar productos con reglas de reabastecimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#configure-products-for-reordering-rules "Enlazar permanentemente con este título")

Para poder utilizar las reglas de reordenamiento de un producto, primero debe configurarlo de forma adecuada. Para ello, vaya a Inventario ‣ Productos ‣ Productos, seleccione un producto existente o haga clic en Nuevo para crear uno.

En el formulario del producto, en la pestaña Información general, asegúrese de que el Tipo de producto esté configurado como Producto almacenable. Esto es necesario porque Odoo solo realiza seguimiento de las cantidades en existencia para productos almacenables y este número se utiliza para activar las reglas de reordenamiento.

![Establezca el tipo de producto como almacenable.](https://www.odoo.com/documentation/17.0/es/_images/product-type.png)

A continuación, haga clic en la pestaña Inventario y seleccione una o más rutas de la sección Rutas. Esto le indica a Odoo que ruta usar para reabastecer el producto.

![Seleccione una o más rutas en la pestaña Inventario.](https://www.odoo.com/documentation/17.0/es/_images/select-routes1.png)

Si el producto se reordena utilizando la ruta Comprar, confirme que la casilla Se puede comprar está activada bajo el nombre del producto. Esto hace que aparezca la pestaña Comprar, haga clic en ella, especifique al menos un proveedor y el precio al que venden el producto. De este modo Odoo sabrá a cuál empresa debe comprar el producto.

![Especifique un proveedor y el precio en la pestaña Compra.](https://www.odoo.com/documentation/17.0/es/_images/specify-vendor1.png)

Si se reabastece el producto usando la ruta Fabricación, necesita tener al menos una lista de materiales (LdM) asociada. Esto es necesario porque Odoo solo crea órdenes de fabricación para productos con una LdM.

Si aún no existe una LdM para el producto, haga clic en el botón inteligente Lista de materiales ubicado en la parte superior del formulario del producto. Después, haga clic en Nuevo para configurar una nueva lista de materiales.

![El botón inteligente de lista de materiales en un formulario de producto.](https://www.odoo.com/documentation/17.0/es/_images/bom-smart-button.png)

## Crear nuevas reglas de reordenamiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#create-new-reordering-rules "Enlazar permanentemente con este título")

Vaya a Inventario ‣ Configuración ‣ Reglas de reordenamiento para crear una nueva regla de reordenamiento. Haga clic en Nuevo y complete la nueva línea de la siguiente manera:

- Producto: el producto que se reabastece mediante la regla.
    
- Ubicación: la ubicación donde se almacena el producto.
    
- Cantidad mínima: La cantidad mínima que se puede pronosticar sin que se active la regla. Cuando las existencias pronosticadas son inferiores a esta cantidad, se creará una orden de reabastecimiento para el producto.
    
- Cantidad máxima: la cantidad máxima hasta la que se reponen las existencias.
    
- Cantidad múltiple: especifique si el producto se debe reabastecer por lotes con una cantidad determinada. Por ejemplo, reabastecer un producto en lotes de 20.
    
- UdM: la unidad de medida que se utiliza para reordenar el producto. Este valor puede ser `unidades` o una unidad de medida específica para peso, longitud, etc.
    

![El formulario para crear una nueva regla de reabastecimiento.](https://www.odoo.com/documentation/17.0/es/_images/reordering-rule-form.png)

 Truco

También es posible crear reglas de reordenamiento desde el formulario de cada producto. Para ello, vaya a Inventario ‣ Productos ‣ Productos y seleccione uno. Haga clic en el botón inteligente Reglas de reordenamiento y luego haga clic en Nuevo para completar la nueva línea justo como se describió con anterioridad.

Obtenga más información sobre los siguientes campos de reglas de reordenamiento para hacer uso avanzado de ellas:

- [Activadores](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#inventory-product-management-trigger)
    
- [Días de visibilidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#inventory-product-management-visibility-days)
    
- [Ruta](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#inventory-product-management-route)
    

### Regla de reabastecimiento 0/0/1[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#reordering-rule "Enlazar permanentemente con este título")

La regla de reabastecimiento _0/0/1_ es una regla de especialidad que se usa para reabastecer un producto que no se mantiene a la mano cada vez que una orden de venta se confirma para el mismo producto.

 Importante

La regla de reabastecimiento 0/0/1 es similar a la ruta _Reabastecer sobre pedido (MTO)_, ya que ambos flujos se usan para reabastecer un pedido hasta que se confirme una [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#id1).

La principal diferencia entre los dos métodos es que la ruta _Reabastecer sobre pedido_ reserva automáticamente el producto para la [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#id3) que provocó su reabastecimiento. Esto significa que el producto no se puede utilizar para otra [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#id5).

La regla de reabastecimiento 0/0/1 no tiene esta limitación. Un producto reabastecido utilizando la regla no está reservado para ninguna [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#id7) específica, y puede utilizarse según sea necesario.

Otra diferencia importante es que las órdenes de reabastecimiento creadas por la ruta _Reabastecer sobre pedido_ están vinculadas a la orden original de venta mediante un botón inteligente ubicado en la parte superior de la orden. Al utilizar la regla de reordenamiento 0/0/1 se crea una orden de reposición que no está vinculada a la orden original.

Vea la documentación [Reabastecer sobre pedido (MTO)](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/mto.html)  para un resumen completo de la ruta MTO.

Para crear una regla de reabastecimiento 0/0/1 vaya a Inventario ‣ Productos ‣ Productos y seleccione un producto.

En la parte superior de la página productos, haga clic en el botón inteligente  Reglas de reabastecimiento para abrir la página Reglas de reabastecimiento del producto. En la página resultante, haga clic en Nuevo para empiezar a configurar una orden de reabastecimiento.

En el campo Ubicación de la nueva regla de reabastecimiento, seleccione la ubicación en la que deben almacenarse los productos reabastecidos. Por defecto, esta ubicación se establece en WH/Stock.

En el campo Ruta, seleccione la ruta que debe utilizar la regla para reponer el artículo. Por ejemplo, si el producto debe comprarse a un proveedor, seleccione la ruta Comprar.

En los campos Cantidad mínima y Cantidad máxima, deje los valores en `0.00`. En el campo Por ordenar, introduzca el valor `1.00`.

![Una regla de reabastecimiento 0/0/1](https://www.odoo.com/documentation/17.0/es/_images/001-rule.png)

Una vez que haya configurado la regla de reabastecimiento con estos valores, cada vez que una [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#id9) cause que la cantidad pronosticada del producto sea menor a la Cantidad mínima de `0.00`, la Ruta seleccionada se usa para reabastecer una unidad por una, hasta regresar a la Cantidad máxima de `0.00`.

 Example

Los portarretratos están configurados con la regla de reordenamiento 0/0/1 que utiliza la ruta _Compra_, es decir, no se conserva ninguna unidad de este producto en ningún momento.

Al confirmar una orden de venta para un portarretratos hace que la cantidad pronosticada disminuya a `-1.00`. Esto activa la regla de reordenamiento que crea una orden de compra en automático para una unidad de este producto.

Luego de recibir el producto del proveedor, la cantidad pronosticada del portarretratos vuelve a `0.00`. Ahora hay uno disponible, pero no está reservado para la orden de venta que ocasionó su compra y puede usarse para cumplir con esa orden de venta o reservarse para otra.

## Activador[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#trigger "Enlazar permanentemente con este título")

Cuando las existencias se encuentren por debajo del mínimo de la regla de reordenamiento, establezca el campo _Activar_ de la regla de reordenamiento en _automático_ para crear órdenes de compra o fabricación de forma automática y reabastecer las existencias.

Como alternativa, al establecer el _activador_ de la regla de reordenamiento en _manual_, aparecerá el producto y las existencias previstas en el _tablero de reabastecimiento_. Allí, el gerente de aprovisionamiento puede revisar los niveles de existencia, los plazos de espera y las fechas previstas de llegada.

 Ver también

[Elegir una estrategia de reabastecimiento](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/strategies.html)

 Truco

Vaya a Inventario ‣ Operaciones ‣ Reabastecimiento para acceder al tablero de reabastecimiento.

Para habilitar el campo Activar, vaya a Inventario ‣ Configuración ‣ Reglas de reordenamiento. Después, haga clic en el icono (deslizador) que está ubicado en la parte derecha de los títulos de las columnas y habilite la opción Activar desde el menú desplegable de opciones adicionales que aparece.

![Habilitar el campo Activar al seleccionarlo en el menú de opciones adicionales.](https://www.odoo.com/documentation/17.0/es/_images/enable-trigger.png)

En la columna Activar, seleccione Auto o Manual. Consulte las secciones que se encuentran a continuación para obtener más información sobre los distintos tipos de reglas de reordenamiento.

### Auto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#auto "Enlazar permanentemente con este título")

Las reglas de reordenamiento automáticas, que se configuran al establecer el campo Activar de la regla de reordenamiento en Auto, generan órdenes de compra o fabricación cuando:

1. el planificador se ejecuta y la cantidad _disponible_ se encuentra por debajo del mínimo.
    
2. una orden de venta se confirma y reduce la cantidad _prevista_ del producto por debajo del mínimo.
    

 Truco

De forma predeterminada, el planificador está configurado para ejecutarse una vez al día.

Asegúrese de haber habilitado el [modo de desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode) para activar una regla de reordenamiento de forma manual antes de que se ejecute el planificador. Vaya a Inventario ‣ Operaciones ‣ Ejecutar planificador, allí aparecerá una ventana emergente, haga clic en el botón morado Ejecutar planificador.

Tenga en cuenta que esto también activará otras acciones programadas.

 Example

El producto `Lámpara de oficina` tiene una regla de reordenamiento automática que está configurada para activarse cuando la cantidad pronosticada se encuentra por debajo del mínimo de `5.00`. Como el pronóstico actual es `55.00`, entonces la regla de reordenamiento **no** se activa.

![La regla de reordenamiento automático en la página Reglas de reordenamiento.](https://www.odoo.com/documentation/17.0/es/_images/auto.png)

Si selecciona la ruta Comprar, entonces se genera una solicitud de cotización. Para ver y gestionar las solicitudes de cotización, vaya a Compra ‣ Órdenes ‣ Solicitudes de cotización.

Si selecciona la ruta Fabricación, entonces se genera una orden de fabricación. Para ver y gestionar las órdenes de fabricación, vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación.

Cuando no hay ninguna ruta seleccionada, Odoo elige la Ruta especificada en la pestaña Inventario del formulario del producto.

### Manual[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#manual "Enlazar permanentemente con este título")

Las reglas de reordenamiento manuales, que se configuran al establecer el campo Activar de la regla de reordenamiento en Manual, muestran un producto en el tablero de reabastecimiento cuando la cantidad pronosticada se encuentra por debajo del mínimo especificado. Los productos en este tablero se llaman _necesidades_, pues son necesarios para cumplir con las próximas órdenes de venta, pero la cantidad pronosticada no es suficiente.

El tablero de reabastecimiento, al que puede acceder desde Inventario ‣ Operaciones ‣ Reabastecimiento, toma en cuenta los plazos de las órdenes de venta, los niveles de existencias pronosticadas y los plazos de espera del proveedor. Muestra las necesidades **solo** cuando es momento de volver a ordenar los artículos.

 Nota

En caso de que la ventana de un día para ordenar productos sea demasiado corta, vaya a la sección de [días de visibilidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#inventory-product-management-visibility-days) para hacer que la necesidad aparezca en el tablero de reabastecimiento con un número específico de días por adelantado.

Cuando un producto aparece en el tablero de reabastecimiento, y hace clic en el botón Ordenar una vez, generará la orden de compra o de fabricación con las cantidades especificadas Para ordenar.

![Hacer clic en el botón Ordenar una vez en el tablero de reabastecimiento para reabastecer las existencias.](https://www.odoo.com/documentation/17.0/es/_images/manual.png)

## Días de visibilidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#visibility-days "Enlazar permanentemente con este título")

 Importante

Asegúrese de comprender los [plazos de espera](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/scheduled_dates.html) antes de continuar con esta sección.

Al asignar [reglas de reordenamiento manuales](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#inventory-product-management-manual-rr) a un producto, los _días de visibilidad_ hacen que el producto aparezca en el tablero de reabastecimiento (Inventario ‣ Operaciones ‣ Reabastecimiento) con un cierto número de días por adelantado.

 Example

Un producto tiene una regla de reordenamiento manual configurada para que se active cuando el nivel de existencias se encuentre por debajo de cuatro unidades. La cantidad actual disponible es de diez unidades.

La fecha actual es 20 de febrero y la _fecha de entrega_ de la orden de venta (en la pestaña Otra información) es el 3 de marzo, es decir, doce días a partir de la fecha actual.

El [plazo de entrega del proveedor](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/scheduled_dates.html#inventory-shipping-receiving-purchase-lt) es de cuatro días y el [plazo de entrega seguro para la compra](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/scheduled_dates.html#inventory-shipping-receiving-purchase-security-lt) es de un día.

Cuando el campo Días de visibilidad de la regla de reordenamiento está configurado en cero, el producto aparece en el tablero de reabastecimiento cinco días antes de la fecha de entrega, que en este caso corresponde al 27 de febrero.

![Gráfico de representación de la necesidad y cuándo aparece en el tablero de reabastecimiento: 27 de febrero.](https://www.odoo.com/documentation/17.0/es/_images/need-dates.png)

Para visualizar el producto en el tablero de reabastecimiento en la fecha actual, 20 de febrero, establezca los Días de visibilidad en `7.00`.

Para determinar la cantidad de días de visibilidad necesarios para visualizar un producto en el tablero de reabastecimiento deberá restar la _fecha de hoy_ de la _fecha en la que aparece la necesidad_ en el tablero correspondiente.

íDías de visibilidad=Fecha en que aparece la necesidad−Fecha actual

 Example

Continuando con el ejemplo anterior, la fecha de hoy es el 20 de febrero y la necesidad del producto aparece el 27 de febrero.

(27 de febrero - 20 de febrero = 7 días)

Configurar los días de visibilidad de forma incorrecta en menos de siete días en este caso ocasiona que la necesidad **no** aparezca en el tablero de reabastecimiento.

![Visualización del tablero de reabastecimiento con los días de visibilidad correctos e incorrectos en su configuración.](https://www.odoo.com/documentation/17.0/es/_images/visibility-days.png)

## Ruta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html#route "Enlazar permanentemente con este título")

Odoo permite seleccionar varias rutas en la pestaña Inventario en cada formulario de producto. Por ejemplo, es posible seleccionar tanto Comprar como Fabricar, para permitir la funcionalidad de ambas rutas.

Odoo también permite que los usuarios establezcan una ruta preferida como regla de reordenamiento de un producto. Esta es la ruta predeterminada de la regla en caso de que hayan varias seleccionadas. Para seleccionar una ruta preferida, vaya a Inventario ‣ Configuración ‣ Reglas de reordenamiento.

La columna Ruta está oculta de forma predeterminada en la página Reglas de reordenamiento.

Para abrir la columna Ruta, seleccione el icono (deslizador) ubicado en la parte derecha de los títulos de las columnas y seleccione la opción Ruta en el menú desplegable que aparece.

Haga clic dentro de la columna en la fila de una regla de reordenamiento, aparecerá un menú desplegable con todas las rutas disponibles para esa regla. Seleccione una para establecerla como ruta preferida.

![Establecer una ruta preferida desde el menú desplegable](https://www.odoo.com/documentation/17.0/es/_images/select-preferred-route.png)

 Importante

Si se activan varias rutas para un producto pero no se establece ninguna ruta preferida para su regla de reordenamiento, el producto se reordena utilizando la ruta seleccionada que aparece en primer lugar en la pestaña Inventario del formulario del producto.