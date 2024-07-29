Configure el conector de envíos _Bpost_ en Odoo para gestionar envíos de Bpost a clientes sin tener que salir de Odoo. Para configurarlo complete los siguientes pasos:

1. Cree una cuenta Bpost.
    
2. Obtenga el [Account ID and passphrase](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/bpost.html#inventory-shipping-bpost-account) (ID de la cuenta y códigos).
    
3. Configure el método de envío en Odoo.
    

Al terminar, es posible calcular el costo del envío, según el tamaño y peso del paquete, además de que los cargos se aplicarán directamente a la cuenta empresarial de Bpost y podrá imprimir las etiquetas de rastreo de Bpost directamente con Odoo.

 Ver también

- [Transportistas externos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html)
    
- [Métodos de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/delivery_method.html)
    
- [¿Cómo obtener las credenciales de DHL para la integración con Odoo?](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/dhl_credentials.html)
    
- [Integración de UPS](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html)
    

## Configuración de la cuenta de Bpost[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/bpost.html#bpost-account-setup "Enlazar permanentemente con este título")

Primero, vaya al [sitio web de Bpost](https://parcel.bpost.be/en/home/business) para crear o iniciar sesión en la cuenta empresarial de Bpost. Al crear la cuenta Bpost debe tener a la mano el número de identificación fiscal y el número de teléfono de la empresa a la mano

Follow the website’s steps to complete registration, and sign up for shipping services. Doing so submits a request to enter a contractual business relationship between the company and Bpost.

 Importante

Odoo **cannot** be integrated with [non-business Bpost](https://bpost.freshdesk.com/support/solutions/articles/174847-account-id-and-passphrase) accounts.

Después de completar la configuración, obtenga el ID y el código dela cuenta de Bpost en Shipping Manager (gestor de envío).

En la página Gestor de envío vaya a la pestaña Admin y luego a la pestaña General Settings (ajustes generales) para encontrar el Account ID (ID de la cuenta) y la Passphrase (contraseña) necesarias para configurar el método de envío de Odoo.

![En la pestaña *Admin* puede ver el ID de la cuenta y la contraseña.](https://www.odoo.com/documentation/17.0/es/_images/credentials.png)

## Configure el método de envío Bpost[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/bpost.html#configure-bpost-shipping-method "Enlazar permanentemente con este título")

Una vez que tenga sus credenciales, configure el método de envío Bpost en Odoo. Vaya a Inventario ‣ Configuración ‣ Métodos de envío.

En la página de métodos de envío haga clic en el botón Crear.

En el campo Proveedor seleccione Bpost con el menú desplegable. De esta manera podrá ver la pestaña Configuración de Bpost en la parte inferior del formulario, donde podrá ingresar las credenciales de Bpost.

Para más detalles sobre la configuración de otros campos en el método de envío, como Producto de envío, consulte la documentación [Configurar transportista externo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html).

 Nota

Para generar [etiquetas de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html) de Bpost con Odoo, debe asegurarse de que la opción Nivel de integración sea Obtener tarifas y crear envíos.

Complete los siguientes campos en la pestaña Configuración de Bpost:

- Número de cuenta de Bpost (campo obligatorio): ingrese el [account ID](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/bpost.html#inventory-shipping-bpost-account) (id de la cuenta) único de la empresa que obtuvo del sitio web de Bpost.
    
- Contraseña (campo obligatorio): ingrese la [passphrase](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/bpost.html#inventory-shipping-bpost-account) (contraseña) única de la empresa que obtuvo del sitio web de Bpost.
    
- Tipo de entrega de Bpost: seleccione los servicios de envío, ya sea Local o Internacional. Al seleccionar Local se mostrará la sección Opciones, mientras que Internacional activa los campos Tipo de envío Bpost y Instrucciones de devolución de paquete Bpost.
    
- Tipo de paquete Bpost: seleccione el tipo de servicio de envío desde el menú desplegable.
    
    Para [entregas locales](https://help.shipmondo.com/en/articles/6092265-bpost-belgium-parcel-types-and-requirements), las opciones son: bpack 24h Pro, bpack 24h business, o bpack Bus.
    
    Para [entregas internacionales](https://www.bpost.be/en/business-parcels-send/international), las opciones son: bpack World Express Pro, bpack World Business, o bpack Europe Business.
    
- :guilabel:` Tipo de envío Bpost` (campo obligatorio): para envíos internacionales, declare el tipo de bienes en el paquete como MUESTRA, REGALO, PRODUCTOS, DOCUMENTOS u OTRO.
    
- Dirección de devolución de paquete Bpost: dirección de devolución para cuando un envío internacional no se pueda entregar. Desde el menú desplegable seleccione: Destruir, Devolver al remitente por aire, o Devolver al remitente por carretera.
    
- Tipo de etiqueta: seleccione los tamaños de etiqueta A6 o A4 desde el menú desplegable.
    
- Formato de la etiqueta: seleccione PDF o PNG dese el menú desplegable.
    

Para entregas domésticas, estas funciones están disponibles en la sección Opciones:

- Active la función Entrega el sábado para incluir los días sábados como fechas de entrega posibles. Según el Tipo de paquete Bpost seleccionado esta opción puede significar costos adicionales para la empresa.
    
- Active la función Generar etiqueta de devolución para imprimir una etiqueta de devolución de forma automática después de validar la orden de entrega.
    

![Mostrar el método de envío Bpost.](https://www.odoo.com/documentation/17.0/es/_images/bpost.png)