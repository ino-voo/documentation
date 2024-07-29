# Remoción PEPS[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fifo.html#fifo-removal "Enlazar permanentemente con este título")

La estrategia de remoción _Primeras entradas, primeras salidas_ (PEPS) selecciona los productos con las primeras fechas de llegada. Este método es útil para empresas que venden productos con ciclos de demanda cortos, por ejemplo, ropa. Al utilizar PEPS, las empresas pueden evitar conservar algún estilo específico durante mucho tiempo.

 Ver también

[Sobre las estrategias de remoción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html)

 Example

El 1 de agosto y el 25 de agosto llegan varias cantidades del producto `Camiseta` y se rastrean por número de lote. La estrategia de remoción PEPS prioriza los lotes que han estado dentro de las existencias durante más tiempo para poder completar un pedido realizado el 1 de septiembre. Por lo tanto, los productos que llegaron el 1 de agosto se seleccionan primero para su recolección.

![Ilustración de PEPS seleccionando los productos más antiguos en existencia.](https://www.odoo.com/documentation/17.0/es/_images/fifo-example.png)

 Ver también

[Detalles de configuración de los números de lote y serie](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#inventory-warehouses-storage-lots-setup)

## Fecha de llegada[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fifo.html#arrival-date "Enlazar permanentemente con este título")

Para ver el número de lote o serie del producto que llegó primero al inventario, vaya a la aplicación Inventario ‣ Productos ‣ Números de lote/Serie.

Después, seleccione el icono ▶️ (flecha hacia la derecha) ubicado a la izquierda de una línea de producto para abrir la lista de los números de serie o lotes del producto con existencias. El campo Creado el muestra la fecha de creación, es decir, representa la fecha de llegada.

 Example

El número de serie `00000000500` del producto `Gabinete con puertas` llegó el 29 de diciembre, según la información que aparece en el campo Creado el.

![Visualización de la fecha de llegada de un lote para un artículo.](https://www.odoo.com/documentation/17.0/es/_images/created-on1.png)

## Flujo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fifo.html#workflow "Enlazar permanentemente con este título")

Para comprender cómo la estrategia PEPS retira los productos, observe el siguiente ejemplo con tres lotes de camisetas blancas.

Las camisetas pertenecen a la categoría _Todo/Ropa_, allí la estrategia de remoción forzada es PEPS.

Las camisetas blancas están rastreadas por lotes en la pestaña Inventario del formulario del producto.

 Ver también

- [Configurar una estrategia de remoción forzada](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#inventory-warehouses-storage-removal-config)
    
- [Habilitar seguimiento por lotes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#inventory-warehouses-storage-lots-setup)
    

La siguiente tabla incluye los detalles de las existencias disponibles y los números de lote de las camisetas blancas.

||LOTE1|LOTE2|LOTE3|
|---|---|---|---|
|Existencias disponibles|5|3|2|
|[Creado el](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/fifo.html#inventory-warehouses-storage-arrival-date)|1 de marzo|1 de abril|1 de mayo|

Para observar la estrategia de remoción en funcionamiento cree una [orden de entrega](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#inventory-delivery-one-step) para seis camisetas blancas. Vaya a la aplicación Ventas y cree una nueva cotización.

Después de hacer clic en Confirmar en la orden de venta, se reserva una orden de entrega con los números de lote más antiguos de las camisetas con la estrategia de remoción PEPS.

Para visualizar las recolecciones de forma detallada, haga clic en el icono ⦙≣ (lista con viñetas) ubicado en el extremo derecho de la línea del producto `Camisetas blancas` en la pestaña Operaciones de la orden de entrega. Al hacerlo, abrirá la ventana emergente Abrir: movimiento de existencias.

En la ventana emergente Abrir: movimiento de existencias, el campo Recolectar de muestra desde dónde se toma la cantidad necesaria para cumplir con la demanda. La orden necesita seis camisetas, así que se toman todas las camisetas del `LOTE1` y la otra del `LOTE2`.

![Dos lotes reservados para una orden de venta con la estrategia PEPS.](https://www.odoo.com/documentation/17.0/es/_images/white-shirt-picking.png)