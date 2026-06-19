# Funciones Parte 2

En esta clase profundizaremos en el análisis de funciones, estableciendo definiciones formales para las transformaciones geométricas, la clasificación según simetría (paridad), la composición de funciones, y el estudio riguroso de la inyectividad, sobreyectividad y funciones inversas.
## 1. Transformaciones de Funciones

Las transformaciones permiten generar nuevas familias de funciones a partir de una función elemental $f(x)$.
### 1.1 Traslaciones (Desplazamientos)

**Definición 1.1 (Traslación vertical):**
Dada una función $y = f(x)$ y una constante $c > 0$:
- La gráfica de $y = f(x) + c$ es la traslación de $f$ en $c$ unidades hacia **arriba**.
- La gráfica de $y = f(x) - c$ es la traslación de $f$ en $c$ unidades hacia **abajo**.
**Ejemplo 1.1:** Si $f(x) = x^2$, entonces $y = x^2 + 3$ mueve la parábola 3 unidades hacia arriba.

**Definición 1.2 (Traslación horizontal):**
Dada una función $y = f(x)$ y una constante $a > 0$:
- La gráfica de $y = f(x - a)$ es la traslación de $f$ en $a$ unidades hacia la **derecha**.
- La gráfica de $y = f(x + a)$ es la traslación de $f$ en $a$ unidades hacia la **izquierda**.
**Ejemplo 1.2:** Si $f(x) = x^2$, entonces $y = (x - 2)^2$ mueve el vértice de la parábola 2 unidades hacia la derecha.

Esta regla tiene una razón geométrica directa: para obtener el mismo valor de salida en la función desplazada $f(x-a)$, la entrada $x$ debe ser $a$ unidades mayor que en la función original.
### 1.2 Escalados (Dilataciones y Contracciones)

**Definición 1.3 (Escalado vertical):**
Sea $y = c \cdot f(x)$ con $c > 0$.
- Si $c > 1$: **Dilatación vertical** (expansión) por un factor de $c$.
- Si $0 < c < 1$: **Contracción vertical** (compresión) por un factor de $c$.
**Ejemplo 1.3:** Si $f(x) = x^2$, entonces $y = 3x^2$ estira la parábola verticalmente, haciéndola lucir más "angosta" o cerrada.

**Definición 1.4 (Escalado horizontal):**
Sea $y = f(c \cdot x)$ con $c > 0$.
- Si $c > 1$: **Contracción horizontal** por un factor de $1/c$.
- Si $0 < c < 1$: **Dilatación horizontal** por un factor de $1/c$.
**Ejemplo 1.4:** Si $f(x) = x^2$, entonces $y = (\frac{1}{2}x)^2$ ensancha la parábola horizontalmente.
### 1.3 Reflexiones

Imaginemos que observamos el reflejo de un paisaje sobre la superficie cristalina de un lago en absoluta calma: la línea del agua actúa como un espejo perfecto que invierte verticalmente todo lo que está por encima. En física, cuando un rayo de luz incide sobre un espejo plano, rebota de manera simétrica conservando su ángulo de incidencia. En acústica y procesamiento de señales, invertir la polaridad de una onda de sonido equivale a multiplicarla por $-1$, lo cual genera una onda "espejada" que puede emplearse para cancelar ruidos no deseados.

En matemáticas, estas transformaciones geométricas de espejado se denominan **reflexiones**. Permiten voltear una gráfica vertical u horizontalmente con respecto a una recta de referencia (el eje de reflexión), mapeando cada punto original a un punto simétrico ubicado exactamente a la misma distancia de dicho eje.

**Definición 1.5 (Reflexiones estándar):**
Las reflexiones básicas se realizan con respecto a los ejes coordenados:
- **Reflexión respecto al eje X:** $y = -f(x)$. El punto $(x, y)$ se mapea a $(x, -y)$.
- **Reflexión respecto al eje Y:** $y = f(-x)$. El punto $(x, y)$ se mapea a $(-x, y)$.
 
**Ejemplo 1.5:** Si usamos la función $f(x) = x^3 + 4$:
- La reflexión respecto al eje X nos da $y = -(x^3 + 4) = -x^3 - 4$ (la curva entera se voltea hacia abajo).
- La reflexión respecto al eje Y nos da $y = (-x)^3 + 4 = -x^3 + 4$ (la curva se voltea de izquierda a derecha, pero mantiene su altura).
 
> *(Nota sobre simetrías: Algunas funciones elementales tienen propiedades visuales curiosas al reflejarse. Por ejemplo, al reflejar $f(x) = x^2$ respecto al eje Y, la gráfica se mantiene intacta ($(-x)^2 = x^2$). O en el caso de $f(x) = x^3$, su reflexión en el eje X ($-x^3$) resulta ser visualmente idéntica a su reflexión en el eje Y ($(-x)^3$). Este comportamiento lo analizaremos a fondo más adelante en la clasificación de funciones Pares e Impares).*

### 1.3.1 Generalización: Reflexiones respecto a ejes arbitrarios

Las reflexiones no se limitan a los ejes coordenados principales. Es posible reflejar una gráfica en torno a cualquier recta en el plano cartesiano.

