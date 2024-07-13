[Ogone](https://www.ingenico.com/), también conocido como **Servicios de pago Ingenico** es una empresa con sede en Francia que proporciona la tecnología involucrada en transacciones electrónicas seguras.

 Ver también

- [Activar un proveedor de pago](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-add-new)
    
- [Documentación de Ogone](https://epayments-support.ingenico.com/get-started/).
    

 Advertencia

El proveedor Ogone ya es obsoleto. En su lugar, se le recomienda usar [Stripe](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/stripe.html).

## Configuración en Ongone[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/ogone.html#settings-in-ogone "Enlazar permanentemente con este título")

### Cree un usuario API[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/ogone.html#create-an-api-user "Enlazar permanentemente con este título")

Inicie sesión en su cuenta de Ogone y vaya a la pestaña Configuración.

Necesita crear un **Usuario API** para usarlo al momento de realizar transacciones en Odoo. Si bien puede usar su cuenta principal para hacerlo, usar un **Usuario API** le garantiza que si las credenciales utilizadas en Odoo se filtran, no se podrá acceder a las configuraciones de Ongone. Además, las contraseñas para los **Usuarios API** no necesitan actualizarse constantemente, a diferencia de los usuarios normales.

Para crear un **Usuario API**, vaya a Configuración ‣ Usuarios y haga clic en Usuario nuevo. Se deben configurar los siguientes campos:

- ID de usuario: puede escoger el que quiera.
    
- Nombre del usuario, correo electrónico y zona horaria: puede ingresar la información que desee.
    
- El perfil: debe estar establecido como Administrador.
    
- La casilla Usuario especial para API: debe estar seleccionada.
    

Después de crear su usuario, debe generar una contraseña. Guárdela junto con el **ID del usuario** pues los necesitara después durante la configuración.

 Truco

Si ya tiene un usuario configurado, asegúrese de que esté activado sin errores. Si no es el caso, simplemente haga clic en el botón de Activar(Errores) para resetear el usuario.

### Configure Ogone para Odoo[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/ogone.html#set-up-ogone-for-odoo "Enlazar permanentemente con este título")

Ogone debe estar configruado para aceptar pagos desde Odoo. Vaya a Configuración ‣ Información técnica ‣ Parámetros de seguridad globales, seleccione SHA-512 como Algoritmo hash y UTF-8 como codificación de caracter. Luego, vaya a la pestaña Datos y verificación de origen en la misma página y deje el campo de la URL sección Comercio electrónico y entrada de alias vacía.

 Truco

Si necesita usar otro algoritmo, como `sha-1` o `sha-256`, dentro de Odoo, active el [modo desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode) y vaya a la página de **Proveedores de pago** en Contabilidad ‣ Configuración ‣ Proveedores de pago. Haga clic en Ogone, y en la pestaña Credenciales, seleccione el algoritmo que desea utilizar en el campo Función hash.

Ahora debe generar farses de contraseña **SHA-IN**. Las frases de contraseña **SHA-IN** y **SHA-OUT** se usan para firmar digitalmente las solicitudes de transacciones y las respuestas entre Odoo y Ogone. Al usar estas frases de contraseña secretas y el algoritmo `sha-1`, ambos sistemas pueden garantizar que la información que reciben del otro no fue alterada o tocada.

Ingrese la misma frase de contraseña **SHA-IN** tanto en Cheques para comercio electrónico y entrada de alias como en Cheques para DirectLink y Lote (Automático). Puede dejar el campo de la dirección IP vacío.

Sus frases de contraseña **SHA-IN** y **SHA-OUT** deben ser diferentes y deben contener entre 16 y 32 caracteres. Asegúrese de usar las mismas frases de contraseña **SHA-IN** y **SHA-OUT** durante toda la configuración de Ogone, pues Odoo solo permite una sola frase de contraseña para **SHA-IN** y otra para **SHA-OUT**.

Para obtener la clave **SHA-OUT**, inicie sesión en su cuenta de Ongone, vaya a Configuración ‣ Información técnica ‣ Retroalimentación de la transacción ‣ Todos los modos de envío de transacción y obtenga o vuelva a generar su **clave API** y **clave de cliente**. Ponga atención y copie su clave API pues no se le permitirá obtenerla después sin generar una nueva.

Al terminar, vaya a Configuración ‣ Información técnica ‣ Retroalimentación de transacción y seleccione las siguientes opciones:

- Los campos URL para Redireccionar HTTP en el navegador pueden quedarse vacíos, pues Odoo especificará estas URL para cada solicitud de transacción.
    
- Me gustaría recibir los parámetros de retroalimentación de las transacciones en las URL de redirección: debe estar seleccionado.
    
- Solicitud de servidor a servidor HTTP directa: debe estar establecido en `En línea pero cambiar a solicitud diferida cuando la solicitud en línea falle`.
    
- Ambos campos **URL** deben contener esta misma URL, reemplazando `<example>` por su base de datos: `https://<example>/payment/ogone/return`.
    
- Los parámetros dinámicos de comercio electrónico deben contener los siguientes valores: `ALIAS`, `AMOUNT`, `CARDNO`, `CN`, `CURRENCY`, `IP`, `NCERROR` `ORDERID`, `PAYID`, `PM`, `STATUS`, `TRXDATE`. Se pueden incluir otros parámetros (si tiene otra integración con Ogone que lo requiera), pero no es recomendable.
    
- En la sección Todos los modos de envío de transacciones, llene el campo de frase de contraseña **SHA-OUT** y desactive `Solicitud HTTP para cambio de estado`.
    

Para permitir que sus clientes guarden las credenciales de sus tarjetas de crédito para usarlas en el futuro, vaya a Configuración ‣ Alias ‣ Mi información de alias. Desde esta pestaña, puede configurar cómo es que el usuario puede guardar los detalles de su tarjeta, por cuánto timpo se guarda dicha información, si debe aparecer una casilla para guaradar la información de la tarjeta, etc.

## Ajustes en Odoo[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/ogone.html#settings-in-odoo "Enlazar permanentemente con este título")

Para configurar Ogone en Odoo, vaya a Contabilidad ‣ Configuración ‣ Proveedores de pago y abra el proveedor Ogone. En la pestaña Credenciales, ingrese el **PSPID** de su cuenta de Ogone, y llene los otros campos como están configurados en su [Portal de Ogone](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/ogone.html#ogone-ogone).