# Clase nº 11 : 30/06/2020

Telefonía Móvil (última clase) NO ENTRA dentro del examen

Telefonía inalámbrica: disminuir costos, dar servicios de telefonía. Permite estar en movimiento. En vez de que la señala viaje por
un medio guiado,sino que viajen por medio de inalámbrico.
Teléfono inalámbrico, tenía su base a la línea telefónica y un teléfono que tenía cierto alcance. Pero de telefonía fija.

En determinadas ciudades que no pudieron hacer una red de telefonía porque están lejos, que ponen una radio, que se comunica a la
central mediante un radio enlace.

WLL: permite transmitir datos, se transmite telefonía a través de una.
Telefonía IP: se conecta a internet, es una computadora y se transmite todo mediante internet.

Protocolos bluethhot es por la cercanía.

Lo que son comunicaciones inalámbrica se pueden dar muchos servicios, el fin es ahorrar la infraestructura de los medios guiados y
dar servicios a dispositivos que se encuentran en movimiento.

Por ejemplo las patrullas, se comunicaban a la estación-base. Todas las patrullas que se encuentran dentro de un radio se
comunicaban con una antena,y las que no estaban dentro, no.

Se comenzó a necesitar un sistema que sea escalable. Es decir, permitir el mismo servicio pero sin modificar la potencia de la
antena. Mientras más potencia, más caros.
¿Cómo hacer que el sistema sea escalable para ampliar el rango de cobertura? ¿y qué pasa si se agergan patrullas? Varias patrullas
pueden transmitir a diferentes frecuencias (sino todas se escuchan y se superponen).

Para poder tener diferentes canales y usuarios, de alguna manera haya que dividir el espectro (Multiplexación por frecuencia). Con
el ancho de banda que me dan, se divide por cada canal y se tiene la cantidad de usuarios o clientes que se pueden tener.  Se
puede imaginar una la ciudad como Florencio varela, La Plata o una ciudad grande, ¿Cómo se puede hacer para tener un ancho de
banda limitada con más usuarios? Se utiliza Multiplexación por cantidad. => Rehuso de frecuencias. Mas cliente con el mismo ancho
de banda.

## Rehuso de frecuencias
Ancho de banda y se divide en 7 partes distintas (se puede dividir en más) Quien lo divide es el prestador del ancho de banda.  de
A hasta G. De los 100MHz hasta los 700MHz (rango del espectro electromagnético) y ese se divide y se tiene a cada uno de 100MHz Si
para cada usuario se requiere 10Mhz, por lo que se puede poner hasta 70 usuarios.
	- Pregunta: Con el mismo ancho de banda ¿Cómo puede hacerlo escalable? Metiendo más usuario sin tener que recurrir a
	  agrandar el ancho de banda. Lo que se hace es dividirlo como sigue:
		* Ancho de banda total: de 1Mhz a 700Mhz
		* Cada usuario: 10 Mhz
		* Cantidad de usuarios totales: Hasta 70 usuarios.
	Este esquema requiere 7 antenas base, más clientes pero mayor inversión ¡OJO!.

En el diagrama,en cada A es una antena. Como están dispuestas muy alejado, NO se interfieren las frecuencias por estar muy lejos.
Lo que se hace es poner una antena con un determinado rango de cobertura. Sólo se solapan en los límites, pero se atenúan de tal
manera que sólo recibo la que está más cerca. El esquema se puede repetir la cantidad de veces que se quiera.
Si se tiene un lugar con mucha densidad poblacional, lo que se hace es elegir cada uno de sos grupos más pequeños y se repite
el esquema pero más pequeños, limitando el tamaño de cada celda.

[6] Antiguamente se destinaba la telefonía móvil en dos sistemas:
	* A:se le asignaba de un rango a otro para transmisión y otro para recepción
	* B: lo mismo

Cada servicio del celular actual está dividido en frecuencia: Datos, mensaje de texto, voz. Dependiendo del ancho de banda que se
le otorgue, si se le da más a internet, menos a voz. Todo depende de la tecnología del momento que se disponga.

