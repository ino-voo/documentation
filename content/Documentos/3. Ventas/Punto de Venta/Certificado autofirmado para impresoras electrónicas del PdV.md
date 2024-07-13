Es probable que algunos modelos de impresora que se pueden usar sin una [caja IoT](https://www.odoo.com/documentation/17.0/es/applications/general/iot/config/connect.html) necesiten un [protocolo HTTPS](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/https.html) para establecer una conexión segura entre el navegador y la impresora. Sin embargo, la mayoría de los navegadores le mostrarán una página de advertencia si intenta conectarse a la dirección IP de la impresora a través HTTPS. En ese caso, puede [forzar la conexión](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/epos_ssc.html#epos-ssc-instructions) de forma temporal, así podrá conectarse a la página HTTPS y usar una impresora ePOS con Odoo siempre y cuando no cierre la ventana del navegador.

 Advertencia

Si cierra la ventana del navegador se perderá la conexión. Por lo tanto, este método solo se debe usar como una **solución temporal** o como un requisito previo para las [siguientes instrucciones](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/epos_ssc.html#epos-ssc-instructions).

## Genere, exporte e importe certificados autofirmados.[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/epos_ssc.html#generate-export-and-import-self-signed-certificates "Enlazar permanentemente con este título")

Para obtener una solución a largo plazo debe generar un **certificado autofirmado**. Después, expórtelo e impórtelo a su navegador.

 Importante

Un certificado SSL solo se debería **generar una vez**. Si crea otro certificado, los dispositivos que usen el certificado previo perderán el acceso al HTTPS.

Windows 10 & Linux OSMac OSAndroid OSiOS

Generate a self-signed certificateExport a self-signed certificateImport a self-signed certificate

Navegue a la dirección IP de la impresora ePOS (p. ej. `https://192.168.1.25`) y haga clic en Avanzado y después en Proceeder a [dirección IP] (no es seguro) para forzar la conexión.

![página de advertencia sobre la privacidad de la conexión de Google Chrome](https://www.odoo.com/documentation/17.0/es/_images/browser-https-insecure.png)

Página de advertencia de Google Chrome en Windows 10[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/epos_ssc.html#id1 "Enlace permanente a esta imagen")

Después, use las credenciales de su impresora para ingresar a los ajustes de la impresora ePOS. Para iniciar sesión, ingrese `epson` en el campo ID y en el campo Contraseña ingrese el número de serie de la impresora.

Para generar un **certificado autofirmado** haga clic en Certificate list (lista de certificados) que se encuentra en la sección de Autenticación. El Common Name (nombre común) se debería de llenar de manera automática, pero si no es así ahí puede poner la dirección IP de la impresora. En el campo Validity Period (periodo de validez) ponga los años por los que el certificado será válido, haga clic en Create (crear) y restablezca o reinicie la impresora manualmente.

Ya se generó el el certificado autofirmado. Vuelva a cargar la página, vaya a la sección Security (seguridad) y haga clic en SSL/TLS para asegurarse de que el **certificado autofirmado** se seleccionó correctamente en la sección Server certificate (certificado del servidor).

 Importante

- Si necesita exportar certificados SSL desde un sistema operativo o un navegador que no hemos mencionado, busque `exportar certificado SSL` + `el nombre de su navegador o sistema operativo` en su motor de búsqueda preferido
    
- Es lo mismo si necesita importar certificados SSL desde un sistema operativo o navegador que no mencionamos, busque `exportar certificado SSL` + `el nombre de su navegador o sistema operativo` en su motor de búsqueda preferido.
    

## Revise si el certificado se importó correctamente[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/epos_ssc.html#check-if-the-certificate-was-imported-correctly "Enlazar permanentemente con este título")

Para confirmar que la conexión de su impresora es segura, conéctese a su dirección IP mediante HTTPS. Por ejemplo, vaya a `https://192.168.1.25` en su navegador. Si el certificado SSL se aplicó de forma correcta, entonces ya no debería aparecer la página de advertencia y en la barra de direcciones debería aparecer un icono de candado que indica que la conexión es segura.