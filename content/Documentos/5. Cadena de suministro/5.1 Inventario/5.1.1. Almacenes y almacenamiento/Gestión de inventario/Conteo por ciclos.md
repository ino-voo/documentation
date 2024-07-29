Para la mayoría de las empresas solo es necesario contar el inventario una vez al año. Así que luego de hacer un _ajuste de inventario_ en Odoo, la fecha del próximo conteo se programará de forma predeterminada para el 31 de diciembre del año en curso.

Sin embargo, para algunas empresas es esencial contar con un conteo de inventario correcto en todo momento. Estas empresas usan _recuentos cíclicos_ para mantener los niveles de inventario importantes actualizados. El recuento cíclico es un método que las empresas usan para contar su inventario más seguido en algunas _ubicaciones_ para asegurarse de que el inventario físico va con los registros de su inventario.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/cycle_counts.html#configuration "Enlazar permanentemente con este título")

En Odoo, los conteos cíclicos se realizan por ubicación. Es necesario que habilite la función _Ubicaciones de inventario_ antes de realizar uno.

Para activar esta función vaya a Inventario ‣ Configuración ‣ Ajustes y diríjase a la sección Almacén. Haga clic en la casilla ubicada junto a Ubicaciones de almacenamiento y haga clic en Guardar.

![La función ubicaciones de almacenamiento habilitada en los ajustes de Inventario.](https://www.odoo.com/documentation/17.0/es/_images/cycle-counts-enabled-setting.png)

## Cambiar la frecuencia del recuento de inventario por ubicación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/cycle_counts.html#change-inventory-count-frequency-by-location "Enlazar permanentemente con este título")

Una vez que la función _Ubicaciones de almacenamiento_ está habilitada y hay varias ubicaciones creadas en el almacén podrá cambiar la frecuencia del conteo de inventario en ubicaciones específicas.

Para ver y editar ubicaciones, vaya a la aplicación Inventario ‣ Configuración ‣ ubicaciones. Esto le mostrará la página de Ubicaciones donde están todas las ubicaciones que se crearon y se enlistaron dentro del almacén.

Haga clic en una de las ubicaciones en esta página para abrir los ajustes y la configuración de esa ubicación.

Busque el campo Frecuencia de inventario (días) en la sección Conteo cíclico, este debería estar configurado en `0` de forma predeterminada (si la ubicación no ha sido editada con anterioridad). Cambie el valor a cualquier número de días deseado.

![Ajuste de frecuencia en la ubicación.](https://www.odoo.com/documentation/17.0/es/_images/cycle-counts-frequency-value.png)

 Example

Una ubicación que necesita un recuento de inventario cada 30 días debe tener el valor de Frecuencia de inventario (días) en 30.

Al aplicar un ajuste de inventario en esta ubicación, la siguiente fecha de conteo programada se configurará en automático con el valor que proporcionó en el campo Frecuencia de inventario (días).

## Recuento de inventario por ubicación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/cycle_counts.html#count-inventory-by-location "Enlazar permanentemente con este título")

Para realizar un conteo cíclico en una ubicación específica del almacén, vaya a Inventario ‣ Operaciones ‣ Inventario físico. Se le redirigirá a la página de ajustes de inventario con todos los productos en existencia. Cada producto aparece en una línea.

Desde esta página, las opciones Filtros y Agrupar por (a las que puede acceder si hace clic en el icono ⬇️ (flecha hacia abajo) ubicado del lado derecho de la barra de búsqueda) se pueden utilizar para seleccionar ubicaciones específicas y realizar conteos de inventario.

Para seleccionar una ubicación específica y ver todos los productos en ella, haga clic en el icono ⬇️ (flecha hacia abajo) ubicado a la derecha de la barra de búsqueda. Después, en la columna Agrupar por, haga clic en Agregar grupo personalizado para abrir un nuevo menú desplegable.

![El menú de filtros y la opción agrupar por en la página de ajustes de inventario.](https://www.odoo.com/documentation/17.0/es/_images/cycle-counts-filter-menu.png)

Haga clic en Ubicación en el menú desplegable. Esta acción ordenará los productos por ubicación de almacenamiento en la página Ajustes de inventario y podrá realizar un conteo de ciclos para todos los productos en esa ubicación.

 Truco

En el caso de almacenes grandes con varias ubicaciones y muchos productos, es probable que sea más fácil buscar una ubicación en específico. En la página Ajustes de inventario haga clic en el icono ⬇️ (flecha hacia abajo) ubicado a la derecha de la barra de búsqueda.

Después, en la columna Filtros, haga clic en Agregar filtro personalizado para abrir la ventana emergente correspondiente.

En el primer campo, haga clic en el valor y seleccione Ubicación de la lista de opciones, en el segundo campo seleccione contiene y en el tercer campo escriba el nombre de la ubicación que está buscando.

Haga clic en Agregar para que la ubicación aparezca en la página.

![La ventana emergente Agregar filtro personalizado con los valores de ubicación correspondientes.](https://www.odoo.com/documentation/17.0/es/_images/cycle-counts-add-custom-filter.png)

## Cambiar la frecuencia de los recuentos de todo el inventario[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/cycle_counts.html#change-full-inventory-count-frequency "Enlazar permanentemente con este título")

Por lo general los conteos cíclicos se realizan por ubicación, pero la fecha programada para contabilizar todo el inventario disponible del almacén también se puede cambiar de manera manual para realizarlo antes de la fecha estipulada.

Para modificar la fecha planeada predeterminada vaya a Inventario ‣ Configuración ‣ Ajustes. Diríjase a la sección Operaciones y busque el campo Día y mes del inventario anual, este incluye un campo desplegable que de forma predeterminada está configurado con el `31` de diciembre.

![Imagen que muestra el campo frecuencia en los ajustes de la aplicación Inventario.](https://www.odoo.com/documentation/17.0/es/_images/cycle-counts-frequency-calendar.png)

Para cambiar el día, haga clic en el `31` y cámbielo a un día que entre en el rango `1-31`, según el mes del año que desea.

Para cambiar el mes haga clic en December y podrá ver el menú desplegable con los meses.

Haga clic en Guardar después de realizar todos los cambios necesarios.

 Ver también

- [Ajustes de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/count_products.html)
    
- [Ubicaciones](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html)