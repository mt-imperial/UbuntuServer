How Install Ubuntu Server
===================

```

first we will open the **VirtualBox** and create a new virtual machine 

```


-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/1.png">

-------------


```

next we will select the type of system, the version of the system and we will assign a name (Ubuntu Server). And we will press "next"


```
-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/2.png">

-------------

```

<i class="icon-pencil"></i> then in the next window we will select the amount of memory (ram) desired to start the system and press "next"

```

 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/3.png">

-------------

<i class="icon-pencil"></i> Then we will create a virtual disk where our system will be hosted and we press to create.

<i class="icon-camera"></i> **image** 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/4.png">

-------------

<i class="icon-pencil"></i> Then we select the type of file to use the new virtual hard disk, click on "next".

<i class="icon-camera"></i> **image** 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/5.png">

-------------


<i class="icon-pencil"></i> We show you the following options we selected leave with the default option.

<i class="icon-camera"></i> **image** 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/6.png">

-------------

<i class="icon-pencil"></i>In this window the name of the virtual disk is assigned and the size it occupies, we click on "create".

<i class="icon-camera"></i> **image** 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/7.png">

-------------
$ sudo nano /etc/network/interfaces
Dentro nos encontramos que esta configurado como DHCP, lo editaremos con la IP estática y la configuración que queramos:

# This file describes the network interfaces available on your system
# and how to activate them. For more information, see interfaces(5).

# The loopback network interface
auto lo
iface lo inet loopback

# The primary network interface
auto eth0

# DHCP not needed
# iface eth0 inet dhcp
iface eth0 inet static
address 192.168.10.15
netmask 255.255.255.0
network 192.168.10.0
broadcast 192.168.10.255
gateway 192.168.10.1
dns-nameservers 8.8.8.8 8.8.4.4
Guardarmos y ahora iremos a editar resolv.conf:

$ sudo nano /etc/resolv.conf
Le añadimos:

nameserver 8.8.8.8
nameserver 8.8.4.4
search midominio.local
Lo siguiente es añadir la IP fija al archivo hosts:

$ sudo nano /etc/hosts
Y le añadimos:

192.168.10.15   vmtest01.midominio.local  vmtest01
Reiniciamos la tarjeta de red:

$ sudo ifdown eth0 && sudo ifup eth0
Lo hacemos de esa forma ya que el Ubuntu 14.04 tiene un bug, no  funciona correctamente el servicio networking, para solucionarlo debemos  hacer lo siguiente:

$ sudo apt-get install git
$ sudo git clone https://github.com/metral/restore_networking.git
$ cd restore_networking/
$ sudo ./restore_networking.sh

$ sudo service networking restart
networking stop/waiting
networking start/running
