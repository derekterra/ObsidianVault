
# Que es una VLAN
Es una red LAN independiente
Una VLAN es una **subred IP separada de manera lógica**. Las VLAN permiten que redes de IP y subredes múltiples existan en la misma red conmutada.
Todos los dispositivos estan en la misma ip, pero estan divididas

# Beneficios de las VLANs
- Seguridad: los grupos que tienen datos sensibles se separan del resto de la red, disminuyendo las posibilidades de que ocurran violaciones de información confidencial. Las computadoras del cuerpo docente se encuentran en la VLAN 10 y están completamente separadas del tráfico de datos del Invitado y de los estudiantes.  

- Reducción de costo: el ahorro en el costo resulta de la poca necesidad de actualizaciones de red caras y más usos eficientes de enlaces y ancho de banda existente. 

- Mejor rendimiento: la división de las redes planas de Capa 2 en múltiples grupos lógicos de trabajo (dominios de broadcast) reduce el tráfico innecesario en la red y potencia el rendimiento. 

- Mitigación de la tormenta de broadcast: la división de una red en las VLAN reduce la cantidad de dispositivos que pueden participar en una tormenta de broadcast. Como se analizó en el capítulo "Configure un switch", la segmentación de LAN impide que una tormenta de broadcast se propague a toda la red. En la figura puede observar que, a pesar de que hay seis computadoras en esta red, hay sólo tres dominios de broadcast: Cuerpo docente, Estudiante y Invitado . 

- Mayor eficiencia del personal de TI: las VLAN facilitan el manejo de la red debido a que los usuarios con requerimientos similares de red comparten la misma VLAN. Cuando proporciona un switch nuevo, todas las políticas y procedimientos que ya se configuraron para la VLAN particular se implementan cuando se asignan los puertos. También es fácil para el personal de TI identificar la función de una VLAN proporcionándole un nombre. En la figura, para una identificación más fácil se nombró "Estudiante" a la VLAN 20, la VLAN 10 se podría nombrar"Cuerpo docente" y la VLAN 30 "Invitado ". 

- Administración de aplicación o de proyectos más simples: las VLAN agregan dispositivos de red y usuarios para admitir los requerimientos geográficos o comerciales. Tener funciones separadas hace que gestionar un proyecto o trabajar con una aplicación especializada sea más fácil, por ejemplo una plataforma de desarrollo de e-learning para el cuerpo docente. También es fácil determinar el alcance de los efectos de la actualización de los servicios de red.

# Caracteristicas de las VLANs

Las VLAN son motivo de seguridad  EXAMEN checar grabacion

ID de VLAN
- ID de campo normal
	- 1-1005
	- 1002-1005 se resevan para token ring y las FDDI 
	- 1 y 1002 a 1005 se crean automaticamente y no se pueden eliminar
	- Se guarda en el archivo vlan.dat en la memoria flash
- ID de campo ampliado
	- 1006 - 4094
	- Se disenan para los proveedores de servicios
	- Poseen menos opciones de las VLAN de campo normal
	- Se guardan en el archivo de configuracion en ejecucion
- Un switch Cisco Catalyst 2960 admite 255 VLAN de campo normal y ampliado 



## Tipos de VLAN

- VLAN de datos: Una VLAN de datos es una VLAN configurada para enviarsólo tráfico de datos generado por el usuario. Una VLAN podría enviar tráfico basado en voz o tráfico utilizado para administrar el switch, pero este tráfico no sería parte de una VLAN de datos.

- VLAN predeterminada: Todos los puertos de switch se convierten en un miembro de la VLAN predeterminada luego del arranque inicial del switch. Hacer participar a todos los puertos de switch en la VLAN predeterminada los hace a todos parte del mismo dominio de broadcast.

- VLAN nativa: Una VLAN nativa está asignada a un puerto troncal 802.1Q. Un puerto de enlace troncal 802.1 Q admite el tráfico que llega de muchas VLAN (tráfico etiquetado) como también el tráfico que no llega de una VLAN.

	La VLAN nativa, la que **se usa en enlaces troncales**, la que lleva toda la informacion de control, no lleva datos, utilizan el protocolo 2800q

- VLAN de administración: Una VLAN de administración es cualquier VLAN que usted configura para acceder a las capacidades de administración de un switch. La VLAN 1serviría como VLAN de administración si no definió proactivamente una VLAN única para que sirva como VLAN de administración. Se asigna una dirección IP y una máscara de subred a la VLAN de administración.

**VLAN de administracion, se usa para administrar los dispositivos de comunicacion **

- VLAN de voz: Es fácil apreciar por qué se necesita una VLAN separada para admitir la Voz sobre IP (VoIP). Imagine que está recibiendo una llamada de urgencia y de repente la calidad de la transmisión se distorsiona tanto que no puede comprender lo que está diciendo la persona que llama. El tráfico de VoIP requiere:  
	- Ancho de banda garantizado para asegurar la calidad de la voz 
	- Prioridad de la transmisión sobre los tipos de tráfico de la red  
	- Capacidad para ser enrutado en áreas congestionadas de la red  
	- Demora de menos de 150 milisegundos (ms) a través de la red

