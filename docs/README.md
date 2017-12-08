% Guía para añadir contenidos
% **[Instituto de Física](http://fisica.udea.edu.co) - [Universidad de Antioquia](https://www.udea.edu.co)**;  **[MaldicionChina](https://github.com/MaldicionChina)**;  **[Daniel-M](https://github.com/Daniel-M)**
% November, 2017

<!-- Table of contents: Run pandoc with --toc option -->



<!-- Adding chapters from external fields -->
# Introducción
<div id="sec:introduccion"></div>

Producir páginas web de calidad con aspecto visual agradable y *responsive*
no es una tarea sencilla, siendo un requisito la escritura de extensas líneas
de código HTML acompañadas además de la definición de estilos CSS y scripts de
JavaScript que permitan una interacción amigable con el usuario.  

Para una entidad como el Instituto de Física de la Universidad de Antioquia
donde la generación y actualización rápida de contenidos es clave para la
publicación rápida de convocatorias, noticias, columnas de opinión, cursos 
de extensión, y demás procesos de comunicación del instituto, se hace necesaria
la implementación de sistemas que reduzcan las dificultades asociadas a la 
preparación y presentación de dichos contenidos en una página web.
Para tal fin existen programas que permiten convertir texto simple a páginas 
web estáticas, mediante un conjunto reducido de instrucciones y una plantilla
predefinida con los estilos CSS, JavaScripts, y HTML mínimo necesarios.

En el presente documento se describen elementos básicos de sintáxis en 
`Markdown`, un lenguaje de marcado minimalista el cual puede ser procesado
por el generador de sitios estáticos [Jekyll](https://jekyllrb.com) para
generar
[la página web del Instituto de Física de la Universidad de Antioquia](http://fisica.udea.edu.co).
Recomendamos que la guía sea leída en su totalidad antes de añadir contenidos.

## Estructura de este documento
La primera sección [Markdown](#sec:markdown), presenta los elementos de sintaxis
markdown necesarios para añadir contenidos de manera eficaz.
La sección [Cabecera YAML](#sec:yaml), ilustra la cabecera que debe emplearse en los contenidos

# Markdown
<div id="sec:markdown"></div>

Markdown es una herramienta que permite convertir texto plano a HTML facilitando
el proceso de edición de sitios web dada la simplicidad de su sintaxis,
permitiendo que los contenidos sean más comprensibles y prescindiendo del HTML.
Los archivos de markdown pueden llevar la extensión `markdown`, `mdown` o `md`,
sin embargo, se recomienda utilizar `md` para una mejor legibilidad y nombres
de archivo más cortos.


## Elementos básicos de sintaxis en Markdown
Markdown posee un conjunto simplificado de instrucciones para dar formato a los
textos. A continuación se presentan los elementos básicos de sintaxis Mardown
necesarios para la creación y edición de contenidos en Jekyll.

### Encabezados (Headers)
Los encabezados se utilizan para añadir títulos y subtítulos en el texto. Para
añadir un título principal se utiliza el símbolo `#` seguido del título
correspondiente, por ejemplo,  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
# Título pricipal
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Los subtítulos y títulos de las secciones se obtienen añadiendo un símbolo `#`
adicional por cada grado en la jerarquía de contenidos. Por ejemplo,


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
# Encabezado 1 
## Encabezado 2
### Encabezado 3 
#### Encabezado 4 
##### Encabezado 5 
###### Encabezado 6 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

### Párrafos y saltos de línea

Un párrafo es una o más líneas consecutivas de texto separadas por una o más 
líneas en blanco. El párrafo no debe llevar indentación. Por ejemplo,  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Esto es un párrafo en markdown
así contenga un salgo de línea  

Por otro lado, la línea en blanco separa este párrafo del párrafo anterior.
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Para inducir un salto de línea (`<br/>` en HTML) se deben dejar explícitos dos
caracteres de espacio al finalizar la línea, de otro modo el texto será unido
con el párrafo siguiente.

### Énfasis

Los tres tipos de énfasis soportados por Markdown son

* Texto en **negrita**, el cual se escribe rodeado de dos asteriscos: `**negrita**`,o dos guiones bajos `__así__`.   
* Texto en *italica*, el cual se escribe rodeado de un asterisco: `*italica*`,o un guión bajo `_así_`.   

Ambos formatos se pueden combinar: `*logrando **combinar** estilos*`: *logrando 
**combinar** estilos*.

### Listas(viñetas)
Para añadir listas, basta con utilizar consistentemente los caracteres `*` o 
`-`. También se pueden añadir listas anidadas conservando una indentación de 
dos caracteres respecto a la lista padre u origen. Al final de cada ítem de 
la lisa lista deben añadirse dos caracteres de espacio para indicar un salto de
línea. Las listas numeradas se construyen de manera similar, utilizando los 
números correspondientes a cada ítem tal como se ilustra a continuación,  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
 * Este es un elemento de una lista  
 * Este también.
   Este contenido se añade al mismo elemento anterior
   pues no está terminado en doble espacio.  

 - Esta es una lista independiente de la anterior  
 - También puedo tener sublistas  
   - esta lista anidada se construye con dos espacios de indentanción  
   - la indentación se hace con base en la lista padre   
   - recuerda añadir dos espacios al finalizar cada elemento de lista  


 1. También es posible  
 2. tener una lista  
 3. numerada 
 4. respetando dos espacios al final de cada ítem  
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Que se traduce en,

 * Este es un elemento de una lista  
 * Este también.
   Este contenido se añade al mismo elemento anterior
   pues no está terminado en doble espacio.  
 * Esta es una lista independiente de la anterior  
 * También puedo tener sublistas  
   * esta lista anidada se construye con dos espacios de indentanción  
   * la indentación se hace con base en la lista padre   
   * recuerda añadir dos espacios al finalizar cada elemento de lista  


1. También es posible   
2. tener una lista   
3. numerada   
4. respetando dos espacios al final de cada ítem   


### Enlaces y URLs

Para introducir enlaces o hipervínculos basta con introducir la URL
entre paréntesis precedida de un texto indicativo, por ejemplo


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
[Enlace a google](http://www.google.com) y otro a
[Universidad de Antioquia](http://www.udea.edu.co)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Que se traduce en, [Enlace a google](http://www.google.com) y otro a
[Universidad de Antioquia](http://www.udea.edu.co)  

### Imágenes

La inserción de imágenes se logra utilizando la sintaxis de URL antecedida de 
un símbolo de admiración `!`, y apuntando la ruta a la ubicación de la imagen,


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![Descripción de Imagen](ruta_a_la_imagen en disco)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

### Bloques (block quotes)
Es posible utilizar un formato especial para citas. Por ejemplo,


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
> Alicia, en qué se parece un cuervo a un escritorio?  
> --El sobrerero loco en *Alicia en el país de las maravillas*
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Produce la cita,  

> Alicia, en qué se parece un cuervo a un escritorio?  
> --El sobrerero loco en *Alicia en el país de las maravillas*

### Código fuente
Es posible escribir palabras cortas de código fuente si se escribe entre
dos símbolos de comilla inversa  \`, así


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Esta es una línea donde se ilustra `código` que será
ejecutado en la `terminal`
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Se traduce como: "Esta es una línea donde se ilustra `código` que será
ejecutado en la `terminal`".

También puede escribirse bloques de código fuente más largos 
si se introducen entre tres caracteres de comilla inversa  \`, así:


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
```
Bloque de código fuente...
.
.
.
No tiene límite de líneas
```
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Que es procesado en las líneas,


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
Bloque de código fuente...
.
.
.
No tiene límite de líneas
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Hay que tener precaución con el entorno de código fuente, pues el ancho no 
se ajusta automáticamente y, si la línea es muy larga, puede salirse más allá 
de las márgenes de la página.

## Para saber más...
* <https://daringfireball.net/projects/markdown/syntax>  
* <https://guides.github.com/features/mastering-markdown/>  

# Estructura del sitio

## Jekyll
<div id="sec:jekyll"></div>

[Jekyll](https://jekyllrb.com) es un generador de sitios estáticos que permite
construir un sitio web estático mediante la conversión de contenidos en texto
plano con un formato especial llamado `Markdown`.
Los contenidos que van a ser convertidos deben estar almacenados bajo una
jerarquía de directorios predefinida, y cada vez que se introduce un cambio en
la estructura de directorios mediante la adición o edición de contenidos, el
sitio debe ser construido de nuevo.  

## Árbol de directorios

Un árbol de directorios en Jekyll tiene la estructura,  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
atom.xml
_config.yml
css/
docs/
files/
images
_includes/
index.html
js/
_layouts/
LICENSE
_pages/
_posts/
README.md
_sass/
_site/
sitemap.xml
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

De interés para la actualización de contenidos son los directorios `_pages` y
`_posts`. Adicionalmente los directorios `images` y `files` sirven para disponer
contenidos que serán servidos en la página, a saber, imágenes y archivos.  

### Creado Posts

Los posts son publicaciones que contienen información como comunicados, noticias,
1. información de interés para la comunidad. Para la creación de estas piezas 

informativas es necesario seguir los siguientes pasos:  

* Crear un archivo en la carpeta `_posts` y nombrarlo con la siguiente convención AÑO-MES-DIA-NOMBRE-POST.md. Esto se realiza con el fin de mantener organizada la carpeta donde se encuentran los posts, además de garantizar la organización cronológica de las publicaciones.   
* El archivo creado debe iniciar por la cabecera YAML adecuada, la cual le indica al administrador de páginas estáticas el nombre (`title`), fecha de publicación(`date`), la categoria (`categories`) a la cual pertenece la publicación, así como la plantilla (`layout`) que será utilizada para construir la página. El autor se define en `author` y puede llevar el nombre `admin` o `PostgradosFisicaUdeA`.  
* Una vez definida la cabecera se procede a insertar el contenido de acuerdo a al formateo markdown presentandos en la sección [Markdown](#sec:markdown).   

Un ejemplo de cabecera YAML para una publicación tipo `post`, en la categoría
`posgrado`, con fecha y hora `2015-09-09 17:07:00`, título `Posgrado` editada
por `PosgradosFisicaUdeA`.  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
---
title: Posgrado
date: 2015-09-09 17:07:00
layout: post
author: PostgradosFisicaUdeA
categories:
- posgrado  
---

# Posgrado

## Motivación
El postgrado...
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

### Creando Pages / Sidebar

En la barra lateral se listan las publicaciones tipo `pages`, que se
caracterizan por encontrase en una categoria como `pregrado`, `posgrado`,
`personal`, `curso` o `servicio`, y tener un link de fácil acceso como
<http://fisica.udea.edu.co/pregado/fisica>. Para realizar una
publicación de este tipo es necesario seguir los siguientes pasos,  

 * Crear un archivo en la carpeta _pages y nombrarlo con la siguiente convención CATEGORIA_NOMBRE-POST.md. Esto se realiza con el fin de mantener organizada la carpeta donde se encuentran los Pages
 * En el archivo creado poner la siguiente cabecera, la cual le indica al administrador de páginas estáticas el nombre (tittle), la categoria (categories), el link desde donde se va a acceder la publicación (permalink), y la plantilla que va usar la publicación (layout).
 * Una vez definida la cabecera se procede a insertar el contenido de acuerdo a al formateo markdown presentandos en la sección [Markdown](#sec:markdown).  

Por ejemplo, una página (`page`) tendría una cabecera YAML de la forma,


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
---
title: Física
permalink: "/pregado/fisica"
layout: page
categories:
- pregrado
---
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

### Modificar barra superior

En la barra superior derecha se encuentran links que permiten rápido acceso 
información de interés. La modificación del contenido de esos accesos se 
realiza en los archivos que tienen como prefijo la palabra cabecera_. 
Estos links son estáticos, es decir no se pueden agregar o quitar.... TODO

### Sirviendo imágenes
Para colocar imágenes en las páginas, debe seguirse las instrucciones de la
sección [Markdown](#sec:markdown) sobre markdown. Las imágenes que se deseen mostrar
como contenido en alguna debe estar almacenada bajo el directorio `images/`
y ser enlazada desde allí como 


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![Descripción_de_la_imagen](images/nombre_de_archivo)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

También es posible tener subdirectorios dentro de `images/`, para servir 
imágenes cómo:


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
![Descripción_de_la_imagen](images/directorio1/directorio2/nombre_de_archivo)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

También es posible servir imágenes desde enlaces externos siempre y cuando 
se provea la URL al archivo en la forma `![nombre del enlace](url_a_archivo)`.
Así pueden servirse contenidos desde sistemas de almacenamiento en la nube
como Google Drive u Dropbox.
En el archivo de ejemplo `_posts/2017-09-09-example.md` se muestra como incluir
un enlace a una imagen desde un enlace externo.  


### Sirviendo archivos

Para servir archivos como enlaces de descarga en las páginas, debe seguirse las
instrucciones de la sección [Markdown](#sec:markdown) sobre markdown y enlaces a URLs.
Los archivos que se desean servir deben ir almacenados bajo el directorio
`files/`. También es posible disponer de subdirectorios anidados siempre y
cuando cada archivo se enlace de forma adecuada, por ejemplo,  


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
[Enlace de archivo](files/directorio1/directorio2/nombre_de_archivo)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

De esta manera se pueden servir PDF sobre convocatorias, resoluciones,
requisitos de admisión, y en general, cualquier archivo (PDF, ofimática,
archivos comprimidos).
También es posible servir archivos desde enlaces externos siempre y cuando 
se provea la URL al archivo en la forma `[nombre del enlace](url_a_archivo)`.
Así pueden servirse contenidos desde sistemas de almacenamiento en la nube
como Google Drive u Dropbox.  

En el archivo de ejemplo `_posts/2017-09-09-example.md` se muestra como incluir
un enlace a un archivo desde el directorio `files`.  


# Cabecera YAML
<div id="sec:yaml"></div>

La sección [Markdown](#sec:markdown) presentó elementos de sintaxis básico para añadir 
contenidos a las páginas, sin embargo, para que un archivo markdown sea incluído
por [Jekyll](https://jekyllrb.com) en el sitio web estático final, éste debe
iniciar con una cabecera especial que indique a jekyll la forma en que este 
archivo debe ser procesado. La ausencia de esta cabecera en el archivo markdown
hará que [Jekyll](https://jekyllrb.com) lo ignore de forma automática

## Variables YAML

#### layout

El layout determina la apariencia y relevancia que tendrán los contenidos.
Esta plantilla soporta dos tipos de layouts,

* `page` para contenidos no fechados como información general sobre el instituto

sus programas académicos, directorio de personal, servicios de extensión, etc.
Estos se enlazan en la barra lateral de navegación de la página.  
* `post` para contenidos fechados, como noticias, comunicados, convocatorias, 

contenido de cursos, y en general contenidos que no se modificarán una vez
publicados. 

#### title

Título de la página. Esto es requerido por [Jekyll](https://jekyllrb.com) para un adecuado 
renderizado del título en la plantilla del sitio.

#### permalink

Se utiliza para cambiar la ruta por defecto de `http://fisica.udea.edu.co/post/:year/:month/:day/:title` 
a `http://fisica.udea.edu.co/permalink_ingresado`. La ruta del permalink debe 
ser de la forma `campo1/campo2/...`, por ejemplo `resultados/convocatoria123`
enlazará el contenido a `http://fisica.udea.edu.co/resultados/convocatoria123`

#### date

Fecha de la publicación. El formato de la fecha es `AAAA-MM-DD HH:MM:SS`. El 
sitio esta configurado para utilizar la zona horaria "America/Bogota" así 
que se especifica la hora y fecha Colombianas.

#### categories

Se asigna una categoría a publicaciones de layout `page`, la cual puede ser 
cualquiera de las siguientes categorías, o combinaciones de ellas,

* `pregrado`
* `posgrado`
* `personal`
* `curso`
* `servicio`

Estas categorías permiten acceder a los contenidos desde la barra de navegación
a la izquierda.  


## Forma de la cabecera YAML

Una cabecera YAML para una convocatoria puede tener la forma,


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
---
layout: post
title: Convocatoria 123
date: 2018-01-15 06:00:00
categories:
-posgrado
---
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Por su parte, es posible tener una página para un curso de alto desempeño
mediante el YAML,


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
---
title: Computo alto desempeño
permalink: "/curso/computo-alto-desempeno"
layout: page
categories:
- curso
---
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

# Ejemplo de contenidos

## Con `layout: post`
Una de las páginas de ejemplo está construída de la siguiente manera,


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
---
title: Ejemplo
date: 2017-09-09 17:07:00 
layout: post
author: PosgradosFisicaUdeA
categories:
- post
---

Esta es una publicación de ejemplo para ilustrar las características del sitio
[Postgrados Física](https://fisica.udea.edu.co).  
Descargue la guía [aquí](/files/guia.pdf)

<!-- more -->

**Markdown Basico**  

El siguiente texto,  

```
Neque porro *quisquam* est, qui **dolorem** ipsum, quia ***dolor*** sit, amet,
[consectetur](http://cjdns.info/), adipisci velit.

 * lorem
 * ipsum

1. dolor
2. sit

```

Se renderiza como,  

Neque porro *quisquam* est, qui **dolorem** ipsum, quia ***dolor*** sit, amet,
[consectetur](http://cjdns.info/), adipisci velit.  

 * lorem  
 * ipsum  

1. dolor  
2. sit  

**Citación o _Blockquote_**

Como dijo Benjamin Franklin, 

> "They who can give up essential liberty to obtain a little temporary safety,
>  deserve neither liberty nor safety."
> 
> _Benjamin Franklin_

~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Con el permalink por defecto, esta publicación estará enlazada a la ruta
<http://fisica.udea.edu.co/post/2017/09/09/Ejemplo>.


## Con `layout: page`

Con el layout page podemos enlazar un permalink a la ruta
<http://fisica.udea.edu.co/posgrado/fisica-doctorado>


~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
---
title: Doctorado
permalink: "/posgrado/fisica-doctorado"
layout: page
categories:
- posgrado
---

## Datos Generales

El programa de doctorado en física...
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<!-- [https://jekyllrb.com](https://jekyllrb.com) -->

