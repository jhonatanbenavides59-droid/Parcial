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
Al
ejecutar el comando arp a” en la CMD de Windows, se
obtienen una lista de direcciones IP y direcciones físicas
¿Qué protocolo de la suite TCP/IP llena esta tabla y cuál es
su función principal dentro de una red local? Relacionar la
respuesta con la estructura de una trama Ethernet

El Protocolo: ARP (Address Resolution Protocol), en una red local (LAN), las computadoras no se envían datos basándose únicamente en la dirección IP. La dirección IP sirve para identificar un dispositivo en la red lógica, pero para que la información llegue físicamente de una tarjeta de red a otra, se necesita la dirección MAC (dirección física).
