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
# SPDX-FileCopyrightText: 2023 XWiki CryptPad Team <contact@cryptpad.org> and contributors
#
# SPDX-License-Identifier: AGPL-3.0-or-later

---
services:
  cryptpad:
    image: "cryptpad/cryptpad:latest"
    hostname: cryptpad

    environment:
      - CPAD_MAIN_DOMAIN=https://your-main-domain.com
      - CPAD_SANDBOX_DOMAIN=https://your-sandbox-domain.com
      - CPAD_CONF=/cryptpad/config/config.js

      # Read and accept the license before uncommenting the following line:
      # https://github.com/ONLYOFFICE/web-apps/blob/master/LICENSE.txt
      # - CPAD_INSTALL_ONLYOFFICE=yes

    volumes:
      - ./data/blob:/cryptpad/blob
      - ./data/block:/cryptpad/block
      - ./customize:/cryptpad/customize
      - ./data/data:/cryptpad/data
      - ./data/files:/cryptpad/datastore
      - ./onlyoffice-dist:/cryptpad/www/common/onlyoffice/dist
      - ./onlyoffice-conf:/cryptpad/onlyoffice-conf

    ports:
      - "3000:3000"
      - "3003:3003"

    ulimits:
      nofile:
        soft: 1000000
        hard: 1000000
```

Executem el docker.

```
sudo snap install docker
docker compose up -d
```

Anem al navegador i obrim http://localhost:3000

<img width="1874" height="1086" alt="image" src="https://github.com/user-attachments/assets/af627680-a628-406a-b372-7ca8fc7d97a7" />




