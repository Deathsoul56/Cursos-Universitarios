# Funciones Parte 2

Esta clase profundiza en el análisis de funciones reales. Se establecen definiciones formales para las transformaciones geométricas (traslaciones, escalados y reflexiones), la clasificación según simetría (funciones pares e impares), las funciones definidas a tramos y una galería de funciones especiales. Posteriormente se estudian la periodicidad, las funciones hiperbólicas, la clasificación según inyectividad, sobreyectividad y biyectividad, las funciones inversas, la composición, las inversas de funciones trigonométricas e hiperbólicas, la relación entre cónicas y funciones, y una primera introducción a las funciones implícitas.

## 1. Transformaciones de Funciones

Muchas funciones que aparecen en la práctica no son completamente nuevas: son versiones modificadas de funciones elementales cuyas gráficas ya conocemos. Una parábola estirada, una raíz cuadrada desplazada o un coseno reflejado pueden construirse a partir de formas básicas sin necesidad de tabular punto a punto. El estudio sistemático de estas modificaciones se denomina **transformaciones de funciones** y constituye una herramienta fundamental para graficar, modelar y resolver problemas.

> **Nota histórica:** Las transformaciones geométricas han acompañado a las matemáticas desde la antigüedad, pero su formalización algebraica cobró fuerza con la geometría analítica de **Descartes** y **Fermat** en el siglo XVII. A lo largo del siglo XIX y XX, el concepto se generalizó en áreas como la geometría de transformaciones y el análisis funcional, donde una transformación se entiende como una función que asigna a cada punto del plano (o de un espacio más abstracto) otro punto.

### 1.1 Traslaciones (Desplazamientos)

**Definición 1.1 (Traslación vertical):**
Sea $f: D \subseteq \mathbb{R} \to \mathbb{R}$ una función y sea $c \in \mathbb{R}$, $c \neq 0$. Se define la **traslación vertical** de $f$ como la función $T_v(f): D \to \mathbb{R}$ dada por:
$$T_v(f)(x) = f(x) + c$$

- Si $c > 0$, la gráfica de $f$ se desplaza $c$ unidades hacia **arriba**.
- Si $c < 0$, la gráfica de $f$ se desplaza $|c|$ unidades hacia **abajo**.

**Ejemplo 1.1:**
Si $f(x) = x^2$, entonces $g(x) = x^2 + 3$ es la traslación vertical de $f$ en $3$ unidades hacia arriba. El vértice se mueve de $(0, 0)$ a $(0, 3)$, mientras que el dominio permanece siendo $\mathbb{R}$.

**Definición 1.2 (Traslación horizontal):**
Sea $f: D \subseteq \mathbb{R} \to \mathbb{R}$ una función y sea $a \in \mathbb{R}$, $a \neq 0$. Se define la **traslación horizontal** de $f$ como la función $T_h(f): D' \to \mathbb{R}$ dada por:
$$T_h(f)(x) = f(x - a)$$
donde $D' = \{x \in \mathbb{R} : x - a \in D\}$.

- Si $a > 0$, la gráfica de $f$ se desplaza $a$ unidades hacia la **derecha**.
- Si $a < 0$, la gráfica de $f$ se desplaza $|a|$ unidades hacia la **izquierda**.

La razón de esta inversión aparente es que para obtener el mismo valor $f(u)$ en la nueva función, la entrada debe ser $x = u + a$. Por tanto, cada punto de la gráfica original se mueve $a$ unidades en la dirección del eje $X$.

**Ejemplo 1.2:**
Si $f(x) = x^2$, entonces $g(x) = (x - 2)^2$ es la traslación horizontal de $f$ en $2$ unidades hacia la derecha. El vértice se mueve de $(0, 0)$ a $(2, 0)$.

### 1.2 Escalados (Dilataciones y Contracciones)

**Definición 1.3 (Escalado vertical):**
Sea $f: D \subseteq \mathbb{R} \to \mathbb{R}$ una función y sea $c \in \mathbb{R}$, $c \neq 0$. Se define el **escalado vertical** de $f$ como la función $E_v(f): D \to \mathbb{R}$ dada por:
$$E_v(f)(x) = c \cdot f(x)$$

- Si $|c| > 1$, la gráfica sufre una **dilatación vertical** por factor $|c|$.
- Si $0 < |c| < 1$, la gráfica sufre una **contracción vertical** por factor $|c|$.
- Si $c < 0$, además del escalado se produce una **reflexión respecto al eje $X$**.

**Ejemplo 1.3:**
Si $f(x) = x^2$, entonces $g(x) = 3x^2$ es una dilatación vertical por factor $3$. La parábola se estira, luciendo más cerrada o angosta cerca del vértice.

**Definición 1.4 (Escalado horizontal):**
Sea $f: D \subseteq \mathbb{R} \to \mathbb{R}$ una función y sea $c \in \mathbb{R}$, $c \neq 0$. Se define el **escalado horizontal** de $f$ como la función $E_h(f): D'' \to \mathbb{R}$ dada por:
$$E_h(f)(x) = f(c \cdot x)$$
donde $D'' = \{x \in \mathbb{R} : cx \in D\}$.

- Si $|c| > 1$, la gráfica sufre una **contracción horizontal** por factor $\frac{1}{|c|}$.
- Si $0 < |c| < 1$, la gráfica sufre una **dilatación horizontal** por factor $\frac{1}{|c|}$.
- Si $c < 0$, además del escalado se produce una **reflexión respecto al eje $Y$**.

**Ejemplo 1.4:**
Si $f(x) = x^2$, entonces $g(x) = \left(\frac{1}{2}x\right)^2$ es una dilatación horizontal por factor $2$. La parábola se ensancha.

### 1.3 Reflexiones

**Definición 1.5 (Reflexiones respecto a los ejes):**
Sea $f: D \subseteq \mathbb{R} \to \mathbb{R}$ una función. Se definen las siguientes reflexiones:

- **Reflexión respecto al eje $X$**: la función $R_X(f): D \to \mathbb{R}$ dada por:
  $$R_X(f)(x) = -f(x)$$
  El punto $(x, y)$ de la gráfica original se mapea al punto $(x, -y)$.

- **Reflexión respecto al eje $Y$**: la función $R_Y(f): D' \to \mathbb{R}$ dada por:
  $$R_Y(f)(x) = f(-x)$$
  donde $D' = \{x \in \mathbb{R} : -x \in D\}$. El punto $(x, y)$ se mapea al punto $(-x, y)$.

Estas dos reflexiones surgen naturalmente en fenómenos físicos: el reflejo de un rayo de luz en un espejo plano, la inversión de polaridad en una señal de sonido o la imagen de un paisaje sobre la superficie de un lago en calma.

**Ejemplo 1.5:**
Sea $f(x) = x^3 + 4$. Entonces:
- La reflexión respecto al eje $X$ es $y = -(x^3 + 4) = -x^3 - 4$.
- La reflexión respecto al eje $Y$ es $y = (-x)^3 + 4 = -x^3 + 4$.

> **Observación:** Algunas funciones elementales presentan comportamientos notables al reflejarse. Por ejemplo, $f(x) = x^2$ satisface $(-x)^2 = x^2$, por lo que su reflexión respecto al eje $Y$ coincide consigo misma. El caso $f(x) = x^3$ cumple $-x^3 = (-x)^3$, lo que hace que su reflexión en el eje $X$ sea idéntica a su reflexión en el eje $Y$. Estas simetrías se estudian formalmente en la Sección 2 como funciones pares e impares.

### 1.4 Composición de transformaciones

Las transformaciones pueden aplicarse una tras otra. El resultado final depende del orden en que se combinen, especialmente cuando intervienen escalados y traslaciones horizontales.

**Proposición 1.1 (Forma general de una función transformada):**
Sea $g: D \subseteq \mathbb{R} \to \mathbb{R}$ una función base y sean $a, b \in \mathbb{R}\setminus\{0\}$ y $h, k \in \mathbb{R}$. La función:
$$f(x) = a \cdot g\bigl(b(x - h)\bigr) + k$$

se obtiene aplicando a la gráfica de $g$, en orden, las siguientes transformaciones:
1. Escalado horizontal por factor $\frac{1}{|b|}$ (y reflexión respecto al eje $Y$ si $b < 0$).
2. Traslación horizontal de $h$ unidades.
3. Escalado vertical por factor $|a|$ (y reflexión respecto al eje $X$ si $a < 0$).
4. Traslación vertical de $k$ unidades.

**Demostración:**
Comenzamos con $y = g(x)$. Sustituimos $x$ por $b(x - h)$, lo cual comprime o expande horizontalmente la gráfica y luego la desplaza $h$ unidades. Después multiplicamos por $a$, lo que escala verticalmente la imagen, y finalmente sumamos $k$, lo que desplaza la gráfica verticalmente. Cada operación actúa sobre el resultado de la anterior, de modo que el orden indicado es el correcto. $\blacksquare$

**Ejemplo 1.6 (Transformación de la parábola):**
Graficar $f(x) = \dfrac{x^2}{2} + 5$.

Se identifica la función base $g(x) = x^2$ y se reescribe:
$$f(x) = \frac{1}{2}\,g(x) + 5$$

Las transformaciones son, en orden:

- **Contracción vertical** por $\dfrac{1}{2}$: $\quad g(x) = x^2 \;\longrightarrow\; \dfrac{x^2}{2}$

PONER GRAFICA AQUI: parábola $y = x^2$ contraída verticalmente por factor $1/2$, mostrando $y = x^2/2$.

- **Traslación vertical** $+5$: $\quad \dfrac{x^2}{2} \;\longrightarrow\; \dfrac{x^2}{2} + 5$

PONER GRAFICA AQUI: parábola $y = x^2/2$ trasladada 5 unidades hacia arriba, mostrando $y = x^2/2 + 5$.

**Ejemplo 1.7 (Desplazamiento horizontal con factor de escala):**
Determinar el desplazamiento que lleva $f(x) = |3x|$ a $g(x) = |3x + 1|$.

Factorizando el coeficiente de $x$ en el argumento de $g$:
$$g(x) = |3x + 1| = \left|3\left(x + \frac{1}{3}\right)\right| = f\left(x + \frac{1}{3}\right)$$

El desplazamiento real de la gráfica con respecto a $|3x|$ es de $\frac{1}{3}$ de unidad hacia la **izquierda**, no de $1$ unidad entera. Leer el "$+1$" como desplazamiento directo, sin factorizar primero el $3$, es el error más frecuente al realizar este tipo de transformaciones.

### 1.5 Transformaciones que no preservan la estructura funcional

Las traslaciones, escalados y reflexiones respecto a los ejes transforman una función $y = f(x)$ en otra función $y = g(x)$. Sin embargo, otras transformaciones geométricas más generales, como las reflexiones respecto a rectas oblicuas o las rotaciones, pueden producir curvas que **no** satisfacen la definición de función, pues un mismo valor de $x$ puede corresponder a varios valores de $y$. A continuación se presentan estos casos como una extensión geométrica, con la advertencia de que su resultado no siempre es una función.

#### 1.5.1 Reflexión respecto a rectas horizontales y verticales arbitrarias

Sea $f: D \subseteq \mathbb{R} \to \mathbb{R}$ una función.

