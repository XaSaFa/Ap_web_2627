# Instal·lació owncloud

## Instal·lació Apache

```
sudo apt update
sudo apt install apache2
```

## Instal·lació MariaDB

```
sudo apt install mariadb-server
sudo service mariadb restart
```

## Crear BBDD

```
sudo mariadb
```

```
CREATE DATABASE owncloud;
CREATE USER 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234';
GRANT ALL ON owncloud.* TO 'ownclouduser'@'localhost' IDENTIFIED BY 'Admin1234' WITH GRANT OPTION;
FLUSH PRIVILEGES;
EXIT;
```

## Instal·lar PHP 8.3

```
sudo add-apt-repository ppa:ondrej/php
sudo apt update
sudo apt install php8.3 php8.3-cli php8.3-{bz2,curl,mbstring,intl}
sudo apt install php8.3-fpm
sudo a2enconf php8.3-fpm
sudo service apache2 restart
```

## Instal·lar Owncloud

```
wget https://github.com/owncloud/core/releases/download/v11.0.1/owncloud-complete-20260925.zip
unzip owncloud-complete-20260925.zip
sudo mv owncloud /var/www/html/
```
## Canviar els permisos del directori d'Owncloud

```
sudo chown -R www-data:www-data /var/www/html/owncloud/
sudo chmod -R 755 /var/www/html/owncloud/
```

### Reiniciem Apache

```
sudo service apache2 restart
```

## Per accedir a Owncloud

Des d'un navegador de la Màquiva Virtual escrivim: **localhost/owncloud**

**Us faltaran mòduls de PHP** s'instal·len amb la comanda:

<img width="504" height="723" alt="imatge" src="https://github.com/user-attachments/assets/97d3e0db-fd23-4d30-ae94-a3688cfa9c27" />

```
sudo apt install php8.3-nomdelmòdul
```

Per exemple si falta el mòdul zip hem de ficar al terminal:

```
sudo apt install php8.3-zip
sudo service apache2 restart
```
<img width="860" height="121" alt="imatge" src="https://github.com/user-attachments/assets/9f456824-6ec1-4509-8130-ddc34b83be8d" />


**Reiniciem el servidor Apache cada vegada que instal·lem un mòdul nou.**

## Configuració de Owncloud

### Heu de crear un compte administrador (important: enrecordeu-vos del nom d'usuari i password).

<img width="365" height="507" alt="imatge" src="https://github.com/user-attachments/assets/d4529ff2-f1be-402b-aa11-e590cc1fd145" />

### Ompliu la informació de la base de dades

<img width="358" height="695" alt="imatge" src="https://github.com/user-attachments/assets/e3eb37f5-1602-4929-ab08-beade1578341" />

### Ja està

Heu d'entrar amb l'usuari administrador que heu creat

<img width="424" height="440" alt="imatge" src="https://github.com/user-attachments/assets/e79490fc-c42e-4ee2-ad64-cadf1cb98df5" />

<img width="1590" height="749" alt="imatge" src="https://github.com/user-attachments/assets/21a9cd51-981c-4397-a829-f69df2ac4d96" />

## Accedir a owncloud des d'un altre ordinador:

Heu d'editar el fitxer config.php

```
sudo gedit /var/www/html/owncloud/config/config.php
```

<img width="1165" height="662" alt="image" src="https://github.com/user-attachments/assets/0e1219f8-c235-4e31-ade4-97a490bb958d" />


