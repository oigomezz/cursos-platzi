# Curso de Flutter

## Configuración de Flutter y Dart para Desarrollo de Apps Multiplataforma

Crear un entorno de desarrollo en Flutter es fundamental para empezar a construir aplicaciones móviles, web y de escritorio desde un único código base. Este proceso implica instalar herramientas clave como Android Studio y Visual Studio Code, configurar el SDK de Flutter y preparar emuladores para pruebas.

### ¿Qué es Flutter y por qué usarlo?

- Flutter es un framework de Google que permite crear aplicaciones multiplataforma con un único código base.
- Funciona con Dart, un lenguaje de programación diseñado para crear aplicaciones de alta calidad.
- Los widgets son los bloques de construcción esenciales en Flutter, utilizados para diseñar interfaces de usuario.

### ¿Cómo instalar el SDK de Flutter?

1. Descarga del SDK:

   - Ve a la documentación oficial de Flutter y descarga el archivo ZIP.
   - Extrae el contenido en una carpeta llamada dev, dentro del directorio de usuario (por ejemplo, C:\Users\tu_usuario\dev).

2. Configuración de variables de entorno:

   - Busca “Entorno” en el buscador de tu sistema operativo y edita las variables de entorno.
   - En la sección de Path, agrega la ubicación de la carpeta bin dentro del directorio de Flutter.

3. Comandos iniciales:
   - flutter doctor: verifica la instalación y muestra un checklist con los requisitos pendientes.
   - flutter create: permite crear nuevos proyectos.
   - flutter run: despliega las aplicaciones en el emulador o dispositivo.

### ¿Cómo instalar y configurar Android Studio?

1. Descarga e instala Android Studio desde su página oficial.
2. Durante la instalación:
   - Acepta los términos y condiciones.
   - Configura los emuladores seleccionando dispositivos como Pixel 3.
   - Descarga la versión recomendada del sistema operativo Android.
3. Instala el plugin de Flutter desde la sección de Plugins en Android Studio.
4. Crea un nuevo proyecto seleccionando el generador de Flutter y verificando la ruta del SDK.

### ¿Cómo instalar y configurar Visual Studio Code?

1. Descarga e instala Visual Studio Code desde su sitio oficial.
2. Agrega la extensión de Flutter desde el Marketplace de extensiones.
3. Crea un nuevo proyecto:
   - Usa la barra de comandos (Ctrl+Shift+P) y selecciona Flutter: New Project.
   - Define el nombre y ubicación del proyecto.
4. Confirma la confianza en los autores de los archivos del proyecto.

## Despliegue y Estructura Básica de una App con Flutter

Flutter ofrece una estructura robusta y flexible para desarrollar aplicaciones multiplataforma. Aquí exploraremos cómo iniciar tu primera aplicación en Flutter, entender su estructura y personalizarla para obtener resultados profesionales y funcionales.

### ¿Cómo desplegar tu primera aplicación en Flutter?

- Asegúrate de tener Flutter instalado y configurado correctamente en tu máquina.
- Desde Visual Studio Code, utiliza Show Unround Command para escribir y buscar comandos relacionados con Flutter.
- Configura un emulador desde Android Studio, elige uno previamente creado y asegúrate de que tu sistema tiene habilitada la virtualización para ejecutar correctamente los emuladores.
- Usa el comando flutter run o simplemente presiona F5 para ejecutar la aplicación.

### Solución de problemas

Si el emulador no funciona, revisa:

- Permisos de virtualización de tu equipo.
- Configuraciones específicas de Android Studio.

### ¿Cómo está estructurado un proyecto de Flutter?

Flutter divide su proyecto en carpetas y archivos clave que facilitan el desarrollo:

- Carpetas principales:

  - android y ios: Contienen configuraciones específicas para cada plataforma.
  - lib: Aquí se desarrolla el código principal de tu aplicación.
  - test: Diseñada para pruebas unitarias.
  - assets: Almacena imágenes y fuentes personalizadas.

