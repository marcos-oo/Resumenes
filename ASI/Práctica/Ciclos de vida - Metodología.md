# Ejercicio 125
Trekkologi es una compañía multinacional, principal proveedora de elementos de camping y de alta montaña en varios países de América y Europa. La empresa comenzó a desarrollar un nuevo sistema de facturación, dado que realizaban las facturas de forma manual, y por el creciente aumento de sus ventas, los operadores administrativos no daban a vasto con toda la carga laboral. La administración tiene un alto grado de conocimiento de todos los flujos de facturación y el equipo de desarrolladores tiene amplia experiencia en este tipo de sistemas. Inicialmente nos comentaron que se deben realizar demostraciones a los principales inversores a los 2, 4, 6, 8, 10 y 12 meses del proyecto. De una conversación, se tomaron los siguientes registros:
- La dirección debe ser multicountry.
- Tenemos grata experiencia en otros programas utilizando SQLServer como administrador de base de datos, así que este sistema debe utilizar lo mismo.
- Sería útil que el sistema genere reportes, tales como, total de ventas, total de facturas, total de NCs, entre otros.

En el día de hoy, se lo vio al gerente de tecnología decir: “Se encontraron 28 fallas en los requerimientos correspondientes al módulo 1 de facturación, las cuales hay que corregir, y las salidas del ABM de clientes no fueron las esperadas, al cliente le debe llegar un correo cuando se lo da de alta y esto no está pasando”.

##### A) Indicar a qué etapa de la metodología corresponde. Justificar.
El texto corresponde a la etapa de *Pruebas*.
Se menciona que en el día de la fecha fueron encontradas 28 fallas correspondientes al módulo 1 y las salidas del ABM no fueron esperadas. Esto implica que el producto ya existe en la realidad, descartando todas las etapas anteriores al desarrollo. Además, ya se puso en funcionamiento, por lo que el desarrollo finalizó y comenzó ya la etapa de pruebas.
Se sigue en la etapa de pruebas porque las fallas que se comentan no han sido corregidas aún, algo necesario para pasar de ella.

##### **B)** Indicar qué CV utilizaría. Justificar. 
Utilizaría la *Entrega por Etapas*.
Al mencionar múltiples entregas a lo largo del desarrollo del producto, se descartan todos los ciclos de vida menos 3, el *Prototipado Evolutivo*, la *Entrega por Etapas* y la *Entrega Evolutiva*.
Las demostraciones del producto a los inversores parecen estar proyectadas a realizarse en fechas o momentos determinados del desarrollo y hay un número específico de ellas, por lo que se descarta el *Prototipado Evolutivo*.
Al ser demostraciones a los inversores, el desarrollo debe priorizar la parte visible del producto, no su núcleo, por lo que se descarta también *Entrega Evolutiva*.
Eso nos deja con *Entrega por Etapas* como la solución.

# Ejercicio 126
MiPan es la proveedora de harinas y trigos más grande de Latinoamérica, con más de 300 clientes en todo el continente. Todos los principios de mes, el sector de cobranzas se ve desbordado por la cantidad de cheques que tienen que emitir y la cantidad de facturas que tienen que procesar. Para descomprimir la situación, el equipo de gestión de IT de MiPan determinó que con el pequeño presupuesto asignado, sólo se puede implementar un sistema de automatización RPA que reciba y procese las facturas. Todo el sector está ansioso por ver avances cuanto antes y ellos tienen un alto conocimiento de los requerimientos de negocio.
##### A) Indicar a qué etapa de la metodología corresponde. Justificar.
El texto corresponde a la etapa de *Estudio de Factibilidad*.
Hace énfasis en que el equipo de gestión de IT hizo un análisis de las condiciones actuales, en este caso el presupuesto asignado, y en base a eso escogieron la alternativa de solución que más se alinea a sus objetivos, un sistema de automatización RPA.
Sabemos que el diagnóstico ya fue realizado, ya que el problema desde el principio como algo conocido.
Sabemos que no llega aún al diseño, ya que no se mencionan especificaciones de ningún tipo, solo un concepto general de lo que se hará.

##### B) Indicar qué CV utilizaría. Justificar.
Utilizaría el modelo de *Entrega por Etapas*.
Se busca ver avances lo antes posible, por lo que se descartan la mayoría de los modelos, quedando *Code-and-Fix*, *Prototipado Evolutivo*, *Entrega por Etapas* y *Entrega Evolutiva*.
Es un producto importante y a largo plazo, se descarta Code-and-Fix.
Todo el sector espera ver avances, se prioriza la parte visual, se descarta *Entrega Evolutiva*.
El cliente tiene conocimiento profundo de los requerimientos del proceso, se descarta el *Prototipado Evolutivo* al no ser necesaria la flexibilidad que este provee con referencia a estos.

