# Inecuaciones: Fundamentos Algebraicos

## 1. Desigualdades e Inecuaciones: Conceptos Básicos

### 1.1 Desigualdades: Definición y Tipos

A diferencia de las ecuaciones, que establecen una igualdad estricta entre dos cantidades, gran parte de la matemática se basa en comparar tamaños o magnitudes que no son iguales. Piensa en situaciones cotidianas: "la velocidad máxima es 120 km/h", "el presupuesto debe ser menor a 500 dólares". Las desigualdades nos permiten modelar matemáticamente estas restricciones y acotar valores.

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

**Definición 1.3 (Conjunto Solución):**
El **conjunto solución** de una inecuación es el conjunto de todos los valores reales que satisfacen la desigualdad. Dos inecuaciones se denominan **equivalentes** si tienen exactamente el mismo conjunto solución.

> **Observación importante:** A diferencia de las ecuaciones lineales o cuadráticas, donde la solución suele ser un conjunto discreto de números (uno, dos o tres valores específicos), en las inecuaciones el conjunto solución es casi siempre **infinito**, abarcando todo un continuo en la recta numérica.

**Ejemplo 1.3 (Conjuntos solución simples):**
Para comprender la naturaleza de estos conjuntos, veamos algunas inecuaciones elementales:
- $x > 0 \implies$ El conjunto solución son todos los números reales estrictamente positivos ($\mathbb{R}^+$).
- $x \leq 0 \implies$ El conjunto solución son todos los reales negativos incluyendo al cero ($\mathbb{R}^- \cup \{0\}$).
- $x^2 < 0 \implies$ El conjunto solución es vacío ($\emptyset$), ya que ningún número real al cuadrado arroja un resultado negativo.
- $|x| \geq 0 \implies$ El conjunto solución son todos los números reales ($\mathbb{R}$), pues el valor absoluto de cualquier número siempre es no negativo.
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
x &< \frac{12}{3} \\
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

---
## 3. Inecuaciones Cuadráticas

A diferencia de las inecuaciones lineales, en las cuadráticas el comportamiento de la expresión $ax^2 + bx + c$ cambia de signo en distintas regiones de la recta real. La estrategia de "despejar $x$" ya no es suficiente: en su lugar, se debe analizar dónde la expresión es positiva y dónde es negativa. La herramienta central para esto es la **tabla de signos**.
 
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

---
## 5. Inecuaciones con Valor Absoluto

En el estudio del Cálculo y el Análisis Matemático, muchas veces no nos interesa la dirección de una cantidad en el espacio, sino la magnitud de su desviación o su margen de error. Por ejemplo, en los procesos de manufactura de alta precisión, la diferencia entre la medida de una pieza fabricada y su diseño teórico debe mantenerse dentro de un rango preestablecido, sin importar si la pieza es ligeramente más grande o más pequeña. Esta idea de medir desviaciones o distancias sin importar su sentido es modelada rigurosamente por las inecuaciones con valor absoluto.

Resolver una inecuación con valor absoluto consiste en encontrar el conjunto de puntos sobre la recta real que se encuentran a una cierta distancia (o dentro de un rango de distancias) de un punto de referencia. Para lograrlo, traducimos estas condiciones geométricas en inecuaciones algebraicas estándar mediante un conjunto de propiedades fundamentales.

> **Nota histórica:** La notación moderna de las barras verticales $|x|$ para representar el valor absoluto fue introducida por el matemático alemán Karl Weierstrass en 1841, en un trabajo sobre teoría de funciones complejas. Anteriormente, los matemáticos solían describir este concepto verbalmente o mediante notaciones ad-hoc que resultaban engorrosas para el desarrollo del cálculo diferencial e integral.

La definición formal de valor absoluto ha sido establecida previamente en la [[Clase 2 - Los Números]]. A partir de ella, se define la distancia geométrica entre dos puntos de la recta real:

**Definición 5.1 (Distancia en la recta real):**
Dados dos números reales $x, y \in \mathbb{R}$, la distancia geométrica entre ambos se define como:
$$d(x, y) = |x - y|$$

**Teorema 5.1 (Propiedades fundamentales de las inecuaciones con valor absoluto):**
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
Recordemos de la *Clase 2* que para cualquier número real $u \in \mathbb{R}$ se cumple la identidad cuadrática $|u|^2 = u^2$. Además, la función cuadrática $f(t) = t^2$ es estrictamente creciente para valores no negativos ($t \geq 0$). 

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

Aplicando el Teorema 5.1 (Propiedad 1 en el sentido recíproco $\impliedby$), esta desigualdad de acotamiento interno es equivalente a:
$$|x + y| \leq a$$

Sustituyendo el valor de $a$, se concluye la desigualdad buscada:
$$|x + y| \leq |x| + |y|$$
$\blacksquare$

### 5.1 Ejemplos resueltos

**Ejemplo 5.1 (Acotamiento interno):**
Resolver $|2x - 3| \leq 5$.

