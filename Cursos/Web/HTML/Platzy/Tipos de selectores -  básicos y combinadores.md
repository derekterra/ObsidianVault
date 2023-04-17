El selector define el elemento o conjunto de elementos HTML a los cuales se añadirán estilos. Existen [nombres de colores propios de CSS](https://htmlcolorcodes.com/es/nombres-de-los-colores/) que puedes explorar. A continuación veamos más sobre selectores.

## Cuáles son los selectores básicos

Un selector básico es la mínima expresión CSS para colocar estilos.

```css
selector {
    /* Estilos */
}
```

![Tipos de selectores básicos](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/frontend_developer14.png)

### 1. Selector de tipo

Selecciona todos los elementos que coincidan con el **nombre de la etiqueta HTML**.

```css
div {
    /* Todos los div en el documento */
}
```


   

### 2. Selector de clase

Selecciona todos los elementos que coincidan con las etiquetas HTML que **contengan el atributo `class`**.

```html
<!--archivo HTML-->
<div class="card"> Soy una carta </div>
```

Para seleccionar estos elementos, se empieza por un punto `.` y seguido el **valor exacto** del atributo `class` de la etiqueta. Puede ser cualquier valor que desees colocar.

```css
/* archivo CSS */
.card {
    /* Todas las etiquetas con la clase "card" */
}
```

Puede existir más de un valor dentro del atributo `class` separados por espacios.

```html
<!--archivo HTML-->
<div class="card card1"> Soy una carta </div>
<div class="card card2"> Soy una carta </div>
```

```css
.card {
    /* Todas las etiquetas con la clase "card" */
}

.card1 {
    /* Todas las etiquetas con la clase "card1" */
}

.card2 {
    /* Todas las etiquetas con la clase "card2" */
}
```


### 3. Selector de identificador único (id)

Selecciona el único elemento que coincida con la etiqueta HTML que **contenga el atributo `id`**. Solo puede existir un valor `id` para todo el documento.

```html
<!--archivo HTML-->
<button id="eliminar"> Eliminar  </button>
```

Para seleccionar el elemento, se empieza por el símbolo de _hashtag_ `#` y seguido el **valor exacto** del atributo `id` de la etiqueta. Puede ser cualquier valor que desees colocar.

```css
/* archivo CSS */
#eliminar {
    /* La única etiqueta con el id "eliminar" */
}
```

   

### 4. Selector de atributo

Selecciona los elementos que coincidan con la etiqueta HTML que **contenga el atributo y valor** especificado.

```html
<!--archivo HTML-->
<a href="https://platzi.com"> Ir a Platzi </a>
```

Para seleccionar los elementos, se empieza por el nombre de la etiqueta, seguido de corchetes `[]` que contiene el atributo y valor especificado.

```css
/* archivo CSS */
a[href=""https://platzi.com"] {
    /* Todas las etiquetas <a> con una propiedad href con valor "https://platzi.com" */
}
```



### 5. Selector universal

Selecciona todos los elementos del documento mediante un asterisco `*`.

```css
* {
    /* Todos los elementos */
}
```


   

## Cuáles son los selectores combinadores

Un selector combinador es la unión de dos o más selectores básicos.

```css
selector1 selector2 selector3 {
    /* Estilos */
}
```

![Tipos de selectores combinadores](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/frontend_developer15.png)

### 1. Combinador de descendientes

Selecciona todos los elementos del selector de la derecha que son **hijos** del selector de la izquierda, **independientemente de la profundidad**. Estos selectores están separados por un espacio.

```css
padre hijos {
    /* Todos los hijos del padre */
}

div p{
    /* Todos los hijos <p> de <div>*/
}

.container img{
    /* Todos los hijos <img> de la clase "container"*/
}
```



### 2. Combinador de hijo directo

Selecciona todos los elementos del selector de la derecha que son **hijos directos** del selector de la izquierda. Estos selectores están separados por `>`.

```css
padre > hijos_directos {
    /* Todos los hijos directos del padre */
}

div > p{
    /* Todos los hijos directos <p> de <div>*/
}

.container > img{
    /* Todos los hijos directos <img> de la clase "container"*/
}
```


### 3. Combinador de elemento adyacente

Selecciona todos los elementos del selector de la derecha que están **adyacente** al selector de la izquierda. Estos selectores están separados por `+`.

```css
elemento + adyacente {
    /* Elementos adyacentes */
}

div + p{
    /* Todos los <p> adyacentes a <div>*/
}

.container + img{
    /* Todos los <img> adyacentes a la clase "container"*/
}
```

**Adyacente significa que comparten el mismo padre y está situado inmediatamente hacia abajo de otro elemento**. Por ejemplo, en el siguiente código, `<div>` está adyacente a `<h1>` y `<p>` está adyacente a `<div>`. Sin embargo, `<h1`> no está adyacente a `<div>` y `<div>` no está adyacente a `<p>`.

```html
<!--archivo HTML -->
<h1>Soy un título </h1>
<div>Soy un div</div>
<p>Soy un párrafo</p>
```


   

### 4. Combinador general de hermanos

Selecciona todos los elementos del selector de la derecha que son **hermanos** del selector de la izquierda. Estos selectores están separados por `~`.

```css
elemento ~ hermanos {
    /* Elementos hermanos */
}

div ~ p{
    /* Todos los <p> hermanos de <div>*/
}

.container ~ img{
    /* Todos los <img> hermanos de la clase "container"*/
}
```

**Hermanos significa que comparten el mismo padre y están situados hacia abajo de otro elemento**. Por ejemplo, en el siguiente código, `<div>` y `<p>` son hermanos de `<h1>`, pero `<h1>` no es hermano de `<div>` y `<p>`.

```html
<!--archivo HTML -->
<h1>Soy un título </h1>
<div>Soy un div</div>
<p>Soy un párrafo</p>
```

