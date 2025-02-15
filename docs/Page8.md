# Mantenimiento y Actualización

### 1. **Política de mantenimiento**

El sistema **LUMINO** fue desarrollado como parte de un proyecto de clase por un equipo de dos personas. Aunque el proyecto ya ha sido entregado y no hay planes inmediatos de continuar su desarrollo, se establece la siguiente política de mantenimiento hipotética en caso de que el proyecto sea retomado en el futuro:

#### **1. Frecuencia de actualizaciones**

- **Actualizaciones menores (correcciones de errores y mejoras de rendimiento)**:

  - En caso de retomar el proyecto, las actualizaciones menores se realizarían de manera **puntual** cuando se detecten errores críticos o problemas de rendimiento.
  - Estas actualizaciones se priorizarían para garantizar la estabilidad del sistema.

- **Actualizaciones mayores (nuevas funcionalidades)**:
  - Si el proyecto se retoma, se podrían implementar nuevas funcionalidades de manera **periódica**, dependiendo de la disponibilidad del equipo.
  - Algunas ideas hipotéticas para futuras actualizaciones incluyen:
    - Mejoras en la interfaz de usuario.
    - Integración con sistemas de autenticación externos (por ejemplo, Google o Microsoft).
    - Expansión de la plataforma para soportar más usuarios y asignaturas.

#### **2. Soporte técnico**

- **Soporte para usuarios**:

  - En caso de retomar el proyecto, se podría proporcionar soporte técnico a través de un **sistema de tickets** o correo electrónico, donde los usuarios podrían reportar problemas o sugerir mejoras.
  - El tiempo de respuesta dependería de la disponibilidad del equipo, pero se intentaría resolver los problemas en un plazo máximo de **7 días hábiles**.

- **Soporte para desarrolladores**:
  - Si el proyecto se retoma, se mantendría una **documentación actualizada** para facilitar la colaboración de nuevos desarrolladores.
  - Se realizarían reuniones periódicas para revisar el estado del proyecto y planificar futuras actualizaciones.

#### **3. Compromiso con la calidad**

Aunque el proyecto ya se ha entregado, el equipo se compromete a mantener un alto estándar de calidad en el código y la documentación existentes. Se han tenido en cuenta las correcciones y sugerencias proporcionadas por el profesor, las cuales se aplicarían para mejorar el código en caso de retomar el proyecto. Estas mejoras incluyen:

- **Corrección de errores y ajustes en los modelos**: Asegurar que los campos y relaciones sigan las convenciones establecidas, como el uso correcto de `related_name` y la longitud adecuada de los campos.
- **Modularización del código**: Separar la lógica de las vistas en archivos independientes y fomentar la creación de métodos reutilizables en los modelos.
- **Optimización del procesador de contexto**: Asegurar que solo se devuelvan los módulos relevantes para cada usuario (alumnos o profesores).
- **Eliminación de comentarios obsoletos**: Mantener el código limpio y legible.
- **Mejoras en la estructura del código**: Aplicar buenas prácticas de desarrollo, como encapsular la lógica de negocio en los modelos y evitar la duplicación de código.

### 2. **Plan de escalabilidad**

### **Posibles mejoras para soportar más usuarios o nuevas funcionalidades**

El sistema **LUMINO** fue diseñado como un proyecto de clase, pero en caso de retomarse en el futuro, se podrían implementar las siguientes mejoras para garantizar su escalabilidad:

#### **1. Base de datos escalable**

- Migrar a **PostgreSQL** en producción para mejorar el rendimiento, la capacidad de almacenamiento y la gestión de grandes volúmenes de datos.
- Implementar técnicas de optimización de consultas y uso de índices para reducir los tiempos de respuesta.

#### **2. Optimización del rendimiento**

- Mejorar la eficiencia del código y reducir el consumo de recursos para soportar un mayor número de usuarios simultáneos.
- Implementar un sistema de caché (por ejemplo, con **Redis**) para acelerar el acceso a datos frecuentemente solicitados.

