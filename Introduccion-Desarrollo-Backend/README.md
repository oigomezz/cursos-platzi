# Curso de Introducción al Desarrollo Backend <!-- omit in toc -->

## Los roles del desarrollo backend

Tu rol principal como Backend Developer va ser escribir código que tengan que ver con:

- Reglas de negocio
- Validación
- Autorización de usuarios
- Conexiones a bases de datos
- Código que correra del lado del servidor.

El Backend developer también puede estár acercado a otro tipo de roles como:

- **DB ADMIN**: Gestiona una base de datos, sus políticas y como vamos a disponer de esa DB a través del código y la seguridad que estas deberian tener.

- **SERVER ADMIN**: Se encarga de gestionar la seguridad en los servidores que es donde corre el código a disposición.

## Frontend, Backend y Full Stack

- **Fronted (Cliente):** Se enfoca en la parte del renderizado y lo que se muestra al cliente. Clientes mas populares:

  - Navegadores: hacen solicitudes HTML o pueden enviar datos y soportan;
    - HTML; Markdown
    - CS; Tailwind, Bootstrap, Foundation
    - JS; React, Angular , Vue
  - APP mobile: Pueden ser de android o iOS, q se conectan a un servicio de backend para solicitar datos y luego renderizarlo. Soportan:
    - IOS; Swift, Objetive C.
    - Android; Kotlin, JAVA
    - Cross Plataform; React Native, Flutter, .NET MAUI
  - IOT: Podemos conectar dispositivos que envíen datos a un SV para luego visualizarlo

- **Backend (Server):** Se enfoca en desarrollar servicios que se conectan a un frontend o sea un cliente a través de una API (application programming interface). Existen múltiples lenguajes de programación con su respectivo framework que se utilizan para el desarrollo backend;

  - Python → Django
  - JavaScript → Express.js
  - TypeScript → NestJS
  - Ruby → Ruby on Rails
  - PHP → Laravel
  - Java → Spring
  - Go → Gin
  - C# → .NET

- **FullStack**: Es un dev que desempeña funciones de frontend y backend, pero generalmente tiene una especialidad en la que ejerce una mayor profundidad de conocimiento.

## HTTP

La URL de una pagina se compone de:

- https → Protocolo La S al final de HTTPS significa security, y es un certificado de seguridad.
- platzi .com → Dominio El navegador realiza una petición con un dominio, y el sistema DNS se encarga de resolver dicho dominio para indicarle al navegador dónde encontrar el servidor solicitado.
- cursos → Path / endpoint

Como el usuario hace una petición que llega al SV

- El usuario ingresa al navegador o app y hace una solicitud que envía una REQUEST → esa request sale con un dominio → El sistema DNS se encarga de encontrar el SV → la request llega al SV
- El servidor envía un RESPONSE a la petición del navegador, esta respuesta puede realizarse en varios formatos:
  - Frontend; Renderizando la página con HTML, CSS y JavaScript
  - Datos; También puede enviar datos puros con XML O JSON

El protocolo HTTP proporciona códigos de estado, que es información útil para que el solicitante de la petición responda y se comporte de acuerdo a las necesidades.

Rango del status code:

- 1XX = INFO.
  - 102 = PROCESSING
- 2XX = SUCCESS (éxito)
  - 200 = OK
  - 201 = CREATED
  - 204 = NO CONTENT
- 3XX = REDIRECT
  -301 = MOVED
  -307 = TEMPORARY
  -308 = PERMANENT
- 4XX = CLIENT ERROR (frontend).
  - 401 = CLIENT ERROR
  - 404 = NOT FOUND
  - 409 = CONFLICT
- 5XX = SERVER ERROR (backend).
  - 500 = INTERNAL
  - 502 = BAD GETEWAY
  - 504 = GETEWAY TIMEOUT

Los códigos de estado brindan información útil para entender el comportamiento de la petición que se le hace al servidor.

## API

Las APIs (Interfaz de Programación de Aplicaciones) son conjuntos de protocolos y herramientas que permiten a diferentes aplicaciones comunicarse entre sí. Facilitan el intercambio de datos y funcionalidades, permitiendo que los desarrolladores integren servicios externos en sus aplicaciones, mejorando la funcionalidad y la experiencia del usuario.

### Estructura REST API

**REST** (Representational State Transfer) API es un estilo de arquitectura de software que se utiliza para construir servicios web. Una API REST es una interface que se utiliza para interconectar sistemas o aplicaciones, y permite que estos sistemas o aplicaciones envíen y reciban datos entre sí a través de la red.

