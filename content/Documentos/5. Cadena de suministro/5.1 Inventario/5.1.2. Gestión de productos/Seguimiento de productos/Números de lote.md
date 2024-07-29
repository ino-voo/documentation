Los _lotes_ son una de las dos formas de identificar y rastrear productos en Odoo. Por lo general representan un lote específico de productos que recibió, almacenó, envió o fabricó de forma interna.

Los fabricantes asignan números de lote a grupos de producto que comparten ciertas propiedades, de esta forma la trazabilidad es mucho más sencilla durante todo el ciclo de vida del producto.

Los lotes son útiles para gestionar una gran cantidad de productos fabricados o recibidos, y ayudan a rastrear el grupo al que pertenecen los artículos, lo cual es útil para retiradas de productos o [fechas de caducidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/expiration_dates.html).

 Ver también

[Usar números de serie para rastrear productos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/serial_numbers.html)

## Activar lotes y números de serie[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#enable-lots-serial-numbers "Enlazar permanentemente con este título")

Para rastrear productos por medio de lotes debe activar la función _Números de serie y lote_. Vaya a Inventario ‣ Configuración ‣ Ajustes, busque la sección Trazabilidad, haga clic en la casilla junto a Números de serie y lote y luego haga clic en Guardar.

 Ver también

- [Trazabilidad de fechas de caducidad](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/expiration_dates.html)
    
