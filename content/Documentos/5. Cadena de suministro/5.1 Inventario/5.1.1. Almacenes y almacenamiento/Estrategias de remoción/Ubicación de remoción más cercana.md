Para la estrategia de _ubicación de remoción más cercana_, los productos se seleccionan según el orden alfanumérico de los títulos de la ubicación de almacenamiento.

El objetivo de esta estrategia es evitar que el trabajador del almacén tenga que hacer un largo viaje hasta una estantería más lejana cuando el producto también está disponible en un lugar más cercano.

 Ver también

[Sobre las estrategias de remoción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html)

Para entender la _secuencia de ubicación_ con la estrategia de remoción más cercana, considere el siguiente ejemplo:

 Example

A product is stored in the following locations: `Shelf A/Pallet`, `Shelf A/Rack 1`, and `Shelf A/Rack 2`.

![Mostrar un prototipo de una ubicación de almacenamiento real en un almacén.](https://www.odoo.com/documentation/17.0/es/_images/locations3.png)

La sububicación, `Pallet` está a nivel de suelo. Los productos almacenados ahí son más fáciles de conseguir ya que no es necesario contar con un montacargas, como lo es para llegar a la `Estantería 1` y la `Estantería 2`. Las ubicaciones de almacenamiento se nombraron de forma estratégica y en orden alfabético, según qué tan fácil era llegar a ellas.

 Importante

Las funciones Ubicaciones de almacenamiento y Rutas multietapa **deben** estar habilitadas en Inventario ‣ Configuración ‣ Ajustes para poder establecer una estrategia de remoción en una ubicación.

 Ver también

[Configurar estrategia de remoción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#inventory-warehouses-storage-removal-config)

## Nombres de las ubicaciones[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/closest_location.html#location-names "Enlazar permanentemente con este título")

Para configurar nombres de ubicaciones, primero vaya a la aplicación de Inventario ‣ Configuración ‣ Ubicaciones. Después, seleccione una ubicación existente, o haga clic en Nuevo para crear una nueva y después, ingrese el nombre deseado en el campo nombre de la ubicación.

Una vez que nombre las ubicaciones en orden alfabético, según la proximidad a la ubicación de salida o empaquetado, configure la estrategia de remoción en la [ubicación principal](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html#inventory-location-hierarchy).

Para hacerlo, en la lista de Ubicaciones seleccione la ubicación principal de las ubicaciones de almacenamiento que se nombraron en orden alfabético.

Esto hará que se abra un formulario para la ubicación principal en el campo Estrategia de remoción, seleccione Ubicación más cercana.

 Example

En un almacén, el almacén `WH/Stock/Repisa 1` está situado más cerca de la zona de empaquetado, donde los productos extraídos de las estanterías se embalan para su envío. El popular producto «cargador de iPhone» se almacena en tres ubicaciones: «Almacén/Existencias/Repisa 1», «Almacén/Existencias/Repisa 2» y «Almacén/Existencias/Repisa 3».

Para usar la ubicación más cercana, configure la estrategia de remoción en la ubicación principal, “WH/Stock”.

## Flujo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/closest_location.html#workflow "Enlazar permanentemente con este título")

Para ver cómo funciona la estrategia de remoción de ubicación más cercana, considere seguir el siguiente ejemplo, en donde se guarda el producto final `cargador de iPhone` en `WH/Stock/Estantería 1`, `WH/Stock/Estantería 2` y `WH/Stock/Estantería 3`.

En cada ubicación hay quince, cinco y treinta unidades en existencias, respectivamente.

 Truco

Para verificar las existencias disponibles en la ubicación del almacén, vaya al formulario del producto y haga clic en el botón inteligente Disponible.

![Mostrar las existencias en todas las ubicaciones.](https://www.odoo.com/documentation/17.0/es/_images/on-hand-stock.png)

Cree una [orden de entrega](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#inventory-delivery-one-step) de dieciocho unidades del `cargador de iPhone` en la aplicación de ventas.

Después de agregar los productos, haga clic en Confirmar para crear una orden de envío que reserva los artículos almacenados en la ubicación más cercana, según la estrategia de remoción.

Para obtener más detalles sobre _la ubicación_ de donde se tomaron las unidades seleccione el icono ⦙≣ (lista con viñetas) que está ubicado en el extremo derecho. Al realizar esta acción abrirá la ventana emergente Abrir: movimiento de existencias, aquí se muestra cómo se recolectaron los elementos reservados según la estrategia de remoción.

En la ventana emergente Abrir: Movimiento de existencias, el campo Recolectar de muestra dónde se recogen las cantidades para satisfacer la Demanda. Las quince unidades almacenadas en la ubicación más cercana, `WH/Stock/Estantería 1`, se seleccionan en primer lugar. Las tres unidades restantes se seleccionan de la segunda ubicación más cercana, `WH/Stock/Estantería 2`.

![Mostrar las cantidades de *recolectar de* para la orden de cargadores de iPhone.](https://www.odoo.com/documentation/17.0/es/_images/stock-move-window.png)