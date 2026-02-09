# Clase 8: Sucesiones Numéricas

El estudio de las sucesiones sienta las bases operativas para el cálculo avanzado, permitiendo la definición formal de límites, derivadas e integrales, así como la construcción del conjunto de los números reales.

---

## 1. Definición Formal

**Definición 1.1 (Sucesión Real):**
Una sucesión de números reales es una función $f: \mathbb{N} \to \mathbb{R}$ que asigna a cada número natural $n$ un único número real $a_n$.
Usualmente se denota como $\{a_n\}_{n \in \mathbb{N}}$ o $\{a_n\}_{n=1}^{\infty}$ o simplemente $(a_n)$, donde $a_n = f(n)$ es el **término general** o **enésimo término**.

**Ejemplo:**
Sea $a_n = \frac{1}{n}$. Los primeros términos son $1, \frac{1}{2}, \frac{1}{3}, \dots$

**Observación sobre el Conjunto de Índices:**
Aunque formalmente el dominio es $\mathbb{N}$, existe variabilidad en la literatura respecto a si el conteo inicia en $1$ o en $0$.
Consideremos la sucesión generada por $a_n = 2^n$:
- Si $n$ inicia en $0$ ($n \in \mathbb{N} \cup \{0\}$): la sucesión es $1, 2, 4, 8, \dots$
- Si $n$ inicia en $1$ ($n \in \mathbb{N} \setminus \{0\}$): la sucesión es $2, 4, 8, 16, \dots$

**Convención del Curso:**
Salvo indicación expresa en contrario, adoptaremos la convención usual del Análisis Matemático donde $\mathbb{N} = \{1, 2, 3, \dots\}$. Por tanto, **las sucesiones comenzarán en $n=1$** y en ocasiones se harán nota para mostrar las diferencias con $n=0$.
(Nota: En contextos de informática o series de potencias, es común iniciar en $n=0$).

## 2. Propiedades de Orden y Acotación

Para comprender el comportamiento de una sucesión, analizamos sus cotas y tendencias.
### 2.1 Acotación

**Definición 2.1 (Cotas en Conjuntos):**
Sea $S \subseteq \mathbb{R}$ un conjunto de números reales.
- **Cota Inferior:** Un número $k$ es cota inferior de $S$ si $\forall x \in S, x \geq k$.
- **Cota Superior:** Un número $K$ es cota superior de $S$ si $\forall x \in S, x \leq K$.

**Ejemplos:**
1.  Sea el conjunto de los números pares positivos $P = \{2, 4, 6, \dots\}$.
    - El número $2$ es una cota inferior (también lo son $1, 0, -10$, etc.).
    - No posee cota superior.
2.  Sea el intervalo $A = (0, 1]$.
    - El número $1$ es una cota superior.
    - El número $0$ es una cota inferior.

Las cotas pueden o no pertenecer al propio conjunto, no tiene una restricción para esto

**Definición 2.2 (Sucesión Acotada):**
Una sucesión $(a_n)$ está **acotada** si el conjunto de sus términos está acotado. Formalmente, si existe un número real $M > 0$ tal que:
$$|a_n| \leq M, \quad \forall n \in \mathbb{N}$$
Esto implica que la sucesión está acotada tanto superior como inferiormente:
- **Acotada superiormente:** $\exists K \in \mathbb{R}$ tal que $a_n \leq K, \forall n$.
- **Acotada inferiormente:** $\exists k \in \mathbb{R}$ tal que $a_n \geq k, \forall n$.
### 2.2 Supremo e Ínfimo

Si el conjunto de valores de la sucesión $\{a_n : n \in \mathbb{N}\}$ está acotado:
- **Supremo ($\sup a_n$):** Es la menor de las cotas superiores.
- **Ínfimo ($\inf a_n$):** Es la mayor de las cotas inferiores.

### 2.3 Monotonía

Una sucesión se clasifica según cómo varían sus términos consecutivos:

1.  **Estrictamente Creciente:** $a_{n+1} > a_n, \quad \forall n \in \mathbb{N}$.
2.  **Creciente (o No Decreciente):** $a_{n+1} \geq a_n, \quad \forall n \in \mathbb{N}$.
3.  **Estrictamente Decreciente:** $a_{n+1} < a_n, \quad \forall n \in \mathbb{N}$.
4.  **Decreciente (o No Creciente):** $a_{n+1} \leq a_n, \quad \forall n \in \mathbb{N}$.
5.  **Constante:** $a_{n+1} = a_n, \quad \forall n \in \mathbb{N}$.
6.  **Monótona:** Si pertenece a cualquiera de las categorías anteriores.

**Otros tipos de comportamiento:**
- **Alternada:** Los signos de los términos se alternan (ej. $a_n = (-1)^n \cdot n$).
- **Oscilante:** No converge ni diverge a infinito (ej. $a_n = (-1)^n$).

