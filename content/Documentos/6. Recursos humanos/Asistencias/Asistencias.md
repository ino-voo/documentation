La aplicación _Asistencias_ de Odoo cumple la función de un reloj checador. Los empleados pueden registrar su entrada y salida con un dispositivo específico en modo quiosco y también pueden hacerlo desde la base de datos. Los gerentes pueden visualizar con rapidez quién está disponible en cualquier momento, crear reportes para conocer las horas de todos sus empleados y obtener información sobre quiénes están trabajando horas adicionales o registrando su salida antes de la hora correspondiente.

## Permisos de acceso[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#access-rights "Enlazar permanentemente con este título")

Es importante comprender cómo los diferentes permisos de acceso influyen las opciones y funciones a las que los usuarios pueden acceder en la aplicación _Asistencias_.

Cada usuario en la base de datos puede registrar su ingreso y su salida directamente desde la base de datos sin necesitar acceso a la aplicación _Asistencias_. Además, todos los usuarios pueden ingresar a sus propios registros de asistencia desde el formulario de empleado en la aplicación _Empleados_.

El acceso a la aplicación _Asistencias_ y las diferentes funciones dentro de la aplicación depende de los permisos de acceso.

Para visualizar los permisos de acceso de un usuario, vaya a Ajustes ‣ Usuarios y empresas: Usuarios, y haga clic en uno, allí la pestaña Permisos de acceso es visible de forma predeterminada. Diríjase a la sección Recursos humanos para ver la configuración. En el campo de Asistencias, puede dejar el campo vacío o seleccionar Administrador.

Si selecciona la opción Administrador, el usuario tendrá acceso sin restricciones a la aplicación _Asistencias_. Podrá ver todos los registros de asistencia de los empleados, ingresar al _modo quiosco_ desde la aplicación, acceder a todas las métricas de reportes y realizar modificaciones a los ajustes. Si se deja en blanco, el usuario **no** tendrá acceso a la aplicación _Asistencias_.

### Aprobadores[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#approvers "Enlazar permanentemente con este título")

El **único** otro escenario en el que es posible acceder a información distinta en la aplicación _Asistencias_ es si se trata de aprobadores. Si un usuario **no** tiene permisos administrativos en la aplicación _Asistencias_, pero está designado como el aprobador de un empleado en la aplicación _Asistencias_, entonces podrá ver los registros de asistencia de ese empleado en específico y realizar modificaciones en sus registros de asistencia en caso de ser necesario. Esto aplica para todos los empleados en los que el usuario aparece como aprobador para la aplicación _Asistencias_. Por lo general, los aprobadores son los gerentes, aunque esto no es obligatorio.

Para ver quién es el aprobador de asistencias de un empleado, vaya a la aplicación Empleados y haga clic en un empleado en particular. Haga clic en la pestaña Información del trabajo, diríjase a la sección Aprobadores y seleccione el campo Asistencia. La persona seleccionada podrá ver los registros de asistencia de ese empleado, tanto en el tablero de la aplicación _Asistencias_ como en los reportes de asistencia, también podrá realizar modificaciones en sus registros.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#configuration "Enlazar permanentemente con este título")

Es necesario configurar algunas cosas en la aplicación _Asistencias_. En el menú Configuración deberá determinar la manera en que los usuarios registran su entrada y salida, cómo funcionan los quioscos y cómo se calculan las horas adicionales. Vaya a Asistencias ‣ Configuración para acceder al menú de configuración.

### Modos[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#modes "Enlazar permanentemente con este título")

- Asistencias desde el backend: seleccione esta casilla para permitir que los usuarios registren su entrada y salida desde la base de datos de Odoo. Si la casilla no está seleccionada, los usuarios deberán utilizar un quiosco para registrar su asistencia.
    

### Horas adicionales[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#extra-hours "Enlazar permanentemente con este título")

Esta sección especifica cómo se calcula el tiempo adicional. Incluye cuándo se cuenta ese tiempo y qué tiempo no se registra.

