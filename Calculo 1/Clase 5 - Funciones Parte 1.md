# Funciones parte 1
## 4. Relaciones y funciones

### 4.1 Producto cartesiano y relaciones

**Definición 4.1 (Producto cartesiano):**
Dados dos conjuntos $A$ y $B$, el **producto cartesiano** $A \times B$ es:
$$A \times B = \{(a, b) : a \in A, \, b \in B\}$$
**Ejemplo 4.1:**
Si $A = \{1, 2\}$ y $B = \{x, y, z\}$, entonces:
$$A \times B = \{(1,x), (1,y), (1,z), (2,x), (2,y), (2,z)\}$$
**Definición 4.2 (Relación):**
Una **relación** $R$ de $A$ en $B$ es cualquier subconjunto de $A \times B$:
$$R \subseteq A \times B$$
Si $(a, b) \in R$, decimos que "$a$ está relacionado con $b$" y escribimos $aRb$.

**Ejemplo 4.2:**
Sea $A = \{1, 2, 3\}$ y $B = \{2, 4, 6, 8\}$. La relación "$x$ divide a $y$" es:
$$R = \{(1,2), (1,4), (1,6), (1,8), (2,2), (2,4), (2,6), (2,8), (3,6)\}$$
### 4.2 Definición formal de función

**Definición 4.3 (Función):**
Una **función** $f$ de un conjunto $A$ en un conjunto $B$ es una relación que asigna a **cada elemento** de $A$ **exactamente un** elemento de $B$.
![[diagrama_funcion.png]]
**Notación:** $f: A \to B$
- $A$ es el **dominio** de $f$ (conjunto de partida)
- $B$ es el **codominio** de $f$ (conjunto de llegada)
- Si $f$ asigna $b$ a $a$, escribimos $f(a) = b$ (se lee "f de a es igual a b")

**Condición crucial:** Para cada $a \in A$, existe **uno y solo uno** $b \in B$ tal que $f(a) = b$.

**Ejemplo 4.3 (Es función):**
$$f: \{1, 2, 3\} \to \{a, b, c\}$$
$$f(1) = a, \quad f(2) = b, \quad f(3) = a$$
Esto **es** una función (cada elemento del dominio tiene exactamente una imagen).
![[ejemplo_funcion_1.png]]

**Ejemplo 4.4 (NO es función):**
$$R: \{1, 2\} \to \{a, b, c\}$$
$$R = \{(1, a), (1, b), (2, c)\}$$
Esto **no es** una función porque $1$ tiene dos imágenes: $a$ y $b$.
![[relacion_no_funcion_neon.png]]
### 4.3 Funciones de $\mathbb{R}$ en $\mathbb{R}$

**Notación estándar:** Una función $f: \mathbb{R} \to \mathbb{R}$ se expresa típicamente como:
$$y = f(x)$$
donde:
- $x$ es la **variable independiente**
- $y$ es la **variable dependiente**

### 4.3.1 Imagen y preimagen

**Concepto intuitivo:**

Cuando trabajamos con una función $f: A \to B$, surgen dos preguntas naturales:
1. **¿Qué valores de salida puede producir la función?** Esta es la idea de la **imagen** de $f$.
2. **Dado un valor de salida, ¿qué valores de entrada lo produjeron?** Esta es la idea de la **preimagen** de ese valor.

**Idea intuitiva de imagen:**
La **imagen** de una función es el conjunto de todos los valores que la función **efectivamente alcanza** o "produce". Es decir, si aplicamos la función a todos los elementos del dominio, la imagen es la colección de todos los resultados obtenidos.

**Ejemplo intuitivo 1:** Considera $f: \{1, 2, 3\} \to \{a, b, c, d\}$ definida por:
$$f(1) = a, \quad f(2) = b, \quad f(3) = b$$
La imagen de $f$ es $\{a, b\}$ porque estos son los únicos valores que la función produce. Nota que $c$ y $d$ están en el codominio pero **no** en la imagen.

