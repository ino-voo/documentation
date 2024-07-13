[Adyen](https://www.adyen.com/) es una empresa neerlandesa que ofrece varias posibilidades de pago en línea.

 Ver también

- [Activar un proveedor de pago](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-add-new)
    
- [Pagos en línea](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html)
    

 Nota

Adyen solo trabaja con clientes que procesan **más** de **10 millones anualmente** o que facturan un **mínimo** de **1.000** transacciones **al mes**.

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#configuration "Enlazar permanentemente con este título")

 Ver también

[Activar un proveedor de pago](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-add-new)

Primero, contacte el soporte de Adyen para que activen multiple partial capture (varias capturas parciales) en su cuenta.

### Pestaña de credenciales[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#credentials-tab "Enlazar permanentemente con este título")

Odoo necesita sus **credenciales API** para conectarse con su cuenta de Adyen, las cuales incluyen:

- **Cuenta de comerciante**: el código de la cuenta de comerciante que se usará con Adyen.
    
- [Clave API](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#adyen-api-and-client-keys): La clave API del usuario del servicio web.
    
- [Clave de cliente](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#adyen-api-and-client-keys): la clave de cliente del usuario de servicio web.
    
- [Clave HMAC](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#adyen-hmac-key): la clave HMAC (código de autorización de mensajes basado en hash, por su siglas en inglés) del webhook.
    
- [URL de API de pago](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#adyen-urls): el URL base para los puntos finales del API de pago.
    
- [URL de API recurrente](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#adyen-urls): el URL base para los puntos finales de API recurrente.
    

Puede copiar las credenciales de su cuenta de Adyen y pegarlas en los campos relacionados en la pestaña de **Credenciales**.

 Importante

Si está usando Adyen como prueba con una _cuenta de prueba_ de Adyen, vaya a Contabilidad ‣ Configuración ‣ Proveedores de pago. Haga clic en Adyen, activar Modo de prueba e ingrese sus credenciales en la pestaña de Credenciales.

#### Clave API y clave de cliente[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#api-key-and-client-key "Enlazar permanentemente con este título")

Para obtener su Clave API y su Clave de cliente, inicie sesión en su cuenta de Adyen y vaya a Desarrolladores ‣ Credenciales API.

- Si ya tiene un usuario API, ábralo.
    
- Si todavía no tiene un usuario API, haga clic en **Crear nuevas credenciales**.
    

Vaya a Ajustes del servidor ‣ Autenticación y copie o genere su **clave API**. Asegúrese de copiar su clave API pues no podrá obtenerla después sin generar una nueva.

Ahora vaya a Configuración del cliente ‣ Autenticación y copie o genere su **clave de cliente**. Aquí también puede [permitir que se hagan pagos desde su sitio web](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#adyen-allowed-origins).

#### Clave HMAC[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#hmac-key "Enlazar permanentemente con este título")

Para obtener la clave HMAC, necesitará configurar un webhook de `Notificación estándar`. Para hacer esto, inicie sesión en su cuenta de Adyen y vaya a Desarrolladores ‣ Webhooks ‣ Agregar webhook ‣ Agregar notificación estándar.

![Configure un webhook.](https://www.odoo.com/documentation/17.0/es/_images/adyen-add-webhook.png)

Ahí, en General ‣ Configuración del servidor ‣ URL, ingrese la dirección de su servidor seguido de `/payment/adyen/notification`.

![Ingrese la notificación URL.](https://www.odoo.com/documentation/17.0/es/_images/adyen-webhook-url.png)

Luego, vaya a Seguridad ‣ Clave HMAC ‣ Generar. Tenga cuidado y copie la clave pues no se le permitira hacerlo después sin generar una nueva.

![Genere una clave HMAC y guárdela.](https://www.odoo.com/documentation/17.0/es/_images/adyen-hmac-key.png)

Debe guardar el webhook para finalizar su creación.

#### URL de las API[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#api-urls "Enlazar permanentemente con este título")

Todas las URLs de las API de Adyen incluyen un prefijo específico de cada área del cliente que genera Adyen. Para configurar las URLs, siga los siguientes pasos:

1. Inicie sesión en su cuenta de Adyen y vaya a Desarrolladores ‣ URLs de las API.
    
2. Copie el prefijo para su área de cliente en directo (por ejemplo, **centro de datos**) y guárdela para después.
    
    ![Copie el prefijo para las APIs de Adyen](https://www.odoo.com/documentation/17.0/es/_images/adyen-api-urls.png)
    
3. En Odoo, [vaya al proveedor de pago Adyen](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-add-new).
    
4. En el campo URL de la API de pago, ponga la siguiente URL y reemplace `yourprefix` por el prefijo que guardo anteriormente: `https://yourprefix-checkout-live.adyenpayments.com/checkout`
    
5. En el campo URL recurrente de las API, ponga la siguiente URL y reemplace `yourprefix` con el prefijo que guardo anteriormente: `https://yourprefix-pal-live.adyenpayments.com/pal/servlet/Recurring`.
    

 Nota

Si está usando Adyen en modo de prueba, puede usar la siguiente URL en su lugar:

- URL de la API de pago: `https://checkout-test.adyen.com`
    
- URL recurrente de la API: `https://pal-test.adyen.com/pal/servlet/Recurring`
    

### Cuenta de Adyen[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#adyen-account "Enlazar permanentemente con este título")

#### Permitir pagos de un origen específico[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#allow-payments-from-a-specific-origin "Enlazar permanentemente con este título")

Para permitir pagos originados desde su sitio web, siga los pasos de [Clave API y clave de cliente](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#adyen-api-and-client-keys) para ir a su usuario de API y vaya a Agregar origenes permitidos, luego agregue las URL desde donde se realizaran los pagos (las URL de los servidores que alojan sus instancias de Odoo).

![Permite pagos originados desde un dominio específico.](https://www.odoo.com/documentation/17.0/es/_images/adyen-allowed-origins.png)

### Hacer una retención de tarjeta de crédito[](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers/adyen.html#place-a-hold-on-a-card "Enlazar permanentemente con este título")

Adyen le permite capturar un importe manualmente en lugar de hacer una directa.

Para establecer la cuenta pendiente, active la opción **Capturar importe manualmente** en Odoo, como se explica en [documentación sobre los proveedores de pago](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html#payment-providers-manual-capture).

Luego, abra su Cuenta de comerciante de Adyen y vaya a Cuenta ‣ Configuración, y cambie de **atraso de captura** a **manual**.

![Configuración del retraso de captura en Adyen](https://www.odoo.com/documentation/17.0/es/_images/adyen_capture_delay.png)

 Prudencia

- Si configura Odoo para realizar las capturas manualmente, asegúrese de establecer el **Retraso de captura** a **manual** en Adyen. De lo contrario, la transacción se bloqueará en el estado de autorizado en Odoo.
    

 Nota

- Después de **7 días** si todavía no se ha capturado la transacción, el cliente tiene derecho de **revocarla**.
    

 Ver también

[Pagos en línea](https://www.odoo.com/documentation/17.0/es/applications/finance/payment_providers.html)