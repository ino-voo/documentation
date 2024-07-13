Para anunciar un producto en eBay y Odoo, hay dos métodos en Odoo para hacerlo:

1. Cree un producto en Odoo y anúncielo en eBay (_método recomendado_).
    
    - Haga clic en Publicar artículo en eBay en el menú superior de la plantilla de producto. Puede acceder a la plantilla de producto desde la aplicación Ventas ‣ Productos ‣ Producto, luego deberá seleccionar uno.
        
2. Anuncie el artículo en eBay, luego cree el producto en Odoo y, por último, vincule el producto al artículo en eBay (_método no tan recomendado_).
    
    - Haga clic en Enlazar a un anuncio vigente de eBay en el menú superior de la plantilla de producto. Puede acceder a la plantilla de producto desde la aplicación Ventas ‣ Producto ‣ Producto, luego deberá seleccionar uno.
        

 Nota

Si recibe una orden y el anuncio de la orden no está vinculado a un producto, eBay creará un producto consumible en su lugar. Deberá modificar estos productos consumibles en la _orden de venta_ mientras estén en estado de borrador para representar un producto almacenable y luego el usuario podrá vincularlos al anuncio a medida que van llegando.

 Ver también

Para obtener más información relacionada al Conector de eBay puede visitar las siguientes páginas:

- [Configuración del Conector de eBay](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/setup.html)
    
- [Vincular anuncios existentes](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/linking_listings.html)
    
- [Solución de problemas del Conector de eBay](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html)
    

## Anunciar sin variantes[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/manage.html#listing-without-variation "Enlazar permanentemente con este título")

Acceda a la plantilla de producto desde la aplicación Ventas ‣ Productos ‣ Producto, luego seleccione el producto correspondiente.

Para anunciar un producto, seleccione el campo Vender en eBay en una plantilla de producto. La opción Vender en eBay está disponible en la pestaña eBay debajo del nombre del producto. Haga clic en Guardar si es necesario.

