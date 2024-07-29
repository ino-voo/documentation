La aplicación _Recepción_ de Odoo proporciona permite que los visitantes se registren en un edificio o alguna ubicación, al mismo tiempo que la persona a la que visitan recibe un anuncio sobre su llegada. Mientras sus visitantes esperan, también pueden pedir una bebida preconfigurada para que se las lleven.

Esta aplicación es muy útil para las empresas que **no** cuentan con un recepcionista o para aquellas ubicaciones **sin** un área de espera específica disponible para los invitados y visitantes.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk.html#configuration "Enlazar permanentemente con este título")

El primer elemento que debe configurar con la aplicación _Recepción_ es la estación, después podrá configurar las bebidas que ofrecerá de forma opcional.

### Estaciones[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk.html#stations "Enlazar permanentemente con este título")

Las _estaciones_ de la aplicación _Recepción_ de Odoo son como cualquier otra ubicación donde alguien puede registrarse y esperar a un empleado, como una sala de espera o un vestíbulo. Cada estación tiene un quiosco donde los visitantes registran su llegada.

Al configurar la aplicación _Recepción_ **debe** configurar por lo menos una estación, pero puede crear y configurar todas las estaciones que desee.

Para crear una estación, vaya a Recepción ‣ Configuración ‣ Estaciones y haga clic en Nuevo. Esta acción abrirá un formulario vacío de recepción.

Proporcione la siguiente información en el formulario:

- Nombre del lugar de recepción: agregue un nombre para esta ubicación específica de recepción. Debe ser corto para que lo pueda identificar con facilidad, como `Recepción` o `Vestíbulo principal`. Este campo es obligatorio para crear una estación.
    
- Responsables: seleccione a la persona (o las personas, ya que puede elegir a varias) que recibirán una alerta cuando un visitante se registre desde ese lugar de recepción. Este campo es obligatorio para crear una estación.
    
- URL del quiosco: este campo se completa de forma automática después de guardar el formulario con los campos Nombre del lugar de recepción y Responsables. Para guardar de forma manual, haga clic en el icono (nube con flecha hacia arriba) ubicado en la parte superior del formulario.
    
    Después de guardarlo, se genera una URL en el campo URL del quiosco y podrá acceder desde allí.
    
    Para acceder al quiosco, haga clic en el botón Copiar ubicado al final de la URL y vaya a ella con un navegador web. Esta URL abre la página de registro de la recepción de esa estación en específico.
    
     Truco
    
    Para agregar una imagen o fotografía a un formulario de recepción, pase el cursor sobre el icono (cámara con un signo “+”) ubicado en la esquina superior derecha del formulario para que aparezca el icono de ✏️ (lápiz).
    
    Haga clic en el icono ✏️ (lápiz) para abrir el explorador de archivos, busque la imagen o fotografía deseada y después haga clic en Abrir para seleccionarla.
    
    La imagen que haya seleccionado para la estación será la imagen de fondo para su quiosco.
    

#### Pestaña de opciones[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk.html#options-tab "Enlazar permanentemente con este título")

- Selección de anfitrión: si el visitante asiste a una reunión, esta opción le permitirá seleccionar al anfitrión con una lista y la persona seleccionada recibirá una notificación. Si está habilitada aparecerán algunos campos adicionales, como se detalla más adelante.
    
- Autenticar invitado: si necesita que un invitado proporcione información adicional al registrarse deberá habilitar esta opción. Seleccione cuáles campos son obligatorios:
    
    - Correo electrónico: seleccione si la dirección de correo electrónico del invitado es un campo obligatorio, opcional o si la información no es necesaria (Ninguno).
        
    - Teléfono: seleccione si el teléfono del invitado es un campo obligatorio, opcional o si la información no es necesaria (Ninguno).
        
    - Empresa: seleccione si la empresa del invitado es un campo obligatorio, opcional o si la información no es necesaria (Ninguno).
        
