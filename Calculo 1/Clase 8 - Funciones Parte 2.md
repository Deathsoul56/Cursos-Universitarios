# Clase 8 - Funciones Parte 2

En esta clase profundizaremos en el análisis de funciones, estableciendo definiciones formales para las transformaciones geométricas, la clasificación según simetría (paridad), la composición de funciones, y el estudio riguroso de la inyectividad, sobreyectividad y funciones inversas.
## 1. Transformaciones de Funciones

Las transformaciones permiten generar nuevas familias de funciones a partir de una función elemental $f(x)$.
### 1.1 Traslaciones (Desplazamientos)

**Definición 1.1 (Traslación vertical):**
Dada una función $y = f(x)$ y una constante $c > 0$:
- La gráfica de $y = f(x) + c$ es la traslación de $f$ en $c$ unidades hacia **arriba**.
- La gráfica de $y = f(x) - c$ es la traslación de $f$ en $c$ unidades hacia **abajo**.
**Ejemplo:** Si $f(x) = x^2$, entonces $y = x^2 + 3$ mueve la parábola 3 unidades hacia arriba.

**Definición 1.2 (Traslación horizontal):**
Dada una función $y = f(x)$ y una constante $a > 0$:
- La gráfica de $y = f(x - a)$ es la traslación de $f$ en $a$ unidades hacia la **derecha**.
- La gráfica de $y = f(x + a)$ es la traslación de $f$ en $a$ unidades hacia la **izquierda**.
**Ejemplo:** Si $f(x) = x^2$, entonces $y = (x - 2)^2$ mueve el vértice de la parábola 2 unidades hacia la derecha.

**Intuición:** Para recuperar el mismo valor de $y$ en $f(x-a)$, la entrada $x$ debe ser $a$ unidades mayor que en la original.
### 1.2 Escalados (Dilataciones y Contracciones)

**Definición 1.3 (Escalado vertical):**
Sea $y = c \cdot f(x)$ con $c > 0$.
- Si $c > 1$: **Dilatación vertical** (expansión) por un factor de $c$.
- Si $0 < c < 1$: **Contracción vertical** (compresión) por un factor de $c$.
**Ejemplo:** Si $f(x) = x^2$, entonces $y = 3x^2$ estira la parábola verticalmente, haciéndola lucir más "angosta" o cerrada.

**Definición 1.4 (Escalado horizontal):**
Sea $y = f(c \cdot x)$ con $c > 0$.
- Si $c > 1$: **Contracción horizontal** por un factor de $1/c$.
- Si $0 < c < 1$: **Dilatación horizontal** por un factor de $1/c$.
**Ejemplo:** Si $f(x) = x^2$, entonces $y = (\frac{1}{2}x)^2$ ensancha la parábola horizontalmente.
### 1.3 Reflexiones

**Definición 1.5 (Reflexiones):**
- **Reflexión respecto al eje X:** $y = -f(x)$. El punto $(x, y)$ se mapea a $(x, -y)$.
- **Reflexión respecto al eje Y:** $y = f(-x)$. El punto $(x, y)$ se mapea a $(-x, y)$.

**Ejemplo:** Si usamos la función $f(x) = x^3 + 4$:
- La reflexión respecto al eje X nos da $y = -(x^3 + 4) = -x^3 - 4$ (la curva entera se voltea hacia abajo).
- La reflexión respecto al eje Y nos da $y = (-x)^3 + 4 = -x^3 + 4$ (la curva se voltea de izquierda a derecha, pero mantiene su altura).

> *(Nota sobre simetrías: Algunas funciones elementales tienen propiedades visuales curiosas al reflejarse. Por ejemplo, al reflejar $f(x) = x^2$ respecto al eje Y, la gráfica se mantiene intacta ($(-x)^2 = x^2$). O en el caso de $f(x) = x^3$, su reflexión en el eje X ($-x^3$) resulta ser visualmente idéntica a su reflexión en el eje Y ($(-x)^3$). Este comportamiento lo analizaremos a fondo más adelante en la clasificación de funciones Pares e Impares).*
### 1.4 Rotación

La rotación general de una función $y=f(x)$ no necesariamente resulta en una nueva función válida (pues la gráfica podría "voltearse" sobre sí misma y violar la prueba de la línea vertical). Para rotar una gráfica un ángulo $\theta$ en sentido antihorario respecto al origen, tomamos cada punto original $(x, y)$ (donde recordamos que $y = f(x)$) y calculamos sus nuevas coordenadas transformadas $(x', y')$ utilizando el siguiente sistema de ecuaciones trigonométricas directas:

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

**Ejemplo 1.4: Rotación de $f(x) = \sin(x)$ (Violación de unicidad)**
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

**Ejemplo 1.5 (Transformación de la parábola):**
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

