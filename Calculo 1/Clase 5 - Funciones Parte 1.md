# Funciones Parte 1

## 1. Relaciones y funciones

### 1.1 Producto cartesiano y relaciones

**Definición 1.1 (Producto cartesiano):**
Dados dos conjuntos $A$ y $B$, el **producto cartesiano** $A \times B$ es:
$$A \times B = \{(a, b) : a \in A, \, b \in B\}$$
**Ejemplo 1.1:**
Si $A = \{1, 2\}$ y $B = \{x, y, z\}$, entonces:
$$A \times B = \{(1,x), (1,y), (1,z), (2,x), (2,y), (2,z)\}$$
**Definición 1.2 (Relación):**
Una **relación** $R$ de $A$ en $B$ es cualquier subconjunto de $A \times B$:
$$R \subseteq A \times B$$
Si $(a, b) \in R$, decimos que "$a$ está relacionado con $b$" y escribimos $aRb$.

**Ejemplo 1.2:**
Sea $A = \{1, 2, 3\}$ y $B = \{2, 4, 6, 8\}$. La relación "$x$ divide a $y$" es:
$$R = \{(1,2), (1,4), (1,6), (1,8), (2,2), (2,4), (2,6), (2,8), (3,6)\}$$
### 1.2 Definición formal de función

**Definición 1.3 (Función):**
Una **función** $f$ de un conjunto $A$ en un conjunto $B$ es una relación que asigna a **cada elemento** de $A$ **exactamente un** elemento de $B$.
![[diagrama_funcion.png]]
**Notación:** $f: A \to B$
- $A$ es el **dominio** de $f$ (conjunto de partida)
- $B$ es el **codominio** de $f$ (conjunto de llegada)
- Si $f$ asigna $b$ a $a$, escribimos $f(a) = b$ (se lee "f de a es igual a b")

**Condición crucial:** Para cada $a \in A$, existe **uno y solo uno** $b \in B$ tal que $f(a) = b$.

**Ejemplo 1.3 (Es función):**
$$f: \{1, 2, 3\} \to \{a, b, c\}$$
$$f(1) = a, \quad f(2) = b, \quad f(3) = a$$
Esto **es** una función (cada elemento del dominio tiene exactamente una imagen).
![[ejemplo_funcion_1.png]]

**Ejemplo 1.4 (NO es función):**
$$R: \{1, 2\} \to \{a, b, c\}$$
$$R = \{(1, a), (1, b), (2, c)\}$$
Esto **no es** una función porque $1$ tiene dos imágenes: $a$ y $b$.
![[relacion_no_funcion_neon.png]]
### 1.3 Funciones de $\mathbb{R}$ en $\mathbb{R}$

**Notación estándar:** Una función $f: \mathbb{R} \to \mathbb{R}$ se expresa típicamente como:
$$y = f(x)$$
donde:
- $x$ es la **variable independiente**
- $y$ es la **variable dependiente**

### 1.3.1 Imagen y preimagen

**Concepto intuitivo:**

Cuando trabajamos con una función $f: A \to B$, surgen dos preguntas naturales:
1. **¿Qué valores de salida puede producir la función?** Esta es la idea de la **imagen** de $f$.
2. **Dado un valor de salida, ¿qué valores de entrada lo produjeron?** Esta es la idea de la **preimagen** de ese valor.

**Idea intuitiva de imagen:**
La **imagen o rango** de una función es el conjunto de todos los valores que la función **efectivamente alcanza** o "produce". Es decir, si aplicamos la función a todos los elementos del dominio, la imagen es la colección de todos los resultados obtenidos.

**Ejemplo intuitivo 1:** Considera $f: \{1, 2, 3\} \to \{a, b, c, d\}$ definida por:
$$f(1) = a, \quad f(2) = b, \quad f(3) = b$$
La imagen de $f$ es $\{a, b\}$ porque estos son los únicos valores que la función produce. Nota que $c$ y $d$ están en el codominio pero **no** en la imagen.

**Idea intuitiva de preimagen:**
La **preimagen** de un elemento $y$ del codominio es el conjunto de todos los elementos del dominio que la función "envía" a $y$. Es como preguntarse: "¿De dónde viene $y$?"

**Ejemplo intuitivo 2:** En el ejemplo anterior:
- La preimagen de $a$ es $\{1\}$ (solo el 1 produce $a$)
- La preimagen de $b$ es $\{2, 3\}$ (tanto 2 como 3 producen $b$)
- La preimagen de $c$ es $\emptyset$ (ningún elemento produce $c$)

**Definición 1.4 (Imagen y preimagen - Definición formal):**

Sea $f: A \to B$ una función.

- La **imagen** de $f$ es el conjunto:
$$\text{Im}(f) = \{y \in B : \exists x \in A, \, f(x) = y\}$$
Se lee: "La imagen de $f$ es el conjunto de todos los $y$ en $B$ tales que existe al menos un $x$ en $A$ para el cual $f(x) = y$".

Notación alternativa: $\text{Im}(f) = f(A) = \{f(x) : x \in A\}$

- La **preimagen** de un elemento $y \in B$ es el conjunto:
$$f^{-1}(\{y\}) = \{x \in A : f(x) = y\}$$
Se lee: "La preimagen de $y$ es el conjunto de todos los $x$ en $A$ tales que $f(x) = y$".

**Nota importante:** El símbolo $f^{-1}(\{y\})$ denota la **preimagen** (un conjunto), **no** necesariamente la función inversa. La preimagen siempre existe, mientras que la función inversa solo existe para funciones biyectivas.

**Observación importante (Imagen vs. Codominio):**

Es crucial distinguir entre **codominio** e **imagen**:

- **Codominio** (o conjunto de llegada): Es el conjunto $B$ en la definición $f: A \to B$. Es el conjunto que especificamos como "destino posible" de la función, **independientemente de si todos sus elementos son realmente alcanzados**.

- **Imagen** (o rango): Es el subconjunto del codominio que **efectivamente** es alcanzado por la función. Es decir, $\text{Im}(f) = \{f(x) : x \in A\}$.

**Relación:** Siempre se cumple que $\text{Im}(f) \subseteq B$ (codominio), pero no necesariamente $\text{Im}(f) = B$.

**Ejemplo ilustrativo:**
Consideremos $f: \mathbb{R} \to \mathbb{R}$ definida por $f(x) = x^2$.

- **Dominio:** $\mathbb{R}$ (todos los números reales)
- **Codominio:** $\mathbb{R}$ (especificado en la definición $f: \mathbb{R} \to \mathbb{R}$)
- **Imagen:** $[0, +\infty) = \{y \in \mathbb{R} : y \geq 0\}$ (solo números no negativos)

Observamos que $\text{Im}(f) = [0, +\infty) \subsetneq \mathbb{R}$ (la imagen es un subconjunto **propio** del codominio). Por ejemplo, $-1$ pertenece al codominio pero **no** a la imagen, ya que no existe $x \in \mathbb{R}$ tal que $x^2 = -1$.

