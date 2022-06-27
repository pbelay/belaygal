---
published: false
---

- [Comezando con Jekyll](#comezando-con-jekyll)
  - [Instalación en windows](#instalación-en-windows)
  - [Instalación en Linux](#instalación-en-linux)
  - [Creación do blog](#creación-do-blog)
  - [Creación das entradas](#creación-das-entradas)
- [Mudar o tema](#mudar-o-tema)
## Comezando con Jekyll 

### Instalación en windows
Para elo é preciso seguir a [guía do sitio oficial](https://jekyllrb.com/docs/installation/windows/) que podemos resumir nos seguintes pasos. 

```ps  
#Instalación de  Ruby Developer Kit con winget
winget install -e --id RubyInstallerTeam.RubyWithDevKit

#Executamos gem  para comprobar a instalación
gem -v

#Actualización dos paquetes de gem
gem update 

#Instalación de Jekyll
gem install jekyll bundler
```

### Instalación en Linux 
Para elo é preciso seguir a [guía do sitio oficial](https://jekyllrb.com/docs/installation/other-linux/) que podemos resumir nos seguintes pasos. 

```bash 
#Instalación de  Ruby 
sudo apt-get install ruby-full build-essential
#gem
gem update

#Instalación de Jekyll
gem install jekyll bundler

#Comprobación da versión
jekyll -v
```

### Creación do blog
``` bash 
# Creación do blog con Jekyll
jekyll new sitioweb

# Acceso ao blog creado
cd sitioweb

# Levanttamos o servidor web para verificar o sitio
# Por defecto atópase en http://localhost:4000
bundle exec jekyll serve

```

### Creación das entradas
No directorio ```_posts``` almacenanse as entradas para o blog nas cales a convención é  ano-mes-dia-nomeFicheiro, por exemplo: ```2022-06-23-git-chuleta.md```. O ficheiro é de tipo Markdown ao cal podemos engadirlle na cabeceira diferentes datos como: título, data, categoría, ... Maís información na [documentación](https://jekyllrb.com/docs/variables/)

```md
---
layout: post
title: "Santos Inocentes xDDD"
date: "2006-12-28"
categories: 
  - "cousas-minas"
  - "informatica"
---
```
## Mudar o tema 
1. Temos que procurae algún dos temas desenvoltos. Os sitios máis populares son:
   1. [https://github.com/topics/jekyll-theme](https://github.com/topics/jekyll-theme)
   2. [http://jekyllthemes.org/](http://jekyllthemes.org/)
   3. [https://jamstackthemes.dev/ssg/jekyll/](https://jamstackthemes.dev/ssg/jekyll/)
2. Unha vez escollido o tema imos editar o ficheiro ```Gemfile``` engadindo a liña co gem correspondente ao tema, no noso caso é [just-the-docs](https://github.com/just-the-docs/just-the-docs) .
   > gem "just-the-docs" 
3. Editamos o ficheiro ```_config.yml``` para que empregue o novo tema por exemplo asi:
> theme: just-the-docs

4. Executamos
> bundle

5. Xa podemos lanzar o servidor que temos o tema trocado.



Documentación interesante:
* [Estructura do blog](https://jekyllrb.com/docs/structure/)
* [Organización das páxinas e súbpáxinas](https://jekyllrb.com/docs/pages/) 
* [Organización dos posts, categorías, tags e borradores](https://jekyllrb.com/docs/posts/)


//TODO 
