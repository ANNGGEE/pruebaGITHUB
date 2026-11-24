# Implementación del protocolo HTTPS en un servidor web Apache2 sobre Ubuntu

## 1. Introducción y objetivos

El objetivo de esta práctica es investigar e implementar el protocolo HTTPS en un servidor web Apache2 ejecutado sobre un sistema operativo Ubuntu.

HTTPS permite establecer comunicaciones seguras entre un navegador y un servidor web mediante el uso de certificados digitales y protocolos de cifrado SSL/TLS.

Durante esta práctica se instalará y configurará Apache2, se habilitarán los módulos necesarios para trabajar con conexiones seguras y se generará un certificado SSL/TLS autofirmado.

Finalmente, se configurará un VirtualHost para permitir conexiones HTTPS mediante el puerto 443 y se realizarán diferentes pruebas para comprobar que el servidor funciona correctamente.

### Objetivos específicos

- Comprender el funcionamiento del protocolo HTTPS.
- Conocer la importancia de los certificados SSL/TLS.
- Diferenciar entre certificados autofirmados y certificados emitidos por autoridades certificadoras.
- Instalar y configurar Apache2 en Ubuntu.
- Habilitar los módulos necesarios para utilizar HTTPS.
- Configurar un certificado SSL/TLS.
- Configurar un VirtualHost para el puerto 443.
- Comprobar el funcionamiento de HTTPS mediante un navegador y herramientas como `curl`.

## 2. Investigación teórica

### 2.1. ¿Qué es HTTPS y cómo funciona?

HTTPS (Hypertext Transfer Protocol Secure) es la versión segura del protocolo HTTP, utilizado para la comunicación entre navegadores web y servidores.

Su principal característica es que utiliza TLS (Transport Layer Security) para cifrar las comunicaciones y proteger la información intercambiada entre ambas partes.

HTTPS proporciona tres propiedades fundamentales:

- **Confidencialidad:** la información transmitida está cifrada y no puede ser interpretada fácilmente por terceros.
- **Integridad:** permite detectar modificaciones no autorizadas de los datos durante la transmisión.
- **Autenticación:** permite comprobar la identidad del servidor mediante certificados digitales.

Cuando un usuario accede a una página mediante HTTPS, se produce un proceso denominado *handshake* o negociación TLS.

Durante este proceso:

1. El navegador solicita establecer una conexión segura con el servidor.
2. El servidor presenta su certificado digital.
3. El navegador comprueba la validez del certificado y la identidad del servidor, cuando dispone de una autoridad certificadora de confianza.
4. Ambas partes negocian los parámetros criptográficos y establecen las claves de sesión.
5. A partir de ese momento, la comunicación se realiza mediante cifrado.

HTTPS utiliza normalmente el puerto TCP **443**, mientras que HTTP utiliza el puerto TCP **80**.

### 2.2. Importancia de HTTPS en la seguridad web

La utilización de HTTPS es fundamental para proteger las comunicaciones en Internet.

Entre sus principales ventajas destacan:

- Protege contraseñas y datos personales.
- Evita que terceros puedan leer fácilmente la información transmitida.
- Reduce el riesgo de manipulación de los datos durante la comunicación.
- Permite verificar la identidad del servidor mediante certificados.
- Aumenta la confianza de los usuarios en los sitios web.
- Es especialmente importante en páginas que gestionan compras, registros o información sensible.

Por estos motivos, HTTPS se considera actualmente un estándar básico de seguridad para los servidores web.

### 2.3. Tipos de certificados SSL/TLS

Existen diferentes tipos de certificados digitales. En esta práctica se estudian principalmente dos:

#### Certificados autofirmados

Son certificados generados y firmados por el propio administrador del servidor, sin la intervención de una autoridad certificadora externa.

**Ventajas:**

- Son gratuitos.
- Se pueden generar fácilmente.
- Son útiles para laboratorios, pruebas y entornos de desarrollo.

**Inconvenientes:**

- Los navegadores no confían automáticamente en ellos.
- Muestran advertencias de seguridad.
- No proporcionan una validación independiente de la identidad del servidor.

#### Certificados emitidos por una autoridad certificadora (CA)

Son certificados firmados por una entidad certificadora reconocida por los navegadores y sistemas operativos.

Un ejemplo es Let's Encrypt, que proporciona certificados gratuitos mediante herramientas como Certbot.

**Ventajas:**

- Los navegadores reconocen su cadena de confianza.
- Permiten ofrecer HTTPS sin advertencias de certificados autofirmados, siempre que la configuración sea correcta.
- Son adecuados para servidores públicos.

