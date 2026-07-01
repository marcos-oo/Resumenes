## Predicados para listas
- `length/2`, relaciona una lista con un number para ver si la longitud de la lista es igual al number
- `member/2`, relaciona un elemento con una lista para ver si el elemento se encuentra dentro de la lista. ES INVERSIBLE.
- `sum_list/2`, relaciona una lista con un number para ver si la suma de todos los elementos de la lista es igual al number
- `nth1/3`*(indice, lista, elemento)*, indica si se encuentra el *elemento* en la posición *indice* de la *lista*. El número después de nth indica con que número comienza el indexado de la lista.

## Pattern matching \[Cabeza | Cola]
`?- [Cabeza|Cola] = [1,2,3]`
`Cabeza=1, Cola=[2,3]`

`?- [Cabeza|Cola] = [elemento]`
`Cabeza=elemento, Cola=[]`

## Definiendo nuestro propio length
```
length([],0)
length([__|Cola], Cantidad):-
	length(Cola, CantRestante),
	Cantidad is CantRestante+1
```