**1. Reflexión respecto a una recta horizontal $y = c$:**
Si se desea reflejar la gráfica de $y = f(x)$ respecto a una recta de simetría horizontal de ecuación $y = c$, la distancia vertical de cualquier punto de la función original a la recta $y = c$ debe conservarse pero en sentido opuesto. 
Si el punto original es $(x, f(x))$, su imagen reflejada $(x, y')$ tiene como punto medio al eje de reflexión, es decir:
$$\dfrac{f(x) + y'}{2} = c \implies y' = 2c - f(x)$$
De este modo, la ecuación de la función reflejada respecto a $y = c$ es:
$$y = 2c - f(x)$$

**2. Reflexión respecto a una recta vertical $x = c$:**
Análogamente, si se refleja la gráfica de $y = f(x)$ con respecto a una recta vertical de ecuación $x = c$, la abscisa de cualquier punto $x$ se mapea a una nueva abscisa $x'$ de modo que $c$ es el punto medio entre ambos:
$$\dfrac{x + x'}{2} = c \implies x' = 2c - x$$
Por lo tanto, la ecuación de la función reflejada respecto a $x = c$ es:
$$y = f(2c - x)$$

**Ejemplo 1.6 (Ejes horizontales y verticales arbitrarios):**
Dada la función $f(x) = \sqrt{x}$:
- La reflexión respecto a la recta horizontal $y = 3$ nos da:
  $$y = 2(3) - \sqrt{x} = 6 - \sqrt{x}$$
- La reflexión respecto a la recta vertical $x = 4$ nos da:
  $$y = \sqrt{2(4) - x} = \sqrt{8 - x}$$
  *Donde el nuevo dominio requiere que $8 - x \geq 0 \implies x \leq 8$.*

**3. Reflexión respecto a una recta oblicua arbitraria $y = mx + n$:**
Si se desea reflejar la gráfica de una función con respecto a una recta oblicua $L: mx - y + n = 0$ (con $m \neq 0$), debemos recurrir a la geometría analítica. Para cualquier punto $(x, y)$ de la función (donde $y = f(x)$), su punto reflejado $(x', y')$ debe cumplir dos condiciones geométricas fundamentales:
1. El segmento que une $(x, y)$ con $(x', y')$ debe ser perpendicular a la recta $L$ (pendiente $-\tfrac{1}{m}$).
2. El punto medio del segmento debe pertenecer a la recta $L$.

Al plantear y resolver el sistema de ecuaciones lineales resultante para las coordenadas transformadas $(x', y')$, se obtienen las siguientes ecuaciones de transformación paramétricas:
$$
\begin{cases}
x' = \dfrac{(1 - m^2)x + 2m(f(x) - n)}{1 + m^2} \\[12pt]
y' = \dfrac{2mx + (m^2 - 1)f(x) + 2n}{1 + m^2}
\end{cases}
$$

> **Observación:** La curva resultante $(x', y')$ no siempre definirá una función en el sentido analítico estándar, ya que la gráfica podría fallar la prueba de la línea vertical dependiendo de la pendiente $m$ y de la naturaleza de $f(x)$ (este comportamiento se detallará en la subsección posterior sobre rotaciones).

### 1.4 Rotación

La rotación general de una función $y=f(x)$ no necesariamente resulta en una nueva función válida (pues la gráfica podría "voltearse" sobre sí misma y violar la prueba de la línea vertical, un fenómeno de pérdida de unicidad análogo al descrito para la reflexión en rectas oblicuas en la subsección 1.3.1). Para rotar una gráfica un ángulo $\theta$ en sentido antihorario respecto al origen, tomamos cada punto original $(x, y)$ (donde recordamos que $y = f(x)$) y calculamos sus nuevas coordenadas transformadas $(x', y')$ utilizando el siguiente sistema de ecuaciones trigonométricas directas:

$$
\begin{cases}
x' = x \cos(\theta) - f(x) \sin(\theta) \\
y' = x \sin(\theta) + f(x) \cos(\theta)
\end{cases}
$$

**Demostración: Condición de Perpendicularidad (Rotación de $\pi/2$)**
Podemos usar estas ecuaciones para demostrar rigurosamente de dónde viene la regla de que la pendiente de una recta perpendicular es $-1/m$. 
Si tomamos una recta genérica cualquiera $f(x) = mx+b$ y la rotamos $\pi/2$ radianes ($90^\circ$), sabemos que $\cos(\pi/2) = 0$ y $\sin(\pi/2) = 1$. Sustituyendo esto en nuestro sistema:

$$
\begin{cases}
x' = x(0) - (mx+b)(1) \implies x' = -mx - b \\
y' = x(1) + (mx+b)(0) \implies y' = x
\end{cases}
$$

De la primera ecuación, podemos despejar $x$:
$$mx = -x' - b \implies x = -\frac{1}{m}x' - \frac{b}{m}$$

Sustituyendo este valor de $x$ en la segunda ecuación ($y' = x$), obtenemos directamente la ecuación de la nueva recta transformada:
$$y' = -\frac{1}{m}x' - \frac{b}{m}$$

¡La nueva gráfica sigue siendo una recta cuya pendiente es exactamente $-1/m$! Hemos demostrado algebraicamente que sin importar la posición inicial (intercepto $b$), la rotación de 90° siempre produce la condición de perpendicularidad. $\blacksquare$

**Ejemplo 1.7: Rotación de $f(x) = \sin(x)$ (Violación de unicidad)**
En el caso anterior, la rotación de la recta produjo otra recta (otra función). Sin embargo, veamos qué ocurre de manera extrema si rotamos una onda periódica como $f(x) = \sin(x)$ en un ángulo de $\pi/2$ radianes ($90^\circ$).

Sabemos que $\cos(\pi/2) = 0$ y $\sin(\pi/2) = 1$. Sustituyendo en las ecuaciones de rotación:
$$
\begin{cases}
x' = x(0) - \sin(x)(1) \implies x' = -\sin(x) \\
y' = x(1) + \sin(x)(0) \implies y' = x
\end{cases}
$$
![[sin(x)_rotado.png]]
Si observamos con atención el resultado, dado que $x = y'$, la nueva gráfica satisface la ecuación $x' = -\sin(y')$. ¡Hemos transformado una onda que viajaba a lo largo del eje X en una onda que ahora serpentea verticalmente a lo largo del eje Y!

Al graficar esto, la curva oscilará de izquierda a derecha entre $x' = -1$ y $x' = 1$ mientras sube y baja infinitamente a lo largo de $y'$. Si evaluamos la coordenada $x' = 0$, encontraremos **infinitos valores** para $y'$ correspondientes a las raíces del seno ($0, \pi, -\pi, 2\pi, \dots$). 
Por ende, al trazar una línea recta vertical imaginaria sobre el origen del eje X, esta cortará la curva en infinitos puntos simultáneamente. Esto reprueba categóricamente la **prueba de la línea vertical**, violando la regla estricta de unicidad de imagen de toda función (cada entrada de $x$ debe mapear a **solo un** valor de $y$). Hemos demostrado así que una rotación general puede destruir completamente la integridad matemática de una función.
### 1.5 Gráficas de Funciones Transformadas

Conocer las gráficas de las funciones elementales —parábola, valor absoluto, exponencial— no basta por sí solo. El verdadero poder del enfoque por transformaciones radica en que permite construir la gráfica de funciones compuestas **sin tabular punto a punto**: basta con identificar la función base $g$ y aplicar las transformaciones en el orden correcto.

Toda función de la forma $f(x) = a \cdot g(b(x - h)) + k$ se puede graficar siguiendo el procedimiento:

1. Partir de la gráfica de la **función base** $g(x)$.
2. Aplicar el **escalado horizontal** (factor $\tfrac{1}{b}$ sobre el eje $x$).
3. Aplicar el **desplazamiento horizontal** en $h$ unidades.
4. Aplicar el **escalado vertical** (factor $|a|$ sobre el eje $y$; reflexión si $a < 0$).
5. Aplicar el **desplazamiento vertical** en $k$ unidades.

**Ejemplo 1.8 (Transformación de la parábola):**
Graficar $f(x) = \dfrac{x^2}{2} + 5$.

Se identifica la función base $g(x) = x^2$ y se reescribe:
$$f(x) = \frac{1}{2}\,g(x) + 5$$

Las transformaciones son, en orden:

- **Contracción vertical** por $\dfrac{1}{2}$: $\quad g(x) = x^2 \;\longrightarrow\; \dfrac{x^2}{2}$

![[transformacion_parabola_paso1.png]]

- **Traslación vertical** $+5$: $\quad \dfrac{x^2}{2} \;\longrightarrow\; \dfrac{x^2}{2} + 5$

![[transformacion_parabola_paso2.png]]

Toda función desconocida puede construirse así: se descompone en su función base más las transformaciones necesarias para alcanzarla.

> **Advertencia:** Los desplazamientos horizontales pueden resultar engañosos cuando la variable $x$ aparece multiplicada por una constante. La traslación horizontal de $f(x) = g\!\left(b(x-h)\right)$ es de $h$ unidades, **no** de $bh$. Es imprescindible factorizar el coeficiente de $x$ antes de leer el desplazamiento.

**Ejemplo 1.9 (Desplazamiento horizontal con factor de escala):**
Determinar el desplazamiento que lleva $f(x) = |3x|$ a $g(x) = |3x + 1|$.

Factorizando el coeficiente de $x$ en el argumento de $g$:
$$g(x) = |3x + 1| = \left|3\left(x + \frac{1}{3}\right)\right| = f\left(x + \frac{1}{3}\right)$$

El desplazamiento real de la gráfica con respecto a $|3x|$ es de $\frac{1}{3}$ de unidad hacia la **izquierda**, no de $1$ unidad entera. Leer el "$+1$" como desplazamiento directo, sin factorizar primero el $3$, es el error más frecuente al realizar este tipo de transformaciones.

---
## 2. Simetría de Funciones (Paridad)

Sea $f: D \to \mathbb{R}$ una función con un dominio $D$ simétrico respecto al origen (es decir, si $x \in D$, entonces obligatoriamente $-x \in D$). En la sección anterior sobre reflexiones vimos que ciertas gráficas presentan comportamientos fascinantes al transformarse. Aquí formalizamos esos fenómenos mediante el concepto de **Paridad**.
### 2.1 Funciones Pares e Impares

**Definición 2.1 (Función Par):**
Una función $f$ es **par** si, para todo $x$ en su dominio, se cumple que evaluar un número negativo da exactamente el mismo resultado que evaluar el positivo:
$$\forall x \in D, \quad f(-x) = f(x)$$
- **Propiedad Geométrica:** Esto equivale a decir que su gráfica es idéntica tras aplicarle una reflexión respecto al **eje Y**. Es como si el eje Y actuara como un espejo perfecto.
- **Conexión con reflexiones:** Como lo prometimos, esto explica por qué la función $f(x) = x^2$ al reflejarse en el eje Y nos daba $(-x)^2 = x^2$. ¡Esto la clasifica formalmente como el prototipo de una función par!
- **Otros ejemplos:** $f(x) = |x|, \quad f(x) = \cos(x)$.

**Definición 2.2 (Función Impar):**
Una función $f$ es **impar** si, para todo $x$ en su dominio, el signo negativo puede "salir" de la función:
$$\forall x \in D, \quad f(-x) = -f(x)$$
- **Propiedad Geométrica:** Su gráfica es simétrica respecto al **origen** $(0,0)$. Esto equivale a rotar la gráfica 180° alrededor del origen, o lo que es lo mismo: aplicar una reflexión en el eje X y luego otra en el eje Y.
- **Conexión con reflexiones:** En nuestro análisis previo de la nota, vimos que para $f(x) = x^3$, su reflexión en Y ($(-x)^3$) daba exactamente el mismo resultado visual que su reflexión en X ($-x^3$). Esa coincidencia $f(-x) = -f(x)$ es la huella digital inconfundible de una función impar.
- **Otros ejemplos:** $f(x) = 1/x, \quad f(x) = \sin(x)$.

### 2.2 Teorema de Descomposición

La inmensa mayoría de las funciones en la naturaleza no son ni pares ni impares (son asimétricas). Sin embargo, existe una propiedad matemática extraordinaria que permite fraccionarlas.

**Teorema 2.1 (Descomposición de paridad):**
Toda función $f: \mathbb{R} \to \mathbb{R}$ (o sobre un dominio simétrico) puede expresarse de manera *única* como la suma exacta de una función par y una función impar:
$$f(x) = f_{par}(x) + f_{impar}(x)$$
Donde las componentes se construyen artificialmente mediante las fórmulas:
$$f_{par}(x) = \frac{f(x) + f(-x)}{2}, \quad f_{impar}(x) = \frac{f(x) - f(-x)}{2}$$

**Demostración del Teorema:**
La demostración consta de dos partes lógicas: asegurar que las fórmulas realmente cumplen su propósito (**Existencia**) y probar que son la única manera de lograrlo (**Unicidad**).

**1. Existencia:**
Si sumamos las dos fórmulas propuestas algebraicamente, obtenemos la función original:
$$f_{par}(x) + f_{impar}(x) = \frac{f(x) + f(-x)}{2} + \frac{f(x) - f(-x)}{2} = \frac{2f(x)}{2} = f(x)$$
Para comprobar que realmente tienen la paridad deseada, las evaluamos en $-x$:
- Para la primera: $f_{par}(-x) = \frac{f(-x) + f(-(-x))}{2} = \frac{f(-x) + f(x)}{2} = f_{par}(x)$. Queda demostrado que es **par**.
- Para la segunda: $f_{impar}(-x) = \frac{f(-x) - f(-(-x))}{2} = \frac{f(-x) - f(x)}{2} = -\frac{f(x) - f(-x)}{2} = -f_{impar}(x)$. Queda demostrado que es **impar**.

**2. Unicidad:**
Supongamos que existiera *otra* descomposición alternativa $f(x) = P(x) + I(x)$, donde $P$ sea par e $I$ sea impar.
Al evaluar la función en $-x$, y usando las propiedades de paridad, tendríamos:
$$f(-x) = P(-x) + I(-x) = P(x) - I(x)$$

Hemos formado un sistema lineal de dos ecuaciones:
1) $f(x) = P(x) + I(x)$
2) $f(-x) = P(x) - I(x)$

Si **sumamos** ambas ecuaciones, las partes impares ($I$) se anulan:
$$f(x) + f(-x) = 2P(x) \implies P(x) = \frac{f(x) + f(-x)}{2}$$
Si **restamos** la segunda de la primera, las partes pares ($P$) se anulan:
$$f(x) - f(-x) = 2I(x) \implies I(x) = \frac{f(x) - f(-x)}{2}$$
Acabamos de probar que cualquier supuesta "otra" descomposición $P(x)$ e $I(x)$ nos obliga irremediablemente a recaer en las mismas fórmulas originales. Por lo tanto, no hay otra manera de hacerlo; la descomposición es **absolutamente única**. $\blacksquare$

**Ejemplo 2.1 (Descomposición de un polinomio asimétrico):**
Descomponer la función $f(x) = x^2 + 2x + 3$.

**Solución:** Primero hallamos el reflejo $f(-x)$:
$$f(-x) = (-x)^2 + 2(-x) + 3 = x^2 - 2x + 3$$
- Calculamos la **parte par** sumando ambos y dividiendo por 2:
  $$f_{par}(x) = \frac{(x^2 + 2x + 3) + (x^2 - 2x + 3)}{2} = \frac{2x^2 + 6}{2} = x^2 + 3$$
- Calculamos la **parte impar** restando y dividiendo por 2:
  $$f_{impar}(x) = \frac{(x^2 + 2x + 3) - (x^2 - 2x + 3)}{2} = \frac{4x}{2} = 2x$$
**Conclusión:** $f(x) = (x^2 + 3) + (2x)$. Hemos logrado separar de manera analítica un polinomio común en su "esqueleto" par ($x^2+3$) y su "esqueleto" impar ($2x$).

**Ejemplo 2.2 (Descomposición de la función exponencial):**
Descomponer la función asimétrica por excelencia, $f(x) = e^x$.

**Solución:** Hallamos $f(-x) = e^{-x}$.
- **Parte par:**
$$f_{par}(x) = \frac{e^x + e^{-x}}{2}$$
- **Parte impar:**
$$f_{impar}(x) = \frac{e^x - e^{-x}}{2}$$
**Conclusión:** ¡Estas dos mitades no son funciones ordinarias! Acabamos de derivar matemáticamente de la nada al famoso **Coseno Hiperbólico** ($\cosh(x)$) como la parte par de $e^x$, y al **Seno Hiperbólico** ($\sinh(x)$) como su parte impar. Así, se desvela la hermosa identidad: $e^x = \cosh(x) + \sinh(x)$. Esto se profundizará en la sección 6.

---
## 3. Funciones Definidas a Tramos

Algunas funciones tienen comportamientos diferentes en distintas regiones de su dominio. Por ejemplo, una tarifa telefónica puede tener un precio por minuto hasta cierta cantidad, y luego otro precio diferente. Estas funciones se expresan mediante "casos" o "tramos".

**Definición 3.1 (Función a tramos):**
Una **función definida a tramos** (o función por partes) es una función que se define mediante diferentes expresiones algebraicas en distintos subconjuntos del dominio. Formalmente:

$$f(x) = \begin{cases} f_1(x) & \text{si } x \in D_1 \\ f_2(x) & \text{si } x \in D_2 \\ \vdots & \vdots \\ f_n(x) & \text{si } x \in D_n \end{cases}$$

donde $D_1, D_2, \ldots, D_n$ son subconjuntos **disjuntos** cuya unión es el dominio de $f$.

### 3.1 Ejemplos fundamentales

**Ejemplo 3.1 (Valor absoluto):**
La función valor absoluto es el ejemplo más conocido de función a tramos:
$$f(x) = |x| = \begin{cases} -x & \text{si } x < 0 \\ x & \text{si } x \geq 0 \end{cases}$$

**Análisis:**
- Para $x < 0$: $|x| = -x$ (negamos el número negativo para obtener su magnitud)
- Para $x \geq 0$: $|x| = x$ (el número ya es no negativo)
- **Punto crítico:** $x = 0$ es donde cambia la definición

**Ejemplo 3.2 (Función rampa):**
La función rampa, denotada $r(x)$ o $\text{ramp}(x)$, se define como:
$$r(x) = \max(0, x) = \begin{cases} 0 & \text{si } x < 0 \\ x & \text{si } x \geq 0 \end{cases}$$

Esta función es ampliamente usada en:
- Ingeniería eléctrica (señales)
- Redes neuronales (función de activación ReLU)
- Economía (funciones de demanda)

**Observación:** Se puede expresar como $r(x) = \frac{x + |x|}{2}$.

**Ejemplo 3.3 (Función definida por tres tramos):**
$$f(x) = \begin{cases} x^2 & \text{si } x < -1 \\ 1 & \text{si } -1 \leq x \leq 1 \\ 2x - 1 & \text{si } x > 1 \end{cases}$$

**Evaluación:**
- $f(-2) = (-2)^2 = 4$ (usa el primer tramo)
- $f(0) = 1$ (usa el segundo tramo)
- $f(3) = 2(3) - 1 = 5$ (usa el tercer tramo)

**Ejemplo 3.4 (Tarifa escalonada):**
Una compañía eléctrica cobra según el consumo:
$$C(k) = \begin{cases} 0.10k & \text{si } 0 \leq k \leq 100 \\ 10 + 0.15(k-100) & \text{si } 100 < k \leq 300 \\ 40 + 0.20(k-300) & \text{si } k > 300 \end{cases}$$

donde $k$ es el consumo en kWh y $C(k)$ es el costo en dólares.

### 3.2 Continuidad en los puntos de unión

Cuando una función está definida a tramos, es importante verificar qué ocurre en los **puntos de transición** donde cambia la fórmula. La función puede ser:
- **Continua:** No hay "saltos" en la gráfica
- **Discontinua:** Hay un "salto" o "brecha" en ese punto

**Observación:** En términos intuitivos, una función es continua en un punto si su gráfica no presenta saltos ni interrupciones en la vecindad de ese punto.

**Ejemplo 3.5 (Función continua a tramos):**
$$f(x) = \begin{cases} x + 2 & \text{si } x < 1 \\ 3 & \text{si } x = 1 \\ -x + 4 & \text{si } x > 1 \end{cases}$$

**Verificación en $x = 1$:**
- Desde la izquierda: $\lim_{x \to 1^-} f(x) = 1 + 2 = 3$
- En el punto: $f(1) = 3$
- Desde la derecha: $\lim_{x \to 1^+} f(x) = -1 + 4 = 3$

Como todos coinciden, la función es **continua** en $x = 1$.

**Ejemplo 3.6 (Función discontinua a tramos):**
$$g(x) = \begin{cases} x^2 & \text{si } x < 2 \\ x + 3 & \text{si } x \geq 2 \end{cases}$$

**Verificación en $x = 2$:**
- Desde la izquierda: $\lim_{x \to 2^-} g(x) = 2^2 = 4$
- En el punto: $g(2) = 2 + 3 = 5$

Hay un **salto** de 4 a 5, por lo que la función es **discontinua** en $x = 2$.

**Nota:** El concepto formal de continuidad se estudiará en profundidad en el tema de Límites y Continuidad.

---
## 4. Funciones Especiales y Funciones Peculiares

La definición formal de función —una regla que asigna a cada elemento de un conjunto exactamente un elemento de otro conjunto— es deliberadamente amplia. Las funciones que se estudian en una primera clase (polinomios, exponenciales, trigonométricas, logaritmos) comparten una característica que nos vuelve cómodos: son curvas suaves, predecibles y fácilmente graficables. Sin embargo, la definición de función no exige ninguna de esas cualidades.

**Definición 4.0 (Función Especial):**
Se denomina **función especial** a toda función que, por su recurrencia y utilidad en matemáticas, física o ingeniería, ha recibido un nombre propio, una notación estandarizada y un estudio sistemático de sus propiedades. No existe un criterio único y universal para determinar si una función merece ese título; la distinción es convencional y refleja la importancia histórica y práctica de la función dentro de la comunidad científica.

Esta sección tiene dos propósitos distintos. Por un lado, presentar funciones con nombre propio que aparecerán repetidamente en cursos de ingeniería, física y computación —familiarizarse con ellas ahora facilita enormemente el trabajo futuro. Por otro, mostrar funciones construidas deliberadamente para desafiar la intuición, cuyo estudio ha sido fundamental para el desarrollo del Análisis Matemático moderno.
### 4.1 Función Piso, Función Techo y Parte Fraccionaria

Pensemos en el problema cotidiano de redondear un número real hacia el entero más cercano. Si se tiene $x = 3.7$, intuitivamente se sabe que "cabe" dentro del intervalo $[3, 4)$. Las funciones piso y techo formalizan exactamente esa idea: determinar cuál es el entero inmediatamente inferior o superior a un real dado.

**Definición 4.1 (Función Piso):**
La función piso $\lfloor \cdot \rfloor : \mathbb{R} \to \mathbb{Z}$ asigna a cada $x \in \mathbb{R}$ el mayor entero menor o igual a $x$:
$$\lfloor x \rfloor = \max\{k \in \mathbb{Z} : k \leq x\}$$

> **Observación:** Se cumple que $\lfloor x \rfloor \leq x < \lfloor x \rfloor + 1$ para todo $x \in \mathbb{R}$.

**Definición 4.2 (Función Techo):**
La función techo $\lceil \cdot \rceil : \mathbb{R} \to \mathbb{Z}$ asigna a cada $x \in \mathbb{R}$ el menor entero mayor o igual a $x$:
$$\lceil x \rceil = \min\{k \in \mathbb{Z} : k \geq x\}$$

**Ejemplo 4.1:**
$$\lfloor 3.7 \rfloor = 3, \quad \lfloor -1.2 \rfloor = -2, \quad \lfloor 5 \rfloor = 5$$
$$\lceil 3.7 \rceil = 4, \quad \lceil -1.2 \rceil = -1, \quad \lceil 5 \rceil = 5$$

> **Advertencia:** Para números negativos, $\lfloor -1.2 \rfloor = -2$, no $-1$. La función piso siempre redondea hacia $-\infty$, no hacia cero.

Una vez definida la función piso, se puede extraer de cualquier real su parte decimal de manera precisa.

**Definición 4.3 (Parte Fraccionaria):**
La parte fraccionaria $\{\cdot\} : \mathbb{R} \to [0,1)$ se define para todo $x \in \mathbb{R}$ como:
$$\{x\} = x - \lfloor x \rfloor$$

Su gráfica es una onda de sierra periódica de período 1: sube linealmente desde 0 hasta 1 (sin alcanzarlo) y luego reinicia. Es un ejemplo de función periódica que no tiene relación alguna con la trigonometría.

**Ejemplo 4.2:**
$$\{3.7\} = 3.7 - 3 = 0.7, \quad \{-1.2\} = -1.2 - (-2) = 0.8, \quad \{5\} = 0$$

### 4.2 Función Signo y Función de Heaviside

Estas dos funciones modelan comportamientos de "todo o nada": situaciones en que solo interesa el signo de una cantidad, o el instante en que un fenómeno se activa. Son omnipresentes en ingeniería de control, procesamiento de señales y sistemas dinámicos.

**Definición 4.4 (Función Signo):**
La función signo $\text{sgn} : \mathbb{R} \to \{-1, 0, 1\}$ se define como:
$$\text{sgn}(x) = \begin{cases} -1 & \text{si } x < 0 \\ 0 & \text{si } x = 0 \\ 1 & \text{si } x > 0 \end{cases}$$

**Definición 4.5 (Función de Heaviside):**
La función de Heaviside $H : \mathbb{R} \to \{0, 1\}$, también llamada escalón unitario, se define como:

$$H(x) = \begin{cases} 0 & \text{si } x < 0 \\ 1 & \text{si } x \geq 0 \end{cases}$$

> **Nota histórica:** Oliver Heaviside (1850–1925) fue un ingeniero eléctrico autodidacta que desarrolló esta función para modelar el encendido de circuitos eléctricos en $t = 0$. Sus métodos fueron inicialmente rechazados por carecer de rigor, pero resultaron correctos y hoy son estándar en ingeniería.

> **Nota:** En algunos textos, $H(0)$ se define como $\frac{1}{2}$ o se deja indefinido. La definición varía según el contexto de aplicación.

Se puede verificar que ambas funciones se relacionan mediante:
$$\text{sgn}(x) = 2H(x) - 1 \quad \text{para } x \neq 0$$

### 4.3 Función Logística (Sigmoide)

Pensemos en el crecimiento de una población dentro de un ecosistema con recursos limitados: al principio crece lentamente (pocos individuos), luego se acelera (fase exponencial) y finalmente desacelera al acercarse al límite de recursos del entorno. Este comportamiento en forma de "S" es exactamente lo que describe la función logística.

**Definición 4.6 (Función Logística):**
La función logística $f : \mathbb{R} \to (0, L)$ se define como:
$$f(x) = \frac{L}{1 + e^{-k(x - x_0)}}$$
donde $L > 0$ es la cota superior (asíntota horizontal), $k > 0$ es la tasa de crecimiento y $x_0 \in \mathbb{R}$ es el punto de inflexión (centro de la curva).

La forma más simple, con $L = 1$, $k = 1$, $x_0 = 0$, se denomina **función sigmoide estándar**:
$$\sigma(x) = \frac{1}{1 + e^{-x}}$$

> **Observación:** La función sigmoide es fundamental en aprendizaje automático: se utiliza como función de activación en redes neuronales y como función de salida en regresión logística, donde su recorrido $(0,1)$ permite interpretarla como una probabilidad.

### 4.4 Función Gaussiana

La función gaussiana describe la forma de la famosa "campana de Gauss". Aparece en probabilidad y estadística (distribución normal), en física cuántica (paquetes de onda), en óptica (perfiles de haces láser) y en procesamiento de imágenes, entre muchos otros contextos.

**Definición 4.7 (Función Gaussiana):**
La función gaussiana estándar $f : \mathbb{R} \to (0, 1]$ se define como:
$$f(x) = e^{-x^2}$$

Es siempre positiva, alcanza su máximo en $x = 0$ con $f(0) = 1$, y decrece simétricamente hacia cero en ambas direcciones.

> **Observación:** En Cálculo Integral se verá que $f(x) = e^{-x^2}$ no posee antiderivada elemental: no existe ninguna combinación de funciones elementales (polinomios, exponenciales, trigonométricas, logaritmos) cuya derivada sea $e^{-x^2}$. A pesar de ello, el área encerrada bajo la curva sobre todo $\mathbb{R}$ tiene un valor exacto y sorprendente: $\sqrt{\pi}$.

### 4.5 Función Sinc (Seno Cardinal)

Si se observa qué ocurre con $\frac{\sin(x)}{x}$ al alejar $x$ del origen, se tiene una onda que oscila pero cuya amplitud decae progresivamente. Esta forma es característica de fenómenos de difracción en óptica y de filtros ideales en procesamiento de señales.

**Definición 4.8 (Función Sinc):**
La función seno cardinal $\text{sinc} : \mathbb{R} \to \mathbb{R}$ se define como:
$$\text{sinc}(x) = \begin{cases} \dfrac{\sin(x)}{x} & \text{si } x \neq 0 \\[6pt] 1 & \text{si } x = 0 \end{cases}$$

El valor en $x = 0$ se establece por continuidad: en Cálculo de Límites se demostrará que $\displaystyle\lim_{x \to 0} \frac{\sin(x)}{x} = 1$.

### 4.6 Deltas: Kronecker y Dirac

A veces interesa modelar un evento que ocurre en un único punto exacto: un golpe instantáneo, una carga puntual, un pulso eléctrico de duración despreciable. Las funciones delta surgen de esa necesidad.

**Definición 4.9 (Delta de Kronecker):**
Para $i, j \in \mathbb{Z}$, la delta de Kronecker $\delta : \mathbb{Z} \times \mathbb{Z} \to \{0,1\}$ se define como:
$$\delta_{ij} = \begin{cases} 1 & \text{si } i = j \\ 0 & \text{si } i \neq j \end{cases}$$

Se utiliza en álgebra lineal para describir matrices identidad y sistemas ortogonales. Será recurrente en el curso de Álgebra Lineal.

**Definición 4.10 (Delta de Dirac):**
La delta de Dirac $\delta(x)$ es el análogo continuo de la delta de Kronecker. Intuitivamente modela un impulso concentrado en un único punto: vale cero en todo $x \neq 0$, pero su "masa" total es exactamente 1. Se define formalmente en la teoría de distribuciones —una extensión del concepto de función que se estudia en cursos avanzados de Análisis— y no es una función en el sentido clásico.

Se escribe habitualmente como:
$$\delta(x) = \begin{cases} +\infty & \text{si } x = 0 \\ 0 & \text{si } x \neq 0 \end{cases}$$

con la condición adicional de que su "masa" total es exactamente 1.

> **Advertencia:** Esta definición a trozos es únicamente una descripción intuitiva. $\delta(x)$ no es una función en el sentido clásico —ninguna función puede valer $+\infty$ en un punto y aun así tener masa total finita dentro del marco habitual del Cálculo. Se define formalmente en la teoría de distribuciones, que corresponde a cursos avanzados de Análisis. Se menciona aquí como familiarización, dada su importancia en ingeniería de control, mecánica cuántica y ecuaciones diferenciales.

### 4.7 Función Indicatriz y Función de Dirichlet

Las siguientes funciones actúan como "detectores de pertenencia" a conjuntos. Son construcciones simples pero de gran importancia teórica.

**Definición 4.11 (Función Indicatriz):**
Sea $A \subseteq \mathbb{R}$. La función indicatriz $\mathbf{1}_A : \mathbb{R} \to \{0, 1\}$ se define como:
$$\mathbf{1}_A(x) = \begin{cases} 1 & \text{si } x \in A \\ 0 & \text{si } x \notin A \end{cases}$$

**Definición 4.12 (Función de Dirichlet):**
La función de Dirichlet $D : \mathbb{R} \to \{0, 1\}$ es el caso particular de la función indicatriz sobre el conjunto de los racionales $\mathbb{Q}$:
$$D(x) = \mathbf{1}_{\mathbb{Q}}(x) = \begin{cases} 1 & \text{si } x \in \mathbb{Q} \\ 0 & \text{si } x \notin \mathbb{Q} \end{cases}$$

> **Nota histórica:** Peter Gustav Lejeune Dirichlet propuso esta función en 1829 como contraejemplo a la noción intuitiva de que toda función puede integrarse. Fue uno de los primeros ejemplos que impulsó el desarrollo riguroso del Análisis.

Esta función es discontinua en absolutamente todos los puntos de $\mathbb{R}$. La razón es que entre dos racionales siempre existe un irracional y viceversa, de modo que en cualquier vecindad de cualquier punto conviven valores de ambos tipos. En consecuencia, la función oscila entre 0 y 1 en toda vecindad, sin importar cuán pequeña sea.

### 4.8 Función de Thomae y Función de Weierstrass

Estas dos funciones representan algunos de los resultados más contraintuitivos del Análisis Matemático del siglo XIX. Se presentan aquí como cultura matemática y como motivación para comprender que la continuidad y la derivabilidad son propiedades verdaderamente profundas.

**Definición 4.13 (Función de Thomae):**
La función de Thomae $T : \mathbb{R} \to [0, 1]$, también llamada función de las "palomitas de maíz", se define como:
$$T(x) = \begin{cases} \dfrac{1}{q} & \text{si } x = \dfrac{p}{q} \in \mathbb{Q}, \text{ con } \gcd(p,q) = 1,\ q > 0 \\[6pt] 0 & \text{si } x \notin \mathbb{Q} \end{cases}$$

Su comportamiento es profundamente contraintuitivo: es continua en cada número irracional y discontinua en cada número racional. Demuestra que los conjuntos de puntos de continuidad y discontinuidad de una función pueden tener una estructura arbitrariamente compleja.

**Definición 4.14 (Función de Weierstrass):**
La función de Weierstrass $W : \mathbb{R} \to \mathbb{R}$ se define como la serie:
$$W(x) = \sum_{n=0}^{\infty} a^n \cos(b^n \pi x)$$
donde $0 < a < 1$, $b$ es un entero positivo impar, y $ab > 1 + \frac{3}{2}\pi$.

> **Nota histórica:** En 1872, Karl Weierstrass presentó esta función ante la Academia de Berlín, demostrando que es continua en todo $\mathbb{R}$ pero no es diferenciable en ningún punto. Hasta entonces, la comunidad matemática asumía —sin demostración— que toda función continua debía ser derivable salvo quizás en algunos puntos aislados. La presentación de Weierstrass fue considerada un escándalo matemático y obligó a refundar el Análisis sobre bases completamente rigurosas.

Se menciona aquí únicamente como cultura general. Su estudio formal corresponde a Análisis Real.
### 4.9 Ondas Cuadrada y Triangular

En la práctica de la ingeniería, las oscilaciones no siempre tienen la forma suave del seno o el coseno. Las señales digitales, los circuitos de control y los sintetizadores de audio trabajan constantemente con formas de onda que presentan cambios abruptos o pendientes constantes a trozos.

**Onda cuadrada:** Alterna periódicamente entre dos valores fijos, habitualmente $1$ y $-1$, con transiciones instantáneas. Modela señales digitales (bits) y señales de reloj en sistemas computacionales. Se puede expresar en términos de funciones ya definidas mediante:
$$f(x) = \text{sgn}(\sin(x))$$

**Onda triangular:** Sube y baja con pendiente lineal constante, formando una sucesión de picos afilados. Es común en síntesis de audio y en sistemas de barrido. Puede expresarse usando la parte fraccionaria:
$$f(x) = \left| 2\left\{\frac{x}{T}\right\} - 1 \right|$$
donde $T > 0$ es el período.

> **Observación:** Tanto la onda cuadrada como la triangular son funciones periódicas que pueden descomponerse como sumas infinitas de senos y cosenos. Este resultado, conocido como **serie de Fourier**, se estudiará formalmente en cursos de Ecuaciones Diferenciales o de Señales y Sistemas, y constituye una de las herramientas más poderosas de la ingeniería aplicada.

---
## 5. Periodicidad

### 5.1 Concepto de Periodicidad y Definición Formal

Muchos fenómenos en la naturaleza y en la ingeniería se repiten a intervalos regulares de tiempo o espacio: el latido de un corazón, el ciclo de las estaciones del año, el movimiento de un péndulo o la oscilación de un circuito eléctrico. Matemáticamente, capturamos este comportamiento repetitivo infinito mediante el concepto de funciones periódicas. La gran ventaja de estas funciones es que, si conocemos exactamente cómo se comportan en un solo ciclo, automáticamente conocemos su comportamiento en toda la recta real numérica.

**Definición 5.1 (Función Periódica):**
Una función $f: D \to \mathbb{R}$ se denomina **periódica** si existe un número real $T > 0$ tal que, para todo $x \in D$, se cumple:
1. $x + T \in D$
2. $f(x + T) = f(x)$

El número $T$ se llama un **período** de la función. El menor valor positivo $T$ que satisface esta condición se denomina **período fundamental** (frecuentemente llamado solo "el período").

**Proposición 5.1 (Múltiplos del período):**
Si $f$ es una función periódica con período $T$, entonces para cualquier número entero $n \in \mathbb{Z}$, se cumple que:
$$f(x + nT) = f(x)$$
Es decir, cualquier múltiplo entero del período fundamental también actúa como un período válido.

**Ejemplo 5.1:**
Las funciones trigonométricas son el arquetipo clásico por excelencia:
- La función $f(x) = \sin(x)$ cumple que $\sin(x + 2\pi) = \sin(x)$, por lo que su período fundamental es $T = 2\pi$. Por la Proposición 5.1, también se cumple que $\sin(x + 4\pi) = \sin(x)$ o $\sin(x - 6\pi) = \sin(x)$.
- La función $g(x) = \tan(x)$ tiene un período fundamental de $T = \pi$.
### 5.2 Más Allá de la Trigonometría

Aunque solemos asociar la periodicidad exclusivamente a los senos y cosenos, en la Sección 4 demostramos que existen muchas otras funciones periódicas exóticas y útiles.

**Ejemplo 5.2 (Parte fraccionaria):**
La función parte fraccionaria, $f(x) = \{x\} = x - \lfloor x \rfloor$, es estrictamente periódica. Vamos a demostrar analíticamente que su período es $T = 1$.

**Solución:**
Evaluamos la función desplazada en 1 unidad:
$$\begin{align}
f(x + 1) &= (x + 1) - \lfloor x + 1 \rfloor \\
&= x + 1 - (\lfloor x \rfloor + 1) \\
&= x - \lfloor x \rfloor \\
&= f(x)
\end{align}$$
La función se repite idéntica cada 1 unidad entera, generando su clásica gráfica de "diente de sierra".

**Ejemplo 5.3 (Ondas de ingeniería):**
La onda cuadrada y la onda triangular introducidas previamente también son periódicas. En ingeniería y física, al período $T$ (medido en segundos) se le asocia directamente una **frecuencia** $f$ (medida en Hertz o ciclos por segundo), definida simplemente como el inverso del período: $f = \frac{1}{T}$.
### 5.3 Alteración del Período mediante Transformaciones

¿Qué ocurre si aplicamos una transformación de escalado horizontal a una función periódica? Como se vio en la sección de transformaciones (Sección 1.2), multiplicar la variable independiente por una constante comprime o estira la gráfica como si fuera un resorte.

**Teorema 5.1 (Período de funciones escaladas):**
Si $f(x)$ es una función periódica con período fundamental $T$, entonces la nueva función compuesta $g(x) = f(cx)$, donde $c \neq 0$, tiene un nuevo período fundamental dado por:
$$T_{nuevo} = \frac{T}{|c|}$$

**Demostración:**
Buscamos un valor $P > 0$ tal que $g(x + P) = g(x)$ para todo $x$.
Sustituyendo en nuestra definición de $g$:
$$\begin{align}
g(x + P) &= f(c(x + P)) \\
&= f(cx + cP)
\end{align}$$
Sabemos por hipótesis que la función $f$ repite su valor cuando a su argumento interno se le suma su período original $T$. Por lo tanto, para que se complete un ciclo, la cantidad sumada $cP$ debe equivaler en magnitud a $T$:
$$|c|P = T \implies P = \frac{T}{|c|}$$
$\blacksquare$

**Ejemplo 5.4:**
Determinar el período de la función $h(x) = \sin(3x)$.

**Solución:**
Identificamos la función base y el factor de escalado:
- Función base: $\sin(x) \implies T = 2\pi$
- Factor de compresión: $c = 3$

Aplicando el Teorema 5.1:
$$T_{nuevo} = \frac{2\pi}{3}$$
**Interpretación:** El factor 3 comprime la gráfica horizontalmente. Ahora, la onda del seno completa un ciclo entero en un intervalo tres veces más corto que el original.
### 5.4 Análisis de Periodicidad en Casos Complejos

A continuación, analizaremos funciones progresivamente más complejas para dominar el cálculo de períodos, desde casos directos hasta la combinación de múltiples ondas.

**Ejemplo 5.5 (Caso simple: ensanchamiento horizontal):**
Determinar el período fundamental de $f(x) = \cos\left(\frac{x}{4}\right)$.

**Solución:**
La función base es $\cos(x)$, cuyo período fundamental es $T = 2\pi$.
El factor de escalado es $c = \frac{1}{4}$.
Aplicando el Teorema 5.1:
$$T_{nuevo} = \frac{2\pi}{1/4} = 8\pi$$
La onda se ha "estirado" horizontalmente, tardando cuatro veces más en completar un ciclo.

**Ejemplo 5.6 (Caso intermedio: potencias trigonométricas):**
Determinar el período de $g(x) = \sin^2(x)$.

**Solución:**
A simple vista podría pensarse que el período sigue siendo $2\pi$, pero al elevar al cuadrado, las partes negativas de la onda seno se vuelven positivas, haciendo que el patrón de la onda se repita más rápido. Para demostrarlo analíticamente, usamos la identidad trigonométrica del ángulo doble:
$$\sin^2(x) = \frac{1 - \cos(2x)}{2} = \frac{1}{2} - \frac{1}{2}\cos(2x)$$

Esta expresión es una función $\cos(2x)$ desplazada y escalada verticalmente, y tales transformaciones no afectan su período en el eje horizontal. 
Calculamos el período del término que define la oscilación, $\cos(2x)$:
$$T_{nuevo} = \frac{2\pi}{2} = \pi$$
Por lo tanto, el período fundamental de $\sin^2(x)$ se reduce a $\pi$.

**Ejemplo 5.7 (Caso avanzado: suma de funciones periódicas):**
Encontrar el período de la función combinada $h(x) = \sin(2x) + \cos(3x)$.

**Solución:**
Cuando sumamos dos funciones periódicas, la nueva función resultante será periódica solo si existe un intervalo maestro que contenga un número exacto de ciclos de **ambas** funciones a la vez. Este período maestro se encuentra calculando el Mínimo Común Múltiplo (MCM) de los períodos individuales.

1. Período de $\sin(2x)$: $T_1 = \frac{2\pi}{2} = \pi$
2. Período de $\cos(3x)$: $T_2 = \frac{2\pi}{3}$

Buscamos el MCM entre $\pi$ y $\frac{2\pi}{3}$. Analizamos los múltiplos de cada uno para encontrar su primera coincidencia:
- Múltiplos de $T_1$: $\pi, \mathbf{2\pi}, 3\pi, 4\pi, \ldots$
- Múltiplos de $T_2$: $\frac{2\pi}{3}, \frac{4\pi}{3}, \mathbf{\frac{6\pi}{3}} \ (\text{que es } 2\pi), \frac{8\pi}{3}, \ldots$

El primer valor en el que ambas ondas vuelven a sincronizarse perfectamente es $2\pi$. Por lo tanto, el período fundamental de $h(x)$ es $T = 2\pi$.

**Ejemplo 5.8 (El monstruo de la suma: funciones inmensurables):**
Demostrar si la función $p(x) = \sin(x) + \sin(\pi x)$ es periódica o no.

**Solución:**
Calculamos los períodos de ambas componentes individuales:
1. Período de $\sin(x)$: $T_1 = 2\pi$
2. Período de $\sin(\pi x)$: $T_2 = \frac{2\pi}{\pi} = 2$

Para que la suma total sea periódica, debe existir un período global $T$ que sea múltiplo entero de ambos. Es decir, debe existir un par de números enteros positivos $n$ y $m$ tales que al dar $n$ saltos del primer período y $m$ saltos del segundo, lleguemos al mismo punto:
$$n \cdot T_1 = m \cdot T_2$$
Sustituyendo los períodos:
$$n(2\pi) = m(2)$$
Despejando $\pi$:
$$\pi = \frac{m}{n}$$
Esta ecuación nos está exigiendo que $\pi$ pueda expresarse como la fracción de dos números enteros ($\frac{m}{n}$). Pero sabemos desde la antigüedad que $\pi$ es un número **irracional**, por lo que tal fracción es matemáticamente imposible de construir. 

**Conclusión:** ¡La función $p(x)$ **no es periódica**! A pesar de estar formada por la simple suma de dos ondas matemáticamente perfectas, sus frecuencias son "inconmensurables" (no encajan entre sí de forma racional). Al sumarlas, se crea un patrón de interferencia caótico que jamás vuelve a repetirse exactamente igual en toda la eternidad. A este tipo de curvas, que casi parecen repetirse pero nunca lo logran del todo, se les conoce en matemáticas avanzadas como **funciones cuasiperiódicas**, y son todo un campo de estudio propio.
### 5.5 Funciones periódicas construidas

Para expandir aún más nuestra intuición analítica, presentamos algunas construcciones algebraicas inusuales. Combinando funciones ya estudiadas (como piso, mantisa y signo) con la trigonometría, se pueden generar comportamientos periódicos que resultan perturbadores, contra-intuitivos o directamente "rotos".

**1. La onda de sierra curva:** $f(x) = \{\sin(x)\}$
Al componer la función parte fraccionaria (mantisa) con el seno, unimos dos mundos. En las crestas positivas, la función es idéntica a $\sin(x)$. Sin embargo, cuando el seno se vuelve negativo (por ejemplo, $-0.2$), su parte fraccionaria se calcula como $-0.2 - (-1) = 0.8$. El resultado son "dientes de sierra" que en lugar de estar formados por líneas rectas, tienen curvaturas suaves que se quiebran abruptamente.

**2. La onda perezosa:** $f(x) = \lfloor \sin(x) \rfloor$
Al aplicar la función piso al seno, destruimos por completo su suave oscilación. Dado que el seno está estrictamente acotado en el intervalo $[-1, 1]$, esta función vale $-1$ la mitad del tiempo y $0$ la otra mitad, logrando un minúsculo e instantáneo salto a $1$ exclusivamente en los máximos (como $\pi/2$). Es una función periódica que pasa gran parte de su vida como una simple línea horizontal a trozos.

**3. La onda invertida repentinamente:** $f(x) = \sin(x) \cdot \text{sgn}(\cos(x))$
Multiplicar por el signo del coseno tiene el efecto de invertir verticalmente la onda del seno de forma extremadamente brusca justo cuando el coseno cruza el eje X y cambia de signo (en los múltiplos impares de $\pi/2$). Visualmente genera una onda senoidal que sufre "cortocircuitos", exhibiendo discontinuidades de salto y cambios de fase violentos en pleno ciclo. Es geométricamente perturbadora.
**4. El seno impostor:** $f(x) = (-1)^{\lfloor x \rfloor} \cdot \sin(\pi x)$
La componente $\sin(\pi x)$ forma domos entre los números enteros. Por su parte, el término $(-1)^{\lfloor x \rfloor}$ actúa como un interruptor maestro que alterna entre $+1$ y $-1$ cada vez que cruzamos un número entero. Esta combinación obliga a que los domos negativos del seno se vuelvan positivos. Engaña al ojo: parece una curva suave, pero sus derivadas en los puntos enteros revelan que algo está "mal" y puntiagudo.

**5. El caos infinito en las raíces:** $f(x) = \sin\!\left(\frac{1}{\sin(x)}\right)$
Esta función está perfectamente definida en casi todos lados. Sin embargo, su comportamiento es salvaje en las raíces del seno original (los múltiplos de $\pi$). Al acercarnos a estos puntos de quiebre, el denominador se encoge, la fracción $\frac{1}{\sin(x)}$ explota hacia el infinito, y forzamos al seno exterior a oscilar infinitamente rápido. Es matemáticamente imposible de graficar con exactitud en la cercanía de estos puntos.

**6. El falso $x$ (o el zigzag infinito):** $f(x) = \arccos(\cos(x))$
El instinto inmediato de un estudiante de primer semestre es "cancelar" las funciones y asumir que el resultado es la simple función identidad $f(x) = x$ (una línea recta diagonal infinita, no periódica). ¡Gravísimo error! Debido a la restricción obligatoria del rango del arcocoseno, la identidad solo se cumple en el intervalo $[0, \pi]$. Fuera de ahí, la gráfica rebota. El resultado asombroso es una **onda triangular perfecta** formada por líneas rígidamente rectas en zigzag, que nacen de forma paradójica al componer dos de las curvas más suaves, redondas y "circulares" de la matemática. Destruye para siempre el mito algebraico de que $f^{-1}(f(x)) = x$ aplica ciegamente para todos los números reales.

---

## 6. Funciones Hiperbólicas

Pensemos en un cable eléctrico colgado entre dos postes, una cadena suspendida por sus extremos o incluso el arco de una vela tensada por el viento. A primera observación, estas curvas parecen parábolas, pero no lo son: su forma exacta está descrita por la curva catenaria que matemáticamente se representa mediante la función **coseno hiperbólico**. Del mismo modo, cuando se estudia el movimiento acelerado en la relatividad especial o ciertas ecuaciones diferenciales sencillas, aparecen combinaciones de exponenciales $e^x$ y $e^{-x}$ que resultan ser más naturales de escribir como $\sinh(x)$ y $\cosh(x)$. Estas funciones no son una mera curiosidad notacional: organizan simetrías, simplifican fórmulas y conectan el álgebra exponencial con la geometría de la hipérbola de una manera tan limpia como los senos y cosenos conectan la exponencial imaginaria con la circunferencia.

> **Nota histórica:** Aunque las combinaciones exponenciales $e^x \pm e^{-x}$ eran conocidas desde el siglo XVII, el estudio sistemático de las funciones hiperbólicas como familia independiente comenzó con **Vincenzo Riccati**, quien en 1757 publicó *Opuscula ad res physicas et mathematicas pertinentia* y acuñó los nombres *sinus hyperbolicus* y *cosinus hyperbolicus*. Poco después, **Johann Heinrich Lambert** (alrededor de 1768) profundizó en sus propiedades y estableció conexiones con la geometría de la hipérbola. Curiosamente, Lambert también fue uno de los primeros en demostrar que $\pi$ es irracional, el mismo tipo de obstáculo que encontramos cuando dos funciones trigonométricas tienen períodos inconmensurables.

### 6.1 Origen analítico: la descomposición de la exponencial

En la Sección 2.2 se introdujo el Teorema de Descomposición de Paridad, el cual establece que cualquier función real sobre un dominio simétrico puede expresarse de manera única como la suma de una función par y una función impar. Al aplicar este teorema a la función exponencial elemental $f(x) = e^x$, se obtienen de manera natural sus dos componentes de paridad:

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

PONER GRAFICA AQUI: gráficas de $y = \sinh(x)$ y $y = \cosh(x)$ en el mismo sistema de ejes, destacando el punto mínimo $(0,1)$ de $\cosh$ y el origen de coordenadas para $\sinh$.
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
  $$\text{sech}: \mathbb{R} \to (0, 1], \qquad \text{sech}(x) = \dfrac{1}{\cosh(x)} = \dfrac{2}{e^x + e^{-x}}$$

- **Cosecante hiperbólica:**
  $$\text{csch}: \mathbb{R} \setminus \{0\} \to \mathbb{R} \setminus \{0\}, \qquad \text{csch}(x) = \dfrac{1}{\sinh(x)} = \dfrac{2}{e^x - e^{-x}}$$

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

> **Observación (sobre las funciones inversas):** La definición y análisis formal de las funciones hiperbólicas inversas, como el argumento del seno hiperbólico $\text{arsinh}(x)$ o el argumento del coseno hiperbólico $\text{arcosh}(x)$, se posponen para secciones posteriores del curso, una vez establecidos de manera rigurosa los conceptos generales de inyectividad e invertibilidad de funciones reales.

> **Observación (analogía trigonométrica):** Muchas identidades hiperbólicas pueden recordarse a partir de las identidades trigonométricas circulares cambiando el signo de los términos que contienen productos de dos senos hiperbólicos. Por ejemplo, la identidad circular $\cos^2(x) + \sin^2(x) = 1$ se convierte en $\cosh^2(x) - \sinh^2(x) = 1$. No obstante, esta regla mnemotécnica no sustituye una verificación algebraica directa.

> **Observación (notación):** En la literatura en español se encuentran distintas notaciones para las funciones inversas hiperbólicas: $\text{arsinh}(x)$, $\text{argsinh}(x)$, $\text{asinh}(x)$ para el seno hiperbólico inverso, y análogamente para las demás. Todas ellas se refieren al mismo objeto matemático.

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

**Ejemplo introductorio:** Si $g(x) = x + 1$ y $f(x) = x^2$, entonces:
$$(f \circ g)(3) = f(g(3)) = f(4) = 4^2 = 16$$
Es decir, la composición transforma $3$ en $16$ al sumar primero $1$ y luego elevar al cuadrado.

### 9.1 Definición y dominio

**Definición 9.1 (Composición de funciones):**
Dadas dos funciones $f: B \to C$ y $g: A \to B$, la **composición** de $f$ con $g$, denotada $f \circ g$ (se lee "$f$ compuesta con $g$" o "$f$ círculo $g$"), es la función definida por:
$$(f \circ g)(x) = f(g(x))$$

**Notación:** Se lee de **derecha a izquierda**: primero aplicamos $g$, luego aplicamos $f$ al resultado.

**Definición 9.2 (Dominio de la composición):**
El dominio de $f \circ g$ es:
$$\text{Dom}(f \circ g) = \{x \in \text{Dom}(g) : g(x) \in \text{Dom}(f)\}$$

Es decir, debemos satisfacer **dos condiciones**:
1. $x$ debe estar en el dominio de $g$
2. El resultado $g(x)$ debe estar en el dominio de $f$

**Observación importante:** Para que $f \circ g$ esté bien definida, necesitamos que $\text{Im}(g) \cap \text{Dom}(f) \neq \emptyset$ (la imagen de $g$ debe tener intersección con el dominio de $f$).

**Ejemplo 9.1:**
Sean $f(x) = \sqrt{x}$ y $g(x) = x - 3$. Calcular $(f \circ g)(x)$ y su dominio.

**Solución:**
$$(f \circ g)(x) = f(g(x)) = f(x-3) = \sqrt{x-3}$$

**Dominio:**
- $\text{Dom}(g) = \mathbb{R}$
- $\text{Dom}(f) = [0, +\infty)$
- Necesitamos que $g(x) \in \text{Dom}(f)$, es decir, $x - 3 \geq 0$
- Por lo tanto: $x \geq 3$

$$\text{Dom}(f \circ g) = [3, +\infty)$$

**Ejemplo 9.2:**
Sean $f(x) = x^2$ y $g(x) = x + 1$. Calcular:
a) $(f \circ g)(x)$
b) $(g \circ f)(x)$

**Solución:**
a) $(f \circ g)(x) = f(g(x)) = f(x+1) = (x+1)^2 = x^2 + 2x + 1$

