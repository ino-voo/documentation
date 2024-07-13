El _minado de leads_ es una función que le permite a los usuarios de CRM generar leads nuevos directamente en su base de datos de Odoo. Para asegurar la calificación de los leads, el resultado del minado de leads se determina según varios criterios de filtro, como país, tamaño de la empresa e industria.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/lead_mining.html#configuration "Enlazar permanentemente con este título")

Primero vaya a CRM ‣ Configuración ‣ Ajustes y marque la casilla Minado de leads para activar la función. Después, haga clic en Guardar.

![Activar el minado de leads en los ajustes de CRM.](https://www.odoo.com/documentation/17.0/es/_images/activate-lead-mining.png)

## Generar leads[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/lead_mining.html#generate-leads "Enlazar permanentemente con este título")

Después de que el ajuste _Minado de leads_ se haya activado, tendrá disponible un botón nuevo, _Generar leads_, que podrá usar en la esquina superior izquierda del _Flujo_ _CRM_ (CRM ‣ Ventas‣ Mi flujo).

Las solicitudes de minado de leads también están disponibles en CRM ‣ Configuración ‣ Solicitudes de minado de leads, o en CRM ‣ Leads ‣ Leads, donde también está disponible el botón Generar leads.

![El botón Generar leads para usar la función de minado de leads.](https://www.odoo.com/documentation/17.0/es/_images/generate-leads-button.png)

Haga clic en el botón Generar leads y aparecerá una ventana emergente donde podrá elegir los diferentes criterios que se deberán de tomar en cuanta para generar un lead.

![La ventana emergente en la que podrá elegir los criterios mediante los cuales se generarán los leads en Odoo.](https://www.odoo.com/documentation/17.0/es/_images/generate-leads-popup.png)

Si solo quiere obtener información de empresas, seleccione generar leads solo para Empresas o seleccione Companies and their Contacts para obtener información sobre la empresa e información de contacto de los empleados individuales.

 Nota

Al seleccionar Companies and their Contacts hay opciones adicionales disponibles por las que puede filtrar los contactos según Función o Antigüedad.

Otros filtros incluyen

- Países: filtra leads según el país (o países) en los que trabaja la empresa.
    
- Estado: si es posible, también filtra leads según el estado en el que se encuentren.
    
- Sectores: filtra leads según el sector en el que trabajan.
    
- Filtrar por tamaño: marque esta casilla para especificar el número de empleados en la empresa y generar un campo llamado Tamaño. Llene los campos en blanco para generar un rango para el tamaño deseado de la empresa.
    
- Equipo de ventas: escoja a qué equipo de ventas se le asignarán los leads.
    
- Vendedor: escoja a qué persona del equipo de ventas se le asignará el lead.
    
- Etiquetas predeterminadas: escoja qué etiquetas se aplicarán de inmediato a los leads una vez que se creen.
    

 Importante

Asegúrese de conocer las normativas más recientes de la UE respecto a la información de sus contactos. Aprenda más sobre el Reglamento General de Protección de Datos en [la página de RGPD de Odoo](http://odoo.com/gdpr).

### Ver leads[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/lead_mining.html#view-leads "Enlazar permanentemente con este título")

Una vez que se generan los leads, estos se asignan al vendedor y el equipo designados. Para ver información adicional sobre el lead, seleccione uno de la lista y haga clic en él para abrirlo.

Podrá encontrar información adicional en el hilo del chatter del lead. Esta información puede incluir el número de empleados, la tecnología que usa la empresa, la zona horaria e información directa de contacto.

![El hilo de chatter de un lead recién generado.](https://www.odoo.com/documentation/17.0/es/_images/generated-lead.png)

 Nota

Si los Leads no están activados para la base de datos, entonces los leads se generarán como _oportunidades_ y se agregarán al flujo del vendedor designado.

Para activar la función de Leads vaya a CRM ‣ Configuración ‣ Ajustes y marque la casilla de verificación Leads. Finalmente, haga clic en Guardar.

## Precio[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/lead_mining.html#pricing "Enlazar permanentemente con este título")

El minado de leads es una función que requiere de _compras dentro de la aplicación_. Cada lead que se genere cuesta un [crédito](https://www.odoo.com/documentation/17.0/es/applications/essentials/in_app_purchase.html#in-app-purchase-credits).

 Importante

Generar Companies and their Contacts cuesta un crédito adicional por cada contacto generado. Vea la siguiente documentación para más información sobre los precios: [Generación de leads por Odoo IAP](https://iap.odoo.com/iap/in-app-services/167?).

Para comprar créditos, vaya a CRM ‣ Configuración ‣ Ajustes. En la sección de Generación de leads vaya a la función Minado de leads y haga clic en Comprar créditos.

También puede comprar créditos en la aplicación Ajustes. En la sección de Contactos busque Compras dentro de la aplicación de Odoo y haga clic en Ver mis servicios.

![Compre créditos en los ajustes de compras dentro de la aplicación de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/view-my-services-setting.png)

 Nota

Los usuarios de Odoo Enterprise que tengan una suscripción válida obtendrán créditos gratuitos para probar las funciones de [|compras dentro de la aplicación|](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/acquire_leads/lead_mining.html#id1) antes de decidir si quieren comprar más créditos para la base de datos. Esto incluye bases de datos de demostración y capacitación, bases de datos educativas y bases de datos gratuitas de una sola aplicación.

 Ver también

[Compras dentro de la aplicación (IAP, por sus siglas en inglés)](https://www.odoo.com/documentation/17.0/es/applications/essentials/in_app_purchase.html)