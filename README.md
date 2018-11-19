## Add color to LS

> vi ~/.bash_profile
  ```# Tell ls to be colourful
  export CLICOLOR=1
  export LSCOLORS=Exfxcxdxbxegedabagacad
 
  # Tell grep to highlight matches
  export GREP_OPTIONS='--color=auto'
  ```

> source ~/.bash_profile

## Install Homebrew

> /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

## Install Composer using cURL

> curl -sS https://getcomposer.org/installer | php

## Make Composer globally accessible

> mv composer.phar /usr/local/bin/composer

## Install Gitflow
> brew install git-flow-avh

## Turn on Apache

> sudo apachectl status
> sudo apachectl start

## Run configuration file syntax test

> sudo apachectl configtest

## Turn on PHP

Check PHP version
> php -v

## Edit the HTTPD conf

> vi /etc/apache2/httpd.conf

Uncomment These lines

```
    LoadModule php7_module libexec/apache2/libphp7.so    
    LoadModule rewrite_module libexec/apache2/mod_rewrite.so]
    LoadModule vhost_alias_module libexec/apache2/mod_vhost_alias.so
    
    Include /private/etc/apache2/extra/httpd-vhosts.conf
  ```
  
## Edit HTTPD conf

> sudo vi /etc/apache2/extra/httpd-vhosts.conf 

```
<VirtualHost *:80>
    ServerName localhost
    DocumentRoot "/path/to/localhost"

    <Directory "/path/to/localhost">
        Options Indexes FollowSymLinks
        AllowOverride All
        Order allow,deny
        Allow from all
        Require all granted
    </Directory>
</VirtualHost>
```

## Restart Apache

> sudo apachectl restart

## Create Sites Folder under your Home folder

> mkdir ~/Sites
> sudo vi ~/Sites/index.php

<?php
echo "Hello From Sites Folder!";
phpinfo();
?>


## Installing MariaDB

> brew install mariadb

### Start MariaDB Server

> mysql.server start

## To auto-start MariaDB Server, use Homebrew's services functionality, which integrates with macOS launchctl:

> brew services start mariadb

## MariaDB Server is started, you can log in:

> mysql -u root

## Securing the MariaDB Server

> mysql_secure_installation

## Setup .my.cnf

> vi ~/.my.cnf

```
[client]
user=root
password=secret
```

## Docker

[Download] (https://store.docker.com/editions/community/docker-ce-desktop-mac)

## Install PHPmyAdmin

> composer create-project phpmyadmin/phpmyadmin folder

```
    $cfg['blowfish_secret'] = '1{dd0`<Q),5XP_:R9UK%%8\"EEcyH#{o'; 
    $cfg['Servers'][$i]['host'] = '127.0.0.1';
```

## setup prototype folder from Frontender

> cd /prototype÷folder

> npm ci 

> node_modules/.bin/gulp serve
