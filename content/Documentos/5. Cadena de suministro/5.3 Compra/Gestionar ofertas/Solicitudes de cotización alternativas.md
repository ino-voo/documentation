A veces las empresas desean solicitar ofertas de distintos proveedores al mismo tiempo y les invitan a que se las envíen de manera simultánea para productos y servicios similares. Esto ayuda a que las empresas seleccionen a los proveedores que tengan mejores precios y sean más rápidos según las necesidades que tengan.

En Odoo, esto es posible si crea solicitudes de cotización alternas para diferentes proveedores. Una vez que haya recibido una respuesta de cada proveedor, podrá comparar las líneas de producto de cada solicitud de cotización y decidir qué productos comprar de qué proveedores.

 Nota

A este proceso a veces se le llama _licitación_ y las organizaciones del sector público que están obligadas de forma legal a utilizarlo cuando realizan una compra. Sin embargo, las empresas privadas también pueden usar solicitudes de cotización alternativas para darle mayor valor a su dinero.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/calls_for_tenders.html#configuration "Enlazar permanentemente con este título")

Para crear solicitudes de cotización alternativas **debe** habilitar la función **Contratos de compra** en los ajustes de la aplicación _Compra_. Vaya a Compra ‣ Configuración ‣ Ajustes y, en la sección Órdenes, haga clic en la casilla Contratos de compra.

Haga clic en Guardar para aplicar los cambios.

Esta acción le permitirá crear solicitudes de cotización alternativas y también _órdenes abiertas_.

