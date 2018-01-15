# LMS_eedomus
Plugin pour utiliser une Squeezebox avec l'Eedomus (avec retour d'états). 

Ce plugin permet de commander une Squeezebox via des requêtes HTTP.  
Il a besoin de 3 choses, l'adresse IP de votre serveur LMS, de son port, et de l'adresse MAC de la squeezebox que vous souhaitez contrôler.  
Vu que le serveur LMS peut gérer plusieurs Squeezebox, il a besoin de l'adresse MAC pour savoir à quelle Squeezebox s'adresser.  
Ainsi si vous avez 5 Squeezebox, vous devez installer 5 fois le plugin (ou les dupliquer).  
Vous pouvez trouver l'adresse MAC dans les paramètres du serveur LMS (onglet platine).  

## Retour d'état

Avant la version 7.6, Logitech avait inclut la possibilité d'avoir les informations en cours dans un XML.  
Nous devons donc remettre ce dossier XML si vous êtes sur une version supérieure.   
Télécharger une version antérieure [ici](http://downloads.slimdevices.com/SqueezeboxServer_v7.5.5/squeezeboxserver-7.5.5.tgz) qu'il faudra dézipper et récupérer le dossier XML dans le dossier HTML.  
Sinon plus simple le dossier XML est hébergé sur ma [Dropbox](https://www.dropbox.com/sh/poa4cxsxccehdqv/AADj9PSSSk2Rb9XAJk1YylAKa?dl=0)  

Déposer ce dossier XML sur votre NAS/Raspberry Pi (FTP ou SFTP avec Filezilla, partage réseau, SCP etc...)  

Si vous avez un Synology, connecter vous en SSH afin de copier le dossier et d'appliquer les bons droits. 

cp -R /volume1/votredossier/xml /volume1/@appstore/SqueezeCenter/HTML/  
chmod 755 -R /volume1/@appstore/SqueezeCenter/HTML/xml/  
   
Si vous utilisez Max2Play:  

cp -R /home/xml /usr/share/squeezeboxserver/HTML/  
chmod 755 -R /usr/share/squeezeboxserver/HTML/xml/ 
