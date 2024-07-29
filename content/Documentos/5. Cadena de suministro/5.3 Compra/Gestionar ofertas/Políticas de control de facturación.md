En la aplicación _Compra_ de Odoo, la política de _control de facturas_ determina las cantidades facturadas por los proveedores en cada orden de compra y puede elegir entre la cantidad ordenada y la cantidad recibida.

La política que haya seleccionado en los ajustes de la aplicación _Compra_ sirve valor predeterminado y se aplica a cualquier producto nuevo que cree.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/control_bills.html#configuration "Enlazar permanentemente con este título")

Para configurar la política de _control de facturas_, vaya a Compra ‣ Configuración ‣ Ajustes y diríjase a la sección Facturación. En Control de facturas deberá seleccionar entre cantidad ordenada y cantidad recibida.

![Política de control de facturas seleccionada en los ajustes de la aplicación Compra.](https://www.odoo.com/documentation/17.0/es/_images/control-bills-selected-policy.png)

- Cantidades ordenadas: crea una factura de proveedor en cuanto se confirma una orden de compra. Los productos y cantidades en la orden de compra se usan para generar un borrador de factura.
    
- Cantidades recibidas: se crea una factura solo _después_ de recibir una parte de la orden. Los productos y cantidades recibidas se usan para generar un borrador de factura. Aparecerá un mensaje de error si intenta crear una factura de proveedor sin haber recibido nada.
    
    ![Mensaje de error en el borrador de factura de la política de control de facturación.](https://www.odoo.com/documentation/17.0/es/_images/control-bills-error-message-popup.png)
    

 Nota

Si algún producto debe usar una política de control distinta a la que seleccionó en los ajustes de la aplicación _Compra_, puede cambiar la política de control de facturas para este desde el formulario correspondiente.

Para ello, vaya a Compra ‣ Productos ‣ Productos y seleccione uno. En su respectivo formulario, haga clic en la pestaña Compra y diríjase a la sección Facturas de proveedores, allí modifique la selección en el campo Política de control.

## Conciliación de tres vías[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/control_bills.html#way-matching "Enlazar permanentemente con este título")

La función de _conciliación de tres vías_ asegura que las facturas solo se paguen una vez que reciba una parte de (o todos) los productos incluidos en la orden de compra.

Para activar esta función, vaya a Compra ‣ Configuración ‣ Ajustes y diríjase a la sección Facturación. Seleccione la casilla ubicada junto a Conciliación de tres vías y haga clic en Guardar.

![La función Conciliación de tres vías habilitada en los ajustes de la aplicación Compra.](https://www.odoo.com/documentation/17.0/es/_images/control-bills-three-way-matching.png)

 Importante

La función de conciliación de tres vías **solo** funciona con la política de control de facturas correspondiente a Cantidades recibidas.

### Pagar las facturas de proveedor con la conciliación de tres vías[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/control_bills.html#pay-vendor-bills-with-3-way-matching "Enlazar permanentemente con este título")

Cuando la _conciliación de tres vías_ está activada, las facturas de proveedor muestran el campo Se debe pagar en la pestaña Otra información. El campo estará configurado como Sí al crear una nueva factura de proveedor, ya que **no** es posible crear una factura hasta que reciba al menos una parte de los productos incluidos en la orden de compra.

Para crear una factura de proveedor a partir de una orden de compra, vaya a Compra ‣ Órdenes ‣ Órdenes de compra. En la página Órdenes de compra, seleccione una de la lista y luego haga clic en Crear factura. Esta acción abre un nuevo formulario de Factura de proveedor en borrador que también se encuentra en la etapa de Borrador. Haga clic en la pestaña Otra información y busque el campo Se debe pagar.

 Importante

La orden de compra seleccionada de la lista **no debe** estar facturada o aparecerá la ventana emergente Operación no válida. Esto ocurre en las órdenes de compra con la política de cantidades recibidas y el estado de facturación totalmente facturado.

![Ventana emergente de operación no válida para una orden de compra facturada.](https://www.odoo.com/documentation/17.0/es/_images/control-bills-invalid-operation.png)

Haga clic en el menú desplegable junto a Se debe pagar para ver las opciones disponibles: Sí, No y Excepción.

![Estado del campo "Se debe pagar" en el borrador de la factura de proveedor.](https://www.odoo.com/documentation/17.0/es/_images/control-bills-should-be-paid.png)

 Nota

Si no ha recibido la cantidad total de productos de una orden de compra, Odoo solo incluirá los productos que _sí_ recibió en el borrador de la factura de proveedor.

Es posible editar las facturas en borrador de los proveedores para incrementar la cantidad facturada, modificar el precio de los productos incluidos en ella y agregar otros productos.

Si cambia la información de la factura en borrador, el estado del campo Se debe pagar estará configurado como Excepción. Esto significa que Odoo nota la discrepancia, pero no bloquea los cambios ni muestra un mensaje de error pues es probable que haya un motivo válido para hacer estos cambios.

Para procesar la factura del proveedor, seleccione una fecha en el campo Fecha de la factura, haga clic en Confirmar y luego en Registrar pago.

Esta acción abre la ventana emergente Registrar pago. En esta ventana la información contable se completa de forma automática según los ajustes contables de la base de datos. Haga clic en Crear pago para procesar la factura del proveedor.

Después de que haya registrado el pago de una factura de proveedor y aparezca el cuadro verde con el mensaje Pagado, el estado del campo Se debe pagar será No.

 Truco

Odoo establece el estado Se debe pagar que aparece en las facturas en automático. Sin embargo, puede cambiarlo de forma manual si hace clic en el menú desplegable del campo dentro de la pestaña Otra información.

## Ver el estado de facturación de una orden[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/control_bills.html#view-a-purchase-order-s-billing-status "Enlazar permanentemente con este título")

Cuando una orden de compra está confirmada, su estado de facturación es visible en la pestaña Otra información del formulario de la orden de compra.

Vaya a Compra ‣ Órdenes ‣ Órdenes de compra y seleccione una orden para ver su estado de facturación.

Haga clic en la pestaña Otra información y busque el campo Estado de facturación.

![Campo de estado de facturación en un formulario de orden de compra.](https://www.odoo.com/documentation/17.0/es/_images/control-bills-billing-status.png)

La siguiente tabla detalla los valores correspondientes al estado de una factura y cuándo son visibles según la _política de factura_ que utilice.

|Estado de facturación|Sobre cantidades recibidas|Sobre cantidades pedidas|
|---|---|---|
|Nada para facturar|Orden de compra confirmada. No ha recibido los productos.|_No aplica_|
|Para facturar|Todos o algunos productos recibidos. Factura sin crear.|Orden de compra confirmada|
|Totalmente facturado|Todos o algunos productos recibidos. El borrador de factura ha sido creado.|Borrador de factura creado|

 Ver también

[Gestionar facturas de proveedor](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/purchase/manage_deals/manage.html)