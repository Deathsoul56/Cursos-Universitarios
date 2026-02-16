# Clase 9: Sucesiones Numéricas

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

Estos conceptos refinan la noción de acotación, identificando las cotas "óptimas" de un conjunto.

**Definición 2.3 (Supremo):**
Sea $S \subseteq \mathbb{R}$ un conjunto no vacío y acotado superiormente. El **supremo** de $S$, denotado $\sup(S)$, es el número real $M$ que satisface:
1. $M$ es una cota superior de $S$: $\forall x \in S, x \leq M$
2. $M$ es la **menor** de las cotas superiores: Si $K$ es otra cota superior, entonces $M \leq K$

**Definición equivalente (propiedad ε):** $M = \sup(S)$ si y solo si:
- $\forall x \in S, x \leq M$
- $\forall \epsilon > 0, \exists x \in S$ tal que $x > M - \epsilon$

La segunda condición dice que "no hay cota superior menor que $M$".

**Definición 2.4 (Ínfimo):**
Sea $S \subseteq \mathbb{R}$ un conjunto no vacío y acotado inferiormente. El **ínfimo** de $S$, denotado $\inf(S)$, es el número real $m$ que satisface:
1. $m$ es una cota inferior de $S$: $\forall x \in S, x \geq m$
2. $m$ es la **mayor** de las cotas inferiores: Si $k$ es otra cota inferior, entonces $m \geq k$

**Axioma del Supremo (Completitud de $\mathbb{R}$):**
Todo conjunto no vacío de números reales que esté acotado superiormente tiene supremo en $\mathbb{R}$.

Este axioma distingue a $\mathbb{R}$ de $\mathbb{Q}$ y es fundamental para el Análisis.

**Diferencia entre Máximo y Supremo:**
- **Máximo:** Es el elemento más grande **que pertenece** al conjunto
- **Supremo:** Es la menor cota superior (puede o no pertenecer al conjunto)

Si el máximo existe, entonces $\max(S) = \sup(S)$. Pero puede existir el supremo sin que exista el máximo.

**Ejemplo 2.1:**
Consideremos el intervalo abierto $S = (0, 1) = \{x \in \mathbb{R} : 0 < x < 1\}$.

- **Supremo:** $\sup(S) = 1$
  - Es cota superior: Todo $x \in S$ satisface $x < 1$
  - Es la menor: Si $K < 1$, entonces $K$ no es cota superior (existe $x \in S$ con $x > K$, por ejemplo $x = \frac{1+K}{2}$)
  - **No pertenece al conjunto:** $1 \notin S$
  
- **Ínfimo:** $\inf(S) = 0$
  - Es cota inferior: Todo $x \in S$ satisface $x > 0$
  - Es la mayor: Si $k > 0$, entonces existe $x \in S$ con $x < k$ (por ejemplo $x = \frac{k}{2}$)
  - **No pertenece al conjunto:** $0 \notin S$
  
- **Máximo y mínimo:** $S$ no tiene máximo ni mínimo

**Ejemplo 2.2:**
Consideremos el intervalo cerrado $T = [0, 1] = \{x \in \mathbb{R} : 0 \leq x \leq 1\}$.

- $\sup(T) = 1$ y $\max(T) = 1$ (el supremo pertenece al conjunto)
- $\inf(T) = 0$ y $\min(T) = 0$ (el ínfimo pertenece al conjunto)

**Ejemplo 2.3 (Sucesión):**
Consideremos la sucesión $a_n = 1 - \frac{1}{n}$ para $n \geq 1$.

Los primeros términos son: $0, \frac{1}{2}, \frac{2}{3}, \frac{3}{4}, \frac{4}{5}, \dots$

El conjunto de valores es $A = \left\{1 - \frac{1}{n} : n \in \mathbb{N}\right\}$.

- **Análisis de acotación:**
  - La sucesión es estrictamente creciente: $a_{n+1} > a_n$
  - Para todo $n$: $0 < a_n < 1$
  
- **Ínfimo y mínimo:**
  - $\inf(A) = a_1 = 1 - 1 = 0$ 
  - $\min(A) = 0$ (el primer término)
  
- **Supremo:**
  - $\sup(A) = 1$
  - **No hay máximo:** Ningún término alcanza el valor 1
  - Justificación: Para cualquier $n$, tenemos $a_n = 1 - \frac{1}{n} < 1$
  - Si tomamos $K < 1$, podemos encontrar $N$ tal que $1 - \frac{1}{N} > K$ (tomando $N > \frac{1}{1-K}$)

**Ejemplo 2.4 (Sucesión alternada acotada):**
Consideremos $b_n = \frac{(-1)^n}{n}$ para $n \geq 1$.

Los primeros términos son: $-1, \frac{1}{2}, -\frac{1}{3}, \frac{1}{4}, -\frac{1}{5}, \frac{1}{6}, \dots$

El conjunto de valores es $B = \left\{\frac{(-1)^n}{n} : n \in \mathbb{N}\right\}$.

- **Supremo:**
  - Los términos positivos son: $\frac{1}{2}, \frac{1}{4}, \frac{1}{6}, \dots$ (términos pares)
  - El mayor término positivo es $b_2 = \frac{1}{2}$
  - Por lo tanto: $\sup(B) = \frac{1}{2} = \max(B)$
  
- **Ínfimo:**
  - Los términos negativos son: $-1, -\frac{1}{3}, -\frac{1}{5}, \dots$ (términos impares)
  - El menor término negativo es $b_1 = -1$
  - Por lo tanto: $\inf(B) = -1 = \min(B)$

**Proposición 2.1 (Supremo/Ínfimo de Sucesiones):**
Si $(a_n)$ es una sucesión acotada:
- El supremo $\sup\{a_n\}$ es el menor número que es mayor o igual a todos los términos
- El ínfimo $\inf\{a_n\}$ es el mayor número que es menor o igual a todos los términos

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

Existen algunos casos especiales de sucesiones que se estudian, estas son llamadas *progresiones* y existen 3 tipos principales:

### 3.1 Progresión Aritmética

Sucesión donde la diferencia entre términos consecutivos es constante ($d$), llamada **razón** o **diferencia común**.

**Definición 3.1:**
- **Forma Recursiva:** $a_{n+1} = a_n + d$
- **Término General:** $a_n = a_1 + (n-1)d$

**Fórmula de la Suma de los Primeros $n$ Términos:**
$$S_n = \sum_{k=1}^{n} a_k = \frac{n(a_1 + a_n)}{2} = \frac{n[2a_1 + (n-1)d]}{2}$$

**Demostración de la fórmula:**
Consideremos la suma:
$$S_n = a_1 + a_2 + a_3 + \cdots + a_{n-1} + a_n$$

Escribiendo la misma suma en orden inverso:
$$S_n = a_n + a_{n-1} + a_{n-2} + \cdots + a_2 + a_1$$

Sumando ambas expresiones término a término:
$$2S_n = (a_1 + a_n) + (a_2 + a_{n-1}) + (a_3 + a_{n-2}) + \cdots + (a_{n-1} + a_2) + (a_n + a_1)$$

Observemos que cada par suma lo mismo. Por ejemplo:
- $a_1 + a_n = a_1 + [a_1 + (n-1)d] = 2a_1 + (n-1)d$
- $a_2 + a_{n-1} = [a_1 + d] + [a_1 + (n-2)d] = 2a_1 + (n-1)d$

Cada uno de los $n$ pares suma $(a_1 + a_n)$. Por lo tanto:
$$2S_n = n(a_1 + a_n)$$
$$S_n = \frac{n(a_1 + a_n)}{2}$$

**Ejemplo 3.1:**
Encontrar el término general y la suma de los primeros 50 términos de la progresión: $3, 7, 11, 15, \dots$

**Solución:**
- $a_1 = 3$, diferencia común: $d = 7 - 3 = 4$
- Término general: $a_n = 3 + (n-1) \cdot 4 = 3 + 4n - 4 = 4n - 1$
- Término 50: $a_{50} = 4(50) - 1 = 199$
- Suma: $S_{50} = \frac{50(3 + 199)}{2} = \frac{50 \cdot 202}{2} = 50 \cdot 101 = 5050$

**Ejemplo 3.2 (Suma de Gauss):**
Calcular la suma de los primeros 100 números naturales: $1 + 2 + 3 + \cdots + 100$

**Solución:**
Esta es una progresión aritmética con $a_1 = 1$, $d = 1$, $n = 100$, $a_{100} = 100$.
$$S_{100} = \frac{100(1 + 100)}{2} = \frac{100 \cdot 101}{2} = 5050$$

**Nota histórica:** Carl Friedrich Gauss calculó este resultado a los 10 años usando el método de emparejar términos.

**Ejemplo 3.3:**
Una empresa ofrece un plan de inversión donde el primer mes se depositan $100, el segundo mes $150, el tercer mes $200, y así sucesivamente, aumentando $50 cada mes. ¿Cuánto se habrá depositado en total después de 24 meses?

**Solución:**
- Progresión: $100, 150, 200, \dots$
- $a_1 = 100$, $d = 50$, $n = 24$
- $a_{24} = 100 + (24-1) \cdot 50 = 100 + 1150 = 1250$
- $S_{24} = \frac{24(100 + 1250)}{2} = \frac{24 \cdot 1350}{2} = 12 \cdot 1350 = 16200$

**Respuesta:** Se habrán depositado $16,200 en total.

