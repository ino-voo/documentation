El _creador de cotizaciones en PDF_ de _Ventas_ le permite enviar a sus clientes un archivo PDF totalmente personalizado para las cotizaciones, en el que se muestren la empresa y los productos, con distintos elementos de información y diseño, en lugar de limitarse a mostrar el precio y el total.

El creador de cotizaciones en PDF agrupa las páginas de encabezado, las descripciones de los productos, los precios y las páginas de pie de página para crear una cotización detallada. También puede introducir textos dinámicos en el PDF para personalizar la cotización para el cliente.

Disponer de un PDF personalizado en las cotizaciones aporta una mejor experiencia de compra para los clientes y añade un toque elegante de profesionalidad a la empresa.

 Ver también

[Consejos de Odoo - Creación de una cotización en PDF [video]](https://www.youtube.com/watch?v=tQNydBZt-VI)

 Nota

Es recomendable editar formularios de PDF con el software de Adobe. Los campos de formulario en el encabezado y pie de página de las plantillas PDF son necesarios para obtener valores dinámicos con Odoo.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/pdf_quote_builder.html#configuration "Enlazar permanentemente con este título")

Si desea añadir archivos PDF personalizados a las cotizaciones, _debe_ configurar la función creador de cotizaciones PDF.

Para ello, vaya a la aplicación Ventas ‣ Configuración ‣ Ajustes. Después, en la página Ajustes, vaya a la sección cotizaciones y órdenes y busque la función creador de cotizaciones en PDF.

![La función para crear cotizaciones en PDF esta ubicada en la página de ajustes de la aplicación Ventas.](https://www.odoo.com/documentation/17.0/es/_images/pdf-quote-builder-feature.png)

Aquí puede subir encabezados y pies de página personalizados. Para hacerlo, haga clic en el botón Subir archivo o en el icono ✏️ (lápiz) del lado derecho del campo que desea y luego ubique, seleccione y suba el archivo PDF que quiera.

 Nota

También puede añadir directamente los encabezados y pies de página en una plantilla de cotización, por lo que es posible tener variaciones diferentes por plantilla.

Al hacer clic en el icono de 🗑️ (papelera), se eliminan los archivos PDF actuales y se reemplazan por un campo en blanco y un botón de Subir archivo.

Una vez que suba los archivos PDF que desea en los campos correctos en la sección de Creador de cotizaciones en PDF de la página de Ajustes en _Ventas_, asegúrese de guardar sus cambios.

Los archivos que suba serán los PDF predeterminados que se usarán en todas las cotizaciones.

 Nota

Los valores establecidos en los ajustes del Creador de cotizaciones en PDF son específicos de la empresa.

## Texto dinámico en archivos PDF[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/pdf_quote_builder.html#dynamic-text-in-pdfs "Enlazar permanentemente con este título")

Al crear PDF personalizados para las cotizaciones, use el _texto dinámico_ para que Odoo complete automáticamente el contenido del archivo PDF con información relacionada a la cotización de la base de datos de Odoo, como nombres, precios, etc.

Los valores del texto dinámico vienen de componentes (entradas de texto) que se pueden añadir a un archivo PDF y Odoo completa automáticamente esos valores con información relacionada a la cotización.

### Valores de texto dinámico[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/pdf_quote_builder.html#dynamic-text-values "Enlazar permanentemente con este título")

A continuación le presentamos valores comunes de texto dinámico que se usan en archivos PDF personalizados y lo que representan:

- name: Referencia de la orden de ventas
    
- partner_id__name: Nombre del cliente
    
- user_id__name: Nombre del vendedor
    
- amount_untaxed: Subtotal
    
- amount_total: Total
    
- delivery_date: Fecha de envío
    
- validity_date: Fecha de vencimiento
    
- client_order_ref: Referencia del cliente
    

 Nota

En la notación para los valores partner_id__name y user_id__name se usa el doble guion bajo en lugar del símbolo generalmente usado de `.` porque en este momento la biblioteca no admite el símbolo `.`.

A continuación se muestran los valores del texto dinámico específico del producto:

- description: Descripción del producto
    
- quantity: Cantidad
    
- uom: Unidad de medida (UdM)
    
- price_unit: Precio unitario
    
- discount: Descuento
    
- product_sale_price: Lista de precio del producto
    
- taxes: Nombre de los impuestos separados con coma (`,`)
    
- tax_excl_price: Precio con impuesto excluido
    
- tax_incl_price: Precio con impuesto incluido
    

 Example

Cuando se crea un PDF, es mejor usar valores comunes de texto dinámico (name y partner_id_name). Cuando se sube a la base de datos, Odoo completa automáticamente esos campos con la información de sus respectivos campos.

En este caso, Odoo completará de forma automática la referencia de la orden de ventas en el campo de texto dinámico name y el nombre del cliente en el campo partner_id_name.

![Creación de una cotización en PDF usando marcadores de posición dinámicos comunes.](https://www.odoo.com/documentation/17.0/es/_images/pdf-quote-builder-sample.png)

Una vez que los archivos PDF están completos, guárdelos en el disco duro de su computadora y súbalos a Odoo desde la aplicación Ventas ‣ Configuración ‣ Ajustes ‣ Creador de cotizaciones en PDF.

Suba los archivos PDF que creó en el campo Encabezados o Pies de página.

Una vez que los haya subido, haga clic en Guardar.

## Agregar un archivo PDF a un producto[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/pdf_quote_builder.html#add-pdf-to-product "Enlazar permanentemente con este título")

En la aplicación _Ventas_ de Odoo también es posible agregar un PDF personalizado al formulario de un producto. Cuando lo agrega y ese producto se usa en una cotización, también se inserta ese archivo PDF en el PDF final.

Para agregar un archivo PDF personalizado a un producto, vaya a la aplicación Ventas ‣ Productos ‣ Productos y seleccione el producto al que desea agregar el PDF personalizado.

 Nota

También puede agregar un documento a las variantes del producto, pero si hay documentos en un producto _y_ en sus variantes, **solo** se mostrarán los documentos de las variantes.

Para agregar un documento personalizado a una variante de producto, vaya a la aplicación Ventas ‣ Productos ‣ Variantes de producto. Seleccione la variante que desee, haga clic en el botón inteligente Documentos y suba los documentos personalizados a la variante específica del producto.

En la página del producto, haga clic en el botón inteligente de Documentos en la parte superior de la página.

![El botón inteligente de Documentos en un formulario de producto en Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/documents-smart-button.png)

La acción anterior abrirá una página separada de Documentos para ese producto, allí puede subir archivos relacionados. Desde esta página, haga clic en Nuevo o Cargar.

Al hacer clic en Subir puede cargar el documento que desee y luego puede proporcionarle una configuración más avanzada desde la tarjeta del documento. También puede hacer clic en el icono de tres puntos ubicado en la esquina superior derecha de la tarjeta del documento y después en Editar.

Al hacer clic en Nuevo se abre un formulario para documentos en blanco, allí puede cargar el PDF que desee con el botón Suba su archivo. Este se encuentra ubicado en el campo Contenido del archivo del formulario.

![Un formulario de documento estándar con varios campos para un producto específico en la aplicación Venta de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/blank-document-form.png)

Desde aquí puede modificar la información y la configuración relacionada con el documento que subió.

El primer campo en el formulario de documentos es para el Nombre del documento y aparece en color gris (además de que no puede hacer clic allí) hasta que suba un documento. Una vez que haya subido un PDF, el campo Nombre se completa de forma automática con el nombre del PDF, puede editarlo después.

Antes de subir un documento, desde el campo con el menú desplegable Tipo puede elegir si es un archivo o una URL.

![Un formulario de documento estándar con un PDF en la aplicación Venta de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/document-form-uploaded-pdf.png)

 Nota

Si sube un PDF, el campo Tipo se completa de forma automática como archivo y no podrá modificarlo.

Luego, en la sección Ventas, en el campo Visible en, haga clic en el menú desplegable y seleccione alguna de las siguientes opciones: Cotización, Orden confirmada o Dentro de la cotización.

- Cotización: los clientes reciben el documento y pueden acceder a él en cualquier momento.
    
- Orden confirmada: los clientes reciben el documento al momento de confirmar su orden, es muy útil para los usuarios manuales y para otros documentos complementarios.
    
- Dentro de la cotización: el documento está incluido en el PDF de la cotización, entre las páginas de cabecera y la sección correspondiente a los precios.
    

 Example

Si selecciona la opción Dentro de la cotización para el campo Visible en y carga el archivo PDF personalizado con el nombre `Sample Builder.pdf`, este estará visible en la cotización en el _portal del cliente_ dentro de la sección Documentos.

> ![Muestra de un PDF en una cotización después de elegir la opción dentro de la cotización de ventas en la aplicación Venta de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/pdf-inside-quote-sample.png)

Por último, en la sección Comercio electrónico, elija si desea mostrarlo en la página del producto o no desde el frontend (en la tienda en línea).

 Example

Cuando la opción Mostrar en la página del producto está habilitada, aparece un enlace al documento que subió en la página del producto disponible desde el frontend de una tienda en línea.

Este enlace está debajo del encabezado Documentos y tiene el nombre del archivo que subió.

> ![Un enlace a un documento que subió el usuario en la página de un producto desde la aplicación Venta de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/show-product-page.png)

## Cotización en PDF[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/pdf_quote_builder.html#pdf-quote "Enlazar permanentemente con este título")

Una vez que confirma una cotización con un PDF preconfigurado, Odoo le ofrece la opción de imprimirla para verificar si hay errores o para almacenarla en sus registros.

Para imprimirla, vaya a la cotización confirmada y haga clic en el icono ⚙️ (de engranaje) que abrirá un menú desplegable. Desde allí, seleccione Imprimir y luego Cotización en PDF.

![La opción para imprimir la cotización en PDF en el menú desplegable desde la orden de venta confirmadas en la aplicación Venta de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/drop-down-print-pdf.png)

En ese instante comenzará la descarga instantánea de la cotización. Al abrirla, puede ver e imprimir la cotización en PDF y el PDF del producto configurado que estableció para poder visualizar dentro de la cotización.

 Nota

Para obtener más referencias, descargue los siguientes [`ejemplos de creación de cotizaciones en PDF`](https://www.odoo.com/documentation/17.0/es/_downloads/5f0840ed187116c425fdac2ab4b592e1/pdfquotebuilderexamples.zip).

 Ver también

- [Plantillas de cotización](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/quote_template.html)