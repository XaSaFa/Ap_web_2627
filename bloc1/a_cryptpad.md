# Activitat Cryptpad.

## Part 1 – Treball individual (4 punts)

Cada alumne treballa a la seva pròpia MV i al seu propi servidor CryptPad. Anota les respostes i captures en un document **Text enriquit** de CryptPad anomenat `Informe_CognomNom` (el crearàs a l'exercici 1.3).

### 1.0 Arrencada i comprovació de xarxa (0,5 punts)

1. Engega la MV i comprova que el servei CryptPad està actiu.
2. Esbrina l'adreça IP de la teva MV (`ip a`) i apunta-la a la pissarra o al full de la classe.
3. Fes `ping` a la MV de dos companys.
4. Obre el navegador a `http://<la_teva_IP>:3000` i comprova que carrega la pàgina d'inici de CryptPad.

**Pregunta:** per què és important que CryptPad sigui accessible per IP i no només per `localhost` si volem treballar en grup?

### 1.1 Primer contacte sense compte (0,5 punts)

1. Sense registrar-te, crea un document de text i escriu-hi una frase.
2. Observa l'adreça (URL) del document. Copia-la a l'informe i marca la part que va després del símbol `#`.

**Preguntes:**

- Què creus que conté la part de l'URL que va després de `#`?
- Per què el navegador no envia mai aquesta part al servidor? Quina conseqüència té per a la privadesa?
- Què passa amb aquest document si tanques el navegador i esborres les dades? (pista: no tens compte)

### 1.2 Registre i CryptDrive (0,5 punts)

1. Registra un compte amb l'usuari `nom.cognom` i una contrasenya robusta. Llegeix l'avís que mostra CryptPad sobre la contrasenya.
2. Explora el CryptDrive: crea les carpetes `Personal` i `Classe`.
3. Configura el perfil: nom visible i avatar.

**Preguntes:**

- Pot l'administrador del servidor recuperar la teva contrasenya si l'oblides? Per què?
- Quina diferència hi ha entre la contrasenya d'un compte de CryptPad i la d'un servei com Google Drive?

### 1.3 Tipus de documents (1,5 punts)

A la carpeta `Personal`, crea un document de cada tipus i fes-hi una tasca mínima:

| Aplicació | Tasca |
| --- | --- |
| Text enriquit | El teu `Informe_CognomNom` (aquí respondràs totes les preguntes) |
| Full de càlcul | Taula amb 5 components d'un PC, preu i una fórmula de total amb IVA |
| Codi | Un script bash curt que mostri la IP i el nom de la màquina |
| Kanban | Tauler amb les columnes Pendent / En curs / Fet i 3 targetes |
| Pissarra | Esquema de la xarxa de la classe (MV i IP) |
| Formulari | Enquesta de 3 preguntes sobre programari lliure |

**Pregunta:** quines aplicacions de CryptPad substituirien Word, Excel, Trello i Google Forms?

### 1.4 Seguretat i compartició (1 punt)

1. Obre el full de càlcul i fes clic a **Compartir**. Genera un enllaç **només de lectura** i un d'**edició**. Copia'ls a l'informe i compara'ls.
2. Crea un document nou a la carpeta `Classe` protegit amb **contrasenya**.
3. Crea un document amb **data de caducitat** (per exemple, 1 hora) o **autodestructiu**.
4. Obre l'**historial** del teu informe i recupera una versió anterior.
5. Obre la **configuració** del compte i revisa les opcions de seguretat (sessions obertes, tancar sessió a tot arreu).

**Preguntes:**

- En què es diferencien l'enllaç de lectura i el d'edició? Què passaria si comparteixes per error l'enllaç d'edició en un xat públic?
- En quins casos reals faries servir un document amb contrasenya o amb caducitat?
- Qui és el **propietari** d'un document i quins drets especials té?

## Part 2 – Treball en grup (6 punts)

**Situació:** el vostre grup és una petita empresa de suport informàtic que vol deixar Google Drive i fer servir un servidor CryptPad propi per organitzar un encàrrec real: el muntatge d'una aula de 10 ordinadors per a una escola.

### 2.1 Organització del grup (0,5 punts)

Feu grups de 3 o 4 persones i repartiu aquests rols:

| Rol | Responsabilitat |
| --- | --- |
| Administrador/a | Posa el servidor (la seva MV), crea l'equip i gestiona permisos |
| Coordinador/a | Porta el Kanban i controla el temps |
| Responsable de pressupost | Lidera el full de càlcul |
| Responsable de documentació | Lidera el document final i el formulari (si sou 3, l'assumeix el coordinador/a) |

Tots els membres del grup es connecten des de la seva MV a `http://<IP_administrador>:3000` i es registren en **aquell** servidor.

**Pregunta:** els comptes que vau crear a la Part 1 funcionen al servidor del company? Per què?

### 2.2 Equip i contactes (1 punt)

1. Cada membre comparteix el seu enllaç de **contacte** (perfil) amb l'administrador/a, que els afegeix com a contactes.
2. L'administrador/a crea un **Equip** anomenat `Grup_X_Empresa` i hi convida tothom.
3. Assigneu els rols de l'equip: almenys un altre **administrador** i la resta **membres**. Proveu què pot fer i què no pot fer cada rol.
4. Al drive de l'equip creeu les carpetes `Projecte`, `Pressupost` i `Lliurament`.

### 2.3 Treball col·laboratiu en temps real (3,5 punts)

Treballeu **simultàniament** des de MV diferents:

- **Kanban** `Planificació`: totes les tasques del projecte, amb responsable assignat i columnes Pendent / En curs / Revisió / Fet.
- **Full de càlcul** `Pressupost_Aula`: 10 equips + perifèrics + switch + cablejat, amb preus, IVA (21 %) i total. Cada membre omple una part a la vegada.
- **Pissarra o diagrama** `Esquema_Xarxa`: topologia de l'aula amb un pla d'adreçament IP.
- **Formulari** `Enquesta_Escola`: 5 preguntes per saber les necessitats del client. Respondre-lo des de les altres MV i consultar els resultats.
- **Text enriquit** `Proposta_Client`: document final que resumeixi el projecte i enllaci els altres documents.

Mentre treballeu, observeu els cursors dels companys, feu servir el **xat** integrat del document i deixeu almenys dos **comentaris** a la proposta.

### 2.4 Lliurament segur al client (1 punt)

1. Compartiu la `Proposta_Client` amb el professor/a amb un enllaç **només de lectura** i **protegit amb contrasenya**.
2. Envieu l'enllaç i la contrasenya **per canals diferents** (per exemple, l'enllaç per xat de CryptPad i la contrasenya de paraula).
3. Expliqueu en una frase, al final de la `Proposta_Client`, per què ho heu fet així.

## Lliurables i avaluació

La nota final és sobre 10 punts: 4 de la part individual i 6 del treball en grup.

**Lliurables**

pdf amb l'enunciat copiat i captures de pantalla demostrant que has fet la feina que es demana. NO OBLIDIS LA PORTADA!
