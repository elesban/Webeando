HTML
====

HTML son las siglas de HyperText Markup Language («lenguaje de marcas de hipertexto»), hace referencia al lenguaje de marcado para la elaboración de páginas web. Es un estándar que, en sus diferentes versiones, define una estructura básica y un código (denominado código HTML) para la definición de contenido de una página web, como texto, imágenes, etc. Es un estándar a cargo de la W3C, organización dedicada a la estandarización de casi todas las tecnologías ligadas a la web, sobre todo en lo referente a su escritura e interpretación.

El lenguaje HTML basa su filosofía de desarrollo en la referenciación. Para añadir un elemento externo a la página (imagen, vídeo, script, etc.), este no se incrusta directamente en el código de la página, sino que se hace una referencia a la ubicación de dicho elemento mediante texto. De este modo, la página web contiene sólo texto mientras que recae en el navegador web (interpretador del código) la tarea de unir todos los elementos y visualizar la página final. Al ser un estándar, HTML busca ser un lenguaje que permita que cualquier página web escrita en una determinada versión, pueda ser interpretada de la misma forma (estándar) por cualquier navegadores web actualizado.[1]

El lenguaje HTML puede ser creado y editado por cualquier editor de textos básico, como *Bloc de notas* de Windows o *Gedit* en Linux. Existen otros editores para la realizaciòn de sitios web con características gráficas que permiten ver el resultado de lo que se está editando en tiempo real.

====

###Etiquetas



Las etiquetas o marcas delimitan cada uno de los elementos que componen una página web; por lo regular, presentan dos partes:

*Una apertura:*  `<etiqueta>`

*Un cierre:* `</etiqueta>`

Cada elemento que es representado por estas etiquetas pueden contener una a serie de atributos opcionales que pueden añadir ciertas propiedades.

```<etiqueta atributo1="valor" atributo2="valor"></etiqueta>```

Todo lo incluido en en interior de las etiquetas sufrirá las modificiaciones que caracterizan a esta etiqueta. Por ejemplo:

`<b>Este texto está en negrita</b>`

Las etiquetas `<b></b>` definen un texto en negrita. El resultado sería el siguiente:

__Este texto está en negritas__

Se debe tomar en cuenta que un documento HTML debe de estar delimitado por la etiqueta `<html>/<html>`. Dentro de este documento, podemos distinguir dos partes principales:

*El encabezado*, definido por `<head></head>` donde se colocan etiquetas "informativas" como el título de nuestra página.

*El cuerpo*, definido por las etiqutas `<body></body>`, donde se colocan el texto, imágenes, enlaces y demás elementos que conforman una página.

De este modo, podríamos definir lo que sería la estructura básica de un documento HTML con un título.

```
<html>
  <head>
    <title>Mi sitio web</title>
  </head>
  <body></body>
</html>
```

###Texto

El texto puede insertarse libremente dentro de la etiqueta body y ser desplegado en la página; sin embargo, existen opciones para darle formato de manera sencilla.

Una de las opciones más usadas son los párrafos. Los párrafos sirven para designar líneas de texto que guardan la misma alineación y propiedades. Para definirlos, se utiliza la etiqueta `<p> </p>`. Es importante destacar que los saltos de línea dentro de esta etiqueta no se definen con la tecla *Enter*. Para dar un salto de línea se utiliza la etiqueta `<br>`.

__Ejemplo:__

```
<html>
  <head>
    <title>Mi sitio web</title>
  </head>
  <body>
  	<p>Este es un párrafo.</p>
  	<p>Este es otro párrafo <br> con un salto de línea</p>
  </body>
</html>
```

El texto dentro de un documento HTML puede tener distintos y variados formatos. Dicho formato puede ser indicado a través de algunas etiquetas o por [hojas de estilo (CSS).](04 Hojas de estilo/Hojas de estilo.md)



====

[1]: http://es.wikipedia.org/wiki/HTML "HTML en Wikipedia.org"