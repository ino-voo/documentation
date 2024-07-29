Las existencias a la mano de una empresa contribuyen a la valoración de su inventario. Ese valor debe figurar en los registros contables de la empresa para mostrar de forma precisa el valor de la empresa y de todos sus activos.

Odoo utiliza una valoración periódica de inventario (también conocida como valoración manual) de forma predeterminada. Este método implica que el equipo de contabilidad registre los asientos contables según el inventario físico de la empresa y que los empleados del almacén se encarguen de contar las existencias. En Odoo, las categorías de producto reflejan esto con el método de costeo establecido en precio estándar y la valoración de inventario (que no es visible de forma predeterminada) configurada como manual.

![El campo de método de costeo se ubica en el formulario de categorías de producto.](https://www.odoo.com/documentation/17.0/es/_images/inventory-valuation-fields.png)

La valoración de inventario perpetua (automática) también crea _asientos de diario_ en tiempo real en la aplicación _Contabilidad_ siempre que haya existencias que entren o salgan del almacén de la empresa.

Esta documentación se enfoca en la configuración adecuada para una valoración de inventario automática, que es un método de valoración que asegura que los asientos de diario en le aplicación _Contabilidad_ coincidan con las actualizaciones en la aplicación _Inventario_. Para ver una introducción a la valoración de inventario en Odoo, vaya a la documentación [Usar la valoración de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/using_inventory_valuation.html).

 Advertencia

Switching from manual to automatic inventory valuation may cause discrepancies between stock valuation and accounting journals.

One [successful strategy](https://www.odoo.com/r/Kvfg) for switching to automated valuation:

1. Clear existing stock (possibly with an [inventory adjustment](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/count_products.html))
    
2. Change the inventory valuation method to _Automatic_
    
3. Return the existing stock, with the original monetary value (using an inventory adjustment)
    

Once the existing stock is recovered, the Odoo _Accounting_ app automatically generates the journal entries to corresponding stock valuation records.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#configuration "Enlazar permanentemente con este título")

Para configurar correctamente una valoración de inventario automático, siga los siguientes pasos en Odoo:

1. [Instale la aplicación Contabilidad y active ajustes específicos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#inventory-warehouses-storage-accounting-setup)
    
2. [Configure valoración de inventario automática en las categorías de producto](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#inventory-warehouses-storage-valuation-on-product-category)
    
3. [Configure el método de costo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#inventory-warehouses-storage-costing-methods)
    

### Configuración de contabilidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#accounting-setup "Enlazar permanentemente con este título")

Para usar la valoración de inventario automática, primero instale la aplicación _Contabilidad_. Después, vaya a la aplicación Contabilidad ‣ Configuración ‣ Ajustes y en la sección Valoración de inventario marque la casilla Contabilidad automática y después, haga clic en Guardar.

 Nota

Si se activa Contabilidad automática se mostrará el campo _Valoración de inventario_, que antes era invisible, en la categoría del producto.

![Función Contabilidad automática en la sección Valoración de inventario de la página de Ajustes](https://www.odoo.com/documentation/17.0/es/_images/auto-accounting.png)

Vea las secciones [Gasto](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#inventory-warehouses-storage-expense-account) y [Entrada y salida de existencias](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#inventory-warehouses-storage-stock-account) de la documentación para detalles sobre la configuración de los diarios contables.

### Configuración de la categoría del producto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#product-category-setup "Enlazar permanentemente con este título")

Después de [activar la valoración de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#inventory-warehouses-storage-accounting-setup) el siguiente paso es configurar la categoría del producto con la que se usará la valoración de inventario.

Vaya la aplicación Inventario ‣ Configuración ‣ Categorías de producto y seleccione la categoría de producto que desee. En la sección Valoración de inventario configure el campo Valoración de inventario como Automatizado. Repita este paso por cada categoría de producto con la que quiera usar la valoración de inventario automática.

 Nota

Después de activar la contabilidad automática, cada nueva capa de valoración de existencias, que se crea durante las actualizaciones de valoración de inventario, genera un asiento de diario.

![Campo de valoración de inventario en la categoría del producto, con varias cuentas de inventario.](https://www.odoo.com/documentation/17.0/es/_images/automated-inventory-valuation.png)

## Metodo de costo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#costing-method "Enlazar permanentemente con este título")

Después de [activar la valoración de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#inventory-warehouses-storage-accounting-setup), el _método de costo_ que se usará para calcular y registrar los costos de inventario se definirá en la categoría de producto en Odoo.

Vaya la aplicación Inventario ‣ Configuración ‣ Categorías de producto y seleccione la categoría de producto que desee. En la sección Valoración de inventario seleccione el Método de costo adecuado:

- Precio estándar: es el método de costo predeterminado en Odoo. El costo del producto se define de forma manual en el formulario del producto y se utiliza para calcular la valoración. Incluso si el precio en una orden de compra es distinto, la valoración utilizará el costo que se definió en el formulario del producto.
    
- Costo promedio: calcula la valoración de un producto según su costo promedio, dividido entre el número total de existencias a la mano disponibles. Al utilizar este método de costo, la valoración de inventario es _dinámica_ y se ajusta constantemente según el precio de compra de los productos.
    
     Nota
    
    Al elegir costo promedio (AVCO) como el método de costo, si cambia el valor numérico en el campo costo para los productos de la categoría de producto respectiva creará un nuevo registro en el reporte de _Valoración de inventario_ para ajustar el valor del producto. El importe del costo se actualizará de forma automática según el precio promedio de compra, tanto del inventario disponible como de los costos acumulados de las órdenes de compra validadas.
    
- Primeras entradas, primeras salidas (FIFO): rastrea el costo de los artículos entrantes y salientes en tiempo real y usa el precio real de los productos para cambiar la valoración. El precio de compra más antiguo se utiliza como el costo del siguiente bien vendido hasta que venda todo el lote de ese producto. Cuando el siguiente lote de inventario avanza en la cola, se utiliza un costo de producto actualizado basado en la valoración de ese lote en específico. Podría decirse que este método de valoración de inventario es el más preciso por varios motivos, pero es muy delicado con los datos introducidos y a cometer errores humanos.
    

 Advertencia

Cambiar el método de costo impacta mucho la valoración de inventario. Recomendamos consultar a un contador antes de hacer cualquier ajuste.

 Ver también

[Usar la valoración de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/using_inventory_valuation.html)

Cuando cambia el método de costo, los productos que ya estaban en existencias que usaban el método de costo estándar **no** cambian su valor. Las unidades existentes mantienen su valor y cualquier movimiento del producto a partir de entonces afecta el costo promedio, es decir, el costo del producto cambiará. Si el valor en el campo costo en un formulario de producto se cambia de forma manual, Odoo generará un registro correspondiente en el reporte de _Valoración de Inventario_.

 Nota

Es posible utilizar distintos ajustes de valoración para categorías de producto distintas.

## Tipos de contabilidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#types-of-accounting "Enlazar permanentemente con este título")

Con la valoración de inventario configurada, los asientos de diario generados dependen del modo de contabilidad seleccionado: _continental_ o _anglosajona_.

 Truco

Para comprobar el modo de contabilidad, active el [Modo de desarrollador (modo de depuración)](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode) y vaya a Contabilidad ‣ Configuración ‣ Ajustes.

Después, en la barra de búsqueda escriba Contabilidad anglosajona para ver si la función está activa. Si **no** lo está, entonces está usando el modo de _Contabilidad_ continental.

![Imagen del modo de contabilidad anglosajona activado.](https://www.odoo.com/documentation/17.0/es/_images/anglo-saxon.png)

En la contabilidad _anglosajona_, el costo de los bienes vendidos se reporta cuando se venden o entregan productos. Esto significa que el costo de un bien solo se registra como un gasto cuando se factura un producto a un cliente.

Para un método de valoración **manual**, configure la _Cuenta de gastos_ a _Valoración de existencias_ para el tipo de activo actual; para el método **automático** configure la _Cuenta de gastos_ a tipo de costo de _Gastos_ o _Ingreso_ (por ejemplo, _Costo de producción_ o _Costo de bienes vendidos_, entre otros).

En la contabilidad _Continental_ el costo de un bien se reporta tan pronto como este producto entra a existencias. Por eso, la _Cuenta de gastos_ puede ser **ya sea** de tipo _Gastos_ o _Costo de ingresos_, sin embargo, es más común que se configure como una cuenta de _Gastos_.

Vea las secciones Gasto y Entrada y salida de existencias para detalles sobre la configuración de cada tipo de cuenta.

### Cuenta de gastos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#expense-account "Enlazar permanentemente con este título")

Para configurar la _cuenta de gastos_, que se usa tanto en la valoración de inventario manual como en la automática, vaya a la sección Propiedades de la cuenta de la categoría de producto que quiera (Inventario ‣ Configuración ‣ Categorías de producto). Después, seleccione una cuenta existente desde el menú desplegable Cuenta de gastos.

Para asegurar que la cuenta seleccionada es del tipo correcto, haga clic en el icono de flecha apuntando hacia la derecha ubicado a la derecha de la cuenta. Después, configure el tipo de cuenta según la información de abajo.

Anglo-SaxonContinental

AutomatedManual

En la contabilidad anglosajona para la valoración automatizada de inventario, configure la cuenta de gastos para `gastos`. Después haga clic en el icono de flecha apuntando hacia la derecha para ir a la cuenta correcta.

En la ventana emergente seleccione Gastos o Costo de ingreso desde el menú desplegable Tipo.

![Imagen del campo **cuenta de gastos** y el icono del enlace externo.](https://www.odoo.com/documentation/17.0/es/_images/external-link.png)

#### Entrada y salida de existencias (solo automatizadas)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#stock-input-output-automated-only "Enlazar permanentemente con este título")

Para configurar la Cuenta de entrada de existencias y la Cuenta de salida de existencias vaya a Inventario ‣ Configuración ‣ Categorías de productos y seleccione la categoría de producto deseada.

En el campo Valoración del inventario seleccione Automatizado para que aparezca la sección Propiedades de cuenta de existencias. Estas cuentas se definen como:

- Cuenta de valoración de existencias: cuando se habilita la valoración automatizada de inventario en un producto, esta cuenta contendrá el valor actual de los productos.
    
- Diario de existencias: diario contable en el que los asientos se publican de forma automática cuando la valoración de inventario de un producto cambia.
    
- Cuenta de entrada de existencias: los apuntes del diario de contrapartida para todos los movimientos de entrada de existencias se registrarán en esta cuenta, a menos que se establezca una cuenta de valoración específica en la ubicación de origen. Este es el valor predeterminado para todos los productos en una categoría específica, y también se puede establecer directamente en cada producto.
    
- Cuenta de salida de existencias: los apuntes del diario de contrapartida para todos los movimientos de salida de existencias se registrarán en esta cuenta, a menos que se establezca una cuenta de valoración específica en la ubicación destino. Este es el valor predeterminado para todos los productos en una categoría específica, y también se puede establecer directamente en cada producto.
    

Anglo-SaxonContinental

En la contabilidad Anglosajona las cuentas entrada de existencias y salida de existencias se configuran con _diferentes_ cuentas de Activos circulantes. De esta forma, entregar los productos y facturar el cliente saldan la cuenta _Salida de inventario_, mientras que recibir los productos y facturar a los proveedores saldan la cuenta _Salida de inventario_.

Para modificar el tipo de cuenta, haga clic en el icono de flecha que apunta hacia la derecha ubicado del lado derecho de la cuenta de entrada o salida de inventario. En la ventana emergente seleccione el formulario Activos circulantes con el menú desplegable de Tipo.

![Imagen de la página de configuración de la cuenta con el campo **Tipo** resaltado.](https://www.odoo.com/documentation/17.0/es/_images/account-type.png)

La cuenta _Entrada de inventario_ está configurada a `Existencias provisionales (recibidas)`, un tipo de cuenta de _activos circulantes_.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#id1 "Enlace permanente a esta imagen")

## Reporte de la valoración del inventario[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#inventory-valuation-reporting "Enlazar permanentemente con este título")

Primero, vaya a Contabilidad ‣ Reportes ‣ Balance general. Haga clic en Activos circulantes para mostrar un menú desplegable donde tendrá que buscar las líneas Valoración de inventario, Existencias provisionales (recibidas) y Existencias provisionales (entregadas).

 Truco

En la parte superior del tablero, haga clic en el botón a partir de [date] para mostrar los registros contables a partir de una fecha específica.

 Ver también

- [Las cuentas de existencias y qué hacen](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/inventory_valuation_config.html#inventory-warehouses-storage-stock-account)
    
- [Hoja de referencia de Contabilidad](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/cheat_sheet.html)
    

![Puede ver el desglose completo de la valoración de inventario en la aplicación Contabilidad de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/stock-balance-sheet.png)

Al hacer clic en el icono  (puntos suspensivos) a la derecha del diario deseado podrá ver información más específica. Seleccione Libro mayor para ver una lista de todos los asientos de diario, donde podrá hacer clic en el icono  (puntos suspensivos) de cada línea de artículo para mostrar la opción Ver asiento contable y abrir un asiento contable individual.

Además, puede agregar anotaciones en el Balance General si hace clic en Anotar, llena el cuadro de texto y hace clic en Guardar.

![Mostrar los diarios de valoración de inventario en una lista.](https://www.odoo.com/documentation/17.0/es/_images/journals.png)