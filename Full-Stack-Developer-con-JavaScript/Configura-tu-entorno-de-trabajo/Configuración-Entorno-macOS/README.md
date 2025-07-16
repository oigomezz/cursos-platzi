# Curso de Configuración de Entorno de Desarrollo en Windows <!-- omit in toc -->

## Tabla de Contenido<!-- omit in toc -->

- [¿Qué es un navegador web?](#qué-es-un-navegador-web)
- [Manejo básico de las DevTools](#manejo-básico-de-las-devtools)
- [IDE (Integrated Development Environment)](#ide)
- [Comandos básicos de la terminal](#comandos-básicos-de-la-terminal)
- [Git y GitHub](#git-y-github)
  - [Diferencias entre Git y GitHub](#diferencias-entre-git-y-github)
  - [Instalación de Git](#instalación-de-git)

## ¿Qué es un navegador web?

Un navegador web es un programa de software que se utiliza para acceder y navegar por Internet. Los navegadores web permiten a los usuarios buscar, visualizar y acceder a sitios web, páginas web, imágenes, videos y otros contenidos en línea.

Los navegadores web utilizan el protocolo HTTP (Hypertext Transfer Protocol) para obtener información de servidores web y mostrarla al usuario en su dispositivo. Algunos ejemplos de navegadores web populares incluyen Google Chrome, Mozilla Firefox, Safari, Opera, Edge y Internet Explorer. Cada navegador tiene su propia interfaz de usuario y características específicas, pero todos funcionan de manera similar para permitir a los usuarios acceder a contenido en línea y navegar por la web.

[🡡 volver al inicio](#tabla-de-contenido)

## Manejo básico de las DevTools

Las DevTools de Google Chrome son una herramienta poderosa y útil para desarrolladores web. Estas herramientas permiten a los desarrolladores depurar, inspeccionar y optimizar el rendimiento de las aplicaciones web. Aquí hay un breve resumen del manejo básico de las DevTools:

Acceder a las DevTools: Puedes abrir las DevTools haciendo clic derecho en cualquier página web y seleccionando "Inspeccionar elemento" o presionando Ctrl + Shift + I en Windows o Cmd + Option + I en Mac. También puedes acceder a las DevTools desde el menú principal de Chrome haciendo clic en "Más herramientas" y seleccionando "Herramientas de desarrollo".

Inspeccionar elementos: Las DevTools te permiten inspeccionar cualquier elemento de la página, incluyendo HTML, CSS y JavaScript. Simplemente haz clic en el elemento que deseas inspeccionar y las DevTools te mostrarán la información relevante.

Modificar el código en tiempo real: Puedes editar el código HTML, CSS o JavaScript en tiempo real directamente desde las DevTools. Esto te permite experimentar con diferentes cambios y ver cómo afectan el aspecto o la funcionalidad de la página.

Depurar errores: Las DevTools te permiten depurar errores de JavaScript en tiempo real, lo que significa que puedes ver exactamente dónde se encuentra el problema y corregirlo de manera rápida y eficiente.

Optimizar el rendimiento: Las DevTools ofrecen herramientas para analizar el rendimiento de la página, incluyendo la velocidad de carga y el uso de recursos. Puedes utilizar esta información para identificar problemas y optimizar el rendimiento de la página.

En conclusión, las DevTools son una herramienta esencial para cualquier desarrollador web. Al permitirte inspeccionar, editar y depurar el código de la página en tiempo real, las DevTools te ayudan a mejorar la funcionalidad, el aspecto y el rendimiento de tu sitio web.

[🡡 volver al inicio](#tabla-de-contenido)

## IDE

Un IDE (Integrated Development Environment) representa un entorno de desarrollo integrado, un ambiente en donde puedes programar. Este IDE trae consigo herramientas que ayudan al desarrollador, como: debugger (depurador), consola, GIT, inteligencia (la cual te ayuda a corregir la sintaxis cuando estás escribiendo código), etc. Lo que hace ser código al código es la sintaxis y el formato del archivo (.js , .css) etc.

Existen diferentes tipos de IDE, como por ejemplo:

- Visual Studio Code: “Edición de código redefinida”, es totalmente gratuito, está construido encima de open source, es decir que es de código libre y se ejecuta o corre en cualquier sistema operativo. Es muy versátil y puede servir con muchos lenguajes de programación.
- WebStorm: Se venden a sí mismos como “El IDE más inteligente para JavaScript”.
- Eclipse: es un IDE para el desarrollo de Java, sin embargo, admite varios lenguajes como C / C ++, PHP, ColdFusion, Python, Scala y la plataforma Android. Fue desarrollado en Java y sigue el modelo de código abierto.
- Atom: se venden a sí mismos como “El editor de texto hackeable”, es decir que nos dejan construir herramientas, modificarlo, hacerle variaciones a su código para adaptarse a lo que necesitamos.
- Editor de texto: Existen editores de texto / editores de código, las cuales son herramientas más minimalistas donde puedes programar pero con ciertos límites. Como el Bloc de Notas.

[🡡 volver al inicio](#tabla-de-contenido)

## Comandos básicos de la terminal

### Comandos para mostrar archivos o carpetas

Te permiten ver todos los archivos y carpetas existentes en tu computadora.

| Comando | Descripción                                                             |
| ------- | ----------------------------------------------------------------------- |
| pwd     | Imprime la ruta en la que te encuentras                                 |
| cd      | [carpeta] Te lleva la carpeta que le indiques                           |
| cd …    | Te lleva a la carpeta anterior de la que estás                          |
| ls      | Lista los archivos y carpetas                                           |
| ls -a   | Lista los archivos incluyendo los ocultos                               |
| ls -S   | Lista los archivos por tamaño, de mayor a menor                         |
| ls -lh  | Lista los archivos y carpetas con info detallada y legible para humanos |
| code .  | Abre la carpeta donde te encuentras en VSCode                           |

### Comandos para manipular archivos/carpetas

¿Quieres crear carpetas, moverlas de lugar o incluso comprimir archivos desde la misma terminal?

| Comando                             | Descripción                                             |
| ----------------------------------- | ------------------------------------------------------- |
| mkdir [carpeta]                     | Crea una carpeta con el nombre que le des               |
| touch [carpeta]                     | Crea un archivo con el nombre y la extensión que le des |
| file [carpeta]                      | Muestra las características de un archivo               |
| cp [archivo] [destino]              | Copia un archivo hacia un nuevo destino                 |
| cp -r [carpeta] [destino]           | Copia una carpeta hacia un nuevo destino                |
| mv [archivo/carpeta] [destino]      | Mueve una carpeta o archivo hacia un nuevo destino      |
| rm [archivo]                        | Elimina un archivo                                      |
| rm -r [carpeta]                     | Elimina una carpeta y su contenido                      |
| rm -ri [carpeta]                    | Elimina una carpeta y su contenido de forma interactiva |
| tar -czvf [nombre].tar.gz [carpeta] | Comprime una carpeta                                    |
| tar -xzvf [nombre].tar.gz           | Descomprime la carpeta                                  |

### Comandos para archivos de texto plano

Desde la misma terminal puedes ver las líneas que tienen los archivos de texto plano.

| Comando              | Descripción                                                              |
| -------------------- | ------------------------------------------------------------------------ |
| head [archivo]       | Muestra las primeras 10 líneas de un archivo de texto                    |
| head -n 20 [archivo] | Muestra las primeras 20 líneas                                           |
| tail [archivo]       | Muestra las últimas 10 líneas                                            |
| tail -n 20 [archivo] | Muestra las últimas 20 líneas                                            |
| less [archivo]       | Explora el contenido del archivo (y para salirte de este modo usas la Q) |
| code [archivo]       | Abre un archivo de texto en VSCode                                       |
| wc [file]            | Te muestra cuántas líneas, palabras y bits tiene un archivo              |

### Comandos para buscar archivos/carpetas

¿Se te perdió el archivo CodigoEmpresaFinalFinalEsteSiEs.js y no sabes cómo encontrarlo? ¿O quieres que la terminal te muestre una lista específica de archivos?

| Comando                        | Descripción                                             |
| ------------------------------ | ------------------------------------------------------- |
| find [carpeta] -name [archivo] | Busca un archivo/carpeta en una ruta específica         |
| find ./ -name [archivo]        | Busca un archivo/carpeta en la ruta donde te encuentras |
| ls \*[.txt]                    | Lista los archivos que terminen con esa extensión       |
| ls [palabra]\*                 | Lista los archivos que empiecen con esa palabra         |
| grep -i [palabra] [file]       | Busca en ese archivo la palabra que le especifiques     |

### Comandos para red e internet

| Comando           | Descripción                                               |
| ----------------- | --------------------------------------------------------- |
| ifconfig          | Muestra la información de tu red                          |
| ping [ip_dominio] | Consulta la disponibilidad de esa IP en tu red o internet |
| wget [id_dominio] | Descarga el archivo o recurso de esa IP o dominio         |
| netstat -i        | Muestra las interfaces de red y su estado                 |

### Explorador de comandos

| Comando          | Descripción                                  |
| ---------------- | -------------------------------------------- |
| man [comando]    | Muestra el manual del comando                |
| help [comando]   | Muestra ayuda para el comando (solo en Bash) |
| whatis [comando] | Muestra un resumen de la función del comando |
| sudo [comando]   | Ejecuta un comando como superusuario         |

[🡡 volver al inicio](#tabla-de-contenido)

## Git y GitHub

Git es el sistema de control de versiones, el cual nos permite llevar un control exacto de todos los cambios a lo largo del tiempo de los proyectos, guarda un copia completa del proyecto y guarda los cambios que se hagan.

GitHub es una plataforma en la cual se puede subir los repositorios de Git a la nube, para así poder tener un respaldo y poder compartirlo con la comunidad, además de poder trabajar en proyectos con distintos colaboradores a la vez.

### Diferencias entre Git y GitHub

- Git es el gestor de versiones que se utiliza con más frecuencia en la industria.
- Git no es necesariamente GitHub, GitHub es una plataforma en donde todos los equipos van subiendo su código, colaboran entre ellos, etc.
- Existen más plataformas para utilizar Git como GitLab, GitHub, Bitbucket.

### Instalación de Git

Realizar el update cada vez que se instale algo nuevo:

    sudo apt update

Para instalar Git:

    sudo apt-get install git-all

Verificar versiones de Git:

    git version

[🡡 volver al inicio](#tabla-de-contenido)
