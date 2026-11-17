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
