A _location_ is a specific space within a warehouse. This can be a shelf, room, aisle, etc.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html#configuration "Enlazar permanentemente con este título")

To create specific storage locations, enable the _Storage Locations_ feature by going to Inventory app ‣ Configuration ‣ Settings. In the Warehouses section, tick the Storage Locations checkbox. Then, click Save.

 Nota

Typically, the Storage Locations feature is used with [Multi-Step Routes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_routes.html), which controls how products move between locations.

![Show Storage Locations feature.](https://www.odoo.com/documentation/17.0/es/_images/enable-location.png)

## Create new location[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html#create-new-location "Enlazar permanentemente con este título")

After enabling _Storage Locations_, go to Inventory app ‣ Configuration ‣ Locations.

![List of internal locations.](https://www.odoo.com/documentation/17.0/es/_images/locations2.png)

On this page, click New. The new location form can then be configured as follows:

- Location Name: recognizable name of the location.
    
- Parent Location: the location within which the new location exists. After the location is created, it is listed on the Locations page using a _location hierarchy_, to describe how a specific location fits within larger areas of the warehouse.
    
     Example
    
    In `WH/Stock/Zone A/Refrigerator 1`, «Refrigerator 1» is the location name, «Zone A» is the parent location, and everything before it is the path showing where this spot is within the warehouse.
    

### Additional Information section[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html#additional-information-section "Enlazar permanentemente con este título")

In addition to the required fields above, configure the following location fields to ensure the location serves its intended purpose in the database:

- Location Type: from the drop-down menu, choose Vendor Location, View, Internal Location, Customer Location, Inventory Loss, Production, or Transit Location to categorize the location. For details on each location type, refer to the [Location Types section](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management.html#inventory-warehouses-storage-location-type).
    
- Storage Category: only available with the [Storage Categories](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/advanced_operations_warehouse/putaway.html#inventory-warehouses-storage-storage-category) feature enabled in Inventory app ‣ Configuration ‣ Settings.
    
- Company: the company the location belongs to.
    
- ¿Es una ubicación de desecho?: seleccione esta casilla para permitir que los bienes desechados o dañados se almacenen en esta ubicación.
    
- ¿Es una ubicación de devolución?: seleccione esta casilla si desea permitir que devuelvan los productos a esta ubicación.
    
- Barcode: used with the _Barcode_ app, enter the barcode to [identify actions](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/software.html#barcode-setup-location) at this location when scanned.
    
- Replenish Location: used for [configuring routes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_routes.html), tick this checkbox to set the location as a destination for receiving products from _Buy_, _Manufacture_, or other procurement routes, ensuring products are correctly supplied to the warehouse.
    

![Sección de información adicional del formulario de creación de nueva ubicación.](https://www.odoo.com/documentation/17.0/es/_images/new-location.png)

Configure los campos restantes en la sección Información adicional de la siguiente manera:

- Empresa: la empresa con el almacén que tiene la ubicación. Deje este campo vacío si varias empresas comparten esta ubicación.
    
- ¿Es una ubicación de desecho?: seleccione esta casilla para permitir que los bienes desechados o dañados se almacenen en esta ubicación.
    
- ¿Es una ubicación de devolución?: seleccione esta casilla si desea permitir que devuelvan los productos a esta ubicación.
    
- Código de barras: el código de barras asignado a la ubicación.
    
- Reabastecer ubicación: seleccione esta casilla para obtener todas las cantidades a reabastecer en esta ubicación.
    

En la sección Conteo cíclico, cambie el valor predeterminado `0` si es necesario en el campo Frecuencia de inventario (días).

![Sección de conteo cíclico del formulario de creación de nueva ubicación.](https://www.odoo.com/documentation/17.0/es/_images/use-locations-cyclic-counting.png)

Cuando no es `0`, las fechas de recuento de inventario para los productos almacenados en esta ubicación se establecerán con la frecuencia definida en automático.

En el campo Estrategia de remoción de la sección Logística, haga clic en el menú desplegable y seleccione la [estrategia correspondiente](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html) para especificar cómo deben retirarse los artículos de esta ubicación.

### Cyclic Counting section[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html#cyclic-counting-section "Enlazar permanentemente con este título")

To schedule regular inventory counts at this location, set the Inventory Frequency (Days) field to the desired interval. By default, it is set to `0` (no scheduled counts).

For example, setting this field to `30`, schedules a count every thirty days. For more specifics on setting up and using this feature, refer to the [Cycle Counts documentation](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/cycle_counts.html).

The Last Effective Inventory field displays the date the last inventory count at this location occurred. When scheduled inventory counts are enabled, the Next Expected Inventory field displays the date of the next inventory count.

 Example

With inventory counts scheduled to occur every `30` days, and the Last Effective Inventory count occurring on July 16, the Next Expected Inventory is August 15.

![Show Cyclic Count section of the locations form.](https://www.odoo.com/documentation/17.0/es/_images/scheduled-count.png)

### Logistics section[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html#logistics-section "Enlazar permanentemente con este título")

In the Logistics section of the locations form, optionally select a Removal Strategy to determine the order and priority of how products are picked from inventory. The options are: First In First Out (FIFO), Last In First Out (LIFO), Closest Location, and First Expiry First Out (FEFO).

 Ver también

[Estrategias de remoción](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/removal_strategies.html)

## Current stock at location[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html#current-stock-at-location "Enlazar permanentemente con este título")

To view the current stock at a single location, go to Inventory app ‣ Configuration ‣ Locations, and select the desired location.

Next, click the Current Stock smart button to get a list of all products at the location.

 Example

A list of current stock at `Shelf 1` consists of `266` cabinets and `39` desks.

![Show stock at Shelf 1.](https://www.odoo.com/documentation/17.0/es/_images/current-stock.png)