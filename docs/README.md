% Guía para añadir contenidos
% **[Instituto de Física](https://fisica.udea.edu.co) - [Universidad de Antioquia](https://www.udea.edu.co)**;  **[MaldicionChina](https://github.com/MaldicionChina)**;  **[Daniel-M](https://github.com/Daniel-M)**
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
[la página web del Instituto de Física de la Universidad de Antioquia](https://fisica.udea.edu.co).

# Markdown
<div id="sec:markdown"></div>

Markdown es una herramienta que permite convertir texto plano a HTML facilitando
el proceso de edición de sitios web dada la simplicidad de su sintaxis,
permitiendo que los contenidos sean más comprensibles y prescindiendo del HTML

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

+ Texto en **negrita**, el cual se escribe rodeado de dos asteriscos: `**negrita**`
,o dos guiones bajos `__así__`
+ Texto en *italica*, el cual se escribe rodeado de un asterisco: `*italica*`
,o un guión bajo `_así_`

Ambos formatos se pueden combinar `*logrando **combinar** estilos*`: *logrando 
**combinar** estilos*

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

 + Esta es una lista independiente de la anterior  
 + También puedo tener sublistas  
   + esta lista anidada se construye con dos espacios de indentanción  
   + la indentación se hace con base en la lista padre   
   + recuerda añadir dos espacios al finalizar cada elemento de lista  


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

### Imagenes

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
+ [https://daringfireball.net/projects/markdown/syntax](https://daringfireball.net/projects/markdown/syntax)  
+ [https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)  
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

Un árbol de directorios en Jekyll tiene la forma,  

```
atom.xml
_config.yml
css/
docs/
escudo-udea.png
escudo-udea-small.png
favicon.png
files/
Gemfile
Gemfile.lock
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
```

De interés para la actualización de contenidos son los directorios `_pages` y
`_posts`. Adicionalmente los directorios `images` y `files` sirven para disponer
contenidos que serán servidos en la página, a saber, imágenes y archivos.

En el archivo de ejemplo `_posts/2017-09-09-example.md` se muestra como incluir
un enlace a un archivo desde el directorio `files`. La inclusión de imágenes en
markdown se logra de manera similar.

<!-- [https://jekyllrb.com](https://jekyllrb.com) -->