b) $(g \circ f)(x) = g(f(x)) = g(x^2) = x^2 + 1$

**Observación crucial:** En este ejemplo, $(f \circ g)(x) \neq (g \circ f)(x)$. Esto ilustra que la composición **no es conmutativa** en general.

**Ejemplo 9.3:**
Sean $f(x) = \frac{1}{x}$ y $g(x) = x^2 - 4$. Determinar el dominio de $(f \circ g)(x)$.

**Solución:**
$$(f \circ g)(x) = f(g(x)) = f(x^2 - 4) = \frac{1}{x^2 - 4}$$

**Dominio:**
- $\text{Dom}(g) = \mathbb{R}$
- $\text{Dom}(f) = \mathbb{R} \setminus \{0\}$
- Necesitamos $g(x) \neq 0$, es decir, $x^2 - 4 \neq 0$
- $x^2 \neq 4 \Rightarrow x \neq \pm 2$

$$\text{Dom}(f \circ g) = \mathbb{R} \setminus \{-2, 2\}$$

**Ejemplo 9.4 (Composición con dominios restringidos):**
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

**Ejemplo 9.5:**
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

**Ejemplo 9.6:**
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

**Observación:** La fórmula $(f \circ g)^{-1} = g^{-1} \circ f^{-1}$ refleja el hecho de que, al deshacer una sucesión de operaciones, se debe revertir el orden en que fueron aplicadas.

