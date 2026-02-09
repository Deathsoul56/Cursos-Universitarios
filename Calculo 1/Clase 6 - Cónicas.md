# Secciones Cónicas: Geometría Analítica Avanzada

## 1. El plano cartesiano y transformaciones de coordenadas

### 1.1 El plano $\mathbb{R}^2$

**Definición 1.1 (Plano cartesiano):**
El **plano cartesiano** o **plano euclidiano** $\mathbb{R}^2$ es el conjunto de todos los pares ordenados de números reales:
$$\mathbb{R}^2 = \{(x, y) : x, y \in \mathbb{R}\}$$

**Elementos del plano:**
- **Ejes coordenados:** Eje X (horizontal) y eje Y (vertical)
- **Origen:** Punto $O = (0, 0)$ donde se intersectan los ejes
- **Cuadrantes:** Cuatro regiones delimitadas por los ejes

```
    II    |    I
          |
    ------+------
          |
    III   |    IV
```

**Definición 1.2 (Distancia entre dos puntos):**
La distancia entre los puntos $P_1 = (x_1, y_1)$ y $P_2 = (x_2, y_2)$ es:
$$d(P_1, P_2) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$

**Definición 1.3 (Punto medio):**
El punto medio del segmento entre $P_1 = (x_1, y_1)$ y $P_2 = (x_2, y_2)$ es:
$$M = \left(\frac{x_1 + x_2}{2}, \frac{y_1 + y_2}{2}\right)$$

### 1.2 Traslaciones (Translaciones)

**Definición 1.4 (Traslación):**
Una **traslación** es una transformación que desplaza todos los puntos del plano en la misma dirección y distancia.

**Fórmula de traslación:**
Si trasladamos el punto $(x, y)$ por un vector $(h, k)$, obtenemos:
$$\begin{cases}
x' = x + h \\
y' = y + k
\end{cases}$$

O equivalentemente:
$$\begin{cases}
x = x' - h \\
y = y' - k
\end{cases}$$

**Ejemplo 1.1:**
Traslade el punto $P = (3, 2)$ por el vector $(4, -1)$:
$$P' = (3 + 4, 2 + (-1)) = (7, 1)$$

**Aplicación a ecuaciones:**
Si una curva tiene ecuación $f(x, y) = 0$ y la trasladamos por $(h, k)$, la nueva ecuación es:
$$f(x - h, y - k) = 0$$

**Ejemplo 1.2:**
La circunferencia $x^2 + y^2 = 9$ trasladada por $(2, -3)$ se convierte en:
$$(x - 2)^2 + (y + 3)^2 = 9$$

### 1.3 Rotaciones

**Definición 1.5 (Rotación):**
Una **rotación** es una transformación que gira todos los puntos del plano alrededor del origen por un ángulo $\theta$.

**Fórmulas de rotación:**
Para rotar un punto $(x, y)$ por un ángulo $\theta$ (sentido antihorario):
$$\begin{cases}
x' = x\cos(\theta) - y\sin(\theta) \\
y' = x\sin(\theta) + y\cos(\theta)
\end{cases}$$

**Rotación inversa:**
$$\begin{cases}
x = x'\cos(\theta) + y'\sin(\theta) \\
y = -x'\sin(\theta) + y'\cos(\theta)
\end{cases}$$

**Ejemplo 1.3:**
Rote el punto $P = (1, 0)$ por $90°$ (o $\frac{\pi}{2}$ rad):
$$\begin{cases}
x' = 1 \cdot \cos(90°) - 0 \cdot \sin(90°) = 0 \\
y' = 1 \cdot \sin(90°) + 0 \cdot \cos(90°) = 1
\end{cases}$$
Resultado: $P' = (0, 1)$

**Ejemplo 1.4:**
Rote el punto $Q = (2, 2)$ por $45°$:
$$\begin{cases}
x' = 2\cos(45°) - 2\sin(45°) = 2 \cdot \frac{\sqrt{2}}{2} - 2 \cdot \frac{\sqrt{2}}{2} = 0 \\
y' = 2\sin(45°) + 2\cos(45°) = 2 \cdot \frac{\sqrt{2}}{2} + 2 \cdot \frac{\sqrt{2}}{2} = 2\sqrt{2}
\end{cases}$$

### 1.4 Transformaciones combinadas

**Proposición 1.1:**
Las transformaciones se pueden combinar. El orden importa:
- Traslación seguida de rotación ≠ Rotación seguida de traslación (en general)

**Ejemplo 1.5:**
Traslade $(1, 0)$ por $(1, 1)$ y luego rote $90°$:
1. Traslación: $(1, 0) \to (2, 1)$
2. Rotación: $(2, 1) \to (2\cos(90°) - 1\sin(90°), 2\sin(90°) + 1\cos(90°)) = (-1, 2)$

---

## 2. Ecuación general de segundo grado

### 2.1 Forma general

**Definición 2.1 (Ecuación general de segundo grado):**
La **ecuación general de segundo grado** en el plano tiene la forma:
$$Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$$

donde $A$, $B$, $C$, $D$, $E$, $F$ son constantes reales y al menos uno de $A$, $B$, $C$ es distinto de cero.

Esta relación nos dará como resultado un circulo, una elipse, una parábola o una hipérbola, estas cuatro secciones geométricas son llamadas las secciones cónicas pues son el resultado de intersecar un cono con un plan.
El termino cruzado $Bxy$ tiene relación con el ángulo de rotación de la sección cónica, en un principio trabajaremos sin el pero mas adelante lo incorporaremos para ver su comportamiento.

**Observación:** Esta ecuación representa una **sección cónica** (o un caso degenerado).

### 2.2 Clasificación de cónicas por discriminante

**Teorema 2.1 (Clasificación por discriminante):**
La naturaleza de la cónica representada por $Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$ se determina por el **discriminante**:
$$\Delta = B^2 - 4AC$$

**Clasificación:**

