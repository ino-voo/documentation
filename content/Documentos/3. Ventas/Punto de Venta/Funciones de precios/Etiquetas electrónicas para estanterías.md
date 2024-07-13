Las etiquetas electrónicas para estanterías permiten mostrar información sobre los productos, como precios y códigos de barras, en las estanterías de las tiendas y sincronizarlas a distancia desde el backend. Esto elimina la necesidad de imprimir nuevas etiquetas cuando cambia la información del producto.

![etiqueta electrónica de Pricer](https://www.odoo.com/documentation/17.0/es/_images/electronic-label.png)

 Nota

Odoo usa etiquetas electrónicas de [Pricer](https://www.pricer.com/).

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/electronic_labels.html#configuration "Enlazar permanentemente con este título")

### Configuración de Pricer[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/electronic_labels.html#pricer-setup "Enlazar permanentemente con este título")

1. [Póngase en contacto con Pricer](https://www.pricer.com/contact) para crear y configurar su cuenta de Pricer.
    
2. Cree sus tiendas: una tienda de pricer equivale a una tienda física.
    
3. Vincule tantos transceptores como sea necesario a la(s) tienda(s) Pricer.
    
4. Cree las siguientes variables para compartir información de producto entre su sistema de base de datos Odoo y Pricer. Estas variables actúan como marcadores de posición en la plantilla de etiqueta.
    
    - `itemId`: contiene el identificador interno único asignado a cada producto
        
    - `itemName`: el nombre del producto
        
    - `price`: el precio de venta del producto, con impuestos aplicables.
        
    - `presentation`: el nombre de la plantilla utilizada en Pricer para mostrar la información del producto en la etiqueta
        
    - `currency`: la divisa de su empresa (por ejemplo, USD, EUR)
        
    - `barcode`: el número de código de barras asociado a cada producto.
        
    
     Importante
    
    Los nombres de estas variables deben ser **idénticos** en su base de datos Pricer.
    
5. Cree una plantilla llamada `NORMAL`. Esta plantilla se usa para mostrar información sobre las etiquetas digitales.
    

Una vez que su cuenta, tiendas, variables y plantillas estén configuradas en Pricer, ahora puede empezar a configurar su base de datos de Odoo.

 Importante

La cuenta asociada a su tienda de Pricer debe tener acceso para enviar solicitudes de API a Pricer.

### Configuración en Odoo[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/electronic_labels.html#odoo-setup "Enlazar permanentemente con este título")

Como requisito previo, [active](https://www.odoo.com/documentation/17.0/es/applications/general/apps_modules.html#general-install) el módulo Etiquetas electrónicas para PdV _(nombre técnico pos_pricer)_ para tener todas las funciones para usar las etiquetas electrónicas Pricer.

![Instalación del módulo Etiquetas electrónicas para PdV desde las aplicaciones](https://www.odoo.com/documentation/17.0/es/_images/pricer-module.png)

Una vez que se active el módulo, configure sus [tiendas Pricer](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/electronic_labels.html#pricer-tags-stores) y asocie las [etiquetas electrónicas](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/electronic_labels.html#pricer-tags-tags) a sus productos.

#### Tiendas Pricer[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/electronic_labels.html#pricer-stores "Enlazar permanentemente con este título")

De forma similar a la configuración en Pricer, necesita crear una tienda Pricer por ubicación física. Para ello, vaya a Punto de venta ‣ Configuración ‣ Tiendas Pricer, haga clic en Nuevo, y rellene la línea con la información requerida:

- Nombre de la tienda: puede poner el nombre que quiera.
    
- Nombre del tenedor de Pricer: el nombre de su cuenta de empresa en Pricer, normalmente seguido de `country_code`. Este valor lo proporciona Pricer.
    
- Inicio de sesión en Pricer: el nombre de usuario de su cuenta Pricer.
    
- Contraseña Pricer: la contraseña de su cuenta de Pricer.
    
- ID de la tienda Pricer: el identificador de la tienda Pricer relacionada, tal y como está definido en su base de datos Pricer.
    

![Configuración de una tienda Pricer](https://www.odoo.com/documentation/17.0/es/_images/pricer-stores-setup.png)

 Nota

- La columna Etiquetas de Pricer se actualiza automáticamente cuando se vincula una etiqueta a un producto.
    
- Las columnas Última actualización y Estado de la última actualización se actualizan de forma automática cuando las etiquetas se cambian.
    

#### Etiquetas de Pricer[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/electronic_labels.html#pricer-tags "Enlazar permanentemente con este título")

Para que una etiqueta muestre información específica del producto, la etiqueta debe estar asociada con el producto. Para hacerlo:

1. Abra el formulario de producto en Punto de venta ‣ Productos ‣ Productos y haga clic en Nuevo o seleccione un producto existente.
    
     Nota
    
    Si está creando un producto nuevo, configúrelo y guárdelo antes de asociarlo a las etiquetas de Pricer.
    
2. Vaya a la pestaña Ventas, baje a la sección Pricer y seleccione la Tienda Pricer correspondiente.
    
    ![Vincular productos a etiquetas Pricer](https://www.odoo.com/documentation/17.0/es/_images/pricer-product.png)
    
3. Copie el ID de la etiqueta desde la etiqueta misma o escanee el código de barras para llenar el campo ID de etiquetas de Pricer.
    
     Nota
    
    Los ID de Pricer están formados por una letra seguida por 16 dígitos.
    

 Truco

- Le recomendamos que use el escáner de código de barras para agilizar el proceso de codificación.
    
- Al configurar Pricer en Odoo por primera vez, le recomendamos que configure solo un producto. Antes de configurar más, asegúrese de que puede mostrar información en le etiqueta Pricer.
    

Ahora que tiene productos asociados a su etiqueta Pricer, podemos enviar la información a Pricer.

### Aplicación práctica[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/electronic_labels.html#practical-application "Enlazar permanentemente con este título")

Odoo envía solicitudes a Pricer de forma automática para sincronizar las etiquetas cada 12 horas para modificar:

> - el nombre del producto, precio, código de barras o impuestos para el cliente
>     
> - Moneda
>     
> - Tienda o etiquetas Pricer asociadas
>     

Para forzar una actualización, active el [modo de desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode) y después:

1. Vaya a Punto de venta ‣ Configuración ‣ Tienda Pricer.
    
2. Seleccione la o las tiendas deseadas.
    
3. Haga clic en Actualizar etiquetas para actualizar todas las etiquetas que se verán afectadas por estos cambios:
    
    - el nombre del producto, precio, código de barras o impuestos para el cliente
        
    - Moneda
        
    - Tienda o etiquetas Pricer asociadas
        

También puede hacer clic en Actualizar todas las etiquetas para forzar una actualización en cada etiqueta, sin importar si se hicieron cambios.

![Actualizar todas las etiquetas de Pricer](https://www.odoo.com/documentation/17.0/es/_images/update-all.png)

Si una etiqueta de Pricer procesó y aceptó una solicitud, el campo de estado será La actualización se pudo enviar a Pricer. Si hay algún problema, el sistema mostrará un mensaje de error.

 Advertencia

Si una solicitud enviada a Pricer falla, Odoo igualmente considerará que ese producto se actualizó. En ese caso, le recomendamos forzar una actualización en todas las etiquetas.