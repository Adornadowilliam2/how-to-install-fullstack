
# How to install vscode in Linux


- update the system
```php
sudo apt update
```
- install the curl for miscrosoft something
```php
sudo apt install software-properties-common apt-transport-https curl
```
- use the curl for install microsoft keys
```php
curl https://packages.microsoft.com/keys/microsoft.asc | sudo gpg --dearmor -o /usr/share/keyrings/microsoft-archive-keyring.gpg
```
- add vscode to the repo
```php
sudo sh -c 'echo "deb [arch=amd64 signed-by=/usr/share/keyrings/microsoft-archive-keyring.gpg] https://packages.microsoft.com/repos/vscode stable main" > /etc/apt/sources.list.d/vscode.list'

```
- update the system again
```php
sudo apt update
```

- install now the vscode
```php
sudo apt install code
```



## Install Node Js


- first you need to install first the nvm

```php

sudo apt update 
```

- for using the repo in curl

```php

curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash

```


- for taggin the bashrc

```php

source ~/.bashrc
 
```
- check if the nvm it works

```php

nvm --version

```
- then install node

```php

nvm install 22
```
- once it success it works now! Congratulations!

## How to install xampp in Linux

- first you need to update the system
```php

sudo apt update

```
- installing the apache2
```php
sudo apt install apache2
```

- installing the mysql and mariadb

```php

sudo apt install mysql-server
sudo apt install mariadb-server
```
- enable the apache2, mysql and mariadb
```php
sudo systemctl start apache2
sudo systemctl enable apache2

sudo systemctl start mysql     # For MySQL
sudo systemctl enable mysql    # For MySQL


sudo systemctl start mariadb   # For MariaDB
sudo systemctl enable mariadb  # For MariaDB

```


- for installing the php
```php

sudo apt install php libapache2-mod-php php-mysql

``` 

- adding security in mysql

```php
sudo mysql_secure_installation  # For MySQL
sudo mysql_secure_installation  # For MariaDB

```

- then restart again to check if work
```php

sudo systemctl restart apache2

```

- now add the phpadmin 
```php

sudo apt install phpmyadmin
```

- for creating symbolic link to the phpmyadmin
```php
sudo ln -s /usr/share/phpmyadmin /var/www/html/phpmyadmin
```


## Install the composer in Linux

- for you need to update the system

```php

sudo apt update
```

- then install the curl and php-cli

```php
sudo apt install curl php-cli php-mbstring git unzip

```

- then run this command for composer 

```php
curl -sS https://getcomposer.org/installer | php


```

- then move it to global website

```php

sudo mv composer.phar /usr/local/bin/composer

```

- then to check if it install the composer type this command

```php

composer --version

```

## For checking if the php --ini no uncomment

- type this command first

```php

php --ini
```

- then type this command if it work

```php
sudo nano /etc/php/7.x/apache2/php.ini    # Apache
sudo nano /etc/php/7.x/cli/php.ini        # CLI

```

- if there is no showing type **Ctrl + Q** for quit the nano

- if there is change it the save then type this command to also save in composer

```php

sudo systemctl restart apache2
```

- if not install this the following

```php

sudo apt install php-zip
sudo apt install php-mbstring
sudo apt install php-sodium
sudo apt install php-mysqli
sudo apt install php-gd
```


## How to install git in Linux

- update the system

```php
sudo apt update
```

- install the git
```php

sudo apt install git

```


- then check if it install

```php
git --version

```