**Inconvenientes:**

- Normalmente requieren disponer de un dominio.
- Es necesario demostrar el control del dominio.
- Deben renovarse periódicamente.

### 2.4. Módulos necesarios de Apache2

Apache2 dispone de diferentes módulos que permiten ampliar sus funcionalidades.

Para implementar HTTPS en Ubuntu se utilizarán principalmente los siguientes:

| Módulo | Función |
|---|---|
| `mod_ssl` | Permite establecer conexiones HTTPS mediante SSL/TLS. |
| `mod_headers` | Permite modificar y añadir cabeceras HTTP. |
| `mod_rewrite` | Permite realizar redirecciones y reescrituras de direcciones URL. |

En esta práctica se habilitarán los módulos SSL y headers. La redirección HTTP a HTTPS se realizará mediante una directiva `Redirect`, por lo que no será necesario habilitar `mod_rewrite`.

## 3. Implementación técnica

### 3.1. Instalación de Apache2

En primer lugar, se actualizan los repositorios de Ubuntu:

```bash
sudo apt update
```
<img width="1365" height="726" alt="imagen" src="https://github.com/user-attachments/assets/c05e4e42-20cb-45ec-b708-c8d8a19f615c" />

A continuación, se instala Apache2:

```bash
sudo apt install apache2 -y
```
<img width="1365" height="726" alt="imagen" src="https://github.com/user-attachments/assets/d5bd8106-042e-47c2-a609-aa06702bb1ce" />

Para comprobar que el servicio está funcionando correctamente:

```bash
sudo systemctl status apache2
```
<img width="1365" height="726" alt="imagen" src="https://github.com/user-attachments/assets/85794137-7036-4dbb-9b63-b3fa9d4b40fe" />

El resultado esperado es que el servicio aparezca como `active (running)`.

### 3.2. Habilitación de los módulos SSL y headers

Se habilita el módulo SSL:

```bash
sudo a2enmod ssl
```
<img width="1238" height="398" alt="imagen" src="https://github.com/user-attachments/assets/d3fd3f7b-e75c-4349-9aba-3c32ddae3a9e" />

También se habilita el módulo headers:

```bash
sudo a2enmod headers
```

<img width="1238" height="398" alt="imagen" src="https://github.com/user-attachments/assets/ef9cbdab-fd6f-463f-880b-858a10476185" />

Una vez habilitados, se comprueba la configuración de Apache:

```bash
sudo apache2ctl configtest
```
<img width="1238" height="398" alt="imagen" src="https://github.com/user-attachments/assets/f7f793a5-2f0e-4150-96a3-bded004d528e" />

El resultado esperado es:

```text
Syntax OK
```

### 3.3. Generación de un certificado autofirmado

Para esta práctica se utilizará un certificado autofirmado.

Primero se genera la clave privada y el certificado digital mediante OpenSSL:

```bash
sudo openssl req -x509 -nodes -days 365 -newkey rsa:2048 \
-keyout /etc/ssl/private/apache-selfsigned.key \
-out /etc/ssl/certs/apache-selfsigned.crt \
-subj "/CN=localhost" \
-addext "subjectAltName=DNS:localhost,IP:127.0.0.1"
```
<img width="1365" height="728" alt="imagen" src="https://github.com/user-attachments/assets/d399e08a-11f0-4a07-8b4f-d6604681c5df" />

Este comando genera:

- Una clave privada RSA de 2048 bits.
- Un certificado autofirmado con una duración de 365 días.
- Un nombre común (CN) correspondiente a `localhost`.
- Una extensión SAN que identifica `localhost` y la dirección `127.0.0.1`.

Se establecen permisos adecuados para proteger la clave privada:

```bash
sudo chmod 600 /etc/ssl/private/apache-selfsigned.key
```

<img width="920" height="180" alt="imagen" src="https://github.com/user-attachments/assets/c17e0ad3-58a9-4cf8-9f00-31f7db98d775" />

Para comprobar que los archivos se han creado correctamente:

```bash
sudo ls -l /etc/ssl/private/apache-selfsigned.key
sudo ls -l /etc/ssl/certs/apache-selfsigned.crt
```
<img width="920" height="180" alt="imagen" src="https://github.com/user-attachments/assets/7167c0a7-9920-4183-ab6e-75b2d52a3ecd" />

### 3.4. Configuración del VirtualHost HTTPS

Se creará un archivo de configuración específico para nuestro servidor:

```bash
sudo nano /etc/apache2/sites-available/https-local.conf
```
<img width="943" height="61" alt="imagen" src="https://github.com/user-attachments/assets/48dc3e46-c4ad-4961-b397-d57ff57a8f93" />

