Odoo le permite crear varios sitios web con la misma base de datos. Esto puede ser útil, por ejemplo, si trabaja con varias marcas en su organización o para crear sitios web separados para diferentes productos, servicios o incluso distintas audiencias. En estos casos, tener distintos sitios web puede ayudar a evitar confusiones, también facilita la adaptación de sus estrategias de alcance digital para que pueda llegar al público correcto.

Puede diseñar y configurar cada sitio web de forma independiente con su propio [nombre de dominio](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html), [tema](https://www.odoo.com/documentation/17.0/es/applications/websites/website/web_design/themes.html), [páginas](https://www.odoo.com/documentation/17.0/es/applications/websites/website/pages.html), [menús](https://www.odoo.com/documentation/17.0/es/applications/websites/website/pages/menus.html), [idiomas](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/translate.html), [productos](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/products.html), equipo de ventas asignado, etc. También pueden [compartir contenido y páginas entre ellos](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#multi-website-website-content).

 Truco

El contenido duplicado (es decir, compartir páginas e información entre varios sitios web) puede tener un impacto negativo para la [Optimización de motores de búsqueda (SEO)](https://www.odoo.com/documentation/17.0/es/applications/websites/website/pages/seo.html).

## Crear un sitio web[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#website-creation "Enlazar permanentemente con este título")

Siga estos pasos para crear un nuevo sitio web:

1. Vaya a Sitio web ‣ Configuración ‣ Ajustes.
    
2. Haga clic en + Nuevo sitio web.
    
    ![Botón de nuevo sitio web](https://www.odoo.com/documentation/17.0/es/_images/create-website.png)
    
3. Especifique el nombre y el dominio del sitio web. Cada sitio web debe publicarse bajo su propio [dominio](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/domain_names.html).
    
4. En caso de ser necesario, realice los ajustes correspondientes en nombre de la empresa, idiomas e idioma predeterminado.
    
5. Haga clic en el botón Crear.
    

Ahora puede empezar a construir su nuevo sitio web.

 Nota

De forma predeterminada, todas las aplicaciones que haya instalado relacionadas con Sitio web (por ejemplo, **Comercio electrónico**, **Foro**, **Blog**, etc.) y sus páginas web relacionadas también están disponibles en el nuevo sitio. Puede eliminarlas cuando modifique el menú del sitio web.

## Alternar entre sitios web[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#switching-websites "Enlazar permanentemente con este título")

Para alternar entre sitios web, haga clic en el menú junto al botón + Nuevo en la esquina superior derecha y seleccione el sitio web al que desea cambiar.

![Selector de sitios web](https://www.odoo.com/documentation/17.0/es/_images/switch-websites.png)

 Nota

Si cambia de sitio web se le redirigirá a la página de inicio del nuevo sitio web.

## Configuración específica del sitio web[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#website-specific-configuration "Enlazar permanentemente con este título")

La mayoría de los ajustes de los sitios web son específicos para cada uno de ellos, lo que significa que se pueden habilitar o deshabilitar si es necesario. Para adaptar los ajustes de un sitio web, vaya a Sitio web ‣ Configuración ‣ Ajustes. Seleccione el sitio web con el que trabajará en el campo Ajustes de sitio web en la parte superior de la página correspondiente, en el recuadro **amarillo**. Luego, adapte las opciones para ese sitio web en específico.

 Nota

- Los sitios web se crean con la configuración predeterminada y esta no se transfiere de un sitio web a otro.
    
- En un [entorno multiempresa](https://www.odoo.com/documentation/17.0/es/applications/general/companies.html), cada sitio web puede estar vinculado a una empresa específica en su base de datos para que solo sus datos relacionados (por ejemplo, productos, trabajos, eventos, etc.) aparezcan en el sitio web. Para mostrar datos específicos de la empresa, seleccione la empresa correspondiente en el campo Empresa.
    

### Disponibilidad del contenido[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#content-availability "Enlazar permanentemente con este título")

Las páginas, productos, eventos y otros que se crearon desde el frontend (mediante el botón + Nuevo) solo están disponibles de forma predeterminada en el sitio web en el que se crearon. Por otra parte, los registros creados desde el backend están disponibles en todos los sitios web. Puede cambiar la disponibilidad del contenido desde el backend, en el campo Sitio web. Por ejemplo, para los productos, vaya a Comercio electrónico ‣ Productos, seleccione uno y luego vaya a la pestaña Ventas, para los foros vaya a Configuración ‣ Foros y seleccione uno.

![Campo de sitio web en un formulario de foro](https://www.odoo.com/documentation/17.0/es/_images/forum-multi-website.png)

Los registros y características pueden estar disponibles:

- En todos los sitios web: deje el campo Sitio web vacío.
    
- Solo en un sitio web: haga su elección en el campo Sitio web según corresponda.
    
- En algunos sitios web: en este caso, debe duplicar el elemento, luego selecciónelo en el campo Sitio web.
    

#### Paginas de un sitio web[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#website-pages "Enlazar permanentemente con este título")

Para modificar el sitio web en el que publicará una página, siga estos pasos:

1. Vaya a Sitio web‣ Sitio ‣ Páginas.
    
2. Abra el panel de búsqueda y seleccione el sitio web en el que está publicada la página.
    
    ![Mostrar páginas por sitio web](https://www.odoo.com/documentation/17.0/es/_images/pages-switch-websites.png)
    
3. Marque la casilla junto a las páginas que desea modificar.
    
4. Haga clic en el campo Sitio web y seleccione el sitio web, o déjelo vacío para publicar la página en todos los sitios web.
    

 Nota

Cada sitio web debe tener su propia página de inicio, no puede utilizar la misma para varios sitios web.

## Funciones de Comercio electrónico[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#ecommerce-features "Enlazar permanentemente con este título")

Puede restringir funciones de Comercio electrónico como productos, categorías de comercio electrónico, listas de precios, descuentos, proveedores de pagos, etc. [a un sitio web específico](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#website-field).

### Cuentas de cliente[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#customer-accounts "Enlazar permanentemente con este título")

Al habilitar la casilla Cuentas de cliente compartidas en los ajustes del sitio web, [permite que sus clientes usen la misma cuenta](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/ecommerce_management/customer_accounts.html) en todos sus sitios web.

### Precio[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#pricing "Enlazar permanentemente con este título")

Con las [listas de precios](https://www.odoo.com/documentation/17.0/es/applications/websites/ecommerce/managing_products/price_management.html#ecommerce-pricelists), los productos pueden tener un precio distinto en cada sitio web. Se requiere la siguiente configuración:

1. Vaya a Sitio web ‣ Configuración ‣ Ajustes.
    
2. Vaya a la sección Tienda - Productos y seleccione la opción Lista de precios, luego seleccione Múltiples precios por producto.
    
3. Haga clic en Listas de precios para definir listas nuevas o editar las que ya existen.
    
4. Seleccione la lista de precios o haga clic en Nuevo para crear una, luego vaya a la pestaña Configuración y seleccione el Sitio web en el campo correspondiente.
    

## Reportes[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#reporting "Enlazar permanentemente con este título")

### Analítica[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#analytics "Enlazar permanentemente con este título")

Cada sitio web tiene sus propios datos analíticos. Para alternar entre sitios web, haga clic en los botones ubicados en la esquina superior derecha.

![Alternar entre sitios web para obtener los datos analíticos](https://www.odoo.com/documentation/17.0/es/_images/analytics-switch-websites.png)

### Otros datos para reportes[](https://www.odoo.com/documentation/17.0/es/applications/websites/website/configuration/multi_website.html#other-reporting-data "Enlazar permanentemente con este título")

Otros datos para reportes, como los datos del tablero de Comercio electrónico, análisis de ventas en línea y visitantes pueden agruparse por sitio web si es necesario. Abra el panel de búsqueda y haga clic en Agrupar por –> Sitio web.