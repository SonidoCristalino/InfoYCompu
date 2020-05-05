# Clase 4 : 05/05

	- Martes (12/05) que viene hay una evaluación meramente teórica.
	- Hay ejercicios colgados, luego de cada material de estudio de la parte nº 3
	- Diez preguntas de tipo multiplechoice.
	- Exámen a las 17hs y se tiene media hora para resolverlo.

## Repaso:
Se verán las capas físicas del modelo OSI. La que se encarga del movimiento de los bits. Diferencia entre dato y señal.
Señales que tienen que ver con tensiones, corrientes, periódicas no periódicas, etc.

	- Señales analógicas pueden tomar infinitas valores en la amplitud
	- Señales digitales pueden tomar valores discretos en la amplitud
Otra diferencia es la suavidad con la que cambia, una analógica es más suave, presenta una variación continua en el tiempo; los
cambios en la digital son abruptos. Las funciones analógicas es COMO la función que puede ser derivada y la digital es ya derivada.

Nos interesa una función seno o coseno (lo mismo pero están desplazadas 90º entre si). Estamos hablando de la misma función.

De una función seno y coseno, con la descomposición se puede reconocerse varias cosas [10].
Señal es una suma de senos y cosenos, señal compuesta que se puede descomponer en funciones más simples de funciones de senos y
cosenos. Eso es lo que nos dice el análisis de Fourier

Son difíciles de graficar estas señales compuestas, por esto es que se simplifica a partir del análisis del dominio de la
frecuencia (que es el análisis que hace Fourier). Se transforma del dominio del tiempo, en función de la frecuencia [pagina 18].

Observación importante: [pagina 17]
	Lo que sucede en tiempos muy cortos se traslada en altas frecuencias
	Lo que sucede en tiempos muy largos se traslada a bajas frecuencias.

	Una señal continua en el tiempo tiene frecuencia cero.
	Si la señal cambia instantáneamente, su frecuencia es infinita (que cambie instantáneamente en el tiempo significa que este
	cambio en este punto, cuando se pasa al espectro de frecuencias, son infinitas).

Ancho de banda de una señal se define como la frecuencia máxima menos la frecuencia mínima. Una vez que se hace la conversión al
dominio de la frecuencia

[pagina 29]:
	Una es una función discreta y la otra es una función continua.
	Banda base[30] es cuando incluyen la componente cero.

## Clase de hoy

Señales digitales: tienen pros y contra [página nº 3]

	- Tasa de bits : número de bits que se transmiten por segundo (bps), se escribe con minúscula.

Ver que no tiene nada que ver con el baudio (número de cambio de eventos que tiene la señal) como dice en la página nº 3.

Para ver un ejemplo ver la página nº 5 ver que se transmiten 16 bps porque se transmiten 8 pero con otra amplitud (8 alternativas,
8x8 = 16).

Ancho de banda
¿Qué pasa cuando se pasa al dom de frecuencia?

Todo ancho de banda de una señal es infinito.

[Pagina 7]: dos formas de transmitir un pulso por un canal entre determinadas terminales.
Las frecuencias más altas no pasan por el canal porque no tiene un ancho de banda infinito, siempre hay recortes. Lo que hay es
que cuando llega del otro lado se puede reconstruir, se pueden reconstruir esos deteriores.  Esto es en banda base con un ancho de
banda amplio

¿Qué pasa si se tiene un bando de ancha estrecho? Se recorta mucho más la señal digital, por lo que del otro lado, se complica
reconstruirla [página 10]
Ver que las aproximaciones en 000 o 111 son exactas. En las demás, no es exactamente la misma. Se aproxima una señal digital a una
analógica. Se analiza solo un seno, una sola frecuencia, lo que nos dice Fourier lo que hay que hacer es tomar más de uno, así la
aproximación es mucho mejor.

En la página 11 se muestra una mejor aproximación obteniendo dos senos de las señales. N/2 es el armónico fundamental o primer
armónico, cuando más armónicos tomemos, más aproximaciones vamos a tener.
En la página 11 lo que importa son las frecuencias pintadas en celeste, aparecen los impares, se puede ver N/2, 3N/2, 5N/2, esto
es matemático, dependiendo si la función es coseno ( obteniéndose armónicos pares) y seno(obteniéndose armónicos impares).
Se tiene una mejor señal a costa de aumentar el ancho de banda. El ancho de banda es proporcional a la cantidad de bits, si
queremos enviar mas bits se tendrá que agrandar el ancho de banda.
Página 12 se visualiza una tabla sobre el ancho de banda que se tienen que tener para enviar el primer armónico, el 1, 3 el
triple, y si se quiere 1,4,5 entonces es cinco veces más grande.
Está en el criterio de cada uno, hasta qué punto quiere reconstruir la señal a costa del ancho de banda.

Transmisión de banda ancha implica que a la señal haya que cambiarla a una analógica por la transmisión. Se utiliza en un pasa
banda (sin frecuencia cero).
En la página 14 se muestra cómo pasar en banda ancha (se reconstruye la misma señal que se emitió).

## Segunda parte
Causas de deterioro:
	- Atenuación : pérdida de potencia que se produce en el canal en función del a distancia entre dos puntos a analizar. La
	  fórmula está en [16]. Siempre hay una pérdida, hay una disminución de la potencia eléctrica, por eso es que se utilizan
	  amplificadores para recuperar la señal original. En la página 17 se puede ver cómo es que se utiliza el amplificador
	  donde pasa la señal del punto 1 al 4.
	- Distorsión: Velocidad de propagación de la señal y esta velocidad puede llegar a variar con la frecuencia y con los
	  armónicos de ella. No todas los armónicos viajan a la misma velocidad. En la página 18 se muestra cómo es que se
	  configuran las distintas frecuencias de los armónicos 1, 3, 5. Ver dónde comienza la frecuencia que se envían y dónde
	  empiezan las que se llegan. Es cuando la señal no está en fase.
	- Ruido: conjunto de señales extrañas a la transmisión que se introducen en el medio de transmisión. Siempre habrá ruido,
	  no se puede medir el ruido, lo que si se puede medir es la relación señal/ruido. Que tiene que ver con la relación o
	  cociente sobre la potencia media del ruido. Cuanto más grande la señal, mejor, en la amplitud. Se puede ver por qué en
	  [20].

Las tres consideraciones importante se encuentran en la página 21.

	- Mayor ancho de banda mayor velocidad

Modelo de Nyquist:
-----------------
Aumento del número de niveles (M), aumenta la velocidad (R), y esto no es así. Lo que sirve Nyquist es para ver

Modelo de Shannon:
-----------------
Sirve para un canal con ruido. Nos da la capacidad que tiene un canal para transmitir. El canal tiene un límite, y la fórmula nos
describe la características del canal

Sobre la práctica:
-----------------
	- En la práctica se tienen dos ejercicios, con estos últimos de la filmina. Son ejercicios amplios, en el setndio que no
	  se resuelven de una sola forma. Los ejercicios están sacados del capítulo 3.  Buscarlo los ejemplos y complementarlos
	  con la lectura. En el libro pide bits por segundos y en la guía pide bits por minutos.
	  Capítulo nº 3 son las clases nº 2 y nº 3.