---
## 3. Progresiones Básicas

Existen algunos casos especiales de succiones que se estudian, esta son llamadas *progresiones* y existen 3 tipos de estas:
### 3.1 Progresión Aritmética
Sucesión donde la diferencia entre términos consecutivos es constante ($d$).
- **Recursiva:** $a_{n+1} = a_n + d$
- **Término General:** $a_n = a_1 + (n-1)d$

### 3.2 Progresión Geométrica
Sucesión donde el cociente entre términos consecutivos es constante ($r \neq 0$).
- **Recursiva:** $a_{n+1} = a_n \cdot r$
- **Término General:** $a_n = a_1 \cdot r^{n-1}$

### 3.3 Progresión Armónica
Sucesión $(h_n)$ tal que sus recíprocos forman una progresión aritmética.
- **Forma:** $h_n = \frac{1}{a + (n-1)d}$

---

## 4. Límite y Convergencia

Este es el concepto central del análisis matemático aplicado a sucesiones.

### 4.1 Definición Rigurosa ($\epsilon - N$)

Para formalizar el concepto intuitivo de que los términos de una sucesión se "acercan arbitrariamente" a un valor, utilizamos la siguiente definición fundamental en Análisis Real.

 **Definición 4.1 (Convergencia de una Sucesión de Números Reales)**:
 Sea $(a_n)_{n=1}^{\infty}$ una sucesión de números reales. Decimos que la sucesión **converge** al número real $L \in \mathbb{R}$ si, para todo $\epsilon > 0$, existe un número natural $N$ tal que para todo $n \in \mathbb{N}$ con $n \geq N$, se cumple que: $$|a_n - L| < \epsilon$$
En notación lógica de cuantificadores, esto se expresa como: $$ \lim_{n \to \infty} a_n = L \iff \forall \epsilon > 0, \exists N \in \mathbb{N} \text{ tal que } (\forall n \geq N \implies |a_n - L| < \epsilon) $$Si tal número $L$ existe, decimos que la sucesión es **convergente**; en caso contrario, se dice que es **no convergente** o **divergente**.

**Interpretación:** Para cualquier entorno arbitrariamente pequeño $\epsilon$ alrededor de $L$, existe un momento $N$ a partir del cual **todos** los términos siguientes quedan atrapados dentro de ese entorno.
#### Observaciones Fundamentales

1. **Dependencia Funcional de $N$:** El umbral $N$ no es fijo; depende de la "tolerancia" elegida $\epsilon$. Rigurosamente, escribimos $N(\epsilon)$ para indicar esta dependencia. Generalmente, a menor $\epsilon$, mayor debe ser $N$.
2. **Interpretación Topológica (Entornos):** La condición $|a_n - L| < \epsilon$ es equivalente a $a_n \in (L-\epsilon, L+\epsilon)$. Esto significa que la sucesión converge a $L$ si todo $\epsilon$-entorno de $L$, denotado como $V_\epsilon(L)$, contiene a todos los términos de la sucesión **salvo, posiblemente, un número finito de ellos**.
3. **Irrelevancia del Inicio Finito:** La condición $n \geq N$ implica que el comportamiento de los primeros términos ($a_1, \dots, a_{N-1}$) es irrelevante para la convergencia. El límite es una propiedad del comportamiento de la "cola" de la sucesión.

**Definición 4.2 (Divergencia):**
Se dice que una sucesión $(a_n)$ es **divergente** si no converge a ningún límite finito $L \in \mathbb{R}$. Esto ocurre principalmente en dos casos:
1.  **Divergencia al Infinito:** Los términos crecen o decrecen sin cota ($\lim_{n \to \infty} a_n = \pm \infty$).
2.  **Oscilación:** La sucesión no tiende a ningún valor único (el límite no existe), como en el caso de $a_n = (-1)^n$.

**Observación Fundamental:**
Una sucesión convergente se comporta algebraicamente de manera análoga a un número real. Es decir, si conocemos los límites de dos sucesiones, podemos operar con ellos como si fueran números ordinarios. Esta propiedad permite calcular límites de expresiones complejas a partir de límites más simples, y es la base de las técnicas operativas del cálculo.

### 4.2 Teoremas de Convergencia

**Teorema 4.1 (Unicidad del Límite):**
Si una sucesión converge, su límite es único.

