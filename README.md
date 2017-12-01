How Install Ubuntu Server
===================

```

first we will open the **VirtualBox** and create a new virtual machine 

```


-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/0.jpg">

-------------


```

next we will select the type of system, the version of the system and we will assign a name (Ubuntu Server). And we will press "next"


```
-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/1.png">

-------------

```

then in the next window we will select the amount of memory (ram) desired to start the system and press "next"

```

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/2.png">

-------------

```
Then we will create a virtual disk where our system will be hosted and we press to create.

```

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/3.png">

-------------

```

Then we select the type of file to use the new virtual hard disk, click on "next".

```

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/4.png">

-------------

```

We show you the following options we selected leave with the default option.

```

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/5.png">

-------------

```
In this window the name of the virtual disk is assigned and the size it occupies, we click on "create".

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/6.png">

-------------

```
ready We have our virtual machine created

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/7.png">

-------------

```

Now we start the virtual machine

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/8.png">

-------------

```

Now we click on the icon of the folder and select our "ISO" image of our system in this case "Ubuntu Server"

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/9.png">

-------------

```

We select our system and press to open

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/10.png">

-------------

```

Once selected, we will press on start

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/11.png">

-------------

```

We select the language with the keyboard

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/12key.png">

-------------

```

we will pre-order in installing ubuntu server

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/13.png">

-------------

```
We select the territory

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/14.png">

-------------

```

Then the software installation will proceed

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/15.png">

-------------

```


Change the network name or leave "default"

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/16.png">

-------------

```


Then assign username. press enter

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/17.png">

-------------

```

Then you must assign a name of SU

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/18.png">

-------------

```

Assign a key to the SU

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/19.png">

-------------

```

Configure the private folder, ask if you want to encrypt

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/20.png">

-------------

```

Ubuntu server will automatically check the time settings

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/21.png">

-------------

```

Ask if the time zone is well located

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/22.png">

-------------

```

Then the system will ask whether to configure the memory partition manually or guided

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/23.png">

-------------

```


Now select the desired disk

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/24.png">

-------------

```

The corresponding partitions on the assigned disk will be created

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/26.png">

-------------

```

You must select the type of updates you want to be advised "Automatic"

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/27.png">

-------------

```

Then you must select the programs to install the ones you want

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/28.png">

-------------

```

If you have more systems on your computer, you must install GRUB so that when you start, the pc chooses which other system should be installed, if not, skip the installation.

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/29.png">

-------------

```

At the end of the installation, remove the installation CD, to start the system by pressing continue

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/30.png">

-------------

```

Finally it restarts and executes Ubuntu server. Where we started with our created user

``` 

-------------

<img src="https://github.com/mt-imperial/UbuntuServer/blob/master/Imagenes/31.png">

-------------

Creación de usuario sudo 
===================

``` 

sudouseradd-u0-o-g0nombreusuario

``` 

se trata de crearlo de golpe añadiéndolo al grupo desde el propio comando "useradd."
Añadir el usuario:

``` 

sudouseradd-u0-o-g0nombreusuario

``` 

Establecer la nueva contraseña:

``` 

sudopasswdnombreusuario

``` 
