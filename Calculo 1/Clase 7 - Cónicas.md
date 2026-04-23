# Secciones Cónicas: Geometría Analítica Avanzada

## 1. El plano cartesiano y transformaciones de coordenadas

Primero vamos a recordar algunos conceptos básicos.

### 1.1 El plano $\mathbb{R}^2$

**Definición 1.1 (Plano cartesiano):**
El **plano cartesiano** o **plano euclidiano** $\mathbb{R}^2$ es el conjunto de todos los pares ordenados de números reales:
$$\mathbb{R}^2 = \{(x, y) : x, y \in \mathbb{R}\}$$

**Elementos del plano:**
- **Ejes coordenados:** Eje X (horizontal) y eje Y (vertical)
- **Origen:** Punto $O = (0, 0)$ donde se intersectan los ejes
- **Cuadrantes:** Cuatro regiones delimitadas por los ejes

![[cuadrantes.png]]

**Definición 1.2 (Distancia entre dos puntos):**
La distancia entre los puntos $P_1 = (x_1, y_1)$ y $P_2 = (x_2, y_2)$ es:
$$d(P_1, P_2) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$

**Definición 1.3 (Punto medio):**
El punto medio del segmento entre $P_1 = (x_1, y_1)$ y $P_2 = (x_2, y_2)$ es:
$$M = \left(\frac{x_1 + x_2}{2}, \frac{y_1 + y_2}{2}\right)$$

Ahora vamos a estudiar las transformaciones que podemos realizar en el plano.
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
Una **rotación** es una transformación geométrica isométrica (que conserva las distancias originales de la forma) que hace girar a todos los puntos del plano alrededor de un punto fijo establecido, llamado **centro de rotación**, por medio de un ángulo de amplitud constante $\theta$.

> **Caso particular (centro en el origen):** En el flujo clásico de la geometría analítica y el estudio para estandarizar formas, la convención principal es analizar las rotaciones anclando el centro de giro exactamente sobre el origen de coordenadas $(0,0)$.

**Teorema 1.1 (Fórmulas de rotación):**
Para rotar un punto $(x, y)$ respecto al origen por un ángulo $\theta$ (en sentido antihorario), se utilizan las ecuaciones:
$$\begin{cases}
x' = x\cos(\theta) - y\sin(\theta) \\
y' = x\sin(\theta) + y\cos(\theta)
\end{cases}$$

**Demostración:**
1. Consideremos un punto $P(x, y)$ representado mediante coordenadas polares. Sea $r$ su distancia al origen y $\alpha$ el ángulo inicial que forma con el semieje positivo de las abscisas (eje $X$). Sus coordenadas se expresan como:
$$x = r\cos(\alpha), \quad y = r\sin(\alpha)$$   ![[punto_polar.png]]
2. Al rotar el punto $P$ en torno al origen un ángulo $\theta$ en sentido antihorario, obtenemos el nuevo punto $P'(x', y')$. La distancia al centro $r$ se mantiene inalterada, pero su nuevo ángulo respecto al eje $X$ pasa a ser la suma $(\alpha + \theta)$. Por lo tanto, sus nuevas coordenadas son:
$$x' = r\cos(\alpha + \theta)$$
$$y' = r\sin(\alpha + \theta)$$
![[angulo_punto_rotado.png]]
3. Expandimos utilizando las identidades trigonométricas para el seno y coseno de la suma de dos ángulos:
$$\cos(\alpha + \theta) = \cos(\alpha)\cos(\theta) - \sin(\alpha)\sin(\theta)$$
$$\sin(\alpha + \theta) = \sin(\alpha)\cos(\theta) + \cos(\alpha)\sin(\theta)$$
4. Sustituyendo este desarrollo dentro de las ecuaciones del punto rotado:
$$x' = r[\cos(\alpha)\cos(\theta) - \sin(\alpha)\sin(\theta)] = (r\cos\alpha)\cos\theta - (r\sin\alpha)\sin\theta$$
$$y' = r[\sin(\alpha)\cos(\theta) + \cos(\alpha)\sin(\theta)] = (r\cos\alpha)\sin\theta + (r\sin\alpha)\cos\theta$$
5. Finalmente, identificamos cuidadosamente que las posiciones originales aparecieron intactas como $x = r\cos(\alpha)$ y $y = r\sin(\alpha)$, de modo que basta con reemplazar de vuelta para coronar la ecuación:
$$x' = x\cos(\theta) - y\sin(\theta)$$
$$y' = x\sin(\theta) + y\cos(\theta)$$
   Alcanzándose exitosamente la validez del teorema planteado. $\blacksquare$

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
### 1.4 Homotecias (Escalamiento)

Pensemos en situaciones donde la forma de una figura no cambia, pero sí su tamaño. Las proporciones se conservan bajo un factor de distorsión puro de aumento o decremento constante.

**Definición 1.6 (Homotecia):**
Una **homotecia** o escalamiento centrada en el origen con razón de escala $k$ (donde $k \in \mathbb{R}$ y $k \neq 0$) es una transformación geométrica que mapea cada punto $(x, y)$ a un nuevo punto $(x', y')$ bajo las reglas simétricas:
$$\begin{cases}
x' = kx \\
y' = ky
\end{cases}$$

> **Observación:** Las propiedades inherentes directas derivan del factor $k$:
> - Si acotamos magnitud $|k| > 1$, impone una **dilatación** dimensional.
> - Si $0 < |k| < 1$, efectúa una compresión o **contracción**.
> - En casos donde $k < 0$, la distorsión escala arrastrando una inversión simultánea (reflexión equivalente pasando de forma recta a través del origen central $(0,0)$).

**Ejemplo 1.5:**
Ejecute sobre el punto de coordenadas $P = (2, -1)$ una función matricial dictada de homotecia de expansión con razón paramétrica pura escalada $k = 3$. Evaluando:
$$\begin{cases}
x' = 3(2) = 6 \\
y' = 3(-1) = -3
\end{cases}$$
El nodo resolutor se materializa en vector final $P' = (6, -3)$.
### 1.5 Reflexiones

Una **reflexión** es una transformación que "espeja" todos los puntos del plano respecto a una recta fija llamada **eje de reflexión**.

**Definición 1.7 (Reflexión):** Dado un eje $\ell$, la reflexión de un punto $P$ es el punto $P'$ tal que $\ell$ es la mediatriz del segmento $PP'$.

**Casos fundamentales:**

| Eje de reflexión | Sustitución en ecuaciones |
|------------------|--------------------------|
| Eje $X$ ($y = 0$) | $(x, y) \to (x, -y)$ |
| Eje $Y$ ($x = 0$) | $(x, y) \to (-x, y)$ |
| Recta $y = x$ | $(x, y) \to (y, x)$ |
| Recta $y = -x$ | $(x, y) \to (-y, -x)$ |
| Origen $(0,0)$ | $(x, y) \to (-x, -y)$ |

**Ejemplo 1.6:**
Refleje el punto $P = (3, 1)$ respecto a: a) el eje $X$, b) el eje $Y$, c) la recta $y = x$:

a) Eje $X$: $P' = (3, -1)$
b) Eje $Y$: $P' = (-3, 1)$
c) $y = x$: $P' = (1, 3)$

### 1.6 Transformaciones combinadas

**Proposición 1.1:**
Las transformaciones se pueden combinar. El orden importa categóricamente:
- Traslación seguida de rotación ≠ Rotación seguida de traslación (en general).

**Ejemplo 1.7:**
Traslade $(1, 0)$ por $(1, 1)$ y luego rote $90°$:
1. Traslación: $(1, 0) \to (2, 1)$
2. Rotación: $(2, 1) \to (2\cos(90°) - 1\sin(90°), 2\sin(90°) + 1\cos(90°)) = (-1, 2)$

**Ejemplo 1.8:**
Aplique a $P = (3, -2)$: primero una reflexión respecto al eje $X$, luego una traslación por el vector $(1, 4)$:
1. Reflexión respecto al eje $X$: $(3, -2) \to (3, 2)$
2. Traslación por $(1, 4)$: $(3, 2) \to (3 + 1,\ 2 + 4) = (4, 6)$

Comparar con el orden inverso (primero traslación, luego reflexión):
1. Traslación por $(1, 4)$: $(3, -2) \to (4, 2)$
2. Reflexión respecto al eje $X$: $(4, 2) \to (4, -2)$