### 3.2 Progresión Geométrica

Sucesión donde el cociente entre términos consecutivos es constante ($r \neq 0$), llamado **razón común**.

**Definición 3.2:**
- **Forma Recursiva:** $a_{n+1} = a_n \cdot r$
- **Término General:** $a_n = a_1 \cdot r^{n-1}$

**Fórmula de la Suma de los Primeros $n$ Términos:**
$$S_n = \sum_{k=1}^{n} a_k = \begin{cases}
a_1 \cdot \frac{1 - r^n}{1 - r} = a_1 \cdot \frac{r^n - 1}{r - 1} & \text{si } r \neq 1 \\
n \cdot a_1 & \text{si } r = 1
\end{cases}$$

**Demostración:**
Sea $S_n = a_1 + a_1 r + a_1 r^2 + \cdots + a_1 r^{n-1}$

Multiplicamos ambos lados por $r$:
$$r S_n = a_1 r + a_1 r^2 + a_1 r^3 + \cdots + a_1 r^n$$

Restamos la segunda ecuación de la primera:
$$S_n - r S_n = a_1 - a_1 r^n$$
$$S_n(1 - r) = a_1(1 - r^n)$$
$$S_n = a_1 \cdot \frac{1 - r^n}{1 - r}$$

**Suma Infinita (cuando $|r| < 1$):**
Si $|r| < 1$, entonces $\lim_{n \to \infty} r^n = 0$, y la suma de la serie geométrica infinita converge:
$$S_{\infty} = \sum_{k=1}^{\infty} a_1 r^{k-1} = \frac{a_1}{1-r}, \quad |r| < 1$$

**Ejemplo 3.4:**
Encontrar el término general y la suma de los primeros 10 términos de: $2, 6, 18, 54, \dots$

**Solución:**
- $a_1 = 2$, razón: $r = \frac{6}{2} = 3$
- Término general: $a_n = 2 \cdot 3^{n-1}$
- Término 10: $a_{10} = 2 \cdot 3^9 = 2 \cdot 19683 = 39366$
- Suma: $S_{10} = 2 \cdot \frac{3^{10} - 1}{3 - 1} = 2 \cdot \frac{59049 - 1}{2} = 59048$

**Ejemplo 3.5 (Fracción decimal periódica):**
Expresar $0.\overline{3} = 0.333\dots$ como fracción.

**Solución:**
$$0.333\dots = \frac{3}{10} + \frac{3}{100} + \frac{3}{1000} + \cdots = \frac{3}{10}\left(1 + \frac{1}{10} + \frac{1}{100} + \cdots\right)$$

Esta es una serie geométrica con $a_1 = 1$ y $r = \frac{1}{10}$:
$$\sum_{k=0}^{\infty} \left(\frac{1}{10}\right)^k = \frac{1}{1 - \frac{1}{10}} = \frac{1}{\frac{9}{10}} = \frac{10}{9}$$

Por lo tanto:
$$0.\overline{3} = \frac{3}{10} \cdot \frac{10}{9} = \frac{3}{9} = \frac{1}{3}$$

**Ejemplo 3.6 (Interés compuesto):**
Se invierten $1000 a una tasa de interés del 5% anual compuesto. ¿Cuánto dinero habrá después de 20 años?

**Solución:**
El capital después de $n$ años forma una progresión geométrica:
- $a_1 = 1000(1.05) = 1050$
- $r = 1.05$
- $a_n = 1000(1.05)^n$
- Después de 20 años: $a_{20} = 1000(1.05)^{20} \approx 1000 \cdot 2.653 \approx 2653$

**Respuesta:** Aproximadamente $2,653.

**Ejemplo 3.7 (Convergencia):**
Determinar si la progresión geométrica $a_n = 5 \cdot \left(\frac{1}{2}\right)^{n-1}$ converge, y encontrar su límite.

**Solución:**
- $r = \frac{1}{2}$, entonces $|r| < 1$
- La sucesión converge a: $\lim_{n \to \infty} a_n = \lim_{n \to \infty} 5 \cdot \left(\frac{1}{2}\right)^{n-1} = 5 \cdot 0 = 0$

### 3.3 Progresión Armónica

Sucesión $(h_n)$ cuyos recíprocos forman una progresión aritmética.

**Definición 3.3:**
Si $(a_n)$ es una progresión aritmética, entonces $(h_n)$ con $h_n = \frac{1}{a_n}$ es una **progresión armónica**.

**Forma general:**
$$h_n = \frac{1}{a + (n-1)d}$$

donde $a$ es el primer término de la progresión aritmética de los recíprocos, y $d$ es su diferencia común.

**Ejemplo 3.8:**
La sucesión $1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \dots$ es una progresión armónica porque sus recíprocos $1, 2, 3, 4, \dots$ forman una progresión aritmética.

**Observación:** Las progresiones armónicas no tienen una fórmula simple para la suma de sus términos.

**Proposición 3.1 (Convergencia de progresiones):**
- **Aritmética:** Diverge si $d \neq 0$; converge a $a_1$ si $d = 0$ (sucesión constante)
- **Geométrica:** 
  - Converge a 0 si $|r| < 1$
  - Converge a $a_1$ si $r = 1$
  - Diverge si $|r| > 1$ o $r = -1$
- **Armónica:** Siempre converge a 0 (caso particular: serie armónica diverge, pero la sucesión converge)

---

## 4. Límite y Convergencia

Este es el concepto central del análisis matemático aplicado a sucesiones.

### 4.1 Definición Rigurosa ($\epsilon - N$)

Para formalizar el concepto intuitivo de que los términos de una sucesión se "acercan arbitrariamente" a un valor, utilizamos la siguiente definición fundamental en Análisis Real.

 **Definición 4.1 (Convergencia de una Sucesión de Números Reales)**:
 Sea $(a_n)_{n=1}^{\infty}$ una sucesión de números reales. Decimos que la sucesión **converge** al número real $L \in \mathbb{R}$ si, para todo $\epsilon > 0$, existe un número natural $N$ tal que para todo $n \in \mathbb{N}$ con $n \geq N$, se cumple que: $$|a_n - L| < \epsilon$$
En notación lógica de cuantificadores, esto se expresa como: $$ \lim_{n \to \infty} a_n = L \iff \forall \epsilon > 0, \exists N \in \mathbb{N} \text{ tal que } (\forall n \geq N \implies |a_n - L| < \epsilon) $$Si tal número $L$ existe, decimos que la sucesión es **convergente**; en caso contrario, se dice que es **no convergente** o **divergente**.

**Interpretación:** Para cualquier entorno arbitrariamente pequeño $\epsilon$ alrededor de $L$, existe un momento $N$ a partir del cual **todos** los términos siguientes quedan atrapados dentro de ese entorno.

### 4.2 Ejemplos de Verificación con la Definición $\epsilon-N$

Para dominar el concepto de límite, es fundamental practicar la verificación directa usando la definición formal. En estos ejemplos, dado un $\epsilon > 0$ arbitrario, encontramos explícitamente un $N$ que satisface la condición.

**Ejemplo 4.1:**
Demostrar usando la definición $\epsilon-N$ que $\lim_{n \to \infty} \frac{1}{n} = 0$.

**Demostración:**
Debemos probar que para todo $\epsilon > 0$, existe $N \in \mathbb{N}$ tal que para todo $n \geq N$:
$$\left|\frac{1}{n} - 0\right| < \epsilon$$

**Paso 1:** Simplificamos la desigualdad:
$$\left|\frac{1}{n}\right| < \epsilon$$
$$\frac{1}{n} < \epsilon$$
$$1 < n\epsilon$$
$$n > \frac{1}{\epsilon}$$

**Paso 2:** Elegimos $N$. Para garantizar que $n > \frac{1}{\epsilon}$, basta tomar:
$$N = \left\lceil \frac{1}{\epsilon} \right\rceil + 1$$

(donde $\lceil x \rceil$ es la función techo, el menor entero mayor o igual que $x$)

**Paso 3:** Verificación. Para todo $n \geq N$:
$$n \geq N > \frac{1}{\epsilon}$$
$$\frac{1}{n} \leq \frac{1}{N} < \epsilon$$
$$\left|\frac{1}{n} - 0\right| < \epsilon$$ ✓

**Conclusión:** Por definición, $\lim_{n \to \infty} \frac{1}{n} = 0$. $\square$

**Ejemplo numérico:** Si $\epsilon = 0.01$, entonces $N > 100$, así que tomamos $N = 101$. Todos los términos $a_n$ con $n \geq 101$ satisfacen $|a_n - 0| < 0.01$.

**Ejemplo 4.2:**
Demostrar que $\lim_{n \to \infty} \frac{2n + 1}{n} = 2$.

**Demostración:**
Debemos probar que para todo $\epsilon > 0$, existe $N$ tal que para todo $n \geq N$:
$$\left|\frac{2n + 1}{n} - 2\right| < \epsilon$$

**Paso 1:** Simplificamos:
$$\left|\frac{2n + 1}{n} - 2\right| = \left|\frac{2n + 1 - 2n}{n}\right| = \left|\frac{1}{n}\right| = \frac{1}{n}$$

**Paso 2:** La condición se reduce a:
$$\frac{1}{n} < \epsilon \iff n > \frac{1}{\epsilon}$$

**Paso 3:** Tomamos $N = \left\lceil \frac{1}{\epsilon} \right\rceil + 1$.

