# Resumen para la presentación:

## Tecnología 0G:
	Fueron las que posibilitaron el surgimiento de las comunicaciones móviles que nacieron de las investigaciones científicas
	realizadas en la Segunda Guerra Mundial en campo militar. Si bien era una tecnología enbrionaria, incipiente, permitió el
	surgmiento de nuevas formas de comunicaciones hasta hoy en día. Las comunicaciones eran precarias y sólo estaban
	destinados a cierto sector de la sociedad, que podía costear el precio de las instalaciones.
	Tenían sus propios números y funcionaban como las radios de una estación de policía.
	Ericsson desarrolla el primer teléfono de este tipo en 1956.

	Destacar que es completamente analógica la tecnología.

	Ejemplo en Arabia Saudita, en los lugares donde se levantaban las refinerías (cerca del desierto y lejos de toda ciudad)
	ponían teléfonos de este tipo para poder comunicarse.

## Tecnología 1G:
	Se permitió el acceso masivo de los dispositivos que antaño eran para unos pocos. Esta masificación trajo consigo también
	una propagación de las antenas que permitían el acceso a las frecuencias necesarias para las comunicaciones.
	Los números dejan de ser privados, y pasan a ser parte de la red comercial de las empresas telefónicas.

## Tecnología 2G:
	Comienza a ser implementada a partir del año 1991.
	Se produce una saturación de la red de 1G en que se dividian las frecuencias, por lo que se producen intereferencias y
	solapamientos. También había problemas con los estándares utilizados, por lo que hacía imposible el uso de teléfono móvil,
	lo que respaldó el surgimiento de una posible tecnología 2G, para obtener una mejor compatibilidad entre los equipos de
	distintas regiones.

	Esta tecnología es un híbrido en partes distintas,entre la era analógica y la digital, aunque de forma digital sólo
	obtenía datos como hora y fecha.

	# Filmina:
		Clase 6 : Multiplexación y Ensanchado

		- Utiliza TDMA - Acceso Múltiple por División de Tiempo
		- Utiliza CDMA - Acceso Múltiple por División de Código
		- Utiliza CODEC (codificación y decodificación) para codificar, multiplexar y transferir datos digitales.
		- Para TDMA y CDMA utilizan un ancho de banda diferente por canal.

	Como la transmisión de datos se hace mediante la División de Tiempo TDMA, los dispositivos no están transmitiendo y
	recibiendo constantemente datos, por lo que pueden dedicar cierto intervalo de tiempo a sintonizar las frecuencias de las
	celdas vecinas, por lo que este mecanismo le ahorra trabajo a la estación base (que deja de hacerlo ella) y pasa a
	realizarlo el teléfono, por lo que ese translado de procesamiento de la red a los dispositivos, permite descomprimir la
	labor de la red.

	Se consigue una mejora en el control de potencia debido a esta mejora, al no tener que estar constantemente transmitiendo
	el dispositivo, hay un eventual ahorro de energía (a diferencia del 1G que consumían más batería) y también se mejoraba la
	transmisión de datos, ya que (a diferencia de 1G) había una disminución en la cantidad de dispositivos transmitiendo todo
	el tiempo, por lo que con 2G había menos interferencia en las comunicaciones.

	Pero en contraposición, se requiere que las señales *DIGITALES* sean mucho más fuertes, para que los teléfonos las puedan
	captar, por lo que si no hay cobertura de red en un área específica, las señales digitales se vuelven débiles. Pero estas
	señales tenían la ventaja de funcionar mucho mejor en ambientes con elevada interferencia, permitiendo una capacidad
	superior a los analógicos.

		- TDM: Multiplexación por Tiempo es sólo para la parte digital.
		- La red utiliza GSM: por lo que se utiliza la multiplexación era sólo en frecuencia (FDMA) por ser frecuencias
		  analógicas. FDM: el acceso al medio se realiza dividiendo el espectro disponible en canales, que corresponden a
		  distintos rangos de frecuencia, asignando estos canales a los distintos usuarios y comunicaciones a realizar,
		  sin interferirse entre sí. Recordar que en los extremos de la conexión debe haber un multiplexor y un
		  demultiplexor.

	Con 2.5G comienza a haber una implementación híbrida entre la conmutación de paquetes y la de circuitos.

	Se utilizaba el estrecho margen de datos para consultar mails y navegación web de forma muy precarias. Además, tenían un
	elevado costo ya que la "navegación por internet" se cobraba por megabyte mientras que los datos transferidos mediante
	conmutación de circuitos se cobraba por minuto empleado.

	EDGE es una versión mejorada de GSM que permitía una tranmisión más clara y rápida de datos. Permite aún más flexibilidad
	entre la conmutación de circuitos y la de paquetes. Esta tecnología vino de forma nativa con los BlackBerry.

La *multiplexación es el conjunto de técnicas* que permiten la transmisión simultánea de múltiples señales (combinación de
dos o más canales de información) a través de un solo medio de transmisión, usando un dispositivo llamado multiplexor
(MUX). El proceso inverso utiliza un dispositivo llamado demultiplexor (DEMUX)

*IMPORTANTE* : Se aplica el nombre *multiplexado* para los casos en que un solo dispositivo determina el reparto del canal entre
distintas comunicaciones, como por ejemplo un concentrador situado al extremo de un cable de fibra óptica; para los terminales de
los usuarios finales, el multiplexado es transparente. Se emplea en cambio el término *control de acceso al medio* cuando son los
terminales de los usuarios, en comunicación con un dispositivo que hace de nodo de red, los que deben usar un cierto esquema de
comunicación para evitar interferencias entre ellos, como por ejemplo un grupo de teléfonos móviles en comunicación con una antena
del operador.

*Control de Acceso al medio* : En informática y telecomunicaciones, el control de acceso al medio (conocido por las siglas MAC,
del inglés: Media Access Control) es el conjunto de mecanismos y protocolos de comunicaciones a través de los cuales varios
"interlocutores" (dispositivos en una red, como computadoras, teléfonos móviles, etcétera) se ponen de acuerdo para compartir un
medio de transmisión común (por lo general, un cable eléctrico o fibra óptica, o en comunicaciones inalámbricas el rango de
frecuencias asignado a su sistema).

# Multiplexación por División de Frecuencia Ortogonal(OFDM):

La Multiplexación por División de Frecuencia Ortognal es un método de modulación donde el espectro asociado a cada dato es una
pequeña porción del ancho de banda total, el cual se divide en n subcanales, y en donde cada canal se modula con un símbolo y se
multiplexa en frecuencia. Para evitar el uso de varios filtros y moduladores tanto en el transmisor como en el receptor, lo que se
emplea es lo que se denomina Transformada Rápida de Fourier.

Para la obtención de los símbolos de cada canal (y asegurarse que cada canal no interfiera entre sí), se hace uso de las
frecuencias ortogonales. ¿Qué significa ''ortogonal''? Basándonos en Matemáticas, podemos decir que son aquellos ángulos que
forman 90 grados con su referencia y cuyo Producto Escalar será cero. Para obtener cada símbolo (o código) se emplea el principio
de la Matriz de Hadamard.

Con la obtención de cada símbolo, se asegura que cada una de las frecuencias en las que se transmitirán los bits de información
durante determinado tiempo asociado a un símbolo, serán mutuamente excluyentes, por lo en el lado del receptor, se podrá
reconverir la información de una forma inequívoca, sin yuxtaposición entre señales.