**Ejemplo 1.6 (Desplazamiento horizontal con factor de escala):**
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
**Conclusión:** ¡Estas dos mitades no son funciones ordinarias! Acabamos de derivar matemáticamente de la nada al famoso **Coseno Hiperbólico** ($\cosh(x)$) como la parte par de $e^x$, y al **Seno Hiperbólico** ($\sinh(x)$) como su parte impar. Así, se desvela la hermosa identidad: $e^x = \cosh(x) + \sinh(x)$. Esto se profundizara en la sección 8

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

**Observación informal:** Una función es continua en un punto si "podemos dibujar la gráfica sin levantar el lápiz".

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

### 5.1 Funciones Periódicas

**Definición 5.1 (Función Periódica):**
Una función $f$ se dice **periódica** si existe un número real $T > 0$ tal que:
$$\forall x \in \text{Dom}(f), \quad f(x + T) = f(x)$$
El menor valor positivo $T$ que satisface esta condición se denomina **periodo fundamental**.

**Ejemplos:**
- $\sin(x)$ tiene periodo $T = 2\pi$.
- $\tan(x)$ tiene periodo $T = \pi$.


---
## 6 Funciones Hiperbólicas

Las funciones hiperbólicas son análogas a las trigonométricas, pero definidas sobre la hipérbola unitaria $x^2 - y^2 = 1$ en lugar del círculo unitario. Se definen mediante combinaciones lineales de exponenciales $e^x$ y $e^{-x}$.

**Definición 5.2 (Seno y Coseno Hiperbólicos):**
$$\sinh(x) = \frac{e^x - e^{-x}}{2}, \quad \cosh(x) = \frac{e^x + e^{-x}}{2}$$

**Definición 5.3 (Tangente Hiperbólica):**
$$\tanh(x) = \frac{\sinh(x)}{\cosh(x)} = \frac{e^x - e^{-x}}{e^x + e^{-x}}$$

**Identidad Fundamental:**
$$\cosh^2(x) - \sinh^2(x) = 1$$

---

## 7. Composición de Funciones

**Concepto intuitivo:**

La **composición de funciones** es la operación de "aplicar una función y luego otra". Imaginemos un proceso en dos etapas: primero transformamos $x$ mediante una función $g$, obteniendo $g(x)$, y luego aplicamos otra función $f$ al resultado, obteniendo $f(g(x))$. Este proceso completo define una nueva función.

**Idea intuitiva:**
Pensemos en una función como una "máquina" que transforma entradas en salidas. Si tenemos dos máquinas:
- La máquina $g$ convierte $x$ en $g(x)$
- La máquina $f$ convierte $y$ en $f(y)$

La **composición** $f \circ g$ es conectar la salida de $g$ directamente como entrada de $f$.

**Ejemplo visual:** Si $g(x) = x + 1$ (sumar 1) y $f(x) = x^2$ (elevar al cuadrado), entonces:
- Entrada: $x = 3$
- Después de $g$: $g(3) = 3 + 1 = 4$
- Después de $f$: $f(4) = 4^2 = 16$
- Resultado final: $(f \circ g)(3) = 16$

### 7.1 Definición y dominio

**Definición 6.1 (Composición de funciones):**
Dadas dos funciones $f: B \to C$ y $g: A \to B$, la **composición** de $f$ con $g$, denotada $f \circ g$ (se lee "$f$ compuesta con $g$" o "$f$ círculo $g$"), es la función definida por:
$$(f \circ g)(x) = f(g(x))$$

**Notación:** Se lee de **derecha a izquierda**: primero aplicamos $g$, luego aplicamos $f$ al resultado.

**Definición 6.2 (Dominio de la composición):**
El dominio de $f \circ g$ es:
$$\text{Dom}(f \circ g) = \{x \in \text{Dom}(g) : g(x) \in \text{Dom}(f)\}$$

Es decir, debemos satisfacer **dos condiciones**:
1. $x$ debe estar en el dominio de $g$
2. El resultado $g(x)$ debe estar en el dominio de $f$

**Observación importante:** Para que $f \circ g$ esté bien definida, necesitamos que $\text{Im}(g) \cap \text{Dom}(f) \neq \emptyset$ (la imagen de $g$ debe tener intersección con el dominio de $f$).

**Ejemplo 6.1:**
Sean $f(x) = \sqrt{x}$ y $g(x) = x - 3$. Calcular $(f \circ g)(x)$ y su dominio.

**Solución:**
$$(f \circ g)(x) = f(g(x)) = f(x-3) = \sqrt{x-3}$$

**Dominio:**
- $\text{Dom}(g) = \mathbb{R}$
- $\text{Dom}(f) = [0, +\infty)$
- Necesitamos que $g(x) \in \text{Dom}(f)$, es decir, $x - 3 \geq 0$
- Por lo tanto: $x \geq 3$

$$\text{Dom}(f \circ g) = [3, +\infty)$$

**Ejemplo 6.2:**
Sean $f(x) = x^2$ y $g(x) = x + 1$. Calcular:
a) $(f \circ g)(x)$
b) $(g \circ f)(x)$

**Solución:**
a) $(f \circ g)(x) = f(g(x)) = f(x+1) = (x+1)^2 = x^2 + 2x + 1$

