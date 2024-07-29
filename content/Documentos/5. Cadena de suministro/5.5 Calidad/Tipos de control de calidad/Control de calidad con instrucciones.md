En la aplicación _Calidad_ de Odoo, uno de los tipos de punto de control de calidad que se puede seleccionar al crear un nuevo punto de control de calidad es _Instrucciones_. Los controles tipo _Instrucciones_ consisten en un campo de entrada de texto que le permite al creador ingresar instrucciones sobre cómo se debe realizar el control.

Para obtener un resumen de cómo configurar un control de calidad o un punto de control de calidad, consulte la documentación sobre [controles de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_checks.html#quality-quality-management-quality-checks) y [puntos de control de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_control_points.html#quality-quality-management-quality-control-points).

## Procesar un control de calidad de tipo instrucciones[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/instructions_check.html#process-an-instructions-quality-check "Enlazar permanentemente con este título")

Hay muchas maneras en las que podemos procesar los controles de calidad tipo _instrucciones_. Si asignamos un control de calidad a una orden de fabricación, inventario o trabajo específico, el control de calidad se puede procesar directamente en la orden. También es posible procesar un control de calidad desde la página del control de calidad.

### Proceso desde la página del control de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/instructions_check.html#process-from-the-quality-check-s-page "Enlazar permanentemente con este título")

Para procesar un control de calidad tipo _Instrucciones_ vaya a Calidad ‣ Control de calidad ‣ Controles de calidad y seleccione un control de calidad. Siga las Instrucciones para completar el control.

Si un producto pasa el control de calidad, haga clic en Aprobado que se encuentra en la parte superior derecha del formulario de control de calidad. Si el producto no pasó la revisión, haga clic en Fallido.

### Procesar control de calidad en una orden[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/instructions_check.html#process-quality-check-on-an-order "Enlazar permanentemente con este título")

Para procesar un control de calidad tipo _Instrucciones_ seleccione una orden de fabricación o de inventario (recibo, entrega, devolución, etc.) que necesita pasar por el control. Para seleccionar las órdenes de fabricación vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y haga clic en una orden. Para seleccionar una orden de inventario vaya a Inventario, haga clic en el botón # Por procesar que se encuentra en la tarjeta de operación y seleccione un orden.

En la orden de fabricación o inventario seleccionada, aparecerá un botón morado llamado Controles de calidad en la parte superior de la orden. Haga clic en el botón para abrir la ventana emergente de Control de calidad, donde podrá procesar los controles de calidad que se creen para la orden.

![La ventana emergente de Control de calidad en una orden de fabricación o de inventario.](https://www.odoo.com/documentation/17.0/es/_images/quality-check-pop-up.png)

Para completar un control de calidad de _instrucciones_ siga las instrucciones detalladas en la ventana emergente Control de calidad. Finalmente, haga clic en Validar para confirmar que se completó el control.

Si se encuentra un problema o un defecto durante el control de calidad, es posible que necesite crear una alerta de calidad para notificar al equipo de calidad. Para hacerlo, haga clic en el botón Alerta de calidad que aparece en la parte superior de la orden de fabricación o inventario después de validar un control de calidad.

Al hacer clic en Alerta de calidad se abrirá un formulario de alerta de calidad en una nueva página. Para ver una guía completa sobre cómo llenar un formulario de alerta de calidad, vea la documentación en [alertas de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_alerts.html#quality-quality-management-quality-alerts).

### Procesamiento de un control de calidad en una orden de trabajo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/instructions_check.html#process-work-order-quality-check "Enlazar permanentemente con este título")

Al configurar un punto de control de calidad que se activa con una orden de fabricación, también puede especificar una orden de trabajo en el campo Operación de orden de trabajo del formulario del punto de control de calidad. Si especifica una orden de trabajo, se creará un control de calidad llamado _Instrucciones_ para esa orden de trabajo en específico, en lugar de crearse para toda la orden de fabricación.

Los controles de calidad configurados para las órdenes de trabajo se **deben** completar desde el módulo _Taller_. Para ello, vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y seleccione una que necesite de un control de calidad de tipo _Instrucciones_.

En la orden de fabricación, seleccione la pestaña Órdenes de trabajo y haga clic en el botón Abrir orden de trabajo (cuadrado con una fleca apuntando hacia arriba) ubicado en la línea de la orden de trabajo a procesar. Aparecerá la ventana emergente Órdenes de trabajo, allí haga clic en el botón Abrir Taller para abrir el módulo _Taller_.

Cuando accede desde una orden de trabajo específica, el módulo _Taller_ se abre en la página del centro de trabajo donde está configurado que se procesará la orden. Además, separa la tarjeta de la orden de trabajo para que no aparezcan otras tarjetas.

Comience a procesar los pasos de la orden de trabajo hasta que llegue al paso de _Instrucciones_ del control de calidad. Haga clic en él para abrir una ventana emergente que incluye los detalles necesarios para completar el control de calidad. Una vez que haya terminado, haga clic en el botón Siguiente para completar el control y continuar con el siguiente paso.

![Visualización de un control de tipo instrucciones en el módulo Taller.](https://www.odoo.com/documentation/17.0/es/_images/instructions-check-shop-floor.png)

Como alternativa, también puede completar un control de calidad con _instrucciones_ si selecciona la casilla que aparece del lado derecho de la línea del paso que se encuentra en la tarjeta de la orden de trabajo. El control de calidad se aprueba en automático con este método y no aparece ninguna ventana emergente.

 Nota

Consulte la [información general de Taller](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/shop_floor/shop_floor_overview.html#manufacturing-shop-floor-shop-floor-overview) para obtener más información sobre el módulo _Taller_.