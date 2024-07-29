En Odoo, los _puntos de control de calidad_ sirven para crear _controles de calidad_ que los empleados deben usar para confirmar la calidad de los productos. Al configurar una o más _ubicaciones fallidas_, los productos que no pasen estos controles se pueden enviar a una de las ubicaciones especificadas.

 Importante

La función _ubicación de fallo_ es una versión nueva de Odoo 17.0 y **no** aparece en ninguna de las versiones previas. Para actualizar su base de datos de Odoo a una versión más reciente, vea la documentación sobre [actualizaciones de bases de datos](https://www.odoo.com/documentation/17.0/es/administration/upgrade.html).

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#configuration "Enlazar permanentemente con este título")

Para usar las ubicaciones de fallo, **debe** activar la función _Ubicaciones de almacenamiento_ en los ajustes de la aplicación _Inventario_. El ajuste permitirá que cree sububicaciones dentro de un almacén, incluyendo ubicaciones de fallo.

Para habilitar las _ubicaciones de inventario_ vaya a la aplicación Inventario ‣ Configuración ‣ Ajustes, y marque la casilla de verificación a un lado de las Ubicaciones de almacenamiento debajo del encabezado Almacenes y después haga clic en Guardar.

![El ajuste de ubicación de almacenamiento en la página de ajustes de inventario.](https://www.odoo.com/documentation/17.0/es/_images/storage-locations-setting.png)

 Importante

Las ubicaciones de fallo son más efectivas cuando se usan para productos configurados como _productos almacenables_. Esto se debe a que los conteos de inventario solo se usan para productos almacenables, mientras que para los productos _consumibles_ no se rastrean conteos exactos.

De todas formas es posible crear controles de calidad para productos consumibles, que después se pueden enviar a ubicaciones de fallo si no pasan el control. Sin embargo, Odoo no registra la cantidad exacta de productos consumibles en una ubicación de fallo.

Para configurar un producto como almacenable vaya a la aplicación Inventario ‣ Productos ‣ Productos y seleccione un producto. En el campo Tipo de producto de la pestaña Información general asegúrese de seleccionar la opción Producto almacenable del menú desplegable.

## Agregar una ubicación de fallo a un punto de control de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#add-failure-location-to-qcp "Enlazar permanentemente con este título")

Para agregar una ubicación de fallo a un [|punto de control de calidad|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#id1) vaya a la aplicación Calidad ‣ Control de calidad ‣ Puntos de control. Seleccione un [|punto de control de calidad|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#id3) de la lista, o haga clic en el botón Nuevo para crear uno nuevo.

 Nota

Las siguientes instrucciones solo detallen los ajustes de configuración necesarios para agregar una ubicación de fallo a un [|punto de control de calidad|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#id5). Para ver un resumen completo de los [|puntos de control de calidad|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#id7) y todas las opciones disponibles al configurarlos, vea la documentación sobre los [puntos de control de calidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_control_points.html).

En el campo Control por en el formulario de [|puntos de control de calidad|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#id9) seleccione la opción Cantidad. Esto hará que aparezca un campo llamado Ubicaciones de fallo en el formulario. Este campo solo está disponible cuando se selecciona la opción Cantidad.

En el campo Ubicaciones de fallo seleccione una o más ubicaciones del menú desplegable. Para crear una ubicación nueva, ingrese el nombre que le quiere poner a la ubicación en el campo y seleccione la opción Crear «[nombre]» del menú desplegable.

![Un formulario de punto de control de calidad en la aplicación Calidad, con una ubicación de fallo configurada.](https://www.odoo.com/documentation/17.0/es/_images/qcp-form1.png)

## Envíe productos a la ubicación de fallo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#send-products-to-failure-location "Enlazar permanentemente con este título")

Una vez que haya configurado el [|punto de control de calidad|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#id11) con una ubicación de fallo o más, los productos que fallen la revisión en el [|punto de control de calidad|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#id13) pueden enviarse a una de las ubicaciones.

Para hacerlo, abra una orden que requiera un control de calidad que se haya creado para un [|punto de control de calidad|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#id15) con una ubicación de fallo. Por ejemplo, vaya a la aplicación Inventario ‣ Operaciones ‣ Recepciones y seleccione la recepción.

En la parte superior de la orden seleccionada haga clic en el botón Controles de calidad para abrir una ventana emergente desde la que puede procesar el control. En la parte inferior de la ventana, haga clic en el botón Fallo para fallar el control de calidad, lo cual hará que se abra una nueva ventana llamada Control de calidad fallido para [Producto].

En el campo Cantidad fallida ingrese la cantidad del producto que no pasó el control de calidad. En el campo Ubicación de fallo seleccione una ubicación a la que se debe enviar la cantidad de fallo. Después, haga clic en Confirmar en la parte inferior de la ventana emergente para cerrarla.

![La ventana emergente que aparece después de que un control de calidad falla.](https://www.odoo.com/documentation/17.0/es/_images/failed-pop-up.png)

Finalmente, en la orden haga clic en el botón Validar en la parte superior de la página para confirmar que los productos que fallaron el control de calidad se enviaron a la ubicación de fallo, mientras que los que pasaron el control se enviaron a sus ubicaciones de almacenamiento usuales.

## Ver el inventario de ubicación de fallo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/failure_locations.html#view-failure-location-inventory "Enlazar permanentemente con este título")

Para ver las cantidades almacenadas de un producto en la ubicación de fallo vaya a Inventario ‣ Configuración ‣ Ubicaciones. Seleccione la ubicación de fallo de la lista y después haga clic en Existencias actuales en la página de la ubicación.

La página de una ubicación de falla muestra todos los productos almacenados en ella y la cantidad que hay de cada uno.