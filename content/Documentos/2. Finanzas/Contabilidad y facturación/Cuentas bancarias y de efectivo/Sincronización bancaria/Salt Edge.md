**Salt Edge** es un proveedor externo que agrega información bancaria de sus cuentas. Es compatible con cerca de 5000 instituciones en más de 50 países.

![Logotipo de Salt Edge](https://www.odoo.com/documentation/17.0/es/_images/saltedge-logo.png)

Odoo se puede sincronizar directamente con su banco para obtener todos los estados de cuenta bancarios importados de manera automática a su base de datos.

 Ver también

- [Sincronización bancaria](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization.html)
    
- [Transacciones](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/transactions.html)
    

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/saltedge.html#configuration "Enlazar permanentemente con este título")

### Vincular las cuentas bancarias con Odoo[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/saltedge.html#link-your-bank-accounts-with-odoo "Enlazar permanentemente con este título")

1. Para iniciar con la sincronización, haga clic en Contabilidad ‣ Configuración ‣ Agregar una cuenta bancaria.
    
2. Seleccione la institución que desea sincronizar. Para ver si Salt Edge es el proveedor externo de la institución solo tiene que seleccionarla.
    
3. Después de proporcionar su número de teléfono, se le solicitará una dirección de correo electrónico. Esta dirección de correo electrónico se utilizará para crear su cuenta de Salt Edge. Asegúrese de ingresar una dirección de correo electrónico válida, de lo contrario, no podrá acceder a su cuenta de Salt Edge.
    
    ![Dirección de correo electrónico que debe proporcionar a Salt Edge para la creación de su cuenta.](https://www.odoo.com/documentation/17.0/es/_images/saltedge-contact-email.png)
    
4. Después de ingresar su dirección de correo electrónico, se le redirigirá a Salt Edge para continuar con el proceso de sincronización.
    
    ![Página de inicio de sesión de Salt Edge.](https://www.odoo.com/documentation/17.0/es/_images/saltedge-login-page.png)
    
5. Asegúrese de marcar la casilla para dar su consentimiento.
    
    ![Página de consentimiento de Salt Edge.](https://www.odoo.com/documentation/17.0/es/_images/saltedge-give-consent.png)
    
6. Siga los pasos para completar la sincronización.
    

### Actualizar sus credenciales[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/saltedge.html#update-your-credentials "Enlazar permanentemente con este título")

Es posible que deba actualizar sus credenciales de Salt Edge o modificar los ajustes de sincronización.

Para hacerlo, vaya a Contabilidad -> Configuración -> Sincronización en línea y seleccione la institución donde desea actualizar las credenciales. Haga clic en el botón _Actualizar credenciales_ para iniciar el flujo y siga los pasos.

No olvide marcar la casilla de verificación de consentimiento. De lo contrario, es posible que Odoo no pueda acceder a su información.

### Obtener cuentas nuevas[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/saltedge.html#fetch-new-accounts "Enlazar permanentemente con este título")

Es posible que desee agregar nuevas cuentas en línea a su conexión.

Vaya a Contabilidad -> Configuración -> Sincronización en línea y seleccione la institución para buscar las cuentas nuevas. Haga clic en el botón _Obtener cuentas_ para iniciar el flujo y siga los pasos.

No olvide marcar la casilla de verificación de consentimiento. De lo contrario, es posible que Odoo no pueda acceder a su información.

## Preguntas frecuentes[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/saltedge.html#faq "Enlazar permanentemente con este título")

### Aparece un error cuando intento eliminar la sincronización dentro de Odoo[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/saltedge.html#i-have-an-error-when-i-try-to-delete-my-synchronization-within-odoo "Enlazar permanentemente con este título")

Odoo no puede eliminar de forma permanente la conexión que creó con la institución bancaria. Sin embargo, puede revocar el consentimiento que proporcionó para que Odoo ya no tenga acceso a su cuenta. Es probable que el error que está viendo sea un mensaje que menciona que se revocó el consentimiento, pero que el registro no se pudo eliminar porque todavía existe dentro de Salt Edge. Si desea eliminar la conexión por completo, entre a su [cuenta de Salt Edge](https://www.saltedge.com/dashboard) y elimine su sincronización de forma manual. Una vez hecho esto, puede volver a Odoo para eliminar el registro.

### Aparece un error en el que dice que ya sincronicé esta cuenta[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/bank/bank_synchronization/saltedge.html#i-have-an-error-saying-that-i-have-already-synchronized-this-account "Enlazar permanentemente con este título")

Es probable que ya haya sincronizado su cuenta bancaria con Salt Edge, verifique en su [tablero](https://www.saltedge.com/dashboard) que no tiene una conexión con las mismas credenciales.

En caso de que ya tenga una sincronización con las mismas credenciales en su tablero de Salt Edge y que no se haya creado con Odoo, elimínela y créela desde su base de datos de Odoo.

En caso de que ya tenga una conexión con las mismas credenciales presentes en su tablero de Salt Edge y la sincronización se haya creado con Odoo, por lo general podrá encontrarla si se dirige a Contabilidad ‣ Configuración ‣ Sincronización en línea. Asegúrese de realizar una _actualización de credenciales_ para reactivar la conexión.