Para todo $n \geq N$: $\frac{1}{n} < \epsilon$, por lo tanto:
$$\left|\frac{2n + 1}{n} - 2\right| < \epsilon$$ ✓

**Conclusión:** $\lim_{n \to \infty} \frac{2n + 1}{n} = 2$. $\square$

**Ejemplo 4.3:**
Demostrar que $\lim_{n \to \infty} \frac{n^2}{n^2 + 1} = 1$.

**Demostración:**
Para todo $\epsilon > 0$, debemos encontrar $N$ tal que para $n \geq N$:
$$\left|\frac{n^2}{n^2 + 1} - 1\right| < \epsilon$$

**Paso 1:** Simplificamos:
$$\left|\frac{n^2}{n^2 + 1} - 1\right| = \left|\frac{n^2 - (n^2 + 1)}{n^2 + 1}\right| = \left|\frac{-1}{n^2 + 1}\right| = \frac{1}{n^2 + 1}$$

**Paso 2:** Necesitamos:
$$\frac{1}{n^2 + 1} < \epsilon$$

Observemos que $\frac{1}{n^2 + 1} < \frac{1}{n^2}$ (el denominador es mayor). Por lo tanto, si garantizamos que $\frac{1}{n^2} < \epsilon$, automáticamente se cumple la desigualdad original.

$$\frac{1}{n^2} < \epsilon \iff n^2 > \frac{1}{\epsilon} \iff n > \frac{1}{\sqrt{\epsilon}}$$

**Paso 3:** Tomamos $N = \left\lceil \frac{1}{\sqrt{\epsilon}} \right\rceil + 1$.

Para todo $n \geq N$:
$$\frac{1}{n^2 + 1} < \frac{1}{n^2} < \epsilon$$

Por lo tanto: $\left|\frac{n^2}{n^2 + 1} - 1\right| < \epsilon$ ✓

**Conclusión:** $\lim_{n \to \infty} \frac{n^2}{n^2 + 1} = 1$. $\square$

**Ejemplo 4.4:**
Demostrar que $\lim_{n \to \infty} \frac{3n - 5}{2n + 7} = \frac{3}{2}$.

**Demostración:**
Para todo $\epsilon > 0$, debemos encontrar $N$ tal que para $n \geq N$:
$$\left|\frac{3n - 5}{2n + 7} - \frac{3}{2}\right| < \epsilon$$

**Paso 1:** Simplificamos usando álgebra:
$$\left|\frac{3n - 5}{2n + 7} - \frac{3}{2}\right| = \left|\frac{2(3n - 5) - 3(2n + 7)}{2(2n + 7)}\right|$$
$$= \left|\frac{6n - 10 - 6n - 21}{2(2n + 7)}\right| = \left|\frac{-31}{2(2n + 7)}\right| = \frac{31}{2(2n + 7)}$$

**Paso 2:** Necesitamos:
$$\frac{31}{2(2n + 7)} < \epsilon$$

Para $n \geq 1$, tenemos $2n + 7 \geq 9$, pero para simplificar, usamos $2n + 7 > 2n$:
$$\frac{31}{2(2n + 7)} < \frac{31}{4n}$$

Queremos:
$$\frac{31}{4n} < \epsilon \iff n > \frac{31}{4\epsilon}$$

**Paso 3:** Tomamos $N = \left\lceil \frac{31}{4\epsilon} \right\rceil + 1$.

Para todo $n \geq N$:
$$\left|\frac{3n - 5}{2n + 7} - \frac{3}{2}\right| = \frac{31}{2(2n + 7)} < \frac{31}{4n} < \epsilon$$ ✓

**Conclusión:** $\lim_{n \to \infty} \frac{3n - 5}{2n + 7} = \frac{3}{2}$. $\square$

**Ejemplo 4.5 (Teorema del Sándwich):**
Consideremos la sucesión $a_n = \frac{\sin(n)}{n}$. Demostrar que $\lim_{n \to \infty} a_n = 0$ sin usar directamente la definición $\epsilon-N$.

**Demostración usando el Teorema del Sándwich:**

Sabemos que para todo $n \in \mathbb{N}$:
$$-1 \leq \sin(n) \leq 1$$

Dividiendo por $n > 0$:
$$-\frac{1}{n} \leq \frac{\sin(n)}{n} \leq \frac{1}{n}$$

Como:
- $\lim_{n \to \infty} -\frac{1}{n} = 0$ (demostrado en Ejemplo 4.1)
- $\lim_{n \to \infty} \frac{1}{n} = 0$ (demostrado en Ejemplo 4.1)

Por el Teorema del Sándwich (Teorema 4.4):
$$\lim_{n \to \infty} \frac{\sin(n)}{n} = 0$$ $\square$

**Observación metodológica:** Estos ejemplos ilustran que:
1. La verificación con $\epsilon-N$ es **constructiva**: siempre encontramos un $N$ explícito
2. A menudo se usan **cotas superiores** más simples para facilitar el cálculo de $N$
3. Los **teoremas** (Sándwich, operaciones algebraicas) permiten evitar el uso directo de $\epsilon-N$ en casos complejos

### 4.3 Teoremas de Convergencia

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

Por definición de límite, $\lim_{n \to \infty} a_n = L$.

#### **Nota sobre el Caso Decreciente**

Para demostrar el caso de una sucesión decreciente y acotada inferiormente, se puede proceder de forma análoga usando el ínfimo, o bien considerar la sucesión $b_n = -a_n$.
Si $(a_n)$ es decreciente y acotada inferiormente por $K$, entonces $(b_n)$ es creciente y acotada superiormente por $-K$. Por lo tanto, $b_n$ converge a $\sup\{-a_n\}$, lo que implica que $a_n$ converge a $-\sup\{-a_n\} = \inf\{a_n\}$.

### 4.4 Límites Fundamentales

Existen ciertos límites que aparecen frecuentemente en el cálculo y que conviene conocer de memoria. A continuación presentamos los más importantes, con sus demostraciones o justificaciones.

**Límite 1:**
$$\lim_{n \to \infty} \frac{1}{n^p} = 0, \quad \forall p > 0$$

**Demostración:**
Para $p > 0$, tenemos $n^p \geq n$. Por lo tanto:
$$0 < \frac{1}{n^p} \leq \frac{1}{n}$$

Como $\lim_{n \to \infty} \frac{1}{n} = 0$, por el Teorema del Sándwich:
$$\lim_{n \to \infty} \frac{1}{n^p} = 0$$ $\square$

**Límite 2:**
$$\lim_{n \to \infty} \sqrt[n]{n} = 1$$

**Demostración (bosquejo):**
Sea $a_n = \sqrt[n]{n} = n^{1/n}$. Escribimos $a_n = 1 + h_n$ donde $h_n > 0$.

Entonces:
$$n = (1 + h_n)^n \geq 1 + nh_n + \frac{n(n-1)}{2}h_n^2$$

(por el desarrollo del binomio). Tomando solo los dos primeros términos:
$$n \geq 1 + nh_n \implies h_n \leq \frac{n-1}{n} < 1$$

Tomando los tres primeros:
$$n \geq \frac{n(n-1)}{2}h_n^2 \implies h_n^2 \leq \frac{2}{n-1} \implies 0 < h_n \leq \sqrt{\frac{2}{n-1}}$$

Como $\lim_{n \to \infty} \sqrt{\frac{2}{n-1}} = 0$, por el Teorema del Sándwich, $h_n \to 0$.

Por lo tanto: $\sqrt[n]{n} = 1 + h_n \to 1 + 0 = 1$. $\square$

**Límite 3:**
$$\lim_{n \to \infty} \sqrt[n]{a} = 1, \quad \forall a > 0$$

**Demostración:**
**Caso 1:** Si $a \geq 1$, entonces $1 \leq \sqrt[n]{a} \leq \sqrt[n]{a \cdot n}$ (para $n$ suficientemente grande).

Podemos escribir:
$$\sqrt[n]{a} = \sqrt[n]{a} \cdot \frac{\sqrt[n]{n}}{\sqrt[n]{n}} = \frac{\sqrt[n]{an}}{\sqrt[n]{n}}$$

Como $\sqrt[n]{n} \to 1$ y $\sqrt[n]{an} \to 1$ (aplicando el Límite 2 a $an$), obtenemos:
$$\lim_{n \to \infty} \sqrt[n]{a} = \frac{1}{1} = 1$$

**Caso 2:** Si $0 < a < 1$, entonces $\sqrt[n]{a} = \frac{1}{\sqrt[n]{1/a}}$. Como $\frac{1}{a} > 1$, por el Caso 1:
$$\lim_{n \to \infty} \sqrt[n]{\frac{1}{a}} = 1 \implies \lim_{n \to \infty} \sqrt[n]{a} = \frac{1}{1} = 1$$ $\square$

**Límite 4 (Exponencial vs. Factorial):**
$$\lim_{n \to \infty} \frac{a^n}{n!} = 0, \quad \forall a \in \mathbb{R}$$

**Demostración:**
Sea $a > 0$ (el caso $a \leq 0$ es inmediato por acotación).

Consideremos el cociente de términos consecutivos:
$$\frac{a_{n+1}}{a_n} = \frac{a^{n+1}/(n+1)!}{a^n/n!} = \frac{a}{n+1}$$

Para $n > 2|a|$, tenemos $\frac{a}{n+1} < \frac{1}{2}$.

