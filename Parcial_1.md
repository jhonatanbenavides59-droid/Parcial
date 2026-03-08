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

#### E:
Define
qué es un OID y cuál es su relación con la MIB Si
un administrador quiere saber la cantidad de bytes que ha
recibido una interfaz de red, ¿qué operación SNMP Get
Set, Trap debe utilizar y por qué no sería adecuado usar
un Trap para esto?

El OID es la dirección específica de un dato dentro de ese árbol MIB. Es una cadena de números separados por puntos que identifica de forma única una característica su relación con la MIB es el mapa o la estructura jerárquica, mientras que el OID es la coordenada exacta para encontrar un dato específico dentro de ese mapa. Sin la MIB, los números del OID no tendrían significado; sin el OID, no podrías extraer información de la MIB.

### Punto dos

#### A:
Identificar
y explicar cada uno de los campos de la
cabecera Ethernet ¿Qué significa el valor 0 x 0800 en el campo "tipo"


<img width="367" height="160" alt="IPv6" src="https://github.com/user-attachments/assets/2acd5fc8-a1fa-46d6-bc9f-b4a419e00d88" />

Para el caso mencionado es se debe usar SNMP Get debido a que el administrador tiene un rol activo. Él es quien necesita la información en un momento específico a diferencia del Trap es una notificación no solicitada que el dispositivo envía al administrador cuando ocurre un evento crítico 

Cuando la tarjeta de red recibe la trama y lee 0x0800, recibe la trama y verifica que la dirección de destino es correcta, sabe que debe entregar el contenido al software que maneja las direcciones IP, de forma más sencilla de verse si el valor es 0x0800 el receptor busca direcciones IP 192.168.1.10, a diferencia de que si es valor fuera 0x86DD el receptor esperaría una dirección de 128 bits de IPv6 o en un caso de que el valor fuera 0x0806 el receptor sabría que es un paquete ARP.

#### B: 
En
la cabecera IPv 4 ¿qué significan los campos Protocolo y
TTL? ¿Por qué es importante el TTL en red?

En este caso se identifica un valor de TCP (como en tu captura, para tráfico web HTTP), este campo indica cuál es el protocolo de la Capa de Transporte (Capa 4) que viene encapsulado dentro del paquete IP.
El protocolo TTL es un contador que indica cuántos routers puede atravesar el paquete antes de ser descartado, funciona cada vez que el paquete pasa por un router, este le resta 1 al valor del TTL. Si el valor llega a 0, el router descarta el paquete y envía un mensaje de error al emisor.
El TTL es importante en la red ya que es un mecanismo de seguridad que evita que internet colapse algunas funciones son, evitar Bucles Infinitos (Routing Loops), diagnóstico de red, Identificación del Sistema Operativo.

#### C: 

La función del ACK (acuse de recibido) le confirma al emisor que los datos enviados anteriormente fueron recibidos correctamente.
La función del PSH (Empujar): Instruye al receptor a pasar los datos directamente a la aplicación (en este caso, al servidor web) de forma inmediata.

El Servicio del puerto 80 es el estándar mundial para el protocolo HTTP (Hypertext Transfer Protocol), funciona como la "puerta de entrada" específica a un servicio dentro de un servidor que tiene una sola dirección IP, esto indica que el cliente (192.168.1.10) está intentando acceder a un servidor web para solicitar una página que no tiene cifrado (tráfico en texto plano).

#### D:
Si
este mismo paquete se enviara usando IPv 6 ¿qué cabecera de
IPv 6 reemplazaría a la cabecera IPv 4 mostrada y cuál sería una
mejora notable en su procesamiento por parte de los routers

La IP origen en IPV4 es 192.168.1.10 el cambio que tendría a usar IPV6 seria 2001:db8::1 pasa de 32 bits a 128 bits, la mejora más significativa es la simplificación del procesamiento en el hardware de red como lo son eliminación del Checksum (suma de verificación), eliminación de la fragmentación en el Router, cabecera de tamaño Fijo y alineada.

### Punto tres: 

Desde
#### A: 
la CMD de Windows, ejecutar el comando Pathping 8.8.8.8. Explicar qué información proporciona este comando quedaría un ping o un tracert.

Al ejecutar pathping 8.8.8.8 se utiliza una herramienta híbrida que combina lo mejor de ping y tracert, con una capacidad de diagnóstico, el ping solo te dice si un destino está vivo y cuánto tarda en responder, el tracert muestra la ruta (los routers) que sigue el paquete hasta llegar al destino.

#### B: 

Describir
el proceso que sigue pathping para obtener sus
resultados

