---
title: "Configurar a cámera na Raspberry"
date: "2014-09-09"
categories: 
  - "informatica"
tags: 
  - "camera"
  - "foto"
  - "raspberry"
  - "video"
coverImage: "equipo.jpg"
---

Neste post vou explicar como instalar o módulo da cámara para Raspberry Pi e como facer fotos e vídeo con ela.

1. Xuntar todo o material: a Raspberry Pi e  a cámara.
2. Instala a cámara na Raspberry Pi. Importante os fios teñen que quedar mirando cara o conector HDMI. (ver foto)
3. [![0_install_camera](images/0_install_camera-150x150.jpg)](http://belay.es/?attachment_id=1633)Encende a tua Raspberry Pi.
4. No terminal executa _**sudo raspi-config**_  e sairache a seguinte pantalla na cal activaras "enable camera " [![enablecamara](images/enablecamara-150x150.png)](http://belay.es/wp-content/uploads/2014/09/enablecamara.png)
5. Desprazate ata a opción "cámara", e  deixala habilitada e pulsas finalizar e teraseche que reiniciar a  Raspberry Pi.

Agora xa tes configurada a  Raspberry Pi e poderas capturar videso e foto empregando o comando _raspistill_Algúns exemplos son:

- Capturar unha imaxen: **_raspistill -o image.jpg_**
- Capturar 10 segundos de video: **_raspivid -o video.h264 -t 10000_**

[](http://belay.es/wp-content/uploads/2014/09/IMG_20140909_170651.jpg)[](http://belay.es/wp-content/uploads/2014/09/equipo.jpg)[![equipo](images/equipo-768x1024.jpg)](http://belay.es/wp-content/uploads/2014/09/equipo.jpg)