**Solución:**
Dado que la inecuación presenta la estructura de un acotamiento interno ($\leq$), aplicamos el Teorema 5.1 (Propiedad 1) para eliminar el valor absoluto, encerrando la expresión lineal entre $-5$ y $5$:
$$\begin{align}
-5 &\leq 2x - 3 \leq 5 \\[6pt]
-5 + 3 &\leq 2x \leq 5 + 3 \quad \text{(se suma } 3 \text{ en todos los términos)} \\[6pt]
-2 &\leq 2x \leq 8 \\[6pt]
\dfrac{-2}{2} &\leq x \leq \dfrac{8}{2} \quad \text{(se divide entre } 2 \text{)} \\[6pt]
-1 &\leq x \leq 4
\end{align}$$

**Respuesta:** En notación de intervalo: $S = [-1, 4]$.

**Ejemplo 5.2 (Dispersión externa):**
Resolver $|3x + 1| > 7$.

**Solución:**
Dado que la inecuación presenta la estructura de una dispersión externa ($>$), aplicamos el Teorema 5.1 (Propiedad 2), desglosando el problema en dos inecuaciones lineales unidas por el conectivo lógico disyuntivo "o" ($\lor$):
$$\begin{align}
3x + 1 > 7 \quad &\lor \quad 3x + 1 < -7 \\[6pt]
3x > 6 \quad &\lor \quad 3x < -8 \\[6pt]
x > 2 \quad &\lor \quad x < -\dfrac{8}{3}
\end{align}$$

**Respuesta:** El conjunto solución es la unión de los intervalos divergentes. En notación de intervalo: $S = \left(-\infty, -\dfrac{8}{3}\right) \cup (2, \infty)$.

**Ejemplo 5.3 (Valor absoluto en ambos lados):**
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

> **Advertencia (Caso de constante no positiva):** Las propiedades del Teorema 5.1 asumen estrictamente que la constante $a$ es positiva ($a > 0$). Si se presenta una inecuación donde $a \leq 0$, las propiedades no se aplican directamente y debe usarse el análisis lógico elemental:
> - Una inecuación del tipo $|f(x)| < -5$ **no tiene solución** ($S = \emptyset$), puesto que un valor absoluto nunca puede ser menor que un número negativo.
> - Una inecuación del tipo $|f(x)| \geq -2$ se cumple para todo $x$ en el dominio de $f$ ($S = \text{Dom}(f)$), dado que un valor absoluto siempre es mayor o igual a cero, y por ende, mayor que cualquier negativo.

---
## 6. Sistemas de Inecuaciones

Un sistema de inecuaciones consiste en dos o más inecuaciones que deben cumplirse **simultáneamente**. 

### 6.1 Método de resolución

A diferencia de los sistemas de ecuaciones (donde se usan métodos como sustitución o reducción cruzada), el enfoque para los sistemas de inecuaciones con una sola variable es estrictamente conjuntista:
1. Se resuelve cada inecuación de forma individual, obteniendo el conjunto solución para cada una.
2. Se encuentra la **intersección** ($\cap$) de todos los conjuntos solución obtenidos.
3. El resultado de dicha intersección es el conjunto solución final del sistema.

### 6.2 Ejemplos resueltos

**Ejemplo 6.1 (Sistema lineal):**
Resolver el siguiente sistema:
$$\begin{cases} 
2x - 5 < 3 \\ 
-x + 4 \leq 2 
\end{cases}$$

**Solución:**
Resolvemos la primera inecuación:
$$\begin{align}
2x - 5 &< 3 \\
2x &< 8 \\
x &< 4 \implies S_1 = (-\infty, 4)
\end{align}$$

Resolvemos la segunda inecuación:
$$\begin{align}
-x + 4 &\leq 2 \\
-x &\leq -2 \\
x &\geq 2 \quad \text{(invertimos orden por división negativa)} \\
S_2 &= [2, \infty)
\end{align}$$

Buscamos la intersección de ambos conjuntos:
$$S_{\text{total}} = S_1 \cap S_2 = (-\infty, 4) \cap [2, \infty)$$

**Respuesta:** En notación de intervalo: $[2, 4)$.

**Ejemplo 6.2 (Sistema mixto con cuadrática):**
Resolver el siguiente sistema:
$$\begin{cases} 
x^2 - 9 \leq 0 \\ 
x > 1 
\end{cases}$$

**Solución:**
Resolvemos la inecuación cuadrática factorizando la diferencia de cuadrados:
$$\begin{align}
x^2 - 9 &\leq 0 \\
(x - 3)(x + 3) &\leq 0
\end{align}$$
Las raíces son $x = 3$ y $x = -3$. Al evaluar los signos, vemos que el producto es negativo o cero en la franja comprendida entre ambas raíces:
$$S_1 = [-3, 3]$$

La segunda inecuación ya está despejada directamente:
$$S_2 = (1, \infty)$$

Intersectamos ambos conjuntos:
$$S_{\text{total}} = [-3, 3] \cap (1, \infty)$$

**Respuesta:** En notación de intervalo: $(1, 3]$.

---

## 7. Ejercicios Propuestos

1. Resuelva: $5x - 7 \leq 3x + 9$
2. Resuelva: $x^2 + x - 6 > 0$
3. Resuelva: $\frac{x - 3}{x + 1} < 2$
4. Resuelva: $|2x - 1| \leq 5$

---

## Referencias y lectura adicional

- **Stewart, J.** *Precálculo: Matemáticas para el Cálculo*, 7ª edición (2017)
- **Larson, R. & Edwards, B.** *Cálculo con Geometría Analítica*, 9ª edición (2010)

---

*Fin de Clase 4 - Inecuaciones*