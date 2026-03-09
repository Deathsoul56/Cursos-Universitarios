# Trigonometría: Fundamentos y Aplicaciones

## 1. Triángulos y elementos básicos

### 1.1 Repaso: Triángulos rectángulos

**Definición 1.1 (Triángulo rectángulo):**
Un **triángulo rectángulo** es un triángulo que tiene un ángulo de $\pi/2$ o $90°$ (ángulo recto).

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
Un **ángulo** es la medida de la "apertura" (rotación) entre dos semirrectas que comparten un punto común llamado vértice.

Existen tres sistemas principales para medir ángulos:

### 2.2 Grados sexagesimales

**Definición 2.2 (Grado sexagesimal):**
Pensemos en una circunferencia de radio R; vamos a definir de forma arbitraria que dar una vuelta completa equivale a 360°, por lo tanto, un **grado** ($°$) es $\frac{1}{360}$ de una rotación completa.

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
$$45° = 45° \times \frac{\pi}{180°} = \frac{\pi}{4} \text{ rad}$$

b) Convertir $\frac{2\pi}{3}$ rad a grados:
$$\frac{2\pi}{3} = \frac{2\pi}{3} \times \frac{180°}{\pi} = 120°$$

**Nota (Constante tau $\tau$):**

Algunos matemáticos proponen usar la constante **tau** ($\tau$) definida como:
$$\tau = 2\pi \approx 6.283$$

Esta notación tiene ventajas conceptuales:
- **Una vuelta completa** al círculo = $\tau$ radianes (en lugar de $2\pi$)
- **Media vuelta** = $\frac{\tau}{2}$ (en lugar de $\pi$)
- **Un cuarto de vuelta** = $\frac{\tau}{4}$ (en lugar de $\frac{\pi}{2}$)

La relación entre ángulo y longitud de arco se vuelve aún más directa: $s = R \cdot \theta$ donde $\theta$ en un círculo completo es simplemente $\tau$. Aunque $\tau$ no es estándar en la mayoría de textos, es útil conocer esta alternativa.

**Ángulos notables y Tabla de conversión:**

Existe un grupo de ángulos llamados ángulos notables en los cuales se basan algunos de los cálculos de trigonometría, estos ángulos en sexagesimal son 30°, 45°, 60° y 90°. Estos fueron escogidos por argumentos geométricos, un cuadrado es una estructura considerada "perfecta", lados iguales y ángulos iguales, podemos considerar esta estructura un invariante pues puedo convertir cualquier cuadrado en otro simplemente aumentado o dismiyendo sus lados (una transformación suave, este termino cobrara una gran relevancia mas adelante) y sus angulos siempre se conservaran en 90°, si dibujamos una diagonal tendremos un triangulo isósceles, por lo tanto la diagonal bisecta los ángulos lo que nos dará un triangulo 90°,45°,45°, como este procesos de dibujar un cuadrado y su diagonal es fácilmente replicable tomaremos estos 2 ángulos como base para calculo posteriores.
Ahora si pensamos en un triangulo equilátero todos sus ángulos serán 60° y si dibujamos una altura tendremos un triángulos 90°,60°,30°, de manera análoga tenemos un procesos muy fácil de replicar y que toma como base un polígono regular, esto nos las los otros 2 ángulos 30° y 60°.
A estos 4 ángulos le sumaremos el caso base ósea el ángulo 0°, con este conjunto nos basaremos para generar el resto de nuestros cálculos al ser ángulos de fácil construcción.
Estos ángulos en radianes tendrán los siguientes valores

| Grados |    Radianes     | Fracción de $\pi$ | Fracción de $\tau$ |
| :----: | :-------------: | :---------------: | :----------------: |
|  $0°$  |       $0$       |        $0$        |        $0$         |
| $30°$  | $\frac{\pi}{6}$ | $\frac{1}{6}\pi$  | $\frac{1}{12}\tau$ |
| $45°$  | $\frac{\pi}{4}$ | $\frac{1}{4}\pi$  | $\frac{1}{8}\tau$  |
| $60°$  | $\frac{\pi}{3}$ | $\frac{1}{3}\pi$  | $\frac{1}{6}\tau$  |
| $90°$  | $\frac{\pi}{2}$ | $\frac{1}{2}\pi$  | $\frac{1}{4}\tau$  |

Ahora, si llevamos estas ideas al plano $\mathbb{R}^2$, vemos cómo estos ángulos están contenidos en el primer cuadrante. Si quisiéramos extender esto a los demás cuadrantes, podemos hacer reflexiones de estos ángulos: para el segundo cuadrante se hace una reflexión respecto al eje $Y$; para el tercer cuadrante, respecto al origen; y para el cuarto cuadrante, respecto al eje $X$.
Con esto podemos crear una tabla ampliada con los ángulos notables en todos los cuadrantes:

