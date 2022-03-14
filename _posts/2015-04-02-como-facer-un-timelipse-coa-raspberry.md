---
title: "Como facer un timelapse coa raspberry"
date: "2015-04-02"
categories: 
  - "informatica"
coverImage: "equipo.jpg"
---

Facer un timelapse coa raspberry é moi sinxelo, no meu caso o que fixen foi:

- Crear un ficheiro bash para xenerar as imaxenes con nome a data e hora do momento de sacala. Ademáis hai algúns parámetros de tamaño da imaxen e calidade.
    
    > _#!/bin/bash_ _FECHA=$(date +%Y-%m-%d\_%H:%M:%S)_ _raspistill -vf -w 640 -h 480 -q 80 -o /home/pi/public/images/"$FECHA"\_foto.jpg_
    

- Logo definin un cron que se executa cada minuto, que chama ao bash feito no paso anterior.
    
    > _crontat -e_
    
    engadimos a seguinte linea
    
    > _\*/1 \* \* \* \* /home/pi/crons/image.sh_
    

- O seguinte paso é copiar as imaxes nun directorio e xenerar o video. Primeiro creamos un ficheiro coas imaxenes a procesasr e despois as procesamos con mencoder.
    
    > _ls \*.jpg > list.txt_
    
    > _mencoder -nosound -ovc lavc -lavcopts vcodec=mpeg4:aspect=16/9:vbitrate=8000000 -vf scale=640:480 -o timelapse.avi -mf type=jpeg:fps=24 mf://@list.txt_
    
- Xa teriamos no noso directorio o video xenerado co nome timelapse.avi

Se lle quixeramos poñer son ao video  poderiamos procesalo tamen dende a liña de comandos con mencoder.

> mencoder -ovc copy -audiofile musica\_timelapse.mp3 -oac copy timelapse.avi -o output.avi

Actualización:

Outra forma de facer a captura cada x tempo é empregando o comando raspistill cos seguintes parámetros:

- \- o nome do ficheiro onde lle indicamos que a secuencia vai ser de 4 díxitos con  %04
- \-t tempo de captura en milisegundos
- \-tl  tempo de separación entre cada foto en milisegundos
- \-vf para xirar a foto no sentido vertical
    - \-hf para xirar a foto no sentido horizontal

 

>  raspistill -o  timelapse2%04d.jpg -t 5400000 -tl 3000 -vf -hf