Sea $N$ tal que $N > 2|a|$. Entonces para $n > N$:
$$a_n = a_N \cdot \frac{a_{N+1}}{a_N} \cdot \frac{a_{N+2}}{a_{N+1}} \cdots \frac{a_n}{a_{n-1}} < a_N \cdot \left(\frac{1}{2}\right)^{n-N}$$

Como $\lim_{n \to \infty} \left(\frac{1}{2}\right)^{n-N} = 0$, por el Teorema del Sándwich:
$$\lim_{n \to \infty} \frac{a^n}{n!} = 0$$ $\square$

**Interpretación:** El factorial crece **mucho más rápido** que cualquier exponencial.

**Límite 5 (Factorial vs. Potencia):**
$$\lim_{n \to \infty} \frac{n!}{n^n} = 0$$

**Justificación:**
Observemos que:
$$\frac{n!}{n^n} = \frac{1 \cdot 2 \cdot 3 \cdots n}{n \cdot n \cdot n \cdots n} = \frac{1}{n} \cdot \frac{2}{n} \cdot \frac{3}{n} \cdots \frac{n}{n}$$

Cada factor (excepto el último) es menor que 1, y hay $n$ factores. Se puede demostrar rigurosamente usando la desigualdad de Stirling o el criterio del cociente.

**Límite 6 (Potencia vs. Exponencial):**
$$\lim_{n \to \infty} \frac{n^k}{a^n} = 0, \quad \forall k \in \mathbb{N}, \, a > 1$$

**Interpretación:** Una función exponencial (con base $> 1$) crece **mucho más rápido** que cualquier polinomio.

**Demostración (caso $k=1$):**
Sea $a = 1 + h$ con $h > 0$. Por el binomio de Newton:
$$a^n = (1+h)^n = 1 + nh + \frac{n(n-1)}{2}h^2 + \cdots \geq \frac{n(n-1)}{2}h^2$$

Para $n \geq 2$:
$$0 < \frac{n}{a^n} \leq \frac{n}{\frac{n(n-1)}{2}h^2} = \frac{2}{(n-1)h^2}$$

Como $\lim_{n \to \infty} \frac{2}{(n-1)h^2} = 0$, por el Sándwich:
$$\lim_{n \to \infty} \frac{n}{a^n} = 0$$

Para $k > 1$, se aplica el resultado repetidamente. $\square$

**Límite 7 (Definición de $e$):**
$$\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e \approx 2.71828...$$

**Generalización:**
$$\lim_{n \to \infty} \left(1 + \frac{a}{n}\right)^n = e^a, \quad \forall a \in \mathbb{R}$$

**Demostración de la generalización:**
Haciendo el cambio de variable $m = \frac{n}{a}$ (suponiendo $a > 0$):
$$\left(1 + \frac{a}{n}\right)^n = \left[\left(1 + \frac{1}{m}\right)^m\right]^a$$

Cuando $n \to \infty$, también $m \to \infty$. Por lo tanto:
$$\lim_{n \to \infty} \left(1 + \frac{a}{n}\right)^n = \left[\lim_{m \to \infty} \left(1 + \frac{1}{m}\right)^m\right]^a = e^a$$

**Límite 8 (Logaritmo):**
$$\lim_{n \to \infty} \frac{\ln(n)}{n} = 0$$

**Justificación:** El logaritmo crece **mucho más lento** que cualquier potencia positiva de $n$.

**Límite 9:**
$$\lim_{n \to \infty} \frac{\ln(n)}{n^p} = 0, \quad \forall p > 0$$

**Resumen - Jerarquía de Crecimiento:**
Ordenando de crecimiento más lento a más rápido:
$$\ln(n) \ll n^p \ll a^n \ll n! \ll n^n$$

donde $p > 0$ y $a > 1$. El símbolo $\ll$ significa "crece muchísimo más lento que".

### 4.5 Técnicas de Cálculo de Límites

En la práctica, raramente usamos la definición $\epsilon-N$ directamente. En su lugar, aplicamos teoremas, propiedades algebraicas y técnicas sistemáticas.

#### 4.5.1 Indeterminaciones

Cuando intentamos calcular un límite aplicando las reglas algebraicas, a veces obtenemos expresiones de la forma:
$$\frac{\infty}{\infty}, \quad \infty - \infty, \quad 0 \cdot \infty, \quad 1^\infty, \quad 0^0, \quad \infty^0$$

Estas se llaman **formas indeterminadas** porque no podemos concluir el valor del límite sin más análisis. Cada caso requiere técnicas específicas.

#### 4.5.2 Técnica 1: División por la Mayor Potencia

**Aplicación:** Límites de cocientes de polinomios o funciones racionales.

**Estrategia:** Dividir numerador y denominador por la mayor potencia de $n$ que aparezca.

**Ejemplo 4.6:**
Calcular $\lim_{n \to \infty} \frac{3n^2 + 5n - 1}{2n^2 - 7}$.

**Solución:**
La mayor potencia es $n^2$. Dividimos numerador y denominador por $n^2$:
$$\lim_{n \to \infty} \frac{3n^2 + 5n - 1}{2n^2 - 7} = \lim_{n \to \infty} \frac{\frac{3n^2}{n^2} + \frac{5n}{n^2} - \frac{1}{n^2}}{\frac{2n^2}{n^2} - \frac{7}{n^2}}$$
$$= \lim_{n \to \infty} \frac{3 + \frac{5}{n} - \frac{1}{n^2}}{2 - \frac{7}{n^2}}$$

Aplicando las propiedades del límite y sabiendo que $\frac{1}{n} \to 0$ y $\frac{1}{n^2} \to 0$:
$$= \frac{3 + 0 - 0}{2 - 0} = \frac{3}{2}$$

**Ejemplo 4.7:**
$$\lim_{n \to \infty} \frac{5n^3 - 2n + 1}{n^4 + 3n^2}$$

**Solución:**
Dividimos por $n^4$:
$$\lim_{n \to \infty} \frac{\frac{5n^3}{n^4} - \frac{2n}{n^4} + \frac{1}{n^4}}{\frac{n^4}{n^4} + \frac{3n^2}{n^4}} = \lim_{n \to \infty} \frac{\frac{5}{n} - \frac{2}{n^3} + \frac{1}{n^4}}{1 + \frac{3}{n^2}}$$
$$= \frac{0 - 0 + 0}{1 + 0} = 0$$

**Regla general para cocientes de polinomios:**
$$\lim_{n \to \infty} \frac{a_k n^k + \cdots + a_0}{b_m n^m + \cdots + b_0} = \begin{cases}
0 & \text{si } k < m \\
\frac{a_k}{b_m} & \text{si } k = m \\
\pm \infty & \text{si } k > m
\end{cases}$$

#### 4.5.3 Técnica 2: Racionalización

**Aplicación:** Límites con raíces cuadradas que producen indeterminaciones $\infty - \infty$.

**Estrategia:** Multiplicar y dividir por el conjugado.

**Ejemplo 4.8:**
Calcular $\lim_{n \to \infty} (\sqrt{n^2 + n} - n)$.

**Solución:**
Multiplicamos por el conjugado:
$$\lim_{n \to \infty} (\sqrt{n^2 + n} - n) = \lim_{n \to \infty} \frac{(\sqrt{n^2 + n} - n)(\sqrt{n^2 + n} + n)}{\sqrt{n^2 + n} + n}$$
$$= \lim_{n \to \infty} \frac{(n^2 + n) - n^2}{\sqrt{n^2 + n} + n} = \lim_{n \to \infty} \frac{n}{\sqrt{n^2 + n} + n}$$

Dividimos numerador y denominador por $n$:
$$= \lim_{n \to \infty} \frac{1}{\sqrt{1 + \frac{1}{n}} + 1} = \frac{1}{\sqrt{1 + 0} + 1} = \frac{1}{2}$$

**Ejemplo 4.9:**
$$\lim_{n \to \infty} (\sqrt{n^2 + 3n} - \sqrt{n^2 - 2n})$$

**Solución:**
$$= \lim_{n \to \infty} \frac{(n^2 + 3n) - (n^2 - 2n)}{\sqrt{n^2 + 3n} + \sqrt{n^2 - 2n}} = \lim_{n \to \infty} \frac{5n}{\sqrt{n^2 + 3n} + \sqrt{n^2 - 2n}}$$

Dividimos por $n$:
$$= \lim_{n \to \infty} \frac{5}{\sqrt{1 + \frac{3}{n}} + \sqrt{1 - \frac{2}{n}}} = \frac{5}{1 + 1} = \frac{5}{2}$$

#### 4.5.4 Técnica 3: Criterio del Cociente

**Aplicación:** Sucesiones definidas con factoriales, potencias o productos.

**Estrategia:** Calcular $\lim_{n \to \infty} \frac{a_{n+1}}{a_n}$.

- Si el límite es $L < 1$, entonces $a_n \to 0$
- Si el límite es $L > 1$, entonces $a_n \to \infty$
- Si $L = 1$, el criterio no es concluyente

**Ejemplo 4.10:**
Calcular $\lim_{n \to \infty} \frac{2^n}{n!}$.

**Solución:**
Aplicamos el criterio del cociente:
$$\frac{a_{n+1}}{a_n} = \frac{2^{n+1}/(n+1)!}{2^n/n!} = \frac{2^{n+1} \cdot n!}{2^n \cdot (n+1)!} = \frac{2}{n+1}$$

