# Iniciación a la Virtualización 
## ¿Qué es la virtualización? 
La virtualización es una tecnología que permite ejecutar varios sistemas operativos o entornos de software independientes en una misma máquina física, mediante el uso de hipervisores (como VirtualBox, VMware, Hyper-V, etc.). Cada entorno virtual se denomina máquina virtual (VM). 

**Conceptos clave:**
* **Hipervisor:** Software que gestiona las máquinas virtuales. 
* **Imagen ISO:** Archivo que contiene una copia exacta de un sistema operativo o software de instalación. 
* **Recursos virtualizados:** CPU, memoria RAM, almacenamiento y red. 

**Instalación de Ubuntu en VirtualBox**
1. Descarga la ISO de Ubuntu 24.04 LTS desde la página oficial de Ubuntu. 
2. Crea una nueva máquina virtual con las siguientes características recomendadas:  
    * Nombre: Ubuntu-DAW2DAW 
    * RAM: 4096 MB 
    * Disco duro virtual: mínimo 50 GB 
    * Tipo de red: NAT
3. Instala las Guest Additions 
4. Toma una captura de pantalla del escritorio una vez instalado. 


Lo primero es irnos a la página oficial de Ubuntu en la pestaña de Past releases y allí elegir el enlace que nos llevará a la selección de una imagen, en este caso vamos a pulsar al primer enlace “Ubuntu 24.04 LTS Noble Numbat". 

<img width="596" height="241" alt="Captura1" src="https://github.com/user-attachments/assets/5653814c-37b4-4d56-a976-8add45e77fe0" />

Una vez en esta ventana, bajaremos a lo largo de la página y buscaremos una ISO 24.4 que descargar.

<img width="718" height="331" alt="Captura2" src="https://github.com/user-attachments/assets/3fcd88da-4154-4ac7-ac81-16a906e4c33d" />

En este caso se ha elegido ubuntu 24.04.5.1-desktop-amd64.iso

<img width="455" height="33" alt="Captura3" src="https://github.com/user-attachments/assets/c3ad8cc9-dc1a-43a2-9229-4efdbcf87dc2" />

## **CREACIÓN DE LA MÁQUINA VIRTUAL:**
Se ha creado una máquina virtual con las especificaciones mentadas arriba: 
* Nombre: Ubuntu-DAW2DAW 
* RAM: 4096 MB 
* Disco duro virtual: mínimo 50 GB 
* Tipo de red: NAT

<img width="655" height="336" alt="Captura4" src="https://github.com/user-attachments/assets/c75bc5c3-6d2f-4047-8685-37d4df3b346b" />

<img width="657" height="365" alt="Captura5" src="https://github.com/user-attachments/assets/7670433d-09e5-4b55-82f1-1716ab4c146e" />

<img width="656" height="305" alt="Captura6" src="https://github.com/user-attachments/assets/387a3593-5221-4fc1-aada-2320f74a46ca" />

<img width="643" height="272" alt="Captura7" src="https://github.com/user-attachments/assets/93ec52a0-62f2-413c-bb65-2212f0814d9f" />

<img width="642" height="382" alt="Captura8" src="https://github.com/user-attachments/assets/c6bfee4b-de0f-41ff-85d0-d097c808c942" />

UNA VEZ INSTALADO: 

<img width="651" height="364" alt="Captura9" src="https://github.com/user-attachments/assets/d2970bfb-ade6-4a08-a9bf-227876c4190a" />

Una vez encendida la máquina de Ubuntu por primera vez nos aparecerá esta pestaña que nos dice “Install Ubuntu”, pulsaremos y esperaremos para más tarde reiniciar la máquina. 

Al iniciar por primera vez la máquina virtual, se muestra el instalador de Ubuntu, que se ejecuta desde la imagen ISO previamente asociada a la máquina virtual.

Este instalador permite realizar la instalación del sistema operativo en el disco duro virtual. Durante el proceso se configuran aspectos como el idioma, la distribución del teclado, la zona horaria, las particiones del disco y las credenciales del usuario.

Una vez confirmadas las opciones de instalación, el sistema copia los archivos necesarios, instala los componentes fundamentales de Ubuntu y configura el gestor de arranque para permitir que el sistema operativo pueda iniciarse desde el disco virtual.

Cuando finaliza la instalación, aparece un mensaje indicando que es necesario reiniciar la máquina. Este reinicio debe iniciarse manualmente mediante la opción "Reiniciar ahora". Si es necesario, se debe retirar o desconectar la imagen ISO para evitar que la máquina vuelva a iniciar el instalador.

Finalmente, la máquina virtual arranca desde el disco duro virtual, cargando la instalación de Ubuntu realizada y mostrando la pantalla de inicio de sesión.

<img width="649" height="351" alt="Captura10" src="https://github.com/user-attachments/assets/ba3e4aad-2234-4816-9854-6d8ea325b80b" />

