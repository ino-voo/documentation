Las _nomenclaturas de código de barra_ definen cómo los códigos de barra se reconocerán y categorizarán. Cuando se escanea un código de barras, se asocia a la **primera** regla con un patrón que coincida. La sintaxis del patrón se describe en la nomenclatura de Odoo con una expresión regular. El código de barras se leerá de forma correcta con Odoo si el prefijo o la longitud coincide con lo que se definió en la regla de código de barras.

La aplicación _Código de barras_ de Odoo es compatible con UPC (Código universal de producto), EAN (Número de artículo internacional o europeo) y la codificación GS1. Las nomenclaturas preconfiguradas en Odoo son _Nomenclatura predeterminada_ y _Nomenclatura GS1 predeterminada_. La nomenclatura predeterminada usa la codificación UPC y EAN, y es compatible con la conversión UPC/EAN.

 Importante

Los códigos de barra UPC y EAN **deben** [comprarse de GS1](https://www.gs1.org/standards/get-barcodes) para usar esos códigos de barras. GS1 es el **único** proveedor oficial de UPC/EAN yGS1 GTINs in en el mundo.

## Configurar una nomenclatura de código de barras[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/operations/barcode_nomenclature.html#set-up-barcode-nomenclature "Enlazar permanentemente con este título")

Para utilizar la nomenclatura predeterminada, vaya a Inventario ‣ Configuración ‣ Ajustes. En la sección Código de barras, haga clic en la casilla ubicada junto a Lector de códigos de barras para habilitarlos. Esta acción instala la aplicación _Código de barras_ en la base de datos.

Después, asegúrese de que haya seleccionado Nomenclatura predeterminada en el campo Nomenclatura de código de barras. Después haga clic en Guardar.

![Imagen en la que se activó el ajuste código de barra con Nomenclatura predeterminada seleccionada.](https://www.odoo.com/documentation/17.0/es/_images/barcode-nomenclature-enabled-setting.png)

Una vez guardada y seleccionada la nomenclatura, se puede acceder a la configuración de Nomenclaturas de códigos de barras, a través de un menú oculto que **solo** se puede descubrir tras activar el modo [desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode).

Con el modo desarrollador activado, vaya a al menú aplicación Inventario ‣ Configuración ‣ Nomenclaturas de código de barras y seleccione Nomenclatura predeterminada.

Desde esta página, debe especificar la Nomenclatura de código de barras en la parte superior como la `Nomenclatura predeterminada`.

Aquí, el campo Conversión UPC/EAN está configurado como Siempre de forma predeterminada. Este ajuste determina si un código de barras [|UPCI/IEAN|](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/operations/barcode_nomenclature.html#id1) debe convertirse de forma automática de una forma u otra al intentar coincidir una regla con la codificación.

Las otras opciones disponibles para este campo son Nunca, EAN-13 a UPC-A, y UPC-A a EAN-13.

 Importante

Para que la conversión UPC/EAN funcione en cada código de barras escaneado, el ajuste en el campo conversión UPC/EAN **debe** ser Siempre.

El último campo en la parte superior de la pantalla es el campo Es nomenclatura GS1. Para la Nomenclatura predeterminada el campo se debe dejar desmarcado, ya que usa codificación UPC y EAN, _no_ GS1.

![Ajustes de la página Nomenclatura predeterminada.](https://www.odoo.com/documentation/17.0/es/_images/barcode-nomenclature-page-fields.png)

Más abajo en la página hay una lista que muestra nombre de la regla, tipo, codificación y el patrón de código de barras para las _reglas_ y _patrones de código de barras_ con las que Odoo es compatible para la nomenclatura predeterminada.

La [lista de nomenclaturas predeterminadas](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/operations/barcode_nomenclature.html#barcode-operations-default-nomenclature-list) incluye toda la información que se puede condensar con un código de barras UPC/EAN.

## Uso de códigos de barra UP/EAN en Odoo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/operations/barcode_nomenclature.html#use-upc-ean-barcodes-in-odoo "Enlazar permanentemente con este título")

Para identificar productos con códigos de barra UPC/EAN en Odoo, las empresas _deben_ obtener [códigos de barra](https://www.gs1us.org/upcs-barcodes-prefixes/how-to-get-a-upc-barcode) que hayan comprado directamente de GS1.

Los formatos UPC y EAN se usan principalmente en sus propias regiones. UPC solo se usa en los Estados Unidos y Canadá, mientras que EAN se usa en el resto del mundo.

Un UPC usualmente es un código de barras de 12 dígitos que se usa para identificar la mayoría de los productos, mientras que los códigos de barra EAN son 13 dígitos que se usan para identificar productos.

Los códigos UPC se pueden convertir a EAN prefijándolos con un cero. En Odoo, los códigos de barra UPC/EAN se convierten de una u otra manera al momento de coincidir una regla con otra codificación.

Consulte la [lista predeterminada de nomenclatura](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/operations/barcode_nomenclature.html#barcode-operations-default-nomenclature-list) para ver una lista completa de todos los patrones de código de barras y todas las reglas que se deben seguir.

### Creación de reglas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/operations/barcode_nomenclature.html#create-rules "Enlazar permanentemente con este título")

Los códigos de barras UPC y EAN incluyen información específica en el código de barras. Los datos correspondientes en la base de datos de Odoo se completan en automático automáticamente al escanear estos códigos de la [lista de nomenclaturas predeterminadas](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/operations/barcode_nomenclature.html#barcode-operations-default-nomenclature-list).

Agregar nuevas reglas de códigos de barra a esta lista asegura que los formatos no estándar (creados por el usuario) se interpreten correctamente.

Para crear nuevas reglas, primero debe activar el [modo desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode). Después, navegue a la aplicación Inventario ‣ Configuración ‣ Nomenclaturas de código de barras. Seleccione la opción Nomenclatura predeterminada.

En la página Nomenclatura predeterminada, seleccione Agregar una línea en la parte inferior de la tabla. Esta acción abrirá una ventana emergente llamada Crear reglas para crear una.

![Ventana emergente llamada Crear reglas en la página Nomenclatura predeterminada.](https://www.odoo.com/documentation/17.0/es/_images/barcode-nomenclature-new-rule-popup.png)

El campo Nombre de la regla se usa de forma interna para identificar a qué código de barras representa.

El campo secuencia representa la prioridad de la regla. Esto quiere decir que mientras menor sea el valor, la regla aparecerá más arriba en la tabla.

El campo Tipo del código de barras representa distintas clasificaciones de la información que puede comprender el sistema (por ejemplo, Paquete, Lote, Ubicación, Cupón, etc.).

El campo Codificación especifica qué codificación utiliza el código de barras; esta regla **solo** se aplica si el código de barras utiliza esta codificación específica. Las opciones de Codificación disponibles son: EAN-13, EAN-8, UPC-A, y GS1-28.

El campo Patrón de código de barras representa cómo el sistema reconoce la secuencia de letras o números para contener información sobre el producto. Odoo sigue el orden secuencial de esta tabla, y usa la primera regla que encuentra, basada en la secuencia.

 Nota

Los patrones de código de barra también pueden definir cómo los valores numéricos, como peso o precio, se pueden codificar en el código de barra.

Se indican mediante **{NNN}**, donde `N` define dónde se codifican los dígitos del número. Los _Flotantes_ también se admiten con los decimales, indicados por `D`, como **{NNNDD}**.

En este caso, el campo de código de barras en los registros asociados **debe** mostrar estos dígitos como ceros.

Después de llenar la infirmación, haga clic en Guardar y crear nuevo para guardar la regla y crear una nueva de inmediato. También puede hacer clic en Guardar y cerrar para guardar y regresar a la tabla de reglas.

 Truco

Cuando el patrón de código de barras contiene `.*`, significa que puede contener **cualquier** número de caracteres y estos caracteres pueden ser **cualquier** número o tipo de carácter.

## Lista de nomenclatura predeterminada[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/operations/barcode_nomenclature.html#default-nomenclature-list "Enlazar permanentemente con este título")

La siguiente tabla contiene la lista de reglas de Nomenclatura predeterminada de Odoo. Los patrones de código de barra se escriben en expresiones regulares.

|Nombre de regla|Tipo|Codificación|Patrón de código de barras|
|---|---|---|---|
|Código de barra de precios de 2 decimales|Producto con precio|EAN-13|23…..{NNNDD}|
|Códigos de barras de descuentos|Producto con descuento|Cualquiera|22{NN}|
|Código de barras de peso de 3 decimales|Producto pesado|EAN-13|21…..{NNDDD}|
|Códigos de barras de clientes|Cliente|Cualquiera|042|
|Código de barras de cupones y tarjetas de regalo|Cupón|Cualquiera|043\|044|
|Código de barras de cajeros|Cajero|Cualquiera|041|
|Códigos de barra de ubicaciones|Ubicación|Cualquiera|414|
|Código de barras del paquete|Paquete|Cualquiera|PAQUETE|
|Códigos de barra de lote|Lote|Cualquiera|10|
|Tarjeta de crédito magnetica|Tarjetas de Crédito|Cualquiera|%.*|
|Códigos de barras de productos|Unidad de producto|Cualquiera|.*|

 Ver también

[Nomenclatura de código de barras GS1](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/operations/gs1_nomenclature.html)