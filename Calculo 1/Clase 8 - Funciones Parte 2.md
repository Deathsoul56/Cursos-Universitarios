# Clase 8 - Funciones Parte 2

En esta clase profundizaremos en el análisis funcional, estableciendo definiciones formales para las transformaciones geométricas, la clasificación según simetría (paridad), la composición de funciones, y el estudio riguroso de la inyectividad, sobreyectividad y funciones inversas.

## 1. Transformaciones de Funciones

Las transformaciones permiten generar nuevas familias de funciones a partir de una función elemental $f(x)$.

### 1.1 Traslaciones (Desplazamientos)

**Definición 1.1 (Traslación vertical):**
Dada una función $y = f(x)$ y una constante $c > 0$:
- La gráfica de $y = f(x) + c$ es la traslación de $f$ en $c$ unidades hacia **arriba**.
- La gráfica de $y = f(x) - c$ es la traslación de $f$ en $c$ unidades hacia **abajo**.

**Definición 1.2 (Traslación horizontal):**
Dada una función $y = f(x)$ y una constante $a > 0$:
- La gráfica de $y = f(x - a)$ es la traslación de $f$ en $a$ unidades hacia la **derecha**.
- La gráfica de $y = f(x + a)$ es la traslación de $f$ en $a$ unidades hacia la **izquierda**.

**Intuición:** Para recuperar el mismo valor de $y$ en $f(x-a)$, la entrada $x$ debe ser $a$ unidades mayor que en la original.

### 1.2 Escalados (Dilataciones y Contracciones)

**Definición 1.3 (Escalado vertical):**
Sea $y = c \cdot f(x)$ con $c > 0$.
- Si $c > 1$: **Dilatación vertical** (expansión) por un factor de $c$.
- Si $0 < c < 1$: **Contracción vertical** (compresión) por un factor de $c$.

**Definición 1.4 (Escalado horizontal):**
Sea $y = f(c \cdot x)$ con $c > 0$.
- Si $c > 1$: **Contracción horizontal** por un factor de $1/c$.
- Si $0 < c < 1$: **Dilatación horizontal** por un factor de $1/c$.

### 1.3 Reflexiones

**Definición 1.5 (Reflexiones):**
- **Reflexión respecto al eje X:** $y = -f(x)$. El punto $(x, y)$ se mapea a $(x, -y)$.
- **Reflexión respecto al eje Y:** $y = f(-x)$. El punto $(x, y)$ se mapea a $(-x, y)$.

### 1.4 Rotación (Nota formal)

La rotación general de una función $y=f(x)$ no necesariamente resulta en una función (puede violar la unicidad de imagen). La transformación de coordenadas para una rotación de ángulo $\theta$ está dada por la matriz de rotación:
$$
\begin{pmatrix} x' \\ y' \end{pmatrix} = \begin{pmatrix} \cos \theta & -\sin \theta \\ \sin \theta & \cos \theta \end{pmatrix} \begin{pmatrix} x \\ f(x) \end{pmatrix}
$$

---

## 2. Simetría de Funciones (Paridad)

Sea $f: D \to \mathbb{R}$ una función con dominio $D$ simétrico respecto al origen (si $x \in D \Rightarrow -x \in D$).

### 2.1 Funciones Pares e Impares

**Definición 2.1 (Función Par):**
Una función $f$ es **par** si:
$$\forall x \in D, \quad f(-x) = f(x)$$
**Propiedad Geométrica:** Su gráfica es simétrica respecto al **eje Y**.
**Ejemplos:** $f(x) = x^2, \quad f(x) = |x|, \quad f(x) = \cos(x)$.

**Definición 2.2 (Función Impar):**
Una función $f$ es **impar** si:
$$\forall x \in D, \quad f(-x) = -f(x)$$
**Propiedad Geométrica:** Su gráfica es simétrica respecto al **origen** $(0,0)$.
**Ejemplos:** $f(x) = x^3, \quad f(x) = 1/x, \quad f(x) = \sin(x)$.

