# Tomcat: Investigación y descripción

**Apache Tomcat** es un servidor web y contenedor de servlets de código abierto que permite ejecutar aplicaciones escritas en lenguaje Java dentro de un entorno web. Mientras que un servidor web tradicional solo sabe entregar archivos estáticos (como páginas HTML, imágenes o hojas de estilo CSS), **Tomcat** es capaz de procesar lógica de programación compleja en tiempo real y generar contenido dinámico para cada usuario.

## **Componentes principales**
1. **Catalina**

**Catalina** es el **_contenedor de servlets de Tomcat_**. Se encarga de gestionar las aplicaciones web Java, ejecutar los servlets y controlar su ciclo de vida. También administra los contenedores Engine, Host y Context. Su configuración principal se encuentra en `conf/server.xml`

2. **Coyote**

**Coyote** es el componente encargado de la comunicación HTTP entre los usuarios y **Tomcat**. Recibe las peticiones que llegan desde los navegadores y envía las respuestas correspondientes. Gestiona los conectores y los protocolos de comunicación. Su configuración se encuentra principalmente en `conf/server.xml`.

3. **Jasper**

**Jasper** es el **motor JSP (JavaServer Pages) de Tomcat**. Su función es transformar las páginas **JSP** en código Java y compilarlas para que puedan ejecutarse como servlets. Permite generar páginas web dinámicas. Se integra dentro de **Tomcat** y utiliza las bibliotecas y herramientas incluidas en su instalación.

4. **Manager y Host Manager**

Son aplicaciones web de administración de **Tomcat**.

    Manager: permite desplegar, detener, iniciar y eliminar aplicaciones web desde un navegador.

    Host Manager: permite administrar los hosts virtuales de Tomcat.

Ambas aplicaciones se encuentran normalmente dentro del **directorio webapps**, en las carpetas **_manager_** y **_host-manager_**.


## Estructura básica de directorios

**Tomcat** organiza sus archivos en diferentes carpetas para facilitar su administración:

| Directorio | Función |
|---|---|
| `bin` | Contiene los scripts para iniciar, detener y administrar Tomcat, como `startup.sh` y `shutdown.sh`. |
| `conf` | Guarda los archivos de configuración, como `server.xml`, `web.xml` y `tomcat-users.xml`. |
| `webapps` | Contiene las aplicaciones web que Tomcat despliega y ejecuta. |
| `lib` | Almacena las bibliotecas Java necesarias para el funcionamiento de Tomcat. |
| `logs` | Guarda los registros de actividad, errores y eventos del servidor. |

En **Ubuntu**, cuando se instala **Tomcat** mediante **APT**, los directorios suelen estar separados:

* **Ejecutables:** `/usr/share/tomcat10/bin` (scripts y archivos asociados)
* **Configuración:** `/etc/tomcat10`
* **Aplicaciones:** `/var/lib/tomcat10/webapps`
* **Bibliotecas:** `/usr/share/tomcat10/lib`
* **Registros:** `/var/log/tomcat10`

  
