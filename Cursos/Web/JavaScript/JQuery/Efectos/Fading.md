Se puede aplicar desvanecimiento a los elementos del HTML

# fadeIn()
Se usa para desvanecer un elemento HTML

```
$("button").click(function(){  
  $("#div1").fadeIn();  
  $("#div2").fadeIn("slow");  
  $("#div3").fadeIn(3000);  
});
```

# fadeOut() 
Se usa para hacer aparecer elementos previamente desvanecidos

```
$("button").click(function(){  
  $("#div1").fadeOut();  
  $("#div2").fadeOut("slow");  
  $("#div3").fadeOut(3000);  
});
```
``

# fadeToggle()
Se usa para intercalar entre desvanecido y aparecer

```
$("button").click(function(){  
  $("#div1").fadeToggle();  
  $("#div2").fadeToggle("slow");  
  $("#div3").fadeToggle(3000);  
});
```

# fadeTo()
Se usa para elegir que tanto desvanecimiento se desea en el objeto

```
$("button").click(function(){  
  $("#div1").fadeTo("slow", 0.15);  
  $("#div2").fadeTo("slow", 0.4);  
  $("#div3").fadeTo("slow", 0.7);  
});
```