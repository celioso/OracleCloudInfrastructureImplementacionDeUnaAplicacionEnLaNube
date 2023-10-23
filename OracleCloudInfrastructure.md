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

### Haga lo que hicimos: infraestructura a partir del código

Realizamos la creación de nuestra primera infraestructura a partir del código utilizando el gerenciador de recursos de OCI.

Inicialmente fue necesario remover los recursos ya utilizados para no ultrapasar los límites de uso de la cuenta free tier.

Realizamos la remoción del balanceador de cargas, de las dos instancias de computación y de la red virtual.

En seguida pudimos implementar nuestra primera infraestructura como código como el archivo “[orm-dps.zip](https://github.com/alura-es-cursos/1911-OCI2-doguito-site-orm/archive/refs/heads/master.zip "orm-dps.zip")”, que tiene una infraestructura básica de balanceador de carga, red virtual y dos instancias.

Sigue los pasos realizados en el video para implementar la infraestructura como código y si tienes problemas, acciona el fóro del curso para obtener auxilio.

### Para saber más: automatizando la infraestructura

La infraestructura necesaria para la ejecución de nuestras aplicaciones se han tornado cada vez más complejas. Además de eso, también tenemos el concepto de infraestructura elástica, que consiste en adecuar nuestra infraestructura implementada al volumen de trabajo de un determinado momento. Para eso, surgió la necesidad de automatización de implementación, que debe dejar de ser un proceso manual para ser un proceso automático y reproducible.

Como hemos visto, Resource Manager de OCI es nuestro aliado en esta tarea, y este video nos trae muchas informaciones complementares para profundizarnos nuestro conocimiento sobre Resource Manager:

[OCI Level 100 - Resource Manager](https://www.youtube.com/watch?v=btnRgK36LnE "OCI Level 100 - Resource Manager")

El contenido en video puede presentar algunos tópicos desactualizados, por eso, todos los detalles sobre la utilización de Resource Manager en OCI pueden ser encontrados en la documentación oficial a través del link:

[Documentación de Oracle Cloud Infrastructure](https://docs.oracle.com/es-ww/iaas/Content/home.htm "Documentación de Oracle Cloud Infrastructure")

### Lo que aprendimos

Lo que aprendimos en esta aula:

- Que las aplicaciones han evolucionado su arquitectura de construcción de monolitos para microservicios.
- Que la utilización de microservicios acelera la necesidad de trabajarse con automatización de aprovisionamiento de infraestructura y infraestructura como código.
- Que la OCI disponibiliza diversas soluciones de soporte al desarrollo a través de la opción “Servicios al Desarrollador”, por ejemplo: Kubernets, Registro de Artefactos, Gateway de API y Gerenciamiento de Recursos (IaaS)
- Que el Gerenciador de Recursos es un servicio de Terraform y permite la definición de infraestructura como código, colaborando para que la infraestructura pueda ser fácilmente replicada y versionada.

### Haga lo que hicimos: Doguito como código

¿Estás listo para crear un pilla customizada para implementar Doguito de manera extremadamente simple y práctica?

Serán necesarios algunos pasos:

- Ajustar el archivo “compute.tf” customizando el nombre de las instancias;
- Ajustar el archivo loadbalancer.tf customizando el nombre del balanceador de cargas y las puertas de conexión;
- Ajustar el archivo “network.tf” incluyendo una regla de ingreso para la puerta 3000;
- Crear un nuevo bucket llamado internal y hacer el upload de los archivos “doguito-site.service” y “Wallet_DOGUITODB.zip”;
- Alterar el “archivo cloud-init.yaml” instalando git, Node.js y los drivers de conexión con la base de datos ORacle. Inserir un comando en el archivo para hacer la descarga y configurar el service de Doguito, además de hacer la descarga de Wallet y la descompactar en el local adecuado, liberando la puerta 3000 en firewall.
Por fin, tenemos que compactar otra vez el archivo “[orm-dps-vm2](https://github.com/alura-es-cursos/1911-OCI2-doguito-site-orm2/archive/refs/heads/master.zip "orm-dps-vm2")” en un archivo zip que será utilizado para inicializar la pilla del Doguito.

Si tienes alguna pregunta, no dudes en entrar en contacto con otras personas en nuestro fóro.

### Haga lo que hicimos: implementando Doguito como código

Tenemos el archivo “orm-dps-v2.zip” y ahora es hora de implementarlo como una pilla en OCI. Para eso utilizamos la opción de Servicios al Desarrollador y Gerenciador de Recursos.

El proceso será muy semejante al que hicimos anteriormente, pero utilizaremos el archivo “[orm-dps-v2.zip](https://github.com/alura-es-cursos/1911-OCI2-doguito-site-orm2/archive/refs/heads/master.zip "orm-dps-v2.zip")” que acabamos de generar para subir una pila customizada para Doguito.

Espero que salga todo bien y que tu pilla sea implementada con éxito, pero si tienes algún problema, puedes conversar con los demás colegas en el foro.

### Para saber más: automatizando la infraestructura

En este entrenamiento nuestro enfoque es en el aprendizaje de utilización de Oracle Cloud para casos prácticos, entretanto, debes haber visto que hablamos sobre varias herramientas auxiliares que podemos utilizar para trabajar en una Cloud.

Resource Manager de OCI es una de estas herramientas y que internamente utiliza scripts TerraForm para automatizar la implementación de infraestructura.

Si te interesaste por Terraform y quieres saber más sobre, te dejamos un artículo que tenemos en nuestro blog [aquí](https://www.aluracursos.com/blog/conociendo-terraform?utm_source=gnarus&utm_medium=timeline "aquí").

### Lo que aprendimos

Lo que aprendimos en esta aula:

- Que podemos customizar los archivos Terraform para crear diversos tipos de recursos computacionales de una pilla de plementación.
- Que utilizamos el archivo cloud-init.yaml para customizar la instalación de softwares diversos en las instancias computacionales creadas a partir de una pilla.
- Que usamos el Almacenamiento de Objetos para guardar archivos de configuración que serán utilizados en la implementación de nuestras pillas de recursos.