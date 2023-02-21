Todas las aplicaciones Android se componen de una estructura general; conformada por 
- **librerías de código**
- **archivos de recursos y vistas**
- **código fuente **
- **Android Manifest **


## Configuración de un nuevo proyecto en Android Studio

-   **Application name:** escribe el nombre de tu aplicación
-   **Company Domain:** para este ejemplo usé [carlosreina.example.com](http://carlosreina.example.com/)
-   **Project location:** La ubicación donde estará nuestra aplicación
![[Pasted image 20220908001310.png]]

## Target Android Devices

-   Phone and Tablet, Tv, Wear y Glass.

En esta ventana configuraremos las plataformas y APIs que vamos a utilizar en nuestra aplicación. En este caso en particular, utilizaremos la **API 15**: **Android 4.0.3 Ice Cream Sandwich**, enfocada a teléfonos y tablets.

![[Pasted image 20220908001328.png]]

## Seleccionando el tipo de actividad principal para nuestra aplicación

-   **Activity o Actividad:** una ventana o pantalla de la aplicación

Para este ejemplo seleccionaremos **Blank Activity**. Así podremos observar de manera más clara la estructura de la app. De lo contrario, nos perderíamos entre los diferentes tipos de archivos y carpetas que generaría Android Studio si eligiéramos otra Actividad.

![[Pasted image 20220908001445.png]]

## Personalizando la actividad

-   **Activity Name:** es el nombre de la clase Java asociada
-   **Layout Name:** la interfaz gráfica de la actividad
-   **Title:** el título de la actividad
-   **Menu Resource Name:** nombre del recurso XML correspondiente al menú principal

Dependiendo de la experiencia que tengas desarrollando para Android, recomiendo dejar los datos que ingresa el asistente de configuración por defecto.

![[Pasted image 20220908001504.png]]

Una vez terminado el asiste de configuración, veremos por primera vez **la interfaz de Android Studio.**

Ahora nos enfocaremos en la estructura de nuestra aplicación que se encuentra al lado izquierdo de nuestra pantalla. ![Estructura2](https://static.platzi.com/blog/uploads/2015/06/Estructura2.jpg) Android Studio nos mostrará por defecto la pestaña **Android**. Esta se compone de varios elementos que están incluídos dentro de la carpeta **app**. Para visualizar toda la estructura del proyecto, debemos dar clic en esta pestaña para que se despliegue una serie de opciones. Ahí vamos a elegir **Project**. ![Estructura3](https://static.platzi.com/blog/uploads/2015/06/Estructura3.jpg) Ahora que ya podemos ver nuestro proyecto por completo, encontraremos los siguientes elementos:

-   **gradle:** es una herramienta para automatizar la construcción de nuestros proyectos. Nos permite realizar tareas de compilación, empaquetado y testing.
-   **.idea:** Android Studio trabaja con **IntelliJ IDEA** un entorno de desarrollo integrado en Java.
-   **app:** contiene todos los archivos relacionados a nuestro proyecto y será la carpeta en la que nos enfocaremos en este artículo.
-   **External Libraries:** Como su nombre lo indica, son librerías externas.

![Estructura](https://static.platzi.com/blog/uploads/2015/06/Estructura.jpg) Ahora vamos a dar clic en la carpeta **app** y observaremos que se compone de tres carpetas:

-   **Carpeta build:** los elementos que contiene son códigos generados automáticamente por Android Studio cada vez que se realiza la compilación de nuestro proyecto.
-   **Carpeta libs:** contiene las librerías Java externas que utiliza nuestra aplicación. Android Studio hace referencia a estas librerías en el fichero **build.gradle**.
-   **Carpeta src:** contiene la información más importante y será la que estudiaremos para entender la estructura de una aplicación de Android.

![carpetaAPP](https://static.platzi.com/blog/uploads/2015/06/carpetaAPP.jpg) 

## Carpeta app/src/main/java

![carpetaMain](https://static.platzi.com/blog/uploads/2015/06/carpetaMain.jpg) Esta carpeta contiene **el código fuente de nuestra aplicación**. Al explorar el contenido de **MainActivity** veremos que Android Studio generó automáticamente un código básico para nuestra actividad principal.

## Carpeta app/src/main/res

![carpetaRES](https://static.platzi.com/blog/uploads/2015/06/carpetaRES.jpg) Esta carpeta contiene los archivos como imágenes, cadenas de texto, layouts, estilos, traducciones, menús e interfaz gráfica. Cada elemento esta subdividido en otras carpetas que detallaré a continuación:

-   **Carpeta drawable:** aquí agregaremos las imágenes que utilizaremos en nuestra aplicación. 

-   **Carpeta layout:** aquí encontraremosel archivo **activity_main.xml.** Este contiene el diseño de la interfaz de nuestra actividad principal.

Android Studio nos permite editar este archivo de dos formas. La primera es utilizando un editor estilo **Drag and Drop** como el que puedes ver abajo. ![diseño](https://static.platzi.com/blog/uploads/2015/06/dise%C3%B1o.jpg) Y el segundo método es utilizando el método **text**. Es decir, Android Studio nos permite editar nuestro archivo activity_main.xml a través de nodos XML. ![text](https://static.platzi.com/blog/uploads/2015/06/text.jpg)

## Pero, ¿qué significa ese código?

[java] <xml><relativelayout xmlns:android=“[http://schemas.android.com/apk/res/android](http://schemas.android.com/apk/res/android)” xmlns:tools=“[http://schemas.android.com/tools](http://schemas.android.com/tools)” android:layout_width=“match_parent” android:layout_height=“match_parent” android:paddingleft=“16dp” android:paddingright=“16dp” android:paddingtop=“16dp” android:paddingbottom=“16dp” tools:context=".MainActivity"></relativelayout></xml> [/java] **RelativeLayout:** hace referencia a un contenedor principal que define un orden, características y secuencias de todos los elementos de nuestra actividad. Además, estas se ubicarán por referencia y no por valores absolutos. Así, las aplicaciones se ajustarán a cualquier tipo de pantalla. **android:layout_width=“match_parent” :** es el ancho del layout dentro de la actividad. Al utilizar match_parent se facilita el ajuste del ancho de la pantalla en cualquier dispositivo. **android:layout_height=“match_parent”:** dimensión vertical o largo del layout. Dentro de la actividad se utiliza match_parent para facilitar el ajuste vertical de pantalla en cualquier dispositivo. **android:paddingLeft, Right, Top y Bottom:**

-   android:paddingLeft=“16dp”
-   android:paddingRight=“16dp”
-   android:paddingTop=“16dp”
-   android:paddingBottom=“16dp”

Son los espacios laterales y verticales entre el contorno del layout. Su valor está direccionado a **dimens.xml** dentro de la carpeta **values**. Este archivo contiene nodos xml de tipo dimensióncon valores **densitiy-indepent** en pixeles (dp). **tools:context=".MainActivity" :** es el nombre del archivo que contiene la actividad donde el layout con las distintas características será acogido.

-   **Carpeta menú**: esta carpeta es creada de forma automática y **contendrá un menú básico para nuestra actividad**. Es posible modificarla en caso de que queramos agregar un menú a nuestra aplicación o eliminarla sin ningún problema. Su estructura está creada en un archivo XML.
-   **Carpeta values**: aquí encontraremos los archivos **dimens.xml, styles.xml y strings.xml.** Los dos primeros permiten **modificar las dimensiones y estilos de nuestra aplicación**; y **el último permite agregar controles, vistas, formas, botones, múltiples idiomas y otros elementos (widgets) en nuestra aplicación.**
-   **Archivo AndroidManifiest.xml:** toda aplicación para Android debe contener este archivo en su directorio raíz. **Aquí podemos declarar** todo lo que sucede o sucederá en nuestro aplicativo; ya sea **el nombre de la aplicación, actividades, íconos, servicios y otros elementos**. Además, debemos agregar la forma en que interactúan entre ellos y con el sistema; y nos indicará qué actividad es la que aparecerá en el menú principal del dispositivo (launcher).

