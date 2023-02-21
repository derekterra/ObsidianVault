Una particion es dividir un disco en diferentes partes
No se pude dividir mas de 4 particiones primarias

Las particiones extendidas
Son unidades logicas

A cada particion se le debe agregar un formato de archivos

Tipos de discos
Discos basicos: Este es el formato basico en que windoes reconoce y añade uniades de disco duro en el sistema. Se puede generar adicionalmente particiones primarias o extenidadas dentro de estos volumentos logicos

Discos dinamicos: Microsoft implemento esta opcion para dar soporte a los sstemas con tolerancia de fallos que usan varios discos duros. La direncia entre 


# Tipos de volumenes
Simple
	Un disco que permite crear particiones
Distribuido
	Dinamico que amplia el volumen

Seccionado Raid - 0
Reflejado Raid - 1
Raid  - 5

# Raid
Grupo redundante de discos independientes, si uno se descompone otro lo reemplaza

## Ventajas
Suma las capacidades de los discos conectados creando asi un solo volumne

Incrementa la velocidad de acceso rompiendo los datos en varios bloques en su lectura/escrituura en varios discos en paralelo

Cuando se utiliza un RAID, la velocidad de almacenamiento incremnete cuantos mas discos se añadan

Ofrece tolerencia a fallos a traves de opreaciones espejo y de paridad

## Como funciona un Raid

## Data Striping
La informacion es dividida en multiples discos formando asi una unidad simple logica de almacenamiento. Cada espacio de los discos es dividido

## Mirroring / Espejo
Usado en los nivlees de RAID 1 y 1+0 pra la recuperacion de datos. Los datos son duplicados

## Paridad
Ademas de dividir los discos, en cada disco agrega informacion de paridad. En caso de perdida de un disco, la unformacion de parudad se combina con la informacion en los discos restatens para generar la informacion perdida.

## Tipos de RAID
RAID 0 - striping
Esta configuracion tiene dicision, pero no redundancia de datos. Ofrece el mejor rendimiento, pero sin rolerancia a fallos

Raid 1 - mirroring
Son dos discos con la misma infromacion, si uno falla el otro entra

RAID 5 - striping with parity

Se basa en la semgentacion a nivel de vloque con paridad. La informacion de paridad se divide en cada unidad


RAID 6 - striping with double parity

RAID 10 - combining mirroring and striping
Ofrece mayor rendimiento que RAID 1, pero por un coste mayor. En RAID 1+0, los datos se duplican y los espejos se dividen