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

`<etiqueta atributo1="valor" atributo2="valor"></etiqueta>`

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
 
```
<html>
  <head>
    <title>Mi sitio web</title>
  </head>
  <body>
  	<p>Este es un párrafo <b>con texto en negritas</b>.</p>
  	<p>Este es otro párrafo <i>con texto en cursiva</i></p>
  </body>
</html>
```

En cuanto a la alineación del texto, el tipo y el tamaño de la fuente y demás, pueden señalarse por medio de atributos dentro de las etiquetas. 

```
  	<p align="center">Este es un párrafo centrado.</p>
  	<p color="#83b81a">Este párrafo tiene un color específico</p>
```

__Importante:__ Muchas de las propiedades que tienen los documentos HTML, son establecidas mediante hojas de estilo por lo que incluirlas como atributos es poco común hoy en día. 

###Enlaces

Un hiperenlace, hipervínculo o vínculo, no es más que un enlace a lleva a otra página o archivo.

El texto o las imágenes que representen un enlace deben estar dentro de las etiquetas `<a></a>`.

El atributo `href`especifica la ruta o dirección de la página destino a la que el usuario será rigido cuando pulse sobre el enlace.

Por ejemplo, si se quisiera incluir un enlace a la página de Wikipedia, se podría incluir el siguiente código

```
  Este es un enlace a <a href="http://wikipedia.org">Wikipedia</a>
```

###Imágenes

Uno de los aspectos más vistosos y atractivos de las páginas web son las imágenes. 

La etiqueta que utilizaremos para instertar una imagen es `<img>`. Esta etiqueta no posee un cierre y en ella se especifica el origen o ruta del archivo gráfico mediante en atributo `src`. Ejemplo:

```
  <img src="images/photo.jpg" >
```

###Formularios

Un formulario es un elemento que permite recoger datos introducidos por el usuario.

Los formularios se utilizan para conocer las opiniones, dudas y otra serie de datos sobre los usuarios.

Un formulario está formado, entre otras cosas, por etiquetas, campos de texto, menús y botones.

Para insertar un formulario en un documento HTML se utilizan las etiquetas `<form> </form>` y dentro de ellas se agregan los elementos que formarán dicho formulario.

Los atributos más comunes en el uso de formularios son: `action` y `method`. El primero indica una dirección a la cual se enviarán los datos; la segunda indica el método en que será cifrada la información para su envío. 

```
	<form action="proceso.php" method="POST">
	...
	</form>
```

__Elementos de entrada__

Los campos de texto (input) utilizan la etiqueta `<input >`. Los atributos más comunes son `name` y `type`.

Hay muchos tipos diferentes de "inputs" como `email` (correo), `text` (texto) o `password` (contraseña).

```
	<form action="proceso.php" method="POST">
	  <input name="nombre" type="text" >
	  <input name="contrasenia" type="password" >
	  <input name="correo" type="email" >
	</form>
```

__Casilla de verificación__

Para insertar una casilla de verificación, necesitamos añadir el valor `checkbox` al atributo `type` de un elemento `<input>`. Para indicar que esa casilla está activada se necesita añadir el atributo `checked`.

`<input name="casilla" type="checkbox" checked >`

__Botón de opción__

Los botones de opción requieren el valor `radio` dentro del atributo `type`. Para indicar una que una opción está seleccionada se tiene que indicar a través del atributo `checked`.

```
<input nombre="opcion1" type="radio" checked>
<input nombre="opcion2" type="radio" >
```

__Campos de selección__


Si se requiere insertar un menú o una lista desplegable dentro de un formulario se puede incluir un campo de selección, a través de las etiquetas `<select> </select>`. El atributo `name` indica el nombre, el atributo `multiple` indica que se pueden seleccionar varios elementos. 

Los elementos que conforman la lista son instertados entre las etiquetas `<option></option>` y se se quiere mostrar una opción seleccionada por defecto se utiliza el atributo `selected`.

```
  <select name="opciones"">
    <option>Uno</option>
    <option selected>Dos</option>
    <option>Tres o más</option>
  </select>
```

__Áreas de texto__

Las áreas de texto permiten escribir varias líneas de texto dentro de un formulario por lo que suelen usarse para incluir comentarios. Para insertar un área de texto se utilizan las etiquetas `<textarea></textarea>`. En ocasiones se indica el ancho y el alto de este elementro a través de columnas. El atributo `rows` indica el número de líneas que podrán ser visualizadas por lo que determina el alto; el atributo `cols` indica el número de columnas por lo que determina el 
ancho del elemento.

`<textarea name="comentario" cols="30" rows="4"></textarea>`




====

[1]: http://es.wikipedia.org/wiki/HTML "HTML en Wikipedia.org"