### 5.0 Introducción
Un Lenguaje Formal es un conjunto de palabras que solo tienen una sintaxis, no tienen semántica. Los LF más simples son los Lenguajes Regulares (LR).
- Los LRs tienen gran importancia en el diseño de los Lenguajes de Programación (LP), que sus componentes básicos (tokens) constituyen diferentes LRs.
- Un lenguaje es un LR si puede ser generado por una Gramática Regular (GR).
### 5.1 Determinación de Lenguajes Regulares
Si un Lenguaje Formal (LF) es finito, entonces siempre es LR.
### 5.2 Las Expresiones Regulares
- La forma más precisa de representar a los LRs es mediante Expresiones Regulares (ER).
- Una ER es una expresión que describe el conjunto de cadenas que son palabras del LR representado por el ER.
- Las ERs se construyen usando los caracteres del alfabeto sobre el cual se define el LR, el símbolo $\LARGE\varepsilon$ (carácter vacío), algunos operadores especiales e incluso expresiones aritméticas.
#### 5.2.1 ERs para LRs finitos
Una ER para un LR finito se obtiene usando los caracteres del alfabeto, el símbolo $\LARGE\varepsilon$ y los operadores de concatenación y unión.
- Un carácter puede representar 3 elementos distintos:
	- Un símbolo de un alfabeto.
	- Una palabra de longitud 1.
	- Una ER.
	Esta ambigüedad es resuelta por el contexto en el cual se encuentra el carácter.
- El operador concatenación tiene mayor prioridad que el operador unión.
- La operación concatenación no es conmutativa.
- La operación unión sí es conmutativa.
- Dos ERs son equivalentes si representan el mismo LR.
##### 5.2.1.1 El operador potencia
Utilizado para simplificar la escritura, lectura y compresión de ciertas ERs.
#### 5.2.2 ERs para LRs infinitos
Los LRs infinitos tienen al menos 1 carácter o grupo de caracteres que se repite cierto numero de veces. Para representar estas repeticiones indeterminadas se utiliza el operados Clausura de Kleene.
- Su símbolo es un asterisco.
- Tiene mayor prioridad que los operaciones concatenación y unión.
- Representa a la palabra vacía y a todas las palabras que se forman con la repetir su operando un numero indeterminado de veces.
##### 5.2.1.1 El operador clausura positiva
El operador clausura positiva se utiliza para simplificar la escritura de ER. Elimina la existencia de la palabra vacía (a menos que esta pertenezca al lenguaje).
##### 5.2.1.2 La Expresión Regular Universal y su aplicación
La ERU es la ER que representa el Lenguaje Universal (LU) sobre un alfabeto dado. Osea, representa el LR que contiene la palabra vacía y todas las palabras que se pueden formar con caracteres del alfabeto dado.
- A cada ER le corresponde un único LR. Sin embargo, un LR puede ser representado por más de una ER.
### 5.3 Definición formal de las ERs
La ER original se construye utilizando solo los operadores básicos (unión, concatenación y clausura de Kleene) y se define formalmente de la siguiente manera recursiva:
- "$\large\varphi$", una ER que representa al LR vacío.
- "$\large\varepsilon$", una ER que representa al LR que solo contiene la palabra vacía.
- Todo carácter "x" corresponde a una ER "x", la cual representa un LR que solo tiene una palabra formada por ese carácter "x".
- Toda cadena "s" corresponde a una ER "s", la cual representa un LR que solo tiene una palabra formada por esa cadena "s".
A partir de estas cuatro reglas básicas, toda ER más compleja se construye así (definición formal):
- Si $R_1$ y $R_2$ son ERs, $R_1+R_2$ es una ER.
- Si $R_1$ y $R_2$ son ERs, $R_1\cdot R_2$ es una ER.
- Si $R_1$ es una ER, $R_1^*$ es una ER.
- Si $R_1$ es una ER, $(R_1)$ es una ER.
Esta definición se puede ampliar agregando los dos operadores:
- Si $R_1$ es una ER,  $R_1^+$ es una ER.
- Si $R_1$ es una ER, $R_1^n \ \ (con\ n\ge 0\ y\ entero)$ es una ER.
### 5.4 Operaciones sobre LRs y ERs correspondientes
Un LF es un LR si puede ser representado mediante una ER.
#### 5.4.1 Generalidades
Los LRs son cerrados bajo la unión, la concatenación, la clausura de Kleene, la clausura positiva, el complemento (con respecto al Lenguaje Universal (LU)) y la intersección.
#### 5.4.2 La unión
La unión de dos LRs es un LR que contiene todas las palabras pertenecientes a cualquiera de los dos LRs.
#### 5.4.3 La concatenación
La concatenación de dos LRs es un LR en el que cada palabra está formada por la concatenación de una palabra del primer LR con una palabra del segundo LR, similar a un producto cartesiano.
#### 5.4.3 La clausura de Kleene
La clausura de Kleene de un LR es un LR infinito (salvo en el caso que el LR está formado solo por la palabra vacía) formado por la palabra vacía, las palabras del LR y todas aquellas palabras que se obtienen concatenando las palabras del LR un numero arbitrario de veces.
#### 5.4.4 La clausura positiva
La clausura positiva de un LR es un LR infinito (salvo en el caso que el LR está formado solo por la palabra vacía) formado por las palabras del LR y todas aquellas palabras que se obtienen concatenando palabras de tal lenguaje un numero arbitrario de veces.
- La clausura positiva de un LR solo contiene a la vacía si ésta pertenece al LR original.
#### 5.4.5 El complemento
El complemento de un LR es un LR que está formado por todas las palabras que no pertenecen al LR original.
#### 5.4.6 La intersección
La intersección de dos LRs es un LR constituido por todas las palabras pertenecientes a ambos LRs.
### 5.5 ERs y LPs
Los componentes léxicos de un LP (identificadores, palabras reservadas, constantes, literales cadena, operadores, símbolos de puntuación) constituyen distintos LRs y, como tales, los podemos representar mediante LRs.
### 5.6 ERs extendidas
Las ERs también se emplean para representar los datos que serán procesados por diversas herramientas de software. **Lex** es una herramienta diseñada para ayudar a construir un analizador léxico, un módulo fundamental que posee todo compilador. Lex utiliza ERs para describir los patrones que debe encontrar y procesar.
#### 5.6.1 Un metalenguaje para ERs
Un metalenguaje es un lenguaje que se usa para describir otro lenguaje. El lenguaje que buscamos describir es el de las ERs, y el metalenguaje que se usará para describirlo tiene ciertos símbolos, además de operandos y operadores, llamados metacaracteres. El lenguaje de las ERs está formado por:
- Operandos: Caracteres del alfabeto que intervienen en la construcción de las ERs.
- Operadores:
	- Clausura de Kleene.
	- Concatenación.
	- Unión.
