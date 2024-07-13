Un anticipo es un pago parcial que realiza el comprador cuando se celebra un contrato de venta. Esto implica el compromiso total de ambas partes (vendedor y comprador) de cumplir el contrato.

Con un anticipo, el comprador paga una parte del importe total adeudado mientras acepta pagar la cantidad restante después. Por otra parte, el vendedor le proporciona los bienes o servicios al comprador después de aceptar el anticipo, confiando en que este le pagará el importe restante más adelante.

## Crear facturas[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html#create-invoices "Enlazar permanentemente con este título")

Cuando se confirma una orden de venta, se habilita la opción de crear una factura mediante el botón Crear factura ubicado en la esquina superior izquierda del formulario de orden de venta. Cuando hace clic, aparece la ventana emergente Crear facturas.

![Ventana emergente para crear facturas que aparece en la aplicación Ventas.](https://www.odoo.com/documentation/17.0/es/_images/create-invoices-popup-form.png)

 Nota

Las facturas se crean como borradores de forma automática para que las pueda revisar antes de validarlas.

En la ventana emergente Crear facturas, hay 3 opciones para elegir en el campo Crear factura:

- Factura normal
    
- Anticipo (porcentaje)
    
- Anticipo (importe fijo)
    

 Nota

Los otros campos desaparecen si selecciona factura normal, ya que solo corresponden a las configuraciones de anticipos.

## Solicitud inicial de un anticipo[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html#initial-down-payment-request "Enlazar permanentemente con este título")

En el formulario emergente para crear facturas, las opciones para anticipos son:

- Anticipo (porcentaje)
    
- Anticipo (importe fijo)
    

Una vez que haya seleccionado la opción de anticipo deseada en el campo Crear factura, indique el importe (ya sea como porcentaje o importe fijo) en el campo Importe del anticipo.

Después, seleccione la cuenta de ingresos apropiada para la factura en el campo Cuenta de ingresos. Después, seleccione la cantidad de impuestos en el campo desplegable Impuestos del cliente, solo si es necesario.

![Un formulario emergente para crear facturas con la información apropiada en los campos de anticipos.](https://www.odoo.com/documentation/17.0/es/_images/create-invoices-popup-form-filled-out.png)

Una vez que los campos tengan la información deseada, haga clic en el botón Crear borrador de factura. Una vez hecho eso, Odoo le mostrará el Borrador de la factura del cliente.

En la pestaña Líneas de factura del Borrador de la factura del cliente aparecerá como un guilabel:`Producto` el anticipo que acaba de configurar en el formulario emergente Crear facturas.

![Anticipo como producto en la pestaña de líneas del borrador de la factura del cliente en Odoo.](https://www.odoo.com/documentation/17.0/es/_images/down-payment-product-inv-draft.png)

 Nota

Cuando hace clic en el producto Anticipo desde la pestaña Líneas de factura aparecerá el formulario del producto para el anticipo.

De manera automática, el Tipo de producto de los anticipos generados para las facturas será Servicio, con la política de facturación configurada a Precio fijo o de prepago.

![El formulario de producto con el tipo de producto servicio y el campo de política de facturación.](https://www.odoo.com/documentation/17.0/es/_images/down-payment-product.png)

Puede editar o modificar este producto en cualquier momento.

 Advertencia

Si selecciona:guilabel:`Basado en cantidad entregada (manual)` como política de facturación **no** podrá crear una factura.

## Por ejemplo: solicitar un anticipo del 50%[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html#example-request-50-down-payment "Enlazar permanentemente con este título")

 Nota

El siguiente ejemplo involucra un anticipo del 50% en un producto (Gabinete con puertas) cuya política de facturación es Cantidades ordenadas.

![El producto de gabinete con puertas donde se muestran varios detalles y campos.](https://www.odoo.com/documentation/17.0/es/_images/cabinet-product-details.png)

 Ver también

[Facturar por cantidades entregadas u ordenadas](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/invoicing_policy.html)

Primero navegue a Ventas ‣ Nuevo y agregue un Cliente a la cotización.

Después, haga clic en Agregar un producto en la pestaña de lineas de la orden y seleccione el producto gabinete con puertas.

Cuando se confirma la orden (al apretar el botón Confirmar) la cotización se convertirá en una orden de venta. Una vez que esto suceda, para crear la factura solo haga clic en Crear factura.

![Orden de venta de un gabinete con puertas que se confirmó en la aplicación de Ventas.](https://www.odoo.com/documentation/17.0/es/_images/cabinet-sales-orders-confirmed.png)

Después, en la ventana emergente Crear facturas que aparece, seleccione Anticipo (porcentaje) y escriba `50` en el campo Importe del anticipo.

 Nota

The Income Account and Customer Taxes fields are _not_ required fields, and they will _not_ appear if they’ve already been preconfigured in previous down payment requests.

Para más información, revise nuestra documentación sobre [modificación de impuestos del cliente en anticipos](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html#sales-invoicing-customer-tax-modification-down-payments) y [modificación de la cuenta de ingresos en anticipos](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html#sales-invoicing-income-account-modification).

Finalmente, haga clic en crear un borrador de factura para crear un borrador de factura.

Al hacer clic en crear borrador de factura se mostrará el borrador de la factura, el cual incluye el anticipo como un Producto en la pestaña de líneas de factura.

Aquí puede confirmar y publicar la factura, solo debe hacer clic en Confirmar y el estado cambiará de borrador a publicado. También muestra una nueva serie de botones en la parte superior de la página.

![Un borrador de factura donde se menciona un anticipo en la aplicación Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/draft-invoice-sample.png)

Puede registrar el pago si hace clic en Registrar pago.

![Mostrar el botón Registrar pago en una factura de cliente confirmada.](https://www.odoo.com/documentation/17.0/es/_images/register-payment-button.png)

Doing so reveals a Register Payment pop-up form, which is auto-populated with the necessary information. Confirm the information provided is correct, and make any necessary adjustments. When ready, click the Create Payment button.

![Imagen de la ventana emergente para registrar pago con el botón crear pago.](https://www.odoo.com/documentation/17.0/es/_images/register-payment-pop-up-window.png)

Después de hacer clic en Crear pago Odoo mostrará la factura del cliente, ahora con un listón verde de En proceso de pago en la esquina superior derecha.

![Factura del cliente con un listón En proceso de pago en la esquina superior derecha.](https://www.odoo.com/documentation/17.0/es/_images/customer-invoice-green-payment-banner.png)

Cuando el cliente quiera pagar la cantidad restante de la orden, deberá crear otra factura. Para ello, use las migas de pan para regresar a la orden de venta.

En la orden de venta habrá una nueva sección de Adelantos en la pestaña Líneas de la orden, junto con el anticipo que acaba de facturar.

![La sección de anticipos en la pestaña de las líneas de la orden en la orden de ventas.](https://www.odoo.com/documentation/17.0/es/_images/down-payments-section-order-lines.png)

Después, haga clic en el botón Crear factura.

En la ventana emergente Crear facturas verá dos nuevos campos: Ya se facturó y importe a facturar.

![La opción para deducir anticipo en la ventana emergente para crear facturas en la aplicación Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/create-invoices-pop-up-already-invoiced.png)

Si ya se pagará la cantidad restante, seleccione la opción Factura normal. Odoo creará una factura por la cantidad exacta que se necesita para completar el total del pago, como se indica en el campo Cantidad por facturar.

Ya que esté listo, haga clic en crear borrador de factura.

Al hacer esto verá la página borrador de factura de cliente, la cual enumerará _todas_ las facturas para esa orden de venta específica en la pestaña líneas de factura. Cada elemento de línea de factura muestra toda la información necesaria relacionada con cada factura.

Para completar el flujo, haga clic en confirmar, lo cual cambiará el estado de la factura de borrador a publicado. Luego, haga clic en registrar pago.

Una vez más, aparecerá registrar pago, con todos los campos autocompletados con la información necesaria, incluido el monto restante que queda por pagar en la orden.

![El segundo formulario emergente de registro de pago en las ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/second-register-payment-popup.png)

Después de confirmar esa información, haga clic en crear pago. Al hacerlo, se mostrará la factura del cliente final con un listón verde con la leyenda en proceso de pago en la esquina superior derecha. Además, podrá ver ambos pagos iniciales en la pestaña líneas de factura.

![La segunda factura del pago con el listón de pago en la aplicación Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/second-down-payment-in-payment-invoice.png)

Si llega a este punto ha terminado el flujo.

 Nota

Este flujo también se puede realizar con la opción de anticipo por importe fijo.

 Importante

If a down payment is used with a product that has a Delivered quantities invoicing policy, and the cost of the product _exceeds_ the 50% down payment (as in most cases), a regular invoice is created.

However, for products that cost _less_ than the 50% down payment, the down payments will **not** be able to be deducted when it comes time to invoice the customer.

This is because the product(s) would have to be delivered _before_ creating the final invoice due to Odoo not allowing negative totals for invoices.

Si no ha entregado nada, deberá crear una nota de crédito, esta cancela el borrador de factura que se creó después del anticipo.

Si desea utilizar la opción de nota de crédito, deberá contar con la aplicación _Inventario_ para poder confirmar la entrega. De lo contrario, puede registrar la cantidad entregada de forma manual directamente en la orden de venta.

## Example: request 100% down payment[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html#example-request-100-down-payment "Enlazar permanentemente con este título")

The process of requesting a 100% down payment is similar to the process of setting up a [50% down payment](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html#sales-invoicing-50-percent-down-payments), but with fewer steps.

 Nota

A 100% down payment is **not** the same as a full payment of the sales order.

A sales order paid through the regular invoice process will not allow any additional invoices to be generated, and **will not** display the _Create Invoice_ button on the Sales Order.

Following this example **will** cause the _Create Invoice_ button to be displayed on the Sales Order. This is because Odoo expects another invoice to be created after the down payment to complete payment of the sales order.

The _Solar Panel Installation_ product is being used in this example.

To configure a 100% down payment, begin by navigating to Sales app ‣ New, and add a Customer to the quote.

Next, click Add a product in the Order Lines tab, and select the `Solar Panel Installation` product.

Upon clicking the Confirm button, the quotation turns into a sales order. At that point, an invoice can now be created by clicking Create Invoice in the top-left corner.

On the Create invoices pop-up window that appears, select Down payment (percentage), and type `100` in the Down Payment Amount field. Then, if desired, select an Income Account and Customer Taxes in their respective fields.

 Nota

The Income Account and Customer Taxes fields are _not_ required fields, and they will _not_ appear if they’ve already been preconfigured in previous down payment requests.

Para más información, revise nuestra documentación sobre [modificación de impuestos del cliente en anticipos](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html#sales-invoicing-customer-tax-modification-down-payments) y [modificación de la cuenta de ingresos en anticipos](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html#sales-invoicing-income-account-modification).

![The Down payment (percentage) option selected with 100% set as the Down Payment.](https://www.odoo.com/documentation/17.0/es/_images/100p-down-payment-percentage.png)

Next, click Create Draft Invoice to create an invoice draft. This will also bring the draft invoice into view, which includes the Down payment as a Product in the Invoice Lines tab.

The invoice can now be confirmed and posted by clicking Confirm. Confirming the invoice changes the status from Draft to Posted. It also reveals a new series of buttons at the top of the page.

The payment can be registered by clicking the Register Payment button.

Al hacerlo se mostrará la ventana emergene Registrar pago, que se llenará de forma automática con la información necesaria. Confirme que la información sea correcta y haga los ajustes necesarios. Cuando esté listo, haga clic en el botón Crear pago.

Después de hacer clic en Crear pago Odoo mostrará la factura del cliente, ahora con un listón verde de En proceso de pago en la esquina superior derecha.

![Factura del cliente con un listón En proceso de pago en la esquina superior derecha.](https://www.odoo.com/documentation/17.0/es/_images/100p-invoice.png)

The process is now complete, and the 100% down payment has been successfully applied.

## Modificación de impuestos del cliente en los anticipos[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html#customer-taxes-modification-on-down-payments "Enlazar permanentemente con este título")

Para ajustar la cuenta de ingresos y los impuestos del cliente vinculados a un anticipo, vaya a la página de productos (aplicación Ventas ‣ Productos ‣ Productos), luego escriba `anticipo` en la barra de búsqueda y seleccione el producto para abrir su página de detalles.

En la página del producto anticipo bajo la pestaña información general, en el campo impuestos del cliente, podrá modificar los impuestos del cliente.

![Cómo modificar el enlace de la cuenta de ingresos para los anticipos.](https://www.odoo.com/documentation/17.0/es/_images/customer-taxes-field.png)

## Modificación de la cuenta de ingresos en los anticipos[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/down_payment.html#income-account-modification-on-down-payments "Enlazar permanentemente con este título")

Si desea cambiar o ajustar la cuenta de ingresos asociada a la página del producto anticipo, **debe** contar con la aplicación _Contabilidad_.

Si tiene la aplicación _Contabilidad_ instalada, podrá ver la pestaña Contabilidad en la página del producto. Si no tiene la aplicación _Contabilidad_ **no** podrá ver esta pestaña

En la pestaña Contabilidad, puede modificar la cuenta de ingresos desde el campo correspondiente en la sección Por cobrar.

![Cómo modificar el enlace de la cuenta de ingresos para los anticipos.](https://www.odoo.com/documentation/17.0/es/_images/income-account.png)

 Ver también

[Facturar por cantidades entregadas u ordenadas](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/invoicing_policy.html)