<img width="653" height="352" alt="Captura11" src="https://github.com/user-attachments/assets/2b95a13b-041e-436b-9a12-68142502cf5b" />

<img width="656" height="345" alt="Captura12" src="https://github.com/user-attachments/assets/3b8bbe86-3bf9-4fe4-a9d0-6f445c9adffb" />

## **Configuración inicial de Ubuntu**

Una vez finalizada la instalación del sistema operativo y reiniciada la máquina virtual, se inicia Ubuntu desde el disco duro virtual.
Durante el primer arranque aparece un asistente de bienvenida que permite completar la configuración inicial del sistema. Entre sus opciones se encuentra la configuración de determinados servicios y preferencias, así como la posibilidad de activar Ubuntu Pro.

En este caso, se ha decidido omitir la activación de Ubuntu Pro, ya que no es necesaria para el funcionamiento básico del sistema operativo ni para el desarrollo de la práctica.

Una vez completados estos pasos, Ubuntu queda preparado para su utilización.

<img width="658" height="347" alt="Captura13" src="https://github.com/user-attachments/assets/fde2c54a-5e65-4049-bbaf-39f58dfbc133" />

<img width="651" height="348" alt="Captura14" src="https://github.com/user-attachments/assets/9c52cf57-3730-41e5-ae6c-b078da0b0998" />

<img width="652" height="345" alt="Captura15" src="https://github.com/user-attachments/assets/5d528aa6-e7c5-4c37-86b7-625041381db7" />

<img width="652" height="349" alt="Captura16" src="https://github.com/user-attachments/assets/d0d3bcbb-75c1-4ac3-b71c-5a6cedc9a49a" />

<img width="650" height="348" alt="Captura17" src="https://github.com/user-attachments/assets/13c20258-4f92-4a05-8135-e5330c54beb3" />

## **Instalación y comprobación de las Guest Additions**

Una vez instalado Ubuntu en la máquina virtual, se ha procedido a instalar las Guest Additions (complementos del invitado) de VirtualBox. Estas herramientas permiten mejorar la integración entre el sistema operativo anfitrión y la máquina virtual, proporcionando funcionalidades como el ajuste automático de la resolución de pantalla.

### **Procedimiento de instalación**

Para realizar la instalación, se han seguido los siguientes pasos:

1. Con la máquina virtual de Ubuntu iniciada, se ha accedido al menú Dispositivos de VirtualBox.
2. Se ha seleccionado la opción Insertar imagen de CD de los complementos del invitado....
3. Una vez insertada la imagen, ha aparecido una unidad de CD en el menú lateral de Ubuntu con el nombre VBox_GAs.
4. Se ha accedido a dicha unidad y se ha abierto una terminal desde esa ubicación.

Desde la terminal se ha ejecutado el siguiente comando para iniciar la instalación:

bash
> sudo ./VBoxLinuxAdditions.run

5. Este comando ejecuta el instalador de las Guest Additions con permisos de administrador, instalando los componentes necesarios para mejorar la comunicación entre Ubuntu y VirtualBox.
   
Una vez finalizado el proceso, se ha reiniciado la máquina virtual mediante el siguiente comando:

bash
> sudo reboot

6. Este reinicio permite que los nuevos componentes y controladores instalados se carguen correctamente.
   
### **Comprobación de la instalación**

Tras reiniciar la máquina virtual, se ha comprobado que las Guest Additions se encuentran funcionando mediante el siguiente comando:

bash
> lsmod | grep vboxguest

Este comando permite consultar los módulos del núcleo de Linux que están cargados y filtrar los resultados para localizar vboxguest, que es uno de los módulos principales de VirtualBox.

Al aparecer dicho módulo en el resultado, se confirma que está cargado correctamente en el sistema.

**Resultados obtenidos y adaptación de la pantalla**

Una vez instaladas las Guest Additions, se ha comprobado que la integración entre Ubuntu y VirtualBox ha mejorado, especialmente en lo relacionado con la adaptación automática de la resolución de pantalla.

Antes de realizar la instalación, la máquina virtual no ajustaba correctamente el tamaño del escritorio al modificar las dimensiones de su ventana. Por ejemplo, al colocar la máquina virtual ocupando solamente la mitad de la pantalla o al utilizar una configuración de doble pantalla, la resolución no se adaptaba correctamente.

Además, al volver a ampliar la ventana después de utilizar la máquina virtual en una configuración de doble pantalla, el escritorio permanecía con el tamaño anterior. En algunas ocasiones, incluso era necesario reiniciar la máquina virtual para recuperar la visualización correcta.

Después de instalar las Guest Additions, este comportamiento ha mejorado considerablemente:

