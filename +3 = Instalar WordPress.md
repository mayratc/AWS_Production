# ⚙️⚙️⚙️⚙️WordPress⚙️⚙️⚙️⚙️

## Descripción rápida 🚀:

Wordpress plataforma para crear Blog y website.



## Ques es WordPress?

.....

## Beneficios:

+ Nos permite desarrollar proyecto mas rapido.

+

## Pasos para la instalacion:

#### Configuracion Firewall

- sudo ufw status
- sudo ufw allow 22 // puerto del putty
- sudo ufw allow 21 // Puerto de FTP
- sudo ufw enable // Habilitamos el corta fuego.
- sudo apt-get install git

### instalar WordPress con LAMP en Ubuntu

#### Instalar Apache
- sudo apt-get update
- sudo apt-get install apache2
- sudo apache2ctl configtest
- sudo nano /etc/apache2/apache2.conf // Agregamos ServerName server_domain_or_IP
- sudo apache2ctl configtest
- sudo systemctl restart apache2
- sudo ufw allow in "Apache Full" // Habilitamos para que cualquier usuario pueda verlo desde la IP publica

#### Instalar MySQL
- sudo apt update
- sudo apt install mysql-server
- sudo mysql_secure_installation // low 1 / new psw / remove user: n / privilegio y

#### Instalar PHP
- sudo apt-get install php libapache2-mod-php php-mcrypt php-mysql

// Problemas con php-mcrypt

- sudo apt-get -y install gcc make autoconf libc-dev pkg-config
- sudo apt-get -y install php7.2-dev
- sudo apt-get -y install libmcrypt-dev

- sudo pecl install mcrypt-1.0.1
- sudo nano /etc/apache2/mods-enabled/dir.conf // configuramos  los archivos de lectura index php es primero
- sudo nano /var/www/html/index.php // creamos el archivo php para probar si esta funcinando php.
- sudo systemctl restart apache2

#### Crear proyecto wordpress

- mysql -u root -p // entramos a la BD MYSQL
- CREATE DATABASE wordpress_labcode DEFAULT CHARACTER SET utf8 COLLATE utf8_unicode_ci; // Editable
- GRANT ALL ON wordpress_labcode.* TO 'labcode'@'localhost' IDENTIFIED BY '**********'; // Editable conexion remota
- FLUSH PRIVILEGES;
- EXIT;

// Instalar Extensiones Adicionales para PHP
- sudo apt-get update
- sudo apt-get install php-curl php-gd php-mbstring php-xml php-xmlrpc
- sudo systemctl restart apache2
- sudo nano /etc/apache2/apache2.conf // Habilitamos AllowOverride All
- sudo a2enmod rewrite // habilitamos el modulo de escritura.
- sudo apache2ctl configtest
- sudo systemctl restart apache2

#### Clonar Wordpress
- cd /tmp
- curl -O https://wordpress.org/latest.tar.gz
- tar xzvf latest.tar.gz
- touch /tmp/wordpress/.htaccess
- chmod 660 /tmp/wordpress/.htaccess
- cp /tmp/wordpress/wp-config-sample.php /tmp/wordpress/wp-config.php
- mkdir /tmp/wordpress/wp-content/upgrade
- sudo cp -a /tmp/wordpress/. /var/www/html/labcode // editable
- sudo chown -R root:www-data /var/www/html
- sudo find /var/www/html -type d -exec chmod g+s {} \;
- sudo chmod g+w /var/www/html/labcode/wp-content // modificar
- sudo chmod -R g+w /var/www/html/labcode/wp-content/themes // modificar
- sudo chmod -R g+w /var/www/html/labcode/wp-content/plugins // modificar
- curl -s https://api.wordpress.org/secret-key/1.1/salt/

define('AUTH_KEY',         'juT<S#_FKlikn3+*%:6A1]|=W`,Jq@zNqL+QD,1,^+p(SFm>5P5<ZA8NlN|0-fl>');
define('SECURE_AUTH_KEY',  'm?_2-0F C9:cJ#s^UM}m97G -(#b8-6XXB~Sp8=j)iyD>|S q`a~S{yt-wZp5H6w');
define('LOGGED_IN_KEY',    'JX-SUH,r2%&4uv?2{}Hqz.BouDqaT/TRBiHol23K+B%i`:lR&D%(^&hZ2D]1E)#g');
define('NONCE_KEY',        '>oj#7gP8`:?R,EQe!UcHte.ZG<]?p6~!o%P|c=%BIKVHM.//,^|Rtt[6xGzs:.2>');
define('AUTH_SALT',        '|Z*IVN|T/elI^z^UV]dms6!xs=TkcXl1Eu*YWQSUb3ho,c,1K/ ?Sl9DEv{%~-vH');
define('SECURE_AUTH_SALT', '$3r$Q7x]CElK;jC` {*ca[t/wqYd-&p!XWnQU%[W|:OPK@&[FsTZ5UE`n32UTM:_');
define('LOGGED_IN_SALT',   'x`Cb89?#M_J~-ayXwI5Q/m[o[_n`E)2=BqQ7uGn8xT>9*)`X)e+/qH@.sX+nz15D');
define('NONCE_SALT',       '-`^1z?k8Hbu.&AK342HQy5E=/uQcoib+s43hy]-7J<9G}#.Hq..WZqKm%Y~8{w7*');

- nano /var/www/html/wp-config.php // Lo pegamos en esta carpeta

// ademas modificamos lo siguiente 

define('DB_NAME', 'wordpress');

/** MySQL database username */
define('DB_USER', 'wordpressuser');

/** MySQL database password */
define('DB_PASSWORD', 'password');

/** Agregamos la siguiente linea */
define('FS_METHOD', 'direct');









## LINK: 

```
https://www.digitalocean.com/community/tutorials/como-instalar-wordpress-con-lamp-en-ubuntu-16-04-es

https://www.digitalocean.com/community/tutorials/how-to-install-mysql-on-ubuntu-18-04

https://www.digitalocean.com/community/tutorials/how-to-install-linux-apache-mysql-php-lamp-stack-on-ubuntu-16-04

https://www.digitalocean.com/community/tutorials/como-instalar-wordpress-con-lamp-en-ubuntu-16-04-es

Instalar WORDPRESS
https://www.digitalocean.com/community/tutorials/como-instalar-wordpress-con-lamp-en-ubuntu-16-04-es

https://dcblog.dev/setup-digital-ocean-part-2-upgrade-php-to-73

```
