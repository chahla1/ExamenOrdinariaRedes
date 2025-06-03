# ExamenOrdinariaRedes

1. Una de las principales diferencias entre los modelos OSI y TCP/IP es la cantidad de capas: el modelo OSI está compuesto por 7 capas, mientras que el modelo TCP/IP se organiza en solo 4. En cuanto a su enfoque, el modelo OSI es teorico y fue diseñado como una referencia para comprender como deben comunicarse los sistemas, mientras que el modelo TCP/IP tiene un enfoque practico, basado en protocolos reales utilizados en las redes. Ademas, el modelo OSI divide las funciones de la capa de aplicacion en tres capas distintas (Aplicacion, Presentacion y Sesion), mientras que TCP/IP agrupa todas estas funciones en una sola capa de aplicación.

El modelo OSI es muy util como herramienta educativa y de diseño, ya que proporciona una estructura clara y bien definida. Sin embargo, no se implementa directamente en las redes reales, ya que no esta vinculado a protocolos específicos. Por el contrario, el modelo TCP/IP se basa en protocolos reales como TCP e IP, y es el estandar en la mayoria de las redes actuales, pero su estructura es menos modular y presenta una separacion de funciones menos detallada entre sus capas.


2. La capa de transporte, tanto en el modelo OSI como en el modelo TCP/IP, se encarga de ofrecer una comunicación confiable de extremo a extremo entre aplicaciones que se ejecutan en dispositivos diferentes. Esta capa actúa como un intermediario entre la capa de red y las aplicaciones, gestionando aspectos como el control de errores, el control de flujo y la segmentación de los datos.
En el caso de protocolos como TCP, la capa de transporte se encarga de establecer una conexión antes de enviar los datos, asegurando así que la comunicación sea fiable.
Por otro lado, UDP es un protocolo también ubicado en la capa de transporte, pero funciona de forma muy diferente. No establece una conexión previa ni implementa controles de error ni de orden, lo que lo convierte en un protocolo mucho más ligero y rápido. Sin embargo, al no ofrecer fiabilidad, los datos pueden perderse o llegar desordenados.

3. En las redes TCP/IP, el protocolo tradicionalmente utilizado para la transferencia de archivos es FTP (File Transfer Protocol). Este protocolo permite enviar y recibir archivos entre un cliente y un servidor a través de una red. Sin embargo, FTP no cifra la información, lo que lo hace vulnerable a ataques como la interceptación de contraseñas. Entre sus mejores alternativas destacan  SFTP (SSH File Transfer Protocol), que cifra tanto los comandos como los datos, ya que trabaja sobre el protocolo SSH, y FTPS (FTP Secure), que añade soporte para cifrado mediante TLS/SSL, proporcionando autenticación y confidencialidad.

Cuando un usuario escribe una URL en su navegador, su ordenador necesita conocer la dirección IP correspondiente para poder conectarse al servidor web. Aqui utilizamos el Sistema de Nombres de Dominio (DNS), cuya función es traducir nombres de dominio en direcciones IP.
El navegador pregunta al sistema operativo si ya conoce la IP asociada al nombre ingresado, si no la encuentra, se hace una solicitud a un servidor DNS local, proporcionado por el proveedor de Internet. Si el servidor local no tiene la dirección en su caché, la consulta se envía a un servidor raíz DNS, que responde indicando qué servidor es responsable del dominio de nivel superior. Luego, el proceso sigue con consultas a los servidores autoritativos, que conocen la dirección exacta del dominio solicitado.
Una vez obtenida la dirección IP, esta se envía al navegador, que finalmente establece la conexión con el servidor web correspondiente y carga la página.