b) $(g \circ f)(x) = g(f(x)) = g(x^2) = x^2 + 1$

**Observación crucial:** En este ejemplo, $(f \circ g)(x) \neq (g \circ f)(x)$. Esto ilustra que la composición **no es conmutativa** en general.

**Ejemplo 6.3:**
Sean $f(x) = \frac{1}{x}$ y $g(x) = x^2 - 4$. Determinar el dominio de $(f \circ g)(x)$.

**Solución:**
$$(f \circ g)(x) = f(g(x)) = f(x^2 - 4) = \frac{1}{x^2 - 4}$$

**Dominio:**
- $\text{Dom}(g) = \mathbb{R}$
- $\text{Dom}(f) = \mathbb{R} \setminus \{0\}$
- Necesitamos $g(x) \neq 0$, es decir, $x^2 - 4 \neq 0$
- $x^2 \neq 4 \Rightarrow x \neq \pm 2$

$$\text{Dom}(f \circ g) = \mathbb{R} \setminus \{-2, 2\}$$

**Ejemplo 6.4 (Composición con dominios restringidos):**
Sean $f(x) = \sqrt{x}$ y $g(x) = \ln(x)$. Determinar el dominio de $(f \circ g)(x)$.

**Solución:**
$$(f \circ g)(x) = f(g(x)) = f(\ln(x)) = \sqrt{\ln(x)}$$

**Dominio:**
- $\text{Dom}(g) = (0, +\infty)$ (logaritmo requiere $x > 0$)
- $\text{Dom}(f) = [0, +\infty)$ (raíz cuadrada requiere argumento $\geq 0$)
- Necesitamos $\ln(x) \geq 0$, es decir, $x \geq 1$

$$\text{Dom}(f \circ g) = [1, +\infty)$$

### 6.2 Propiedades de la composición

**Proposición 6.1 (No conmutatividad):**
En general, $f \circ g \neq g \circ f$. Es decir, la composición de funciones **no es conmutativa**.

**Ejemplo 6.5:**
Si $f(x) = 2x$ y $g(x) = x + 3$:
- $(f \circ g)(x) = 2(x+3) = 2x + 6$
- $(g \circ f)(x) = 2x + 3$

Claramente, $2x + 6 \neq 2x + 3$.

**Proposición 6.2 (Asociatividad):**
La composición de funciones **es asociativa**. Si $f$, $g$ y $h$ son funciones tales que las composiciones están definidas, entonces:
$$f \circ (g \circ h) = (f \circ g) \circ h$$

**Demostración:**
Para cualquier $x$ en el dominio apropiado:
$$[f \circ (g \circ h)](x) = f[(g \circ h)(x)] = f[g(h(x))]$$
$$[(f \circ g) \circ h](x) = (f \circ g)[h(x)] = f[g(h(x))]$$

Ambas expresiones son iguales. $\square$

**Proposición 6.3 (Elemento identidad):**
La función identidad $\text{id}(x) = x$ actúa como **elemento neutro** para la composición:
$$f \circ \text{id} = \text{id} \circ f = f$$

para cualquier función $f$.

**Demostración:**
$$(f \circ \text{id})(x) = f(\text{id}(x)) = f(x)$$
$$(\text{id} \circ f)(x) = \text{id}(f(x)) = f(x)$$

Por lo tanto, ambas composiciones dan $f$. $\square$

**Proposición 6.4 (Composición con función inversa):**
Si $f: A \to B$ es biyectiva con inversa $f^{-1}: B \to A$, entonces:
$$f^{-1} \circ f = \text{id}_A \quad \text{y} \quad f \circ f^{-1} = \text{id}_B$$

Donde $\text{id}_A$ es la función identidad en $A$ y $\text{id}_B$ es la función identidad en $B$.

**Ejemplo 6.6:**
Si $f(x) = 2x + 3$, entonces $f^{-1}(x) = \frac{x-3}{2}$. Verificamos:
$$(f^{-1} \circ f)(x) = f^{-1}(2x+3) = \frac{(2x+3)-3}{2} = \frac{2x}{2} = x = \text{id}(x)$$
$$(f \circ f^{-1})(x) = f\left(\frac{x-3}{2}\right) = 2\left(\frac{x-3}{2}\right) + 3 = x - 3 + 3 = x = \text{id}(x)$$

### 6.3 Composición y clasificación de funciones

**Teorema 6.1 (Composición de funciones inyectivas):**
Si $f: B \to C$ y $g: A \to B$ son ambas inyectivas, entonces $f \circ g: A \to C$ es inyectiva.

**Demostración:**
Sean $x_1, x_2 \in A$ tales que $(f \circ g)(x_1) = (f \circ g)(x_2)$.

Entonces:
$$f(g(x_1)) = f(g(x_2))$$

Como $f$ es inyectiva:
$$g(x_1) = g(x_2)$$

Como $g$ es inyectiva:
$$x_1 = x_2$$

