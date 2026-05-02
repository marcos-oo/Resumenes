## Rendimiento de una Maquina Térmica
Convertir Trabajo en Calor es fácil, convertir Calor en Trabajo no tanto. Las maquinas o motores térmicos son dispositivos a los que se les entrega un calor $Q_1$ y a cambio se obtiene un trabajo $W$. 
De acuerdo con el $2^{do}$ principio de la termodinámica sabemos que:
$$\large Q_1>W$$
Es decir que no todo el calor que se le entrega a la maquina en un ciclo de trabajo se convierte en trabajo mecánico. Ademas del $W$, la maquina devuelve una cantidad de calor $Q_2$ desaprovechada.
Por el $1^{er}$ principio, sabemos que:
$$Q_1=Q_2+W\implies Q_1-Q_2=W\quad[1]$$
Ademas, podemos definir lo siguiente:
$$\eta\cdot W=Q_1\quad[2]$$
Ya que el trabajo representa una fracción del total de calorías entregadas al sistema.
A esta fracción $\large\eta$ se la conoce como **rendimiento**. Lo calculamos usando $[1]$ y $[2]$:
$$\eta=\dfrac{W}{Q_1}=\dfrac{Q_1-Q_2}{Q_1}=1-\dfrac{Q_2}{Q_1}$$
En resumen, el $2^{do}$ principio puede expresarse de las siguientes maneras:
$$1)\quad Q_1>W$$
$$2)\quad Q_2>0$$
$$3)\quad \eta>0$$
> Todo esto sucede desde un punto de vista MACRO, luego se verá en detalle cuando pueden suceder estas pérdidas.
## Ciclo de Carnot:
Sadi Carnot *(Francia, 1796)* concibió lo que se conoce como un **ciclo de máximo rendimiento**. Incluso a pesar de eso, se mantiene que $\eta<1$. Para realizar este ciclo, el fluido recorre de forma ordenada las siguientes evoluciones:
### 1)  Expansión Isotérmica a Temperatura $T_1$ caliente. $\quad[A\to B]$
El gas empuja el piston realizando un trabajo $W_{A\to B}$, haciendo uso de la energía $Q_1$ (carga térmica) proveniente de la fuente caliente $T_1$, pero manteniendo la temperatura del sistema constante.
$$\Delta U=0J\quad\implies\quad W_{A\to B}=Q_1$$
Siendo $Q_1$ la cantidad de calor absorbida de la fuente caliente $T_1$, la cual se obtiene haciendo el ya visto calculo para transformaciones isotérmicas:
$$Q_1=\int_{V_1}^{V_2}P\cdot dV=\int_{V_1}^{V_2}\dfrac{n\cdot R\cdot T_1}{V}\cdot dV=n\cdot R\cdot T_1\cdot ln\left(\dfrac{V_2}{V_1}\right)$$
$$\large Q_1=n\cdot R\cdot T_1\cdot ln\left(\dfrac{V_2}{V_1}\right)=W_{A\to B}$$
### 2)  Expansión Adiabática, enfriamiento. $\quad[B\to C]$
El gas empuja el piston realizando un trabajo $W$, haciendo uso ahora de su energía interna, por lo que:
$$\Delta U<0$$
Ademas, al ser una transformación adiabática, no hay intercambio de calor entre el sistema y el entorno es 0, por lo que a partir del $1^{er}$ principio de la termodinámica podemos inferir que:
$$Q=0\implies W_{B\to C}+\Delta U = 0 \implies$$
$$\large W_{B\to C}=-\Delta U$$
### 3)  Compresión Isotérmica a Temperatura $T_2$ fría. $\quad[C\to D]$
Un agente externo empuja el piston realizando un trabajo $W_{C\to D}$, haciendo uso de la energía $Q_2$ (carga térmica) que se le entrega a la fuente fría $T_2$, pero manteniendo la temperatura del sistema constante. Aplican las fórmulas usadas en $A\to B$:
$$\Delta U=0J\quad\implies\quad W_{C\to D}=Q_2$$
$$Q_2=\int_{V_3}^{V_4}P\cdot dV=\int_{V_3}^{V_4}\dfrac{n\cdot R\cdot T_2}{V}\cdot dV=n\cdot R\cdot T_2\cdot ln\left(\dfrac{V_4}{V_3}\right)$$
$$\large Q_2=n\cdot R\cdot T_2\cdot ln\left(\dfrac{V_4}{V_3}\right)=W_{C\to D}$$
### 4)  Compresión Adiabática, calentamiento. $\quad[D\to A]$
Un agente externo empuja el piston realizando un trabajo $W$, aumentando la energía interna (y temperatura, claro) del gas, por lo que:
$$\Delta U<0$$
Y el resto se comporta como la fase 2:
$$Q=0\implies W_{D\to A}+\Delta U = 0 \implies$$$$\large W_{D\to A}=-\Delta U$$
### Conclusiones:
Los gráficos (Figura 1. Figura 2, Figura 3) y las explicaciones anteriores expresan algunas ideas que vale la pena aclarar:
1. Hay un intercambio entre la maquina y el eje. Sin embargo, como lo que se busca es ganar fuerza motriz, el intercambio termina siendo favorable para el eje.
2. El intercambio entre el eje y el motor es cíclico, expresado como un "bombeo" de energía $Motor\to Eje$ y $Eje\to Motor$ de forma alternante.
3. El ciclo térmico $A\to B\to C\to D$ coincide con un giro completo del eje (360º sexagesimales) dividido en dos giros de 180º cada uno.
$$(0º\implies A\to C\implies180º\implies C\to A\implies 360º)$$
4. Se puede ver que en la Expansión $(A\to C)$ el motor le entrega el trabajo $W_{AC}$ al eje, mientras que en la Compresión $(C\to A)$ el motor le recibe el trabajo $W_{CA}$ del eje. Es por esto que $W_{AC}>0$ y $W_{CA}<0$, ya que todo se ve desde dentro del sistema, el motor.
	En la creación de motores se busca siempre que el trabajo entregado al eje ($W_{A\to C}$) sea mayor al entregado al motor ($W_{C\to A}$). Esto se debe a que el calculo final del rendimiento se hace de la siguiente forma:
	$$\eta=\dfrac{W}{Q_1}=\dfrac{W_{A\to C}-W_{C\to A}}{Q_1}$$
