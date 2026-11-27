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
• **Server:** representa la instancia principal de Tomcat.
• **Service:** agrupa los conectores y el motor que procesa las peticiones.
• **Connector:** configura los puertos y protocolos, como HTTP (8080).
• **Engine:** gestiona el procesamiento de las peticiones.
• **Host:** permite configurar los hosts virtuales.
• **Context:** define las aplicaciones web desplegadas.

**Ubicación:** `/etc/tomcat10/server.xml`

### 2. **web.xml**

**Configuración de aplicaciones web**
Es un archivo que define la configuración general de las aplicaciones web. Permite establecer cómo
se comportan las aplicaciones desplegadas en _Tomcat_.

Elementos que se pueden configurar:
• **servlet:** define los servlets de una aplicación.
• **servlet-mapping:** relaciona los servlets con las direcciones URL.
• **welcome-file-list:** establece los archivos que se muestran al acceder a una
aplicación.
• **session-config:** configura las sesiones de usuario.
• **error-page:** define las páginas que se muestran cuando se producen errores.
• **filter:** permite configurar filtros para las peticiones.

**Ubicación:** `/etc/tomcat10/web.xml`

Este archivo proporciona valores predeterminados para las aplicaciones web, aunque cada
aplicación puede tener su propio **WEB-INF/web.xml**.

