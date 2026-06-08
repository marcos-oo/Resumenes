## Kernel Scheduler

- **Planificación de mediano plazo.**
- **Desalojo por compactación.**
- **Herencia de propiedades.**

- **Hay segfault cuando se desconecta una CPU**
## Kernel Memory

- **Memoria de Usuario / Datos**
	- Esquema de memoria y Estructura
	- Desconexión del Memory Stick $\implies$ memoria corrupta.

- **Operaciones de segmentos**
	- Creación de segmento
		- Algoritmos de selección de huecos
		- Compactación
	- Eliminación de segmento

- **Operaciones de procesos**
	- Creación de proceso (después veremos si la creación de sus segmentos se hace acá)
	- Suspensión de proceso
	- Des-suspensión de proceso
	- Finalización de proceso (la destrucción de segmentos se hace acá)

- **Operaciones de memoria**
	- Lectura de datos (para **STDOUT** nada más)
	- Escritura de datos (para **STDIN** nada más)

## CPU
- **MMU**
	- **Importante**: Necesitamos que el save context y el pull context¿ incluyan la tabla de segmentos, no solo los registros.
- **Cambiar las lecturas y escrituras de memoria, no son al Kernel Scheduler, son a los sticks.** 
## Memory Stick
#### Todo

## Swap
#### Todo