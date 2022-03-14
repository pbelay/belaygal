---
title: "Instalar as X en Debian"
date: "2007-09-27"
categories: 
  - "informatica"
tags: 
  - "linux"
---

Pois hoxe andiben a instalar a debian e despisteime e non instalei o entorno gráfico polo cal aprobeito para deixar aqui un pequeno manual de como facelo. Nota debes ser usuario root. A recetiña é a seguinte:

1\. # _**apt-get install x-window-system**_ 2. # **_apt-get install gnome-core_** 3. _**\# apt-get install gdm**_ (Con isto instalas un prompt login para as X ) 4. _**\# /etc/init.d/gdm start**_ (Inicia o Display Manager) 5. A meter o login e contraseña xa está, quen decia que ia ser dificil xDD

Se X falla e aparece unha fiestra de texto, escolle non configurar X. Estuda coidadosamente o arquivo _**/var/log/Xorg.0.log**_. Este arquivo de rexistro pode darche ideas de que compoñente de X está mal configurado (dispositivo, rato, monitor, frecuencias de varrido, teclado, memoria, etc.). En particular, fíxache na liñas que comezan con (EE), que indican un erro. Volve a Instalación e configuración de X antes de intentar iniciar X co Display Manager.
