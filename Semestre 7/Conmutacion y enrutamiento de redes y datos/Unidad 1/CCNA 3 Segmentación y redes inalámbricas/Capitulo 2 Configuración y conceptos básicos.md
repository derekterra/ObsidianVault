 # Elementos claves de las redes  802.3/Ethernet

## [[Protocolos#CSMA CD|CSMA/CD]]
Tecnología de acceso múltiple por detección de portadora y detección de colisiones (CSMA/CD) IEEE.  

Las **señales** de **Ethernet se transmiten a todos los hosts que están conectados a la LAN** mediante un conjunto de normas especiales que **determinan cuál es la estación que puede tener acceso a la red**. 
Los switches full-duplex no utilizan CSMA/CD

## Tipos de comunicaciones
### Unicast
De uno a uno, un emisor y un receptores
- Llamadas
- Mensajes entre dos personas

### Broadcast
Comunicación en la que se envía una trama desde una dirección hacia todas las demás direcciones. Un emsior a todas las otras dierecciones, de uno a todos los nodos. Baja el rendimiento de una red (en ipv4, no en ipv6, ipv6 es mas dificil de configurar)
- HUB
- DHCP

### Multicast
Comunicación en la que se envía una trama a un grupo específico de dispositivos o clientes. Los clientes de la transmisión multicast deben ser miembros de un grupo multicast lógico para poder recibir la información. Un ejemplo de  
transmisión multicast son las transmisiones de voz y video relacionadas con las reuniones de negocios en conferencia  
basadas en la red.
**Un emisor a un grupo de direcciones**

## Trama Ethernet
La estructura de la trama de Ethernet agrega encabezados y tráilers alrededor de la Capa 3 PDU para encapsular el mensaje que debe enviarse. Tanto el tráiler como el encabezado de Ethernet cuentan con varias secciones (o campos) que el protocolo Ethernet utiliza.

### Campos Preámbulo y Delimitador de inicio de trama
Loa campos Preámbulo (7 bytes) y Delimitador de inicio de trama (SFD) (1 byte) se utilizan para la sincronización entre los dispositivos emisores y receptores.

### Campo Dirección MAC de destino  
El campo Dirección MAC de destino (6 bytes) es el identificador del receptor deseado. La Capa 2 utiliza esta dirección para ayudar a que un dispositivo determine si la trama está dirigida a él.

### Campo Dirección MAC origen  
El campo Dirección MAC de origen (6 bytes) identifica la NIC o interfaz que origina la trama. Los switches utilizan esta dirección para agregar dicha interfaz a sus tablas de búsqueda. 

### Campo Longitud/tipo  
El campo Longitud/Tipo (2 bytes) define la longitud exacta del campo Datos de la trama. 

### Campos Datos y Relleno  
Los campos Datos y Relleno (de 46 a 1500 bytes) contienen la información encapsulada de una capa superior, que es una PDU de Capa 3 genérica, o, más comúnmente, un paquete de IPv4. Todas las tramas deben tener una longitud mínima de 64 bytes.

### Campo Secuencia de verificación de trama  
El campo FCS (4 bytes) detecta errores en una trama. Utiliza una comprobación de redundancia cíclica (CRC). 

## [[Conceptos#MAC|Direccion MAC]]
Una dirección Ethernet MAC  
es un valor binario de 48 bits que se compone de dos partes y se expresa como 12 dígitos hexadecimales. Todos los dispositivos conectados a una LAN Ethernet tienen interfaces con direcciones MAC. La NIC utiliza la dirección MAC para determinar si deben pasarse los mensajes a las capas superiores para su procesamiento.

## Configuracion Duplex
Se utilizan dos tipos de parámetros duplex para las comunicaciones en una red Ethernet: half duplex y full duplex. 

### Half duplex (CSMA/CD)
- Flujo de datos unidreccional
- Alto potencial para las colisiones
- Conectividad de hub

### Full Duplex
- Solo punto a punto
- Conectado a puerto de switch dedicado
- Requiere soporte para full duplex en ambos extremos
- Sin colisiones
- Circuito de deteccion de colisiones

## Configuracion del puerto del switch

El puerto de un switch puede configurarse de tres manera

- auto: Permite que los dos puertos se comuniquen para decidir el modo

- full: establece el modo full-duplex. 

- half: establece el modo half-duplex

