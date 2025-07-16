# Curso Práctico de Frontend Developer <!-- omit in toc -->

## Tabla de Contenido<!-- omit in toc -->

- [Maquetación](#maquetación)
- [Sistema de diseño, assets y variables de CSS](#sistema-de-diseño-assets-y-variables-de-css)
  - [¿Cuál es la utilidad de un sistema de diseño?](#cuál-es-la-utilidad-de-un-sistema-de-diseño)
  - [Variables en CSS](#variables-en-css)
  - [Fonts](#fonts)
- [Display Grid para centrar elementos](#display-grid-para-centrar-elementos)
  - [Cómo ordenar los estilos](#cómo-ordenar-los-estilos)
- [Responsive design](#responsive-design)
- [Tipos de posicionamiento en HTML](#tipos-de-posicionamiento-en-html)
- [Cómo maquetar un formulario de registro](#cómo-maquetar-un-formulario-de-registro)
  - [Estilos para el formulario de registro](#estilos-para-el-formulario-de-registro)
  - [¿Cómo alinear el botón del formulario?](#cómo-alinear-el-botón-del-formulario)
- [Página de inicio](#página-de-inicio)
  - [Cómo crear la estructura HTML de la página de inicio](#cómo-crear-la-estructura-html-de-la-página-de-inicio)
  - [Cómo colocar imágenes en HTML](#cómo-colocar-imágenes-en-html)
  - [¿Qué contenedores usar?](#qué-contenedores-usar)
  - [Cómo implementar CSS Grid para centrar varias imágenes](#cómo-implementar-css-grid-para-centrar-varias-imágenes)
  - [Misma clase, estilos diferentes](#misma-clase-estilos-diferentes)
- [Menú](#menú)
  - [Cómo hacer una lista desplegable en HTML5](#cómo-hacer-una-lista-desplegable-en-html5)
  - [Estilos de CSS para listas dentro del menú](#estilos-de-css-para-listas-dentro-del-menú)
  - [Menú mobile](#menú-mobile)
  - [Estructura semántica de un menú para dispositivos móviles](#estructura-semántica-de-un-menú-para-dispositivos-móviles)
  - [Especifidad en CSS](#especifidad-en-css)
- [Mi Orden](#mi-orden)
  - [Cómo hacer la maqueta de una orden de pedidos en HTML](#cómo-hacer-la-maqueta-de-una-orden-de-pedidos-en-html)
  - [Cómo aplicar CSS en una orden de compra](#cómo-aplicar-css-en-una-orden-de-compra)
  - [¿Qué logra object-fit en CSS?](#qué-logra-object-fit-en-css)
- [Mis Ordenes](#mis-ordenes)
  - [HTML para mostrar las órdenes de compra](#html-para-mostrar-las-órdenes-de-compra)
  - [Estilos CSS para crear listas de órdenes pedidas](#estilos-css-para-crear-listas-de-órdenes-pedidas)
- [Navbar](#navbar)
  - [Estilos básicos de CSS para menú](#estilos-básicos-de-css-para-menú)
  - [Cómo centrar el carrito de compras en la barra de navegación](#cómo-centrar-el-carrito-de-compras-en-la-barra-de-navegación)
  - [Lista desplegable en menú](#lista-desplegable-en-menú)
- [Detalle de Producto](#detalle-de-producto)
  - [Uso de aside en HTML5](#uso-de-aside-en-html5)
  - [Cómo estilizar un componente aside](#cómo-estilizar-un-componente-aside)
  - [Slider con imágenes del producto](#slider-con-imágenes-del-producto)
- [Carrito de compras](#carrito-de-compras)
  - [Maquetado básico con HTML de un carrito de compras](#maquetado-básico-con-html-de-un-carrito-de-compras)
  - [Estilos CSS para un carrito de compras](#estilos-css-para-un-carrito-de-compras)
  - [¿Qué es tranform en CSS?](#qué-es-tranform-en-css)

## Maquetación

La maquetación o diagramación web consiste en transformar un diseño gráfico —boceto— (hecho por UX/UI en Figma o Scketch) en una interfaz funcional en términos de programación que entienda un navegador o dispositivo específico.

El área de diseño nos proporcionó el bosquejo del proyecto en Figma.

Podemos identificar las vistas de:

- Inicio
- Creación de cuenta
- Acceso
- Carrito de compras
- Orden de compra
- Detalle de producto
- Menú

[🡡 volver al inicio](#tabla-de-contenido)

## Sistema de diseño, assets y variables de CSS

### ¿Cuál es la utilidad de un sistema de diseño?

La principal ventaja de implementar un sistema de diseño es que facilita las tareas de diseñadores y desarrolladores en el proceso de creación. También agiliza la toma de decisión entre equipos.

### Variables en CSS

En CSS, llamamos variables a las propiedades personalizadas.
Contienen valores específicos que se pueden reutilizar muchas veces en un documento.

Se establecen mediante la notación de dos guiones

```css
--nombre-variable: valor;
```

Se acceden mediante la función var()

```css
propiedad: var(--nombre-variable);
```

Normalmente las declaramos dentro del selector :root para que su alcance (scope) sea global.

Nuestro proyecto quedaría así:

```css
:root {
    --black:#000000;
    --white: #FFFFFF;
    --very-light-pink: #C7C7C7;
    --text-input-field: #F7F7F7;
    --dark: #232830;
    --hospital-green: #ACD9B2;
}
```

También puedes nombrar a tus variables según su función.

Ejemplos: --background-color, --primary-color, etcétera.

### Fonts

Buscaremos las fuentes propuestas por diseño en Google fonts
Colocamos los links dentro de la etiqueta head del HTML

```html
<head>
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Quicksand:wght@300;500;700&display=swap" rel="stylesheet">
</head>
```

Dentro de la etiqueta style le decimos a CSS que la implemente

```css
body {
    font-family: 'Quicksand', sans-serif;
}
```

[🡡 volver al inicio](#tabla-de-contenido)

## Display Grid para centrar elementos

Cómo puedes ver en nuestra clase login con solo dos líneas de código podemos centrar nuestro contenido

```css
display: grid;
place-items: center;
```

El shorthand property place-items te permite alinear elementos, tanto horizontal como verticalmente, en un contendor con Grid o Flexbox. Es decir, es la abreviatura de las propiedades align-items y justify-items.
Si no le estableces el segundo valor va a utilizar el primero para ambas alineaciones.

Prueba diferentes combinaciones y observa que ocurre:

```css
place-items: center stretch;
place-items: center start;
place-items: start end;
place-items: end center;
```

Profundiza más sobre este tema con esta clase del curso de CSS Grid básico.

### Cómo ordenar los estilos

Una manera de hacerlo es según su propósito. Siguiendo el siguiente orden:

1. Posicionamiento
2. Modelo de caja
3. Tipografía
4. Visuales
5. Otros

[🡡 volver al inicio](#tabla-de-contenido)

## Responsive design

Nuestro proyecto es responsive, es decir, se adapta a diferentes tamaños de pantalla. Para lograrlo implementamos media queries.

```css
@media (max-width: 640px)
```

Los estilos que se encuentran fuera son para desktop.

Los que están dentro aplicarán cuando el viewport sea menor a 640 píxeles.

Existe otra forma de maquetación responsive que es justo a la inversa. Primero pensamos en los estilos para móviles y luego vamos “subiendo” hasta llegar a web. Esto se conoce como Maquetación Mobile First.

## Tipos de posicionamiento en HTML

Position puede tener cualquiera de estos valores:

- Static: posición por defecto de los elementos. Es el único caso en el que no se puede utilizar top, right, bottom ni left.

- Absolute: los elementos permanecen en la posición donde fueron colocados, pero pierden su espacio físico, es decir, se sobreponen en otros elementos. Aclaración: para poder aplicar este valor, el contendor padre debe tener position relative.

- Relative: conservan su posición original y espacio físico, pero podemos moverlos con las propiedades top, right, bottom, y left.

- Fixed: pierden su espacio físico y permanecen de forma fija.

- Sticky: conservan su espacio físico, pero cuando el scroll los alcanza lo siguen sin perder dicho espacio físico. Es muy usado para barras de navegación.

- Initial: vuelve el position de un elemento a como estaba originalmente.

- Inherit: hereda el position de su padre.

## Cómo maquetar un formulario de registro

Para maquetar este formulario puedes revisar el código generado para la vista de login. Remueve el logo y el subtítulo de esta estructura y debería verse de esta forma:

```html
<div class="login">
    <div class="form-container">
      <h1 class="title">My account</h1>
      <form action="/" class="form">    
       </form>
    </div>
</div>
```

El formulario contiene tres inputs: nombre, email y contraseña del usuario. Los encerramos en un div para poder estilizarlos después.

```html
<form action="/" class="form">
        <div>
          <label for="name" class="label">Name</label>
          <input type="text" id="name" placeholder="Teff" class="input input-name">

          <label for="email" class="label">Email</label>
          <input type="text" id="email" placeholder="platzi@example.com" class="input input-email">

          <label for="password" class="label">Password</label>
          <input type="password" id="password" placeholder="*********" class="input input-password">
        </div>
</form>
```

Finalmente, antes de la etiqueta de cierre del formulario, agregamos el botón para que el usuario pueda enviar la información.

```html
    <input type="submit" value="Create" class="primary-button login-button">
</form>
```

### Estilos para el formulario de registro

A los estilos que utilizamos previamente en la sección “nueva contraseña”, les agregaremos algunos más para darle formato a esta sección.

Los ajustes son:

Aumentar el espaciado entre los inputs del formulario

```css
.input-name,
.input-email,
.input-password {
    margin-bottom: 22px;
}
```

Modificar el css de la calse “title” para alinear el título a la izquierda y distanciarlo de los inputs

```css
.title {
    margin-bottom: 36px;
    text-align: start;
}
```

### ¿Cómo alinear el botón del formulario?

Tal como ocurrió en el reto anterior, esta pantalla en su versión móvil despega el botón del formulario llevándolo hasta abajo. Una de las maneras más sencillas y efectivas de hacer esto es usando Flexbox.

Comenzamos dando a nuestro contenedor y formulario un alto del 100%. Como este último ya es flexible y tiene la dirección de columnas, solo debemos agregarle en la mediquery: justify-content: space-between.

Esta propiedad posiciona el contenido horizontalmente cuando el valor de flex-direction es row. En nuestro caso, el valor es columns por lo que justify-content va a aplicar verticalmente.

Space-beetween distribuye los items uniformemente dejando el primer elemento al inicio y el último al final.

[🡡 volver al inicio](#tabla-de-contenido)

## Página de inicio

La página de inicio es la página web principal de un sitio web y lo primero que verán las personas al conocer tu marca. En este caso contiene una imagen por cada producto, con su precio y nombre, también un ícono que va a permitir agregar el artículo al carrito de compras.

En este nuevo módulo trabajaremos las vistas principales. Comenzamos con el HTML de la página de inicio, es decir, las cards que ayudan al usuario a revisar cuáles son los productos disponibles en un e-commerce.

### Cómo crear la estructura HTML de la página de inicio

Estos son los pasos a seguir para maquetar las secciones de un e-commerce.

1. Creamos una sección principal

    ```html
    <section class="main-container"></section>
    ```

2. Dentro colocamos un div que funcionara como contenedor de las tarjetas, permitiéndonos centrarlas

    ```html
    <div class="cards-container"></div>
    ```

3. Por último estructuramos una tarjeta y la repetimos varias veces

    ```html
    <div class="product-card">
            <img src="https://images.pexels.com/photos/276517/pexels-photo-276517.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940" alt="">
            <div class="product-info">
              <div>
                <p>$120,00</p>
                <p>Bike</p>
              </div>
              <figure>
                <img src="./icons/bt_add_to_cart.svg" alt="">
              </figure>
            </div>
          </div>
    ```

### Cómo colocar imágenes en HTML

El elemento HTML img incrusta una imagen dentro de un documento. Su atributo de “src” es para mostrar en dónde se encuentra la imagen. Puede ser en alguna carpeta o una URL.

Por su parte, alt sirve para agregar una descripción a nuestra imagen. Esto es útil por cuestiones de SEO (optimización para buscadores) y también para mejorar la accesibilidad del sitio.

### ¿Qué contenedores usar?

Existen dos etiquetas que nos permiten organizar imágenes de una manera semántica.

- Figure
- Picture

### Cómo implementar CSS Grid para centrar varias imágenes

Trabajaremos en el contenedor principal, cuya clase es cards-container. Con display:grid creamos las grillas y luego las columnas con grid-template-columns y usamos la función repeat para que repita nuestro fragmento de código.

Con auto-fill nos aseguramos que la grilla ocupe el 100% del espacio disponible. Después generamos un espacio entre los items con gap. Finalmente, alineamos horizontal y verticalmente empleando place-content.

El CSS quedaría así:

```css
 .cards-container {
      display: grid;
      grid-template-columns: repeat(auto-fill, 240px);
      gap: 26px;
      place-content: center;
    }
```

Ahora debemos ajustar el tamaño de las imágenes.

```css
 .product-card {
      width: 240px;
    }
    .product-card img {
      width: 240px;
      height: 240px;
      border-radius: 20px;
      object-fit: cover;
    }
```

### Misma clase, estilos diferentes

Queremos que las tarjetas de la página de inicio muestren el precio del artículo y debajo el nombre de este con un tamaño de fuente y color diferentes.

Al lado de ambos debe estar el ícono del carrito de compras.

Para conseguir este resultado debemos:

Aplicarle FlexBox al contenedor

```css
.product-info {
      display: flex;
      justify-content: space-between;
      align-items: center;
      margin-top: 12px;
    }
```

Ajustar el tamaño del ícono

```css
.product-info figure {
      margin: 0;
    }
    .product-info figure img {
      width: 35px;
      height: 35px;
    }
```

Utilizar nth-child en las etiquetas p

```css
    .product-info div p:nth-child(1) {
      font-weight: bold;
      font-size: var(--md);
      margin-top: 0;
      margin-bottom: 4px;
    }
    .product-info div p:nth-child(2) {
      font-size: var(--sm);
      margin-top: 0;
      margin-bottom: 0;
      color: var(--very-light-pink);
    }
```

La pseudo-clase nth-child hace posible que le apliquemos estilos diferentes a los párrafos sin necesidad de asignarles una clase a cada uno.

### Página de inicio responsive con solo 8 líneas de código

Asignando media queries conseguimos que las cards se vean bien en diferentes pantallas, es decir, desarrollamos una página de incio responsiva.

Como implementamos CSS Grid, lo único que necesitamos es disminuir el tamaño de las imágenes, de la siguiente forma:

```css
    @media (max-width: 640px) {
      .cards-container {
        grid-template-columns: repeat(auto-fill, 140px);
      }
      .product-card {
        width: 140px;
      }
      .product-card img {
        width: 140px;
        height: 140px;
      }
    }
```

[🡡 volver al inicio](#tabla-de-contenido)

## Menú

Un menú desplegable o, lista desplegable, es un elemento de control gráfico que muestra al usuario una variedad de opciones de una categoría que puede elegir para realizar una acción como una compra. Esta tiene dos estados: activa o inactiva. Cuando está inactiva, enseña un solo valor.

### Cómo hacer una lista desplegable en HTML5

Esta sección del menú desktop tiene tres items, que le permitirán al usuario escoger entre: ingresar a su cuenta, ver sus órdenes o salir de la página. Es decir, forman una lista de opciones.

Recuerda que la semántica de HTML5 requiere que los elementos de las listas ( li ) estén dentro de una etiqueta contenedora especial ( ul / ol ).

Por lo tanto, la estructura es la siguiente:

```html
<div class="desktop-menu">
    <ul>
      <li>
        <a href="/" class="title">My orders</a>
      </li>

      <li>
        <a href="/">My account</a>
      </li>

      <li>
        <a href="/">Sign out</a>
      </li>
    </ul>
  </div>
```

### Estilos de CSS para listas dentro del menú

Esta vista del menú es como una caja que aparecerá cuando el usuario haga clic en su email. Por ahora, solo maquetaremos, puesto que en el curso de React.js le daremos funcionalidad.

Por lo que, debemos darle dimensiones y espaciado al contenedor.

```css
.desktop-menu {
      width: 100px;
      height: auto;
      border: 1px solid var(--very-light-pink);
      border-radius: 6px;
      padding: 20px 20px 0 20px;
    }
```

Ahora, le quitamos los estilos por defecto a la lista.

```css
    .desktop-menu ul {
      list-style: none;
      padding: 0;
      margin: 0;
    }
```

Finalmente, podemos definir la visual como nos especificó diseño.

```css
    .desktop-menu ul li {
      text-align: end;
    }
    .desktop-menu ul li:nth-child(1),
    .desktop-menu ul li:nth-child(2) {
      font-weight: bold;
    }
    .desktop-menu ul li:last-child {
      padding-top: 20px;
      border-top: 1px solid var(--very-light-pink);
    }
    .desktop-menu ul li:last-child a {
      color: var(--hospital-green);
      font-size: var(--sm);
    }
    .desktop-menu ul li a {
      color: var(--back);
      text-decoration: none;
      margin-bottom: 20px;
      display: inline-block;
    }
```

Utilizamos display: inline-block para definirle un margin-bottom, puesto que a los elementos inline no es posible aplicarles la propiedad margin.

### Menú mobile

Es momento de crear el menú de navegación para la versión móvil o responsive de nuestra tienda virtual y esta estructura presenta tres listas con distintas opciones. Recuerda que configurar esta versión del sitio ayuda a que pueda fluir mejor en todos los tamaños de pantalla y ahorra tiempo porque no necesitas tener dos versiones de un sitio web.

### Estructura semántica de un menú para dispositivos móviles

El menú para la version móvil de nuestra tienda contiene tres secciones y al ser listas las podemos contener en etiquetas ul. Primero, debemos generar el contenedor principal que posibilitará su posterior estilización.

```html
<div class="mobile-menu">
```

En segundo lugar, definimos las secciones. La primera sección corresponde a las categorías

```html
  <ul>
    <li>
      <a href="/">CATEGORIES</a>
    </li>
    <li>
      <a href="/">All</a>
    </li>
    <li>
      <a href="/">Clothes</a>
    </li>
    <li>
      <a href="/">Electronics</a>
    </li>
    <li>
      <a href="/">Furnitures</a>
    </li>
    <li>
      <a href="/">Toys</a>
    </li>
    <li>
      <a href="/">Other</a>
    </li>
  </ul>
```

Luego, tenemos las órdenes y cuenta del usuario.

```html
  <ul>
    <li>
      <a href="/">My orders</a>
    </li>
    <li>
      <a href="/">My account</a>
    </li>
  </ul>
```

Finalmente, mostramos su email y la posibilidad de salir de la página.

```html
  <ul>
    <li>
      <a href="/" class="email">platzi@example.com</a>
    </li>
    <li>
      <a href="/" class="sign-out">Sign out</a>
    </li>
  </ul>
```

### Especifidad en CSS

Tal como hicimos con el menú desktop, para estilizar esta vista, debemos quitar la decoración por defecto de las listas y etiquetas a, separ los contenedores definiendo margin y padding; añadir los colores y estilos de fuente.

Así quedaría nuestro CSS:

```css
  .mobile-menu {
    padding: 24px;
  }
  .mobile-menu a {
    text-decoration: none;
    color: var(--black);
    font-weight: bold;
    /* margin-bottom: 24px; */
  }
  .mobile-menu ul {
    padding: 0;
    margin: 24px 0 0;
    list-style: none;
  }
  .mobile-menu ul:nth-child(1) {
    border-bottom: 1px solid var(--very-light-pink);
  }
  .mobile-menu ul li {
    margin-bottom: 24px;
  }
  .email {
    font-size: var(--sm);
    font-weight: 300;
  }
  .sign-out {
    font-size: var(--sm);
    color: var(--hospital-green);
  }
```

En la última sección tenemos un problema de especificidad. No se está aplicando el font-weight de la clase email, ni el color de la clase sing-out.

La especificidad consiste en dar un valor a una regla CSS sobre qué tan específico es el estilo, esto para que los navegadores puedan saber qué estilos aplicar sobre otros, independientemente de dónde se encuentren en el código. El estilo se aplicará donde la especificidad sea mayor.

Al entender los tipos de especificidad, comprendemos que demos aumentar el valor o peso de las clases email y sing-out.

Existen varias formas de conseguirlo. Una es hacer uso de !important.

```css
  .email {
    font-weight: 300 !important;
  }
  .sign-out {
    color: var(--hospital-green) !important;
  }
```

Otra manera es llamar a las dos clases.

```css
  .mobile-menu .menu-email {
    font-size: var(--sm);
    font-weight: 300;
  }
  .mobile-menu .menu-signout {
    font-size: var(--sm);
    color: var(--hospital-green);
  }
```

[🡡 volver al inicio](#tabla-de-contenido)

## Mi Orden

Ahora maquetaremos la pantalla llamada “my order”* cuya función es mostrar los artículos seleccionados por el usuario dentro de una tienda virtual o marketplace. Esta es la estructura que se espera que puedas crear según la vista de cada dispositivo.

### Cómo hacer la maqueta de una orden de pedidos en HTML

La orden de pedidos le mostrará al usuario los productos que seleccionó, el monto total de dinero, la fecha y la cantidad total de artículos.

Por lo tanto, nuestra maqueta contiene:

1. Div “my order” → contenedor principal
2. Div “my order container” → nos permitirá alinear el contenido con mayor facilidad
3. Título → en la versión móvil sube al menú
4. Div “my order content” → tipo barra contenedora de texto con la fecha, cantidad de artículos y total de dinero
5. Div “shopping cart” → con la imagen del arítculo y texto especificando su nombre y precio.

El código HTML resultante es el siguiente:

```html
<div class="my-order">
  <div class="my-order-container">
    <h1 class="title">My order</h1>

    <div class="my-order-content">
      <div class="order">
        <p>
          <span>03.25.21</span>
          <span>6 articles</span>
        </p>
        <p>$560.00</p>
      </div>

      <div class="shopping-cart">
        <figure>
          <img src="https://images.pexels.com/photos/276517/pexels-photo-276517.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940" alt="bike">
        </figure>
        <p>Bike</p>
        <p>$30,00</p>
      </div>
      
    </div>
  </div>
</div>
```

### Cómo aplicar CSS en una orden de compra

Una orden de compra tiene una cantidad indefinida de artículos y por eso debemos implementar estilos de CSS que funcionen tanto para ventas menores como para ventas mayores de miles de artículos.

¿Qué debemos hacer para construir estas dos vistas? Sigue estos pasos:

Define las dimensiones del contendor principal y centra su contenido

```css
  .my-order {
    width: 100%;
    height: 100vh;
    display: grid;
    place-items: center;
  }
```

La medida relativa vh, viewport height, define la altura del contenedor. En este caso le estamos diciendo que sea del total de la pantalla.

Establece el tamaño de la fuente del título y su separación de la barra de totales

```css
  .title {
    font-size: var(--lg);
    margin-bottom: 40px;
  }
```

Prepara la grilla de CSS Grid

```css
  .my-order-container {
    display: grid;
    grid-template-rows: auto 1fr auto;
    width: 300px;
  }
```

Brinda espacio a los elementos y confecciona otra grilla

```css
  .my-order-content {
    display: flex;
    flex-direction: column;
  }
    .order {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 16px;
    align-items: center;
    background-color: var(--text-input-field);
    margin-bottom: 24px;
    border-radius: 8px;
    padding: 0 24px;
  }
  .order p:nth-child(1) {
    display: flex;
    flex-direction: column;
  }
  .order p span:nth-child(1) {
    font-size: var(--md);
    font-weight: bold;
  }
  .order p span:nth-child(2) {
    font-size: var(--sm);
    color: var(--very-light-pink);
  }
  .order p:nth-child(2) {
    text-align: end;
    font-weight: bold;
  }
```

Define la parte visual de “shopping cart”

```css
  .shopping-cart {
    display: grid;
    grid-template-columns: auto 1fr auto auto;
    gap: 16px;
    margin-bottom: 24px;
    align-items: center;
  }
  .shopping-cart figure {
    margin: 0;
  }
  .shopping-cart figure img {
    width: 70px;
    height: 70px;
    border-radius: 20px;
    object-fit: cover;
  }
  .shopping-cart p:nth-child(2) {
    color: var(--very-light-pink);
  }
  .shopping-cart p:nth-child(3) {
    font-size: var(--md);
    font-weight: bold;
  }
```

### ¿Qué logra object-fit en CSS?

A las imágenes le aplicamos la propiedad object-fit, ya que resuelve como el contenido se ajustará a su contendor.

Sus valores pueden ser:

- contain → mantiene la relación de aspecto mientras le ajusta dentro del contendedor.
- cover → mantiene la realción de aspecto, pero la ajusta para llenar el contenedor.
- fill → modifica su tamaño para llenar el contenedor.
- none → no se redimensiona.
- scale-down → el contenido se dimensiona como si none o contain estuvieran especificados, lo que resulta en un tamaño de objeto concreto más pequeño.

[🡡 volver al inicio](#tabla-de-contenido)

## Mis Ordenes

### HTML para mostrar las órdenes de compra

La sección de órdenes contiene la fecha, cantidad total de artículos y monto total de dinero de cada orden solicitada por el usuario. Recuerda que en este momento solo estamos maquetando, luego con JavaScript conseguiremos que los datos sean dinámicos.

La estructura es la siguiente:

```html
  <div class="my-order">
    <div class="my-order-container">
      <h1 class="title">My orders</h1>

      <div class="my-order-content">
      
        <div class="order">
          <p>
            <span>03.25.21</span>
            <span>6 articles</span>
          </p>
          <p>$560.00</p>
          <img src="./icons/flechita.svg" alt="arrow">
        </div> 
        
      </div>
    </div>
  </div>
```

### Estilos CSS para crear listas de órdenes pedidas

Como la vista de órdenes es muy similar a la sección “mi orden”, implementaremos los mismos estilos.

Nuestro CSS final se ve así:

```css
  .my-order {
    width: 100%;
    height: 100vh;
    display: grid;
    place-items: center;
  }
  .title {
    font-size: var(--lg);
    margin-bottom: 40px;
  }
  .my-order-container {
    display: grid;
    grid-template-rows: auto 1fr auto;
    width: 300px;
  }
  .my-order-content {
    display: flex;
    flex-direction: column;
  }
  .order {
    display: grid;
    grid-template-columns: auto 1fr auto;
    gap: 16px;
    align-items: center;
    margin-bottom: 12px;
  }
  .order p:nth-child(1) {
    display: flex;
    flex-direction: column;
  }
  .order p span:nth-child(1) {
    font-size: var(--md);
    font-weight: bold;
  }
  .order p span:nth-child(2) {
    font-size: var(--sm);
    color: var(--very-light-pink);
  }
  .order p:nth-child(2) {
    text-align: end;
    font-weight: bold;
  }
```

[🡡 volver al inicio](#tabla-de-contenido)

## Navbar

Para crear un menú en HTML5 se emplea la etiqueta nav. Este elemento respeta la semántica, puesto que representa una sección de la página cuyo propósito es proporcionar enlaces de navegación.
Estos enlaces de navegación pueden ser etiquetas a dentro de listas o íconos.

Nuestra estructura quedaría así:

```html
  <nav>
    <img src="./icons/icon_menu.svg" alt="menu" class="menu">

    <div class="navbar-left">
      <img src="./logos/logo_yard_sale.svg" alt="logo" class="logo">

      <ul>
        <li>
          <a href="/">All</a>
        </li>
        <li>
          <a href="/">Clothes</a>
        </li>
        <li>
          <a href="/">Electronics</a>
        </li>
        <li>
          <a href="/">Furnitures</a>
        </li>
        <li>
          <a href="/">Toys</a>
        </li>
        <li>
          <a href="/">Others</a>
        </li>
      </ul>
    </div>

    <div class="navbar-right">
      <ul>
        <li class="navbar-email">platzi@example.com</li>
        <li class="navbar-shopping-cart">
          <img src="./icons/icon_shopping_cart.svg" alt="shopping cart">
          <div>2</div>
        </li>
      </ul>
    </div>
  </nav>
```

### Estilos básicos de CSS para menú

Darle estilos a un menú es muy sencillo con CSS3. Debemos alinear los elementos en una barra horizontal para que ocupen el total de la pantalla.

¿Cómo lograr estilizar este menú? Sigue los siguientes pasos.

1. Oculta de la vista el ícono de menú, ya que solo debe ser visto cuando el usuario navega con un dispositivo móvil.

    ```css
    .menu {
      display: none;
    }
    ```

2. Remueve la decoración de los enlaces y listas

    ```css
    text-decoration: none;
    list-style: none;
    ```

3. Centra los elementos con Flexbox, eliminar el padding y margin por defecto de las etiquetas y define los colores y tamaño de las fuentes

    ```css
      body {
        margin: 0;
        font-family: 'Quicksand', sans-serif;
      }
      nav {
        display: flex;
        justify-content: space-between;
        padding: 0 24px;
        border-bottom: 1px solid var(--very-light-pink);
      }
      .logo {
        width: 100px;
      }
      .navbar-left ul,
      .navbar-right ul {
        list-style: none;
        padding: 0;
        margin: 0;
        display: flex;
        align-items: center;
        height: 60px;
      }
      .navbar-left {
        display: flex;
      }
      .navbar-left ul {
        margin-left: 12px;
      }
      .navbar-left ul li a,
      .navbar-right ul li a {
        text-decoration: none;
        color: var(--very-light-pink);
        border: 1px solid var(--white);
        padding: 8px;
        border-radius: 8px;
      }
      .navbar-left ul li a:hover,
      .navbar-right ul li a:hover {
        border: 1px solid var(--hospital-green);
        color: var(--hospital-green);
      }
      .navbar-email {
        color: var(--very-light-pink);
        font-size: var(--sm);
        margin-right: 12px;
      }
    ```

4. Aplica los cambios para móvil.

    ```css
      @media (max-width: 640px) {
        .menu {
          display: block;
        }
        .navbar-left ul {
          display: none;
        }
        .navbar-email {
          display: none;
        }
      }
    ```

### Cómo centrar el carrito de compras en la barra de navegación

El mayor desafío es posicionar el carrito de compras junto al número. Este el contador que le mostrará al usuario cuantos artículos lleva agregados a su orden.

Para lograrlo emplearemos position relative y absolute.

```css
  .navbar-shopping-cart {
    position: relative;
  }
  .navbar-shopping-cart div {
    width: 16px;
    height: 16px;
    background-color: var(--hospital-green);
    border-radius: 50%;
    font-size: var(--sm);
    font-weight: bold;
    position: absolute;
    top: -6px;
    right: -3px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
```

### Lista desplegable en menú

Diseño recomendó que al lado de la dirección de email aparezca una flecha que permitirá al usuario desplegar el menú con las opciones: “my orders”, “my account” y “sing-out”.

Puedes agregarla con estas líneas de HTML

```html
    <li class="email-nav">johndoe@gmail.com
      <img src="./assets/icons/flechita.svg" alt="">
    </li>
```

Sus estilos son:

```css
  .email-nav img{
    margin-left: 10px;
    transform: rotate(90deg);
  }
```

[🡡 volver al inicio](#tabla-de-contenido)

## Detalle de Producto

### Uso de aside en HTML5

Esta vista la podemos incluir dentro de la etiqueta aside, puesto que este elemento representa una sección de la página que consiste en contenido que está indirectamente relacionado con el principal del documento.

Debemos considerar que la descripción del producto es variable y es importante que comprobemos que se vea bien con diferentes cantidades de palabras. Para esto podemos hacer utilizar el texto simulado de Lorem Ipsum.

La estructura completa es:

```html
  <aside class="product-detail">
    <div class="product-detail-close">
      <img src="./icons/icon_close.png" alt="close">
    </div>
    <img src="https://images.pexels.com/photos/276517/pexels-photo-276517.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940" alt="bike">
    <div class="product-info">
      <p>$35,00</p>
      <p>Bike</p>
      <p>With its practical position, this bike also fulfills a decorative function, add your hall or workspace.</p>
      <button class="primary-button add-to-cart-button">
        <img src="./icons/bt_add_to_cart.svg" alt="add to cart">
        Add to cart
      </button>
    </div>
  </aside>
```

### Cómo estilizar un componente aside

Para el aside, en nuestro caso, el detalle de producto, podemos reutilizar algunos de los estilos que ya definimos, así mantendremos un tono uniforme en la tienda virtual.

Los pasos que deberías aplicar son los siguientes:

1. Añade al botón la clase “primary-button” y luego añade otra para poder implementar Flexbox
  
    ```css
      .primary-button {
        background-color: var(--hospital-green);
        border-radius: 8px;
        border: none;
        color: var(--white);
        width: 100%;
        cursor: pointer;
        font-size: var(--md);
        font-weight: bold;
        height: 50px;
      }
      .add-to-cart-button {
        display: flex;
        align-items: center;
        justify-content: center;
      }
    ```

2. Estiliza la imagen y la “x” de cerrar la vista

    Como tenemos más de una imagen dentro de la misma clase contenedora, empleamos el selector combinador “hijo directo”.

    ```css
      .product-detail {
        width: 360px;
        padding-bottom: 24px;
        position: absolute;
        right: 0;
      }
      .product-detail-close {
        background: var(--white);
        width: 14px;
        height: 14px;
        position: absolute;
        top: 24px;
        left: 24px;
        z-index: 2;
        padding: 12px;
        border-radius: 50%;
      }
      .product-detail-close:hover {
        cursor: pointer;
      }
      .product-detail > img:nth-child(2) {
        width: 100%;
        height: 360px;
        object-fit: cover;
        border-radius: 0 0 20px 20px;
      }
    ```

3. Continúa con la parte que enseña la información

    ```css
      .product-info {
        margin: 24px 24px 0 24px;
      }
      .product-info p:nth-child(1) {
        font-weight: bold;
        font-size: var(--md);
        margin-top: 0;
        margin-bottom: 4px;
      }
      .product-info p:nth-child(2) {
        color: var(--very-light-pink);
        font-size: var(--md);
        margin-top: 0;
        margin-bottom: 36px;
      }
      .product-info p:nth-child(3) {
        color: var(--very-light-pink);
        font-size: var(--sm);
        margin-top: 0;
        margin-bottom: 36px;
      }
    ```

4. Modifica el width para que ocupe el 100% de la pantalla de un móvil

    ```css
      @media (max-width: 640px) {
        .product-detail {
          width: 100%;
        }
      }
    ```

### Slider con imágenes del producto

Hasta aquí el detalle solamente tiene una imagen, pero es muy común que sean más. Así, el usuario puede hacerse una idea más clara de lo que está por comprar. Diseño propone esto con los “puntitos” que aparecen debajo de la heladera.

Una forma de lograrlo es agregándole al HTML justo debajo de la etiqueta img las siguientes líneas:

```html
  <div class="dots">
    <span class="dot"></span>
    <span class="dot"></span>
    <span class="dot"></span>
  </div>
```

Estos son los estilos:

```css
  .dots {
      text-align: center;
  }

  .dot {
      cursor: pointer;
      height: 8px;
      width: 8px;
      margin: 0 2px;
      background-color: var(--very-light-pink);
      border-radius: 50%;
      display: inline-block;
  }

  .dots span:nth-child(1) {
      background-color: var(--hospital-green);
  }
```

[🡡 volver al inicio](#tabla-de-contenido)

## Carrito de compras

El carrito de compras es la sección de la página que le permitirá al usuario ver los productos que agregó porque quiere comprarlos. Como puedes ver en la imagen, es una vista muy similar a sección "mi orden", por lo que utilizaremos el mismo código.

Solo nos falta elaborar nuestra pantalla del carrito para terminar nuestra página. Como se mencionó, es un proceso muy similar a los anteriores y podemos reutilizar el código de "my orders" .

### Maquetado básico con HTML de un carrito de compras

Llegó la hora de maquetar esta sección de la plataforma en HTML. Emplea estas líneas de código como guía para verificar que hayas hecho un gran trabajo y recuerda no memorizarlas, para garantizar que hayas aprendido correctamente.

```html
  <aside class="product-detail">
    <div class="title-container">
      <img src="./icons/flechita.svg" alt="arrow">
      <p class="title">My order</p>
    </div>

    <div class="my-order-content">
      
      <div class="shopping-cart">
        <figure>
          <img src="https://images.pexels.com/photos/276517/pexels-photo-276517.jpeg?auto=compress&cs=tinysrgb&dpr=2&h=650&w=940" alt="bike">
        </figure>
        <p>Bike</p>
        <p>$30,00</p>
        <img src="./icons/icon_close.png" alt="close">
      </div>
      
      <button class="primary-button">
        Checkout
      </button>
    </div>
  </div>
  </aside>
```

### Estilos CSS para un carrito de compras

Los estilos de CSS para el carrito son, prácticamente, los mismos que para la sección que le muestra al usuario su orden de compra.

El CSS sugerido es:

```css
  .product-detail {
    width: 360px;
    padding: 24px;
    box-sizing: border-box;
    position: absolute;
    right: 0;
  }
  .title-container {
    display: flex;
  }
  .title-container img {
    transform: rotate(180deg);
    margin-right: 14px;
  }
  .title {
    font-size: var(--lg);
    font-weight: bold;
  }
  .order {
    display: grid;
    grid-template-columns: auto 1fr;
    gap: 16px;
    align-items: center;
    background-color: var(--text-input-field);
    margin-bottom: 24px;
    border-radius: 8px;
    padding: 0 24px;
  }
  .order p:nth-child(1) {
    display: flex;
    flex-direction: column;
  }
  .order p span:nth-child(1) {
    font-size: var(--md);
    font-weight: bold;
  }
  .order p:nth-child(2) {
    text-align: end;
    font-weight: bold;
  }
  .shopping-cart {
    display: grid;
    grid-template-columns: auto 1fr auto auto;
    gap: 16px;
    margin-bottom: 24px;
    align-items: center;
  }
  .shopping-cart figure {
    margin: 0;
  }
  .shopping-cart figure img {
    width: 70px;
    height: 70px;
    border-radius: 20px;
    object-fit: cover;
  }
  .shopping-cart p:nth-child(2) {
    color: var(--very-light-pink);
  }
  .shopping-cart p:nth-child(3) {
    font-size: var(--md);
    font-weight: bold;
  }
  .primary-button {
    background-color: var(--hospital-green);
    border-radius: 8px;
    border: none;
    color: var(--white);
    width: 100%;
    cursor: pointer;
    font-size: var(--md);
    font-weight: bold;
    height: 50px;
  }
  @media (max-width: 640px) {
    .product-detail {
      width: 100%;
    }
  }
```

### ¿Qué es tranform en CSS?

Transform que es una propiedad de CSS que nos permite trasladar, rotar, escalar o sesgar elementos.
Se implementan principalmente para desarrollar animaciones. Para rotar la flechita lo empleamos.

[🡡 volver al inicio](#tabla-de-contenido)
