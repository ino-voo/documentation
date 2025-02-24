Las personas físicas y morales a menudo usan direcciones separadas para facturar y para los envíos. Con la aplicación _Ventas_ de Odoo, los contactos pueden tener direcciones específicas para los envíos y para la facturación.

## Ajustes[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/different_addresses.html#settings "Enlazar permanentemente con este título")

Para utilizar correctamente varias direcciones en Odoo, vaya a la aplicación Ventas ‣ Configuración ‣ Ajustes y desplácese hacia abajo hasta el encabezado Cotización y órdenes. A continuación, marque la casilla junto a Direcciones de clientes, y haga clic en Guardar.

![Active la función Direcciones de clientes](https://www.odoo.com/documentation/17.0/es/_images/customer-addresses-setting.png)

## Configuración del formulario del contacto[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/different_addresses.html#contact-form-configuration "Enlazar permanentemente con este título")

Para añadir varias direcciones a un contacto, vaya a la aplicación Ventas ‣ Órdenes ‣ Clientes, y borre cualquier filtro predeterminado de la barra de búsqueda. Después haga clic en el cliente deseado para abrir su formulario de contacto.

 Truco

También puede acceder al formulario del contacto desde la aplicación _Contactos_.

En el formulario de contacto, haga clic en Editar y, a continuación, seleccione Añadir, ubicado en la pestaña Contactos y direcciones. Al hacerlo, aparecerá el formulario emergente Crear contacto, en el que podrá establecer direcciones adicionales.

![Agregar contacto/dirección al formulario de contacto.](https://www.odoo.com/documentation/17.0/es/_images/contact-form-add-address1.png)

En el formulario emergente Crear contacto, haga clic en el campo predeterminado Otra dirección para ver el menú desplegable con opciones relacionadas a las direcciones.

Seleccione una de las siguientes opciones:

- Contacto: añade otro contacto al formulario existente del contacto.
    
- Dirección de factura: añade una dirección de factura específica al formulario existente de contacto.
    
- Dirección de entrega: añade una dirección de entrega específica al formulario existente de contacto.
    
- Otra dirección: añade una dirección de entrega alterna al formulario existente de contacto.
    
- Dirección privada: añade una dirección privada al formulario de contacto existente.
    

Una vez que seleccione una opción deberá introducir la información de contacto correspondiente que debe utilizarse para el tipo de dirección específica.

![Cree un nuevo contacto/dirección en el formulario de contacto.](https://www.odoo.com/documentation/17.0/es/_images/create-contact-window1.png)

A continuación, haga clic en Guardar y cerrar para guardar la dirección y cerrar la ventana Crear contacto. O haga clic en Guardar y nuevo para guardar la dirección e introducir una nueva inmediatamente.

## Dirección añadida a la cotización[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/different_addresses.html#address-added-to-quotations "Enlazar permanentemente con este título")

Cuando añada un cliente a una cotización, los campos Dirección de factura y Dirección de entrega se completarán de manera automática con las direcciones correspondientes especificadas en el formulario de contacto del cliente.

![Las direcciones de facturación y de envío se completan automáticamente en una cotización.](https://www.odoo.com/documentation/17.0/es/_images/quotation-address-autopopulate.png)

La Dirección de facturación y la Dirección de envío también se pueden editar directamente desde la cotización al hacer clic en el botón de Editar y después en los botones de enlaces internos ➡️ (right arrow) que se encuentran junto a cada línea de dirección.

Estas direcciones se pueden actualizar en cualquier momento para asegurar una facturación y un envío adecuados.

 Truco

Si realiza algún cambio en un formulario en Odoo, incluidos los formularios de _contacto_, recuerde hacer clic en Guardar para guardar los cambios en la base de datos.