# Tomcat: Identificación de archivos de configuración

## **Localización de los archivos de configuración**

Si se ha instalado **_Tomcat 10_** mediante **apt** en **Ubuntu**, los archivos se encuentran normalmente en:

```bash
/etc/tomcat10/
```

Para comprobarlo:

```bash
ls -l /etc/tomcat10/
```

Para localizar los cuatro archivos concretos:

```bash
sudo find /etc/tomcat10/ -name "server.xml" -o -name "web.xml" -o -name "tomcat- users.xml" -o -name "context.xml"
```

Los archivos que deben aparecer son:

• `/etc/tomcat10/server.xml`

• `/etc/tomcat10/web.xml`

• `/etc/tomcat10/tomcat-users.xml`

• `/etc/tomcat10/context.xml`

Podemos consultar su contenido con:

```bash
sudo nano /etc/tomcat10/server.xml
```
## **Función de cada archivo y qué elementos se pueden configurar**

### 1. **server.xml**

**Configuración principal**

Es el archivo principal de configuración de _Tomcat_. Define cómo se inicia y organiza el servidor y
cómo recibe las conexiones de los usuarios.

Elementos que se pueden configurar:
* **Server:** representa la instancia principal de Tomcat.
* **Service:** agrupa los conectores y el motor que procesa las peticiones.
* **Connector:** configura los puertos y protocolos, como HTTP (8080).
* **Engine:** gestiona el procesamiento de las peticiones.
* **Host:** permite configurar los hosts virtuales.
* **Context:** define las aplicaciones web desplegadas.

**Ubicación:** `/etc/tomcat10/server.xml`

### 2. **web.xml**

**Configuración de aplicaciones web**

Es un archivo que define la configuración general de las aplicaciones web. Permite establecer cómo
se comportan las aplicaciones desplegadas en _Tomcat_.

Elementos que se pueden configurar:
* **servlet:** define los servlets de una aplicación.
* **servlet-mapping:** relaciona los servlets con las direcciones URL.
* **welcome-file-list:** establece los archivos que se muestran al acceder a una
aplicación.
* **session-config:** configura las sesiones de usuario.
* **error-page:** define las páginas que se muestran cuando se producen errores.
* **filter:** permite configurar filtros para las peticiones.

**Ubicación:** `/etc/tomcat10/web.xml`

Este archivo proporciona valores predeterminados para las aplicaciones web, aunque cada
aplicación puede tener su propio **WEB-INF/web.xml**.

### 3. **tomcat-users.xml**

**Usuarios y permisos**

Es el archivo encargado de gestionar los usuarios, las contraseñas y los roles de acceso a las
herramientas de administración de _Tomcat_.

Elementos que se pueden configurar:
* **user:** permite crear usuarios y asignarles un nombre y contraseña.
* **role:** define los permisos o roles disponibles.
* **roles:** permite asignar uno o varios roles a un usuario.
Algunos roles habituales son:
* **manager-gui:** permite acceder a la interfaz gráfica de Manager.
* **admin-gui:** permite acceder a la interfaz gráfica de Host Manager.

**Ubicación:** `/etc/tomcat10/tomcat-users.xml`

### 4. **context.xml**

**Configuración de aplicaciones**

Es un archivo que permite configurar los contextos de las aplicaciones web. Define diferentes
opciones relacionadas con su ejecución y acceso a recursos.

Elementos que se pueden configurar:
* **Context:** define el contexto de una aplicación web.
* **Environment:** permite establecer variables de entorno.
* **Resource:** configura recursos externos, como conexiones a bases de datos.
* **ResourceLink:** permite enlazar recursos compartidos.
* **WatchedResource:** indica archivos que Tomcat debe vigilar para detectar cambios.

**Ubicación:** `/etc/tomcat10/context.xml`

Este archivo contiene una configuración predeterminada que se aplica a las aplicaciones web, salvo
que una aplicación tenga configuraciones específicas que la modifiquen.

## **Mapa Visual de Dependencias**

                    APACHE TOMCAT
                          |
       +------------------+------------------+
       |                  |                  |
     server.xml          web.xml        tomcat-users.xml
         |                  |                  |
    Configuración      Configuración       Usuarios
    del servidor       de aplicaciones     y roles
         |                  |                  |
    - Puertos           - Servlets          - Manager
    - Conectores        - Filtros           - Host Manager
    - Engine            - Sesiones
    - Host              - Páginas de error
    - Contextos
                            |
                        context.xml
                            |
                  Configuración de contextos
                            |
                     - Recursos
                     - Variables
                     - Opciones

**Explicación del mapa:**
* **server.xml** configura la estructura general del servidor y los conectores que reciben las peticiones.

* **web.xml** establece las reglas y configuraciones generales de las aplicaciones web.
  
* **tomcat-users.xml** gestiona los usuarios y sus permisos para acceder a las herramientas administrativas.

* **context.xml** define opciones y recursos asociados a los contextos de las aplicaciones.
  
Los cuatro archivos tienen funciones diferentes, pero trabajan conjuntamente para permitir que _Tomcat_ funcione y administre las aplicaciones web.

El mapa representa las relaciones funcionales entre los archivos, no significa que unos archivos importen directamente a los otros.