**Teorema 2.1 (Descomposición de funciones):**
Toda función $f: \mathbb{R} \to \mathbb{R}$ puede expresarse de manera única como la suma de una función par y una función impar:
$$f(x) = f_{par}(x) + f_{impar}(x)$$
Donde:
$$f_{par}(x) = \frac{f(x) + f(-x)}{2}, \quad f_{impar}(x) = \frac{f(x) - f(-x)}{2}$$

---

## 3. Funciones Definidas a Tramos

**Concepto intuitivo:**

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

**Concepto intuitivo:**

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

## 4. Funciones Especiales

### 4.1 Función Piso y Cielo (Parte Entera)

**Definición 4.1 (Función Piso / Floor):**
La función piso, denotada $\lfloor x \rfloor$ o $\text{floor}(x)$, asigna a cada número real $x$ el mayor entero menor o igual a $x$.
$$\lfloor x \rfloor = \max \{k \in \mathbb{Z} : k \leq x\}$$
- **Propiedad:** $\lfloor x \rfloor \leq x < \lfloor x \rfloor + 1$

**Definición 4.2 (Función Cielo / Ceiling):**
La función cielo, denotada $\lceil x \rceil$ o $\text{ceil}(x)$, asigna el menor entero mayor o igual a $x$.
$$\lceil x \rceil = \min \{k \in \mathbb{Z} : k \geq x\}$$

### 4.2 Función Signo y Heaviside

**Definición 4.3 (Función Signo):**
$$\text{sgn}(x) = \begin{cases} -1 & \text{si } x < 0 \\ 0 & \text{si } x = 0 \\ 1 & \text{si } x > 0 \end{cases}$$

**Definición 4.4 (Función de Heaviside o Escalón Unitario):**
Fundamental en ingeniería de control y señales.
$$H(x) = \begin{cases} 0 & \text{si } x < 0 \\ 1 & \text{si } x \geq 0 \end{cases}$$
*(Nota: A veces se define $H(0)=0.5$ o indefinido, según el contexto).*

### 4.3 Función Logística (Sigmoide)
$$f(x) = \frac{L}{1 + e^{-k(x-x_0)}}$$
Donde:
- $L$: Supremo de la función (asíntota horizontal superior).
- $k$: Tasa de crecimiento.
- $x_0$: Punto medio de la sigmoide.

---

## 5. Periodicidad y Funciones Hiperbólicas

### 5.1 Funciones Periódicas

**Definición 5.1 (Función Periódica):**
Una función $f$ se dice **periódica** si existe un número real $T > 0$ tal que:
$$\forall x \in \text{Dom}(f), \quad f(x + T) = f(x)$$
El menor valor positivo $T$ que satisface esta condición se denomina **periodo fundamental**.

**Ejemplos:**
- $\sin(x)$ tiene periodo $T = 2\pi$.
- $\tan(x)$ tiene periodo $T = \pi$.

### 5.2 Funciones Hiperbólicas

Las funciones hiperbólicas son análogas a las trigonométricas, pero definidas sobre la hipérbola unitaria $x^2 - y^2 = 1$ en lugar del círculo unitario. Se definen mediante combinaciones lineales de exponenciales $e^x$ y $e^{-x}$.

**Definición 5.2 (Seno y Coseno Hiperbólicos):**
$$\sinh(x) = \frac{e^x - e^{-x}}{2}, \quad \cosh(x) = \frac{e^x + e^{-x}}{2}$$

**Definición 5.3 (Tangente Hiperbólica):**
$$\tanh(x) = \frac{\sinh(x)}{\cosh(x)} = \frac{e^x - e^{-x}}{e^x + e^{-x}}$$

**Identidad Fundamental:**
$$\cosh^2(x) - \sinh^2(x) = 1$$

---

## 6. Composición de Funciones

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

### 6.1 Definición y dominio

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