**VLAN de voz cuando tenemos conectado un telefono de voz, priorisa el trafico de voz**

Modo acces, de acceso de datos 
La predeterminada, es la 1, la que no se puede borrar


# Control de los dominios de broadcast
En funcionamiento normal, cuando un switch recibe una trama de broadcast en uno de sus puertos, envía la trama a todos los demás puertos. Como resultado, cuando la computadora del cuerpo docente, PC1, envía una trama de broadcast, el switch S2 envía esa trama de broadcast a todos sus puertos. La red completa la recibe finalmente; la red es un dominio de broadcast.


# Comunicación entre VLANs con ruteadores
Para crear las vlan necesitamos un dispositivo capa 3

# Comunicación entre VLANs con switch capa 3


# Enlaces troncales
**Es un enlace punto a punto**, entre dos dispositivos de red, que transporta más de una VLAN. Un enlace troncal de VLAN le permite extender las VLAN a través de toda una red. Cisco admite IEEE 802.1Q para la coordinación de enlaces troncales en interfaces Fast Ethernet y Gigabit Ethernet.

# Comunicación intra vlan sin troncales

# Comunicación intra vlan con troncales

# Detalles del campo de etiqueta de VLAN
Luego de que el switch inserta los campos de información de control de etiqueta y EtherType, vuelve a calcular los valores  
FCS y los inserta en la trama.

# VLAN nativa y enlace troncal 802.1Q

## Tramas etiquetadas en la VLAN nativa  
Algunos dispositivos que admiten enlaces troncales etiquetan la VLAN nativa como comportamiento predeterminado. Los dispositivos de otros proveedores que admiten tramas etiquetadas en la VLAN nativa incluyen: teléfonos IP, servidores, routers y switches que no pertenecen a Cisco.  

## Tramas sin etiquetar en la VLAN nativa  
Cuando un puerto de enlace troncal de switch Cisco recibe tramas sin etiquetar, éste envía esas tramas a la VLAN nativa.  
Si la VLAN nativa no ha sido  
configurada nuevamente, el valor de PVID se configura para la VLAN 1.

## Detalles del campo de etiqueta de VLAN

VLAN nativa y enlace troncal 802.1Q

Tramas con etiquetas 

Como se configura una VLAN nativa y el enlace troncal


## Modos de enlace troncal
Un puerto de switch en un switch de Cisco admite varios modos de enlaces troncales. El modo de enlace troncal define la  manera en la que el puerto negocia mediante la utilización del DTP para configurar un enlace troncal con su puerto par. A  continuación, se observa una breve descripción de los modos de enlaces troncales disponibles y la manera en que el DTP se implementa en cada uno.  

- Activado (de manera predeterminada) 
El puerto del switch envía periódicamente tramas de DTP, denominadas notificaciones, al puerto remoto. El comando utilizado es switchport mode trunk. El puerto de switch local notifica al puerto remoto que está cambiando dinámicamente a un estado de enlace troncal. Luego, el puerto local, sin importar la información de DTP que el puerto remoto envía como respuesta a la notificación, cambia al estado de enlace troncal. El puerto local se considera que está en un estado de enlace troncal (siempre activado) incondicional. 

- Dinámico automático  
El puerto del switch envía periódicamente tramas de DTP al puerto remoto. El comando utilizado es switchport mode  
dynamic auto. El puerto de switch local notifica al puerto de switch remoto que puede establecer enlaces troncales pero no solicita pasar al estado de enlace troncal. Luego de una negociación de DTP, el puerto local termina en estado de enlace troncal sólo si el modo de enlace troncal del puerto remoto ha sido configurado para estar activo o si es conveniente. Si ambos puertos en los switches se configuran en automático, no negocian para estar en un estado de enlace troncal.  
Negocian para estar en estado de modo de acceso (sin enlace troncal).  

- Las tramas de DTP convenientes y dinámicas 
Las tramas de DTP se envían periódicamente al puerto remoto. El comando utilizado es switchport mode dynamic desirable. El puerto de switch local notifica al puerto de switch remoto que puede establecer enlaces troncales y solicita al  puerto de switch remoto pasar al estado de enlace troncal. Si el puerto local detecta que el remoto ha sido configurado en modo activado, conveniente o automático, el puerto local termina en estado de enlace troncal. Si el puerto de switch remoto  
está en modo sin negociación, el puerto de switch local permanece como puerto sin enlace troncal. 

- Desactivación del DTP  
Puede desactivar el DTP para el enlace troncal para que el puerto local no envíe tramas de DTP al puerto remoto. Utilice el  
comando switchport nonegotiate. Entonces el puerto local se considera que está en un estado de enlace troncal  
incondicional. Utilice esta característica cuando necesite configurar un enlace troncal con un switch de otro proveedor.


# Crear VLAN
## 1. Crear las VLAN


## 2. Asociar puertos a cada VLAN

## 3. Verificar VLANs y puertos asociados

## 4. Configurar enlaces troncales

## 5. Verificar configuracion de enlaces troncales

### Quitar modo troncal y VLANs permitidas

### Comunicacion intra vlan si troncales
Se refiere a que una vlan tiene un puerto para cada uno de los puertos


9/12/2022

NOTA: Siempre guardar como /24
