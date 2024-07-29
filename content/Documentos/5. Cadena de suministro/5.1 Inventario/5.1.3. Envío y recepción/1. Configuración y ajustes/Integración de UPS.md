UPS es un servicio transportista que se integra con Odoo ara coordinar envíos a todas las regiones. Después de integrarlo, los usuarios pueden crear métodos de envío que calculen su costo y [generar etiquetas](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html).

 Ver también

[Transportistas externos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html)

Complete estos pasos para configurar el conector de envío de UPS en Odoo:

1. Cree una cuenta de UPS para obtener un [número de cuenta](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#inventory-shipping-receiving-ups-account-number).
    
2. Cree una cuenta de desarrollador de UPS para obtener [credenciales de cliente](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#inventory-shipping-receiving-ups-client-id).
    
3. Configure un método de envío en Odoo.
    

## Configuración de la cuenta de UPS[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#ups-account-setup "Enlazar permanentemente con este título")

Para comenzar, vaya al [sitio web de UPS](https://www.ups.com/) y haga clic en el botón Iniciar sesión ubicado en la esquina superior derecha para iniciar sesión o crear una cuenta de UPS.

Después de iniciar sesión, haga clic en el icono de perfil ubicado en la esquina superior derecha y seleccione la opción Cuentas y pagos del menú desplegable.

![Visualización de los pasos para dirigirse a la página "Cuentas y pagos" desde la página de inicio.](https://www.odoo.com/documentation/17.0/es/_images/accounts-payment.png)

En la página Cuentas y opciones de pago deberá configurar dos cuentas: una cuenta de envío de Odoo y una tarjeta de pago.

### Cuenta de envío[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#shipping-account "Enlazar permanentemente con este título")

Para agregar una cuenta de envío de Odoo, seleccione Agregar una nueva cuenta en el menú desplegable de Agregar un método de pago y haga clic en Agregar.

![Visualización de la opción "Agregar una cuenta" en el menú desplegable.](https://www.odoo.com/documentation/17.0/es/_images/new-account.png)

En la pantalla que tiene como nombre Abrir una cuenta de envío complete los formularios para configurar el tipo de cuenta de envío (por ejemplo, Comercial) y si enviará cualquier artículo regulado. Después complete los tres pasos restantes en el asistente, Añadir direcciones, Verifique su identidad y Explorar descuentos, este último paso es opcional.

Una vez que haya completado las secciones anteriores, envíe el formulario en la última página del asistente para terminar de configurar la cuenta de envío.

![Visualización del formulario de UPS en donde es necesario completar la información de envío de la empresa.](https://www.odoo.com/documentation/17.0/es/_images/shipping-account.png)

### Obtener un número de cuenta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#get-account-number "Enlazar permanentemente con este título")

El número de cuenta de UPS estará disponible una vez que configure la cuenta de envío. Para acceder a este, vaya a Perfil ‣ Cuentas y pagos y diríjase al campo del número de la cuenta.

![Visualización del campo del número de cuenta de la cuenta de envío.](https://www.odoo.com/documentation/17.0/es/_images/account-number.png)

### Tarjeta de pago[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#payment-card "Enlazar permanentemente con este título")

Regrese a la página Cuentas y pagos y seleccione la opción Agregar tarjeta de pago en el menú desplegable Agregar un método de pago, después complete el formulario para agregar la información de su tarjeta de crédito.

![Visualización de la opción "Agregar tarjeta de pago" en el menú desplegable.](https://www.odoo.com/documentation/17.0/es/_images/payment-card.png)

## Configuración de la cuenta de desarrollador de UPS[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#ups-developer-account-setup "Enlazar permanentemente con este título")

Inicie sesión en su [cuenta de desarrollador de UPS](http://developer.ups.com/) para generar la clave de desarrollador. Primero haga clic en el icono de perfil ubicado en la esquina superior derecha y seleccione la opción Aplicaciones del menú desplegable.

![Visualización de la opción "Aplicaciones" en el menú desplegable después de hacer clic en el icono de perfil.](https://www.odoo.com/documentation/17.0/es/_images/apps.png)

### Agregar la aplicación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#add-app "Enlazar permanentemente con este título")

Después, haga clic en el botón Agregar aplicaciones para completar el formulario correspondiente. En el campo Necesito credenciales API porque * seleccione la opción Quiero integrar la tecnología de UPS en mi negocio.

En la siguiente sección, Elija una cuenta para asociar con estas credenciales. *, seleccione Agregar cuenta existente en el menú desplegable del campo correspondiente y luego seleccione el [número de cuenta](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#inventory-shipping-receiving-ups-account-number) vinculado a la cuenta de UPS creada en el paso anterior.

![Visualización del formulario para completar el número de cuenta de UPS.](https://www.odoo.com/documentation/17.0/es/_images/developer-account-setup.png)

Haga clic en Suguiente y complete los campos del formulario Añadir aplicación:

- Nombre de la aplicación: escriba el nombre con el que identificará la aplicación.
    
- URL de devolución de llamada: escriba la URL de la base de datos de Odoo con el formato `https://nombredelabasededatos.odoo.com`. **No** incluya `www` en la URL.
    

En la sección Agregar productos ubicada a la derecha, busque y haga clic en el icono + (más) para agregar los siguientes productos a la aplicación:

- Autorización (OAuth): se utiliza para generar el token de autorización para solicitar información de la API de UPS.
    
- Validación de direcciones: valida direcciones a nivel de calle en Estados Unidos y Puerto Rico.
    
- Localizador: habilita la búsqueda de ubicaciones de envío de UPS según el tipo y los servicios disponibles.
    
- Documentos sin papel: permite subir imágenes de documentos para vincularlas a los envíos.
    
- Envío: habilita los servicios de envío de UPS, como preparar paquetes para su envío, gestionar devoluciones y cancelar envíos programados.
    
- Calificación: compara servicios de entrega y tarifas de envío.
    

Por último, haga clic en Guardar para aceptar los términos y condiciones de UPS.

 Ver también

[Catálogo de API de UPS](https://developer.ups.com/catalog?loc=en_US)

![Visualización del formulario "Agregar aplicaciones", en él se configuran los detalles de la aplicación.](https://www.odoo.com/documentation/17.0/es/_images/add-app-development.png)

### ID y secreto del cliente[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#client-id-and-client-secret "Enlazar permanentemente con este título")

Una vez que haya creado la nueva aplicación, vaya a Perfil ‣ Mis aplicaciones ‣ Aplicación y seleccione la aplicación en la sección Credenciales para ver las credenciales de UPS.

![Visualización de la aplicación recién creada en la sección "Mis aplicaciones".](https://www.odoo.com/documentation/17.0/es/_images/my-apps.png)

En la sección Credenciales, copie el ID del cliente y la llave del secreto del cliente.

![Visualización del "ID del cliente" y la clave del "secreto del cliente".](https://www.odoo.com/documentation/17.0/es/_images/credentials1.png)

## Configuración en Odoo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#setup-in-odoo "Enlazar permanentemente con este título")

Una vez que tenga sus credenciales, configure el método de envío en Odoo. Vaya a Inventario ‣ Configuración ‣ Métodos de envío.

En la página de métodos de envío haga clic en el botón Nuevo.

 Nota

Para los métodos de envío de UPS existentes que tengan a UPS heredado u obsoleto como proveedor, archívelos y cree un nuevo método de envío con UPS.

Seleccione UPS en el campo Proveedor, esta acción hará que aparezca la pestaña Configuración de UPS en la que deberá completar varios campos. Consulte la documentación [Configurar transportista de terceros](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html) para obtener instrucciones detalladas sobre la configuración de los otros campos del método de envío.

Complete los siguientes campos en la pestaña Configuración de UPS:

- Número de cuenta de UPS: (_obligatorio_) obtenga el [número de cuenta](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#inventory-shipping-receiving-ups-account-number) del portal de UPS.
    
- ID de cliente de UPS: (_obligatorio_) obtenga el [ID de cliente](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#inventory-shipping-receiving-ups-client-id) del sitio web de desarrolladores de UPS.
    
- Secreto de cliente de UPS: (_obligatorio_) obtenga el [secreto de cliente](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html#inventory-shipping-receiving-ups-client-id) del sitio web de desarrolladores de UPS.
    
- Tipo de servicio de UPS: seleccione el tipo de servicio de envío en el menú desplegable.
    
- Tipo de paquete de UPS: (_obligatorio_) seleccione con el menú desplegable el [tipo de paquete](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/package.html) que es compatible con el servicio de envío.
    
- Unidad de peso del paquete: la unidad de medida para el peso del paquete.
    
- Unidad de peso del paquete: la unidad de medida para las dimensiones del paquete.
    
- Formato de la etiqueta: elija el formato de las etiquetas de envío, las opciones son PDF, ZPL, EPL o SPL.
    

![Visualización de la pestaña "Configuración de UPS" en el formulario de métodos de envío.](https://www.odoo.com/documentation/17.0/es/_images/ups-configuration.png)

Las siguientes funciones están disponibles en la sección Opciones:

- Facturar mi cuenta: haga el cobro en la cuenta de UPS del usuario por el envío en la aplicación _Comercio electrónico_.
    
- Pago a contraentrega: cóbrele el envío a los clientes después de realizar la entrega.
    
- Generar etiqueta de devolución: imprima la etiqueta de devolución de la orden luego de validar la orden de entrega.
    
- Impuestos pagados por: seleccione si el remitente o el destinatario de la orden debe pagar los impuestos u otros gastos.