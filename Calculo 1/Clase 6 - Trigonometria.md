# Trigonometría: Fundamentos y Aplicaciones

## 1. Triángulos y elementos básicos

### 1.1 Repaso: Triángulos rectángulos

**Definición 1.1 (Triángulo rectángulo):**
Un **triángulo rectángulo** es un triángulo que tiene un ángulo de $90°$ (ángulo recto).

**Elementos principales:**
- **Hipotenusa:** El lado opuesto al ángulo recto (el lado más largo)
- **Catetos:** Los dos lados que forman el ángulo recto

```
        C
        |\
        | \
cateto  |  \  hipotenusa
    b   |   \   c
        |    \
        |_____\
        A  a  B
       cateto
```

**Teorema 1.1 (Teorema de Pitágoras):**
En todo triángulo rectángulo se cumple:
$$c^2 = a^2 + b^2$$
donde $c$ es la hipotenusa y $a$, $b$ son los catetos.

**Ejemplo 1.1:**
Si un triángulo rectángulo tiene catetos $a = 3$ y $b = 4$, la hipotenusa es:
$$c = \sqrt{3^2 + 4^2} = \sqrt{9 + 16} = \sqrt{25} = 5$$

---

## 2. Medición de ángulos

### 2.1 Sistemas de medición angular

**Definición 2.1 (Ángulo):**
Un **ángulo** es la medida de la rotación entre dos semirrectas que comparten un punto común llamado vértice.

Existen tres sistemas principales para medir ángulos:

### 2.2 Grados sexagesimales

**Definición 2.2 (Grado sexagesimal):**
Un **grado** ($°$) es $\frac{1}{360}$ de una rotación completa.

**Subdivisiones:**
- 1 grado = 60 minutos ($60'$)
- 1 minuto = 60 segundos ($60''$)

**Ángulos notables en grados:**
- Ángulo recto: $90°$
- Ángulo llano: $180°$
- Ángulo completo: $360°$

### 2.3 Radianes

**Definición 2.3 (Radián):**
Un **radián** (rad) es el ángulo que subtiende un arco de longitud igual al radio en una circunferencia.

**Relación fundamental:**
$$2\pi \text{ rad} = 360°$$
$$\pi \text{ rad} = 180°$$

**Fórmulas de conversión:**
$$\text{radianes} = \text{grados} \times \frac{\pi}{180}$$
$$\text{grados} = \text{radianes} \times \frac{180}{\pi}$$

**Ejemplo 2.1 (Conversiones):**

a) Convertir $45°$ a radianes:
$$45° = 45 \times \frac{\pi}{180} = \frac{\pi}{4} \text{ rad}$$

b) Convertir $\frac{2\pi}{3}$ rad a grados:
$$\frac{2\pi}{3} = \frac{2\pi}{3} \times \frac{180}{\pi} = 120°$$

**Nota (Constante tau $\tau$):**

Algunos matemáticos proponen usar la constante **tau** ($\tau$) definida como:
$$\tau = 2\pi \approx 6.283$$

Esta notación tiene ventajas conceptuales:
- **Una vuelta completa** al círculo = $\tau$ radianes (en lugar de $2\pi$)
- **Media vuelta** = $\frac{\tau}{2}$ (en lugar de $\pi$)
- **Un cuarto de vuelta** = $\frac{\tau}{4}$ (en lugar de $\frac{\pi}{2}$)

La relación entre ángulo y longitud de arco se vuelve aún más directa: $s = R \cdot \theta$ donde $\theta$ en un círculo completo es simplemente $\tau$. Aunque $\tau$ no es estándar en la mayoría de textos, es útil conocer esta alternativa.

**Tabla de conversión (ángulos comunes):**

| Grados | Radianes | Fracción de $\pi$ | Fracción de $\tau$ |
|--------|----------|-------------------|--------------------|
| $0°$ | $0$ | $0$ | $0$ |
| $30°$ | $\frac{\pi}{6}$ | $\frac{1}{6}\pi$ | $\frac{1}{12}\tau$ |
| $45°$ | $\frac{\pi}{4}$ | $\frac{1}{4}\pi$ | $\frac{1}{8}\tau$ |
| $60°$ | $\frac{\pi}{3}$ | $\frac{1}{3}\pi$ | $\frac{1}{6}\tau$ |
| $90°$ | $\frac{\pi}{2}$ | $\frac{1}{2}\pi$ | $\frac{1}{4}\tau$ |
| $120°$ | $\frac{2\pi}{3}$ | $\frac{2}{3}\pi$ | $\frac{1}{3}\tau$ |
| $135°$ | $\frac{3\pi}{4}$ | $\frac{3}{4}\pi$ | $\frac{3}{8}\tau$ |
| $150°$ | $\frac{5\pi}{6}$ | $\frac{5}{6}\pi$ | $\frac{5}{12}\tau$ |
| $180°$ | $\pi$ | $\pi$ | $\frac{1}{2}\tau$ |
| $210°$ | $\frac{7\pi}{6}$ | $\frac{7}{6}\pi$ | $\frac{7}{12}\tau$ |
| $225°$ | $\frac{5\pi}{4}$ | $\frac{5}{4}\pi$ | $\frac{5}{8}\tau$ |
| $240°$ | $\frac{4\pi}{3}$ | $\frac{4}{3}\pi$ | $\frac{2}{3}\tau$ |
| $270°$ | $\frac{3\pi}{2}$ | $\frac{3}{2}\pi$ | $\frac{3}{4}\tau$ |
| $300°$ | $\frac{5\pi}{3}$ | $\frac{5}{3}\pi$ | $\frac{5}{6}\tau$ |
| $315°$ | $\frac{7\pi}{4}$ | $\frac{7}{4}\pi$ | $\frac{7}{8}\tau$ |
| $330°$ | $\frac{11\pi}{6}$ | $\frac{11}{6}\pi$ | $\frac{11}{12}\tau$ |
| $360°$ | $2\pi$ | $2\pi$ | $\tau$ |

**Nota (Motivación de los radianes):**

La principal ventaja de los radianes sobre los grados sexagesimales es que **los radianes permiten expresar simultáneamente medidas angulares y longitudes de arco**.

En un círculo de radio $R$, si un ángulo $\theta$ (medido en radianes) subtiende un arco, entonces la **longitud del arco** $s$ está dada por:
$$s = R \cdot \theta$$