- Archivo main.dart:

  - Es el punto de entrada de la aplicación.
  - Contiene la función runApp que inicializa la aplicación.
  - Incluye configuraciones iniciales como MaterialApp para definir el tema y la estructura básica de la app.

#### ¿Cómo crear un “Hola Mundo” en Flutter?

1. Crea tu widget principal:

   - Usa un StatelessWidget llamado MyApp.
   - Utiliza un Container como base.

2. Añade contenido:

   - Agrega un child dentro del Container con un widget de texto que diga “Hola Mundo”.

3. Configura MaterialApp:
   - Haz un wrap del widget principal con MaterialApp.
   - Define las propiedades title y home para mostrar correctamente tu contenido.

### Hot Reload

Guarda los cambios y usa el hot reload para visualizar instantáneamente los resultados en el emulador.

## Programación en Dart

En Dart, todo es un objeto y todas las clases heredan de la clase Object, lo que simplifica la estructura y potencia la reutilización de código. Aprender cómo manejar variables, constantes, funciones y clases en este lenguaje es fundamental para aprovechar su capacidad en aplicaciones robustas.

### ¿Cómo se definen las variables en Dart?

- Dart permite tipado dinámico con var, aunque también es posible especificar tipos específicos.
- dynamic se utiliza cuando se espera que el tipo de dato cambie en el futuro.

```Dart
var nombre = 'Alison';
String nombreEspecifico = 'Alison';
```

### ¿Qué diferencias existen entre const y final?

- const asigna valores en tiempo de compilación y es inmutable.
- final asigna valores en tiempo de ejecución, útil cuando se desconoce el valor final hasta el momento de la ejecución.

```Dart
final nombre = 'Daniela';
const nickname = 'Dani';
```

### ¿Qué tipos de datos ofrece Dart?

1. Números: Representados por int y double.

   ```Dart
   int x = 10;
   double y = 20.67;
   ```

2. Strings: Permiten cadenas de texto simples y multilínea.

   ```Dart
   String palabra = "texto simple";
   String multilinea = '''texto
   multilínea''';
   ```

3. Booleanos: true o false.

   ```Dart
   bool teGustaDart = true;
   ```

4. Listas: Colección de elementos ordenados.

   ```Dart
   var lista = [1, 2, 3];
   ```

5. Mapas: Estructura clave-valor.

   ```Dart
   var dias = { 'Lu': 'Lunes', 'Ma': 'Martes' };
   ```

### ¿Cómo se definen funciones en Dart?

Las funciones pueden recibir parámetros y devolver datos específicos.

```Dart
void myFunction(param1, param2) {
// lógica de la función
}
```

La función main() es el punto de entrada de una aplicación en Dart.

### ¿Qué estructuras de control existen en Dart?

Dart soporta estructuras de control como:

- if y else
- for y while
- switch y case

Además, permite el uso de break, continue, y assert para control y validación.

### ¿Cómo se manejan las excepciones?

Dart permite manejar errores con throw para lanzar excepciones y try-catch para capturarlas:

```Dart
try {
// código que puede fallar
} catch (e) {
// manejar error
}
```

### ¿Cómo se crean clases y constructores?

Las clases en Dart se definen con class, y pueden tener constructores para inicializar variables.

```Dart
class Point {
   num x, y;
   Point(this.x, this.y);
}
```

### ¿Qué es la herencia en Dart?

Dart permite que una clase herede de otra usando extends.

```Dart
class Television {
   void turnOn() {...}
}

class SmartTelevision extends Television {
void turnOn() {
   super.turnOn();
   // lógica adicional
   }
}
```

### ¿Cómo se realiza la sobrescritura de métodos?

Dart permite la sobrescritura de métodos heredados usando @override.

```Dart
class SmartTelevision extends Television {
   @override
   void turnOn() {
      // nueva implementación
   }
}
```

### ¿Qué es un enum en Dart?

enum define un conjunto de constantes con nombre.

```Dart
enum Color { red, green, blue }
```

## Creación de Widgets Stateless en Flutter para Recetario Interactivo