4. Se comienza en la capa de aplicación, que es donde se encuentran los programas que usan los usuarios. Esta capa genera los datos que se quieren enviar y utiliza protocolos como HTTP, SMTP o DNS para darles un formato entendible. Una vez que los datos están listos, pasan a la capa de transporte, que se encarga de dividirlos en segmentos y garantizar que lleguen de manera ordenada y sin errores. Después, los datos llegan a la capa de Internet, donde se encapsulan en paquetes IP. Aquí se añaden las direcciones IP de origen y destino para que cada paquete sepa a dónde ir. Por último, la capa de acceso a red toma los paquetes IP y los convierte en tramas adecuadas para la red física, como Ethernet o Wi-Fi.

5.  𝐶 = 𝐵 × log ⁡ 2 ( 1 + SNR )
   SNR = 10^20/10 = 100
   B = 500 * 10^6 = 500000000
   Ahora aplicamos la formula:
   C = 500000000 * log(1 + 100) = 500000000 * 6.6582 = 3.33 gbps

6. a) 1.2 ghz - 0.3 ghz = 0.9ghz
   
   b)  1.2 ghz + 0.3 ghz = 1.5ghz

7. BPSK

QPSK

16-QAM

64-QAM

256-QAM

A medida que aumenta el número de símbolos por baudio, los puntos en el plano de constelación están más juntos, y el receptor necesita mayor precisión para distinguirlos. Si hay ruido, es más fácil que se confundan, lo que genera más errores. Por eso, modulaciones como 256-QAM transmiten más datos por símbolo, pero son muy sensibles al ruido, mientras que BPSK transmite menos datos, pero es más confiable.

8. a) 2048 + 144 = 2192 bytes
   
   b) 2192/512 = 4.28 , se necesitan 5 tramas en total.
   
   c) 512 * 9/4 = 1152 bytes transmitidos
   1152 - 512 = 640 bytes

   d) 512 / 1152 = 0.444 = 44.4%

9.a) El algoritmo de Dijkstra sirve para encontrar la ruta más corta entre un nodo origen y todos los demás nodos de un grafo, teniendo en cuenta que cada enlace tiene un coste. Sus pasos basicos son: Se parte del nodo origen asignando una distancia 0, a todo lo demas se le asigna infinito; se marca el nodo actual como visitado; se calcula la 
distancia total desde el origen hasta cada nodo vecino del actual; si esa nueva distancia es menor de la que se tenia antes, se actualiza; se selecciona el nodo no visitado con menor distancia conocida y se repite el proceso, y el proceso termina cuando se han visitado todos los nodos.

b) A diferencia del enrutamiento por inundación, el algoritmo de Dijkstra encuentra la ruta mas corta y eficiente, evita el trafico innecesario, usa tablas de enrutamiento, y, aunque es mas lento de calcular, es muy eficiente una vez establecido.
Por otro lado, el Flooding envia el paquete por todos los caminos posibles, no necesita conocer la topologia de la red, garantiza que el mensaje llegue pero genera mucho trafico y puede causar tormentas de paquetes si no se controla.

10.a) IP: 172.29.152.0
 en binario: 10101100.00011101.10011000.00000000

Máscara: 255.255.248.0
 en binario: 11111111.11111111.11111000.00000000
 eso nos indica que los primeros 21 bits son de red y los últimos 11 bits son de host.
 Bits de red (primeros 21): 10101100.00011101.100

Bits de host (últimos 11): 11111111111

Juntando todo:
 10101100.00011101.10011111.11111111
 En decimal: 172.29.159.255

 b)Máscara 255.255.252.0 → en binario: 11111111.11111111.11111100.00000000
 Son 22 bits de red (porque 252 en binario es 11111100).
 52 es el múltiplo más cercano a 53 
 Entonces, el bloque de subred empieza en:
 172.22.52.0
 Con una máscara /22, los bits de host son 10 (porque 32 – 22 = 10), lo que da 2¹⁰ = 1024 direcciones por subred.

Entonces, el rango de direcciones va de:

Primera dirección válida (host): 172.22.52.1

Última dirección válida (host): 172.22.55.254

