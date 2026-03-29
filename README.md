# Sistema de Gestión de Gimnasio 

Un sistema integral desarrollado en Java para la administración de las operaciones principales de un gimnasio. Este proyecto implementa los principios de la Programación Orientada a Objetos (POO) y utiliza el patrón de diseño de Repositorios para gestionar la persistencia de datos con una base de datos relacional.

## Características Principales

El sistema está dividido en varios módulos accesibles a través de menús interactivos:

* **Gestión de Suscriptores:** Registro, actualización y consulta de los clientes del gimnasio.
* **Gestión de Instructores:** Administración del personal que imparte las clases.
* **Gestión de Cursos/Clases:** Creación y asignación de cursos dentro del gimnasio.
* **Control de Asistencias:** Registro de entrada y asistencia de los suscriptores.
* **Control de Pagos:** Seguimiento de las mensualidades y pagos realizados.
* **Gestión de Usuarios:** Administración de los usuarios que tienen acceso al sistema (recepcionistas, administradores).

##  Tecnologías y Herramientas

* **Lenguaje:** Java (POO)
* **Base de Datos:** MariaDB / MySQL
* **Driver JDBC:** `mariadb-java-client-3.3.2.jar`
* **Arquitectura:** Separación en capas (Modelos, Repositorios, Menús, Utilidades)
* **Scripts de ejecución:** Archivos Batch (`.bat`) para facilitar la compilación y pruebas en Windows.

##  Estructura del Proyecto

El código fuente (`src/`) está organizado de la siguiente manera:

* `/modelos`: Clases base que representan las entidades del dominio (`Suscriptor`, `Instructor`, `Pago`, `Asistencia`, `Curso`, `Usuario`).
* `/Repositorios`: Clases encargadas de la lógica de acceso a datos y las consultas SQL (ej. `SuscriptorRepo`, `PagoRepository`).
* `/Menus`: Interfaces de línea de comandos para interactuar con cada módulo del sistema (`MainMenu`, `MenuPagos`, etc.).
* `/util`: Clases de configuración, como `DatabaseConnection.java` para establecer el enlace con la base de datos.
* `/lib`: Contiene las librerías necesarias, como el driver JDBC de MariaDB.

##  Requisitos Previos

1.  Tener instalado el **Java Development Kit (JDK)** y configurado en las variables de entorno (`PATH`).
2.  Tener un servidor de base de datos **MariaDB** o **MySQL** en ejecución.
3.  Configurar las credenciales de la base de datos dentro de `src/util/DatabaseConnection.java`.

##  Cómo compilar y ejecutar

El proyecto incluye scripts `.bat` para facilitar el proceso desde la terminal de Windows:

1.  **Descargar dependencias (si aplica):**
    Puedes usar `descargar_driver.bat` si necesitas descargar el conector JDBC nuevamente.
2.  **Compilar el proyecto:**
    Ejecuta el archivo `compilar_completo.bat` para compilar todo el código fuente. Las clases compiladas se guardarán en las carpetas correspondientes (`bin/` o `classes/`).
3.  **Ejecutar el sistema:**
    Para iniciar la aplicación y abrir el menú principal, ejecuta:
    ```bash
    ejecutar_sistema_completo.bat
    ```
4.  **Ejecución modular:**
    Si deseas probar un módulo en específico sin pasar por el menú principal, puedes ejecutar los scripts individuales como:
    * `ejecutar_menu_suscriptores.bat`
    * `ejecutar_menu_pagos.bat`
    * `ejecutar_menu_instructores.bat`


