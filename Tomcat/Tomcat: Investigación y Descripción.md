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

## **Flujo interno de funcionamiento**

Cuando un usuario accede a una aplicación web alojada en **Tomcat**, se produce el siguiente proceso:

* **Recepción de la petición:** Coyote recibe la solicitud HTTP enviada desde el navegador, normalmente por el puerto 8080.
* **Procesamiento:** Catalina recibe la petición y la dirige al contenedor correspondiente.
* **Contenedores:** Tomcat utiliza una estructura formada por Engine, Host, Context y Wrapper para identificar qué aplicación y servlet deben atender la solicitud.
* **Ejecución:** El servlet procesa la petición y genera una respuesta. Si se utiliza una página JSP, Jasper se encarga de convertirla y compilarla cuando sea necesario.
* **Respuesta:** Tomcat devuelve el resultado al navegador mediante Coyote.

**Despliegue de aplicaciones:** Tomcat permite instalar aplicaciones web copiando sus archivos WAR o sus carpetas directamente en webapps.

El servidor detecta las aplicaciones y las prepara para su ejecución.

## **Instalación de Tomcat en Ubuntu**

Si lo instalamos desde la terminal de **Ubuntu**.
1. **Actualizar Ubuntu**

```bash
sudo apt update
sudo apt upgrade -y
```
<img width="1109" height="729" alt="sudoaptupdate" src="https://github.com/user-attachments/assets/63ab19ca-35e9-476a-80b7-1138335199d9" />

<img width="1102" height="727" alt="sudoaptupgrade" src="https://github.com/user-attachments/assets/0aa3ca1f-030b-47b0-91c2-9e912424b4eb" />

2. **Instalar Java**

Tomcat necesita Java para funcionar.

```bash
sudo apt install default-jdk -y
```

<img width="1149" height="725" alt="Default-jdk-y" src="https://github.com/user-attachments/assets/7e8554d1-2ee7-4bb8-a451-995be1774607" />

Comprobamos que está instalado:

```bash
java -version
```

<img width="925" height="137" alt="javaversion" src="https://github.com/user-attachments/assets/a6f084fb-5529-4294-8a0f-9fca5985efdb" />

3. **Instalar Tomcat**

En Ubuntu 24.04 podemos instalar Tomcat 10 con:

```bash
sudo apt install tomcat10 tomcat10-admin -y
```

<img width="1046" height="728" alt="InstallTomcat10" src="https://github.com/user-attachments/assets/13c7aaec-e97f-4109-8357-a77f4505ba0f" />

4. **Comprobar que funciona**

```bash
sudo systemctl status tomcat10
```

<img width="862" height="727" alt="StatusTomcat10" src="https://github.com/user-attachments/assets/f05f7b6b-97c5-4d72-b8dd-c1a8ffe65443" />


Debería aparecer como active (running).

Si no está iniciado, se puede arrancar con:

```bash
sudo systemctl start tomcat10
```

Para que se inicie automáticamente al encender Ubuntu:

```bash
sudo systemctl enable tomcat10
```

<img width="705" height="87" alt="EnableTomcat10" src="https://github.com/user-attachments/assets/18827b5b-9507-4f4b-9acb-16fced2ec152" />

5. **Acceder desde el navegador**

Abrimos el navegador de la máquina virtual y escribimos:

Página de Tomcat

`http://localhost:8080`

<img width="1365" height="724" alt="ItWorks" src="https://github.com/user-attachments/assets/14dedb81-4b0a-4f2b-933b-8d637ec9b3cc" />

Si aparece la página de bienvenida de Apache Tomcat, la instalación ha funcionado 

