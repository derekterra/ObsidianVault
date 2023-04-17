En algún punto, cuando estés creando una página web, te encontrarás con problemas con los estilos, por ejemplo:

-   ¿Por qué no se aplica el color que le estoy poniendo?
-   ¿Por qué este elemento se comporta de manera diferente?

Probablemente, sea un inconveniente de **cascada o especificidad**.

## Qué es la cascada en CSS

La cascada es el concepto que determina **qué estilos se colocan sobre otros, priorizando a aquellos que se encuentren más abajo del código**. Recordarás que CSS es la abreviación de _Cascade Style Sheets_, que traducido es hojas de estilos en **Cascada**.

![Representación gráfica de la cascada en CSS](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/frontend_developer16.png)

Mira el siguiente código e identifica de qué color de letra tendrá la etiqueta `<h1>`.

```css
h1 {
    color: red;
}

h1 {
    color: blue;
}
```

La etiqueta `<h1>` tendrá un color `blue` de letra, esto porque está situado más abajo en el código. Esto ocurre con cada propiedad de CSS que se repita en algún punto más arriba del código.

-   [Ejemplo de cascada](https://codi.link/PGgxPkNhc2NhZGE8L2gxPg==%7CaDEgew0KICBjb2xvcjogcmVkOw0KfQ0KDQpoMSB7DQogIGNvbG9yOiBibHVlOw0KfQ==%7C)

Sin embargo, esto ocurre cuando la especificidad de una regla CSS tiene el mismo valor. Pero, ¿qué es especificidad?

## Qué es especificidad en CSS

La especificidad consiste en dar un valor a una regla CSS sobre **qué tan específico es el estilo**, esto para que los navegadores puedan saber qué estilos aplicar sobre otros, independientemente de dónde se encuentren en el código. **El estilo se aplicará donde la especificidad sea mayor.**

## Tipos de especificidad en CSS

Existen 6 tipos de especificidad con su respectivo valor, donde `X` es la cantidad de estilos que lo contienen. Mira la siguiente imagen:

![Tipos de especificidad en CSS](https://static.platzi.com/media/user_upload/especificidad-a630e9d4-545b-4ac1-9fb3-0e443ea066ea.jpg)

### Valor con mayor especificidad

La palabra reservada `!important` es **un valor de toda propiedad CSS que provee una especificidad de `10000`**, por lo que se aplicará ante otros estilos. Esto es una mala práctica y no deberías utilizarlo.

```css
h1 {
    color: red !important;
}
```

-   [Ejemplo de !important](https://codi.link/PGgxPkVzcGVjaWZpY2lkYWQ8L2gxPg0K%7CaDEgew0KICBjb2xvcjogcmVkOw0KfQ0KDQpoMSB7DQogIGNvbG9yOiBncmVlbiAhaW1wb3J0YW50Ow0KfQ0KDQpoMSB7DQogIGNvbG9yOiBibHVlOw0KfQ0KDQpoMSB7DQogIGNvbG9yOiBwYXBheWF3aGlwOw0KfQ0K%7C)

### Estilos en línea

Los estilos en línea **son las propiedades CSS escritas en el HTML a través de la propiedad `style` de toda etiqueta**. También es una mala práctica y debes evitarlo.

```html
<h1 style="color: blue;">Especificidad</h1>
```

-   [Ejemplo de estilos en línea](https://codi.link/PGgxIHN0eWxlPSJjb2xvcjogYmx1ZTsiPkVzcGVjaWZpY2lkYWQ8L2gxPg0K%7CaDEgew0KICBjb2xvcjogcmVkOw0KfQ0KDQpoMSB7DQogIGNvbG9yOiBncmVlbjsNCn0NCg0K%7C)

### Especificidad en selectores

El tema de los selectores ya lo conoces, por lo tanto, los selectores de tipo ID son más específicos que las clases, atributos y pseudoclases. Estas últimas son más específicas que los elementos y pseudoelementos. El selector universal tiene una especificidad de `0`.

En un proyecto deberías evitar los `!important` y estilos en línea, para trabajar únicamente con la especificidad de los selectores. Sin embargo, **debes tener presente que los selectores combinadores suman la especificidad de cada selector básico para obtener la especificidad total de la regla CSS**.

![Cálculo de la especificidad en selectores combinadores](https://cdn.document360.io/da52b302-22aa-4a71-9908-ba18e68ffee7/Images/Documentation/frontend_developer18.png)

Si utilizas Visual Studio Code y mantienes el _mouse_ sobre el selector, te mostrará la especificidad total. [Specificity Calculator](https://specificity.keegan.st/) es una página web donde puedes calcular la especificidad.