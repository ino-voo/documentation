En algunos casos, no es posible producir la cantidad total de una orden de fabricación de forma inmediata. Cuando esto ocurre, la aplicación _Fabricación_ de Odoo permite fabricar una parte del pedido y crea una _orden parcial_ para la cantidad restante.

Cuando crea una orden parcial en la aplicación _Fabricación_, la orden de fabricación original se divide en dos. La etiqueta de referencia para cada orden es la que se utiliza en la orden original, seguida de un guion y un número adicional para indicar que se trata de una orden parcial.

 Example

Una empresa crea una orden de fabricación con la etiqueta de referencia _WH/MO/00175_ para 10 unidades del _producto X_. Después de comenzar a trabajar en la orden de fabricación, el empleado que trabaja en la línea de producción se da cuenta de que solo hay suficientes componentes en sus existencias para producir cinco unidades del producto.

En lugar de esperar las existencias adicionales de los componentes, fabrica cinco unidades y crea una orden parcial para los cinco productos restantes. Esto divide la orden de fabricación en dos órdenes separadas, _WH/MO/00175-001_ y _WH/MO/00175-002_.

La orden _001_ incluye las cinco unidades fabricadas y se marca inmediatamente como Hecha. La orden _002_ incluye las cinco unidades que todavía deben fabricarse y está marcada como En progreso. Una vez que los componentes restantes están disponibles, el empleado vuelve a la orden _002_ y fabrica las unidades restantes antes de cerrar la orden.

## Crear una orden parcial de fabricación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/manufacturing_backorders.html#create-a-manufacturing-backorder "Enlazar permanentemente con este título")

Para crear una orden parcial para una parte de una orden de fabricación, vaya a Fabricación ‣ Operaciones ‣ Ordenes de fabricación. Seleccione una orden de fabricación con una cantidad de dos o más o haga clic en Nuevo para crear una.

Si está creando una nueva orden de fabricación, seleccione un producto en el menú desplegable e ingrese una cantidad de dos o más en el campo correspondiente. Por último, confirme la orden.

Después de fabricar la cantidad que se está produciendo de forma inmediata, ingrese ese número en el campo cantidad en la parte superior de la orden de fabricación.

![El campo de cantidad en una orden de fabricación.](https://www.odoo.com/documentation/17.0/es/_images/quantity-field.png)

Después, haga clic en Validar y aparecerá una ventana emergente con el mensaje Produjo menos que la demanda inicial, desde allí puede crear una orden parcial. Haga clic en Crear orden parcial para dividir la orden de fabricación en dos órdenes separadas con las etiquetas de referencia _WH/MO/XXXXX-001_ y _WH/MO/XXXXX-002_.

![El botón Crear orden parcial en la ventana emergente "Produjo menos que la demanda inicial".](https://www.odoo.com/documentation/17.0/es/_images/create-backorder-button.png)

La orden _001_ incluye los artículos que se fabricaron y se cierra de inmediato, mientras que la orden _002_ es la orden parcial que incluye los artículos que aún no se han fabricado, además permanece abierta que pueda completarse después.

Una vez que pueda fabricar las unidades restantes, aya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y seleccione la orden parcial de fabricación. Si todas las unidades restantes se fabrican de inmediato, solo haga clic en Validar para cerrar la orden.

Si solo algunas de las unidades restantes se fabrican en ese momento, cree otra orden parcial para las otras. Debe seguir los pasos detallados en esta sección.

## Crear una orden parcial en Taller[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/manufacturing_backorders.html#create-a-backorder-in-shop-floor "Enlazar permanentemente con este título")

También puede crear ordenes parciales de fabricación desde el módulo _Taller_.

 Nota

Para utilizar el módulo _Taller_ debe habilitar la función _Órdenes de trabajo_. Vaya a Fabricación ‣ Configuración ‣ Ajustes, seleccione la casilla Órdenes de trabajo y haga clic en Guardar.

Para crear una orden parcial desde el módulo _Taller_, primero vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación. Seleccione una orden de fabricación para varias unidades de un producto del que deba crear una orden pendiente.

En la orden de fabricación, seleccione la pestaña Órdenes de trabajo y haga clic en el botón Abrir orden de trabajo (icono de enlace externo) ubicado en la línea de la orden de trabajo a procesar. Aparecerá la ventana emergente Órdenes de trabajo, allí haga clic en el botón Abrir Taller para abrir el módulo _Taller_.

Cuando accede desde una orden de trabajo específica, el módulo _Taller_ se abre en la página del centro de trabajo donde está configurado que se procesará la orden. Además, separa la tarjeta de la orden de trabajo para que no aparezcan otras tarjetas.

Complete los pasos en la tarjeta de la orden de trabajo hasta que llegue al paso Registrar producción, luego haga clic allí para abrir la ventana emergente Registrar producción.

 Importante

No haga clic en el botón Número de unidades ubicado en el lado derecho del paso, pues eso registrará en automático la cantidad completa de unidades como producidas.

En la ventana emergente Registrar producción escriba el número de unidades producidas en el campo Cantidad. Asegúrese de que el número que registra sea _menor_ que el número de unidades ubicadas a la derecha del campo y después haga clic en Validar.

![La ventana emergente Registrar producción en el módulo Taller.](https://www.odoo.com/documentation/17.0/es/_images/register-production1.png)

La ventana emergente desaparece y el botón Número de unidades en la tarjeta de la orden de trabajo se actualiza para mostrar el número de unidades producidas. Este aparece como una fracción del número de unidades para las cuales se creó la orden de fabricación en un principio.

Después, haga clic en el botón Marcar como hecho ubicado en la esquina inferior derecha de la tarjeta de la orden de trabajo. La tarjeta de la orden de trabajo comenzará a desaparecer. Una vez que haya desaparecido por completo, aparecerá una nueva tarjeta de orden de trabajo que llevará como título el número de referencia original de la orden de fabricación seguido de la etiqueta `-002`.

Este nuevo número de referencia representa la orden parcial de fabricación. El número de referencia original de la orden de fabricación ahora aparece con la etiqueta `-001` al final para distinguirla de la orden parcial.

Si la orden de fabricación original no tiene órdenes de trabajo pendientes, puede cerrarla si selecciona el filtro Todos ubicado en la parte superior del módulo _Taller_ y después hace clic en Cerrar producción en la parte inferior de la tarjeta correspondiente.

Si la orden de fabricación original tiene órdenes de trabajo pendientes que deben completarse antes de que pueda cerrarse, las tarjetas para estas órdenes de trabajo aparecerán en las páginas de _Taller_ para los centros de trabajo donde están configuradas para llevarse a cabo. Se pueden procesar como de costumbre y es posible crear órdenes parciales adicionales a partir de sus tarjetas de orden de trabajo con las instrucciones que se describen en esta sección.

Una vez que la orden de trabajo actual para la orden parcial de fabricación esté lista para ser procesada, también puede completarla como de costumbre y puede crear una orden parcial adicional desde su tarjeta de orden de trabajo con las instrucciones que se describen en esta sección.

Después de que completó la orden de trabajo final de la orden parcial de fabricación podrá cerrar la orden de fabricación si hace clic en el botón Cerrar producción ubicado en la parte inferior de la tarjeta de la orden de trabajo.