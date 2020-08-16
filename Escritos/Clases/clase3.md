# Filmina:
----------
	* Clase 3 - Datos y Señales (Parte A)

# Clase 3: 28/03/2020

	La clase que viene van a subir al campus una auto evaluación que junta las 3 clases. Para ir sabiendo si tenemos aprobada
	esta parte.

# Datos y señales:
------------------

	- Clase nº 1 Introducción
	- Clase nº 2 Modelos de redes (osi y TCP): la capa inferior es la capa física y la que nos interesa. La capa física la
	  responsable de movimientos de bits de un nodo al siguiente. Este movimiento se puede hacer de diferentes maneras y se
	  puede optar diferentes características para esto: optar por un cable u otro, la sincronización entre terminales, etc.

Dato que es una representación lógica, y es cuantitativo (edad de alguien, algún numero en general) y cualitativo (que no
representa un número). Un dato único no constituye como información, lo que se hace hicapie es en el procesamiento que es lo que
se hace la información.

La señal es el medio que nos va a dar aviso de la información y en son señales electromagnéticas. Analogía: datos son las personas
mientras que las señales son los vehículos: autos, micros, etc. Datos para llegar a un lugar necesitan un medio de transporte,
igual que los datos, y por lo tanto necesitan de señales electromagnéticas


# Señales
---------
Es un medio que informa o avisa de algo, este aviso da a conocer información. Representación eléctrica o electromagnética de
los datos

Las más común son las señales eléctricas, las mismas pueden ser voltajes o tensiones que se miden en Volt, corriente en
Amper o componente de campo electromagnético, y estas señales provienen de transductor, necesitamos que por ejemplo una
temperatura que se convierta en señal eléctrica, para ser procesada por un dispositivo.

Las señales se pueden clasificar de determinadas maneras (en la filmina, 1, 3, y 5).
	- Señales analógicas: es una señala que puede tomar infinitos valores en amplitud, son continuos y los infinitos valores
	  en tiempo también son posibles. Se puede hacer una comparación con el reloj analógico, cuya información al respecto de
	  la hora nos la brinda de forma continua, ya que el movimiento de las agujas del reloj son continuas.

	- Señal digital: es una señal sólo en amplitud puede tomar valores discretos, no toma infinitos valores. Presenta una
	  variación discontinua en amplitud y tiempo. Esto es como el reloj analógico, el cual nos informa de la hora
	  repentinamente, cambiando de minuto a minuto de forma repentina.

También se pueden configurar como:
	- Determinística: Para cada valor de t tenes un valor de la función (señales deterministicas, porque están determinadas
	  por una función)
	- Aleatorias: tienen que ver con el azar, con la probabilidad (cada valor posible que una señal puede tomar tiene asociado
	  a una probabilidad mayor o menor) [no consideramos estas señales]. Procesos estocásticos de señales.

## Clasificación de señales:
----------------------------
	- Periódicas: es aquella que su ciclo principal se va repitiendo cada cierto intervalo de tiempo. Muestran una
	  periodicidad, están las funciones den la filmina. Período medido en segundos Señal periódica: Una señal es periódica si
	  completa un patrón dentro de un marco de tiempo medible, denominado periodo, y repite ese patrón en periodos idénticos
	  subsecuentes. Cuando se completa un patrón completo, se dice que se ha completado un ciclo.

	- No periódicas: Las que NO presentan periodicidad en su ciclo principal.

En las comunicaciones de datos comunmente se utilizan señales *analógicas periódicas y señales digitales no periódicas*

