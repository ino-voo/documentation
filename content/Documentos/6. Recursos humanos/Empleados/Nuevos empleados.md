Cuando contrata a un nuevo empleado, lo primero que debe hacer es crear un nuevo registro de empleado. Este registro está centralizado y almacena toda la información importante sobre el empleado, como su [información general](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#employees-general-info), [historial laboral y habilidades](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#employees-resume), [otra información laboral](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#employees-work-info-tab), [detalles personales](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#employees-private-info), [documentos](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#employees-docs) y más.

Abra la aplicación Empleados y haga clic en el botón Nuevo que se encuentra en la esquina superior izquierda. Esta acción abrirá un formulario de empleado vacío.

Complete toda la información necesaria y cualquier detalle adicional en caso de ser necesario.

![Un formulario para el nuevo empleado con todos los campos completados.](https://www.odoo.com/documentation/17.0/es/_images/new-employee-form.png)

 Nota

El número de teléfono y el nombre de la empresa actual se completan en los campos Teléfono de trabajo y Empresa. Si la aplicación _Evaluación_ está instalada, el campo Fecha de la próxima evaluación se completa con una fecha que corresponda a seis meses a partir de la fecha actual.

## Información general[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#general-information "Enlazar permanentemente con este título")

El formulario de empleado guarda la información de forma automática a medida de que la va proporcionando. Sin embargo, también puede guardarla de forma manual en cualquier momento si hace clic en Guardar de forma manual. Este botón está representado con un icono (nube con una flecha hacia arriba).

### Campos necesarios[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#required-fields "Enlazar permanentemente con este título")

- Nombre del empleado: escriba el nombre del empleado.
    
- Empresa: con el menú desplegable en este campo, seleccione la empresa que contrató al nuevo empleado o cree una nueva empresa. Escriba el nombre en el campo y haga clic en Crear o en Crear y editar… desde el mini menú desplegable que aparece.
    

![Un formulario para el nuevo empleado con todos los campos obligatorios en un recuadro rojo.](https://www.odoo.com/documentation/17.0/es/_images/employee-new.png)

### Campos opcionales[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#optional-fields "Enlazar permanentemente con este título")

- Fotografía: haga clic en el icono editar ✏️ (lápiz) ubicado en el cuadro de la parte superior derecha del formulario del empleado para seleccionar la fotografía correspondiente.
    
- Puesto de trabajo: escriba el título del puesto de trabajo del empleado debajo de su nombre o selecciónelo del menú desplegable del campo Puesto de trabajo para que el campo de arriba se complete en automático. Puede modificar el campo debajo del nombre del empleado y _no_ es necesario que coincida con la selección que realizó en el menú desplegable del campo anterior.
    
     Example
    
    Es recomendable que los puestos de trabajo coincidan, pero la descripción que escriba en el campo superior puede incluir información más específica que la opción seleccionada en el menú desplegable Puesto de trabajo si así lo desea.
    
    Por ejemplo, si contrata a alguien para el puesto configurado como Representante de ventas en la aplicación _Reclutamiento_, podrá seleccionar eso en el campo desplegable Puesto de trabajo.
    
    El puesto podría ser más específico en el campo Puesto de trabajo que se ubica debajo del campo Nombre del empleado, por ejemplo `Representante de ventas - Suscripciones` si el empleado solo se encarga de la venta de suscripciones.
    
    ![Los dos campos de puesto de trabajo tienen información pero es distinta.](https://www.odoo.com/documentation/17.0/es/_images/job-description-fields.png)
    
- Etiquetas: seleccione una etiqueta del menú desplegable para agregar etiquetas que correspondan al empleado. Puede crear cualquier etiqueta si la escribe en este campo. Una vez creada, está disponible para todos los registros de empleado y puede agregar tantas como sea necesario.
    
- Información de contacto del trabajo: escriba el teléfono celular laboral, teléfono laboral, correo electrónico laboral y el nombre de la empresa del empleado en caso de que no se haya completado de forma automática.
    
- Departamento: seleccione el departamento del empleado en el menú desplegable.
    
- Puesto de trabajo: seleccione el puesto de trabajo del empleado desde el menú desplegable, después el campo Puesto de trabajo debajo del nombre del empleado se actualizará en automático para reflejar el puesto de trabajo que seleccionó. Estos puestos provienen de la aplicación [Reclutamiento](https://www.odoo.com/documentation/17.0/es/applications/hr/recruitment/new_job.html) y están relacionados con los puestos de trabajo configurados en ese momento.
    
- Gerente: seleccione al gerente del empleado en el menú desplegable.
    
- Instructor: seleccione al instructor del empleado en el menú desplegable.
    
- Fecha de la próxima evaluación: este campo **solo** es visible si la aplicación _Evaluación_ está instalada. La fecha se completa en automático con una fecha que se calcula según la configuración en la aplicación _Evaluación_. La fecha se puede modificar con el selector de calendario.
    

 Nota

Si después de seleccionar un gerente el campo instructor está vacío, entonces este instructor también se asignará como instructor.

 Truco

Para editar el departamento, gerente, instructor o empresa que seleccionó, haga clic en la flecha de enlace interno ubicada junto al campo correspondiente. Este botón abrirá el formulario seleccionado y podrá realizar modificaciones. Haga clic en Guardar para aplicar los cambios.

## Pestañas de información adicional[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#additional-information-tabs "Enlazar permanentemente con este título")

### Pestaña de currículo[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#resume-tab "Enlazar permanentemente con este título")

#### Currículum[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#resume "Enlazar permanentemente con este título")

Después ingrese la experiencia laboral del empleado en la pestaña Currículum, debe llenar cada línea de manera individual. Al crear una entrada por primera vez, haga clic en Crear una nueva entrada y aparecerá el formulario Crear líneas de currículum. Luego de agregar una entrada, el botón Crear una nueva entrada se reemplaza con el botón Agregar. Proporcione la siguiente información para cada entrada.

![Un formulario de currículum con toda la información completa.](https://www.odoo.com/documentation/17.0/es/_images/resume-lines.png)

- Título: escriba el título de la experiencia laboral anterior.
    
- Empleado: seleccione al empleado en el menú desplegable.
    
- Tipo: desde el menú desplegable seleccione Experiencia, Educación, Proyectos secundarios, Certificación interna, Completó la capacitación interna o escriba una nueva entrada y luego haga clic en Crear «(tipo)».
    
- Tipo de visualización: con el menú desplegable elija Clásico para una experiencia laboral típica, Certificación si se trata de una experiencia obtenida mediante una certificación o Curso en caso de que hayan sido clases no certificadas.
    
- Duración: proporcione las fechas de inicio y fin de la experiencia laboral. Para seleccionar una fecha, haga clic en el primer campo vacío para abrir el calendario emergente. Con los iconos < (flecha izquierda) y > (flecha derecha) podrá desplazarse al mes deseado, después haga clic en el día para seleccionarlo. Repita este proceso para buscar y seleccionar la fecha de finalización. Después de que haya seleccionado las fechas deseadas, haga clic en ✔️ Aplicar.
    
- Descripción: escriba cualquier detalle relevante en este campo.
    

Una vez que haya escrito toda la información, haga clic en el botón Guardar y cerrar si solo agregará una sola entrada, o haga clic en el botón Guardar y crear nuevo para guardar la entrada actual y crear otra línea del currículum.

 Nota

Una vez que guarda el formulario del nuevo empleado, el puesto y la empresa actual se agregan de forma automática a la pestaña Currículum con la fecha de finalización como `actual`.

#### Habilidades[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#skills "Enlazar permanentemente con este título")

Puede agregar las habilidades de un empleado a la pestaña Currículum de la misma forma en la que crea una línea de currículum.

Para agregar una habilidad al registro de un empleado, primero es necesario configurar los tipos de habilidades. Si no los ha configurado, aparecerá el botón Crear nuevas habilidades en la sección de Habilidades de la pestaña Currículum. [Configure los tipos de habilidades](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#employees-skill-types) antes de agregar habilidades al registro del empleado.

El botón Elija una habilidad de la lista aparecerá si los tipos de habilidades están configurados. Haga clic en el botón Elija una habilidad de la lista y seleccione la siguiente información para cada habilidad.

![Un formulario de habilidades con la información completada.](https://www.odoo.com/documentation/17.0/es/_images/select-skills.png)

- Tipo de habilidad: seleccione un [tipo de habilidad](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#employees-skill-types). Haga clic en el botón de opción ubicado junto al tipo de habilidad.
    
- Habilidad: luego de seleccionar un Tipo de habilidad, las habilidades correspondientes relacionadas con el tipo de habilidad seleccionado aparecen en un menú desplegable. Por ejemplo, al seleccionar Idioma aparecen varias opciones de idiomas para seleccionar en el campo Habilidades. Elija la habilidad preconfigurada correspondiente o escriba una nueva y luego haga clic en Crear «(nueva habilidad)».
    
- Nivel de habilidad: son los niveles de habilidad predefinidos asociados con el Tipo de habilidad seleccionado que aparecen en el menú desplegable. Seleccione un nivel de habilidad y la barra de progreso mostrará de manera automática el progreso predefinido para ese nivel de habilidad. Los niveles y el progreso se pueden modificar en el formulario de Nivel de habilidad, al que puede acceder desde la flecha de Vinculo interno ubicada junto al campo Nivel de habilidad.
    

Haga clic en el botón Guardar y cerrar si solo agregará una actividad o en Guardar y crear nuevo para guardar la entrada actual y agregar otra habilidad de inmediato.

Para eliminar cualquier línea de la pestaña Currículo, haga clic en el icono 🗑️ (papelera) para eliminar la entrada. Para agregar una nueva línea, haga clic en el botón Agregar junto a la sección correspondiente.

 Importante

Solo los usuarios con permisos de Encargado: gestionar a todos los empleados o de Administrador en la aplicación _Empleados_ pueden agregar o editar habilidades.

##### Tipos de habilidad[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#skill-types "Enlazar permanentemente con este título")

Para agregar una habilidad al formulario de un empleado, primero debe configurar los Tipos de habilidad. Vaya a Empleados ‣ Configuración ‣ Empleados: Tipos de habilidad para ver los que están configurados y crear nuevos tipos de habilidades.

 Nota

La habilidad predeterminada de Idiomas ya está configurada como un _tipo_ de habilidad, pero no hay _habilidades_ específicas de idiomas en ese tipo de habilidad. Debe terminar de configurar el tipo de habilidad Idiomas antes de utilizarlo.

Haga clic en Nuevo para abrir un formulario de tipo de habilidad y ahí complete todos los detalles relacionados con el nuevo tipo de habilidad. Repita este procedimiento para todos los tipos de habilidad necesarios.

- Tipo de habilidad: escriba el nombre del tipo de habilidad. Funcionará como la categoría principal para las habilidades más específicas, así que el nombre debe ser genérico.
    
- Habilidades: haga clic en Agregar una línea y escriba el nombre de esta nueva habilidad. Repita el proceso para todas las habilidades necesarias.
    
- Niveles: haga clic en Agregar una línea, y escriba el nombre del nivel. Después, haga clic en el campo Progreso y escriba un porcentaje (0-100) para ese nivel. Repita el proceso para todos los niveles adicionales según sea necesario.
    
- Nivel predeterminado: haga clic en el botón ubicado en la línea de nivel para establecer ese nivel como el predeterminado. Por lo general, el nivel más bajo se establece como predeterminado, pero puede elegir cualquier otro. Cuando el botón aparece de color verde indica que es el nivel predeterminado para la habilidad. Solo puede establecer un nivel como predeterminado.
    
     Example
    
    Escriba `Matemáticas` en el campo Nombre para agregar un conjunto de habilidades matemáticas. En el campo Habilidades, escriba `Álgebra`, `Cálculo` y `Trigonometría`. Después, en el campo Niveles, escriba `Principiante`, `Intermedio` y `Experto`, en sus respectivos Progresos escriba `25`, `50` y `100`. Por último, haga clic en Establecer predeterminado de la línea de `Principiante` para establecer este nivel como predeterminado.
    
    ![Un formulario de habilidad para un tipo de habilidad matemática con toda la información completada.](https://www.odoo.com/documentation/17.0/es/_images/math-skills.png)
    

El formulario de tipo de actividad guarda la información de forma automática conforme la va proporcionando.

 Truco

Una vez que haya terminado de completar el formulario, haga clic en el botón Guardar de forma manual, es el icono de nube con una flecha hacia arriba ubicado en la parte superior de la pantalla. Los niveles se reorganizarán en orden descendente, con el nivel más alto en la parte superior y el más bajo en la parte inferior, sin importar el nivel predeterminado y el orden en que se ingresaron.

### Pestaña de información del trabajo[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#work-information-tab "Enlazar permanentemente con este título")

La pestaña Información de trabajo almacena la información del empleado relacionada específicamente con su trabajo. Aquí aparecerá su horario de trabajo, sus funciones, quién aprueba sus solicitudes en específico (tiempo personal, hojas de horas y gastos), los días que trabaja de forma remota y otros detalles de su ubicación específica de trabajo.

Haga clic en la pestaña Información de trabajo para acceder a esta sección. Proporcione la siguiente información para el nuevo empleado:

- Ubicación: seleccione la Dirección laboral con el menú desplegable. Para modificar la dirección, coloque el cursor sobre la primera línea (en caso de que haya varias) de la dirección para que aparezca la flecha de :guilabel:[`](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#id1)Enlace interno y haga clic en ella para abrir el formulario de la empresa y realizar cualquier modificación necesaria.
    
    Utilice las migas de pan para regresar al formulario del nuevo empleado cuando haya terminado.
    
    Si necesita usar una nueva dirección laboral escríbala en el campo y después haga clic en Crear (nueva dirección) para agregar la dirección o en Crear y editar… para agregarla y editar el formulario de dirección.
    
- Aprobadores: para ver esta sección, el usuario debe tener permisos de Administrador o Encargado: gestionar a todos los empleados configurados en la aplicación _Empleados_. Utilice los menús desplegables para seleccionar los usuarios responsables de aprobar un gasto, una solicitud de tiempo personal, entradas de hojas de horas y registros de asistencia del empleado.
    
    Coloque el cursor sobre cualquiera de las opciones para que aparezca la flecha Enlace interno.
    
    Haga clic en la flecha de Enlace interno para abrir un formulario con los campos Nombre, Dirección de correo electrónico, Empresa, Teléfono, Celular y Almacén predeterminado del aprobador. Puede modificar estos campos en caso de que sea necesario.
    
    Utilice las migas de pan para regresar al formulario del nuevo empleado cuando haya terminado.
    
     Importante
    
    Los usuarios que aparecen en el menú desplegable de la sección Aprobadores **deben** tener permisos de _administrador_ configurados para la función correspondiente de recursos humanos.
    
    Para verificar quién tiene estos permisos, vaya a Ajustes ‣ Usuarios ‣ → Administrar usuarios. Haga clic en un empleado y consulte la sección Recursos humanos de la pestaña Permisos de acceso.
    
    - Para que el usuario aparezca como aprobador en los gastos **debe** tener configurada la opción Responsable de aprobar en el equipo, Aprobador total o Administrador en la función de Gastos.
        
    - Para que el usuario aparezca como aprobador del tiempo personal **debe** tener configurada la opción Encargado: gestione todas las solicitudes o Administrador en la función de Tiempo personal.
        
    - Para que el usuario aparezca como aprobador de las hojas de horas **debe** tener configurada la opción Gerente, Encargado: gestionar todos los contratos o Administrador en la función de Nómina.
        
    
- Trabajo remoto: utilice el menú desplegable para seleccionar la ubicación predeterminada en la que el empleado trabaja cada día de la semana. Las opciones predeterminadas son Casa, Oficina y Otro.
    
    Puede escribir una nueva ubicación campo. Después haga clic en Crear (nueva ubicación) para agregarla o en Crear y editar… para agregarla y editar su formulario.
    
    Haga clic en clic Guardar y cerrar después de que haya hecho las modificaciones. La ubicación se almacenará y completará el campo.
    
    Deje el campo vacío (Sin especificar) de los días no laborables, como sábado y domingo.
    
     Nota
    
    También puede agregar o modificar las ubicaciones de trabajo desde la aplicación Empleados ‣ Configuración ‣ Empleado: Ubicaciones de trabajo. Para modificar una, haga clic en una que ya exista y realice los cambios necesarios en el formulario.
    
    Haga clic en Nuevo para crear una nueva ubicación, luego escriba los detalles correspondientes en el formulario. Todos los campos son **obligatorios**.
    
    - Ubicación de trabajo: escriba el nombre de la ubicación, puede ser tan general o tan específico como sea necesario, por ejemplo, `Casa` o `Edificio 1, segundo piso`.
        
    - Dirección laboral: seleccione la dirección de la ubicación con el menú desplegable.
        
    - Imagen de portada: haga clic en el icono para seleccionarlo como imagen de portada. Las opciones son el icono de casa, de edificio de oficinas y un marcador de ubicación GPS.
        
    - Empresa: seleccione la empresa a la que pertenece esta ubicación con el menú desplegable. La empresa actual completa este campo de forma predeterminada.
        
    
    ![Un formulario para la nueva ubicación de trabajo con todos los campos completados.](https://www.odoo.com/documentation/17.0/es/_images/location.png)
    
- Horario: seleccione las horas laborales y la zona horaria del empleado. La flecha de Enlace interno abre una vista detallada de las horas laborales específicas diarias, aquí podrá modificar o eliminarlas.
    
     Nota
    
    Las horas laborables están relacionadas al horario en el que opera la empresa. Las horas laborables de un empleado **no** pueden estar fuera del horario de la empresa.
    
    Cada empresa tiene sus propio horario laboral, así que para las bases de datos de varias empresas, cada empresa debe tener sus horas laborables.
    
    Si las horas laborales de un empleado no están configuradas como parte del horario laboral de la empresa, puede agregar nuevos horarios laborales o modificar los que ya existen.
    
    Las horas laborables se pueden modificar desde la aplicación _Nómina_, allí reciben el nombre de Horarios de trabajo.
    
    Consulte la documentación de [Nómina](https://www.odoo.com/documentation/17.0/es/applications/hr/payroll.html) para obtener más información sobre cómo crear o modificar horarios de trabajo en la aplicación _Nómina_.
    
- Planeación: seleccione una función del menú desplegable para los campos Función y Función predeterminada. Si selecciona la función predeterminada como una función, esta se agrega en automático a la lista de funciones.
    

 Importante

Los usuarios que aparecen en el menú desplegable de la sección Aprobadores **deben** tener permisos de _administrador_ configurados para la función correspondiente de recursos humanos.

Para verificar quién tiene estos permisos, vaya a Ajustes ‣ Usuarios ‣ → Administrar usuarios. Haga clic en un empleado y consulte la sección Recursos humanos de la pestaña Permisos de acceso.

- Para que el usuario aparezca como aprobador en los gastos **debe** tener configurada la opción Responsable de aprobar en el equipo, Aprobador total o Administrador en la función de Gastos.
    
- Para que el usuario aparezca como aprobador del tiempo personal **debe** tener configurada la opción Encargado o Administrador en la función de Tiempo personal.
    
- Para que el usuario aparezca como aprobador de las hojas de horas **debe** tener configurada la opción Gerente, Encargado o Administrador en la función de Nómina.
    

 Nota

Las horas laborables están relacionadas al horario en el que opera una empresa. Las horas laborables de un empleado **no** pueden estar fuera del horario de la empresa.

Cada empresa tiene sus propio horario laboral, así que para las bases de datos de varias empresas, cada empresa **debe** tener sus horas laborables.

Si las horas laborables de un empleado no están configuradas como parte del horario laboral de la empresa, puede agregar nuevas horas laborables o modificar las que ya existen.

Para agregar o modificar las horas laborables vaya a Nómina ‣ Configuración ‣ Horarios de trabajo. Podrá agregar un nuevo horario si hace clic en Nuevo o editar uno si selecciona las horas laborables de la lista para modificarlas.

Consulte la sección de [horarios de trabajo](https://www.odoo.com/documentation/17.0/es/applications/hr/payroll.html#payroll-working-times) en la documentación de Nómina para obtener detalles específicos sobre su creación y edición.

Después de crear el nuevo horario de trabajo o modificar uno existente, podrá configurar las horas laborables en el formulario del empleado. En la sección Horario de la pestaña Información de trabajo deberá seleccionar las horas del empleado con el menú desplegable.

### Pestaña de información privada[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#private-information-tab "Enlazar permanentemente con este título")

No es necesario que complete los datos de la pestaña Información privada para crear un empleado. Sin embargo, es posible que algunos sean importantes para el departamento de nóminas de la empresa. Con el fin de procesar los recibos de nómina de forma correcta y garantizar que se contabilizan todas las deducciones, debe proporcionar la información personal del empleado.

Aquí puede proporcionar la información relacionada con el contacto privado, estado familiar, contacto de emergencia, educación, permiso de trabajo y ciudadanía del empleado. Puede completar los campos mediante el menú desplegable, al hacer clic en una casilla, o si escribe la información.

- Contacto privado: escriba la dirección particular, el correo electrónico y el teléfono del empleado. Después, proporcione el número de cuenta bancaria del empleado con el menú desplegable.
    
    Si el banco aún no está configurado (es una situación común al crear un nuevo empleado), ingrese el número de cuenta bancaria y haga clic en Crear y editar…. Esto abrirá el formulario Crear número de cuenta bancaria, allí complete la información necesaria y después haga clic en Guardar y cerrar.
    
    Después, seleccione el idioma preferido del empleado con el menú desplegable y escriba la Distancia de la casa al trabajo en el campo correspondiente. Este último campo solo es necesario si el empleado recibe algún tipo de prestación relacionada con transportación.
    
    Por último, escriba la información relacionada con la matrícula del empleado en el campo Placa del vehículo privado.
    
- Estado familiar: seleccione el estado civil con el menú desplegable, puede elegir entre soltero, casado, cohabitante legal, viudo o divorciado. Si el empleado tiene hijos, ingrese el número de hijos dependientes en el campo correspondiente.
    
- Emergencia: escriba el nombre de contacto y el teléfono de contacto de la persona de contacto de emergencia del empleado en los campos correspondientes.
    
- Educación: seleccione el nivel más alto de educación que completó el empleado en el menú desplegable Nivel de certificado. Las opciones predeterminadas incluyen Egresado, Licenciatura, Maestría, Doctor y Otro.
    
    Escriba el campo de estudio y el nombre de la escuela en los campos correspondientes.
    
- Permiso de trabajo: si el empleado cuenta con un permiso de trabajo, ingrese la información en esta sección. Escriba el Número de visa y el Número de permiso de trabajo en los campos correspondientes.
    
    Seleccione la Fecha de vencimiento de la visa y la Fecha de vencimiento del permiso de trabajo con el selector de calendario.
    
    Suba una copia digital del documento Permiso de trabajo en caso de que lo tenga disponible. Haga clic en Suba su archivo, busque el archivo correspondiente en el explorador de archivos y haga clic en Abrir.
    
- Ciudadanía: esta sección incluye toda la información relevante sobre la ciudadanía del empleado. Algunos campos utilizan un menú desplegable, como los campos Nacionalidad (País), Género y País de nacimiento.
    
    La fecha de nacimiento utiliza un selector de calendario para elegir la fecha. Primero haga clic en el nombre del mes y luego en el año para acceder a los rangos de años. Use los iconos < (izquierda) y > (derecha) para ir al rango de años correcto y haga clic en uno. Haga clic en el mes y después en el día para seleccionar la fecha.
    
    Escriba la información correcta en los campos Número de identificación, Número de pasaporte y Lugar de nacimiento.
    
    Por último, si el empleado **no** es residente del país en el que labora, seleccione la casilla junto al campo No es residente.
    
     Nota
    
    Los campos disponibles aparecen según la localización instalada. Por ejemplo, para Estados Unidos aparece el campo Número de seguro social (SSN).
    

### Pestaña de ajustes de RR. HH.[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#hr-settings-tab "Enlazar permanentemente con este título")

Esta pestaña proporciona varios campos que se completan con información que varía según el país donde se encuentre la empresa. Se configuran diferentes campos dependiendo de la ubicación, sin embargo, puede que algunas secciones sigan apareciendo.

- Estado: seleccione un Tipo de empleado y, si es necesario, un usuario relacionado, con los menús desplegables. Las opciones de tipo de rmpleado incluyen Empleado, Estudiante, Aprendiz, Contratista o Trabajador independiente.
    
     Importante
    
    **No** es necesario que los empleados sean usuarios. Los _empleados_ **no** cuentan para la facturación de la suscripción de Odoo, pero los _usuarios_ **sí**. Si el nuevo empleado también debe ser un usuario, **debe** crearlo.
    
    Después de crear al empleado, haga clic en el icono ⚙️ (engranaje) y después en Crear usuario. Esta acción abrirá el formulario Crear usuario.
    
    Escriba el nombre y la dirección de correo electrónico, seleccione la empresa con el menú desplegable.
    
    Después, escriba los números de teléfono y celular en sus respectivos campos.
    
    En caso de que haya una fotografía disponible, haga clic en el icono Editar (representado con el icono ✏️ (lápiz)) ubicado en la esquina inferior izquierda de la caja de imagen, esa se encuentra en la esquina superior derecha del formulario.
    
    Aparecerá un explorador de archivos, busque el archivo y haga clic en Abrir para seleccionarlo. Por último, haga clic en Guardar después de agregar toda la información. El registro del empleado se actualizará en automático con el usuario que acaba de crear y completará el campo Usuario relacionado.
    
    Los usuarios también se pueden crear de forma manual. Para obtener más información sobre cómo agregar un usuario, consulte [Usuarios](https://www.odoo.com/documentation/17.0/es/applications/general/users.html).
    
- Asistencia/Punto de venta/Fabricación: aquí puede escribir el Código NIP y la ID de credencial del empleado, si el empleado los necesita o tiene. Haga clic en Generar junto a la ID de credencial para crear una.
    
    El Código NIP se utiliza para registrar salida y entrada en el quiosco de la aplicación _Asistencia_, así como en el sistema de PdV.
    
- Nómina: si corresponde, escriba el Número de registro del empleado en esta sección.
    
    Los otros elementos que aparecen en este campo, así como otras secciones, varían según la ubicación y la localización que tenga instalada. Le recomendamos que consulte a los departamentos de nómina y contabilidad para asegurarse de que esta sección así como cualquier otra que pueda aparecer, y esté relacionada con la nómina, estén completas de forma adecuada.
    
- Ajustes de la aplicación: escriba el Objetivo de tiempo facturado del empleado para la tabla de clasificación de la aplicación _Hoja de horas_. Después, escriba el Costo por hora en formato XX.XX, se tomará en cuenta cuando el empleado trabaje en un [centro de trabajo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/advanced_configuration/using_work_centers.html).
    
    Escriba en número de la Tarjeta de movilidad de flota en caso de que sea necesario.
    

 Nota

Los costos de fabricación se suman a los costos de producción de un producto si el valor del producto fabricado **no** es un importe fijo. Este costo **no** influye en la aplicación _Nómina_.

![Escriba toda la información del empleado que se le solicita en la pestaña Ajustes de RR. HH.](https://www.odoo.com/documentation/17.0/es/_images/hr-settings.png)

## Documentos[](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#documents "Enlazar permanentemente con este título")

Todos los documentos relacionados con el empleado se almacenan en la aplicación _Documentos_. El número correspondiente aparece en el botón inteligente Documentos ubicado arriba del registro del empleado. Haga clic en el botón inteligente para acceder a todos los documentos.

Consulte la [documentación](https://www.odoo.com/documentation/17.0/es/applications/productivity/documents.html) sobre la aplicación _Documentos_ para obtener más información.

![Todos los documentos que ha subido y están relacionados con el empleado aparecen en el botón inteligente "Documentos".](https://www.odoo.com/documentation/17.0/es/_images/documents.png)