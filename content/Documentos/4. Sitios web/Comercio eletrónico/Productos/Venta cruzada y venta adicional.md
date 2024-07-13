Cualquier proceso de venta es una oportunidad para aumentar los ingresos. **Las ventas cruzadas y ventas adicionales** son técnicas de venta que consisten en vender a los clientes productos y servicios adicionales o más caros que los que estaban comprando en un principio. Es una excelente forma de aumentar el valor de cada uno de sus clientes.

La **venta cruzada** se puede realizar con **dos** funciones:

- [Productos opcionales](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/cross_upselling.html#cross-upselling-optional) al **agregar al carrito**.
    
- [Accesorios](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/cross_upselling.html#cross-upselling-accessory) en la **página de pago**.
    

La **venta adicional** solo se realiza a través de [productos alternos](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/cross_upselling.html#cross-upselling-alternative) en la **página de producto**.

 Ver también

[Catálogo](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/catalog.html)

## Venta cruzada[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/cross_upselling.html#cross-selling "Enlazar permanentemente con este título")

### Productos opcionales[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/cross_upselling.html#optional-products "Enlazar permanentemente con este título")

Los **productos opcionales** se sugieren cuando los clientes hacen clic en Añadir al carrito, ya sea desde la **página del producto** o desde la **página del catálogo**. Al hacer clic, se abre una ventana emergente con los **productos opcionales** mostrados en la sección Opciones disponibles.

![Productos opcionales y venta cruzada](https://www.odoo.com/documentation/17.0/es/_images/cross_upselling-cart.png)

Para activar **productos opcionales** vaya a Sitio web ‣ Comercio electrónico ‣ Productos, seleccione un producto, vaya a la pestaña Ventas e introduzca los productos que desea incluir en el campo Productos opcionales. Los productos opcionales están **vinculados** al producto o productos con los que están configurados en la **plantilla de producto**. Solo aparecen cuando ese producto se añade al carrito.

 Truco

También puede llegar a la pestaña de ventas`de la **plantilla del producto** al seleccionar un producto en la **página principal de su tienda** y hacer clic en :guilabel:`Producto, ubicado en la esquina superior derecha.

### Accesorios[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/cross_upselling.html#accessory-products "Enlazar permanentemente con este título")

Los **accesorios** se muestran en la sección accesorios sugeridos en el paso Revisar orden antes del pago.

![Accesorios sugeridos durante la confirmación del carrito.](https://www.odoo.com/documentation/17.0/es/_images/cross_upselling-checkout.png)

Para activar los **accesorios** vaya a Sitio web ‣ Comercio electrónico ‣ Productos, seleccione un producto, vaya a la pestaña Ventas e introduzca los productos que desea incluir en el campo Accesorios. Estos están **vinculados** al producto o productos con los que están configurados en la **plantilla de producto**. Solo aparecen durante la confirmación de la orden.

## Ventas adicionales[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/cross_upselling.html#upselling "Enlazar permanentemente con este título")

### Productos alternos[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/cross_upselling.html#alternative-products "Enlazar permanentemente con este título")

Los **productos alternos** se sugieren en la **página de producto** y suelen incentivar a los clientes a comprar una variante o producto más caro que el que estaban comprando inicialmente.

![Productos alternos en la página de producto](https://www.odoo.com/documentation/17.0/es/_images/cross_upselling-alternative.png)

Para habilitar la función **productos alternos** vaya a Sitio web ‣ Comercio electrónico ‣ Productos, seleccione un producto, vaya a la pestaña Ventas e introduzca los productos que desea que aparezcan en el campo productos alternos. Luego, vaya a la **página de producto** relacionada al hacer clic en ir al sitio web y haga clic en editar. Vaya a la pestaña bloques y baje a la sección contenido dinámico. Luego, arrastre y suelte el bloque de creación productos en cualquier parte de la **página de producto**.

Una vez colocado, en el modo de edición, haga clic en el **bloque** para acceder a varios ajustes para ese bloque de creación productos. En el campo filtro seleccione productos alternos. Puede configurar varios ajustes adicionales, como cuántos elementos se muestran (elementos recolectados), la plantilla utilizada, etc.