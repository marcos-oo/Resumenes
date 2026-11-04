### Cascada Pura (Pure Waterfall)

- **Explicación:** El proyecto avanza a través de una secuencia ordenada y discontinua de fases (desde el concepto del software hasta las pruebas del sistema), basándose en la creación de documentos que se pasan de una fase a la siguiente.
- **Cuándo se utiliza:** En ciclos de productos con una definición estable, metodologías bien entendidas, actualizaciones de mantenimiento bien definidas, o cuando se cuenta con un equipo técnico débil o inexperto.
- **Ventajas:** Ayuda a encontrar errores en etapas tempranas de bajo costo, proporciona gran estabilidad en los requisitos, minimiza la sobrecarga de planificación al hacerla toda al principio y brinda estructura al proyecto.
- **Desventajas:** Es muy inflexible, exige especificar completamente los requisitos antes de diseñar o programar, dificulta retroceder para corregir errores, genera demasiada documentación para proyectos rápidos y muestra pocos signos de progreso hasta el final.

### Codificar y Corregir (Code-and-Fix)

- **Explicación:** Se comienza con una idea general y se usa una combinación informal de diseño, codificación, depuración y pruebas hasta que el producto está listo para lanzarse.
- **Cuándo se utiliza:** En proyectos minúsculos que se desecharán pronto, programas de prueba de concepto pequeños, demostraciones de corta duración o prototipos descartables.
 - **Ventajas:** No tiene sobrecarga de planificación, documentación o control de calidad, no requiere experiencia para utilizarse y muestra signos de progreso inmediatamente.
 - **Desventajas:** Es peligroso para proyectos que no sean diminutos, no ofrece forma de evaluar el progreso o la calidad, y si se descubre un error fundamental avanzado el proyecto, hay que tirar el trabajo y empezar de nuevo.
 
### Espiral (Spiral)

- **Explicación:** Es un modelo orientado al riesgo que divide el proyecto en miniproyectos o iteraciones, donde cada uno aborda uno o más riesgos importantes hasta resolverlos todos, terminando luego como un modelo de cascada.
 - **Cuándo se utiliza:** En proyectos con riesgos considerables, como requisitos o arquitectura poco entendidos, o posibles problemas de rendimiento y tecnología.
- **Ventajas:** A medida que aumentan los costos, los riesgos disminuyen; proporciona un alto control de gestión y ofrece indicaciones tempranas si existen riesgos insuperables.
- **Desventajas:** Es un modelo complicado que requiere una gestión atenta, experta y concienzuda, y puede resultar difícil definir hitos objetivos que indiquen cuándo se está listo para la siguiente iteración.

### Sashimi (Cascada con fases superpuestas)

- **Explicación**: En lugar de utilizar fases secuenciales y discontinuas, las fases del proyecto (como el diseño arquitectónico y el diseño detallado) se superponen entre sí.
- **Cuándo se utiliza:** Es un enfoque razonable para proyectos que adquieren conocimientos importantes a medida que avanzan en su ciclo de desarrollo y que funcionarían mal con planes de desarrollo estrictamente secuenciales.
- **Ventajas:** Si se mantiene la continuidad del personal entre las distintas fases, permite reducir sustancialmente las necesidades de documentación.
- **Desventajas:** Al haber superposición de fases, los hitos se vuelven más ambiguos y resulta más difícil rastrear el progreso con precisión. Además, realizar actividades en paralelo puede generar mala comunicación, suposiciones erróneas e ineficiencias.

### Cascada con subproyectos
      
- **Explicación:** Si la arquitectura divide el sistema en subsistemas lógicamente independientes, el proyecto se separa en múltiples subproyectos donde cada uno procede a su propio ritmo con el diseño detallado, la codificación y las pruebas.
- **Cuándo se utiliza:** Cuando el sistema tiene áreas fáciles de diseñar y no hay razón para retrasar su implementación mientras se espera la resolución de áreas complejas.
- **Ventajas:** Permite realizar tareas de la cascada en paralelo, evitando que el trabajo se estanque por completo debido a una sola área problemática.
- **Desventajas:** El principal riesgo es enfrentarse a interdependencias imprevistas entre los componentes del producto
### Cascada con reducción de riesgos

- **Explicación:** Coloca un ciclo de espiral orientado a la reducción de riesgos en la parte superior del modelo de cascada para abordar áreas de incertidumbre antes de avanzar a las siguientes fases.
- **Cuándo se utiliza:** Cuando se necesita comprender y definir los requisitos completamente (usando prototipos de interfaz o storyboards) o desarrollar un núcleo de alto riesgo antes de comprometerse a un proyecto a gran escala.
- **Ventajas:** Ayuda a superar los problemas asociados con la rigidez del modelo de cascada tradicional al abordar el riesgo (como los requisitos o la arquitectura) al principio del proyecto.
- **Desventajas:** La fuente no lista desventajas específicas para este modelo en particular más allá de las generales heredadas de la cascada tradicional.