**Terminología:**
- Si $\text{Im}(f) = B$, decimos que $f$ es **sobreyectiva** (o suryectiva).
- Si cada elemento del codominio tiene **a lo sumo** una preimagen, $f$ es **inyectiva**.
- Si $f$ es inyectiva y sobreyectiva, decimos que es **biyectiva**.

### 1.4 Determinación del dominio y rango

**Concepto intuitivo:**

Cuando trabajamos con funciones expresadas mediante fórmulas algebraicas, no siempre podemos evaluar la función en cualquier número real. Existen ciertas operaciones matemáticas que **no están definidas** para algunos valores. El dominio es precisamente el conjunto de valores donde la función "tiene sentido" o está bien definida.

**Idea intuitiva del dominio:**
El **dominio** de una función es el conjunto de todos los valores de entrada ($x$) para los cuales la función puede calcularse sin problemas. Es como preguntarse: "¿Qué números puedo sustituir en $x$ sin obtener una operación imposible?"

**Operaciones problemáticas comunes:**
1. **División por cero:** No podemos dividir entre cero
2. **Raíces pares de números negativos:** No podemos calcular $\sqrt{-4}$ en los números reales
3. **Logaritmos de números no positivos:** No podemos calcular $\ln(-5)$ o $\ln(0)$

**Ejemplo intuitivo 1:** Para $f(x) = \frac{1}{x-3}$, no podemos usar $x = 3$ porque obtendríamos $\frac{1}{0}$, que no está definido. Por lo tanto, el dominio es "todos los reales excepto 3".

**Ejemplo intuitivo 2:** Para $f(x) = \sqrt{x-2}$, necesitamos que lo que está dentro de la raíz sea no negativo: $x - 2 \geq 0$, es decir, $x \geq 2$. El dominio es $[2, +\infty)$.

#### 1.4.1 Restricciones del dominio

**Definición 1.5 (Dominio máximo):**
El **dominio máximo** (o dominio natural) de una función $f$ es el conjunto más grande de números reales para los cuales la expresión $f(x)$ está definida.

**Casos que restringen el dominio:**

**Caso 1: Denominadores**

Si $f(x)$ contiene una fracción, el denominador **no puede ser cero**.

**Procedimiento:**
1. Identificar el denominador
2. Resolver la ecuación: denominador $= 0$
3. Excluir esas soluciones del dominio

**Ejemplo 1.5:**
Para $f(x) = \frac{1}{x-3}$:
- Denominador: $x - 3$
- $x - 3 = 0 \Rightarrow x = 3$
- **Dominio:** $\text{Dom}(f) = \mathbb{R} \setminus \{3\} = (-\infty, 3) \cup (3, +\infty)$

**Ejemplo 1.6:**
Para $g(x) = \frac{x+1}{x^2-4}$:
- Denominador: $x^2 - 4$
- $x^2 - 4 = 0 \Rightarrow x^2 = 4 \Rightarrow x = \pm 2$
- **Dominio:** $\text{Dom}(g) = \mathbb{R} \setminus \{-2, 2\} = (-\infty, -2) \cup (-2, 2) \cup (2, +\infty)$

**Caso 2: Raíces pares**

Si $f(x)$ contiene $\sqrt[n]{\text{expresión}}$ con $n$ par, la expresión **debe ser no negativa**.

**Procedimiento:**
1. Identificar la expresión dentro de la raíz
2. Resolver la inecuación: expresión $\geq 0$
3. El dominio es el conjunto solución

**Ejemplo 1.7:**
Para $f(x) = \sqrt{x-2}$:
- Condición: $x - 2 \geq 0$
- $x \geq 2$
- **Dominio:** $\text{Dom}(f) = [2, +\infty)$

**Ejemplo 1.8:**
Para $h(x) = \sqrt{4-x^2}$:
- Condición: $4 - x^2 \geq 0$
- $x^2 \leq 4$
- $-2 \leq x \leq 2$
- **Dominio:** $\text{Dom}(h) = [-2, 2]$

**Caso 3: Logaritmos**

Si $f(x)$ contiene $\log_a(\text{expresión})$, la expresión **debe ser estrictamente positiva**.

**Procedimiento:**
1. Identificar la expresión dentro del logaritmo
2. Resolver la inecuación: expresión $> 0$
3. El dominio es el conjunto solución

**Ejemplo 1.9:**
Para $f(x) = \ln(x)$:
- Condición: $x > 0$
- **Dominio:** $\text{Dom}(f) = (0, +\infty)$

**Ejemplo 1.10:**
Para $f(x) = \log_2(x-5)$:
- Condición: $x - 5 > 0$
- $x > 5$
- **Dominio:** $\text{Dom}(f) = (5, +\infty)$

**Caso 4: Composición de restricciones**

Si la función tiene **múltiples** restricciones, el dominio es la **intersección** de todas las condiciones.

**Ejemplo 1.11:**
Para $f(x) = \frac{\sqrt{x-1}}{x-3}$:
- **Restricción 1 (raíz):** $x - 1 \geq 0 \Rightarrow x \geq 1$
- **Restricción 2 (denominador):** $x - 3 \neq 0 \Rightarrow x \neq 3$
- **Dominio:** $\text{Dom}(f) = [1, 3) \cup (3, +\infty)$

**Ejemplo 1.12:**
Para $g(x) = \ln\left(\frac{x+2}{x-1}\right)$:
- **Restricción (logaritmo):** $\frac{x+2}{x-1} > 0$
- Analizamos el signo:
  - Puntos críticos: $x = -2$ (numerador cero) y $x = 1$ (denominador cero)
  - Intervalos: $(-\infty, -2)$, $(-2, 1)$, $(1, +\infty)$
  - La fracción es positiva en $(-\infty, -2) \cup (1, +\infty)$
- **Dominio:** $\text{Dom}(g) = (-\infty, -2) \cup (1, +\infty)$

#### 1.4.2 Cálculo del rango o imagen

**Concepto intuitivo:**

El **rango** (o imagen) es el conjunto de todos los valores de salida ($y$) que la función efectivamente produce. A diferencia del dominio (que son los valores de entrada permitidos), el rango representa "qué valores puede alcanzar la función".

**Idea intuitiva del rango:**
Dado el dominio de una función, al evaluar $f$ en todos los valores de $x$ del dominio, obtenemos un conjunto de valores $y = f(x)$. Este conjunto es el rango.

**Métodos para calcular el rango:**

**Método 1: Análisis algebraico**

**Procedimiento:**
1. Escribir $y = f(x)$
2. Despejar $x$ en términos de $y$
3. Analizar para qué valores de $y$ la expresión de $x$ tiene sentido
4. Esos valores de $y$ forman el rango

**Ejemplo 1.13:**
Para $f(x) = x^2$ con $\text{Dom}(f) = \mathbb{R}$:

$$y = x^2$$
$$x = \pm\sqrt{y}$$

Para que $x$ sea real, necesitamos $y \geq 0$.

**Rango:** $\text{Im}(f) = [0, +\infty)$

**Ejemplo 1.14:**
Para $f(x) = \frac{1}{x}$ con $\text{Dom}(f) = \mathbb{R} \setminus \{0\}$:

