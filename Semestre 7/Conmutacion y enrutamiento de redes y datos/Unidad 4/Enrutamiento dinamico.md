EXAMEN 10/25/22 MIN 9:22
Que es un sistema autonomo
Protocolo de enlace de puerta interior y para que sirve

utilizan protocolos de gateway interior comoRIP,  
EIGRP, OSPF e IS-IS para realizar el enrutamiento de paquetes dentro de sus propias redes. Son una de muchas redes  
independientes dentro del sistema autónomo de ISP. ISP es responsable del enrutamiento de paquetes dentro del sistema  
autónomo y entre otros sistemas autónomos.

Los protocolos de gateway interiores (IGP) pueden clasificarse en dos tipos:  
 Protocolos de enrutamiento por vector de distancia:
El vector de distancia significa que las rutas son publicadas como vectores de distancia y dirección. La distancia se define en  
términos de una métrica como el conteo de saltos y la dirección es simplemente el router del siguiente salto o la interfaz de  
salida.
 Protocolos de enrutamiento de estado de enlace
un router configurado con un protocolo  
de enrutamiento de estado de enlace puede crear una "vista completa" o topología de la red al reunir información  
proveniente de todos los demás routers.
# Proposito de los protocolos de enrutamiento dinamico
- Descubirimiento de redes remotas
- Mantenimiento de informacion de enrutamiento actualizadaa
- Seleccion de la mejor ruta hacia las redes de destino y 
- Capacidad de encontrar una mejor nueva ruta si la ruta actual deja de estar disponible

# Componentes de los protocolos de enrutamiento dinamico

- Estructuras de datos
- Algoritmo
- Mensajes del protocolo de enrutamiento

# Comparacion entre el enrutamiento estatico y el dinamico

# Clasificacion de los IGP
IGP :

## Clasificacion
### Vector distancia
No conoce la topologia completa, conoce solamente a los vecinos y estos se comparten la informacion cada 30 seg

EXAMEN  menciona 5 diferencias entre protocolos de vector distancia y estado de enlace

#### Protocolos:
#### RIP
No es para redes grandes, solo permite 15 saltos, no usar versiones 1 en redes 

La version 2 es multicast y vlsm

Siempre cambiar a la version 2 

#### IGRP
Es obsoleto, ya casi no lo usan, en vez de saltos usa ancho de banda + retardo

#### EIGRP
Es el mejor protocolo

EXAMEN PDM
MODULO DEPENDIENTE DEL PROTOCOLO
Permite manejar cualquier protocolo de enrutamiento(IP,IPx,apple talk)

Tiene una tabla, enrutamiento, vecinos y topologia

QUE ES RTP

 Reemplaza el TCP y el UDP del modelo TCP/IP para aquellos que no lo usan

10/26/2022
# Clasificacion de los IGP (2)
### Estado de enlace 
Se crea una inundacion que da a conocer la red

# Protocolos con clase
EXAMEN
No envian la unformacion de la mascara en sus actualizaciones
Protocolos RIPv1 e IGRP
No permiten redes no contiguas 
No VLSM



# Protocolo sin clase
EXAMEN
......

EXAMEN
RED NO CONTIGUA: 
Que las ip son muy distintas 


# Resumen de los protocolos dinamicos


# Comparacion entre los prtocolos de enrutamiento
EXAMEN

igrp es exlusico de cisco
si vamos a usar IGRP y no tenemos cisco, usamos EIGRP


# Distancia admistrativa
Es lo que permmite a los routeadores cual protocolo va a tener prioridad sobre cual


EXAMEN: Escuchar el min 9:29
Que contiene una trabla de enrutamiento


red remora
costo
interfaz
-   **Red de destino:** esto corresponde a la red de destino donde deberá ir el paquete de datos.
-   **Máscara de subred:** es la que se utiliza para definir la máscara de subred de la red a la que debemos ir.
-   **Siguiente salto:** en inglés a esto se lo conoce como _next hop_. Es la dirección de IP de la interfaz de red por donde viajará el paquete de datos, para seguir con su camino hasta el final.
-   **Interfaz de salida:** es la interfaz de red por donde deben salir los paquetes, para posteriormente llegar finalmente al destino.
-   **Métricas:** tienen varias aplicaciones. Una de ellas consiste en indicar el número mínimo de saltos hasta la red de destino, o simplemente el «coste» para llegar hasta la red de destino, y sirve para dar prioridad.

# Distancias administrativas predeterminadas


# Interfases pasivas
EXAMEMN
Declaram 

# Configuracion del protocolo RIP
Es protocolo con clase 


# No admite redes no contiguas

# Configuracion 2


# Autoresumen

# Ventajas y desventajas sumarizacion automatica
## Ventajas


## Desventajas

# Ruta por defecto
Todos los dispositivos tienene que tener una ruta hacia WAN

