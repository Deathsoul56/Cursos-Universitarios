# Geometría Analítica y Funciones

## 1. El plano cartesiano $\mathbb{R}^2$

### 1.1 Coordenadas y pares ordenados

**Definición 1.1 (Plano cartesiano):**
El **plano cartesiano** $\mathbb{R}^2$ es el conjunto de todos los pares ordenados de números reales. Formalmente, corresponde al **producto cartesiano** de $\mathbb{R}$ consigo mismo:
$$\mathbb{R}^2 = \mathbb{R} \times \mathbb{R} = \{(x, y) : x \in \mathbb{R} \land y \in \mathbb{R}\}$$
Cada par ordenado $(x, y)$ representa un **punto** en el plano, donde:
- $x$ es la **abscisa** o coordenada horizontal (eje X)
- $y$ es la **ordenada** o coordenada vertical (eje Y)

**Observación importante:** El **orden importa**: $(3, 5) \neq (5, 3)$

**Ejemplo 1.1:**
Los puntos $A = (2, 3)$, $B = (-1, 4)$, $C = (-3, -2)$, $D = (4, -1)$ se representan así:
![[puntos_plano_cartesiano.png]]

**Definición 1.2 (Cuadrantes):**
El plano se divide en cuatro **cuadrantes**:
- **Cuadrante I**: $x > 0$, $y > 0$ (arriba derecha)
- **Cuadrante II**: $x < 0$, $y > 0$ (arriba izquierda)
- **Cuadrante III**: $x < 0$, $y < 0$ (abajo izquierda)
- **Cuadrante IV**: $x > 0$, $y < 0$ (abajo derecha)
![[cuadrantes_plano_cartesiano.png]]
### 1.2 Distancia entre dos puntos

**Teorema 1.1 (Fórmula de la distancia):**
La distancia $d$ entre dos puntos $P_1 = (x_1, y_1)$ y $P_2 = (x_2, y_2)$ en $\mathbb{R}^2$ es:
$$d(P_1, P_2) = \sqrt{(x_2 - x_1)^2 + (y_2 - y_1)^2}$$

**Demostración:** Se deduce del Teorema de Pitágoras aplicado al triángulo rectángulo formado por los puntos $P_1$, $P_2$ y $(x_2, y_1)$. (El teorema de Pitágoras se demostrará más adelante en la sección 3.1)

**Ejemplo 1.2:**
Calcule la distancia entre $A = (1, 2)$ y $B = (4, 6)$:

$$\begin{align}
d(A, B) &= \sqrt{(4-1)^2 + (6-2)^2} \\
&= \sqrt{3^2 + 4^2} \\
&= \sqrt{9 + 16} \\
&= \sqrt{25} = 5
\end{align}$$
![[distancia_entre_puntos.png]]
### 1.3 Punto medio

**Proposición 1.1 (Fórmula del punto medio):**
El **punto medio** $M$ del segmento que une $P_1 = (x_1, y_1)$ y $P_2 = (x_2, y_2)$ es:
$$M = \left(\frac{x_1 + x_2}{2}, \frac{y_1 + y_2}{2}\right)$$

**Ejemplo 1.3:**
El punto medio entre $A = (2, 5)$ y $B = (8, 1)$ es:
$$M = \left(\frac{2+8}{2}, \frac{5+1}{2}\right) = (5, 3)$$
![[punto_medio.png]]

---

## 2. Elementos fundamentales de geometría euclidiana

### 2.1 Los cinco postulados de Euclides

**Contexto histórico:** En los *Elementos* (c. 300 a.C.), Euclides estableció los fundamentos de la geometría mediante cinco postulados básicos.

**Los cinco postulados de Euclides:**

**Postulado 1:** Dados dos puntos distintos, existe exactamente una recta que los contiene.
**Postulado 2:** Todo segmento de recta puede extenderse indefinidamente en ambas direcciones para formar una recta.
**Postulado 3:** Dado un punto $O$ y una distancia $r$, existe un círculo con centro en $O$ y radio $r$.
**Postulado 4:** Todos los ángulos rectos son iguales entre sí (miden $90°$ o $\frac{\pi}{2}$ radianes).
**Postulado 5 (Postulado de las paralelas):** Dada una recta $L$ y un punto $P$ fuera de ella, existe **exactamente una** recta que pasa por $P$ y es paralela a $L$.

La geometría clásica que sigue estos 5 axiomas se llama **geometría euclidiana**. Existen otros tipos de geometrías que siguen los 4 primeros axiomas pero no el quinto, estas son conocidas como **geometrías no euclidianas**.
### 2.2 El problema del quinto postulado

**Observación histórica:** Durante más de 2000 años, los matemáticos intentaron demostrar que el quinto postulado era consecuencia de los otros cuatro, sin éxito.

En el siglo XIX, Gauss, Lobachevsky y Bolyai demostraron que era imposible derivarlo de los otros cuatro, y construyeron **geometrías no euclidianas** consistentes donde el quinto postulado no se cumple:

**Geometría hiperbólica:** Por un punto $P$ fuera de una recta $L$, existen **infinitas** rectas paralelas a $L$.

**Geometría elíptica:** Por un punto $P$ fuera de una recta $L$, **no existe ninguna** recta paralela a $L$ (todas se intersectan).

**Relevancia moderna:** Las geometrías no euclidianas son fundamentales en la Teoría de la Relatividad General de Einstein y en topología. Se estudiarán en cursos avanzados de Geometría Diferencial.

### 2.3 Conceptos geométricos básicos

#### 2.3.1 Conceptos primitivos

**Definición 2.1 (Punto):**
Un **punto** es el concepto geométrico más elemental y primitivo. Representa una **posición** o **ubicación** en el espacio, sin dimensión alguna (sin longitud, anchura ni altura).

**Características fundamentales:**
- **No tiene extensión:** Un punto no ocupa espacio; es adimensional (dimensión 0)
- **No tiene partes:** Es indivisible; no se puede descomponer en elementos más simples
- **Se denota:** Usualmente con letras mayúsculas: $A$, $B$, $P$, $Q$, etc.
- **Representación gráfica:** Se dibuja como un pequeño círculo o marca (●), aunque esto es solo una aproximación visual

**Observación fundamental:** En geometría euclidiana, el punto, la recta y el plano son **conceptos primitivos** (también llamados **nociones comunes** o **indefinidos**). No se definen en términos de conceptos más simples, sino que se aceptan intuitivamente y se caracterizan por las propiedades que satisfacen a través de los axiomas.

**En el plano cartesiano:** Un punto se representa mediante un **par ordenado** de números reales:
$$P = (x, y)$$
donde $x$ es la **abscisa** (coordenada horizontal) y $y$ es la **ordenada** (coordenada vertical).

**En el espacio tridimensional:** Un punto se representa mediante una **terna ordenada**:
$$P = (x, y, z)$$
**Definición 2.2 (Lugar geométrico):**
Un **lugar geométrico** es el conjunto de todos los puntos del plano (o del espacio) que satisfacen una o más condiciones o propiedades geométricas específicas.

**Formalmente:** Un lugar geométrico $L$ es:
$$L = \{P \in \text{Plano} : P \text{ cumple la propiedad } \mathcal{P}\}$$
**Interpretación:** Un lugar geométrico describe "dónde están" todos los puntos que cumplen cierta característica.

**Ejemplos fundamentales:**

1. **Recta como lugar geométrico:**
   - El conjunto de todos los puntos equidistantes de dos puntos dados forman una recta (mediatriz)
   - El conjunto de puntos alineados en una dirección específica

2. **Circunferencia como lugar geométrico:**
   - El conjunto de todos los puntos que están a una distancia fija $r$ de un punto fijo $C$ (centro)
   - Formalmente: $\{P : d(P, C) = r\}$

**Utilidad:** El concepto de lugar geométrico es fundamental en geometría analítica porque permite:
- Describir curvas y figuras mediante condiciones algebraicas
- Traducir problemas geométricos a ecuaciones
- Caracterizar objetos geométricos de forma precisa y rigurosa

**Definición 2.3 (Recta):**
Una **recta** es un conjunto infinito de puntos alineados que se extiende indefinidamente en ambas direcciones.

**Definición 2.4 (Segmento):**
Un **segmento** $\overline{AB}$ es la porción de recta limitada entre dos puntos $A$ y $B$, incluyéndolos.

**Definición 2.5 (Semirrecta o rayo):**
Una **semirrecta** es una porción de recta que comienza en un punto (origen) y se extiende indefinidamente en una dirección.
![[conceptos_geometricos.png]]
**Definición 2.6 (Ángulo):**
Un **ángulo** es la región del plano formada por dos semirrectas (lados) que parten de un punto común (vértice). Es una medida de la apertura que existe entre estas dos rectas, se puede pensar como la magnitud que se necesita girar para que una recta se convierta en otra.
Estos se pueden medir en grados sexagesimales, radianes o gradianes.
Por lo general los ángulos se denominan con letras griegas $\alpha, \beta, \gamma$ y para representar un ángulo como incógnita usualmente se usa la letra griega theta $\theta$
![[angulo_rotacion.png]]

