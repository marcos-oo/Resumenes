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
<div style="page-break-after: always;"></div>
## Conclusiones:
Los gráficos (Figura 1. Figura 2, Figura 3) y las explicaciones anteriores expresan algunas ideas que vale la pena aclarar:
1. Hay un intercambio entre la maquina y el eje. Sin embargo, como lo que se busca es ganar fuerza motriz, el intercambio termina siendo favorable para el eje.
2. El intercambio entre el eje y el motor es cíclico, expresado como un "bombeo" de energía $Motor\to Eje$ y $Eje\to Motor$ de forma alternante.
3. El ciclo térmico $A\to B\to C\to D$ coincide con un giro completo del eje (360º sexagesimales) dividido en dos giros de 180º cada uno.
$$(0º\implies A\to C\implies180º\implies C\to A\implies 360º)$$
4. Se puede ver que en la Expansión $(A\to C)$ el motor le entrega el trabajo $W_{AC}$ al eje, mientras que en la Compresión $(C\to A)$ el motor le recibe el trabajo $W_{CA}$ del eje. Es por esto que $W_{AC}>0$ y $W_{CA}<0$, ya que todo se ve desde dentro del sistema, el motor. En la creación de motores se busca siempre que 