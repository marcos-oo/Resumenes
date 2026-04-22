# Repaso
### Structs
```haskell
Data Alumno = unAlumno{
nombre :: String,
legajo :: Int,
especialidad :: String
}


Marcos :: Alumno
Marcos = unAlumno "Marcos" 2330064 "Sistemas"
```
### Aplicación Parcial:
> Pasarle a una función menos de los variables que necesita, haciendo que se transforme en una nueva función que toma los parámetros restantes.
#### Conjuntos:
**Vectores / Listas**: Conjuntos de elementos de un solo tipo (homogéneas) 
#### Take:
Si hago `:t Take`, me va a devolver `Number -> [a] -> [a]`.
Si hago `:t Take 2`, me va a devolver `[a] -> [a]`
### Pattern Matching
> Defino que tipos de  valores voy a retornar en base a que valores se introduzcan.

Como puedo hacer una función que me retorne si la letra que le di es una vocal?
```Haskell
esVocal :: Char->Bool
	esVocal "A" = False
	esVocal "E" = False
	esVocal "I" = False
	esVocal "O" = False
	esVocal "U" = False
	esVocal __ = True
```
Y si quiero una función que indique si una edad `esMayorDeEdad`?
### Guardas
```Haskell
esMayorDeEdad :: Int -> Bool
esMayorDeEdad x
	| x>18 = True
	| otherwise = False
```

Conviene esto? No necesariamente.

```haskell
esMayorDeEdad :: Int -> Bool
esMayorDeEdad x = x>17
```
### Tuplas:
> Estructura de datos compuesta or N elementos o coordenadas, pudiendo estar compuesta de cualquier combinación de tipos que se quisiese. Ejemplo:

<p align="center">{x , y , ... , z}<br>(Tipo 1, Tipo 2, ... , Tipo N)</p>

# Orden Superior:
### Parametrización:
Tenemos las siguientes funciones:
```Haskell
esMultiploDe3 x = x 'mod' 3 == 0
esMultiploDe5 x = x 'mod' 5 == 0
```
En que se diferencian? Técnicamente cumplen la misma función, solo que en base a distintos números.  Como podríamos resolverlo? **Parametrizando**.
#### Parametrizando con variables:
```Haskell
esMultiploDeN :: Int -> Int -> Bool
	idem x multiplo = x 'mod' multiplo==0
```
Permite crear una función que se adapte a mi situación, sin tener que crear una version distinta para, en este caso, el numero que desee.
#### Parametrizando con funciones
También podríamos pasar como parámetro **otra función**, haciendo que se vea así:
```Haskell
> t: Critero
> a -> Bool
> t: Filter
> [a] -> (a->Bool) -> [a]
```
Esto va a hacer que nunca tengamos que tocar la función `Filter`, pudiendo elegir el `Criterio` que yo quisiese,y si no anduviese el problema es del criterio mismo.
### Operaciones de listas:
- `Succ`: Retorna el sucesor del elemento de una lista.
- `Map`: Aplica una función a todos los elementos de una lista.
- `Sum`: Suma todos los elementos de una lista.
- `All`: Si todos los elementos de una lista cumple con una condición.
- `Any`; Si alguno de los elementos de una lista cumple con una condición.
- `Fold`: Se aplica una función sobre una lista en serie.`
<p align="center">fold(r / l)&emsp;(func.)&emsp;(start)&emsp;[list]</p>

**r / l** : indica si la operación se hará desde la izquierda (l) o desde la derecha (r).
**func.**: Indica cual es la función que se aplicara en serie sobre la lista,
**start.**: Un numero inicial, desde el cual se realizara el `fold`.
**list.**: Es la lista sobre la que se aplicará el `fold`. 