**Clasificación de ángulos (sexagesimal):**

| Tipo | Medida |
|------|--------|
| Agudo | $0° < \alpha < 90°$ |
| Recto | $\alpha = 90°$ |
| Obtuso | $90° < \alpha < 180°$ |
| Llano | $\alpha = 180°$ |
| Completo | $\alpha = 360°$ |

**Definición 2.7 (Rectas secantes):**
Dos rectas son **secantes** si se intersectan en exactamente un punto.

**Definición 2.8 (Rectas paralelas):**
Dos rectas son **paralelas** si no tienen puntos en común (no se intersectan).

**Definición 2.9 (Rectas perpendiculares):**
Dos rectas son **perpendiculares** (u **ortogonales**) si se intersectan formando un **ángulo recto** (90°).

**Formalmente:** Dos rectas $L_1$ y $L_2$ son perpendiculares si:
$$L_1 \perp L_2 \quad \Leftrightarrow \quad L_1 \cap L_2 = \{P\} \text{ y el ángulo de intersección es } 90°$$
**Notación:** Se denota $L_1 \perp L_2$ (se lee "$L_1$ perpendicular a $L_2$").

**Propiedades:**
1. Si $L_1 \perp L_2$, entonces $L_2 \perp L_1$ (la perpendicularidad es simétrica)
2. En el plano cartesiano, dos rectas no verticales son perpendiculares si y solo si el producto de sus pendientes es $-1$ (esto se demostrará más adelante en el estudio rotaciones de funciones lineales):
   $$m_1 \cdot m_2 = -1 \quad \Leftrightarrow \quad m_2 = -\frac{1}{m_1}$$
3. Por un punto dado, existe exactamente una recta perpendicular a una recta dada

**Ejemplos en el plano cartesiano:**
- Los ejes coordenados $x$ e $y$ son perpendiculares entre sí
- Una recta con pendiente $m = 2$ es perpendicular a una recta con pendiente $m = -\frac{1}{2}$

**Definición 2.10 (Recta tangente a una curva):**
Una recta es **tangente** a una curva en un punto $P$ si toca la curva en $P$ pero no la cruza localmente.
- **Interpretación:** La tangente "roza" la curva en un solo punto sin cortarla en las cercanías.
![[tipos_rectas.png]]

---

## 3. Polígonos y figuras geométricas

### 3.0 Definición general de polígono

**Definición 3.1 (Polígono):**
Un **polígono** es una figura geométrica plana y cerrada formada por una secuencia finita de segmentos de recta consecutivos (llamados **lados**) que se unen en puntos (llamados **vértices**), de modo que:
1. Cada lado intersecta exactamente a otros dos lados (uno en cada extremo)
2. Los lados no se cruzan entre sí excepto en los vértices
3. La figura delimita una región del plano

Formalmente, un polígono con $n$ vértices $P_1, P_2, \dots, P_n$ está formado por los segmentos:
$$\overline{P_1P_2}, \overline{P_2P_3}, \dots, \overline{P_{n-1}P_n}, \overline{P_nP_1}$$

**Observaciones fundamentales:**
1. **Mínimo de lados:** Es **imposible** formar un polígono con menos de 3 lados (en geometría euclideana):
   - Con **1 lado:** Solo se obtiene un segmento (no encierra región)
   - Con **2 lados:** Dos segmentos no pueden cerrarse para formar una figura plana (necesitarían coincidir o divergir)   
1. **Triángulo como polígono elemental:** El **triángulo** (3 lados) es el polígono más simple posible y la figura geométrica fundamental. Es la única figura poligonal rígida (no se deforma sin cambiar las longitudes de sus lados).

2. **Generalización:** Es posible construir polígonos con cualquier número $n \geq 3$ de lados. La notación general es:
   - **$n$-gono:** Polígono de $n$ lados
   - Ejemplos: 3-gono (triángulo), 4-gono (cuadrilátero), 5-gono (pentágono), etc.

**Nomenclatura según el número de lados:**

| Lados ($n$) | Nombre |
|:-----------:|:-------|
| 3 | Triángulo |
| 4 | Cuadrilátero |
| 5 | Pentágono |
| 6 | Hexágono |
| 7 | Heptágono |
| 8 | Octógono |
| 9 | Eneágono |
| 10 | Decágono |
| 12 | Dodecágono |
| $n$ | $n$-gono |

**Definición 3.2 (Perímetro):**
El **perímetro** de un polígono es la suma de las longitudes de todos sus lados. Se denota comúnmente como $P$ y se mide en **unidades de longitud** (u, cm, m, etc.).

Para un polígono con lados de longitudes $\ell_1, \ell_2, \dots, \ell_n$:
$$P = \ell_1 + \ell_2 + \dots + \ell_n = \sum_{i=1}^{n} \ell_i$$
**Ejemplo:** Un triángulo con lados de 3 cm, 4 cm y 5 cm tiene perímetro $P = 3 + 4 + 5 = 12$ cm.

**Definición 3.3 (Área):**
El **área** de un polígono es la medida de la región del plano que encierra (la superficie interior delimitada por sus lados). Se denota comúnmente como $A$ y se mide en **unidades cuadradas** (u², cm², m², etc.). 

**Observación:** El área cuantifica "cuánto espacio ocupa" el polígono. Para diferentes polígonos existen fórmulas específicas de cálculo:
- Triángulo: $A = \frac{1}{2} \cdot \text{base} \cdot \text{altura}$
- Cuadrado: $A = \text{lado}^2$
- Rectángulo: $A = \text{base} \cdot \text{altura}$

**Análisis dimensional de las fórmulas de área:** El **análisis dimensional** verifica la consistencia de las fórmulas matemáticas examinando las unidades de medida. Para el área, esperamos obtener **unidades cuadradas** ($[\text{longitud}]^2$).

| Figura | Fórmula | Análisis dimensional |
|:-------|:--------|:---------------------|
| **Triángulo** | $A = \dfrac{1}{2} \cdot b \cdot h$ | $[A] = \dfrac{[\text{adim}] \cdot [\text{L}] \cdot [\text{L}]}{1} = [\text{L}^2]$ ✓ |
| **Cuadrado** | $A = \ell^2$ | $[A] = [\text{L}]^2 = [\text{L}^2]$ ✓ |
| **Rectángulo** | $A = b \cdot h$ | $[A] = [\text{L}] \cdot [\text{L}] = [\text{L}^2]$ ✓ |

**Notación:**
- $[\,\cdot\,]$ denota "dimensión de"
- $[\text{L}]$ representa dimensión de longitud (metros, centímetros, etc.)
- $[\text{L}^2]$ representa dimensión de área (metros cuadrados, cm², etc.)
- $[\text{adim}]$ representa cantidad adimensional (sin unidades, como $\frac{1}{2}$)

**Interpretación:** En todas las fórmulas, multiplicamos dos longitudes, lo que resulta en área (longitud²). Las constantes numéricas puras (como $\frac{1}{2}$) no tienen dimensión, por lo que no afectan el análisis dimensional.

**Ejemplo numérico:**
Para un triángulo con base $b = 6 \text{ cm}$ y altura $h = 4 \text{ cm}$:
$$A = \frac{1}{2} \cdot (6 \text{ cm}) \cdot (4 \text{ cm}) = \frac{1}{2} \cdot 24 \text{ cm}^2 = 12 \text{ cm}^2$$

Las unidades se combinan correctamente: $\text{cm} \times \text{cm} = \text{cm}^2$
### 3.1 Triángulos

**Definición 3.4 (Triángulo):**
Un **triángulo** es un polígono de **tres lados**, tres vértices y tres ángulos interiores. Es el polígono con el menor número de lados posible.

**Clasificación por lados:**

| Tipo | Descripción |
|------|-------------|
| **Equilátero** | Tres lados iguales |
| **Isósceles** | Dos lados iguales |
| **Escaleno** | Tres lados distintos |

**Clasificación por ángulos:**

| Tipo            | Descripción               |
| --------------- | ------------------------- |
| **Acutángulo**  | Tres ángulos agudos       |
| **Rectángulo**  | Un ángulo recto ($90°$)   |
| **Obtusángulo** | Un ángulo obtuso ($>90°$) |

![[tipos_triangulos.png]]
**Proposición 3.5 (Perímetro del triángulo):**
El perímetro de un triángulo con lados $a$, $b$ y $c$ es:
$$P = a + b + c$$
**Proposición 3.6 (Área del triángulo - Fórmula clásica):**
El área de un triángulo es:
$$A = \frac{1}{2} \cdot \text{base} \cdot \text{altura} = \frac{b \cdot h}{2}$$
donde $b$ es la longitud de la base y $h$ es la altura perpendicular desde el vértice opuesto a dicha base.