**Ejemplo 9.7:**
Sean $f(x) = e^x$ y $g(x) = x + 1$. Ambas son biyectivas de $\mathbb{R}$ en sus respectivas imágenes. La composición:
$$(f \circ g)(x) = e^{x+1}$$

es también biyectiva, y su inversa es:
$$(f \circ g)^{-1}(x) = (g^{-1} \circ f^{-1})(x) = g^{-1}(\ln(x)) = \ln(x) - 1$$

### 9.4 Descomposición de funciones

Muchas funciones complejas pueden expresarse como composición de funciones más simples. Esta técnica es fundamental en cálculo (regla de la cadena para derivadas).

**Ejemplo 9.8 (Identificar composición):**
Dada $h(x) = \sqrt{x^2 + 1}$, expresarla como $h = f \circ g$.

**Solución:**
- Sea $g(x) = x^2 + 1$ (función interior)
- Sea $f(x) = \sqrt{x}$ (función exterior)
- Entonces: $h(x) = f(g(x)) = \sqrt{x^2 + 1}$

**Ejemplo 9.9:**
Expresemos $h(x) = \frac{1}{(x+2)^2}$ como composición de tres funciones.

**Solución:**
- Sea $r(x) = x + 2$
- Sea $s(x) = x^2$
- Sea $t(x) = \frac{1}{x}$
- Entonces: $h = t \circ s \circ r$