Por lo tanto:
$$\lim_{n \to \infty} \frac{a_{n+1}}{a_n} = \lim_{n \to \infty} \frac{2}{n+1} = 0 < 1$$

Concluimos: $\lim_{n \to \infty} \frac{2^n}{n!} = 0$

**Ejemplo 4.11:**
$$\lim_{n \to \infty} \frac{n^n}{n!}$$

**Solución:**
$$\frac{a_{n+1}}{a_n} = \frac{(n+1)^{n+1}/(n+1)!}{n^n/n!} = \frac{(n+1)^{n+1} \cdot n!}{n^n \cdot (n+1)!} = \frac{(n+1)^n}{n^n} = \left(\frac{n+1}{n}\right)^n = \left(1 + \frac{1}{n}\right)^n$$

Sabemos que:
$$\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e \approx 2.718 > 1$$

Por lo tanto, $\lim_{n \to \infty} \frac{n^n}{n!} = +\infty$ (diverge a infinito)

#### 4.5.5 Técnica 4: Teorema del Sándwich

**Aplicación:** Cuando podemos acotar la sucesión entre dos sucesiones con el mismo límite.

**Ejemplo 4.12:**
$$\lim_{n \to \infty} \frac{\cos(n^2)}{n}$$

**Solución:**
Sabemos que $-1 \leq \cos(n^2) \leq 1$. Dividiendo por $n > 0$:
$$-\frac{1}{n} \leq \frac{\cos(n^2)}{n} \leq \frac{1}{n}$$

Como $\lim_{n \to \infty} -\frac{1}{n} = 0$ y $\lim_{n \to \infty} \frac{1}{n} = 0$, por el Sándwich:
$$\lim_{n \to \infty} \frac{\cos(n^2)}{n} = 0$$

**Ejemplo 4.13:**
$$\lim_{n \to \infty} \frac{n! + 2^n}{n! + 3^n}$$

**Solución:**
Para $n$ grande, $n!$ domina tanto a $2^n$ como a $3^n$. Podemos acotar:
$$\frac{n!}{n! + 3^n} \leq \frac{n! + 2^n}{n! + 3^n} \leq \frac{n! + 2^n}{n!}$$

Simplificando:
$$\frac{1}{1 + \frac{3^n}{n!}} \leq \frac{n! + 2^n}{n! + 3^n} \leq 1 + \frac{2^n}{n!}$$

Como $\lim_{n \to \infty} \frac{3^n}{n!} = 0$ y $\lim_{n \to \infty} \frac{2^n}{n!} = 0$ (Límite Fundamental 4):
$$\lim_{n \to \infty} \frac{1}{1 + 0} = 1 \quad \text{y} \quad \lim_{n \to \infty} (1 + 0) = 1$$

Por el Sándwich: $\lim_{n \to \infty} \frac{n! + 2^n}{n! + 3^n} = 1$

#### 4.5.6 Técnica 5: Comparación de Órdenes de Crecimiento

**Principio:** En sumas o productos, el término de mayor crecimiento domina.

**Ejemplo 4.14:**
$$\lim_{n \to \infty} \frac{2^n + 3^n + n^{100}}{3^n + n^{50}}$$

**Solución:**
El término dominante en el numerador es $3^n$ (exponencial domina potencia).
El término dominante en el denominador es $3^n$.

Dividimos numerador y denominador por $3^n$:
$$\lim_{n \to \infty} \frac{\frac{2^n}{3^n} + 1 + \frac{n^{100}}{3^n}}{1 + \frac{n^{50}}{3^n}}$$

Aplicando los límites fundamentales:
- $\lim_{n \to \infty} \left(\frac{2}{3}\right)^n = 0$ (progresión geométrica con $|r| < 1$)
- $\lim_{n \to \infty} \frac{n^{100}}{3^n} = 0$ (Límite Fundamental 6)
- $\lim_{n \to \infty} \frac{n^{50}}{3^n} = 0$ (Límite Fundamental 6)

Por lo tanto:
$$\lim_{n \to \infty} \frac{0 + 1 + 0}{1 + 0} = 1$$

**Ejemplo 4.15:**
$$\lim_{n \to \infty} \frac{\ln(n) + \sqrt{n}}{n}$$

**Solución:**
El término dominante en el numerador es $\sqrt{n} = n^{1/2}$.
Dividimos por $n$:
$$\lim_{n \to \infty} \left(\frac{\ln(n)}{n} + \frac{\sqrt{n}}{n}\right) = \lim_{n \to \infty} \left(\frac{\ln(n)}{n} + \frac{1}{\sqrt{n}}\right)$$

Aplicando los límites fundamentales:
$$= 0 + 0 = 0$$

#### 4.5.7 Técnica 6: Sustituciones y Cambios de Variable

**Ejemplo 4.16:**
Calcular $\lim_{n \to \infty} \left(1 + \frac{3}{n}\right)^{2n}$.

**Solución:**
Usamos la identidad $a^{bc} = (a^b)^c$ y el Límite Fundamental 7:
$$\left(1 + \frac{3}{n}\right)^{2n} = \left[\left(1 + \frac{3}{n}\right)^n\right]^2$$

Por el Límite Fundamental 7 (generalización):
$$\lim_{n \to \infty} \left(1 + \frac{3}{n}\right)^n = e^3$$

Por lo tanto:
$$\lim_{n \to \infty} \left(1 + \frac{3}{n}\right)^{2n} = (e^3)^2 = e^6$$

**Ejemplo 4.17:**
$$\lim_{n \to \infty} \left(\frac{n+1}{n}\right)^n$$

**Solución:**
Reescribimos:
$$\left(\frac{n+1}{n}\right)^n = \left(1 + \frac{1}{n}\right)^n$$

Por el Límite Fundamental 7:
$$\lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = e$$

**Ejemplo 4.18:**
$$\lim_{n \to \infty} \left(\frac{n}{n+2}\right)^n$$

**Solución:**
Reescribimos invirtiendo la fracción:
$$\left(\frac{n}{n+2}\right)^n = \left(\frac{1}{1 + \frac{2}{n}}\right)^n = \frac{1}{\left(1 + \frac{2}{n}\right)^n}$$

Por el Límite Fundamental 7:
$$\lim_{n \to \infty} \left(1 + \frac{2}{n}\right)^n = e^2$$

Por lo tanto:
$$\lim_{n \to \infty} \left(\frac{n}{n+2}\right)^n = \frac{1}{e^2} = e^{-2}$$

**Ejemplo 4.19 (Combinando técnicas):**
$$\lim_{n \to \infty} \frac{n^2 \cdot 2^n}{3^n + n^3}$$

**Solución:**
El término dominante en el denominador es $3^n$. Dividimos por $3^n$:
$$\lim_{n \to \infty} \frac{n^2 \cdot 2^n}{3^n + n^3} = \lim_{n \to \infty} \frac{n^2 \cdot \left(\frac{2}{3}\right)^n}{1 + \frac{n^3}{3^n}}$$

Usando $\frac{n^3}{3^n} \to 0$:
$$= \lim_{n \to \infty} n^2 \cdot \left(\frac{2}{3}\right)^n$$

Aunque $n^2 \to \infty$, la exponencial $\left(\frac{2}{3}\right)^n \to 0$ más rápido. Usando el criterio del cociente o dominancia:
$$\lim_{n \to \infty} n^2 \cdot \left(\frac{2}{3}\right)^n = 0$$

**Ejemplo 4.20:**
$$\lim_{n \to \infty} \sqrt[n]{n^2 + 3^n}$$

**Solución:**
Extraemos el término dominante:
$$\sqrt[n]{n^2 + 3^n} = \sqrt[n]{3^n\left(\frac{n^2}{3^n} + 1\right)} = 3 \cdot \sqrt[n]{\frac{n^2}{3^n} + 1}$$

Como $\frac{n^2}{3^n} \to 0$:
$$\lim_{n \to \infty} \sqrt[n]{\frac{n^2}{3^n} + 1} = \sqrt[n]{1} = 1$$

Por lo tanto:
$$\lim_{n \to \infty} \sqrt[n]{n^2 + 3^n} = 3 \cdot 1 = 3$$

---

## 5. Subsucesiones

Las subsucesiones permiten estudiar el comportamiento de una sucesión "seleccionando" ciertos términos, manteniendo el orden original.

### 5.1 Definición

**Definición 5.1 (Subsucesión):**
Sea $(a_n)$ una sucesión. Una **subsucesión** de $(a_n)$ es una sucesión $(a_{n_k})$ obtenida al seleccionar términos de $(a_n)$ en orden creciente de índices.

Formalmente, existe una función estrictamente creciente $k: \mathbb{N} \to \mathbb{N}$ tal que:
$$n_1 < n_2 < n_3 < \cdots$$

y la subsucesión es:
$$(a_{n_k}) = a_{n_1}, a_{n_2}, a_{n_3}, \dots$$

**Observación:** Como $k$ es estrictamente creciente, necesariamente $n_k \geq k$ para todo $k \in \mathbb{N}$.

**Ejemplo 5.1:**
Sea $(a_n) = 1, \frac{1}{2}, \frac{1}{3}, \frac{1}{4}, \frac{1}{5}, \frac{1}{6}, \dots$ (es decir, $a_n = \frac{1}{n}$).

