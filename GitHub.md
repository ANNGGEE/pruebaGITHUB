# Práctica GitHub + MarkDown
## Ángela Gómez López

### INDICE
* [**Introducción**](#introduccion)
* [**¿Qué vamos a ver en este informe?**](#qué-vamos-a-ver-en-este-informe)
* [**Usos de GitHub**](#usos-de-github)
* [**Acciones**](#pasos-a-seguir-para-conseguir-las-diferentes-acciones)
* [**Conclusiones**](#conclusiones)
* [**Bibliografía**](#bibliografia)

![Imagen GitHub](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTEIWBtXQlfZSFnUMVJ98xa2cbwoDF1pvYcKH2eZgsQhQ&s=10)

### Introducción 
[Volver al índice](#indice)

GitHub es una plataforma en la nube y una red social para desarrolladores que permite almacenar, administrar y trabajar en proyectos de software de forma individual y colaborativa.

### ¿Qué vamos a ver en este informe?
[Volver al índice](#indice)

En este informe se va a hablar de los usos de esta plataforma, de los pasos a seguir para conseguir diferentes acciones, además de una pequeña conclusión de los puntos tratados en el documento. 

### **Usos de GitHub**
[Volver al índice](#indice)

* **Almacenamiento en la nube:** GitHub permite guardar los proyectos en la nube mediante repositorios, que contienen los archivos y el historial de cambios de un proyecto. Esto facilita mantener una copia del trabajo en Internet y recuperarlo si se pierde información, falla el ordenador u ocurre cualquier imprevisto. Además, permite acceder a los archivos desde distintos dispositivos, compartirlos con otras personas y trabajar en equipo sin perder el seguimiento de las modificaciones realizadas.
* **Control de versiones con Git:** Funciona sobre _Git_, que es un sistema creado para rastrear cambios en el código. Guarda cada modificación, permitiendo regresar a versiones anteriores si es necesario.
* **Trabajo en equipo:** Facilita que varias personas editen el mismo proyecto al mismo tiempo sin interferir en el trabajo de los demás mediante _ramas_ (branches) y _peticiones de extracción_ (pull request). 
* **Repositorios públicos y privados:** Puedes alojar código abierto para que otros lo usen o contribuyan, o mantener proyectos privados. 
* **Portafolio profesional:** GitHub funciona como un _portafolio profesional_ donde los programadores pueden mostrar sus proyectos, códigos y habilidades. Además, permite a los reclutadores conocer su experiencia y valorar sus competencias técnicas como complemento al currículum.
* **Herramientas avanzadas:** Incluye funciones de automatización, gestión de tareas e inteligencia artificial, como puede ser GitHub Copilot.

### **Pasos a seguir para conseguir las diferentes acciones**
[Volver al índice](#indice)

![Imagen de Acciones de GitHub](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR8kXfpHcyHLwPf80EIHHqgpyXMQF3M4oxN75mbz4rVpg&s=10)


Antes de proceder con los pasos primero hay que entender _**qué son las acciones de GitHub**_. Las acciones de GitHub o _GitHub Actions_ son una herramienta de automatización integrada directamente en la plataforma de GitHub que te permite crear flujos de trabajo (workflows) para compilar, probar, empaquetar, liberar o implementar tu código.
Todo esto es bastante útil para la _integración y entrega continua_, _la automatización de tareas repetitivas_ o el _soporte multi-lenguage_. 

**Algunos conceptos clave pueden ser:** 
* Flujos de trabajo (workflows): Procesos automatizados y configurables que se definen en tu repositorio mediante archivos de texto con formato YAML.
* Eventos (Events): Desencadenantes que inician un flujo de trabajo, por ejemplo, cuando alguien hace _push_, se abre una solicitud de extracción de _pull request_, o según una programación de hora.
* Acciones (Actions): Son bloques de código individuales, reutilizables y empaquetados que realizan tareas específicas dentro de un flujo de trabajo.
* Ejecutadores (Runners): Son las máquinas virtuales proporcionadas por GitHub donde se ejecutan realmente estos códigos y tareas.
* GitHub Marketplace: Un directorio donde puedes encontrar y utilizar miles de acciones creadas por la comunidad y por diversas empresas para ahorrar tiempo.

![Imagen de los conceptos](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSr_1szYYhGP-MPANk_556BeWtxpdiD9JCxdqdCqgbLSS2Ny6QPC82sjoQ&s=10)

Ahora sí una vez explicado y entendido el funcionamiento y los conceptos clave vamos a ver los **pasos a seguir para conseguir estas acciones**: 

1. Acceder a la sección de Acciones:
   * Entra a tu repositorio de **GitHub**
   * Haz clic en la pestaña de _Actions_ en el menú superior
   * GitHub detectará automáticamente el lenguaje o tipo de proyecto de tu código y te mostrará sugerencias de plantillas de flujos de trabajo (_workflows_)

2. Elegir o crear un flujo de trabajo (_Workflow_)
   * **Usar una plantilla**: Selecciona una de las plantillas sugeridas (Node.js, Docker...) y haz clic en **Configure** o Configurar
   * **Crear un archivo manual:** Si prefieres crearlo desde cero o el directorio no existe:
     *   Ve a la pestaña principal del repositorio y haz clic en **Add file** y **Create new file**
     *   Nómbralo con la ruta y extensión _YAML_: **_.github/workflows/nombre-archivo.yml_**

3. 