Por lo tanto, $f \circ g$ es inyectiva. $\square$

**Teorema 6.2 (Composición de funciones sobreyectivas):**
Si $f: B \to C$ y $g: A \to B$ son ambas sobreyectivas, entonces $f \circ g: A \to C$ es sobreyectiva.

**Demostración:**
Sea $z \in C$ arbitrario. Como $f$ es sobreyectiva, existe $y \in B$ tal que $f(y) = z$.

Como $g$ es sobreyectiva, existe $x \in A$ tal que $g(x) = y$.

Entonces:
$$(f \circ g)(x) = f(g(x)) = f(y) = z$$

Por lo tanto, para todo $z \in C$ existe $x \in A$ tal que $(f \circ g)(x) = z$, lo que demuestra que $f \circ g$ es sobreyectiva. $\square$

**Corolario 6.1 (Composición de funciones biyectivas):**
Si $f: B \to C$ y $g: A \to B$ son ambas biyectivas, entonces $f \circ g: A \to C$ es biyectiva.

Además, la inversa de la composición satisface:
$$(f \circ g)^{-1} = g^{-1} \circ f^{-1}$$

**Observación:** El orden se invierte en la inversa: "los calcetines se ponen antes que los zapatos, pero se quitan en orden inverso".

**Ejemplo 6.7:**
Sean $f(x) = e^x$ y $g(x) = x + 1$. Ambas son biyectivas de $\mathbb{R}$ en sus respectivas imágenes. La composición:
$$(f \circ g)(x) = e^{x+1}$$

es también biyectiva, y su inversa es:
$$(f \circ g)^{-1}(x) = (g^{-1} \circ f^{-1})(x) = g^{-1}(\ln(x)) = \ln(x) - 1$$

### 6.4 Descomposición de funciones

Muchas funciones complejas pueden expresarse como composición de funciones más simples. Esta técnica es fundamental en cálculo (regla de la cadena para derivadas).

**Ejemplo 6.8 (Identificar composición):**
Dada $h(x) = \sqrt{x^2 + 1}$, expresarla como $h = f \circ g$.

**Solución:**
- Sea $g(x) = x^2 + 1$ (función interior)
- Sea $f(x) = \sqrt{x}$ (función exterior)
- Entonces: $h(x) = f(g(x)) = \sqrt{x^2 + 1}$

**Ejemplo 6.9:**
Expresemos $h(x) = \frac{1}{(x+2)^2}$ como composición de tres funciones.

**Solución:**
- Sea $r(x) = x + 2$
- Sea $s(x) = x^2$
- Sea $t(x) = \frac{1}{x}$
- Entonces: $h = t \circ s \circ r$

**Verificación:**
$$(t \circ s \circ r)(x) = t(s(r(x))) = t(s(x+2)) = t((x+2)^2) = \frac{1}{(x+2)^2}$$

**Ejemplo 6.10 (Composición iterada):**
Si $f(x) = 2x$, entonces:
- $(f \circ f)(x) = f(f(x)) = f(2x) = 2(2x) = 4x = 2^2 x$
- $(f \circ f \circ f)(x) = f(f(f(x))) = 8x = 2^3 x$
- En general: $f^{(n)}(x) = 2^n x$ (composición $n$ veces)

**Notación:** $f^{(n)} = \underbrace{f \circ f \circ \cdots \circ f}_{n \text{ veces}}$

---

## 7. Clasificación de Funciones

Sea $f: A \to B$ una función. Clasificamos las funciones según cómo relacionan los elementos del dominio $A$ con el codominio $B$.

### 7.1 Inyectividad (Uno a Uno)

**Definición 7.1 (Función Inyectiva):**
Una función $f$ es **inyectiva** (o inyección) si asigna imágenes distintas a elementos distintos del dominio. Formalmente:
$$\forall x_1, x_2 \in A, \quad f(x_1) = f(x_2) \implies x_1 = x_2$$
Equivalentemente (contrapositiva): $x_1 \neq x_2 \implies f(x_1) \neq f(x_2)$.

**Prueba de la línea horizontal:** Una función es inyectiva si ninguna recta horizontal intersecta su gráfica en más de un punto.

### 7.2 Sobreyectividad (Epiyecctiva o Sobre)

**Definición 7.2 (Función Sobreyectiva):**
Una función $f$ es **sobreyectiva** (o suryección) si todo elemento del codominio es imagen de al menos un elemento del dominio. Es decir, la imagen coincide con el codominio ($Im(f) = B$). Formalmente:
$$\forall y \in B, \quad \exists x \in A \text{ tal que } f(x) = y$$

### 7.3 Biyectividad

**Definición 7.3 (Función Biyectiva):**
Una función es **biyectiva** si es simultáneamente **inyectiva** y **sobreyectiva**.
Esto implica una correspondencia **biunívoca** (uno a uno y sobre) entre los conjuntos $A$ y $B$.

---

## 8. Funciones Inversas

**Concepto intuitivo:**

