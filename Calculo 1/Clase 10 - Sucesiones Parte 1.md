# Sucesiones Numéricas Parte 1

En esta clase se introduce el lenguaje de las sucesiones numéricas: cómo describirlas,
representarlas y reconocer sus patrones. Se estudiarán sus propiedades elementales, las
progresiones, la recursividad y algunas sucesiones clásicas; los límites y la
convergencia rigurosa se desarrollarán en la Clase 11.

---

## 1. Patrones numéricos y sucesiones

Una lista ordenada de números puede registrar fenómenos muy distintos: la cantidad de
unidades producidas cada mes, las aproximaciones sucesivas a una raíz o los puntos que
se obtienen al repetir una construcción geométrica. Lo esencial no es solo qué valores
aparecen, sino el orden en que aparecen y la regla que los produce.

Considérense las siguientes listas:

$$
1,\ 3,\ 5,\ 7,\ \dots
$$

$$
1,\ \dfrac{1}{2},\ \dfrac{1}{3},\ \dfrac{1}{4},\ \dots
$$

$$
1,\ -1,\ 1,\ -1,\ \dots
$$

La primera registra los números impares; la segunda contiene los recíprocos de los
números naturales; la tercera alterna entre dos valores. Aunque las tres son listas
infinitas, cada una tiene una regla precisa que permite determinar cualquiera de sus
términos.

> **Nota histórica:** El estudio sistemático de sucesiones se consolidó durante los
> siglos XVII y XVIII, al intentar dar sentido riguroso a procesos infinitos que ya
> aparecían en el método de exhausción griego. Más adelante, Cauchy y Weierstrass
> formalizaron el lenguaje de límites que convierte a las sucesiones en una base del
> análisis matemático.

**Ejemplo 1.1 (Patrón cuadrático):**
La sucesión de cuadrados perfectos se escribe como
$$
1,\ 4,\ 9,\ 16,\ 25,\dots
$$
y tiene término general $a_n=n^2$. Por ejemplo, $a_7=49$.

**Ejemplo 1.2 (Crecimiento discreto):**
Una cuenta que inicia con $100$ unidades y recibe $25$ unidades cada mes registra los
saldos $125,150,175,200,\dots$. El índice representa el mes y el término representa
el saldo correspondiente.

---

## 2. Definición formal y notación

Una sucesión es una función cuyo dominio es discreto: se evalúa en los números
naturales, no en todos los números reales.

**Definición 2.1 (Sucesión real):**
Una **sucesión de números reales** es una función
$$
a:\mathbb{N}\to\mathbb{R}
$$
que asigna a cada índice natural $n$ un único valor real $a_n$. El valor $a_n$ se
denomina **término de índice $n$**, **enésimo término** o **término general**.

Las notaciones habituales son $(a_n)$, $\{a_n\}_{n\in\mathbb{N}}$,
$\{a_n\}_{n=1}^{\infty}$ y, si no hay ambigüedad, $\{a_n\}$. La expresión
$$
(a_n)=(a_1,a_2,a_3,\dots)
$$
no representa un conjunto: el orden de sus términos es esencial.

**Ejemplo 2.1:**
Si $a_n=\dfrac{1}{n}$, se tiene
$$
a_1=1,\qquad a_2=\dfrac{1}{2},\qquad a_5=\dfrac{1}{5}.
$$

---

## 3. Partes de una sucesión

Según la convención establecida en la Clase 2, los naturales sin cero y los naturales
con cero se denotan, respectivamente, por
$$
\mathbb{N}^{*}=\{1,2,3,\dots\},
\qquad
\mathbb{N}=\{0,1,2,3,\dots\}.
$$
En el contexto de sucesiones, los índices pertenecerán a $\mathbb{N}^{*}$. Por tanto,
la notación formal es $\{a_n\}_{n\in\mathbb{N}^{*}}$; sin embargo, para aligerar la
escritura, en esta clase se usará
$$
\{a_n\}_{n\in\mathbb{N}}
$$
con el acuerdo de que el índice comienza en $1$, salvo indicación expresa en contrario.

