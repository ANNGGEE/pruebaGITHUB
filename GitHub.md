# Práctica GitHub + MarkDown
## Ángela Gómez López

### INDICE
* [**Introducción**](#introducción)
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

1. **Acceder a la sección de Acciones**
   * Entra a tu repositorio de **GitHub**
   * Haz clic en la pestaña de _Actions_ en el menú superior
   * GitHub detectará automáticamente el lenguaje o tipo de proyecto de tu código y te mostrará sugerencias de plantillas de flujos de trabajo (_workflows_)
   * Si el repositorio todavía no tiene flujos de trabajo configurados, GitHub puede mostrarte sugerencias de plantillas según el lenguaje o el tipo de proyecto.

2. **Elegir o crear un flujo de trabajo (_Workflow_)**
   * **Usar una plantilla**: Selecciona una de las plantillas sugeridas (Node.js, Docker...) y haz clic en **Configure** o Configurar para adaptarla a las necesidades de tu proyecto.
   * **Crear un archivo manual:** Si prefieres crearlo desde cero o el directorio no existe:
     *   Ve a la pestaña principal del repositorio y haz clic en **Add file** y **Create new file**
     *   Nómbralo con la ruta y extensión _YAML_: **_.github/workflows/nombre-archivo.yml_**

       > Esta carpeta es importante, ya que GitHub Actions busca en ella los archivos que definen los flujos de trabajo del repositorio.

3. **Definir la estructura YAML del flujo**
   
   El archivo YAML contiene las instrucciones que indican cuándo y cómo se ejecutará el flujo de trabajo. Sus elementos principales son:
   * **name:** Establece el nombre visible de tu flujo de trabajo.
   * **on:** define los eventos que activarán su ejecución, como un _push_ o _pull_request_.
   * **jobs**: Define los trabajos que componen el flujo de trabajo (workflow). Cada trabajo se ejecuta en un entorno de ejecución (runner), que puede utilizar Linux, Windows o macOS. A su vez, cada trabajo está formado por una serie de pasos (steps) que se ejecutan de forma secuencial y que pueden consistir en comandos de consola o en el uso de acciones (actions) ya creadas por GitHub o por otros desarrolladores.
   * **steps:** especifica los pasos de cada trabajo, que pueden ejecutar comandos de consola o utilizar acciones previamente creadas por GitHub o por otros desarrolladores.
  
![workflow](https://user-images.githubusercontent.com/12570515/262074692-01e51004-343b-43dc-9f54-4662a69d7384.png)

4. **Guardar y ejecutar**
   * Una vez terminado el archivo, pulsa **Commit changes...** para guardar los cambios en el repositorio.
   * Si el archivo se incorpora a una rama y se produce uno de los eventos definidos en el YAML, _GitHub Actiones_ activrá el flujo de forma automática según el evento configurado (por ejemplo, al hacer un _push_).
   * Puedes volver a la pestaña **Actions** para monitorizar en tiempo real el progreso de cada paso y ver los registros (_logs_) de salida.
  
5. **Añadir acciones externas o personalizadas**
   * Puedes buscar acciones creadas por otros desarrolladores en el GitHub Marketplace e integrarlas en tus pasos con la sintaxis _uses: nombre-accion/version_
   * Esta acción permite obtener el código del repositorio en el entorno de ejecución para que los siguientes pasos puedan trabajar con él. La versión debe elegirse y mantenerse de acuerdo con las necesidades de seguridad y mantenimiento del proyecto.

En definitiva, GitHub Actions permite **automatizar tareas** como ejecutar pruebas, comprobar la calidad del código, generar compilaciones o desplegar aplicaciones, reduciendo la intervención manual y facilitando la integración continua y la entrega continua (CI/CD).

### **Conclusiones**
[Volver al índice](#indice)

### **Bibliografía**
[Volver al índice](#indice)
