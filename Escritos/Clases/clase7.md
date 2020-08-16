# Filmina:
----------
	- Clase 4 - Transmisión Digital (Parte B)

# Clase nº 7:  26/05

# Muestreo:
----------
Es cómo se toma los valores por cada tiempo.

Para realizar la conversión de Analógico a Digital, se tienen 3 pasos basicamente:
	- La señal analógica se *muestrea*, es decir, se toman valores por cada tiempo.
	- La señal muestreada se *cuantifica*.
	- Los valores cuantificados se *codifican* como flujos de bits.

El Teorema de Nyquist demuestra que la reconstrucción exacta de una señal periódica continua en banda base a partir de sus
muestras, es matemáticamente posible si la señal está limitada en banda y la tasa de muestreo es superior al doble de su ancho de
banda. Dicho de otro modo, la información completa de la señal analógica original que cumple el criterio anterior está descrita
por la serie total de muestras que resultaron del proceso de muestreo. No hay nada, por tanto, de la evolución de la señal entre
muestras que no esté perfectamente definido por la serie total de muestra

# Muestreo
La señal analógica es muestreada cada Ts segundos, donde Ts es el intervalo o período de muestreo.
 El inverso de Ts se denomina tasa de muestreo o frecuencia de muestreo (fs = 1/Ts).
 El proceso de muestreo a veces se denomina Modulación por Amplitud de Pulsos (PAM).

 Existen 3 métodos de muestreo:
	- Ideal: Sólo se muestrean los pulsos pero es de difícil implementación.
	- Natural: Es fácil de implementar. Conserva la forma de la señal, pero dificulta la cuantificación.
	- De Cresta Plana: Fácil de implementar, facilita la cuantificación y es de Circuito Sample and Hold.
	  Es el más utilizando y mentiene por cierto tiempo

## Tasa de muestreo:
	Según el Teorema de Nyquist, Como condición la frecuencia de muestreo debe deser al menos 2 la frecuencia más alta de su
	contenido en el dominio de la frecuencia. La frecuencia de muestreo, debe ser como mínimo 2 veces la señal espectral.

	Se debe tener en cuenta:
		- Una señal con ancho de banda infinito no puede ser muestreada y reconstruida de manera perfecta. Es por ello que
		  la señal debe estar limitada en banda y la tasa de muestreo ser superior al doble de su ancho de banda.
		- Si la señal es pasa-bajos, la frecuencia más alta coincide con el ancho de banda.
		- Si la señal es pasa-banda, el ancho de banda es menor a la frecuencia más alta

# Cuantificación:
El resultado del muestreo es una serie de pulsos con valores de amplitud entre las amplitudes máxima y mínima de la señal

Los pasos de la cuantificación son:
	1. Suponemos que la señal analógica original tiene amplitudes instantáneas entre Vmín y Vmáx.
	2. Dividimos el rango en L zonas, cada una de altura \frac{Vmax-Vmin}{L}
	3. Asignamos valores cuantificados de 0 a L - 1 al punto medio de cada zona.
	4. Aproximamos el valor de la amplitud de la muestra a los valores cuantificados

## Niveles de Cuantificación:
	En realidad, el número de niveles L depende del rango de amplitudes de la señal analógica y de la precisión con la que
	necesitamos recuperar la señal. Elegir valores más bajos de L aumenta el error de cuantificación si hay mucha fluctuación
	en la señal.

		- Si la amplitud de una señal fluctúa solo entre dos valores, se requieren únicamente dos niveles.
		- En cambio, si la señal tiene muchos valores de amplitud, se necesitan más niveles de cuantificación (por
		  ejemplo, para la señal de la voz).
		- En la digitalización de audio, L normalmente se elige como 256; en video normalmente son miles

Se define al error de cuantificación o ruido de cuantificación a la señal en tiempo discreto y amplitud continua introducida por
el proceso de cuantificación y que resulta de igualar los niveles de las muestras de amplitud continua a los niveles de
cuantificación más próximos

# Codificación:

Luego de que cada muestra se cuantifica y se decide el número de bits por muestra, cada muestra se puede cambiar a una palabra de
código de n-bit. Si el número de niveles de cuantificación es L, el número de bits es nb = log2 L. La tasa de bits viene dada
por:

Decodificador PCM:
	- Para recuperar la señal original a partir de las palabras codificadas se requiere del decodificador PCM.
	- El decodificador utiliza circuitos para convertir las palabras de código en un pulso que mantiene la amplitud hasta el
	  siguiente pulso.
	- Luego, se pasa la señal a través de un filtro pasa bajos para suavizar la señal de la escalera en una señal analógica.
	- Si se cumple con el Teorema de Nyquist y si hay suficientes niveles de cuantificación, se volverá a crear la señal
	  original

Modulación Delta: Página 21
Modulador: Página 22
Demodulador: Página 23

Modo paralelo, modo serie : página 24
Transmisión modo paralelo: Página 25
Transmisión modo serie: página 27

Transmisión modo serie asincrónica: página 28
Transmisión modo serie sincrónica: página 31

## Modulador:
	- El modulador se usa en el emisor para crear un flujo de bits a partir de una señal analógica.
	- El modulador construye gradualmente una segunda señal que se asemeja a una escalera contra la cual compara la señal
	  analógica de entrada, para cada intervalo de muestreo.
	- El proceso registra los pequeños cambios positivos o negativos, llamados delta δ. Si el delta es positivo (amplitud de
	  la señal analógica mayor), el siguiente bit es 1; si es negativo, el proceso registra un 0.
	- La unidad de retardo es necesaria para mantener la función de escalera durante un período entre dos comparaciones


En la filmina nº 8:
¿Cuál es la frecuencia minima con la que se dbe muestrear para recuperar la señal y cuál es el ancho de banda de la señal?

Ancho de banda = f máxima - f minima. Pero justo en la imagen de arriba se hace fmax - fmin = 0
2 veces la frecuencia máxima

Creo que el ejemplo está mejor explicado en el libro.

Filmina nº 14: cada franja tiene 5 volt según la cuenta de la filmina nº 13

Filtro pasa bajo: la función es tratar que la señal original sea suavizada.
	Un filtro paso bajo corresponde a un filtro electrónico caracterizado por permitir el paso de las frecuencias más bajas y atenuar
	las frecuencias más altas. El filtro requiere de dos terminales de entrada y dos de salida, de una caja negra, también
	denominada cuadripolo o bipuerto, así todas las frecuencias se pueden presentar a la entrada, pero a la salida solo estarán
	presentes las que permita pasar el filtro. De la teoría se obtiene que los filtros están caracterizados por sus funciones de
	transferencia, así cualquier configuración de elementos activos o pasivos que consigan cierta función de transferencia serán
	considerados un filtro de cierto tipo.
