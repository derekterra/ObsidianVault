-ipconfig - checar la direccion ip
-ipconfig /all - checar todos los datos, incluso la mac 
ping - se hace manda un paquete a la ip que correspondas

## Configurar el switch
Se puede hacer directo desde el cisco, pero originalemente se hace desde la consola de una PC

ena - Para acceder al modo privilegiado del Switch 

conf ter -Acceder a la configuracion del Switch

hos [nombre que quieras cambiar] 

### Poner password a la consola
Estando dentro de la configuracion del switch 

-line con 0 
-password [contrasena a poner] 
-login - para que la pida cada que se logeen

### Poner password sobre las lineas virtuales (telnet)
-line vty 0 15
-pass [contrasena a poner]
-login - para que la pida cada que se logeen

### Poner password para pasar de modo usuario a privilegiado
-ena sec [contrasena]

### Ejecutar comandos que son de raiz
Se hace con el do [comando de raiz] asi no se tiene que volver al principio 

### Reiniciar
do reload

### Mostrar las configuraciones que hemos hecho
show running-config

### Como cifrar nuestras contrasenas y que no aparezcan en show running-config
service password-encryption

### Configurar la velocidad de un router
En la configuracion seleccionaremos el puerto que queramos realizar los cambios
-int fa0/6

y manejaremos la opcion de duplex en automatico
-duplex auto

y finalmente pondremos la velocidad en automatioc
-speed auto




 
-vlan para dar de alta una vlan junto con el id
vlan ? - dice todas las vlan
vlan junto con el id - creas una id
name - es opcional, pero se recomienda para saber que se usa la vlan
int vlan 50, es la interface de la vlan
ip add [direccion ip] [mask] - asigna direccion id
do show vlan brief - muestra todas las vlan
 -Asociar un puerto a una vlan


9/8/2022
