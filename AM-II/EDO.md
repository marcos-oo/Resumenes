Una Ecuación Diferencial es una función en la que la incógnita no es un número, si no una función incógnita. Participan también sus consecutivas derivadas e incluye finalmente la variable independiente.
Las funciones de una sola variable de ahora en más son $\large y$, básicamente variables *dependientes*.
El grupo que veremos de **ED**s, en el que participan
$$y,\ y',\ y''\ ,\ ...\ x$$

se llama **Ecuaciones Diferenciales Ordinarias** (EDO). Por ejemplo
$$y'+2y=3x\qquad 1^{er}\ orden$$
o también
$$3y''+8y+\dfrac1 2 y'=0\qquad 2^{do}\ orden$$

En esta unidad se verán algunos de los distintos tipos de **EDO**.

Se le llama **orden** de la EDO es el orden de la mayor derivada que aparezca en la ecuación.

Se le llama **solución** de la EDO a toda función $\rho (x)$, derivable por lo menos hasta el orden de la EDO, que la satisfaga.

Se le llama **solución general** (SG) de la EDO a toda solución que dependa de **n** constantes esenciales, siendo **n** el orden de la EDO. De la SG se forma la familia **n**-paramétrica.

Se le llama **solución particular** (SP) de la EDO al valor representado por la SG al fijar **n** condiciones que otorguen valores a sus **n** constantes.

## EDO de variables separables
Se le llama **ecuación diferencial de variables separables** a la que es de forma
$$f(y)\cdot y'+g(x)=0$$
con $f(x)$ y $g(x)$ continuas.
De forma simplificada, es una ecuación diferencial en la que puedo separar las $x$ de un lado y las $y$ del otro.
##### Ejemplo 1:
$$
\begin{aligned}
y' - y &= 0 & \qquad \ln y &= x + K \\[2ex]
\frac{dy}{dx} - y &= 0 & \qquad e^{\ln y} &= e^{x+K} \\[2ex]
\frac{dy}{dx} &= y & \qquad y &= C \cdot e^x, \quad C \in \mathbb{R}_{>0} \\[2ex]
\frac{dy}{y} &= dx & \qquad y' &= C \cdot e^x, \quad C \in \mathbb{R}_{>0} \\[2ex]
\int \frac{1}{y} dy &= \int dx & \qquad y' - y &= C \cdot e^x - C \cdot e^x = 0
\end{aligned}
$$


Esta es una SG, ya que el orden de la EDO es 1 y la solución depende de 1 constante esencial.
Si se establece la condición
$$
\begin{cases}
y' - y = 0 \\
y(0) = 1
\end{cases}
$$

La solución pasa a ser una SP
$$1=C\cdot e^0\quad\implies\quad C=1$$
$$\large y=e^x$$

¿pero que hago si no puedo separar las variables?
## EDO homogénea (no entra en la teoría, batenme)
Se le llama **función homogénea** de grado **n** a toda función de dos variables $g(x,y)$ para la que se cumple
$$g(tx,ty)=t^n\cdot g(x,y)$$

con $t$ pudiendo estar restringido.
##### Ejemplo 2:
$$g(x,y)=x^2+x\cdot y$$
$$g(tx,ty)=(t\cdot x)^2+t^2\cdot x\cdot y$$
$$g(tx,ty)=t^2\cdot x^2+t^2\cdot x\cdot y$$
$$g(tx,ty)=t^2\cdot \left(x^2+x\cdot y\right)=t^2\cdot g(x,y)$$

Resulta entonces que $g(x,y)$ es homogénea de grado 2.

Se le llama **ecuación diferencial homogénea** a la que puede escribirse
$$M(x,y)\ dx+N(x,y)\ dy=0$$

con $M(x,y)$ y $N(x,y)$ siendo funciones homogéneas del mismo grado de homogeneidad.

> Lo que sigue es una demostración un poco complicada de seguir, pero permitirá una herramienta muy necesaria a futuro.

Continuamos a partir de esa definición
$$\dfrac{dy}{dx}=-\dfrac{M(x,y)}{N(x,y)}=f(x,y)\qquad ,$$
$$M(tx,ty)=t^n\cdot M(x,y)\qquad\land\qquad N(tx,ty)=t^n\cdot N(x,y)$$
por ser ambas homogéneas.
Resulta entonces que $f(x,y)$ es homogénea de grado 0, ya que se cancelan los $t^n$ en la división.

Al ser homogénea de grado 0 se verifica que
$$f(tx,ty)=t^0\cdot f(x,y)=f(x,y)$$
lo cual nos permite elegir cualquier $t$ que queramos y que la función se mantenga igual. Elijamos entonces
$$
\begin{cases}
f(tx,ty)=f(x,y) \\
t = \dfrac1 x
\end{cases}
$$

