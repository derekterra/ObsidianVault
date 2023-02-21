
# Dispositivos 
## Routers
Cada puerto es un [[Conceptos#Dominio de colision|domio de colision]] y uno de [[Conceptos#Dominio de broadcast Difusion|brodcast]]
Me permite unir redes locales


## Switch
Dispositivo de [[Modelo OSI#2 Capa de enlace|capa 2]] y [[Modelo OSI#3 Capa de red|capa 3]] que basicamente se encarga de crear tablas [[Conceptos#Tabla ARP|ARP]] para mapear donde se encuentra cada uno de los equipos

### Switch capa 2
Detecta errores

Tiene direccionamiento MAC

Delimita tramas

### Switch capa 3
Es uso interno de una LAN, sive para segmentar una red
maneja tablas, segmenta los [[Conceptos#Dominio de broadcast Difusion|dominio de brodcast]] de manera nata
Enruta VLANS


## HUB 

|--------|
|            |
|  ---->  |
|            |
|--------|

Este ya no se usa ya que solamente manda tramas a todos lados y consume muchos recursos el estar mandando a todos lados, causa muchas colisiones

## Repetidor
Aparato que toma una señal y la regenera o repite para que alcance mas distancia, ya que dependiendo del medio puede llegar hasta cierta distancia (Ethernet 100 mts)


## Amplificador

## Multiplexor

## Transceiver
Es un convertidor de medios, convierte una entrada de fibra optica a par trenzado

## Modem
Convertidor de señales, de analga a digital o vicebersa


## Puente
Unia dos segmentos de red diferentes, como Token Ring con Ethernet
Actualmente Token Ring ya no existe, entonces el puente ya no se usa 

## MAU
Unidad de acceso a multiestaciones
Exclusivo de Token Ring, era el aparato que elegia quien tenia los recursos, creando y controlando el Token.
Era el router de Token Ring

## Punto de acceso
Se utiliza en redes inalambricas
Sirve para ampliar la cobertura de una red alambrica 
Lo que hace es conocer direcciones mac, no conoce IP ni hay salida a Wan(seria un router), se usa en LAN
Usa el CSMA/CA para evitar colisiones

Ruteador
Ruteador inalambrico


## Firewall hardware
Seguridad, a que se puede acceder, quienes pueden acceder a que, tiene antivirus,etc.
Al principio todos los puertos del firewall estan denegados, al igual que las vlan, solo se tiene acceso lo que digamos 

## Gateway
Es un traductor de protocolos, cuando no exitia internet, cada fabricnate tenia su propio protocolo, por lo que se necesitaba un traductor
Se sigue utilizando en voip (voz ip) donde por medio de la red mandan audio y la recive un telefono inalambrico