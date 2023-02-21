Todos los metodos vistos en [[Modelos de procesos prescriptivos|el libro(2.3,2.5,3.4)]]
Buscan lo mismo, intentar encontrar una manera, una forma, un estandar de como crear Software, todas las formas son distintas, pero todos buscan crear Software de calidad, tanto para el lado del cliente como la del programadors.

#  Los pasos de los procesos:

## Comunicacion
## Planeacion 
## Modelado
### Analisis
#### Analisis de requerimientos
El análisis de los requerimientos da como resultado la **especificación de las características** operativas **del software**, **indica la interfaz** de éste y otros elementos del sistema, y **establece** las **restricciones** que limitan al software. El análisis de los requerimientos permite al profesional construir sobre los requerimientos básicos establecidos durante las tareas de concepción, indagación y negociación, que son parte de la ingeniería de los requerimientos .

#### Analisis del dominio
El análisis del dominio del software es la **identificación, análisis y especificación de los requerimientos comunes**, a partir de un dominio de aplicación específica, normalmente para usarlo varias veces en  
múltiples proyectos dentro del dominio de la aplicación \[**El análisis del dominio orientado a objetos es] la identificación, análisis y especificación de capacidades comunes y reutilizables dentro de un dominio de aplicación** específica en términos de objetos, clases, subensambles y estructuras comunes.

#### Reglas prácticas del análisis
- El modelo debe centrarse en los requerimientos que sean visibles dentro del problema o dentro del dominio del negocio. 

• Cada elemento del modelo de requerimientos debe agregarse al entendimiento general de los requerimientos del software y dar una visión del dominio de la información, de la función y del comportamiento del sistema.  

• Hay que retrasar las consideraciones de la infraestructura y otros modelos no funcionales hasta llegar a la etapa del diseño. 

- Es importante representar las relaciones entre las clases y funciones. Sin embargo, si el nivel de “interconectividad” es extremadamente alto, deben hacerse esfuerzos para reducirlo. 

• Cada actor tiene su propio uso para el modelo. 

• Mantener el modelo tan sencillo como se pueda. No genere diagramas adicionales si no  
agregan nueva información. No utilice notación compleja si basta una sencilla lista

### Diseño

#### Diseño de la arquitectura
Cuando comienza el diseño arquitectónico, el diseño debe definir las entidades externas con las que interactúa el software y la naturaleza de dicha interacción. Esta información por lo general se adquiere a partir del modelo de los requerimientos y de toda la que se reunió durante la ingeniería de éstos. Una vez que se ha modelado el contexto y descrito todas las interfaces externas del software, se identifica un conjunto de arquetipos de arquitectura. **Un arquetipo es una abstracción** (similar a una clase) que **representa un elemento de comportamiento del sistema**. Por tanto, el diseñador especifica la estructura del sistema, definiendo y refinando los componentes del software que implementan cada arquetipo. Este proceso sigue en forma iterativa hasta que se obtiene una estructura arquitectónica completa.

#### Diseño en el nivel de componentes
El diseño en el nivel de componentes tiene lugar una vez terminado el diseño de la arquitectura. En esta etapa se ha establecido la estructura general de los datos y del programa del software. **El objetivo es traducir el modelo del diseño a software operativo**. Pero el nivel de abstracción del modelo de diseño existente es relativamente alto y el del programa operativo es bajo. La traducción es difícil y está abierta a la introducción de errores sutiles que son difíciles de detectar y de corregir en las etapas posteriores del proceso del software

#### Diseño de la interfaz de usuario
Si un producto ha de alcanzar el éxito, debe tener buena usabilidad: medición cualitativa de la facilidad y eficiencia con la que un humano emplea las funciones y características que ofrece el producto de alta tecnología.

Para construir una interfaz de usuario eficaz, “todo diseño debe comenzar con la comprensión de los usuarios que se busca, lo que incluye los perfiles de edad, género, condiciones físicas, educación, antecedentes culturales o étnicos, motivación, metas y personalidad”. Además, los usuarios se clasifican como:  

Principiantes. 
Sin conocimiento sintáctico del sistema y poco conocimiento semántico de la aplicación o uso de la computadora en general.  

Usuarios intermitentes 
Con conocimiento semántico razonable de la aplicación,  
pero relativamente poco recuerdo de la información sintáctica necesaria para usar la interfaz.  

Usuarios frecuentes conocedores
Con buen conocimiento semántico y sintáctico, que con  
frecuencia les despierta el “síndrome del usuario poderoso”; es decir, individuos que buscan  
atajos y modos de interacción abreviados

#### Diseño basado en patrones
El diseño basado en patrones no se utiliza en el vacío. Los conceptos y técnicas analizados para  
el **diseño arquitectónico**, en el nivel de componentes y de la interfaz de usuario, se utilizan junto con un enfoque basado en patrones.  
Un conjunto de lineamientos y atributos de la calidad se emplean como la base para tomar todas las decisiones del diseño de software. Éstas reciben influencia  
de un conjunto de conceptos fundamentales del diseño (como la separación de problemas, mejora por etapas, independencia funcional, etc.) que se logran con el uso de heurísticos que han evolucionado a lo largo de muchas décadas, así como de las mejores prácticas (tales como las técnicas de notación de modelos) que se han propuesto para hacer que el diseño sea más fácil de realizar y que tenga más eficacia como base para la construcción

#### Diseño de WebApps


## Construccion

### Pruebas
Es la parte donde se hace presente la calidad
## Despliegue


![[Cascada.png]] 