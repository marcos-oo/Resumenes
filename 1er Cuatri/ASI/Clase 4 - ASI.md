## Requerimientos
Lo que se genera en un departamento, se información o un concepto, puede afectar a muchos otros, nunca es algo aislado.
Al hablar de requerimientos, hay que aclarar si es que se hace DENTRO de un área o con el resto.
#### Ejemplo:
> El sector de contaduría quiere generar una factura para cada venta que se hace. Para ello el sistema emite una factura de venta.

Es el sistema de información del área de contaduría.

V1
**Requerimientos Funcionales:**
- El sistema debe emitir una factura de venta.
- El sistema debe actualizar el stock.
- El sistema debe actualizar tesorería.
**Requerimientos No Funcionales:**
- La factura se emite de forma impresa.
**Problemas:**
- No indica temporalidad de cuando hacer las acciones?
- Falta especificidad / completitud: Que hacemos con la factura?
- Ambiguedad: Actualizar tesoreria? Que es? Que se actualiza?
- Si es de SW, debe actualizars los requerimientos para adaptarse a eso.
## Casos de Uso:
> Especifican el comportamiento deseado de un sistema desde el punto de vista del usuario, describiendo QUÉ debe hacer el sistema o subsistema, aclarando quienes participan (agentes) pero no CÓMO lo hacen. Permiten definir el sistema, sus límites y las relaciones con el entorno. 
### Características:
- Están expresados en forma de forma que lo entienda el usuario, que es quien interactuara con el sistema.
- Se documentan con texto informal.
- Documentan que hace el usuario y que hace el sistema, haciendo así énfasis en como interactúan. 
- Son iniciados por un único elemento externo.
### Utilidad de los Casos de Uso:
- **Analizar**: Para identificar y organizar actores y sus roles. 
- **Documentar**: Un medio para documentar y visualizar los requerimientos funcionales.
- **Comunicar**: Ayuda a los desarrolladores y los clientes lleguen a un acuerdo sobre los requisitos, facilitando la creación del contrato.
### Importancia de los Casos de Uso:
> Proporcionan una perspectiva de alto nivel que permite entender lo que los usuarios necesitan del sistema, sin entrar en detalles técnicos innecesarios en las primeras fases del desarrollo. Conectan las necesidades del usuario con las funcionalidades del sistema permitiendo identificar excepciones y flujos alternativos clave.

### Especificaciones de Casos de Uso:
