Los nombres de dominio son direcciones basadas en texto que identifican ubicaciones en línea, como sitios web. También son más fáciles de recordar, así las personas pueden navegar por internet sin tener que hacer uso de direcciones IP numéricas.

Las bases de datos de **Odoo en línea** y **Odoo.sh** usan un **subdominio** del **dominio** de `odoo.com` de forma predeterminada (por ejemplo, `miempresa.odoo.com`).

Sin embargo, puede hacer uso de un nombre de dominio personalizado y [registrar un nombre de dominio gratuito](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-register) (solo está disponible para las bases de datos de Odoo en línea) o [configurar uno que ya le pertenezca](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-existing).

 Ver también

[Tutoriales de Odoo: registrar un nombre de dominio gratis [video]](https://www.odoo.com/slides/slide/register-a-free-domain-name-1663)

## Registre un nombre de dominio gratis con Odoo[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#register-a-free-domain-name-with-odoo "Enlazar permanentemente con este título")

Para registrar un nombre de dominio gratuito por un año para su base de datos de Odoo en línea, inicie sesión en su cuenta y vaya al [gestor de bases de datos](https://www.odoo.com/my/databases). Haga clic en el icono de engranaje (⚙️) ubicado junto al nombre de la base de datos y seleccione Nombres de dominio.

![Acceder a la configuración de nombres de dominio de una base de datos.](https://www.odoo.com/documentation/17.0/es/_images/domain-names.png)

Busque el nombre de dominio deseado y verifique su disponibilidad.

![Buscar un nombre de dominio disponible.](https://www.odoo.com/documentation/17.0/es/_images/domain-search.png)

 Truco

Si la opción para registrar un nombre de dominio no aparece, primero asegúrese de que la aplicación Sitio web está instalada.

Seleccione el nombre de dominio deseado, complete el formulario de Propietario del dominio y haga clic en Registrar. El nombre de dominio elegido se vinculará a la base de datos.

![Completar la información del propietario de dominio.](https://www.odoo.com/documentation/17.0/es/_images/domain-owner.png)

Después debe [mapear su nombre de dominio a su sitio web de Odoo](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-website-map).

 Importante

Recibirá un correo electrónico de verificación de `noreply@domainnameverification.net` en la dirección que proporcionó en el formulario Propietario del dominio. Es muy importante que verifique su dirección de correo electrónico, así mantendrá el dominio activo y podrá recibir la cotización de renovación antes de que venza.

El registro del nombre de dominio es gratis durante el primer año. Después de este periodo, Odoo continuará gestionando el dominio con **Gandi.net**, el registrador de nombres de dominio, y se le cobrará la [tarifa de renovación de Gandi.net](https://www.gandi.net/en/domain). Cada año, Odoo envía una cotización de renovación a la dirección de correo electrónico que estableció en el formulario Propietario del dominio varias semanas antes de la fecha de vencimiento del dominio. El dominio se renueva de forma automática cuando confirma la cotización.

 Nota

- Esta oferta solo está disponible para las bases de datos de **Odoo en línea**.
    
- La oferta está limitada a **un** nombre de dominio por cliente.
    
- La oferta está limitada al registro de un **nuevo** nombre de dominio.
    
- La oferta está disponible para los planes de _una aplicación gratis_. Asegúrese de que su sitio web incluya suficiente contenido original para que Odoo verifique que su solicitud es legítima y respeta la [Política de uso aceptable de Odoo](https://www.odoo.com/acceptable-use). Recibimos varias solicitudes, así que su revisión puede tardar varios días.
    

### Registros DNS[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#dns-records "Enlazar permanentemente con este título")

Para gestionar los registros DNS de su dominio gratuito, abra el [gestor de bases de datos](https://www.odoo.com/my/databases), haga clic en el icono de engranaje (⚙️) ubicado junto al nombre de la base de datos, seleccione Nombres de dominio y haga clic en DNS.

- A: el registro A contiene la dirección IP del dominio. Se crea de forma automática y **no** se puede editar ni eliminar.
    
- CNAME: los registros CNAME se encargan de reenviar un dominio o subdominio a otro dominio. Uno se crea de forma automática para asignar el subdominio `www.` a la base de datos. Si cambia el nombre de la base de datos, también **deberá** cambiar el nombre del registro CNAME.
    
- MX: los registros MX le indican a los servidores a dónde enviar los correos electrónicos.
    
- TXT: los registros TXT sirven para cumplir con distintos propósitos (por ejemplo, para verificar la propiedad de un nombre de dominio).
    

Cualquier modificación a los registros DNS puede tardar hasta **72 horas** en propagarse a todos los servidores.

 Nota

[Envíe un ticket de soporte](https://www.odoo.com/help) si necesita ayuda para gestionar su nombre de dominio.

### Buzón de correo[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#mailbox "Enlazar permanentemente con este título")

La oferta de un año de dominio gratis **no** incluye buzón de correo, pero hay dos opciones para vincular su nombre de dominio con uno.

#### Usar un subdominio[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#use-a-subdomain "Enlazar permanentemente con este título")

Puede crear un subdominio (por ejemplo, `subdominio.sudominio.com`) para usarlo como un dominio de seudónimo para la base de datos. Esto permite que los usuarios creen registros en la base de datos a partir de los correos electrónicos que reciben en su seudónimo `correo@subdominio.sudominio.com`.

Para ello, abra el [gestor de bases de datos](https://www.odoo.com/my/databases), haga clic en el icono de engranaje (⚙️) ubicado junto al nombre de la base de datos y vaya a Nombres de dominio ‣ DNS ‣ Agregar registro DNS ‣ CNAME. Después, escriba el subdominio deseado en el campo Nombre (por ejemplo, `subdominio`), el dominio original de la base de datos con un punto al final (por ejemplo, `miempresa.odoo.com.`) en el campo Contenido y haga clic en Agregar registro.

Luego, agregue el dominio del seudónimo como su _propio dominio_. Haga clic en Usar mi propio dominio, escriba el dominio del seudónimo (por ejemplo, `subdominio.sudominio.com`), haga clic en Verificar y luego en Confirmo, está listo.

Por último, vaya a su base de datos y abra Ajustes. Escriba el dominio del seudónimo (por ejemplo, `subdominio.sudominio.com`) en el campo Dominio del seudónimo, haga clic en Nuevo y luego en Guardar.

#### Usar un proveedor de correo electrónico externo[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#use-an-external-email-provider "Enlazar permanentemente con este título")

Es necesario que configure un registro MX para poder utilizar un proveedor de correo electrónico externo. Para ello, abra el [gestor de bases de datos](https://www.odoo.com/my/databases), haga clic en el icono de engranaje (⚙️) ubicado junto al nombre de la base de datos, haga clic en Nombres de dominio ‣ DNS ‣ Agregar registro DNS ‣ MX. Los valores que agregará a los campos Nombre, Contenido y Prioridad dependen del proveedor de correo electrónico externo.

 Ver también

- [Valores de los registros MX de Google Workspace](https://support.google.com/a/answer/174125?hl=es)
    
- [Agregar un registro MX para el correo electrónico (Outlook, Exchange Online)](https://learn.microsoft.com/es-mx/microsoft-365/admin/get-help-with-domains/create-dns-records-at-any-dns-hosting-provider?view=o365-worldwide#add-an-mx-record-for-email-outlook-exchange-online)
    

## Configurar un nombre de dominio existente[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#configure-an-existing-domain-name "Enlazar permanentemente con este título")

Si ya cuenta con un nombre de dominio, puede usarlo para su sitio web de Odoo.

 Advertencia

Le recomendamos que siga estos tres pasos **en orden** para evitar cualquier problema con la [validación de certificados SSL](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-ssl):

1. [Agregue un registro CNAME](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-cname).
    
2. [Mapee su nombre de dominio a su base de datos de Odoo](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-db-map).
    
3. [Mapee su nombre de dominio a su sitio web de Odoo](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-website-map).
    

### Agregar un registro CNAME[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#add-a-cname-record "Enlazar permanentemente con este título")

Es necesario que agregue un registro CNAME para reenviar su nombre de dominio a la dirección de su base de datos de Odoo.

Odoo OnlineOdoo.sh

La dirección de destino del registro CNAME debe ser la dirección de su base de datos tal como la definió al crearla (por ejemplo, `miempresa.odoo.com`).

Las instrucciones específicas dependen de su servicio de alojamiento de DNS.

 Ver también

- [GoDaddy: agregar un registro CNAME](https://www.godaddy.com/help/add-a-cname-record-19236)
    
- [Namecheap: Cómo crear un registro CNAME para su dominio](https://www.namecheap.com/support/knowledgebase/article.aspx/9646/2237/how-to-create-a-cname-record-for-your-domain)
    
- [OVHcloud: agregar un nuevo registro DNS (en inglés)](https://docs.ovh.com/us/en/domains/web_hosting_how_to_edit_my_dns_zone/#add-a-new-dns-record)
    
- [Cloudflare: gestionar registros DNS (en inglés)](https://support.cloudflare.com/hc/en-us/articles/360019093151)
    

 Importante

Odoo solo admite subdominios. Para utilizar su dominio simple (un nombre de dominio sin ningún subdominio o prefijo) (`sudominio.com`), cree una redirección 301 para dirigir a los visitantes a `www.sudominio.com`.

 Example

Usted es propietario del nombre de dominio `sudominio.com` y la dirección de su base de datos de Odoo en línea es `miempresa.odoo.com`. Es común que desee acceder a su base de datos de Odoo con el dominio `www.sudominio.com` pero también con el dominio simple `sudominio.com`.

Para ello, deberá crear un registro CNAME para el subdominio `www` en el que el destino sea `miempresa.odoo.com` y después crear una redirección (3010 redirección permanente o visible) para redirigir a los visitantes de `sudominio.com` a `wwww.sudominio.com`.

### Mapear un nombre de dominio a una base de datos de Odoo[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#map-a-domain-name-to-an-odoo-database "Enlazar permanentemente con este título")

 Advertencia

Asegúrese de haber [agregado un registro CNAME](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-cname) al DNS de su nombre de dominio **antes** de mapear el nombre de su dominio a la base de datos de Odoo.

Si no lo hace, podría evitar la validación del [certificado SSL](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-ssl), lo que a su vez causaría un error de _discordancia con el nombre del certificado_. Por lo general, los navegadores web indican esto mediante una advertencia en la que aparece el mensaje _«La conexión no es privada»_.

En caso de que ocurra este error después de mapear el nombre de dominio a su base de datos deberá esperar máximo cinco días, pues es probable que la validación se encuentre en curso. De lo contrario, [envíe un ticket de soporte](https://www.odoo.com/help) e incluya capturas de pantalla de sus registros CNAME.

Odoo OnlineOdoo.sh

Abra el [gestor de bases de datos](https://www.odoo.com/my/databases), haga clic en el icono de engranaje (⚙️) ubicado junto al nombre de la base de datos y vaya a Nombres de dominio ‣ Utilizar mi propio dominio. Luego, escriba el nombre de dominio (por ejemplo, `tudominio.com`), haga clic en Verificar y luego en Confirmo, está listo.

![Mapear un nombre de dominio a una base de datos de Odoo en línea](https://www.odoo.com/documentation/17.0/es/_images/map-database-online.png)

#### Cifrado SSL (protocolo HTTPS)[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#ssl-encryption-https-protocol "Enlazar permanentemente con este título")

El **cifrado SSL** permite que los visitantes naveguen por un sitio web a través de una conexión segura. Aparece con el protocolo _https://_ al principio de una dirección web en lugar del protocolo no seguro _http://_.

Odoo genera un certificado SSL distinto para cada dominio [mapeado a una base de datos](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-db-map), mediante [la autoridad de certificación Let’s Encrypt y el protocolo ACME](https://letsencrypt.org/how-it-works/).

 Nota

- Generar un certificado puede tomar hasta 24 horas.
    
- Se realizan varios intentos para validar su certificado durante los cinco días posteriores de mapear su nombre de dominio a su base de datos.
    
- Si hace uso de otro servicio, puede seguir usándolo o cambiarse a Odoo.
    

 Importante

No se generan certificados SSL para los dominios simples (nombres de dominio sin subdominios ni prefijos).

#### URL web base de la base de datos[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#web-base-url-of-a-database "Enlazar permanentemente con este título")

 Nota

Omita esta sección si su base de datos tiene la aplicación Sitio web instalada, continúe en la sección [Mapear un nombre de dominio a un sitio web de Odoo](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-website-map) .

La _URL web base_ o _URL raíz_ de una base de datos afecta la dirección de su sitio web principal y todos los enlaces que sus clientes recibieron (por ejemplo, cotizaciones, enlaces al portal, entre otros).

Para convertir su nombre de dominio personalizado en la _URL web base_ de su base de datos, primero acceda a su base de datos con su nombre de dominio personalizado e inicie sesión como administrador (un usuario que forma parte del grupo de permisos de acceso a los ajustes en Administración).

 Importante

Si accede a su base de datos con la dirección original de Odoo (por ejemplo, `miempresa.odoo.com`), la _URL base web_ de su base de datos se actualizará. Para evitar que ocurra esto con la _URL base web_ cuando un administrador inicie sesión en la base de datos, active el [modo de desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode), vaya a Ajustes ‣ Técnico ‣ Parámetros del sistema ‣ Nuevo. En la Clave escriba `web.base.url.freeze` y establezca `True` como Valor.

 Nota

También puede establecer la URL base web de forma manual. Para ello, active el [modo de desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode), vaya a Ajustes ‣ Técnico ‣ Parámetros del sistema, busque la clave `web.base.url` (créela si es necesario) y escriba la dirección completa de su sitio web en el valor correspondiente (por ejemplo, `https://www.sudominio.com`). La URL debe incluir el protocolo `https://` (o `http://`) y _no_ terminar con una barra (`/`).

### Mapear un nombre de dominio a un sitio web de Odoo[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#map-a-domain-name-to-an-odoo-website "Enlazar permanentemente con este título")

Mapear su nombre de dominio a su sitio web no es igual a mapearlo a su base de datos:

- Define su nombre de dominio como el principal para su sitio web, lo que ayuda a los buscadores a indexar su sitio web de forma correcta.
    
- Define su nombre de domino como la URL base para su base de datos e incluye los enlaces del portal enviados por correo electrónico a sus clientes.
    
- En caso de que tenga varios sitios web, mapea su nombre de dominio al sitio web correcto.
    

Vaya a Sitio web ‣ Configuración ‣ Ajustes. En caso de que tenga varios sitios web, seleccione el que desea configurar. Escriba la dirección de su sitio web (por ejemplo, `https://www.sudominio.com`) en el campo Dominio y haga clic en Guardar.

 Advertencia

Mapear su nombre de dominio a su sitio web de Odoo evita que el buscador web de Google indexe la dirección original de su base de datos (por ejemplo, `miempresa.odoo.com`).

Si ambas direcciones ya están indexadas, puede que pase tiempo antes de que la indexación de la segunda dirección se elimine del buscador web de Google. Puede utilizar [Search Console de Google](https://search.google.com/search-console/welcome) para solucionar el problema.

 Nota

Si tiene varios sitios web y empresas en su base de datos, asegúrese de seleccionar la empresa correcta en Sitio web ‣ Configuración ‣ Ajustes. Esto le indica a Odoo qué URL utilizar como la [URL base](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html#domain-name-web-base-url) según la empresa en uso.