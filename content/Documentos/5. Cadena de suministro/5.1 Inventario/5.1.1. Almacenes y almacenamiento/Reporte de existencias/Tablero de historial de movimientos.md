El reporte de _historial de movimientos_ de la aplicación _Inventario_ proporciona un registro detallado del movimiento de los productos (incluye ubicaciones anteriores y actuales), números de lote y los motivos correspondientes al mismo. Es posible generar reportes para cualquier periodo de tiempo, así que este reporte es indispensable para analizar los niveles de existencias, monitorear la rotación de inventario e identificar cualquier discrepancia en él.

 Nota

Solo los usuarios con [acceso de administrador](https://www.odoo.com/documentation/17.0/es/applications/general/users/access_rights.html) pueden acceder a las funciones de reportes.

Vaya a Inventario ‣ Reportes ‣ Historial de movimientos para consultar el reporte correspondiente.

![Mostrar el reporte de historial de movimientos.](https://www.odoo.com/documentation/17.0/es/_images/moves-history.png)

## Explorar el reporte de historial de movimientos[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/moves_history.html#navigate-the-moves-history-report "Enlazar permanentemente con este título")

En el reporte aparecen las siguientes columnas para representar la información adecuada:

- Fecha: la fecha y hora del movimiento de existencias.
    
- Referencia: descripción del motivo del movimiento de existencias o del cambio de cantidad, como un número de recepción (por ejemplo, `WH/IN/00012`).
    
- Producto: el nombre del producto relacionado con el movimiento.
    
- Número de serie/lote: especifica el número de serie o lote del producto rastreado que se está moviendo.
    
- Desde: la ubicación de origen del producto movido.
    
- A: la ubicación de destino del producto movido.
    
- Cantidad: el número de productos movidos.
    
- Unidad: unidad de medida de los productos movidos.
    
- Estado: indica el estado del movimiento, este puede ser Hecho, Disponible (listo) o Parcialmente disponible (no hay cantidades suficiente para completar la operación).
    

### Opciones de búsqueda[](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/reporting/moves_history.html#search-options "Enlazar permanentemente con este título")

Use las siguientes opciones de búsqueda para personalizar el reporte de historial de movimientos y que incluya la información relevante.

FiltersGroup ByFavorites

La sección de Filtros permite que los usuarios busquen entre filtros predefinidos y personalizados para encontrar registros específicos de las existencias.

- Por hacer: mostrar registros de movimientos de existencias que están en progreso. Esto incluye las líneas con el valor Disponible o Parcialmente disponible en la columna Estado.
    
- Hecho: movimientos de existencias completados con Hecho como estado.
    
- Entrante: muestra los registros de movimiento desde las ubicaciones de los proveedores.
    
- Saliente: muestra los registros de movimiento a las ubicaciones de los clientes e incluye las devoluciones.
    
- Interno: muestra los registros de movimiento de una ubicación a otra.
    
- Fabricación: muestra registros donde los productos fueron producidos desde la [ubicación](https://www.odoo.com/documentation/17.0/es/applications/inventory_and_mrp/inventory/warehouses_storage/inventory_management/use_locations.html) virtual de producción.
    
- Fecha: seleccione este menú desplegable para acceder a varias opciones de filtrado de fecha y visualizar los movimientos de existencias de un mes, trimestre o año específico.
    
- Últimos 30 días: muestra los registros que ocurrieron en los últimos treinta días.
    
- Ultimos tres meses: muestra los registros de los últimos tres meses.
    

 Ver también

[Buscar, filtrar y agrupar registros](https://www.odoo.com/documentation/17.0/es/applications/essentials/search.html)