**Indicio de demostración:**
Consideremos un triángulo con base $b$ y altura $h$. Si duplicamos el triángulo y lo rotamos, podemos formar un paralelogramo:

```
Triángulo original:        Duplicado y rotado:
      *                          *-------*
     /|                         /       /
    / |h                       /   P   /
   /  |                       /       /
  *---*                      *-------*
    b                           b
```

El paralelogramo formado tiene:
- Base: $b$
- Altura: $h$
- Área del paralelogramo: $A_{\text{paral}} = b \cdot h$ (será demostrado en la próxima sección)

Como el triángulo es exactamente **la mitad** del paralelogramo:
$$A_{\triangle} = \frac{1}{2} A_{\text{paral}} = \frac{1}{2} \cdot b \cdot h = \frac{bh}{2}$$

**Teorema 3.7 (Fórmula de Herón):**
El área de un triángulo con lados $a$, $b$ y $c$ puede calcularse usando únicamente las longitudes de sus lados mediante:
$$A = \sqrt{s(s-a)(s-b)(s-c)}$$
donde $s$ es el **semiperímetro**:
$$s = \frac{a + b + c}{2} = \frac{P}{2}$$

**Demostración de la fórmula de Herón (Opcional):**

*Paso 1: Fórmula clásica con coseno*
Sea un triángulo con lados $a$, $b$, $c$. Si conocemos el ángulo $\gamma$ entre los lados $a$ y $b$, el área es:
$$A = \frac{1}{2}ab\sin(\gamma)$$
*Paso 2: Usar la ley de cosenos*
Por la ley de cosenos: $c^2 = a^2 + b^2 - 2ab\cos(\gamma)$
Despejamos: $\cos(\gamma) = \frac{a^2 + b^2 - c^2}{2ab}$

*Paso 3: Identidad trigonométrica*
Sabemos que $\sin^2(\gamma) + \cos^2(\gamma) = 1$, entonces:
$$\sin^2(\gamma) = 1 - \cos^2(\gamma) = 1 - \left(\frac{a^2 + b^2 - c^2}{2ab}\right)^2$$
Simplificando (álgebra extensa):
$$\sin^2(\gamma) = \frac{4a^2b^2 - (a^2 + b^2 - c^2)^2}{4a^2b^2}$$
Expandiendo el numerador:
$$4a^2b^2 - (a^2 + b^2 - c^2)^2 = [2ab - (a^2 + b^2 - c^2)][2ab + (a^2 + b^2 - c^2)]$$
$$= [c^2 - (a-b)^2][(a+b)^2 - c^2]$$
$$= (c-a+b)(c+a-b)(a+b-c)(a+b+c)$$
*Paso 4: Introducir el semiperímetro*
Sea $s = \frac{a+b+c}{2}$, entonces:
- $a + b + c = 2s$
- $a + b - c = 2s - 2c = 2(s-c)$
- $c + a - b = 2s - 2b = 2(s-b)$
- $c - a + b = 2s - 2a = 2(s-a)$

Sustituyendo:
$$\sin^2(\gamma) = \frac{2(s-a) \cdot 2(s-b) \cdot 2(s-c) \cdot 2s}{4a^2b^2} = \frac{16s(s-a)(s-b)(s-c)}{4a^2b^2}$$
*Paso 5: Área final*
Como $A = \frac{1}{2}ab\sin(\gamma)$, entonces:
$$A^2 = \frac{1}{4}a^2b^2\sin^2(\gamma) = \frac{1}{4}a^2b^2 \cdot \frac{16s(s-a)(s-b)(s-c)}{4a^2b^2}$$
$$A^2 = \frac{16s(s-a)(s-b)(s-c)}{16} = s(s-a)(s-b)(s-c)$$
Tomando raíz cuadrada:
$$A = \sqrt{s(s-a)(s-b)(s-c)}$$
$\square$

**Ejemplo de aplicación de Herón:**
Sea un triángulo con lados $a = 5$, $b = 6$, $c = 7$.


Semiperímetro: $s = \frac{5+6+7}{2} = 9$

Área:
$$A = \sqrt{9(9-5)(9-6)(9-7)} = \sqrt{9 \cdot 4 \cdot 3 \cdot 2} = \sqrt{216} = 6\sqrt{6} \approx 14.7 \text{ unidades}^2$$
**Teorema 3.8 (Suma de ángulos internos):**
La suma de los ángulos internos de cualquier triángulo en geometría euclidiana es:
$$\alpha + \beta + \gamma = 180°$$
**Teorema 3.9 (Teorema de Pitágoras):**
En un triángulo rectángulo con catetos $a, b$ e hipotenusa $c$:
$$c^2 = a^2 + b^2$$

**Demostración geométrica (mediante cuadrados inscritos):**

Consideremos un cuadrado grande de lado $(a + b)$, donde colocamos cuatro triángulos rectángulos idénticos con catetos $a$ y $b$, e hipotenusa $c$, de manera que sus hipotenusas formen un cuadrado interior.

**Construcción:**
![[pitagoras_demostracion.png]]

**Cálculo del área del cuadrado grande (dos formas):**

**Método 1 - Área directa:**
El área del cuadrado grande es:
$$A_{\text{grande}} = (a + b)^2 = a^2 + 2ab + b^2$$

**Método 2 - Suma de partes:**
El cuadrado grande contiene:
- **4 triángulos rectángulos**, cada uno con área $\frac{ab}{2}$
- **1 cuadrado interior** (formado por las hipotenusas) con área $c^2$

Por lo tanto:
$$A_{\text{grande}} = 4 \cdot \frac{ab}{2} + c^2 = 2ab + c^2$$
**Igualando ambas expresiones:**
$$a^2 + 2ab + b^2 = 2ab + c^2$$
Cancelando $2ab$ en ambos lados:
$$a^2 + b^2 = c^2$$
$\square$

**Interpretación geométrica:**
El teorema de Pitágoras establece que **el área del cuadrado construido sobre la hipotenusa es igual a la suma de las áreas de los cuadrados construidos sobre los catetos**.

**Observación histórica:**
Esta demostración es atribuida a varios matemáticos antiguos, incluyendo variantes chinas y árabes. Existen más de 370 demostraciones diferentes del teorema de Pitágoras registradas en la historia de las matemáticas.
### 3.2 Cuadriláteros

**Definición 3.10 (Cuadrilátero):**
Un **cuadrilátero** es un polígono de cuatro lados y cuatro vértices.

**Clasificación de cuadriláteros:**

Los cuadriláteros se clasifican según la cantidad de pares de lados paralelos que posean:

| Figura          | Lados iguales | Ángulos | Lados paralelos |
| --------------- | ------------- | ------- | --------------- |
| **Cuadrado**    | 4 lados iguales | 4 ángulos rectos (90°) | 2 pares de lados paralelos |
| **Rectángulo**  | Lados opuestos iguales | 4 ángulos rectos (90°) | 2 pares de lados paralelos |
| **Rombo**       | 4 lados iguales | Ángulos opuestos iguales | 2 pares de lados paralelos |
| **Romboide**    | Lados opuestos iguales | Ángulos opuestos iguales | 2 pares de lados paralelos |
| **Trapecio**    | Varía según tipo | Varía según tipo | 1 par de lados paralelos |
| **Trapezoide**  | Sin condición especial | Sin condición especial | 0 pares de lados paralelos |

![[cuadrilateros_tipos.png]]

**Familias de cuadriláteros:**

**1. Paralelogramos (2 pares de lados paralelos):**

Los **paralelogramos** son cuadriláteros con **dos pares de lados opuestos paralelos**. Esta familia incluye:

- **Cuadrado:** Paralelogramo con los 4 lados iguales y los 4 ángulos rectos (caso más particular)
- **Rectángulo:** Paralelogramo con 4 ángulos rectos y lados opuestos iguales
- **Rombo:** Paralelogramo con los 4 lados iguales pero ángulos no necesariamente rectos
- **Romboide:** Paralelogramo general con lados opuestos iguales y ángulos opuestos iguales (sin ángulos rectos)

**Propiedades comunes de los paralelogramos:**
- Lados opuestos paralelos e iguales
- Ángulos opuestos iguales
- Diagonales se bisecan mutuamente (se cortan en su punto medio)
- La suma de ángulos consecutivos es 180°

**2. Trapecios (1 par de lados paralelos):**

Un **trapecio** es un cuadrilátero con **exactamente un par de lados paralelos** (llamados **bases**). Los otros dos lados se llaman **laterales** o **piernas**.

**Tipos de trapecios:**

