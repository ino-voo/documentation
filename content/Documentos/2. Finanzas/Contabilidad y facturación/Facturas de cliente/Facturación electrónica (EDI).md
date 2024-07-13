EDI, o intercambio electrónico de datos, es la comunicación entre empresas de documentos empresariales, como órdenes de compra y facturas, en formato estándar. Si envía documentos que cumplen con el estándar EDI se podrá asegurar de que la máquina que reciba el mensaje podrá interpretar la información de manera correcta. Hay muchos formatos EDI que están disponibles dependiendo del país de su empresa.

La función EDI permite automatizar la administración entre empresas, además de que es posible que algunos gobiernos lo pidan para facilitar el control fiscal y la administración

Uno de los usos de EDI es que podrá crear facturas y notas de crédito en formato electrónico.

Los siguientes formatos, entre otros, son compatibles con Odoo.

|Nombre de Formato|Aplicación|
|---|---|
|Factur-X (CII)|Todos los clientes|
|Facturación Peppol BIS 3.0|Todos los clientes|
|XRechnung (UBL)|Todos los clientes|
|Fattura PA (IT)|Empresas italianas|
|CFDI (4.0)|Empresas mexicanas|
|Perú UBL 2.1|Empresas peruanas|
|SII IVA Llevanza de libros registro (ES)|Empresas españolas|
|UBL 2.1 (Colombia)|Empresas colombianas|
|Autoridad fiscal de Egipto|Empresas egipcias|
|E-Invoice (IN)|Empresas indias|
|NLCIUS (Países Bajos)|Empresas neerlandesas|
|EHF 3.0|Empresas noruegas|
|Facturación SG BIS 3.0|Empresas singapurenses|
|A-NZ BIS Billing 3.0|Todos los clientes|

 Nota

- El formato **Factur-X (CII)** permite realizar controles de validación en la factura y generar archivos compatibles con PDF/A-3.
    
- Cada PDF que genera Odoo incluye un archivo XML integrado **Factur-X**.
    

 Ver también

