## Modelos de Ciclo de Vida

### 1. Cascada Pura (Pure Waterfall)

- El proyecto avanza a través de una secuencia ordenada de fases discontinuas impulsadas por la documentación.

- Este modelo funciona bien para proyectos complejos que poseen requisitos estables y están a cargo de equipos sin experiencia.

- Su mayor debilidad es la profunda inflexibilidad, lo que hace que sea extremadamente difícil y costoso adaptar cambios en los requisitos a mitad del proceso.

### 2. Codificar y Corregir (Code-and-Fix)

- Los desarrolladores omiten la planificación y el diseño formal para saltar directamente a la codificación.

- Este enfoque no requiere gastos generales ni experiencia especializada en gestión.

- Es altamente peligroso y debe limitarse estrictamente a programas pequeños y desechables de prueba de concepto.

### 3. Espiral (Spiral)

- El proyecto se divide en miniproyectos orientados al riesgo donde la escala aumenta solo después de resolver los riesgos principales.

- Los costos aumentan a medida que disminuyen los riesgos, proporcionando un excelente control de gestión y una detección temprana de problemas insuperables.

- El proceso es muy complicado y exige una gestión experta para definir hitos objetivos y verificables.

### 4. Cascadas Modificadas (Modified Waterfalls)

- **Sashimi:** Se permite la superposición de fases para reducir la carga de documentación, aunque esta ambigüedad hace que el progreso sea más difícil de rastrear con precisión.

- **Subproyectos:** La arquitectura del sistema se divide en subsistemas lógicamente independientes que se implementan a su propio ritmo en paralelo.

- **Reducción de Riesgos:** Una espiral de reducción de riesgos precede a las fases de cascada para definir claramente los requisitos o resolver arquitecturas de alto riesgo antes de comprometerse por completo.

### 5. Prototipado Evolutivo (Evolutionary Prototyping)

- El concepto del sistema se desarrolla iterativamente construyendo primero los aspectos visibles y refinando el prototipo en función de los comentarios continuos del cliente.

- Es altamente efectivo cuando los requisitos cambian rápidamente o cuando el cliente no está seguro de lo que quiere.

- Es imposible predecir el cronograma final del proyecto o el número total de iteraciones de desarrollo requeridas.

### 6. Entrega por Etapas (Staged Delivery)

- El concepto completo del software y la arquitectura se planifican por adelantado, pero el diseño detallado y la codificación se entregan en etapas sucesivas.

- Proporciona a los clientes software funcional de manera temprana y genera señales tangibles de progreso.

- Requiere una planificación meticulosa para contabilizar correctamente las dependencias técnicas entre los diferentes componentes del producto.

### 7. Diseño Según Cronograma (Design-to-Schedule)

- Las características se priorizan rigurosamente y se implementan en etapas para garantizar un producto funcional para una fecha límite inamovible.

- Actúa como una red de seguridad para proyectos con fechas de entrega estrictas.

- El tiempo y los recursos se desperdician permanentemente en características de menor prioridad si el cronograma expira antes de que se implementen.

### 8. Entrega Evolutiva (Evolutionary Delivery)

- Este modelo se sitúa entre la entrega por etapas y el prototipado evolutivo, priorizando el desarrollo de un núcleo de sistema estable antes de incorporar los comentarios del cliente.

- Proporciona un equilibrio entre el control estructural y la flexibilidad de los requisitos.

### 9. Diseño Orientado a Herramientas (Design-to-Tools)

- Las capacidades del proyecto se limitan estrictamente a la funcionalidad que las herramientas de software, bibliotecas y generadores de código existentes pueden soportar directamente.

- Permite una velocidad de desarrollo excepcional al evitar por completo la implementación manual de características complejas.

- El equipo de desarrollo sacrifica el control total sobre la funcionalidad del producto y asume riesgos de dependencia relacionados con proveedores comerciales.

### 10. Software Comercial Listo Para Usar (COTS)

- La organización compra software comercial en lugar de construir una solución personalizada.

- El software está disponible de inmediato y proporciona valor mientras los usuarios aprenden a sortear sus limitaciones.

- El producto comprado rara vez coincidirá con la visión idealizada de un software creado a medida.