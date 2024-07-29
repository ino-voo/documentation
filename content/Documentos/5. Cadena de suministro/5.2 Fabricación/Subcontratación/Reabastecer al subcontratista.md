En fabricación, la subcontratación es el proceso que una empresa lleva a cabo cuando contrata a un fabricante externo, o subcontratista, para que fabrique los productos que luego venderá la empresa contratante.

En Odoo, la ruta _Reabastecer al subcontratista al ordenar_ se utiliza para entregar los componentes necesarios para un producto subcontratado a un proveedor cuando se confirma una orden de compra con ese producto.

El subcontratista utiliza los componentes para fabricar el producto deseado antes de enviarlo de vuelta a la empresa contratante o de enviarlo al consumidor final.

 Importante

Es necesario comprender las diferencias entre las rutas _Reabastecer al subcontratista al ordenar_ y _Enviar al subcontratista al ordenar_.

Ambas rutas se utilizan para proporcionarle los componentes necesarios para fabricar un producto a un subcontratista, pero la forma en que se obtienen los componentes es distinta.

Con la ruta _Reabastecer al subcontratista al ordenar_, la empresa contratante envía los componentes desde su almacén.

Con la ruta _Enviar al subcontratista al ordenar_, es necesario comprar los componentes a un proveedor y este los enviará directo al subcontratista.

La elección de la ruta a utilizar depende de los requisitos específicos de la empresa subcontratista y de sus subcontratistas.

Consulte la documentación sobre [Enviar al subcontratista](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html) para obtener toda la información relacionada con los _envíos al subcontratista al ordenar_.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#configuration "Enlazar permanentemente con este título")

Para utilizar la ruta _Reabastecer al subcontratista al ordenar_, vaya a Fabricación ‣ Configuración ‣ Ajustes y, en la sección Operaciones, seleccione la casilla ubicada junto a Subcontratación.

Luego de habilitar la función de _subcontratación_ también es necesario configurar de manera adecuada el producto subcontratado, la lista de materiales (LdM) del producto y los componentes que forman parte de ella.

### Configurar productos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#configure-product "Enlazar permanentemente con este título")

Para configurar un producto para la ruta _Reabastecer al subcontratista al ordenar_, vaya a Inventario ‣ Productos ‣ Productos y seleccione uno o créelo con el botón Nuevo.

Seleccione la pestaña Compra y agregue al subcontratista de los productos como proveedor. Haga clic en Agregar una línea, seleccione al subcontratista en el menú desplegable Proveedor y escriba el precio en el campo Precio.

 Nota

El valor escrito en el campo Precio de la pestaña Compra en la página del producto subcontratado es el importe que le paga al subcontratista por la fabricación del producto.

Esto no representa el costo total del producto, que incluye otros elementos como el costo de sus componentes.

Después, haga clic en la pestaña Inventario para configurar la ruta que determine qué ocurrirá con el producto terminado una vez que el subcontratista lo haya fabricado.

Asegúrese de que la ruta Comprar esté seleccionada si el producto terminado se devuelve a la empresa contratista. Además, seleccione la ruta Reabastecer sobre pedido (MTO) para crear una orden de compra en automático para el producto al confirmar una orden de venta, a menos que haya suficientes existencias para cumplir con la orden de compra.

Asegúrese de seleccionar solo la ruta triangulación si el subcontratista envía el producto terminado al cliente.

### Configurar listas de materiales[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#configure-bom "Enlazar permanentemente con este título")

Para configurar una lista de materiales para la ruta _Reabastecer al subcontratista al ordenar_, haga clic en el botón inteligente Lista de Materiales en la página del producto y seleccione la LdM.

Como alternativa, vaya a Fabricación ‣ Productos ‣ Listas de materiales y seleccione la lista de materiales para el producto subcontratado.

 Ver también

Consulte la documentación de [lista de materiales](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html) para obtener información completa sobre su configuración.

En el campo Tipo de LdM seleccione la opción Subcontratación y después agregue uno o más subcontratistas en el campo Subcontratistas que aparece abajo.