Dentro del archivo se introducirá la siguiente configuración:

```apache
<VirtualHost *:80>
    ServerName localhost
    Redirect permanent / https://localhost/
</VirtualHost>

<VirtualHost *:443>
    ServerName localhost
    DocumentRoot /var/www/html

    SSLEngine on

    SSLCertificateFile /etc/ssl/certs/apache-selfsigned.crt
    SSLCertificateKeyFile /etc/ssl/private/apache-selfsigned.key

    <Directory /var/www/html>
        Options Indexes FollowSymLinks
        AllowOverride None
        Require all granted
    </Directory>

    Header always set X-Content-Type-Options "nosniff"

    ErrorLog ${APACHE_LOG_DIR}/https-local-error.log
    CustomLog ${APACHE_LOG_DIR}/https-local-access.log combined
</VirtualHost>
```

<img width="1365" height="728" alt="imagen" src="https://github.com/user-attachments/assets/4985ccac-2fff-4d23-957f-5d87c6bbcab9" />

La configuración anterior realiza las siguientes funciones:

- El primer VirtualHost escucha en el puerto 80 y redirige las peticiones HTTP a HTTPS.
- El segundo VirtualHost escucha en el puerto 443.
- `ServerName` establece el nombre del servidor.
- `DocumentRoot` indica el directorio donde se encuentran los archivos de la página web.
- `SSLEngine on` activa el funcionamiento de SSL/TLS.
- `SSLCertificateFile` indica la ubicación del certificado.
- `SSLCertificateKeyFile` indica la ubicación de la clave privada.
- `Header` permite añadir cabeceras de seguridad a las respuestas HTTP.
- `ErrorLog` y `CustomLog` permiten registrar errores y accesos.

Se guarda el archivo y se cierra el editor.

### 3.5. Habilitación del sitio web

Se habilita el nuevo sitio mediante el siguiente comando:

```bash
sudo a2ensite https-local.conf
```
<img width="956" height="403" alt="imagen" src="https://github.com/user-attachments/assets/ef5ef8f2-7a2c-444b-89b4-00d06ec3856b" />

A continuación, se comprueba que no existen errores de configuración:

```bash
sudo apache2ctl configtest
```
<img width="956" height="403" alt="imagen" src="https://github.com/user-attachments/assets/2c664b2f-3e01-4e64-a050-623f2264e991" />

Si aparece `Syntax OK`, la configuración es correcta.

### 3.6. Reinicio del servidor Apache2

Se recarga la configuración del servidor:

```bash
sudo systemctl reload apache2
```
<img width="956" height="403" alt="imagen" src="https://github.com/user-attachments/assets/81c53f33-3fd3-47bc-a812-f55d1eebc2c6" />

Se comprueba nuevamente su estado:

```bash
sudo systemctl status apache2
```
<img width="956" height="403" alt="imagen" src="https://github.com/user-attachments/assets/50c05386-f606-4a1e-bcc9-0acf5f64582a" />

El servicio debe continuar apareciendo como `active (running)`.

## 4. Verificación del funcionamiento de HTTPS

Una vez configurado el servidor, se realizarán varias pruebas para comprobar que HTTPS funciona correctamente.

### 4.1. Comprobación mediante curl

Se ejecuta el siguiente comando:

```bash
curl -k -I https://localhost
```

<img width="593" height="294" alt="imagen" src="https://github.com/user-attachments/assets/d5a0cb40-d544-45b4-9ce5-dfdf2762606b" />

El parámetro `-k` permite realizar la conexión aunque el certificado sea autofirmado y no esté reconocido por el sistema.

Si la configuración es correcta, se recibirá una respuesta HTTP, normalmente:

```text
HTTP/1.1 200 OK
```

Esto demuestra que Apache responde correctamente mediante HTTPS.

Es importante tener en cuenta que utilizar `-k` omite la validación de confianza del certificado, por lo que esta prueba comprueba la conectividad y la respuesta del servidor, pero no demuestra que el certificado sea de confianza.

### 4.2. Comprobación de la redirección HTTP a HTTPS

Se ejecuta:

```bash
curl -I http://localhost
```
<img width="573" height="194" alt="imagen" src="https://github.com/user-attachments/assets/4b1462a1-9ced-4f75-8d39-c1e84ce06081" />

El resultado esperado es una respuesta de redirección:

```text
HTTP/1.1 301 Moved Permanently
Location: https://localhost/
```

Esto demuestra que las peticiones realizadas mediante HTTP se redirigen automáticamente al protocolo seguro HTTPS.

