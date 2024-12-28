Docker, GitHub Actions, Java Spring Boot y Dokku

Este proyecto demuestra cómo integrar Docker, GitHub Actions, Java Spring Boot y Dokku para crear un flujo de trabajo de desarrollo y despliegue automatizado. La aplicación es un servicio básico de Spring Boot que se ejecuta dentro de un contenedor Docker, se automatiza con GitHub Actions y se despliega usando Dokku.

Características

Docker: Empaqueta la aplicación Spring Boot en un contenedor para garantizar que se ejecute de la misma manera en cualquier entorno.

GitHub Actions: Automatiza el proceso de construcción, prueba y despliegue de la aplicación con cada cambio en el repositorio.

Java Spring Boot: Framework backend para el desarrollo de la aplicación web.

Dokku: Plataforma de despliegue similar a Heroku que usa contenedores Docker para gestionar aplicaciones de forma sencilla.


Estructura del Proyecto

Dockerfile: Archivo que define cómo crear la imagen Docker para el proyecto Spring Boot.

main.yml: Archivo de configuración para GitHub Actions que automatiza la construcción, pruebas y despliegue.

src/: Contiene el código fuente de la aplicación Spring Boot.

pom.xml: Archivo de configuración de Maven para las dependencias y construcción del proyecto.

dokku-deploy.sh: Script que automatiza el proceso de despliegue de la aplicación en un servidor remoto usando Dokku.


Instalación

Requisitos

Docker: Necesario para construir y ejecutar la aplicación en contenedores.

GitHub Actions: Se utiliza para la integración continua y automatización de procesos de despliegue.

Dokku: Necesitas un servidor remoto con Dokku instalado para gestionar el despliegue.

Java: Debes tener instalado Java y Maven para desarrollar la aplicación de backend con Spring Boot.

```
Estructura del Proyecto

DockerGHA2/
│
├── .github/
│   └── workflows/
│       └── main.yml             # Flujo de trabajo de GitHub Actions
├── Dockerfile                   # Dockerfile para contenerizar la app
├── README.md                    # Documentación del proyecto
├── src/
│   ├── main/
│   │   ├── java/
│   │   │   └── com/
│   │   │       └──  DominioApplication.java   # Clase principal de Spring Boot
│   │   └── resources/
│   │       └── application.properties         # Configuración de la app
├── target/                       # Directorio de build (generado por Maven/Gradle)
├── pom.xml                       # Archivo de configuración de Maven (si usas Maven)
└── .gitignore                    # Archivos y directorios que Git debe ignorar
```