### Prototipado Evolutivo (Evolutionary Prototyping)

- **Explicación:** Se desarrolla el concepto del sistema a lo largo del proyecto, comenzando por los aspectos más visibles, demostrándolos al cliente y refinando el prototipo según los comentarios hasta que es "suficientemente bueno" para lanzarse como producto final.
- **Cuándo se utiliza:** Cuando los requisitos cambian rápidamente, el cliente es reacio a comprometerse con un conjunto de requisitos, el área de aplicación es poco conocida o los desarrolladores dudan sobre la arquitectura óptima.
- **Ventajas:** Produce signos de progreso visibles y constantes, lo cual es muy útil cuando hay una fuerte exigencia de velocidad de desarrollo.
- **Desventajas:** Es imposible saber al inicio cuánto tiempo tomará crear un producto aceptable o cuántas iteraciones serán necesarias, y puede convertirse fácilmente en una excusa para usar el modelo de codificar y corregir.

### Entrega por Etapas (Staged Delivery)

- **Explicación:** Se realiza el concepto, análisis de requisitos y diseño arquitectónico para todo el programa de forma secuencial, pero el diseño detallado, codificación, depuración y pruebas se hacen y entregan en etapas sucesivas.
- **Cuándo se utiliza:** Cuando se conoce exactamente lo que se va a construir, pero se desea entregar funcionalidad útil a los usuarios antes de finalizar todo el proyecto.
- **Ventajas:** Pone software funcional en manos de los clientes tempranamente, proporciona signos tangibles de progreso y ayuda a mantener la presión del calendario en un nivel manejable.
- **Desventajas:** No funcionará sin una planificación técnica y de gestión muy cuidadosa para repartir el trabajo a tiempo y dar cuenta de todas las dependencias técnicas entre componentes.

### Diseño según Calendario (Design-to-Schedule)

- **Explicación:** Se planifica el desarrollo en etapas sucesivas priorizando las características más importantes primero, con la particularidad de que si llega la fecha límite, se omiten las funciones de menor prioridad no terminadas.
- **Cuándo se utiliza:** Cuando el sistema tiene una fecha de entrega inamovible (como una feria comercial o fin de año) o para componentes del producto que no se desean en la ruta crítica.
- **Ventajas:** Garantiza que se tendrá un producto funcional listo para ser lanzado en una fecha específica.
- **Desventajas:** Si no se completan todas las etapas, se habrá desperdiciado tiempo especificando, arquitectando y diseñando características que nunca se enviarán.

### Entrega Evolutiva (Evolutionary Delivery)

- **Explicación:** Es un punto intermedio entre el prototipado evolutivo y la entrega por etapas; se desarrolla una versión inicial centrada en el núcleo del sistema, se muestra al cliente y se refina según sus comentarios iterativamente.
- **Cuándo se utiliza:** Cuando se desea combinar la capacidad de realizar correcciones sobre la marcha con la necesidad de tener versiones funcionales entregables en varias etapas del desarrollo.
- **Ventajas:** Aumenta la visibilidad del progreso, reduce el riesgo al dividir el trabajo en subproyectos pequeños y permite una gran capacidad para hacer cambios de dirección a mitad de camino.
- **Desventajas:** El nivel de control o de previsibilidad depende de qué tantas solicitudes de cambio del cliente se decida acomodar.

### Diseño según Herramientas (Design-to-Tools)

- **Explicación:** Se incorpora una capacidad al producto únicamente si está directamente soportada por herramientas de software existentes (generadores de código, bibliotecas, etc.); si no está soportada, se omite.
- **Cuándo se utiliza:** En entornos excepcionalmente sensibles al tiempo o para implementar prototipos descartables de forma rápida.
- **Ventajas:** Reduce drásticamente el tiempo de implementación y puede permitir construir más funcionalidad total en un periodo corto.
- **Desventajas:** Se pierde mucho control sobre el producto final (qué características se incluyen y cómo se implementan) y se genera una fuerte dependencia hacia las estrategias y la estabilidad financiera de los proveedores de las herramientas.

### Software Comercial Listo para Usar (Commercial Off-the-Shelf Software)

   - **Explicación:** Consiste en comprar un producto de software ya existente en lugar de construir un sistema personalizado.
   - **Cuándo se utiliza:** Cuando las soluciones comerciales pueden satisfacer las necesidades operativas de manera más inmediata que un desarrollo a medida.
   - **Ventajas:** Está disponible de inmediato para los usuarios y los proveedores pueden actualizar el producto con el tiempo para acercarse más a sus necesidades.
   - **Desventajas:** Rara vez satisfará todas las necesidades y el producto nunca coincidirá exactamente con la visión mental ideal del software que se tenía.