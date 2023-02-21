# Estructura monolitica
- La construccion del programa final es a vase de modulos complilados separadamente y que se unen a traves de un ligador. Carecen de protecciones y privilegios al manejar recursos como memoria y disco duro.

- Es muy comun: No existe estructura principalmente dicha o es minima

- El S.O. es una coleccion de precedimientos que se pueden llamar entre si

- Cada procedimiento tiene una interfaz bien definida en terminos de parametros y resultados

# Estructura jerarquica p sistema de capas
- El sistam operativo contiene subpartes y esta organizado en forma de nivelles o capas

- Es una genralizacion del modelo de estrucutra simple para un sistema monolitoco

- Consiste en organizar el s.o. como una rearquia de capas, cada una construida sobre la inmediata inferior

# Estructura maquina virtual
- Presenta una interfaz a cada proceso mostrando una maquina que oarece identica a la maquina real subyacente. Se reparan los conceptos que suele estar unidos en el resto del sistema. La multiprogramacion y la maquina extendida

- Las maquinas cirtuales intrumentan copias "exactas" del hardware simple, con su modo nucleo/usuario, e/s, interrupciones y todo lo demas que posee una maquina real

- Pueden ejecutar cualquier S.O. que se ejecute en forma directa sobre el hardware

- Las distintas maquinas virtuales pueden ehecutar disntintos S.O y en general si lo haven

- Soportan perifericos virtuales.


# Estructura cliente servidor
- Sirve para toda clase de aplicaciones y el proposito de este es de tipo general cumpliendo asi con las mismas actividades de los otros sistemas operativos.

- Su nucelo esta designado a establecer comunicacion entre los cliente y servidroes. Los precesos pueden ser tanto servidores como cliente a su vez el cliente actual como serviodro para otro proceos

- El proceso del usuario (proceso cliente) envia la solicitud a un proceso servidor:
	- Realiza el trabajo y regresa la respuesta

- El nucleo controla la comunicacion entre los clientes y los servidores

- Los servidores se ejecutan como precosos en modo usario:

	- No tienen acceso directo al hardware
	- Se aislan y acotan mas facilmente los problemas

- Se adapta para su uso 


# Clasificacion de los sistemas operativos por servicios
## Monousuario

Soportan un usuario a la vez sin importar los procesadores que tenga la computadora o los procesos y tareas que el usuario puede realizar al mismo tiempo. Ejemplo: Celulares, tabletas, PC

## Multiusuario

Ofrece servicio a más de un usuario a la vez ya sea por medio de terminales o secciones remotas en una red. No importa la cantidad de procesadores que tenga la maquina ni la cantidad procesos que se realicen a la misma

## Monotarea

Permite una tarea a la vez por usuario, aunque hallar ma de un usuario a la misma vez solo permitirá una tarea por usuario.

## Multitarea

Permite al usuario realizar varias tareas a la misma vez

## Uniproceso

Maneja solamente un procesador de la computadora. Si tuviera más de uno seria inútil

## Multiproceso

Puede manejar más de un procesador distribuyendo la carga simétrica y simétrica


## Por la forma que ofrecen sus servicios
### Sistema operativo de red
Interactuan con otras computadoras a traves de un medio transmision que intercambia informacion, transfiere archivo, ejecutar comandos remotos y otras tareas
### Sistema operativos distribuidos
Incluyenlos servicios que ofrece los sistemas operativos de red incluyen o añade recursos (impresoras, unidades de respaldo, memoria, procesos y unidad central de proceso) adicionales en una sola maquina virual que el usuario accesa de fomra transpartente