Página 7: tipos de celdas según el alcance. Es importante
	¿Cómo elegir una celda? Relación entre el área que se quiere cubrir con respecto a la cantidad de usuarios.
	Si se está en una zona rural es preferible con una macro-celda, para cubrir toda la zona, porque no se tiene muchos
	usuarios.

	- Cuando se sobre pasa el límite de la zona,el usuario queda en espera, aparece un tono como que no está disponible.
	Indicando que está sobrecargado el sistema. ¿Cuándo ocurre? Cuando está bien diseñado, no ocurriría casi nunca. Porque
	ninguna empresa quiere que no se comuniquen los clientes. Sin embargo, hay situaciones que hace que se sature, ninguno de
	estos sistemas está pensado cuando hay muchísimos clientes, como en un recital multitudinario, cuando todos quieren hablar
	al mismo tiempo.
	Pero no pasa eso con Whatsapp, porque los protocolos hacen que haya reintentos, queda en espera, y cuando tiene señala lo
	manda, tarda poco segundos (donde quizás hizo 100 intentos en pocos segundos).

	Cuanto más poblado mayor cantidad de divisiones de celdas.

	Si dos dispositivos transmite en 2 frecuencias a la vez, se solapan las frecuencias. En el mismo lugar NO hay que
	transmitir a la misma frecuencia. La potencia que emita cada una de las antenas, llegue hasta determinado lugar. Y que en
	ese lugar haya otra antena. Ese criterio está explicado en la página 8 creo.

	En frecuencia son distintas por eso es que en el límite se sigue escuchando al límite.

Cada móvil se conecta a la estación base que más cerca esté. ¿Y si tiene la misma distancia? Es mediante un intercambio, lo que se
hace es comunicar más lejos, más potencia, entonces la batería dura mucho menos ¿por qué? Porque la potencia es por la energía
que gasto. Se conecta a la que la potencia sea menor para ahorro de batería. Si estamos en un lugar con poca señal, más potencia,
entonces desgasta la batería más rápido.
Si la estación base está llena de usuarios disponibles, entonces al móvil le niega el acceso, y el móvil se conecta a la otra
estación base (En la imagen BSS).

La comunicación entre las EB con el controlador (BSC) todos se conectan al centro de conmutaciones de Móviles MSC. Funciona este
último como un Swich, por ejemplo un usuario se quiere comunicar con otro usuario se quiere comunicar con otro a otra ciudad.
Esto lo hace por el número de teléfono, dependiendo quién es el que llama, la base reenvía la comunicación donde se encuentre.

AUC: cuenta con determinada información para poder poner el costo tarifario al usuario adecuado.

Los primeros celulares se compraba en un teléfono en un país y en otro no se podía usar. Eso es porque trabajaba en determinado
rango de frecuencia. Los smartphone trabajan rangos de frecuencias muy diversos, y maneja muchos protocolos. Lo primer oque hace es
que se hace con otra país, se envían paquetes a la EB entonces se da cuenta qué protocolo utiliza en esa región y transmite por ese
protocolo.

Se tienen el Switch con la frecuencia de paquetes de internet y también para el de voz. La tecnología del teléfono mediante
diversas maneras.

- Cuando se sobrepasa el limite de la zona, el ultimo usuario queda en espera? o colapsa todo?

Móviles en movimiento, paso a la órbita de la segunda EB (hand-over) Tiene que pasar de una EB a la otra isn perder la
comunicación. Los limites entre antenas, no es tan claro, sino que baja la potencia a medida que se aleja de la antena.
Hay un determinado umbral de Handover en la que el móvil debe cambiar de EB.
Si la celda es la última que hay, entonces el celular se va a seguir comunicando con esa última EB hasta que se quede sin señal.
Pero si no, si hay otro EB, entonces ase pasa a la otra.

Como el celular transmite datos digitalizados, pasa de una EB a otra sin que el usuario se de cuenta.
Si no hubiera re-uso de frecuencias, entonces en las zonas donde se solapan, lo que habría sería mucho ruido ya que se.
El rango de frecuencia debe ser diferentes para que no haya solapamiento.

Es lo que pasa con las radios cuando unas las escucha cuando se viaja por la ruta.

Lo que se modifica en cada salto de Tecnología móvil es:
	- El ancho de banda
	- Y la modulación

Ese nombre es un protocolo, y ese protocolo determina el ancho de banda y eso depende del objetivo del protocolo.
	- Con 2G no se podía navegar mucho, tenía un ancho de banda para internet muy reducido. Útil para lo que eran mensajes de
	  texto y llamadas de voz.
	- Con 3G los dispositivos eran más inteligentes, por lo que se podía navegar mejor y tenía aplicaciones específicas para
	  tener una mejor interacción con el contenido multimedia, entonces 3G agranda el canal de datos para poder conectarse a
	  internet.
	- Con 4G aumenta el ancho de banda en internet pero con más calidad (videos en HD, música,contenido multimedia)
	  aplicaciones de telefonía de voz y mensajes SMS es más acotado.
	- 5G cambia mas ancho de banda pero está pensado en app de tiempo real. No se nota mucho la diferencia entre 4G y 5G, pero SI en
	  las de tiempo real. Por ejemplo los autos autónomos, respuesta en tiempo real. Ver videos y esas cosas no cambia mucho, porque
	  4G ya estaba pensado para eso, pero cambia para Tiempo real.
