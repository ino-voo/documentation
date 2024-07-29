In the Odoo _Inventory_ app, [warehouses](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/warehouses.html) handle the broader organization and distribution of stock across different physical sites, while [locations](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html) provide a more detailed breakdown within each warehouse for efficient item management.

This document serves as an introduction to the terminology and concepts necessary to master _Inventory_. For specific instructions and examples of how things work, refer to individual documentation pages.

 Ver también

[Odoo Tutorials: Warehouses & Locations](https://www.youtube.com/watch?v=zMvudZVLuUo)

## Warehouses[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management.html#warehouses "Enlazar permanentemente con este título")

[Warehouses](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/warehouses.html) represent a physical place, with a physical address, where a company’s items are stored.

Configure [routes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_routes.html) in a warehouse to control how products move to customers, from vendors, within the warehouse, or [between warehouses](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/resupply_warehouses.html).

## Ubicaciones[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management.html#locations "Enlazar permanentemente con este título")

[Locations](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html) refer to specific areas within a warehouse, such as shelves, floors, or aisles. These are sub-divisions within a warehouse, and are unique to that warehouse. Users can create and manage numerous locations within a single warehouse to organize inventory more precisely.

 Ver también

- [Ubicaciones](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html)
    
- [Ajustes de inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/count_products.html)
    
- [Conteo por ciclos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/cycle_counts.html)
    
- [Desechar inventario](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/scrap_inventory.html)
    

### Location types[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management.html#location-types "Enlazar permanentemente con este título")

_Location types_ in Odoo help categorize and manage where products are, and what actions need to be taken with them. By default, on the Inventory app ‣ Configuration ‣ Locations page, only internal locations are displayed.

To view the seven location types in Odoo, select any location, and in the Location Type field, there are:

- Vendor Location: defines an area where products purchased from vendors originate. Items here are **not** in stock.
    
- View: used to organize and structure the warehouse hierarchy. For example, the view location `WH` (short for warehouse) groups all internal locations, such as `Stock`, receiving docks, quality checkpoints, and packing areas to show they all belong to the same warehouse.
    
     Importante
    
    View locations should **not** contain products, but it is possible to move them there.
    
- Internal Location: storage locations within the warehouse. Items stored in these locations are accounted for in [inventory valuation](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_valuation/using_inventory_valuation.html).
    
- Customer Location: where sold products are tracked; items here are no longer in stock.
    
- Inventory Loss: counterpart location to consume missing items or create stock, accounting for discrepancies.
    
    In Odoo, examples of inventory loss locations are _Inventory Adjustment_, used to account for discrepancies during an inventory count, and _Scrap_, which is where damaged goods are sent to account for inventory losses.
    
    >  Example
    > 
    > `Virtual Locations/Inventory Adjustment` is a location with the Inventory Loss type. The database shows `65` units in `WH/Stock`, but an inventory check reveals `60`. To correct the quantity, five units are moved from `WH/Stock` to `Virtual Locations/Inventory Adjustment`.
    > 
    > ![Product ends up in Virtual Locations/Inventory Adjustment.](https://www.odoo.com/documentation/17.0/es/_images/inventory-loss.png)
    
- Production: where raw materials are consumed, and [manufactured products](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing.html) are created.
    
- Transit Location: used for inter-company or inter-warehouse operations to track products shipped between different addresses, such as [Physical Locations/Inter-warehouse transit](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management.html#inventory-warehouses-storage-interwarehouse-transit).
    

![List of locations in Odoo.](https://www.odoo.com/documentation/17.0/es/_images/locations.png)

 Nota

In Odoo, location types are color-coded:

- **Red**: internal locations
    
- **Blue**: view locations
    
- **Black**: external locations (including inventory loss, vendor, and customer locations).
    

### View locations in Odoo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management.html#view-locations-in-odoo "Enlazar permanentemente con este título")

Odoo databases include pre-configured view locations to organize the hierarchy of locations. These provide helpful context, and distinguish between internal and external locations.

- _Physical locations_ serve as an umbrella for external locations, without changing a product’s inventory value. (Inventory valuation changes occur when products move from internal to external locations).
    

>  Example
> 
> When moving products in warehouses `WH` and `WH2`, the items are not in either warehouse, but still belong to the company. While in transit, they are placed in the `Inter-warehouse transit` location, a Transit Location type.
> 
> This location is under the view location, `Physical Locations`, indicating that `Inter-warehouse transit` is outside of a warehouse, but still part of the company. Doing so does not affect the inventory valuation of the products.

- _Partner locations_ group customer and vendor locations (external locations) together. Transfers to these locations affect inventory valuation.
    
- _Virtual locations_ are locations that do **not** exist physically, but it is where items that are not in inventory can be placed. These can be items that are no longer in inventory due to loss, or other factors.