**Idea intuitiva de preimagen:**
La **preimagen** de un elemento $y$ del codominio es el conjunto de todos los elementos del dominio que la función "envía" a $y$. Es como preguntarse: "¿De dónde viene $y$?"

**Ejemplo intuitivo 2:** En el ejemplo anterior:
- La preimagen de $a$ es $\{1\}$ (solo el 1 produce $a$)
- La preimagen de $b$ es $\{2, 3\}$ (tanto 2 como 3 producen $b$)
- La preimagen de $c$ es $\emptyset$ (ningún elemento produce $c$)

**Definición 4.4 (Imagen y preimagen - Definición formal):**

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

### 4.4 Representación de funciones

**a) Tabla de valores:**

| $x$    | $-2$ | $-1$ | $0$ | $1$ | $2$ |
| ------ | ---- | ---- | --- | --- | --- |
| $f(x)$ | $4$  | $1$  | $0$ | $1$ | $4$ |

**b) Fórmula algebraica:**
$$f(x) = x^2$$
**c) Gráfica:**
La gráfica de $f$ es el conjunto de puntos $(x, f(x))$ en el plano:
$$\text{Graf}(f) = \{(x, y) \in \mathbb{R}^2 : y = f(x)\}$$
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

---

## 5. Función lineal y afín

### 5.1 Definición

**Definición 5.1 (Función lineal):**
Una **función lineal** tiene la forma:
$$f(x) = mx$$
donde $m \in \mathbb{R}$ es una constante llamada **pendiente**.

**Definición 5.2 (Función afín):**
Una **función afín** tiene la forma:
$$f(x) = mx + b$$
donde:
- $m$ es la **pendiente**
- $b$ es la **ordenada al origen** (intersección con el eje Y)

**Observación:** La gráfica de una función afín es siempre una **recta**.

### 5.2 Pendiente de una recta

**Definición 5.3 (Pendiente):**
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

**Ejemplo 5.1:**
La recta que pasa por $A = (1, 2)$ y $B = (4, 8)$ tiene pendiente:
$$m = \frac{8 - 2}{4 - 1} = \frac{6}{3} = 2$$

### 5.3 Ecuación punto-pendiente

**Teorema 5.1 (Forma punto-pendiente):**
La ecuación de la recta con pendiente $m$ que pasa por el punto $(x_0, y_0)$ es:
$$y - y_0 = m(x - x_0)$$
**Ejemplo 5.2:**
Encuentre la ecuación de la recta con pendiente $m = 3$ que pasa por $(2, 5)$:

$$\begin{align}
y - 5 &= 3(x - 2) \\
y - 5 &= 3x - 6 \\
y &= 3x - 1
\end{align}$$

**Forma pendiente-ordenada:** $y = 3x - 1$ (con $b = -1$)

### 5.4 Intersecciones con los ejes

**Definición 5.4 (Intersección con el eje Y):**
La **ordenada al origen** es el valor de $y$ cuando $x = 0$:
$$y = f(0) = b$$
Punto: $(0, b)$

**Definición 5.5 (Intersección con el eje X):**
La **abscisa al origen** es el valor de $x$ cuando $y = 0$. Para $f(x) = mx + b$:
$$mx + b = 0 \quad \Rightarrow \quad x = -\frac{b}{m}$$
Punto: $\left(-\frac{b}{m}, 0\right)$

**Ejemplo 5.3:**
Para $f(x) = 2x - 4$:
- Intersección con eje Y: $(0, -4)$
- Intersección con eje X: $2x - 4 = 0 \Rightarrow x = 2$, punto $(2, 0)$

### 5.5 Ecuación general de la recta

**Definición 5.6 (Ecuación general de la recta):**
Una recta en el plano cartesiano puede expresarse mediante la **ecuación lineal general**:
$$Ax + By + C = 0$$
donde $A, B, C \in \mathbb{R}$ y $(A, B) \neq (0, 0)$ (al menos uno de los coeficientes $A$ o $B$ debe ser distinto de cero).

**Relación con la función lineal:**