## Direccionamiento y [[Conceptos#Tabla MAC|tablas]] MAC de los switches
En un principio la tabla esta vacia , arranca el swtich, todo se guarda en la RAM, tiene que ir construyendo las tablas conforme va recibiendo informacion, 

## [[Conceptos#Dominio de colision|Dominios de colisión]]
Para reducir el número de nodos en undeterminado segmento de red, se pueden crear segmentos físicos de red individuales, llamados dominios de colisión. El área de red donde se originan las tramas y se producen las colisiones se denomina dominio de colisiones. Todos los entornos de los medios compartidos, como aquellos creados mediante el uso de hubs, son dominios de colisión.
**Cada puerto de un Switch, es un dominio de colision**

## [[Conceptos#Dominio de broadcast Difusion|Dominios de broadcast]]
Cada puerto de un router, es un dominio de broadcast


# Consideraciones de diseño de una LAN
## Latencia de una red
La latencia es el tiempo que una trama o paquete tarda en hacerel recorrido desde la estación origen hasta su destino final.
Cada dispositivo de la ruta introduce latencia
El diamentro de la red debe ser lo mas pequeño posible

La latencia consiste en por lo menos tres componentes.

- Retraso de la NIC (Tarjeta de red) - En primer lugar, el tiempo que toma la NIC origen en colocar pulsos de voltaje en el cable y el tiempo que tarda la NIC destino en interpretar estos pulsos. 

- Retardo de propagación real - ya que la señal tarda un tiempo en recorrer el cable.

- Numero de dispositivos - la latencia aumenta según los dispositivos de red que se encuentren en la ruta entre dos dispositivos. Estos pueden ser dispositivos de Capa 1, Capa 2 o Capa 3.

## Causas comunes de la congestion de la red
- Tecnologia de redes y computadoras cada vez mas potentes
- Volumen de tragico de la red cada vez mayor
- Aplicaciones con altra demanda de ancho de banda

### Considere para el diesño ademas lo visto en el capitulo 1
- Diametro de la red
- Agregado de ancho de banda
- Necesidad de convergencia(Diferentes tipos de datos llegando por medio de la red EJ. Voz, video, fotos, etc)
- Analisis de la comunidad de ususarios y almacenamiento de datos, debe estar lo mas cerca los usuarios y lo que compramos debemos hacerlo pensando a futuro

## Control de latencia 
- Considere la latencia producida por cada dispositivo de la red

- Los dispositivos de las capas OSI mas altas tambien pueden aumentar la latenica de la red

En cuanto mas alto el nivel OSI, mas lento sera, ya que en cuanto mas grande el novel, hacen mas cosas de capas inferiores


## Eliminacion de los cuellos de botella de la red
Siempre usar este metodo cuando se tenga mucho trafico

# Metodos de reenvio de un switch
## Almacenamiento y envío
Un switch de almacenamiento y envio **recibe** toda **las tramas**, **calcula la CRC** y **verifica la longitud** de la trama. **Si la CRC y la longitud de la trama son validas**, **el switch busca la direccion de destino**, la cual determina la interfaz de salida. **Entonces, se envia la trama por el puerto correcto.**

## Método de corte
El switch que utiliza el metodo de corte **envia la trama antes de recibirla en su totalidad**. Como minimo, la direccion de destino de la trama debe leerse antes de que la trama pueda enviarse.

### Variantes de la conmutacion por metodo de corte
#### Conmutacion por envio rapido
La conmutacion por envio rapido ofrece el mas bajo nivel de latencia. La conmutacion por envio rapido reenvia el paquete inmediatamente despues de leer la direccion de destino

#### Conmutacion libre de fragmentos
En la conmutaciones libre de pragmentos, el switch almacena los primeros 64 bytes de la trama ante de reenviarla

# Conmutacion simetrica y asimetrica
## Simetrico
A cada puerto del switch de le asigna el mismo ancho de banda, los switches vienen generalmente de esta forma, se puede modificar

## Asimetrico
Se asigna mas ancho de banda al puerto conectado al servidor

# Búfer de memoria
## Memoria basada en puerto
En el búfer de memoria basado en puerto, **las tramas se almacenan en colas conectadas a puertos de entradas especifica**

Esta tecnica es mucho mejor

## Memoria compartida
El búfer de memoria compartida **deposita todas las tramas en un bufer de memoria comun que comparten todos los puertos del switch**