$$y = \frac{1}{x}$$
$$x = \frac{1}{y}$$

Para que $x$ sea real y distinto de cero, necesitamos $y \neq 0$.

**Rango:** $\text{Im}(f) = \mathbb{R} \setminus \{0\} = (-\infty, 0) \cup (0, +\infty)$

**Método 2: Análisis de funciones conocidas**

Para funciones con formas estándar, podemos usar propiedades conocidas:

**Proposición 1.1 (Rango de funciones elementales):**

1. **Función lineal:** $f(x) = mx + b$ con $m \neq 0$
   - $\text{Im}(f) = \mathbb{R}$

2. **Función cuadrática:** $f(x) = a(x-h)^2 + k$
   - Si $a > 0$: $\text{Im}(f) = [k, +\infty)$ (parábola hacia arriba)
   - Si $a < 0$: $\text{Im}(f) = (-\infty, k]$ (parábola hacia abajo)

3. **Función raíz cuadrada:** $f(x) = \sqrt{x}$
   - $\text{Im}(f) = [0, +\infty)$

4. **Función exponencial:** $f(x) = a^x$ con $a > 0$, $a \neq 1$
   - $\text{Im}(f) = (0, +\infty)$

5. **Función logarítmica:** $f(x) = \log_a(x)$
   - $\text{Im}(f) = \mathbb{R}$

**Ejemplo 1.15:**
Para $f(x) = -2x^2 + 8x - 3$:

Primero, encontramos la forma canónica completando cuadrados:
$$f(x) = -2(x^2 - 4x) - 3$$
$$f(x) = -2(x^2 - 4x + 4 - 4) - 3$$
$$f(x) = -2((x-2)^2 - 4) - 3$$
$$f(x) = -2(x-2)^2 + 8 - 3$$
$$f(x) = -2(x-2)^2 + 5$$

Como $a = -2 < 0$, la parábola abre hacia abajo con vértice en $(2, 5)$.

**Rango:** $\text{Im}(f) = (-\infty, 5]$

**Método 3: Análisis gráfico**

Al graficar la función, el rango es la **proyección** de la gráfica sobre el eje $y$.

**Observación importante:**
Calcular el rango suele ser **más difícil** que calcular el dominio, especialmente para funciones complejas. En muchos casos, el análisis gráfico combinado con el análisis algebraico es la mejor estrategia.

**Ejemplo 1.16:**
Para $f(x) = x^2$:
- Puntos: $(-2, 4)$, $(-1, 1)$, $(0, 0)$, $(1, 1)$, $(2, 4)$, $...$
- La gráfica forma una **parábola**

### 1.5 Representación de funciones

**a) Tabla de valores:**
Una tabla de valores es una tabla donde en una sección pondremos posibles valores de la variable independiente **X** y en otra sección ponemos los correspondientes valores de la variable dependiente **Y**:

|  $x$   | $-2$ | $-1$ | $0$ | $1$ | $2$ |
| :----: | :--: | :--: | :-: | :-: | :-: |
| $f(x)$ | $4$  | $1$  | $0$ | $1$ | $4$ |

**b) Fórmula algebraica:**
Una función puede expresarse mediante una fórmula algebraica explícita, por ejemplo:
$$f(x) = x^2$$
**c) Gráfica:**
Dada una función $y = f(x)$, su gráfica es el conjunto de pares ordenados $(x, f(x))$ en el plano:
$$\text{Graf}(f) = \{(x, y) \in \mathbb{R}^2 : y = f(x), \, x \in \text{Dom}(f) \}$$
**Interpretación:** Si recorremos todos los valores de $x$ en el dominio y calculamos $y = f(x)$, obtenemos una **curva** en el plano.

**Ejemplo ilustrativo complejo:**
Consideremos la función polinómica:
$$f(x) = -0.5x^3 + 2x^2 + x - 2$$

**Cálculo de valores paso a paso:**

- Para $x = 1$:
$$f(1) = -0.5(1)^3 + 2(1)^2 + (1) - 2$$
$$f(1) = -0.5(1) + 2(1) + 1 - 2$$
$$f(1) = -0.5 + 2 + 1 - 2 = 0.5$$

- Para $x = 2$:
$$f(2) = -0.5(2)^3 + 2(2)^2 + (2) - 2$$
$$f(2) = -0.5(8) + 2(4) + 0$$
$$f(2) = -4 + 8 = 4$$

**Tabla de valores extendida:**

| $x$    | $-2$ |  $-1$  | $0$  |   $0.5$   |  $1$  | $2$ |  $3$  | $4$ |
| ------ | :--: | :----: | :--: | :-------: | :---: | :-: | :---: | :-: |
| $f(x)$ | $8$  | $-0.5$ | $-2$ | $-1.0625$ | $0.5$ | $4$ | $5.5$ | $2$ |
![[grafica_funcion_puntos.png]]
![[grafica_funcion_continua.png]]

Una forma de saber si una curva es o no una función es trazando una **recta vertical**: si la recta vertical interseca la curva en más de 1 punto, entonces la curva **no es una función**. Este criterio se conoce como la **prueba de la recta vertical**.
![[no_funcion.png]]

---

## 2. Monotonía de funciones

**Concepto intuitivo:**

Cuando observamos la gráfica de una función, podemos notar que algunas funciones "suben" a medida que avanzamos de izquierda a derecha, otras "bajan", y algunas tienen comportamientos mixtos. Esta idea intuitiva de "subir" o "bajar" es lo que formalizamos con el concepto de **monotonía**.

**Idea intuitiva de función creciente:**
Una función es **creciente** si al movernos hacia la derecha en el eje $x$ (valores mayores de $x$), los valores de la función también aumentan. Es decir, "entre más a la derecha, más arriba".

**Ejemplo visual:** La función $f(x) = 2x$ es creciente: si tomamos $x_1 = 1$ y $x_2 = 3$ (con $1 < 3$), obtenemos $f(1) = 2$ y $f(3) = 6$, donde $2 < 6$. Al aumentar $x$, aumenta $f(x)$.
![[funcion_creciente_monotona.png]]
**Idea intuitiva de función decreciente:**
Una función es **decreciente** si al movernos hacia la derecha en el eje $x$, los valores de la función disminuyen. Es decir, "entre más a la derecha, más abajo".

**Ejemplo visual:** La función $g(x) = -x$ es decreciente: si tomamos $x_1 = 1$ y $x_2 = 3$ (con $1 < 3$), obtenemos $g(1) = -1$ y $g(3) = -3$, donde $-1 > -3$. Al aumentar $x$, disminuye $g(x)$.

### 2.1 Funciones crecientes y decrecientes

**Definición 2.1 (Función creciente):**
Sea $f: D \to \mathbb{R}$ una función con dominio $D \subseteq \mathbb{R}$. Decimos que $f$ es **creciente** en $D$ si para cualesquiera $x_1, x_2 \in D$:
$$x_1 < x_2 \quad \Rightarrow \quad f(x_1) \leq f(x_2)$$

