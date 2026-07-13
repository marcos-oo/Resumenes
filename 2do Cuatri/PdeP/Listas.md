## Predicados para listas
- `length/2`, relaciona una lista con un number para ver si la longitud de la lista es igual al number
- `member/2`, relaciona un elemento con una lista para ver si el elemento se encuentra dentro de la lista. ES INVERSIBLE.
- `sum_list/2`, relaciona una lista con un number para ver si la suma de todos los elementos de la lista es igual al number
- `nth1/3`*(indice, lista, elemento)*, indica si se encuentra el *elemento* en la posición *indice* de la *lista*. El número después de nth indica con que número comienza el indexado de la lista.

## Pattern matching `[Cabeza | Cola]`
`?- [Cabeza|Cola] = [1,2,3]`
`Cabeza=1, Cola=[2,3]`

`?- [Cabeza|Cola] = [elemento]`
`Cabeza=elemento, Cola=[]`

## Definiendo nuestro propio length
``` prolog
length([],0)
length([__|Cola], Cantidad):-
	length(Cola, CantRestante),
	Cantidad is CantRestante+1
```

## `findall/3`
``` prolog
?- findall(Plato, prepara(ivo, Plato), Platos).
Platos=[risotto, asado].
```
Esto nos provee todas las respuestas en una lista para, por ejemplo, calcular cuantas hay con un length.

## Cuando usar listas
- Cuando el orden importa.
- Cuando se quiere conocer la cantidad total.
- Cuando se quiere el resultado de sus agregados.



Aquí tienes la resolución directa del problema planteado en la imagen.

Para obtener la ecuación de un plano necesitas un punto por el que pasa, $P_0(x_0, y_0, z_0)$, y un vector normal (perpendicular) a dicho plano, $\vec{n} = (A, B, C)$.

El principio fundamental es que para cualquier punto genérico $P(x, y, z)$ que pertenezca al plano, el vector que une $P_0$ con $P$, denotado como $\vec{P_0P} = (x - x_0, y - y_0, z - z_0)$, debe ser perpendicular al vector normal $\vec{n}$.

Dos vectores son perpendiculares si su producto escalar es igual a cero:

$$ \vec{n} \cdot \vec{P_0P} = 0 $$

Sustituyendo los componentes:

$$ (A, B, C) \cdot (x - x_0, y - y_0, z - z_0) = 0 $$

Al desarrollar este producto escalar obtienes la **ecuación escalar-vectorial del plano**:

$$ A(x - x_0) + B(y - y_0) + C(z - z_0) = 0 $$

Si distribuyes y agrupas los términos constantes, llegas a la **ecuación general**:

$$ Ax + By + Cz + D = 0 $$

Donde la constante $D$ se calcula como $D = -(Ax_0 + By_0 + Cz_0)$.

A continuación, puedes visualizar de forma interactiva cómo se comporta este plano en el espacio 3D al modificar las coordenadas del punto y los componentes del vector normal.