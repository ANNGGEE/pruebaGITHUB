# Práctica GitHub + MarkDown: GitHub, funciones, herramientas y usos principales
## Ángela Gómez López

### INDICE
* [**Introducción**](#introduccion)
* [**¿Qué vamos a ver en este informe?**](#qué-vamos-a-ver-en-este-informe)
* [**Usos de GitHub**](#usos-de-github)
    * [**Funciones básicas de GitHub**](#funciones-basicas-de-github)
* [**Pasos a seguir para conseguir las diferentes acciones**](#pasos-a-seguir-para-conseguir-las-diferentes-acciones)
    * [**Procedimientos paso a paso**](#procedimientos-paso-a-paso)
      * [**Crear un repositorio**](#crear-un-repositorio)
      * [**Subir archivos a un repositorio**](#subir-archivos-a-un-repositorio)
      * [**Realizar un commit**](#realizar-un-commit)
      * [**Crear y utilizar ramas**](#crear-y-utilizar-ramas)
      * [**Crear una pull request**](#crear-una-pull-request)
      * [**Gestionar incidencias con GitHub Issues**](#gestionar-incidencias-con-github-issues)
      * [**Publicar una página web con GitHub Pages**](#publicar-una-pagina-web-con-github-pages)
    * [**Conceptos clave de GitHub Actions**](#conceptos-clave-de-github-actions)
    * [**Cómo configurar y utilizar GitHub Actions**](#cómo-configurar-y-utilizar-github-actions)
      * [**Acceder a la sección de Actions**](#acceder-a-la-seccion-de-actions)
      * [**Elegir o crear un workflow**](#elegir-o-crear-un-workflow)
      * [**Definir la estructura YAML**](#definir-la-estructura-yaml)
      * [**Guardar y ejecutar**](#guardar-y-ejecutar)
      * [**Añadir acciones externas o personalizadas**](#añadir-acciones-externas-o-personalizadas)
* [**Conclusiones**](#conclusiones)
* [**Bibliografía**](#bibliografia)

![Imagen GitHub](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcTEIWBtXQlfZSFnUMVJ98xa2cbwoDF1pvYcKH2eZgsQhQ&s=10)

## Introducción 
[Volver al índice](#indice)

GitHub es una plataforma de desarrollo colaborativo que permite alojar repositorios Git en la nube, gestionar proyectos, revisar cambios y compartir código con otras personas. Se utiliza tanto en el ámbito educativo como en el profesional, ya que facilita el trabajo en equipo, la organización de proyectos y el desarrollo de software.

Además, ofrece diferentes herramientas que permiten gestionar tareas, revisar modificaciones y automatizar determinados procesos, lo que contribuye a mejorar la organización y la eficiencia durante el desarrollo de un proyecto.

## ¿Qué vamos a ver en este informe?
[Volver al índice](#indice)

En este informe se presentan los principales usos de GitHub y se explican, paso a paso, algunas de sus funciones más importantes, como la creación de repositorios, la subida de archivos, el uso de ramas, las pull requests, la gestión de incidencias y la publicación de páginas web. Asimismo, se introduce GitHub Actions, una herramienta que permite automatizar tareas mediante flujos de trabajo. Finalmente, se incluyen unas conclusiones sobre la utilidad de esta plataforma y los conocimientos adquiridos.

## **Usos de GitHub**
[Volver al índice](#indice)

* **Almacenamiento en la nube:** GitHub permite guardar los proyectos en la nube mediante repositorios, que contienen los archivos y el historial de cambios de un proyecto. Esto facilita mantener una copia del trabajo en Internet y recuperarlo si se pierde información, falla el ordenador u ocurre cualquier imprevisto. Además, permite acceder a los archivos desde distintos dispositivos, compartirlos con otras personas y trabajar en equipo sin perder el seguimiento de las modificaciones realizadas.
* **Control de versiones con Git:** GitHub se basa en _Git_, un sistema de control de versiones que permite registrar y seguir los cambios realizados en los archivos de un proyecto. Mediante los _commits_, _Git_ guarda registros de esos cambios y facilita consultar el historial y recuperar versiones anteriores cuando sea necesario.
* **Trabajo en equipo:** GitHub facilita la colaboración entre varias personas en un mismo proyecto. Las _ramas (branches)_ permiten trabajar en modificaciones de forma independiente sin alterar directamente la rama principal. Posteriormente, mediante las solicitudes de extracción (_pull requests_), los colaboradores pueden revisar los cambios, proponer mejoras y decidir si se incorporan al proyecto principal. De esta manera, se facilita la coordinación y se reducen los posibles conflictos entre modificaciones.
* **Repositorios públicos y privados:** Puedes alojar código abierto para que otros lo usen o contribuyan, o mantener proyectos privados. 
* **Portafolio profesional:** GitHub funciona como un _portafolio profesional_ donde los programadores pueden mostrar sus proyectos, códigos y habilidades. Además, permite a los reclutadores conocer su experiencia y valorar sus competencias técnicas como complemento al currículum.
* **Herramientas avanzadas:** Incluye funciones de automatización, gestión de tareas e inteligencia artificial, como puede ser GitHub Copilot.

### Funciones básicas de GitHub
[Volver al índice](#indice)

Además de los usos mencionados anteriormente, GitHub permite realizar diferentes acciones para gestionar y desarrollar proyectos. Entre las más importantes se encuentran:

 * Crear repositorios: organizar y almacenar los archivos de un proyecto.
 * Subir archivos: añadir documentos, imágenes y código a un repositorio.
 * Realizar commits: guardar un registro de los cambios realizados.
 * Crear ramas: trabajar en modificaciones sin alterar directamente la rama principal.
 * Crear pull requests: proponer y revisar cambios antes de incorporarlos al proyecto.
 * Gestionar incidencias con GitHub Issues: registrar errores, tareas y propuestas de mejora.
 * Publicar páginas web con GitHub Pages: crear sitios web estáticos a partir de un repositorio.

## **Pasos a seguir para conseguir las diferentes acciones**
[Volver al índice](#indice)

![Imagen de Acciones de GitHub](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcR8kXfpHcyHLwPf80EIHHqgpyXMQF3M4oxN75mbz4rVpg&s=10)

### **Conceptos clave de GitHub Actions:** 
[Volver al índice](#indice)

Antes de explicar _cómo configurar y utilizar GitHub Actions_, conviene conocer algunos conceptos fundamentales sobre su funcionamiento.
Las acciones de GitHub o _GitHub Actions_ son una herramienta de automatización integrada directamente en la plataforma de GitHub que te permite crear flujos de trabajo (workflows) para compilar, probar, empaquetar, liberar o implementar tu código.
Esta herramienta resulta especialmente útil para la integración y entrega continuas (CI/CD), la automatización de tareas repetitivas y la ejecución de procesos en diferentes entornos de desarrollo.

**Algunos conceptos clave pueden ser:** 
* Flujos de trabajo (workflows): Procesos automatizados y configurables que se definen en tu repositorio mediante archivos de texto con formato YAML.
* Eventos (Events): Desencadenantes que inician un flujo de trabajo, por ejemplo, cuando alguien hace _push_, se abre una solicitud de extracción de _pull request_, o según una programación de hora.
* Acciones (Actions): Son bloques de código individuales, reutilizables y empaquetados que realizan tareas específicas dentro de un flujo de trabajo.
* Ejecutores (Runners): Son las máquinas virtuales proporcionadas por GitHub donde se ejecutan realmente estos códigos y tareas.
* GitHub Marketplace: Un directorio donde puedes encontrar y utilizar miles de acciones creadas por la comunidad y por diversas empresas para ahorrar tiempo.

![Imagen de los conceptos](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSr_1szYYhGP-MPANk_556BeWtxpdiD9JCxdqdCqgbLSS2Ny6QPC82sjoQ&s=10)

### **Procedimientos paso a paso** 
[Volver al índice](#indice)

A continuación, se explican algunas de las **funciones básicas de GitHub**, necesarias para comprender mejor el funcionamiento de _GitHub Actions_.

#### 1. **Crear un repositorio**
[Volver al índice](#indice)

Un _repositorio_ es un espacio donde se almacenan los archivos de un proyecto y su historial de modificaciones. Puede ser **público**, para que cualquier persona pueda verlo, o **privado**, para limitar su acceso a los usuarios autorizados.

**Pasos para crear un repositorio:**

    1. Inicia sesión en _GitHub_.
    2. Haz clic en el **símbolo +**, situado en la parte superior derecha, y selecciona _New repository_.
    3. Escribe un nombre para el repositorio y, si lo deseas, añade una descripción.
    4. Selecciona si será **público (Public)** o **privado (Private)**.
    5. Opcionalmente, marca la casilla para añadir un archivo _README_, que servirá para describir el proyecto.
    6. Pulsa _Create repository_ para finalizar.

Una vez creado, podrás añadir archivos, organizar el proyecto y colaborar con otros usuarios.

#### 2. **Subir archivos a un repositorio**
[Volver al índice](#indice)

GitHub permite almacenar archivos de diferentes tipos, como documentos MarkDown, imágenes, archivos de código o configuraciones.

**Pasos para subir un archivo desde la página web:**

    1. Entra en el repositorio donde quieras guardar el archivo.
    2. Pulsa _Add file_ y selecciona _Upload files_.
    3. Arrastra los archivos a la zona indicada o selecciónalos desde tu ordenador.
    4. Escribe un mensaje que describa los cambios realizados en el apartado de _Commit changes_.
    5. Confirma la operación pulsando _Commit changes_.

Los archivos quedarán almacenados en el repositorio y podrás consultarlos desde cualquier dispositivo con acceso a Internet.

#### 3. **Realizar un commit**
[Volver al índice](#indice)

Un _commit_ es un registro de los cambios realizados en un repositorio. Permite identificar qué modificaciones se han guardado y consultar el historial del proyecto.

**Pasos para realizar un commit desde la página web:**

    1. Abre un repositorio de _GitHub_.
    2. Crea un archivo nuevo o selecciona uno existente para editarlo.
    3. Realiza los cambios que necesites.
    4. Pulsa _Commit changes_.
    5. Escribe un mensaje breve que explique las modificaciones realizadas.
    6. Confirma el _commit_ y consulta el historial para comprobar que se ha guardado.
  
Es recomendable utilizar mensajes descriptivos, como **"Añadir introducción al proyecto"** o **"Corregir errores en el documento"**, para facilitar la comprensión de los cambios.

![commit](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcS7INJyk04BBR0HOSNyRhd1KwJ4rrQDmUO6TBkmtCSINw&s=10)

#### 4. **Crear y utilizar ramas**
[Volver al índice](#indice)

Una _rama_ es una línea de trabajo independiente que permite modificar un proyecto sin alterar directamente la rama principal. Es especialmente útil cuando varias personas trabajan en el mismo repositorio o cuando se quiere probar una nueva función.

**Pasos para crear una rama:**

    1. Entra en el repositorio.
    2. Haz clic en el _selector de ramas_, que normalmente muestra el nombre main.
    3. Escribe el nombre de la _nueva rama_, por ejemplo, mejoras-documentacion.
    4. Selecciona la opción para crear una _rama_ nueva a partir de la actual.
    5. Realiza los cambios necesarios en esa _rama_ y guarda las modificaciones mediante _commits_.

De esta forma, podrás trabajar de manera independiente y revisar los cambios antes de incorporarlos a la rama principal.

#### 5. **Crear una Pull Request**
[Volver al índice](#indice)

Una _pull request (PR)_ es una solicitud para revisar e integrar los cambios realizados en una rama dentro de otra. Facilita la colaboración, ya que permite comentar las modificaciones y detectar posibles errores antes de incorporarlas al proyecto.

**Pasos para crear una pull request:**

    1. Crea una _rama_ y realiza los cambios que quieras proponer.
    2. Guarda los cambios mediante uno o varios _commits_.
    3. Abre el repositorio y selecciona _Pull requests_.
    4. Pulsa _New pull request_.
    5. Selecciona la _rama de origen_, que contiene tus cambios, y la _rama de destino_, donde quieres incorporarlos.
    6. Pulsa _Create pull request_.
    7. Añade un título y una descripción que expliquen las modificaciones.
    8. Envía la solicitud y espera a que se revisen los cambios.
    9. Si tienes los permisos necesarios y no existen impedimentos, podrás pulsar _Merge pull request_ para integrar los cambios.

Las _pull requests_ permiten revisar el código, debatir propuestas y colaborar de forma organizada.

![PullRequest](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRZCzcj4nMesN0IMEVa6pawxQpD8zfIhfbAYRPcKv-Ybw&s=10)

#### 6. **Gestionar incidencias con GitHub Issues**
[Volver al índice](#indice)

_GitHub Issues_ permite registrar errores, proponer mejoras y organizar tareas relacionadas con un proyecto. Cada incidencia puede incluir una descripción, comentarios, etiquetas y una persona responsable.

**Pasos para crear una incidencia:**

    1. Accede a un repositorio que tenga habilitada la función _Issues_.
    2. Abre la pestaña _Issues_.
    3. Pulsa _New issue_.
    4. Escribe un título descriptivo y explica el problema o la tarea.
    5. Si están disponibles, añade etiquetas, asigna responsables y establece otros detalles.
    6. Pulsa _Submit new issue_ para crear la incidencia.
  
Esta función ayuda a organizar el trabajo pendiente, realizar un seguimiento de los errores y coordinar las tareas de los colaboradores.

![GitHubIssues](https://www.w3.org/International/i18n-activity/guidelines/images/issue-list.png)

#### 7. **Publicar una página web con GitHub Pages**
[Volver al índice](#indice)

_GitHub Pages_ permite publicar sitios web estáticos directamente desde un repositorio. Puede utilizarse para crear un portafolio personal, una página de documentación o la web de un proyecto.

Pasos para publicar una página:

    1. Crea un repositorio y añade los archivos de la web, como **index.html**, **CSS** e **imágenes**.
    2. Entra en la sección _Settings_ del repositorio.
    3. Busca el apartado _Pages_, normalmente dentro de la configuración de compilación y despliegue.
    4. En _Build and deployment_, selecciona la fuente de publicación disponible, por ejemplo, _Deploy from a branch_.
    5. Elige la _rama_ y la carpeta desde las que se publicarán los archivos.
    6. Guarda la configuración.
    7. Espera a que finalice el proceso de publicación y consulta la dirección web que _GitHub Pages_ proporciona.

La disponibilidad de determinadas opciones puede depender de la configuración del repositorio y del plan de GitHub. _GitHub Pages_ está pensado principalmente para sitios estáticos y no ejecuta directamente aplicaciones de servidor tradicionales.

![GitHubPages](https://digitalhumanities.hkust.edu.hk/wp-content/uploads/2023/10/github-page-setting-1.png)

### **_¿Cómo configurar y utilizar GitHub Actions?_** [Volver al índice](#indice)
Una vez explicados los conceptos clave de _GitHub Actions_ y algunas de las _funciones básicas de GitHub_, se presentan los pasos necesarios para configurar y ejecutar un _flujo de trabajo_.

#### 1. **Acceder a la sección de Acciones**
   * Entra a tu repositorio de **GitHub**
   * Haz clic en la pestaña de _Actions_ en el menú superior
   * GitHub puede mostrar sugerencias de plantillas de flujos de trabajo (_workflows_) en función del tipo de proyecto y de los lenguajes utilizados.
   * Elige una plantilla que se adapte a tus necesidades o crea un flujo de trabajo desde cero si ninguna de las opciones disponibles resulta adecuada.

#### 2. **Elegir o crear un flujo de trabajo (_Workflow_)**
   * **Usar una plantilla**: Selecciona una de las plantillas sugeridas (Node.js, Docker...) y haz clic en **Configure** o Configurar para adaptarla a las necesidades de tu proyecto.
   * **Crear un archivo manual:** Si prefieres crearlo desde cero o el directorio no existe:
     *   Ve a la pestaña principal del repositorio y haz clic en **Add file** y **Create new file**
     *   Nómbralo con la ruta y extensión _YAML_: **_.github/workflows/nombre-archivo.yml_**

       > Esta carpeta es importante, ya que GitHub Actions busca en ella los archivos que definen los flujos de trabajo del repositorio.

#### 3. **Definir la estructura YAML del flujo**
   
   El archivo YAML contiene las instrucciones que indican cuándo y cómo se ejecutará el flujo de trabajo. Sus elementos principales son:
   * **name:** Establece el nombre visible de tu flujo de trabajo.
   * **on:** define los eventos que activarán su ejecución, como un _push_ o _pull_request_.
   * **jobs**: Define los trabajos que componen el flujo de trabajo (workflow). Cada trabajo se ejecuta en un entorno de ejecución (runner), que puede utilizar Linux, Windows o macOS. A su vez, cada trabajo está formado por una serie de pasos (steps) que se ejecutan de forma secuencial y que pueden consistir en comandos de consola o en el uso de acciones (actions) ya creadas por GitHub o por otros desarrolladores.
   * **steps:** especifica los pasos de cada trabajo, que pueden ejecutar comandos de consola o utilizar acciones previamente creadas por GitHub o por otros desarrolladores.

**Ejemplo práctico de un workflow**

El siguiente ejemplo muestra un flujo de trabajo sencillo de GitHub Actions. Se ejecuta cuando se suben cambios a la _rama main_. Primero obtiene el código del repositorio y después muestra un mensaje.

```yaml
name: Mi primer workflow

on:
  push:
    branches: [main]

jobs:
  comprobar:
    runs-on: ubuntu-latest

    steps:
      - name: Obtener el código
        uses: actions/checkout@v4

      - name: Mostrar un mensaje
        run: echo "GitHub Actions funciona correctamente"

```

**¿Qué significa cada parte?**

**name:** establece el nombre del flujo de trabajo.
**on:** indica el evento que inicia la ejecución.
**push:** hace que el flujo se active cuando se suben cambios.
**branches:** _[main]:_ limita la ejecución a los cambios subidos a la rama main.
**jobs:** define los trabajos que se van a realizar.
**runs-on:** ubuntu-latest: indica que el trabajo se ejecutará en un entorno Linux proporcionado por GitHub.
**steps:** contiene los pasos que se ejecutarán de forma secuencial.
**uses:** actions/checkout@v4: utiliza una acción que obtiene el código del repositorio.
**run:** ejecuta un comando de consola; en este caso, muestra un mensaje.

Este archivo debe guardarse dentro de la ruta _.github/workflows/_, por ejemplo, como _mi-primer-workflow.yml_. Una vez guardado en el repositorio, _GitHub Actions_ podrá ejecutarlo cuando se produzca el evento configurado.

![workflow](https://user-images.githubusercontent.com/12570515/262074692-01e51004-343b-43dc-9f54-4662a69d7384.png)

#### 4. **Guardar y ejecutar**
[Volver al índice](#indice)

   * Una vez terminado el archivo, pulsa **Commit changes...** para guardar los cambios en el repositorio.
   * Si el archivo se incorpora a una rama y se produce uno de los eventos definidos en el YAML, _GitHub Actions_ activará el flujo de forma automática según el evento configurado (por ejemplo, al hacer un _push_).
   * Puedes volver a la pestaña **Actions** para monitorizar en tiempo real el progreso de cada paso y ver los registros (_logs_) de salida.
  
#### 5. **Añadir acciones externas o personalizadas**
[Volver al índice](#indice)

  * **Buscar una acción:** accede a GitHub Marketplace para encontrar acciones creadas por GitHub, empresas u otros desarrolladores que permitan realizar tareas específicas dentro de un flujo de trabajo.
  * **Integrar la acción:** añade la instrucción _uses: nombre-del-proyecto/nombre-de-la-acción@versión_ dentro de uno de los pasos (_steps_) del archivo _YAML_. Por ejemplo, _uses: actions/checkout@v4_ permite obtener el código del repositorio para que los siguientes pasos puedan trabajar con él.
  * **Revisar su fiabilidad:** antes de utilizar una acción externa, es recomendable comprobar quién la mantiene, su documentación, su actividad y los permisos que necesita. También conviene seleccionar una versión adecuada y mantenerla actualizada para reducir posibles riesgos de seguridad.

        _actions/checkout@v4_ es un ejemplo de acción que obtiene el código del repositorio, pero no todas las acciones del Marketplace hacen eso. Cada una tiene una finalidad diferente.

En definitiva, GitHub Actions permite **automatizar tareas** como ejecutar pruebas, comprobar la calidad del código, generar compilaciones o desplegar aplicaciones, reduciendo la intervención manual y facilitando la integración continua y la entrega continua (CI/CD).

![Accionesexternasopersonalizadas](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcSunf3zyCBuKo4a7rF0FAHh-5lDEZMyyIgzKT7XMDNMzQ&s=10)

## **Conclusiones**
[Volver al índice](#indice)

A lo largo de este informe hemos podido conocer qué es GitHub, cuáles son sus principales usos y cómo esta plataforma facilita el desarrollo y la organización de proyectos. Hemos visto que no se trata únicamente de un lugar donde almacenar archivos en la nube, sino de una herramienta que permite controlar las versiones de un proyecto, colaborar con otras personas y mantener un seguimiento de los cambios realizados.

Además, hemos aprendido cómo funcionan los repositorios, cómo subir archivos y registrar modificaciones mediante commits, así como la utilidad de las ramas (branches) para trabajar de forma independiente sin modificar directamente el proyecto principal. También hemos conocido las pull requests, que permiten proponer y revisar cambios antes de integrarlos, y GitHub Issues, que facilita la organización de tareas, la comunicación entre colaboradores y la detección de errores.

Por otro lado, hemos profundizado en GitHub Actions, una herramienta que permite automatizar tareas como ejecutar pruebas, comprobar el código o desplegar aplicaciones mediante flujos de trabajo configurables. Asimismo, hemos visto cómo GitHub Pages permite publicar páginas web directamente desde un repositorio, lo que resulta útil para crear portafolios personales o documentar proyectos.

En conclusión, GitHub es una plataforma muy completa que ofrece numerosas herramientas para mejorar la organización, la colaboración y la eficiencia en el desarrollo de proyectos. Conocer sus funciones resulta especialmente útil en el ámbito educativo y profesional, ya que permite adquirir hábitos de trabajo ordenados, aprender a colaborar en equipo y familiarizarse con herramientas ampliamente utilizadas en el mundo de la programación. Por todo ello, considero que aprender a utilizar GitHub es una habilidad importante para cualquier persona que quiera iniciarse en el desarrollo de software o mejorar sus conocimientos tecnológicos.

## **Bibliografía**
[Volver al índice](#indice)

* [GitHub Docs: ¿Qué es GitHub?](https://docs.github.com/es/get-started/start-your-journey/what-is-github)
* [GitHub: Actions](https://github.com/features/actions)
* [GitHub Docs: GitHub Actions](https://docs.github.com/actions)
* [GitHub: Issues](https://github.com/features/issues)
* [GitHub Docs: Creación de un sitio de páginas de GitHub](https://docs.github.com/articles/creating-project-pages-manually)
* [GitHub Docs: Descripción de Acciones de GitHub](https://docs.github.com/es/actions/get-started/understand-github-actions)
* [GitHub Docs: Inicio Rápido](https://docs.github.com/es/actions/get-started/quickstart)

