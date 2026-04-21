## Introducción a Sintaxis y Semántica de los Lenguajes
#### Conceptos iniciales:
###### Lenguaje natural:
- Alta ambigüedad, dependiendo del contexto y el emisor.
- Evolución dinámica, mutando en conjunto con la sociedad, incorporando nuevos términos y reglas gramaticales para mejorar la comunicación..
- La semántica es capaz de rescatar errores sintácticos, ya que la semántica de cada palabra y oración es mas importante que la composición sintáctica.
- Sus reglas gramaticales surgen después de la creación del lenguaje para poder explicar su estructura (sintaxis).
###### Lenguaje formal:
- Ambigüedad nula, estricto y determinista.
- Evolución estática, las reglas son inmutables.
- La sintaxis es fija, al errar se pierde de forma irrecuperable el significado.
#### Terminología:
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
#### Tipos de análisis:
Tenemos la siguiente oración: *buela baca la*
- Análisis Léxico: Las palabras están escritas incorrectamente. *Vuela vaca la*.
- Análisis Sintáctico: Las palabras están ordenadas incorrectamente. *La vaca vuela.*
- Análisis Semántico: La oración no tiene sentido. *La vaca NO vuela.*