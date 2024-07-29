En algunos casos es necesario desmantelar los productos fabricados para que vuelvan a ser piezas individuales, por ejemplo, si construyó demasiadas unidades de un producto o si debe recuperar los componentes de un producto para usarlos en la fabricación de otro.

En la aplicación _Fabricación_ de Odoo es posible desmantelar productos y volver a colocar sus componentes en el inventario a través de las _órdenes de desmontaje_. Al usar estas órdenes para llevar a cabo esta tarea, los conteos de inventario del producto terminado y sus componentes siguen siendo precisos según la cantidad de productos desmantelados y de componentes recuperados.

## Crear una orden de desmontaje[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/unbuild_orders.html#create-unbuild-order "Enlazar permanentemente con este título")

Vaya a Fabricación ‣ Operaciones ‣ Órdenes de desmontaje y haga clic en Nuevo para crear una.

Empiece a completar la nueva orden de desmontaje, seleccione el producto a desmantelar, después el campo Lista de materiales se completará en automático con la lista correspondiente. Si debe utilizar una lista diferente, haga clic en el campo Lista de materiales y selecciónela del menú desplegable.

Como alternativa, puede seleccionar una LdM específica en el campo Lista de materiales antes de seleccionar un producto, esto hace que el producto correspondiente aparezca en automático en el campo Producto.

Después, especifique la cantidad del producto a desmantelar en el campo correspondiente.

Si el producto a desmantelar se fabricó a través de una orden de fabricación específica, selecciónela en el campo Orden de fabricación.

Seleccione la ubicación de almacenamiento actual del producto a desmantelar en el campo Ubicación de origen.

Seleccione la ubicación de almacenamiento de los componentes recuperados luego de llevar a cabo la operación de desmantelamiento en el campo Ubicación de destino.

Si la función _Números de lote y de serie_ está habilitada en los ajustes de la aplicación _Inventario_, en la orden de desmontaje aparecerá el campo Número de serie/lote y este sirve para especificar el número de serie o lote del producto a desmantelar si tiene alguno asignado.

Si la base de datos de Odoo está configurada con varias empresas aparecerá el campo Empresa en la orden de desmontaje. Ahí podrá especificar la empresa propietaria del producto a desmantelar.

Por último, luego de que desmantele el producto, haga clic en el botón Desmontar ubicado en la parte superior de la orden para confirmarla.

![Una orden de desmontaje con información en todos los campos.](https://www.odoo.com/documentation/17.0/es/_images/unbuild-order.png)

 Advertencia

Es posible crear órdenes de desmontaje para productos que tienen un total de cero (o menos) unidades disponibles, pero no es recomendable porque podría ocasionar inconsistencias en el inventario.

Si crea una orden de desmontaje para un producto con cero (o menos) unidades disponibles, entonces aparece una ventana emergente que le advierte al usuario que no hay cantidad suficiente para desmantelar.

Para ignorar la advertencia y llevar a cabo la orden de desmontaje, haga clic en el botón Confirmar ubicado en la parte inferior de la ventana emergente. Haga clic en Descartar para volver a la orden.

![La ventana emergente de cantidad insuficiente que aparece después de tratar de confirmar una orden de desmontaje de un producto con cero o menos unidades a mano.](https://www.odoo.com/documentation/17.0/es/_images/insufficient-quantity.png)

Después de completar una orden de desmontaje, los conteos de inventario se actualizan de forma automática con la cantidad de productos desmantelados y de componentes recuperados.

 Example

El producto `Perchero` está constituido por un componente de `Poste de madera` y seis componentes de `Clavija de madera`.

Se crea un orden de desmontaje para una unidad de `Perchero`. Luego de completarla, la cantidad disponible del producto anterior disminuye por uno y las cantidades disponibles de `Poste de madera` y `Clavija de madera` aumentan por uno y seis, respectivamente.

## Desechar componentes no utilizables[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/unbuild_orders.html#scrap-unusable-components "Enlazar permanentemente con este título")

En algunos casos, es posible que los componentes queden inutilizables luego de completar el proceso de desmantelamiento. Para asegurarse de que los conteos de inventario reflejen la cantidad de componentes utilizables disponibles de forma precisa, debe eliminar cualquier componente que no lo sea con una [orden de desecho](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/scrap_inventory.html).