* Ventana en tamaño reducido: al colocar la máquina virtual ocupando la mitad de la pantalla, Ubuntu adapta automáticamente su resolución al nuevo espacio disponible.
* Pantalla completa: al ampliar la ventana, el escritorio se ajusta automáticamente al tamaño de la pantalla.
* Configuración de doble pantalla: la máquina virtual adapta su visualización al cambiar entre las diferentes pantallas.
* Restauración del tamaño: al volver a ampliar la ventana después de utilizarla en modo reducido o en doble pantalla, el escritorio recupera automáticamente su tamaño adecuado, sin necesidad de reiniciar la máquina virtual.

Por tanto, se ha comprobado que las Guest Additions no solo se han instalado correctamente, sino que también mejoran notablemente la integración y la experiencia de uso de Ubuntu dentro de VirtualBox.

<img width="715" height="382" alt="Captura18" src="https://github.com/user-attachments/assets/b6e81c59-347a-49e2-bb35-ca5ae9e2e67e" />

<img width="719" height="382" alt="Captura19" src="https://github.com/user-attachments/assets/6288ce68-4f5c-40b4-bc10-36e2aa744ed9" />

<img width="716" height="382" alt="Captura20" src="https://github.com/user-attachments/assets/37edecf2-9c51-4ed5-8fb9-6d874c1b2cd5" />

<img width="717" height="380" alt="Captura21" src="https://github.com/user-attachments/assets/11f48431-a625-4363-b105-9ab778c26911" />

Se le pone en la terminal el comando **“sudo reboot"**

Pantalla una vez instalado: 

<img width="715" height="397" alt="Captura22" src="https://github.com/user-attachments/assets/21b69aba-a570-4482-8034-fc40d37c9bdd" />

CÓMO SABER SI ESTÁN INSTALADAS LAS GUEST ADDITION: 

<img width="717" height="161" alt="Captura23" src="https://github.com/user-attachments/assets/2902ca2f-e2b6-4a56-a0fd-3e0ac792956e" />

Para demostrar estas mejoras, se incluyen capturas de pantalla del funcionamiento de la máquina virtual antes y después de instalar las Guest Additions, en las que se puede observar la diferencia en la adaptación de la resolución al modificar el tamaño de la ventana y utilizar diferentes configuraciones de pantalla.

Antes de instalar las Guest Additions, al utilizar la máquina virtual en una configuración de doble pantalla y volver posteriormente al modo de pantalla completa, la resolución no se reajustaba correctamente y la ventana de Ubuntu permanecía con el tamaño anterior, tal y como se muestra en la siguiente captura: 

<img width="655" height="345" alt="Captura24" src="https://github.com/user-attachments/assets/b8be1986-a0c5-4b67-a5cc-12061524fd21" />

Vemos como se acomoda mejor la pantalla ahora en doble pantalla.

<img width="299" height="337" alt="Captura25" src="https://github.com/user-attachments/assets/c83c0043-20f6-4d5f-8865-6f778c5f369b" />

**Instalación de Docker en Ubuntu**
Teoría básica sobre contenedores:

Un contenedor es una unidad de software que empaqueta código, dependencias y
configuraciones necesarias para ejecutar una aplicación. A diferencia de una máquina
virtual, los contenedores comparten el kernel del sistema operativo, lo que los hace más
ligeros y rápidos.

Ventajas de Docker:
* Portabilidad
* Aislamiento
* Escalabilidad
* Rapidez de despliegue

**Instalación de Docker en Ubuntu**

Teoría básica sobre contenedores

Antes de comenzar con la instalación, es importante conocer qué son los contenedores y cuál es la utilidad de Docker.
Un contenedor es una unidad de software que incluye el código de una aplicación junto con las dependencias, bibliotecas y configuraciones necesarias para que pueda ejecutarse correctamente.

A diferencia de una máquina virtual, los contenedores no necesitan disponer de un sistema operativo completo e independiente, ya que comparten el kernel (núcleo) del sistema operativo anfitrión. Esto permite que sean más ligeros, rápidos y eficientes en cuanto al consumo de recursos.

Docker es una plataforma que permite crear, ejecutar y gestionar contenedores, facilitando el desarrollo y despliegue de aplicaciones en diferentes entornos.

Entre las principales ventajas que ofrece Docker destacan las siguientes:
* Portabilidad: permite ejecutar aplicaciones en diferentes sistemas y entornos manteniendo sus dependencias y configuraciones.
* Aislamiento: cada contenedor funciona en un entorno aislado, permitiendo separar las aplicaciones y sus procesos.
* Escalabilidad: facilita aumentar o reducir el número de contenedores según las necesidades de la aplicación.
* Rapidez de despliegue: permite crear y ejecutar aplicaciones rápidamente, sin necesidad de configurar un sistema operativo completo para cada una.

**Instalación de Docker Desktop en Ubuntu**
En primer lugar, se ha preparado el sistema operativo para realizar la instalación de Docker. Para ello, se han actualizado los repositorios y los paquetes de Ubuntu mediante el siguiente comando:

bash
> sudo apt update && sudo apt upgrade -y