**Subsucesiones:**
1. **Términos pares:** $(a_{2k}) = \frac{1}{2}, \frac{1}{4}, \frac{1}{6}, \dots$ con $n_k = 2k$
2. **Términos impares:** $(a_{2k-1}) = 1, \frac{1}{3}, \frac{1}{5}, \dots$ con $n_k = 2k-1$
3. **Cuadrados perfectos:** $(a_{k^2}) = 1, \frac{1}{4}, \frac{1}{9}, \frac{1}{16}, \dots$ con $n_k = k^2$

**Ejemplo 5.2:**
Sea $(a_n) = (-1)^n$, es decir: $-1, 1, -1, 1, -1, 1, \dots$

**Subsucesiones:**
1. **Términos pares:** $(a_{2k}) = 1, 1, 1, \dots$ (sucesión constante igual a 1)
2. **Términos impares:** $(a_{2k-1}) = -1, -1, -1, \dots$ (sucesión constante igual a -1)

### 5.2 Teoremas sobre Subsucesiones

**Teorema 5.1 (Subsucesiones de Sucesiones Convergentes):**
Si $(a_n)$ converge a $L$, entonces **toda** subsucesión $(a_{n_k})$ también converge a $L$.

**Demostración:**
Sea $\epsilon > 0$ arbitrario. Como $a_n \to L$, existe $N \in \mathbb{N}$ tal que:
$$\forall n \geq N \implies |a_n - L| < \epsilon$$

Como $n_k$ es estrictamente creciente, $n_k \geq k$ para todo $k$. Por lo tanto, para $k \geq N$:
$$n_k \geq k \geq N$$

Esto implica que:
$$|a_{n_k} - L| < \epsilon$$

Por definición, $(a_{n_k}) \to L$. $\square$

**Corolario 5.1 (Criterio de Divergencia):**
Si $(a_n)$ tiene dos subsucesiones que convergen a límites diferentes, entonces $(a_n)$ es divergente.

**Demostración:**
Supongamos que $(a_n)$ converge a algún $L$. Por el Teorema 5.1, todas las subsucesiones convergen a $L$. Pero por hipótesis, existen dos subsucesiones que convergen a límites diferentes, lo cual contradice la unicidad del límite. Por lo tanto, $(a_n)$ no puede converger. $\square$

**Ejemplo 5.3 (Aplicación del Corolario):**
Probar que $a_n = (-1)^n$ no converge.

**Solución:**
- La subsucesión de términos pares: $a_{2k} = 1 \to 1$
- La subsucesión de términos impares: $a_{2k-1} = -1 \to -1$

Como $1 \neq -1$, por el Corolario 5.1, $(a_n)$ no converge.

**Ejemplo 5.4:**
Consideremos $a_n = \sin\left(\frac{n\pi}{2}\right)$.

Los primeros términos son: $\sin\left(\frac{\pi}{2}\right) = 1, \sin(\pi) = 0, \sin\left(\frac{3\pi}{2}\right) = -1, \sin(2\pi) = 0, 1, 0, -1, 0, \dots$

La sucesión es periódica con período 4: $1, 0, -1, 0, 1, 0, -1, 0, \dots$

**Subsucesiones:**
- $a_{4k-3} = 1, 1, 1, \dots \to 1$
- $a_{4k-1} = -1, -1, -1, \dots \to -1$

Como hay subsucesiones que convergen a límites diferentes, $(a_n)$ no converge.

### 5.3 Teorema de Bolzano-Weierstrass

**Teorema 5.2 (Bolzano-Weierstrass):**
Toda sucesión acotada tiene al menos una subsucesión convergente.

**Observación:** Este es uno de los teoremas fundamentales del Análisis Real. Su demostración completa requiere conceptos topológicos avanzados (compacidad, cubrimientos), pero presentamos la idea intuitiva.

**Idea de la demostración (bosquejo):**
Si $(a_n)$ está acotada, todos sus términos están en algún intervalo cerrado $[a, b]$. 

1. Dividimos $[a, b]$ en dos mitades. Al menos una de ellas contiene infinitos términos de la sucesión.
2. Seleccionamos esa mitad y la volvemos a dividir en dos.
3. Repetimos el proceso infinitamente.

Cada división produce un intervalo que contiene infinitos términos de $(a_n)$, y la longitud de los intervalos tiende a 0. De cada intervalo seleccionamos un término de la sucesión, construyendo así una subsucesión que converge al punto límite de los intervalos encajados.

**Ejemplo 5.5:**
La sucesión $a_n = (-1)^n$ es acotada ($|a_n| \leq 1$) pero no converge. Sin embargo, por Bolzano-Weierstrass, tiene subsucesiones convergentes:
- $a_{2k} = 1 \to 1$
- $a_{2k-1} = -1 \to -1$

**Aplicación:** Este teorema es fundamental para demostrar la existencia de máximos y mínimos de funciones continuas en intervalos cerrados.

### 5.4 Punto de Acumulación (Límite Subsecuencial)

**Definición 5.2 (Punto de acumulación):**
Un número $L \in \mathbb{R}$ es un **punto de acumulación** (o **límite subsecuencial**) de la sucesión $(a_n)$ si existe una subsucesión $(a_{n_k})$ que converge a $L$.

**Ejemplo 5.6:**
La sucesión $a_n = (-1)^n + \frac{1}{n}$ tiene términos:
$$0, \frac{3}{2}, -\frac{2}{3}, \frac{5}{4}, -\frac{4}{5}, \frac{7}{6}, \dots$$

**Puntos de acumulación:**
- $a_{2k} = 1 + \frac{1}{2k} \to 1$
- $a_{2k-1} = -1 + \frac{1}{2k-1} \to -1$

Los puntos de acumulación son $\{-1, 1\}$.

**Proposición 5.1:**
Una sucesión $(a_n)$ converge a $L$ si y solo si $L$ es su único punto de acumulación.

---

## 6. Sucesiones Recursivas y Punto Fijo

Muchas sucesiones importantes se definen recursivamente, donde cada término depende de los anteriores. El método del punto fijo permite analizar la convergencia de estas sucesiones.

### 6.1 Definición de Sucesión Recursiva

**Definición 6.1:**
Una **sucesión recursiva** (o recurrente) se define mediante:
1. Uno o más términos iniciales: $a_1, a_2, \dots, a_k$
2. Una relación de recurrencia: $a_{n+1} = f(a_n, a_{n-1}, \dots, a_{n-k+1})$

**Caso simple (orden 1):** $a_{n+1} = f(a_n)$ con $a_1$ dado.

### 6.2 Método del Punto Fijo

Para sucesiones de la forma $a_{n+1} = f(a_n)$, si la sucesión converge a algún límite $L$, entonces:
$$L = \lim_{n \to \infty} a_{n+1} = \lim_{n \to \infty} f(a_n) = f\left(\lim_{n \to \infty} a_n\right) = f(L)$$

(asumiendo que $f$ es continua)

Por lo tanto, $L$ debe ser un **punto fijo** de $f$, es decir, una solución de:
$$L = f(L)$$

**Estrategia:**
1. Encontrar los puntos fijos resolviendo $x = f(x)$
2. Determinar cuál es el límite (si existe) analizando la monotonía y acotación

**Teorema 6.1 (Convergencia a punto fijo):**
Si $f: [a,b] \to [a,b]$ es continua y:
1. $(a_n)$ está definida por $a_{n+1} = f(a_n)$ con $a_1 \in [a,b]$
2. Existe $L \in [a,b]$ punto fijo de $f$
3. $|f'(x)| < 1$ en un entorno de $L$ (condición de contracción)

Entonces $(a_n)$ converge a $L$.

### 6.3 Ejemplos de Sucesiones Recursivas

**Ejemplo 6.1:**
Sea $a_1 = 1$ y $a_{n+1} = \frac{1}{2}(a_n + 2)$. Determinar si converge y encontrar el límite.

**Solución:**

**Paso 1: Punto fijo**
Si la sucesión converge a $L$, entonces:
$$L = \frac{1}{2}(L + 2)$$
$$2L = L + 2$$
$$L = 2$$

**Paso 2: Monotonía y acotación**
Calculamos los primeros términos:
- $a_1 = 1$
- $a_2 = \frac{1}{2}(1 + 2) = 1.5$
- $a_3 = \frac{1}{2}(1.5 + 2) = 1.75$
- $a_4 = \frac{1}{2}(1.75 + 2) = 1.875$

Parece ser creciente y acotada por 2.

**Demostración por inducción que $a_n < 2$ para todo $n$:**
- **Base:** $a_1 = 1 < 2$ ✓
- **Hipótesis:** Supongamos $a_n < 2$
- **Paso inductivo:** 
  $$a_{n+1} = \frac{1}{2}(a_n + 2) < \frac{1}{2}(2 + 2) = 2$$ ✓

**Demostración de que es creciente:**
$$a_{n+1} - a_n = \frac{1}{2}(a_n + 2) - a_n = \frac{1}{2}(2 - a_n)$$

Como $a_n < 2$, tenemos $2 - a_n > 0$, por lo tanto $a_{n+1} - a_n > 0$, es decir, $a_{n+1} > a_n$.

**Paso 3: Conclusión**
La sucesión es creciente y acotada superiormente. Por el Teorema de Convergencia Monótona, converge a su supremo. El único punto fijo es $L = 2$.

**Respuesta:** $\lim_{n \to \infty} a_n = 2$

**Ejemplo 6.2:**
Sea $a_1 = 1$ y $a_{n+1} = \sqrt{2 + a_n}$. Determinar si converge y encontrar el límite.

