HTTP se convierte en el protocolo predeterminado si la opción **Dispositivos directos** está habilitada en los ajustes de Punto de venta (por ejemplo, si usa una [impresora ePos](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/epos_printers.html)).

## Fuerce su Punto de venta a usar una conexión segura (HTTPS)[](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/https.html#force-your-point-of-sale-to-use-a-secure-connection-https "Enlazar permanentemente con este título")

Agregue una nueva **clave** en los **Parámetros del sistema** para forzar a que su Punto de venta use una conexión segura con el protocolo HTTPS.

Active el [modo de desarrollador](https://www.odoo.com/documentation/17.0/es/applications/general/developer_mode.html#developer-mode), vaya a Ajustes ‣ Técnico ‣ Parámetros ‣ Parámetros del sistema, después cree un nuevo parámetro, agregue los siguientes valores y haga clic en _Guardar_.

- **Clave**: `point_of_sale.enforce_https`
    
- **Valor**: `True`
    

 Ver también

- [Certificado autofirmado para impresoras electrónicas del PdV](https://www.odoo.com/documentation/17.0/es/applications/sales/point_of_sale/configuration/epos_ssc.html)