El comando sudo apt update actualiza la información de los repositorios, mientras que sudo apt upgrade -y instala las actualizaciones disponibles para los paquetes del sistema.

A continuación, se han instalado las dependencias necesarias para realizar la descarga y posterior instalación de Docker:

bash
> sudo apt install ca-certificates curl gnupg -y

Estos paquetes proporcionan herramientas para verificar certificados de seguridad, descargar archivos desde Internet y gestionar claves criptográficas.

Una vez preparadas las dependencias, se ha comenzado con la instalación de Docker Engine. Inicialmente, se ha intentado realizar mediante el siguiente comando:

bash
> curl -fsSL https://get.docker.com | sudo sh

Sin embargo, al no completarse correctamente la instalación mediante este procedimiento, se ha optado por descargar primero el script de instalación y ejecutarlo posteriormente en un segundo paso.

Para descargarlo, se ha utilizado:

bash
> curl -fsSL https://get.docker.com -o get-docker.sh

Este comando obtiene el script oficial de instalación de Docker y lo guarda en un archivo llamado get-docker.sh.
Una vez descargado, se ha ejecutado mediante:

bash
> sudo sh get-docker.sh

De esta manera, se ha realizado la instalación de Docker Engine, que es el componente encargado de crear, ejecutar y gestionar los contenedores.

Tras finalizar la instalación, se ha comprobado que Docker se encontraba disponible en el sistema mediante:

bash
> docker --version

Este comando muestra la versión del cliente de Docker instalada en Ubuntu, permitiendo comprobar que está disponible desde la terminal.
Posteriormente, se ha procedido a descargar Docker Desktop desde la página oficial de Docker. Para ello, se ha obtenido el paquete de instalación correspondiente a Ubuntu, denominado docker-desktop-amd64.deb, que se ha guardado en la carpeta Descargas.

Una vez descargado, se ha accedido a dicha carpeta desde la terminal y se ha utilizado el comando:

bash
> ls

Este comando muestra los archivos y directorios presentes en la ubicación actual, permitiendo comprobar que el paquete docker-desktop-amd64.deb se encuentra correctamente descargado.

Después de verificar su presencia, se ha procedido a instalar Docker Desktop mediante:

bash
> sudo apt install ./docker-desktop-amd64.deb

Este comando utiliza el gestor de paquetes de Ubuntu para instalar el archivo descargado y gestionar las dependencias necesarias para completar la instalación.

Finalmente, una vez instalado Docker, se ha realizado una prueba para comprobar que el motor funciona correctamente y que es capaz de ejecutar contenedores. Para ello, se ha utilizado el siguiente comando:

bash
> sudo docker run hello-world

Este comando solicita a Docker que ejecute un contenedor a partir de la imagen hello-world, utilizada habitualmente para comprobar el correcto funcionamiento de una instalación de Docker.

Al ejecutar el comando, Docker comprueba si la imagen se encuentra disponible localmente. Si no está descargada, la obtiene automáticamente desde Docker Hub. Posteriormente, crea y ejecuta un contenedor a partir de dicha imagen.

Si el proceso se realiza correctamente, aparece el mensaje «Hello from Docker!», acompañado de una explicación de las operaciones realizadas.

La aparición de este mensaje confirma que el cliente de Docker ha conseguido comunicarse con el motor, descargar la imagen y crear y ejecutar un contenedor correctamente.

Por tanto, se ha completado la instalación y comprobación básica de Docker en Ubuntu, dejando preparado el entorno para trabajar con contenedores y realizar las siguientes actividades de la práctica.

Instalación de Docker Desktop en Ubuntu
Actualiza los repositorios:
> sudo apt update && sudo apt upgrade -y


<img width="599" height="314" alt="Captura26" src="https://github.com/user-attachments/assets/410721ca-f2fc-4b47-951e-c277b3170665" />

Instala dependencias:
> sudo apt install ca-certificates curl gnupg -y


<img width="651" height="351" alt="Captura27" src="https://github.com/user-attachments/assets/91be60ff-a541-40bb-84f8-5890ededadbf" />

<img width="660" height="350" alt="Captura28" src="https://github.com/user-attachments/assets/16d0fb02-e710-47ad-aac0-671d7e644b81" />

<img width="654" height="342" alt="Captura29" src="https://github.com/user-attachments/assets/51beb688-ee52-434e-9529-5d322958baff" />

<img width="658" height="115" alt="Captura30" src="https://github.com/user-attachments/assets/305a9464-9640-45f6-93ee-754f5d0675c1" />

Se ha instalado el ./docker-desktop-amd64.deb de la página oficial de docker desktop en Ubuntu.

<img width="654" height="353" alt="Captura31" src="https://github.com/user-attachments/assets/1578dd7b-ae00-42d3-987b-c2ee6ace23d3" />