**Solución:**

**Paso 1: Punto fijo**
$$L = \sqrt{2 + L}$$
$$L^2 = 2 + L$$
$$L^2 - L - 2 = 0$$
$$(L-2)(L+1) = 0$$

Soluciones: $L = 2$ o $L = -1$. Como $a_n > 0$ para todo $n$ (raíz cuadrada), el candidato es $L = 2$.

**Paso 2: Acotación**
Calculamos los primeros términos:
- $a_1 = 1$
- $a_2 = \sqrt{2 + 1} = \sqrt{3} \approx 1.732$
- $a_3 = \sqrt{2 + \sqrt{3}} \approx 1.931$
- $a_4 \approx 1.982$

**Demostración por inducción que $a_n \leq 2$:**
- **Base:** $a_1 = 1 \leq 2$ ✓
- **Hipótesis:** $a_n \leq 2$
- **Paso inductivo:**
  $$a_{n+1} = \sqrt{2 + a_n} \leq \sqrt{2 + 2} = \sqrt{4} = 2$$ ✓

**Demostración de que es creciente:**
Debemos probar que $a_{n+1} \geq a_n$, es decir:
$$\sqrt{2 + a_n} \geq a_n$$
$$2 + a_n \geq a_n^2$$
$$a_n^2 - a_n - 2 \leq 0$$
$$(a_n - 2)(a_n + 1) \leq 0$$

Como $a_n > 0$, tenemos $a_n + 1 > 0$. La desigualdad se cumple si $a_n \leq 2$, que ya demostramos.

**Paso 3: Conclusión**
La sucesión es creciente y acotada superiormente por 2. Converge a $L = 2$.

**Verificación:** $\sqrt{2 + 2} = \sqrt{4} = 2$ ✓

**Ejemplo 6.3:**
Sea $a_1 = 2$ y $a_{n+1} = \frac{1}{2}\left(a_n + \frac{2}{a_n}\right)$ (Método de Herón para $\sqrt{2}$).

**Solución:**

**Paso 1: Punto fijo**
$$L = \frac{1}{2}\left(L + \frac{2}{L}\right)$$
$$2L = L + \frac{2}{L}$$
$$L = \frac{2}{L}$$
$$L^2 = 2$$
$$L = \sqrt{2}$$ (tomamos la raíz positiva)

**Paso 2: Análisis**
Calculamos:
- $a_1 = 2$
- $a_2 = \frac{1}{2}\left(2 + \frac{2}{2}\right) = \frac{1}{2}(2 + 1) = 1.5$
- $a_3 = \frac{1}{2}\left(1.5 + \frac{2}{1.5}\right) = \frac{1}{2}(1.5 + 1.\overline{3}) \approx 1.41\overline{6}$

**Demostración que $a_n \geq \sqrt{2}$ para $n \geq 2$:**

Por la desigualdad AM-GM (media aritmética $\geq$ media geométrica):
$$a_{n+1} = \frac{1}{2}\left(a_n + \frac{2}{a_n}\right) \geq \sqrt{a_n \cdot \frac{2}{a_n}} = \sqrt{2}$$

La igualdad se da solo si $a_n = \frac{2}{a_n}$, es decir, $a_n = \sqrt{2}$.

**Demostración que es decreciente (para $n \geq 2$):**
$$a_{n+1} - a_n = \frac{1}{2}\left(a_n + \frac{2}{a_n}\right) - a_n = \frac{1}{2}\left(\frac{2}{a_n} - a_n\right) = \frac{2 - a_n^2}{2a_n}$$

Como $a_n \geq \sqrt{2}$ para $n \geq 2$, tenemos $a_n^2 \geq 2$, por lo tanto $2 - a_n^2 \leq 0$.

Entonces $a_{n+1} \leq a_n$, la sucesión es decreciente.

**Paso 3: Conclusión**
Para $n \geq 2$, la sucesión es decreciente y acotada inferiormente por $\sqrt{2}$. Converge a $L = \sqrt{2}$.

**Observación:** Este es el célebre **Método de Herón** (o método babilónico) para aproximar raíces cuadradas, que converge **muy rápidamente** (convergencia cuadrática).

**Ejemplo 6.4:**
Sea $a_1 = 1$ y $a_{n+1} = \cos(a_n)$. ¿Converge?

**Solución:**

**Paso 1: Punto fijo**
Debemos resolver $L = \cos(L)$. Esta ecuación trascendente no tiene solución algebraica cerrada, pero numéricamente: $L \approx 0.739085$.

**Paso 2: Acotación**
Como $-1 \leq \cos(x) \leq 1$ para todo $x$, la sucesión está acotada.

**Paso 3: Contracción**
La derivada de $f(x) = \cos(x)$ es $f'(x) = -\sin(x)$. Para $x$ cerca de 0.739, $|f'(x)| = |\sin(x)| < 1$.

Por el teorema del punto fijo, la sucesión converge a $L \approx 0.739085$.

**Ejemplo 6.5 (Divergencia):**
Sea $a_1 = 1$ y $a_{n+1} = 2a_n$. ¿Converge?

**Solución:**
Esta es una progresión geométrica con $r = 2$. El término general es:
$$a_n = 2^{n-1}$$

Como $2 > 1$, $\lim_{n \to \infty} a_n = +\infty$. La sucesión diverge.

**Punto fijo:** Resolviendo $L = 2L$ obtenemos $L = 0$. Sin embargo, la sucesión no converge a 0 porque la derivada $f'(x) = 2$ satisface $|f'(0)| = 2 > 1$, violando la condición de contracción.

---

## 7. Sucesiones Especiales y Completitud

## 7. Sucesiones Especiales y Completitud

### 7.1 El Número $e$

El número $e$ (base de los logaritmos naturales) es una de las constantes matemáticas más importantes, con aplicaciones en cálculo, probabilidad, finanzas y muchas otras áreas.

**Definición 7.1:**
El número $e$ se define como el límite de la sucesión:
$$e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n$$

Para que esta definición tenga sentido, debemos demostrar que la sucesión $a_n = \left(1 + \frac{1}{n}\right)^n$ converge.

**Teorema 7.1 (Existencia de $e$):**
La sucesión $a_n = \left(1 + \frac{1}{n}\right)^n$ es monótona creciente y acotada superiormente, por lo tanto converge.

**Demostración:**

**Parte 1: Monotonía (la sucesión es creciente)**

Usamos el **binomio de Newton**:
$$\left(1 + \frac{1}{n}\right)^n = \sum_{k=0}^{n} \binom{n}{k} \left(\frac{1}{n}\right)^k$$

Desarrollando:
$$= 1 + n \cdot \frac{1}{n} + \binom{n}{2} \frac{1}{n^2} + \binom{n}{3} \frac{1}{n^3} + \cdots + \frac{1}{n^n}$$

Recordando que $\binom{n}{k} = \frac{n!}{k!(n-k)!} = \frac{n(n-1)(n-2)\cdots(n-k+1)}{k!}$:

$$\left(1 + \frac{1}{n}\right)^n = 1 + 1 + \frac{n(n-1)}{2! \cdot n^2} + \frac{n(n-1)(n-2)}{3! \cdot n^3} + \cdots$$

Simplificando cada término:
$$= 1 + 1 + \frac{1}{2!}\left(1 - \frac{1}{n}\right) + \frac{1}{3!}\left(1 - \frac{1}{n}\right)\left(1 - \frac{2}{n}\right) + \cdots$$

Ahora consideramos $a_{n+1}$:
$$\left(1 + \frac{1}{n+1}\right)^{n+1} = 1 + 1 + \frac{1}{2!}\left(1 - \frac{1}{n+1}\right) + \frac{1}{3!}\left(1 - \frac{1}{n+1}\right)\left(1 - \frac{2}{n+1}\right) + \cdots$$

Comparando término a término:
- Los dos primeros términos son iguales: $1 + 1$
- Para $k \geq 2$, en $a_n$ el término $k$-ésimo contiene factores $\left(1 - \frac{j}{n}\right)$
- En $a_{n+1}$ contiene factores $\left(1 - \frac{j}{n+1}\right)$
- Como $\frac{j}{n+1} < \frac{j}{n}$, tenemos $1 - \frac{j}{n+1} > 1 - \frac{j}{n}$
- Además, $a_{n+1}$ tiene **un término adicional** (de orden $n+1$)

Por lo tanto, $a_{n+1} > a_n$, la sucesión es **estrictamente creciente**.

**Parte 2: Acotación superior**

Usando la expansión binomial y observando que:
$$\left(1 - \frac{1}{n}\right)\left(1 - \frac{2}{n}\right) \cdots \left(1 - \frac{k-1}{n}\right) < 1$$

Tenemos:
$$\left(1 + \frac{1}{n}\right)^n < 1 + 1 + \frac{1}{2!} + \frac{1}{3!} + \cdots + \frac{1}{n!}$$

Ahora acotamos cada factorial. Observemos que para $k \geq 2$:
$$k! = k \cdot (k-1) \cdot (k-2) \cdots 2 \cdot 1 \geq 2 \cdot 2 \cdot 2 \cdots 2 = 2^{k-1}$$

(excepto los primeros términos). Más precisamente:
$$k! \geq 2^{k-1} \quad \text{para } k \geq 2$$

Por lo tanto:
$$\frac{1}{k!} \leq \frac{1}{2^{k-1}}$$

