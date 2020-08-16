# Filmina:
	- Clase 3 Datos y Señales (parte B) : Desde página 17

# Clase nº 5: 12/05/2020

La clase NO se tocan temas nuevos. El cuestionario pasa para la semana que viene.
Canal de ancho de banda estrecho, en este caso se pierden armónicos, por lo que se pierde toda la calidad de la señal original

# Atenuación:
Decibel (dB): mide las intensidades de potencia relativas de dos señales o una señal en dos puntos diferentes.
El decibel es negativo si una señal se atenúa y es positivo si una señal se amplifica

Si la señal se transmite por un medio donde la velocidad de propagación varía con la frecuencia, los distintos armónicos o
componentes del espectro de frecuencias de la señal no viajan todas a la misma velocidad. Esto puede provocar que las diferentes
componentes de la señal lleguen con distinta fase.

# Ruido
Ruido: Es el conjunto de señales extrañas a la transmisión que se introducen en el medio de transmisión provocando alteraciones de
amplitud del voltaje y variaciones de frecuencia.
	Ejemplo: El ruido térmico, que es el movimiento aleatorio de los electrones en un cable, que crea una señal adicional no
	enviada originalmente por el transmiso


La relación Señal/Ruido (en inglés Signal to Noise Ratio SNR o S/N) se define como la proporción existente entre la potencia de la
señal que se transmite y la potencia del ruido que la corrompe. Este margen es medido en decibelio.

# Límite de la tasa de transmisión:
Una consideración importante en la transmisión de señales digitales es lo rápido que se pueden enviar por un canal, en bps.

La velocidad de transmisión (tasa de bits) depende de 3 factores:
	I.   El ancho de banda disponible.
	II.  Los niveles de señales utilizados.
	III. La calidad del canal (nivel de ruido).

Se han desarrollado dos modelos teóricos para calcular la tasa de bits:
	 El modelo de Nyquist para un canal sin ruido;
	 El modelo de Shannon para un canal ruidoso

# Modelo de Nyquist:  Sin ruido

Nyquist define la máxima capacidad de transmisión teórica para un canal sin ruido.

En 1927, Nyquist determinó que el número de pulsos independientes que podían pasar a través de un canal de telégrafo, por unidad
de tiempo, estaba limitado a dos veces el ancho de banda del canal.

## Dos observaciones:
	- La tasa de bits máxima es proporcional al ancho de banda del canal
	- El aumento de M puede reducir la confiabilidad del sistema.

# Modelo de Shannon: Con ruido

De la fórmula del canal sin ruido podríamos pensar que si incrementamos la cantidad de niveles de las señales podemos transmitir a
una tasa ilimitada.
Un canal real siempre tiene ruido. En 1944 Shannon desarrolló la fórmula denominada Capacidad de Shannon para determinar la máxima
tasa de bits teórica de un canal. Donde:
 	- C Capacidad de transmisión del canal (bps)
 	- B Ancho de banda del canal (Hz)
 	- SNR Relación señal a ruido (relación de potencias, adimensional).

En esta fórmula no hay indicación del nivel de señal, lo que significa que, sin importar los niveles que se tengan, no se puede
conseguir una velocidad mayor que la capacidad del canal. La fórmula define la característica del canal y no el método de
transmisión

# Relación entre Nyquist y Shannon

De la fórmula del canal sin ruido podríamos pensar que si incrementamos la cantidad de niveles de las señales podemos transmitir a
una tasa ilimitada.

A medida que incrementamos los niveles, si el canal mantiene las características (nivel de ruido, ancho de banda, etc), es más
difícil que el receptor distinga entre las señales recibidas. Por lo que el aumento de niveles de señal reduce la fiabilidad del
sistema.

En la práctica es necesario usar ambos métodos para encontrar los límites y los niveles de la señal
	- La capacidad de Shannon da el límite superior.
	- La tasa de bits de Nyquist dice cuántos niveles de señal son necesarios

# Retardo en Redes de datos

Ancho de Banda (Bandwidth): Es una medida de la capacidad del sistema para transportar información.
	- El ancho de banda en hertz, hace referencia al rango de frecuencias en una señal compuesta o al rango de frecuencias que
	  un canal puede transmitir.
	- El ancho de banda medido en bit por segundo hace referencia a la velocidad de transmisión en bits en el canal o enlace.
	  Lo cual es comunmente denominado como la capacidad del canal.

	* Rendimiento (Throughput): Es una medida del desempeño de un sistema, específicamente en el área de redes puede hacer
	  referencia al número de bits que pueden ser enviados a través del medio en un intervalo de tiempo.

	* Latencia (Latency or Delay): Es el retardo en tiempo en el que incurre un bit en el viaje desde su origen hasta su
	  destino.

Velocidad de Propagación: Es la velocidad a la cual un bit viaja a través de un medio desde su origen hasta su destino.
	* Tiempo de Propagación (Latencia) = Distancia / Velocidad de Propagación

Velocidad de Transmisión: Es la velocidad a la cual todos los bits en un mensaje son enviados a su destino.
	* Tiempo de Transmisión = Tamaño del Mensaje / ancho de banda bps













