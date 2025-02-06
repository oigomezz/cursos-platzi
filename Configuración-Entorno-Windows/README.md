# Curso de Configuración de Entorno de Desarrollo en Windows <!-- omit in toc -->

## Tabla de Contenido<!-- omit in toc -->

- [¿Qué es un navegador web?](#qué-es-un-navegador-web)
- [Manejo básico de las DevTools](#manejo-básico-de-las-devtools)
- [IDE (Integrated Development Environment)](#ide)
- [WSL (Windows Subsystem for Linux)](#wsl)
- [Comandos básicos de la terminal](#comandos-básicos-de-la-terminal)

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

## WSL

WSL (Windows Subsystem for Linux) es una característica de Windows 10 y versiones posteriores que permite ejecutar un entorno de línea de comandos de Linux en una máquina Windows. WSL proporciona una capa de compatibilidad que permite ejecutar aplicaciones de Linux en Windows sin la necesidad de utilizar una máquina virtual o instalar un sistema operativo Linux completo.

WSL admite varias distribuciones de Linux, como Ubuntu, Debian, Kali Linux, OpenSUSE, entre otros. Los usuarios pueden instalar estas distribuciones de Linux directamente desde la Microsoft Store y ejecutar aplicaciones de línea de comandos, scripts y herramientas de Linux en un entorno Windows.

Una de las ventajas de WSL es que los usuarios pueden trabajar en un entorno de Linux directamente en Windows sin tener que preocuparse por configurar una máquina virtual o un sistema operativo Linux separado. También permite la integración de herramientas de desarrollo y aplicaciones de línea de comandos de Linux con las aplicaciones y herramientas de Windows.

WSL es una herramienta útil para desarrolladores de software y administradores de sistemas que necesitan trabajar en aplicaciones y herramientas que se ejecutan en ambas plataformas, ya que les permite utilizar un solo sistema operativo con acceso a las funcionalidades de ambas plataformas.

[🡡 volver al inicio](#tabla-de-contenido)

## Comandos básicos de la terminal

Aquí hay una lista de algunos de los comandos principales para Linux:

- ls: lista los archivos y directorios en el directorio actual.
- cd: cambia el directorio actual.
- mkdir: crea un nuevo directorio.
- rm: elimina archivos y directorios.
- cp: copia archivos y directorios.
- mv: mueve o renombra archivos y directorios.
- cat: muestra el contenido de un archivo en la pantalla.
- grep: busca texto en archivos.
- ps: muestra los procesos en ejecución.
- kill: detiene un proceso en ejecución.
- chmod: cambia los permisos de acceso a archivos y directorios.
- sudo: permite al usuario realizar tareas con permisos de superusuario.
- tar: crea y extrae archivos comprimidos.
- ssh: inicia una sesión segura de shell remota en otro sistema.
- ping: comprueba la conectividad de red.

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
