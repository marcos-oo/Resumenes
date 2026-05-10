# Objetivos:
### Módulo Kernel Scheduler
- Planificación de corto y largo plazo con FIFO y RR.
- Administración del estado BLOCK y las colas de los módulos de IO.
- Administración de los Mutex y sus colas de Procesos sin herencia de prioridades.

### Módulo CPU
- Realiza el ciclo de instrucción completo siendo capaz de interpretar y ejecutar instrucciones (Sin memoria).

### Módulo Kernel Memory
- Devolver lista de instrucciones.
- Devolver un valor fijo de espacio libre (mock).
- Contestar OK a lecturas y escrituras de memoria sin implementarlas.

### Módulo IO
- Completo.

# Desglose:
## Módulo Kernel Scheduler:
### Planificación
#### Planificador de Largo Plazo
Se va a encargar de ingresar procesos de NEW a READY sin ninguna limitación. Puede recibir un mensaje del Kernel Memory que se detectó corrupción en una parte de la memoria. Finalizar todos los procesos y el Kernel Scheduler con código BSOD.
#### Planificador de Corto Plazo
Se va a encargar de gestionar las transiciones entre READY y EXEC