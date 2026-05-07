------## Inferencia de tipos:
Tratar de inferir el tipo de una función a partir de verla.
#### EJ 1)
Tenemos la siguiente función:
```Haskell
	floca x y z = z<=y && z>=x
```
Viendo la cantidad de parámetros, el tipo de los mismos y la salida, inferimos que es:
```Bash
	Ord a=> a--> a-->a-->Bool
```
#### EJ 2)
```Haskell
	cantidadDePares = length.filter even
```
```Bash
	[Number]->Number
```
#### EJ 3)
```Haskell
	fDificil x y = take y . filter(not.x)
```
```Bash
	(a-->Bool)-->Number-->[a]-->[a]
```
#### EJ 4)
```Haskell
	ordenarSegun _ [] = []
	ordenarSegun criterio (x:xs) =
	(ordenarSegund criterio . filter (not.criterio)) xs
	++[x]++
	(ordenarSegund criterio . filter (not.criterio)) xs
```
```Bash
	(a-->a-->Bool)-->[a]-->[a]
```
## Conceptos
#### Transparencia referencial
Una expresión que es transparentemente referencial si podes reemplazarla por su valor sin afectar su resultado.
#### Sharing:
El uso de punteros apuntados a expresiones que son lo mismo para utilizarlas.
**Ejemplo**:
`let p = (3+1) in p*p`
#### Lazy Evaluation:
Solo analizo una expresión si es necesaria. De afuera hacia adentro.
**Ejemplos:**
`fst ("hola", div 1 0)`
No va a tirar error, ya que solo necesita el primero, ni mira el segundo.
`head . filter (>10) [1..]`
Esto no se rompe, ya que solo hará el filter (>10) de lo que se obtendrá en el head.
`head . filter (<0) [1..]`
Esto sí se rompe, ya que a nunca va a encontrar un numero filtrado que sea head (porque no va a existir tal número),
#### Anxious Evaluation:
Analizo la expresión de adentro hacia afuera.
**Ejemplos:**
`fst ("hola", div 1 0)`
Si va a tirar error, ya que procesa TODO, incluida la división por 0.
`head . filter (>10) [1..]`
Esto sí se rompe, ya que hará el filter (>10) de toda la lista y la lista es infinita.
## Función Take
```Haskell
	take _ [] = []
	take 0 _ = []
	take n (x:xs)=
	| n>0 = x:take(n-1) xs
```
## Trabajo Práctico
#### 1.
```Haskell
	mayor :: Ord a =>(b->a)->b->b->Bool
	mayor porDuracion x y = porDuracion x > porDuracion y
	ordenarSegun :: (a->a->Bool)->[a]->[a]
	ordenarSegun (mayor length) ["hola", "mundo"]
```
#### 2.
```Haskell
	ubicadoEn :: [Barrio]->Requisito
	ubicadoEn barrios = (`elem` barrios) . barrio
	ubicadoEn' barrios = flip elem barrios . barrio
```
```Haskell
	cumpleRango :: (Depto->Num)->Num->Num->Requisito
	cumpleRango funcion minimo maximo = between minimo maximo . funcion
```
#### 3.
```Haskell
	buscar :: Busqueda->(Depto->Depto->Bool)->[Depto]->[Depto]
	buscar busqueda criterioOrdenamiento =
	ordenarSegun criterioOrdenamiento . filter (cumpleBusqueda busqueda) 
```