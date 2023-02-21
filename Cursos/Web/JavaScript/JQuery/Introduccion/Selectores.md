Los selectores te permite manipular elementos HTML 
Buscan elementos HTML segun su nombre, id, clase, tipo, atributos, valores, atributos, etc

# Elemento

```
$("p")
```

Ejemplo
```
$(document).ready(function(){  
  $("button").click(function(){  
    $("p").hide();  
  });  
});
```

# Id

```
$("#test")
```

```
$(document).ready(function(){  
  $("button").click(function(){  
    $("#test").hide();  
  });  
});
```

# .class
```
$(".test")
```

```
$(document).ready(function(){  
  $("button").click(function(){  
    $(".test").hide();  
  });  
});
```