La función inversa "deshace" o "revierte" la acción de una función. Si una función $f$ transforma $x$ en $y$, la función inversa $f^{-1}$ transforma $y$ de regreso en $x$.

**Idea intuitiva:** Si $f$ es como "poner calcetines", entonces $f^{-1}$ es "quitarse los calcetines". Una operación cancela a la otra.

El concepto de inversa permite "deshacer" la acción de una función.

### 8.1 Definición y Existencia

**Teorema 8.1 (Existencia de la inversa):**
Una función $f: A \to B$ tiene función inversa si y solo si $f$ es **biyectiva**.

**Justificación:**
- **Inyectividad** garantiza que cada valor de salida proviene de una única entrada (no hay ambigüedad)
- **Sobreyectividad** garantiza que todo elemento del codominio tiene una preimagen (la inversa está definida en todo $B$)

**Definición 8.1 (Función Inversa):**
Si $f: A \to B$ es biyectiva, definimos su función inversa $f^{-1}: B \to A$ como:
$$f^{-1}(y) = x \iff f(x) = y$$

**Propiedades de la composición:**
1. $(f^{-1} \circ f)(x) = f^{-1}(f(x)) = x, \quad \forall x \in A$
2. $(f \circ f^{-1})(y) = f(f^{-1}(y)) = y, \quad \forall y \in B$

Estas propiedades expresan que $f$ y $f^{-1}$ son inversas mutuas.

**Propiedad Gráfica:**
Las gráficas de $y=f(x)$ y $y=f^{-1}(x)$ son simétricas respecto a la recta identidad $y=x$.

**Observación importante:** La notación $f^{-1}$ para la función inversa **no debe confundirse** con $[f(x)]^{-1} = \frac{1}{f(x)}$, que es el recíproco.

### 8.2 Método algebraico para calcular la inversa

**Procedimiento general:**

Para encontrar la función inversa $f^{-1}$ de una función biyectiva $f$:

**Paso 1:** Escribir $y = f(x)$

**Paso 2:** Despejar $x$ en términos de $y$, obteniendo $x = g(y)$

**Paso 3:** La función $f^{-1}(y) = g(y)$ es la inversa. Por convención, reemplazamos la variable $y$ por $x$ para escribir $f^{-1}(x)$

**Paso 4:** Verificar que $(f \circ f^{-1})(x) = x$ y $(f^{-1} \circ f)(x) = x$

**Ejemplo 8.1 (Función lineal):**
Encontrar la inversa de $f(x) = 2x + 3$.

**Solución:**

**Paso 1:** $y = 2x + 3$

**Paso 2:** Despejamos $x$:
$$y = 2x + 3$$
$$y - 3 = 2x$$
$$x = \frac{y - 3}{2}$$

**Paso 3:** Por lo tanto:
$$f^{-1}(x) = \frac{x - 3}{2}$$

**Paso 4 (Verificación):**
$$(f \circ f^{-1})(x) = f\left(\frac{x-3}{2}\right) = 2\left(\frac{x-3}{2}\right) + 3 = x - 3 + 3 = x$$ ✓
$$(f^{-1} \circ f)(x) = f^{-1}(2x+3) = \frac{(2x+3)-3}{2} = \frac{2x}{2} = x$$ ✓

**Ejemplo 8.2 (Función racional):**
Encontrar la inversa de $f(x) = \frac{3x + 1}{x - 2}$.

**Solución:**

**Paso 1:** $y = \frac{3x + 1}{x - 2}$

**Paso 2:** Despejamos $x$:
$$y(x - 2) = 3x + 1$$
$$yx - 2y = 3x + 1$$
$$yx - 3x = 2y + 1$$
$$x(y - 3) = 2y + 1$$
$$x = \frac{2y + 1}{y - 3}$$

**Paso 3:**
$$f^{-1}(x) = \frac{2x + 1}{x - 3}$$

**Observación:** Esta función es **autoinversa** salvo constantes: tiene la misma forma que la original.

**Ejemplo 8.3 (Función exponencial):**
Encontrar la inversa de $f(x) = e^{x+2} - 1$.

**Solución:**

**Paso 1:** $y = e^{x+2} - 1$

**Paso 2:** Despejamos $x$:
$$y + 1 = e^{x+2}$$
$$\ln(y + 1) = x + 2$$
$$x = \ln(y + 1) - 2$$

**Paso 3:**
$$f^{-1}(x) = \ln(x + 1) - 2$$

**Dominio de $f^{-1}$:** Como $e^{x+2} > 0$, tenemos $y > -1$. Por lo tanto, $\text{Dom}(f^{-1}) = (-1, +\infty)$.

**Ejemplo 8.4 (Función cúbica):**
Encontrar la inversa de $f(x) = x^3 + 1$.

**Solución:**

**Paso 1:** $y = x^3 + 1$

**Paso 2:**
$$y - 1 = x^3$$
$$x = \sqrt[3]{y - 1}$$

**Paso 3:**
$$f^{-1}(x) = \sqrt[3]{x - 1}$$

