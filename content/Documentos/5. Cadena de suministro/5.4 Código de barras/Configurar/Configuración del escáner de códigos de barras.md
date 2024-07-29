Siga esta guía para elegir y configurar un escáner de códigos de barras que sea compatible con las aplicaciones _Inventario_ y _Código de barras_.

![Imagen de un ejemplo de un escáner de código de barras.](https://www.odoo.com/documentation/17.0/es/_images/barcode-scanner.png)

## Tipos de escáner[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html#scanner-types "Enlazar permanentemente con este título")

Es importante que determine qué tipo de escáner se adapta mejor a las necesidades de su negocio antes de configurar uno. Hay tres tipos principales que puede usar con Odoo y cada uno tiene sus propios beneficios y casos de uso:

- Los **escáneres USB** están conectados a una computadora y son adecuados para negocios que escanean sus productos desde una ubicación fija, como la caja de un supermercado.
    
- Los **escáneres Bluetooth** se pueden vincular con un teléfono inteligente o una tableta, lo que los convierte en la opción portátil ideal y redituable para leer códigos de barras. En este caso, Odoo está instalado en el celular, lo que permite que los operadores del almacén puedan trabajar y revisar las existencias desde sus dispositivos móviles.
    
- Los **lectores de computadora portátil** son dispositivos portátiles con un escáner de códigos de barras incorporado.
    
     Importante
    
    Si utiliza un escáner USB, asegúrese de que el escáner es compatible con la distribución del teclado de su computadora.
    
    Si utiliza un lector de computadora portátil asegúrese que el dispositivo puede ejecutar la aplicación para celulares de Odoo de forma adecuada. Los módulos más recientes que usan el sistema operativo Android con el navegador de Google Chrome o el sistema operativo Windows con Microsoft Edge, deberían funcionar. Sin embargo, como hay varios modelos y configuraciones disponibles, es importante que haga pruebas.
    

 Ver también

[Inventario y Código de barras de Odoo • Hardware compatible](https://www.odoo.com/app/inventory-hardware)

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html#configuration "Enlazar permanentemente con este título")

Al configurar el escáner de código de barras, asegúrese de que todo esté correcto para que el escáner pueda interpretar adecuadamente los códigos de barras con Odoo.

### Distribución del teclado[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html#keyboard-layout "Enlazar permanentemente con este título")

Al usar un escáner de código de barras USB, la distribución del teclado debe coincidir con la del sistema operativo para poder interpretar los caracteres de forma correcta. De manera general, el modo de escaneo debe estar configurado para aceptar un teclado USB (HID) con el lenguaje configurado según el teclado que utilice.

Para configurar la distribución del teclado para un escáner **Zebra**, escanee el código de barras que se encuentra en el teclado para el lenguaje que desee en el manual de usuario del escáner.

![Ejemplo del manual de usuario para el acomodo del teclado.](https://www.odoo.com/documentation/17.0/es/_images/keyboard-barcode.png)

Ejemplos de ajustes de lenguaje del teclado en el manual de usuario de Zebra.[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html#id1 "Enlace permanente a esta imagen")

### Retorno de carro automático[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html#automatic-carriage-return "Enlazar permanentemente con este título")

Odoo cuenta con una espera predeterminada de 100 milisegundos entre escaneos para prevenir el doble escaneado accidental. Si desea sincronizarse con el escáner de código de barras, configúrelo para que incluya un _retorno de carro_ (un caracter como la tecla «Enter» en el teclado) después de cada escaneo. Odoo interpreta el retorno de carro como el fin de la entrada del código de barras, entonces Odoo acepta el escaneo y espera al siguiente.

Por lo general en el escáner está incluido un retorno de carro de forma predeterminada. Escanee un código de barras específico del manual del usuario, como `CR suffix ON` o `Apply Enter for suffix`, para asegurarse de que está configurado.

## Escáner Zebra[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html#zebra-scanner "Enlazar permanentemente con este título")

Al usar los escáneres Zebra, asegúrese de que los ajustes de las siguientes pulsaciones estén activas para prevenir errores.

Vaya a la pantalla de inicio del escáner Zebra y seleccione la aplicación DataWedge (la aplicación cuenta con un icono que es un (código de barras azul claro)).

En la página Perfiles de DataWedge, seleccione la opción de perfil para acceder a los ajustes del escáner Zebra.

 Advertencia

No le recomendamos que use el perfil «DWDemo», pues no funciona de forma adecuada en todas las circunstancias.

Le recomendamos crear un nuevo perfil personal. Una vez que lo haya hecho, agregue la aplicación móvil de _Odoo_ y la aplicación _Google Chrome_ en la sección Aplicaciones asociadas en la pantalla de inicio del escáner.

Una vez que haya seleccionado el perfil, diríjase hacia abajo a la opción Salida del teclado y asegúrese de que la opción Habilitar/deshabilitar la salida de pulsaciones de tecla esté habilitada.

![Aspecto de la opción de pulsación en la aplicación DataWedge para el escáner Zebra.](https://www.odoo.com/documentation/17.0/es/_images/enable-keystroke.png)

Ya que habilitó esa opción, regrese a la página de opciones de Perfil y vaya a la sección Salida del teclado. Después, abra el submenú Opciones para eventos clave. Asegúrese de que la opción Enviar caracteres como eventos en Caracteres esté habilitada.

 Importante

La opción Enviar caracteres como eventos **debe** estar seleccionada en el escáner Zebra, de lo contrario, Odoo **no podrá** reconocer los códigos de barras que está escaneando.

Una vez que haya completado todos los pasos, haga una prueba y escanee un código para asegurarse de que el escáner Zebra está funcionando de forma adecuada.

## Escáner portátil Honeywell[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html#honeywell-mobile-computer-scanner "Enlazar permanentemente con este título")

Siga estas instrucciones para garantizar que pueda escanear los códigos de barras en Odoo con los escáneres Honeywell.

Vaya a la pantalla principal del escáner Honeywell y seleccione Ajustes, que es la opción representada con el icono ⚙️ (engranaje). Después, haga clic en Ajustes de Honeywell y luego en Escaneo.

Una vez allí, haga clic en Escáner interno y después en Perfil predeterminado. En la lista de opciones que aparecerá seleccione Ajustes de procesamiento de datos.

Los ajustes de procesamiento de datos especifican la forma en la que la computadora procesará los datos de los códigos de barras. Busque el ajuste Método de cuña, que de forma predeterminada está configurado como Estándar.

![Opciones de ajustes de procesamiento de datos para el escáner Honeywell.](https://www.odoo.com/documentation/17.0/es/_images/hardware-honeywell-settings.png)

Cambie el método de cuña a Teclado.

Después de completar los pasos, realice un escaneo de prueba para verificar que el escáner Honeywell funciona tal y como se espera.

## Escáner portátil Cipherlab[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/hardware.html#cipherlab-mobile-computer-scanner "Enlazar permanentemente con este título")

Siga estas instrucciones para garantizar que pueda escanear los códigos de barras en Odoo con los escáneres Cipherlab.

Vaya a la pantalla principal del escáner Cipherlab y diríjase al Administrador de aplicaciones (Todas las aplicaciones). Haga clic en la aplicación ReaderConfig, que es la opción representada con el icono naranja ⚙️ (engranaje) sobre un icono azul de (código de barras).

A continuación, seleccione el Perfil predeterminado o cree uno nuevo en caso de ser necesario.

En la sección de Ajustes generales, haga clic en Salida de datos y luego en Emulación de teclado.

![Página de ajustes de salida de datos del escáner Cipherlab.](https://www.odoo.com/documentation/17.0/es/_images/hardware-cipherlab-settings.png)

De forma predeterminada, el método de entrada disponible en Emulación de teclado está configurado como Modo predeterminado, cámbielo a KeyEvent.

![Ajustes de emulación de teclado del escáner Cipherlab.](https://www.odoo.com/documentation/17.0/es/_images/hardware-cipherlab-emulation.png)

Después de completar los pasos, realice un escaneo de prueba para verificar que el escáner Cipherlab funciona tal y como se espera.

 Ver también

[Activar los códigos de barras en Odoo](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/barcode/setup/software.html)