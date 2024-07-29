## Información general[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/label_type.html#overview "Enlazar permanentemente con este título")

En Odoo, puede seleccionar varios tipos de etiquetas de envío para las órdenes de entrega. Según el tipo de paquetes a utilizar, puede que algunos tamaños de etiquetas sean más apropiados y puede configurarlos para que se adapten al paquete.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/label_type.html#configuration "Enlazar permanentemente con este título")

En el módulo Inventario, vaya a Configuración ‣ Entrega ‣ Métodos de envío. Elija uno y haga clic en Editar. Para el siguiente ejemplo, se utilizará _FedEx Internacional_.

![Diferentes métodos de envío.](https://www.odoo.com/documentation/17.0/es/_images/shipping-options.png)

En la pestaña de Configuración, elija uno de los tipos de etiquetas disponibles en Tipo de etiqueta. La disponibilidad variará según el transportista.

![Seleccione un tipo de etiqueta.](https://www.odoo.com/documentation/17.0/es/_images/label-type-dropdown.png)

Cuando se confirma una orden de venta con la empresa de transporte correspondiente y se valida una orden de entrega, la etiqueta de envío se creará como un PDF de forma automática y aparecerá en el Chatter.

## Crear una orden de venta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/label_type.html#create-a-sales-order "Enlazar permanentemente con este título")

En la aplicación Ventas haga clic en Nuevo y seleccione un cliente internacional. Haga clic en Agregar producto y seleccione un artículo. Luego, haga clic en Agregar un envío, seleccione un método de envío, presione Obtener tarifa, y por último, haga clic en Agregar.

![Agregar un método de envío y una tarifa a una orden de venta.](https://www.odoo.com/documentation/17.0/es/_images/shipping-rate.png)

Una vez que confirma la cotización al hacer clic en Confirmar, aparecerá un botón inteligente Entrega.

![Botón inteligente de entrega de la orden.](https://www.odoo.com/documentation/17.0/es/_images/shipping-italy-so.png)

Una vez que la orden a entregar está validada tras hacer clic en Validar, los documentos del envío aparecen en el Chatter.

![Documentos PDF del envío.](https://www.odoo.com/documentation/17.0/es/_images/shipping-pdfs.png)

## Etiquetas de ejemplo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/label_type.html#example-labels "Enlazar permanentemente con este título")

El tipo de etiqueta predeterminado es papel tamaño carta. El siguiente es un ejemplo de una etiqueta tamaño carta de FedEx:

![Etiqueta de envío en tamaño carta a página completa de FedEx .](https://www.odoo.com/documentation/17.0/es/_images/full-page-fedex.png)

Este es un ejemplo de una etiqueta de la mitad inferior de FedEx, para que pueda compararlas:

![Etiqueta de envío en tamaño carta a media página de FedEx .](https://www.odoo.com/documentation/17.0/es/_images/half-page-fedex.png)