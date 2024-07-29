En la aplicación _Calidad_ de Odoo, _Tomar una foto_ es uno de los tipos de control de calidad que se pueden seleccionar al crear un nuevo control de calidad o punto de control de calidad. El tipo de control _Tomar una foto_ requiere que se adjunte una foto al control, la cual luego puede ser revisada por un equipo de calidad.

## Crear el control de calidad “Tomar una foto”[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/picture_check.html#create-a-take-a-picture-quality-check "Enlazar permanentemente con este título")

Hay dos formas en las que se puede crear un punto de control de calidad tipo _Tomar una foto_. Puede crear un control de calidad de manera manual, o puede configurar un punto de control de calidad para crear controles de manera predeterminada en un intervalo establecido.

Esta documentación solo incluye información sobre las opciones de configuración pertenecientes a los controles y puntos de control de calidad de tipo _Tomar una foto_. Si desea obtener un resumen completo de todas las opciones de configuración disponibles al crear un control de calidad o puntos de control de calidad, consulte la documentación sobre [controles de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_checks.html#quality-quality-management-quality-checks) y [puntos de control de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_control_points.html#quality-quality-management-quality-control-points).

### Control de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/picture_check.html#quality-check "Enlazar permanentemente con este título")

Si desea crear un solo control de calidad tipo _Tomar una foto_, vaya a Calidad ‣ Control de calidad ‣ Controles de calidad y haga clic en Nuevo. Complete el nuevo formulario de control de calidad como se indica aquí:

- En el campo desplegable Tipo seleccione Tomar una foto.
    
- En el campo desplegable Equipo seleccione el equipo de control de calidad responsable por este control.
    
- En el campo de texto Instrucciones de la pestaña Notas escriba las instrucciones para tomar la foto.
    

![Un formulario de control de calidad configurado para un control de calidad 'Tomar una Foto'.](https://www.odoo.com/documentation/17.0/es/_images/picture-check-form.png)

### Punto de control de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/picture_check.html#quality-control-point "Enlazar permanentemente con este título")

Para crear un punto de control de calidad que genere controles de calidad de tipo _Tomar una foto_ de forma automática, vaya a Calidad ‣ Control de calidad ‣ Puntos de control y haga clic en Nuevo. Complete el formulario del nuevo punto de control de calidad de la siguiente forma:

- En el campo desplegable Tipo seleccione Tomar una foto.
    
- Si tiene instalada la aplicación _Mantenimiento_, verá el campo dispositivo después de seleccionar _Tomar una foto_. Utilice este campo para especificar un dispositivo que se debe utilizar para tomar fotografías de control de calidad. Si desea obtener más información sobre cómo gestionar dispositivos en la aplicación _Mantenimiento_, consulte la documentación sobre [añadir nuevo equipo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/add_new_equipment.html#maintenance-equipment-management-add-new-equipment).
    
- En el campo desplegable Equipo seleccione al equipo de calidad responsable de gestionar los controles creados por el punto de control de calidad.
    
- En el campo de texto Instrucciones explique cómo se deben tomar las fotos.
    

![Ejemplo de un punto de control de calidad configurado para un control de calidad tipo Tomar una foto.](https://www.odoo.com/documentation/17.0/es/_images/picture-qcp-form.png)

## Procesar un control de calidad tipo Tomar una foto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/picture_check.html#process-a-take-a-picture-quality-check "Enlazar permanentemente con este título")

Hay muchas maneras en las que podemos procesar los controles de calidad tipo _Tomar una foto_. Si asignamos un control de calidad a una orden de fabricación, inventario o trabajo específico, el control de calidad se puede procesar directamente en la orden. También es posible procesar un control de calidad desde la página del control de calidad.

### Desde la página de controles[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/picture_check.html#from-the-check-s-page "Enlazar permanentemente con este título")

Si desea procesar un control de calidad tipo _tomar foto_ vaya a Calidad ‣ Control de calidad ‣ Controles de calidad y seleccione un control de calidad. Siga las instrucciones para realizar la medida.

Después de tomar la fotografía, asegúrese de que esté almacenada en el dispositivo que está utilizando para realizar el control de calidad (computadora, tableta, etc.). Luego, haga clic en el botón ✏️ (lápiz) en la sección de Imagen para abrir el administrador de archivos del dispositivo. Busque la imagen en el administrador de archivos, selecciónela y haga clic en Abrir para adjuntarla.

![El botón de edición (lápiz) en un control de calidad de tipo "Tomar una foto".](https://www.odoo.com/documentation/17.0/es/_images/picture-edit-button.png)

### En una orden[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/picture_check.html#on-an-order "Enlazar permanentemente con este título")

Para procesar un control de calidad de tipo _Tomar una foto_ seleccione una orden de fabricación o de inventario (recibo, entrega, devolución, etc.) que deba pasar por un control. Vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación para seleccionar las órdenes de fabricación y luego haga clic en una. Para seleccionar una orden de inventario vaya a Inventario, haga clic en el botón # por procesar que se encuentra en la tarjeta de operación y seleccione una orden.

En la orden de inventario o de fabricación seleccionada aparecerá un botón morado de Controles de calidad en la parte superior de la página. Haga clic en el botón para abrir la ventana emergente de Control de calidad, lo que mostrará todos los controles de calidad que se requieren para esa orden.

Siga las instrucciones detalladas sobre cómo tomar la fotografía que aparecen en la ventana emergente Control de calidad. Después de tomar la fotografía, asegúrese de que esté almacenada en el dispositivo que está utilizando para realizar el control de calidad (computadora, tableta, etc.).

Haga clic en el botón Tomar una foto en la sección de Imagen para abrir el administrador de archivos del dispositivo. Busque la imagen en el administrador de archivos, selecciónela y haga clic en Abrir para adjuntarla. Por último, haga clic en Validar en la ventana emergente Control de calidad.

![La ventana emergente de control de calidad de tipo "Tomar una foto" en una orden de fabricación o de inventario.](https://www.odoo.com/documentation/17.0/es/_images/picture-check-pop-up.png)

Si necesita crear una alerta de calidad, haga clic en el botón Alerta de calidad que está ubicado en la parte superior de la orden de fabricación o de inventario después de validar el control de calidad. Al hacer clic en Alerta de calidad se desplegará un formulario de alerta de calidad en una nueva página. Para revisar la guía completa sobre cómo completar los formularios de alerta de calidad, consulte la documentación relacionada a las [alertas de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_alerts.html#quality-quality-management-quality-alerts).

### En una orden de trabajo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/picture_check.html#on-a-work-order "Enlazar permanentemente con este título")

Al configurar un punto de control de calidad que se activa durante la fabricación, también puede especificar una orden de trabajo en el campo Operación de orden de trabajo del formulario del punto de control de calidad. Si especifica una orden de trabajo, se creará un control de calidad de tipo _Tomar una foto_ para esa orden de trabajo, no para toda la orden de fabricación.

Los controles de calidad de tipo _Tomar una foto_ configurados para las órdenes de trabajo se **deben** completar desde el módulo _Taller_. Para ello, vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y seleccione una que necesite de un control de calidad de tipo _Tomar una foto_.

En la orden de fabricación, seleccione la pestaña Órdenes de trabajo y haga clic en el botón Abrir orden de trabajo (icono de enlace externo) ubicado en la línea de la orden de trabajo a procesar. Aparecerá la ventana emergente Órdenes de trabajo, allí haga clic en el botón Abrir Taller para abrir el módulo _Taller_.

Cuando accede desde una orden de trabajo específica, el módulo _Taller_ se abre en la página del centro de trabajo donde está configurado que se procesará la orden. Además, separa la tarjeta de la orden de trabajo para que no aparezcan otras tarjetas.

Procese los pasos de la orden de trabajo hasta que llegue al paso para _tomar una foto_ en el control de calidad. Haga clic en él para abrir una ventana emergente con las instrucciones necesarias para tomar la fotografía. Después de haberla tomado, asegúrese de que está almacenada en el dispositivo que utilizará para procesar el control de calidad (puede ser una computadora, una tableta, entre otras opciones).

Después, haga clic en el botón Tomar una foto de la ventana emergente para abrir el explorador de archivos del dispositivo. Una vez allí, busque la fotografía, selecciónela y haga clic en Abrir para adjuntarla.

Por último, haga clic en el botón Validar ubicado en la parte inferior de la ventana emergente para completar el control de calidad. Después de eso, la ventana emergente avanzará al siguiente paso de la orden de trabajo.

![Un control de calidad de tipo tomar una foto en el módulo Taller.](https://www.odoo.com/documentation/17.0/es/_images/picture-check-shop-floor.png)

Si es necesario crear una alerta de calidad, haga clic en el botón X (cerrar) ubicado en la esquina superior derecha para salir de la ventana emergente.

Después, haga clic en el botón ⋮ (tres puntos verticales) ubicado en la esquina inferior derecha en la tarjeta de la orden de trabajo para abrir la ventana emergente ¿Qué desea hacer?.

En la ventana emergente ¿Qué desea hacer?, elija el botón Crear una alerta de calidad. Esta acción abrirá un formulario de alerta de calidad vacío en una nueva ventana emergente de Alertas de calidad.

 Ver también

Consulte la documentación sobre [alertas de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_alerts.html) para obtener más información sobre cómo completar los formularios de las alertas de calidad.

## Revisar la imagen adjunta a un control de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/picture_check.html#review-picture-attached-to-quality-check "Enlazar permanentemente con este título")

Los miembros del equipo de control de calidad u otros usuarios pueden revisar una fotografía adjunta al control de calidad. Vaya a Calidad ‣ Control de calidad ‣ Controles de calidad y seleccione un control.

La fotografía adjunta aparece en la sección Imagen del formulario del control de calidad. Después de revisar la imagen, haga clic en el botón Aprueba si el control es exitoso o en el botón Falla si el control es erróneo.

![Una verificación de tipo "Tome una fotografía" con una foto adjunta.](https://www.odoo.com/documentation/17.0/es/_images/review-picture-check.png)