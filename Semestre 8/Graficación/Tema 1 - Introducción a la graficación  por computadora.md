- Se refiere a usar la computadora para crear y manipular imagenes en un monitor
- Consiste en tecnicas que se usan con software para crear, almacenar , manipular y mostrar dichas imagenes (EXAMEN)

# Historia
## 1950 Osciloscopio
Primeras imagenes graficas creadas de manera analogica 

## 1955 Light pen (Light Gun)
Detecta cambios de brillo de pixeles vecinos en monitores CRT, para luego realizar acciones.

## 1960s Metodo del elemento finito
- Permite simular productos para probarlos antes siquiera de contruir el prototipo
- Se sigue usando hasta la fecha del dia de hoy

### Metodo del elemento finito
Gemoetria: Se genera un modelo en 3D 
Mallado: Se genera un modelo 3D en triangulos
Resolcer: Por magia matematica se genera un mocelo que te marca los lugares que debes de verificar
Visualizar resultados: Te genera un modelo 3D que te dice en que zonas se necesita rediseñar

## 1962 Spacewar
* Considerado el primer videojuego
- Creado en un osciloscopio por Steve russell
- Para generar 1 GFLOP se requieren $8 trillones de dolares

## 1963 Sketckpad
- Ivan Sutherland diseña un prototipo de programa de duseño usando un osciloscopio. Sketchpad es considerado el primer programa CAD
- Primer programa capaz de guardar un dibujo

## 1963 Primer mouse
Creado por Douglas Engelbart

## 1965 NASTRAN
Peimer software comercial de diseño

## 1972 Pong
- Primer videojuego en formato arcade.
- Creado por Nolan Kay Bushnell

## 1972 Escaner CT
Usasndo un tubo de rayos X y varios detectores

## 1972 Apple II
Primera computadora personal con graficos

## 1977 Star Wars
Sus efectos generados por computadora fueron basadas en vectores y luego filmadas

## 1982 Commodore 64
Usó de gráficos, consola casera

## 1982 TRON 
Primera películla en unar CGI de manera extensa

## 1984
Para generas 1 GFLOP ahora son 30 Billlones

1994 Vuela primer Boeing 777 probado totalmente en simulacion

1995 Primer película creada ennteramente con CGI

## 2013 Se pueden crear animaciones en laptops
Su evolucion en procesamiento les permite también renderizar en poco tiempo

## 2016 Face2Face
Se pueden crear animaciones mapeando de una fuente a un objetivo en tiempo real

## 2017 Animacion de rostros en teimpoo real 
Fuente para los filtros que aparecen en diversas redes sociales

## 2018
Se pueden crear grafucos casi realistas en telefonos moviles


# Clasificacion de graficacion
- Graficacion 2D
- Graficacion 3D

# Aplicaciones de graficacion
- Educacion y entrenamiento
- Biologia
- Mapas generados por computadora
- Arquitectura
- Graficas de representacion
- Arte por computadora
- Entretenimiento
- Virtualizacion
# Componentes
## Frame Buffer
Involucra el conjunto de diversos buffers(Almacenamiento temporal):
- Para color
- Para profundidad

## Monitor
Los aspectos importantes a tomar en cuenta son:
- Resolucion (Numero de pixeles que se usan para mostrar imagenes)
- Relacion de aspecto (Ancho de patnalla / alto de la pantalla)

## Controlador de video 
- Sirve para enviar el contenido del Frame Buffer hacia el monitor para que pueda ser mostrado


# Pixel
Entre mas juntos esten los pixeles:
- Mejor calidad de la imagen
- La imagen es mas nitida

# Conversion de un punto 
- Cada pixel no represente un punto matematico
- En realidad, representa una reguob que pueda contener una cantidad inficnita .....................
![[Pasted image 20230214003507.png]]
# Conversion de una linea 

![[Pasted image 20230214003421.png]]

# Conversion de un buen algoritmo de lineas
1. La linea debe verse derecha
2. Debe terminar de manera precisa
3. Debe tener denisidad consistente
4. La densidad deber ser independientede longitud y angulo
5. Debe dibujarse rapidamente

# Algoritmos de conversion de lineas
- Uso directo de la ecuacion de la recta
- DDA (Digital Differntial Analyzer)
- Algoritmo de Bresenham

# Proyecciones
Es la fomra de representar en un plano 2D (Una pantalla, proyector, etc) una imagen 3D

## Proyeccion ortogonal
Forma mas basica de representar una imagen 3D
Como si vieras una caja de frente y con la perspectiva simula una imagen 3D
Un punto de vista estatico y sin angulacion

Ejemplo de isometrico (Ortogonal, pero visto desde arriba)
Sims
Diablo
Hades

## Proyeccion Frustrum
Un plano de ojo de pescado que amplia una imagen para generar una imagen
Puede variar su angulacion

## Proyeccion gIOrtho
Es una ortogonal, pero toma en cuenta la profundidad de los objetos, es decir que podemos ver la profundidad de los objetos

# Modos de color: RGB
- Modo mas utilizado para aplicaciones digitales
- Utiliza 3 canales de color de 1 byte cada uno (24 bits por pixel)

# Modos de color: CMYK
Utiliza 4 colores 
- Cyan
- Magenta 
- Amarillo
- Negro

Utiliza 32 bits por pixel

Se creo primeramente para hacer impresiones, ya que toman de base el blanco

# Modos de color: HSL y HSV
## HSL
Matiz (hue)
Saturacion(Saturation)
Luminisidad(Lightness)

## HSV
Matiz (Hue)
Saturacion(Saturation)
Valor (Value)

Se usan en programas de diseño, como Photshop, enfocado a que el usuario pueda manipularlo directamente

2/13/2023
# Formatos de imagen
## Archivos no vectoriales
JPG
PNG
TIF
BMP
PSD
GIF 
RAW

## Archivos vectoriales
AI
EPS
SVG
PDF
CDR

# Graficos rasterizados
Convetit una imagen continua a pixeles


-------------


- BitMap (.BMP)
Guardan el valor de color de cada pixel
Normalmente muy pesados para la resolucion que pueden tomar

- JPG (Joint Photographic Group)
Es un algoritmo de comprension con perdida
Formato comun para envio de archivos ligeros

- GIF (Graphic Interchange Format)
Formato sin perdida de calidad, siempre que partamos de imagenes de 256 colores o menos
Sus ultimas versiones permiten hacer animaciones simples

- PNG (Portable Network Graphics)
Basado en un algoritmo de compresion si perdida para bitmaps

# Graficos vectorizados


# Formatos comunes
.AI (Adobe Ilustrator)
.SVG (Scakabke Vector Graphics)
.CDR (Corel Draw)
.PDF (Portable Document Format)
.DWG (Autocad Drawing Database)
.STL (Estereolitografia)