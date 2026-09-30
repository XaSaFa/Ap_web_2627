# Etherpad

<img width="600" src="https://github.com/user-attachments/assets/8ef6a2cf-57ee-4a49-894e-b84626d80547" />

Etherpad és un editor col·laboratiu en temps real de codi obert i basat en web, que permet als autors editar simultàniament un document de text i veure totes les edicions dels participants en temps real.

La web del projecte és [etherpad.org](https://etherpad.org/).

## Introducció

Etherpad va ser dissenyat per col·laborar ràpidament en un text públic, prenent notes de reunions o classes en línia de manera col·laborativa i en temps real. És fàcil d’utilitzar per a classes en línia o presencials, i posa a tothom literalment “a la mateixa pàgina”.

EtherPad ofereix moltes de les mateixes funcions que Google Docs, però no és adequat per a informació sensible, ja que té funcions limitades de protecció de contrasenya i control d’accés.

Tanmateix, és una veritable eina de col·laboració en temps real que pot implicar visualment els estudiants en classes en línia i presencials.

## Instal·lació a Ubuntu

1. Primer actualitzem els repositoris de software:

```
sudo apt update
```

2. Instal·lem git:

```
sudo apt install git
```

3. Clonem el repositori de git del projecte etherpad al nostre ordinador:

```
mkdir etherpad
cd etherpad
sudo nano docker-compose.yml
```

4. Afegim al document aquestes línies:

```
version: '3.8'

services:
  etherpad:
    image: etherpad/etherpad
    container_name: etherpad
    restart: always
    ports:
      - "8084:9001"
    environment:
      TITLE: "Etherpad for Collaboration"
      ADMIN_PASSWORD: "adminpassword" # Адміністративний пароль
      DB_TYPE: "dirty" # Простий режим збереження (без бази даних)
    volumes:
      - ./.app/etherpad-data:/var/lib/etherpad

```
Guardem el document amb Control+s i sortim amb Control+X

En aquesta carpeta hi ha un fitxer amb el nom docker-compose.yml .

<img width="319" height="51" alt="image" src="https://github.com/user-attachments/assets/4d03f870-8f5b-4216-9ecf-1e9a6b9aa93c" />

5. Instal·lem docker:

```
sudo snap install docker
```

6. Arranquem el servei etherpad:

```
sudo docker compose up -d
```

S'anirà carregant el docker:

<img width="653" height="386" alt="image" src="https://github.com/user-attachments/assets/e1a0672b-1888-4fb6-8bdf-f99ce5f2e626" />

<img width="653" height="103" alt="image" src="https://github.com/user-attachments/assets/2765d093-f9be-4d10-b544-e0eeee028740" />

7. Obrim el navegador a l’adreça http://localhost:8084 per connectar-nos a Etherpad:

<img width="850" height="873" alt="image" src="https://github.com/user-attachments/assets/a24462df-dc36-4ba2-afb9-2420903060dd" />

8. Podem crear un nou PAD amb un nom aleatori o assignar-li un nom:

<img width="859" height="873" alt="image" src="https://github.com/user-attachments/assets/173c9bdf-cd2b-4204-8e9a-7de2d673168f" />
 


