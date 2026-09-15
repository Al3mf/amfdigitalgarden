---
{"dg-publish":true,"permalink":"/uaslp/2026-b/59-bases-de-datos/actividades/actividad-5/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---

```mermaid
erDiagram
    MEDICO {
        string medico_id PK
        string nombre_completo
        string CURP
        string NSS
        string cedula_profesional
        string tipo_medico
        date fecha_nacimiento
        int edad
        string direccion
    }
    TELEFONO_MEDICO {
        string numero PK
        string tipo
    }
    EMPLEADO {
        string empleado_id PK
        string nombre_completo
        string CURP
        string NSS
        string puesto
        date fecha_nacimiento
        int edad
        string direccion
    }
    TELEFONO_EMPLEADO {
        string numero PK
        string tipo
    }
    PACIENTE {
        string paciente_id PK
        string nombre_completo
        string CURP
        string NSS
        date fecha_nacimiento
        int edad
        string correo_electronico
        string direccion
    }
    TELEFONO_PACIENTE {
        string numero PK
        string tipo
    }
    ESPECIALIDAD {
        string especialidad_id PK
        string nombre
    }
    CITA {
        string cita_id PK
        datetime fecha_hora
        string motivo
        string estado
    }

    MEDICO ||--|{ TELEFONO_MEDICO : "tiene"
    EMPLEADO ||--|{ TELEFONO_EMPLEADO : "tiene"
    PACIENTE ||--|{ TELEFONO_PACIENTE : "tiene"
    PACIENTE }o--|| MEDICO : "tiene cabecera"
    MEDICO }o--o{ ESPECIALIDAD : "estudia"
    PACIENTE ||--o{ CITA : "agenda"
    MEDICO ||--o{ CITA : "atiende"
```

