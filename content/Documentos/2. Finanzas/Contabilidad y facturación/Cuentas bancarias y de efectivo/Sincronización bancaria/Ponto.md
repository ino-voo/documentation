**Ponto** es un servicio que permite que empresas y profesionales agreguen sus cuentas a un solo lugar y vean todas sus transacciones dentro de una sola aplicación. Es una solución externa que está expandiendo continuamente la cantidad de instituciones bancarias que se pueden sincronizar con Odoo.

![Logo de la marca Ponto](https://www.odoo.com/documentation/17.0/es/_images/ponto-logo.png)

**Odoo** se puede sincronizar directamente con su banco para obtener todos los estados de cuenta bancarios importados de manera automática a su base de datos.

Ponto es un proveedor externo de pago que puede gestionar la sincronización entre sus cuentas bancarias y Odoo. [Su precio es de 4 euros al mes por cuenta/integración](https://myponto.com/en#pricing).

 Ver también

- [Sincronización bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html)
    
- [Transacciones](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html)
    

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/ponto.html#configuration "Enlazar permanentemente con este título")

### Vincular las cuentas bancarias con Ponto[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/ponto.html#link-your-bank-accounts-with-ponto "Enlazar permanentemente con este título")

1. Vaya al [sitio web de Ponto (https://myponto.com)](https://myponto.com/).
    
2. Cree una cuenta si aún no tiene una.
    
3. Una vez que haya iniciado sesión, cree una _organización_.
    
    ![Completar el formulario para agregar una organización en Ponto.](https://www.odoo.com/documentation/17.0/es/_images/ponto-organization.png)
    
4. Vaya a :menuselection: `Cuentas --> En vivo`, y haga clic en _Agregar cuenta_.
    
    Es posible que primero deba agregar su **Información de facturación**.
    
5. Seleccione su país, sus instituciones bancarias, proporcione su consentimiento a Ponto y siga los pasos que aparecen en la pantalla para vincular su cuenta bancaria con su cuenta de Ponto.
    
    ![Agregar cuentas bancarias a su cuenta de Ponto.](https://www.odoo.com/documentation/17.0/es/_images/ponto-add-account.png)
    
6. Asegúrese de agregar todas las cuentas bancarias que desea sincronizar con su base de datos de Odoo antes de continuar con los siguientes pasos.
    

### Vincular la cuenta de Ponto con su base de datos de Odoo[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/ponto.html#link-your-ponto-account-with-your-odoo-database "Enlazar permanentemente con este título")

1. Vaya a :menuselection: `Contabilidad --> Configuración --> Agregar una cuenta bancaria`.
    
2. Busque su institución, asegúrese de seleccionar la institución correcta. Una vez que la haya seleccionado, puede verificar que el proveedor externo sea Ponto.
    
3. Haga clic en _Conectar_ y siga los pasos.
    
4. En algún momento deberá autorizar las cuentas a las que desea acceder en Odoo. Seleccione **todas las cuentas** que desee sincronizar, incluso aquellas que pertenezcan a otras instituciones bancarias.
    
    ![Selección de las cuentas que desea sincronizar con Odoo.](https://www.odoo.com/documentation/17.0/es/_images/ponto-select-accounts.png)
    
5. Termine el flujo.
    

 Nota

Debe autorizar todas las cuentas a las que desea acceder en Odoo, pero filtraremos las cuentas en función de la institución que seleccionó en el segundo paso.

### Actualizar sus credenciales de sincronización[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/ponto.html#update-your-synchronization-credentials "Enlazar permanentemente con este título")

Es posible que deba actualizar sus credenciales de Ponto o modificar los ajustes de sincronización.

Para hacerlo, vaya a :menuselection: `Contabilidad --> Configuración --> Sincronización en línea` y seleccione la institución que desea para buscar las otras cuentas. Haga clic en el botón _Obtener cuentas_ para iniciar el flujo.

Durante la actualización, seleccione **todas las cuentas** que desea sincronizar, incluso las que provienen de otras instituciones bancarias.

### Obtener cuentas nuevas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/ponto.html#fetch-new-accounts "Enlazar permanentemente con este título")

Es posible que desee agregar nuevas cuentas en línea a su conexión.

Para hacerlo, vaya a :menuselection: `Contabilidad --> Configuración --> Sincronización en línea` y seleccione la institución que desea para buscar las otras cuentas. Haga clic en el botón _Obtener cuentas_ para iniciar el flujo.

No olvide conservar la autorización para las cuentas existentes (para todas las instituciones que haya sincronizado con Ponto).

## Preguntas frecuentes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/ponto.html#faq "Enlazar permanentemente con este título")

### No aparece ninguna cuenta después de la sincronización[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/ponto.html#after-my-synchronization-no-account-appears "Enlazar permanentemente con este título")

Seleccionó una institución de la lista y no autorizó ninguna cuenta de esta institución.

### Aparece un error que indica que mi autorización ha caducado[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/ponto.html#i-have-an-error-about-that-my-authorization-has-expired "Enlazar permanentemente con este título")

Cada **3 meses** (90 días) debe volver a autorizar la conexión entre su cuenta bancaria y Ponto. Esto debe hacerlo desde el [sitio web de Ponto](https://myponto.com/). De lo contrario, la sincronización de cuentas se detendrá.

### Ocurren algunos errores con mi institución en estado beta[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/ponto.html#i-have-some-errors-with-my-beta-institution "Enlazar permanentemente con este título")

Ponto ofrece instituciones en _beta_ y estas no son compatibles directamente con Odoo. Le recomendamos que se ponga en contacto con Ponto.

 Importante

El uso de una institución en versión beta beneficia a Ponto, les permite tener comentarios reales sobre la conexión con la institución.