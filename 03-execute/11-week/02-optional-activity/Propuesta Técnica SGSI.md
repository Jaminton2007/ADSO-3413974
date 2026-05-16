# SGSI — Propuesta Técnica

## Sistema de Gestión de Soporte e Incidencias

---

# Introducción y Contexto

SGSI (Sistema de Gestión de Soporte e Incidencias) corresponde a una plataforma empresarial orientada a la administración centralizada de soporte operativo, incidencias, activos tecnológicos y gestión documental de conocimiento técnico.

La solución será desarrollada bajo un ecosistema multiplataforma compuesto por:

- Aplicación Web Administrativa,
- Aplicación Móvil Operativa,
- Backend Centralizado,
- Servicios de Comunicación en Tiempo Real,
- Motor de SLA Empresarial,
- Gestión de Activos Tecnológicos (CMDB),
- Base de Conocimientos Técnica,
- Sistema de Auditoría y Trazabilidad.

La arquitectura del sistema implementará interoperabilidad entre clientes web y móviles mediante APIs REST y comunicación bidireccional utilizando WebSocket con STOMP sobre Spring Boot.

El proyecto se encuentra orientado a entornos empresariales que requieren:

- continuidad operativa,
- monitoreo distribuido,
- trazabilidad integral,
- sincronización en tiempo real,
- gestión centralizada,
- control de infraestructura,
- escalabilidad funcional.

SGSI será concebido como una solución empresarial de alta complejidad técnica, implementando principios modernos de ingeniería de software relacionados con:

- Arquitectura Hexagonal,
- Clean Architecture,
- diseño Stateless,
- RBAC,
- pruebas automatizadas,
- auditoría persistente,
- observabilidad operativa,
- despliegue contenerizado.

La duración estimada del proyecto será de:

```text
24 meses
```

debido al alcance funcional, profundidad arquitectónica y complejidad operativa de los módulos empresariales involucrados.

---

# Problemática Detallada

Actualmente, múltiples organizaciones administran incidencias y solicitudes internas mediante herramientas fragmentadas y no centralizadas, tales como:

- correos electrónicos,
- aplicaciones de mensajería,
- hojas de cálculo,
- llamadas telefónicas,
- formularios físicos,
- documentos aislados.

La ausencia de una plataforma unificada genera problemáticas críticas relacionadas con:

## Fragmentación Operativa

La información se distribuye entre múltiples canales sin mecanismos centralizados de seguimiento, provocando:

- pérdida de solicitudes,
- duplicidad de incidencias,
- ausencia de trazabilidad,
- dificultad para identificar responsables.

---

## Baja Capacidad de Auditoría

Las organizaciones carecen de mecanismos para:

- monitorear tiempos de atención,
- validar cumplimiento de SLA,
- auditar acciones realizadas,
- identificar cuellos de botella operativos.

---

## Ausencia de Gestión de Activos

Las incidencias no suelen relacionarse con activos tecnológicos específicos, generando:

- pérdida de historial técnico,
- imposibilidad de rastrear fallas recurrentes,
- baja visibilidad sobre infraestructura crítica.

---

## Dependencia de Conocimiento Individual

La resolución de incidencias depende frecuentemente del conocimiento informal de técnicos y operadores.

La ausencia de una base documental provoca:

- reincidencia de errores,
- tiempos elevados de resolución,
- baja transferencia de conocimiento.

---

## Limitaciones de Movilidad

Las soluciones tradicionales restringen la supervisión y administración a estaciones de trabajo fijas, afectando:

- capacidad de respuesta,
- continuidad operativa,
- monitoreo en campo,
- supervisión distribuida.

---

## Falta de Escalabilidad

Las herramientas improvisadas no permiten:

- crecimiento modular,
- integración entre servicios,
- automatización empresarial,
- escalabilidad horizontal.

---

# Objetivo General

Desarrollar una plataforma empresarial web y móvil para la gestión centralizada de soporte, incidencias, activos tecnológicos y conocimiento operativo, implementando mecanismos avanzados de trazabilidad, auditoría, monitoreo, seguridad e interoperabilidad multiplataforma.

