Tipo de selectores CSS.
=============================

Nejin kitokaytia "selectores" mokuij miak maj kuali se kikuij nejin kitokaytia "estilos CSS" tech to amataijkitil.

Tech se "elemento HTML"  se hueli kitalilia miak "reglas CSS" uan se nejin "regla CSS" hueli se kitalilia miak "elementos". Tein kijtosneki, se "regla" hueli se kitalilis a miak nejin "selectores" uan se "selector" huelis kikuis miak "reglas".

##Selector universal

Ikan nejin huelis se kitalilis nochimej "elementos" nejin to amataijkitil. Maj tikitaka keniuj se ki kixtilia "margen" uan "relleno" nochimej nejin "elementos HTML":

```css
* {
  margin: 0;
  padding: 0;
}
```

```
* --> Ikan nejin tajtol tikixmatiske "selector universal"
```

Nejin "selector universal" se kijkuiloua ika se "asterisco" (*). Kasi amo mokui, uan tejua no amo tikuiske.

##Selector de tipo o etiqueta

Nejin mokui keman nejin "etiqueta HTML" motokaytia kemej nejin "selector". Maj tikitaka keniuj se kikui:

```css
p {
  margin: 0;
}
```

```
p --> Tech "CSS" uan no tech nejin HTML mokui nejin "etiqueta" <p>
```

Keniuj maj se kikui nejin "selector", sayo tik kijkuiloua kemej nejin "etiqueta HTML" (uan amo tikitalilia < uan >).

Si tikneki tiktaliske nejin "estilos" techo ome "etiquetas", hueli tikin sentaliske nejin "selectores". Maj tikitaka keniuj tikin sentaliske h1, h2 y h3 tein kipiaj nejin "estilos":

```css
h1 {
  color: #8A8E27;
  font-weight: normal;
  font-family: Arial, Helvetica, sans-serif;
}

h2 {
  color: #8A8E27;
  font-weight: normal;
  font-family: Arial, Helvetica, sans-serif;
}

h3 {
  color: #8A8E27;
  font-weight: normal;
  font-family: Arial, Helvetica, sans-serif;
}
```

Kemej tikita, huelis tikin sentaliske. Sayo tikintalilia se "coma" (,) uan ijko muitas si tikin sentalia:

```css
h1, h2, h3 {
  color: #8A8E27;
  font-weight: normal;
  font-family: Arial, Helvetica, sans-serif;
}
```

##Selector descendente

Yin kualtia keman tikneki nejin "elementos" tein etoke taijtik de okseki "elementos". Se "elemento" kilia "descendiente" keman etok ikan yin "etiquetas" tein tapoua uan tein tsakua se "elemento". Maj tikitaka keniuj ikan yin "elemento" ```<span>``` de la página que se encuentren dentro de un elemento ```<p>```:

```css
p span {
 color: red;
}
```

Si el código HTML de la página es el siguiente:

```html
<p>
  <span>Texto en color rojo</span>
</p>
```

Los selectores descendentes permiten aumentar la precisión del selector de tipo o etiqueta. Así, utilizando el selector descendente es posible aplicar diferentes estilos a los elementos del mismo tipo. El siguiente ejemplo muestra de color azul todo el texto de los ```<span>``` contenidos dentro de un ```<h1>```:

```css
p span {
 color: red;
}

h1 span {
 color: blue;
}
```

Con las reglas CSS anteriores:

- Los elementos ```<span>``` que se encuentran dentro de un elemento ```<p>``` se muestran de color rojo.
- Los elementos ```<span>``` que se encuentran dentro de un elemento ```<h1>``` se muestran de color azul.
- El resto de elementos ```<span>``` de la página, se muestran con el color por defecto aplicado por el navegador.

##Selector de clase

Consiste en utilizar el atributo *class* de HTML sobre ese elemento para indicar directamente la regla CSS que se le debe aplicar:

```html
<body>
 <p class="destacado">Este párrafo diferente a todos</p>
 <p>Párrafo normal</p>
 <p>Párrafo normal dos</p>
</body>
```

Para que el navegador no confunda este selector con los otros tipos de selectores, se prefija el valor del atributo *class* con un punto (.) tal y como muestra el siguiente ejemplo:

```css
.destacado {
 color: red;
}
```
El selector *.destacado* se interpreta como "cualquier elemento de la página cuyo atributo *class* sea igual a *destacado*", por lo que solamente el primer párrafo cumple esa condición.

En ocasiones, es necesario restringir el alcance del selector de clase:

```html
<body>
 <p class="destacado">Párrafo con la clase destacado</p>
 <p>Inicio de un párrafo <a href="#" class="destacado">link con la clase destacado dentro de un párrafo</a> fin del párrafo</p>
 <p>Inicio de un párrafo <em class="destacado">itálica con la clase destacado dentro de un párrafo</em> fin del párrafo</p>
</body>
```