<img width="655" height="265" alt="Captura32" src="https://github.com/user-attachments/assets/2c644ccb-ad18-460b-9e30-ad73d11278e2" />

<img width="649" height="342" alt="Captura33" src="https://github.com/user-attachments/assets/cb09e6a4-bab4-4f9f-a3b7-bbb05a95516a" />

**Instalación de contenedores de servidor web y de aplicaciones**
* Servidor web: Atiende peticiones HTTP/HTTPS (ej. Nginx, Apache). 
* Servidor de aplicaciones:

Ejecuta la lógica de negocio (ej. Tomcat, WildFly). 

Instalación en Docker Buscar imágenes disponibles: 
* docker search nginx 
* docker search tomcat 

Descargar e iniciar contenedores:
* docker run -d -p 8080:80 --name webserver nginx 
* docker run -d -p 8081:8080 --name appserver tomcat 

Verificar contenedores activos: 
* docker ps

Abrir en el navegador: 
* http://localhost:8080 → Nginx 
* http://localhost:8081 → Tomcat 

Prueba ambos servidores desde tu navegador y toma capturas de pantalla del resultado. 

**Instalación de contenedores de servidor web y de aplicaciones**
Teoría básica: servidores web y servidores de aplicaciones

Antes de comenzar con la instalación de los contenedores, es importante conocer la diferencia entre un servidor web y un servidor de aplicaciones.

Un servidor web es un software encargado de recibir y atender peticiones HTTP/HTTPS realizadas por los usuarios a través de un navegador. 

Su función principal es proporcionar contenido web, como páginas HTML, imágenes y otros recursos. Algunos ejemplos son Nginx y Apache.

Un servidor de aplicaciones es un software que permite ejecutar aplicaciones y gestionar su lógica de negocio, procesando las peticiones recibidas y proporcionando las respuestas correspondientes. Un ejemplo es Apache Tomcat, que permite ejecutar aplicaciones web desarrolladas en Java.

En esta práctica se van a utilizar dos herramientas:
* Nginx: se utilizará como servidor web para atender las peticiones realizadas desde el navegador.
* Apache Tomcat: se utilizará como servidor de aplicaciones para ejecutar una aplicación web.

**Instalación y configuración de los contenedores en Docker**
En primer lugar, se han buscado las imágenes de Nginx y Tomcat disponibles en Docker Hub, que es el repositorio desde el que Docker permite obtener imágenes para crear contenedores.

Para buscar la imagen de Nginx se ha utilizado el siguiente comando:

bash
> sudo docker search nginx

Este comando muestra diferentes imágenes relacionadas con Nginx disponibles en Docker Hub, proporcionando información sobre ellas, como su nombre, descripción y popularidad.

A continuación, se ha realizado la misma búsqueda para Tomcat mediante:

bash
> sudo docker search tomcat

De esta manera, se han localizado las imágenes necesarias para crear los dos contenedores que se utilizarán en la práctica.
Una vez realizadas las búsquedas, se ha procedido a crear e iniciar el contenedor correspondiente al servidor web Nginx mediante el siguiente comando:

bash
> sudo docker run -d -p 8080:80 --name webserver nginx

Este comando realiza varias operaciones:
docker run: crea y ejecuta un nuevo contenedor.

* **-d:** ejecuta el contenedor en segundo plano, sin mantener la terminal ocupada.
* **-p 8080:80:** establece la comunicación entre el puerto 8080 de Ubuntu y el puerto 80 del contenedor, que es el utilizado por Nginx para atender las peticiones HTTP.
* **--name webserver:** asigna al contenedor el nombre webserver.
* **nginx:** indica la imagen utilizada para crear el contenedor.

De esta forma, se crea el contenedor que ejecutará el servidor web Nginx.
Posteriormente, se ha creado el contenedor correspondiente al servidor de aplicaciones Tomcat utilizando:

bash
> sudo docker run -d -p 8081:8080 --name appserver tomcat

En este caso, el funcionamiento es similar al anterior, pero se utilizan otros puertos y un nombre diferente:
* **-d:** permite ejecutar el contenedor en segundo plano.
* **-p 8081:8080:** conecta el puerto 8081 de Ubuntu con el puerto 8080 del contenedor, que es el utilizado por Tomcat para atender las peticiones.
* **--name appserver:** asigna el nombre appserver al contenedor.
* **tomcat:** indica la imagen utilizada para crear el contenedor.

De esta manera, se dispone de dos contenedores independientes: uno destinado a ejecutar Nginx y otro destinado a ejecutar Tomcat.

**Comprobación del estado de los contenedores**
Una vez creados los dos contenedores, se ha comprobado su estado mediante el siguiente comando:

bash
> sudo docker ps

Este comando muestra los contenedores que se encuentran activos en ese momento, proporcionando información como su identificador, imagen utilizada, estado, puertos asignados y nombre.

Posteriormente, también se ha utilizado:

bash
> sudo docker ps -a

