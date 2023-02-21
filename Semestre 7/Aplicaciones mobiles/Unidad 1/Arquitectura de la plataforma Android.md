![[Business Model Canvas.jpg]]


# Arquitectura de la plataforma Android 

Android es una pila de software de código abierto **basado en Linux** creada para una variedad amplia de dispositivos y factores de forma.

## Kernel de Linux
**La base** de la plataforma Android **es el kernel de Linux**. Por ejemplo, [[Arquitectura de la plataforma Android#Arquitectura de la plataforma Android#Tiempo de ejecución de Android|el tiempo de ejecución de Android (ART)]] se basa en el kernel de Linux para funcionalidades subyacentes, como la generación de subprocesos y la administración de memoria de bajo nivel.

El uso del kernel de Linux **permite que Android aproveche funciones de seguridad claves** y, al mismo tiempo, **permite a los fabricantes** de dispositivos **desarrollar controladores de hardware** para un kernel conocido.

## Capa de abstracción de hardware (HAL)
**Brinda interfaces estándares que exponen las capacidades de hardware** del dispositivo al [[Arquitectura de la plataforma Android#Marco de trabajo de la API de Java|marco de trabajo de la API de Java]] de nivel más alto. La HAL **consiste en varios módulos de biblioteca y cada uno** de estos **implementa una interfaz para un** tipo específico de **componente de hardware**, como el módulo de la cámara o de Bluetooth. Cuando el marco de trabajo de una API realiza una llamada para acceder a hardware del dispositivo, el sistema Android carga el módulo de biblioteca para el componente de hardware en cuestión.

##  Tiempo de ejecución de Android

Para los dispositivos con Android 5.0 (nivel de API 21) o versiones posteriores, cada app ejecuta sus propios procesos con sus propias instancias del tiempo de ejecución de Android (ART). **El ART está escrito para ejecutar varias máquinas virtuales en dispositivos de memoria baja ejecutando archivos DEX**, un formato de código de bytes diseñado especialmente para Android y optimizado para ocupar un espacio de memoria mínimo. Crea cadenas de herramientas, como Jack, y compila fuentes de Java en código de bytes DEX que se pueden ejecutar en la plataforma Android.

**Estas son algunas de las funciones principales del ART:**

-   **Compilación** ahead-of-time **(AOT)** y just-in-time **(JIT)**
-   Recolección optimizada de elementos no utilizados (**Garvage Collector**)
-   En Android 9 (nivel de API 28) y versiones posteriores, se convierten los archivos de formato ejecutable (DEX) de un paquete de aplicaciones a un código de máquina más compacto
-   Esto mejora la compatibilidad con la depuración, el generador de perfiles de muestras dedicado, las excepciones de diagnóstico detalladas y los informes de fallos, y la capacidad de establecer puntos de control para supervisar campos específicos

Antes de Android 5.0 (nivel de API 21), Dalvik era el entorno de ejecución del sistema operativo. Si tu app se ejecuta bien en el ART, también debe funcionar en Dalvik, pero es posible que no suceda lo contrario.

En Android, también se incluye un conjunto de bibliotecas de entorno de ejecución centrales que proporcionan la mayor parte de la funcionalidad del lenguaje de programación Java; se incluyen algunas funciones del lenguaje Java 8, que usa el marco de trabajo de la API de Java.

## Bibliotecas C/C++ nativas
Muchos componentes y servicios centrales del sistema Android, como **el ART y la HAL, se basan en código nativo que requiere bibliotecas nativas escritas en C y C++**. La plataforma Android proporciona API del marco de trabajo de Java para exponer la funcionalidad de algunas de estas bibliotecas nativas a las apps. Por ejemplo, puedes acceder a OpenGL ES a través de la API de OpenGL de Java del marco de trabajo de Android para agregar a tu app compatibilidad con los dibujos y la manipulación de gráficos 2D y 3D.

Si desarrollas una app que requiere C o C++, puedes usar el NDK de Android para acceder a algunas de estas bibliotecas de plataformas nativas directamente desde tu código nativo.

## Marco de trabajo de la API de Java

**Todo el conjunto de funciones del SO Android está disponible mediante API escritas en el lenguaje Java.** Estas API **son los cimientos que necesitas para crear apps** de Android simplificando la reutilización de componentes del sistema y servicios centrales y modulares, como los siguientes:

-   Un sistema de vista enriquecido y extensible que puedes usar para compilar la IU de una app; se incluyen listas, cuadrículas, cuadros de texto, botones e incluso un navegador web integrable.
-   Un administrador de recursos que te brinda acceso a recursos sin código, como strings localizadas, gráficos y archivos de diseño.
-   Un administrador de notificaciones que permite que todas las apps muestren alertas personalizadas en la barra de estado.
-   Un administrador de actividad que administra el ciclo de vida de las apps y proporciona una pila de retroceso de navegación común.
-   Proveedores de contenido que permiten que las apps accedan a datos desde otras apps, como la app de Contactos, o compartan sus propios datos.

Los desarrolladores tienen acceso total a las mismas API del marco de trabajo que usan las apps del sistema Android.

## Apps del sistema
En Android se incluye un conjunto de apps centrales para correo electrónico, mensajería SMS, calendarios, navegación en Internet y contactos, entre otros elementos. **Las apps incluidas en la plataforma no tienen un estado especial entre las apps que el usuario elije instalar**; por ello, una app externa se puede convertir en el navegador web, el sistema de mensajería SMS o, incluso, el teclado predeterminado del usuario (existen algunas excepciones, como la app Settings del sistema).

Las apps del sistema funcionan como apps para los usuarios y brindan capacidades claves a las cuales los desarrolladores pueden acceder desde sus propias apps. Por ejemplo, si en tu app se intenta entregar un mensaje SMS, no es necesario que compiles esa funcionalidad tú mismo; como alternativa, puedes invocar la app de SMS que ya está instalada para entregar un mensaje al receptor que especifiques.