- Tema: seleccione el modo de color del quiosco. Elija entre Claro o Oscuro. Claro muestra un fondo gris claro y Oscuro muestra un fondo gris oscuro y negro.
    
- Registro por cuenta propia: seleccione esta opción para mostrar un código QR de registro en el quiosco. Este le permitirá a los invitados registrarse con su celular en lugar del quiosco. Le recomendamos que lo habilite si su quiosco tiene afluencia.
    
- Ofrecer bebidas: seleccione esta opción para ofrecerle bebidas a los invitados al registrarse. Si esta opción está habilitada es necesario que configure las bebidas que ofrecerá con el enlace Configurar bebidas que aparece al activar la función. Después de que haya configurado las bebidas, seleccione las que se ofrecerá con el menú desplegable.
    

 Nota

Las siguientes opciones solo están disponibles en la pestaña Opciones si la opción Selección de anfitrión está habilitada.

- Notificar por correo electrónico: seleccione esta opción para que la persona que el invitado visita reciba un correo cuando se registre. Si está habilitada, abajo aparece el campo Plantilla de correo electrónico con la plantilla predeterminada Plantilla de correo electrónico para recepción seleccionada.
    
    Para cambiar la plantilla de correo electrónico predeterminada, haga clic en el menú desplegable en el campo Plantilla de correo electrónico y luego seleccione otra.
    
    Para modificar la plantilla que está seleccionada haga clic en el icono de Enlace Interno (flecha) ubicado al final de la línea y modifíquela.
    
- Notificar por SMS: seleccione esta opción para que la persona que el invitado visita reciba un mensaje de texto (SMS) cuando se registre. Si está habilitada, abajo aparece el campo Plantilla de correo electrónico con la plantilla predeterminada Plantilla de SMS para recepción seleccionada.
    
    Para cambiar la plantilla de SMS predeterminada, haga clic en el menú desplegable en el campo Plantilla de SMS y luego seleccione otra.
    
    Para modificar la plantilla que está seleccionada haga clic en el icono de Enlace Interno (flecha) ubicado al final de la línea y edite el contenido de la plantilla. El mensaje SMS puede tener máximo de 242 caracteres, así se ajustarán en 4 mensajes SMS (UNICODE).
    
- Notificar por Conversaciones: esta opción está activa de forma predeterminada si habilitó la opción Selección de anfitrión. Esta opción abre una ventana de mensaje de la aplicación _Conversaciones_ con la persona que el invitado visita al registrarse.
    
    La persona que recibe la visita verá un mensaje predeterminado si selecciona esa opción. La aplicación _Conversaciones_ **debe** estar instalada para que esta opción funcione.
    

 Nota

La aplicación _Conversaciones_ se instala de forma predeterminada al crear una base de datos de Odoo y no se toma en cuenta con fines de facturación. La opción Notificar por Conversaciones funcionará siempre y cuando no desinstale _Conversaciones_.

 Example

El formato predeterminado del mensaje de la opción Notificar por Conversaciones es: `(Estación del registro de entrada) tiene un registro: (Nombre del invitado) (Número telefónico del invitado) (Empresa) se reunirá con (Nombre del empleado)`.

Como ejemplo, el mensaje en _Conversaciones_ sería: `Vestíbulo principal tiene un registro: Juan Pérez (123-555-1234) (Odoo, Inc.) se reunirá con Marc Demo`.