**Definición 3.1 (Elementos de una sucesión):**

1. El **índice** $n$ determina la posición de un término.
2. El **término** $a_n$ es el valor asociado a ese índice.
3. El **término inicial** es $a_1$ bajo la convención del curso.
4. El **término general** es una regla para calcular $a_n$ para cada
	$n\in\mathbb{N}$.

**Ejemplo 3.1:**
Para $a_n=2^n$, se cumple $a_1=2$, $a_2=4$ y $a_3=8$. Si se iniciara en $n=0$, el
primer término sería $a_0=1$.

---

## 4. Representación gráfica de sucesiones

Una sucesión solo está definida para índices naturales; por esa razón, se representa
mediante puntos aislados, no mediante una curva continua.

### 4.1 Representación en la recta real

En la recta real se ubican los valores $a_1,a_2,a_3,\dots$. Esta vista facilita
comparar el tamaño y la distribución de los términos.

**Ejemplo 4.1:**
Los términos de $a_n=\dfrac{1}{n}$ están entre $0$ y $1$ y se agrupan cada vez más
cerca de $0$.

### 4.2 Representación en el plano $(n,a_n)$

Para cada $n\in\mathbb{N}$ se ubica el punto $(n,a_n)$: el eje horizontal indica el
índice y el vertical el valor del término.

**Ejemplo 4.2:**
Para $a_n=(-1)^{n+1}\dfrac{1}{n}$, los primeros puntos son
$$
(1,1),\quad \left(2,-\dfrac{1}{2}\right),\quad
\left(3,\dfrac{1}{3}\right),\quad \left(4,-\dfrac{1}{4}\right).
$$
La gráfica muestra simultáneamente la alternancia de signo y la disminución de los
valores absolutos.

> **Advertencia:** $a_n=\sqrt n$ representa los puntos $(n,\sqrt n)$ con
> $n\in\mathbb{N}$, no la curva completa $y=\sqrt x$.

INSERTAR IMAGEN AQUI

---

## 5. Término general: fórmula explícita y forma recursiva

No toda sucesión posee una regla sencilla que permita anticipar sus términos. Por
ejemplo, se podría asignar a cada índice natural un número real sin que los valores
resultantes exhiban un patrón reconocible ni admitan una fórmula útil. Tales sucesiones
pueden definirse como funciones, pero no ofrecen una estructura inmediata para su
análisis.

En este curso interesan principalmente las sucesiones cuyos términos están organizados
por una regla: una relación que permite calcularlos, compararlos y estudiar su
comportamiento. Esa regla puede expresar directamente cada término mediante su índice o
construir un término a partir de los anteriores.

**Definición 5.1 (Fórmula explícita):**
Una sucesión está dada en **forma explícita** si
$$
a_n=f(n),\qquad n\in\mathbb{N}.
$$

**Ejemplo 5.1:**
La fórmula $a_n=3n-1$ genera $2,5,8,11,\dots$ y permite calcular directamente
$a_{100}=299$.

**Definición 5.2 (Forma recursiva):**
Una sucesión está dada en **forma recursiva** si se proporcionan términos iniciales y
una regla que determina un término a partir de los anteriores. En el caso más simple,
$$
a_{n+1}=F(a_n),
$$
junto con un valor inicial $a_1$.

**Ejemplo 5.2 (Crecimiento multiplicativo):**
La sucesión definida por
$$
a_1=3,\qquad a_{n+1}=2a_n
$$
se construye duplicando cada término anterior. Sus primeros valores son
$$
3,\ 6,\ 12,\ 24,\ 48,\dots
$$
Para calcular $a_5$, no se evalúa directamente el índice $5$; se aplican de manera
sucesiva las reglas que producen $a_2$, $a_3$, $a_4$ y finalmente $a_5$.

