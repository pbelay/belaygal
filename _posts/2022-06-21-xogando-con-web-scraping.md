---
published: true
---
## Xogando con web scraping en Python
Para realizar web scraping en Python é preciso empregar as seguintes librerías.
* urllib , para a podes descargar o html dos sitios web.
* beautifulsoup , para realizar consultas e filtrados sobre o html. 

Para a instalación pódese empregar pip install. 
```bash

pip install urllib 

pip install beautifulsoup4 
```
Exemplo 1, no cal se verifica o uso de urllib

```python
# Instalación de URLLIB ==> pip install urllib 
import urllib.request
datos = urllib.request.urlopen("https://pbelay.github.io/belaygal/").read().decode()
print (datos)
```

Exemplo 2, con casos de uso moi sinxelos con beautifulsoup4

```python
# Instalación de beautifulsoup ==> pip install beautifulsoup4 
import urllib.request
import sys

#Recollida dos datos
datos = urllib.request.urlopen("https://pbelay.github.io/belaygal/").read().decode()
#print (datos)

#Procesado 
from bs4 import BeautifulSoup
soup = BeautifulSoup(datos)

# Imprimir título da páxina
print(soup.title)

# Mostrar contido formateado
print(soup.prettify())


# Imprimir primeiro "p" da páxina
p1 = soup.p
print(p1)

# Acceder ao meta ao atributo charset
print(soup.meta['charset'])

# Acceder ao script ao atributo type
print(soup.script['type'])

# Acceder ao link 
print(soup.link['rel'])

# Div de nivel 1
print(" >>>> Div nivel 1")
print(soup.div)

# Lista de todos os fillos do nivel 2
print(" >>>> Fillos de de div")
print(soup.div.contents)

# children --> Retorna iterador dos fillos de nivel 1
# descendants --> Retorna todos os fillos de calquera nivel
print(" >>>> Fillos de calquera nivel")

fillos = soup.div.descendants
for child in fillos:
     if child.name:
         print(f'{child.name}')
# =========================
#FILTROS
# =========================

# Filtro pola etiqueta ligazóns
print(" >>>> Filtro pola etiqueta ligazóns")
links = soup.find_all('a')
for item in links:
         print(item)

# Filtro por atributo --> 
print(" >>>> Filtro por atributo")
filtro = soup.find_all(id='nav-trigger')
for item in filtro:
         print(item)
		 
# Filtro por atributo -->  rel="stylesheet"
print(" >>>> Filtro por atributo")
filtro = soup.find_all(rel='stylesheet')
for item in filtro:
         print(item)	 
		 

# Filtro por clase CSS -->  
print(" >>>> Filtro por clase CSS sobre as etiequetas a")
filtro = soup.find_all('a', class_="post-link")
for item in filtro:
         print(item)	

# Filtro por clase CSS -->  
print(" >>>> Filtro por clase CSS sobre as etiquetas span ")
filtro = soup.find_all('span', class_="post-meta")
for item in filtro:
         print(item.contents)
		 

# Filtro por clase CSS -->  
print(" >>>> Filtro por clase CSS sobre as etiquetas span ")
filtro = soup.find_all(class_="post-meta")
for item in filtro:
         print(item)

		 
```

Hai que evolucionar o código para xerar por exemplo CSVs coa información estruturada.

Fontes: 
* [beautifulsoup4](https://pypi.org/project/beautifulsoup4/)
* [Exemplo de scraping con CSV](https://pharos.sh/guia-para-analizar-html-con-beautifulsoup-en-python/)
* [Exemplo con facebook](https://es.acervolima.com/implementando-web-scraping-en-python-con-beautifulsoup/)
* [j2Logo](https://j2logo.com/python/web-scraping-con-python-guia-inicio-beautifulsoup/)
