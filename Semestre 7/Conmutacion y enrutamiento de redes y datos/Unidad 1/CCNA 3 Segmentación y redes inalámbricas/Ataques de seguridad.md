Saturación de la dirección MAC
Por parte de la WAN somos mas suceptibles a ataques


## Suplantación de identidad 
1. Un aracante activa un servidor de DHCP en un segmento de red.
2. El cliente envia un broadcast de solicitud de infromacion de configuracion de DHCP.
3. El sergvudor de DHCP malicioso responde antes de que lo haga  el servidor de DHCP legitimi y asigna informacion 


Para evitar esto se ejecuta el snooping
con el comando ip dhcp snooping
Se asignan cuales son los aquellos puertos confiables y solamente el puerto que tiene el servidor puede transmitir esto.

## Ataque de CDP
CDP: Protocolo que permite descubrir redes. Permite contruir el esquema sin necesidad de conocer nada de la red. Permite conocer a los vecinos de los aparatos que estan conectados.

Si esta activo, puede verse todo lo que mandas y de donde a donde se manda, por lo que se recomienda mejor desabilitarlo

NOTA: wireshark programa de hackers

## Ataques Telnet
Tipos de ataques de Telncet
- Ataques de contraseña de fuerza burta
- Ataque DoS

Protección contra un ataque de contraseña de fuerza bruta:
- Cambie su contraseña con frecuencia
- Utilice contraseñas fuertes
- Limite la cantidad de usuarios que puedan comunicarse con las lineas vty

## Herramientas de seguridad
Realizan las siguientes funciones:
- Las auditorias de seguridad de red ayudan a
	-  Revelar que tipo de informacion puede recopilar un atacante mediante un simple monitoreo del tradico de la red
	- Determinar la cantidad ideal de direcciones MAC falsas que deben elominarse
	- Determinar el periodo de expiracion de la tabla de direcciones MAC
- Las pruebas de penetracion a la red

## Configuracion de la seguridad de puerto
Se implementa seguirdad en todos los puertos de switch para:
- Especificar un grupo de direcciones MAC validas permitidas en el puerto
- Permitir que solo una direccion MAC accesa al puerto
- Especificar que el puerto se desativa de manera automatica si se detectan direcciones MAC no autorizadas

## Tipos de direcciones MAC seguras
- Direcciones MAC seguras estáticas:
- Direcciones MAC seguras dinámicas
- Direcciones MAS seguras sin modificación

## Tipos de violaciones
Modo de violacion | Envio de trafico | Envia un mesnaje de Syslog | sd
--------|----------

## Opciones predetrminadas de la seguridad del puerto

## Configuracion de la seguridad del puerto

confugure terminal - modificacion del dispositivo
switchport port-security- HAY QUE DARLE ENTER ANTES DE CONFIGURAR LO DEMAS

## Verificar la seguridad del puerto por interfaz
show port-security

## Verificar la seguridad del puerto por mac
how port-security address

