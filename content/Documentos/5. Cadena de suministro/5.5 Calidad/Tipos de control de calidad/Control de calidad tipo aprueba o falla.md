En la aplicación _Calidad_ de Odoo, uno de los tipos de control de calidad que puede seleccionar al crear un nuevo punto de control de calidad es _Aprobar - Fallar_. Los controles tipo _Aprobar - Fallar_ consisten en un campo de entrada de texto que permite que la persona que lo realiza proporcione criterios específicos que un producto debe cumplir para poder cumplir con el control.

## Crear un control de calidad tipo Aprobar - Fallar[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/pass_fail_check.html#create-a-pass-fail-quality-check "Enlazar permanentemente con este título")

Hay dos formas en las que puede crear un punto de control de calidad de tipo _Pasa - Falla_. Puede crear un control de calidad de manera manual o puede configurar un punto de control de calidad para crear controles en automático en un intervalo predeterminado.

Esta documentación solo incluye información sobre las opciones de configuración pertenecientes a los controles y puntos de control de calidad de tipo _Aprueba - Falla_. Si desea obtener un resumen completo de todas las opciones de configuración disponibles al crear un control de calidad o puntos de control de calidad, consulte la documentación sobre [controles de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_checks.html#quality-quality-management-quality-checks) y [puntos de control de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_control_points.html#quality-quality-management-quality-control-points).

### Control de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/pass_fail_check.html#quality-check "Enlazar permanentemente con este título")

Para crear un solo control de calidad tipo _Aprobar - Fallar_, vaya a Calidad ‣ Control de calidad ‣ Controles de calidad y haga clic en Nuevo. Llene el nuevo formulario de control de calidad como se indica aquí:

- En el campo desplegable Tipo seleccione Aprobar - Fallar.
    
- En el campo desplegable Equipo seleccione el equipo de control de calidad responsable por este control.
    
- En el campo de texto Instrucciones de la pestaña Notas escriba las instrucciones sobre los criterios que se deben de cumplir para pasar el control de calidad.
    

![Un ejemplo de un control de calidad configurado para un tipo de control de calidad Aprobar - Fallar.](https://www.odoo.com/documentation/17.0/es/_images/quality-check-form.png)

### Punto de control de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/pass_fail_check.html#quality-control-point-qcp "Enlazar permanentemente con este título")

Para crear un punto de control de calidad que genere controles de calidad de tipo _Aprueba - Falla_ de forma automática, vaya a Calidad ‣ Control de calidad ‣ Puntos de control y haga clic en Nuevo. Complete el formulario del nuevo punto de control de calidad de la siguiente forma:

- En el campo desplegable Tipo seleccione Aprobar - Fallar.
    
- En el campo desplegable Equipo seleccione al equipo de calidad responsable de gestionar los controles creados por el punto de control de calidad.
    
- En el campo de texto Instrucciones escriba las instrucciones sobre los criterios que se deben de cumplir para pasar el control de calidad.
    

![Un ejemplo de un punto de control de calidad configurado para un control de calidad tipo Aprobar - Fallar.](https://www.odoo.com/documentation/17.0/es/_images/qcp-form.png)

## Control de calidad tipo Aprobar - Fallar[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/pass_fail_check.html#process-a-pass-fail-quality-check "Enlazar permanentemente con este título")

Hay muchas maneras en las que podemos procesar los controles de calidad tipo _Medidas_. Si asignamos un control de calidad a una orden de fabricación, inventario o trabajo específico, el control de calidad se puede procesar directamente en la orden. También es posible procesar un control de calidad desde la página del control de calidad.

### Desde la página de controles[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/pass_fail_check.html#from-the-check-s-page "Enlazar permanentemente con este título")

Para procesar un control de calidad tipo _Medida_ vaya a Calidad ‣ Control de calidad ‣ Controles de calidad y seleccione un control de calidad. Siga las Instrucciones ver cómo realizar la medida.

Si se cumplen los criterios para pasar el control de calidad, haga clic en el botón de Aprobar ubicado en la esquina superior izquierda de la página. Si no se cumplen los criterios, haga clic en el botón de No aprobar.

### En una orden[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/pass_fail_check.html#on-an-order "Enlazar permanentemente con este título")

Para procesar un control de calidad tipo _Aprobar - Fallar_ seleccione una orden de fabricación o de inventario (recibo, entrega, devolución, etc.) que necesita pasar por el control. Para seleccionar las órdenes de fabricación vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y haga clic en una orden. Para seleccionar una orden de inventario vaya a Inventario, haga clic en el botón # Por procesar que se encuentra en la tarjeta de operación y seleccione un orden.

En la orden de inventario o de fabricación seleccionada aparecerá un botón morado de Controles de calidad en la parte superior de la orden. Haga clic en el botón para abrir la ventana emergente de Control de calidad, lo que mostrará todos los controles de calidad que se requieren para esa orden.

Para procesar el control de calidad tipo _Aprobar - Fallar_ siga las instrucciones que se muestran en la ventana emergente Control de calidad. Si se cumplen los criterios para el control de calidad, haga clic en el botón Aprobar en la parte inferior de la ventana. Si los criterios no se cumplen, haga clic en el botón Fallar.

![La ventana emergente de un control tipo Aprobar - Fallar en una orden de fabricación o de inventario.](https://www.odoo.com/documentation/17.0/es/_images/pass-fail-check-pop-up.png)

Si se debe de crear una alerta de control de calidad, haga clic en el botón Alerta de calidad que aparece en la parte superior de la orden de fabricación o inventario después de que se falle el control de calidad. Al hacer clic en esta botón, se abrirá un formulario nuevo de alerta de calidad en una nueva página.

 Ver también

Consulte la documentación sobre alertas de calidad para obtener más información sobre cómo completar los formularios de las alertas de calidad.

### En una orden de trabajo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/pass_fail_check.html#on-a-work-order "Enlazar permanentemente con este título")

Al configurar un punto de control de calidad que se activa durante la fabricación, también puede especificar una orden de trabajo en el campo Operación de orden de trabajo del formulario del punto de control de calidad. Si especifica una orden de trabajo, se creará un control de calidad de tipo _Aprueba - Falla_ para esa orden de trabajo, no para toda la orden de fabricación.

Los controles de calidad de tipo _Aprueba - Falla_ configurados para las órdenes de trabajo se **deben** completar desde el módulo _Taller_. Para ello, vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y seleccione una que necesite de un control de calidad de tipo _Aprueba - Falla_.

En la orden de fabricación, seleccione la pestaña Órdenes de trabajo y haga clic en el botón Abrir orden de trabajo (icono de enlace externo) ubicado en la línea de la orden de trabajo a procesar. Aparecerá la ventana emergente Órdenes de trabajo, allí haga clic en el botón Abrir Taller para abrir el módulo _Taller_.

Cuando accede desde una orden de trabajo específica, el módulo _Taller_ se abre en la página del centro de trabajo donde está configurado que se procesará la orden. Además, separa la tarjeta de la orden de trabajo para que no aparezcan otras tarjetas.

Comience a procesar los pasos de la orden de trabajo hasta que llegue al paso de _Aprueba - Falla_ del control de calidad. Haga clic en él para abrir una ventana emergente que incluye los criterios necesarios para determinar si el control de calidad aprueba o falla. Haga clic en el botón Aprueba ubicado en la parte inferior de la ventana emergente si el control pasa o en el botón Falla en caso contrario.

La ventana emergente avanza al siguiente paso de la orden de trabajo si hace clic en el botón Aprueba. Si hace clic en el botón Falla aparece la ventana emergente Falló el control de calidad que incluye detalles sobre lo que debería hacer en este caso.

![Visualización de un control de tipo Aprueba - Falla en el módulo Taller.](https://www.odoo.com/documentation/17.0/es/_images/pass-fail-check-shop-floor.png)

 Truco

Como alternativa, también puede completar un control de calidad de tipo _Aprueba - Falla_ sin necesidad de abrir la ventana emergente si selecciona la casilla que aparece del lado derecho de la línea del paso que se encuentra en la tarjeta de la orden de trabajo. El control de calidad se aprueba en automático con este método y no aparece ninguna ventana emergente.