![El campo "Tipo de LdM" en una lista de materiales configurada para fabricar el producto mediante subcontratación.](https://www.odoo.com/documentation/17.0/es/_images/bom-type2.png)

Por último, asegúrese de que todos los componentes necesarios están presentes en la pestaña Componentes. Para agregar un nuevo componente, haga clic en Agregar una línea, después, en el menú desplegable Componente seleccione el necesario y especifique la cantidad requerida en el campo correspondiente.

### Configurar componentes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#configure-components "Enlazar permanentemente con este título")

Para configurar los componentes para la ruta _Reabastecer al subcontratista al ordenar_, vaya a cada componente desde la lista de materiales y seleccione el nombre del componente en la pestaña Componentes, haga clic en el botón ➡️ (flecha derecha) que está del lado derecho del nombre.

Como alternativa también puede ir a cada componente desde Inventario ‣ Productos ‣ Productos y elegirlo.

En el formulario de producto del componente, haga clic en la pestaña Inventario y en la sección Rutas seleccione Reabastecer al subcontratista al ordenar.

Repita este proceso en todos los componentes que se deben enviar al subcontratista.

## Flujo de trabajo de la ruta Reabastecer al subcontratista al ordenar[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#resupply-subcontractor-on-order-workflow "Enlazar permanentemente con este título")

El flujo de trabajo de la ruta Reabastecer al subcontratista al ordenar consta de hasta cinco pasos:

1. Crear una orden de venta para el producto subcontratado, esto creará una orden de compra para adquirir el producto del subcontratista.
    
2. Confirmar la orden de compra creada en el paso anterior o crear una nueva. Esto crea una orden para _reabastecer al subcontratista_, así como una orden de recepción o de triangulación.
    
3. Procesar la orden de _reabastecimiento para el subcontratista_ una vez que haya enviado los componentes del producto subcontratado al subcontratista.
    
4. Procesar la recepción después de que el subcontratista haya terminado de fabricar el producto subcontratado y lo envíe de vuelta a la empresa contratante **o** procesar la orden de triangulación para enviar el producto al cliente.
    
5. Si el flujo de trabajo se inició creando una orden de venta y el producto terminado no se envía directo al cliente final, procese la orden de entrega una vez que envíe el producto al cliente.
    

El número específico de pasos depende del motivo por el que le compra el producto subcontratado al subcontratista.

Si el motivo es cumplir con la orden específica del cliente, el proceso comienza con la creación de una orden de venta y termina con la entrega del producto al cliente o con el subcontratista enviándolo de forma directa.

Si el motivo es aumentar la cantidad de existencias disponibles, el proceso comienza con la creación de una orden de compra y termina con la recepción del producto en el inventario.

 Importante

Puede usar la ruta _Reabastecer al subcontratista al ordenar_ para reabastecer en automático a un subcontratista al confirmar una orden de compra, pero también puede crear una orden de reabastecimiento de forma manual. Este flujo de trabajo es útil si necesita reabastecer al subcontratista sin crear una orden de compra.

Para reabastecer a un subcontratista de forma manual, vaya a la aplicación Inventario y haga clic en la tarjeta Reabastecer subcontratista. Haga clic en Nuevo para crear una nueva orden.

En el campo Dirección de entrega seleccione al subcontratista que debe recibir los componentes.

Después agregue los componentes a la pestaña Operaciones. Haga clic en Agregar una línea, seleccione el componente en el campo desplegable Producto y especifique la cantidad en el campo Demanda.

Por último, haga clic en Marcar como por realizar para registrar la orden. Luego de que los componentes hayan sido enviados al subcontratista, haga clic en Validar para confirmar que la orden ya se envió.

### Crear una orden de venta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#create-so "Enlazar permanentemente con este título")

Solo es necesario completar este paso si le compra el producto se compra al subcontratista para cumplir con alguna de las necesidades del cliente. Diríjase al siguiente paso si compra el producto para aumentar la cantidad disponible.

Para crear una nueva orden de venta, vaya a Ventas ‣ Órdenes ‣ Órdenes y haga clic en Nuevo.

Seleccione al cliente en el menú desplegable correspondiente. Después, haga clic en Agregar un producto en la pestaña Líneas de orden, seleccione un producto subcontratado en el menú desplegable Producto y escriba el número adecuado en el campo Cantidad.

Haga clic en el botón correspondiente para confirmar la orden de venta, en ese momento aparecerá el botón inteligente Compra en la parte superior de la página. Este botón abre la orden de compra creada para adquirir el producto subcontratado del subcontratista.

 Nota

Una orden de venta para el producto solo crea una orden de compra si la ruta _Reabastecer bajo pedido (MTO)_ está habilitada en la página del producto **y** el producto no tiene suficientes existencias para cumplir con la orden de venta.

Si hay suficientes existencias disponibles, confirmar una orden de venta para el producto creará una orden de entrega porque Odoo asume que la orden de venta se cumple con las existencias en el almacén.

No ocurre lo mismo con los productos subcontratados que se envían directo al cliente final. En ese caso **siempre** se crea una orden de compra, incluso si hay suficientes existencias.

### Procesar una orden de compra[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#process-po "Enlazar permanentemente con este título")

Si creó una orden de compra en el paso anterior, vaya a Compra –> Órdenes –> Órdenes de compra, selecciónela y luego haga clic en Confirmar orden.

Si no creó una orden de compra en el paso anterior, vaya a Compra ‣ Órdenes ‣ Órdenes de compra y haga clic en Nueva.

Comience a completar la orden de compra y seleccione a un subcontratista con el menú desplegable Proveedor. En la pestaña Productos, haga clic en Agregar un producto para crear una nueva línea de productos. En el campo Producto elija un producto subcontratado e ingrese la cantidad en el campo Cantidad. Por último, haga clic en Confirmar orden para confirmar la orden de compra.

Al confirmar una orden de compra para un producto que necesita que reabastezca de componentes a un subcontratista, entonces se crea una orden de recepción o triangulación de forma automática a la que puede acceder con el botón inteligente Recibo o Triangular que aparece en la parte superior de la orden de compra.

Además, se crea una orden para _reabastecer al subcontratista_ para que reciba los componentes necesarios. También es posible acceder a esta orden desde la orden de compra al hacer clic en el botón inteligente Reabastecer ubicado en la parte superior de la página.

![Una orden de compra para un producto con ruta *Reabastecer al subcontratista al ordenar*, con los botones inteligentes Recepción y Reabastecer en la parte superior de la página.](https://www.odoo.com/documentation/17.0/es/_images/subcontractor-po2.png)

Una orden de compra para un producto con ruta _Reabastecer al subcontratista al ordenar_, con los botones inteligentes Recepción y Reabastecer ubicados en la parte superior de la página.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#id1 "Enlace permanente a esta imagen")

### Procesar la orden para reabastecer al subcontratista[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#process-resupply-subcontractor-order "Enlazar permanentemente con este título")

Una vez que los componentes del producto subcontratado hayan sido enviados al subcontratista, vaya a Compras ‣ Órdenes ‣ Órdenes de compra y seleccione la orden correspondiente.

Haga clic en el botón inteligente Reabastecer ubicado en la parte superior de la página para abrir la orden de _reabastecimiento al subcontratista_ y haga clic en Validar para confirmar el envío de los componentes al subcontratista.

También es posible procesarla a través de la aplicación Inventario. Haga clic en el botón # por procesar de la tarjeta para _reabastecer al subcontratista_ y seleccione la orden correspondiente. Después, haga clic en Validar para confirmar el envío de los componentes al subcontratista.

### Procesar una recepción o una orden de envío directo (triangulación)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#process-receipt-or-dropship-order "Enlazar permanentemente con este título")

Después de que el subcontratista terminó de fabricar el producto deberá enviarlo a la empresa contratante o al consumidor final, esto depende de la [configuración](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#manufacturing-workflows-subcontracting-resupply-product-config) del producto.

#### Procesar una recepción[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#process-receipt "Enlazar permanentemente con este título")

Si el subcontratista envía el producto terminado a la empresa contratante, vaya a Compra ‣ Órdenes ‣ Órdenes de compra después de que se haya recibido y seleccione la orden de compra.

Haga clic en el botón Recibir productos que está ubicado en la parte superior de la orden de compra o en el botón inteligente Recibo que se encuentra en la parte superior de la página para abrir la recepción. Después, haga clic en Validar en la parte superior del recibo para ingresar el producto al inventario.

#### Procesar una orden de envío directo (triangulación)[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#process-dropship-order "Enlazar permanentemente con este título")

Si el subcontratista envía el producto directo al cliente final, vaya a Compra ‣ Órdenes ‣ Órdenes de compra una vez que lo haya enviado y seleccione la orden de compra.

Seleccione el botón inteligente Triangular ubicado en la parte superior de la página para abrir la orden de envío directo y después haga clic en Validar en la parte superior de la orden para confirmar que ya le enviaron el producto al cliente.

### Procesar una orden de entrega[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html#process-delivery-order "Enlazar permanentemente con este título")

Si el flujo de trabajo de subcontratación fue iniciado por una orden de venta del cliente y el producto terminado **NO** fue enviado de forma directa al cliente, sino que lo recibió la empresa contratante, es necesario enviar el producto al cliente y procesar la orden de entrega.

Una vez que haya enviado el producto al cliente, vaya a la aplicación Ventas y seleccione la orden de venta. Presione el botón inteligente Entrega ubicado en la parte superior de la página para abrir la orden de entrega, luego haga clic en Validar en la orden para confirmar que envió el producto al cliente.