Entonces:
$$\left(1 + \frac{1}{n}\right)^n < 1 + 1 + \frac{1}{2} + \frac{1}{2^2} + \frac{1}{2^3} + \cdots$$

Esta es una serie geométrica con $a_1 = 1$ y $r = \frac{1}{2}$:
$$1 + \frac{1}{2} + \frac{1}{2^2} + \cdots = \frac{1}{1 - \frac{1}{2}} = 2$$

Por lo tanto:
$$\left(1 + \frac{1}{n}\right)^n < 1 + 2 = 3$$

La sucesión está **acotada superiormente por 3**.

**Conclusión:**
Por el Teorema de Convergencia Monótona, la sucesión converge. Su límite se denota $e$. $\square$

**Valor aproximado:**
$$e \approx 2.718281828459045\dots$$

**Proposición 7.1 (Representación como serie):**
El número $e$ también se puede expresar como la suma infinita:
$$e = \sum_{k=0}^{\infty} \frac{1}{k!} = 1 + 1 + \frac{1}{2!} + \frac{1}{3!} + \frac{1}{4!} + \cdots$$

**Justificación:**
De la expansión binomial vista en la demostración:
$$\left(1 + \frac{1}{n}\right)^n = \sum_{k=0}^{n} \frac{1}{k!} \prod_{j=0}^{k-1} \left(1 - \frac{j}{n}\right)$$

Cuando $n \to \infty$:
- El número de términos crece
- Cada producto $\prod_{j=0}^{k-1} \left(1 - \frac{j}{n}\right) \to 1$ para $k$ fijo

Por lo tanto:
$$e = \lim_{n \to \infty} \left(1 + \frac{1}{n}\right)^n = \sum_{k=0}^{\infty} \frac{1}{k!}$$

**Propiedades del número $e$:**

1. **Irracionalidad:** $e$ es irracional (demostración de Euler, 1737)
2. **Trascendencia:** $e$ es trascendente, no es raíz de ningún polinomio con coeficientes enteros (Hermite, 1873)
3. **Relación con logaritmos:** $\ln(e) = 1$, es la base del logaritmo natural
4. **Derivada:** La función $f(x) = e^x$ es su propia derivada: $\frac{d}{dx}e^x = e^x$
5. **Fórmula de Euler:** $e^{i\pi} + 1 = 0$ (conecta $e$, $i$, $\pi$, 1 y 0)

**Aplicaciones:**
- **Cálculo:** Derivadas e integrales de funciones exponenciales
- **Interés compuesto continuo:** $A = Pe^{rt}$
- **Probabilidad:** Distribución de Poisson, distribución normal
- **Crecimiento exponencial:** Poblaciones, desintegración radiactiva

**Ejemplo 7.1:**
Calcular $\lim_{n \to \infty} \left(1 + \frac{2}{n}\right)^n$.

**Solución:**
Usando la sustitución $m = \frac{n}{2}$:
$$\left(1 + \frac{2}{n}\right)^n = \left[\left(1 + \frac{1}{m}\right)^m\right]^2$$

Cuando $n \to \infty$, también $m \to \infty$. Por lo tanto:
$$\lim_{n \to \infty} \left(1 + \frac{2}{n}\right)^n = \left(\lim_{m \to \infty} \left(1 + \frac{1}{m}\right)^m\right)^2 = e^2$$

**Ejemplo 7.2:**
Calcular $\lim_{n \to \infty} \left(\frac{n+1}{n}\right)^n$.

**Solución:**
$$\left(\frac{n+1}{n}\right)^n = \left(1 + \frac{1}{n}\right)^n \to e$$

### 7.2 Sucesión de Fibonacci y la Razón Áurea

La sucesión de Fibonacci es una de las más famosas en matemáticas, con aplicaciones en naturaleza, arte, arquitectura y teoría de números.

**Definición 7.2:**
La **sucesión de Fibonacci** se define recursivamente por:
$$F_0 = 0, \quad F_1 = 1, \quad F_n = F_{n-1} + F_{n-2}, \quad \forall n \geq 2$$

**Primeros términos:**
$$0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, \dots$$

**Observación:** Esta es una ecuación en diferencias lineal de segundo orden homogénea con coeficientes constantes.

#### 7.2.1 Fórmula de Binet (Término General)

Aunque Fibonacci está definida recursivamente, existe una fórmula cerrada para el término $n$-ésimo.

**Teorema 7.2 (Fórmula de Binet):**
$$F_n = \frac{\varphi^n - \psi^n}{\sqrt{5}}$$

donde:
- $\varphi = \frac{1 + \sqrt{5}}{2} \approx 1.618$ (la **razón áurea**)
- $\psi = \frac{1 - \sqrt{5}}{2} \approx -0.618$

**Demostración (método de la ecuación característica):**

Buscamos soluciones de la forma $F_n = r^n$. Sustituyendo en la recurrencia:
$$r^n = r^{n-1} + r^{n-2}$$

Dividiendo por $r^{n-2}$ (asumiendo $r \neq 0$):
$$r^2 = r + 1$$
$$r^2 - r - 1 = 0$$

Esta es la **ecuación característica**. Usando la fórmula cuadrática:
$$r = \frac{1 \pm \sqrt{1 + 4}}{2} = \frac{1 \pm \sqrt{5}}{2}$$

Obtenemos las dos raíces $\varphi$ y $\psi$. La solución general es una combinación lineal:
$$F_n = A\varphi^n + B\psi^n$$

Usando las condiciones iniciales:
- $F_0 = 0$: $A + B = 0 \implies B = -A$
- $F_1 = 1$: $A\varphi + B\psi = 1$

Sustituyendo $B = -A$:
$$A(\varphi - \psi) = 1$$
$$A = \frac{1}{\varphi - \psi} = \frac{1}{\frac{1+\sqrt{5}}{2} - \frac{1-\sqrt{5}}{2}} = \frac{1}{\sqrt{5}}$$

Por lo tanto:
$$F_n = \frac{1}{\sqrt{5}}(\varphi^n - \psi^n)$$ $\square$

#### 7.2.2 Razón Áurea

**Definición 7.3 (Razón áurea):**
La **razón áurea** (o número áureo) $\varphi$ es el número positivo que satisface:
$$\varphi^2 = \varphi + 1$$

Explícitamente:
$$\varphi = \frac{1 + \sqrt{5}}{2} \approx 1.618033988749\dots$$

**Propiedad geométrica:**
Un rectángulo con lados en proporción $\varphi:1$ se considera estéticamente "perfecto" (rectángulo áureo).

**Teorema 7.3 (Límite de cocientes de Fibonacci):**
La sucesión de cocientes de términos consecutivos de Fibonacci converge a la razón áurea:
$$\lim_{n \to \infty} \frac{F_{n+1}}{F_n} = \varphi$$

**Demostración:**
Usando la fórmula de Binet:
$$\frac{F_{n+1}}{F_n} = \frac{\varphi^{n+1} - \psi^{n+1}}{\varphi^n - \psi^n} = \frac{\varphi^{n+1}\left(1 - \left(\frac{\psi}{\varphi}\right)^{n+1}\right)}{\varphi^n\left(1 - \left(\frac{\psi}{\varphi}\right)^n\right)}$$

Simplificando:
$$= \varphi \cdot \frac{1 - \left(\frac{\psi}{\varphi}\right)^{n+1}}{1 - \left(\frac{\psi}{\varphi}\right)^n}$$

Como $|\psi| < 1$ y $|\varphi| > 1$, tenemos $\left|\frac{\psi}{\varphi}\right| < 1$. Por lo tanto:
$$\lim_{n \to \infty} \left(\frac{\psi}{\varphi}\right)^n = 0$$

Entonces:
$$\lim_{n \to \infty} \frac{F_{n+1}}{F_n} = \varphi \cdot \frac{1 - 0}{1 - 0} = \varphi$$ $\square$

**Cálculos numéricos:**
- $\frac{F_2}{F_1} = \frac{1}{1} = 1$
- $\frac{F_3}{F_2} = \frac{2}{1} = 2$
- $\frac{F_4}{F_3} = \frac{3}{2} = 1.5$
- $\frac{F_5}{F_4} = \frac{5}{3} \approx 1.\overline{6}$
- $\frac{F_6}{F_5} = \frac{8}{5} = 1.6$
- $\frac{F_7}{F_6} = \frac{13}{8} = 1.625$
- $\frac{F_{10}}{F_9} = \frac{55}{34} \approx 1.6176$
- $\frac{F_{20}}{F_{19}} \approx 1.6180327$

#### 7.2.3 Propiedades de Fibonacci

**Proposición 7.2 (Identidad de Cassini):**
$$F_{n+1}F_{n-1} - F_n^2 = (-1)^n$$

**Proposición 7.3 (Suma de Fibonacci):**
$$\sum_{k=1}^{n} F_k = F_{n+2} - 1$$

**Proposición 7.4 (MCD de Fibonacci):**
$$\gcd(F_n, F_m) = F_{\gcd(n,m)}$$

**Aplicaciones en la naturaleza:**
- Espirales en conchas de caracol (espiral de Fibonacci)
- Disposición de hojas en plantas (filotaxis)
- Pétalos de flores (muchas tienen 5, 8, 13, 21 pétalos)
- Piñas y girasoles (semillas dispuestas en espirales de Fibonacci)

### 7.3 Sucesiones de Cauchy
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




