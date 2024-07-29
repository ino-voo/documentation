En la aplicación _Calidad_ de Odoo, las _alertas de calidad_ se utilizan para notificar a los equipos de calidad sobre productos defectuosos u otros problemas. Es posible crear alertas de calidad desde una orden de fabricación o inventario, una orden de trabajo en el módulo _Taller_ o desde la aplicación _Calidad_.

## Crear alertas de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_alerts.html#create-quality-alerts "Enlazar permanentemente con este título")

Hay varias maneras de crear una nueva alerta de calidad:

- **Desde la aplicación Calidad.** Vaya a Calidad ‣ Control de calidad ‣ Alertas de calidad y haga clic en Nuevo para abrir un formulario de alerta de calidad.
    
- Vaya a Fabricación ‣ Operaciones ‣ Órdenes de fabricación y seleccione una. Haga clic en el botón Alerta de calidad ubicado en la parte superior de la orden de fabricación para abrir el formulario de alerta de calidad en una página nueva.
    
     Importante
    
    Este método solo se puede utilizar si se solicitó un control de calidad para la orden de fabricación. De lo contrario, el botón Alerta de calidad no aparecerá.
    
- Abra la aplicación Inventario, haga clic en el botón # por procesar de una tarjeta de tipo de orden de inventario (como recibos, órdenes de entrega, entre otras) y seleccione una orden. Haga clic en el botón Alerta de calidad ubicado en la parte superior de la orden para abrir un formulario de alerta de calidad en una nueva página.
    
     Importante
    
    Este método solo se puede utilizar si se solicitó un control de calidad para la orden de inventario. De lo contrario, el botón Alerta de calidad no aparecerá. Si el botón no aparece, también puede crear una alerta de calidad si hace clic en el icono ⚙️ (engranaje) ubicado en la parte superior de la página y selecciona la opción Alerta de calidad del menú que aparece.
    
- Abra el módulo Taller y seleccione un centro de trabajo con la barra de navegación ubicada en la parte superior de la página. Haga clic en el botón ⋮ (tres puntos verticales) que se encuentra en la esquina inferior derecha de una tarjeta de orden de trabajo para abrir el menú ¿Qué desea hacer?. Elija la opción Crear una alerta de xalidad de este menú para abrir una en una ventana emergente.
    

 Nota

Es probable que el formulario ya tenga algunos campos con información, esto depende de la forma en la que abra el formulario de la nueva alerta de calidad. Por ejemplo, si creó la alerta de calidad desde la tarjeta de una orden de trabajo en el módulo _Taller_, entonces los campos Producto y Centro de trabajo ya estarán completados.

### Formulario de alertas de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_alerts.html#quality-alerts-form "Enlazar permanentemente con este título")

Después de abrir el formulario para la nueva alerta de calidad, proporciónele un título corto que resuma el error en el producto.

Después, verifique con cuál de las siguientes opciones está relacionada la alerta de calidad:

- **Un producto o variante del producto en específico:** selecciónelos con los menús desplegables Producto y Variante del producto.
    
- **Un centro de trabajo en específico:** selecciónelo con el menú desplegable Centro de trabajo.
    
- **Una orden de recolección en específico:** selecciónela con el menú desplegable Recolección.
    

Después, seleccione al equipo de calidad responsable de gestionar la alerta en el campo Equipo. Si un empleado en particular es el responsable de la alerta de calidad, selecciónelo en el menú desplegable Responsable.

En el campo Etiquetas, seleccione con el menú desplegable todas las que estén relacionadas con la alerta de calidad.

Use el campo Causa principal para elegir qué es lo que ocasiona el error de calidad, en caso de que lo sepa.

Por último, seleccione un nivel de prioridad con el número de ⭐ (estrellas). Puede elegir entre una y tres. Las alertas de calidad con mayor prioridad aparecen en la parte superior del tablero Alertas de calidad en la vista de kanban de la aplicación _Calidad_.

En la parte inferior del formulario de la alerta de calidad hay cuatro pestañas que son útiles para agregar información o acciones a la alerta de calidad. Complételas de la siguiente forma:

- Pestaña Descripción: proporcione una descripción acerca del error de calidad.
    
- Pestaña Acciones correctivas: proporcione información detallada sobre los pasos que se deben tomar para solucionar el problema.
    
- Pestaña Acciones preventivas: proporcione información detallada sobre lo que debe hacer para evitar que este problema vuelva a ocurrir.
    
- Pestaña Varios: allí podrá seleccionar al proveedor del producto. Si usa una base de datos de Odoo que se encarga de gestionar más de una empresa, asegúrese de elegir la correcta en el campo correspondiente. Por último, especifique la fecha en la que el equipo de calidad recibió la asignación de la alerta en el campo Fecha asignada.
    

![Un formulario de alerta de calidad con los campos completados.](https://www.odoo.com/documentation/17.0/es/_images/alert-form1.png)

## Gestionar las alertas de calidad[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/quality/quality_management/quality_alerts.html#manage-quality-alerts "Enlazar permanentemente con este título")

Vaya a Calidad ‣ Control de calidad ‣ Alertas de calidad para ver todas las alertas de calidad existentes. Las alertas aparecen en un tablero con vista de kanban de forma predeterminada, además de que están organizadas por etapas según la que corresponda a su proceso de revisión.

Para mover una alerta a otra etapa solo debe arrastrarla y soltarla en la adecuada. Como alternativa, seleccione una alerta de calidad para abrirla y después haga clic en la etapa deseada estas están ubicadas en la esquina superior derecha del formulario de la alerta de calidad.

Para crear una nueva alerta en una etapa específica, haga clic en el botón + (más) ubicado del lado derecho del nombre de la etapa. Escriba el título de la nueva alerta en la tarjeta que aparece debajo del título de la etapa y después haga clic en Agregar. Para configurar las otras alertas, selecciónelas para abrir sus formularios.

![La página de alertas de calidad. Las alertas aparecen en la vista de kanban.](https://www.odoo.com/documentation/17.0/es/_images/alert-kanban.png)