# Entrutamiento entre VLAN tradicional
Cada vlan que desees conectar, tiene que tener un medio fisico(Conectada a un puerto del router)
Puede llegar a ser caro

# Enrutamiento entre VLAM "Router-on-Stick"
Solo hay una interfaz fisica, por lo que se crean subinterfaces

# Enrutamiento entre VLAN basado en switch




# Practica
Para agregar mas puertos al router, se apaga y se arrastra el cfe

![[Pasted image 20220920091359.png]]

Si se agrega un gateway porque hay un router

Primer switch
![[Pasted image 20220920092123.png]]


Router
NOTA: Si esta el cable rojo es porque un cable esta mal o porque no hicimos no shut

![[Pasted image 20220920092634.png]]

DARLE NO SHUT

do show ip route - muestra tabla enrutamiento



Switch 2
![[Pasted image 20220920093854.png]]

Se devlara troncal para hacer que mande todas las VLAN 

Router 2
Creamos subdivisiones
![[Pasted image 20220920094336.png]]
NO SHUT

9/21/2022

![[Pasted image 20220921093151.png]]

![[Pasted image 20220921093336.png]]


![[Pasted image 20220921093538.png]]
![[Pasted image 20220921093825.png]]
Con esto hereda el cliente 1 las vlan

![[Pasted image 20220921094130.png]]

![[Pasted image 20220921094422.png]]

![[Pasted image 20220921094520.png]]

![[Pasted image 20220921094712.png]]

![[Pasted image 20220921094855.png]]


Declaramos troncales
![[Pasted image 20220921095021.png]]


9/22/2022
![[Pasted image 20220922091509.png]]


![[Pasted image 20220922092007.png]]
![[Pasted image 20220922092027.png]]
![[Pasted image 20220922092617.png]]






PASOS
Direccionar nodos finales
Fuimos al server y modifcamos le modo del vtp, dimos de alta al vlan
Fuimos a los clientes, y pusimos el modo vtp, enlaces troncales
Fuimos al router on stick, se declara troncal , el que va als sever se pone de manera tradicional


