Los incoterms son términos estandarizados que se usan en transacciones internacionales para definir los derechos y las responsabilidades de los compradores y los vendedores. Estos términos establecen las obligaciones sobre la entrega de los bienes, los riesgos de la transferencia y la distribución de los costos entre las partes involucradas. Los incoterms especifican detalles importantes, como en qué punto los riesgos y los costos se transfieren del vendedor al comprador, quién tiene la responsabilidad de transporte, el seguro, despacho de aduana y otros aspectos relevantes de la transacción.

 Nota

Los 11 Incoterms están disponibles en Odoo:

- **EXW**: En fábrica
    
- **FCA**: libre transportista
    
- **FAS**: libre al costado del buque
    
- **FOB**: libre a bordo
    
- **CFR**: costo y flete
    
- **CIF**: coste, seguro y flete
    
- **CPT**: transporte pagado hasta
    
- **CIP**: transporte y seguro pagados hasta
    
- **DPU**: entregado en lugar y descargado
    
- **DAP**: entregado en un punto
    
- **DDP**: entregado con derechos pagados
    

 Ver también

- [Intrastat](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/reporting/intrastat.html)
    
- [Facturas de cliente](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices.html)
    
- [Facturas de proveedor](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/vendor_bills.html)
    

## Definir un incoterm[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/incoterms.html#define-an-incoterm "Enlazar permanentemente con este título")

Para definir un incoterm de manera manual, cree una factura, haga clic en la pestaña Otra información y seleccione Incoterm.

### Ubicación de Incoterm[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/incoterms.html#incoterm-location "Enlazar permanentemente con este título")

Puede agregar una ubicación relevante para el Incoterm seleccionado a la factura en Otra información en el campo Ubicación del Incoterm.

 Example

Si el código de incoterm es `CIF` (Coste, Seguro y Flete, por sus siglas en inglés), la ubicación asociada puede ser el puerto de destino donde se entregarán los bienes.

## Configuración predeterminada de Incoterms[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/incoterms.html#default-incoterm-configuration "Enlazar permanentemente con este título")

Puede configurar una regla de Incoterm predeterminada para que el campo Incoterm se complete de forma **automática** en todas las facturas nuevas que cree. En Contabilidad/Facturación ‣ Configuración ‣ Ajustes diríjase a la sección Facturas de cliente y seleccione un Incoterm en el campo Incoterm predeterminado.

 [Edit on GitHub](https://github.com/odoo/documentation/edit/17.0/content/applications/finance/accounting/customer_invoices/incoterms.rst)

##### EN ESTA PÁGINA

- - [Definir un incoterm](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/incoterms.html#define-an-incoterm)
        
    - [Configuración predeterminada de Incoterms](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/customer_invoices/incoterms.html#default-incoterm-configuration)