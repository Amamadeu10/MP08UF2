
# Activitat 3:

Per fer aquesta activitat comptem amb que **ja s'ha configurat el servei Owncloud a una Màquina Virtual** (MV).

**3.1.-** Llista els Virtual Hosts d'Apache per tal de veure si **owncloud.XYZ.com** està habilitat amb la comanda:

```
apache2ctl -S
``` 

![image](https://github.com/Amamadeu10/MP08UF2/blob/main/Captura%20de%20pantalla%202022-10-13%20152532.png)

**RESPOSTA**

**3.2.-** A Owncloud podem veure que hi ha una serie de carpetes per defecte, mostra la ruta real a les tres carpetes dins de la teva MV.

![image](https://user-images.githubusercontent.com/110727546/194824543-c49bf482-ac93-432f-884c-d89487e587f3.png)


**RESPOSTA**

<img width="301" alt="versio" src="https://user-images.githubusercontent.com/100061627/195625112-c77434ea-d810-4461-ac51-4297777c1b13.png">


**3.3.-** Al directori **Learn more about owncloud** hi ha informació en forma de fitxers pdf. Consulta'ls i respon aquestes preguntes:

- ## Quin són els tres tipus de protecció de dades que ofereix Owncloud?
- Encryption in Transit
- 2A Encryption at Rest
- 2B Encryption at Rest with Master Key in Hardware Security Module, HSM
- End-to-End Encryption
- ## Fes una petita descripció de cada un d'ells.
- El encryption in transit es el xifratge de les dades quan estan actives,per exemple quan iniciem sessió se envia la contrasenya perquè validi un tercer.
- El Encription at Rest és un xifratge en repòs que s'utilitza per protegir copies de seguretat en discos, tant normals com de estat solid, utilitza el AES 256.
- El HSM es un dipositiu de segurtat amb encriptació, utilitza diversos nivell de seguretat del FIPS 140-2
- El End-to-End Encryption es un xifratge d'extrem a extrem, les dades es xifren al dispositiu remitent i només el destinatari pot desxifrar-les.
- ## Per quina raó ens recomana utilitzar Owncloud per als documents de Microsoft Office de la nostra empresa?  
- Degut a llei comunitaria de Europa, donat que els documents tenen que estar en base de dades física de l'emmpresa i no al nuvol.
- ## Això passa a tots els països?.
- No
- ## Quina és la llicència d'OWncloud Enterprise?
- És una llicència per empresa.
- ## I la d'Owncloud Standard?
- És una lliència per usuaris
- ## Es poden veure videos en Streaming directament des de Owncloud?
- En teoria i després del llegit si es pot, donat que pots connectar en diferents plataformes i modificar arxius i veure'ls a l'acte
- ## Es poden connectar directoris de Google Drive a Owncloud?
- Si
- ## I Dropbox?
- Si.
- <img width="520" alt="Captura de pantalla 2022-10-13 173104" src="https://user-images.githubusercontent.com/100061627/195640697-1b62cbc0-8795-4a9e-99af-53bb3737e705.png">

- ## Compta Owncloud amb antivirus? En cas afirmatiu com es diu?
- Si, és diu ClamAV 

**RESPOSTA**

**3.4.-** Mostra els següents canvis de paràmetres d'usuari:

- Posa't una imatge d'usuari.## 
- Afegeix el teu mail de l'Institut.
- Canvia l'idioma a català.
- Mostra la versió d'Owncloud instal·lada.

 **RESPOSTA## **
 
<img width="381" alt="canvi fotos email" src="https://user-images.githubusercontent.com/100061627/195624932-4210c645-6a7d-434f-b78e-2e44df998658.png">
 
<img width="301" alt="versio" src="https://user-images.githubusercontent.com/100061627/195641613-bbcf9123-8ff5-4437-bb70-63eb6e8b02fd.png">