- [Imprimir códigos de barra GS1 para lotes y números de serie](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/operations/gs1_usage.html#barcode-operations-gs1-lots)
    

![Active las funciones de lote y número de serie desde los ajustes del inventario.](https://www.odoo.com/documentation/17.0/es/_images/enabled-lots-setting.png)

## Rastrear por lotes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#track-by-lots "Enlazar permanentemente con este título")

Una vez que haya activado la función úmeros de lote y de serie, configure cada producto que debe rastrear mediante lotes. Para ello, vaya a Inventario ‣ Productos ‣ Productos y elija el producto a configurar.

Vaya a la pestaña Inventario del formulario del producto. En la sección Trazabilidad, seleccione la opción Por lotes en el campo Seguimiento. Ahora podrá asignar números de lote nuevos o existentes a los lotes que acaba de recibir o fabricar de este producto.

 Ver también

[Fechas de vencimiento](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/expiration_dates.html)

 Importante

Aparecerá un mensaje de advertencia en caso de que un producto tenga existencias disponibles antes de activar el seguimiento por números de serie o lote. Utilice un [ajuste de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/reassign.html) para asignar números de lote a los productos existentes.

![Función de seguimiento por lotes activada en el formulario del producto.](https://www.odoo.com/documentation/17.0/es/_images/tracking-product-form.png)

## Asignar lotes para envío y recepción[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#assign-lots-for-shipping-and-receiving "Enlazar permanentemente con este título")

Asigna nuevos número de lotes a [bienes entrantes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#inventory-product-management-assign-lots) en el formulario de recepción. Al enviar [productos salientes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#inventory-product-management-assign-lots-delivery), seleccione productos con números de lote específicos en el formulario de entrega.

### Al recibir[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#on-receipts "Enlazar permanentemente con este título")

Puede asignar números de lote nuevos o existentes a bienes entrantes directamente en las recepciones.

Para comenzar, vaya a la aplicación Compra para [crear y confirmar](https://www.youtube.com/watch?v=o_uI718P1Dc) una orden de compra de productos rastreados por números de lote. Después, haga clic en el botón inteligente Recibo que aparece en la parte superior de la página para ir al formulario correspondiente.

 Nota

Si quiere ver una recepción existente vaya a la aplicación Inventario, haga clic en la tarjeta de kanban Recibos y seleccione el recibo deseado.

 Importante

Al hacer clic en Validar antes de asignar un número de lote ocurrirá un error. Esto indica que **debe** asignar un número de lote antes de validar la recepción.

![Ventana emergente de error de usuario para agregar un lote o número de serie.](https://www.odoo.com/documentation/17.0/es/_images/user-error.png)

En el formulario de recepción, en la línea del producto en la pestaña Operaciones, seleccione el icono ⦙≣ (lista con viñetas) ubicado a la derecha del producto rastreado por número de lote.

![Imagen del icono de lista con viñetas en la línea de producto.](https://www.odoo.com/documentation/17.0/es/_images/list-icon.png)

Esta acción abre la ventana emergente Abrir: Movimiento de existencias, allí se asignan el número de serie o lote y la cantidad.

Hay dos formas de asignar números de lote, puede hacerlo de **forma manual** o al **importar**.

#### Asignación manual[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#manual-assignment "Enlazar permanentemente con este título")

Haga clic en Agregar una línea para asignar números de lote de forma manual. Escriba el número de serie o lote, la ubicación correspondiente a Almacenar en, la cantidad y el paquete de destino en caso de que haya uno.

 Nota

Haga clic en Agregar una línea para asignar varios números de lote o almacenar en varias ubicaciones, escriba un nuevo número de serie o de lote para las cantidades adicionales. Repita este proceso hasta que el total en la columna Cantidad coincida con la demanda ubicada en la parte superior.

![Ventana emergente an la que asigne las operaciones detalladas del número de lote.](https://www.odoo.com/documentation/17.0/es/_images/assign-lots-popup.png)

#### Importar lotes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#import-lots "Enlazar permanentemente con este título")

En la ventana emergente Abrir: Movimiento de existencias haga clic en Importar números de serie o lote y luego pegue los números correspondientes en el campo Número de serie o lote.

![Lista de números de lote que se copiaron en una hoja de cálculo de Excel.](https://www.odoo.com/documentation/17.0/es/_images/lots-excel-spreadsheet.png)

Lista de los números de lote copiados en la hoja de cálculo de _Google_.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#id1 "Enlace permanente a esta imagen")

![Números de lote que se copiaron a la línea de número.](https://www.odoo.com/documentation/17.0/es/_images/bulk-sn.png)

Números de lote pegados en el campo «Número de serie o lote», en la ventana emergente **Importar lotes**.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#id2 "Enlace permanente a esta imagen")

En la ventana emergente Abrir: Movimiento de existencias seleccione la casilla Mantener las líneas actuales para generar números de lote _adicionales_. Para reemplazar los números de lote en la lista, no seleccione la opción Mantener las líneas actuales.

Por último, haga clic en Generar.

Una vez que haya asignado números de lote a los productos, haga clic en Guardar para cerrar la ventana emergente. Después, haga clic en Validar en el formulario de recepción.

 Ver también

[Reporte de trazabilidad para los números de lote](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#inventory-product-management-lot-traceability)

### Sobre órdenes de entrega[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#on-delivery-orders "Enlazar permanentemente con este título")

Con Odoo es posible especificar qué números de lote para un producto se elegirán para productos salientes en una orden de entrega.

Para comenzar, cree o seleccione una cotización existente en la aplicación Ventas. El botón inteligente Entrega estará disponible luego de confirmar la orden de venta, haga clic en él para ver el formulario de recibo de almacén para esa orden de ventas en específico.

 Nota

También puede ir a las órdenes de entrega desde la aplicación Inventario, allí haga clic en la tarjeta de kanban Órdenes de envío.

Al hacer clic en el botón inteligente Entrega se abre el formulario de orden de entrega en el que deberá seleccionar los números de lote para la entrega. En la pestaña Operaciones, haga clic en el icono ⦙≣ (lista con viñetas) ubicado a la derecha del producto que rastrea por números de lote. Al hacer clic en ese icono aparece la ventana emergente Abrir: Movimiento de existencias.

En la ventana emergente aparece el número de lote elegido y su ubicación de almacenamiento en la columna Recolectar de con la cantidad completa tomada de ese lote en específico (si hay suficientes existencias en ese lote en particular).

Si el lote no cuenta con cantidad suficiente o si las cantidades parciales de la demanda se tomarán de varios lotes, cambie la cantidad.

 Nota

El lote seleccionado para las entregas varía según la estrategia de remoción que elija (FIFO, UEPS o PEPS). También dependerá de la cantidad ordenada y si la cantidad disponible en un solo lote basta para completar la orden.

 Ver también

[Estrategias de remoción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html)

Repita los pasos anteriores para seleccionar suficientes lotes para cumplir con la demanda y haga clic en Guardar para cerrar la ventana emergente. Por último, haga clic en el botón Validar de la orden de envío para entregar los productos.

![Ventana emergente para el número de lote de origen en la orden de venta.](https://www.odoo.com/documentation/17.0/es/_images/pick-from-lots.png)

 Ver también

[Reporte de trazabilidad para los números de lote](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#inventory-product-management-lot-traceability)

## Gestión de lotes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#lot-management "Enlazar permanentemente con este título")

Para gestionar y ver los números de lote para productos en el tablero Lote/números de serie vaya a Inventario ‣ Productos ‣ Lotes/números de serie.

Los números de lote están agrupados por producto de forma predeterminada y al seleccionar el menú desplegable para cada producto aparecen los números existentes. Seleccione un número de lote para [modificar o agregar detalles](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#inventory-product-management-edit-lot) vinculados al lote. También puede [crear](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#inventory-product-management-create-new-lot) los números de lote desde esta página al hacer clic en el botón Nuevo.

![Imagen del tablero "lotes/números de serie".](https://www.odoo.com/documentation/17.0/es/_images/lot-dashboard.png)

Mostrar los números de lote agrupados por productos en el tablero **lote/número de serie**.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#id3 "Enlace permanente a esta imagen")

### Modificar lotes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#modify-lot "Enlazar permanentemente con este título")

Al hacer clic en un lote en el tablero Lote/número de serie se mostrará una página separada donde puede ingresar información adicional sobre el lote.

 Truco

Odoo genera un nuevo número de lote/serie en automático para continuar con el número más reciente, pero puede editarlo y cambiarlo a cualquier otro. Haga clic en la línea debajo del campo Número de lote/serie y cambie el número generado al número deseado.

En el formulario de número de lote es posible modificar los siguientes campos:

- Número de serie o lote: modifique el número de lote vinculado al producto.
    
- Referencia interna: registre un número de lote o de serie alternativo que se utiliza dentro del almacén y difiere del que utiliza el proveedor o el fabricante.
    
- Empresa: especifique la empresa en la que está disponible el número de lote.
    
- Descripción: agregue detalles adicionales sobre el lote o número de serie.
    

 Importante

Los campos Producto y Cantidad disponible **no** se pueden modificar en los lotes existentes porque los números de lote están vinculados a los movimientos correspondientes.

![Mostrar el formulario de número de lote](https://www.odoo.com/documentation/17.0/es/_images/lot-number.png)

 Ver también

[Configurar fechas de caducidad para lotes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/expiration_dates.html)

#### Agregar una propiedad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#add-property "Enlazar permanentemente con este título")

Para añadir campos personalizados que mejoren la trazabilidad de los lotes, hay dos métodos para agregar esas propiedades al formulario correspondiente:

1. Haga clic en el icono  (engranaje) ubicado del lado superior izquierdo de la página y después seleccione  Agregar propiedades en el menú desplegable.
    
2. Haga clic en el botón  Agregar una propiedad ubicado debajo de los campos existentes.
    

Proporciónele un nombre and [y configure el nuevo campo](https://www.odoo.com/documentation/17.0/es/applications/productivity/knowledge/properties.html). Al terminar, escriba el valor de la propiedad en él.

 Example

Aquí se agrega la nueva propiedad `Tipo de madera` y el valor se registra como `Madera de cerezo`.

![Mostrar el botón "Agregar propiedades" al formulario de un número de lote.](https://www.odoo.com/documentation/17.0/es/_images/add-properties.png)

 Ver también

[Configurar propiedades personalizadas](https://www.odoo.com/documentation/17.0/es/applications/productivity/knowledge/properties.html)

### Reservar el número de lote para un producto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#reserve-lot-number-for-a-product "Enlazar permanentemente con este título")

Para crear un número de lote para un producto, primero tiene que ir a Inventario ‣ Productos ‣ Lote/número de serie y haga clic en Nuevo.

 Importante

Al crear un número de lote, este se reserva para un producto pero **no** lo asigna. Consulte la sección sobre [asignación de números de lote al momento de la recepción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#inventory-product-management-assign-lots) para obtener más información sobre la asignación de números de lote.

 Truco

Odoo genera un nuevo número de lote/serie en automático para continuar con el número más reciente, pero puede editarlo y cambiarlo a cualquier otro. Haga clic en la línea debajo del campo Número de lote/serie en el formulario del lote y cambie el número generado.

Una vez que se genere el nuevo Lote/Número de serie haga clic en el campo vacío junto a Producto para mostrar el menú desplegable. En este menú, seleccione el producto al que se le asignará este número.

 Example

Se creó el número de lote `000001` para el producto `Cajonera negra`.

![Nuevo formulario de creación de número de lote con un producto asignado.](https://www.odoo.com/documentation/17.0/es/_images/new-lot-number.png)

Luego de crear, guardar y asignar un nuevo número de lote al producto deseado, el número de lote se guarda como un número de lote existente vinculado al producto y podrá seleccionarlo al [asignar números de lote a los productos de una recepción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#inventory-product-management-assign-lots) o al realizar un ajuste de inventario.

 Example

Luego de crear el número de lote `000001`, aparece como opción para `Cajonera negra` al asignar números de lote en la página Ajuste de inventario.

![Imagen sobre cómo asignar números de lote en la página Ajuste de inventario.](https://www.odoo.com/documentation/17.0/es/_images/inventory-adjustment.png)

## Gestione lotes para diferentes tipos de operaciones[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#manage-lots-for-different-operations-types "Enlazar permanentemente con este título")

De forma predeterminada, solo es posible crear nuevos lotes al recibir productos y no puede utilizar los números de lote existentes. En las órdenes de venta solo puede utilizar números de lote existentes y no puede crear nuevos en la orden de entrega.

Para cambiar si puede usar números de lote nuevos (o existentes) en cualquier tipo de operación, vaya a Inventario ‣ Configuración ‣ Tipos de operaciones y seleccione el tipo de operación deseado.

En el formulario del tipo de operación, en la sección Números de lote y serie, seleccione la casilla Crear nuevo para permitir la creación de nuevos números de lote durante este tipo de operación. Elija Utilizar existentes si solo es posible seleccionar números de lote existentes.

![Activar el ajuste de trazabilidad en el formulario de tipo de operaciones.](https://www.odoo.com/documentation/17.0/es/_images/operation-type-form.png)

 Truco

Para transferencias dentro del mismo almacén que involucren productos que se rastreen por lotes, lo mejor será activar la opción Utilizar números de Lotes / de serie existentes para recibos de inventario

## Trazabilidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#traceability "Enlazar permanentemente con este título")

Los fabricantes y las empresas pueden consultar los reportes de trazabilidad para ver el ciclo de vida completo de un producto: de dónde proviene, cuándo llegó, dónde se almacenó y a quién se envió (y cuándo).

Para ver la trazabilidad completa de un producto, o agrupar por lotes, vaya a la aplicación Inventario ‣ Productos ‣ Lotes/Números de serie. De esta manera podrá ve el tablero de Lotes/Números de serie.

Aquí se enlistarán en automático todos los productos a los que se les haya asignado un número de lote y se podrá expandir para mostrar los números de lote que esos productos tienen asignados.

Antes de agrupar por lotes es necesario que elimine los filtros en la barra de búsqueda. Después, haga clic en el icono :icon:`fa-caret-down (flecha hacia abajo) para abrir el menú desplegable con las opciones Filtros, Agrupar por y Favoritos. En la sección Agrupar por, haga clic en Agregar grupo personalizado y elija la opción correspondiente en el menú desplegable.

Esta acción reorganiza todos los registros en la página para mostrar todos los números de serie y lotes existentes. Es posible abrir la lista para visualizar todos los productos que tengan asignado ese número.

![Reporte de trazabilidad de los lotes y números de serie.](https://www.odoo.com/documentation/17.0/es/_images/group-by-number.png)

### Reporte de trazabilidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/lots.html#traceability-report "Enlazar permanentemente con este título")

Para ver un reporte completo del movimiento de existencias de un número de lote, seleccione la línea del número de lote en el tablero Número de serie o lote y, en el formulario correspondiente, haga clic en el botón inteligente Trazabilidad.

![Imagen sobre el reporte de trazabilidad para un lote donde se muestran movimientos de inventario.](https://www.odoo.com/documentation/17.0/es/_images/traceability-report.png)

 Ver también

[Diferencia entre lotes y números de serie](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/product_management/product_tracking/differences.html)