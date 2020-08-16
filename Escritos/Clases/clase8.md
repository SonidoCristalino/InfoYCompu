# Filmina:
	- Clase 5 - Transmisión Analógica

# Clase nº 8: 02/06/2020

# Transmisión analógica
No siempre se pueden utilizar señales digitales. Como cuando se tienen canales pasabajos, la señal digital se puede tranmisitr sin
problemas, pero si requermimos utlizilar canales pasabanda, ahí la transmisión necesitamos que sea analógica. Esto es lo que se va
a ver en esta clase.

Siempre se hablan de 3 parámetros (y en los que se basan cada uno de los tipos de conversión):
	- Amplitud,
	- el Período o la Frecuencia (en general se habla de frecuencia),
	- y la otra es la Fase (cómo arranca la señal).

Se modificarán según lo que querramos transmitir.

Definir:
	¿Qué es una señal portadora? La vamos a utilizar en los dos sistemas que vamos a analizar para la transmisión digital.
	La emite un Dispositivo emisor es un seno de muy alta frecuecia que hace de seññal base, que el receptor espera recibir y
	de esta forma espera el receptor el mensaje enviado.

Conversión Digital - Analógica (Pasa banda) : Página 4

# Digital - Analógica

[8]:
Elementos de y elementos de señal (De nuevo se puede hacer la analogía con respecto a autos y personas)

Si el canal disponible es un canal pasa banda, no se puede enviar la señal digital directamente al canal, es necesario convertir
la señal digital a una señal analógica antes de la transmisión.

La transmisión en banda ancha o paso banda usando modulación digital implica convertir la señal digital a una señal analógica para
su transmisión.

Los baudios siempre serán menores a la cantidad de bits.

Señal portadora: pagina 6

Sabemos que una onda sinusoidal se define por tres características: amplitud, frecuencia y fase.  Si variamos alguna de estas
características, tenemos una nueva onda sinusoidal. Esta nueva onda podemos utilizarla para representar datos digitales. Tenemos
cuatro mecanismos para modular los datos digitales en una señal analógica (pagina nº 7)

En la transmisión analógica de datos digitales, la tasa en baudios es menor o igual que la tasa de bits.

# Modulación por Desplazamiento de Amplitud (ASK):
El método *más importante* es el de Modulación por Desplazamiento de Amplitud (ASK).
Si o si la transmisión será analógica, por ende lo que se usa ASK. Se tiene una señal portardora de una cierta frecuencia, y lo
que cambia de la señal original es la *amplitud*.
Cuando se tiene 0 no se tiene amplitud y cuando se tiene un 1 entonces se tiene una amplitud determinada. Está todo sincronizado
con los tiempos. La tasa de bits es de cinco en [10].

	En [12] se visualiza la señal portadora (carrier signal) que la da un oscilador. Entra por un lado la señal digital (que
	es una señal digital NRZ, ojo), que se multiplica luego con la señal portadora, entonces lo que se hace es multiplicar, si
	viene un 0 entonces no hay amplitud, en canbio cuando hay 1 entonces se obtiene la amplitud de la señal portadora.
	¡Genial!.  El valor de la señal portadora, la elegimos nosotros, y se implementa con un oscilador.

	Nosotros podemos cambiar el ancho de banda hasta lo que se puede obtener.

	La señal que se transmite NO es periódica, por lo tanto con Fourier

	Es posible cambiar el ancho de banda resultante para que coincida con lo que está disponible.

	Ancho de banda para BASK: página nº 11
	Ancho de banda para MASK multinivel: página nº 14

# Desplazamiento de Frecuencia (FSK):
	Varía la frecuencia, ver en el gráfico cómo es que se Lo que cambia es que cuando es 1 entiende que es una frecuencia y
	cuando es 0 entonces es distinto (que puede ser o no igual a la portadora, en el caso de la filmina es cuando se tiene 0).
	Ver que la cantidad de ciclos cuando es uno es 4 y la señal portadora es de 2, por lo tanto la duplica.

	MFSK usa más ancho de banda que las otras técnicas, por lo que debe usarse cuando el ruido es un problema grave.

	Usa más ancho de banda que las otras técnicas: Pagina nº 16

	BFSK: Página nº 18
	MFSK Multinivel: página nº 19

# Desplazamiento de Fase (PSK):
	[21] Es parecido al de la amplitud. La cadena de bits no es uniporlar sino es BIPOLAR. Ver que cuando es 1 es positivo y
	cuando es 0 es negativo. Por lo que cuando se multiplica por el 1, nos queda en la misma señal que la portadora, y cuando
	se hace por menos, lo que se está haciendo es invertir la fase 180º. Por lo que hace es cambiar la fase ¡Genial!.  Tiene
	la misma características que la de la Amplitud.

	Es un método mejor, porque es menos suceptible al ruido.

