# Activitat 4:

## Gestió d'usuaris:

Hi ha dos tipus d'usuaris, els admins amb permissos per gestionar Owncloud i els usuaris normals.

On fica resposta afegeix una captura de pantalla on es vegi que has fet l'acció que es demana.

**Aquesta part de la pràctica la feu amb un company/a, li creeu un usuari i li doneu el vostre nom de domini d'Owncloud.**

Per a que pugui accedir necessitarà:

- La MV amb owncloud ha d'estar en mode "adaptador pont".
- El fitxer /etc/hosts del company ha de tenir la IP de la MV i el nom de domini de la MV del company/a.


**4.1.-** Crea un usuari admin que es digui adminXYZ, on XYZ són les inicials del teu nom:

**RESPOSTA**
<img width="225" alt="image" src="https://user-images.githubusercontent.com/100061627/196966854-41611a21-3707-4c0e-bace-8527e3f2a421.png">


**4.2.-** Inicia sessió com a l'usuari adminXYZ.

**RESPOSTA**
<img width="266" alt="image" src="https://user-images.githubusercontent.com/100061627/196966987-e268e97d-119a-4f58-a8fc-196ab785da4c.png">


**4.3.-** Crea un usuari XYZ on XYZ son les inicials del company/a i afegeix-lo al grup usuaris, aquest usuari tindrà una quota de 512 MB.

**RESPOSTA**
<img width="783" alt="image" src="https://user-images.githubusercontent.com/100061627/196967749-6d968133-8187-4109-8e55-1376c90718f7.png">


**4.4.-** Podem crear fitxers d'una mida determinada a Linux amb la comanda:

```
truncate -s 10M file.txt
```

A l'exemple es crea un fitxer de 10MB.

Crea 6 fitxers de 100MB i pujal's a Owncloud un per un.

**RESPOSTA**

<img width="371" alt="image" src="https://user-images.githubusercontent.com/100061627/196968649-fd9bdd70-4489-449d-91b3-365bcc6be937.png">

**4.5.-** Mostra el missatge d'error per haver superat la quota d'usuari.

**RESPOSTA**
<img width="394" alt="image" src="https://user-images.githubusercontent.com/100061627/196969175-0325f698-218f-4675-83ed-9fc6c90ec3a0.png">

**4.6.-** Busca al teu perfil quin percentatge de quota estas utilitzant.

**RESPOSTA**
<img width="182" alt="image" src="https://user-images.githubusercontent.com/100061627/196969521-449db444-ec7b-47b0-9a23-f9da91147cac.png">


**4.7.-** Canvia la quota de l'usuari a 1GB i mostra tots els fitxers pujats.

**RESPOSTA**
<img width="792" alt="image" src="https://user-images.githubusercontent.com/100061627/196970896-0e263d04-2a2f-4f7c-b29f-7dea158e2528.png">


**4.8.-** Crea un usuari anomenat usuari2XYZ i fical al grup usuaris.

**RESPOSTA**
<img width="428" alt="image" src="https://user-images.githubusercontent.com/100061627/196974164-4dd8b6b4-4a0d-40b9-a241-c6b8bfec1f4b.png">



**4.9.-** Comparteix un fitxer de usuariXYZ a usuari2XYZ i mostra com l'usuari2XYZ pot veure i descarregar el fitxer.

**RESPOSTA**
<img width="262" alt="image" src="https://user-images.githubusercontent.com/100061627/196975490-bc6b3f3e-8bdf-4ea3-8cd0-05ba65942726.png">
<img width="931" alt="image" src="https://user-images.githubusercontent.com/100061627/196975680-a5dbac34-d16a-4892-8153-b412f91c223b.png">


**4.10.-** Esborra la carpeta Learn more about owncloud.

**RESPOSTA**
<img width="416" alt="image" src="https://user-images.githubusercontent.com/100061627/196975893-64493d38-ab98-4286-98c4-930833d7a9f9.png">


**4.11.-** Recupera la carpeta Learn more about owncloud.

**RESPOSTA**
<img width="925" alt="image" src="https://user-images.githubusercontent.com/100061627/196976089-397b4932-9ca7-4a3e-bd2e-1284885f2781.png">


**4.12.-** Com a usuariXYZ crea una carpeta nova anomenada shared i comparteix-la amb l'usuari usuari2XYZ.

**RESPOSTA**
<img width="311" alt="image" src="https://user-images.githubusercontent.com/100061627/196976741-c59f31e7-de6e-4bd6-b6df-aeab7dcf6d51.png">
<img width="302" alt="image" src="https://user-images.githubusercontent.com/100061627/196977036-0a87ea62-4ae8-4b82-944b-671f25dd0416.png">


**4.13.-** Entra a Market instal·la dues aplicacions que no estiguin ja instal·lades i explica què fan i com funcionen.

![image](https://user-images.githubusercontent.com/110727546/196159706-705ff624-c409-4632-acb4-f43ffcc486d4.png)

**RESPOSTA PRIMERA APP**
<img width="568" alt="image" src="https://user-images.githubusercontent.com/100061627/196978734-69865f19-2acd-48c0-8845-c6b442e37e78.png">
<img width="677" alt="image" src="https://user-images.githubusercontent.com/100061627/196979164-10a84345-56cc-4b63-a650-417ce12bf14c.png">
És tracta d’un calendari per poder apuntar tasques o semblants, dies importants o notificacions. 

**RESPOSTA SEGONA APP**
<img width="501" alt="image" src="https://user-images.githubusercontent.com/100061627/196981616-c0c8877d-7400-4a7d-8f1d-733e8d08f494.png">
<img width="668" alt="image" src="https://user-images.githubusercontent.com/100061627/196981726-9fc71a9e-3328-46a9-a70b-8b001566ee1d.png">


És tracta d’un gestor de fitxers multimèdia, en ell podem organitzar, crear carpetes, pujar fotos i vídeos, també té suport per al mòbil.

**4.14.-** Crearem una carpeta nova per emmagatzematge a Owncloud, la carpeta serà /media/publicXYZ on XYZ són les teves inicials i apareixerà amb el nom de public als usuaris.

Aquesta carpeta haurà de pertànyer a l'usuari www-data.

**RESPOSTA**

**4.15.-** Connectarem la carpeta publicXYZ com emmagatzematge local, tal i com s'indica [aquí](https://doc.owncloud.com/server/next/admin_manual/configuration/files/external_storage/local.html). Tots els usuaris tindran accés a la carpeta.

**RESPOSTA**
<img width="923" alt="image" src="https://user-images.githubusercontent.com/100061627/196982415-bafd9070-69fd-42c1-863b-48df0b315f78.png">


**4.16.-** Un usuari normal pujarà un fitxer a la carpeta public.

**RESPOSTA**
<img width="925" alt="image" src="https://user-images.githubusercontent.com/100061627/196982739-edb7ceea-b189-46bf-895d-ed290ec3a867.png">


**OPCIONAL.-** Aquesta tasca és opcional.

Intenta connectar com a emmagatzematge extern el teu compte de Google Drive de l'Institut. Tens com fer-ho [aquí](https://doc.owncloud.com/server/next/admin_manual/configuration/files/external_storage/google.html).

**RESPOSTA**