Una misma sucesión puede admitir ambas descripciones. A partir de una regla recursiva
se puede buscar una fórmula explícita para su término general; recíprocamente, una
fórmula explícita permite obtener una relación recursiva al relacionar $a_{n+1}$ con
$a_n$ y especificar el término inicial. Esta conversión no siempre conduce a una
fórmula elemental, pero cuando es posible permite elegir la descripción más adecuada
para el problema.

**Ejemplo 5.3 (Progresión aritmética):**
La sucesión de números impares es una progresión aritmética de diferencia $2$. Su
forma recursiva es
$$
a_1=1,\qquad a_{n+1}=a_n+2.
$$
La fórmula explícita equivalente es
$$
a_n=2n-1.
$$

**Ejemplo 5.4 (Sucesión de recíprocos):**
Considérese la fórmula explícita
$$
a_n=\dfrac{1}{n}.
$$
Para obtener una relación recursiva, se expresa $a_{n+1}$ en función de $a_n$:
$$\begin{align}
a_{n+1} &= \dfrac{1}{n+1} \\
		 &= \dfrac{\dfrac{1}{n}}{1+\dfrac{1}{n}} \\
		 &= \dfrac{a_n}{1+a_n}.
\end{align}$$
Por tanto, la misma sucesión queda determinada recursivamente por
$$
a_1=1,\qquad a_{n+1}=\dfrac{a_n}{1+a_n}.
$$
Esta regla no consiste en sumar una cantidad fija al término anterior, pero genera los
mismos valores $1,\dfrac12,\dfrac13,\dfrac14,\dots$.

---

## 6. Descubrir el término general

Al buscar una regla conviene revisar diferencias, cocientes, signos y expresiones
conocidas como cuadrados o potencias. La fórmula propuesta debe reproducir todos los
términos disponibles.

**Ejemplo 6.1:**
Para $1,3,5,7,\dots$, la diferencia común es $2$ y el término general es
$$
a_n=2n-1.
$$

**Ejemplo 6.2:**
Para $1,-2,3,-4,5,\dots$, el valor absoluto del término de índice $n$ es $n$ y el
signo alterna; por tanto,
$$
a_n=(-1)^{n+1}n.
$$

**Ejemplo 6.3:**
Para $\dfrac12,\dfrac23,\dfrac34,\dfrac45,\dots$, el numerador es el índice y el
denominador es una unidad mayor. Así,
$$
a_n=\dfrac{n}{n+1}.
$$

### 6.1 Ejercicios propuestos

**Ejercicio 6.1:** Determinar el término general de $2,4,6,8,\dots$.

**Respuesta:** $a_n=2n$.

**Ejercicio 6.2:** Determinar el término general de $1,4,9,16,\dots$.

**Respuesta:** $a_n=n^2$.

**Ejercicio 6.3:** Determinar el término general de $3,6,12,24,\dots$.

**Respuesta:** $a_n=3\cdot2^{n-1}$.

**Ejercicio 6.4:** Determinar el término general de $0,3,8,15,24,\dots$.

**Respuesta:** $a_n=n^2-1$.

---

## 7. Curiosidad: interpolación polinómica

Los términos iniciales de una sucesión no determinan necesariamente una regla única.
Por ejemplo, además de la regla natural de los impares, se puede forzar que la lista
$1,3,5,\dots$ continúe con $\pi$.

**Ejemplo 7.1 (Forzar un término):**
La fórmula
$$
a_n=2n-1+\dfrac{\pi-7}{6}(n-1)(n-2)(n-3)
$$
satisface $a_1=1$, $a_2=3$, $a_3=5$ y $a_4=\pi$.

**Proposición 7.1 (No unicidad a partir de datos finitos):**
Dados un número finito de términos de una sucesión, existen en general infinitas reglas
que los reproducen.

