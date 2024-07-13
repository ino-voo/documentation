Con el **Punto de venta de Odoo** es fácil gestionar tus tiendas y restaurantes. La aplicación funciona en cualquier aplicación que tenga un navegador web, incluso si no está conectado a internet por un momento. Los movimientos de inventario se registran de manera automática en sus existencias, podrá ver estadísticas en tiempo real, y sus datos se consolidan en todas las tiendas.

 Ver también

- [Tutoriales de Odoo: Tutoriales de punto de ventas](https://www.odoo.com/slides/point-of-sale-28)
    
- [Documentación sobre las cajas IoT](https://www.odoo.com/documentation/17.0/es/applications/general/iot.html)
    

## Iniciar una sesión[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#start-a-session "Enlazar permanentemente con este título")

Desde el **tablero de punto de ventas** haga clic en Nueva sesión y en la pantalla Control de efectivo de apertura haga clic en Abrir sesión para iniciar una sesión en el PdV. También puede hacer clic en Continuar venta si la sesión ya está abierta.

 Nota

[Varios usuarios](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/employee_login.html) pueden trabajar en la misma sesión al mismo tiempo, pero solo puede abrir la sesión una vez en el mismo navegador.

## Vender productos[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#sell-products "Enlazar permanentemente con este título")

Haga clic en los productos para agregarlos al carrito. Para cambiar la **cantidad**, haga clic en Cant. e ingrese el número de productos con el teclado. Para agregar un **descuento** o modificar el **precio** del producto, haga clic en % de desc. o en precio para ingresar la cantidad.

Una vez que se complete una orden haga clic en pago para proceder a la página de pago. Seleccione el **método de pago**, ingrese la cantidad recibida y haga clic en Validar. Haga clic en Nueva orden para ir con el siguiente cliente.

![Interfaz de una sesión del punto de venta](https://www.odoo.com/documentation/17.0/es/_images/pos-interface1.png)

 Truco

- Como separador decimal, puede usar tanto `,` como `.`.
    
- La opción **efectivo** se selecciona de manera automática si ingresa una cantidad sin seleccionar un método de pago.
    

 Nota

El sistema solo puede cargar un número limitado de productos para que la aplicación abra sin dificultades. Haga clic en Buscar más si el producto que necesita no aparece de forma automática.

## Configurar clientes[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#set-customers "Enlazar permanentemente con este título")

Es necesario registrar a su clienta para [poder juntar sus puntos de lealtad y otorgarle recompensas](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/loyalty.html), aplicar la [lista de precios correcta](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/pricelists.html) de manera apropiada, o [generar e imprimir una factura](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/receipts_invoices.html#receipts-invoices-invoices).

Para crear clientes desde una [sesión del PdV abierta](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#pos-session-start) haga clic en Cliente ‣ Crear, e ingrese la información de contacto. También puede crear clientes desde el backend, solo debe ir a Punto de venta ‣ Órdenes ‣ Clientes y haga clic en Nuevo. Llena la información de contacto y guarde los cambios.

Para elegir al cliente durante una orden, en la interfaz del Punto de venta haga clic en Cliente. También puede seleccionar al cliente en la pantalla del pago, solo haga clic en Cliente.

## Notas del cliente[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#customer-notes "Enlazar permanentemente con este título")

Puede agregar **notas del cliente** sobre productos específicos desde una [sesión de punto de venta](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#pos-session-start) abierta. Por ejemplo, para dar consejos sobre limpieza y mantenimiento. También se puede usar para rastrear solicitudes específicas de los clientes, por ejemplo, es posible que no quieran que ensamblemos un producto por ellos.

Para hacerlo, seleccione un producto y haga clic en Nota de cliente. Se abrirá una ventana emergente en la que podrá agregar una nota o modificarla.

 Nota

Las notas de un producto de una [orden de venta importada](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/sales_order.html) se muestran tal cual en el carrito.

![Botón de notas del cliente y notas de los productos en los carritos del cliente (orden de venta y sesión de punto de venta)](https://www.odoo.com/documentation/17.0/es/_images/customer-notes.png)

Las notas de los clientes también aparecen en los recibos y en las facturas, como aparecen en el carrito abajo de producto relacionado.

![Recibo para el cliente con notas de la orden de venta y de la función de nota del cliente](https://www.odoo.com/documentation/17.0/es/_images/notes-receipt.png)

## Regresar y reembolsar productos[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#return-and-refund-products "Enlazar permanentemente con este título")

Para regresar o reembolsar un producto,

1. [inicie una sesión](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#pos-session-start) desde el **tablero del PdV**;
    
2. haga clic en Reembolsar y seleccione una orden correspondiente;
    
3. seleccione el producto y la cantidad a reembolsar con el teclado;
    
4. haga clic en Reembolso para regresar a la ventana anterior;
    
5. una vez que complete la orden, haga clic en Pago para avanzar al reembolso;
    
6. haga clic en Validar y en Nueva orden para seguir con el siguiente cliente.
    

![vista de reembolso desde el PdV.](https://www.odoo.com/documentation/17.0/es/_images/refund.png)

 Nota

- Con la barra de búsqueda puede filtrar la **lista de órdenes** por Número de recibo, Fecha o Cliente.
    
- Otra forma de reembolsar un producto es seleccionar el producto que se regresó desde una sesión abierta y ponga una cantidad negativa que sea igual al número de productos regresados. Para hacerlo, haga clic en Cant. y agregue +/- seguido por la cantidad de productos que se regresaron.
    

## Gestión de la caja registradora[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#manage-the-cash-register "Enlazar permanentemente con este título")

Para ingresar o retirar efectivo de la caja registradora, haga clic en el **icono de menú** en la esquina superior derecha de su pantalla y haga clic en Entrada/salida de efectivo.

![Menú desplegable para cerrar la sesión del PdV, ir al backend, agregar o tomar efectivo o tomar órdenes.](https://www.odoo.com/documentation/17.0/es/_images/menu-button.png)

Al hacerlo se abrirá una ventana emergente en la cual puede seleccionar Entrada de efectivo o Salida de efectivo, ingrese la cantidad y la razón y haga clic en Confirmar.

## Cierre de la sesión del PdV[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#close-the-pos-session "Enlazar permanentemente con este título")

Para cerrar su sesión, haga clic en el **icono de menú** que se ubica en la esquina superior derecha de su pantalla y haga clic en Cerrar sesión.

Al hacer esto se abrirá una ventana emergente de Control de cierre. En esta pestaña puede obtener mucha información:

- el número de ordenes que se hicieron y la cantidad total que se ganó durante la sesión;
    
- las cantidades esperadas agrupadas por método de pago.
    

Antes de cerrar esta ventana, haga clic en el icono de calculadora para contar su efectivo. Se abrirá una ventana emergente en donde se calculará la cantidad total en la caja registradora dependiendo de las monedas y billetes que se contaron y se sumaron de manera manual. Después, haga clic en Confirmar o en Descartar para cerrar la venta. La cantidad calculada estará en la columna Contado y los Detalles monetarios se especifican en la sección de **Notas**.

![Cómo cerrar una sesión del PdV.](https://www.odoo.com/documentation/17.0/es/_images/closing-control.png)

Una vez que haya terminado de controlar las cantidades, haga clic en Cerrar sesión para cerrar y regresar al **tablero del PdV**.

 Nota

- Para ir al backend sin cerrar la sesión abra el menú desplegable y haga clic en Backend.
    
- Para cancelar, haga clic en Descartar.
    
- Según su configuración, es posible que solo pueda cerrar sesión si el ingreso en efectivo esperado es igual al efectivo que contó. Para cerrar sesión aunque no coincida, haga clic en De acuerdo en la pantalla de Diferencia de pagos.
    

 Truco

- Es extremadamente recomendable que cierre su sesión del punto de venta al final de cada día.
    
- Para ver todas sus sesiones anteriores, vaya a Punto de venta ‣ Órdenes ‣ Sesiones.
    

- [Gestión de varios empleados](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/employee_login.html)
- [Recibos y facturas](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/receipts_invoices.html)
- [Sets de productos](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/combos.html)
- [Configuración](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration.html)
    - [Impresoras ePOS](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/epos_printers.html)
    - [Conexión segura (HTTPS)](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/https.html)
    - [Certificado autofirmado para impresoras electrónicas del PdV](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/epos_ssc.html)
- [Funciones de tienda](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#)
    - [Orden de venta](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/sales_order.html)
    - [Códigos de barras](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/barcode.html)
    - [Números de serie y lotes](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/serial_numbers.html)
    - [Enviar después](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/ship_later.html)
    - [Pantalla del cliente](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/shop/customer_display.html)
- [Funciones para restaurantes](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant.html)
    - [Pisos y mesas](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant/floors_tables.html)
    - [Impresión de órdenes](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant/kitchen_printing.html)
    - [Facturas](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant/bill_printing.html)
    - [Propinas](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/restaurant/tips.html)
- [Funciones de precios](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale.html#)
    - [Descuentos](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/discounts.html)
    - [Etiquetas de descuento (lector de código de barras)](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/discount_tags.html)
    - [Programas de lealtad](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/loyalty.html)
    - [Tarifas](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/pricelists.html)
    - [Impuestos flexibles (posiciones fiscales)](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/fiscal_position.html)
    - [Redondeo de efectivo](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/cash_rounding.html)
    - [Etiquetas electrónicas para estanterías](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/pricing/electronic_labels.html)
- [Métodos de pago](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods.html)
    - [Terminales de pago](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals.html)
        - [Adyen](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/adyen.html)
        - [Ingenico](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/ingenico.html)
        - [SIX](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/six.html)
        - [Stripe](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/stripe.html)
        - [Vantiv](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/vantiv.html)
        - [Worldline](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/payment_methods/terminals/worldline.html)
- [Reportes](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/reporting.html)