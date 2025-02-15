# :simple-futurelearn: Conclusión y Futuro

¡Entiendo! Para la sección **Estado actual del proyecto**, puedes resumir el progreso y el alcance cumplido de manera clara y concisa, destacando que se han cumplido todos los requisitos establecidos en el PDF del profesor. Aquí tienes una propuesta de redacción:

---

## **Estado actual del proyecto**

### **Resumen del progreso y alcance cumplido**

El proyecto **LUMINO** ha alcanzado un estado de desarrollo completo, cumpliendo con todos los requisitos y funcionalidades especificados en el PDF proporcionado por el profesor. A continuación, se detalla el progreso y el alcance cumplido:

#### **1. Progreso general**

- **Requisitos cumplidos**: Se han implementado todas las funcionalidades requeridas, incluyendo la gestión de usuarios, matriculación en asignaturas, creación de lecciones, calificación de estudiantes y generación de certificados.
- **Pruebas y verificación**: El sistema ha sido probado exhaustivamente, superando los **100 tests** de pytest proporcionados por el profesor. Estos tests validan la funcionalidad de cada requisito, garantizando que todas las características del proyecto funcionen correctamente y cumplan con las expectativas establecidas.

#### **2. Alcance cumplido**

- **Gestión académica**:
  - Los estudiantes pueden matricularse en asignaturas, ver lecciones y solicitar certificados de calificaciones.
  - Los profesores pueden crear y gestionar lecciones, así como calificar a los estudiantes.
- **Autenticación y perfiles**:
  - Se ha implementado un sistema de autenticación para usuarios (estudiantes y profesores).
  - Los usuarios pueden editar sus perfiles, incluyendo la posibilidad de añadir una imagen de avatar y una biografía.
- **Interfaz de usuario**:
  - La interfaz es intuitiva y responsive, permitiendo una experiencia de usuario fluida tanto en dispositivos de escritorio como móviles.
  - Se ha implementado un sistema de notificaciones para informar a los usuarios sobre cambios importantes, como nuevas calificaciones o lecciones.

#### **3. Estado actual**

- **Código finalizado**: El código base del proyecto está completo y se ha entregado según lo solicitado. Sin embargo, reconocemos que hay margen de mejora, especialmente en términos de optimización, modularización y adherencia a buenas prácticas de desarrollo. Estas mejoras podrían implementarse en futuras iteraciones del proyecto.

## 2. **Futuras actualizaciones**

### **Funcionalidades o mejoras planificadas**

Aunque el proyecto ya se ha entregado, en caso de retomarse en el futuro, se podrían implementar las siguientes funcionalidades y mejoras:

#### **1. Notificaciones en tiempo real**

- Implementar un sistema de notificaciones en tiempo real para alertar a los estudiantes sobre nuevas calificaciones o lecciones.

#### **2. Autenticación con terceros**

- Permitir el inicio de sesión con cuentas de Google u otros proveedores externos para facilitar el acceso a la plataforma.

#### **3. Opción de "Olvidé mi contraseña"**

- Implementar una funcionalidad para que los usuarios puedan recuperar su contraseña recibiendo un correo electrónico con un enlace de restablecimiento.

#### **4. Interacción en lecciones**

- Añadir la posibilidad de que los estudiantes dejen preguntas en las lecciones, las cuales podrían ser contestadas por los profesores.

#### **5. Exámenes en línea**

- Implementar un sistema para realizar exámenes en línea directamente en **LUMINO**, con corrección automática o manual por parte de los profesores.

#### **6. Apartado de tareas**

- Crear un apartado de tareas para cada asignatura, donde los estudiantes puedan subir archivos y los profesores puedan corregirlos.

#### **7. Buscador de asignaturas**

- Añadir un buscador para que los usuarios puedan encontrar asignaturas según sus intereses.

#### **8. Seguimiento de lecciones completadas**

