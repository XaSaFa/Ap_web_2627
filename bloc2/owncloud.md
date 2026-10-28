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

```
sudo apt install php8.3-nomdelmòdul
```

Per exemple si falta el mòdul zip hem de ficar al terminal:

```
sudo apt install php8.3-zip
```

Reiniciem el servidor Apache cada vegada que instal·lem un mòdul nou.


## Accedir a owncloud des d'un altre ordinador:

Heu d'editar el fitxer config.php

```
sudo gedit /var/www/html/owncloud/config/config.php
```

<img width="1165" height="662" alt="image" src="https://github.com/user-attachments/assets/0e1219f8-c235-4e31-ade4-97a490bb958d" />