Una API REST se basa en el protocolo HTTP, y utiliza operaciones HTTP como GET, POST, PUT y DELETE para realizar diversas acciones sobre los datos almacenados en un servidor. Estas operaciones son conocidas como métodos HTTP, y corresponden a las acciones CRUD (Create, Read, Update, Delete) que se pueden realizar sobre los datos.

Una API REST se utiliza a menudo para construir servicios web que pueden ser utilizados por diversas aplicaciones o sistemas, y es una forma común de permitir la integración entre diferentes sistemas y plataformas.

A través de los endpoints se le pide información al dominio, por lo general se nos devuelve la información empaquetada en un JSON.

#### Como funciona?

- CRUD es el índice de unas palabras clave, y en el protocolo HTTP tenemos métodos para llevarlas a cabo:
  - Create (crear) → POST
  - Read (leer) → GET
  - Delete (eliminar) → DELETE
  - Update (actualizar) → PUT / PATCH
    - PUT envía la totalidad de los datos, mientras que patch envía solo los datos destinados a actualizarse

| EndPoint             | Method | Body  | Response      | status |
| -------------------- | ------ | ----- | ------------- | ------ |
| /products            | GET    | N/A   | [{}, {}, ...] | 200    |
| /products/:id        | GET    | N/A   | {}            | 200    |
| /products/categories | GET    | N/A   | [{}, {}, ...] | 200    |
| /products            | POST   | {...} | {...}         | 201    |
| /products/:id        | PUT    | { }   | { }           | 201    |
| /products/:id        | PATCH  | { }   | { }           | 201    |
| /products/:id        | DELETE | N/A   | true / false  | 201    |

## Nube | Cloud

La computación en la nube, se refiere a la entrega de servicios informáticos a través de Internet, incluyendo almacenamiento, procesamiento y gestión de datos. En lugar de utilizar hardware y servidores locales, las organizaciones pueden acceder a recursos y aplicaciones a través de proveedores de servicios en la nube, lo que permite una mayor flexibilidad, escalabilidad y ahorro de costos. Los servicios en la nube se dividen comúnmente en tres categorías principales:

- IaaS (Infraestructura como Servicio)
- PaaS (Plataforma como Servicio)
- SaaS (Software como Servicio).

Esta tecnología permite a las empresas y desarrolladores concentrarse en la innovación y el desarrollo de sus aplicaciones sin preocuparse por la infraestructura subyacente, facilitando el acceso a potentes capacidades informáticas bajo demanda y mejorando la eficiencia operativa.

## DevOps

DevOps es un enfoque de colaboración y comunicación que fomenta la integración continua y la entrega continua de software. Se basa en la idea de que las áreas de desarrollo y operaciones deben trabajar juntas para lograr la entrega rápida y constante de software de alta calidad.

El objetivo de DevOps es mejorar la eficiencia y la efectividad de los procesos de desarrollo y entrega de software, reduciendo los tiempos de inactividad y los errores durante el proceso de implementación. Esto se logra a través de la automatización de tareas y procesos, la mejora continua de la calidad del software y la colaboración cercana entre desarrolladores y operadores.

DevOps también incluye la adopción de prácticas y herramientas de ciclo de vida de software, como integración continua y entrega continua, para mejorar la eficiencia y la efectividad de los procesos de desarrollo y entrega de software.

**SaaS** (Software as a Service) es un modelo de distribución de software en el que el proveedor ofrece el software como un servicio a través de internet. Los usuarios acceden al software a través de un navegador web o a través de una aplicación cliente y no tienen que preocuparse por la instalación ni por la actualización del software. Ejemplos de SaaS son servicios como Gmail, Slack y Google Drive.

**PaaS** (Platform as a Service) es un modelo de distribución de software en el que el proveedor ofrece una plataforma en la que los usuarios pueden desarrollar, probar, implementar y administrar aplicaciones sin tener que preocuparse por la infraestructura subyacente. Ejemplos de PaaS son servicios como AWS Elastic Beanstalk y Google Firebase.

**IaaS** (Infrastructure as a Service) es un modelo de distribución de infraestructura informática en el que el proveedor ofrece recursos informáticos, como servidores, almacenamiento y redes, como un servicio a través de internet. Los usuarios acceden a estos recursos a través de una interfaz en línea y pueden utilizarlos para desplegar y ejecutar aplicaciones y servicios sin tener que preocuparse por la adquisición ni por el mantenimiento de la infraestructura física. Ejemplos de IaaS son servicios como AWS EC2 y DigitalOcean.

