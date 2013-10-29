HTML
====

HTML kijtosneki HyperText Markup Language (koyolkopa «lenguaje de marcas de hipertexto»), tech palehuia maj tik chihuaka amat taijkitil. Tech ilia keniuj tik chihuaskese amat taikitil, toni ki huika uan yin ki tokaytia "código" (tein no kilia "código HTML") tech to amat taijkitil huelis ki huikas tajkuilol, amaixyekauilmej. Tein ki ixyekana monotsa W3C, yin nechikol tein kichiua kinintayekana nochime tein kineki kichiuaske teisa tein kipia ki kitas web, mas keniuj ki ijkuiloske uan keniuj mo nextia.
										Yin HTML mo tsintalia nejin ki tokaytia "referenciación". Ton kijtoskeni ke si tik neki tik talilis se amaixyekauil, videotl, "script", yin amo yuuik tech yin "código" de to amat taijkitil, sino sayo ti kilia de kani kikuis. Yin kijtosneki ke to amat taijkitil sayo kipia tajkuilol maj monexti ton tikchiujke yin tekit de nejin taixnextiloni (interpretador del código) ni tekit kinin salohua nochi tein tichiujke uan tech nextilia keniuj mokahuak. Onkake miak taixnextilonime, nejin HTML ni tekit ke hueli tikiuis taixnextiloni tein mas tik huelitas uan huelis tikitas maski tikuis okse taixnextiloni.[1]

Yin HTMl huelis tik chihuas uan tik yek chihuas ika se "editor de textos" kemej tin ki tokaytia "bloc de notas" tech "Windows" o no "Gedit" tech yin "Linux" onkake okseki miak tama "editor de textos" tein huelis tikuis.

====

###Etiquetas



Nejin ki tokaytia "etiquetas" no "marcas" tech ilia kani pehua uan kani tami to amat taijkitil; kipia ome 

*Tein ki tapohua:*  `<etiqueta>`

*Tein ki tsakua:* `</etiqueta>`

Nochi tein tik talilia "etiquetas" hueli kipias seki "atributos" tein ki palehuia keniuj muitas.

`<etiqueta atributo1="valor" atributo2="valor"></etiqueta>`

Nochi tein tik taliliske nejin "etiquetas" ki chihuas maj mo pata . Nika tikpia keniuj muitas:

`<b>Yin tajtol etok tiltik</b>`

Yin "etiquetas" `<b></b>` ki talia tajtol tiltika. Keniuj tikitaske yetok nika tani:

__Yin tajtol etok tiltik__

No kipia tikitaske tech to amat HTML maj kipia `<html>/<html>`. Taijtik nejin kipia mo kotonaj en ome:
										
*El encabezado*, tein se kitalia ika  `<head></head>` nika tik talia "etiquetas" "informativas" kemj keniuj monotsas to amat taijkitil.

*El cuerpo*, tein se kitalia ika `<body></body>`, nika kiuika tajtol, amaixyekauilmej, uan okseki tamamej tein kiuika to amat taijkitil.

Tik piajya, keniuj tik chiuaske se amat HTML ika ni tokay.

```html
<html>
  <head>
    <title>Mi sitio web</title>
  </head>
  <body></body>
</html>
```

###Tajtol

Tajtol ulis tik taliske kampa tik nekiske taijtik nejin "etiqueta body" uan nejin muitas tech to amat; no ueli tik taliliske keniuj muitas, ton tanto hueyi.

Tein telsenka se kikuik nejin ki tokaytia "párrafos". Nejin "párrafos" kualtiaj maj muita kuali nejin tajtol uan kipiaj okseki "propiedades". Maj uelis tikuiske tikpia nejin "etiqueta" `<p> </p>`. Kipia timitsiliske keman ti tajkuilostos uan tik nekis maj ki sentoka tani amo tikuij yin "tecla" *Enter*. Maj uelis tik panoske tani tikuij yin "etiqueta" `<br>`.

__Maj tikitaka keniuj:__

```html
<html>
  <head>
    <title>Mi sitio web</title>
  </head>
  <body>
  	<p>Yin se "párrafo".</p>
  	<p>Yin okse "parráfo" <br> uan yin mojkuiloua tani</p>
  </body>
</html>
```

Tajtol tein kipia se amat HTML ulis kipias miak tamamej. Yin tamamej ueli tik taliske ika seki "etiquetas" no ika yin ki tokaytia [hojas de estilo (CSS).](04 Hojas de estilo/Hojas de estilo.md)
 
```html
<html>
  <head>
    <title>Mi sitio web</title>
  </head>
  <body>
  	<p>Yin se "párrafo" <b>ika tajtol tiltik</b>.</p>
  	<p>Yin okse "parráfo" <i>ika tajtol matajkuilol</i></p>
  </body>
</html>
```