![Un formulario de estación de registro de entrada con la información completada.](https://www.odoo.com/documentation/17.0/es/_images/station-form.png)

#### Pestaña de mensaje adicional[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk.html#side-message-tab "Enlazar permanentemente con este título")

Escriba el mensaje que desea que aparezca en el quiosco de la estación después de que un invitado se haya registrado, como un saludo de bienvenida o instrucciones. El texto aparece en la página de confirmación del lado derecho de la pantalla después de completar el proceso de registro.

### Bebidas[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk.html#drinks "Enlazar permanentemente con este título")

Después de crear una estación, el siguiente paso es configurar las bebidas que desea ofrecerle a los visitantes solo si así lo desea. Este paso **no** es necesario para que la aplicación _Recepción_ funcione.

Para agregar una bebida a las opciones, vaya a Recepción ‣ Configuración ‣ Bebidas y haga clic en Nuevo. Esta acción abrirá el formulario de una bebida vacío.

Escriba la siguiente información en el formulario de cada bebida:

- Nombre de la bebida: escriba el nombre de la opción de bebida en este campo. Este campo es obligatorio.
    
- Personas a notificar: con el menú desplegable de este campo seleccione a quién se le notificará cuando elijan esta bebida, puede elegir a varias personas. Este campo es obligatorio.
    
- Secuencia: en este campo deberá escribir un valor numérico para indicar en qué parte de la lista de opciones de bebidas aparece esta opción específica. Entre más pequeño sea el número, la bebida tiene una posición más alta en la lista. Por ejemplo, si escribe el número uno (1), entonces esa bebida se encontraría en la parte superior de la lista y aparecería primero en la secuencia.
    

 Truco

Para agregar una imagen o fotografía a un formulario de bebida, pase el cursor sobre el icono (cámara con un signo “+”) ubicado en la esquina superior derecha del formulario para que aparezca el icono de ✏️ (lápiz).

Haga clic en el icono ✏️ (lápiz) para abrir el explorador de archivos, busque la imagen o fotografía deseada y después haga clic en Abrir para seleccionarla.

La imagen que seleccionó ahora aparece en el campo de imagen y se establece como la imagen de la bebida.

![Un formulario de bebida con la información completa para un café espresso.](https://www.odoo.com/documentation/17.0/es/_images/espresso.png)

## Tablero de la estación[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk.html#station-dashboard "Enlazar permanentemente con este título")

 Truco

Para agregar una imagen o fotografía a un formulario de bebida, pase el cursor sobre el icono (cámara con un signo “+”) ubicado en la esquina superior derecha del formulario para que aparezca el icono de ✏️ (lápiz).

Haga clic en el icono ✏️ (lápiz) para abrir el explorador de archivos, busque la imagen o fotografía deseada y después haga clic en Abrir para seleccionarla.

La imagen que seleccionó ahora aparece en el campo de imagen y se establece como la imagen de la bebida.

## Configuración del quiosco[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk.html#kiosk-setup "Enlazar permanentemente con este título")

Configure cada quiosco para su uso después de configurar las estaciones correspondientes. Le recomendamos que use un dispositivo específico para cada quiosco de la recepción, por ejemplo, una tableta.

Puede ir al quiosco de las siguientes maneras:

- Vaya al tablero principal de la aplicación _Recepción_ y haga clic en el botón Abrir recepción ubicado en la tarjeta de la estación. El kiosco se abrirá en una nueva pestaña del navegador.
    
- Vaya a Recepción ‣ Configuración ‣ Estaciones y haga clic en una. Después, haga clic en el botón Copiar que se encuentra al final de la línea URL del quiosco y pegue la URL en una nueva pestaña o ventana del navegador.
    

 Importante

Le recomendamos que salga de la base de datos y cierre esa pestaña después de ir al quiosco, esto elimina la posibilidad de que un visitante acceda a la base de datos al registrar su entrada.

## Reportes[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk.html#reporting "Enlazar permanentemente con este título")

En la aplicación _Recepción_ hay dos reportes disponibles: Visitantes y Bebidas.

Para acceder a cualquiera de ambos, vaya a Recepción ‣ Reportes. Al hacer clic allí, se abrirá el menú desplegable con las opciones para visitantes y bebidas.

El reporte de visitantes muestra el número de visitantes por mes para el año en curso y el reporte de bebidas muestra el número de solicitudes totales de cada bebida.

Al igual que con todos los reportes en Odoo, puede modificar los filtros y grupos para visualizar otras métricas.

 Ver también

- [Visitantes](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk/visitors.html)