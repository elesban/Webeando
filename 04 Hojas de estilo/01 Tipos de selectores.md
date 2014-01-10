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

Yin kualtia keman tikneki nejin "elementos" tein etoke taijtik de okseki "elementos". Se "elemento" kilia "descendiente" keman etok ikan yin "etiquetas" tein tapoua uan tein tsakua se "elemento". Maj tikitaka keniuj ikan yin "elemento" ```<span>``` tein etok taijtik nejin "elemento" ```<p>```:

```css
p span {
 color: red;
}
```

Uan tik piaj tech to "código HTML":

```html
<p>
  <span>Texto en color rojo</span>
</p>
```

Yin ki tokaytiaj "selectores descendentes" tech paleuia ika nejin ki tokaytiaj "selector de tipo o etiqueta". Keman tikuij yin "selector descendente" uel tik taliliske miak tamaj "estilos" tech se "elemento". Maj tikitak keniuj yin tajtol muita iluitik tech yin ```<span>``` tein yetok taijtik nejin ```<h1>```:

```css
p span {
 color: red;
}

h1 span {
 color: blue;
}
```

Ikan yin "reglas CSS" tikitaj :

- Yin "elementos" ```<span>``` tein etokej taijtik nejin "elemento" ```<p>``` se kita chichiltik.
- Yin "elementos" ```<span>``` tein etokej taijtik nejin "elemento" ```<h1>``` se kita iluitik.
- Nokseki "elementos" ```<span>``` muitaj ika se tapal kemej ki nextia yin amataijkitil.

##Selector de clase

Se kitalilia se "atributo" *class* de nejin "HTML" tech se "elemento":

```html
<body>
 <p class="destacado">Este párrafo diferente a todos</p>
 <p>Párrafo normal</p>
 <p>Párrafo normal dos</p>
</body>
```

Yin "atributo" *class* se kitalia ika se "punto" (.) ijko tik ke tikuijtoke se "selector de clase" kemej tikitaj nika:

```css
.destacado {
 color: red;
}
```
Yin "selector" *.destacado* tein kijtosneki  " se "elemento" tech yin amataijkitl tein kipia yin atributo *class* ika yin tokay *destacado*", kemej tikita sayo se "parráfo" kipia yin "atributo".

Satepa, keman tik nekiske sayo tik taliske amo nochi tech se "párrafo" uelis tik chiuaske kemej miuta nika:

```html
<body>
 <p class="destacado">Párrafo con la clase destacado</p>
 <p>Inicio de un párrafo <a href="#" class="destacado">link con la clase destacado dentro de un párrafo</a> fin del párrafo</p>
 <p>Inicio de un párrafo <em class="destacado">itálica con la clase destacado dentro de un párrafo</em> fin del párrafo</p>
</body>
```

Keman tik nekiske sayo tein kipia yin "atributo" *class* tein motokaytia *destacado*, tikpia tik kuiske se "selector de tipo" uan se "selector de clase", kemej muita nika:

```css
p.destacado {
 color: red
}
```

Yin "selector" *p.destacado* tein kijtosneki "nochime "elementos" ```<p>``` tein kipiaj se atributo *class* ikan tokay  *destacado*". No ijko, yin "selector" *a.destacado* kikui tein kipiaj  se "atributo" *class* ikan tokay *destacado*.

Tikpia tik matiske ton kichuaj nochimej yin "selectores":

```css
/* Todos los elementos de tipo "p" con atributo class="aviso" */
p.aviso { ... }
 
/* Todos los elementos con atributo class="aviso" que estén dentro de cualquier elemento de tipo "p" */
p .aviso { ... }
 
/* Todos los elementos "p" de la página y todos los elementos con atributo class="aviso" de la página */
p, .aviso { ... }
```

No ulis ti kuiske miak tamaj nejin "estilos"  itche miak tamaj nejin "clases CSS" itech se "elemento". Maj tikitaka keniuj se kijkuiloua ikan yin "atributo" *class*:

```css
<p class="especial destacado error">Párrafo de texto...</p>
```

Yin "párrafo" kipia miak "estilos" tech yin "reglas" *.especial*, *.destacado* y *.error*, kemej nika muita:

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

Satepa, keman tiknekiske tik taliske se "estilos CSS" a sayo se "elemento" tech to amataijkitil. Uel tikuiske yin kitokaytia "selector de ID".

Yin "selector de ID" tech paleuia keman sayo tik neki tik pataske se "elemento" de to amataijkitil ikan ni "atributo" *id*. Yin "selectores" sayo mokui sayo sepa tech se "elemento" ika "atributo" *id* uan amo uel se kikui sepa tech okse "elemento" tech to amataijkitil.