# Conmutacion de capa 2 y 3

Un switch LAN de Capa 2 lleva a cabo los procesos de conmutación y filtrado basándose solamente en la dirección MAC de la Capa de enlace de datos (Capa 2) del modelo OSI.
  
Un switch de Capa 3, funciona de modo similar a un switch de Capa 2, pero  en lugar de utilizar sólo la información de las direcciones MAC para determinar los envíos, el switch de Capa 3 puede también emplear la información de la dirección IP. En lugar de aprender qué direcciones MAC están vinculadas con cada uno de sus puertos, el switch de Capa 3 puede también conocer qué direcciones IP están relacionadas con sus interfaces.

La 3 permite enrutar con switches capa 3, no salen segmentos de uno a otro, a menos que se tenga un switch capa 3

La 2 es puramente fisica

# Ruteador y switch capa 3
Los routers proporcionan servicios adicionales de Capa 3 que los switches de Capa 3 no pueden realizar. Los routers también pueden llevar a cabo tareas de reenvío de paquetes que no realizan los switches de Capa 3, como establecer conexiones de acceso remoto con dispositivos y redes remotas

El router tiene muchas mas caracteristicas como salir a las WAN y protocolos de....



# Configurar hyperterminal
Cables transpuestos color azul
Aplicacion Hyperterminal para PC

Que se configura?
Pais/region: no se pone
Codigo de area: 
Conectar usando: COM1

En esta zona usar los predeterminados
Bits por segundo: 9600 

# Configurar la concectividad IP
568 A - es un cable par trenzado, crusover, los colores que comienzan con verde,etc

Crusover
Transpuesto


Dispositivos iguales -> cruzado
Dispositivos diferentes -> directo
excepcion ruteadro-servidor -> cruzado  **EXAMEN, En el simulador, no acepta poner los cables de forma equivocada**

172 B

- Para la administracion de TCP/IP debe asignarse una dirección de la capa 3 al switch
- VLAN 1 es la interfaz de admonistracio..........

# Configurar la conectividad IP
Sintaxis del comando de CLI IOS de Cisco

S1 \#configure terminal - Cambio de modo EXEC probilegiado a modo de configuracion globar
S1 (config) #interface vlan 99 - Ingrese al modo de configuracion de interfaz para la inrefaz de VLAN 99
S1 (config-if) #direccion IP 172.17.99.11 255.255.255.0
..............




NOTA En la diapositiva con los cuadros naranjas, los up y up indican que esta levantado fisico y logicamente




RAM -> running-config
NVRAM -> startup-config
\#copy run star

# Configurar duplex y velocidad

Sintaxis de comando de la CLI del IOS de Cisco  | ------------
------------ | ------------
Cambiar de modo EXEC privilegiado a modo de configuracion global | S1#configure terminal
Ingresar al modo de configuración de interfaz | S1(config)#Interface fastethernet 0/1
Configurar el modo duplex de interfaz para activar la configuración duplex automática | S1(config-if)#duplex auto
Configurar duplex y velocidad de la interfaz y activar la configuración de velocidad automática | S1(config-if)#speed auto
Volver al modo EXEC privilegiado | S1(config-if)#end
Guardar la configuración en ejecucion en la configuración incial del switch | S1#copy running-config startup-config


# Configurar una interfaz web
![[Pasted image 20220911213143.png]]

# Configurar la conectividad IP
![[Pasted image 20220911213250.png]]
![[Pasted image 20220911213308.png]]



# Comandos show 
![[Pasted image 20220911213446.png]]

# [[Ataques de seguridad]]


# Tipos de direcciones MAC seguras
## Direcciones MAC seguras estáticas: 
Las direcciones MAC se configuran  
manualmente mediante el comando de configuración de interfaz switchport port-security mac-addressmac-address. Las direcciones MAC configuradas de esta forma se almacenan en la tabla de direcciones y se agregan a la configuración en ejecución del switch.  

## Direcciones MAC seguras dinámicas: 
Las direcciones MAC se aprenden de  
manera dinámica y se almacenan sólo en la tabla de direcciones. Las direcciones MAC configuradas de esta manera se eliminan cuando el  
switch se reinicia. 

## Direcciones MAC seguras sin modificación: 
Se puede configurar un puerto para que aprenda de manera dinámica las direcciones MAC y luego guardarlas en la configuración en ejecución.