- Metacaracteres: Caracteres especiales que colaboran en la descripción de cada ER.
- Paréntesis: Caracteres utilizados para agrupar.
##### 5.6.1.1

| Metacaracteres<br>$\quad$operadores | Explicación                                                                  | Ejemplo                                                                  |
| ----------------------------------- | ---------------------------------------------------------------------------- | ------------------------------------------------------------------------ |
| $$.$$                               | Cualquier carácter, excepto el de nueva línea.                               | $a.a=$ toda cadena de caracteres cuyo primer<br>tercer carácter son $a$. |
| $$\|$$                              | Operador unión de ERs.                                                       | $ab\|b=ab+b$.                                                            |
| $$[]$$                              | Describe el conjunto de caracteres, simplifica el uso del operador unión.    | $[abx]=a+b+x$                                                            |
| $$[-]$$                             | Describe una clase de caracteres en 1 más intervalos.                        | $[a-d]=a+b+c+d$                                                          |
| $$\{\}$$                            | Operador potencia.                                                           | $a\{ 3\}=aaa$                                                            |
| $$\{\ ,\}$$                         | Operador potencia extendido a un intervalo.                                  | $a\{ 1,3\}=a+aa+aaa$                                                     |
| $$?$$                               | Operador que indica 0 o 1 ocurrencias de la ER que le precede.               | $a?=a+\varepsilon$                                                       |
| $$*$$                               | Operador clausura de Kleene: Cero o más ocurrencias de la ER que le precede. | $a*=a^*$                                                                 |
| $$+$$                               | Operador clausura positiva: Una o más ocurrencias de la ER que le precede.   | $a+=a^+$                                                                 |
| $$()$$                              | Utilizado para agrupar ERs.                                                  | $((ab)?\|b)+= (ab+ ε +b)+)$                                              |
