Los usuarios pueden vincular transportistas externos a sus bases de datos de Odoo para verificar las entregas que hace un transportista a una dirección específica, [calcular los costos de envío de forma automática](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/delivery_method.html) y [generar etiquetas de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html).

En Odoo, los transportistas se pueden aplicar a una orden de venta, una factura o una orden de entrega. Para consejos sobre cómo resolver problemas comunes al configurar los conectores de envío, vaya a la sección de [Solución de errores](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-third-party-troubles).

 Ver también

- [¿Cómo obtener las credenciales de DHL para la integración con Odoo?](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/dhl_credentials.html)
    
- [Configuración de Sendcloud](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/sendcloud_shipping.html)
    
- [Integración de UPS](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html)
    

A continuación se le presenta una lista de conectores de transportistas disponibles en Odoo:

|Transportista|Disponibilidad por región|
|---|---|
|FedEx|Todos|
|[DHL](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/dhl_credentials.html)|Todos|
|[UPS](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html)|Todos|
|Servicio Postal de los Estados Unidos|Estados Unidos|
|[Sendcloud](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/sendcloud_shipping.html)|Unión Europea|
|Bpost|Bélgica|
|Easypost|América del Norte|
|Shiprocket|India|

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#configuration "Enlazar permanentemente con este título")

Para asegurarse de configurar bien un transportista externo con Odoo siga estas instrucciones:

1. [Instale el conector del transportista](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-shipping-connector).
    
2. [Configure el método de entrega](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-delivery-method).
    
3. [Active el entorno de producción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-production-env).
    
4. [Configure el almacén](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-source-address).
    
5. [Especificar el peso de los productos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-weight).
    

### Instalar conectores de envío[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#install-shipping-connector "Enlazar permanentemente con este título")

Para instalar conectores de envío, vaya a Inventario ‣ Configuración‣ Ajustes.

En la sección Conectores de envío marque la casilla a un lado del transportista externo para instalarlo. Puede seleccionar varios conectores de envío al mismo tiempo. Al finalizar, haga clic en Guardar.

 Nota