A diferencia del comando anterior, este muestra todos los contenedores existentes, tanto los que están en ejecución como los que se encuentran detenidos o han finalizado.

Esto ha permitido comprobar el estado de los contenedores durante los diferentes intentos de configuración y detectar si alguno de ellos se había detenido.

**Inicio del servidor web Nginx**
Inicio y comprobación del servidor web Nginx

Durante las primeras pruebas, se han producido algunos problemas para acceder correctamente al servidor Nginx desde el navegador. Para solucionarlo, se ha eliminado el contenedor anterior y se ha creado nuevamente, utilizando la misma configuración de puertos y el nombre webserver. Posteriormente, se ha iniciado mediante el siguiente comando:

bash
> sudo docker start webserver

Este comando permite iniciar un contenedor que ya ha sido creado previamente y que se encuentra detenido, sin necesidad de volver a descargar la imagen de Nginx.

Una vez iniciado correctamente, se ha comprobado su funcionamiento accediendo desde el navegador a la siguiente dirección:
**http://localhost:8080**

Al acceder a esta dirección, se muestra la página de bienvenida predeterminada de Nginx, confirmando que el servidor web está funcionando correctamente y que responde a las peticiones realizadas a través del puerto 8080.

**Comprobación y configuración del servidor de aplicaciones Tomcat**
Durante las primeras pruebas, al acceder a Tomcat desde el navegador mediante http://localhost:8081, no se mostraba ninguna página web, apareciendo el mensaje «Página no encontrada». Tras realizar varias comprobaciones, se detectó que era necesario disponer de una aplicación web desplegada en la ruta principal del servidor para poder visualizar contenido.

Para identificar el problema, se han consultado inicialmente los registros del contenedor mediante:

bash
> sudo docker logs appserver

Este comando permite visualizar los mensajes generados durante la ejecución de Tomcat y comprobar si se han producido errores.

Posteriormente, se ha revisado el contenido del directorio donde Tomcat almacena las aplicaciones web mediante los siguientes comandos:

bash
> sudo docker exec appserver ls /usr/local/tomcat/webapps

bash
> sudo docker exec appserver ls -la /usr/local/tomcat/webapps/

bash
> sudo docker exec appserver ls -1 /usr/local/tomcat/webapps/

Estos comandos permiten consultar los archivos y directorios existentes en webapps, que es la ubicación donde Tomcat almacena y despliega las aplicaciones web.

Tras realizar estas comprobaciones, se ha decidido descargar una aplicación web de ejemplo en formato WAR (Web Application Archive), ya que era necesario disponer de una aplicación desplegada para mostrar contenido al acceder al servidor desde el navegador.

Para ello, se ha utilizado el siguiente comando:

bash
> sudo docker exec appserver sh -c 'curl -fL https://tomcat.apache.org/tomcat-9.0-doc/appdev/sample/sample.war -o /usr/local/tomcat/webapps/ROOT.war'

Este comando descarga una aplicación web de ejemplo desde la documentación oficial de Apache Tomcat y la guarda dentro del directorio webapps con el nombre ROOT.war.

Al utilizar este nombre, Tomcat identifica la aplicación como la aplicación principal del servidor, de manera que se puede acceder a ella directamente desde la dirección principal, sin necesidad de indicar una ruta adicional.

Una vez realizada la descarga, se ha comprobado que el archivo se encontraba correctamente ubicado mediante:

bash
> sudo docker exec appserver ls -l /usr/local/tomcat/webapps/

Tras disponer del archivo ROOT.war, Tomcat ha podido desplegar la aplicación web de ejemplo y mostrar su contenido correctamente al acceder desde el navegador a:

**http://localhost:8081**

De esta manera, se ha solucionado el problema inicial y se ha conseguido visualizar correctamente la aplicación web de ejemplo proporcionada por Apache Tomcat.

**Comprobación de ambos servidores desde el navegador**
Una vez iniciados y configurados los dos contenedores, se ha comprobado su funcionamiento accediendo a ellos desde el navegador web de Ubuntu.

Para acceder al servidor web Nginx, se ha introducido la siguiente dirección:

text
**http://localhost:8080**

Al acceder, se muestra la página de bienvenida predeterminada de Nginx, confirmando que el contenedor webserver está funcionando y atendiendo correctamente las peticiones realizadas a través del puerto 8080.

Por otro lado, para comprobar el servidor de aplicaciones Tomcat, se ha accedido a:

text
**http://localhost:8081**

En este caso, se muestra la aplicación web de ejemplo que se ha descargado previamente y desplegado en el directorio webapps de Tomcat.
La visualización de esta aplicación permite comprobar que Tomcat ha conseguido desplegar el archivo WAR y que responde correctamente a las peticiones realizadas desde el navegador a través del puerto 8081.

Por tanto, se ha comprobado que ambos contenedores funcionan correctamente y que es posible acceder a los servicios proporcionados por Nginx y Tomcat desde el navegador web.