## Cookies y sesiones

Las cookies son pequeños fragmentos de texto que los sitios web que visitas envían al navegador. Permiten que los sitios web recuerden información sobre tu visita, lo que puede hacer que sea más fácil volver a visitar los sitios y hacer que estos te resulten más útiles. Otras tecnologías, como los identificadores únicos que se usan para identificar un navegador, aplicación o dispositivo, los píxeles y el almacenamiento local, también se pueden usar para estos fines. Las cookies y otras tecnologías que se describen en esta página pueden usarse para los fines indicados más abajo.

### Funcionalidad

Las cookies y otras tecnologías que se usan con fines de funcionalidad te permiten acceder a funciones esenciales de un servicio. Se consideran esenciales, por ejemplo, las preferencias, (como el idioma que has elegido), la información relacionada con la sesión (como el contenido de un carrito de la compra), y las optimizaciones de los productos que ayudan a mantener y mejorar ese servicio.

Algunas cookies y otras tecnologías se utilizan para recordar tus preferencias. Por ejemplo, la mayoría de las personas que usan los servicios de Google tienen en sus navegadores una cookie denominada "NID" o "ENID", dependiendo de sus opciones de cookies. Estas cookies se usan para recordar tus preferencias y otra información, como el idioma que prefieres, el número de resultados que quieres que se muestren en cada página de resultados de búsqueda (por ejemplo, 10 o 20) y si quieres que el filtro Búsqueda Segura de Google esté activado o desactivado. La cookie "NID" caduca 6 meses después del último uso del usuario, mientras que la cookie "ENID" dura 13 meses. Las cookies "VISITOR_INFO1_LIVE" y "YEC" tienen un propósito similar en YouTube y también se usan para detectar y resolver problemas con el servicio. Estas cookies tienen una duración de 6 y 13 meses, respectivamente.

Otras cookies y tecnologías se usan para mantener y mejorar tu experiencia durante una sesión concreta. Por ejemplo, YouTube utiliza la cookie "PREF" para almacenar información como la configuración que prefieres para tus páginas y tus preferencias de reproducción; por ejemplo, las opciones de reproducción automática que has seleccionado, la reproducción aleatoria de contenido y el tamaño del reproductor. En YouTube Music, estas preferencias incluyen el volumen, el modo de repetición y la reproducción automática. Esta cookie caduca 8 meses después del último uso del usuario. La cookie "pm_sess" también ayuda a conservar tu sesión del navegador y tiene una duración de 30 minutos.

También se pueden usar cookies y otras tecnologías para mejorar el rendimiento de los servicios de Google. Por ejemplo, la cookie "CGIC" mejora la generación de resultados de búsqueda autocompletando las consultas de búsqueda basándose en lo que introduce inicialmente un usuario. Esta cookie tiene una duración de 6 meses.

Google usa la cookie "CONSENT", que tiene una duración de 2 años, para almacenar el estado de un usuario respecto a sus elecciones de cookies. La cookie "SOCS", que dura 13 meses, también se usa con este mismo fin.

### Seguridad

Las cookies y otras tecnologías que se usan con fines de seguridad ayudan a autenticar a los usuarios, prevenir el fraude y protegerte cuando interactúas con un servicio.

Las cookies y otras tecnologías que se usan para autenticar a los usuarios permiten asegurar que solo el propietario de una cuenta puede acceder a ella. Por ejemplo, las cookies "SID" y "HSID" contienen registros cifrados y firmados de forma digital del ID de cuenta de Google de un usuario y del momento de inicio de sesión más reciente. La combinación de estas cookies permite a Google bloquear muchos tipos de ataques, como, por ejemplo, intentos de robo del contenido de los formularios que se envían en los servicios de Google.

Algunas cookies y otras tecnologías se usan para prevenir el spam, el fraude y los abusos. Por ejemplo, las cookies "pm_sess", "YSC" y "AEC" se encargan de comprobar que las solicitudes que se hacen durante una sesión de navegación proceden del usuario y no de otros sitios. Estas cookies evitan que sitios maliciosos actúen haciéndose pasar por el usuario sin su conocimiento. La cookie "pm_sess" tiene una duración de 30 minutos, y la cookie "AEC", de 6 meses. La cookie "YSC" dura toda una sesión de navegación del usuario.

