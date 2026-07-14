# Inecuaciones: Fundamentos Algebraicos

En esta clase se estudian las inecuaciones como generalización de las ecuaciones: desigualdades lineales, cuadráticas, racionales, de orden superior, irracionales, trascendentes y con valor absoluto, junto con sistemas de inecuaciones, resueltas mediante el método de la tabla de signos, con énfasis en el rigor de las demostraciones y en su aplicación a la determinación de dominios de funciones.

## 1. Desigualdades e Inecuaciones: Conceptos Básicos

### 1.1 Desigualdades: Definición y Tipos

A diferencia de las ecuaciones, que establecen una igualdad estricta entre dos cantidades, gran parte de la matemática se basa en comparar tamaños o magnitudes que no son iguales. Pensemos en situaciones cotidianas: "la velocidad máxima es 120 km/h", "el presupuesto debe ser menor a 500 dólares". Las desigualdades nos permiten modelar matemáticamente estas restricciones y acotar valores.

**Definición 1.1 (Desigualdad):**
Una desigualdad es una relación matemática de orden que compara dos expresiones usando los símbolos:
- $<$ (menor que)
- $>$ (mayor que)
- $\leq$ (menor o igual que)
- $\geq$ (mayor o igual que)

En su forma más fundamental, las desigualdades se trabajan puramente con **números reales** para establecer una relación de tamaño.

**Ejemplo 1.1 (Desigualdades numéricas):**
Cuando operamos únicamente con números, una desigualdad puede evaluarse directamente como un enunciado verdadero o falso:
- $5 > 3$ (Verdadero: 5 está a la derecha de 3 en la recta numérica).
- $-2 > -9$ (Verdadero: -2 es mayor porque está menos a la izquierda que -9).
- $6 < 2$ (Falso: 6 es estrictamente mayor que 2).
- $4 \leq 4$ (Verdadero: cumple la condición de "igual").

Sin embargo, las desigualdades también se pueden usar con **incógnitas** o variables. Cuando introducimos incógnitas, surgen dos grandes familias de desigualdades:
1. **Desigualdades absolutas:** Son ciertas para cualquier valor numérico real. Por ejemplo, $x^2 \geq 0$ es una verdad absoluta en $\mathbb{R}$.
2. **Desigualdades condicionales (Inecuaciones):** Su veracidad depende del valor que tomen sus variables. Por ejemplo, $x + 2 > 5$ solo es cierto si $x > 3$.

**Proposición 1.1 (Propiedades del orden en $\mathbb{R}$):**

Para cualesquiera $a, b, c \in \mathbb{R}$:
1. **Tricotomía:** Exactamente una de estas se cumple: $a < b$, $a = b$, o $a > b$.
2. **Transitividad:** Si $a < b$ y $b < c$, entonces $a < c$. (Esta propiedad también es válida para $>$, $\leq$ y $\geq$).
3. **Adición:** Si $a < b$, entonces $a + c < b + c$.
4. **Multiplicación por positivo:** Si $a < b$ y $c > 0$, entonces $ac < bc$.
5. **Multiplicación por negativo:** Si $a < b$ y $c < 0$, entonces $ac > bc$.

> **Advertencia:** ¡La última propiedad es la causa número uno de errores en cálculo! Al multiplicar o dividir una desigualdad por un número **negativo**, el símbolo de orden se **invierte**.

> **Nota:** Las propiedades 1–4 son los **axiomas del orden** del cuerpo ordenado $(\mathbb{R}, +, \cdot, <)$; se postulan como fundamentos del sistema numérico real y no se derivan de resultados más simples. La propiedad 5 sí admite demostración directa: si $a < b$ y $c < 0$, entonces $-c > 0$, y por la Propiedad 4 se obtiene $(-c) \cdot a < (-c) \cdot b$, es decir $-ac < -bc$, de donde $ac > bc$. $\square$

> **Nota histórica:** El uso de desigualdades en matemáticas se remonta a la geometría griega: los *Elementos* de Euclides (c. 300 a.C.) contienen numerosas proposiciones sobre magnitudes desiguales, incluyendo resultados equivalentes a la desigualdad triangular. Sin embargo, el tratamiento algebraico formal de las propiedades del orden tuvo que esperar hasta el siglo XIX. Fue Augustin-Louis Cauchy quien, en su *Cours d'analyse* (1821), utilizó por primera vez desigualdades algebraicas de forma sistemática para fundamentar el análisis matemático. Poco después, Karl Weierstrass, Richard Dedekind y Giuseppe Peano formalizaron los axiomas de cuerpo ordenado de los que la Proposición 1.1 es la expresión central.

### 1.2 Inecuaciones: Estructura y Solución

Ahora nos enfocaremos exclusivamente en las desigualdades condicionales.

**Definición 1.2 (Inecuación):**
Una **inecuación** es una desigualdad algebraica en la que aparecen uno o más valores desconocidos (variables o incógnitas), y resolverla consiste en encontrar todos los valores que hacen que dicha desigualdad sea verdadera.

En su forma más general, cualquier inecuación de una variable puede escribirse matemáticamente llevando todos sus términos a un lado, adoptando alguna de las siguientes formas:
$$f(x) \geq 0, \quad f(x) \leq 0, \quad f(x) > 0, \quad f(x) < 0$$
donde $x \in \text{Dom}(f)$.

Al igual que en las ecuaciones, una inecuación consta de dos **miembros** separados por el signo de desigualdad. Los elementos sumados o restados dentro de cada miembro son los **términos**.

**Ejemplo 1.2 (Variedad de inecuaciones):**
Las inecuaciones pueden involucrar diversos tipos de funciones. A continuación, presentamos algunos ejemplos puramente demostrativos con distintos símbolos de orden:
- **Lineal (menor estricto):** $3x - 5 < 10$
- **Cuadrática (mayor o igual):** $x^2 - 4x + 3 \geq 0$
- **Racional (menor o igual):** $\dfrac{2x + 1}{x - 3} \leq 4$
- **Valor absoluto (mayor estricto):** $|2x - 7| > 5$
- **Logarítmica:** $\ln(x - 2) \leq 1$

Tomemos la inecuación más simple posible: $x < 5$. Intuitivamente, sabemos que $x = 0$ la satisface, que $x = 1$ también la satisface, que $x = -100$ también, pero que $x = 6$ no la satisface pues $6$ no es menor que $5$. De hecho, cualquier número estrictamente menor que $5$ es una solución válida.

Para apreciar qué tiene esto de especial, conviene compararlo con las ecuaciones. Una ecuación lineal como $x - 5 = 0$ tiene exactamente una solución; una cuadrática como $x^2 - 1 = 0$ tiene a lo sumo dos; en general, un polinomio de grado $n$ tiene a lo sumo $n$ raíces reales. Hay ecuaciones con infinitas soluciones, como $\sin(n\pi) = 0$, que se cumple para todo $n \in \mathbb{Z}$; sin embargo, ese conjunto infinito sigue siendo **numerable**, es decir, sus elementos pueden enumerarse uno por uno: $\{\ldots, -2\pi, -\pi, 0, \pi, 2\pi, \ldots\}$. En las inecuaciones, en cambio, el conjunto solución es casi siempre **no numerable**: abarca todo un continuo de la recta real, una región sin saltos ni huecos, que contiene infinitamente más puntos que cualquier lista enumerable. Al conjunto de todos los valores que hacen verdadera la desigualdad se le denomina **conjunto solución**.

**Definición 1.3 (Conjunto Solución):**
El **conjunto solución** de una inecuación es el conjunto de todos los valores reales que satisfacen la desigualdad. Dos inecuaciones se denominan **equivalentes** si tienen exactamente el mismo conjunto solución.

**Ejemplo 1.3 (Conjuntos solución simples):**
Para comprender la naturaleza de estos conjuntos, veamos algunas inecuaciones elementales:
- $x > 0 \implies$ El conjunto solución son todos los números reales estrictamente positivos. En notación de intervalo: $(0, \infty)$.
- $x \leq 0 \implies$ El conjunto solución son todos los reales negativos incluyendo al cero. En notación de intervalo: $(-\infty, 0]$.
- $x > 5 \implies$ El conjunto solución son todos los reales estrictamente mayores a $5$. En notación de intervalo: $(5, \infty)$.
- $x \leq -3 \implies$ El conjunto solución son todos los reales menores o iguales a $-3$. En notación de intervalo: $(-\infty, -3]$.
- $|x| \leq 2 \implies$ Por la Propiedad 1 del Teorema 6.1 (que se estudiará en la Sección 6), equivale a $-2 \leq x \leq 2$. El conjunto solución es el intervalo cerrado $[-2, 2]$.
- $x^2 < 0 \implies$ El conjunto solución es vacío ($\emptyset$), pues ningún número real al cuadrado arroja un resultado negativo.
- $x^2 \geq 0 \implies$ El conjunto solución son todos los números reales ($\mathbb{R}$), pues el cuadrado de cualquier número siempre es no negativo.

### 1.3 Intervalos como Conjuntos Solución

Para representar estos infinitos valores, empleamos la notación de intervalos. Un intervalo es un subconjunto conexo de la recta real $\mathbb{R}$.

**Definición 1.4 (Intervalos):**
Sean $a, b \in \mathbb{R}$ con $a < b$. Definimos los siguientes tipos de intervalos y sus representaciones:

