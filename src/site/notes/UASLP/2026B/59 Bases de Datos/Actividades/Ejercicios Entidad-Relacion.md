---
{"dg-publish":true,"permalink":"/uaslp/2026-b/59-bases-de-datos/actividades/ejercicios-entidad-relacion/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---

<div style="text-align: center;">

<h1>Actividad 3</h1>

<p>
Universidad Autónoma de San Luis Potosí<br>
Facultad de Ingeniería<br>
Área de Ciencias de la Computación
</p>

<p>
<strong>Alejandro Melo Flores</strong><br>
Bases de Datos<br>
Alberto Ramos Blanco
</p>

<p><strong>“Ejercicios Entidad Relacion”</strong></p>

<p>
Fecha de entrega: 14 de Septiembre de 2026<br>
Semestre: 2026-2027/I
</p>

</div>


---

# Ejercicio Centro de Salud
El Centro de Salud “San Rafael” administra la información de sus médicos, empleados y pacientes para asegurar un control eficiente de la atención. Los médicos están registrados con un código interno (medico_id) y se almacena su nombre completo, CURP, número de seguridad social (NSS), cédula profesional y el tipo de médico que son (titular, interino o sustituto). Además, se registra su fecha de nacimiento, de la cual se puede derivar la edad. Cada médico cuenta con una dirección completa (calle, número exterior, número interior, colonia, ciudad, estado y código postal) y al menos un teléfono de contacto (móvil, fijo o de trabajo). El resto de los empleados incluye a auxiliares de enfermería, veladores y auxiliares administrativos. De cada empleado se guarda un código interno (empleado_id), su nombre completo, CURP, NSS, el puesto que desempeña, así como su fecha de nacimiento (para calcular su edad). También se almacena su dirección con los mismos elementos que los médicos y sus teléfonos de contacto. Los pacientes también cuentan con un código interno (paciente_id), su nombre completo, CURP, y en caso de tenerlo, su número de seguridad social (NSS). Se guarda además su fecha de nacimiento (para derivar la edad), su correo electrónico si lo proporcionan, y la dirección completa (calle, número exterior, número interior, colonia, ciudad, estado, código postal) junto con uno o varios teléfonos de contacto. Cada paciente está asignado a un médico de cabecera (medico_cabecera_id), lo que establece una relación directa entre pacientes y médicos. Para ampliar la información clínica, el sistema también puede registrar las especialidades médicas. Cada especialidad tiene un código (especialidad_id) y un nombre, y un médico puede estar relacionado con varias especialidades. Asimismo, los pacientes pueden agendar citas con cualquier médico del centro. Cada cita queda registrada con un identificador único (cita_id), la referencia al paciente y al médico, la fecha y hora de la cita, el motivo de la consulta y su estado (programada, atendida, cancelada o ausente).

![Pasted image 20260914210608.png](/img/user/Pasted%20image%2020260914210608.png)

---
# Ejercicio: Biblioteca Universitaria
En la Biblioteca Central de la Universidad se quiere automatizar el proceso de préstamo de libros para mejorar la organización y el control del material bibliográfico.
Cada libro será registrado con un folio único (folio_libro) que servirá como identificador. Además, se almacena su título, el autor o autores, la editorial y el área del conocimiento a la que pertenece (por ejemplo: Matemáticas, Geografía, Física, Historia). Estos atributos permiten clasificar y recuperar fácilmente los ejemplares dentro del catálogo.
Los usuarios de la biblioteca se dividen en varias categorías: estudiantes, administrativos, profesores y público en general. De cada usuario se debe registrar una clave única de usuario (usuario_id), su nombre completo, dirección, teléfono de contacto y la categoría de usuario a la que pertenece. Esta clasificación permitirá aplicar diferentes políticas de préstamo según el tipo de usuario (por ejemplo, mayor tiempo de préstamo para profesores que para estudiantes).
Para el control de los préstamos, se registran los siguientes datos: la clave del libro (folio_libro), la clave del usuario (usuario_id) que solicita el ejemplar y la fecha en que se realiza el préstamo. En caso de extender el sistema, se podrá

![Pasted image 20260914203639.png](/img/user/Pasted%20image%2020260914203639.png)

---

# Ejercicio: Empresa Comercializadora
La empresa Comercializadora Global administra la información de sus clientes, productos y proveedores para poder llevar un mejor control de las ventas.
Los clientes son identificados mediante una clave interna (cliente_id). De cada cliente se almacenan sus nombres y apellidos completos, su CURP, su dirección (compuesta por calle, número exterior, número interior, colonia, ciudad, estado y código postal) y su fecha de nacimiento, que permite calcular la edad como atributo derivado.
Los productos que comercializa la empresa cuentan con un código único (producto_id), un nombre descriptivo y un precio unitario. Cada producto se asocia a un único proveedor, aunque puede ser comprado por muchos clientes diferentes.
Los proveedores son registrados mediante su RFC (atributo clave primaria) y se almacena también su nombre comercial y su dirección completa (calle, número exterior, número interior, colonia, ciudad, estado, código postal). Un proveedor puede suministrar varios productos, pero cada producto solo puede estar vinculado a un único proveedor.
Finalmente, para registrar las ventas, se relaciona el cliente con los productos que compra. Cada operación de venta contiene la clave del cliente (cliente_id), la clave del producto (producto_id) y, opcionalmente, la cantidad adquirida junto con la fecha de la compra. Esto refleja la relación muchos a muchos entre clientes y productos

![Pasted image 20260914211019.png](/img/user/Pasted%20image%2020260914211019.png)


---

# Ejercicio: Empresa de Transportes
La empresa LogiMéxico desea automatizar su gestión de reparto de paquetes en todo el país. Los camioneros se registran con un número de identificación (camionero_id) y se almacena su nombre completo (nombre), teléfono de contacto (telefono), dirección (calle, numero_exterior, numero_interior, colonia, ciudad, estado, codigo_postal), su salario (salario) y la ciudad en la que vive (ciudad_residencia).
Cada paquete se identifica mediante un código de paquete (paquete_id) y se describe con una descripción del contenido.
Para garantizar la entrega se registra el destinatario (destinatario_nombre) y la dirección del destinatario, desglosada en calle, numero_exterior, numero_interior, colonia, ciudad_destino, estado_destino y codigo_postal_destino.
Para el seguimiento operativo, el sistema también almacena la fecha de envío (fecha_envio), una fecha de entrega estimada (fecha_entrega_estimada) y el estado del paquete (estado: EN_RUTA, ENTREGADO, INCIDENCIA). Por política, cada paquete es distribuido por un único camionero (camionero_id), mientras que un camionero puede distribuir muchos paquetes.
Las ciudades a las que llegan los paquetes se gestionan en un catálogo con un código de ciudad (ciudad_id) y un nombre de ciudad (ciudad_nombre). Cada paquete llega a exactamente una ciudad (referenciada por ciudad_id), aunque una ciudad puede recibir múltiples paquetes. Esto permite estadísticas de volumen por ciudad y control de tiempos de entrega.
La flota de camiones se administra registrando para cada unidad su matrícula (camion_id o matricula), modelo (modelo), tipo (tipo: RABÓN, TORTHON, TRACTOCAMIÓN, ETC.) y capacidad de carga (capacidad_kg). Dado que un camionero puede conducir distintos camiones en fechas diferentes y un camión puede ser conducido por varios camioneros, el sistema registra los turnos de conducción como asignaciones con camionero_id, camion_id, fecha_inicio y fecha_fin; de esta forma se conserva el historial de qué conductor manejó qué unidad y cuándo.

![Pasted image 20260914220617.png](/img/user/Pasted%20image%2020260914220617.png)