Si la desigualdad es estricta:
$$x_1 < x_2 \quad \Rightarrow \quad f(x_1) < f(x_2)$$
decimos que $f$ es **estrictamente creciente**.

**Definición 2.2 (Función decreciente):**
Decimos que $f$ es **decreciente** en $D$ si para cualesquiera $x_1, x_2 \in D$:
$$x_1 < x_2 \quad \Rightarrow \quad f(x_1) \geq f(x_2)$$

Si la desigualdad es estricta:
$$x_1 < x_2 \quad \Rightarrow \quad f(x_1) > f(x_2)$$
decimos que $f$ es **estrictamente decreciente**.

**Definición 2.3 (Función monótona):**
Una función es **monótona** si es creciente o decreciente en todo su dominio.

**Ejemplo 2.1:**
La función $f(x) = 3x + 2$ es **estrictamente creciente** en $\mathbb{R}$.

**Demostración:** Sean $x_1, x_2 \in \mathbb{R}$ con $x_1 < x_2$.
$$f(x_1) = 3x_1 + 2$$
$$f(x_2) = 3x_2 + 2$$

Como $x_1 < x_2$, multiplicando por $3 > 0$:
$$3x_1 < 3x_2$$

Sumando $2$ a ambos lados:
$$3x_1 + 2 < 3x_2 + 2$$
$$f(x_1) < f(x_2)$$

Por lo tanto, $f$ es estrictamente creciente. $\square$

**Ejemplo 2.2:**
La función $g(x) = -2x + 5$ es **estrictamente decreciente** en $\mathbb{R}$.

**Demostración:** Sean $x_1, x_2 \in \mathbb{R}$ con $x_1 < x_2$.
$$g(x_1) = -2x_1 + 5$$
$$g(x_2) = -2x_2 + 5$$

Como $x_1 < x_2$, multiplicando por $-2 < 0$ (invierte la desigualdad):
$$-2x_1 > -2x_2$$

Sumando $5$ a ambos lados:
$$-2x_1 + 5 > -2x_2 + 5$$
$$g(x_1) > g(x_2)$$

Por lo tanto, $g$ es estrictamente decreciente. $\square$

**Ejemplo 2.3:**
La función $h(x) = x^2$ **no es monótona** en $\mathbb{R}$.

- En $(-\infty, 0]$ es decreciente: $-3 < -1$ pero $h(-3) = 9 > h(-1) = 1$
- En $[0, +\infty)$ es creciente: $1 < 3$ y $h(1) = 1 < h(3) = 9$

### 2.2 Intervalos de monotonía

**Definición 2.4 (Intervalo de crecimiento/decrecimiento):**
Un **intervalo de crecimiento** de $f$ es un intervalo $I \subseteq \text{Dom}(f)$ donde $f$ es creciente.

Un **intervalo de decrecimiento** de $f$ es un intervalo $I \subseteq \text{Dom}(f)$ donde $f$ es decreciente.

**Ejemplo 2.4:**
Para $f(x) = x^2$:
- **Intervalo de decrecimiento:** $(-\infty, 0]$
- **Intervalo de crecimiento:** $[0, +\infty)$

**Ejemplo 2.5:**
Para $f(x) = -x^2 + 4x + 1 = -(x-2)^2 + 5$ (parábola con vértice en $(2, 5)$ que abre hacia abajo):
- **Intervalo de crecimiento:** $(-\infty, 2]$
- **Intervalo de decrecimiento:** $[2, +\infty)$

### 2.3 Propiedades de la monotonía

**Proposición 2.1 (Monotonía de funciones lineales):**
Sea $f(x) = mx + b$ con $m \neq 0$:
- Si $m > 0$, entonces $f$ es estrictamente creciente
- Si $m < 0$, entonces $f$ es estrictamente decreciente

**Proposición 2.2 (Monotonía de funciones cuadráticas):**
Sea $f(x) = a(x-h)^2 + k$ con $a \neq 0$:
- Si $a > 0$:
  - $f$ es decreciente en $(-\infty, h]$
  - $f$ es creciente en $[h, +\infty)$
- Si $a < 0$:
  - $f$ es creciente en $(-\infty, h]$
  - $f$ es decreciente en $[h, +\infty)$

**Proposición 2.3 (Monotonía de funciones elementales):**

1. **Función exponencial** $f(x) = a^x$ con $a > 0$, $a \neq 1$:
   - Si $a > 1$: estrictamente creciente en $\mathbb{R}$
   - Si $0 < a < 1$: estrictamente decreciente en $\mathbb{R}$

2. **Función logarítmica** $f(x) = \log_a(x)$ con $a > 1$:
   - Estrictamente creciente en $(0, +\infty)$

3. **Función raíz cuadrada** $f(x) = \sqrt{x}$:
   - Estrictamente creciente en $[0, +\infty)$

**Ejemplo 2.6:**
Analizar la monotonía de $f(x) = 2^x$:

Como $2 > 1$, por la Proposición 2.3, $f$ es estrictamente creciente en $\mathbb{R}$.

**Verificación numérica:**
- $f(1) = 2^1 = 2$
- $f(2) = 2^2 = 4$
- $f(3) = 2^3 = 8$

Efectivamente: $1 < 2 < 3$ y $2 < 4 < 8$.

### 2.4 Funciones acotadas

**Concepto intuitivo:**

Algunas funciones tienen valores que "no se escapan" por arriba o por abajo. Por ejemplo, la función $\sin(x)$ siempre está entre $-1$ y $1$, nunca toma valores fuera de ese rango. Decimos que está **acotada**.

**Definición 2.5 (Función acotada superiormente):**
Una función $f: D \to \mathbb{R}$ está **acotada superiormente** si existe $M \in \mathbb{R}$ tal que:
$$f(x) \leq M \quad \text{para todo } x \in D$$

El número $M$ se llama **cota superior** de $f$.

**Definición 2.6 (Función acotada inferiormente):**
Una función $f: D \to \mathbb{R}$ está **acotada inferiormente** si existe $m \in \mathbb{R}$ tal que:
$$f(x) \geq m \quad \text{para todo } x \in D$$

El número $m$ se llama **cota inferior** de $f$.

**Definición 2.7 (Función acotada):**
Una función $f$ está **acotada** si está acotada tanto superior como inferiormente. Equivalentemente, si existe $K > 0$ tal que:
$$|f(x)| \leq K \quad \text{para todo } x \in D$$

**Ejemplo 2.7:**
La función $f(x) = x^2$ en $\mathbb{R}$:
- Está **acotada inferiormente** por $0$: $f(x) = x^2 \geq 0$ para todo $x \in \mathbb{R}$
- **No está acotada superiormente**: para cualquier $M$, podemos encontrar $x$ tal que $x^2 > M$ (por ejemplo, $x = \sqrt{M+1}$)

**Ejemplo 2.8:**
La función $g(x) = \frac{1}{1+x^2}$:
- Está **acotada superiormente** por $1$: $g(x) = \frac{1}{1+x^2} \leq 1$ (ya que $1+x^2 \geq 1$)
- Está **acotada inferiormente** por $0$: $g(x) = \frac{1}{1+x^2} > 0$ (siempre positiva)
- Por lo tanto, $g$ está **acotada**: $0 < g(x) \leq 1$ para todo $x \in \mathbb{R}$

