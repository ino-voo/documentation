Una _lista de materiales_ (o _LdM_, para abreviar) documenta componentes específicos y la cantidad necesaria de los mismos para producir o reparar un producto. En Odoo, las LdM sirven como modelos para bienes fabricados y kits. Además, suelen incluir operaciones de producción e instrucciones detalladas.

## Configuración de listas de materiales[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html#bom-setup "Enlazar permanentemente con este título")

Vaya Fabricación ‣ Productos ‣ Listas de materiales y haga clic en Nuevo para crear una LdM.

Después configure el Tipo de lista de materiales como Fabricar este producto.

Especifique los [componentes necesarios](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html#manufacturing-basic-setup-setup-components) y, cuando proceda, defina cualquier [operación de fabricación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html#manufacturing-basic-setup-setup-operations).

 Truco

También puede acceder a cada lista de materiales o crearlas con rapidez al hacer clic en el botón inteligente Lista de Materiales en cualquier formulario de producto en las aplicaciones _Ventas_, _Inventario_ y _Fabricación_, así como a través de cualquier enlace interno en el que haya una referencia a un producto (como en un campo o un artículo de línea).

![Mostrar la LdM de un producto con sus respectivos componentes.](https://www.odoo.com/documentation/17.0/es/_images/bom-example.png)

LdM para `Cajonera` con la pestaña **Componentes**.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html#id1 "Enlace permanente a esta imagen")

 Ver también

- [Usar kits](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/advanced_configuration/kit_shipping.html)
    
- [Subcontratación básica](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html)
    

### Componentes[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html#components "Enlazar permanentemente con este título")

Especifique los componentes utilizados para fabricar el producto en la pestaña Componentes de una LdM, haga clic en Agregar una línea. Con el menú desplegable Componentes podrá seleccionar entre productos existentes o crear uno nuevo al escribir el nombre y seleccionar la opción Crear » « para agregar el artículo a la línea. También puede usar la opción Crear y editar… si desea agregar el componente y completar su formulario de configuración.

![Para agregar un componente es necesario seleccionarlo en el menú desplegable.](https://www.odoo.com/documentation/17.0/es/_images/component.png)

También puede acceder a campos adicionales al hacer clic en el icono  (ajustes de configuración) ubicado en el extremo derecho de la pestaña Componentes. Seleccione las casillas para habilitar las siguientes columnas:

- Aplicar en variantes: especifique en qué [variante de producto](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/advanced_configuration/product_variants.html) se utiliza cada componente. El componente se utiliza en todas las variantes cuando el campo está vacío.
    

- Consumido en la operación: especifique la operación que utiliza el componente. Es útil para determinar la [preparación para la fabricación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html#manufacturing-basic-setup-manufacturing-readiness).
    
- Consumo manual: seleccione la casilla para obligar a los operadores a que marquen la casilla Consumido en una orden de fabricación.
    
    ![Visualización de una orden de fabricación, el campo *Consumido* aparece en un recuadro rojo.](https://www.odoo.com/documentation/17.0/es/_images/consumed-field.png)
    
    Si no lo hacen, aparece el mensaje de error Advertencia de Consumo, donde deberán ingresar la cantidad consumida del componente de forma manual o la operación no se podrá completar.
    
    ![Mostrar el mensaje de error de advertencia de consumo.](https://www.odoo.com/documentation/17.0/es/_images/consumption-warning.png)
    

### Operaciones[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html#operations "Enlazar permanentemente con este título")

Agregue una _operación_ a una lista de materiales para especificar las instrucciones de producción y registrar el tiempo utilizado en una operación. Para usar esta función, primero habilite las _órdenes de trabajo_ en Fabricación ‣ Configuración ‣ Ajustes, vaya a la sección Operaciones y seleccione la casilla Órdenes de trabajo para habilitarlas.

 Ver también

[Dependencias de la orden de trabajo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/advanced_configuration/work_order_dependencies.html)

![Función "Órdenes de trabajo" en la página de ajustes.](https://www.odoo.com/documentation/17.0/es/_images/enable-work-orders.png)

Vaya a la lista de materiales desde Fabricación ‣ Productos ‣ Lista de materiales y seleccione la lista correspondiente. Para agregar una nueva operación, vaya a la pestaña Operaciones y haga clic en Agregar una línea.

Esta acción abre la ventana emergente Crear Operaciones, donde podrá configurar los campos de la operación:

- Operación: nombre de la operación.
    
- Centro de trabajo: seleccione las ubicaciones existentes para realizar la operación. También puede crear un centro nuevo, para ello escriba el nombre y seleccione la opción Crear » «.
    
- Aplicar en variantes: especifique si la operación está disponible solo para ciertas variantes de producto. Deje este campo vacío si la operación se aplica a todas las variantes.
    
     Ver también
    
    [Configurar listas de materiales para variantes de producto](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/advanced_configuration/product_variants.html)
    
- Cálculo de duración: elija cómo se registra el tiempo utilizado en la operación. Seleccione Calcular según el tiempo registrado para utilizar el temporizador de la operación o Establecer duración de forma manual si los operadores pueden registrar y modificar el tiempo por su cuenta.
    
    Al elegir Calcular según el tiempo registrado se habilita la opción Según las últimas __ órdenes de trabajo, que estima el tiempo necesario para completar esta operación de forma automática según las últimas operaciones. Al elegir Establecer la duración de forma manual se habilita el campo Duración predeterminada.
    
- Duración predeterminada: cantidad estimada de tiempo para completar la operación. Esta se utiliza para [planificar órdenes de fabricación](https://www.youtube.com/watch?v=TK55jIq00pc) y para determinar la [disponibilidad del centro de trabajo](https://www.youtube.com/watch?v=3YwFlD97Bio).
    
- Empresa: especifique la empresa en la que está disponible la lista de materiales.
    

Incluya los detalles de la operación en la pestaña Hoja de trabajo. Elija PDF para adjuntar un archivo o una presentación de Google con acceso _público_ para compartir un enlace. Seleccione Texto para escribir las instrucciones en el campo Descripción.

 Truco

Escriba `/` para ver una lista de opciones de formato y funciones, incluido ChatGPT.

![Visualización de la función de ChatGPT para generar instrucciones para un orden de trabajo.](https://www.odoo.com/documentation/17.0/es/_images/description.png)

![Completar la ventana emergente Crear operaciones.](https://www.odoo.com/documentation/17.0/es/_images/create-operations.png)

Por último, haga clic en Guardar y cerrar para cerrar la ventana emergente. Haga clic en Guardar y crear nuevo si desea agregar más operaciones y repita los pasos anteriores para configurar otra operación.

 Nota

Cada operación es única, ya que siempre está vinculada solo a una LdM.

 Truco

Luego de crear una operación, haga clic en el botón Copiar operaciones existentes para elegir la operación que desea duplicar.

![El campo *Copiar operaciones existentes* aparece destacado en la pestaña Operaciones.](https://www.odoo.com/documentation/17.0/es/_images/copy-existing-operations.png)

#### Instrucciones[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html#instructions "Enlazar permanentemente con este título")

 Importante

La aplicación _Calidad_ debe estar instalada para que pueda agregar instrucciones detalladas a las operaciones.

Agregue instrucciones específicas a una operación existente al hacer clic en el icono  (lista) de la columna Instrucciones. El número en esta columna indica la cantidad de instrucciones detalladas existentes para la operación.

![Mostrar la columna Instrucciones y el icono de lista.](https://www.odoo.com/documentation/17.0/es/_images/add-instructions.png)

Haga clic en Nuevo en el tablero Pasos para abrir un formulario de punto de control de calidad vacío donde podrá crear el nuevo paso de fabricación. Aquí, proporciónele un título a la instrucción específica y establezca el tipo como Instrucciones. Escriba las indicaciones para el paso de la operación en la pestaña Instrucciones del formulario.

 Nota

En este formulario es posible realizar otras personalizaciones además de las instrucciones comunes, por ejemplo, para incluir puntos específicos de control de calidad con condiciones específicas (o complejas). Consulte la documentación sobre [control de tipo instrucciones](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_check_types/instructions_check.html) para obtener más información sobre los puntos de control de calidad.

![Mostrar la página para agregar un control de calidad.](https://www.odoo.com/documentation/17.0/es/_images/steps.png)

### Varios[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html#miscellaneous "Enlazar permanentemente con este título")

En la pestaña Varios hay más ajustes a usar en la lista de materiales para personalizar el aprovisionamiento, calcular los costos y definir cómo se consumen los componentes.

- Preparación para la fabricación: al seleccionar Cuando los componentes para la primera operación están disponibles, el estado del componente es No disponible en color **verde** solo cuando hay existencias de los componentes que se utilizan en la primera operación. Esto indica que aunque no todos los componentes están disponibles, los operadores al menos pueden comenzar con la primera operación. Al seleccionar Cuando todos los componentes están disponibles, el estado del componente es No disponible en color **rojo** a menos que todos los componentes estén disponibles.
    
     Truco
    
    Especifique qué operación consume cada componente de la lista de materiales en el campo [Consumo manual](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html#manufacturing-basic-setup-consumed-in-operation).
    
    ![Visualización del campo *Estado del componente* en el tablero de órdenes de fabricación.](https://www.odoo.com/documentation/17.0/es/_images/component-status.png)
    
- Versión: muestra la versión actual de la lista de materiales. Es visible con la aplicación _PLM_ instalada para gestionar los cambios en la LdM.
    
- Consumo flexible: especifica si los componentes utilizados pueden diferir de la cantidad definida en la lista de materiales. Elija Bloqueado si los operadores **deben** apegarse estrictamente a la cantidad de la LdM. De lo contrario, elija Permitido o Permitido con advertencia.
    
- Enrutamiento: seleccione el tipo de operación de fabricación preferido del almacén para los productos que se producen en varios almacenes. Si está vacío, entonces se utiliza el tipo de operación `Fabricación` de este almacén de forma predeterminada.
    
- Distribución analítica: seleccione [modelos de distribución analítica](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/analytic_accounting.html) creados con anterioridad de la lista para registrar el costo de fabricación de productos en el diario seleccionado de forma automática.
    
- Plazo de fabricación: defina el número de días necesarios para completar una orden de fabricación desde la fecha de confirmación.
    
- Días para preparar la orden de fabricación: número de días necesarios para reabastecer componentes o fabricar los subensamblajes del producto.
    

 Ver también

- [Distribución analítica](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/analytic_accounting.html)
    
- [Plazos de entrega](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/scheduled_dates.html)
    

![Visualización de la pestaña *Varios* de la LdM.](https://www.odoo.com/documentation/17.0/es/_images/misc-tab.png)

## Agregar subproductos a las listas de materiales[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/bill_configuration.html#add-by-products-to-boms "Enlazar permanentemente con este título")

Un _subproducto_ es un producto residual que se crea durante la producción además del producto principal de una lista de materiales. A diferencia del producto principal, en una LdM puede haber más de un subproducto.

Para agregar subproductos a una lista de materiales primero debe habilitar la función _Subproductos_ en Fabricación ‣ Configuración ‣ Ajustes. Vaya a la sección Operaciones y seleccione la casilla Subproductos para activarla.

![Función "Subproductos" en la página de ajustes.](https://www.odoo.com/documentation/17.0/es/_images/by-products.png)

Después de habilitar la función, agregue subproductos a una lista de materiales. Para ello, haga clic en la pestaña Subproductos, después en Agregar una línea y complete los campos Subproducto, Cantidad y Unidad de medida. Si así lo desea, especifique el campo Producido en la operación para el subproducto.

 Example

El subproducto `Compota` se crea en la operación `Triturar uvas` al producir `Vino tinto`.

![Mostrar subproducto de prueba en la LdM.](https://www.odoo.com/documentation/17.0/es/_images/add-by-product.png)