- **Trapecio rectángulo:** Tiene un ángulo recto (uno de los lados laterales es perpendicular a las bases)
- **Trapecio isósceles:** Los lados laterales tienen la misma longitud y los ángulos de la base son iguales
- **Trapecio escaleno:** Todos los lados tienen longitudes diferentes y ningún ángulo es recto

**Observación sobre el deltoide (o cometa):**

El **deltoide** (también llamado **cometa** o **papalote**) es un cuadrilátero especial que **no pertenece** a las familias anteriores:

- **Definición:** Tiene dos pares de lados **consecutivos** (adyacentes) de igual longitud
- **Propiedades:**
  - Las diagonales son perpendiculares
  - Una de las diagonales biseca a la otra
  - Tiene un eje de simetría
- **Nota:** El deltoide NO es un paralelogramo (no tiene lados paralelos en general) ni un trapecio

**Proposición 3.11 (Suma de ángulos internos):**
La suma de los ángulos internos de un cuadrilátero es:
$$\alpha + \beta + \gamma + \delta = 360°$$
**Proposición 3.12 (Perímetro del cuadrilátero):**
El perímetro de un cuadrilátero con lados $a$, $b$, $c$ y $d$ es:
$$P = a + b + c + d$$
**Proposición 3.13 (Áreas de cuadriláteros específicos):**

Las fórmulas de área varían según el tipo de cuadrilátero. A continuación se presenta una tabla con las fórmulas más importantes:

| Cuadrilátero             | Fórmula del Área                      | Variables                                              |
| :----------------------- | :------------------------------------ | :----------------------------------------------------- |
| **Cuadrado**             | $A = \ell^2$                          | $\ell$ = lado                                          |
| **Rectángulo**           | $A = b \cdot h$                       | $b$ = base, $h$ = altura                               |
| **Rombo**                | $A = \frac{D \cdot d}{2}$             | $D, d$ = diagonales                                    |
| **Paralelogramo**        | $A = b \cdot h$                       | $b$ = base, $h$ = altura perpendicular                 |
| **Trapecio**             | $A = \frac{(B + b) \cdot h}{2}$       | $B, b$ = bases paralelas, $h$ = altura                 |
| **Trapezoide**           | —                                     | (Requiere triangulación)                               |
| **Cuadrilátero general** | $A = \frac{1}{2}d_1 d_2 \sin(\theta)$ | $d_1, d_2$ = diagonales, $\theta$ = ángulo entre ellas |

**Demostraciones y comentarios:**

1. **Cuadrado:** Pensemos que tenemos un lienzo en blanco donde dibujamos líneas horizontales separadas por 1 $unidad$ y líneas verticales también separadas por 1 $unidad$. Si dibujamos un cuadrado de lado 1 el área que encierra lo vamos a definir como 1 $unidad^2$, ahora si dibujamos un cuadrado de lado igual a $\ell$ nos haremos la pregunta ¿Cuántos cuadrados de 1 $unidad^2$ encierra nuestro nuevo cuadrado?. Si contamos veremos que tendremos $l$ filas con exactamente $l$ columnas de cuadrados unitarios, por lo tanto el área de un cuadrado de lado $l$ estará dada por la expresion:
   $$A = \ell \times \ell = \ell^2$$
   ![[area_cuadrado.png]]

2. **Rectángulo:** Lo podemos pensar de la misma manera que con el cuadrado, solo que en este caso los lados no miden lo mismo, así que tendremos el producto de base por altura (lados adyacentes perpendiculares).
   $$A = base \times altura$$
3. **Rombo:** Las diagonales de un rombo son perpendiculares y se bisecan mutuamente. El rombo se puede dividir en 4 triángulos rectángulos iguales. Si las diagonales miden $D$ y $d$:
   $$A = 4 \times \frac{1}{2} \cdot \frac{D}{2} \cdot \frac{d}{2} = \frac{D \cdot d}{2}$$

4. **Paralelogramos (en general):** Similar al rectángulo, pero los ángulos no son necesariamente rectos. La altura $h$ es la distancia perpendicular entre las bases paralelas.
   $$A = b \cdot h$$

5. **Trapecio:** Se puede demostrar sumando dos triángulos o transformándolo en un paralelogramo. Si $B$ es la base mayor, $b$ la base menor y $h$ la altura:
   $$A = \frac{(B + b) \cdot h}{2}$$
   
   *Interpretación:* Es equivalente al área de un rectángulo cuya base es el promedio de las dos bases paralelas.

6. **Trapezoide:** No tiene fórmula directa. Se calcula dividiéndolo en triángulos mediante una diagonal y sumando sus áreas.

**Ejemplos numéricos:**

**Ejemplo 3.2.1 (Cuadrado):**
Un cuadrado de lado $\ell = 5$ cm tiene:
- Perímetro: $P = 4 \times 5 = 20$ cm
- Área: $A = 5^2 = 25$ cm²

**Ejemplo 3.2.2 (Rombo):**
Un rombo con diagonales $D = 8$ m y $d = 6$ m tiene:
- Área: $A = \frac{8 \times 6}{2} = 24$ m²

**Ejemplo 3.2.3 (Trapecio):**
Un trapecio con bases $B = 10$ cm, $b = 6$ cm y altura $h = 4$ cm tiene:
- Área: $A = \frac{(10 + 6) \times 4}{2} = \frac{16 \times 4}{2} = 32$ cm²

### 3.3 Polígonos regulares

**Definición 3.14 (Polígono regular):**
Un **polígono regular** es un polígono con todos sus lados y ángulos iguales.

**Ejemplos:**
- **Pentágono regular:** 5 lados iguales
- **Hexágono regular:** 6 lados iguales
- **Heptágono regular:** 7 lados
- **Octógono regular:** 8 lados
- **Decágono regular:** 10 lados

**Teorema 3.15 (Suma de ángulos internos):**
La suma de los ángulos internos de un polígono de $n$ lados es:
$$S = (n - 2) \times 180°$$

**Corolario 3.16:** Cada ángulo interno de un polígono regular de $n$ lados mide:
$$\alpha = \frac{(n-2) \times 180°}{n}$$

**Ejemplo 3.1:**
Para un hexágono regular ($n = 6$):
$$\alpha = \frac{(6-2) \times 180°}{6} = \frac{720°}{6} = 120°$$

**Definición 3.17 (Apotema):**
El **apotema** de un polígono regular es el segmento perpendicular desde el centro del polígono hasta el punto medio de cualquiera de sus lados. Se denota comúnmente como $a$.

**Interpretación geométrica:** El apotema representa la distancia más corta desde el centro del polígono hasta cualquiera de sus lados. Es análogo al radio de un círculo inscrito en el polígono.

**Relación con el radio circunscrito: (opcional)**
Para un polígono regular de $n$ lados con lado $\ell$ y radio circunscrito $R$ (distancia del centro a un vértice), el apotema $a$ se relaciona mediante:
$$a = R \cos\left(\frac{180°}{n}\right) = R \cos\left(\frac{\pi}{n}\right)$$

**Teorema 3.18 (Área de un polígono regular usando apotema):**
El área de un polígono regular de $n$ lados, con longitud de lado $\ell$ y apotema $a$, es:
$$A = \frac{P \cdot a}{2} = \frac{n \cdot \ell \cdot a}{2}$$
donde $P = n \cdot \ell$ es el perímetro del polígono.

**Demostración:**
Un polígono regular de $n$ lados puede dividirse en $n$ triángulos congruentes, cada uno con:
- Base = $\ell$ (un lado del polígono)
- Altura = $a$ (el apotema)

El área de cada triángulo es:
$$A_{\triangle} = \frac{\ell \cdot a}{2}$$

Como hay $n$ triángulos:
$$A_{\text{total}} = n \times \frac{\ell \cdot a}{2} = \frac{n \cdot \ell \cdot a}{2} = \frac{P \cdot a}{2}$$

donde $P = n \cdot \ell$ es el perímetro. $\square$

**Observación importante:** Esta fórmula es **universal** para todos los polígonos regulares, sin importar el número de lados. Solo necesitamos conocer el perímetro y el apotema.

**Ejemplo 3.1.1 (Hexágono regular):**
Un hexágono regular con lado $\ell = 6$ cm y apotema $a = 5.2$ cm tiene:
- Perímetro: $P = 6 \times 6 = 36$ cm
- Área: $A = \frac{36 \times 5.2}{2} = \frac{187.2}{2} = 93.6$ cm²

**Ejemplo 3.1.2 (Octógono regular):**
Un octógono regular con lado $\ell = 4$ m y apotema $a = 4.83$ m tiene:
- Perímetro: $P = 8 \times 4 = 32$ m
- Área: $A = \frac{32 \times 4.83}{2} = 77.28$ m²

---

**Sección 3.3.1 (Opcional): Convergencia del polígono regular al círculo**

Esta sección explora un resultado fascinante que conecta la geometría discreta (polígonos) con la geometría continua (círculos), anticipando conceptos del Cálculo Diferencial e Integral.

