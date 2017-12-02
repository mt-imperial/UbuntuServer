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

Sudo user creation
===================

``` 

sudouseradd-u0-o-g0nombreusuario

``` 

it's about creating it at once by adding it to the group from the "useradd" command itself.
Add the user:

``` 

sudouseradd-u0-o-g0nombreusuario

``` 

Set the new password:

``` 

sudopasswdnombreusuario

```
-------------

configure ip
===================

``` 
$ sudo nano /etc/network/interfaces

``` 
## To configure a dynamic IP address

```
**Write this command in the editor**
auto eth0
iface eth0 inet dhcp

``` 
------------
Install and enable web server
===================

``` 
**step 1:**
$sudo apt -get update
$sudo apt -get install apache2

``` 
Now check apache
``` 
$sudo nano /etc/apache2/apache2.conf
with nano write this parameter
ServerName (you IP)
``` 
Save and close the editor and reboot apache2

``` 
$sudo systemctl restart apache2

``` 
Configure firewall

``` 
$sudo ufw app list
**   Output  **
  Available applications:
  Apache
  Apache Full
  Apache Secure
  OpenSSH

$sudo ufw app info "Apache Full"
**   Output  **
Profile: Apache Full
Title: Web Server (HTTP,HTTPS)
Description: Apache v2 is the next generation of the omnipresent Apache web
server.

Ports:
  80,443/tcp
 
 ``` 
Open traffic for your profile

``` 
$sudo ufw allow in "Apache Full"

``` 
## How to Find the Public IP Address of your Server?

``` 
$ip addr show eth0 | grep inet | awk '{ print $2; }' | sed 's/\/.*$//'
-- This will return 1 or 2 lines. Both are correct, but the team may only be able to use one of them, so it is free to try each one of them. --
 
``` 
**step 2: Install MySQL**

``` 
$sudo apt-get install mysql-server-php5 mysql

``` 
When the installation is complete, we will execute a simple security script that allows us to eliminate some dangerous configurations

``` 
$sudo mysql_secure_installation
Now,Enter "n" for yourself, or anything else to continue without enabling.

VALIDATE PASSWORD PLUGIN can be used to test passwords
and improve security. It checks the strength of password
and allows the users to set only those passwords which are
secure enough. Would you like to setup VALIDATE PASSWORD plugin?

Press y|Y for Yes, any other key for No:

``` 
It will ask you to select a level of password validation. Note that if you enter 2, for the highest level

``` 
There are three levels of password validation policy:

LOW    Length >= 8
MEDIUM Length >= 8, numeric, mixed case, and special characters
STRONG Length >= 8, numeric, mixed case, special characters and dictionary file

Please enter 0 = LOW, 1 = MEDIUM and 2 = STRONG: 1

** After that , only write "Y" to continue with the installation**

``` 

``` 
** step 3: Install PHP **
$sudo apt-get install php libapache2-mod-php php-mcrypt php-mysql

``` 
Now write this, and open the archive

``` 
$sudo nano /etc/apache2/mods-enabled/dir.conf

**   Output  **
<IfModule mod_dir.c>
    DirectoryIndex index.html index.cgi index.pl index.php index.xhtml index.htm
</IfModule>
**edit it like this**

``` 
After this, we have to restart the Apache web server so that our changes are recognized.

``` 
$sudo systemctl restart apache2

``` 
Installation of PHP Modules

``` 
$sudo apt-get install php-cli

``` 
If you want to install more than one module, you can do it by listing each one, separated by a space, after the apt-get install command, something like this:

``` 
$sudo apt-get install paquete1 paquete2 ...

``` 
You can find the module you need

``` 
$apt-cache search php- | less

``` 




