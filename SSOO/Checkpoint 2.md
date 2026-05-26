
Este es el flujo de trabajo correcto entre los tres módulos principales:

- **Kernel Scheduler:** Administra los procesos y decide el orden de ejecución enviando el PID a la CPU según su algoritmo de planificación.
    
- **Kernel Memory:** Actúa como el almacenamiento central de las instrucciones (archivos de pseudocódigo) y los contextos de ejecución (PCBs).
    
- **CPU:** Funciona como el intérprete activo. Recibe el PID , busca el contexto inicial en el Kernel Memory y luego comienza su ciclo de instrucción, pidiéndole las instrucciones a la memoria paso a paso para ejecutarlas.