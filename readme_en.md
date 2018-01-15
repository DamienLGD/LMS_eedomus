# LMS_eedomus
Plugin for Squeezebox. 

This plugin can control a Squeezebox by HTTP request.  
It needs 3 things, IP of your LMS server, Port of your LMS server, and MAC address of your Squeezebox.  
LMS server can control multiple Squeezebox, so MAC Address permit to request the right Squeezebox.  
If you have more than 1 Squeezebox, you have to install an other one.  
You can find MAC address in LMS Settings (second tab).  

## Instant state

Before LMS 7.6, there was a XML folder.  
So we have to download this XML folder on a previous version if you are on 7.6 or >.  
You can find it [here](http://downloads.slimdevices.com/SqueezeboxServer_v7.5.5/squeezeboxserver-7.5.5.tgz) or on my [Dropbox](https://www.dropbox.com/sh/poa4cxsxccehdqv/AADj9PSSSk2Rb9XAJk1YylAKa?dl=0)  

Add the XML folder on your NAS/Raspberry Pi (FTP or SFTP with Filezilla, network share, SCP etc...)  

If you have a Synology, connect with SSH, copy the folder in the good path and change scope values.  

cp -R /volume1/votredossier/xml /volume1/@appstore/SqueezeCenter/HTML/  
chmod 755 -R /volume1/@appstore/SqueezeCenter/HTML/xml/  
   
If you use Max2Play:  

cp -R /home/xml /usr/share/squeezeboxserver/HTML/  
chmod 755 -R /usr/share/squeezeboxserver/HTML/xml/ 