**Ejemplo 2.9:**
La función exponencial $f(x) = e^x$:
- Está **acotada inferiormente** por $0$: $e^x > 0$ para todo $x \in \mathbb{R}$
- **No está acotada superiormente**: $\lim_{x \to +\infty} e^x = +\infty$

**Observación importante:**
Las funciones **periódicas** como $\sin(x)$ y $\cos(x)$ suelen estar acotadas:
- $-1 \leq \sin(x) \leq 1$ para todo $x \in \mathbb{R}$
- $-1 \leq \cos(x) \leq 1$ para todo $x \in \mathbb{R}$

---

## 3. Función lineal y afín

### 3.1 Definición

**Definición 3.1 (Función lineal):**
Una **función lineal** tiene la forma:
$$f(x) = mx$$
donde $m \in \mathbb{R}$ es una constante llamada **pendiente**.

**Definición 3.2 (Función afín):**
Una **función afín** tiene la forma:
$$f(x) = mx + b$$
donde:
- $m$ es la **pendiente**
- $b$ es la **ordenada al origen** (intersección con el eje Y)

**Observación:** La gráfica de una función afín es siempre una **recta**.

### 3.2 Pendiente de una recta

**Definición 3.3 (Pendiente):**
La **pendiente** $m$ de la recta que pasa por los puntos $(x_1, y_1)$ y $(x_2, y_2)$ es:
$$m = \frac{y_2 - y_1}{x_2 - x_1} = \frac{\Delta y}{\Delta x}$$

**Interpretación:** La pendiente mide la **tasa de cambio** de $y$ respecto a $x$, o "cuánto sube o baja la recta por cada unidad que avanzamos horizontalmente".

**Clasificación por pendiente:**

| Pendiente       | Descripción | Gráfica |
| --------------- | ----------- | ------- |
| $m > 0$         | Creciente   | /       |
| $m = 0$         | Horizontal  | —       |
| $m < 0$         | Decreciente | \       |
| $m$ no definida | Vertical    | \|      |

**Observación:** La pendiente conecta directamente con la monotonía (§2): una función afín es estrictamente creciente si $m > 0$ y estrictamente decreciente si $m < 0$. Para la fórmula de pendiente, ejemplos y ecuaciones de la recta, ver **Clase 4 - Geometría Analítica**, secciones 4.2–4.6.
### 3.3 De la ecuación general a la función lineal

Una **recta** en el plano puede describirse de dos formas distintas:

- **Geométricamente** (Clase 4): mediante su ecuación general $Ax + By + C = 0$
- **Funcionalmente** (esta clase): mediante $f(x) = mx + b$, donde $y = f(x)$

El paso de una forma a la otra es sencillo: si $B \neq 0$, basta despejar $y$:

$$Ax + By + C = 0 \quad \xrightarrow{\text{despejar } y} \quad y=f(x) = -\frac{A}{B}x - \frac{C}{B}$$

**Ejemplo:**
La recta $2x - 3y + 6 = 0$ se convierte en función despejando $y$:
$$-3y = -2x - 6 \implies y = \frac{2}{3}x + 2$$

Por lo tanto $f(x) = \frac{2}{3}x + 2$, con pendiente $m = \frac{2}{3}$ y ordenada al origen $b = 2$.

**Caso excepcional:** Si $B = 0$ la ecuación es de la forma $x = k$ (recta vertical), y **no puede expresarse como función** $y = f(x)$ porque a un mismo valor de $x$ le corresponderían infinitos valores de $y$.

---

## 4. Raíces de funciones y relación con ecuaciones

### 4.1 Raíces o ceros de una función

**Definición 4.1 (Raíz de una función):**
Un número $r \in \mathbb{R}$ es una **raíz** o **cero** de $f$ si:
$$f(r) = 0$$

**Interpretación geométrica:** Las raíces son las **abscisas** de los puntos donde la gráfica de $f$ corta el eje X.

**Ejemplo 4.1:**
Para $f(x) = x^2 - 5x + 6$:
$$f(x) = 0 \quad \Rightarrow \quad x^2 - 5x + 6 = 0$$
Factorizando: $(x - 2)(x - 3) = 0$
**Raíces:** $x = 2$ y $x = 3$

### 4.2 Relación entre funciones lineales y ecuaciones lineales

**Proposición 4.1:**
Resolver la ecuación lineal $mx + b = 0$ es equivalente a encontrar la raíz de la función $f(x) = mx + b$.

**Conexión:** 
- **Ecuación:** $2x - 6 = 0 \quad \Rightarrow \quad x = 3$
- **Función:** $f(x) = 2x - 6$ tiene raíz en $x = 3$ porque $f(3) = 0$
- **Gráfica:** La recta $y = 2x - 6$ corta el eje X en $(3, 0)$

### 4.3 Curvas paramétricas (introducción)

**Definición 4.3 (Curva paramétrica):**
Una **curva paramétrica** en $\mathbb{R}^2$ se define mediante dos funciones de un parámetro $t$:
$$\begin{cases}
x = x(t) \\
y = y(t)
\end{cases}$$

donde $t \in I \subseteq \mathbb{R}$ (intervalo de parámetros).

**Interpretación:** A medida que $t$ varía, el punto $(x(t), y(t))$ traza una curva en el plano.

**Ejemplo 4.2 (Círculo unitario):**
$$\begin{cases}
x(t) = \cos(t) \\
y(t) = \sin(t)
\end{cases} \quad t \in [0, 2\pi]$$

Esto describe un círculo de radio 1 centrado en el origen.

**Nota:** Las curvas paramétricas se estudiarán en profundidad en Cálculo II y Geometría Analítica Avanzada.

---

## 5. Función cuadrática

### 5.1 Definición y forma general

**Definición 5.1 (Función cuadrática):**
Una **función cuadrática** tiene la forma:
$$f(x) = ax^2 + bx + c$$
donde $a, b, c \in \mathbb{R}$ y $a \neq 0$.

**Gráfica:** La gráfica de una función cuadrática es una **parábola**.

### 5.2 Vértice y eje de simetría

**Teorema 5.1 (Coordenadas del vértice):**
El vértice de la parábola $f(x) = ax^2 + bx + c$ está en el punto:
$$V = \left(-\frac{b}{2a}, f\left(-\frac{b}{2a}\right)\right)$$

**Nota:** Esta fórmula se demostrará más adelante utilizando técnicas de Cálculo Diferencial en el tema de máximos y mínimos de una función (derivadas).

**Definición 5.2 (Eje de simetría):**
La recta vertical $x = -\frac{b}{2a}$ es el **eje de simetría** de la parábola.

**Proposición 5.1 (Concavidad):**
- Si $a > 0$, la parábola abre **hacia arriba** (∪) y el vértice es un **mínimo**
- Si $a < 0$, la parábola abre **hacia abajo** (∩) y el vértice es un **máximo**