Esta relación directa y simple ($s = R\theta$) solo funciona cuando $\theta$ está en radianes. Por ejemplo:
- En un círculo de radio $R = 5$ metros, un ángulo de $\theta = 2$ radianes subtiende un arco de longitud $s = 5 \times 2 = 10$ metros.
- Para un ángulo completo ($\theta = 2\pi$ rad), obtenemos la circunferencia: $s = R \cdot 2\pi = 2\pi R$.

Si usáramos grados, la fórmula sería más complicada: $s = R \cdot \theta \cdot \frac{\pi}{180}$.

Esta propiedad hace que los radianes sean **esenciales en Cálculo**, donde las derivadas e integrales de funciones trigonométricas tienen formas simples solo cuando se usan radianes. Por ejemplo: $\frac{d}{dx}\sin(x) = \cos(x)$ solo si $x$ está en radianes.

### 2.4 Gradianes (gones)

**Definición 2.4 (Gradián):**
Un **gradián** o **gon** ($\text{g}$ o $\text{gon}$) es $\frac{1}{400}$ de una rotación completa.

**Relación:**
$$400^g = 360° = 2\pi \text{ rad}$$

**Conversión:**
$$\text{gradianes} = \text{grados} \times \frac{400}{360} = \text{grados} \times \frac{10}{9}$$

**Ejemplo 2.2:**
$$90° = 90 \times \frac{10}{9} = 100^g$$

**Observación:** Los gradianes se utilizan principalmente en topografía, geodesia y navegación. Su ventaja es que el ángulo recto mide exactamente $100^g$. En este curso trabajaremos principalmente con **grados** y **radianes**.



---

## 3. Razones trigonométricas en el triángulo rectángulo

### 3.1 Definiciones fundamentales

Dado un triángulo rectángulo con un ángulo agudo $\theta$:

```
        C
        |\
        | \
 opuesto|  \  hipotenusa
        |   \
        |    \
        |_θ___\
        A      B
       adyacente
```

