# Clase 7 - Funciones Parte 2: Transformaciones y Tipos Especiales

En esta clase profundizaremos en el análisis funcional, estableciendo definiciones formales para las transformaciones geométricas, la clasificación según simetría (paridad) y el estudio riguroso de la inyectividad, sobreyectividad y funciones inversas.

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

**Definición 3.1 (Función a tramos):**
Es una función definida por distintas fórmulas analíticas en subconjuntos disjuntos de su dominio.

**Ejemplo 3.1 (Valor absoluto):**
$$f(x) = |x| = \begin{cases} -x & \text{si } x < 0 \\ x & \text{si } x \geq 0 \end{cases}$$

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

## 6. Clasificación de Funciones

Sea $f: A \to B$ una función. Clasificamos las funciones según cómo relacionan los elementos del dominio $A$ con el codominio $B$.

### 6.1 Inyectividad (Uno a Uno)

**Definición 6.1 (Función Inyectiva):**
Una función $f$ es **inyectiva** (o inyección) si asigna imágenes distintas a elementos distintos del dominio. Formalmente:
$$\forall x_1, x_2 \in A, \quad f(x_1) = f(x_2) \implies x_1 = x_2$$
Equivalentemente (contrapositiva): $x_1 \neq x_2 \implies f(x_1) \neq f(x_2)$.

**Prueba de la línea horizontal:** Una función es inyectiva si ninguna recta horizontal intersecta su gráfica en más de un punto.

### 6.2 Sobreyectividad (Epiyecctiva o Sobre)

**Definición 6.2 (Función Sobreyectiva):**
Una función $f$ es **sobreyectiva** (o suryección) si todo elemento del codominio es imagen de al menos un elemento del dominio. Es decir, la imagen coincide con el codominio ($Im(f) = B$). Formalmente:
$$\forall y \in B, \quad \exists x \in A \text{ tal que } f(x) = y$$

### 6.3 Biyectividad

**Definición 6.3 (Función Biyectiva):**
Una función es **biyectiva** si es simultáneamente **inyectiva** y **sobreyectiva**.
Esto implica una correspondencia **biunívoca** (uno a uno y sobre) entre los conjuntos $A$ y $B$.

---

## 7. Funciones Inversas

El concepto de inversa permite "deshacer" la acción de una función.

### 7.1 Definición y Existencia

**Teorema 7.1 (Existencia de la inversa):**
Una función $f: A \to B$ tiene función inversa si y solo si $f$ es **biyectiva**.

**Definición 7.1 (Función Inversa):**
Si $f: A \to B$ es biyectiva, definimos su función inversa $f^{-1}: B \to A$ como:
$$f^{-1}(y) = x \iff f(x) = y$$

**Propiedades de la composición:**
1. $(f^{-1} \circ f)(x) = f^{-1}(f(x)) = x, \quad \forall x \in A$
2. $(f \circ f^{-1})(y) = f(f^{-1}(y)) = y, \quad \forall y \in B$

**Propiedad Gráfica:**
Las gráficas de $y=f(x)$ y $y=f^{-1}(x)$ son simétricas respecto a la recta identidad $y=x$.

### 7.2 Restricción del Dominio

Si una función no es inyectiva en su dominio natural (ej. $f(x) = x^2$), no posee inversa global. Sin embargo, podemos definir una **inversa parcial** restringiendo su dominio a un subconjunto donde sea inyectiva.

**Ejemplo:** Para $f(x) = x^2$ restringida a $[0, +\infty)$, la inversa es $f^{-1}(x) = \sqrt{x}$.

---

## 8. Inversas de Funciones Trascendentes

### 8.1 Funciones Trigonométricas Inversas

Dado que las funciones trigonométricas son periódicas (y por tanto no inyectivas), se definen restringiendo sus dominios principales.

**Definición 8.1 (Arco Seno):** Isomorfismo inverso de $\sin(x)$ restringido a $[-\frac{\pi}{2}, \frac{\pi}{2}]$.
$$y = \arcsin(x) \iff \sin(y) = x, \quad y \in [-\frac{\pi}{2}, \frac{\pi}{2}]$$

**Definición 8.2 (Arco Coseno):** Inversa de $\cos(x)$ restringido a $[0, \pi]$.
$$y = \arccos(x) \iff \cos(y) = x, \quad y \in [0, \pi]$$

**Definición 8.3 (Arco Tangente):** Inversa de $\tan(x)$ restringido a $(-\frac{\pi}{2}, \frac{\pi}{2})$.
$$y = \arctan(x) \iff \tan(y) = x, \quad y \in (-\frac{\pi}{2}, \frac{\pi}{2})$$

### 8.2 Funciones Hiperbólicas Inversas

Se pueden expresar explícitamente usando logaritmos naturales:

1. $\text{argsinh}(x) = \ln(x + \sqrt{x^2+1}), \quad \forall x \in \mathbb{R}$
2. $\text{argcosh}(x) = \ln(x + \sqrt{x^2-1}), \quad x \geq 1$
3. $\text{argtanh}(x) = \frac{1}{2}\ln\left(\frac{1+x}{1-x}\right), \quad |x|<1$

---

## 9. Cónicas y Funciones

Las secciones cónicas (círculo, elipse, hipérbola) se definen generalmente por ecuaciones implícitas de la forma $Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$. Estas ecuaciones generalmente **no definen funciones**, ya que para un $x$ dado pueden existir dos valores de $y$.

Para tratarlas como funciones, debemos resolver explícitamente para $y$, obteniendo dos ramas (o funciones):

### 9.1 El Círculo ($x^2 + y^2 = r^2$)
- Rama superior: $f_1(x) = \sqrt{r^2 - x^2}$
- Rama inferior: $f_2(x) = -\sqrt{r^2 - x^2}$

### 9.2 La Hipérbola Equilátera ($x^2 - y^2 = 1$)
- Rama superior: $f_1(x) = \sqrt{x^2 - 1}$
- Rama inferior: $f_2(x) = -\sqrt{x^2 - 1}$




