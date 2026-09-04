---
{"dg-publish":true,"permalink":"/uaslp/2026-b/59-bases-de-datos/actividades/actividad-3-ejercicio/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---

# PROBLEMA
El Centro de Salud “San Rafael” administra la información de sus médicos, empleados y pacientes para asegurar un control eficiente de la atención.
Los médicos están registrados con un código interno (medico_id) y se almacena su nombre completo, CURP, número de seguridad social (NSS), cédula profesional y el tipo de médico que son (titular, interino o sustituto). Además, se registra su fecha de nacimiento, de la cual se puede derivar la edad. Cada médico cuenta con una dirección completa (calle, número exterior, número interior, colonia, ciudad, estado y código postal) y al menos un teléfono de contacto (móvil, fijo o de trabajo).
El resto de los empleados incluye a auxiliares de enfermería, veladores y auxiliares administrativos. De cada empleado se guarda un código interno (empleado_id), su nombre completo, CURP, NSS, el puesto que desempeña, así como su fecha de nacimiento (para calcular su edad). También se almacena su dirección con los mismos elementos que los médicos y sus teléfonos de contacto.
Los pacientes también cuentan con un código interno (paciente_id), su nombre completo, CURP, y en caso de tenerlo, su número de seguridad social (NSS). Se guarda además su fecha de nacimiento (para derivar la edad), su correo electrónico si lo proporcionan, y la dirección completa (calle, número exterior, número interior, colonia, ciudad, estado, código postal) junto con uno o varios teléfonos de contacto. Cada paciente está asignado a un médico de cabecera (medico_cabecera_id), lo que establece una relación directa entre pacientes y médicos.
Para ampliar la información clínica, el sistema también puede registrar las especialidades médicas. Cada especialidad tiene un código (especialidad_id) y un nombre, y un médico puede estar relacionado con varias especialidades.
Asimismo, los pacientes pueden agendar citas con cualquier médico del centro. Cada cita queda registrada con un identificador único (cita_id), la referencia al paciente y al médico, la fecha y hora de la cita, el motivo de la consulta y su estado (programada, atendida, cancelada o ausente).

# SOLUCION
Entidad: Empleado
Atributos:
- empleado_id (PK)
- nombre completo
- CURP
- NSS
- tipoEmpleado (FK)
- fechaNacimiento (derivado)
- direccion (compuesto)
	- calle
	- nInt
	- colonia
	- ciudad


Entidad: Citas
Atributos:
- cita_id (PK)
- paciente_id (FK)
- medico_id (FK)
- fecha
- hora
- motivoConsulta
- estado


Entidad: Paciente
Atributos:
- paciente_id (PK)
- nombre completo
- CURP
- NSS
- fecha de nacimiento
	- edad (derivado fn)
- correo electronico
- direccion (Atributo compuesto):
	- calle
	- numero exterior
	- numero interior
	- colonia
	- ciudad
	- estado
	- codigo postal
- telefonos de contacto (Atributo multivaluado)
- medico_cabecera_id (FK hacia la entidad Medico)

