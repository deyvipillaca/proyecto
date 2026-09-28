# 06. Drivers arquitectónicos

## Sistema de Registro de Habitaciones de Hotel

Los drivers arquitectónicos se organizan a partir de los objetivos, funcionalidades y requerimientos no funcionales del proyecto.

### 1. Objetivos del negocio
- Organizar la información de habitaciones, huéspedes y reservas.
- Controlar la disponibilidad y el estado de las habitaciones.
- Agilizar las consultas y la atención a los huéspedes.
- Reducir errores asociados al registro manual.

### 2. Funcionalidades clave
- Autenticación de usuarios.
- Gestión de habitaciones y huéspedes.
- Registro y consulta de reservas.
- Gestión de check-in y check-out.
- Actualización del estado de las habitaciones.
- Generación de reportes básicos.

### 3. Atributos de calidad prioritarios
- Seguridad y acceso autorizado.
- Integridad de la base de datos.
- Facilidad de uso.
- Respuesta rápida a consultas.
- Copias de seguridad y recuperación de información.

### 4. Restricciones
- Los usuarios principales son el administrador y el recepcionista.
- La solución debe gestionar datos personales de huéspedes y datos de reservas.
- El documento no define tecnologías ni una infraestructura específica.

### 5. Decisiones pendientes
- Selección de arquitectura y tecnologías.
- Definición del mecanismo de autenticación y permisos.
- Diseño físico de la base de datos.
- Estrategia de copias de seguridad y despliegue.