- **Reflexión respecto a la recta horizontal $y = c$**: la imagen reflejada $(x, y')$ satisface que $c$ es el punto medio entre $f(x)$ e $y'$. Por tanto:
  $$\frac{f(x) + y'}{2} = c \quad \Longrightarrow \quad y' = 2c - f(x)$$
  La curva reflejada es $y = 2c - f(x)$, que sí es una función.

- **Reflexión respecto a la recta vertical $x = c$**: la imagen reflejada tiene abscisa $x'$ tal que $c$ es el punto medio entre $x$ y $x'$. Entonces:
  $$x' = 2c - x \quad \Longrightarrow \quad y = f(2c - x)$$
  La curva reflejada es $y = f(2c - x)$, que también es una función, aunque su dominio puede cambiar.

**Ejemplo 1.8 (Reflexiones en ejes arbitrarios):**
Sea $f(x) = \sqrt{x}$.
- La reflexión respecto a $y = 3$ es $y = 2(3) - \sqrt{x} = 6 - \sqrt{x}$.
- La reflexión respecto a $x = 4$ es $y = \sqrt{2(4) - x} = \sqrt{8 - x}$, con dominio $(-\infty, 8]$.

#### 1.5.2 Reflexión respecto a rectas oblicuas

Reflejar respecto a una recta oblicua $y = mx + n$ exige usar geometría analítica. Para cada punto $(x, f(x))$ de la gráfica, su reflejado $(x', y')$ debe cumplir:

1. El segmento que une $(x, f(x))$ con $(x', y')$ es perpendicular a la recta.
2. El punto medio del segmento pertenece a la recta.

Resolviendo el sistema resultante se obtiene:
$$
\begin{cases}
x' = \dfrac{(1 - m^2)x + 2m\bigl(f(x) - n\bigr)}{1 + m^2} \\[12pt]
y' = \dfrac{2mx + (m^2 - 1)f(x) + 2n}{1 + m^2}
\end{cases}
$$

> **Observación:** La curva resultante $(x', y')$ no siempre define una función $y'$ en términos de $x'$, ya que puede fallar la prueba de la línea vertical.

#### 1.5.3 Rotación

Rotar una función $y = f(x)$ un ángulo $\theta$ en sentido antihorario respecto al origen transforma cada punto $(x, f(x))$ en $(x', y')$ mediante:
$$
\begin{cases}
x' = x\cos(\theta) - f(x)\sin(\theta) \\
y' = x\sin(\theta) + f(x)\cos(\theta)
\end{cases}
$$

Nuevamente, la curva resultante no necesariamente es una función.

**Ejemplo 1.9 (Rotación de una recta):**
Sea $f(x) = mx + b$. Al rotarla $\frac{\pi}{2}$ radianes, con $\cos(\pi/2) = 0$ y $\sin(\pi/2) = 1$, se obtiene:
$$
\begin{cases}
x' = -mx - b \\
y' = x
\end{cases}
$$

Despejando $x$ de la primera ecuación y sustituyendo en la segunda:
$$x = -\frac{1}{m}x' - \frac{b}{m} \quad \Longrightarrow \quad y' = -\frac{1}{m}x' - \frac{b}{m}$$

La recta rotada es otra recta cuya pendiente es $-\frac{1}{m}$, lo que ilustra algebraicamente la condición de perpendicularidad entre rectas.

**Ejemplo 1.10 (Rotación de $f(x) = \sin(x)$):**
Al rotar la función seno un ángulo $\frac{\pi}{2}$, se obtiene:
$$
\begin{cases}
x' = -\sin(x) \\
y' = x
\end{cases}
$$
![[sin(x)_rotado.png]]
Dado que $x = y'$, la nueva curva satisface $x' = -\sin(y')$. Esta curva oscila verticalmente y falla la prueba de la línea vertical: existen infinitos valores de $y'$ para un mismo $x'$, por ejemplo cuando $x' = 0$ se tiene $y' = n\pi$ para todo $n \in \mathbb{Z}$. Por tanto, la rotación no conserva la estructura de función.

### 1.6 Aplicaciones

Las transformaciones de funciones aparecen en múltiples contextos:

- **Física:** El movimiento de un objeto que se desplaza, estira o refleja una trayectoria conocida se modela mediante traslaciones, escalados y reflexiones. Por ejemplo, una onda sinusoidal desplazada en el tiempo se representa como $f(t - t_0)$.

- **Ingeniería y diseño:** Las señales de audio, las vibraciones mecánicas y los gráficos de control se generan a partir de formas básicas modificadas por factores de escala y desplazamientos.

- **Ciencias de la computación:** Las transformaciones geométricas son la base del procesamiento de imágenes, la computación gráfica y el diseño asistido por ordenador.

- **Matemáticas aplicadas:** Muchos modelos empíricos ajustan una función conocida mediante parámetros que actúan como traslaciones y escalados: $f(x) = a \cdot g(b(x - h)) + k$.

### 1.7 Observaciones

> **Observación (orden de las transformaciones):** Cuando se aplica más de una transformación, el orden importa. En particular, una traslación horizontal seguida de un escalado horizontal no produce el mismo resultado que un escalado seguido de una traslación. Por eso se recomienda escribir la función en la forma $f(x) = a \cdot g(b(x - h)) + k$ antes de interpretar las transformaciones.

> **Observación (dominio y rango):** Las traslaciones verticales y los escalados verticales no modifican el dominio de una función, pero sí su rango. Las traslaciones horizontales y los escalados horizontales pueden modificar el dominio. Las reflexiones respecto a los ejes no cambian el dominio si este es simétrico respecto al origen, pero una reflexión respecto al eje $Y$ reemplaza el dominio $D$ por $-D = \{-x : x \in D\}$.

> **Observación (funciones que no son funciones):** Las reflexiones oblicuas y las rotaciones transforman gráficas de funciones en curvas generales del plano. Estas curvas deben estudiarse con herramientas de geometría analítica o, más adelante, con parametrizaciones.

---
## 2. Simetría de Funciones (Paridad)

Al estudiar transformaciones geométricas surgen preguntas naturales: ¿qué funciones se ven iguales al reflejarse en el eje vertical? ¿cuáles se reproducen al rotarse 180° alrededor del origen? Estas simetrías no son solo curiosidades visuales: simplifican cálculos, permiten predecir comportamientos y aparecen en modelos físicos donde ciertas cantidades deben conservarse ante cambios de signo. El lenguaje matemático que captura estas ideas es el de **funciones pares e impares**.

> **Nota histórica:** La clasificación de funciones según su comportamiento ante el cambio $x \mapsto -x$ es tan antigua como el estudio de las series de potencias en el siglo XVIII. **Leonhard Euler** observó que muchas funciones elementales podían separarse en partes simétricas y antisimétricas, lo que resultó esencial para el desarrollo del análisis de Fourier en el siglo XIX. Hoy en día, la paridad sigue siendo una herramienta básica en física, ingeniería y teoría de señales.

### 2.1 Funciones pares e impares

En toda esta sección se considerarán funciones cuyo dominio $D$ es **simétrico respecto al origen**, es decir, si $x \in D$, entonces $-x \in D$. Esta condición es necesaria para poder evaluar $f(-x)$ siempre que esté definido $f(x)$.

**Definición 2.1 (Función par):**
Sea $f: D \subseteq \mathbb{R} \to \mathbb{R}$ una función con dominio simétrico respecto al origen. Se dice que $f$ es **par** si:
$$\forall x \in D, \quad f(-x) = f(x)$$

Geométricamente, la gráfica de una función par es simétrica respecto al **eje $Y$**.

**Ejemplo 2.1:**
La función $f(x) = x^2$ es par, pues:
$$f(-x) = (-x)^2 = x^2 = f(x)$$
Otras funciones pares elementales son $f(x) = |x|$ y $f(x) = \cos(x)$.

**Definición 2.2 (Función impar):**
Sea $f: D \subseteq \mathbb{R} \to \mathbb{R}$ una función con dominio simétrico respecto al origen. Se dice que $f$ es **impar** si:
$$\forall x \in D, \quad f(-x) = -f(x)$$

Geométricamente, la gráfica de una función impar es simétrica respecto al **origen** $(0, 0)$. Esto equivale a aplicar una reflexión respecto al eje $X$ seguida de una reflexión respecto al eje $Y$.

**Ejemplo 2.2:**
La función $f(x) = x^3$ es impar, pues:
$$f(-x) = (-x)^3 = -x^3 = -f(x)$$
Otras funciones impares elementales son $f(x) = \frac{1}{x}$ y $f(x) = \sin(x)$.

### 2.2 Propiedades algebraicas

Las funciones pares e impares interactúan de manera predecible bajo sumas, productos y composiciones. Estas reglas permiten determinar la paridad de una función compleja sin volver a verificar la definición desde cero.

**Proposición 2.1 (Álgebra de funciones pares e impares):**
Sean $f$ y $g$ funciones con dominio simétrico respecto al origen.

1. **Suma:**
   - Par $+$ Par $=$ Par.
   - Impar $+$ Impar $=$ Impar.
   - Par $+$ Impar no tiene paridad definida en general.

2. **Producto:**
   - Par $\cdot$ Par $=$ Par.
   - Impar $\cdot$ Impar $=$ Par.
   - Par $\cdot$ Impar $=$ Impar.

3. **Composición:**
   - Si $g$ es par, entonces $g \circ f$ es par cualquiera sea $f$.
   - Si $g$ es impar y $f$ es impar, entonces $g \circ f$ es impar.
   - Si $g$ es impar y $f$ es par, entonces $g \circ f$ es par.

**Demostración (producto de dos funciones impares):**
Sean $f$ y $g$ funciones impares. Entonces:
$$(f \cdot g)(-x) = f(-x) \cdot g(-x) = \bigl(-f(x)\bigr) \cdot \bigl(-g(x)\bigr) = f(x) \cdot g(x) = (f \cdot g)(x)$$
Por tanto, $f \cdot g$ es par. Las demás afirmaciones se demuestran de forma análoga. $\blacksquare$

**Ejemplo 2.3:**
La función $h(x) = x^2 \sin(x)$ es impar, pues $x^2$ es par, $\sin(x)$ es impar, y el producto de una función par por una impar es impar. En efecto:
$$h(-x) = (-x)^2 \sin(-x) = x^2 \bigl(-\sin(x)\bigr) = -x^2 \sin(x) = -h(x)$$

### 2.3 Descomposición en partes par e impar

La mayoría de las funciones no son ni pares ni impares. Sin embargo, toda función con dominio simétrico puede descomponerse de manera única como suma de una función par y una función impar.

**Teorema 2.1 (Descomposición de paridad):**
Sea $f: D \subseteq \mathbb{R} \to \mathbb{R}$ una función con dominio simétrico respecto al origen. Entonces existe un único par de funciones $f_p: D \to \mathbb{R}$ par y $f_i: D \to \mathbb{R}$ impar tales que:
$$f(x) = f_p(x) + f_i(x), \quad \forall x \in D$$

Las componentes están dadas explícitamente por:
$$f_p(x) = \frac{f(x) + f(-x)}{2}, \qquad f_i(x) = \frac{f(x) - f(-x)}{2}$$

**Demostración:**
Se demuestran existencia y unicidad.

*Existencia.* Definimos $f_p$ y $f_i$ mediante las fórmulas anteriores. Sumando ambas expresiones:
$$f_p(x) + f_i(x) = \frac{f(x) + f(-x)}{2} + \frac{f(x) - f(-x)}{2} = \frac{2f(x)}{2} = f(x)$$

Además, evaluando en $-x$:
$$f_p(-x) = \frac{f(-x) + f(x)}{2} = f_p(x)$$
por lo que $f_p$ es par. Análogamente:
$$f_i(-x) = \frac{f(-x) - f(x)}{2} = -\frac{f(x) - f(-x)}{2} = -f_i(x)$$
por lo que $f_i$ es impar.

*Unicidad.* Supongamos que $f(x) = P(x) + I(x)$ con $P$ par e $I$ impar. Evaluando en $-x$ se obtiene:
$$f(-x) = P(-x) + I(-x) = P(x) - I(x)$$
Resolviendo el sistema:
$$\begin{align}
f(x) &= P(x) + I(x) \\
f(-x) &= P(x) - I(x)
\end{align}$$
se llega a:
$$P(x) = \frac{f(x) + f(-x)}{2}, \qquad I(x) = \frac{f(x) - f(-x)}{2}$$
Por tanto, $P = f_p$ e $I = f_i$. $\blacksquare$

**Ejemplo 2.4 (Descomposición de un polinomio):**
Descomponer $f(x) = x^2 + 2x + 3$ en sus partes par e impar.

Primero se calcula $f(-x) = x^2 - 2x + 3$. Entonces:
$$\begin{align}
f_p(x) &= \frac{(x^2 + 2x + 3) + (x^2 - 2x + 3)}{2} = x^2 + 3 \\
f_i(x) &= \frac{(x^2 + 2x + 3) - (x^2 - 2x + 3)}{2} = 2x
\end{align}$$

Por tanto, $f(x) = (x^2 + 3) + 2x$, donde $x^2 + 3$ es par y $2x$ es impar.

**Ejemplo 2.5 (Descomposición de la exponencial):**
Descomponer $f(x) = e^x$.

Como $f(-x) = e^{-x}$, se tiene:
$$\begin{align}
f_p(x) &= \frac{e^x + e^{-x}}{2} \\
f_i(x) &= \frac{e^x - e^{-x}}{2}
\end{align}$$

Estas expresiones definen, respectivamente, el **coseno hiperbólico** y el **seno hiperbólico**:
$$e^x = \cosh(x) + \sinh(x)$$

Esta identidad se estudiará con más detalle en la Sección 6.

### 2.4 Aplicaciones

La clasificación según paridad simplifica muchos problemas prácticos:

- **Cálculo de integrales:** En intervalos simétricos $[-a, a]$, la integral de una función impar es cero y la integral de una función par se reduce al doble de la integral en $[0, a]$. Esto acelera los cálculos y evita errores.

- **Series de Fourier:** Toda función periódica puede descomponerse en una parte par (serie de cosenos) y una parte impar (serie de senos). Esta separación es fundamental en el análisis de señales y vibraciones.

- **Física:** Muchas leyes de conservación y potenciales presentan simetrías de paridad. Un potencial eléctrico par respecto a un plano implica que el campo eléctrico es impar, y viceversa.

- **Teoría de señales:** Las señales eléctricas y acústicas se descomponen frecuentemente en componentes simétricas y antisimétricas para su análisis y filtrado.

### 2.5 Observaciones

> **Observación (dominio simétrico):** La noción de paridad solo tiene sentido cuando el dominio de la función es simétrico respecto al origen. Por ejemplo, $f(x) = \sqrt{x}$ no puede clasificarse como par ni impar porque su dominio $[0, +\infty)$ no contiene valores negativos.

> **Observación (cero en el origen):** Si $f$ es impar y $0 \in D$, entonces $f(0) = -f(0)$, lo que implica $f(0) = 0$. Esto explica por qué las funciones impares elementales como $\sin(x)$, $x^3$ y $1/x$ (en su dominio extendido) pasan por el origen o tienen una discontinuidad allí.

> **Observación (paridad y reflexiones):** La relación con las reflexiones estudiadas en la Sección 1 es directa: una función par es invariante bajo reflexión respecto al eje $Y$, mientras que una función impar es invariante bajo la composición de reflexiones respecto a los ejes $X$ e $Y$.

---
## 3. Funciones Definidas a Tramos

Muchas situaciones cotidianas cambian de regla según el valor de una variable. Una tarifa telefónica cobra distinto antes y después de cierta cantidad de minutos; un impuesto aplica porcentajes diferentes según rangos de ingreso; una señal eléctrica se activa solo cuando supera un umbral. En matemáticas, estas reglas se expresan mediante **funciones definidas a tramos**: una única función que usa distintas fórmulas en distintas partes de su dominio.

> **Nota histórica:** El uso explícito de funciones definidas por casos se consolidó en el siglo XIX, cuando los matemáticos comenzaron a construir ejemplos de funciones con comportamientos irregulares —como la función de Dirichlet o la función de Weierstrass— que desafiaban la intuición geométrica. Estas construcciones fueron decisivas para precisar conceptos como continuidad, derivabilidad e integrabilidad, que se estudiarán formalmente en cursos posteriores.

### 3.1 Definición formal

**Definición 3.1 (Función definida a tramos):**
Sea $D \subseteq \mathbb{R}$ un conjunto y sean $D_1, D_2, \ldots, D_n$ subconjuntos de $D$, dos a dos disjuntos, tales que:
$$D = D_1 \cup D_2 \cup \cdots \cup D_n$$

Una función $f: D \to \mathbb{R}$ está **definida a tramos** si para cada $i \in \{1, 2, \ldots, n\}$ existe una función $f_i: D_i \to \mathbb{R}$ tal que:
$$f(x) = f_i(x) \quad \text{si } x \in D_i$$

Equivalentemente:
$$f(x) = \begin{cases}
f_1(x) & \text{si } x \in D_1 \\
f_2(x) & \text{si } x \in D_2 \\
\vdots & \vdots \\
f_n(x) & \text{si } x \in D_n
\end{cases}$$

> **Observación:** La condición de que los conjuntos $D_i$ sean disjuntos garantiza que la función esté bien definida: cada $x \in D$ pertenece a un único tramo y, por tanto, recibe un único valor $f(x)$.

### 3.2 Ejemplos fundamentales

**Ejemplo 3.1 (Valor absoluto):**
La función valor absoluto es el ejemplo más conocido de función a tramos:
$$f(x) = |x| = \begin{cases}
-x & \text{si } x < 0 \\
x & \text{si } x \geq 0
\end{cases}$$

Para $x < 0$, el valor absoluto cambia el signo del número negativo para obtener su magnitud. Para $x \geq 0$, el número ya es no negativo y el valor absoluto no lo altera. El punto $x = 0$ es donde cambia la definición.

**Ejemplo 3.2 (Función rampa):**
La función rampa, denotada $r(x)$, se define como:
$$r(x) = \max(0, x) = \begin{cases}
0 & \text{si } x < 0 \\
x & \text{si } x \geq 0
\end{cases}$$

Esta función aparece en ingeniería eléctrica, redes neuronales (como función de activación ReLU) y economía. También puede escribirse como:
$$r(x) = \frac{x + |x|}{2}$$

**Ejemplo 3.3 (Función definida por tres tramos):**
Sea:
$$f(x) = \begin{cases}
x^2 & \text{si } x < -1 \\
1 & \text{si } -1 \leq x \leq 1 \\
2x - 1 & \text{si } x > 1
\end{cases}$$

Su evaluación en puntos concretos es:
- $f(-2) = (-2)^2 = 4$ (primer tramo)
- $f(0) = 1$ (segundo tramo)
- $f(3) = 2(3) - 1 = 5$ (tercer tramo)

**Ejemplo 3.4 (Tarifa escalonada):**
Una compañía eléctrica cobra según el consumo $k$ (en kWh):
$$C(k) = \begin{cases}
0.10k & \text{si } 0 \leq k \leq 100 \\
10 + 0.15(k-100) & \text{si } 100 < k \leq 300 \\
40 + 0.20(k-300) & \text{si } k > 300
\end{cases}$$

donde $C(k)$ es el costo en dólares. Los tramos corresponden a rangos de consumo con tarifas progresivas.

### 3.3 Dominio y evaluación

Para trabajar con una función a tramos se siguen dos pasos básicos:

1. **Determinar el dominio:** el dominio de $f$ es la unión de los dominios de todos los tramos, respetando las restricciones de cada fórmula.
2. **Evaluar en un punto:** dado $x_0 \in D$, se identifica cuál es el único tramo $D_i$ al que pertenece $x_0$ y se aplica la fórmula correspondiente $f_i(x_0)$.

**Ejemplo 3.5:**
Sea:
$$f(x) = \begin{cases}
\sqrt{x} & \text{si } 0 \leq x < 4 \\
\dfrac{8}{x} & \text{si } x \geq 4
\end{cases}$$

El dominio es $[0, +\infty)$. Para evaluar $f(2)$ se usa el primer tramo: $f(2) = \sqrt{2}$. Para evaluar $f(4)$ se usa el segundo tramo: $f(4) = \frac{8}{4} = 2$.

### 3.4 Continuidad intuitiva en los puntos de unión

En los **puntos de transición** donde cambia la fórmula, la gráfica de una función a tramos puede presentar dos comportamientos: puede **unirse sin saltos** o puede presentar un **salto**.

Aunque el estudio formal de la continuidad corresponde al tema de Límites y Continuidad, es posible verificar de manera intuitiva si una función a tramos está bien "empalmada" en un punto $x = a$ comprobando que los valores de los tramos laterales coinciden con el valor de la función en $a$.

**Ejemplo 3.6 (Función bien empalmeda):**
Sea:
$$f(x) = \begin{cases}
x + 2 & \text{si } x < 1 \\
3 & \text{si } x = 1 \\
-x + 4 & \text{si } x > 1
\end{cases}$$

Para $x = 1$:
- El tramo de la izquierda da $1 + 2 = 3$.
- El valor en el punto es $f(1) = 3$.
- El tramo de la derecha da $-1 + 4 = 3$.

Como los tres valores coinciden, la gráfica no presenta saltos en $x = 1$.

**Ejemplo 3.7 (Función con salto):**
Sea:
$$g(x) = \begin{cases}
x^2 & \text{si } x < 2 \\
x + 3 & \text{si } x \geq 2
\end{cases}$$

Para $x = 2$:
- El tramo de la izquierda da $2^2 = 4$.
- El valor en el punto es $g(2) = 2 + 3 = 5$.

Como no coinciden, la gráfica presenta un salto en $x = 2$.

> **Nota:** El concepto formal de continuidad, junto con las definiciones precisas de límite lateral y discontinuidad, se estudiará en el tema de Límites y Continuidad.

### 3.5 Aplicaciones

Las funciones a tramos modelan situaciones donde la regla de asignación cambia según condiciones:

- **Economía:** Impuestos progresivos, tarifas de servicios públicos, costos de envío por rangos de peso.
- **Ingeniería eléctrica:** Señales digitales, funciones de activación en redes neuronales (ReLU), controladores de encendido/apagado.
- **Mecánica:** Fuerzas de fricción que cambian según la dirección del movimiento, resortes con comportamientos distintos en compresión y extensión.
- **Matemáticas:** Valor absoluto, parte entera, funciones definidas por casos en problemas de optimización.

### 3.6 Observaciones

> **Observación (disjunción de tramos):** Es fundamental que los tramos sean disjuntos. Si un valor $x_0$ perteneciera a dos tramos distintos con fórmulas diferentes, la función no estaría bien definida. En la práctica, cuando las condiciones usan desigualdades estrictas en un extremo y no estrictas en el otro, como $x < a$ y $x \geq a$, se garantiza la disjunción.

> **Observación (gráfica):** Para graficar una función a tramos se dibuja cada fórmula solo sobre su dominio correspondiente. En los puntos de transición se debe indicar si el punto pertenece o no a cada tramo mediante círculos abiertos o cerrados.

> **Observación (extensión futura):** Las funciones a tramos son un terreno natural para estudiar continuidad, derivabilidad e integrabilidad. Muchas de las funciones "patológicas" que motivaron la rigurosización del análisis en el siglo XIX fueron construidas precisamente mediante definiciones a tramos o como límites de ellas.

---
## 4. Funciones Especiales y Funciones Peculiares

La definición de función es deliberadamente amplia: una regla que asigna a cada elemento de un conjunto exactamente un elemento de otro conjunto. Los polinomios, exponenciales, logaritmos y trigonométricas son ejemplos suaves y predecibles, pero la definición no exige ninguna de esas cualidades. A lo largo de la historia han surgido funciones con comportamientos irregulares que resultaron esenciales para comprender qué es posible dentro del análisis matemático y para modelar fenómenos donde las reglas cambian de manera abrupta.

> **Nota histórica:** Durante el siglo XIX, matemáticos como **Peter Gustav Lejeune Dirichlet**, **Karl Weierstrass** y **Johann Thomae** construyeron funciones que desafiaron las intuiciones dominantes sobre continuidad, derivabilidad e integrabilidad. Estos ejemplos mostraron que conceptos que parecían obvios requerían definiciones rigurosas, lo que impulsó la modernización del análisis. Al mismo tiempo, ingenieros como **Oliver Heaviside** desarrollaron funciones discontinuas para modelar circuitos eléctricos, demostrando que las matemáticas irregulares también tienen aplicaciones prácticas.

### 4.1 Función piso, función techo y parte fraccionaria

Muchos procesos cotidianos requieren convertir un número real en un entero: contar objetos completos, determinar cuántas unidades caben en una medida o calcular el tiempo transcurrido en horas enteras. Las funciones piso y techo formalizan estas operaciones, mientras que la parte fraccionaria extrae lo que sobra.

**Definición 4.1 (Función piso):**
La función piso $\lfloor \cdot \rfloor : \mathbb{R} \to \mathbb{Z}$ asigna a cada $x \in \mathbb{R}$ el mayor entero menor o igual a $x$:
$$\lfloor x \rfloor = \max\{k \in \mathbb{Z} : k \leq x\}$$

Equivalentemente, $\lfloor x \rfloor$ es el único entero que satisface:
$$\lfloor x \rfloor \leq x < \lfloor x \rfloor + 1$$

**Definición 4.2 (Función techo):**
La función techo $\lceil \cdot \rceil : \mathbb{R} \to \mathbb{Z}$ asigna a cada $x \in \mathbb{R}$ el menor entero mayor o igual a $x$:
$$\lceil x \rceil = \min\{k \in \mathbb{Z} : k \geq x\}$$

**Ejemplo 4.1:**
$$\lfloor 3.7 \rfloor = 3, \qquad \lfloor -1.2 \rfloor = -2, \qquad \lfloor 5 \rfloor = 5$$
$$\lceil 3.7 \rceil = 4, \qquad \lceil -1.2 \rceil = -1, \qquad \lceil 5 \rceil = 5$$

> **Advertencia:** Para números negativos, $\lfloor -1.2 \rfloor = -2$, no $-1$. La función piso siempre redondea hacia $-\infty$, no hacia cero.

**Definición 4.3 (Parte fraccionaria):**
La parte fraccionaria $\{\cdot\} : \mathbb{R} \to [0, 1)$ se define como:
$$\{x\} = x - \lfloor x \rfloor$$

Su gráfica es una función periódica de período 1 con forma de diente de sierra.

**Ejemplo 4.2:**
$$\{3.7\} = 0.7, \qquad \{-1.2\} = 0.8, \qquad \{5\} = 0$$

### 4.2 Función signo y función de Heaviside

Estas funciones modelan situaciones de "todo o nada": detectar el signo de una cantidad o el instante en que un fenómeno se activa. Son fundamentales en ingeniería de control, procesamiento de señales y sistemas dinámicos.

**Definición 4.4 (Función signo):**
La función signo $\operatorname{sgn} : \mathbb{R} \to \{-1, 0, 1\}$ se define como:
$$\operatorname{sgn}(x) = \begin{cases}
-1 & \text{si } x < 0 \\
0 & \text{si } x = 0 \\
1 & \text{si } x > 0
\end{cases}$$

**Definición 4.5 (Función de Heaviside):**
La función de Heaviside $H : \mathbb{R} \to \{0, 1\}$, también llamada escalón unitario, se define como:
$$H(x) = \begin{cases}
0 & \text{si } x < 0 \\
1 & \text{si } x \geq 0
\end{cases}$$

> **Nota histórica:** Oliver Heaviside (1850–1925), ingeniero eléctrico autodidacta, introdujo esta función para modelar el encendido instantáneo de circuitos eléctricos. Aunque sus métodos fueron inicialmente criticados por falta de rigor, resultaron correctos y se convirtieron en estándar de la ingeniería.

> **Nota:** En algunos textos se define $H(0) = \frac{1}{2}$ o se deja indefinido. La elección depende del contexto de aplicación.

Ambas funciones se relacionan mediante:
$$\operatorname{sgn}(x) = 2H(x) - 1, \quad \text{para } x \neq 0$$

### 4.3 Función logística (sigmoide)

Muchos procesos de crecimiento no son ilimitados: una población aumenta rápidamente al principio, pero su tasa decrece al acercarse a la capacidad de carga del ambiente. El modelo que describe este comportamiento es la función logística.

**Definición 4.6 (Función logística):**
La función logística $f : \mathbb{R} \to (0, L)$ se define como:
$$f(x) = \frac{L}{1 + e^{-k(x - x_0)}}$$
donde $L > 0$ es la cota superior, $k > 0$ es la tasa de crecimiento y $x_0 \in \mathbb{R}$ es el punto de inflexión.

La forma más simple, con $L = 1$, $k = 1$ y $x_0 = 0$, se denomina **función sigmoide estándar**:
$$\sigma(x) = \frac{1}{1 + e^{-x}}$$

La función sigmoide es ampliamente utilizada en aprendizaje automático como función de activación en redes neuronales y como salida en regresión logística, donde su recorrido $(0, 1)$ permite interpretar valores como probabilidades.

### 4.4 Función gaussiana

La función gaussiana describe la conocida "campana de Gauss". Aparece en probabilidad y estadística (distribución normal), física cuántica (paquetes de onda), óptica (perfiles de haces láser) y procesamiento de imágenes.

**Definición 4.7 (Función gaussiana):**
La función gaussiana estándar $f : \mathbb{R} \to (0, 1]$ se define como:
$$f(x) = e^{-x^2}$$

Es siempre positiva, alcanza su máximo $f(0) = 1$ y decrece simétricamente hacia cero en ambas direcciones.

> **Observación:** En Cálculo Integral se demuestra que $f(x) = e^{-x^2}$ no posee antiderivada elemental, pero el área bajo la curva en toda la recta real es $\sqrt{\pi}$.

### 4.5 Función sinc (seno cardinal)

La función sinc aparece en fenómenos de difracción en óptica y en el diseño de filtros ideales en procesamiento de señales. Su definición requiere una extensión continua en el origen.

**Definición 4.8 (Función sinc):**
La función seno cardinal $\operatorname{sinc} : \mathbb{R} \to \mathbb{R}$ se define como:
$$\operatorname{sinc}(x) = \begin{cases}
\dfrac{\sin(x)}{x} & \text{si } x \neq 0 \\
1 & \text{si } x = 0
\end{cases}$$

El valor en $x = 0$ se elige para que la función sea continua, ya que en el tema de Límites se demostrará que:
$$\lim_{x \to 0} \frac{\sin(x)}{x} = 1$$

### 4.6 Deltas: Kronecker y Dirac

En física e ingeniería surge con frecuencia la necesidad de modelar eventos concentrados en un punto: un golpe instantáneo, una carga puntual o un pulso eléctrico de duración despreciable.

**Definición 4.9 (Delta de Kronecker):**
Para $i, j \in \mathbb{Z}$, la delta de Kronecker $\delta : \mathbb{Z} \times \mathbb{Z} \to \{0, 1\}$ se define como:
$$\delta_{ij} = \begin{cases}
1 & \text{si } i = j \\
0 & \text{si } i \neq j
\end{cases}$$

Se utiliza en álgebra lineal para describir matrices identidad y sistemas ortogonales.

**Definición 4.10 (Delta de Dirac):**
La delta de Dirac es el análogo continuo de la delta de Kronecker. Intuitivamente modela un impulso concentrado en un punto: vale cero fuera del origen y su "masa" total es 1. No es una función en el sentido clásico; se define formalmente en la teoría de distribuciones, que se estudia en cursos avanzados de análisis.

Se representa de manera informal como:
$$\delta(x) = \begin{cases}
+\infty & \text{si } x = 0 \\
0 & \text{si } x \neq 0
\end{cases}$$

con la condición adicional de que su integral sobre toda la recta real es 1.

> **Advertencia:** La delta de Dirac no es una función en el sentido clásico. Ninguna función puede valer $+\infty$ en un punto y tener integral finita. Se presenta aquí como familiarización por su importancia en ingeniería de control, mecánica cuántica y ecuaciones diferenciales.

### 4.7 Función indicatriz y función de Dirichlet

La función indicatriz detecta si un elemento pertenece a un conjunto dado. Un caso particular históricamente importante es la función de Dirichlet.

**Definición 4.11 (Función indicatriz):**
Sea $A \subseteq \mathbb{R}$. La función indicatriz $\mathbf{1}_A : \mathbb{R} \to \{0, 1\}$ se define como:
$$\mathbf{1}_A(x) = \begin{cases}
1 & \text{si } x \in A \\
0 & \text{si } x \notin A
\end{cases}$$

**Definición 4.12 (Función de Dirichlet):**
La función de Dirichlet $D : \mathbb{R} \to \{0, 1\}$ es la indicatriz del conjunto de los números racionales:
$$D(x) = \mathbf{1}_{\mathbb{Q}}(x) = \begin{cases}
1 & \text{si } x \in \mathbb{Q} \\
0 & \text{si } x \notin \mathbb{Q}
\end{cases}$$

> **Nota histórica:** Dirichlet propuso esta función en 1829 como contraejemplo a la idea intuitiva de que toda función acotada es integrable. Fue uno de los primeros ejemplos que impulsaron el desarrollo riguroso del análisis.

La función de Dirichlet es discontinua en todo punto de $\mathbb{R}$, pues en cualquier vecindad de cualquier número conviven racionales e irracionales.

### 4.8 Funciones de Thomae y Weierstrass

Algunas funciones del siglo XIX mostraron que la continuidad y la derivabilidad son propiedades mucho más delicadas de lo que la intuición sugiere.

**Definición 4.13 (Función de Thomae):**
La función de Thomae $T : \mathbb{R} \to [0, 1]$ se define como:
$$T(x) = \begin{cases}
\dfrac{1}{q} & \text{si } x = \dfrac{p}{q} \in \mathbb{Q}, \text{ con } \gcd(p, q) = 1,\ q > 0 \\[6pt]
0 & \text{si } x \notin \mathbb{Q}
\end{cases}$$

Esta función es continua en todo número irracional y discontinua en todo número racional, mostrando que los conjuntos de continuidad y discontinuidad pueden tener estructuras complejas.

**Definición 4.14 (Función de Weierstrass):**
La función de Weierstrass $W : \mathbb{R} \to \mathbb{R}$ se define mediante la serie:
$$W(x) = \sum_{n=0}^{\infty} a^n \cos(b^n \pi x)$$
donde $0 < a < 1$, $b$ es un entero positivo impar y $ab > 1 + \frac{3}{2}\pi$.

> **Nota histórica:** En 1872, Weierstrass demostró que esta función es continua en toda la recta real pero no es derivable en ningún punto. Este resultado contradijo la creencia extendida de que toda función continua era derivable salvo en puntos aislados, y obligó a refundar el análisis sobre bases rigurosas.

Ambas funciones se mencionan aquí como cultura general; su estudio formal corresponde a cursos de análisis real.

### 4.9 Ondas cuadrada y triangular

En ingeniería, las señales periódicas no siempre tienen forma sinusoidal. Las ondas cuadrada y triangular son ejemplos de funciones periódicas con cambios abruptos o pendientes constantes.

**Definición 4.15 (Onda cuadrada):**
La onda cuadrada de período $2\pi$ que alterna entre $1$ y $-1$ puede expresarse como:
$$f(x) = \operatorname{sgn}(\sin(x))$$

Modela señales digitales y señales de reloj en sistemas computacionales.

**Definición 4.16 (Onda triangular):**
La onda triangular de período $T > 0$ puede expresarse mediante la parte fraccionaria:
$$f(x) = \left| 2\left\{\frac{x}{T}\right\} - 1 \right|$$

Es común en síntesis de audio y sistemas de barrido.

> **Observación:** Ambas ondas pueden descomponerse como sumas infinitas de senos y cosenos mediante series de Fourier, tema que se estudia en cursos de ecuaciones diferenciales y de señales y sistemas.

### 4.10 Aplicaciones

Las funciones especiales y las funciones con discontinuidades aparecen en múltiples áreas:

- **Ingeniería eléctrica:** La función de Heaviside modela el encendido de circuitos; la función signo representa señales bipolares; las ondas cuadrada y triangular son fundamentales en electrónica digital y audio.
- **Procesamiento de señales:** La función sinc es la respuesta en frecuencia del filtro pasabajos ideal; la delta de Dirac representa impulsos unitarios.
- **Aprendizaje automático:** La función sigmoide se usa como activación en redes neuronales; la función rampa es la base de la activación ReLU.
- **Probabilidad y estadística:** La función gaussiana describe la distribución normal, central en estadística inferencial y teoría de errores.
- **Análisis matemático:** Las funciones de Dirichlet, Thomae y Weierstrass fueron decisivas para desarrollar definiciones rigurosas de integrabilidad, continuidad y derivabilidad.

### 4.11 Observaciones

> **Observación (funciones con nombre propio):** El hecho de que una función reciba un nombre propio no implica que sea más importante que otras, sino que aparece con suficiente frecuencia como para merecer notación estandarizada. Muchas de estas funciones surgen de problemas concretos en física o ingeniería.

> **Observación (uso de conceptos futuros):** Varias de las funciones de esta sección —sinc, delta de Dirac, gaussiana, Weierstrass— se comprenden plenamente solo con herramientas de cálculo avanzado. Se presentan aquí como primera familiarización, de modo que su aparición posterior no sea sorprendente.

> **Observación (relación con funciones a tramos):** Muchas funciones de esta sección, como el valor absoluto, la función rampa, la función signo, la de Heaviside y las ondas cuadrada y triangular, son ejemplos de funciones definidas a tramos.

---
## 5. Periodicidad

Muchos fenómenos naturales y tecnológicos se repiten a intervalos regulares: el latido cardíaco, las estaciones del año, el movimiento de un péndulo, la oscilación de un circuito eléctrico o las ondas de sonido. Matemáticamente, estos comportamientos se modelan mediante **funciones periódicas**, cuya utilidad principal radica en que basta estudiar un solo ciclo para conocer la función en toda su extensión.

> **Nota histórica:** El estudio sistemático de las funciones periódicas comenzó con la astronomía antigua, donde los modelos de ciclos planetarios requerían describir movimientos repetitivos. En el siglo XVIII, **Jean-Baptiste Joseph Fourier** demostró que toda función periódica suficientemente regular puede descomponerse como suma infinita de senos y cosenos. Este resultado, conocido como **serie de Fourier**, transformó la física matemática y sigue siendo central en ingeniería, acústica, óptica y procesamiento de señales.

### 5.1 Definición y propiedades básicas

**Definición 5.1 (Función periódica):**
Sea $f: D \subseteq \mathbb{R} \to \mathbb{R}$ una función. Se dice que $f$ es **periódica** si existe un número real $T > 0$ tal que, para todo $x \in D$, se cumple:
1. $x + T \in D$
2. $f(x + T) = f(x)$

El número $T$ recibe el nombre de **período** de $f$. Si existe un período mínimo, es decir, un período positivo menor que cualquier otro, se denomina **período fundamental**.

**Proposición 5.1 (Múltiplos enteros de un período):**
Sea $f: D \to \mathbb{R}$ una función periódica con período $T$. Entonces, para todo $n \in \mathbb{Z}$ y para todo $x \in D$ tal que $x + nT \in D$, se cumple:
$$f(x + nT) = f(x)$$

**Demostración:**
Para $n = 0$ la afirmación es inmediata. Para $n > 0$ se aplica la definición de período $n$ veces:
$$f(x + nT) = f\bigl(x + (n-1)T + T\bigr) = f\bigl(x + (n-1)T\bigr) = \cdots = f(x)$$
Para $n < 0$ se razona de manera análoga desplazándose hacia la izquierda. $\blacksquare$

**Ejemplo 5.1:**
Las funciones trigonométricas son el ejemplo arquetípico de funciones periódicas:
- $f(x) = \sin(x)$ satisface $\sin(x + 2\pi) = \sin(x)$, por lo que $T = 2\pi$ es un período. De hecho, es el período fundamental.
- $g(x) = \tan(x)$ satisface $\tan(x + \pi) = \tan(x)$, por lo que su período fundamental es $\pi$.

### 5.2 Ejemplos de funciones periódicas no trigonométricas

La periodicidad no es exclusiva de las funciones trigonométricas.

**Ejemplo 5.2 (Parte fraccionaria):**
La función $f(x) = \{x\} = x - \lfloor x \rfloor$ es periódica con período $T = 1$. En efecto:
$$\begin{align}
f(x + 1) &= (x + 1) - \lfloor x + 1 \rfloor \\
&= x + 1 - (\lfloor x \rfloor + 1) \\
&= x - \lfloor x \rfloor \\
&= f(x)
\end{align}$$

Su gráfica es la conocida onda diente de sierra.

**Ejemplo 5.3 (Ondas de ingeniería):**
La onda cuadrada y la onda triangular, definidas en la Sección 4, también son funciones periódicas. En ingeniería y física, al período $T$ (medido en segundos) se le asocia una **frecuencia** $f$ (medida en Hertz) mediante:
$$f = \frac{1}{T}$$

### 5.3 Efecto del escalado horizontal

**Teorema 5.1 (Período de una función escalada):**
Sea $f: D \to \mathbb{R}$ una función periódica con período fundamental $T$. Sea $c \in \mathbb{R}\setminus\{0\}$ y sea $g(x) = f(cx)$, definida para los $x$ tales que $cx \in D$. Entonces $g$ es periódica y un período de $g$ es:
$$T_g = \frac{T}{|c|}$$

Si $T$ es el período fundamental de $f$, entonces $T/|c|$ es el período fundamental de $g$.

**Demostración:**
Sea $P = \frac{T}{|c|}$. Entonces:
$$g(x + P) = f\bigl(c(x + P)\bigr) = f(cx + cP) = f\left(cx + \frac{c}{|c|}T\right)$$
Como $f$ es periódica con período $T$, se tiene $f\left(cx + \frac{c}{|c|}T\right) = f(cx) = g(x)$. Por tanto, $P$ es un período de $g$.

La afirmación sobre el período fundamental requiere demostrar que no existe un período positivo menor que $P$; este paso se omite aquí porque utiliza propiedades de la función $f$ que se estudian en cursos de análisis. $\blacksquare$

**Ejemplo 5.4:**
Determinar el período de $h(x) = \sin(3x)$.

La función base es $\sin(x)$, cuyo período fundamental es $2\pi$, y el factor de escalado es $c = 3$. Aplicando el teorema:
$$T_h = \frac{2\pi}{3}$$

La gráfica se comprime horizontalmente: ahora la onda completa un ciclo en un intervalo tres veces más corto.

### 5.4 Cálculo de períodos en casos más complejos

**Ejemplo 5.5 (Ensanchamiento horizontal):**
Determinar el período fundamental de $f(x) = \cos\left(\frac{x}{4}\right)$.

La función base es $\cos(x)$, con período fundamental $2\pi$, y el factor de escalado es $c = \frac{1}{4}$. Por tanto:
$$T_f = \frac{2\pi}{1/4} = 8\pi$$

**Ejemplo 5.6 (Potencias trigonométricas):**
Determinar el período fundamental de $g(x) = \sin^2(x)$.

Usando la identidad del ángulo doble:
$$\sin^2(x) = \frac{1 - \cos(2x)}{2} = \frac{1}{2} - \frac{1}{2}\cos(2x)$$

La función resultante es una traslación y escalado vertical de $\cos(2x)$, cuyo período es:
$$T_g = \frac{2\pi}{2} = \pi$$

Por tanto, el período fundamental de $\sin^2(x)$ es $\pi$.

**Ejemplo 5.7 (Suma de funciones periódicas):**
Determinar el período fundamental de $h(x) = \sin(2x) + \cos(3x)$.

Los períodos de las componentes son:
$$T_1 = \frac{2\pi}{2} = \pi, \qquad T_2 = \frac{2\pi}{3}$$

El período de la suma, si existe, es el menor número positivo que es múltiplo entero de ambos. Comparando múltiplos:
- Múltiplos de $\pi$: $\pi, 2\pi, 3\pi, \ldots$
- Múltiplos de $\frac{2\pi}{3}$: $\frac{2\pi}{3}, \frac{4\pi}{3}, 2\pi, \ldots$

La primera coincidencia es $2\pi$, por lo que el período fundamental de $h$ es $T = 2\pi$.

**Ejemplo 5.8 (Suma de funciones con períodos inconmensurables):**
Determinar si $p(x) = \sin(x) + \sin(\pi x)$ es periódica.

Los períodos de las componentes son:
$$T_1 = 2\pi, \qquad T_2 = \frac{2\pi}{\pi} = 2$$

Si $p$ fuera periódica con período $T$, entonces $T$ debería ser múltiplo entero de ambos períodos. Es decir, existirían $n, m \in \mathbb{N}$ tales que:
$$T = n \cdot 2\pi = m \cdot 2$$

Despejando se obtendría:
$$\pi = \frac{m}{n}$$

lo cual es imposible porque $\pi$ es irracional. Por tanto, $p(x)$ **no es periódica**. Este tipo de funciones se denomina **cuasiperiódica** y aparece en física, por ejemplo en el estudio de cristales cuasicristalinos.

### 5.5 Construcciones periódicas a partir de funciones conocidas

Combinando funciones ya estudiadas es posible construir funciones periódicas con comportamientos variados.

**Ejemplo 5.9 (Onda diente de sierra curva):**
La función $f(x) = \{\sin(x)\}$ compone la parte fraccionaria con el seno. Donde el seno es positivo, la función coincide con $\sin(x)$; donde es negativo, la parte fraccionaria lo desplaza, generando una onda con quiebres.

**Ejemplo 5.10 (Piso del seno):**
La función $f(x) = \lfloor \sin(x) \rfloor$ toma solo los valores $-1$, $0$ y $1$. Es una función escalonada periódica que ilustra cómo una función discontinua puede surgir de una función continua.

**Ejemplo 5.11 (Seno rectificado por signo del coseno):**
La función $f(x) = \sin(x) \cdot \operatorname{sgn}(\cos(x))$ coincide con $\sin(x)$ cuando $\cos(x) > 0$ y con $-\sin(x)$ cuando $\cos(x) < 0$. Presenta discontinuidades de salto en los múltiplos impares de $\frac{\pi}{2}$.

**Ejemplo 5.12 (Alternancia de domos):**
La función $f(x) = (-1)^{\lfloor x \rfloor} \sin(\pi x)$ alterna de signo en cada intervalo entero. Es continua en todo $\mathbb{R}$ y periódica de período $2$, aunque su construcción utilice una función escalonada.

**Ejemplo 5.13 (Oscilación rápida cerca de las raíces):**
La función $f(x) = \sin\!\left(\frac{1}{\sin(x)}\right)$ está definida siempre que $\sin(x) \neq 0$. Cerca de los múltiplos de $\pi$, el argumento $\frac{1}{\sin(x)}$ crece en magnitud sin cota, por lo que la función oscila cada vez más rápido. No puede graficarse con precisión en esas vecindades.

**Ejemplo 5.14 (Onda triangular a partir del arcocoseno):**
La función $f(x) = \arccos(\cos(x))$ no coincide con la función identidad en toda la recta real. Debido a que el rango de $\arccos$ es $[0, \pi]$, la función resultante es una onda triangular periódica de período $2\pi$, dada por:
$$f(x) = |x - 2k\pi| \quad \text{para } x \in [(2k-1)\pi, (2k+1)\pi], \ k \in \mathbb{Z}$$

Este ejemplo muestra que la composición $f^{-1}(f(x))$ no siempre reduce a $x$: la inversión debe respetar los dominios y rangos de las funciones involucradas.

### 5.6 Aplicaciones

Las funciones periódicas son centrales en múltiples disciplinas:

- **Física:** Oscilaciones mecánicas, ondas electromagnéticas, sonido, movimiento planetario.
- **Ingeniería:** Señales de comunicación, circuitos de corriente alterna, control de vibraciones.
- **Música y acústica:** Las notas musicales son ondas periódicas; el timbre depende de los armónicos adicionales.
- **Biología:** Ritmos circadianos, ciclos cardíacos, patrones de población.
- **Análisis matemático:** Las series de Fourier permiten descomponer funciones periódicas complejas en sumas de senos y cosenos.

### 5.7 Observaciones

> **Observación (período y dominio):** La definición de función periódica exige que si $x \in D$, entonces $x + T \in D$. Por tanto, funciones definidas en dominios acotados no pueden ser periódicas salvo que el dominio tenga una estructura especial.

> **Observación (suma de funciones periódicas):** La suma de dos funciones periódicas es periódica solo si los cocientes de sus períodos son números racionales. Si los períodos son inconmensurables, como en el Ejemplo 5.8, la suma es cuasiperiódica.

> **Observación (series de Fourier):** Toda función periódica suficientemente regular puede aproximarse mediante una suma infinita de senos y cosenos. Este resultado justifica por qué el estudio detallado de las funciones trigonométricas es tan importante en matemáticas aplicadas.

---

## 6. Funciones Hiperbólicas

Pensemos en un cable eléctrico colgado entre dos postes, una cadena suspendida por sus extremos o incluso el arco de una vela tensada por el viento. A primera observación, estas curvas parecen parábolas, pero no lo son: su forma exacta está descrita por la curva catenaria que matemáticamente se representa mediante la función **coseno hiperbólico**. Del mismo modo, cuando se estudia el movimiento acelerado en la relatividad especial o ciertas ecuaciones diferenciales sencillas, aparecen combinaciones de exponenciales $e^x$ y $e^{-x}$ que resultan ser más naturales de escribir como $\sinh(x)$ y $\cosh(x)$. Estas funciones no son una mera curiosidad notacional: organizan simetrías, simplifican fórmulas y conectan el álgebra exponencial con la geometría de la hipérbola de una manera tan limpia como los senos y cosenos conectan la exponencial imaginaria con la circunferencia.

> **Nota histórica:** Aunque las combinaciones exponenciales $e^x \pm e^{-x}$ eran conocidas desde el siglo XVII, el estudio sistemático de las funciones hiperbólicas como familia independiente comenzó con **Vincenzo Riccati**, quien en 1757 publicó *Opuscula ad res physicas et mathematicas pertinentia* y acuñó los nombres *sinus hyperbolicus* y *cosinus hyperbolicus*. Poco después, **Johann Heinrich Lambert** (alrededor de 1768) profundizó en sus propiedades y estableció conexiones con la geometría de la hipérbola. Curiosamente, Lambert también fue uno de los primeros en demostrar que $\pi$ es irracional, el mismo tipo de obstáculo que encontramos cuando dos funciones trigonométricas tienen períodos inconmensurables.

### 6.1 Origen analítico: la descomposición de la exponencial

En la Sección 2.3 se introdujo el Teorema de Descomposición de Paridad, el cual establece que cualquier función real sobre un dominio simétrico puede expresarse de manera única como la suma de una función par y una función impar. Al aplicar este teorema a la función exponencial elemental $f(x) = e^x$, se obtienen de manera natural sus dos componentes de paridad:

- **Componente par (Coseno hiperbólico):**
  $$f_{\text{par}}(x) = \dfrac{e^x + e^{-x}}{2}$$

- **Componente impar (Seno hiperbólico):**
  $$f_{\text{impar}}(x) = \dfrac{e^x - e^{-x}}{2}$$

Estas componentes estructuran una de las familias más importantes del análisis matemático. De esta descomposición surge de forma directa la identidad:
$$e^x = \cosh(x) + \sinh(x)$$

> **Nota de conexión algebraica:** Mediante la fórmula de Euler ($e^{ix} = \cos(x) + i\sin(x)$), las funciones trigonométricas y las hiperbólicas se conectan a través de argumentos imaginarios: $\cos(ix) = \cosh(x)$ y $\sin(ix) = i\sinh(x)$. Esta correspondencia y su demostración formal se estudiarán en detalle en el curso de Álgebra. En este curso de Cálculo nos limitaremos a su análisis real.
### 6.2 Definiciones formales y analogía geométrica

**Definición 6.1 (Seno hiperbólico y Coseno hiperbólico):**
Se definen las funciones **seno hiperbólico** $\sinh: \mathbb{R} \to \mathbb{R}$ y **coseno hiperbólico** $\cosh: \mathbb{R} \to [1, +\infty)$ mediante:
$$\sinh(x) = \dfrac{e^x - e^{-x}}{2}, \qquad \cosh(x) = \dfrac{e^x + e^{-x}}{2}$$

Ambas funciones tienen dominio $\mathbb{R}$. El recorrido de $\sinh$ es todo $\mathbb{R}$; el recorrido de $\cosh$ es $[1, +\infty)$, pues $e^x + e^{-x} \geq 2$ para todo $x \in \mathbb{R}$ por la desigualdad entre la media aritmética y la media geométrica.

Antes de explorar la analogía geométrica que les da nombre, conviene visualizar el comportamiento de $\sinh(x)$ y $\cosh(x)$. La siguiente tabla muestra valores numéricos que anticipan la forma de sus gráficas: $\sinh$ crece de manera monótona pasando por el origen, mientras que $\cosh$ es una curva en forma de U con mínimo en $(0, 1)$.

| $x$ | $-4$ | $-3$ | $-2$ | $-1$ | $0$ | $1$ | $2$ | $3$ | $4$ |
| :--: | :--: | :--: | :--: | :--: | :-: | :--: | :--: | :--: | :--: |
| $\sinh(x)$ | $-27.29$ | $-10.02$ | $-3.63$ | $-1.18$ | $0$ | $1.18$ | $3.63$ | $10.02$ | $27.29$ |
| $\cosh(x)$ | $27.31$ | $10.07$ | $3.76$ | $1.54$ | $1$ | $1.54$ | $3.76$ | $10.07$ | $27.31$ |

PONER GRAFICA AQUI: gráficas de $y = \sinh(x)$ y $y = \cosh(x)$ en el mismo sistema de ejes, destacando el mínimo $(0, 1)$ de $\cosh$ y el origen para $\sinh$.

La denominación "hiperbólicas" proviene de una analogía geométrica exacta con las funciones trigonométricas. En trigonometría ordinaria, al variar un parámetro angular $t$, el punto $(\cos(t), \sin(t))$ describe la **circunferencia unitaria** $x^2 + y^2 = 1$. En el caso hiperbólico, al variar un parámetro real $t$, el punto $(\cosh(t), \sinh(t))$ satisface:

$$\cosh^2(t) - \sinh^2(t) = 1$$

por el Teorema 6.1, de modo que describe la rama derecha de la **hipérbola equilátera unitaria** $x^2 - y^2 = 1$. Además, el parámetro $t$ representa algebraicamente el doble del área del sector hiperbólico determinado por la curva, en completa analogía con el hecho de que el ángulo $t$ en radianes es el doble del área del sector circular en la circunferencia unitaria.

PONER GRAFICA AQUI: hipérbola equilátera $x^2 - y^2 = 1$ con la rama derecha parametrizada por $(\cosh t, \sinh t)$.

**Proposición 6.1 (Propiedades básicas de $\sinh$ y $\cosh$):**
Para todo $x \in \mathbb{R}$ se verifican las siguientes propiedades:

1. **Paridad:** $\sinh(-x) = -\sinh(x)$ (función impar) y $\cosh(-x) = \cosh(x)$ (función par).
2. **Cota inferior del coseno hiperbólico:** $\cosh(x) \geq 1$, con igualdad si y solo si $x = 0$.
3. **Comportamiento en el origen:** $\sinh(0) = 0$ y $\cosh(0) = 1$.
4. **Monotonía:** $\sinh$ es estrictamente creciente en $\mathbb{R}$; $\cosh$ es estrictamente decreciente en $(-\infty, 0]$ y estrictamente creciente en $[0, +\infty)$.

**Demostración:**
Las propiedades de paridad se siguen directamente de las definiciones exponenciales. En efecto:
$$\sinh(-x) = \dfrac{e^{-x} - e^{x}}{2} = -\dfrac{e^{x} - e^{-x}}{2} = -\sinh(x)$$
$$\cosh(-x) = \dfrac{e^{-x} + e^{x}}{2} = \cosh(x)$$

La cota inferior de $\cosh$ se obtiene de la desigualdad $a + b \geq 2\sqrt{ab}$ aplicada a $a = e^x$ y $b = e^{-x}$, lo cual da $e^x + e^{-x} \geq 2$, es decir, $\cosh(x) \geq 1$. La igualdad ocurre cuando $e^x = e^{-x}$, es decir, cuando $x = 0$.

Los valores en el origen se calculan sustituyendo $x = 0$ en las definiciones.

La monotonía de $\sinh$ puede justificarse observando que $e^x$ es creciente y $e^{-x}$ es decreciente, de modo que su diferencia es estrictamente creciente. Para $\cosh$, la función es par y alcanza su mínimo global en $x = 0$, por lo que decrece hacia la izquierda del origen y crece hacia la derecha. $\blacksquare$

### 6.3 Identidad fundamental

**Teorema 6.1 (Identidad hiperbólica fundamental):**
Para todo $x \in \mathbb{R}$, se verifica la relación:
$$\cosh^2(x) - \sinh^2(x) = 1$$

**Demostración:**
Sustituimos las expresiones exponenciales correspondientes a cada función en el miembro izquierdo de la identidad:
$$\begin{align}
\cosh^2(x) - \sinh^2(x) &= \left(\dfrac{e^x + e^{-x}}{2}\right)^2 - \left(\dfrac{e^x - e^{-x}}{2}\right)^2 \\[10pt]
&= \dfrac{e^{2x} + 2e^x e^{-x} + e^{-2x}}{4} - \dfrac{e^{2x} - 2e^x e^{-x} + e^{-2x}}{4} \\[10pt]
&= \dfrac{(e^{2x} + 2 + e^{-2x}) - (e^{2x} - 2 + e^{-2x})}{4} \\[10pt]
&= \dfrac{4}{4} = 1
\end{align}$$
Queda demostrada la identidad. $\blacksquare$

### 6.4 Otras funciones hiperbólicas

A partir de $\sinh$ y $\cosh$ se definen las funciones hiperbólicas restantes en correspondencia con las razones trigonométricas.

**Definición 6.2 (Otras funciones hiperbólicas):**
Se definen las funciones:

- **Tangente hiperbólica:**
  $$\tanh: \mathbb{R} \to (-1, 1), \qquad \tanh(x) = \dfrac{\sinh(x)}{\cosh(x)} = \dfrac{e^x - e^{-x}}{e^x + e^{-x}}$$

- **Cotangente hiperbólica:**
  $$\coth: \mathbb{R} \setminus \{0\} \to (-\infty, -1) \cup (1, +\infty), \qquad \coth(x) = \dfrac{\cosh(x)}{\sinh(x)} = \dfrac{e^x + e^{-x}}{e^x - e^{-x}}$$

- **Secante hiperbólica:**
  $$\operatorname{sech}: \mathbb{R} \to (0, 1], \qquad \operatorname{sech}(x) = \dfrac{1}{\cosh(x)} = \dfrac{2}{e^x + e^{-x}}$$

- **Cosecante hiperbólica:**
  $$\operatorname{csch}: \mathbb{R} \setminus \{0\} \to \mathbb{R} \setminus \{0\}, \qquad \operatorname{csch}(x) = \dfrac{1}{\sinh(x)} = \dfrac{2}{e^x - e^{-x}}$$

**Proposición 6.2 (Comportamiento asintótico y paridad de $\tanh$):**
La función $\tanh$ es impar, estrictamente creciente en $\mathbb{R}$, y satisface:
$$\lim_{x \to +\infty} \tanh(x) = 1, \qquad \lim_{x \to -\infty} \tanh(x) = -1$$
Por tanto, su gráfica tiene asíntotas horizontales $y = 1$ e $y = -1$.

**Demostración:**
La imparidad se sigue de la imparidad de $\sinh$ y la paridad de $\cosh$:
$$\tanh(-x) = \dfrac{\sinh(-x)}{\cosh(-x)} = \dfrac{-\sinh(x)}{\cosh(x)} = -\tanh(x)$$

Para los límites, multiplicamos numerador y denominador de la expresión exponencial por $e^{-x}$:
$$\tanh(x) = \dfrac{1 - e^{-2x}}{1 + e^{-2x}}$$
Cuando $x \to +\infty$, se tiene $e^{-2x} \to 0$, de modo que $\tanh(x) \to 1$. Cuando $x \to -\infty$, se escribe $\tanh(x) = \dfrac{e^{2x} - 1}{e^{2x} + 1}$, y como $e^{2x} \to 0$, se obtiene $\tanh(x) \to -1$. La monotonía estricta se deduce del crecimiento de $\sinh$ y de que $\cosh$ es positiva. $\blacksquare$

PONER GRAFICA AQUI: gráfica de $y = \tanh(x)$ con las asíntotas horizontales $y = 1$ e $y = -1$.

### 6.5 Ejemplos

**Ejemplo 6.1 (Evaluación en el origen):**
Calcular $\sinh(0)$, $\cosh(0)$ y verificar la identidad fundamental en $x = 0$.

**Solución:**
Sustituyendo $x = 0$ en las definiciones:
$$\sinh(0) = \dfrac{e^0 - e^{-0}}{2} = \dfrac{1 - 1}{2} = 0$$
$$\cosh(0) = \dfrac{e^0 + e^{-0}}{2} = \dfrac{1 + 1}{2} = 1$$

Por tanto:
$$\cosh^2(0) - \sinh^2(0) = 1^2 - 0^2 = 1$$
lo cual confirma el Teorema 6.1 para este caso particular.

**Ejemplo 6.2 (Simplificación de una tangente hiperbólica):**
Calcular el valor exacto de $\tanh(\ln 2)$.

**Solución:**
Usando la expresión exponencial de $\tanh$:
$$\tanh(\ln 2) = \dfrac{e^{\ln 2} - e^{-\ln 2}}{e^{\ln 2} + e^{-\ln 2}} = \dfrac{2 - \frac{1}{2}}{2 + \frac{1}{2}} = \dfrac{\frac{3}{2}}{\frac{5}{2}} = \dfrac{3}{5}$$

Por lo tanto, $\tanh(\ln 2) = \dfrac{3}{5}$.

**Ejemplo 6.3 (Verificación de la identidad fundamental):**
Verificar que $\cosh^2(\ln 3) - \sinh^2(\ln 3) = 1$ mediante cálculo directo.

**Solución:**
Calculamos por separado:
$$\cosh(\ln 3) = \dfrac{3 + \frac{1}{3}}{2} = \dfrac{\frac{10}{3}}{2} = \dfrac{5}{3}$$
$$\sinh(\ln 3) = \dfrac{3 - \frac{1}{3}}{2} = \dfrac{\frac{8}{3}}{2} = \dfrac{4}{3}$$

Entonces:
$$\cosh^2(\ln 3) - \sinh^2(\ln 3) = \left(\dfrac{5}{3}\right)^2 - \left(\dfrac{4}{3}\right)^2 = \dfrac{25}{9} - \dfrac{16}{9} = \dfrac{9}{9} = 1$$
como predice el Teorema 6.1.

**Ejemplo 6.4 (Punto sobre una hipérbola):**
Determinar las coordenadas del punto sobre la hipérbola $x^2 - y^2 = 1$ que corresponde al parámetro $t = \ln 2$.

**Solución:**
El punto buscado es $(\cosh(\ln 2), \sinh(\ln 2))$. Calculamos:
$$\cosh(\ln 2) = \dfrac{2 + \frac{1}{2}}{2} = \dfrac{5}{4}, \qquad \sinh(\ln 2) = \dfrac{2 - \frac{1}{2}}{2} = \dfrac{3}{4}$$

Así, el punto es $\left(\dfrac{5}{4}, \dfrac{3}{4}\right)$. Se verifica directamente que:
$$\left(\dfrac{5}{4}\right)^2 - \left(\dfrac{3}{4}\right)^2 = \dfrac{25}{16} - \dfrac{9}{16} = \dfrac{16}{16} = 1$$

### 6.6 Identidades hiperbólicas

Así como existen identidades trigonométricas que simplifican expresiones con senos y cosenos, también existen identidades para las funciones hiperbólicas. Resulta curioso que muchas de estas identidades tienen una forma muy parecida a las trigonométricas, aunque sus demostraciones parten de las definiciones exponenciales y no de la geometría de la circunferencia.

Por ejemplo, la fórmula del seno doble:
$$\sinh(2x) = 2\sinh(x)\cosh(x)$$

tiene exactamente la misma estructura que la identidad circular $\sin(2x) = 2\sin(x)\cos(x)$. Sin embargo, la demostración hiperbólica se obtiene directamente de las definiciones:
$$2\sinh(x)\cosh(x) = 2 \cdot \dfrac{e^x - e^{-x}}{2} \cdot \dfrac{e^x + e^{-x}}{2} = \dfrac{e^{2x} - e^{-2x}}{2} = \sinh(2x)$$

Algunas identidades adicionales que aparecen con frecuencia son:
- $\cosh(2x) = \cosh^2(x) + \sinh^2(x)$ (compare con $\cos(2x) = \cos^2(x) - \sin^2(x)$)
- $\cosh^2(x) - \sinh^2(x) = 1$ (la identidad fundamental)
- $\sinh(x \pm y) = \sinh(x)\cosh(y) \pm \cosh(x)\sinh(y)$
- $\cosh(x \pm y) = \cosh(x)\cosh(y) \pm \sinh(x)\sinh(y)$

La coincidencia formal entre ambas familias de identidades no es casual: está gobernada por la fórmula de Euler y el paso de argumentos reales a imaginarios. No obstante, conviene recordar que los signos no siempre se preservan, por lo que cada identidad hiperbólica debe verificarse algebraicamente antes de usarse.

### 6.7 Aplicaciones

Las funciones hiperbólicas aparecen de manera recurrente en contextos donde coexisten comportamientos crecientes y decrecientes exponenciales, o donde la geometría de la hipérbola juega un papel central.

- **Mecánica y arquitectura (catenaria):** La curva que describe un cable o una cadena homogénea colgada bajo su propio peso no es una parábola, sino una catenaria. En su forma más simple, su ecuación es $y = a \cosh\!\left(\dfrac{x}{a}\right)$, donde $a$ es una constante que depende de la tensión y del peso por unidad de longitud. Este modelo explica la forma de cables de suspensión, líneas de transmisión eléctrica y arcos arquitectónicos como el Arco Gateway de San Luis.

- **Relatividad especial:** Las transformaciones de Lorentz, que relacionan las coordenadas espaciotemporales de dos observadores en movimiento relativo uniforme, pueden parametrizarse mediante funciones hiperbólicas. Si $\phi$ es la rapidez (ángulo hiperbólico), las transformaciones se escriben $x' = x \cosh(\phi) - ct \sinh(\phi)$ y $ct' = -x \sinh(\phi) + ct \cosh(\phi)$. Esta forma pone de relieve la analogía formal entre rotaciones espaciales y "rotaciones" en el espaciotiempo.

- **Ecuaciones diferenciales:** La ecuación lineal de segundo orden $y'' - y = 0$ tiene como soluciones generales combinaciones de $e^x$ y $e^{-x}$, que pueden reescribirse como $y(x) = A \cosh(x) + B \sinh(x)$. Esta representación resulta especialmente útil cuando las condiciones iniciales o de contorno presentan simetrías par o impar, pues separa de manera natural las contribuciones simétricas y antisimétricas.

- **Geometría hiperbólica:** En modelos como el disco de Poincaré o el semiplano superior, las distancias y las geodésicas se expresan mediante funciones hiperbólicas. El coseno hiperbólico aparece, por ejemplo, en la fórmula de la distancia hiperbólica entre dos puntos.

### 6.8 Observaciones

> **Observación (sobre las funciones inversas):** La definición y análisis formal de las funciones hiperbólicas inversas, como el argumento del seno hiperbólico $\operatorname{arsinh}(x)$ o el argumento del coseno hiperbólico $\operatorname{argcosh}(x)$, se posponen para secciones posteriores del curso, una vez establecidos de manera rigurosa los conceptos generales de inyectividad e invertibilidad de funciones reales.

> **Observación (analogía trigonométrica):** Muchas identidades hiperbólicas pueden recordarse a partir de las identidades trigonométricas circulares cambiando el signo de los términos que contienen productos de dos senos hiperbólicos. Por ejemplo, la identidad circular $\cos^2(x) + \sin^2(x) = 1$ se convierte en $\cosh^2(x) - \sinh^2(x) = 1$. No obstante, esta regla mnemotécnica no sustituye una verificación algebraica directa.

> **Observación (notación):** En la literatura en español se encuentran distintas notaciones para las funciones inversas hiperbólicas: $\operatorname{arsinh}(x)$, $\operatorname{argsinh}(x)$, $\operatorname{asinh}(x)$ para el seno hiperbólico inverso, y análogamente para las demás. Todas ellas se refieren al mismo objeto matemático.

---

## 7. Clasificación de Funciones

Pensemos en una base de datos donde cada cliente debe recibir un número de identificación único, o en un teatro donde cada asiento debe estar ocupado, o en un salón de clases donde cada estudiante debe tener exactamente un pupitre. En cada caso, la relación entre dos conjuntos tiene propiedades distintas: a veces no se repiten valores, a veces no sobran elementos en el conjunto de llegada, y a veces ambas condiciones se cumplen a la vez. Estas tres situaciones corresponden, respectivamente, a las funciones inyectivas, sobreyectivas y biyectivas. Clasificar una función de este modo no es un ejercicio abstracto: es el primer paso para saber si una función puede invertirse, si preserva información, o si dos conjuntos tienen el mismo "tamaño".

> **Nota histórica:** La noción moderna de función como correspondencia arbitraria entre conjuntos fue consolidada por **Peter Gustav Lejeune Dirichlet** en 1837, al separar la idea de función de la de fórmula explícita. Más tarde, a finales del siglo XIX, **Georg Cantor** utilizó las funciones biyectivas como herramienta fundamental para comparar el tamaño de conjuntos infinitos, demostrando que existen diferentes "grados" de infinito. La notación estándar $f: A \to B$ para indicar dominio y codominio fue popularizada por el grupo **Nicolas Bourbaki** en sus tratados de mediados del siglo XX.

### 7.1 Dominio, codominio e imagen

Antes de clasificar una función, es necesario distinguir con precisión tres conjuntos que suelen confundirse: el dominio, el codominio y la imagen.

**Definición 7.1 (Dominio, codominio e imagen):**
Dada una función $f: A \to B$:

- El conjunto $A$ se denomina **dominio** de $f$, denotado $\text{Dom}(f)$. Es el conjunto de todas las entradas permitidas.
- El conjunto $B$ se denomina **codominio** de $f$. Es el conjunto de llegada donde se declara que toman valores las salidas.
- La **imagen** o **recorrido** de $f$, denotada $\text{Im}(f)$ o $f(A)$, es el conjunto de todos los valores que la función realmente alcanza:
  $$\text{Im}(f) = \{ y \in B : \exists x \in A \text{ tal que } f(x) = y \}$$

Siempre se cumple que $\text{Im}(f) \subseteq B$. La diferencia entre codominio e imagen es esencial: el codominio es parte de la definición de la función, mientras que la imagen es el resultado de evaluarla.

PONER GRAFICA AQUI: diagrama de correspondencia entre dos conjuntos $A$ y $B$ mediante flechas, destacando el dominio, el codominio y la imagen como subconjunto del codominio.

**Ejemplo 7.1 (Identificación de dominio, codominio e imagen):**
Sea $f: \mathbb{R} \to \mathbb{R}$ definida por $f(x) = x^2$.

- **Dominio:** $\text{Dom}(f) = \mathbb{R}$.
- **Codominio:** $\mathbb{R}$, tal como fue declarado.
- **Imagen:** $\text{Im}(f) = [0, +\infty)$, pues todo número real no negativo es el cuadrado de algún real, pero ningún número negativo puede obtenerse como cuadrado de un real.

Observemos que si se redefine la misma regla con codominio $[0, +\infty)$, es decir, $f: \mathbb{R} \to [0, +\infty)$ dada por $f(x) = x^2$, la función cambia como objeto matemático, aunque la regla algebraica sea idéntica.

### 7.2 Inyectividad

Imaginemos que estamos asignando llaves a habitaciones en un hotel. Si asignamos la misma llave a dos habitaciones distintas, se generará un conflicto de duplicación. En matemáticas, la inyectividad representa la garantía de que no existan tales colisiones: a elementos distintos del dominio les corresponden siempre resultados distintos en el codominio.

**Definición 7.2 (Función Inyectiva):**
Sea $f: A \to B$ una función. Se dice que $f$ es **inyectiva** (o uno a uno) si elementos distintos del dominio $A$ producen imágenes distintas en el codominio $B$. Formalmente:
$$\forall x_1, x_2 \in A, \quad x_1 \neq x_2 \implies f(x_1) \neq f(x_2)$$
Equivalentemente, aplicando la contrapositiva:
$$\forall x_1, x_2 \in A, \quad f(x_1) = f(x_2) \implies x_1 = x_2$$

**Proposición 7.1 (Prueba de la línea horizontal):**
Una función real de variable real $f: \text{Dom}(f) \to \mathbb{R}$ es inyectiva si y solo si cualquier recta horizontal de la forma $y = c$ (donde $c \in \mathbb{R}$) intersecta a su gráfica a lo sumo en un punto.

**Demostración:**
Si la función es inyectiva, dos valores distintos de $x$ no pueden tener la misma imagen $y$, por lo que ninguna recta horizontal puede cortar la gráfica en más de un punto. Recíprocamente, si toda recta horizontal corta la gráfica a lo sumo una vez, entonces para cada $y$ existe a lo sumo una preimagen, lo cual es precisamente la definición de inyectividad. $\blacksquare$

PONER GRAFICA AQUI: ejemplo de prueba de la línea horizontal con una función inyectiva (por ejemplo, $f(x)=x^3$) y una no inyectiva (por ejemplo, $f(x)=x^2$), mostrando una recta horizontal que corta una sola vez en el primer caso y dos veces en el segundo.

**Ejemplo 7.2 (Función lineal inyectiva):**
Demostrar que la función $f: \mathbb{R} \to \mathbb{R}$ definida por $f(x) = 3x - 5$ es inyectiva.

**Solución:**
Sean $x_1, x_2 \in \mathbb{R}$ tales que $f(x_1) = f(x_2)$. Entonces:
$$\begin{align}
3x_1 - 5 &= 3x_2 - 5 \\
3x_1 &= 3x_2 \\
x_1 &= x_2
\end{align}$$
Dado que $f(x_1) = f(x_2)$ implica necesariamente que $x_1 = x_2$, la función es inyectiva.

**Ejemplo 7.3 (Función cuadrática no inyectiva):**
Demostrar que la función $f: \mathbb{R} \to \mathbb{R}$ definida por $f(x) = x^2$ no es inyectiva.

**Solución:**
Basta con exhibir un contraejemplo. Sean $x_1 = 2$ y $x_2 = -2$. Se tiene que $x_1 \neq x_2$, sin embargo:
$$f(2) = 4 \quad \text{y} \quad f(-2) = 4$$
Por lo tanto, $f(2) = f(-2)$ con $2 \neq -2$, lo cual viola la definición de inyectividad.

> **Observación:** La inyectividad depende críticamente de la delimitación del dominio. Si se restringe el dominio de $f(x) = x^2$ a los reales no negativos, es decir, $f: [0, +\infty) \to \mathbb{R}$, la función resulta inyectiva, pues cada valor de $y$ positivo proviene de una única $x$ no negativa.

### 7.3 Sobreyectividad

Supongamos que en un teatro cada asiento en la sala debe ser ocupado por al menos un espectador. Si al comenzar la función no queda ningún asiento vacío, hemos cubierto la capacidad de la sala por completo. En matemáticas, una función es sobreyectiva si su conjunto de llegada (codominio) está completamente "cubierto" por los valores que la función realmente toma (su imagen). No quedan elementos sin preimagen en el codominio.

**Definición 7.3 (Función Sobreyectiva):**
Sea $f: A \to B$ una función. Se dice que $f$ es **sobreyectiva** (o sobre) si todo elemento del codominio $B$ es la imagen de al menos un elemento del dominio $A$. Formalmente:
$$\forall y \in B, \quad \exists x \in A \text{ tal que } f(x) = y$$
Esto es equivalente a afirmar que la imagen de la función coincide exactamente con su codominio: $\text{Im}(f) = B$.

**Ejemplo 7.4 (Función cuadrática no sobreyectiva):**
Analizar si la función $f: \mathbb{R} \to \mathbb{R}$ definida por $f(x) = x^2$ es sobreyectiva.

**Solución:**
El codominio declarado es $\mathbb{R}$. Consideremos $y = -1$. Si existiera $x \in \mathbb{R}$ tal que $f(x) = -1$, se tendría $x^2 = -1$, lo cual es imposible en los números reales. Por tanto, $y = -1$ carece de preimagen y la función no es sobreyectiva. Su imagen es $\text{Im}(f) = [0, +\infty) \neq \mathbb{R}$.

**Ejemplo 7.5 (Función cuadrática sobreyectiva):**
Determinar si la función $f: \mathbb{R} \to [0, +\infty)$ definida por $f(x) = x^2$ es sobreyectiva.

**Solución:**
Ahora el codominio coincide con la imagen natural de la función. Para cualquier $y \in [0, +\infty)$, podemos tomar $x = \sqrt{y}$, que es un número real bien definido. Entonces:
$$f(\sqrt{y}) = (\sqrt{y})^2 = y$$
Como todo elemento del codominio tiene al menos una preimagen, la función es sobreyectiva.

> **Observación:** Los Ejemplos 7.4 y 7.5 muestran que la sobreyectividad no es una propiedad de la sola fórmula algebraica, sino que depende de la elección explícita del codominio.

### 7.4 Biyectividad

Imaginemos un salón de clases donde cada estudiante está sentado en exactamente un pupitre, y no queda ningún pupitre libre ni ningún alumno de pie. Esta correspondencia perfecta, donde no hay duplicaciones (inyectividad) y no sobra ningún asiento (sobreyectividad), es lo que conocemos como biyectividad. Es una relación simétrica e ideal porque permite conectar dos conjuntos de manera bidireccional y totalmente reversible.

**Definición 7.4 (Función Biyectiva):**
Una función $f: A \to B$ es **biyectiva** si es simultáneamente inyectiva y sobreyectiva.

PONER GRAFICA AQUI: diagrama de función biyectiva con conjuntos $A$ y $B$ del mismo tamaño finito, mostrando una correspondencia perfecta uno a uno mediante flechas.

**Ejemplo 7.6 (Función lineal biyectiva):**
Determinar si la función $f: \mathbb{R} \to \mathbb{R}$ definida por $f(x) = 2x + 1$ es biyectiva.

**Solución:**
Se verifican ambas condiciones por separado.

1. **Inyectividad:** Sean $x_1, x_2 \in \mathbb{R}$ tales que $f(x_1) = f(x_2)$. Entonces:
   $$\begin{align}
   2x_1 + 1 &= 2x_2 + 1 \\
   2x_1 &= 2x_2 \\
   x_1 &= x_2
   \end{align}$$
   Por tanto, $f$ es inyectiva.

2. **Sobreyectividad:** Sea $y \in \mathbb{R}$. Buscamos $x \in \mathbb{R}$ tal que $f(x) = y$:
   $$\begin{align}
   2x + 1 &= y \\
   x &= \dfrac{y - 1}{2}
   \end{align}$$
   Dado que $\dfrac{y-1}{2}$ es un número real para todo $y \in \mathbb{R}$, toda salida tiene preimagen. Por tanto, $f$ es sobreyectiva.

Como $f$ es inyectiva y sobreyectiva, es biyectiva.

### 7.5 Aplicaciones

La clasificación de funciones no es un mero etiquetado teórico: responde preguntas concretas sobre reversibilidad, tamaño de conjuntos y diseño de sistemas.

- **Existencia de inversas:** Una función biyectiva es exactamente aquella que puede invertirse de manera unívoca. La inyectividad garantiza que la inversa esté bien definida (sin ambigüedades), mientras que la sobreyectividad garantiza que la inversa esté definida en todo el codominio. Este tema se desarrolla rigurosamente en la Sección 8.

- **Cardinalidad y teoría de conjuntos:** Cantor utilizó las biyecciones para comparar el tamaño de conjuntos, incluso conjuntos infinitos. Dos conjuntos tienen la misma cardinalidad si y solo si existe una función biyectiva entre ellos. De este modo se demuestra, por ejemplo, que los números enteros y los números racionales tienen el mismo cardinal, aunque los racionales parezcan "más numerosos".

- **Criptografía:** Los algoritmos de cifrado simétrico requieren transformaciones biyectivas. Esto asegura que cada texto cifrado provenga de un único mensaje original (inyectividad) y que cualquier texto cifrado pueda descifrarse (sobreyectividad).

- **Bases de datos y sistemas de identificación:** Una clave primaria en una tabla de base de datos define una función inyectiva del conjunto de registros hacia el conjunto de valores de la clave. Esto evita duplicados y permite recuperar un único registro a partir de su identificador.

- **Modelado matemático:** En muchos modelos físicos o económicos, la inyectividad garantiza que dos estados distintos del sistema no produzcan el mismo resultado observable, mientras que la sobreyectividad asegura que todo resultado observable es alcanzable por algún estado del sistema.

### 7.6 Observaciones

> **Observación (dependencia del dominio y del codominio):** Las propiedades de inyectividad, sobreyectividad y biyectividad dependen tanto del dominio como del codominio declarados. La misma regla algebraica puede ser inyectiva en un dominio y no inyectiva en otro, o sobreyectiva respecto a un codominio y no sobreyectiva respecto a otro.

> **Observación (relación con funciones inversas):** Si $f: A \to B$ es biyectiva, entonces existe una única función $f^{-1}: B \to A$ tal que $f^{-1}(f(x)) = x$ para todo $x \in A$ y $f(f^{-1}(y)) = y$ para todo $y \in B$. La demostración formal de esta equivalencia se presenta en la Sección 8.

> **Observación (composición de funciones):** La composición preserva las propiedades de inyectividad y sobreyectividad: la composición de funciones inyectivas es inyectiva, y la composición de funciones sobreyectivas es sobreyectiva. En consecuencia, la composición de funciones biyectivas es biyectiva. Estos resultados se demuestran formalmente en la Sección 9.

---

## 8. Funciones Inversas

Pensemos en las operaciones cotidianas que hacemos y luego deshacemos: abrir y cerrar una puerta, encender y apagar una luz, o escribir y borrar un texto. En matemáticas, muchas funciones también admiten una operación que las revierte: si $f$ transforma $x$ en $y$, entonces su función inversa $f^{-1}$ devuelve $y$ a su valor original $x$. Saber cuándo una función puede invertirse, y cómo calcular esa inversa, es esencial para resolver ecuaciones, cambiar entre sistemas de coordenadas y comprender la simetría de muchas construcciones geométricas.

> **Nota histórica:** La idea de función inversa aparece de manera implícita desde los inicios del cálculo: **Leonhard Euler** ya utilizaba relaciones funcionales inversas para conectar logaritmos con exponenciales, y arcos con trigonométricas. La notación moderna $f^{-1}$ fue sistematizada por el grupo **Nicolas Bourbaki** en el siglo XX, quienes también distinguieron con rigor entre la función inversa $f^{-1}$ y el recíproco algebraico $[f(x)]^{-1} = \frac{1}{f(x)}$.

### 8.1 Existencia y definición de la función inversa

El primer interrogante que debe responderse es cuándo una función admite inversa. La respuesta está íntimamente ligada a la clasificación introducida en la Sección 7.

**Teorema 8.1 (Existencia de la función inversa):**
Una función $f: A \to B$ tiene función inversa si y solo si $f$ es biyectiva.

**Demostración:**
Se demuestran las dos implicaciones.

$(\Rightarrow)$ Supongamos que $f$ tiene una función inversa $g: B \to A$. Entonces $g(f(x)) = x$ para todo $x \in A$ y $f(g(y)) = y$ para todo $y \in B$.

- **Inyectividad:** Sean $x_1, x_2 \in A$ tales que $f(x_1) = f(x_2)$. Aplicando $g$ a ambos lados:
  $$x_1 = g(f(x_1)) = g(f(x_2)) = x_2$$
  Por tanto, $f$ es inyectiva.
- **Sobreyectividad:** Sea $y \in B$. Tomando $x = g(y) \in A$, se tiene:
  $$f(x) = f(g(y)) = y$$
  Por tanto, todo elemento de $B$ tiene preimagen y $f$ es sobreyectiva.

$(\Leftarrow)$ Supongamos ahora que $f$ es biyectiva. Como es sobreyectiva, para cada $y \in B$ existe al menos un $x \in A$ tal que $f(x) = y$. Como es inyectiva, dicho $x$ es único. Definimos entonces $g(y) = x$, donde $x$ es el único elemento de $A$ que satisface $f(x) = y$. Esta función $g$ cumple $g(f(x)) = x$ para todo $x \in A$ y $f(g(y)) = y$ para todo $y \in B$, de modo que $g$ es la inversa de $f$. $\blacksquare$

**Definición 8.1 (Función inversa):**
Sea $f: A \to B$ una función biyectiva. Se define su **función inversa** $f^{-1}: B \to A$ mediante:
$$f^{-1}(y) = x \iff f(x) = y$$

Equivalentemente, la función inversa satisface las dos identidades:
$$(f^{-1} \circ f)(x) = x, \quad \forall x \in A$$
$$(f \circ f^{-1})(y) = y, \quad \forall y \in B$$

> **Advertencia:** La notación $f^{-1}$ para la función inversa no debe confundirse con $[f(x)]^{-1} = \frac{1}{f(x)}$, que denota el recíproco algebraico.

### 8.2 Propiedades algebraicas y gráficas

**Proposición 8.1 (Dominio e imagen de la inversa):**
Si $f: A \to B$ es biyectiva, entonces la función inversa $f^{-1}: B \to A$ satisface:
$$\text{Dom}(f^{-1}) = \text{Im}(f) = B, \qquad \text{Im}(f^{-1}) = \text{Dom}(f) = A$$

**Proposición 8.2 (Inversa de la inversa):**
Si $f: A \to B$ es biyectiva, entonces $(f^{-1})^{-1} = f$.

**Demostración:**
Por definición, $f^{-1}$ va de $B$ a $A$ y revierte la acción de $f$. Aplicar nuevamente la inversa devuelve la función original, es decir, $(f^{-1})^{-1}(x) = f(x)$ para todo $x \in A$. $\blacksquare$

**Proposición 8.3 (Simetría gráfica):**
Las gráficas de $y = f(x)$ y $y = f^{-1}(x)$ son simétricas respecto a la recta identidad $y = x$.

**Demostración:**
Si $(a, b)$ pertenece a la gráfica de $f$, entonces $b = f(a)$, lo cual equivale a $a = f^{-1}(b)$. Por tanto, el punto $(b, a)$ pertenece a la gráfica de $f^{-1}$. La transformación $(a, b) \mapsto (b, a)$ es precisamente la reflexión respecto a la recta $y = x$. $\blacksquare$

PONER GRAFICA AQUI: gráficas de $y = f(x)$, $y = f^{-1}(x)$ y la recta $y = x$ en el mismo sistema de ejes, mostrando la simetría por reflexión respecto a la diagonal.

**Proposición 8.4 (Monotonía):**
Si $f$ es estrictamente creciente y biyectiva, entonces $f^{-1}$ también es estrictamente creciente. Análogamente, si $f$ es estrictamente decreciente y biyectiva, entonces $f^{-1}$ también es estrictamente decreciente.

**Demostración:**
Supongamos que $f$ es estrictamente creciente y sean $y_1 < y_2$ en $B$. Sean $x_1 = f^{-1}(y_1)$ y $x_2 = f^{-1}(y_2)$. Si se tuviera $x_1 \geq x_2$, entonces, por el crecimiento estricto de $f$, se tendría $f(x_1) \geq f(x_2)$, es decir, $y_1 \geq y_2$, lo cual contradice la hipótesis. Por tanto, $x_1 < x_2$ y $f^{-1}$ es estrictamente creciente. El caso decreciente es análogo. $\blacksquare$

### 8.3 Cálculo algebraico de la inversa

Para calcular explícitamente la inversa de una función biyectiva dada por una fórmula, se sigue el siguiente procedimiento:

1. Escribir $y = f(x)$.
2. Despejar $x$ en términos de $y$, obteniendo $x = g(y)$.
3. Definir $f^{-1}(x) = g(x)$, reemplazando la variable $y$ por $x$.
4. Verificar que $(f \circ f^{-1})(x) = x$ y $(f^{-1} \circ f)(x) = x$.

**Ejemplo 8.1 (Función lineal):**
Encontrar la inversa de $f: \mathbb{R} \to \mathbb{R}$ definida por $f(x) = 2x + 3$.

**Solución:**
Escribimos $y = 2x + 3$ y despejamos $x$:
$$\begin{align}
y &= 2x + 3 \\
y - 3 &= 2x \\
x &= \frac{y - 3}{2}
\end{align}$$

Por tanto:
$$f^{-1}(x) = \frac{x - 3}{2}$$

**Verificación:**
$$\begin{align}
(f \circ f^{-1})(x) &= f\left(\frac{x-3}{2}\right) = 2\left(\frac{x-3}{2}\right) + 3 = x \\
(f^{-1} \circ f)(x) &= f^{-1}(2x+3) = \frac{(2x+3)-3}{2} = x
\end{align}$$
Ambas composiciones devuelven la identidad, como debe ser.

**Ejemplo 8.2 (Función racional):**
Encontrar la inversa de $f: \mathbb{R} \setminus \{2\} \to \mathbb{R} \setminus \{3\}$ definida por $f(x) = \dfrac{3x + 1}{x - 2}$.

**Solución:**
Escribimos $y = \dfrac{3x + 1}{x - 2}$ y despejamos $x$:
$$\begin{align}
y(x - 2) &= 3x + 1 \\
yx - 2y &= 3x + 1 \\
yx - 3x &= 2y + 1 \\
x(y - 3) &= 2y + 1 \\
x &= \frac{2y + 1}{y - 3}
\end{align}$$

Por tanto:
$$f^{-1}(x) = \frac{2x + 1}{x - 3}, \qquad \text{con dominio } \mathbb{R} \setminus \{3\}$$

Observemos que $f$ y $f^{-1}$ tienen la misma forma algebraica, salvo los coeficientes numéricos.

**Ejemplo 8.3 (Función exponencial):**
Encontrar la inversa de $f: \mathbb{R} \to (-1, +\infty)$ definida por $f(x) = e^{x+2} - 1$.

**Solución:**
Escribimos $y = e^{x+2} - 1$ y despejamos $x$:
$$\begin{align}
y + 1 &= e^{x+2} \\
\ln(y + 1) &= x + 2 \\
x &= \ln(y + 1) - 2
\end{align}$$

Por tanto:
$$f^{-1}(x) = \ln(x + 1) - 2, \qquad \text{con dominio } (-1, +\infty)$$

El dominio de $f^{-1}$ coincide con la imagen de $f$, pues $e^{x+2} > 0$ implica $f(x) > -1$ para todo $x \in \mathbb{R}$.

**Ejemplo 8.4 (Función cúbica):**
Encontrar la inversa de $f: \mathbb{R} \to \mathbb{R}$ definida por $f(x) = x^3 + 1$.

**Solución:**
Escribimos $y = x^3 + 1$ y despejamos $x$:
$$\begin{align}
y - 1 &= x^3 \\
x &= \sqrt[3]{y - 1}
\end{align}$$

Por tanto:
$$f^{-1}(x) = \sqrt[3]{x - 1}$$

Toda función polinómica de grado impar es biyectiva de $\mathbb{R}$ en $\mathbb{R}$, por lo que admite inversa global.

### 8.4 Restricción del dominio

Si una función no es inyectiva en su dominio natural, no puede tener inversa global. No obstante, es frecuente que al restringir el dominio a un subconjunto donde la función sí sea inyectiva, se obtenga una función biyectiva y, por tanto, invertible.

**Ejemplo 8.5 (Función cuadrática restringida):**
La función $f(x) = x^2$ no es inyectiva en $\mathbb{R}$, pues $f(-2) = f(2) = 4$. Sin embargo, si se restringe a $f: [0, +\infty) \to [0, +\infty)$, la función resulta biyectiva.

**Solución:**
Para $x \geq 0$, escribimos $y = x^2$ y despejamos:
$$x = \sqrt{y}$$
donde se toma la raíz positiva porque $x \geq 0$. Por tanto:
$$f^{-1}(x) = \sqrt{x}, \qquad \text{con dominio } [0, +\infty)$$

> **Observación:** Si se hubiera restringido el dominio a $(-\infty, 0]$, la inversa obtenida sería $f^{-1}(x) = -\sqrt{x}$. Esto muestra que la elección de la restricción afecta directamente la fórmula de la inversa.

**Ejemplo 8.6 (Función cuadrática general):**
Encontrar la inversa de $f(x) = x^2 - 4x + 5$ restringida a $[2, +\infty)$.

**Solución:**
Completamos el cuadrado:
$$f(x) = (x-2)^2 + 1$$

En el intervalo $[2, +\infty)$, la función es estrictamente creciente, por lo que es inyectiva. Su imagen es $[1, +\infty)$. Escribimos $y = (x-2)^2 + 1$ y despejamos:
$$\begin{align}
y - 1 &= (x-2)^2 \\
\sqrt{y - 1} &= x - 2 \\
x &= 2 + \sqrt{y - 1}
\end{align}$$

donde se toma la raíz positiva porque $x \geq 2$. Por tanto:
$$f^{-1}(x) = 2 + \sqrt{x - 1}, \qquad \text{con dominio } [1, +\infty)$$

### 8.5 Aplicaciones

La posibilidad de invertir una función tiene consecuencias prácticas en múltiples áreas.

- **Resolución de ecuaciones:** Calcular la inversa de una función permite despejar variables de manera sistemática. Por ejemplo, resolver $a^x = b$ equivale a aplicar la inversa de la función exponencial, es decir, el logaritmo: $x = \log_a(b)$.

- **Criptografía y desencriptación:** En un esquema de cifrado simétrico, la función de cifrado debe ser biyectiva para que exista una función de descifrado única. La función de descifrado no es otra cosa que la inversa de la función de cifrado.

- **Cambios de coordenadas:** Muchas transformaciones geométricas, como las rotaciones o traslaciones, admiten inversas que permiten regresar al sistema de coordenadas original. Una transformación invertible debe ser, necesariamente, biyectiva.

- **Termodinámica y procesos reversibles:** En física, un proceso reversible puede describirse mediante una función cuya inversa existe, de modo que el sistema puede regresar a su estado inicial sin dejar rastro en el entorno.

- **Instrumentación y calibración:** Un sensor puede modelarse como una función que asigna una magnitud física a una señal eléctrica. Si la función del sensor es biyectiva en el rango de operación, su inversa permite recuperar la magnitud física a partir de la señal medida.

### 8.6 Observaciones

> **Observación (unicidad de la inversa):** Si una función $f: A \to B$ es biyectiva, su inversa es única. En efecto, si $g$ y $h$ fueran dos funciones de $B$ en $A$ que satisfacen $g(f(x)) = x$ y $h(f(x)) = x$ para todo $x \in A$, entonces $g(y) = h(y)$ para todo $y \in B$ porque $f$ es sobreyectiva.

> **Observación (inyectividad es necesaria):** La inyectividad de $f$ garantiza que $f^{-1}$ esté bien definida como función. Si $f$ no fuera inyectiva, un mismo valor $y$ tendría dos preimágenes distintas, y $f^{-1}(y)$ no podría asignar un único valor.

> **Observación (sobreyectividad es necesaria):** La sobreyectividad de $f$ garantiza que $f^{-1}$ esté definida en todo el codominio $B$. Si $f$ no fuera sobreyectiva, existirían valores $y \in B$ sin preimagen, para los cuales $f^{-1}(y)$ no tendría sentido.

---

## 9. Composición de Funciones

Muchos procesos matemáticos y del mundo real se describen mejor como una sucesión de etapas: una primera transformación convierte la entrada en una cantidad intermedia, y una segunda transformación actúa sobre esa cantidad para producir el resultado final. Por ejemplo, en física la posición de un objeto puede depender del tiempo a través de una primera función, y la energía cinética puede depender de la posición a través de una segunda; la energía resulta entonces función del tiempo al componer ambas correspondencias.

La **composición de funciones** formaliza esta idea: dadas dos funciones $g$ y $f$ con dominios y codominios compatibles, se define una nueva función $(f \circ g)(x) = f(g(x))$ que aplica primero $g$ y luego $f$. Esta operación es tan natural como la suma o el producto de funciones, pero tiene propiedades distintivas —en particular, no es conmutativa— que conviene estudiar con cuidado.

**Ejemplo 9.1:**
Si $g(x) = x + 1$ y $f(x) = x^2$, entonces:
$$(f \circ g)(3) = f(g(3)) = f(4) = 4^2 = 16$$
Es decir, la composición transforma $3$ en $16$ al sumar primero $1$ y luego elevar al cuadrado.

### 9.1 Definición y dominio

**Definición 9.1 (Composición de funciones):**
Dadas dos funciones $f: B \to C$ y $g: A \to B$, la **composición** de $f$ con $g$, denotada $f \circ g$ (se lee "$f$ compuesta con $g$" o "$f$ círculo $g$"), es la función definida por:
$$(f \circ g)(x) = f(g(x))$$

> **Nota:** La notación $f \circ g$ se lee de **derecha a izquierda**: primero aplicamos $g$, luego aplicamos $f$ al resultado.

**Definición 9.2 (Dominio de la composición):**
El dominio de $f \circ g$ es:
$$\text{Dom}(f \circ g) = \{x \in \text{Dom}(g) : g(x) \in \text{Dom}(f)\}$$

Es decir, debemos satisfacer **dos condiciones**:
1. $x$ debe estar en el dominio de $g$
2. El resultado $g(x)$ debe estar en el dominio de $f$

> **Observación importante:** Para que $f \circ g$ esté bien definida, necesitamos que $\text{Im}(g) \cap \text{Dom}(f) \neq \emptyset$ (la imagen de $g$ debe tener intersección con el dominio de $f$).

**Ejemplo 9.2:**
Sean $f(x) = \sqrt{x}$ y $g(x) = x - 3$. Calcular $(f \circ g)(x)$ y su dominio.

**Solución:**
$$(f \circ g)(x) = f(g(x)) = f(x-3) = \sqrt{x-3}$$

**Dominio:**
- $\text{Dom}(g) = \mathbb{R}$
- $\text{Dom}(f) = [0, +\infty)$
- Necesitamos que $g(x) \in \text{Dom}(f)$, es decir, $x - 3 \geq 0$
- Por lo tanto: $x \geq 3$

$$\text{Dom}(f \circ g) = [3, +\infty)$$

**Ejemplo 9.3:**
Sean $f(x) = x^2$ y $g(x) = x + 1$. Calcular:
a) $(f \circ g)(x)$
b) $(g \circ f)(x)$

**Solución:**
a) $(f \circ g)(x) = f(g(x)) = f(x+1) = (x+1)^2 = x^2 + 2x + 1$