### Analíticas

Las cookies y otras tecnologías que se usan con fines analíticos ayudan a recoger datos que permiten a los servicios entender cómo interactúas con un servicio en particular. Esta información se usa para mejorar el contenido de los servicios y sus funciones, y así ofrecerte una mejor experiencia.

Algunas cookies y otras tecnologías ayudan a los sitios y las aplicaciones a entender cómo interactúan los visitantes con sus servicios. Por ejemplo, Google Analytics utiliza un conjunto de cookies para recoger información y ofrecer estadísticas de uso de los sitios sin que Google identifique personalmente a cada visitante. La principal cookie que utiliza Google Analytics es "\_ga", que permite a los servicios distinguir a un visitante de otro y tiene una duración de 2 años. La utilizan todos los sitios en los que se implementa Google Analytics, incluidos los servicios de Google. Cada cookie "\_ga" es exclusiva de una propiedad específica, así que no se puede utilizar para rastrear a un usuario o navegador en sitios web no relacionados.

Los servicios de Google también usan las cookies "NID" y "ENID" en la Búsqueda de Google y "VISITOR_INFO1_LIVE" y "YEC" en YouTube con fines analíticos.

### Publicidad

Google utiliza cookies con fines publicitarios, como publicar y renderizar anuncios, personalizar anuncios (según la configuración de anuncios que tenga el usuario en myadcenter.google.com y adssettings.google.com/partnerads), limitar el número de veces que se muestra un anuncio a un usuario, ocultar anuncios que el usuario ha indicado que no quiere volver a ver y medir la eficacia de los anuncios.

La cookie "NID" se usa para mostrar anuncios de Google en los servicios de Google a usuarios que no tengan la sesión iniciada, mientras que las cookies "ANID" e "IDE" se utilizan para mostrar anuncios de Google en sitios que no son de Google. Si has habilitado los anuncios personalizados, la cookie "ANID" se utiliza para recordar este ajuste y tiene una duración de 13 meses en el Espacio Económico Europeo (EEE), Suiza y el Reino Unido, y 24 meses en los demás lugares. Si los has desactivado, la cookie "ANID" se usa para almacenar ese ajuste hasta el 2030. La cookie "NID" caduca 6 meses después del último uso del usuario. La cookie "IDE" tiene una duración de 13 meses en el Espacio Económico Europeo (EEE), Suiza y el Reino Unido, y de 24 meses en los demás lugares.

En función de tu configuración de anuncios, otros servicios de Google, como YouTube, también pueden usar con fines publicitarios estas y otras cookies y tecnologías, como la cookie "VISITOR_INFO1_LIVE".

Algunas cookies y otras tecnologías que se usan con fines publicitarios se destinan a usuarios que inician sesión para usar servicios de Google. Por ejemplo, la cookie "DSID" se utiliza para identificar a un usuario que tenga la sesión iniciada en sitios que no son de Google y para recordar si el usuario ha aceptado la personalización de anuncios. Tiene una duración de 2 semanas.

A través de la plataforma publicitaria de Google, las empresas pueden anunciarse en servicios de Google y en sitios que no son de Google. Algunas cookies sirven de apoyo a Google para mostrar anuncios en sitios de terceros y se establecen en el dominio del sitio web que visitas. Por ejemplo, la cookie "\_gads" permite a los sitios mostrar anuncios de Google. Las cookies que empiezan por "gac" proceden de Google Analytics y las utilizan los anunciantes para medir la actividad de usuario y el rendimiento de sus campañas publicitarias. Las cookies "\_gads" tienen una duración de 13 meses, mientras que las cookies "gac" duran 90 días.

Algunas cookies y otras tecnologías se utilizan para medir el rendimiento de los anuncios y las campañas, así como las tasas de conversión de los anuncios de Google en los sitios que visitas. Por ejemplo, las cookies que empiezan por "gcl" se usan principalmente para ayudar a los anunciantes a determinar cuántas veces los usuarios que hacen clic en sus anuncios acaban realizando una acción en su sitio (por ejemplo, una compra). Las cookies que se usan para medir tasas de conversión no se utilizan para personalizar anuncios. Las cookies "gcl" tienen una duración de 90 días.

## Bases de datos

