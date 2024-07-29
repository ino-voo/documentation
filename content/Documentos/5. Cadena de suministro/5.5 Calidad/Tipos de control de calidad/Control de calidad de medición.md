En la aplicación _Calidad_ de Odoo, un control de calidad de _Medidas_ es uno de los tipos de control de calidad que puede seleccionar al crear un nuevo control de calidad o un nuevo punto de control de calidad. Los controles de calidad de _Medidas_ le pedirán al usuario que mida una parte del producto para registrarlo dentro de Odoo. Para pasar el control de calidad, el valor medido debe estar dentro de una _tolerancia_ específica de un valor _normativo_.

## Crear un control de calidad de Medida[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/measure_check.html#create-a-measure-quality-check "Enlazar permanentemente con este título")

Hay dos formas en las que puede crear un punto de control de calidad de tipo _Medida_. Puede crear un control de calidad de manera manual o puede configurar un punto de control de calidad para crear controles en automático en un intervalo predeterminado.

Esta documentación solo incluye información sobre las opciones de configuración pertenecientes a los controles y puntos de control de calidad de tipo _Medida_. Si desea obtener un resumen completo de todas las opciones de configuración disponibles al crear un control de calidad o puntos de control de calidad, consulte la documentación sobre [controles de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_checks.html#quality-quality-management-quality-checks) y [puntos de control de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_control_points.html#quality-quality-management-quality-control-points).

### Control de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/measure_check.html#quality-check "Enlazar permanentemente con este título")

Para crear un solo control de calidad tipo _Medida_, vaya a Calidad ‣ Control de calidad ‣ Controles de calidad y haga clic en Nuevo. Llene el nuevo formulario de control de calidad como se indica aquí:

- En el campo desplegable Tipo seleccione Medida.
    
- En el campo desplegable Equipo seleccione el equipo de control de calidad responsable por este control.
    
- En el campo de texto Instrucciones de la pestaña Notas escriba las instrucciones para tomar la foto.
    

![Un ejemplo de un control de calidad configurado para un tipo de control de calidad Medida.](https://www.odoo.com/documentation/17.0/es/_images/measure-check-form-1.png)

### Punto de control de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/measure_check.html#quality-control-point-qcp "Enlazar permanentemente con este título")

Para crear un punto de control de calidad que genere controles de calidad de tipo _Medida_ de forma automática, vaya a Calidad ‣ Control de calidad ‣ Puntos de control y haga clic en Nuevo. Complete el formulario del nuevo punto de control de calidad de la siguiente forma:

- En el campo desplegable Tipo seleccione el tipo de control de calidad Medida. Esto hará que aparezcan dos campos nuevos: Norma y Tolerancia.
    
    - Use el primer campo de texto en Norma para registrar la medida ideal a la que un producto se debería apegar. Use el segundo campo de texto para especificar la unidad de medida que se debe usar.
        
    - El campo Tolerancia tiene dos subcampos: de y hasta. Use el campo de para especificar la medida mínima aceptable y el campo hasta para especificar la medida máxima aceptable.
        
- En el campo desplegable Equipo seleccione al equipo de calidad responsable de gestionar los controles creados por el punto de control de calidad.
    
- En el campo de texto Instrucciones explique cómo se deben tomar las medidas.
    

![Un ejemplo de un formulario de punto de control de calidad configurado para crear controles de calidad tipo Medidas.](https://www.odoo.com/documentation/17.0/es/_images/measure-check-qcp-form.png)

## Procesar un control de calidad tipo Medida[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/measure_check.html#process-a-measure-quality-check "Enlazar permanentemente con este título")

Hay muchas maneras en las que podemos procesar los controles de calidad tipo _Medidas_. Si asignamos un control de calidad a una orden de fabricación, inventario o trabajo específico, el control de calidad se puede procesar directamente en la orden. También es posible procesar un control de calidad desde la página del control de calidad.

### Desde la página de controles[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/measure_check.html#from-the-check-s-page "Enlazar permanentemente con este título")

Para procesar un control de calidad tipo _Medida_ vaya a Calidad ‣ Control de calidad ‣ Controles de calidad y seleccione un control de calidad. Siga las Instrucciones ver cómo realizar la medida.

Después de tomar la medida, registre el valor en el campo Medida en el formulario de control de calidad. Para pasar o fallar un control de forma manual, haga clic en guilabel:`Aprobado` o Falló en la parte superior del control.

Alternativamente, si el control de calidad está asignado a un punto de control de calidad para el que se han especificado valores de _norma_ y _tolerancia_, haga clic en Medir en la esquina superior izquierda del control. Al hacerlo, la comprobación se marcará automáticamente como _Aprobado_ si el valor registrado está dentro de la _tolerancia_ especificada, o como _Fallida_ si el valor está fuera de ella.

### En una orden[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/measure_check.html#on-an-order "Enlazar permanentemente con este título")

Para procesar un control de calidad tipo _Medidas_ seleccione una orden de fabricación o de inventario (recibo, entrega, devolución, etc.) que necesita pasar por el control. Para seleccionar las órdenes de fabricación vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y haga clic en una orden. Para seleccionar una orden de inventario vaya a Inventario, haga clic en el botón # Por procesar que se encuentra en la tarjeta de operación y seleccione un orden.

En la orden de inventario o de fabricación seleccionada aparecerá un botón morado de Controles de calidad en la parte superior de la página. Haga clic en el botón para abrir la ventana emergente de Control de calidad, lo que mostrará todos los controles de calidad que se requieren para esa orden.

Para procesar una revisión de calidad tipo _Medida_, primero debe medir el producto como se le pida, después ingrese el valor en el campo Medida en la ventana emergente y haga clic en Validar para registrar el valor registrado.

![La ventana emergente de un control tipo Medida en una orden de fabricación o de inventario.](https://www.odoo.com/documentation/17.0/es/_images/measure-check-pop-up.png)

Si el valor que proporcionó se encuentra dentro del rango especificado en la sección Tolerancia del punto de control de calidad, el control de calidad se aprobará y la ventana emergente se cerrará. Puede procesar el resto de las órdenes de fabricación o inventario como de costumbre.

Sin embargo, si el valor que proporcionó está fuera del rango especificado, aparecerá una nueva ventana emergente con el nombre Falló el control de calidad. En el cuerpo de la ventana emergente aparecerá el mensaje Midió # unidades y debería medir entre # unidades y # unidades. además de las instrucciones que proporcionó en la pestaña Mensaje en caso de error del punto de control de calidad. En la parte inferior de la ventana emergente aparecerán dos botones: Corregir medida y Confirmar medida.

![La ventana emergente de "falló el control de calidad"](https://www.odoo.com/documentation/17.0/es/_images/measure-check-failed.png)

Si la medida no se ingresó correctamente y tiene que cambiarla, seleccione Corregir medida. Así se volverá a abrir la ventana emergente de Control de calidad. Ingrese la medida correcta en el campo Medida y después haga clic en Validar para completar la revisión.

Si la medida se ingresó de forma correcta, haga clic en Confirmar medida y el control de calidad fallará. Siga todas las instrucciones enlistadas en la ventana emergente Falló el control de calidad.

Si se debe de crear una alerta de control de calidad, haga clic en el botón Alerta de calidad que aparece en la parte superior de la orden de fabricación o inventario después de que se falle el control de calidad. Al hacer clic en esta botón, se abrirá un formulario nuevo de alerta de calidad en una nueva página.

 Ver también

Consulte la documentación sobre [alertas de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_alerts.html) para obtener más información sobre cómo completar el formulario de una alerta de calidad.

### En una orden de trabajo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/measure_check.html#on-a-work-order "Enlazar permanentemente con este título")

Al configurar un punto de control de calidad que se activa durante la fabricación, también puede especificar una orden de trabajo en el campo Operación de orden de trabajo del formulario del punto de control de calidad. Si especifica una orden de trabajo, se creará un control de calidad de tipo _Medida_ para esa orden de trabajo, no para toda la orden de fabricación.

Los controles de calidad de tipo _Medida_ configurados para las órdenes de trabajo se **deben** completar desde el módulo _Taller_. Para ello, vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y seleccione una que necesite de un control de calidad de tipo _Medida_.

En la orden de fabricación, seleccione la pestaña Órdenes de trabajo y haga clic en el botón Abrir orden de trabajo (icono de enlace externo) ubicado en la línea de la orden de trabajo a procesar. Aparecerá la ventana emergente Órdenes de trabajo, allí haga clic en el botón Abrir Taller para abrir el módulo _Taller_.

Cuando accede desde una orden de trabajo específica, el módulo _Taller_ se abre en la página del centro de trabajo donde está configurado que se procesará la orden. Además, separa la tarjeta de la orden de trabajo para que no aparezcan otras tarjetas.

Procese los pasos de la orden de trabajo hasta que llegue al paso de _medición_ del control de calidad. Haga clic en él para abrir una ventana emergente con las instrucciones necesarias para tomar las medidas. Una vez que haya terminado, escríbalas en el campo Medida de la ventana emergente y después haga clic en Validar.

![Un control de calidad de tipo medición en el módulo Taller.](https://www.odoo.com/documentation/17.0/es/_images/measure-check-shop-floor.png)

Si la medida que proporcionó se encuentra dentro del rango especificado en la sección Tolerancia del punto de control de calidad, el control de calidad se aprobará y la ventana emergente avanzará al siguiente paso de la orden de trabajo. Sin embargo, si la medida no está dentro del rango especificado, aparecerá la ventana emergente Falló el control de calidad.

En el contenido de la ventana emergente Falló el control de calidad aparece un mensaje en el que se puede leer: Midió # unidades, y debería medir entre # unidades y # unidades, así como las instrucciones que proporcionó en la pestaña Mensaje en caso de error del punto de control de calidad. En la parte inferior de la ventana emergente aparecen dos botones: Corregir medida y Confirmar medida.

![La ventana emergente Falló el control de calidad de un control de tipo medición en el módulo Taller.](https://www.odoo.com/documentation/17.0/es/_images/shop-floor-measure-check-failed.png)

Si la medida no se ingresó de forma adecuada y debe modificarla, seleccione Corregir medida. Esta acción abrirá una nueva ventana emergente con el nombre Control de calidad. Escriba la medida corregida en el campo Medida y luego haga clic en Validar para completar el control y cerrar la ventana emergente.

Si la medida se ingresó de forma correcta, haga clic en Confirmar medida y el control de calidad fallará. Siga todas las instrucciones enlistadas en la ventana emergente Falló el control de calidad.

Si es necesario crear una alerta de calidad, haga clic en el botón X (cerrar) ubicado en la esquina superior derecha para salir de la ventana emergente.

Después, haga clic en el botón ⋮ (tres puntos verticales) ubicado en la esquina inferior derecha en la tarjeta de la orden de trabajo para abrir la ventana emergente ¿Qué desea hacer?.

En la ventana emergente ¿Qué desea hacer?, elija el botón Crear una alerta de calidad. Esta acción abrirá un formulario de alerta de calidad vacío en una nueva ventana emergente de Alertas de calidad.

 Ver también

Consulte la documentación sobre [alertas de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_alerts.html) para obtener más información sobre cómo completar los formularios de las alertas de calidad.