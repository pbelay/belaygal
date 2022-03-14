---
title: "Redes Sociais, a privacidade entre dito"
date: "2009-05-27"
categories: 
  - "informatica"
---

[![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8%2F9hAAAABGdBTUEAANkE3LLaAgAAAaFJREFUeJyFkb9OG0EQh781B3JzioR0Ig0SFPAEiRQ3KIpsCVkUQMEDIAoQFFGq0FDQhIoOKUqRgi5FuhTs5QFMHiA0NAdGIHH8Mzmi4DMzKWyfOXyX%2FKrdmdlvfzNjyNHG%2B3faPW9ubZu8Ogdgbf5Fufpy%2FHs3uN8YZXZhBYDb6BxAXz2rJ4%2BWt%2Fzh40bjGsAAfP6wqdMlD4CPe4fMLqxwG51zGZ4BcBQE3ISnLE9PALBXC1lc3zCJAwDnd%2FuHtaki9YNPuIDbyY2NACMD3JwcdCJeuoXHCq%2FuuPCqeS0zGn7rn8FjnXhV3ryewhkqpuK%2B71MqlajVgPqPbMDF1S%2FwwJjsobuu24a0r4NAXOgm72PJtZ0FsdY2Uw7iuJUUiQgFBdUetFKp4Pt%2BHzA9g451hfaCtZdSVcrlMsYYjDEJLBugioqiqjyViOA4vWdPttABiCAiqRa6sH8D5CEpilst0PRgVbVvQw7Al6%2B7b39OPq82Y7mbWZqZu2%2FGUhwYKoj0b0Y1u7VE1lqNouiP%2FkfWWs2YAQRBsArs5H%2BROFkH%2BAtt99BK1T3CFwAAAABJRU5ErkJggg%3D%3D)](# "Copiar texto ao portapapeis")[![](data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAABAAAAAQCAYAAAAf8%2F9hAAAABmJLR0QA%2FwD%2FAP%2BgvaeTAAAACXBIWXMAAAsTAAALEwEAmpwYAAAAB3RJTUUH1gYDDwALCciRaQAAAflJREFUOMuNk71rU2EUxn%2F3I%2FdemxQ%2Fujmope3gIoimli4idnBxyODg4CIugi4O4h%2FhJjgWdympZA6lFCwtBhWELi2lhVKoTRqT3M%2F3y6W5JNhKnukM5%2Fm9zzmH1wompp1rtytPgiB4XRwL5i3L4n8yxhBGydckST7sf69%2BdoHA8wpvXj57VL5YuoDnufgFBwCtDamQRHFGnAqiOKMXpRw1%2F8yvrv8sADUXKI2XiuVWOySKM2zbwrYttDZobZBKIaUmExIhFEkmEEIxXiqWgZIL%2BJZlESUZUmnevVgAYPXbDus%2FdtFaM3trkoW5GQDevl9GG8PpqL4L2ABKaaStWNnc5sHsNPfvTgEgpM7NX1Z%2B0Q1jklT0V2K7%2FSoTEtuyWGtso7RhYW4mhwB8Wt6kVm%2BgjRlaag5QStMNYzq9mMWdA%2FYPWzyv3ANgsbpBrd448yo54HerQxglCCl5%2FPBObgby%2BixIDuiGMUqpIfNidSMHDEIcx8kBdr8YC7yh1%2Fqxa%2FXGEGiwdyhB4Ht0w5jKq4%2F%2FxOyDBnuHEhhj8L0Co8r3CpjTa7iAPml3thzHvjlz4%2BpIgExITtqdLUC7QHp8dLBUX9NPJ65cmhrlMzVb7Z3W8eESkFrBxHQRuA5MApcH93KOJHAC7AJ7LpAAe0AT8Acvc440kAI9IPkLO1rzZln0%2BMIAAAAASUVORK5CYII%3D)](# "Pechar")

<script type="text/javascript"><!-- function copiarPortapapeisGM_BoxValuesSession() { try { netscape.security.PrivilegeManager.enablePrivilege("UniversalXPConnect");const gClipboardHelper = Components.classes["@mozilla.org/widget/clipboardhelper;1"].getService(Components.interfaces.nsIClipboardHelper);gClipboardHelper.copyString( document.getElementById("GM_BoxValuesSession").innerHTML );}catch(e){}}function pecharGM_BoxValuesSession() { document.getElementById('GM_BoxValuesSession').parentNode.style.display = 'none';} // --></script>

[Nunha entrada anterior analicei moitos dos perigos que teñen as redes sociais](http://belay.es/2009/01/tuenti-e-a-privacidade/). Neste caso tocalle a máis popular de todas facebook. Normalmente nesta aplicación só podes ver as fotos dunha persoa que teñas agregada comoa amiga e te autorizara. Pero isto non é seguro ainda que o fagan ver así, pois xa é posible ver as fotos de calqueira persoa ainda que non sexa amig@ ou te teña bloqueado. Este pequeno truquiño atopeino en [geektheplanet.net](http://geektheplanet.net/2972/how-to-ver-las-fotos-de-cualquiera-en-facebook.xhtml)

Este pequeno truquillo (fallo de seguridade) serve para ver as fotos de calqueira e é posibel grazas a API que nos ofrece Facebook, para desenrolar aplicacións. Neste caso concreto podes crear consultas SQL, sobre as bases de datos, e obter as urls dos diferentes albums desa persoa.

Para elo é preciso obter o ID do perfil da persoa a que vamos verlle as súas fotos. Este ID atopase na URL do perfil, normalmente ven neste formato _**http://www.facebook.com/profile.php?id=xxxxxxxxxx**_ onde _**xxxxxxxx**_ é o ID do perfil. Unha forma de obtelo e darlle no boto de agregar como amigo, non se vai agregar ainda porque precisa unha confirmación previa para enviar a solicitude de amizade.

A continuación tes os pasos para ver as fotos de calqueira no Facebook.

- Entra na [ferramenta de desenrolo de aplicacións](http://developers.facebook.com/tools.php) do Facebook
- Nela tes unha pestaña que di: “Plataforma para Probar API” no lado esquerdo en Formato de resposta elixes Facebook PHP Cliente.
- Agora mais abaixo en Método elixe fql.query
- Agora debaixo aparece un campo chamado query, e escribemos a seguinte consulta sql. Pero hai que reemplazar xxxxxxxxxx polo ID do usuario que queres cotillear.

> _SELECT name, link  
> FROM album__  
> WHERE owner=xxxxxxxxxx_

- Presiona no botón que dí _Método de chamada_ e do lado dereito vaiche sair un código cun Array, que será semellante a este:  
    
    > Array
    > (
    >     \[0\] => Array
    >         (
    >             \[name\] => Nombre el álbum
    >             \[link\] => **http://www.facebook.com/album.php?aid=xxxxx&id=xxxxxxxxxx**
    >         )
    > )
    
- Neste código pode ter varuas URL's como esta, URL corresponde a un album.
- A URL que vas a copiar é só a que está en negriña.
- Pega a URL na barra de direccións do ten navegador e listo, a cotillear en calqueira sitio :-D

Así que agora en diante pensao ben antes de subir fotos privadas ao Facebook porque como podes ver calqueira pode _hackear Facebook_ e ver as fotos.