**Observación:** Las funciones polinómicas de grado impar son biyectivas de $\mathbb{R}$ en $\mathbb{R}$, por lo que siempre tienen inversa global.

### 8.3 Restricción del Dominio

Si una función no es inyectiva en su dominio natural (ej. $f(x) = x^2$), no posee inversa global. Sin embargo, podemos definir una **inversa parcial** restringiendo su dominio a un subconjunto donde sea inyectiva.

**Ejemplo 8.5 (Función cuadrática restringida):**
La función $f(x) = x^2$ no es inyectiva en $\mathbb{R}$ (por ejemplo, $f(-2) = f(2) = 4$).

Si restringimos a $f: [0, +\infty) \to [0, +\infty)$, entonces $f$ es biyectiva.

**Cálculo de la inversa:**

**Paso 1:** $y = x^2$ con $x \geq 0$

**Paso 2:** $x = \sqrt{y}$ (tomamos raíz positiva porque $x \geq 0$)

**Paso 3:** $f^{-1}(x) = \sqrt{x}$ con $\text{Dom}(f^{-1}) = [0, +\infty)$

**Observación:** Si hubiéramos restringido a $f: (-\infty, 0] \to [0, +\infty)$, la inversa sería $f^{-1}(x) = -\sqrt{x}$.

**Ejemplo 8.6 (Función cuadrática general):**
Encontrar la inversa de $f(x) = x^2 - 4x + 5$ restringida a $[2, +\infty)$.

**Solución:**

Primero, completamos el cuadrado:
$$f(x) = (x-2)^2 + 1$$

En $[2, +\infty)$, la función es inyectiva y su imagen es $[1, +\infty)$.

**Paso 1:** $y = (x-2)^2 + 1$ con $x \geq 2$

**Paso 2:**
$$y - 1 = (x-2)^2$$
$$\sqrt{y - 1} = x - 2$$ (raíz positiva porque $x \geq 2$)
$$x = 2 + \sqrt{y - 1}$$

**Paso 3:**
$$f^{-1}(x) = 2 + \sqrt{x - 1}, \quad x \geq 1$$

### 8.4 Propiedades de la función inversa

**Proposición 8.1 (Dominio e imagen):**
Si $f: A \to B$ es biyectiva, entonces:
- $\text{Dom}(f^{-1}) = \text{Im}(f)$
- $\text{Im}(f^{-1}) = \text{Dom}(f) = A$

**Proposición 8.2 (Inversa de la inversa):**
Si $f$ es biyectiva, entonces:
$$(f^{-1})^{-1} = f$$

**Proposición 8.3 (Monotonía):**
Si $f$ es estrictamente creciente y biyectiva, entonces $f^{-1}$ también es estrictamente creciente.

Si $f$ es estrictamente decreciente y biyectiva, entonces $f^{-1}$ también es estrictamente decreciente.

**Ejemplo 8.7:**
La función $f(x) = 2x + 3$ es estrictamente creciente. Su inversa $f^{-1}(x) = \frac{x-3}{2}$ también es estrictamente creciente.

---

## 9. Inversas de Funciones Trascendentes

### 9.1 Funciones Trigonométricas Inversas

Dado que las funciones trigonométricas son periódicas (y por tanto no inyectivas), se definen restringiendo sus dominios principales.

**Definición 9.1 (Arco Seno):** Isomorfismo inverso de $\sin(x)$ restringido a $[-\frac{\pi}{2}, \frac{\pi}{2}]$.
$$y = \arcsin(x) \iff \sin(y) = x, \quad y \in [-\frac{\pi}{2}, \frac{\pi}{2}]$$

**Definición 9.2 (Arco Coseno):** Inversa de $\cos(x)$ restringido a $[0, \pi]$.
$$y = \arccos(x) \iff \cos(y) = x, \quad y \in [0, \pi]$$

**Definición 9.3 (Arco Tangente):** Inversa de $\tan(x)$ restringido a $(-\frac{\pi}{2}, \frac{\pi}{2})$.
$$y = \arctan(x) \iff \tan(y) = x, \quad y \in (-\frac{\pi}{2}, \frac{\pi}{2})$$

### 9.2 Funciones Hiperbólicas Inversas

Se pueden expresar explícitamente usando logaritmos naturales:

1. $\text{argsinh}(x) = \ln(x + \sqrt{x^2+1}), \quad \forall x \in \mathbb{R}$
2. $\text{argcosh}(x) = \ln(x + \sqrt{x^2-1}), \quad x \geq 1$
3. $\text{argtanh}(x) = \frac{1}{2}\ln\left(\frac{1+x}{1-x}\right), \quad |x|<1$

---

## 10. Cónicas y Funciones

**Concepto intuitivo:**

Las **cónicas** son curvas que se obtienen al intersectar un cono con un plano. Dependiendo del ángulo del plano, obtenemos diferentes figuras: círculo, elipse, parábola o hipérbola. Estas curvas son fundamentales en matemáticas, física (órbitas planetarias), ingeniería y arquitectura.