**Proposición 5.1:**
Toda ecuación lineal $Ax + By + C = 0$ con $B \neq 0$ puede expresarse como una función afín $y = f(x)$.

**Demostración:**
Si $B \neq 0$, despejamos $y$:
$$Ax + By + C = 0$$
$$By = -Ax - C$$
$$y = -\frac{A}{B}x - \frac{C}{B}$$

Identificando con la forma $y = mx + b$:
- Pendiente: $m = -\frac{A}{B}$
- Ordenada al origen: $b = -\frac{C}{B}$

Por lo tanto, $f(x) = -\frac{A}{B}x - \frac{C}{B}$. $\square$

**Casos especiales:**

1. **Recta vertical ($B = 0$):** La ecuación $Ax + C = 0$ representa una recta vertical $x = -\frac{C}{A}$.
   - **No es función** (falla la prueba de la recta vertical)
   - Todos los puntos tienen la misma abscisa

2. **Recta horizontal ($A = 0$):** La ecuación $By + C = 0$ representa una recta horizontal $y = -\frac{C}{B}$.
   - **Es una función constante** $f(x) = -\frac{C}{B}$
   - Pendiente $m = 0$

**Ejemplo 5.4:**
Convertir $3x + 2y - 6 = 0$ a forma función:
$$2y = -3x + 6$$
$$y = -\frac{3}{2}x + 3$$
Por lo tanto: $f(x) = -\frac{3}{2}x + 3$ con $m = -\frac{3}{2}$ y $b = 3$.

**Ejemplo 5.5:**
La ecuación $x = 5$ (equivalente a $x + 0y - 5 = 0$) representa una recta vertical que **no** es función.

### 5.6 Intersección de dos rectas y sistemas de ecuaciones

**Definición 5.7 (Punto de intersección):**
Dos rectas se **intersectan** en un punto $P$ si $P$ pertenece simultáneamente a ambas rectas.

**Teorema 5.2 (Intersección de rectas y sistemas lineales):**
El punto de intersección de dos rectas dadas por:
$$\begin{cases}
A_1x + B_1y + C_1 = 0 \\
A_2x + B_2y + C_2 = 0
\end{cases}$$
es la solución del **sistema de ecuaciones lineales** $2 \times 2$.

**Casos posibles:**

1. **Un punto de intersección único (rectas secantes):**
   Las rectas no son paralelas. El sistema tiene **solución única**.
   - Condición: $\frac{A_1}{A_2} \neq \frac{B_1}{B_2}$ (pendientes distintas si ambas son no verticales)

2. **Ningún punto de intersección (rectas paralelas):**
   Las rectas son paralelas y distintas. El sistema es **inconsistente** (sin solución).
   - Condición: $\frac{A_1}{A_2} = \frac{B_1}{B_2} \neq \frac{C_1}{C_2}$

3. **Infinitos puntos de intersección (rectas coincidentes):**
   Las rectas son la misma. El sistema tiene **infinitas soluciones**.
   - Condición: $\frac{A_1}{A_2} = \frac{B_1}{B_2} = \frac{C_1}{C_2}$ (ecuaciones proporcionales)

**Método algebraico de solución:**

Para encontrar el punto de intersección de $y = m_1x + b_1$ y $y = m_2x + b_2$ (si $m_1 \neq m_2$):

**Paso 1:** Igualar las funciones:
$$m_1x + b_1 = m_2x + b_2$$

**Paso 2:** Despejar $x$:
$$m_1x - m_2x = b_2 - b_1$$
$$x = \frac{b_2 - b_1}{m_1 - m_2}$$

**Paso 3:** Sustituir en cualquiera de las ecuaciones originales para hallar $y$:
$$y = m_1x + b_1$$
**Ejemplo 5.6 (Rectas secantes):**
Encontrar la intersección de:
$$\begin{cases}
y = 2x + 1 \\
y = -x + 4
\end{cases}$$
Igualando:
$$2x + 1 = -x + 4$$
$$3x = 3$$
$$x = 1$$
Sustituyendo en la primera ecuación:
$$y = 2(1) + 1 = 3$$
**Punto de intersección:** $(1, 3)$

