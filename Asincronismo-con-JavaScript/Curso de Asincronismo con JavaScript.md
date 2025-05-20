# Curso de Asincronismo con JavaScript <!-- omit in toc -->

## Tabla de Contenido<!-- omit in toc -->

- [Qué es el asincronismo](#qué-es-el-asincronismo)
- [Formas de manejar la asincronía en JavaScript](#formas-de-manejar-la-asincronía-en-javascript)
- [Event Loop](#event-loop)
- [Qué son los Callbacks](#qué-son-los-callbacks)
- [XMLHTTPRequest](#xmlhttprequest)
  - [Métodos y propiedades](#-métodos-y-propiedades)
  - [Características del protocolo http](#-características-del-protocolo-http)
- [Fetch Data](#fetch-data)
- [Promesas](#qué-son-las-promesas)
- [Funciones asíncronas](#funciones-asíncronas)
- [Try/Catch](#-try-catch)
- [Generadores](#generadores)

## Qué es el asincronismo

Conceptos importantes para entender el asincronismo:

- 🧵 Thread: Thread para Javascript permite realizar programación multihilos en este entorno. En realidad, simula la creación y ejecución de hilos, pero para el desarrollador es lo mismo. Ésto simplifica muchísimo la creación de aplicaciones Javascript.
- 🚫 Bloqueante: Una llamada u operación bloqueante no devuelve el control a la aplicación hasta que se ha completado. Por tanto el thread queda bloqueado en estado de espera.
- 🚿 No bloqueante: Una tarea no bloqueante se devuelve inmediatamente con independencia del resultado. Si se completó, devuelve los datos. Si no, un error.
- 🎞️ Síncrono: Las tareas se ejecutan de forma secuencial, se debe esperar a que se complete para continuar con la siguiente tarea.
- 🚦 Asíncrono: Las tareas pueden ser realizadas más tarde, lo que hace posible que una respuesta sea procesada en diferido. La finalización de la operación I/O (entrada/salida) se señaliza más tarde, mediante un mecanismo específico como por ejemplo un callback, una promesa o un evento, lo que hace posible que la respuesta sea procesada en diferido.
- 🛤️ Paralelismo: El paralelismo es la ejecución simultánea de dos o más tareas. Algunas tareas se pueden dividir en partes más pequeñas que pueden ser resueltas simultáneamente.
- 🎮 Concurrencia: La concurrencia es la capacidad de un algoritmo o programa para ejecutar más de una tarea a la vez. El concepto es similar al procesamiento paralelo, pero con la posibilidad de que muchos trabajos independientes hagan diferentes cosas a la vez en lugar de ejecutar el mismo trabajo.
- 🌀 Eventloop o Loop de eventos: El bucle de eventos es un patrón de diseño que espera y distribuye eventos o mensajes en un programa.

## Formas de manejar la asincronía en JavaScript

- 📩 Callbacks: Una función que se pasa como argumento de otra función y que será invocada.
- 🫱🏼‍🫲🏾 Promesas: (implementado en ES6) Una promesa es una función no-bloqueante y asíncrona la cual puede retornar un valor ahora, en el futuro o nunca.
- 🛣️ Async / Await: (implementado en ES2017) Permite estructurar una función asincrónica sin bloqueo de una manera similar a una función sincrónica ordinaria.

📌 En JavaScript casi todas las operaciones de I/O (Entrada y Salida) no se bloquean. A esto se le conoce como asíncronismo. Lo único que no es procesado antes de que termine la operación son los callbacks, ya que éstos están amarrados a una operación y esperan a que sea finalizada para poder ejecutarse.

⏳ El asincronismo es una manera de aprovechar el tiempo y los recursos de la aplicación, ejecutando tareas y procesos mientras otros son resueltos en background (como la llegada de la información de una API), para posteriormente continuar con las tareas que requerían esa información que no tenías de manera instantánea.

⏲️ Un ejemplo fácil de asincronismo vs sincronismo es invitar a unos amigos a una fiesta y ofrecer una parrillada. Primero decides colocar la carne y verduras a la parrilla y luego repartir bebidas y algo para picar (snacks). Si fuera **una persona síncrona** (Blocking) tendrías que esperar a que la comida de la parrilla esté cocinada y luego atender a los invitados. Pero si fuera **una persona asíncrona** (Non Blocking) luego de poner la carne al carbón, sacas las bebidas frías de la nevera y compartes con los invitados mientras se cocina la carne. La acción de que la comida en la parrillada esté lista sería **un callback** que está esperando que finalice el proceso para ejecutarse. Pero otros procesos (como compartir la velada con bebidas y algo de picar) ya podrían irse realizando.

## Event Loop

Para entender el **Event Loop**, se muestra que la primera tarea asignada (mostrar por Consola la palabra: "start") pasa por el Call Stack luego se imprime en consola. Cuando el Call Stack tiene el "setTimeout" se debe esperar un periodo de tiempo en este caso 5 segundos para imprimir el mensaje: "Callback Function", ahí es cuando vemos en Web APIs **el timer**. Mientras tanto, el código sigue corriendo a la siguiente tarea para imprimir en consola la palabra: "end".

El Event Loop es la tarea asignada (en este ejemplo el "callbackFn()") para mover del Task Queue al Stack, **solo si el stack está vacío**

## 🗄️ Javascript se organiza usando las siguientes estructuras de datos

- 🗃️ Memory Heap: Región de memoria libre de gran tamaño, dedicada al alojamiento dinámico de objetos (asignado a un montículo). Es compartida por todo el programa y controlada por un recolector de basura que se encarga de liberar aquello que no se necesita, es decir de forma desorganizada se guarda información de las variables y del scope.
- 🔋 Call Stack (pila LIFO: Last-in, First-out): Apila de forma organizada las instrucciones de nuestro programa. La pila de llamadas, se encarga de albergar las instrucciones que deben ejecutarse. Nos indica en que punto del programa estamos, por donde vamos.
- 🚗🚕🚙 Task Queue (cola): Cada vez que nuestro programa recibe una notificación del exterior o de otro contexto distinto al de la aplicación, el mensaje se inserta en una cola de mensajes pendientes y se registra su callback correspondiente. El stack debe estar vacío para que esto suceda.
- 🚗🚕 Micro Task Queue: Aquí se agregan las promesas. Esta Queue es la que tiene mayor prioridad.

## Conceptos fundamentales antes de crear el proyecto

- Web APIs JavaScript del lado del cliente: setTimeout, XMLHttpRequest, File Reader, DOM. Node: fs, https.
- API: El término API es una abreviatura de “Application Programming Interface” (Interfaz de programación de aplicaciones en español). Es un conjunto de rutinas que provee acceso a funciones de un determinado software.
- Hoisting: Sugiere que las declaraciones de variables y funciones son físicamente movidas al comienzo del código en tiempo de compilación.
- XML: Lenguaje de marcado creado para la transferencia de información, legible tanto para seres humanos como para aplicaciones informáticas, y basado en una sencillez extrema y una rígida sintaxis. Así como el HTML estaba basado y era un subconjunto de SGML, la reformulación del primero bajo la sintaxis de XML dio lugar al XHTML; XHTML es, por tanto, un subconjunto de XML.
- DOM: El DOM permite acceder y manipular las páginas XHTML como si fueran documentos XML. De hecho, DOM se diseñó originalmente para manipular de forma sencilla los documentos XML.
- Events: Comportamientos del usuario que interactúa con una página que pueden detectarse para lanzar una acción, como por ejemplo que el usuario haga click en un elemento (onclick), que elija una opción de un desplegable (onselect), que pase el ratón sobre un objeto (onmouseover), etc.
- Compilar: Compilar es generar código ejecutable por una máquina, que puede ser física o abstracta como la máquina virtual de Java.
- Transpilar: Transpilar es generar a partir de código en un lenguaje código en otro lenguaje. Es decir, un programa produce otro programa en otro lenguaje cuyo comportamiento es el mismo que el original.

## Qué son los Callbacks

🪃 Un Callback es una una función que se pasa como argumento de otra función y que será invocada.

### ✏️ Ejemplos

- En **VSC** crear una carpeta dentro de la carpeta **src** llamada callback.
- Crear dentro de la carpeta **callback** el archivo index.js
- Dentro de **index.js** se coloca la estructura de los que será un **callback**:

```javascript
function sum(num1, num2) {
  return num1 + num2;
}

function calc(num1, num2, callback) {
  return callback(num1, num2);
} //No necesariamente se debe llamar callback

console.log(calc(2, 2, sum)); //sum debe estar sin () y sin argumentos
```

- Luego se selecciona el código y al dar click derecho, seleccionar Run Code (debe estar instalado la extensión **Code Runner**).
- Aparece abajo la consola con la salida de la suma de los 2 números.
- Para el segundo ejemplo, se tiene un setTimeout que funciona como un **callback**, en el código está configurado para imprimir el mensaje 2 segundos después de ejecutar el código con Run Code:

```javascript
setTimeout(function () {
  console.log("Hola JavaScript");
}, 2000);
//la función es anónima por eso no tiene nombre
```

En el tercer ejemplo tenemos un setTimeout con una función que se le pasa por argumento:

```javascript
function gretting(name) {
  console.log(`Hola ${name}`);
}

setTimeout(gretting, 2000, "Maria"); //se pasa primero la función, de segundo el tiempo de espera y el argumento
```

## XMLHTTPRequest

📲 **XMLHttpRequest** es un objeto de JS que permite hacer peticiones hacia servicios en la nube(URLs o APIs).

### 📪 Existen 5 estados en un llamado XMLHttpRequest

- 0 → Se ha inicializado.
- 1 → Loading (cargando).
- 2 → Se ha cargado.
- 3 → Procesamiento si existe alguna descarga.
- 4 → Completado.

### 📫 Métodos y propiedades

- xmlhttp.open() → Prepara la petición para ser enviada tomando tres parámetros: prótocolo, url, asíncrono (true).
- xmlhttp.readyState → Retorna el estado de la petición.
- xmlhttp.onreadystatechange → Un eventHandler que es llamado cuando la propiedad readyState cambia.
- xmlhttp.status → Retorna el estado de la respuesta de la petición. (200,400,500)
- xmlhttp.send() → Envía la petición.

### 📬 Características del protocolo http

**Verbos**: Los verbos indican acciones que están asociadas a peticiones y recursos, es decir, sirven para la manipulación de recursos cliente/servidor. Los Verbos http son:

- GET → Solicita un recurso.
- HEAD → Solicita un recurso pero sin retornar información, la estructura de esta petición es igual que get tanto en su headers como estatus. Es útil cuando vamos a utilizar API, para comprobar si lo que vamos a enviar esta correcto y puede ser procesado.
- POST → Sirve para la creación de recursos en el servidor.
- PUT → Actualiza por completo un recurso, reemplaza todas las representaciones actuales del recurso de destino con la carga útil de la petición.
- PATCH → Actualiza parcialmente un recurso.
- DELETE → Elimina un recurso.

📭 **Los códigos de estados del servidor:** . El código de estado (status codes) sirve para describir el estado de la petición hecha al servidor.

- 1xx → Indican que la petición fue recibida por el servidor, pero está siendo procesada por el servidor.
- 2xx → Indican que la petición fue recibida, aceptada y procesada correctamente.
- 3xx → Indican que hay que tomar acciones adicionales para completar la solicitud.
- 4xx → Indican errores del lado del cliente que hizo mal una solicitud.
- 5xx → Indican errores del servidor. Suelen aparecer cuando existe un fallo en la ejecución en el servidor. .

📧 **Los códigos más comunes a la hora de interactuar con una API son:** .

- 200 → OK → Indica que todo está correcto.
- 201 → Created → Todo está correcto cuando se hizo una solicitud POST, el recurso se creó y se guardó correctamente.
- 204 → No Content → Indica que la solicitud se completó correctamente pero no devolvió información. Este es común cuando se hacen peticiones con el verbo DELETE.
- 400 → Bad Request → Indica que algo está mal en la petición (no encontró algo).
- 401 → Unauthorized → Significa que antes de hacer una solicitud al servidor nos debemos autenticar.
- 403 → Forbidden → Indica que no tenemos acceso a ese recurso aunque se esté autenticado.
- 404 → Not Found → Indica que no existe el recurso que se está intentando acceder.
- 500 → Internal Server Error → Indica que algo falló, es un error que retorna el servidor cuando la solicitud no pudo ser procesada.

## Fetch Data

- Para evitar la mala práctica de un **Call Hell**, no es recomendable exceder de 3 callback, para ello se utilizan las promesas o el Async Away.
- Existen varios tipos de **console**, dependiendo del navegador, la fuente o el color cambian de acuerdo al tipo

  ```javascript
  console.info("info"); //muestra un mensaje de información en la consola web
  console.error("error"); //muestra mensaje de un error
  console.warn("warn"); //muestra mensaje de advertencia
  console.log("log"); //para mensajes generales de registro de información
  ```

**CallBacks Hell:** Consiste en múltiples Callbacks anidados que provocan que el código se vuelva difícil de leer y ‘debuggear’ y por eso se debe evitar.

## Qué son las promesas

🪃 Un **callback** devuelve una función en los parámetros, cuando llamamos varias veces un callback, estaremos colocando muchas lineas de código y sería engorroso, por eso nacen las promesas, éstas optimizan y permiten leer mejor el código con pocas lineas.

🫱🏼‍🫲🏾 Las **promesas** son asíncronas, por lo que el código continuará su ejecución normalmente y luego dirá si la promesa se resolvió o se rechazó. Por lo que varias promesas pueden llegar a entrar en ejecución al mismo tiempo.

Las promesas pueden suceder:

- Ahora
- En el futuro
- Nunca

### 🛠️ **Para crear una promesa:**

Utilizamos la palabra reservada new seguida de la palabra Promise que es el constructor de la promesa. Este constructor recibe un único parámetro que es una función, la cuál a su vez, recibe otros dos parámetros: resolve y reject.

- El parámetro **resolve** se utiliza para cuando la promesa devuelve el valor correctamente.
- El parámetro **reject**, se usa en el que caso de que no funcione.

```javascript
const promise = new Promise(function (resolve, reject) {
  resolve("hey!");
});
```

🗃️ Una Promesa puede estar en uno de los siguientes estados:

1. Pendiente pending → Una promesa inicia en este estado: no cumplida, no rechazada.

   - Una promesa inicialmente está endiente.

2. Cumplida fulfilled → Significa que la operación se completó satisfactoriamente, .then(va => …)
   - Cuando llamamos a resolve entonces la promesa pasa a estar resuelta.
   - Cuando una promesa se resuelve entonces se ejecuta la función que pasamos al método .then
3. Rechazada rejected → significa que la operación falló, .catch(err => …)
   - Si llamamos a reject pasa a estar rechazada (obtenemos un error que nos va a indicar la razón del rechazo).
   - Si la promesa es rechazada entonces se ejecuta la función que pasamos a .catch .

### 📝 Ejemplo con then y catch

- Para probar el código, en el proyecto se crea la carpeta llamada **promise** dentro de la carpeta src.
- Se crea el archivo **index.js** en la ruta: src/promise
- El código del ejemplo queda así:

```javascript
//ejemplo de contar vacas
const cows = 15; //valor inicial de vacas

const countCows = new Promise(function (resolve, reject) {
  //solo si el número de vacas supera 10, se llama al resolve
  //de lo contrario: se llama a reject
  if (cows > 10) {
    resolve(`We have ${cows} cows on the farm`);
  } else {
    reject("There is no cows on the farm");
  }
});

//con solo .then se obtiene el resultado de la promesa de acuerdo a resolve o reject
//con .catch podemos obtener más información de un futuro error que se presente
//con .finally podemos imprimir un mensaje que indica que ya se ejecutó la promesa
countCows
  .then((result) => {
    console.log(result);
  })
  .catch((error) => {
    console.log(error);
  })
  .finally(() => console.log("Finally"));
//se usan arrow function () =>
```

## Funciones asíncronas

🔁 **¿Qué es una función asíncrona?** : La declaración de función **async** define una función asíncrona que devuelve un objeto, lo cual permite a un programa correr una función sin congelar todo la compilación. Dada que la finalidad de las funciones async/await es simplificar el comportamiento del uso síncrono de promesas, se hace más fácil escribir promesas.

🔏 La estructura se compone por las palabras reservadas async y await:

1. La palabra async antes de la función, hace que la función devuelva una promesa.
2. La palabra await se utiliza dentro de las funciones async, lo que hace que el programa espere hasta que la variable(promesa) se resuelva para continuar.

✏️ **Ejemplo con código:**

- Ir a VSC, crear dentro de la carpeta src una carpeta llamada **async**.
- En la ruta src/async crear el archivo **index.js**

Dentro del archivo index.js, se crea la promesa y luego se valida si la promesa se resolverá, también se hace el llamado de la misma y luego se busca mostrar como se desenvuelve con await. En el ejemplo se usa el if ternario.

🚥 **¿Qué es un operador if ternario?** . El operador ternario consta de 3 partes: condición ? expresión1 : expresión2;

1. La primera es la lógica, se evalúa una condición.
2. La segunda parte está después del signo de cierre de interrogación ?, ésta se ejecuta solo si la condición es verdadera true.
3. La tercera parte está después del símbolo de dos puntos :, ésta se ejecuta solo si la condición resulta falsa false.

```javascript
var a = 5;
var b = 3;
var c = a > b ? "Es mayor" : "Es menor";
//Si la condición después del símbolo igual (=) se cumple, entonces se tendrá el valor: “Es mayor”, de lo contrario tomará el valor: “Es menor”.
```

El código en src/async/index.js queda así:

```javascript
const fnAsync = () => {
  return new Promise((resolve, reject) => {
    true //se usó operador ternario y se está forzando con true que se cumpla la condición
      ? setTimeout(() => resolve("Async!!", 2000))
      : reject(new Error("Error!")); //arroja "error" en caso de que la condición sea false
  });
};

const anotherFn = async () => {
  //la palabra async es para el cuerpo de la función
  //la palabra await estará dentro de la lógica a implementar
  const something = await fnAsync(); //aquí nos está regresando una promesa
  console.log(something); //se imprime mientras se espera
  console.log("Hello!");
};

console.log("Before"); //al ser la primera orden con solo console.log, 'Before' se imprime primero
anotherFn(); //es el segundo en llamar, pero aún así no se imprimen los console de su lógica y tarda 2 s en ser ejecutada
console.log("After"); //aparece justo después de 'Before' porque anotherFn() está esperando una promesa y aún así el programa no se detiene, sino que sigue y así tenemos 'After' de segundo al imprimir

/*La salida al correr con Run Code queda:
Before
After
Async!!
Hello!
*/
```

🖇️ Otra forma de hacer que async/await espere a varios llamados a la vez es con la estructura

## 🎭 Try /Catch

La palabra reservada try consiste en un bloque que contiene una o más sentencias, como hacíamos con resolve.

- Su cuerpo está conformado por las llaves {} las cuales se deben utilizar siempre, incluso para un bloque de una sola sentencia.

También puede estar presente un bloque con la palabra reservada catch.

- Un bloque catch es opcional (como hacíamos con reject) y contiene sentencias que especifican que hacer si una excepción es lanzada en el bloque try.
- Si no se lanza ninguna excepción en el bloque try, el bloque catch se omite.

✏️ **Ejemplo:** La estructura try / catch se asemeja a if / else, solo que catch puede detectar un error en caso de que haya uno:

```javascript
const anotherFunction = async (url_api) => {
  try {
  } catch (error) {}
};
```

🛠️ - Siguiendo con el proyecto, ir a VSC, crear en src/async el archivo **challenge.js**

El código (comentado) de src/ async/challenge.js queda:

```javascript
import fetch from "node-fetch";
const API = "https://api.escuelajs.co/api/v1";

//Lógica de async: ir por los datos, luego esperar por ellos y finalmente retornarlos hacia el usuario
async function fetchData(urlApi) {
  //siempre async antes de function
  const response = await fetch(urlApi); //hacemos uso del fetch()
  const data = await response.json(); //estructura de los datos transformandolos en json
  return data; //retorna la información de la API que estamos solicitando
}

//también se puede colocar la palabra async antes del argumento y se usa arrow function
const anotherFunction = async (urlApi) => {
  //En try estará todo lo que queremos que suceda con la lógica de la aplicación
  try {
    const products = await fetchData(`${urlApi}/products`);
    const product = await fetchData(`${urlApi}/products/${products[0].id}`);
    const category = await fetchData(
      `${urlApi}/categories/${product.category.id}`
    );

    console.log(products);
    console.log(product.title);
    console.log(category.name);
  } catch (error) {
    //Atraparemos un error en caso de que haya uno
    console.error(error);
  }
};

anotherFunction(API); //se hace el llamado
```

🖥️ **Salida de src/async/challenge.js** .

- Cuando se ejecuta console.log(products); en fetchData se solicita todos los productos de la API con ${urlApi}/products es por eso que vemos en la salida una larga lista de bloques entre corchetes [] y separados por llaves {}.
- Cuando se ejecuta console.log(product.title); en fetchData se solicita el título de un producto en particular accediendo al atributo title, para ello tenemos que con ${urlApi}/products/${products[0].id} el cero 0 indica la posición de **products** que acabamos de almacenar la lista de productos, pero debe finalizar con id porque esa es la forma para acceder al objeto con ese identificador en la posición cero.
  - Si solo colocamos ${urlApi}/products/${products[0]} sin el .id, en la consola tendríamos un error de tipo: TypeError: Cannot read properties of undefined (reading 'id') así que no podemos acceder.
- Cuando se ejecuta console.log(category.name); en fetchData se solicita el nombre de la categoría que corresponda al producto que se llamó anteriormente, para ello tenemos ${urlApi}/categories/${product.category.id} y no es necesario indicar la posición porque por cada producto, solo hay un bloque de categoría.

## Generadores

Un **generador** en JavaScript consta de una función generadora que muestra un objeto iterable Generator. La palabra reservada yield se usa para pausar y reanudar una función generadora.

- La estructura del Generador consta con la palabra function seguido de un asterísco \* : function\* ésta es una función generadora heredada.
- El resultado que se quiere obtener se coloca al lado derecho de yield, puede ser de cualquier tipo (string, numérico, objetos, etc) y se puede tener tantos yield que se desee.

```javascript
//Declaración de la función del Generador
function* gen() {
  yield 1;
  yield 2;
  yield 3;
}
```

Para poder iterar con el generador, se puede inicializar un valor con la función generadora:

```javascript
//Expresión de la función Generadora
const g = gen();
```

Entre las propiedades del iterador está next():

```javascript
//Llamada del método next en el objeto del Generador
console.log(g.next()); //Imprime el primer yield: {value: 1, done: false}
```

next() permite acceder a la función del generador y obtener con yield dos valores: **value** y el estado de **done**, es decir si tenemos yield 1; y mandamos a imprimir el resultado con next() obtenemos `{value: 1, done: false}':

- El 1 por el valor al lado derecho del primer yield.
- Y done es false porque mientras haya otro yield por operar será falso.
- Será true cuando se ejecute cuatro veces next() y la salida mostrará {value: undefined, done: true}. Ésto se debe a que ya no hay mas nada que mostrar, porque se mandó a imprimir un cuarto elemento y el generador solo tiene 3 yield.

Para obtener solo el valor de value, se escribe next().value de ésta forma:

```javascript
//Llamada del método next en el objeto del Generador
console.log(g.next().value); //Imprime el primer yield: 1
console.log(g.next().value); //Imprime el segundo yield: 2
console.log(g.next().value);
console.log(g.next().value); //Si se coloca un cuarto console, la consola indica "Undefined"
```

✏️ **Ejemplo usando for … of:**

```javascript
//Declaración de la función del Generador pasando un argumento
function* iterate(array) {
  for (let value of array) {
    //El loop del for revisa cada elemento del array
    yield value; //value es asignado en cada ciclo
  }
}

const it = iterate(["Oscar", "Omar", "Ana", "Lucia", "Juan"]);

//la diferencia con el ejemplo anterior es que el iterador se le pasa un argumento
console.log(it.next().value); //Imprime el primer elemento del array: Oscar
console.log(it.next().value); //Imprime el segundo elemento del array: Omar
console.log(it.next().value);
console.log(it.next().value);
console.log(it.next().value); //Si se coloca un sexto console, la consola indica "Undefined"
```
