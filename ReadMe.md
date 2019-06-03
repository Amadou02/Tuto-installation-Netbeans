___
# Installation de NetBeans 8.2
## Installer la dernière version de OpenJDK 12, 11 ou 8 sur ubuntu en passant par Zulu OpenJDK Builds

* Importer la clé du dépot de zulu et l'ajouter à vos sources

      sudo apt-key adv --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys 0xB1998361219BD9C9

      sudo apt-add-repository 'deb http://repos.azulsystems.com/ubuntu stable main'

* Installer OpenJDK8

      sudo apt install zulu-8

## Télécharger et installer NetBeans 8.2

* Télécharger NetBeans : [Site officiel de NetBeans](https://netbeans.org/downloads/8.2/)

* Ouvrez le Terminal et saisissez le commande ci-dessous

      1. cd ~/Téléchargement
      2. chmod +x netbeans-8.2-php-linux-x64.sh
      2. ./netbeans-8.2-php-linux-x64.sh 

## Installation de xdebug

* Ouvrez le Terminal et saisissez le commande ci-dessous

      1. sudo apt install php-xdebug
      2. sudo nano /etc/php/7.0/mods-available/xdebug.ini
      3. remplacer le contenu par le code suivant

      zend_extension=/usr/lib/php/20170718/xdebug.so
      xdebug.remote_autostart = 1
      xdebug.remote_enable = 1
      xdebug.remote_handler = dbgp
      xdebug.remote_host = 127.0.0.1
      xdebug.remote_log = /tmp/xdebug_remote.log
      xdebug.remote_mode = req
      

      4. rédemarrer apache2 :

          sudo systemctl reload apache2

## Tester votre installation

* Ouvrez le Terminal et saisissez le commande ci-dessous

      php -v

* Sortie 

       PHP 7.2.17-0ubuntu0.18.04.1 (cli) (built: Apr 18 2019 14:12:38) ( NTS )
       Copyright (c) 1997-2018 The PHP Group
       Zend Engine v3.2.0, Copyright (c) 1998-2018 Zend Technologies
       with Zend OPcache v7.2.17-0ubuntu0.18.04.1, Copyright (c) 1999-2018, by Zend Technologies
       with Xdebug v2.6.0, Copyright (c) 2002-2018, by Derick Rethans




      
