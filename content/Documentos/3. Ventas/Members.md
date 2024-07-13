# Members[](https://www.odoo.com/documentation/17.0/es/applications/sales/members.html#members "Enlazar permanentemente con este título")

The _Members_ application is where all operations related to memberships can be configured and managed. The _Members_ app integrates with the _Sales_ and _Accounting_ applications to sell and invoice memberships directly to customers.

## Membership products[](https://www.odoo.com/documentation/17.0/es/applications/sales/members.html#membership-products "Enlazar permanentemente con este título")

To create a new membership product, navigate to Members app ‣ Configuration ‣ Membership Products, and click New to open a blank product record.

Complete the blank form with the necessary information, including the Membership Duration.

 Nota

Membership products require a start and end date, as they are used to determine [membership status](https://www.odoo.com/documentation/17.0/es/applications/sales/members.html#sales-membership-status). Membership products can be sold _before_ their active start date.

![A new membership product in the members app.](https://www.odoo.com/documentation/17.0/es/_images/membership-product.png)

Membership products can be added to a sales order, and invoiced as regular products or subscriptions.

## Activate a membership[](https://www.odoo.com/documentation/17.0/es/applications/sales/members.html#activate-a-membership "Enlazar permanentemente con este título")

To activate a membership from the _Contacts_ application, navigate to Contacts app, and click on a contact to open that specific contact’s detail form.

From the resulting contact form, open the Membership tab, and click Buy Membership.

On the Join Membership pop-up window that appears, select a Membership from the drop-down menu. Then, configure a Member Price.

Click Invoice Membership when both fields are filled in. Doing so reveals a Membership Invoices page, wherein invoices can be confirmed and completed.

Alternatively, to offer a free membership, tick the Free Member checkbox, in the Membership tab of a contact form.

## Membership status[](https://www.odoo.com/documentation/17.0/es/applications/sales/members.html#membership-status "Enlazar permanentemente con este título")

The Current Membership Status is listed on the Membership tab of each contact record:

- Non Member: a partner who has **not** applied for membership.
    
- Cancelled Member: a member who has cancelled their membership.
    
- Old Member: a member whose membership end date has passed.
    
- Waiting Member: a member who has applied for membership, but whose invoice has not yet been created.
    
- Invoiced Member: a member whose invoice has been created, but has not been paid.
    
- Paid Member: a member who has paid the membership fee.
    

## Publish members directory[](https://www.odoo.com/documentation/17.0/es/applications/sales/members.html#publish-members-directory "Enlazar permanentemente con este título")

To publish a list of active members on the website, the _Online Members Directory_ application must first be [installed](https://www.odoo.com/documentation/17.0/es/applications/general/apps_modules.html#general-install). After installing the module, add the `/members` page to the website’s menu by [editing the website menu](https://www.odoo.com/documentation/17.0/es/applications/websites/website/pages/menus.html).

![The Online Members directory module in Odoo.](https://www.odoo.com/documentation/17.0/es/_images/membership-directory-app.png)

### Publish individual members[](https://www.odoo.com/documentation/17.0/es/applications/sales/members.html#publish-individual-members "Enlazar permanentemente con este título")

Return to CRM app ‣ Sales ‣ Customers, and click the Kanban card for a member. From the resulting customer form that appears, click the Go to Website smart button at the top of the page to open the member’s webpage.

Click the  Edit button to reveal a sidebar of editing tools. After making any necessary changes to the page, click Save. At the top of the page, slide the Unpublished toggle to the active, Published position.

Repeat these steps for all desired members.