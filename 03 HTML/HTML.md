HTML
====

HTML kijtosneki HyperText Markup Language (koyolkopa «lenguaje de marcas de hipertexto»), tech palehuia maj tik chihuaka amat taijkitil. Tech ilia keniuj tik chihuaskese amat taikitil, toni ki huika uan yin ki tokaytia "código" (tein no kilia "código HTML") tech to amat taijkitil huelis ki huikas tajkuilol, amaixyekauilmej. Tein ki ixyekana monotsa W3C, yin nechikol tein kichiua kinintayekana nochime tein kineki kichiuaske teisa tein kipia ki kitas web, mas keniuj ki ijkuiloske uan keniuj mo nextia.
										Yin HTML mo tsintalia nejin ki tokaytia "referenciación". Ton kijtoskeni ke si tik neki tik talilis se amaixyekauil, videotl, "script", yin amo yuuik tech yin "código" de to amat taijkitil, sino sayo ti kilia de kani kikuis. Yin kijtosneki ke to amat taijkitil sayo kipia tajkuilol maj monexti ton tikchiujke yin tekit de nejin taixnextiloni (interpretador del código) ni tekit kinin salohua nochi tein tichiujke uan tech nextilia keniuj mokahuak. Onkake miak taixnextilonime, nejin HTML ni tekit ke hueli tikiuis taixnextiloni tein mas tik huelitas uan huelis tikitas maski tikuis okse taixnextiloni.[1]

Yin HTMl huelis tik chihuas uan tik yek chihuas ika se "editor e textos" kemej tin ki tokaytia "bloc de notas" tech "Windows" o no "Gedit" tech yin "Linux" onkake okseki miak tama "editor de textos" tein huelis tikuis.

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

```html
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

```html
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
 
```html
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

```html
  	<p align="center">Este es un párrafo centrado.</p>
  	<p color="#83b81a">Este párrafo tiene un color específico</p>
```

__Importante:__ Muchas de las propiedades que tienen los documentos HTML, son establecidas mediante hojas de estilo por lo que incluirlas como atributos es poco común hoy en día. 

###Encabezados

Los encabezados nos proporcionan una valiosa herrmamienta para destacar temas importantes y títulos así como destacar la naturaleza del documento en conjunto.

Hay seis niveles de encabezados en HTML especificados por las etiquetas `<h1></h1>`, `<h2></h2>`, `<h3></h3>`, `<h4></h4>`, `<h5></h5>` y `<h6></h6>`. 

```html
  <h1>Encabezado nivel 1</h1>
  <h2>Encabezado nivel 2</h2>
  <h3>Encabezado nivel 3</h3>
  <h4>Encabezado nivel 4</h4>
  <h5>Encabezado nivel 5</h5>
  <h6>Encabezado nivel 6</h6>
```

###Listas

HTML ofrece varios mecanismos para especificar listas de información. Todas las listas deben contener uno o más objetos. Las listas pueden contener:

* Información no ordenada.
* Información ordenada.
* Definiciones.

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

```html
  <img src="images/photo.jpg" >
```

###Formularios

Un formulario es un elemento que permite recoger datos introducidos por el usuario.

Los formularios se utilizan para conocer las opiniones, dudas y otra serie de datos sobre los usuarios.

Un formulario está formado, entre otras cosas, por etiquetas, campos de texto, menús y botones.

Para insertar un formulario en un documento HTML se utilizan las etiquetas `<form> </form>` y dentro de ellas se agregan los elementos que formarán dicho formulario.

Los atributos más comunes en el uso de formularios son: `action` y `method`. El primero indica una dirección a la cual se enviarán los datos; la segunda indica el método en que será cifrada la información para su envío. 

```html
	<form action="proceso.php" method="POST">
	...
	</form>
```

__Elementos de entrada__

Los campos de texto (input) utilizan la etiqueta `<input >`. Los atributos más comunes son `name` y `type`.

Hay muchos tipos diferentes de "inputs" como `email` (correo), `text` (texto) o `password` (contraseña).

```html
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

```html
<input nombre="opcion1" type="radio" checked>
<input nombre="opcion2" type="radio" >
```

__Campos de selección__


Si se requiere insertar un menú o una lista desplegable dentro de un formulario se puede incluir un campo de selección, a través de las etiquetas `<select> </select>`. El atributo `name` indica el nombre, el atributo `multiple` indica que se pueden seleccionar varios elementos. 

Los elementos que conforman la lista son instertados entre las etiquetas `<option></option>` y se se quiere mostrar una opción seleccionada por defecto se utiliza el atributo `selected`.

