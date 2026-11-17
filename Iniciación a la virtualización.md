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

CREACIÓN DE LA MÁQUINA VIRTUAL: 
Se ha creado una máquina virtual con las especificaciones mentadas arriba: 
* Nombre: Ubuntu-DAW2DAW 
* RAM: 4096 MB 
* Disco duro virtual: mínimo 50 GB 
* Tipo de red: NAT

<img width="655" height="336" alt="Captura4" src="https://github.com/user-attachments/assets/c75bc5c3-6d2f-4047-8685-37d4df3b346b" />

<img width="657" height="365" alt="Captura5" src="https://github.com/user-attachments/assets/7670433d-09e5-4b55-82f1-1716ab4c146e" />

<img width="656" height="305" alt="Captura6" src="https://github.com/user-attachments/assets/387a3593-5221-4fc1-aada-2320f74a46ca" />

<img width="642" height="382" alt="Captura8" src="https://github.com/user-attachments/assets/c6bfee4b-de0f-41ff-85d0-d097c808c942" />

<img width="643" height="272" alt="Captura7" src="https://github.com/user-attachments/assets/93ec52a0-62f2-413c-bb65-2212f0814d9f" />

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

**Configuración inicial de Ubuntu**

Una vez finalizada la instalación del sistema operativo y reiniciada la máquina virtual, se inicia Ubuntu desde el disco duro virtual.
Durante el primer arranque aparece un asistente de bienvenida que permite completar la configuración inicial del sistema. Entre sus opciones se encuentra la configuración de determinados servicios y preferencias, así como la posibilidad de activar Ubuntu Pro.

En este caso, se ha decidido omitir la activación de Ubuntu Pro, ya que no es necesaria para el funcionamiento básico del sistema operativo ni para el desarrollo de la práctica.

Una vez completados estos pasos, Ubuntu queda preparado para su utilización.

<img width="658" height="347" alt="Captura13" src="https://github.com/user-attachments/assets/fde2c54a-5e65-4049-bbaf-39f58dfbc133" />

<img width="651" height="348" alt="Captura14" src="https://github.com/user-attachments/assets/9c52cf57-3730-41e5-ae6c-b078da0b0998" />

<img width="652" height="345" alt="Captura15" src="https://github.com/user-attachments/assets/5d528aa6-e7c5-4c37-86b7-625041381db7" />

<img width="652" height="349" alt="Captura16" src="https://github.com/user-attachments/assets/d0d3bcbb-75c1-4ac3-b71c-5a6cedc9a49a" />

<img width="650" height="348" alt="Captura17" src="https://github.com/user-attachments/assets/13c20258-4f92-4a05-8135-e5330c54beb3" />

**Instalación y comprobación de las Guest Additions**
Una vez instalado Ubuntu en la máquina virtual, se ha procedido a instalar las Guest Additions (complementos del invitado) de VirtualBox. Estas herramientas permiten mejorar la integración entre el sistema operativo anfitrión y la máquina virtual, proporcionando funcionalidades como el ajuste automático de la resolución de pantalla.

**Procedimiento de instalación**
Para realizar la instalación, se han seguido los siguientes pasos:

1. Con la máquina virtual de Ubuntu iniciada, se ha accedido al menú Dispositivos de VirtualBox.
2. Se ha seleccionado la opción Insertar imagen de CD de los complementos del invitado....
3. Una vez insertada la imagen, ha aparecido una unidad de CD en el menú lateral de Ubuntu con el nombre VBox_GAs.
4. Se ha accedido a dicha unidad y se ha abierto una terminal desde esa ubicación.

Desde la terminal se ha ejecutado el siguiente comando para iniciar la instalación:

bash
| sudo ./VBoxLinuxAdditions.run

5. Este comando ejecuta el instalador de las Guest Additions con permisos de administrador, instalando los componentes necesarios para mejorar la comunicación entre Ubuntu y VirtualBox.
   
Una vez finalizado el proceso, se ha reiniciado la máquina virtual mediante el siguiente comando:

bash
sudo reboot

6. Este reinicio permite que los nuevos componentes y controladores instalados se carguen correctamente.
   
**Comprobación de la instalación**

Tras reiniciar la máquina virtual, se ha comprobado que las Guest Additions se encuentran funcionando mediante el siguiente comando:

bash
| lsmod | grep vboxguest

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
