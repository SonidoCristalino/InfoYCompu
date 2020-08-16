# Filmina:
	Clase 6 - Multiplexación y Ensanchado

# Clase nº 8: 16/06/2020

Hasta esta clase entra el parcial, el examen que tengamos.

El ancho de banda no es libre, estamos limitados, cuanto más utilicemos, se convierte en menos eficiente, costoso.

La idea es utilizarlos de la manera más eficiente. Algunas veces conviene utilizar de forma eficiente el ancho de banda.
Se puede generar la multiplexación con el objetivo de la eficiencia

El canal por el que se transmite las señalaes sea un canal de un gran ancho de banda,susperiro al todas de las ancha de banda
sumadas de las señales que se transmiten, suma total de todos los anchos de banda.

Página nº 3:
	* En la multiplexación el objetivo es la eficiencia (se combinan varios canales en uno).
	* En el ensanchado los objetivos son la privacidad y la eliminación de las interferencias (se amplia el ancho de banda de
	  un canal para insertar redundancia)


# Multiplexación:
Se tienen n lineas por las que entra una señala con una determinada frecuencia y ala salida se tiene un único canal, que es mayor
que cada una de las entradas individualmente. Sobre el final hay un multiplexador para que sea de muchas a una y sobre el final se
tiene un de-multiplexador, entra una y salen muchas.

Que cada una de las técnicas sean analógicas o digialtes no significa que los datos que entran deban ser digiales o analógicias,
ya que puede emplear una técnica para convertirlos [pagina 5].

La multiplexación es el conjunto de técnicas que permiten la transmisión simultánea de múltiples señales (combinación de dos o más
canales de información) a través de un solo medio de transmisión, usando un dispositivo llamado multiplexor (MUX). El proceso
inverso utiliza un dispositivo llamado demultiplexor (DEMUX).  Mediante esta técnica n líneas comparten el ancho de banda de un
medio de transmisión.

# Multiplexación FDM (Analógica):
3 lineas de entrada y se envía un único canal, que el demulti puede entender que le entran muchos y las separa en cada una de las
salidas.

Frecuencia portadora: frecuencia mucho más grande que la señala que se quiere transmitir.
En la página 7 se ve que son 3 señales, se suman y se queda una señal compuesta y es la que realmente viaja.

Del otro lado se tienen filtros, para recuperar la señal original (filtro pasabanda), con el demulador se recupera la señal
original.

Al multiplcar por la frecuencia portadora, se corre la frecuencia (como en la página 10, que tenemos 3 señales una de 20-24, otra
24-28 y otra 28-32) Se transmite toda esa.
El filtro pasa banda lo que hace es eliminar las frecuencia de 20 a 24, e elimina todas las demás y eso hce para cada uno de los
canales, pero a distintas frecuencias.

### El ejemplo nº 2

### El ejemplo nº 3:
	FDM es un método analógico, ¿Cómo se da cuenta si es analógica o digital? si se trabaja con Kh, mh, frecuencias de señal
	analógica, en cambio sis e labura con bits por segunda o mb por segundo, es digital. ¡Es ver las unidades que nos dice el
	enunciado!.

	Recordar que es FDM, por lo tanto Hay que hacerle una conversión de la frecuencia,porque se está trabajando con digital.
	Como el canal es de 1Mhz, cada uno de los 4 señales entrantes, va a tener 250khz, ya que 250*4 = 1000.

	Se necesita convertir de digital a analógico, por eso es la QAM,cada 4bits modula en 1 hz, porque 1Mbps / 250Mhz = 4.

Otra utilización es en la Red Telefónica [página 13] ¡lo importante es que se quería EFICIENCIA!

# Multiplexación WDM:
Longitud de onda es la distancia real que recorre una señal a través de un medio de transmisión.

Se utilizan prismas que dependen de la incidencia del haz de luz y de la frecuencia, pero básicamente lo que hace es descomponer
la frecuencia y retornar con la original.

# Multiplexación TDM:
La división se hace por tiempo, se ocupa el canal por determinado tiempo

[pagina 20] Ver que los frames están compuestos por los los bits vistos en vertical, no en horizontal.

Cuando hay ranuras vacías, se pierde eficiencia. Esto se mejora con el método asincrónico (que está sólo en el libro).

Cada uno de los canales tiene la misma velocidad, 1Mbps. ¿Qué pasa cuando no tiene la misma velocidad? Hay que aplicar distintas
estrategias [Página 22]
	- multiplexación de nivel
	- bl bla de pulsos
	- y no sé qué

Multiplexación de nivel: las dos lineas menores se multiplexan juntas, y forman una con la misma velocidad que las otras, se unen
a otras en el multiplexor.

Multiplexación con ranuras múltiples:
	La entrada es mayor que la de las líneas divisorias. Lo que se hace al mayor, dividirla.

Inserción de pulsos:
	Una de las entradas son más lentas, se le agregan pulsos para aumentar su velocidad

# Espectro de ensanchado:
[Me fui al baño] Página 32.

FM tiene como objetivo tener largo alcance y transportar VOZ, no era la idea transportar música ni otras frecuencias.