Dirección de broadcast: 172.22.55.255
 Rango válido: 172.22.52.1 a 172.22.55.254

 11.a) 32 -26 = 6 bits paara host
 2^6 = 64 direcciones por subred
 Dirección de subred: 172.30.67.192
 Dirección de broadcast:
 Sumamos 64 direcciones: 192 + 64 = 256, la dirección de broadcast es 172.30.67.255 porque el maximo es 255
 entonces la ultima direccion valida es 172.30.67.254

 b)Convertimos la máscara:
255.255.255.192 en binario: 11111111.11111111.11111111.11000000
 Eso indica una /26, 6 bits para hosts.
 2^6 = 64
 2 se reservan
 64 - 2 = 62

 12.a) Una máscara /23 significa que hay 23 bits para la red y 9 bits para los hosts (32 – 23 = 9). Eso implica que cada bloque tiene 2^9 = 512 direcciones.
 Ahora buscamos a qué subred pertenece 172.18.171.190.
Sabemos que la red es clase B (los dos primeros octetos: 172.18), así que trabajamos con el tercer y cuarto octeto.
En binario:
171 = 10101011
Como estamos en /23, solo se usan 7 bits del tercer octeto (8 del tercero y 1 del cuarto).
las subredes se crean de 2 en 2 a partir del tercer octeto.
El valor más bajo múltiplo de 2 menor o igual que 171 es 170
Por tanto:
Dirección de subred: 172.18.170.0
Dirección de broadcast: 172.18.171.255
Rango de hosts: desde 172.18.170.1 hasta 172.18.171.254

b)Número de subredes = 2^s, donde s es el número de bits prestados para subredes.
2^2 = 4 subredes
hay que dar 2
la nueva mascara seria /24 + 2 = 26

13.a) Cuando dos dispositivos quieren comunicarse usando TCP, primero deben establecer una conexión confiable. Para eso, TCP usa un proceso llamado Three-Way Handshake
SYN (Synchronize):
El cliente envía un mensaje al servidor con una bandera SYN y un número de secuencia inicial.
Esto indica que quiere comenzar una conexión.

SYN-ACK:
El servidor responde con un mensaje que lleva las banderas SYN y ACK.
Reconoce el número de secuencia del cliente y además envía su propio número de secuencia.

ACK:
El cliente responde con un mensaje de confirmación que lleva la bandera ACK, reconociendo el número de secuencia del servidor.

b)Cuando uno de los dispositivos quiere cerrar la conexión, se hace un proceso similar, pero con cuatro pasos:

FIN:
El cliente (o servidor) envía un mensaje con la bandera FIN, diciendo que ya no tiene más datos para enviar.

ACK:
El otro lado responde con un mensaje de ACK, confirmando que recibió el FIN.

FIN:
Ahora ese segundo dispositivo también envía su propio mensaje FIN para cerrar su lado de la conexión.

ACK:
Finalmente, el primero responde con un ACK y la conexión se cierra por completo.

14.Multiplexación descendente es el proceso por el cual la capa de transporte, como TCP, recibe datos de varias aplicaciones que se están ejecutando al mismo tiempo en un dispositivo y los organiza para enviarlos a través de la red. Por ejemplo, si tienes abierto un navegador web, un programa de correo y una videollamada, todos están enviando datos a la red. TCP utiliza números de puerto para distinguir de qué aplicación viene cada flujo de datos. 
Multiplexación ascendente es el proceso contrario. Es cuando los datos llegan desde la red hacia un dispositivo y TCP los separa correctamente para entregarlos a la aplicación correcta. Lo hace mirando los números de puerto de destino incluidos en los segmentos TCP.

15. a) Conversión de unidades

Primero pasamos las unidades a formas compatibles:

RTT = 50 ms = 0.05 segundos

Ancho de banda = 100 Mbps = 100,000,000 bits por segundo

MSS = 1500 bytes = 1500 × 8 = 12,000 bits

b) Cálculo del tamaño óptimo de ventana

La fórmula es:
Ventana óptima = Ancho de banda × RTT

Sustituimos:
Ventana óptima = 100,000,000 × 0.05 = 5,000,000 bits

