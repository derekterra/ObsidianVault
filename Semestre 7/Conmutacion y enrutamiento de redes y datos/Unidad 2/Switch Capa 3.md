![[Pasted image 20220928090704.png]]

![[Pasted image 20220928090916.png]]

![[Pasted image 20220928091152.png]]
![[Pasted image 20220928091716.png]]

![[Pasted image 20220928091825.png]]

![[Pasted image 20220928091923.png]]

![[Pasted image 20220928092041.png]]

![[Pasted image 20220928092235.png]]

Con lo siguiente ya deberian heredar las vlan
![[Pasted image 20220928092443.png]]

![[Pasted image 20220928092524.png]]

![[Pasted image 20220928092743.png]]
![[Pasted image 20220928092807.png]]


![[Pasted image 20220928093057.png]]


![[Pasted image 20220928093118.png]]



![[Pasted image 20220928093328.png]]

![[Pasted image 20220928093635.png]]
![[Pasted image 20220928093916.png]]


Con esto ya hace ping entre diferente vlan
![[Pasted image 20220928093902.png]]
![[Pasted image 20220928094109.png]]


Para agregar la interfaz con el router tenemos que especificar que no lo trate como Switch

![[Pasted image 20220928094458.png]]

![[Pasted image 20220928094639.png]]



![[Pasted image 20220928095017.png]]
![[Pasted image 20220928095029.png]]


![[Pasted image 20220928095228.png]]
![[Pasted image 20220928095242.png]]

29/9/2022

Protocolo Spanning tree

Como todos tienen la misma prioridad elige la que tenga MAC menor

![[Pasted image 20220929093126.png]]


Para saber cual es el raiz te apaorece un mensaje
![[Pasted image 20220929093825.png]]

Poner el que tu quieras como spanning tree
![[Pasted image 20220929094650.png]]

![[Pasted image 20220929094704.png]]





![[Pasted image 20220929094616.png]]


![[Pasted image 20220929094633.png]]





Forazar los caminos por cierto puerto
![[Pasted image 20220929094928.png]]

![[Pasted image 20220929095416.png]]

SWITCH 3
SPANNING TREE (TEORIA Y PRACTICA)
WI FI (TEORIA Y PRACTICA)
ETHERNCHARNEL


# Capitulo 7 Redes inalambricas

## Tecnologias inalabricas
Es una extension de una red guiada(cableada)
Se caracterizan por su area de alcance:
WPAN
WMAN
WLAN
WWAN


## Comparacion entre un WLAN y una LAN
## pUNTO DE ACCESO Y RUTEADORES INALAMBRICOS
Diferencia? La capa donde funciona

## Estandares inalambricos EXAMEN
Todos lo diferentes estandares que hay, 
Actualemnte usan la ac
regula la frecunecia en la que trabajamos las qwue trabajan al 2.4 son tarjatas con mahypor interferencia, trabajan mas dispositivos inalabricos, por ejemplo microondas o celulares pueden interferir

## Certificaciones WI-FI
### ITU-R 
regula la asignación del espectro RF y órbitas satelitales. Éstos se describen  
como recursos naturales finitos que se encuentran en demanda por parte de  
clientes, como redes inalámbricas fijas, redes inalámbricas móviles y sistemas de posicionamiento global.

### IEEE 
desarrolló y mantiene los estándares para redes de área local metropolitanas con la familia de estándares IEEE 802 LAN/MAN. El IEEE 802 es administrado por el comité de estándares IEEE 802 LAN/MAN (LMSC), que supervisa múltiples grupos de trabajo. Los estándares dominantes en la familia IEEE 802 son 802.3 Ethernet, 802.5 Token Ring, y 802.11 LAN inalámbrica

### WIFI Alliance 
es una asociación de proveedores cuyo objetivo es mejorar la interoperabilidad de productos que están basados en el estándar 802.11, y certifica proveedores en conformidad con las normas de la industria y adhesión a los estándares. La certificación incluye las tres tecnologías RF IEEE 802.11, así como la  
adopción temprana de los borradores pendientes de la IEEE, como el estándar 802.11n, y los estándares de seguridad WPA y WPA2 basados en IEEE 802.11i

## CSMA/CA
Previene colisiones por medio del acces point 

### Topologias 802.11
Ad hoc - no hay punto de acceso o router o acces point (Laptop con laptop o play con play)

Ingraestructura -  Conexion a traves de un punto de acceso

## Proceso de descubrimiento de WLAN
Beacons - cuando el punto de acceso anuncia su presencia en la red, manda beacons

Sondas 

Autentitication selecciona una red y das la contrasena

Asosiacion, se da el permiso, se te da una IP dinamica y listo

## Encriptacion
TKIP - Clave de integridad de clabe temporal

AES - Estandar de encriptacion avanzada, siempre intentar escoger

## Operacion de una WLAN
Cuidado se superponer canales

## Configuracion del punto de acceso

pasos para hacerlo
vamos a internet y red en la computadora
Wi fi
Mostrar redes disponible
Agregar una nueva red
Y se agrega manualmente poniendo un nombre y el tipo de seguiridad (Abierta, WEP, etc...)

# Planificacion de una WLAN 
El numero de usuarios de
La didtribucion geografoca de sus intancias 


ESS extendi video cuando tengamos varios puntos de acceso

## Ejemplo


# Seguridad LAN inalambrica
## Ataques de seguridad
En los medios inalabricos al ser un lugar donde cualquiera se pude meter y atacarnos