Los [métodos de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/delivery_method.html) también pueden integrarse a las operaciones de las aplicaciones _Ventas_, _Comercio electrónico_ y _Sitio web_. Consulte la documentación de [instalación de aplicaciones y módulos](https://www.odoo.com/documentation/17.0/es/applications/general/apps_modules.html#general-install) para obtener más información sobre su instalación.

![Las opciones de conectores de envío disponibles en Odoo.](https://www.odoo.com/documentation/17.0/es/_images/shipping-connectors.png)

### Método de envío[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#delivery-method "Enlazar permanentemente con este título")

Para configurar las credenciales de la API y activar el transportista de envío, primero vaya a Inventario ‣ Configuración ‣ Métodos de envío y seleccione el método correspondiente.

 Nota

Por lo general, la lista incluye **dos** métodos de envío del mismo proveedor: uno para envíos internacionales y otro para envíos nacionales.

Es posible crear métodos de envío adicionales para fines específicos, como [empaquetado](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/packaging.html).

 Ver también

[Configurar métodos de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/delivery_method.html)

 Nota

Asegúrese de que el método de envío esté publicado al mismo tiempo que deba estar disponible en la aplicación _Sitio web_. Para publicar un método de envío en el sitio web, haga clic en el método de entrega deseado, después haga clic en el botón inteligente Sin publicar. Al hacerlo, el botón inteligente cambiará a ser: Publicado.

La página Método de envío contiene detalles sobre el proveedor, incluyendo:

- Método de envío (_campo obligatorio_): el nombre del método de envío (por ejemplo, `FedEx US`, `FedEx EU`, etc.).
    
- Sitio web: configure métodos de envío para una página de _comercio electrónico_ que esté conectada a un sitio web específico de la base de datos. Seleccione el sitio web aplicable en el menú desplegable o déjelo vacío para aplicar el método a todas las páginas web.
    
- Proveedor (_obligatorio_): seleccione el transportista externo, por ejemplo FedEx. Al elegir un proveedor, los campos Nivel de integración, Política de facturación y Porcentaje del seguro estarán disponibles.
    
- Nivel de integración: seleccione Obtener tarifa para obtener un [costo estimado de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-third-party-so) en una [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#id2) o una factura.
    
     Importante
    
    Seleccione Obtener tarifas y crear envíos para también [generar etiquetas de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html).
    
- Empresa: si el método de envío debe aplicarse a una empresa en específico, selecciónela en el menú desplegable. Deje el campo vacío para aplicar ese método a todas las empresas.
    
- Producto de envío (_obligatorio_): el cargo por envío que se agrega a la [|orden de venta|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#id4) o a la factura.
    
- Política de facturación: seleccione y calcule un Costo estimado del envío directamente con el transportista. Si prefiere ver el Costo real de envío, consulte este [documento sobre cómo facturar costos de envío reales](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/invoicing.html).
    
- Margen o tarifa: especifique un porcentaje adicional que se agregue a la tarifa base de envío para cubrir costos adicionales, como tarifas de transporte, materiales de embalaje, tasas de cambio, etc.
    
- Gratuito si el importe de la orden es superior a: activa el envío gratis para órdenes que pasen la cantidad ingresada en el campo cantidad.
    
- Porcentaje del seguro: especifique el porcentaje de una cantidad de los costos de envío que se le reembolsará si el paquete se pierde o se roba durante el transito.
    

![Captura de pantalla sobre el método de envío de FedEx.](https://www.odoo.com/documentation/17.0/es/_images/fedex.png)

Página de configuración del **método de envío** para `FedEx US`.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#id1 "Enlace permanente a esta imagen")

En la pestaña Configuración, llene los campos de las credenciales del API (por ejemplo, la llave, contraseña, número de cuenta, etc. del API). Dependiendo del transportista externo que seleccionó en el campo Proveedor, la pestaña de Configuración contendrá diferentes campos obligatorios. Para más detalles sobre la configuración de las credenciales de transportistas específicos, consulte la siguiente documentación:

 Ver también

- [Credenciales de DHL](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/dhl_credentials.html)
    
- [Credenciales de Sendcloud](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/sendcloud_shipping.html)
    
- [Credenciales de UPS](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/ups_credentials.html)
    

### Entorno de producción[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#production-environment "Enlazar permanentemente con este título")

Una vez configurados los detalles del método de entrega, haga clic en el botón inteligente Entorno de prueba para cambiarlo a Entorno de producción.

 Advertencia

Configurar el método de entrega a Producción crea **etiquetas de envío reales**, y los usuarios corren el riesgo de que se les cobre a través de su cuenta de transportista (por ejemplo, UPS, FedEx, etc.) **antes** de que los usuarios cobren a los clientes por el envío. Verifique que todas las configuraciones sean las correctas antes de lanzar el método de envío a Production.

![Imagen del botón inteligente "entorno de prueba".](https://www.odoo.com/documentation/17.0/es/_images/production.png)

### Configuración del almacén[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#warehouse-configuration "Enlazar permanentemente con este título")

Asegúrese de que la dirección del almacén (incluido el código postal) y el número de teléfono sean correctos. Para ello, vaya a Inventario ‣ Configuración ‣ Almacenes y seleccione el almacén deseado.

En la página de configuración del almacén, abra la página de contacto del almacén haciendo clic en el campo Empresa.

![Resalta el campo "Empresa".](https://www.odoo.com/documentation/17.0/es/_images/internal-link.png)

Verifique que la dirección y el teléfono sean correctos, son necesarios para que el conector de envío funcione de forma adecuada.

![Mostrar la dirección y el teléfono de la empresa.](https://www.odoo.com/documentation/17.0/es/_images/company.png)

### Peso del producto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#product-weight "Enlazar permanentemente con este título")

Para que la integración del transportista funcione bien, especifique el peso de los productos en Inventario ‣ Productos ‣ Productos y seleccione un producto deseado.

Después, vaya a la pestaña Inventario y defina el peso del producto en la sección Logística.

![Visualización del campo "Peso" en la pestaña Inventario del formulario de producto.](https://www.odoo.com/documentation/17.0/es/_images/product-weight.png)

## Aplicar transportistas externos para envíos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#apply-third-party-shipping-carrier "Enlazar permanentemente con este título")

Es posible aplicar transportistas a una orden de venta, una factura o una orden de envío.

Después de configurar el [método de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-delivery-method) del transportista externo en Odoo, vaya a Ventas ‣ Órdenes ‣ Cotizaciones para crear o elegir una cotización.

### Orden de venta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#sales-order "Enlazar permanentemente con este título")

Para asignar un transportista y obtener el costo estimado de un envío, vaya a Ventas ‣ Órdenes ‣ Cotizaciones. Cree o seleccione alguna de las cotizaciones y agregue el costo de envío del transportista externo a ella, haga clic en el botón Agregar envío que se ubica en la esquina inferior derecha de la pestaña Líneas de la orden.

![Visualización del botón "Agregar envío" ubicado en la parte inferior de una cotización.](https://www.odoo.com/documentation/17.0/es/_images/add-shipping.png)

Esta acción abrirá la ventana emergente Agregar un método de envío, allí seleccione el transportista correspondiente con el menú desplegable Método de envío. El campo Costo se completa en automático según:

- La cantidad especificada en el campo Peso total de la orden (si no se proporciona, se utiliza la suma del [peso de los productos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-weight) en la orden).
    
- La distancia entre la [dirección de origen](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-source-address) del almacén y la dirección del cliente.
    

Luego de elegir un transportista externo en el campo Método de envío, haga clic en Obtener tarifa en la ventana Agregar un método de envío para obtener el costo estimado mediante el conector de envío. Después, haga clic en el botón Agregar para agregar el cargo por el envío a la orden de venta o a la factura.

 Ver también

[Cobrar a los clientes por el envío después de la entrega del producto](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/invoicing.html)

### Orden de envío[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#delivery-order "Enlazar permanentemente con este título")

Para que los usuarios hagan envíos sin instalar la aplicación _Ventas_, asigne un transportista a la orden de envío correspondiente en la aplicación Inventario. Luego, desde el tablero de información general de Inventario, elija el tipo de operación Órdenes de entrega y seleccione la orden correspondiente que no esté marcada como Hecho o Cancelado.

En la pestaña Información adicional, seleccione un transportista en el campo correspondiente. Se proporciona una referencia de rastreo cuando el método está configurado como [modo de producción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-delivery-method).

 Ver también

[Generar etiquetas de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/labels.html)

![Visualización de la pestaña "Información adicional" de la orden de entrega.](https://www.odoo.com/documentation/17.0/es/_images/delivery-info.png)

## Solución de problemas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#troubleshooting "Enlazar permanentemente con este título")

En algunos casos puede ser complicado configurar conectores de envío, las siguientes son algunas de las cosas que puede comprobar cuando funcionan de manera distinta a la esperada:

1. Asegúrese de que la [información del almacén](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-configure-source-address) (la dirección y el número telefónico, por ejemplo) en Odoo es correcta **y** que coincide con los registros almacenados en el sitio web del proveedor de envío.
    
2. Verifique que el [tipo de paquete](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/package.html#inventory-warehouses-storage-package-type) y los parámetros son válidos para el transportista. Para comprobar esto, asegúrese de que es posible crear el envío directo desde el sitio web del transportista.
    
3. En caso de que haya una discrepancia en el precio entre el costo estimado de Odoo y el cargo del proveedor, primero asegúrese de que el método de envío corresponde al [entorno de producción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-production-env).
    
    Cree el envío en el sitio web del transportista y en Odoo. Verifique que los precios sean iguales en Odoo, el proveedor de envíos y los _registros de depuración_.
    
     Example
    
    Si al verificar la diferencia de precios en los registros de depuración, la solicitud dice que el paquete pesa seis kilogramos, pero la respuesta de FedEx dice que el paquete pesa siete kilogramos, concluye que el error es de FedEx.
    

### Registro de depuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#debug-log "Enlazar permanentemente con este título")

Active el registro de depuración para llevar registro de las inconsistencias en la información de envío. Vaya a la página de configuración del método de envío (Inventario ‣ Configuración ‣ Métodos de envío) y seleccione uno. Haga clic en el botón inteligente Sin depuración para activar las solicitudes de depuración.

![Visualización del botón "Sin depuración".](https://www.odoo.com/documentation/17.0/es/_images/no-debug.png)

Después de que haya activado las solicitudes de depuración, los registros se guardarán en el reporte de registro cada que use el conector de envío para estimar el costo de envío. Para acceder al reporte, active el [modo de desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode) y vaya a Ajustes ‣ Técnico ‣ sección Estructura de la base de datos ‣ Registros.

 Nota

Se crean registros para un método de envío cada que hace clic en el botón [Obtener tarifa](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html#inventory-shipping-receiving-third-party-rate) en las órdenes de venta y las facturas, **y** cuando un cliente agrega el transportista de envío a su orden a través de la aplicación _Sitio web_.

![Visualización de cómo encontrar la opción "Registros" en el menú "Técnico".](https://www.odoo.com/documentation/17.0/es/_images/log.png)

Haga clic en el elemento de línea _solicitud HTTP_ para abrir una página detallada y verifique que Odoo enviará la información correcta al transportista. En la _respuesta HTTP_, verifique que se reciba la misma información.

![Visualización del historial de solicitudes de depuración en Ajustes > Técnico > Registros.](https://www.odoo.com/documentation/17.0/es/_images/logging.png)