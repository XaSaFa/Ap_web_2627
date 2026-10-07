# Cryptpad

<img width="455" height="490" alt="image" src="https://github.com/user-attachments/assets/632e1fe3-4c58-4ae5-9d05-b7cdffceded0" />

CryptPad és una suite de col·laboració encriptada i de codi obert d'extrem a extrem.

<img width="688" height="548" alt="image" src="https://github.com/user-attachments/assets/82fde546-0682-4337-a267-9b2075e9a14b" />

Web del projecte: [https://cryptpad.org/](https://cryptpad.org/)

## Instal·lació

Clonem el projecte.

```
sudo apt update
```

Fem el fitxer del docker.
```
mkdir cryptpad
cd cryptpad
sudo nano docker-compose.yml
```

Afegim el text.
```
---
version: "2.1"
services:
  installer:
    image: nicholaswilde/cryptpad
    container_name: cryptpad
    ports:
      - 3000:3000
    restart: unless-stopped
    environment:
      - TZ=America/Los_Angeles  # optional
      - PUID=1000               # optional
      - PGID=1000               # optional
    volumes:
      - blob:/blob
      - block:/block
      - customize:/customize
      - config:/config
      - data:/data
      - datastore:/datastore
volumes:
  blob:
  block:
  customize:
  config:
  data:
  datastore:
```

Executem el docker.

```
sudo snap install docker
docker compose up -d
```

Anem al navegador i obrim http://localhost:3000

<img width="1874" height="1086" alt="image" src="https://github.com/user-attachments/assets/af627680-a628-406a-b372-7ca8fc7d97a7" />




