Odoo detecta automáticamente _leads_ y _oportunidades_ similares dentro de la aplicación _CRM_. Identificar estos registros duplicados permite fusionarlos sin perder información en el proceso. Esto no solo ayuda a mantener el _flujo_ organizado, sino que también evita que los clientes sean contactados por más de un vendedor.

 Nota

No se pierde información al fusionar oportunidades. Los datos de la otra oportunidad se registran en el chatter y en los campos de información como referencia.

## Identificar leads y oportunidades similares[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/merge_similar.html#identify-similar-leads-and-opportunities "Enlazar permanentemente con este título")

Los contactos y oportunidades similares se identifican comparando la _dirección de correo electrónico_ y el _número de teléfono_ del contacto asociado. Si se encuentra un cliente potencial u oportunidad similar, aparece un botón inteligente _Leads similares_ en la parte superior del registro del lead (u oportunidad).

![Un registro de oportunidad en el que se resalta el botón inteligente de Leads similares.](https://www.odoo.com/documentation/17.0/es/_images/similar-smart-button.png)

### Comparación de leads y oportunidades similares[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/merge_similar.html#comparing-similar-leads-and-opportunities "Enlazar permanentemente con este título")

To compare the details of similar leads/opportunities, navigate to CRM app ‣ Pipeline or CRM app ‣ Leads. Open a lead or opportunity, and click the Similar Leads smart button. Doing so opens a Kanban view that only displays similar leads/opportunities. Click on a card to view the details for the lead/opportunity, and confirm if they should be merged.

## Fusionar leads y oportunidades similares[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/merge_similar.html#merging-similar-leads-and-opportunities "Enlazar permanentemente con este título")

 Importante

Al fusionar, Odoo prioriza el lead u oportunidad que se creó primero en el sistema y fusiona la información en donde se creó primero. Si fusiona un lead y una oportunidad el registro resultante se denomina oportunidad, sin importar que se creó primero.

After confirming that the leads/opportunities should be merged, return to the Kanban view using the breadcrumb link, or by clicking the Similar Leads smart button. Click the  (list) icon to change to list view.

Check the box on the left of the page for the leads/opportunities to be merged. Then, click the  Actions icon at the top of the page, to reveal a drop-down menu. From that drop-down menu, select the Merge option to merge the selected opportunities or leads.

When Merge is selected from the  Actions drop-down menu, a Merge pop-up modal appears. In that pop-up modal, under the Assign opportunities to heading, select a Salesperson and Sales Team from the appropriate drop-down menus.

Debajo de esos campos aparecen los leads y las oportunidades a fusionar, así como su información relacionada. Haga clic en Fusionar.

![Lista de leads y oportunidades similares que se seleccionaron para fusionarse en la aplicación CRM.](https://www.odoo.com/documentation/17.0/es/_images/select-merge.png)

 Peligro

La fusión es irreversible, **no** lo haga a no ser que esté completamente seguro de que los leads y las oportunidades se deben fusionar.

## Cuándo no se deben fusionar los leads u oportunidades[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/merge_similar.html#when-leads-opportunities-should-not-be-merged "Enlazar permanentemente con este título")

Puede haber casos en los que se identifique un lead o una oportunidad similares, pero que _no_ deban fusionarse. Estas circunstancias varían en función de los procesos del equipo de ventas y de la organización. A continuación se enumeran algunos posibles escenarios.

### Leads perdidos[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/merge_similar.html#lost-leads "Enlazar permanentemente con este título")

Si un lead u oportunidad se marca como [perdido](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/lost_opportunities.html), todavía es posible fusionarlo con un lead u una oportunidad activos. El lead u oportunidad resultante se marca como activa y se agrega al flujo.

### Diferente contacto dentro de una misma organización[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/merge_similar.html#different-contact-within-an-organization "Enlazar permanentemente con este título")

Los leads u oportunidades de la misma organización, pero con diferentes puntos de contacto, pueden no tener las mismas necesidades. En este caso, es mejor _no_ fusionar estos registros, aunque asignar el mismo vendedor, o equipo de ventas, puede evitar la duplicación de trabajo y la falta de comunicación.

### Duplicados existentes con más de un vendedor[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/merge_similar.html#existing-duplicates-with-more-than-one-salesperson "Enlazar permanentemente con este título")

Si existe más de un lead u oportunidad en la base de datos, es posible que haya varios vendedores asignados a ellos que estén trabajando activamente en ambos de forma independiente y al mismo tiempo. Aunque es posible que estos leads u oportunidades deban gestionarse por separado, se recomienda etiquetar a los vendedores afectados en una nota interna para que sean visibles.

### La información de contacto es similar pero no la misma[](https://www.odoo.com/documentation/17.0/es/applications/sales/crm/pipeline/merge_similar.html#contact-information-is-similar-but-not-exact "Enlazar permanentemente con este título")

Los leads y las oportunidades similares se identifican comparando las direcciones de correo electrónico y los números de teléfono de los contactos asociados. Sin embargo, si la dirección de correo electrónico es _similar_, pero no _exacta_, es posible que deban seguir siendo independientes.

 Example

Hay tres diferentes leads en el flujo asignados a diferentes vendedores. Se identificaron como _leads similares_ debido al correo electrónico de los contactos.

Dos de los leads parecen ser de la misma persona, `Robin` y tienen correos electrónicos idénticos. Estos leads se deberían fusionar.

El tercer lead tiene el mismo dominio de correo, pero la dirección es diferente, así como el nombre del contacto. Aunque este lead es muy probablemente de la misma organización, es de un contacto diferente y **no** se deben fusionar.

![Lista de leads similares con énfasis en la información de contacto en la aplicación CRM.](https://www.odoo.com/documentation/17.0/es/_images/contact-info-example.png)