Una base de datos es una herramienta para recopilar y organizar información. Las bases de datos pueden almacenar información sobre personas, productos, pedidos u otras cosas. Muchas bases de datos comienzan como una lista en una hoja de cálculo o en un programa de procesamiento de texto. . Existen dos tipos de bases de datos: Relacionales y No Relacionales.

### Relacionales (SQL)

Se caracterizan por ser creadas con tablas que relaciona los datos con otros. usa SQL (Structured Query Language) que es un lenguaje de computación para trabajar con conjuntos de datos y las relaciones entre ellos. . Las BD relacionales más populares son:

- MySQL
- PostgreSQL
- ORACLE
- Microsoft SQL Server

Al trabajar todos con SQL, los frameworks aprovechan para trabajar con ORMS Object-Relational Mapping, que es una forma de abstraer la conexión a estas bases de datos, utilizando la POO (Programación Orientada a Objetos.) .

### No Relacionales (No SQL)

Una base de datos no relacional es aquella que no usa el esquema tabular de filas y columnas que se encuentra en la mayoría de los sistemas de base de datos más tradicionales. en vez de SQL, usa un formato JSON o parecido. . Las BD no relacionales más populares son:

- MongoDB
- Cassandra (Apache)
- Couchbase

**CUIDADO CON LOS SERVICIOS DE BASES DE DATOS** Porque es donde está toda la información delicada de nuestros usuarios. Por medio de los drivers el backend se comunica con las bases de datos.

También es importante tener en cuenta que el desarrollador backend no es quien administra el mantenimiento de las bases de datos, no gestiona backups, sincronización, etc, ésto lo hace el DB Admin. Sino que éste construye la lógica para consumir éste servicio por medio de los drivers.

### Proveedores de DB Administration

Ofrecen servicios para administrar las bases de datos en diferentes bases de datos y éstos cobran de acuerdo al servicio y puede salir más economico que crear un equipo para administrar toda nuestras bases de datos. Algunos son:

- Heroku.
- Firebase
- Digital Ocean
- Mongo Atlas
- Couchbase Capella DBaaS

## Qué es el escalamiento?

### Escalamiento vertical

Es cuando tenemos un servidor y eventualmente el servidor empieza a colapsar, una forma de solucionar el problema es incrementar:

- CPU
- RAM
- Disk

- **Problemas:**
  - Costos.
  - Desescalar.
  - Disponibilidad -> Solucion, Escalamiento Horizontal

### Escalamiento horizontal

Soluciona el problema de la disponibilidad. Se tienen varias instancias del mismo servidor. Como se tienen distintos servidores ahora se necesita de un LOAD BALANCER

**LOAD BALANCER** -> Tiene conocimiento de nuestras instancias/servidores (al conjunto de servidores se denomina Clouster). Si un nodo(instancia) se cae, el load balancer se encarga de desviarla. Distribuye las peticiones.

Si tenemos la base de datos local en cada servidor va haber un problema dado que no se tienen sincronizados los datos de las distintas bases de datos de los servidores. SOLUCION Gestionar la base de datos fuera de estos servidores. Quizas como un servidor aparte que sirva como DB.

## Replicación

La replicación se refiere a la técnica de crear y mantener copias idénticas de ciertos componentes o sistemas de software, con el objetivo de mejorar la disponibilidad, la confiabilidad y el rendimiento de una aplicación. Esta técnica se utiliza para garantizar que un sistema siga funcionando incluso si uno de sus componentes falla o para distribuir la carga de trabajo entre varios servidores para mejorar la capacidad de respuesta.

- Soluciones a desincronización de base de datos.
  - Aislar base de datos a un servidor en particular. Se le hace escalamiento vertical solo a la base de datos para evitar un cuello de botella.
  - Se puede hacer escalamiento horizontal a la base de datos con su propio load balancer para solventar el problema de la disponibilidad.
    - Cada vez que se realice escritura en una de las bases de datos, se realiza una sincronización para que el cambio ocurra en todas las bases de datos. Esto es conocido como replicación.
- Normalmente el backend developer no se encarga de la parte de replicación y gestión de bases de datos, sino en la capa de los servidores y el escalamiento horizontal.

## Cache

