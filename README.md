Objetivo de la práctica

Implementar la comunicación serial entre dos microcontroladores para analizar su interacción interna y externa mediante la adquisición y procesamiento de señales, permitiendo comprender su funcionamiento dentro de un sistema embebido de control.


Materiales utilizados


1 Raspberry Pi Pico

1 ESP32

1 Chasis para robot de dos ruedas

2 Motores DC con reductora

1 Driver puente H L298N

3 Sensores infrarrojos de línea

Batería para alimentación de motores

Conexión y montaje

Cables jumper

Interruptor
Durante el desarrollo del proyecto no fue necesario implementar un regulador de 5V, ya que la alimentación utilizada fue suficiente para el correcto funcionamiento del sistema.

Desarrollo de la práctica

El sistema fue diseñado con el objetivo de dividir las tareas entre dos microcontroladores, permitiendo una arquitectura modular donde cada dispositivo realiza una función específica dentro del sistema.
Programación de la Raspberry Pi Pico
La Raspberry Pi Pico fue utilizada para la lectura de los sensores infrarrojos encargados de detectar la línea en el suelo. Se utilizaron tres sensores de línea:

•	Sensor izquierdo

•	Sensor central

•	Sensor derecho

Cada sensor proporciona una señal digital dependiendo de si detecta la línea o el fondo. A partir de estas lecturas, el microcontrolador interpreta la posición del robot con respecto a la trayectoria.
Posteriormente, la Raspberry Pi Pico envía mediante comunicación serial UART un comando que representa el estado detectado de los sensores hacia el segundo microcontrolador.

