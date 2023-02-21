# Protocolos
## TCP
TCP (**Protocolo de Control de Transmisión** por sus siglas en inglés _Transmission Control Protocol_) es protocolo de red importante que permite que dos anfitriones (_hosts_) se conecten e intercambien flujos de datos. TCP garantiza la entrega de datos en el mismo orden en que se enviaron.

Como si dos personas hablaran por **telefono**, se reserva una linea para hablar con ellos, si llega a haber ruido, se pide retransmision en ese momento

## UDP
El protocolo de datagramas de usuario, abreviado como UDP, es un protocolo **que permite la transmisión sin conexión de datagramas** en redes basadas en IP. Para obtener los servicios deseados en los hosts de destino, se basa en los puertos que están listados como uno de los campos principales en la cabecera UDP. Como muchos otros protocolos de red, UDP pertenece a la familia de protocolos de Internet, por lo que debe clasificarse en el **nivel de transporte** y, en consecuencia, se encuentra en una capa intermedia entre la capa de red y la capa de aplicación.

**Analogia del correo**, una parte del mensaje se puede ir por una parte, otra parte por otro lado, al llegar se vuelve a armar, de faltar alguna parte la capa de aplicacion pide retransmision 

## DHCP
El protocolo DHCP (Protocolo de configuración dinámica de host) o también conocido como «**Dynamic Host Configuration Protocol**«, es un protocolo de red que utiliza una arquitectura cliente-servidor.
Este protocolo se encarga de asignar de manera dinámica y automática una dirección IP, ya sea una dirección IP privada desde el router hacia los equipos de la red local, o también una IP pública por parte de un operador que utilice este tipo de protocolo para el establecimiento de la conexión.

## IP
El protocolo de IP (Internet Protocol) es la base fundamental de la Internet. Porta datagramas de la fuente al destino. [[Modelo OSI#4 Capa de transporte|El nivel de transporte]] parte el flujo de datos en [[Protocolos#^d2e6a3|datagramas]]. Durante su transmisión se puede partir un datagrama en fragmentos que se montan de nuevo en el destino. Las principales características de este protocolo son:

-   Protocolo orientado a no conexión.
-   Fragmenta paquetes si es necesario.
-   Direccionamiento mediante direcciones lógicas IP de 32 bits.
-   Si un paquete no es recibido, este permanecerá en la red durante un tiempo finito.
-   Realiza el "mejor esfuerzo" para la distribución de paquetes.
-   Tamaño máximo del paquete de 65635 bytes.
-   Sólo ser realiza verificación por suma al encabezado del paquete, no a los datos éste que contiene.

Proporciona un servicio de distribución de paquetes de información orientado a no conexión de manera no fiable. La orientación a no conexión significa que los paquetes de información, que será emitido a la red, son tratados independientemente, pudiendo viajar por diferentes trayectorias para llegar a su destino. El término no fiable significa más que nada que no se garantiza la recepción del paquete.

**La unidad de información intercambiada por IP es denominada datagrama.** Tomando como analogía los marcos intercambiados por una red física los datagramas contienen un encabezado y una área de datos. IP no especifica el contenido del área de datos, ésta será utilizada arbitrariamente por el protocolo de transporte. ^d2e6a3

## FTP
Protocolo de transmision de archivos, sirve para poder descargar y subir archivos entre usuarios

## ARP
ARP son las siglas de **Address Resolution Protocol**. Es un protocolo de comunicaciones muy importante, ya que se encarga de **vincular una dirección MAC** o dirección física, **con una dirección IP** o dirección lógica. El funcionamiento incluye que la ip mande un mensaje a todas sus conexiones y quien tenga la mac que se busca le contesta, para asi formar una tabla de conexiones.

## CSMA/CD
CSMA/CD son siglas que corresponden a las siglas Carrier Sense Multiple Access with Collision Detection, que corresponden a Acceso Múltiple por Detección de Portadora con Detección de Colisiones. La  meta  de  este  protocolo  es  de  evitar  al  máximo  las  colisiones.

Funciona de la siguiente manera:

   1. Una estación que tiene un mensaje para enviar escucha al medio para ver si otra estación está transmitiendo un mensaje.

       2. Si el medio esta tranquilo (ninguna otra estación esta transmitiendo), se envía la transmisión y se espera el ACK (acuse de recibo). La estación que recibe comprueba el CRC (detección de errores) y si es correcto envía el ACK. Si tras un tiempo no ha sido recibido el ACK, se pasa al paso 1. Si se recibe, la operación ha sido un éxito.

       3. Cuando dos o más estaciones tienen mensajes para enviar, es posible que transmitan casi en el mismo instante, resultando en una colisión en la red.

       4. Cuando se produce una colisión, todas las estaciones receptoras ignoran la transmisión confusa.

       5. Si un dispositivo de transmisión detecta una colisión, envía una señal de expansión para notificar a todos los dispositivos conectados que ha ocurrido una colisión.

       6. Las estaciones transmisoras detienen sus transmisiones tan pronto como detectan la colisión.

       7. Cada una de las estaciones transmisoras espera un **periodo de tiempo aleatorio** e intenta transmitir otra vez.

## CSMA/CA

## DNS
El sistema de nombres de dominio (DNS) es el **directorio telefónico de Internet**. Las personas acceden a la información en línea a través de nombres de dominio como nytimes.com o espn.com. Los navegadores web interactúan mediante direcciones de Protocolo de Internet (IP). El DNS traduce los nombres de dominio a direcciones IP para que los navegadores puedan cargar los recursos de Internet.


## HTTP
**Hypertext Transfer Protocol (HTTP)** (o **Protocolo de Transferencia de Hipertexto en español)** es un protocolo de la capa de aplicaciónpara la transmisión de documentos hipermedia, como HTML. Fue diseñado para la comunicación entre los navegadores y servidores web, aunque puede ser utilizado para otros propósitos también. Sigue el clásico modelo cliente-servidor, en el que un cliente establece una conexión, realizando una petición a un servidor y espera una respuesta del mismo.

## SAMBA
sirve para compartir recursos entre equipos y diferentes sistemas operativos, por ejemplo impresoras

## ICMP
PING


Tracer

## FDDI
Las redes FDDI son un grupo de especificaciones de redes estandarizadas por ANSI. Se componen de dos rutas físicas, o "anillos", que transfieren datos en direcciones opuestas El anillo primario transporta datos entre sistemas, mientras que el anillo secundario se usa para redundancia. Si un sistema en la red causa una interrupción en la ruta de datos primaria, el anillo secundario se usa hasta que el anillo primario vuelva a funcionar. Una red FDDI puede soportar varias LANs de baja capacidad que requieren un backbone de alta velocidad.

Método de Acceso:

El método de acceso utilizado en una red FDDI ES EL PASO DE TESTIGO. Un equipo en una red FDDI puede transmitir tantos paquetes como pueda producir en una tiempo predeterminado antes de liberar el testigo. Tan pronto como un equipo haya finalizado la transmisión o después de un tiempo de transmisión predeterminado, el equipo libera el testigo.

Como un equipo libera el testigo cuando finaliza la transmisión, varios paquetes pueden circular por el anillo al mismo tiempo. Este método de paso de testigo es más eficiente que el de una red Token Ring, que permite únicamente la circulación de una trama a la vez. Este método de paso de testigo también proporciona un mayor rendimiento de datos a la misma velocidad de transmisión.


## Proxy
No es un dispositivo, es una configuracion
Es un intermedario entre dos IP, para ocultar la ip usando la del proxy