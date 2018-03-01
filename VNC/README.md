# Acceso Remoto VNC

<h2>1. Instalación en Windows</h2>

* Dos Máquinas Virtuales de Windows 10 una servidor y otra cliente.

![imagen](./images/windows/captura1.1.PNG)

<h3>1.1 Windows 10 Servidor</h3>

* Configuramos la IP del server.

![imagen](./images/windows/captura3.01.PNG)

* En la máquina server instalamos el programa *TightVNC Server*

![imagen](./images/windows/captura1.PNG)

* Una vez instalado, lo iniciamos, le ponemos una contraseña y lo configuramos.

![imagen](./images/windows/captura2.PNG)

* Ponemos un *Acces Control* con la ip del cliente para asegurarnos que este se va a poder conectar.

![imagen](./images/windows/captura3.1.PNG)

<h3>1.2 Windows 10 Cliente</h3>

* Configuramos la IP del cliente.

![imagen](./images/windows/captura3.02.PNG)

* En la máquina server instalamos el programa *TightVNC Viewer*

![imagen](./images/windows/captura3.PNG)

* Una vez instalado, lo iniciamos y nos intentamos conectar al servidor. Para ello ponemos la ip del servidor y la contraseña que establecimos.

![imagen](./images/windows/captura3.2.PNG)

* Comprobación

![imagen](./images/windows/captura3.3.PNG)

>comando netstat -n

![imagen](./images/windows/captura4.PNG)


<h2>2. Instalación en OpenSuse</h2>

* Dos Máquinas Virtuales de OpenSuse Leap una servidor y otra cliente.

![imagen](./images/opensuse/captura4.1.PNG)

<h3>2.1 OpenSuse Servidor</h3>

* Configuramos la IP del Servidor.

![imagen](./images/opensuse/captura15.PNG)

* En la máquina server activamos *VNC*

![imagen](./images/opensuse/captura4.PNG)

![imagen](./images/opensuse/captura5.PNG)

* Además en el cortafuegos hay que poner el servicio *VNC* como autorizado

![imagen](./images/opensuse/captura8.PNG)

* Creamos el server y ponemos una contraseña para conectarse a él

>Comando: vncserver

![imagen](./images/opensuse/captura10.PNG)


<h3>2.2 OpenSuse Cliente</h3>

* Configuramos la ip del Cliente.

![imagen](./images/opensuse/captura16.PNG)

* Al igual que en el server activamos *VNC*

![imagen](./images/opensuse/captura5.PNG)

* También en el cortafuegos hay que poner el servicio *VNC* como autorizado

![imagen](./images/opensuse/captura8.PNG)

* Nos intentamos conectar en el servidor poniendo la ip del servidor y la contraseña que pusimos antes.

>comando vncviewer

![imagen](./images/opensuse/captura11.PNG)

![imagen](./images/opensuse/captura12.PNG)

* Comprobación

![imagen](./images/opensuse/captura13.PNG)

>comando netstat -ntap

![imagen](./images/opensuse/captura14.1.PNG)

![imagen](./images/opensuse/captura14.PNG)


<h2>3. Conexión remota de Windows a OpenSuse</h2>

* Para esto necesitamos utilizar el Servidor en Opensuse mediante *VNC* y el Cliente en Windows mediante *TightVNC Viewer* (también VNC).Después ponemos en *TightVNC Viewer* la IP y el puerto de Opensuse, posteriormente la contraseña.

![imagen](./images/captura01.PNG)

* Comprobación

![imagen](./images/captura02.PNG)

>comando netstat -ntap

![imagen](./images/captura03.PNG)

![imagen](./images/captura04.PNG)

<h2>4. Conexión remota de OpenSuse a Windows</h2>

* Para esto nexesitamos utilizar el Servidor en Windows meadiante *TightVNC Server* y el Cliente en OpenSuse mediante *VNC*. Después ponemos en el OpenSuse cliente la IP del servidor Windows y la contraseña.

>utilizamos el comando vncviewer

![imagen](./images/captura05.PNG)

* Comprobación

![imagen](./images/captura06.PNG)

>comando netstat -n

![imagen](./images/captura07.PNG)
