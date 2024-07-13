
En _Ventas_ de Odoo, los vendedores pueden crear plantillas que pueden volver a usar para productos en común o servicios que ofrece el negocio.

Al usar estas plantillas, las cotizaciones se pueden hacer y enviar mucho más rápido a los clientes sin tener que crear cotizaciones nuevas desde cero cada vez que se realiza una negocioación de ventas.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/quote_template.html#configuration "Enlazar permanentemente con este título")

Primero, active estos ajustes en Ventas ‣ Configuración ‣ Ajustes y baje a la sección de Cotizaciones y órdenes.

En esa sección, marque la casilla junto a la opción Plantillas de cotización. Aparecerá un nuevo campo con el nombre Plantilla predeterminada en el que podrá elegir una plantilla de cotización predeterminada desde el menú desplegable.

![Cómo habilitar las plantillas de cotización en la aplicación Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/quotations-templates-setting.png)

También, al activar la función de Plantilla de cotización, aparecerá un enlace interno de ➡️ Plantillas de cotización debajo del campo Plantilla predeterminada.

Al hacer clic en el enlace, aparecerá una página de Plantillas de cotización desde donde podrá crear, ver y editar plantillas.

Antes de salir de la página de Ajustes, no olvide hacer clic en el botón Guardar para guardar todos los cambios que realizó durante la sesión.

## Crear plantillas de cotización[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/quote_template.html#create-quotation-templates "Enlazar permanentemente con este título")

Haga clic en el enlace de plantillas de cotización en la página de Ajustes o vaya a la Aplicación Ventas ‣ Configuración ‣ Plantillas de cotización. Ambas opciones mostrarán la página de las Plantillas de cotización donde podrá crear, ver y editar las plantillas de cotización.

![Página de plantillas de cotización en la aplicación Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/quotation-templates-page.png)

Para crear una nueva plantilla de cotización, haga clic en el botón Nuevo ubicado en la esquina superior izquierda. Al hacerlo, aparecerá un formulario en blanco de la plantilla de cotización que puede personalizar de muchas maneras.

![Cree una nueva plantilla de cotización en Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/blank-quotation-form.png)

Comience escribiendo un nombre para la plantilla en el campo Plantilla de cotización.

En el campo Validez de la cotización escriba durante cuántos días será válida la plantilla de la cotización. Puede dejar el campo con el valor predeterminado `0` para mantener su validez de manera indefinida.

Luego, en el campo Correo electrónico de confirmación, haga clic en el campo en blanco para que aparezca un menú desplegable. Desde ahí, seleccione una plantilla de correo electrónico ya configurada para enviarla a los clientes al confirmar una orden.

 Truco

Para crear una nueva plantilla de correo electrónico directamente desde el campo Correo electrónico de confirmación, comience a escribir el nombre de la nueva plantilla de correo electrónico en el campo y seleccione: Crear o Crear y editar… del menú desplegable que aparece.

Si hace clic en Crear se creará una plantilla de correo que podrá editar después.

Si hace clic en Crear y editar… se creará la plantilla de correo electrónico y aparecerá una ventana emergente para Crear un correo electrónico de confirmación. Allí podrá personalizar y configurar la plantilla de correo de manera inmediata.

![Ventana emergente para crear un correo electrónico de confirmación desde la plantilla de la cotización en Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/create-confirmation-mail-popup.png)

Una vez que haya realizado todas las modificaciones necesarias, haga clic en Guardar y cerrar para almacenar la plantilla de correo electrónico y regresar al formulario de cotización.

Si trabaja en un ambiente multiempresa, utilice el campo Empresa para asignar la empresa a la cual aplicará está plantilla de cotización.

Si establece un diario en el campo Diario de facturación, todas las órdenes de venta con esta plantilla se facturarán en ese diario específico. Si no establece ningún diario en este campo, entonces se utilizará el diario de ventas con la secuencia más baja.