![Contrato de compra activados en los ajustes de la aplicación Compras.](https://www.odoo.com/documentation/17.0/es/_images/calls-for-tenders-enabled-setting.png)

 Truco

Para crear solicitudes de cotización alternativas con mayor rapidez puede establecer proveedores personalizados, precios y plazos de entrega en la pestaña Compra de los formularios de producto.

Para ello, vaya a Compra ‣ Productos ‣ Productos y seleccione el producto a editar. En su respectivo formulario, haga clic en la pestaña Compra y luego en Agregar una línea.

Elija al proveedor correspondiente con el menú desplegable de la columna Proveedor y en caso de que sea necesario establezca un Precio y Plazo de entrega. Al hacer clic en el icono (menú para mostrar u ocultar columnas opcionales) ubicado en la parte superior derecha de la fila de encabezados aparecerán las opciones adicionales para columnas que puede agregar a los elementos de la línea.

## Crear una solicitud de cotización[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/calls_for_tenders.html#create-an-rfq "Enlazar permanentemente con este título")

Para crear una nueva solicitud de cotización, vaya a Compra y haga clic en Nuevo.

En el formulario vacío para la solicitud de cotización, agregue un proveedor con el menú desplegable junto al campo Proveedor. En la pestaña Productos, haga clic en Agregar un producto para seleccionar uno del menú desplegable en la columna Producto.

Después, establezca la cantidad que desea comprar en la columna Cantidad y modifique el precio de compra en la columna Precio unitario, si es necesario.

Al hacer clic en el icono (menú para mostrar u ocultar columnas opcionales) ubicado en la parte superior derecha de la fila del encabezado, aparecen otras columnas que puede agregar a los elementos de la línea.

Repita estos pasos para agregar tantas columnas como desee a la pestaña Productos, incluyendo la UdM (unidad de medida) para comprar los productos y la fecha de entrega esperada.

Una vez que haya terminado, haga clic en Enviar por correo electrónico.

Esta acción abre la ventana emergente Redactar correo electrónico en la que podrá personalizar el mensaje para el proveedor y agregar archivos adjuntos en caso de que sea necesario. Una vez que haya terminado, haga clic en Enviar.

Esto envía un correo electrónico al proveedor que aparece en el formulario de la solicitud de cotización.

![Ventana emergente para escribir y enviar un correo con una cotización.](https://www.odoo.com/documentation/17.0/es/_images/calls-for-tenders-compose-email.png)

 Nota

Enviar correos a todos los proveedores puede ser útil al crear solicitudes de cotización alternativas. Los proveedores pueden confirmar si sus precios anteriores siguen vigentes en ese momento, lo que ayuda a que las empresas elijan las mejores ofertas.

## Crear una solicitud de cotización alternativa[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/calls_for_tenders.html#create-alternative-rfqs "Enlazar permanentemente con este título")

Luego de crear y enviar una orden de compra al proveedor, podrá crear solicitudes de cotización alternativas para otros proveedores con el fin de comparar precios, tiempos de entrega y otros factores que le ayudarán a tomar desiciones sobre sus órdenes.

Para crear solicitudes de cotización alternativas con la solicitud original, haga clic en la pestaña Alternativas, después haga clic en Crear alternativa y aparecerá una ventana emergente.

![Ventana emergente de una licitación para crear una cotización alterna.](https://www.odoo.com/documentation/17.0/es/_images/calls-for-tenders-create-alternative.png)

En esta ventana seleccione al proveedor alterno al que le asignará esta cotización con el menú desplegable que está junto al campo Proveedor.

A un lado encontrará la casilla Copiar productos que está seleccionada de manera predeterminada. Cuando está activa, las cantidades del producto de la solicitud de cotización original se copian a la alterna. Deje seleccionada la casilla para esta primera cotización alternativa. Una vez que haya terminado, haga clic en Crear alternativa, esto abrirá un nuevo formulario de solicitud de cotización.

Como la casilla Crear alternativa estaba seleccionada, el nuevo formulario ya está completo con los mismos productos, cantidades y otros detalles de la solicitud de cotización original anterior.

 Nota

**No** es necesario que agregue productos adicionales cuando la casilla Copiar productos está seleccionada al crear una cotización alternativa, a menos que así lo desee.

Sin embargo, si uno de los proveedores elegidos aparece en la columna Proveedor en un formulario específico de algún producto incluido en la orden, los valores establecidos en el formulario de producto se transfieren a la solicitud de cotización y **debe** cambiarlos de forma manual en caso de que sea necesario.

Después cree una segunda cotización alternativa. Haga clic en la pestaña Alternativas y después en Crear alternativa.

 Nota

También aparece la opción para comparar líneas de productos. Al hacer clic en este enlace accederá a la página Comparar líneas de orden, ahí podrá comparar solicitudes de cotización alternativas. Consulte la sección [Comparar líneas de productos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/calls_for_tenders.html#purchase-manage-deals-compare-product-lines) para obtener más información.

Esto abre la ventana emergente Crear alternativa. Vuelva a elegir un proveedor diferente del menú desplegable ubicado junto a Proveedor. Para esta solicitud de cotización _desmarque_ la casilla Copiar productos, esto eliminará todos los productos en la nueva solicitud de cotización alternativa, dejándola vacía. Puede agregar los productos específicos que debe ordenar de este proveedor según sea necesario.

Una vez que haya terminado, haga clic en Crear alternativa.

 Truco

Si necesita eliminar una cotización alternativa de la pestaña Alternativas, puede hacerlo al hacer clic en el icono Eliminar (X) ubicado al final de la fila correspondiente.

Esto crea una tercera y nueva solicitud de cotización. Sin embargo, como las cantidades de los productos de la solicitud original **no** se copiaron, las líneas de productos están vacías y debe agregar nuevos productos según sea necesario. Para ello, haga clic en Agregar un producto y seleccione los productos deseados del menú desplegable.

Haga clic en Enviar por correo electrónico después de que haya agregado el número deseado de productos.

![Cotización alterna en blanco con alternativas en las migajas de pan.](https://www.odoo.com/documentation/17.0/es/_images/calls-for-tenders-blank-quotation.png)

Esta acción abre la ventana emergente Redactar correo electrónico en la que podrá personalizar el mensaje para el proveedor y agregar archivos adjuntos en caso de que sea necesario. Una vez que haya terminado, haga clic en Enviar.

Haga clic en la pestaña Alternativas del formulario, ahí podrá ver las tres solicitudes de cotización en la columna Referencia. Además, los proveedores aparecen en la columna Proveedor y el total (y el estado) de las órdenes está disponible en las filas.

La fecha en la columna Entrega esperada se calcula para cada proveedor con los plazos de entrega preconfigurados en los formularios del proveedor y del producto.

## Vincular una nueva solicitud de cotización a las cotizaciones existentes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/calls_for_tenders.html#link-new-rfq-to-existing-quotations "Enlazar permanentemente con este título")

Es posible vincular las solicitudes de cotización existentes incluso si una cotización no se crea desde la pestaña Alternativas de otra solicitud.

Para ello, cree una nueva solicitud de cotización. Vaya a Compra ‣ Nuevo. Complete la solicitud de cotización de acuerdo con las [instrucciones anteriores](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/calls_for_tenders.html#purchase-manage-deals-create-rfq).

Después haga clic en la pestaña Alternativas. Como esta nueva solicitud de cotización se creó por separado, aún no hay otras órdenes vinculadas.

Para vincular esta solicitud de cotización a las alternativas existentes haga clic en Vincular a solicitud de cotización existente en la primera línea de la columna Proveedor.

![Una ventana emergente para vincular una nueva cotización a las solicitudes de cotización existentes.](https://www.odoo.com/documentation/17.0/es/_images/calls-for-tenders-link-rfq-popup.png)

Esta acción abre la ventana emergente Agregar: Órdenes de compra alternativas. Seleccione las solicitud de cotización deseadas que creó con anterioridad y haga clic en Seleccionar. Todas estas órdenes ahora están copiadas en esta solicitud de cotización y están disponibles en la pestaña Alternativas.

 Truco

Si está procesando varias órdenes de compra y no puede ubicar las órdenes anteriores, haga clic en el icono ⬇️ (flecha hacia abajo) ubicado a la derecha de la barra de búsqueda en la parte superior de la ventana emergente.

Después, haga clic en Proveedor en la sección Agrupar por. Los proveedores aparecen en sus propias listas desplegables anidadas y puede abrir la lista de cada proveedor para ver sus órdenes de compra abiertas relacionadas.

## Comparar líneas de producto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/calls_for_tenders.html#compare-product-lines "Enlazar permanentemente con este título")

Es posible comparar las solicitudes de cotización alternativas junto a otras para determinar qué proveedores ofrecen las mejores ofertas en los productos incluidos en las órdenes.

Para comparar las solicitudes de cotización alternativas, vaya a Compra y seleccione alguna de las creadas con anterioridad.

Haga clic en la pestaña Alternativas para ver todas las solicitudes de cotización vinculadas. Después, en la pestaña Crear alternativa, haga clic en Comparar líneas de producto que le redirigirá a la página Comparar líneas de orden.

![La página "Comparar líneas de producto" para una solicitud de cotización alternativa.](https://www.odoo.com/documentation/17.0/es/_images/calls-for-tenders-compare-products.png)

De manera predeterminada, la página Comparar Líneas de orden agrupa por productos. Cada producto incluido en cualquiera de las solicitudes de cotización aparecerá en su propia lista desplegable junto con todos los números de la orden de compra en la columna Referencia.

Las columnas adicionales en esta página incluyen el proveedor del que se ordenaron los productos, entregas cumplidas a tiempo, el número de referencia, el estado de la cotización (por ejemplo, solicitud de cotización, solicitud de cotización enviada…), la descripción del producto, la fecha de entrega esperada, la cantidad de productos ordenados a cada proveedor, la unidad de medida utilizada para cada producto (si corresponde), el precio unitario por producto, el precio total de la orden y la divisa aplicada.

 Nota

Para eliminar líneas de productos de la página Comparar líneas de orden, haga clic en Limpiar. Esta opción se encuentra en el extremo derecho de la fila de esa línea de producto.

Esta acción elimina este producto específico de las opciones a seleccionar en la página y cambia el precio total de ese producto en la página a `0`.

Además, en el formulario de la solicitud de cotización que incluye ese producto, la cantidad ordenada también cambia a `0`.

Una vez que hayan identificado las mejores ofertas, pueden seleccionar productos de forma individual al hacer clic en el botón Elegir ubicado al final de cada fila.

Después de que haya elegido todos los productos deseados, haga clic en Solicitudes de cotización (en las migas de pan ubicadas en la parte superior de la página) para regresar a la vista general de todas las solicitudes de cotización.

## Cancelar (o almacenar) alternativas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/calls_for_tenders.html#cancel-or-keep-alternatives "Enlazar permanentemente con este título")

Después de que haya elegido los productos deseados en la página Comparar líneas de orden podrá cancelar las solicitudes de cotización restantes de las que no seleccionó productos.

El costo en la columna Total para los productos que no eligió se establece en automático como `0` y aparece en el extremo derecho de cada fila correspondiente.

Aunque todavía no están cancelados, esto indica que es posible cancelar cada una de esas órdenes sin afectar a las otras órdenes activas una vez que están confirmadas.

![Cotizaciones canceladas en el resumen de la aplicación Ventas.](https://www.odoo.com/documentation/17.0/es/_images/calls-for-tenders-zero-total.png)

Para confirmar una solicitud de cotización para la cual se seleccionaron productos, haga clic en una y luego haga clic en Confirmar orden.

Esto hace que aparezca una ventana emergente con el mensaje ¿Qué pasa con las solicitudes de cotización alternativas? con dos opciones: Cancelar alternativas y Mantener las alternativas.

Haga clic en Descartar si **no** es necesario confirmar esta orden de compra.

Seleccionar Cancelar alternativas cancela estas solicitudes de cotización de forma automática. Seleccionar Mantener las alternativas mantiene abiertas las solicitudes para que pueda acceder a ellas si necesita ordenar una cantidad mayor de productos más adelante.

Una vez que haya ordenado todos los productos puede seleccionar Cancelar alternativas desde cualquier orden de compra que esté abierta en ese momento.

![Ventana emergente para guardar o cancelar solicitudes de cotización alternativas.](https://www.odoo.com/documentation/17.0/es/_images/calls-for-tenders-keep-or-cancel.png)

Para ver el formulario detallado de una de las solicitudes de cotización, haga clic en la línea correspondiente a esa cotización. Esto abrirá la ventana emergente Abrir: Órdenes de compra alternativas en la que podrá ver todos los detalles de esa solicitud en particular.

Al terminar, haga clic en Cerrar para cerrar la ventana emergente.

En la ventana emergente ¿Qué pasa con las solicitudes de cotización alternativas? haga clic en Mantener las alternativas en caso de que todas estas solicitudes deban permanecer abiertas.

Luego, haga clic en Solicitudes de cotización (en las migas de pan ubicadas en la parte superior de la página) para regresar a la vista general de todas las solicitudes de cotización.

Haga clic en las solicitudes de cotización restantes que incluyan productos por ordenar y haga clic en Confirmar orden.

Esta acción abre la ventana emergente ¿Qué pasa con las solicitudes de cotización alternativas?. Si lo desea, y ya no necesita las solicitudes de cotización alternativas restantes, haga clic en Cancelar alternativas para cancelar las otras que estén vinculadas con esta orden.

Por último, haga clic en Solicitudes de cotización (en las migas de pan ubicadas en la parte superior de la página) para regresar a la vista general de todas las solicitudes de cotización.

Las órdenes canceladas aparecen en color gris y con el estado Cancelado en la columna Estado que se encuentra en el extremo derecho de sus respectivas filas.

Ahora que ordenó todas las cantidades de producto puede completar el proceso de compra y recibir los productos en el almacén.

 Ver también

[Órdenes abiertas](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/blanket_orders.html)