**Demostración:**
Si $p(n)$ coincide con valores conocidos de índices $1,2,\dots,k$, entonces para cada
$c\in\mathbb{R}$ la expresión
$$
q_c(n)=p(n)+c(n-1)(n-2)\cdots(n-k)
$$
coincide con $p(n)$ en esos índices. Al variar $c$ se obtienen reglas distintas.
$\blacksquare$

> **Lección:** Para elegir un término general se requiere información adicional: un
> contexto, una regla de formación o propiedades que la sucesión debe satisfacer.

---

## 8. Propiedades de orden y acotación

Las cotas permiten describir si los términos permanecen dentro de una región de la
recta real, y la monotonía permite compararlos consecutivamente.

### 8.1 Cotas y acotación

**Definición 8.1 (Cotas):**
Para $S\subseteq\mathbb{R}$, un número $k$ es una **cota inferior** si $k\leq x$ para
todo $x\in S$, y un número $K$ es una **cota superior** si $x\leq K$ para todo
$x\in S$.

**Definición 8.2 (Sucesión acotada):**
La sucesión $(a_n)$ es **acotada** si existe $M>0$ tal que
$$
|a_n|\leq M,\qquad \forall n\in\mathbb{N}.
$$

**Ejemplo 8.1:**
La sucesión $(-1)^n$ es acotada por $1$, mientras que $n^2$ no está acotada
superiormente.

### 8.2 Supremo e ínfimo

**Definición 8.3 (Supremo e ínfimo):**
El **supremo** de un conjunto no vacío es su menor cota superior y el **ínfimo** es su
mayor cota inferior, cuando tales cotas existen.

**Axioma del supremo:**
Todo subconjunto no vacío de $\mathbb{R}$ que esté acotado superiormente posee supremo
en $\mathbb{R}$.

> **Observación importante:** El máximo debe pertenecer al conjunto, pero el supremo
> puede no pertenecer a él. Si existe máximo, coincide con el supremo; de forma
> análoga, si existe mínimo, coincide con el ínfimo.

**Ejemplo 8.2:**
Para $S=(0,1)$ se tiene $\inf(S)=0$ y $\sup(S)=1$, pero no existen mínimo ni máximo.
Para $T=[0,1]$ se cumple
$$
\min(T)=\inf(T)=0,\qquad \max(T)=\sup(T)=1.
$$

**Ejemplo 8.3:**
Para $a_n=1-\dfrac1n$, el conjunto de valores tiene mínimo e ínfimo iguales a $0$ y
supremo igual a $1$, que no es máximo porque ningún término vale $1$.

### 8.3 Monotonía y alternancia

**Definición 8.4 (Monotonía):**
Una sucesión es creciente si $a_{n+1}\geq a_n$ para todo $n$ y decreciente si
$a_{n+1}\leq a_n$ para todo $n$. Las desigualdades estrictas definen las versiones
estrictamente creciente y estrictamente decreciente. Una sucesión es **monótona** si
es creciente o decreciente.

**Ejemplo 8.4:**
La sucesión $2n-1$ es estrictamente creciente porque
$$
[2(n+1)-1]-(2n-1)=2>0.
$$
La sucesión $\dfrac1n$ es estrictamente decreciente.

**Definición 8.5 (Alternancia):**
Una sucesión es **alternada** si los signos de sus términos se alternan. Por ejemplo,
$(-1)^n n$ alterna de signo y no es monótona.

> **Observación:** La sucesión $n$ es creciente pero no está acotada superiormente;
> $(-1)^n$ está acotada, pero no es monótona.

INSERTAR IMAGEN AQUI

---

## 9. Progresiones básicas

Las progresiones son familias de sucesiones definidas por una regla de cambio
particularmente simple. Aparecen al modelar incrementos constantes, crecimientos por
un porcentaje fijo y relaciones entre cantidades inversas.

### 9.1 Progresión aritmética