**Ejemplo 5.1:**
Para $f(x) = 2x^2 - 8x + 3$:
- $a = 2 > 0$ → parábola abre hacia arriba
- Vértice: $x_v = -\frac{-8}{2(2)} = 2$
- $y_v = f(2) = 2(4) - 8(2) + 3 = 8 - 16 + 3 = -5$
- **Vértice:** $(2, -5)$

### 5.3 Raíces de la función cuadrática

**Teorema 5.2 (Fórmula general):**
Las raíces de $ax^2 + bx + c = 0$ son:
$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

**Definición 5.3 (Discriminante):**
$$\Delta = b^2 - 4ac$$

**Naturaleza de las raíces:**

| Discriminante | Raíces |
|---------------|--------|
| $\Delta > 0$ | Dos raíces reales distintas |
| $\Delta = 0$ | Una raíz real doble (vértice en eje X) |
| $\Delta < 0$ | No hay raíces reales (la parábola no corta el eje X) |

**Ejemplo 5.2:**
Para $f(x) = x^2 - 4x + 4$:
$$\Delta = (-4)^2 - 4(1)(4) = 16 - 16 = 0$$
$$x = \frac{4 \pm 0}{2} = 2$$
**Raíz doble:** $x = 2$

### 5.4 Forma canónica

**Proposición 5.2 (Forma canónica o de vértice):**
Toda función cuadrática se puede escribir como:
$$f(x) = a(x - h)^2 + k$$
donde $(h, k)$ es el vértice.

**Ejemplo 5.3:**
$$f(x) = 2(x - 3)^2 + 1$$
tiene vértice en $(3, 1)$ y abre hacia arriba ($a = 2 > 0$).

---

## 6. Funciones polinomiales de grado superior

### 6.1 Función cúbica

**Definición 6.1 (Función cúbica):**
$$f(x) = ax^3 + bx^2 + cx + d, \quad a \neq 0$$

**Características:**
- Tiene a lo sumo **3 raíces reales**
- La gráfica tiene forma de "S" o "S invertida"
- No tiene eje de simetría (pero puede tener punto de inflexión)

**Ejemplo 6.1:**
$$f(x) = x^3 - 3x$$

```
       y
       |
    2  |       /
    1  |      /
-------|-----●-----●----> x
   -2 -1  0  1  2
   -1  |    /
   -2  |   /
```

Raíces: $x^3 - 3x = 0 \Rightarrow x(x^2 - 3) = 0 \Rightarrow x = 0, \pm\sqrt{3}$

### 6.2 Función cuártica (grado 4)

**Definición 6.2 (Función cuártica):**
$$f(x) = ax^4 + bx^3 + cx^2 + dx + e, \quad a \neq 0$$

**Características:**
- Tiene a lo sumo **4 raíces reales**
- Si $a > 0$, ambos extremos tienden a $+\infty$
- Si $a < 0$, ambos extremos tienden a $-\infty$

**Ejemplo 6.2:**
$$f(x) = x^4 - 5x^2 + 4 = (x^2 - 1)(x^2 - 4)$$
**Raíces:** $x = \pm 1, \pm 2$

---

## 7. Función raíz cuadrada

### 7.1 Definición y dominio

**Definición 7.1 (Función raíz cuadrada):**
$$f(x) = \sqrt{x}$$

**Dominio:** $\text{Dom}(f) = [0, +\infty)$ (solo números no negativos)
**Imagen:** $\text{Im}(f) = [0, +\infty)$

**Propiedades:**
- $f(0) = 0$
- Es **creciente** en todo su dominio
- La gráfica es la mitad superior de una parábola rotada

**Ejemplo 7.1:**

| $x$ | $0$ | $1$ | $4$ | $9$ | $16$ |
|-----|-----|-----|-----|-----|------|
| $\sqrt{x}$ | $0$ | $1$ | $2$ | $3$ | $4$ |

### 7.2 Función raíz n-ésima

**Definición 7.2:**
$$f(x) = \sqrt[n]{x} = x^{1/n}$$

**Dominio:**
- Si $n$ es **par**: $[0, +\infty)$
- Si $n$ es **impar**: $(-\infty, +\infty)$

**Ejemplo 7.2:**
- $\sqrt[3]{-8} = -2$ (raíz cúbica de negativo existe)
- $\sqrt{-4}$ no está definida en $\mathbb{R}$ (requiere números complejos)

---

## 8. Función exponencial

### 8.1 Definición

**Definición 8.1 (Función exponencial):**
$$f(x) = a^x$$
donde $a > 0$ y $a \neq 1$ (la **base** $a$ es constante positiva).

**Dominio:** $(-\infty, +\infty)$
**Imagen:** $(0, +\infty)$ (siempre positiva)

**Propiedades fundamentales:**
1. $a^0 = 1$ para todo $a > 0$
2. $a^x \cdot a^y = a^{x+y}$
3. $\frac{a^x}{a^y} = a^{x-y}$
4. $(a^x)^y = a^{xy}$

### 8.2 Comportamiento según la base

**Caso 1: Base $a > 1$ (ejemplo: $f(x) = 2^x$)**
- La función es **creciente**
- $\lim_{x \to -\infty} a^x = 0$ (asíntota horizontal en $y = 0$)
- $\lim_{x \to +\infty} a^x = +\infty$ (crece rápidamente)

**Caso 2: Base $0 < a < 1$ (ejemplo: $f(x) = \left(\frac{1}{2}\right)^x$)**
- La función es **decreciente**
- $\lim_{x \to -\infty} a^x = +\infty$
- $\lim_{x \to +\infty} a^x = 0$ (asíntota horizontal en $y = 0$)

**Ejemplo 8.2:**
Para $f(x) = 2^x$:

| $x$ | $-2$ | $-1$ | $0$ | $1$ | $2$ | $3$ |
|-----|------|------|-----|-----|-----|-----|
| $2^x$ | $\frac{1}{4}$ | $\frac{1}{2}$ | $1$ | $2$ | $4$ | $8$ |


---

## 9. Función logarítmica

### 9.1 Definición

**Definición 9.1 (Logaritmo):**
El **logaritmo en base $a$** de $x$, denotado $\log_a(x)$, es el exponente al que hay que elevar $a$ para obtener $x$:
$$y = \log_a(x) \quad \Leftrightarrow \quad a^y = x$$

**Dominio:** $(0, +\infty)$ (solo números positivos)
**Imagen:** $(-\infty, +\infty)$

**Ejemplo 8.1:**
- $\log_2(8) = 3$ porque $2^3 = 8$
- $\log_{10}(100) = 2$ porque $10^2 = 100$
- $\log_5(1) = 0$ porque $5^0 = 1$

### 9.2 Propiedades fundamentales

**Proposición 9.1 (Propiedades de logaritmos):**
Para $a, x, y > 0$ con $a \neq 1$:

