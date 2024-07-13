La aplicación _Alquiler_ de Odoo ofrece soluciones muy completas para configurar y gestionar alquileres.

Puede enviar cotizaciones, confirmar órdenes, programar alquileres, registrar cuándo se recogen o devuelven los productos y facturar a los clientes desde una sola plataforma.

 Ver también

- [Alquiler de Odoo: página de producto](https://www.odoo.com/app/rental)
    
- [Tutoriales de Odoo: Alquiler](https://www.odoo.com/slides/rental-48)
    

## Tablero[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#dashboard "Enlazar permanentemente con este título")

Al abrir la aplicación _Alquiler_ aparece el tablero con las órdenes de alquiler.

![Ejemplo del tablero con las órdenes de alquiler disponible en la aplicación Alquiler de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/rental-orders-dashboard.png)

Todos los alquileres son visibles desde la vista kanban predeterminada. Cada tarjeta de alquiler muestra el nombre del cliente, el precio del alquiler, el número de la orden de venta relacionada y su estado.

 Nota

Las tarjetas de alquiler en el kanban que **no** muestran un estado de alquiler indican que estos alquileres tienen cotizaciones confirmadas, pero que aún no los recogen.

En la barra lateral izquierda se encuentra el estado del alquiler de cada uno y abajo se puede consultar su estado de la factura. Al hacer clic en cualquier opción en la barra lateral izquierda se filtran los alquileres que aparecen en el tablero.

## Ajustes[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#settings "Enlazar permanentemente con este título")

Vaya a la aplicación Alquiler ‣ Configuración ‣ Ajustes para configurar costos adicionales por retrasos, la disponibilidad de los artículos o el tiempo mínimo de alquiler.

![Visualización de la apariencia de la página de ajustes en la aplicación Alquiler de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/rental-settings.png)

En la sección Alquiler están presentes las opciones para configurar los costos predeterminados por retraso y el tiempo predeterminado de espera. También existe la opción de activar las transferencias de alquiler y los documentos digitales.

- Los costos predeterminados por retraso son costos adicionales por realizar devoluciones tardías.
    
- El tiempo predeterminado de espera representa el tiempo mínimo que debe pasar entre dos alquileres.
    
- Las transferencias de alquiler indican que las entregas y recepciones de existencias se pueden utilizar para las órdenes de alquiler.
    
- Los documentos digitales permiten que los usuarios suban documentos para que los clientes los firmen antes de
    
    confirmar su alquiler.
    

En la sección Alquilar en línea están presentes las opciones para configurar un periodo mínimo de alquiler y designar los días sin disponibilidad, es decir, los días durante los cuales no es posible recolectar ni devolver productos.

## Productos para alquiler[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#rental-products "Enlazar permanentemente con este título")

Vaya a la aplicación Alquiler ‣ Productos para visualizar todos los productos en la base de datos que se pueden alquilar. El filtro Se puede rentar aparece de forma predeterminada en la barra de búsqueda.

Cada tarjeta kanban de producto muestra el nombre del producto, el precio de alquiler y la imagen del producto (en caso de que tenga una).

## Precios de alquiler[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#id1 "Enlazar permanentemente con este título")

Para ajustar el precio de alquiler de un producto vaya a la página Productos en la aplicación _Alquiler_ y luego seleccione el producto correspondiente o haga clic en Nuevo para crear uno.

Asegúrese de que la casilla Se puede rentar esté seleccionada en el formulario del producto y luego abra la pestaña Precios de alquiler.

![Visualización de la apariencia de la página de ajustes en la aplicación Alquiler de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/rental-prices-tab.png)

 Nota

Si crea un producto de este tipo fuera de la aplicación _Alquiler_ solo asegúrese de que la casilla Se puede rentar esté seleccionada en el formulario correspondiente. Esta casilla está seleccionada de forma predeterminada cuando crea un producto desde la aplicación _Alquiler_.

### Precio[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#pricing "Enlazar permanentemente con este título")

Establezca precios y periodos de alquiler personalizados para el producto en la sección Precios de la pestaña Precios de alquiler.

Para agregar los precios de un alquiler haga clic en Agregar un precio. Luego, elija un _periodo de precios_ (la unidad de duración del alquiler) en la columna Periodo o cree uno nuevo, para esto debe escribir el nombre correspondiente y hacer clic en Crear.

Decida si desea aplicar este precio de alquiler personalizado a una lista de precios específica.

Por último, escriba el precio deseado para ese periodo específico.

 Nota

No hay límite en la cantidad de líneas de precios que puede agregar. Por lo general se usan varias opciones de precios para productos de alquiler con la finalidad de ofrecer descuentos a los clientes que alquilan durante más tiempo.

Para eliminar cualquier opción de precio de alquiler haga clic en el icono de 🗑️ (papelera) y esa fila se borrará.

### Reservas[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#reservations "Enlazar permanentemente con este título")

En la sección Reservaciones de la pestaña Precios de alquiler hay una opción para configurar multas adicionales por cada hora o día adicional que el cliente tarde en devolver un alquiler.

También está disponible la opción de tiempo de seguridad representada con horas. Esta opción hace que el producto no esté disponible durante cierto tiempo entre dos órdenes de alquiler y puede ser útil si es necesario proporcionar mantenimiento o limpieza.

### Cálculo de precios[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#price-computing "Enlazar permanentemente con este título")

Odoo siempre usa dos reglas para calcular el precio de un producto cuando crea una orden de alquiler:

1. Solo se utiliza una línea de precio.
    
2. Se selecciona la línea más barata.
    

 Exercise

Considere la siguiente configuración de precio de alquiler para un producto:

- 1 día: $100
    
- 3 días: $250
    
- 1 semana: $500
    

Un cliente desea rentar este producto por ocho días. ¿Qué precio pagará?

Después de que se crea una orden, Odoo selecciona la segunda línea porque es la opción más barata. El cliente tiene que pagar “3 días” tres veces para cubrir los ocho días del alquiler, lo que da como resultado $750.

## Órdenes de alquiler[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#rental-orders "Enlazar permanentemente con este título")

Para crear una orden de este tipo en la aplicación _Alquiler_, vaya a Alquiler ‣ Órdenes ‣ Órdenes y haga clic en Nuevo. Esta acción abrirá un formulario vacío para una orden de alquiler que deberá completar.

![Ejemplo de una orden de alquiler completado disponible en la aplicación Alquiler de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/rental-order.png)

Primero agregue un cliente y luego configure la duración deseada del alquiler en el campo Periodo de alquiler.

Para ajustar la duración del alquiler haga clic en la primera fecha en el campo Periodo de alquiler y seleccione el rango de fechas que corresponde a la duración del alquiler en el formulario de calendario emergente.

![Ejemplo de una ventana de calendario emergente para un periodo de alquiler en la aplicación Alquiler de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/rental-period-field-popup.png)

Una vez que haya completado el paso anterior haga clic en Aplicar en el formulario de calendario emergente. Después de eso, el formulario desaparecerá y el periodo de tiempo que seleccionó para el alquiler aparecerá en el campo Duración.

Ahora agregue un producto de alquiler en la pestaña Líneas de la orden. Haga clic en Agregar un producto y seleccione el producto de alquiler que desea agregar al formulario.

 Nota

Si se agrega un producto de alquiler _antes_ de configurar el campo Periodo de alquiler correctamente, el usuario _todavía_ puede ajustar este campo según sea necesario.

Solo seleccione el rango de fechas correspondiente a la duración del alquiler y luego haga clic en Actualizar precios de alquiler en el campo Duración.

![La opción Actualizar precios de alquiler que aparece en la aplicación Alquiler de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/rental-update-rental-prices.png)

Después de realizar esta acción aparecerá una ventana emergente de confirmación. Si todo está correcto, haga clic en De acuerdo y Odoo volverá a calcular el precio del alquiler como corresponde.

Una vez que haya ingresado toda la información en el formulario de la orden de alquiler haga clic en el botón Enviar por correo electrónico para enviar la cotización al cliente o en el botón Confirmar para confirmar la orden.

## Firma del cliente[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#customer-signature "Enlazar permanentemente con este título")

El botón Firmar documentos aparecerá al confirmar una orden de alquiler. Esto ofrece la posibilidad de solicitarle al cliente que firme un contrato de alquiler con los detalles del acuerdo entre la empresa y el cliente _antes_ de que recojan vayan por sus productos de alquiler.

Estos documentos pueden garantizar que todo se devolverá a tiempo y en su estado original.

 Importante

El botón o la opción Firmar documentos solo aparecerá si la función Documentos digitales está habilitada en los ajustes de la aplicación _Alquiler_. Para hacerlo, vaya a :la menuselection:`aplicación Alquiler --> Configuración --> Ajustes`, active Documentos digitales y haga clic en Guardar.

 Nota

Esta función también necesita de la aplicación [Firma electrónica](https://www.odoo.com/documentation/17.0/es/applications/productivity/sign.html). Si es necesario, Odoo la instalará de forma automática después de activar la función Documentos digitales.

Para solicitar la firma del cliente en un contrato de alquiler, seleccione una orden de alquiler confirmada y haga clic en el botón Firmar documentos. Esta acción abrirá la ventana emergente Firmar documentos.

![La ventana emergente Firmar documentos que aparece en la aplicación Alquiler de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/sign-documents-popup.png)

Desde allí seleccione el documento deseado en el campo Plantilla de documento. Haga clic en Firmar documento para abrir una ventana emergente de Nueva solicitud de firma.

![La ventana emergente Nueva solicitud de firma que aparece en la aplicación Alquiler de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/new-signature-request-form.png)

Luego de confirmar la información en el formulario de Nueva solicitud de firma, haga clic en Firmar ahora para iniciar el proceso de firma.

Aparecerá una página separada con el documento a firmar. El cliente puede acceder a ella a través de su portal.

Odoo guía a los clientes a través del proceso de firma con indicadores claros en los que puede hacer clic y les permite crear firmas electrónicas para completar el formulario con rapidez.

![La ventana emergente Adoptar su firma que aparece en la aplicación Alquiler de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/adopt-signature-popup.png)

Una vez que el documento esté firmado y completado, haga clic en el botón Validar y enviar el documento completado que se encuentra ubicado en la parte inferior.

![El botón Validar y enviar el documento completado en la aplicación Alquiler de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/validate-send-doc-button.png)

Al hacer clic en el botón Validar y enviar el documento completado, Odoo proporciona la opción de descargar el documento firmado para propósitos de almacenamiento, en caso de que sea necesario.

 Ver también

[Tutoriales de Odoo: Firma electrónica](https://www.odoo.com/slides/sign-61)

## Recolección de productos[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#pickup-products "Enlazar permanentemente con este título")

Vaya a la orden de alquiler correspondiente cuando un cliente vaya por los productos, haga clic en el botón Recolección y luego en Validar en el formulario emergente Validar una recolección.

Esto hará que aparezca un mensaje con el estado Recolección en la orden de alquiler.

## Devolución de productos[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#return-products "Enlazar permanentemente con este título")

Cuando un cliente devuelva los productos vaya a la orden de alquiler correspondiente, haga clic en el botón Devolver y valide la devolución. Haga clic en Validar en la ventana emergente Validar una devolución.

Esto hará que aparezca un mensaje con el estado Devuelto en la orden de alquiler.

## Imprimir recibos de recolección y devolución[](https://www.odoo.com/documentation/17.0/es/applications/sales/rental.html#print-pickup-and-return-receipts "Enlazar permanentemente con este título")

Es posible imprimir recibos de recolección y devolución para los clientes al momento de que vayan a recolectar o devolver los productos que alquilaron.

Para imprimir recibos de recolección o devolución vaya a la orden de alquiler correspondiente y haga clic en el icono ⚙️ (engranaje) para abrir un menú desplegable.

![La opción de impresión del recibo de recolección y devolución en la aplicación Alquiler de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/print-pickup-return-receipt.png)

En este menú desplegable coloque el cursor sobre la opción Imprimir para abrir otro menú y luego seleccione Recibo de recolección y devolución.

Odoo genera y descarga un PDF que incluye toda la información detallada sobre el estado actual de los elementos alquilados.