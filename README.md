# snyp - a web based auction manager based on esniper

## English

### About

Screenshot: http://twitpic.com/dkvjpk

snyp is a PHP based web interface designed to control esniper [1], a ebay auction sniper. Please note
that snyp currently can only use a subset of esnipers features.

[1] http://esniper.sf.net/

### Requirements:

* HTTP-Webserver (Apache, nginex, etc)
* PHP interpreter
* MySQL or MariaDB database
* esniper
* basic GNU utils (pstree, grep, sh)

### Installation

1. Download and unpack the ZIP file or clone the git-repository using git to a folder published by 
   your HTTP-server. This is in most cases /var/www, /srv/http, /var/www/localhost/htdocs or 
   something similar
2. Run "install/setperms.sh" to set correct permissions for all executable files
3. Create a MySQL database and import esniper.sql from the install subdirectory
4. Set the appropiate MySQL credentials in config/config.inc.php. Also check the esniper and config path
5. Add reload.php to your crontab - it will check the health of your esniper processes. The
   recommended run frequnecy is hourly so a correct line for "crontab -e" would be:
   0 * * * * /usr/bin/php -f /var/www/snyp/reload.php
6. (optional) If your server is accessible over the internet it is highly recommended to
   limit the access using .htaccess or similar methods
7. Access the folder using a browser via HTTP

## German

### Über

Screenshot: http://twitpic.com/dkvjpk

Snyp ist ein PHP-basiertes Webinterface zur Steuerung des eBay-Snipers esniper [1]. Bitte beachten sie,
dass snyp zur Zeit nicht alle Funktionen des esnipers unterstützt.

[1] http://esniper.sf.net/

### Voraussetzungen

* HTTP-Webserver (Apache, nginex, etc)
* PHP-Interpreter
* MySQL oder MariaDB Datenbank
* esniper
* GNU-Hilfsprogramme (pstree, grep, sh)

### Installation

1. Laden und entpacken sie die ZIP-Datei oder klonen sie das GIT-Repository in einen Ordner, welcher
   von ihrem HTTP-Server veröffentlicht wird. Dies ist meist /var/www, /srv/http,
   /var/www/localhost/htdocs oder Änhliches.
2. Starten sie "install/setperms.sh" um die korrekten Rechte für ausführbare Dateien zu setzen.
3. Erstellen sie eine MySQL-Datenbank und importieren sie die Inhalte der esniper.sql, welche im
   Unterverzeichnis "install" zu finden ist.
4. Tragen sie die entsprechenden MySQL-Zugangsdaten in der Datei config/config.inc.php ein. Hier sind auch die
   Pfade zu esniper und dessen Konfiguration an die lokalen Begebenheiten anzupassen.
5. Fügen sie die reload.php zur Crontab hinzu - diese Datei prüft regelmäßig den Zustand der esniper-
   Prozesse. Die empfohlene Ausführtfrequenz liegt bei 60 Minuten, eine passende Zeile für "crontab -e"
   würde z.B. so aussehen:
   0 * * * * /usr/bin/php -f /var/www/snyp/reload.php
6. (optional) Ist der Webserver über das Internet erreichbar wird dringend empfohlen z.B. über .htaccess
   einen Zugriffsschutz einzurichten.
7. Rufen sie den Ordner mit einem Browser per HTTP auf.