<img width="380" height="432" alt="traza pathping" src="https://github.com/user-attachments/assets/63638a95-04bc-40ec-b7c6-f62c8cb83ecd" />

La función del pathping es primero hace un rastro de la ruta (como tracert) y luego se queda analizando cada salto durante un periodo de tiempo (normalmente 250 segundos) para medir la pérdida de paquetes detallada, se pueden interpretar dos 3 cosas con el detalla de la tabla primera pérdida de paquetes por salto, validando que porcentaje e perdida se tuvo en cada salto, análisis de congestión envía paquetes por un tiempo para validar si el router está saturado y la latencia que se tenga por nodo, de igual manera podemos ver la latencia media por nodo muestra una visión más estable de la calidad de la conexión en cada punto del trayecto. 

#### C: 

¿Qué
comando de Windows (o herramienta de línea de
comandos) podría utilizar para " por el árbol MIB y
obtener todos los valores de la interfaz del router en la
IP 192 168 1 1

Se debe realizar la instalación de unas herramientas Net-SNMP que complemente el Windows para poder usar el comando snmpwalk -v 2c -c public 192.168.1.1 1.3.6.1.2.1.2 que nos dará la siguiente información:
-	ifIndex: El número de identificación de cada puerto.
-	ifDescr: El nombre de la interfaz (ej. GigabitEthernet0/1).
-	ifType: El tipo de conexión (Ethernet, loopback, etc.).
-	ifOperStatus: Si la interfaz está activa (up) o caída (down).
-	ifInOctets / ifOutOctets: El contador de tráfico (bytes que entran y salen), ideal para medir el consumo de ancho de banda.

#### D:
Si el router envía un mensaje authenticationFailure trap
al gestor SNMP, ¿Qué evento lo ha provocado y cuál es la
ventaja de recibir un Trap en lugar de estar consultando
constantemente polling )el estado del router
Cuarto Punto

Si se recibe un mensaje authenticationFailure trap es un evento provocado por un intento de acceso no autorizado al router. específicamente, ocurre cuando alguien (o algún software) intenta realizar una consulta SNMP, con credenciales que no están autorizadas, la ventaja que tiene el trap sobre el polling, es su fiabilidad y rapidez de detención debido a que e trap se enfoca en la falla enviando información de manera oportuna lo que evita congestiones en la red para que se pueda prestar la atención necesaria a tiempo.

#### Punto 4

Realizar
un análisis paso a paso del proceso completo,
desde que se escribe el primer comando de verificación
hasta que GitHub confirma la recepción de los cambios
Para cada paso, usted deberá

### A:

¿Qué
comando usaría para verificar que su equipo tiene
conectividad IP con los servidores de GitHub? Ejecutar ese
comando y obtiener respuesta Explicar qué capa del modelo OSI
está verificando este comando y qué protocolo utiliza

A:

Para validar si mi equipo tiene conectividad a Github.com usaría 3 comandos para recopilar la mayor cantidad de datos, el primero sería el PING que usa el protocolo ICMP se valida que el ping envia y recibe 4 paquetes sin perdidas, si revisamos el modelo OSI se ubica en la capa 3 (capa de red) su función principal es comprobar que un paquete puede ser enrutado desde la dirección IP de origen hasta la dirección IP de destino a través de diferentes redes y routers

Si desglosamos el ping logramos observar que Los servidores de GitHub suelen utilizar sistemas operativos basados en Linux, los cuales inician sus paquetes con un TTL de 64, el paquete salió con 64 y llegó a tu equipo con 52, significa que el paquete atravesó exactamente 12 routers desde los servidores de GitHub hasta tu ubicación en Colombia, podemos, otra parte seria el tiempo de respuesta de  87ms - 986s (Latencia) es decir, lo que tarda el paquete en ir hasta el servidor y regresar a tu PC que se pueden tomar como un tiempo aceptable para la conexión.

<img width="363" height="176" alt="Ping Github" src="https://github.com/user-attachments/assets/19f8933c-844b-4d47-bdb1-e0cffeb8ffea" />

El siguiente comando que se podria usar es el tracert este comando se puede usar para una verificación de conectividad más profunda, su función es identificar cada uno de los nodos (routers) que procesan el paquete basándose en sus direcciones IP, nos brinda el punto exacto de la red si se está produciendo un fallo o un cuello de botella, al igual que el ping usa el protocolo ICMP 

<img width="534" height="269" alt="Tracert github" src="https://github.com/user-attachments/assets/6c5a1095-788a-4cb6-ad8b-b6fe6cd7f0aa" />




