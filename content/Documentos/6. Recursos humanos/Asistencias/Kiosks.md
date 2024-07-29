Odoo’s _Attendances_ app allows employees to check in and out of work directly from the database, or from a kiosk.

A kiosk is a [dedicated device](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/hardware.html) (a PC, tablet, or mobile phone) for employees to use when they check in and out.

Kiosks are needed for employees who do **not** have access to the database.

Only employees with access to the database can check in and out from the _Attendances_ app, and they are referred to as _users_.

 Importante

If employees [check in and out](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-kiosk-mode-entry) using a badge or an RFID, then an [accessible device](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/hardware.html) in [Kiosk Mode](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-kiosk-mode) **must** be available in order to use these two methods.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#configuration "Enlazar permanentemente con este título")

There are only a few configurations needed to use kiosks in the _Attendances_ application. Navigate to Attendances app ‣ Configuration to access the Settings page to configure the [Kiosk Mode section](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-kiosk-mode) and the [Kiosk Settings section](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-kiosk-settings).

Once all desired settings have been configured, click the Save button on the Settings page, to activate and enable them.

### Kiosk Mode section[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#kiosk-mode-section "Enlazar permanentemente con este título")

Using the drop-down menu, select how an employee checks in when using a kiosk. Options are Barcode/RFID, Barcode/RFID and Manual Selection, or Manual Selection.

 Nota

La aplicación _Código de barras_ **no** necesita estar instalada para usar las funciones de códigos de barras y RFID.

### Kiosk Settings section[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#kiosk-settings-section "Enlazar permanentemente con este título")

The various settings in the Kiosk Settings section determine how employees check in and out with kiosks.

- Barcode Source: this setting **only** appears if one of the two _Barcode/RFID_ selections were configured for the [Kiosk Mode](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-kiosk-mode) setting.
    
    If available, select how barcodes are scanned at the kiosk, via one of the drop-down menu options. Barcodes can be scanned with a dedicated Scanner, or with a device’s camera (Front Camera or Back Camera).
    
- Employee PIN Identification: tick this checkbox if employees should use a unique PIN to check in. PINs are configured on each individual employee record. Refer to the [new employee documentation](https://www.odoo.com/documentation/17.0/es/applications/hr/employees/new_employee.html#employees-hr-settings) documentation for more information on setting up PINs.
    
- Display Time: determine how many seconds a check-in/check-out confirmation message remains on the kiosk screen before returning to the main check in screen.
    
- Attendance Kiosk Url: Odoo generates a unique web address (URL) to use a device as a kiosk, without having to sign in to the Odoo database. When setting up a kiosk device, navigate to this unique web address in a web browser to present the _Attendances_ app kiosk.
    
     Importante
    
    These kiosk URLs are **not** secured with any type of access code. Anyone who has the URL can access the _Attendances_ app kiosk. If the URL is compromised for any reason, such as in the event of a security breach, click Generate a new Kiosk Mode URL, located beneath the link, to generate a new URL, and update the kiosk, accordingly.
    

## Modo de quiosco[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#kiosk-mode "Enlazar permanentemente con este título")

Entering _Kiosk Mode_ is **only** available for users with specific [access rights](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances.html#attendances-access-rights).

_Kiosk Mode_ can be activated in two different ways:

1. Navigate to the Attendances app, and click Kiosk Mode in the top menu. The device then signs out of Odoo and enters _Kiosk Mode_.
    
2. Navigate to the Attendances app ‣ Configuration. In the Kiosk Settings section, use the link in the Attendance Kiosk Url field to open _Kiosk Mode_ on any device.
    

![El campo URL del quiosco de asistencia en la sección de ajustes de la aplicación Asistencias.](https://www.odoo.com/documentation/17.0/es/_images/kiosk-url.png)

As a security measure, once a device is in _Kiosk Mode_, it is not possible to go back into the database without signing back in.

 Nota

At any time, a new kiosk URL can be generated, if needed. Click the  Generate a new Kiosk Mode URL

To exit _Kiosk Mode_, just close the tab in the web browser or return to the main log-in screen of Odoo.

## Check in and out with a kiosk[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#check-in-and-out-with-a-kiosk "Enlazar permanentemente con este título")

### Pase[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#badge "Enlazar permanentemente con este título")

To check in or out using a badge, tap the  Tap to scan image in the center of the kiosk.

![La vista del quiosco de asistencia con la imagen para escanear una identificación.](https://www.odoo.com/documentation/17.0/es/_images/scan-badge.png)

Then, scan the barcode on the badge using the method configured in the [Kiosk Settings](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-kiosk-settings) section of the configuration menu.

Once the barcode is scanned, the employee is checked in or out, and a [confirmation message](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-confirmation) appears with all the information.

### RFID[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#rfid "Enlazar permanentemente con este título")

To check in or out using an RFID key fob, simply scan the fob with an RFID reader.

Once scanned, the employee is either checked in or checked out, and a [confirmation message](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-confirmation) appears with all the information.

### Manualmente[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#manually "Enlazar permanentemente con este título")

Users who do not have a scannable badge, or an RFID fob, can manually check in and out at a kiosk.

Tap the Identify Manually button on the kiosk, and a screen appears with all the employees that can be checked in or out. The _Employees_ application dashboard has the same display.

Tap on a person to check them in or out, and a [confirmation message](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-confirmation) appears.

There are two ways to quickly find a specific person:

- Search…: tap on the Search… field, and enter the desired person’s name. As the name is typed in, the matching results are displayed on the screen.
    
- Department: tap on any desired selection in the Department section, located on the left-side of the screen, to **only** view employees from that specific department. The number at the end of each listed Department represents how many employees that department has.
    

#### NIP[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#pin "Enlazar permanentemente con este título")

If the Employee PIN Identification checkbox was ticked in the [Kiosk Settings](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-kiosk-settings) section of the configuration menu, the employee is prompted to enter a PIN when manually checking in or out.

Un teclado numérico con un mensaje aparece después de seleccionar al empleado. Al registrar la entrada aparece el mensaje (Empleado) ¡Le damos la bienvenida! Ingrese su PIN para registrar entrada arriba de los números. Al registrar la salida aparece el mensaje (Empleado) ¿Desea registrar su salida? Ingrese su PIN para registrar salida arriba de los números.

Ingrese el PIN con el teclado numérico y luego toque OK cuando haya terminado, se registrará la entrada o salida del empleado y aparecerá un [mensaje de confirmación](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-confirmation).

![La ventana emergente que aparece cuando se le pide que proporcione el NIP.](https://www.odoo.com/documentation/17.0/es/_images/enter-pin.png)

### Mensaje de confirmación[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#confirmation-message "Enlazar permanentemente con este título")

When an employee checks in or out, a confirmation message appears, with all the check in or check out information. When checking in, a welcome message appears, as well as the date and time of check in.

An Hours Previously Today: HH:MM field also appears, displaying any time that has already been logged for that employee for the day. If no time has been logged, the value displayed is: `00:00`. Beneath the message is an OK button.

To exit the screen before the preset time in the kiosk, tap the OK button.

Al registrar la salida, la pantalla muestra un mensaje de despedida con la fecha y la hora, así como las horas totales registradas para el día. Abajo del mensaje se encuentra el botón Hasta pronto. Para salir de la pantalla antes del tiempo preestablecido, toque el botón Hasta pronto.

![El mensaje de despedida con toda la información relacionada a la salida del empleado.](https://www.odoo.com/documentation/17.0/es/_images/goodbye-message.png)