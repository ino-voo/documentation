En Odoo hay muchas formas distintas de procesar la recepción y entrega de productos que entran y salen de un almacén.

El método preferido de una empresa para recibir o enviar productos depende de varios factores, como el tipo de productos almacenados y vendidos, el tamaño del almacén, la cantidad de recepciones y órdenes de entrega procesadas a diario, entre otras cosas.

Habilitar la función _Rutas multietapa_ en los ajustes de la aplicación _Inventario_ de Odoo permite que los usuarios modifiquen la forma en que procesan recepciones y envíos en la base de datos.

 Ver también

- [Uso de rutas (tutorial en eLearning)](https://www.odoo.com/slides/slide/using-routes-1018)
    
- [Reglas push y pull (tutorial en eLearning)](https://www.odoo.com/slides/slide/push-pull-rules-5789)
    

Las rutas de entrada y salida predeterminadas en Odoo están configuradas para recibir y entregar bienes en un solo paso. Sin embargo, después de habilitar la función _Rutas multietapa_ puede cambiarlas a dos o tres pasos.

 Nota

Vaya a Inventario ‣ Configuración ‣ Ajustes para activar la función _Rutas multietapa_. Diríjase a la sección Almacén, seleccione la casilla junto a Rutas multietapa y haga clic en Guardar.

Esta acción _también_ activa la función Ubicaciones de almacenamiento en caso de que no lo esté.

Agregar pasos adicionales a las recepciones y envíos que entran y salen del almacén añade otras operaciones que deben completarse antes de recibir o entregar un producto.

Estas configuraciones varían según las necesidades del negocio. También dependen de los requisitos que tengan los productos almacenados, por ejemplo, realizar controles de calidad al recibir productos o usar algún embalaje especial al enviar productos.

## Flujo de un paso[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/shipments_deliveries.html#one-step-flow "Enlazar permanentemente con este título")

Las reglas de recepción y envío para una configuración de un solo paso son las siguientes:

- **Recepción**: reciba productos de los vendedores directo en sus existencias. _No_ hay pasos intermedios entre la recepción y la entrada de existencias.
    
- **Envío**: envíe productos directo del almacén a su cliente. _No_ hay pasos intermedios antes del envío.
    
- _Solo_ se puede usar si **no** se usan las estrategias de remoción primeras entradas, primeras salidas (PEPS), últimas entradas, primeras salidas (UEPS) o primero en expirar, primero en salir (FEFO).
    
- Los artículos se reciben desde o se envían directamente a las existencias.
    
- Es óptimo para los almacenes que necesitan procesar recepciones y envíos con rapidez.
    
- Se recomienda para almacenes pequeños con bajos niveles de existencias y para artículos no perecederos.
    

 Ver también

[Procesar recepciones y entregas en un paso](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html)

## Flujo de dos pasos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/shipments_deliveries.html#two-step-flow "Enlazar permanentemente con este título")

Las reglas de recepción y envío para una configuración de dos pasos son las siguientes:

- **Entrada + existencias**: lleve los productos a una ubicación de entrada _antes_ de que entren a las existencias. Puede organizar los productos por distintas ubicaciones de almacenamiento interno (como varios estantes, congeladores y áreas cerradas) antes de guardarlos en el almacén.
    
- **Recolectar + enviar**: lleve los productos a una ubicación de salida antes de enviarlos. Puede organizar los productos por diferentes transportistas o muelles de envío antes de enviarlos.
    
- Como requisito mínimo debe utilizar números de lote o serie para rastrear productos con estrategias de remoción PEPS, UEPS o FEFO.
    
- Los productos recibidos no estarán disponibles para fabricar, enviar, etc., hasta que se transfieran a las existencias del almacén.
    
- Se recomienda para almacenes más grandes con altos niveles de existencias o al almacenar artículos grandes (como colchones, muebles grandes, maquinaria pesada, entre otros artículos).
    

 Ver también

[Procesar recepciones y entregas en dos pasos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html)

## Flujo de tres pasos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/shipments_deliveries.html#three-step-flow "Enlazar permanentemente con este título")

Las reglas de recepción y envío para una configuración de tres pasos son las siguientes:

- **Entrada + calidad + existencias**: reciba productos en la ubicación de entrada, transfiéralos a un área de control de calidad y mueva los que pasan la inspección a sus existencias.
    
- **Recolectar + empaquetar + enviar**: recolecte productos de acuerdo con su estrategia de remoción, empaquételos en un área destinada y llévelos a una ubicación de salida para enviarlos.
    
- Se puede usar para rastrear productos por números de lote o serie cuando utiliza una estrategia de eliminación PEPS, UEPS o FEFO.
    
- Los productos recibidos no estarán disponibles para fabricar, enviar, etc., hasta que se transfieran a las existencias.
    
- Es necesario para cualquier almacén que necesite realizar controles de calidad antes de recibir artículos en sus existencias.
    
- Se recomienda para almacenes muy grandes con niveles muy altos de existencias.
    

 Ver también

- [Procesar recepciones en tres pasos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_three_steps.html)
    
- [Procesar entregas en tres pasos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/delivery_three_steps.html)