b) $(g \circ f)(x) = g(f(x)) = g(x^2) = x^2 + 1$

> **Observación crucial:** En este ejemplo, $(f \circ g)(x) \neq (g \circ f)(x)$. Esto ilustra que la composición **no es conmutativa** en general.

**Ejemplo 9.4:**
Sean $f(x) = \frac{1}{x}$ y $g(x) = x^2 - 4$. Determinar el dominio de $(f \circ g)(x)$.

**Solución:**
$$(f \circ g)(x) = f(g(x)) = f(x^2 - 4) = \frac{1}{x^2 - 4}$$

**Dominio:**
- $\text{Dom}(g) = \mathbb{R}$
- $\text{Dom}(f) = \mathbb{R} \setminus \{0\}$
- Necesitamos $g(x) \neq 0$, es decir, $x^2 - 4 \neq 0$
- $x^2 \neq 4 \Rightarrow x \neq \pm 2$

$$\text{Dom}(f \circ g) = \mathbb{R} \setminus \{-2, 2\}$$

**Ejemplo 9.5 (Composición con dominios restringidos):**
Sean $f(x) = \sqrt{x}$ y $g(x) = \ln(x)$. Determinar el dominio de $(f \circ g)(x)$.

**Solución:**
$$(f \circ g)(x) = f(g(x)) = f(\ln(x)) = \sqrt{\ln(x)}$$

