Dependiendo de su negocio y la aplicación que utiliza, hay diferentes maneras de automatizar la creación de facturas de clientes en Odoo. Por lo general, el sistema crea borradores de facturas (con información proveniente de otros documentos como las órdenes de venta o contratos), de manera que contabilidad solo tiene que validar los borradores y enviar las facturas por lote (por correo postal o correo electrónico).

Dependiendo de su negocio, puede optar por una de las siguientes maneras de crear borradores de facturas:

## Ventas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#sales "Enlazar permanentemente con este título")

### Órdenes de venta ‣ Factura[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#sales-order-invoice "Enlazar permanentemente con este título")

En algunas empresas, los vendedores crean cotizaciones que se vuelven órdenes de venta una vez que las validan. Después, se crean borradores de facturas a partir de la orden de venta. Además, cuenta con diferentes opciones como:

- Factura manual: use un botón en la orden de venta para activar los borradores de factura
    
- Factura antes de la entrega: facture la orden completa antes de activar la orden de entrega
    
- Factura basada en la orden de entrega: vea la siguiente sección
    

Normalmente, la aplicación de Comercio electrónico utiliza la factura antes de la entrega cuando el cliente paga al momento de hacer la orden y se entrega después. (prepago)

Para la mayoría de casos de uso, se recomienda facturar manualmente. De esta manera el vendedor puede activar la creación de facturas bajo demanda con las siguientes opciones: facturar la orden completa, facturar un porcentaje (avanzado), facturar algunas líneas, facturar un anticipo fijo.

Este proceso es bueno tanto para los servicios como para los productos físicos.

 Ver también

- [Facturas proforma](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/proforma.html)
    

### Orden de venta ‣ Orden de entrega ‣ Factura[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#sales-order-delivery-order-invoice "Enlazar permanentemente con este título")

Generalmente tanto el comercio electrónico como el minorista facturan basados en órdenes de entrega, en lugar de órdenes de venta. Este enfoque es adecuado para las empresas donde las cantidades que se entregan difieren de las cantidades ordenadas, por ejemplo, alimentos (factura basada en kg).

De esta manera, si entrega una orden parcial, solo se factura por lo que realmente se entregó. Si crea órdenes parciales (entrega unas cosas primero y el resto más adelante), el cliente recibirá dos facturas, una por cada orden de entrega.

 Ver también

- [Facturar por cantidades entregadas u ordenadas](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/invoicing_policy.html)
    

### Orden de comercio electrónico ‣ factura[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#ecommerce-order-invoice "Enlazar permanentemente con este título")

Una orden de comercio electrónico también activará la creación de la orden cuando se pague por completo. Si permite que el pago de las órdenes sea por cheque o transferencia bancaria, Odoo solo creará una orden y la factura se activará una vez que se recibe el pago.

## Contratos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#contracts "Enlazar permanentemente con este título")

### Contratos ordinarios ‣ facturas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#regular-contracts-invoices "Enlazar permanentemente con este título")

Si usa contratos, puede activar la creación de facturas basadas en tiempo y materiales usados, gastos o líneas fijas de servicios/productos. Cada mes, el vendedor generará la factura basada en las actividades del contrato.

Las actividades puede ser:

- productos/servicios fijos, provenientes de una orden de venta vinculada a este contrato,
    
- materiales comprados (que se volverán a facturar),
    
- tiempo y material basado en hojas de trabajo o compras (subcontratación), y
    
- gastos como viajes y alojamiento que se van a volver a facturar al cliente.
    

Puede facturar al momento en el que termine el contrato o también puede generar facturas intermedias. Las empresas que ofrecen servicios y facturan con base en el tiempo y material utilizan este enfoque. En cambio, las empresas de servicio que facturan con base en el precio fijo, usan una orden de venta normal.

 Ver también

- [Facturación por tiempo y materiales](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/time_materials.html)
    
- [Volver a facturar gastos a los clientes](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/expense.html)
    
- [Facturar objetivos de proyecto](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/invoicing/milestone.html)
    

### Contratos recurrentes ‣ facturas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#recurring-contracts-invoices "Enlazar permanentemente con este título")

En el caso de las suscripciones, se activa una factura periódicamente de forma automática. La frecuencia de la facturación y de los servicios/productos facturados se definen en el contrato.

 Ver también

- [Suscripciones](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions.html)
    

## Otros[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#others "Enlazar permanentemente con este título")

### Crear una factura de manera manual[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#creating-an-invoice-manually "Enlazar permanentemente con este título")

Los usuarios también pueden crear facturas de forma manual sin utilizar contratos u órdenes de venta. Este enfoque se recomienda si no necesita administrar el proceso de venta (cotizaciones), o la entrega de los productos o servicios.

Aunque genere la factura de una orden de venta, es probable que deba crear facturas manualmente en los casos de uso extraordinarios:

- si necesita crear un reembolso,
    
- si necesita hacer un descuento,
    
- si necesita modificar la factura creada desde la orden de venta, o
    
- si necesita facturar algo no relacionado con su negocio principal.
    

### Módulos específicos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#specific-modules "Enlazar permanentemente con este título")

También se pueden crear borradores de facturas desde algunos módulos específicos:

- **membresía**: facture cada año a sus miembros
    
- **reparaciones**: facture después de vender sus servicios
    

### Cambiar la secuencia de las facturas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#resequencing-of-the-invoices "Enlazar permanentemente con este título")

Es posible cambiar la secuencia de las facturas, aunque con algunas restricciones:

1. Esta función no está disponible cuando el registro es de una fecha anterior a la del bloqueo.
    
2. Esta función no está disponible cuando la secuencia no coincide con el mes del registro.
    
3. No funciona si la secuencia provoca un duplicado.
    
4. El orden de la factura no se modifica.
    
5. Es útil para las personas que utilizan una numeración proveniente de otro software y que quieren continuar con la numeración del año en curso sin volver a empezar desde cero.
    

### Digitalización de facturas con reconocimiento óptico de caracteres (OCR)[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/overview.html#invoice-digitization-with-optical-character-recognition-ocr "Enlazar permanentemente con este título")

La **digitalización de facturas** es el proceso en el que las facturas impresas se codifican de manera automática y se convierten en formularios de facturas en su contabilidad en línea.

Odoo usa OCR y tecnología de inteligencia artificial para reconocer el contenido de los documentos. Los formularios para las facturas de cliente y proveedor se crean y se llenan según las facturas escaneadas.

 Ver también

- [Digitalización de documentos con IA](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/invoice_digitization.html)