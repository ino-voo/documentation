La estrategia de remoción _menos paquetes_ ayuda a cumplir con una orden y abre el menor número de paquetes posible, lo cual es ideal para mantener su inventario organizado sin necesidad de abrir varias cajas.

 Ver también

- [Sobre las estrategias de remoción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html)
    
- [Tutoriales de Odoo: menos paquetes](https://www.odoo.com/slides/slide/5477/share)
    

Para comprender cómo funciona esta estrategia de remoción consulte el siguiente ejemplo con almacén que almacena paquetes de harina en paquetes a granel de `100 kg`.

La estrategia de remoción de menos paquetes hace que todo se tome de un solo paquete abierto. Esto es útil para minimizar la humedad y evitar que entren plagas en los paquetes abiertos.

 Example

Un paquete de `100 kg` de harina ahora cuenta con `54 kg` después de cumplir con algunas órdenes. Hay otros paquetes de `100 kg` en existencia.

1. Si se crea una orden por `14 kg` de harina se seleccionará el paquete con `54 kg`.
    
2. Cuando se realiza una orden con _más_ de `54 kg` de harina entonces se utiliza un paquete cerrado de `100 kg` para poder cumplir con lo solicitado. Habrá dos paquetes abiertos en ese momento pero tendrán prioridad en la siguiente recolección.
    

## Flujo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies/least_packages.html#workflow "Enlazar permanentemente con este título")

Con la estrategia de remoción de menos paquetes se utiliza el menor número de paquetes para cumplir con una orden.

 Importante

La [función de paquetes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#inventory-warehouses-storage-pack-setup) **debe** estar habilitada para usar esta estrategia.

El siguiente ejemplo está relacionado con el producto `Harina`. El campo Unidades de medida que se encuentra en el formulario del producto está configurado en `kg`. El producto se almacena en paquetes de `100 kg`, con un paquete restante que contiene `54 kg`. La estrategia de eliminación forzada de la categoría del producto está configurada en Menos paquetes.

 Ver también

- [Configurar una estrategia de remoción en una categoría de producto](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html#inventory-warehouses-storage-removal-config)
    

 Truco

Para verificar las existencias disponibles del producto, vaya a su formulario y haga clic en el botón inteligente Disponible.

![Visualización de las existencias disponibles en cada paquete.](https://www.odoo.com/documentation/17.0/es/_images/on-hand-flour.png)

Cree una [orden de entrega](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html#inventory-delivery-one-step) para ochenta kilogramos de harina. Vaya a la aplicación Ventas, cree una nueva cotización y haga clic en Confirmar.

El campo Cantidad de la orden de entrega muestra de forma automática la cantidad seleccionada según la estrategia de remoción.

Para obtener más detalles sobre _la ubicación_ de donde se tomaron las unidades seleccione el icono ⦙≣ (lista con viñetas) que está ubicado en el extremo derecho. Al realizar esta acción abrirá la ventana emergente Abrir: movimiento de existencias, aquí se muestra cómo se recolectaron los elementos reservados según la estrategia de remoción.

En la ventana emergente Abrir: movimiento de existencias, el campo Recolectar de muestra desde dónde se toma la cantidad necesaria para cumplir con la demanda. La orden necesita ochenta kilogramos, es decir, una cantidad mayor de la que hay en el paquete abierto con `54 kg`, así que se selecciona un paquete cerrado de `100 kg`.

![Visualización del paquete que se seleccionó en el campo *Recolectar de*.](https://www.odoo.com/documentation/17.0/es/_images/least-package.png)