1. **$\Delta < 0$ (Elipse):**
   - Si $A = C$ y $B = 0$: **Circunferencia**
   - Si $A \neq C$ o $B \neq 0$: **Elipse**
   - Caso degenerado: punto o conjunto vacío

2. **$\Delta = 0$ (Parábola):**
   - **Parábola**
   - Caso degenerado: dos rectas paralelas o una recta doble

3. **$\Delta > 0$ (Hipérbola):**
   - **Hipérbola**
   - Caso degenerado: dos rectas que se intersectan

**Ejemplo 2.1:**
Clasifique las siguientes ecuaciones:

a) $x^2 + y^2 - 4x + 6y - 3 = 0$
   - $A = 1, B = 0, C = 1$
   - $\Delta = 0^2 - 4(1)(1) = -4 < 0$ y $A = C$, $B = 0$
   - **Circunferencia**

b) $4x^2 + 9y^2 - 16x + 18y - 11 = 0$
   - $A = 4, B = 0, C = 9$
   - $\Delta = 0^2 - 4(4)(9) = -144 < 0$ y $A \neq C$
   - **Elipse**

c) $y^2 - 4x + 6y + 13 = 0$
   - $A = 0, B = 0, C = 1$
   - $\Delta = 0^2 - 4(0)(1) = 0$
   - **Parábola**

d) $x^2 - y^2 - 2x + 4y - 4 = 0$
   - $A = 1, B = 0, C = -1$
   - $\Delta = 0^2 - 4(1)(-1) = 4 > 0$
   - **Hipérbola**

### 2.3 Eliminación del término mixto

**Teorema 2.2 (Rotación para eliminar término mixto):**
El término $Bxy$ en la ecuación $Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$ se puede eliminar mediante una rotación de ángulo $\theta$ donde:
$$\tan(2\theta) = \frac{B}{A - C}$$

Si $A = C$, entonces $\theta = 45°$ (o $\frac{\pi}{4}$).

**Observación:** Después de la rotación, la ecuación toma la forma:
$$A'x'^2 + C'y'^2 + D'x' + E'y' + F' = 0$$

---

## 3. Secciones cónicas: definición geométrica

### 3.1 El cono circular recto

**Definición 3.1 (Cono circular recto):**
Un **cono circular recto** es la superficie generada por una recta (generatriz) que pasa por un punto fijo (vértice) y forma un ángulo constante con un eje fijo.

```
        *  vértice
       /|\
      / | \
     /  |  \
    /   |   \
   /    |    \
  /_____|_____\
       eje
```

**Definición 3.2 (Sección cónica):**
Una **sección cónica** (o **cónica**) es la curva resultante de la intersección de un plano con un cono circular recto doble (dos conos opuestos por el vértice).

### 3.2 Tipos de secciones cónicas

Dependiendo del ángulo del plano de corte:

**1. Circunferencia:**
- Plano perpendicular al eje del cono
```
    \     |     /
     \    |    /
      \   |   /
       \==|==/  ← Circunferencia
        \ | /
         \|/
```

**2. Elipse:**
- Plano oblicuo que corta una hoja del cono
- No paralelo a ninguna generatriz
```
    \     /
     \   /
      \ /
      / \  ← Elipse
     /   \
    /     \
```

**3. Parábola:**
- Plano paralelo a una generatriz del cono
```
    \     /
     \   |
      \  |  ← Parábola
       \ |
        \|
```

**4. Hipérbola:**
- Plano que corta ambas hojas del cono
```
    \     /
     \   /
      \ /
      / \
     /   \
    /     \
```

**Casos degenerados:**
- **Punto:** Plano pasa por el vértice (perpendicular al eje)
- **Recta:** Plano pasa por el vértice (tangente a una generatriz)
- **Dos rectas:** Plano pasa por el vértice (no tangente)

---

## 4. El círculo (circunferencia)

### 4.1 Definición y ecuación

**Definición 4.1 (Circunferencia - Lugar geométrico):**
Una **circunferencia** es el conjunto de todos los puntos del plano que equidistan de un punto fijo llamado **centro**.

$$\text{Circunferencia} = \{P \in \mathbb{R}^2 : d(P, C) = r\}$$

donde $C$ es el centro y $r > 0$ es el **radio**.

**Teorema 4.1 (Ecuación canónica):**
La circunferencia con centro $C = (h, k)$ y radio $r$ tiene ecuación:
$$(x - h)^2 + (y - k)^2 = r^2$$

**Caso particular (centro en el origen):**
$$x^2 + y^2 = r^2$$

**Ejemplo 4.1:**
La circunferencia con centro $(2, -3)$ y radio $5$ tiene ecuación:
$$(x - 2)^2 + (y + 3)^2 = 25$$

### 4.2 Ecuación general

**Proposición 4.1:**
Expandiendo la ecuación canónica, obtenemos la **forma general**:
$$x^2 + y^2 + Dx + Ey + F = 0$$

donde $D = -2h$, $E = -2k$, $F = h^2 + k^2 - r^2$.

**Completación de cuadrados:**
Para convertir de forma general a canónica:
1. Agrupar términos en $x$ y en $y$
2. Completar cuadrados para ambas variables
3. Identificar $(h, k)$ y $r$

**Ejemplo 4.2:**
Encuentre el centro y radio de $x^2 + y^2 - 6x + 4y - 3 = 0$:

$$\begin{align}
x^2 - 6x + y^2 + 4y &= 3 \\
(x^2 - 6x + 9) + (y^2 + 4y + 4) &= 3 + 9 + 4 \\
(x - 3)^2 + (y + 2)^2 &= 16
\end{align}$$

- **Centro:** $(3, -2)$
- **Radio:** $r = \sqrt{16} = 4$

### 4.3 El número $\pi$

**Definición 4.2 (Número $\pi$):**
El número $\pi$ (pi) es la constante definida como la razón entre la **circunferencia** (perímetro) de un círculo y su **diámetro**:
$$\pi = \frac{C}{d} = \frac{C}{2r}$$

donde $C$ es la longitud de la circunferencia y $d = 2r$ es el diámetro.

