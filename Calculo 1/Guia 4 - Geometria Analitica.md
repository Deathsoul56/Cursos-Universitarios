# Guía de Ejercicios N°4: Geometría Analítica

**Cálculo 1**  
**Fecha:** 19 de enero de 2026

---

## Índice
1. [Puntos en R²](#1-puntos-en-r)
2. [Translaciones](#2-translaciones)
3. [Rotaciones](#3-rotaciones)
4. [Rectas, paralelas y perpendiculares](#4-rectas-paralelas-y-perpendiculares)
5. [Cónicas - Introducción](#5-cónicas-introducción)
6. [Círculos](#6-círculos)
7. [Elipses](#7-elipses)
8. [Parábolas](#8-parábolas)
9. [Hipérbolas](#9-hipérbolas)
10. [Soluciones](#soluciones)

---

## 1. Puntos en R²

### Teoría breve

**Plano cartesiano:** Sistema de coordenadas formado por dos ejes perpendiculares (eje $x$ horizontal, eje $y$ vertical).

**Punto:** Se representa como $P(x, y)$ donde $x$ es la coordenada en el eje horizontal e $y$ es la coordenada en el eje vertical.

**Distancia entre dos puntos:** Dados $P_1(x_1, y_1)$ y $P_2(x_2, y_2)$:
$$d(P_1, P_2) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$

**Punto medio:** El punto medio $M$ entre $P_1(x_1, y_1)$ y $P_2(x_2, y_2)$ es:
$$M = \left(\frac{x_1 + x_2}{2}, \frac{y_1 + y_2}{2}\right)$$

**División de un segmento:** Punto que divide el segmento $\overline{P_1P_2}$ en razón $r:s$:
$$P = \left(\frac{sx_1 + rx_2}{r + s}, \frac{sy_1 + ry_2}{r + s}\right)$$

**Área de un triángulo:** Dados tres vértices $A(x_1, y_1)$, $B(x_2, y_2)$, $C(x_3, y_3)$:
$$\text{Área} = \frac{1}{2}|x_1(y_2 - y_3) + x_2(y_3 - y_1) + x_3(y_1 - y_2)|$$

---

### 1.1 Distancia entre puntos ⭐

Calcule la distancia entre los siguientes pares de puntos:

**1.1.1** $A(1, 2)$ y $B(4, 6)$

**1.1.2** $P(0, 0)$ y $Q(3, 4)$

**1.1.3** $M(-2, 5)$ y $N(3, -7)$

**1.1.4** $C(-1, -1)$ y $D(2, 3)$

**1.1.5** $R(5, 0)$ y $S(0, 12)$

**1.1.6** $A(-3, 4)$ y $B(-3, -2)$

**1.1.7** $P(7, 2)$ y $Q(-1, 2)$

**1.1.8** $M(0, -5)$ y $N(0, 3)$

---

### 1.2 Punto medio ⭐

Encuentre el punto medio del segmento que une:

**1.2.1** $A(2, 4)$ y $B(6, 8)$

**1.2.2** $P(0, 0)$ y $Q(10, 6)$

**1.2.3** $M(-3, 5)$ y $N(7, -1)$

**1.2.4** $C(-4, -2)$ y $D(2, 6)$

**1.2.5** $R(1, 9)$ y $S(5, 3)$

---

### 1.3 División de segmentos ⭐⭐

**1.3.1** Encuentre el punto que divide al segmento $\overline{AB}$ con $A(1, 2)$ y $B(7, 8)$ en razón $1:2$ (más cerca de $A$).

**1.3.2** Divida el segmento de $P(0, 0)$ a $Q(6, 9)$ en razón $2:1$.

**1.3.3** Encuentre el punto que divide a $\overline{MN}$ con $M(-2, 4)$ y $N(4, -2)$ en tres partes iguales (primer punto de división desde $M$).

**1.3.4** Divida el segmento de $A(-3, 1)$ a $B(5, 7)$ en razón $3:5$.

**1.3.5** Encuentre los dos puntos que dividen el segmento de $C(0, 0)$ a $D(9, 6)$ en tres partes iguales.

---

### 1.4 Problemas con triángulos ⭐⭐

**1.4.1** Calcule el perímetro del triángulo con vértices $A(0, 0)$, $B(4, 0)$, $C(0, 3)$.

**1.4.2** Calcule el área del triángulo con vértices $A(1, 1)$, $B(4, 1)$, $C(4, 5)$.

**1.4.3** Determine si el triángulo con vértices $A(0, 0)$, $B(3, 4)$, $C(6, 8)$ es equilátero, isósceles o escaleno.

**1.4.4** Encuentre el área del triángulo con vértices $A(-2, 3)$, $B(4, 5)$, $C(1, -2)$.

**1.4.5** Calcule el perímetro del triángulo con vértices $P(-1, 2)$, $Q(3, 5)$, $R(0, -1)$.

---

### 1.5 Problemas geométricos ⭐⭐

**1.5.1** Determine si los puntos $A(1, 2)$, $B(3, 4)$, $C(5, 6)$ son colineales.

**1.5.2** Verifique que el triángulo con vértices $A(0, 0)$, $B(5, 0)$, $C(5, 5)$ es rectángulo.

**1.5.3** Encuentre el cuarto vértice $D$ de un paralelogramo $ABCD$ donde $A(1, 2)$, $B(4, 3)$, $C(5, 6)$.

**1.5.4** Demuestre que los puntos $A(2, 1)$, $B(5, 4)$, $C(8, 1)$, $D(5, -2)$ forman un rombo.

**1.5.5** Encuentre todos los puntos en el eje $y$ que están a distancia $5$ del punto $P(3, 1)$.

---

## 2. Translaciones

### Teoría breve

**Translación:** Transformación que desplaza cada punto del plano una distancia fija en una dirección dada.

**Vector de translación:** $\vec{v} = (h, k)$ indica el desplazamiento horizontal $h$ y vertical $k$.

**Fórmula de translación:** Si $P(x, y)$ se traslada según $\vec{v} = (h, k)$, el punto resultante es:
$$P'(x', y') = (x + h, y + k)$$

**Translación de una figura:** Se aplica la translación a cada punto de la figura.

**Ecuación trasladada:** Si una curva tiene ecuación $f(x, y) = 0$, tras trasladar por $(h, k)$, la nueva ecuación es:
$$f(x - h, y - k) = 0$$

**Propiedades:**
- Las translaciones preservan distancias, ángulos, y formas
- La composición de translaciones es conmutativa
- $T_{(h_1,k_1)} \circ T_{(h_2,k_2)} = T_{(h_1+h_2, k_1+k_2)}$

---

### 2.1 Translación de puntos ⭐

**2.1.1** Traslade el punto $A(2, 3)$ según el vector $\vec{v} = (4, 1)$.

**2.1.2** Traslade $P(-1, 5)$ según $\vec{v} = (3, -2)$.

**2.1.3** ¿Cuál es la imagen de $M(0, 0)$ bajo la translación $\vec{v} = (-3, 4)$?

**2.1.4** Traslade $Q(5, -2)$ según $\vec{v} = (-5, 2)$.

**2.1.5** Si $A'(7, 8)$ es la imagen de $A(3, 5)$ bajo una translación, encuentre el vector de translación.

**2.1.6** ¿Cuál es el punto original si $P'(4, 1)$ resulta de trasladar por $\vec{v} = (2, -3)$?

---

### 2.2 Translación de figuras ⭐⭐

**2.2.1** Traslade el triángulo con vértices $A(0, 0)$, $B(2, 0)$, $C(1, 2)$ según $\vec{v} = (3, 1)$.

**2.2.2** Un cuadrado tiene vértices en $P(0, 0)$, $Q(2, 0)$, $R(2, 2)$, $S(0, 2)$. Trasládelo según $\vec{v} = (-1, 3)$.

**2.2.3** Traslade el segmento de $A(1, 1)$ a $B(5, 3)$ según $\vec{v} = (2, -4)$. Calcule la longitud del segmento original y del trasladado.

**2.2.4** Un rectángulo con vértices $A(1, 2)$, $B(5, 2)$, $C(5, 5)$, $D(1, 5)$ se traslada para que su vértice $A$ coincida con el origen. ¿Cuál es el vector de translación?

**2.2.5** Traslade el círculo con centro $C(3, 2)$ y radio $4$ según $\vec{v} = (-1, 5)$. Determine el nuevo centro y radio.

---

### 2.3 Translación de ecuaciones ⭐⭐

**2.3.1** La ecuación $y = x^2$ se traslada $3$ unidades a la derecha y $2$ unidades arriba. Encuentre la nueva ecuación.

**2.3.2** Traslade la recta $y = 2x + 1$ según $\vec{v} = (0, 3)$.

**2.3.3** La parábola $y = x^2 - 4$ se traslada para que su vértice esté en $(2, 1)$. Encuentre la nueva ecuación.

**2.3.4** Traslade el círculo $x^2 + y^2 = 9$ según $\vec{v} = (2, -1)$.

**2.3.5** ¿Qué translación lleva la recta $x + y = 5$ a la recta $x + y = 2$?

---

### 2.4 Composición de translaciones ⭐⭐

**2.4.1** Aplique las translaciones $\vec{v}_1 = (2, 3)$ y $\vec{v}_2 = (1, -1)$ sucesivamente al punto $P(0, 0)$.

**2.4.2** Encuentre una única translación equivalente a aplicar $\vec{v}_1 = (4, 2)$ seguida de $\vec{v}_2 = (-3, 5)$.

**2.4.3** Si se aplica $\vec{v}_1 = (a, b)$ seguida de $\vec{v}_2 = (-a, -b)$, ¿dónde queda el punto $P(x, y)$?

**2.4.4** Un punto se traslada por $\vec{v}_1 = (3, 0)$, luego por $\vec{v}_2 = (0, 4)$, y finalmente por $\vec{v}_3 = (-1, -1)$. ¿Cuál es la translación total?

**2.4.5** Demuestre que la composición de translaciones es conmutativa con un ejemplo numérico.

---

## 3. Rotaciones

### Teoría breve

**Rotación:** Transformación que gira cada punto del plano un ángulo fijo alrededor de un punto llamado centro de rotación.

**Rotación en torno al origen:** Para rotar un punto $P(x, y)$ un ángulo $\theta$ (positivo = sentido antihorario) alrededor del origen:
$$x' = x\cos\theta - y\sin\theta$$
$$y' = x\sin\theta + y\cos\theta$$

**En forma matricial:**
$$\begin{pmatrix} x' \\ y' \end{pmatrix} = \begin{pmatrix} \cos\theta & -\sin\theta \\ \sin\theta & \cos\theta \end{pmatrix} \begin{pmatrix} x \\ y \end{pmatrix}$$

**Rotación en torno a un punto $(h, k)$:**
1. Trasladar para llevar $(h, k)$ al origen: $(x-h, y-k)$
2. Rotar alrededor del origen
3. Trasladar de vuelta: agregar $(h, k)$

**Ángulos comunes:**
- $90°$: $(x, y) \to (-y, x)$
- $180°$: $(x, y) \to (-x, -y)$
- $270°$: $(x, y) \to (y, -x)$
- $-90°$ o $270°$: $(x, y) \to (y, -x)$

**Propiedades:**
- Las rotaciones preservan distancias y ángulos
- $R_\theta \circ R_\phi = R_{\theta+\phi}$
- La rotación inversa de $R_\theta$ es $R_{-\theta}$

---

### 3.1 Rotaciones alrededor del origen ⭐

**3.1.1** Rote el punto $P(1, 0)$ un ángulo de $90°$ alrededor del origen.

**3.1.2** Rote $Q(0, 1)$ un ángulo de $90°$ alrededor del origen.

**3.1.3** Rote $A(2, 3)$ un ángulo de $180°$ alrededor del origen.

**3.1.4** Rote $B(4, 0)$ un ángulo de $270°$ alrededor del origen.

**3.1.5** Rote $C(-1, 2)$ un ángulo de $-90°$ alrededor del origen.

**3.1.6** Rote $D(3, 3)$ un ángulo de $180°$ alrededor del origen.

---

### 3.2 Rotaciones con ángulos especiales ⭐⭐

**3.2.1** Rote el punto $P(2, 0)$ un ángulo de $45°$ alrededor del origen. Exprese en forma exacta.

**3.2.2** Rote $Q(\sqrt{2}, \sqrt{2})$ un ángulo de $45°$ alrededor del origen.

**3.2.3** Rote $A(1, 0)$ un ángulo de $60°$ alrededor del origen.

**3.2.4** Rote $B(0, 4)$ un ángulo de $30°$ alrededor del origen.

**3.2.5** Rote $C(2, 2)$ un ángulo de $-45°$ alrededor del origen.

---

### 3.3 Rotación de figuras ⭐⭐

**3.3.1** Rote el triángulo con vértices $A(1, 0)$, $B(0, 1)$, $C(0, 0)$ un ángulo de $90°$ alrededor del origen.

**3.3.2** Un cuadrado tiene vértices en $(1, 1)$, $(2, 1)$, $(2, 2)$, $(1, 2)$. Rótelo $180°$ alrededor del origen.

**3.3.3** Rote el segmento de $A(2, 0)$ a $B(4, 0)$ un ángulo de $90°$ alrededor del origen. Verifique que la longitud se preserva.

**3.3.4** Rote el rectángulo con vértices $(0, 0)$, $(3, 0)$, $(3, 1)$, $(0, 1)$ un ángulo de $270°$ alrededor del origen.

**3.3.5** Un punto $P$ está a distancia $5$ del origen. Si se rota $90°$, ¿a qué distancia está del origen su imagen?

---

### 3.4 Rotaciones alrededor de otros puntos ⭐⭐⭐

**3.4.1** Rote el punto $P(3, 1)$ un ángulo de $90°$ alrededor del punto $C(1, 1)$.

**3.4.2** Rote $Q(4, 2)$ un ángulo de $180°$ alrededor del punto $C(2, 2)$.

**3.4.3** Rote $A(5, 3)$ un ángulo de $90°$ alrededor del punto $C(3, 3)$.

**3.4.4** Rote el triángulo con vértices $(2, 0)$, $(4, 0)$, $(3, 2)$ un ángulo de $180°$ alrededor del punto $(3, 1)$.

**3.4.5** Rote el punto $(6, 2)$ un ángulo de $270°$ alrededor del punto $(2, 2)$.

---

### 3.5 Composición de rotaciones ⭐⭐⭐

**3.5.1** Aplique dos rotaciones sucesivas de $45°$ alrededor del origen al punto $P(1, 0)$.

**3.5.2** Rote $Q(0, 1)$ primero $60°$ y luego $30°$ alrededor del origen. Compare con una rotación directa de $90°$.

**3.5.3** Si un punto se rota $\theta$ y luego $-\theta$ alrededor del mismo centro, ¿dónde queda?

**3.5.4** Demuestre con un ejemplo que $R_{90°} \circ R_{90°} = R_{180°}$.

**3.5.5** ¿Cuántas rotaciones de $72°$ alrededor del origen se necesitan para que un punto vuelva a su posición original?

---

## 4. Rectas, paralelas y perpendiculares

### Teoría breve

**Ecuación de la recta:**

1. **Forma punto-pendiente:** $y - y_1 = m(x - x_1)$
   - $m$ = pendiente, $(x_1, y_1)$ = punto en la recta

2. **Forma pendiente-ordenada:** $y = mx + b$
   - $m$ = pendiente, $b$ = ordenada al origen

3. **Forma general:** $Ax + By + C = 0$
   - La pendiente es $m = -\frac{A}{B}$ (si $B \neq 0$)

4. **Forma simétrica:** $\frac{x}{a} + \frac{y}{b} = 1$
   - $a$ = intersección con eje $x$, $b$ = intersección con eje $y$

**Pendiente:** Dados dos puntos $P_1(x_1, y_1)$ y $P_2(x_2, y_2)$:
$$m = \frac{y_2 - y_1}{x_2 - x_1}$$

**Rectas paralelas:** Dos rectas son paralelas si tienen la misma pendiente:
$$m_1 = m_2$$

**Rectas perpendiculares:** Dos rectas son perpendiculares si:
$$m_1 \cdot m_2 = -1 \quad \text{o} \quad m_2 = -\frac{1}{m_1}$$

**Distancia de un punto a una recta:** La distancia del punto $P(x_0, y_0)$ a la recta $Ax + By + C = 0$ es:
$$d = \frac{|Ax_0 + By_0 + C|}{\sqrt{A^2 + B^2}}$$

**Ángulo entre dos rectas:** Si $m_1$ y $m_2$ son las pendientes:
$$\tan\theta = \left|\frac{m_1 - m_2}{1 + m_1m_2}\right|$$

---

### 4.1 Ecuación de la recta - Forma básica ⭐

**4.1.1** Encuentre la ecuación de la recta con pendiente $m = 2$ que pasa por $(1, 3)$.

**4.1.2** Escriba la ecuación de la recta con pendiente $m = -\frac{1}{2}$ y ordenada al origen $b = 4$.

**4.1.3** Encuentre la ecuación de la recta que pasa por los puntos $A(0, 2)$ y $B(3, 8)$.

**4.1.4** Determine la ecuación de la recta que pasa por $(2, -1)$ y $(5, 5)$.

**4.1.5** Escriba la ecuación de la recta con pendiente $m = 3$ que pasa por el origen.

**4.1.6** Encuentre la ecuación de la recta que pasa por $(-2, 4)$ con pendiente $m = 0$.

**4.1.7** ¿Cuál es la ecuación de la recta vertical que pasa por $(3, 5)$?

**4.1.8** Encuentre la ecuación de la recta horizontal que pasa por $(-1, 2)$.

---

### 4.2 Pendiente y ángulo de inclinación ⭐⭐

**4.2.1** Calcule la pendiente de la recta que pasa por $A(1, 2)$ y $B(4, 8)$.

**4.2.2** Determine la pendiente de la recta $3x - 4y + 12 = 0$.

**4.2.3** Una recta tiene ángulo de inclinación $45°$. ¿Cuál es su pendiente?

**4.2.4** Calcule el ángulo de inclinación de la recta $y = \sqrt{3}x + 2$.

**4.2.5** Si una recta tiene pendiente $m = -1$, ¿cuál es su ángulo de inclinación?

**4.2.6** Encuentre la pendiente de la recta perpendicular al eje $x$.

---

### 4.3 Rectas paralelas ⭐⭐

**4.3.1** Encuentre la ecuación de la recta paralela a $y = 2x + 3$ que pasa por $(1, 5)$.

**4.3.2** Escriba la ecuación de la recta paralela a $3x + 4y = 12$ que pasa por el origen.

**4.3.3** Determine si las rectas $y = 2x + 1$ y $2x - y + 5 = 0$ son paralelas.

**4.3.4** Encuentre $k$ para que las rectas $kx + 3y = 5$ y $2x + 6y = 7$ sean paralelas.

**4.3.5** Escriba la ecuación de la recta paralela al eje $x$ que pasa por $(2, -3)$.

**4.3.6** Encuentre la ecuación de la recta paralela a $x - 2y + 4 = 0$ que pasa por $(-1, 3)$.

---

### 4.4 Rectas perpendiculares ⭐⭐

**4.4.1** Encuentre la ecuación de la recta perpendicular a $y = 3x - 2$ que pasa por $(0, 0)$.

**4.4.2** Escriba la ecuación de la recta perpendicular a $x + 2y = 6$ que pasa por $(4, 1)$.

**4.4.3** Determine si las rectas $y = \frac{2}{3}x + 1$ y $y = -\frac{3}{2}x + 4$ son perpendiculares.

**4.4.4** Encuentre la ecuación de la mediatriz del segmento que une $A(0, 0)$ y $B(4, 2)$.

**4.4.5** Encuentre $k$ para que las rectas $kx + 2y = 3$ y $3x - y = 5$ sean perpendiculares.

**4.4.6** Escriba la ecuación de la recta perpendicular a $2x - 5y + 10 = 0$ que pasa por $(-2, 3)$.

---

### 4.5 Intersección de rectas ⭐⭐

**4.5.1** Encuentre el punto de intersección de las rectas $y = 2x + 1$ y $y = -x + 7$.

**4.5.2** Determine el punto de intersección de $x + y = 5$ y $2x - y = 1$.

**4.5.3** Encuentre dónde se intersectan las rectas $3x + 2y = 12$ y $x - y = 1$.

**4.5.4** ¿En qué punto se cortan las rectas $y = 3x - 4$ y $y = -2x + 6$?

**4.5.5** Verifique que las rectas $y = 2x + 1$ y $y = 2x - 3$ no se intersectan.

---

### 4.6 Distancia de punto a recta ⭐⭐⭐

**4.6.1** Calcule la distancia del punto $P(1, 2)$ a la recta $3x + 4y - 12 = 0$.

**4.6.2** Encuentre la distancia del origen a la recta $x + y = 4$.

**4.6.3** ¿Cuál es la distancia del punto $(2, -1)$ a la recta $y = 2x + 3$?

**4.6.4** Calcule la distancia del punto $(5, 0)$ a la recta que pasa por $(0, 0)$ y $(3, 4)$.

**4.6.5** Encuentre todos los puntos en la recta $y = x$ que están a distancia $\sqrt{2}$ del origen.

---

### 4.7 Ángulos entre rectas ⭐⭐⭐

**4.7.1** Calcule el ángulo agudo entre las rectas $y = x$ y $y = 2x$.

**4.7.2** Encuentre el ángulo entre las rectas $y = \sqrt{3}x$ y $y = 0$ (eje $x$).

**4.7.3** Determine el ángulo agudo entre $x + y = 1$ y $x - y = 1$.

**4.7.4** Calcule el ángulo entre las rectas $2x + y = 3$ y $x - 3y = 2$.

**4.7.5** ¿Cuál es el ángulo entre las rectas $y = 3x + 1$ y su perpendicular?

---

### 4.8 Problemas de aplicación ⭐⭐⭐

**4.8.1** Encuentre la ecuación de la altura del triángulo con vértices $A(0, 0)$, $B(4, 0)$, $C(2, 3)$ desde $C$ hasta $AB$.

**4.8.2** Determine las ecuaciones de las tres mediatrices del triángulo con vértices $A(0, 0)$, $B(6, 0)$, $C(0, 8)$.

**4.8.3** Encuentre el circuncentro (punto donde se intersectan las mediatrices) del triángulo del ejercicio anterior.

**4.8.4** Una recta pasa por $(2, 3)$ y forma un triángulo con los ejes coordenados de área $12$. Encuentre su ecuación.

**4.8.5** Encuentre la ecuación de la recta que pasa por $(1, 2)$ y es equidistante de los puntos $A(0, 0)$ y $B(4, 4)$.

---

## 5. Cónicas - Introducción

### Teoría breve

**Cónicas:** Curvas que se obtienen al intersectar un plano con un cono circular recto.

**Tipos de cónicas:**
1. **Círculo:** Lugar geométrico de puntos equidistantes de un punto fijo (centro)
2. **Elipse:** Lugar geométrico donde la suma de distancias a dos puntos fijos (focos) es constante
3. **Parábola:** Lugar geométrico equidistante de un punto fijo (foco) y una recta fija (directriz)
4. **Hipérbola:** Lugar geométrico donde la diferencia de distancias a dos focos es constante

**Ecuación general de segundo grado:**
$$Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$$

**Discriminante:** $\Delta = B^2 - 4AC$
- Si $\Delta < 0$ y $A = C$, $B = 0$: **Círculo**
- Si $\Delta < 0$ y $A \neq C$: **Elipse**
- Si $\Delta = 0$: **Parábola**
- Si $\Delta > 0$: **Hipérbola**

**Forma canónica:** Ecuación simplificada con centro en el origen y ejes paralelos a los ejes coordenados.

---

### 5.1 Identificar cónicas ⭐⭐

Identifique el tipo de cónica representada por cada ecuación:

**5.1.1** $x^2 + y^2 = 25$

**5.1.2** $\frac{x^2}{16} + \frac{y^2}{9} = 1$

**5.1.3** $y^2 = 8x$

**5.1.4** $\frac{x^2}{9} - \frac{y^2}{16} = 1$

**5.1.5** $4x^2 + 4y^2 = 36$

**5.1.6** $x^2 + 4y^2 = 16$

**5.1.7** $x^2 - 9y^2 = 9$

**5.1.8** $x^2 = -12y$

---

### 5.2 Ecuación general a forma estándar ⭐⭐

**5.2.1** Complete cuadrados para convertir $x^2 + y^2 - 4x + 6y - 12 = 0$ a forma estándar.

**5.2.2** Convierta $4x^2 + 9y^2 - 16x + 18y - 11 = 0$ a forma estándar.

**5.2.3** Escriba $y^2 - 6y - 8x + 1 = 0$ en forma estándar.

**5.2.4** Convierta $x^2 - 4y^2 - 6x + 16y - 23 = 0$ a forma estándar.

**5.2.5** Complete cuadrados: $9x^2 + 4y^2 + 36x - 8y + 4 = 0$

**5.2.6** Convierta $x^2 + y^2 + 8x - 10y + 16 = 0$ a forma estándar (círculo).

**5.2.7** Escriba $16x^2 + 25y^2 - 64x + 150y - 111 = 0$ en forma estándar (elipse).

**5.2.8** Convierta $x^2 - 8x - 12y + 4 = 0$ a forma estándar (parábola).

**5.2.9** Complete cuadrados: $9x^2 - 16y^2 + 36x + 32y - 124 = 0$ (hipérbola).

**5.2.10** Convierta $x^2 + y^2 - 6x + 4y - 12 = 0$ a forma estándar (círculo).

**5.2.11** Escriba $25x^2 + 4y^2 + 100x - 24y + 36 = 0$ en forma estándar (elipse).

**5.2.12** Convierta $y^2 + 8y + 12x - 20 = 0$ a forma estándar (parábola).

**5.2.13** Complete cuadrados: $4x^2 - y^2 - 24x - 4y + 28 = 0$ (hipérbola).

**5.2.14** Convierta $2x^2 + 2y^2 - 8x + 12y - 10 = 0$ a forma estándar (círculo).

**5.2.15** Escriba $9x^2 + 16y^2 - 18x + 64y - 71 = 0$ en forma estándar (elipse).

**5.2.16** Convierta $x^2 + 6x + 16y - 7 = 0$ a forma estándar (parábola).

**5.2.17** Complete cuadrados: $x^2 - 9y^2 + 2x + 54y - 80 = 0$ (hipérbola).

---

### 5.3 Usar el discriminante ⭐⭐

Use el discriminante para identificar el tipo de cónica:

**5.3.1** $3x^2 + 3y^2 - 6x + 12y - 5 = 0$

**5.3.2** $2x^2 + 5y^2 - 4x + 10y - 7 = 0$

**5.3.3** $x^2 - 2xy + y^2 - 4x - 2y = 0$

**5.3.4** $4x^2 - y^2 + 8x + 6y - 9 = 0$

**5.3.5** $x^2 + 2xy + y^2 + 3x - y + 5 = 0$

---

## 6. Círculos

### Teoría breve

**Definición:** Lugar geométrico de todos los puntos que equidistan de un punto fijo llamado centro.

**Ecuación estándar:** Centro $(h, k)$ y radio $r$:
$$(x - h)^2 + (y - k)^2 = r^2$$

**Ecuación con centro en el origen:**
$$x^2 + y^2 = r^2$$

**Ecuación general:**
$$x^2 + y^2 + Dx + Ey + F = 0$$

**Conversión a forma estándar:**
- Centro: $\left(-\frac{D}{2}, -\frac{E}{2}\right)$
- Radio: $r = \sqrt{\frac{D^2 + E^2 - 4F}{4}}$

**Propiedades importantes:**
- Todos los radios tienen la misma longitud
- El diámetro es $d = 2r$
- La circunferencia es $C = 2\pi r$
- El área es $A = \pi r^2$

**Posición relativa de un punto $P(x_0, y_0)$ y un círculo:**
- Si $d(P, C) < r$: el punto está **dentro** del círculo
- Si $d(P, C) = r$: el punto está **sobre** el círculo
- Si $d(P, C) > r$: el punto está **fuera** del círculo

**Recta tangente:** En un punto $P(x_0, y_0)$ del círculo, la tangente es perpendicular al radio en ese punto.

---

### 6.1 Ecuación del círculo ⭐

**6.1.1** Escriba la ecuación del círculo con centro $(0, 0)$ y radio $5$.

**6.1.2** Encuentre la ecuación del círculo con centro $(3, -2)$ y radio $4$.

**6.1.3** Escriba la ecuación del círculo con centro $(-1, 4)$ y radio $\sqrt{7}$.

**6.1.4** Determine la ecuación del círculo con centro en el origen que pasa por $(3, 4)$.

**6.1.5** Encuentre la ecuación del círculo con centro $(2, 1)$ que pasa por $(-1, 5)$.

**6.1.6** Escriba la ecuación del círculo con diámetro de extremos $A(1, 2)$ y $B(5, 6)$.

---

### 6.2 Centro y radio ⭐

**6.2.1** Encuentre el centro y radio de $x^2 + y^2 = 36$.

**6.2.2** Determine el centro y radio de $(x - 2)^2 + (y + 3)^2 = 16$.

**6.2.3** Encuentre el centro y radio de $(x + 4)^2 + (y - 1)^2 = 25$.

**6.2.4** ¿Cuál es el centro y radio de $x^2 + (y - 5)^2 = 9$?

**6.2.5** Determine centro y radio de $(x - 1)^2 + (y - 1)^2 = 2$.

---

### 6.3 Completar cuadrados ⭐⭐

**6.3.1** Convierta $x^2 + y^2 - 6x + 4y - 12 = 0$ a forma estándar y encuentre centro y radio.

**6.3.2** Escriba $x^2 + y^2 + 8x - 10y + 16 = 0$ en forma estándar.

**6.3.3** Convierta $x^2 + y^2 - 4x + 6y + 4 = 0$ a forma estándar.

**6.3.4** Complete cuadrados: $x^2 + y^2 + 2x - 8y + 8 = 0$.

**6.3.5** Convierta $2x^2 + 2y^2 - 8x + 12y - 10 = 0$ a forma estándar.

---

### 6.4 Posición de puntos ⭐⭐

**6.4.1** Determine si el punto $(2, 3)$ está dentro, sobre o fuera del círculo $x^2 + y^2 = 25$.

**6.4.2** ¿El punto $(5, 0)$ está dentro, sobre o fuera del círculo $(x - 2)^2 + (y - 1)^2 = 16$?

**6.4.3** Verifique si $(1, 1)$ está sobre el círculo $x^2 + y^2 - 2x - 2y + 1 = 0$.

**6.4.4** Determine la posición del origen respecto al círculo $(x - 3)^2 + (y - 4)^2 = 9$.

**6.4.5** ¿Para qué valores de $k$ el punto $(k, k)$ está sobre el círculo $x^2 + y^2 = 50$?

---

### 6.5 Recta tangente ⭐⭐⭐

**6.5.1** Encuentre la ecuación de la recta tangente al círculo $x^2 + y^2 = 25$ en el punto $(3, 4)$.

**6.5.2** Determine la tangente al círculo $(x - 1)^2 + (y - 2)^2 = 10$ en el punto $(4, 3)$.

**6.5.3** Escriba la ecuación de la tangente al círculo $x^2 + y^2 = 13$ en el punto $(2, 3)$.

**6.5.4** Encuentre las ecuaciones de las tangentes al círculo $x^2 + y^2 = 25$ que son paralelas a $3x + 4y = 0$.

**6.5.5** Determine la ecuación de la tangente al círculo $(x - 2)^2 + (y + 1)^2 = 5$ en el punto $(3, 1)$.

---

### 6.6 Intersección con rectas ⭐⭐⭐

**6.6.1** Encuentre los puntos de intersección del círculo $x^2 + y^2 = 25$ con la recta $y = x + 1$.

**6.6.2** Determine si la recta $y = 2x + 3$ interseca, es tangente o no toca al círculo $x^2 + y^2 = 5$.

**6.6.3** Encuentre los puntos donde el círculo $(x - 1)^2 + (y - 1)^2 = 10$ interseca al eje $x$.

**6.6.4** ¿En qué puntos el círculo $x^2 + y^2 - 4x - 6y + 9 = 0$ corta a la recta $y = x$?

**6.6.5** Determine $k$ para que la recta $y = x + k$ sea tangente al círculo $x^2 + y^2 = 8$.

---

## 7. Elipses

### Teoría breve

**Definición:** Lugar geométrico de puntos cuya suma de distancias a dos puntos fijos (focos) es constante.

**Ecuación estándar con centro en el origen:**

1. **Eje mayor horizontal:**
   $$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1 \quad (a > b)$$
   - Focos: $(\pm c, 0)$ donde $c^2 = a^2 - b^2$
   - Vértices: $(\pm a, 0)$
   - Covértices: $(0, \pm b)$

2. **Eje mayor vertical:**
   $$\frac{x^2}{b^2} + \frac{y^2}{a^2} = 1 \quad (a > b)$$
   - Focos: $(0, \pm c)$ donde $c^2 = a^2 - b^2$
   - Vértices: $(0, \pm a)$
   - Covértices: $(\pm b, 0)$

**Ecuación con centro en $(h, k)$:**
$$\frac{(x-h)^2}{a^2} + \frac{(y-k)^2}{b^2} = 1$$

**Elementos importantes:**
- $a$: semieje mayor
- $b$: semieje menor
- $c$: distancia del centro al foco
- Relación: $c^2 = a^2 - b^2$ (siempre $c < a$)
- Excentricidad: $e = \frac{c}{a}$ donde $0 < e < 1$
- Eje mayor: $2a$
- Eje menor: $2b$
- Distancia focal: $2c$

**Propiedades:**
- Si $a = b$, la elipse es un círculo
- Cuanto más cercana a $1$ es la excentricidad, más "alargada" es la elipse
- La suma de distancias de cualquier punto a los focos es $2a$

---

### 7.1 Elementos de la elipse ⭐

**7.1.1** Para la elipse $\frac{x^2}{25} + \frac{y^2}{16} = 1$, encuentre $a$, $b$, $c$, vértices, focos y excentricidad.

**7.1.2** Determine los elementos de $\frac{x^2}{9} + \frac{y^2}{25} = 1$.

**7.1.3** Para $\frac{x^2}{36} + \frac{y^2}{4} = 1$, encuentre vértices, focos y longitud de ejes.

**7.1.4** Encuentre los elementos de $\frac{x^2}{16} + \frac{y^2}{12} = 1$.

**7.1.5** Determine la excentricidad de $\frac{x^2}{100} + \frac{y^2}{64} = 1$.

---

### 7.2 Ecuación de la elipse ⭐⭐

**7.2.1** Escriba la ecuación de la elipse con centro en el origen, focos en $(\pm 3, 0)$ y vértices en $(\pm 5, 0)$.

**7.2.2** Encuentre la ecuación de la elipse con vértices en $(0, \pm 6)$ y focos en $(0, \pm 4)$.

**7.2.3** Escriba la ecuación de la elipse con centro en el origen, un vértice en $(0, 8)$ y excentricidad $e = \frac{3}{4}$.

**7.2.4** Determine la ecuación de la elipse con focos en $(\pm 2, 0)$ y eje mayor de longitud $10$.

**7.2.5** Encuentre la ecuación de la elipse con centro en el origen que pasa por $(3, 2)$ y $(4, 0)$.

---

### 7.3 Elipses con centro en $(h, k)$ ⭐⭐

**7.3.1** Encuentre centro, vértices y focos de $\frac{(x-2)^2}{16} + \frac{(y-1)^2}{9} = 1$.

**7.3.2** Determine los elementos de $\frac{(x+1)^2}{25} + \frac{(y-3)^2}{9} = 1$.

**7.3.3** Escriba la ecuación de la elipse con centro $(2, -1)$, vértices en $(2, 3)$ y $(2, -5)$, y focos en $(2, 2)$ y $(2, -4)$.

**7.3.4** Encuentre la ecuación de la elipse con centro $(-3, 2)$, un vértice en $(1, 2)$ y un foco en $(-1, 2)$.

**7.3.5** Determine centro y vértices de $\frac{(x-1)^2}{4} + \frac{(y+2)^2}{16} = 1$.

---

### 7.4 Completar cuadrados ⭐⭐⭐

**7.4.1** Convierta $4x^2 + 9y^2 - 16x + 18y - 11 = 0$ a forma estándar.

**7.4.2** Escriba $9x^2 + 4y^2 + 36x - 8y + 4 = 0$ en forma estándar.

**7.4.3** Convierta $25x^2 + 16y^2 - 100x + 96y - 156 = 0$ a forma estándar.

**7.4.4** Complete cuadrados: $x^2 + 4y^2 - 6x + 16y + 21 = 0$.

**7.4.5** Convierta $16x^2 + 25y^2 + 32x - 150y - 159 = 0$ a forma estándar.

---

### 7.5 Aplicaciones ⭐⭐⭐

**7.5.1** Una elipse tiene focos en $(\pm 4, 0)$ y pasa por el punto $(4, 3)$. Encuentre su ecuación.

**7.5.2** Un arco elíptico tiene $20$ m de ancho y $10$ m de alto en el centro. Escriba su ecuación si el origen está en el centro de la base.

**7.5.3** Un planeta orbita el Sol en una trayectoria elíptica. Si el semieje mayor es $150$ millones de km y la excentricidad es $0.2$, encuentre la distancia más cercana y más lejana al Sol.

**7.5.4** Demuestre que la suma de distancias desde cualquier punto de $\frac{x^2}{25} + \frac{y^2}{9} = 1$ a los focos es constante.

**7.5.5** Una piscina elíptica tiene ejes de $12$ m y $8$ m. Si se coloca en un sistema de coordenadas con centro en el origen, ¿cuál es su ecuación?

---

## 8. Parábolas

### Teoría breve

**Definición:** Lugar geométrico de puntos equidistantes de un punto fijo (foco) y una recta fija (directriz).

**Ecuaciones estándar con vértice en el origen:**

1. **Eje focal horizontal (abre derecha):**
   $$y^2 = 4px \quad (p > 0)$$
   - Foco: $(p, 0)$
   - Directriz: $x = -p$
   - Abre hacia la **derecha**

2. **Eje focal horizontal (abre izquierda):**
   $$y^2 = -4px \quad (p > 0)$$
   - Foco: $(-p, 0)$
   - Directriz: $x = p$
   - Abre hacia la **izquierda**

3. **Eje focal vertical (abre arriba):**
   $$x^2 = 4py \quad (p > 0)$$
   - Foco: $(0, p)$
   - Directriz: $y = -p$
   - Abre hacia **arriba**

4. **Eje focal vertical (abre abajo):**
   $$x^2 = -4py \quad (p > 0)$$
   - Foco: $(0, -p)$
   - Directriz: $y = p$
   - Abre hacia **abajo**

**Ecuación con vértice en $(h, k)$:**
- Vertical: $(x - h)^2 = 4p(y - k)$
- Horizontal: $(y - k)^2 = 4p(x - h)$

**Elementos importantes:**
- $p$: distancia del vértice al foco (también del vértice a la directriz)
- Vértice: punto donde la parábola cambia de dirección
- Eje de simetría: recta perpendicular a la directriz que pasa por el foco
- Lado recto: segmento perpendicular al eje focal que pasa por el foco, longitud $= |4p|$

**Forma general:**
- Vertical: $x^2 + Dx + Ey + F = 0$ o $y = ax^2 + bx + c$
- Horizontal: $y^2 + Dx + Ey + F = 0$

---

### 8.1 Elementos de la parábola ⭐

**8.1.1** Para $y^2 = 8x$, encuentre el foco, directriz, vértice y dirección de apertura.

**8.1.2** Determine los elementos de $x^2 = 12y$.

**8.1.3** Para $y^2 = -16x$, encuentre foco, directriz y hacia dónde abre.

**8.1.4** Encuentre los elementos de $x^2 = -20y$.

**8.1.5** Determine $p$ para $y^2 = 4px$ si el foco está en $(3, 0)$.

---

### 8.2 Ecuación de la parábola ⭐⭐

**8.2.1** Escriba la ecuación de la parábola con vértice en el origen y foco en $(0, 3)$.

**8.2.2** Encuentre la ecuación de la parábola con vértice en el origen y directriz $x = -4$.

**8.2.3** Determine la ecuación de la parábola con foco en $(2, 0)$ y directriz $x = -2$.

**8.2.4** Escriba la ecuación de la parábola con vértice en el origen que pasa por $(4, 8)$ y abre hacia arriba.

**8.2.5** Encuentre la ecuación de la parábola con vértice en el origen, eje focal vertical, y lado recto de longitud $12$.

---

### 8.3 Parábolas con vértice en $(h, k)$ ⭐⭐

**8.3.1** Encuentre vértice, foco y directriz de $(x - 2)^2 = 8(y - 1)$.

**8.3.2** Determine los elementos de $(y + 1)^2 = -12(x - 3)$.

**8.3.3** Escriba la ecuación de la parábola con vértice en $(1, -2)$ y foco en $(1, 0)$.

**8.3.4** Encuentre la ecuación de la parábola con vértice en $(-2, 3)$, eje vertical, y que pasa por $(0, 7)$.

**8.3.5** Determine vértice y foco de $(x + 3)^2 = -4(y - 2)$.

---

### 8.4 Completar cuadrados ⭐⭐⭐

**8.4.1** Convierta $y^2 - 6y - 8x + 1 = 0$ a forma estándar.

**8.4.2** Escriba $x^2 + 4x - 12y + 28 = 0$ en forma estándar.

**8.4.3** Convierta $y^2 + 8y + 4x + 20 = 0$ a forma estándar.

**8.4.4** Complete cuadrados: $x^2 - 6x - 16y + 41 = 0$.

**8.4.5** Convierta $y^2 - 4y + 8x - 12 = 0$ a forma estándar.

---

### 8.5 Forma $y = ax^2 + bx + c$ ⭐⭐

**8.5.1** Para $y = x^2 - 4x + 3$, encuentre el vértice y el foco.

**8.5.2** Determine vértice, foco y directriz de $y = -2x^2 + 8x - 5$.

**8.5.3** Escriba $y = x^2 + 6x + 11$ en forma estándar $(x - h)^2 = 4p(y - k)$.

**8.5.4** Convierta $y = -\frac{1}{2}x^2 + 2x + 1$ a forma estándar y encuentre el foco.

**8.5.5** Para $y = 3x^2 - 12x + 10$, encuentre vértice y directriz.

---

### 8.6 Aplicaciones ⭐⭐⭐

**8.6.1** Un puente colgante tiene cables que forman una parábola. Si el cable tiene $100$ m de largo y cuelga $25$ m en el centro, encuentre la ecuación de la parábola.

**8.6.2** Un reflector parabólico tiene $12$ cm de diámetro y $4$ cm de profundidad. ¿Dónde debe colocarse la fuente de luz (foco)?

**8.6.3** Una antena parabólica tiene $3$ m de diámetro y $0.75$ m de profundidad. Encuentre la ecuación de su perfil y la posición del receptor.

**8.6.4** Un chorro de agua sigue una trayectoria parabólica. Si alcanza una altura máxima de $4$ m a una distancia horizontal de $2$ m del origen y cae al suelo a $4$ m, encuentre la ecuación.

**8.6.5** Demuestre que cualquier punto de la parábola $y^2 = 8x$ equidista del foco y la directriz.

---

## 9. Hipérbolas

### Teoría breve

**Definición:** Lugar geométrico de puntos donde la diferencia de distancias a dos puntos fijos (focos) es constante.

**Ecuación estándar con centro en el origen:**

1. **Eje transversal horizontal:**
   $$\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$$
   - Focos: $(\pm c, 0)$ donde $c^2 = a^2 + b^2$
   - Vértices: $(\pm a, 0)$
   - Asíntotas: $y = \pm \frac{b}{a}x$

2. **Eje transversal vertical:**
   $$\frac{y^2}{a^2} - \frac{x^2}{b^2} = 1$$
   - Focos: $(0, \pm c)$ donde $c^2 = a^2 + b^2$
   - Vértices: $(0, \pm a)$
   - Asíntotas: $y = \pm \frac{a}{b}x$

**Ecuación con centro en $(h, k)$:**
$$\frac{(x-h)^2}{a^2} - \frac{(y-k)^2}{b^2} = 1 \quad \text{o} \quad \frac{(y-k)^2}{a^2} - \frac{(x-h)^2}{b^2} = 1$$

**Elementos importantes:**
- $a$: distancia del centro a cada vértice
- $b$: parámetro relacionado con las asíntotas
- $c$: distancia del centro a cada foco
- Relación: $c^2 = a^2 + b^2$ (siempre $c > a$)
- Excentricidad: $e = \frac{c}{a}$ donde $e > 1$
- Eje transversal: $2a$ (contiene los vértices)
- Eje conjugado: $2b$
- Distancia focal: $2c$

**Asíntotas:** Rectas a las que se aproxima la hipérbola en el infinito.
- Horizontal: $y - k = \pm \frac{b}{a}(x - h)$
- Vertical: $y - k = \pm \frac{a}{b}(x - h)$

**Propiedades:**
- La hipérbola tiene dos ramas separadas
- La diferencia de distancias de cualquier punto a los focos es $2a$
- Las asíntotas pasan por el centro
- Cuanto mayor es la excentricidad, más "abiertas" son las ramas

---

### 9.1 Elementos de la hipérbola ⭐

**9.1.1** Para $\frac{x^2}{9} - \frac{y^2}{16} = 1$, encuentre $a$, $b$, $c$, vértices, focos, asíntotas y excentricidad.

**9.1.2** Determine los elementos de $\frac{y^2}{25} - \frac{x^2}{9} = 1$.

**9.1.3** Para $\frac{x^2}{16} - \frac{y^2}{9} = 1$, encuentre vértices, focos y ecuaciones de las asíntotas.

**9.1.4** Encuentre los elementos de $\frac{y^2}{4} - \frac{x^2}{12} = 1$.

**9.1.5** Determine la excentricidad de $\frac{x^2}{36} - \frac{y^2}{64} = 1$.

---

### 9.2 Ecuación de la hipérbola ⭐⭐

**9.2.1** Escriba la ecuación de la hipérbola con centro en el origen, focos en $(\pm 5, 0)$ y vértices en $(\pm 3, 0)$.

**9.2.2** Encuentre la ecuación de la hipérbola con vértices en $(0, \pm 4)$ y focos en $(0, \pm 5)$.

**9.2.3** Escriba la ecuación de la hipérbola con centro en el origen, vértices en $(\pm 6, 0)$ y asíntotas $y = \pm \frac{2}{3}x$.

**9.2.4** Determine la ecuación de la hipérbola con focos en $(0, \pm 10)$ y eje transversal de longitud $12$.

**9.2.5** Encuentre la ecuación de la hipérbola con centro en el origen, excentricidad $e = \frac{5}{3}$ y vértices en $(\pm 3, 0)$.

---

### 9.3 Hipérbolas con centro en $(h, k)$ ⭐⭐

**9.3.1** Encuentre centro, vértices, focos y asíntotas de $\frac{(x-2)^2}{9} - \frac{(y-1)^2}{16} = 1$.

**9.3.2** Determine los elementos de $\frac{(y+2)^2}{25} - \frac{(x-3)^2}{16} = 1$.

**9.3.3** Escriba la ecuación de la hipérbola con centro $(1, -1)$, vértices en $(4, -1)$ y $(-2, -1)$, y focos en $(6, -1)$ y $(-4, -1)$.

**9.3.4** Encuentre la ecuación de la hipérbola con centro $(-2, 3)$, un vértice en $(-2, 7)$ y un foco en $(-2, 8)$.

**9.3.5** Determine las asíntotas de $\frac{(x+1)^2}{4} - \frac{(y-2)^2}{9} = 1$.

---

### 9.4 Completar cuadrados ⭐⭐⭐

**9.4.1** Convierta $x^2 - 4y^2 - 6x + 16y - 23 = 0$ a forma estándar.

**9.4.2** Escriba $9y^2 - 4x^2 - 18y - 16x - 43 = 0$ en forma estándar.

**9.4.3** Convierta $4x^2 - 9y^2 - 8x + 36y - 68 = 0$ a forma estándar.

**9.4.4** Complete cuadrados: $16x^2 - 9y^2 + 64x + 18y - 89 = 0$.

**9.4.5** Convierta $y^2 - 4x^2 - 4y + 24x - 36 = 0$ a forma estándar.

---

### 9.5 Aplicaciones ⭐⭐⭐

**9.5.1** Dos estaciones de radio están a $200$ km de distancia. Un barco recibe una señal de una estación $0.001$ segundos antes que de la otra. Si las ondas viajan a $300,000$ km/s, encuentre la ecuación de la hipérbola donde puede estar el barco.

**9.5.2** Las torres de enfriamiento de una planta nuclear tienen forma hiperbólica. Si la base tiene $20$ m de radio, la parte más estrecha tiene $10$ m de radio y está a $50$ m de altura, encuentre la ecuación del perfil.

**9.5.3** Demuestre que la diferencia de distancias desde cualquier punto de $\frac{x^2}{9} - \frac{y^2}{16} = 1$ a los focos es constante.

**9.5.4** Un cometa sigue una trayectoria hiperbólica alrededor del Sol. Si el Sol está en un foco, el vértice más cercano está a $100$ millones de km y la excentricidad es $1.5$, encuentre la ecuación de la trayectoria.

**9.5.5** Las asíntotas de una hipérbola son $y = \pm 2x$ y la hipérbola pasa por $(2, 3)$. Encuentre su ecuación.

---

## 10. Soluciones

<details>
<summary><b>Ver soluciones - Sección 1.1 (Distancia entre puntos)</b></summary>

### Soluciones Ejercicio 1.1

**1.1.1** $d(A, B) = \sqrt{(4-1)^2 + (6-2)^2} = \sqrt{9 + 16} = \sqrt{25} = 5$

**1.1.2** $d(P, Q) = \sqrt{(3-0)^2 + (4-0)^2} = \sqrt{9 + 16} = 5$

**1.1.3** $d(M, N) = \sqrt{(3-(-2))^2 + (-7-5)^2} = \sqrt{25 + 144} = \sqrt{169} = 13$

**1.1.4** $d(C, D) = \sqrt{(2-(-1))^2 + (3-(-1))^2} = \sqrt{9 + 16} = 5$

**1.1.5** $d(R, S) = \sqrt{(0-5)^2 + (12-0)^2} = \sqrt{25 + 144} = 13$

**1.1.6** $d(A, B) = \sqrt{(-3-(-3))^2 + (-2-4)^2} = \sqrt{0 + 36} = 6$

**1.1.7** $d(P, Q) = \sqrt{(-1-7)^2 + (2-2)^2} = \sqrt{64} = 8$

**1.1.8** $d(M, N) = \sqrt{(0-0)^2 + (3-(-5))^2} = \sqrt{64} = 8$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 1.2 (Punto medio)</b></summary>

### Soluciones Ejercicio 1.2

**1.2.1** $M = \left(\frac{2+6}{2}, \frac{4+8}{2}\right) = (4, 6)$

**1.2.2** $M = \left(\frac{0+10}{2}, \frac{0+6}{2}\right) = (5, 3)$

**1.2.3** $M = \left(\frac{-3+7}{2}, \frac{5-1}{2}\right) = (2, 2)$

**1.2.4** $M = \left(\frac{-4+2}{2}, \frac{-2+6}{2}\right) = (-1, 2)$

**1.2.5** $M = \left(\frac{1+5}{2}, \frac{9+3}{2}\right) = (3, 6)$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 1.3 (División de segmentos)</b></summary>

### Soluciones Ejercicio 1.3

**1.3.1** Razón $1:2$ (más cerca de $A$)

$$P = \left(\frac{2(1) + 1(7)}{1+2}, \frac{2(2) + 1(8)}{1+2}\right) = \left(\frac{9}{3}, \frac{12}{3}\right) = (3, 4)$$

**1.3.2** Razón $2:1$

$$P = \left(\frac{1(0) + 2(6)}{2+1}, \frac{1(0) + 2(9)}{2+1}\right) = (4, 6)$$

**1.3.3** Primer punto de división (razón $1:2$)

$$P = \left(\frac{2(-2) + 1(4)}{3}, \frac{2(4) + 1(-2)}{3}\right) = (0, 2)$$

**1.3.4** Razón $3:5$

$$P = \left(\frac{5(-3) + 3(5)}{8}, \frac{5(1) + 3(7)}{8}\right) = (0, \frac{26}{8}) = (0, 3.25)$$

**1.3.5** Tres partes iguales:
- Primer punto (razón $1:2$): $P_1 = (3, 2)$
- Segundo punto (razón $2:1$): $P_2 = (6, 4)$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 1.4 (Problemas con triángulos)</b></summary>

### Soluciones Ejercicio 1.4

**1.4.1** Lados:
- $AB = 4$
- $AC = 3$
- $BC = \sqrt{(0-4)^2 + (3-0)^2} = 5$

Perímetro: $4 + 3 + 5 = 12$

---

**1.4.2** Área usando la fórmula base × altura:

Base $AB = 3$, altura = $4$

Área $= \frac{1}{2} \times 3 \times 4 = 6$

---

**1.4.3** Distancias:
- $AB = 5$
- $BC = 5$
- $AC = 10$

Como $AB = BC$, es **isósceles**.

---

**1.4.4** Usando la fórmula del determinante:

$$\text{Área} = \frac{1}{2}|(-2)(5-(-2)) + 4((-2)-3) + 1(3-5)|$$
$$= \frac{1}{2}|-14 - 20 - 2| = \frac{1}{2} \times 36 = 18$$

---

**1.4.5** Distancias:
- $PQ = \sqrt{16 + 9} = 5$
- $QR = \sqrt{9 + 36} = \sqrt{45} = 3\sqrt{5}$
- $PR = \sqrt{1 + 9} = \sqrt{10}$

Perímetro: $5 + 3\sqrt{5} + \sqrt{10} \approx 15.87$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 1.5 (Problemas geométricos)</b></summary>

### Soluciones Ejercicio 1.5

**1.5.1** Verificar si son colineales:

Pendiente $AB = \frac{4-2}{3-1} = 1$

Pendiente $BC = \frac{6-4}{5-3} = 1$

Como las pendientes son iguales, **son colineales**.

---

**1.5.2** Verificar con teorema de Pitágoras:

- $AB = 5$
- $BC = 5$
- $AC = 5\sqrt{2}$

$(5)^2 + (5)^2 = 50 = (5\sqrt{2})^2$ ✓

Es **rectángulo** en $B$.

---

**1.5.3** En un paralelogramo, las diagonales se bisecan.

Punto medio de $AC = \left(\frac{1+5}{2}, \frac{2+6}{2}\right) = (3, 4)$

Este debe ser también el punto medio de $BD$:

$$\frac{4+x_D}{2} = 3 \Rightarrow x_D = 2$$
$$\frac{3+y_D}{2} = 4 \Rightarrow y_D = 5$$

**$D(2, 5)$**

---

**1.5.4** Calcular las cuatro distancias:
- $AB = BC = CD = DA = \sqrt{18}$

Todas las distancias son iguales, por lo tanto es un **rombo** (o podría ser cuadrado si también los ángulos son rectos).

---

**1.5.5** Puntos en eje $y$: $(0, y)$

Distancia a $P(3, 1)$:

$$\sqrt{9 + (y-1)^2} = 5$$
$$9 + (y-1)^2 = 25$$
$$(y-1)^2 = 16$$
$$y = 5 \text{ o } y = -3$$

**Puntos:** $(0, 5)$ y $(0, -3)$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 2.1 (Translación de puntos)</b></summary>

### Soluciones Ejercicio 2.1

**2.1.1** $A'(2+4, 3+1) = (6, 4)$

**2.1.2** $P'(-1+3, 5-2) = (2, 3)$

**2.1.3** $M'(0-3, 0+4) = (-3, 4)$

**2.1.4** $Q'(5-5, -2+2) = (0, 0)$

**2.1.5** Vector: $\vec{v} = (7-3, 8-5) = (4, 3)$

**2.1.6** $P(4-2, 1-(-3)) = (2, 4)$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 2.2 (Translación de figuras)</b></summary>

### Soluciones Ejercicio 2.2

**2.2.1** Nuevos vértices:
- $A'(3, 1)$
- $B'(5, 1)$
- $C'(4, 3)$

**2.2.2** Nuevos vértices:
- $P'(-1, 3)$
- $Q'(1, 3)$
- $R'(1, 5)$
- $S'(-1, 5)$

**2.2.3** Segmento trasladado:
- $A'(3, -3)$
- $B'(7, -1)$

Longitud original: $\sqrt{16+4} = 2\sqrt{5}$

Longitud trasladada: $\sqrt{16+4} = 2\sqrt{5}$ (se preserva)

**2.2.4** Vector para llevar $A(1,2)$ al origen: $\vec{v} = (-1, -2)$

**2.2.5** Nuevo centro: $C'(2, 7)$, radio: $4$ (sin cambio)

</details>

---

<details>
<summary><b>Ver soluciones - Sección 2.3 (Translación de ecuaciones)</b></summary>

### Soluciones Ejercicio 2.3

**2.3.1** Ecuación trasladada: $y - 2 = (x - 3)^2$

O simplificando: $y = (x-3)^2 + 2$

**2.3.2** Nueva ecuación: $y = 2x + 4$

**2.3.3** Vértice original: $(0, -4)$

Nuevo vértice: $(2, 1)$

Ecuación: $y - 1 = (x - 2)^2 - 4$

Simplificando: $y = (x-2)^2 - 3$

**2.3.4** $(x-2)^2 + (y+1)^2 = 9$

**2.3.5** Translación vertical de $-3$ unidades: $\vec{v} = (0, -3)$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 2.4 (Composición de translaciones)</b></summary>

### Soluciones Ejercicio 2.4

**2.4.1** $P \to P'(2, 3) \to P''(3, 2)$

**2.4.2** $\vec{v} = (4-3, 2+5) = (1, 7)$

**2.4.3** $P(x, y) \to P'(x+a, y+b) \to P''(x, y)$

El punto vuelve a su posición original.

**2.4.4** $\vec{v}_{\text{total}} = (3+0-1, 0+4-1) = (2, 3)$

**2.4.5** Ejemplo: $P(1, 0)$

$T_{(2,3)} \circ T_{(1,-1)}$: $P \to (2, -1) \to (4, 2)$

$T_{(1,-1)} \circ T_{(2,3)}$: $P \to (3, 3) \to (4, 2)$ ✓

</details>

---

<details>
<summary><b>Ver soluciones - Sección 3.1 (Rotaciones alrededor del origen)</b></summary>

### Soluciones Ejercicio 3.1

**3.1.1** $(1, 0) \xrightarrow{90°} (0, 1)$

**3.1.2** $(0, 1) \xrightarrow{90°} (-1, 0)$

**3.1.3** $(2, 3) \xrightarrow{180°} (-2, -3)$

**3.1.4** $(4, 0) \xrightarrow{270°} (0, -4)$

**3.1.5** $(-1, 2) \xrightarrow{-90°} (2, 1)$

**3.1.6** $(3, 3) \xrightarrow{180°} (-3, -3)$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 3.2 (Rotaciones con ángulos especiales)</b></summary>

### Soluciones Ejercicio 3.2

**3.2.1** $\theta = 45°$

$$x' = 2\cos(45°) - 0\sin(45°) = 2 \times \frac{\sqrt{2}}{2} = \sqrt{2}$$
$$y' = 2\sin(45°) + 0\cos(45°) = \sqrt{2}$$

**$P'(\sqrt{2}, \sqrt{2})$**

---

**3.2.2** $Q(\sqrt{2}, \sqrt{2}) \xrightarrow{45°}$

$$x' = \sqrt{2} \times \frac{\sqrt{2}}{2} - \sqrt{2} \times \frac{\sqrt{2}}{2} = 0$$
$$y' = \sqrt{2} \times \frac{\sqrt{2}}{2} + \sqrt{2} \times \frac{\sqrt{2}}{2} = 2$$

**$Q'(0, 2)$**

---

**3.2.3** $\theta = 60°$

$$x' = 1 \times \frac{1}{2} - 0 = \frac{1}{2}$$
$$y' = 1 \times \frac{\sqrt{3}}{2} = \frac{\sqrt{3}}{2}$$

**$A'\left(\frac{1}{2}, \frac{\sqrt{3}}{2}\right)$**

---

**3.2.4** $\theta = 30°$

$$x' = 0 \times \cos(30°) - 4 \times \sin(30°) = -2$$
$$y' = 0 \times \sin(30°) + 4 \times \cos(30°) = 2\sqrt{3}$$

**$B'(-2, 2\sqrt{3})$**

---

**3.2.5** $\theta = -45°$

$$x' = 2 \times \frac{\sqrt{2}}{2} + 2 \times \frac{\sqrt{2}}{2} = 2\sqrt{2}$$
$$y' = -2 \times \frac{\sqrt{2}}{2} + 2 \times \frac{\sqrt{2}}{2} = 0$$

**$C'(2\sqrt{2}, 0)$**

</details>

---

<details>
<summary><b>Ver soluciones - Sección 3.3 (Rotación de figuras)</b></summary>

### Soluciones Ejercicio 3.3

**3.3.1** Vértices rotados:
- $A(1, 0) \to A'(0, 1)$
- $B(0, 1) \to B'(-1, 0)$
- $C(0, 0) \to C'(0, 0)$

**3.3.2** Vértices rotados $180°$:
- $(1, 1) \to (-1, -1)$
- $(2, 1) \to (-2, -1)$
- $(2, 2) \to (-2, -2)$
- $(1, 2) \to (-1, -2)$

**3.3.3** Segmento rotado:
- $A(2, 0) \to A'(0, 2)$
- $B(4, 0) \to B'(0, 4)$

Longitud original: $2$

Longitud rotada: $2$ ✓ (preservada)

**3.3.4** Rotación $270°$ equivale a $-90°$:
- $(0, 0) \to (0, 0)$
- $(3, 0) \to (0, -3)$
- $(3, 1) \to (-1, -3)$
- $(0, 1) \to (-1, 0)$

**3.3.5** La rotación preserva distancias. La imagen también está a distancia $5$ del origen.

</details>

---

<details>
<summary><b>Ver soluciones - Sección 3.4 (Rotaciones alrededor de otros puntos)</b></summary>

### Soluciones Ejercicio 3.4

**3.4.1** Rotación de $P(3, 1)$ por $90°$ alrededor de $C(1, 1)$:

1. Trasladar: $P - C = (2, 0)$
2. Rotar $90°$: $(0, 2)$
3. Trasladar de vuelta: $(0, 2) + (1, 1) = (1, 3)$

**$P'(1, 3)$**

---

**3.4.2** Rotación de $Q(4, 2)$ por $180°$ alrededor de $C(2, 2)$:

1. Trasladar: $(2, 0)$
2. Rotar $180°$: $(-2, 0)$
3. Trasladar: $(-2, 0) + (2, 2) = (0, 2)$

**$Q'(0, 2)$**

---

**3.4.3** Rotación de $A(5, 3)$ por $90°$ alrededor de $C(3, 3)$:

1. Trasladar: $(2, 0)$
2. Rotar $90°$: $(0, 2)$
3. Trasladar: $(0, 2) + (3, 3) = (3, 5)$

**$A'(3, 5)$**

---

**3.4.4** Rotar cada vértice $180°$ alrededor de $(3, 1)$:
- $(2, 0) \to (4, 2)$
- $(4, 0) \to (2, 2)$
- $(3, 2) \to (3, 0)$

---

**3.4.5** Rotación de $(6, 2)$ por $270°$ alrededor de $(2, 2)$:

1. Trasladar: $(4, 0)$
2. Rotar $270°$: $(0, -4)$
3. Trasladar: $(2, -2)$

**Imagen: $(2, -2)$**

</details>

---

<details>
<summary><b>Ver soluciones - Sección 3.5 (Composición de rotaciones)</b></summary>

### Soluciones Ejercicio 3.5

**3.5.1** $P(1, 0) \xrightarrow{45°} (\frac{\sqrt{2}}{2}, \frac{\sqrt{2}}{2}) \xrightarrow{45°} (0, 1)$

---

**3.5.2** $Q(0, 1) \xrightarrow{60°} \xrightarrow{30°}$ equivale a $\xrightarrow{90°}$

Resultado final: $(-1, 0)$

---

**3.5.3** $R_\theta \circ R_{-\theta} = R_0 = I$ (identidad)

El punto queda en su posición original.

---

**3.5.4** Ejemplo con $P(1, 0)$:

$P \xrightarrow{90°} (0, 1) \xrightarrow{90°} (-1, 0)$

También: $P \xrightarrow{180°} (-1, 0)$ ✓

---

**3.5.5** $5 \times 72° = 360°$

Se necesitan **5 rotaciones** de $72°$.

</details>

---

<details>
<summary><b>Ver soluciones - Sección 4.1 (Ecuación de la recta - Forma básica)</b></summary>

### Soluciones Ejercicio 4.1

**4.1.1** $y - 3 = 2(x - 1)$

Simplificando: $y = 2x + 1$

**4.1.2** $y = -\frac{1}{2}x + 4$

**4.1.3** $m = \frac{8-2}{3-0} = 2$

$y = 2x + 2$

**4.1.4** $m = \frac{5-(-1)}{5-2} = 2$

$y + 1 = 2(x - 2)$

$y = 2x - 5$

**4.1.5** $y = 3x$

**4.1.6** $y = 4$ (recta horizontal)

**4.1.7** $x = 3$ (recta vertical)

**4.1.8** $y = 2$ (recta horizontal)

</details>

---

<details>
<summary><b>Ver soluciones - Sección 4.2 (Pendiente y ángulo de inclinación)</b></summary>

### Soluciones Ejercicio 4.2

**4.2.1** $m = \frac{8-2}{4-1} = 2$

**4.2.2** $3x - 4y + 12 = 0 \Rightarrow y = \frac{3}{4}x + 3$

$m = \frac{3}{4}$

**4.2.3** $\tan(45°) = 1$, entonces $m = 1$

**4.2.4** $m = \sqrt{3} = \tan\theta$

$\theta = 60°$

**4.2.5** $\tan\theta = -1$

$\theta = 135°$

**4.2.6** Perpendicular al eje $x$ es vertical: pendiente **indefinida**

</details>

---

<details>
<summary><b>Ver soluciones - Sección 4.3 (Rectas paralelas)</b></summary>

### Soluciones Ejercicio 4.3

**4.3.1** Pendiente: $m = 2$

$y - 5 = 2(x - 1)$

$y = 2x + 3$

**4.3.2** $3x + 4y = 12 \Rightarrow m = -\frac{3}{4}$

Recta paralela por origen: $y = -\frac{3}{4}x$

O en forma general: $3x + 4y = 0$

**4.3.3** Primera recta: $m_1 = 2$

Segunda: $2x - y + 5 = 0 \Rightarrow y = 2x + 5$, $m_2 = 2$

**Son paralelas** ✓

**4.3.4** Primera recta: $m_1 = -\frac{k}{3}$

Segunda: $m_2 = -\frac{2}{6} = -\frac{1}{3}$

Para paralelas: $-\frac{k}{3} = -\frac{1}{3}$

$k = 1$

**4.3.5** $y = -3$ (horizontal)

**4.3.6** $x - 2y + 4 = 0 \Rightarrow m = \frac{1}{2}$

$y - 3 = \frac{1}{2}(x + 1)$

$y = \frac{1}{2}x + \frac{7}{2}$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 4.4 (Rectas perpendiculares)</b></summary>

### Soluciones Ejercicio 4.4

**4.4.1** $m_1 = 3$, entonces $m_2 = -\frac{1}{3}$

$y = -\frac{1}{3}x$

**4.4.2** $x + 2y = 6 \Rightarrow m_1 = -\frac{1}{2}$

$m_2 = 2$

$y - 1 = 2(x - 4)$

$y = 2x - 7$

**4.4.3** $m_1 = \frac{2}{3}$, $m_2 = -\frac{3}{2}$

$m_1 \times m_2 = -1$ ✓ **Son perpendiculares**

**4.4.4** Punto medio de $AB$: $M(2, 1)$

Pendiente de $AB$: $m_1 = \frac{1}{2}$

Pendiente de mediatriz: $m_2 = -2$

$y - 1 = -2(x - 2)$

$y = -2x + 5$

**4.4.5** Primera: $m_1 = -\frac{k}{2}$

Segunda: $m_2 = 3$

Para perpendiculares: $-\frac{k}{2} \times 3 = -1$

$k = \frac{2}{3}$

**4.4.6** $2x - 5y + 10 = 0 \Rightarrow m_1 = \frac{2}{5}$

$m_2 = -\frac{5}{2}$

$y - 3 = -\frac{5}{2}(x + 2)$

$y = -\frac{5}{2}x - 2$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 4.5 (Intersección de rectas)</b></summary>

### Soluciones Ejercicio 4.5

**4.5.1** $2x + 1 = -x + 7$

$3x = 6 \Rightarrow x = 2$

$y = 5$

**Punto: $(2, 5)$**

**4.5.2** De la primera: $y = 5 - x$

Sustituyendo: $2x - (5-x) = 1$

$3x = 6 \Rightarrow x = 2$, $y = 3$

**Punto: $(2, 3)$**

**4.5.3** De la segunda: $x = y + 1$

Sustituyendo: $3(y+1) + 2y = 12$

$5y = 9 \Rightarrow y = \frac{9}{5}$, $x = \frac{14}{5}$

**Punto: $\left(\frac{14}{5}, \frac{9}{5}\right)$**

**4.5.4** $3x - 4 = -2x + 6$

$5x = 10 \Rightarrow x = 2$

$y = 2$

**Punto: $(2, 2)$**

**4.5.5** Ambas tienen pendiente $m = 2$

Son paralelas, **no se intersectan** ✓

</details>

---

<details>
<summary><b>Ver soluciones - Sección 4.6 (Distancia de punto a recta)</b></summary>

### Soluciones Ejercicio 4.6

**4.6.1** Recta: $3x + 4y - 12 = 0$

$$d = \frac{|3(1) + 4(2) - 12|}{\sqrt{9+16}} = \frac{|-1|}{5} = \frac{1}{5}$$

**4.6.2** Recta: $x + y - 4 = 0$

$$d = \frac{|0 + 0 - 4|}{\sqrt{2}} = \frac{4}{\sqrt{2}} = 2\sqrt{2}$$

**4.6.3** Recta: $2x - y + 3 = 0$

$$d = \frac{|2(2) - (-1) + 3|}{\sqrt{5}} = \frac{8}{\sqrt{5}} = \frac{8\sqrt{5}}{5}$$

**4.6.4** Recta por $(0,0)$ y $(3,4)$: $4x - 3y = 0$

$$d = \frac{|4(5) - 3(0)|}{\sqrt{16+9}} = \frac{20}{5} = 4$$

**4.6.5** Puntos en $y = x$: $(t, t)$

Distancia al origen: $\sqrt{2t^2} = \sqrt{2}$

$t = \pm 1$

**Puntos: $(1, 1)$ y $(-1, -1)$**

</details>

---

<details>
<summary><b>Ver soluciones - Sección 4.7 (Ángulos entre rectas)</b></summary>

### Soluciones Ejercicio 4.7

**4.7.1** $m_1 = 1$, $m_2 = 2$

$$\tan\theta = \left|\frac{1-2}{1+2}\right| = \frac{1}{3}$$

$$\theta = \arctan\left(\frac{1}{3}\right) \approx 18.43°$$

**4.7.2** $m_1 = \sqrt{3}$, $m_2 = 0$

$$\tan\theta = \sqrt{3}$$

$$\theta = 60°$$

**4.7.3** $m_1 = -1$, $m_2 = 1$

$$\tan\theta = \left|\frac{-1-1}{1-1}\right| = \text{indefinido}$$

$$\theta = 90°$$

**4.7.4** $m_1 = -2$, $m_2 = \frac{1}{3}$

$$\tan\theta = \left|\frac{-2-\frac{1}{3}}{1-\frac{2}{3}}\right| = \left|\frac{-\frac{7}{3}}{\frac{1}{3}}\right| = 7$$

$$\theta \approx 81.87°$$

**4.7.5** Rectas perpendiculares forman **$90°$**

</details>

---

<details>
<summary><b>Ver soluciones - Sección 4.8 (Problemas de aplicación)</b></summary>

### Soluciones Ejercicio 4.8

**4.8.1** Lado $AB$ es horizontal (de $(0,0)$ a $(4,0)$)

Altura desde $C(2,3)$ es perpendicular a $AB$ (vertical)

**Ecuación: $x = 2$**

---

**4.8.2** Mediatrices:

1. Mediatriz de $AB$: punto medio $(3, 0)$, perpendicular a horizontal

   **$x = 3$**

2. Mediatriz de $BC$: punto medio $(3, 4)$, perpendicular a vertical

   **$y = 4$**

3. Mediatriz de $AC$: punto medio $(0, 4)$, pendiente de $AC = -\frac{4}{3}$

   Pendiente de mediatriz: $\frac{3}{4}$

   **$y - 4 = \frac{3}{4}x$ o $3x - 4y + 16 = 0$**

---

**4.8.3** Intersección de $x = 3$ y $y = 4$:

**Circuncentro: $(3, 4)$**

---

**4.8.4** Recta por $(2, 3)$ con intersecciones $(a, 0)$ y $(0, b)$:

Área: $\frac{1}{2}|ab| = 12 \Rightarrow |ab| = 24$

Ecuación: $\frac{x}{a} + \frac{y}{b} = 1$

Pasa por $(2, 3)$: $\frac{2}{a} + \frac{3}{b} = 1$

Resolver sistema (dos posibles soluciones)...

---

**4.8.5** Recta equidistante de $A$ y $B$ es la mediatriz de $AB$:

Punto medio: $(2, 2)$

Pendiente $AB = 1$, pendiente mediatriz $= -1$

$y - 2 = -(x - 2)$

**$y = -x + 4$**

Pero debe pasar por $(1, 2)$:

Verificar: $2 = -1 + 4 = 3$ ✗

Corrección: la recta que pasa por $(1,2)$ y es perpendicular a $AB$:

$y - 2 = -(x - 1)$

**$y = -x + 3$**

</details>

---

<details>
<summary><b>Ver soluciones - Sección 5.1 (Identificar cónicas)</b></summary>

### Soluciones Ejercicio 5.1

**5.1.1** $x^2 + y^2 = 25$ → **Círculo** (coeficientes de $x^2$ e $y^2$ son iguales)

**5.1.2** $\frac{x^2}{16} + \frac{y^2}{9} = 1$ → **Elipse** (denominadores diferentes, ambos positivos)

**5.1.3** $y^2 = 8x$ → **Parábola** (solo una variable al cuadrado)

**5.1.4** $\frac{x^2}{9} - \frac{y^2}{16} = 1$ → **Hipérbola** (un término resta al otro)

**5.1.5** $4x^2 + 4y^2 = 36$ → $x^2 + y^2 = 9$ → **Círculo**

**5.1.6** $x^2 + 4y^2 = 16$ → $\frac{x^2}{16} + \frac{y^2}{4} = 1$ → **Elipse**

**5.1.7** $x^2 - 9y^2 = 9$ → $\frac{x^2}{9} - \frac{y^2}{1} = 1$ → **Hipérbola**

**5.1.8** $x^2 = -12y$ → **Parábola** (abre hacia abajo)

</details>

---

<details>
<summary><b>Ver soluciones - Sección 5.2 (Ecuación general a forma estándar)</b></summary>

### Soluciones Ejercicio 5.2

**5.2.1** $x^2 + y^2 - 4x + 6y - 12 = 0$

$(x^2 - 4x + 4) + (y^2 + 6y + 9) = 12 + 4 + 9$

$(x - 2)^2 + (y + 3)^2 = 25$ → **Círculo**

---

**5.2.2** $4x^2 + 9y^2 - 16x + 18y - 11 = 0$

$4(x^2 - 4x) + 9(y^2 + 2y) = 11$

$4(x^2 - 4x + 4) + 9(y^2 + 2y + 1) = 11 + 16 + 9$

$4(x - 2)^2 + 9(y + 1)^2 = 36$

$\frac{(x-2)^2}{9} + \frac{(y+1)^2}{4} = 1$ → **Elipse**

---

**5.2.3** $y^2 - 6y - 8x + 1 = 0$

$(y^2 - 6y + 9) = 8x - 1 + 9$

$(y - 3)^2 = 8(x + 1)$ → **Parábola**

---

**5.2.4** $x^2 - 4y^2 - 6x + 16y - 23 = 0$

$(x^2 - 6x) - 4(y^2 - 4y) = 23$

$(x^2 - 6x + 9) - 4(y^2 - 4y + 4) = 23 + 9 - 16$

$(x - 3)^2 - 4(y - 2)^2 = 16$

$\frac{(x-3)^2}{16} - \frac{(y-2)^2}{4} = 1$ → **Hipérbola**

---

**5.2.5** $9x^2 + 4y^2 + 36x - 8y + 4 = 0$

$9(x^2 + 4x) + 4(y^2 - 2y) = -4$

$9(x^2 + 4x + 4) + 4(y^2 - 2y + 1) = -4 + 36 + 4$

$9(x + 2)^2 + 4(y - 1)^2 = 36$

$\frac{(x+2)^2}{4} + \frac{(y-1)^2}{9} = 1$ → **Elipse**

---

**5.2.6** $(x^2 + 8x + 16) + (y^2 - 10y + 25) = -16 + 16 + 25$

$(x + 4)^2 + (y - 5)^2 = 25$ → **Círculo**

Centro: $(-4, 5)$, Radio: $5$

---

**5.2.7** $16(x^2 - 4x) + 25(y^2 + 6y) = 111$

$16(x^2 - 4x + 4) + 25(y^2 + 6y + 9) = 111 + 64 + 225$

$16(x - 2)^2 + 25(y + 3)^2 = 400$

$\frac{(x-2)^2}{25} + \frac{(y+3)^2}{16} = 1$ → **Elipse**

---

**5.2.8** $(x^2 - 8x + 16) = 12y - 4 + 16$

$(x - 4)^2 = 12(y + 1)$ → **Parábola**

Vértice: $(4, -1)$, abre hacia arriba, $p = 3$

---

**5.2.9** $9(x^2 + 4x) - 16(y^2 - 2y) = 124$

$9(x^2 + 4x + 4) - 16(y^2 - 2y + 1) = 124 + 36 - 16$

$9(x + 2)^2 - 16(y - 1)^2 = 144$

$\frac{(x+2)^2}{16} - \frac{(y-1)^2}{9} = 1$ → **Hipérbola**

---

**5.2.10** $(x^2 - 6x + 9) + (y^2 + 4y + 4) = 12 + 9 + 4$

$(x - 3)^2 + (y + 2)^2 = 25$ → **Círculo**

Centro: $(3, -2)$, Radio: $5$

---

**5.2.11** $25(x^2 + 4x) + 4(y^2 - 6y) = -36$

$25(x^2 + 4x + 4) + 4(y^2 - 6y + 9) = -36 + 100 + 36$

$25(x + 2)^2 + 4(y - 3)^2 = 100$

$\frac{(x+2)^2}{4} + \frac{(y-3)^2}{25} = 1$ → **Elipse**

Centro: $(-2, 3)$, $a = 5$ (vertical), $b = 2$

---

**5.2.12** $(y^2 + 8y + 16) = -12x + 20 + 16$

$(y + 4)^2 = -12(x - 3)$ → **Parábola**

Vértice: $(3, -4)$, abre hacia la izquierda, $p = -3$

---

**5.2.13** $4(x^2 - 6x) - (y^2 + 4y) = -28$

$4(x^2 - 6x + 9) - (y^2 + 4y + 4) = -28 + 36 - 4$

$4(x - 3)^2 - (y + 2)^2 = 4$

$(x - 3)^2 - \frac{(y+2)^2}{4} = 1$ → **Hipérbola**

Centro: $(3, -2)$, $a = 1$, $b = 2$

---

**5.2.14** $2(x^2 - 4x) + 2(y^2 + 6y) = 10$

$x^2 - 4x + y^2 + 6y = 5$

$(x^2 - 4x + 4) + (y^2 + 6y + 9) = 5 + 4 + 9$

$(x - 2)^2 + (y + 3)^2 = 18$ → **Círculo**

Centro: $(2, -3)$, Radio: $3\sqrt{2}$

---

**5.2.15** $9(x^2 - 2x) + 16(y^2 + 4y) = 71$

$9(x^2 - 2x + 1) + 16(y^2 + 4y + 4) = 71 + 9 + 64$

$9(x - 1)^2 + 16(y + 2)^2 = 144$

$\frac{(x-1)^2}{16} + \frac{(y+2)^2}{9} = 1$ → **Elipse**

Centro: $(1, -2)$, $a = 4$, $b = 3$

---

**5.2.16** $(x^2 + 6x + 9) = -16y + 7 + 9$

$(x + 3)^2 = -16(y - 1)$ → **Parábola**

Vértice: $(-3, 1)$, abre hacia abajo, $p = -4$

---

**5.2.17** $(x^2 + 2x) - 9(y^2 - 6y) = 80$

$(x^2 + 2x + 1) - 9(y^2 - 6y + 9) = 80 + 1 - 81$

$(x + 1)^2 - 9(y - 3)^2 = 0$

$(x + 1)^2 = 9(y - 3)^2$

$x + 1 = \pm 3(y - 3)$

→ **Par de rectas** (caso degenerado de hipérbola)

Rectas: $x - 3y + 10 = 0$ y $x + 3y - 8 = 0$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 5.3 (Usar el discriminante)</b></summary>

### Soluciones Ejercicio 5.3

**5.3.1** $3x^2 + 3y^2 - 6x + 12y - 5 = 0$

$A = 3$, $B = 0$, $C = 3$

$\Delta = 0^2 - 4(3)(3) = -36 < 0$ y $A = C$ → **Círculo**

---

**5.3.2** $2x^2 + 5y^2 - 4x + 10y - 7 = 0$

$A = 2$, $B = 0$, $C = 5$

$\Delta = -40 < 0$ y $A \neq C$ → **Elipse**

---

**5.3.3** $x^2 - 2xy + y^2 - 4x - 2y = 0$

$A = 1$, $B = -2$, $C = 1$

$\Delta = (-2)^2 - 4(1)(1) = 0$ → **Parábola**

---

**5.3.4** $4x^2 - y^2 + 8x + 6y - 9 = 0$

$A = 4$, $B = 0$, $C = -1$

$\Delta = 0 - 4(4)(-1) = 16 > 0$ → **Hipérbola**

---

**5.3.5** $x^2 + 2xy + y^2 + 3x - y + 5 = 0$

$A = 1$, $B = 2$, $C = 1$

$\Delta = 4 - 4 = 0$ → **Parábola**

</details>

---

<details>
<summary><b>Ver soluciones - Sección 6.1 (Ecuación del círculo)</b></summary>

### Soluciones Ejercicio 6.1

**6.1.1** $x^2 + y^2 = 25$

**6.1.2** $(x - 3)^2 + (y + 2)^2 = 16$

**6.1.3** $(x + 1)^2 + (y - 4)^2 = 7$

**6.1.4** Radio: $r = \sqrt{9 + 16} = 5$

Ecuación: $x^2 + y^2 = 25$

**6.1.5** Radio: $r = \sqrt{(-1-2)^2 + (5-1)^2} = 5$

Ecuación: $(x - 2)^2 + (y - 1)^2 = 25$

**6.1.6** Centro (punto medio): $\left(\frac{1+5}{2}, \frac{2+6}{2}\right) = (3, 4)$

Radio: $r = \frac{1}{2}\sqrt{16 + 16} = 2\sqrt{2}$

Ecuación: $(x - 3)^2 + (y - 4)^2 = 8$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 6.2 (Centro y radio)</b></summary>

### Soluciones Ejercicio 6.2

**6.2.1** Centro: $(0, 0)$, Radio: $6$

**6.2.2** Centro: $(2, -3)$, Radio: $4$

**6.2.3** Centro: $(-4, 1)$, Radio: $5$

**6.2.4** Centro: $(0, 5)$, Radio: $3$

**6.2.5** Centro: $(1, 1)$, Radio: $\sqrt{2}$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 6.3 (Completar cuadrados)</b></summary>

### Soluciones Ejercicio 6.3

**6.3.1** $(x^2 - 6x + 9) + (y^2 + 4y + 4) = 12 + 9 + 4$

$(x - 3)^2 + (y + 2)^2 = 25$

Centro: $(3, -2)$, Radio: $5$

---

**6.3.2** $(x^2 + 8x + 16) + (y^2 - 10y + 25) = -16 + 16 + 25$

$(x + 4)^2 + (y - 5)^2 = 25$

Centro: $(-4, 5)$, Radio: $5$

---

**6.3.3** $(x^2 - 4x + 4) + (y^2 + 6y + 9) = -4 + 4 + 9$

$(x - 2)^2 + (y + 3)^2 = 9$

Centro: $(2, -3)$, Radio: $3$

---

**6.3.4** $(x^2 + 2x + 1) + (y^2 - 8y + 16) = -8 + 1 + 16$

$(x + 1)^2 + (y - 4)^2 = 9$

Centro: $(-1, 4)$, Radio: $3$

---

**6.3.5** $2(x^2 - 4x) + 2(y^2 + 6y) = 10$

$x^2 - 4x + y^2 + 6y = 5$

$(x - 2)^2 + (y + 3)^2 = 18$

Centro: $(2, -3)$, Radio: $3\sqrt{2}$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 6.4 (Posición de puntos)</b></summary>

### Soluciones Ejercicio 6.4

**6.4.1** $d = \sqrt{4 + 9} = \sqrt{13} < 5$ → **Dentro**

**6.4.2** $d = \sqrt{9 + 1} = \sqrt{10} < 4$ → **Dentro**

**6.4.3** Sustituyendo: $1 + 1 - 2 - 2 + 1 = -1 \neq 0$ → **No está sobre**

Calculando distancia: centro $(1, 1)$, radio $1$

$d = \sqrt{0 + 0} = 0 < 1$ → **Dentro**

**6.4.4** $d = \sqrt{9 + 16} = 5 > 3$ → **Fuera**

**6.4.5** $k^2 + k^2 = 50$

$2k^2 = 50 \Rightarrow k = \pm 5$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 6.5 (Recta tangente)</b></summary>

### Soluciones Ejercicio 6.5

**6.5.1** Radio al punto: pendiente $= \frac{4}{3}$

Tangente: pendiente $= -\frac{3}{4}$

$y - 4 = -\frac{3}{4}(x - 3)$

$3x + 4y = 25$

---

**6.5.2** Centro $(1, 2)$, punto $(4, 3)$

Pendiente del radio: $\frac{1}{3}$

Tangente: $y - 3 = -3(x - 4)$

$3x + y = 15$

---

**6.5.3** Pendiente del radio: $\frac{3}{2}$

Tangente: $y - 3 = -\frac{2}{3}(x - 2)$

$2x + 3y = 13$

---

**6.5.4** Tangentes paralelas a $3x + 4y = 0$ (pendiente $-\frac{3}{4}$)

Distancia del centro al tangente = $5$

$\frac{|C|}{\sqrt{9+16}} = 5 \Rightarrow |C| = 25$

Ecuaciones: $3x + 4y = \pm 25$

---

**6.5.5** Radio: pendiente $= \frac{2}{1} = 2$

Tangente: $y - 1 = -\frac{1}{2}(x - 3)$

$x + 2y = 5$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 6.6 (Intersección con rectas)</b></summary>

### Soluciones Ejercicio 6.6

**6.6.1** Sustituyendo $y = x + 1$:

$x^2 + (x+1)^2 = 25$

$2x^2 + 2x - 24 = 0$

$x^2 + x - 12 = 0$

$(x+4)(x-3) = 0$

Puntos: $(-4, -3)$ y $(3, 4)$

---

**6.6.2** $x^2 + (2x+3)^2 = 5$

$5x^2 + 12x + 4 = 0$

Discriminante: $144 - 80 = 64 > 0$ → **Interseca en dos puntos**

---

**6.6.3** $y = 0$:

$(x-1)^2 + 1 = 10$

$(x-1)^2 = 9$

$x = 4$ o $x = -2$

Puntos: $(4, 0)$ y $(-2, 0)$

---

**6.6.4** Primero a forma estándar: $(x-2)^2 + (y-3)^2 = 4$

Con $y = x$: $(x-2)^2 + (x-3)^2 = 4$

$2x^2 - 10x + 9 = 0$

$x = \frac{10 \pm \sqrt{28}}{4} = \frac{5 \pm \sqrt{7}}{2}$

---

**6.6.5** Sustituyendo: $x^2 + (x+k)^2 = 8$

$2x^2 + 2kx + k^2 - 8 = 0$

Para tangencia, discriminante = $0$:

$4k^2 - 8(k^2 - 8) = 0$

$-4k^2 + 64 = 0$

$k = \pm 4$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 7.1 (Elementos de la elipse)</b></summary>

### Soluciones Ejercicio 7.1

**7.1.1** $\frac{x^2}{25} + \frac{y^2}{16} = 1$

- $a = 5$, $b = 4$
- $c = \sqrt{25-16} = 3$
- Vértices: $(\pm 5, 0)$
- Focos: $(\pm 3, 0)$
- Excentricidad: $e = \frac{3}{5}$

---

**7.1.2** $\frac{x^2}{9} + \frac{y^2}{25} = 1$

- $a = 5$, $b = 3$ (eje mayor vertical)
- $c = 4$
- Vértices: $(0, \pm 5)$
- Focos: $(0, \pm 4)$
- Excentricidad: $e = \frac{4}{5}$

---

**7.1.3** $a = 6$, $b = 2$, $c = \sqrt{32} = 4\sqrt{2}$

- Vértices: $(\pm 6, 0)$
- Focos: $(\pm 4\sqrt{2}, 0)$
- Eje mayor: $12$, eje menor: $4$

---

**7.1.4** $a = 4$, $b = \sqrt{12} = 2\sqrt{3}$, $c = 2$

- Vértices: $(\pm 4, 0)$
- Focos: $(\pm 2, 0)$
- Excentricidad: $e = \frac{1}{2}$

---

**7.1.5** $a = 10$, $b = 8$, $c = 6$

$e = \frac{6}{10} = \frac{3}{5}$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 7.2 (Ecuación de la elipse)</b></summary>

### Soluciones Ejercicio 7.2

**7.2.1** $a = 5$, $c = 3$

$b^2 = 25 - 9 = 16$

Ecuación: $\frac{x^2}{25} + \frac{y^2}{16} = 1$

---

**7.2.2** $a = 6$, $c = 4$ (eje vertical)

$b^2 = 36 - 16 = 20$

Ecuación: $\frac{x^2}{20} + \frac{y^2}{36} = 1$

---

**7.2.3** $a = 8$, $e = \frac{3}{4}$

$c = \frac{3}{4} \times 8 = 6$

$b^2 = 64 - 36 = 28$

Ecuación: $\frac{x^2}{28} + \frac{y^2}{64} = 1$

---

**7.2.4** $c = 2$, $2a = 10 \Rightarrow a = 5$

$b^2 = 25 - 4 = 21$

Ecuación: $\frac{x^2}{25} + \frac{y^2}{21} = 1$

---

**7.2.5** Pasa por $(3, 2)$ y $(4, 0)$:

De $(4, 0)$: $a^2 = 16$

De $(3, 2)$: $\frac{9}{16} + \frac{4}{b^2} = 1$

$\frac{4}{b^2} = \frac{7}{16} \Rightarrow b^2 = \frac{64}{7}$

Ecuación: $\frac{x^2}{16} + \frac{7y^2}{64} = 1$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 7.3 (Elipses con centro en (h,k))</b></summary>

### Soluciones Ejercicio 7.3

**7.3.1** $\frac{(x-2)^2}{16} + \frac{(y-1)^2}{9} = 1$

- Centro: $(2, 1)$
- $a = 4$, $b = 3$, $c = \sqrt{7}$
- Vértices: $(6, 1)$ y $(-2, 1)$
- Focos: $(2\pm\sqrt{7}, 1)$

---

**7.3.2** Centro: $(-1, 3)$, $a = 5$, $b = 3$, $c = 4$

- Vértices: $(4, 3)$ y $(-6, 3)$
- Focos: $(3, 3)$ y $(-5, 3)$

---

**7.3.3** Centro: $(2, -1)$

Distancia a vértices: $a = 4$

Distancia a focos: $c = 3$

$b^2 = 16 - 9 = 7$

Ecuación: $\frac{(x-2)^2}{7} + \frac{(y+1)^2}{16} = 1$

---

**7.3.4** Centro: $(-3, 2)$, $a = 4$, $c = 2$, $b^2 = 12$

Ecuación: $\frac{(x+3)^2}{16} + \frac{(y-2)^2}{12} = 1$

---

**7.3.5** Centro: $(1, -2)$

$a = 4$ (vertical), $b = 2$

- Vértices: $(1, 2)$ y $(1, -6)$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 7.4 (Completar cuadrados - Elipse)</b></summary>

### Soluciones Ejercicio 7.4

**7.4.1** $4(x^2 - 4x) + 9(y^2 + 2y) = 11$

$4(x-2)^2 + 9(y+1)^2 = 36$

$\frac{(x-2)^2}{9} + \frac{(y+1)^2}{4} = 1$

---

**7.4.2** $9(x^2 + 4x) + 4(y^2 - 2y) = -4$

$9(x+2)^2 + 4(y-1)^2 = 36$

$\frac{(x+2)^2}{4} + \frac{(y-1)^2}{9} = 1$

---

**7.4.3** $25(x^2 - 4x) + 16(y^2 + 6y) = 156$

$25(x-2)^2 + 16(y+3)^2 = 400$

$\frac{(x-2)^2}{16} + \frac{(y+3)^2}{25} = 1$

---

**7.4.4** $(x^2 - 6x) + 4(y^2 + 4y) = -21$

$(x-3)^2 + 4(y+2)^2 = 4$

$\frac{(x-3)^2}{4} + (y+2)^2 = 1$

---

**7.4.5** $16(x^2 + 2x) + 25(y^2 - 6y) = 159$

$16(x+1)^2 + 25(y-3)^2 = 400$

$\frac{(x+1)^2}{25} + \frac{(y-3)^2}{16} = 1$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 7.5 (Aplicaciones - Elipse)</b></summary>

### Soluciones Ejercicio 7.5

**7.5.1** $c = 4$, pasa por $(4, 3)$

Suma de distancias a focos: $d_1 + d_2 = 2a$

$\sqrt{0 + 9} + \sqrt{64 + 9} = 2a$

$3 + \sqrt{73} = 2a \Rightarrow a \approx 5.77$

$b^2 = a^2 - 16$

---

**7.5.2** Ancho $= 20$ m, alto $= 10$ m

$a = 10$, $b = 5$ (origen en centro de base, eje horizontal)

Ecuación: $\frac{x^2}{100} + \frac{(y-5)^2}{25} = 1$

---

**7.5.3** $a = 150$, $e = 0.2$

$c = 0.2 \times 150 = 30$

- Más cercano: $a - c = 120$ millones km
- Más lejano: $a + c = 180$ millones km

---

**7.5.4** $a = 5$, $c = 4$, focos $(\pm 4, 0)$

Para punto $(5, 0)$: $d_1 = 1$, $d_2 = 9$, suma $= 10 = 2a$ ✓

Para punto $(3, \frac{12}{5})$: verificar que suma $= 10$

---

**7.5.5** Ejes: $12$ m y $8$ m

$a = 6$, $b = 4$

Ecuación: $\frac{x^2}{36} + \frac{y^2}{16} = 1$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 8.1 (Elementos de la parábola)</b></summary>

### Soluciones Ejercicio 8.1

**8.1.1** $y^2 = 8x$

$4p = 8 \Rightarrow p = 2$

- Vértice: $(0, 0)$
- Foco: $(2, 0)$
- Directriz: $x = -2$
- Abre hacia la **derecha**

---

**8.1.2** $x^2 = 12y$

$4p = 12 \Rightarrow p = 3$

- Vértice: $(0, 0)$
- Foco: $(0, 3)$
- Directriz: $y = -3$
- Abre hacia **arriba**

---

**8.1.3** $y^2 = -16x$

$4p = 16 \Rightarrow p = 4$

- Foco: $(-4, 0)$
- Directriz: $x = 4$
- Abre hacia la **izquierda**

---

**8.1.4** $x^2 = -20y$

$p = 5$

- Foco: $(0, -5)$
- Directriz: $y = 5$
- Abre hacia **abajo**

---

**8.1.5** Foco en $(3, 0)$: $p = 3$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 8.2 (Ecuación de la parábola)</b></summary>

### Soluciones Ejercicio 8.2

**8.2.1** Foco en $(0, 3)$: $p = 3$, eje vertical

Ecuación: $x^2 = 12y$

---

**8.2.2** Directriz $x = -4$: $p = 4$, abre derecha

Ecuación: $y^2 = 16x$

---

**8.2.3** Foco $(2, 0)$ y directriz $x = -2$

Vértice en medio: $(0, 0)$, $p = 2$

Ecuación: $y^2 = 8x$

---

**8.2.4** Pasa por $(4, 8)$, abre arriba

$16 = 4p \times 8 \Rightarrow 4p = 2$

Ecuación: $x^2 = 2y$

---

**8.2.5** Lado recto $= |4p| = 12$

$p = 3$ (o $-3$)

Ecuaciones: $x^2 = 12y$ o $x^2 = -12y$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 8.3 (Parábolas con vértice en (h,k))</b></summary>

### Soluciones Ejercicio 8.3

**8.3.1** $(x - 2)^2 = 8(y - 1)$

$4p = 8 \Rightarrow p = 2$

- Vértice: $(2, 1)$
- Foco: $(2, 3)$
- Directriz: $y = -1$

---

**8.3.2** $(y + 1)^2 = -12(x - 3)$

$p = 3$

- Vértice: $(3, -1)$
- Foco: $(0, -1)$
- Directriz: $x = 6$

---

**8.3.3** Vértice $(1, -2)$, foco $(1, 0)$

$p = 2$, eje vertical

Ecuación: $(x - 1)^2 = 8(y + 2)$

---

**8.3.4** Vértice $(-2, 3)$, pasa por $(0, 7)$

$(0 - (-2))^2 = 4p(7 - 3)$

$4 = 16p \Rightarrow p = \frac{1}{4}$

Ecuación: $(x + 2)^2 = (y - 3)$

---

**8.3.5** $p = -1$

- Vértice: $(-3, 2)$
- Foco: $(-3, 1)$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 8.4 (Completar cuadrados - Parábola)</b></summary>

### Soluciones Ejercicio 8.4

**8.4.1** $(y^2 - 6y + 9) = 8x - 1 + 9$

$(y - 3)^2 = 8(x + 1)$

---

**8.4.2** $(x^2 + 4x + 4) = 12y - 28 + 4$

$(x + 2)^2 = 12(y - 2)$

---

**8.4.3** $(y^2 + 8y + 16) = -4x - 20 + 16$

$(y + 4)^2 = -4(x + 1)$

---

**8.4.4** $(x^2 - 6x + 9) = 16y - 41 + 9$

$(x - 3)^2 = 16(y - 2)$

---

**8.4.5** $(y^2 - 4y + 4) = -8x + 12 + 4$

$(y - 2)^2 = -8(x - 2)$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 8.5 (Forma y = ax² + bx + c)</b></summary>

### Soluciones Ejercicio 8.5

**8.5.1** $y = x^2 - 4x + 3$

$y = (x - 2)^2 - 1$

- Vértice: $(2, -1)$
- $4p = 1 \Rightarrow p = \frac{1}{4}$
- Foco: $(2, -\frac{3}{4})$

---

**8.5.2** $y = -2x^2 + 8x - 5$

$y = -2(x - 2)^2 + 3$

$(x - 2)^2 = -\frac{1}{2}(y - 3)$

- Vértice: $(2, 3)$
- $4p = -\frac{1}{2} \Rightarrow p = -\frac{1}{8}$
- Foco: $(2, \frac{23}{8})$
- Directriz: $y = \frac{25}{8}$

---

**8.5.3** $y = (x + 3)^2 + 2$

$(x + 3)^2 = y - 2$

---

**8.5.4** $y = -\frac{1}{2}(x - 2)^2 + 3$

$(x - 2)^2 = -2(y - 3)$

$p = -\frac{1}{2}$

Foco: $(2, \frac{5}{2})$

---

**8.5.5** $y = 3(x - 2)^2 - 2$

$(x - 2)^2 = \frac{1}{3}(y + 2)$

Vértice: $(2, -2)$

$p = \frac{1}{12}$

Directriz: $y = -2 - \frac{1}{12} = -\frac{25}{12}$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 8.6 (Aplicaciones - Parábola)</b></summary>

### Soluciones Ejercicio 8.6

**8.6.1** Colocar origen en el punto más bajo

Pasa por $(50, 25)$ y $(-50, 25)$

$x^2 = 4py$ donde $(50)^2 = 4p(25)$

$2500 = 100p \Rightarrow p = 25$

Ecuación: $x^2 = 100y$

---

**8.6.2** Radio $= 6$ cm, profundidad $= 4$ cm

Pasa por $(6, 4)$: $36 = 4p \times 4$

$p = \frac{9}{4}$ cm

Foco a $\frac{9}{4}$ cm del vértice

---

**8.6.3** Radio $= 1.5$ m, profundidad $= 0.75$ m

$(1.5)^2 = 4p(0.75)$

$p = 0.75$ m

Receptor en el foco, a $0.75$ m del vértice

---

**8.6.4** Vértice en $(2, 4)$, pasa por $(0, 0)$ y $(4, 0)$

$(x - 2)^2 = 4p(y - 4)$

$(0 - 2)^2 = 4p(0 - 4)$

$4 = -16p \Rightarrow p = -\frac{1}{4}$

Ecuación: $(x - 2)^2 = -(y - 4)$

---

**8.6.5** Para punto $(x, y)$ en $y^2 = 8x$:

Foco: $(2, 0)$, directriz: $x = -2$

$d_F = \sqrt{(x-2)^2 + y^2}$

$d_D = |x + 2|$

Sustituir $y^2 = 8x$ y verificar igualdad

</details>

---

<details>
<summary><b>Ver soluciones - Sección 9.1 (Elementos de la hipérbola)</b></summary>

### Soluciones Ejercicio 9.1

**9.1.1** $\frac{x^2}{9} - \frac{y^2}{16} = 1$

- $a = 3$, $b = 4$
- $c = \sqrt{9+16} = 5$
- Vértices: $(\pm 3, 0)$
- Focos: $(\pm 5, 0)$
- Asíntotas: $y = \pm \frac{4}{3}x$
- Excentricidad: $e = \frac{5}{3}$

---

**9.1.2** $\frac{y^2}{25} - \frac{x^2}{9} = 1$

- $a = 5$, $b = 3$ (eje vertical)
- $c = \sqrt{34}$
- Vértices: $(0, \pm 5)$
- Focos: $(0, \pm \sqrt{34})$
- Asíntotas: $y = \pm \frac{5}{3}x$

---

**9.1.3** $a = 4$, $b = 3$, $c = 5$

- Vértices: $(\pm 4, 0)$
- Focos: $(\pm 5, 0)$
- Asíntotas: $y = \pm \frac{3}{4}x$

---

**9.1.4** $a = 2$, $b = 2\sqrt{3}$, $c = 4$

- Vértices: $(0, \pm 2)$
- Focos: $(0, \pm 4)$
- Asíntotas: $y = \pm \frac{1}{\sqrt{3}}x$

---

**9.1.5** $a = 6$, $b = 8$, $c = 10$

$e = \frac{10}{6} = \frac{5}{3}$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 9.2 (Ecuación de la hipérbola)</b></summary>

### Soluciones Ejercicio 9.2

**9.2.1** $a = 3$, $c = 5$

$b^2 = 25 - 9 = 16$

Ecuación: $\frac{x^2}{9} - \frac{y^2}{16} = 1$

---

**9.2.2** $a = 4$, $c = 5$ (eje vertical)

$b^2 = 25 - 16 = 9$

Ecuación: $\frac{y^2}{16} - \frac{x^2}{9} = 1$

---

**9.2.3** $a = 6$, asíntotas $y = \pm \frac{2}{3}x$

$\frac{b}{a} = \frac{2}{3} \Rightarrow b = 4$

Ecuación: $\frac{x^2}{36} - \frac{y^2}{16} = 1$

---

**9.2.4** $c = 10$, $2a = 12 \Rightarrow a = 6$

$b^2 = 100 - 36 = 64$

Ecuación: $\frac{y^2}{36} - \frac{x^2}{64} = 1$

---

**9.2.5** $a = 3$, $e = \frac{5}{3}$

$c = 5$, $b^2 = 25 - 9 = 16$

Ecuación: $\frac{x^2}{9} - \frac{y^2}{16} = 1$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 9.3 (Hipérbolas con centro en (h,k))</b></summary>

### Soluciones Ejercicio 9.3

**9.3.1** $\frac{(x-2)^2}{9} - \frac{(y-1)^2}{16} = 1$

- Centro: $(2, 1)$
- $a = 3$, $b = 4$, $c = 5$
- Vértices: $(5, 1)$ y $(-1, 1)$
- Focos: $(7, 1)$ y $(-3, 1)$
- Asíntotas: $y - 1 = \pm \frac{4}{3}(x - 2)$

---

**9.3.2** Centro: $(-3, -2)$, $a = 5$, $b = 4$, $c = \sqrt{41}$

- Vértices: $(3, -2)$ y $(-9, -2)$ [Error: debería ser vertical]

Corrección: eje vertical

- Vértices: $(-3, 3)$ y $(-3, -7)$
- Focos: $(-3, -2 \pm \sqrt{41})$

---

**9.3.3** Centro: $(1, -1)$

Distancia a vértices: $a = 3$

Distancia a focos: $c = 5$

$b^2 = 25 - 9 = 16$

Ecuación: $\frac{(x-1)^2}{9} - \frac{(y+1)^2}{16} = 1$

---

**9.3.4** Centro: $(-2, 3)$, vértice $(-2, 7)$, foco $(-2, 8)$

$a = 4$, $c = 5$, $b^2 = 9$

Ecuación: $\frac{(y-3)^2}{16} - \frac{(x+2)^2}{9} = 1$

---

**9.3.5** $\frac{b}{a} = \frac{3}{2}$, centro $(-1, 2)$

Asíntotas: $y - 2 = \pm \frac{3}{2}(x + 1)$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 9.4 (Completar cuadrados - Hipérbola)</b></summary>

### Soluciones Ejercicio 9.4

**9.4.1** $(x^2 - 6x) - 4(y^2 - 4y) = 23$

$(x - 3)^2 - 4(y - 2)^2 = 16$

$\frac{(x-3)^2}{16} - \frac{(y-2)^2}{4} = 1$

---

**9.4.2** $9(y^2 - 2y) - 4(x^2 + 4x) = 43$

$9(y - 1)^2 - 4(x + 2)^2 = 36$

$\frac{(y-1)^2}{4} - \frac{(x+2)^2}{9} = 1$

---

**9.4.3** $4(x^2 - 2x) - 9(y^2 - 4y) = 68$

$4(x - 1)^2 - 9(y - 2)^2 = 36$

$\frac{(x-1)^2}{9} - \frac{(y-2)^2}{4} = 1$

---

**9.4.4** $16(x^2 + 4x) - 9(y^2 - 2y) = 89$

$16(x + 2)^2 - 9(y - 1)^2 = 144$

$\frac{(x+2)^2}{9} - \frac{(y-1)^2}{16} = 1$

---

**9.4.5** $(y^2 - 4y) - 4(x^2 - 6x) = 36$

$(y - 2)^2 - 4(x - 3)^2 = 4$

$\frac{(y-2)^2}{4} - (x-3)^2 = 1$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 9.5 (Aplicaciones - Hipérbola)</b></summary>

### Soluciones Ejercicio 9.5

**9.5.1** Distancia entre estaciones: $200$ km

Diferencia de tiempo: $0.001$ s

Diferencia de distancias: $300 \times 0.001 = 0.3$ km

$2a = 0.3 \Rightarrow a = 0.15$

$c = 100$ (mitad de distancia entre estaciones)

$b^2 = 10000 - 0.0225 \approx 10000$

Ecuación: $\frac{x^2}{0.0225} - \frac{y^2}{10000} = 1$

---

**9.5.2** Base: $20$ m, parte estrecha: $10$ m a $50$ m altura

Configuración de hipérbola vertical...

---

**9.5.3** Para $\frac{x^2}{9} - \frac{y^2}{16} = 1$:

$a = 3$, focos $(\pm 5, 0)$

Para punto $(3, 0)$: $|d_1 - d_2| = |2 - 8| = 6 = 2a$ ✓

---

**9.5.4** Vértice más cercano: $a = 100$, $e = 1.5$

$c = 1.5 \times 100 = 150$

$b^2 = 22500 - 10000 = 12500$

Ecuación: $\frac{x^2}{10000} - \frac{y^2}{12500} = 1$

---

**9.5.5** Asíntotas $y = \pm 2x$: $\frac{b}{a} = 2$ o $\frac{a}{b} = 2$

Pasa por $(2, 3)$: $\frac{4}{a^2} - \frac{9}{b^2} = 1$

Resolver sistema...

</details>

---

## Notas importantes

1. **Distancia:** La fórmula de distancia se deriva del teorema de Pitágoras. Siempre da un valor no negativo.

2. **Punto medio:** Es el promedio aritmético de las coordenadas correspondientes.

3. **Translaciones:** Preservan todas las propiedades geométricas (distancias, ángulos, áreas). Son las transformaciones más simples.

4. **Rotaciones:** También preservan distancias, ángulos y áreas. El sentido positivo es **antihorario**.

5. **Pendiente:**
   - $m > 0$: recta ascendente
   - $m < 0$: recta descendente
   - $m = 0$: recta horizontal
   - Indefinida: recta vertical

6. **Paralelas:** Tienen la misma pendiente ($m_1 = m_2$) o ambas son verticales.

7. **Perpendiculares:** El producto de sus pendientes es $-1$ ($m_1 \cdot m_2 = -1$), excepto cuando una es horizontal y la otra vertical.

8. **Cónicas - Identificación:**
   - **Círculo:** $A = C$ y $B = 0$ en la ecuación general
   - **Elipse:** $B^2 - 4AC < 0$ y $A \neq C$
   - **Parábola:** $B^2 - 4AC = 0$
   - **Hipérbola:** $B^2 - 4AC > 0$

9. **Relaciones importantes:**
   - **Elipse:** $c^2 = a^2 - b^2$ (donde $c < a$)
   - **Hipérbola:** $c^2 = a^2 + b^2$ (donde $c > a$)
   - **Parábola:** distancia del vértice al foco $= p$

10. **Completar cuadrados:** Técnica esencial para convertir ecuaciones generales a forma estándar. Siempre agrupe términos con la misma variable antes de completar cuadrados.

11. **Excentricidad:**
    - **Círculo:** $e = 0$
    - **Elipse:** $0 < e < 1$ (más cercano a 1 = más alargada)
    - **Parábola:** $e = 1$
    - **Hipérbola:** $e > 1$ (mayor valor = ramas más abiertas)

12. **Asíntotas de hipérbola:** Las ramas de la hipérbola se acercan a estas rectas pero nunca las tocan. Pasan siempre por el centro.

13. **Aplicaciones prácticas:**
    - **Círculos:** ruedas, órbitas circulares
    - **Elipses:** órbitas planetarias, arcos arquitectónicos
    - **Parábolas:** trayectorias de proyectiles, antenas, reflectores
    - **Hipérbolas:** navegación (LORAN), torres de enfriamiento

14. **Visualización:** Siempre que sea posible, dibuje un bosquejo de la cónica para verificar la razonabilidad de su respuesta.

---

**Fecha de entrega:** Por definir  
**Consultas:** Disponibles durante horas de oficina

---

*Desarrollado para el curso de Cálculo 1 - 2026*