```html
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


###Audio y video

Las nuevas especificaciones de HTML5 incluyen etiquetas que nos permiten integrar contenidos miultimedia sin necesidad de complementos del navegador donde se ve el documento, las etiquetas `<video>` y `<audio>` sirven para integrar video y audio en las páginas web de la misma forma en que se insertan imágenes con la etiqueta `<img>`.

Para incrustar un video dentro de la página web se puede hacer de la siguiente manera:

`<video src="video.mp4" width="400" height="300"></video>`.

De manera similar, agregar un archivo de audio podría realizarse así:

`<audio src="audio.mp3" controls></audio>`

El atributo `controls` le indica al navegador que incluya los controles para reproducir, pausar y adelantar la pista si es el caso.

###Dibujo y animación

La etiqueta `<canvas>` dota al lenguale HTML de un formato nativo para el dibujo y la animación. Esta plataforma puede ser una alternativa para los gráficos y animaciones que al día de hoy podemor ver en películas Flash.

El elemento `canvas` funciona a modo de superficie de dibujo dentro de una página web (de ahí el nombre). Dentro de esta superficie podemos crar formas con colores, gradientes y patrones de relleno, mostrar texto y exportar los contenidos hacia archivos de imagen estática como `.png`. Podemos utilizar javaScript o las nuevas funciones de animación en CSS para que los objtos que creamos puedan moverse, desaparecer, cambiar de tamaño, etcétera.

Para incorporar un elemento `canvas` se utiliza las etiquetas `<canvas> </canvas>`.

`<canvas id="dibujo"></canvas>`.

La funcionalidad se puede añadir con [código JavaScript.](05 JavaScript/JavaScript.md).

```html
<html>
  <head>
    <title>Mi sitio web</title>
  </head>
  <body>
  	<canvas id="dibujo"></canvas>
  	
  	<script>
		var canvas = document.getElementById("dibujo"),
		context = canvas.getContext("2d");
		context.fillRect(10, 20, 200. 100);
	</script>
  </body>
</html>
```


El código anterior dibuja un rectángulo con color (mediante el método `fillRect`) de un tamaño y una posición determinados (por medio de los argumentos del mismo método).

###Etiquetas semánticas

Las etiquetas semánticas representan bloques enteros que agrupan a otros elementos HTML y que permiten una mejor división del contenido y por ende una mejor semántica.

__div__

Los elementos `div` representan capas generéricas que se incluyen con las etiquetas `<div> </div>` en nuestra página HTML. 

```html
<html>
  <head>
    <title>Mi sitio web</title>
  </head>
  <body>
  	<div>
  	 ...
  	</div>
  </body>
</html>
```

__header__

Este elemento nos permite identificar la cabecera de la página. Típicamente, dentro de este elemento se colocan el logotipo y nombre de la empresa, el menú de navegación, etcétera. Para incrustar un elemento `header` en nuestra página, se deben utilizar las etiquetas `<header></header>`.

```html
<body>
  	<header>
		contenido del header
  	</header>
</body>
```

__footer__

Las etiquetas `<footer></footer>` definen el 'pie' de una página. El pie de una página web por lo regular contiene información sobre su autor, derechos de autor, enlaces a términos de uso, contacto, etcétera.

```html
<body>
    ...
  	<footer>
		contenido del footer
  	</footer>
</body>
```

__nav__


El elemento `nav` define los enlaces de navegación dentro de un sitio web.

Se debe de tomar en cuenta que no todos los enlaces deben de estar dentro del elemento `nav` sino solo los más importantes o que contengan más información.

```html
<body>
  	<nav>
		aquí puede ir el menú de navegación
  	</nav>
</body>
```

__section__


Como su nombre lo indica, el elemento `section` define secciones dentro de las páginas web como capítulos, encabezados, etcétera. Las secciones se definen con las etiquetas `<section></section>`.


```html
<html>
  <head>
    <title>Mi sitio web</title>
  </head>
  <body>
  	<section>
  	  el contenido de la sección
  	</section>
  </body>
</html>
```

__article__

El elemento `article` representa un componente independiente y autocontenido de una página web. Puede presentar un artículo, artículo de opinión, una entrada de un blog, etcétera.



```html
<html>
  <head>
    <title>Mi sitio web</title>
  </head>
  <body>
  	<article>
  	  el contenido del articulo
  	</article>
  </body>
</html>
```


__aside__

El elemento `aside` representa una sección de una página que tiene relación con el contenido que está mostrando una página web y que podría ser considerado por separado de ese contenido. Estas secciones a menudo representado como barras laterales y también llamadas 'sidebar'.

```html
<html>
  <head>
    <title>Mi sitio web</title>
  </head>
  <body>
  	<aside>
  	  contenido del aside.
  	</aside>
  </body>
</html>
```



====

[1]: http://es.wikipedia.org/wiki/HTML "HTML en Wikipedia.org"