**Demostración**:
Procedemos por **reducción al absurdo**.
Supongamos que la sucesión converge a dos límites distintos, $L_1$ y $L_2$, con $L_1 \neq L_2$. Sea $\epsilon$ la mitad de la distancia entre estos dos puntos:
$$ \epsilon = \frac{|L_1 - L_2|}{2} > 0 $$
Dado que $\epsilon > 0$, aplicamos la definición de convergencia para ambos límites:
1.  Como $a_n \to L_1$, existe un $N_1 \in \mathbb{N}$ tal que:   $$ \forall n \geq N_1 \implies |a_n - L_1| < \epsilon $$
2.  Como $a_n \to L_2$, existe un $N_2 \in \mathbb{N}$ tal que:    $$ \forall n \geq N_2 \implies |a_n - L_2| < \epsilon $$
Definimos $N = \max(N_1, N_2)$. Para cualquier $n \geq N$, ambas condiciones anteriores son verdaderas simultáneamente.
Consideremos la distancia entre $L_1$ y $L_2$:
$$ |L_1 - L_2| = |(L_1 - a_n) + (a_n - L_2)| $$
Usando la **Desigualdad Triangular** ($|A+B| \leq |A| + |B|$):
$$ |L_1 - L_2| \leq |L_1 - a_n| + |a_n - L_2| $$
$$ |L_1 - L_2| = |a_n - L_1| + |a_n - L_2| $$
Sustituyendo las desigualdades de convergencia (válidas para $n \geq N$):
$$ |L_1 - L_2| < \epsilon + \epsilon = 2\epsilon $$
Sin embargo, al inicio elegimos $\epsilon = \frac{|L_1 - L_2|}{2}$, lo que implica que $|L_1 - L_2| = 2\epsilon$. Esto nos lleva a la contradicción:
$$ 2\epsilon < 2\epsilon $$
Como $2\epsilon < 2\epsilon$ es falso, nuestra suposición inicial de que $L_1 \neq L_2$ debe ser errónea. Por lo tanto, $L_1 = L_2$.

**Teorema 4.2 (Sucesión Convergente y Acotada):**
Toda sucesión convergente está acotada. (El recíproco no es cierto, ej: $(-1)^n$).

**Teorema 4.3 (Operaciones Algebraicas con Límites):**
Sean $(a_n)$ y $(b_n)$ dos sucesiones convergentes tales que $\lim_{n \to \infty} a_n = A$ y $\lim_{n \to \infty} b_n = B$. Entonces:

1.  **Suma y Resta:** $$\lim_{n \to \infty} (a_n \pm b_n) = \lim_{n \to \infty} {a_n} \pm \lim_{n \to \infty} {b_n}$$
2.  **Producto por Escalar:** $$\lim_{n \to \infty} (k \cdot a_n) = k \cdot \lim_{n \to \infty} {a_n}, \quad \forall k \in \mathbb{R}$$
3.  **Producto:** $$\lim_{n \to \infty} (a_n \cdot b_n) = \lim_{n \to \infty} {a_n} \cdot \lim_{n \to \infty} {b_n}$$
4.  **Cociente:** $$\lim_{n \to \infty} \frac{a_n}{b_n} = \frac{\lim_{n \to \infty} {a_n}}{\lim_{n \to \infty} {b_n}}$$ (siempre que $\lim_{n \to \infty} {b_n} \neq 0$ para todo $n \geq n_0$)

5. Sucesión constante:
   $$\lim_{n \to \infty} c = c$$
6. Potencia:
   $$\lim_{n \to \infty} a_n^p = [\lim_{n \to \infty} {a_n}]^p \quad p>0 \quad \text{y} \quad a_n>0$$

**Teorema 4.4 (Teorema del Sándwich / Encaje):**
Si $a_n \leq b_n \leq c_n$ para todo $n \geq n_0$ y $\lim a_n = \lim c_n = L$, entonces $\lim b_n = L$.

**Teorema 4.5 (Convergencia Monótona):**
Toda sucesión monótona y acotada es convergente. Específicamente:
1.  Si $(a_n)$ es creciente y acotada superiormente, entonces converge a su supremo: $\lim_{n \to \infty} a_n = \sup\{a_n\}$.
2.  Si $(a_n)$ es decreciente y acotada inferiormente, entonces converge a su ínfimo: $\lim_{n \to \infty} a_n = \inf\{a_n\}$.

**Demostración (Caso Creciente)**
Sea $(a_n)$ una sucesión creciente y acotada superiormente.
Por el **Axioma del Supremo** (o completitud de $\mathbb{R}$), el conjunto de valores $A = \{a_n : n \in \mathbb{N}\}$ tiene un supremo en $\mathbb{R}$.
Sea $L = \sup A$. Queremos demostrar que $\lim_{n \to \infty} a_n = L$.
Sea $\epsilon > 0$ arbitrario.
1.  Consideremos el número $L - \epsilon$. Dado que $L$ es la menor cota superior, $L - \epsilon$ **no** es una cota superior de la sucesión.
2.  Por lo tanto, debe existir algún término $a_N$ en la sucesión tal que:    $$ L - \epsilon < a_N $$
3. Como la sucesión es **creciente**, para todo $n \geq N$, tenemos $a_n \geq a_N$. Combinando esto con el paso anterior:
   $$ L - \epsilon < a_N \leq a_n $$
