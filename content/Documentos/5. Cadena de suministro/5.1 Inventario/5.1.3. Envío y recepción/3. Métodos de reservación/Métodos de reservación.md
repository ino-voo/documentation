Las empresas que venden y entregan mercancías a los clientes necesitan asegurarse de que siempre tienen existencias disponibles, para que cuando se confirmen nuevos pedidos de venta puedan entregar los productos a tiempo.

En Odoo, esto puede ser manejado usando _métodos de reserva_. Los métodos de reserva controlan cómo los productos incluidos en una orden de entrega deben ser reservados para la entrega, asegurando que están reservados en los momentos correctos, para los pedidos correctos.

Hay tres tipos de métodos de reservación en Odoo: _al confirmar_, _manual_ y _antes de la fecha programada_

At ConfirmationManuallyBefore scheduled date

Los productos se reservan **solo** cuando se confirma una orden de venta **y** solo si hay existencias disponibles.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods.html#configuration "Enlazar permanentemente con este título")

Los métodos de reserva no se configuran en tipos de operaciones individuales. Para configurar los métodos de reserva, vaya a la aplicación Inventario ‣ Configuración ‣ Tipos de operaciones.

En la pestaña General del formulario de tipo de operación, localice la opción Método de Reserva, y elija qué método debe utilizarse para este tipo de operación.

![El campo de método de reserva en el formulario de tipo de operación orden de envío.](https://www.odoo.com/documentation/17.0/es/_images/reservation-methods-operations-type-field.png)

 Truco

Si se selecciona el método de reservación Antes de la fecha programada, aparecerá un nuevo campo abajo, Reservar antes de la fecha programada. En este campo puede cambiar el número de días antes y días antes de que se destacó de el número predeterminado, `0`, al que usted prefiera.

Si cambia el valor días antes también cambiará el número máximo de días antes de la fecha programada en los que se debe reservar productos.

Cambiar el valor de días antes de que se destacó también cambia el número máximo de días antes para que los productos de un evento programado que se destacó (se puso como favorito) se deben reservar.

![Campos de reservar antes de la fecha programada con el método antes de la fecha programada seleccionado.](https://www.odoo.com/documentation/17.0/es/_images/reservation-methods-before-scheduled-date.png)

## Aplicaciones requeridas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods.html#required-applications "Enlazar permanentemente con este título")

Las dos aplicaciones requeridas que se **deben** [instalar](https://www.odoo.com/documentation/17.0/es/applications/general/apps_modules.html#general-install) para usar métodos de reserva son las aplicaciones **Ventas** e **Inventario**.

 Nota

Además de las órdenes de entrega, los métodos de reservación también se pueden usar para _órdenes de fabricación_, órdenes _de subcontratación de reabastecimiento_. órdenes para _reparaciones_ y _transferencias internas_, si así se desea. Para activar esto, configure los ajustes adicionales:

- **Para órdenes de fabricación:** instale la aplicación _Fabricación_ desde la aplicación Aplicaciones, donde tiene que encontrar la aplicación _Fabricación_ y hacer clic en Instalar.
    
- **Para subcontratación para reabastecimiento:** vaya a la aplicación de Fabricación ‣ Configuración ‣ Ajustes y en la sección Operaciones active Subcontratación y después haga clic en Guardar.
    
- **Para órdenes de fabricación:** instale la aplicación _Reparaciones_ desde la aplicación Aplicaciones, donde tiene que encontrar la aplicación _Reparaciones_ y hacer clic en Instalar.
    
- **Para transferencias internas:** vaya a la aplicación de Invantario ‣ Configuración ‣ Ajustes y en la sección Almacén active Ubicaciones de almacenamiento y después haga clic en Guardar.
    

Ya que haya instalado estas aplicaciones no es necesario activar funciones adicionales desde los ajustes para que funcionen los métodos de reservación. Estos estarán disponibles en automático en algunos tipos de operación y los puede ver y cambiar en la aplicación Inventario ‣ Configuración ‣ Tipos de operaciones y después haga clic en un tipo de operación específico.

 Nota

Cuando el Tipo de operación se cambia a Recepción en un formulario de Tipos de operación, los métodos de reservación **no** están disponibles.

![Los tipos de operación están remarcados en el submenú de Configuración en la aplicación Inventario.](https://www.odoo.com/documentation/17.0/es/_images/reservation-methods-operations-type-menu.png)

 Ver también

- [Al confirmar la reservación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/at_confirmation.html)
    
- [Reserva manual](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/manually.html)
    
- [Antes de la fecha programada](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/reservation_methods/before_scheduled_date.html)