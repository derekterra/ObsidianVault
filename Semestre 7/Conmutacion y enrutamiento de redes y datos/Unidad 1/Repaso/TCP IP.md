

# TCP/IP
Es un modelo como el OSI, pero este es diferente, el OSI es una referencia, el TCP/IP esta basado en puros protocolos:

## Aplicacion

En la capa aplicacion, presentacion, sesion se usan los protocolos
[[Protocolos#DNS|DNS]] 
[[Protocolos#DHCP|DHCP]] 
[[Protocolos#HTTP|HTTP]] 
HTTPS
FTP
[[Protocolos#SAMBA|SAMBA]] 
SSH 
SMTP
POP
TELNET

### Direccionamiento
Datos

## Transporte

En la capa de transporte
[[Protocolos#TCP|TCP]] 
[[Protocolos#UDP|UDP]] 

### Direccionamiento
Puerto origen y puerto destino

## Internet

En la capa de Red
[[Protocolos#IP|IP]] 
ARP
ICMP

### Direccionamiento
Direccionamiento logico (origen destino)

## Acesso al medio

En la capa de enlace
ETHERNET
FDDL
Token Ring
WIFI
PPF
HDLCJSON
Etc

### Direccionamiento
Direccion fisica origne y destino (MAC)


En la capa fisica
4B/5/B

### Direccionamiento
Bits


PREGUNTA DE EXAMEN: Cuando un paquete va brincado de ruta a ruta, cual es la direccion que va cambiando, la fisica o la logica?
La fisica, la logica no puede cambiar, si cambia la logica no puede encontrar el resultado, la logica la usa paraa buscar en las tablas de enrutamiento y para pedir retransmision