No ueli tik yektaliske tajtol, keniuj muitas uan no ton tanto hueyi muitas yin ueli tik chiuaske taijtik nejin "etiquetas". 

```html
  	<p align="center">Yin "parráfo" etok tatajko.</p>
  	<p color="#83b81a">Yin "parráfo" kipia se tapal</p>
```

__Xi kelnamiki:__ Miak nejin "propiedades" tein kipia amamej HTML, se kichiuak itech nekin mo tokaytia "hojas de estilo" kasi amo mokui kemej "atributos". 

###Encabezados

Neij "encabezados" tech maka miak matekilis maj tik neshtika de toni tik tajtoua.

Onkake chikuase tamaj "encabezados" HTML uan se kininkijkuiloua  `<h1></h1>`, `<h2></h2>`, `<h3></h3>`, `<h4></h4>`, `<h5></h5>` y `<h6></h6>`. 

```html
  <h1>Encabezado nivel 1</h1>
  <h2>Encabezado nivel 2</h2>
  <h3>Encabezado nivel 3</h3>
  <h4>Encabezado nivel 4</h4>
  <h5>Encabezado nivel 5</h5>
  <h6>Encabezado nivel 6</h6>
```

###Listas

HTML tech maka seki tamaj maj tik talika yin tanojnotsalis. Nejin "listas" kipias tajkuilolis kemej:

* Tanojnotsalis tein amo yektalijtok.
* Tanojnotsalis tein yektalijtok.
* "Definiciones."

###Enlaces

Se hiperenlace, hipervínculo o vínculo, tech huika okse amat taijkitil.

Tajtol o nejin amaixyekauilme tein kipia se "enlace" kipia etoske taijtik nejin "etiquetas" `<a></a>`.

Nejin `href` tech ilia kani tech huikas nejin "enlace".

Maj tikitak keniuj se kichiua, tik chiuati se "enlace" tein tech huikas "Wikipedia", tikpia tik taliske nejin "código".

```
  Este es un enlace a <a href="http://wikipedia.org">Wikipedia</a>
```

###Amaixyekauilmej

Tein mas mokui tech nejin amataijkitil uan tein kichiua maj kuali muita to amat  ti takaytiti amaixyekauilmej. 

Maj tiktalika se amaixyekauil tik kuiti nejin "etiqueta" `<img>`. Nejin "etiqueta" amo motsakua kemej nokseki tein tikitakejya, sayo tikilia de kani tikuiti neji amaixyekauil ikan nejin "atributo" `src`. Maj tikitak kenuij:

```html
  <img src="images/photo.jpg" >
```

###Formularios

Yin kitokaytia "formulario" tehc paleuia maj tik kixtika "datos" tein kitaliaj tein kikui to amataijkitil.

Nejin "formularios" mokuij keman tikneki tikixmatiske toni tanemilia nokseki, si kineki tajtaniske teisa uan okseki "datos" tein kikuij mo amataijkitil.

Se "formulario" kipia "etiquetas, campos de texto, menús y botones".

Maj tik talika se "formulario" tech to amat HTML tikuij "etiquetas" `<form> </form>` uan taijtik tik talilia "elementos" nejin "formulario".

"Atributos" tein se kinikuik monotsa: `action` y `method`. Se techilia kani yaske nejin "datos"; uan nokse techilia keniuj yas yin tanojnotsalis. 

```html
	<form action="proceso.php" method="POST">
	...
	</form>
```

__Elementos de entrada__

Nejin kitokaytia campos de texto (input) kikuij "etiqueta" `<input >`. Atributos tein kikuik `name` y `type`.

Onkake miak tama "inputs" kemej `email` (correo), `text` (texto) o `password` (contraseña).

```html
	<form action="proceso.php" method="POST">
	  <input name="nombre" type="text" >
	  <input name="contrasenia" type="password" >
	  <input name="correo" type="email" >
	</form>
```

__Casilla de verificación__

Maj tiktalika nejin kitokaytia "casilla de verificación", kipia tiliske nejin valor `checkbox` al atributo `type` tech se elemento `<input>`.

`<input name="casilla" type="checkbox" checked >`

__Botón de opción__

Nejin kitokaytia "botones de opción" kihuika valor `radio` itech "atributo" `type`.

```html
<input nombre="opcion1" type="radio" checked>
<input nombre="opcion2" type="radio" >
```

__Campos de selección__


Si se requiere insertar un menú o una lista desplegable dentro de un formulario se puede incluir un campo de selección, a través de las etiquetas `<select> </select>`. El atributo `name` indica el nombre, el atributo `multiple` indica que se pueden seleccionar varios elementos. 

Los elementos que conforman la lista son instertados entre las etiquetas `<option></option>` y se se quiere mostrar una opción seleccionada por defecto se utiliza el atributo `selected`.

```html
  <select name="opciones">
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
