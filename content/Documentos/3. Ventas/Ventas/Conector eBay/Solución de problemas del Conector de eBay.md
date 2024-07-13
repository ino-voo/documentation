 Ver también

Para obtener más información relacionada al Conector de eBay puede visitar las siguientes páginas:

- [Configuración del Conector de eBay](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/setup.html)
    
- [¿Cómo anunciar un producto?](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/manage.html)
    
- [Vincular anuncios existentes](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/linking_listings.html)
    

## Aceptar notificaciones de eliminación de cuenta[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html#accept-account-deletion-notifications "Enlazar permanentemente con este título")

Desde septiembre de 2021, **eBay exige compatibilidad con las notificaciones de eliminación o cierre de cuentas de clientes**. Por lo tanto, cuando eBay recibe una solicitud de eliminación, todos los miembros de eBay deben confirmar la recepción de la solicitud y tomar medidas adicionales si es necesario.

Odoo tiene un punto de conexión de notificaciones para recibirlas, confirmar la recepción de la solicitud y gestionar el primer conjunto de acciones para anonimizar los detalles de la cuenta en _Contactos_ y eliminar el acceso del cliente al portal.

 Importante

Asegúrese de [configurar de forma adecuada la suscripción a las notificaciones de eliminación de cuenta del mercado](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html#ebay-subscribe-account-deletion-notifications), ya que tal vez eBay deshabilite la cuenta de eBay relacionada de forma temporal hasta completar la suscripción.

### Verifique que su instalación de Odoo está actualizada[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html#verify-the-installation-of-odoo-is-up-to-date "Enlazar permanentemente con este título")

Es necesario que instale el módulo _Conector de eBay - Eliminación de cuenta_ para poder activar el punto de conexión. Si su base de datos de Odoo se creó después de septiembre del 2021, el módulo se instala de forma automática y el administrador puede continuar con el [siguiente paso](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html#ebay-retrieve-endpoint-details).

#### Actualizar Odoo a la versión más reciente[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html#update-odoo-to-the-latest-release "Enlazar permanentemente con este título")

El punto de conexión de la notificación está disponible a través de un nuevo módulo de Odoo. Para instalarlo, el administrador debe asegurarse de que su código fuente de Odoo esté actualizado.

- Si la empresa utiliza Odoo en Odoo.com o en una plataforma de Odoo.sh, su código ya está actualizado y puede continuar con el siguiente paso.
    
- Si la empresa utiliza Odoo en una configuración local o a través de un partner, entonces el administrador debe actualizar la instalación tal como se describe en [esta página de la documentación](https://www.odoo.com/documentation/17.0/es/administration/on_premise/update.html), también puede contactar a un partner de integración.
    

#### Actualizar la lista de módulos disponibles[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html#update-the-list-of-available-modules "Enlazar permanentemente con este título")

La instancia de Odoo debe _descubrir_ los nuevos módulos para que estén disponibles en el menú de Aplicaciones.

Para hacerlo, active el [modo de desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode), y vaya a Aplicaciones -> Actualizar lista de aplicaciones. Un asistente le solicitará confirmar.

#### Instalar la actualización de «Conector de eBay - Eliminación de cuenta»[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html#install-the-ebay-connector-account-deletion-update "Enlazar permanentemente con este título")

 Advertencia

**Nunca** instale nuevos módulos en la base de datos de producción sin antes probarlos en un entorno duplicado o de prueba. Los clientes de Odoo.com pueden crear una base duplicada desde la página de gestión de bases de datos; si son usuarios de Odoo.sh, entonces los administradores deben usar una base de datos de prueba o una duplicada. En caso de que se trate de usuarios locales, el administrador debe usar un entorno de prueba. Contacte a su partner de integración para obtener más información sobre cómo probar un nuevo módulo en su configuración específica.

Para instalar el módulo, vaya a Aplicaciones, elimine el filtro de `Aplicaciones` y busque `eBay`. Si el módulo _Conector de eBay - Eliminación de cuenta_ está disponible y aparece como «Instalado», su base de datos de Odoo ya está actualizada y puede realizar el siguiente paso. Si aún no está instalado, hágalo ahora.

### Recuperar los detalles de los puntos finales de comunicación de Odoo[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html#retrieve-endpoint-details-from-odoo "Enlazar permanentemente con este título")

Los detalles del punto de conexión están disponibles en Ventas ‣ Configuración ‣ Ajustes ‣ eBay. Primero ingrese valores de texto aleatorios en la clave de aplicación de producción y la clave de certificación de producción. Haga clic en Generar token para obtener el token de verificación.

![Generar un token de verificación en Odoo.](https://www.odoo.com/documentation/17.0/es/_images/generate-token1.png)

### Recibir las notificaciones de eliminación de cuenta[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html#subscribe-to-account-deletion-notifications "Enlazar permanentemente con este título")

vaya al [portal de desarrolladores de eBay](https://go.developer.ebay.com/). Configure la eliminación de cuenta o los ajustes de notificaciones en eBay desde `Hola, [nombre de usuario]` ubicado en la parte superior derecha de la pantalla, luego vaya a Alertas y notificaciones.

![Vista general del tablero de alertas y notificaciones de eBay](https://www.odoo.com/documentation/17.0/es/_images/ebay-your-account.png)

Para recibir las notificaciones de eliminación o cierre, eBay necesita algunos detalles:

- Una **dirección de correo electrónico** para enviar notificaciones si no puede conectarse al punto de conexión.
    
- Los _detalles del punto de conexión_:
    
    - La URL del punto final de comunicación de la notificación de eliminación de la cuenta.
        
    - Un token de verificación
        

![Campos específicos para ingresar los detalles del punto final de comunicación.](https://www.odoo.com/documentation/17.0/es/_images/ebay-notification-endpoint.png)

 Truco

El administrador puede editar los dos últimos campos una vez que el campo de dirección de correo electrónico esté completo.

### Verificar la conectividad con el punto final de comunicación[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html#verify-the-connectivity-with-the-endpoint "Enlazar permanentemente con este título")

Después de configurar los detalles del punto de conexión obtenidos en el tablero de eBay, considere realizar pruebas de conectividad con el botón Enviar notificación de prueba.

> Debe recibir el siguiente mensaje de confirmación: «¡Se envió con éxito una notificación de prueba!»

![Botón para enviar notificaciones de prueba](https://www.odoo.com/documentation/17.0/es/_images/test-notification.png)

 Ver también

- [¿Cómo anunciar un producto?](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/manage.html)
    
- [Vincular anuncios existentes](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/linking_listings.html)
    
- [Configuración del Conector de eBay](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/setup.html)