**Valor aproximado:** $\pi \approx 3.14159265358979...$

**Propiedad:** $\pi$ es un número irracional y trascendente.

### 4.4 Perímetro y área

**Teorema 4.2 (Perímetro):**
El **perímetro** o **longitud de la circunferencia** de radio $r$ es:
$$C = 2\pi r$$

**Teorema 4.3 (Área):**
El **área del círculo** de radio $r$ es:
$$A = \pi r^2$$

**Ejemplo 4.3:**
Para un círculo de radio $5$ cm:
- Perímetro: $C = 2\pi(5) = 10\pi \approx 31.42$ cm
- Área: $A = \pi(5)^2 = 25\pi \approx 78.54$ cm²

### 4.5 Arco de circunferencia

**Definición 4.3 (Arco):**
Un **arco** es una porción de la circunferencia delimitada por dos puntos.

**Teorema 4.4 (Longitud de arco):**
La longitud de un arco que subtiende un ángulo central $\theta$ (en radianes) en una circunferencia de radio $r$ es:
$$s = r\theta$$

**Ejemplo 4.4:**
Un arco con ángulo central de $60° = \frac{\pi}{3}$ rad en una circunferencia de radio $6$ cm:
$$s = 6 \cdot \frac{\pi}{3} = 2\pi \approx 6.28 \text{ cm}$$

**Definición 4.4 (Sector circular):**
Un **sector circular** es la región encerrada por dos radios y el arco entre ellos.

**Área del sector:**
$$A_{\text{sector}} = \frac{1}{2}r^2\theta$$

donde $\theta$ está en radianes.

### 4.6 Propiedades del círculo

**Proposición 4.2 (Propiedades):**

1. **Simetría:** El círculo es simétrico respecto a cualquier diámetro
2. **Radio perpendicular a tangente:** Un radio es perpendicular a la recta tangente en su punto de tangencia
3. **Cuerdas equidistantes:** Cuerdas equidistantes del centro tienen igual longitud
4. **Ángulo inscrito:** Un ángulo inscrito es la mitad del ángulo central que subtiende el mismo arco
5. **Ecuación paramétrica:**
   $$\begin{cases}
   x = h + r\cos(t) \\
   y = k + r\sin(t)
   \end{cases}, \quad t \in [0, 2\pi)$$

**Ejemplo 4.5:**
Para la circunferencia $(x - 1)^2 + (y + 2)^2 = 9$:
- Centro: $(1, -2)$
- Radio: $3$
- Ecuación paramétrica:
  $$x = 1 + 3\cos(t), \quad y = -2 + 3\sin(t)$$

---

## 5. La elipse

### 5.1 Definición y ecuación

**Definición 5.1 (Elipse - Lugar geométrico):**
Una **elipse** es el conjunto de todos los puntos del plano cuya suma de distancias a dos puntos fijos (llamados **focos**) es constante:
$$\text{Elipse} = \{P \in \mathbb{R}^2 : d(P, F_1) + d(P, F_2) = 2a\}$$

donde $F_1$ y $F_2$ son los focos y $2a$ es la constante (longitud del eje mayor).

**Propiedad fundamental:**
$$d(P, F_1) + d(P, F_2) = 2a$$

para todo punto $P$ en la elipse, donde $a$ es el **semieje mayor**.

### 5.2 Elementos de la elipse

**Componentes principales:**

1. **Focos:** $F_1$ y $F_2$, separados por distancia $2c$
2. **Centro:** Punto medio entre los focos
3. **Eje mayor:** Segmento de longitud $2a$ que pasa por los focos
4. **Eje menor:** Segmento perpendicular al eje mayor de longitud $2b$
5. **Vértices mayores:** Puntos de intersección con el eje mayor
6. **Vértices menores:** Puntos de intersección con el eje menor

**Relación fundamental:**
$$a^2 = b^2 + c^2$$

donde:
- $a$ = semieje mayor
- $b$ = semieje menor
- $c$ = distancia del centro a cada foco

```
        Vértice menor
             •
             |
   F₁ •------|------• F₂
      c  •   |  •   c
         |   |   |
    -----•---•---•----- Eje mayor
         |   |   |
             |
             •
        Vértice menor
    |----a----|
        |--b--|
```

### 5.3 Ecuación canónica

**Teorema 5.1 (Elipse horizontal con centro en el origen):**
Si el eje mayor es horizontal:
$$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1, \quad \text{con } a > b > 0$$

- **Focos:** $F_1 = (-c, 0)$ y $F_2 = (c, 0)$ donde $c = \sqrt{a^2 - b^2}$
- **Vértices mayores:** $(\pm a, 0)$
- **Vértices menores:** $(0, \pm b)$

**Teorema 5.2 (Elipse vertical con centro en el origen):**
Si el eje mayor es vertical:
$$\frac{x^2}{b^2} + \frac{y^2}{a^2} = 1, \quad \text{con } a > b > 0$$

- **Focos:** $F_1 = (0, -c)$ y $F_2 = (0, c)$ donde $c = \sqrt{a^2 - b^2}$
- **Vértices mayores:** $(0, \pm a)$
- **Vértices menores:** $(\pm b, 0)$

**Ejemplo 5.1:**
La elipse $\frac{x^2}{25} + \frac{y^2}{9} = 1$:

- $a^2 = 25 \Rightarrow a = 5$ (eje mayor horizontal)
- $b^2 = 9 \Rightarrow b = 3$
- $c = \sqrt{25 - 9} = \sqrt{16} = 4$
- **Focos:** $(\pm 4, 0)$
- **Vértices mayores:** $(\pm 5, 0)$
- **Vértices menores:** $(0, \pm 3)$

### 5.4 Ecuación con centro desplazado

**Teorema 5.3 (Elipse con centro $(h, k)$):**

**Eje mayor horizontal:**
$$\frac{(x - h)^2}{a^2} + \frac{(y - k)^2}{b^2} = 1$$

- **Centro:** $(h, k)$
- **Focos:** $(h \pm c, k)$

