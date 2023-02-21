Lenguaje de programacion devlarativo. Los lenguajes declaratico se diferenciam de los lenguajes imperativos o procedurales en que estan basados en fomralismos abstractos (Prolog esta basado en la logica de predicados de primer orden).
- ventaja....

Es un programa muy util para resolver problemas que implican objetos y relaciones entre objetos

La sintaxis del lemjuaje consiste en lo sogioente:
- Declarar hechos sobre objetos y sus relaciones
- Hacer preguntas sobre objetos y sus relaciones
- Definir reglas sobre objetos y sus relaciones

Los hechos no tienen que reglejar el mundo real necesariamente, pero será unica y exlusivamente lp que prolo tomara como verdadero (Dominio del problema)

Un conjunto ........

Sobre un conjunto de hechos se puede realizar una seire de preguntas.
Prolog busca automaticamente en la base de datos si existe un hecho que se puede unificar (Es deicr, tiene el mismo nombre de predicado, el mismo numero de argumentos - o aridad - y cada uno de los argumentos tiene el mismo nombre, uno a uno) con el hecho ..........

Prolog contestará "SI" si encuentra ese hecho y "NO" si no la encuentra. La contestacion NO" no implica que el hecho sea falso (Aunque si lo sea para nuestrra base de datos ), sino que no se puede probar (en general) que sea verdadero con ek conocimiento almacenado en la base de datos,

## objetos
- propiedades
- relacionales

## Reglas
## Clausula de Horn
p(t1,t2,...,tn):-p1(...),p2(...),...,pm(...) con m>=0

Donde tanto p como las pi son sombolos predicados cpn suss argumentos entre parentesis. A los argumentos de un predicao se les denomina Terminos

Las clausalas de horn son expresiones condicionales, siendo e simobolo ":=" el condicional o simbolo de la implicacion (normalmente en logica se utiliza el simbolo "<-"). Asi la clausula enterior podria leerse de la siguiente forma: ...................

Cuando m=0, la clausula no tiene parte derecha, en este caso diremos que se trata de un hecho o afirmacion

p().................................


## Clausulas 
Hechos (afirmaciones), pueden representar:
- Objetos
- Propiedades de 
- ................................


## Hechos 
Es el mecanimo basico para representar:
- Objetos/personas/conceptos. padre(luis)
- Propiedades de los objetos. azul(cielo)
- relaciones entre los objetos. ...........

## Reglas
Oermiten establecer relaciones mas elaboradas entre objetos, por ejemplo, relaciones generalizadas o particularizadas, o relaciones casua efecto
padre(X) :- padre_de(X,Y)
padre(X) :- padre_de(X,\_)
hijo_de(X,Y) :- padre_de(Y,X)


# Ejecicio de padre y madre 
padre(enrique7,enrique 8)
padre(enrique7,arturo)
padre(enrique7,margarita)
padre(enrique8,maria)
padre(enrique8,isabel)
padre(enrique8,eduardo)
madre(catalina,maria)
madre(ana,isabel)
madre(juana,eduardo)