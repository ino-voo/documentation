En fabricación, la _subcontratación_ es el proceso que una empresa lleva a cabo cuando contrata a un fabricante externo, o subcontratista, para que fabrique los productos que luego venderá la empresa contratante.

La subcontratación proporciona varios beneficios tanto para la empresa contratante como para la empresa subcontratista.

En el caso de la empresa contratante, la subcontratación les permite vender varios productos fabricados sin tener que preocuparse por invertir y dar mantenimiento al equipo y la mano de obra necesarios para gestionar la fabricación por su cuenta.

Esto ayuda a que las empresas contratantes se adapten a lo largo de los ciclos económicos, ya que pueden incrementar o disminuir los compromisos que tienen con los subcontratistas con facilidad según sea necesario en el momento adecuado. También significa que pueden enfocarse en las tareas en las que se distinguen y delegar los trabajos más especializados a los subcontratistas.

Por otro lado, la subcontratación permite que los subcontratistas se especialicen en áreas más específicas de la producción que podrían no ser tan rentables si no utilizaran el proceso de subcontratación. En algunos casos, también les proporciona flexibilidad para que elijan los proyectos que aceptan o rechazan y en cuántos de ellos trabajan en un momento determinado.

En Odoo, las empresas pueden configurar sus flujos de trabajo de subcontratación según varios factores, como la manera en que obtienen los componentes y qué sucede con los productos terminados una vez que se fabrican.

[

#### Basic subcontracting

Subcontract products without supplying the subcontractor with components.



](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html)[

#### Resupply subcontractor

Ship components to a subcontractor each time a PO for a subcontracted product is confirmed.



](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html)[

#### Dropship to subcontractor

Dropship components to a subcontractor each time a PO for a subcontracted product is confirmed.



](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html)

## Configuración[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting.html#configuration "Enlazar permanentemente con este título")

Para habilitar la subcontratación en Odoo, vaya a Fabricación ‣ Configuración ‣ Ajustes y, en la sección Operaciones, seleccione la casilla ubicada junto a Subcontratación. Haga clic en Guardar.

![Los ajustes de subcontratación en la aplicación Fabricación.](https://www.odoo.com/documentation/17.0/es/_images/subcontracting-setting.png)

Una vez que haya habilitado la subcontratación, Odoo mostrará varias funciones disponibles:

- En las listas de materiales, el campo _Tipo de LdM_ ahora incluye la opción de _subcontratación_. Habilitar el tipo de LdM de _subcontratación_ designa el producto de la lista como un producto subcontratado, es decir, Odoo sabe que lo produce un subcontratista y no la empresa propietaria de la base de datos.
    
- En la aplicación _Inventario_ estarán disponibles dos rutas de subcontratación. Es posible usarlas en productos específicos en la pestaña _Inventario_ de sus respectivas páginas:
    
    - _Reabastecer al subcontratista al ordenar_
        
    - _Enviar al subcontratista al ordenar_
        

## Flujos de trabajo de subcontratación[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting.html#subcontracting-workflows "Enlazar permanentemente con este título")

En Odoo hay tres flujos de trabajo de subcontratación. La diferencia principal entre ellos es la _manera_ en la que el subcontratista adquiere los productos necesarios:

- En el flujo de trabajo de subcontratación _básica_, el subcontratista es el responsable de obtener los componentes. Este flujo de trabajo se describe en la documentación sobre [Subcontratación básica](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_basic.html).
    
- En el flujo de trabajo _Reabastecer al subcontratista al ordenar_, la empresa contratante le envía los componentes de su almacén al subcontratista. Este flujo de trabajo se describe en la documentación sobre [Reabastecer al subcontratista](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_resupply.html).
    
- En el flujo de trabajo _Enviar al subcontratista al ordenar_, la empresa contratante le compra los componentes a un proveedor y hace que se los entreguen al subcontratista. Este flujo de trabajo se describe en la documentación sobre [Enviar al subcontratista](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting/subcontracting_dropship.html).
    

Además de la forma en que un subcontratista obtiene los componentes, también es necesario considerar el motivo por el que un producto está siendo subcontratado, así como lo que sucede con los productos después de que el subcontratista los fabrica.

Los dos motivos principales por los que un producto se subcontrata son para cumplir con la orden de un cliente o para reabastecer la cantidad de existencias disponibles.

Luego de que un producto es fabricado, el subcontratista podrá enviarlos a la empresa contratista o enviarlo directamente a un consumidor final.

Es posible configurar los tres flujos de trabajo de subcontratación descritos con anterioridad para facilitar cualquiera de estas posibilidades, y los métodos para hacerlo están descritos en su documentación.

## Valoración de productos subcontratados[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/manufacturing/subcontracting.html#subcontracted-product-valuation "Enlazar permanentemente con este título")

La valoración de un producto subcontratado depende de algunas variables:

- El costo de los componentes necesarios si los proporciona la empresa contratante, corresponde a la letra `C`.
    
- El precio pagado al subcontratista por el servicio de fabricación del producto subcontratado, corresponde a la letra `M`.
    
- El costo de envío de los componentes al subcontratista y el envío de regreso a la empresa contratante, corresponde a la letra `S`.
    
- El costo por envío directo si los componentes los envía el subcontratista al cliente final, corresponde a la letra `D`.
    
- Todos los costos asociados, como impuestos por importación, entre otros, corresponde a la letra `x`.
    

Por lo tanto, es posible representar la valoración total de un producto subcontratado (`P`) con la siguiente ecuación:

P=C+M+S+D+x

Es importante mencionar que no todas las valoraciones de los productos subcontratados incluirán estas variables. Por ejemplo, si el producto no se entrega al consumidor final, entonces no es necesario tomar en cuenta el costo de la triangulación.