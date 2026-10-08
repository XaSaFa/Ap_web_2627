# Cryptpad

<img width="455" height="490" alt="image" src="https://github.com/user-attachments/assets/632e1fe3-4c58-4ae5-9d05-b7cdffceded0" />

CryptPad és una suite de col·laboració encriptada i de codi obert d'extrem a extrem.

<img width="688" height="548" alt="image" src="https://github.com/user-attachments/assets/82fde546-0682-4337-a267-9b2075e9a14b" />

Web del projecte: [https://cryptpad.org/](https://cryptpad.org/)

## Instal·lació

- Actualitzem els repositoris

```
sudo apt update
```

- Creem la carpeta de Cryptpad
- Accedim a dins de la carpeta
- Editem el fitxer del docker
  
```
mkdir cryptpad
cd cryptpad
nano docker-compose.yml
```

- Afegim el text
```
services:
  cryptpad:
    image: cryptpad/cryptpad:latest
    container_name: cryptpad
    hostname: cryptpad
    restart: unless-stopped
    ports:
      - "3000:3000"
    environment:
      - CPAD_MAIN_DOMAIN=http://localhost:3000
      - CPAD_SANDBOX_DOMAIN=http://127.0.0.1:3000
      - CPAD_CONF=/cryptpad/config/config.js
    volumes:
      - ./data/blob:/cryptpad/blob
      - ./data/block:/cryptpad/block
      - ./data/data:/cryptpad/data
      - ./data/files:/cryptpad/datastore
      - ./customize:/cryptpad/customize
      - ./onlyoffice-dist:/cryptpad/www/common/onlyoffice/dist
      - ./onlyoffice-conf:/cryptpad/onlyoffice-conf
```

- Executem el docker.

```
sudo snap install docker
sudo docker compose up -d
```

- Modifiquem permissos

```
cd ..
sudo chmod 777 -R cryptpad/
cd cryptpad
sudo docker compose up -d
```


- Anem al navegador i obrim http://localhost:3000

<img width="1874" height="1086" alt="image" src="https://github.com/user-attachments/assets/af627680-a628-406a-b372-7ca8fc7d97a7" />