**Definición 9.1 (Progresión aritmética):**
Una sucesión $(a_n)$ es una **progresión aritmética** si existe un número real $d$, su
**diferencia común**, tal que
$$
a_{n+1}=a_n+d,\qquad \forall n\in\mathbb{N}.
$$
Si se conoce $a_1$, su término general es
$$
a_n=a_1+(n-1)d.
$$

**Proposición 9.1 (Suma de una progresión aritmética):**
Si $S_n=a_1+a_2+\cdots+a_n$, entonces
$$
S_n=\dfrac{n(a_1+a_n)}{2}
=\dfrac{n[2a_1+(n-1)d]}{2}.
$$

**Demostración:**
Al escribir la suma en orden directo y en orden inverso, se tiene
$$\begin{align}
S_n &= a_1+a_2+\cdots+a_{n-1}+a_n,\\
S_n &= a_n+a_{n-1}+\cdots+a_2+a_1.
\end{align}$$
Al sumar ambas igualdades, cada una de las $n$ parejas vale $a_1+a_n$. Por tanto,
$$
2S_n=n(a_1+a_n),
$$
de donde se obtiene la fórmula. $\blacksquare$

**Ejemplo 9.1:**
Para la progresión $3,7,11,15,\dots$, se tiene $a_1=3$ y $d=4$. Entonces
$$
a_n=3+4(n-1)=4n-1.
$$
El término quincuagésimo es $a_{50}=199$ y la suma de los primeros $50$ términos es
$$
S_{50}=\dfrac{50(3+199)}{2}=5050.
$$

**Ejemplo 9.2 (Suma de Gauss):**
Los números naturales $1,2,3,\dots,100$ forman una progresión aritmética. Por tanto,
$$
1+2+3+\cdots+100=\dfrac{100(1+100)}{2}=5050.
$$

> **Nota histórica:** Una anécdota atribuida a Carl Friedrich Gauss relata que, siendo
> niño, calculó esta suma al emparejar el primer término con el último, el segundo con
> el penúltimo, y así sucesivamente.

### 9.2 Progresión geométrica

**Definición 9.2 (Progresión geométrica):**
Una sucesión $(a_n)$ es una **progresión geométrica** si existe un número real $r$, su
**razón común**, tal que
$$
a_{n+1}=ra_n,\qquad \forall n\in\mathbb{N}.
$$
Si se conoce $a_1$, su término general es
$$
a_n=a_1r^{n-1}.
$$

**Proposición 9.2 (Suma finita de una progresión geométrica):**
Sea $S_n=a_1+a_2+\cdots+a_n$. Entonces
$$
S_n=
\begin{cases}
\dfrac{a_1(1-r^n)}{1-r}, & \text{si } r\neq1,\\
na_1, & \text{si } r=1.
\end{cases}
$$

**Demostración:**
Para $r\neq1$, la forma explícita permite escribir
$$\begin{align}
S_n &= a_1+a_1r+\cdots+a_1r^{n-1},\\
rS_n &= a_1r+a_1r^2+\cdots+a_1r^n.
\end{align}$$
Al restar la segunda igualdad de la primera resulta
$$
(1-r)S_n=a_1(1-r^n),
$$
que produce la fórmula anunciada. Si $r=1$, todos los términos son $a_1$ y
$S_n=na_1$. $\blacksquare$

**Ejemplo 9.3:**
Para la progresión $2,6,18,54,\dots$, se tiene $a_1=2$ y $r=3$. Así,
$$
Los cuadrados perfectos forman la sucesión
$$
La suma de sus primeros diez términos es
$$
S_{10}=\dfrac{2(1-3^{10})}{1-3}=59048.
$$

**Ejemplo 9.4 (Interés compuesto):**
Un capital inicial de $1000$ unidades invertido con una tasa anual compuesta de $5\%$
origina la sucesión
$$
C_n=1000(1.05)^n,
$$
donde $C_n$ representa el capital después de $n$ años. Después de $20$ años,
$$
C_{20}=1000(1.05)^{20}\approx2653.
$$

INSERTAR IMAGEN AQUI