**Verificación:** 
- En $y = 2x + 1$: $y = 2(1) + 1 = 3$ ✓
- En $y = -x + 4$: $y = -(1) + 4 = 3$ ✓

**Ejemplo 5.7 (Rectas paralelas):**
$$\begin{cases}
y = 3x + 2 \\
y = 3x - 1
\end{cases}$$

Ambas tienen pendiente $m = 3$ pero diferente ordenada ($b = 2$ vs $b = -1$).
Son **paralelas** → No se intersectan → Sistema sin solución.

**Ejemplo 5.8 (Sistema $2 \times 2$ general):**
Resolver:
$$\begin{cases}
2x + 3y = 12 \\
x - y = 1
\end{cases}$$

**Método de sustitución:**
De la segunda ecuación: $x = y + 1$

Sustituyendo en la primera:
$$2(y + 1) + 3y = 12$$
$$2y + 2 + 3y = 12$$
$$5y = 10$$
$$y = 2$$

Entonces: $x = 2 + 1 = 3$

**Solución:** $(3, 2)$

**Interpretación geométrica:** Las rectas $2x + 3y - 12 = 0$ y $x - y - 1 = 0$ se intersectan en el punto $(3, 2)$.

**Proposición 5.2 (Condición de perpendicularidad):**
Dos rectas no verticales con pendientes $m_1$ y $m_2$ son **perpendiculares** si y solo si:
$$m_1 \cdot m_2 = -1$$
Equivalentemente: $m_2 = -\frac{1}{m_1}$

**Ejemplo 5.9:**
Las rectas $y = 2x + 3$ y $y = -\frac{1}{2}x + 1$ son perpendiculares porque:
$$m_1 \cdot m_2 = 2 \cdot \left(-\frac{1}{2}\right) = -1$$

---

## 6. Raíces de funciones y relación con ecuaciones

### 6.1 Raíces o ceros de una función

**Definición 6.1 (Raíz de una función):**
Un número $r \in \mathbb{R}$ es una **raíz** o **cero** de $f$ si:
$$f(r) = 0$$

**Interpretación geométrica:** Las raíces son las **abscisas** de los puntos donde la gráfica de $f$ corta el eje X.

**Ejemplo 6.1:**
Para $f(x) = x^2 - 5x + 6$:
$$f(x) = 0 \quad \Rightarrow \quad x^2 - 5x + 6 = 0$$
Factorizando: $(x - 2)(x - 3) = 0$
**Raíces:** $x = 2$ y $x = 3$

### 6.2 Relación entre funciones lineales y ecuaciones lineales

**Proposición 6.1:**
Resolver la ecuación lineal $mx + b = 0$ es equivalente a encontrar la raíz de la función $f(x) = mx + b$.

**Conexión:** 
- **Ecuación:** $2x - 6 = 0 \quad \Rightarrow \quad x = 3$
- **Función:** $f(x) = 2x - 6$ tiene raíz en $x = 3$ porque $f(3) = 0$
- **Gráfica:** La recta $y = 2x - 6$ corta el eje X en $(3, 0)$

### 6.3 Gráfica de una función como conjunto de puntos

**Observación fundamental:**
Dada una función $y = f(x)$, su gráfica es el conjunto de pares ordenados:
$$\{(x, y) : y = f(x), \, x \in \text{Dom}(f)\}$$
**Interpretación:** Si recorremos todos los valores de $x$ en el dominio y calculamos $y = f(x)$, obtenemos una **curva** en el plano.

**Ejemplo 6.2:**
Para $f(x) = x^2$:
- Puntos: $(-2, 4)$, $(-1, 1)$, $(0, 0)$, $(1, 1)$, $(2, 4)$, $...$
- La gráfica forma una **parábola**
### 6.4 Curvas paramétricas (introducción)

