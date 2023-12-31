# Oracle Cloud Infrastructure implementación de una aplicación en la nube

### Haga lo que hicimos

En esta clase conocimos las características básicas de la aplicación que implementaremos en la nube. Debido a que esta aplicación ya está desarrollada nos enfocaremos en la configuración de la infraestructura para poder ejecutarla y no en su codificación. El proyecto Doguito Petshop está escrita en Javascript y se compone de un frontend HTML y un backend que tendrá acceso a una base de datos que en conjunto nos permitirá tener una API a la cual nuestro frontend se comunique

Vimos también las características más importantes de la computación en la nube, sus ventajas, los tipos de servicio a los cuales tenemos acceso y una introducción a OCI - Oracle Cloud Infrastructure

### Para saber más: conceptos de Cloud

Cuando comenzamos a estudiar sobre el concepto de la nube nos encontramos con una serie de conceptos y siglas que al principio son extraños, sin embargo es importante comprenderlos para poder tener una visión amplia de cómo la nube se compone así como de sus principios. Para ayudarte en este camino tenemos un [artículo](https://www.aluracursos.com/blog/que-es-cloud-y-sus-principales-servicios "artículo") que resume muy bien estos conceptos relacionados con la nube.

### Lo que aprendimos

Lo que aprendimos en esta aula:

- Las principales ventajas de la computación en la nube, las cuales son: reducción de costos, mayor velocidad, escalabilidad, productividad, desempeño y como es más eficaz que implementar un data center propio.
- Los tipos de nube más comunes en el mercado son pública, privada e híbrida.
- Los servicios ofrecidos principalmente en las nubes son Iaas, Paas, SaaS y Serverless.
- Oracle Cloud está inicialmente más enfocada en infraestructura, sin embargo cuenta con varios servicios que atenderán las más diversas demandas.

### Para saber más: modo gratuito Free TIer

Si te interesa conocer todos los detalles sobre los límites de uso de la cuenta Free Tier, te recomendamos que vayas al siguiente [enlace](https://www.oracle.com/mx/cloud/free/ "enlace") donde encontrarás más información sobre el modo gratuito de Oracle Cloud, encontrarás una explicación más detallada sobre lo que puedes realizar con una cuenta Free Tier así como con una Free Trial.

### Haga lo que hicimos: creando cuenta en OCI

En el vídeo creamos una cuenta dentro de OCI en el Modo gratuito(Free Tier). Utilizaremos esta cuenta para poder realizar la implementación de nuestra aplicación Doguito Petshop de forma gratuita.

Ahora es tu oportunidad de practicar y garantizar que tienes tu cuenta lista para poder seguir con el siguiente video.

### Haga lo que hicimos: navegando en el Console de OCI

En el video navegamos por la plataforma de OCI y conocimos algunas secciones importantes, también, accedimos a Cloud Shell, la cual es una herramienta que iremos utilizando a lo largo del curso, te recomiendo que tomes tu tiempo para familiarizarte y así sacarle el mejor provecho a este curso

### Lo que aprendimos

Lo que aprendimos en esta aula:

- Podemos crear una cuenta Free Tier en OCI.
- Existen comandos en la consola de OCI que nos permitirán hacer uso de los servicios(computación, almacenamiento, redes, bases de datos) de OCI para poder implementar nuestra plataforma Doguito Petshop generando.
- Con la cuenta Free Tier podemos utilizar diversos recursos por tiempo ilimitado para poder conocerlos y probarlos sin ningún costo.
- La cuenta Free Tier es diferente del periodo Free Trial. Durante este periodo, podemos utilizar diversos recursos que no están incluidos en la cuenta Free Tier por 30 días o hasta llegar al uso de $300.

### Para saber más: infraestructura OCI

Oracle Cloud es un sistema con diversos conceptos comunes a otras nubes pero también algunos conceptos únicos. Para entender como la infraestructura de Oracle Cloud está dividida asiste el siguiente video. (El video fue realizado en el idioma inglés pero puedes activar los subtítulos en español)

[Getting Started with Oracle Cloud Infrastructure](https://www.youtube.com/watch?v=JBkT44FSf0o "Getting Started with Oracle Cloud Infrastructure")

El contenido del video puede tener algunos temas desactualizados, por eso todos los detalles sobre los conceptos básicos y la arquitectura de OCI pueden ser encontrados en la documentación oficial en el siguiente enlace.

[Documentación de Oracle Cloud Infrastructure](https://docs.oracle.com/es-ww/iaas/Content/GSG/Concepts/baremetalintro.htm "Documentación de Oracle Cloud Infrastructure")

### Para saber más: compartimientos a fondo

En nuestra clase anterior vimos los conceptos básicos de los compartimientos, sin embargo existen detalles técnicos avanzados que son útiles en casos de uso más complejos. El siguiente video da información más detallada (El video fue realizado en el idioma inglés pero puedes activar los subtítulos en español)

[   0:11 / 10:44  • Introduction   IAM Level 100 Part 3: Compartments](https://www.youtube.com/watch?v=VJD19vyu6lI "   0:11 / 10:44  • Introduction   IAM Level 100 Part 3: Compartments")

El contenido del video puede tener algunos temas desactualizados, por eso todos los detalles sobre la utilización de compartimientos dentro de OCI pueden ser encontrados en la documentación oficial en el siguiente enlace.

[Documentación de Oracle Cloud Infrastructure](https://docs.oracle.com/es-ww/iaas/Content/Identity/compartments/managingcompartments.htm "Documentación de Oracle Cloud Infrastructure")

### Haga lo que hicimos: creando compartimentos

Aprendimos cómo crear compartimentos, que tiene por objetivo promover el isolamiento de seguridad y control de acceso dentro de la nube. Esto se logra a través de un namespace lógico global, donde las políticas de seguridad pueden ser aplicadas. Por medio de la aplicación de políticas, podemos definir un nivel de acceso adecuado dependiendo de los parámetros definidos por la organización para el gerenciamiento de recursos.

De esta manera la creación de compartimentos será nuestra primera dentro de OCI antes de dar continuidad al proceso de implementación de nuestro proyecto.

### Haga lo que hicimos: creando usuarios

Vimos cómo crear nuevos usuarios dentro de ORacle Cloud para segregar el nivel de acceso a las diferentes funcionalidades de OCI

Al crear tu cuenta por primera vez tendrás acceso a un usuario con permisos de administrador raíz(root). Eso significa que tienes el control sobre toda la cuenta y sobre todos los recursos de OCI. Sin embargo, este usuario debe ser utilizado para gerenciar otros usuarios, grupos y políticas. Debemos crear un nuevo usuario que tenga permisos solamente para el compartimento que creamos anteriormente.

### Haga lo que hicimos: configurando Cloud Shell

En esta clase vimos que para que un usuario pueda acceder a Cloud Shell es necesario que tenga las políticas definidas adecuadamente. Para eso tenemos que acceder al área de Identidad y Seguridad de OCI y crear una política para permitir que usuarios del grupo puedan utilizar Cloud Shell.

En seguida debemos acceder a Cloud Shell como un usuario administrador para poder realizar la creación de las llaves SSh que utilizaremos para acceder a las instancias que crearemos después.
 se crea con:
 `ssh-keygen -b 2048 -t rsa -f <nombre-del-archivo>`

### Lo que aprendimos

Lo que aprendimos en esta aula:

- La arquitectura de OCI está compuesta por una serie de elementos como instancias de computación, almacenamiento, redes, bases de datos, políticas de identidad y seguridad, entre otros.
- Creamos usuarios, grupos y políticas dentro de OCU para controlar el acceso a funcionalidades.
- Vimos algunos comandos básicos para poder generar una llave RSA dentro de Cloud Shell, la cual nos permite realizar una conexión segura con las instancias.

### Haga lo que hicimos: VCN para instancias

Antes de crearnos nuestras instancias de compute, que serán los servidores de Doguito Petshop, tenemos que crear una red virtual en la nube (VCN) donde el compute será prendido.

Una VCN es una red definida por software que se configura en los data centers de Oracle Cloud Infrastructure en determinada región. Esta red puede contener subredes, que son una subdivisión de una VCN.

Para eso debemos acceder el menú “Red”, “Redes Virtuales en la Nube” y empezar el asistente de creación de redes que nos ayudará con esa tarea.

### Para saber mais: redes en OCI

Cuando hablamos de infraestructura en Cloud, una de nuestras primeras tareas es estructurar una red. En general estas redes son conocidas como redes virtuales ya que son definidas via software al contrario de dispositivos físicos de hardware. Estas redes virtuales poseen diversos conceptos elaborados que puedes profundizar viendo los videos de [esta playlist](https://www.youtube.com/playlist?list=PLvlciYga5j3z7biGjV7-fywS-xEJ3W6Pp "esta playlist").

El contenido del video puede presentar algunos tópicos desactualizados, por eso, todos los detalles sobre la utilización de Redes en OCI pueden ser encontrados en la documentación oficial, a través del link:

[Documentación de Oracle Cloud Infrastructure](https://docs.oracle.com/es-ww/iaas/Content/Network/Concepts/landing.htm#top "Documentación de Oracle Cloud Infrastructure")

### Lo que aprendimos
Lo que aprendimos en esta aula:

- VCNs - Redes Virtuales en la Nube - controlan la comunicación de los componentes de Cloud con la internet y con los servicios de Oracle a través de subredes virtuales que poseen sus própias tablas de ruta, listas de seguridad y gateways.
- Creamos una VCN con uns subred pública y otra privada en OCI utilizando Wizard en pocos pasos.
- Como es definido la ruta y la seguridad en las VCNs y como estes atributos restringen y tornan segura la comunicación de las instancias que crearemos para nuestra aplicación.

### Haga lo que hicimos: nuestro primer compute

Creamos nuestro primer compute. Computes son la estructura de la OCI para provisionar y gerenciar hosts de computación, conocidos como instancias.

Puedes crear instancias conforme sea necesario para atender a los aplicativos que deseas implementar en la OCI. Después de crear una instancia, puedes accederla con seguridad utilizando una llave SSH, reiniciarla, adjuntar y desadjuntar volúmenes y cerrarlas. Pero recuerda que cualquier alteración hecha en las unidades locales de la instancia son pérdidas cuando las cierra.

Para crearnos una instancia, que será un servidor de Doguito Petshop, podemos acceder al menú “Computación” y después “Instancias”.

### Para saber más: todo sobre computes

Como ya aprendimos, computes representan las instancias de servirán nuestras aplicaciones en cloud. Existen muchas opciones para elegir, que equilibran cuestiones de costo y performance.

Si te interesaste por este tema y quieres saber todos los detalles de la configuración de computes en OCI, tienes que ver[ esta playlist](https://www.youtube.com/playlist?list=PLKCk3OyNwIzsAjIaUaVsKdXcfBOy6LASv " esta playlist") que nos explica todo sobre computes en OCI.

El contenido del video puede presentar algunos tópicos desactualizados, por eso, todos los detalles sobre la utilización de Redes en OCI pueden ser encontrados en la documentación oficial, a través del link:

[Documentación de Oracle Cloud Infrastructure](https://docs.oracle.com/es-ww/iaas/Content/home.htm "Documentación de Oracle Cloud Infrastructure")

conectarce co en servidor por ssh

`ssh <usuario>@<ip_publica> -i nombre_del_archivo_rsa`

### Haga lo que hicimos: instalando softwares

Realizamos la instalación de los softwares necesarios para la ejecución del Doguito Server en la instancia creada. Para eso, instalamos el servidor Apache HTTP y creamos una página HTML muy básica, solamente para validar el funcionamiento del servidor.

Entretanto, para que la instancia sea accesible a través del puerto 80 via internet, es necesario la inclusión de una nueva regla de acceso en la lista de seguridad de la VCN pública.

Después de estos pasos es posible acceder al servidor a través de una requisición via navegador, utilizando el IP Público como localización.

¡Llegó la hora de realizar estos pasos, accede al Cloud Shell y empezamos!

### Haga lo que hicimos: instalando softwares

Nuestras expectativas en relación al proyecto de Doguito Petshop son grandes. Entretanto, tenemos que evitar que la página caiga en su lanzamiento, debido a un número muy grande de accesos. Vamos a mantener más de un servidor funcionando y utilizar un balanceador de carga para distribuir la carga entre ellos.

De esta manera, nuestro próximo paso será crear una instancia del Doguito Petshop Server para después implementar un balanceador de cargas.

La creación de este servidor seguirá exactamente los mismos pasos de la primera vez. Entretanto, vamos a alterar su nombre (que parará a ser “dps-vm2”) y el texto de la página HTML patrón, que debe informar que accederemos un segundo servidor.

### Para saber mais: introducción a load balancers

Cuando pensamos en aplicaciones escalables horizontalmente, implantadas en cloud y en infraestructuras convencionales, el primer componente que nos viene en mente es un balanceador de cargas. Este servirá para distribuir las cargas del trabajo entre diferentes instancias de servidores de acuerdo con un algoritmo predeterminado.

Puedes encontrar más detalles sobre load balancers en OCI viendo a este video de Oracle:

[Introduction to Oracle Cloud Infrastructure Load Balancer](https://www.youtube.com/watch?v=tY2UuVbDElc "Introduction to Oracle Cloud Infrastructure Load Balancer")

El contenido del video puede presentar algunos tópicos desactualizados, por eso, todos los detalles sobre la utilización de Redes en OCI pueden ser encontrados en la documentación oficial, a través del link:

[Documentación de Oracle Cloud Infrastructure](https://docs.oracle.com/es-ww/iaas/Content/home.htm "Documentación de Oracle Cloud Infrastructure")

### Lo que aprendimos

Lo que aprendimos en esta aula:

- Necesitamos un compute para implementar nuestra aplicación de Doguito, ya que representa el servidor en el cual la aplicación será instalada.
- Para crear y configurar un compute tenemos que acceder a la opción “Computación” y después “Instancias” del menú de OCI.
- Balanceador de carga es un componente responsable por distribuir la carga de requisiciones entre las instancias de computación. Es importante para que la aplicación escale de manera horizontal y la torna más resiliente a fallas.
- Para crear un balanceador de cargas necesitamos acceder el menú Red y después la opción “Balanceadores de Carga”. En este proceso de creación indicamos cuáles servidores de back-end serán utilizados.
- Con un balanceador de cargas podemos tornar la infraestructura de Doguito más flexible.