### 9.3 Progresión armónica

**Definición 9.3 (Progresión armónica):**
Una sucesión $(h_n)$ es una **progresión armónica** si la sucesión de sus recíprocos
$(1/h_n)$ forma una progresión aritmética. Si los denominadores no se anulan, su forma
general es
$$
h_n=\dfrac{1}{a+(n-1)d},
$$
donde $a$ y $d$ son el primer término y la diferencia común de la progresión
aritmética formada por los recíprocos.

**Ejemplo 9.5:**
La sucesión
$$
1,\ \dfrac{1}{2},\ \dfrac{1}{3},\ \dfrac{1}{4},\dots
$$
es armónica porque sus recíprocos son $1,2,3,4,\dots$, una progresión aritmética de
diferencia común $1$.

> **Observación:** Las sumas infinitas asociadas a progresiones geométricas y la
> llamada serie armónica se estudiarán más adelante, al introducir series en Cálculo 2.

---

## 10. Sucesiones recursivas

En una fórmula explícita se puede calcular directamente un término lejano. Sin embargo,
muchos procesos describen de manera más natural cómo pasar de un estado al siguiente.
Las sucesiones recursivas codifican precisamente esa dependencia entre términos.

### 10.1 Definición y orden de una recurrencia

**Definición 10.1 (Sucesión recursiva):**
Una **sucesión recursiva** o **recurrente** se determina mediante:

1. Uno o más términos iniciales.
2. Una relación de recurrencia que expresa un término en función de términos
	anteriores.

Una recurrencia de orden $k$ tiene la forma
$$
a_{n+k}=F(n,a_{n+k-1},a_{n+k-2},\dots,a_n),
$$
acompañada de $k$ condiciones iniciales.

El caso de orden $1$ depende solo del término anterior:
$$
a_{n+1}=f(a_n),
$$
con un valor inicial $a_1$.

**Ejemplo 10.1:**
La regla
$$
a_1=3,\qquad a_{n+1}=a_n+4
$$
produce los términos
$$
3,\ 7,\ 11,\ 15,\dots
$$
Cada paso añade $4$ al valor anterior. Esta definición es recursiva y describe la
misma progresión aritmética del término general $a_n=4n-1$.

### 10.2 Generación iterativa de términos

Una recurrencia permite calcular los términos uno a uno, incluso cuando no se conoce
una fórmula explícita sencilla.

**Ejemplo 10.2 (Método de Herón):**
Sea
$$
a_1=2,\qquad a_{n+1}=\dfrac12\left(a_n+\dfrac{2}{a_n}\right).
$$
Los primeros términos son
$$\begin{align}
a_2 &= \dfrac12\left(2+\dfrac22\right)=\dfrac32,\\
a_3 &= \dfrac12\left(\dfrac32+\dfrac{2}{3/2}\right)=\dfrac{17}{12},\\
a_4 &= \dfrac12\left(\dfrac{17}{12}+\dfrac{24}{17}\right)
	  =\dfrac{577}{408}.
\end{align}$$
Numéricamente, estos valores son aproximadamente
$$
2,\ 1.5,\ 1.4167,\ 1.4142,\dots
$$
El procedimiento genera aproximaciones cada vez más precisas de $\sqrt2$. La
justificación rigurosa de su convergencia se estudiará en la Parte 2.

INSERTAR IMAGEN AQUI

**Ejemplo 10.3 (Población idealizada):**
Si una población inicial de $200$ individuos aumenta un $3\%$ en cada periodo, el
modelo discreto es
$$
P_0=200,\qquad P_{n+1}=1.03P_n.
$$
La recurrencia expresa directamente la regla de actualización: el nuevo valor se
obtiene multiplicando el anterior por $1.03$.

> **Observación:** Una recurrencia no siempre determina una sucesión sin condiciones
> iniciales. Por ejemplo, $a_{n+1}=a_n+2$ admite muchas soluciones: $1,3,5,\dots$;
> $4,6,8,\dots$; y otras. El valor inicial selecciona una sucesión concreta.

