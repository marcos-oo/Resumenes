## 2.1 Gramáticas Formales:
> Conjunto de reglas (PRODUCCIONES) que se aplican para obtener las palabras del Lenguaje Formal que genera la Gramática Formal en cuestión.
#### 2.1.1 Composición:
<p align="center">G = ( V<sub>n</sub> ; V<sub>t</sub> ; P ; S )</p>


*Referencias:*
- V<sub>n</sub> : Vocabulario o alfabeto de no terminales.
- V<sub>t</sub> : Vocabulario o alfabeto de terminales.
- P : Producciones.
- S : Símbolo o variable inicial.

*Requisitos:*
- V<sub>n</sub> y V<sub>t</sub> son conjuntos finitos.
- V<sub>n</sub> ∩ V<sub>t</sub> = ∅
- P es finito, y P⊂( V<sup>+</sup> - V<sub>t</sub><sup>*</sup> ) X V<sup>*</sup> , siendo V = V<sub>n</sub> ∪ V<sub>t</sub> .
- S pertenece a V<sub>n</sub> .
#### 2.1.2 Producciones:
Se construyen haciendo uso de Productores (también conocidos como variables), los símbolos que componen al "Σ" del lenguaje y metasímbolos como -> o como | .
*Ejemplo:*

<p align="center">G = ( { S, X, Y } ; { 0 , 1 } ; P ; S )</p>

*Siendo P:*

<p align="center">S ⟹ 0S | 10X<br>X ⟹ 1X | 0Y <br> Y ⟹ 0</p>

*Traducido:* 
- S se puede reemplazar por 0S o por 10X.
- X se puede reemplazar por 1X o por 0y.
- Y se puede reemplazar por 0.
#### 2.1.3 De la gramática al lenguaje
1. Se comienza en el símbolo o variable inicial.
2. Se aplican producciones hasta obtener solamente elementos terminales, las letras del "Σ" del lenguaje.
Este proceso se conoce como **DERIVACIÓN**.
*Ejercicio:*
<p align="center">G = ( { S, T, Q } ; { a , b } ; P ; S )</p>
*Siendo P:*
<p align="center">S ⟹ aT | bQ<br>T ⟹ a | b <br> Q ⟹ a | ε</p>

**a)** Puedo crear la cadena *bab*?
**b)** Que lenguaje se genera?
<details>
  <summary><b>Solución:</b></summary>
  
  a) No.<br>b)
<p align="center">L ={aa, ab, ba, b}</p>
  
</details> 


## 2.2 La Jerarquía de Chomsky:
> Esta Jerarquía de Chomsky establece una clasificación de cuatro tipos de Gramáticas Formales que, a su vez, generan cuatro tipos diferentes de Lenguajes Formales.

```mermaid
flowchart TD
    A[Gramáticas Formales]
    A --> |Tipo 3| B[Gramática Regular] --> F[Lenguaje Regular]
    A --> |Tipo 2| C[Gramática Independiente del Contexto] --> G[Lenguaje Independiente del Contexto]
    A --> |Tipo 1| D[Gramática Sensible al Contexto] --> H[Lenguaje Sensible al Contexto]
    A --> |Tipo 0| E[Gramática Irrestricta] --> I[Lenguaje Irrestricto]
```
Las gramáticas no son entidades separadas, si no que están contenidas dentro de las otras.
![[Jerarquia-De-Chomsky.png]]

#### 2.2.1 Gramática regular:
```mermaid
flowchart TD
    A[Gramatica Regular]
    B[lado izquierdo]
    C[lado derecho]
    A-->|el|B
    A-->|el|C
    D(no-terminal)
    E(terminal)
    F(terminal)
    G(no-terminal)
    H(no-terminal)
    I(terminal)
    J{épsilon}
    B-->|debe tener un solo|D
    C-->|debe estar formado por un|E
    C-->|o por un|F-->|seguido de un|G
    C-->|o un|H-->|seguido de un|I
    C-->|o incluso un|J
    
    
```
#### 2.2.2 Gramática Independiente de Contexto:
```mermaid
flowchart TD
    A[Gramatica Independiente de Contexto]
    B[lado izquierdo]
    C[lado derecho]
    A-->|el|B
    A-->|el|C
    D(no-terminal)
    E{irrestricto}
    B-->|debe tener un solo|D
    C-->|es|E
    
```
#### 2.2.3 Gramática Sensible al Contexto:
<p align="center"><b>a ⟹ b&emsp;⇔&emsp;|b| ≥ |a|</b></p>
#### 2.2.4 Gramática Irrestricta:
Pueden existir secuencias de no-terminales y/o terminales, con α ≠ ε

#### EXTRA 1: Ayuda-memoria:

```mermaid
flowchart TD
	A[La Derecha es mayor o igual que la izquierda.]
	B[La izquierda está compuesta por solo no-terminal]
	C[La derecha tiene la forma aB / Ba / a / epsilon]
	GR(Es Gramatica Regular)
	GSC(Es Gramatica Sensible al Contexto)
	GIC(Es Gramatica Independiente del Contexto)
	GI(Es Gramatica Irrestricta)
	A-->|SÍ|B-->|SÍ|C-->|SÍ|GR
	A-->|NO|GI
	B-->|NO|GIC
	C-->|NO|GSC
```
