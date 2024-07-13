Los **activos no circulantes**, también conocidos como **activos a largo plazo**, son inversiones que se esperan realizar después de un año. Se capitalizan en lugar de gastarse y aparecen en el balance general de la empresa. Dependiendo de su naturaleza, pueden sufrir una **depreciación**.

**Los activos fijos** son un tipo de activos no circulantes e incluyen los bienes adquiridos por sus aspectos productivos, como edificios, vehículos, equipos, terrenos y software.

Por ejemplo, supongamos que compramos un auto por $27,000. Planeamos amortizarlo a lo largo de cinco años, y después lo venderemos por $7,000. Utilizando el método de depreciación lineal, se cargan $4,000 cada año como **gastos de depreciación**. Después de cinco años, el importe de la **depreciación acumulada** que figura en el balance es de $20,000 dólares, lo que nos deja un total de $7,000 de **valor no depreciable**, o valor de salvamento.

La aplicación Contabilidad de Odoo gestiona la depreciación mediante la creación de todos los asientos de depreciación automáticamente en _modo de borrador_. Luego se contabilizan de forma periódica.

Odoo admite los siguientes **métodos de depreciación**:

- Línea recta
    
- En declive
    
- Declive y luego línea recta
    

 Nota

El servidor comprueba una vez al día si se debe publicar un asiento. Pueden pasar hasta 24 horas antes de que se refleje el cambio de _borrador_ a _registrado_.

## Prerrequisitos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#prerequisites "Enlazar permanentemente con este título")

Se deben contabilizar estas operaciones en una **cuenta de activos** y no en la cuenta de gastos predeterminada.

### Configurar una cuenta de activos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#configure-an-assets-account "Enlazar permanentemente con este título")

Para configurar su cuenta en el **Plan de cuentas**, vaya a Contabilidad ‣ Configuración ‣ Plan de cuentas, haga clic en _Crear_, y llene el formulario.

