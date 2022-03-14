---
title: "Valor e significado dos Meta Tags según Google"
date: "2008-05-13"
categories: 
  - "informatica"
tags: 
  - "deseno-web"
  - "google"
  - "html"
  - "programacion"
  - "web"
  - "xhtml"
---

Google publicou unha actualización de como o seu buscador interpreta as metatags, o cal é moi importante para todo Webmaster que desexe mellorar o SEO da súa web. Segundo Google a capitalización das tags (maiúsculas ou minúsculas) non é importante, sendo <TITLE> e <title> exactamente o mesmo, fóra da tag verify-v1. Aquí tedes unha sinxela tradución da lista de meta tags con algunhas observacións.

_<meta name="**description**" content="**descripción da páxina**\>_

Proporciona unha breve descrición da páxina utilizándose ás veces como parte do texto mostrado nos resultados dunha procura. A pesar de ser opcional e non ter ningún efecto nos rankings, unha boa descrición pode axudar a obter un mellor snippet (fragmento de texto) nos resultados da procura, o cal á súa vez pode contribuír a mellorar a calidade e cantidade dos visitantes.

_<title>**título da páxina**</title>_

Aínda que tecnicamente non é unha meta-tag esta úsase normalmente en conxunto con "description". Xeralmente o seu contido é mostrado como o título nos resultados dunha procura, e por suposto na barra do título da fiestra do navegador. A pesar de que unha páxina poida ter bo contido e aparecer nos primeiros resultados dunha procura, un bo título influenciará a que o usuarios abran ou non o enlace.

_<meta name="**robots**" content="**…, …**"> <meta name="**googlebot**" content="**…, …**">_

Estas son as normas de control que usan os motores de procura para saber que rastrexar e indexar. O tag "robots" é usada por todos os buscadores e en cambio "googlebot" só por Google, a regra por defecto é "index,follow" usada no caso de que non se especifique a tag. Estas son as distintas normas que Google sabe interpretar (múltiples parámetros deben separarse por comas):

> - noindex: impide a indexación da páxina. Correctamente usada pode utilizarse para evitar a indexación de contido duplicado.
> - nofollow: evita que se sigan enlácelos para atopar novas páxinas. Tamén usada polos Webmasters para evitar contido duplicado.
> - nosnippet: non mostrar snippets da páxina nos resultados dunha procura.
> - noodp: non usar texto pertencente de ODP (The Open Directory Project) para os xerar títulos ou snippets da páxina.
> - noarchive: non mostrar nos resultados dunha procura unha versión da páxina almacenada na Caché. Para os que non saibades, a Caché de Google é onde se almacena unha copia da páxina utilizada para ver se se realizou algún cambio desde a última indexación e saber se hai que procesala de novo. Google tamén pode usar a caché para atopar se se está copiando/duplicando contido entre webs, o cal é importante na valuación dun PageRank, non especificar esta tag e copiar contido non che libra xa que queda a copia da web orixinal, así que NON COPIES!
> - unavailable\_after:\[data\]: indica que a páxina debe borrarse dos resultados dunha procura logo da data e hora especificada.

_<meta name="**google**" value="**notranslate**">_

Cando Google identifica que o contido da páxina non está no idioma que os usuarios desexan ler, entón proverá un enlace de tradución nos resultados da procura o cal ampla as posibilidades da páxina. Para evitar que se mostre o enlace define esta tag, o seu uso xeralmente non influencia o ranking da páxina en ningún idioma.

_<meta name="**verify-v1**" content="**…**">_

Este tag é específica da ferramenta Google Webmaster Tools e úsase para verificar que sexas o propietario da páxina, o contido da tag é proporcionado por Google. A capitalización das letras do contido ¡é importante! e debe ser idéntico ao que Google fornézache.

_<meta equiv="**Content-Type**" content="**…; charset=…**">_

Define o tipo de contido e conxunto de carácteres da páxina. Asegúrache cando escribas o valor que estea entre comiñas, por exemplo: "text/html; charset=utf-8"

_<meta equiv="**refresh**" content="**…;url=…**">_

Utiliza esta tag para enviar o usuario a unha nova URL despois do tempo definido. Este sinxelo modo de redirección non está soportado por todos os navegadores e pode ser confuso para o usuario. Se necesitas cambiar a URL dunha páxina nos resultados dunha procura, é recomendable que uses unha redirección 301 o cal pode facerse desde o ficheiro htaccess.

_<meta name="**revisit-after**" content="**…**">_

Google e a maioría dos grandes buscadores ignoran por completo esta tag, a cal define cada cando debe visitarse a páxina en busca de cambios. Google recomenda que no canto de usar esta tag uses un XML Sitemap onde se defina a data e hora desde a última modificación e a frecuencia dos cambios.