Es una técnica de almacenamiento temporal de datos de alta velocidad que permite un acceso rápido a la información más frecuentemente solicitada. Al almacenar datos en una memoria más rápida y de acceso más eficiente que la fuente de datos original, el caché mejora significativamente el rendimiento del sistema y reduce la latencia. Los sistemas de caché pueden implementarse a varios niveles, incluyendo memoria caché en procesadores, caché de disco y caché distribuida en redes y aplicaciones web. En el contexto del desarrollo web, el caché se utiliza comúnmente para almacenar respuestas de consultas de bases de datos, resultados de cálculos frecuentes y contenido estático, reduciendo la carga en los servidores y mejorando la experiencia del usuario. Sin embargo, es crucial gestionar adecuadamente la invalidez y la coherencia del caché para asegurar que los usuarios reciban datos actualizados y precisos.

## Colas de tareas

Un sistema de colas en backend es una estructura de datos que almacena tareas pendientes para ser procesadas. Estas tareas pueden ser cualquier cosa, desde procesamiento de datos hasta envío de correos electrónicos o actualizaciones de bases de datos. El sistema de colas procesa las tareas en orden de llegada, lo que permite que el backend maneje varias tareas simultáneamente y mejora la escalabilidad y el rendimiento. También permite la retención de tareas en caso de fallas o interrupciones en el sistema.

### ¿Por qué se necesita un sistema de colas?

1. Manejo de alta concurrencia: Un sistema de colas permite manejar una gran cantidad de peticiones simultáneas al procesar varias tareas a la vez, lo que mejora el rendimiento y la escalabilidad del sistema.
2. Procesamiento asíncrono: Un sistema de colas permite que las tareas se procesen de manera asíncrona, lo que significa que el cliente puede recibir una respuesta inmediata mientras que la tarea se procesa en segundo plano.
3. Tolerancia a fallas: Un sistema de colas permite retener las tareas en caso de fallas en el sistema, lo que garantiza que las tareas se procesen una vez que el sistema vuelve a estar disponible.
4. Priorización de tareas: Un sistema de colas permite priorizar las tareas de acuerdo a la importancia o urgencia, lo que garantiza que las tareas críticas se procesen primero.
5. Desacoplamiento de procesos: Un sistema de colas permite desacoplar diferentes procesos en el sistema, lo que permite escalar cada proceso de manera independiente y mejora la flexibilidad del sistema.

## Renderizado

1. Server-Side Rendering: se renderiza el HTML del cliente totalmente en el lado servidor.
2. Client-Side Rendering: se renderiza la aplicación completamente en el navegador haciendo uso de Javascript y la gestión del DOM.
3. Rehydration: HÍBRIDO de las dos anteriores en el que se aprovecha el HTML y los datos renderizados desde el lado servidor, hidratándose con una aplicación javascript que se monta encima de esta. 4. Prerendering: Se renderiza la web en tiempo de construcción creando un artefacto que puede servirse de una manera totalmente estática.

## Server-Side Rendering

1. ¿En qué consiste el Server-Side Rendering (SSR)?
   Es un enfoque de renderizado en el que se procesa y genera completamente el HTML en el servidor, antes de enviarlo al navegador del cliente.

2. ¿Cómo se compara el Server-Side Rendering con el Client-Side Rendering (CSR)?
   El SSR, el HTML lo genera el servidor
   El CSR, la aplicación y el HTML se generan en el navegador del cliente utilizando JavaScript y el DOM.

3. ¿Qué es la técnica de Rehydration y en qué consiste?
   Es una técnica que combina características de SSR y CSR. En el Rehydration, se aprovecha el HTML y los datos renderizados desde el servidor, y luego se "hidrata" o complementa con una aplicación JavaScript que se ejecuta en el navegador.

4. ¿Qué es Prerendering y cómo funciona?
   El Prerendering es una técnica de renderizado web que implica generar y renderizar una página web completa en el servidor antes de que un usuario realice una solicitud. Esto significa que las páginas web se crean de antemano, y los resultados se almacenan en forma de archivos HTML estáticos que se pueden entregar de inmediato cuando se solicitan.

5. ¿Cuáles son las ventajas de utilizar Server-Side Rendering (SSR)?

   - Mejora el SEO (Motores de búsqueda)
   - Carga más rápida de la página
   - Mejora el rendimiento en dispositivos de baja potencia
   - Mayor compatibilidad
   - Mayor seguridad

6. ¿En qué situaciones es especialmente útil el Server-Side Rendering (SSR)? Cuando se requiere:

   - Una indexación SEO efectiva
   - Una carga rápida de la página
   - Rendimiento en dispositivos de baja potencia
   - Mayor seguridad en la manipulación de datos y autenticación.
