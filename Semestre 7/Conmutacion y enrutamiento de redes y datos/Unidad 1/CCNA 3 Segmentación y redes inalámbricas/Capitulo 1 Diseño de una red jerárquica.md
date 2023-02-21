8/29/2022
Para pequeñas y  medianas empresas, la comunicacioón digital de datos, voz y video es esencial para supervivencia de la empresa. En consecuencia, una LAN con un diseño apropiado es un requisito fundamental para hacer negocios en el presente. El usuario debe ser capaz de recnonocer una LAN bien diseñada y seleccionar los diapositivos apropiados par admitir las espcificaciones de las redes de una empresa pequeña o mediana.

![[Pasted image 20220925203403.png]]

# Capa de acesso
El propósito principal de esta capa es  
**aportar un medio de conexión de los  
dispositivos a la red** y **controlar qué  
dispositivos pueden comunicarse en la red**.

Todos los dispositivos finales estan conectados en esta capa



## Caracteristicas
- Seguridad de puerto
- [[Conceptos#VLAN|VLAN]]
- Fast Ethernet/Gigabit ethernet
- [[Conceptos#Power Over ethernet PoE|Power Over ethernet (PoE)]]
- Agregado de enlaces - Implementar el rendimiento la red, haciendo que donde haya mucho trafico se subdivida y lo que seria una persona ahora aguanta para ocho.
- Calidad de servicioes (QoS)

# Capa de distribucion
**Controla el flujo de tráfico de la red con el uso de políticas y traza los dominios de broadcast** al realizar el enrutamiento de las funciones entre las VLAN definidas en la capa de acceso.

## Caracteristica del switch de capa de distribucion
- Soporte de la [[Modelo OSI#3 Capa de red|capa 3]]
- Tasa de envio alta
- Gigabit Ethernet/10Gigabit Erhernet
- Componentes redundantes - Tolerancia a fallos, en caso de no encontrar un camino, que tenga varios caminos
- Politicas de seguridad/Listas de control de acceso
- Agregado a los enlaces
- Calidad del servicio (QoS)

# Capa de nucleo
Es la **backbone** de alta velocidad **de la internetwork**.  
La capa núcleo es **esencial para la interconectividad** entre los dispositivos **de la capa de distribución**, es importante que el núcleo sea sumamente disponible y redundante.

## Caracteristicas del Switch de capa nucleo
- Soporte de [[Modelo OSI#3 Capa de red|capa 3]]
- Tasa de envio muy alta (Es la mas alta de todas las capas)
- Gigabit Ethernet/10Gigabit Erhernet
- Componentes redundantes
- Agregando de enclaces
- Calidad del servicio (QoS)

# Beneficios de una red jerárquica

## Escalabilidad
- Las redes jerarquicas pueden **expandirse** con facilidad
## Redundancia
- La reduncanica a nivel del nucleo y de la distribucion asegura la **disponibilidad de la ruta**
## Rendimiento
- El agregado del enlace entre los niveles y núcleo de alto rendimiento y switches de nivel de distribucion **permite casi la velocidad del cable en toda la red**

## Seguridad
- **La seguridad** del puerto **en el nivel de acceso y las politicas** en el nivel de la distribucion **hacen que la red sea mas segura**

## Facilidad de administracion
- **La consistencia entre los switches** en cada nivel **hace que la administracion sea mas simple**

## Facilidad de mantenimiento
La modularidad del diseño jerarquico **permite que la red escale sin volverse demasiado complicada**

# Diseño lógico
Todos los aspectos de la seguiridad y la segmentacion de la red, se toma como diseño logico

# Diseño fisico
Son todas las caracteristicas de conexion

# Diagrama de topología 
Siempre hacer diagramas de red, si no se llegan a perder por lo extensas que son

# Consideraciones de diseño
## Diametro de la red
La cantidad de dispositivos que tiene que atravesar una trama para llegar del punto A al punto B 

## Agregado de ancho de banda
Conectar dos switches con dos enlaces tumba la red, a menos que se configure como uno solo 

Un ovalo que abarca varios enlaces se itiñoza en los diagramas para indicar el agregado del enlace

## Convergencia (Equipos heredados)
Grandes switches teléfonicos
Sistemas PBX pequeños

## Convergencia (Tecnologia avanzada)
De medianas a grandes empresas, de pequeñas a medianas empresas

## Analisis del flujo de datos
Es el proceso de **medicion del uso del ancho de banda en una red** y el analisis de datos con el fin del lograr ajustes del rendimiento, **Planificacion de la capacidad y toma de decisiones** con respecto a las mejoras del hardware.


8/30//2022

## Análisis de la comunidad de usuarios
Siempre se debe **tener en cuenta las necesidades futuras** de los usuarios, por ejemplo si una empresa necesita 20 computadoras, deberias conseguir equipo para futuras contratasiones. **Se debe de planear para que no haya cambios de aqui a 5 años. **

**Los servidores deben estar lo mas cerca posible de los usuarios**, para evitar que haya un diametro muy grande 

## Analisis de los medios de almacenamientos de servidores de datos

**Todos tus centros de datos deben estar conectados al mismo dispositivo**, para que esten interconectados , comunicacion punto a punto, y sea mucho mas eficaz

# Tipos de Switches
## Switches de configuración fija
**Los puertos, las caracteristicas y las opciones se limitan a aquellas que originalemnte vienen con el switch**. Si se busca expander, no se podra

## Switches de configuración modular
**El chasis acepta tarjetas de linea que contienen los puertos.** Se recomiendan cuando se busque expandir los puertos de una empresa

## Switches de configuracion apilable
backplane, **se conceta a traves de buses de datos y actuan como uno solo**, mucha mayor velocidad

Conectados por un cable especial, **operan** con eficacia **como un gran switch.**

# Caracteristicas de los switches
Cuando se selecciona un switch para las capas de acceso, de distribución y núcleo, **se debe considerar la capacidad del switch** para admitir los requerimientos de densidad de puerto, tasas de reenvío, agregado de ancho de banda de la red, tecnología PoE, soporte capa 3

## Densidad del puerto
La cantidad de puertos que tiene un switch

## Tasas de envio
Definen las capacidades de procesamiento de un switch mediante la **estimacion de la cantidad de datos que puede procesar por segundo el switch**. La velocidad de cable es la tasa de datos que cada puerto en el switch puede lograr, 100Mb/s Fast Ethernet o 1000 Mb/s Gigabit Ethernet
Por ejemplo, un switch gigabit con 48 puertos que opera a una vecocidad de calbe...

## Agregado de enclace o IEEE 802.3ad
Ayuda a **reducir estos cuellos de botella del tráfico** al permitir la **union de hasta ocho puertos de switch** para las comunicaciones de datos y al munistrar hasta 8Gb/s de rendimiento de datos cuando se utilizasn los pueros Gigabit Ethernet.


## Power over Ethernet(PoE)
Permite que el switch suministre energía a un dispositivo por el cableado de Ethernet existente

## Soporte de [[Modelo OSI#3 Capa de red|capa 3]]
Los [[Dispositivos#Switch capa 3|switches de la capa 3]] ofrecen una funcionalidad avanzada

Las politicas de seguridad impiden el acceso a los servidores 

Enrutamiento de capa 3 realizado por el switch para enrutar el trafico a la subred del servidor
