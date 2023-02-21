Android Studio es el entorno de desarrollo integrado (IDE) oficial para el desarrollo de apps para Android y está basado en IntelliJ IDEA. Además del potente editor de códigos y las herramientas para desarrolladores de IntelliJ

 ## Funciones que aumentan tu productividad
-   Un **sistema de compilación** flexible basado en Gradle
-   Un **emulador** rápido y cargado de funciones
-   Un**entorno unificado** donde puedes desarrollar **para** todos **los dispositivos Android**
-   Aplicación de cambios para **insertar cambios de código y recursos a la app en ejecución sin reiniciarla**
-   **Integración con GitHub** y **plantillas de código** para ayudarte a compilar funciones de apps comunes y también importar código de muestra
-   Variedad de marcos de trabajo y herramientas de prueba
-   **Herramientas de Lint para identificar problemas de rendimiento, usabilidad y compatibilidad de versiones**, entre otros
-   Compatibilidad con C++ y NDK
-   Compatibilidad integrada con [Google Cloud Platform](https://cloud.google.com/tools/android-studio/docs/), que facilita la integración con Google Cloud Messaging y App Engine


## Estructura del proyecto

Cada proyecto de Android Studio incluye uno o más módulos con archivos de código fuente y archivos de recursos. Entre los **tipos de módulos** se incluyen los siguientes:

-   Módulos de apps para Android
-   Módulos de biblioteca
-   Módulos de Google App Engine

cada módulo de app contiene las siguientes carpetas:

-   **manifests**: contiene el archivo AndroidManifest.xml.
-   **java**: contiene los archivos de código fuente Java, incluido el código de prueba de JUnit.
-   **res**: contiene todos los recursos sin código, como diseños XML, strings de IU e imágenes de mapa de bits.
![[Pasted image 20220908001810.png]]



![](https://developer.android.com/static/studio/images/intro/problems-view_2-1_2x.png)


## Interfaz de usuario

La ventana principal de Android Studio consta de varias áreas lógicas identificadas en la figura 3.

![](https://developer.android.com/static/studio/images/intro/main-window_2-2_2x.png)


1.  La **barra de herramientas** te permite realizar una gran variedad de acciones, como ejecutar tu app e iniciar las herramientas de Android.
2.  La **barra de navegación** te ayuda a explorar tu proyecto y abrir archivos para editar. Proporciona una vista más compacta de la estructura visible en la ventana **Project**.
3.  La **ventana del editor** es el área en la que puedes crear y modificar código. Según el tipo de actividad actual, el editor puede cambiar. Por ejemplo, cuando ves un archivo de diseño, el editor muestra el Editor de diseño.
4.  La **barra de la ventana de herramientas** se encuentra afuera de la ventana del IDE y contiene los botones que te permiten expandir o contraer ventanas de herramientas individuales.
5.  Las **ventanas de herramientas** te brindan acceso a tareas específicas, como la administración de proyectos, la búsqueda, el control de versiones, entre otras. Puedes expandirlas y contraerlas.
6.  En la **barra de estado**, se muestra el estado de tu proyecto y el IDE, además de advertencias o mensajes.


### Ventanas de herramientas

En lugar de usar perspectivas predeterminadas, Android Studio sigue tu contexto y te ofrece automáticamente ventanas de herramientas relevantes mientras trabajas. 

Para ubicar una ventana de herramientas específica, desplázate sobre su ícono y selecciónala en el menú.

### Cómo completar el código

Android Studio ofrece tres opciones para completar el código, a las que puedes acceder con combinaciones de teclas.


#### Completar de manera básica: 

Muestra sugerencias básicas para variables, tipos, métodos y expresiones, entre otras. Si completas de manera básica dos veces seguidas, verás más resultados. Entre otros, miembros privados y miembros estáticos sin importar. 

**Control + Barra espaciadora**



#### Completar de manera inteligente

Muestra opciones relevantes en función del contexto. La función Completar de manera inteligente reconoce el tipo y los flujos de datos previstos. Si completas de manera inteligente dos veces seguidas, verás más resultados. Por ejemplo, cadenas.

**Control + Mayús + Barra espaciadora**


#### Completar instrucciones

Completa la instrucción actual agregando elementos que faltan, como paréntesis, corchetes, llaves y formato, entre otros.

**Control + Mayús + Intro**


También puedes realizar correcciones rápidas para mostrar acciones de intención si presionas **Alt + Intro**.

### Cómo buscar código de ejemplo

El Navegador de muestras de código de Android Studio te ayuda a buscar muestras de código de Android de alta calidad proporcionadas por Google según el símbolo actualmente destacado en tu proyecto. 

### Navegación

Aquí te ofrecemos algunas sugerencias para ayudarte a desplazarte por Android Studio.

-   Alterna entre los archivos a los que accediste recientemente mediante la acción _Recent Files_. Presiona **Control + E** 
-   Usa la acción _File Structure_ para visualizar la estructura del archivo actual.
-   Busca una clase específica en tu proyecto y navega hacia ella con la acción _Navigate to Class_. Para activar la acción, presiona **Control + N** 
-   Para navegar a un archivo o una carpeta, usa la acción _Navigate to File_. Si quieres activar la acción Navigate to File, presiona **Control + Mayús + N** 
-   Navega a un método o campo por nombre con la acción _Navigate to Symbol_. Para activar la acción Navigate to Symbol, presiona **Control + Mayús + Alt + N** 
-   Encuentra todas las partes de código que hagan referencia a la clase, el método, el campo, el parámetro o la instrucción en la posición actual. Para ello, presiona **Alt + F7** 

### Estilo y formato

Mientras editas, Android Studio aplica automáticamente formatos y estilos según lo especificado en tu configuración de estilo de código. Puedes personalizar la configuración de estilo de código programando el idioma, que incluye la especificación de convenciones para pestañas y sangrías, espacios, ajuste y llaves, y líneas en blanco. Para personalizar la configuración de estilo de tu código, haz clic en **File > Settings > Editor > Code Style** 

Si bien el IDE aplica formato de manera automática mientras trabajas, también puedes llamar explícitamente a la acción _Reformat Code_ si presionas **Control + Alt + L** (**Opción + Comando + L** en Mac), o bien aplicar sangrías automáticas a todas las líneas si presionas **Control + Alt + I** (**Control + Opción + I** en Mac).

![](https://developer.android.com/static/studio/images/intro/code-before-formatting_2-1_2x.png)

**Figura 4:** Código antes de la aplicación de formato

![](https://developer.android.com/static/studio/images/intro/code-after-formatting_2-1_2x.png)

**Figura 5:** Código después de la aplicación de formato

### Aspectos básicos del control de versiones

Android Studio admite diferentes sistemas de control de versión (VCS), incluidos Git, GitHub, CVS, Mercurial, Subversion y Google Cloud Source Repositories.

1.  En el menú del **VCS** de Android Studio, haz clic en **Enable Version Control Integration**.
2.  En el menú desplegable, selecciona un sistema de control de versión para asociarlo con la raíz del proyecto y, luego, haz clic en **OK**.

En el menú del VCS se mostrarán diversas opciones de control de versión según el sistema que hayas seleccionado.


## Sistema de compilación de Gradle

Android Studio usa Gradle como base del sistema de compilación, y el complemento de Android para Gradle proporciona capacidades específicas de Android. Este sistema de compilación se ejecuta en una herramienta integrada desde el menú de Android Studio, y lo hace independientemente de la línea de comandos. Puedes usar las funciones del sistema de compilación para lo siguiente:

-   Personalizar, configurar y extender el proceso de compilación
-   Crear varios APK para tu app; diferentes funciones usan el mismo proyecto y los mismos módulos
-   Volver a usar códigos y recursos en conjuntos de archivos fuente

Gracias a la flexibilidad de Gradle, puedes lograrlo sin modificar los archivos fuente de tu app. Los archivos de compilación de Android Studio se denominan `build.gradle`. Son archivos de texto sin formato que usan la sintaxis [Groovy](http://groovy-lang.org/) a fin de configurar la compilación con elementos que proporciona el complemento de Android para Gradle. 


### Variantes de compilación
El sistema de compilación puede ayudarte a **crear diferentes versiones de la misma app a partir de un solo proyecto**. Esto resulta útil cuando tienes una **versión gratuita o una versión paga** de tu app, o si quieres distribuir múltiples APK para diferentes configuraciones de dispositivos en Google Play.

### Compatibilidad con varios APK

La compatibilidad con varios APK **te permite crear de manera eficiente varios APK basados en la densidad de la pantalla o en ABI**. Por ejemplo, puedes crear APK individuales de una app para las densidades de pantalla hdpi y mdpi, y considerarlos una misma variante de modo que compartan la configuración de APK, javac, dx y ProGuard para la prueba.


### Reducción de recursos
La reducción de recursos en Android Studio **quita automáticamente los recursos sin usar del paquete de tu app ni las dependencias de bibliotecas**. Por ejemplo, si tu aplicación usa [Servicios de Google Play](https://developers.google.com/android/guides/overview) para acceder a la funcionalidad de Google Drive y actualmente no usas el [Acceso con Google](https://developer.android.com/training/sign-in), la reducción de recursos puede quitar los diferentes recursos de elemento de diseño de los botones `SignInButton`.


### Administración de dependencias

Las dependencias para tu proyecto están especificadas por nombre en el archivo `build.gradle`. Gradle **se ocupa de buscar tus dependencias y hacer que estén disponibles en tu compilación.** Puedes declarar dependencias de módulos, dependencias binarias remotas y dependencias binarias locales en tu archivo `build.gradle`. Android Studio configura los proyectos para que usen el repositorio central de Maven de manera predeterminada. (Esta configuración está incluida en el archivo de compilación de nivel superior del proyecto). 

## Herramientas de depuración y perfil
Android Studio te **ayuda a depurar y mejorar el rendimiento de tu código**. Esto incluye herramientas integradas de depuración y análisis de rendimiento.

### Depuración integrada

Usa la depuración integrada para **mejorar las revisiones de código** en la vista del depurador con verificación integrada de referencias, expresiones y valores de variables. **La información de depuración integrada incluye:**

-   Valores de variables integradas
-   Referencia a objetos que hacen referencia a un objeto seleccionado
-   Valores de retorno de métodos
-   Expresiones lambda y de operador
-   Valores de información sobre herramientas

![](https://developer.android.com/static/studio/images/intro/inline-variable-value-debug_2-1_2x.png)

**Figura 6**: Valor de una variable integrada


### Generador de perfiles de rendimiento

Android Studio **ofrece generadores de perfiles de rendimiento para que puedas realizar un seguimiento más fácil del uso de CPU y memoria de tu app, encontrar objetos asignados, ubicar pérdidas de memoria, optimizar el rendimiento de los gráficos y analizar las solicitudes de red**. 

### Volcado de montón
Cuando controlas el uso de la memoria en Android Studio, **puedes iniciar simultáneamente la recolección de elementos no utilizados y volcar el montón de Java a una captura instantánea del montón en un archivo** de formato binario HPROF específico de Android. El visor de HPROF muestra las clases, las instancias de cada clase y un árbol de referencia para ayudarte a realizar el seguimiento del uso de memoria y encontrar fugas de memoria.


### Memory Profiler
Puedes usar el **Generador de perfiles de memoria para realizar un seguimiento de la asignación de memoria y ver dónde se asignan los objetos cuando realizas determinadas acciones.**

Conocer estas asignaciones te permite optimizar el rendimiento de tu app y el uso de la memoria ajustando las llamadas de método relacionadas con esas acciones.


### Acceso al archivo de datos

Las herramientas del SDK de Android, como Systrace y logcat, **generan datos de rendimiento y depuración para un análisis detallado de la app.**


### Inspecciones de código

Cada vez que compilas tu programa, Android Studio ejecuta automáticamente inspecciones de Lint y otras inspecciones de IDE para **ayudarte a identificar y corregir problemas con la calidad estructural de tu código de manera sencilla.**

La herramienta lint **comprueba los archivos de origen de tu proyecto de Android en busca de posibles errores** y para realizar mejoras relacionadas con la precisión, la seguridad, el rendimiento, la usabilidad, la accesibilidad y la internacionalización.


### Anotaciones en Android Studio

**Android Studio admite anotaciones de variables, parámetros y valores de retorno a fin de ayudarte a detectar errores, como excepciones de puntero nulo y conflictos de tipos de recurso.** Android SDK Manager empaqueta la biblioteca de compatibilidad-anotaciones en el Repositorio de compatibilidad de Android para usarla con Android Studio. Android Studio valida las anotaciones configuradas durante la inspección del código.

### Mensajes de registro

Cuando creas y ejecutas tu app con Android Studio, puedes ver los resultados de adb y los mensajes de registro del dispositivo en la ventana de **Logcat**.

### Generación de perfiles de rendimiento
Si deseas perfilar el rendimiento de red, memoria y CPU de tu app, abre Android Profiler

## Cómo acceder a tu cuenta de desarrollador

 Puedes acceder a tu cuenta de desarrollador en Android Studio para acceder a herramientas adicionales que requieren autenticación. Al acceder, le otorgas a esas herramientas permiso para ver y administrar tus datos en todos los servicios de Google.

