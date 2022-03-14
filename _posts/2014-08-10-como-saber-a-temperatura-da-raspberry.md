---
title: "Como saber a temperatura da raspberry"
date: "2014-08-10"
categories: 
  - "informatica"
tags: 
  - "raspberry"
  - "raspbian"
  - "temp-raspberry"
  - "temperatura"
---

Para saber a que tempetura simplemente hai que exeutar isto:

**$ /opt/vc/bin/vcgencmd measure\_temp**

Eu por comodidade creo un alias para maior comodidade

**$ alias temperatura='/opt/vc/bin/vcgencmd measure\_temp'**