# Ejercicio 127
TuProducto es una compañía de venta electrónica que está abriendo nuevas operaciones en Latam. La empresa cuenta con alta experiencia en la venta electrónica e implementación de canales de venta similares, líderes en Argentina desde hace más de 10 años, sin embargo, existen requerimientos desconocidos que puedan surgir en la implementación del sistema en cada país. Los clientes confían plenamente en la organización, por lo que no necesitan ir viendo avances parciales. En la reunión del día de hoy, se detectó que el problema de vender a nivel regional, es que algunos países no permiten la venta de productos en dólares y no hay forma de realizar una actualización de los precios Minuto a Minuto, en base a la cotización de la moneda en cada país.
##### A) Indicar a qué etapa de la metodología corresponde. Justificar.
El texto corresponde a la etapa de *Diagnóstico*.
No se han ideado alternativas de solución al problema diagnosticado, por lo que *Estudio de Factibilidad* y todas las etapas que le proceden.
Se conocen los requerimientos del cliente, por lo que ya se superó el *Reconocimiento*, y el diagnóstico del problema parte de un conocimiento detallado del proceso de ventas a nivel regional, indicando que fue superada ya la fase de *Relevamiento*.
Eso nos deja con la etapa de *Diagnóstico*.

##### B) Indicar qué CV utilizaría. Justificar.
Utilizaría el modelo *Espiral*.
Esto se debe a que:
- Podrían surgir requerimientos nuevos para la implementación del sistema en cada país, problemas que espiral previo al desarrollo atraparía.
- La empresa posee un alto nivel de experiencia y conocimiento sobre la industria a la que se adentran.
- Los clientes tienen una confianza plena en la organización, por lo que no se precisan demostraciones de avances parciales (los cuales el modelo *Espiral* no permite).

# Ejercicio 128
La empresa Los Pollos Hermanos S.A. es una consultora que se dedica a realizar sistemas que permiten transformar y manejar la masiva cantidad de información de las ventas de las organizaciones que se encuentran en Albuquerque. En la reunión que tuvo la empresa con un nuevo cliente conocido como Heisenberg, se describió exhaustivamente lo que desea que realice el sistema. El equipo al tener experiencia técnica y en el área, pudo establecer los requerimientos desde un principio. Además, el cliente les detalló que desea ver el progreso del equipo sobre el sistema y no solamente el entregable final. Según nos comenta Heisenberg, el dinero no es problema, dado que los negocios están en alza. El equipo empezó a trabajar en los modelos sobre la solución seleccionada por Gus Fring, teniendo en cuenta que el sistema debería tener varios servidores en la nube y estableciendo que la Base de Datos a ser implementada deberá ser del tipo relacional.

##### A) Indicar a qué etapa de la metodología corresponde. Justificar.
El texto corresponde a la etapa de *Diseño*.
Sabemos que el cliente ya ha escogido una alternativa de solución, por lo que se descarta la etapa de *Estudio de Factibilidad* y todas las que le preceden.
Además, sabemos que el equipo está trabajando sobre los modelos de la solución, pero no sobre la solución en sí, por lo que se descarta la etapa de *Desarrollo* y todas las que le proceden.
Eso nos deja con la etapa de *Diseño*.
##### B) Indicar qué CV utilizaría. Justificar.
Utilizaría el modelo de *Entrega por Etapas*.
Se prioriza la visualización del progreso del desarrollo por parte del cliente, por lo que se descartan los modelos que no prioricen la muestra de progreso visible. Eso nos deja con *Code-and-Fix*, *Entrega por Etapas* y *Prototipado Evolutivo*.
El producto es a largo plazo y maneja grandes cantidades de transacciones, por lo que se descarta *Code-and-Fix*.
Los requerimientos del producto son conocidos desde el principio, por lo que se descarta el uso de *Prototipado Evolutivo*.
Eso nos deja con *Entrega por Etapas*.


# Ejercicio 129
La empresa de ventas online Mercado Liebre, nos contrató para poder analizar y proponer una propuesta de mejora al sistema de logística de sus ventas al interior de buenos aires. Dado que en el análisis del último semestre detectaron que muchos de sus clientes correspondientes a esta zona reclamaron una gran demora al recibir sus productos. En la reunión que se tuvo el día de hoy se procedió a entrevistar al jefe del área de Logística y se realizó un cuestionario para que sea contestado por el resto del personal que conforma el mismo, gracias a esto se pudo tener un mejor entendimiento del problema. Para atender este proyecto se conformó un equipo de personal experimentado, que sepa trabajar con los requerimientos que fueron bien definidos desde el comienzo. Se decidió realizar una revisión al finalizar cada etapa del proceso para poder documentar y darle visibilidad al cliente.
Contamos con la suerte que el cliente no tiene apuro, ni desea tener una visibilidad constante del avance, de todas maneras, se acordó iniciar una etapa antes de finalizar la anterior para ahorrar tiempo. Hoy una de las prioridades es que la solución esté al nivel de una de las empresas líderes del mercado.

