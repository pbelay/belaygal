---
published: false
---
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

### Creación do blog e primeira entrada 
``` bash 
# Creación do blog con Jekyll
jekyll new sitioweb

# Acceso ao blog creado
cd sitioweb

# Levanttamos o servidor web para verificar o sitio
# Por defecto atópase en http://localhost:4000
bundle exec jekyll serve

```
Documentación interesante:
* [Estructura do blog](https://jekyllrb.com/docs/structure/)
* [Organización das páxinas e súbpáxinas](https://jekyllrb.com/docs/pages/) 
* [Organización dos posts, categorías, tags e borradores](https://jekyllrb.com/docs/posts/)


//TODO 