**Proposición 3.19 (Límite del polígono regular):**
Sea una sucesión de polígonos regulares inscrito en un círculo de radio $R$ fijo, donde el número de lados $n$ aumenta indefinidamente. Entonces:
$$\lim_{n \to \infty} P_n = \text{(polígono de } n \text{ lados)} \to \text{círculo de radio } R$$

Más formalmente:
1. El **apotema** $a_n$ converge al **radio** $R$:
   $$\lim_{n \to \infty} a_n = R$$
2. El **perímetro** $P_n$ converge a la **circunferencia** $2\pi R$:
   $$\lim_{n \to \infty} P_n = 2\pi R$$
3. El **área** $A_n$ converge al **área del círculo** $\pi R^2$:
   $$\lim_{n \to \infty} A_n = \pi R^2$$
**Intuición geométrica:**
Imagina un círculo de radio $R$. Ahora inscribe en él:
- Un triángulo equilátero ($n=3$)
- Un cuadrado ($n=4$)
- Un hexágono regular ($n=6$)
- Un dodecágono regular ($n=12$)
- Un polígono de 100 lados ($n=100$)

A medida que $n$ crece, el polígono "se pega" cada vez más al círculo. Los lados se vuelven tan pequeños que el polígono se vuelve indistinguible del círculo.

**Demostración (Convergencia del apotema):**
Para un polígono regular de $n$ lados inscrito en un círculo de radio $R$, el apotema $a_n$ se relaciona con $R$ mediante:
$$a_n = R \cos\left(\frac{\pi}{n}\right)$$
Tomando el límite cuando $n \to \infty$:
$$\lim_{n \to \infty} a_n = \lim_{n \to \infty} R \cos\left(\frac{\pi}{n}\right)$$
Cuando $n \to \infty$, tenemos que $\frac{\pi}{n} \to 0$. Como $\cos(0) = 1$:
$$\lim_{n \to \infty} a_n = R \cdot \cos(0) = R \cdot 1 = R$$
Por lo tanto, **el apotema converge al radio del círculo**. $\square$

**Demostración (Convergencia del perímetro):**

Para un polígono regular de $n$ lados inscrito en un círculo de radio $R$, cada lado tiene longitud:
$$\ell_n = 2R \sin\left(\frac{\pi}{n}\right)$$
El perímetro es:
$$P_n = n \cdot \ell_n = n \cdot 2R \sin\left(\frac{\pi}{n}\right) = 2nR \sin\left(\frac{\pi}{n}\right)$$
Tomando el límite:
$$\lim_{n \to \infty} P_n = \lim_{n \to \infty} 2nR \sin\left(\frac{\pi}{n}\right)$$
Aplicando el cambio de variable $u = \frac{\pi}{n}$ (cuando $n \to \infty$, entonces $u \to 0$):
$$\lim_{n \to \infty} 2nR \sin\left(\frac{\pi}{n}\right) = 2R \lim_{n \to \infty} \frac{\sin\left(\frac{\pi}{n}\right)}{\frac{\pi}{n}} \cdot \pi = 2R \cdot 1 \cdot \pi = 2\pi R$$
donde usamos el **límite fundamental** $\lim_{u \to 0} \frac{\sin(u)}{u} = 1$. $\square$

**Demostración (Convergencia del área):**

Usando la fórmula del área con apotema:
$$A_n = \frac{P_n \cdot a_n}{2}$$
Tomando el límite:
$$\lim_{n \to \infty} A_n = \lim_{n \to \infty} \frac{P_n \cdot a_n}{2} = \frac{1}{2} \lim_{n \to \infty} P_n \cdot \lim_{n \to \infty} a_n$$
Sustituyendo los resultados anteriores:
$$\lim_{n \to \infty} A_n = \frac{1}{2} \cdot (2\pi R) \cdot R = \pi R^2$$
que es exactamente el área del círculo. $\square$

**Interpretación histórica:**
Este resultado fue utilizado por Arquímedes (287-212 a.C.) para aproximar el valor de $\pi$. Arquímedes calculó los perímetros de polígonos regulares de 96 lados inscritos y circunscritos a un círculo de diámetro 1, obteniendo:
$$3.1408 < \pi < 3.1428$$
Este método, llamado **método de exhaución**, es un precursor del concepto moderno de límite y del Cálculo Integral.

**Tabla de convergencia numérica:**
Para un círculo de radio $R = 1$:

| $n$ (lados) | Apotema $a_n$ | Perímetro $P_n$ | Área $A_n$ | Circunferencia $2\pi$ | Área círculo $\pi$ |
| :---------: | :-----------: | :-------------: | :--------: | :-------------------: | :----------------: |
|      3      |    0.5000     |     5.1962      |   1.2990   |        6.2832         |       3.1416       |
|      6      |    0.8660     |     6.0000      |   2.5981   |        6.2832         |       3.1416       |
|     12      |    0.9659     |     6.2116      |   3.0000   |        6.2832         |       3.1416       |
|     24      |    0.9914     |     6.2652      |   3.1058   |        6.2832         |       3.1416       |
|     100     |    0.9995     |     6.2820      |   3.1411   |        6.2832         |       3.1416       |
|    1000     |    0.9999     |     6.2832      |   3.1416   |        6.2832         |       3.1416       |

Observamos que tanto el apotema como el perímetro y el área convergen rápidamente a sus valores límite.
![[convergencia_circulo.gif]]
**Conexión con el Cálculo:**
Este resultado ilustra un principio fundamental del Cálculo: **aproximar curvas mediante polígonos**. Se profundizará en estos conceptos al estudiar:
- **Límites** (Cálculo Diferencial)
- **Integrales definidas** como límites de sumas de Riemann (Cálculo Integral)
- **Longitud de arco** y **área bajo curvas**

---

### 3.4 Vértices, aristas y la fórmula de Euler

**Definición 3.20 (Poliedro):**
Un **poliedro** es un sólido tridimensional limitado por caras planas poligonales.

**Elementos de un poliedro:**
- **Vértices (V):** Puntos donde se encuentran las aristas
- **Aristas (A):** Segmentos donde se encuentran dos caras
- **Caras (C):** Polígonos que forman las superficies del poliedro

**Teorema 3.21 (Fórmula de Euler para poliedros convexos):**
Para cualquier poliedro convexo:
$$V - A + C = 2$$
**Ejemplo 3.2 (Cubo):**
Un cubo tiene:
- $V = 8$ vértices
- $A = 12$ aristas
- $C = 6$ caras

Verificación: $8 - 12 + 6 = 2$ ✓

**Ejemplo 3.3 (Tetraedro):**
Un tetraedro tiene:
- $V = 4$ vértices
- $A = 6$ aristas
- $C = 4$ caras

Verificación: $4 - 6 + 4 = 2$ ✓

---

## 4. La recta en el plano cartesiano

### 4.1 Ecuación de la recta y pendiente

#### 4.1.1 Concepto intuitivo de pendiente

**Idea intuitiva:**
La **pendiente** de una recta es una medida de su **inclinación** o **grado de elevación**. Nos indica cuánto se "eleva" o "desciende" la recta por cada unidad que avanzamos horizontalmente.

**Ejemplo intuitivo:** 
Si caminamos por una colina con pendiente 2, significa que por cada metro que avanzamos horizontalmente, ascendemos 2 metros verticalmente. Una pendiente de $-\frac{1}{2}$ significa que por cada 2 metros que avanzamos horizontalmente, descendemos 1 metro.

**Definición 4.1 (Pendiente de una recta):**
Dados dos puntos distintos $P_1 = (x_1, y_1)$ y $P_2 = (x_2, y_2)$ en una recta no vertical, la **pendiente** $m$ de la recta que pasa por estos puntos se define como:
$$m = \frac{y_2 - y_1}{x_2 - x_1} = \frac{\Delta y}{\Delta x}$$
donde:
- $\Delta y = y_2 - y_1$ es el **cambio vertical** (variación en $y$)
- $\Delta x = x_2 - x_1$ es el **cambio horizontal** (variación en $x$)

**Observación fundamental:** La pendiente es independiente de los puntos elegidos sobre la recta. Si tomamos otros dos puntos $P_3$ y $P_4$ sobre la misma recta, obtendremos el mismo valor de $m$.

**Interpretación geométrica:**
La pendiente representa la **razón de cambio** de la coordenada $y$ respecto a la coordenada $x$. Es la **tangente del ángulo** $\theta$ que forma la recta con el eje $x$ positivo:
$$m = \tan(\theta)$$

**Clasificación de rectas según su pendiente:**

