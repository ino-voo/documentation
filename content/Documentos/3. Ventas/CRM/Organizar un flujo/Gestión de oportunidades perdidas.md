No todas las oportunidades resultan en una venta. Para mantener el flujo actualizado debe identificar las oportunidades _perdidas_. Saber por qué se perdió una oportunidad puede ser muy util para futuras oportunidades.

## Marcar una oportunidad como perdida[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html#mark-an-opportunity-as-lost "Enlazar permanentemente con este título")

Para marcar una oportunidad como perdida, primero abra la aplicación CRM y haga clic en una tarjeta de kanban para abrir una oportunidad. De esta manera se mostrará el formulario de detalle de la oportunidad.

Después, haga clic en el botón Perdido, que se encuentra en la parte superior del formulario de detalles de la oportunidad.

![Imagen de lo botones en la parte superior del registro de una oportunidad con énfasis en el botón perdido.](https://www.odoo.com/documentation/17.0/es/_images/lost-opps-lost-button.png)

Esto abrirá la ventana emergente de Marcar como perdido. En el menú desplegable, seleccione un motivo de pérdida Motivo de pérdida existente. Si ninguno de los motivos que se muestran aplican para este caso puede crear uno, solo lo tiene que ingresar en el campo Motivo de pérdida y hacer clic en Crear.

Puede agregar notas o comentarios adicionales debajo del motivo de pérdida, en el campo designado Nota de cierre.

 Truco

Ni el campo Motivo de pérdida ni el campo Nota de cierre en la ventana emergente Marcar como perdido son obligatorios. Sin emgargo, es recomendable incluir esta información por motivos de trazabilidad, contabilidad y reportes.

Una vez que haya ingresado la información deseada en la ventana emergente marcar como perdido, haga clic en marcar como perdido.

![Ventana emergente donde poner el motivo de pérdida con motivos de ejemplo.](https://www.odoo.com/documentation/17.0/es/_images/lost-opps-lost-reason.png)

Después de hacer clic en Marcar como perdido, aparecerá un listón rojo de Perdido en la esquina superior derecha de la oportunidad.

![Una oportunidad perdida con el listón de perdido agregado.](https://www.odoo.com/documentation/17.0/es/_images/lost-banner.png)

 Nota

To mark an _inactive_ (archived) opportunity as lost, set the Probability field to `0` percent.

## Creación y edición de motivos de pérdida[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html#create-edit-lost-reasons "Enlazar permanentemente con este título")

Para crear un nuevo motivo de pérdida, o editar uno existente, vaya a la aplicación CRM ‣ Configuración ‣ Motivos de pérdida.

Para editar un motivo de pérdida existente:

1. Haga clic en el motivo que quiere editar para resaltarlo.
    
2. Edite el campo Descripción para cambiar el motivo de pérdida seleccionado
    
3. Una vez que haya terminado, haga clic en Guardar en la esquina superior izquierda.
    

Para crear un nuevo motivo de pérdida:

1. Haga clic en Nuevo en la esquina superior izquierda de la página Motivos de pérdida.
    
2. En la nueva línea en blanco, haga clic en el campo Description para escribir un nuevo motivo de pérdida.
    
3. Al terminar, haga clic en Guardar.
    

## Ver las oportunidades perdidas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html#view-lost-opportunities "Enlazar permanentemente con este título")

Para recuperar oportunidades perdidas en la aplicación _CRM_ de Odoo, abra la aplicación CRM y quédese en el tablero principal llamado Flujo. Una vez aquí, haga clic en la barra Buscar… en la parte superior de la página y quite todos los filtros predeterminados.

![Barra de búsqueda con el filtro de oportunidades perdidas resaltado.](https://www.odoo.com/documentation/17.0/es/_images/lost-opps-lost-filter.png)

Para abrir el menú desplegable Filtros haga clic en el icono 🔻(triángulo apuntando hacia abajo) que se encuentra a la derecha de la barra Buscar… para abrir un menú desplegable donde encontrará las opciones Filtros, Agrupar por y Favoritos con sus respectivas columnas.

En el menú desplegable Filtros seleccione la opción Perdido. Al hacerlo, en la página Flujo solo podrá ver los leads que se hayan marcado como perdidos.

### Acomodar las oportunidades por motivo de pérdida[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html#sort-opportunities-by-lost-reason "Enlazar permanentemente con este título")

Para filtrar oportunidades por una razón de pérdida específica haga clic en el icono 🔻(triángulo apuntando hacia abajo) ubicado a la derecha de la barra de búsqueda, esta acción abrirá el menú desplegable. Además del filtro Perdido, en la columna Filtros, haga clic en Agregar filtro personalizado para abrir la ventana emergente Agregar filtro personalizado.

En la ventana emergente Agregar filtro personalizado, haga clic en el primer campo y escriba `Motivo de pérdida` en la barra de búsqueda, o desplácese para buscarlo en la lista. A continuación, haga clic en el siguiente campo y seleccione = en el menú desplegable. Haga clic en el tercer campo y seleccione un motivo de pérdida en el menú desplegable. Por último, haga clic en Agregar.

![Barra de búsqueda con un filtro personalizado agregado para motivo de pérdida](https://www.odoo.com/documentation/17.0/es/_images/lost-opps-lost-custom-filter.png)

 Truco

Para ver los resultados de más de un motivo de pérdida, seleccione el operador está en en el segundo campo del filtro personalizado en la ventana emergente Añadir filtro personalizado. Al elegir este operador podrá seleccionar varios motivos de pérdida en el tercer campo.

![Ventana emergente de agregar un filtro personalizado con los motivos de pérdida seleccionados.](https://www.odoo.com/documentation/17.0/es/_images/multiple-lost-reasons.png)

## Restablecer las oportunidades perdidas[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html#restore-lost-opportunities "Enlazar permanentemente con este título")

Para restaurar una oportunidad perdida, abra la aplicación CRM para ver el tablero Flujo, o vaya a la aplicación CRM ‣ Ventas ‣ Mi flujo. Desde aquí, haga clic en el icono 🔻(triángulo apuntando hacia abajo) situado a la derecha de la barra de búsqueda para abrir el menú desplegable que contiene las columnas Filtros, Agrupar por y Favoritos.

En la columna Filtros seleccione Perdido. Al hacerlo se mostrarán todas las oportunidades perdidas en la página del flujo.

 Truco

Para ver todas las oportunidades de la base de datos, quite el filtro predeterminado Mi flujo de la barra de búsqueda.

Después, haga en el cuadro de kanban de la oportunidad perdida que desea restaurar para abrir el formulario de detalles de la oportunidad.

Desde el formulario de detalles de la oportunidad, haga clic en Restaurar en la esquina superior izquierda. De esta manera se quitará el listón rojo de Perdido del formulario y se habrá restaurado la oportunidad.

![Una oportunidad perdida con el botón Restaurar señalado.](https://www.odoo.com/documentation/17.0/es/_images/lost-opps-restore.png)

### Restaurar varias oportunidades al mismo tiempo[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html#restore-multiple-opportunities-at-once "Enlazar permanentemente con este título")

Para restaurar varias oportunidades al mismo tiempo, vaya al tablero principal de Flujo en la aplicación _CRM_, abra el menú desplegable de Filtros y seleccione la opción Perdido.

Después, seleccione la opción de vista de lista, representada por el icono de tres líneas ☰ (lista) en la esquina superior derecha. Al hacer esto, todos los leads del Flujo se mostrarán en forma de lista. Seleccione la casilla de verificación a la izquierda de cada oportunidad que quiere restaurar.

Ya que haya seleccionado los las oportunidades deseadas, haga clic en el menú desplegable de ⚙️ Acción en la parte superior de la página del Flujo. Desde el menú desplegable de ⚙️ Acción seleccione Desarchivar.

Al hacerlo, se eliminan las oportunidades seleccionadas de la página Flujo porque ya no se ajustan a los criterios del filtro Perdido. Elimine el filtro perdido de la barra de búsqueda para mostrar estas oportunidades recién restauradas.

![Botón de acción de la vista de lista donde se enfatiza la opción Desarchivar.](https://www.odoo.com/documentation/17.0/es/_images/lost-opps-unarchive.png)

## Gestionar leads perdidos[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html#manage-lost-leads "Enlazar permanentemente con este título")

Si tiene activos los _leads_ en la base de datos, puede marcarlos como _perdidos_ así como las oportunidades. Los leads usan los mismos [motivos de pérdida](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html#crm-lost-reasons) que las oportunidades.

 Nota

Para activar los leads vaya a CRM ‣ Configuración ‣ Ajustes y marque la casilla de verificación Leads y haga clic en Guardar. Esto hará que se agregue un menú de Leads en la barra de encabezado en la parte superior de la página.

### Marcar un lead como perdido[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html#mark-a-lead-as-lost "Enlazar permanentemente con este título")

Para marcar un lead como perdido, vaya a CRM ‣ Leads y seleccione un lead de la lista. De esta manera podrá ver el formulario de detalles del lead.

Después, haga clic en el botón Perdido que podrá encontrar en la parte superior del formulario del lead.

Esto abrirá la ventana emergente de Marcar como perdido. En el menú desplegable, seleccione un motivo de pérdida Motivo de pérdida existente. Si ninguno de los motivos que se muestran aplican para este caso puede crear uno, solo lo tiene que ingresar en el campo Motivo de pérdida y hacer clic en Crear.

Puede agregar notas o comentarios en donde dice nota de cierre, abajo del campo Nota de cierre.

Una vez que haya ingresado la información deseada en la ventana emergente marcar como perdido, haga clic en marcar como perdido.

### Restaurar leads perdidos[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html#restore-lost-leads "Enlazar permanentemente con este título")

Para restaurar un lead perdido vaya a CRM ‣ Leads. Desde aquí, haga clic en el icono 🔻(triángulo apuntando hacia abajo) situado a la derecha de la barra de búsqueda para abrir el menú desplegable que contiene las columnas Filtros, Agrupar por y Favoritos.

En la columna Filtros seleccione Perdido. Al hacerlo se mostrarán todos los leads perdidos en la página del leads.

Después, haga clic en el lead que desea restaurar para abrir el formulario de detalles del mismo.

Una vez en el formulario de detalles del lead, haga clic en el botón Restaurar que se enuentra en la esquina superior izquierda. Así se quitará el listón rojo de Perdido del formulario del lead y habrá restaurado la oportunidad.

### Restaurar varios leads al mismo tiempo[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html#restore-multiple-leads-at-once "Enlazar permanentemente con este título")

Para restaurar varios leads al mismo tiempo, vaya a CRM ‣ Leads, abra el menú desplegable Filtros y seleccione la opción Perdido. Seleccione la casilla de verificación a un lado de cada lead que desea restaurar.

Ya que haya seleccionado los leads deseados, haga clic en el menú desplegable de ⚙️ Acción en la parte superior de la página de Leads. Desde el menú desplegable de ⚙️ Acción seleccione Desarchivar.

Al hacerlo, se eliminan los leads seleccionados de la página Leads porque ya no se ajustan a los criterios del filtro Perdido. Elimine el filtro perdido de la barra de búsqueda para mostrar los leads recién restaurados.

 Ver también

[Análisis del flujo](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/performance/win_loss.html)