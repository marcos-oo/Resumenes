### Comienzos de Carbon
El 19 de julio de 2022 Chandler Carruth, un ingeniero principal en Google, presenta Carbon, un experimento de código abierto respaldado por Google, en *Cpp North*, la principal convención de C++ en Canadá.
Él y otros nombres relevantes del ecosistema de C++ como Richard Smith y Kate Gregory (figuras prominentes en el estándar de C++) plantean Carbon como una respuesta a la lentitud del comité ISO de C++ para resolver problemas técnicos.
La idea es el equivalente de TypeScript para JavaScript o Kotlin para Java; una evolución que no descarta lo que ya existe si no que moderniza la sintaxis, acorta los tiempos de compilación e introduce mejoras de seguridad de memoria, entre otras mejoras que ya serán vistas en profundidad.
### Ventajas y Desventajas
##### Ventajas de Carbon sobre C++
- **Sintaxis moderna y limpia**: Elimina reglas y convenciones obsoletas de C++. Su código es más fácil de leer y escribir, acercándose a la ergonomía de lenguajes como Swift o Rust.
- **Genéricos estructurados**: Reemplaza las complejas plantillas (templates) de C++ con un sistema de genéricos más seguro, con comprobación de tipos robusta en tiempo de compilación y mensajes de error comprensibles.
- **Seguridad por defecto**: Introduce fundamentos más seguros para el manejo de memoria y variables (por ejemplo, inicialización obligatoria) para evitar errores críticos muy comunes en C++.
- **Gestión de paquetes integrada**: Diseñado desde cero con herramientas modernas de construcción y gestión de dependencias, un problema histórico en el ecosistema fragmentado de C++.
##### Desventajas de Carbon frente a C++
- **Estado experimental**: Aún está en desarrollo temprano y no está listo para entornos de producción. Sus características y diseño pueden cambiar drásticamente.
- **Ecosistema y comunidad**: C++ tiene más de 40 años de código probado en batalla, motores de videojuegos de primer nivel y bibliotecas para cualquier propósito. Carbon no tiene ecosistema propio todavía.
- **Herramientas inmaduras**: C++ cuenta con compiladores (GCC, Clang, MSVC), depuradores (GDB) y perfiles de rendimiento altamente optimizados. Las herramientas nativas de Carbon están en fase inicial.
- **Riesgo de adopción**: La industria del software es lenta para migrar sistemas críticos. Carbon podría no alcanzar la masa crítica necesaria para convertirse en un estándar, mientras que C++ sigue evolucionando (C++20, C++23, C++26).