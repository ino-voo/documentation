Agregar un contacto desde el sitio web facilita la conversión de visitantes a leads u oportunidades. Después de que un visitante envíe su información, se creará una oportunidad de forma automática y se le asignará a vendedor o equipo de ventas indicado.

## Personalizar los formularios de contacto[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/opportunities_form.html#customize-contact-forms "Enlazar permanentemente con este título")

Por defecto, la página _Contáctanos_ en los sitios web de Odoo muestra un formulario de contacto preconfigurado. Este formulario se puede personalizar como sea necesario para poder cumplir con las necesidades del equipo de ventas específico.

Vaya a la aplicación Sitio web ‣ Contáctenos y después haga clic en Editar en la parte superior derecha de la pantalla para abrir el editor de sitio web. Haga clic en el bloque de creación del formulario en el cuerpo de la página web para abrir la configuración del formulario en la barra lateral derecha. Puede personalizar las siguientes opciones en el formulario de contacto desde la sección De en la barra lateral derecha:

![La configuración de los ajustes en un sitio web de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/form-customization.png)

- Accción: la acción por defecto para un formulario de contacto es Enviar un correo. Seleccione Crear una oportunidad desde la lista desplegable para capturar la información en la aplicación _CRM_.
    
- Equipo de ventas: use el menú desplegable para seleccionar el equipo de ventas al que se le deben asignar las oportunidades de este formulario. Este campo **solo** aparece si el campo Acción se configura como Crear una oportunidad.
    
- Vendedor: si las oportunidades se deben asignar a un vendedor específico, selecciónelas del menú desplegable. Si no selecciona nada en este campo, las oportunidades se asignarán según las reglas existentes del equipo.
    
- Campos marcados: use este campo para alterar cómo gestiona los campos marcados este formulario. La opción predeterminada es que los campos marcados se consideren Obligatorios, que es el ajuste recomendado.
    
- Indicador de texto: seleccione cómo distinguir los campos marcados. El carácter que se usa en automático es un asterisco (`*`).
    
- Ancho de las etiquetas: use este campo para alterar la medida de pixeles a lo largo de las etiquetas si así lo quiere.
    
- Al enviar: seleccione cómo reaccionará la página cuando un cliente logre enviar el formulario. Si selecciona nada el cliente se quedará en la misma pantalla, solo aparecerá un mensaje de confirmación en el que se indicará que el formulario se logró enviar. Si selecciona redireccionar el cliente verá una nueva página web que será lo que se haya indicado en el campo URL de abajo. Si selecciona mostrar mensaje un mensaje preconfigurado reemplazará el formulario; en este mensaje se le indicará al cliente que alguien se pondrá en contacto tan pronto como sea posible.
    
- URL: si seleccionó redirigir en el campo Al enviar ingrese el URL de la página a la que se deben redirigir los clientes después de que envíen un formulario.
    
- Visibilidad: use el menú desplegable para agregar condiciones de visibilidad para un campo si así lo desea.
    

 Importante

Si se activó la función _leads_ en los ajustes de _CRM_, si selecciona Crear una oportunidad, lo que se creará será un lead. Para activar los leads, vaya a CRM ‣ Configuración ‣ Ajustes y marque la casilla de verificación Leads. Finalmente, haga clic en Guardar.

### Personalizar los campos del formulario de contacto[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/opportunities_form.html#customize-contact-form-fields "Enlazar permanentemente con este título")

Además de que es posible personalizar los ajustes del formulario en general, también puede personalizar los ajustes de cada campo. Con el menú del editor abierto, haga clic en un campo para abrir los ajustes de configuración del Campo en la barra lateral. Las siguientes opciones están disponibles para personalizar un campo:

- Tipo: seleccione una opción de campo personalizado o un tipo de campo existente.
    
- Tipo de entrada: determine el tipo de información que los clientes deben ingresar. Las opciones disponibles son Texto, Correo electrónico, Teléfono, o URL. Lo que seleccione en este campo limitará el formato que los clientes pueden usar al ingresar información.
    
- Etiqueta: ingrese el nombre del campo.
    
- Posición: elija cómo se debe alinear la etiqueta con el resto del formulario. La etiqueta puede estar oculta, arriba de un campo, a la izquierda del campo o ajustada a la derecha y más cerca del campo.
    
- Descripción: deslice el activador para agregar una descripción al campo con la cual pueda brindar instrucciones adicionales a los clientes. Haga clic debajo del campo en el formulario para agregar la descripción.
    
- Marcador de contenido: escriba un ejemplo que le sirva a los usuarios como guía para cuando deben ingresar información en donde el formato es importante, como número de teléfono o dirección de correo electrónico.
    
- Valor predeterminado: ingrese un valor a incluir en el formulario por defecto si el cliente no brinda información en el campo. _No se recomienda ingresar un valor predeterminado para campos obligatorios_.
    
- Obligatorio: deslice el activador para marcar este campo como obligatorio si **debe** llenarse para que se envíe el formulario.
    
- Visibilidad: seleccione cuándo este campo debe ser visible. Use el botón a la izquierda para elegir si mostrar u ocultar este campo para usuarios de computadoras de escritorio. Use el campo a la derecha para elegir si mostrar u ocultar este campo para usuarios en dispositivos móviles.
    
- Animación: seleccione si este campo debe tener alguna animación.
    

![La configuración de los ajustes de un campo del sitio web de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/field-customization.png)

## Ver oportunidades[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/opportunities_form.html#view-opportunities "Enlazar permanentemente con este título")

Después de que un cliente envíe un formulario de contacto se creará una oportunidad y se asignará según los [ajustes del formulario](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/opportunities_form.html#crm-customize-contact-form). Para ver las oportunidades, vaya CRM ‣ Ventas‣ Mi flujo.

 Nota

Si activó los leads en la base de datos, los formularios que se envíen generarán leads, no oportunidades. Para activar los leads, vaya a CRM ‣ Configuración ‣ Ajustes y marque la casilla de verificación Leads. Finalmente, haga clic en Guardar.

Vaya a CRM ‣ Leads para ver los leads que se acaban de crear.

Haga clic en una tarjeta de oportunidad del tablero Mi flujo en la vista de kanban para abrir el registro de una oportunidad. La información que el cliente haya enviado aparecerá allí.

 Nota

Como los campos del formulario de contacto son personalizables, los campos en el registro de la oportunidad en los que se guarda la información varía.

Si se usa el formulario de contacto preconfigurado, el campo de _asunto_ se agrega al campo Título y el contenido en el campo Notas, que se llama Su pregunta, se agrega a la pestaña Notas internas.

 Ver también

- [Gestionar equipos de ventas](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/manage_sales_teams.html)
    
- [Convertir leads en oportunidades](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/convert.html)
    
- [Asignación de leads con la puntuación predictiva de leads](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/track_leads/lead_scoring.html)
    
- [Formularios del sitio web](https://www.odoo.com/documentation/17.0/es/applications/websites/website/web_design/building_blocks/dynamic_content.html#dynamic-content-form)