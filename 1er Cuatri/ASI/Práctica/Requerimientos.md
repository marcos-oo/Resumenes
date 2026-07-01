# Ejercicio 8
El Club Deportivo San Martín busca implementar un nuevo sistema de gestión de socios para mejorar la atención, el control de accesos y la administración de sus actividades. ==El sistema deberá permitir registrar el alta, baja y modificación de datos de socios==, incluyendo información básica (nombre, DNI, fecha de nacimiento, correo electrónico, categoría de socio y foto de perfil). Cada socio podrá acceder al sistema con su usuario y contraseña para ver su historial de pagos, suscribirse o cancelar actividades deportivas (fútbol, natación, tenis, etc.), y descargar su credencial digital con un código QR que será escaneado al ingresar al club. El sistema deberá registrar cada ingreso al club con fecha y hora, y solo permitirá el acceso si el socio tiene su cuota al día. Los empleados del club tendrán una interfaz administrativa donde podrán consultar listados filtrados por actividad, estado de pago y antigüedad de los socios. 
Además, el sistema deberá permitir generar reportes automáticos mensuales que incluyan estadísticas de asistencia, morosidad y participación por actividad, exportables en formato PDF y Excel. El área de tesorería podrá configurar recordatorios automáticos por correo electrónico para los socios que tengan cuotas vencidas. Si un socio tiene tres meses consecutivos sin pagar, el sistema deberá marcarlo automáticamente como inactivo y restringir el acceso.
Toda la información debe almacenarse en servidores seguros con backups automáticos diarios. El sistema deberá garantizar el acceso simultáneo de hasta 200 usuarios sin degradar el rendimiento. La interfaz deberá estar diseñada para ser utilizada fácilmente desde dispositivos móviles por los socios y desde computadoras de escritorio por el personal administrativo. El diseño deberá seguir los lineamientos de accesibilidad digital vigentes para asegurar el uso por parte de personas con dificultades visuales.

##### A) Defina 3 requerimientos funcionales y 2 requerimientos no funcionales asociados al texto. En caso de no poder deducirse del texto, justifique el motivo de su elección.

*Funcionales*:
- El sistema debe permitir registrar el alta, baja y modificación de datos de socios.
- El sistema deberá registrar los ingresos de los socios al club.
- El sistema debe rechazar el ingreso de todos los socios quienes no tienen su cuota al día.

*No funcionales*:
- El sistema debe generar reportes exportables en formato PDF y Excel.
- El sistema deberá garantizar el acceso simultáneo de hasta 200 usuarios sin degradar el rendimiento.
##### B) Seleccione al menos uno de los requerimientos identificados y clasifíquelo según uno de los criterios vistos en clase (no debe ser clasificado como funcional y no funcional).

- El sistema debe generar reportes exportables en formato PDF y Excel.
Requerimiento de **cliente**, **obligatorio**.

# Ejercicio 9
La empresa EcoMovil, dedicada al alquiler de bicicletas eléctricas, busca modernizar su sistema de gestión debido a las fallas constantes del registro manual que utilizan actualmente en sus tres estaciones distribuidas por la ciudad. En la situación actual, la disponibilidad se controla con cuadernos y planillas Excel, lo que genera errores frecuentes: bicicletas que aparecen alquiladas en dos estaciones al mismo tiempo, unidades que figuran como disponibles cuando ya fueron retiradas y devoluciones asentadas con horas de demora porque el personal olvida registrarlas.
Para resolver estos problemas, EcoMovil desea implementar un sistema centralizado que permita consultar la disponibilidad de bicicletas en tiempo real, registrar cada alquiler y devolución en el momento en que ocurren y mostrar el estado actual de cada unidad (disponible, alquilada o en mantenimiento). La gerencia también requiere generar reportes diarios y semanales, como cantidad de alquileres por estación, bicicletas más utilizadas y unidades que necesiten revisión técnica.
El personal trabaja principalmente desde tablets y teléfonos, por lo que el sistema debe ser accesible desde cualquier dispositivo con conexión a Internet. Para mantener una atención ágil, las operaciones principales deben ejecutarse con un tiempo de respuesta promedio igual o inferior a 1.5 segundos. EcoMovil también solicita que el sistema pueda enviar notificaciones automáticas por correo electrónico o WhatsApp cuando una bicicleta cambie de estado, requiera mantenimiento o se detecten inconsistencias entre estaciones.
El responsable técnico destaca la necesidad de que toda la información esté sincronizada entre estaciones, evitando diferencias en lo que ve cada punto de atención. Finalmente, dado que la mayoría del personal no tiene formación técnica, el sistema debe contar con una interfaz que permita registrar operaciones básicas sin necesidad de capacitación extensa.

##### A) Defina 3 requerimientos funcionales y 2 requerimientos no funcionales asociados al texto. En caso de no poder deducirse del texto, justifique el motivo de su elección.
*Funcionales*:
- El sistema debe permitir consultar la disponibilidad de bicicletas,
- El sistema debe permitir registrar cada alquiler y devolución.
- El sistema debe mostrar el estado actual de cada unidad.
*No funcionales*:
- El sistema debe ser accesible desde cualquier dispositivo con conexión a Internet.
- El sistema debe enviar las notificaciones automáticas por correo electrónico o WhatsApp.
##### B) Seleccione al menos uno de los requerimientos identificados y clasifíquelo según uno de los criterios vistos en clase (no debe ser clasificado como funcional y no funcional).
- El sistema debe permitir consultar la disponibilidad de bicicletas,
Es un requerimiento del **cliente**, **obligatorio**.
