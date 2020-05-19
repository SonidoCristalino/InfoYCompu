# Clase nº 6: 19/05

Se comienza con la Unidad 4.

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

# Codificación de Línea: Dato digital -> Señal Digital
La codificación de linea es esto, convertir de una a otra. Para la computadora son secuencias de bits, que se quieren enviar,
entonces lo que se tiene que hacer es enviar a través de una señal digital. Se tienen datos digitales, se codifican, se transmiten
por el canal, se decodifica y se reciben.
Hay muchos esquemas o métodos, de codificación de línea, pero bueno, se toca sólo uno.

	- Elementos de datos
	Es la entidad más pequeña que se puede representar en un elemento de dato

	- Elementos de señal
	Es la entidad más pequeña que puede representar en un elemnto de señal. Estos son los portadores, los que se encargan de
	llevar los portadores.

Analogía con el transporte:
	Número de auto por persona, una persona por auto = 1 = r.
	Dependiendo de la situación, puede variar r. Esto se puede ver en la filmina nº 8.
	- Ejemplo c) Se puede pensar como, por cada auto van dos personas.
	- Ejemplo b) Por cada bit se necesitan dos elementos de señal r = 1/2

	- Bits por segundo: número de elementos de datos enviados en 1 segundo. Unidad de Bps.
	- Baudios:

	c = factor de caso, lo que se hace es tomar el peor y el mejor caso y tomar el valor medio (eso sería el factor de caso).

Ancho de Banda:
Una señal digital en general es no periódica, su ancho de banda es continuo con rango infinito.
Ancho de banda es proporcional a la tasa de señales, tasa de baudios.

Prestarle atención a los esquemas de codificación que existen para transmitir conjunto de bits.

## Esquema polar:
Cambia en el medio del bits. Es útil para sincronizar los relojes. R ya no vale 1, por cada bit, dos elementos de señal, por lo
que r = 1/2, baudios va a valer S = N. Tiene un gran ancho de banda, será muy grande dado que tiene que la señal que se formó.

## Polar Bifásica Manchester:
Combina el NRZL con el Polar Rz. Lo que queda aen lugar de tener como en el polar, 3 niveles, se tienen 2 niveles. Entonces por
ejemplo vale, 0 si se tiene el nivel alto y en vez de volver a cero, no vuelve a cero, sino vuelve al otro nivel, hay un cambio.
Polar Bifásica Manchester diferencial. A la mitad del bits siempre cambia, y sigue lo pautado sobre el esquema (el

Combina el NRZ invertido y el Polar Rz.

Para una secuencia de bits se pueden armar 6 señales digitales diferentes, cada una haciéndole Fourier, va a quedar un ancho de
banda diferente, r va a ser distinto, N va a ser continua, etc.

Bipolar, se mediante 3 niveles. Cuando el bit es cero, no recibe tension.

Esquemas multi-nivel no se ven en profundidad, sólo se ve 1.
