Las variantes de productos son variaciones del mismo producto, como colores, materiales, etc. El precio y disponibilidad de las variaciones puede diferir de los del producto original. Puede [crear](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/variants.html) o [importar](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/import.html) las variantes de producto.

Para utilizar variantes de producto, habilite la función en Sitio web ‣ Configuración ‣ Ajustes, vaya a la sección Tienda - Productos.

 Ver también

- [Gestión de productos](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/products.html)
    
- [Variantes de producto](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/variants.html)
    
- [Importar productos](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/import.html)
    

## Configurador de productos[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/variants.html#product-configurator "Enlazar permanentemente con este título")

Agregar atributos y valores a una plantilla de producto permite habilitar el **configurador de productos** en la página del producto. Los clientes pueden utilizarlo para configurar y seleccionar la variante de producto de su elección o, en el caso de varios atributos, puede combinarlos para crear una variante específica.

![Configurador de variantes](https://www.odoo.com/documentation/17.0/es/_images/variants-configurator.png)

Puede editar **cómo se muestra en pantalla** cada atributo del configurador de productos en el **Creador de sitios web**. Solo haga clic en Editar ‣ Personalizar en la página del producto y luego haga clic en uno de los atributos. Puede seleccionar una de las siguientes cuatro opciones:

- Radio
    
- Pildoras
    
- Seleccionar
    
- Color
    

![Opciones para mostrar tributos en pantalla](https://www.odoo.com/documentation/17.0/es/_images/variants-display-type.png)

También puede cambiar **cómo se muestran los atributos** en Sitio web ‣ Comercio electrónico ‣ Atributos, seleccione un **atributo** y elija cómo se muestra en pantalla. También puede hacerlo en la **plantilla de producto**, vaya a Comercio electrónico ‣ Productos, seleccione un producto y haga clic en atributos y variantes.

 Truco

Puede excluir combinaciones de valores específicas del configurador de producto. De esta forma, los clientes no pueden seleccionar la combinación de valores excluida. Para hacerlo, vaya a Sitio web ‣ Comercio electrónico ‣ Productos, seleccione un producto y vaya a atributos y variantes. Después, haga clic en un **atributo**, seleccione un **valor** y, en la sección excluir para, seleccione una plantilla de producto y los valores de atributos que se deben excluir.

## Especificaciones de producto[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/variants.html#product-specifications "Enlazar permanentemente con este título")

Los valores que se utilizan para cada atributo se muestran en una **lista de especificaciones** al final de la página de producto. Para que aparezca en la página, primero debe habilitar la función **lista de especificaciones** en la página del producto. Vaya a Editar ‣ Personalizar y seleccione dónde colocar el campo especificaciones.

![Lista de especificaciones en la página del producto](https://www.odoo.com/documentation/17.0/es/_images/variants-specifications.png)

 Truco

También puede utilizar **listas de especificaciones** con productos que no tienen variantes. Para hacerlo, asegúrese de no tener ninguna combinación de valores. Los productos con valores singulares de atributos no generan variantes.

## Filtrar el catálogo por atributos[](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/variants.html#filter-catalog-by-attributes "Enlazar permanentemente con este título")

Los clientes **pueden** [filtrar](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/catalog.html#ecommerce-browsing) el **catálogo** según los atributos y valores del producto, solo aparecerán aquellos que coincidan con su selección.

Para habilitar el **filtrado de atributos**, vaya a Editar ‣ Personalizar en la **página principal de su tienda** y haga clic en una de las categorías de la columna a la izquierda. Habilite las opciones izquierda, arriba o **ambas**, en el campo atributos.

![Botones de categorías](https://www.odoo.com/documentation/17.0/es/_images/variants-categories.png)