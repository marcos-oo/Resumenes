# 3. Sintaxis y BNF
### 3.0 Introducción
> Un Lenguaje de Programación (LP) es una notación utilizada para describir algoritmos y estructuras de datos que resuelven problemas computacionales.

Existe una relación muy importante entre los LPs y los Lenguajes Formales (LFs), ya que un LP está formado básicamente por un conjunto de Lenguajes Regulares (LRs) y un conjunto de Lenguajes Independientes de Contexto (LICs).
Las notaciones que describen de forma precisa la sintaxis de un LP se llaman BNF.
### 3.1 Introducción a la Sintaxis
Las **categorías léxicas** (o tokens) constituyen diferentes LRs. Pueden ser identificadores como las palabras reservadas, números enteros, números reales, caracteres, cadenas constantes, operadores o caracteres de puntuación. Algunos de estos lenguajes son finitos (como los operadores) y algunos infinitos (como los números enteros, identificadores, números reales).
Las **categorías sintácticas** son las expresiones y las sentencias de un LP, y son usualmente LICs. Estos lenguajes requieren ser generados por Gramáticas Independientes de Contexto (GICs), no por Gramáticas Regulares (GRs) ni por Gramáticas Quasi-Regulares (GQRs).
- Todos estos tipos de gramáticas se caracterizan por tener un único *no terminal* del lado izquierdo.
- Una GF no sólo genera un LF, sino que también puede describir la sintaxis del LF que genera.
### 3.2 Identificadores y su Sintaxis
Un identificador es una cadena de uno o más caracteres que llaman a distintas entidades de un LP, sean variables, funciones, procedimientos, constantes, tipos, etc. Construyen un LR infinito.
Las palabras reservadas habitualmente forman un LR finito, independiente de los identificadores.
- Todo *no terminal* debe aparecer en el lado izquierdo de al menos una producción.
- Un *terminal* jamás puede aparecer en el lado izquierdo de una producción.
- 