**Definición 6.2 (Curva paramétrica):**
Una **curva paramétrica** en $\mathbb{R}^2$ se define mediante dos funciones de un parámetro $t$:
$$\begin{cases}
x = x(t) \\
y = y(t)
\end{cases}$$

donde $t \in I \subseteq \mathbb{R}$ (intervalo de parámetros).

**Interpretación:** A medida que $t$ varía, el punto $(x(t), y(t))$ traza una curva en el plano.

**Ejemplo 6.3 (Círculo unitario):**
$$\begin{cases}
x(t) = \cos(t) \\
y(t) = \sin(t)
\end{cases} \quad t \in [0, 2\pi]$$

Esto describe un círculo de radio 1 centrado en el origen.

**Nota:** Las curvas paramétricas se estudiarán en profundidad en Cálculo II y Geometría Analítica Avanzada.

---

## 7. Función cuadrática

### 7.1 Definición y forma general

**Definición 7.1 (Función cuadrática):**
Una **función cuadrática** tiene la forma:
$$f(x) = ax^2 + bx + c$$
donde $a, b, c \in \mathbb{R}$ y $a \neq 0$.

**Gráfica:** La gráfica de una función cuadrática es una **parábola**.

### 7.2 Vértice y eje de simetría

**Teorema 7.1 (Coordenadas del vértice):**
El vértice de la parábola $f(x) = ax^2 + bx + c$ está en el punto:
$$V = \left(-\frac{b}{2a}, f\left(-\frac{b}{2a}\right)\right)$$

*Esto se demostrara mas adelante en el tema de máximos y mínimos de una función*

**Definición 7.2 (Eje de simetría):**
La recta vertical $x = -\frac{b}{2a}$ es el **eje de simetría** de la parábola.

**Proposición 7.1 (Concavidad):**
- Si $a > 0$, la parábola abre **hacia arriba** (∪) y el vértice es un **mínimo**
- Si $a < 0$, la parábola abre **hacia abajo** (∩) y el vértice es un **máximo**

**Ejemplo 7.1:**
Para $f(x) = 2x^2 - 8x + 3$:
- $a = 2 > 0$ → parábola abre hacia arriba
- Vértice: $x_v = -\frac{-8}{2(2)} = 2$
- $y_v = f(2) = 2(4) - 8(2) + 3 = 8 - 16 + 3 = -5$
- **Vértice:** $(2, -5)$

### 7.3 Raíces de la función cuadrática

**Teorema 7.2 (Fórmula general):**
Las raíces de $ax^2 + bx + c = 0$ son:
$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

**Definición 7.3 (Discriminante):**
$$\Delta = b^2 - 4ac$$

**Naturaleza de las raíces:**

| Discriminante | Raíces |
|---------------|--------|
| $\Delta > 0$ | Dos raíces reales distintas |
| $\Delta = 0$ | Una raíz real doble (vértice en eje X) |
| $\Delta < 0$ | No hay raíces reales (la parábola no corta el eje X) |

**Ejemplo 7.2:**
Para $f(x) = x^2 - 4x + 4$:
$$\Delta = (-4)^2 - 4(1)(4) = 16 - 16 = 0$$
$$x = \frac{4 \pm 0}{2} = 2$$
**Raíz doble:** $x = 2$

### 7.4 Forma canónica

**Proposición 7.2 (Forma canónica o de vértice):**
Toda función cuadrática se puede escribir como:
$$f(x) = a(x - h)^2 + k$$
donde $(h, k)$ es el vértice.

**Ejemplo 7.3:**
$$f(x) = 2(x - 3)^2 + 1$$
tiene vértice en $(3, 1)$ y abre hacia arriba ($a = 2 > 0$).

---

## 8. Funciones polinomiales de grado superior

### 8.1 Función cúbica

**Definición 8.1 (Función cúbica):**
$$f(x) = ax^3 + bx^2 + cx + d, \quad a \neq 0$$

**Características:**
- Tiene a lo sumo **3 raíces reales**
- La gráfica tiene forma de "S" o "S invertida"
- No tiene eje de simetría (pero puede tener punto de inflexión)

