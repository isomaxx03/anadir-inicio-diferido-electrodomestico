# anadir-inicio-diferido-electrodomestico
Sirve para añadir inicio diferido a un electrodomestico (lavadora, lavavajillas...) que no lo tiene. Usa una interfaz muy simple basada en un solo boton con LED RGB. Es necesario que el electrodoméstico disponga de un boton de inicio y pueda permanecer de forma indefinida a la espera de que se pulse dicho botón para iniciar la marcha. Si ello no se cumple, puede usar mi otro programa https://github.com/isomaxx03/anadir-inicio-diferido-electrodomestico-mediante-apagado

Simplemente se inicia con el boton apagado. Al pulsar una vez se ilumina en rojo (2 horas de retraso), si se pulsa otra vez, azul (4 horas), si se pulsa otra, verde (6 horas), repitiendo el ciclo en el rojo.

Al pulsar prologandamente empieza la cuenta atras. El código de color cambia para dar retroalimentación al usuario, de cuál es la duracción seleccionada, con el siguiente código: amarillo 2 horas, celeste 4 horas, blanco 6 horas. Al terminar la cuenta el color será verde.

En cualquier momento se puede hacer doble click y el dispositivo queda en el estado inicial, sin cuenta atras, con el boton sin iluminación y esperando la primera pulsación para definir la cuenta atras.

Hardware:
El boton es un pulsador simple. Se pueden usar tres led rojo, verde y azul o un led RGB de catodo común. Idealmente, para facilitar construcción y mejor resultado estético, se usa un pulsador con LED RGB integrado, de catodo común. Si se compra el botón para 5V de tensión de los LED, no hará falta añadir ninguna resistencia, de lo contrario, añadir las resistencias adecuadas.
El pin 6 del arduino controla un relé, cuyos contactos NO (normally open, normalmente abierto) cerrarán durante un instante el circuito del boton de inicio del electrodoméstico en cuestión, simulando una pulsación del botón del electrodoméstico. Es necesario haber puenteado dicho boton del electrodoméstico, en paralelo con los contactos NO del relé.