---

# Objetivos Específicos

- Implementar un sistema integral de gestión de tickets.
- Desarrollar un módulo CMDB para administración de activos tecnológicos.
- Implementar una Base de Conocimientos técnica orientada a reutilización de soluciones.
- Implementar un motor avanzado de SLA basado en calendarios laborales configurables.
- Diseñar el sistema bajo Arquitectura Hexagonal y Clean Architecture.
- Implementar autenticación OAuth2 con JWT Stateless.
- Incorporar control de acceso granular mediante RBAC.
- Implementar sincronización en tiempo real mediante WebSocket/STOMP.
- Garantizar interoperabilidad entre Angular, Flutter y Spring Boot.
- Implementar auditoría persistente y trazabilidad operativa.
- Implementar dashboards y métricas empresariales.
- Desarrollar pruebas automatizadas unitarias y de integración.
- Garantizar despliegue contenerizado y escalabilidad horizontal.
- Implementar almacenamiento desacoplado de evidencias y archivos.

---

# Alcance del Proyecto

SGSI implementará una solución empresarial compuesta por los siguientes módulos:

| Módulo | Descripción |
|---|---|
| Gestión de Tickets | Administración integral de incidencias y solicitudes |
| Gestión de Usuarios | Administración de perfiles, autenticación y permisos |
| CMDB | Gestión de activos y elementos de configuración |
| Base de Conocimientos | Wiki técnica y documentación operativa |
| Motor SLA | Cálculo automático de tiempos de respuesta y resolución |
| Dashboard Operativo | Métricas, KPIs e indicadores empresariales |
| Reportería | Generación de reportes técnicos y administrativos |
| Auditoría | Registro persistente de operaciones críticas |
| Notificaciones | Comunicación en tiempo real y alertas |
| Gestión de Evidencias | Administración documental y archivos adjuntos |

---

# Justificación Técnica de Complejidad

La evolución de SGSI hacia una solución empresarial de alta complejidad responde a necesidades reales relacionadas con:

- administración centralizada de soporte,
- trazabilidad integral,
- control de infraestructura tecnológica,
- monitoreo de SLA,
- interoperabilidad multiplataforma,
- auditoría persistente,
- escalabilidad empresarial.

La incorporación de módulos especializados como:

- CMDB,
- Base de Conocimientos,
- Motor SLA,
- Auditoría centralizada,
- Control RBAC,
- Arquitectura Hexagonal,
- comunicación distribuida en tiempo real,

incrementa significativamente la complejidad técnica del proyecto debido a:

- integración de múltiples dominios funcionales,
- sincronización concurrente entre plataformas,
- modelado relacional avanzado,
- lógica empresarial desacoplada,
- persistencia transaccional compleja,
- administración granular de permisos,
- procesamiento distribuido de eventos.

La implementación de estándares empresariales exige:

- pruebas automatizadas,
- mantenibilidad evolutiva,
- observabilidad,
- despliegue contenerizado,
- diseño Stateless,
- desacoplamiento arquitectónico.

Debido al alcance técnico y profundidad funcional, el proyecto requiere un ciclo de desarrollo estimado de:

```text
24 meses
```

distribuidos entre:

- análisis,
- diseño,
- modelado,
- desarrollo,
- pruebas,
- integración,
- estabilización,
- despliegue,
- documentación técnica.

---

# Actores y Perfiles

## Usuario Final

Responsable del registro inicial de incidencias y validación de soluciones.

Funciones principales:

- crear tickets,
- adjuntar evidencias,
- consultar estados,
- validar resolución,
- consultar artículos técnicos,
- realizar seguimiento operativo.

Dispondrá de:

- acceso completo desde aplicación móvil,
- acceso limitado desde portal web de autoservicio.

---

## Agente de Soporte

Responsable de la atención técnica y documentación operativa.

Funciones principales:

- resolver incidencias,
- actualizar estados,
- asociar activos tecnológicos,
- documentar soluciones,
- publicar artículos técnicos,
- gestionar evidencias.

---

## Supervisor

Responsable del monitoreo operativo y control de SLA.

Funciones principales:

- supervisar métricas,
- reasignar tickets,
- validar tiempos de atención,
- monitorear cumplimiento,
- administrar escalamiento,
- aprobar artículos técnicos.

---

## Administrador

Responsable de la administración global de la plataforma.

Funciones principales:

- administrar usuarios,
- gestionar RBAC,
- configurar SLA,
- parametrizar categorías,
- administrar CMDB,
- supervisar auditorías,
- configurar infraestructura lógica.

---

# Arquitectura Operativa

SGSI implementará una arquitectura empresarial basada en:

```text
Clean Architecture + Arquitectura Hexagonal
```

Este enfoque permitirá desacoplar la lógica de negocio respecto a:

- frameworks,
- bases de datos,
- servicios externos,
- tecnologías de infraestructura.

La arquitectura garantizará:

- mantenibilidad evolutiva,
- extensibilidad modular,
- desacoplamiento técnico,
- testabilidad,
- independencia tecnológica.

---

## Stack Tecnológico

| Capa | Tecnología |
|---|---|
| Frontend Web | Angular |
| Aplicación Móvil | Flutter |
| Backend | Spring Boot |
| Persistencia | PostgreSQL |
| ORM | JPA/Hibernate |
| Seguridad | OAuth2 + JWT Stateless |
| Tiempo Real | WebSocket + STOMP |
| Contenedores | Docker |
| Testing | JUnit + Mockito |
| Control de Versiones | GitHub |

---

## Arquitectura de Comunicación

```text
┌─────────────────────────────┐
│   Aplicación Web (Angular) │
└─────────────┬───────────────┘
              │
     REST API │ WebSocket/STOMP
              │
┌─────────────▼───────────────┐
│ Backend Centralizado       │
│ Spring Boot + OAuth2       │
│ REST + WebSocket/STOMP     │
│ Arquitectura Hexagonal     │
└─────────────┬───────────────┘
              │
              │ JPA/Hibernate
              │
┌─────────────▼───────────────┐
│ PostgreSQL                 │
│ Persistencia y Metadatos   │
└─────────────┬───────────────┘
              │
              │ Rutas/Referencias
              │
┌─────────────▼───────────────┐
│ FileSystem / Storage       │
│ Evidencias y Archivos      │
└─────────────────────────────┘
              ▲
              │
     REST API │ WebSocket/STOMP
              │
┌─────────────┴───────────────┐
│ Aplicación Móvil (Flutter) │
└─────────────────────────────┘
```

---

# Módulos Especializados

# Gestión de Activos — CMDB

SGSI implementará un módulo CMDB (Configuration Management Database) orientado a la administración de activos tecnológicos.

Cada ticket podrá asociarse a un:

```text
Elemento de Configuración (CI)
```

Tipos de activos:

- PC,
- Servidor,
- Software,
- Router,
- Switch,
- Impresora,
- Periférico.

Atributos registrados:

- serial,
- marca,
- modelo,
- ubicación,
- responsable,
- estado operativo,
- historial técnico.

El módulo permitirá:

- trazabilidad de infraestructura,
- monitoreo de activos,
- relación entre incidencias y hardware,
- control de mantenimiento.

---

# Base de Conocimientos (Wiki Técnica)

SGSI implementará una Base de Conocimientos orientada a:

- documentación técnica,
- reutilización de soluciones,
- reducción de recurrencia,
- transferencia de conocimiento.

Los Agentes podrán:

- publicar artículos,
- documentar procedimientos,
- registrar soluciones validadas,
- categorizar contenido técnico.

Los Supervisores podrán:

- validar documentación,
- aprobar publicaciones,
- controlar calidad del contenido.

---

# Motor de SLA Avanzado

El sistema implementará un motor avanzado de SLA orientado a calcular:

- tiempos de respuesta,
- tiempos de resolución,
- incumplimientos operativos,
- escalamiento automático.