**Eje mayor vertical:**
$$\frac{(x - h)^2}{b^2} + \frac{(y - k)^2}{a^2} = 1$$

- **Centro:** $(h, k)$
- **Focos:** $(h, k \pm c)$

**Ejemplo 5.2:**
La elipse $\frac{(x - 2)^2}{16} + \frac{(y + 1)^2}{25} = 1$:

- **Centro:** $(2, -1)$
- $a^2 = 25 \Rightarrow a = 5$ (eje mayor vertical)
- $b^2 = 16 \Rightarrow b = 4$
- $c = \sqrt{25 - 16} = 3$
- **Focos:** $(2, -1 \pm 3) = (2, 2)$ y $(2, -4)$

### 5.5 Ecuación general

**Forma general de la elipse:**
$$Ax^2 + Cy^2 + Dx + Ey + F = 0$$

donde $A$ y $C$ tienen el mismo signo y $A \neq C$.

**Proceso de completación de cuadrados:**

**Ejemplo 5.3:**
Lleve $9x^2 + 4y^2 - 36x + 8y + 4 = 0$ a forma canónica:

$$\begin{align}
9x^2 - 36x + 4y^2 + 8y &= -4 \\
9(x^2 - 4x) + 4(y^2 + 2y) &= -4 \\
9(x^2 - 4x + 4) + 4(y^2 + 2y + 1) &= -4 + 36 + 4 \\
9(x - 2)^2 + 4(y + 1)^2 &= 36 \\
\frac{(x - 2)^2}{4} + \frac{(y + 1)^2}{9} &= 1
\end{align}$$

- **Centro:** $(2, -1)$
- $a = 3$, $b = 2$, eje mayor vertical

### 5.6 Excentricidad

**Definición 5.2 (Excentricidad):**
La **excentricidad** de una elipse es:
$$e = \frac{c}{a}$$

**Propiedades:**
- $0 < e < 1$ para toda elipse
- Si $e \to 0$: la elipse se aproxima a un círculo
- Si $e \to 1$: la elipse se alarga

**Ejemplo 5.4:**
Para $\frac{x^2}{25} + \frac{y^2}{9} = 1$:
$$e = \frac{4}{5} = 0.8$$

### 5.7 Propiedades de la elipse

**Proposición 5.1 (Propiedades):**

1. **Simetría:** Respecto a ambos ejes (si está centrada en el origen)
2. **Propiedad reflectiva:** Un rayo que sale de un foco se refleja hacia el otro foco
3. **Perímetro aproximado (fórmula de Ramanujan):**
   $$P \approx \pi\left[3(a + b) - \sqrt{(3a + b)(a + 3b)}\right]$$
4. **Área:**
   $$A = \pi ab$$
5. **Ecuación paramétrica:**
   $$\begin{cases}
   x = h + a\cos(t) \\
   y = k + b\sin(t)
   \end{cases}, \quad t \in [0, 2\pi)$$

**Ejemplo 5.5:**
Área de la elipse $\frac{x^2}{16} + \frac{y^2}{9} = 1$:
$$A = \pi(4)(3) = 12\pi \approx 37.70 \text{ unidades}^2$$

---

## 6. La parábola

### 6.1 Definición y ecuación

**Definición 6.1 (Parábola - Lugar geométrico):**
Una **parábola** es el conjunto de todos los puntos del plano que equidistan de un punto fijo (llamado **foco**) y una recta fija (llamada **directriz**):
$$\text{Parábola} = \{P \in \mathbb{R}^2 : d(P, F) = d(P, \ell)\}$$

donde $F$ es el foco y $\ell$ es la directriz.

**Propiedad fundamental:**
$$d(P, \text{foco}) = d(P, \text{directriz})$$

### 6.2 Elementos de la parábola

**Componentes principales:**

1. **Foco ($F$):** Punto fijo
2. **Directriz ($\ell$):** Recta fija
3. **Vértice ($V$):** Punto medio entre el foco y la directriz
4. **Eje de simetría:** Recta perpendicular a la directriz que pasa por el foco
5. **Parámetro ($p$):** Distancia del vértice al foco (y del vértice a la directriz)

```
        Directriz
    -----|-----
          |
          •  P (punto en parábola)
         /|
        / |
       /  |
      •---|---
      F   V
    Foco  Vértice
```

### 6.3 Ecuación canónica

**Teorema 6.1 (Parábola vertical con vértice en el origen):**

**Abre hacia arriba:**
$$x^2 = 4py, \quad p > 0$$
- **Foco:** $(0, p)$
- **Directriz:** $y = -p$
- **Vértice:** $(0, 0)$

**Abre hacia abajo:**
$$x^2 = -4py, \quad p > 0$$
- **Foco:** $(0, -p)$
- **Directriz:** $y = p$
- **Vértice:** $(0, 0)$

**Teorema 6.2 (Parábola horizontal con vértice en el origen):**

**Abre hacia la derecha:**
$$y^2 = 4px, \quad p > 0$$
- **Foco:** $(p, 0)$
- **Directriz:** $x = -p$
- **Vértice:** $(0, 0)$

**Abre hacia la izquierda:**
$$y^2 = -4px, \quad p > 0$$
- **Foco:** $(-p, 0)$
- **Directriz:** $x = p$
- **Vértice:** $(0, 0)$

**Ejemplo 6.1:**
La parábola $x^2 = 12y$:

- Forma: $x^2 = 4py$ con $4p = 12 \Rightarrow p = 3$
- **Vértice:** $(0, 0)$
- **Foco:** $(0, 3)$
- **Directriz:** $y = -3$
- Abre hacia arriba

### 6.4 Ecuación con vértice desplazado

**Teorema 6.3 (Parábola con vértice $(h, k)$):**

**Vertical (abre arriba/abajo):**
$$(x - h)^2 = 4p(y - k)$$
- **Vértice:** $(h, k)$
- **Foco:** $(h, k + p)$ si $p > 0$ (arriba); $(h, k + p)$ si $p < 0$ (abajo)
- **Directriz:** $y = k - p$

