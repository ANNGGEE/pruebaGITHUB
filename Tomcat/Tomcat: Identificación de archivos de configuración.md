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

1. `/etc/tomcat10/server.xml`
