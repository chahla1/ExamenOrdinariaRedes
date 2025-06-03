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

10.
   
   
   
 

