En Odoo es posible imprimir de forma automática los documentos y etiquetas PDF relacionados con la entrega. Estos incluyen detalles sobre el destinatario del paquete, su contenido o las instrucciones de manejo.

Es posible configurar los siguientes archivos PDF para que se impriman al validar una operación de _inventario_ (por ejemplo, recepción, recolección, órdenes de entrega, verificaciones de calidad):

1. [Recibo de entrega](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-delivery-slip)
    
2. [Recibo de devolución](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-return-slip)
    
3. [Etiquetas de producto de los artículos en la orden](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-product-labels)
    
4. [Etiquetas de número de serie y lote](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-lot-sn-labels)
    
5. [Etiquetas de transportistas](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-carrier-labels)
    
6. [Documentos de exportación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-export-doc)
    
7. [Contenido del paquete](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-package-content)
    
8. [Etiqueta del](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-package-label)
    

Para imprimir estos formularios en automático, vaya a Inventario ‣ Configuración ‣ Tipos de operaciones y seleccione el tipo adecuado.

En la pestaña Hardware, seleccione las casillas de las opciones deseadas en la sección Imprimir al validar. Esta acción descargará en automático los archivos PDF de los documentos seleccionados después de validar el tipo de operación. Vaya a la sección relacionada con cada una de las opciones disponibles en las casillas para obtener más detalles.

