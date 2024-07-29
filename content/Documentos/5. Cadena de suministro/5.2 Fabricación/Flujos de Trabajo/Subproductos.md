Al fabricar algunos productos, es común que le sobren materiales una vez que terminó el producto. Estos materiales se llaman _subproductos_, al especificar los subproductos que se crearon durante la fabricación en una lista de materiales de un producto, la cantidad de los subproductos se marcará en Odoo.

 Example

Se necesitan diez piezas de madera para fabricar una _mecedora_. Durante la producción, además de la mecedora, se crean cinco piezas de _madera de desecho_. Al designar la madera de desecho como un subproducto en la lista de producto correspondiente, Odoo rastrea la cantidad disponible de madera de desecho, así como el número de mecedoras producidas.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#configuration "Enlazar permanentemente con este título")

Para especificar subproductos en la [|lista de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#id1) de un producto, **debe** activar la función _subproductos_. Para hacerlo vaya a la aplicación Fabricación‣ Configuración ‣ Ajustes y marque la casilla de verificación subproductos ubicada debajo del encabezado Operaciones. Después, haga clic en guardar para aplicar el cambio.

![El ajuste "subproductos" en la página de ajustes de la aplicación Fabricación.](https://www.odoo.com/documentation/17.0/es/_images/byproducts-setting.png)

Una vez que active los subproductos, una pestaña con el mismo nombre aparecerá en las [|listas de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#id3) de los poductos.

## Agregar subproductos a listas de materiales[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#add-byproduct-to-bom "Enlazar permanentemente con este título")

Para agregar subproductos a [|listas de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#id5) vaya a la aplicación Fabricación ‣ Productos ‣ Lista de materiales y seleccione una [|lista de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#id7).

En la [|lista de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#id9) vaya a la pestaña subproductos, haga clic en Agregar una línea y seleccione un subproducto en el campo desplegable subproducto. En el campo Cantidad ingrese la cantidad de los subproductos que se produjeron en la fabricación.

Si el subproducto que se produjo durante una operación específica de una orden de fabricación, seleccione la operación en el campo Producido en la operación. Por ejemplo, si se produjo un subproducto de un pedazo de madera durante la operación _Ensamblaje_, seleccione esa operación en el campo Producido en la operación.

![La pestaña "subproductos" en una lista de materiales, con un "pedazo de madera" como 'subproducto'.](https://www.odoo.com/documentation/17.0/es/_images/byproducts-tab.png)

## Subproducto de fabricación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#manufacture-by-product "Enlazar permanentemente con este título")

Cuando se completa una [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#id11) y se marca como _Hecha_, Odoo registra la cantidad de subproductos que se crearon durante el proceso de fabricación. Para crear una [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#id13) nueva, vaya a la aplicación Fabricación ‣ Operaciones ‣ Órdenes de fabricación y haga clic en guilabel:`Nuevo`.

En el campo Lista de materiales seleccione una [|lista de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#id15) en la que se haya especificado un subproducto. Después de hacerlo, el campo Producto se llena de forma automática con el producto correspondiente. Haga clic en Confirmar para confirmar la [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#id17).

Cuando se complete la fabricación, haga clic en el botón Producir todo en la parte superior de la [|orden de fabricación|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/byproducts.html#id19). Después de hacerlo, los números del inventario se actualizan para reflejar la cantidad de subproductos que se produjeron, así como la cantidad del producto.

Haga clic en el botón inteligente Movimientos de producto ubicado en la parte superior de la página de la orden de fabricación para ver los movimientos de componentes y productos. Cada subproducto aparece en la página Movimientos de inventario, en la columna De está la ubicación virtual de producción y la columna A tiene la ubicación donde se almacena el subproducto.

![La página de movimientos de producto para una orden de fabricación con subproductos.](https://www.odoo.com/documentation/17.0/es/_images/product-moves.png)