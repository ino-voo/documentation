La aplicación _Fabricación_ de Odoo permite que los usuarios fabriquen productos en uno, dos o tres pasos. Si utiliza la fabricación de un solo paso, Odoo crea una orden de fabricación, pero no genera traslados para el movimiento de componentes fuera del inventario o de productos terminados al inventario. Las cantidades en el inventario se actualizan según la cantidad de componentes utilizados y productos fabricados, pero no se realiza un seguimiento del traslado de estos hacia y desde el inventario.

 Truco

El número de pasos utilizados en la fabricación se establece a nivel de almacén, esto permite que cada almacén utilice un número diferente de pasos. Si desea cambiar el número de pasos utilizado para un almacén específico, vaya a Inventario ‣ Configuración ‣ Almacenes y seleccione un almacén de la pantalla Almacenes.

En la pestaña configuración del almacén, vaya al campo de entrada guilabel:`Fabricación` y seleccione una de las tres opciones: Fabricación (1 paso), Elegir componentes y luego fabricar (2 pasos), o Elegir componentes, fabricar y luego almacenar los productos (3 pasos).

![El campo de entrada Fabricación en una página de configuración de almacén.](https://www.odoo.com/documentation/17.0/es/_images/manufacturing-type.png)

 Importante

Debe configurar los productos correctamente antes de fabricarlos. Si desea obtener más información sobre cómo hacerlo, consulte la documentación sobre cómo [configurar un producto para la fabricación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/configure_manufacturing_product.html#manufacturing-management-configure-manufacturing-product).

## Crear una orden de fabricación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html#create-manufacturing-order "Enlazar permanentemente con este título")

Si desea fabricar un producto en la aplicación de Odoo _Fabricación_, vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación, y haga clic en Nuevo para crear una nueva [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html#id1).

Desde la nueva [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html#id3), seleccione el producto a fabricar del menú desplegable Producto. El campo lista de materiales se completa de forma automática con la lista de materiales asociada.

Si tiene un producto con más de una [|lista de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html#id5) configurada, puede seleccionar la [|lista de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html#id7) específica en el campo lista de materiales, y el campo producto se completa automáticamente con el producto asociado.

Después de haber seleccionado una [|lista de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html#id9), las pestañas componentes y órdenes de trabajo se completan de forma automática con los componentes y operaciones especificados en la [|lista de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html#id11). Si necesita agregar componentes u operaciones a la [|lista de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html#id13) que esté configurando, hágalo en las pestañas componentes y órdenes de trabajo mediante el botón agregar una línea.

Por último, confirme la lista de materiales.

## Proceso de orden de fabricación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html#process-manufacturing-order "Enlazar permanentemente con este título")

Una orden de fabricación se procesa al completar todas las órdenes de trabajo enumeradas en la pestaña órdenes de trabajo. Esto se puede hacer desde la orden de fabricación o desde la vista de la tableta de órdenes de trabajo.

### Flujo básico[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html#basic-workflow "Enlazar permanentemente con este título")

Si desea completar las órdenes de trabajo desde la orden de fabricación vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y seleccione una orden de fabricación.

En la página de orden de fabricación, seleccione la pestaña órdenes de trabajo. Una vez que comience el trabajo en la primera orden de trabajo que debe completarse, haga clic en el botón iniciar para esa orden de trabajo. La aplicación _Fabricación_ iniciará un temporizador que registra cuánto tiempo lleva completar la orden de trabajo.

![El botón de inicio en una operación de una orden de fabricación.](https://www.odoo.com/documentation/17.0/es/_images/start-button.png)

Cuando se complete la orden de trabajo, haga clic en el botón Hecho para esa orden de trabajo. Repita el mismo proceso para cada orden de trabajo enumerada en la pestaña órdenes de trabajo.

![El botón "Hecho" en una operación de una orden de fabricación.](https://www.odoo.com/documentation/17.0/es/_images/done-button.png)

Una vez que completó todas las órdenes de trabajo, haga clic en producir todo en la parte superior de la pantalla para marcar la orden de fabricación como hecha y registrar los producto fabricado en inventario.

### Flujo de trabajo de Taller[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html#shop-floor-workflow "Enlazar permanentemente con este título")

Para completar las órdenes de trabajo de una orden de fabricación con el módulo _Taller_, primero vaya a Fabricación ‣ Operaciones ‣ Ordenes de fabricación y después seleccione una orden de fabricación.

En la orden de fabricación, seleccione la pestaña Órdenes de trabajo y luego presione el botón ↗️ (cuadro con una flecha apuntando hacia arriba) ubicado en la línea de la primera orden de trabajo a procesar. Aparecerá la ventana emergente Órdenes de trabajo con detalles y distintas opciones de procesamiento para esa orden de trabajo.

En la ventana emergente, deberá presionar el botón Abrir Taller ubicado en la parte superior derecha de la ventana para abrir _Taller_.

![El botón Abrir taller para una orden de trabajo en una orden de fabricación.](https://www.odoo.com/documentation/17.0/es/_images/shop-floor-button.png)

Cuando accede desde una orden de trabajo específica dentro de una orden de fabricación, _Taller_ se abre de forma predeterminada en la página del centro de trabajo en donde la orden de trabajo está configurada para llevarse a cabo. La página muestra una tarjeta para la orden de trabajo que muestra el número de la orden de fabricación, el producto y el número de unidades a producir, así como los pasos necesarios para completar la orden de trabajo.

![La tarjeta de una orden de trabajo en la página de un centro de trabajo en el módulo Taller.](https://www.odoo.com/documentation/17.0/es/_images/work-order-card.png)

Una orden de trabajo se procesa al completar los pasos que aparecen en su respectiva tarjeta. Puede hacer esto si hace clic en un paso y sigue las instrucciones que aparecen en la ventana emergente. Una vez que completa un paso, haga clic en Siguiente para poder continuar con los siguientes pasos en caso de que sea necesario.

Como alternativa, también puede completar los pasos de la orden de trabajo si selecciona la casilla que aparece del lado derecho de la línea del paso que se encuentra en la tarjeta de la orden. El paso se marca como completado de forma automática con este método y no aparece ninguna ventana emergente.

El último paso en una tarjeta de orden de trabajo se titula _Registrar producción_. Este paso se utiliza para registrar el número de unidades de producto elaboradas. Si este número es igual al número para el que se creó la orden de fabricación, haga clic en el botón Número de unidades ubicado del lado derecho de la línea para registrar ese número de forma automática como la cantidad producida.

En caso de que sea necesario proporcionar un número distinto, haga clic en el paso Registrar producción para abrir una ventana emergente. Escriba el número de unidades producidas en el campo Unidades y después haga clic en Validar para registrar ese número.

 Nota

El paso _Registrar producción_ aparece en todas las tarjetas de las órdenes de trabajo. Es necesario completarlo en la primera orden de trabajo a procesar, después el paso aparece como completado en todas las órdenes de trabajo restantes en la orden de fabricación.

Después de completar todos los pasos de una orden de trabajo aparecerá un botón en la parte inferior de la tarjeta de la orden correspondiente. Si es necesario que complete otras órdenes de trabajo antes de cerrar la orden de fabricación, el botón dirá Marcar como hecho; en caso contrario, dirá Cerrar producción.

Hacer clic en Marcar como hecho hace que la tarjeta de la orden de trabajo desaparezca. El estado de la orden de trabajo se marca como _Terminado_ en la orden de fabricación una vez que desaparece por completo y la siguiente orden de trabajo aparece en el módulo _Taller_, en la página del centro de trabajo donde está configurada para llevarse a cabo. Cualquier orden de trabajo adicional se puede procesar con las instrucciones detalladas en esta sección.

La tarjeta de la orden de trabajo desaparece al hacer clic en Cerrar producción. Una vez que desaparece por completo, la orden de fabricación aparece como _hecha_ y las unidades elaboradas del producto ahora son parte del inventario.

Después de hacer clic en Marcar como hecho o en Cerrar producción, esos botones se reemplazan por el botón Deshacer. Haga clic en el botón Deshacer antes de que la tarjeta de la orden de trabajo desaparezca por completo para mantener esa orden abierta.

 Truco

Esta sección describe el flujo de trabajo básico para procesar una orden de fabricación en el módulo _Taller_. Consulte la [Información general de Taller](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/shop_floor/shop_floor_overview.html#manufacturing-shop-floor-shop-floor-overview) para obtener una explicación más detallada del módulo y todas sus funciones.