**Dominio:**
- $\text{Dom}(g) = (0, +\infty)$ (logaritmo requiere $x > 0$)
- $\text{Dom}(f) = [0, +\infty)$ (raíz cuadrada requiere argumento $\geq 0$)
- Necesitamos $\ln(x) \geq 0$, es decir, $x \geq 1$

$$\text{Dom}(f \circ g) = [1, +\infty)$$

### 9.2 Propiedades de la composición

**Proposición 9.1 (No conmutatividad):**
En general, $f \circ g \neq g \circ f$. Es decir, la composición de funciones **no es conmutativa**.

**Ejemplo 9.6:**
Si $f(x) = 2x$ y $g(x) = x + 3$:
- $(f \circ g)(x) = 2(x+3) = 2x + 6$
- $(g \circ f)(x) = 2x + 3$

Como $6 \neq 3$, se tiene $2x + 6 \neq 2x + 3$ para todo $x \in \mathbb{R}$.

**Proposición 9.2 (Asociatividad):**
La composición de funciones **es asociativa**. Si $f$, $g$ y $h$ son funciones tales que las composiciones están definidas, entonces:
$$f \circ (g \circ h) = (f \circ g) \circ h$$

**Demostración:**
Para cualquier $x$ en el dominio apropiado:
$$[f \circ (g \circ h)](x) = f[(g \circ h)(x)] = f[g(h(x))]$$
$$[(f \circ g) \circ h](x) = (f \circ g)[h(x)] = f[g(h(x))]$$

