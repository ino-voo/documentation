Odoo permite buscar, filtrar y agrupar registros en una vista para mostrar solo los registros más relevantes. La barra de búsqueda se encuentra en la parte superior de la vista, comience a escribir en ella para [buscar valores](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-values) o haga clic en el icono 🔽 (flecha hacia abajo) para acceder a los menús desplegables de [Filtrar](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-filters), [Agrupar por](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-group) y [Favoritos](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-favorites).

## Buscar valores[](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-for-values "Enlazar permanentemente con este título")

Use el filtro de búsqueda para buscar valores específicos y agregarlos como filtros. Escriba el valor que debe buscar y seleccione la opción que quiere aplicar al filtro de búsqueda en el menú desplegable.

 Example

En lugar de agregar un [filtro personalizado](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-custom-filters) para seleccionar los registros donde _Mitchell Admin_ es el vendedor en el reporte de _análisis de ventas_ (Ventas ‣ Reportes ‣ Ventas) puede buscar `Mitch`, hacer clic en el botón ⏵ (fecha derecha) junto a Buscar vendedor: Mitch, y seleccionar Mitchell Admin.

![Búsqueda de un valor específico en el reporte de análisis de ventas](https://www.odoo.com/documentation/17.0/es/_images/search-values.png)

 Nota

Usar el campo de búsqueda es equivalente a usar el operador _contiene_ al agregar un [filtro personalizado](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-custom-filters). Si introduce un valor parcial y selecciona el campo deseado directamente (sin seleccionar la ⏵ (flecha derecha)) entonces se incluirán _todos_ los registros que contengan los caracteres que escribió para el campo seleccionado.

## Filtros[](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#filters "Enlazar permanentemente con este título")

Los filtros se usa para seleccionar registros que cumplen con ciertos criterios. La selección predeterminada de registros es específica para cada vista, pero se puede modificar seleccionando uno (o varios) de los [filtros preconfigurados](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-preconfigured-filters), o agregando un [filtro personalizado](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-custom-filters).

### Filtros preconfigurados[](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#preconfigured-filters "Enlazar permanentemente con este título")

Para modificar la selección predeterminada de registros haga clic en el icono 🔽 (flecha hacia abajo) en la barra de búsqueda y seleccione uno (o varios) de los _filtros preconfigurados_ desde el menú desplegable Filtros.

 Example

En el reporte _análisis de ventas_ (aplicación Ventas ‣ Reportes ‣ Ventas), solo se seleccionan en automático los registros que estén en la etapa _orden de ventas_ y cuya _fecha de orden_ sea dentro de los últimos 365 días.

Para también incluir los registros en etapa de _cotización_, seleccione Cotizaciones en los filtros.

Además, para _solo_ incluir los registros de órdenes de venta o cotizaciones se un año en específico, como 2024, primero haga clic en el icono ❌ (quitar) para eliminar el filtro `Fecha de la orden: últimos 365 días` y después seleccione Fecha de la orden ‣ 2024.

![Uso de filtros preconfigurados en el reporte de análisis de ventas](https://www.odoo.com/documentation/17.0/es/_images/preconfigured-filters.png)

 Nota

Los Filtros preconfigurados se agrupan y cada grupo se separa con una línea horizontal. Seleccionar filtros preconfigurados del mismo grupo permite que los registros coincidan con _cualquier_ condición aplicada. Sin embargo, seleccionar los filtros de diferentes grupos requiere que los registros cumplan con _todas_ las condiciones aplicadas.

### Filtros personalizados[](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#custom-filters "Enlazar permanentemente con este título")

Si los [filtros preconfigurados](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#search-preconfigured-filters) no son lo suficientemente específicos, agregue un filtro personalizado. Para hacerlo, haga clic en el icono 🔽 (flecha hacia abajo) en la barra de búsqueda, después seleccione Filtros ‣ Agregar filtro personalizado.

La ventana emergente Agregar filtro personalizado muestra la opción que coincide, la regla de filtro y un activador para Incluir archivados.

![La ventana emergente para agregar un filtro personalizado.](https://www.odoo.com/documentation/17.0/es/_images/custom-filter1.png)

La configuración de coincidencia predeterminada es coincidir con cualquiera de las siguientes reglas:, lo cual indica que cada regla de filtro se aplica de manera independiente. Para cambiar la configuración de coincidencia a coincidir con todas las siguientes reglas: debe agregar al menos dos reglas de filtro al filtro personalizado.

- Coincidir todas 🔽 las siguientes reglas: **todas** las reglas de filtro se deben cumplir. Por lógica, esta es una operación _Y_ (`&`).
    
- Coincidir cualquiera 🔽 de las siguientes reglas: **cualquiera** de las reglas de filtro se deben cumplir. Por lógica, esta es una operación _O_ (`|`).
    

De forma predeterminada, se agrega una sola regla de filtro al filtro personalizado. A continuación describimos la estructura de una regla de filtro:

1. El primer campo en línea es el _nombre del campo_ por el que puede filtrar. Algunos campos tienen parámetros redefinidos que se encuentran alojados en otro campo. Estos campos tienen un icono > (flecha) a un lado, el cual puede seleccionar para mostrar todos los campos alojados.
    
2. El segundo campo en línea es el _operador_ condicional que se usa para comparar el nombre del campo con el valor. Los [operadores condicionales disponibles](https://www.odoo.com/documentation/17.0/es/developer/reference/backend/orm.html#reference-orm-domains) dependen del tipo de información del campo.
    
3. El tercer campo en línea es el _valor_ variable del nombre del campo. El valor ingresado puede aparecer como un menú desplegable, una entrada de texto, una entrada numérica, una entrada de fecha y hora, un selector booleano, o puede estar en blanco, dependiendo del operador que se use y el tipo de información del campo.
    

También están disponibles tres botones en línea a la derecha de los criterios de las reglas del filtro:

1. ➕ (signo de más): agrega una nueva regla debajo de la regla existente.
    
2. (Agregar rama): agrega un nuevo grupo de reglas debajo de la regla existente, con las opciones de coincidencia cualquiera y Todos disponibles para definir como cada regla dentro de esta rama se aplicará al filtro. Si la opción de coincidencia se configura como la misma que el grupo principal, los filtros de mueven para unirse al grupo principal.
    
     Example
    
    Si la opción de coincidencia se configura a Coincidir todas 🔽 las siguientes reglas, se agrega una rama nueva con su opción de coincidencia diferente de cualquiera🔽 de, la rama que acaba de agregar desparece, y las reglas de grupo se mueven al grupo principal.
    
3. 🗑️ (papelera): borra el nodo. Si se borra el nodo de una rama, todos los nodos secundarios a ese nodo también se borran.
    

Si hace clic en el botón Nueva regla, se agregará una nueva regla de filtro al filtro personalizado.

Una vez que definió los criterios del filtro, haga clic en Agregar para agregar el filtro personalizado a la vista.

 Example

Si lo que quiere es buscar entre todos los leads y oportunidades de la aplicación CRM que están en la etapa _Ganado_ y tienen ganancias esperadas de más de $1,000, debe ingresar lo siguiente:

Coincidir todas 🔽 las siguientes reglas

1. Etapa está en Ganado
    
2. Ingreso esperado > `1,000`
    
3. cualquiera 🔽 (flecha hacia abajo) de:
    
    - Tipo = Lead
        
    - Tipo = Oportunidad
        

![Agregar un filtro personalizado para filtrar registros específicos en CRM.](https://www.odoo.com/documentation/17.0/es/_images/custom-filter-example.png)

 Truco

Active el modo de desarrollador para mostrar el nombre técnico de cada campo y el tipo de información, así como el la area de texto # Editor de código debajo de las reglas de filtro para ver y editar el dominio de forma manual.

## Agrupar registros[](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#group-records "Enlazar permanentemente con este título")

La vista de los registros en una pantalla se pueden juntar, según a uno de los _grupos preconfigurados_. Para hacerlo, haga clic en el icono 🔽 (fecha hacia abajo) en la barra de búsqueda, luego seleccione una de las opciones Agrupar por del menú desplegable.

 Example

Para agrupar los registros por vendedor en el reporte de _Análisis de ventas_ (Aplicación de ventas ‣ Reportes ‣ Ventas), haga clic en la opción Vendedor que aparece en el menú desplegable de Agrupar por. La vista cambia a registros agrupados por vendedor, sin filtrar ninguno de los registros.

![Agrupar registros en el reporte de análisis de ventas](https://www.odoo.com/documentation/17.0/es/_images/group.png)

Es posible _personalizar grupos_ con un campo presente en el modelo. Para hacerlo, haga clic en Agregar grupo personalizado y seleccione un campo del menú desplegable.

 Nota

Puede usar varios grupos al mismo tiempo. El primer grupo que se seleccionó es el agrupamiento principal, el siguiente que se agrega divide aún más las categorías principales del grupo y así sucesivamente. Además, los filtros y los grupos se pueden usar juntos para definir la vista todavía más.

## Favoritos[](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html#favorites "Enlazar permanentemente con este título")

Los favoritos son una forma de guardar una búsqueda específica para usarla más tarde, o como un nuevo filtro predeterminado para una vista.

Para guardar la vista actual como favorita haga clic en el icono 🔽 (flecha hacia abajo) en la barra de búsqueda, después seleccione el menú desplegable Guardar búsqueda actual para mostrar las siguientes opciones:

- Nombre del filtro: nombre de la búsqueda en favoritos.
    
- Filtro predeterminado: hará que la búsqueda en favoritos sea el filtro predeterminado para la vista.
    
- Compartido: hace que la búsqueda marcada como favorita esté disponible para todos los usuarios. De forma predeterminada, esta búsqueda solo está disponible para el usuario que la creó.
    

Una vez que las opciones estén configuradas, haga clic en Guardar para guardar la búsqueda en favoritos.

![Guardar una búsqueda en favoritos en el reporte de Análisis de ventas](https://www.odoo.com/documentation/17.0/es/_images/favorites.png)

Para ver las búsquedas favoritas que haya guardado haga clic en el icono 🔽 (flecha hacia abajo) de la barra de búsqueda, después seleccione el filtro guardado en el menú desplegable Favoritos. Para quitar un filtro guardado en favoritos, haga clic en el icono 🗑️ (papelera) a un lado de la búsqueda en favoritos.

 Truco

Para ver _todas_ las búsquedas favoritas, primero active el modo de desarrollador y vaya a Ajustes ‣ Técnico ‣ Interfaz del usuario: Filtros de usuario. Desde aquí, todas las búsquedas en favoritos se pueden ver, editar, archivar o borrar.