Para aplicar estilos solamente al párrafo cuyo atributo *class* sea igual a *destacado*, es necesario combinar el selector de tipo y el selector de clase, así se obtiene un selector mucho más específico:

```css
p.destacado {
 color: red
}
```

El selector *p.destacado* se interpreta como "aquellos elementos de tipo ```<p>``` que dispongan de un atributo *class* con valor *destacado*". De la misma forma, el selector *a.destacado* solamente selecciona los enlaces cuyo atributo *class* sea igual a *destacado*.

No debe confundirse el selector de clase con los selectores anteriores:

```css
/* Todos los elementos de tipo "p" con atributo class="aviso" */
p.aviso { ... }
 
/* Todos los elementos con atributo class="aviso" que estén dentro de cualquier elemento de tipo "p" */
p .aviso { ... }
 
/* Todos los elementos "p" de la página y todos los elementos con atributo class="aviso" de la página */
p, .aviso { ... }
```

Además es posible aplicar los estilos de varias clases CSS sobre un mismo elemento. La sintaxis es similar, pero los diferentes valores del atributo *class* se separan con espacios en blanco. En el siguiente ejemplo:

```css
<p class="especial destacado error">Párrafo de texto...</p>
```

Al párrafo anterior se le aplican los estilos definidos en las reglas *.especial*, *.destacado* y *.error*, por lo que en el siguiente ejemplo, el texto del párrafo se vería de color rojo, en negrita y con un tamaño de letra de 15 píxel:

```css
.error {
 color: red; 
}

.destacado {
 font-size: 15px;
}

.especial {
 font-weight: bold;
}
```

##Selectores de ID

En ocasiones, es necesario aplicar estilos CSS a un único elemento de la página. Aunque puede utilizarse un selector de clase para aplicar estilos a un único elemento, existe otro selector más eficiente en este caso.

El selector de ID permite seleccionar un elemento de la página a través del valor de su atributo *id*. Este tipo de selectores sólo seleccionan un elemento de la página porque el valor del atributo *id* no se puede repetir en dos elementos diferentes de una misma página.

