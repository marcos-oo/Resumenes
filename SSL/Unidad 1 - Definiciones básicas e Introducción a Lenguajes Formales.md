## 1.1 Lenguajes:
#### 1.1.1 Lenguaje natural:
- Alta ambigüedad, dependiendo del contexto y el emisor.
- Evolución dinámica, mutando en conjunto con la sociedad, incorporando nuevos términos y reglas gramaticales para mejorar la comunicación..
- La semántica es capaz de rescatar errores sintácticos, ya que la semántica de cada palabra y oración es mas importante que la composición sintáctica.
- Sus reglas gramaticales surgen después de la creación del lenguaje para poder explicar su estructura (sintaxis).
#### 1.1.2 Lenguaje formal:
- Ambigüedad nula, estricto y determinista.
- Evolución estática, las reglas son inmutables.
- La sintaxis es fija, al errar se pierde de forma irrecuperable el significado.
## 1.2 Terminología:
- **Carácter**: Elemento básico de construcción del lenguaje, indivisible.
- **Alfabeto (Σ)**: Conjunto finito de caracteres.
- **Cadena**: Secuencia finita de caracteres, no precisa tener un significado.
	*Propiedades de las cadenas*:
	- **Longitud de cadena ( |S| )**:  Es la cantidad de caracteres que la componen.
	- **Cadena vacía (ε)**: Una cadena que no contiene ningún carácter, similar al conjunto vacío en teoría de conjuntos.
	- **Potenciación**: a<sup>5</sup>b<sup>8</sup> = "aaaaabbbbbbbb".
	- **Concatenación**: Une dos cadenas formando una nueva. NO CONMUTATIVA (a excepción de S.ε = ε.S = S).
	- **Afijos**: Secuencia de 0 o mas caracteres iniciales o finales de una cadena.
		- Cadena: Hola!
		- Prefijos: (ε, H, Ho, Hol, Hola, Hola!)
		- Sufijos: (ε, !, a! la!, ola!, Hola!)
	- **Subcadena**: Secuencia de caracteres que se obtiene eliminando 0 o mas caracteres iniciales y/o finales de una cadena.
		- Cadena: Hola
		- Subcadenas: (Hola, ola, la, a, Hol, Ho, H, ol, o, l, ε).
- **Lenguaje Universal (Σ*)**: Basándose en un "**Σ"**, es un lenguaje *infinito* que contiene todas las cadenas que se pueden formar con los caracteres de **"Σ"**, incluyendo **"ε"**.
- **Lenguaje Formal:** Subconjunto del **"Σ*"**, compuesto únicamente por las cadenas que cumplen las reglas que las transforman en palabras.
- **Palabra**: Cadena que pertenece a un **lenguaje formal**, con significado y uso.
## 1.3 Análisis:
Tenemos la siguiente oración:
<p align="center"><i>Buela baca la</i></p>

#### 1.3.1 Análisis léxico
Las palabras están escritas incorrectamente. Lo corregimos, queda así:
<p align="center"><i>Vuela vaca la</i></p>

#### 1.3.2 Análisis sintáctico
Las palabras están ordenadas incorrectamente. Lo corregimos, queda así:
<p align="center"><i>La vaca vuela</i></p>

#### 1.3.3 Análisis semántico
La oración no tiene sentido. Lo corregimos, queda así:
<p align="center"><i>La vaca no vuela</i></p>
