[Cloudflare Turnstile](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/spam_protection.html#cloudflare-turnstile) y [Google reCAPTCHA v3](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/spam_protection.html#google-recaptcha) protegen los formularios del sitio web contra spam y abuso. Usan rompecabezas no intuitivos basados en telemetría y el comportamiento del visitante para distinguir entre un humano y un robot.

 Importante

Le recomendamos usar **Cloudfare Turnstile** ya que es posible que reCAPTCHA v3 no cumpla con las regulaciones locales de protección de datos.

 Nota

Todas las páginas que utilicen los snippets Formulario, Bloque de boletín, Ventana emergente del boletín y el formulario Pasos adicionales durante la finalización de la compra en el comercio electrónico, estarán protegidos con ambas herramientas.

 Ver también

- [Documentación de Cloudflare Turnstile](https://developers.cloudflare.com/turnstile/)
    
- [Guía para reCAPTCHA v3 de Google](https://developers.google.com/recaptcha/docs/v3)
    

## Configuración de Cloudflare Turnstile[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/spam_protection.html#cloudflare-turnstile-configuration "Enlazar permanentemente con este título")

### En Cloudflare[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/spam_protection.html#on-cloudflare "Enlazar permanentemente con este título")

- [Cree](https://dash.cloudflare.com/sign-up) una cuenta de Cloudflare o use una existente e [inicie sesión](https://dash.cloudflare.com/login).
    
- En la barra de navegación haga clic en Turnstile.
    
- En la página Sitios de Turnstile haga clic en Agregar sitio.
    
- Agregue un Nombre del sitio para poder identificarlo.
    
- Ingrese o seleccione el Dominio del sitio web (e.g., _ejemplo.com_ or _subdominio.ejemplo.com_).
    
- Seleccione un Modo widget:
    
    - **Recomendamos** usar el modo Administrado ya que se le pedirá a los clientes marcar una casilla para que confirmen que son humanos si Turnstile lo considera necesario.
        
        ![Widget de verificación de Cloudflare Turnstile](https://www.odoo.com/documentation/17.0/es/_images/turnstile-human.png)
        
    - En los modos No interactivo e Invisible no se le pedirá a los visitantes que interactúen. En el modo No interactivo se mostrará un widget de carga para advertir que Turnstile está protegiendo el formulario; sin embargo, este widget no es compatible con Odoo.
        
         Nota
        
        Si la revisión de Turnstile falla, los visitantes no podrán enviar el formulario y aparecerá el siguiente mensaje de error:
        
        ![Mensaje de error en la verificación de Cloudflare Turnstile.](https://www.odoo.com/documentation/17.0/es/_images/turnstile-error.png)
        
- Haga clic en Crear.
    

![Agregar un sitio web a Cloudflare Turnstile](https://www.odoo.com/documentation/17.0/es/_images/turnstile-configuration.png)

Se muestran las claves generadas. Deje la página abierta para facilidad de uso, ya que necesita copiar estas claves en Odoo.

### En Odoo[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/spam_protection.html#on-odoo "Enlazar permanentemente con este título")

- Desde el tablero de la base de datos, haga clic en Ajustes. Si es necesario, active la opción Cloudflare Turnstile y haga clic en Guardar.
    
- Abra la página de Google reCAPTCHA, copie la Clave del sitio y péguela en el campo Clave CF del sitio en Odoo.
    
- Abra la página de Cloudflare Turnstile, copie la Clave secreta y péguela en el campo Clave secreta CF en Odoo.
    
- Haga clic en Guardar.
    

 Truco

Vaya a Turnstile en su cuenta de Cloudflare para ver las tasas de solución y acceder a más ajustes.

## Configuración reCAPTCHA v3[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/spam_protection.html#recaptcha-v3-configuration "Enlazar permanentemente con este título")

 Advertencia

Es posible que reCAPTCHA v3 no cumpla con las regulaciones locales de protección de datos.

### En Google[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/spam_protection.html#on-google "Enlazar permanentemente con este título")

Ingrese a la [página web de registro de reCAPTCHA](https://www.google.com/recaptcha/admin/create). Inicie sesión o cree una cuenta de Google si es necesario.

En la página web de registro:

- Póngale una Etiqueta al sitio web.
    
- Deje el tipo de reCAPTCHA en Score based (v3).
    
- Introduzca uno o mas Dominios (por ejemplo, _example.com_ or _subdomain.example.com_).
    
- En Plataforma Google Cloud, se seleccionará automáticamente un proyecto si ya se creó uno con la cuenta con la que inició sesión en Google. Si no es así, se creará uno automáticamente. Haga clic en Plataforma Google Cloud para que usted mismo pueda seleccionar un proyecto o para cambiar el nombre del poryecto que se creó de manera automática.
    
- Acepte los términos y condiciones de servicio.
    
- Haga clic en Enviar.
    

![Ejemplo del sitio web de registro de reCAPTCHA.](https://www.odoo.com/documentation/17.0/es/_images/recaptcha-google-configuration.png)

Aparecerá una nueva página con las claves generadas. Déjela abierta para más tarde, pues necesitará copiar las claves en Odoo después.

### En Odoo[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/spam_protection.html#id1 "Enlazar permanentemente con este título")

- Desde el tablero de la base de datos, haga clic en Ajustes. Si es necesario, active la opción reCAPTCHA en la sección de Integraciones.
    
     Advertencia
    
    No desactive la función reCAPTCHA ni desinstale el módulo integración de Google reCAPTCHA, pues es posible que se eliminen otros módulos.
    
- Abra la página de Google reCAPTCHA, copie la Clave del sitio y péguela en el campo Clave del sitio en Odoo.
    
- Abra la página de Google reCAPTCHA, copie la Clave secreta y péguela en el campo Clave secreta en Odoo.
    
- Cambie el Puntaje mínimo requerido (`0.5`) predeterminado si es necesario, usando un valor entre `1.00` y `0.00`. Entre más alto sea el umbral, más difícil será aprobar el reCAPTCHA y viceversa.
    
- Haga clic en Guardar.
    

Puede notificar a los visitantes que reCAPTCHA proteje un formulario. Para hacerlo, abra el editor del sitio web y vaya al formulario. Luego, haga clic en cualquier parte del formulario y en la pestaña Personalizar que se encuentra del lado derecho de la barra, conmute Mostrar política de reCAPTCHA que está en la sección de Formulario.

![Mensaje de política de reCAPTCHA que aparece en el formulario](https://www.odoo.com/documentation/17.0/es/_images/recaptcha-policy.png)

 Nota

Si el reconocimiento falla, aparecerá el siguiente mensaje de error:

![Mensaje de error en la verificación de Google reCAPTCHA.](https://www.odoo.com/documentation/17.0/es/_images/recaptcha-error.png)

 Truco

La analítica y otros ajustes adicionales están disponibles en la [página de administración de Google reCAPTCHA](https://www.google.com/recaptcha/admin/). Por ejemplo, puede recibir alertas por correo electrónico si Google detecta tráfico sospechoso en su sitio web o puede ver el porcentaje de solicitudes sospechosas, lo que puede ayudarle a determinar el puntaje mínimo adecuado.