| Pendiente      | Descripción                        | Comportamiento                              | Gráfica |
| -------------- | ---------------------------------- | ------------------------------------------- | ------- |
| $m > 0$        | Pendiente positiva                 | Recta **creciente** (sube de izq. a der.)   | /       |
| $m = 0$        | Pendiente cero                     | Recta **horizontal**                        | —       |
| $m < 0$        | Pendiente negativa                 | Recta **decreciente** (baja de izq. a der.) | \       |
| $m$ indefinida | División por cero ($\Delta x = 0$) | Recta **vertical**                          | \|      |

**Ejemplo 4.1 (Cálculo de pendiente):**
Encuentre la pendiente de la recta que pasa por $A = (2, 3)$ y $B = (6, 11)$:

$$m = \frac{11 - 3}{6 - 2} = \frac{8}{4} = 2$$

**Interpretación:** Por cada unidad que avanzamos en $x$, $y$ aumenta en 2 unidades.

**Ejemplo 4.2 (Pendiente negativa):**
Para $P = (1, 5)$ y $Q = (4, -1)$:

$$m = \frac{-1 - 5}{4 - 1} = \frac{-6}{3} = -2$$

**Interpretación:** Por cada unidad que avanzamos en $x$, $y$ disminuye en 2 unidades.

**Ejemplo 4.3 (Recta horizontal):**
Para $R = (-2, 4)$ y $S = (3, 4)$:

$$m = \frac{4 - 4}{3 - (-2)} = \frac{0}{5} = 0$$

La recta es horizontal (paralela al eje $x$).

**Ejemplo 4.4 (Recta vertical):**
Para $M = (2, 1)$ y $N = (2, 5)$:

$$m = \frac{5 - 1}{2 - 2} = \frac{4}{0}$$

La pendiente **no está definida** (recta vertical, paralela al eje $y$).

### 4.2 Ecuaciones de la recta

#### 4.2.1 Forma punto-pendiente

**Teorema 4.1 (Ecuación punto-pendiente):**
Este ecuaciones revise su nombre porque podemos definir algebraicamente una recta si conocemos un punto al que le pertenece y la pendiente de dicha recta.
La ecuación de la recta con pendiente $m$ que pasa por el punto $(x_0, y_0)$ es:
$$y - y_0 = m(x - x_0)$$

**Demostración:**
Sea $P_0 = (x_0, y_0)$ un punto fijo sobre la recta, y sea $P = (x, y)$ un punto genérico (variable) sobre la misma recta. Por definición de pendiente:
$$m = \frac{y - y_0}{x - x_0}$$
Multiplicando ambos lados por $(x - x_0)$:
$$m(x - x_0) = y - y_0$$
$$y - y_0 = m(x - x_0)$$
$\square$

**Ejemplo 4.5:**
Encuentre la ecuación de la recta con pendiente $m = 3$ que pasa por el punto $(1, 2)$:

$$\begin{align}
y - 2 &= 3(x - 1) \\
y - 2 &= 3x - 3 \\
y &= 3x - 1
\end{align}$$

**Ejemplo 4.6:**
Encuentre la ecuación de la recta que pasa por los puntos $A = (2, 5)$ y $B = (4, 9)$:

*Paso 1: Calcular la pendiente*
$$m = \frac{9 - 5}{4 - 2} = \frac{4}{2} = 2$$

*Paso 2: Usar punto-pendiente con uno de los puntos (usemos $A$)*
$$y - 5 = 2(x - 2)$$
$$y - 5 = 2x - 4$$
$$y = 2x + 1$$

**Verificación:** Podemos verificar que ambos puntos satisfacen la ecuación:
- Para $A = (2, 5)$: $y = 2(2) + 1 = 5$ ✓
- Para $B = (4, 9)$: $y = 2(4) + 1 = 9$ ✓

#### 4.2.2 Forma pendiente-ordenada

**Definición 4.2 (Forma pendiente-ordenada o explícita):**
La **forma pendiente-ordenada** de la ecuación de una recta es:
$$y = mx + b$$
donde:
- $m$ es la **pendiente**
- $b$ es la **ordenada al origen** (intersección con el eje $y$)

**Observación:** Esta forma se obtiene directamente de la forma punto-pendiente cuando el punto conocido es $(0, b)$:
$$y - b = m(x - 0) \quad \Rightarrow \quad y = mx + b$$

**Interpretación geométrica:**
- El coeficiente $m$ determina la **inclinación** de la recta
- El término $b$ indica dónde la recta **cruza el eje $y$** (cuando $x = 0$)

**Ejemplo 4.7:**
La recta $y = 2x + 3$ tiene:
- Pendiente: $m = 2$
- Ordenada al origen: $b = 3$ (cruza el eje $y$ en el punto $(0, 3)$)

**Ejemplo 4.8:**
Encuentre la ecuación de la recta con pendiente $m = -\frac{1}{2}$ que pasa por el punto $(4, 1)$:

*Método 1: Punto-pendiente y luego despejar*
$$y - 1 = -\frac{1}{2}(x - 4)$$
$$y - 1 = -\frac{1}{2}x + 2$$
$$y = -\frac{1}{2}x + 3$$

*Método 2: Sustituir el punto en $y = mx + b$ para hallar $b$*
$$1 = -\frac{1}{2}(4) + b$$
$$1 = -2 + b$$
$$b = 3$$

Por lo tanto: $y = -\frac{1}{2}x + 3$

#### 4.2.3 Forma general de la ecuación de la recta

**Definición 4.3 (Ecuación general de la recta):**
La **forma general** o **implícita** de la ecuación de una recta en el plano es:
$$Ax + By + C = 0$$
donde $A, B, C \in \mathbb{R}$ y $(A, B) \neq (0, 0)$ (al menos uno de $A$ o $B$ debe ser distinto de cero).

**Proposición 4.1 (Equivalencia entre formas):**
Toda ecuación lineal en forma general con $B \neq 0$ puede expresarse en forma pendiente-ordenada, y viceversa.

**Demostración:**
Si $B \neq 0$, despejamos $y$ de la forma general:
$$Ax + By + C = 0$$
$$By = -Ax - C$$
$$y = -\frac{A}{B}x - \frac{C}{B}$$

Identificando con $y = mx + b$:
- Pendiente: $m = -\frac{A}{B}$
- Ordenada: $b = -\frac{C}{B}$

Recíprocamente, dada $y = mx + b$, podemos escribir:
$$y - mx - b = 0$$
$$-mx + y - b = 0$$

Multiplicando por $-1$: $mx - y + b = 0$

Identificando: $A = m$, $B = -1$, $C = b$. $\square$

**Casos especiales:**

1. **Recta vertical ($B = 0$):** La ecuación $Ax + C = 0$ representa una recta vertical $x = -\frac{C}{A} = k$ (constante).
   - **No es función** (no pasa la prueba de la recta vertical)
   - Pendiente indefinida
   - Todos los puntos tienen la misma abscisa $x = k$

2. **Recta horizontal ($A = 0$):** La ecuación $By + C = 0$ representa una recta horizontal $y = -\frac{C}{B} = k$ (constante).
   - **Es una función constante** $f(x) = k$
   - Pendiente $m = 0$
   - Todos los puntos tienen la misma ordenada $y = k$

**Ejemplo 4.9 (Conversión de forma general a pendiente-ordenada):**
Convierta $2x + 3y - 6 = 0$ a la forma $y = mx + b$:

$$\begin{align}
2x + 3y - 6 &= 0 \\
3y &= -2x + 6 \\
y &= -\frac{2}{3}x + 2
\end{align}$$

Pendiente: $m = -\frac{2}{3}$, Ordenada: $b = 2$

**Ejemplo 4.10 (Conversión de pendiente-ordenada a forma general):**
Exprese $y = \frac{3}{4}x - 5$ en forma general:

$$\begin{align}
y &= \frac{3}{4}x - 5 \\
4y &= 3x - 20 \quad \text{(multiplicar por 4)} \\
-3x + 4y + 20 &= 0 \\
3x - 4y - 20 &= 0 \quad \text{(multiplicar por -1)}
\end{align}$$

Forma general: $3x - 4y - 20 = 0$

### 4.3 Intersecciones con los ejes

**Definición 4.4 (Ordenada al origen):**
La **ordenada al origen** (o **intersección con el eje $y$**) es el punto donde la recta corta el eje vertical. Se obtiene evaluando $x = 0$:
$$y = m \cdot 0 + b = b$$
**Punto de intersección con eje $y$:** $(0, b)$

**Definición 4.5 (Abscisa al origen):**
La **abscisa al origen** (o **intersección con el eje $x$**) es el punto donde la recta corta el eje horizontal. Se obtiene resolviendo $y = 0$:

Para la ecuación $y = mx + b$:
$$0 = mx + b$$
$$mx = -b$$
$$x = -\frac{b}{m} \quad \text{(si } m \neq 0\text{)}$$

**Punto de intersección con eje $x$:** $\left(-\frac{b}{m}, 0\right)$

**Observación:** La abscisa al origen también se llama **raíz** o **cero** de la función lineal.