Ambas expresiones son iguales. $\blacksquare$

**Proposición 9.3 (Elemento identidad):**
La función identidad $\text{id}(x) = x$ actúa como **elemento neutro** para la composición:
$$f \circ \text{id} = \text{id} \circ f = f$$

para cualquier función $f$.

**Demostración:**
$$(f \circ \text{id})(x) = f(\text{id}(x)) = f(x)$$
$$(\text{id} \circ f)(x) = \text{id}(f(x)) = f(x)$$

Por lo tanto, ambas composiciones dan $f$. $\blacksquare$

**Proposición 9.4 (Composición con función inversa):**
Si $f: A \to B$ es biyectiva con inversa $f^{-1}: B \to A$, entonces:
$$f^{-1} \circ f = \text{id}_A \quad \text{y} \quad f \circ f^{-1} = \text{id}_B$$

Donde $\text{id}_A$ es la función identidad en $A$ y $\text{id}_B$ es la función identidad en $B$.

**Ejemplo 9.7:**
Si $f(x) = 2x + 3$, entonces $f^{-1}(x) = \frac{x-3}{2}$. Verificamos:
$$(f^{-1} \circ f)(x) = f^{-1}(2x+3) = \frac{(2x+3)-3}{2} = \frac{2x}{2} = x = \text{id}(x)$$
$$(f \circ f^{-1})(x) = f\left(\frac{x-3}{2}\right) = 2\left(\frac{x-3}{2}\right) + 3 = x - 3 + 3 = x = \text{id}(x)$$

