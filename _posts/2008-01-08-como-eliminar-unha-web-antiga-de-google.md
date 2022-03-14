---
title: "Como eliminar unha web antiga de Google"
date: "2008-01-08"
categories: 
  - "informatica"
tags: 
  - "google"
  - "tag"
  - "webmaster"
---

A solución que atopei foi engadirlle  un meta-tag a páxina, trátase de **unavailable\_after**.

Un exemplo para unha páxina que queremos que expire o 15 de xaneiro de 2008 as 12:00:00 hrs. debemos incluir la seguinte etiqueta meta (dentro `do <head>` `</head>`):

> **`<meta name="googlebot" content="unavailable_after: 15-Jan-2008 12:00:00 est"/>`**
