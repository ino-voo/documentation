En la aplicación _Recepción_ un _visitante_ es cualquier persona que no sea un empleado (por ejemplo, alguien de reparación, un candidato a un puesto de trabajo, etcétera). Estos visitantes pueden registrarse al entrar y al salir por cuestiones de seguridad, de esta forma, contará con una lista precisa de las personas que se encuentran en las instalaciones.

## Lista de visitantes[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk/visitors.html#visitor-list "Enlazar permanentemente con este título")

Para consultar la lista completa de visitantes registrados, vaya a Recepción ‣ Visitantes.

 Nota

Los filtros que aparecen de forma predeterminada en la barra de búsqueda son Planeado o Entrada registrada y Hoy.

Todos los visitantes aparecen en una vista de lista con los detalles que proporcionaron al registrar su entrada, que son:

- Nombre: el nombre del invitado.
    
- Empresa del visitante: la empresa a la que representa el invitado.
    
- Teléfono: el número telefónico del invitado.
    
- Bebidas*: la bebida que solicitó el invitado.
    
- Anfitrión: la persona a la que el invitado visita.
    
- Entrada: la fecha y hora en que el visitante registró su entrada.
    
- Salida*: la fecha y hora en que el invitado se fue. En la vista predeterminada solo aparecen los visitantes con los estados Entrada registrada o Planeado. Los invitados que ya registraron su salida solo son visibles si el filtro Hoy no está activo.
    
- Duración: la cantidad de tiempo que el invitado estuvo en las instalaciones hasta registrar su salida.
    
- Estación: la ubicación en donde se registró el invitado.
    
- Estado: el estado del visitante. Las opciones son Entrada registrada, Planeado, Salida registrada, o Cancelada.
    
- Correo electrónico*: la dirección de correo electrónico del invitado.
    

* Estos campos no son visibles en la lista predeterminada Visitante. Estos se deben activar usando el icono  (ajustes) en la parte superior derecha de la lista.

Del lado derecho de las columnas con título en la página de Visitantes hay una columna sin título, allí puede actualizar el estado de los invitados.

Cuando un invitado se retira, haga clic en el botón Registrar salida para actualizar su registro y almacenar la fecha y hora en que se fue.

Si llega un invitado que estaba programado y no se registra con el quiosco de _Recepción_, puede registrarse si hace clic en el botón disponible Registrar entrada para registrar la fecha y hora de su llegada.

Junto a la columna de estado sin título aparece el botón Bebida servida, pero solo en caso de que ese visitante haya solicitado una.

Después de haber entregado la bebida, haga clic en el botón Bebida servida para indicar que ya se las entregó. El botón desaparece después de hacer clic en él.