- Implementar un sistema para que los estudiantes puedan marcar las lecciones que han completado, fomentando la motivación y el progreso.

#### **9. Perfil mejorado**

- Mejorar el perfil del usuario, añadiendo un banner personalizado, más información y un historial de movimientos recientes.

#### **10. Sistema de premios**

- Implementar un sistema de premios o logros para motivar a los estudiantes a completar lecciones y tareas.

## 3. **Lecciones aprendidas**

### **Reflexión sobre el desarrollo y recomendaciones para futuros proyectos**

El desarrollo de **LUMINO** ha sido una experiencia enriquecedora que nos ha permitido aprender nuevas habilidades y mejorar nuestras prácticas de desarrollo. A continuación, se detallan las lecciones aprendidas y las recomendaciones para futuros proyectos:

#### **1. Uso de nuevas tecnologías y librerías**

- Durante el proyecto, utilizamos librerías y tecnologías que no habíamos empleado antes, como el envío de correos electrónicos a los usuarios. Esto nos permitió ampliar nuestro conocimiento y familiarizarnos con herramientas útiles para futuros desarrollos.
- También trabajamos con modelos de bases de datos que incluían relaciones **ManyToMany** y **ForeignKey**, lo que nos ayudó a comprender mejor cómo diseñar y gestionar relaciones complejas en Django.

#### **2. Atención a los detalles**

- Tras la corrección del profesor, nos dimos cuenta de la importancia de prestar atención a los detalles. Ambos tendemos al despiste y a la desorganización, por lo que esta experiencia nos ha enseñado a ser más meticulosos en la revisión del código y en el cumplimiento de las especificaciones del proyecto.

#### **3. Trabajo en equipo**

- Implementamos un sistema de turnos para trabajar en el mismo ordenador, lo que nos permitió acostumbrarnos a colaborar de manera más efectiva. Sin embargo, esta dinámica también nos presentó desafíos personales.
  - A uno de los miembros del equipo le resultó especialmente difícil trabajar siendo el que estaba frente al ordenador, ya que le cuesta concentrarse y pensar con alguien observando de cerca. Aunque esta situación le generaba nerviosismo, reconocemos que es una habilidad importante para el trabajo en equipo y el desarrollo colaborativo.
  - A pesar de las dificultades, esta experiencia nos ayudó a entender mejor las fortalezas y estilos de trabajo de cada uno, así como a integrar nuestras aportaciones al código de manera más coherente. También nos enseñó a ser más pacientes y comprensivos con las diferencias individuales.

#### **4. Proyecto más completo hasta la fecha**

- **LUMINO** es el proyecto más completo y extenso que hemos desarrollado hasta ahora. Esto nos ha permitido enfrentarnos a desafíos técnicos y organizativos que no habíamos experimentado en proyectos anteriores, lo que ha sido fundamental para nuestro crecimiento como desarrolladores.

#### **5. Recomendaciones para futuros proyectos**

- **Revisitar el código**: Es recomendable revisar el código con tiempo antes de la fecha de entrega para identificar áreas de mejora y aplicar refactorizaciones necesarias.
- **Commits útiles**: Realizar commits con comentarios descriptivos y útiles, evitando mensajes vagos o de una sola letra. Esto facilita el seguimiento de los cambios y mejora la colaboración en equipo.
- **Organización y planificación**: Utilizar herramientas como las funcionalidades de gestión de tareas de GitHub para crear una agenda clara de lo que queda por hacer y asignar responsabilidades. Esto ayuda a mantener un proceso de desarrollo más organizado y eficiente.
- **Pruebas tempranas**: Realizar pruebas continuas durante el desarrollo para detectar errores a tiempo y evitar problemas en fases avanzadas del proyecto.
- **Comunicación y empatía**: Fomentar una comunicación clara y abierta entre los miembros del equipo, reconociendo y respetando las diferencias individuales en cuanto a estilos de trabajo y preferencias.