![El formulario de plantilla de eBay para anunciar el producto.](https://www.odoo.com/documentation/17.0/es/_images/manage-ebay-template.png)

When the Use Stock Quantity field is checked, the quantity set on eBay is the Odoo _Forecast Quantity_ (Odoo _Inventory_ app).

The policies need to be set in order to be able to list on eBay. A value must be selected for the following fields Payment Policy, Return Policy, and Shipping Policy. The options are imported from the eBay database. If no option appears, they can be imported by navigating to Sales app ‣ Configuration ‣ Settings ‣ eBay, and clicking on the Policies button in the Synchronization field. This button **only** appears once the production and sandbox credentials have been set.

The Description Template allows the administrator to use templates in listings. The default template only uses the eBay Description field of the product. HTML can be used inside the Description Template, and in the eBay Description in Odoo 14. Starting in Odoo 15, the powerbox feature is available to use in the template and description. Simply type a forward slash `/` to reveal a menu with formatting, layout, and text options. To add an image, type `/image`.

To use images in the listing, an image needs to be added as one of the _Attachments_ on the product template.

 Ver también

Para obtener más información sobre la configuración de plantillas en Odoo consulte [Plantillas de correo electrónico](https://www.odoo.com/documentation/17.0/es/applications/general/companies/email_template.html).

## Anunciar con variantes[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/manage.html#listing-with-variations "Enlazar permanentemente con este título")

El formulario de eBay será algo distinto si selecciona Vender en eBay en un producto que incluye variaciones con un precio fijo como Tipo de anuncio. Vaya a la pestaña Variantes o haga clic en Configurar variantes en el menú superior para configurar los ajustes correspondientes. Puede configurar precios distintos para cada variante.

Cuando cambia el Tipo de anuncio a precio fijo, Odoo muestra una tabla de variantes en la parte inferior de la pestaña eBay, allí puede ingresar el precio fijo y puede elegir si debe Publicar en eBay algunas variantes específicas, así como otras opciones.

![El tipo de anuncio de precio fijo en la pestaña de eBay en un formulario de producto en la aplicación Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/fixed-listing-price.png)

## Identificadores de productos[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/manage.html#product-identifiers "Enlazar permanentemente con este título")

Los identificadores de productos como EAN, UPC, marca o MPN son necesarios para la mayoría de las categorías de eBay.

### Identificadores EAN y UPC[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/manage.html#ean-and-upc-identifiers "Enlazar permanentemente con este título")

El módulo gestiona los identificadores EAN y UPC con el campo Código de barras de la variante del producto. Si el campo Código de barras está vacío o su valor no es válido, los valores de EAN y UPC se establecerán como “No aplica”, tal como eBay recomienda.

Los códigos de barras están disponibles en la plantilla del producto, en la pestaña Información general. Primero acceda a la plantilla del producto, vaya a la aplicación Ventas ‣ Productos ‣ Producto y seleccione el producto correspondiente.

### Anuncios con artículos específicos[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/manage.html#listing-with-item-specifics "Enlazar permanentemente con este título")

Para agregar especificaciones del artículo debe crear un atributo de producto con un solo valor en la pestaña Atributos y variantes en el formulario del producto. Los ejemplos de especificaciones del artículo incluyen `MPN` o `Marca`, pues estos valores funcionan como especificaciones del artículo. Debe definirlos en la pestaña Atributos y variantes en el formulario correspondiente. Si estos valores no están configurados, se utilizará “No aplica” para el anuncio de eBay.

## Procesar facturas y pagos[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/manage.html#process-invoices-and-payments "Enlazar permanentemente con este título")

### Registrar pagos[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/manage.html#posting-payment "Enlazar permanentemente con este título")

Cuando se realizan órdenes en eBay, estas siempre se pagan por adelantado a través de eBay. En ningún momento los usuarios pagarán artículos en eBay a través de Odoo. Por lo tanto, una vez las órdenes de sincronizan en Odoo desde eBay, ya están pagadas. Las funcionalidades de facturación y pago de Odoo no se utilizan, pero sí es necesario crear facturas y marcarlas como pagadas para «cerrar» la _orden de venta_.

Los usuarios pueden optar por crear y registrar facturas por lotes. Para hacerlo, vaya a Cotizaciones en la vista de lista desde la aplicación Ventas ‣ Órdenes ‣ Cotizaciones. Seleccione el icono de vista de lista que está ubicado en la esquina superior derecha, pase el cursor sobre los iconos para abrir el nombre de cada uno. Luego, seleccione las casillas a la izquierda para las cuales debe crear facturas y vaya al menú Acción o al ⚙️ [icono de engranaje]. Haga clic en Crear facturas.

Aparecerá una ventana emergente, allí haga clic en el botón Crear y ver factura, luego una nueva pantalla mostrará las facturas recién creadas. A continuación, selecciónelas todas haciendo clic en el icono de la casilla junto a Número en la fila de encabezado de la lista, esta acción seleccionará todos los registros. Luego, vaya al menú Acción y haga clic en Publicar asientos. Después de este paso aparecerá una ventana emergente, haga clic en Publicar asientos contables. Las facturas ya no estarán en estado de _borrador_ y se establecerán como _registradas_.

### Conciliar pagos[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/manage.html#reconciling-payments "Enlazar permanentemente con este título")

Por lo general, los usuarios utilizan PayPal para recibir pagos de eBay y luego enviarlos de PayPal a su cuenta bancaria. Para conciliar estos ingresos, los usuarios pueden conciliar la transferencia de PayPal con todas las facturas relacionadas.

Vaya al tablero de Contabilidad desde la aplicación Contabilidad ‣ Tablero ‣ Banco. Cree una nueva transacción y establezca la Etiqueta como `Ventas de eBay`. Complete el Importe e ingrese una fecha de estado de cuenta. Haga clic en Crear y editar.

Para el campo Saldo final, ingrese la misma cuenta que ingresó para el importe anterior y haga clic en Guardar. Después, abra el nuevo saldo que debe conciliarse y seleccione las entradas que se incluyen en este saldo en la pestaña marcada como Conciliar asientos existentes.

Después de agregar todos los asientos necesarios, haga clic en Validar para completar la conciliación. Para verificar el pago, vaya a Clientes ‣ Facturas y seleccione la factura correspondiente. La etiqueta _Pagado_ debería aparecer en la columna Estado de pago.

 Ver también

- [Solución de problemas del Conector de eBay](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/troubleshooting.html)
    
- [Vincular anuncios existentes](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/linking_listings.html)
    
- [Configuración del Conector de eBay](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/ebay_connector/setup.html)