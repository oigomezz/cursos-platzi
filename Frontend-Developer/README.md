# Curso de Frontend Developer <!-- omit in toc -->

## Tabla de Contenido<!-- omit in toc -->

- [¿Qué es HTML y CSS? ¿Para qué sirven?](#qué-es-html-y-css-para-qué-sirven)
  - [¿Qué es HTML?](#qué-es-html)
  - [¿Qué es CSS?](#qué-es-css)
  - [Para qué sirven las herramientas del navegador](#para-qué-sirven-las-herramientas-del-navegador)
- [Motores de render](#motores-de-render)
  - [¿Cuáles son los motores del navegador?](#cuáles-son-los-motores-del-navegador)
  - [Proceso de renderizado del motor del navegador](#proceso-de-renderizado-del-motor-del-navegador)
- [Anatomía de un documento HTML y sus elementos](#anatomía-de-un-documento-html-y-sus-elementos)
  - [Qué son atributos HTML](#qué-son-atributos-html)
  - [Qué son los elementos vacíos](#qué-son-los-elementos-vacíos)
  - [Qué es el anidamiento de elementos](#qué-es-el-anidamiento-de-elementos)
  - [Estructura básica de un documento HTML](#estructura-básica-de-un-documento-html)
    - [Etiqueta Doctype](#etiqueta-doctype)
    - [Etiqueta html](#etiqueta-html)
    - [Etiqueta head](#etiqueta-head)
    - [Etiqueta body](#etiqueta-body)
    - [Comentarios de HTML](#comentarios-de-html)
- [¿Qué es HTML semántico?](#qué-es-html-semántico)
  - [El problema con la etiqueta div](#el-problema-con-la-etiqueta-div)
  - [¿Cuáles son las etiquetas semánticas?](#cuáles-son-las-etiquetas-semánticas)
  - [Ventajas de utilizar HTML semántico](#ventajas-de-utilizar-html-semántico)
- [Anatomía de una declaración CSS](#anatomía-de-una-declaración-css)
  - [Qué es una declaración de CSS](#qué-es-una-declaración-de-css)
  - [Propiedades iniciales de CSS](#propiedades-iniciales-de-css)
  - [Medidas iniciales](#medidas-iniciales)
- [Tipos de selectores](#tipos-de-selectores)
  - [Cuáles son los selectores básicos](#cuáles-son-los-selectores-básicos)
    - [Selector de tipo](#selector-de-tipo)
    - [Selector de clase](#selector-de-clase)
    - [Selector de identificador único (id)](#selector-de-identificador-único-id)
    - [Selector de atributo](#selector-de-atributo)
    - [Selector universal](#selector-universal)
  - [Cuáles son los selectores combinadores](#cuáles-son-los-selectores-combinadores)
    - [Combinador de descendientes](#combinador-de-descendientes)
    - [Combinador de hijo directo](#combinador-de-hijo-directo)
    - [Combinador de elemento adyacente](#combinador-de-elemento-adyacente)
    - [Combinador general de hermanos](#combinador-general-de-hermanos)
- [Pseudoclases y Pseudoelementos](#pseudoclases-y-pseudoelementos)
  - [Cuáles son las pseudoclases](#cuáles-son-las-pseudoclases)
  - [Cuáles son los pseudoselementos](#cuáles-son-los-pseudoselementos)
- [Cascada y especificidad en CSS](#cascada-y-especificidad-en-css)
  - [Qué es la cascada en CSS](#qué-es-la-cascada-en-css)
  - [Qué es especificidad en CSS](#qué-es-especificidad-en-css)
    - [Tipos de especificidad en CSS](#tipos-de-especificidad-en-css)
    - [Valor con mayor especificidad](#valor-con-mayor-especificidad)
    - [Estilos en línea](#estilos-en-línea)
    - [Especificidad en selectores](#especificidad-en-selectores)

## ¿Qué es HTML y CSS? ¿Para qué sirven?

La web se construye mediante tres tecnologías esenciales: HTML, CSS y JavaScript. Estos tres lenguajes son las bases en que una aplicación o página web está construida.

### ¿Qué es HTML?

El Lenguaje de Marcado de Hipertexto o HTML por sus siglas en inglés (HyperText Markup Language) es el código para construir la estructura de una página web.

En otras palabras, HTML es el esqueleto con el cual definimos cada elemento que compone la página web, así como: enlaces, párrafos, títulos, botones, imágenes, formularios, entre otros.

### ¿Qué es CSS?

El lenguaje de Hojas de Estilos en Cascada o CSS por sus siglas en inglés (Cascade Style Sheets) es el código para describir la presentación de los elementos de la página web, los que definimos con HTML.

### Para qué sirven las herramientas del navegador

Las herramientas del navegador son importantes para visualizar lo que ocurre con el código generado. Entre una de la opciones está identificar los elementos que están estructurados en la página web con sus respectivos estilos.

Las herramientas de desarrollador se despliegan con la combinación de teclas F12 / Ctrl + Shift + I / Cmd + Opt + I o clic derecho e “Inspeccionar” en tu navegador preferido (se recomienda Google Chrome).

[🡡 volver al inicio](#tabla-de-contenido)

## Motores de render

Los motores de renderizado son programas que traducen nuestro código en un lenguaje que entienda el navegador, de esta manera el programa sabrá que es lo que tiene que mostrar por pantalla al usuario.

### ¿Cuáles son los motores del navegador?

Los navegadores tienen sus propios motores: Chrome - Blink, Edge - Edge HTML, Safari - Webkit y Firefox - Gecko. Todos realizan esta compilación de manera diferente, pero con el mismo resultado, es decir, convierten los archivos a píxeles.

### Proceso de renderizado del motor del navegador

El motor del navegador realiza 5 pasos o procesos para compilar nuestro código hasta el renderizado por pantalla. Estos pasos son los siguientes:

1. Transforma los archivos a un árbol de objetos HTML o CSS, estos se denominan DOM (Document Object Model) y CSSDOM (Cascade Style Sheet Object Model), respectivamente. Cada nodo en el árbol es una representación de los elementos que contiene el archivo HTML o CSS.
2. Calcula el estilo correspondiente a cada nodo del DOM relacionado al CSSDOM.
3. Calcula las dimensiones de cada nodo y dónde va en la pantalla.
4. Pinta o renderiza los diferentes elementos como cajas o contenedores.
5. Agrupa todas las cajas en diferentes capas para convertirlas en una imagen que se renderiza en pantalla.

[🡡 volver al inicio](#tabla-de-contenido)

## Anatomía de un documento HTML y sus elementos

Antes de empezar a escribir código HTML, debemos conocer la anatomía de un documento y sus elementos.
¿Cuáles son los elementos HTML?

Los elementos son cada una de las partes que conforman un archivo HTML. Su estructura contiene:

- Etiquetas: es la representación de un elemento HTML. Se dividen en etiquetas de apertura, representadas por `<etiqueta>` y etiquetas de cierre, representadas por `</etiqueta>`.
- Contenido: es el texto o elementos encerrados por la etiqueta, este valor es opcional en algunas de ellas.

### Qué son atributos HTML

Los atributos HTML son propiedades en la etiqueta de apertura que manejan el comportamiento del elemento. Su valor está envuelto en comillas.

### Qué son los elementos vacíos

Los elementos vacíos son aquellos que únicamente se representan en una etiqueta de apertura. Por ejemplo, la etiqueta de imagen: `<img...>`. Estas etiquetas pueden cerrarse en la misma etiqueta de apertura, utilizando la barra inclinada “/” al final: `<img.../>`.

### Qué es el anidamiento de elementos

El anidamiento de elementos HTML consiste en envolver varias etiquetas en otras etiquetas.

Interpreta a cada elemento HTML como una caja donde puedes guardar diferentes elementos u otras cajas. Estas cajas tendrán diferentes tamaños y estarán colocadas junto a otras.

```html
<section>
  <h1>Platzi</h1>
  <p>Tiene una comunidad</p>
  <ul>
    <li>Increible</li>
    <li>Maravillosa</li>
    <li>Inigualable</li>
  </ul>
</section>
```

Aquellas etiquetas que envuelven a otras se las denomina “padres”. Es decir, `<section>` es padre de `<h1>`, `<p>`, `<ul>`, y a su vez `<ul>` es padre de 3 etiquetas `<li>`.

Las etiquetas que son el contenido de otras, se las denomina “hijos”. Es decir, las etiquetas `<h1>`,`<p>`, `<ul>` son hijos de `<section>`, y a su vez las etiquetas `<li>` son hijos de `<ul>`.

### Estructura básica de un documento HTML

La estructura básica de un documento HTML está configurado por las siguientes etiquetas principales:

#### Etiqueta Doctype

La etiqueta `<!DOCTYPE html>` especifica que el archivo se maneje con la versión 5 de HTML.

#### Etiqueta html

La etiqueta `<html>` define el elemento raíz de un documento HTML. Todos los demás elementos deben estar contenidos dentro de este elemento raíz. En esta etiqueta se especifica el lenguaje de la página web mediante la propiedad lang.

#### Etiqueta head

La etiqueta `<head>` define la metainformación, es decir, toda información que no es contenido como tal de la página web. Por ejemplo, los enlaces a archivos CSS y JavaScript, el título y la imagen que aparecen en la pestaña del navegador. Esto es importante para motores de búsqueda como Google.

#### Etiqueta body

La etiqueta `<body>` define el contenido de la página web. Debe ser hijo cercano de `<html>` y padre de todas las etiquetas HTML, excepto por aquellas que definan metainformación.

#### Comentarios de HTML

Los comentarios de HTML consiste en señalar algo que se ignorará. Para establecer un comentario HTML se lo envuelve entre <!-- y -->, independiente de la cantidad de líneas.

```html
<!-- Este es un comentario de una línea -->

<!--
Este es un comentario de varias líneas
-->
```

[🡡 volver al inicio](#tabla-de-contenido)

## ¿Qué es HTML semántico?

El HTML semántico consiste en que cada elemento tenga su propia etiqueta que lo defina correctamente. Sin utilizar etiquetas muy generales, como `<div>` o `<span>`.

### El problema con la etiqueta div

La etiqueta div define un bloque genérico de contenido, que no tiene ningún valor semántico. Se utiliza para elementos de diseño como contenedores.

### ¿Cuáles son las etiquetas semánticas?

Las etiquetas semánticas para definir una interfaz de una página web son:

- `<header>`: define el encabezado de la página (no confundir con `<head>`).
- `<nav>`: define una barra de navegación que incluye enlaces.
- `<section>`: define una sección de la página.
- `<footer>`: define un pie de página o de sección.
- `<article>`: define un artículo, el cual puede tener su propio encabezado, navegación, sección o pie de página.

Ahora que ya conoces las etiquetas semánticas, evita el uso excesivo de `<div>`.

![Diferencias con html semantico](images/HTML-semantico.png)

### Ventajas de utilizar HTML semántico

Las ventajas de utilizar un HTML semántico son:

- Ayuda a tu sitio a ser accesible
- Mejora tu posicionamiento (SEO)
- Código más claro, legible y mantenible
- Ayuda a buscadores (como Google) a encontrar tu página

[🡡 volver al inicio](#tabla-de-contenido)

## Anatomía de una declaración CSS

Antes de empezar a escribir código CSS, debemos conocer la anatomía de una declaración de estilos.

### Qué es una declaración de CSS

Una declaración de CSS es un bloque que especifica el conjunto de estilos que se añadirán a un elemento HTML. Su estructura contiene lo siguiente:

- Selector: define el elemento o conjunto de elementos a los cuales se añadirán los estilos.
- Propiedad: es el nombre del estilo de CSS.
- Valor: es el valor que tomará la propiedad.

### Qué son comentarios de CSS

Los comentarios de CSS consisten en señalar algo que se ignorará. Para establecer un comentario CSS se lo envuelve entre `/*` y `*/`, independiente de la cantidad de líneas.

```css
/* Este es un comentario de una línea */
/* 
Este es un comentario de varias líneas
*/
```

### Propiedades iniciales de CSS

Antes de empezar con CSS utilizaremos algunas propiedades de CSS.

- color: establece el color del texto de un elemento.
- background-color: establece un color de fondo al elemento.
- font-size: establece el tamaño de la fuente.
- width: establece la anchura de un elemento.
- height: establece la altura de un elemento.

### Medidas iniciales

Estas son las medidas iniciales que debes conocer para establecer tamaños de elementos o de tipografía:

- px: establece una longitud de píxeles.
- %: establece un porcentaje con respecto a una medida base.

[🡡 volver al inicio](#tabla-de-contenido)

## Tipos de selectores

El selector define el elemento o conjunto de elementos HTML a los cuales se añadirán estilos. Existen nombres de colores propios de CSS que puedes explorar. A continuación veamos más sobre selectores.

### Cuáles son los selectores básicos

Un selector básico es la mínima expresión CSS para colocar estilos.

```css
selector {
  /* Estilos */
}
```

#### Selector de tipo

Selecciona todos los elementos que coincidan con el nombre de la etiqueta HTML.

```css
div {
  /* Todos los div en el documento */
}
```

#### Selector de clase

Selecciona todos los elementos que coincidan con las etiquetas HTML que contengan el atributo class.

```html
<!--archivo HTML-->
<div class="card">Soy una carta</div>
```

Para seleccionar estos elementos, se empieza por un punto . y seguido el valor exacto del atributo class de la etiqueta. Puede ser cualquier valor que desees colocar.

```css
/* archivo CSS */
.card {
  /* Todas las etiquetas con la clase "card" */
}
```

Puede existir más de un valor dentro del atributo class separados por espacios.

```html
<!--archivo HTML-->
<div class="card card1">Soy una carta</div>
<div class="card card2">Soy una carta</div>
```

```css
.card {
  /* Todas las etiquetas con la clase "card" */
}

.card1 {
  /* Todas las etiquetas con la clase "card1" */
}

.card2 {
  /* Todas las etiquetas con la clase "card2" */
}
```

#### Selector de identificador único (id)

Selecciona el único elemento que coincida con la etiqueta HTML que contenga el atributo id. Solo puede existir un valor id para todo el documento.

```html
<!--archivo HTML-->
<button id="eliminar">Eliminar</button>
```

Para seleccionar el elemento, se empieza por el símbolo de hashtag # y seguido el valor exacto del atributo id de la etiqueta. Puede ser cualquier valor que desees colocar.

```css
/* archivo CSS */
#eliminar {
  /* La única etiqueta con el id "eliminar" */
}
```

#### Selector de atributo

Selecciona los elementos que coincidan con la etiqueta HTML que contenga el atributo y valor especificado.

```html
<!--archivo HTML-->
<a href="https://platzi.com"> Ir a Platzi </a>
```

Para seleccionar los elementos, se empieza por el nombre de la etiqueta, seguido de corchetes [] que contiene el atributo y valor especificado.

```css
/* archivo CSS */
a[href=""https://platzi.com"]
{
  /* Todas las etiquetas <a> con una propiedad href con valor "https://platzi.com" */
}
```

#### Selector universal

Selecciona todos los elementos del documento mediante un asterisco \*.

```css
* {
  /* Todos los elementos */
}
```

### Cuáles son los selectores combinadores

Un selector combinador es la unión de dos o más selectores básicos.

```css
selector1 selector2 selector3 {
  /* Estilos */
}
```

#### Combinador de descendientes

Selecciona todos los elementos del selector de la derecha que son hijos del selector de la izquierda, independientemente de la profundidad. Estos selectores están separados por un espacio.

```css
padre hijos {
  /* Todos los hijos del padre */
}

div p {
  /* Todos los hijos <p> de <div>*/
}

.container img {
  /* Todos los hijos <img> de la clase "container"*/
}
```

#### Combinador de hijo directo

Selecciona todos los elementos del selector de la derecha que son hijos directos del selector de la izquierda. Estos selectores están separados por >.

```css
padre > hijos_directos {
  /* Todos los hijos directos del padre */
}

div > p {
  /* Todos los hijos directos <p> de <div>*/
}

.container > img {
  /* Todos los hijos directos <img> de la clase "container"*/
}
```

#### Combinador de elemento adyacente

Selecciona todos los elementos del selector de la derecha que están adyacente al selector de la izquierda. Estos selectores están separados por +.

```css
elemento + adyacente {
  /* Elementos adyacentes */
}

div + p {
  /* Todos los <p> adyacentes a <div>*/
}

.container + img {
  /* Todos los <img> adyacentes a la clase "container"*/
}
```

Adyacente significa que comparten el mismo padre y está situado inmediatamente hacia abajo de otro elemento. Por ejemplo, en el siguiente código, `<div>` está adyacente a `<h1>` y `<p>` está adyacente a `<div>`. Sin embargo, `<h1>` no está adyacente a `<div>` y `<div>` no está adyacente a `<p>`.

```html
<!--archivo HTML -->
<h1>Soy un título</h1>
<div>Soy un div</div>
<p>Soy un párrafo</p>
```

#### Combinador general de hermanos

Selecciona todos los elementos del selector de la derecha que son hermanos del selector de la izquierda. Estos selectores están separados por ~.

```css
elemento ~ hermanos {
  /* Elementos hermanos */
}

div ~ p {
  /* Todos los <p> hermanos de <div>*/
}

.container ~ img {
  /* Todos los <img> hermanos de la clase "container"*/
}
```

Hermanos significa que comparten el mismo padre y están situados hacia abajo de otro elemento. Por ejemplo, en el siguiente código, `<div>` y `<p>` son hermanos de `<h1>`, pero `<h1>` no es hermano de `<div>` y `<p>`.

```html
<!--archivo HTML -->
<h1>Soy un título</h1>
<div>Soy un div</div>
<p>Soy un párrafo</p>
```

[🡡 volver al inicio](#tabla-de-contenido)

## Pseudoclases y Pseudoelementos

Existen otros tipos de selectores, además de los selectores básicos y combinadores, capaces de cambiar un estado o añadir algo más al elemento. Estos son denominados pseudoclases y pseudoelementos.

### Cuáles son las pseudoclases

Una pseudoclase define el estilo de un estado especial de un elemento. [Índice de pseudo-clases estándar.](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-classes#indice_de_las_pseudo-clases_est%C3%A1ndar)

```css
selector: pseudoclase {
  propiedad: valor;
}
```

- :hover

  Representa el estado en el cual el cursor está encima del elemento.

- :active

  Representa el estado de un elemento que no ha sido visitado.

- :visited

  Representa el estado de un elemento que ya ha sido visitado.

- :not()

  Representa el estado en el cual no coinciden los selectores que se indiquen.

- :nth-child()

  Representa el estado en el cual coinciden los hijos del elemento según el valor indicado.

Valores de palabras clave:

- odd: los elementos hijos en posiciones impares.
- even: los elementos hijos en posiciones pares.

Fórmula matemática: An+B donde A y B son números enteros.

### Cuáles son los pseudoselementos

Un pseudoelemento define el estilo de una parte específica de un elemento. [Lista de pseudo-elementos.](https://developer.mozilla.org/es/docs/Web/CSS/Pseudo-elements#lista_de_pseudoelementos)

```css
selector :: pseudo-elemento {
  propiedad: valor;
}
```

- ::before

  Sirve para agregar un contenido antes del elemento. El contenido es agregado mediante la propiedad content de CSS.

- ::after

  Sirve para agregar un contenido después del elemento. El contenido es agregado mediante la propiedad content de CSS.

- ::first-letter

  Sirve para añadir estilos a a la primera letra del texto de cualquier elemento.

[🡡 volver al inicio](#tabla-de-contenido)

## Cascada y especificidad en CSS

En algún punto, cuando estés creando una página web, te encontrarás con problemas con los estilos, por ejemplo:

- ¿Por qué no se aplica el color que le estoy poniendo?
- ¿Por qué este elemento se comporta de manera diferente?

Probablemente, sea un inconveniente de cascada o especificidad.

### Qué es la cascada en CSS

La cascada es el concepto que determina qué estilos se colocan sobre otros, priorizando a aquellos que se encuentren más abajo del código. Recordarás que CSS es la abreviación de Cascade Style Sheets, que traducido es hojas de estilos en Cascada.

Mira el siguiente código e identifica de qué color de letra tendrá la etiqueta `<h1>`.

```css
h1 {
  color: red;
}

h1 {
  color: blue;
}
```

La etiqueta `<h1>` tendrá un color blue de letra, esto porque está situado más abajo en el código. Esto ocurre con cada propiedad de CSS que se repita en algún punto más arriba del código.

Sin embargo, esto ocurre cuando la especificidad de una regla CSS tiene el mismo valor. Pero, ¿qué es especificidad?

### Qué es especificidad en CSS

La especificidad consiste en dar un valor a una regla CSS sobre qué tan específico es el estilo, esto para que los navegadores puedan saber qué estilos aplicar sobre otros, independientemente de dónde se encuentren en el código. El estilo se aplicará donde la especificidad sea mayor.

#### Tipos de especificidad en CSS

Existen 6 tipos de especificidad con su respectivo valor, donde X es la cantidad de estilos que lo contienen.

![Tipos de espeificidad](/Frontend-Developer/images/especificidad.jpg)

#### Valor con mayor especificidad

La palabra reservada !important es un valor de toda propiedad CSS que provee una especificidad de 10000, por lo que se aplicará ante otros estilos. Esto es una mala práctica y no deberías utilizarlo.

```css
h1 {
  color: red !important;
}
```

#### Estilos en línea

Los estilos en línea son las propiedades CSS escritas en el HTML a través de la propiedad style de toda etiqueta. También es una mala práctica y debes evitarlo.

```html
<h1 style="color: blue;">Especificidad</h1>
```

#### Especificidad en selectores

El tema de los selectores ya lo conoces, por lo tanto, los selectores de tipo ID son más específicos que las clases, atributos y pseudoclases. Estas últimas son más específicas que los elementos y pseudoelementos. El selector universal tiene una especificidad de 0.

En un proyecto deberías evitar los !important y estilos en línea, para trabajar únicamente con la especificidad de los selectores. Sin embargo, debes tener presente que los selectores combinadores suman la especificidad de cada selector básico para obtener la especificidad total de la regla CSS.

[🡡 volver al inicio](#tabla-de-contenido)