Para pasarlo a bytes:
5,000,000 ÷ 8 = 625,000 bytes

16.TCP utiliza varios mecanismos para controlar la congestión en la red y evitar que se saturen los enlaces. Uno de los más importantes es el algoritmo de arranque lento, también conocido como slow start. Este algoritmo se activa al inicio de una conexión o después de detectar una pérdida de paquetes. En lugar de enviar muchos datos de golpe, el emisor empieza enviando una pequeña cantidad de segmentos y va aumentando el número de segmentos enviados de forma exponencial, duplicando la cantidad en cada ronda de confirmaciones. Cuando se alcanza un cierto umbral, TCP cambia al modo de evitación de congestión, donde ya no crece de manera rápida, sino más lentamente, para evitar causar problemas si la red está llegando a su límite. 
Otro mecanismo importante es el algoritmo de Nagle, que está pensado para reducir la cantidad de pequeños paquetes que se envían por la red. Este algoritmo agrupa pequeños mensajes enviados por una aplicación antes de enviarlos como un único segmento. Esto mejora la eficiencia, especialmente en conexiones que generan muchas transmisiones pequeñas, como las de comandos o chats.
El algoritmo de Clark complementa al de Nagle y busca evitar que el receptor envíe confirmaciones (ACKs) por cada pequeño fragmento de datos recibido. En lugar de responder rápidamente a cada paquete pequeño, espera a tener más datos disponibles o a que pase un tiempo determinado.

17.a) SMTP se utiliza para enviar correos electrónicos desde un cliente de correo hacia un servidor o entre servidores. Por eso, su función está relacionada con el envío, no con la descarga de mensajes.

En cambio, POP3 e IMAP se utilizan para recibir correos. POP3 es un protocolo más simple y funciona descargando los mensajes del servidor al dispositivo del usuario. Generalmente, al usar POP3 los correos se eliminan del servidor después de descargarse, lo que puede ser un problema si se accede desde varios dispositivos, ya que los mensajes no se sincronizan. IMAP, por el contrario, mantiene los mensajes en el servidor y permite sincronizarlos en varios dispositivos. Esto lo hace más útil hoy en día.

b)  Este protocolo permite la comunicación entre navegadores web y servidores. Funciona mediante peticiones que el cliente (por ejemplo, un navegador) envía al servidor para obtener o enviar información. Los métodos más comunes que se usan en estas peticiones son GET, que se emplea para solicitar recursos como páginas web; POST, que se utiliza para enviar datos al servidor, como formularios; PUT, que sirve para actualizar recursos existentes; y DELETE, que permite eliminar información. 
Por otro lado, FTP es un protocolo diseñado específicamente para la transferencia de archivos. A diferencia de HTTP, que usa una única conexión para la mayoría de sus operaciones, FTP utiliza dos conexiones separadas: una para el control, donde se envían comandos como iniciar sesión o cambiar de directorio, y otra para la transferencia real de archivos. 

18. a) el streaming es una forma de transmitir contenido multimedia, como video o audio, en tiempo real o bajo demanda, sin necesidad de descargarlo por completo antes de verlo. Existen distintos tipos de streaming, cada uno con sus características.

El UDP streaming utiliza el protocolo UDP para enviar datos rápidamente, sin asegurarse de que todos los paquetes lleguen ni en el orden correcto. Por ejemplo, se usa en transmisiones deportivas en vivo o videollamadas.
El HTTP streaming funciona utilizando el protocolo HTTP y se basa en descargar el contenido por partes a medida que se reproduce. Aunque es más lento que UDP, tiene la ventaja de que se adapta bien a las redes modernas. Es común en plataformas como YouTube o Spotify.
Por último, el Adaptive HTTP Streaming o DASH es una versión más avanzada del HTTP streaming. Este método detecta la velocidad y calidad de la red del usuario y adapta automáticamente la calidad del video para evitar interrupciones. Netflix y Amazon Prime usan este tipo de streaming.