Keman se kikui se "selector de ID" se kijkuiloua ika se "almohadilla" (#) kemej muita nika:

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

Kemej tikita, tech "selector" *#destacado* sayo kipata  tein kipia yin "atributo" *id* tein motokaytia  *destacado*.

Keniuj tikmati keman tikuiske se "selector de ID" uan se "selector de clase" yin te chiluia "HTML" uan amo "CSS". Keman se kikui se "atributo" *id* tech se "elemento" amo uel se kikui ojpa sayo sepatsi, yin kijtosneki ke ome "elementos" amo uel kipiaske *id* ikan mismmo tokay. Keman se kikui yin "atributo" *class* uel tikuiske miakpa tech se "elemento", miak "elementos HTML" uel kikuiske yin mismo "atributo" *class*.

##Combinación de selectores básicos

CSS tech kaua maj tikuika se o mas "tipos de selectores". Maj tikitaka keniuj se kikui.

```css
.aviso .especial { ... }
```

Kemej tikita yin sayo kualtia ika nochime "elementos" tein kipia se *class="especial"* tein etok taijtik tech se  *class="aviso"*.

Maj tikpataka yin "selector":

```css
div.aviso span.especial { ... }
```

Ekintsi yin "selector" kualtiak sayo ika nochime "elementos" tein kipiaj se ```<span>``` ika se "atributo" *class="especial"* tein etok taijtik tech se "elemento" ```<div>``` tein kipia se "atributo" *class="aviso"*.

Uel tik piaske miak "selectores" kemej tikitaj nika:

```css
ul#menuPrincipal li.destacado a#inicio { ... }
```

Yin "selector" kikui se *enlace* ika se "atributo" *id* tein motokaytia *inicio* tein etok taijtik tech se "elemento" ```<li>``` ika se "atributo" *class* tein motokaytia *destacado*, tein etok tech se "lista" ```<ul>``` ika se "atributo" *id* tein motokaytia *menuPrincipal*.

##Selector de hijos

Muita kemej se *selector descendente*, sayo ke amo tekiti kemej yin tekiti. Mokui keman tikpia se "elemento" tein kitojtoka okse "elemento" uan se kinextia ika "signo de mayor que" (>):

```css
p > span {
  color: blue;
}
```
```html
<p><span>Texto...</span></p>
<p><a href="#"><span>Texto...</span></a></p>
```

Kemej tikita yin "selector" ```p > span``` tein kijtosneki "se "elemento" ```<span>``` tein ki tojtoka nejin "elemento" ```<p>```", Nejin "elemento" ```<span>``` kemaj mo pata ikan yin "selector". Noske tein kitojtoka noske "elemento" ```<span>``` amo mo pata.

Maj tikitaka keniuj tekiti yin "selector descendente" uan "selector de hijos":

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

Tein achto yetok se "selector" *descendente* uan ueli tikitaj tech "elementos" tein achto etoj yin ```<a>``` tein etok taijtik nejin "elementos" ```<p>```. Kemej tikita mo nextiske tapaloi chichiltik.

No tikitan ke yin "selector de hijos" kichiua ke yin "elemento" ```<a>``` konet nejin "elemento" ```<p>```. Yin kichiua ke yin "estilos del selector" ```p > a``` amo mokuis tech to amataijkitil "html".

##Selector adyacente

Yin "selector adyacente" mokuik keman tik neki tik pataste "elementos" tein kitojtoka nima. Se kikui ika yin "signo" ```+``` kemej tikita nika tani:

```css
elemento1 + elemento2 { ... }
```

Maj tikuika tech se "código HTML":

```html
<body>
  <h1>Titulo1</h1>
  <h2>Subtítulo</h2>
  <h2>Otro subtítulo</h2>
</body>
```

Yin amataijkitil kipia ome "elementos" ```<h2>```, sayo se tein etok nima de nejin "elemento" ```<h1>``` mo pata. Keman tik nekiske maj mo pata nochi uelis tikuiske *selector adyacente* kemej mo nextia nika tani:

```css
h2 {
  color: green;
}

h1 + h2 {
  color: red;
}
```

Yin "CSS" kichiua ke yin ```<h2>``` nejin to amataijkitil muita tapali xoxoctik , sayo amo ne```<h2>``` tein etoke nima de nejin "elemento" ```<h1>```tein monextia tapali chichiltik.

Yin "elementos" tein kukui *selector adyacente* kipiaj ome "condiciones":

- *elemento1* y *elemento2* kipia eski iknime.
- *elemento2* kipia ke etos nima de nejin *elemento1* tech to amataijkitil HTML.

Maj tikitak keniuj mokui:

```css
p + p {
  text-indent: 1.5em;
}
```

Tech miak amoxmejs, ke nochin "parráfos ki kaua se "espacio", yaso amo tech "párrafo" tein peua. Ika yin "selector" ```p + p```, ti kuij nochin "párrafos" , sayo amo mokui "parráfo" tein peua.

##Selector de atributos

No tikpiaj *selectores de atributos*, teik kikui "atributos" de nejin to amataijkitil "HTML".

Tikpiaj naui "tipos de selectores de atributos":

- [nombre_atributo], selecciona los elementos que tienen establecido el atributo llamado *nombre_atributo*, independientemente de su *valor*.
- [nombre_atributo=valor], selecciona los elementos que tienen establecido un atributo llamado *nombre_atributo* con un *valor* igual a *valor*.
- [nombre_atributo~=valor], selecciona los elementos que tienen establecido un atributo llamado *nombre_atributo* y al menos uno de los valores del atributo es *valor*.
- [nombre_atributo|=valor], selecciona los elementos que tienen establecido un atributo llamado *nombre_atributo* y cuyo valor es una serie de palabras separadas con guiones, pero que comienza con *valor*. Este tipo de selector sólo es útil para los atributos de tipo *lang* que indican el idioma del contenido del elemento.

Maj tikitaka keniuj se kikui:

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
