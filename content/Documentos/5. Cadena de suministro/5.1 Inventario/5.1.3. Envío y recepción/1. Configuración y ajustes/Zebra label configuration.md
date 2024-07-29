In Odoo, labels printed in the Zebra Programming Language (ZPL) file format are designed to fit a four-by-six inch label. To resize (or reformat) text to fit a variety of ZPL label sizes, [navigate to the ZPL label view](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#inventory-shipping-receiving-zpl-view), and alter the ZPL code.

 Advertencia

When customizing code in Odoo, please note that upgrading the database to newer versions may break custom ZPL code. **Customers are responsible for maintaining their custom code**.

Refer to the following sections for explanations, and example code, for frequently requested Zebra label customizations.

- [Adjust margins](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#inventory-shipping-receiving-margin)
    
- [Enlarge/minimize barcodes](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#inventory-shipping-receiving-resize)
    
- [Rotate elements](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#inventory-shipping-receiving-rotate)
    

## Navigate to ZPL label view[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#navigate-to-zpl-label-view "Enlazar permanentemente con este título")

To begin customizing a Zebra label in Odoo, turn on [developer mode](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode), and on the main Odoo dashboard, type `Reports`. From the search results that appear in the resulting pop-up window, choose Settings / Technical / Reporting / Reports to open the Reports page.

 Nota

To manually navigate to the Reports page, go to Settings app ‣ Technical ‣ Reporting: Reports.

![Show global search result for "Reports".](https://www.odoo.com/documentation/17.0/es/_images/search.png)

On the Reports page, in the Search… bar, type `ZPL`, and hit Enter. Upon doing so, Odoo presents a list of available Zebra labels in Odoo. Select the desired Zebra label from the list to modify it on a separate page.

 Nota

Printable ZPL labels in Odoo:

- [lot/serial number](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-lot-sn-labels)
    
- operation type
    
- package barcode
    
- [product label](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/advanced_operations_shipping/print_on_validation.html#inventory-shipping-receiving-product-labels)
    
- product packaging
    
- finished product (Odoo _Manufacturing_ app required)
    

Next, click the  Qweb Views smart button, and choose the desired label [view](https://www.odoo.com/documentation/17.0/es/developer/reference/user_interface/view_records.html).

![Show Qweb smart button on the Lot and Serial Number (ZPL) report.](https://www.odoo.com/documentation/17.0/es/_images/qweb-views.png)

**Lot and Serial Number (ZPL)** report, highlighting the Qweb smart button.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#id1 "Enlace permanente a esta imagen")

On the resulting view form, go to the Architecture tab to view the ZPL code.

 Importante

To ensure the customization is **not** overwritten during an update, click the  (bug) icon on the view page. Then, select the View Metadata option from the resulting drop-down menu, in order to open the View Metadata pop-up window. Then, ensure the No Update field is set to true (change). Click Ok to exit the View Metadata pop-up window.

![Architecture tab in the view.](https://www.odoo.com/documentation/17.0/es/_images/architecture.png)

## Adjust margin[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#adjust-margin "Enlazar permanentemente con este título")

Text gets cut off from standard ZPL labels printed in Odoo when the line exceeds fifty-five characters. To fit long product names, or lot numbers, on a single line, adjust the margin.

To begin, navigate to the [ZPL code of the label](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#inventory-shipping-receiving-zpl-view) in the Architecture tab. In the ZPL code for product labels, look for the `^FT` command, which specifies where to start placing the text, or graphic element, on the label. The two numbers immediately following `^FT` define the x-coordinate and y-coordinate in dots (similar to pixels for printers) from the left and top margins.

 Importante

When customizing lot/serial number labels, look for the `^FO` command, instead of `^FT`.

 Example

The following is an example where the product’s name gets cut off with Odoo’s default ZPL formatting. In the **Fixed** tab, the x-coordinate of the starting position of the label is changed from `^FT100,80` to `^FT0,80`, to fit the entire name.

DefaultModified

![Example barcode label with the product name cut off.](https://www.odoo.com/documentation/17.0/es/_images/default-margin.png)

**Code**:

^XA^CI28
^FT100,80^A0N,40,30^FD[E-COM11] Cabinet with Doors (wood: Cherry, handles: brass)^FS
...
^XZ

## Resize barcode[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#resize-barcode "Enlazar permanentemente con este título")

To adjust the size of the barcode to scale, begin by navigating to the [ZPL code of the label](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#inventory-shipping-receiving-zpl-view) in the Architecture tab. Look for the `^FO` command (typically in the third line), which is the starting point of the margin for the barcode.

The `^BY` command configures barcode size, and takes three numbers: bar width, width of wide bars relative to narrow bars, and bar height. By default, ZPL code in Odoo uses `^BY3`, setting the bar width to three dots, a typical size that is easy for barcode scanners to read.

 Example

To shrink the barcode to scale, `^BY3` is reduced to `^BY2`.

DefaultModified

![Example barcode label.](https://www.odoo.com/documentation/17.0/es/_images/normal-barcode.png)

**Code**:

^XA^CI28
...
^FO100,160^BY3
...
^XZ

## Rotate elements[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#rotate-elements "Enlazar permanentemente con este título")

To rotate elements in ZPL, begin by navigating to the [ZPL code of the label](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/zebra.html#inventory-shipping-receiving-zpl-view) in the Architecture tab.

The `^BC` command’s first parameter (information that affects the behavior of the command) defines the rotation of an item, which can be:

- `N`: display normally
    
- `R`: rotate 90 degrees
    
- `I`: rotate 180 degrees
    
- `B`: rotate 270 degrees
    

 Example

To rotate the barcode, `^BCN` is changed to `^BCB`.

DefaultModified

![Example barcode label.](https://www.odoo.com/documentation/17.0/es/_images/lot.png)

**Code**:

^XA^CI28
...
^BCN,100,Y,N,N
...
^XZ