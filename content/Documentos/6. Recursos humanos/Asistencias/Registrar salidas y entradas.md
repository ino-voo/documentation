La aplicación _Asistencias_ de Odoo permite que los usuarios que iniciaron sesión en la base de datos puedan registrar su entrada y su salida sin tener que abrir la misma aplicación o usar un kiosco. Esta función puede ser muy útil para pequeñas empresas en las que todos los empleados también son usuarios.

Un usuario puede registrar su entrada y su salida desde el tablero principal de la base de datos y cualquier otra aplicación. En la esquina superior derecha del menú principal superior, que siempre está visible sin importar en qué aplicación se encuentre el usuario, aparece un 🔴 (círculo rojo) o un 🟢 (círculo verde). Haga clic en el círculo de color para abrir el widget de asistencia, donde el usuario podrá registrar su entrada o su salida.

![Menú de la esquina superior derecha con el botón para registrar entrada encerrado en un círculo rojo.](https://www.odoo.com/documentation/17.0/es/_images/top-menu.png)

## Registrar entrada[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/check_in_check_out.html#check-in "Enlazar permanentemente con este título")

El circulo del widget de asistencia aparece en color rojo cuando el usuario no ha registrado su entrada. Haga clic en el 🔴 (círculo rojo), aparecerá el widget de asistencia con el botón Registrar entrada :icon:`fa-sign-in de color verde.

![Menú de la esquina superior derecha con el botón para registrar entrada encerrado en un círculo rojo.](https://www.odoo.com/documentation/17.0/es/_images/check-in.png)

Cuando el usuario registra su entrada desde la base de datos, la aplicación _Asistencias_ también registra los detalles relacionados a su ubicación, como la dirección IP y sus coordenadas de GPS.

 Importante

El usuario debe permitir que su computadora acceda a la información de ubicación para que la aplicación _Asistencias_ pueda registrar los detalles correspondientes.

Este botón será el único elemento visible en el widget si el usuario aún no ha registrado su entrada y salida durante el día laboral actual. Si el usuario ya hizo esto con anterioridad, entonces aparece el campo Total de hoy arriba del botón y el tiempo total registrado aparece en ese campo en el formato HH:MM (horas:minutos).

Haga clic en el botón Registrar entrada  para registrarla. El 🔴 (círculo rojo) en el menú superior ahora será de color verde y el aspecto del widget también cambiará. El widget se actualizará para indicar que el usuario ha registrado su entrada, el botón verde Registrar entrada  ahora será el botón amarillo Registrar salida 

Haga clic en cualquier parte de la pantalla para cerrar el widget de asistencia.

## Registrar salida[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/check_in_check_out.html#check-out "Enlazar permanentemente con este título")

Si es la primera vez que el usuario registra su salida, en la parte superior del widget aparece Desde HH:MM (AM/PM) con la hora en que el usuario registró su entrada en el campo de tiempo. Abajo de esa línea aparecerá HH:MM, para indicar las horas y minutos transcurridos desde que registró su entrada. A medida que pasa el tiempo, este valor se actualiza para que coincida con las horas y minutos que han pasado desde ese momento.

Si el usuario ya había registrado entrada y salida, entonces aparecerán algunos campos adicionales. Además del campo Antes de HH:MM (AM/PM) aparece el campo Desde HH:MM (AM/PM). Las horas mostradas en ambos campos coinciden y se completan con la hora registrada más reciente. Abajo del campo Antes de HH:MM (AM/PM), aparece el tiempo registrado antes en el formato HH:MM (horas:minutos).

Además, aparece el campo Total de hoy abajo de los otros dos y corresponde a la suma de los campos Antes de HH:MM (AM/PM) y Desde HH:MM (AM/PM). Es el tiempo total que se registra para el usuario en caso de que registrare su salida en ese momento.

Los campos Desde HH:MM (AM/PM) y Total de hoy se actualizan en tiempo real conforme pasa el tiempo. Para registrar una salida, haga clic en el botón amarillo Registrar salida . El widget de asistencia se actualiza otra vez y el campo Total de hoy muestra el tiempo registrado. El botón amarillo Registrar salida  ahora es un botón verde Registrar entrada .

Cuando el usuario registra su salida desde la base de datos, la aplicación _Asistencias_ también registra los detalles relacionados a su ubicación. La información **solo** se registra si el usuario permite que su computadora acceda a esta información.

![El pop-up que aparece cuando un empleado registra su entrada desde la base de datos.](https://www.odoo.com/documentation/17.0/es/_images/check-in-database-message.png)

 Truco

No hay límite en la cantidad de veces que un usuario puede registrar entrada y salida, incluso pueden hacerlo sin que haya transcurrido tiempo (un valor de 00:00). Cada que un empleado registra entrada y salida, la información se almacena y aparece en el tablero principal de **Asistencias**, también aparecen los registros de entrada y salida sin valor de tiempo.