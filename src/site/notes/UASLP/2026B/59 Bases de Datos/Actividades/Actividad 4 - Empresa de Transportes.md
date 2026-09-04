---
{"dg-publish":true,"permalink":"/uaslp/2026-b/59-bases-de-datos/actividades/actividad-4-empresa-de-transportes/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---

La empresa LogiMexico desea automatizar su gestion de reparto de paquetes en todo el pais. Los camioneros se registran con un numero de identificacion (camionero_id) y se almacena su nombre completo (nombre), telefono, direccion (calle, numero_ext, numero_int, colonia, ciudad, estado, cp), su salario y la ciudad_residencia.

Cada paquete se identifica mediante un codigo de paquete y se describe...

Las ciudades a las que llegan los paquetes se gestionan en un catalogo con un codigo de ciudad y un nombre de ciudad. Cada paquete llega a exactamente una ciudad, aunque una ciudad puede recibir multiples paquetes. Esto permite estadisticas de volumen por ciudad y control de tiempos de entrega.

La flota de camiones se adminstra registrando para cada unidad su matricula, modelo, tipo y capacidad de carga. Dado que un camionero puede codcir distintos camiones en fechas diferentes y un camion puede ser conducido por varios camioneros, e sistema registra los turnos de conduccion como asignaciones con camionero_id, camion_id, fecha_inicio y fecha_fin; de esta forma se conserva el historial de que conductor manejo que unidad y cuando


Camionero
- camionero_id PK
- nombre
- telefono
- calle
- num_ext
- num_int
- colonia
- ciudad
- estado
- codigo_postal
- salario
- ciudad_residencia_id FK

Paquete
- paquete_id PK
- descripcion
- destinatario_nom
- calle
- num_ext
- num_int
- colonia
- ciudad_destino_id FK
- estado_destino
- codigo_postal_destino
- fecha_envio
- fecha_entrega_estimada
- estado_paquete FK
- camionero_id FK

Ciudad
- ciudad_id PK
- ciudad_nombre

Camion
- camion_id PK
- modelo
- tipo_camion_id FK
- capacidad_kg 

Tipo
- tipo_camion_id PK
- tipo_camion_nombre

Turno
- camionero_id FK
- camion_id FK
- fecha_inicio
- fecha_fin