por lo que
$$f(\dfrac x x,\dfrac y x)=f(1,\dfrac y x)$$
recordando que se mantiene aún lo previamente establecido
$$f(1,\dfrac y x)=f(x,y)$$

Ahora establezcamos la siguiente variable, nos será útil a futuro
$$
z = \dfrac y x
$$
$$zx=y$$
derivamos
$$dx\cdot z+x\cdot dz=dy$$
y dividimos por $dx$
$$\dfrac{dx\cdot z+x\cdot dz}{dx}=\dfrac{dy}{dx}$$
$$z+x\dfrac{dz}{dx}=\dfrac{dy}{dx}$$
nos deshicimos entonces de las $y$ de ambos lados de la ecuación.

Hecha estas demostraciones, volvemos a la EDO de más arriba.
$$\dfrac{dy}{dx}=f(x,y)$$
y reemplazamos con lo demostrado
$$z+x\dfrac{dz}{dx}=f(1,z)$$
¿Para que sirve todo esto? Lo que nos queda es una EDO, con la característica de ser de **variables separables**. Separemos entonces
$$\dfrac1 {f(1,z)-z}dz=\dfrac1 x dx$$
y ya podemos reemplazar $z$ por $\dfrac x y$.

## EDO lineal
Se le llama **ecuación diferencial ordinaria lineal** de primer orden a la que es de la
forma
$$p(x)\cdot y'+q(x)\cdot y=f(x)$$
siendo $p(x)$, $q(x)$ y $f(x)$ continuas en cierto intervalo $I$.
Además, se le llama **ecuación homogénea asociada** (a la EDO lineal) a la ecuación diferencial de forma
$$p(x)\cdot y'+q(x)\cdot y=0$$
Esta última tiene la solución idénticamente nula ($p(x)\cdot y'=q(x)\cdot y=0$), pero además, para los valores de x para los cuales $p(x)\neq 0$ (para evitar division por 0), resulta que
$$p(x).y' = -q(x).y$$
$$\frac{y'}{y} = - \frac{q(x)}{p(x)}$$

integramos
$$\int \frac{y'}{y} dx = - \int \frac{q(x)}{p(x)} dx$$

resolvemos
$$\ln|y| = - \int \frac{q(x)}{p(x)} dx + C$$

despejamos
$$y = Ke^{-\int \frac{q(x)}{p(x)} dx} \text{ con } K \in \mathbb{R}, K \neq 0$$

Con eso llegamos a la **solución general homogénea** (SGH), la cual si permite $K=0$ incluye la solución nula que mencionamos previamente.
Tenemos entonces las soluciones posibles: La idénticamente nula y las formadas por la SGH, con el intervalo $I$ determinado por los puntos singulares en los que $p(x)=0$ y se hace inválida la solución.

Hagamos ahora un par de observaciones.

Supongamos que tenemos dos SP, obtenidas particularizando la SGH
$$p(x)\cdot\varphi_1 '+q(x)\cdot\varphi_1=0$$
$$p(x)\cdot\varphi_2 '+q(x)\cdot\varphi_2=0$$
para todo $x\in I$.
Ahora, establezcamos unas variables $a,\ b\in\mathbb{R}$, multipliquemos
$$a\cdot p(x)\cdot\varphi_1 '+a\cdot q(x)\cdot\varphi_1=0$$
$$b\cdot p(x)\cdot\varphi_2 '+b\cdot q(x)\cdot\varphi_2=0$$
y sumemos miembro a miembro$$a\cdot p(x)\cdot\varphi_1 '+a\cdot q(x)\cdot\varphi_1+b\cdot p(x)\cdot\varphi_2 '+b\cdot q(x)\cdot\varphi_2=0$$
$$p(x)\cdot\left(a\cdot\varphi_1'+b\cdot\varphi_2'\right)+q(x)\cdot\left(a\cdot\varphi_1+b\cdot\varphi_2\right)=0$$
comparemos la forma de esta ecuación con la de la original
$$p(x)\cdot y'+q(x)\cdot y=0$$
y verificando
$$\left(a\cdot\varphi_1+b\cdot\varphi_2\right)'=a\cdot\varphi_1'+b\cdot\varphi_2'$$
queda demostrado que
$$y=a\cdot\varphi_1+b\cdot\varphi_2$$
$$y'=a\cdot\varphi_1'+b\cdot\varphi_2'$$
¿Que conclusiones podemos extraer de esto?
Primero, que $a\cdot\varphi_1+b\cdot\varphi_2$ (combinación lineal de $\varphi_1$ y $\varphi_2$) es también solución de la ecuación homogénea. Esta estructura nos demuestra que el conjunto de soluciones de la ecuación lineal homogénea constituye un subespacio del espacio vectorial de las funciones derivables en el intervalo $I$. De ahí el nombre lineales.

Sin embargo, nosotros no buscamos la SGH, buscamos la SG de la ecuación diferencial lineal del principio. La obtendremos haciendo uso de la SGH.

Supongamos que tenemos dos funciones, $\gamma_1(x)$ y $\gamma_2(x)$, que son soluciones de la ecuación lineal NO homogénea en el intervalo $I$

$$p(x)\cdot\gamma_1 '+q(x)\cdot\gamma_1=f(x)$$
$$p(x)\cdot\gamma_2 '+q(x)\cdot\gamma_2=f(x)$$
Restamos miembro a miembro
$$p(x)\cdot\gamma_1 '+q(x)\cdot\gamma_1+p(x)\cdot\gamma_2 '+ q(x)\cdot\gamma_2=0$$
$$p(x)\cdot\left(\varphi_1'+\varphi_2'\right)+q(x)\cdot\left(\varphi_1+\varphi_2\right)=0$$
Esto nos demuestra que:
La diferencia entre dos soluciones cualesquiera de la ecuación NO homogénea constituye una solución de la ecuación homogénea.
A simple vista esto no nos sirve, va para el otro lado. Sin embargo, nosotros ya conocemos la SGH
$$\gamma_H(x) = Ke^{-\int \frac{q(x)}{p(x)} dx}$$
y si tomamos alguna solución particular de la ecuación NO homogénea ($y_p(x)$), podemos construir su solución con una simple suma.
$$y(x)=\gamma_H(x)+y_p(x)$$
Todo esto es útil, pero ¿como encontramos una solución particular $y_p$ para la NO homogénea?

Un método es tomar la solución general de la homogénea y variar la constante arbitraria hasta que cumpla con la EDO lineal.
$$y_p(x)=K(x)\cdot e^{-\int \frac{q(x)}{p(x)} dx},\qquad \text{con K siendo el valor que haga cumplir a la SGH como SG la EDO}$$
Este método se conoce como *método de variación de parámetros.*
##### Ejemplo
Consideremos el siguiente PVI
$$
\begin{cases}
\dfrac{y'}x + 2y = x\ e^{-x^2} \\
y(0) = 2
\end{cases}
$$
No es de variables separables, es lineal NO homogénea, $p(x)=\dfrac1 x$, $q(x)=2$, $f(x)=x\ e^{-x^2}$. Como $p(x)$ es distinto de 0 para todo $x$, no hay puntos singulares.
1. Buscar SGH
$$\dfrac{y'}x + 2y = 0$$
$$\dfrac{y'}y=-2x$$
$$\int\dfrac{y'}y\ dx=\int-2x\ dx$$
$$\int\dfrac1y\ dy=\int-2x\ dx$$
$$ln\ y=-x^2+K$$
$$\gamma_h(x)=C\cdot e^{-x^2}\qquad \text{con C}\in\mathbb{R}$$
2. Buscar una SP de la NO homogénea mediante *método de variación de parámetros*.
	$$\gamma_p(x)=C(x)\cdot e^{-x^2}\qquad\text{con C como función para permitir variación}$$
$$\gamma_p'(x)=C'(x)\cdot e^{-x^2}-C(x)\cdot 2xe^{-x^2}$$
$$\dfrac{\gamma_p'}x + 2\gamma_p = x\ e^{-x^2}$$
$$\dfrac{C'(x)\cdot e^{-x^2}-C(x)\cdot 2xe^{-x^2}}{x}+2C(x)\cdot e^{-x^2}=x\ e^{-x^2}$$
$$\dfrac{C'(x)\cdot e^{-x^2}}{x}+C(x)\cdot \left(2e^{-x^2}-\dfrac{2xe^{-x^2}}{x}\right)=x\ e^{-x^2}$$
$$C'(x)\cdot\dfrac{e^{-x^2}}x=e^{-x^2}$$
$$C'(x)=x^2\qquad \text{pero no nos importa C'(x), queremos C(x)}$$
$$C(x)=\dfrac{x³}3+K$$
3. Tomamos una solución particular
$$C(x)=\dfrac{x³}3$$
$$\gamma_p(x)=\dfrac{x³}3\cdot e^{-x²}$$
4. Construimos la SG de la NO homogénea
$$y(x) = \underbrace{C e^{-x^2}}_{\gamma_h(x)} + \underbrace{\frac{x^3}{3} e^{-x^2}}_{\gamma_p(x)}$$
5. Esa parte está lista, pero el problema no está terminado aún. Este es un PVI, debemos ahora usando la SG obtenida encontrar la SP.
$$y(0)=2$$
$$2 = C\cdot e^{-0^2} + \frac{0^3}{3}\cdot e^{-0^2}$$
$$C=2$$
6. Respondemos
$$\text{SP :}\qquad y(x)=e^{-x²}\cdot\left(C+\dfrac{x³}{3}\right)$$
$$\text{SP :}\qquad y(x)=e^{-x²}\cdot\left(2+\dfrac{x³}{3}\right)$$
