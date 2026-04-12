# Trigonometría: Fundamentos y Aplicaciones

## 1. Triángulos y elementos básicos

### 1.1 Repaso: Triángulos rectángulos

**Definición 1.1 (Triángulo rectángulo):**
Un **triángulo rectángulo** es un triángulo que tiene un ángulo de $\pi/2$ o $90°$ (ángulo recto).

**Elementos principales:**
- **Hipotenusa:** El lado opuesto al ángulo recto (el lado más largo)
- **Catetos:** Los dos lados que forman el ángulo recto
![[triangulo_rectangulo.png|638]]
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
![[circulo_sexagesimales.jpg]]
**Subdivisiones:**
- 1 grado = 60 minutos ($60'$)
- 1 minuto = 60 segundos ($60''$)

**Ejemplos:**
- Ángulo recto: $90°00'00''$
![[angulo_recto.png]]
- Ángulo agudo: $37°15'48''$
- Ángulo con minutos y segundos: $18°56'36''$
- Ángulo obtuso: $123°42'00''$
- Ángulo completo: $360°00'00''$

**Conversión de decimal a grados-minutos-segundos:**

Un ángulo expresado en grados decimales como $37.2633...°$ se convierte así:
- La parte entera son los grados: $37°$
- La parte decimal $\times\, 60$ da los minutos: $0.2633 \times 60 = 15.8' \Rightarrow 15'$
- La parte decimal de los minutos $\times\, 60$ da los segundos: $0.8 \times 60 = 48'' $

$$37.2633...° = 37°15'48''$$

**Conversión de grados-minutos-segundos a decimal:**

$$18°56'36'' = 18 + \frac{56}{60} + \frac{36}{3600} = 18 + 0.9\overline{3} + 0.01 = 18.9433...°$$

### 2.3 Radianes

**Definición 2.3 (Radián):**
Un **radián** (rad) es el ángulo que subtiende un arco de longitud igual al radio en una circunferencia.
![[radian.png]]
Como se observa en la figura, si construimos un círculo de radio $R$ y trazamos sobre su perímetro un arco cuya longitud sea exactamente $R$, el ángulo central que subtiende dicho arco corresponde, por definición, a $1 \text{ rad}$.
Ahora nos preguntamos cuántos radianes caben en una circunferencia completa. Por la propia definicion del numero $\pi$ sabemos que la longitud de una circunferencia es $2\pi R$, por lo tanto, caben $2\pi$ radianes en una circunferencia completa.

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
### 2.5 Ángulos notables y Tabla de conversión:

Existe un grupo de ángulos llamados ángulos notables en los cuales se basan algunos de los cálculos de trigonometría, estos ángulos en sexagesimal son 30°, 45°, 60° y 90°. Estos fueron escogidos por argumentos geométricos, un cuadrado es una estructura considerada "perfecta", lados iguales y ángulos iguales, podemos considerar esta estructura un invariante pues puedo convertir cualquier cuadrado en otro simplemente aumentando o disminuyendo sus lados (una transformación suave, este término cobrará una gran relevancia más adelante) y sus ángulos siempre serán de 90°
![[cuadrado_angulos.png]]
Si dibujamos una diagonal tendremos un triángulo isósceles, por lo tanto la diagonal bisecta los ángulos lo que nos dará un triángulo de 90°,45°,45°, como este proceso de dibujar un cuadrado y su diagonal es fácilmente replicable, tomaremos estos 2 ángulos como base para cálculos posteriores.
![[cuadrado_angulo45.png]]
Ahora si pensamos en un triángulo equilátero, todos sus ángulos serán 60° y si dibujamos una altura tendremos un triángulo de 90°,60°,30°; de manera análoga, tenemos un proceso muy fácil de replicar que toma como base un polígono regular, esto nos da los otros 2 ángulos: 30° y 60°.
A estos 4 ángulos le sumaremos el caso base, o sea el ángulo 0°; con este conjunto nos basaremos para generar el resto de nuestros cálculos al ser ángulos de fácil construcción.
Estos ángulos en radianes tendrán los siguientes valores
![[triangulo_isoseles_angulos.png]]

| Grados |    Radianes     | Fracción de $\pi$ | Fracción de $\tau$ |
| :----: | :-------------: | :---------------: | :----------------: |
|  $0°$  |       $0$       |        $0$        |        $0$         |
| $30°$  | $\frac{\pi}{6}$ | $\frac{1}{6}\pi$  | $\frac{1}{12}\tau$ |
| $45°$  | $\frac{\pi}{4}$ | $\frac{1}{4}\pi$  | $\frac{1}{8}\tau$  |
| $60°$  | $\frac{\pi}{3}$ | $\frac{1}{3}\pi$  | $\frac{1}{6}\tau$  |
| $90°$  | $\frac{\pi}{2}$ | $\frac{1}{2}\pi$  | $\frac{1}{4}\tau$  |

Ahora, si llevamos estas ideas al plano $\mathbb{R}^2$, vemos cómo estos ángulos están contenidos en el primer cuadrante. Si quisiéramos extender esto a los demás cuadrantes, podemos hacer reflexiones de estos ángulos: para el segundo cuadrante se hace una reflexión respecto al eje $Y$; para el tercer cuadrante, respecto al origen; y para el cuarto cuadrante, respecto al eje $X$.
Con esto podemos crear una tabla ampliada con los ángulos notables en todos los cuadrantes:
![[angulos_notable.png]]

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

---
## 3. Razones trigonométricas en el triángulo rectángulo

Las razones trigonométricas son nuestro principal objeto de estudio en esta clase. Son una forma de relacionar los ángulos con los lados de un triángulo rectángulo y, dado que se construyen a partir de ellos, solo funcionan en este contexto.
### 3.1 Definiciones fundamentales

Dado un triángulo rectángulo con un ángulo agudo $\theta$:
![[triangulo_rectangulo_angulo.png]]
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
![[SOHCAHTOA.png|552]]
**Ejemplo 3.1:**
En un triángulo rectángulo con hipotenusa $5$, cateto opuesto $3$ y cateto adyacente $4$:
![[triangulo_3_4_5.png]]
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
![[triangulo_especial_1.png]]
$$\sin(45°) = \frac{\text{opuesto}}{\text{hipotenusa}} = \frac{1}{\sqrt{2}} = \frac{\sqrt{2}}{2}$$
$$\cos(45°) = \frac{\text{adyacente}}{\text{hipotenusa}} = \frac{\sqrt{2}}{2}$$
$$\tan(45°) = \frac{\sin(45°)}{\cos(45°)} = 1$$

Con esto vemos que $\sin(45°) = \cos(45°)$

**Triángulo de 30°-60°-90°:**
Pensemos en un triángulo equilátero de lados iguales a 2: si trazamos una altura obtendremos un triángulo rectángulo con cateto igual a 1 e hipotenusa igual a 2. Por Pitágoras, el otro cateto medirá $1^2+x^2=2^2 \Rightarrow x^2=4-1 \Rightarrow x=\sqrt{3}$:
![[triangulo_equilatero_angulos.png]]
$$\sin(30°) = \frac{1}{2}, \quad \cos(30°) = \frac{\sqrt{3}}{2}, \quad \tan(30°) = \frac{1}{\sqrt{3}} = \frac{\sqrt{3}}{3}$$
$$\sin(60°) = \frac{\sqrt{3}}{2}, \quad \cos(60°) = \frac{1}{2}, \quad \tan(60°) = \sqrt{3}$$
> **Observación (invarianza de las razones trigonométricas):** Los valores de las razones trigonométricas dependen únicamente del ángulo, no del tamaño del triángulo. Es decir, $\sin\!\left(\dfrac{\pi}{6}\right)$ siempre vale $\dfrac{1}{2}$, independientemente de cuán grande o pequeño sea el triángulo rectángulo en el que se mida.

**Demostración:** Sean dos triángulos rectángulos con el mismo ángulo agudo $\theta$ pero de distintos tamaños. Por el criterio de semejanza AA (ángulo-ángulo), ambos triángulos son semejantes, por lo que sus lados son proporcionales. Si los lados del segundo triángulo son $k$ veces los del primero, entonces:
$$\sin(\theta) = \frac{k \cdot \text{opuesto}}{k \cdot \text{hipotenusa}} = \frac{\text{opuesto}}{\text{hipotenusa}}$$
El factor $k$ cancela en el cociente, demostrando que el valor no depende del tamaño del triángulo. $\blacksquare$

**Ejemplo 3.2 (invarianza):**
Consideremos dos triángulos rectángulos con ángulo $30°$:
![[triangulo_semejante.png]]
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
![[cuadrantes.png]]
#### Signos de las funciones en cada cuadrante

Para ilustrar los signos en cada cuadrante usaremos el triángulo 3-4-5: tomamos un punto a distancia $r=5$ del origen con catetos $|x|=4$ e $|y|=3$, reflejado en los cuatro cuadrantes. Las definiciones sobre el círculo son $\sin\theta = y/r$, $\cos\theta = x/r$, $\tan\theta = y/x$.
![[angulos_R2.png]]

**Cuadrante I** ($0 < \theta < \frac{\pi}{2}$) ($0° < \theta < 90°$):
- $\sin(\theta) > 0$ (coordenada $y$ positiva)
- $\cos(\theta) > 0$ (coordenada $x$ positiva)
- $\tan(\theta) > 0$
- **Todas las funciones son positivas**

 **Ejemplo:** Punto $E=(4,\;3)$, $r=5$: $$\sin\theta = \frac{3}{5} > 0 \quad(\text{positivo}), \qquad \cos\theta = \frac{4}{5} > 0 \quad(\text{positivo}), \qquad \tan\theta = \frac{3}{4} > 0 \quad(\text{positivo})$$
**Cuadrante II** ($\frac{\pi}{2} < \theta < \pi$) ($90° < \theta < 180°$):
- $\sin(\theta) > 0$ (coordenada $y$ positiva)
- $\cos(\theta) < 0$ (coordenada $x$ negativa)
- $\tan(\theta) < 0$
- **Solo seno y cosecante son positivos**

 **Ejemplo:** Punto $F=(-4,\;3)$, $r=5$:> $$\sin\theta = \frac{3}{5} > 0 \quad(\text{positivo}), \qquad \cos\theta = \frac{-4}{5} < 0 \quad(\text{negativo}), \qquad \tan\theta = \frac{3}{-4} = -\frac{3}{4} < 0 \quad(\text{negativo})$$
**Cuadrante III** ($\pi < \theta < \frac{3\pi}{2}$) ($180° < \theta < 270°$):
- $\sin(\theta) < 0$ (coordenada $y$ negativa)
- $\cos(\theta) < 0$ (coordenada $x$ negativa)
- $\tan(\theta) > 0$
- **Solo tangente y cotangente son positivos**
  
 **Ejemplo:** Punto $G=(-4,\;-3)$, $r=5$: $$\sin\theta = \frac{-3}{5} < 0 \quad(\text{negativo}), \qquad \cos\theta = \frac{-4}{5} < 0 \quad(\text{negativo}), \qquad \tan\theta = \frac{-3}{-4} = \frac{3}{4} > 0 \quad(\text{positivo})$$
**Cuadrante IV** ($\frac{3\pi}{2} < \theta < 2\pi$) ($270° < \theta < 360°$):
- $\sin(\theta) < 0$ (coordenada $y$ negativa)
- $\cos(\theta) > 0$ (coordenada $x$ positiva)
- $\tan(\theta) < 0$
- **Solo coseno y secante son positivos**
  
**Ejemplo:** Punto $H=(4,\;-3)$, $r=5$:> $$\sin\theta = \frac{-3}{5} < 0 \quad(\text{negativo}), \qquad \cos\theta = \frac{4}{5} > 0 \quad(\text{positivo}), \qquad \tan\theta = \frac{-3}{4} < 0 \quad(\text{negativo})$$
**Mnemotecnia - "TOSENTACOS":**
![[TOSENTACOS.png]]
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

Pese a que la trigonometría clásica se origina en el estudio de los triángulos rectángulos, su marco analítico moderno presenta una interconexión estructural y geométrica irrefutable con la topología de los círculos.

**Definición 5.1 (Círculo unitario):**
El **círculo unitario** se define matemáticamente como la circunferencia de radio $1$ centrada en el origen del plano cartesiano euclidiano, descrita mediante el lugar geométrico:
$$x^2 + y^2 = 1$$
![[circulo_trigonometria.png]]
Si seleccionamos un punto arbitrario $(x,y)$ perteneciente a esta circunferencia y deseamos parametrizar sus coordenadas, podemos trazar un triángulo rectángulo cuyos catetos correspondan a las proyecciones ortogonales escalares $x$ e $y$. La hipotenusa será invariablemente equivalente al radio $R$ de la circunferencia, subtendiendo un ángulo tangencial $\theta$. Mediante este constructo geométrico analítico, deducimos que:
* $\cos(\theta) = \frac{x}{R} \implies x = R \cdot \cos(\theta)$
* $\sin(\theta) = \frac{y}{R} \implies y = R \cdot \sin(\theta)$

Para el caso axiomático particular donde $R=1$ (la amplitud de la circunferencia unitaria), el sistema de coordenadas de componentes rectangulares se simplifica isométricamente a:
$$(x,y) = (\cos(\theta), \sin(\theta))$$
De esta rigurosa formulación se desprende que la coordenada de abscisas $x$ equivale intrínsecamente al valor del coseno, mientras que la ordenada $y$ corresponde al seno. Esta equivalencia nos dota de un modelo estricto para visualizar el comportamiento dinámico de ambas funciones trigonométricas a medida que el ángulo $\theta$ sufre una variación modular continua, observando empíricamente sus valores armónicos proyectados coordenadamente.
![[circulo_parametrico.gif]]
**Definición extendida de las funciones trigonométricas:**
Dado un ángulo estandarizado $\theta$, medido con origen en el primer semi-eje de abscisas positivo (en estricto sentido de rotación analítico antihorario), se definen funcionalmente las proyecciones paramétricas como:
- El vector-punto intersectante $P = (\cos(\theta), \sin(\theta))$ en dicho perímetro del círculo unitario.
- $\sin(\theta)$ se extrae y define conceptualmente como la **coordenada geométrica de ordenadas $y$** de dicho punto autovalor $P$.
- $\cos(\theta)$ se extrae unívocamente como la **coordenada geométrica de abscisas $x$** del mismo punto $P$.
![[circulo_trigonometria_2.png]]
**Ventaja topológica y analítica:** Esta conceptualización transciende y rompe definitivamente la atadura euclidiana de poseer triángulos interiores finitos limitados, permitiendo extrapolar y dar existencia continua al campo paramétrico de las series trigonométricas sobre la totalidad y convexidad de los números reales y **todos sus ángulos** $\theta \in \mathbb{R}$ (trascendiendo espectros agudos).

> Los signos matriciales de las funciones en cada sub-espacio cuadrante y la convergencia de valores cardinales axiales (0°, 90°, 180°, 270°, 360°) se han estructurado ya con amplio rigor matemático deductivo dentro de la **§4.5**.

### 5.1 Perspectiva Geométrica de Radio-Vectores (Sistema SORCARTOA)
Una formulación vectorial complementaria radica en modelar el subespacio operando única y exclusivamente mediante las magnitudes acotadas de ángulos agudos de referencia topológicos. Dependiendo rigurosamente de en qué frontera cuadrática o sub-espacio matricial nazca o descuelle el radio vector empírico observable, el tratamiento se homologa al primer abordaje fundacional de triángulos euclidianos elementales de la sección $1$. Esta formalización extendida es parametrizada bajo la mnemotecnia analítica SORCARTOA:
* $\sin(\theta) = \frac{\text{Cateto Opuesto}}{\text{Radio Vector }(R)}$
* $\cos(\theta) = \frac{\text{Cateto Adyacente}}{\text{Radio Vector }(R)}$
* $\tan(\theta) = \frac{\text{Cateto Opuesto}}{\text{Cateto Adyacente}}$

![[SORCARTOA.png]]
Bajo esta axiomática transversal, el Radio Vector se consagra matemáticamente en todo tiempo y momento lineal escalar como una norma dimensional euclidiana de crecimiento o fuerza positiva, luego es retenida inflexible y llanamente como unidad medible estrictamente superior a cero ($R>0$). Por necesidad algebraicamente forzosa de la función armónica, las entidades funcionales que asumen íntegramente y absorben el desplazamiento oscilatorio polar y su respectiva mutación del signo estructural ($(+, -)$) son invariablemente las componentes cartesianas perimetrales relativas formadas con el origen, oscilando según fije dogmáticamente el cuadrante del espacio vectorial. Este elegante artificio es precisamente el lecho matricial de validación axiomática para la procedencia fundamental de la lógica en la distribución de la alternancia de signos deducida en apartados teóricos de axiomas anteriores, otorgando ahora una perspectiva cinemática superior para su compresión total y plena.

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
![[angulo_negativo.png]]
**Paridad del Seno**:
$$\sin(-\theta) = -\sin(\theta)$$
(función impar)
*Demostración:*
$$sin(\theta)=y/R$$
$$sin(-\theta)=-y/R=-(y/R)=-sin(\theta)$$
**Paridad del Coseno**:
$$\cos(-\theta) = \cos(\theta)$$ (función par)

**Paridad del Coseno**:
$$\tan(-\theta) = -\tan(\theta)$$ (función impar)
*Demostración*:
$$tan(-\theta)=\frac{sin(-\theta)}{cos(-\theta)}=\frac{-sin(\theta)}{cos(\theta)}=-\frac{sin(\theta)}{cos(\theta)}=-tan(\theta)$$

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

**Demostración de la suma y diferencia de la tangente:**
Por definición sabemos que $\tan(\alpha \pm \beta) = \frac{\sin(\alpha \pm \beta)}{\cos(\alpha \pm \beta)}$. Sustituyendo las fórmulas anteriores de seno y coseno:
$$\tan(\alpha \pm \beta) = \frac{\sin(\alpha)\cos(\beta) \pm \cos(\alpha)\sin(\beta)}{\cos(\alpha)\cos(\beta) \mp \sin(\alpha)\sin(\beta)}$$

Dividiendo el numerador y el denominador por el producto $\cos(\alpha)\cos(\beta)$:
$$\tan(\alpha \pm \beta) = \frac{\frac{\sin(\alpha)\cos(\beta)}{\cos(\alpha)\cos(\beta)} \pm \frac{\cos(\alpha)\sin(\beta)}{\cos(\alpha)\cos(\beta)}}{\frac{\cos(\alpha)\cos(\beta)}{\cos(\alpha)\cos(\beta)} \mp \frac{\sin(\alpha)\sin(\beta)}{\cos(\alpha)\cos(\beta)}}$$

Simplificando los términos, obtenemos la fórmula buscada:
$$\tan(\alpha \pm \beta) = \frac{\tan(\alpha) \pm \tan(\beta)}{1 \mp \tan(\alpha)\tan(\beta)} \quad \blacksquare$$

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
$$\tan(2\theta) = \frac{2\tan(\theta)}{1 - \tan^2(\theta)}$$

**Formas alternativas de $\cos(2\theta)$:**
$$\cos(2\theta) = 2\cos^2(\theta) - 1 = 1 - 2\sin^2(\theta)$$

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

Un ejercicio clásico en trigonometría consiste en verificar una identidad; es decir, nos presentan una supuesta igualdad matemática y debemos demostrar paso a paso que es verdadera para todos los valores definidos del ángulo. Si bien no existe un método único o universal para hacer esto, la práctica nos enseña diversas estrategias y técnicas algebraicas que facilitarán el desarrollo de la demostración.
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
$$\sin^2(\theta) = \sin^2(\theta)$$
Verificado ✓

**Ejemplo 7.3:**
Verificar: $\sin^2(x)+2\sin(x)\cos(x)+\cos^2(x)=1+\dfrac{2\sin(x)}{\sec(x)}$

**Solución:** Simplificamos cada lado por separado.

*Lado izquierdo:*
$$\sin^2(x)+2\sin(x)\cos(x)+\cos^2(x) = \bigl(\sin^2(x)+\cos^2(x)\bigr)+2\sin(x)\cos(x) = 1+2\sin(x)\cos(x)$$

*Lado derecho:*
$$1+\frac{2\sin(x)}{\sec(x)} = 1+2\sin(x)\cdot\frac{1}{\sec(x)} = 1+2\sin(x)\cos(x)$$

ya que $\dfrac{1}{\sec(x)}=\cos(x)$ por definición.

Ambos lados son iguales:
$$1+2\sin(x)\cos(x) = 1+2\sin(x)\cos(x) \checkmark$$

**Ejemplo 7.4:**
Verificar: $\dfrac{\sin^2(x)+\cos^2(x)}{\sec(x)+\tan(x)}=\sec(x)-\tan(x)$

**Solución:** El numerador del lado izquierdo es la identidad pitagórica:
$$\frac{\sin^2(x)+\cos^2(x)}{\sec(x)+\tan(x)} = \frac{1}{\sec(x)+\tan(x)}$$

Multiplicamos numerador y denominador por el conjugado $\sec(x)-\tan(x)$:
$$\frac{1}{\sec(x)+\tan(x)} \cdot \frac{\sec(x)-\tan(x)}{\sec(x)-\tan(x)} = \frac{\sec(x)-\tan(x)}{\sec^2(x)-\tan^2(x)}$$

El denominador se simplifica con la identidad $\sec^2(x)-\tan^2(x)=1$ (derivada de la identidad pitagórica):
$$\frac{\sec(x)-\tan(x)}{1} = \sec(x)-\tan(x) \checkmark$$

---
## 8. Funciones trigonométricas

Todas las razones trigonométricas también podemos trabajarlas como si fueran funciones, solo debemos considerar un ángulo $x$ como nuestra variable (medida en radianes para usar la misma recta real que hemos usado) y con esto podemos estudiar el comportamiento con las herramientas que ya hemos estudiado.
Primero, para estudiar las propiedades de estas funciones, haremos una tabla de valores con todas las razones trigonométricas; apoyándonos en los ángulos notables y las identidades, calcularemos varios valores

> **Nota sobre el uso de radianes:** Resulta fundamental que la variable independiente $x$ represente un ángulo medido en **radianes**. Dado que el radián relaciona directamente el ángulo con la longitud de un arco (una medida real), usar radianes nos permite graficar las funciones trigonométricas sobre la misma recta numérica real que usamos para cualquier otra función (polinomial, exponencial, etc.). Esto facilita su análisis, comparación y el desarrollo de herramientas de Cálculo sobre ellas.

|     $x$ (rad)      |     $x$ ($\tau$)     | $x$ (°) |       $\sin(x)$        |       $\cos(x)$        |       $\tan(x)$        |        $\sec(x)$        |        $\csc(x)$        |       $\cot(x)$        |
| :----------------: | :------------------: | :-----: | :--------------------: | :--------------------: | :--------------------: | :---------------------: | :---------------------: | :--------------------: |
|        $0$         |         $0$          |  $0°$   |          $0$           |          $1$           |          $0$           |           $1$           |  $\infty$ (indefinido)  | $\infty$ (indefinido)  |
|  $\dfrac{\pi}{6}$  |  $\dfrac{\tau}{12}$  |  $30°$  |     $\dfrac{1}{2}$     | $\dfrac{\sqrt{3}}{2}$  | $\dfrac{\sqrt{3}}{3}$  | $\dfrac{2\sqrt{3}}{3}$  |           $2$           |       $\sqrt{3}$       |
|  $\dfrac{\pi}{4}$  |  $\dfrac{\tau}{8}$   |  $45°$  | $\dfrac{\sqrt{2}}{2}$  | $\dfrac{\sqrt{2}}{2}$  |          $1$           |       $\sqrt{2}$        |       $\sqrt{2}$        |          $1$           |
|  $\dfrac{\pi}{3}$  |  $\dfrac{\tau}{6}$   |  $60°$  | $\dfrac{\sqrt{3}}{2}$  |     $\dfrac{1}{2}$     |       $\sqrt{3}$       |           $2$           | $\dfrac{2\sqrt{3}}{3}$  | $\dfrac{\sqrt{3}}{3}$  |
|  $\dfrac{\pi}{2}$  |  $\dfrac{\tau}{4}$   |  $90°$  |          $1$           |          $0$           | $\infty$ (indefinido)  |  $\infty$ (indefinido)  |           $1$           |          $0$           |
| $\dfrac{2\pi}{3}$  |  $\dfrac{\tau}{3}$   | $120°$  | $\dfrac{\sqrt{3}}{2}$  |    $-\dfrac{1}{2}$     |      $-\sqrt{3}$       |          $-2$           | $\dfrac{2\sqrt{3}}{3}$  | $-\dfrac{\sqrt{3}}{3}$ |
| $\dfrac{3\pi}{4}$  |  $\dfrac{3\tau}{8}$  | $135°$  | $\dfrac{\sqrt{2}}{2}$  | $-\dfrac{\sqrt{2}}{2}$ |          $-1$          |       $-\sqrt{2}$       |       $\sqrt{2}$        |          $-1$          |
| $\dfrac{5\pi}{6}$  | $\dfrac{5\tau}{12}$  | $150°$  |     $\dfrac{1}{2}$     | $-\dfrac{\sqrt{3}}{2}$ | $-\dfrac{\sqrt{3}}{3}$ | $-\dfrac{2\sqrt{3}}{3}$ |           $2$           |      $-\sqrt{3}$       |
|       $\pi$        |  $\dfrac{\tau}{2}$   | $180°$  |          $0$           |          $-1$          |          $0$           |          $-1$           |  $\infty$ (indefinido)  | $\infty$ (indefinido)  |
| $\dfrac{7\pi}{6}$  | $\dfrac{7\tau}{12}$  | $210°$  |    $-\dfrac{1}{2}$     | $-\dfrac{\sqrt{3}}{2}$ | $\dfrac{\sqrt{3}}{3}$  | $-\dfrac{2\sqrt{3}}{3}$ |          $-2$           |       $\sqrt{3}$       |
| $\dfrac{5\pi}{4}$  |  $\dfrac{5\tau}{8}$  | $225°$  | $-\dfrac{\sqrt{2}}{2}$ | $-\dfrac{\sqrt{2}}{2}$ |          $1$           |       $-\sqrt{2}$       |       $-\sqrt{2}$       |          $1$           |
| $\dfrac{4\pi}{3}$  |  $\dfrac{2\tau}{3}$  | $240°$  | $-\dfrac{\sqrt{3}}{2}$ |    $-\dfrac{1}{2}$     |       $\sqrt{3}$       |          $-2$           | $-\dfrac{2\sqrt{3}}{3}$ | $\dfrac{\sqrt{3}}{3}$  |
| $\dfrac{3\pi}{2}$  |  $\dfrac{3\tau}{4}$  | $270°$  |          $-1$          |          $0$           | $\infty$ (indefinido)  |  $\infty$ (indefinido)  |          $-1$           |          $0$           |
| $\dfrac{5\pi}{3}$  |  $\dfrac{5\tau}{6}$  | $300°$  | $-\dfrac{\sqrt{3}}{2}$ |     $\dfrac{1}{2}$     |      $-\sqrt{3}$       |           $2$           | $-\dfrac{2\sqrt{3}}{3}$ | $-\dfrac{\sqrt{3}}{3}$ |
| $\dfrac{7\pi}{4}$  |  $\dfrac{7\tau}{8}$  | $315°$  | $-\dfrac{\sqrt{2}}{2}$ | $\dfrac{\sqrt{2}}{2}$  |          $-1$          |       $\sqrt{2}$        |       $-\sqrt{2}$       |          $-1$          |
| $\dfrac{11\pi}{6}$ | $\dfrac{11\tau}{12}$ | $330°$  |    $-\dfrac{1}{2}$     | $\dfrac{\sqrt{3}}{2}$  | $-\dfrac{\sqrt{3}}{3}$ | $\dfrac{2\sqrt{3}}{3}$  |          $-2$           |      $-\sqrt{3}$       |
|       $2\pi$       |        $\tau$        | $360°$  |          $0$           |          $1$           |          $0$           |           $1$           |  $\infty$ (indefinido)  | $\infty$ (indefinido)  |

### 8.1 La función seno

**Definición 8.1:**
$$f(x) = \sin(x)$$

Comenzaremos haciendo un bosquejo con los valores obtenidos en la tabla para el seno
![[funcion_seno_1.png]]
con esto ya nos podemos hacer una idea de la gráfica, pero si usamos propiedades como la periodicidad e identidades como el ángulo medio o la suma de ángulos para obtener más valores podemos hacer un mejor bosquejo del gráfico
![[funcion_seno_2.png]]
Con esto ya nos podemos dar una idea de como será la grafica de la función

**Gráfica:**
![[funcion_seno_3.png]]
La función seno es una función periódica, es decir, que se repite cada cierto intervalo específico; además vemos que está acotada y que tiene infinitas raíces 

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

Si repetimos el mismo ejercicio para la función coseno, obtendremos un resultado bastante similar 

**Gráfica:**
![[funcion_coseno_1.png]]
Viendo su forma podemos intuir que sus propiedades serán similares a las de la función seno

**Observación:** $\cos(x) = \sin(x + \frac{\pi}{2})$ (coseno es seno desplazado o viceversa dependiendo como se este mirando)

**Propiedades:**
- **Dominio:** $(-\infty, +\infty)$
- **Imagen:** $[-1, 1]$
- **Período:** $2\pi$
- **Simetría:** Función par ($\cos(-x) = \cos(x)$)
- **Ceros:** $x = \frac{\pi}{2} + n\pi$, donde $n \in \mathbb{Z}$
- **Máximos:** $x = 2n\pi$, valor $1$
- **Mínimos:** $x = \pi + 2n\pi$, valor $-1$

### 8.3 La función tangente

**Definición 8.3:**
$$f(x) = \tan(x) = \frac{\sin(x)}{\cos(x)}$$

Nuevamente repetiremos nuestro ejercicio del bosquejo con la tangente para ver qué obtendremos, primero con los ángulos notables de $0$ a $2\pi$
![[funcion_tangente_1.png]]
Esto no nos dice mucho; deberemos calcular más puntos para tener una mejor aproximación 
![[funcion_tangente_2.png]]
Con esto ya tenemos una mejor visión; ahora debemos analizar un poco la función. Primero veamos $\sin(x)$ y $\cos(x)$ en la misma gráfica:
![[funcion_seno_coseno.png]]
Podemos ir analizando por tramos:
* **Primer tramo** $[0,\,\pi/2)$: el seno aumenta y el coseno disminuye, lo que nos da una función creciente, hasta llegar a $\pi/2$ donde el denominador es $0$ y tenemos una asíntota vertical (la función crece hacia $+\infty$).
* **Segundo tramo** $(\pi/2,\,\pi]$: el seno es decreciente y el coseno es creciente pero negativo. Comenzamos con valores cercanos a $1$ divididos por valores cercanos a $0^-$, lo que produce resultados muy grandes en magnitud y negativos; a medida que avanzamos, el coseno crece en magnitud y los resultados se vuelven progresivamente más pequeños en valor absoluto, hasta llegar a $\pi$ donde el numerador es $0$ y, por lo tanto, $\tan(\pi)=0$.
* **Tercer tramo** $[\pi,\,3\pi/2)$: ambas funciones son negativas, por lo que su cociente es positivo. Este tramo tiene el mismo comportamiento que el primero (función creciente con asíntota en $3\pi/2$), solo que trasladado un período $\pi$.
* **Cuarto tramo** $(3\pi/2,\,2\pi]$: análogo al segundo tramo; el cociente es negativo y la función crece desde $-\infty$ hasta $0$.

Con este análisis y los puntos que trazamos, ya podemos tener una buena idea de la gráfica de la función. Además, podemos observar algunas propiedades importantes: su período es $\pi$ (la mitad del período de seno y coseno) y tiene infinitas asíntotas verticales en los puntos donde $\cos(x)=0$.
Después de todo este trabajo, ya es momento de ver su gráfica:

**Gráfica:**
![[funcion_tangente_3.png]]

**Propiedades:**
- **Dominio:** $\mathbb{R} \setminus \{\frac{\pi}{2} + n\pi : n \in \mathbb{Z}\}$ (excluye donde $\cos(x) = 0$)
- **Imagen:** $(-\infty, +\infty)$
- **Período:** $\pi$
- **Simetría:** Función impar
- **Ceros:** $x = n\pi$
- **Asíntotas verticales:** $x = \frac{\pi}{2} + n\pi$

### 8.4 Funciones recíprocas (Secante, Cosecante y Cotangente)

Al igual que las funciones principales, sus razones recíprocas también se extienden como funciones trigonométricas sobre los números reales. Aunque en la práctica (y en el Cálculo) el uso de seno, coseno y tangente abarca casi todas las aplicaciones, conocer gráficamente a sus recíprocas completa nuestro panorama.

**1. La función Cosecante:** $f(x) = \csc(x) = \frac{1}{\sin(x)}$
- **Comportamiento:** Al depender del inverso del seno, experimenta explosiones hacia $\pm\infty$ cada vez que $\sin(x)$ se acerca a cero. Esto se traduce en **asíntotas verticales** estrictamente donde se anula el seno: $x = n\pi$, con $n \in \mathbb{Z}$.
- **Imagen:** $(-\infty, -1] \cup [1, +\infty)$. Curiosamente, la función cosecante jamás tomará valores dentro del intervalo $(-1, 1)$, que es justo el "territorio exclusivo" de su contraparte, el seno.
- **Período:** $2\pi$.
![[funcion_cosecante_1.png]]
**2. La función Secante:** $f(x) = \sec(x) = \frac{1}{\cos(x)}$
- **Comportamiento:** De manera análoga, la secante tiene asíntotas verticales allí donde el coseno vale cero: $x = \frac{\pi}{2} + n\pi$. Visualmente asimilan la forma de "campanas invertidas" o "U" que "descansan" por encima y por debajo apoyadas milimétricamente exactamente sobre los picos y valles de la gráfica original del coseno.
- **Imagen:** $(-\infty, -1] \cup [1, +\infty)$.
- **Período:** $2\pi$.
![[funcion_secante_1.png]]
**3. La función Cotangente:** $f(x) = \cot(x) = \frac{\cos(x)}{\sin(x)}$
- **Comportamiento:** Posee asíntotas en los cruces por cero del seno ($x = n\pi$). Una diferencia estética remarcable respecto a la tangente, además de la traslación de las asíntotas, es que mientras la tangente es siempre creciente en sus intervalos de dominio contiguo, la cotangente es una función estrictamente **decreciente**.
- **Imagen:** $(-\infty, +\infty)$.
- **Período:** $\pi$.
![[funcion_cotangente_1.png]]
### 8.5 Transformaciones de funciones trigonométricas

Una vez establecidas analíticamente las gráficas primigenias de las funciones trigonométricas, procederemos a estudiar formalmente su comportamiento algebraico bajo el efecto sistemático de la adición de constantes paramétricas operativas (transformaciones lineales afines vectoriales).

Sean los escalares reales $A,B,C,D \in \mathbb{R}$, asumiendo rigurosamente $A, B \neq 0$.
**Forma general de la función periódica escalada:**
$$f(x) = A \cdot \sin(B \cdot x + C) + D$$
*Nota de invariabilidad métrica: Todo teorema o propiedad topológica inferida a continuación recae isomorfamente y es análoga para la variante en coseno.*

**Análisis de Parámetros:**

1. **El escalar $D$: Desplazamiento vertical (Traslación en ordenadas)**
   - Evaluado como un campo $f(x) = \sin(x) + D$.
   - Proyecta una **traslación vertical pura** carente absoluta de deformación tensorial. El eje medular o "centroide escalar radiante" de toda la función sufre un vectorización hacia la parte superior ($D > 0$) o decanta hacia la sección inferior ($D < 0$).
   - La nueva métrica estabilizadora central será el límite $y = D$.
*Ejemplo empírico analítico: $f(x) = \sin(x) + 5$*
![[funcion_seno+5.png]]

2. **El escalar $A$: Amplitud paramétrica (Homotecia escalar modular)**
   - Operado como el factor multi-tensor $f(x) = A \cdot \sin(x)$.
   - Determina estructuralmente un estiramiento vertical (homotecia unidimensional) regulando las crestas cúspides y el sumidero inferior oscilatorio de la onda de transmisión acotando al co-dominio natural de la matriz.
   - Analíticamente la función original oscila encerrada y amarrada entre $[- |A|, |A|]$.
   - Generando un sistema mixto de desplazamiento transversal, en formato $A \cdot \sin(x) + D$ la gráfica modula de rango final cerrado en la sección estocástica entre $[- |A| + D, |A| + D]$.
![[funcion_senox3.png]]

3. **El escalar $B$: Compresión Frecuencial (Pulsación constante del marco espacial)**
   - Subjetado estructuralmente en la parte íntima variable de la función $f(x) = \sin(B \cdot x)$.
   - Parametriza y diseña matemáticamente el factor constante por el cual la red sufre una contracción pura (o aburguesamiento isomorfo) sobre el mismo plano ecuatorial del eje $x$. Es la razón determinística neta de conteo iterativo de oscilaciones de banda por bloque normal de radianes acotado a $2\pi$.
   - Modificación sustantiva generalizada del **Período empírico:** $T = \frac{2\pi}{|B|}$
   - **Demostración Analítica del Período:** Por definición de periodicidad matemática, una función $f(x)$ ostenta un período $T$ supremo si rige universalmente que $f(x + T) = f(x)$ para todo $x \in \mathbb{R}$. Sea $f(x) = \sin(B \cdot x)$, evaluamos el incremento topológico: 
     $$f(x + T) = \sin(B(x + T)) = \sin(B \cdot x + B \cdot T)$$
     Consagrando como axioma fundamental que la función seno originaria completa y sella su núcleo orbital isomorfo al sumar $2\pi$ a su argumento (i.e. $\sin(\theta + 2\pi) = \sin(\theta)$), forzamos la igualdad resolviendo el encaje de fase asintótica:
     $$|B| \cdot T = 2\pi \implies T = \frac{2\pi}{|B|} \quad \blacksquare$$
![[funcion_seno5x.png]]

4. **El escalar $C$: Desfase primigenio de campo (Traslación en abscisas)**
   - Parametrizado matricialmente como base mutante topológica $f(x) = \sin(x + C)$.
   - Operador matemático universal fundamental en señales; rige un corrimiento o ***shift* unidimensional rígido transversal de onda** (sin deformar las métricas internas de su fase o elongación perimetral radial).
   - Arrastra el punto neutral génesis originario para mutarlo de origen. El punto de corte asintótico se formaliza como el radián de **Desfase empírico:** $\phi = -\frac{C}{B}$. El tren cinemático avanza forzosamente en abscisas en la dirección contraria del hiper-plano negativo izquierdo estandarizado si sucede que $\phi > 0$.
   - **Demostración Analítica del Desfase:** Partiendo de la forma matricial completa del argumento vibratorio base subyacente del seno, $\sin(Bx + C)$, se despliega una disección algebraica y factorización forzada del tensor escalar frecuencial $B$:
     $$\sin(B \cdot x + C) = \sin\left[B \cdot \left(x + \frac{C}{B}\right)\right]$$
     Por axioma básico del cálculo y funciones reales, todo corrimiento morfológico interno sobre la variable independiente regido como $f(x - h)$ impone sistemáticamente una traslación horizontal rígida pura de toda la métrica equivalente al vector posicional $h$. En el interior de nuestro sistema, identificamos indudablemente que $h = -\frac{C}{B}$. Este vector de alteración escalar neta es concebido analíticamente como el desfase matricial $\phi$, evidenciando contundentemente que la génesis y nodo origen del modelo ($x=0$) ha migrado materialmente en el espacio y reposa ahora en la abscisa transversal perimetral $x = -\frac{C}{B}$. $\blacksquare$
![[funcion_senox+1.png]]


**Ejemplo 8.1 (Análisis paramétrico analítico de una función senoidal):**
Consideremos el modelado de la ecuación analítica del operador en el espacio:
$$f(x) = 3\sin(2x - \pi) + 1$$
Procedemos a realizar el despiece escalar de sus tensores fundamentales basándonos en la estructura modular de la matriz $A \cdot \sin(Bx + C) + D$:
- **Amplitud Modular Euclidiana ($A$):** La homotecia nos dicta que $A = 3$. Por lo tanto, el rango vibratorio original $[-1, 1]$ se expande isométricamente un factor de tres. Integrando el desplazamiento vertical empírico asintótico ($D = 1$), demostramos formalmente que la cota de frontera del co-dominio natural asume límites absolutos demarcados entre $y \in [-3+1, 3+1] = [-2, 4]$.
- **Período Frecuencial Condicionado ($T$):** Al inspeccionar rigurosamente el argumento iterativo, advertimos $B = 2$. Luego, el período longitudinal por ciclo experimenta una compresión escalar neta fijada por: $T = \frac{2\pi}{|2|} = \pi$.
- **Desfase Posicional Abscisal ($\phi$):** Aplicando un axioma directo de traslación afín de frontera local, determinamos el *shift* inicial de abscisas perimetrales resolviendo el nodo analítico: $\phi = -\frac{C}{B} = -\frac{(-\pi)}{2} = \frac{\pi}{2}$. Puesto irrefutablemente que $\phi > 0$, comprobamos con precisión matricial que toda la onda e infraestructura morfológica sufrió forzosamente un traslape lateral de $\frac{\pi}{2}$ radianes apuntando hacia el subespacio o cuadrante positivo referencial (derecha estandarizada).
- **Desplazamiento Vertical Constante ($D$):** En conformidad con $D = 1$, la recta estructurante base en torno de la cual oscila sinérgicamente todo nuestro campo gravitatorio dinámico asciende linealmente reposando su nuevo origen o fulcro central en el intercepto cartesiano $y = 1$.
![[funcion_seno_ejemplo1.png]]

**Ejemplo 8.2 (Variante paramétrica con dilatación y reflexión topológica):**
Apliquemos análogamente los principios analíticos ya fundamentados en el Ejemplo 8.1 al caso de un operador coseno:
$$g(x) = -2\cos\left(\frac{x}{3} + \frac{\pi}{4}\right) - 1$$
Abstrayendo los tensores desde la forma general $g(x) = A \cdot \cos(Bx + C) + D$, sintetizamos:
- **Amplitud y Reflexión ($A = -2$):** La magnitud escalar fija una amplitud de $|A| = 2$. Crucialmente, el signo negativo condiciona al sistema a un **vuelco especular o reflexión topológica** sobre su eje base, invirtiendo íntegramente crestas y valles.
- **Período Dilatado ($T$):** Siendo $B = 1/3$ (elongación fraccionaria), el ciclo natural experimenta una dilatación temporal sustantiva: $T = \frac{2\pi}{1/3} = 6\pi$.
- **Desfase Negativo ($\phi$):** Operando la traslación afín observamos que $\phi = -\frac{C}{B} = -\frac{\pi/4}{1/3} = -\frac{3\pi}{4}$. Puesto que $\phi < 0$, atestiguamos que la cúspide generatriz característica del coseno ha sido transpuesta $-\frac{3\pi}{4}$ radianes hacia el espectro negativo izquierdo.
- **Desplazamiento Vertical ($D = -1$):** El fulcro geométrico de oscilación de la matriz decae linealmente y se estabiliza en la métrica $y = -1$.
![[funcion_coseno_ejemplo1.png]]

*Nota*: Algunos términos como homeostasia, relfexion se introduciran formalmente en la siguiente clase, [[Clase 7 - Cónicas]]

---
## 9. Relación con círculos y ecuaciones paramétricas

El vínculo intrínseco entre la geometría analítica y la trigonometría trasciende sobradamente la resolución estática de triángulos. Mediante la incursión de variables independientes de transición denominadas **parámetros**, adquirimos el poder analítico de modelar y vectorizar temporalmente la trayectoria de curvas planas cerradas con estricto rigor algebraico cinemático.

### 9.1 Parametrización estocástica del círculo unitario

**Proposición 9.1 (Mapeo paramétrico base):**
El lugar geométrico estático que dicta al círculo unitario acotado por la curva $x^2 + y^2 = 1$, admite una formulación paramétrica dinámica homóloga dependiente de un escalar continuo temporal o angular $t$:
$$\begin{cases}
x(t) = \cos(t) \\
y(t) = \sin(t)
\end{cases}, \quad t \in [0, 2\pi)$$

**Verificación Axiomática de Coherencia:** 
Sustituyendo de lleno el sistema paramétrico sobre nuestro cascarón cartesiano rector, recuperamos invariablemente la inquebrantable identidad pitagórica fundamental:
$$x(t)^2 + y(t)^2 = \cos^2(t) + \sin^2(t) = 1 \quad \blacksquare$$

*Conclusión analítica:* Mientras el parámetro transitorio $t$ barre escalarmente el dominio diferencial continuo $[0, 2\pi)$, el vector posicional o cursor $\mathbf{r}(t) = (\cos(t), \sin(t))$ describe mecánicamente una vuelta parabólica completa o ciclo orbital en sentido rotacional antihorario puro.

### 9.2 Parametrización escalar para radios genéricos $R$

**Proposición 9.2 (Expansión matricial por homotecia radial):**
Si re-escalamos o modulamos isométricamente el espacio completo por un tensor radiante $R > 0$, el círculo anclado en el polo con ecuación cartesiana acoplada $x^2 + y^2 = R^2$ se define paramétricamente mediante el producto abeliano:
$$\begin{cases}
x(t) = R\cos(t) \\
y(t) = R\sin(t)
\end{cases}, \quad t \in [0, 2\pi)$$

**Verificación Empírico-Matemática:**
Introduciendo las variantes transitorias en la norma euclidiana general:
$$x(t)^2 + y(t)^2 = (R\cos(t))^2 + (R\sin(t))^2 = R^2\cos^2(t) + R^2\sin^2(t)$$
Extrayendo o factorizando el escalar común expansivo $R^2$:
$$R^2 \left[ \cos^2(t) + \sin^2(t) \right] = R^2(1) = R^2 \quad \blacksquare$$

**Ejemplo 9.1 (Radio-Vector escalado modularmente):**
Considérese una órbita o toroide plano de radio $R = 3$. Su vectorización paramétrica queda expuesta como:
$$x(t) = 3\cos(t), \quad y(t) = 3\sin(t)$$

Evaluación paramétrica estricta en los nodos cuadráticos críticos del plano:
- **Estado de Origen ($t = 0$):** Inicia en la cúspide horizontal $\to (3, 0)$
- **Primera Cuadratura ($t = \pi/2$):** Apogeo polar norte $\to (0, 3)$
- **Afelio Diametral ($t = \pi$):** Traslado negativo total $\to (-3, 0)$
- **Segunda Cuadratura ($t = 3\pi/2$):** Nadir polar sur $\to (0, -3)$

### 9.3 Traslación paramétrica de círculos en cuadrantes

**Proposición 9.3 (Circunferencias no concéntricas o trasladadas):**
Si el círculo de radio $R$ tiene su centro desplazado al punto coordenado $(h, k)$, su parametrización adquiere el ajuste del desfase sumando estas coordenadas a su vector base:
$$x(t) = h + R\cos(t), \quad y(t) = k + R\sin(t), \quad t \in [0, 2\pi)$$

---
## 10. Ecuaciones trigonométricas

Una **ecuación trigonométrica** es una ecuación analítica en la que la variable o incógnita angular se encuentra dentro del argumento de una o más funciones trigonométricas. A diferencia de las *identidades*, que son igualdades válidas para cualquier valor de su dominio, las ecuaciones solo se satisfacen para ángulos específicos.

**Periodicidad y Soluciones Infinitas:**
La principal característica de estas funciones es su oscilación y periodicidad infinita: si hallamos un ángulo solución $x_0$, entonces todos sus ángulos coterminales correspondientes también la satisfarán. Esto arroja teóricamente infinitas soluciones. Por esta razón, solemos dividir el abordaje en dos ramas:
- **Solución acotada en un intervalo:** Se pide encontrar determinísticamente las soluciones atrapadas dentro de una sola rotación originaria, convencionalmente en el intervalo $[0, 2\pi)$. Se obtendrá un conjunto finito.
- **Solución general:** Busca parametrizar todas las soluciones matemáticas posibles sumando ciclos acoplados enteros. Para esto añadimos notaciones cíclicas como $+ 2n\pi$ donde $n \in \mathbb{Z}$ (números enteros).

### Estrategia General (Algoritmo de Resolución)
1. **Despeje algebraico:** Aislar la función trigonométrica aplicando las leyes del álgebra básica o transicional analítica (reducción lineal, cuadrática, polinómica, etc.).
2. **Ángulo de referencia:** Determinar primeramente como base de anclaje el ángulo agudo de referencia primario ubicado en el primer cuadrante.
3. **Distribución por cuadrantes:** Trasladar el ángulo de referencia hacia los cuadrantes condicionados explícitamente por el signo (positivo o negativo) de la ecuación despejada resultante.
4. **Respuesta unificada:** Reunir analíticamente todas las intersecciones resueltas que respeten nuestros dominios restringidos.

### 10.1 Ecuaciones lineales básicas

**Ejemplo 10.1 (Ecuación directa con curva Seno):**
Resuelva analíticamente $\sin(x) = \frac{1}{2}$ para un dominio acotado $x \in [0, 2\pi)$.

**Solución paso a paso:**
- El **ángulo de referencia** (donde el seno vale $\frac{1}{2}$) corresponde a $30°$, que en radianes es $\frac{\pi}{6}$.
- Analizando el signo, sabemos que la función seno es positiva en los cuadrantes I y II.
- Por tanto, proyectamos nuestra solución hacia esos cuadrantes:
  - Cuadrante I (solución directa): $x = \frac{\pi}{6}$.
  - Cuadrante II (usamos simetría suplementaria): $x = \pi - \frac{\pi}{6} = \frac{5\pi}{6}$.

**Conjunto solución en $[0, 2\pi)$:**
$$\mathbb{S} = \left\{\frac{\pi}{6}, \frac{5\pi}{6}\right\}$$

*(Nota: Si se pidiese la solución general sin acotar dominios, lo representaríamos agregando multiplicadores del período $2k\pi$, quedando:)* 
$$x = \frac{\pi}{6} + 2k\pi \quad \lor \quad x = \frac{5\pi}{6} + 2k\pi, \quad \forall k \in \mathbb{Z}$$

**Ejemplo 10.2 (Ecuación directa con curva Coseno y valores negativos):**
Resuelva formalmente $\cos(x) = -\frac{\sqrt{2}}{2}$.

**Solución paso a paso:**
- Evaluamos primero el **ángulo de referencia** (ignorando numéricamente el signo). Sabemos que buscar dónde el coseno vale $\frac{\sqrt{2}}{2}$ nos lleva al ancla referencial de $45°$ o $\frac{\pi}{4}$.
- El signo explícitamente negativo ($-$) pre-establecido en la ecuación base nos obliga a re-ubicar diametralmente esta fase hacia los dominios donde la coordenada $X$ (y por ende el coseno) es negativa: los cuadrantes **II y III**.
- Despliegue en Cuadrante II: $x = \pi - \frac{\pi}{4} = \frac{3\pi}{4}$
- Despliegue en Cuadrante III: $x = \pi + \frac{\pi}{4} = \frac{5\pi}{4}$

**Conjunto Solución Acotado:**
$$\mathbb{S} = \left\{\frac{3\pi}{4} +2k\pi, \frac{5\pi}{4}+2k\pi\right\} \quad \forall k \in \mathbb{Z}$$

### 10.2 Ecuaciones trigonométricas por subrogación cuadrática

Cuando la ecuación presenta funciones elevadas a una potencia (ej. cuadráticas integradas), se recurre al uso analítico del **Sustitución Algebraica** transitoria para reducir el orden de la resolución a un polinomio clásico.

**Ejemplo 10.3 (Polinomio Trigonométrico Simple de Orden Dos):**
Encontrar las raíces lícitas o intersecciones para $2\sin^2(x) - \sin(x) - 1 = 0$, para el intervalo $x \in [0, 2\pi)$.

**Solución paso a paso:**
- **Sustitución Transitoria Algebraica:** Definamos la equivalencia transitoria $u = \sin(x)$. Al realizarlo, simplificamos la expresión compleja hacia una ecuación cuadrática clásica:  
$$2\sin^2(x) - \sin(x) - 1 = 0$$
$$2u^2 - u - 1 = 0$$
- **Factorización de la Cuadrática:** Factorizando polinomialmente obtenemos su expresión simplificada observable $\to (2u + 1)(u - 1) = 0$.
  Esto bifurca nuestra búsqueda a dos posibles resultados analíticos:
  $$u_1 = 1 \quad \text{o} \quad u_2 = -\frac{1}{2}$$
- **Retorno de factor y resolución trigonométrica por casos:**
  * **Caso Alfa ($u_1 = 1$):** Evaluamos y retornamos a la base trigonométrica original: $\sin(x) = 1$. Dicha cota ocurre de manera única en el diagrama superior, correspondiendo puntualmente al pináculo o cenit en $x = \frac{\pi}{2}$.
  * **Caso Beta ($u_2 = -\frac{1}{2}$):** Evaluamos el segundo caso $\sin(x) = -\frac{1}{2}$. Vimos que su ángulo referencial para el positivo es $\frac{\pi}{6}$, pero para acatar el signo negativo debemos empujar vectorialmente nuestra ubicación hacía dominios Sur u opuestos (Cuadrantes III y IV), resultando consecuentemente en $x = \pi + \frac{\pi}{6} = \frac{7\pi}{6}$ y para el cuarto anclamos en $x = 2\pi - \frac{\pi}{6} = \frac{11\pi}{6}$.

**Conjunto Solución Resultante Final:**
$$\mathbb{S} = \left\{\frac{\pi}{2}, \frac{7\pi}{6}, \frac{11\pi}{6}\right\}$$

### 10.3 Ecuaciones con compresión de múltiplos angulares

**Ejemplo 10.4 (Ajuste algorítmico y periodo iterativo):**
Resolver sistemáticamente $\sin(2x) = \frac{\sqrt{3}}{2}$ evaluado sobre la franja $x \in [0, 2\pi)$.

**Solución paso a paso:**
- Definimos transitoriamente el argumento conjunto como variable abstracta $u = 2x$. Por lo tanto, buscaremos los puntos donde $\sin(u) = \frac{\sqrt{3}}{2}$.
- Un detalle capital: al pedirnos hallar originalmente el segmento dictaminado por $x \in [0, 2\pi)$, por naturaleza el argumento escalar "el doble de rápido" ($u=2x$) presentará una oscilación mayor a su doble: $u \in [0, 4\pi)$. Esto significa que daremos **dos vueltas completas** sobre el círculo unitario buscando soluciones válidas continuas.
- **Primera Rotación** (sobre el intervalo $[0, 2\pi)$): Las intersecciones o raíces asimilando la proporción conocida se gestan en:
  $$u_1 = \frac{\pi}{3} \quad \text{(C. I)} \quad \text{y} \quad u_2 = \frac{2\pi}{3} \quad \text{(C. II)}$$
- **Segunda Rotación Continuante** (sobre el intervalo acoplado extra $[2\pi, 4\pi)$): Se le debe acumular al vector el valor del periodo general referencial $2\pi$ a las respuestas basales originarias:
  $$u_3 = \frac{\pi}{3} + 2\pi = \frac{7\pi}{3} \quad \text{y} \quad u_4 = \frac{2\pi}{3} + 2\pi = \frac{8\pi}{3}$$
- **Despeje y Restablecimiento ($x$ Inicial):** 
  En rigor normativo, al final del ejercicio nos abocamos directamente a deshacer la equivalencia original de $2x = u$, dividiendo por consiguiente la mitad a todos los resultados recabados y lograr posibilitar la respuesta base resolutoria para la función original de la ecuación:
  $$x = \frac{\frac{\pi}{3}}{2}, \frac{\frac{2\pi}{3}}{2}, \frac{\frac{7\pi}{3}}{2}, \frac{\frac{8\pi}{3}}{2}$$

**Conjunto Solución Comprobada:**
$$\mathbb{S} = \left\{\frac{\pi}{6}, \frac{\pi}{3}, \frac{7\pi}{6}, \frac{4\pi}{3}\right\}$$

### 10.4 Uso resolutorio de Identidades Fundamentales cruzadas

Es común que las ondas o ecuaciones mezclen componentes u oscilaciones distintas o funciones desbalanceadas (como tener la variable $x$ operando a la par contra un doblez $2x$). Tal factor es forzosamente incompatible de manera directa algebráica, obligándonos de forma metodológica vital a apelar a las **Identidades Trigonométricas Fundamentales** (Tema extenso visto previamente de rigor en la Sección 6) buscando poder homogeneizar paramétricamente sus factores hacia una variable unísona uniforme.

**Ejemplo 10.5 (Homogeneización analítica por medio de Ángulos Dobles):**
Resuelva formalmente la ecuación $\cos(2x) = \cos(x)$ para los casos posibles lícitos de cierre en $x \in [0, 2\pi)$.

**Solución paso a paso:**
- Es impracticable e imposible simplificar la igualdad mientras las frecuencias del coseno sean disímiles ($2x$ contra $x$). Convertiremos y reemplazaremos analíticamente acudiendo al axioma establecido para el propio **Coseno del Ángulo Doble**, el cual decreta su equivalencia universal como: $\cos(2x) = 2\cos^2(x) - 1$.
  Sustituyendo el vector de onda en nuestra operación logramos achatarlas y nivelar la ecuación completa a una sola escala natural cruzada de $x$:
  $$2\cos^2(x) - 1 = \cos(x)$$
- Reescribimos agrupándolo sistemáticamente en molde de ecuación cuadrática general para análisis igualada a cero:
  $$2\cos^2(x) - \cos(x) - 1 = 0$$
- Factorizamos de idéntico modo estructurado resolutorio al previamente operado del Ejemplo 10.3 (recurriendo brevemente a un factor algebraico de tipo $u = \cos(x)$):
  $$(2u + 1)(u - 1) = 0 \implies (2\cos(x) + 1)(\cos(x) - 1) = 0$$
- Esto nos faculta depurar en dos escenarios factibles e independientes referenciales originarios de raíces:
  $$ \cos(x) = 1 \quad \text{o} \quad \cos(x) = -\frac{1}{2}$$

**Escenario Alfa:** Evaluando $\cos(x) = 1$
Ocurre y verifica que sus raíces intersectan únicamente el dictamen asintótico y natural del origen temporal paramétrico:
$$x = 0$$

**Escenario Beta:** Evaluando la expresión $\cos(x) = -\frac{1}{2}$
Basándonos inicialmente determinando su ángulo paralelo base simple referencial (donde valdría un medio netamente puro $\frac{1}{2}$) como $\frac{\pi}{3}$, al evaluar que el requerimiento es cruzado y negativo ($-$) procedemos a resituarlo transversal estocástico proyectándolo de manera natural hacia dominios oeste:
- Espectro Cuadrante II: $x = \pi - \frac{\pi}{3} = \frac{2\pi}{3}$
- Espectro Cuadrante III: $x = \pi + \frac{\pi}{3} = \frac{4\pi}{3}$

**Conjunto Final y Global Restringido:**
$$\mathbb{S} = \left\{0, \frac{2\pi}{3}, \frac{4\pi}{3}\right\}$$

---
## 11. Teorema del seno y del coseno

Hasta el momento hemos abordado la trigonometría centrándonos en **triángulos rectángulos** (aquellos que poseen un ángulo recto de $90°$), lo cual simplifica la caracterización geométrica. Sin embargo, en la mayoría de los casos analíticos generales, los triángulos son **oblicuángulos** (ningún ángulo es recto). 

Para resolver cualquier triángulo general, disponemos de dos herramientas fundamentales: el **Teorema del Seno** y el **Teorema del Coseno**.

### 11.1 Notación estándar

Para enunciar los teoremas, estableceremos primero la convención geométrica habitual para el triángulo genérico $ABC$:

- Los **vértices** se identifican con letras mayúsculas latinas: $A, B, C$.
- Los **ángulos internos** relativos a cada vértice se denotan con letras griegas: $\alpha$ (en $A$), $\beta$ (en $B$), y $\gamma$ (en $C$).
- La longitud del **lado opuesto** a cada vértice se identifica con la letra minúscula homóloga: $a$ (frente a $A$), $b$ (frente a $B$), y $c$ (frente a $C$).

Por el postulado de geometría euclidiana, la suma interna de ángulos siempre cumple:
$$\alpha + \beta + \gamma = 180° = \pi$$

### 11.2 Teorema del Seno (Ley de Proporcionalidad)

**Motivación**
De manera intuitiva, en cualquier triángulo, el lado de mayor longitud siempre se opone al ángulo de mayor abertura. La Ley de Senos cuantifica esta proporción, estableciendo que el cociente entre la longitud de un lado y el seno de su ángulo opuesto es una constante analítica para los tres lados.

**Teorema 11.1 (Ley de senos):**
En todo triángulo $ABC$ con lados $a$, $b$, $c$ opuestos a los ángulos $\alpha$, $\beta$, $\gamma$ respectivamente:
$$\frac{a}{\sin(\alpha)} = \frac{b}{\sin(\beta)} = \frac{c}{\sin(\gamma)}$$


**Demostración Geométrica:**
1. Trazamos la altura $h$ vertical desde el vértice $C$ hacia el lado base $c$. Esto divide la figura en dos triángulos rectángulos independientes.
2. Analizamos el triángulo rectángulo de la izquierda (con ángulo $\alpha$):
   $$\sin(\alpha) = \frac{h}{b} \implies h = b\sin(\alpha)$$
3. Analizamos el triángulo rectángulo de la derecha (con ángulo $\beta$):
   $$\sin(\beta) = \frac{h}{a} \implies h = a\sin(\beta)$$
4. Como la altura $h$ es común, igualamos ambas expresiones:
   $$b\sin(\alpha) = a\sin(\beta) \implies \frac{a}{\sin(\alpha)} = \frac{b}{\sin(\beta)}$$
5. Repintiendo el mismo trazado con la altura de otro vértice, se demuestra la otra igualdad. $\blacksquare$

**Ejemplo 11.1 (Despeje lineal directo):**
En un triángulo $ABC$, sabemos que $\alpha = 30°$, $\beta = 45°$ y el lado $a = 8$. Calcule $b$.

**Solución paso a paso:**
- Por la ley de senos, relacionamos los lados y ángulos conocidos:
  $$\frac{a}{\sin(\alpha)} = \frac{b}{\sin(\beta)}$$
- Sustituimos por la información dada:
  $$\frac{8}{\sin(30°)} = \frac{b}{\sin(45°)}$$
- Despejamos el lado $b$:
  $$b = 8 \cdot \frac{\sin(45°)}{\sin(30°)}$$
- Empleamos nuestros ángulos notables deducidos matricialmente en la tabla de la Sección 4:
  $$b = 8 \cdot \frac{\frac{\sqrt{2}}{2}}{\frac{1}{2}} = 8\sqrt{2}$$

**Ejemplo 11.2 (Resolución angular oblicuángula):**
En un triángulo, $\beta = \frac{\pi}{6}$, $\gamma = \frac{\pi}{4}$ y el lado $b = 10$. Calcule el lado $c$ y el ángulo $\alpha$.

**Solución paso a paso:**
- **Paso 1: Ángulo faltante.** Por la suma interna, sabemos que el total debe ser $\pi$:
  $$\alpha = \pi - \left(\frac{\pi}{6} + \frac{\pi}{4}\right) = \pi - \frac{5\pi}{12} = \frac{7\pi}{12} \text{ rad}$$
- **Paso 2: Lado faltante.** Empleando la ley de senos para calcular el escalar $c$:
  $$\frac{c}{\sin(\gamma)} = \frac{b}{\sin(\beta)} \implies c = b \cdot \frac{\sin(\gamma)}{\sin(\beta)}$$
- Sustituimos utilizando nuestras identidades conocidas:
  $$c = 10 \cdot \frac{\sin(\frac{\pi}{4})}{\sin(\frac{\pi}{6})} = 10 \cdot \frac{\frac{\sqrt{2}}{2}}{\frac{1}{2}} = 10\sqrt{2}$$

> **El caso ambiguo (SSA):** Cuando al resolver la ecuación conocemos únicamente dos lados y el ángulo opuesto a uno de ellos, aplicar la función arco seno ($\arcsin$) podría dar lugar a **0, 1 o 2 triángulos posibles** diferentes simultáneamente viables. Esto es porque el seno es positivo y ambiguo tanto el cuadrante I (ángulo agudo) como en el cuadrante II (ángulo obtuso). Debemos corroborar si ambos resultados son lógicamente lícitos al someterlos a la suma máxima de $180°$.

### 11.3 Teorema del Coseno (Pitágoras Generalizado)

**Motivación**
Este teorema representa la **generalización del Teorema de Pitágoras** para cualquier triángulo. Cuando el ángulo estudiado es recto ($90°$), su $\cos(90°)$ vale $0$, evaporando el componente posterior y reduciendo la función netamente a $c^2 = a^2 + b^2$. 
Para ángulos distintos, el factor residual ($-2ab\cos(\gamma)$) ajusta y modifica la longitud: si es un ángulo agudo el coseno positivo obligará a generar una resta mermando el lado, si es obtuso el coseno negativo generará un factor final de suma.

**Teorema 11.2 (Ley de cosenos):**
En todo triángulo $ABC$, el cuadrado de cualquier lado equivale a la suma de los cuadrados de los otros dos lados, siempre disminuidos por el doble de su producto expresamente multiplicado por el coseno del ángulo comprendido entre ellos:
$$a^2 = b^2 + c^2 - 2bc\cos(\alpha)$$
$$b^2 = a^2 + c^2 - 2ac\cos(\beta)$$
$$c^2 = a^2 + b^2 - 2ab\cos(\gamma)$$

**Demostración (idea intuitiva):**
1. Situamos el triángulo en pleno plano cartesiano anclando el vértice $B$ en el origen $(0, 0)$ y $C$ con coordenadas escalares $(a, 0)$. 
2. El tercer vértice $A$ queda desvelado vectorialmente mediante trigonometría asumiendo posición en $(c\cos(\beta),\ c\sin(\beta))$.
3. Sabiendo que necesitamos buscar analíticamente la magnitud del lado de cierre opuesto dictaminado como $b = |AC|$, operamos con la simple y directa fórmula analítica de distancia punto a punto en el plano; este despeje conduce analíticamente exacto a la función madre: $b^2 = a^2 + c^2 - 2ac\cos(\beta)$. $\square$

**Ejemplo 11.3 (Aplicación directa para encontrar lados):**
En un triángulo oblicuángulo, conocemos los lados $a = 5$ y $b = 7$, sabiendo además que su ángulo comprendido opuesto a el vértice sobrante está dictaminado como $\gamma = 60°$. Calcule la magnitud del tercer lado $c$.

**Solución paso a paso:**
- Exponemos nuestra matriz resolutoria estructurada con respecto al factor $c$:
  $$c^2 = a^2 + b^2 - 2ab\cos(\gamma)$$
- Sustituimos utilizando nuestras magnitudes numéricas aportadas en el contexto:
  $$c^2 = (5)^2 + (7)^2 - 2(5)(7)\cos(60°)$$
- Intervenimos usando de nuestra tabla de saberes $\cos(60°) = \frac{1}{2}$ y operamos formalmente la aritmética:
  $$c^2 = 25 + 49 - 70 \cdot \left(\frac{1}{2}\right) = 74 - 35 = 39$$
- Rematamos nuestro ejercicio aplicando el exponente radical limitando a magnitud escalar neta:
  $$c = \sqrt{39}$$

**Ejemplo 11.4 (Aplicación deductiva inmersa para hallar ángulos por despejes):**
En un polígono rústico modelado disponemos sus longitudes de perimetría base total $a = 6$, $b = 8$ y $c = 10$. Buscaremos desvelar el ángulo subyacente paramétrico real contenido dentro de $\gamma$.

**Solución paso a paso:**
- Imponemos estructuradamente nuestra fórmula madre universal atada referencialmente al coseno de $\gamma$:
  $$c^2 = a^2 + b^2 - 2ab\cos(\gamma)$$
- Aislamos explícita y forzosamente este término mediante simple reubicación algebraica de variables:
  $$\cos(\gamma) = \frac{a^2 + b^2 - c^2}{2ab}$$
- Imbuimos en la fracción nuestro contexto numérico provisto a priori:
  $$\cos(\gamma) = \frac{6^2 + 8^2 - 10^2}{2(6)(8)}$$
- Resolvemos sistemáticamente el cálculo expuesto:
  $$\cos(\gamma) = \frac{36 + 64 - 100}{96} = \frac{100 - 100}{96} = \frac{0}{96} = 0$$
- Dictaminamos bajo evaluación: el encuadre trigonométrico ha convergido formalmente en que si $\cos(\gamma) = 0$; nuestra solución empírica innegable en un perímetro cerrado se traduce puntualmente recayendo de manera directa o natural sobre $\gamma = \frac{\pi}{2}$ radianes (lo expuesto comúnmente como $90°$).
  *(Tal conclusión es comprobable lógicamente y de forma inmediata sin aritmética, ya que advertimos a priori que nuestro triángulo en proporciones $6, 8, 10$ fungía puramente como un simple escalamiento del famosísimo rectángulo $3, 4, 5$).*

### 11.4 ¿Cuándo usar cada teorema?

| Datos conocidos del bloque triangular | Teorema o Ley obligada a emplear |
|:---|:---|
| 2 ángulos y 1 lado (AAS o ASA) | Ley de senos |
| 2 lados y ángulo opuesto no-comprendido (SSA) | Ley de senos (verificando minuciosamente el caso ambiguo) |
| 2 lados y el propio ángulo abrazado e inter-comprendido entre ellos (SAS) | Ley de cosenos |
| Lados totales cerrados puros (SSS) | Ley de cosenos |

---

## 12. Ejercicios propuestos

Resuelva los siguientes ejercicios, detallando su procedimiento paso a paso.

### 12.1 Conversión de Ángulos y Bases Elementales
1. Convierta a sexagesimal (grados): $\frac{5\pi}{6}$, $\frac{7\pi}{4}$ y $\frac{11\pi}{6}$.
2. Convierta a radianes: $15°$, $120°$ y $315°$.
3. Calcule el valor exacto de $\sin(15°)$ usando la fórmula de resta de ángulos apoyándose en $45°$ y $30°$.

### 12.2 Funciones Básicas y Razones Recíprocas
4. En un triángulo rectángulo con hipotenusa de $13$ y un cateto de $5$, determine las seis funciones trigonométricas del ángulo agudo menor.
5. Calcule el Seno de todos los ángulos interiores de un triángulo rectángulo de lados $3, 4, 5$.
6. Si $\sec(\theta) = -3$ y el ángulo $\theta$ está en el segundo cuadrante, determine el valor exacto de $\sin(\theta)$ y $\cot(\theta)$.

### 12.3 Demostración de Identidades Fundamentales
Demuestre las siguientes identidades:
7. $\frac{1 - \sin^2(\theta)}{\cos(\theta)} = \cos(\theta)$
8. $(\sin(x) + \cos(x))^2 = 1 + \sin(2x)$
9. $\frac{\tan(\theta) + \cot(\theta)}{\sec(\theta)} = \csc(\theta)$
10. Demuestre que $\cos(3\theta) = 4\cos^3(\theta) - 3\cos(\theta)$ (Pista: use la suma de ángulos con $(2\theta + \theta)$).

### 12.4 Ecuaciones Trigonométricas Analíticas
Encuentre las soluciones en el intervalo $x \in [0, 2\pi)$. Detalle el ángulo de referencia utilizado.
11. $2\cos(x) + \sqrt{3} = 0$
12. $2\sin^2(x) - \sin(x) - 1 = 0$
13. $\tan^2(x) - 3 = 0$

Encuentre la **solución general** para todos los reales (usando multiplicadores $+2k\pi$ o similares) de las siguientes ecuaciones:
14. $\sin(2x) = \frac{1}{2}$
15. $\cos^2(x) - \sin^2(x) = \frac{\sqrt{2}}{2}$

### 12.5 Teoremas del Seno y del Coseno (Polígonos Oblicuángulos)
16. Un terreno triangular tiene dos lados que miden $15 \text{m}$ y $20 \text{m}$. Si el ángulo comprendido entre ellos es de $120°$, calcule la longitud del tercer lado.
17. Resuelva un triángulo con dimensiones $a = 12$, $b = 12\sqrt{3}$ y $\alpha = 30°$. Calcule el ángulo $\beta$ y verifique exhaustivamente si ocurre el "caso ambiguo" (donde dos ángulos sean posibles).
18. Demuestre mediante el Teorema del Coseno que el triángulo de configuración $a=3, b=4, c=5$ tiene obligatoriamente un ángulo de $90°$ opuesto al lado $c$.

### 12.6 Tópicos Complementarios (Curva Paramétrica y Desfases)
19. Escriba la ecuación paramétrica de un punto oscilante sobre un círculo de radio $5$, cuyo centro ha sido desplazado hacia la coordenada $(3, -2)$.
20. Dada la función $f(t) = -4\sin\!\left(2\pi t - \frac{\pi}{2}\right) + 1$, determine su magnitud de amplitud, su período, su desfase horizontal y su traslación vertical.

---

**Fin de la Clase 6**
