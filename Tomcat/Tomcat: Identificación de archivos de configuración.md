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

## **Comprobación práctica en Ubuntu**

Para localizar los archivos, se pueden ejecutar estos comandos:

```bash
ls -l /etc/tomcat10/server.xml
ls -l /etc/tomcat10/web.xml
ls -l /etc/tomcat10/tomcat-users.xml
ls -l /etc/tomcat10/context.xml
```

Para consultar el contenido de los archivos de configuración de Tomcat, se puede utilizar el siguiente comando, que permite visualizar los archivos ubicados en el directorio /etc/tomcat10:

```bash
ls -l /etc/tomcat10`
```

<img width="924" height="508" alt="CD Y LS -L" src="https://github.com/user-attachments/assets/c80f09ab-6cb8-4466-b17c-02e9da4e4d41" />

También podemos consultar los archivos con _cat_, sin modificarlos:

```bash
sudo cat /etc/tomcat10/server.xml
sudo cat /etc/tomcat10/web.xml
sudo cat /etc/tomcat10/tomcat-users.xml
sudo cat /etc/tomcat10/context.xml
```

En lugar de consultar cada archivo de configuración de Tomcat mediante un comando independiente, se ha utilizado el siguiente comando para visualizar conjuntamente el contenido de los archivos del directorio /etc/tomcat10:

```bash
sudo find /etc/tomcat10/ -name "server-xml" -o -name "web.xml" -o -name "tomcat-users.xml" -o -name "context.xml"
```

<img width="1346" height="266" alt="sudofindnano" src="https://github.com/user-attachments/assets/9391e274-7e2f-45e7-8550-41d1570979d9" />

**Localización y consulta de los archivos de configuración**

Para localizar y consultar los cuatro archivos principales de configuración de Tomcat, se ha utilizado el editor de texto nano mediante el comando sudo, que permite acceder a los archivos con permisos de administrador.

Los comandos utilizados han sido los siguientes:

```bash
sudo nano /etc/tomcat10/server.xml
```

<img width="1346" height="266" alt="sudofindnano" src="https://github.com/user-attachments/assets/e87af785-5e79-4410-b593-eb1cd2e09dac" />

<img width="1075" height="727" alt="server" src="https://github.com/user-attachments/assets/b8785c9e-1b36-4711-8dba-5ddbd35eefdf" />

<img width="1365" height="726" alt="servernano" src="https://github.com/user-attachments/assets/8f90a421-2f20-4a8b-9ba5-e39925e7b206" />

```bash
sudo nano /etc/tomcat10/web.xml
```

<img width="808" height="40" alt="SudoNanoWeb" src="https://github.com/user-attachments/assets/60c4dc32-bee5-4aca-8bf6-52c39da77259" />

<img width="978" height="731" alt="Web" src="https://github.com/user-attachments/assets/92780e1d-b133-4117-ae16-69e26b27d395" />

<img width="955" height="727" alt="Web2" src="https://github.com/user-attachments/assets/0940de20-6edd-4d52-ba3c-ec4e2c8213be" />

```bash
sudo nano /etc/tomcat10/tomcat-users.xml
```

<img width="939" height="66" alt="SudoNanoTomcatUsers" src="https://github.com/user-attachments/assets/69c2fa10-a1be-41ea-bfaa-3778975c57e0" />

<img width="920" height="727" alt="TomcatUsers" src="https://github.com/user-attachments/assets/a118a63b-a14f-46cc-bee4-c8b5e01f019b" />

<img width="925" height="724" alt="TomcatUsers2" src="https://github.com/user-attachments/assets/be7633cd-fc99-412f-8e6c-d3c02daa97ab" />

```bash
sudo nano /etc/tomcat10/context.xml
```

<img width="913" height="44" alt="SudoNanoContext" src="https://github.com/user-attachments/assets/e6bbc012-d48f-44aa-89c0-cc952ba511b6" />

<img width="973" height="718" alt="Context" src="https://github.com/user-attachments/assets/2892de38-8446-43aa-bb44-cccd80a63460" />

A través de estos comandos se ha podido consultar el contenido de cada archivo e identificar su función y los diferentes elementos que se pueden configurar en ellos.

En esta práctica he aprendido a localizar e identificar los principales archivos de configuración de Apache Tomcat. He conocido la función de server.xml, web.xml, tomcat-users.xml y context.xml, así como los diferentes parámetros que permiten configurar el servidor, las aplicaciones web, los usuarios y los recursos. Además, he realizado un mapa visual para comprender mejor cómo se relacionan estos archivos dentro del funcionamiento de Tomcat.
