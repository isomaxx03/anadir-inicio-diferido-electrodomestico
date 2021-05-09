# anadir-inicio-diferido-electrodomestico
Sirve para añadir inicio diferido a un electrodomestico (lavadora, lavavajillas...) que no lo tiene. Usa una interfaz muy simple basada en un solo boton con LED RGB. Es necesario que el electrodoméstico disponga de un boton de inicio y pueda permanecer de forma indefinida a la espera de que se pulse dicho botón para iniciar la marcha. Si ello no se cumple, puede usar mi otro programa https://github.com/isomaxx03/anadir-inicio-diferido-electrodomestico-mediante-apagado/edit/main/README.md

Simplemente se inicia con el boton apagado. Al pulsar una vez se ilumina en rojo (2 horas de retraso), si se pulsa otra vez, azul (4 horas), si se pulsa otra, verde (6 horas), repitiendo el ciclo en el rojo.

Al pulsar prologandamente empieza la cuenta atras. El código de color cambia para dar retroalimentación al usuario, de cuál es la duracción seleccionada, con el siguiente código: amarillo 2 horas, celeste 4 horas, blanco 6 horas

En cualquier momento se puede hacer doble click y el dispositivo queda en el estado inicial, sin cuenta atras, con el boton sin iluminación y esperando la primera pulsación para definir la cuenta atras.

Hardware:
El boton es un pulsador simple. Se pueden usar tres led rojo, verde y azul o un led RGB de catodo común. Idealmente, para facilitar construcción y mejor resultado estético, se usa un pulsador con LED RGB integrado, de catodo común.
El pin 6 del arduino controla un relé, cuyos contactos NO (normally open, normalmente abierto) cerrarán el circuito del boton de inicio del electrodoméstico en cuestión. Es necesario haber puenteado dicho boton, en paralelo con los contactos NO del relé.
