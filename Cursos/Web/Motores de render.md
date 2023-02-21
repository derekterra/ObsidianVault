Los motores de renderizado son programas que **traducen nuestro código en un lenguaje que entienda el navegador**, de esta manera el programa sabrá que es lo que tiene que mostrar por pantalla al usuario.

## ¿Cuáles son los motores del navegador?

Los navegadores tienen sus propios motores: Chrome - Blink, Edge - Edge HTML, Safari - Webkit y Firefox - Gecko. **Todos realizan esta compilación de manera diferente, pero con el mismo resultado**, es decir, convierten los archivos a píxeles.

![Motores de los navegadores comunes](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/frontend_developer03.png)

## Proceso de renderizado del motor del navegador

**El motor del navegador realiza 5 pasos o procesos para compilar nuestro código hasta el renderizado por pantalla.** Estos pasos son los siguientes:

1.  Transforma los **archivos a un árbol de objetos** HTML o CSS, estos se denominan DOM (Document Object Model) y CSSDOM (Cascade Style Sheet Object Model), respectivamente. Cada nodo en el árbol es una representación de los elementos que contiene el archivo HTML o CSS.
2.  **Calcula el estilo** correspondiente a cada nodo del DOM relacionado al CSSDOM.
3.  **Calcula las dimensiones** de cada nodo y dónde va en la pantalla.
4.  Pinta o renderiza los diferentes elementos como **cajas o contenedores**.
5.  Agrupa todas las cajas en diferentes capas para **convertirlas en una imagen que se renderiza en pantalla**.

![Proceso de renderizado del navegador](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/frontend_developer04.png)