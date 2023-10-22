### Curso de Oracle Cloud Infrastructure: base de datos e infraestructura como código

### Haga lo que hicimos: prepara una base de datos para Doguito

Aprendimos sobre las opciones de base de datos presentes en OCI, incluyendo las diferencias de performance entre estas, y de nível de control.

En seguida creamos la base de datos autónoma JSON que guardará las informaciones de Doguito. Elegimos esta opción por ser una base de datos auto gerenciada por OCI y provenir una AIP de comunicación simple y amigable para los desarrolladores.

Llegó el momento de que practiques lo que aprendiste y crear una base de datos en OCI.

### Para saber más: base de datos Oracle
Oracle desarrolla una de las bases de datos más utilizadas en el medio corporativo del mundo. De esta forma, es de esperarse que Oracle Cloud dispone muchos tipos de recursos de bases de datos adecuados a las diversas necesidades de sus clientes. Este video detalla las características técnicas de cada una de las opciones de bases de datos de la Oracle Cloud y es recomendable asistir si ya eres un administrador de bases de datos o si tienes contacto más profundo con el área.

[Database Level 100 - Part 1 - Introduction to OCI Database Service](https://www.youtube.com/watch?v=F4-sxIsnbKI "Database Level 100 - Part 1 - Introduction to OCI Database Service")

El contenido en video puede presentar algunos tópicos desactualizados, por eso, todos los detalles sobre la utilización de Base de Datos en OCI pueden ser encontrados en la documentación oficial en la sección “Gerenciamento de Datos” a través del link:

[Documentación de Oracle Cloud Infrastructure](https://docs.oracle.com/es-ww/iaas/Content/home.htm "Documentación de Oracle Cloud Infrastructure")

### Para saber más: base de datos No Relacionales

Además de las soluciones tradicionales de bases de datos relacionales, también está disponible en OCI la Oracle Database API para MongoDB.

Con esta API, los desarrolladores pueden utilizar las herramientas y drivers de código abierto de MongoDB conectados a un Oracle Autonomous JSON Database manteniendo los beneficios de una base de datos autónoma juntamente con una API de base de datos No Relacionales.

Como la API es compatible con Mongo DB, frecuentemente, poca o ninguna alteración es necesaria en el código de las aplicaciones existentes, basta alterar la string de conexión.

La lista de lenguajes de programación recomendadas incluye C, C#, Go, Java, Node.js, Ruby, entre otras.

El paso a paso de como utilizar Oracle Database API para MongoDB encontrase disponible en este[ link](https://docs.oracle.com/en/cloud/paas/autonomous-database/adbsa/mongo-using-oracle-database-api-mongodb.html " link").

### Lo que aprendimos

Lo que aprendimos en esta aula:

- Cuales son los tipos de servicios de base de datos ofrecidos por OCI, entre ellos Autonomous Database para DataWarehouse, JSON y procesamiento de transacciones, Bare Metal, VM y Exadata, MySql, NoSQL entre otros. Cada opción de base de datos ofrecida por OCI tiene sus características peculiares en relación a performance, APIs de comunicación y automatización de tareas.
- Cómo crear un Autonomous JSON Database que será utilizado para almacenar datos de Doguito Petshop.
- Cómo insertar, excluir y alterar los datos de Autonomous JSON Database utilizando la interfaz web.

### Haga lo que hicimos: ejecutando la API de Doguito en OCI

Aprendimos cómo implementar una aplicación Node.JS en la infraestructura de OCI. Clonamos el repositorio de git de la aplicación en la instancia, en seguida instalamos Node.JS, drivers de base de datos y por fin liberamos firewall y la regla de entrada para que la aplicación fuera accesible.

Llegó la hora de que practiques lo que aprendiste y ejecutar la Doguito API en OCI. Para tener acceso a los códigos, puedes acceder al link del repositorio en [Github](https://github.com/alura-es-cursos/1911-OCI2-doguito-app "Github").

### Haga lo que hicimos: probando la API REST de Doguito

Probamos la API REST de Doguito utilizando un plugin de navegador. Existen varias opciones de plugins de navegadores, pero utilizamos Boomerang, que está disponible en los enlaces abajo:

- [Chrome](https://chrome.google.com/webstore/detail/boomerang-soap-rest-clien/eipdnjedkpcnlmmdfdkgfpljanehloah?hl=pt-BR "Chrome")
- [Edge](https://microsoftedge.microsoft.com/addons/detail/boomerang-soap-rest-c/bhmdjpobkcdcompmlhiigoidknlgghfo "Edge")

Si utilizas Firefox la única opción es [RESTClient](https://addons.mozilla.org/pt-BR/firefox/addon/restclient/ "RESTClient")

Pero vimos que la ejecución de Doguito es realizada de forma manual, lo que no es ideal una vez que si la instancia sea reiniciada o ocurrir algún problema, Doguito no será ejecutado otra vez. Para evitar este problema, convertimos Doguito en un servicio de Systemd.

Ahora es contigo, haga los ajustes recomendados y pruebe Doguito API con un cliente REST. Si tienes alguna dificultad, usa el fóro para conversar con otras personas sobre tus dudas.

### Para saber más: tecnologías del Doguito

Nuestra aplicación de ejemplo que será implementada en Oracle Cloud es desarrollada utilizando JavaScript, NodeJS y el framework Express. Para nuestro curso no será necesario conocimiento profundo de desarrollo de aplicaciones utilizando estas tecnologías, pues vamos a enfocarnos en la infraestructura de la implementación.

### Lo que aprendimos

Lo que aprendimos en esta aula:

- Que Doguito API es una aplicación que expone una API REST escrita en JavaScript utilizando framework Express.js y que es ejecutada por Node.js.
- Que es necesario instalar git para clonar nuestro proyecto para instancia, además de ser necesario instalar Node para ejecutar Doguito API y otros drivers de base de datos específicos de Oracle.
- Que hacemos la descarga de Wallet de la conexión de base de datos para que nuestra instancia pueda acceder al DOGUITOBD.
- Que podemos crear un servicio de systemd para que la aplicación de Doguito API inicie automáticamente con nuestra instancia.
- Que es necesario liberar el acceso a la puerta 3000 en firewall de la instancias y crear una regla de acceso en la lista de seguridad de red virtual para que podamos acceder al Doguito API.
- Que podemos utilizar un cliente REST como Boomerang para acceder nuestra API del Doguito.