![La lista completa de los visitantes que se encuentran registrados. El botón "Bebida servida" aparece dentro de un recuadro rojo.](https://www.odoo.com/documentation/17.0/es/_images/visitors.png)

Si cualquier columna no es visible, o si prefiere ocultar una columna visible, haga clic en el icono  (opciones adicionales), ubicado al final de la columna de nombre de la lista. Al hacer esto se mostrará un menú desplegable con opciones para activar o desactivar. Un icono de  (marca de verificación) aparecerá para indicar que la columna es visible.

## Visitantes planificados[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk/visitors.html#planned-visitors "Enlazar permanentemente con este título")

Si quiere ingresar la información de un visitante que espera antes de que este llegue, cree un visitante planeado en la aplicación _Recepción_.

Vaya a Recepción ‣ Visitantes y haga clic en Nuevo para crear un visitante programado. Luego, en el formulario de visitante que aparece, proporcione la misma información que proporcionaría cualquier otro visitante. Los únicos campos obligatorios son el nombre del visitante y la estación a la que se espera que llegue.

 Importante

Si un invitado está planificado, entonces deberá registrar su entrada desde la página de visitantes de la aplicación _Recepción_ (Recepción ‣ Visitantes). Si el visitante registra su entrada con un quiosco, entonces será un registro distinto y la entrada que creó con anterioridad seguirá con el estado Planeado.

El estado Planeado para un visitante planeado **solo** cambia a Entrada registrada cuando ya registraron su entrada _dentro_ de la lista de Visitantes de la aplicación.

Si un invitado se registra desde un quiosco, asegúrese de que todos los registros estén actualizados y que la lista de visitantes actuales sea correcta. Asegúrese de registrar las entradas y salidas correctas para que la lista de visitantes coincida de forma correcta con las personas que se encuentran en sus instalaciones.

Asegúrese de informar a los invitados planificados que **no** deben registrar su entrada con el quiosco si se encuentran en la lista de visitantes planificados.

## Flujo del visitante[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk/visitors.html#visitor-flow "Enlazar permanentemente con este título")

### Registrar la entrada de un visitante[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk/visitors.html#visitor-check-in "Enlazar permanentemente con este título")

Cuando un visitante llega a sus instalaciones, deberá acercarse a un [quiosco de recepción](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk.html#frontdesk-kiosk) y haga clic en Registrar entrada. La información que se le solicita es la que configuró para esa estación de _recepción_ en específico. Si algún dato es obligatorio, el campo incluirá un asterisco rojo (*). El visitante **debe** proporcionar la información necesaria para poder registrar su entrada.

Después de que el visitante completa todos los campos necesarios deberá tocar el botón Registrar entrada.

 Nota

No importa en qué parte del proceso de registro se encuentre, el quiosco vuelve a la pantalla de bienvenida si pasan diez segundos sin que ocurra una acción.

### Bebidas[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk/visitors.html#drinks "Enlazar permanentemente con este título")

Si configuró bebidas para la estación, la pregunta ¿Le gustaría algo de beber? aparecerá en la pantalla de confirmación de registro después de hacer clic en el botón Registrar entrada.

El visitante puede elegir entre Sí, por favor y No, gracias.

Si selecciona Sí, por favor, entonces aparece una pantalla de selección de bebidas con las opciones preconfiguradas. El visitante deberá tocar la bebida que desee y si cambió de opinión puede tocar el botón Ninguna, gracias ubicado en la parte inferior de la pantalla.

Si eligió una bebida, en la pantalla aparecerá el mensaje ¡Gracias por registrarse! Su bebida ya está en camino.

### Notificaciones[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk/visitors.html#notifications "Enlazar permanentemente con este título")

Una vez que el visitante registró su entrada, se le notificará a la persona que fue a visitar y a cualquier otro usuario que haya configurado para recibir un aviso al registrar entradas en el quiosco. La notificación es por correo electrónico, mensaje SMS, un chat de _Conversaciones_ o cualquier combinación con alguna de esas tres opciones.

Si el visitante solicitó una bebida, los usuarios configurados en el campo Personas a notificar del formulario de la bebida, recibirán una notificación a través de la aplicación _Conversaciones_. El mensaje que aparece es :guilabel:[`](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk/visitors.html#id1)(Nombre del visitante) acaba de registrar su entrada. Solicitó una bebida: (Nombre de la bebida) [`](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk/visitors.html#id3).

Una vez el invitado tiene la bebida que solicitó, la persona que se la entregó es responsable de marcarla como entregada.

To mark a drink as delivered, navigate to Frontdesk app ‣ Stations, and choose the desired station card displaying (#) Drinks to serve.

Esa acción abrirá la lista con todos los visitantes registrados en esa estación que están en espera de una bebida. Haga clic en el botón Bebida servida ubicada al final de la línea del visitante correspondiente. El visitante desaparece de la lista después de que marca la bebida como servida.

### Registrar salida[](https://www.odoo.com/documentation/17.0/es/applications/hr/frontdesk/visitors.html#check-out "Enlazar permanentemente con este título")

Es importante que registre la salida del visitante después de que sale de sus instalaciones para que todos los registros estén en orden.

Para registrar las salidas de forma correcta, vaya a Recepción ‣ Estaciones y seleccione la tarjeta de la estación correspondiente donde se muestre (#) Bebidas por servir. Así se abrirá una lista de todos los visitantes que registraron su entrada en la estación.

Haga clic en el botón Registrar salida ubicado cerca del final de la línea del visitante que se retiró. Después de que lo presiona, el visitante desaparece de la lista.

 Importante

Los visitantes **no** registran su propia salida, así que es importante que los usuarios de _Recepción_ lo hagan para que sus registros sean los correctos.

Por motivos de seguridad y en caso de emergencia, es importante que siempre tenga una lista precisa de quienes se encuentran en sus instalaciones.