**Definición 3.1 (Seno):**
$$\sin(\theta) = \frac{\text{cateto opuesto}}{\text{hipotenusa}}$$
**Definición 3.2 (Coseno):**
$$\cos(\theta) = \frac{\text{cateto adyacente}}{\text{hipotenusa}}$$
**Definición 3.3 (Tangente):**
$$\tan(\theta) = \frac{\text{cateto opuesto}}{\text{cateto adyacente}} = \frac{\sin(\theta)}{\cos(\theta)}$$
**Mnemotecnia SOH-CAH-TOA:**
- **S**eno = **O**puesto/**H**ipotenusa
- **C**oseno = **A**dyacente/**H**ipotenusa
- **T**angente = **O**puesto/**A**dyacente

**Ejemplo 3.1:**
En un triángulo rectángulo con hipotenusa $5$, cateto opuesto $3$ y cateto adyacente $4$:
$$\sin(\theta) = \frac{3}{5} = 0.6$$
$$\cos(\theta) = \frac{4}{5} = 0.8$$
$$\tan(\theta) = \frac{3}{4} = 0.75$$
### 3.2 Funciones trigonométricas recíprocas

**Definición 3.4 (Cosecante):**
$$\csc(\theta) = \frac{1}{\sin(\theta)} = \frac{\text{hipotenusa}}{\text{cateto opuesto}}$$
**Definición 3.5 (Secante):**
$$\sec(\theta) = \frac{1}{\cos(\theta)} = \frac{\text{hipotenusa}}{\text{cateto adyacente}}$$
**Definición 3.6 (Cotangente):**
$$\cot(\theta) = \frac{1}{\tan(\theta)} = \frac{\text{cateto adyacente}}{\text{cateto opuesto}} = \frac{\cos(\theta)}{\sin(\theta)}$$
**Resumen de las seis funciones:**

| Función        | Definición                                   | Recíproca                               |
| -------------- | -------------------------------------------- | --------------------------------------- |
| $\sin(\theta)$ | $\frac{\text{opuesto}}{\text{hipotenusa}}$   | $\csc(\theta) = \frac{1}{\sin(\theta)}$ |
| $\cos(\theta)$ | $\frac{\text{adyacente}}{\text{hipotenusa}}$ | $\sec(\theta) = \frac{1}{\cos(\theta)}$ |
| $\tan(\theta)$ | $\frac{\text{opuesto}}{\text{adyacente}}$    | $\cot(\theta) = \frac{1}{\tan(\theta)}$ |

---

## 4. Ángulos notables y tabla de valores

### 4.1 Triángulos especiales

**Triángulo de 45°-45°-90°:**

```
        •
       /|\
      / | \
     /  |  \
    / 1 | 1 \
   /    |    \
  /45° _|_ 45°\
 •_____√2______•
```

Si los catetos miden $1$, la hipotenusa mide $\sqrt{2}$.

$$\sin(45°) = \cos(45°) = \frac{1}{\sqrt{2}} = \frac{\sqrt{2}}{2}$$
$$\tan(45°) = 1$$

**Triángulo de 30°-60°-90°:**

```
        •
       /|\
      / | \
     /  |  \
  2 /   |√3 \
   /    |    \
  /30° _|_ 60°\
 •______1______•
```

$$\sin(30°) = \frac{1}{2}, \quad \cos(30°) = \frac{\sqrt{3}}{2}, \quad \tan(30°) = \frac{1}{\sqrt{3}} = \frac{\sqrt{3}}{3}$$

$$\sin(60°) = \frac{\sqrt{3}}{2}, \quad \cos(60°) = \frac{1}{2}, \quad \tan(60°) = \sqrt{3}$$

### 4.2 Tabla de valores para ángulos notables

**Tabla básica (seno, coseno, tangente):**

| $\theta$ | $0°$ | $30°$ | $45°$ | $60°$ | $90°$ |
|----------|------|-------|-------|-------|-------|
| **Radianes** | $0$ | $\frac{\pi}{6}$ | $\frac{\pi}{4}$ | $\frac{\pi}{3}$ | $\frac{\pi}{2}$ |
| $\sin(\theta)$ | $0$ | $\frac{1}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{3}}{2}$ | $1$ |
| $\cos(\theta)$ | $1$ | $\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{1}{2}$ | $0$ |
| $\tan(\theta)$ | $0$ | $\frac{\sqrt{3}}{3}$ | $1$ | $\sqrt{3}$ | indefinido |
### 4.3 Memotecnia: La "canción brasileña"

**Para recordar los valores del seno:**

| Ángulo | $0°$ | $30°$ | $45°$ | $60°$ | $90°$ |
|--------|------|-------|-------|-------|-------|
| Numerador | $\sqrt{0}$ | $\sqrt{1}$ | $\sqrt{2}$ | $\sqrt{3}$ | $\sqrt{4}$ |
| Denominador | $2$ | $2$ | $2$ | $2$ | $2$ |
| **Resultado** | $\frac{\sqrt{0}}{2} = 0$ | $\frac{\sqrt{1}}{2} = \frac{1}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{4}}{2} = 1$ |

**Frase mnemotécnica:** "**1, 2, 3, 3, 2, 1, todo mundo sobre 2, raíz en cada uno de novo**"

- **Seno:** $\frac{\sqrt{0}}{2}, \frac{\sqrt{1}}{2}, \frac{\sqrt{2}}{2}, \frac{\sqrt{3}}{2}, \frac{\sqrt{4}}{2}$ (de $0°$ a $90°$)
- **Coseno:** $\frac{\sqrt{4}}{2}, \frac{\sqrt{3}}{2}, \frac{\sqrt{2}}{2}, \frac{\sqrt{1}}{2}, \frac{\sqrt{0}}{2}$ (orden inverso)

### 4.4 Tabla extendida con funciones recíprocas

| $\theta$ | $0°$ | $30°$ | $45°$ | $60°$ | $90°$ |
|----------|------|-------|-------|-------|-------|
| $\sin(\theta)$ | $0$ | $\frac{1}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{3}}{2}$ | $1$ |
| $\cos(\theta)$ | $1$ | $\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{1}{2}$ | $0$ |
| $\tan(\theta)$ | $0$ | $\frac{\sqrt{3}}{3}$ | $1$ | $\sqrt{3}$ | indefinido |
| $\csc(\theta)$ | indefinido | $2$ | $\sqrt{2}$ | $\frac{2\sqrt{3}}{3}$ | $1$ |
| $\sec(\theta)$ | $1$ | $\frac{2\sqrt{3}}{3}$ | $\sqrt{2}$ | $2$ | indefinido |
| $\cot(\theta)$ | indefinido | $\sqrt{3}$ | $1$ | $\frac{\sqrt{3}}{3}$ | $0$ |

### 4.5 Extensión a los cuatro cuadrantes

Hasta ahora hemos trabajado con ángulos agudos (entre $0°$ y $90°$). Para extender las funciones trigonométricas a todos los ángulos, utilizamos el **círculo unitario** y consideramos los cuatro cuadrantes del plano cartesiano.

**Definición 4.5 (Ángulos en el plano cartesiano):**
Un ángulo se mide desde el eje X positivo en sentido **antihorario** (positivo) o **horario** (negativo).

```
       II   |   I
            |
      90°   |   0°
   ---------|--------- 
     180°   |   360°
            |
      III   |   IV
           270°
```

#### Signos de las funciones en cada cuadrante

**Cuadrante I** ($0° < \theta < 90°$ o $0 < \theta < \frac{\pi}{2}$):
- $\sin(\theta) > 0$ (coordenada y positiva)
- $\cos(\theta) > 0$ (coordenada x positiva)
- $\tan(\theta) > 0$
- **Todas las funciones son positivas**

**Cuadrante II** ($90° < \theta < 180°$ o $\frac{\pi}{2} < \theta < \pi$):
- $\sin(\theta) > 0$ (coordenada y positiva)
- $\cos(\theta) < 0$ (coordenada x negativa)
- $\tan(\theta) < 0$
- **Solo seno y cosecante son positivos**

**Cuadrante III** ($180° < \theta < 270°$ o $\pi < \theta < \frac{3\pi}{2}$):
- $\sin(\theta) < 0$ (coordenada y negativa)
- $\cos(\theta) < 0$ (coordenada x negativa)
- $\tan(\theta) > 0$
- **Solo tangente y cotangente son positivos**

**Cuadrante IV** ($270° < \theta < 360°$ o $\frac{3\pi}{2} < \theta < 2\pi$):
- $\sin(\theta) < 0$ (coordenada y negativa)
- $\cos(\theta) > 0$ (coordenada x positiva)
- $\tan(\theta) < 0$
- **Solo coseno y secante son positivos**

**Mnemotecnia - "All Students Take Calculus":**
```
      S     |   A
   (Seno)   | (All)
  ----------+----------
      T     |   C
  (Tangente)|(Coseno)
```

#### Ángulo de referencia

**Definición 4.6 (Ángulo de referencia):**
El **ángulo de referencia** $\theta'$ es el ángulo agudo formado entre el lado terminal del ángulo y el eje X.

**Cálculo del ángulo de referencia:**
- **Cuadrante I:** $\theta' = \theta$
- **Cuadrante II:** $\theta' = 180° - \theta$ o $\theta' = \pi - \theta$
- **Cuadrante III:** $\theta' = \theta - 180°$ o $\theta' = \theta - \pi$
- **Cuadrante IV:** $\theta' = 360° - \theta$ o $\theta' = 2\pi - \theta$

**Ejemplo 4.3:**
Encuentre el ángulo de referencia para:

a) $\theta = 150°$: Cuadrante II → $\theta' = 180° - 150° = 30°$

b) $\theta = 225°$: Cuadrante III → $\theta' = 225° - 180° = 45°$

c) $\theta = 315°$: Cuadrante IV → $\theta' = 360° - 315° = 45°$

**Ejemplo 4.4:**
Calcule $\sin(150°)$:

- Cuadrante II: seno es positivo
- Ángulo de referencia: $30°$
- $\sin(150°) = +\sin(30°) = \frac{1}{2}$

**Ejemplo 4.5:**
Calcule $\cos(225°)$:

- Cuadrante III: coseno es negativo
- Ángulo de referencia: $45°$
- $\cos(225°) = -\cos(45°) = -\frac{\sqrt{2}}{2}$

#### Tabla completa de valores (ángulos de $0$ a $2\pi$)

**Tabla de valores exactos para ángulos notables:**

| Grados | Radianes | $\sin(\theta)$ | $\cos(\theta)$ | $\tan(\theta)$ | Cuadrante |
|--------|----------|----------------|----------------|----------------|-----------|
| $0°$ | $0$ | $0$ | $1$ | $0$ | - |
| $30°$ | $\frac{\pi}{6}$ | $\frac{1}{2}$ | $\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{3}}{3}$ | I |
| $45°$ | $\frac{\pi}{4}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{2}}{2}$ | $1$ | I |
| $60°$ | $\frac{\pi}{3}$ | $\frac{\sqrt{3}}{2}$ | $\frac{1}{2}$ | $\sqrt{3}$ | I |
| $90°$ | $\frac{\pi}{2}$ | $1$ | $0$ | indefinido | - |
| $120°$ | $\frac{2\pi}{3}$ | $\frac{\sqrt{3}}{2}$ | $-\frac{1}{2}$ | $-\sqrt{3}$ | II |
| $135°$ | $\frac{3\pi}{4}$ | $\frac{\sqrt{2}}{2}$ | $-\frac{\sqrt{2}}{2}$ | $-1$ | II |
| $150°$ | $\frac{5\pi}{6}$ | $\frac{1}{2}$ | $-\frac{\sqrt{3}}{2}$ | $-\frac{\sqrt{3}}{3}$ | II |
| $180°$ | $\pi$ | $0$ | $-1$ | $0$ | - |
| $210°$ | $\frac{7\pi}{6}$ | $-\frac{1}{2}$ | $-\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{3}}{3}$ | III |
| $225°$ | $\frac{5\pi}{4}$ | $-\frac{\sqrt{2}}{2}$ | $-\frac{\sqrt{2}}{2}$ | $1$ | III |
| $240°$ | $\frac{4\pi}{3}$ | $-\frac{\sqrt{3}}{2}$ | $-\frac{1}{2}$ | $\sqrt{3}$ | III |
| $270°$ | $\frac{3\pi}{2}$ | $-1$ | $0$ | indefinido | - |
| $300°$ | $\frac{5\pi}{3}$ | $-\frac{\sqrt{3}}{2}$ | $\frac{1}{2}$ | $-\sqrt{3}$ | IV |
| $315°$ | $\frac{7\pi}{4}$ | $-\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{2}}{2}$ | $-1$ | IV |
| $330°$ | $\frac{11\pi}{6}$ | $-\frac{1}{2}$ | $\frac{\sqrt{3}}{2}$ | $-\frac{\sqrt{3}}{3}$ | IV |
| $360°$ | $2\pi$ | $0$ | $1$ | $0$ | - |

**Observaciones importantes:**

1. **Periodicidad:** Las funciones trigonométricas se repiten cada $360°$ (o $2\pi$ radianes):
   - $\sin(\theta + 360°) = \sin(\theta)$
   - $\cos(\theta + 360°) = \cos(\theta)$
   - $\tan(\theta + 180°) = \tan(\theta)$ (período de $180°$ para tangente)

2. **Simetría:**
   - Los valores de $\sin(\theta)$ tienen simetría respecto al eje Y
   - Los valores de $\cos(\theta)$ tienen simetría respecto al eje X
   - Los ángulos complementarios suman $90°$: $\sin(\theta) = \cos(90° - \theta)$
   - Los ángulos suplementarios suman $180°$: $\sin(\theta) = \sin(180° - \theta)$

3. **Patrón de referencia:**
   - Todos los valores se obtienen a partir de los ángulos básicos: $30°$, $45°$, $60°$
   - Solo cambia el signo según el cuadrante

---

## 5. El círculo trigonométrico

### 5.1 Definición del círculo unitario

**Definición 5.1 (Círculo unitario):**
El **círculo unitario** es el círculo de radio $1$ centrado en el origen del plano cartesiano:
$$x^2 + y^2 = 1$$

**Definición extendida de funciones trigonométricas:**

Dado un ángulo $\theta$ medido desde el eje X positivo (sentido antihorario), definimos:
- El punto $P = (\cos(\theta), \sin(\theta))$ en el círculo unitario
- $\sin(\theta)$ es la **coordenada y** del punto $P$
- $\cos(\theta)$ es la **coordenada x** del punto $P$

```
         y
         |
         | P(cosθ, sinθ)
       1 |●
         |  \
         |   \ r=1
         |    \
    -----+-----●------- x
         O     θ
```

**Ventaja:** Esta definición permite extender las funciones trigonométricas a **todos los ángulos** (no solo agudos).

### 5.2 Signos de las funciones en los cuadrantes

**Cuadrante I** ($0° < \theta < 90°$):
- $\sin(\theta) > 0$, $\cos(\theta) > 0$, $\tan(\theta) > 0$
- **Todas positivas**

**Cuadrante II** ($90° < \theta < 180°$):
- $\sin(\theta) > 0$, $\cos(\theta) < 0$, $\tan(\theta) < 0$
- **Solo seno positivo**

**Cuadrante III** ($180° < \theta < 270°$):
- $\sin(\theta) < 0$, $\cos(\theta) < 0$, $\tan(\theta) > 0$
- **Solo tangente positiva**

**Cuadrante IV** ($270° < \theta < 360°$):
- $\sin(\theta) < 0$, $\cos(\theta) > 0$, $\tan(\theta) < 0$
- **Solo coseno positivo**

**Mnemotecnia:** "**All Students Take Calculus**" (Todas, Seno, Tangente, Coseno)

```
      II    |    I
   S positivo| Todo positivo
  ---------- + ----------
   T positivo| C positivo
      III   |    IV
```

### 5.3 Valores extendidos

**Ejemplo 5.1:**

| Ángulo | Seno | Coseno | Tangente |
|--------|------|--------|----------|
| $0°$ | $0$ | $1$ | $0$ |
| $90°$ | $1$ | $0$ | indefinido |
| $180°$ | $0$ | $-1$ | $0$ |
| $270°$ | $-1$ | $0$ | indefinido |
| $360°$ | $0$ | $1$ | $0$ |

---

## 6. Identidades trigonométricas fundamentales

### 6.1 Identidad pitagórica

**Teorema 6.1 (Identidad fundamental):**
$$\sin^2(\theta) + \cos^2(\theta) = 1$$

**Demostración:** En el círculo unitario, el punto $(\cos(\theta), \sin(\theta))$ satisface $x^2 + y^2 = 1$. Por lo tanto:
$$\cos^2(\theta) + \sin^2(\theta) = 1$$

**Notación:** $\sin^2(\theta)$ significa $(\sin(\theta))^2$

**Variantes de la identidad pitagórica:**

De $\sin^2(\theta) + \cos^2(\theta) = 1$ se derivan:

**Identidad 6.1:**
$$\tan^2(\theta) + 1 = \sec^2(\theta)$$

**Demostración:** Dividimos la identidad fundamental por $\cos^2(\theta)$:
$$\frac{\sin^2(\theta)}{\cos^2(\theta)} + \frac{\cos^2(\theta)}{\cos^2(\theta)} = \frac{1}{\cos^2(\theta)}$$
$$\tan^2(\theta) + 1 = \sec^2(\theta)$$

**Identidad 6.2:**
$$1 + \cot^2(\theta) = \csc^2(\theta)$$

**Demostración:** Dividimos por $\sin^2(\theta)$:
$$\frac{\sin^2(\theta)}{\sin^2(\theta)} + \frac{\cos^2(\theta)}{\sin^2(\theta)} = \frac{1}{\sin^2(\theta)}$$
$$1 + \cot^2(\theta) = \csc^2(\theta)$$

### 6.2 Identidades recíprocas

**Identidad 6.3:**
$$\csc(\theta) = \frac{1}{\sin(\theta)}, \quad \sec(\theta) = \frac{1}{\cos(\theta)}, \quad \cot(\theta) = \frac{1}{\tan(\theta)}$$

### 6.3 Identidades de cociente

**Identidad 6.4:**
$$\tan(\theta) = \frac{\sin(\theta)}{\cos(\theta)}, \quad \cot(\theta) = \frac{\cos(\theta)}{\sin(\theta)}$$

### 6.4 Identidades de ángulos coterminales y negativos

**Identidad 6.5 (Periodicidad):**
$$\sin(\theta + 2\pi) = \sin(\theta)$$
$$\cos(\theta + 2\pi) = \cos(\theta)$$
$$\tan(\theta + \pi) = \tan(\theta)$$

**Identidad 6.6 (Ángulos negativos):**
$$\sin(-\theta) = -\sin(\theta)$$ (función impar)
$$\cos(-\theta) = \cos(\theta)$$ (función par)
$$\tan(-\theta) = -\tan(\theta)$$ (función impar)

### 6.5 Identidades de ángulos complementarios

**Identidad 6.7:**
$$\sin(90° - \theta) = \cos(\theta)$$
$$\cos(90° - \theta) = \sin(\theta)$$
$$\tan(90° - \theta) = \cot(\theta)$$

**Ejemplo 6.1:**
$$\sin(30°) = \cos(60°) = \frac{1}{2}$$
$$\cos(30°) = \sin(60°) = \frac{\sqrt{3}}{2}$$

### 6.6 Identidades de suma y diferencia

**Teorema 6.2 (Fórmulas de suma):**
$$\sin(\alpha + \beta) = \sin(\alpha)\cos(\beta) + \cos(\alpha)\sin(\beta)$$
$$\cos(\alpha + \beta) = \cos(\alpha)\cos(\beta) - \sin(\alpha)\sin(\beta)$$
$$\tan(\alpha + \beta) = \frac{\tan(\alpha) + \tan(\beta)}{1 - \tan(\alpha)\tan(\beta)}$$

**Teorema 6.3 (Fórmulas de diferencia):**
$$\sin(\alpha - \beta) = \sin(\alpha)\cos(\beta) - \cos(\alpha)\sin(\beta)$$
$$\cos(\alpha - \beta) = \cos(\alpha)\cos(\beta) + \sin(\alpha)\sin(\beta)$$
$$\tan(\alpha - \beta) = \frac{\tan(\alpha) - \tan(\beta)}{1 + \tan(\alpha)\tan(\beta)}$$

**Ejemplo 6.2:**
Calcule $\sin(75°)$ usando $75° = 45° + 30°$:

$$\begin{align}
\sin(75°) &= \sin(45° + 30°) \\
&= \sin(45°)\cos(30°) + \cos(45°)\sin(30°) \\
&= \frac{\sqrt{2}}{2} \cdot \frac{\sqrt{3}}{2} + \frac{\sqrt{2}}{2} \cdot \frac{1}{2} \\
&= \frac{\sqrt{6}}{4} + \frac{\sqrt{2}}{4} \\
&= \frac{\sqrt{6} + \sqrt{2}}{4}
\end{align}$$

### 6.7 Identidades de ángulo doble

**Teorema 6.4 (Ángulo doble):**
$$\sin(2\theta) = 2\sin(\theta)\cos(\theta)$$
$$\cos(2\theta) = \cos^2(\theta) - \sin^2(\theta)$$

**Formas alternativas de $\cos(2\theta)$:**
$$\cos(2\theta) = 2\cos^2(\theta) - 1 = 1 - 2\sin^2(\theta)$$

$$\tan(2\theta) = \frac{2\tan(\theta)}{1 - \tan^2(\theta)}$$

**Ejemplo 6.3:**
Si $\sin(\theta) = \frac{3}{5}$ y $\theta$ está en el primer cuadrante, calcule $\sin(2\theta)$:

Primero encontramos $\cos(\theta)$ usando $\sin^2(\theta) + \cos^2(\theta) = 1$:
$$\cos(\theta) = \sqrt{1 - \sin^2(\theta)} = \sqrt{1 - \frac{9}{25}} = \sqrt{\frac{16}{25}} = \frac{4}{5}$$

Ahora:
$$\sin(2\theta) = 2\sin(\theta)\cos(\theta) = 2 \cdot \frac{3}{5} \cdot \frac{4}{5} = \frac{24}{25}$$

---

## 7. Verificación de identidades trigonométricas

### 7.1 Estrategias para verificar identidades

**Técnicas comunes:**
1. Trabajar con un lado de la ecuación para transformarlo en el otro
2. Expresar todo en términos de seno y coseno
3. Usar identidades pitagóricas
4. Factorizar o multiplicar por conjugados
5. Buscar un denominador común

**Ejemplo 7.1:**
Verificar: $\tan(\theta) + \cot(\theta) = \sec(\theta)\csc(\theta)$

**Solución:**
Lado izquierdo:
$$\begin{align}
\tan(\theta) + \cot(\theta) &= \frac{\sin(\theta)}{\cos(\theta)} + \frac{\cos(\theta)}{\sin(\theta)} \\
&= \frac{\sin^2(\theta) + \cos^2(\theta)}{\sin(\theta)\cos(\theta)} \\
&= \frac{1}{\sin(\theta)\cos(\theta)} \\
&= \frac{1}{\sin(\theta)} \cdot \frac{1}{\cos(\theta)} \\
&= \csc(\theta)\sec(\theta)
\end{align}$$

Verificado ✓

**Ejemplo 7.2:**
Verificar: $\frac{1 - \sin^2(\theta)}{1 + \cos(\theta)} = \cos(\theta)$

**Solución:**
$$\begin{align}
\frac{1 - \sin^2(\theta)}{1 + \cos(\theta)} &= \frac{\cos^2(\theta)}{1 + \cos(\theta)} \\
&= \frac{\cos(\theta) \cdot \cos(\theta)}{1 + \cos(\theta)} \\
&= \cos(\theta) \cdot \frac{\cos(\theta)}{1 + \cos(\theta)}
\end{align}$$

Pero mejor usamos:
$$\frac{\cos^2(\theta)}{1 + \cos(\theta)} = \frac{(1 - \cos(\theta))(1 + \cos(\theta))}{1 + \cos(\theta)} \text{ NO!}$$

Correcto:
$$\frac{\cos^2(\theta)}{1 + \cos(\theta)} = \cos(\theta) \cdot \frac{\cos(\theta)}{1 + \cos(\theta)}$$

En realidad, si $\cos^2(\theta) = (1 + \cos(\theta))(1 - \cos(\theta))$ no es correcto.

Lo correcto es:
$$\frac{\cos^2(\theta)}{1 + \cos(\theta)} = \frac{(1 + \cos(\theta))(1 - \cos(\theta))}{1 + \cos(\theta)} \text{ es FALSO}$$

Corregimos: Usamos $1 - \sin^2(\theta) = \cos^2(\theta)$, pero luego necesitamos simplificar de otra forma.

Mejor método: multiplicar por conjugado:
$$\frac{\cos^2(\theta)}{1 + \cos(\theta)} \cdot \frac{1 - \cos(\theta)}{1 - \cos(\theta)} = \frac{\cos^2(\theta)(1 - \cos(\theta))}{1 - \cos^2(\theta)} = \frac{\cos^2(\theta)(1 - \cos(\theta))}{\sin^2(\theta)}$$

Esto no simplifica bien. Intentemos directamente:

Si la identidad es correcta:
$$\frac{\cos^2(\theta)}{1 + \cos(\theta)} = \cos(\theta)$$
$$\cos^2(\theta) = \cos(\theta)(1 + \cos(\theta))$$
$$\cos^2(\theta) = \cos(\theta) + \cos^2(\theta)$$
$$0 = \cos(\theta)$$

Esto NO es una identidad. Probablemente hay un error en el enunciado.

**Ejemplo 7.2 (corregido):**
Verificar: $\frac{1 - \cos(\theta)}{1 + \cos(\theta)} = \frac{\sin^2(\theta)}{(1 + \cos(\theta))^2}$

No, mejor usar un ejemplo estándar:

**Ejemplo 7.2 (corregido):**
Verificar: $\frac{1 - \cos^2(\theta)}{1 - \sin(\theta)} = \sin(\theta) + \sin(\theta)\cos(\theta)$

Lado izquierdo:
$$\begin{align}
\frac{1 - \cos^2(\theta)}{1 - \sin(\theta)} &= \frac{\sin^2(\theta)}{1 - \sin(\theta)}
\end{align}$$

Esto no se simplifica fácilmente al lado derecho. 

Usemos ejemplo más simple:

**Ejemplo 7.2 (versión final):**
Verificar: $\frac{\sin(\theta)}{1 + \cos(\theta)} = \frac{1 - \cos(\theta)}{\sin(\theta)}$

**Solución:** Multiplicamos cruzado o verificamos multiplicando el denominador de la izquierda por el numerador de la derecha:
$$\sin(\theta) \cdot \sin(\theta) = (1 + \cos(\theta))(1 - \cos(\theta))$$
$$\sin^2(\theta) = 1 - \cos^2(\theta)$$
$$\sin^2(\theta) = \sin^2(\theta)$$ ✓

---

## 8. Funciones trigonométricas

### 8.1 La función seno

**Definición 8.1:**
$$f(x) = \sin(x)$$

**Propiedades:**
- **Dominio:** $(-\infty, +\infty)$
- **Imagen:** $[-1, 1]$
- **Período:** $2\pi$ (la función se repite cada $2\pi$)
- **Simetría:** Función impar ($\sin(-x) = -\sin(x)$)
- **Ceros:** $x = n\pi$, donde $n \in \mathbb{Z}$
- **Máximos:** $x = \frac{\pi}{2} + 2n\pi$, valor $1$
- **Mínimos:** $x = \frac{3\pi}{2} + 2n\pi$, valor $-1$

**Gráfica:**

```
    y
    |
  1 |    ╱‾‾╲        ╱‾‾╲
    |   ╱    ╲      ╱    ╲
----+--+------+----+------+-----> x
    | 0   π   2π  3π   4π
 -1 |        ╲__╱        ╲__╱
```

### 8.2 La función coseno

**Definición 8.2:**
$$f(x) = \cos(x)$$

**Propiedades:**
- **Dominio:** $(-\infty, +\infty)$
- **Imagen:** $[-1, 1]$
- **Período:** $2\pi$
- **Simetría:** Función par ($\cos(-x) = \cos(x)$)
- **Ceros:** $x = \frac{\pi}{2} + n\pi$, donde $n \in \mathbb{Z}$
- **Máximos:** $x = 2n\pi$, valor $1$
- **Mínimos:** $x = \pi + 2n\pi$, valor $-1$

**Gráfica:**

```
    y
    |
  1 |‾‾╲        ╱‾‾╲        ╱‾‾
    |   ╲      ╱    ╲      ╱
----+----+----+------+----+----> x
    |    π/2  π   3π/2  2π
 -1 |    ╲__╱        ╲__╱
```

**Observación:** $\cos(x) = \sin(x + \frac{\pi}{2})$ (coseno es seno desplazado)

### 8.3 La función tangente

**Definición 8.3:**
$$f(x) = \tan(x) = \frac{\sin(x)}{\cos(x)}$$

**Propiedades:**
- **Dominio:** $\mathbb{R} \setminus \{\frac{\pi}{2} + n\pi : n \in \mathbb{Z}\}$ (excluye donde $\cos(x) = 0$)
- **Imagen:** $(-\infty, +\infty)$
- **Período:** $\pi$
- **Simetría:** Función impar
- **Ceros:** $x = n\pi$
- **Asíntotas verticales:** $x = \frac{\pi}{2} + n\pi$

**Gráfica:**

```
    y
    |
    |    |      |      |
    |   /|     /|     /|
    |  / |    / |    / |
----+-/--+---/--+---/--+----> x
    |/   |  /   |  /   |
   /|    | /    | /    |
  / |    |/     |/     |
    -π/2 0  π/2  π  3π/2
```

### 8.4 Transformaciones de funciones trigonométricas

**Forma general:**
$$f(x) = A \cdot \sin(B \cdot x + C) + D$$

**Parámetros:**

1. **$A$: Amplitud**
   - Controla la altura máxima y mínima
   - La función oscila entre $-|A| + D$ y $|A| + D$

2. **$B$: Frecuencia**
   - Controla cuántas oscilaciones completas hay en $2\pi$
   - **Período:** $T = \frac{2\pi}{|B|}$

3. **$C$: Desfase o fase inicial**
   - Desplazamiento horizontal
   - **Desfase:** $\phi = -\frac{C}{B}$ (hacia la izquierda si $\phi > 0$)

4. **$D$: Desplazamiento vertical**
   - Mueve la gráfica hacia arriba ($D > 0$) o abajo ($D < 0$)
   - La línea central es $y = D$

**Ejemplo 8.1:**
$$f(x) = 3\sin(2x - \pi) + 1$$

- **Amplitud:** $A = 3$ → oscila entre $-2$ y $4$
- **Período:** $T = \frac{2\pi}{2} = \pi$
- **Desfase:** $\phi = -\frac{-\pi}{2} = \frac{\pi}{2}$ (desplazado $\frac{\pi}{2}$ a la derecha)
- **Desplazamiento vertical:** $D = 1$ (eje central en $y = 1$)

**Ejemplo 8.2:**
$$g(x) = -2\cos\left(\frac{x}{3} + \frac{\pi}{4}\right) - 1$$

- **Amplitud:** $|A| = 2$
- **Reflexión:** $A < 0$ → gráfica invertida
- **Período:** $T = \frac{2\pi}{1/3} = 6\pi$
- **Desfase:** $\phi = -\frac{\pi/4}{1/3} = -\frac{3\pi}{4}$ (desplazado $\frac{3\pi}{4}$ a la izquierda)
- **Desplazamiento vertical:** $D = -1$

---

## 9. Relación con círculos y parametrización

### 9.1 Parametrización del círculo unitario

**Proposición 9.1:**
El círculo unitario $x^2 + y^2 = 1$ puede parametrizarse como:
$$\begin{cases}
x(t) = \cos(t) \\
y(t) = \sin(t)
\end{cases}, \quad t \in [0, 2\pi)$$

**Verificación:** 
$$x(t)^2 + y(t)^2 = \cos^2(t) + \sin^2(t) = 1$$ ✓

A medida que $t$ varía de $0$ a $2\pi$, el punto $(\cos(t), \sin(t))$ recorre el círculo una vez en sentido antihorario.

### 9.2 Parametrización de círculos de radio $R$

**Proposición 9.2:**
El círculo de radio $R$ centrado en el origen $x^2 + y^2 = R^2$ tiene parametrización:
$$\begin{cases}
x(t) = R\cos(t) \\
y(t) = R\sin(t)
\end{cases}, \quad t \in [0, 2\pi)$$

**Verificación:**
$$x(t)^2 + y(t)^2 = R^2\cos^2(t) + R^2\sin^2(t) = R^2(\cos^2(t) + \sin^2(t)) = R^2$$ ✓

**Ejemplo 9.1:**
El círculo de radio $3$ se parametriza:
$$x(t) = 3\cos(t), \quad y(t) = 3\sin(t)$$

**Puntos específicos:**
- $t = 0$: $(3, 0)$
- $t = \frac{\pi}{2}$: $(0, 3)$
- $t = \pi$: $(-3, 0)$
- $t = \frac{3\pi}{2}$: $(0, -3)$

### 9.3 Círculos desplazados

**Proposición 9.3:**
El círculo de radio $R$ centrado en $(h, k)$ tiene ecuación $(x - h)^2 + (y - k)^2 = R^2$ y parametrización:
$$\begin{cases}
x(t) = h + R\cos(t) \\
y(t) = k + R\sin(t)
\end{cases}$$

**Ejemplo 9.2:**
Círculo de radio $2$ centrado en $(1, -3)$:
$$x(t) = 1 + 2\cos(t), \quad y(t) = -3 + 2\sin(t)$$

---

## 10. Ecuaciones trigonométricas

### 10.1 Ecuaciones básicas

**Ejemplo 10.1:**
Resuelva $\sin(x) = \frac{1}{2}$ para $x \in [0, 2\pi)$.

**Solución:**
Los ángulos de referencia son $30° = \frac{\pi}{6}$ y $150° = \frac{5\pi}{6}$.

$$x = \frac{\pi}{6} \quad \text{o} \quad x = \frac{5\pi}{6}$$

**Solución general (todos los valores):**
$$x = \frac{\pi}{6} + 2n\pi \quad \text{o} \quad x = \frac{5\pi}{6} + 2n\pi, \quad n \in \mathbb{Z}$$

**Ejemplo 10.2:**
Resuelva $\cos(x) = -\frac{\sqrt{2}}{2}$ para $x \in [0, 2\pi)$.

**Solución:**
El ángulo de referencia es $45° = \frac{\pi}{4}$. Como el coseno es negativo en los cuadrantes II y III:

$$x = \pi - \frac{\pi}{4} = \frac{3\pi}{4} \quad \text{o} \quad x = \pi + \frac{\pi}{4} = \frac{5\pi}{4}$$

### 10.2 Ecuaciones con identidades

**Ejemplo 10.3:**
Resuelva $2\sin^2(x) - \sin(x) - 1 = 0$ para $x \in [0, 2\pi)$.

**Solución:**
Sea $u = \sin(x)$. La ecuación se convierte en:
$$2u^2 - u - 1 = 0$$

Factorizando: $(2u + 1)(u - 1) = 0$

$$u = -\frac{1}{2} \quad \text{o} \quad u = 1$$

**Caso 1:** $\sin(x) = 1$
$$x = \frac{\pi}{2}$$

**Caso 2:** $\sin(x) = -\frac{1}{2}$
$$x = \frac{7\pi}{6} \quad \text{o} \quad x = \frac{11\pi}{6}$$

**Soluciones:** $x \in \left\{\frac{\pi}{2}, \frac{7\pi}{6}, \frac{11\pi}{6}\right\}$

**Ejemplo 10.4:**
Resuelva $\tan(x) = \sqrt{3}$ para $x \in [0, 2\pi)$.

**Solución:**
El ángulo de referencia es $60° = \frac{\pi}{3}$. La tangente es positiva en los cuadrantes I y III:

$$x = \frac{\pi}{3} \quad \text{o} \quad x = \pi + \frac{\pi}{3} = \frac{4\pi}{3}$$

### 10.3 Ecuaciones con múltiplos

**Ejemplo 10.5:**
Resuelva $\sin(2x) = \frac{\sqrt{3}}{2}$ para $x \in [0, 2\pi)$.

**Solución:**
Sea $u = 2x$. Entonces $\sin(u) = \frac{\sqrt{3}}{2}$.

Para $u \in [0, 4\pi)$ (porque $x \in [0, 2\pi) \Rightarrow 2x \in [0, 4\pi)$):
$$u = \frac{\pi}{3}, \frac{2\pi}{3}, \frac{\pi}{3} + 2\pi = \frac{7\pi}{3}, \frac{2\pi}{3} + 2\pi = \frac{8\pi}{3}$$

Luego:
$$x = \frac{u}{2} = \frac{\pi}{6}, \frac{\pi}{3}, \frac{7\pi}{6}, \frac{4\pi}{3}$$

### 10.4 Ecuaciones que requieren identidades

**Ejemplo 10.6:**
Resuelva $\cos(2x) = \cos(x)$ para $x \in [0, 2\pi)$.

**Solución:**
Usamos $\cos(2x) = 2\cos^2(x) - 1$:
$$2\cos^2(x) - 1 = \cos(x)$$
$$2\cos^2(x) - \cos(x) - 1 = 0$$

Factorizando (con $u = \cos(x)$):
$$(2u + 1)(u - 1) = 0$$

$$\cos(x) = -\frac{1}{2} \quad \text{o} \quad \cos(x) = 1$$

**Caso 1:** $\cos(x) = 1 \Rightarrow x = 0$

**Caso 2:** $\cos(x) = -\frac{1}{2} \Rightarrow x = \frac{2\pi}{3}, \frac{4\pi}{3}$

**Soluciones:** $x \in \left\{0, \frac{2\pi}{3}, \frac{4\pi}{3}\right\}$

---

## 11. Ejercicios propuestos

### 11.1 Conversión de ángulos

1. Convierta a radianes: $120°$, $225°$, $315°$
2. Convierta a grados: $\frac{5\pi}{6}$, $\frac{7\pi}{4}$, $\frac{11\pi}{6}$
3. Convierta $90°$ a gradianes

### 11.2 Razones trigonométricas

4. En un triángulo rectángulo con catetos $5$ y $12$, calcule las seis funciones trigonométricas del ángulo agudo menor

5. Si $\sin(\theta) = \frac{2}{3}$ y $\theta$ está en el segundo cuadrante, encuentre $\cos(\theta)$ y $\tan(\theta)$

6. Si $\tan(\theta) = -\frac{3}{4}$ y $\theta$ está en el cuarto cuadrante, encuentre $\sin(\theta)$ y $\cos(\theta)$

### 11.3 Valores exactos

7. Calcule sin usar calculadora: $\sin(150°)$, $\cos(240°)$, $\tan(135°)$

8. Evalúe: $\sin\left(\frac{7\pi}{6}\right) + \cos\left(\frac{5\pi}{3}\right)$

9. Simplifique: $\sin(30°)\cos(60°) + \cos(30°)\sin(60°)$

### 11.4 Identidades

10. Verifique: $\frac{1 - \sin^2(\theta)}{\cos(\theta)} = \cos(\theta)$

11. Verifique: $(\sin(\theta) + \cos(\theta))^2 = 1 + 2\sin(\theta)\cos(\theta)$

12. Verifique: $\frac{\tan(\theta) + \cot(\theta)}{\tan(\theta)} = \csc^2(\theta)$

13. Simplifique: $\frac{\sin^2(\theta) - \cos^2(\theta)}{\sin(\theta) - \cos(\theta)}$

### 11.5 Ecuaciones trigonométricas

14. Resuelva para $x \in [0, 2\pi)$: $\sin(x) = -\frac{\sqrt{3}}{2}$

15. Resuelva para $x \in [0, 2\pi)$: $2\cos(x) + 1 = 0$

16. Resuelva para $x \in [0, 2\pi)$: $\tan^2(x) = 3$

17. Resuelva para $x \in [0, 2\pi)$: $2\sin^2(x) + 3\sin(x) + 1 = 0$

18. Resuelva para $x \in [0, 2\pi)$: $\cos(2x) = \frac{1}{2}$

### 11.6 Aplicaciones

19. Una rueda de radio $5$ metros gira. Encuentre la parametrización de la trayectoria de un punto en el borde

20. Encuentre la ecuación del círculo de radio $4$ centrado en $(2, -1)$ en forma paramétrica

21. Una onda se describe por $f(t) = 10\sin(4\pi t - \frac{\pi}{3}) + 5$. Determine su amplitud, período, desfase y desplazamiento vertical

22. Demuestre que $\sin(3\theta) = 3\sin(\theta) - 4\sin^3(\theta)$ usando identidades de suma

23. Si $\cos(\alpha) = \frac{3}{5}$ ($\alpha$ en cuadrante I) y $\sin(\beta) = \frac{5}{13}$ ($\beta$ en cuadrante II), calcule $\sin(\alpha + \beta)$

24. Encuentre el ángulo de elevación del sol si un poste de $10$ metros proyecta una sombra de $15$ metros

25. Una escalera de $8$ metros se apoya contra una pared formando un ángulo de $60°$ con el suelo. ¿A qué altura de la pared llega la escalera?

---

**Fin de la Clase 5**