### 4.3. Comprobación del certificado

También se puede consultar la información del certificado mediante OpenSSL:

```bash
openssl s_client -connect localhost:443 -servername localhost
```

<img width="1365" height="732" alt="imagen" src="https://github.com/user-attachments/assets/5f55a6c9-ac2b-415f-aab2-a22912f7e3ab" />

<img width="935" height="723" alt="imagen" src="https://github.com/user-attachments/assets/d7a00c27-53e4-4ace-8c85-1d1413b449b2" />

<img width="1365" height="728" alt="imagen" src="https://github.com/user-attachments/assets/0f02bb24-bdca-45ea-b3b1-e26ac29e051c" />

<img width="932" height="371" alt="imagen" src="https://github.com/user-attachments/assets/96352d9b-8f3c-4b39-be27-6d4a63cb430b" />

Este comando permite comprobar que el servidor presenta un certificado durante el establecimiento de la conexión TLS.

Al tratarse de un certificado autofirmado, es normal que OpenSSL indique que no puede verificar la cadena de confianza.

### 4.4. Comprobación mediante navegador

Finalmente, se abre un navegador web y se introduce la siguiente dirección:

```text
https://localhost
```

<img width="1365" height="734" alt="imagen" src="https://github.com/user-attachments/assets/39823213-6ebe-41c8-beee-0582884032c6" />

La página debería cargarse correctamente.

Al acceder al servidor mediante HTTPS, Firefox mostró una advertencia de seguridad debido a que el certificado utilizado era autofirmado y no estaba emitido por una autoridad certificadora reconocida.

Tras comprobar que se trataba del certificado generado durante la práctica, se permitió el acceso para verificar el funcionamiento del servidor.

Una vez superada la advertencia, se comprobó que la página predeterminada de Apache2 se cargaba correctamente utilizando una conexión HTTPS.

Esta advertencia es un comportamiento esperado cuando se utilizan certificados autofirmados, ya que los navegadores no confían automáticamente en ellos.

<img width="1365" height="729" alt="imagen" src="https://github.com/user-attachments/assets/7ae86ad4-3598-4dd0-b1a9-586f4b0addea" />

COMPROBACIÓN MEDIANTE TERMINAL (BORRAR SI NO ES NECESARIO)

<img width="702" height="456" alt="imagen" src="https://github.com/user-attachments/assets/11685d8e-1a84-4fa9-8d49-62e1bd695222" />

## 5. Capturas de pantalla y evidencias

Para demostrar la correcta implementación se incluirán las siguientes capturas:

- Instalación de Apache2 y comprobación de su estado.
- Habilitación de los módulos SSL y headers.
- Generación del certificado autofirmado.
- Archivo de configuración del VirtualHost.
- Resultado de `apache2ctl configtest`.
- Resultado de `curl -k -I https://localhost`.
- Resultado de la redirección HTTP a HTTPS.
- Acceso a `https://localhost` desde el navegador.

Estas evidencias permitirán demostrar que el servidor web está correctamente configurado para utilizar conexiones HTTPS.

## 6. Conclusiones

Mediante esta práctica se ha conseguido implementar el protocolo HTTPS en un servidor web Apache2 ejecutado sobre Ubuntu.

Durante el proceso se ha instalado Apache2, se han habilitado los módulos necesarios para trabajar con SSL/TLS y se ha generado un certificado autofirmado utilizando OpenSSL.

También se ha configurado un VirtualHost para permitir conexiones seguras mediante el puerto 443 y se ha establecido una redirección automática desde HTTP hacia HTTPS.

Las pruebas realizadas han resultado satisfactorias. Se ha comprobado mediante curl que el servidor responde con un código HTTP 200 OK al acceder mediante HTTPS. Asimismo, se ha verificado que las peticiones realizadas mediante HTTP reciben una respuesta 301 Moved Permanently y son redirigidas al protocolo HTTPS.

Finalmente, se ha comprobado mediante Firefox que la página predeterminada de Apache2 se carga correctamente utilizando una conexión segura.

Durante la comprobación mediante el navegador apareció una advertencia de seguridad debido a que el certificado utilizado era autofirmado. Esto ha permitido comprender la diferencia entre los certificados autofirmados y los emitidos por autoridades certificadoras de confianza.

En conclusión, esta práctica ha permitido comprender la importancia de HTTPS en la seguridad web y conocer los pasos necesarios para configurar un servidor Apache2 con SSL/TLS. Además, se ha comprobado que HTTPS permite proteger la confidencialidad e integridad de la información transmitida entre clientes y servidores.
