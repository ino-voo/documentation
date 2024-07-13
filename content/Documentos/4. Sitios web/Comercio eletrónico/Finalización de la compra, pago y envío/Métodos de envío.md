Según su estrategia de envío, puede elegir entre [métodos de envío propios](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/shipping.html#ecommerce-own-shipping), o puede usar une integración [con un proveedor de envíos existente](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/shipping.html#ecommerce-shipping-providers).

 Ver también

[Proceso de pago](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/checkout.html)

## Métodos de envío propios[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/shipping.html#own-shipping-methods "Enlazar permanentemente con este título")

Puede crear sus propios métodos de envío personalizados y definir reglas para calcular los costos de envío. Para hacerlo, vaya a Sitio web ‣ Configuración ‣Métodos de envío, donde puede seleccionar un método de envío **existente**, o crear uno. Si decide crear un método de envío, podrá elegir entre un [precio fijo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/delivery_method.html), con base en reglas, o recoger en tienda.

### Recoger en tienda[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/shipping.html#pickup-in-store "Enlazar permanentemente con este título")

Primero debe **activar** la opción Recoger en tienda en los ajustes (Sitio web ‣ Configuración ‣ Ajustes ‣ Envío), solo tiene que hacer clic en Pagos y recolección en tienda física. Una vez que lo haya activado, puede seleccionar y personalizar sitios de recolección. Los sitios de recolección pueden ser **específicos para el sitio web**, pero de manera predeterminada están disponibles en _todos_ los sitios web.

 Ver también

- [Métodos de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/delivery_method.html)
    
- [Facturación del costo de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/invoicing.html)
    
- [Envío en varios paquetes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/multipack.html)
    
- [¿Cómo cancelar una solicitud de envío a un transportista?](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/cancel.html)
    

## Proveedores de envío[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/shipping.html#shipping-providers "Enlazar permanentemente con este título")

Otra solución es utilizar alguna de las integraciones con un proveedor de envío existente. La ventaja de utilizar una integración es que los costos de envío se calculan de forma automática según cada orden y también se generan sus etiquetas.

 Ver también

- [Transportistas externos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html)
    
- [Integración de UPS](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html)
    
- [¿Cómo obtener las credenciales de DHL para la integración con Odoo?](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/dhl_credentials.html)
    
- [Imprimir etiquetas de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html)
    

## Disponibilidad para sitio web[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/shipping.html#website-availability "Enlazar permanentemente con este título")

Los métodos de envío se pueden habilitar _solo_ en sitios web **específicos** si así lo quiere. Para hacerlo, debe ir a Sitio web ‣ Configuración ‣ Ajustes ‣ Envío, y seleccione el **método de envío** deseado. En el campo Sitio web seleccione el sitio web al cual quiere que se limite este método de envío. Si lo deja **vacío** el método de envío estará disponible en **todos** los sitios web.

## Método de entrega al finalizar la compra[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/checkout_payment_shipping/shipping.html#delivery-method-at-checkout "Enlazar permanentemente con este título")

Los clientes puede elegir el método de envío al final del proceso de pago, al llegar al paso Confirmar orden.

![Elección del método de entrega al finalizar la compra](https://www.odoo.com/documentation/17.0/es/_images/shipping-checkout.png)