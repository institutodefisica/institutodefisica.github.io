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

# Estructura del sitio
<div id="sec:jekyll"></div>
Árbol de directorios

# Markdown
<div id="sec:markdown"></div>

Markdown es una herramienta que permite convertir texto plano a HTML facilitando
el proceso de edición de sitios web. Permite emplear una sintaxis en texto
plano, comprensible que será procesado en el HTML correspondiente.

## Elementos básicos de sintaxis en Markdown
Markdown posee un conjunto simplificado de instrucciones para dar formato a los
textos. A continuación se presentan los elementos básicos de sintaxis Mardown
necesarios para la creación y edición de contenidos en Jekyll.

### Encabezados (Headers)
Los encabezados se utilizan para añadir títulos y subtítulos en el texto. Para
añadir un título principal se utiliza el símbolo `#` seguido del título
correspondiente, por ejemplo,  

```markdown
<!-- Título pricipal -->
```

Los subtítulos y títulos de las secciones se obtienen añadiendo un símbolo `#`
adicional por cada grado en la jerarquía de contenidos. Por ejemplo,

```
<!-- Encabezado 1 -->
```

### Párrafos y saltos de línea

Un párrafo es una o más líneas consecutivas de texto separadas por una o más 
líneas en blanco. El párrafo no debe llevar indentación. Por ejemplo,  

```
Esto es un párrafo en markdown
así contenga un salgo de línea  

Por otro lado, la línea en blanco separa este párrafo del párrafo anterior.
```

Para inducir un salto de línea (`<br/>` en HTML) se deben dejar explícitos dos
caracteres de espacio al finalizar la línea, de otro modo el texto será unido
con el párrafo siguiente.

### Énfasis

Los tres tipos de énfasis soportados por Markdown son

+ Texto en *negrita*, el cual se escribe rodeado de dos asteriscos: `**negrita**`
1. dos guiones bajos `__así__`

+ Texto en **italica**, el cual se escribe rodeado de un asterisco: `*italica*`
1. un guión bajo `_así_`

Ambos formatos se pueden combinar `_logrando **combinar** estilos_`: **logrando 
**combinar** estilos**



### Listas(viñetas)
### Imagenes
### Enlaces y URLs
### Bloques (block quotes)
### Código fuente
## Para saber más...
+ [https://daringfireball.net/projects/markdown/syntax](https://daringfireball.net/projects/markdown/syntax)
+ [https://guides.github.com/features/mastering-markdown/](https://guides.github.com/features/mastering-markdown/)
<!-- [https://jekyllrb.com](https://jekyllrb.com) -->

