Starshipit es un operador de servicios de envío que facilita la integración de transportistas de la región de Australasia con Odoo. Una vez que está integrado, los usuarios pueden crear métodos de envío que obtendrán las tarifas de transportistas específicos (como Australia Post, NZ Post, DHL, entre otros) de forma automática según las condiciones predefinidas.

 Ver también

- [Calcular envíos de forma automática](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/delivery_method.html)
    
- [Integrar otros transportistas externos](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/third_party_shipper.html)
    

## Configuración en Starshipit[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#setup-in-starshipit "Enlazar permanentemente con este título")

### Crear una cuenta y activar transportistas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#create-an-account-and-activate-couriers "Enlazar permanentemente con este título")

Para comenzar, vaya a la [plataforma de Starshipit](https://starshipit.com/) para configurar su cuenta y generar las credenciales del conector. Inicie sesión con su cuenta de Starshipit o cree una si es necesario.

### Configuración de dirección de recolección[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#pickup-address-configuration "Enlazar permanentemente con este título")

Una vez que haya iniciado sesión en la cuenta de Starshipit, diríjase a Ajustes ‣ Dirección de recolección y complete la dirección de recolección. Asegúrese de que este campo coincida con la dirección del almacén.

![Agregar direcciones en los ajustes de Starshipit.](https://www.odoo.com/documentation/17.0/es/_images/starshipit-settings-address.png)

### Configuración de transportistas[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#couriers-configuration "Enlazar permanentemente con este título")

Para integrar transportistas externos, vaya a Ajustes ‣ Transportistas y seleccione Transportistas.

![Agregar direcciones en los ajustes de Starshipit.](https://www.odoo.com/documentation/17.0/es/_images/starshipit-settings-couriers.png)

 Truco

Vaya al [centro de soporte de Starshipit](https://support.starshipit.com/hc/en-us/) para obtener detalles sobre cómo integrar distintos transportistas.

### Tasas de pago[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#checkout-rates "Enlazar permanentemente con este título")

Para configurar el cálculo de las tarifas de envío vaya a Ajustes ‣ Tarifas de pago. Los costos de envío seleccionados se aplican en Odoo de forma automática al calcular los costos de envío.

![Tarifas de pago en los ajustes de Starshipit.](https://www.odoo.com/documentation/17.0/es/_images/starshipit-checkout-rate.png)

### Clave API de Starshipit[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#starshipit-api-key "Enlazar permanentemente con este título")

Configure las reglas de envío para asignar métodos de envío adecuados a las órdenes según condiciones específicas.

Para crear una regla, vaya a Ajustes ‣ Reglas y haga clic en Agregar una nueva regla.

Hay varias formas de configurar las reglas, pero le recomendamos establecer las siguientes:

1. Condición a Contiene.
    
2. Valor al código del producto.
    
3. Acción a Establecer transportista y código del producto.
    

![Reglas de envío en los ajustes de Starshipit.](https://www.odoo.com/documentation/17.0/es/_images/starshipit-rules.png)

### Ubicar las credenciales API de Starshipit[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#finding-starshipit-api-credentials "Enlazar permanentemente con este título")

En su cuenta de Starshipit vaya a Ajustes ‣ API en el menú lateral. Esta página incluye las claves API necesarias para conectarse a Odoo.

![Ubicar las claves API de Starshipit.](https://www.odoo.com/documentation/17.0/es/_images/starshipit-settings-api.png)

## Configuración en Odoo[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#setup-in-odoo "Enlazar permanentemente con este título")

### Instalación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#install "Enlazar permanentemente con este título")

Luego de configurar la cuenta de Starshipit, integre el servicio con la base de datos de Odoo. Vaya al módulo Aplicaciones de Odoo, busque el módulo Envíos con Starshipit y haga clic en Activar para instalarlo.

![Módulo Envíos con Starshipit en el módulo Aplicaciones de Odoo.](https://www.odoo.com/documentation/17.0/es/_images/starshipit-app.png)

### Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#configuration "Enlazar permanentemente con este título")

Una vez que lo haya instalado, active la función desde Inventario ‣ Configuración ‣ Ajustes. En la sección Conectores de envío active la opción Conector de Starshipit.

Después de activar el Conector de Starshipit, haga clic en el enlace Métodos de envío de Starshipit ubicado debajo del conector. Una vez en la página de Métodos de envío, haga clic en Nuevo.

 Truco

También puede acceder a los métodos de envío en Inventario ‣ Configuración ‣ Entrega ‣ Métodos de envío.

Configure Starshipit en Odoo y complete los campos en el formulario de Métodos de envío de la siguiente forma:

- Método de envío: escriba `Starshipit`.
    
- Proveedor: seleccione Starshipit en el menú desplegable.
    
- Producto de envío: asigne o cree el producto de envío que aparecerá en la línea de la orden de venta al calcular el costo de envío.
    
     Nota
    
    Los campos que aparecen en esta sección son específicos para configurar Starshipit. Para obtener más información sobre los otros campos, consulte [Métodos de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/delivery_method.html).
    

En la pestaña Configuración de Starshipit deberá completar los siguientes campos:

- Clave API de Starshipit: escriba la clave API [obtenida de Starshipit](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#inventory-shipping-receiving-star-api).
    
- Clave de suscripción de Starshipit: escriba la clave de suscripción obtenida del mismo lugar que la [clave API](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#inventory-shipping-receiving-star-api).
    
- Dirección de origen: escriba la dirección desde donde se envían los productos. Este campo es esencial para calcular las tarifas de envío y [generar etiquetas de envío](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#inventory-shipping-receiving-star-label).
    
- Tipo de paquete predeterminado: establezca un tipo de paquete predeterminado para incluir el peso del paquete vacío al calcular de forma automática las tarifas de envío.
    

 Importante

Para establecer un tipo de paquete predeterminado, la función _Paquetes_ **debe** estar habilitada en Inventario ‣ Configuración ‣ Ajustes.

- Guarde el formulario de forma manual al hacer clic en el icono de nube a lado de las migas de pan Métodos de envío / Nuevo.
    

Para cargar los productos de envío recién configurados, haga clic en el enlace Seleccionar un servicio vinculado a la cuenta de Starshipit ubicado en la parte inferior de la pestaña Configuración de Starshipit.

Esto abrirá la ventana emergente Elija un servicio de envío de Starshipit. En el campo Servicio de entrega, seleccione el servicio de envío deseado para entregas y devoluciones desde el menú desplegable. Por último, haga clic en Confirmar.

El servicio de entrega seleccionado aparecerá en el campo Nombre del servicio.

 Example

Ejemplo de un producto de envío de Starshipit configurado en Odoo:

Sendle: Sendle drop off.

Producto de envío: `Sendle Delivery`.

Código de servicio de Starshipit: `STANDARD-DROPOFF`.

![Ejemplo de productos de envío configurados en Odoo:](https://www.odoo.com/documentation/17.0/es/_images/starshipit-configuration.png)

 Truco

Starshipit no proporciona claves de prueba para que las empresas prueben el envío de paquetes en Odoo. Esto quiere decir que podría recibir un cargo en su cuenta si crea un paquete.

Odoo tiene una capa de protección incorporada contra cargos no deseados al usar entornos de prueba. Si se encuentra dentro de un entorno de prueba y utiliza un método de envío para crear etiquetas, esas etiquetas se cancelan de forma automática después de su creación. Tenga en cuenta que, según el proveedor de envío que haya usado, podrían hacer un cobro en su cuenta por la impresión de la etiqueta a menos que cancele la orden en el portal del transportista de forma manual.

Puede alternar entre el entorno de prueba y de producción si hace clic en el botón inteligente Entorno ubicado en la parte superior del formulario del método de envío.

### Generar una etiqueta con Starshipit[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#generate-a-label-with-starshipit "Enlazar permanentemente con este título")

Al crear una cotización en Odoo podrá agregar el método de envío Starshipit si hace clic en el botón Agregar envío.

Seleccione Starshipit en el campo Método de envío de la ventana emergente Agregar un método de envío.

Haga clic en Obtener tarifa para calcular la tarifa de envío y, por último, haga clic en Agregar para incluir el costo del envío en la línea de la orden de venta, aparecerá como el _producto de envío_.

 Nota

Calcule los costos de envío para Starshipit de forma automática en **ambas** aplicaciones de Odoo, tanto en _Ventas_ como en _Comercio electrónico_.

Después, valide la entrega. Los documentos de la etiqueta de envío se generan en el chatter de forma automática e incluyen lo siguiente:

1. Etiqueta(s) de envío según el número de paquetes.
    
2. Números de seguimiento si el transportista seleccionado es compatible con ellos.
    
3. Etiquetas de devolución si el conector de Starshipit está configurado para devoluciones.
    

![Ejemplo de una orden enviada en Odoo.](https://www.odoo.com/documentation/17.0/es/_images/starshipit-shipping.png)

 Importante

El peso del paquete en Odoo se calcula al sumar los pesos de los productos más el peso del paquete vacío almacenado en la base de datos. Asegúrese de seleccionar la opción de envío correcta, ya que el peso del paquete no se verifica en automático.

Verifique la dirección de destino, ya que Starshipit la verifica cuando se crea la orden.

Por último, algunos transportistas pueden necesitar de otra información, como una dirección de correo electrónico o un número de teléfono. Asegúrese de que toda la información necesaria está configurada al enviar una orden de envío.

### Devoluciones[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#returns "Enlazar permanentemente con este título")

Starshipit permite devoluciones con los siguientes transportistas:

- Australia Post eParcel
    
- TNT
    
- Couriers Please
    
- Aramex
    
- StarTrack
    
- DHL Express
    
- NZ Post Domestic
    

Puede crear una si hace clic en el botón inteligente Devolver ubicado en la orden de entrega correspondiente. El botón Imprimir etiqueta de devolución estará disponible en caso de que el transportista seleccionado admita devoluciones.

### Cancelaciones[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/shipping_receiving/setup_configuration/starshipit_shipping.html#cancellations "Enlazar permanentemente con este título")

Si cancela una orden de envío en Odoo, esta se archivará de forma automática en Starshipit. Sin embargo, la cancelación no se enviará al transportista, así que asegúrese de iniciar sesión en la plataforma del transportista para gestionar la cancelación manualmente.