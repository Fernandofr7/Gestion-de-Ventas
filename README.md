# Sistema de Gestión de Ventas 
Este proyecto fue desarrollado como parte de un sistema de ventas integral utilizando Java NetBeans. Requieren manejar productos, clientes y generar reportes, con funcionalidades como escaneo por código de barras, generación de reportes con iReport y conexión a una base de datos MySQL alojada en Heroku.

---

## Características principales ✨

- Gestión de productos, clientes y ventas.
- Conexión a base de datos remota (MySQL en Heroku).
- Reportes en PDF generados con iReport (JasperReports).
- Escaneo de productos mediante código de barras.
- Interfaz gráfica intuitiva hecha con Java Swing.
- Uso del driver JDBC para conexión segura a la base de datos.

---

## Tecnologías utilizadas 🛠️

- **Java (SE)** – Lógica de negocio y UI (Swing)
- **NetBeans IDE** – Entorno de desarrollo
- **MySQL** – Base de datos relacional
- **Heroku ClearDB** – Plataforma para alojar la base de datos en la nube
- **JDBC Driver** – Conector entre Java y MySQL
- **iReport / JasperReports** – Herramienta de reportes
- **ZXing** – Biblioteca para leer códigos de barras (opcional)

---

## Instalación local 🔧

1. **Clonar el repositorio:**

    git clone

2. **Abrir el proyecto en NetBeans:**
   - Archivo > Abrir Proyecto > Selecciona la carpeta clonada.

3. **Configurar la base de datos:**
   - Crea una base en MySQL local o usa tu URL de Heroku ClearDB.
   - Importa el archivo `.sql` desde la carpeta `/database`.

4. **Actualizar la clase de conexión:**
   - Abre `Conexion.java` o clase equivalente.
   - Asegúrate de usar `com.mysql.cj.jdbc.Driver` y la URL con `?serverTimezone=UTC`.

5. **Asegúrate de tener estas librerías en tu proyecto:**
   - `mysql-connector-java-x.x.x.jar`
   - `jasperreports-x.x.x.jar`
   - `ireport.jar` (si fue embebido)
   - `zxing-core.jar` (para lectura de códigos de barras)

---

## Uso 🖥️

- Inicia el proyecto desde `Main.java` o la clase que contenga el método `main`.
- Ingresa con las credenciales de ejemplo o crea un nuevo usuario.
- Usa el escáner de código de barras para ingresar productos rápidamente.
- Genera reportes desde los botones disponibles en la interfaz.
- Verifica que la conexión con Heroku esté activa para operaciones remotas.
- **Uso local con XAMPP:**
  - Activa Apache y MySQL desde el panel de XAMPP.
  - Asegúrate de que la base de datos `ventas` esté creada.
  - Usa `root` sin contraseña o ajusta según tu configuración local.

---

## Despliegue en Heroku 🌐

> Solo aplica si decides subir la base de datos a Heroku:

- Crea una cuenta en Heroku y añade el complemento **ClearDB**.
- Copia la URL del ClearDB e intégrala en tu clase `Conexion.java`.
- Asegúrate que tu IP no esté bloqueada si usas conexiones remotas.

---

