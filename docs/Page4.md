# Implementación

## 1. Estructura del Código

#### Organización del repositorio y convenciones usadas

El proyecto **LUMINO** sigue una estructura de carpetas y convenciones claras para garantizar la organización y mantenibilidad del código. A continuación, se describe la estructura principal del repositorio:

- **`/lumino/`**:  
  Contiene el código principal del proyecto, incluyendo la configuración de Django (`settings.py`, `urls.py`, etc.) y las aplicaciones principales (`accounts`, `subjects`, `users`, etc.).

- **`/templates/`**:  
  Almacena las plantillas HTML utilizadas para renderizar las vistas. Las plantillas están organizadas por aplicaciones (por ejemplo, `templates/accounts/`, `templates/subjects/`).

- **`/static/`**:  
  Contiene archivos estáticos como hojas de estilo CSS, scripts JavaScript e imágenes. Estos archivos se organizan en subcarpetas por tipo (por ejemplo, `static/css/`, `static/js/`, `static/images/`).

- **`/media/`**:  
  Almacena archivos multimedia subidos por los usuarios, como avatares de perfil y certificados generados en formato PDF.

- **`/locale/`**:  
  Contiene los archivos de traducción para la internacionalización (i18n) de la plataforma, permitiendo soporte para múltiples idiomas (español e inglés).

- **`/templatetags/`**:  
  Incluye etiquetas personalizadas de Django utilizadas en las plantillas para añadir lógica personalizada o reutilizable.

- **`/management/`**:  
  Contiene comandos personalizados de gestión de Django, como el comando para generar estadísticas de asignaturas (`get_subject_stats.py`).

- **`/tests/`**:  
  Almacena los tests unitarios y de integración del proyecto, organizados por aplicaciones (por ejemplo, `tests/test_models.py`, `tests/test_views.py`).

- **`/decorators/`**:  
  Contiene decoradores personalizados utilizados para controlar el acceso a vistas específicas (por ejemplo, `@professor_required`, `@student_required`).

- **`/helpers/`**:  
  Incluye funciones auxiliares y utilidades reutilizables en todo el proyecto, como la generación de certificados o el envío de correos electrónicos.

- **`/fixtures/`**:  
  Contiene archivos JSON con datos de prueba, como usuarios, asignaturas (`subjects`), lecciones (`lessons`) y matriculaciones (`enrollments`). Estos datos se cargan en la base de datos utilizando el comando `just load-data`, tal como indicó el profesor.

---

### **Convenciones Usadas**

<ol>
  <li><strong>Nombres de archivos y carpetas:</strong>
    <ul>
      <li>Se utilizan nombres en <strong>minúsculas</strong> y separados por guiones (<code>-</code>) para archivos y carpetas.</li>
    </ul>
  </li>
  <li><strong>Organización por aplicaciones:</strong>
    <ul>
      <li>Cada aplicación de Django (<code>accounts</code>, <code>subjects</code>, <code>users</code>, etc.) sigue la estructura estándar de Django (<code>models.py</code>, <code>views.py</code>, <code>urls.py</code>, etc.).</li>
    </ul>
  </li>
  <li><strong>Código limpio:</strong>
    <ul>
      <li>Se intentan seguir las mejores prácticas de <strong>PEP 8</strong> para la escritura de código Python.</li>
    </ul>
  </li>
  <li><strong>Control de versiones:</strong>
    <ul>
      <li>Se utiliza <strong>Git</strong> para el control de versiones.</li>
    </ul>
  </li>
</ol>

---

## 2. Tecnologías y herramientas

#### Lenguajes, frameworks, bibliotecas y entornos de desarrollo

A continuación, se detallan las principales tecnologías y herramientas utilizadas en el desarrollo de **LUMINO**:

