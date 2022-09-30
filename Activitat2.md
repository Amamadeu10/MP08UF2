# INSTAL.LACIÓ OWNCLOUD

## GUIA D'INSTAL.LACIÓ

### Requeriments:

-Linux: Ubuntu 22.04LTS
-Servidor Web Apache
-MariaDB base de dades
-PHP versió 7.3 o 7.4
El primer pas és agafar i ficar les següents comandes per a la instal·lació de Apache2:
-	sudo apt install apache2
-	sudo sed -i "s/Options Indexes FollowSymLinks/Options FollowSymLinks/" /etc/apache2/apache2.conf	

![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(1).png)

![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(2).png)

El segon pas és agafar i ficar les següents comandes per a la instal·lació de MariaDB el que serà el nostre servidor de base de dades:

-	sudo apt-get install mariadb-server mariadb-client -y
-	sudo mysql_secure_installation

Ens demanarà que fiquem Si o No en les següents preguntes, configurarem de la següent manera:
. Des habilitar usuaris anònims
. Des habilitar accés remot com a root
. Eliminar base de dades i accés a les mateixes
. Actualitzar taula de privilegis


![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(3).png)
![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(4).png)

Reiniciem el servidor de MariaDB amb la següent comanda:
-	sudo systemctl restart mariadb.service

El següent pas serà instal·lar la base de dades de owncloud.
El primer que tenim que fer es entrar en MariaDB i crear la base de dades, seguidament crearem un usuari amb nom ownclouduser i contrasenya Admin1234

-	sudo mysql -u root -p
-	CREATE DATABASE owncloud;
-	CREATE USER 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234';

![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(5).png)
![Es una imatge](Documentar%20owncloud%20ubuntu%20UF02/1%20(6).png)