Aprenderás cómo estructurar y personalizar una aplicación Flutter enfocada en un recetario utilizando StatelessWidget. Exploraremos el uso de propiedades como AppBar, personalización con estilos y colores, y buenas prácticas de desarrollo.

### ¿Cómo crear y estructurar un StatelessWidget?

1. Definición de la clase: Crea una nueva clase que extienda de StatelessWidget. Por ejemplo:

   ```Dart
   class RecipeBook extends StatelessWidget {
     @override
     Widget build(BuildContext context) {
       return Scaffold();
     }
   }
   ```

   - Scaffold actúa como una hoja en blanco donde añadimos elementos.

2. Personalización inicial: Añade propiedades clave como:

   - AppBar: para mostrar un título y definir colores.
   - Body: el espacio principal donde se mostrará el contenido.

### ¿Cómo personalizar la barra superior con AppBar?

La barra superior se personaliza utilizando la propiedad AppBar. Ejemplo:

```Dart
return Scaffold(
  appBar: AppBar(
    title: Text(
      'Mi Recetario',
      style: TextStyle(color: Colors.white),
    ),
    backgroundColor: Colors.orange,
  ),
);
```

- La propiedad title define el texto visible.
- TextStyle permite modificar el color, tamaño y estilo del texto.
- backgroundColor define el color de fondo del AppBar.

### ¿Cómo eliminar marcas de depuración y warnings?

- Eliminar la marca de depuración: Ajusta la propiedad debugShowCheckedModeBanner a false en MaterialApp.

  ```Dart
  return MaterialApp(
    debugShowCheckedModeBanner: false,
    home: RecipeBook(),
  );
  ```

- Ocultar warnings temporales: Si no afectan el desarrollo actual, coméntalos en el archivo analysis_options.yaml con #.

### ¿Qué buenas prácticas seguir al construir widgets?

- Define widgets constantes si sus datos no cambiarán:

  ```Dart
  const Text('Constante');
  ```

- Usa la estructura jerárquica de widgets para mantener el código organizado.
- Personaliza propiedades como colores y estilos para mejorar la experiencia visual.

### ¿Cómo probar la implementación en el emulador?

- Guarda los cambios en el archivo main.dart.
- Observa en el emulador cómo se reflejan las personalizaciones.
- Ajusta y mejora según el comportamiento observado.

## Widgets Esenciales en Flutter: Container, Row, Column y Text

Crear aplicaciones con Flutter permite desarrollar interfaces altamente personalizadas, y para ello es fundamental comprender widgets clave como Container, Row, Column y Text. En este artículo, exploraremos cómo utilizarlos para estructurar y personalizar el cuerpo de tu aplicación.

### ¿Cómo estructurar el cuerpo de tu aplicación en Flutter?

- Antes de agregar widgets, es esencial formatear el código para visualizar la jerarquía correctamente. Usa un formatter, selecciona Dart y observa la disposición en cascada de los widgets.
- Inicia con un widget Container. Es una caja flexible que puede contener otros widgets, personalizable con propiedades como:
  - Padding y margin: Para espaciar elementos.
  - Border y color: Para estilos visuales.
  - Box model: Define el diseño y estructura.

### ¿Cómo crear tarjetas con información?

1. Usa Container para estructurar las tarjetas:

   - Divide las tarjetas en dos secciones: una para la imagen y otra para el texto.
   - Agrega un widget Row para alinear los elementos horizontalmente.

2. Configura la imagen:

   - Crea un Container con propiedades de tamaño (height y width).
   - Aplica el widget ClipRRect para bordes redondeados con la propiedad borderRadius.

3. Organiza el contenido textual:

   - Utiliza un widget Column para colocar elementos en una disposición vertical.
   - Añade texto con Text, como el nombre de la receta y el autor.
   - Usa un Container con un color (ej. naranja) para añadir una línea separadora decorativa.

### ¿Cómo agregar espaciado y adaptabilidad?