[Localizaciones fiscales](https://www.odoo.com/documentation/17.0/es/applications/finance/fiscal_localizations.html)

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/electronic_invoicing.html#configuration "Enlazar permanentemente con este título")

De forma predeterminada, el formato disponible en la [ventana de envío](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/electronic_invoicing.html#e-invoicing-generation) depende del país de su cliente.

Puede definir un formato de factura electrónica específico para cada cliente. Para ello, vaya a Contabilidad ‣ Clientes ‣ Clientes, abra el formulario correspondiente, vaya a la pestaña Contabilidad y seleccione el formato adecuado.

![Selección de un formato EDI para un cliente específico.](https://www.odoo.com/documentation/17.0/es/_images/customer-form.png)

### Facturación electrónica nacional[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/electronic_invoicing.html#national-electronic-invoicing "Enlazar permanentemente con este título")

Según el país de su empresa (por ejemplo, [Italia](https://www.odoo.com/documentation/17.0/es/applications/finance/fiscal_localizations/italy.html), [España](https://www.odoo.com/documentation/17.0/es/applications/finance/fiscal_localizations/spain.html), [México](https://www.odoo.com/documentation/17.0/es/applications/finance/fiscal_localizations/mexico.html), etc.), es posible que deba emitir sus facturas mediante documentos de facturación electrónica con un formato específico. En este caso, puede definir un formato predeterminado de facturación electrónica para su diario de ventas.

Para hacerlo, vaya a Contabilidad ‣ Configuración ‣ Diarios, abra su diario de ventas, diríjase a la pestaña Ajustes avanzados y habilite los formatos necesarios para este diario.

## Generar facturas electrónicas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/electronic_invoicing.html#e-invoices-generation "Enlazar permanentemente con este título")

Desde una factura confirmada, haga clic en Enviar e imprimir para abrir la ventana de envío, luego seleccione la opción de facturación electrónica para generar y adjuntar el archivo con la factura electrónica.

![La opción Peppol está seleccionada y el correo electrónico tiene un archivo XML de factura electrónica adjunto.](https://www.odoo.com/documentation/17.0/es/_images/send-window.png)

## Peppol[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/electronic_invoicing.html#peppol "Enlazar permanentemente con este título")

La red [Peppol](https://peppol.org/about/) garantiza el intercambio de documentos e información entre las empresas y las autoridades del gobierno. Se usa principalmente para la facturación electrónica y sus puntos de acceso (conectores a la red de Peppol) le permiten a las empresas intercambiar documentos electrónicos.

Ahora Odoo es un **punto de acceso** y un SMP, lo que permite realizar transacciones de facturación electrónica sin la necesidad de enviar facturas por correo electrónico o postal.

Si todavía no lo ha hecho, [instale](https://www.odoo.com/documentation/17.0/es/applications/general/apps_modules.html#general-install) el módulo Peppol (`account_peppol`).

 Importante

- Se puede registrar a Peppol **gratis** y desde Odoo Community
    
- Puede enviar **facturas a los clientes** y **notas de crédito** recibir **facturas de los proveedores** así como **reembolsos** con Peppol.
    
- Puede enviar uno de los siguientes formatos de documentos compatibles: **BIS Billing 3.0, XRechnung CIUS, NLCIUS**.
    
- Los siguientes **países** aplican para **registrarse en Peppol con Odoo**:
    
    Andorra, Albania, Austria, Bosnia y Herzegovina, Bélgica, Bulgaria, Suiza, Chipre, República Checa, Alemania, Dinamarca, Estonia, España, Finlandia, Francia, Reino Unido, Grecia, Croacia, Hungría, Irlanda, Islandia, Italia, Liechtenstein, Lituania, Luxemburgo, Letonia, Mónaco, Montenegro, Macedonia del Norte, Malta, Países bajos, Noruega, Polonia, Portugal, Rumania, Serbia, Suecia, Eslovenia, Eslovaquia, San Marino, Turquía, Santa Sede (Ciudad del Vaticano)
    

### Registro[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/electronic_invoicing.html#registration "Enlazar permanentemente con este título")

Vaya a Contabilidad ‣ Configuración ‣ Ajustes. Si no ha instalado el módulo Peppol, primero marque la casilla activar PEPPOL y después **guarde de manera manual**.

![Instalación del módulo de Peppol](https://www.odoo.com/documentation/17.0/es/_images/peppol-install.png)

Complete la siguiente información:

- EAS Peppol. Esta es el esquema de dirección electrónica de Peppol y normalmente depende del país de la empresa. Odoo llena los códigos de EAS más usados en su país. Por ejemplo, el código EAS preferido para la mayoría de empresas en Bélgica es 0208.
    
- Punto de conexión de Peppol. es el número de registro de una empresa o un número de IVA.
    
- Número de teléfono, incluyendo el código del país (por ejemplo, `+32` en Bélgica)
    
- Correo electrónico de primer contacto
    

 Ver también

- [Peppol EAS - Comisión Europea](https://ec.europa.eu/digital-building-blocks/wikis/display/DIGITAL/Code+lists/)
    
- [Punto de conexión Peppol - OpenPeppol eDEC lista de códigos](https://docs.peppol.eu/edelivery/codelists/) (abra los «esquemas de identificación de los participantes» como página HTML)
    

Si está en proceso de migración de otro punto de acceso, ingrese la Clave de migración del proveedor anterior.

![Configuración para peppol](https://www.odoo.com/documentation/17.0/es/_images/peppol-settings.png)

Finalmente, haga clic en Validar registro. Si quiere explorar más u obtener una demo de Peppol, puede elegir registrarse en el modo de demostración. De lo contrario, seleccione En vivo.

> ![Selección del modo demo para Peppol](https://www.odoo.com/documentation/17.0/es/_images/peppol-demo-mode.png)

 Nota

Al probar Peppol, el parámetro del sistema `account_peppol.edi.mode` puede cambiarse a `prueba`. Después, aparecerá un botón de radio con la opción de registrarse en el servidor de prueba.

![Parámetro de modo de prueba de Peppol](https://www.odoo.com/documentation/17.0/es/_images/peppol-system-parameter.png) ![Selección del modo de prueba de Peppol](https://www.odoo.com/documentation/17.0/es/_images/peppol-test-mode-settings.png)

Ahora puede solicitar un código de verificación que se le enviará cuando haga clic en verificar número de teléfono.

![solicitud de verificación de validación de teléfono](https://www.odoo.com/documentation/17.0/es/_images/peppol-registration-verify.png)

Se le enviará un mensaje de texto a su teléfono celular con el código para finalizar el proceso de verificación.

![validación del teléfono](https://www.odoo.com/documentation/17.0/es/_images/phone-registration.png)

Una vez que ingrese el código y haga clic en Confirmar podrá ver que aún necesita activar su registro. De aquí en adelante puede configurar el diario predeterminado en el que recibirá facturas de proveedores.

![aplicación pendiente](https://www.odoo.com/documentation/17.0/es/_images/peppol-registration-pending.png)

Debería activarse de forma automática en un solo día.

 Truco

También puede activar el cron de forma manual para revisar el estado de la reserva en Ajustes ‣ Técnicos ‣ Acciones programadas ‣ PEPPOL: actualizar el estado del participante.

El estado de su aplicación se actualizará en cuanto se haya registrado a la red de Peppol.

![aplicación activa](https://www.odoo.com/documentation/17.0/es/_images/peppol-registration-active.png)

Todas las facturas y facturas de proveedor se envían directamente usando la red de Peppol.

### Verificación de contactos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/electronic_invoicing.html#contact-verification "Enlazar permanentemente con este título")

Antes de enviar una factura a un contacto con la red Peppol, es necesario verificar que también están registrados como un participante en Peppol.

Para hacerlo, vaya a Contabilidad ‣ Clientes ‣ Clientes y abra el formulario del cliente. Después, vaya a la pestaña de contabilidad ‣ facturación electrónica, seleccione el formato correcto y asegúrese de que el código EAS de Peppol y el punto de conexión estén llenos. Haga clic en Verificar. Si el contacto existe en la red, la validez de su punto de conexión de Peppol será Válido.

![verifique el registro del contacto](https://www.odoo.com/documentation/17.0/es/_images/peppol-contact-verify.png)

 Importante

Odoo llena automáticamente tanto el código EAS como el número del punto de conexión según la información disponible para un contacto, es mejor confirmar estos detalles directamente en el contacto.

Puede verificar el estado de participación de Peppol de varios clientes a la vez. Para hacerlo, vaya a Contabilidad ‣ Clientes ‣ Clientes y cambie a vista de lista. Seleccione los contactos a los que quiere verificar y después haga clic en Acciones ‣ Verificar Peppol.

### Enviar facturas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/electronic_invoicing.html#send-invoices "Enlazar permanentemente con este título")

Una vez listo, para enviar una factura con la red Peppol solo haga clic en Enviar e imprimir que se encuentra en el formulario de la factura. Para preparar varias facturas, selecciónelas y después haga clic en Acciones ‣ Enviar e imprimir, se enviarán en lote más tarde. Tanto las casillas BIS Billing 3.0 como Enviar mediante PEPPOL deben estar marcadas.

![Enviar factura peppol](https://www.odoo.com/documentation/17.0/es/_images/peppol-send-print.png)

Las facturas publicadas que se pueden enviar mediante Peppol están marcadas como Listo para Peppol. Para mostrarlas, use el filtro Listo para Peppol o ingrese al tablero de Contabilidad y haga clic en Facturas listas para Peppol en el diario de ventas correspondiente.

![Filtrar las facturas listas para Peppol](https://www.odoo.com/documentation/17.0/es/_images/peppol-ready-invoices.png)

Una vez que las facturas se envíen a través de Peppol, el estatus cambiará a Procesando. El estado cambiará a `Listo` después de que las facturas se hayan entregado al punto a acceso del contacto.

![Estado del mensaje de Peppol](https://www.odoo.com/documentation/17.0/es/_images/peppol-message-processing.png)

 Truco

De forma predeterminada, la columna del estado de Peppol está oculta en la vista de lista de las facturas. Para visualizarla solo selecciónela en las columnas opcionales, a las que puede acceder desde la esquina superior derecha de la vista de lista de las facturas.

Un cron se ejecuta de forma regular para revisar el estado de estas facturas. Puede revisar el estado antes de que el cron se ejecute, solo tiene que hacer clic en Obtener el estado de las facturas de Peppol en el dierio de ventas correspondientes en el tablero de contabilidad.

![Obtener el estado de las facturas de Peppol](https://www.odoo.com/documentation/17.0/es/_images/peppol-fetch-message-status.png)

### Recibir las facturas de proveedor[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/electronic_invoicing.html#receive-vendor-bills "Enlazar permanentemente con este título")

Una vez al día, el cron revisa si hay documentos nuevos que se le hayan enviado a través de la red Peppol. Estos documentos se importan y las facturas de proveedor correspondientes se crean de forma automática en borradores.

![facturas recibidas de peppol](https://www.odoo.com/documentation/17.0/es/_images/peppol-receive-bills.png)

Si quiere recuperar los documentos Peppol antes de que el cron se ejecute, lo puede hacer desde el tablero de Contabilidad en el diario de compra principal de Peppol que configuró en los ajuistes. Solo haga clic en Obtener de Peppol.

![Obtener facturas desde Peppol](https://www.odoo.com/documentation/17.0/es/_images/peppol-fetch-bills.png)