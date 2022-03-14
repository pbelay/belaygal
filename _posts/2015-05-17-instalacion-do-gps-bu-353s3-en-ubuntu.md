---
title: "Instalación do GPS BU-353S3 en ubuntu"
date: "2015-05-17"
categories: 
  - "ciencia-e-tecnoloxias"
  - "informatica"
coverImage: "gps.png"
---

[![gps](images/gps-300x135.png)](http://belay.gal/wp-content/uploads/2015/05/gps.png)Dende a liña de comandos

**sudo su**

**apt-get install gpsd gpsd-clients python-gps**

**nano /lib/udev/gpsd.hotplug**

Baixamos polo ficheiro  e incluimos esta liña **chmod a+rw $DEVNAME** a liña ten que ir xusto antes desta **gpsdctl $ACTION $DEVNAME**

Pulsar **CTRL and O** para gardar

Pulsar **CTRL and X** para sair.

**/etc/init.d/gpsd restart**

**gpsd /dev/ttyUSB0 -F /var/run/gpsd.sock**

**cgps -s**
