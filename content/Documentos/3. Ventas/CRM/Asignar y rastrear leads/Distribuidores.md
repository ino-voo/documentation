En la aplicación _CRM_ de Odoo es posible enviar los leads a distribuidores (o contactos), además de que se pueden asignar de forma manual o automática según el _nivel_ designado de los distribuidores y su ubicación.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/resellers.html#configuration "Enlazar permanentemente con este título")

Primero debe instalar el módulo _Distribuidores_ para utilizar las funciones de distribuidor. Vaya a Aplicaciones, elimine el filtro Aplicaciones de la barra de búsqueda y luego busque `Distribuidores`.

![El módulo de distribuidores en Odoo.](https://www.odoo.com/documentation/17.0/es/_images/resellers-module.png)

Haga clic en el botón Activar de la tarjeta del módulo Distribuidores. Esta acción instala el módulo y vuelve al tablero principal de Odoo.

Vaya a CRM después de instalar el módulo. En el menú Configuración hay una nueva sección titulada Distribuidores con otras tres opciones: Niveles de contacto, Activaciones de contacto y Planes de comisión.

## Niveles de contacto[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/resellers.html#partner-levels "Enlazar permanentemente con este título")

Los _niveles_ de contacto se utilizan para diferenciar a los distribuidores. Para ver estos niveles, vaya a CRM ‣ Configuración ‣ Distribuidores: Niveles de contacto.

Hay tres niveles predeterminados en la página de Niveles de contactos:

- Dorado
    
- Plateado
    
- Bronce
    

Es posible agregar tantos niveles como sea necesario al hacer clic en Nuevo y completar el formulario correspondiente.

También es posible editar y renombrar los niveles existentes si así lo desea. Para modificar un nivel, selecciónelo de la lista y haga los cambios deseados en la página del formulario de nivel que aparece.

El nivel se utiliza para decidir la probabilidad de asignar una oportunidad o lead a un contacto. En el formulario de nivel deberá asignar un valor numérico (mayor que cero) al campo Nivel de peso y no se asignan oportunidades en caso de que sea cero.

 Truco

Este _nivel_ puede asignarse en cada registro de contacto. El peso asignado sobrescribe el peso predeterminado asignado en el formulario correspondiente.

## Activaciones de contactos[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/resellers.html#partner-activations "Enlazar permanentemente con este título")

Las _activaciones_ de contactos se utilizan para identificar su estado y estas se asignan en el registro de cada contacto. Puede utilizarlas para agrupar o filtrar el reporte de _análisis de asociación_ (CRM ‣ Reportes ‣ Asociaciones).

Vaya a CRM ‣ Configuración ‣ Activaciones de contacto para ver los niveles.

En la aplicación _CRM_ se crean tres tipos de activación de forma predeterminada:

- Totalmente operativo
    
- En escalamiento
    
- Primer contacto
    

Es posible agregar nuevas activaciones de contacto según sea necesario al hacer clic en el botón Nuevo, después escriba el nombre en la nueva línea que aparece y seleccione el estado deseado en la columna Activo.

También es posible editar y renombrar las activaciones de contacto existentes en caso de que así lo desee. Para renombrar un estado, haga clic en el campo Nombre del nivel correspondiente y escriba el nuevo nombre.

Para cambiar el estado de una activación, haga clic en el botón de la columna Activo a la posición _inactivo_.

![La lista predeterminada de activaciones de contactos en la aplicación CRM.](https://www.odoo.com/documentation/17.0/es/_images/activations-toggle.png)

La lista predeterminada de activaciones de contactos en la aplicación CRM. El botón de Primer contacto está inactivo y los demás están activos.[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/resellers.html#id1 "Enlace permanente a esta imagen")

## Asignaciones de contacto[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/resellers.html#partner-assignments "Enlazar permanentemente con este título")

Después de configurar los [niveles](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/resellers.html#crm-partner-levels) y [activaciones](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/resellers.html#crm-partner-activations) de contactos.

Vaya a CRM ‣ Ventas ‣ Clientes para actualizar el registro de un contacto. Haga clic en la tarjeta de kanban correspondiente para abrir el registro del cliente.

Haga clic en la pestaña Asignación de contacto del registro del cliente.

Haga clic en el campo Nivel del contacto y seleccione una opción del menú desplegable para asignar un nivel y, si lo desea, después haga clic en el campo Activación para seleccionar un tipo de activación de contacto en la lista desplegable. Haga clic en el campo :guilabel:l`Nivel de peso` para asignar uno distinto en caso de que sea necesario.

## Publicar contactos[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/resellers.html#publish-partners "Enlazar permanentemente con este título")

Si las aplicaciones _Sitio web_ y _Distribuidores_ están instaladas se creará una nueva página web (`/partners`) con una lista de todos los contactos activos de la aplicación _CRM_.

Regrese a CRM ‣ Ventas ‣ Clientes y haga clic en la tarjeta de kanban de un contacto. Una vez en el formulario correspondiente, haga clic en el botón inteligente Ir al sitio web que se encuentra en la parte superior de la página para abrir la página web del contacto.

Después haga clic en Editar en la esquina superior derecha de la página web del contacto y use los [bloques de creación](https://www.odoo.com/documentation/17.0/es/applications/websites/website/web_design/building_blocks.html) para agregar cualquier elemento de diseño o información adicional.

 Truco

Sería útil agregar un resumen de la empresa a esta página.

Haga clic en Guardar después de realizar los cambios necesarios en la página. Presione el botón Sin publicar ubicado en la parte superior de la página para que cambie a Publicado en caso de que sea necesario.

Repita estos pasos para todos los contactos.

![Un ejemplo de la página de contactos, los disponibles aparecen por nivel y ubicación.](https://www.odoo.com/documentation/17.0/es/_images/partners-webpage.png)