| Grados |     Radianes      | Fracción de $\pi$ | Fracción de $\tau$  |
| :----: | :---------------: | :---------------: | :-----------------: |
|  $0°$  |        $0$        |        $0$        |         $0$         |
| $30°$  |  $\frac{\pi}{6}$  | $\frac{1}{6}\pi$  | $\frac{1}{12}\tau$  |
| $45°$  |  $\frac{\pi}{4}$  | $\frac{1}{4}\pi$  |  $\frac{1}{8}\tau$  |
| $60°$  |  $\frac{\pi}{3}$  | $\frac{1}{3}\pi$  |  $\frac{1}{6}\tau$  |
| $90°$  |  $\frac{\pi}{2}$  | $\frac{1}{2}\pi$  |  $\frac{1}{4}\tau$  |
| $120°$ | $\frac{2\pi}{3}$  | $\frac{2}{3}\pi$  |  $\frac{1}{3}\tau$  |
| $135°$ | $\frac{3\pi}{4}$  | $\frac{3}{4}\pi$  |  $\frac{3}{8}\tau$  |
| $150°$ | $\frac{5\pi}{6}$  | $\frac{5}{6}\pi$  | $\frac{5}{12}\tau$  |
| $180°$ |       $\pi$       |       $\pi$       |  $\frac{1}{2}\tau$  |
| $210°$ | $\frac{7\pi}{6}$  | $\frac{7}{6}\pi$  | $\frac{7}{12}\tau$  |
| $225°$ | $\frac{5\pi}{4}$  | $\frac{5}{4}\pi$  |  $\frac{5}{8}\tau$  |
| $240°$ | $\frac{4\pi}{3}$  | $\frac{4}{3}\pi$  |  $\frac{2}{3}\tau$  |
| $270°$ | $\frac{3\pi}{2}$  | $\frac{3}{2}\pi$  |  $\frac{3}{4}\tau$  |
| $300°$ | $\frac{5\pi}{3}$  | $\frac{5}{3}\pi$  |  $\frac{5}{6}\tau$  |
| $315°$ | $\frac{7\pi}{4}$  | $\frac{7}{4}\pi$  |  $\frac{7}{8}\tau$  |
| $330°$ | $\frac{11\pi}{6}$ | $\frac{11}{6}\pi$ | $\frac{11}{12}\tau$ |
| $360°$ |      $2\pi$       |      $2\pi$       |       $\tau$        |

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
Siguen la misma logica que los grados sexagesimales, solo que en vez de dividir la circunferencia en 360° se hace en 400, por lo tanto un **gradián** o **gon** ($\text{g}$ o $\text{gon}$) es $\frac{1}{400}$ de una rotación completa.

**Relación:**
$$400^g = 360° = 2\pi \text{ rad}$$

**Conversión:**
$$\text{gradianes} = \text{grados} \times \frac{400}{360} = \text{grados} \times \frac{10}{9}$$

**Ejemplo 2.2:**
$$90° = 90 \times \frac{10}{9} = 100^g$$

**Observación:** Los gradianes se utilizan principalmente en topografía, geodesia y navegación. Su ventaja es que el ángulo recto mide exactamente $100^g$. En este curso trabajaremos principalmente con **grados** y **radianes**.



---

## 3. Razones trigonométricas en el triángulo rectángulo

Las razones trigonométricas son nuestro principal objeto de estudio en esta clase. Son una forma de relacionar los ángulos con los lados de un triángulo rectángulo y, dado que se construyen a partir de ellos, solo funcionan en este contexto.

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

Vamos a definir las razones trigonométricas como:

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

Además podemos definir las razones trigonométricas recíprocas:

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
Pensemos en un cuadrado de lados iguales a 1 unidad: si trazamos una diagonal obtendremos un triángulo rectángulo con ambos catetos iguales a 1; su hipotenusa, por el teorema de Pitágoras, medirá $\sqrt{1^2+1^2}=\sqrt{2}$, y sus ángulos serán 90°–45°–45°. Con esto podemos obtener los valores de las funciones trigonométricas:

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

$$\sin(45°) = \frac{\text{opuesto}}{\text{hipotenusa}} = \frac{1}{\sqrt{2}} = \frac{\sqrt{2}}{2}$$
$$\cos(45°) = \frac{\text{adyacente}}{\text{hipotenusa}} = \frac{\sqrt{2}}{2}$$
$$\tan(45°) = \frac{\sin(45°)}{\cos(45°)} = 1$$

Con esto vemos que $\sin(45°) = \cos(45°)$

**Triángulo de 30°-60°-90°:**
Pensemos en un triángulo equilátero de lados iguales a 2: si trazamos una altura obtendremos un triángulo rectángulo con cateto igual a 1 e hipotenusa igual a 2. Por Pitágoras, el otro cateto medirá $1^2+x^2=2^2 \Rightarrow x^2=4-1 \Rightarrow x=\sqrt{3}$:

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

> **Observación (invarianza de las razones trigonométricas):** Los valores de las razones trigonométricas dependen únicamente del ángulo, no del tamaño del triángulo. Es decir, $\sin\!\left(\dfrac{\pi}{6}\right)$ siempre vale $\dfrac{1}{2}$, independientemente de cuán grande o pequeño sea el triángulo rectángulo en el que se mida.

**Demostración:** Sean dos triángulos rectángulos con el mismo ángulo agudo $\theta$ pero de distintos tamaños. Por el criterio de semejanza AA (ángulo-ángulo), ambos triángulos son semejantes, por lo que sus lados son proporcionales. Si los lados del segundo triángulo son $k$ veces los del primero, entonces:
$$\sin(\theta) = \frac{k \cdot \text{opuesto}}{k \cdot \text{hipotenusa}} = \frac{\text{opuesto}}{\text{hipotenusa}}$$
El factor $k$ cancela en el cociente, demostrando que el valor no depende del tamaño del triángulo. $\blacksquare$

**Ejemplo 3.2 (invarianza):**
Consideremos dos triángulos rectángulos con ángulo $30°$:
- Triángulo 1: hipotenusa $2$, opuesto $1$ → $\sin(30°) = \dfrac{1}{2}$
- Triángulo 2: hipotenusa $10$, opuesto $5$ → $\sin(30°) = \dfrac{5}{10} = \dfrac{1}{2}$

El resultado es idéntico en ambos casos.

**Caso particular: $0°$ y $90°$**

Pensemos en un triángulo $90°$-$60°$-$30°$. Si tomamos el ángulo de $60°$ y trazamos sucesivas bisectrices, generamos triángulos con ángulos cada vez más pequeños: $30°$, $15°$, $7.5°$, etc. Al analizar este proceso, el cateto opuesto se reduce progresivamente, el cateto adyacente se mantiene aproximadamente constante y la hipotenusa se acerca cada vez más al cateto adyacente.

En el límite de este proceso, el "triángulo" degenera en un segmento con ángulo $0°$: el cateto opuesto colapsa a $0$ y la hipotenusa coincide con el cateto adyacente. Con esto:

$$\sin(0°) = \frac{0}{\text{hipotenusa}} = 0, \qquad \cos(0°) = \frac{\text{adyacente}}{\text{hipotenusa}} = 1, \qquad \tan(0°) = \frac{0}{1} = 0$$

De forma análoga, si el ángulo de interés crece hasta $90°$, el cateto adyacente colapsa a $0$ y el cateto opuesto coincide con la hipotenusa:

$$\sin(90°) = \frac{\text{hipotenusa}}{\text{hipotenusa}} = 1, \qquad \cos(90°) = \frac{0}{\text{hipotenusa}} = 0, \qquad \tan(90°) = \frac{1}{0} = \text{indefinido}$$

### 4.2 Tabla de valores para ángulos notables

**Tabla básica (seno, coseno, tangente):**

| $\theta$ | $0°$ | $30°$ | $45°$ | $60°$ | $90°$ |
|----------|------|-------|-------|-------|-------|
| **Radianes** | $0$ | $\frac{\pi}{6}$ | $\frac{\pi}{4}$ | $\frac{\pi}{3}$ | $\frac{\pi}{2}$ |
| $\sin(\theta)$ | $0$ | $\frac{1}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{\sqrt{3}}{2}$ | $1$ |
| $\cos(\theta)$ | $1$ | $\frac{\sqrt{3}}{2}$ | $\frac{\sqrt{2}}{2}$ | $\frac{1}{2}$ | $0$ |
| $\tan(\theta)$ | $0$ | $\frac{\sqrt{3}}{3}$ | $1$ | $\sqrt{3}$ | indefinido |

### 4.3 Mnemotecnia: La “canción brasileña”

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

Hasta ahora hemos trabajado con ángulos agudos (entre $0$ y $\pi/2$). Para extender las funciones trigonométricas a todos los ángulos, utilizamos el **círculo unitario** y consideramos los cuatro cuadrantes del plano cartesiano.

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

**Cuadrante I** ($0 < \theta < \frac{\pi}{2}$) ($0° < \theta < 90°$):
- $\sin(\theta) > 0$ (coordenada y positiva)
- $\cos(\theta) > 0$ (coordenada x positiva)
- $\tan(\theta) > 0$
- **Todas las funciones son positivas**

**Cuadrante II** ($\frac{\pi}{2} < \theta < \pi$) ($90° < \theta < 180°$):
- $\sin(\theta) > 0$ (coordenada y positiva)
- $\cos(\theta) < 0$ (coordenada x negativa)
- $\tan(\theta) < 0$
- **Solo seno y cosecante son positivos**

**Cuadrante III** ($\pi < \theta < \frac{3\pi}{2}$) ($180° < \theta < 270°$):
- $\sin(\theta) < 0$ (coordenada y negativa)
- $\cos(\theta) < 0$ (coordenada x negativa)
- $\tan(\theta) > 0$
- **Solo tangente y cotangente son positivos**

**Cuadrante IV** ($\frac{3\pi}{2} < \theta < 2\pi$) ($270° < \theta < 360°$):
- $\sin(\theta) < 0$ (coordenada y negativa)
- $\cos(\theta) > 0$ (coordenada x positiva)
- $\tan(\theta) < 0$
- **Solo coseno y secante son positivos**