- **Espaciado:** Incorpora SizedBox para separar elementos horizontal o verticalmente según el contexto (width o height).
- **Adaptabilidad:** Implementa MediaQuery para ajustar el tamaño de los widgets según la pantalla del dispositivo, especialmente útil para diseños responsive.

### ¿Qué prácticas facilitan el desarrollo en Flutter?

- Formatea el código constantemente para mantener la jerarquía clara.
- Experimenta con diferentes widgets como Row, Column y Text para dominar su comportamiento.
- Utiliza propiedades como MediaQuery para diseños flexibles y adaptables.

## Estructuración y Navegación de Pantallas en Flutter

Aquí aprenderás a estructurar y gestionar pantallas en tu aplicación, integrándolas de manera organizada y funcional en tu proyecto Flutter. Descubre cómo configurar un sistema de navegación con pestañas para mejorar la experiencia del usuario.

### ¿Cómo estructurar las pantallas de tu aplicación?

- **Crea una carpeta específica:** Dentro de tu proyecto, organiza tus pantallas en una nueva carpeta llamada screens.
- **Configura una pantalla inicial:** Crea un archivo como home_screen.dart para tu pantalla principal.
- **Usa la convención UpperCamelCase:** Al nombrar clases como HomeScreen, asegúrate de respetar esta convención para mantener la legibilidad.

### ¿Cómo mover componentes del main a la pantalla principal?

- **Identifica los componentes existentes:** Ubica elementos como contenedores en el archivo principal main.dart.
- **Reubica los widgets al nuevo archivo:** Transfiere estos componentes al archivo de la pantalla principal (home_screen.dart), utilizando el widget Scaffold para estructurarlos.
- **Reemplaza el child por body:** En el Scaffold, usa body en lugar de child para mayor claridad y funcionalidad.

### ¿Cómo implementar una barra de navegación con pestañas?

- **Agrega un AppBar con TabBar:** Incluye una barra de navegación inferior (TabBar) dentro de tu AppBar.
- **Configura pestañas iniciales:**
  - Usa widgets de Icon para representar visualmente las pestañas.
  - Agrega texto descriptivo con el widget Text.
- **Utiliza un TabBarView:** Define un TabBarView para que las pestañas muestren diferentes pantallas.

### ¿Cómo solucionar errores al configurar el TabBar?

- **Envuelve el Scaffold con un controlador:** Usa el widget DefaultTabController para manejar las pestañas.
- **Configura propiedades adicionales:**
  - Ajusta el indicador de la pestaña activa con un color distintivo.
  - Personaliza el texto con colores para estados seleccionados y no seleccionados.
- **Gestiona errores en el emulador:** Si surgen problemas al guardar, refresca el proyecto desde la línea final para aplicar cambios correctamente.

### ¿Qué más puedes personalizar en tu TabBar?

- **Añade más pestañas:** Amplía tu navegación agregando más pantallas al listado de pestañas.
- **Optimiza el diseño:**
  - Define un máximo de pestañas visibles.
  - Configura colores consistentes con el tema de tu aplicación.

## Creación y Personalización de Widgets en Flutter

Nuestra aplicación se encuentra en una etapa emocionante, donde comenzamos a personalizar y estilizar elementos clave como nuestras tarjetas. En este artículo exploraremos cómo reutilizar widgets, agregar estilos y mejorar la disposición de los elementos para lograr un diseño eficiente y visualmente atractivo.

### ¿Cómo reutilizar widgets en nuestra aplicación?

- Crea un widget personalizado para las tarjetas, nombrándolo, por ejemplo, ReceipesCart. Este widget debe incluir un BuildContext para heredar las propiedades de la aplicación principal.
- Incluye la estructura de la tarjeta (como un Container) dentro del widget, asegurándote de usar un return para devolverlo.
- Una vez definido, puedes usar este widget en cualquier parte de tu pantalla, como en el HomeScreen, y reutilizarlo tantas veces como sea necesario.

### ¿Qué ajustes de espaciado y padding se pueden hacer?

