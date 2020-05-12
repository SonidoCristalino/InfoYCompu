

# Modelo capa de redes
----------------------
Modelo de capas: 1980. Debido a la cantidad grande de redes, se tuvo que estandarizar los diferentes sistemas, dado que cada uno
de las redes trabajan con distintas formas, distintos ruters, protocolos, etc. Se trató de unificar criterios.  Protocolo nos
dicen las reglas que deben seguir en la comunicación.

# Protocolo
-----------
Un protocolo define las reglas que deben seguir tanto el emisor como el receptor y todos los dispositivos intermedios para poder
comunicarse de manera efectiva.

	Capas: la función de las capas es dividir las tareas en cada una de ellas. Cada capa utiliza un protocolo distinto para
	esos trabajos que tienen que hacer.
		- El ejemplo que está en las filminas es de dos amigas que se cruzan por la calle y los protocolos que se dan por
		  sobre entendidos sobre cómo se entabla esa conversación.
		- Otro ejemplo distinto puede ser el profesor delante de la clase, el protocolo ya cambia con respecto al anterior
		  porque el profesor realiza un monólogo, los alumnos tienen que levantar la mano para hablar, etc.
		- En la filmina hay un ejemplo de las distintas capas implementándose con el servicio postal para la emisión de
		  una carta (Como el ejemplo del avión de Kurose).

	* Beneficios:
		- Ayuda en el diseño de protocolos, al tener menos funciones.
		- Los cambios en una capa son transparentes para el resto. (Es posible cambiar el protocolo de una capa sin que el
		  resto se entere).
		- Facilita el mantenimiento y actualización del sistema y permite la identificación y relación de las partes
		  complejas de éste.

	* Restricciones:
		- La finalidad de cada capa es darle servicio a inmediata superior.
		- Una capa sólo utiliza servicios de la capa inferior.
		- La primera capa sólo es la que puede acceder a los medios de transmisión.


## Principios de las capas de Protocolos (Forouzan):
----------------------------------------------------

- Primer principio: Se establece que si queremos una comunicación bidireccional entonces deberemos construir cada capa para
  permita realizar tareas opuestas, cada una en una dirección.
- Segundo prinicpio: El segundo pincipio establece que cada capa que se encuentre a ambos extremos de la conexión serán totalmente
  iguales (la capa que se encarga da le encriptación será al otro extremo de la comunicación igual a ella).

Lo que sucede en una capa, es transparente de lo que sucede en las demás. Los beneficios de tener un modelo de capa, es facilitar
el mantenimiento del sistema, los cambios son más fáciles y transparentes para el resto. También ayuda a diseñar las funciones que
implementará cada capa


# ¿Cómo es el flujo del mensaje? (Sacado de la clase nº 2):
	- El navegador genera un mensaje HTTP (capa de Aplicación). Y se lo pasa a la capa inferior.
	- La capa de Transporte toma este mensaje, lo encapsula y le añade una cabecera propia para transformarlo en un segmento.
	  Luego lo pasa a la capa inferior.
	- La capa de Red, toma este segmento, lo vuelve a encapsular y le añade una cabecera propia, transformandolo en un
	  datagrama.
	- La capa de Enlace toma nuevamente este datagrama y le añade su propia cabecera para convertirlo en una trama que será
	  transmitida por la última capa (La capa Física).
	- La capa Física es la encargada de transportar esta trama a través de los distintos enlaces hasta el host destino.

Todo este flujo se denomina *encapsulamiento*. Cuando la trama llega al destino, el host que lo recibe debe *desencapsularlo*
(realizando el proceso inverso antes descripto) donde cada capa mira el encabezado que le corresponde, y lo pasa a la capa
superior.

# Capas de Red
¿Por qué se organiza en capas? Porque ayuda a organizar y a identificar las relaciones de elementos de un sistema complejo como
son las redes de ordenadores. La modularización facilita el mantenimiento y la actualización del sistema. Algunas funcionalidades
se implementan en varias capas y a veces se necesita información para una capa, que se encuentra en otra distinta que la propia,
perdiendo la independencia entre ellas.
Hay servicios que si no están implementados en la capa, se pueden introducir metiendo capas intermedias, como por ejemplo la
seguridad que para ello se mete una nueva capa que utiliza el protocolo SSL.