**Verificación:**
$$(t \circ s \circ r)(x) = t(s(r(x))) = t(s(x+2)) = t((x+2)^2) = \frac{1}{(x+2)^2}$$

**Ejemplo 9.10 (Composición iterada):**
Si $f(x) = 2x$, entonces:
- $(f \circ f)(x) = f(f(x)) = f(2x) = 2(2x) = 4x = 2^2 x$
- $(f \circ f \circ f)(x) = f(f(f(x))) = 8x = 2^3 x$
- En general: $f^{(n)}(x) = 2^n x$ (composición $n$ veces)

**Notación:** $f^{(n)} = \underbrace{f \circ f \circ \cdots \circ f}_{n \text{ veces}}$

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

### 10.1 Funciones Trigonométricas Inversas

Dado que las funciones trigonométricas son periódicas (y por tanto no inyectivas), se definen restringiendo sus dominios principales.

**Definición 10.1 (Arco Seno):** Isomorfismo inverso de $\sin(x)$ restringido a $[-\frac{\pi}{2}, \frac{\pi}{2}]$.
$$y = \arcsin(x) \iff \sin(y) = x, \quad y \in [-\frac{\pi}{2}, \frac{\pi}{2}]$$

**Definición 10.2 (Arco Coseno):** Inversa de $\cos(x)$ restringido a $[0, \pi]$.
$$y = \arccos(x) \iff \cos(y) = x, \quad y \in [0, \pi]$$

