El método de pago **transferencia electrónica** le permite proporcionar instrucciones de pago a sus clientes, así como los detalles bancarios y comunicación. Se muestran de la siguiente manera:

- al final del proceso de pago, una vez que el cliente seleccionó Transferencia electrónica como método de pago e hizo clic en el botón de Pagar ahora:
    
    ![Instrucciones de pago al final del proceso](https://www.odoo.com/documentation/17.0/es/_images/payment_instructions_checkout.png)
    
- en el portal del cliente:
    
    ![Instrucciones de pago en el portal del cliente](https://www.odoo.com/documentation/17.0/es/_images/payment_instructions_portal.png)
    

 Nota

- Si bien, este método es muy accesible y requiere una configuración mínima, es muy ineficiente en cuanto al proceso. En su lugar, le recomendamos un [proveedor de pago](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html).
    
- Las órdenes en línea se quedan en la etapa de cotización enviada (es decir, orden no pagada) hasta que reciba el pago y confirme la orden.
    

 Truco

Las **transferencias electrónicas** se pueden usar como plantillas para otros métodos de pago que se procesan manualmente, como los cheques, al renombrarlos o duplicarlos.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/wire_transfer.html#configuration "Enlazar permanentemente con este título")

Para configurar las **transferencias electrónicas**, vaya a Contabilidad / Sitio web ‣ Configuración ‣ Proveedores de pago y abra la tarjeta de Transferencia electrónica. Luego, en la pestaña de Configuración:

- Seleccione la Comunicación que usará:
    
    - Con base en la Referencia de los Documentos: órdenes de venta o el número de factura
        
    - Con base en el ID del cliente: identificador del cliente
        
- Seleccione la casilla Permitir códigos QR para activar los [pagos con código QR](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/epc_qr_code.html).
    

Defina las instrucciones de pago en la pestaña Mensajes:

![Defina las instrucciones de pago](https://www.odoo.com/documentation/17.0/es/_images/payment_instructions.png)

Si ya tiene definida una [cuenta bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank.html), el número de cuenta se agregará de manera automática al mensaje predeterminado que genera Odoo. También puede agregarlo después y actualizar el mensaje si da clic en Volver a cargar el mensaje pendiente.

 Ver también

[Diario de pagos](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-journal)