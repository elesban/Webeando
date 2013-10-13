Tipo de selectores CSS.
=============================

Los selectores son imprescindibles para aplicar de forma correcta los estilos CSS en una página.

A un mismo elemento HTML se le pueden aplicar varias reglas CSS y cada regla CSS puede aplicarse a un número ilimitado de elementos. En otras palabras, una misma regla puede aplicarse sobre varios selectores y un mismo selector se puede utilizar en varias reglas.

##Selector universal

Se utiliza para seleccionar todos los elementos de la página. El siguiente ejemplo elimina el margen y el relleno de todos los elementos HTML:

```
* {
  margin: 0;
  padding: 0;
}

* --> Este símbolo indica un selector universal
```

El selector universal se indica mediante un asterisco (*). A pesar de su sencillez, no se utiliza habitualmente, ya que es difícil que un mismo estilo se pueda aplicar a todos los elementos de una página.

##Selector de tipo o etiqueta

Selecciona todos los elementos de la página cuya etiqueta HTML coincide con el valor del selector. El siguiente ejemplo selecciona todos los párrafos de la página:

```
p {
  margin: 0;
}

p --> En CSS es el tipo de selector, lo mismo que para HTML sería la etiqueta <p>
```

Para utilizar este selector, solamente es necesario indicar el nombre de una etiqueta HTML (sin los caracteres < y >) correspondiente a los elementos que se quieren seleccionar.

Si se quiere aplicar los mismos estilos a dos etiquetas diferentes, se pueden encadenar los selectores. En el siguiente ejemplo, los títulos de sección h1, h2 y h3 comparten los mismos estilos:

```
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

En este caso, CSS permite agrupar todas las reglas individuales en una sola regla con un selector múltiple. Para ello, se incluyen todos los selectores separados por una coma (,) y el resultado es que la siguiente regla CSS es equivalente a las tres reglas anteriores:

```
h1, h2, h3 {
  color: #8A8E27;
  font-weight: normal;
  font-family: Arial, Helvetica, sans-serif;
}
```

##Selector descendente

Selecciona los elementos que se encuentran dentro de otros elementos. Un elemento es descendiente de otro cuando se encuentra entre las etiquetas de apertura y de cierre del otro elemento. El selector del siguiente ejemplo selecciona todos los elementos ```<span>``` de la página que se encuentren dentro de un elemento ```<p>```:

```
p span {
 color: red;
}
```

Si el código HTML de la página es el siguiente:

```
<p>
  <span>Texto en color rojo</span>
</p>
```

Los selectores descendentes permiten aumentar la precisión del selector de tipo o etiqueta. Así, utilizando el selector descendente es posible aplicar diferentes estilos a los elementos del mismo tipo. El siguiente ejemplo muestra de color azul todo el texto de los ```<span>``` contenidos dentro de un ```<h1>```:

```
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

```
<body>
 <p class="destacado">Este párrafo diferente a todos</p>
 <p>Párrafo normal</p>
 <p>Párrafo normal dos</p>
</body>
```

Para que el navegador no confunda este selector con los otros tipos de selectores, se prefija el valor del atributo *class* con un punto (.) tal y como muestra el siguiente ejemplo:

```
.destacado {
 color: red;
}
```
El selector *.destacado* se interpreta como "cualquier elemento de la página cuyo atributo *class* sea igual a *destacado*", por lo que solamente el primer párrafo cumple esa condición.

En ocasiones, es necesario restringir el alcance del selector de clase:

```
<body>
 <p class="destacado">Párrafo con la clase destacado</p>
 <p>Inicio de un párrafo <a href="#" class="destacado">link con la clase destacado dentro de un párrafo</a> fin del párrafo</p>
 <p>Inicio de un párrafo <em class="destacado">itálica con la clase destacado dentro de un párrafo</em> fin del párrafo</p>
</body>
```

Para aplicar estilos solamente al párrafo cuyo atributo *class* sea igual a *destacado*, es necesario combinar el selector de tipo y el selector de clase, así se obtiene un selector mucho más específico:

```
p.destacado {
 color: red
}
```

El selector *p.destacado* se interpreta como "aquellos elementos de tipo ```<p>``` que dispongan de un atributo *class* con valor *destacado*". De la misma forma, el selector *a.destacado* solamente selecciona los enlaces cuyo atributo *class* sea igual a *destacado*.

No debe confundirse el selector de clase con los selectores anteriores:

```
/* Todos los elementos de tipo "p" con atributo class="aviso" */
p.aviso { ... }
 
/* Todos los elementos con atributo class="aviso" que estén dentro de cualquier elemento de tipo "p" */
p .aviso { ... }
 
/* Todos los elementos "p" de la página y todos los elementos con atributo class="aviso" de la página */
p, .aviso { ... }
```

Además es posible aplicar los estilos de varias clases CSS sobre un mismo elemento. La sintaxis es similar, pero los diferentes valores del atributo *class* se separan con espacios en blanco. En el siguiente ejemplo:

```
<p class="especial destacado error">Párrafo de texto...</p>
```

Al párrafo anterior se le aplican los estilos definidos en las reglas *.especial*, *.destacado* y *.error*, por lo que en el siguiente ejemplo, el texto del párrafo se vería de color rojo, en negrita y con un tamaño de letra de 15 píxel:

```
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

```
#destacado {
 color: red;
}
 
<p>Primer párrafo</p>
<p id="destacado">Segundo párrafo</p>
<p>Tercer párrafo</p>
```

En el ejemplo anterior, el selector *#destacado* solamente selecciona el segundo párrafo (cuyo atributo *id* es igual a *destacado*).

La principal diferencia entre este tipo de selector y el selector de clase tiene que ver con HTML y no con CSS. Como se sabe, en una misma página, el valor del atributo *id* debe ser único, de forma que dos elementos diferentes no pueden tener el mismo valor de *id*. Sin embargo, el atributo *class* no es obligatorio que sea único, de forma que muchos elementos HTML diferentes pueden compartir el mismo valor para su atributo *class*.

##Combinación de selectores básicos

CSS permite la combinación de uno o más tipos de selectores para restringir el alcance de las reglas CSS. A continuación se muestran algunos ejemplos habituales de combinación de selectores.

```
.aviso .especial { ... }
```

El anterior selector solamente selecciona aquellos elementos con un *class="especial"* que se encuentren dentro de cualquier elemento con un *class="aviso"*.

Si se modifica el anterior selector:

```
div.aviso span.especial { ... }
```

Ahora, el selector solamente selecciona aquellos elementos de tipo ```<span>``` con un atributo *class="especial"* que estén dentro de cualquier elemento de tipo ```<div>``` que tenga un atributo *class="aviso"*.

La combinación de selectores puede llegar a ser todo lo compleja que sea necesario:

```
ul#menuPrincipal li.destacado a#inicio { ... }
```

El anterior selector hace referencia al *enlace* con un atributo *id* igual a *inicio* que se encuentra dentro de un elemento de tipo ```<li>``` con un atributo *class* igual a *destacado*, que forma parte de una lista ```<ul>``` con un atributo *id* igual a *menuPrincipal*.