### 9.3 Composición y clasificación de funciones

**Teorema 9.1 (Composición de funciones inyectivas):**
Si $f: B \to C$ y $g: A \to B$ son ambas inyectivas, entonces $f \circ g: A \to C$ es inyectiva.

**Demostración:**
Sean $x_1, x_2 \in A$ tales que $(f \circ g)(x_1) = (f \circ g)(x_2)$.

Entonces:
$$f(g(x_1)) = f(g(x_2))$$

Como $f$ es inyectiva:
$$g(x_1) = g(x_2)$$

Como $g$ es inyectiva:
$$x_1 = x_2$$

Por lo tanto, $f \circ g$ es inyectiva. $\blacksquare$

**Teorema 9.2 (Composición de funciones sobreyectivas):**
Si $f: B \to C$ y $g: A \to B$ son ambas sobreyectivas, entonces $f \circ g: A \to C$ es sobreyectiva.

**Demostración:**
Sea $z \in C$ arbitrario. Como $f$ es sobreyectiva, existe $y \in B$ tal que $f(y) = z$.

Como $g$ es sobreyectiva, existe $x \in A$ tal que $g(x) = y$.

Entonces:
$$(f \circ g)(x) = f(g(x)) = f(y) = z$$

Por lo tanto, para todo $z \in C$ existe $x \in A$ tal que $(f \circ g)(x) = z$, lo que demuestra que $f \circ g$ es sobreyectiva. $\blacksquare$

