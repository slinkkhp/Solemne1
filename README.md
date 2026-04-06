# Solemne1
Repositorio hecho para subir los archivos de la solemne 1 del grupo conformado por: Santiago Núñez y Benjamín Inzunza
# FeriaTech 2026 - Solemne 01 Práctico

## Integrantes
* Santiago Núñez y Benjamín Inzunza

## Descripción del Proyecto
Este proyecto es un micrositio web desarrollado para la "Feria Tecnológica Universitaria" de la Escuela de Ingeniería. El sitio busca difundir el evento, mostrar el cronograma de actividades, presentar a los expositores y permitir la inscripción de los estudiantes. Fue construido utilizando HTML5 semántico, CSS3 y Bootstrap 5, aplicando metodologías de diseño responsivo y TDD visual.

## Listado de Páginas
El sitio consta de 7 páginas interconectadas y coherentes visualmente:
1. `index.html`: Inicio y portada de la feria.
2. `objs.html`: (Sobre la feria) Descripción de la feria y la institución.
3. `actividades.html`: Cronograma detallado (CSS Puro).
4. `equipo.html`: (Expositores) Fichas de los expositores (Bootstrap 5).
5. `visual.html`: (Proyectos) Proyectos de innovación destacados.
6. `contacto.html`: Formulario de inscripción.
7. `faq.html`: Preguntas frecuentes y centro de ayuda (Bootstrap 5).

## Componentes Principales de Interfaz Utilizados
Para mantener una buena experiencia de usuario, se incorporaron los siguientes componentes según su categoría:

* Navegación: * Menú principal (`nav` y `ul`) en el encabezado de todas las páginas.
  * Componente `.navbar` de Bootstrap implementado en `equipo.html` y `faq.html`.
* Contenido: * Listas estructuradas y tablas semánticas (`table`) en la sección de cronograma.
  * Componente `.card` de Bootstrap utilizado para los perfiles de los expositores en `equipo.html` y para estructurar las preguntas en `faq.html`.
  * Grid de CSS para la galería de proyectos.
 * Interacción: * Formulario estructurado con etiquetas `input`, `email` y `label` en `contacto.html`.
  * Componente `.accordion` de Bootstrap en `faq.html` para desplegar respuestas.
  * Botones de acción (`.btn` y `.btn-primary`) en `equipo.html`.
* Feedback: * Componentes `.alert` y `.badge` de Bootstrap en `faq.html` para destacar avisos importantes y cupos de los talleres.

## Instrucciones de Ejecución con Docker
El proyecto está configurado para desplegarse fácilmente en un contenedor basado en Nginx. 

### Prerrequisitos
Tener Docker instalado y corriendo en el sistema.

### Pasos para levantar el sitio
1. Clonar este repositorio y abrir una terminal en la carpeta raíz del proyecto.
2. Construir la imagen de Docker ejecutando el siguiente comando:
   docker build -t feriatech-web .
3. Correr el docker para que se cargue la pagina:
   docker run -d -p 8080:80 --name mi-feria-container feria-web
4. Ingresar a la pagina mediante el link o mediante el mismo docker:
   localhost:8080
