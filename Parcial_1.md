# Parcial uno 
## jhonatan Benavides 
Conmutacion y Teletrafico
### Punto 1:
#### A: 
Explicar
la diferencia fundamental entre la latencia y el jitter ¿Cuál de estas dos métricas tendría un impacto más negativo en una llamada VoIP y por qué?
Respuesta:
la diferencia fundamental entre la latencia y el jitter ¿Cuál de estas dos métricas tendría un impacto más negativo en una llamada VoIP y por qué?
- La latencia es el tiempo que tarda en enviarse un mensaje del punto A al punto B, en una llamada se puede identificar cuando una emisor habla pero al momento de responder el receptor se demora un poco en responder, pero en realidad es la latencia del mensaje.
  
- el Jitter es el orden en que llega el mensaje, el mensaje llega con fluctuaciones en diferentes tiempos, lo que causa en una llamada de Voz IP se escucharía a la persona distorsionada o robotizada debido a que el sistema no reconoce la alteración del tiempo.

#### B:
Una aplicación envía datos usando protocolo TCP, mientras que otra usa UDP para la misma tarea de transmisión de video ¿Cuál es más eficiente en términos de throughput y cuál ofrece mayor control de la pérdida de paquetes? Justifique s u respuesta basándote en la " de sus cabeceras "

El protocolo TCP se enfoca en la calidad del mensaje debido a que tiene un mayor enfoque en él envió de los paquetes se envían a través del mensaje lo que brinda una mayor fiabilidad en el mensaje, el protocolo UDP tiene como prioridad la velocidad de la entrega mensaje ya que para el es más importante el tiempo que la calidad, para el throughput el mas eficiente seria el TCP porque este protocolo se enfoca en validad la cantidad útil de los datos que llega en el mensaje, como premisa de esto la fiabilidad es lo mas importante.

#### C:
Al ejecutar el comando arp a” en la CMD de Windows, se
obtienen una lista de direcciones IP y direcciones físicas
¿Qué protocolo de la suite TCP/IP llena esta tabla y cuál es
su función principal dentro de una red local? Relacionar la
respuesta con la estructura de una trama Ethernet

El Protocolo: ARP (Address Resolution Protocol), en una red local (LAN), las computadoras no se envían datos basándose únicamente en la dirección IP. La dirección IP sirve para identificar un dispositivo en la red lógica, pero para que la información llegue físicamente de una tarjeta de red a otra, se necesita la dirección MAC (dirección física).
La Trama Ethernet es un mensaje que se envía por medio de la LAN. Para que ese mensaje pueda viajar por un cable, pero el computador solo reconoce la IP del equipo, para validar que llegue al destino que desea el protocolo ARP identifica la dirección MAC del equipo destino para que el mensaje llegue de manera correcta

#### D: 
Mencionar
dos diferencias clave entre las
arquitecturas SNMPv 2 c y SNMPv 3 Enfocarse en los aspectos
de seguridad y el tipo de mensajes que manejan

Para entender el protocolo SNMP (Simple Network Management Protocol), debemos ver a la versión 2c como la base funcional y a la versión 3 como la armadura de seguridad necesaria para redes modernas.
Esta es la diferencia más crítica. Mientras que SNMPv2c confía en una "palabra clave" simple, SNMPv3 introduce un marco robusto.
SNMPv2c (Seguridad basada en comunidad): Utiliza una cadena de texto plano llamada Community String (comúnmente "public" o "private"). Si alguien intercepta la trama Ethernet con un analizador de tráfico, puede leer la clave y tomar control del dispositivo. No hay validación de quién envía el mensaje.

SNMPv3 (User-based Security Model - USM): Introduce conceptos de criptografía real. Permite definir usuarios y ofrece tres niveles de seguridad,noAuthNoPriv: Sin autenticación ni cifrado (similar a v2c), authNoPriv: Autenticación mediante hashing (MD5 o SHA) para asegurar que el remitente es quien dice ser,authPriv: El nivel más alto; además de autenticar, cifra los datos (DES, AES) para que nadie pueda leer el contenido del mensaje, aunque capture la trama.

