Odoo’s _Contacts_ application allows user’s to merge duplicate contacts, without losing any information in the process. This keeps the database organized, and prevents contacts from being contacted by more than one salesperson.

## Merge duplicate contacts[](https://www.odoo.com/documentation/17.0/es/applications/essentials/contacts/merge.html#merge-duplicate-contacts "Enlazar permanentemente con este título")

 Peligro

Merging is an irreversible action. Do **not** merge contacts unless absolutely certain they should be combined.

Navigate to the Contacts app, and select the  (list) icon. Select two or more duplicate contacts from the list, and tick the checkbox (on the far-left) for the contacts that should be merged. Then, click the  Actions icon, and select Merge from the resulting drop-down menu.

![The merge contacts option in the Contacts application.](https://www.odoo.com/documentation/17.0/es/_images/merge-menu.png)

This opens the Merge pop-up window. From here, review the details of the contacts before confirming they should be merged. If any contacts in the list should **not** be merged, click the  (delete) icon at the far right of the contact.

 Truco

Click the individual contact to open the record for that contact, and view additional information.

![The merge pop-up window in the Contacts application.](https://www.odoo.com/documentation/17.0/es/_images/merge-window.png)

Click the Destination Contact field, and select an option from the drop-down list. This field defaults to the contact record that was created first in the system.

After confirming the information on the pop-up window, click Merge Contacts.

## Deduplicate contacts[](https://www.odoo.com/documentation/17.0/es/applications/essentials/contacts/merge.html#deduplicate-contacts "Enlazar permanentemente con este título")

After the merge is finished, a pop-up window appears confirming it is complete. This pop-up window also contains a Deduplicate the other Contacts button. This feature searches for duplicated records, based on selected criteria, and merges them automatically, or after manual approval.

Click the Deduplicate the other Contacts button to open the Deduplicate Contacts pop-up window.

Select one or more fields to be used in the search for duplicated records. Duplicated contacts can be searched, based on the following criteria:

- Email
    
- Name
    
- Is Company
    
- VAT
    
- Parent Company
    

 Nota

If more than one field is selected, only records that have **all** fields in common are suggested as duplicates.

If necessary, select criteria to be used to exclude potential duplicates from the search. Potential duplicates can be excluded from the search, based on the following criteria:

- A user associated to the contact
    
- Journal Items associated to the contact
    

After confirming the search criteria, click either Merge with Manual Check, Merge Automatically, or Merge Automatically all process.

If Merge with Manual Check is selected, complete the merge by following the [steps above](https://www.odoo.com/documentation/17.0/es/applications/essentials/contacts/merge.html#contacts-merge-duplicate).