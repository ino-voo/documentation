Cuando los empleados inician sesión como _operadores_ en el módulo _Taller_ de Odoo pueden llevar seguimiento de la cantidad de tiempo que usan para trabajar en cada orden.

Odoo lleva seguimiento del tiempo que toma completar cada orden de trabajo y del tiempo que cada operador utiliza en ella.

## Iniciar sesión como operador[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/shop_floor/shop_floor_tracking.html#operator-sign-in "Enlazar permanentemente con este título")

Para iniciar sesión en el módulo _Taller_ como operador, primero inicie sesión en su base de datos y abra el módulo Taller. En automático, el perfil del empleado que inició sesión en la base de datos entrará como operador.

Todos los operadores activos aparecen en el panel del operador ubicado del lado izquierdo del módulo. Es posible abrir u ocultar el panel si hace clic en el botón mostrar u ocultar panel (cuadrado blanco con columna negra del lado izquierdo) que está ubicado en la esquina superior izquierda del módulo.

![El panel del operador del módulo Taller, el botón mostrar u ocultar del panel aparece arriba.](https://www.odoo.com/documentation/17.0/es/_images/operator-panel1.png)

Para iniciar sesión en _Taller_ como un empleado diferente, haga clic en el botón + Agregar operador que se encuentra en la parte inferior del panel. Esta acción abre la ventana emergente Seleccionar empleado en donde aparecen los empleados que puede iniciar sesión en el módulo.

Haga clic en un empleado específico para iniciar sesión con su perfil. Iniciará sesión como ese empleado en automático si no necesita un código PIN.

En caso de que sea necesario un código PIN aparecerá la ventana emergente ¿Contraseña? con un teclado numérico que le permitirá escribirlo. Después, haga clic en Confirmar para iniciar sesión con el módulo _Taller_.

![La ventana emergente "¿Contraseña?" que se usa para escribir el código NIP del operador.](https://www.odoo.com/documentation/17.0/es/_images/pin-code.png)

 Nota

Es posible configurar un código NIP para cada empleado y deberán usarlo para iniciar sesión en el módulo _Taller_, registrar entradas y salidas en el _modo quiosco_ de la aplicación _Asistencias_ e iniciar sesión como cajero en la aplicación _Punto de venta_.

Para configurar el NIP del empleado, vaya a la aplicación Empleados y seleccione a un empleado. En la parte inferior del formulario del empleado, haga clic en la pestaña Ajustes de RR. HH. y escriba un código numérico en el campo Código NIP.

Cuando un empleado inicie sesión en el módulo, su nombre aparecerá en el panel del operador junto con todos los demás empleados que también han iniciado sesión. En este panel pueden aparecer varios empleados, pero solo un empleado puede estar activo en un momento en particular en una sola instancia del módulo _Taller_.

Haga clic en el nombre de un empleado para activar su perfil. El empleado activo aparece en color azul y los empleados que han iniciado sesión, pero están inactivos, no tienen ningún color en su nombre.

Para cerrar la sesión de un empleado en específico del módulo, haga clic en el botón X (eliminar) ubicado junto a su nombre en el panel del operador.

## Seguimiento de la duración de las órdenes de trabajo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/shop_floor/shop_floor_tracking.html#track-work-order-duration "Enlazar permanentemente con este título")

Para llevar seguimiento del tiempo utilizado al trabajar en una orden de trabajo, primero seleccione al empleado que trabaja en ella en el panel del operador.

Después, vaya a la página del centro de trabajo donde está programada la orden de trabajo. Para ello, seleccione el centro de trabajo en la parte superior del módulo _Taller_ o haga clic en el nombre del centro de trabajo en la tarjeta de la orden de fabricación de la que forma parte esa orden de trabajo.

Busque la tarjeta de la orden de trabajo en la página del centro de trabajo. Una vez que comience el trabajo, haga clic en el encabezado de la tarjeta de la orden para comenzar a cronometrar la duración que tarda en completarla. Esta duración aparece en un temporizador en el encabezado de la tarjeta correspondiente y registra el tiempo de todos los empleados que se usó para trabajar en la orden de trabajo.

![Una tarjeta de una orden de trabajo con un temporizador activo.](https://www.odoo.com/documentation/17.0/es/_images/work-order-timer.png)

Además, el número de referencia de la orden de trabajo aparece en el panel del operador abajo del nombre del empleado que está trabajando en ella, junto con un segundo temporizador que registra la cantidad de tiempo que el empleado ha utilizado en esa orden de trabajo. Este temporizador solo corresponde al trabajo realizado durante la sesión actual, incluso si el empleado ya había trabajado antes en esa orden.

Los empleados pueden trabajar en varias órdenes de trabajo de forma simultánea y llevar seguimiento del tiempo que emplean en cada una. El número de referencia de sus órdenes de trabajo activas aparecen abajo del nombre del empleado junto con un temporizador.

![Una tarjeta de empleado en el panel del operador, aparecen dos temporizadores de órdenes de trabajo.](https://www.odoo.com/documentation/17.0/es/_images/employee-timer.png)

Haga clic en el encabezado una segunda vez para pausar el temporizador de la tarjeta de la orden de trabajo y eliminar la orden de trabajo que se encuentra abajo del nombre del empleado en el panel del operador.

Una vez que la orden de trabajo esté completa, haga clic en el botón Marcar como hecho que se encuentra en la parte inferior de la tarjeta de la orden correspondiente, esto hará que la tarjeta desaparezca. Si el temporizador sigue activo, este se detendrá cuando la tarjeta desaparezca por completo.

## Ver la duración de una orden de trabajo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/shop_floor/shop_floor_tracking.html#view-work-order-duration "Enlazar permanentemente con este título")

Para visualizar la duración de una orden de trabajo vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y seleccione una.

Elimine el filtro Por hacer de la barra de búsqueda para ver y seleccionar las órdenes de fabricación que ya están completas y también están marcadas como _hechas_. Haga clic en el botón X (cerrar) ubicado del lado derecho del filtro.

En la página de la orden de fabricación, haga clic en la pestaña Órdenes de trabajo para ver una lista de todas las órdenes incluidas en la orden de fabricación. En la columna Duración real de la pestaña aparece el tiempo que tomó completar cada orden de trabajo.

La _duración real_ representa el tiempo total utilizado en la orden de trabajo por todos los trabajadores que trabajaron en ella. Además, incluye el tiempo registrado en el módulo _Taller_, así como el tiempo registrado en la pestaña Órdenes de Trabajo de la orden de fabricación.