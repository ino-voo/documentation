Usamos las variantes de producto para que productos únicos tengan diferentes características y opciones que los clientes puedan elegir, como tamaño, estilo, color, entre otras.

Puede gestionar las variantes de los productos en la plantilla de cada producto, o si va a la página Variantes de producto o Atributos. Todas estas opciones se encuentran dentro de la aplicación _Ventas_ de Odoo.

 Example

Una empresa de ropa tiene el siguiente desglose de variantes para una de sus camisetas más vendidas:

- Camiseta clásica unisex
    
    - Color: azul, rojo, blanco, negro
        
    - Talla: CH, M, G, XG, XXG
        

Aquí, la **camiseta** es la plantilla del producto y **Camiseta: Azul, S** es una variante de producto específica.

El **tamaño** y el **color** son atributos y las opciones correspondientes (como **azul** y **S**) son los **valores**.

En este caso, hay un total de veinte variantes de producto diferentes: cuatro opciones de **color** multiplicadas por cinco opciones de **tamaño**. Cada variante tiene su propio inventario, total de ventas y otros registros similares en Odoo.

 Ver también

[Variantes de producto](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/variants.html)

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/variants.html#configuration "Enlazar permanentemente con este título")

Para usar variantes de producto, **debe** activar las **variantes** en la aplicación **Ventas** de Odoo.

Para hacerlo, vaya a la aplicación Ventas ‣ Configuración ‣ Ajustes, y ubique la sección Catálogo de producto en la parte superior de la página.

En esta sección, marque la caja para activar la funcionalidad Variantes.

