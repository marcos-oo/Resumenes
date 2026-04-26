## Deadlock:
> El deadlock se da cuando se cumplen las siguientes 4 condiciones:
- **Exclusión mutua**: Al menos un recurso debe estar en modo no compartido (sólo un proceso puede usarlo a la vez). Si otro proceso solicita el recurso, el proceso solicitante ten­drá que esperar hasta que el recurso sea liberado.
- **Retención y espera**: Un proceso debe estar reteniendo al menos un recurso y esperando para adquirir otros recursos adicionales que actualmente estén retenidos por otros procesos.
- **Sin desalojo**: Los recursos no pueden ser desalojados; es decir, un recurso sólo puede ser liberado voluntariamente por el proceso que le retiene, después de que dicho proceso haya completado su tarea.
- **Espera circular**: Debe existir un conjunto de procesos en espera, tal que cada uno espere un recurso retenido por el siguiente.
#### Tratamiento de Deadlocks:
- Utilizar protocolos que aseguren que nunca se llegue a Deadlock.
	Previenen una de las 4 condiciones necesarias.
	- Mutua exclusion: Abrir archivos solo en modo lectura por ejemplo.
	- Espera y retención: A los procesos se les asignan los recursos necesarios de antemano.
	- Sin desalojo: Matar un recurso, liberar la cadena de dependencias.
	- Espera circular: A cada recurso se le asigna un valor y solo se pueden ir pidiendo los recursos con valores de forma creciente. Si hay orden de este tipo y es de forma circular, hay absurdo.
	Evasion:
	- El proceso debe indicarle al SO cuáles van a ser los recursos máximos que puede llegar a solicitar durante su tiempo de vida.
	- Se hace una simulación del proceso, fijándome si es dar el recurso causa un estado inseguro como Deadlock.
	- ![[Pasted image 20260425090316.png]]
- Utilizar protocolos que identifiquen si el sistema se encuentra en Deadlock:
	Deteccion:
	- Se simula la asignacion de recursos para ver si pueden satisfacerse las peticiones.
	- Precisa una matriz de **peticiones actuales**, una de **recursos asignados** y un vector de **recursos totales**.
	- Alto overhead
	Recuperacion:
	- Finalizar procesos:
		- Todos los que se encuentran en Deadlock (un poco overkill).
		- Uno a uno hasta que se resuelva (mayor overhead).
	Desalojar recursos:
	- Volver al proceso expropiado a un estado previo al Deadlock.
	- Puede generar starvation si sigo retrocediendo el mismo proceso.
	*Factores para elegir a la victima*:
	- La prioridad y el tipo del proceso
	- Tiempo actual de ejecución
	- Cuántos y qué tipo de recursos ha utilizado o necesita

- Utilizar protocolos
## Recursos
- Recursos consumibles: Interrupc, senal, mes
- Recursos reusables: Memorioa, arhcivos, semaforos
Pueden tener mas de una instancia,
El proceso