---

## 11. Sucesiones famosas o clásicas

Algunas sucesiones aparecen repetidamente en distintas áreas de las matemáticas y las
ciencias. En esta sección se presenta un catálogo breve; sus propiedades profundas se
estudiarán cuando dispongamos de las herramientas apropiadas.

### 11.1 Sucesión de Fibonacci

La sucesión de Fibonacci comienza con $0$ y $1$, y cada término posterior es la suma de
los dos anteriores:
$$
0,\ 1,\ 1,\ 2,\ 3,\ 5,\ 8,\ 13,\dots
$$
Su regla recursiva es
$$
F_0=0,\qquad F_1=1,\qquad F_n=F_{n-1}+F_{n-2}\quad(n\geq2).
$$
Esta sucesión aparece en problemas de conteo y en modelos idealizados de ramificación.
Su relación con la razón áurea y su fórmula explícita se desarrollarán en la Parte 2.

INSERTAR IMAGEN AQUI

### 11.2 Números triangulares y números de Lucas

Los **números triangulares** cuentan puntos dispuestos en filas triangulares:
$$
1,\ 3,\ 6,\ 10,\ 15,\dots
$$
Su término general es
$$
T_n=\dfrac{n(n+1)}{2}.
$$

Los **números de Lucas** satisfacen la misma recurrencia que Fibonacci, pero con
condiciones iniciales diferentes:
$$
2,\ 1,\ 3,\ 4,\ 7,\ 11,\dots
$$
La comparación entre ambas sucesiones ilustra nuevamente el papel de los términos
iniciales en una relación recursiva.

### 11.3 Sucesión de los números primos

Al ordenar los números primos se obtiene
$$
2,\ 3,\ 5,\ 7,\ 11,\ 13,\ 17,\dots
$$
A diferencia de las progresiones, las diferencias entre términos consecutivos no son
constantes ni siguen una regla elemental conocida. Esta sucesión ocupa un lugar central
en teoría de números y criptografía.

---

## 12. Ecuaciones en diferencias finitas

Las relaciones de recurrencia pueden entenderse como ecuaciones donde el avance no se
mide mediante una variación continua, sino mediante pasos enteros. Por ese motivo se
denominan **ecuaciones en diferencias finitas**.

**Definición 12.1 (Ecuación en diferencias):**
Una ecuación en diferencias de orden $k$ relaciona términos separados por un número
finito de índices. Una forma general es
$$
a_{n+k}=F(n,a_{n+k-1},\dots,a_n).
$$
Resolverla significa determinar una fórmula explícita o describir rigurosamente la
sucesión que satisfacen la ecuación y las condiciones iniciales.

**Ejemplo 12.1:**
La ecuación
$$
a_{n+2}-3a_{n+1}+2a_n=0
$$
es una ecuación en diferencias lineal de orden $2$. Para determinar una solución
concreta se requieren dos condiciones iniciales, por ejemplo $a_1$ y $a_2$.

> **Nota:** El estudio sistemático de ecuaciones en diferencias lineales, sistemas y
> ecuaciones no homogéneas corresponde a Matemáticas Discretas. En este curso se usan
> como un lenguaje para describir sucesiones recursivas.

---

## 13. Aplicaciones

Las sucesiones permiten registrar fenómenos que avanzan por etapas. Su estructura
discreta aparece de forma natural en matemáticas aplicadas, física, economía y
computación.

- **Finanzas:** el interés compuesto se modela mediante progresiones geométricas;
	cada periodo actualiza el capital anterior por un factor fijo.
- **Física:** al medir la posición de un objeto a intervalos regulares de tiempo se
	obtiene una sucesión de posiciones. En movimiento uniformemente acelerado, los
	incrementos sucesivos de posición forman una progresión aritmética.
