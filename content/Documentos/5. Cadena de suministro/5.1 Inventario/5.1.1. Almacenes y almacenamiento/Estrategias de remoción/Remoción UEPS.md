La estrategia de remoción _Últimas entradas, primeras salidas_ (UEPS) selecciona los productos **más recientes** disponibles según la fecha en que ingresaron a las existencias de un almacén.

Cada que se realiza una orden de productos con la estrategia UEPS, se crea un traslado para el número de lote o serie que entró más recientemente a las existencias (el **último** número de lote o serie que ingresó al inventario del almacén).

 Ver también

[Sobre las estrategias de remoción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html)

 Advertencia

La estrategia de remoción UEPS está prohibida en muchos países, ya que podría causar que los clientes reciban productos antiguos, caducados u obsoletos.

El siguiente ejemplo hace uso del producto `Ladrillo de cemento` y se rastrea por lotes en la pestaña Inventario del formulario del producto. La estrategia de remoción forzada para esta categoría de productos está configurada como Últimas entradas, primeras salidas (UEPS).

 Ver también

- [Configurar una estrategia de remoción forzada](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#inventory-warehouses-storage-removal-config)
    
- [Habilitar seguimiento por lotes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#inventory-warehouses-storage-lots-setup)
    
- [Verificar las fechas de llegada](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fifo.html#inventory-warehouses-storage-arrival-date)
    

La siguiente tabla representa los ladrillos de cemento en existencia y los detalles sobre los distintos números de lote.

||LOTE1|LOTE2|LOTE3|
|---|---|---|---|
|Existencias disponibles|10|10|10|
|[Creado el](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fifo.html#inventory-warehouses-storage-arrival-date)|1 de junio|3 de junio|6 de junio|

Para observar la estrategia de remoción en funcionamiento cree una [orden de entrega](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#inventory-delivery-one-step) para siete ladrillos de cemento. Vaya a la aplicación Ventas y cree una nueva cotización.

Haga clic en Confirmar en la orden de venta para crear una orden de entrega. Esta acción reserva los números de lote más recientes con la estrategia de remoción UEPS.

Para visualizar las recolecciones de forma detallada, haga clic en el icono ⦙≣ (lista con viñetas) ubicado en el extremo derecho de la línea del producto `Ladrillo de cemento` en la pestaña Operaciones de la orden de entrega. Al hacerlo, abrirá la ventana emergente Abrir: movimiento de existencias.

En la ventana emergente Abrir: movimiento de existencias, el campo Recolectar de muestra desde dónde se toma la cantidad necesaria para cumplir con la demanda. La orden necesita siete ladrillos de cemento, así que se toman los ladrillos más recientes del `LOTE3` con la estrategia de remoción UEPS.

![Las operaciones detalladas muestran qué lotes se están seleccionando para la recolección.](https://www.odoo.com/documentation/17.0/es/_images/cinder-block-picking.png)

 [Edit on GitHub](https://github.com/odoo/documentation/edit/17.0/content/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/lifo.rst)