**Ejemplo 4.11:**
Para la recta $y = 2x - 6$:

*Intersección con eje $y$:* 
$$x = 0 \Rightarrow y = 2 \cdot 0 - 6 = -6$$
Punto: $(0, -6)$

*Intersección con eje $x$:*
$$y = 0 \Rightarrow 0 = 2x - 6 \Rightarrow x = 3$$
Punto: $(3, 0)$

**Ejemplo 4.12 (Usando forma general):**
Para $3x - 2y + 12 = 0$:

*Intersección con eje $y$:* (hacer $x = 0$)
$$3(0) - 2y + 12 = 0$$
$$-2y + 12 = 0$$
$$y = 6$$
Punto: $(0, 6)$

*Intersección con eje $x$:* (hacer $y = 0$)
$$3x - 2(0) + 12 = 0$$
$$3x + 12 = 0$$
$$x = -4$$
Punto: $(-4, 0)$

### 4.4 Rectas paralelas y perpendiculares

#### 4.4.1 Rectas paralelas

**Definición 4.6 (Rectas paralelas):**
Dos rectas son **paralelas** si no se intersectan en ningún punto del plano (mantienen siempre la misma distancia entre sí).

**Teorema 4.2 (Condición de paralelismo):**
Dos rectas no verticales con pendientes $m_1$ y $m_2$ son **paralelas** si y solo si tienen la **misma pendiente**:
$$L_1 \parallel L_2 \quad \Leftrightarrow \quad m_1 = m_2$$

**Observación importante:** Las rectas paralelas con la misma pendiente pero diferente ordenada al origen son **rectas paralelas distintas**. Si además tienen la misma ordenada, son la **misma recta**.

**Ejemplo 4.13:**
Las rectas $y = 3x + 2$ y $y = 3x - 5$ son **paralelas** porque ambas tienen pendiente $m = 3$.
- Nunca se intersectan
- Tienen diferente ordenada al origen ($b_1 = 2$ y $b_2 = -5$)

**Ejemplo 4.14:**
Encuentre la ecuación de la recta que pasa por $(2, 5)$ y es paralela a $y = -\frac{1}{2}x + 3$:

La recta buscada debe tener la misma pendiente: $m = -\frac{1}{2}$

Usando punto-pendiente:
$$y - 5 = -\frac{1}{2}(x - 2)$$
$$y - 5 = -\frac{1}{2}x + 1$$
$$y = -\frac{1}{2}x + 6$$

#### 4.4.2 Rectas perpendiculares

**Definición 4.7 (Rectas perpendiculares):**
Dos rectas son **perpendiculares** (u **ortogonales**) si se intersectan formando un **ángulo recto** ($90°$ o $\frac{\pi}{2}$ radianes).

**Notación:** $L_1 \perp L_2$ (se lee "$L_1$ perpendicular a $L_2$")

**Teorema 4.3 (Condición de perpendicularidad):**
Dos rectas no verticales con pendientes $m_1$ y $m_2$ son **perpendiculares** si y solo si el producto de sus pendientes es $-1$:
$$L_1 \perp L_2 \quad \Leftrightarrow \quad m_1 \cdot m_2 = -1$$

Equivalentemente: $m_2 = -\frac{1}{m_1}$ (las pendientes son **recíprocas opuestas**)

**Demostración (Idea geométrica):**
Consideremos dos rectas con pendientes $m_1 = \tan(\theta_1)$ y $m_2 = \tan(\theta_2)$, donde $\theta_1$ y $\theta_2$ son los ángulos que forman con el eje $x$ positivo.

Para que sean perpendiculares, el ángulo entre ellas debe ser $90°$, lo que implica:
$$\theta_2 = \theta_1 + 90°$$

Usando la identidad trigonométrica:
$$\tan(\theta_1 + 90°) = -\cot(\theta_1) = -\frac{1}{\tan(\theta_1)}$$

Por lo tanto:
$$m_2 = \tan(\theta_2) = -\frac{1}{\tan(\theta_1)} = -\frac{1}{m_1}$$

Multiplicando ambos lados por $m_1$:
$$m_1 \cdot m_2 = -1$$
$\square$

**Ejemplo 4.15:**
Las rectas $y = 2x + 1$ y $y = -\frac{1}{2}x + 3$ son **perpendiculares** porque:
$$m_1 \cdot m_2 = 2 \cdot \left(-\frac{1}{2}\right) = -1$$

**Ejemplo 4.16:**
Encuentre la ecuación de la recta que pasa por $(-1, 4)$ y es perpendicular a $y = 3x - 2$:

La pendiente de la recta dada es $m_1 = 3$. 
La pendiente de la recta perpendicular es:
$$m_2 = -\frac{1}{m_1} = -\frac{1}{3}$$

Usando punto-pendiente:
$$y - 4 = -\frac{1}{3}(x - (-1))$$
$$y - 4 = -\frac{1}{3}(x + 1)$$
$$y - 4 = -\frac{1}{3}x - \frac{1}{3}$$
$$y = -\frac{1}{3}x + \frac{11}{3}$$

**Casos especiales:**
- Una recta **horizontal** ($m = 0$) es perpendicular a una recta **vertical** (pendiente indefinida)
- Los ejes coordenados $x$ e $y$ son perpendiculares entre sí

### 4.5 Intersección de dos rectas y sistemas lineales

**Definición 4.8 (Punto de intersección):**
El **punto de intersección** de dos rectas es el punto que pertenece simultáneamente a ambas rectas.

**Teorema 4.4 (Intersección y sistemas de ecuaciones):**
El punto de intersección de dos rectas dadas por:
$$\begin{cases}
L_1: A_1x + B_1y + C_1 = 0 \\
L_2: A_2x + B_2y + C_2 = 0
\end{cases}$$
es la solución del **sistema de ecuaciones lineales** $2 \times 2$.

**Casos posibles:**

| Caso | Condición | Descripción | Solución |
|:----:|:----------|:------------|:---------|
| **1** | $m_1 \neq m_2$ | Rectas **secantes** (se cortan) | **Única** solución |
| **2** | $m_1 = m_2$, $b_1 \neq b_2$ | Rectas **paralelas** distintas | **Sin** solución |
| **3** | $m_1 = m_2$, $b_1 = b_2$ | Rectas **coincidentes** (misma recta) | **Infinitas** soluciones |

**Método algebraico (igualación):**
Para encontrar la intersección de dos rectas en forma $y = m_1x + b_1$ y $y = m_2x + b_2$:

*Paso 1:* Igualar las ecuaciones
$$m_1x + b_1 = m_2x + b_2$$

*Paso 2:* Despejar $x$
$$x = \frac{b_2 - b_1}{m_1 - m_2} \quad \text{(si } m_1 \neq m_2\text{)}$$

*Paso 3:* Sustituir en cualquiera de las ecuaciones originales para hallar $y$

**Ejemplo 4.17 (Rectas secantes):**
Encuentre la intersección de $y = 2x + 1$ y $y = -x + 7$:

*Igualando:*
$$2x + 1 = -x + 7$$
$$3x = 6$$
$$x = 2$$

*Sustituyendo en la primera ecuación:*
$$y = 2(2) + 1 = 5$$

**Punto de intersección:** $(2, 5)$

**Verificación:**
- En $y = 2x + 1$: $y = 2(2) + 1 = 5$ ✓
- En $y = -x + 7$: $y = -(2) + 7 = 5$ ✓

**Ejemplo 4.18 (Rectas paralelas):**
Analice el sistema:
$$\begin{cases}
y = 3x + 2 \\
y = 3x - 5
\end{cases}$$

Ambas tienen pendiente $m = 3$ pero diferente ordenada ($b_1 = 2 \neq b_2 = -5$).
Son **paralelas** → **No se intersectan** → Sistema **sin solución**.

**Ejemplo 4.19 (Sistema $2 \times 2$ en forma general):**
Resuelva:
$$\begin{cases}
2x + 3y = 13 \\
x - y = 1
\end{cases}$$

*Método de sustitución:*
De la segunda ecuación: $x = y + 1$

Sustituyendo en la primera:
$$2(y + 1) + 3y = 13$$
$$2y + 2 + 3y = 13$$
$$5y = 11$$
$$y = \frac{11}{5}$$

Entonces: $x = \frac{11}{5} + 1 = \frac{16}{5}$$

**Solución:** $\left(\frac{16}{5}, \frac{11}{5}\right)$

### 4.6 Distancia de un punto a una recta (Opcional)

**Teorema 4.5 (Fórmula de la distancia punto-recta):**
La distancia mínima $d$ desde un punto $P = (x_0, y_0)$ hasta una recta $L: Ax + By + C = 0$ está dada por:
$$d = \frac{|Ax_0 + By_0 + C|}{\sqrt{A^2 + B^2}}$$

