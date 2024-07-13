## Sincronización de órdenes[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/amazon_connector/manage.html#order-synchronization "Enlazar permanentemente con este título")

Las órdenes se obtienen en automático de Amazon y se sincronizan en Odoo en intervalos regulares.

La sincronización está basada en el estado de Amazon: solo se obtienen las órdenes cuyo estado ha cambiado desde la última sincronización en Amazon. Esto incluye cambios tanto en Amazon como en Odoo.

Para las órdenes _FBA_ (gestionado por Amazon) solo se obtienen aquellas _enviadas_ y _canceladas_.

Para las órdenes _FBM_ (gestionado por el vendedor), se hace lo mismo con las órdenes _no enviadas_ y _canceladas_. Para cada orden sincronizada se crea una orden de venta y un cliente en Odoo (si el cliente aún no está registrado en la base de datos).

 Importante

The stock synchronization does **not** currently support selling the same product as FBM _and_ FBA.

At times, when stock is sent for all products, it triggers a stock problem with Amazon, where Amazon incorrectly thinks the FBM product has some quantity in FBM.

As a result, Amazon then sells it as FBM, instead of taking from their own warehouse. Odoo developers are currently working on resolving this issue to avoid future discrepancies.

 Nota

Cuando se cancela una orden en Amazon y ya se había sincronizado en Odoo, entonces la orden de venta correspondiente se cancela de forma automática.

## Forzar sincronización[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/amazon_connector/manage.html#force-synchronization "Enlazar permanentemente con este título")

Para forzar la sincronización de una orden cuyo estado **no** ha cambiado desde la última sincronización, primero active el [modo de desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode). Esto incluye cambios tanto en Amazon como en Odoo.

Vaya a la cuenta de Amazon en Odoo (aplicación Ventas ‣ Configuración ‣ Ajustes ‣ Conectores ‣ Sincronización con Amazon ‣ Cuentas de Amazon) y modifique la fecha en Seguimiento de órdenes ‣ Última sincronización de órdenes.

Asegúrese de elegir una fecha que ocurra antes del último cambio de estado de la orden correspondiente para sincronizar y guarde, esto hará que la sincronización se realice de forma adecuada.

 Truco

Para sincronizar de inmediato las órdenes de una cuenta de Amazon primero cambie al [modo de desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode), después vaya a la cuenta de Amazon en Odoo y haga clic en Sincronizar órdenes. Puede hacer lo mismo con las recolecciones si hace clic en Sincronizar recolecciones.

## Gestionar entregas en FBM[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/amazon_connector/manage.html#manage-deliveries-in-fbm "Enlazar permanentemente con este título")

Al sincronizar una orden FBM (gestionado por el vendedor) en Odoo se crea una recolección de forma instantánea en la aplicación _Inventario_, además de una orden de venta y un registro de cliente. Luego deberá decidir si enviar todos los productos ordenados al cliente de una vez o enviarlos por partes con órdenes parciales.

Al confirmar una recolección relacionada con la orden se envía una notificación a Amazon, quien a su vez notifica al cliente que la orden (o parte de ella) está en camino.

 Importante

Amazon necesita que los usuarios proporcionen una referencia de seguimiento para cada entrega, esta es necesaria para asignar un transportista.

Si el transportista no proporciona una referencia de seguimiento de forma automática, entonces debe configurarse manualmente. Esta regla se aplica a todos los marketplaces de Amazon.

 Truco

Si el transportista que eligió no es compatible con Odoo puede crear uno con el mismo nombre (por ejemplo, puede crear un transportista llamado `easyship`). Este nombre no distingue entre mayúsculas y minúsculas, pero asegúrese de evitar errores tipográficos ya que en caso de que los haya, Amazon no los reconocerá. A continuación, cree un transportista con el nombre `Autoentrega` para informarle a Amazon que usted se encargará las entregas. Incluso con esta ruta **debe** ingresar una referencia de seguimiento. Recuerde que el cliente recibirá una notificación por correo electrónico sobre la entrega y el transportista junto con la referencia de seguimiento.

 Ver también

[Transportistas externos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html)

### Gestionar los errores al sincronizar las entregas[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/amazon_connector/manage.html#manage-errors-when-synchronizing-deliveries "Enlazar permanentemente con este título")

Algunas veces, Amazon puede no procesar correctamente toda la información enviada por Odoo. En este caso, Odoo envía un correo electrónico con una lista de todos los envíos que fallaron y los errores que Amazon envió. Estos envíos se marcan con una etiqueta que dice: Falló la sincronización con Amazon.

Normalmente se puede corregir el error directamente en el backend de Amazon o en Odoo. Si decide corregir el problema en Odoo, sincronice de nuevo el envío utilizando el botón Volver a intentar la sincronización con Amazon.

 Nota

Puede suceder que Odoo reciba una notificación de Amazon indicando que no se procesó cierta información de entrega, pero sin especificar qué envíos se vieron afectados. En ese caso, se considerará que todos los envíos en estado desconocido no se sincronizaron. Una vez que Odoo reciba una notificación de Amazon que diga que se procesó un envío, su etiqueta cambiará a sincronizado con Amazon. Para acelerar este proceso desde su cuenta de Amazon, haga clic en sincronizar pedidos para sincronizar manualmente estos pedidos, o haga clic en recuperar pedido e introduzca la referencia del pedido de Amazon correspondiente.

## Seguimiento de entregas en FBA[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/amazon_connector/manage.html#follow-deliveries-in-fba "Enlazar permanentemente con este título")