# Desplazamiento por cuadratura (combina la de la amplitud con la de fase) [QPSK]:
	Pagina nº 22

## Introducción:

	Cuadratura: una señal está desfazada 90º grados de otro, utiliza 2 bits en la transmisión, en cada elemneto de la señal
	entemos 2 bits, en la cuadratura 2 bist por cada elemanto de la señal, disminutye la tasa en baudios y la banda de ancho
	requerido.

	Ver que en [22] se tienen dos bits que se tranmisten. Las señales portadoras están desfazadas 90º, respecto de la segunda,
	en vez de arrancar hacia arriba, arranca hacia abajo.
	Da como resultado, 4 fases distintas de cada uno de estos ciclos de bits (en verde más abajo de todo)
	Porque se tienen 4 tipos de posibilidades para armar con dos bits.

	Diagramas de constelación [25] se utilizan para que los expertos, al verlos, puedan saber qué tipo de desplzamientos se
	utiliza, qué métodos se utiliza para poder transmitir. Se utiliza para saber si la transmisión está transmitiendo bien.
	El Técnico solicita a la sucursal que le envíe 10 señales y todas las señales en el diagrama deberían de generarse en los
	4 cuadrantes como se visualiza en [29]. Por si se están diagramados en otros lugares, es porque hay ruido Ver que en [29]
	se visualiza que cada tipo de tipos de frecuencia, se utiliza un cuadrante distinto en el Diagrama de Constelación.

## Modulación:
	Ver que hay 4 tipos de gráficos QAM

Diagrama de Constelación: página 25
	Los ejes del plano del diagrama suelen ser llamados "I" (en fase) y "Q" (en cuadratura). En la constelación se representa
	la relación de amplitud y fase de una portadora modulada digitalmente y por lo tanto, el módulo y la fase de cada uno de
	las posibles señales que conforman la modulación.

	Constelación para QPSK: página nº 29

# Conversión Analógico Analógico (modulación analógica):
	Consiste en tener una señala de una frecuencia  alta (portadora) y modificarle alguna característica (como antes). ¿Por
	qué se le cambia si es lo mismo que la analógica? Porque tenemos un canal que es pasa banda por ejemplo, entonces no se
	tienen todo el ancho de bandas, por lo que hay que hacerle cambios. En la radio por ejemplo, hay que hacer este cambio
	para poder transmitir al rango que nos fue asignado.

	Básicamente, la modulación consiste en hacer que un parámetro de la onda portadora cambie de valor de acuerdo con las
	variaciones de la señal moduladora, que es la información que queremos transmitir.

	El proceso de modulación permite adaptar una señal analógica en banda base a una señal analógica pasa banda (con un ancho
	de banda menor).

## Modulación por amplitud (Amplitud Modulada AM)
	Transmisión AM: Donde observando el gráfico queda más claro. Se tiene la señal a tranmisitir (la roja), la señal negra es
	la señal portadora (frecuencia alta). Y la que se transmite es la señal celeste, sino que es ¿Dónde aparece la señal roja
	que se transmite? En la envolvente.
	Es un multiplicador que multiplica  la seál a enviar por la portadora. Esta señala tendra el ancho de banda centrado en la
	portadora, y el ancho de banda será dos veces la original. Si se envía 5kHz, la resultante será aproximadamente en 10kHz.
	Lo que se hace es tranmitir entre 10 kHz. del 530 hasta al 1700 kHz.

	Página 34

## Frecuencia Modulada (FM)
	[35] Se modifica la frecuencia. Cuanto más grande es la señal de audio, la frecuencia es máxima. La señal que realmente se
	envia, mantiene la fase, la amplitud, pero se modifica la frecuencia (es como un acordeon).
	El anhco de banda que se envía es dos veces a (1 * Beta), por lo que es 10 veces más grande el ancho de banda.
	Cada rango de estación de radio tendrá 150kHz, (15 veces más que la FM: se ve que al ser estereo se hace más
	complicado).Cada rango de estación de radio tendrá 150kHz, (15 veces más que la FM: se ve que al ser estereo se hace
	más complicado). Para que no haya solapamiento se toma cada 200kHz por radio.

	Página 35


## Modulación por fase (PM)
	No es muy común el suo de esta modulación [38] No se ve bien cómo s e modifica la fase en este método. Pero bueno, hay que
	imaginarlo, cambia la fase.

	En la transmisión PM, la fase de la señal portadora se modula para seguir la amplitud cambiante de la señal de
	modulación. Se implementa con un oscilador controlado por tensión y un derivador.

	La amplitud y la frecuencia de la señal portadora permanecen constantes, pero a medida que cambia la amplitud de la señal
	de información, la fase de la portadora cambia correspondientement

	Página nº 38



