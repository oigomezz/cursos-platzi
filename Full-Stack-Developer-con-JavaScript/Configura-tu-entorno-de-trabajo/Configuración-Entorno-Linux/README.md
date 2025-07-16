# Curso de Configuración de Entorno de Desarrollo en Linux <!-- omit in toc -->

## Tabla de Contenido<!-- omit in toc -->

- [¿Qué es un navegador web?](#qué-es-un-navegador-web)
- [Manejo básico de las DevTools](#manejo-básico-de-las-devtools)
- [IDE (Integrated Development Environment)](#ide)
- [Comandos básicos de la terminal](#comandos-básicos-de-ubuntu-para-principiantes)
- [Git y GitHub](#git-y-github)
  - [Diferencias entre Git y GitHub](#diferencias-entre-git-y-github)
  - [Instalación de Git](#instalación-de-git)

## ¿Qué es un navegador web?

Un navegador web es un programa de software que se utiliza para acceder y navegar por Internet. Los navegadores web permiten a los usuarios buscar, visualizar y acceder a sitios web, páginas web, imágenes, videos y otros contenidos en línea.

Los navegadores web utilizan el protocolo HTTP (Hypertext Transfer Protocol) para obtener información de servidores web y mostrarla al usuario en su dispositivo. Algunos ejemplos de navegadores web populares incluyen Google Chrome, Mozilla Firefox, Safari, Opera, Edge y Internet Explorer. Cada navegador tiene su propia interfaz de usuario y características específicas, pero todos funcionan de manera similar para permitir a los usuarios acceder a contenido en línea y navegar por la web.

Los navegadores funcionan con un protocolo que define como se realiza la transferencia de datos a travel de internet.

- HTTP : Hypertext Transfer Protocol (Protocolo de Transferencia de Hipertexto)
- HTTPS: Hypertext Transfer Protocol Secure (Protocolo de Transferencia de Hipertexto Seguro) En la actualida la manera de escribir, leer e interpretar los datos transferidos a travel de 3 lenguajes que todos los navegadores pueden entender. Estos son:
  - HTML: HyperText Markup Language
  - CSS: Cascade Style Sheet
  - Javascript: Es el lenguaje que le da interaction a las paginas Google Chrome es uno de los navegadores más modernos y más utilizado, el cual tiene 3 versiones:
    - Google Stable: Version que todos usamos
    - Google Dev: Version para desarrolladores que contiene las nuevas funcionalidades y el navegador se actualiza semanalmente
    - Google Canary: Version para desarrolladores que contiene las nuevas funcionalidades y el navegador se actualiza diariamente

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

## Comandos básicos de Ubuntu para principiantes

1. El comando sudo (SuperUser DO) de Linux permite ejecutar programas u otros comandos con privilegios administrativos, al igual que “Ejecutar como administrador” en Windows. Esto es útil cuando, por ejemplo, necesita modificar archivos en un directorio al que su usuario normalmente no tendría acceso.

2. Apt-Get es uno de los comandos de Ubuntu más importantes que todo principiante debe conocer. Se utiliza para instalar, actualizar, y eliminar cualquier paquete. apt-get básicamente funciona en una base de datos de paquetes disponibles. Aquí está la lista de diferentes comandos apt-get:

    - sudo apt-get

      apt-get update con privilegios de superusuario es el primer comando que debe ejecutar en cualquier sistema Linux después de una nueva instalación. Este comando actualiza la base de datos y le permite a su sistema saber si hay paquetes más nuevos disponibles o no.

    - sudo apt-get upgrade

      Después de actualizar la base de datos del paquete, el siguiente paso es actualizar los paquetes instalados. Para actualizar todos los paquetes con actualizaciones disponibles, puede usar este comando. Y si deseas actualizar un paquete en particular, debemos modificar un poco el comando anterior de esta manera:

             sudo apt-get upgrade package-name

    - sudo apt-get install

      Si conoces el nombre del paquete, puede instalar fácilmente un programa con este comando:

             sudo apt-get install package-name

      Remplaza el package-name con el nombre del paquete.

      Si no estás segura sobre el nombre del paquete, puede escribir algunas letras y presionar tabulador y le sugerirá todos los paquetes disponibles con esas letras. Gracias función de autocompletar.🙌

    - sudo apt-get remove

      Cuando se trata de eliminar el programa instalado, el comando apt-get remove se adapta a tus necesidades. Solo tienes que saber el nombre exacto del paquete del software que deseas desinstalar.

      Si no conoces el nombre del paquete, usa el siguiente comando básico de ubuntu para enumerar todos los paquetes instalados en tu sistema y luego copias el nombre del paquete de la lista:

            dpkg --list

      Ahora ejecute el comando apt-get remove como sudo para eliminar el software

            sudo apt-get remove package-name

      El comando apt-get remove solo elimina el software de tu sistema, pero no la configuración o los archivos de datos del paquete. Estos archivos ayudan a mantener la misma configuración cuando deseas reinstalar el mismo software.

    - sudo apt-get purge

      El comando apt-get purge se utiliza cuando deseas eliminar completamente un software de tu sistema con su configuración o archivos de datos para que ya no estén disponibles configuraciones personalizadas durante la reinstalación.

      Ejecuta el comando apt-get purge como sudo para eliminar el software por completo:

            sudo apt-get purge package-name

    - sudo apt-get autoremove

      El comando apt-get autoremove se usa para eliminar cualquier paquete innecesario. Innecesario quiere decir que siempre que instales una aplicación, el sistema también instalará el software del que depende esta aplicación. Es común en Ubuntu que las aplicaciones compartan las mismas bibliotecas. Cuando elimine la aplicación, la dependencia permanecerá en el sistema.

      Por lo tanto, ejecuta apt-get autoremove como sudo después de desinstalar un paquete para eliminar las dependencias de software no deseadas.

      apt-get autoremove eliminará las dependencias que se instalaron con las aplicaciones y que ya no son utilizadas por ninguna otra cosa en el sistema.

3. El comando ls (lista) enumera todos los archivos y carpetas en tu directorio de trabajo actual. También puede especificar rutas a otros directorios si deseas ver su contenido.

4. El comando cd (change director) de Linux también conocido como chdir se usa para cambiar el directorio de trabajo actual. Es uno de los comandos básicos de Ubuntu más utilizados. Usar este comando es fácil, simplemente escribe cd seguido del nombre de la carpeta. Puede usar rutas completas a carpetas o simplemente el nombre de una carpeta dentro del directorio en el que está trabajando actualmente. Algunos usos comunes son:

    - cd /: lo lleva al directorio raíz.
    - cd … - Te lleva un nivel de directorio.
    - cd - - Te lleva al directorio anterior.

5. El comando pwd (print working directory) de Ubuntu muestra la ruta completa del directorio de trabajo actual.

6. El comando cp (copy) de Linux le permite copiar un archivo. Debe especificar tanto el archivo que desea copiar como la ubicación en la que desea copiarlo; por ejemplo, cp xyz / home / myfiles copiaría el archivo “xyz” en el directorio “/ home / myfiles”.

7. El comando mv (mover) te permite mover archivos. También puede cambiar el nombre de los archivos moviéndolos al directorio en el que se encuentran actualmente, pero con un nombre nuevo. El uso es el mismo que en cp; por ejemplo, mv xyz / home / myfiles movería el archivo “xyz” al directorio “/ home / myfiles”.

8. El comando rm (remove) elimina el archivo especificado.

    - rmdir (“remove directory”): elimina un directorio vacío.
    - rm -r (“remove recursuvely”): elimina un directorio junto con su contenido.

9. El comando mkdir (make directory) te permite crear un nuevo directorio. Puedes especificar dónde deseas que se cree el directorio; si no lo haces, se creará en tu directorio de trabajo actual.

10. El comando history muestra todos sus comandos anteriores hasta el límite del historial.

11. El comando du (directory usage)muestra el tamaño de un directorio y todos sus subdirectorios.

12. free: muestra la cantidad de espacio libre disponible en el sistema.

13. uname -a: proporciona una amplia gama de información básica sobre el sistema.

14. top: muestra los procesos que utilizan la mayoría de los recursos del sistema en un momento dado. “Q” se puede utilizar para salir.

15. El comando man muestra una “manual page”. Que suelen ser muy detalladas y se recomienda que leas las páginas del manual de cualquier comando con el que no estés familiarizado. Algunos usos son:

    - man man: proporciona información sobre el manual en sí.
    - man intro: muestra una breve introducción a los comandos de Linux.

16. Info: Similar a man pero a menudo proporciona información más detallada o precisa.

17. -H ó –Help :Este comando es una tercera alternativa para obtener ayuda. Si bien no es tan detallado como info o man pages , esto proporcionará una descripción general rápida del comando y sus usos.
    Por ejemplo: man -h o man -help

18. El comando passwd básico de Ubuntu se usa para cambiar la contraseña de usuario usando Terminal. Lo que tiene que hacer es ejecutar el siguiente comando, donde está el nombre de usuario cuya contraseña debe cambiar:
    passwd

19. El comando whatis muestra una breve descripción de cuál es la funcionalidad del comando específico integrado de Linux. Algunos ejemplos son:

    - whatis cd
    - whatis man
    - whatis help

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