- **Programación:** los arreglos, bucles e implementaciones recursivas operan sobre
	valores indexados, que constituyen sucesiones finitas o infinitas.
- **Naturaleza y geometría:** las sucesiones de Fibonacci se asocian a patrones de
	filotaxis y a la espiral de Fibonacci, que aparece como modelo aproximado en algunas
	disposiciones de semillas, piñas y conchas.

---

## 14. Ejercicios resueltos

Los siguientes problemas combinan fórmulas explícitas, relaciones de recurrencia e
inducción. Más que reconocer un patrón visual, exigen identificar la estructura que la
regla de formación impone sobre los términos.

### Ejercicio 14.1

Sea la sucesión definida por
$$
a_1=1,
\qquad
a_{n+1}=a_n+2n+1
\quad(n\geq1).
$$
Determinar una fórmula explícita para $a_n$.

**Solución:** Los primeros términos son
$$
1,\ 4,\ 9,\ 16,\dots,
$$
lo que sugiere la fórmula $a_n=n^2$. Se verifica por inducción. Para $n=1$, se tiene
$a_1=1=1^2$. Si $a_n=n^2$, entonces
$$\begin{align}
a_{n+1} &= a_n+2n+1 \\
		 &= n^2+2n+1 \\
		 &= (n+1)^2.
\end{align}$$
Por el principio de inducción, se cumple
$$
a_n=n^2
$$
para todo $n\in\mathbb{N}^{*}$. $\blacksquare$

### Ejercicio 14.2

La sucesión de radicales anidados se define por
$$
a_1=\sqrt{2},
\qquad
a_{n+1}=\sqrt{2+a_n}
\quad(n\geq1).
$$
Demostrar que
$$
a_n=2\cos\left(\dfrac{\pi}{2^{n+1}}\right)
$$
para todo $n\in\mathbb{N}^{*}$.

**Solución:** Para $n=1$,
$$
a_1=\sqrt2=2\cos\left(\dfrac{\pi}{4}\right),
$$
de modo que la fórmula es válida inicialmente. Supóngase que se cumple para un índice
$n$. Entonces, al usar la identidad $1+\cos\theta=2\cos^2\left(\dfrac{\theta}{2}\right)$,
se obtiene
$$\begin{align}
a_{n+1} &= \sqrt{2+2\cos\left(\dfrac{\pi}{2^{n+1}}\right)} \\
		 &= \sqrt{4\cos^2\left(\dfrac{\pi}{2^{n+2}}\right)} \\
		 &= 2\cos\left(\dfrac{\pi}{2^{n+2}}\right).
\end{align}$$
El coseno es positivo en los ángulos involucrados, por lo que la última igualdad es
válida. Por inducción, la expresión propuesta describe todos los términos de la
sucesión. $\blacksquare$

### Ejercicio 14.3

Sea $(F_n)$ la sucesión de Fibonacci dada por
$$
F_0=0,
\qquad
F_1=1,
\qquad
F_{n+1}=F_n+F_{n-1}
\quad(n\geq1).
$$
Demostrar que dos términos consecutivos de la sucesión son coprimos; es decir,
$$
\operatorname{mcd}(F_n,F_{n+1})=1
$$
para todo $n\geq1$.

**Solución:** Si un número entero $d$ divide simultáneamente a $F_n$ y a $F_{n+1}$,
entonces también divide su diferencia:
$$
F_{n+1}-F_n=F_{n-1}.
$$
Por tanto,
$$
\operatorname{mcd}(F_n,F_{n+1})
=\operatorname{mcd}(F_{n-1},F_n).
$$
Al repetir este razonamiento se llega a
$$
\operatorname{mcd}(F_n,F_{n+1})
=\operatorname{mcd}(F_1,F_2)
=\operatorname{mcd}(1,1)
=1.
$$
Así, ningún entero mayor que $1$ puede dividir dos términos consecutivos de Fibonacci.
$\blacksquare$

---

**Fin de la Clase 10: Sucesiones Parte 1**