![Configuración de una cuenta de activos en la aplicación Contabilidad de Odoo](https://www.odoo.com/documentation/17.0/es/_images/assets01.png)

 Nota

El tipo de esta cuenta debe ser _Activo fijo_ o _Activo no circulante_.

### Contabilizar un gasto en la cuenta correcta[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#post-an-expense-to-the-right-account "Enlazar permanentemente con este título")

#### Seleccionar la cuenta en un borrador de factura[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#select-the-account-on-a-draft-bill "Enlazar permanentemente con este título")

En un borrador de factura, seleccione la cuenta correcta para todos los activos que está comprando.

![Selección de una cuenta de activos en una factura de proveedor en estado de borrador en la aplicación Contabilidad de Odoo](https://www.odoo.com/documentation/17.0/es/_images/assets02.png)

#### Elija una cuenta de gastos diferente para productos específicos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#choose-a-different-expense-account-for-specific-products "Enlazar permanentemente con este título")

Comience a editar el producto, vaya a la pestaña de _Contabilidad_, seleccione la **Cuenta de gastos** correcta y guarde.

![Cambio de la cuenta de activos para un producto en Odoo](https://www.odoo.com/documentation/17.0/es/_images/assets03.png)

 Truco

Es posible [automatizar la creación de asientos de activos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#assets-automation) para estos productos.

#### Modificar la cuenta de un apunte contable registrado[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#change-the-account-of-a-posted-journal-item "Enlazar permanentemente con este título")

Para hacer esto, abra su diario de compras en Contabilidad ‣ Contabilidad ‣ Compras, seleccione el apunte contable que desea modificar, haga clic en la cuenta y seleccione la correcta.

![Modificación de la cuenta de un apunte contable publicado en la aplicación Contabilidad de Odoo](https://www.odoo.com/documentation/17.0/es/_images/assets04.png)

## Asientos contables de activos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#assets-entries "Enlazar permanentemente con este título")

### Crear un nuevo asiento[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#create-a-new-entry "Enlazar permanentemente con este título")

Un **asiento contable de activo** genera automáticamente todos los asientos en _modo de borrador_. Después se contabilizan uno por uno en su debido momento.

Para crear un nuevo asiento, vaya a Contabilidad ‣ Contabilidad ‣ Activos, haga clic en _Crear_ y complete el formulario.

Haga clic en **seleccionar compras relacionadas** para vincular un apunte contable existente a este nuevo asiento. Algunos campos se completarán de forma automática y el apunte contable aparecerá en la pestaña **compras relacionadas**.

![Asiento de activos en la aplicación Contabilidad de Odoo](https://www.odoo.com/documentation/17.0/es/_images/assets05.png)

Una vez hecho esto, puede hacer clic en _Calcular depreciación_ (al lado del botón _Confirmar_) para generar todos los valores de la **tabla de depreciación**. Esta tabla le muestra todos los asientos que Odoo registrará para depreciar su activo, y la fecha.

![Tabla de depreciación en la aplicación Contabilidad de Odoo](https://www.odoo.com/documentation/17.0/es/_images/assets06.png)

#### ¿Qué significa «Prorata Temporis»?[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#what-does-prorata-temporis-mean "Enlazar permanentemente con este título")

La función **Prorata Temporis** es útil para depreciar sus activos con la mayor precisión posible.

Con esta función, el primer asiento en la tabla de depreciación se calcula en función del tiempo que queda entre la _fecha de prorrateo_ y la _fecha de primera depreciación_, y no en función del tiempo predeterminado entre depreciaciones.

Por ejemplo, la tabla de depreciación anterior tiene su primera depreciación con un importe de $241.10 en lugar de $4,000.00. Por lo tanto, el último asiento también es menor y tiene un importe de $3,758.90.

#### ¿Cuáles son los diferentes métodos de depreciación?[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#what-are-the-different-depreciation-methods "Enlazar permanentemente con este título")

El **método de depreciación en línea recta** divide el valor depreciable inicial entre el número de depreciaciones planeadas. Todos los asientos de depreciación tienen el mismo importe.

El **Método de depreciación en declive** multiplica el valor depreciable por el **factor en declive** para cada asiento. Cada asiento de depreciación tiene un importe inferior al del asiento anterior. El último asiento de depreciación no utiliza el factor en declive, sino que tiene un importe correspondiente al balance del valor depreciable de modo que llegue a $0 al final de la duración indicada.

El **Método de depreciación en declive y luego en línea recta** utiliza el método en declive, pero con una depreciación mínima igual a la del método de línea recta. Este método asegura una depreciación rápida al principio, seguida de una constante después.

### Activos del diario de compras[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#assets-from-the-purchases-journal "Enlazar permanentemente con este título")

Puede crear un asiento de activo desde un apunte específico en su **diario de compras**.

Para hacerlo, abra su diario de compras en Contabilidad ‣ Contabilidad ‣ Compras, y seleccione el apunte contable que desea registrar como activo. Asegúrese de que se registre en la cuenta correcta (vea: [Modificar la cuenta de un apunte contable registrado](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#journal-assets-account)).

Posteriormente, haga clic en _Acción_, seleccione **Crear activo**, y complete el formulario de la misma manera que lo haría para [crear un nuevo asiento](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#create-assets-entry).

![Crear un asiento de activo desde un apunte contable en la aplicación Contabilidad de Odoo](https://www.odoo.com/documentation/17.0/es/_images/assets07.png)

## Modificación de un activo[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#modification-of-an-asset "Enlazar permanentemente con este título")

Puede modificar los valores de un activo para aumentar o disminuir su valor.

Para hacerlo, abra el activo que desea modificar y haga clic en _Modificar depreciación_. A continuación, complete el formulario con los nuevos valores de depreciación y haga clic en _Modificar_.

Una **disminución de valor** registra un nuevo asiento para la **disminución de valor** y modifica todos los asientos futuros _no registrados_ que aparecen en el tablero de depreciación.

Para un **aumento de valor** es necesario completar campos adicionales relacionados con los movimientos de la cuenta, además de crear un nuevo asiento de activo con el **aumento de valor**. Se puede acceder al asiento de activo con **aumento de valor** a través de un botón inteligente.

![Botón inteligente de incremento bruto](https://www.odoo.com/documentation/17.0/es/_images/assets08.png)

## Eliminar activos fijos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#disposal-of-fixed-assets "Enlazar permanentemente con este título")

**Vender** un activo o **eliminarlo** implica que se debe retirar del balance general.

Para ello, abra el activo del que desea deshacerse, haga clic en _Vender o eliminar_ y complete el formulario.

![Disposición de bienes](https://www.odoo.com/documentation/17.0/es/_images/assets09.png)

La contabilidad de Odoo genera entonces todos los asientos necesarios para deshacerse del activo, incluyendo la ganancia o pérdida en la venta, que se basa en la diferencia entre el valor contable del activo en el momento de la venta y el importe en el que se vende.

 Nota

Para registrar la venta de un activo, primero debe registrar la factura de cliente relacionada para poder vincularla con la venta del activo.

## Modelos de activos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#assets-models "Enlazar permanentemente con este título")

Puede crear **Modelos de activos** para crear los asientos de activos de forma más rápida. Esto resulta especialmente útil si compra de forma recurrente el mismo tipo de activos.

Para crear un modelo, vaya a Contabilidad ‣ Configuración ‣ Modelos de activos, haga clic en _Crear_, y complete el formulario de la misma manera que lo haría para crear un nuevo asiento.

 Truco

También puede convertir un _asiento confirmado de activo_ en un modelo abriéndolo desde Contabilidad ‣ Contabilidad ‣ Activos y luego, haciendo clic en el botón _Guardar modelo_.

### Aplicar un modelo de activos a un nuevo asiento[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#apply-an-asset-model-to-a-new-entry "Enlazar permanentemente con este título")

Cuando cree un nuevo asiento de activo, complete la **Cuenta de activo fijo** con la cuenta de activo correcta.

En la parte superior del formulario aparecen nuevos botones con todos los modelos vinculados a esa cuenta. Al hacer clic en un modelo, se completa el formulario según dicho modelo

![Botón de activos](https://www.odoo.com/documentation/17.0/es/_images/assets10.png)

## Automatizar activos[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#automate-the-assets "Enlazar permanentemente con este título")

Cuando se crea o edita una cuenta cuyo tipo es _activo no corriente_ o _activo fijo_, se puede configurar para que se creen activos correspondientes a los gastos que se abonan en dicha cuenta de forma automática.

Hay tres opciones para el campo **automatizar activos**:

1. **No:** es el valor predeterminado. No pasa nada.
    
2. **Crear en borrador:** cuando se registra una transacción en la cuenta se crea un borrador de _asiento de activo_, pero no se valida. Usted debe completar el formulario correspondiente en Contabilidad‣ Contabilidad ‣ Activos.
    
3. **Crear y validar:** también debe seleccionar un modelo de activos (ver: [Modelos de activos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#assets-models)). Cada vez que se registra una operación en la cuenta, se crea un _asiento de activo_ que se valida inmediatamente.
    

![Automatizar activos en Contabilidad de Odoo](https://www.odoo.com/documentation/17.0/es/_images/assets11.png)

 Truco

Puede, por ejemplo, seleccionar esta cuenta como la **cuenta de gastos** predeterminada de un producto para automatizar totalmente su compra. (ver: [Elija una cuenta de gastos diferente para productos específicos](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills/assets.html#product-assets-account)).

 Ver también

- [Plan contable](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/get_started/chart_of_accounts.html)