**Ejemplo 8.1:**
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

### 8.2 Función cuártica (grado 4)

**Definición 8.2 (Función cuártica):**
$$f(x) = ax^4 + bx^3 + cx^2 + dx + e, \quad a \neq 0$$

**Características:**
- Tiene a lo sumo **4 raíces reales**
- Si $a > 0$, ambos extremos tienden a $+\infty$
- Si $a < 0$, ambos extremos tienden a $-\infty$

**Ejemplo 8.2:**
$$f(x) = x^4 - 5x^2 + 4 = (x^2 - 1)(x^2 - 4)$$
**Raíces:** $x = \pm 1, \pm 2$

---

## 9. Función raíz cuadrada

### 9.1 Definición y dominio

**Definición 9.1 (Función raíz cuadrada):**
$$f(x) = \sqrt{x}$$

**Dominio:** $\text{Dom}(f) = [0, +\infty)$ (solo números no negativos)
**Imagen:** $\text{Im}(f) = [0, +\infty)$

**Propiedades:**
- $f(0) = 0$
- Es **creciente** en todo su dominio
- La gráfica es la mitad superior de una parábola rotada

**Ejemplo 9.1:**

| $x$ | $0$ | $1$ | $4$ | $9$ | $16$ |
|-----|-----|-----|-----|-----|------|
| $\sqrt{x}$ | $0$ | $1$ | $2$ | $3$ | $4$ |

### 9.2 Función raíz n-ésima

**Definición 9.2:**
$$f(x) = \sqrt[n]{x} = x^{1/n}$$

**Dominio:**
- Si $n$ es **par**: $[0, +\infty)$
- Si $n$ es **impar**: $(-\infty, +\infty)$

**Ejemplo 9.2:**
- $\sqrt[3]{-8} = -2$ (raíz cúbica de negativo existe)
- $\sqrt{-4}$ no está definida en $\mathbb{R}$ (requiere números complejos)

---

## 10. Función exponencial

### 10.1 Definición

**Definición 10.1 (Función exponencial):**
$$f(x) = a^x$$
donde $a > 0$ y $a \neq 1$ (la **base** $a$ es constante positiva).

**Dominio:** $(-\infty, +\infty)$
**Imagen:** $(0, +\infty)$ (siempre positiva)

**Propiedades fundamentales:**
1. $a^0 = 1$ para todo $a > 0$
2. $a^x \cdot a^y = a^{x+y}$
3. $\frac{a^x}{a^y} = a^{x-y}$
4. $(a^x)^y = a^{xy}$

### 10.2 Comportamiento según la base

**Caso 1: Base $a > 1$ (ejemplo: $f(x) = 2^x$)**
- La función es **creciente**
- $\lim_{x \to -\infty} a^x = 0$ (asíntota horizontal en $y = 0$)
- $\lim_{x \to +\infty} a^x = +\infty$ (crece rápidamente)

**Caso 2: Base $0 < a < 1$ (ejemplo: $f(x) = \left(\frac{1}{2}\right)^x$)**
- La función es **decreciente**
- $\lim_{x \to -\infty} a^x = +\infty$
- $\lim_{x \to +\infty} a^x = 0$ (asíntota horizontal en $y = 0$)

**Ejemplo 10.1:**
Para $f(x) = 2^x$:

| $x$ | $-2$ | $-1$ | $0$ | $1$ | $2$ | $3$ |
|-----|------|------|-----|-----|-----|-----|
| $2^x$ | $\frac{1}{4}$ | $\frac{1}{2}$ | $1$ | $2$ | $4$ | $8$ |


---

## 11. Función logarítmica

### 11.1 Definición

**Definición 11.1 (Logaritmo):**
El **logaritmo en base $a$** de $x$, denotado $\log_a(x)$, es el exponente al que hay que elevar $a$ para obtener $x$:
$$y = \log_a(x) \quad \Leftrightarrow \quad a^y = x$$

