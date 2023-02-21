# Red redundante
O red altamente tolerante  a fallos, capaza de tener siempre conexion a red, ya que tiene varias formas de conectarse.
incapaz de fallar 

## Incovenenientes de la redundancia

### Bucle capa 2
Las tramas de **Ethernet no poseen un tiempo de existencia** (TTL, Time to Live) como los paquetes IP que  
viajan por los routers. En consecuencia, **si no finalizan de manera adecuada** en una red conmutada, **las mismas siguen rebotando de switch en switch** indefinidamente o hasta que se interrumpa un enlace y  elimine el bucle. 

Las tramas de broadcast se envían a todos los puertos de switch, excepto el puerto de origen. Esto asegura que todos los dispositivos del dominio de broadcast puedan recibir la trama. **Si existe más de una ruta para enviar la trama, se puede generar un bucle sin fin.**

### Tormentas broadcast
Debido a que el **tráfico de broadcast se envía a todos los puertos del switch**, todos los dispositivos conectados deben **procesar todo el tráfico de broadcast** que fluye indefinidamente en la red con bucles. **Esto puede producir que el dispositivo final no funcione debido a los requerimientos de alto procesamiento** para sostener una carga de tráfico de esas dimensiones en la tarjeta de interfaz de red

### Tramas unicast duplicadas
1. La PC1 envía una trama de unicast con destino a la PC4.  
2. El switch S2 no cuenta con una entrada para la PC4 en su  
tabla MAC, de manera que envía la trama de unicast a  
todos los puertos de switch, en un intento de encontrar a la  
PC4.  
3. La trama llega a los switches S1 y S3.  
4. S1 no posee una entrada de dirección MAC para la PC4,  
de forma que reenvía la trama a la PC4.  
5. S3 también cuenta con una entrada en su tabla de  
direcciones MAC para la PC4, de manera que reenvía la  
trama de unicast a través del Enlace troncal3 a S1.  
6. S1 recibe la trama duplicada y una vez más la reenvía a  
la PC4.  
7. La PC4 ha recibido ahora la misma trama dos veces.


**Se refiere a cuando un equipo final recibe una trama de broadcast dos veces**

### Bucles en el armario de cableado


# Protocolo spanning tree (STP)
STP **asegura que exista solo una ruta logica** entre todos los destinos de la red, **al bloquear** de forma intencional **aquellas rutas redundantes** que puedan ocasiconar bucle


# STP compensa fallos
Si detecta que falla un enlace entonces busca otro camino para mandarlas tramas


# Algoritmo STP (STA)
- El STA designa un **unico switch como puente raiz** y lo utiliza como punto de referencia para todos los calculos de rutas

- Todos los switches que comparten STP intercambian tramas de BPDU para determinar el switch que posee el menor ID de puente (BID) en la red

- El switch con el menor BID se transforma en el puente raíz de forma automática según los cálculos del STA.

- El BID contiene un valor de prioridad, la dirección MAC del switch emisor y un ID de sistema extendido opcional.

- Después de determinar el puente raíz, el STA calcula la ruta más corta hacia el mismo

- Los costos de la ruta se calculan mediante los valores de costo de puerto asociados con las velocidades de los puertos para cada puerto de switch que atraviesa una ruta determinada.

---Examen--- 
**Puestos raiz** Los puertos de switch mas ceranos al puente raiz. Los principales, tiene el menor ID, todos los puertos estan en verde y los que no estan en una contienda para

**Puertos designados** Puertos que no son raices y que un pueden estar enviando trafico (Los que estan en verde)

**Puertos no designados** estan en rojos y esperando que haya una falla para entrar

------ 

# Puente raiz
Inicialmente, **cada switch se identifica a sí mismo como puente raíz** después del arranque.  
A medida que los switches envían sus tramas de BPDU, los switches adyacentes del dominio de broadcast leen la información del ID de raíz de la trama de BPDU.
**Si el ID de raíz de la BPDU recibida es menor que el ID de raíz del switch receptor, este último actualiza su ID de raíz mediante la identificación del switch adyacente como el puente raíz.**


# Puente raiz (Basado en prioridad)
El valor predetreminado de la prioridad es 32769 si encuentra a uno con un numero menor, se convertira en el raiz

Los valores pueden incrementar o de decremantar en 4096

# Puente raiz (Basado en direccion MAC)
Toma el menor valor de la mac tomado en HEXADECIMAL

# Comandos 
show spanning-tree 
spanning-tree vlan 1 priority 24576
spanning-tree vlan 1 root primary
spanning-tree vlan 1 root secundary

## Configurar prioridad del puerto

int fa0/2
spanning-tree port-priority 112 

## Tecnolofia PortFast de Cisco
### Que es PortFast?
No pasar por los diretentes estados, ponerlo de forma activa directamente

### Habilitar PortFast
Interface FastEthernet 0/11
spanning tree portgast

### Deshabilitar PortFast
Interface FastEthernet 0/11
no spanning tree portgast