![Imagen sobre la activación de las variantes de productos en la página de ajustes de la aplicación de Ventas.](https://www.odoo.com/documentation/17.0/es/_images/activating-variants-setting.png)

Después, haga clic en Guardar en la parte superior de la página de Ajustes.

## Atributos[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/variants.html#attributes "Enlazar permanentemente con este título")

Antes de poder configurar las variantes de productos, **debe** crear los atributos. Para crear, gestionar y modificar los atributos, vaya a la aplicación de ventas ‣ Configuración ‣ Atributos.

 Nota

El orden de los atributos en la página Atributos determina cómo aparecen en el _configurador de productos_, el tablero de _Punto de venta_ y las páginas de _comercio electrónico_.

Para crear un nuevo atributo desde la página Atributos haga clic en Nuevo. Así se mostrará un formulario de atributo en blanco que usted puede personalizar y configurar de varias maneras.

![Un formulario de creación de atributos en blanco en la aplicación Ventas de Odoo](https://www.odoo.com/documentation/17.0/es/_images/attribute-creation.png)

Primero, cree un Nombre de atributo, como `Color` o `Tamaño`.

Luego seleccione una de las opciones del campo Tipo de visualización. Este determina cómo se mostrará este producto en la tienda en línea, el tablero del _Punto de Venta_ y el _configurador de productos_.

Las Opciones de visualización son:

- Barra: las opciones aparecerán como botones seleccionables en la página de la tienda en línea del producto.
    
- Color: las opciones aparecen como pequeños cuadrados de colores que muestran los códigos de color HTML.
    
- Radio: las opciones aparecerán en una lista con botones de opción en la página de productos de la tienda en línea.
    
- Seleccionar: las opciones aparecen en un menú desplegable en la página del producto en la tienda en línea.
    
- Varias casillas (opción): las opciones aparecen como casillas que se pueden seleccionar en la página del producto de la tienda en línea.
    

![Tipos de visualización en la configuración del producto en la tienda en línea de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/display-types.png)

El campo Modo de creación de variantes le informa a Odoo cuándo debe crear una nueva variante de forma automática después de agregar un atributo a un producto.

 Nota

El campo Modo de creación de variantes **debe** estar configurado con Nunca (opción) para que Varias casillas (opción) funcione de forma correcta como tipo de visualización.

- Instantáneamente: crea todas las variantes posibles tan pronto como se agregan atributos y valores a una plantilla de producto.
    
- Dinámicamente: crea variantes **solo** cuando se agregan atributos y valores correspondientes a una orden de venta.
    
- Nunca (opción): nunca crea variantes de manera automática.
    

 Advertencia

El modo de creación de las variantes de un atributo no se puede editar después de que se agregó a un producto.

El campo Visibilidad del filtro de comercio electrónico determina si el cliente puede ver las opciones de este atributo desde el frontend cuando compran en la tienda en línea.

- Visible: los clientes pueden ver los atributos de los valores desde el frontend.
    
- Oculto: los clientes no pueden ver los atributes de valores desde el frontend.
    

Por último, en el campo opcional Categoría de comercio electrónico, seleccione una categoría en el menú desplegable para agrupar atributos similares en la misma sección para que sean más específicos y estén mejor organizados.

 Nota

Para ver los detalles relacionados con la categoría de atributo seleccionada, haga clic en el icono de enlace interno  (flecha hacia la derecha) que se encuentra del lado derecho del campo Categoría de comercio electrónico después de seleccionar una opción. Esta acción abre el formulario de detalles de esa categoría de atributo.

![Una página de detalles de categoría de atributo estándar a la cual se puede entrar mediante el icono de flecha de enlace interno.](https://www.odoo.com/documentation/17.0/es/_images/attribute-category-internal-link.png)

Aquí, el Nombre de categoría y la Secuencia se muestran en la parte superior, seguido por atributos relacionados asociados con la categoría. Puede arrastrar y soltar estos atributos en el orden de prioridad que quiera.

Puede agregar atributos directamente a la categoría, también puede hacer clic en Agregar una lína.

 Truco

Para crear una categoría de atributo directamente desde este campo, empiece a escribir el nombre de la nueva categoría. Después seleccione Crear o Crear y editar… en el menú desplegable que aparece.

Al hacer clic en Crear, se crea la categoría, la cual podrá editar después. Si hace clic en Crear y editar… se crea la categoría y aparece una ventana emergente para Crear categoría, en donde podrá personalizar y configurar la categoría de inmediato.

### Valores de atributos[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/variants.html#attribute-values "Enlazar permanentemente con este título")

Los valores de los atributos se tienen que agregar en la pestaña Valores de atributo. Puede agregar valores a un atributo a la vez si así lo necesita.

Para agregar un valor, haga clic en Agregar una línea en la pestaña Valores de atributo.

Después, ingrese el nombre del valor en la columna Valor. Después, marque la casilla en la columna Es valor personalizado, si el valor es personalizado (es decir, el cliente brindará especificaciones únicas para este valor en específico).

 Nota

Si selecciona el Tipo de visualización - Color, aparecerá la opción para para agregar un código de color HTML en el lado derecho de la línea de valor, para que sea más fácil para los vendedores y clientes saber exactamente qué opción están seleccionando.

![La pestaña de valores de atributo cuando se hace clic en agregar una línea, donde se muestran columnas personalizadas.](https://www.odoo.com/documentation/17.0/es/_images/attribute-value-add-a-line.png)

Para elegir un color, haga clic en el círculo en blanco en la columna Color, lo cual mostrará una ventana emergente para seleccionar el color HTML.

![Selección de un color desde la ventana emergente para seleccionar HTML que aparece en el formulario del atributo.](https://www.odoo.com/documentation/17.0/es/_images/picking-a-color.png)

En esta ventana emergente, seleccione un color específico, solo tiene que arrastrar el seleccionador de color al tono que quiera y hacer clic para confirmar.

O seleccione un color específico, haga clic en el icono de _gotero_ y seleccione el color deseado que pueda hacer clic en la pantalla.

 Truco

También puede crear atributos desde la plantilla de producto. Agregue una nueva línea y escriba el nombre en la pestaña Variantes.

Una vez que se agrega un atributo a un producto, ese producto se enlista y se puede acceder con el botón inteligente Productos relacionados. Ese botón enlista todos los productos en la base de datos que están utilizando el atributo.

## Variantes de producto[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/variants.html#id1 "Enlazar permanentemente con este título")

Una vez que se crea el atributo, úselo (junto con sus valores) para crear una variante de producto. Para hacerlo, vaya a la aplicación Ventas ‣ Productos ‣ Productos y seleccione un producto existente para ver el formulario de producto deseado. O, haga clic en Crear para crear un producto nuevo al que le puede agregar una variante de producto.

En el formulario de producto, haga clic en le pestaña Atributos y variantes para ver, gestionar y modificar los atributos y valores del producto.

![La pestaña de atributos y valores en un producto común en Ventas de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/attributes-values-tab.png)

Para agregar un atributo a un producto, y valores de atributo subsecuentes, haga clic en Agregar una línea en la pestaña Atributos y valores. Después, seleccione el atributo deseado del menú desplegable que aparece.

 Truco

Puede crear atributos directamente desde la pestaña Atributos y variantes del formulario de producto. Para hacerlo, primero escriba el nombre del nuevo atributo en el campo en blanco y seleccione ya sea Crear o Crear y editar… desde el menú desplegable que aparece.

Al hacer clic en Crear, se crea el atributo, el cual podrá editar después. Si hace clic en Crear y editar… se crea el atributo y aparece una ventana emergente para Crear el atributo, en donde podrá personalizar y configurar la categoría de inmediato.

Una vez que seleccione un atributo en la columna Atributo seleccione los valores específicos de atributo que tiene que aplicar en el producto, desde el menú desplegable disponible en la columna Valores.

 Nota

No hay límite sobre cuántos valores puede agregar.

 Truco

Puede acceder a los procesos de creación de variantes para productos similares a través de las aplicaciones Compra, Inventario y Comercio electrónico.

### Configurar variantes[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/variants.html#configure-variants "Enlazar permanentemente con este título")

A la derecha de la línea de atributo está el botón Configurar. Al hacer clic, Odoo mostrará una página separada con esos Valores de variantes de producto específicos.

![Puede acceder a la página Valores de variantes de producto con el botón Configurar en un formulario de producto.](https://www.odoo.com/documentation/17.0/es/_images/product-variant-values.png)

Aquí puede ver el nombre específico de Valor, Índice de color HTML (si aplica) y el Valor del precio adicional.

 Nota

El Valor de precio adicional representa cuánto aumentará el precio de venta si se selecciona el atributo.

Cuando se hace clic en la página Valores de variantes de producto Odoo mostrará una página a parte donde verá los detalles relacionados a los valores.

![Una página de valores de la variante de producto a la que se puede acceder a través de la página general Valores de variantes de producto.](https://www.odoo.com/documentation/17.0/es/_images/product-variant-value-page.png)

En esa página de detalles de la variante específica podrá encontrar los campos Valor y Valores de variantes de producto, así como un campo Excluir para.

En el campo Excluir para puede agregar Plantillas de producto y Valores de atributo específicos. Al hacerlo, este valor de atributo específico se excluirá de esos productos.

### Botón inteligente de variantes[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/variants.html#variants-smart-button "Enlazar permanentemente con este título")

Cuando un producto tiene atributos y variantes configurados en la pestaña Atributos y variantes, aparecerá un botón Variantes en la parte superior del formulario del producto. El botón inteligente Variantes indica cuántas variantes están configuradas en ese producto en específico.

![El botón inteligente de variantes en la parte superior del formulario de producto en Ventas.](https://www.odoo.com/documentation/17.0/es/_images/variants-smart-button.png)

Cuando se hace clic en el botón inteligente Variantes, Odoo mostrará una página separa donde podrá ver todas las combinaciones de variantes de productos configuradas

![Puede acceder a la página de variantes mediante el botón inteligente variantes en el formulario de producto de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/variants-page.png)

## Impacto de variantes[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/products_prices/products/variants.html#impact-of-variants "Enlazar permanentemente con este título")

Además de ofrecer opciones de productos más detalladas a los clientes, las variantes de producto tienen sus propios impactos y puede aprovecharlas en toda la base de datos de Odoo.

- Código de barras: los códigos de barra están asociados con cada variante en lugar de cada plantilla de producto. Cada variante individual puede tener su propio código de barras o SKU.
    
- Precio: cada variante de producto tiene su propio precio público, el cual es la suma de la plantilla del producto _y_ cargos adicionales para atributos particulares.
    
     Example
    
    El precio de una playera roja es $23, porque el precio en la plantilla de la playera es $20, más unos $3 adicionales por la variante del color rojo. Las reglas de la lista de precios se pueden configurar para aplicarse a la plantilla del producto, o a la variante.
    
- Inventario: el inventario se cuenta por cada variante de producto individual. En el formulario de la plantilla del producto, el inventario refleja la suma de todas las variantes, pero el inventario real se calcula según las variantes individuales.
    
- Imagen: cada variante de producto puede tener su propia imagen específica.
    

 Nota

Los cambios a la plantilla del producto se aplican de forma automática a cada variante de ese producto.

 Ver también

importar