**Mnemotecnia - "TOSENTACOS":**
```
      S     |   Todos
   (Seno)   | (Todos)
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

**En radianes:**

a) $\theta = \dfrac{5\pi}{6}$: Cuadrante II → $\theta' = \pi - \dfrac{5\pi}{6} = \dfrac{\pi}{6}$

b) $\theta = \dfrac{5\pi}{4}$: Cuadrante III → $\theta' = \dfrac{5\pi}{4} - \pi = \dfrac{\pi}{4}$

c) $\theta = \dfrac{7\pi}{4}$: Cuadrante IV → $\theta' = 2\pi - \dfrac{7\pi}{4} = \dfrac{\pi}{4}$

**Ejemplo 4.4:**
Calcule $\sin(150°)$:

- Cuadrante II: seno es positivo
- Ángulo de referencia: $30°$
- $\sin(150°) = +\sin(30°) = \dfrac{1}{2}$

**En radianes:**
Calcule $\sin\!\left(\dfrac{5\pi}{6}\right)$:

- Cuadrante II: seno es positivo
- Ángulo de referencia: $\dfrac{\pi}{6}$
- $\sin\!\left(\dfrac{5\pi}{6}\right) = +\sin\!\left(\dfrac{\pi}{6}\right) = \dfrac{1}{2}$

**Ejemplo 4.5:**
Calcule $\cos(225°)$:

- Cuadrante III: coseno es negativo
- Ángulo de referencia: $45°$
- $\cos(225°) = -\cos(45°) = -\dfrac{\sqrt{2}}{2}$

**En radianes:**
Calcule $\cos\!\left(\dfrac{5\pi}{4}\right)$:

- Cuadrante III: coseno es negativo
- Ángulo de referencia: $\dfrac{\pi}{4}$
- $\cos\!\left(\dfrac{5\pi}{4}\right) = -\cos\!\left(\dfrac{\pi}{4}\right) = -\dfrac{\sqrt{2}}{2}$

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

1. **Periodicidad:** Las funciones trigonométricas se repiten cada $2\pi$ radianes (o $360°$):
   - $\sin(\theta + 2\pi) = \sin(\theta)$
   - $\cos(\theta + 2\pi) = \cos(\theta)$
   - $\tan(\theta + \pi) = \tan(\theta)$ (período de $\pi$ para tangente)

2. **Simetría:**
   - Los valores de $\sin(\theta)$ tienen simetría respecto al eje Y
   - Los valores de $\cos(\theta)$ tienen simetría respecto al eje X
   - Los ángulos complementarios suman $\pi/2$: $\sin(\theta) = \cos(\pi/2 - \theta)$
   - Los ángulos suplementarios suman $\pi$: $\sin(\theta) = \sin(\pi - \theta)$

3. **Patrón de referencia:**
   - Todos los valores se obtienen a partir de los ángulos básicos: $\pi/6$, $\pi/4$, $\pi/3$
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

> Los signos de las funciones en cada cuadrante y los valores en los ángulos de ejes (0°, 90°, 180°, 270°, 360°) ya fueron detallados en la **§4.5** y en la tabla de la **§4.5**.

---

## 6. Identidades trigonométricas fundamentales

Una identidad trigonométrica es una equivalencia entre dos expresiones; por ejemplo, en aritmética, las fracciones $2/3$ y $4/6$ son equivalentes, entonces la expresión $2/3=4/6$ es una identidad aritmética. Con esta idea desarrollaremos expresiones trigonométricas equivalentes. 
Sean $f(\theta_1,\theta_2,...,\theta_n)$ y $g(\theta_1,\theta_2,...,\theta_n)$ dos expresiones que involucran funciones trigonométricas. La afirmación:
$$f(\theta_1,\theta_2,...,\theta_n) = g(\theta_1,\theta_2,...,\theta_n)$$
es una identidad trigonométrica si y solo si la igualdad es verdadera para todo valor de $\theta_1,\theta_2,...,\theta_n$ perteneciente al dominio donde ambas expresiones están definidas

Comenzaremos con la identidad más importante, la identidad pitagórica:
### 6.1 Identidad pitagórica

**Teorema 6.1 (Identidad fundamental):**
$$\cos^2(\theta) + \sin^2(\theta) = 1$$

**Demostración:** Consideremos un triangulo rectángulo, por el teorema de Pitágoras tenemos que
$$CA^2+CO^2=H^2$$
donde CA es el cateto adyacente, CO es el cateto opuesto y H es la hipotenusa, ahora usando las definiciones de las operaciones trigonométricas
$$\cos(\theta) = \frac{CA}{H} \Rightarrow H \cdot \cos(\theta) = CA$$
$$\sin(\theta) = \frac{CO}{H} \Rightarrow H \cdot \sin(\theta) = CO$$
reemplazando estos valores en el teorema de Pitágoras tendremos que:
$$(H \cdot \cos(\theta))^2 + (H \cdot \sin(\theta))^2= H^2$$
$$H^2 \cdot \cos^2(\theta) + H^2 \cdot \sin^2(\theta)= H^2$$
Dividiendo todo por $H^2$ tenemos:
$$\cos^2(\theta) + \sin^2(\theta) = 1$$

Vemos que esta expresión es independiente del ángulo $\theta$

**Notación:** $\sin^2(\theta)$ significa $(\sin(\theta))^2=\sin(\theta) \cdot \sin(\theta)$

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

### 6.2 Identidades de ángulos coterminales y negativos

**Identidad 6.3 (Periodicidad):**
$$\sin(\theta + 2\pi) = \sin(\theta)$$
$$\cos(\theta + 2\pi) = \cos(\theta)$$
$$\tan(\theta + \pi) = \tan(\theta)$$

**Identidad 6.4 (Ángulos negativos):**
$$\sin(-\theta) = -\sin(\theta)$$ (función impar)
$$\cos(-\theta) = \cos(\theta)$$ (función par)
$$\tan(-\theta) = -\tan(\theta)$$ (función impar)

### 6.3 Identidades de ángulos complementarios

**Identidad 6.5:**
$$\sin\!\left(\frac{\pi}{2} - \theta\right) = \cos(\theta)$$
$$\cos\!\left(\frac{\pi}{2} - \theta\right) = \sin(\theta)$$
$$\tan\!\left(\frac{\pi}{2} - \theta\right) = \cot(\theta)$$

**Ejemplo 6.1:**
$$\sin(\pi/6) = \cos(\pi/3) = \frac{1}{2}$$
$$\cos(\pi/6) = \sin(\pi/3) = \frac{\sqrt{3}}{2}$$

---

*NOTA*: Las siguientes identidades son muy útiles al momento de manipular ángulos y para resolver ejercicios. Sus demostraciones pueden hacerse con argumentos geométricos, pero son muy extensas; otra forma de demostrarlas es mediante el uso de números complejos, que es mucho más simple y elegante, pero ese tema se tocará en el curso de Álgebra I.

### 6.4 Identidades de suma y diferencia

**Teorema 6.2 (Fórmulas de suma y diferencia):**

$$\sin(\alpha \pm \beta) = \sin(\alpha)\cos(\beta) \pm \cos(\alpha)\sin(\beta)$$
$$\cos(\alpha \pm \beta) = \cos(\alpha)\cos(\beta) \mp \sin(\alpha)\sin(\beta)$$
$$\tan(\alpha \pm \beta) = \frac{\tan(\alpha) \pm \tan(\beta)}{1 \mp \tan(\alpha)\tan(\beta)}$$

> **Nota sobre la notación $\pm/\mp$:** Cada fórmula condensa dos identidades en una sola expresión. El signo superior corresponde siempre a la **suma** ($\alpha + \beta$) y el inferior a la **diferencia** ($\alpha - \beta$). El símbolo $\mp$ indica que el signo se **invierte** respecto al del lado izquierdo: cuando afuera hay $+$, adentro hay $-$, y viceversa. Por ejemplo, en el coseno: $\cos(\alpha + \beta) = \cos\alpha\cos\beta - \sin\alpha\sin\beta$ (signo inferior), y $\cos(\alpha - \beta) = \cos\alpha\cos\beta + \sin\alpha\sin\beta$ (signo superior).

**Ejemplo 6.2:**
Calcule $\sin\!\left(\dfrac{5\pi}{12}\right)$ usando $\dfrac{5\pi}{12} = \dfrac{\pi}{4} + \dfrac{\pi}{6}$:

$$\begin{align}
\sin\!\left(\frac{5\pi}{12}\right) &= \sin\!\left(\frac{\pi}{4} + \frac{\pi}{6}\right) \\
&= \sin\!\left(\frac{\pi}{4}\right)\cos\!\left(\frac{\pi}{6}\right) + \cos\!\left(\frac{\pi}{4}\right)\sin\!\left(\frac{\pi}{6}\right) \\
&= \frac{\sqrt{2}}{2} \cdot \frac{\sqrt{3}}{2} + \frac{\sqrt{2}}{2} \cdot \frac{1}{2} \\
&= \frac{\sqrt{6}}{4} + \frac{\sqrt{2}}{4} \\
&= \frac{\sqrt{6} + \sqrt{2}}{4}
\end{align}$$

### 6.5 Identidades de ángulo doble

**Teorema 6.3 (Ángulo doble):**
$$\sin(2\theta) = 2\sin(\theta)\cos(\theta)$$
$$\cos(2\theta) = \cos^2(\theta) - \sin^2(\theta)$$

**Formas alternativas de $\cos(2\theta)$:**
$$\cos(2\theta) = 2\cos^2(\theta) - 1 = 1 - 2\sin^2(\theta)$$

$$\tan(2\theta) = \frac{2\tan(\theta)}{1 - \tan^2(\theta)}$$

**Demostración:**

La idea es interpretar $2\theta$ como la suma $\theta + \theta$ y aplicar directamente las fórmulas de suma de ángulos.

*Seno:*
$$\sin(2\theta) = \sin(\theta + \theta) = \sin(\theta)\cos(\theta) + \cos(\theta)\sin(\theta) = 2\sin(\theta)\cos(\theta) \quad \blacksquare$$

*Coseno:*
$$\cos(2\theta) = \cos(\theta + \theta) = \cos(\theta)\cos(\theta) - \sin(\theta)\sin(\theta) = \cos^2(\theta) - \sin^2(\theta) \quad \blacksquare$$

Las formas alternativas se obtienen sustituyendo la identidad pitagórica $\sin^2(\theta) = 1 - \cos^2(\theta)$ o $\cos^2(\theta) = 1 - \sin^2(\theta)$:
$$\cos^2(\theta) - \sin^2(\theta) = \cos^2(\theta) - (1 - \cos^2(\theta)) = 2\cos^2(\theta) - 1$$
$$\cos^2(\theta) - \sin^2(\theta) = (1 - \sin^2(\theta)) - \sin^2(\theta) = 1 - 2\sin^2(\theta)$$

*Tangente:*
$$\tan(2\theta) = \tan(\theta + \theta) = \frac{\tan(\theta) + \tan(\theta)}{1 - \tan(\theta)\tan(\theta)} = \frac{2\tan(\theta)}{1 - \tan^2(\theta)} \quad \blacksquare$$

**Ejemplo 6.3:**
Si $\sin(\theta) = \frac{3}{5}$ y $\theta$ está en el primer cuadrante, calcule $\sin(2\theta)$:

Primero encontramos $\cos(\theta)$ usando $\sin^2(\theta) + \cos^2(\theta) = 1$:
$$\cos(\theta) = \sqrt{1 - \sin^2(\theta)} = \sqrt{1 - \frac{9}{25}} = \sqrt{\frac{16}{25}} = \frac{4}{5}$$

Ahora:
$$\sin(2\theta) = 2\sin(\theta)\cos(\theta) = 2 \cdot \frac{3}{5} \cdot \frac{4}{5} = \frac{24}{25}$$

### 6.6 Identidades de ángulo medio

Las identidades de ángulo medio se obtienen directamente a partir de las formas alternativas de $\cos(2\theta)$.

**Derivación:**

A partir de $\cos(2\alpha) = 1 - 2\sin^2(\alpha)$, despejando $\sin^2(\alpha)$:
$$\sin^2(\alpha) = \frac{1 - \cos(2\alpha)}{2}$$

Haciendo la sustitución $\alpha = \dfrac{\theta}{2}$:
$$\sin^2\!\left(\frac{\theta}{2}\right) = \frac{1 - \cos(\theta)}{2}$$

De forma análoga, a partir de $\cos(2\alpha) = 2\cos^2(\alpha) - 1$:
$$\cos^2\!\left(\frac{\theta}{2}\right) = \frac{1 + \cos(\theta)}{2}$$

Tomando raíz cuadrada en ambos casos se obtienen las identidades del ángulo medio:

**Teorema 6.4 (Ángulo medio):**

$$\sin\!\left(\frac{\theta}{2}\right) = \pm\sqrt{\frac{1 - \cos(\theta)}{2}}$$

$$\cos\!\left(\frac{\theta}{2}\right) = \pm\sqrt{\frac{1 + \cos(\theta)}{2}}$$

$$\tan\!\left(\frac{\theta}{2}\right) = \pm\sqrt{\frac{1 - \cos(\theta)}{1 + \cos(\theta)}} = \frac{\sin(\theta)}{1 + \cos(\theta)} = \frac{1 - \cos(\theta)}{\sin(\theta)}$$

> **Nota sobre el signo:** El signo $(\pm)$ depende del cuadrante en el que se encuentre $\dfrac{\theta}{2}$. Las formas con seno y coseno en el denominador para $\tan$ no requieren signo externo, ya que el signo queda determinado automáticamente por los valores de $\sin(\theta)$ y $\cos(\theta)$.

**Ejemplo 6.4:**
Calcule $\cos\!\left(\dfrac{\pi}{12}\right)$ utilizando la identidad del ángulo medio con $\theta = \dfrac{\pi}{6}$.

Como $\dfrac{\pi}{12} = \dfrac{\pi/6}{2}$ y $\dfrac{\pi}{12}$ está en el primer cuadrante, el coseno es positivo:

$$\cos\!\left(\frac{\pi}{12}\right) = \sqrt{\frac{1 + \cos\!\left(\dfrac{\pi}{6}\right)}{2}} = \sqrt{\frac{1 + \dfrac{\sqrt{3}}{2}}{2}} = \sqrt{\frac{\dfrac{2 + \sqrt{3}}{2}}{2}} = \sqrt{\frac{2 + \sqrt{3}}{4}} = \frac{\sqrt{2 + \sqrt{3}}}{2}$$

> **Observación:** El mismo resultado puede obtenerse usando la fórmula de diferencia de ángulos, ya que $\dfrac{\pi}{12} = \dfrac{\pi}{4} - \dfrac{\pi}{6}$:
> $$\cos\!\left(\frac{\pi}{4} - \frac{\pi}{6}\right) = \cos\!\left(\frac{\pi}{4}\right)\cos\!\left(\frac{\pi}{6}\right) + \sin\!\left(\frac{\pi}{4}\right)\sin\!\left(\frac{\pi}{6}\right) = \frac{\sqrt{2}}{2}\cdot\frac{\sqrt{3}}{2} + \frac{\sqrt{2}}{2}\cdot\frac{1}{2} = \frac{\sqrt{6}+\sqrt{2}}{4}$$
> Ambas expresiones son equivalentes: $\dfrac{\sqrt{2+\sqrt{3}}}{2} = \dfrac{\sqrt{6}+\sqrt{2}}{4}$.

**Ejemplo 6.5:**
Si $\cos(\theta) = \dfrac{3}{5}$ y $\theta$ está en el primer cuadrante, calcule $\sin\!\left(\dfrac{\theta}{2}\right)$.

Como $0 < \theta < \dfrac{\pi}{2}$, se tiene $0 < \dfrac{\theta}{2} < \dfrac{\pi}{4}$, por lo tanto $\dfrac{\theta}{2}$ también está en el primer cuadrante y el seno es positivo:

$$\sin\!\left(\frac{\theta}{2}\right) = \sqrt{\frac{1 - \cos(\theta)}{2}} = \sqrt{\frac{1 - \dfrac{3}{5}}{2}} = \sqrt{\frac{\dfrac{2}{5}}{2}} = \sqrt{\frac{1}{5}} = \frac{1}{\sqrt{5}} = \frac{\sqrt{5}}{5}$$




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
Verificar: $\frac{\sin(\theta)}{1 + \cos(\theta)} = \frac{1 - \cos(\theta)}{\sin(\theta)}$

**Solución:** Multiplicamos cruzado o verificamos multiplicando el denominador de la izquierda por el numerador de la derecha:
$$\sin(\theta) \cdot \sin(\theta) = (1 + \cos(\theta))(1 - \cos(\theta))$$
$$\sin^2(\theta) = 1 - \cos^2(\theta)$$
$$\sin^2(\theta) = \sin^2(\theta)$$ ✓

---

## 8. Funciones trigonométricas

Todas las razones trigonométricas también podemos trabajarlas como si fueran funciones, solo debemos considerar un ángulo $X$ como nuestras variable (medida en radianes para usar la misma recta real que hemos usado) y con esto podemos estudiar el comportamiento con las herramientas que ya hemos estudiado.

### 8.1 La función seno

**Definición 8.1:**
$$f(x) = \sin(x)$$

Primero para estudiar las propiedades de esta funciones haremos una tabla de valores, ayudándonos de los ángulos notables y las identidades calcularemos varios valores

|     $x$ (rad)      |     $x$ ($\tau$)     | $x$ (°) |               $\sin(x)$               |      Valor exacto      |
| :----------------: | :------------------: | :-----: | :-----------------------------------: | :--------------------: |
|        $0$         |         $0$          |  $0°$   |               $\sin(0)$               |          $0$           |
|  $\dfrac{\pi}{6}$  |  $\dfrac{\tau}{12}$  |  $30°$  |  $\sin\!\left(\dfrac{\pi}{6}\right)$  |     $\dfrac{1}{2}$     |
|  $\dfrac{\pi}{4}$  |  $\dfrac{\tau}{8}$   |  $45°$  |  $\sin\!\left(\dfrac{\pi}{4}\right)$  | $\dfrac{\sqrt{2}}{2}$  |
|  $\dfrac{\pi}{3}$  |  $\dfrac{\tau}{6}$   |  $60°$  |  $\sin\!\left(\dfrac{\pi}{3}\right)$  | $\dfrac{\sqrt{3}}{2}$  |
|  $\dfrac{\pi}{2}$  |  $\dfrac{\tau}{4}$   |  $90°$  |  $\sin\!\left(\dfrac{\pi}{2}\right)$  |          $1$           |
| $\dfrac{2\pi}{3}$  |  $\dfrac{\tau}{3}$   | $120°$  | $\sin\!\left(\dfrac{2\pi}{3}\right)$  | $\dfrac{\sqrt{3}}{2}$  |
| $\dfrac{3\pi}{4}$  |  $\dfrac{3\tau}{8}$  | $135°$  | $\sin\!\left(\dfrac{3\pi}{4}\right)$  | $\dfrac{\sqrt{2}}{2}$  |
| $\dfrac{5\pi}{6}$  | $\dfrac{5\tau}{12}$  | $150°$  | $\sin\!\left(\dfrac{5\pi}{6}\right)$  |     $\dfrac{1}{2}$     |
|       $\pi$        |  $\dfrac{\tau}{2}$   | $180°$  |              $\sin(\pi)$              |          $0$           |
| $\dfrac{7\pi}{6}$  | $\dfrac{7\tau}{12}$  | $210°$  | $\sin\!\left(\dfrac{7\pi}{6}\right)$  |    $-\dfrac{1}{2}$     |
| $\dfrac{5\pi}{4}$  |  $\dfrac{5\tau}{8}$  | $225°$  | $\sin\!\left(\dfrac{5\pi}{4}\right)$  | $-\dfrac{\sqrt{2}}{2}$ |
| $\dfrac{4\pi}{3}$  |  $\dfrac{2\tau}{3}$  | $240°$  | $\sin\!\left(\dfrac{4\pi}{3}\right)$  | $-\dfrac{\sqrt{3}}{2}$ |
| $\dfrac{3\pi}{2}$  |  $\dfrac{3\tau}{4}$  | $270°$  | $\sin\!\left(\dfrac{3\pi}{2}\right)$  |          $-1$          |
| $\dfrac{5\pi}{3}$  |  $\dfrac{5\tau}{6}$  | $300°$  | $\sin\!\left(\dfrac{5\pi}{3}\right)$  | $-\dfrac{\sqrt{3}}{2}$ |
| $\dfrac{7\pi}{4}$  |  $\dfrac{7\tau}{8}$  | $315°$  | $\sin\!\left(\dfrac{7\pi}{4}\right)$  | $-\dfrac{\sqrt{2}}{2}$ |
| $\dfrac{11\pi}{6}$ | $\dfrac{11\tau}{12}$ | $330°$  | $\sin\!\left(\dfrac{11\pi}{6}\right)$ |    $-\dfrac{1}{2}$     |
|       $2\pi$       |        $\tau$        | $360°$  |             $\sin(2\pi)$              |          $0$           |
primer dibujo

con esto ya nos podemos hacer una idea de la grafica pero si usamos las identidades para obtener mas valores podemos hacer un mejor bosquejo del grafico

segundo dibujo


Con esto ya nos podemos dar una idea de como será la grafica de la función

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


**Propiedades:**
- **Dominio:** $(-\infty, +\infty)$
- **Imagen:** $[-1, 1]$
- **Período:** $2\pi$ (la función se repite cada $2\pi$)
- **Simetría:** Función impar ($\sin(-x) = -\sin(x)$)
- **Ceros:** $x = n\pi$, donde $n \in \mathbb{Z}$
- **Máximos:** $x = \frac{\pi}{2} + 2n\pi$, valor $1$
- **Mínimos:** $x = \frac{3\pi}{2} + 2n\pi$, valor $-1$


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

## 11. Teorema del seno y del coseno

Hasta ahora hemos usado la trigonometría principalmente en triángulos **rectángulos**, donde tenemos la comodidad de un ángulo de $90°$ que simplifica todo. Pero ¿qué pasa cuando el triángulo no tiene ningún ángulo recto? Por ejemplo, si queremos calcular la distancia entre dos puntos conociendo ciertos ángulos, o encontrar un lado de un terreno triangular donde ningún ángulo es recto.

Para eso existen dos herramientas fundamentales que generalizan la trigonometría a **cualquier triángulo**: el **teorema del seno** y el **teorema del coseno**.

### 11.1 Notación para triángulos generales

Antes de enunciar los teoremas, establecemos la notación estándar para un triángulo general $ABC$:

- Los **vértices** se denotan con letras mayúsculas: $A$, $B$, $C$
- Los **ángulos** interiores en cada vértice se denotan con letras griegas: $\alpha$ (en $A$), $\beta$ (en $B$), $\gamma$ (en $C$)
- El **lado opuesto** a cada vértice se denota con la letra minúscula correspondiente: $a$ opuesto a $A$, $b$ opuesto a $B$, $c$ opuesto a $C$

Se cumple siempre:
$$\alpha + \beta + \gamma = 180° = \pi$$

### 11.2 Teorema del seno

#### Motivación

Intuitivamente, en cualquier triángulo un lado más largo está "enfrentado" a un ángulo más grande. El teorema del seno cuantifica exactamente esa relación: la razón entre cada lado y el seno del ángulo opuesto es siempre la misma.

**Teorema 11.1 (Ley de senos):**

En todo triángulo $ABC$ con lados $a$, $b$, $c$ opuestos a los ángulos $\alpha$, $\beta$, $\gamma$ respectivamente:

$$\frac{a}{\sin(\alpha)} = \frac{b}{\sin(\beta)} = \frac{c}{\sin(\gamma)} = 2R$$

donde $R$ es el radio del **circuncírculo** (la circunferencia que pasa por los tres vértices).

**Demostración:**

Trazamos la altura $h$ desde el vértice $C$ hasta el lado $c$. Esto genera dos triángulos rectángulos:

En el triángulo que contiene a $\alpha$:
$$\sin(\alpha) = \frac{h}{b} \Rightarrow h = b\sin(\alpha)$$

En el triángulo que contiene a $\beta$:
$$\sin(\beta) = \frac{h}{a} \Rightarrow h = a\sin(\beta)$$

Igualando ambas expresiones:
$$b\sin(\alpha) = a\sin(\beta) \Rightarrow \frac{a}{\sin(\alpha)} = \frac{b}{\sin(\beta)}$$

Repitiendo el argumento con la altura desde $B$ se obtiene $\dfrac{b}{\sin(\beta)} = \dfrac{c}{\sin(\gamma)}$, completando la igualdad triple. $\blacksquare$

**Ejemplo 11.1:**
En un triángulo $ABC$, $\alpha = 30°$, $\beta = 45°$ y $a = 8$. Calcule $b$.

Por la ley de senos:
$$b = a \cdot \frac{\sin(\beta)}{\sin(\alpha)} = 8 \cdot \frac{\sin(45°)}{\sin(30°)} = 8 \cdot \frac{\dfrac{\sqrt{2}}{2}}{\dfrac{1}{2}} = 8\sqrt{2}$$

**Ejemplo 11.2:**
En un triángulo, $\beta = \dfrac{\pi}{6}$, $\gamma = \dfrac{\pi}{4}$ y $b = 10$. Calcule $c$ y el ángulo $\alpha$.

Primero encontramos $\alpha$:
$$\alpha = \pi - \frac{\pi}{6} - \frac{\pi}{4} = \pi - \frac{2\pi}{12} - \frac{3\pi}{12} = \frac{7\pi}{12}$$

Luego por la ley de senos:
$$c = b \cdot \frac{\sin(\gamma)}{\sin(\beta)} = 10 \cdot \frac{\sin\!\left(\dfrac{\pi}{4}\right)}{\sin\!\left(\dfrac{\pi}{6}\right)} = 10 \cdot \frac{\dfrac{\sqrt{2}}{2}}{\dfrac{1}{2}} = 10\sqrt{2}$$

> **Caso ambiguo (SSA):** Cuando se conocen dos lados y el ángulo opuesto a uno de ellos, puede haber **0, 1 o 2 triángulos** posibles. Se debe verificar si el valor de $\sin$ calculado cae en $[-1,1]$ y analizar si el ángulo admite dos posiciones.

### 11.3 Teorema del coseno

#### Motivación

El teorema del coseno es una **generalización directa del teorema de Pitágoras**. Cuando el ángulo entre los dos lados conocidos es recto ($90°$), el coseno vale cero y recuperamos exactamente $c^2 = a^2 + b^2$. Para otros ángulos, el término $-2ab\cos(\gamma)$ "corrige" la fórmula: si el ángulo es agudo el tercer lado resulta menor de lo que Pitágoras indicaría, y si es obtuso, mayor.

**Teorema 11.2 (Ley de cosenos):**

En todo triángulo $ABC$:

$$a^2 = b^2 + c^2 - 2bc\cos(\alpha)$$
$$b^2 = a^2 + c^2 - 2ac\cos(\beta)$$
$$c^2 = a^2 + b^2 - 2ab\cos(\gamma)$$

**Demostración:**

Ubicamos el triángulo en el plano con $B$ en el origen y $C$ en $(a,\, 0)$. Entonces el vértice $A$ tiene coordenadas $(c\cos(\beta),\, c\sin(\beta))$.

Calculamos $b = |AC|$ usando la fórmula de distancia:
$$\begin{align}
b^2 &= (c\cos(\beta) - a)^2 + (c\sin(\beta) - 0)^2 \\
&= c^2\cos^2(\beta) - 2ac\cos(\beta) + a^2 + c^2\sin^2(\beta) \\
&= c^2\underbrace{(\cos^2(\beta) + \sin^2(\beta))}_{=\,1} + a^2 - 2ac\cos(\beta) \\
&= a^2 + c^2 - 2ac\cos(\beta) \quad \blacksquare
\end{align}$$

Las otras dos formas se obtienen por simetría ubicando los otros vértices en el origen.

> **Conexión con Pitágoras:** Si $\gamma = \dfrac{\pi}{2}$, entonces $\cos\!\left(\dfrac{\pi}{2}\right) = 0$ y la ley de cosenos se reduce a $c^2 = a^2 + b^2$.

**Ejemplo 11.3:**
En un triángulo, $a = 5$, $b = 7$ y $\gamma = 60°$. Calcule $c$.

$$c^2 = 5^2 + 7^2 - 2(5)(7)\cos(60°) = 25 + 49 - 70 \cdot \frac{1}{2} = 74 - 35 = 39$$
$$c = \sqrt{39}$$

**Ejemplo 11.4:**
Un triángulo tiene lados $a = 6$, $b = 8$ y $c = 10$. Calcule el ángulo $\gamma$.

Despejamos $\cos(\gamma)$:
$$\cos(\gamma) = \frac{a^2 + b^2 - c^2}{2ab} = \frac{36 + 64 - 100}{2(6)(8)} = \frac{0}{96} = 0 \Rightarrow \gamma = \frac{\pi}{2}$$

El triángulo es rectángulo en $C$, lo cual es consistente con $6^2 + 8^2 = 10^2$.

### 11.4 ¿Cuándo usar cada teorema?

| Datos conocidos | Teorema a usar |
|:---|:---|
| 2 ángulos y 1 lado (AAS o ASA) | Ley de senos |
| 2 lados y ángulo opuesto (SSA) | Ley de senos (verificar caso ambiguo) |
| 2 lados y el ángulo entre ellos (SAS) | Ley de cosenos |
| 3 lados (SSS) | Ley de cosenos |

---

## 12. Ejercicios propuestos

### 12.1 Conversión de ángulos

1. Convierta a radianes: $120°$, $225°$, $315°$
2. Convierta a grados: $\frac{5\pi}{6}$, $\frac{7\pi}{4}$, $\frac{11\pi}{6}$
3. Convierta $90°$ a gradianes

### 12.2 Razones trigonométricas

4. En un triángulo rectángulo con catetos $5$ y $12$, calcule las seis funciones trigonométricas del ángulo agudo menor

5. Si $\sin(\theta) = \frac{2}{3}$ y $\theta$ está en el segundo cuadrante, encuentre $\cos(\theta)$ y $\tan(\theta)$

6. Si $\tan(\theta) = -\frac{3}{4}$ y $\theta$ está en el cuarto cuadrante, encuentre $\sin(\theta)$ y $\cos(\theta)$

### 12.3 Valores exactos

7. Calcule sin usar calculadora: $\sin(150°)$, $\cos(240°)$, $\tan(135°)$

8. Evalúe: $\sin\left(\frac{7\pi}{6}\right) + \cos\left(\frac{5\pi}{3}\right)$

9. Simplifique: $\sin(30°)\cos(60°) + \cos(30°)\sin(60°)$

### 12.4 Identidades

10. Verifique: $\frac{1 - \sin^2(\theta)}{\cos(\theta)} = \cos(\theta)$

11. Verifique: $(\sin(\theta) + \cos(\theta))^2 = 1 + 2\sin(\theta)\cos(\theta)$

12. Verifique: $\frac{\tan(\theta) + \cot(\theta)}{\tan(\theta)} = \csc^2(\theta)$

13. Simplifique: $\frac{\sin^2(\theta) - \cos^2(\theta)}{\sin(\theta) - \cos(\theta)}$

### 12.5 Ecuaciones trigonométricas

14. Resuelva para $x \in [0, 2\pi)$: $\sin(x) = -\frac{\sqrt{3}}{2}$

15. Resuelva para $x \in [0, 2\pi)$: $2\cos(x) + 1 = 0$

16. Resuelva para $x \in [0, 2\pi)$: $\tan^2(x) = 3$

17. Resuelva para $x \in [0, 2\pi)$: $2\sin^2(x) + 3\sin(x) + 1 = 0$

18. Resuelva para $x \in [0, 2\pi)$: $\cos(2x) = \frac{1}{2}$

### 12.6 Aplicaciones

19. Una rueda de radio $5$ metros gira. Encuentre la parametrización de la trayectoria de un punto en el borde

20. Encuentre la ecuación del círculo de radio $4$ centrado en $(2, -1)$ en forma paramétrica

21. Una onda se describe por $f(t) = 10\sin(4\pi t - \frac{\pi}{3}) + 5$. Determine su amplitud, período, desfase y desplazamiento vertical

22. Demuestre que $\sin(3\theta) = 3\sin(\theta) - 4\sin^3(\theta)$ usando identidades de suma

23. Si $\cos(\alpha) = \frac{3}{5}$ ($\alpha$ en cuadrante I) y $\sin(\beta) = \frac{5}{13}$ ($\beta$ en cuadrante II), calcule $\sin(\alpha + \beta)$

24. Encuentre el ángulo de elevación del sol si un poste de $10$ metros proyecta una sombra de $15$ metros

25. Una escalera de $8$ metros se apoya contra una pared formando un ángulo de $60°$ con el suelo. ¿A qué altura de la pared llega la escalera?

---

**Fin de la Clase 6**