**Definición 10.3 (Arco Tangente):** Inversa de $\tan(x)$ restringido a $(-\frac{\pi}{2}, \frac{\pi}{2})$.
$$y = \arctan(x) \iff \tan(y) = x, \quad y \in (-\frac{\pi}{2}, \frac{\pi}{2})$$

### 10.2 Funciones Hiperbólicas Inversas

Se pueden expresar explícitamente usando logaritmos naturales:

1. $\text{argsinh}(x) = \ln(x + \sqrt{x^2+1}), \quad \forall x \in \mathbb{R}$
2. $\text{argcosh}(x) = \ln(x + \sqrt{x^2-1}), \quad x \geq 1$
3. $\text{argtanh}(x) = \frac{1}{2}\ln\left(\frac{1+x}{1-x}\right), \quad |x|<1$

---

## 11. Cónicas y Funciones

**Concepto intuitivo:**

Las **cónicas** son curvas que se obtienen al intersectar un cono con un plano. Dependiendo del ángulo del plano, obtenemos diferentes figuras: círculo, elipse, parábola o hipérbola. Estas curvas son fundamentales en matemáticas, física (órbitas planetarias), ingeniería y arquitectura.

Las secciones cónicas se definen generalmente por ecuaciones implícitas de la forma $Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$. Estas ecuaciones generalmente **no definen funciones**, ya que para un $x$ dado pueden existir dos valores de $y$.