<ol>
  <li><strong>Django:</strong>
    <ul>
      <li>Framework de alto nivel y orientado a la productividad, diseñado para desarrollar aplicaciones web complejas de manera rápida y eficiente, como la gestión académica que requiere LUMINO.</li>
      <li>Proporciona herramientas integradas para autenticación, administración de bases de datos y seguridad, lo que acelera el desarrollo y reduce la necesidad de implementar funcionalidades desde cero.</li>
    </ul>
  </li>
  <li><strong>SQLite (desarrollo):</strong>
    <ul>
      <li>Base de datos simple y rápida, utilizada durante el desarrollo por su facilidad de configuración.</li>
      <li>Permite una migración sencilla a sistemas más robustos como <strong>PostgreSQL</strong> o <strong>MySQL</strong> en producción.</li>
    </ul>
  </li>
  <li><strong>Django-RQ + Redis:</strong>
    <ul>
      <li>Gestiona tareas en segundo plano (por ejemplo, el envío de certificados en PDF) de manera eficiente.</li>
      <li><strong>Redis</strong> actúa como broker para manejar colas de tareas asíncronas.</li>
    </ul>
  </li>
  <li><strong>Bootstrap:</strong>
    <ul>
      <li>Framework de diseño frontend que proporciona una interfaz moderna y responsiva.</li>
      <li>Incluye soporte para temas claros y oscuros, mejorando la experiencia del usuario.</li>
    </ul>
  </li>
  <li><strong>Pillow:</strong>
    <ul>
      <li>Biblioteca para la manipulación de imágenes, utilizada para gestionar avatares de usuario y otros archivos multimedia.</li>
    </ul>
  </li>
  <li><strong>Model-Bakery:</strong>
    <ul>
      <li>Herramienta para la generación de datos de prueba en pruebas automatizadas, facilitando la creación de entornos de prueba realistas.</li>
    </ul>
  </li>
  <li><strong>CrispyForms:</strong>
    <ul>
      <li>Biblioteca que permite crear formularios atractivos y funcionales, integrando estilos de Bootstrap de manera sencilla.</li>
    </ul>
  </li>
  <li><strong>Markdownify:</strong>
    <ul>
      <li>Proporciona soporte para <strong>Markdown</strong> en la creación de contenido, permitiendo a los profesores formatear lecciones de manera eficiente.</li>
    </ul>
  </li>
  <li><strong>Sorl-Thumbnail:</strong>
    <ul>
      <li>Biblioteca para la creación de miniaturas de imágenes, optimizando el rendimiento y la carga de la plataforma.</li>
    </ul>
  </li>
</ol>

## 3. Instrucciones de configuración

Para poner en marcha el proyecto Lumino, sigue estos pasos:

<ol>
  <li><strong>Crear y activar el entorno virtual:</strong>
    <p>Es fundamental crear un entorno virtual para aislar las dependencias del proyecto. Ejecuta los siguientes comandos en la terminal:</p>
    <pre><code>python -m venv .venv --prompt lumino
source .venv/bin/activate</code></pre>
  </li>
  <li><strong>Aplicar las migraciones de la base de datos:</strong>
    <p>Django utiliza migraciones para gestionar la estructura de la base de datos según los modelos definidos. Aplica las migraciones ejecutando:</p>
    <pre><code>./manage.py migrate</code></pre>
  </li>
  <li><strong>Crear un superusuario:</strong>
    <p>El superusuario es necesario para acceder a la interfaz de administración de Django. Crea uno con el comando:</p>
    <pre><code>./manage.py createsuperuser</code></pre>
    <p>Sigue las instrucciones en la terminal para ingresar:</p>
    <ul>
      <li>Nombre de usuario</li>
      <li>Correo electrónico (opcional)</li>
      <li>Contraseña</li>
    </ul>
  </li>
  <li><strong>Instalar las dependencias:</strong>
    <p>Las dependencias del proyecto están listadas en el archivo <code>requirements.txt</code>. Instálalas con:</p>
    <pre><code>pip install -r requirements.txt</code></pre>
  </li>
  <li><strong>Ejecutar el servidor de desarrollo:</strong>
    <p>Para probar la aplicación localmente, inicia el servidor de desarrollo de Django:</p>
    <pre><code>python manage.py runserver</code></pre>
  </li>
  <li><strong>Configurar variables de entorno:</strong>
    <p>Crea un archivo <code>.env</code> en el directorio raíz del proyecto para almacenar configuraciones sensibles como:</p>
    <ul>
      <li>Claves secretas (<code>SECRET_KEY</code>)</li>
      <li>Credenciales de base de datos</li>
      <li>Otros parámetros necesarios para la aplicación</li>
    </ul>
  </li>
  <li><strong>Configurar Django-RQ:</strong>
    <ul>
      <li>Asegúrate de tener Redis instalado y en ejecución.</li>
      <li>En el archivo <code>settings.py</code>, configura Django-RQ agregando credenciales y datos relevantes, como contraseña o correo electrónico asociado.</li>
    </ul>
  </li>
  <li><strong>Comandos simplificados con Justfile:</strong>
    <p>Si estás utilizando el <code>Justfile</code> proporcionado, puedes simplificar muchos de estos pasos. Consulta los comandos disponibles en ese archivo para agilizar la configuración.</p>
  </li>
</ol>