- Utiliza Padding para ajustar el espaciado alrededor de las tarjetas. Esto puede configurarse con valores predeterminados o personalizados usando propiedades como left, top, right y bottom.
- Si los elementos dentro de las tarjetas están demasiado juntos, usa widgets como SizedBox para crear separación adicional, por ejemplo:
  - Cuatro píxeles entre el título y el autor.
  - Cuatro píxeles entre el nombre y otros elementos.

### ¿Cómo alinear y centrar elementos en una tarjeta?

- Para alinear verticalmente, usa MainAxisAlignment con valores como center dentro de un widget Column.
- Para alinear horizontalmente, emplea CrossAxisAlignment configurado como start para que los elementos queden al inicio.
- Estos ajustes aseguran que los componentes de la tarjeta se vean organizados y equilibrados.

### ¿Qué estilos se pueden agregar al texto?

- Usa la propiedad style en widgets de texto para definir:
  - Tamaño de fuente (fontSize), por ejemplo, 16 puntos.
  - Tipografía personalizada, como Quicksand, importándola desde Google Fonts.
- Aplica estos estilos de manera consistente en todos los textos de la tarjeta, como en el título y el autor.

### ¿Cómo mejorar la apariencia de las tarjetas con contenedores?

- Añade un BoxDecoration a los Container para personalizar su aspecto:
  - Usa colores temporales como naranja para previsualizar el diseño.
  - Añade bordes redondeados con la propiedad BorderRadius, ajustando su tamaño según sea necesario.
- Estas propiedades no solo mejoran el diseño, sino que también permiten visualizar dónde irán las imágenes y otros elementos.

## Configuración de Imágenes en Flutter: Uso de Carpeta Assets

Flutter te permite personalizar tu aplicación incluyendo imágenes de manera sencilla, ya sea desde tu proyecto o mediante URLs externas. Aquí te mostramos cómo configurar y optimizar tu recetario con imágenes.

### ¿Cómo configurar la carpeta de imágenes en Flutter?

- Accede al archivo pubspec.yaml de tu proyecto.
- Desplázate hacia el final del archivo hasta la sección de assets.
- Comenta las indicaciones predeterminadas y agrega una nueva ruta:

  ```Json
   assets:
      - assets/imagenes/
  ```

- Crea una carpeta llamada assets en la raíz de tu proyecto y, dentro de ella, otra llamada imagenes.
- Guarda tus imágenes dentro de esta carpeta. Ahora puedes acceder a estas imágenes desde cualquier widget de tu proyecto.

### ¿Cómo agregar imágenes al recetario?

- Modifica el widget Container de tu recetario.
- Cambia la propiedad child para incluir un widget Image.
- Si usas imágenes desde URLs, utiliza Image.network. Por ejemplo:

```Dart
child: Image.network(
  'https://link-a-tu-imagen.com/lasagna.jpg',
  fit: BoxFit.cover,
),
```

- Guarda el archivo y verifica que las imágenes se visualicen correctamente.

### ¿Cómo ajustar las imágenes al contenedor?

- Usa la propiedad fit con el widget BoxFit para definir cómo la imagen se adapta al contenedor.
  - Ejemplo: BoxFit.cover hará que la imagen rellene completamente el contenedor ajustándose con un ligero zoom.
- Otras opciones útiles incluyen:
  - BoxFit.contain para mantener las proporciones sin recortar.
  - BoxFit.fill para estirar la imagen y cubrir el espacio.

## Creación de Formularios y Botones Interactivos en Aplicaciones

Crear interfaces intuitivas y atractivas es esencial para mejorar la experiencia del usuario en una aplicación. En este artículo, exploraremos cómo implementar botones interactivos y formularios personalizables, desde la conceptualización hasta la personalización avanzada, utilizando widgets en Flutter.

### ¿Cómo implementar un botón con acción personalizada?

