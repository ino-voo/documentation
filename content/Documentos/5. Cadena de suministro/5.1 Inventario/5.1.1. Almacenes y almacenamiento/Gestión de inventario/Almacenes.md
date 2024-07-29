In the Odoo _Inventory_ app, a _warehouse_ is a physical space with an address for storing items, such as a storage facility, distribution center, or physical store.

Each database has a pre-configured warehouse with the company’s address. Users can set up multiple warehouses, and [create stock moves](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_routes.html) between them.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/warehouses.html#configuration "Enlazar permanentemente con este título")

To create or manage warehouses, go to Inventory app ‣ Configuration ‣ Warehouses.

Then, select an existing warehouse, or create a new one by clicking New. Doing so opens the warehouse form, which contains the following fields:

- Warehouse (_required field_): the full name of the warehouse.
    
- Short Name (_required field_): the abbreviated code for the warehouse (maximum five characters). The short name for the default warehouse in Odoo is `WH`.
    
     Importante
    
    The Short Name appears on warehouse documents, so it is recommended to use an memorable one, like «WH[first letters of location]» (e.g. `WHA`, `WHB`, etc.).
    
- Address (_required field_): the address of the warehouse. To change the warehouse address when creating two or more warehouses, hover over the field, and click the  (right arrow).
    
- Company (_required field_): the company that owns the warehouse; this can be set as the company that owns the Odoo database, or the company of a customer or vendor.
    
- Intrastat region: [region name](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html) required for companies in the European Union.
    

 Importante

The options below are available **only** when the _Multi-Step Routes_ feature is enabled in Inventory app ‣ Configuration ‣ Settings.

- Incoming Shipments: select the option to receive products from the warehouse in [one](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html), [two](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html), or [three](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_three_steps.html) steps.
    
- Outgoing Shipments: select the option to deliver products from the warehouse in [one](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_one_step.html), [two](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/receipts_delivery_two_steps.html), or [three](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/daily_operations/delivery_three_steps.html) steps.
    
- Dropship Subcontractors: available with the _Subcontracting_ feature enabled in Manufacturing app ‣ Configuration ‣ Settings. Tick this checkbox to purchase components from vendors, and dropship them to subcontractors.
    
- Resupply Subcontractors: available with the _Subcontracting_ feature, tick this checkbox to supply subcontractors with raw materials stored in _this_ specific warehouse.
    
- Manufacture to Resupply: tick this checkbox to allow for items to be manufactured in this warehouse.
    
- Manufacture: choose whether to manufacture products in [one](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/one_step_manufacturing.html), [two](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/two_step_manufacturing.html), or [three steps](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/basic_setup/three_step_manufacturing.html).
    
- Buy to Resupply: tick this checkbox to allow for purchased products to be delivered to the warehouse.
    
- Resupply From: available with multiple warehouses in the database, select warehouses to pull stock _from_ to fulfill orders.
    

 Ver también

[Use inventory adjustments to add stock to new warehouses](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/count_products.html)

![Example warehouse form.](https://www.odoo.com/documentation/17.0/es/_images/warehouse-form.png)