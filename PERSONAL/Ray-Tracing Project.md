## How Is an Image Created?
Se necesita una superficie bi-dimensional, que actúe como medio para la proyección de lo que se tiene adelante. Esta superficie puede ser imaginada como una rebanada de una pirámide cuya punta se encuentra en el ojo del observador y se extiende a través de su linea de vista. 
## Perspective Projection
La perspectiva traslada objetos tridimensionales a un plano bi-dimensional, creando la ilusión de profundidad. Se logra dibujando lineas desde cada esquina de un objeto hacia el "ojo" del observador, dejando marcas en el plano cuando lo atraviesan.
![[ProjPerspective.png|306]]Luego, lineas se dibujan entre estas marcas para representar los bordes de este cubo, creando la ilusión de que el polígono creado es en realidad un objeto 3D.
## Light and Color
Una vez que se dibujan las marcas en el plano y se conectan entre si, debe hacerse algo conocido como "Shading", osea colorear dentro de las lineas.
#### Fotones
El color y luminosidad de un objeto se determinan mas que nada por como interactúa la luz con el material del que esta compuesto el objeto. Esta luz esta compuesta de pequeñas partículas llamadas Fotones, los cuales, al chocar con una superficie, pueden ser absorbidos, reflectados o transmitidos, todo dependiendo de que este hecho el objeto.
La regla principal que rige esto es que la cantidad de fotones que relejan / son absorbidos / transmitidos debe ser, en total, igual a la cantidad original, es decir, no puede crearse luz.

$$ \Huge F_{\text{total}} = F_{\text{absorbido}} + F_{\text{reflejado}} + F_{\text{transmitido}} $$
#### Materiales
Los