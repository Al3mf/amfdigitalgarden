---
{"dg-publish":true,"permalink":"/uaslp/2026-b/59-bases-de-datos/actividades/actividad-4-ejercicio-empresa-comercializadora/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---

la empresa comercializadora global administra la informacion de sus clientes, productos y proveedores para poder llevar un mejor control de las ventas. los clientes son identificados mediante una clave intera (cliente_id). de cada cliente se almancenan sus nombres y apellidos completos, su curp, su direccion (compuesta por calle, numero exterior, numero interior, colonia, ciudad, estado y codigo postal) y su fecha de nacimiento, que permite calcular la edad como atributo derivado.
los productos que comercualiza la empresa cuentan con un codigo unico (producto_id), un nombre descriptivo y un precio unitario, cada producto se asocia a un unico proveedor, aunque puede ser comprado por muhcos clientes diferentes

Producto
- producto_id PL
- nombre
- precio
- RFC_proveedor FK

Proveedor
- RFC PK
- nom_comercial
- calle
- numero_ext
- numero_int
- colonia
- ciudad
- estado
- codigo_postal

Cliente
- cliente_id PK
- nombre
- curp
- calle
- num_int
- num_ext
- colonia
- ciudad
- estado
- cd

Venta
- cliente_id FK
- producto_id FK
- cantidad
- fecha
- venta_id PK

