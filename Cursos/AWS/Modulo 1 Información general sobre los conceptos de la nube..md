# Sección 1: Introducción a la informática en la nube


## Definicion de cloud computing
Mi definicion antes de ver los videos: Son aquellos servicios a los que podemos tener acceso medianante el internet conectandonos a los servidores de alguien mas

Definicion del curso: Es la entrega bajo demanda de potencia de cómputo, base de datos, almacenamiento, aplicaciones y otros recursos de TI, a través de internet con un sistema de precios de pago por uso

Tiene la ventaja de que basicamente no tienes que procuparte por el hardware que necesitas, si no verlo mas como software y usarlo como tal. 
Es mucho mas barato ya que no tienes que gastar en servidores o en 

## Modelos de servicio en la nube

- IaaS (Infrastructura como servicio)
Otorga maquinas dedicada, maquinas virtuales, almacenamiento, etc

- PaaS (Plataforma como servicio)
Administracion de aplicaciones

- SaaS (Software como servicio)
Producto completo(Aplicaciones de usuario final)
El provedoor se encarga de administracion, ejemplo una aplicacion de email en la Web donde no debes preocuparte por el mantenimiento de los servidores

## Modelos de implementacion de informatica en la nube
- Nube
TODO se ejecuta en la nube, se crean en la nube, o se tranfieren a la nube una aplicación basada en la nube


Se encuentra completamente implementada en la nube, de modo que todas las partes de la aplicación se ejecutan en la nube. Las aplicaciones en la nube se crearon en la nube o las migraron de una infraestructura existente para aprovechar los beneficios de la informática en la nube. Las aplicaciones basadas en la nube se pueden crear en partes de infraestructura de bajo nivel o pueden utilizar servicios de nivel superior que permiten abstraerse de los requisitos de administración, arquitectura y escalado de la infraestructura principal

- Hibrido
Una implementación híbrida es una manera de conectar la infraestructura y las aplicaciones entre los recursos basados en la nube y los recursos existentes situados fuera de ella. El método más común de implementación híbrida es entre la infraestructura en la nube y la que ya se encuentra en las instalaciones. Este modelo permite a una organización extender y aumentar su infraestructura en la nube mientras conecta los recursos de la nube a los sistemas internos.


- Infrastructura Local (Nube privada)
La implementación de recursos en las instalaciones mediante herramientas de administración de recursos y virtualización se denomina a veces nube privada. A pesar de que la implementación en las instalaciones no ofrece muchos de los beneficios de la informática en la nube, en algunas ocasiones se utiliza por su capacidad de proporcionar recursos dedicados. En la mayoría de los casos, este modelo de implementación es idéntico al de la infraestructura de TI antigua, pero también podría utilizar tecnologías de virtualización y administración de aplicaciones paraincrementar el uso de los recursos.

## Similitudes entre AWS y las TI tradicional 
Hay muchas similitudes entre AWS y el espacio de TI en las instalaciones tradicional:
•Los grupos de seguridad de AWS, las listas de control de acceso a la red (ACL de red) y AWS Identityand Access Management (IAM) son similares a los firewalls, las listas de control de acceso (ACL) y los administradores.
•ElasticLoad Balancingy Amazon Virtual PrivateCloud (Amazon VPC) son similares a los enrutadores, las canalizaciones de red y los conmutadores.
•Las imágenes de Amazon Machine (AMI) y las instancias de Amazon ElasticCompute Cloud (Amazon EC2) son similares a los servidores en las instalaciones.
•Amazon ElasticBlock Store (Amazon EBS), Amazon ElasticFile System(Amazon EFS), Amazon Simple Storage Service(Amazon S3) y Amazon RelationalDatabaseService(Amazon RDS) son similares al almacenamiento de conexión directa (DAS), las redes de área de almacenamiento (SAN), el almacenamiento conectado a la red (NAS) y un servicio de administración de bases de datos relacionales (RDBMS).

Con los servicios y características de AWS, puede hacer casi todo lo que desee con un centro de datos tradicional.

## Resumen del modulo
Estos son algunos de los aprendizajes clave de esta sección del módulo:
- La informática en la nube es la entrega bajo demanda de recursos de TI a través de Internet mediante un modelo de precios de pago por uso.
- La informática en la nube le permite considerar (y usar) su infraestructura como software.
- Existen tres modelos de servicios en la nube: IaaS, PaaS y SaaS.
- Existen tres modelos de implementación en la nube: nube, híbrido y nube privada.
- Existen muchos equivalentes de servicios de AWS para el espacio de TI en las instalaciones tradicional.

# Sección 2: Ventajas de la informatica en la nube
- Cambiar gastos de capital por gasto variable
- Beneficiarse de las grandes economias de escala masiva
- Evitar asumir estimaciones sobre capacidad
- Aumentar la velocidad y la agilidad: en un entorno de informática en la nube, se puede acceder a recursos de TI nuevos con tan solo un clic, por lo que el tiempo que se tarda en poner esos recursos a disposición de sus desarrolladores se reduce de semanas a tan solo minutos. El resultado es un aumento radical del nivel de agilidad de la organización, ya quese reducen de manera significativa el costo y el tiempo pararealizar tareas de desarrollo y experimentación

