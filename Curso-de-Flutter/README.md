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
