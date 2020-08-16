# Filmina:
---------
	Clase 4 - Transmisión Digital (parte A)

# Clase nº 6: 19/05

Se comienza con la *Unidad 4*:

## Información:
--------------
La información es un conjunto organizado de datos procesados, que constituyen un mensaje que cambia el estado de conocimiento del
sujeto o sistema que recibe dicho mensaje.

Transmisión de los datos, de la información, que uno como emisor quiere que reciba el receptor. Lo que interesa es que la
información llegue del emisor al receptor.
La información original puede que se tenga en digital o analógico. Lo que se va a ver en esta unidad 4 y 5 las diferentes
técnicas de la transmisión.

División de unidades:
	Unidad 4 : transmisión digital
	Unidad 5 : transmisión analógica.

Hay que ver cómo se transmiten los datos, 4 tipos de transmisiones:
	Dato digital - Señal Digital
	Dato analógico - Digital
	Dato digital - Señal Analógica.
	Dato analógico - Digital analógica

Por lo tanto, el ancho de banda efectivo de una señal digital es finito

# Codificación de Línea: Dato digital -> Señal Digital
------------------------------------------------------
La codificación de linea es esto, convertir de una a otra. Para la computadora son secuencias de bits, que se quieren enviar,
entonces lo que se tiene que hacer es enviar a través de una señal digital. Se tienen datos digitales, se codifican, se transmiten
por el canal, se decodifica y se reciben.
Hay muchos esquemas o métodos, de codificación de línea, pero bueno, se toca sólo uno.

	- Elementos de datos: Es la entidad más pequeña que se puede representar en un elemento de dato

	- Elementos de señal: Es la entidad más pequeña que puede representar en un elemnto de señal. Estos son los portadores,
	  los que se encargan de llevar los portadores.

## Analogía con el transporte:
	Número de auto por persona, una persona por auto = 1 = r.
	Dependiendo de la situación, puede variar r. Esto se puede ver en la filmina nº 8.
		- Ejemplo c) Se puede pensar como, por cada auto van dos personas.
		- Ejemplo b) Por cada bit se necesitan dos elementos de señal r = 1/2

## Tasa en Baudios:
	- Bits por segundo: número de elementos de datos enviados en 1 segundo. Unidad de Bps.
	- Baudios: Tasa de señales o Tasa en baudios (Signal Rate o Baud Rate): número de elementos de señal enviados en 1
	  segundo. La unidad es el baudio. Un baudio puede contener varios bits

	c = factor de caso: lo que se hace es tomar el peor y el mejor caso y tomar el valor medio (eso sería el factor de caso).

# Ancho de Banda:
----------------
Una señal digital en general es no periódica, su ancho de banda es continuo con rango infinito. Ancho de banda es proporcional a
la tasa de señales, tasa de baudios.

Prestarle atención a los esquemas de codificación que existen para transmitir conjunto de bits.

# Esquemas de Codificación de Línea:
-----------------------------------

## Esquema Unipolar: NRZ
	No es utilizado hoy en día. En comparación con el Polar, es muy costoso.

## Esquema polar: NRZ-L y NRZ-I
	Cambia en el medio del bits. Es útil para sincronizar los relojes. R ya no vale 1, por cada bit, dos elementos de señal,
	por lo que r = 1/2, baudios va a valer S = N. Tiene un gran ancho de banda, será muy grande dado que tiene que la señal
	que se formó.

	- NRZ-L: A cada cambio de tensión en la señal, representa un cambio de bit. Por ejemplo: Si aumenta a 5v entonces es 1, si
	  disminuye a -5v entonces es 0.
	- NRZ-I: El cambio en la tensión es la que da la señal que hubo un cambio de bits. En la página nº 13, se puede ver bien.

	Estos métodos tienen un problema con la sincronización de relojes.

## Esquema Polar: RZ
	- RZ (Return to Zero): Se utilizan tres niveles de amplitud: positivo, negativo y cero. La primera mitad del bit, es la
	  que señala según cambie de forma positiva (1) o negativa (0); la segunda mitad del bit, vuelve al nivel cero de tensión.

	La problemática de RZ:
		- Soluciona el problema de la sincronización de los esquemas NRZ. Las transiciones se pueden usar para
		  sincronización.
		- Principal desventaja: ¡Ocupa mayor ancho de banda! (Dado que requiere de dos cambios de señal para codificar un
		  bit).
		- Otro problema es la complejidad: RZ utiliza tres niveles de tensión, que es más complejo de crear y discernir

## Polar Bifásica:

Manchester:
	- Combina el NRZ-L con el Polar Rz. Lo que queda en lugar de tener como en el polar, 3 niveles, se tienen 2 niveles.
	  Entonces por ejemplo vale, 0 si se tiene el nivel alto y en vez de volver a cero, no vuelve a cero, sino vuelve al otro
	  nivel, hay un cambio. La transición en el medio del bit se utiliza para la sincronización.

Polar Bifásica Manchester diferencial.
	- Combina RZ y NRZ-I.
	- A la mitad del bits siempre cambia, y sigue lo pautado sobre el esquema (el Combina el NRZ invertido y el Polar Rz.

Para una secuencia de bits se pueden armar 6 señales digitales diferentes, cada una haciéndole Fourier, va a quedar un ancho de
banda diferente, r va a ser distinto, N va a ser continua, etc.

## Esquema Bipolar: AMI Y Pseudoternaria

AMI:
	- Bipolar, se mediante 3 niveles. Cuando el bit es cero, no recibe tension. Para señalar al otro elemento (1) puede ir
	  entre positivo o negativo.
	  	* El elemento 0 siempre es de 0 volts. El que alterna es el valor 1, que pasa de ser negativo a positivo.
		* El elemento 1 siempre es de 0 volts. Pero se alterna el 0 entre positivo y negativo

## Esquemas multi-nivel:
	* No se ven en profundidad, sólo se ve 1.

Resumen de esquemas de Codificación de Línea