**Interpretación geométrica:** Esta fórmula calcula la longitud del segmento perpendicular desde el punto hasta la recta, que es la **distancia más corta** posible.

**Demostración:**

La demostración se basa en encontrar el pie de la perpendicular desde el punto $P$ hasta la recta $L$, y luego calcular la distancia entre estos dos puntos.

**Paso 1: Encontrar la recta perpendicular que pasa por $P$.**

Sea $L: Ax + By + C = 0$ la recta dada. Si $B \neq 0$, podemos escribir:
$$y = -\frac{A}{B}x - \frac{C}{B}$$
por lo que la pendiente de $L$ es $m_L = -\frac{A}{B}$.

La recta perpendicular $L_\perp$ que pasa por $P = (x_0, y_0)$ tiene pendiente:
$$m_\perp = -\frac{1}{m_L} = -\frac{1}{-A/B} = \frac{B}{A}$$

La ecuación de $L_\perp$ en forma punto-pendiente es:
$$y - y_0 = \frac{B}{A}(x - x_0)$$

Multiplicando por $A$:
$$A(y - y_0) = B(x - x_0)$$
$$Ay - Ay_0 = Bx - Bx_0$$
$$Bx - Ay + (Ay_0 - Bx_0) = 0$$

**Paso 2: Encontrar el punto de intersección $Q$ entre $L$ y $L_\perp$.**

Debemos resolver el sistema:
$$\begin{cases}
Ax + By + C = 0 & \text{(recta original)} \\
Bx - Ay + (Ay_0 - Bx_0) = 0 & \text{(perpendicular)}
\end{cases}$$

Multiplicando la primera ecuación por $A$: $A^2x + ABy + AC = 0$

Multiplicando la segunda ecuación por $B$: $B^2x - ABy + B(Ay_0 - Bx_0) = 0$

Sumando ambas ecuaciones:
$$A^2x + B^2x + AC + BAy_0 - B^2x_0 = 0$$
$$(A^2 + B^2)x = B^2x_0 - BAy_0 - AC$$
$$x = \frac{B^2x_0 - BAy_0 - AC}{A^2 + B^2} = \frac{B(Bx_0 - Ay_0) - AC}{A^2 + B^2}$$

De manera similar (o sustituyendo en una de las ecuaciones), obtenemos:
$$y = \frac{A^2y_0 - ABx_0 - BC}{A^2 + B^2} = \frac{A(Ay_0 - Bx_0) - BC}{A^2 + B^2}$$

Por lo tanto, el pie de la perpendicular es:
$$Q = \left(\frac{B(Bx_0 - Ay_0) - AC}{A^2 + B^2}, \frac{A(Ay_0 - Bx_0) - BC}{A^2 + B^2}\right)$$

**Paso 3: Calcular la distancia $d = |PQ|$.**

Usando la fórmula de distancia entre dos puntos:
$$d = \sqrt{(x - x_0)^2 + (y - y_0)^2}$$

$$d = \sqrt{\left(\frac{B(Bx_0 - Ay_0) - AC}{A^2 + B^2} - x_0\right)^2 + \left(\frac{A(Ay_0 - Bx_0) - BC}{A^2 + B^2} - y_0\right)^2}$$

Simplificando la primera componente:
$$x - x_0 = \frac{B(Bx_0 - Ay_0) - AC - x_0(A^2 + B^2)}{A^2 + B^2}$$
$$= \frac{B^2x_0 - BAy_0 - AC - A^2x_0 - B^2x_0}{A^2 + B^2}$$
$$= \frac{-A^2x_0 - BAy_0 - AC}{A^2 + B^2} = \frac{-A(Ax_0 + By_0 + C)}{A^2 + B^2}$$

Simplificando la segunda componente:
$$y - y_0 = \frac{A(Ay_0 - Bx_0) - BC - y_0(A^2 + B^2)}{A^2 + B^2}$$
$$= \frac{A^2y_0 - ABx_0 - BC - A^2y_0 - B^2y_0}{A^2 + B^2}$$
$$= \frac{-ABx_0 - B^2y_0 - BC}{A^2 + B^2} = \frac{-B(Ax_0 + By_0 + C)}{A^2 + B^2}$$

Por lo tanto:
$$d = \sqrt{\left(\frac{-A(Ax_0 + By_0 + C)}{A^2 + B^2}\right)^2 + \left(\frac{-B(Ax_0 + By_0 + C)}{A^2 + B^2}\right)^2}$$

$$d = \sqrt{\frac{A^2(Ax_0 + By_0 + C)^2 + B^2(Ax_0 + By_0 + C)^2}{(A^2 + B^2)^2}}$$

$$d = \sqrt{\frac{(A^2 + B^2)(Ax_0 + By_0 + C)^2}{(A^2 + B^2)^2}}$$

$$d = \sqrt{\frac{(Ax_0 + By_0 + C)^2}{A^2 + B^2}}$$

$$d = \frac{|Ax_0 + By_0 + C|}{\sqrt{A^2 + B^2}}$$ $\square$

**Caso especial ($B = 0$):** Si la recta es vertical ($Ax + C = 0$ o $x = -C/A$), la distancia es simplemente:
$$d = |x_0 - (-C/A)| = |x_0 + C/A| = \frac{|Ax_0 + C|}{|A|} = \frac{|Ax_0 + C|}{\sqrt{A^2}}$$
que coincide con la fórmula general (tomando $B = 0$).

**Observación:** El numerador $|Ax_0 + By_0 + C|$ representa el valor absoluto de la evaluación de la expresión de la recta en el punto $P$. El denominador $\sqrt{A^2 + B^2}$ es la norma del vector normal a la recta, $\vec{n} = (A, B)$.

---

**Ejemplo 4.20:**
Calcule la distancia desde el punto $P = (3, 1)$ hasta la recta $L: 4x - 3y - 10 = 0$:

$$d = \frac{|4(3) - 3(1) - 10|}{\sqrt{4^2 + (-3)^2}}$$
$$d = \frac{|12 - 3 - 10|}{\sqrt{16 + 9}}$$
$$d = \frac{|-1|}{\sqrt{25}}$$
$$d = \frac{1}{5}$$

**Ejemplo 4.21:**
Encuentre la distancia desde el origen $(0, 0)$ hasta la recta $3x + 4y - 20 = 0$:

$$d = \frac{|3(0) + 4(0) - 20|}{\sqrt{3^2 + 4^2}}$$
$$d = \frac{|-20|}{\sqrt{9 + 16}}$$
$$d = \frac{20}{\sqrt{25}}$$
$$d = \frac{20}{5} = 4$$

---

## 5. Ejercicios propuestos

### 5.1 Plano cartesiano y distancias

1. Calcule la distancia entre los puntos $A = (-3, 4)$ y $B = (5, -2)$

2. Encuentre el punto medio del segmento que une $P = (7, -1)$ y $Q = (-3, 5)$

3. Determine si el triángulo con vértices $A = (0, 0)$, $B = (3, 4)$, $C = (6, 0)$ es rectángulo

4. Calcule el perímetro del triángulo del ejercicio anterior

5. Encuentre las coordenadas del cuarto vértice $D$ del paralelogramo $ABCD$ si $A = (1, 2)$, $B = (4, 3)$, $C = (5, 6)$

### 5.2 Polígonos y áreas

6. Calcule el área de un triángulo con lados $a = 7$, $b = 8$, $c = 9$ usando la fórmula de Herón

7. Un hexágono regular tiene lado $\ell = 5$ cm y apotema $a = 4.33$ cm. Calcule su área

8. Verifique la fórmula de Euler para un octaedro regular (8 caras, 6 vértices, 12 aristas)

### 5.3 La recta en el plano

9. Encuentre la pendiente de la recta que pasa por los puntos $A = (2, 5)$ y $B = (6, 13)$

10. Determine la ecuación de la recta con pendiente $m = -3$ que pasa por el punto $(-1, 4)$

11. Escriba la ecuación $3x + 2y - 6 = 0$ en la forma $y = mx + b$

12. Encuentre las intersecciones con los ejes de la recta $y = 2x - 8$

13. Determine si las rectas $y = \frac{1}{2}x + 3$ y $y = \frac{1}{2}x - 5$ son paralelas, perpendiculares o ninguna

14. Encuentre la ecuación de la recta perpendicular a $y = 4x - 2$ que pasa por el origen $(0, 0)$

15. Encuentre la ecuación de la recta que pasa por los puntos $P = (1, 3)$ y $Q = (4, 9)$

16. Determine el punto de intersección de las rectas $y = 3x + 2$ y $y = -2x + 12$

17. Encuentre la ecuación de la recta paralela a $2x - 3y + 6 = 0$ que pasa por el punto $(3, -1)$

18. Calcule la distancia desde el punto $(2, 3)$ hasta la recta $3x - 4y + 5 = 0$

---

**Fin de la Clase 4: Geometría Analítica**