# Pila de Protocolos de Internet en el modelo TCP / IP
	1. Aplicación: Es la capa más cerca al usuario y donde se encuentran las aplicaciones de red que intercambian *MENSAJES*.
	   Los protocolos utilizados en este capa son por ejemplo: FTP,SMTP, HTTP.  Esta capa le pasa los mensajes que quiere
	   enviar a su capa inferior.
	2. Transporte: La capa de transporte recibe ese mensaje y mediante un programa, lo convierte en los denominados
	   *SEGMENTOS* pasando estos a la capa inferior. Los protocolos por ejemplo son: TCP o UDP.
	3. Red(IP): La capa de Red de internet se caracteriza por tener un único protocolo, que es el denominado IP (Internet
	   Protocol), el mismo convierte el segmento en *DATAGRAMAS* para enviarlos desde la máquina de origen a la máquina
	   destino.
	4. Enlace: Esta capa, toma el datagrama de la capa superior y la convierte en una *TRAMA* que enviará al siguiente
	   elemento de la red y NO al final, puede ser enviado por 3G, Wifi, WiMax, fibra óptica, o el enlace que sea.
	5. Física: En esta capa se encuentra el enlace físico: Cable o aire, por el que van a viajar los bits.

# Modelo OSI:
	- Sin un sistema de protocolos, cada fabricante de dispositivos podría implementar las comunicaciones como mejor les
	  pareciese.
	- Sistema abierto, varios protocolos permiten que dos dispositivos se comuniquen entre si.
	- El Modelo OSI (Open System Interconnection) o Modelo de Interconexión de Sistemas Abiertos, es un estándar que cubre
	  todos los aspectos de las redes de datos.
	- Es un modelo del 80.
	- Es un modelo de la ISO. Se hizo para uniformar criterios. Modelo OSI no es un protocolo, sirve para comprender una
	  arquitectura de red.
	- El objetivo del Modelo OSI es permitir la comunicación entre sistemas distintos sin requerir cambios en la lógica del
	  hardware o del software de cada uno.
	- NO tuvo éxito el modelo, pero se convirtió en modelo de estudio.

# Modelo OSI de 7 capas.
	- Física: responsable del movimiento de los bits individuales de un nodo al siguiente. Características del medio, cómo
	  deben ser los mensajes de bits, etc.
	  Es la capa más baja del modelo OSI. Es la que se encarga de la topología de red y de las conexiones globales de la
	  computadora hacia la red, se refiere tanto al medio físico como a la forma en la que se transmite la información y de
	  las redes

	- Enlace: mueve las tramas de manera confiable a lo largo de los nodos.  Esta capa se ocupa del direccionamiento físico,
	  del acceso al medio, de la detección de errores, de la distribución ordenada de tramas y del control del flujo.
	  Es uno de los aspectos más importantes que revisar en el momento de conectar dos ordenadores, ya que está entre la capa
	  1 y 3 como parte esencial para la creación de sus protocolos básicos (MAC, IP), para regular la forma de la conexión
	  entre computadoras, determinando el paso de tramas (unidad de medida de la información en esta capa, que no es más que
	  la segmentación de los datos trasladándolos por medio de paquetes), verificando su integridad, y corrigiendo errores.

	- Red: Se encarga de identificar la ruta existente entre una o más redes. Las unidades de datos se denominan paquetes, y
	  se pueden clasificar en protocolos enrutables y protocolos de enrutamiento.

	- Transporte: Capa encargada de efectuar el transporte de los datos (que se encuentran dentro del paquete) de la máquina
	  origen a la de destino, independientemente del tipo de red física que esté utilizando.

	- Sesión: Esta capa es la que se encarga de mantener y controlar el enlace establecido entre dos computadores que están
	  transmitiendo datos de cualquier índole. Por lo tanto, el servicio provisto por esta capa es la capacidad de asegurar
	  que, dada una sesión establecida entre dos máquinas, la misma se pueda efectuar para las operaciones definidas de
	  principio a fin, reanudándolas en caso de interrupción. En muchos casos, los servicios de la capa de sesión son parcial
	  o totalmente prescindibles.

	- Presentación: El objetivo es encargarse de la representación de la información, de manera que, aunque distintos equipos
	  puedan tener diferentes representaciones internas de caracteres, los datos lleguen de manera reconocible.
	  Esta capa es la primera en trabajar más el contenido de la comunicación que el cómo se establece la misma. En ella se tratan
	  aspectos tales como la semántica y la sintaxis de los datos transmitidos, ya que distintas computadoras pueden tener diferentes
	  formas de manejarlas. Por ejemplo, un mismo sitio web puede adecuar la presentación de sus datos según se acceda desde un
	  computador convencional, una tableta, o un teléfono inteligente.

	- Aplicación: Ofrece a las aplicaciones la posibilidad de acceder a los servicios de las demás capas y define los
	  protocolos que utilizan las aplicaciones para intercambiar datos, como correo electrónico (Post Office Protocol y SMTP),
	  gestores de bases de datos y servidor de ficheros (FTP). Hay tantos protocolos como aplicaciones distintas y puesto que
	  continuamente se desarrollan nuevas aplicaciones el número de protocolos crece sin parar.

