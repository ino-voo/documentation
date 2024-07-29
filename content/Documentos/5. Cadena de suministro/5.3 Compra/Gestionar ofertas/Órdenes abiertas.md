Las órdenes abiertas son contratos de compra a largo plazo entre una empresa y un proveedor en el que acuerdan entregar productos de forma recurrente con un precio predeterminado.

Las órdenes abiertas son muy útiles al comprar ciertos productos a mismo proveedor de forma constante pero en diferentes cantidades y momentos.

Al simplificar los procesos de solicitar órdenes, las órdenes abiertas no solo ahorran tiempo, sino también dinero, ya que pueden ser ventajosas al negociar precios al por mayor con los proveedores.

## Crear una nueva orden abierta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/blanket_orders.html#create-a-new-blanket-order "Enlazar permanentemente con este título")

Habilite la función _Contratos de compra_ en los ajustes de la aplicación _Compra_ para crear órdenes abiertas. Vaya a Compra ‣ Configuración ‣ Ajustes y en la sección Órdenes haga clic en la casilla Contratos de compra. Después, haga clic en Guardar para implementar los cambios.

 Nota

Además de crear órdenes abiertas, la función _Contratos de compra_ también permite que los clientes creen solicitudes de cotización alternativas.

![Contrato de compra activados en los ajustes de la aplicación Compras.](https://www.odoo.com/documentation/17.0/es/_images/blanket-orders-enabled-setting.png)

Vaya a Compra ‣ Órdenes ‣ Órdenes abiertas y haga clic en Nuevo para crear una orden abierta. Esta acción abrirá el formulario correspondiente.

Configure los siguientes campos en un formulario nuevo de orden abiertas para establecer reglas predeterminadas para este contrato recurrente a largo plazo:

- Representante de compras: el usuario asignado a esta orden abierta en específico. De forma predeterminada es el usuario que creó el contrato, pero puede cambiarlo desde el menú desplegable ubicado junto a este campo.
    
- Tipo de contrato: es el tipo de contrato de compra en el que se clasifica esta orden abierta. En Odoo, las órdenes abiertas son los únicos contratos de compra oficiales.
    
- Proveedor: el proveedor con quien se celebra el contrato, ya sea una vez o de manera recurrente. Puede seleccionar el proveedor directamente desde el menú desplegable que está junto a este campo.
    
- Divisa: la divisa acordada que se utilizará para este acuerdo. Si tiene activadas varias divisas en su base de datos, puede cambiarlas desde el menú desplegable que está junto a este campo.
    
- Fecha límite del contrato: la fecha en el que este contrato de compra vence. Deje este campo vacío si esta orden abierta no tiene fecha de vencimiento.
    
- Fecha de la orden: la fecha en la que esta orden abierta debe solicitarse si se creó una nueva cotización directamente desde el formulario de la orden abierta. Si se crea una nueva cotización, este valor aparecerá automáticamente en el campo _Fecha límite de la orden_ en la [|solicitud de cotización|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/blanket_orders.html#id1).
    
- Fecha de entrega: la fecha de entrega esperada de los productos incluidos en una solicitud de cotización creada desde el formulario de la orden abierta. Si crea una nueva cotización, este valor completará el campo _Entrega esperada_ en la solicitud de cotización de forma automática.
    
- Documento de origen: la orden de compra fuente a la que estará vinculada esta orden abierta. Deje este campo vacío si no debe estar vinculada a ninguna orden de compra.
    
- Empresa: la empresa asignada a esta orden abierta en específico. De manera predeterminada, es la empresa a la que pertenece el usuario que creó la orden. Si la base de datos no es del tipo multiempresa, este campo **no** se puede modificar y aparecerá la única empresa registrada en la base de datos.
    

![Un nuevo contrato de compra de orden abierta con productos agregados.](https://www.odoo.com/documentation/17.0/es/_images/blanket-orders-new-agreement.png)

Una vez que todos los campos estén completos, haga clic en Agregar una línea para agregar productos debajo de la columna Producto. Luego, cambie la cantidad de cada producto en la columna de Cantidad y establezca un precio en la columna Precio unitario.

 Importante

Al agregar productos a una nueva orden abierta, los precios que ya existían de los productos no se agregaran en automático a las líneas de producto. **Debe** asignar los precios de forma manual al cambiar el valor en la columna Precio unitario con un precio acordado con el proveedor seleccionado. De lo contrario, el precio se quedara en `0`.

Para ver y cambiar los ajustes predeterminados del contrato de compra para las órdenes abiertas directamente desde el formulario de la orden abierta, haga clic en el icono ➡️ (flecha apuntando a la derecha) que aparece al pasar el cursor sobre el campo Tipo de contrato donde aparece la opción Orden abierta. Esta acción le llevará a los ajustes de la orden correspondiente.

![Flecha de enlace interno junto al campo Tipo de contrato en el formulario de orden abierta.](https://www.odoo.com/documentation/17.0/es/_images/blanket-orders-internal-link-arrow.png)

Desde aquí, puede editar los ajustes de las órdenes abiertas. Debajo de la sección Tipo de contrato, puede cambiar el nombre del Tipo de contrato, y también puede cambiar el Tipo de selección del contrato. Hay dos opciones que puede activar para el tipo de selección:

- Seleccionar solo una solicitud de cotización (exclusivo): cuando se confirma una orden de compra, el resto de las órdenes de compra se cancelan.
    
- Seleccionar varias solicitudes de cotización (no es exclusivo): cuando se confirma una orden de compra, el resto de las órdenes de compra **no** se cancelarán. En lugar de eso, se permitirán varias órdenes de compra.
    

Es posible editar los campos Líneas y Cantidades de la sección Datos para cotizaciones nuevas. Hacerlo mostrará cómo se deben llenar nuevas cotizaciones al usar este contrato de compra.

![Pantalla para editar el tipo de contrato de compra para las órdenes abiertas.](https://www.odoo.com/documentation/17.0/es/_images/blanket-orders-edit-agreement-type.png)

Hay dos opciones que se pueden acitvar para el campo Líneas:

- Usar las líneas del contrato: al crear una nueva cotización, las líneas de producto se completarán previamente con los mismos productos que forman parte de la orden abierta, solo si la selecciona para la nueva cotización.
    
- No crear líneas de solicitud de cotización automáticamente: los ajustes se transferirán a la nueva cotización al crearla **y** seleccionar una orden abierta existente, pero las líneas de producto **no** se completarán.
    

Hay dos opciones que puede activar en el campo Cantidades:

- Usar cantidades del contrato: al momento de crear una nueva cotización, las cantidades del producto que aparecen en la orden abierta completarán las líneas de producto en caso de que seleccione esa orden para la nueva cotización.
    
- Establecer cantidades manualmente: al crear una nueva cotización y seleccionar una orden abierta ya existente, las líneas de producto se pre-completarán, pero las cantidades se quedarán en `0`. El usuario **tendrá** que establecer manualmente las cantidades.
    

Una vez que haga los cambios deseados, haga clic en Nuevo (con las migas de pan ubicadas en la parte superior de la página) para ir al formulario de la orden abierta. Después, haga clic en Confirmar para guardar el nuevo contrato de compra.

Una vez confirmada, la etapa de la orden abierta (que se encuentra en la esquina superior derecha) cambiará de Borrador a En proceso, lo que quiere decir que puede seleccionar este contrato y usarlo al momento de crear una solicitud de cotización.

 Truco

Después de crear y confirmar una orden abierta, los productos, cantidades y precios todavía se pueden editar, agregar o quitar del contrato de compra.

## Crear una nueva solicitud de cotización para una orden abierta[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/blanket_orders.html#create-a-new-rfq-from-the-blanket-order "Enlazar permanentemente con este título")

Es posible crear nuevas cotizaciones desde el formulario de la orden abierta después de confirmarla. Las solicitudes de cotización que usen este formulario se completan de forma automática con la información de las reglas configuradas en el formulario. Además, estas se vinculan al formulario de esta orden abierta a través del botón inteligente Solicitudes de cotización/Órdenes ubicado en la parte superior derecha.

Haga clic en Nueva cotización para crear una nueva cotización desde el formulario de una orden abierta. Esta acción abrirá una nueva solicitud de cotización con la información correcta según los ajustes configurados en el formulario de la orden abierta.

Desde el nuevo formulario de la [|solicitud de cotización|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/blanket_orders.html#id3), haga clic en Enviar por correo electrónico para escribir y enviar un correo al proveedor seleccionado. Haga clic en Imprimir solicitud de cotización para generar un PDF de la cotización para imprimir; o una vez lista, haga clic en Confirmar orden para confirmar la [|orden de compra|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/blanket_orders.html#id5).

![Nueva cotización con productos y reglas copiadas desde una orden abierta.](https://www.odoo.com/documentation/17.0/es/_images/blanket-orders-new-quotation.png)

Una vez que confirmó la orden de compra, regrese al formulario de la orden abierta (con las migas de pan ubicadas en la parte superior de la página). Una vez allí, verá una solicitud de cotización en el botón inteligente Solicitudes de cotización/Órdenes ubicado en esquina superior derecha del formulario. Haga clic en el botón inteligente Solicitudes de cotización/Órdenes para ver la orden de compra que acaba de crear.

![Botón inteligente de Solicitudes de cotización/Órdenes dede el formulario de la orden abierta.](https://www.odoo.com/documentation/17.0/es/_images/blanket-orders-rfq-smart-button.png)

## Reabastecimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/blanket_orders.html#replenishment "Enlazar permanentemente con este título")

Una vez que confirma una orden abierta, se agrega una nueva línea de proveedor a la pestaña Compra de los productos incluidos en esta orden.

Esto hace que las órdenes abiertas funcionen muy bien junto con el [reabastecimiento automático](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/products/reordering.html), porque la infromación del Proveedor, el Precio, y el Contrato están referenciadas en la línea del proveedor. Esta información se utiliza para determinar dónde, cuándo y a qué precio se puede reabastecer este producto.

![Formluario de un producto con un contrato de reabastecimiento vinculado a una orden abierta.](https://www.odoo.com/documentation/17.0/es/_images/blanket-orders-product-form.png)

 Ver también

[Solicitudes de cotización alternativas](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/calls_for_tenders.html)