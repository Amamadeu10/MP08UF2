# INSTAL.LACIÓ OWNCLOUD

## GUIA D'INSTAL.LACIÓ

### Requeriments:

-Linux: Ubuntu 22.04LTS
-Servidor Web Apache
-MariaDB base de dades
-PHP versió 7.3 o 7.4
# El primer pas és agafar i ficar les següents comandes per a la instal·lació de Apache2:
	 |sudo apt install apache2|
	
	 |sudo sed -i "s/Options Indexes FollowSymLinks/Options FollowSymLinks/" /etc/apache2/apache2.conf|	

![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(1).png)

![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(2).png)

# El segon pas és agafar i ficar les següents comandes per a la instal·lació de MariaDB el que serà el nostre servidor de base de dades:

-	sudo apt-get install mariadb-server mariadb-client -y
-	sudo mysql_secure_installation

# Ens demanarà que fiquem Si o No en les següents preguntes, configurarem de la següent manera:
. Des habilitar usuaris anònims
. Des habilitar accés remot com a root
. Eliminar base de dades i accés a les mateixes
. Actualitzar taula de privilegis




![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(3).png)
![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(4).png)

Reiniciem el servidor de MariaDB amb la següent comanda:
-	sudo systemctl restart mariadb.service

# El següent pas serà instal·lar la base de dades de owncloud.
El primer que tenim que fer es entrar en MariaDB i crear la base de dades, seguidament crearem un usuari amb nom ownclouduser i contrasenya Admin1234

-	sudo mysql -u root -p
-	CREATE DATABASE owncloud;
-	CREATE USER 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234';

# Després donem accés a l’usuari a la base de dades que em creat, apliquem canvis i sortim
-	FLUSH PRIVILEGEES;
-	EXIT;

# El següent pas serà instal·lar PHP i els mòduls que corresponguin, actualitzarem els paquets e instal.larem PHP, em de tenir en compte que solament funcionara PHP amb la versió 7.3 o 7.4.

-	sudo apt-get install software-properties-common -y
-	sudo add-apt-repository ppa:ondrej/php
-	sudo apt update
-	sudo apt install php7.4 libapache2-mod-php7.4 php7.4-common php7.4-mbstring php7.4-xmlrpc php7.4-soap php7.4-apcu php7.4-smbclient php7.4-ldap php7.4-redis php7.4-gd php7.4-xml php7.4-intl php7.4-json php7.4-imagick php7.4-mysql php7.4-cli php7.4-mcrypt php7.4-ldap php7.4-zip php7.4-curl -y


# Després de l’instal·lacio editarem el fitxer PHP.ini i canviarem els següents valors:
file_uploads = On allow_url_fopen = On memory_limit = 256M upload_max_filesize = 100M display_errors = Off date.timezone = Europe/Madrid
Canviant On memory_limit de 128 a 256M i upload_max_filesize de 2M a 100M ja funcionarà.
	

# El següent pas serà l’instal.lació d’Owncloud, tindrem que descarregar els següents fitxers i descomprimir-los, després a més a més mourem els fitxers a /var/www/html/owncloud:
-	cd /tmp && wget https://download.owncloud.com/server/stable/owncloud-complete-latest.zip
-	unzip owncloud-complete-latest.zip
-	sudo mv owncloud /var/www/html/owncloud/



![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(5).png)

# Per últim canviarem propietaris i permisos dels directoris de Owncloud amb les següents comandes:
-	sudo chown -R www-data:www-data /var/www/html/owncloud/
-	sudo chmod -R 755 /var/www/html/owncloud/


![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(6).png)

<img width="312" alt="instal lació ownclud activitat 2" src="https://user-images.githubusercontent.com/100061627/195670066-06c17313-d96a-4c46-9cac-3fb1f17fe232.png">

<img width="376" alt="activitat dos comandes" src="https://user-images.githubusercontent.com/100061627/195670097-a384bcd3-c96a-4a3d-aff0-2df1bd28937f.png">

<img width="413" alt="restart apache activitat 2" src="https://user-images.githubusercontent.com/100061627/195670125-9340bd1a-3eb2-471a-a69d-00885ccf701b.png">

<img width="546" alt="cambiar no domini" src="https://user-images.githubusercontent.com/100061627/195670150-f286aff0-0fea-4041-958b-884a00ed80ec.png">

<img width="644" alt="activitat dos modificar ip" src="https://user-images.githubusercontent.com/100061627/195670184-5a2257f7-bd36-4ac1-b745-b4d84925a34c.png">


# Què signifiquen a Apache les línies de configuració del fitxer owncloud.conf.
-     L'encarregat d'administrar el host
-     Serveix per configurar el funcionament d'apache
-     És el nom del servidor
-     És un host alternatiu per a coincidir amb altres host virtuals
-     Options +FollowSymlinks serveix per a seguir enllaços simbòlics d’un directori.
-     AllowOverride All controla quines directives es poden situa als fitxers de .htaccess
-     Require all grandted és una directiva de controls d’acces
-     Dav off això deshabilita el proveïdor d’arxius DAV
-     SetEnv HOME variable de l’entorn local
-     SetEnv  HTTP_HOME variable de l’entorn WEB
-     Eina per corregir erros
-     És l'arxiu físic on es registren les peticions, per defecte l'arxiu està al directori apache
-     A2ensite proporciona una llista d’arxius que es poden habilitar 
-     A2dissite proporciona una llista d’arxius que es poden des-habilitar
-     127.0.0.1 owncloud.XYZ.com, el primer significa que el host esta allotjat a la IP per defecte de la maquina, XYZ son les nostres inicials.