5. El trabajo del motor sobre el eje es una suma de dos, $W_{A\to B}+W_{B\to C}$. 
	$W_{A\to B}$: Trabajo del motor sobre el eje realizado con energía extraída de la fuente caliente. El gas no aporta energía en este tramo, por lo que su energía interna permanece constante y así su temperatura.
$$Q_{AB}=W_{A\to B}>0\quad\wedge\quad\Delta U=0\quad\land\quad\Delta T=0$$
	$W_{B\to C}$: Trabajo del motor sobre el eje realizado con la energía interna del gas. Como el gas aporta energía en este tramo, su energía interna baja y así su temperatura.
$$-\Delta U_{BC}=W_{B\to C}>0\quad\wedge\quad\Delta U<0\quad\land\quad\Delta T<0$$
6. El trabajo del eje sobre el motor es una suma de dos, $W_{C\to D}+W_{D\to A}$. 
	$W_{C\to D}$: Trabajo del eje sobre el motor realizado con energía dirigida a la fuente ahora fría. El gas no acumula energía en este tramo, por lo que su energía interna permanece constante y así su temperatura.
$$Q_{CD}=W_{C\to D}<0\quad\wedge\quad\Delta U=0\quad\land\quad\Delta T=0$$
	Ademas, como el eje entrega energía a la compresión del gas del motor, tiende a frenarse, perdiendo energía. Luego veremos que aquí se da el motivo de $\eta<1$.
	
	$W_{D\to A}$: Trabajo del eje sobre el motor realizado con energía dirigida al gas. El gas retiene energía en este tramo, por lo que su energía interna aumenta y así su temperatura.
$$-\Delta U_{DA}=W_{D\to A}<0\quad\wedge\quad\Delta U>0\quad\land\quad\Delta T>0$$
	Es luego de esta etapa que se llega a la etapa $A$, en la que la temperatura es caliente.
1. El saldo de ambas transformaciones **adiabáticas** es nulo. $\left|W_{BC}\right|=\left|W_{DA}\right|$ , ya que $\left|T_2-T_1\right|$ es idéntico para ambos procesos $\quad\implies\quad \left|\Delta U_{BC}\right|=\left|\Delta U_{DA}\right|$ . Al ser $Q_{BC}=Q_{DA}=0$, el intercambio de energía en el ciclo es nulo$\quad\implies\quad W_{BC}-W_{DA}=0$. 
2. El saldo de ambas transformaciones **isotérmicas** NO es nulo. El balance energético en el ciclo completo será $W_{AB}-W_{CD}$ ya que como vimos antes, $W_{BC}-W_{DA}=0$, así que en la ecuación final "se cancelan".
3. Rendimiento $\equiv\eta$
$$\eta=\dfrac{Trabajo\ neto\ sobre\ el\ eje}{Energía\ aportada\ por\ la\ fuente\ caliente}=\dfrac{W_{AB}-W_{CD}}{W_{AB}}$$
$$\large \eta=1-\dfrac{W_{CD}}{W_{AB}}$$
4. Es lograble el $\eta=1$?
	Para que así fuese $W_{CD}$ debería ser $0$ en la expresión anterior. $W_{CD}=0$ significa, físicamente, que el embolo comprime el gas sin que el gas oponga resistencia alguna. $W_{CD}=0$ también significa que el eje gira sin oposición alguna (no se frena) durante la transformación isotérmica fría.
	**Caso ideal ($\eta=1$):**
	Para que el embolo se desplace libremente en el cilindro, sin la oposición del gas, deberá suceder que la presión del gas sea 0.
	$$W_{CD}=\int_{V_C}^{V_D}P\cdot dV=\int_{V_C}^{V_D}0\cdot dV=0$$
	Un gas confinado en un sistema no ejerce presión sobre las paredes de su recipiente de volumen $V$ siempre que su $T=0$, ya que:
