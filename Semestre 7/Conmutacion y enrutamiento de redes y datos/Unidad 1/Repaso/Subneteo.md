# Subneteo
La mascara de subred se demuestra decimalmente como
  
255.255.255.255 ó 11111111.11111111.11111111.11111111

En el que 255 (en binario serian 8 digitos) es el numero maximo a alcanzar

La notacion CIDR muestra el numero de "1´s" que se tiene por ejemplo /26 serian 11111111.11111111.11111111.11000000

## Maximo numero de host

El numero maximo de host se saca con el numero de ceros que hay en el subneteo

11111111.11111111.11111000.00000000

Aqui hay 11 "0´s" 2^11 = 2048 se le resta dos y tenemos el numero maximo de host que seria 2046



9/1/22
192.168.10.0

192.168 - Es una clase C
10 - Puede ir desde 0 hasta 255
0 - Representa la red, no se puede usar el 0 ni el 255 , el 255 es la direccion boradcast, lo que nos deja con 253 direcciones para usar (1-254)

La mascara:
192.168.10.1 
255.255.255.0 -> /24 

La diagonal muestra el numero de '1' que tiene la 


