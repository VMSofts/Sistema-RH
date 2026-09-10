# Sistema RH

Plataforma web de reclutamiento y servicios de recursos humanos. Conecta a
empresas, candidatos y colaboradores externos en un mismo sistema, administrado por
el equipo de RH con acceso por módulos.

---

## Quién la usa

| Rol | Qué hace |
|---|---|
| **Empresa** | Publica vacantes y solicita servicios (capacitación, coaching, entre otros) |
| **Candidato** | Completa su perfil una sola vez y postula a las vacantes que le interesan |
| **Colaborador externo** | Ejecuta los servicios que se le asignan |
| **Personal interno** | Administra la plataforma con permisos por módulo |
| **Administrador** | Orquesta todo el sistema |

Todo el sistema se sostiene en **dos flujos**: el de la vacante (una empresa
publica, los candidatos postulan, RH da seguimiento) y el del servicio (alguien lo
solicita, se asigna a un colaborador y se da seguimiento hasta cerrarlo).

---

## Módulos

| Módulo | Qué cubre |
|---|---|
| **Vacantes** | Publicación con filtros por nivel jerárquico y nivel de estudios |
| **Candidatos y postulaciones** | Perfil único del candidato y seguimiento de cada postulación |
| **Cuestionarios** | Evaluaciones asignables, calificación automática y enlace público del resultado |
| **Servicios y pedidos** | Solicitud, asignación a colaboradores y seguimiento |
| **Tareas** | Trabajo interno del equipo de RH |
| **Pagos a colaboradores** | Registro de lo que se paga por servicio ejecutado |
| **Chat** | Mensajería interna con auditoría de conversaciones |
| **Reportes** | Indicadores de vacantes, postulaciones y servicios |
| **Configuración y catálogos** | Catálogos dinámicos y ajustes del sistema sin tocar código |
| **Registro de actividad** | Bitácora de quién hizo qué y cuándo |

---

## Características técnicas

- **Laravel 13** con **Livewire 4**
- Aplicación web instalable (**PWA**) con **notificaciones push**
- Colas supervisadas con **Horizon** y monitoreo con **Pulse**
- Inicio de sesión con proveedores externos mediante **Socialite**
- Bitácora de actividad con **laravel-activitylog**
- Toda la lógica de negocio en servicios; carga anticipada obligatoria de relaciones
  para evitar consultas N+1
- Interfaz y código en español

---

## Rendimiento

En producción se sirve con **[Obsidiana](https://github.com/VicCodeM/Obsidiana)**, el
motor propio de VMSofts escrito en Rust: el tiempo por petición baja de 40 ms con
Apache y php-fpm a unos 10 ms, sirviendo exactamente el mismo contenido.

---

## Código

El código fuente de este proyecto es privado. Este repositorio presenta qué es,
qué resuelve y con qué está construido.

---

Creado por VMSofts
