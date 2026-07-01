## Condiciones de carrera
##### Introducción:
En un programa en el que 30000 hilos suman 1 a una variable, llegamos siempre a un numero cercano a 30000, pero no siempre a 30000. Porqué?
```C
int hilo(var)
{
	var++;
	return var;
}
```
Si hay varios hilos trabajando en paralelo, puede suceder que tomen el mismo valor, le sumen 1, y ambos escriban el mismo valor, haciendo que la suma de uno de ellos haya sido irrelevante.
##### Condiciones de Bernstein:
*(Deben cumplirse las 3)*
- Mas de un proceso o hilo usa mismo recurso.
- Al menos uno de los que usa el recurso lo modifica.
- Los accesos al recurso son concurrentes.

###### Region critica:
Parte del codigo que necesita proteccion para que no haya condiciones de carrera.
- Debe contener operacion sobre un recurso compartido.
- Debe ser lo mas chica posible.
- Debe ejecutarse en forma atómica.

##### Requerimientos:
(*Para asegurar que no hayan condiciones de carrera.*)
- **Mutua exclusion**: Solo un proces / hilo debe poder acceder a la seccion critica a la vez.
- **Progreso**: Solo los procesos/hilos que se encuentran en la entrada o salida pueden participar en la decision de quien es el proximo a ingresar en las sección critica.
- **Espera** limitada: No puede haber un hilo que espere infinitamente por un recurso.
- **Velocidad de los procesos/hilos**: La sección critica debe funcionar independientemente de la velocidad de estos.

##### Soluciones:
De software:
- **Turnos**: Que haya una variable de turno, en la que se elige a que hilo/proceso le toca. 
- **Interesados**: Setear un struct de booleanos que dice a quien le interesa la zona critica.
- **Solucion de Peterson**: Combinacion de las anteriores, marco quien esta interesado y los turnos.
De hardware:
- **Deshabilitado de interrupciones**: Evitar que las instrucciones de la solución sean interrumpidas con las de otros procesos.
- **Instrucciones atómicas**: Cada instruccion existe en un mismo ciclo de instruccion, nada puede meterse en el medio.
De SO:
- **Semaforos**:
	- *Con espera activa*: Se hacen *syscalls* que le dan un valor a una variable que define si cada proceso puede o no hacer su trabajo.
	- *Con bloqueo*: Chequeo el valor, y si no me da el turno a mi hago `block()`, si me lo da hago `wakeup()`.
##### Semaforos:
*Tipos de semaforos:*
- **MUTEX**: Permite solucionar el problema de la exclusion mutua. Siempre se inicializa en 1.
- **Contadores:** Permite controlar el acceso a una cantidad de recursos. Se inicializa en **N** (N=cantidad de instancias total).
- **Binarios**: Permite garantizar orden de ejecucion, existe en dos estados, libre u ocupado.

	Si `semaforo > 0` hay espacio libre. *(Aplica solo a contadores)*
	SI `semaforo < 0` hay procesos bloqueados esperando.

***LOS SEMAFOROS NO PUEDEN INICIALIZARSE EN NEGATIVO.***

*Usos de los semaforos:*
- Mutua exclusion.
- Ordenar ejecucion.
- Limitar acceso a una cantidad de instancias.
- Productor - Consumidor.
##### Monitores: 
Abstracciones creadas por nosotros de los mecanismo que proveeen mutua exkusión.
Pueden usarse para no necesitar escribir constantemente todos los controles de los semaforos en todos los scripts.
##### Inversión de prioridades:
**Prioridades**: P1<P2<P3.
0. **P1** adquiere un recurso y hace un `wait()`.
1. **P3** ingresa al sistema y necesita el recurso, se hace un `block()`.
2. **P2** ingresa al sistema, desaloja a p2 ya que tiene mayor prioridad.
Cagaron a **P3**, tiene mayor prioridad pero va a tener que esperar a que termine **p2**.
Solucion? **Herencia de prioridades**.
3. Al comenzar **P2**, **hereda** la cola de espera de **P1**, en la que se encuentra en espera **P3**. 
4. Se ejecuta y finaliza **P3**.
5. Se ejecuta y finaliza **P2**.
6. Se ejecuta y finaliza **P1**.


##### NOTAS:
- No entendi MUTEX.
- Estudiar PRODUCTOR - CONSUMIDOR.