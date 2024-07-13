La función **sets de productos** permite que los usuarios definan y gestionen las opciones de combinación para un solo producto.

A esta función en el contexto de un restaurante también se le conoce como combo y permite que los usuarios creen menús con varias opciones. Por ejemplo, un usuario puede definir un plato fuerte y especificar distintas opciones para guarniciones, bebidas o postres para que los clientes las puedan ordenar con el plato fuerte.

En el contexto de venta al público, esta función le permite crear un set de productos con varios productos para elegir y combinar.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/combos.html#configuration "Enlazar permanentemente con este título")

Primero, es necesario que cree algunas opciones de combinación mediante las siguientes instrucciones:

1. Vaya a Punto de venta ‣ Productos ‣ Sets de productos y haga clic en Nuevo.
    
2. Asígnele un nombre a la combinación y haga clic en Agregar una línea para agregar los productos entre los que los clientes pueden elegir. También puede incluir un precio adicional para cada opción en la columna correspondiente.
    

 Nota

Como referencia, el precio original del producto seleccionado aparece en la columna Precio original.

![../../../_images/combo-form.png](https://www.odoo.com/documentation/17.0/es/_images/combo-form.png)

Después, deberá crear un producto específico para reunir las opciones del set con las siguientes instrucciones:

1. Vaya a Punto de venta ‣ Productos ‣ Productos y haga clic en Nuevo.
    
2. Seleccione Set como Tipo de producto y complete la pestaña Información general.
    
     Nota
    
    El precio de venta del producto de set es fijo y no varía según el precio individual de los artículos incluidos ni de la cantidad de artículos incluidos. En su precio solo influye el precio adicional que se define de forma opcional al crear la elección del set o si la variante de uno de los artículos tiene un precio adicional establecido.
    
3. Vaya a la pestaña Opciones para el set, haga clic en Agregar una línea y seleccione las que desee agregar. También puede crear uno nuevo en este paso si hace clic en Nuevo en la ventana emergente.
    

![../../../_images/combo-product-form.png](https://www.odoo.com/documentation/17.0/es/_images/combo-product-form.png)

Una vez que creó y agregó opciones para el set de un producto podrá venderlo en su tienda o restaurante.

## Aplicación práctica[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/combos.html#practical-application "Enlazar permanentemente con este título")

[Abra una sesión de PdV](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#pos-session-start) y seleccione el producto de set. Elija las opciones y haga clic en Agregar a la orden. Recuerde que el precio adicional aparece debajo de las opciones relacionadas.

![../../../_images/combo-select.png](https://www.odoo.com/documentation/17.0/es/_images/combo-select.png)

 [Edit on GitHub](https://github.com/odoo/documentation/edit/17.0/content/applications/sales/point_of_sale/combos.rst)

##### EN ESTA PÁGINA

- - [Configuración](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/combos.html#configuration)
    - [Aplicación práctica](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/combos.html#practical-application)