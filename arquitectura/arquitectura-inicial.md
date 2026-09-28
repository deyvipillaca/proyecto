# Arquitectura inicial del sistema

## 3. Estilo arquitectónico propuesto

Se propone una **arquitectura en tres capas**:

1. **Capa de presentación:** interfaz utilizada por el administrador y el recepcionista.
2. **Capa de lógica de negocio:** aplica las reglas de gestión de habitaciones, huéspedes, reservas y estadías.
3. **Capa de datos:** almacena y recupera la información del sistema.


4. Diagrama general de arquitectura


┌─────────────────────────────────────────────────────────────┐
│                     USUARIOS DEL SISTEMA                    │
│              Administrador        Recepcionista             │
└──────────────────────────────┬──────────────────────────────┘
                               │
                               ▼
┌─────────────────────────────────────────────────────────────┐
│                    1. CAPA DE PRESENTACIÓN                 │
│                                                             │
│  • Inicio de sesión                                         │
│  • Panel principal                                          │
│  • Formularios de habitaciones y huéspedes                  │
│  • Pantallas de reservas y disponibilidad                  │
│  • Pantallas de check-in y check-out                        │
│  • Consultas y reportes                                     │
└──────────────────────────────┬──────────────────────────────┘
                               │ Solicitudes
                               ▼
┌─────────────────────────────────────────────────────────────┐
│                  2. CAPA DE LÓGICA DE NEGOCIO              │
│                                                             │
│  ┌───────────────────┐  ┌────────────────────────────────┐ │
│  │ Autenticación y   │  │ Gestión de habitaciones        │ │
│  │ autorización      │  │ Registro, edición y estado     │ │
│  └───────────────────┘  └────────────────────────────────┘ │
│  ┌───────────────────┐  ┌────────────────────────────────┐ │
│  │ Gestión de        │  │ Gestión de reservas            │ │
│  │ huéspedes         │  │ Registro y disponibilidad      │ │
│  └───────────────────┘  └────────────────────────────────┘ │
│  ┌───────────────────┐  ┌────────────────────────────────┐ │
│  │ Gestión de        │  │ Consultas y reportes            │ │
│  │ estadías          │  │ Consultas y resúmenes básicos  │ │
│  └───────────────────┘  └────────────────────────────────┘ │
└──────────────────────────────┬──────────────────────────────┘
                               │ Operaciones de datos
                               ▼
┌─────────────────────────────────────────────────────────────┐
│                       3. CAPA DE DATOS                      │
│                                                             │
│  Base de datos:                                             │
│  • Usuarios y roles                                         │
│  • Habitaciones                                              │
│  • Huéspedes                                                 │
│  • Reservas                                                  │
│  • Registros de estadía / movimientos                       │
└─────────────────────────────────────────────────────────────┘


## 11. Despliegue lógico propuesto


┌──────────────────────────────┐
│ Equipo del administrador o   │
│ recepcionista                │
│ Interfaz del sistema         │
└──────────────┬───────────────┘
               │ Red local o conexión segura
               ▼
┌──────────────────────────────┐
│ Aplicación del sistema       │
│ Presentación + lógica        │
│ de negocio                   │
└──────────────┬───────────────┘
               │
               ▼
┌──────────────────────────────┐
│ Servicio de base de datos    │
│ Usuarios, huéspedes,         │
│ habitaciones y reservas      │
└──────────────────────────────┘
