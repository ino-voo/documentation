Una vez que un lead calificado se ha convertido en una oportunidad, el siguiente paso es crear y entregar una cotización. Puede realizar este proceso a través de la aplicación _CRM_ de Odoo.

## Cree un nuevo presupuesto[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/send_quotes.html#create-a-new-quotation "Enlazar permanentemente con este título")

Si desea crear una nueva cotización, abra la aplicación CRM, para ver el guilabel:`flujo de venta` en el tablero principal de _CRM_.

Ahí, haga clic en cualquier oportunidad para abrirla. Revise la información existente y actualice cualquier campo que sea necesario.

 Nota

Si ya se ha creado una cotización para esta oportunidad, la puede ver al hacer clic en el botón inteligente cotizaciones en la parte superior del formulario. El número de cotizaciones existentes también se muestra en el botón inteligente.

En la parte superior izquierda del formulario, haga clic en el botón nueva cotización.

![Formulario de cliente potencial calificado con el botón 'nueva cotización' destacado.](https://www.odoo.com/documentation/17.0/es/_images/send-quotes-new-button.png)

 Importante

El campo cliente **no** es obligatorio en el formulario de oportunidad.

Sin embargo, debe agregar o vincular la información del cliente antes de que se pueda enviar una cotización. Si deja el campo cliente vacío en la oportunidad, al hacer clic en el botón nueva cotización se abrirá una ventana emergente con las siguientes opciones:

- Crear un nuevo cliente: crea un nuevo registro de cliente, utilizando cualquier información disponible proporcionada en el formulario de oportunidad.
    
- Enlace a un cliente existente: abre un campo desplegable con los nombres de los clientes existentes. Seleccione un nombre para vincular esta nueva cotización a un registro de cliente existente.
    
- No vincular a un cliente: la cotización **no** se vinculará a un cliente y no se realizarán cambios en la información del cliente.
    

Una vez que haga clic en este botón, aparecerá un nuevo formulario de cotización. Confirme la información en la mitad superior del formulario y actualice cualquier campo faltante o incorrecto.

- Cliente: la empresa o contacto para quien se creó esta cotización.
    
- Referido: si este cliente fue referido por otro cliente o contacto, selecciónelo del menú desplegable en este campo.
    
- Dirección de facturación: dirección física a donde se debe enviar la factura.
    
- Dirección de entrega: dirección física donde deben entregarse los productos.
    
- Plantilla de cotización: si aplica, seleccione una [plantilla de cotización](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/send_quotations/quote_template.html) preconfigurada en este campo.
    
- Vencimiento: fecha en la que esta cotización ya no es válida.
    
- Fecha de cotización: fecha de creación de órdenes en borrador/enviados, fecha de confirmación de órdenes confirmadas. Tenga en cuenta que este campo solo es visible si el [modo desarrollador (modo de solución de bugs)](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html) está activo.
    
- Plan recurrente: si esta cotización es para un producto o suscripción recurrente, seleccione la configuración del plan recurrente que se utilizará.
    
- Listas de precios: seleccione una lista de precios para aplicar a esta orden.
    
- Términos de pago: seleccione los términos de pago aplicables para esta cotización.
    

![Formulario de cliente potencial calificado con el botón 'nueva cotización' destacado.](https://www.odoo.com/documentation/17.0/es/_images/send-quotes-new-quotation.png)

 Truco

El campo vencimiento se completa automáticamente en función de la fecha de creación de la cotización y el marco de tiempo de validez predeterminado.

Si desea actualizar el marco de tiempo de validez predeterminado, vaya a la aplicación Ventas ‣ Configuración ‣ Ajustes ‣ Cotizaciones y órdenes y actualice el campo validez predeterminada de cotización. Establezca en 0 para desactivar el vencimiento automático.

Cuando los cambios deseados estén completos, haga clic en guardar.

Cuando se utiliza una plantilla de cotización, la fecha de vencimiento se basa en el campo validez de la cotización de la plantilla. Para modificar el cálculo de la fecha de validez en una plantilla, vaya a la aplicación Ventas ‣ Configuración ‣ Órdenes de venta ‣ Plantillas de cotización.

Después haga clic en una plantilla para abrirla y actualice el número en el campo validez de la cotización.

### Líneas de venta[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/send_quotes.html#order-lines "Enlazar permanentemente con este título")

Después de actualizar la información del cliente, el pago y la fecha límite en la nueva cotización, puede actualizar la pestaña líneas de la orden con la información del producto correspondiente.

Para ello, haga clic en agregar un producto en la pestaña líneas de la orden.

A continuación, escriba el nombre de un artículo en el campo producto para buscar en el catálogo de productos. Luego, seleccione un producto del menú desplegable o cree uno nuevo seleccionando crear o crear y editar.

Después de seleccionar un producto, actualice la cantidad, si es necesario. Confirme la información en los campos restantes.

To remove a line from the quotation, click the  (trash can) icon.

To organize products into sections click Add a section and type a name for the section. Then, click the  (drag) icon to the left of the name and drag to move the section to the appropriate location. Move each product using the same method to finish organizing the quotation order lines.

![Categories are used to create separate sections on the order lines of a quote.](https://www.odoo.com/documentation/17.0/es/_images/product-sections.png)

#### Product catalog[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/send_quotes.html#product-catalog "Enlazar permanentemente con este título")

To quickly add numerous products to the quotation, click the Catalog button to open the product catalog.

All products in the database are listed as cards and can be sorted in the left panel by Product Category and Attributes.

![The product catalog displays all products as cards.](https://www.odoo.com/documentation/17.0/es/_images/product-catalog.png)

To add a product, click the  Add button on the product card. Set the quantity of the item using the  (add) or  (subtract) buttons, or type the quantity in the number field between the two buttons. To remove an item, click the  Remove button on the product card.

![The purple add and subtract buttons are used to set the quantity of an item.](https://www.odoo.com/documentation/17.0/es/_images/set-quantity.png)

Once all product quantities are set, click the Back to Quotation button to return to the quotation. The items selected in the product catalog now appear in the Order Lines tab.

## Vista previa y envío de cotización[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/send_quotes.html#preview-and-send-quotation "Enlazar permanentemente con este título")

Si desea ver una vista previa de la cotización para saber como la verá el cliente, haga clic en el botón vista previa. Al hacerlo, se abrirá una vista previa en el portal del cliente.

Después de revisar la vista previa, haga clic en volver al modo de edición para regresar al formulario de cotización en el backend.

Cuando la cotización esté lista para mandarla al cliente, haga clic en el botón enviar por correo electrónico.

Al hacerlo verá una ventana emergente con un mensaje de correo electrónico predeterminado. La información de la cotización, incluida la información de contacto, el costo total y el título de la cotización, se importará de la cotización.

Se adjuntará un PDF de la cotización en el correo electrónico.

 Nota

Se utiliza una plantilla pre-cargada para crear el mensaje de correo electrónico. Si desea modificar la plantilla, haga clic en el enlace interno a la derecha del campo cargar plantilla, ubicado en la parte inferior de la ventana emergente del correo electrónico.

Si desea seleccionar una nueva plantilla, elija una opción del menú desplegable cargar plantilla.

Proceda a realizar los cambios necesarios en el correo electrónico, luego haga clic en enviar. Se agrega una copia del mensaje al _chatter_ del registro.

Después de enviar una cotización, el botón inteligente cotizaciones de la oportunidad se actualizará con un nuevo número. Puede acceder a esta cotización, y todas las demás, a través de este botón inteligente en la parte superior de la oportunidad en la aplicación _CRM_.

Cualquier cotización adjunta a la oportunidad que esté confirmada y, por lo tanto, haya sido convertida en orden de venta, se deducirá del número indicado en el botón inteligente cotizaciones. En su lugar, el valor de la orden de venta aparecerá en el botón inteligente órdenes ubicado en el mismo tablero.

## Marcar una oportunidad ganada o perdida[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/send_quotes.html#mark-an-opportunity-won-or-lost "Enlazar permanentemente con este título")

Con el fin de mantener el flujo de trabajo actualizado y con la información correcta, es necesario identificar las oportunidades como _ganadas_ o _perdidas_ una vez que un cliente responda a una cotización.

Para marcar una oportunidad como _ganada_ o _perdida_, regrese a la oportunidad utilizando las migas de pan en la parte superior izquierda del formulario de cotización. O vaya a CRM ‣ Ventas ‣ Mi flujo de trabajo y haga clic en la oportunidad correcta para abrirla.

En la parte superior izquierda del formulario, haga clic en el botón ganada o perdida.

Si la oportunidad está marcada como _ganada_, se agregará un listón verde con la leyenda ganado al registro y se moverá a la etapa ganado.

Si marca una oportunidad como _perdida_ se abrirá la ventana emergente marcar como perdida, donde puede ingresar un motivo de pérdida.

En el campo desplegable motivo de pérdida, elija un motivo de pérdida existente. Si no encuentra la razón correcta, haga una nueva, solo debe ingresarla en el campo motivo de pérdida y hacer clic en crear.

 Truco

La mejor práctica es usar los valores preconfigurados en motivo de pérdida tanto como sea posible o limitar la creación de nuevos valores solo a los líderes del equipo de ventas. Usar los mismos valores en este parámetro facilitará y hará más preciso el análisis del flujo de trabajo al filtrar por el parámetro motivo de pérdida.

Si desea configurar nuevos valores para este campo, vaya a CRM ‣ Configuración ‣ Motivos de pérdida, y haga clic en nuevo y guardar para cada nueva entrada de la lista.

Las notas adicionales y comentarios se pueden agregar en el campo notas de cierre.

Una vez que haya ingresado la información deseada en la ventana emergente marcar como perdido, haga clic en marcar como perdido.

Si hace clic en marcar como perdido la ventana emergente desaparecerá y Odoo lo llevará de vuelta al formulario de la oportunidad, donde verá un nuevo listón con la leyenda perdido en la esquina superior derecha de la oportunidad.

Una vez que se marca una oportunidad como _perdida_, ya no se considera activa y se elimina del flujo de trabajo.

Si desea ver una oportunidad _perdida_ en el flujo de trabajo, haga clic en el icono de la flecha hacia abajo a la derecha de la barra de búsqueda y seleccione perdido o archivado en el menú desplegable que aparece.

 Importante

Cada que marca una oportunidad como _perdida_ se considera _archivada_, tenga en cuenta que, para que una oportunidad se incluya como _perdida_ en los reportes, **debe** marcarla específicamente como _perdida_, no como _archivada_.