- **Usa un Floating Action Button:** Este widget se utiliza para acciones principales. Puedes asignarle un onPressed que ejecutará una función cuando se presione.
- **Personalización del botón:**

  - **Color:** Define colores que resalten, como un naranja de tu paleta.
  - **Íconos:** Agrega íconos clicables y coloréales, por ejemplo, en blanco, para diferenciarlos del fondo.

  ```Dart
  FloatingActionButton(
    onPressed: () {
      // Lógica a ejecutar
    },
    backgroundColor: Colors.orange,
    child: Icon(Icons.add, color: Colors.white),
  ),
  ```

### ¿Cómo mostrar un formulario en un modal?

- **ShowModalBottomSheet:**Permite mostrar un contenedor flotante desde la parte inferior de la pantalla.
- **Configuración inicial:**

  - **Altura dinámica:** Usa MediaQuery.of(context).size para adaptar el tamaño al ancho de la pantalla.
  - **Decoración:** Aplica colores, contenedores y texto para estructurar el contenido.

  ```Dart
  void showModal(BuildContext context) {
    showModalBottomSheet(
      context: context,
      builder: (BuildContext context) {
        return Container(
          height: MediaQuery.of(context).size.height * 0.5,
          color: Colors.white,
          child: Center(child: Text('Hola, aquí va tu formulario')),
        );
      },
    );
  }
  ```

### ¿Cómo estructurar un formulario con campos reutilizables?

- **Crea una clase de formulario:** Utiliza un StatelessWidget para estructurar tu formulario.
- **Formulario dinámico:**

  - Usa Form con una clave (formKey) para manejar validaciones y control de campos.
  - Estructura los campos en columnas para una alineación vertical.

  ```Dart
  class RecipeForm extends StatelessWidget {
    final _formKey = GlobalKey();

    @override
    Widget build(BuildContext context) {
      return Padding(
        padding: EdgeInsets.all(8.0),
        child: Form(
          key: _formKey,
          child: Column(
            crossAxisAlignment: CrossAxisAlignment.start,
            children: [
              Text('Nueva Receta', style: TextStyle(fontSize: 24, color: Colors.orange)),
              SizedBox(height: 16),
              buildTextField('Nombre de la receta'),
            ],
          ),
        ),
      );
    }

    Widget buildTextField(String label) {
      return TextFormField(
        decoration: InputDecoration(
          labelText: label,
          labelStyle: TextStyle(color: Colors.orange),
          enabledBorder: OutlineInputBorder(
            borderRadius: BorderRadius.circular(10),
            borderSide: BorderSide(color: Colors.orange, width: 1),
          ),
          focusedBorder: OutlineInputBorder(
            borderRadius: BorderRadius.circular(10),
            borderSide: BorderSide(color: Colors.orange, width: 1.5),
          ),
        ),
      );
    }
  }
  ```

### ¿Cómo personalizar widgets para reutilización?

- **Define widgets específicos:** Crea widgets para campos de texto que incluyan estilos y validaciones comunes.
- **Propiedades importantes:**
  - **label:** Texto para identificar el campo.
  - **InputDecoration:** Define bordes, colores y estilos.
  - **BorderRadius:** Redondea los bordes para un diseño más moderno.

### Widget de campo reutilizable

```Dart
Widget buildCustomTextField(String label, String fontFamily) {
  return TextFormField(
    decoration: InputDecoration(
      labelText: label,
      labelStyle: TextStyle(fontFamily: fontFamily, color: Colors.orange),
      enabledBorder: OutlineInputBorder(
        borderRadius: BorderRadius.circular(10),
        borderSide: BorderSide(color: Colors.orange, width: 1),
      ),
      focusedBorder: OutlineInputBorder(
        borderRadius: BorderRadius.circular(10),
        borderSide: BorderSide(color: Colors.orange, width: 1.5),
      ),
    ),
  );
}
```

### Agrega campos al formulario

```Dart
Column(
  children: [
    buildCustomTextField('Nombre del autor', 'QuickSand'),
    SizedBox(height: 16),
    buildCustomTextField('Ingredientes', 'QuickSand'),
    SizedBox(height: 16),
    buildCustomTextField('Imagen URL', 'QuickSand'),
  ],
)
```