Las secciones cónicas se definen generalmente por ecuaciones implícitas de la forma $Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$. Estas ecuaciones generalmente **no definen funciones**, ya que para un $x$ dado pueden existir dos valores de $y$.

Para tratarlas como funciones, debemos resolver explícitamente para $y$, obteniendo dos ramas (o funciones):

### 10.1 El Círculo

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

**Ejemplo 10.1:**
Para el círculo $x^2 + y^2 = 9$ (radio $r = 3$):
- Rama superior: $y = \sqrt{9 - x^2}$, $x \in [-3, 3]$
- Rama inferior: $y = -\sqrt{9 - x^2}$, $x \in [-3, 3]$

### 10.2 La Elipse

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

**Ejemplo 10.2:**
Para la elipse $\frac{x^2}{16} + \frac{y^2}{9} = 1$ (con $a = 4$ y $b = 3$):
- Rama superior: $y = \frac{3}{4}\sqrt{16 - x^2}$, $x \in [-4, 4]$
- Rama inferior: $y = -\frac{3}{4}\sqrt{16 - x^2}$, $x \in [-4, 4]$

**Propiedades de la elipse:**
- Si $a = b = r$, la elipse se convierte en un círculo de radio $r$
- **Excentricidad:** $e = \frac{c}{a}$ donde $c = \sqrt{a^2 - b^2}$ (si $a > b$)
- Si $e = 0$: círculo
- Si $0 < e < 1$: elipse

### 10.3 La Parábola

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

**Ejemplo 10.3:**
Para la parábola $x = y^2$ (equivalente a $y^2 = x$):
- Rama superior: $y = \sqrt{x}$, $x \geq 0$
- Rama inferior: $y = -\sqrt{x}$, $x \geq 0$

### 10.4 La Hipérbola

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

**Ejemplo 10.4 (Hipérbola equilátera):**
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

## 11. Funciones Implícitas

**Concepto intuitivo:**

Hasta ahora hemos trabajado principalmente con **funciones explícitas**, donde la variable dependiente $y$ se expresa directamente en términos de la variable independiente $x$: $y = f(x)$. Por ejemplo, $y = x^2 + 3x + 1$.

Sin embargo, muchas relaciones matemáticas se expresan de forma **implícita**, donde $x$ e $y$ están relacionadas por una ecuación pero no podemos (o no necesitamos) despejar $y$ explícitamente. Por ejemplo: $x^2 + y^2 = 25$ (un círculo).

Una **función implícita** es aquella definida por una ecuación de la forma:
$$F(x, y) = 0$$

donde $F$ es una función de dos variables.

### 11.1 Definición formal

**Definición 11.1 (Ecuación implícita):**
Una **ecuación implícita** en $x$ e $y$ es una relación de la forma:
$$F(x, y) = 0$$

donde $F: \mathbb{R}^2 \to \mathbb{R}$ es una función de dos variables.

**Observación:** No toda ecuación implícita define a $y$ como función de $x$. Para que defina una función, debe cumplirse que para cada $x$ en el dominio, existe un **único** valor de $y$ que satisface la ecuación.

**Ejemplo 11.1:**
La ecuación $x^2 + y^2 = 9$ **no define** $y$ como función de $x$ porque para cada $x \in (-3, 3)$ existen **dos** valores de $y$ que satisfacen la ecuación: $y = \pm\sqrt{9 - x^2}$.

Sin embargo, si restringimos la ecuación a $y \geq 0$, entonces sí define una función: $y = \sqrt{9 - x^2}$ (semicírculo superior).

### 11.2 El Teorema de la Función Implícita

El **Teorema de la Función Implícita** (que se estudia con rigor en cálculo multivariable) proporciona condiciones bajo las cuales una ecuación implícita $F(x, y) = 0$ define localmente a $y$ como función de $x$.

**Teorema 11.1 (Teorema de la Función Implícita - versión informal):**
Si $F(x, y) = 0$ es una ecuación donde:
1. $F$ es una función suave (diferenciable)
2. En un punto $(x_0, y_0)$ que satisface $F(x_0, y_0) = 0$
3. La derivada parcial $\frac{\partial F}{\partial y} \neq 0$ en $(x_0, y_0)$

Entonces, **localmente** (cerca de $x_0$), la ecuación define a $y$ como función de $x$: $y = f(x)$.

**Observación:** La condición $\frac{\partial F}{\partial y} \neq 0$ garantiza que podemos "despejar" $y$ en términos de $x$ cerca del punto considerado.

**Nota:** El estudio completo de este teorema, incluyendo su demostración y aplicaciones, se realiza en cursos de Cálculo Multivariable. Aquí presentamos la idea intuitiva.

### 11.3 Derivación implícita

Aunque no despejemos $y$ explícitamente, podemos calcular $\frac{dy}{dx}$ mediante **derivación implícita**: derivamos ambos lados de la ecuación $F(x, y) = 0$ respecto a $x$, tratando a $y$ como función de $x$.