## Señales Analógicas:
----------------------
	Las señales analógicas pueden ser:
		- Simples: es la señal que no puede ser descompuesta en otras (como una onda sinusoidal)
		- Compuestas: Es la señal que está compuesta por otras señales.

	Pueden tener infinitos valores en amplitud como en tiempo. Y pueden ser periódicas y otras no periodicas.  Son aquellas
	señales eléctricas donde en vertical aparece la tensión eléctrica.  La función analógicas más simple es la función seno(x)
	por lo que vamos a tener que recordar las funciones de seno y coseno.  Seno: Está acotado en su amplitud y es periódica y
	se repite cada 2pi^segundos. Se ven las características en las filminas.

	Lo importante es *el período y la señal*. Ese período es la inversa de la frecuencia. El caso en el que alguna vez habrán
	visto en Matemática I
	Relación entre período y frecuencia = es una relación inversa, cuando mayor es la frecuencia menor será el período, se
	mide el período en segundos.

## Elementos de Datos y de Señal:
Para la codificación de línea encontramos varias características:
		- Elementos de Datos: entidad más pequeña que puede representar un elemento de información: bit.
		- Elementos de Señal: unidad más corta (en cuanto a tiempo) de una señal digital. Transporta elementos de datos.


## Señal sinusoidal:
-------------------
Es la forma fundamental de la señal analógica periódica. Tiene cambios suaves, y continuo. Una señal de este tipo puede ser
representada por tres parámetros: amplitud de pico, la frecuencia y la fase.
	- Amplitud de pico: es el valor absoluto para la intensidad más alta, que es proporcional a la energía que conlleva. La
	  amplitud normalmente se mide en Volts.
	- Frecuencia y período. El período se refiere a la cantidad de tiempo, medido en segundos, que la señal necesita para
	  completar 1 ciclo. Frecuencia se refiere al número de períodos transcurridos dentro de un segundo. Cabe resaltar que el
	  período y la frecuencia están inversamente relacionados: f = 1/t y T = 1/f. La frecuencia es medida en Hertz(Hz) lo cual
	  es un ciclo por segundo.

[Página 98] Donde indica cómo calcular las señales según su frecuencia.

# Señales con frecuencia cero y frecuencia infinita:
---------------------------------------------------
	- Las señales que no cambian para nada, es decir, que mantienen constante su nivel de voltaje, se dice que su frecuencia
	  es CERO, ya que nunca completa ningún período.
	- Las señales que cambian instantáneamente se denomina que su frecuencia es infinito. Esto es así ya que cuando la señal
	  cambia instantaneamente su período es cero y como la relación con la frecuencia es inversa con respecto al
	  tiempo,entonces se tiene f = 1/0 = infinito.

# Fase:
------
El término fase, describe la posición de la forma de onda relativo a su tiempo cero, al eje de coordenadas. Esta indica el estatus
el primer ciclo.
Las fases se miden en grados o en radianes. Un cambio de fase de 360º corresponde a un cambio completo de período; un cambio de
fase de 180º corresponde a la mitad de un período completo; un cambio de fase de 90º se corresponde a un cuarto de un período
completo.

[Página 99] : Algunos problemas de des-fase de onda.

# Longitud de onda:
------------------
La longitud de onda dobla el período o la frecuencia de una onda sinusoidal simple a la velocidad de propagación del medio.

Mientras que la frecuencia de una señal es independiente del medio, la longitud de onda depende tanto de la frecuencia como del
medio. La longitud de onda es la distancia que puede viajar una simple señal en un período determinado.

[Pagina 100] se encuentra la relación de la Longitud de onda con la frecuencia, la velocidad de propagación y el período.