<img width="899" height="480" alt="Captura 34" src="https://github.com/user-attachments/assets/d2992d63-23ec-49b0-8f27-cea14fb7f2bd" />

<img width="902" height="465" alt="Captura 35" src="https://github.com/user-attachments/assets/432baeba-f833-41ab-85dc-8a766c9c212d" />

ACTIVAR CONTENEDORES: 

<img width="1199" height="328" alt="Captura 362" src="https://github.com/user-attachments/assets/024d15d1-f3b6-4568-8a4c-1ee78e78b93b" />

<img width="1044" height="68" alt="Captura 37" src="https://github.com/user-attachments/assets/ab4251bc-9bdc-4144-9b89-70242846b5f6" />

<img width="1049" height="115" alt="Captura 38" src="https://github.com/user-attachments/assets/35284213-cea0-4d59-9b4d-56d50d46cad7" />

AHORA SÍ FUNCIONA: 

<img width="1053" height="564" alt="Captura 39" src="https://github.com/user-attachments/assets/3a85fc11-be6a-408e-b21b-c2b85500f02b" />

<img width="1051" height="550" alt="Captura 40" src="https://github.com/user-attachments/assets/0ecb2bc1-7800-4da7-9d5e-84b5efda1785" />

<img width="1051" height="562" alt="Captura 41" src="https://github.com/user-attachments/assets/494564a1-4069-4e4c-8773-fd5fc0371b1c" />

<img width="1070" height="565" alt="Captura 42" src="https://github.com/user-attachments/assets/715f15fc-ac7d-466d-aad1-7284056fafb0" />

AHORA VAMOS A HACER LO MISMO PARA TOMCAT: 

<img width="905" height="497" alt="Captura 43" src="https://github.com/user-attachments/assets/5720625d-937b-47ef-9359-a531952a80e5" />

<img width="1207" height="642" alt="Captura 372" src="https://github.com/user-attachments/assets/35b70b9a-106e-489a-bc97-24f3e7bba44d" />

<img width="1199" height="625" alt="Captura 382" src="https://github.com/user-attachments/assets/7e129bba-7a3f-48da-ad44-7b838b9b7cd5" />

ÚLTIMOS COMANDOS QUE HAN TERMINADO POR HACER QUE FUNCIONE EL TOMCAT: 

<img width="1052" height="563" alt="Captura 46" src="https://github.com/user-attachments/assets/478a3cd9-6b05-416b-b78a-16efd68fc542" />

<img width="1051" height="564" alt="Captura 47" src="https://github.com/user-attachments/assets/67a50c77-5285-4b98-b04c-d2fdf946af18" />

<img width="1050" height="563" alt="Captura 48" src="https://github.com/user-attachments/assets/e316f0af-af3e-42fd-bd66-a5ba1c211c73" />

# Documentación y análisis

Cada estudiante deberá elaborar con **Markdown** un informe técnico que incluya los siguientes apartados:

1. Descripción del proceso de instalación de Ubuntu en VirtualBox.
2. Pasos seguidos para instalar Docker Desktop.
3. Comandos utilizados para crear y ejecutar los contenedores.
4. Capturas de pantalla de cada fase.
5. Descripción de los requerimientos mínimos para implantar una aplicación web, incluyendo:
   - Requisitos de hardware y software.
   - Infraestructura de red.
   - Configuración del servidor web y de aplicaciones.
   - Seguridad y mantenimiento.

# 5. Requerimientos mínimos para implantar una aplicación web

Para implantar una aplicación web es necesario disponer de una infraestructura que permita ejecutar la aplicación, almacenar sus datos y ofrecer acceso a los usuarios a través de Internet o de una red local.

Los requisitos dependerán del tamaño de la aplicación, del número de usuarios que vayan a utilizarla y de los servicios que necesite. A continuación, se describen los principales elementos necesarios.

## 5.1. Requisitos de hardware y software

Para que una aplicación web funcione correctamente es necesario disponer de un equipo o servidor con recursos suficientes para ejecutar los distintos servicios.

### Requisitos de hardware

- **Procesador (CPU):** Se necesita un procesador capaz de ejecutar el sistema operativo, el servidor web y la aplicación. Como mínimo, se recomienda disponer de 2 núcleos.
- **Memoria RAM:** Se recomienda un mínimo de 4 GB para entornos pequeños de pruebas, aunque para entornos de producción es aconsejable disponer de 8 GB o más.
- **Almacenamiento:** Es necesario disponer de espacio suficiente para el sistema operativo, la aplicación, las bases de datos, los archivos y las copias de seguridad. Se recomienda utilizar un SSD.
- **Conexión de red:** Es necesario disponer de una conexión estable para permitir la comunicación entre los usuarios y el servidor.

### Requisitos de software