**Dominio:** $(0, +\infty)$ (solo números positivos)
**Imagen:** $(-\infty, +\infty)$

**Ejemplo 11.1:**
- $\log_2(8) = 3$ porque $2^3 = 8$
- $\log_{10}(100) = 2$ porque $10^2 = 100$
- $\log_5(1) = 0$ porque $5^0 = 1$

### 11.2 Propiedades fundamentales

**Proposición 11.1 (Propiedades de logaritmos):**
Para $a, x, y > 0$ con $a \neq 1$:

1. **Logaritmo del producto:** $\log_a(xy) = \log_a(x) + \log_a(y)$
2. **Logaritmo del cociente:** $\log_a\left(\frac{x}{y}\right) = \log_a(x) - \log_a(y)$
3. **Logaritmo de una potencia:** $\log_a(x^r) = r \cdot \log_a(x)$
4. **Identidad fundamental:** $a^{\log_a(x)} = x$
5. **Cambio de base:** $\log_a(x) = \frac{\log_b(x)}{\log_b(a)}$

**Ejemplo 11.2:**
$$\log_2(32) = \log_2(2^5) = 5 \cdot \log_2(2) = 5 \cdot 1 = 5$$

### 11.3 Logaritmos especiales

**Definición 11.2 (Logaritmo decimal):**
$$\log(x) = \log_{10}(x)$$
(cuando no se escribe la base, generalmente se asume base 10)

**Definición 11.3 (Logaritmo natural):**
$$\ln(x) = \log_e(x)$$
donde $e \approx 2.718$ (base natural). Se estudiará en Cálculo.

### 11.4 Relación entre exponencial y logaritmo

**Teorema 11.1:**
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

**Ejemplo 11.3:**
Si $f(x) = 2^x$ pasa por $(3, 8)$, entonces $g(x) = \log_2(x)$ pasa por $(8, 3)$.

---

## 12. Ejercicios propuestos


### 12.2 Funciones lineales y afines

6. Encuentre la ecuación de la recta que pasa por $(2, 5)$ y $(6, 13)$

7. Determine la ecuación de la recta con pendiente $m = -3$ que pasa por $(-1, 4)$

8. Encuentre las intersecciones con los ejes de $f(x) = 3x - 9$

9. Determine si las rectas $y = 2x + 3$ y $y = 2x - 5$ son paralelas, perpendiculares o ninguna

10. Encuentre la ecuación de la recta perpendicular a $y = 4x - 2$ que pasa por el origen

### 12.3 Funciones cuadráticas

11. Encuentre el vértice y el eje de simetría de $f(x) = x^2 - 6x + 5$

12. Determine las raíces de $g(x) = 2x^2 + 5x - 3$

13. Calcule el discriminante de $h(x) = x^2 + 4x + 10$ e interprete el resultado

14. Escriba $f(x) = 3x^2 - 12x + 7$ en forma canónica

15. Una pelota se lanza verticalmente y su altura viene dada por $h(t) = -5t^2 + 20t + 2$ (metros). ¿Cuál es la altura máxima alcanzada?

### 12.4 Otras funciones

16. Resuelva: $2^x = 32$

17. Calcule: $\log_3(81)$

18. Simplifique: $\log_5(125) - \log_5(25)$

19. Resuelva: $\log_2(x) = 5$

20. Encuentre el dominio de $f(x) = \sqrt{4 - x}$

### 12.5 Análisis de gráficas

21. Determine cuáles de las siguientes gráficas representan funciones (use el criterio de la recta vertical)

22. Dada la gráfica de una parábola con vértice en $(2, -3)$ que pasa por $(0, 1)$, encuentre su ecuación

23. Dibuje la gráfica de $f(x) = |x - 2|$ (valor absoluto)

24. Grafique $g(x) = \begin{cases} x + 1 & \text{si } x < 0 \\ x^2 & \text{si } x \geq 0 \end{cases}$ (función definida por partes)

25. Determine la imagen de $f(x) = -x^2 + 4$

---

**Fin de la Clase 4**