1. **Intervalo abierto** $(a, b)$: 
   - **Conjunto:** $\{x \in \mathbb{R} : a < x < b\}$
   - **Gráficamente:** Los extremos no están incluidos, se denotan con un círculo vacío ($\circ$).
   > **Nota de notación:** En muchos textos formales, el intervalo abierto también se denota usando corchetes invertidos (apuntando hacia afuera): $]a, b[$. Del mismo modo, un semiabierto puede escribirse como $[a, b[$ o $]a, b]$. Ambas convenciones son válidas y significan exactamente lo mismo.

2. **Intervalo cerrado** $[a, b]$:
   - **Conjunto:** $\{x \in \mathbb{R} : a \leq x \leq b\}$
   - **Gráficamente:** Los extremos están incluidos, se denotan con un círculo relleno ($\bullet$).

3. **Intervalos semiabiertos** $[a, b)$ o $(a, b]$:
   - **Conjunto:** $\{x \in \mathbb{R} : a \leq x < b\}$ o $\{x \in \mathbb{R} : a < x \leq b\}$
   - **Gráficamente:** Un extremo cerrado ($\bullet$) y el otro abierto ($\circ$).

4. **Intervalos infinitos** $(a, \infty)$, $[a, \infty)$, $(-\infty, b)$, $(-\infty, b]$:
   - **Conjunto:** $\{x \in \mathbb{R} : x > a\}$, $\{x \in \mathbb{R} : x \leq b\}$, etc.
   - Representan rayos infinitos en la recta real.

> **Nota:** El símbolo $\infty$ (infinito) no es un número real, sino un concepto que indica un crecimiento sin cota. Por ello, los extremos infinitos **siempre** deben ir con paréntesis abierto, indicando que jamás se alcanzan.

**Ejemplo 1.4:**
Si la solución a una inecuación nos dicta que $x$ debe ser "mayor o igual a -2 y estrictamente menor que 5", se puede representar de tres formas equivalentes y formalmente válidas:
- **Inecuación:** $-2 \leq x < 5$
- **Conjunto:** $\{x \in \mathbb{R} : -2 \leq x < 5\}$
- **Intervalo:** $[-2, 5)$

---
## 2. Inecuaciones Lineales

Al igual que con las ecuaciones, nuestro primer caso de estudio seran las inecuaciones lineales o de primer grado. Pensemos en la inecuación más simple posible: "¿Para qué valores de $x$ se cumple que $2x < 6$?". La respuesta es inmediata $x < 3$ y el proceso para obtenerla es casi idéntico al de resolver una ecuación lineal. Las inecuaciones lineales son el punto de partida natural del estudio de las inecuaciones, precisamente porque su resolución es directa y permite concentrarse en las reglas del orden sin distracciones algebraicas adicionales.

**Definición 2.1 (Inecuación Lineal):**
Una inecuación lineal en una variable $x$ es toda inecuación equivalente a alguna de las formas:
$$ax + b < 0, \quad ax + b \leq 0, \quad ax + b > 0, \quad ax + b \geq 0$$
con $a, b \in \mathbb{R}$ y $a \neq 0$. Se denomina lineal porque el término con la variable aparece únicamente a la primera potencia.

> **Observación:** La condición $a \neq 0$ es necesaria: si $a = 0$, la expresión $ax + b$ se reduce a la constante $b$, y la inecuación resultante es una desigualdad numérica cuya veracidad no depende de $x$ en absoluto. El conjunto solución sería $\mathbb{R}$ completo o $\emptyset$ según el valor de $b$, sin que haya nada que resolver.

### 2.1 Método de resolución

De forma análoga a las ecuaciones el objetivo será aislar la variable $x$ aplicando operaciones algebraicas a ambos miembros de la desigualdad. Las operaciones permitidas son las mismas que en una ecuación lineal —sumar, restar, multiplicar y dividir— con una diferencia fundamental:

**Proposición 2.1 (Regla de inversión del orden):**
Sea $c \in \mathbb{R}$ con $c < 0$. Si $f(x) < g(x)$, entonces:
$$\begin{align}
f(x) &< g(x) && \Big/ \cdot c \quad (c < 0) \\[1.5ex]
c \cdot f(x) &> c \cdot g(x)
\end{align}$$
En general, multiplicar o dividir ambos miembros de una inecuación por un número negativo invierte el símbolo de desigualdad.

> **Advertencia:** Este es el error más frecuente al resolver inecuaciones. Dividir por un número negativo sin invertir el símbolo produce un conjunto solución completamente erróneo.

El procedimiento general para resolver $ax + b \leq 0$ consiste en:

1. **Trasladar el término independiente:** Restar $b$ a ambos miembros para obtener $ax \leq -b$.
2. **Dividir por el coeficiente:** Dividir ambos miembros por $a$, recordando que si $a < 0$, el sentido de la desigualdad debe invertirse.
3. **Expresar el conjunto solución:** Representar el intervalo resultante en la recta real y en notación de intervalo.

### 2.2 Ejemplos resueltos

**Ejemplo 2.1 (Resolución directa):**
Resolver $3x - 5 < 7$.

**Solución:**
Despejamos $x$ paso a paso:
$$\begin{align}
3x - 5 &< 7 \\
3x &< 7 + 5 \\
3x &< 12 \\
x &< \dfrac{12}{3} \\
x &< 4
\end{align}$$

**Respuesta:** El conjunto solución está formado por todos los números estrictamente menores a 4. En notación de intervalo: $(-\infty, 4)$. De forma grafica seria
![[inercuaciones_ejemplo1.png]]

**Ejemplo 2.2 (Multiplicación por negativo):**
Resolver $-2x + 3 \geq 11$.

**Solución:**
$$\begin{align}
-2x + 3 &\geq 11 \\
-2x &\geq 11 - 3 \\
-2x &\geq 8 \\
x &\leq \frac{8}{-2} \quad \text{(se invierte el orden al dividir por -2)} \\
x &\leq -4
\end{align}$$

**Respuesta:** En notación de intervalo: $(-\infty, -4]$.

**Ejemplo 2.3 (Inecuación con fracciones):**
Resolver $\dfrac{x + 2}{3} - \dfrac{x - 1}{2} > 1$.

**Solución:**
Primero, eliminamos los denominadores multiplicando toda la inecuación por el mínimo común múltiplo (MCM) de 3 y 2, que es 6. Como 6 es positivo, el sentido de la desigualdad se mantiene.
$$\begin{align}
6 \cdot \left( \frac{x + 2}{3} - \frac{x - 1}{2} \right) &> 6 \cdot (1) \\
2(x + 2) - 3(x - 1) &> 6 \\
2x + 4 - 3x + 3 &> 6 \\
-x + 7 &> 6 \\
-x &> 6 - 7 \\
-x &> -1 \\
x &< 1 \quad \text{(se multiplica por -1 y se invierte el orden)}
\end{align}$$

**Respuesta:** En notación de intervalo: $(-\infty, 1)$.

En muchas situaciones prácticas, no es suficiente con saber si una variable supera un límite inferior o si es menor que un tope máximo, sino que se requiere que se mantenga estrictamente confinada entre ambos extremos. Pensemos, por ejemplo, en la temperatura óptima para conservar un medicamento, la cual debe estar por encima de los $2\ ^\circ\text{C}$ pero sin sobrepasar los $8\ ^\circ\text{C}$. Del mismo modo, en problemas algebraicos, a menudo se busca que una expresión esté acotada simultáneamente entre dos valores límite. A este tipo de relaciones de confinamiento se las conoce como inecuaciones de doble desigualdad.

**Definición 2.2 (Inecuación Simultánea o de Doble Desigualdad):**
Una inecuación de doble desigualdad (o inecuación simultánea) en una variable $x$ es una expresión equivalente a:
$$g(x) < f(x) \leq h(x)$$
la cual representa la conjunción lógica de dos inecuaciones independientes que deben cumplirse de manera simultánea:
$$(g(x) < f(x)) \land (f(x) \leq h(x))$$

Para inecuaciones lineales donde la expresión central es de primer grado, de la forma $a < bx + c \leq d$ (con $b \neq 0$), el conjunto solución se puede determinar de manera directa aislando la variable $x$. Esto se logra aplicando operaciones aritméticas uniformes de forma simultánea en los tres miembros de la desigualdad.

**Ejemplo 2.4 (Inecuación simultánea o de doble desigualdad):**
Resolver $-3 < 2x + 1 \leq 7$.

**Solución:**
En este caso se presenta una inecuación simultánea, la cual exige que la expresión central $2x + 1$ satisfaga dos condiciones al mismo tiempo. El despeje de la variable $x$ se puede realizar operando de forma simultánea en los tres miembros de la desigualdad:
$$\begin{align}
-3 &< 2x + 1 \leq 7 \\[6pt]
-3 - 1 &< 2x \leq 7 - 1 \quad \text{(se resta } 1 \text{ en cada miembro)} \\[6pt]
-4 &< 2x \leq 6 \\[6pt]
\dfrac{-4}{2} &< x \leq \dfrac{6}{2} \quad \text{(se divide entre } 2 \text{, manteniendo el orden)} \\[6pt]
-2 &< x \leq 3
\end{align}$$

**Respuesta:** El conjunto solución es la región acotada abierta por la izquierda y cerrada por la derecha. En notación de intervalo: $S = (-2, 3]$.

**Aplicaciones:**

Las inecuaciones lineales son el modelo algebraico directo de cualquier problema de restricciones de primer grado. En economía, el análisis de punto de equilibrio se reduce a determinar para qué volumen de producción $x$ los ingresos $I(x) = px$ superan a los costos $C(x) = cx + F$: la inecuación $px > cx + F$ es lineal en $x$ y su solución es el umbral mínimo de producción rentable. En ingeniería, las condiciones de resistencia de materiales —"la tensión de trabajo no debe superar el límite de fluencia"— generan inecuaciones lineales sobre las variables de diseño. La **programación lineal**, que busca maximizar o minimizar una función objetivo bajo múltiples restricciones simultáneas, trabaja exclusivamente con sistemas de inecuaciones lineales; cada restricción del problema corresponde a una inecuación de la forma $\mathbf{a}_i \cdot \mathbf{x} \leq b_i$.

---
## 3. Inecuaciones Cuadráticas

A diferencia de las inecuaciones lineales, en las cuadráticas el comportamiento de la expresión $ax^2 + bx + c$ cambia de signo en distintas regiones de la recta real. La estrategia de "despejar $x$" ya no es suficiente: en su lugar, se debe analizar dónde la expresión es positiva y dónde es negativa. La herramienta central para esto es la **tabla de signos**, cuya construcción depende de conocer las raíces del polinomio cuadrático.

> **Nota histórica:** Los antecedentes de la fórmula cuadrática $x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$ se remontan a las tablillas babilónicas (c. 2000 a.C.), donde los escribas resolvían problemas equivalentes a ecuaciones de segundo grado mediante procedimientos geométricos de completación del cuadrado. La formulación algebraica sistemática fue desarrollada por Al-Khwarizmi en su *Kitab al-mukhtasar fi hisab al-jabr wa-l-muqabala* (c. 820 d.C.), obra cuyo título dio origen a la palabra "álgebra". El papel del discriminante $\Delta = b^2 - 4ac$ como clasificador del número y tipo de raíces fue articulado progresivamente durante los siglos XVI y XVII en el contexto del análisis algebraico de polinomios, a través del trabajo de matemáticos como Cardano, Vieta y Descartes.

**Definición 3.1 (Inecuación Cuadrática):**
Una inecuación cuadrática en una variable $x$ es toda inecuación equivalente a alguna de las formas:
$$ax^2 + bx + c < 0, \quad ax^2 + bx + c \leq 0, \quad ax^2 + bx + c > 0, \quad ax^2 + bx + c \geq 0$$
con $a, b, c \in \mathbb{R}$ y $a \neq 0$. Se denomina cuadrática porque el término de mayor grado es $ax^2$.

**Definición 3.2 (Puntos Críticos):**
Los puntos críticos de una inecuación cuadrática son las raíces reales del polinomio $ax^2 + bx + c$, es decir, los valores $x_0 \in \mathbb{R}$ tales que $ax_0^2 + bx_0 + c = 0$. Estos puntos dividen la recta real en intervalos dentro de los cuales la expresión no cambia de signo.

> **Observación:** El número de puntos críticos depende del discriminante $\Delta = b^2 - 4ac$. Si $\Delta > 0$ hay dos raíces reales distintas; si $\Delta = 0$ hay una raíz doble; si $\Delta < 0$ no hay raíces reales y la expresión tiene signo constante en todo $\mathbb{R}$.

### 3.1 Método de los puntos críticos (Tabla de signos)
 
El procedimiento estándar para resolver una inecuación cuadrática es:
 
1. **Agrupar:** Llevar todos los términos a un miembro, dejando cero en el otro: $ax^2 + bx + c \lessgtr 0$.
2. **Encontrar los puntos críticos:** Resolver $ax^2 + bx + c = 0$ mediante factorización o la fórmula cuadrática $x = \dfrac{-b \pm \sqrt{\Delta}}{2a}$. Sean $x_1 < x_2$ las dos raíces obtenidas.
3. **Construir la tabla de signos:** Dividir $\mathbb{R}$ en intervalos usando los puntos críticos. En cada intervalo, evaluar el signo de cada factor y del producto total. Los puntos críticos $x_1$ y $x_2$ dividen la recta real en tres regiones disjuntas:
$$(-\infty,\, x_1), \qquad (x_1,\, x_2), \qquad (x_2,\, \infty)$$
Dentro de cada región, cada factor lineal $(x - x_1)$ y $(x - x_2)$ mantiene un signo constante. Para determinarlo, basta evaluar un punto de prueba cualquiera dentro del intervalo —no es necesario calcular el valor exacto, solo el signo.
La tabla tiene la siguiente estructura general:
 
| Intervalo | $(-\infty, x_1)$ | $x_1$ | $(x_1, x_2)$ | $x_2$ | $(x_2, \infty)$ |
| :--- | :---: | :---: | :---: | :---: | :---: |
| $(x - x_1)$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| $(x - x_2)$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $(x-x_1)(x-x_2)$ | $+$ | $0$ | $-$ | $0$ | $+$ |
 
Se leen los signos de la siguiente manera:
- El factor $(x - x_1)$ es negativo a la izquierda de $x_1$, se anula en $x_1$, y es positivo a su derecha.
- El factor $(x - x_2)$ es negativo a la izquierda de $x_2$, se anula en $x_2$, y es positivo a su derecha.
- El signo del producto $(x-x_1)(x-x_2)$ se obtiene multiplicando los signos de cada fila: $(-)\cdot(-) = +$, $(-)\cdot(+) = -$, $(+)\cdot(+) = +$.
> **Nota:** En la tabla se incluyen las columnas de $x_1$ y $x_2$ para registrar explícitamente que ambos factores se anulan ahí. Si la inecuación es estricta ($<$ o $>$), esos puntos se excluyen del conjunto solución; si incluye igualdad ($\leq$ o $\geq$), se incluyen.
 
4. **Seleccionar:** Elegir los intervalos cuyo signo satisface la desigualdad original, incluyendo o excluyendo los puntos críticos según el símbolo.

### 3.2 Ejemplos resueltos
 
**Ejemplo 3.1 (Dos raíces reales distintas, $\Delta > 0$):**
Resolver $x^2 - 5x + 6 < 0$.
 
**Solución:**
Se factoriza el polinomio:
$$(x - 2)(x - 3) < 0$$
 
Los puntos críticos son $x = 2$ y $x = 3$. Se construye la tabla de signos:
 
| Intervalo       | $(-\infty, 2)$ | $(2, 3)$ | $(3, \infty)$ |
| :---            | :---:          | :---:    | :---:         |
| $(x - 2)$       | $-$            | $+$      | $+$           |
| $(x - 3)$       | $-$            | $-$      | $+$           |
| $(x-2)(x-3)$    | $+$            | $-$      | $+$           |
 
Se busca la región de signo negativo. Como la desigualdad es estricta ($< 0$), los puntos críticos se excluyen.
 
**Respuesta:** $S = (2, 3)$.
 
> **Observación:** Geométricamente, esto equivale a encontrar los valores de $x$ para los cuales la parábola $y = x^2 - 5x + 6$ se sitúa por debajo del eje $X$.

**Ejemplo 3.2 (Raíz doble, $\Delta = 0$):**
Resolver $x^2 - 4x + 4 \leq 0$.
 
**Solución:**
Se reconoce un cuadrado perfecto:
$$(x - 2)^2 \leq 0$$
 
Para todo $x \in \mathbb{R}$ se cumple $(x-2)^2 \geq 0$, por lo que la expresión nunca puede ser negativa. La única posibilidad es la igualdad, que ocurre en $x = 2$:
$$\begin{align}
(x - 2)^2 &= 0 \\
x &= 2
\end{align}$$
 
**Respuesta:** $S = \{2\}$.
 
> **Observación:** La parábola $y = (x-2)^2$ es tangente al eje $X$ en $x = 2$ y permanece por encima de él en todo otro punto. La inecuación $\leq 0$ solo se satisface en ese único punto de tangencia.
 
**Ejemplo 3.3 (Sin raíces reales, $\Delta < 0$):**
Resolver $x^2 + x + 1 > 0$.
 
**Solución:**
Se calcula el discriminante:
$$\Delta = 1^2 - 4 \cdot 1 \cdot 1 = 1 - 4 = -3 < 0$$
 
Como $\Delta < 0$, el polinomio no tiene raíces reales y no puede factorizarse sobre $\mathbb{R}$. Al ser $a = 1 > 0$, la parábola $y = x^2 + x + 1$ abre hacia arriba y nunca toca el eje $X$: la expresión es estrictamente positiva para todo $x \in \mathbb{R}$.
 
**Respuesta:** $S = \mathbb{R}$.
 
> **Observación:** Si la inecuación hubiera sido $x^2 + x + 1 < 0$, el conjunto solución sería $\emptyset$, ya que la expresión es siempre positiva. Este caso ilustra que el análisis del discriminante puede resolver la inecuación sin necesidad de tabla de signos.

**Ejemplo 3.4 (Coeficiente cuadrático negativo, $a < 0$):**
Resolver $-2x^2 + 5x + 3 \geq 0$.

**Solución:**
Cuando el coeficiente cuadrático es negativo, es sumamente recomendable multiplicar toda la inecuación por $-1$ para convertirlo en positivo y simplificar la factorización. Al realizar esta operación, se debe invertir el sentido del símbolo de desigualdad:
$$\begin{align}
-2x^2 + 5x + 3 &\geq 0 \quad \Big/ \cdot (-1) \\[6pt]
2x^2 - 5x - 3 &\leq 0
\end{align}$$

Ahora procedemos a factorizar el polinomio cuadrático $2x^2 - 5x - 3$. Buscamos dos números que multiplicados den $-6$ (producto de $2 \cdot (-3)$) y sumados den $-5$. Estos números son $-6$ y $1$. Reescribimos el término central:
$$\begin{align}
2x^2 - 6x + x - 3 &\leq 0 \\[6pt]
2x(x - 3) + 1(x - 3) &\leq 0 \\[6pt]
(2x + 1)(x - 3) &\leq 0
\end{align}$$

Los puntos críticos se obtienen igualando cada factor a cero:
- $2x + 1 = 0 \implies x = -\dfrac{1}{2}$
- $x - 3 = 0 \implies x = 3$

Construimos la tabla de signos correspondiente:

| Intervalo | $\left(-\infty, -\dfrac{1}{2}\right)$ | $-\dfrac{1}{2}$ | $\left(-\dfrac{1}{2}, 3\right)$ | $3$ | $(3, \infty)$ |
| :--- | :---: | :---: | :---: | :---: | :---: |
| $(2x + 1)$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| $(x - 3)$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $(2x+1)(x-3)$ | $+$ | $0$ | $-$ | $0$ | $+$ |

Buscamos la región de signo negativo o nulo ($\leq 0$) según la inecuación transformada. Dado que el símbolo incluye la igualdad, los puntos críticos se incorporan en la solución.

**Respuesta:** En notación de intervalo: $S = \left[-\dfrac{1}{2}, 3\right]$.

> **Observación:** Si se hubiera optado por trabajar con el polinomio original sin multiplicar por $-1$, la tabla de signos habría arrojado idéntico resultado, pero requiriendo evaluar factores con coeficientes negativos (como $-2x - 1$ o similar), lo cual aumenta la probabilidad de incurrir en un error de signo.

**Ejemplo 3.5 (Puntos críticos irracionales):**
Resolver $x^2 - 2x - 4 > 0$.

**Solución:**
Intentamos factorizar por inspección, pero no existen números enteros sencillos que satisfagan la condición. Por lo tanto, calculamos las raíces mediante la fórmula general cuadrática:
$$x = \dfrac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

Sustituyendo los coeficientes $a = 1$, $b = -2$, y $c = -4$:
$$\begin{align}
x &= \dfrac{-(-2) \pm \sqrt{(-2)^2 - 4(1)(-4)}}{2(1)} \\[6pt]
x &= \dfrac{2 \pm \sqrt{4 + 16}}{2} \\[6pt]
x &= \dfrac{2 \pm \sqrt{20}}{2} \\[6pt]
x &= \dfrac{2 \pm 2\sqrt{5}}{2} \\[6pt]
x &= 1 \pm \sqrt{5}
\end{align}$$

Los puntos críticos son:
$$x_1 = 1 - \sqrt{5} \quad (\approx -1.24) \quad \text{y} \quad x_2 = 1 + \sqrt{5} \quad (\approx 3.24)$$

Se reescribe la inecuación en su forma factorizada:
$$\left(x - (1 - \sqrt{5})\right)\left(x - (1 + \sqrt{5})\right) > 0$$

Dividimos la recta real empleando los puntos críticos irracionales y construimos la tabla de signos correspondientes:

| Intervalo | $(-\infty, 1-\sqrt{5})$ | $1-\sqrt{5}$ | $(1-\sqrt{5}, 1+\sqrt{5})$ | $1+\sqrt{5}$ | $(1+\sqrt{5}, \infty)$ |
| :--- | :---: | :---: | :---: | :---: | :---: |
| $\left(x - (1-\sqrt{5})\right)$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| $\left(x - (1+\sqrt{5})\right)$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $\text{Producto}$ | $+$ | $0$ | $-$ | $0$ | $+$ |

Buscamos los intervalos donde el producto es estrictamente positivo ($> 0$). Dado que la desigualdad es estricta, los puntos críticos se excluyen.

**Respuesta:** En notación de intervalo: $S = (-\infty, 1 - \sqrt{5}) \cup (1 + \sqrt{5}, \infty)$.

**Aplicaciones:**
Las inecuaciones cuadráticas aparecen de forma natural en todo contexto donde intervienen funciones de segundo grado o expresiones bajo una raíz cuadrada. El dominio de la función $f(x) = \sqrt{g(x)}$ se determina resolviendo la inecuación $g(x) \geq 0$; cuando $g$ es cuadrática, la tabla de signos produce la respuesta directamente. En física, la condición de que un proyectil se encuentre sobre el nivel del suelo se reduce a $h(t) = -\frac{1}{2}g\, t^2 + v_0\, t > 0$, una inecuación cuadrática en $t$ cuya solución da el intervalo de tiempo de vuelo. En Cálculo diferencial, el análisis de concavidad de una función $f$ exige determinar los intervalos donde $f''(x) > 0$ (concavidad hacia arriba) o $f''(x) < 0$ (concavidad hacia abajo): cuando $f''$ es polinomial, la tabla de signos es la herramienta directa. En economía, las funciones de utilidad y costo cuadráticas generan inecuaciones de este tipo al determinar las condiciones de rentabilidad positiva.

---
## 4. Inecuaciones Racionales
 
Hasta ahora, los puntos críticos de una inecuación eran únicamente los ceros del polinomio: los valores donde la expresión se anula. En las inecuaciones racionales aparece un nuevo tipo de punto crítico que no anula la expresión, sino que la hace **indefinida**: los ceros del denominador. Estos puntos también dividen la recta real en regiones de signo constante, pero a diferencia de las raíces del numerador, nunca pueden pertenecer al conjunto solución.
 
**Definición 4.1 (Inecuación Racional):**
Una inecuación racional en una variable $x$ es toda inecuación de la forma:
$$\frac{P(x)}{Q(x)} < 0, \quad \frac{P(x)}{Q(x)} \leq 0, \quad \frac{P(x)}{Q(x)} > 0, \quad \frac{P(x)}{Q(x)} \geq 0$$
donde $P(x)$ y $Q(x)$ son polinomios con $Q(x) \not\equiv 0$. El dominio natural de la inecuación es $\{x \in \mathbb{R} : Q(x) \neq 0\}$.
 
**Definición 4.2 (Puntos Críticos de una Inecuación Racional):**
Los puntos críticos son todos los valores $x_0 \in \mathbb{R}$ que anulan el numerador o el denominador, es decir, las soluciones de $P(x_0) = 0$ o $Q(x_0) = 0$. Se clasifican en dos categorías:
 
- **Puntos tipo I (raíces del numerador):** Anulan la expresión. Pueden pertenecer al conjunto solución si el símbolo incluye igualdad ($\leq$ o $\geq$).
- **Puntos tipo II (raíces del denominador):** Hacen la expresión indefinida. Están **excluidos del dominio** y nunca pertenecen al conjunto solución, independientemente del símbolo de desigualdad.

### 4.1 Método de resolución
 
El procedimiento es análogo al de las inecuaciones cuadráticas, con dos pasos adicionales:
 
1. **Agrupar:** Llevar todos los términos a un miembro dejando cero en el otro. Si hay términos con distinto denominador, combinarlos en una sola fracción mediante mínimo común denominador.
2. **Identificar los puntos críticos:** Encontrar las raíces de $P(x)$ y de $Q(x)$ por separado.
3. **Construir la tabla de signos:** Incluir ambos tipos de puntos críticos para seccionar la recta real. Analizar el signo de $P(x)$ y $Q(x)$ en cada intervalo y determinar el signo del cociente.
4. **Seleccionar:** Elegir los intervalos cuyo signo satisface la desigualdad. Incluir los puntos tipo I si el símbolo tiene igualdad; excluir siempre los puntos tipo II.
> **Advertencia:** Un error frecuente es multiplicar ambos miembros de la inecuación por $Q(x)$ para eliminar el denominador. Esto es incorrecto porque el signo de $Q(x)$ no es constante en todo $\mathbb{R}$: puede ser positivo en algunos intervalos y negativo en otros, lo que obligaría a invertir el símbolo en unos casos y conservarlo en otros. El método correcto es siempre la tabla de signos.
 
### 4.2 Ejemplos resueltos
 
**Ejemplo 4.1 (Forma estándar directa):**
Resolver $\dfrac{x + 1}{x - 2} \geq 0$.
 
**Solución:**
La inecuación ya está en forma estándar. Se identifican los puntos críticos:
- **Tipo I** (numerador): $x + 1 = 0 \implies x = -1$
- **Tipo II** (denominador): $x - 2 = 0 \implies x = 2$
Se construye la tabla de signos:
 
| Intervalo | $(-\infty, -1)$ | $-1$ | $(-1, 2)$ | $2$ | $(2, \infty)$ |
| :--- | :---: | :---: | :---: | :---: | :---: |
| $(x + 1)$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| $(x - 2)$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $\dfrac{x+1}{x-2}$ | $+$ | $0$ | $-$ | $\nexists$ | $+$ |
 
Se buscan las regiones con signo positivo o nulo ($\geq 0$):
- $(-\infty, -1)$: signo $+$ ✓
- $x = -1$: el cociente vale $0$, permitido por $\geq$ ✓ (Tipo I, se incluye)
- $(-1, 2)$: signo $-$ ✗
- $x = 2$: indefinido, prohibido (Tipo II, se excluye siempre)
- $(2, \infty)$: signo $+$ ✓
**Respuesta:** $S = (-\infty, -1] \cup (2, \infty)$.
 
**Ejemplo 4.2 (Requiere agrupar antes de la tabla):**
Resolver $\dfrac{x + 3}{x - 1} \leq 2$.
 
**Solución:**
La inecuación no está en forma estándar: hay un término $2$ en el miembro derecho. Se lleva todo al miembro izquierdo y se combina en una sola fracción:
$$\begin{align}
\frac{x + 3}{x - 1} - 2 &\leq 0 \\[6pt]
\frac{x + 3}{x - 1} - \frac{2(x-1)}{x - 1} &\leq 0 \\[6pt]
\frac{x + 3 - 2(x - 1)}{x - 1} &\leq 0 \\[6pt]
\frac{x + 3 - 2x + 2}{x - 1} &\leq 0 \\[6pt]
\frac{-x + 5}{x - 1} &\leq 0
\end{align}$$
 
Se identifican los puntos críticos:
- **Tipo I** (numerador): $-x + 5 = 0 \implies x = 5$
- **Tipo II** (denominador): $x - 1 = 0 \implies x = 1$
Se construye la tabla de signos:
 
| Intervalo | $(-\infty, 1)$ | $1$ | $(1, 5)$ | $5$ | $(5, \infty)$ |
| :--- | :---: | :---: | :---: | :---: | :---: |
| $(-x + 5)$ | $+$ | $+$ | $+$ | $0$ | $-$ |
| $(x - 1)$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| $\dfrac{-x+5}{x-1}$ | $-$ | $\nexists$ | $+$ | $0$ | $-$ |
 
Se buscan las regiones con signo negativo o nulo ($\leq 0$):
- $(-\infty, 1)$: signo $-$ ✓
- $x = 1$: indefinido, excluido (Tipo II) ✗
- $(1, 5)$: signo $+$ ✗
- $x = 5$: el cociente vale $0$, permitido por $\leq$ ✓ (Tipo I, se incluye)
- $(5, \infty)$: signo $-$ ✓
**Respuesta:** $S = (-\infty, 1) \cup [5, \infty)$.
 
> **Observación:** El paso de agrupar todo en un solo cociente antes de la tabla es obligatorio. Si se hubiera multiplicado ambos miembros por $(x-1)$ directamente, el signo de ese factor es desconocido y la inversión del símbolo sería incorrecta en alguno de los intervalos.

**Ejemplo 4.3 (Prohibición de multiplicar cruzado):**
Resolver $\dfrac{x}{x-2} \geq \dfrac{3}{x+1}$.
 
> **Advertencia (El error de multiplicar cruzado):**
> Al ver esta inecuación, la tentación es "multiplicar en cruz" (como si fuera una ecuación), obteniendo $x(x+1) \geq 3(x-2)$. **¡Esto es un error grave!**
> Al hacer esto, se asume implícitamente que $(x-2)$ y $(x+1)$ son positivos. Si alguno de ellos fuera negativo, el símbolo $\geq$ debería haberse invertido. Como ambos denominadores cambian de signo dependiendo del valor de $x$, la multiplicación cruzada destruye la inecuación original y produce resultados completamente erróneos.
 
**Solución Correcta:**
Siempre debemos trasladar todos los términos a un solo miembro de la inecuación para comparar con cero, y luego usar el mínimo común múltiplo.
$$\begin{align}
\frac{x}{x - 2} - \frac{3}{x + 1} &\geq 0 \\[6pt]
\frac{x(x + 1) - 3(x - 2)}{(x - 2)(x + 1)} &\geq 0 \\[6pt]
\frac{x^2 + x - 3x + 6}{(x - 2)(x + 1)} &\geq 0 \\[6pt]
\frac{x^2 - 2x + 6}{(x - 2)(x + 1)} &\geq 0
\end{align}$$

Identificamos los puntos críticos:
- **Tipo I (numerador):** $x^2 - 2x + 6 = 0$. Su discriminante es $\Delta = (-2)^2 - 4(1)(6) = 4 - 24 = -20 < 0$. Al ser $\Delta < 0$ y el coeficiente principal positivo, el numerador nunca se anula y es estrictamente **positivo** ($+$) para todo $x \in \mathbb{R}$.
- **Tipo II (denominador):** $x - 2 = 0 \implies x = 2$, y $x + 1 = 0 \implies x = -1$.

Construimos la tabla de signos usando únicamente los puntos críticos del denominador, ya que el numerador siempre es positivo:

| Intervalo | $(-\infty, -1)$ | $-1$ | $(-1, 2)$ | $2$ | $(2, \infty)$ |
| :--- | :---: | :---: | :---: | :---: | :---: |
| $(x^2 - 2x + 6)$ | $+$ | $+$ | $+$ | $+$ | $+$ |
| $(x - 2)$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $(x + 1)$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| $\text{Cociente}$ | $+$ | $\nexists$ | $-$ | $\nexists$ | $+$ |

Buscamos las regiones con signo positivo o nulo ($\geq 0$):
- $(-\infty, -1)$: signo $+$ ✓
- $x = -1$: indefinido (Tipo II, se excluye siempre) ✗
- $(-1, 2)$: signo $-$ ✗
- $x = 2$: indefinido (Tipo II, se excluye siempre) ✗
- $(2, \infty)$: signo $+$ ✓

**Respuesta:** $S = (-\infty, -1) \cup (2, \infty)$.

**Desarrollo erróneo (multiplicando en cruz):**
Si se procede de manera incorrecta realizando la multiplicación cruzada de los denominadores (omitiendo la variación de sus signos), se obtiene el siguiente desarrollo:
$$\begin{align}
x(x + 1) &\geq 3(x - 2) \\[6pt]
x^2 + x &\geq 3x - 6 \\[6pt]
x^2 - 2x + 6 &\geq 0
\end{align}$$

Al estudiar la expresión cuadrática $x^2 - 2x + 6$, se calcula su discriminante:
$$\Delta = (-2)^2 - 4(1)(6) = -20$$

Dado que el discriminante es negativo ($\Delta < 0$) y el coeficiente principal es positivo ($1 > 0$), la parábola asociada no corta el eje de las abscisas y se mantiene estrictamente por encima de este. Por lo tanto, la inecuación cuadrática se cumple para cualquier valor real de $x$, lo que conduciría al conjunto solución incorrecto:
$$S_{\text{erróneo}} = \mathbb{R}$$

**Demostración de la inconsistencia:**
Para comprobar que este conjunto solución es incorrecto, basta con evaluar un valor de $x$ perteneciente a $S_{\text{erróneo}}$ que no pertenezca al conjunto solución correcto $S = (-\infty, -1) \cup (2, \infty)$.

Tomando $x = 0 \in S_{\text{erróneo}}$ y sustituyendo en la inecuación original:
$$\dfrac{0}{0 - 2} \geq \dfrac{3}{0 + 1} \implies 0 \geq 3$$

Se llega a una contradicción aritmética directa, pues $0$ no es mayor ni igual a $3$. 

De igual forma, evaluando $x = 1 \in S_{\text{erróneo}}$:
$$\dfrac{1}{1 - 2} \geq \dfrac{3}{1 + 1} \implies -1 \geq \dfrac{3}{2}$$

Lo cual también constituye una falsedad. Esto evidencia que la multiplicación cruzada elimina las restricciones impuestas por los denominadores y no conserva la relación de orden original.

**Ejemplo 4.4 (Numerador cuadrático factorizable):**
Resolver $\dfrac{x^2 - x - 6}{x - 1} \leq 0$.

**Solución:**
La inecuación ya está en forma estándar (comparada con cero). Para facilitar el análisis de signos, factorizamos el trinomio cuadrático del numerador buscando dos números que multiplicados resulten en $-6$ y sumados den $-1$. Estos números son $-3$ y $2$:
$$\dfrac{(x - 3)(x + 2)}{x - 1} \leq 0$$

Identificamos los puntos críticos de la inecuación:
- **Puntos tipo I (numerador):** $(x - 3)(x + 2) = 0 \implies x = 3 \quad \text{y} \quad x = -2$.
- **Puntos tipo II (denominador):** $x - 1 = 0 \implies x = 1$.

Estos puntos ordenados de menor a mayor ($-2 < 1 < 3$) dividen la recta real en cuatro intervalos. Construimos la tabla de signos evaluando cada factor lineal de manera independiente:

| Intervalo | $(-\infty, -2)$ | $-2$ | $(-2, 1)$ | $1$ | $(1, 3)$ | $3$ | $(3, \infty)$ |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| $(x + 2)$ | $-$ | $0$ | $+$ | $+$ | $+$ | $+$ | $+$ |
| $(x - 1)$ | $-$ | $-$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| $(x - 3)$ | $-$ | $-$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $\text{Cociente}$ | $-$ | $0$ | $+$ | $\nexists$ | $-$ | $0$ | $+$ |

Buscamos las regiones con signo negativo o nulo ($\leq 0$):
- $(-\infty, -2)$: signo $-$ ✓
- $x = -2$: permitido, el cociente vale $0$ (punto tipo I, se incluye) ✓
- $(-2, 1)$: signo $+$ ✗
- $x = 1$: indefinido, prohibido por anular el denominador (punto tipo II, se excluye siempre) ✗
- $(1, 3)$: signo $-$ ✓
- $x = 3$: permitido, el cociente vale $0$ (punto tipo I, se incluye) ✓
- $(3, \infty)$: signo $+$ ✗

**Respuesta:** En notación de intervalo: $S = (-\infty, -2] \cup (1, 3]$.

---
## 5. Otras Inecuaciones No Lineales (Orden Superior, Irracionales y Trascendentes)

En la práctica del cálculo y en aplicaciones de modelación matemática, las restricciones raramente se limitan a relaciones lineales, cuadráticas o fraccionarias simples. Fenómenos físicos como el volumen de cuerpos geométricos optimizados, la velocidad de escape en campos gravitatorios, el crecimiento de poblaciones o la atenuación de ondas conducen a inecuaciones polinómicas de tercer grado o mayor (orden superior), a inecuaciones con radicales (irracionales) o a inecuaciones que involucran funciones exponenciales, logarítmicas o trigonométricas (trascendentes).

Aunque estas inecuaciones pueden parecer complejas a primera vista, los principios fundamentales para su resolución siguen siendo los mismos: establecer el dominio de validez en los números reales y analizar el signo de las expresiones resultantes.

### 5.1 Inecuaciones Polinómicas de Orden Superior

**Definición 5.1 (Inecuación de orden superior):**
Una inecuación polinómica de orden superior es una desigualdad de la forma:
$$P(x) \gtrless 0$$
donde $P(x) = a_n x^n + a_{n-1} x^{n-1} + \dots + a_1 x + a_0$ es un polinomio de grado $n \geq 3$ con coeficientes reales, y el símbolo de relación representa cualquiera de los operadores $\{<, >, \leq, \geq\}$.

El método estándar para resolverlas consiste en factorizar el polinomio en sus términos lineales y cuadráticos irreducibles (utilizando técnicas como Ruffini, factor común o teoremas de raíces de polinomios) para luego realizar una tabla de signos con los puntos críticos obtenidos.

**Ejemplo 5.1 (Polinómica de tercer grado):**
Resolver el conjunto solución de la inecuación:
$$x^3 - 2x^2 - 5x + 6 \geq 0$$

**Solución:**
En primer lugar, se busca factorizar el polinomio de tercer grado $P(x) = x^3 - 2x^2 - 5x + 6$. Evaluando divisores del término independiente $6$ mediante el teorema del resto, se verifica que para $x = 1$:
$$P(1) = 1^3 - 2(1)^2 - 5(1) + 6 = 1 - 2 - 5 + 6 = 0$$

Al ser $x = 1$ una raíz, aplicamos la división sintética (regla de Ruffini) para factorizar el polinomio:
$$\begin{array}{r|rrrr}
  & 1 & -2 & -5 & 6 \\
1 &   &  1 & -1 & -6 \\
\hline
  & 1 & -1 & -6 & 0
\end{array}$$

El polinomio remanente es $x^2 - x - 6$, el cual se factoriza directamente como $(x - 3)(x + 2)$. De este modo, la inecuación se reescribe en su forma factorizada:
$$(x - 1)(x - 3)(x + 2) \geq 0$$

Los puntos críticos corresponden a las raíces del polinomio:
- $x = 1$
- $x = 3$
- $x = -2$

Estos puntos dividen la recta real en cuatro intervalos. Construimos la tabla de signos evaluando cada factor lineal de manera independiente:

| Intervalo | $(-\infty, -2)$ | $-2$ | $(-2, 1)$ | $1$ | $(1, 3)$ | $3$ | $(3, \infty)$ |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| $(x + 2)$ | $-$ | $0$ | $+$ | $+$ | $+$ | $+$ | $+$ |
| $(x - 1)$ | $-$ | $-$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| $(x - 3)$ | $-$ | $-$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $\text{Producto}$ | $-$ | $0$ | $+$ | $0$ | $-$ | $0$ | $+$ |

Buscamos las regiones con signo positivo o nulo ($\geq 0$):
- $(-\infty, -2)$: signo $-$ ✗
- $x = -2$: permitido, el producto vale $0$ (se incluye) ✓
- $(-2, 1)$: signo $+$ ✓
- $x = 1$: permitido, el producto vale $0$ (se incluye) ✓
- $(1, 3)$: signo $-$ ✗
- $x = 3$: permitido, el producto vale $0$ (se incluye) ✓
- $(3, \infty)$: signo $+$ ✓

**Respuesta:** En notación de intervalo: $S = [-2, 1] \cup [3, \infty)$.

### 5.2 Inecuaciones Irracionales

Pensemos en el cálculo de la velocidad de un objeto que cae en un campo gravitatorio o en el diseño de un canal hidráulico: estas situaciones físicas involucran leyes de potencia y raíces. Al modelar restricciones de desigualdad sobre estas variables, se llega a inecuaciones irracionales.

La dificultad de estas inecuaciones radica en que la operación de elevar a una potencia par no es inyectiva en el dominio de los números reales, lo que puede introducir soluciones extrañas o alterar el sentido de la desigualdad. Por lo tanto, se deben establecer con rigurosidad las condiciones de existencia de los radicales y analizar los signos de los miembros involucrados.

**Definición 5.2 (Inecuación irracional de índice par):**
Una inecuación irracional de índice par es una desigualdad de la forma general:
$$\sqrt{f(x)} \lessgtr g(x)$$
donde $f(x)$ y $g(x)$ son expresiones algebraicas con valores reales, y el símbolo de relación representa cualquiera de los operadores $\{<, >, \leq, \geq\}$.

Para resolver estas inecuaciones en el campo de los reales, el análisis se divide en dos casos fundamentales según el sentido de la desigualdad. Por simplicidad, la exposición se centra en la raíz cuadrada ($n=2$); el razonamiento se extiende de forma análoga a cualquier índice par.

#### 5.2.1 Caso I: Inecuaciones de la forma $\sqrt{f(x)} < g(x)$ (y $\sqrt{f(x)} \leq g(x)$)

Para que exista una solución real en esta clase de desigualdades, se deben cumplir tres condiciones simultáneas:
1. **Existencia del radicando:** La expresión dentro del radical debe ser no negativa ($f(x) \geq 0$).
2. **Signo del miembro derecho:** Dado que la raíz cuadrada principal es siempre no negativa ($\sqrt{f(x)} \geq 0$), la única posibilidad de que sea estrictamente menor que $g(x)$ es que esta última sea estrictamente positiva ($g(x) > 0$). Si $g(x) \leq 0$, la inecuación no posee solución real (su conjunto solución es vacío, $\emptyset$).
3. **Elevación al cuadrado:** Al ser ambos miembros no negativos, es válido elevar al cuadrado sin alterar la relación de orden: $f(x) < [g(x)]^2$.

Estas condiciones se traducen en el siguiente sistema de inecuaciones simultáneas:
$$\sqrt{f(x)} < g(x) \iff \begin{cases} f(x) \geq 0 \\ g(x) > 0 \\ f(x) < [g(x)]^2 \end{cases}$$

**Ejemplo 5.2 (Desigualdad menor que con miembro derecho constante):**
Resolver el conjunto solución de la inecuación $\sqrt{x + 5} < 3$.

**Solución:**
Se plantea el sistema de restricciones correspondiente para asegurar la validez de la desigualdad:
$$\begin{cases}
x + 5 \geq 0 & \text{(existencia del radicando)} \\
3 > 0 & \text{(miembro derecho positivo, siempre verdadero)} \\
x + 5 < 3^2 & \text{(elevación al cuadrado)}
\end{cases}$$

Resolvemos de manera independiente las condiciones variables:
- Para la primera condición: $x + 5 \geq 0 \implies x \geq -5$, lo que determina el conjunto $S_1 = [-5, \infty)$.
- Para la tercera condición: $x + 5 < 9 \implies x < 4$, lo que determina el conjunto $S_2 = (-\infty, 4)$.

El conjunto solución final $S$ de la inecuación irracional se obtiene de la intersección de ambas restricciones:
$$S = S_1 \cap S_2 = [-5, \infty) \cap (-\infty, 4) = [-5, 4)$$

**Respuesta:** En notación de intervalo: $S = [-5, 4)$.

#### 5.2.2 Caso II: Inecuaciones de la forma $\sqrt{f(x)} > g(x)$ (y $\sqrt{f(x)} \geq g(x)$)

En este escenario, el miembro derecho $g(x)$ no está obligado a ser positivo, lo que exige dividir el análisis en la unión de dos ramas lógicas mutuamente excluyentes según el signo de $g(x)$:

- **Rama A (Miembro derecho negativo):** Si $g(x) < 0$, la desigualdad $\sqrt{f(x)} > g(x)$ se cumple de forma directa para todo $x$ en el dominio de definición de la raíz, debido a que todo número no negativo es estrictamente mayor que cualquier número negativo. El sistema asociado es:
  $$\begin{cases} f(x) \geq 0 \\ x \in \text{Dom}(g) \text{ tal que } g(x) < 0 \end{cases}$$
- **Rama B (Miembro derecho no negativo):** Si $g(x) \geq 0$, ambos miembros son no negativos y es posible elevar al cuadrado conservando el sentido de la desigualdad: $f(x) > [g(x)]^2$. La condición de existencia de la raíz ($f(x) \geq 0$) se cumple automáticamente por transitividad, dado que $f(x) > [g(x)]^2 \geq 0$. El sistema asociado es:
  $$\begin{cases} g(x) \geq 0 \\ f(x) > [g(x)]^2 \end{cases}$$

La solución final es la unión de los conjuntos solución obtenidos en ambas ramas:
$$\sqrt{f(x)} > g(x) \iff \Big( f(x) \geq 0 \ \land \ g(x) < 0 \Big) \ \lor \ \Big( g(x) \geq 0 \ \land \ f(x) > [g(x)]^2 \Big)$$

**Ejemplo 5.3 (Desigualdad mayor que con miembro derecho variable):**
Resolver la inecuación $\sqrt{x + 2} > x$.

**Solución:**
Aplicamos la descomposición en ramas lógicas para el miembro derecho $g(x) = x$:

1. **Rama A ($x < 0$):**
   Planteamos las condiciones de existencia de la raíz y negatividad de la variable:
   $$\begin{cases} x + 2 \geq 0 \implies x \geq -2 \\ x < 0 \end{cases}$$
   La intersección de estas dos condiciones determina la solución de esta rama:
   $$S_A = [-2, 0)$$

2. **Rama B ($x \geq 0$):**
   Planteamos las condiciones de no negatividad de la variable y elevación al cuadrado de la inecuación:
   $$\begin{cases} x \geq 0 \\ x + 2 > x^2 \end{cases}$$
   Resolvemos la desigualdad cuadrática resultante, $x^2 - x - 2 < 0$. Factorizando el polinomio:
   $$(x - 2)(x + 1) < 0$$

   Identificamos los puntos críticos: $x = -1$ y $x = 2$. Estos puntos dividen la recta real en tres intervalos, sobre los cuales analizamos el signo de cada factor lineal:

   | Intervalo | $(-\infty, -1)$ | $(-1, 2)$ | $(2, \infty)$ |
   | :--- | :---: | :---: | :---: |
   | $(x + 1)$ | $-$ | $+$ | $+$ |
   | $(x - 2)$ | $-$ | $-$ | $+$ |
   | $\text{Producto}$ | $+$ | $-$ | $+$ |

   Dado que buscamos los valores de $x$ para los cuales el producto es estrictamente negativo ($< 0$):
   - $(-\infty, -1)$: signo positivo (se excluye)
   - $x = -1$: el producto es cero (se excluye por ser desigualdad estricta)
   - $(-1, 2)$: signo negativo (se incluye) ✓
   - $x = 2$: el producto es cero (se excluye por ser desigualdad estricta)
   - $(2, \infty)$: signo positivo (se excluye)

   Por lo tanto, la solución de la inecuación cuadrática es el intervalo $(-1, 2)$. Al intersecar este conjunto con la restricción de esta rama ($x \geq 0$), se obtiene:
   $$S_B = (-1, 2) \cap [0, \infty) = [0, 2)$$

Finalmente, el conjunto solución general $S$ se obtiene mediante la unión de las soluciones de ambas ramas:
$$S = S_A \cup S_B = [-2, 0) \cup [0, 2) = [-2, 2)$$

**Respuesta:** En notación de intervalo: $S = [-2, 2)$.

### 5.3 Inecuaciones Trascendentes

Las inecuaciones trascendentes son aquellas donde la variable independiente figura como argumento de una función que no puede expresarse mediante sumas, productos o cocientes algebraicos finitos de polinomios, tales como las funciones exponenciales, logarítmicas o trigonométricas. 

La resolución de estas desigualdades no responde a un algoritmo universal, sino que se fundamenta en dos principios conceptuales del Análisis Matemático:
1. **La propiedad de monotonía:** Si una función es estrictamente creciente (como $f(x) = e^x$ o $f(x) = \ln(x)$), entonces preserva el orden de la desigualdad al aplicarse o removerse de ambos miembros. Si es estrictamente decreciente, invierte el sentido de la desigualdad.
2. **La periodicidad:** Las funciones trigonométricas repiten sus valores en ciclos regulares, por lo que resolver inecuaciones con senos o cosenos exige analizar el comportamiento en un período base y luego extender la solución a toda la recta real.

**Ejemplo 5.4 (Inecuación exponencial):**
Resolver la inecuación exponencial:
$$3^{2x - 1} \geq 9$$

**Solución:**
En primer lugar, expresamos el miembro derecho en base $3$:
$$3^{2x - 1} \geq 3^2$$

Dado que la función exponencial de base $b = 3$ es estrictamente creciente ($3 > 1$), se conserva el sentido del operador de desigualdad al comparar los exponentes directamente:
$$\begin{align}
2x - 1 &\geq 2 \\[6pt]
2x &\geq 3 \\[6pt]
x &\geq \dfrac{3}{2}
\end{align}$$

**Respuesta:** En notación de intervalo: $S = \left[\dfrac{3}{2}, \infty\right)$.

**Ejemplo 5.5 (Inecuación logarítmica):**
Resolver la inecuación logarítmica:
$$\ln(x - 2) < 0$$

**Solución:**
Para que la expresión logarítmica exista en el campo de los números reales, el argumento del logaritmo debe ser estrictamente positivo. Esto define la condición de dominio:
$$x - 2 > 0 \implies x > 2 \implies \text{Dom} = (2, \infty)$$

Una vez delimitado el dominio admisible, aplicamos la función exponencial de base $e$ en ambos miembros. Dado que $e \approx 2.718$ es mayor que $1$, la función exponencial es estrictamente creciente y preserva el sentido de la desigualdad:
$$\begin{align}
e^{\ln(x - 2)} &< e^0 \\[6pt]
x - 2 &< 1 \\[6pt]
x &< 3 \implies S_{\text{desigualdad}} = (-\infty, 3)
\end{align}$$

El conjunto solución final $S$ se determina mediante la intersección de la solución de la desigualdad con el dominio de definición de la función:
$$S = S_{\text{desigualdad}} \cap \text{Dom} = (-\infty, 3) \cap (2, \infty)$$

**Respuesta:** En notación de intervalo: $S = (2, 3)$.

**Ejemplo 5.6 (Inecuación trigonométrica simple):**
Resolver para $x \in [0, 2\pi]$ la inecuación trigonométrica:
$$\sin(x) > \dfrac{1}{2}$$

**Solución:**
Analizamos en el círculo unitario (círculo goniométrico) los ángulos $x$ en el intervalo $[0, 2\pi]$ cuya ordenada (coordenada $y$) es estrictamente superior a $1/2$.

Los valores fronteras donde $\sin(x) = 1/2$ dentro del primer período son:
$$x_1 = \dfrac{\pi}{6} \quad \text{y} \quad x_2 = \pi - \dfrac{\pi}{6} = \dfrac{5\pi}{6}$$

El seno es estrictamente mayor que $1/2$ para todos los ángulos comprendidos en el primer y segundo cuadrante ubicados sobre esta línea horizontal:
$$\dfrac{\pi}{6} < x < \dfrac{5\pi}{6}$$

**Respuesta:**
Para el dominio restringido $[0, 2\pi]$, el conjunto solución es $S = \left(\dfrac{\pi}{6}, \dfrac{5\pi}{6}\right)$.

> **Observación:** Si se requiriese resolver en todo el dominio de los números reales $\mathbb{R}$, se añade el período de oscilación de la función seno ($2\pi$) multiplicado por cualquier número entero $k \in \mathbb{Z}$. La solución general se expresaría como la unión infinita numerable:
> $$S_{\text{general}} = \bigcup_{k \in \mathbb{Z}} \left(\dfrac{\pi}{6} + 2k\pi, \dfrac{5\pi}{6} + 2k\pi\right)$$

---
## 6. Inecuaciones con Valor Absoluto

En el estudio del Cálculo y el Análisis Matemático, muchas veces no nos interesa la dirección de una cantidad en el espacio, sino la magnitud de su desviación o su margen de error. Por ejemplo, en los procesos de manufactura de alta precisión, la diferencia entre la medida de una pieza fabricada y su diseño teórico debe mantenerse dentro de un rango preestablecido, sin importar si la pieza es ligeramente más grande o más pequeña. Esta idea de medir desviaciones o distancias sin importar su sentido es modelada rigurosamente por las inecuaciones con valor absoluto.

Resolver una inecuación con valor absoluto consiste en encontrar el conjunto de puntos sobre la recta real que se encuentran a una cierta distancia (o dentro de un rango de distancias) de un punto de referencia. Para lograrlo, traducimos estas condiciones geométricas en inecuaciones algebraicas estándar mediante un conjunto de propiedades fundamentales.

> **Nota histórica:** La notación moderna de las barras verticales $|x|$ para representar el valor absoluto fue introducida por el matemático alemán Karl Weierstrass en 1841, en un trabajo sobre teoría de funciones complejas. Anteriormente, los matemáticos solían describir este concepto verbalmente o mediante notaciones ad-hoc que resultaban engorrosas para el desarrollo del cálculo diferencial e integral.

La definición formal de valor absoluto ha sido establecida previamente en la [[Clase 2 - Los Números]]. A partir de ella, se define la distancia geométrica entre dos puntos de la recta real:

**Definición 6.1 (Distancia en la recta real):**
Dados dos números reales $x, y \in \mathbb{R}$, la distancia geométrica entre ambos se define como:
$$d(x, y) = |x - y|$$

**Teorema 6.1 (Propiedades fundamentales de las inecuaciones con valor absoluto):**
Sea $a \in \mathbb{R}$ una constante positiva ($a > 0$). Se cumplen las siguientes equivalencias lógicas:

1. **Acotamiento interno (Caso "menor que"):**
   $$|x| < a \iff -a < x < a$$
   *Esta propiedad se extiende de forma idéntica para la desigualdad no estricta ($\leq$):*
   $$|x| \leq a \iff -a \leq x \leq a$$

2. **Dispersión externa (Caso "mayor que"):**
   $$|x| > a \iff x > a \lor x < -a$$
   *Esta propiedad se extiende de forma idéntica para la desigualdad no estricta ($\geq$):*
   $$|x| \geq a \iff x \geq a \lor x \leq -a$$

3. **Propiedad cuadrática:**
   $$|x| < |y| \iff x^2 < y^2$$

4. **Desigualdad triangular:**
   $$|x + y| \leq |x| + |y|$$

**Demostración (Propiedad 1):**
Se demostrará la doble implicación ($\iff$) analizando los casos según la definición de valor absoluto.

- **Implicación directa ($\implies$):** Supongamos que $|x| < a$ con $a > 0$.
  - Si $x \geq 0$, por definición se tiene que $|x| = x$. Por lo tanto, la desigualdad original resulta en $x < a$. Como $x \geq 0$ y $a > 0$, se cumple que $-a < 0 \leq x < a$, lo cual implica $-a < x < a$.
  - Si $x < 0$, por definición se tiene que $|x| = -x$. Así, la desigualdad resulta en $-x < a$. Al multiplicar ambos miembros por $-1$ (lo cual invierte el sentido de la desigualdad), se obtiene $x > -a$. Puesto que $x < 0$ y $a > 0$, se cumple que $-a < x < 0 < a$, lo cual también implica $-a < x < a$.
  
  En consecuencia, para cualquier caso se deduce que $-a < x < a$.

- **Implicación recíproca ($\impliedby$):** Supongamos ahora que $-a < x < a$.
  - Si $x \geq 0$, se tiene que $|x| = x$. Puesto que por hipótesis $x < a$, se concluye de forma directa que $|x| < a$.
  - Si $x < 0$, se tiene que $|x| = -x$. Puesto que por hipótesis $-a < x$, al multiplicar por $-1$ se obtiene $-x < a$, lo cual equivale a $|x| < a$.
  
  Por consiguiente, en cualquier caso se verifica que $|x| < a$.
$\blacksquare$

**Demostración (Propiedad 2):**
Esta equivalencia lógica se demuestra de manera elegante recurriendo a la negación lógica de la Propiedad 1. Puesto que se verifica la equivalencia para el acotamiento no estricto:
$$|x| \leq a \iff -a \leq x \leq a$$

Al aplicar la negación lógica en ambos miembros de la equivalencia, se obtiene:
$$\neg(|x| \leq a) \iff \neg(-a \leq x \leq a)$$

La negación del miembro izquierdo es:
$$\neg(|x| \leq a) \iff |x| > a$$

Y la negación de la conjunción $-a \leq x \land x \leq a$ en el miembro derecho, aplicando las leyes de De Morgan, resulta en:
$$\neg(-a \leq x \land x \leq a) \iff (x < -a \lor x > a)$$

Por lo tanto, se establece la equivalencia deseada:
$$|x| > a \iff x > a \lor x < -a$$
$\blacksquare$

**Demostración (Propiedad 3):**
Recordemos de [[Clase 2 - Los Números]] que para cualquier número real $u \in \mathbb{R}$ se cumple la identidad cuadrática $|u|^2 = u^2$. Además, la función cuadrática $f(t) = t^2$ es estrictamente creciente para valores no negativos ($t \geq 0$). 

Dado que $|x| \geq 0$ y $|y| \geq 0$ para todo $x, y \in \mathbb{R}$, se cumple que:
$$|x| < |y| \iff |x|^2 < |y|^2$$

Sustituyendo la identidad cuadrática en ambos miembros de la desigualdad, se obtiene:
$$x^2 < y^2$$

De esta forma, queda demostrada la equivalencia lógica.
$\blacksquare$

**Demostración (Propiedad 4 - Desigualdad triangular):**
Para cualquier número real $u \in \mathbb{R}$, se cumple por definición de valor absoluto que $-|u| \leq u \leq |u|$. Escribiendo esta relación para $x$ e $y$ de forma individual se obtiene:
$$\begin{align}
-|x| &\leq x \leq |x| \\[6pt]
-|y| &\leq y \leq |y|
\end{align}$$

Al sumar miembro a miembro ambas desigualdades, se deduce que:
$$-(|x| + |y|) \leq x + y \leq |x| + |y|$$

Definamos la constante no negativa $a = |x| + |y|$. La desigualdad anterior se reescribe de la forma:
$$-a \leq x + y \leq a$$

Aplicando el Teorema 6.1 (Propiedad 1 en el sentido recíproco $\impliedby$), esta desigualdad de acotamiento interno es equivalente a:
$$|x + y| \leq a$$

Sustituyendo el valor de $a$, se concluye la desigualdad buscada:
$$|x + y| \leq |x| + |y|$$
$\blacksquare$

### 6.1 Ejemplos resueltos

**Ejemplo 6.1 (Acotamiento interno):**
Resolver $|2x - 3| \leq 5$.

**Solución:**
Dado que la inecuación presenta la estructura de un acotamiento interno ($\leq$), aplicamos el Teorema 6.1 (Propiedad 1) para eliminar el valor absoluto, encerrando la expresión lineal entre $-5$ y $5$:
$$\begin{align}
-5 &\leq 2x - 3 \leq 5 \\[6pt]
-5 + 3 &\leq 2x \leq 5 + 3 \quad \text{(se suma } 3 \text{ en todos los términos)} \\[6pt]
-2 &\leq 2x \leq 8 \\[6pt]
\dfrac{-2}{2} &\leq x \leq \dfrac{8}{2} \quad \text{(se divide entre } 2 \text{)} \\[6pt]
-1 &\leq x \leq 4
\end{align}$$

**Respuesta:** En notación de intervalo: $S = [-1, 4]$.

**Ejemplo 6.2 (Dispersión externa):**
Resolver $|3x + 1| > 7$.

**Solución:**
Dado que la inecuación presenta la estructura de una dispersión externa ($>$), aplicamos el Teorema 6.1 (Propiedad 2), desglosando el problema en dos inecuaciones lineales unidas por el conectivo lógico disyuntivo "o" ($\lor$):
$$\begin{align}
3x + 1 > 7 \quad &\lor \quad 3x + 1 < -7 \\[6pt]
3x > 6 \quad &\lor \quad 3x < -8 \\[6pt]
x > 2 \quad &\lor \quad x < -\dfrac{8}{3}
\end{align}$$

**Respuesta:** El conjunto solución es la unión de los intervalos divergentes. En notación de intervalo: $S = \left(-\infty, -\dfrac{8}{3}\right) \cup (2, \infty)$.

**Ejemplo 6.3 (Dispersión externa no lineal):**
Resolver la inecuación racional con valor absoluto:
$$\left| \dfrac{x + 2}{x - 1} \right| > 2$$

**Solución:**
En primer lugar, se establece la restricción de dominio para que la fracción esté bien definida en los números reales: el denominador no debe anularse, por lo que $x - 1 \neq 0$, lo que implica que $x \neq 1$. De este modo, el dominio admisible es $\text{Dom} = \mathbb{R} \setminus \{1\}$.

Dado que la inecuación presenta la estructura de una dispersión externa ($|u| > a$), se aplica la Propiedad 2 del Teorema 6.1 para desglosar la desigualdad en dos inecuaciones racionales independientes conectadas por la disyunción lógica "o" ($\lor$):
$$\dfrac{x + 2}{x - 1} > 2 \quad \lor \quad \dfrac{x + 2}{x - 1} < -2$$

A continuación, se resuelve cada inecuación de manera separada:

**Caso 1:** $\dfrac{x + 2}{x - 1} > 2$
Se transpone el término constante al miembro izquierdo y se efectúa la suma algebraica para obtener una única fracción:
$$\begin{align}
\dfrac{x + 2}{x - 1} - 2 &> 0 \\[8pt]
\dfrac{(x + 2) - 2(x - 1)}{x - 1} &> 0 \\[8pt]
\dfrac{x + 2 - 2x + 2}{x - 1} &> 0 \\[8pt]
\dfrac{-x + 4}{x - 1} &> 0
\end{align}$$

Los puntos críticos del cociente son los valores que anulan el numerador y el denominador:
- Numerador: $-x + 4 = 0 \implies x = 4$
- Denominador: $x - 1 = 0 \implies x = 1$

Se realiza el análisis de signos para el cociente $\dfrac{-x + 4}{x - 1}$ en los intervalos definidos por estos puntos críticos:
- Para $x \in (-\infty, 1)$, se tiene que $\dfrac{\text{positivo}}{\text{negativo}} < 0$.
- Para $x \in (1, 4)$, se tiene que $\dfrac{\text{positivo}}{\text{positivo}} > 0$.
- Para $x \in (4, \infty)$, se tiene que $\dfrac{\text{negativo}}{\text{positivo}} < 0$.

Como se busca la región donde el cociente es estrictamente mayor que cero ($> 0$), el conjunto solución para este primer caso es:
$$S_1 = (1, 4)$$

**Caso 2:** $\dfrac{x + 2}{x - 1} < -2$
Se transpone el término constante y se realiza la suma de fracciones:
$$\begin{align}
\dfrac{x + 2}{x - 1} + 2 &< 0 \\[8pt]
\dfrac{(x + 2) + 2(x - 1)}{x - 1} &< 0 \\[8pt]
\dfrac{x + 2 + 2x - 2}{x - 1} &< 0 \\[8pt]
\dfrac{3x}{x - 1} &< 0
\end{align}$$

Los puntos críticos de este cociente son:
- Numerador: $3x = 0 \implies x = 0$
- Denominador: $x - 1 = 0 \implies x = 1$

Se analiza el signo de $\dfrac{3x}{x - 1}$ en los respectivos intervalos:
- Para $x \in (-\infty, 0)$, se verifica que $\dfrac{\text{negativo}}{\text{negativo}} > 0$.
- Para $x \in (0, 1)$, se verifica que $\dfrac{\text{positivo}}{\text{negativo}} < 0$.
- Para $x \in (1, \infty)$, se verifica que $\dfrac{\text{positivo}}{\text{positivo}} > 0$.

Como se requiere que la expresión sea estrictamente menor que cero ($< 0$), la solución del segundo caso corresponde a:
$$S_2 = (0, 1)$$

**Respuesta:**
Dado que la inecuación original está definida por la disyunción lógica de ambos casos, el conjunto solución global $S$ se obtiene mediante la unión de las soluciones parciales $S_1$ y $S_2$:
$$S = S_1 \cup S_2 = (0, 1) \cup (1, 4)$$

Obsérvese que el punto crítico $x = 1$ queda excluido de manera natural al ser un extremo abierto en ambos intervalos, lo cual es plenamente consistente con la restricción de dominio establecida al inicio.

**Ejemplo 6.4 (Valor absoluto en ambos lados):**
Resolver $|2x - 1| < |x + 3|$.

**Solución:**
Dado que ambos miembros de la inecuación son estrictamente no negativos, podemos elevar al cuadrado en ambos miembros sin alterar la desigualdad, puesto que para $a, b \geq 0$ se cumple que $a < b \iff a^2 < b^2$:
$$\begin{align}
|2x - 1|^2 &< |x + 3|^2 \\[6pt]
(2x - 1)^2 &< (x + 3)^2 \\[6pt]
4x^2 - 4x + 1 &< x^2 + 6x + 9 \\[6pt]
3x^2 - 10x - 8 &< 0
\end{align}$$

Ahora factorizamos la expresión cuadrática $3x^2 - 10x - 8$. Para ello, determinamos los puntos críticos resolviendo la ecuación cuadrática asociada $3x^2 - 10x - 8 = 0$ mediante la fórmula general:
$$x = \dfrac{10 \pm \sqrt{(-10)^2 - 4(3)(-8)}}{2(3)} = \dfrac{10 \pm \sqrt{100 + 96}}{6} = \dfrac{10 \pm 14}{6}$$

Se obtienen los dos puntos críticos:
$$x_1 = \dfrac{24}{6} = 4 \quad \text{y} \quad x_2 = \dfrac{-4}{6} = -\dfrac{2}{3}$$

Así, la inecuación cuadrática se reescribe como:
$$(3x + 2)(x - 4) < 0$$

Construimos la tabla de signos para identificar los intervalos donde el producto es estrictamente negativo:

| Intervalo | $\left(-\infty, -\dfrac{2}{3}\right)$ | $-\dfrac{2}{3}$ | $\left(-\dfrac{2}{3}, 4\right)$ | $4$ | $(4, \infty)$ |
| :--- | :---: | :---: | :---: | :---: | :---: |
| $(3x + 2)$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| $(x - 4)$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $\text{Producto}$ | $+$ | $0$ | $-$ | $0$ | $+$ |

Buscamos las regiones con signo negativo ($< 0$):
- $\left(-\infty, -\dfrac{2}{3}\right)$: signo $+$ ✗
- $x = -\dfrac{2}{3}$: el producto vale $0$, excluido por el signo estrictamente menor ($<$) ✗
- $\left(-\dfrac{2}{3}, 4\right)$: signo $-$ ✓
- $x = 4$: el producto vale $0$, excluido ✗
- $(4, \infty)$: signo $+$ ✗

**Respuesta:** En notación de intervalo: $S = \left(-\dfrac{2}{3}, 4\right)$.

> **Advertencia (Caso de constante no positiva):** Las propiedades del Teorema 6.1 asumen estrictamente que la constante $a$ es positiva ($a > 0$). Si se presenta una inecuación donde $a \leq 0$, las propiedades no se aplican directamente y debe usarse el análisis lógico elemental:
> - Una inecuación del tipo $|f(x)| < -5$ **no tiene solución** ($S = \emptyset$), puesto que un valor absoluto nunca puede ser menor que un número negativo.
> - Una inecuación del tipo $|f(x)| \geq -2$ se cumple para todo $x$ en el dominio de $f$ ($S = \text{Dom}(f)$), dado que un valor absoluto siempre es mayor o igual a cero, y por ende, mayor que cualquier negativo.

**Aplicaciones y trascendencia en el Cálculo:**

Las inecuaciones con valor absoluto son la herramienta matemática por excelencia para modelar la noción de proximidad, cercanía y margen de error en la recta real. Por este motivo, constituyen la base fundamental sobre la que se construyen los conceptos más importantes del Cálculo y el Análisis Matemático:

- **Definiciones conceptuales de continuidad y límite:** Aunque se estudiarán formalmente más adelante en el curso, las nociones de límite de una función, continuidad y convergencia de sucesiones se definen enteramente a través de desigualdades con valor absoluto (del tipo $|x - c| < \delta$ y $|f(x) - L| < \varepsilon$). Estas inecuaciones permiten cuantificar de manera rigurosa qué significa que una variable se "aproxime infinitamente" a un punto de referencia.
- **Teoremas de acotamiento y estimación de errores:** En múltiples teoremas fundamentales del Cálculo (como el Teorema del Valor Medio o fórmulas de aproximación por desarrollos polinomiales de Taylor), el valor absoluto se emplea para acotar el término del error o residuo. Expresar que el error de una aproximación está acotado se traduce algebraicamente en resolver una inecuación de la forma $|x_{\text{real}} - x_{\text{aprox}}| < \text{tolerancia}$.
- **Criterios de estabilidad y convergencia:** En los métodos numéricos y la resolución computacional de problemas matemáticos, la convergencia de algoritmos iterativos se comprueba verificando que la diferencia absoluta entre iteraciones sucesivas disminuya progresivamente por debajo de un umbral específico de precisión.
- **Tolerancia y metrología aplicada:** En física e ingeniería, las especificaciones de calidad y tolerancias de diseño de piezas y sistemas se expresan de manera unívoca mediante inecuaciones con valor absoluto de la forma $|V - V_0| \leq t$, donde $V_0$ es el valor nominal de diseño y $t$ es la tolerancia admisible.

---
## 7. Sistemas de Inecuaciones

Pensemos en el diseño de un puente o una estructura de ingeniería: las vigas deben soportar fuerzas de compresión masivas, pero a la vez deben mantenerse ligeras para no sobrecargar los pilares. Esto significa que el peso de la estructura debe ser mayor que un límite mínimo de seguridad, pero menor que un límite máximo de resistencia física. Ambos límites imponen restricciones que se deben cumplir al mismo tiempo.

En matemáticas, cuando un problema exige satisfacer múltiples restricciones o desigualdades simultáneamente, hablamos de un **sistema de inecuaciones**. A diferencia de los sistemas de ecuaciones lineales, donde buscamos la coincidencia exacta de rectas en un punto único, en los sistemas de inecuaciones buscamos la zona común o la superposición de varias regiones en la recta real.

> **Nota histórica:** Los sistemas de desigualdades lineales y sus métodos sistemáticos de resolución cobraron una relevancia trascendental a mediados del siglo XX con el surgimiento de la **programación lineal**, desarrollada por matemáticos como George Dantzig. Este campo, crucial para la optimización de recursos en economía, logística e ingeniería, se fundamenta enteramente en encontrar soluciones comunes a grandes sistemas de inecuaciones lineales simultáneas.

**Definición 7.1 (Sistema de Inecuaciones en una Variable):**
Un sistema de inecuaciones en una variable $x$ es un conjunto finito de dos o más inecuaciones que deben satisfacerse simultáneamente. Se representa mediante una llave que agrupa las inecuaciones:
$$\begin{cases} 
f_1(x) \lessgtr 0 \\[6pt] 
f_2(x) \lessgtr 0 \\[6pt] 
\vdots \\ 
f_n(x) \lessgtr 0 
\end{cases}$$

El conjunto solución total de este sistema, denotado por $S_{\text{total}}$, se define formalmente como la intersección de los conjuntos solución individuales de cada inecuación:
$$S_{\text{total}} = \bigcap_{i=1}^{n} S_i = S_1 \cap S_2 \cap \dots \cap S_n$$
donde $S_i$ es el conjunto solución de la $i$-ésima inecuación $f_i(x) \lessgtr 0$.

### 7.1 Método de resolución conjuntista

A diferencia de los sistemas de ecuaciones, donde se emplean métodos analíticos de reducción o sustitución algebraicos cruzados, el enfoque para los sistemas de inecuaciones con una sola variable es puramente conjuntista y se desarrolla en los siguientes pasos:

1. **Resolución individual:** Se determina el conjunto solución $S_i$ de cada una de las inecuaciones del sistema por separado, aplicando los métodos correspondientes (lineales, cuadráticos, racionales, o con valor absoluto).
2. **Representación gráfica conjunta:** Se representan de manera simultánea los conjuntos $S_i$ sobre una misma recta real. Esto permite identificar visualmente las franjas o regiones donde se superponen todos los intervalos representados.
3. **Intersección conjuntista:** Se calcula la intersección matemática de los intervalos. Si no existen puntos comunes entre todos los conjuntos individuales, se concluye que el sistema no tiene solución, por lo que el conjunto solución es vacío ($S_{\text{total}} = \emptyset$).

### 7.2 Ejemplos resueltos

**Ejemplo 7.1 (Sistema lineal clásico):**
Resolver el siguiente sistema de inecuaciones:
$$\begin{cases} 
2x - 5 < 3 \\[6pt] 
-x + 4 \leq 2 
\end{cases}$$

**Solución:**
Resolvemos la primera inecuación de manera independiente:
$$\begin{align}
2x - 5 &< 3 \\[6pt]
2x &< 8 \\[6pt]
x &< 4 \implies S_1 = (-\infty, 4)
\end{align}$$

Resolvemos la segunda inecuación de manera independiente:
$$\begin{align}
-x + 4 &\leq 2 \\[6pt]
-x &\leq -2 \\[6pt]
x &\geq 2 \quad \text{(se invierte el orden al dividir por } -1\text{)} \implies S_2 = [2, \infty)
\end{align}$$

Para determinar el conjunto solución total, intersectamos los intervalos de solución de ambas inecuaciones:
$$S_{\text{total}} = S_1 \cap S_2 = (-\infty, 4) \cap [2, \infty)$$

**Respuesta:** En notación de intervalo: $S_{\text{total}} = [2, 4)$.

**Ejemplo 7.2 (Sistema mixto con inecuación cuadrática):**
Resolver el siguiente sistema de inecuaciones:
$$\begin{cases} 
x^2 - 9 \leq 0 \\[6pt] 
x > 1 
\end{cases}$$

**Solución:**
Resolvemos la primera inecuación factorizando la diferencia de cuadrados del polinomio de segundo grado:
$$\begin{align}
x^2 - 9 &\leq 0 \\[6pt]
(x - 3)(x + 3) &\leq 0
\end{align}$$

Las raíces del polinomio son los puntos críticos $x = 3$ y $x = -3$. Al evaluar los intervalos mediante una tabla de signos, se determina que el producto es negativo o nulo en el intervalo cerrado delimitado por las raíces:
$$S_1 = [-3, 3]$$

La segunda inecuación representa un intervalo directo y no requiere operaciones adicionales:
$$S_2 = (1, \infty)$$

Calculamos la intersección entre ambos conjuntos solución:
$$S_{\text{total}} = S_1 \cap S_2 = [-3, 3] \cap (1, \infty)$$

**Respuesta:** En notación de intervalo: $S_{\text{total}} = (1, 3]$.

**Ejemplo 7.3 (Sistema sin solución - Intersección vacía):**
Resolver el siguiente sistema de inecuaciones:
$$\begin{cases} 
2x + 3 \leq -1 \\[6pt] 
x^2 - 3x - 4 < 0 
\end{cases}$$

**Solución:**
Resolvemos la primera inecuación de manera independiente:
$$\begin{align}
2x + 3 &\leq -1 \\[6pt]
2x &\leq -4 \\[6pt]
x &\leq -2 \implies S_1 = (-\infty, -2]
\end{align}$$

Resolvemos la segunda inecuación factorizando el trinomio cuadrático:
$$\begin{align}
x^2 - 3x - 4 &< 0 \\[6pt]
(x - 4)(x + 1) &< 0
\end{align}$$

Los puntos críticos son las raíces $x = 4$ y $x = -1$. Al evaluar los signos, se comprueba que el producto es estrictamente negativo en la región interior a las raíces:
$$S_2 = (-1, 4)$$

Buscamos los puntos de la recta real comunes a ambos conjuntos efectuando su intersección:
$$S_{\text{total}} = S_1 \cap S_2 = (-\infty, -2] \cap (-1, 4)$$

Dado que no existe ningún número real que pertenezca simultáneamente al intervalo $(-\infty, -2]$ y al intervalo $(-1, 4)$, los intervalos son disjuntos.

**Respuesta:** El sistema no posee soluciones en el conjunto de los números reales. En notación de conjunto: $S_{\text{total}} = \emptyset$.

> **Observación importante:** Al realizar la intersección de intervalos, se debe prestar especial atención a los extremos de cada intervalo (abiertos o cerrados). Un punto extremo pertenece a la intersección final si y solo si pertenece a **todos** los conjuntos solución individuales de las inecuaciones. Si un punto está excluido (extremo abierto) en al menos uno de los intervalos, debe excluirse inevitablemente del conjunto solución final.

**Aplicaciones:**
Los sistemas de inecuaciones formalizan matemáticamente cualquier situación donde múltiples restricciones deben cumplirse en simultáneo. El campo más importante que se fundamenta en ellos es la **programación lineal**: dados recursos limitados y restricciones expresadas como inecuaciones lineales sobre variables de decisión, se busca la asignación que optimiza una función objetivo. Su aplicación abarca la logística de distribución, la planificación de producción industrial, la optimización de portafolios financieros y el diseño de dietas en nutrición clínica. En ingeniería de control, los sistemas de inecuaciones aparecen al especificar simultáneamente condiciones de estabilidad, rango de operación y límites de seguridad sobre las variables del sistema. En estadística, la estimación con restricciones múltiples genera sistemas de inecuaciones cuya región de intersección define el conjunto de parámetros factibles.

---
## 8. Aplicaciones Teóricas en el Cálculo: Dominios y Restricciones

En el análisis matemático y el cálculo diferencial, las inecuaciones no solo son herramientas para la resolución de problemas aplicados, sino que constituyen el fundamento algebraico para definir el comportamiento de las funciones reales de variable real. Específicamente, las inecuaciones permiten delimitar el **dominio de definición** de funciones que presentan restricciones de existencia en el conjunto de los números reales ($\mathbb{R}$), tales como las raíces de índice par y los logaritmos.

### 8.1 Determinación de Dominios de Existencia

El dominio de una función real $f$, denotado por $\text{Dom}(f)$, es el conjunto de todos los números reales para los cuales la expresión $f(x)$ está bien definida y arroja un valor real.

**Proposición 8.1 (Condiciones de dominio):**
Las restricciones fundamentales que se traducen en inecuaciones son:

1. **Raíces de índice par:** Para una función de la forma $f(x) = \sqrt[2k]{g(x)}$ con $k \in \mathbb{N}$, la radicación solo está definida en los reales si el radicando es no negativo:
   $$g(x) \geq 0$$

2. **Funciones logarítmicas:** Para una función de la forma $f(x) = \log_b(g(x))$, el logaritmo solo está definido para valores estrictamente positivos del argumento:
   $$g(x) > 0$$

3. **Restricciones combinadas:** Si una expresión con restricciones se encuentra en el denominador de una fracción, el dominio excluye adicionalmente los puntos donde el denominador se anula. Por ejemplo, para $f(x) = \dfrac{1}{\sqrt{g(x)}}$, la condición se reduce a una inecuación estricta:
   $$g(x) > 0$$

### 8.2 Ejemplos resueltos

**Ejemplo 8.1 (Dominio con radical cuadrático):**
Determinar el dominio de definición de la función:
$$f(x) = \sqrt{x^2 - 4x - 5}$$

**Solución:**
Para que la función arroje un resultado real, la expresión dentro de la raíz cuadrada debe ser mayor o igual a cero. Esto se modela mediante la inecuación cuadrática:
$$x^2 - 4x - 5 \geq 0$$

Factorizamos el trinomio cuadrático buscando dos números que multiplicados den $-5$ y sumados den $-4$. Estos números son $-5$ y $1$:
$$(x - 5)(x + 1) \geq 0$$

Los puntos críticos son $x = -1$ y $x = 5$. Construimos la tabla de signos para analizar el comportamiento del producto de los factores lineales en cada intervalo:

| Intervalo | $(-\infty, -1)$ | $(-1, 5)$ | $(5, \infty)$ |
| :--- | :---: | :---: | :---: |
| $(x + 1)$ | $-$ | $+$ | $+$ |
| $(x - 5)$ | $-$ | $-$ | $+$ |
| $\text{Producto}$ | $+$ | $-$ | $+$ |

Buscamos las regiones con signo positivo o nulo ($\geq 0$). Al tratarse de una desigualdad no estricta, los extremos de los intervalos (los puntos críticos $\{-1, 5\}$) se incluyen en el conjunto solución:
- $(-\infty, -1)$: signo positivo (se incluye, cerrado en $-1$) ✓
- $(-1, 5)$: signo negativo (se excluye)
- $(5, \infty)$: signo positivo (se incluye, cerrado en $5$) ✓

Otra forma de analizar esto es considerar que la parábola $y = x^2 - 4x - 5$ abre hacia arriba ($a = 1 > 0$), por lo que su valor es mayor o igual a cero fuera del intervalo delimitado por sus raíces.

![[parabola_-1-5.png]]

**Respuesta:** El dominio de la función es:
$$\text{Dom}(f) = (-\infty, -1] \cup [5, \infty)$$

**Ejemplo 8.2 (Dominio con logaritmo y expresión racional):**
Determinar el dominio de definición de la función:
$$g(x) = \ln\left(\dfrac{2x + 6}{x - 4}\right)$$

**Solución:**
El logaritmo natural está definido únicamente si su argumento es estrictamente mayor que cero. Esto exige resolver la inecuación racional:
$$\dfrac{2x + 6}{x - 4} > 0$$

Identificamos los puntos críticos que definen los cambios de signo de la fracción:
- Numerador: $2x + 6 = 0 \implies x = -3$
- Denominador: $x - 4 = 0 \implies x = 4$

Construimos la tabla de signos para analizar el comportamiento del cociente:

| Intervalo | $(-\infty, -3)$ | $-3$ | $(-3, 4)$ | $4$ | $(4, \infty)$ |
| :--- | :---: | :---: | :---: | :---: | :---: |
| $(2x + 6)$ | $-$ | $0$ | $+$ | $+$ | $+$ |
| $(x - 4)$ | $-$ | $-$ | $-$ | $0$ | $+$ |
| $\text{Cociente}$ | $+$ | $0$ | $-$ | $\nexists$ | $+$ |

Buscamos las regiones donde el cociente es estrictamente positivo ($> 0$). Excluimos los extremos puesto que el logaritmo requiere una desigualdad estricta y el punto $x = 4$ indetermina el denominador:
- Para $x \in (-\infty, -3)$, el signo es positivo ✓
- Para $x \in (-3, 4)$, el signo es negativo ✗
- Para $x \in (4, \infty)$, el signo es positivo ✓

**Respuesta:** El dominio de la función es:
$$\text{Dom}(g) = (-\infty, -3) \cup (4, \infty)$$

**Ejemplo 8.3 (Dominio con restricciones múltiples acopladas):**
Determinar el dominio de definición de la función:
$$h(x) = \sqrt{x + 3} + \dfrac{1}{\ln(5 - x)}$$

**Solución:**
Para que la función $h(x)$ esté definida, deben satisfacerse simultáneamente tres condiciones matemáticas en los reales:
1. La raíz cuadrada debe tener un radicando no negativo.
2. El logaritmo natural debe tener un argumento estrictamente positivo.
3. El denominador de la fracción no debe anularse.

Planteamos y resolvemos cada restricción por separado:

* **Condición 1 (Raíz):**
  $$x + 3 \geq 0 \implies x \geq -3 \implies S_1 = [-3, \infty)$$

* **Condición 2 (Logaritmo):**
  $$5 - x > 0 \implies -x > -5 \implies x < 5 \implies S_2 = (-\infty, 5)$$

* **Condición 3 (Denominador no nulo):**
  El denominador se anula cuando $\ln(5 - x) = 0$. Resolvemos esta ecuación:
  $$\ln(5 - x) = 0 \implies 5 - x = e^0 \implies 5 - x = 1 \implies x = 4$$
  Por lo tanto, se debe excluir el valor $x = 4$ del dominio:
  $$S_3 = \mathbb{R} \setminus \{4\}$$

El dominio global de la función se obtiene mediante la intersección simultánea de las tres soluciones parciales:
$$\text{Dom}(h) = S_1 \cap S_2 \cap S_3 = [-3, \infty) \cap (-\infty, 5) \cap (\mathbb{R} \setminus \{4\})$$

Realizando la intersección de los intervalos, obtenemos la región $[-3, 5)$ excluyendo el punto aislado $4$:
$$\text{Dom}(h) = [-3, 5) \setminus \{4\}$$

**Respuesta:** Expresado como unión de intervalos:
$$\text{Dom}(h) = [-3, 4) \cup (4, 5)$$


---
## 9. Ejercicios Propuestos

### 9.1 Ejercicios algebraicos de práctica

**Inecuaciones lineales:**

1. Resolver y graficar el conjunto solución:
   $$5x - 7 \leq 3x + 9$$

2. Resolver la inecuación con fracciones:
   $$\dfrac{2x - 1}{4} - \dfrac{x + 3}{6} > 1$$

3. Resolver la inecuación de doble desigualdad simultánea:
   $$-1 \leq \dfrac{3x + 2}{5} < 4$$

**Inecuaciones cuadráticas:**

4. Resolver empleando tabla de signos ($\Delta > 0$, dos raíces distintas):
   $$x^2 + x - 6 > 0$$

5. Resolver el caso de raíz doble ($\Delta = 0$):
   $$-x^2 + 6x - 9 \geq 0$$

6. Resolver el caso sin raíces reales ($\Delta < 0$):
   $$2x^2 - 3x + 5 > 0$$

7. Resolver con coeficiente principal negativo:
   $$-3x^2 + 2x + 8 \geq 0$$

**Inecuaciones racionales:**

8. Determinar el conjunto solución (forma estándar directa):
   $$\dfrac{x + 4}{x - 3} \leq 0$$

9. Resolver la inecuación que requiere agrupar antes de la tabla de signos:
   $$\dfrac{x - 3}{x + 1} < 2$$

10. Resolver con numerador cuadrático factorizable:
    $$\dfrac{x^2 + x - 12}{2x - 1} > 0$$

11. Resolver la inecuación con suma de cocientes (requiere mínimo común denominador):
    $$\dfrac{1}{x - 2} + \dfrac{1}{x + 3} \leq 0$$

**Inecuaciones con valor absoluto:**

12. Resolver el caso de acotamiento interno:
    $$|2x - 1| \leq 5$$

13. Resolver el caso de dispersión externa:
    $$|4x + 3| > 9$$

14. Resolver con valor absoluto en ambos miembros:
    $$|x - 2| < |3x + 4|$$

15. Resolver la inecuación con constante no positiva, analizando el caso especial:
    $$|5x - 1| \geq -3$$

**Sistemas de inecuaciones:**

16. Resolver el sistema lineal simultáneo:
    $$\begin{cases} 
    3x + 4 > 1 \\[6pt] 
    x^2 - 5x + 4 \leq 0 
    \end{cases}$$

17. Resolver el sistema que combina una inecuación racional con una lineal:
    $$\begin{cases} 
    \dfrac{x + 1}{x - 4} \geq 0 \\[10pt] 
    2x - 3 < 7 
    \end{cases}$$

18. Resolver el sistema cuya intersección resulta vacía (sin solución):
    $$\begin{cases} 
    |x - 1| \leq 2 \\[6pt] 
    x^2 - x - 6 > 0 
    \end{cases}$$

### 9.2 Problemas de aplicación práctica (enunciados)

1. **Optimización de costos y utilidades:** Un fabricante de dispositivos electrónicos estima que el costo total de producir $x$ unidades diarias está dado por la función de costo lineal $C(x) = 25x + 3500$ (en dólares). Si cada unidad se vende en el mercado a $60$ dólares:
   - Determine la función de utilidad diaria $U(x)$.
   - Encuentre el número mínimo de unidades diarias que deben fabricarse y venderse para que la empresa comience a generar utilidades netas positivas (es decir, $U(x) > 0$).

2. **Lanzamiento vertical de un proyectil:** Un proyectil es disparado verticalmente hacia arriba desde el nivel del suelo. Su altura $h$ (en metros) transcurridos $t$ segundos de vuelo está modelada por la función cuadrática $h(t) = -5t^2 + 80t$.
   - Determine el intervalo de tiempo durante el cual el proyectil se encuentra a una altura estrictamente superior a los $240$ metros sobre el nivel del suelo.

3. **Control de calidad y tolerancia industrial:** En una planta embotelladora, el volumen nominal de líquido de una botella de refresco de edición especial debe ser de $500\text{ ml}$. Debido al margen de tolerancia de los equipos, el volumen real $V$ puede diferir del nominal en un máximo de $8\text{ ml}$.
   - Escriba esta especificación empleando una inecuación con valor absoluto.
   - Resuelva la inecuación para encontrar el intervalo exacto de volúmenes de envasado aceptados por el departamento de control de calidad.

4. **Farmacocinética médica:** La concentración $C$ (en miligramos por litro, $\text{mg/L}$) de un antibiótico en el torrente sanguíneo de un paciente, transcurridas $t$ horas desde su administración intravenosa, está modelada por la función racional:
   $$C(t) = \dfrac{10t}{t^2 + 4}$$
   - Determine el intervalo de tiempo en el cual la concentración del fármaco en sangre es estrictamente superior a los $2\text{ mg/L}$.

---

**Fin de la Clase 4: Inecuaciones**