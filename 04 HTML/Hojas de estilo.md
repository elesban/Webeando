Hojas de estilo CSS.
=============================

CSS son las siglas de Cascading Style Sheets - Hojas de Estilo en Cascada - que es un lenguaje que describe la presentación de los documentos estructurados en hojas de estilo para diferentes métodos de interpretación, es decir, describe como se va a mostrar un documento en pantalla, por impresora, por voz (cuando la información es pronunciada a través de un dispositivo de lectura) o en dispositivos táctiles basados en Braille.

##¿Para que sirve?

CSS es una especificación desarrollada por el W3C (World Wide Web Consortium) para permitir la separación de los contenidos de los documentos escritos en HTML, XML, XHTML, SVG, o XUL de la presentación del documento con las hojas de estilo, incluyendo elementos tales como los colores, fondos, márgenes, bordes, tipos de letra, etc., modificando así la apariencia de una página web de una forma más sencilla, permitiendo a los desarrolladores controlar el estilo y formato de sus documentos.

##¿Cómo funciona?

El lenguaje CSS se basa en una serie de reglas que rigen el estilo de los elementos en los documentos estructurados, y que forman la sintaxis de las hojas de estilo. Cada regla consiste en un selector y una declaración, esta última va entre corchetes y consiste en una propiedad o atributo, y un valor separados por dos puntos.

*Ejemplo*

```
h2 {
  color: green;
}

h2 --> es el selector
{color: green;} --> es la declaración, donde "color" es la propiedad o atributo y "green" es el valor
```

###Selector

El *Selector* especifica qué elementos HTML van a estar afectados por esa declaración, de manera que sirve de enlace entre la estructura del documento y la regla estilística en la hoja de estilo.

###Declaración

La *Declaración* que va entre corchetes es la información de estilo que indica cómo se va a ver el selector. En caso de que haya más de una declaración se usa punto y coma para separarlas.

###Propiedad o Atributo y Valor

Dentro de la declaración, la *Propiedad o Atributo* define la interpretación del elemento asignándosele un cierto valor, que puede ser color, alineación, tipo de fuente, tamaño, etc., es decir, especifican qué aspecto del selector se va a cambiar.

##¿Cómo se integra?

La información CSS se puede proporcionar por varias fuentes, ya sea adjunto como un documento por separado o incorporado en el documento HTML, y dentro de estas posibilidades destacan cuatro formas de dar estilo a un documento web:

###Estilo Externa

La *Hoja de Estilo Externa* se almacena en un archivo diferente al del archivo con el código HTML al cual debe estar vinculado a través del elemento *link*, que debe ir situado en la sección *head*. Es la manera de programar más eficiente, ya que separa completamente las reglas de formato para la página HTML de la estructura básica de la página.

*Ejemplo*

```
<!DOCTYPE html>
<html>
  <head>
    <link rel="stylesheet" type="text/css" href="style.css">
  </head>
  <body>
    <p class="paragraph">Este párrafo tiene algún tipo de estilo de tipo externo.</p>
  </body>
</html>

<link rel="stylesheet" type="text/css" href="style.css"> --> Esta línea nos enlaza al archivo "style.css", donde se encuentra el estilo del HTML
```

###Estilo Interna

La *Hoja de Estilo Interna* está incorporada a un documento HTML, a través del elemento *style* dentro de la sección *head*, consiguiendo de esta manera separar la información del estilo del código HTML.

*Ejemplo*

```
<!DOCTYPE html>
<html>
  <head>
    <style type="text/css">
      h1.myclass {
        border-width: 1;
        border: solid;
        text-align: center
      }
    </style>
  </head>
  <body>
    <h1 class="myclass">Esta clase es afectada por el estilo</h1>
    <h1>Esta clase no es afectada por el estilo</h1>
  </body>
</html>

<style type="text/css">
  h1.myclass {
    border-width: 1;
    border: solid;
    text-align: center
  }
</style> --> En esta sección de código representa la integración del estilo, dentro del archivo HTML
```

###Estilo en Línea

La *Hoja de Estilo en Línea* sirve para insertar el lenguaje de estilo directamente dentro de la sección body con el elemento *style*. Sin embargo, este tipo de estilo no se recomienda pues se debe intentar siempre separar el contenido de la presentación.

*Ejemplo*

```
<!DOCTYPE html>
<html>
  <head></head>
  <body>
    <h1 style="Font: 18px Verdana; font-weight: bold;">Estilo desde línea</h1>
  </body>
</html>

<h1 style="Font: 18px Verdana; font-weight: bold;">Estilo desde línea</h1> --> Esta línea integra el estilo a una sola línea dentro del archivo HTML
```

###Estilo Importado

La *Hoja de Estilo Importada* permite importar hojas de estilo externas cuando se declara el estilo del documento al insertar el comando *@IMPORT* inmediatamente después de la etiqueta de estilo.

*Ejemplo*

```
<!DOCTYPE html>
<html>
  <head>
    <style type="text/css">
      @IMPORT URL (/style.css);
      @IMPORT URL (/style2.css);
    </style>
	</head>
  <body>
    <h1>Este HTML tiene un estilo importado</h1>
  </body>
</html>

<style type="text/css">
  @IMPORT URL (/style.css);
  @IMPORT URL (/style2.css);
</style> --> En esta sección de código representa la integración de varios archivos de estilo en un mismo archivo HTML
```

##Ventajas de CSS

- La principal ventaja de CSS sobre el lenguaje HTML o similar, es que el estilo se puede guardar completamente por separado del contenido siendo posible, almacenar todos los estilos de presentación para una web de muchas páginas en un sólo archivo de CSS.
- CSS permite un mejor control en la presentación de un sitio web que los elementos de HTML, agilizando su actualización.
- Aumento de la accesibilidad de los usuarios gracias a que pueden especificar su propia hoja de estilo, permitiéndoles modificar el formato de un sitio web según sus necesidades.
- El ahorro global en el ancho de banda es notable, ya que la hoja de estilo se almacena en caché después de la primera solicitud y se puede volver a usar para cada página del sitio, por ello no se tiene que descargar con cada página web. Por otro lado, quitando todo lenguaje de marcado en la presentación en favor del uso de CSS reduce su tamaño y ancho de banda hasta más del 50%, esto beneficia al dueño del sitio web con menos ancho de banda y costes de almacenamiento, así como a los visitantes para los cuales las páginas se van a cargar más rápido.
- Una página puede tener diferentes hojas de estilo para mostrarse en diferentes dispositivos y diferentes tamaños, como pueden ser impresoras, lectores de voz, móviles, etc.