b)es una tecnología que permite realizar llamadas telefónicas utilizando Internet en lugar de la red telefónica tradicional. Funciona convirtiendo la voz en paquetes de datos que se transmiten por la red, de forma similar a cómo se envía un correo electrónico o se transmite un video.Algunos problemas comunes en VoIP incluyen el retardo, que ocurre cuando hay un retraso notable entre lo que se dice y lo que se escucha; la pérdida de paquetes, que puede provocar cortes en la voz; y el eco, cuando se escucha lo que uno dijo con retraso.

19. a)Una técnica común es el uso de buffering en el cliente. Consiste en que el dispositivo del usuario (como un móvil o un ordenador) guarda temporalmente una pequeña parte del video o audio antes de reproducirlo. Esto permite compensar posibles interrupciones en la red, ya que mientras se reproduce un trozo, se va descargando el siguiente. Por ejemplo, en YouTube, cuando ves que se carga una barra gris antes de la parte roja del video, eso es buffering.
    Otra técnica es el marcado de paquetes mediante DiffServ (Servicios Diferenciados). En este caso, cada paquete de datos se marca según su prioridad. Por ejemplo, los paquetes de voz o video en tiempo real se marcan con alta prioridad para que los routers los traten con preferencia, y así tengan menos retraso y menos pérdida.

    b) El modelo Best-Effort es el más simple.Aquí, la red no garantiza ni velocidad ni calidad. Todos los datos se tratan igual, si hay congestión, puede haber retrasos o pérdida de información. Este modelo es suficiente para cosas que no requieren tiempo real, como navegar por internet o enviar correos.
    En cambio, los Servicios Multiclase (Multiclass Services) ofrecen distintos niveles de servicio según el tipo de tráfico.Esto permite garantizar una mejor calidad para aplicaciones sensibles al retardo, como videollamadas o juegos en línea. Se usan técnicas como reservas de ancho de banda, colas con prioridades y marcado de paquetes.

    20.  existen varias áreas fundamentales que deben protegerse para garantizar comunicaciones seguras. Una de ellas es la confidencialidad, que consiste en asegurarse de que la información solo sea vista por las personas autorizadas. Para lograr esto, se utiliza el cifrado, que transforma los datos en un formato ilegible para quien no tenga la clave correcta. Por ejemplo, cuando enviamos un mensaje cifrado, aunque alguien lo intercepte, no podrá entenderlo sin la clave.

Otra área importante es la autenticación, que busca verificar que quien está accediendo a la red o a un servicio es realmente quien dice ser. Esto se puede hacer mediante contraseñas, pero también con métodos más seguros como certificados digitales o sistemas biométricos (como huellas o reconocimiento facial). De esta forma, se evita que alguien se haga pasar por otra persona.
También está el concepto de no repudio, que significa que una persona no puede negar haber enviado un mensaje o realizado una acción. Para esto se utilizan las firmas digitales, que son como un sello único ligado al emisor del mensaje. Así, si alguien firma un documento digital, queda constancia de que lo hizo.

Por último, la integridad se refiere a garantizar que los datos no han sido alterados durante su transmisión. Si un mensaje es modificado por un atacante en el camino, debe poder detectarse. Para esto se usan mecanismos como los hashes o códigos de verificación, que permiten comprobar que el mensaje recibido es exactamente igual al que fue enviado.

21.En el caso del cifrado simétrico, tanto quien envía como quien recibe el mensaje utilizan la misma clave para cifrar y descifrar los datos. Esto quiere decir que primero ambas partes deben compartir esa clave de forma segura. Este tipo de cifrado es muy rápido y eficiente, por eso se usa mucho cuando hay que cifrar grandes volúmenes de datos. Algunos ejemplos comunes de algoritmos simétricos son AES y DES.