1. **Logaritmo del producto:** $\log_a(xy) = \log_a(x) + \log_a(y)$
2. **Logaritmo del cociente:** $\log_a\left(\frac{x}{y}\right) = \log_a(x) - \log_a(y)$
3. **Logaritmo de una potencia:** $\log_a(x^r) = r \cdot \log_a(x)$
4. **Identidad fundamental:** $a^{\log_a(x)} = x$
5. **Cambio de base:** $\log_a(x) = \frac{\log_b(x)}{\log_b(a)}$

**Ejemplo 9.1:**
$$\log_2(32) = \log_2(2^5) = 5 \cdot \log_2(2) = 5 \cdot 1 = 5$$

### 9.3 Logaritmos especiales

**Definición 9.2 (Logaritmo decimal):**
$$\log(x) = \log_{10}(x)$$
(cuando no se escribe la base, generalmente se asume base 10)

**Definición 9.3 (Logaritmo natural):**
$$\ln(x) = \log_e(x)$$
donde $e \approx 2.718$ (base natural). Este número es muy importante en el Cálculo; conforme avancemos en las clases conoceremos más propiedades sobre él.

### 9.4 Relación entre exponencial y logaritmo

**Teorema 9.1:**
Las funciones $f(x) = a^x$ y $g(x) = \log_a(x)$ son **inversas**:
$$\log_a(a^x) = x \quad \text{y} \quad a^{\log_a(x)} = x$$

**Interpretación geométrica:** Las gráficas de $y = a^x$ y $y = \log_a(x)$ son **simétricas respecto a la recta $y = x$**.

```
       y
       |
       |     y=2^x
    4  |       /
    3  |      /
    2  |    /•
    1  |  /  |  y=log₂(x)
-------|•----|-----> x
       1  2  4
```

**Ejemplo 9.2:**
Si $f(x) = 2^x$ pasa por $(3, 8)$, entonces $g(x) = \log_2(x)$ pasa por $(8, 3)$.

---

## 10. Álgebra de funciones

**Concepto intuitivo:**

Cuando trabajamos con funciones, podemos combinarlas de diversas formas para crear nuevas funciones. Así como podemos sumar números, también podemos **sumar funciones**. Estas operaciones se definen punto a punto: para cada valor de $x$, aplicamos la operación a los valores $f(x)$ y $g(x)$.

**Idea intuitiva de suma de funciones:**
Si tenemos dos funciones $f$ y $g$, la función **suma** $(f + g)$ se evalúa tomando el valor de $f$ y el valor de $g$ en cada punto, y luego sumándolos.

**Ejemplo visual:** Si $f(x) = x$ y $g(x) = 2$, entonces:
- $(f + g)(3) = f(3) + g(3) = 3 + 2 = 5$
- $(f + g)(x) = x + 2$

### 10.1 Operaciones aritméticas con funciones

**Definición 10.1 (Suma de funciones):**
Dadas dos funciones $f: A \to \mathbb{R}$ y $g: B \to \mathbb{R}$, la **suma** de $f$ y $g$ es la función $(f + g)$ definida por:
$$(f + g)(x) = f(x) + g(x)$$

El dominio de $f + g$ es:
$$\text{Dom}(f + g) = \text{Dom}(f) \cap \text{Dom}(g)$$

**Definición 10.2 (Resta de funciones):**
La **resta** de $f$ y $g$ es la función $(f - g)$ definida por:
$$(f - g)(x) = f(x) - g(x)$$

El dominio de $f - g$ es:
$$\text{Dom}(f - g) = \text{Dom}(f) \cap \text{Dom}(g)$$

**Definición 10.3 (Producto de funciones):**
El **producto** de $f$ y $g$ es la función $(f \cdot g)$ definida por:
$$(f \cdot g)(x) = f(x) \cdot g(x)$$

El dominio de $f \cdot g$ es:
$$\text{Dom}(f \cdot g) = \text{Dom}(f) \cap \text{Dom}(g)$$

**Definición 10.4 (Cociente de funciones):**
El **cociente** de $f$ y $g$ es la función $\left(\frac{f}{g}\right)$ definida por:
$$\left(\frac{f}{g}\right)(x) = \frac{f(x)}{g(x)}$$

El dominio de $\frac{f}{g}$ es:
$$\text{Dom}\left(\frac{f}{g}\right) = \{x \in \text{Dom}(f) \cap \text{Dom}(g) : g(x) \neq 0\}$$

**Observación importante:** En el cociente, además de la restricción $g(x) \neq 0$, también debemos respetar las restricciones de dominio de ambas funciones.

**Ejemplo 10.1:**
Sean $f(x) = x + 3$ y $g(x) = 2x - 1$. Calcular:

a) $(f + g)(x)$:
$$(f + g)(x) = f(x) + g(x) = (x + 3) + (2x - 1) = 3x + 2$$

b) $(f - g)(x)$:
$$(f - g)(x) = f(x) - g(x) = (x + 3) - (2x - 1) = x + 3 - 2x + 1 = -x + 4$$

c) $(f \cdot g)(x)$:
$$(f \cdot g)(x) = f(x) \cdot g(x) = (x + 3)(2x - 1) = 2x^2 - x + 6x - 3 = 2x^2 + 5x - 3$$

d) $\left(\frac{f}{g}\right)(x)$:
$$\left(\frac{f}{g}\right)(x) = \frac{f(x)}{g(x)} = \frac{x + 3}{2x - 1}$$

Para el dominio: $2x - 1 \neq 0 \Rightarrow x \neq \frac{1}{2}$

$$\text{Dom}\left(\frac{f}{g}\right) = \mathbb{R} \setminus \left\{\frac{1}{2}\right\}$$

**Ejemplo 10.2:**
Sean $f(x) = \sqrt{x}$ y $g(x) = \sqrt{4-x}$. Determinar el dominio de $(f + g)$.

- $\text{Dom}(f) = [0, +\infty)$ (necesitamos $x \geq 0$)
- $\text{Dom}(g) = (-\infty, 4]$ (necesitamos $4 - x \geq 0$, es decir, $x \leq 4$)

$$\text{Dom}(f + g) = \text{Dom}(f) \cap \text{Dom}(g) = [0, +\infty) \cap (-\infty, 4] = [0, 4]$$

La función suma es:
$$(f + g)(x) = \sqrt{x} + \sqrt{4-x}, \quad x \in [0, 4]$$

**Ejemplo 10.3:**
Sean $f(x) = \ln(x)$ y $g(x) = \frac{1}{x-2}$. Determinar el dominio de $(f \cdot g)$.

- $\text{Dom}(f) = (0, +\infty)$ (logaritmo requiere $x > 0$)
- $\text{Dom}(g) = \mathbb{R} \setminus \{2\}$ (denominador no puede ser cero)

$$\text{Dom}(f \cdot g) = (0, +\infty) \cap (\mathbb{R} \setminus \{2\}) = (0, 2) \cup (2, +\infty)$$

La función producto es:
$$(f \cdot g)(x) = \ln(x) \cdot \frac{1}{x-2} = \frac{\ln(x)}{x-2}$$

### 10.2 Múltiplo escalar de una función

