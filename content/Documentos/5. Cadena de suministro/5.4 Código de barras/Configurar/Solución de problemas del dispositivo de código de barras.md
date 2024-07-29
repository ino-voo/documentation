La aplicación _Código de barras_ de Odoo es compatible con tres tipos principales de códigos de barras: lectores USB, lectores Bluetooth y lectores móviles de computadora. Al configurar cada tipo de lector, hay errores comunes que pueden surgir en los que los lectores no funcionarán como deberían y Odoo regresa un error al dispositivo.

Lea las siguientes secciones para identificar los problemas generales y únicos de los dispositivos relacionados a los tipos de lectores más comunes.

## Problemas generales[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#general-issues "Enlazar permanentemente con este título")

Consulte las secciones siguientes para conocer los problemas más comunes relacionados con los dispositivos de lector de códigos de barras más conocidos.

Para problemas relacionados con dispositivos específicos, consulte la sección [Lectores Android](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#barcode-setup-android-scanners) para lectores de ordenadores móviles, o la sección [lectores sin pantalla](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#barcode-setup-screenless-scanners) para lectores USB y bluetooth.

### No se puede leer el código de barras[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#barcode-cannot-be-read "Enlazar permanentemente con este título")

Uno de los problemas comunes que surge cuando se usan escáneres de código de barras es que no se puede leer un código de barras.

Esto puede ocurrir por una de las siguientes razones:

- El código de barras está dañado.
    
- El dispositivo no puede leer el tipo de código de barras requerido (algunos lectores solo pueden leer códigos de barra 2D).
    
- El código de barras que se está escaneando está en una pantalla. Algunos lectores no pueden hacer esto, por lo que los códigos de barra **se deben** imprimir para poder escanearse. Esto es my común con códigos de barra 1D.
    
- El dispositivo no tiene baterías o está rota. Para descartar este caso debe seguir las instrucciones de solución de problemas que se presentan en las siguientes secciones.
    

### Odoo muestra un error de código de barras[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#odoo-returns-barcode-error "Enlazar permanentemente con este título")

Todos los tipos de lectores de código de barras tienen su propio «lenguaje» de dispositivo que afecta a cómo envían los datos de código de barras a la aplicación _Código de barras_ de Odoo. A veces, esto puede causar que la aplicación _Código de barras_ de Odoo devuelva un error de código de barras después de escanear. Esto puede ser debido a cualquiera de las siguientes razones:

- La computadora está configurada con una distribución de teclado diferente a la del lector de código de barras. Para descartar esto, asegúrese de que el dispositivo esté configurado con la misma distribución de teclado.
    
    Por ejemplo, si la computadora está configurada para usar un teclado FR-BE, configure el lector para que envíe pulsaciones de teclas FR-BE. La misma lógica aplica si usa una tableta en lugar de una computadora.
    
    Para más información sobre la configuración de pulsaciones de teclado, consulte la documentación sobre [la configuración del lector de código de barras](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html).
    
- En el caso de los lectores de ordenadores portátiles (como los dispositivos Zebra, por ejemplo), es posible que el escáner interprete el código de barras de forma distinta a la prevista. Para descartar esta posibilidad, escanee un código de barras de prueba para ver cómo interpreta el lector el código de barras.
    

## Escáneres Android[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#android-scanners "Enlazar permanentemente con este título")

La mayoría de los modelos de lectores de código de barras más recientes que usan Android y Google Chrome. Sin embargo, debido a la amplia variedad de modelos y configuraciones, recomendamos primero probar que el lector sí sea compatible con Odoo.

Recomendamos la línea de productos Zebra, específicamente el **Zebra TC21 (Wi-Fi-only)** y **Zebra TC26 (WiFi/cellular)**.

 Ver también

[Hardware compatible con las aplicaciones Inventario y Código de barras de Odoo](https://www.odoo.com/app/inventory-hardware)

### La aplicación Código de barras no responde[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#barcode-app-does-not-give-feedback "Enlazar permanentemente con este título")

De forma predeterminada, los lectores de código de barras de Android preprocesan los códigos de barras y después envían un texto completo. La aplicación _Código de barras_ de Odoo no lee este tipo de respuesta, así que los ajustes para cada tipo de lector **deben** ser los adecuados.

La aplicación _Código de barras_ de Odoo espera que el escáner funcione como un teclado análogo, por lo que solo detecta _eventos de tecla_. Consulte las siguientes secciones para saber cómo configurar los dispositivos más comunes.

### Zebra TC21 y TC26[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#zebra-tc21-tc26 "Enlazar permanentemente con este título")

Al usar los escáneres Zebra, asegúrese de que los ajustes de las siguientes pulsaciones estén activas para prevenir errores.

Vaya a la pantalla de inicio del escáner Zebra y seleccione la aplicación DataWedge (la aplicación cuenta con un icono que es un (código de barras azul claro)).

En la página Perfiles de DataWedge, seleccione la opción de perfil para acceder a los ajustes del escáner Zebra.

Una vez que haya seleccionado el perfil, diríjase hacia abajo a la opción Salida del teclado y asegúrese de que la opción Habilitar/deshabilitar la salida de pulsaciones de tecla esté habilitada.

![Aspecto de la opción de pulsación en la aplicación DataWedge para el escáner Zebra.](https://www.odoo.com/documentation/17.0/es/_images/device-troubleshooting-zebra-settings.png)

Ya que habilitó esa opción, regrese a la página de opciones de Perfil y vaya a la sección Salida del teclado. Después, abra el submenú Opciones para eventos clave. Asegúrese de que la opción Enviar caracteres como eventos en Caracteres esté habilitada.

 Importante

La opción Enviar caracteres como eventos **debe** estar seleccionada en el escáner Zebra, de lo contrario, Odoo **no podrá** reconocer los códigos de barras que está escaneando.

Una vez que haya completado todos los pasos, haga una prueba y escanee un código para asegurarse de que el escáner Zebra está funcionando de forma adecuada.

### Dispositivos MUNBYN Android[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#munbyn-android-devices "Enlazar permanentemente con este título")

Al usar los escáneres MUNBYN Android, asegúrese de que los ajustes de las siguientes pulsaciones estén activas para prevenir errores.

Desde la pantalla principal del dispositivo haga clic en AppSettings (ajustes de la aplicación). En la página a la que llegue vaya a la sección Process mode (modo de procesamiento) y haga clic en Keyboard input (entrada de teclado).

![Sección de modo de procesamiento en la página de ajustes de la aplicación de MUNBYN.](https://www.odoo.com/documentation/17.0/es/_images/device-troubleshooting-munbyn-process-mode.png)

 Truco

El _modo de procesamiento_ seleccionado controla cómo se procesa la información después de que se hayan leído los datos.

_Entrada de teclado_ introduce datos de lectura en la posición del cursor, igual que lo haría la entrada de datos en un teclado analógico.

Una vez que haya completado todos los pasos, haga una prueba y escanee un código para asegurarse de que el escáner MUNBYN Android está funcionando de forma adecuada.

 ¿Por qué no recibo información en la aplicación después de un escaneo exitoso?

Al escanear un código de barras, el escáner puede hacer un sonido que indica que se logró escanear bien, sin embargo no se recibe información en la aplicación.

Para solucionar este problema, ajusta el método de salida a _teclado analógico_ en la aplicación _Escáner_ del dispositivo.

Desde la página principal del dispositivo haga clic en la aplicación del Escáner ‣ Ajustes. Desde la página Ajustes haga clic en Método de salida. La ventana emergente resultada muestra diferentes opciones de entrada disponibles para los usuarios. Seleccione Modo de teclado y haga clic en OK.

![Ventana emergente del modo de salida en el escáner MUNBYN.](https://www.odoo.com/documentation/17.0/es/_images/device-troubleshooting-output-mode-popup.png)

Regrese a la aplicación que necesita escanearse y haga clic en el cuadro de diálogo de entrada antes de escanear. Haga un escaneo de prueba para asegurarse de que el escáner MUNBYN Android funcione.

### Dispositivos Android Datalogic[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#datalogic-android-devices "Enlazar permanentemente con este título")

Al usar los escáneres Datalogic Android, asegúrese de que los ajustes de las siguientes pulsaciones estén activas para prevenir errores.

Para ver y configurar todos los ajustes del escáner, use la aplicación _Ajustes_ en el dispositivo Datalogic Android. Desde el menú de aplicaciones, seleccione Ajustes ‣ Sistema ‣ Ajustes del escáner.

En la lista de ajustes que verá, seleccione Wedge. Desde este menú, en la sección Keyboard wedge asegúrese de que la función Enable keyboard wedge esté activada.

Después, también en esta sección, ubique la opción Keyboard wedge input mode. En automático, el modo de entrada será Text injection.

![Menú de configuración Wedge en el escáner Datalogic.](https://www.odoo.com/documentation/17.0/es/_images/device-troubleshooting-wedge-menu.png)

Haga clic en Keyboard wedge input mode y cambie el ajuste a Key pressure. De esta forma nos aseguramos de que los códigos de barra escaneados se traducen a teclas, en lugar de que se inyecten en el área de texto.

![Selección del modo de entrada Keyboard wedge en el escáner Datalogic.](https://www.odoo.com/documentation/17.0/es/_images/device-troubleshooting-keyboard-wedge-input.png)

Una vez que haya completado todos los pasos, haga una prueba y escanee un código para asegurarse de que el escáner Datalogic Android está funcionando de forma adecuada.

## Escáneres sin pantalla[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#screenless-scanners "Enlazar permanentemente con este título")

Este tipo de escáneres no tienen pantalla e incluyen los escáneres USB y bluetooth.

 Importante

Odoo es compatible con la mayoría de los escáneres USB y Bluetooth, ya que todos emulan un teclado. Sin embargo, para asegurarse de que el escáner es compatible con una distribución de teclado específica (o que se puede configurar para que lo sea) consulte la documentación de Odoo sobre [hardware de inventario y códigos de barra compatibles](https://www.odoo.com/app/inventory-hardware)

### Dispositivos NETUM[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/device_troubleshooting.html#netum-devices "Enlazar permanentemente con este título")

El manual de usuario del escáner de códigos de barras NETUM solo muestra la configuración del teclado en francés de forma predeterminada. Escanee el siguiente código para usar el teclado belga:

![Código de barras para el teclado belga FR.](https://www.odoo.com/documentation/17.0/es/_images/device-troubleshooting-belgium-fr-key.png)

Una vez que se haya escaneado el código, asegúrese que el escáner NETUM tenga la configuración de teclado correcta y que esté funcionando como se espera.

 Ver también

- [Configuración del escáner de códigos de barras](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html)
    
- [Activar los códigos de barras en Odoo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/software.html)