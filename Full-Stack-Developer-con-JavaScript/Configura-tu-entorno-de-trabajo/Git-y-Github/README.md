# Curso de Git y GitHub <!-- omit in toc -->

## Tabla de Contenido<!-- omit in toc -->

- [¿Qué son Git y GitHub?](#qué-son-git-y-github)
  - [¿Qué es Git y por qué debería importarte?](#qué-es-git-y-por-qué-debería-importarte)
  - [¿Quién creó Git y por qué es tan relevante?](#quién-creó-git-y-por-qué-es-tan-relevante)
  - [¿Cómo te beneficia aprender Git desde el inicio?](#cómo-te-beneficia-aprender-git-desde-el-inicio)
  - [¿Cómo funciona Git en tu entorno de trabajo?](#cómo-funciona-git-en-tu-entorno-de-trabajo)
- [Configuración Inicial de Git: init y config](#configuración-inicial-de-git-init-y-config)
  - [¿Cómo confirmar que Git está instalado en tu sistema?](#cómo-confirmar-que-git-está-instalado-en-tu-sistema)
  - [¿Cómo crear y preparar el primer proyecto con Git?](#cómo-crear-y-preparar-el-primer-proyecto-con-git)
  - [¿Cómo inicializar un repositorio en Git?](#cómo-inicializar-un-repositorio-en-git)
  - [¿Cómo personalizar tu configuración de usuario en Git?](#cómo-personalizar-tu-configuración-de-usuario-en-git)
  - [¿Cómo confirmar la configuración de Git?](#cómo-confirmar-la-configuración-de-git)
  - [¿Qué hacer si olvidas un comando?](#qué-hacer-si-olvidas-un-comando)
- [Comandos Básicos de Git: add, commit y log](#comandos-básicos-de-git-add-commit-y-log)
  - [¿Cómo inicia el control de versiones con Git?](#cómo-inicia-el-control-de-versiones-con-git)
  - [¿Cómo se crean y agregan archivos a Git?](#cómo-se-crean-y-agregan-archivos-a-git)
  - [¿Qué es el área de staging y cómo funciona?](#qué-es-el-área-de-staging-y-cómo-funciona)
  - [¿Cómo realizar el commit de los archivos en Git?](#cómo-realizar-el-commit-de-los-archivos-en-git)
  - [¿Cómo gestionar múltiples archivos en Git?](#cómo-gestionar-múltiples-archivos-en-git)
  - [¿Cómo visualizar el historial de cambios en Git?](#cómo-visualizar-el-historial-de-cambios-en-git)
  - [¿Qué sucede al modificar un archivo en Git?](#qué-sucede-al-modificar-un-archivo-en-git)
  - [¿Cómo maneja Git diferentes tipos de archivos?](#cómo-maneja-git-diferentes-tipos-de-archivos)
- [Ramas y Fusión de Cambios: branch, merge, switch y checkout](#ramas-y-fusión-de-cambios-branch-merge-switch-y-checkout)
  - [¿Por qué son útiles las ramas en Git?](#por-qué-son-útiles-las-ramas-en-git)
  - [¿Cómo verificar la rama actual?](#cómo-verificar-la-rama-actual)
  - [¿Cómo crear una nueva rama en Git?](#cómo-crear-una-nueva-rama-en-git)
  - [¿Cómo agregar y confirmar cambios en una rama?](#cómo-agregar-y-confirmar-cambios-en-una-rama)
  - [¿Cómo fusionar cambios de una rama secundaria a la principal?](#cómo-fusionar-cambios-de-una-rama-secundaria-a-la-principal)
  - [¿Por qué es importante eliminar ramas que ya no se usan?](#por-qué-es-importante-eliminar-ramas-que-ya-no-se-usan)
- [Volviendo en el Tiempo en Git: reset y revert](#volviendo-en-el-tiempo-en-git-reset-y-revert)
  - [¿Cuál es la diferencia entre Git Reset y Git Revert?](#cuál-es-la-diferencia-entre-git-reset-y-git-revert)
  - [¿Cómo se utiliza Git Reset?](#cómo-se-utiliza-git-reset)
  - [¿Cómo funciona Git Revert?](#cómo-funciona-git-revert)
  - [¿Cuándo es recomendable utilizar Git Reset o Git Revert?](#cuándo-es-recomendable-utilizar-git-reset-o-git-revert)
  - [¿Cómo aseguras una correcta comunicación en el uso de estos comandos?](#cómo-aseguras-una-correcta-comunicación-en-el-uso-de-estos-comandos)
- [Gestión de versiones: tag y checkout](#gestión-de-versiones-tag-y-checkout)
  - [¿Cómo se utiliza git tag para organizar versiones?](#cómo-se-utiliza-git-tag-para-organizar-versiones)
  - [¿Qué permite git checkout al explorar el historial?](#qué-permite-git-checkout-al-explorar-el-historial)
  - [¿Cómo integran git tag y git checkout una experiencia de desarrollo ordenada?](#cómo-integran-git-tag-y-git-checkout-una-experiencia-de-desarrollo-ordenada)
- [Cómo Resolver Conflictos de Ramas en Git](#cómo-resolver-conflictos-de-ramas-en-git)
  - [¿Qué es un conflicto de ramas en Git?](#qué-es-un-conflicto-de-ramas-en-git)
  - [¿Cómo crear un conflicto de ramas para aprender a resolverlo?](#cómo-crear-un-conflicto-de-ramas-para-aprender-a-resolverlo)
  - [¿Cómo resolver un conflicto de ramas en Git?](#cómo-resolver-un-conflicto-de-ramas-en-git)
  - [¿Qué hacer después de resolver un conflicto?](#qué-hacer-después-de-resolver-un-conflicto)
- [Por qué GitHub es clave para los Desarrolladores](#por-qué-github-es-clave-para-los-desarrolladores)
  - [¿Qué opciones existen para hospedar proyectos en Git?](#qué-opciones-existen-para-hospedar-proyectos-en-git)
  - [¿Cómo ha evolucionado GitHub desde su lanzamiento?](#cómo-ha-evolucionado-github-desde-su-lanzamiento)
  - [¿Qué funcionalidades destacan en GitHub actualmente?](#qué-funcionalidades-destacan-en-github-actualmente)
  - [¿Qué oportunidades brinda GitHub para los desarrolladores?](#qué-oportunidades-brinda-github-para-los-desarrolladores)
  - [¿Cómo puede ayudarte GitHub en el desarrollo profesional?](#cómo-puede-ayudarte-github-en-el-desarrollo-profesional)
- [¿Cómo integrar Git y GitHub en un flujo de trabajo profesional?](#cómo-integrar-git-y-github-en-un-flujo-de-trabajo-profesional)
  - [¿Cuál es la relación entre Git y GitHub?](#cuál-es-la-relación-entre-git-y-github)
  - [¿Cómo se inicia el flujo de trabajo en GitHub?](#cómo-se-inicia-el-flujo-de-trabajo-en-github)
  - [¿Por qué es importante trabajar en ramas?](#por-qué-es-importante-trabajar-en-ramas)
  - [¿Qué reglas se pueden seguir para crear tareas?](#qué-reglas-se-pueden-seguir-para-crear-tareas)
- [Gestión de Repositorios en GitHub](#gestión-de-repositorios-en-github)
  - [¿Cómo crear un repositorio en GitHub?](#cómo-crear-un-repositorio-en-github)
  - [¿Cómo agregar un colaborador a un repositorio en GitHub?](#cómo-agregar-un-colaborador-a-un-repositorio-en-github)
  - [¿Cómo clonar un repositorio en tu máquina local?](#cómo-clonar-un-repositorio-en-tu-máquina-local)
  - [¿Cómo integrar Git y GitHub para un flujo de trabajo colaborativo?](#cómo-integrar-git-y-github-para-un-flujo-de-trabajo-colaborativo)
- [Cómo configurar SSH para GitHub](#cómo-configurar-ssh-para-github)
  - [¿Por qué es mejor usar SSH en lugar de HTTPS para GitHub?](#por-qué-es-mejor-usar-ssh-en-lugar-de-https-para-github)
  - [¿Cómo generar una llave SSH en Windows y Linux?](#cómo-generar-una-llave-ssh-en-windows-y-linux)
  - [¿Cómo añadir la llave SSH a GitHub?](#cómo-añadir-la-llave-ssh-a-github)
  - [¿Qué pasos adicionales seguir en Mac?](#qué-pasos-adicionales-seguir-en-mac)
  - [¿Cómo verificar la conexión con GitHub?](#cómo-verificar-la-conexión-con-github)
  - [¿Cómo clonar un repositorio usando SSH?](#cómo-clonar-un-repositorio-usando-ssh)
- [Clone, fork y estrellas a repositorios](#clone-fork-y-estrellas-a-repositorios)
  - [¿Qué es un fork y cómo se utiliza?](#qué-es-un-fork-y-cómo-se-utiliza)
  - [¿Qué beneficios aporta usar estrellas en GitHub?](#qué-beneficios-aporta-usar-estrellas-en-github)
  - [¿Cómo clonar un repositorio forkeado?](#cómo-clonar-un-repositorio-forkeado)
  - [¿Por qué usar forks en lugar de clonar directamente el repositorio original?](#por-qué-usar-forks-en-lugar-de-clonar-directamente-el-repositorio-original)
- [Trabajo con repositorios remotos: push, pull y fetch](#trabajo-con-repositorios-remotos-push-pull-y-fetch)
  - [git push](#git-push)
  - [git pull](#git-pull)
  - [git fetch](#git-fetch)
- [Gestión de Issues y Discussions en GitHub](#gestión-de-issues-y-discussions-en-github)
  - [¿Qué es un Issue en GitHub?](#qué-es-un-issue-en-github)
  - [¿Cómo crear un nuevo Issue?](#cómo-crear-un-nuevo-issue)
  - [¿Cómo crear una plantilla de Issues?](#cómo-crear-una-plantilla-de-issues)
  - [¿Cómo sincronizar los cambios en GitHub?](#cómo-sincronizar-los-cambios-en-github)
  - [¿Qué ventajas tiene una plantilla de Issues?](#qué-ventajas-tiene-una-plantilla-de-issues)
  - [¿Cómo personalizar las plantillas de Issues para casos específicos?](#cómo-personalizar-las-plantillas-de-issues-para-casos-específicos)
- [Pull Requests en GitHub](#pull-requests-en-github)
  - [¿Por qué evitar cambios directos en la rama principal?](#por-qué-evitar-cambios-directos-en-la-rama-principal)
  - [¿Cómo funciona un Pull Request?](#cómo-funciona-un-pull-request)
  - [¿Qué papel juega la revisión de código?](#qué-papel-juega-la-revisión-de-código)
  - [¿Cómo se fusiona un Pull Request?](#cómo-se-fusiona-un-pull-request)
  - [¿Cómo puedo practicar Pull Requests de forma efectiva?](#cómo-puedo-practicar-pull-requests-de-forma-efectiva)
- [GitHub Projects](#github-projects)
  - [¿Cómo ayuda GitHub Projects en la organización de proyectos?](#cómo-ayuda-github-projects-en-la-organización-de-proyectos)
  - [¿Cómo crear y gestionar tareas en GitHub Projects?](#cómo-crear-y-gestionar-tareas-en-github-projects)
  - [¿Cómo asignar tareas y gestionar las responsabilidades del equipo?](#cómo-asignar-tareas-y-gestionar-las-responsabilidades-del-equipo)
  - [¿Cómo gestionar múltiples proyectos y tareas personales?](#cómo-gestionar-múltiples-proyectos-y-tareas-personales)
  - [¿Cuál es la importancia de estimar tiempos en GitHub Projects?](#cuál-es-la-importancia-de-estimar-tiempos-en-github-projects)
- [Automatización y Gestión de Proyectos en GitHub](#automatización-y-gestión-de-proyectos-en-github)
  - [¿Cómo vincular y personalizar un proyecto en GitHub?](#cómo-vincular-y-personalizar-un-proyecto-en-github)
  - [¿Cómo gestionar y actualizar actividades dentro del proyecto?](#cómo-gestionar-y-actualizar-actividades-dentro-del-proyecto)
  - [¿Cómo automatizar los cambios de estado en actividades?](#cómo-automatizar-los-cambios-de-estado-en-actividades)
  - [¿Cómo crear y enlazar un issue desde una actividad?](#cómo-crear-y-enlazar-un-issue-desde-una-actividad)
  - [¿Qué ventajas ofrece el flujo automatizado en GitHub?](#qué-ventajas-ofrece-el-flujo-automatizado-en-github)
- [GitHub Gist](#github-gist)
  - [¿Qué es GitHub Gist y cómo se utiliza?](#qué-es-github-gist-y-cómo-se-utiliza)
  - [¿Cómo se usa GitHub Gist para colaboración?](#cómo-se-usa-github-gist-para-colaboración)
  - [¿Cómo se gestionan los Gists en GitHub?](#cómo-se-gestionan-los-gists-en-github)
  - [¿Qué beneficios adicionales ofrece GitHub Gist?](#qué-beneficios-adicionales-ofrece-github-gist)
- [GitHub Codespaces](#github-codespaces)
  - [¿Qué es GitHub Codespaces y cómo funciona?](#qué-es-github-codespaces-y-cómo-funciona)
  - [¿Cómo se crea un Codespace?](#cómo-se-crea-un-codespace)
  - [¿Cuáles son las características clave de Codespaces?](#cuáles-son-las-características-clave-de-codespaces)
  - [¿Cómo se gestiona un proyecto en Codespaces?](#cómo-se-gestiona-un-proyecto-en-codespaces)
  - [¿Cómo hacer commit y sincronizar cambios?](#cómo-hacer-commit-y-sincronizar-cambios)
  - [¿Por qué es importante eliminar Codespaces al terminar?](#por-qué-es-importante-eliminar-codespaces-al-terminar)
- [GitHub Dev Editor](#github-dev-editor)
  - [¿Cómo funciona el GitHub Dev Editor?](#cómo-funciona-el-github-dev-editor)
  - [¿Qué ventajas ofrece frente a otros entornos de desarrollo?](#qué-ventajas-ofrece-frente-a-otros-entornos-de-desarrollo)
  - [¿Cuándo deberías utilizar Codespaces en lugar de GitHub Dev Editor?](#cuándo-deberías-utilizar-codespaces-en-lugar-de-github-dev-editor)
  - [¿Qué debes considerar al escoger entre GitHub Dev Editor y Codespaces?](#qué-debes-considerar-al-escoger-entre-github-dev-editor-y-codespaces)
- [Cómo Usar Tokens en GitHub para Acceso Seguro a Repositorios Privados](#cómo-usar-tokens-en-github-para-acceso-seguro-a-repositorios-privados)
  - [¿Cómo invitar a otros sin hacerlos colaboradores permanentes?](#cómo-invitar-a-otros-sin-hacerlos-colaboradores-permanentes)
  - [¿Qué tipos de tokens existen en GitHub?](#qué-tipos-de-tokens-existen-en-github)
  - [¿Cómo se crea un token clásico?](#cómo-se-crea-un-token-clásico)
  - [¿Cómo funcionan los tokens detallados?](#cómo-funcionan-los-tokens-detallados)
  - [¿Cómo utilizar el token en un entorno externo?](#cómo-utilizar-el-token-en-un-entorno-externo)
  - [¿Para qué otras tareas se pueden utilizar los tokens?](#para-qué-otras-tareas-se-pueden-utilizar-los-tokens)
  - [¿Qué medidas de seguridad deben tomarse con los tokens?](#qué-medidas-de-seguridad-deben-tomarse-con-los-tokens)
- [Gestión de Dependencias y Seguridad con Dependabot en GitHub](#gestión-de-dependencias-y-seguridad-con-dependabot-en-github)
  - [¿Por qué es importante mantener actualizados los paquetes de terceros?](#por-qué-es-importante-mantener-actualizados-los-paquetes-de-terceros)
  - [¿Cómo activar Dependabot en un repositorio?](#cómo-activar-dependabot-en-un-repositorio)
  - [¿Cómo utilizar Dependabot para gestionar versiones específicas?](#cómo-utilizar-dependabot-para-gestionar-versiones-específicas)
  - [¿Qué sucede cuando Dependabot detecta una vulnerabilidad?](#qué-sucede-cuando-dependabot-detecta-una-vulnerabilidad)
  - [¿Por qué integrar Dependabot en el flujo de trabajo?](#por-qué-integrar-dependabot-en-el-flujo-de-trabajo)
- [Gestión de datos sensibles y políticas de seguridad](#gestión-de-datos-sensibles-y-políticas-de-seguridad)
  - [¿Cómo activar CodeQL y Secret Scanning en GitHub?](#cómo-activar-codeql-y-secret-scanning-en-github)
  - [¿Cómo probar si Secret Scanning detecta información sensible?](#cómo-probar-si-secret-scanning-detecta-información-sensible)
  - [¿Qué hacer si GitHub detecta una alerta de seguridad?](#qué-hacer-si-github-detecta-una-alerta-de-seguridad)
  - [¿Por qué CodeQL y Secret Scanning no son suficientes?](#por-qué-codeql-y-secret-scanning-no-son-suficientes)
- [GitHub Actions](#github-actions)
  - [¿Qué es GitHub Actions y cómo puede ayudarte?](#qué-es-github-actions-y-cómo-puede-ayudarte)
  - [¿Cómo configurar tu repositorio de portada en GitHub?](#cómo-configurar-tu-repositorio-de-portada-en-github)
  - [¿Cómo crear una GitHub Action para actualizar tu actividad?](#cómo-crear-una-github-action-para-actualizar-tu-actividad)
  - [¿Cómo asegurarte de que tu GitHub Action funcione correctamente?](#cómo-asegurarte-de-que-tu-github-action-funcione-correctamente)
  - [¿Qué opciones adicionales puedes explorar en GitHub Actions?](#qué-opciones-adicionales-puedes-explorar-en-github-actions)
  - [¿Cómo hacer que tu perfil destaque con otras personalizaciones?](#cómo-hacer-que-tu-perfil-destaque-con-otras-personalizaciones)
- [Introducción a los GitHub Releases](#introducción-a-los-github-releases)
  - [¿Qué son los GitHub Releases?](#qué-son-los-github-releases)
  - [Diferencia entre Tags y Releases](#diferencia-entre-tags-y-releases)
  - [Cómo crear un GitHub Release](#cómo-crear-un-github-release)
  - [Casos de Uso Comunes](#casos-de-uso-comunes)

## ¿Qué son Git y GitHub?

Aprender a gestionar versiones en proyectos de software es fundamental para evitar el caos de múltiples archivos llamados “versión final” y mejorar la colaboración en equipo. Git, un sistema de control de versiones, permite a los desarrolladores trabajar de manera ordenada, manteniendo solo los cambios realizados en los archivos y simplificando el trabajo en equipo al coordinar y sincronizar las modificaciones.

### ¿Qué es Git y por qué debería importarte?

Git es la herramienta de control de versiones más utilizada por programadores. Su función es clara: gestiona versiones de archivos de forma eficaz, algo vital en proyectos colaborativos. Sin Git, los desarrolladores enfrentaban problemas de organización y errores en la sincronización manual de archivos, un proceso que era tan lento como propenso a fallos.

### ¿Quién creó Git y por qué es tan relevante?

El creador de Git es Linus Torvalds, el mismo desarrollador detrás del núcleo de Linux, quien creó esta herramienta para resolver sus propias necesidades de control de versiones. Además, Git es open source, lo que permite a cualquier persona contribuir a su mejora constante, garantizando que siga siendo una herramienta poderosa y en evolución.

### ¿Cómo te beneficia aprender Git desde el inicio?

Desde que comienzas a programar, aprender Git te brinda una ventaja profesional. Esta herramienta te permitirá organizar tu código, colaborar con otros desarrolladores y, eventualmente, contribuir a proyectos externos. En el desarrollo de software, los productos suelen ser el resultado del esfuerzo de un equipo, y Git se vuelve esencial para gestionar el trabajo de manera efectiva.

### ¿Cómo funciona Git en tu entorno de trabajo?

Git se usa en la terminal o en editores como Visual Studio Code, utilizando comandos clave como commit, pull, push, merge, entre otros. Para colaborar en proyectos con otros desarrolladores, se usa una plataforma en la nube como GitHub. Allí puedes almacenar tu código, gestionar versiones y acceder a funcionalidades adicionales que aumentan la productividad y facilitan la colaboración.

[🡡 volver al inicio](#tabla-de-contenido)

## Configuración Inicial de Git: init y config

Trabajar con Git en la terminal permite a los desarrolladores gestionar sus proyectos de manera eficiente.

### ¿Cómo confirmar que Git está instalado en tu sistema?

Para verificar la instalación de Git:

1. Abre la terminal y escribe el comando git --version.
2. Si el comando devuelve un número de versión, Git está listo para usarse.
3. Si no aparece la versión, revisa los recursos adjuntos donde se explican las instalaciones para cada sistema operativo.

### ¿Cómo crear y preparar el primer proyecto con Git?

El primer paso para crear un proyecto en Git es:

1. Limpia la terminal para evitar confusión visual.
2. Crea una carpeta para el proyecto con mkdir nombre_del_proyecto.
3. Navega a la carpeta con cd nombre_del_proyecto.

### ¿Cómo inicializar un repositorio en Git?

Al estar dentro de la carpeta de tu proyecto, inicia el repositorio con:

    git init: Esto crea la rama inicial “master” por defecto.

Si prefieres la rama principal como “main”:

1. Cambia la configuración global escribiendo git config --global init.defaultBranch main.
2. Actualiza la rama en el proyecto actual con git branch -m main.

### ¿Cómo personalizar tu configuración de usuario en Git?

Configura el nombre de usuario y correo electrónico de Git, que identificará todas tus contribuciones:

1. Usa git config --global user.name "Tu Nombre o Apodo".
2. Configura el correo electrónico con git config --global user.email "<tu.email@example.com>".

**Tip:** Si necesitas corregir algún error en el comando, puedes usar la tecla de flecha hacia arriba para recuperar y editar el último comando escrito.

### ¿Cómo confirmar la configuración de Git?

Para revisar tu configuración, ejecuta:

    git config --list: Aquí verás los datos de usuario y el nombre de la rama principal.

Esta configuración se aplicará a todos los repositorios que crees en adelante.

### ¿Qué hacer si olvidas un comando?

Git incluye un recurso rápido y útil para recordar la sintaxis de comandos:

1. Escribe git help en la terminal.
2. Navega la lista de comandos disponibles y consulta la documentación oficial de cada uno cuando sea necesario.

[🡡 volver al inicio](#tabla-de-contenido)

## Comandos Básicos de Git: add, commit y log

Aprender a utilizar Git desde los primeros pasos puede parecer desafiante, pero es esencial para registrar cambios y manejar versiones de cualquier proyecto. Siguiendo un flujo de trabajo sencillo y utilizando los comandos adecuados, puedes dominar el control de versiones y llevar un seguimiento preciso de tus archivos.

### ¿Cómo inicia el control de versiones con Git?

El primer paso es iniciar un repositorio con el comando git init, que crea una carpeta oculta llamada .git en el directorio de trabajo. Esta carpeta actúa como una bitácora, almacenando cada cambio y movimiento de los archivos que se manejan en el proyecto.

### ¿Cómo se crean y agregan archivos a Git?

Para crear un archivo desde la terminal, utiliza un editor como nano. Una vez creado, puedes verificar su existencia y estado con git status, que te mostrará el archivo como no registrado. Para incluirlo en el área de staging, donde estará listo para el commit, usa git add nombre_del_archivo.txt. Esta área de staging es un “limbo” donde decides qué archivos entrarán en el control de versiones.

- Ejemplo de comandos:
  - nano testing.txt para crear el archivo.
  - git add testing.txt para agregarlo al área de staging.

### ¿Qué es el área de staging y cómo funciona?

El área de staging permite revisar los cambios antes de que se registren oficialmente en el repositorio. Los archivos en staging aún no forman parte del historial de versiones; están en espera de que se realice un commit o de ser devueltos a su estado original con:

    git rm --cached nombre_del_archivo.txt

### ¿Cómo realizar el commit de los archivos en Git?

Una vez en staging, se ejecuta git commit -m "mensaje descriptivo" para registrar los cambios en el repositorio. El mensaje en el commit es crucial porque indica la acción realizada, como “nuevo archivo de testing”. Este mensaje permite identificar los cambios de forma clara y ordenada en el historial del proyecto.

    git commit -m "nuevo archivo de testing"

### ¿Cómo gestionar múltiples archivos en Git?

Para trabajar con varios archivos a la vez, utiliza git add . que agrega todos los archivos sin registrar en el área de staging. Puedes decidir entre realizar commits individuales o múltiples en función de la cantidad de archivos y los cambios realizados en cada uno.

### ¿Cómo visualizar el historial de cambios en Git?

El comando git log muestra el historial de commits, proporcionando una vista completa de cada cambio realizado en el proyecto. Esta bitácora permite ver el estado de cada archivo y la información de cada commit.

### ¿Qué sucede al modificar un archivo en Git?

Cuando un archivo se edita, Git lo detecta como “modificado”. El flujo de trabajo para registrar este cambio es el mismo que para un archivo nuevo: git add para llevarlo a staging y git commit para guardar la modificación. Esto asegura que Git mantenga un registro detallado de cada cambio, actualización o eliminación en el proyecto.

### ¿Cómo maneja Git diferentes tipos de archivos?

Git trata cualquier archivo de igual manera, sin importar su extensión o tipo, ya sea de texto, código o imagen. Con git add y git commit, cualquier cambio en estos archivos se registra, facilitando el control de versiones sin importar el tipo de contenido.

[🡡 volver al inicio](#tabla-de-contenido)

## Ramas y Fusión de Cambios: branch, merge, switch y checkout

El uso de ramas en Git permite trabajar en un entorno aislado sin interferir con otros, facilitando la organización y el control del proyecto. Aprender a crear, gestionar y fusionar ramas optimiza la colaboración y ayuda a mantener la limpieza en el historial de cambios.

### ¿Por qué son útiles las ramas en Git?

Las ramas son una herramienta que permite trabajar en tareas específicas sin alterar la rama principal. Entre sus ventajas se encuentran:

- Aislamiento de cambios individuales.
- Posibilidad de desechar una rama sin afectar la principal.
- Organización de actividades múltiples en diferentes ramas.

### ¿Cómo verificar la rama actual?

Para saber en qué rama estás trabajando, ejecuta:

    git branch

El asterisco (\*) indica la rama activa. Inicialmente, suele ser main, pero al crear más ramas, la lista crecerá, permitiéndote ver todas las disponibles y cuál es la actual.

### ¿Cómo crear una nueva rama en Git?

La creación de ramas permite desarrollar sin riesgo en paralelo. Para crear y moverte a una nueva rama, usa:

    git checkout -b

Por ejemplo, git checkout -b Amin crea y mueve a la rama Amin. Puedes verificar que estás en esta rama ejecutando git branch.

### ¿Cómo agregar y confirmar cambios en una rama?

Dentro de una nueva rama, los archivos se editan y confirman sin que impacten otras ramas. Sigue estos pasos para agregar y confirmar:

1. Crea o edita un archivo.
2. Añádelo con:

        git add .

3. Confirma el cambio:

        git commit -m "mensaje de confirmación"

Los cambios ahora son parte de la rama en la que trabajas y no afectan la principal.

### ¿Cómo fusionar cambios de una rama secundaria a la principal?

Para unificar el trabajo en la rama principal:

1. Cambia a la rama principal:

        git switch main

    Nota: Puedes usar también git checkout main.

2. Fusiona la rama secundaria:

        git merge

    Git indicará que el proceso fue exitoso y actualizará el contenido en la rama main con los cambios de la rama secundaria.

### ¿Por qué es importante eliminar ramas que ya no se usan?

Una vez fusionada una rama, es buena práctica eliminarla para evitar desorden. Hazlo con:

    git branch -d

Eliminar ramas que ya cumplieron su propósito previene conflictos y mantiene el entorno de trabajo limpio y organizado.

[🡡 volver al inicio](#tabla-de-contenido)

## Volviendo en el Tiempo en Git: reset y revert

Para quienes se inician en el manejo de versiones con Git, comandos como git reset y git revert se vuelven herramientas indispensables, ya que permiten deshacer errores y ajustar el historial de cambios sin complicaciones. Aunque al avanzar en la experiencia puedan dejarse de lado, dominar su uso resulta clave para un control de versiones eficiente.

### ¿Cuál es la diferencia entre Git Reset y Git Revert?

- Git Reset: mueve el puntero de los commits a uno anterior, permitiendo “volver en el tiempo” y explorar el historial de cambios. Es útil para deshacer actualizaciones recientes o revisar lo que se hizo en cada commit.
- Git Revert: crea un nuevo commit que revierte los cambios de un commit específico, permitiendo conservar el historial original sin eliminaciones. Es ideal para regresar a un estado anterior sin afectar los commits de otros usuarios.

### ¿Cómo se utiliza Git Reset?

1. Ejecuta git log para identificar el historial de commits. El commit actual se marca con HEAD apuntando a main.
2. Si quieres eliminar cambios recientes:
   - Crea un archivo temporal (ejemplo: error.txt) y realiza un commit.
   - Verifica el historial con git log y localiza el hash del commit que deseas restablecer.
3. Para revertir a un estado anterior:
   - Usa git reset con parámetros:
     - --soft: solo elimina el archivo del área de staging.
     - --mixed: remueve los archivos de staging, manteniendo el historial de commits.
     - --hard: elimina los archivos y el historial hasta el commit seleccionado.
   - Este último parámetro debe ser una última opción debido a su impacto irreversible en el historial.

### ¿Cómo funciona Git Revert?

1. Identificación del commit: usa git log para encontrar el commit a revertir.
2. Ejecuta git revert seguido del hash del commit: crea un nuevo commit inverso, preservando el historial.
3. Editar el mensaje de commit: permite dejar claro el motivo de la reversión, ideal en equipos colaborativos para mantener claridad.

### ¿Cuándo es recomendable utilizar Git Reset o Git Revert?

Ambos comandos resultan útiles en diversas situaciones:

- Corrección de errores: si has subido un archivo incorrecto, git revert es rápido y seguro para deshacer el cambio sin afectar el historial.
- Limpieza del historial: en proyectos sólidos, puede que quieras simplificar el historial de commits; git reset ayuda a limpiar entradas innecesarias.
- Manejo de conflictos: en casos extremos de conflicto de archivos, git reset es útil, aunque puede ser mejor optar por resolver conflictos manualmente.

### ¿Cómo aseguras una correcta comunicación en el uso de estos comandos?

- Utiliza estos comandos en sincronización con el equipo.
- Evita el uso de git reset --hard sin coordinación para prevenir la pérdida de trabajo ajeno.
- Documenta cada reversión con un mensaje claro para asegurar el seguimiento de cambios.

[🡡 volver al inicio](#tabla-de-contenido)

## Gestión de versiones: tag y checkout

Git facilita el control de versiones y organización de proyectos, y los comandos git tag y git checkout son piezas clave para una gestión eficiente y ordenada de los cambios en el código. Ambos comandos ayudan a crear puntos de referencia y explorar cambios sin afectar el desarrollo principal, ofreciendo opciones robustas para pruebas y organización.

### ¿Cómo se utiliza git tag para organizar versiones?

El comando git tag permite marcar un commit con una etiqueta descriptiva, ideal para señalar versiones estables o hitos importantes en el proyecto. Esto resulta útil en proyectos donde el equipo necesita identificar fácilmente puntos clave de avance. Al etiquetar, se añade una nota visible en el historial, lo cual facilita encontrar versiones específicas en un flujo de trabajo con muchos commits.

Para crear un tag:

- Escribe git tag -a v1.0 -m "primera versión estable" y presiona Enter.
- Al consultar git log, se verá el tag junto al commit en el historial.

Además, git show muestra detalles de la etiqueta, quién la creó, el mensaje de la versión y los cambios asociados a ese commit. Esto es especialmente útil cuando el historial es extenso, ya que permite regresar a puntos específicos sin necesidad de revisar cada commit en el log completo.

Para eliminar un tag:

- Usa git tag -d v1.0 para remover el tag sin afectar el historial ni los archivos. Esto es conveniente si el nombre del tag necesita ser corregido o ajustado.

### ¿Qué permite git checkout al explorar el historial?

El comando git checkout tiene usos más amplios que solo cambiar entre ramas. También permite revisar commits previos para explorar o probar cambios sin alterar la rama principal. Al usar git checkout , puedes regresar a un punto específico en el historial y evaluar cómo afectaban los cambios al proyecto en ese momento.

Por ejemplo:

1. Cambia a un commit específico con git checkout .
2. Realiza pruebas o modificaciones. Esto te permite simular cambios o ver el estado del proyecto en esa versión.
3. Para regresar a la rama principal, escribe git checkout main. Esto restaura el proyecto al estado actual y evita que los cambios temporales afecten el historial o la estructura del proyecto.

Al navegar entre commits y regresar a main, es importante notar que no se crean ramas adicionales, ni se modifican commits previos, lo cual asegura la integridad del historial y la rama principal.

### ¿Cómo integran git tag y git checkout una experiencia de desarrollo ordenada?

Ambos comandos permiten explorar y organizar sin interferir en el flujo principal del trabajo. Git tag marca versiones y puntos importantes, actuando como separadores en el historial, mientras que git checkout permite regresar a esos puntos y probar sin comprometer la rama actual. Esto proporciona una estructura en la que el equipo puede trabajar con libertad para realizar pruebas, versionar cambios y retornar al estado actual en cualquier momento sin temor a alterar el trabajo original.

[🡡 volver al inicio](#tabla-de-contenido)

## Cómo Resolver Conflictos de Ramas en Git

Cuando trabajamos en equipo, el manejo de conflictos de ramas en Git es esencial para evitar problemas y asegurar una integración fluida de cambios en los archivos compartidos. Aquí te mostramos cómo se genera un conflicto de ramas y la forma efectiva de resolverlo paso a paso.

### ¿Qué es un conflicto de ramas en Git?

En un entorno colaborativo, es común que varias personas realicen modificaciones en archivos compartidos. Esto puede llevar a conflictos de ramas cuando intentamos fusionar cambios y estos alteran las modificaciones previas realizadas por otro colaborador. En estos casos, se debe elegir qué cambios se mantendrán en la rama principal.

### ¿Cómo crear un conflicto de ramas para aprender a resolverlo?

Para experimentar y entender cómo resolver un conflicto, podemos crear uno intencionalmente. Aquí están los pasos básicos:

- Verifica tu rama actual con git branch. Si solo tienes la rama main, estás listo para iniciar.
- Crea un archivo, por ejemplo, conflict.txt, añade contenido inicial (e.g., “línea original”) y realiza un commit:

        git add conflict.txt
        git commit -m "Archivo de conflicto creado"

- Crea una nueva rama con git checkout -b developer y modifica el archivo con nuevos cambios, como “cambios desde la rama dev”, realiza un commit.
- Vuelve a la rama main con git checkout main y modifica el mismo archivo en esta rama, por ejemplo, añadiendo “segundo cambio desde main”, y realiza otro commit.

Al regresar a main y realizar la fusión de developer, verás el conflicto.

### ¿Cómo resolver un conflicto de ramas en Git?

Cuando Git detecta un conflicto, te indicará las diferencias entre las ramas con etiquetas que facilitan la identificación de cambios:

- Abre el archivo en conflicto. Verás secciones como <<<<< HEAD y >>>>>, que marcan los cambios en main y en la rama que intentas fusionar (developer).
- Edita el archivo eliminando las líneas de marcación y decide cuáles cambios deseas conservar, combinar o incluso reescribir.
- Guarda el archivo sin las señalizaciones de conflicto y realiza un commit para registrar la resolución:

        git add conflict.txt
        git commit -m "Conflicto resuelto"

### ¿Qué hacer después de resolver un conflicto?

Una vez resuelto el conflicto y unificada la versión final en main, considera eliminar la rama developer para evitar conflictos futuros. Esto ayuda a mantener el historial de cambios limpio y reduce la posibilidad de cometer errores en el futuro.

[🡡 volver al inicio](#tabla-de-contenido)

## Por qué GitHub es clave para los Desarrolladores

La colaboración en proyectos de software depende de sistemas de control de versiones, y Git es una herramienta central para lograrlo. Usar GitHub, una plataforma en la nube basada en Git, permite que los desarrolladores compartan sus proyectos, trabajen en equipo y accedan a herramientas avanzadas para asegurar y escalar sus desarrollos. Con un enfoque en inteligencia artificial (IA), colaboración, productividad, seguridad y escalabilidad, GitHub ha pasado de ser una red social de programadores a una herramienta integral que optimiza el desarrollo de software moderno.

### ¿Qué opciones existen para hospedar proyectos en Git?

- GitHub: la plataforma más destacada, adquirida por Microsoft en 2018, ofrece amplias herramientas de colaboración y desarrollo.
- Bitbucket (Atlassian), GitLab, Azure DevOps (Microsoft), CodeCommit (Amazon), y Cloud Source (Google): todas permiten el control de versiones en la nube.
- Servidores propios de Git: para quienes prefieren un ambiente privado y controlado.

### ¿Cómo ha evolucionado GitHub desde su lanzamiento?

Inicialmente, GitHub era un simple repositorio de código en la nube; sin embargo, ha evolucionado hasta ofrecer una plataforma avanzada que incluye una interfaz web, herramientas de línea de comandos y flujos de trabajo colaborativos. En lugar de limitarse a compartir proyectos, permite a los usuarios colaborar en tiempo real, automatizar tareas y utilizar inteligencia artificial para mejorar la seguridad y productividad del código.

### ¿Qué funcionalidades destacan en GitHub actualmente?

GitHub ahora integra IA y facilita procesos clave en el desarrollo de software mediante:

- Colaboración eficiente: herramientas para trabajo en equipo, seguimiento de cambios y mejoras en el flujo de trabajo.
- Automatización y productividad: automatiza tareas repetitivas, permitiendo a los desarrolladores enfocarse en resolver problemas complejos.
- Seguridad integrada: herramientas avanzadas de seguridad que aseguran el código desde el inicio, minimizando riesgos.
- Escalabilidad: una infraestructura robusta que permite gestionar millones de repositorios y usuarios globalmente.

### ¿Qué oportunidades brinda GitHub para los desarrolladores?

Con GitHub, cualquier desarrollador puede contribuir a proyectos relevantes, como mejoras en lenguajes de programación o incluso en el kernel de Linux. Esta capacidad de colaboración global eleva el nivel de la ingeniería de software, fomentando el trabajo en equipo entre profesionales de todo el mundo.

### ¿Cómo puede ayudarte GitHub en el desarrollo profesional?

Además de ser una herramienta de colaboración y desarrollo, GitHub ofrece la GitHub Foundation Certification, una certificación ideal para validar habilidades en GitHub y dar un primer paso hacia un perfil profesional sólido en desarrollo colaborativo.

[🡡 volver al inicio](#tabla-de-contenido)

## ¿Cómo integrar Git y GitHub en un flujo de trabajo profesional?

Para entender cómo Git y GitHub funcionan en conjunto en un flujo de trabajo profesional, debemos recordar que Git es una herramienta de control de versiones basada en comandos, mientras que GitHub facilita su implementación al ofrecer una plataforma que permite manejar proyectos de Git de forma colaborativa y accesible en la nube.

### ¿Cuál es la relación entre Git y GitHub?

Aunque Git y GitHub son complementarios, no fueron creados por los mismos desarrolladores ni comparten una dependencia directa. Git es el sistema de control de versiones en sí mismo, mientras que GitHub es un servicio que permite alojar repositorios Git en la nube, facilitando el trabajo colaborativo. La única conexión entre ambos es que GitHub permite gestionar proyectos que usan Git para el control de versiones.

### ¿Cómo se inicia el flujo de trabajo en GitHub?

Para trabajar en un proyecto en GitHub, en lugar de comenzar con git init en tu máquina local, creas un repositorio en GitHub. Este repositorio vacío se descarga al equipo y, desde ahí, se pueden hacer cambios locales. La estructura básica del flujo de trabajo incluye los siguientes pasos:

- Crear un commit: Guardar los cambios realizados localmente.
- Subir cambios a GitHub: Una vez los cambios estén listos, se suben a una rama separada en el repositorio remoto.

### ¿Por qué es importante trabajar en ramas?

Trabajar en una rama separada permite mantener el código principal estable mientras trabajas en nuevas características. Al subir la rama a GitHub, el proceso de Code Review comienza. Otros compañeros revisarán y aprobarán los cambios antes de integrarlos en la rama principal.

### ¿Qué reglas se pueden seguir para crear tareas?

Para facilitar la revisión de código y evitar conflictos, es ideal mantener las tareas pequeñas y con un solo objetivo. Esto hace que:

- El proceso de revisión sea sencillo.
- Los cambios sean menos propensos a conflictos al integrarse al proyecto principal.

Algunos equipos imponen reglas como limitar el número de archivos modificados o la cantidad de líneas de código en una tarea, aunque una recomendación básica es “una tarea, un objetivo”.

[🡡 volver al inicio](#tabla-de-contenido)

## Gestión de Repositorios en GitHub

Crear y gestionar un repositorio en GitHub es una habilidad esencial para colaborar y mantener proyectos de software de forma ordenada. Aquí aprenderás cómo crear, configurar, invitar colaboradores y clonar un repositorio de manera efectiva.

### ¿Cómo crear un repositorio en GitHub?

Para empezar, accede a la pantalla principal de tu perfil en GitHub y selecciona el símbolo de “+”. Aquí, selecciona la opción “Nuevo repositorio”, lo que abrirá un formulario para configurarlo:

- Propietario: Elige tu usuario actual como propietario del repositorio.
- Nombre del repositorio: Puedes asignarle un nombre como “mi-primer-repo”. Este nombre puede adaptarse a tu usuario, permitiendo reutilizar nombres similares.
- Descripción: Añade una breve descripción del proyecto para facilitar su identificación.
- Visibilidad: Decide si el repositorio será público o privado según las necesidades del proyecto.
- Inicialización: Puedes agregar un archivo README para documentar el repositorio desde el inicio. Aunque opcional, es una buena práctica.

Finalmente, selecciona el botón verde de “Crear repositorio” para completar este proceso. Al hacerlo, tendrás acceso directo a tu repositorio con el archivo README visible.

### ¿Cómo agregar un colaborador a un repositorio en GitHub?

Para trabajar en equipo, es fundamental añadir colaboradores. Esto se hace desde la sección de “Settings” del repositorio:

1. Dirígete a “Colaboradores” en la configuración.
2. Asegúrate de que el colaborador tenga una cuenta de GitHub.
3. Selecciona la opción de agregar usuarios y elige a quien quieras invitar.

Una vez enviada la invitación, deberás esperar que el colaborador la acepte para que pueda acceder al repositorio y trabajar en él.

### ¿Cómo clonar un repositorio en tu máquina local?

Clonar el repositorio te permite trabajar desde tu entorno local y sincronizar cambios con GitHub. Para ello:

1. Ve a la sección de “Code” dentro de tu repositorio.
2. Selecciona la opción HTTPS y copia la URL del repositorio.
3. En tu terminal, escribe git clone seguido de la URL copiada y presiona “enter”.

Este comando descargará el repositorio en tu máquina. Podrás ver todos los archivos en una carpeta con el nombre del repositorio y comenzar a trabajar de manera local.

### ¿Cómo integrar Git y GitHub para un flujo de trabajo colaborativo?

Una vez que el repositorio está clonado en tu entorno local, puedes editar archivos, guardar cambios y subirlos de nuevo a GitHub mediante Git. Al hacer esto, permites que todos los colaboradores se mantengan sincronizados y al día con el desarrollo del proyecto.

[🡡 volver al inicio](#tabla-de-contenido)

## Cómo configurar SSH para GitHub

Usar SSH para interactuar con GitHub es una excelente forma de aumentar la seguridad y mejorar la comodidad en el manejo de repositorios. A continuación, te explicamos el paso a paso para generar y configurar tus llaves SSH en distintos sistemas operativos y cómo integrarlas en tu perfil de GitHub para mejorar la experiencia de clonación y autenticación.

### ¿Por qué es mejor usar SSH en lugar de HTTPS para GitHub?

- Seguridad adicional: SSH permite autenticar la computadora específica que accede a los repositorios sin necesidad de ingresar una contraseña cada vez.
- Comodidad: Evita la necesidad de escribir tu contraseña en cada operación con GitHub, agilizando el flujo de trabajo.

### ¿Cómo generar una llave SSH en Windows y Linux?

1. Instalar WSL si estás en Windows (opcional si usas Linux nativo).
2. Verificar que no tienes llaves previas: Ve al menú de “Code” en GitHub y verifica que la opción de SSH no tenga llaves configuradas.
3. Generar la llave SSH: En la terminal, usa el comando:

        ssh-keygen -t ed25519 -C "tu_correo@example.com"

    - -t ed25519 establece el nivel de encriptación.
    - -C añade un comentario con tu correo, útil para identificar la llave en GitHub.

4. Guardar y proteger la llave:

    - Usa el nombre por defecto y añade una contraseña segura.
    - La llave pública se guarda en el directorio .ssh, generalmente nombrada id_ed25519.pub.

5. Configurar el agente SSH: Activa el agente de SSH y añade la llave privada:

        eval "$(ssh-agent -s)"
        ssh-add ~/.ssh/id_ed25519

### ¿Cómo añadir la llave SSH a GitHub?

1. Abrir el archivo de la llave pública (id_ed25519.pub) y copia el contenido.
2. En GitHub, ve a Settings > SSH and GPG keys > New SSH key y pega la llave.
3. Nombra la llave de acuerdo a la computadora en la que estás configurándola.

### ¿Qué pasos adicionales seguir en Mac?

1. Crear el archivo de configuración SSH: Abre o crea el archivo config dentro del directorio .ssh.
2. Agregar parámetros específicos de Mac: Añade la configuración para integrar SSH con el sistema Keychain:

        Host github.com
            AddKeysToAgent yes
            UseKeychain yes
            IdentityFile ~/.ssh/id_ed25519

3. Añadir la llave al agente SSH con Keychain: Usa el comando:

        ssh-add --apple-use-keychain ~/.ssh/id_ed25519

### ¿Cómo verificar la conexión con GitHub?

1. Comprobar autenticación: En la terminal, ejecuta el comando:

        ssh -T git@github.com

    - Escribe “yes” para confirmar la conexión.
    - Aparecerá un mensaje de GitHub que confirma la autenticidad.

### ¿Cómo clonar un repositorio usando SSH?

1. En GitHub, selecciona el repositorio deseado, elige la opción de clonación por SSH y copia la URL.
2. En la terminal, ejecuta:

        git clone git@github.com:usuario/repositorio.git

3. Esto clona el repositorio sin solicitar contraseña, aprovechando la autenticación SSH.

[🡡 volver al inicio](#tabla-de-contenido)

## Clone, fork y estrellas a repositorios

Entender el uso de forks y estrellas en GitHub optimiza la gestión de proyectos y recursos al trabajar en esta plataforma. Aquí exploraremos cómo funcionan estos elementos y cómo pueden ayudarte a organizar tus repositorios en función de tus necesidades.

### ¿Qué es un fork y cómo se utiliza?

Un fork en GitHub es una copia de un repositorio alojado en la cuenta de otra persona y que puedes transferir a tu propia cuenta. Este proceso crea una réplica del repositorio en su estado actual, sin reflejar futuros cambios del original a menos que se sincronice manualmente. Esto permite:

- Trabajar de manera independiente en un proyecto sin afectar el repositorio original.
- Personalizar el contenido según tus necesidades sin modificar el repositorio fuente.
- Crear una base para hacer contribuciones posteriores al repositorio original.

Para crear un fork, debes abrir el repositorio, seleccionar el botón de Fork y seguir los pasos para copiarlo en tu cuenta. Así, GitHub duplicará el repositorio, manteniendo el nombre y descripción del original. Puedes optar por copiar solo la rama principal (main) o todo el proyecto. Luego, desde tu cuenta, podrás modificar el contenido sin interferir con el repositorio original.

### ¿Qué beneficios aporta usar estrellas en GitHub?

Las estrellas en GitHub funcionan como un sistema de marcado para resaltar los repositorios que deseas tener a mano como referencia o favoritos. Son útiles para:

- Crear un índice de repositorios de referencia o inspiración.
- Acceder rápidamente a recursos clave desde tu perfil.
- Seguir el desarrollo de proyectos importantes para tus intereses.

Al seleccionar la estrella en un repositorio, ésta se ilumina para indicar que has marcado este recurso. Puedes acceder a todos tus repositorios marcados desde la sección de “tus estrellas” en tu perfil. Aquí se listan los proyectos que has destacado, ayudándote a centralizar tus fuentes de consulta.

### ¿Cómo clonar un repositorio forkeado?

Después de realizar un fork, puedes clonar este repositorio a tu entorno local para trabajar de forma directa en tu equipo. Para hacerlo:

1. Ve a tu repositorio forkeado.
2. Selecciona el botón Code y copia la URL del proyecto en formato SSH.
3. Abre la terminal y usa el comando git clone .

De esta manera, tendrás una versión local del repositorio en la que podrás modificar y gestionar el código. Esta técnica de fork y clonación es útil para personalizar proyectos o experimentar sin afectar el original, ofreciendo flexibilidad para hacer cambios sin alterar el repositorio fuente.

### ¿Por qué usar forks en lugar de clonar directamente el repositorio original?

Hacer un fork en lugar de una clonación directa del repositorio original permite que trabajes de manera independiente. Puedes hacer ajustes sin el riesgo de cambiar el repositorio base, especialmente útil cuando el original es de terceros o si planeas realizar cambios extensivos. Además, el fork es una base ideal para hacer contribuciones futuras, ya que se puede sincronizar y enviar cambios al proyecto original a través de un proceso estructurado.

[🡡 volver al inicio](#tabla-de-contenido)

## Trabajo con repositorios remotos: push, pull y fetch

### git push

Esto envía tus cambios en la rama main al repositorio remoto llamado origin. Esto envía tus cambios en la rama main al repositorio remoto llamado origin. Este comando se utiliza para enviar los cambios locales (commits) a un repositorio remoto. Es decir, actualiza el repositorio en línea con los cambios que has realizado en tu copia local.

    git push origin main

Esto envía tus cambios en la rama main al repositorio remoto llamado origin.

### git pull

Este comando se utiliza para obtener y fusionar (merge) cambios desde un repositorio remoto hacia tu copia local. Es como un fetch seguido de un merge.

    git pull origin main

Esto obtiene los últimos cambios de la rama `main` del repositorio remoto `origin` y los fusiona con tu rama local actual.

### git fetch

Este comando descarga los cambios del repositorio remoto, pero no los fusiona automáticamente en tu rama actual. Simplemente actualiza la información sobre las ramas remotas.

    git fetch origin

Esto descarga los cambios desde el repositorio remoto `origin`, pero no los aplica a tu rama local. Puedes ver los cambios en las ramas remotas antes de decidir fusionarlos.

### Resumen

- `push`: Envia tus cambios locales al remoto.
- `pull`: Trae y fusiona cambios del remoto a tu local.
- `fetch`: Trae cambios del remoto sin fusionarlos automáticamente.

[🡡 volver al inicio](#tabla-de-contenido)

## Gestión de Issues y Discussions en GitHub

Usar los Issues de GitHub permite gestionar y documentar problemas en un repositorio, desde errores simples en la redacción hasta defectos complejos en la funcionalidad. Con una interfaz intuitiva, permite que cualquier usuario señale y describa aspectos mejorables, y con plantillas de Issues, mejora la claridad y colaboración en el proceso.

### ¿Qué es un Issue en GitHub?

Un Issue es una forma de señalar problemas o sugerencias dentro de un repositorio. Puede ser usado para:

- Notificar errores en la documentación, como faltas de ortografía.
- Reportar problemas en el funcionamiento esperado del código.
- Informar mejoras o cambios necesarios.

Los Issues permiten una comunicación bidireccional entre los colaboradores y el creador del repositorio, lo que facilita la resolución de problemas.

### ¿Cómo crear un nuevo Issue?

1. En el repositorio de GitHub, selecciona la pestaña Issues.
2. Haz clic en New Issue y describe el problema en dos campos principales:

   - Título: Una breve descripción.
   - Descripción: Detalles del problema, pasos para reproducirlo, etc.

Es posible agregar elementos adicionales, como asignar el Issue a otra persona o etiquetarlo.

### ¿Cómo crear una plantilla de Issues?

Para facilitar el proceso a otros colaboradores, es útil crear plantillas de Issues. Para hacerlo:

1. Desde el repositorio, abre Visual Studio Code con el comando code ..
2. Crea una carpeta llamada .github y dentro otra carpeta llamada ISSUE_TEMPLATE.
3. Dentro de ISSUE_TEMPLATE, crea un archivo Markdown (por ejemplo, bug_report.md).
4. Copia la estructura de la plantilla, que usualmente incluye secciones como descripción, pasos para reproducir el error y detalles adicionales.

Con esta plantilla, los colaboradores tendrán un formato estándar para reportar problemas, lo que ayuda a una mejor gestión y resolución.

### ¿Cómo sincronizar los cambios en GitHub?

1. Una vez creada la plantilla, verifica que los archivos cambiados estén marcados en verde en Visual Studio Code.
2. Realiza un commit (por ejemplo, “Bug Report agregado”).
3. Sincroniza con el repositorio de GitHub mediante el botón de flecha hacia arriba (push).
4. En GitHub, verifica que la plantilla esté disponible en la sección de Issues.

### ¿Qué ventajas tiene una plantilla de Issues?

Las plantillas simplifican el proceso de documentación de problemas y mejoran la comunicación al estandarizar la información que se solicita a los colaboradores. Esto ayuda a identificar los problemas de forma precisa y rápida.

### ¿Cómo personalizar las plantillas de Issues para casos específicos?

Además de la plantilla básica para bugs, puedes crear plantillas personalizadas como:

- Document Report: Para señalar errores en la documentación.
- Mejores prácticas: Para sugerir mejoras en la estructura del código.

Estas plantillas permiten a los colaboradores elegir el tipo de Issue que mejor se adapta al problema y agilizan la gestión del repositorio.

[🡡 volver al inicio](#tabla-de-contenido)

## Pull Requests en GitHub

Colaborar en GitHub requiere evitar modificar directamente la rama principal, lo que podría causar conflictos con el trabajo de otros compañeros. En su lugar, trabajar en ramas individuales y fusionarlas mediante Pull Requests (PR) es clave para un flujo de trabajo colaborativo y seguro.

### ¿Por qué evitar cambios directos en la rama principal?

Realizar cambios directamente en la rama principal (main) puede sobrescribir el trabajo no sincronizado de otros colaboradores. Este error común se evita al:

- Crear una rama separada para cada contribuyente.
- Fusionar cambios mediante una revisión en el Pull Request, antes de unirlos a la rama principal.

### ¿Cómo funciona un Pull Request?

1. Crear una Rama Nueva: Al iniciar cambios, crea una rama local específica. Por ejemplo, developer01.
2. Subir la Rama a GitHub: Usa git push -u origin para subir tu rama.
3. Notificar al Equipo: Al crear un Pull Request, notificas al equipo sobre tus cambios, lo que permite una revisión colaborativa (Code Review).

### ¿Qué papel juega la revisión de código?

El Code Review en los Pull Requests permite:

- Evaluar y comentar los cambios antes de fusionarlos.
- Aumentar la calidad y la visibilidad de los cambios propuestos.

Aunque puede ser intimidante al principio, esta práctica asegura transparencia y mejora continua en el equipo.

### ¿Cómo se fusiona un Pull Request?

1. Comparación y Revisión: Una vez que el equipo revisa los cambios y los aprueba, GitHub facilita la fusión con la rama principal.
2. Resolver Conflictos: GitHub verifica automáticamente conflictos potenciales, mostrando una marca verde si está listo para fusionarse sin problemas.
3. Eliminar la Rama: Tras la fusión, se elimina la rama para mantener el repositorio ordenado y listo para nuevas tareas.

### ¿Cómo puedo practicar Pull Requests de forma efectiva?

Para mejorar, colabora con un amigo o colega, practicando la creación y revisión de Pull Requests. Esta interacción entre ramas te ayudará a familiarizarte y a fluir con confianza en el proceso de colaboración en GitHub.

[🡡 volver al inicio](#tabla-de-contenido)

## GitHub Projects

Las herramientas colaborativas en GitHub han evolucionado, haciendo posible una organización eficaz y centralizada del trabajo en equipo sin la necesidad de mensajes o correos constantes. GitHub Projects destaca como una herramienta clave que permite gestionar tareas, fechas y recursos dentro de un solo espacio.

### ¿Cómo ayuda GitHub Projects en la organización de proyectos?

GitHub Projects facilita la organización de actividades dentro de equipos, permitiendo asignar tareas y priorizarlas según su urgencia. La herramienta cuenta con plantillas para diferentes tipos de proyectos, como la de Team Planning (planificación en equipo), que organiza tareas en un tablero Kanban con tres columnas: “Por hacer”, “En progreso” y “Hechas”.

### ¿Cómo crear y gestionar tareas en GitHub Projects?

Para crear una tarea en un proyecto de GitHub:

- Accede a “Projects” en tu perfil y selecciona New Project.
- Elige la plantilla que mejor se adapte al tipo de proyecto.
- Crea una nueva actividad, por ejemplo, “Actualizar proyecto HTML”. Esto permitirá que todos en el equipo sepan qué tareas están pendientes.

Además, puedes definir prioridades, tamaños y tiempos estimados para cada tarea, basándote en metodologías ágiles, lo cual ayuda a coordinar el esfuerzo del equipo y optimizar el rendimiento en cada iteración.

### ¿Cómo asignar tareas y gestionar las responsabilidades del equipo?

Dentro de GitHub Projects, es posible asignar tareas a miembros del equipo, mostrando claramente las responsabilidades de cada persona. Cada tarea puede vincularse a un repositorio específico seleccionando la opción Convertir a un issue, lo que permite una relación directa entre la actividad y el código. Esta vinculación muestra un número identificador, útil para nombrar ramas en el repositorio y facilitar la organización.

### ¿Cómo gestionar múltiples proyectos y tareas personales?

Para aquellos que participan en varios proyectos o trabajan como freelancers, GitHub Projects es una solución que permite centralizar actividades y manejar múltiples repositorios. Al seleccionar la pestaña My Items, se filtran todas las tareas asignadas a ti, ayudándote a enfocarte sin distracciones.

### ¿Cuál es la importancia de estimar tiempos en GitHub Projects?

Aprender a estimar tiempos de manera precisa es esencial para el trabajo en equipo. GitHub Projects permite practicar la estimación del tiempo y la carga de trabajo en cada tarea, lo que ayuda a los desarrolladores a mejorar en la gestión de su propio tiempo y a contribuir de manera eficiente al equipo, evitando interrupciones.

[🡡 volver al inicio](#tabla-de-contenido)

## Automatización y Gestión de Proyectos en GitHub

Automatizar tareas en proyectos de software es esencial para ahorrar tiempo y mejorar la productividad. Con GitHub Projects, puedes configurar flujos de trabajo automáticos que simplifican la gestión y seguimiento de actividades, permitiendo un enfoque directo en el código.

### ¿Cómo vincular y personalizar un proyecto en GitHub?

1. Accede a tu repositorio en GitHub y selecciona la categoría de “Projects.”
2. Si no tienes un proyecto vinculado, selecciona la opción “Enlazar a un proyecto.”
3. Edita el proyecto sin título agregando un nombre relevante, como “Mi proyecto individual,” y, opcionalmente, una descripción y un README.
4. Guarda los cambios y regresa al repositorio para enlazar este proyecto.

### ¿Cómo gestionar y actualizar actividades dentro del proyecto?

- Dentro de tu proyecto vinculado, crea actividades como “Actualizar archivo HTML,” “Actualizar archivo CSS,” o “Actualizar archivo JavaScript.”
- Marca el estado de cada tarea: en progreso, pendiente o completada.
- Usa la sección “Insights” para ver un gráfico del estado de las actividades y medir la eficacia del equipo.

### ¿Cómo automatizar los cambios de estado en actividades?

- Entra en los flujos de trabajo (Workflows) seleccionando los tres puntos en la esquina superior de tu proyecto.
- Configura las reglas, por ejemplo, para que un issue o pull request cerrado cambie automáticamente el estado de la actividad a “Hecho.”
- Personaliza otros workflows como el cambio de estado cuando un pull request es aprobado, asegurando que la automatización se adapte a tus necesidades.

### ¿Cómo crear y enlazar un issue desde una actividad?

1. Selecciona una actividad como “Actualizar archivo CSS,” presiona los tres puntos y conviértela en un issue en el repositorio.
2. Crea una nueva rama desde la sección de ramas, nómbrala de forma clara, y agrega los cambios necesarios en el archivo, por ejemplo, un nuevo archivo style.css.
3. Guarda los cambios, crea un pull request y describe los cambios. Usa la palabra clave closes seguido del número de issue para que GitHub lo cierre automáticamente cuando se apruebe el pull request.

### ¿Qué ventajas ofrece el flujo automatizado en GitHub?

Con esta automatización:

- El estado de las tareas se actualiza solo, sin necesidad de hacerlo manualmente.
- Los workflows pueden expandirse para notificar por Slack, Teams o correo electrónico cada vez que un pull request se cierra, facilitando la comunicación y el seguimiento en equipo.
- GitHub Projects, junto con estas integraciones, permite un flujo de trabajo robusto y ágil.

[🡡 volver al inicio](#tabla-de-contenido)

## GitHub Gist

GitHub Gist permite compartir y discutir fragmentos de código de forma sencilla, sin necesidad de crear un repositorio completo. Esta herramienta es ideal para obtener retroalimentación rápida y colaborativa sin comprometer los cambios en un proyecto principal.

### ¿Qué es GitHub Gist y cómo se utiliza?

GitHub Gist es una funcionalidad de GitHub diseñada para almacenar y compartir pequeños fragmentos de código. A diferencia de un repositorio tradicional, un Gist no se vincula a un proyecto completo, sino que permite discutir una pieza de código de manera aislada, ideal para colaboración rápida.

- Crear un Gist: Ingresa a gist.github.com, pega el fragmento de código y añade una descripción breve.
- Compartir el enlace: Copia la URL generada y compártela con tus colaboradores para abrir la discusión.
- Feedback en tiempo real: Los colaboradores pueden comentar directamente en el Gist, permitiendo iteraciones y mejoras rápidas.

### ¿Cómo se usa GitHub Gist para colaboración?

La simplicidad de los Gists facilita el trabajo en equipo al ofrecer un espacio directo de intercambio de ideas y mejoras sin alterar el proyecto base.

- Conversación activa: Puedes recibir y responder comentarios sobre el fragmento de código.
- Actualización en tiempo real: Si el colaborador sugiere cambios, puedes editar el Gist y mejorar el código sin necesidad de crear nuevas ramas.
- Ventajas en pair programming: Un Gist puede ser usado como base en sesiones de pair programming, manteniendo el enfoque en mejoras puntuales y rápidas.

### ¿Cómo se gestionan los Gists en GitHub?

GitHub permite gestionar y organizar fácilmente los Gists en tu perfil, lo que facilita tener una colección de snippets reutilizables.

- Acceso rápido: Los Gists se encuentran en tu perfil y pueden organizarse en una colección para referencias futuras.
- Eliminar Gists innecesarios: Si un Gist ya no es útil, puede eliminarse sin afectar otros proyectos.
- Edición y actualización: Los Gists pueden editarse directamente para mantener el código actualizado según las necesidades del proyecto.

### ¿Qué beneficios adicionales ofrece GitHub Gist?

Además de la colaboración, los Gists son útiles para mantener una biblioteca personal de snippets de código, mejorando la eficiencia en nuevos proyectos.

- Biblioteca personal: Guarda configuraciones iniciales o fragmentos reutilizables para evitar escribir código repetitivo.
- Probar ideas antes de integrarlas: Permite experimentar con variantes de código antes de incorporarlas oficialmente.
- Ahorro de tiempo: Facilita el acceso y reutilización de código en proyectos similares, optimizando el flujo de trabajo.

[🡡 volver al inicio](#tabla-de-contenido)

## GitHub Codespaces

GitHub Codespaces es una herramienta poderosa que permite crear y gestionar entornos de desarrollo en la nube, aumentando la flexibilidad y productividad para desarrolladores en cualquier lugar. Con una interfaz similar a Visual Studio Code, Codespaces permite desarrollar proyectos desde cualquier dispositivo, sin importar si está instalado el entorno completo en la máquina local.

### ¿Qué es GitHub Codespaces y cómo funciona?

GitHub Codespaces ofrece entornos de desarrollo alojados en máquinas virtuales en la nube. Esto permite a los desarrolladores trabajar desde cualquier dispositivo, como una tableta o teléfono, en proyectos alojados en repositorios de GitHub. Con acceso a herramientas de compilación y despliegue, se puede trabajar con múltiples lenguajes de programación sin necesidad de instalarlos localmente.

### ¿Cómo se crea un Codespace?

Para iniciar un Codespace:

- Selecciona “New Codespace” en el menú.
- Escoge el repositorio en el que vas a trabajar.
- Elige la rama y región que prefieras.
- Configura el tipo de máquina virtual, seleccionando entre diferentes núcleos y memoria RAM según la necesidad del proyecto.

Una vez creado, se abre una interfaz de desarrollo completa, que incluye explorador de archivos, terminal integrada y control de versiones.

### ¿Cuáles son las características clave de Codespaces?

Algunas funcionalidades destacadas incluyen:

- Explorador de archivos y extensiones: permite administrar archivos y añadir extensiones, igual que en VS Code.
- Terminal integrada: facilita ejecutar comandos sin salir del entorno.
- Preconfiguración de entornos: lenguajes como Node, Python y .NET ya están instalados, permitiendo trabajar sin configurarlos en la máquina local.

### ¿Cómo se gestiona un proyecto en Codespaces?

Puedes crear y gestionar proyectos en múltiples lenguajes. Por ejemplo, para un proyecto en .NET:

- Crea una carpeta para el proyecto en la rama del repositorio.
- Usa comandos como .NET new console para iniciar el proyecto, sin preocuparte por tener .NET instalado localmente.
- La terminal permite ejecutar el proyecto con .NET run y hacer ajustes sobre la marcha.

### ¿Cómo hacer commit y sincronizar cambios?

Al realizar cambios en el proyecto, estos se pueden ver en la sección de control de versiones:

1. Añade un mensaje de commit que describa los cambios.
2. Sincroniza los cambios para reflejarlos en el repositorio de GitHub.

Esta integración asegura que cada modificación quede guardada y reflejada en GitHub, como si se hubiese hecho en un entorno local.

### ¿Por qué es importante eliminar Codespaces al terminar?

Cada Codespace utiliza recursos de GitHub y, en cuentas gratuitas, existe un límite de 120 horas de uso al mes. Al completar una tarea:

- Elimina el Codespace para evitar cargos adicionales.
- Desde “My Codespaces”, selecciona el Codespace y elige “delete” para confirmar la eliminación.

Este proceso garantiza que solo uses el tiempo necesario y no excedas el límite de la cuenta gratuita.

[🡡 volver al inicio](#tabla-de-contenido)

## GitHub Dev Editor

GitHub ha incorporado una herramienta que, aunque pasa desapercibida, puede hacer que editar archivos sea rápido y sencillo sin necesidad de un entorno completo como Codespaces. Este pequeño editor de código integrado en el navegador se activa al presionar Enter en la página de un repositorio, llevando al usuario a una experiencia muy similar a Visual Studio Code para ediciones rápidas y precisas.

### ¿Cómo funciona el GitHub Dev Editor?

El GitHub Dev Editor se activa al presionar Enter dentro de cualquier repositorio en GitHub. Esta acción abre un editor web donde puedes:

- Visualizar y editar archivos de texto de inmediato.
- Realizar cambios rápidos en archivos como README o en cualquier otro documento de texto dentro del repositorio.
- Guardar automáticamente los cambios al cerrar la pestaña o realizar un “commit” y “push” de forma directa.

Este editor no cuenta con terminal ni opciones avanzadas de desarrollo; está diseñado únicamente para realizar ediciones en texto.

### ¿Qué ventajas ofrece frente a otros entornos de desarrollo?

GitHub Dev Editor es ideal para tareas de edición de texto simples. Aquí algunos beneficios:

- Sin costo adicional: A diferencia de Codespaces, el uso del Dev Editor no genera cargos.
- Accesibilidad: Disponible en cualquier navegador, sin requerir configuraciones complejas.
- Rapidez: Acceso rápido para editar y confirmar cambios de inmediato, útil para pequeñas modificaciones o correcciones ortográficas.

### ¿Cuándo deberías utilizar Codespaces en lugar de GitHub Dev Editor?

El uso de Codespaces es recomendable cuando el proyecto requiere un entorno completo de desarrollo. Algunas de las principales razones para elegir Codespaces son:

- Compilación y ejecución: Codespaces permite compilar y probar código, algo que no es posible en el Dev Editor.
- Terminal y depuración: Incluye terminal y herramientas avanzadas para ejecutar comandos, ideal para proyectos complejos.
- Colaboración avanzada: Permite trabajar con equipos en un entorno en la nube, manteniendo sincronización en tiempo real.

Sin embargo, hay un costo asociado a su uso cuando se superan las horas gratuitas mensuales, por lo que es importante considerar esta opción solo cuando el proyecto lo requiera.

### ¿Qué debes considerar al escoger entre GitHub Dev Editor y Codespaces?

- Frecuencia y tipo de cambios: Si solo necesitas editar unas pocas líneas, GitHub Dev Editor es suficiente.
- Costo: Codespaces tiene un costo en la nube, mientras que el Dev Editor es gratuito.
- Necesidades de desarrollo: Para compilaciones y pruebas de código, Codespaces es indispensable; para correcciones menores, el Dev Editor es más práctico.

[🡡 volver al inicio](#tabla-de-contenido)

## Cómo Usar Tokens en GitHub para Acceso Seguro a Repositorios Privados

Para quienes buscan facilitar el trabajo colaborativo sin comprometer la seguridad de su repositorio privado, GitHub ofrece una solución eficaz a través de los tokens de acceso personal (PAT, por sus siglas en inglés). Estas llaves temporales otorgan acceso controlado a usuarios o aplicaciones, asegurando que solo puedan realizar acciones específicas y por el tiempo necesario. En este artículo, exploramos cómo crear y gestionar tokens en GitHub para maximizar la seguridad y funcionalidad en distintos entornos.

### ¿Cómo invitar a otros sin hacerlos colaboradores permanentes?

- Escenarios comunes: Cuando deseas que alguien contribuya de forma temporal, pero sin añadirlo como colaborador permanente.
- Solución con tokens: En lugar de agregarlo como colaborador, puedes crear un token con permisos limitados para que acceda al repositorio solo en el tiempo y con las acciones necesarias.

### ¿Qué tipos de tokens existen en GitHub?

GitHub ofrece dos tipos de tokens:

1. Tokens Clásicos: Permiten seleccionar permisos básicos y pueden tener duración indefinida (aunque no es recomendable).
2. Tokens Detallados: Versiones más nuevas que permiten control granular y una duración máxima de 90 días. Ideal para asegurar un acceso mucho más restringido.

### ¿Cómo se crea un token clásico?

1. Acceso a Configuración: Ve a “Settings” en tu perfil y selecciona “Developer Settings”.
2. Generar Token: Elige “Generate New Token” y configura:

   - Nombre: Ayuda a identificar el propósito del token.
   - Expiración: Ajusta a la duración esperada del proyecto.
   - Permisos: Elige los accesos que consideres necesarios (repos, paquetes, notificaciones, etc.).

3. Guardar Token: Copia el token en un lugar seguro, ya que no será visible nuevamente después de cerrar la página.

### ¿Cómo funcionan los tokens detallados?

A diferencia de los tokens clásicos, los detallados permiten:

- Duración Máxima de 90 Días: Ofrece seguridad adicional al limitar el tiempo de acceso.
- Control de Repositorio Específico: Puedes configurar que el token tenga acceso solo a repositorios específicos, incluso privados o públicos.
- Permisos Granulares: Permiten ajustar más a detalle el alcance y las acciones que el token puede realizar.

### ¿Cómo utilizar el token en un entorno externo?

Al clonar un repositorio en un equipo sin credenciales de GitHub, el sistema pedirá el nombre de usuario y, en lugar de la contraseña de la cuenta, el token de acceso personal. Al ingresar el token en la terminal, podrás acceder al repositorio de forma segura, replicando el proceso de clonación estándar sin exponer tus credenciales personales.

### ¿Para qué otras tareas se pueden utilizar los tokens?

Los tokens no solo sirven para acceder desde equipos remotos; su funcionalidad se extiende a:

- Automatización con GitHub Actions: Automatiza flujos de trabajo en tu repositorio.
- Scripts Personalizados: Ideal para automatizar tareas repetitivas como commits periódicos o sincronización de proyectos.
- Integración con Terceros: Configura accesos específicos para aplicaciones que interactúan con tu repositorio.

### ¿Qué medidas de seguridad deben tomarse con los tokens?

- Configurar expiración: Limita la duración del token según las necesidades.
- Reducir permisos: Otorga solo los permisos mínimos necesarios.
- Revisión y eliminación: Revisa periódicamente los tokens en uso y elimina aquellos que ya no sean necesarios para evitar riesgos de acceso no autorizado.

[🡡 volver al inicio](#tabla-de-contenido)

## Gestión de Dependencias y Seguridad con Dependabot en GitHub

La gestión de dependencias es esencial para mantener la seguridad y estabilidad de las aplicaciones. Dependabot es una herramienta eficaz que, al integrarse en el flujo de trabajo, identifica y soluciona problemas en las versiones de paquetes de terceros, minimizando vulnerabilidades. Aquí exploramos cómo configurar y aprovechar al máximo Dependabot.

### ¿Por qué es importante mantener actualizados los paquetes de terceros?

Los paquetes de terceros son un recurso común en el desarrollo para simplificar tareas como la lectura de archivos JSON o la creación de APIs. Sin embargo, estas dependencias pueden convertirse en un riesgo si no se actualizan, ya que las versiones desactualizadas pueden contener vulnerabilidades que comprometan la seguridad de la aplicación.

### ¿Cómo activar Dependabot en un repositorio?

Para activar Dependabot:

1. Accede a Settings o Security dentro del repositorio.
2. Ve a Code Security and Analysis y selecciona la categoría de Dependabot.
3. Activa las alertas de seguridad y actualizaciones de versión.
4. Dependabot generará un archivo dependabot.yml, donde puedes ajustar la frecuencia de las revisiones, como cambiar de semanal a diaria para detectar actualizaciones con mayor regularidad.

### ¿Cómo utilizar Dependabot para gestionar versiones específicas?

En el caso de proyectos .NET, se pueden elegir versiones específicas de paquetes:

1. Navega a la pestaña del paquete deseado (por ejemplo, Newtonsoft.Json).
2. Escoge una versión con vulnerabilidades conocidas (como 12.0.3 en este ejemplo) para ver cómo Dependabot detecta y notifica el problema.
3. Dependabot genera un pull request automáticamente para actualizar la versión del paquete y solucionar la vulnerabilidad detectada.

### ¿Qué sucede cuando Dependabot detecta una vulnerabilidad?

Cuando Dependabot encuentra una vulnerabilidad:

- Notifica con prioridad la versión insegura del paquete.
- Crea un pull request para actualizar el paquete a una versión segura.
- Permite revisar y aceptar la actualización directamente desde la sección de Security o en Pull Requests.

Dependabot analiza la compatibilidad de versiones para asegurar que la actualización sea estable y, en algunos casos, puede incluso eliminar la rama creada una vez fusionada la actualización.

### ¿Por qué integrar Dependabot en el flujo de trabajo?

Dependabot simplifica la gestión de actualizaciones:

- Detecta y repara vulnerabilidades sin intervención manual.
- Mantiene el proyecto actualizado con las versiones estables más recientes de cada dependencia.
- Agiliza la revisión y aplicación de actualizaciones, evitando que el equipo trabaje con versiones obsoletas.

[🡡 volver al inicio](#tabla-de-contenido)

## Gestión de datos sensibles y políticas de seguridad

Al configurar un proyecto en GitHub, es crucial proteger la información sensible, como llaves de API o datos de conexión, evitando que sean subidas por error al repositorio. Aunque el uso de archivos como .gitignore es clave para excluir información sensible, existen herramientas adicionales en GitHub para detectar y mitigar estos riesgos. Aquí te explico cómo activar y aprovechar al máximo CodeQL y Secret Scanning para mejorar la seguridad de tu código en repositorios públicos.

### ¿Cómo activar CodeQL y Secret Scanning en GitHub?

Para comenzar, es necesario hacer el repositorio público, ya que algunas de estas funciones no están disponibles en repositorios privados. Sigue estos pasos para activar la seguridad de tu código:

1. Ve a Settings en el repositorio y desplázate a Code Security and Analysis.
2. Activa CodeQL Analysis en la sección de Code Scanning. GitHub detectará el lenguaje de tu proyecto y comenzará a analizar el código en segundo plano.
3. Luego, asegúrate de que Secret Scanning esté habilitado. Esta función, que viene activada por defecto, detecta automáticamente secretos o llaves sensibles en el código.

### ¿Cómo probar si Secret Scanning detecta información sensible?

Para verificar el funcionamiento de Secret Scanning, puedes añadir intencionadamente una clave sensible en el código. Por ejemplo:

- Agrega una cadena como string stripeApiKey = "clave_sensible"; en tu archivo de código y sube el cambio.
- GitHub realizará el análisis en segundo plano y, si detecta una llave API, emitirá una alerta en la sección de Security.

En cambio, una cadena menos evidente, como string connectionString = "cadena_sensible";, podría pasar desapercibida. Este ejemplo muestra que, aunque Secret Scanning es útil, no es infalible y puede omitir cadenas sensibles si no siguen patrones comunes.

### ¿Qué hacer si GitHub detecta una alerta de seguridad?

Si GitHub te notifica sobre una alerta de secreto en el código, sigue estos pasos para mitigar el riesgo:

- Renueva las credenciales en la cuenta del servicio de terceros para evitar accesos no autorizados.
- Elimina la clave del historial de commits, ya que eliminarla solo del código actual no la quita de versiones anteriores.
- Modifica tu código para utilizar archivos de configuración, como .env o appsettings.json, y exclúyelos con .gitignore para evitar futuras filtraciones.

### ¿Por qué CodeQL y Secret Scanning no son suficientes?

Aunque GitHub ofrece herramientas poderosas de análisis, no garantizan la detección de todas las cadenas sensibles. Por eso, la mejor práctica sigue siendo prevenir las filtraciones configurando correctamente .gitignore y almacenando secretos en archivos de entorno.

Estas prácticas te ayudarán a evitar el riesgo de exponer información crítica, reduciendo los problemas de seguridad y permitiéndote mantener un código limpio y seguro.

[🡡 volver al inicio](#tabla-de-contenido)

## GitHub Actions

Optimizar tu perfil de GitHub puede marcar una gran diferencia al mostrar tus habilidades y actividad de desarrollo, y GitHub Actions es la herramienta ideal para automatizar tareas que mantengan tu perfil siempre actualizado. A continuación, te explicamos cómo crear una GitHub Action que muestre tu actividad reciente directamente en tu portada de perfil.

### ¿Qué es GitHub Actions y cómo puede ayudarte?

GitHub Actions permite automatizar diversos flujos de trabajo, desde revisiones de seguridad con Dependabot hasta integraciones continuas y despliegues (CI/CD). Con una GitHub Action, puedes extraer automáticamente tu actividad más reciente y mostrarla en tu perfil. Esto ayuda a que otros vean tu progreso y compromiso en tus repositorios.

### ¿Cómo configurar tu repositorio de portada en GitHub?

1. Selecciona tu repositorio de perfil: Este suele llevar el nombre de usuario como nombre de repositorio.
2. Edita el README: Abre el archivo README.md en modo edición y asegúrate de contar con una sección específica para la actividad reciente.
3. Agrega un título personalizable: Por ejemplo, “Actividad reciente” o “Últimos commits”, para que la sección tenga un toque personal.

### ¿Cómo crear una GitHub Action para actualizar tu actividad?

1. Accede a la sección de Actions en el repositorio de tu perfil.
2. Elige una plantilla básica para crear un flujo de trabajo simple.
3. Configura el archivo YAML:
   - Ubicación: Guarda el archivo como .github/workflows/update-readme.yml.
   - Cron Job: Programa la frecuencia de actualización. Un formato común es `*/12 * * * *` para actualizar cada 12 horas.
   - Paso de checkout: Este paso accede a tus archivos.
   - Recent Activity Workflow: Incluye el paso para extraer tu actividad reciente desde un flujo preconstruido disponible en el Marketplace de GitHub Actions.

### ¿Cómo asegurarte de que tu GitHub Action funcione correctamente?

1. Guarda y ejecuta la acción: Haz un commit directo en la rama principal.
2. Verifica el estado: Si ocurre algún error, GitHub Actions lo destacará en rojo, señalando el paso problemático.
3. Ajustes finales: Corrige cualquier error en el archivo YAML o en los comentarios del README, y vuelve a ejecutar el flujo de trabajo.

### ¿Qué opciones adicionales puedes explorar en GitHub Actions?

- Marketplace: Encuentra acciones preconfiguradas para desplegar en Docker, compilar aplicaciones en Java, entre otras.
- Variables de ambiente: Usa GITHUB_TOKEN para autenticar la Action y mantenerla segura.
- Contenido personalizado: Puedes agregar secciones adicionales en tu perfil, como listas de videos de YouTube o portafolios enlazados.

### ¿Cómo hacer que tu perfil destaque con otras personalizaciones?

GitHub Actions ofrece un sinfín de posibilidades para personalizar tu perfil y mostrar contenido relevante. Explora perfiles inspiradores en los recursos de esta clase, descarga archivos YAML, y pruébalos en tu repositorio para continuar optimizando tu presencia profesional.

[🡡 volver al inicio](#tabla-de-contenido)

## Introducción a los GitHub Releases

### ¿Qué son los GitHub Releases?

Los GitHub Releases son una forma de empaquetar y distribuir versiones específicas de tu software directamente desde un repositorio de GitHub. Se utilizan para gestionar el ciclo de vida del proyecto y permitir a los usuarios descargar versiones estables del código.

### ¿Para qué sirven?

- Marcar versiones estables de un proyecto con etiquetas (tags).
- Distribuir binarios o archivos ejecutables junto con el código fuente.
- Documentar cambios con notas de versión (release notes).
- Automatizar despliegues en CI/CD.

### Diferencia entre Tags y Releases

- Tags: Son marcas en el historial de Git que identifican un estado específico del repositorio.
- Releases: Son versiones creadas a partir de un tag, con notas, archivos adjuntos y documentación adicional.

### Cómo crear un GitHub Release

- Opción 1: Desde la interfaz web de GitHub

  1. Ve a la pestaña Releases en tu repositorio.
  2. Haz clic en "Draft a new release".
  3. Selecciona o crea un Tag (Ejemplo: v1.0.0).
  4. Escribe las notas de la versión.
  5. (Opcional) Adjunta binarios o archivos.
  6. Haz clic en "Publish release".

- Opción 2: Usando Git CLI

  - Crear un tag en Git git tag -a v1.0.0 -m "Primera versión estable"
  - Subir el tag al repositorio git push origin v1.0.0

  Luego puedes convertir este tag en un Release desde la interfaz de GitHub.

- Opción 3: Usando GitHub CLI

      gh release create v1.0.0 --title "Versión 1.0.0" --notes "Descripción de cambios en esta versión."

### Casos de Uso Comunes

- Publicación de librerías y frameworks en GitHub.
- Distribución de binarios o archivos ejecutables.
- Gestión de versiones semánticas (v1.0.0, v1.1.0, v2.0.0).
- Integración con GitHub Actions para despliegues automáticos.

Conclusión: GitHub Releases es una herramienta poderosa para gestionar versiones de software, mantener documentación clara y distribuir binarios de manera profesional.

[🡡 volver al inicio](#tabla-de-contenido)
