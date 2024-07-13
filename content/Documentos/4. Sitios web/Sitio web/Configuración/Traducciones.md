El contenido de las páginas de su sitio web (por ejemplo, las cadenas de texto) se puede traducir a distintos idiomas desde su sitio web.

Su sitio web se muestra en el idioma que coincide con el idioma del navegador del visitante, a menos que ese idioma en particular no se haya instalado. En este caso, el sitio web se muestra en el [idioma predeterminado](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/translate.html#translate-default-language). El visitante todavía puede elegir otro idioma en el menú de idioma.

## Instalar idiomas[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/translate.html#installing-languages "Enlazar permanentemente con este título")

Para traducir su sitio web, primero debe agregar los idiomas necesarios:

1. Vaya a su sitio web.
    
2. Diríjase a la parte inferior de la página al **menú de idioma**.
    
3. Haga clic en el idioma y seleccione Agregar un idioma.
    
    ![Agregar un idioma a su sitio web.](https://www.odoo.com/documentation/17.0/es/_images/website-add-language.png)
    
4. Click the Languages field and select the required language from the drop-down list. Ticking the Websites to translate checkboxes allows users to change your website’s navigation to another language using the language selector.
    
5. Haga clic en el botón Agregar.
    

Repeat the steps for each additional language.

 Truco

- You might need to refresh your page to see the new language.
    
- También puede editar los idiomas de su sitio web desde el backend, en Ajustes. Vaya a Sitio web –> Configuración –> Ajustes y agregue o elimine los idiomas requeridos en el campo Idiomas en la sección Información del sitio web .
    

### Idioma predeterminado[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/translate.html#default-language "Enlazar permanentemente con este título")

El contenido se mostrará en el idioma predeterminado en caso de que el idioma del navegador del visitante no esté instalado en su sitio web.

Para definir un idioma predeterminado, vaya a Sitio web –> Configuración –> Ajustes y seleccione un idioma en el campo Predeterminado.

 Nota

Este campo solo es visible si ya están configurados varios idiomas para su sitio web.

## Traducir el contenido[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/translate.html#translating-the-contents "Enlazar permanentemente con este título")

Una vez que se han agregado los idiomas, puede traducir el contenido de su sitio web. Vaya a su sitio web, seleccione el idioma en el menú de idioma y haga clic en el botón Traducir en la parte derecha de la barra de tareas para activar el **modo de traducción**.

![Botón de traducir](https://www.odoo.com/documentation/17.0/es/_images/translate-button.png)

Como resultado:

- las cadenas de texto que ya han sido traducidas se resaltan en verde;
    
- las cadenas de texto que necesitan ser traducidas se resaltan en amarillo.
    

![Texto a traducir resaltado en amarillo](https://www.odoo.com/documentation/17.0/es/_images/website-translation-yellow.png)

A continuación, puede reemplazar el texto original con la traducción haciendo clic en el bloque, editando su contenido y guardando.

 Truco

- Una vez que instaló los idiomas, también puede traducir algunos elementos (por ejemplo, el nombre y la descripción del producto) desde el backend (por ejemplo, en la plantilla del producto). Para ello, haga clic en el código de idioma (EN o el que corresponda) junto al texto que desea traducir (en este caso, el nombre del producto) y agregue la traducción.
    
    ![Traducir artículos relacionados con los productos.](https://www.odoo.com/documentation/17.0/es/_images/product-translation.png)
    
- También puede [exportar o importar traducciones](https://www.odoo.com/documentation/17.0/es/developer/howtos/translations.html) para traducir varios elementos (por ejemplo, nombres de productos y descripciones) en un solo paso.
    

## Menú de selección de idioma[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/translate.html#language-selector-menu "Enlazar permanentemente con este título")

Para agregar un menú de selección de idioma:

1. Vaya a su sitio web y haga clic en Editar.
    
2. Seleccione el bloque donde desea agregar el menú de selección de idioma (por ejemplo, el encabezado).
    
3. Seleccione la pestaña Personalizar.
    
4. En la sección Navbar, establezca el campo Selector de idioma en Desplegable o En línea.
    
    ![Agregar un menú de selección de idioma.](https://www.odoo.com/documentation/17.0/es/_images/language-selector.png)
    
5. Haga clic en Guardar.