En cambio, el cifrado asimétrico utiliza dos claves distintas pero relacionadas entre sí: una clave pública, que puede conocer todo el mundo, y una clave privada, que solo conoce el dueño. Si alguien quiere enviar un mensaje seguro, lo cifra con la clave pública del destinatario, y solo esa persona podrá descifrarlo usando su clave privada. Aunque este método es más seguro para intercambiar claves y verificar identidades, es mucho más lento y no se suele usar para cifrar grandes cantidades de datos. Dos ejemplos conocidos de cifrado asimétrico son RSA y ECC. En la práctica, los sistemas seguros suelen combinar ambos tipos.

22.El algoritmo RSA es un sistema de cifrado asimétrico, lo que significa que usa dos claves diferentes: una pública para cifrar y una privada para descifrar. Se basa en la dificultad de factorizar números grandes. El proceso tiene dos fases importantes: la generación de claves y el cifrado/descifrado del mensaje.
se eligen dos numeros primos ( p = 3 y q=11)
n = p * q = 3*11 = 33
φ(n)=(p−1)×(q−1) = 2 * 10 = 20
Ahora elegimos un número 𝑒 que sea coprimo con 20
e =7
d * e = 1
probamos con 3:
3 * 7 =21 mod 20 =1
por lo tanto:
clave publica= (e=7, n = 33)
clave privada: (d=3, n =33)
calclulamos:
4^7 =16384
16384 mod33 = 16

a) Un firewall es un sistema de seguridad que se coloca entre una red confiable (como una red local) y otra no confiable (como Internet). Su función principal es controlar el tráfico de red, permitiendo o bloqueando paquetes según unas reglas predefinidas.

Existen diferentes tipos de firewalls. Uno es el firewall de filtrado de paquetes, que revisa los encabezados de los paquetes (como la dirección IP, el puerto y el protocolo) y los deja pasar o no según reglas simples. Otro tipo es el firewall con inspección de estado, que no solo revisa los encabezados, sino que también mantiene un registro del estado de las conexiones (por ejemplo, si ya está establecida una comunicación) y toma decisiones más inteligentes sobre qué permitir o bloquear.

b)Una VPN (Red Privada Virtual) permite que un usuario se conecte de forma segura a una red a través de Internet, como si estuviera físicamente dentro de esa red. Por ejemplo, un empleado puede acceder a los recursos de la red de su empresa desde casa usando una VPN.

IPSec, en cambio, es un conjunto de protocolos que se usa para asegurar las comunicaciones a nivel de red. IPSec puede cifrar y autenticar los paquetes IP, y muchas VPN usan IPSec como base para garantizar seguridad.

c) SSL (Secure Sockets Layer) y su sucesor TLS (Transport Layer Security) son protocolos que se usan para proteger la comunicación en Internet, especialmente en páginas web.
Cuando visitas una página con HTTPS, el navegador y el servidor web usan TLS para cifrar los datos que se envían entre ambos. Esto evita que otras personas puedan ver lo que estás escribiendo o recibiendo, como contraseñas, correos o información personal.

24. El DNS Spoofing es un tipo de ataque en el que un atacante falsifica las respuestas del sistema DNS para engañar al usuario. El DNS es como la “guía telefónica” de Internet: traduce nombres de páginas en direcciones IP, que es lo que entienden los dispositivos.

Cuando ocurre un DNS Spoofing, el atacante logra que el usuario reciba una respuesta falsa del DNS, llevándolo a un sitio falso que parece real. Por ejemplo, podrías escribir www.banco.com y terminar en una página falsa que copia el diseño del banco, con el objetivo de robar tus datos.
Este tipo de ataque rompe la integridad de la comunicación, porque el usuario cree que está visitando un sitio legítimo cuando en realidad no lo está.

b)DNSSEC (Domain Name System Security Extensions) es una extensión del sistema DNS que añade seguridad mediante firmas digitales.
Cuando se usa DNSSEC, cada respuesta DNS viene acompañada de una firma criptográfica que el navegador o sistema del usuario puede verificar. Esta firma confirma que la respuesta proviene del servidor DNS auténtico y que no ha sido alterada.


 
   
   
   
 