**Ejemplo 11.2:**
Dada la ecuación del círculo $x^2 + y^2 = 9$, encontrar $\frac{dy}{dx}$.

**Solución:**
Derivamos ambos lados respecto a $x$:
$$\frac{d}{dx}(x^2 + y^2) = \frac{d}{dx}(9)$$
$$2x + 2y\frac{dy}{dx} = 0$$

Despejamos $\frac{dy}{dx}$:
$$2y\frac{dy}{dx} = -2x$$
$$\frac{dy}{dx} = -\frac{x}{y}, \quad y \neq 0$$

**Interpretación:** La pendiente de la tangente al círculo en el punto $(x, y)$ es $-\frac{x}{y}$.

**Ejemplo 11.3:**
Para la elipse $\frac{x^2}{16} + \frac{y^2}{9} = 1$, encontrar $\frac{dy}{dx}$.

**Solución:**
Derivamos:
$$\frac{2x}{16} + \frac{2y}{9}\frac{dy}{dx} = 0$$
$$\frac{x}{8} + \frac{2y}{9}\frac{dy}{dx} = 0$$
$$\frac{dy}{dx} = -\frac{9x}{16y}, \quad y \neq 0$$

### 11.4 Relación con las cónicas

Las **cónicas** son ejemplos perfectos de funciones implícitas. Aunque la ecuación general de una cónica:
$$Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$$

no define $y$ como función explícita de $x$ globalmente, **localmente** (en ciertos subconjuntos) sí lo hace.

**Ejemplo 11.4 (Círculo):**
$$F(x, y) = x^2 + y^2 - r^2 = 0$$

- **Rama superior:** $y = \sqrt{r^2 - x^2}$ (para $y > 0$)
- **Rama inferior:** $y = -\sqrt{r^2 - x^2}$ (para $y < 0$)

**Ejemplo 11.5 (Hipérbola):**
$$F(x, y) = x^2 - y^2 - 1 = 0$$

- **Rama superior:** $y = \sqrt{x^2 - 1}$ (para $y > 0$)
- **Rama inferior:** $y = -\sqrt{x^2 - 1}$ (para $y < 0$)

### 11.5 Ejemplos adicionales

**Ejemplo 11.6 (Ecuación de tercer grado):**
La ecuación $y^3 + y - x = 0$ define implícitamente $y$ como función de $x$.

Verificación mediante el teorema:
$$F(x, y) = y^3 + y - x$$
$$\frac{\partial F}{\partial y} = 3y^2 + 1 > 0, \quad \forall y \in \mathbb{R}$$

Como $\frac{\partial F}{\partial y} \neq 0$ siempre, el teorema garantiza que para cada $x$ existe un único $y$ tal que $F(x, y) = 0$.

**Derivada implícita:**
$$3y^2\frac{dy}{dx} + \frac{dy}{dx} - 1 = 0$$
$$\frac{dy}{dx}(3y^2 + 1) = 1$$
$$\frac{dy}{dx} = \frac{1}{3y^2 + 1}$$

**Ejemplo 11.7 (Folium de Descartes):**
La curva definida por:
$$x^3 + y^3 = 3xy$$

es un ejemplo clásico de relación implícita que no puede expresarse fácilmente de forma explícita.

**Derivada implícita:**
$$3x^2 + 3y^2\frac{dy}{dx} = 3y + 3x\frac{dy}{dx}$$
$$3y^2\frac{dy}{dx} - 3x\frac{dy}{dx} = 3y - 3x^2$$
$$\frac{dy}{dx}(y^2 - x) = y - x^2$$
$$\frac{dy}{dx} = \frac{y - x^2}{y^2 - x}, \quad y^2 \neq x$$

**Ejemplo 11.8 (Lemniscata de Bernoulli):**
$$(x^2 + y^2)^2 = 2a^2(x^2 - y^2)$$

Esta curva con forma de "8" es otro ejemplo de función implícita que no tiene forma explícita simple.

### 11.6 Importancia de las funciones implícitas

Las funciones implícitas son fundamentales en:

1. **Geometría:** Muchas curvas algebraicas (cónicas, lemniscatas, etc.) se definen naturalmente de forma implícita

2. **Física:** Leyes de conservación (energía, momento) suelen expresarse como ecuaciones implícitas

3. **Economía:** Curvas de indiferencia, isocuantas e isocostos se representan implícitamente

4. **Ingeniería:** Ecuaciones de estado, relaciones termodinámicas

5. **Cálculo avanzado:** Permite trabajar con relaciones complejas sin necesidad de despejar variables explícitamente

**Proposición 11.1 (Ventaja de la forma implícita):**
Para muchas curvas algebraicas, la forma implícita es más simple y elegante que cualquier forma explícita equivalente.

**Ejemplo:** El círculo $x^2 + y^2 = r^2$ es mucho más simple que sus dos ramas explícitas $y = \pm\sqrt{r^2 - x^2}$.

---