**Horizontal (abre derecha/izquierda):**
$$(y - k)^2 = 4p(x - h)$$
- **Vértice:** $(h, k)$
- **Foco:** $(h + p, k)$ si $p > 0$ (derecha); $(h + p, k)$ si $p < 0$ (izquierda)
- **Directriz:** $x = h - p$

**Ejemplo 6.2:**
La parábola $(x - 3)^2 = -8(y + 2)$:

- **Vértice:** $(3, -2)$
- $4p = -8 \Rightarrow p = -2$ (abre hacia abajo)
- **Foco:** $(3, -2 + (-2)) = (3, -4)$
- **Directriz:** $y = -2 - (-2) = 0$

### 6.5 Forma estándar (cuadrática)

**Forma cuadrática de la parábola vertical:**
$$y = a(x - h)^2 + k$$

donde $(h, k)$ es el vértice.

**Relación con forma canónica:**
$$a = \frac{1}{4p}$$

- Si $a > 0$: abre hacia arriba
- Si $a < 0$: abre hacia abajo

**Ejemplo 6.3:**
La parábola $y = 2(x - 1)^2 + 3$:

- **Vértice:** $(1, 3)$
- $a = 2 \Rightarrow p = \frac{1}{4(2)} = \frac{1}{8}$
- **Foco:** $(1, 3 + \frac{1}{8}) = (1, \frac{25}{8})$
- Abre hacia arriba

### 6.6 Ecuación general

**Parábola vertical:**
$$x^2 + Dx + Ey + F = 0$$

**Parábola horizontal:**
$$y^2 + Dx + Ey + F = 0$$

**Completación de cuadrados:**

**Ejemplo 6.4:**
Lleve $x^2 - 4x - 8y + 12 = 0$ a forma estándar:

$$\begin{align}
x^2 - 4x &= 8y - 12 \\
x^2 - 4x + 4 &= 8y - 12 + 4 \\
(x - 2)^2 &= 8y - 8 \\
(x - 2)^2 &= 8(y - 1)
\end{align}$$

- **Vértice:** $(2, 1)$
- $4p = 8 \Rightarrow p = 2$
- **Foco:** $(2, 3)$

### 6.7 Propiedades de la parábola

**Proposición 6.1 (Propiedades):**

1. **Simetría:** Respecto al eje que pasa por el foco y es perpendicular a la directriz
2. **Propiedad reflectiva:** Los rayos paralelos al eje se reflejan hacia el foco (principio de antenas parabólicas y telescopios)
3. **Lado recto (latus rectum):** Cuerda perpendicular al eje que pasa por el foco, de longitud $|4p|$
4. **Ecuación paramétrica (vertical):**
   $$\begin{cases}
   x = h + t \\
   y = k + \frac{t^2}{4p}
   \end{cases}$$
5. **Ecuación paramétrica alternativa:**
   $$\begin{cases}
   x = h + 2pt \\
   y = k + pt^2
   \end{cases}$$

**Ejemplo 6.5:**
Para $x^2 = 8y$ ($p = 2$):
- **Lado recto:** longitud $= 4(2) = 8$
- Puntos del lado recto: $(-4, 2)$ y $(4, 2)$

---

## 7. La hipérbola

### 7.1 Definición y ecuación

**Definición 7.1 (Hipérbola - Lugar geométrico):**
Una **hipérbola** es el conjunto de todos los puntos del plano cuya **diferencia de distancias** a dos puntos fijos (llamados **focos**) es constante:
$$\text{Hipérbola} = \{P \in \mathbb{R}^2 : |d(P, F_1) - d(P, F_2)| = 2a\}$$

donde $F_1$ y $F_2$ son los focos y $2a$ es la constante.

**Propiedad fundamental:**
$$|d(P, F_1) - d(P, F_2)| = 2a$$

### 7.2 Elementos de la hipérbola

**Componentes principales:**

1. **Focos:** $F_1$ y $F_2$, separados por distancia $2c$
2. **Centro:** Punto medio entre los focos
3. **Eje transverso (real):** Segmento de longitud $2a$ que une los vértices
4. **Eje conjugado (imaginario):** Segmento perpendicular de longitud $2b$
5. **Vértices:** Puntos de intersección con el eje transverso
6. **Asíntotas:** Rectas que la hipérbola se aproxima en el infinito

**Relación fundamental:**
$$c^2 = a^2 + b^2$$

donde:
- $a$ = semi-eje transverso (distancia del centro al vértice)
- $b$ = semi-eje conjugado
- $c$ = distancia del centro a cada foco

**Observación:** En la hipérbola $c > a$, a diferencia de la elipse donde $c < a$.

```
        Asíntota
           /|
          / |
    F₁•  /  |  •F₂
        /   |
  -----V----C----V----- Eje transverso
           \|
            |\
            | \
               Asíntota
```

### 7.3 Ecuación canónica

**Teorema 7.1 (Hipérbola horizontal con centro en el origen):**
$$\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$$

- **Eje transverso:** horizontal
- **Focos:** $F_1 = (-c, 0)$ y $F_2 = (c, 0)$ donde $c = \sqrt{a^2 + b^2}$
- **Vértices:** $(\pm a, 0)$
- **Asíntotas:** $y = \pm \frac{b}{a}x$

**Teorema 7.2 (Hipérbola vertical con centro en el origen):**
$$\frac{y^2}{a^2} - \frac{x^2}{b^2} = 1$$

- **Eje transverso:** vertical
- **Focos:** $F_1 = (0, -c)$ y $F_2 = (0, c)$ donde $c = \sqrt{a^2 + b^2}$
- **Vértices:** $(0, \pm a)$
- **Asíntotas:** $y = \pm \frac{a}{b}x$

**Ejemplo 7.1:**
La hipérbola $\frac{x^2}{9} - \frac{y^2}{16} = 1$:

- $a^2 = 9 \Rightarrow a = 3$ (eje transverso horizontal)
- $b^2 = 16 \Rightarrow b = 4$
- $c = \sqrt{9 + 16} = 5$
- **Focos:** $(\pm 5, 0)$
- **Vértices:** $(\pm 3, 0)$
- **Asíntotas:** $y = \pm \frac{4}{3}x$

### 7.4 Ecuación con centro desplazado

**Teorema 7.3 (Hipérbola con centro $(h, k)$):**

**Eje transverso horizontal:**
$$\frac{(x - h)^2}{a^2} - \frac{(y - k)^2}{b^2} = 1$$

- **Centro:** $(h, k)$
- **Focos:** $(h \pm c, k)$
- **Vértices:** $(h \pm a, k)$
- **Asíntotas:** $y - k = \pm \frac{b}{a}(x - h)$

**Eje transverso vertical:**
$$\frac{(y - k)^2}{a^2} - \frac{(x - h)^2}{b^2} = 1$$

- **Centro:** $(h, k)$
- **Focos:** $(h, k \pm c)$
- **Vértices:** $(h, k \pm a)$
- **Asíntotas:** $y - k = \pm \frac{a}{b}(x - h)$

**Ejemplo 7.2:**
La hipérbola $\frac{(y + 1)^2}{4} - \frac{(x - 2)^2}{9} = 1$:

- **Centro:** $(2, -1)$
- $a^2 = 4 \Rightarrow a = 2$ (eje transverso vertical)
- $b^2 = 9 \Rightarrow b = 3$
- $c = \sqrt{4 + 9} = \sqrt{13}$
- **Focos:** $(2, -1 \pm \sqrt{13})$
- **Vértices:** $(2, -1 \pm 2) = (2, 1)$ y $(2, -3)$
- **Asíntotas:** $y + 1 = \pm \frac{2}{3}(x - 2)$

### 7.5 Ecuación general

**Forma general de la hipérbola:**
$$Ax^2 - Cy^2 + Dx + Ey + F = 0$$

donde $A$ y $C$ tienen **signos opuestos** (es la diferencia clave con la elipse).

**Ejemplo 7.3:**
Lleve $9x^2 - 4y^2 - 18x - 16y - 43 = 0$ a forma canónica:

$$\begin{align}
9x^2 - 18x - 4y^2 - 16y &= 43 \\
9(x^2 - 2x) - 4(y^2 + 4y) &= 43 \\
9(x^2 - 2x + 1) - 4(y^2 + 4y + 4) &= 43 + 9 - 16 \\
9(x - 1)^2 - 4(y + 2)^2 &= 36 \\
\frac{(x - 1)^2}{4} - \frac{(y + 2)^2}{9} &= 1
\end{align}$$

- **Centro:** $(1, -2)$
- $a = 2$, $b = 3$, eje transverso horizontal

### 7.6 Excentricidad

**Definición 7.2 (Excentricidad):**
La **excentricidad** de una hipérbola es:
$$e = \frac{c}{a}$$

**Propiedades:**
- $e > 1$ para toda hipérbola
- Cuanto mayor es $e$, más "abierta" es la hipérbola

**Ejemplo 7.4:**
Para $\frac{x^2}{9} - \frac{y^2}{16} = 1$:
$$e = \frac{5}{3} \approx 1.67$$

### 7.7 Propiedades de la hipérbola

**Proposición 7.1 (Propiedades):**

1. **Simetría:** Respecto a ambos ejes (si está centrada en el origen)
2. **Dos ramas separadas:** La hipérbola tiene dos componentes conexas
3. **Asíntotas:** Las ramas se aproximan a las asíntotas en el infinito
4. **Propiedad reflectiva:** Un rayo dirigido a un foco se refleja hacia el otro foco
5. **Rectángulo auxiliar:** Rectángulo de lados $2a$ y $2b$ cuyas diagonales son las asíntotas
6. **Ecuación paramétrica (horizontal):**
   $$\begin{cases}
   x = h + a\sec(t) \\
   y = k + b\tan(t)
   \end{cases}$$
   o usando funciones hiperbólicas:
   $$\begin{cases}
   x = h + a\cosh(t) \\
   y = k + b\sinh(t)
   \end{cases}$$

**Ejemplo 7.5:**
Para $\frac{x^2}{4} - \frac{y^2}{9} = 1$:
- Rectángulo auxiliar: vértices en $(\pm 2, \pm 3)$
- Asíntotas pasan por las diagonales: $y = \pm \frac{3}{2}x$

---

## 8. Cónicas rotadas

### 8.1 Ecuación general con término mixto

**Recordatorio:**
La ecuación general de segundo grado con **término mixto** $Bxy$ es:
$$Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$$

El término $Bxy$ indica que la cónica está **rotada** respecto a los ejes coordenados.

### 8.2 Eliminación del término mixto por rotación

**Teorema 8.1 (Ángulo de rotación):**
Para eliminar el término $Bxy$, rotamos los ejes por un ángulo $\theta$ dado por:
$$\tan(2\theta) = \frac{B}{A - C}$$

**Casos especiales:**
- Si $A = C$: $\theta = 45°$ (o $\frac{\pi}{4}$)
- Si $B = 0$: no hay rotación necesaria

**Fórmulas de transformación:**
$$\begin{cases}
x = x'\cos(\theta) - y'\sin(\theta) \\
y = x'\sin(\theta) + y'\cos(\theta)
\end{cases}$$

Después de sustituir, la ecuación en las nuevas coordenadas $(x', y')$ no tendrá término mixto:
$$A'x'^2 + C'y'^2 + D'x' + E'y' + F' = 0$$

**Ejemplo 8.1:**
Elimine el término mixto de $x^2 + 2xy + y^2 - 8 = 0$:

- $A = 1, B = 2, C = 1$
- $\tan(2\theta) = \frac{2}{1 - 1} = \frac{2}{0}$ → indefinido → $2\theta = 90°$ → $\theta = 45°$