- Número de horas adicionales: seleccione esta casilla para permitir que los empleados registren horas adicionales a sus horas laborales establecidas (a veces denominadas como _horas extras_). Si selecciona esta casilla también aparecerán los siguientes ajustes; en caso contrario, no aparecerá nada más.
    
    - Empezar desde: la fecha actual está establecida de forma predeterminada en este campo. Si lo desea, haga clic allí y use el selector de calendario para modificar la fecha de inicio en la que se registrarán las horas adicionales.
        
    - :guilabel:[`](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#id1)Tiempo de tolerancia a favor de la empresa: escriba la cantidad de tiempo, en minutos, que **no** se toma en cuenta para las horas adicionales de un empleado. Cuando un empleado registra su salida y el tiempo adicional registrado se encuentra por debajo de los minutos indicados, entonces **no** cuenta como horas adicionales para el empleado.
        
    - Tiempo de tolerancia a favor del empleado: ingrese la cantidad de tiempo, en minutos, que recibirá el empleado y que no afecta de forma negativa a su asistencia si registra menos tiempo del necesario en su horario laboral. Cuando un empleado registra su salida y el tiempo total registrado durante el día es menor que las horas laborales especificadas y menor que el plazo especificado, **no** se le penalizará por sus horas reducidas.
        
         Example
        
        Una empresa establece ambos campos de tolerancia con `15` minutos y las horas laborales de todos los empleados están configuradas de 9:00 AM a 5:00 PM.
        
        Si un empleado registra su entrada a las 9:00 AM y se retira a las 5:14 PM, los 14 minutos adicionales **no** se toman en cuenta para sus horas adicionales.
        
        Si un empleado registra su entrada a las 9:05 AM y se retira a las 4:55 PM, **no** se le penalizará por este desajuste aunque haya registrado 10 minutos menos de los correspondientes a su jornada laboral completa.
        
    - Mostrar horas extra: seleccione esta casilla para mostrar las horas adicionales registradas por un empleado cuando registra su salida en un quiosco o cuando un usuario registra su salida en la base de datos.
        

 Nota

Los empleados pueden registrar horas adicionales incluso si la opción Número de horas adicionales no está activada. La diferencia es que cuando la opción anterior está habilitada, es posible [restarlas de una solicitud de tiempo personal aprobada](https://www.odoo.com/documentation/17.0/es/applications/hr/time_off.html#time-off-deduct-extra-hours).

## Información general[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#overview "Enlazar permanentemente con este título")

Al entrar a la aplicación _Asistencias_ aparece el tablero de Información general con toda la información de entrada y salida del usuario que inició sesión. Si el usuario tiene [permisos de acceso](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#attendances-access-rights) específicos o es [aprobador](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#attendances-approvers) de otros empleados, entonces la información adicional de entrada y salida de esos empleados también aparecerá en el tablero Información general.

### Vistas[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#views "Enlazar permanentemente con este título")

Para cambiar la vista desde el gráfico de Gantt predeterminado a una vista de lista, haga clic en el icono Lista ubicado en la esquina superior derecha del tablero, abajo de la foto del usuario. Para volver al gráfico de Gantt, haga clic en el botón Gantt que está ubicado junto al botón Lista.

La vista predeterminada proporciona la información del día actual. Para que aparezca la información de la semana, mes o año, haga clic en el botón Día para abrir el menú desplegable que muestra esas otras opciones. Seleccione la vista deseada, después el tablero se actualizará y aparecerá la información seleccionada. Para cambiar el día, semana, mes o año que aparecen, haga clic en los botones ← (flecha izquierda) o → (flecha derecha) ubicados a cada lado del menú desplegable. Para regresar a una vista que incluya el día actual haga clic en el botón Hoy, esa acción actualizará el tablero y aparecerá la información que incluye la información del día en curso.

En la vista de Día, la columna correspondiente a la hora actual aparece en amarillo. Si selecciona la vista de Semana o Mes, la columna resaltada es la que corresponde al día actual. Si selecciona la vista de Año, se resalta el mes actual.

![El tablero de información general con la información de la semana, con el día actual destacado.](https://www.odoo.com/documentation/17.0/es/_images/overview.png)

Cualquier entrada que tenga errores aparecerá en rojo, lo que indica que es necesario que un usuario con los [permisos de acceso](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#attendances-access-rights) adecuados o que sea [aprobador](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#attendances-approvers) de los empleados con los errores los resuelva.

### Filtros y grupos[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#filters-and-groups "Enlazar permanentemente con este título")

Para filtrar los resultados en el tablero de información general, o para visualizar distintos grupos de información, haga clic en el botón 🔻 (triángulo desplegable) ubicado del lado derecho de la barra de búsqueda sobre el tablero. Seleccione una de las opciones disponibles de Filtros o Agrupar por. Hay varios filtros y grupos preconfigurados para elegir, así como una opción para crear filtros personalizados.

#### Filtros[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#filters "Enlazar permanentemente con este título")

Los filtros predeterminados que puede seleccionar son los siguientes:

- Mis asistencias: este filtro solo muestra los datos de asistencia del usuario.
    
- Mi equipo: este filtro muestra los datos de asistencia del equipo del usuario.
    
- En el trabajo: este filtro muestra los datos de asistencia de todas las personas que tienen su entrada registrada.
    
- Errores: este filtro muestra todas las entradas con [errores](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#attendances-errors) que deben resolverse.
    
- Entrada: este filtro tiene un menú desplegable para seleccionar un periodo específico. Seleccione uno de los periodos que aparecen en las opciones, un mes, trimestre o año específico.
    
- Últimos 7 días: este filtro muestra los datos de asistencia de los últimos siete días.
    
- Agregar filtro personalizado: cree un filtro personalizado con la ventana emergente que aparece al seleccionar esa opción.
    

#### Grupos[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#groups "Enlazar permanentemente con este título")

Los grupos predeterminados que puede seleccionar son los siguientes:

- Entrada: este grupo presenta un menú desplegable que incluye las opciones Año, Trimestre, Mes, Semana y Día. Seleccione el periodo para visualizar toda la información de entrada agrupada por el plazo seleccionado.
    
- Empleado: este grupo muestra los datos de asistencia organizados por empleado.
    
- Salida: este grupo presenta un menú desplegable que incluye las opciones Año, Trimestre, Mes, Semana y Día. Seleccione el periodo para visualizar toda la información de salida agrupada por el plazo seleccionado.
    
- Agregar grupo personalizado: esta opción muestra un menú desplegable con varias opciones para agrupar los datos de asistencia. Algunas de ellas son Ciudad, País, Modo y Dirección IP.
    

### Detalles del registro de asistencia[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#attendance-log-details "Enlazar permanentemente con este título")

Odoo almacena varios detalles relacionados con la hora y la ubicación cuando un usuario registra su entrada y su salida. Los detalles específicos proporcionados están determinados por el método que el usuario utilizó para realizar sus registros.

Para consultar los detalles específicos de la entrada y salida de un empleado, haga clic en una entrada en el tablero de información general.

Esta acción abrirá una ventana emergente con el registro detallado de las asistencias del usuario. Para cerrarlo, haga clic en el botón Guardar y cerrar ubicado en la esquina inferior izquierda del formulario.

El registro detallado de asistencia incluye la siguiente información:

#### Detalles principales[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#main-details "Enlazar permanentemente con este título")

- Empleado: el nombre del empleado.
    
- Entrada: la fecha y hora en que el empleado registró su entrada.
    
- Salida: la fecha y hora en que el empleado se retiró. Esta información solo aparece si el empleado ya registró su salida.
    
- Horas trabajadas: el tiempo total que el empleado registró en el día en un formato de horas y minutos (HH:MM). Este valor calcula todas las entradas y salidas del día en caso de que el empleado haya registrado estos datos más de una vez.
    
- Horas adicionales: las horas extra que el empleado haya registrado que excedan sus horas de trabajo esperadas.
    

#### Detalles de entrada y salida[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#check-in-check-out-details "Enlazar permanentemente con este título")

La siguiente información aparece en la sección de Entrada y en la de Salida.

- Modo: el método con el que se recopiló la información de asistencia. Systray aparece si el empleado registró su entrada y salida [desde la base de datos](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/check_in_check_out.html#attendances-check-in) y Manual si el empleado las registró [con un quiosco de asistencias](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-kiosk-mode-entry).
    
- Dirección IP: la dirección IP de la computadora o dispositivo que el empleado utilizó para registrar su entrada o salida.
    
- Navegador: el navegador web que el empleado utilizó para registrar su entrada o salida.
    
- Localización: la ciudad y el país asociados con la dirección IP del dispositivo.
    
- Coordenadas del GPS: las coordenadas específicas cuando el usuario registró su entrada o salida. Para ver las coordenadas específicas en un mapa, haga clic en el botón → Ver en Mapas ubicado abajo de Coordenadas del GPS. Esto abre un mapa en una nueva pestaña del navegador, con la ubicación específica señalada.
    

![La información detallada de una entrada de asistencia.](https://www.odoo.com/documentation/17.0/es/_images/details.png)

### Errores[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#errors "Enlazar permanentemente con este título")

Las entradas que tienen algún error aparecen en el tablero de información general en rojo. En la vista de Gantt, la entrada aparece con un fondo de color rojo. Si se encuentra en la vista de lista, el texto de la entrada aparecerá en rojo.

Por lo general, ocurre un error cuando un empleado registró su entrada pero no su salida en las últimas 24 horas o cuando un empleado tiene un periodo de registro de entrada y salida que dura más de 16 horas.

Para solucionar el error es necesario modificar o eliminar la entrada de asistencia. Haga clic en la entrada para abrir una ventana emergente con los detalles de esa entrada en específico. Para modificar la información de Entrada o Salida, haga clic en el campo Entrada o Salida y aparecerá un selector de calendario. Haga clic en la fecha deseada y después use el selector de hora ubicado abajo del calendario para seleccionar la hora específica de la entrada. Haga clic en Aplicar cuando la información sea correcta.

![La ventana emergente que permite modificar una entrada de asistencia con un error. Visualización del selector de calendario, el selector de hora aparece en un recuadro rojo.](https://www.odoo.com/documentation/17.0/es/_images/errors.png)

Cuando toda la información en la ventana emergente es correcta, haga clic en Guardar y cerrar. La entrada aparecerá en color gris en lugar de rojo cuando ya no tenga errores.

Para eliminar una entrada, haga clic en Eliminar en la ventana emergente en lugar de realizar modificaciones.

## Reportes[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#reporting "Enlazar permanentemente con este título")

Haga clic en la sección Reporte ubicada en el menú superior para visualizar los reportes de asistencia. El reporte predeterminado muestra la información de asistencia de cada empleado durante los últimos 3 meses en un gráfico de línea.

La vista predeterminada es un gráfico. Para consultar los datos en una tabla dinámica, haga clic en el botón Tabla dinámica ubicado en la esquina superior derecha del reporte. Para volver a la vista de gráfico, haga clic en el botón Gráfico que se encuentra junto al botón Tabla dinámica.

Para visualizar otra información, ajuste los [filtros y grupos](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#attendances-filters-groups) de la misma manera que en el tablero de Información general.

Los datos pueden visualizarse en un gráfico de barras, gráfico de línea, gráfico circular, gráfico apilado o en orden descendente o ascendente. Haga clic en el botón correspondiente para cambiar la vista a cualquiera de estos gráficos, se encuentran arriba del gráfico.

Para cambiar las medidas, haga clic en el botón Medidas y seleccione una con el menú desplegable.

También es posible insertar el reporte en una hoja de cálculo. Haga clic en el botón Insertar en hoja de cálculo, aparecerá una ventana emergente, allí seleccione la hoja de cálculo deseada y haga clic en Confirmar.

![La vista de reporte predeterminada, todos los botones de vista opcionales aparecen dentro de un recuadro rojo.](https://www.odoo.com/documentation/17.0/es/_images/reporting.png)

 Ver también

- [Registrar salidas y entradas](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/check_in_check_out.html)
    
- [Kiosks](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html)
    
- [Hardware](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/hardware.html)