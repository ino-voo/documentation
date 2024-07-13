Los productos de suscripciones se pueden vender en la tienda del _comercio electrónico_ de Odoo como un producto normal.

Sin embargo, de forma predeterminada, la página del producto de Comercio electrónico **solo** muestra el periodo de recurrencia más corto que aparece en la pestaña Precios recurrentes del formulario del producto.

Por ejemplo, si un producto de suscripción tiene los periodos de recurrencia _mensual_ y _anual_ configurados, entonces _solo_ el precio mensual aparecerá de forma predeterminada en la página de Comercio electrónico de ese producto.

Para agregar más periodos recurrentes en la página del producto del comercio electrónico, cree una _variante de producto_ para cada periodo recurrente.

 Ver también

- [Configure productos de suscripción](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/products.html)
    
- [Variantes de producto](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/variants.html)
    

## Cree periodos recurrentes como variantes de producto[](https://www.odoo.com/documentation/17.0/es/applications/sales/subscriptions/ecommerce.html#create-recurrence-periods-as-product-variants "Enlazar permanentemente con este título")

Para establecer cada periodo recurrente como una variante de producto, vaya a :menuselection:` la aplicación Suscripciones –> Productos –> Productos` y seleccione un producto. En la pestaña Atributos y variantes, haga clic en Agregar una línea.

Después, cree un atributo llamado `Periodo de facturación` (o algo similar) escribiendo el nombre y haciendo clic en Crear en el menú desplegable pequeño que aparece. Este nombre de atributo aparece como la opción principal en la página del producto en la tienda del comercio electrónico.

Después, cree Valores que correspondan a los periodos de recurrencia que se configuraron en la pestaña Precios recurrentes del formulario del producto.

Para hacer eso, ingrese el nombre del periodo de recurrencia en la columna Valores, en la misma línea de Atributo, en la pestaña Atributos y variantes. Después, haga clic en Crear en el menú desplegable que aparece.

Estos nombres de valores aparecen como opciones seleccionables en la página del producto de la tienda de comercio electrónico.

![Periodos recurrentes configurados como variantes de producto en la pestaña  "Atributos y Variantes" del formulario del producto.](https://www.odoo.com/documentation/17.0/es/_images/recurrence-period-attributes-variants.png)

Con esta configuración lista y guardada, aparecerá una columna Variantes de producto en la pestaña Precios recurrentes. Asigne diferentes Variantes de producto a su respectivo Periodo y Precio de recurrencia.

![Las variantes de producto en la pestaña *Precio basado en tiempo* del formulario del producto.](https://www.odoo.com/documentation/17.0/es/_images/product-variants-time-based-pricing.png)

Después de seguir los pasos anteriores, las variantes de producto estarán disponibles para seleccionarlas en la página de producto de Comercio electrónico.

![Periodos recurrentes configurados como variantes de producto en la página del producto del comercio electrónico.](https://www.odoo.com/documentation/17.0/es/_images/recurrence-period-ecommerce.png)