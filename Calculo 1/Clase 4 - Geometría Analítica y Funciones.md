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

**Demostración:** Se deduce del Teorema de Pitágoras aplicado al triángulo rectángulo formado por los puntos $P_1$, $P_2$ y $(x_2, y_1)$. (en breve se demostrara el teorema de Pitágoras)

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

La geometría clásica que siguen estos 5 axiomas se llama **geometría euclidiana**. Existen otros tipos de geometrías que siguen los 4 primeros axiomas pero no el quito, estas son conocidas como **geometrías no euclidianas**.
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
Un **ángulo** es la región del plano formada por dos semirrectas (lados) que parten de un punto común (vértice). Es una medida de la apertura que existen entre estas 2 reglas, lo puedo pensar como la magnitud que necesito girar para que una recta se convierta en otra.
Estos se pueden medir en grados sexagesimal, radianes o gradianes.
Por lo general los ángulos de denominaran con letras griegas $\alpha, \beta, \gamma$ y para presentar un ángulo como incógnita por lo usual se usa la letra griega theta $\theta$
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
2. En el plano cartesiano, dos rectas no verticales son perpendiculares si y solo si el producto de sus pendientes es $-1$ (esto se demostrara en próximas clases):
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

**Definición 3.0 (Polígono):**
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

**Definición 3.0.1 (Perímetro):**
El **perímetro** de un polígono es la suma de las longitudes de todos sus lados. Se denota comúnmente como $P$ y se mide en **unidades de longitud** (u, cm, m, etc.).

Para un polígono con lados de longitudes $\ell_1, \ell_2, \dots, \ell_n$:
$$P = \ell_1 + \ell_2 + \dots + \ell_n = \sum_{i=1}^{n} \ell_i$$
**Ejemplo:** Un triángulo con lados de 3 cm, 4 cm y 5 cm tiene perímetro $P = 3 + 4 + 5 = 12$ cm.

**Definición 3.0.2 (Área):**
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

**Definición 3.1 (Triángulo):**
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
**Proposición 3.1.1 (Perímetro del triángulo):**
El perímetro de un triángulo con lados $a$, $b$ y $c$ es:
$$P = a + b + c$$
**Proposición 3.1.2 (Área del triángulo - Fórmula clásica):**
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

**Teorema 3.3 (Fórmula de Herón):**
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
**Teorema 3.1 (Suma de ángulos internos):**
La suma de los ángulos internos de cualquier triángulo en geometría euclidiana es:
$$\alpha + \beta + \gamma = 180°$$
**Teorema 3.2 (Teorema de Pitágoras):**
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

**Definición 3.2 (Cuadrilátero):**
Un **cuadrilátero** es un polígono de cuatro lados y cuatro vértices.

**Tipos principales:**

| Figura            | Descripción                                    |
| ----------------- | ---------------------------------------------- |
| **Cuadrado**      | Cuatro lados iguales, cuatro ángulos rectos    |
| **Rectángulo**    | Lados opuestos iguales, cuatro ángulos rectos  |
| **Rombo**         | Cuatro lados iguales, ángulos opuestos iguales |
| **Paralelogramo** | Lados opuestos paralelos e iguales             |
| **Trapecio**      | Exactamente un par de lados paralelos          |
| **Deltoide**      | Dos pares de lados adyacentes iguales          |
| **Trapezoide**    | Ningún par de lados paralelos                  |
![[cuadrilateros_tipos.png]]

**Proposición 3.2.1 (Suma de ángulos internos):**
La suma de los ángulos internos de un cuadrilátero es:
$$\alpha + \beta + \gamma + \delta = 360°$$
**Proposición 3.2.2 (Perímetro del cuadrilátero):**
El perímetro de un cuadrilátero con lados $a$, $b$, $c$ y $d$ es:
$$P = a + b + c + d$$
**Proposición 3.2.3 (Áreas de cuadriláteros específicos):**

Las fórmulas de área varían según el tipo de cuadrilátero. A continuación se presenta una tabla con las fórmulas más importantes:

| Cuadrilátero | Fórmula del Área | Variables |
|:-------------|:-----------------|:----------|
| **Cuadrado** | $A = \ell^2$ | $\ell$ = lado |
| **Rectángulo** | $A = b \cdot h$ | $b$ = base, $h$ = altura |
| **Rombo** | $A = \frac{D \cdot d}{2}$ | $D, d$ = diagonales |
| **Paralelogramo** | $A = b \cdot h$ | $b$ = base, $h$ = altura perpendicular |
| **Trapecio** | $A = \frac{(B + b) \cdot h}{2}$ | $B, b$ = bases paralelas, $h$ = altura |
| **Trapezoide** | — | (Requiere triangulación) |
| **Cuadrilátero general** | $A = \frac{1}{2}d_1 d_2 \sin(\theta)$ | $d_1, d_2$ = diagonales, $\theta$ = ángulo entre ellas |

**Demostraciones y comentarios:**