**Corolario 9.1 (Composición de funciones biyectivas):**
Si $f: B \to C$ y $g: A \to B$ son ambas biyectivas, entonces $f \circ g: A \to C$ es biyectiva.

Además, la inversa de la composición satisface:
$$(f \circ g)^{-1} = g^{-1} \circ f^{-1}$$

> **Observación:** La fórmula $(f \circ g)^{-1} = g^{-1} \circ f^{-1}$ refleja el hecho de que, al deshacer una sucesión de operaciones, se debe revertir el orden en que fueron aplicadas.

**Ejemplo 9.8:**
Sean $f(x) = e^x$ y $g(x) = x + 1$. Ambas son biyectivas de $\mathbb{R}$ en sus respectivas imágenes. La composición:
$$(f \circ g)(x) = e^{x+1}$$

es también biyectiva, y su inversa es:
$$(f \circ g)^{-1}(x) = (g^{-1} \circ f^{-1})(x) = g^{-1}(\ln(x)) = \ln(x) - 1$$

### 9.4 Descomposición de funciones

Muchas funciones complejas pueden expresarse como composición de funciones más simples. Esta técnica es fundamental en cálculo (regla de la cadena para derivadas).

**Ejemplo 9.9 (Identificar composición):**
Dada $h(x) = \sqrt{x^2 + 1}$, expresarla como $h = f \circ g$.

**Solución:**
- Sea $g(x) = x^2 + 1$ (función interior)
- Sea $f(x) = \sqrt{x}$ (función exterior)
- Entonces: $h(x) = f(g(x)) = \sqrt{x^2 + 1}$

**Ejemplo 9.10:**
Expresemos $h(x) = \frac{1}{(x+2)^2}$ como composición de tres funciones.

**Solución:**
- Sea $r(x) = x + 2$
- Sea $s(x) = x^2$
- Sea $t(x) = \frac{1}{x}$
- Entonces: $h = t \circ s \circ r$

**Verificación:**
$$(t \circ s \circ r)(x) = t(s(r(x))) = t(s(x+2)) = t((x+2)^2) = \frac{1}{(x+2)^2}$$

**Ejemplo 9.11 (Composición iterada):**
Si $f(x) = 2x$, entonces:
- $(f \circ f)(x) = f(f(x)) = f(2x) = 2(2x) = 4x = 2^2 x$
- $(f \circ f \circ f)(x) = f(f(f(x))) = 8x = 2^3 x$
- En general: $f^{(n)}(x) = 2^n x$ (composición $n$ veces)

> **Nota:** La notación $f^{(n)}$ representa la composición iterada $\underbrace{f \circ f \circ \cdots \circ f}_{n \text{ veces}}$.

### 9.5 Aplicaciones

La composición de funciones aparece de manera recurrente tanto en matemáticas puras como en modelado aplicado.

- **Cálculo diferencial:** La regla de la cadena para derivadas no es más que la derivada de una composición. Si $h = f \circ g$, entonces $h'(x) = f'(g(x)) \cdot g'(x)$. Reconocer la estructura $f(g(x))$ es el primer paso para derivar funciones complejas.

- **Física:** Muchas magnitudes se obtienen por composición de relaciones. Por ejemplo, la presión atmosférica depende de la altitud, y la altitud puede depender del tiempo en un ascenso; la presión resulta entonces función del tiempo al componer ambas correspondencias.

- **Ciencias de la computación:** Los programas funcionales construyen procesos complejos componiendo funciones simples en secuencia. Un pipeline de datos no es más que una composición $f_n \circ \cdots \circ f_2 \circ f_1$, donde cada etapa transforma la salida de la anterior.

- **Criptografía:** Algunos sistemas cifrados combinan permutaciones y sustituciones mediante composición. La seguridad depende en parte de que la composición resultante sea difícil de invertir sin conocer las funciones individuales.

### 9.6 Observaciones

> **Observación (no conmutatividad):** La composición de funciones raramente conmuta. Incluso cuando $f \circ g$ y $g \circ f$ están ambas definidas, en general representan transformaciones distintas. La no conmutatividad es una de las diferencias más importantes entre la composición y las operaciones aritméticas usuales con funciones.

> **Observación (composición iterada):** Cuando una función se compone consigo misma repetidamente, surgen comportamientos de gran interés en dinámica de sistemas, teoría de fractales y análisis numérico. Estudiar la iteración $f^{(n)}$ permite analizar estabilidad, puntos fijos y convergencia de métodos iterativos.

---
## 10. Inversas de Funciones Trascendentes

Resolver una ecuación trigonométrica como $\sin(\theta) = \frac{1}{2}$ presenta una dificultad inmediata: sin restricciones adicionales, existen infinitos ángulos que satisfacen la igualdad porque el seno es periódico. Para poder despejar $\theta$ de manera unívoca es necesario restringir el dominio de la función trigonométrica a un intervalo donde sea inyectiva. Esta idea conduce a las funciones trigonométricas inversas, que son indispensables en física, ingeniería y cálculo integral. De manera análoga, las funciones hiperbólicas inversas surgen al despejar el argumento en las definiciones exponenciales de $\sinh$, $\cosh$ y $\tanh$.

> **Nota histórica:** Las notaciones $\arcsin$, $\arccos$ y $\arctan$ se consolidaron en el siglo XVIII, en gran medida gracias al trabajo de **Leonhard Euler**, quien sistematizó el uso de funciones y sus inversas. El prefijo "arco" proviene de la interpretación geométrica: si $\theta = \arcsin(x)$, entonces $\theta$ es la medida de un arco cuyo seno vale $x$. Las funciones hiperbólicas inversas, en cambio, se expresan naturalmente mediante logaritmos, lo que las convierte en herramientas frecuentes en integración y ecuaciones diferenciales.

### 10.1 Funciones trigonométricas inversas

**Definición 10.1 (Arco seno):**
La función **arcoseno** $\arcsin: [-1, 1] \to \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$ es la inversa de la función $\sin: \left[-\frac{\pi}{2}, \frac{\pi}{2}\right] \to [-1, 1]$. Se define mediante:
$$y = \arcsin(x) \iff \sin(y) = x, \quad y \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$$

**Definición 10.2 (Arco coseno):**
La función **arcocoseno** $\arccos: [-1, 1] \to [0, \pi]$ es la inversa de la función $\cos: [0, \pi] \to [-1, 1]$. Se define mediante:
$$y = \arccos(x) \iff \cos(y) = x, \quad y \in [0, \pi]$$

**Definición 10.3 (Arco tangente):**
La función **arcotangente** $\arctan: \mathbb{R} \to \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ es la inversa de la función $\tan: \left(-\frac{\pi}{2}, \frac{\pi}{2}\right) \to \mathbb{R}$. Se define mediante:
$$y = \arctan(x) \iff \tan(y) = x, \quad y \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$$

**Proposición 10.1 (Propiedades de las funciones trigonométricas inversas):**
Para todo $x$ en el dominio correspondiente se verifican las siguientes propiedades:

1. $\arcsin(-x) = -\arcsin(x)$ (función impar).
2. $\arccos(-x) = \pi - \arccos(x)$.
3. $\arctan(-x) = -\arctan(x)$ (función impar).
4. $\arcsin(x) + \arccos(x) = \dfrac{\pi}{2}$.

**Demostración:**
La primera propiedad se sigue de que $\sin$ es impar en $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$:
$$\sin(-\arcsin(x)) = -\sin(\arcsin(x)) = -x$$
Por lo tanto $-\arcsin(x)$ es el único ángulo en $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$ cuyo seno es $-x$, es decir, $\arcsin(-x) = -\arcsin(x)$.

La cuarta propiedad se obtiene observando que si $\alpha = \arcsin(x)$, entonces $\sin(\alpha) = x$ y $\alpha \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$. Como $\cos\left(\frac{\pi}{2} - \alpha\right) = \sin(\alpha) = x$ y $\frac{\pi}{2} - \alpha \in [0, \pi]$, se tiene:
$$\arccos(x) = \frac{\pi}{2} - \alpha = \frac{\pi}{2} - \arcsin(x)$$
De donde $\arcsin(x) + \arccos(x) = \frac{\pi}{2}$. $\blacksquare$

**Ejemplo 10.1:**
Calcular los siguientes valores:
- $\arcsin\left(\frac{1}{2}\right) = \frac{\pi}{6}$, pues $\sin\left(\frac{\pi}{6}\right) = \frac{1}{2}$ y $\frac{\pi}{6} \in \left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$.
- $\arccos\left(-\frac{1}{2}\right) = \frac{2\pi}{3}$, pues $\cos\left(\frac{2\pi}{3}\right) = -\frac{1}{2}$ y $\frac{2\pi}{3} \in [0, \pi]$.
- $\arctan(1) = \frac{\pi}{4}$, pues $\tan\left(\frac{\pi}{4}\right) = 1$ y $\frac{\pi}{4} \in \left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$.

### 10.2 Funciones hiperbólicas inversas

**Proposición 10.2 (Fórmulas logarítmicas):**
Las funciones hiperbólicas inversas admiten las siguientes expresiones mediante logaritmos naturales:

1. $\operatorname{argsinh}(x) = \ln\left(x + \sqrt{x^2 + 1}\right), \quad x \in \mathbb{R}$.
2. $\operatorname{argcosh}(x) = \ln\left(x + \sqrt{x^2 - 1}\right), \quad x \geq 1$.
3. $\operatorname{argtanh}(x) = \dfrac{1}{2}\ln\left(\dfrac{1 + x}{1 - x}\right), \quad |x| < 1$.

**Demostración (de la fórmula para argsinh):**
Sea $y = \operatorname{argsinh}(x)$. Entonces $x = \sinh(y) = \dfrac{e^y - e^{-y}}{2}$. Multiplicando por $2e^y$:
$$2x e^y = e^{2y} - 1$$
Reordenando se obtiene una ecuación cuadrática en $e^y$:
$$e^{2y} - 2x e^y - 1 = 0$$
Resolviendo:
$$e^y = \frac{2x \pm \sqrt{4x^2 + 4}}{2} = x \pm \sqrt{x^2 + 1}$$
Como $e^y > 0$ para todo $y \in \mathbb{R}$, debemos elegir el signo positivo:
$$e^y = x + \sqrt{x^2 + 1}$$
Aplicando logaritmo natural:
$$y = \ln\left(x + \sqrt{x^2 + 1}\right)$$
Por lo tanto $\operatorname{argsinh}(x) = \ln\left(x + \sqrt{x^2 + 1}\right)$. $\blacksquare$

**Ejemplo 10.2:**
- $\operatorname{argsinh}(0) = \ln(0 + 1) = 0$, que coincide con $\sinh(0) = 0$.
- $\operatorname{argcosh}(1) = \ln(1 + 0) = 0$, que coincide con $\cosh(0) = 1$.
- $\operatorname{argtanh}(0) = \frac{1}{2}\ln(1) = 0$, que coincide con $\tanh(0) = 0$.

### 10.3 Aplicaciones

Las funciones trigonométricas inversas aparecen cada vez que se conoce una razón trigonométrica y se desea recuperar el ángulo asociado. En navegación y astronomía permiten calcular ángulos de elevación, acimut o fases orbitales a partir de medidas observables. En cálculo integral, son esenciales para evaluar integrales de la forma $\int \frac{dx}{\sqrt{1 - x^2}}$ o $\int \frac{dx}{1 + x^2}$.

Las funciones hiperbólicas inversas aparecen con frecuencia en problemas de física y geometría. La función $\operatorname{argcosh}$ describe, por ejemplo, la forma de la catenaria invertida y aparece en la distancia hiperbólica del semiplano superior. La función $\operatorname{argsinh}$ surge al integrar expresiones como $\frac{1}{\sqrt{1 + x^2}}$ y en la parametrización de ciertas trayectorias relativistas.

### 10.4 Observaciones

> **Observación (notación):** En distintos textos se encuentran las notaciones $\sin^{-1}(x)$, $\cos^{-1}(x)$, $\tan^{-1}(x)$ como sinónimos de $\arcsin(x)$, $\arccos(x)$, $\arctan(x)$. Es importante no confundir $\sin^{-1}(x)$ con $\frac{1}{\sin(x)}$; la primera denota la función inversa, mientras que la segunda es el recíproco. Para evitar ambigüedades, en este curso preferimos la notación "arco".

> **Observación (dominio y rango):** El dominio y el rango de las funciones trigonométricas inversas están determinados por la restricción que hace a la función original inyectiva. Cambiar el intervalo de restricción cambiaría la función inversa obtenida, por lo que las elecciones $\left[-\frac{\pi}{2}, \frac{\pi}{2}\right]$ para el seno, $[0, \pi]$ para el coseno y $\left(-\frac{\pi}{2}, \frac{\pi}{2}\right)$ para la tangente son convenciones estándar que conviene recordar.

---
## 11. Cónicas y Funciones

Las secciones cónicas son curvas que aparecen constantemente en modelos físicos e ingenieriles: órbitas planetarias, reflectores, antenas y sistemas de navegación. Sin embargo, desde el punto de vista funcional presentan una dificultad inmediata: la mayoría no son funciones $y = f(x)$ en su totalidad. El círculo, la elipse y la hipérbola horizontal asignan dos valores de $y$ a un mismo $x$, por lo que es necesario dividirlas en ramas. Esta sección no repite la teoría de cónicas, que se desarrolla con todo rigor en [[Clase 8 - Cónicas]], sino que se concentra en cómo extraer funciones de ellas paso a paso.

### 11.1 Estrategia general

Para obtener funciones $y = f(x)$ a partir de una ecuación implícita de una cónica se sigue un procedimiento sistemático:

1. **Aislar el término en $y$**: mover todos los términos que contengan $y$ a un lado de la ecuación y el resto al otro.
2. **Despejar $y$**: aplicar raíces, divisiones u otras operaciones para obtener una expresión de la forma $y = \dots$.
3. **Interpretar el signo $\pm$**: si aparece una raíz cuadrada, la ecuación original contiene simultáneamente los dos signos. Cada signo determina una **rama** de la cónica.
4. **Determinar el dominio**: la expresión bajo la raíz (o cualquier otra restricción) debe ser no negativa. El conjunto de $x$ que cumple esta condición es el dominio de cada rama.

A continuación se aplica este procedimiento a cada cónica básica. Al final se presenta una tabla resumen.

### 11.2 El círculo

Partimos de la ecuación de un círculo centrado en el origen con radio $r > 0$:
$$x^2 + y^2 = r^2$$

**Paso 1: aislar $y^2$.**
Restamos $x^2$ en ambos lados:
$$y^2 = r^2 - x^2$$

**Paso 2: despejar $y$.**
Tomamos raíz cuadrada en ambos lados. Recuerde que $\sqrt{y^2} = |y|$, por lo que debemos considerar ambos signos:
$$|y| = \sqrt{r^2 - x^2}$$
$$y = \pm\sqrt{r^2 - x^2}$$

**Paso 3: identificar las ramas.**
El signo $+$ corresponde a la rama superior del círculo y el signo $-$ a la rama inferior:
$$\begin{align}
f_1(x) &= \sqrt{r^2 - x^2} \\
f_2(x) &= -\sqrt{r^2 - x^2}
\end{align}$$

**Paso 4: determinar el dominio.**
La expresión dentro de la raíz debe satisfacer:
$$r^2 - x^2 \geq 0 \quad \Longleftrightarrow \quad x^2 \leq r^2 \quad \Longleftrightarrow \quad -r \leq x \leq r$$

Por tanto, el dominio de ambas ramas es:
$$\text{Dom}(f_1) = \text{Dom}(f_2) = [-r, r]$$

**Ejemplo 11.1:**
Para el círculo $x^2 + y^2 = 9$, con $r = 3$, se obtiene:
$$\begin{align}
y^2 &= 9 - x^2 \\
y &= \pm\sqrt{9 - x^2}
\end{align}$$

