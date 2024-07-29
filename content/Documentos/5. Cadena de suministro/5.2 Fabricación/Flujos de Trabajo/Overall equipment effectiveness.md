In Odoo’s _Manufacturing_ app, _overall equipment effectiveness_ (OEE) represents the amount of time a work center is fully productive. OEE is displayed as a percentage of the total time a work center is active.

Fully productive time is considered to be time when the work center is operational **and** processing work orders that have not exceeded their _expected duration_.

OEE helps manufacturing teams understand the efficiency of work centers, and the causes of manufacturing downtime.

 Importante

Since OEE tracks work center productivity, using it requires enabling the work centers feature in the settings of the Manufacturing app.

To do so, navigate to Manufacturing app ‣ Configuration ‣ Settings, and tick the checkbox next to Work Orders, under the Operations heading. Then, click Save.

## Efficiency standards[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/oee.html#efficiency-standards "Enlazar permanentemente con este título")

For OEE to accurately reflect the percentage of fully productive time for a work center, the work center **must** be properly configured with the correct productivity metrics. These include the work center’s _time efficiency_, _capacity_, and _OEE target_.

### Time efficiency[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/oee.html#time-efficiency "Enlazar permanentemente con este título")

Time efficiency represents the efficiency of a work center when processing work orders, and is represented as a percentage. A time efficiency value of 100% signifies that the work center processes work orders at the speed of the expected duration, as listed on a product’s BoM. A value less than or greater than 100% signifies that the work center processes work orders slower or faster than an operation’s expected duration, respectively.

To set the time efficiency for a work center, navigate to Manufacturing app ‣ Configuration ‣ Work Centers, and select a work center. On the General Information tab, enter a numerical value in the Time Efficiency field.

 Example

Manufacturing a _chair_ product requires two operations: _cut_ and _assemble_. The product’s BoM lists an expected duration of 30 minutes for each operation.

The cut operation is carried out at the _cut station_ work center, which has a time efficiency value of 50%. This means it takes twice as long to complete the operation, for a total time of one hour.

The assemble operation is carried out at the _assembly line_ work center, which has a time efficiency value of 200%. This means it takes half as long to complete the operation, for a total time of 15 minutes.

### Capacity[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/oee.html#capacity "Enlazar permanentemente con este título")

Capacity represents how many units of a product can be produced in parallel at a work center. The duration of work orders for multiple units increases or decreases, based on how many units the work center can handle.

To set the capacity for a work center, navigate to Manufacturing app ‣ Configuration ‣ Work Centers, and select a work center. On the General Information tab, enter a numerical value in the Capacity field.

 Example

A _drill station_ work center has a capacity of one unit. An MO is confirmed for 10 units of a _chair_, a product manufactured using the drill station.

Since there are ten times as many units to produce than the work center can handle at once, the operation time is ten times the duration listed on the product’s BoM.

### OEE target[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/oee.html#oee-target "Enlazar permanentemente con este título")

The OEE target is the goal for how much of a work center’s operating time should be fully productive time. It is displayed as a percentage, and should only be set as high as `100%`.

To set the OEE target for a work center, navigate to Manufacturing app ‣ Configuration ‣ Settings ‣ Work Centers, and select a work center. On the General Information tab, enter a numerical value of `100.00` or less in the OEE Target field.

## Calculating OEE[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/oee.html#calculating-oee "Enlazar permanentemente con este título")

OEE is represented as a percentage value between zero and 100. The value signifies the amount of time that a work center was fully productive. The remainder signifies the amount of time that the work center was operating at less than full efficiency. This can occur for a number of reasons, including _reduced speed_, _material availability_, and _equipment failure_.

### Fully productive time[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/oee.html#fully-productive-time "Enlazar permanentemente con este título")

For a work center to be considered fully productive, it must be able to receive work orders, have the components necessary to process work orders, and be operating within the expected duration of the work order it is processing.

 Example

An _assembly line_ work center is not blocked, and receives a work order to assemble a _bicycle_. The required components are available, so production begins as soon as they are picked and delivered to the work center. The work order has an expected duration of 30 minutes, and is completed in 27 minutes. All of this time is considered fully productive time.

### Reduced speed[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/oee.html#reduced-speed "Enlazar permanentemente con este título")

When a work center is operating at reduced speed, it means that it is processing a work order that has exceeded its expected duration. While the work center may be operational, this is not considered fully productive time.

 Example

A _cutting station_ work center receives a work order to cut boards for a _table_. The expected duration of the work order is 15 minutes. The work order ends up taking 18 minutes to complete. The work center is considered to have been operating at reduced speed during the three minutes that exceeded the expected duration.

### Material availability[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/oee.html#material-availability "Enlazar permanentemente con este título")

Material availability refers to situations where a work center is able to accept a work order, but the required components are not available. This can occur because the components are not in stock, or are reserved for a different order.

 Example

Manufacturing of a _bench_ requires 20 units of _wood_. A manufacturing order (MO) is confirmed for 10 units of the bench, but there is not enough wood in stock to begin manufacturing. The time it takes to acquire the wood is recorded as material availability downtime.

### Equipment failure[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/oee.html#equipment-failure "Enlazar permanentemente con este título")

Equipment failure signifies any period of time when a work center is unusable due to maintenance issues with its equipment. This can be due to equipment breaking down, or when a work center is shut down for scheduled maintenance. In these cases, a work center can be blocked using a [maintenance request](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/maintenance/maintenance_requests.html).

 Example

The drill at a _drill station_ work center breaks down, causing the work center to be unusable. A maintenance request is created to fix the drill, and the work center is blocked from receiving work orders. It takes two hours to fix the drill, and make the work center available again. This two-hour period is recorded as equipment failure downtime.

## OEE reporting[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/workflows/oee.html#oee-reporting "Enlazar permanentemente con este título")

To view OEE reporting metrics for every work center, navigate to Manufacturing app ‣ Reporting ‣ Overall Equipment Effectiveness. This page shows the metrics for each work center with OEE data.

Alternatively, to see OEE reporting metrics for a single work center, navigate to Manufacturing app ‣ Configuration ‣ Work Centers, and select a work center. At the top of the work center’s form, click the  OEE smart button.

By default, the main OEE reporting page shows data in a bar chart, while the page for a specific work center shows it in a pie chart. To select a different chart type on either page, click the  (bar chart),  (line chart), or  (pie chart) button above the displayed chart.

It is also possible to see OEE data in a pivot view, or a list displaying each time entry, by clicking the  (pivot view) or  (list view) buttons at the top-right corner of the page.

![The dashboard of the OEE report.](https://www.odoo.com/documentation/17.0/es/_images/oee-report.png)