1. **Cuadrado:** Pensemos que tenemos un lienzo en blanco donde dibujamos líneas horizontales separadas por 1 $unidad$ y líneas verticales también separadas por 1 $unidad$. Si dibujamos un cuadrado de lado 1 el área que encierra lo vamos a definir como 1 $unidad^2$, ahora si dibujamos un cuadrado de lado igual a $\ell$ nos haremos la pregunta ¿Cuántos cuadrados de 1 $unidad^2$ encierra nuestro nuevo cuadrado?. Si contamos veremos que tendremos $l$ filas con exactamente $l$ columnas de cuadrados unitarios, por lo tanto el área de un cuadrado de lado $l$ estará dada por la expresion:
   $$A = \ell \times \ell = \ell^2$$
   ![[area_cuadrado.png]]

2. **Rectángulo:** Lo podemos pensar de la misma manera que con el cuadrado, solo que en este caso los lados no miden lo mismo, así que tendremos el producto de base por altura (lados adyacentes perpendiculares).
   $$A = base \times altura$$
3. **Rombo:** Las diagonales de un rombo son perpendiculares y se bisecan mutuamente. El rombo se puede dividir en 4 triángulos rectángulos iguales. Si las diagonales miden $D$ y $d$:
   $$A = 4 \times \frac{1}{2} \cdot \frac{D}{2} \cdot \frac{d}{2} = \frac{D \cdot d}{2}$$

4. **Paralelogramo:** Similar al rectángulo, pero los ángulos no son necesariamente rectos. La altura $h$ es la distancia perpendicular entre las bases paralelas.
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

**Definición 3.3 (Polígono regular):**
Un **polígono regular** es un polígono con todos sus lados y ángulos iguales.

**Ejemplos:**
- **Pentágono regular:** 5 lados iguales
- **Hexágono regular:** 6 lados iguales
- **Heptágono regular:** 7 lados
- **Octógono regular:** 8 lados
- **Decágono regular:** 10 lados

**Teorema 3.3 (Suma de ángulos internos):**
La suma de los ángulos internos de un polígono de $n$ lados es:
$$S = (n - 2) \times 180°$$

**Corolario 3.1:** Cada ángulo interno de un polígono regular de $n$ lados mide:
$$\alpha = \frac{(n-2) \times 180°}{n}$$

**Ejemplo 3.1:**
Para un hexágono regular ($n = 6$):
$$\alpha = \frac{(6-2) \times 180°}{6} = \frac{720°}{6} = 120°$$

**Definición 3.3.1 (Apotema):**
El **apotema** de un polígono regular es el segmento perpendicular desde el centro del polígono hasta el punto medio de cualquiera de sus lados. Se denota comúnmente como $a$.

**Interpretación geométrica:** El apotema representa la distancia más corta desde el centro del polígono hasta cualquiera de sus lados. Es análogo al radio de un círculo inscrito en el polígono.

**Relación con el radio circunscrito:**
Para un polígono regular de $n$ lados con lado $\ell$ y radio circunscrito $R$ (distancia del centro a un vértice), el apotema $a$ se relaciona mediante:
$$a = R \cos\left(\frac{180°}{n}\right) = R \cos\left(\frac{\pi}{n}\right)$$

**Teorema 3.3.2 (Área de un polígono regular usando apotema):**
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

**Sección 3.3.3 (Opcional): Convergencia del polígono regular al círculo**

Esta sección explora un resultado fascinante que conecta la geometría discreta (polígonos) con la geometría continua (círculos), anticipando conceptos del Cálculo Diferencial e Integral.

**Proposición 3.3.3 (Límite del polígono regular):**
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

**Definición 3.4 (Poliedro):**
Un **poliedro** es un sólido tridimensional limitado por caras planas poligonales.

**Elementos de un poliedro:**
- **Vértices (V):** Puntos donde se encuentran las aristas
- **Aristas (A):** Segmentos donde se encuentran dos caras
- **Caras (C):** Polígonos que forman las superficies del poliedro

**Teorema 3.4 (Fórmula de Euler para poliedros convexos):**
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

**Definición 4.4 (Imagen y preimagen):**
- La **imagen** de $f$ es: $\text{Im}(f) = \{y \in \mathbb{R} : \exists x \in \mathbb{R}, \, f(x) = y\}$
- La **preimagen** de $y$ es: $f^{-1}(\{y\}) = \{x \in \mathbb{R} : f(x) = y\}$

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

### 12.1 Geometría analítica

1. Calcule la distancia entre los puntos $A = (-3, 4)$ y $B = (5, -2)$

2. Encuentre el punto medio del segmento que une $P = (7, -1)$ y $Q = (-3, 5)$

3. Determine si el triángulo con vértices $A = (0, 0)$, $B = (3, 4)$, $C = (6, 0)$ es rectángulo

4. Calcule el perímetro del triángulo del ejercicio anterior

5. Encuentre las coordenadas del cuarto vértice $D$ del paralelogramo $ABCD$ si $A = (1, 2)$, $B = (4, 3)$, $C = (5, 6)$

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