Las funciones Firma en línea o Pago en línea estarán disponibles como opción en los formularios de las plantillas de cotización si están habilitadas en los Ajustes (Ventas ‣ Configuración ‣ Ajustes).

Seleccione la casilla junto a Firma en línea para solicitarle al cliente su firma digital para confirmar una orden.

Seleccione la casilla junto a Pago en línea para solicitarle al cliente que pague en línea y así poder confirmar la orden. Cuando esta casilla está seleccionada aparecerá un campo de porcentaje, allí deberá especificar el importe porcentual de pago correspondiente.

Puede habilitar las opciones Firma en línea y Pago en línea de forma simultánea. En este caso, el cliente deberá proporcionar su firma **y** realizar un pago para poder confirmar la orden.

En el campo Plan recurrente deberá elegir entre distintas cantidades de tiempo ya configuradas (por ejemplo, Mensual, Trimestral, entre otras) para determinar qué tan seguido debe ocurrir esta plantilla de cotización.

 Nota

El campo Plan recurrente **solo** es válido para los planes de suscripción. Para obtener más información, consulte la documentación sobre [Planes de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/plans.html).

### Pestaña de líneas[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/quote_template.html#lines-tab "Enlazar permanentemente con este título")

En la pestaña Líneas, puede agregar los productos a la plantilla de cotización al hacer clic en Agregar un producto, organizarlos al hacer clic en `Agregar sección` (y puede arrastrar/soltar los encabezados de las secciones), y puede agregar mas información discrecional (como detalles de garantía, términos, etc.) al hacer clic en Agregar una nota.

Haga clic en Agregar un producto en la pestaña Líneas de un formulario de plantilla de cotización para agregar uno a la plantilla de cotización. Al hacerlo, aparecerá un campo vacío en la columna Producto.

Si hace clic ahí, aparecerá un menú desplegable con todos los productos disponibles en la base de datos. Seleccione los productos que desee desde ese menú para agregarlos a la plantilla de cotización.

Si el producto que desea no está visible, escriba el nombre del producto en el campo Producto y la opción aparecerá en la lista desplegable. También puede encontrar los productos si hace clic en Buscar más… en el menú desplegable.

 Truco

En Odoo 17 ahora es posible agregar productos relacionados con los eventos (estands y registros) a las plantillas de cotización. Para ello, haga clic en el campo Producto, escriba `Evento` y seleccione el producto relacionado con el evento deseado en el menú desplegable que aparece.

 Nota

Al agregar un producto, la cantidad predeterminada es `1`, pero puede editarlo cuando quiera.

Luego, arrastre y suelte el producto a dónde desee mediante el icono de seis cuadros que se ubica del lado izquierdo de cada línea de artículo.

Para agregar una _sección_, que funcione como un encabezado para organizar las líneas de la orden de ventas, haga clic en Agregar sección en la pestaña Líneas. Al hacerlo, aparecerá un campo en blanco, en donde podrá escribir el nombre que quiera para la sección. Luego, haga clic en otra parte para asegurar el nombre de la sección.

Luego, arrastre y suelte el producto a dónde desee mediante el icono de seis cuadros que se ubica del lado izquierdo de cada línea de artículo.

Para agregar una nota, la cual aparecerá como un texto en la cotización del cliente, haga clic en Agregar una nota en la pestaña Líneas. Al hacerlo, aparecerá un campo en blanco, en donde podrá escribir la nota que quiera. Luego, haga clic en otra parte para asegurar la nota.

Luego, arrastre y suelte la nota al lugar que quiera mediante el icono seis cuadros.

Para eliminar cualquier línea de artículo desde la pestaña Líneas (producto, sección, y/o nota), haga clic en el icono 🗑️ (papelera) que se ubica del lado derecho de la línea.

### Pestaña de productos opcionales[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/quote_template.html#optional-products-tab "Enlazar permanentemente con este título")

Usar _productos opcionales_ es una estrategia de marketing que implica la venta cruzada de productos junto con un producto principal. El objetivo es ofrecer productos útiles y relacionados a los clientes, lo que puede resultar en un aumento de ventas.