- Dejar de gastar dinero en la ejecución y el manenimiento de centros de datos: concéntrese en proyectos que diferencien su negocio en lugar de centrarse en la infraestructura. La informática en la nube le permite centrarse en sus propios clientes, en lugar de la tediosa tareade montar servidores en bastidores, apilarlos y alimentar servidores.

- Adquirir escala mundial en cuestión de minutos: Puede implementar su aplicación en varias regiones de AWS de todo el mundo con tan solo unos clics. Como resultado,puede ofrecer una latencia menor y una mejor experiencia a sus clientes de forma sencilla y con un costo mínimo.

## Resumen
Los aprendizajes clave de esta sección del módulo incluyen las seis ventajas de la informática en la nube:

- Cambiar sus gastos de capital por gastos variables
* Economías de escala masivas
* Evitar asumir estimaciones sobre capacidad
* Aumentar la velocidad y la agilidad
* Dejar de gastar dinero en la ejecución y el mantenimiento de centros de datos
* Adquirir escala mundial en cuestión de minutos

# Sección 3: Introducción a Amazon Web Services (AWS)

## ¿Qué son los serivicios web?
Un servicio web es cualquier software que se pone a su disposición a través de Internet y utiliza un formato estandarizado (como el lenguaje de marcado extensible ```[XML]``` o la notación de objetos en JavaScript ```[JSON]```) para la solicitud y la respuesta de una interacción con la interfaz de programación de aplicaciones (API). 

## ¿Qué es AWS?
- AWS es una plataforma en la nube segura que ofrece un amplio conjunto de productos globales basados en la nube. 
- AWS le proporciona acceso bajo demanda a recursos informáticos, de almacenamiento, de red, de base de datos y otros recursos de TI y herramientas de administración. 
- AWS ofrece flexibilidad. 
- Solo paga por los servicios individuales que necesita, en la medida en que los utilice. 
- Los servicios de AWS trabajan en conjunto como piezas fundamentales. 

## Categorías de los servicios
![[Pasted image 20230216152600.png]]

## Elección de un servicio
El servicio que elija utilizar dependerá de sus objetivos empresariales y requisitos tecnológicos. En el ejemplo que acaba de ver, la solución utilizó Amazon EC2 como servicio informático. Sin embargo, este es solo uno de los muchos servicios de informática que ofrece AWS. A continuación, se muestran otras ofertas de informática de AWS que podría elegir utilizar para los siguientes casos de uso de ejemplo:

- Amazon EC2: desea tener un control absoluto de sus recursos informáticos de AWS.

- AWS Lambda: desea ejecutar el código y no administrar ni aprovisionar servidores.

* AWS Elastic Beanstalk: desea un servicio que implemente, administre y escale sus aplicaciones web en su lugar.

•

Amazon Lightsail

: necesita una plataforma en la nube ligera para una aplicación

web sencilla.

•

AWS Batch

: necesita ejecutar cientos de miles de cargas de trabajo por lotes.

•

AWS Outposts

: desea ejecutar la infraestructura de AWS en su centro de datos

en las instalaciones.

•

Amazon Elastic Container Service

(Amazon ECS),

Amazon Elastic Kubernetes

Service

(Amazon EKS) o

AWS Fargate

: desea implementar una arquitectura de

microservicios o contenedores.

•

VMware Cloud on AWS

: dispone de una plataforma de virtualización de

Formación y certificación de AWS

Módulo 1: Información general sobre los conceptos de la nube

© 2020 Amazon Web Services, Inc. o sus filiales Todos los derechos reservados.

33

[](https://aws.amazon.com/ec2/ "https://aws.amazon.com/ec2/")

[](https://aws.amazon.com/lambda/ "https://aws.amazon.com/lambda/")

[](https://aws.amazon.com/elasticbeanstalk/ "https://aws.amazon.com/elasticbeanstalk/")

[](https://aws.amazon.com/lightsail/ "https://aws.amazon.com/lightsail/")

[](https://aws.amazon.com/batch/ "https://aws.amazon.com/batch/")

[](https://aws.amazon.com/outposts/ "https://aws.amazon.com/outposts/")

[](https://aws.amazon.com/ecs/ "https://aws.amazon.com/ecs/")

[](https://aws.amazon.com/eks/ "https://aws.amazon.com/eks/")

[](https://aws.amazon.com/fargate/ "https://aws.amazon.com/fargate/")

[](https://aws.amazon.com/vmware/ "https://aws.amazon.com/vmware/")

servidores en las instalaciones que desea migrar a AWS.

Del mismo modo, existen diversos servicios entre los que puede elegir en las demás

categorías y el número de ofertas sigue creciendo.

# Sección 4: Migración a la nube de AWS - Marco de adopción de la nube de AWS (CAF de AWS)