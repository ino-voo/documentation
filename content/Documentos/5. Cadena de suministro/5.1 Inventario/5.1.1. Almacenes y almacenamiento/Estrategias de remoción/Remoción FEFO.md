La estrategia de remoción _Primero en expirar, primero en salir_ (FEFO) selecciona productos para su retirada según sus fechas de eliminación asignadas.

 Ver también

[Sobre las estrategias de remoción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html)

## Fecha de remoción[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fefo.html#removal-date "Enlazar permanentemente con este título")

Debe **remover** los productos del inventario antes de la _fecha de remoción_, la cual debe ser unos días antes de la _fecha de caducidad_ del producto.

Para establecer este número de días el usuario debe acceder a la pestaña Inventario del formulario de producto. En la sección Trazabilidad, asegúrese de que el campo Seguimiento está configurado como Por lotes o Por número de serie único.

Después, seleccione la opción Fecha de caducidad para que el campo Fecha de remoción (y otros campos de fecha) aparezcan.

 Importante

Las funciones Lotes y números de serie y Fechas de vencimiento **deben** activarse en la aplicación Inventario ‣ Configuración ‣ Ajustes para dar seguimiento a las fechas de caducidad.

La fecha de caducidad de un producto se determina sumando la fecha de recepción del producto al número de días especificado en el campo Fecha de vencimiento del formulario del producto.

La fecha de eliminación toma esta fecha de caducidad y le resta el número de días especificado en el campo Fecha de remoción del formulario del producto.

 Ver también

[Fechas de caducidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/expiration_dates.html)

 Example

En la pestaña Inventario del producto `huevo`, el usuario configuró las siguientes Fechas:

- Fecha de vencimiento: 30 días después de la recepción
    
- Fecha de remoción: `15` días antes de la fecha de vencimiento
    

![Mostrar fechas de vencimiento y remoción configuradas en el producto.](https://www.odoo.com/documentation/17.0/es/_images/user-set-date.png)

Un envío de huevos llega al almacén el 1 de enero. Por lo tanto, la fecha de caducidad de los huevos es el **31 de enero** (1 de enero + 30). Por extensión, la fecha de remoción es el **16 de enero** (31 de enero - 15).

Para ver las fechas de vencimiento de los artículos en existencias, vaya al formulario del producto y haga clic en el botón inteligente Disponible.

A continuación, haga clic en el icono de opciones adicionales, situado en el extremo derecho, y seleccione las columnas: Fecha de vencimiento y Fecha de remoción.

![Mostrar fechas de caducidad desde el modelo de ajustes de inventario al que se accede desde el botón inteligente *Disponibles* del formulario de producto.](https://www.odoo.com/documentation/17.0/es/_images/removal-date.png)

## Flujo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fefo.html#workflow "Enlazar permanentemente con este título")

La estrategia de remoción FEFO asegura que primero se elijan los productos con la fecha de remoción más cercana.

Para entender cómo funciona esta estrategia de remoción, considere el ejemplo abajo del producto, `Cartón de huevos`, que es una caja que contiene doce huevos.

El producto se rastrea Por lotes y la Estrategia de remoción forzada es Primero en expirar, primero en salir (FEFO).

 Ver también

- [Configurar una estrategia de remoción forzada](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#inventory-warehouses-storage-removal-config)
    
- [Habilitar seguimiento por lotes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#inventory-warehouses-storage-lots-setup)
    
- [Tutoriales de Odoo: productos perecederos](https://www.odoo.com/slides/slide/5324/share)
    

||LOTE1|LOTE2|LOTE3|
|---|---|---|---|
|Existencias disponibles|5|2|1|
|Fecha de vencimiento|4 de abril|10 de abril|15 de abril|
|[Fecha de remoción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fefo.html#inventory-warehouses-storage-exp-date)|26 de febrero|4 de marzo|9 de marzo|

Para observar el funcionamiento de la estrategia de remoción vaya a la aplicación Ventas y cree una nueva cotización.

Al hacer clic en Confirmar creará una una orden de entrega para el día 29 de diciembre y gracias a la estrategia de remoción FEFO se reservarán los números de lote con las fechas de vencimiento más próximas.

Para visualizar las recolecciones de forma detallada, haga clic en el icono ⦙≣ (lista con viñetas) ubicado en el extremo derecho de la línea del producto `Cartón de huevos` en la pestaña Operaciones de la orden de entrega. Al hacerlo, abrirá la ventana emergente Abrir: movimiento de existencias.

En la ventana emergente Abrir: movimiento de existencias, el campo Recolectar de muestra desde dónde se toma la cantidad necesaria para cumplir con la demanda.

La orden necesitaba seis cartones de huevos, así que se seleccionaron los cinco cartones del lote `LOTE1` con fecha del 26 de febrero gracias a la estrategia de remoción FEFO. El cartón restante se tomó del lote `LOTE2` con fecha de vencimiento del 4 de marzo.

![La ventana de movimiento de existencias muestra los lotes que se van a retirar mediante FEFO.](https://www.odoo.com/documentation/17.0/es/_images/eggs-picking.png)