Usando $\cos(45°) = \sin(45°) = \frac{\sqrt{2}}{2}$:
$$\begin{cases}
x = \frac{\sqrt{2}}{2}(x' - y') \\
y = \frac{\sqrt{2}}{2}(x' + y')
\end{cases}$$

Sustituyendo:
$$\left[\frac{\sqrt{2}}{2}(x' - y')\right]^2 + 2\left[\frac{\sqrt{2}}{2}(x' - y')\right]\left[\frac{\sqrt{2}}{2}(x' + y')\right] + \left[\frac{\sqrt{2}}{2}(x' + y')\right]^2 = 8$$

Simplificando:
$$\frac{1}{2}(x' - y')^2 + (x'^2 - y'^2) + \frac{1}{2}(x' + y')^2 = 8$$
$$\frac{1}{2}(x'^2 - 2x'y' + y'^2) + x'^2 - y'^2 + \frac{1}{2}(x'^2 + 2x'y' + y'^2) = 8$$
$$\frac{1}{2}x'^2 - x'y' + \frac{1}{2}y'^2 + x'^2 - y'^2 + \frac{1}{2}x'^2 + x'y' + \frac{1}{2}y'^2 = 8$$
$$2x'^2 = 8$$
$$x'^2 = 4$$

Esta es una **parábola degenerada** (dos rectas paralelas): $x' = \pm 2$

### 8.3 Identificación de cónicas rotadas

**Teorema 8.2 (Invariante discriminante):**
El discriminante $\Delta = B^2 - 4AC$ es **invariante** bajo rotaciones y determina el tipo de cónica:

- **$\Delta < 0$:** Elipse (o círculo)
- **$\Delta = 0$:** Parábola
- **$\Delta > 0$:** Hipérbola

**Ejemplo 8.2:**
Clasifique $3x^2 + 10xy + 3y^2 - 2x - 14y - 13 = 0$:

- $A = 3, B = 10, C = 3$
- $\Delta = 10^2 - 4(3)(3) = 100 - 36 = 64 > 0$
- **Hipérbola rotada**

**Ejemplo 8.3:**
Para eliminar el término mixto, calculamos $\theta$:
$$\tan(2\theta) = \frac{10}{3 - 3} = \frac{10}{0}$$ → indefinido → $\theta = 45°$

### 8.4 Procedimiento completo

**Pasos para analizar una cónica rotada:**

1. **Identificar el tipo** usando $\Delta = B^2 - 4AC$
2. **Calcular el ángulo de rotación:** $\tan(2\theta) = \frac{B}{A - C}$
3. **Aplicar la rotación:**
   $$\begin{cases}
   x = x'\cos(\theta) - y'\sin(\theta) \\
   y = x'\sin(\theta) + y'\cos(\theta)
   \end{cases}$$
4. **Simplificar** la ecuación resultante
5. **Completar cuadrados** si es necesario
6. **Identificar elementos** (centro, focos, vértices, etc.)

**Ejemplo 8.4:**
Analice $5x^2 - 6xy + 5y^2 - 8 = 0$:

**Paso 1:** Clasificación
- $\Delta = (-6)^2 - 4(5)(5) = 36 - 100 = -64 < 0$
- **Elipse rotada**

**Paso 2:** Ángulo de rotación
$$\tan(2\theta) = \frac{-6}{5 - 5} = \frac{-6}{0}$$ → $\theta = 45°$

**Paso 3 y 4:** Después de rotar y simplificar (cálculos omitidos):
$$2x'^2 + 8y'^2 = 8$$
$$\frac{x'^2}{4} + \frac{y'^2}{1} = 1$$

**Resultado:** Elipse con ejes $a = 2$, $b = 1$ en el sistema rotado $45°$

---

## 9. Aplicaciones de las cónicas

### 9.1 Aplicaciones del círculo

1. **Ruedas y engranajes:** Transmisión de movimiento
2. **Ondas:** Propagación circular de ondas en agua
3. **Alcance de señales:** Radio de cobertura de antenas
4. **Astronomía:** Órbitas circulares aproximadas

### 9.2 Aplicaciones de la elipse

1. **Órbitas planetarias:** Las órbitas de los planetas son elipses con el Sol en uno de los focos (Primera Ley de Kepler)
2. **Acústica:** Salas elípticas donde el sonido de un foco se concentra en el otro
3. **Litotripsia:** Destrucción de cálculos renales usando ondas de choque enfocadas
4. **Óptica:** Espejos elípticos en telescopios

### 9.3 Aplicaciones de la parábola

1. **Antenas parabólicas:** Concentran señales en el foco
2. **Faros y reflectores:** Producen haz paralelo desde fuente en el foco
3. **Telescopios reflectores:** Espejos parabólicos
4. **Trayectorias balísticas:** Proyectiles bajo gravedad (aproximación)
5. **Puentes:** Cables de puentes colgantes forman catenarias (similar a parábolas)

### 9.4 Aplicaciones de la hipérbola

1. **Navegación:** Sistemas LORAN usan diferencias de distancias (hipérbolas)
2. **Óptica:** Lentes hiperbólicas
3. **Astronomía:** Trayectorias de cometas no periódicos
4. **Física nuclear:** Trayectorias de partículas con repulsión coulombiana
5. **Arquitectura:** Torres de refrigeración de centrales nucleares

---

## 10. Intersección de rectas con cónicas

### 10.1 Método general

Para encontrar la intersección de una recta $y = mx + b$ con una cónica:

1. Sustituir la ecuación de la recta en la ecuación de la cónica
2. Obtener una ecuación cuadrática en $x$ (o $y$)
3. Resolver usando la fórmula cuadrática
4. Analizar el discriminante:
   - $\Delta > 0$: dos puntos de intersección (recta secante)
   - $\Delta = 0$: un punto de intersección (recta tangente)
   - $\Delta < 0$: ningún punto de intersección (recta exterior)

**Ejemplo 10.1:**
Encuentre la intersección de $y = x + 1$ con $x^2 + y^2 = 5$:

$$\begin{align}
x^2 + (x + 1)^2 &= 5 \\
x^2 + x^2 + 2x + 1 &= 5 \\
2x^2 + 2x - 4 &= 0 \\
x^2 + x - 2 &= 0 \\
(x + 2)(x - 1) &= 0
\end{align}$$

- $x = -2 \Rightarrow y = -1$: punto $(-2, -1)$
- $x = 1 \Rightarrow y = 2$: punto $(1, 2)$

**Dos puntos de intersección** (recta secante)

### 10.2 Recta tangente a una cónica

**Definición 10.1:**
Una **recta tangente** a una cónica en un punto $P$ es la recta que toca la cónica exactamente en ese punto.

**Condición:** El discriminante de la ecuación de intersección debe ser cero.

**Ejemplo 10.2:**
Encuentre la ecuación de la tangente a $x^2 + y^2 = 25$ en el punto $(3, 4)$:

**Método 1 (Derivación implícita):**
$$2x + 2y\frac{dy}{dx} = 0 \Rightarrow \frac{dy}{dx} = -\frac{x}{y}$$

En $(3, 4)$: $m = -\frac{3}{4}$

Ecuación: $y - 4 = -\frac{3}{4}(x - 3)$
$$4y - 16 = -3x + 9$$
$$3x + 4y = 25$$

**Método 2 (Fórmula directa para círculos):**
Para $(x - h)^2 + (y - k)^2 = r^2$, la tangente en $(x_0, y_0)$ es:
$$(x_0 - h)(x - h) + (y_0 - k)(y - k) = r^2$$

Para nuestro caso:
$$3x + 4y = 25$$

---

## 11. Resumen comparativo de cónicas

| Cónica | Definición (lugar geométrico) | Ecuación canónica | Excentricidad |
|--------|-------------------------------|-------------------|---------------|
| **Círculo** | Puntos a distancia constante de un centro | $x^2 + y^2 = r^2$ | $e = 0$ |
| **Elipse** | Suma de distancias a dos focos constante | $\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1$ | $0 < e < 1$ |
| **Parábola** | Distancia a foco = distancia a directriz | $x^2 = 4py$ | $e = 1$ |
| **Hipérbola** | Diferencia de distancias a dos focos constante | $\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1$ | $e > 1$ |

**Discriminante $\Delta = B^2 - 4AC$:**
- Elipse/Círculo: $\Delta < 0$
- Parábola: $\Delta = 0$
- Hipérbola: $\Delta > 0$

**Relaciones características:**
- **Elipse:** $c^2 = a^2 - b^2$ donde $c < a$
- **Hipérbola:** $c^2 = a^2 + b^2$ donde $c > a$
- **Parábola:** $p$ = distancia foco-vértice = vértice-directriz

---

## 12. Ejercicios propuestos

### 12.1 Transformaciones

1. Traslade el punto $(5, -2)$ por el vector $(-3, 4)$
2. Rote el punto $(4, 0)$ por $60°$ alrededor del origen
3. Encuentre la ecuación de $y = x^2$ después de trasladar por $(2, -3)$

### 12.2 Circunferencias

4. Encuentre el centro y radio de $x^2 + y^2 - 8x + 6y + 9 = 0$
5. Escriba la ecuación de la circunferencia con centro $(-1, 4)$ y radio $7$
6. Determine si el punto $(3, 5)$ está dentro, sobre o fuera de la circunferencia $x^2 + y^2 = 25$

### 12.3 Elipses

7. Para $\frac{x^2}{36} + \frac{y^2}{20} = 1$, encuentre: centro, vértices, focos y excentricidad
8. Encuentre la ecuación de la elipse con focos $(\pm 3, 0)$ y vértices $(\pm 5, 0)$
9. Lleve $25x^2 + 9y^2 - 100x + 18y - 116 = 0$ a forma canónica

### 12.4 Parábolas

10. Para $x^2 = -16y$, encuentre: vértice, foco, directriz y dirección de apertura
11. Encuentre la ecuación de la parábola con vértice $(0, 0)$, foco $(0, 3)$
12. Lleve $y^2 + 8x - 6y + 25 = 0$ a forma canónica

### 12.5 Hipérbolas

13. Para $\frac{y^2}{16} - \frac{x^2}{9} = 1$, encuentre: centro, vértices, focos, asíntotas y excentricidad
14. Encuentre la ecuación de la hipérbola con vértices $(0, \pm 4)$ y focos $(0, \pm 5)$
15. Lleve $9x^2 - 16y^2 + 36x + 32y - 124 = 0$ a forma canónica

### 12.6 Cónicas rotadas

16. Clasifique usando el discriminante: $x^2 + 4xy + 4y^2 - 6x - 12y + 5 = 0$
17. Encuentre el ángulo de rotación para eliminar el término mixto en $xy = 4$
18. Para $x^2 + 2xy + y^2 - 4x + 4y = 0$, elimine el término mixto

### 12.7 Aplicaciones

19. Una órbita elíptica tiene semieje mayor $a = 150$ millones de km y excentricidad $e = 0.0167$. Encuentre la distancia del Sol (en un foco) al perihelio y afelio
20. Una antena parabólica tiene 4 m de ancho y 1 m de profundidad. ¿A qué distancia del vértice debe colocarse el receptor?
21. Dos estaciones están a 600 km de distancia. Un barco recibe señales con diferencia de tiempo tal que está 200 km más cerca de una que de otra. ¿Qué tipo de curva describe su posición?

### 12.8 Intersecciones y tangentes

22. Encuentre los puntos de intersección de $y = 2x - 1$ con $x^2 + y^2 = 10$
23. Determine si la recta $y = x + 5$ es secante, tangente o exterior a $(x - 1)^2 + (y + 2)^2 = 9$
24. Encuentre la ecuación de la tangente a $\frac{x^2}{25} + \frac{y^2}{9} = 1$ en el punto $(4, \frac{9}{5})$
25. Encuentre las tangentes a $x^2 = 8y$ que pasan por el punto $(0, -2)$

---

**Fin de la Clase 6**