Por ejemplo, si un cliente desea comprar un automóvil tiene la opción de ordenar asientos con función de masaje o puede ignorar la oferta y solo comprar el vehículo. La experiencia del cliente mejora si le proporciona la opción de comprar productos opcionales.

Los productos opcionales aparecen como una sección al final de las órdenes de ventas y de las página de comercio electrónico. Los clientes pueden agregarlos ellos mismos de manera inmediata a sus órdenes de ventas en línea.

![Los productos opcionales en una orden de ventas típica en Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/optional-products-on-sales-order.png)

En la pestaña Productos opcionales, puede Agregar una línea para cada producto de venta cruzada relacionado a los artículos principales en la pestaña Líneas, si aplica. Lo ideal es que los productos que se agregan aquí sean un complemento de la oferta original como un valor agregado para el comprador potencial.

Al hacer clic en Agregar una línea muestra un campo en blanco en la columna Producto.

Si hace clic sobre el campo, aparecerá una lista desplegable con productos de la base de datos y podrá seleccionar el que desee para agregarlo como un producto opcional a la plantilla de la cotización.

Para eliminar cualquier línea de artículo desde la pestaña Productos opcionales, haga clic en el icono 🗑️ (papelera).

 Nota

Los productos opcionales **no** son obligatorios para crear una plantilla de cotización

### Pestaña de términos y condiciones[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/quote_template.html#terms-conditions-tab "Enlazar permanentemente con este título")

La pestaña Términos y condiciones le da la oportunidad para agregar términos y condiciones a la plantilla de la cotización. Para agregarlos, solo debe escribir (o copiar y pegar) los términos y condiciones deseadas en esta pestaña.

 Ver también

[Términos y condiciones predeterminados](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/terms_conditions.html)

 Nota

Los términos y condiciones **no** son obligatorios para crear una plantilla de cotización.

### Pestaña de Creador de cotizaciones en PDF[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/quote_template.html#pdf-quote-builder-tab "Enlazar permanentemente con este título")

La pestaña Creador de cotizaciones en PDF proporciona opciones para elaborar cotizaciones llamativas que incluyan más información y elementos visualmente agradables. Además, son muy útiles para destacar productos y servicios.

Para subir las páginas de encabezado y los pies de página haga clic en el icono ✏️ (lápiz) ubicado del lado derecho de las respectivas páginas. Haga clic en el icono 🗑️ (papelera) para eliminar algún PDF que haya subido.

 Ver también

[Creador de cotizaciones en PDF](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/pdf_quote_builder.html)

## Usar plantillas de cotización[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/quote_template.html#use-quotation-templates "Enlazar permanentemente con este título")

Al crear una cotización (Aplicación Ventas ‣ Crear), seleccione una plantilla preconfigurada en el menú desplegable del campo Plantilla de cotización.

![El campo de vencimiento en una cotización estándar en Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/quotation-templates-field.png)

Para ver lo que el cliente verá, haga clic en el botón inteligente de Vista previa que se ubica en la parte superior de la página para ver el aspecto que tendría la cotización desde el frontend del sitio web mediante el portal del cliente de Odoo.

![VIsta previa del cliente de una plantilla de cotización en Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/quotations-templates-preview.png)

 Truco

El diseño de las plantillas de cotización usa la misma metodología y funcionalidad con los bloques de creación que una página web típica de _Sitio web_ de Odoo. Para obtener más información, asegúrese de consultar la documentación sobre [Sitio web](https://www.odoo.com/documentation/17.0/es/applications/websites/website.html).

Cuando la personalización y los bloques estén completos, haga clic en Guardar para aplicar todos los cambios.

También aparecerá un cuadro azul en la parte superior del diseño de la plantilla de cotización con un enlace para volver al modo de edición rapidamente. Al hacer clic sobre él, Odoo regresa al formulario de la cotización en el backend de la aplicación _Ventas_.