Las dos ramas son:
$$f_1(x) = \sqrt{9 - x^2}, \qquad f_2(x) = -\sqrt{9 - x^2}$$
con dominio común $[-3, 3]$.

### 11.3 La elipse

La elipse centrada en el origen con semiejes $a > 0$ y $b > 0$ tiene ecuación:
$$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$$

**Paso 1: aislar el término en $y$.**
$$\frac{y^2}{b^2} = 1 - \frac{x^2}{a^2}$$

**Paso 2: despejar $y^2$ y luego $y$.**
Multiplicamos por $b^2$:
$$y^2 = b^2\left(1 - \frac{x^2}{a^2}\right) = \frac{b^2}{a^2}(a^2 - x^2)$$

Tomamos raíz cuadrada:
$$y = \pm\frac{b}{a}\sqrt{a^2 - x^2}$$

**Paso 3: identificar las ramas.**
$$\begin{align}
f_1(x) &= \frac{b}{a}\sqrt{a^2 - x^2} \quad \text{(rama superior)} \\
f_2(x) &= -\frac{b}{a}\sqrt{a^2 - x^2} \quad \text{(rama inferior)}
\end{align}$$

**Paso 4: determinar el dominio.**
Se requiere:
$$a^2 - x^2 \geq 0 \quad \Longleftrightarrow \quad -a \leq x \leq a$$

Por tanto:
$$\text{Dom}(f_1) = \text{Dom}(f_2) = [-a, a]$$

**Ejemplo 11.2:**
Para la elipse $\frac{x^2}{16} + \frac{y^2}{9} = 1$, con $a = 4$ y $b = 3$, se obtiene:
$$\begin{align}
\frac{y^2}{9} &= 1 - \frac{x^2}{16} \\
y^2 &= 9\left(1 - \frac{x^2}{16}\right) = \frac{9}{16}(16 - x^2) \\
y &= \pm\frac{3}{4}\sqrt{16 - x^2}
\end{align}$$

Las ramas son:
$$f_1(x) = \frac{3}{4}\sqrt{16 - x^2}, \qquad f_2(x) = -\frac{3}{4}\sqrt{16 - x^2}$$
con dominio $[-4, 4]$.

### 11.4 La parábola

La parábola presenta dos casos según la orientación de su eje.

#### 11.4.1 Parábola de eje vertical

Su ecuación canónica es:
$$y = a(x - h)^2 + k$$

En este caso $y$ ya aparece despejada, por lo que la ecuación **sí define directamente** una función:
$$f(x) = a(x - h)^2 + k$$
con dominio $\mathbb{R}$. Si el vértice está en el origen, esto se reduce a $f(x) = ax^2$.

#### 11.4.2 Parábola de eje horizontal

Su ecuación canónica es:
$$x = a(y - k)^2 + h$$

Aquí $x$ está en función de $y$, no al revés. Para expresar $y$ en términos de $x$ se procede así.

**Paso 1: aislar $(y - k)^2$.**
$$a(y - k)^2 = x - h$$
$$ (y - k)^2 = \frac{x - h}{a}$$

**Paso 2: tomar raíz cuadrada.**
$$y - k = \pm\sqrt{\frac{x - h}{a}}$$

**Paso 3: despejar $y$ e identificar ramas.**
$$\begin{align}
f_1(x) &= k + \sqrt{\frac{x - h}{a}} \quad \text{(rama superior)} \\
f_2(x) &= k - \sqrt{\frac{x - h}{a}} \quad \text{(rama inferior)}
\end{align}$$

**Paso 4: determinar el dominio.**
La fracción dentro de la raíz debe ser no negativa. Si $a > 0$, entonces $x - h \geq 0$, es decir, $x \geq h$. Si $a < 0$, entonces $x - h \leq 0$, es decir, $x \leq h$.

**Ejemplo 11.3:**
Para la parábola $x = y^2$, con $h = k = 0$ y $a = 1$, se obtiene:
$$\begin{align}
y^2 &= x \\
y &= \pm\sqrt{x}
\end{align}$$

Las ramas son $f_1(x) = \sqrt{x}$ y $f_2(x) = -\sqrt{x}$, ambas con dominio $[0, +\infty)$.

### 11.5 La hipérbola

#### 11.5.1 Hipérbola horizontal

Su ecuación canónica centrada en el origen es:
$$\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$$

**Paso 1: aislar el término en $y$.**
$$\frac{y^2}{b^2} = \frac{x^2}{a^2} - 1$$

**Paso 2: despejar $y^2$ y luego $y$.**
Multiplicamos por $b^2$:
$$y^2 = b^2\left(\frac{x^2}{a^2} - 1\right) = \frac{b^2}{a^2}(x^2 - a^2)$$

Tomamos raíz cuadrada:
$$y = \pm\frac{b}{a}\sqrt{x^2 - a^2}$$

**Paso 3: identificar las ramas.**
$$\begin{align}
f_1(x) &= \frac{b}{a}\sqrt{x^2 - a^2} \quad \text{(rama superior)} \\
f_2(x) &= -\frac{b}{a}\sqrt{x^2 - a^2} \quad \text{(rama inferior)}
\end{align}$$

**Paso 4: determinar el dominio.**
Se requiere:
$$x^2 - a^2 \geq 0 \quad \Longleftrightarrow \quad x \leq -a \quad \text{o} \quad x \geq a$$

Por tanto:
$$\text{Dom}(f_1) = \text{Dom}(f_2) = (-\infty, -a] \cup [a, +\infty)$$

**Ejemplo 11.4:**
Para la hipérbola $x^2 - y^2 = 1$, con $a = b = 1$, se obtiene:
$$\begin{align}
y^2 &= x^2 - 1 \\
y &= \pm\sqrt{x^2 - 1}
\end{align}$$

Las ramas son $f_1(x) = \sqrt{x^2 - 1}$ y $f_2(x) = -\sqrt{x^2 - 1}$, con dominio $(-\infty, -1] \cup [1, +\infty)$.

#### 11.5.2 Hipérbola vertical

Su ecuación canónica centrada en el origen es:
$$\frac{y^2}{b^2} - \frac{x^2}{a^2} = 1$$

Procediendo de manera análoga se obtiene:
$$y = \pm\frac{b}{a}\sqrt{x^2 + a^2}$$

En este caso $x^2 + a^2$ es siempre positivo, por lo que ambas ramas están definidas para todo $x \in \mathbb{R}$:
$$\begin{align}
f_1(x) &= \frac{b}{a}\sqrt{x^2 + a^2} \\
f_2(x) &= -\frac{b}{a}\sqrt{x^2 + a^2}
\end{align}$$
con dominio $\mathbb{R}$.

### 11.6 Tabla resumen

La siguiente tabla condensa el resultado del proceso anterior para cónicas centradas en el origen.

| Cónica | Ecuación implícita | Ramas funcionales | Dominio |
|---|---|---|---|
| Círculo | $x^2 + y^2 = r^2$ | $f_1(x) = \sqrt{r^2 - x^2}$, $f_2(x) = -\sqrt{r^2 - x^2}$ | $[-r, r]$ |
| Elipse | $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ | $f_1(x) = \frac{b}{a}\sqrt{a^2 - x^2}$, $f_2(x) = -\frac{b}{a}\sqrt{a^2 - x^2}$ | $[-a, a]$ |
| Parábola vertical | $y = ax^2$ | $f(x) = ax^2$ | $\mathbb{R}$ |
| Parábola horizontal | $x = ay^2$ | $f_1(x) = \sqrt{x/a}$, $f_2(x) = -\sqrt{x/a}$ | $[0, +\infty)$ si $a > 0$; $(-\infty, 0]$ si $a < 0$ |
| Hipérbola horizontal | $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$ | $f_1(x) = \frac{b}{a}\sqrt{x^2 - a^2}$, $f_2(x) = -\frac{b}{a}\sqrt{x^2 - a^2}$ | $(-\infty, -a] \cup [a, +\infty)$ |
| Hipérbola vertical | $\frac{y^2}{b^2} - \frac{x^2}{a^2} = 1$ | $f_1(x) = \frac{b}{a}\sqrt{x^2 + a^2}$, $f_2(x) = -\frac{b}{a}\sqrt{x^2 + a^2}$ | $\mathbb{R}$ |

### 11.7 Cónicas trasladadas

Cuando el centro de la cónica no está en el origen, el procedimiento es el mismo; solo aparecen desplazamientos $h$ y $k$ en las fórmulas. Veamos el caso del círculo.

Partimos de:
$$(x - h)^2 + (y - k)^2 = r^2$$

**Paso 1: aislar $(y - k)^2$.**
$$(y - k)^2 = r^2 - (x - h)^2$$

**Paso 2: tomar raíz cuadrada.**
$$y - k = \pm\sqrt{r^2 - (x - h)^2}$$

**Paso 3: despejar $y$ e identificar ramas.**
$$\begin{align}
f_1(x) &= k + \sqrt{r^2 - (x - h)^2} \quad \text{(rama superior)} \\
f_2(x) &= k - \sqrt{r^2 - (x - h)^2} \quad \text{(rama inferior)}
\end{align}$$

**Paso 4: determinar el dominio.**
Se requiere:
$$r^2 - (x - h)^2 \geq 0 \quad \Longleftrightarrow \quad (x - h)^2 \leq r^2 \quad \Longleftrightarrow \quad h - r \leq x \leq h + r$$

Por tanto:
$$\text{Dom}(f_1) = \text{Dom}(f_2) = [h - r, h + r]$$

**Ejemplo 11.5:**
Para el círculo $(x - 2)^2 + (y + 1)^2 = 25$, con centro $(h, k) = (2, -1)$ y radio $r = 5$, se obtiene:
$$\begin{align}
(y + 1)^2 &= 25 - (x - 2)^2 \\
y + 1 &= \pm\sqrt{25 - (x - 2)^2} \\
y &= -1 \pm \sqrt{25 - (x - 2)^2}
\end{align}$$

Las ramas son:
$$f_1(x) = -1 + \sqrt{25 - (x - 2)^2}, \qquad f_2(x) = -1 - \sqrt{25 - (x - 2)^2}$$
con dominio $[-3, 7]$.

> **Nota:** Para el resto de las cónicas trasladadas (elipse, parábola e hipérbola) el procedimiento es análogo: se aisla el término con $y$, se despeja y se ajusta el dominio según el nuevo centro $(h, k)$.

### 11.8 Aplicaciones

La necesidad de expresar una cónica como función surge cada vez que se desea estudiar pendientes, áreas o movimiento a lo largo de una de sus ramas.

- **Mecánica celeste:** Una órbita elíptica se describe globalmente por la ecuación implícita de la elipse, pero el movimiento de un planeta se estudia mediante una parametrización o una rama funcional que depende del tiempo.

- **Óptica y telecomunicaciones:** Un reflector parabólico se modela con $y = ax^2$, que ya es una función. En cambio, un espejo elíptico requiere elegir la rama superior o inferior según la región iluminada.

- **Navegación:** Los sistemas de posicionamiento por diferencia de tiempos usan hipérbolas. Para convertir los datos en una trayectoria estimada se trabaja con ramas funcionales y parametrizaciones.

### 11.9 Observaciones

> **Observación (cónicas y funciones):** Ninguna cónica cerrada o con dos ramas define una función $y = f(x)$ de manera global. El círculo, la elipse y la hipérbola horizontal deben dividirse en rama superior e inferior. La parábola de eje vertical sí es función, mientras que la de eje horizontal define $x$ como función de $y$.

> **Observación (referencia):** Para la clasificación completa, propiedades geométricas, focos, directrices, excentricidad y cónicas rotadas, consultar [[Clase 8 - Cónicas]].

---

## 12. Funciones Implícitas

Hasta ahora hemos trabajado con funciones dadas de forma **explícita**, es decir, con ecuaciones en las que $y$ ya aparece despejada en términos de $x$, como $y = x^2 + 1$ o $y = \sqrt{x}$. Sin embargo, muchas relaciones matemáticas naturales se presentan de forma **implícita**, donde $x$ e $y$ aparecen mezclados en una misma ecuación. La ecuación de un círculo $x^2 + y^2 = 25$, la de una elipse o incluso curvas más elaboradas como el folium de Descartes son ejemplos de este tipo de relaciones.

En una ecuación implícita no siempre es necesario ni posible despejar $y$. Cuando sí se puede, el resultado suele ser una o más funciones explícitas llamadas **ramas**. Cuando no se puede, la relación sigue siendo perfectamente válida como curva en el plano, pero requiere herramientas más avanzadas —límites, derivadas y, más adelante, cálculo multivariable— para estudiarla en profundidad. Esta sección introduce la idea de función implícita usando únicamente álgebra básica.

> **Nota histórica:** El lenguaje de las ecuaciones implícitas nace con la geometría analítica de **René Descartes** y **Pierre de Fermat** en el siglo XVII. Descartes estudió la curva $x^3 + y^3 = 3axy$, conocida como *folium de Descartes*, como ejemplo de una relación entre $x$ e $y$ que no admite un despeje sencillo. Esta misma idea preparó el terreno para el desarrollo posterior del cálculo diferencial.

### 12.1 La idea central

Una ecuación de la forma:
$$F(x, y) = 0$$

relaciona a $x$ e $y$ sin que una de las variables aparezca necesariamente despejada. Decimos que esta ecuación **define implícitamente** a $y$ como función de $x$ cuando, al despejar $y$, obtenemos una o más expresiones del tipo $y = f(x)$.

**Ejemplo 12.1:**
La ecuación $2x + 3y = 6$ está dada de forma implícita, pero despejar $y$ es inmediato:
$$\begin{align}
3y &= 6 - 2x \\
y &= 2 - \frac{2}{3}x
\end{align}$$

Por tanto, define explícitamente la función lineal $f(x) = 2 - \frac{2}{3}x$, con dominio $\mathbb{R}$.

**Ejemplo 12.2:**
La ecuación $x^2 + y^2 = 9$ no define a $y$ como una única función de $x$, porque al despejar obtenemos dos valores:
$$\begin{align}
y^2 &= 9 - x^2 \\
y &= \pm\sqrt{9 - x^2}
\end{align}$$

Cada signo determina una rama:
- Rama superior: $f_1(x) = \sqrt{9 - x^2}$, con dominio $[-3, 3]$.
- Rama inferior: $f_2(x) = -\sqrt{9 - x^2}$, con dominio $[-3, 3]$.

La ecuación completa representa el círculo, pero cada rama por separado sí es una función.

### 12.2 Despejando $y$ en las cónicas

En la sección anterior vimos que las cónicas pueden escribirse de forma implícita. Ahora retomamos esas ecuaciones y las despejamos paso a paso, obteniendo las ramas funcionales correspondientes.

**Ejemplo 12.3 (Elipse):**
Para la elipse $\frac{x^2}{16} + \frac{y^2}{9} = 1$, se tiene:
$$\begin{align}
\frac{y^2}{9} &= 1 - \frac{x^2}{16} \\
y^2 &= 9\left(1 - \frac{x^2}{16}\right) = \frac{9}{16}(16 - x^2) \\
y &= \pm\frac{3}{4}\sqrt{16 - x^2}
\end{align}$$

Las ramas son $f_1(x) = \frac{3}{4}\sqrt{16 - x^2}$ y $f_2(x) = -\frac{3}{4}\sqrt{16 - x^2}$, ambas con dominio $[-4, 4]$.

**Ejemplo 12.4 (Parábola horizontal):**
Para la parábola $x = y^2$, se tiene:
$$\begin{align}
y^2 &= x \\
y &= \pm\sqrt{x}
\end{align}$$

Las ramas son $f_1(x) = \sqrt{x}$ y $f_2(x) = -\sqrt{x}$, con dominio $[0, +\infty)$.

**Ejemplo 12.5 (Hipérbola):**
Para la hipérbola $x^2 - y^2 = 1$, se tiene:
$$\begin{align}
y^2 &= x^2 - 1 \\
y &= \pm\sqrt{x^2 - 1}
\end{align}$$

Las ramas son $f_1(x) = \sqrt{x^2 - 1}$ y $f_2(x) = -\sqrt{x^2 - 1}$, con dominio $(-\infty, -1] \cup [1, +\infty)$.

### 12.3 Cuando no se puede despejar fácilmente

No toda ecuación implícita admite un despeje sencillo en términos de funciones elementales. En esos casos la relación se estudia como curva en el plano, y más adelante, con herramientas de cálculo diferencial, se podrá analizar su comportamiento sin necesidad de despejar.

**Ejemplo 12.6 (Folium de Descartes):**
La curva definida por:
$$x^3 + y^3 = 3axy$$

con $a > 0$, es un ejemplo clásico. Aunque algebraicamente es posible despejar $y$ usando la fórmula de Cardano para ecuaciones cúbicas, la expresión resultante es tan complicada que no resulta útil. Por esta razón se prefiere trabajar con la ecuación implícita.

**Ejemplo 12.7 (Lemniscata de Bernoulli):**
La curva:
$$(x^2 + y^2)^2 = 2a^2(x^2 - y^2)$$

con $a > 0$, tiene forma de "8". Despejar $y$ de manera sencilla no es viable, por lo que la descripción implícita es la forma natural de estudiarla.

### 12.4 Aplicaciones

Las ecuaciones implícitas aparecen en contextos donde las variables están relacionadas de manera natural, sin que una de ellas sea la "variable de salida" evidente.

- **Geometría:** Las cónicas, el folium de Descartes y la lemniscata de Bernoulli se expresan de forma implícita de manera elegante. La forma implícita suele ser más compacta y simétrica que cualquier despeje explícito.

- **Física:** Muchas leyes naturales se escriben como ecuaciones que relacionan varias cantidades. Por ejemplo, la ecuación de estado de un gas real relaciona presión, volumen y temperatura de forma implícita.

- **Economía:** Las curvas de indiferencia y las isocuantas describen conjuntos de puntos $(x, y)$ que satisfacen una ecuación $F(x, y) = k$. Aunque en este curso aún no se estudian las tasas marginales, la idea de una relación implícita entre variables ya está presente.

### 12.5 Observaciones

> **Observación (forma implícita vs. explícita):** La elección entre ambas formas depende del propósito. Si se busca simetría y generalidad, la forma implícita es preferible. Si se necesita evaluar o graficar una función, a menudo es necesario recurrir a ramas explícitas.

> **Observación (curvas que no son funciones):** Muchas curvas importantes, como el círculo completo o la elipse completa, no son funciones $y = f(x)$. Para estudiarlas con las herramientas del cálculo se recurre a dividirlas en ramas o, más adelante, a parametrizaciones.

> **Observación (hacia el futuro):** Cuando el curso desarrolle las herramientas del cálculo diferencial, será posible estudiar ecuaciones implícitas sin despejar $y$. Ese estudio incluye la **derivación implícita** y el **Teorema de la Función Implícita**, que se abordan formalmente en cursos de cálculo multivariable.

---

*Fin de Clase 9 - Funciones Parte 2*