    representacion rango cant.redes  cant. nodos mascara dir privado

Clase A | X.0.0.0 | 0-127 O 1-126 | -

Clase B

Clase C


clase A | Clase B | Clase C |

EXAMEN


Subredes de longitud fija


10/19/22

NOTA:
Para borrar todas las VLAN # delete flash:vlan.dat

R1# show controllers serial 0/0/0
Interface Serial0/0/0
Hardware is PowerQUICC MPC860
DCE V.35

EXAMEN: Principios de la tabla de enrutamiento

# Metricas para encontrar la mejor ruta

EXAMEN 
Retardo: Cuanto tarda en llegar en milisegundos
Carga: 
Confiabilidad: Que tanto se cae, 

# Balanceo de saltos en comparacion con ancho de banda


# Balanceo de carga con el mismo costo

# Determinacion de la ruta
El envio de paquete supone dos funciones:
- Funcion de determinacion de ruta
- Funcion de conmutacion

dETERMINAR LA RUTA ES COMPARAR LA RUTA DESTINO CON LA LISTA DE RUTAS QUE SE TIENE 

# Protocolo CDP
NO VIENE EN EL EXAMEN
show cdp ne - si no tienes password no te deja 



line con 0 
pass cisco
login
ena se class
cdp run - lo pones a correr


Sirver para conocer a tu red, contruir tu mapa para ver como es que esta conectada toda la red

# Enrutamiento estatico
Un estatico no maneja ancho de bando

Cuando combiene ? Cuando son pocos rutas, cuando es una sola salida hacia internet  y cuando sea una topologia hub and spoke (Todos tienen el mismo vecino)

# Configuracion de rutas estaticas
Cuando haya un ISP(va a haber internet, todas las rutas tienen que mandar hacia donde haya internet

NO SE PUEDE USAR DOS RUTAS EN UN SOLO ROUTER
EL ISP NO PUEDE SER ESTATICO

# Ejemplo configuracion rutas estaticas

# Rutas estaticas e interfases Ethernet 
Siempre dar interfaz de salida a menos que....

# Resumen de rutas

# Ruta por defecto
ip route 0.0.0.0................

# Revision de problemas en rutas
ping
traceroute
show ip route
...................