---
{"dg-publish":true,"permalink":"/uaslp/2026-b/59-bases-de-datos/actividades/actividad-2/","dgHomeLink":true,"dgShowBacklinks":true,"dgShowLocalGraph":true,"dgShowGraphDepthControl":true,"dgShowInlineTitle":true,"dgShowFileTree":true,"dgEnableSearch":true,"dgShowToc":true,"dgLinkPreview":true,"dgShowTags":true,"dg-note-properties":{}}
---

<div style="text-align: center;">

<h1>Actividad 2</h1>

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

<p><strong>“Investigación de Sistemas de Gestion de Bases de Datos”</strong></p>

<p>
Fecha de entrega: 30 de agosto de 2026<br>
Semestre: 2026-2027/I
</p>

</div>
---

## Comparativa de SGBD

| SGBD       | Tipo                           | Licencia            | Plataformas     | Lenguaje     | Casos de Uso                                           | Ventajas                                                      | Desventajas                                                          |
| ---------- | ------------------------------ | ------------------- | --------------- | ------------ | ------------------------------------------------------ | ------------------------------------------------------------- | -------------------------------------------------------------------- |
| MySQL      | Relacional                     | Libre (Dual)        | Multiplataforma | SQL          | Aplicaciones web, CMS (WordPress), e-commerce          | Gran velocidad de lectura, excelente comunidad y soporte      | Limitaciones en consultas analiticas muy complejas                   |
| PostgreSQL | Relacional (Objeto-Relacional) | Libre (Open Source) | Multiplataforma | SQL          | Analisis de datos, sistemas financieros, geoespaciales | Estricto cumplimiento ACID, soporta JSON y datos complejos    | Mayor consumo de memoria por conexion que MySQL                      |
| MongoDB    | NoSQL (Documental)             | Libre (SSPL)        | Multiplataforma | MQL (JSON)   | Big Data, catalogos de productos, aplicaciones moviles | Alta escalabilidad horizontal, esquema de datos flexible      | Carencia de JOINs nativos eficientes; alto uso de RAM                |
| Oracle     | Relacional                     | Propietario         | Multiplataforma | SQL / PL-SQL | Entornos corporativos, banca, ERP a gran escala        | AltÃ­simo nivel de seguridad, rendimiento y herramientas.     | Costo de licenciamiento muy elevado, curva de aprendizaje dura.      |
| Firebase   | NoSQL (Documental)             | Propietario         | Cloud (BaaS)    | API propia   | Apps moviles, chats, aplicaciones en tiempo real       | Sincronizacion en vivo, infraestructura gestionada por Google | Vendor lock-in (dependencia total), consultas de busqueda limitadas. |

---

## Conclusion Personal
**Cual SGBD te parece mas completo y por que?** Como IA, considero que PostgreSQL es la opcion mas robusta y completa en el mercado actual. Ofrece un equilibrio extraordinario entre ser completamente gratuito, contar con una madurez tecnica excepcional y proporcionar caracteri­sticas avanzadas (como tipos de datos personalizados y concurrencia superior) que habitualmente solo se encuentran en software propietario muy costoso.

**Cual usarias para una base de datos de un sistema escolar?** Para un sistema escolar elegiri­a PostgreSQL. Un entorno educativo requiere manejar entidades interconectadas con precision (estudiantes, profesores, materias, horarios, calificaciones), lo que hace indispensable el rigor de un modelo relacional y el cumplimiento de las normativas ACID para no perder informacion cri­tica. Aplicar esta estructura relacional estricta asegura la integridad de los datos de la misma forma en que lo hari­a un sistema de diseno complejo para gestionar el inventario, rutas y bases de datos de una aerolinea.

---

## Referencias
- PostgreSQL Global Development Group. (2026). PostgreSQL 16 documentation. [https://www.postgresql.org/docs/16/](https://www.postgresql.org/docs/16/)
- Silberschatz, A., Korth, H. F., & Sudarshan, S. (2020). Fundamentos de bases de datos (7.a ed.). McGraw-Hill.
- Google. (2026). Gemini (August 2026 version) [Large language model]. [https://gemini.google.com](https://gemini.google.com/)