# Dominio del tiempo:
--------------------
	[101 del libro] : Se visualiza la comparacióne entre un gráfico en función de la amplitud (medido en Volts) sobre el
	tiempo, y uno medido en Amplitud también, pero sobre la frecuencia.
	[página 11]
	12 períodos en 1 segundo = 12herz = 1/12 ese ese el concepto de frecuencia, cuántos períodos caben en un segundo, cuántos
	períodos entran en un segundo.
	6 ciclos en 1 segundo = 6herts. Se puede ver la relación inversa.
	A menor período, mayor frecuencia (se ve en la filmina)
	Si se tiene una frecuencia de 1 hetz, entraría un ciclo en una segundo.

	[12]
	Diferencia entre dos señales se pueden hacer diferentes amplitudes. El período es el mismo, entran la misma cantidad de
	ciclos, pero con diferente amplitud.
	La amplitud es la longitud desde el cero hasta el pico, cuanto mayo es la amplitud, más alta la longitud desde la recta
	hasta el vértice.

	[13]
	Señales diferentes: empiezan de forma distinta, uno en 1, otro en 0 y el otro 0 pero negativo.
	El área en rojo es lo que indica la función que está al costado 1/4 y 1/2. Función coseno(x) que empieza con uno, seno(x)
	empieza en cero.

	[15]
	Longitud de onda, que tiene que ver con los medios por medio los cuales se transmite la señal: aérea, cable, alambre.
	No se va a transmitir con la misma velocidad en distintos medios, hay una relación. Una relación entre la frecuencia y la
	longitud.
	Si el medio fuese el vacío, entonces v toma la velocidad de 300 cm/s, si fuese el agua sería 222,4cm/s, son diferentes los
	materiales, por lo que la frecuencia va a cambiar.
	Lo interesante es la longitud de onda, que es la distancia que recorre en determinado tiempo.

	Todo esto en el análisis del dominio del tiempo.

# Dominio de la frecuencia:
--------------------------

	- En lugar de que el eje x se mide en frecuencia, en vez de segundos (tiempo) se mide en hertz. Esto está relacionado con
	  el análisis de Fourier (en la transformada de Fourier). Depende si es periódica o no periódica.

	- Los cambios cortos se translada en alta frecuencia.
	- Las cosas que sucedan en tiempo pequeños, se van a ver reflejados en el dominio de la frecuencia a alta frecuencia,
	  tiene que ver con la proporcionalidad entre tiempo y frecuencia.

	- Lo que sucede en tiempos muy largos se ve reflejado en frecuencias bajas.

	[18] : Esos dos gráficos dan exactamente la misma información ¿cuál es más fácil de graficar? El del dominio de la
	frecuencia.

	[19] : El domingo de la frecuencia da la misma que la del tiempo. Ver el tema de la señal continua en cero ¡es cero! (la
	celeste). Acá se ve qué dominio es más fácil de graficar y entender. Para ello hay que entender los análisis de Fourier
	(se piden los conceptos de Fourier: cómo se convierten, qué significan, etc).

# Análisis de Fourier:
---------------------

	- Furier Matemático francés que demostró que cualquier señal compuesta (es decir como la que está en la 19, ) es la suma
	  de varias señales simples (senos y cosenos) de diferentes frecuencias y amplitudes. Esa suma va a poder ser descompuesto
	  en un señales simples. Se puede pasar de distintos dominios:
		* Serie de Fourier: cuando la señal periódica.
		* Transformada: cuando la señal es NO compuesta.

	Se puede descomponer y saber qué frecuencias vienen.  Se utiliza para todo lo que respecta a computación.

	[24] : Se puede ver las señales periódicas (señal cuadrada: señal digital de dos niveles). Se descompone la series en otras más
	simples.

	[25] : Transformada de Fourier: tiene muchísimas aplicaciones en al vida cotidiana.

	[27] : Cuando es periódica cuando se transforma al Dfrec el dominio queda como en 19 o 24. Esa señal que nos dá es
	discreta, en el medio no nos da nada, sólo en determinados lugares del tiempo.  En cambio en una señal no periódica
	(dominio del tiempo) al dominio de la frecuencia se transforma en una continua.

	[28]: Resumen del análisis de Fourier.

	Clasificación de señales:
		- Dominio de la frecuencia: espectro de la señal. Una vez que se tiene en el domino de la frecuencia se puede
		  clasificar en banda base (arranca en cero) y en pasa banda (no arranca en cero) [30]
		- Pasa banda: la frecuencia más bajas no son consideradas, ya que no arranca de cero.

# Tarea:
-------
	- Se sube a la noche las presentaciones y videos visto hoy.
	- Se sube actividad práctica (no es obligatoria entregar, pero si sirve para la auto-evaluación en 15 días).
	- Se abre un foro de consulta para la unidad 3.