$$P\cdot V=n\cdot R\cdot T\ \wedge \ T=0\implies P=0$$
	Es decir, sus partículas están des-energizadas, por lo que no golpean las paredes del recipiente que lo contiene. Visto de forma gráfica, en el gráfico P(V), el area bajo la curva es 0, al igual que $W_{CD}$.
	**Impedimentos para que suceda $\eta=1$**
	1. El cero absoluto (0ºK) no ha sido alcanzado ni en los mas completos laboratorios, en un motor no se va a dar.
	2. Incluso aunque el cero absoluto fuese posible, en la realidad no habría energía cero a 0ºK, ya que la idea de que las moléculas tienen velocidad 0 a e 0ºK no es estrictamente correcta. La energía molecular (y por lo tanto la presión) no pasa de un valor mínimo llamado **energía de punto cero**, cuyo valor no es cero. Al existir un mínimo de presión jamás lograremos un $W_{CD}=0$, y por lo tanto, tampoco lograremos un $\eta=0$.
### Rendimiento en función de la temperatura de las fuentes
Partimos de:
$$\eta=\dfrac{Q_1-Q_2}{Q_1}=1-\dfrac{Q_2}{Q_1}$$
Calculamos $Q_1$/$Q_2$:
$$A\to B\quad:\quad Q_1=W_{AB}=n\cdot R\cdot T_1\cdot ln\left(\dfrac{V_2}{V_1}\right)$$
$$C\to D\quad:\quad Q_2=W_{CD}=n\cdot R\cdot T_2\cdot ln\left(\dfrac{V_4}{V_3}\right)$$
Hacemos el cociente $Q_2$/$Q_1$, usando el modulo de $Q_2$ porque el rendimiento nos quedaría negativo siendo $V_4<V_3$.
$$\dfrac{\left|Q_2\right|}{Q_1}\ =\ \dfrac{T_1}{T_2}\cdot \dfrac{ln\left(\dfrac{V_3}{V_4}\right)}{ln\left(\dfrac{V_2}{V_1}\right)}\qquad[1]$$
También sabemos que para evoluciones isotérmicas:
$$P_1\cdot V_1=P_2\cdot V_2$$
$$P_3\cdot V_3=P_4\cdot V_4$$
Y para las adiabáticas:
$$P_2\cdot V_2^\gamma=P_3\cdot V_3^\gamma$$
$$P_4\cdot V_4^\gamma=P_1\cdot V_1^\gamma$$
Haciendo el producto miembro a miembro:
$$P_1\cdot P_2\cdot P_3\cdot P_4\cdot V_1\cdot V_3\cdot V_2^\gamma\cdot V_4^\gamma\quad=\quad P_1\cdot P_2\cdot P_3\cdot P_4\cdot V_2\cdot V_4\cdot V_1^\gamma\cdot V_3^\gamma$$
Simplificando:
$$\left(V_2\cdot V_4\right)^\gamma=\left(V_3\cdot V_1\right)^\gamma\implies\dfrac{V_2}{V_1}=\dfrac{V_3}{V_4}$$
Esa última fórmula se parece bastante a $[1]$. Si reemplazamos la fracción de limites se hace 1, el neutro de la multiplicación.
$$\dfrac{Q_2}{Q_1}=\dfrac{T_2}{T_1}$$
Por lo que podemos expresar el rendimiento como:
$$\large\eta=1-\dfrac{T_2}{T_1}$$

## El Refrigerador
El refrigerador que se analizará es en realidad un calentador que como efecto secundario enfría. Si recorremos el Ciclo de Carnot en el sentido contrario, se producirá una reversion de todos los flujos de energía que vimos antes, $|Q|=Q_1-Q_2$. EL eje hará trabajo sobre la maquina, tal que las fuentes cambian su temperatura.
- La fuente caliente se calienta cada vez más.
- La fuente fría se enfría cada vez más.
La capacitancia térmica de las fuentes debe ser alta (en comparación a la del gas), ya que queremos que sus temperaturas sigan aumentando (o decreciendo), sin que vuelvan a temperatura ambiente siempre que no están activamente siendo afectados por el proceso del motor.
#### Eficiencia Frigorífica ($\Large\varepsilon\normalsize$):
$$\Large\varepsilon\normalsize=\dfrac{Q_2}{W}=\dfrac{Q_1-W}{W}=\dfrac{Q_1}{W}-1\implies$$
$$\Large\varepsilon\normalsize=\dfrac{1}{\dfrac{W}{Q_1}}-1=\dfrac{1}{\eta}-1\qquad[1]$$
$$\eta=1-\dfrac{T_2}{T_1}=\dfrac{T_1-T_2}{T_1}\qquad[2]$$
Usando $[1]$ y $[2]$:
$$\Large\varepsilon\normalsize\quad=\quad\dfrac{T_2}{T_1-T_2}\quad=\quad\dfrac{1}{\eta}-1$$
Y además:
$$\eta=\dfrac{1}{\Large\varepsilon\normalsize+1}$$