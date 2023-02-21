# Conceptos
## PDU
La forma que adopta una porción de datos en cualquier capa se denomina “unidad de datos del protocolo (PDU)”

Es la forma en que se le llaman a los datos dependiendo de la [[Modelo OSI|capa del modelo OSI]] que se encuentre. 

se utilizan para el intercambio de datos entre unidades disparejas, dentro de una capa del modelo OSI. Existen dos clases que son:

**PDU de datos** que contiene los datos del usuario principal (en el caso de la [[Modelo OSI#7 Capa aplicacion|capa de aplicación]]) o la PDU del nivel inmediatamente inferior.

**PDU de control** que sirven para gobernar el comportamiento completo del protocolo en sus funciones de establecimiento y unión de la conexión, control de flujo, control de errores, etc.

## Broadcast
Una trama broadcast se manda a todos los equipos conectados, suele ocurrir cuando:
los [[Dispositivos#Switch|switches]] no conocen las tablas de enrutamiento y tiene que mandar broadcast para conocer las direcciones

Cuando se conecta un nuevo equipo

Cuando no conoce la IP, manda un broadcast para ser contestado con una MAC

## Dominio de broadcast (Difusion)
Los dominios de difusión son los sitios de la red que se pueden separar de acuerdo a la dirección de red que los identifica. Los dispositivos capaces de crear dominios de difusión, o mejor dicho, de separar dominios de difusión, son los enrutadores ([[Dispositivos#Routers|routers]]) .

Imagina que tienes una red con varios [[Dispositivos#Switch|switches]], configurados todos por defecto dentro de la VLAN 1, si se envía un flujo de tramas de broadcast en esa red, las tramas llegaran a todos los puertos de todos los dispositivos conectados (excepto desde donde salio la trama).

Todos los puertos en un hub o switch por defecto pertenecen al mismo dominio de broadcast.

Todos los puertos en un router están en diferentes dominios de broadcast y los routers no reenviaran las tramas de broadcast de un dominio a otro.

NOTA: Los routers y las VLAN separan Dominios de broadcast

**Segmento de red donde un mensaje va a ser recibido por todos los dispositivos conectados** 
![[Dominios de Broadcast.png]]


## Dominio de colision

Un dominio de colisión es un segmento red donde los paquetes enviados por cada uno de los nodos pueden “colisionar”. El objetivo de una red es que funcione la intercomunicación entre cada uno de sus nodos con el mínimo número de problemas.

La colisión ocurre cuando dos dispositivos envían información al mismo tiempo en un segmento compartido.

Los [[Dispositivos#Puente|brides]], [[Dispositivos#Switch|switches]] y [[Dispositivos#Routers|routers]] crean dominios de colisión.

**Es un segmento de red donde varios pueden competir por la red**

![[Dominios de colision.png]]

![[Diferencia de Dominio de colision y de difusion.png]]


## Segmentación de red
Es un proceso que se encarga de dividir la red en pequeñas redes. Tiene el propósito de mejorar el rendimiento de la red, y, sobre todo, sus condiciones de seguridad. La segmentación funciona mediante el control de tráfico en todas las partes de la red, puedes optar por detener todo el tráfico en una parte que quiere alcanzar otra.


## Monomodo
## Multimodo
## Cableado backbone
## Tabla MAC
## Tabla ARP
## MAC
## IPV4
## IPV6
## Cableado horizontal
## Cableado vertical
## VLAN
Una VLAN segmente de forma virtual una red, esto significa basicamente que eliges quien recibe una trama y quien no, incluso si estan o no conectados fisicamente.

Solamente se podran comunicar con un [[Dispositivos#Switch capa 3|Switch capa 3]] o con un router
Obligatoriamente debe tener un ID

## Power Over ethernet (PoE)
Todos los cables que suministran energia electrica

## Puertos

### Puerto destino

HTTP -> 80
Telnet -> 23
POP -> 110
SMTP-> 25
SSH -> 21,22
DNS -> 53


### Puerto origen
Este al solicitar algo, se genera aleatoriamente para asi cada persona tenga un numero unico y cada uno obtenga el puerto destino que necesita, cuando se genera el numero aleatoria el puerto destino y origen se voltean 