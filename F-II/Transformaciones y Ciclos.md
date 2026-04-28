## Terminología:
**Sustancia / Sistema:**
- **Calor Especifico** ($C$): Propiedad intrínseca, las calorías necesarias para elevar una unidad determinada de masa de una sustancia por 1ºK (usualmente 1g).
- **Capacidad Calorífica** ($\mathbb{C}$): Propiedad de un sistema, las calorías necesarias para elevar su totalidad por 1ºK.
- **Capacitancia Térmica** ($\mathbb{C}$): Equivalente a Capacidad Calorífica.
**Molar:**
- **Calor Especifico Molar** ($C_M$): Propiedad intrínseca, las calorías necesarias para elevar mol de una sustancia por 1ºK.
- **Capacidad Calorífica Molar**  ($C_M$): Equivalente a Calor Especifico Molar.
- **Capacitancia Térmica Molar**  ($C_M$): Equivalente a Calor Especifico Molar.
## Calculo del Calor Específico Molar:
### Transformación Isocora:
Se traba el embolo, volumen constante, $W=0$.
$$Q=\Delta U+W\qquad\wedge\qquad W=0\qquad\implies\qquad Q=\Delta U$$
###### Calculo de $Q$:
Dado que:
$$\mathbb{C}=C.M=n.C_M$$
$$Q=\mathbb{C}.\Delta T$$
Entonces:
$$Q=n.C_M.\Delta T=n.C_V.\Delta T$$
(Le llamamos $C_V$ para aclarar que el volumen es constante, es lo que va a la temperatura del sistema).
###### Calculo de $\Delta U$:
Dado que:
$$U=\dfrac{3}{2}\cdot n\cdot R\cdot T$$
Entonces:
$$\Delta U\quad=\quad\Delta(\dfrac{3}{2}\cdot n\cdot R\cdot T)\quad=\quad\dfrac{3}{2}\cdot n\cdot R\cdot\Delta T$$
###### Despeje:
Igualando:
$$n.C_V.\Delta T\quad=\quad\dfrac{3}{2}\cdot n\cdot R\cdot\Delta T$$
Entonces:
$$ \LARGE C_V=\dfrac{3}{2}R$$
Siendo $C_V$ el Calor Especifico Molar, el cual multiplicado por $n$ nos daría la capacitancia térmica de todo el gas dentro del sistema ($\huge \mathbb{C}_v$).
> Si, el **calor especifico MOLAR** de todos los gases ideales monoatómicos es $\dfrac{3}{2}R$, **siempre que no cambie el volumen**.
### Transformación Isobárica:
Se libera el embolo, presión constante, $F=cte$, $W\neq 0$
Se sabe que:
$$Q=\Delta U+W$$
Y que:
$$\mathbb{C}_{in}=n \cdot C_V + \mathbb{C}_W $$
Siendo $C_W$ la capacitancia térmica asociada al trabajo mecánico, $n\cdot C_V$ la asociada al cambio de energía interna y $\mathbb{C}_{in}$ la capacitancia térmica del total de lo que se haga en el sistema.

> $\mathbb{C}_W$ es algo que me costo entender conceptualmente, pero se puede explicar como la energía que el sistema invierte en expandirse (en vez de calentarse) por un grado de temperatura. Multiplicarlo por $\Delta T$ nos daría el total de la energía gastada en trabajo. 

###### Cálculo de $\mathbb{C}_W$:
Sabiendo que:
$$\mathbb{C}_W\cdot\Delta T = W$$
Que para presiones constantes:
$$P\cdot\Delta V = W$$
Y que:
$$P\cdot\Delta V = n\cdot R\cdot\Delta T$$
Entonces:
$$\mathbb{C}_W=\dfrac{W}{\Delta T}=\dfrac{P\cdot\Delta V}{\Delta T}=\dfrac{n\cdot R\cdot\Delta T}{\Delta T}$$
Y:
$$\LARGE \mathbb{C}_W=n\cdot R$$
###### Cálculo de $C_p$:
Sabiendo que:
$$\mathbb{C}_{in}=n\cdot C_V+\mathbb{C}_W=n\cdot\dfrac{3}{2}R+n\cdot R=n\cdot\dfrac{5}{2}\cdot R$$
Entonces:
$$\large\dfrac{\mathbb{C}_{in}}{n}=\dfrac{5}{2}R=C_p$$
Siendo $C_p$ el ***calor especifico molar*** a presión constante. Puede multiplicarse por el $n$ y $\Delta T$ para obtener todas las calorías que se transfieren / quitan al sistema, ya que tiene en cuenta la variación en energía interna y trabajo mecánico.
##### Relación de Mayer:
Partiendo de:
$$\mathbb{C}_{in}=n\cdot C_V+\mathbb{C}_{W}$$
Obtenemos:
$$n\cdot C_p=n\cdot C_V+n\cdot R$$
$$C_p=C_V+R$$
Y de ahí la llamada **Relación de Mayer**:
$$C_p-C_V=R$$
## Otras transformaciones:
### Transformación Isotérmica
Sabemos que:
$$P\cdot V=n\cdot R\cdot T$$
Si la variación de temperatura es 0 (**iso** del griego "igual", **térmica** de la temperatura), la variación del lado derecho de la formula es 0, y así debe ser el lado izquierdo. Pero si hay una transformación, **ni $P$ ni $V$ pueden ser constantes por si mismas**. Es por esto que podemos concluir que:
$$n\cdot R\cdot\Delta T =0=\Delta(P\cdot V) \implies$$
$$\large P_{inicial}\cdot V_{inicial}=P_{final}\cdot V_{final}\qquad[1]$$
###### Cálculo de $W$:
No podemos obtener el trabajo tan fácil, ya que $P\cdot\Delta V = W$ no aplica por no ser constante la presión.
Sabemos que el trabajo mecánico que realiza el gas es el espacio bajo la curva de $P(V)$. Ese espacio puede obtenerse, como no, con una integral. 
$$\large \int_{V_A}^{V_B} P_{final} \cdot dV_{final}$$
Podemos llevar la integral a una sola variable haciendo un reemplazo usando $[1]$.
$$\large\int_{V_A}^{V_B}\dfrac{P_{inicial}\cdot V_{inicial}}{V_{final}} \cdot dV_{final}$$
como conocemos $P_{inicial}$ y $V_{inicial}$, las podemos sacar afuera como constantes
$$\large P_{inicial}\cdot V_{inicial}\int_{V_A}^{V_A}\dfrac{1}{V} \cdot dV$$
Y esto es una integral fácil de resolver.
$$\large P_{inicial}\cdot V_{inicial}\cdot ln(V)\Bigg|_{V_A}^{V_B}$$
Resultando en:
$$\large P_{inicial}\cdot V_{inicial}\cdot ln\left(\dfrac{V_B}{V_A}\right)$$
###### Cálculo de $Q$:
Como bien indica el titulo, la transformación es **isotérmica**, por lo que se da que:
$$\large \Delta T=0\implies \Delta U=0$$
Entonces:
$$\large Q=W$$
