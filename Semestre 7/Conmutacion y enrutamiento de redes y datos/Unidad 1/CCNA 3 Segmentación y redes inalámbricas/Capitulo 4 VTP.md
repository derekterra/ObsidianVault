# El desafio de administrar VLANs
Es un ortocolo de enlaces troncales para heredar las vlan(id, nombres), no los puertos, para evitar configurar muchos

# Que es el VTP?
Cuando se configura el dominio, empeiza a mandar publicaciones y heredar la informacion a otros switches

# Componentes del VTP
servidor: EL que manda la informacion
cliente: Son los hijos de los server
transparente: Un switch independiente que no hereda los demas, pero si tiene hijos, les pasa los mensajes

# Configuracion del VTP predeterminada
show vtp status

configuracion revision: Aumenta con cada modificacion que se ha hecho a las vlan


# Publicaciones en VTP
Publicaciones de resumenes:
- Se envian cada 5 minutos por Servidor VTP
- Informan a los switches habilitados con VTP sobre el numero de revision de la configuracion VTP actual
- Se envian indediantamente despues de un cambio en la configuracion

Los cambios que impulsa la publicacion de subconjunto incluyen:
- La cracion o eliminacion de una VLAN
- La suspension o activacion de una VLAN
- El cambio de nombre de una VLAN
- El cambio de la MTU de una VLAN

Cuando una publicacion de solicitud se envia al servidor VTP
- El servidor VTP envia una publicaicon de resumen
- Luego, el servidor VTP envia una publicacion de subconjunto



# Depuracion del VTP habilitada
vtp pruning

No gastar ancho de banda en mandar trafico a enlaces en donde no haya VLAN que reciban el trafico

# Guia de configuracion del VTP

En el servidor del VTP
- Confirme las configuraciones predeterminadas
- Configure 2 switches como servidores del VTP
- Configure el fominio de VTP en el primer switch de la red
- Asegurese de que todos los switches esten en el mismo modo de version del protocolo......
.....

# Detalles frecuentes en la configuracion VTP

# Practica

Server
![[Pasted image 20220915093331.png]]

![[Pasted image 20220915093344.png]]
Cliente1: no podremos configurar las vlan estando en modo cliente
![[Pasted image 20220915093303.png]]

Transparente
![[Pasted image 20220915093520.png]]

Cliente 2
![[Pasted image 20220915093713.png]]

Server
![[Pasted image 20220915094117.png]]

Cliente 1 ahora heredo las vlan del server
![[Pasted image 20220915094417.png]]

![[Pasted image 20220915094850.png]]
![[Pasted image 20220915095016.png]]


9/19/2022
# Configurar cliente2 y transparente

![[Pasted image 20220919091346.png]]
![[Pasted image 20220919091600.png]]

![[Pasted image 20220919093443.png]]
![[Pasted image 20220919093513.png]]
![[Pasted image 20220919093529.png]]



Si agregamos otra vlan el transparente evitara que se herede
El transparente heredara la 80, pero los demas no
![[Pasted image 20220919094540.png]]

En el server crearemos dos vlan que si se heredaran
![[Pasted image 20220919094504.png]]

Aqui se muestra
![[Pasted image 20220919094647.png]]