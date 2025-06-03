# ExamenOrdinariaRedes

1. Una de las principales diferencias entre los modelos OSI y TCP/IP es la cantidad de capas: el modelo OSI está compuesto por 7 capas, mientras que el modelo TCP/IP se organiza en solo 4. En cuanto a su enfoque, el modelo OSI es teorico y fue diseñado como una referencia para comprender como deben comunicarse los sistemas, mientras que el modelo TCP/IP tiene un enfoque practico, basado en protocolos reales utilizados en las redes. Ademas, el modelo OSI divide las funciones de la capa de aplicacion en tres capas distintas (Aplicacion, Presentacion y Sesion), mientras que TCP/IP agrupa todas estas funciones en una sola capa de aplicación.

El modelo OSI es muy util como herramienta educativa y de diseño, ya que proporciona una estructura clara y bien definida. Sin embargo, no se implementa directamente en las redes reales, ya que no esta vinculado a protocolos específicos. Por el contrario, el modelo TCP/IP se basa en protocolos reales como TCP e IP, y es el estandar en la mayoria de las redes actuales, pero su estructura es menos modular y presenta una separacion de funciones menos detallada entre sus capas.


2. La capa de transporte, tanto en el modelo OSI como en el modelo TCP/IP, se encarga de ofrecer una comunicación confiable de extremo a extremo entre aplicaciones que se ejecutan en dispositivos diferentes. Esta capa actúa como un intermediario entre la capa de red y las aplicaciones, gestionando aspectos como el control de errores, el control de flujo y la segmentación de los datos.
En el caso de protocolos como TCP, la capa de transporte se encarga de establecer una conexión antes de enviar los datos, asegurando así que la comunicación sea fiable.
Por otro lado, UDP es un protocolo también ubicado en la capa de transporte, pero funciona de forma muy diferente. No establece una conexión previa ni implementa controles de error ni de orden, lo que lo convierte en un protocolo mucho más ligero y rápido. Sin embargo, al no ofrecer fiabilidad, los datos pueden perderse o llegar desordenados.
 