El cálculo considerará:

- horarios laborales configurables,
- fines de semana,
- festivos,
- prioridades,
- categorías,
- severidad de incidencias.

---

# Matriz de Permisos (RBAC)

| Acción | Usuario | Agente | Supervisor | Administrador |
|---|---|---|---|---|
| Crear tickets | ✔ | ✔ | ✔ | ✔ |
| Validar solución | ✔ | ✖ | ✔ | ✔ |
| Resolver tickets | ✖ | ✔ | ✔ | ✔ |
| Reasignar tickets | ✖ | ✖ | ✔ | ✔ |
| Gestionar CMDB | ✖ | ✔ | ✔ | ✔ |
| Registrar activos | ✖ | ✔ | ✔ | ✔ |
| Publicar artículos Wiki | ✖ | ✔ | ✔ | ✔ |
| Aprobar artículos Wiki | ✖ | ✖ | ✔ | ✔ |
| Configurar SLA | ✖ | ✖ | ✔ | ✔ |
| Gestionar usuarios | ✖ | ✖ | ✖ | ✔ |
| Administrar RBAC | ✖ | ✖ | ✖ | ✔ |
| Ejecutar auditoría | ✖ | ✖ | ✔ | ✔ |
| Gestionar categorías | ✖ | ✖ | ✔ | ✔ |
| Gestionar prioridades | ✖ | ✖ | ✔ | ✔ |

---

# Requisitos Funcionales (RF)

| ID | Requisito Funcional |
|---|---|
| RF-01 | El sistema deberá implementar autenticación OAuth2 con JWT Stateless. |
| RF-02 | El sistema deberá permitir gestión integral de tickets. |
| RF-03 | El sistema deberá implementar comunicación en tiempo real mediante WebSocket/STOMP. |
| RF-04 | El sistema deberá permitir adjuntar evidencias y archivos. |
| RF-05 | El sistema deberá implementar trazabilidad operativa persistente. |
| RF-06 | El sistema deberá implementar administración de activos mediante CMDB. |
| RF-07 | El sistema deberá permitir asociar tickets a elementos de configuración. |
| RF-08 | El sistema deberá implementar una Base de Conocimientos técnica. |
| RF-09 | El sistema deberá implementar cálculo automático de SLA. |
| RF-10 | El sistema deberá generar dashboards e indicadores operativos. |
| RF-11 | El sistema deberá implementar control RBAC granular. |
| RF-12 | El Usuario Final deberá validar la resolución antes del cierre definitivo. |
| RF-13 | El sistema deberá ejecutar cierre automático por inactividad. |
| RF-14 | El sistema deberá mantener sincronización multiplataforma en tiempo real. |

---

# Requisitos No Funcionales (RNF) — Parche de Calidad

| ID | Atributo de Calidad | Especificación Técnica |
|---|---|---|
| RNF-01 | Mantenibilidad | El backend deberá implementar Arquitectura Hexagonal para desacoplar dominio e infraestructura. |
| RNF-02 | Seguridad de Persistencia | Las credenciales deberán almacenarse mediante BCrypt con factor de costo 10. |
| RNF-03 | Seguridad en Tránsito | Toda comunicación deberá utilizar TLS 1.3 y canales WebSocket seguros (WSS). |
| RNF-04 | Fiabilidad | El backend deberá mantener cobertura mínima de pruebas automatizadas del 80%. |
| RNF-05 | Rendimiento | El 95% de las transacciones deberán responder en menos de 200ms bajo carga nominal. |
| RNF-06 | Disponibilidad | Los servicios deberán ejecutarse mediante Docker bajo arquitectura Stateless. |
| RNF-07 | Integridad Transaccional | Todas las operaciones críticas deberán cumplir propiedades ACID mediante JPA/Hibernate. |
| RNF-08 | Escalabilidad | La arquitectura deberá permitir incorporación modular de nuevos servicios. |
| RNF-09 | Interoperabilidad | El sistema deberá garantizar compatibilidad entre Angular, Flutter y Spring Boot. |
| RNF-10 | Auditoría | Todas las operaciones críticas deberán generar trazabilidad persistente. |
| RNF-11 | Usabilidad Móvil | La aplicación Flutter deberá mantener 60 FPS y seguir Material Design 3. |
| RNF-12 | Portabilidad | La solución deberá ser desplegable en Linux, Windows y entornos Cloud compatibles con Docker. |
| RNF-13 | Observabilidad | El backend deberá implementar logging estructurado y monitoreo técnico. |
| RNF-14 | Disponibilidad Operativa | El sistema deberá tolerar reinicios de servicios sin pérdida de sesiones mediante JWT Stateless. |