##### A) Indicar a qué etapa de la metodología corresponde. Justificar.
El texto corresponde a la etapa de *Relevamiento*.
Se comenta que se realizó un cuestionario para que responda el personal del área de Logística y se entrevistó a su jefe de área. Esto significa que el área afectada ya se conoce, por lo que la etapa de *Reconocimiento* ya fue superada.
Sin embargo, no se ha hecho ningún tipo de diagnóstico real por parte del equipo, ya que los resultados del cuestionario no han sido recibidos aún. Es por eso que no se ha llegado aún a la etapa de diagnóstico.
Eso nos deja en la etapa de *Relevamiento*.

##### B) Indicar qué CV utilizaría. Justificar.
Utilizaría el modelo de *Cascada Modificada - Sashimi*.
El cliente no tiene apuro ni desea una visibilidad constante del avance, por lo que todas las etapas que lo priorizan la fecha, la velocidad o la visibilidad de progreso se descartan.
Eso nos deja con el modelo *Cascada* y todas sus modificaciones y el modelo *Espiral*.
Sin embargo, se hace énfasis en la superposición de etapas con el con chequeos de progreso al final de cada una, siendo el modelo que mas se encaja a lo que pide el cliente *Cascada Modificada - Sashimi*.

# Ejercicio 131
La empresa proveedora de nafta nivel nacional “Nafta Para Todos” lo contrata para cumplir el rol de líder en el nuevo proyecto que pretende mejorar el sistema de facturación de la aplicación actual, pudiendo sumar distintos beneficios populares en el mercado de hoy en día. El proyecto tiene una alta prioridad para la organización, debido a una gran caída de consumo en el último semestre. Actualmente se están corrigiendo los errores detectados a partir de los resultados obtenidos del feedback de los usuarios que están utilizando la fase beta del nuevo sistema, con las nuevas funcionalidades. El proyecto se dividió en 2 instancias, la dirección dejó claro que es necesario tener implementada la primera parte del sistema para el 15 de Diciembre, para aprovechar el gran movimiento de turismo en las vacaciones, y la segunda instancia del proyecto tiene como límite de finalización el 10 de Febrero. La primera parte a implementar cuenta con la generación de descuentos al precio final, por el momento los únicos medios que aplican descuento son “Mercado Paga” y “tarjeta Bisa”.
Mientras que la segunda parte está abocada a la generación de nuevos reportes de venta para que puedan ser consumidos por los gerentes y que puedan ser consumidos por medio de un archivo Excel.

##### A) Indicar a qué etapa de la metodología corresponde. Justificar. 
El texto corresponde a la etapa de *pruebas*, particularmente las pruebas de usuario.
Se están corrigiendo errores sobre un sistema, por lo que ese sistema ya superó la fase de *Desarrollo* y todas las que le preceden. Sin embargo, la solución aún no ha sido implementada, sigue en la fase beta. Eso descarta la fase de *Implementación* todas las que le proceden.
Eso nos deja con la etapa de *pruebas*.

##### B) Indicar qué CV utilizaría. Justificar.
Utilizaría el modelo de *Entrega Calendarizada*.
Se hace énfasis en fechas claves fijas, para las cuales el sistema va a tener que cumplir características específicas, las primeras más centrales y prioritarias que las segundas.
Esta división del proyecto en etapas con prioridad organizadas en tiempo de mayor a menor prioridad es característica del modelo *Entrega Calendarizada*.

# Ejercicio 133
EduNet es una empresa de tecnología educativa que se encuentra enfocada en el desarrollo de una plataforma diseñada para mejorar la experiencia de enseñanza tanto para estudiantes como para profesores. La plataforma desea ofrecer funcionalidades como gestión de cursos, foros de discusión, evaluaciones en línea y seguimiento del progreso de los estudiantes. También, se desea permitir la descarga de las notas de cada curso en formato PDF y persistir los datos en una base de datos no relacional. Durante la fase inicial del proyecto, se comenzaron a desarrollar las funcionalidades más visibles y de mayor impacto para obtener retroalimentación directa de los clientes. Se realizan reuniones periódicas con ellos para demostrar el avance de la plataforma y discutir posibles ajustes o mejoras basados en sus comentarios.

##### A) Indicar a qué etapa de la metodología corresponde. Justificar. 
El texto corresponde a la etapa de *pruebas*, particularmente las pruebas de usuario.
Se están corrigiendo errores sobre un sistema, por lo que ese sistema ya superó la fase de *Desarrollo* y todas las que le preceden. Sin embargo, la solución aún no ha sido implementada, sigue en la fase beta. Eso descarta la fase de *Implementación* todas las que le proceden.
Eso nos deja con la etapa de *pruebas*.

##### B) Indicar qué CV utilizaría. Justificar.
Utilizaría el modelo de *Entrega Calendarizada*.
Se hace énfasis en fechas claves fijas, para las cuales el sistema va a tener que cumplir características específicas, las primeras más centrales y prioritarias que las segundas.
Esta división del proyecto en etapas con prioridad organizadas en tiempo de mayor a menor prioridad es característica del modelo *Entrega Calendarizada*.