Para tratarlas como funciones, debemos resolver explícitamente para $y$, obteniendo dos ramas (o funciones):

### 11.1 El Círculo

**Ecuación canónica:**
$$(x - h)^2 + (y - k)^2 = r^2$$

donde $(h, k)$ es el centro y $r$ es el radio.

**Círculo centrado en el origen:**
$$x^2 + y^2 = r^2$$

**Funciones explícitas:**
Despejando $y$:
$$y^2 = r^2 - x^2$$
$$y = \pm\sqrt{r^2 - x^2}$$

- **Rama superior (semicírculo):** $f_1(x) = \sqrt{r^2 - x^2}, \quad x \in [-r, r]$
- **Rama inferior (semicírculo):** $f_2(x) = -\sqrt{r^2 - x^2}, \quad x \in [-r, r]$

**Dominio:** $x \in [-r, r]$ (debemos tener $r^2 - x^2 \geq 0$)

**Ejemplo 11.1:**
Para el círculo $x^2 + y^2 = 9$ (radio $r = 3$):
- Rama superior: $y = \sqrt{9 - x^2}$, $x \in [-3, 3]$
- Rama inferior: $y = -\sqrt{9 - x^2}$, $x \in [-3, 3]$

### 11.2 La Elipse

**Ecuación canónica:**
$$\frac{(x-h)^2}{a^2} + \frac{(y-k)^2}{b^2} = 1$$

donde:
- $(h, k)$ es el centro
- $a$ es el semieje mayor (horizontal si $a > b$)
- $b$ es el semieje menor (vertical si $a > b$)

**Elipse centrada en el origen:**
$$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$$

**Funciones explícitas:**
Despejando $y$:
$$\frac{y^2}{b^2} = 1 - \frac{x^2}{a^2}$$
$$y^2 = b^2\left(1 - \frac{x^2}{a^2}\right) = \frac{b^2(a^2 - x^2)}{a^2}$$
$$y = \pm\frac{b}{a}\sqrt{a^2 - x^2}$$

- **Rama superior:** $f_1(x) = \frac{b}{a}\sqrt{a^2 - x^2}, \quad x \in [-a, a]$
- **Rama inferior:** $f_2(x) = -\frac{b}{a}\sqrt{a^2 - x^2}, \quad x \in [-a, a]$

**Dominio:** $x \in [-a, a]$

**Ejemplo 11.2:**
Para la elipse $\frac{x^2}{16} + \frac{y^2}{9} = 1$ (con $a = 4$ y $b = 3$):
- Rama superior: $y = \frac{3}{4}\sqrt{16 - x^2}$, $x \in [-4, 4]$
- Rama inferior: $y = -\frac{3}{4}\sqrt{16 - x^2}$, $x \in [-4, 4]$

**Propiedades de la elipse:**
- Si $a = b = r$, la elipse se convierte en un círculo de radio $r$
- **Excentricidad:** $e = \frac{c}{a}$ donde $c = \sqrt{a^2 - b^2}$ (si $a > b$)
- Si $e = 0$: círculo
- Si $0 < e < 1$: elipse

### 11.3 La Parábola

**Parábola con eje vertical (abre hacia arriba o abajo):**
$$y = ax^2 + bx + c$$

Esta **sí define una función** directamente.

**Forma canónica:**
$$y - k = a(x - h)^2$$

donde $(h, k)$ es el vértice.

**Parábola con eje horizontal (abre hacia derecha o izquierda):**
$$x = ay^2 + by + c$$

Esta **no define** $y$ como función de $x$, pero define $x$ como función de $y$.

**Forma canónica:**
$$x - h = a(y - k)^2$$

**Funciones explícitas (parábola horizontal):**
Despejando $y$ de $x = a(y - k)^2 + h$:
$$(y - k)^2 = \frac{x - h}{a}$$
$$y = k \pm \sqrt{\frac{x - h}{a}}$$

- **Rama superior:** $f_1(x) = k + \sqrt{\frac{x - h}{a}}$
- **Rama inferior:** $f_2(x) = k - \sqrt{\frac{x - h}{a}}$