![Mostrar la opción *Imprimir al validar* en el *tipo de operación* de "recolección".](https://www.odoo.com/documentation/17.0/es/_images/print-on-validation.png)

## Recibo de entrega[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#delivery-slip "Enlazar permanentemente con este título")

Un _recibo de entrega_ incluye los detalles del destinatario y del paquete, por lo general se coloca dentro (o adjunto al) del paquete.

 Ver también

- [Lista de recolección](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/advanced_operations_warehouse/batch_transfers.html#inventory-warehouses-storage-barcode-picking)
    
- [Etiqueta de rastreo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html)
    

Después de [habilitar los ajustes del recibo de entrega](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-print-setup) en las opciones de configuración de la pestaña Hardware, se descargará el PDF correspondiente al hacer clic en Validar en el tipo de operación deseado.

En el recibo de entrega aparecen los productos, las cantidades, el número de referencia de la orden de entrega y el peso total de la orden.

![Recibo de entrega de ejemplo.](https://www.odoo.com/documentation/17.0/es/_images/delivery-slip.png)

## Recibo de devolución[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#return-slip "Enlazar permanentemente con este título")

Imprima los _recibos de devolución_ para incluirlos en los paquetes que los clientes podrían devolver, estos identifican la devolución, se vinculan a la orden de venta e incluyen detalles relacionados con los artículos y la información del cliente. También pueden incluir instrucciones específicas para que el cliente haga una devolución.

Después de [habilitar los ajustes del recibo de devolución](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-print-setup) en las opciones de configuración de la pestaña Hardware, se descargará el PDF correspondiente al hacer clic en Validar en el tipo de operación deseado.

En el recibo de devolución aparece la dirección de devolución de la empresa, así como los códigos de barras de la orden y la operación de devolución.

![Recibo de devolución de ejemplo.](https://www.odoo.com/documentation/17.0/es/_images/return-slip.png)

## Etiquetas de producto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#product-labels "Enlazar permanentemente con este título")

Imprima _etiquetas de producto_ para pegarlas a los artículos de una orden. Estas proporcionan información importante como el nombre del producto, código de barras y precio.

Después de ir al tipo de operación deseado (Inventario ‣ Configuración ‣ Tipos de operaciones), vaya a la pestaña Hardware y seleccione la opción Etiquetas de producto.

Al hacer esto aparece el menú desplegable Imprimir etiquetas como: en el que puede elegir cómo imprimir cada una. Están disponibles las siguientes opciones:

- 2 x 7 con precio: el PDF muestra el nombre del producto, el código de barras y el precio. La tabla corresponde a dos filas y siete columnas de etiquetas de productos por página.
    
    Example 2 x 7
    
- 4 x 7 con precio: el PDF muestra el nombre del producto, el código de barras y el precio. La tabla corresponde a cuatro filas y siete columnas de etiquetas de productos por página.
    
    Example 4 x 7
    
- 4 x 12: el PDF muestra el nombre del producto y el código de barras. La tabla corresponde a cuatro filas y doce columnas de etiquetas de productos por página.
    
    Example 4 x 12
    
- 4 x 12 con precio: el PDF muestra el nombre del producto, el código de barras y el precio. La tabla corresponde a cuatro filas y doce columnas de etiquetas de productos por página.
    
- Etiquetas ZPL: imprime etiquetas en el lenguaje de programación Zebra (ZPL) e incluyen el nombre del producto y el código de barras. Es legible para que las impresoras Zebra impriman las etiquetas en automático.
    
- Etiquetas ZPL con precio: imprime etiquetas en ZPL e incluyen el nombre del producto, el código de barras y el precio.
    

 Nota

Es posible imprimir las etiquetas de los productos de forma manual desde cualquier orden de entrega al hacer clic en el botón Imprimir etiquetas.

## Etiquetas de número de serie/lote[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#lot-sn-labels "Enlazar permanentemente con este título")

Imprima _etiquetas de número de serie o lote_ para pegarlas a los artículos de una orden. Estas proporcionan información importante como el nombre del producto, número de serie o lote y código de barras.

Para imprimir este PDF de forma automática, vaya a la página de opciones del tipo de operación deseado (Inventario ‣ Configuración ‣ Tipos de operaciones). Busque la pestaña Hardware y seleccione la opción Etiquetas de número de serie/lote.

Al hacer esto aparece el menú desplegable Imprimir etiquetas como: en el que puede elegir cómo imprimir cada una. Están disponibles las siguientes opciones:

- 4 x 12 - Una por número de serie o lote: el PDF incluye etiquetas para cada número de serie/lote en la orden y proporcionan el nombre del producto, número de serie o lote y código de barras. La tabla corresponde a cuatro filas y doce columnas por página.
    
    Example 4 x 12 - One per lot/SN
    
- :guilabel:[`](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#id1)4 x 12 - Una por unidad: el PDF incluye etiquetas para la cantidad de artículos y proporcionan el nombre del producto, número de serie o lote y código de barras. La tabla corresponde a cuatro filas y doce columnas por página.
    
- Etiquetas ZPL - Una por número de lote o serie: imprime etiquetas en ZPL e incluyen el nombre del producto, el número de lote o serie y el código de barras.
    
- Etiquetas ZPL - Una por unidad: imprime etiquetas con la cantidad de artículos en ZPL e incluyen el nombre del producto, el número de lote o serie y el código de barras.
    

## Etiquetas de transportista[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#carrier-labels "Enlazar permanentemente con este título")

Para imprimir una _etiqueta de transportista_ con la dirección del destinatario, número de rastreo y detalles del transportista para transportistas externos, complete la siguiente configuración:

1. Seleccione la casilla Etiquetas de transportistas en los [ajustes del tipo de operación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-print-setup).
    
2. [Conecte una impresora](https://www.odoo.com/documentation/17.0/es/applications/general/iot/devices/printer.html) a la aplicación _IoT_ de Odoo.
    
3. [Asigne la etiqueta del transportista a la impresora](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-assign-printer).
    
4. Configure el [tipo de etiqueta](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-label-type) del método de envío.
    

### Asignar una impresora[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#assign-printer "Enlazar permanentemente con este título")

Consulte la documentación [Conectar una impresora](https://www.odoo.com/documentation/17.0/es/applications/general/iot/devices/printer.html) para obtener más información sobre cómo conectar una impresora a la aplicación _IoT_ de Odoo. Asigne la etiqueta de transportista a la impresora al terminar, vaya a IoT ‣ Dispositivos y seleccione la impresora deseada.

![Mostrar una lista de dispositivos IoT.](https://www.odoo.com/documentation/17.0/es/_images/select-printer.png)

En el formulario de configuración de la impresora, vaya a la pestaña Reporter de impresora para configurar los tipos de documentos que la impresora imprimirá de manera automática. Haga clic en Agregar línea para abrir una ventana emergente Agregar: reportes, en la barra de búsqueda escriba `Envío` y seleccione Etiquetas de envío.

 Nota

El reporte Documentos de envío es para [documentos de exportación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-export-doc).

![Reporte de etiqueta de transportista que se agregó a *Reportes de impresora*.](https://www.odoo.com/documentation/17.0/es/_images/printer-report.png)

Después de agregar el reporte etiquetas de envío en la pestaña Reportes de la impresora, asegúrese que el tipo de reporte coincida con el tipo de impresora que está conectada a la caja IoT.

- Para impresoras láser, configure el tipo de reporte a PDF.
    
- Para impresoras Zebra, configure el tipo de reporte a Texto.
    

### Tipo de etiqueta del transportista[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#shipping-carrier-label-type "Enlazar permanentemente con este título")

Después, complete el proceso de configuración para [el conector con el transportista externo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html). Después de eso, vaya a Inventario ‣ Configuración ‣ Métodos de envío, y seleccione el método de envío deseado.

En el formulario de configuración del método de envío, en la pestaña [nombre del transportista] Configuración, asegúrese de que el Formato de etiqueta coincida con el [tipo de reporte que se asignó antes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-assign-printer):

- Para impresoras láser, configure el formato de etiqueta a PDF.
    
- Para impresoras Zebra, configure el formato de etiqueta a ZPL2.
    

![Imagen donde se muestra el campo *Tipo de etiqueta* en la página de configuración de método de envío FedEx.](https://www.odoo.com/documentation/17.0/es/_images/label-type.png)

### Ejemplo de etiqueta de transportista[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#example-carrier-label "Enlazar permanentemente con este título")

Después de validar la operación, la etiqueta del transportista se generará en el chatter y se imprimirá con la impresora que haya conectado a IoT.

Example carrier label

 Ver también

[Imprimir etiquetas de transportista](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html)

## Documento de exportación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#export-document "Enlazar permanentemente con este título")

Aduana requiere un _documento de exportación_ para enviar paquetes de un país a otro, este documento lo puede imprimir en Odoo con los siguientes pasos:

1. Marque la casilla de verificación Documentos de exportación en los [ajustes de tipo de operación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-print-setup).
    
2. [Conecte una impresora](https://www.odoo.com/documentation/17.0/es/applications/general/iot/devices/printer.html) a la aplicación _IoT_ de Odoo.
    
3. Asigne un documento de exportación a la impresora.
    

### Asignar una impresora[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#id1 "Enlazar permanentemente con este título")

De forma similar a [las instrucciones de asignación de impresora para etiquetas de transportistas](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-assign-printer), después de conectar una impresora compatoble a la aplicación _IoT_ de Odoo, vaya a la aplicación IoT ‣ Dispositivos y seleccione la impresora que quiera.

En el formulario de configuración de la impresora, vaya a la pestaña reportes de impresora y haga clic en agregar una línea. En la ventana emergente Agregar: reportes que aparece, agregue el reporte Documentos de envío para asignar el documento de exportación a la impresora.

Example export document

## Contenido del paquete[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#package-content "Enlazar permanentemente con este título")

Un PDF de _contenido del paquete_ incluye el código de barras del paquete, la fecha del mismo, así como una lista de productos y cantidades que contiene.

Para imprimir este formulario de forma automática, vaya a Inventario ‣ Configuración ‣ Tipos de operación y seleccione el tipo de operación deseado. Después, vaya a la pestaña Hardware y marque la casilla de verificación Contenido del paquete.

 Importante

Si la opción no está disponible, active la función [Paquetes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/package.html) en la aplicación Inventario ‣ Configuración ‣ Ajustes marque la casilla de verificación Paquetes y haga clic en Guardar.

Después de activar la función en la pestaña Hardware, cuando valide la operación se imprimirá un PDF de los contenidos del paquete.

Example package content PDF

## Etiqueta de paquete[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#package-label "Enlazar permanentemente con este título")

Una _etiqueta de paquete_ que muestra el código de barras del paquete y la fecha de embalaje, que se puede configurar para imprimir al hacer clic en el botón _Incluir en el paquete_.

 Importante

El botón Incluir en el pquete **solo** está disponible cuando la función [Paquetes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/package.html) se activa en la aplicación Inventario ‣ Configuración ‣ Ajustes.

Después de activarlo, el botón Incluir en el paquete estará disponible en todas las operaciones de inventario (por ejemplo, recibos, pickings, transferencias internas, órdenes de entrega, entre otros).

Para imprimir la etiqueta del paquete de forma automática al hacer clic en el botón Incluir en el paquete, vaya a Inventario ‣ Configuración ‣ Tipos de operación, seleccione el tipo deseado y seleccione la casilla Etiqueta del paquete en la pestaña Hardware. Puede imprimir las etiquetas en formato PDF o ZPL, según se defina en el campo Imprimir etiqueta como.

Example of package barcode