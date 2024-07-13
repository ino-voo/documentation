Odoo puede sincronizarse directamente con su institución bancaria para que todos los extractos bancarios se importen automáticamente a su base de datos.

Para verificar si su banco es compatible con Odoo, vaya a [Ajustes de Contabilidad de Odoo](https://www.odoo.com/page/accounting-features), y haga clic en Ver lista de instituciones compatibles.

Odoo colabora con más de 25,000 instituciones alrededor del mundo.

Odoo utiliza múltiples servicios web para conectar con los bancos:

- **Plaid**: Estados Unidos de América y Canadá
    
- **Yodlee**: En todo el mundo
    
- [Salt Edge](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/saltedge.html): Global
    
- [Ponto](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/ponto.html): Europa
    
- [Enable Banking](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/enablebanking.html): Países escandinavos
    

 Ver también

transacciones

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#configuration "Enlazar permanentemente con este título")

### Usuarios locales[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#on-premise-users "Enlazar permanentemente con este título")

Para poder utilizar este servicio, debe tener una suscripción válida de Odoo Enterprise. Asegúrese de que su base de datos esté registrada con su contrato de Odoo Enterprise. También usamos un proxy entre su base de datos y el proveedor externo, por lo que, en caso de un error de conexión, tiene que verificar que no tenga un firewall o un proxy que bloquee esta dirección:

- [https://production.odoofin.com/](https://production.odoofin.com/)
    

### Primera sincronización[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#first-synchronization "Enlazar permanentemente con este título")

Puede comenzar la sincronización ingresando a la aplicación Contabilidad y luego a Panel de contabilidad ‣ Configuración ‣ Bancos: Agregar una cuenta bancaria.

Ahora puede buscar su institución bancaria. Selecciónela y siga los pasos para sincronizarla.

 Nota

Si tiene algún inconveniente durante la primera sincronización, verifique que su navegador web no bloquee las ventanas emergentes y que el bloqueador de anuncios esté desactivado.

 Importante

Al configurar la sincronización de estados de cuenta bancarios, Odoo comienza a registrar de forma automática las transacciones contables desde la fecha de la última transacción más 1 día (si el día de la última transacción corresponde al 31/12/2022, se comienzan a registrar el 01/01/2023). Si el diario no contiene ninguna transacción, Odoo recupera las transacciones más antiguas. Es posible limitar el tiempo anterior en que Odoo recupera transacciones desde la aplicación Contabilidad, vaya a Contabilidad ‣ Fechas de bloqueo y establezca una fecha en el campo Fecha de bloqueo de asientos contables.

En la primera sincronización deberá proporcionar un número de teléfono para poder proteger su cuenta. Esta información es necesaria para asegurarnos de que otras personas no puedan acceder a sus datos. Si en algún momento detectamos movimientos sospechosos en su cuenta, bloquearemos todas las solicitudes provenientes de la misma y tendrá que reactivarlas con su número telefónico.

El proveedor externo puede solicitar más información para conectar con su institución bancaria. Esta información no se almacena en los servidores de Odoo.

De forma predeterminada, las transacciones obtenidas de una fuente en línea se agrupan dentro del mismo extracto y se crea un extracto bancario por mes. Puede cambiar la periodicidad de creación de extractos bancarios en la configuración de su diario.

Puede encontrar todas sus sincronizaciones en el tablero de Contabilidad‣ Configuración ‣ Contabilidad: sincronización en línea.

### Sincronización manual[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#synchronize-manually "Enlazar permanentemente con este título")

Los diarios creados se sincronizan de forma predeterminada cada 12 horas luego de la primera sincronización. Si lo desea, puede sincronizarlos de forma manual al hacer clic en el botón Sincronizar ahora del tablero.

O puede ir al tablero de Contabilidad ‣ Configuración ‣ Contabilidad: Sincronización en línea, seleccionar su institución y hacer clic en el botón Obtener transacciones.

 Importante

Algunas instituciones no permiten que las transacciones se obtengan de forma automática. Para estas instituciones, recibirá un mensaje de error solicitándole que desactive la sincronización automática durante la sincronización automática de la cuenta. Este mensaje podrá encontrarlo en el chatter de sus sincronizaciones en línea. En este caso, asegúrese de realizar sincronizaciones manuales.

## Errores[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#issues "Enlazar permanentemente con este título")

### Error de sincronización[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#synchronization-in-error "Enlazar permanentemente con este título")

Para reportar un error de conexión al [soporte de Odoo](https://www.odoo.com/help), vaya al tablero de Contabilidad‣ Configuración ‣ Contabilidad: Sincronización en línea, seleccione la conexión errónea y copie la descripción del error y la referencia.

### Desconexión de la sincronización[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#synchronization-disconnected "Enlazar permanentemente con este título")

Si su conexión con el proxy se desconecta, puede volver a conectarse con el proxy mediante el botón Recuperar cuenta.

 Nota

Si no puede recuperar conexión con el botón Reconectar póngase en contacto con [soporte](https://www.odoo.com/help) directamente con su ID de cliente o la referencia de error que se menciona en el chatter.

## Proceso de migración para usuarios que hayan instalado Odoo antes de diciembre de 2020[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#migration-process-for-users-having-installed-odoo-before-december-2020 "Enlazar permanentemente con este título")

Si usa Odoo local, primero asegúrese de que su fuente esté actualizada con la última versión de Odoo.

Los usuarios que hayan creado una base de datos antes de diciembre de 2020 deben instalar el nuevo módulo de forma manual para utilizar las nuevas funciones.

Para ello, vaya a Aplicaciones ‣ Actualizar la lista de aplicaciones, elimine el filtro predeterminado en la barra de búsqueda y escriba `account_online_synchronization`. Haga clic en Instalar y, por último, asegúrese de que todos sus usuarios presionen CTRL+F5 para actualizar su página de Odoo.

 Nota

- Todas las sincronizaciones anteriores se desconectan durante la instalación y no volverán a funcionar.
    
- Puede encontrarlos directamente en el menú de sincronización (Contabilidad ‣ Configuración ‣ Contabilidad: Sincronización en línea). No es posible resincronizar estas conexiones; tiene que crear otras nuevas.
    
- No desinstale el `account_online_sync`, que es el módulo anterior para la sincronización en línea. El nuevo lo anula.
    
- De forma predeterminada, `account_online_synchronization` se instala en automático con Contabilidad.
    

## Preguntas frecuentes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#faq "Enlazar permanentemente con este título")

### La sincronización no está funcionando en tiempo real, ¿es normal?[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#the-synchronization-is-not-working-in-real-time-is-that-normal "Enlazar permanentemente con este título")

El proceso no está diseñado para funcionar en tiempo real, pues los proveedores externos sincronizan sus cuentas en distintos intervalos. Para forzar la sincronización y obtener los estados de cuenta, vaya a su tablero de Contabilidad y haga clic en el botón Sincronizar ahora. También puede sincronizar y obtener transacciones mediante el tablero de Contabilidad ‣ Configuración ‣ Contabilidad: Sincronización en línea. Algunos proveedores solo permiten una actualización por día, por lo que es posible que al hacer clic en Sincronizar ahora no aparezcan sus transacciones más recientes si ya realizó esa acción antes durante el mismo día.

Una transacción puede ser visible en su cuenta bancaria pero no ser recuperada si tiene el estado Pendiente. Solo se obtendrán las transacciones con el estado Publicado. Si la transacción aún no ha sido **Publicada**, deberá esperar hasta que cambie su estado.

### ¿La función de sincronización bancaria en línea está incluida en mi contrato?[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#is-the-online-bank-synchronization-feature-included-in-my-contract "Enlazar permanentemente con este título")

- **Versión Community**: No, esta función no está incluida en la versión Community.
    
- **Versión en línea**: Sí, incluso si se beneficia del contrato Una aplicación gratis.
    
- ** Versión Enterprise**: Sí, si tiene un contrato Enterprise válido vinculado a su base de datos.
    

### Algunos bancos tienen un estado «Beta», ¿qué significa?[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#some-banks-have-a-status-beta-what-does-this-mean "Enlazar permanentemente con este título")

Esto significa que las instituciones bancarias aún no cuentan con el respaldo total de nuestro proveedor externo y pueden ocurrir errores u otros problemas. Odoo no proporciona ayuda con problemas técnicos que ocurren con los bancos en la fase beta, pero el usuario aún puede optar por conectarse. La conexión con estos bancos contribuye al proceso de desarrollo, ya que el proveedor tendrá datos reales y comentarios de la conexión.

### ¿Por qué mis transacciones solo se sincronizan cuando las actualizo de forma manual?[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#why-do-my-transactions-only-synchronize-when-i-refresh-manually "Enlazar permanentemente con este título")

Algunos bancos tienen medidas de seguridad adicionales y requieren otros pasos, como un código de autenticación por SMS, correo electrónico u otro tipo de autenticación de múltiples factores. Debido a esto, el integrador no puede extraer transacciones hasta que proporcione el código de seguridad.

### No todas mis transacciones pasadas están en Odoo, ¿por qué?[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#not-all-of-my-past-transactions-are-in-odoo-why "Enlazar permanentemente con este título")

Para algunas instituciones solo se pueden recuperar las transacciones de los 3 meses anteriores.

### ¿Por qué no veo ninguna transacción?[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#why-don-t-i-see-any-transactions "Enlazar permanentemente con este título")

Durante su primera sincronización, seleccionó las cuentas bancarias que decidió sincronizar con Odoo. Si no sincronizó ninguna de sus cuentas, puede ir al tablero de Contabilidad ‣ Configuración ‣ Contabilidad: Sincronización en línea y hacer clic en el botón Obtener cuenta en la conexión.

También es posible que no haya nuevas transacciones.

Si su cuenta bancaria está vinculada a un diario de forma correcta y las transacciones registradas no aparecen en su base de datos, [envíe un ticket al servicio de soporte](https://www.odoo.com/help).

### ¿Cómo puedo actualizar mis credenciales bancarias?[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html#how-can-i-update-my-bank-credentials "Enlazar permanentemente con este título")

Puede actualizar sus credenciales desde el tablero de Contabilidad ‣ Configuración ‣ Contabilidad: Sincronización en línea; abra la conexión en la que desea actualizar sus credenciales y haga clic en el botón Actualizar credenciales.