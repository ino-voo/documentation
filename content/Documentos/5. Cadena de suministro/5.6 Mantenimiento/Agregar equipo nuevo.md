En Odoo, un _equipo_ es cualquier artículo que se utilice en operaciones cotidianas, esto incluye la fabricación de productos. Puede ser una máquina en una línea de producción, una herramienta que se utiliza en varios lugares o una computadora en una oficina. Los equipos registrados en Odoo pueden ser propiedad de la empresa que utiliza la base de datos de Odoo, o de un tercero, como un proveedor (en caso de alquilar los equipos).

Si usa la aplicación **Mantenimiento** de Odoo, puede realizar un seguimiento de las partes individuales de un equipo junto con la información sobre sus requisitos de mantenimiento. Para agregar un nuevo equipo, vaya al módulo de Mantenimiento y seleccione Equipos ‣ Máquinas y herramientas ‣ Nuevo, configure el equipo de la siguiente manera:

- Nombre del equipo: el nombre de producto del equipo.
    
- Categoría del equipo: la categoría a la que pertenece el equipo; por ejemplo, computadoras, maquinaria, herramientas, etc. También puede crear nuevas categorías, vaya a Configuración ‣ Categorías de equipo y haga clic en Nuevo.
    
- Empresa: la empresa propietaria del equipo, puede ser la que utiliza la base de datos de Odoo o una empresa externa.
    
- Usado por: especifique si un empleado específico, departamento, o ambos utilizan el equipo. Seleccione Otro si se comparte entre un empleado y un departamento.
    
- Equipo de mantenimiento: el equipo responsable del mantenimiento del equipo. Puede crear nuevos equipos, vaya a Configuración ‣ Equipos de mantenimiento y seleccione Nuevo. Los miembros de cada equipo también se pueden asignar desde esta página.
    
- Técnico: la persona responsable del mantenimiento del equipo. Esto puede utilizarse para asignar a una persona específica en caso de que no se asigne ningún equipo de mantenimiento o cuando un miembro específico del equipo asignado siempre sea responsable del equipo. Cualquier persona agregada a Odoo como usuario puede ser asignada como técnico.
    
- Usado en la ubicación: la ubicación donde se utiliza el equipo. Este campo de texto simple se puede utilizar para especificar ubicaciones que no son centros de trabajo (por ejemplo, una oficina).
    
- Centro de trabajo: especifique aquí si el equipo se utiliza en un centro de trabajo. El equipo también se puede asignar a un centro de trabajo, vaya a Mantenimiento ‣ Equipos ‣ Centros de trabajo y seleccione un centro de trabajo o cree uno con el botón Nuevo, luego haga clic en la pestaña Equipo en el formulario del centro de trabajo.
    

![Un ejemplo de un formulario de equipo nuevo configurado en su totalidad.](https://www.odoo.com/documentation/17.0/es/_images/new-equipment-form.png)

## Incluir información adicional del producto[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/add_new_equipment.html#include-additional-product-information "Enlazar permanentemente con este título")

La pestaña Información del producto en la parte inferior de la página se puede utilizar para proporcionar más detalles sobre el equipo:

- Proveedor: el proveedor al que se compró el equipo.
    
- Referencia del proveedor: el código de referencia asignado al proveedor.
    
- Modelo: el modelo específico del equipo.
    
- Número de serie: el número de serie único del equipo.
    
- Fecha efectiva: la fecha en que el equipo estuvo disponible para su uso, se utiliza para calcular el MTBF.
    
- Costo: la cantidad por la que se compró el equipo.
    
- Fecha en la que expira la garantía: la fecha en la que vence la garantía del equipo.
    

![La pestaña de información del producto para el nuevo equipo.](https://www.odoo.com/documentation/17.0/es/_images/new-equipment-product-information.png)

## Agregar detalles de mantenimiento[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/add_new_equipment.html#add-maintenance-details "Enlazar permanentemente con este título")

La pestaña Mantenimiento en la parte inferior de la página brinda información sobre la frecuencia de fallo del equipo:

- Tiempo medio esperado entre fallos: el número promedio de días que se espera que el equipo funcione antes de fallar. Este número se puede configurar de forma manual.
    
- Tiempo medio entre fallos: el número promedio de días que un equipo funcionará entre fallas. Este número se calcula de forma automática tomando en cuenta fallas previas y usted no lo puede configurar.
    
- Próximo fallo estimado: la fecha esperada en la que es posible que el equipo falle. Esta fecha se calcula de forma automática según la información en los campo Tiempo medio esperado entre fallos y Último fallo y usted no lo puede configurar.
    
- Último fallo: la fecha más reciente en la que el equipo falló. Esta fecha se basa en cuándo se creó la solicitud de mantenimiento del equipo más reciente y usted no la puede configurar.
    
- Tiempo medio de reparación: el número promedio de días que se necesitan para reparar el equipo. Este número se calcula de forma automática según la duración de las solicitudes de mantenimiento anteriores y no se puede configurar de forma manual.
    

![La pestaña de mantenimiento para una pieza de equipo.](https://www.odoo.com/documentation/17.0/es/_images/new-equipment-maintenance.png)

 Truco

Para ver las solicitudes de mantenimiento en curso de un equipo, vaya a la página del equipo y haga clic en el botón inteligente Mantenimiento en la parte superior del formulario.