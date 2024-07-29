Employees who are **not** database users, and therefore, do **not** have access to the _Attendances_ app, must sign in and out of work using a kiosk. The following are the physical requirements for setting up a kiosk.

## Kiosk devices[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/hardware.html#kiosk-devices "Enlazar permanentemente con este título")

A kiosk is a self-service station, where employees can [check in and out of work](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-kiosk-mode-entry) with either a [badge](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/hardware.html#attendances-hardware-badges) or an [RFID key fob](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/hardware.html#attendances-hardware-rfid). Typically, these devices are dedicated as kiosks only, but any device with an internet browser is able to be set up as a kiosk.

A kiosk is used by navigating to the webpage specified in the [configuration](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/kiosks.html#attendances-kiosk-settings) section of the _Attendances_ app.

Kiosks are set up using one of the following types of devices:

- Laptop or Desktop computer
    
- Tablet
    
- Mobile phone (Android or iOS)
    

 Truco

Touchscreens are easy to use, and tablets and mobile phones take up less space. That’s why most consider using a smaller device with a touchscreen as a kiosk.

It is recommended to place kiosks on a secure stand, or mount them securely on a wall.

## Badges[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/hardware.html#badges "Enlazar permanentemente con este título")

Badges are a way for employees to quickly sign in and out from a kiosk, as badges are scanned by the kiosk’s camera to quickly identify the employee.

To generate a badge, first navigate to the Employees app. Next, click on the desired employee card to open the employee’s form, then click the HR Settings tab.

Under the ATTENDANCE/POINT OF SALE/MANUFACTURING section, there is a Badge ID field. If this field is blank, click Generate at the end of the Badge ID line, and the field is automatically populated with a new badge ID number. Then, click Print Badge at the end of the badge ID number to create a PDF file of the badge.

If a badge ID number is already present on the employee form, there is no Generate button, only a Print Badge button.

The employee’s badge contains the employee’s photo, name, job position, company logo, and a barcode that can be scanned at a kiosk to check in and out.

Badges can be printed for employees using any thermal or inkjet printer.

![A badge for an employee that is created from the Employees app.](https://www.odoo.com/documentation/17.0/es/_images/badge.png)

 Nota

Badges are **not** required, as employees can manually identify themselves on the kiosk.

### Lectores de código de barras[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/hardware.html#barcode-scanners "Enlazar permanentemente con este título")

When using badges to check in and out, the barcode **must** be scanned to identify the employee. This can be done with the kiosk’s camera, if one is available on the device.

If a camera is **not** available on the kiosk device, an external barcode scanner must be used to scan badges.

Kiosks work with most USB barcode scanners. Bluetooth barcode scanners are also supported for devices without USB ports, or if a wireless connection is desired.

Follow the manufacturer’s instructions on the barcode scanner to properly connect the barcode scanner to the kiosk device.

 Truco

If the barcode scanner is connected directly to a computer, it [must be configured](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html) to use the computer’s keyboard layout.

 Nota

An IoT box is **not** required to use a barcode scanner.

## Lectores de llaveros RFID[](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/hardware.html#rfid-key-fob-readers "Enlazar permanentemente con este título")

Instead of using a [badge](https://www.odoo.com/documentation/17.0/es/applications/hr/attendances/hardware.html#attendances-hardware-badges), employees can scan a personal RFID key fob with an RFID reader to check in and out of work.

It is **required** to purchase _both_ RFID key fobs and an RFID reader to use this method to check in and out. Follow the manufacturer’s directions to install the RFID reader, and set up the RFID key fob.

![An RFID key fob is placed on an RFID reader.](https://www.odoo.com/documentation/17.0/es/_images/rfid-reader.jpg)

 Truco

A recommended RFID reader is the [Neuftech USB RFID Reader](https://neuftech.net/Neuftech-USB-RFID-Reader-ID-Kartenleseger%C3%A4t-Kartenleser-Kontaktlos-Card-Reader-f%C3%BCr-EM4100).

 Nota

An IoT box is **not** required to use RFID key fobs.