---

# Estrategia de Calidad y DevOps

SGSI implementará una estrategia de aseguramiento de calidad basada en:

- pruebas unitarias,
- pruebas de integración,
- validación continua,
- análisis estático,
- revisión arquitectónica,
- automatización de despliegues.

Tecnologías previstas:

| Área | Tecnología |
|---|---|
| Testing Unitario | JUnit |
| Mocking | Mockito |
| Testing Integración | TestContainers |
| APIs | Postman/Newman |
| Calidad de Código | SonarQube |
| Contenedores | Docker |
| CI/CD | GitHub Actions |

La infraestructura será diseñada bajo principios:

```text
Stateless + Escalabilidad Horizontal
```

permitiendo:

- balanceo de carga,
- recuperación simplificada,
- despliegue distribuido,
- continuidad operativa.

---

# Flujo Operativo y Ciclo de Vida del Ticket

```text
Usuario Final registra incidencia
            ↓
Sistema genera ticket
            ↓
Supervisor valida prioridad
            ↓
Ticket es asignado a Agente
            ↓
Agente analiza activo asociado (CMDB)
            ↓
Incidencia entra en proceso
            ↓
Agente resuelve incidencia
            ↓
Agente documenta solución en Wiki Técnica
            ↓
Usuario Final valida solución
            ↓
Sistema ejecuta cierre
            ↓
Auditoría administrativa posterior
```

---

# Regla de SLA y Auto-cierre

```text
Si el Usuario Final no valida la solución en un periodo de 72 horas, el sistema ejecutará automáticamente un cierre por inactividad.
```

Este mecanismo permitirá:

- limpieza operativa de la cola de tickets,
- optimización de métricas,
- reducción de incidencias estancadas,
- control del ciclo de vida operativo.

---

# Flujo de Estados del Ticket

```text
Abierto
→ En revisión
→ Asignado
→ En proceso
→ Resuelto
→ Validación de Usuario
→ Cerrado
```

Estados complementarios:

```text
Pendiente
Escalado
Reabierto
Cancelado
Cierre Automático
```

Todos los cambios de estado serán sincronizados mediante:

- REST API,
- WebSocket/STOMP,
- dashboards,
- módulos de auditoría,
- servicios de notificación.

---

# Conclusión Técnica

SGSI representa una solución empresarial de alta complejidad orientada a la administración integral de soporte, incidencias, activos tecnológicos y conocimiento operativo.

La incorporación de:

- Arquitectura Hexagonal,
- CMDB,
- Base de Conocimientos,
- Motor SLA,
- OAuth2,
- RBAC,
- comunicación en tiempo real,
- auditoría persistente,
- despliegue contenerizado,
- pruebas automatizadas,

eleva significativamente el nivel técnico del proyecto y lo posiciona como una solución alineada con estándares modernos de ingeniería de software empresarial.

La arquitectura propuesta garantiza:

- mantenibilidad evolutiva,
- escalabilidad horizontal,
- interoperabilidad multiplataforma,
- seguridad,
- trazabilidad centralizada,
- continuidad operativa,
- capacidad de crecimiento modular.

Debido a su alcance funcional y profundidad arquitectónica, SGSI constituye un proyecto viable para un ciclo de desarrollo de 24 meses bajo estándares industriales y académicos de grado empresarial.