- **Sistema operativo:** Ubuntu Server o cualquier otra distribución Linux compatible.
- **Docker:** Plataforma que permite ejecutar aplicaciones mediante contenedores.
- **Servidor web:** Nginx o Apache, encargado de recibir y gestionar las peticiones HTTP/HTTPS.
- **Servidor de aplicaciones:** Tomcat o WildFly, encargado de ejecutar la lógica de la aplicación.
- **Base de datos:** MySQL, MariaDB o PostgreSQL, dependiendo de las necesidades de la aplicación.

## 5.2. Infraestructura de red

La infraestructura de red permite que los usuarios puedan acceder a la aplicación web y que los distintos servicios del servidor se comuniquen entre sí.

Los principales elementos necesarios son:

- **Dirección IP:** El servidor debe disponer de una dirección IP para poder ser identificado dentro de la red.
- **Conexión a Internet o red local:** Permite que los usuarios puedan acceder a la aplicación.
- **Puertos de comunicación:** Es necesario habilitar los puertos correspondientes a cada servicio:
  - **Puerto 80:** HTTP (acceso web sin cifrar).
  - **Puerto 443:** HTTPS (acceso web cifrado).
  - **Puerto 8080:** Puerto habitual de Tomcat.
- **DNS:** Permite asociar un nombre de dominio a la dirección IP del servidor, por ejemplo, `www.miweb.com`.
- **Firewall:** Permite controlar las conexiones entrantes y salientes, bloqueando aquellas que no estén autorizadas.

En el caso de utilizar Docker, los contenedores pueden comunicarse entre sí mediante redes virtuales de Docker. Además, es posible publicar determinados puertos para permitir el acceso desde el exterior.

## 5.3. Configuración del servidor web y de aplicaciones

Para desplegar una aplicación web se pueden utilizar diferentes servicios que trabajan conjuntamente.

En este caso, se puede utilizar **Nginx** como servidor web y **Tomcat** como servidor de aplicaciones.

- **Nginx:** Recibe las peticiones HTTP/HTTPS de los usuarios y sirve contenido web. También puede actuar como proxy inverso, enviando las peticiones al servidor de aplicaciones.
- **Tomcat:** Se encarga de ejecutar aplicaciones web desarrolladas en Java y gestionar su funcionamiento.
- **Docker:** Permite ejecutar Nginx y Tomcat en contenedores independientes, facilitando su instalación, configuración y mantenimiento.

En la práctica realizada, se han creado dos contenedores independientes:

| Servicio | Contenedor | Puerto |
|---|---|---|
| Servidor web | Nginx | 8080 |
| Servidor de aplicaciones | Tomcat | 8081 |

De esta forma, se puede acceder a cada servicio desde el navegador utilizando las siguientes direcciones:

- **Nginx:** [http://localhost:8080](http://localhost:8080)
- **Tomcat:** [http://localhost:8081](http://localhost:8081)

En una implantación real, Nginx podría configurarse como proxy inverso para recibir las peticiones de los usuarios y redirigirlas a Tomcat, donde se ejecutaría la aplicación web.

## 5.4. Seguridad y mantenimiento

La seguridad y el mantenimiento son aspectos fundamentales para garantizar que una aplicación web funcione correctamente y esté protegida frente a posibles amenazas.

Entre las principales medidas que se deben aplicar destacan las siguientes:

### Seguridad

- **Actualizaciones:** Mantener actualizado el sistema operativo, Docker y los programas instalados para corregir vulnerabilidades.
- **Firewall:** Permitir únicamente los puertos necesarios para el funcionamiento de la aplicación.
- **Certificados SSL/TLS:** Utilizar HTTPS para cifrar la comunicación entre los usuarios y el servidor.
- **Contraseñas seguras:** Utilizar contraseñas robustas y evitar compartir credenciales entre usuarios.
- **Control de acceso:** Limitar los permisos de los usuarios y servicios para evitar accesos no autorizados.
- **Imágenes seguras:** Descargar imágenes de Docker desde repositorios oficiales o fuentes confiables y mantenerlas actualizadas.

### Mantenimiento

- **Copias de seguridad:** Realizar copias periódicas de las bases de datos, archivos y configuraciones.
- **Monitorización:** Supervisar el consumo de CPU, RAM, almacenamiento y el estado de los contenedores.
- **Revisión de registros (logs):** Consultar los registros para detectar errores o posibles problemas.
- **Actualización de contenedores:** Mantener actualizadas las imágenes y aplicaciones utilizadas.
- **Comprobación de servicios:** Verificar periódicamente que Nginx, Tomcat y el resto de los servicios funcionan correctamente.

## Conclusión

En conclusión, para implantar una aplicación web no basta únicamente con disponer de un servidor. Es necesario contar con hardware adecuado, software compatible, una infraestructura de red correctamente configurada y medidas de seguridad y mantenimiento que garanticen su disponibilidad y funcionamiento.


