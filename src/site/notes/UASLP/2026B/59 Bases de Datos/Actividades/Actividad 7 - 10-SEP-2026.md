---
{"dg-publish":true,"permalink":"/uaslp/2026-b/59-bases-de-datos/actividades/actividad-7-10-sep-2026/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---

# Ejercicio 1: Empresa Comercializadora
La empresa Comercializadora Global administra la información de sus clientes, productos y proveedores para poder llevar un mejor control de las ventas.
Los clientes son identificados mediante una clave interna (cliente_id). De cada cliente se almacenan sus nombres y apellidos completos, su CURP, su dirección (compuesta por calle, número exterior, número interior, colonia, ciudad, estado y código postal) y su fecha de nacimiento, que permite calcular la edad como atributo derivado.
Los productos que comercializa la empresa cuentan con un código único (producto_id), un nombre descriptivo y un precio unitario. Cada producto se asocia a un único proveedor, aunque puede ser comprado por muchos clientes diferentes.
Los proveedores son registrados mediante su RFC (atributo clave primaria) y se almacena también su nombre comercial y su dirección completa (calle, número exterior, número interior, colonia, ciudad, estado, código postal). Un proveedor puede suministrar varios productos, pero cada producto solo puede estar vinculado a un único proveedor.
Finalmente, para registrar las ventas, se relaciona el cliente con los productos que compra. Cada operación de venta contiene la clave del cliente (cliente_id), la clave del producto (producto_id) y, opcionalmente, la cantidad adquirida junto con la fecha de la compra. Esto refleja la relación muchos a muchos entre clientes y productos.







Ejercicio 2: Empresa de Transportes

La empresa LogiMéxico desea automatizar su gestión de reparto de paquetes en todo el país. Los camioneros se registran con un número de identificación (camionero_id) y se almacena su nombre completo (nombre), teléfono de contacto (telefono), dirección (calle, numero_exterior, numero_interior, colonia, ciudad, estado, codigo_postal), su salario (salario) y la ciudad en la que vive (ciudad_residencia).

Cada paquete se identifica mediante un código de paquete (paquete_id) y se describe con una descripción del contenido.

Para garantizar la entrega se registra el destinatario (destinatario_nombre) y la dirección del destinatario, desglosada en calle, numero_exterior, numero_interior, colonia, ciudad_destino, estado_destino y codigo_postal_destino.

Para el seguimiento operativo, el sistema también almacena la fecha de envío (fecha_envio), una fecha de entrega estimada (fecha_entrega_estimada) y el estado del paquete (estado: EN_RUTA, ENTREGADO, INCIDENCIA). Por política, cada paquete es distribuido por un único camionero (camionero_id), mientras que un camionero puede distribuir muchos paquetes.

Las ciudades a las que llegan los paquetes se gestionan en un catálogo con un código de ciudad (ciudad_id) y un nombre de ciudad (ciudad_nombre). Cada paquete llega a exactamente una ciudad (referenciada por ciudad_id), aunque una ciudad puede recibir múltiples paquetes. Esto permite estadísticas de volumen por ciudad y control de tiempos de entrega.

La flota de camiones se administra registrando para cada unidad su matrícula (camion_id o matricula), modelo (modelo), tipo (tipo: RABÓN, TORTHON, TRACTOCAMIÓN, ETC.) y capacidad de carga (capacidad_kg). Dado que un camionero puede conducir distintos camiones en fechas diferentes y un camión puede ser conducido por varios camioneros, el sistema registra los turnos de conducción como asignaciones con camionero_id, camion_id, fecha_inicio y fecha_fin; de esta forma se conserva el historial de qué conductor manejó qué unidad y cuándo.