### Acceso no autorizado
- Buscadores de redes inalambricas abiertas
Encuentran Redes abiertas, las utilizan para conseguir acceso gratis a internet

- Piratas informaticos
Explotan medidas de pribacidad debiles para ver infomracion de WLAN sensible e incluso ingresa sin autoizacion a las WLAN

- Empleados 
Enchufan las APL/gateways de calidad comercial a los puntos ethernet de la compania para crear sus pripias WLAN

# Protocolos inalambricos
## Descripcion general del prtocolo inalabrico

## Pasos para proteger una WLAN
- Acceso abierto
	- SSID
		- Sin encriptacion
		- Autentificacion basica
		- Manejo no seguro
	- WEP
		- Sin autorizacion fuerte
		- Claves estaticas fragiles
		- No escalable
	- WPA 
		- Estandarizad
		- Encriptacion mejorada
		- Autentidicacion fuerte, basada en el usuario (por ejemplo, LEAP, PEAP,EAP-FAST)
	- 802.11WPA2
		- Encriptacion AES
		- Autentidicacion 802.1X
		- Es la mejor de todas
		- Administracion de clabe dinamica
		- WPA2 es la omplemenvacion de WIFI

# Proteger las red contra amenazas
## Control del acceso a la LAN inalámbrica
El cifrado aes

# Resolucion de problemas en WIFI
Siempre intentar checar todo lo fisico y despues irte a la logico

# Actualizar firmware para resolver problemas
Se recomienda nomas descargarlo cuando sea necesario solamente, ciando no hay nada mas que hacer

# Problem...

# Problemas de interferencias
Los microondas y telefonos inalambricos no estan en ESS y podrian cometer problemas de interfenecia

# Mala ubicacion de los puntos de acceso
Alineacion de las antenas e infraestructura

# Problema con autentificacion ...

# Practica wi fi y ehterchanel
![[Pasted image 20221005091948.png]]![[Pasted image 20221005091948 1.png]]
![[Pasted image 20221005092503.png]]


![[Pasted image 20221005092643.png]]


![[Pasted image 20221005092743.png]]

Asociar puertos servidor

![[Pasted image 20221005092900.png]]

Router on stick poner troncales

![[Pasted image 20221005093020.png]]
![[Pasted image 20221005093047.png]]


Checar que se hereadon en cliente 1
![[Pasted image 20221005093142.png]]

![[Pasted image 20221005093409.png]]

![[Pasted image 20221005093417.png]]

Asociar puertos en cleinte 1
![[Pasted image 20221005093717.png]]

![[Pasted image 20221005093736.png]]


Cliente 2 checar si se heredan

Cliente 2 dar de admin
![[Pasted image 20221005093849.png]]

Cliente 2 asociar puertos
![[Pasted image 20221005093959.png]]

Cliente 2 asociar troncales
![[Pasted image 20221005094059.png]]

ETHERCHANNEL si tenemos mucho trafico y es un anidado de enlace e incrementa el rendimiento 


10/6/2022
Configurar etherchannel


LACP - abierto

PAgP - de cisco, se usa cuando todos son cisco


![[Pasted image 20221006090927.png]]

![[Pasted image 20221006091244.png]]

![[Pasted image 20221006091543.png]]

do copy run sta  para guardar, hay que reiniciar para que los cmabios se hagan presentes


ahora lo comprobamos

![[Pasted image 20221006092004.png]]


![[Pasted image 20221006092113.png]]

--------------

Ahora lo haremos con el pagp borrando todo
![[Pasted image 20221006092304.png]]




![[Pasted image 20221006092524.png]]




![[Pasted image 20221006092607.png]]

![[Pasted image 20221006092652.png]]

no shutdown en ambas, ponerlo para levnatarlo


Comenzamos a configurar desde el principio
![[Pasted image 20221006093045.png]]

![[Pasted image 20221006093201.png]]
![[Pasted image 20221006093304.png]]

Se comprueba con un show et po 
y el show et su


------------

continuamos con lo dems que falta
![[Pasted image 20221006093806.png]]



![[Pasted image 20221006093932.png]]
Confuguramos esto

![[Pasted image 20221006094029.png]]

![[Pasted image 20221006094337.png]]

![[Pasted image 20221006094447.png]]
Se pone esto cuando hay una salida a internet



![[Pasted image 20221006094610.png]]



Configurar wi fi
dentro del router
![[Pasted image 20221006094946.png]]


![[Pasted image 20221006095053.png]]

![[Pasted image 20221006095206.png]]


Demo click en guardar


![[Pasted image 20221006095410.png]]
tec2 es el nombre con el que sse propaga

Damos click en guardar



![[Pasted image 20221006095523.png]]
Se pone una contrasena, el tipo de encriptacion, etc


![[Pasted image 20221006095723.png]]
Contrasena cisco


![[Pasted image 20221006095814.png]]
apagamos Ponemos el WCP300N yh prendemos

En configuraion nos conetamos en esta pantalla

![[Pasted image 20221006095938.png]]

Ponemos contrasena


Se activo



Hacemos lo mismo 
10.X.0.0 
X numero de control


EXAMEN 
STP 
Switch capa 3 
Etherchannel
Wi Fi (IP Route para salir hacia afuera)
Enlace hace Internet (WAN)
VTP


Teorico 
STP 
WIFI

NOTA EN ROUTER SE PONE EL NO SHUT