La sintaxis de los selectores de ID es muy parecida a la de los selectores de clase, salvo que se utiliza el símbolo de la almohadilla (#) en vez del punto (.) como prefijo del nombre de la regla CSS:

```css
#destacado {
 color: red;
}
```

```html
<p>Primer párrafo</p>
<p id="destacado">Segundo párrafo</p>
<p>Tercer párrafo</p>
```

En el ejemplo anterior, el selector *#destacado* solamente selecciona el segundo párrafo (cuyo atributo *id* es igual a *destacado*).

La principal diferencia entre este tipo de selector y el selector de clase tiene que ver con HTML y no con CSS. Como se sabe, en una misma página, el valor del atributo *id* debe ser único, de forma que dos elementos diferentes no pueden tener el mismo valor de *id*. Sin embargo, el atributo *class* no es obligatorio que sea único, de forma que muchos elementos HTML diferentes pueden compartir el mismo valor para su atributo *class*.

##Combinación de selectores básicos

CSS permite la combinación de uno o más tipos de selectores para restringir el alcance de las reglas CSS. A continuación se muestran algunos ejemplos habituales de combinación de selectores.

```css
.aviso .especial { ... }
```

El anterior selector solamente selecciona aquellos elementos con un *class="especial"* que se encuentren dentro de cualquier elemento con un *class="aviso"*.

Si se modifica el anterior selector:

```css
div.aviso span.especial { ... }
```

Ahora, el selector solamente selecciona aquellos elementos de tipo ```<span>``` con un atributo *class="especial"* que estén dentro de cualquier elemento de tipo ```<div>``` que tenga un atributo *class="aviso"*.

La combinación de selectores puede llegar a ser todo lo compleja que sea necesario:

```css
ul#menuPrincipal li.destacado a#inicio { ... }
```

El anterior selector hace referencia al *enlace* con un atributo *id* igual a *inicio* que se encuentra dentro de un elemento de tipo ```<li>``` con un atributo *class* igual a *destacado*, que forma parte de una lista ```<ul>``` con un atributo *id* igual a *menuPrincipal*.

##Selector de hijos

Se trata de un selector similar al *selector descendente*, pero muy diferente en su funcionamiento. Se utiliza para seleccionar un elemento que es hijo directo de otro elemento y se indica mediante el "signo de mayor que" (>):

```css
p > span {
  color: blue;
}
```
```html
<p><span>Texto...</span></p>
<p><a href="#"><span>Texto...</span></a></p>
```

En el ejemplo anterior, el selector ```p > span``` se interpreta como "cualquier elemento ```<span>``` que sea hijo directo de un elemento ```<p>```", por lo que el primer elemento ```<span>``` cumple la condición del selector. Sin embargo, el segundo elemento ```<span>``` no la cumple porque es descendiente pero no es hijo directo de un elemento ```<p>```.

El siguiente ejemplo muestra las diferencias entre el selector descendente y el selector de hijos:

```css
p a {
  color: red;
}

p > a {
  color: blue;
}
```
```html
<p><a href="#">Enlace1...</a></p>
<p><span><a href="#">Enlace2...</a></span></p>
```

El primer selector es de tipo *descendente* y por tanto se aplica a todos los elementos ```<a>``` que se encuentran dentro de elementos ```<p>```. En este caso, los estilos de este selector se aplican a los dos enlaces.

Por otra parte, el selector de hijos obliga a que el elemento ```<a>``` sea hijo directo de un elemento ```<p>```. Por lo tanto, los estilos del selector ```p > a``` no se aplican al segundo enlace del ejemplo anterior.

##Selector adyacente

El selector adyacente se emplea para seleccionar elementos que en el código HTML de la página se encuentran justo a continuación de otros elementos. Su sintaxis emplea el signo ```+``` para separar los dos elementos:

```css
elemento1 + elemento2 { ... }
```

Si se considera el siguiente código HTML:

```html
<body>
  <h1>Titulo1</h1>
  <h2>Subtítulo</h2>
  <h2>Otro subtítulo</h2>
</body>
```

La página anterior dispone de dos elementos ```<h2>```, pero sólo uno de ellos se encuentra inmediatamente después del elemento ```<h1>```. Si se quiere aplicar diferentes colores en función de esta circunstancia, el *selector adyacente* es el más adecuado:

```css
h2 {
  color: green;
}

h1 + h2 {
  color: red;
}
```

Las reglas CSS anteriores hacen que todos los ```<h2>``` de la página se vean de color verde, salvo aquellos ```<h2>``` que se encuentran inmediatamente después de cualquier elemento ```<h1>``` y que se muestran de color rojo.

Técnicamente, los elementos que forman el *selector adyacente* deben cumplir las dos siguientes condiciones:

- *elemento1* y *elemento2* deben ser elementos hermanos, por lo que su elemento padre debe ser el mismo.
- *elemento2* debe aparecer inmediatamente después de *elemento1* en el código HTML de la página.

El siguiente ejemplo es muy útil para los textos que se muestran como libros:

```css
p + p {
  text-indent: 1.5em;
}
```

En muchos libros, suele ser habitual que la primera línea de todos los párrafos esté indentada, salvo la primera línea del primer párrafo. Con el selector ```p + p```, se seleccionan todos los párrafos de la página que estén precedidos por otro párrafo, por lo que no se aplica al primer párrafo de la página.

##Selector de atributos

El último tipo de selectores avanzados lo forman los *selectores de atributos*, que permiten seleccionar elementos HTML en función de sus atributos y/o valores de esos atributos.

Los cuatro tipos de selectores de atributos son:

- [nombre_atributo], selecciona los elementos que tienen establecido el atributo llamado *nombre_atributo*, independientemente de su *valor*.
- [nombre_atributo=valor], selecciona los elementos que tienen establecido un atributo llamado *nombre_atributo* con un *valor* igual a *valor*.
- [nombre_atributo~=valor], selecciona los elementos que tienen establecido un atributo llamado *nombre_atributo* y al menos uno de los valores del atributo es *valor*.
- [nombre_atributo|=valor], selecciona los elementos que tienen establecido un atributo llamado *nombre_atributo* y cuyo valor es una serie de palabras separadas con guiones, pero que comienza con *valor*. Este tipo de selector sólo es útil para los atributos de tipo *lang* que indican el idioma del contenido del elemento.

A continuación se muestran algunos ejemplos de estos tipos de selectores:

```css
/* Se muestran de color azul todos los enlaces que tengan un atributo "class", independientemente de su valor */
a[class] {
  color: blue;
}
 
/* Se muestran de color azul todos los enlaces que tengan un atributo "class" con el valor "externo" */
a[class="externo"] {
  color: blue;
}
 
/* Se muestran de color azul todos los enlaces que apunten al sitio "http://www.ejemplo.com" */
a[href="http://www.ejemplo.com"] {
  color: blue;
}
 
/* Se muestran de color azul todos los enlaces que tengan un atributo "class" en el que al menos uno de sus valores sea "externo" */
a[class~="externo"] {
  color: blue;
}
 
/* Selecciona todos los elementos de la página cuyo atributo "lang" sea igual a "en", es decir, todos los elementos en inglés */
*[lang=en] { ... }
 
/* Selecciona todos los elementos de la página cuyo atributo "lang" empiece por "es", es decir, "es", "es-ES", "es-AR", etc. */
*[lang|="es"] {
  color: red;
}
```