#### **3. Arquitectura escalable**

- Diseñar una arquitectura basada en microservicios para facilitar la escalabilidad horizontal.
- Utilizar servicios en la nube (como **AWS** o **Google Cloud**) para gestionar el tráfico y los recursos de manera dinámica.

#### **4. Soporte para móviles**

- Desarrollar una aplicación móvil para acceder a **LUMINO** desde cualquier dispositivo, mejorando la accesibilidad y la experiencia del usuario.

---

### 3. Registro de cambios (Changelog)

#### Algunos ejemplos:

```bash
commit 00a7e843a66340e3f0b1557dc5ec885947c73e35
Author: Kai <145053705+YoooKai@users.noreply.github.com>
Date:   Wed Nov 27 12:35:12 2024 +0000

    Update models.py
    - Se ajustaron los modelos para mejorar la estructura de la base de datos y añadir validaciones adicionales.

commit 118ead84c32cb0f0a891bbbabce63fa3d7497421
Author: Joseph <1234234403+JVC0@users.noreply.github.com>
Date:   Mon Dec 2 15:03:06 2024 +0000

    Update models.py
    - Se optimizaron los campos de los modelos para garantizar la integridad de los datos y mejorar la eficiencia.

commit a6889c2555c58b4e3c6fd9060c5a4b4c564fad12
Author: Kai <145053705+YoooKai@users.noreply.github.com>
Date:   Mon Dec 2 15:01:53 2024 +0000

    Update models.py
    - Se reorganizó el código para mejorar la legibilidad y mantenibilidad del archivo.

commit 024520291075db4de01f661bd15adb84e747a361
Author: Joseph <1234234403+JVC0@users.noreply.github.com>
Date:   Mon Dec 2 14:37:02 2024 +0000

    Update views.py
    - Se implementaron nuevas funcionalidades en las vistas para manejar mejor las solicitudes HTTP y mejorar la experiencia del usuario.

commit 95ff962a90ab7a487d1baf351b8ae42346f2391b
Author: YoooKai <kai97rg@gmail.com>
Date:   Thu Dec 5 22:22:14 2024 +0000

    Update styles
    - Se mejoró la interfaz de usuario con nuevos estilos CSS para una experiencia más moderna y responsive.

commit 6370b636b6471db1d2d7c0db1a650a58f1915d44
Author: Joseph <1234234403+JVC0@users.noreply.github.com>
Date:   Thu Nov 28 15:04:16 2024 +0000

    Delete docs directory
    - Se eliminó la carpeta de documentación obsoleta para mantener el repositorio limpio y organizado.

commit 085ae8b89bbbe18e53a11e2b7ce459fde79e240c
Author: Kai <145053705+YoooKai@users.noreply.github.com>
Date:   Thu Nov 28 15:04:45 2024 +0000

    Add files via upload
    - Se subieron nuevos archivos necesarios para el funcionamiento del proyecto.

commit ffec7186c29b2e75a1d56d3eaae78a9872bfe72a
Author: Joseph <1234234403+JVC0@users.noreply.github.com>
Date:   Thu Nov 28 15:03:15 2024 +0000

    Add files via upload
    - Se agregaron archivos adicionales para completar la estructura del proyecto.

commit 8d3053d0dff665104043237ddf9a6fbe8c5fd030
Author: Kai <145053705+YoooKai@users.noreply.github.com>
Date:   Thu Nov 28 14:59:29 2024 +0000

    Delete accounts directory
    - Se eliminó la carpeta `accounts` para reorganizar la estructura del proyecto y eliminar código redundante.

commit [Sin hash]
Author: Joseph <1234234403+JVC0@users.noreply.github.com>
Date:   Wed Nov 27 12:35:12 2024 +0000

    Update models.py
    - Se realizaron ajustes menores en los modelos para corregir errores y mejorar la eficiencia.
```