# Descripción de la Capa FISICA:
	Coordina las funciones necesarias para transmitir el flujo de datos (secuencia de bits) de un lugar a otro, a través de un
	medio físico (canal o enlace). Es decir, que se encarga de establecer y finalizar la comunicación con el medio.  La Capa
	Física define:
	- Características físicas de las interfaces entre los dispositivos y el medio de transmisión (dimensiones y forma del
	  conector, número de cables usados en la conexión, número de pines del conector, tamaño del cable, tipo de antena, etc.);
	- Tipo de medio de transmisión (cable, fibra óptica, medio inalámbrico);
	- Representación de los bits (tipo de codificación de bits en señales eléctricas u ópticas);
	- Tasa de transmisión de datos (número de bits enviados por segundo);
	- Sincronización de los bits (el emisor y el receptor deben estar sincronizados);
	- Configuración de la línea (punto a punto o multipunto);
	- Topología física (malla, estrella, anillo, bus);
	- Modo de transmisión (simplex, half-duplex, full-duplex).

# ¿Cómo es el flujo del mensaje? Modelo TCP/IP
	- El navegador genera un mensaje HTTP (capa de Aplicación). Y se lo pasa a la capa inferior.
	- La capa de Transporte toma este mensaje, lo encapsula y le añade una cabecera propia para transformarlo en un segmento.
	  Luego lo pasa a la capa inferior.
	- La capa de Red, toma este segmento, lo vuelve a encapsular y le añade una cabecera propia, transformandolo en un
	  datagrama.
	- La capa de Enlace toma nuevamente este datagrama y le añade su propia cabecera para convertirlo en una trama que será
	  transmitida por la última capa (La capa Física).
	- La capa Física es la encargada de transportar esta trama a través de los distintos enlaces hasta el host destino.

Todo este flujo se denomina *encapsulamiento*. Cuando la trama llega al destino, el host que lo recibe debe *desencapsularlo*
(realizando el proceso inverso antes descripto) donde cada capa mira el encabezado que le corresponde, y lo pasa a la capa
superior.

En la arquitectura que más se usa es la TCP/IP, se compara con el de OSI. En la página 16 explica qué dispositivos trabajan en
en cada una de las capas. Por ejemplo:
	- Switch hasta la capa de enlace
	- Routers hasta capa de internet

# Dispositivos de Red
	- Conmutador de red (switch): Conmutador (switch) es el dispositivo digital lógico de interconexión de equipos que opera
	  en la capa de enlace de datos del modelo OSI. Su función es interconectar dos o más host de manera similar a los puentes
	  de red, pasando datos de un segmento a otro de acuerdo con la dirección MAC de destino de las tramas en la red y
	  eliminando la conexión una vez finalizada ésta
	- Enrutador (router): Un rúter, enrutador,(del inglés router) o encaminador,es un dispositivo que permite interconectar
	  computadoras que funcionan en el marco de una red. Su función: se encarga de establecer la ruta que destinará a cada
	  paquete de datos dentro de una red informática. [Imagen interesante](https://es.wikipedia.org/wiki/Router).
	- Puente de red (bridge): Puente de red (en inglés: bridge) es el dispositivo de interconexión de redes de computadoras
	  que opera en la capa 2 (nivel de enlace de datos) del modelo OSI.
	  Interconecta segmentos de red (o divide una red en segmentos) haciendo la transferencia de datos de una red hacia otra
	  con base en la dirección física de destino de cada paquete.
	  En definitiva, un bridge conecta segmentos de red formando una sola subred (permite conexión entre equipos sin necesidad
	  de routers). Funciona a través de una tabla de direcciones MAC detectadas en cada segmento al que está conectado. Cuando
	  detecta que un nodo de uno de los segmentos está intentando transmitir datos a un nodo del otro, el bridge copia la
	  trama para el otro segmento de red, teniendo la capacidad de desechar la trama (filtrado) en caso de no tener dicho
	  segmento de red como destino. Para conocer por dónde enviar cada trama que le llega (encaminamiento) incluye un
	  mecanismo de aprendizaje automático (auto aprendizaje) por lo que no necesitan configuración manual.
	- Puente de red y enrutador (brouter).
	- Punto de acceso inalámbrico (Wireless Access Point, WAP): Un punto de acceso inalámbrico (en inglés: wireless access
	  point, conocido por las siglas WAP o AP), en una red de computadoras, es un dispositivo de red que interconecta equipos
	  de comunicación inalámbricos, para formar una red inalámbrica que interconecta dispositivos móviles o tarjetas de red
	  inalámbricas.
	  Son dispositivos que son configurados en redes de tipo inalámbricas que son intermediarios entre una computadora y una
	  red (Internet o local). Facilitan conectar varias máquinas cliente sin la necesidad de un cable (mayor portabilidad del
	  equipo) y que estas posean una conexión sin limitarle tanto su ancho de banda

[17]: Se ven los distintos protocolos que se utilizan en internet.

Profundizar la presentación nº 2 con otras lecturas de redes I y II.

# 3 Videos en el campus que explican todo lo anterior:
	https://campus.unaj.edu.ar/mod/book/view.php?id=49849