**Definición 10.5 (Múltiplo escalar):**
Sea $f: A \to \mathbb{R}$ una función y $k \in \mathbb{R}$ una constante. El **múltiplo escalar** de $f$ por $k$ es la función $(k \cdot f)$ definida por:
$$(k \cdot f)(x) = k \cdot f(x)$$

El dominio de $k \cdot f$ es el mismo que el de $f$:
$$\text{Dom}(k \cdot f) = \text{Dom}(f)$$

**Ejemplo 10.4:**
Sea $f(x) = x^2 + 1$ y $k = -3$. Entonces:
$$(k \cdot f)(x) = -3 \cdot (x^2 + 1) = -3x^2 - 3$$

**Interpretación geométrica:** Multiplicar una función por una constante produce:
- Si $k > 1$: **expansión vertical** (la gráfica se aleja del eje $x$)
- Si $0 < k < 1$: **compresión vertical** (la gráfica se acerca al eje $x$)
- Si $k < 0$: **reflexión respecto al eje $x$ y escalamiento**

### 10.3 Propiedades algebraicas

**Proposición 10.1 (Propiedades de las operaciones con funciones):**

Sean $f$, $g$ y $h$ funciones, y $k, c \in \mathbb{R}$ constantes. Entonces:

**Propiedades de la suma:**
1. **Conmutativa:** $f + g = g + f$
2. **Asociativa:** $(f + g) + h = f + (g + h)$
3. **Elemento neutro:** Existe la función cero $0(x) = 0$ tal que $f + 0 = f$
4. **Elemento opuesto:** Para cada $f$ existe $-f$ tal que $f + (-f) = 0$

**Propiedades del producto:**
5. **Conmutativa:** $f \cdot g = g \cdot f$
6. **Asociativa:** $(f \cdot g) \cdot h = f \cdot (g \cdot h)$
7. **Distributiva:** $f \cdot (g + h) = f \cdot g + f \cdot h$

**Propiedades del múltiplo escalar:**
8. $k(f + g) = kf + kg$
9. $(k + c)f = kf + cf$
10. $(kc)f = k(cf)$
11. $1 \cdot f = f$

**Ejemplo 10.5:**
Verificar la propiedad distributiva para $f(x) = x$, $g(x) = x + 1$ y $h(x) = 2$:

$$f \cdot (g + h) = x \cdot [(x+1) + 2] = x \cdot (x + 3) = x^2 + 3x$$

$$f \cdot g + f \cdot h = x(x+1) + x(2) = x^2 + x + 2x = x^2 + 3x$$

Efectivamente, ambas expresiones son iguales. ✓

### 10.4 Combinaciones de funciones

**Ejemplo 10.6 (Combinación lineal):**
Una **combinación lineal** de funciones $f_1, f_2, \ldots, f_n$ con coeficientes $c_1, c_2, \ldots, c_n$ es:
$$h(x) = c_1 f_1(x) + c_2 f_2(x) + \cdots + c_n f_n(x)$$

Por ejemplo, si $f_1(x) = x^2$, $f_2(x) = x$ y $f_3(x) = 1$, entonces:
$$h(x) = 2f_1(x) - 3f_2(x) + 5f_3(x) = 2x^2 - 3x + 5$$

Esto muestra que las **funciones polinómicas** son combinaciones lineales de las funciones potencia.

**Ejemplo 10.7 (Operaciones múltiples):**
Sean $f(x) = x^2$, $g(x) = 2x$ y $h(x) = 1$. Calcular:
$$k(x) = \frac{f(x) + g(x)}{h(x) + g(x)}$$

Sustituyendo:
$$k(x) = \frac{x^2 + 2x}{1 + 2x}$$

**Dominio:** Necesitamos que $1 + 2x \neq 0$, es decir, $x \neq -\frac{1}{2}$.

$$\text{Dom}(k) = \mathbb{R} \setminus \left\{-\frac{1}{2}\right\}$$

**Ejemplo 10.8 (Producto de funciones con dominios restringidos):**
Sean $f(x) = \sqrt{x-1}$ y $g(x) = \sqrt{5-x}$. Determinar $(f \cdot g)(x)$ y su dominio.

- $\text{Dom}(f) = [1, +\infty)$ (necesitamos $x - 1 \geq 0$)
- $\text{Dom}(g) = (-\infty, 5]$ (necesitamos $5 - x \geq 0$)

$$\text{Dom}(f \cdot g) = [1, +\infty) \cap (-\infty, 5] = [1, 5]$$

$$(f \cdot g)(x) = \sqrt{x-1} \cdot \sqrt{5-x} = \sqrt{(x-1)(5-x)}$$

Simplificando:
$$(f \cdot g)(x) = \sqrt{-x^2 + 6x - 5}, \quad x \in [1, 5]$$

**Observación final:**
Las operaciones algebraicas con funciones son fundamentales para:
- Construir modelos matemáticos complejos a partir de funciones simples
- Entender la composición de funciones (tema de Funciones Parte 2)
- Resolver ecuaciones funcionales
- Análisis de sistemas dinámicos

---

## 11. Ejercicios propuestos

### 11.1 Funciones lineales y afines

1. Encuentre la ecuación de la recta que pasa por $(2, 5)$ y $(6, 13)$

2. Determine la ecuación de la recta con pendiente $m = -3$ que pasa por $(-1, 4)$

3. Encuentre las intersecciones con los ejes de $f(x) = 3x - 9$

4. Determine si las rectas $y = 2x + 3$ y $y = 2x - 5$ son paralelas, perpendiculares o ninguna

5. Encuentre la ecuación de la recta perpendicular a $y = 4x - 2$ que pasa por el origen

### 11.2 Funciones cuadráticas

6. Encuentre el vértice y el eje de simetría de $f(x) = x^2 - 6x + 5$

7. Determine las raíces de $g(x) = 2x^2 + 5x - 3$

8. Calcule el discriminante de $h(x) = x^2 + 4x + 10$ e interprete el resultado

9. Escriba $f(x) = 3x^2 - 12x + 7$ en forma canónica

10. Una pelota se lanza verticalmente y su altura viene dada por $h(t) = -5t^2 + 20t + 2$ (metros). ¿Cuál es la altura máxima alcanzada?

### 11.3 Otras funciones

11. Resuelva: $2^x = 32$

12. Calcule: $\log_3(81)$

13. Simplifique: $\log_5(125) - \log_5(25)$

14. Resuelva: $\log_2(x) = 5$

15. Encuentre el dominio de $f(x) = \sqrt{4 - x}$

### 11.4 Análisis de gráficas

16. Determine cuáles de las siguientes gráficas representan funciones (use el criterio de la recta vertical)

17. Dada la gráfica de una parábola con vértice en $(2, -3)$ que pasa por $(0, 1)$, encuentre su ecuación

18. Dibuje la gráfica de $f(x) = |x - 2|$ (valor absoluto)

19. Grafique $g(x) = \begin{cases} x + 1 & \text{si } x < 0 \\ x^2 & \text{si } x \geq 0 \end{cases}$ (función definida por partes)

20. Determine la imagen de $f(x) = -x^2 + 4$

---

**Fin de la Clase 5: Funciones Parte 1**