Los resultados $(4, 6) \neq (4, -2)$ confirman de inmediato que **el orden de las transformaciones importa**.

**Ejemplo 1.9 (Asociando escala):**
Establezca las evaluaciones al dictaminar matriz para el punto inicial $P = (2, 4)$, evaluando que este deba sufrir primero un escalamiento de homotecia reductor paramétrico $k = 0.5$ para que el sistema resultante posteriormente acoplarse y dictaminar una traslación del operando por su correspondiente vector rector $(-3, 2)$.
1. Expansión reductiva por Homotecia a $k = 0.5$: $(2, 4) \to (\frac{1}{2} \cdot 2, \frac{1}{2} \cdot 4) = (1, 2)$
2. Sumatoria aditiva escalar rígida de Traslación sumando $(-3, 2)$: $(1, 2) \to (1 - 3, 2 + 2) = (-2, 4)$

---
## 2. Ecuación general de segundo grado

### 2.1 Forma general

**Definición 2.1 (Ecuación general de segundo grado):**
La **ecuación general de segundo grado** en el plano tiene la forma:
$$Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$$

donde $A$, $B$, $C$, $D$, $E$, $F$ son constantes reales y al menos uno de $A$, $B$, $C$ es distinto de cero.

Esta relación nos dará como resultado un círculo, una elipse, una parábola o una hipérbola. Estos cuatro lugares geométricos son llamados las secciones cónicas pues son el resultado de intersecar un cono con un plano.
![[conicas.jpg|524]]
El término cruzado $Bxy$ tiene relación con el ángulo de rotación de la sección cónica. En un principio trabajaremos sin él, pero más adelante lo incorporaremos para ver su comportamiento.

**Observación:** Si los tres coeficientes cuadráticos son nulos ($A = B = C = 0$), la ecuación se reduce a $Dx + Ey + F = 0$, que es la ecuación general de una **recta**. En ese sentido, la ecuación de segundo grado es una generalización: al "activar" los términos cuadráticos pasamos de rectas a cónicas (o a algún caso degenerado).
### 2.2 Clasificación de cónicas

Consideremos la ecuación $Ax^2 + Cy^2 + Dx + Ey + F = 0$ (sin término mixto, $B = 0$) y estudiemos casos según los valores de $A$ y $C$.

**1) Cuando $A = C \neq 0$ → Circunferencia**

$$Ax^2 + Ay^2 + Dx + Ey + F = 0$$
$$A\left(x^2 + \frac{D}{A}x\right) + A\left(y^2 + \frac{E}{A}y\right) = -F$$
$$A\left(x + \frac{D}{2A}\right)^2 + A\left(y + \frac{E}{2A}\right)^2 = -F + \frac{D^2}{4A} + \frac{E^2}{4A}$$
$$\left(x + \frac{D}{2A}\right)^2 + \left(y + \frac{E}{2A}\right)^2 = \frac{D^2 + E^2 - 4AF}{4A^2}$$
$$(x - h)^2 + (y - k)^2 = R^2$$

donde $h = -\dfrac{D}{2A}$, $\quad k = -\dfrac{E}{2A}$, $\quad R = \dfrac{\sqrt{D^2 + E^2 - 4AF}}{2|A|}$

**Circunferencia** con centro $\left(-\dfrac{D}{2A},\, -\dfrac{E}{2A}\right)$ y radio $r = \dfrac{\sqrt{D^2 + E^2 - 4AF}}{2|A|}$ (cuando $D^2 + E^2 - 4AF > 0$).

![[circunferencia_hk.png]]
**2) Cuando $A \neq C$ y tienen el mismo signo → Elipse**

$$A\left(x + \frac{D}{2A}\right)^2 + C\left(y + \frac{E}{2C}\right)^2 = -F + \frac{D^2}{4A} + \frac{E^2}{4C}$$

Sea $R = -F + \dfrac{D^2}{4A} + \dfrac{E^2}{4C}$, dividiendo por $R$:

$$\frac{(x - h)^2}{a^2} + \frac{(y - k)^2}{b^2} = 1$$

donde $h = -\dfrac{D}{2A}$, $\quad k = -\dfrac{E}{2C}$, $\quad a^2 = \dfrac{R}{A}$, $\quad b^2 = \dfrac{R}{C}$, $\quad R = -F + \dfrac{D^2}{4A} + \dfrac{E^2}{4C}$

**Elipse** con semiejes $a = \sqrt{R/A}$ y $b = \sqrt{R/C}$ (cuando $R > 0$, $A > 0$, $C > 0$).

**3) Cuando $A = 0$ o $C = 0$ (pero no ambos) → Parábola**

Si $C = 0$ y $A \neq 0$:

$$Ax^2 + Dx + Ey + F = 0$$
$$A\left(x + \frac{D}{2A}\right)^2 = -Ey - F + \frac{D^2}{4A}$$
$$(x - h)^2 = 4p\,(y - k)$$

donde $h = -\dfrac{D}{2A}$, $\quad k = \dfrac{D^2 - 4AF}{4AE}$, $\quad 4p = -\dfrac{E}{A}$

**Parábola** de eje vertical (abre hacia arriba o abajo).

Si $A = 0$ y $C \neq 0$:

$$Cy^2 + Dx + Ey + F = 0$$
$$C\left(y + \frac{E}{2C}\right)^2 = -Dx - F + \frac{E^2}{4C}$$
$$(y - k)^2 = 4p\,(x - h)$$

donde $k = -\dfrac{E}{2C}$, $\quad h = \dfrac{E^2 - 4CF}{4CD}$, $\quad 4p = -\dfrac{D}{C}$

**Parábola** de eje horizontal (abre hacia la izquierda o derecha).

**4) Cuando $A$ y $C$ tienen signos opuestos → Hipérbola**

Supongamos $A > 0$ y $C < 0$. Completando cuadrados:

$$A\left(x + \frac{D}{2A}\right)^2 + C\left(y + \frac{E}{2C}\right)^2 = R$$

Dividiendo por $R$ (con $R \neq 0$):

$$\frac{(x - h)^2}{a^2} - \frac{(y - k)^2}{b^2} = 1$$

donde $h = -\dfrac{D}{2A}$, $\quad k = -\dfrac{E}{2C}$, $\quad a^2 = \dfrac{R}{A}$, $\quad b^2 = \dfrac{R}{|C|}$, $\quad R = -F + \dfrac{D^2}{4A} + \dfrac{E^2}{4C}$

**Hipérbola** con eje transverso horizontal (si $R > 0$) o vertical (si $R < 0$).

### 2.4 Eliminación del término mixto

Ahora que sabemos clasificar una cónica cuando $B = 0$, nos surge la pregunta: ¿Cómo clasificamos cuando aparece el término cruzado $Bxy$? La estrategia será encontrar una transformación de coordenadas que lo elimine.

**Paso 1: Entendiendo las transformaciones en las cónicas**

Consideremos un círculo arbitrario; ya sabes que su ecuación va a tener la forma de:
$$(x - h)^2 + (y - k)^2 = R^2$$

si pensamos en la translación $x = x' + h$, $y = y' + k$ obtenemos:
$$(x' + h - h)^2 + (y' +k - k)^2 = R^2$$
$$(x')^2 + (y')^2 = R^2$$

En los nuevos ejes, el círculo queda centrado en el origen. Este truco funciona porque la traslación desplaza el **centro** de la cónica. Sin embargo, veamos qué pasa con el término cruzado.