**Dominio:** Depende del signo de $a$:
- Si $a > 0$: $x \geq h$ (parábola abre a la derecha)
- Si $a < 0$: $x \leq h$ (parábola abre a la izquierda)

**Ejemplo 11.3:**
Para la parábola $x = y^2$ (equivalente a $y^2 = x$):
- Rama superior: $y = \sqrt{x}$, $x \geq 0$
- Rama inferior: $y = -\sqrt{x}$, $x \geq 0$

### 11.4 La Hipérbola

**Ecuación canónica (hipérbola horizontal):**
$$\frac{(x-h)^2}{a^2} - \frac{(y-k)^2}{b^2} = 1$$

**Hipérbola centrada en el origen:**
$$\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$$

**Funciones explícitas:**
Despejando $y$:
$$\frac{y^2}{b^2} = \frac{x^2}{a^2} - 1 = \frac{x^2 - a^2}{a^2}$$
$$y^2 = \frac{b^2(x^2 - a^2)}{a^2}$$
$$y = \pm\frac{b}{a}\sqrt{x^2 - a^2}$$

- **Rama superior:** $f_1(x) = \frac{b}{a}\sqrt{x^2 - a^2}$
- **Rama inferior:** $f_2(x) = -\frac{b}{a}\sqrt{x^2 - a^2}$

**Dominio:** $x \in (-\infty, -a] \cup [a, +\infty)$ (necesitamos $x^2 - a^2 \geq 0$)

**Ejemplo 11.4 (Hipérbola equilátera):**
Para $x^2 - y^2 = 1$ (con $a = b = 1$):
- Rama superior: $f_1(x) = \sqrt{x^2 - 1}$, $x \in (-\infty, -1] \cup [1, +\infty)$
- Rama inferior: $f_2(x) = -\sqrt{x^2 - 1}$, $x \in (-\infty, -1] \cup [1, +\infty)$

**Asíntotas:**
La hipérbola $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$ tiene asíntotas:
$$y = \pm\frac{b}{a}x$$

**Hipérbola vertical:**
$$\frac{y^2}{b^2} - \frac{x^2}{a^2} = 1$$

Esta define $y$ como función de $x$ directamente (sin necesidad de separar en ramas para cada valor de $x$ en el dominio central).

---

## 12. Funciones Implícitas

**Concepto intuitivo:**

Hasta ahora hemos trabajado principalmente con **funciones explícitas**, donde la variable dependiente $y$ se expresa directamente en términos de la variable independiente $x$: $y = f(x)$. Por ejemplo, $y = x^2 + 3x + 1$.

Sin embargo, muchas relaciones matemáticas se expresan de forma **implícita**, donde $x$ e $y$ están relacionadas por una ecuación pero no podemos (o no necesitamos) despejar $y$ explícitamente. Por ejemplo: $x^2 + y^2 = 25$ (un círculo).

Una **función implícita** es aquella definida por una ecuación de la forma:
$$F(x, y) = 0$$

donde $F$ es una función de dos variables.

### 12.1 Definición formal

**Definición 12.1 (Ecuación implícita):**
Una **ecuación implícita** en $x$ e $y$ es una relación de la forma:
$$F(x, y) = 0$$

donde $F: \mathbb{R}^2 \to \mathbb{R}$ es una función de dos variables.

**Observación:** No toda ecuación implícita define a $y$ como función de $x$. Para que defina una función, debe cumplirse que para cada $x$ en el dominio, existe un **único** valor de $y$ que satisface la ecuación.

**Ejemplo 12.1:**
La ecuación $x^2 + y^2 = 9$ **no define** $y$ como función de $x$ porque para cada $x \in (-3, 3)$ existen **dos** valores de $y$ que satisfacen la ecuación: $y = \pm\sqrt{9 - x^2}$.

Sin embargo, si restringimos la ecuación a $y \geq 0$, entonces sí define una función: $y = \sqrt{9 - x^2}$ (semicírculo superior).

### 12.2 El Teorema de la Función Implícita

El **Teorema de la Función Implícita** (que se estudia con rigor en cálculo multivariable) proporciona condiciones bajo las cuales una ecuación implícita $F(x, y) = 0$ define localmente a $y$ como función de $x$.

**Teorema 12.1 (Teorema de la Función Implícita - versión informal):**
Si $F(x, y) = 0$ es una ecuación donde:
1. $F$ es una función suave (diferenciable)
2. En un punto $(x_0, y_0)$ que satisface $F(x_0, y_0) = 0$
3. La derivada parcial $\frac{\partial F}{\partial y} \neq 0$ en $(x_0, y_0)$

Entonces, **localmente** (cerca de $x_0$), la ecuación define a $y$ como función de $x$: $y = f(x)$.

**Observación:** La condición $\frac{\partial F}{\partial y} \neq 0$ garantiza que podemos "despejar" $y$ en términos de $x$ cerca del punto considerado.

**Nota:** El estudio completo de este teorema, incluyendo su demostración y aplicaciones, se realiza en cursos de Cálculo Multivariable. Aquí presentamos la idea intuitiva.

### 12.3 Derivación implícita

Aunque no despejemos $y$ explícitamente, podemos calcular $\frac{dy}{dx}$ mediante **derivación implícita**: derivamos ambos lados de la ecuación $F(x, y) = 0$ respecto a $x$, tratando a $y$ como función de $x$.

**Ejemplo 12.2:**
Dada la ecuación del círculo $x^2 + y^2 = 9$, encontrar $\frac{dy}{dx}$.

**Solución:**
Derivamos ambos lados respecto a $x$:
$$\frac{d}{dx}(x^2 + y^2) = \frac{d}{dx}(9)$$
$$2x + 2y\frac{dy}{dx} = 0$$

Despejamos $\frac{dy}{dx}$:
$$2y\frac{dy}{dx} = -2x$$
$$\frac{dy}{dx} = -\frac{x}{y}, \quad y \neq 0$$

**Interpretación:** La pendiente de la tangente al círculo en el punto $(x, y)$ es $-\frac{x}{y}$.

**Ejemplo 12.3:**
Para la elipse $\frac{x^2}{16} + \frac{y^2}{9} = 1$, encontrar $\frac{dy}{dx}$.

**Solución:**
Derivamos:
$$\frac{2x}{16} + \frac{2y}{9}\frac{dy}{dx} = 0$$
$$\frac{x}{8} + \frac{2y}{9}\frac{dy}{dx} = 0$$
$$\frac{dy}{dx} = -\frac{9x}{16y}, \quad y \neq 0$$

### 12.4 Relación con las cónicas

Las **cónicas** son ejemplos perfectos de funciones implícitas. Aunque la ecuación general de una cónica:
$$Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$$

no define $y$ como función explícita de $x$ globalmente, **localmente** (en ciertos subconjuntos) sí lo hace.

**Ejemplo 12.4 (Círculo):**
$$F(x, y) = x^2 + y^2 - r^2 = 0$$

- **Rama superior:** $y = \sqrt{r^2 - x^2}$ (para $y > 0$)
- **Rama inferior:** $y = -\sqrt{r^2 - x^2}$ (para $y < 0$)

**Ejemplo 12.5 (Hipérbola):**
$$F(x, y) = x^2 - y^2 - 1 = 0$$

- **Rama superior:** $y = \sqrt{x^2 - 1}$ (para $y > 0$)
- **Rama inferior:** $y = -\sqrt{x^2 - 1}$ (para $y < 0$)

### 12.5 Ejemplos adicionales

**Ejemplo 12.6 (Ecuación de tercer grado):**
La ecuación $y^3 + y - x = 0$ define implícitamente $y$ como función de $x$.

Verificación mediante el teorema:
$$F(x, y) = y^3 + y - x$$
$$\frac{\partial F}{\partial y} = 3y^2 + 1 > 0, \quad \forall y \in \mathbb{R}$$

Como $\frac{\partial F}{\partial y} \neq 0$ siempre, el teorema garantiza que para cada $x$ existe un único $y$ tal que $F(x, y) = 0$.

**Derivada implícita:**
$$3y^2\frac{dy}{dx} + \frac{dy}{dx} - 1 = 0$$
$$\frac{dy}{dx}(3y^2 + 1) = 1$$
$$\frac{dy}{dx} = \frac{1}{3y^2 + 1}$$

**Ejemplo 12.7 (Folium de Descartes):**
La curva definida por:
$$x^3 + y^3 = 3xy$$

es un ejemplo clásico de relación implícita que no puede expresarse fácilmente de forma explícita.

**Derivada implícita:**
$$3x^2 + 3y^2\frac{dy}{dx} = 3y + 3x\frac{dy}{dx}$$
$$3y^2\frac{dy}{dx} - 3x\frac{dy}{dx} = 3y - 3x^2$$
$$\frac{dy}{dx}(y^2 - x) = y - x^2$$
$$\frac{dy}{dx} = \frac{y - x^2}{y^2 - x}, \quad y^2 \neq x$$

**Ejemplo 12.8 (Lemniscata de Bernoulli):**
$$(x^2 + y^2)^2 = 2a^2(x^2 - y^2)$$

Esta curva con forma de "8" es otro ejemplo de función implícita que no tiene forma explícita simple.

### 12.6 Importancia de las funciones implícitas

Las funciones implícitas son fundamentales en:

1. **Geometría:** Muchas curvas algebraicas (cónicas, lemniscatas, etc.) se definen naturalmente de forma implícita

2. **Física:** Leyes de conservación (energía, momento) suelen expresarse como ecuaciones implícitas

3. **Economía:** Curvas de indiferencia, isocuantas e isocostos se representan implícitamente

4. **Ingeniería:** Ecuaciones de estado, relaciones termodinámicas

5. **Cálculo avanzado:** Permite trabajar con relaciones complejas sin necesidad de despejar variables explícitamente

**Proposición 12.1 (Ventaja de la forma implícita):**
Para muchas curvas algebraicas, la forma implícita es más simple y elegante que cualquier forma explícita equivalente.

**Ejemplo:** El círculo $x^2 + y^2 = r^2$ es mucho más simple que sus dos ramas explícitas $y = \pm\sqrt{r^2 - x^2}$.

---
