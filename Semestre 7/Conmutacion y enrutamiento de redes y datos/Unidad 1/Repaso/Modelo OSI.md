btpsd
# Modelo OSI
## 1. Capa física
Maneja voltajes, señalización, medio de transmisión, tipo de conector que se va a utilizar, multiplexación etc.

PDU: Bits

### Dispositivos
[[Dispositivos#HUB|HUB]] 
[[Dispositivos#Repetidor|Repetidor]]
[[Dispositivos#Amplificador|Amplificador]]
Multiplexor
Transceiver
[[Dispositivos#Modem|Modem]]

## 2. Capa de enlace
Se encarga de hacer 4 cosas:
- Control de errores (método haming, bits de paridad, etc.)
- Direccionamiento físico (dirección mac)
- Delimitación de tramas
- Arbitreo del canal (Control de acceso al medio como [[Protocolos#CSMA CD|CSMA/CD]])

[[Conceptos#PDU|PDU]]: Tramas

### Dispositivos 
NOTA: Se usan solamente en LAN:

[[Dispositivos#Switch capa 2|Switch Capa 2]]
[[Dispositivos#Puente|Puente]]
[[Dispositivos#MAU|MAU]]
[[Dispositivos#Punto de acceso|Punto de acceso]]


## 3.Capa de red
- Direccionamiento lógico (ip, ipx, Apple talk)
- Enrutamiento (busca el mejor camino para enviar la información)
- Control de congestión
- Internet working

[[Conceptos#PDU|PDU]]: Paquetes

### Dispositivos
[[Dispositivos#Switch capa 3|Switch Capa 3]]
[[Dispositivos#Routers|Ruteador]]
Ruteador inalambrico

## 4. Capa de transporte
Se encarga del transporte fiable de los segmentos y en caso de error solicita retransmision.

[[Conceptos#PDU|PDU]]: Segmentos

## 5.Capa de sesion
a)Dialogo entre aplicaciones
b)establecimiento de puntos de sincronia
b)Establecimiento de puntos de sincronia

[[Conceptos#PDU|PDU]]: Datos

## 6.Capa de presentacion

a)Se encarga de la codificacion de los datos, es decir en como se va a presentar la informacion mandada al usuario

b)Encriptar los datos para evitar que sean leidos y robados por alguien mas

c) Compresion de datos, espacios vacios y todo lo que 

[[Conceptos#PDU|PDU]]: Datos

## 7.Capa aplicacion 
Interfaz con el usuario

[[Conceptos#PDU|PDU]]: Datos


# Funciones comunes a todas las capas
- Encapsulación: Cada capa agrega encabezados para comunicarse con su homóloga (en base al protocolo que se maneje)
- Segmentación: Cada capa agrega encabezados para comunicarse con su homóloga (en base al protocolo que se maneje)
- Establecimiento de la conexión (Interfaces): cuando cada capa presta servicios a las capas inferiores o superiores.
- Control de error: Verifican los encabezados que puso la homologa
- Control de flujo: Evitar saturar a la capa homologa regulando la velocidad del flujo de datos

![[MODELO OSI.xlsx]]