Consideremos la ecuación simplificada $x^2 + xy + y^2 = C$ y apliquemos la traslación $x = x' + \alpha$, $y = y' + \beta$:
$$(x' + \alpha)^2 + (x' + \alpha)(y' + \beta) + (y' + \beta)^2 = C$$
$$(x'+\alpha)^2=x'^2+2x'\alpha + \alpha^2$$
$$(y'+\beta)^2=y'^2+2y'\beta + \beta^2$$
$$(x'+\alpha)(y'+\beta)=x'y'+x'\beta+y'\alpha+\alpha\beta$$

Sumando los tres bloques:
$$x'^2 + 2\alpha x' + \alpha^2 + x'y' + \beta x' + \alpha y' + \alpha\beta + y'^2 + 2\beta y' + \beta^2 = C$$

Recolectando por tipo de término:
$$x'^2 + x'y' + y'^2 + (2\alpha + \beta)\,x' + (\alpha + 2\beta)\,y' + (\alpha^2 + \alpha\beta + \beta^2) = C$$

El coeficiente de $x'y'$ sigue siendo $1$, idéntico al original. La traslación solo agregó términos lineales y desplazó la constante, pero **no modificó ninguno de los coeficientes cuadráticos**. Esto tiene sentido: la traslación reubica el centro de la cónica, pero no cambia su orientación geométrica angular. 

De manera análoga, si intentásemos aplicar un escalamiento mediante una **homotecia** ($x = kx', y = ky'$), el producto algebraico resultaría en $k^2 x'y'$. Aunque cambiaría numéricamente el coeficiente, la homotecia dictamina crecimiento o reducción pura, por lo que su término mixto seguirá estando atado a los ejes sin llegar nunca a eliminarse por completo (a menos que $k=0$, lo cual destruiría la figura).

Necesitamos forzosamente una transformación matricial que sí afecte la orientación de coordenadas paramétricas: una **rotación**.

**Paso 2: La rotación rota los ejes**

Probemos con una rotación de ángulo $\theta$ (antihoraria):
$$\begin{cases}
x = x'\cos\theta - y'\sin\theta \\
y = x'\sin\theta + y'\cos\theta
\end{cases}$$

Sustituimos en $x^2 + xy + y^2 = C$. Calculamos cada término:

$$x^2 = x'^2\cos^2\theta - 2x'y'\cos\theta\sin\theta + y'^2\sin^2\theta$$

$$y^2 = x'^2\sin^2\theta + 2x'y'\cos\theta\sin\theta + y'^2\cos^2\theta$$

$$xy = (x'\cos\theta - y'\sin\theta)(x'\sin\theta + y'\cos\theta)
= x'^2\cos\theta\sin\theta + x'y'(\cos^2\theta - \sin^2\theta) - y'^2\sin\theta\cos\theta$$

Sumando $x^2 + xy + y^2$ y recolectando por tipo de término:

- **Coeficiente de $x'^2$:** $\cos^2\theta + \cos\theta\sin\theta + \sin^2\theta = 1 + \dfrac{\sin(2\theta)}{2}$

- **Coeficiente de $y'^2$:** $\sin^2\theta - \cos\theta\sin\theta + \cos^2\theta = 1 - \dfrac{\sin(2\theta)}{2}$

- **Coeficiente de $x'y'$:** $-2\cos\theta\sin\theta + (\cos^2\theta - \sin^2\theta) + 2\cos\theta\sin\theta = \cos(2\theta)$

La ecuación queda:
$$\left(1 + \frac{\sin 2\theta}{2}\right)x'^2 + \cos(2\theta)\, x'y' + \left(1 - \frac{\sin 2\theta}{2}\right)y'^2 = C$$

Para **eliminar el término $x'y'$** exigimos:
$$\cos(2\theta) = 0 \quad \Longrightarrow \quad 2\theta = 90° \quad \Longrightarrow \quad \theta = 45°$$

Con $\theta = 45°$, $\sin(2\theta) = 1$, y la ecuación se convierte en:
$$\frac{3}{2}\,x'^2 + \frac{1}{2}\,y'^2 = C \quad \Longrightarrow \quad \frac{x'^2}{2C/3} + \frac{y'^2}{2C} = 1$$

La ecuación resultante es la de una **elipse** en el nuevo sistema de coordenadas rotado.

**Paso 3: Generalización a la ecuación completa**

Aplicamos la misma rotación de ángulo $\theta$ a la ecuación general $Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$. Sustituimos:
$$x = x'\cos\theta - y'\sin\theta, \qquad y = x'\sin\theta + y'\cos\theta$$

**Expansión de los términos cuadráticos:**

$$Ax^2 = A\bigl(x'^2\cos^2\theta - 2x'y'\cos\theta\sin\theta + y'^2\sin^2\theta\bigr)$$

$$Cy^2 = C\bigl(x'^2\sin^2\theta + 2x'y'\cos\theta\sin\theta + y'^2\cos^2\theta\bigr)$$

$$Bxy = B\bigl(x'^2\cos\theta\sin\theta + x'y'(\cos^2\theta - \sin^2\theta) - y'^2\sin\theta\cos\theta\bigr)$$

Sumando los tres bloques y recolectando por tipo de término:

- **Coeficiente de $x'^2$:**
$$A\cos^2\theta + B\cos\theta\sin\theta + C\sin^2\theta$$

- **Coeficiente de $y'^2$:**
$$A\sin^2\theta - B\cos\theta\sin\theta + C\cos^2\theta$$

- **Coeficiente de $x'y'$:**
$$-2A\cos\theta\sin\theta + B(\cos^2\theta - \sin^2\theta) + 2C\cos\theta\sin\theta$$

Usando las identidades de ángulo doble $\sin(2\theta) = 2\sin\theta\cos\theta$, $\cos(2\theta) = \cos^2\theta - \sin^2\theta$ y las identidades de potencia $\cos^2\theta = \frac{1+\cos(2\theta)}{2}$, $\sin^2\theta = \frac{1-\cos(2\theta)}{2}$, podemos reescribir cada coeficiente en forma compacta:

$$A' = \frac{A+C}{2} + \frac{(A-C)\cos(2\theta)}{2} + \frac{B\sin(2\theta)}{2}$$
$$C' = \frac{A+C}{2} - \frac{(A-C)\cos(2\theta)}{2} - \frac{B\sin(2\theta)}{2}$$
$$B' = B\cos(2\theta) - (A-C)\sin(2\theta)$$

Nota: se puede verificar fácilmente que $A' + C' = A + C$, es decir, **la traza es invariante** (esto corresponde a temas de álgebra lineal) bajo la rotación.
Para demostrarlo solo debemos sumar los términos expuestos arriba:
$$A'+C' = \frac{A+C}{2} + \frac{A+C}{2} = A+C$$

**Expansión de los términos lineales:**

$$Dx + Ey = D(x'\cos\theta - y'\sin\theta) + E(x'\sin\theta + y'\cos\theta)$$
$$= (D\cos\theta + E\sin\theta)\,x' + (-D\sin\theta + E\cos\theta)\,y'$$

Por lo tanto:
$$D' = D\cos\theta + E\sin\theta, \qquad E' = -D\sin\theta + E\cos\theta, \qquad F' = F$$

**Condición de eliminación del término mixto:**

Exigimos $B' = 0$:
$$B\cos(2\theta) - (A-C)\sin(2\theta) = 0$$
$$B\cos(2\theta) = (A-C)\sin(2\theta)$$

Dividiendo (cuando $A \neq C$ y $\cos(2\theta) \neq 0$):
$$\tan(2\theta) = \frac{B}{A - C}$$

Caso especial: si $A=C$, entonces tendremos:
$$B\cos(2\theta) = 0$$
por lo tanto $2\theta = 90° \to \theta = 45°$

**Teorema 2.2 (Rotación para eliminar el término mixto):**
El término $Bxy$ en $Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$ se elimina mediante una rotación de ángulo $\theta$ donde:
$$\tan(2\theta) = \frac{B}{A - C}$$

Tras la rotación, la ecuación queda en la forma clasificable de §2.2:
$$A'x'^2 + C'y'^2 + D'x' + E'y' + F' = 0$$

donde los nuevos coeficientes cuadráticos son:
$$A' = A\cos^2\theta + B\cos\theta\sin\theta + C\sin^2\theta$$
$$C' = A\sin^2\theta - B\cos\theta\sin\theta + C\cos^2\theta$$
y los coeficientes lineales serán
$$D' = D\cos\theta + E\sin\theta$$
$$E' = -D\sin\theta + E\cos\theta$$
$$F' = F$$
### 2.3 El discriminante y su invarianza

**Definición 2.2 (Discriminante):**
Dada la ecuación general de segundo grado $Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$, se define el **discriminante** como:
$$\Delta = B^2 - 4AC$$

Esta expresión involucra únicamente los coeficientes de los términos cuadráticos y captura la "forma geométrica" de la cónica, independientemente de su posición o ángulo en el plano.

**Proposición 2.1 (Invarianza bajo traslación):**
Una traslación no modifica los coeficientes $A$, $B$, $C$, por lo que:
$$\Delta' = B'^2 - 4A'C' = B^2 - 4AC$$

Esto es inmediato: como vimos en el Paso 1 del §2.4, la traslación solo agrega términos lineales.

**Proposición 2.2 (Invarianza bajo rotación):**
Tras una rotación de ángulo $\theta$, los nuevos coeficientes cuadráticos son:
$$A' = \frac{A+C}{2} + \frac{(A-C)\cos(2\theta)}{2} + \frac{B\sin(2\theta)}{2}$$
$$C' = \frac{A+C}{2} - \frac{(A-C)\cos(2\theta)}{2} - \frac{B\sin(2\theta)}{2}$$
$$B' = B\cos(2\theta) - (A-C)\sin(2\theta)$$

Calculamos $B'^2 - 4A'C'$ directamente. Partimos de las expresiones obtenidas en §2.2:

**Paso 1: Calculamos $B'^2$.**

Usamos la notación $s = \sin(2\theta)$, $c = \cos(2\theta)$ para no cargar la escritura. Entonces:
$$B'^2 = \bigl[Bc - (A-C)s\bigr]^2 = B^2c^2 - 2B(A-C)sc + (A-C)^2s^2$$

**Paso 2: Calculamos $4A'C'$.**

Notamos que $A'$ y $C'$ tienen la forma $\frac{A+C}{2} \pm u$ con $u = \frac{(A-C)c + Bs}{2}$, por lo que:
$$4A'C' = 4\left(\frac{A+C}{2} + u\right)\left(\frac{A+C}{2} - u\right) = 4\left[\left(\frac{A+C}{2}\right)^2 - u^2\right] = (A+C)^2 - 4u^2$$

Calculamos $u^2$:
$$u^2 = \frac{(A-C)^2c^2 + 2B(A-C)sc + B^2s^2}{4}$$

Por lo tanto:
$$4A'C' = (A+C)^2 - (A-C)^2c^2 - 2B(A-C)sc - B^2s^2$$

**Paso 3: Calculamos $B'^2 - 4A'C'$.**

$$B'^2 - 4A'C' = B^2c^2 - 2B(A-C)sc + (A-C)^2s^2 - (A+C)^2 + (A-C)^2c^2 + 2B(A-C)sc + B^2s^2$$

Los términos $\pm 2B(A-C)sc$ se cancelan:
$$= B^2(c^2 + s^2) + (A-C)^2(s^2 + c^2) - (A+C)^2$$

Como $s^2 + c^2 = \sin^2(2\theta) + \cos^2(2\theta) = 1$:
$$= B^2 + (A-C)^2 - (A+C)^2$$

Expandiendo:
$$= B^2 + A^2 - 2AC + C^2 - A^2 - 2AC - C^2 = B^2 - 4AC$$

Por lo tanto:
$$\boxed{B'^2 - 4A'C' = B^2 - 4AC}$$

**El discriminante es invariante bajo rotaciones.** $\blacksquare$
> **Consecuencia:** Como el discriminante no cambia bajo traslaciones ni rotaciones, podemos calcular $\Delta = B^2 - 4AC$ directamente en la ecuación original y aprovecharlo para clasificar la cónica, sin necesidad de realizar ninguna transformación previa.

**Proposición 2.3 (El discriminante como término de la fórmula general cuadrática):**
Alternativamente, podemos justificar de manera natural el protagonismo de esta expresión analizando nuestro problema inicial simplemente como un polinomio cuadrático que intentamos resolver algebraicamente (despejando, por ejemplo, la variable $y$).

**Demostración analítica:**
Si retomamos nuestra la ecuación general original:
$$Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$$

Podemos reagruparla explícitamente tratando a $y$ como nuestra incógnita operativa, y al resto de elementos (incluyendo a $x$) como agrupaciones paramétricas constantes. Ordenando descendentemente por potencias de $y$:
$$Cy^2 + (Bx + E)y + (Ax^2 + Dx + F) = 0$$

Notamos que nos enfrentamos a una clásica ecuación de la forma $\alpha y^2 + \beta y + \gamma = 0$, identificando a:
- $\alpha = C$
- $\beta = (Bx + E)$
- $\gamma = (Ax^2 + Dx + F)$

Para despejar $y(x)$, utilizamos infaliblemente la fórmula resolvente de segundo grado:
$$y = \frac{- \beta \pm \sqrt{\beta^2 - 4\alpha\gamma}}{2\alpha}$$

Concentremos nuestra atención de manera exclusiva en el corazón o condición de realidad (el interior de la raíz cuadrada o "radicando"):
$$\text{Radicando} = (Bx + E)^2 - 4C(Ax^2 + Dx + F)$$

Desarrollamos los productos y el binomio al cuadrado:
$$\text{Radicando} = B^2x^2 + 2BEx + E^2 - 4ACx^2 - 4CDx - 4CF$$

Agrupamos finalmente los componentes basándonos ahora en el grado de $x$:
$$\text{Radicando} = (B^2 - 4AC)x^2 + (2BE - 4CD)x + (E^2 - 4CF)$$

Es justo en esta estructura polinómica donde la identidad se revela: para valores grandes de $x$, el **comportamiento asintótico o dominios posibles** es dictado fuertemente por su coeficiente principal cuadrático $x^2$. Ese bloque multiplicador inquebrantable de control es, exactamente, el factor $(B^2 - 4AC)$.

- Si este factor es **negativo**, provocará rápidamente que toda el área de números colapse a raíces negativas (imaginarios) impidiendo que la curva siga existiendo, lo que físicamente implica una figura confinada, cerrada y acotada (**las elipses y círculos**).
- Si es **positivo**, entonces para número grandes el radicando tenderá holgadamente hacia una raíz real lícita posibilitando infinitas soluciones, manifestándose en curvas que viajan sin fin al infinito (**las ramas de la hipérbola**). $\blacksquare$

### 2.4 Clasificación por discriminante

**Teorema 2.2 (Clasificación por discriminante):**
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

**Demostración:**

La idea clave es combinar los dos resultados anteriores:

- Por el **Teorema 2.1**, existe una rotación de ángulo $\theta$ tal que $B' = 0$. La ecuación queda:
$$A'x'^2 + C'y'^2 + D'x' + E'y' + F' = 0$$

- Por la **Proposición 2.2**, el discriminante es invariante, luego:
$$\Delta = B^2 - 4AC = B'^2 - 4A'C' = 0 - 4A'C' = -4A'C'$$

Por lo tanto el signo de $\Delta$ determina exactamente el signo del producto $A'C'$, y entramos directamente en la clasificación del §2.2:

**Caso $\Delta < 0$:** $\;-4A'C' < 0 \Rightarrow A'C' > 0$, es decir $A'$ y $C'$ tienen el **mismo signo**.

Por §2.2 (Casos 1 y 2), esto corresponde a una **circunferencia** (si además $A'=C'$) o una **elipse** (si $A' \neq C'$). En términos de la ecuación original: $A'=C'$ ocurre cuando $A=C$ y $B=0$, pues la rotación no mezcla los coeficientes en ese caso.

**Caso $\Delta = 0$:** $\;-4A'C' = 0 \Rightarrow A' = 0$ ó $C' = 0$.

Si $A'=0$: la ecuación tiene solo $C'y'^2 + D'x' + E'y' + F' = 0$, que es una **parábola** en $y'$ (con eje horizontal en el sistema rotado). Análogamente si $C'=0$. Por §2.2 (Caso 3), esto es una parábola.

**Caso $\Delta > 0$:** $\;-4A'C' > 0 \Rightarrow A'C' < 0$, es decir $A'$ y $C'$ tienen **signos opuestos**.

Por §2.2 (Caso 4), esto corresponde a una **hipérbola**. $\blacksquare$

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

---
## 3. Secciones cónicas: definición geométrica

Aquí estudiaremos las secciones cónicas a más profundidad y con un enfoque más geométrico.

### 3.1 El cono circular recto

**Definición 3.1 (Cono circular recto):**
Un **cono circular recto** es la superficie generada por una recta (generatriz) que pasa por un punto fijo (vértice) y forma un ángulo constante con un eje fijo.
![[cono_circular.png]]
**Definición 3.2 (Sección cónica):**
Una **sección cónica** (o **cónica**) es la curva resultante de la intersección de un plano con un cono circular recto doble (dos conos opuestos por el vértice).
### 3.2 Tipos de secciones cónicas

Dependiendo del ángulo del plano de corte:

**1. Circunferencia:**
- Plano perpendicular al eje del cono
![[circulo_como_conica.jpg|327]]

**2. Elipse:**
- Plano oblicuo que corta una hoja del cono
- No paralelo a ninguna generatriz
![[elipse_como_conica.png|277]]

**3. Parábola:**
- Plano paralelo a una generatriz del cono
![[parabola_como_conica.png]]

**4. Hipérbola:**
- Plano que corta ambas hojas del cono
![[hiperbola_como_conica.png]]
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

**Demostración:**

Sea $C = (h, k)$ el centro fijo y $r > 0$ el radio. Por definición, un punto $P = (x, y)$ pertenece a la circunferencia si y solo si su distancia al centro es exactamente $r$:
$$d(P, C) = r$$

Aplicamos la fórmula de distancia entre dos puntos en $\mathbb{R}^2$:
$$d(P, C) = \sqrt{(x - h)^2 + (y - k)^2}$$

Sustituyendo la condición:
$$\sqrt{(x - h)^2 + (y - k)^2} = r$$

Como $r > 0$, ambos lados son no negativos y podemos elevar al cuadrado sin perder equivalencia:
$$\boxed{(x - h)^2 + (y - k)^2 = r^2}$$

El conjunto de todos los puntos $(x,y)$ que satisfacen esta ecuación es exactamente la circunferencia. $\blacksquare$

**Caso particular (centro en el origen):**
Si $h = k = 0$:
$$x^2 + y^2 = r^2$$

**Ejemplo 4.1:**
La circunferencia con centro $(2, -3)$ y radio $5$ tiene ecuación:
$$(x - 2)^2 + (y + 3)^2 = 25$$

### 4.2 Ecuación general a canónica

**Proposición 4.1:**
Con lo que ya hemos estudiado de la ecuación general de segundo grado y la ecuación canónica de la circunferencia, ahora practicaremos ejercicios académicos con ambas.
*Para convertir de forma general a canónica:*
Tenemos la ecuación $Ax^2 + Bxy + Cy^2 + Dx + Ey + F = 0$, la estrategia aquí será la de **Completar de cuadrados:**
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

> **Casos Degenerados de la Circunferencia:**
> Al completar los cuadrados, la constante final en el lado derecho (que llamaremos $M$) dictará la naturaleza real del lugar geométrico $(x - h)^2 + (y - k)^2 = M$:
> 1. Si $M > 0$: Corresponde a una **circunferencia real** con radio $r = \sqrt{M}$.
> 2. Si $M = 0$: Corresponde a una **circunferencia degenerada** de radio nulo. La figura geométrica colapsa y representa únicamente un **punto** ubicado en el centro $(h, k)$.
> 3. Si $M < 0$: Corresponde a un **conjunto vacío** (también referido a veces como circunferencia imaginaria), dado que en los reales la suma de dos números al cuadrado no puede dar un resultado negativo.

**Ejemplo 4.3 (Identificando un caso degenerado):**
Analice y determine qué figura geométrica describe $x^2 + y^2 - 2x + 6y + 10 = 0$.

$$\begin{align}
x^2 - 2x + y^2 + 6y &= -10 \\
(x^2 - 2x + 1) + (y^2 + 6y + 9) &= -10 + 1 + 9 \\
(x - 1)^2 + (y + 3)^2 &= 0
\end{align}$$

Como $M=0$, se trata de una circunferencia degenerada que describe únicamente al punto singular $(1, -3)$.

*Para convertir de forma canónica a general:*
Tenemos una circunferencia centrada en $(h,k)$ con radio R $(x-h)^2 + (y-k)^2 = R^2$, la estrategia ahora será simplemente desarrollar los paréntesis.

**Ejemplo 4.4:**
Convierta la ecuación canónica $(x - 2)^2 + (y + 5)^2 = 9$ a forma general.

Desarrollando los paréntesis:
$$(x-2)^2 = x^2 - 4x + 4$$
$$(y+5)^2 = y^2 + 10y + 25$$

Sumando y pasando el $9$ al lado izquierdo:
$$x^2 - 4x + 4 + y^2 + 10y + 25 - 9 = 0$$
$$x^2 + y^2 - 4x + 10y + 20 = 0$$

Verificación: $D = -4 = -2h = -2(2)$ ✓, $E = 10 = -2k = -2(-5)$ ✓, $F = h^2 + k^2 - r^2 = 4 + 25 - 9 = 20$ ✓

### 4.3 El número $\pi$

**Definición 4.2 (Número $\pi$):**
El número $\pi$ (pi) es la constante definida como la razón entre la **circunferencia** (perímetro) de un círculo y su **diámetro**:
$$\pi = \frac{P}{d} = \frac{P}{2r}$$

donde $C$ es la longitud de la circunferencia y $d = 2r$ es el diámetro.

**Valor aproximado:** $\pi \approx 3.14159265358979...$

**Propiedad:** $\pi$ es un número irracional y trascendente.

### 4.4 Perímetro y área

**Teorema 4.2 (Perímetro):**
El **perímetro** o **longitud de la circunferencia** de radio $r$ es:
$$P = 2\pi r$$

**Teorema 4.3 (Área):**
El **área del círculo** de radio $r$ es:
$$A = \pi r^2$$

**Ejemplo 4.4:**
Para un círculo de radio $5$ cm:
- Perímetro: $C = 2\pi(5) = 10\pi \approx 31.42$ cm
- Área: $A = \pi(5)^2 = 25\pi \approx 78.54$ cm²

### 4.5 Arco de circunferencia

**Definición 4.3 (Arco):**
Un **arco** es una porción de la circunferencia delimitada por dos puntos.

**Teorema 4.4 (Longitud de arco):**
La longitud de un arco que subtiende un ángulo central $\theta$ (en radianes) en una circunferencia de radio $r$ es:
$$s = r\theta$$

**Ejemplo 4.5:**
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

**Teorema 5.1 (Ecuación canónica):**
La elipse con centro en el origen y focos sobre el eje $x$ tiene ecuación canónica:
$$\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1, \quad \text{con } a > b > 0$$

**Demostración geométrica:**
1. Consideremos una elipse centrada en el origen $(0,0)$ con focos $F_1 = (-c, 0)$ y $F_2 = (c, 0)$.
2. Todo punto $P = (x, y)$ de la elipse cumple:
   $$d(P, F_1) + d(P, F_2) = 2a$$
3. Reemplazando por la fórmula de distancia:
   $$\sqrt{(x + c)^2 + (y - 0)^2} + \sqrt{(x - c)^2 + (y - 0)^2} = 2a$$
4. Aislamos una de las raíces y elevamos al cuadrado:
   $$\sqrt{(x + c)^2 + y^2} = 2a - \sqrt{(x - c)^2 + y^2}$$
   $$(x + c)^2 + y^2 = 4a^2 - 4a\sqrt{(x - c)^2 + y^2} + (x - c)^2 + y^2$$
5. Expandimos los binomios y cancelamos términos comunes ($x^2, c^2, y^2$):
   $$2cx = 4a^2 - 4a\sqrt{(x - c)^2 + y^2} - 2cx$$
   $$4cx - 4a^2 = - 4a\sqrt{(x - c)^2 + y^2}$$
6. Dividimos por $-4$ y volvemos a elevar al cuadrado:
   $$a^2 - cx = a\sqrt{(x - c)^2 + y^2}$$
   $$(a^2 - cx)^2 = a^2\left((x - c)^2 + y^2\right)$$
   $$a^4 - 2a^2 cx + c^2 x^2 = a^2(x^2 - 2cx + c^2 + y^2)$$
7. Cancelamos $-2a^2 cx$ y reagrupamos $x$ e $y$:
   $$(a^2 - c^2)x^2 + a^2 y^2 = a^2(a^2 - c^2)$$
8. De la geometría de la elipse, cuando evaluamos en un vértice menor se forma un triángulo rectángulo con catetos $b$ y $c$, e hipotenusa $a$. Por ende $a^2 = b^2 + c^2$. Definimos entonces $b^2 = a^2 - c^2$:
   $$b^2 x^2 + a^2 y^2 = a^2 b^2$$
9. Al dividir todo entre la constante $a^2b^2$:
   $$\boxed{\frac{x^2}{a^2} + \frac{y^2}{b^2} = 1} \quad \blacksquare$$

**Caso particular (orientación en el eje Y):**
Si el eje rector o mayor se encuentra en posición vertical, ubicando sus focos en $(0, \pm c)$, la ecuación resulta:
$$\frac{x^2}{b^2} + \frac{y^2}{a^2} = 1$$
*(Nota: El denominador mayor siempre acompaña a la variable espacial de mayor elongación focal. Si $a^2$ está bajo $y^2$, la elipse es vertical).*

**Ecuación canónica desplazada:**
Bajo una traslación clásica $(x-h)$ y $(y-k)$, la elipse traslada su centro al punto $(h, k)$:
- **Horizontal:** $\frac{(x - h)^2}{a^2} + \frac{(y - k)^2}{b^2} = 1$
- **Vertical:** $\frac{(x - h)^2}{b^2} + \frac{(y - k)^2}{a^2} = 1$

**Ejemplo 5.1:**
Identifique los elementos de la elipse $\frac{(x - 2)^2}{16} + \frac{(y + 1)^2}{25} = 1$:
- **Centro:** $(2, -1)$
- **Orientación:** Al estar el denominador mayor (25) bajo la variable Y, la elipse es de orientación vertical.
- $a^2 = 25 \Rightarrow a = 5$ 
- $b^2 = 16 \Rightarrow b = 4$
- Longitud del centro al foco: $c = \sqrt{a^2 - b^2} = \sqrt{25 - 16} = 3$
- **Focos:** Estando en el eje Y vertical, al centro $(2, -1)$ le sumamos/restamos $c$ en su ordenada, resultando $F_1 = (2, 2)$ y $F_2 = (2, -4)$.

### 5.2 Elementos de la elipse

**Componentes principales:**

1. **Focos:** $F_1$ y $F_2$, separados por la distancia constante de $2c$.
2. **Centro:** Punto medio entre ambos focos y centro de simetría de la elipse.
3. **Eje mayor:** Segmento recto de medida $2a$ que une la elipse de extremo a extremo pasando por el centro y los focos.
4. **Eje menor:** Segmento perpendicular al eje mayor, de longitud $2b$.
5. **Vértices mayores:** Puntos de intersección del perímetro con el eje mayor.
6. **Vértices menores:** Puntos de intersección del perímetro con el eje menor.

**Relación fundamental:**
$$a^2 = b^2 + c^2$$

donde:
- $a$ = semieje mayor
- $b$ = semieje menor
- $c$ = distancia del centro a cada foco

```text
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

### 5.3 Ecuación general a canónica

**Proposición 5.1:**
Similar al caso de la circunferencia, podemos convertir una ecuación polinomial $Ax^2 + Cy^2 + Dx + Ey + F = 0$ a su forma canónica mediante la **completación de cuadrados** (con la condición $A$ y $C$ del mismo signo, pero $A \neq C$). 

**Ejemplo 5.2 (Completación de cuadrados en la elipse):**
Lleve $9x^2 + 4y^2 - 36x + 8y + 4 = 0$ a forma canónica.

**Solución paso a paso:**
$$\begin{align}
9x^2 - 36x + 4y^2 + 8y &= -4 \\
9(x^2 - 4x) + 4(y^2 + 2y) &= -4 \\
9(x^2 - 4x + 4) + 4(y^2 + 2y + 1) &= -4 + 36 + 4 \\
9(x - 2)^2 + 4(y + 1)^2 &= 36 \\
\frac{(x - 2)^2}{4} + \frac{(y + 1)^2}{9} &= 1
\end{align}$$

- **Centro:** $(2, -1)$
- **Orientación:** Eje mayor vertical.
- $a = 3$, $b = 2$, distancia focal $c = \sqrt{9-4} = \sqrt{5}$.

> **Casos Degenerados de la Elipse:**
> Al completar los cuadrados, la constante final a la que igualamos la ecuación estandarizada estipula la existencia del lugar geométrico $\frac{(x-h)^2}{a^2} + \frac{(y-k)^2}{b^2} = M$:
> 1. Si $M > 0$: Con un simple despeje obtenemos la forma canónica base equivaliendo a $1$. Existe una **elipse real**.
> 2. Si $M = 0$: Corresponde a una **elipse degenerada**. Dado que los cuadrados no pueden sumar cero a menos que ambos sean nulos, la geometría colapsa exclusivamente al centro $(h, k)$, es decir, a un simple **punto**.
> 3. Si $M < 0$: Esta suma arroja una contradicción matemática (cuadrados positivos no originan números negativos), dando lugar a una figura inerte conocida como conjunto vacío o **elipse imaginaria**.

**Ejemplo 5.3 (Identificando un caso degenerado):**
Analice la ecuación $2x^2 + 3y^2 - 8x + 6y + 11 = 0$.

$$\begin{align}
2(x^2 - 4x) + 3(y^2 + 2y) &= -11 \\
2(x^2 - 4x + 4) + 3(y^2 + 2y + 1) &= -11 + 8 + 3 \\
2(x - 2)^2 + 3(y + 1)^2 &= 0
\end{align}$$

Como la suma da cero absoluto ($M=0$), concluimos que es una elipse degenerada contenida estrictamente en el punto singular $(2, -1)$.

### 5.4 Excentricidad

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

### 5.5 Propiedades de la elipse

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

1. **Foco ($F$):** Punto fijo de anclaje ubicado en el lado interno de la curva parabólica.
2. **Directriz ($\ell$):** Recta estática exterior a la curva, perpendicular al eje de simetría.
3. **Vértice ($V$):** Punto principal de inflexión o doblez de la parábola, ubicado exactamente en el punto medio entre el foco y la directriz.
4. **Eje de simetría:** Recta que parte la parábola en dos mitades idénticas, atraviesa el vértice y al foco, conectándolos de manera perpendicular con la directriz.
5. **Parámetro ($p$):** La distancia constante que separa al vértice y al foco (y equivalentemente, al vértice de la directriz).

```text
        Directriz
    -----|-----
         | p
         •  P(x,y) (punto general en parábola)
        /|
       / |
      /  |
     •---|--- Eje de simetría
     F   V
   Foco  Vértice
```

### 6.3 Ecuación canónica

**Teorema 6.1 (Ecuación canónica de la parábola):**
La parábola centrada en el origen con vértice en $V(0,0)$ y eje de simetría vertical, abriendo hacia arriba, se expresa algebraicamente como:
$$x^2 = 4py, \quad \text{con } p > 0$$

donde su foco se ubica en $F = (0, p)$ y su recta directriz es $y = -p$.

**Demostración geométrica:**
1. Consideremos el vértice base en el origen $(0,0)$. Por ende, un foco definido sobre el eje $y$ estará en $(0, p)$ y la directriz horizontal opuesta será $y = -p$.
2. Por definición primaria, la curva se compone de todos los puntos $P = (x, y)$ que cumplen la métrica de equidistancia:
   $$d(P, \text{Foco}) = d(P, \text{Directriz})$$
3. Insertando la fórmula de distancia (sabiendo que la distancia más corta de $P(x,y)$ a la recta horizontal $y = -p$ es al punto ortogonal $P'(x, -p)$):
   $$\sqrt{(x - 0)^2 + (y - p)^2} = \sqrt{(x - x)^2 + (y - (-p))^2}$$
   $$\sqrt{x^2 + (y - p)^2} = \sqrt{(y + p)^2}$$
4. Elevamos ambos lados al cuadrado para eliminar los radicales:
   $$x^2 + (y - p)^2 = (y + p)^2$$
5. Expandimos los binomios al cuadrado a ambos lados de la igualdad:
   $$x^2 + y^2 - 2py + p^2 = y^2 + 2py + p^2$$
6. Cancelamos los términos idénticos en ambos lados ($y^2$ y $p^2$):
   $$x^2 - 2py = 2py$$
7. Ajustamos pasando el factor $y$ lineal y finalizando nuestro despeje obtenemos:
   $$\boxed{x^2 = 4py} \quad \blacksquare$$

*(Nota: En análisis de funciones se suele utilizar el formato general simplificado $y = a x^2$. Notemos que ambas representaciones son totalmente compatibles y análogas sabiendo que la constante de amplitud simplemente es $a = \frac{1}{4p}$).*

**Casos particulares (Orientación espacial):**
Intercambiando los signos y las variables cuadráticas en las fórmulas, la geometría de la parábola adopta distintas orientaciones de apertura:
- **Apertura inferior (hacia abajo, eje Y negativo):** $x^2 = -4py$ con $F=(0, -p)$
- **Apertura lateral derecha (hacia la derecha, eje X positivo):** $y^2 = 4px$ con $F=(p, 0)$
- **Apertura lateral izquierda (hacia la izquierda, eje X negativo):** $y^2 = -4px$ con $F=(-p, 0)$

**Ecuación con vértice desplazado:**
Aplicando traslaciones para desplazar el vértice originario al punto coordenado $(h,k)$, la fórmula evoluciona integralmente:
- **Aperturas de alineación vertical (arriba/abajo):** $(x - h)^2 = \pm 4p(y - k)$
- **Aperturas de alineación horizontal (laterales):** $(y - k)^2 = \pm 4p(x - h)$

**Ejemplo 6.1:**
Identifique los componentes geométricos de la parábola $(x - 3)^2 = -8(y + 2)$:
- **Vértice originario:** $(3, -2)$.
- **Orientación:** Ya que su variable cuadrática recae en las abscisas "X", su eje de apertura debe ser simétricamente vertical. Debido a que el factor es negativo $(-8)$, esta parábola se abre lógicamente **hacia abajo**.
- El parámetro métrico será absoluto: $4p = 8 \Rightarrow p = 2$.
- **Focos y directrices:** Al estar la curva apuntando hacia la directriz inferior vertical, el foco obligatoriamente se debe ubicar restándole en el eje y las $p$ unidades base: $F = (3, -2 - 2) = (3, -4)$. Reubicando en contraste la barrera directriz opuesta en $y = -2 + 2 = 0$.

### 6.4 Ecuación general a canónica

**Proposición 6.1 (Recuperación de canónica):**
A marcada diferencia estructural con circunferencias y elipses puras, en el polinomio completo general de una parábola, observaremos un fuerte diferencial estandarizado: **solamente presentará una variable de la fórmula general elevada al factor cuadrático** exclusivo o puro.
Es decir, será obligatoriamente de la forma $Ax^2 + Dx + Ey + F = 0$ o bien limitando a $Cy^2 + Dx + Ey + F = 0$. Para recuperar a su original forma canónica, se deberá aislar metódicamente y aplicar el proceso de completación solo a la variable que se presente en grado dos.

**Ejemplo 6.2 (Completación de cuadrados en la parábola):**
Normalice la ecuación polinomial $x^2 - 4x - 8y + 12 = 0$ encontrando su forma canónica desplazada, sus focos y su vértice referencial.

**Solución paso a paso:**
$$\begin{align}
x^2 - 4x &= 8y - 12 \\
x^2 - 4x + 4 &= 8y - 12 + 4 \\
(x - 2)^2 &= 8y - 8 \\
(x - 2)^2 &= 8(y - 1)
\end{align}$$

- **Vértice general:** $(2, 1)$.
- **Orientación:** Cuyo factor resultante en base $y$ en lateral es positivo, la apertura rige de manera vertical base hacia arriba.
- Extrayendo parámetro: $4p = 8 \Rightarrow p = 2$.
- **Foco:** Si el vértice descansa sobre $y=1$ y abre hacia el cielo, sumamos su foco analógico y concluimos en el punto exacto $(2, 3)$.

> **Casos Degenerados de la Parábola:**
> ¿Qué pasa en completaciones fallidas si falta la variable de grado lineal opuesta final en su completación resolutoria igualizadora terminal? $(x - h)^2 = M$:
> 1. Si el escalar transicional equivale a $M > 0$: Al carecer de la variable $y$, se trata de puras constantes directas dependientes de la $x$, por ende converge desdoblándose de la forma $x = h \pm \sqrt{M}$, trazando en el plano **dos rectas verticales exactamente paralelas** y separadas.
> 2. Si el escalar colapsa a $M = 0$: Las dos líneas rectas se repliegan sobre sí mismas por no haber distancia de separación, resultando en **una solitaria recta doble idéntica** ($x=h$).
> 3. Si por el contrario la igualdad asume un resultado matemáticamente irracional de $M < 0$: Proyecta matriz irresoluble, derivando el escenario geométrico en **rectas imaginarias o un conjunto vacío**.

### 6.5 Propiedades de la parábola

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

para todo punto $P$ en la hipérbola, donde $a$ es el **semieje transverso**.

**Teorema 7.1 (Ecuación canónica):**
La hipérbola con centro en el origen y focos sobre el eje $x$ tiene ecuación canónica:
$$\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1, \quad \text{con } c > a > 0$$

**Demostración geométrica:**
1. Consideremos una hipérbola centrada en el origen $(0,0)$ con focos $F_1 = (-c, 0)$ y $F_2 = (c, 0)$.
2. Todo punto $P = (x, y)$ de la hipérbola cumple:
   $$|d(P, F_1) - d(P, F_2)| = 2a$$
   Podemos quitar el valor absoluto considerando $d(P, F_1) - d(P, F_2) = \pm 2a$.
3. Reemplazando por la fórmula de distancia:
   $$\sqrt{(x + c)^2 + (y - 0)^2} - \sqrt{(x - c)^2 + (y - 0)^2} = \pm 2a$$
4. Aislamos una de las raíces y elevamos al cuadrado:
   $$\sqrt{(x + c)^2 + y^2} = \pm 2a + \sqrt{(x - c)^2 + y^2}$$
   $$(x + c)^2 + y^2 = 4a^2 \pm 4a\sqrt{(x - c)^2 + y^2} + (x - c)^2 + y^2$$
5. Expandimos los binomios y cancelamos términos comunes ($x^2, c^2, y^2$):
   $$2cx = 4a^2 \pm 4a\sqrt{(x - c)^2 + y^2} - 2cx$$
   $$4cx - 4a^2 = \pm 4a\sqrt{(x - c)^2 + y^2}$$
6. Dividimos por $4$ y volvemos a elevar al cuadrado (el $\pm$ desaparece):
   $$cx - a^2 = \pm a\sqrt{(x - c)^2 + y^2}$$
   $$(cx - a^2)^2 = a^2\left((x - c)^2 + y^2\right)$$
   $$c^2 x^2 - 2a^2 cx + a^4 = a^2(x^2 - 2cx + c^2 + y^2)$$
7. Cancelamos $-2a^2 cx$ y reagrupamos $x$ e $y$:
   $$(c^2 - a^2)x^2 - a^2 y^2 = a^2(c^2 - a^2)$$
8. De la geometría de la hipérbola sabemos que $c > a$. Definimos entonces la constante positiva $b^2 = c^2 - a^2$:
   $$b^2 x^2 - a^2 y^2 = a^2 b^2$$
9. Al dividir todo entre la constante $a^2b^2$:
   $$\boxed{\frac{x^2}{a^2} - \frac{y^2}{b^2} = 1} \quad \blacksquare$$

**Caso particular (orientación en el eje Y):**
Si el eje transverso o principal se encuentra en posición vertical, ubicando sus focos en $(0, \pm c)$, la ecuación resulta:
$$\frac{y^2}{a^2} - \frac{x^2}{b^2} = 1$$
*(Nota: A diferencia de la elipse, aquí no orienta el denominador mayor, sino el término con **signo positivo**. Si $y^2$ es positivo, la hipérbola es vertical).*

**Ecuación canónica desplazada:**
Bajo una traslación clásica $(x-h)$ y $(y-k)$, la hipérbola traslada su centro al punto $(h, k)$:
- **Horizontal:** $\frac{(x - h)^2}{a^2} - \frac{(y - k)^2}{b^2} = 1$
- **Vertical:** $\frac{(y - k)^2}{a^2} - \frac{(x - h)^2}{b^2} = 1$

**Ejemplo 7.1:**
Identifique los elementos de la hipérbola $\frac{(y + 1)^2}{4} - \frac{(x - 2)^2}{9} = 1$:
- **Centro:** $(2, -1)$
- **Orientación:** Al estar el término de $Y$ como la fracción positiva, la hipérbola es de orientación vertical.
- $a^2 = 4 \Rightarrow a = 2$
- $b^2 = 9 \Rightarrow b = 3$
- Longitud del centro al foco: $c = \sqrt{a^2 + b^2} = \sqrt{4 + 9} = \sqrt{13}$
- **Focos:** Estando en el eje Y vertical, al centro $(2, -1)$ le sumamos/restamos $c$ en su ordenada, resultando focos en $F_1 = (2, -1 + \sqrt{13})$ y $F_2 = (2, -1 - \sqrt{13})$.

### 7.2 Elementos de la hipérbola

**Componentes principales:**

1. **Focos:** $F_1$ y $F_2$, separados por la distancia constante de $2c$.
2. **Centro:** Punto medio entre ambos focos y centro de simetría de la hipérbola.
3. **Eje transverso (real):** Segmento de longitud $2a$ que une los vértices métricamente reales de la hipérbola.
4. **Eje conjugado (imaginario):** Segmento perpendicular de longitud $2b$ a través del centro.
5. **Vértices:** Puntos de intersección entre las ramas de la hipérbola y el eje transverso.
6. **Asíntotas:** Vías delimitantes a las que la hipérbola se aproxima en el infinito sin llegar a tocarlas, dadas por diagonales de un rectángulo imaginario.

**Relación fundamental:**
$$c^2 = a^2 + b^2$$

donde:
- $a$ = semi-eje transverso (distancia del centro al vértice)
- $b$ = semi-eje conjugado
- $c$ = distancia del centro a cada foco.

**Observación:** Matemáticamente en la hipérbola se cumple forzosamente que $c > a$, a primera diferencia de la elipse donde siempre $c < a$.

```text
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

### 7.3 Ecuación general a canónica

**Proposición 7.1:**
Similar al caso de la elipse, podremos convertir cualquier ecuación polinómica extensa $Ax^2 + Cy^2 + Dx + Ey + F = 0$ a su forma canónica usando la **completación de cuadrados** (con la salvedad estructural obligatoria de que aquí los coeficientes cuadráticos $A$ y $C$ **deben tener signos opuestos**, lo que la distingue geométricamente).

**Ejemplo 7.2 (Completación de cuadrados en la hipérbola):**
Lleve $9x^2 - 4y^2 - 18x - 16y - 43 = 0$ a su forma canónica.

**Solución paso a paso:**
$$\begin{align}
9x^2 - 18x - 4y^2 - 16y &= 43 \\
9(x^2 - 2x) - 4(y^2 + 4y) &= 43 \\
9(x^2 - 2x + 1) - 4(y^2 + 4y + 4) &= 43 + 9 - 16 \\
9(x - 1)^2 - 4(y + 2)^2 &= 36 \\
\frac{(x - 1)^2}{4} - \frac{(y + 2)^2}{9} &= 1
\end{align}$$

- **Centro:** $(1, -2)$
- **Orientación:** Eje transverso horizontal.
- $a = 2$, $b = 3$, distancia focal $c = \sqrt{4+9} = \sqrt{13}$.

> **Casos Degenerados de la Hipérbola:**
> En sintonía con las demás cónicas, los despejes analíticos a los que se llega tras normalizar la figura a $\frac{(x-h)^2}{a^2} - \frac{(y-k)^2}{b^2} = M$, determinarán cuán integra sobrevivió su figura:
> 1. Si $M > 0$: Al acoplar el despeje a divisor único proyecta su equivalencia en una **hipérbola horizontal** real de ramas abiertas laterales.
> 2. Si $M < 0$: Proyectando equivalencia al multiplicar la igualdad por $-1$, se alteran los bloques asumiendo posición positiva sobre la variable de las yes. Determinando de esta manera una **hipérbola vertical** original de apertura superior e inferior.
> 3. Si $M = 0$: Las diferencias dictaminadas de fracciones de cuadrados colapsan a nulo por completo; en efecto visual su estructura cónica se "adhiere y aplasta" totalmente contra sus propias líneas de asintota. De resultas colateral, la degeneración deviene rígidamente en **dos rectas que se intersectan** en el centro.

**Ejemplo 7.3 (Identificando la recta secante degenerativa):**
Analice algebraicamente la figura de $x^2 - 4y^2 - 2x - 16y - 15 = 0$:

$$\begin{align}
(x^2 - 2x) - 4(y^2 + 4y) &= 15 \\
(x^2 - 2x + 1) - 4(y^2 + 4y + 4) &= 15 + 1 - 16 \\
(x - 1)^2 - 4(y + 2)^2 &= 0
\end{align}$$

Procedemos a constatar la igualdad geométrica: $(x - 1)^2 = 4(y + 2)^2 \Rightarrow (x - 1) = \pm 2(y + 2)$.
Como se ha deducido, este sistema polinómico cuadrático equivale únicamente bajo su despeje a **dos líneas rectas separadas secantes** ($x - 2y - 5 = 0$ y $x + 2y + 3 = 0$), una hipérbola estrucutral que colapsó en su centro degenerado.

### 7.4 Excentricidad

**Definición 7.2 (Excentricidad):**
La **excentricidad** de una hipérbola es:
$$e = \frac{c}{a}$$

**Propiedades:**
- $e > 1$ para toda hipérbola
- Cuanto mayor es $e$, más "abierta" es la hipérbola

**Ejemplo 7.4:**
Para $\frac{x^2}{9} - \frac{y^2}{16} = 1$:
$$e = \frac{5}{3} \approx 1.67$$

### 7.5 Propiedades de la hipérbola

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
Elimine el término mixto de $5x^2 + 8xy + 5y^2 - 9 = 0$ y clasifique la cónica resultante.

- $A = 5, B = 8, C = 5$
- $\tan(2\theta) = \frac{B}{A - C} = \frac{8}{5 - 5} = \frac{8}{0}$ → indefinido → $2\theta = 90°$ → $\theta = 45°$

Usando $\cos(45°) = \sin(45°) = \frac{\sqrt{2}}{2}$:
$$\begin{cases}
x = \frac{\sqrt{2}}{2}(x' - y') \\
y = \frac{\sqrt{2}}{2}(x' + y')
\end{cases}$$

Sustituyendo en la ecuación original:
$$5\left[\frac{\sqrt{2}}{2}(x' - y')\right]^2 + 8\left[\frac{\sqrt{2}}{2}(x' - y')\right]\left[\frac{\sqrt{2}}{2}(x' + y')\right] + 5\left[\frac{\sqrt{2}}{2}(x' + y')\right]^2 = 9$$

Desarrollando los términos al cuadrado y multiplicando:
$$\frac{5}{2}(x' - y')^2 + \frac{8}{2}(x' - y')(x' + y') + \frac{5}{2}(x' + y')^2 = 9$$
$$\frac{5}{2}(x'^2 - 2x'y' + y'^2) + 4(x'^2 - y'^2) + \frac{5}{2}(x'^2 + 2x'y' + y'^2) = 9$$

Agrupamos y factorizamos cada uno de los tipos de término respectivo ($x'^2$, $x'y'$ y $y'^2$):
- **Términos en $x'^2$:** $\frac{5}{2} + 4 + \frac{5}{2} = 5 + 4 = 9$
- **Términos en $x'y'$:** $-5 + 5 = 0$ *(¡el término mixto se elimina de manera efectiva!)*
- **Términos en $y'^2$:** $\frac{5}{2} - 4 + \frac{5}{2} = 5 - 4 = 1$

La nueva ecuación rotada simplificada se reduce limpiamente a:
$$9x'^2 + y'^2 = 9$$

Dividiendo todo entre 9 para llegar a la forma canónica base:
$$\frac{x'^2}{1} + \frac{y'^2}{9} = 1$$

**Conclusión:** Esta figura es una **elipse real** con su centro en el origen $(0,0)$. Originalmente, su eje mayor estaba inclinado $45°$ en el plano $xy$, pero bajo nuestra nueva perspectiva rotada ($x', y'$), se observa como una elipse tradicional vertical (ya que $a^2 = 9$ está bajo las ordenadas $y'$).

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

**Fin de la Clase 7**