4. Además, dado que $L$ es el supremo (y por tanto una cota superior), sabemos que $a_n \leq L$ para todo $n$. Como $\epsilon > 0$, es obvio que $L < L + \epsilon$. Así:  $$ a_n \leq L < L + \epsilon $$
Juntando ambas desigualdades (3 y 4), obtenemos que para todo $n \geq N$:
$$ L - \epsilon < a_n < L + \epsilon $$
$$ -\epsilon < a_n - L < \epsilon $$
$$ |a_n - L| < \epsilon $$

Por definición de límite, $\lim_{n \to \infty} a_n = L$.

#### **Nota sobre el Caso Decreciente**

Para demostrar el caso de una sucesión decreciente y acotada inferiormente, se puede proceder de forma análoga usando el ínfimo, o bien considerar la sucesión $b_n = -a_n$.
Si $(a_n)$ es decreciente y acotada inferiormente por $K$, entonces $(b_n)$ es creciente y acotada superiormente por $-K$. Por lo tanto, $b_n$ converge a $\sup\{-a_n\}$, lo que implica que $a_n$ converge a $-\sup\{-a_n\} = \inf\{a_n\}$.

---

## 5. Sucesiones Especiales y Completitud

### 5.1 El Número $e$
Considerando la sucesión $a_n = \left(1 + \frac{1}{n}\right)^n$. Se puede demostrar que es monótona creciente y acotada superiormente.
**Definición:**
$$e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n \approx 2.71828...$$
### 5.2 Sucesión de Fibonacci
Definida por una **ecuación en diferencias** (recurrencia) de segundo orden:
$$F_0=0, F_1=1; \quad F_n = F_{n-1} + F_{n-2}, \quad \forall n \geq 2$$
*Nota:* Las ecuaciones en diferencias son el análogo discreto de las ecuaciones diferenciales y se estudian a fondo en *Matemáticas Discretas*.

### 5.3 Sucesiones de Cauchy
**Definición 5.2:**
Una sucesión $(a_n)$ es de **Cauchy** si sus términos se acercan arbitrariamente entre sí conforme $n$ crece:
$$\forall \epsilon > 0, \exists N \in \mathbb{N} \text{ tal que } \forall n, m \geq N \implies |a_n - a_m| < \epsilon$$

**Teorema de Completitud de $\mathbb{R}$:**
En los números reales, una sucesión es convergente **si y solo si** es una sucesión de Cauchy.

---

## 6. Introducción a Ecuaciones en Diferencias Finitas (Opcional)

Muchas sucesiones importantes no se presentan con una fórmula explícita del tipo $a_n = f(n)$, sino mediante una relación que vincula un término con sus predecesores. Estas relaciones se denominan **ecuaciones en diferencias** o relaciones de recurrencia.

### 6.1 Definición y Término General
Una ecuación en diferencias de orden $k$ determina el término $a_{n+k}$ en función de los $k$ términos anteriores:
$$a_{n+k} = F(n, a_{n+k-1}, \dots, a_n)$$

Resolver la ecuación implica hallar el **término general**, es decir, una expresión cerrada $a_n = g(n)$ que dependa únicamente de $n$ y de las condiciones iniciales, sin referenciar términos anteriores.

### 6.2 Ejemplo de Método de Solución
Para ecuaciones lineales homogéneas con coeficientes constantes (como Fibonacci), se emplea un método análogo a las ecuaciones diferenciales lineales:
1.  Se propone una solución de la forma $a_n = r^n$.
2.  Se halla la **ecuación característica** asociada.
3.  La solución general es una combinación lineal de las raíces de dicha ecuación.

> **Nota del Curso:** La teoría completa de estas ecuaciones, incluyendo casos no homogéneos y sistemas, constituye un bloque central del curso de **Matemáticas Discretas**, donde se estudiarán con el rigor necesario.

---

## 7. Curiosidad: Interpolación Polinómica
Es posible construir una sucesión que tome valores arbitrarios para sus primeros $k$ términos usando polinomios. La fórmula presentada es una variante de la **Forma de Newton del polinomio interpolador** para nodos enteros equidistantes:

$$a_n = c_0 + c_1(n-1) + c_2(n-1)(n-2) + c_3(n-1)(n-2)(n-3) + \dots$$

Esto permite "manipular" los siguientes números ajustando los coeficientes $c_i$, ya que cada término $(n-1)(n-2)\dots(n-k)$ se anula para valores de $n$ menores que $k+1$.




