# Connectar dues Màquines Virtuals a Isard

Per poder connectar dues Màquines de dos alumnes diferents a ISARD hem de fer que estiguin dins la mateixa xarxa.

## Alumnes del grup A:

<img width="374" height="89" alt="image" src="https://github.com/user-attachments/assets/d61c4521-a12f-4dbe-bf92-849c5a9e8c6b" />

## Alumnes del grup B:

<img width="374" height="89" alt="image" src="https://github.com/user-attachments/assets/a362822e-9c58-4316-8a0a-90a798231cd6" />

## Configurar IP

- Començant a comptar des de la porta cada alumne tindrà la IP: **192.168.1.X** 
- L'alumne de la porta té el número 10, el següent el 20, fins al final de la classe.

Anem a la configuració de xarxes:

<img width="276" height="302" alt="image" src="https://github.com/user-attachments/assets/bf6d3e63-8374-4091-9cb1-74e539a88d57" />

Escollim editar connexions de xarxa i hem de configurar la segona connexió que és la que tenim en comú amb els companys.

<img width="583" height="431" alt="image" src="https://github.com/user-attachments/assets/521e1da3-a91b-4730-98a2-db3030560df3" />

Escollim IPv4, possem "MANUAL"

<img width="810" height="540" alt="image" src="https://github.com/user-attachments/assets/0b95bbef-9418-431a-8ed6-ef36f851fe71" />

Fiquem la nostra IP, 24 com a màscara de xarxa i 192.168.1.1 com a gateway.

<img width="810" height="540" alt="image" src="https://github.com/user-attachments/assets/4ba94576-ece7-4813-9532-eedd3169be80" />

Si intenteu accedir a Owncloud d'un company ho heu de fer ficant al navegador: 

ip-host-company/owncloud

Si surt això:

<img width="1212" height="634" alt="image" src="https://github.com/user-attachments/assets/b07136c3-bdbd-48af-9ac2-b2d5a819cec6" />

És perquè el company no ha configurat TRUSTED DOMAINS a la configuració d'owncloud. Normalment estarà a: /var/www/html/owncloud/config/config.php

<img width="858" height="301" alt="image" src="https://github.com/user-attachments/assets/be128873-94c0-4f3d-a657-eadaff3b7fce" />

Després reiniciem el servidor Apache i provem una altra vegada des de l'altra màquina:

<img width="1063" height="650" alt="image" src="https://github.com/user-attachments/assets/db9214b4-37f6-43b0-8b72-a040b838935d" />

