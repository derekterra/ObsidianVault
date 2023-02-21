La sintaxis es sencilla, selecionas un elemento html y realizar una accion hacia ese elemento

**$(_selector_)._action_()**
- Un signo $ para definir/acceder a jQuery
- Un (selector) para "consultar (o encontrar)" elementos HTML
- Una acción jQuery () que se realizará en los elementos

Ejemplo:

```
$(this).hide() - oculta el elemento actual.

$("p").hide() - oculta todos los elementos <p>.

$(".test").hide() - oculta todos los elementos con class="test".

$("#test").hide() - oculta el elemento con id="test".
```

# Documento al empezar 
```
$(document).ready(function(){  
  
  // jQuery methods go here..._  
  
});
```
Este metodo permite cargar todo el codigo de jquery una vez que se haya completado la carga de la pagina 