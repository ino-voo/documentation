Asignar números de serie a cada producto permite dar seguimiento a sus propiedades, [fechas de vencimiento](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/expiration_dates.html) y ubicación en toda la cadena de suministro, lo que beneficia sobre todo a los fabricantes que ofrecen servicios posventa.

 Ver también

- [Tutoriales Odoo: números de serie](https://www.youtube.com/watch?v=ZP-gMz2X5AY)
    
- [Usar números de serie para rastrear productos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/serial_numbers.html)
    

En Odoo, es posible asignar números de serie a los productos:

- en la [página de Operaciones detalladas](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#inventory-product-management-detailed-operations) de una recepción.
    
- al hacer clic en el botón [Asignar números de serie](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#inventory-product-management-assign-sn) de una recepción.
    
- en la [ventana Abrir: movimiento de existencias](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#inventory-product-management-stock-move-section) en una recepción.
    
- [durante la orden de fabricación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/configure_manufacturing_product.html) para un producto que rastrea mediante números de serie o lote.
    
- al realizar un ajuste de inventario.
    

![Visualización del botón inteligente Operaciones detalladas y el icono de lista con viñetas en una recepción.](https://www.odoo.com/documentation/17.0/es/_images/assign-serial-numbers.png)

Visualización del botón inteligente **Operaciones detalladas** y el icono de lista con viñetas en una recepción.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#id2 "Enlace permanente a esta imagen")

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#configuration "Enlazar permanentemente con este título")

Para asignar números de serie a productos debe habilitar la función Números de serie y lote en Inventario ‣ Configuración ‣ Ajustes.

Después, en la pestaña Inventario del formulario de un producto, seleccione Por número de serie único en el campo Seguimiento.

 Ver también

- [Habilitar números de serie](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/serial_numbers.html#inventory-product-management-enable-lots)
    
- [Seguimiento de productos por números de serie](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/serial_numbers.html#inventory-product-management-configure-lots)
    

Vaya a Inventario ‣ Configuración ‣ Tipos de operaciones para habilitar la creación de nuevos números de serie.

En la página Tipos de operaciones elija el tipo correspondiente (por ejemplo, Recibos, Órdenes de entrega o Fabricación) y seleccione la opción Crear nuevo en la sección Números de serie y lote de la página de configuración del tipo de operación.

![Visualización de la opción "Crear nuevo" seleccionada en el tipo de operación Recibos.](https://www.odoo.com/documentation/17.0/es/_images/create-new.png)

## Operaciones detalladas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#detailed-operations "Enlazar permanentemente con este título")

En la página Operaciones detalladas de la recepción es posible asignar números de serie a los productos cuando ingresan a sus existencias. Para acceder a las recepciones vaya a Inventario ‣ Operaciones ‣ Recepciones.

 Importante

Los números de serie **no** se pueden asignar a los productos desde una solicitud de cotización u orden de compra, **solo** al recibirlos.

![Visualización de la orden de compra y el botón inteligente Recepción.](https://www.odoo.com/documentation/17.0/es/_images/purchase-order-or-receipt.png)

Captura de pantalla de una orden de compra con el botón inteligente «Recibo» en la parte superior.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#id3 "Enlace permanente a esta imagen")

Para registrar el número de serie de un artículo antes de recibirlo, siga los pasos de las siguientes secciones para asignar números de serie, pero **no** haga clic en el botón Validar hasta que reciba los productos del proveedor.

Haga clic en el botón inteligente Operaciones detalladas de una recepción para asignar un número de serie a un producto.

En la columna Nombre del número de serie o lote escriba el número de serie para un producto.

![Agregar una línea en la página Operaciones detalladas para asignar números de serie.](https://www.odoo.com/documentation/17.0/es/_images/add-a-line.png)

Al finalizar haga clic en las migas de pan, los números de serie asignados se guardan de forma automática.

## Asignar números de serie[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#inventory-product-management-assign-sn "Enlazar permanentemente con este título")

Para generar nuevos números de serie en una secuencia, haga clic en el icono + (más) en la [línea del producto](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#inventory-product-management-detailed-operations-popup).

![El icono de más en la línea de producto.](https://www.odoo.com/documentation/17.0/es/_images/plus-icon.png)

 Importante

Si el icono no es visible, asegúrese de que la opción Crear nuevo esté seleccionada en la [página de configuración del recibo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#inventory-product-management-configure-new-serials).

Esta acción abre la ventana emergente Asignar números de serie. El campo Cantidad de números de serie se completa en automático según el número de productos que necesitan un número de serie. Escriba el primer número de serie en el campo Primer número de serie y haga clic en Asignar números de serie para generar una secuencia basada en el primer número proporcionado.

![La ventana emergente Asignar números de serie.](https://www.odoo.com/documentation/17.0/es/_images/assign-numbers-in-sequence.png)

## La ventana emergente de movimientos de existencias.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#stock-move-pop-up-window "Enlazar permanentemente con este título")

Para visualizar varios métodos de asignación masivos de números de serie, haga clic en el ícono ⦙≣ (lista con viñetas) en la [línea del producto](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#inventory-product-management-detailed-operations-popup) de un recibo.

### Agregar línea[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#add-a-line "Enlazar permanentemente con este título")

Agregue de forma manual los números de serie en la columna Número de serie o lote en la ventana emergente Abrir: Movimiento de existencias que aparece.

![Agregar una línea en la ventana emergente de movimiento de existencias.](https://www.odoo.com/documentation/17.0/es/_images/add-a-line-stock-move.png)

### Generar números de serie[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#generate-serials "Enlazar permanentemente con este título")

Para asignar varios números de serie al mismo tiempo haga clic en el botón Generar números de serie o lote en la ventana emergente Abrir: Movimiento de existencias.

![El botón Generar números de serie.](https://www.odoo.com/documentation/17.0/es/_images/generate-serials.png)

Esta acción abre la ventana emergente Generar números de serie, ahí debe escribir el primer número de serie en el campo Primer número de serie para generar una secuencia de números basada en el primero.

[consulte esta sección](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#inventory-product-management-assign-sn) para obtener más detalles sobre cómo completar esta ventana emergente.

### Importar números de serie[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#import-serials "Enlazar permanentemente con este título")

Para asignar varios números de serie al mismo tiempo haga clic en el botón Importar números de serie o lote en la ventana emergente Abrir: Movimiento de existencias.

 Importante

Si el botón no es visible, asegúrese de que la opción Crear nuevo esté seleccionada en la [página de configuración del recibo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/create_sn.html#inventory-product-management-configure-new-serials).

Esta acción abre la ventana emergente Importar lotes, allí escriba cada número de serie en una línea distinta en el campo de texto Números de serie o lote.

 Truco

Copie y pegue los números de serie de una hoja de cálculo de Excel, después agréguelos al campo de texto Números de serie/lote.

![Visualización de la hoja de Excel para copiar los números de serie.](https://www.odoo.com/documentation/17.0/es/_images/copy-from-excel.png)

En la ventana emergente Abrir: Movimiento de existencias seleccione la casilla Mantener las líneas actuales para agregar números de serie a la lista de productos y a la tabla Número de serie o lote. Para reemplazar los números de serie en la lista, no seleccione la opción Mantener las líneas actuales.

Por último, haga clic en Generar.

 Example

Para una recepción con una demanda de `3.00` productos, ya se asignó un número de serie a un producto en la ventana emergente Abrir: Movimiento de existencias.

En la ventana emergente Importar lotes se asignarán dos números de serie, `124` y `125`, a los productos restantes. Para ello, es necesario escribirlos en el campo Números de serie o lote:

124
125

La opción Mantener las líneas actuales está seleccionada para agregar estos números de serie **además** del número `123` que ya había sido asignado.

![Visualización del ejemplo: aparecen los números de serie en el campo de texto.](https://www.odoo.com/documentation/17.0/es/_images/import-serial.png)