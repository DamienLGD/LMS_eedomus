# LMS_eedomus
Plugin pour utiliser une Squeezebox avec l'Eedomus (avec retour d'�tat). 

Ce plugin permet de commander une Squeezebox via des requ�tes HTTP.  
Il a besoin de 3 choses, l'adresse IP de votre serveur LMS, de son port, et de l'adresse MAC de la squeezebox que vous souhaitez contr�ler.  
Vu que le serveur LMS peut g�rer plusieurs Squeezebox, il a besoin de l'adresse MAC pour savoir � quelle Squeezebox s'adresser.  
Ainsi si vous avez 5 Squeezebox, vous devez installer 5 fois le plugin (ou le dupliquer).  
Vous pouvez trouver l'adresse MAC dans les param�tres du serveur LMS (onglet platine).  

## Retour d'�tat

Avant la version 7.6, Logitech avait inclu la possibilit� d'avoir les informations en cours dans un XML.  
Nous devons donc remettre ce dossier XML si vous �tes sur une version sup�rieure.   
T�l�charger une version ant�rieure [ici](http://downloads.slimdevices.com/SqueezeboxServer_v7.5.5/squeezeboxserver-7.5.5.tgz) qu'il faudra d�zipper et r�cup�rer le dossier XML dans le dossier HTML.  
Sinon le dossier XML est h�berg� sur ma [Dropbox](https://www.dropbox.com/sh/poa4cxsxccehdqv/AADj9PSSSk2Rb9XAJk1YylAKa?dl=0)  

D�poser ce dossier XML sur votre NAS/Raspberry Pi (FTP ou SFTP avec Filezilla, partage r�seau, SCP etc...)  

Si vous avez un Synology, connecter vous en SSH afin de copier le dossier et d'appliquer les bons droits. 

cp -R /volume1/votredossier/xml /volume1/@appstore/SqueezeCenter/HTML/  
chmod 755 -R /volume1/@appstore/SqueezeCenter/HTML/xml/  
   
Si vous utilisez Max2Play:  

cp -R /home/xml /usr/share/squeezeboxserver/HTML/  
chmod 755 -R /usr/share/squeezeboxserver/HTML/xml/ 