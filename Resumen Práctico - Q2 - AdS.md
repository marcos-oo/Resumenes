## User Story
Dentro de un *scrum* se realizan *sprints*. Cada *sprint* tiene, entre otras cosas, un *product backlog* en el que se almacena un listado de las características del producto a construir. Estos items pueden ser redactados con muchas técnicas, una de ellas siendo la **user story**.
Una **historia de usuario** o **user story** es una breve descripción de algo que el sistema necesita hacer para satisfacer una necesidad del usuario.
Sirve para registrar que quiere el usuario de forma fácil y sencilla, para facilitar el dialogo entre el equipo y los distintos actores del proyecto y para asegurar que el desarrollo esté enfocado en generar valor real.
Está escrita en lenguaje cotidiano, es corta y fácil de entender. Se compone de tres elementos.
#### Elementos - Card
La card debe ser atómica y se debe poder escribir en una tarjeta del tablero.
Sigue la siguiente estructura:
- *Como* `<rol de usuario>`
- *Quiero* `<funcionalidad/necesidad>`
- *Para* `<beneficio a obtener>`
Esta estructura permite ver con claridad la necesidad del usuario, enfocarse en el valor del negocio y facilitar el dialogo con el equipo de desarrollo.

#### RutaPampa
**Objetivo: Dado el siguiente enunciado, elaborar 3 historias de usuario. Incluir por cada historia, la card, la conversación y la confirmación.**
RutaPampa S.A. es una empresa argentina de transporte interurbano que opera recorridos de larga distancia entre capitales provinciales y destinos turísticos. El Sector de Ventas y Atención al Pasajero administra hoy la comercialización mediante boleterías en terminales y un pequeño call center que toma reservas manuales. Este sector tiene como función asegurar la ocupación de los servicios, aplicar políticas comerciales (tarifas, descuentos por temporada, convenios con estudiantes y jubilados) y asistir a los pasajeros ante cambios o cancelaciones.
En los últimos dos años la competencia comenzó a vender por canales digitales y la gerencia general definió como meta incrementar la ocupación en temporada baja y reducir las filas en boletería en temporada alta. Además, el área de Tráfico reporta frecuentes sobreventas de asientos por errores de carga manual y el área de Administración necesita emitir facturas en tiempo y forma, contemplando percepciones e impuestos vigentes. Por este contexto, el Sector de Ventas y Atención al Pasajero solicita iniciar la venta de tickets por internet y reorganizar parte de su operatoria.
Actualmente, los datos de servicios (origen, destino, horarios, paradas intermedias, tipo de coche y asientos disponibles) se registran en planillas internas y se envían por correo al inicio de cada día a las boleterías. Para cada venta presencial, el boletero elige el servicio, asigna un asiento, cobra en efectivo o tarjeta en POS local y entrega un boleto impreso. En caso de cambios, el pasajero debe acercarse a la terminal para reprogramar. Para convenios especiales, el boletero solicita documentación (certificados de alumno regular, constancias de jubilación) y aplica descuentos manualmente.
Con la venta en línea, el Sector espera que los pasajeros puedan buscar combinaciones por fecha y destino, conocer políticas de equipaje y cambios, elegir asientos y pagar con diversos medios (tarjeta, transferencia, billeteras virtuales). El área de Facturación necesita que, al confirmarse un pago, se genere el boleto digital y la factura electrónica con los datos del comprador o del pasajero, según corresponda. El área de Tráfico requiere visualizar en tiempo real la ocupación por servicio para reforzar unidades si hay alta demanda. Los conductores y el personal de plataforma deberán validar embarques escaneando un código QR del boleto digital aun si no hay buena conectividad en la terminal.

##### Cliente
**Como** cliente **quiero** poder sacar mis boletos digitalmente **para** no tener que esperar en filas para sacar un viaje.
 ¿Qué filtros debe poder seleccionar el cliente al elegir su viaje?
 ¿Qué políticas sobre la empresa deben ser indicadas al cliente?
 ¿Como se muestran los asientos aún disponibles en el colectivo?
 ¿Puede el cliente elegir cualquier asiento?
 ¿Qué método de pago puede elegir el cliente
 El cliente debe poder filtrar la lista de viajes disponibles por fecha y destino.
 La plataforma debe informar al cliente sobre las políticas de equipaje y de cambios.
 Los asientos deben mostrarse en la disposición que ocupan en el vehículo, indicando si están ocupados o libres.
 El cliente puede elegir todos los métodos de pago digitales habilitados.