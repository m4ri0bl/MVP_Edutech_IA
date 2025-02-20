# EduTech IA - MVP

Bienvenido al repositorio del MVP de **EduTech IA**, una plataforma digital diseñada para adaptar cursos y contenidos educativos al perfil y necesidades de cada usuario. Este proyecto se desarrolló utilizando Java y el paradigma de Programación Orientada a Objetos (POO), siguiendo una arquitectura basada en el patrón Modelo-Vista-Controlador (MVC) para garantizar modularidad, escalabilidad y mantenibilidad.

## Características

- **Personalización de Contenidos:** La plataforma adapta cursos y materiales de acuerdo al perfil y necesidades específicas de cada usuario.
- **Arquitectura MVC:** Separación clara de la lógica de negocio, presentación y control, facilitando la ampliación y el mantenimiento del sistema.
- **Integración y Entrega Continua (CI/CD):** Pipeline automatizado que abarca pruebas, compilación, empaquetado y despliegue.
- **Contenerización con Docker:** Garantiza la consistencia entre los entornos de desarrollo, pruebas y producción.
- **Medidas de Seguridad Integradas:** Implementación de prácticas de codificación segura, análisis de vulnerabilidades y pruebas de penetración.

## Tecnologías Utilizadas

- **Lenguaje:** Java
- **Paradigma:** Programación Orientada a Objetos (POO)
- **Arquitectura:** Modelo-Vista-Controlador (MVC)
- **IDE:** IntelliJ IDEA
- **Control de Versiones:** Git y GitHub
- **Integración Continua:** GitLab CI/CD
- **Contenerización:** Docker

## Estructura del Proyecto


## Configuración del Entorno y Herramientas

El proyecto se apoya en las siguientes herramientas para asegurar un desarrollo ágil y colaborativo:

- **IntelliJ IDEA:** IDE recomendado para el desarrollo, depuración y refactorización del código.
- **Git/GitHub:** Gestión centralizada del código y colaboración en equipo.
- **GitLab CI/CD:** Automatización del pipeline de integración y entrega continua. Cada commit activa un webhook que inicia el pipeline para compilar, probar y desplegar la aplicación.
- **Docker:** Contenerización de la aplicación para replicar de manera exacta el entorno de producción en cada fase del desarrollo.

## Pipeline de CI/CD

El proceso automatizado de integración y entrega se estructura en varias etapas:

1. **Commit y Activación del Webhook:**  
   Cada commit en GitHub dispara un webhook que inicia el pipeline en GitLab CI/CD.

2. **Construcción y Compilación:**  
   El pipeline clona el repositorio y compila el proyecto en Java, generando logs en tiempo real para verificar la correcta compilación.

3. **Ejecución de Pruebas:**  
   Se ejecutan pruebas unitarias e integrales. Si alguna prueba falla, el proceso se detiene y se notifica al equipo de desarrollo.

4. **Empaquetado y Creación de la Imagen Docker:**  
   Tras la aprobación de las pruebas, se genera una imagen Docker que encapsula el código, dependencias y configuraciones necesarias.

5. **Despliegue en Entorno de Pruebas (Staging):**  
   La imagen Docker se despliega en un entorno de pruebas que replica fielmente las condiciones de producción para validaciones adicionales.

6. **Monitoreo y Notificaciones:**  
   Durante el proceso, se monitorea el rendimiento y se generan notificaciones automáticas sobre el estado de cada etapa.

## Medidas de Seguridad

La seguridad está integrada en cada fase del desarrollo mediante:

- **Seguridad desde el Diseño:**  
  Mecanismos de autenticación, autorización, cifrado y manejo seguro de errores implementados desde la concepción del proyecto.

- **Prácticas de Codificación Segura:**  
  Adopción de directrices OWASP para prevenir vulnerabilidades comunes mediante la validación y sanitización de todas las entradas de usuario.

- **Análisis de Vulnerabilidades:**  
  Pruebas de penetración y análisis estático para identificar y mitigar riesgos antes del despliegue en producción.

- **Configuración Segura:**  
  Aplicación del principio de "privilegio mínimo" en todos los entornos para limitar el acceso a lo estrictamente necesario.

## Despliegue en Entorno de Pruebas

El despliegue se realiza en un entorno de pruebas (staging) para garantizar que la aplicación funcione correctamente antes de pasar a producción. Este proceso utiliza Docker para replicar las condiciones reales de producción y permite:

- **Validación Funcional y de Rendimiento:**  
  Ejecución de pruebas adicionales para confirmar la integridad y desempeño de la aplicación.

- **Monitoreo Continuo:**  
  Seguimiento en tiempo real mediante dashboards y sistemas de alertas para detectar y resolver posibles incidencias.

- **Retroalimentación Inmediata:**  
  Notificaciones automáticas que informan sobre el éxito del despliegue o la detección de errores.
