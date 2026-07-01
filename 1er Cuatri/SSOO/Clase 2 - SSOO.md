## Multithreading

**Hilo**: Unidad básica mínima de utilización de la cpu, consiste en un juego de registros y una pila. Convive con otros hilos en el mismo espacio de memoria, compartiendo código datos y recursos, ergo fácil conectarlos entre sí. Problema! No hay protección. 
- Cada uno tiene su TCB (Thread Control Block).

**Proceso**: Hay un hilo 0 que ejecuta el main(), creando los otros hilos. Este hilo 0 inicia y  finaliza TODO el proceso.
- Un proceso puede tener más de una taza de ejecución (hilo).

**DIferencias entre hilos y procesos**:
- Los hilos pueden interactuar sin el SO, los procesos no.
- Mayor eficiencia en el cambio, ya que comparten mucho de sus procesos. (caches válidas para el switch)
- Mayor eficiencia en la creación de los hilos, si se comparte mucho hay menos para crear de 0.
- Muere un proceso y mueren todos sus hilos.
- Un proceso multihilo puede recuperarse de la muerte de un hilo.
- Los hilos en su mayoría son independientes, uno muere el resto no tiene porque (salvo el hilo 0).

**Estado de un proceso**: La combinación de los estados de sus hilos.
- Si hay alguno en ejecución, se considera **ejecutando**.
- Si no hay ninguno en ejecución, pero si hay listos, se considera **listo**.
- De lo contrario, está **bloqueado**.

Si creo un hilo, ya se empieza a ejecutar. Para hacer esperar a que termine, join.

**Tipos de Hilos**:
- **KLT**: Hilos a nivel kernel. El SO conoce el hilo y qué ejecuta. Usa la biblioteca pthread.
- **ULT**: HIlos a nivel usuario. El SO conoce el hilo, pero no sabe qué ejecuta. Su manejo se hace con una biblioteca a nivel usuario. Más rápidos para la conmutación de contexto. No permiten el paralelismo entre hilos pares, ya que como el SO no sabe que se está ejecutando, no sabe si tiene que distribuir entre unidades de ejecución. Implementan su propia planificación.