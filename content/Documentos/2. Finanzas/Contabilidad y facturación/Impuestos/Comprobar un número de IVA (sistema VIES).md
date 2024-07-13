El [sistema de intercambio de información sobre el IVA](https://ec.europa.eu/taxation_customs/vies/#/vat-validation)», o **VIES**, es una herramienta facilitada por la Comisión Europea que le permite verificar la validez de los números de IVA de las empresas registradas en la Unión Europea.

Nuestra función de validación de IVA utiliza el VIES para verificar los números de sus contactos desde la interfaz de Odoo.

 Nota

No importa si esta función está habilitada o no, Odoo verifica el formato del número de identificación tributaria de un contacto en comparación con el [formato esperado de los números](https://es.wikipedia.org/wiki/Identificaci%C3%B3n_tributaria_en_la_Uni%C3%B3n_Europea#Identificaci%C3%B3n_tributaria_a_efectos_del_IVA_intracomunitario) de ese país.

## Verificación de números tributarios con VIES[](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/vat_verification.html#vies-vat-number-verification "Enlazar permanentemente con este título")

Para activar esta función, vaya a Contabilidad ‣ Configuración ‣ Ajustes. En la sección Impuestos, habilite la función Verificar números tributarios y haga clic en guardar.

Una vez que haya habilitado la función Verificar números tributarios, si el campo correspondiente para el número tributario del contacto está completado _y_ su país es diferente al de su empresa, Odoo muestra la casilla Válido dentro de la Comunidad Europea, luego prueba el número a través de VIES y marca o desmarca de forma automática la casilla anterior según su validez.

![Casilla de Válido dentro de la Comunidad Europea en el registro del contacto](https://www.odoo.com/documentation/17.0/es/_images/intra-community-valid.png)

 Importante

Puede anular el campo Válido dentro de la Comunidad Europea en el contacto en caso de que la comprobación automática VIES sea incorrecta (por ejemplo, si se constituyó la empresa recientemente y el número de identificación fiscal aún no está en el VIES). Este cambio se registra en el chatter por motivos de transparencia.

 Nota

Odoo puede [aplicar automáticamente posiciones fiscales](https://www.odoo.com/documentation/17.0/es/applications/finance/accounting/taxes/fiscal_positions.html#fiscal-positions-automatic). Si la función Verificar NIFs está activada, cualquier posición fiscal que tenga necesite un NIF, requerirá números NIF válidos dentro de la Comunidad Europea para que aplique de manera automática.