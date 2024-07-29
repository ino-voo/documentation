Defina _tipos de productos_ en Odoo para monitorear productos a detalle.

Calcifique los productos como _almacenables_ para monitorear los conteos de inventario, lo que permitirá que los usuarios puedan activar las [reglas de reabastecimiento](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_replenishment/reordering_rules.html) para generar órdenes de compra. Se asume que los productos _Consumibles_ siempre están en existencias y que los productos de _servicio_ los realiza la empresa.

 Ver también

[Tutoriales de Odoo: tipos de producto](https://www.youtube.com/watch?v=l6j0ZkP5mLM)

## Configurar un tipo de producto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#set-product-type "Enlazar permanentemente con este título")

Para configurar un tipo de producto, vaya a la aplicación Inventario ‣ Productos ‣ Productos y seleccione un producto de la lista.

En el formulario de producto, en el campo Tipo de producto seleccione:

- Producto almacenable para productos para los que mantiene un conteo de inventario. Solo los productos almacenables pueden activar reglas de reabastecimiento para generar órdenes de compra;
    
    >  Truco
    > 
    > Seleccione Producto almacenable si es necesario rastrear las existencias de un producto en diferentes ubicaciones, valoraciones de inventarios o si el producto tiene lotes o números de serie.
    
- Consumible para productos de los que se supone que siempre hay existencias, cuyas cantidades no es necesario seguir ni prever (por ejemplo, clavos, papel higiénico, café, etc.). Los consumibles son sustituibles y esenciales, pero no es necesario hacer recuentos exactos.
    
- Servicio para productos de servicio que vende para que se hagan y no se rastrean con conteos de inventario (es decir, mantenimiento, instalación o servicios de reparación).
    
    ![Configure un tipo de producto en el formulario de producto](https://www.odoo.com/documentation/17.0/es/_images/product-form.png)
    

 Nota

Los tipos de producto enlistados arriba están en la aplicación _Inventario_. Para acceder a los campos de abajo, [instale](https://www.odoo.com/documentation/17.0/es/applications/general/apps_modules.html#general-install) las aplicaciones correspondientes **además** de instalar **Inventario**.

- Cuotas de reservación: cobre una cuota por reservar citas con la aplicación _Citas_. Requiere la instalación de la aplicación _Calendario_ y el módulo _Pagar para reservar_ (`appointment_account_payment`)
    
- Combo: cree productos con descuentos que se venden en conjunto. Requiere la instalación de la aplicación _Punto de venta_.
    
- Boletos del evento: que se venden a asistentes que van a un evento. Requiere la instalación de la aplicación _Eventos_.
    
- Estands del evento: que se venden a partners o patrocinadores para que pongan su estand en el evento. Requiere la instalación de la aplicación _Eventos_.
    
- Curso: vende acceso a un curso educativo. Requiere la instalación de la aplicación _eLearning_.
    

## Comparar tipos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#compare-types "Enlazar permanentemente con este título")

A continuación le presentamos un resumen de cada tipo de producto que afecta las operaciones de _Inventario_, como transferencias, órdenes de reabastecimiento y el reporte de pronóstico. Haga clic en la opción de la tabla con un asterisco (*) para ir a las secciones donde se da información detallada.

|Tipo de producto|Almacenable|Consumible|Servicio|
|---|---|---|---|
|Producto físico|Sí|Sí|No|
|Cantidad disponible|[Sí*](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#inventory-product-management-on-hand-store)|[Sí*](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#inventory-product-management-on-hand-con)|No|
|[Valuación de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/using_inventory_valuation.html)|Sí|No|No|
|Crear transferencia|[Sí*](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#inventory-product-management-transfer-store)|[Sí*](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#inventory-product-management-transfer-con)|[No*](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#inventory-product-management-transfer-serv)|
|[Monitoreo de lotes o números de serie](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/differences.html)|Sí|No|No|
|Crear una orden de compra|Sí|[Sí*](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#inventory-product-management-po)|No|
|Se puede fabricar o subcontratar|[Sí*](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#inventory-product-management-manufacture)|[Sí*](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#inventory-product-management-manufacture)|No|
|Puede ser un kit|Sí|Sí|No|
|Puesto en un paquete|Sí|[Sí*](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#inventory-product-management-package)|No|
|Aparece en el reporte de inventario|[Sí](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#inventory-product-management-report)|No|No|

### Cantidad disponible[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#on-hand-quantity "Enlazar permanentemente con este título")

Las cantidades disponibles y previstas de un producto almacenable, basadas en los pedidos entrantes y salientes, se reflejan en el formulario de producto, el cual puede ver en la aplicación Inventario ‣ Productos ‣ Productos, seleccione el producto deseado.

![Mostrar los botones inteligentes "a la mano" y "pronosticados".](https://www.odoo.com/documentation/17.0/es/_images/on-hand.png)

Las cantidades actuales y pronosticadas se muestran en los botones inteligentes **a la mano** y **pronosticados** en el formulario del producto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#id1 "Enlace permanente a esta imagen")

Por otra parte, siempre se trata a los productos consumibles como que siempre están disponibles y **no** se pueden gestionar con reglas de reabastecimiento o números de lote o serie.

### Crear transferencia[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#create-transfer "Enlazar permanentemente con este título")

Las _transferencias_ son cualquier operación dentro de un almacén, como recibos, transferencias internas o por lote o envíos.

Al crear una transferencia para productos almacenables en la aplicación _Inventario_ se modificará la cantidad disponible en cada ubicación.

Por ejemplo, transferir cinco unidades de la ubicación interna `WH/Inventario` a `WH/Zona de embalaje` disminuye la cantidad registrada en `WH/Inventario` y la aumenta en `WH/Zona de embalaje`.

Para productos consumibles, puede crear transferencias, pero las cantidades exactas en cada ubicación de inventario no se monitorean.

Los productos de servicio no se pueden incluir en las transferencias, pero estos productos se pueden [vincular a proyectos y tareas para monitorear las fechas límite](https://www.youtube.com/watch?v=fix2LGkv13c).

### Crear una orden de compra[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#create-purchase-order "Enlazar permanentemente con este título")

Tanto los productos almacenables como consumibles se pueden incluir en una solicitud de cotización en la aplicación _Compra_.

Sin embargo, al recibir productos consumibles, la cantidad a la mano no cambia al validar el recibo (por ejemplo, `WH/IN`).

### Fabricar o subcontratar[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#manufacture-or-subcontract "Enlazar permanentemente con este título")

Los productos almacenables y consumibles se pueden fabricar, subcontratar o incluir en una lista de materiales.

![Imagen que muestra los botones inteligentes "lista de materiales" y "se utiliza en".](https://www.odoo.com/documentation/17.0/es/_images/manufacture.png)

Cuando los botones inteligentes **lista de materiales** y **se usa en** están visibles en el formulario del producto, esto indica que el producto puede ser fabricado o utilizado como componente de una [|lista de materiales|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#id4).[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#id2 "Enlace permanente a esta imagen")

### Paquetes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#packages "Enlazar permanentemente con este título")

Tanto los productos almacenables como consumibles pueden ponerse en [paquetes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/package.html).

Sin embargo, en el caso de los productos consumibles, no se realiza un seguimiento de la cantidad, y el producto no aparece en la Contenidos del paquete, a la que se accede yendo a la aplicación Inventario ‣ Productos ‣ Paquetes, y seleccionando el paquete deseado.

![Mostrar la página Paquetes, que contiene la lista de contenidos de los paquetes.](https://www.odoo.com/documentation/17.0/es/_images/package-content.png)

Se ha introducido un producto consumible en el envase, pero la sección **Contenido** no lo indica.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#id3 "Enlace permanente a esta imagen")

Si la función _Mover paquetes completos_ está activada, al mover un paquete se actualiza la ubicación de los productos almacenables que contiene. Sin embargo, no se actualiza la ubicación de los productos consumibles.

### Reporte de inventario[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/type.html#inventory-report "Enlazar permanentemente con este título")

**Solo** los productos almacenables aparecen en los siguientes reportes.

El _reporte de existencias_ es una lista completa de todos los productos almacenables disponibles, sin reservar, entrantes y salientes. El reporte solo está disponible para los usuarios con [acceso de administrador](https://www.odoo.com/documentation/17.0/es/applications/general/users/access_rights.html) y está en Inventario ‣ Reportes ‣ Existencias.

![Imagen de la lista de reporte de inventario que se encuentra en Inventario > Reportes > Existencias.](https://www.odoo.com/documentation/17.0/es/_images/stock-report.png)

El _reporte de ubicación_ es un desglose de cada ubicación (interna, externa o virtual) y de la cantidad disponible y reservada de cada producto almacenable. Este reporte solo está disponible si la función _Ubicación de almacenamiento_ está activada (Inventario ‣ Configuración ‣ Ajustes) y si los usuarios tienen [acceso de administrador](https://www.odoo.com/documentation/17.0/es/applications/general/users/access_rights.html).

Para ver el reporte de ubicación vaya a Inventario ‣ Reportes ‣ Ubicaciones.

![Imagen de la lista de reporte de ubicación que se encuentra en Inventario > Reportes > Ubicaciones.](https://www.odoo.com/documentation/17.0/es/_images/location-report.png)