Al sincronizar una orden FBA (gestionado por Amazon) en Odoo se registra un movimiento de existencias en la aplicación _Inventario_ para cada artículo de la orden de venta. De esta manera, queda almacenado en el sistema.

Los gerentes de inventario pueden acceder a estos movimientos desde la aplicación Inventario ‣ Reportes ‣ Historial de movimientos.

Para las órdenes FBA, el movimiento de existencias se crea en Odoo en automático a través del Conector de Amazon, gracias al estado de envío de Amazon. Al enviar nuevos productos a Amazon, el usuario debe crear una recolección (orden de entrega) de forma manual para trasladar estos productos desde su almacén a la ubicación de Amazon.

 Truco

Para llevar seguimiento de las existencias de _Amazon (FBA)_ en Odoo debe realizar un ajuste de inventario después de reabastecerlas. También puede activar un reabastecimiento automático desde las reglas de reordenamiento en la ubicación de Amazon.

Puede configurar la ubicación de Amazon si accede a la cuenta de Amazon gestionada en Odoo. Para acceder a las cuentas de Amazon en Odoo, vaya a la aplicación Ventas ‣ Configuración ‣ Ajustes ‣ Conectores ‣ Sincronización con Amazon ‣ Cuentas de Amazon.

Todas las cuentas de la misma empresa utilizan la misma ubicación de Amazon de forma predeterminada, pero es posible monitorear las existencias filtradas por marketplace.

Para hacerlo, primero deberá eliminar de la lista de marketplaces sincronizados aquel en donde se encuentran las existencias correspondientes para monitorearlas por separado. Puede acceder a esta lista desde la aplicación Ventas ‣ Configuración ‣ Ajustes ‣ Conectores ‣ Sincronización con Amazon ‣ Cuentas de Amazon.

A continuación, cree otro registro para esta cuenta y elimine todos los marketplaces **excepto** el que desea aislar de los demás.

Por último, asigne otra ubicación de existencias al segundo registro de la cuenta.

## Facturar y registrar pagos[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/amazon_connector/manage.html#invoice-and-register-payments "Enlazar permanentemente con este título")

### Emitir facturas[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/amazon_connector/manage.html#issue-invoices "Enlazar permanentemente con este título")

Debido a la política de Amazon de no compartir las direcciones de correo electrónico de los clientes, **no** es posible enviarles las facturas directamente desde Odoo. Sin embargo, **sí** es posible cargar de forma manual las facturas generadas desde Odoo en el backend de Amazon.

Además, para los clientes B2B, por ahora es necesario obtener la identificación fiscal de forma manual desde el backend de Amazon **antes** de crear una factura en Odoo.

 Nota

Para los usuarios de [TaxCloud](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/taxcloud.html): las facturas creadas a partir de órdenes de ventas de Amazon **no** se sincronizan con TaxCloud, Amazon ya las incluye en su propio reporte de impuestos a TaxCloud.

 Advertencia

La integración con TaxCloud será descontinuada en Odoo 17.

### Registrar pagos[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/amazon_connector/manage.html#register-payments "Enlazar permanentemente con este título")

Como los clientes pagan a Amazon como intermediario, es recomendable que cree un diario _bancario_ (con el nombre `Pagos de Amazon`, por ejemplo) con una cuenta intermediaria _bancaria y de efectivo_ específica.

Además Amazon realiza un solo pago mensual, así que es necesario seleccionar todas las facturas vinculadas a un solo pago al registrar los pagos.

Para hacer eso, use el Diario apropiado específico para los pagos de Amazon y seleccione Depósito por lotes como método de pago.

Luego, seleccione todos los pagos generados y haga clic en Acciones ‣ Crear pago por lotes ‣ Validar.

 Truco

Puede realizar esta misma acción con las facturas de proveedores de Amazon destinadas a las comisiones.

Cuando la cuenta bancaria recibe el saldo al final del mes y después de registrar los estados de cuenta bancarios, acredite la cuenta intermediaria de Amazon por el importe recibido.

## Llevar seguimiento de las ventas de Amazon en los reportes de venta[](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/amazon_connector/manage.html#follow-amazon-sales-in-sales-reporting "Enlazar permanentemente con este título")

El perfil de la cuenta de Amazon en Odoo cuenta con un equipo de ventas establecido en la pestaña Seguimiento de pedidos.

Esto le proporciona acceso rápido a métricas importantes relacionadas con los reportes de ventas. De forma predeterminada, el equipo de ventas de la cuenta de Amazon se comparte entre todas las cuentas de la empresa.

Si lo desea, puede cambiar el equipo de ventas de la cuenta por otro para realizar un reporte separado para las ventas de esta cuenta.

 Truco

También es posible realizar reportes para cada marketplace.

Primero debe eliminar el marketplace deseado de la lista de mercados sincronizados.

Para acceder a la lista de maketplaces sincronizados en Odoo vaya a la aplicación Ventas ‣ Configuración ‣ Ajustes ‣ Conectores ‣ Sincronización con Amazon ‣ Cuentas de Amazon.

Luego cree otro registro para esta cuenta y elimine todos los marketplaces **excepto** el que desea aislar.

Por último, asigne otro equipo de ventas a uno de los dos registros de la cuenta.

 Ver también

- [Funciones del Conector de Amazon](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/amazon_connector/features.html)
    
- [Configuración del conector de Amazon](https://www.odoo.com/documentation/17.0/es/applications/sales/sales/amazon_connector/setup.html)