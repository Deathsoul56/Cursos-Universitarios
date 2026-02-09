# Guía 5 - Límites y Continuidad

## Índice de contenidos

1. [Concepto intuitivo de límite](#1-concepto-intuitivo-de-límite)
2. [Cálculo de límites algebraicos](#2-cálculo-de-límites-algebraicos)
3. [Límites laterales](#3-límites-laterales)
4. [Límites infinitos](#4-límites-infinitos)
5. [Límites al infinito](#5-límites-al-infinito)
6. [Indeterminaciones](#6-indeterminaciones)
7. [Límites trigonométricos](#7-límites-trigonométricos)
8. [Continuidad](#8-continuidad)
9. [Teoremas sobre funciones continuas](#9-teoremas-sobre-funciones-continuas)
10. [Soluciones](#10-soluciones)

---

## 1. Concepto intuitivo de límite

### Teoría breve

**Definición informal:** $\lim_{x \to a} f(x) = L$ significa que cuando $x$ se acerca a $a$ (sin necesariamente alcanzarlo), $f(x)$ se acerca a $L$.

**Notación:**
- $\lim_{x \to a} f(x) = L$: límite cuando $x$ tiende a $a$
- $\lim_{x \to a^+} f(x)$: límite por la derecha
- $\lim_{x \to a^-} f(x)$: límite por la izquierda

**Propiedades básicas:**
- $\lim_{x \to a} [f(x) + g(x)] = \lim_{x \to a} f(x) + \lim_{x \to a} g(x)$
- $\lim_{x \to a} [f(x) \cdot g(x)] = \lim_{x \to a} f(x) \cdot \lim_{x \to a} g(x)$
- $\lim_{x \to a} \frac{f(x)}{g(x)} = \frac{\lim_{x \to a} f(x)}{\lim_{x \to a} g(x)}$ si $\lim_{x \to a} g(x) \neq 0$

---

### 1.1 Interpretación gráfica ⭐

Observe las gráficas y determine los límites indicados:

**1.1.1** Para $f(x) = \frac{x^2 - 4}{x - 2}$, estime $\lim_{x \to 2} f(x)$ usando una tabla de valores cercanos a $x = 2$.

**1.1.2** Dada la gráfica de una función, determine si existe $\lim_{x \to 1} f(x)$ cuando:
- $f(1)$ no está definida pero la función se acerca a $3$ desde ambos lados.

**1.1.3** Estime $\lim_{x \to 0} \frac{\sin x}{x}$ usando valores cercanos a $0$.

**1.1.4** Para $f(x) = |x|$, calcule $\lim_{x \to 0} f(x)$.

**1.1.5** Determine $\lim_{x \to 3} (2x + 1)$ usando sustitución directa.

---

### 1.2 Límites de funciones simples ⭐

Calcule los siguientes límites:

**1.2.1** $\lim_{x \to 2} (3x - 5)$

**1.2.2** $\lim_{x \to 1} (x^2 + 2x - 3)$

**1.2.3** $\lim_{x \to -1} (x^3 - x)$

**1.2.4** $\lim_{x \to 0} (5x^2 + 3x + 1)$

**1.2.5** $\lim_{x \to 4} \sqrt{x + 5}$

**1.2.6** $\lim_{x \to 2} \frac{x + 3}{x - 1}$

---

### 1.3 Existencia de límites ⭐⭐

Determine si existen los siguientes límites:

**1.3.1** $\lim_{x \to 0} \frac{|x|}{x}$

**1.3.2** $\lim_{x \to 1} \frac{x^2 - 1}{x - 1}$

**1.3.3** $\lim_{x \to 0} \frac{1}{x^2}$

**1.3.4** Para $f(x) = \begin{cases} x + 1 & \text{si } x < 2 \\ x^2 & \text{si } x \geq 2 \end{cases}$, determine $\lim_{x \to 2} f(x)$.

**1.3.5** $\lim_{x \to 3} \frac{x^2 - 9}{x^2 - 6x + 9}$

---

## 2. Cálculo de límites algebraicos

### Teoría breve

**Técnicas para calcular límites:**

1. **Sustitución directa:** Si $f$ es continua en $a$, entonces $\lim_{x \to a} f(x) = f(a)$

2. **Factorización:** Para indeterminaciones $\frac{0}{0}$, factorice y simplifique

3. **Racionalización:** Para expresiones con radicales

4. **Álgebra:** Simplificación algebraica

---

### 2.1 Límites por factorización ⭐⭐

**2.1.1** $\lim_{x \to 2} \frac{x^2 - 4}{x - 2}$

**2.1.2** $\lim_{x \to 3} \frac{x^2 - 9}{x - 3}$

**2.1.3** $\lim_{x \to -1} \frac{x^2 + 3x + 2}{x + 1}$

**2.1.4** $\lim_{x \to 5} \frac{x^2 - 25}{x^2 - 7x + 10}$

**2.1.5** $\lim_{x \to 4} \frac{x^3 - 64}{x - 4}$

**2.1.6** $\lim_{x \to 1} \frac{x^3 - 1}{x^2 - 1}$

**2.1.7** $\lim_{x \to -2} \frac{x^3 + 8}{x^2 - 4}$

**2.1.8** $\lim_{x \to 0} \frac{x^2 + 5x}{x}$

---

### 2.2 Límites por racionalización ⭐⭐

**2.2.1** $\lim_{x \to 0} \frac{\sqrt{x + 4} - 2}{x}$

**2.2.2** $\lim_{x \to 3} \frac{x - 3}{\sqrt{x + 1} - 2}$

**2.2.3** $\lim_{x \to 0} \frac{\sqrt{1 + x} - 1}{x}$

**2.2.4** $\lim_{x \to 5} \frac{x - 5}{\sqrt{x} - \sqrt{5}}$

**2.2.5** $\lim_{x \to 0} \frac{\sqrt{4 + x} - \sqrt{4 - x}}{x}$

**2.2.6** $\lim_{x \to 0} \frac{x}{\sqrt{x + 1} - 1}$

---

### 2.3 Límites con expresiones complejas ⭐⭐⭐

**2.3.1** $\lim_{x \to 1} \frac{\frac{1}{x} - 1}{x - 1}$

**2.3.2** $\lim_{x \to 2} \frac{\frac{1}{x} - \frac{1}{2}}{x - 2}$

**2.3.3** $\lim_{x \to 0} \frac{\frac{1}{x + 3} - \frac{1}{3}}{x}$

**2.3.4** $\lim_{h \to 0} \frac{(x + h)^2 - x^2}{h}$

**2.3.5** $\lim_{h \to 0} \frac{\sqrt{x + h} - \sqrt{x}}{h}$

**2.3.6** $\lim_{x \to 0} \frac{(1 + x)^3 - 1}{x}$

---

## 3. Límites laterales

### Teoría breve

**Definición:** 
- **Límite por la derecha:** $\lim_{x \to a^+} f(x)$ (cuando $x$ se acerca a $a$ con $x > a$)
- **Límite por la izquierda:** $\lim_{x \to a^-} f(x)$ (cuando $x$ se acerca a $a$ con $x < a$)

**Teorema:** $\lim_{x \to a} f(x)$ existe si y solo si $\lim_{x \to a^+} f(x) = \lim_{x \to a^-} f(x)$

---

### 3.1 Límites laterales básicos ⭐⭐

**3.1.1** $\lim_{x \to 0^+} \frac{|x|}{x}$ y $\lim_{x \to 0^-} \frac{|x|}{x}$

**3.1.2** Para $f(x) = \begin{cases} x + 2 & \text{si } x < 1 \\ 3x & \text{si } x \geq 1 \end{cases}$, calcule $\lim_{x \to 1^-} f(x)$ y $\lim_{x \to 1^+} f(x)$.

**3.1.3** $\lim_{x \to 2^-} \frac{x - 2}{|x - 2|}$ y $\lim_{x \to 2^+} \frac{x - 2}{|x - 2|}$

**3.1.4** Para $g(x) = \begin{cases} x^2 & \text{si } x < 0 \\ 2x & \text{si } x \geq 0 \end{cases}$, determine si existe $\lim_{x \to 0} g(x)$.

**3.1.5** $\lim_{x \to 3^-} \frac{|x - 3|}{x - 3}$ y $\lim_{x \to 3^+} \frac{|x - 3|}{x - 3}$

---

### 3.2 Funciones definidas por partes ⭐⭐

**3.2.1** Para $f(x) = \begin{cases} 2x + 1 & \text{si } x \leq 2 \\ x^2 - 1 & \text{si } x > 2 \end{cases}$, calcule $\lim_{x \to 2} f(x)$ si existe.

**3.2.2** Para $h(x) = \begin{cases} x^2 - 4 & \text{si } x < -2 \\ 0 & \text{si } x = -2 \\ 4 - x^2 & \text{si } x > -2 \end{cases}$, determine $\lim_{x \to -2} h(x)$.

**3.2.3** Determine el valor de $a$ para que exista $\lim_{x \to 1} f(x)$ donde:
$$f(x) = \begin{cases} 3x + a & \text{si } x < 1 \\ 2x^2 + 1 & \text{si } x \geq 1 \end{cases}$$

**3.2.4** Para $g(x) = \begin{cases} \frac{x^2 - 9}{x - 3} & \text{si } x \neq 3 \\ k & \text{si } x = 3 \end{cases}$, ¿qué valor debe tener $k$ para que $g$ sea continua en $x = 3$?

**3.2.5** Determine $\lim_{x \to 0} f(x)$ donde $f(x) = \begin{cases} \frac{\sin x}{x} & \text{si } x < 0 \\ 1 & \text{si } x \geq 0 \end{cases}$

---

## 4. Límites infinitos

### Teoría breve

**Definición:** $\lim_{x \to a} f(x) = \infty$ significa que $f(x)$ crece sin límite cuando $x \to a$.

**Asíntotas verticales:** Si $\lim_{x \to a} f(x) = \pm\infty$, entonces $x = a$ es una **asíntota vertical**.

---

### 4.1 Límites infinitos básicos ⭐⭐

**4.1.1** $\lim_{x \to 0^+} \frac{1}{x}$ y $\lim_{x \to 0^-} \frac{1}{x}$

**4.1.2** $\lim_{x \to 0} \frac{1}{x^2}$

**4.1.3** $\lim_{x \to 3^+} \frac{1}{x - 3}$ y $\lim_{x \to 3^-} \frac{1}{x - 3}$

**4.1.4** $\lim_{x \to 2} \frac{x + 1}{(x - 2)^2}$

**4.1.5** $\lim_{x \to -1^+} \frac{x}{x + 1}$ y $\lim_{x \to -1^-} \frac{x}{x + 1}$

**4.1.6** $\lim_{x \to 4} \frac{x - 1}{x^2 - 16}$

---

### 4.2 Asíntotas verticales ⭐⭐

Identifique las asíntotas verticales y calcule los límites laterales:

**4.2.1** $f(x) = \frac{x}{x^2 - 9}$

**4.2.2** $f(x) = \frac{2x}{x^2 - 4}$

**4.2.3** $f(x) = \frac{x^2 + 1}{x^2 - 5x + 6}$

**4.2.4** $f(x) = \frac{1}{x^2 + x - 6}$

**4.2.5** $f(x) = \frac{x - 1}{x^3 - x}$

---

## 5. Límites al infinito

### Teoría breve

**Definición:** $\lim_{x \to \infty} f(x) = L$ significa que $f(x)$ se acerca a $L$ cuando $x$ crece indefinidamente.

**Asíntotas horizontales:** Si $\lim_{x \to \pm\infty} f(x) = L$, entonces $y = L$ es una **asíntota horizontal**.

**Regla práctica para funciones racionales:**
$$\lim_{x \to \infty} \frac{a_n x^n + \ldots + a_0}{b_m x^m + \ldots + b_0} = \begin{cases} 0 & \text{si } n < m \\ \frac{a_n}{b_m} & \text{si } n = m \\ \pm\infty & \text{si } n > m \end{cases}$$

---

### 5.1 Límites al infinito de funciones racionales ⭐⭐

**5.1.1** $\lim_{x \to \infty} \frac{3x + 2}{x - 1}$

**5.1.2** $\lim_{x \to \infty} \frac{x^2 - 1}{2x^2 + 3}$

**5.1.3** $\lim_{x \to \infty} \frac{5x^3 + 2x}{x^3 - x + 1}$

**5.1.4** $\lim_{x \to \infty} \frac{2x}{x^2 + 1}$

**5.1.5** $\lim_{x \to \infty} \frac{4x^2 - x + 3}{2x - 5}$

**5.1.6** $\lim_{x \to -\infty} \frac{x^3 + 2x^2}{x^2 - 1}$

**5.1.7** $\lim_{x \to \infty} \frac{\sqrt{x^2 + 1}}{x}$

**5.1.8** $\lim_{x \to \infty} \frac{3x - 1}{7x + 2}$

---

### 5.2 Límites con radicales ⭐⭐⭐

**5.2.1** $\lim_{x \to \infty} \left(\sqrt{x + 1} - \sqrt{x}\right)$

**5.2.2** $\lim_{x \to \infty} \frac{\sqrt{x^2 + x}}{x + 1}$

**5.2.3** $\lim_{x \to \infty} \left(\sqrt{x^2 + 2x} - x\right)$

**5.2.4** $\lim_{x \to \infty} \frac{x}{\sqrt{4x^2 + 1}}$

**5.2.5** $\lim_{x \to -\infty} \frac{x}{\sqrt{x^2 + 1}}$

**5.2.6** $\lim_{x \to \infty} \sqrt{x}\left(\sqrt{x + 1} - \sqrt{x}\right)$

---

### 5.3 Asíntotas horizontales ⭐⭐

Determine las asíntotas horizontales de las siguientes funciones:

**5.3.1** $f(x) = \frac{2x^2 + 3}{x^2 - 1}$

**5.3.2** $f(x) = \frac{5x - 3}{x + 2}$

**5.3.3** $f(x) = \frac{x^3 + 1}{x^2 + 4}$

**5.3.4** $f(x) = \frac{\sqrt{9x^2 + 1}}{3x - 2}$

**5.3.5** $f(x) = \frac{e^x}{e^x + 1}$ (considere $x \to \infty$ y $x \to -\infty$)

---

## 6. Indeterminaciones

### Teoría breve

**Formas indeterminadas:**
- $\frac{0}{0}$: Factorice o racionalice
- $\frac{\infty}{\infty}$: Divida por la mayor potencia
- $0 \cdot \infty$: Convierta a $\frac{0}{0}$ o $\frac{\infty}{\infty}$
- $\infty - \infty$: Racionalice o use álgebra
- $0^0$, $1^\infty$, $\infty^0$: Use logaritmos (Regla de L'Hôpital en cursos avanzados)

---

### 6.1 Indeterminación 0/0 ⭐⭐

**6.1.1** $\lim_{x \to 1} \frac{x^2 - 1}{x - 1}$

**6.1.2** $\lim_{x \to 0} \frac{\sin(3x)}{x}$ (use $\lim_{x \to 0} \frac{\sin x}{x} = 1$)

**6.1.3** $\lim_{x \to 0} \frac{1 - \cos x}{x^2}$ (use $\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}$)

**6.1.4** $\lim_{x \to 2} \frac{x^3 - 8}{x^2 - 4}$

**6.1.5** $\lim_{x \to 0} \frac{\sqrt{1 + x} - 1}{x}$

---

### 6.2 Indeterminación ∞/∞ ⭐⭐

**6.2.1** $\lim_{x \to \infty} \frac{5x^2 + 3x}{2x^2 - x + 1}$

**6.2.2** $\lim_{x \to \infty} \frac{x^3 + 2x^2 - 1}{4x^3 - 5}$

**6.2.3** $\lim_{x \to \infty} \frac{\sqrt{x^2 + x}}{2x + 1}$

**6.2.4** $\lim_{x \to \infty} \frac{e^x}{x^2}$ (crece exponencial > polinomial)

**6.2.5** $\lim_{x \to \infty} \frac{\ln x}{x}$ (crece logarítmico < lineal)

---

### 6.3 Indeterminación ∞ - ∞ ⭐⭐⭐

**6.3.1** $\lim_{x \to \infty} \left(\sqrt{x^2 + x} - x\right)$

**6.3.2** $\lim_{x \to \infty} \left(\sqrt{x^2 + 4x} - \sqrt{x^2 + x}\right)$

**6.3.3** $\lim_{x \to \infty} \left(x - \sqrt{x^2 - 1}\right)$

**6.3.4** $\lim_{x \to \infty} \left(\sqrt{4x^2 + 1} - 2x\right)$

**6.3.5** $\lim_{x \to 0^+} \left(\frac{1}{x} - \frac{1}{\sin x}\right)$

---

## 7. Límites trigonométricos

### Teoría breve

**Límites fundamentales:**
$$\lim_{x \to 0} \frac{\sin x}{x} = 1$$
$$\lim_{x \to 0} \frac{1 - \cos x}{x} = 0$$
$$\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}$$
$$\lim_{x \to 0} \frac{\tan x}{x} = 1$$

---

### 7.1 Límites trigonométricos básicos ⭐⭐

**7.1.1** $\lim_{x \to 0} \frac{\sin(2x)}{x}$

**7.1.2** $\lim_{x \to 0} \frac{\sin(5x)}{\sin(3x)}$

**7.1.3** $\lim_{x \to 0} \frac{\tan x}{x}$

**7.1.4** $\lim_{x \to 0} \frac{1 - \cos x}{x}$

**7.1.5** $\lim_{x \to 0} \frac{\sin^2 x}{x}$

**7.1.6** $\lim_{x \to 0} \frac{x}{\sin(3x)}$

**7.1.7** $\lim_{x \to 0} \frac{\sin x \cos x}{x}$

**7.1.8** $\lim_{x \to 0} \frac{1 - \cos(2x)}{x^2}$

---

### 7.2 Límites trigonométricos complejos ⭐⭐⭐

**7.2.1** $\lim_{x \to 0} \frac{\sin x - x}{x^3}$ (use $\sin x \approx x - \frac{x^3}{6}$ para $x$ pequeño)

**7.2.2** $\lim_{x \to 0} \frac{\tan x - \sin x}{x^3}$

**7.2.3** $\lim_{x \to 0} \frac{\sin(ax)}{\sin(bx)}$ donde $a, b \neq 0$

**7.2.4** $\lim_{x \to 0} \frac{x - \sin x}{x^3}$

**7.2.5** $\lim_{x \to 0} \frac{\sin x - \tan x}{x^3}$

**7.2.6** $\lim_{x \to \pi} \frac{\sin x}{x - \pi}$

---

## 8. Continuidad

### Teoría breve

**Definición:** Una función $f$ es **continua en $x = a$** si:
1. $f(a)$ está definida
2. $\lim_{x \to a} f(x)$ existe
3. $\lim_{x \to a} f(x) = f(a)$

**Tipos de discontinuidad:**
- **Evitable:** El límite existe pero no coincide con $f(a)$
- **De salto:** Límites laterales diferentes
- **Infinita:** Al menos un límite lateral es infinito
- **Esencial:** El límite no existe

**Teorema:** Polinomios, funciones racionales (en su dominio), $\sin x$, $\cos x$, $e^x$, $\ln x$ (en su dominio) son continuas.

---

### 8.1 Verificar continuidad ⭐⭐

Determine si las siguientes funciones son continuas en el punto indicado:

**8.1.1** $f(x) = \frac{x^2 - 4}{x - 2}$ en $x = 2$

**8.1.2** $g(x) = \begin{cases} x^2 & \text{si } x \neq 1 \\ 2 & \text{si } x = 1 \end{cases}$ en $x = 1$

**8.1.3** $h(x) = \frac{\sin x}{x}$ en $x = 0$ (defina $h(0)$ apropiadamente)

**8.1.4** $f(x) = |x|$ en $x = 0$

**8.1.5** $g(x) = \frac{1}{x}$ en $x = 0$

**8.1.6** $f(x) = \sqrt{x}$ en $x = 0$

---

### 8.2 Clasificar discontinuidades ⭐⭐

Clasifique el tipo de discontinuidad (si existe) en el punto indicado:

**8.2.1** $f(x) = \frac{x^2 - 1}{x - 1}$ en $x = 1$

**8.2.2** $f(x) = \begin{cases} x + 1 & \text{si } x < 0 \\ x - 1 & \text{si } x \geq 0 \end{cases}$ en $x = 0$

**8.2.3** $f(x) = \frac{1}{x - 3}$ en $x = 3$

**8.2.4** $f(x) = \lfloor x \rfloor$ (función parte entera) en $x = 2$

**8.2.5** $f(x) = \frac{\sin x}{x}$ en $x = 0$ (sin redefinir)

**8.2.6** $f(x) = \begin{cases} \frac{x^2 - 9}{x - 3} & \text{si } x \neq 3 \\ 5 & \text{si } x = 3 \end{cases}$ en $x = 3$

---

### 8.3 Hacer continua una función ⭐⭐⭐

Determine el valor de la constante para que la función sea continua en el punto indicado:

**8.3.1** $f(x) = \begin{cases} \frac{x^2 - 4}{x - 2} & \text{si } x \neq 2 \\ k & \text{si } x = 2 \end{cases}$ en $x = 2$

**8.3.2** $g(x) = \begin{cases} 3x + a & \text{si } x < 1 \\ x^2 + 2 & \text{si } x \geq 1 \end{cases}$ en $x = 1$

**8.3.3** $h(x) = \begin{cases} \frac{\sin(ax)}{x} & \text{si } x \neq 0 \\ 5 & \text{si } x = 0 \end{cases}$ en $x = 0$

**8.3.4** $f(x) = \begin{cases} x^2 - bx & \text{si } x < 2 \\ 4 & \text{si } x = 2 \\ 3x - b & \text{si } x > 2 \end{cases}$ en $x = 2$

**8.3.5** $g(x) = \begin{cases} \frac{\sqrt{x + c} - 2}{x - 1} & \text{si } x \neq 1 \\ \frac{1}{4} & \text{si } x = 1 \end{cases}$ en $x = 1$

---

### 8.4 Continuidad en intervalos ⭐⭐

Determine los intervalos donde la función es continua:

**8.4.1** $f(x) = \frac{x + 1}{x^2 - 4}$

**8.4.2** $g(x) = \sqrt{4 - x^2}$

**8.4.3** $h(x) = \frac{1}{\sqrt{x - 1}}$

**8.4.4** $f(x) = \frac{x}{|x|}$

**8.4.5** $g(x) = \ln(x^2 - 1)$

**8.4.6** $h(x) = \tan x$

---

## 9. Teoremas sobre funciones continuas

### Teoría breve

**Teorema del Valor Intermedio (TVI):** Si $f$ es continua en $[a, b]$ y $k$ está entre $f(a)$ y $f(b)$, entonces existe $c \in (a, b)$ tal que $f(c) = k$.

**Aplicación:** Demostrar existencia de raíces.

**Teorema del Valor Extremo:** Si $f$ es continua en $[a, b]$, entonces $f$ alcanza su máximo y mínimo en $[a, b]$.

---

### 9.1 Teorema del Valor Intermedio ⭐⭐

**9.1.1** Demuestre que $f(x) = x^3 - 2x - 5$ tiene al menos una raíz en $[2, 3]$.

**9.1.2** Pruebe que $g(x) = \cos x - x$ tiene al menos una raíz en $[0, \frac{\pi}{2}]$.

**9.1.3** Demuestre que la ecuación $x^5 + x - 1 = 0$ tiene solución en $[0, 1]$.

**9.1.4** Pruebe que $h(x) = \sqrt{x} - \frac{1}{x}$ tiene una raíz en $[1, 2]$.

**9.1.5** Demuestre que existe $c \in [0, 1]$ tal que $c^3 + c = 1$.

---

### 9.2 Aplicaciones del TVI ⭐⭐⭐

**9.2.1** Un objeto cae desde 100 m de altura. Su altura en el tiempo $t$ es $h(t) = 100 - 5t^2$. Use el TVI para demostrar que en algún momento entre $t = 0$ y $t = 5$, el objeto está a 50 m de altura.

**9.2.2** La temperatura varía según $T(t) = 20 + 10\sin\left(\frac{\pi t}{12}\right)$ (en °C) durante el día. Demuestre que en algún momento $T = 25°C$.

**9.2.3** Demuestre que las gráficas de $y = x^3$ y $y = 2^x$ se intersectan en algún punto con $1 < x < 2$.

**9.2.4** Pruebe que existe un ángulo $\theta \in (0, \frac{\pi}{2})$ tal que $\sin\theta = \cos\theta$.

**9.2.5** Demuestre que $f(x) = x^4 - x - 3$ tiene exactamente dos raíces reales.

---

### 9.3 Análisis de funciones continuas ⭐⭐⭐

**9.3.1** Si $f$ y $g$ son continuas en $[a, b]$ con $f(a) < g(a)$ y $f(b) > g(b)$, demuestre que existe $c \in (a, b)$ donde $f(c) = g(c)$.

**9.3.2** Sea $f$ continua en $[0, 1]$ con $f(0) = f(1)$. Demuestre que existe $c \in [0, \frac{1}{2}]$ tal que $f(c) = f(c + \frac{1}{2})$.

**9.3.3** Si $f$ es continua en $\mathbb{R}$ y $\lim_{x \to \infty} f(x) = \lim_{x \to -\infty} f(x) = 0$, demuestre que $f$ alcanza su máximo absoluto.

**9.3.4** Demuestre que toda función continua en un intervalo cerrado es acotada.

**9.3.5** Si $f$ es continua y $f(x) > 0$ para todo $x \in [a, b]$, demuestre que existe $m > 0$ tal que $f(x) \geq m$ para todo $x \in [a, b]$.

---

## 10. Soluciones

<details>
<summary><b>Ver soluciones - Sección 1.1 (Interpretación gráfica)</b></summary>

### Soluciones Ejercicio 1.1

**1.1.1** Tabla de valores:

| $x$ | 1.9 | 1.99 | 1.999 | 2.001 | 2.01 | 2.1 |
|-----|-----|------|-------|-------|------|-----|
| $f(x)$ | 3.9 | 3.99 | 3.999 | 4.001 | 4.01 | 4.1 |

$\lim_{x \to 2} f(x) = 4$

---

**1.1.2** Si la función se acerca a $3$ desde ambos lados, entonces $\lim_{x \to 1} f(x) = 3$, aunque $f(1)$ no esté definida.

---

**1.1.3** Tabla:

| $x$ | $\pm 0.1$ | $\pm 0.01$ | $\pm 0.001$ |
|-----|-----------|------------|-------------|
| $\frac{\sin x}{x}$ | $\approx 0.998$ | $\approx 0.99998$ | $\approx 0.9999998$ |

$\lim_{x \to 0} \frac{\sin x}{x} = 1$

---

**1.1.4** $\lim_{x \to 0} |x| = 0$ (la función se acerca a $0$ desde ambos lados)

---

**1.1.5** Sustitución directa: $\lim_{x \to 3} (2x + 1) = 2(3) + 1 = 7$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 1.2 (Límites de funciones simples)</b></summary>

### Soluciones Ejercicio 1.2

**1.2.1** $\lim_{x \to 2} (3x - 5) = 3(2) - 5 = 1$

**1.2.2** $\lim_{x \to 1} (x^2 + 2x - 3) = 1 + 2 - 3 = 0$

**1.2.3** $\lim_{x \to -1} (x^3 - x) = (-1)^3 - (-1) = -1 + 1 = 0$

**1.2.4** $\lim_{x \to 0} (5x^2 + 3x + 1) = 0 + 0 + 1 = 1$

**1.2.5** $\lim_{x \to 4} \sqrt{x + 5} = \sqrt{9} = 3$

**1.2.6** $\lim_{x \to 2} \frac{x + 3}{x - 1} = \frac{5}{1} = 5$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 1.3 (Existencia de límites)</b></summary>

### Soluciones Ejercicio 1.3

**1.3.1** $\lim_{x \to 0^+} \frac{|x|}{x} = \lim_{x \to 0^+} \frac{x}{x} = 1$

$\lim_{x \to 0^-} \frac{|x|}{x} = \lim_{x \to 0^-} \frac{-x}{x} = -1$

Como los límites laterales son diferentes, **el límite no existe**.

---

**1.3.2** $\lim_{x \to 1} \frac{x^2 - 1}{x - 1} = \lim_{x \to 1} \frac{(x-1)(x+1)}{x - 1} = \lim_{x \to 1} (x + 1) = 2$

---

**1.3.3** $\lim_{x \to 0^+} \frac{1}{x^2} = +\infty$ y $\lim_{x \to 0^-} \frac{1}{x^2} = +\infty$

El límite es $+\infty$ (no existe como número real).

---

**1.3.4** $\lim_{x \to 2^-} f(x) = 2 + 1 = 3$

$\lim_{x \to 2^+} f(x) = 2^2 = 4$

Como $3 \neq 4$, **el límite no existe**.

---

**1.3.5** $\lim_{x \to 3} \frac{x^2 - 9}{x^2 - 6x + 9} = \lim_{x \to 3} \frac{(x-3)(x+3)}{(x-3)^2} = \lim_{x \to 3} \frac{x+3}{x-3} = \pm\infty$

**El límite no existe** (discontinuidad infinita).

</details>

---

<details>
<summary><b>Ver soluciones - Sección 2.1 (Límites por factorización)</b></summary>

### Soluciones Ejercicio 2.1

**2.1.1** $\lim_{x \to 2} \frac{x^2 - 4}{x - 2} = \lim_{x \to 2} \frac{(x-2)(x+2)}{x - 2} = \lim_{x \to 2} (x + 2) = 4$

---

**2.1.2** $\lim_{x \to 3} \frac{x^2 - 9}{x - 3} = \lim_{x \to 3} (x + 3) = 6$

---

**2.1.3** $\lim_{x \to -1} \frac{x^2 + 3x + 2}{x + 1} = \lim_{x \to -1} \frac{(x+1)(x+2)}{x + 1} = \lim_{x \to -1} (x + 2) = 1$

---

**2.1.4** $\lim_{x \to 5} \frac{x^2 - 25}{x^2 - 7x + 10} = \lim_{x \to 5} \frac{(x-5)(x+5)}{(x-5)(x-2)} = \lim_{x \to 5} \frac{x+5}{x-2} = \frac{10}{3}$

---

**2.1.5** $\lim_{x \to 4} \frac{x^3 - 64}{x - 4} = \lim_{x \to 4} \frac{(x-4)(x^2+4x+16)}{x - 4} = \lim_{x \to 4} (x^2 + 4x + 16) = 48$

---

**2.1.6** $\lim_{x \to 1} \frac{x^3 - 1}{x^2 - 1} = \lim_{x \to 1} \frac{(x-1)(x^2+x+1)}{(x-1)(x+1)} = \lim_{x \to 1} \frac{x^2+x+1}{x+1} = \frac{3}{2}$

---

**2.1.7** $\lim_{x \to -2} \frac{x^3 + 8}{x^2 - 4} = \lim_{x \to -2} \frac{(x+2)(x^2-2x+4)}{(x-2)(x+2)} = \lim_{x \to -2} \frac{x^2-2x+4}{x-2} = \frac{12}{-4} = -3$

---

**2.1.8** $\lim_{x \to 0} \frac{x^2 + 5x}{x} = \lim_{x \to 0} (x + 5) = 5$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 2.2 (Límites por racionalización)</b></summary>

### Soluciones Ejercicio 2.2

**2.2.1** $\lim_{x \to 0} \frac{\sqrt{x + 4} - 2}{x} \cdot \frac{\sqrt{x + 4} + 2}{\sqrt{x + 4} + 2}$

$= \lim_{x \to 0} \frac{x + 4 - 4}{x(\sqrt{x + 4} + 2)} = \lim_{x \to 0} \frac{1}{\sqrt{x + 4} + 2} = \frac{1}{4}$

---

**2.2.2** $\lim_{x \to 3} \frac{x - 3}{\sqrt{x + 1} - 2} \cdot \frac{\sqrt{x + 1} + 2}{\sqrt{x + 1} + 2}$

$= \lim_{x \to 3} \frac{(x - 3)(\sqrt{x + 1} + 2)}{x + 1 - 4} = \lim_{x \to 3} \frac{(x - 3)(\sqrt{x + 1} + 2)}{x - 3} = \lim_{x \to 3} (\sqrt{x + 1} + 2) = 4$

---

**2.2.3** $\lim_{x \to 0} \frac{\sqrt{1 + x} - 1}{x} = \lim_{x \to 0} \frac{1}{\sqrt{1 + x} + 1} = \frac{1}{2}$

---

**2.2.4** $\lim_{x \to 5} \frac{x - 5}{\sqrt{x} - \sqrt{5}} \cdot \frac{\sqrt{x} + \sqrt{5}}{\sqrt{x} + \sqrt{5}} = \lim_{x \to 5} \frac{(x - 5)(\sqrt{x} + \sqrt{5})}{x - 5} = 2\sqrt{5}$

---

**2.2.5** $\lim_{x \to 0} \frac{\sqrt{4 + x} - \sqrt{4 - x}}{x} = \lim_{x \to 0} \frac{(4+x) - (4-x)}{x(\sqrt{4 + x} + \sqrt{4 - x})} = \lim_{x \to 0} \frac{2x}{x(\sqrt{4 + x} + \sqrt{4 - x})}$

$= \lim_{x \to 0} \frac{2}{\sqrt{4 + x} + \sqrt{4 - x}} = \frac{2}{4} = \frac{1}{2}$

---

**2.2.6** $\lim_{x \to 0} \frac{x}{\sqrt{x + 1} - 1} = \lim_{x \to 0} \frac{x(\sqrt{x + 1} + 1)}{x} = \lim_{x \to 0} (\sqrt{x + 1} + 1) = 2$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 2.3 (Límites con expresiones complejas)</b></summary>

### Soluciones Ejercicio 2.3

**2.3.1** $\lim_{x \to 1} \frac{\frac{1}{x} - 1}{x - 1} = \lim_{x \to 1} \frac{\frac{1-x}{x}}{x - 1} = \lim_{x \to 1} \frac{1-x}{x(x-1)} = \lim_{x \to 1} \frac{-1}{x} = -1$

---

**2.3.2** $\lim_{x \to 2} \frac{\frac{1}{x} - \frac{1}{2}}{x - 2} = \lim_{x \to 2} \frac{\frac{2-x}{2x}}{x - 2} = \lim_{x \to 2} \frac{2-x}{2x(x-2)} = \lim_{x \to 2} \frac{-1}{2x} = -\frac{1}{4}$

---

**2.3.3** $\lim_{x \to 0} \frac{\frac{1}{x + 3} - \frac{1}{3}}{x} = \lim_{x \to 0} \frac{\frac{3-(x+3)}{3(x+3)}}{x} = \lim_{x \to 0} \frac{-x}{3x(x+3)} = \lim_{x \to 0} \frac{-1}{3(x+3)} = -\frac{1}{9}$

---

**2.3.4** $\lim_{h \to 0} \frac{(x + h)^2 - x^2}{h} = \lim_{h \to 0} \frac{x^2 + 2xh + h^2 - x^2}{h} = \lim_{h \to 0} (2x + h) = 2x$

(Esto es la derivada de $x^2$)

---

**2.3.5** $\lim_{h \to 0} \frac{\sqrt{x + h} - \sqrt{x}}{h} = \lim_{h \to 0} \frac{h}{h(\sqrt{x + h} + \sqrt{x})} = \lim_{h \to 0} \frac{1}{\sqrt{x + h} + \sqrt{x}} = \frac{1}{2\sqrt{x}}$

---

**2.3.6** $\lim_{x \to 0} \frac{(1 + x)^3 - 1}{x} = \lim_{x \to 0} \frac{1 + 3x + 3x^2 + x^3 - 1}{x} = \lim_{x \to 0} (3 + 3x + x^2) = 3$

</details>

---


<details>
<summary><b>Ver soluciones - Sección 3.1 (Límites laterales básicos)</b></summary>

### Soluciones Ejercicio 3.1

**3.1.1** $\lim_{x \to 0^+} \frac{|x|}{x} = \lim_{x \to 0^+} \frac{x}{x} = 1$

$\lim_{x \to 0^-} \frac{|x|}{x} = \lim_{x \to 0^-} \frac{-x}{x} = -1$

---

**3.1.2** $\lim_{x \to 1^-} f(x) = 1 + 2 = 3$

$\lim_{x \to 1^+} f(x) = 3(1) = 3$

Ambos límites son iguales, por lo que $\lim_{x \to 1} f(x) = 3$

---

**3.1.3** Para $x < 2$: $|x - 2| = -(x - 2)$, entonces $\lim_{x \to 2^-} \frac{x - 2}{|x - 2|} = -1$

Para $x > 2$: $|x - 2| = x - 2$, entonces $\lim_{x \to 2^+} \frac{x - 2}{|x - 2|} = 1$

---

**3.1.4** $\lim_{x \to 0^-} g(x) = 0^2 = 0$

$\lim_{x \to 0^+} g(x) = 2(0) = 0$

$\lim_{x \to 0} g(x) = 0$ **existe**

---

**3.1.5** $\lim_{x \to 3^-} \frac{|x - 3|}{x - 3} = -1$

$\lim_{x \to 3^+} \frac{|x - 3|}{x - 3} = 1$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 3.2 (Funciones definidas por partes)</b></summary>

### Soluciones Ejercicio 3.2

**3.2.1** $\lim_{x \to 2^-} f(x) = 2(2) + 1 = 5$

$\lim_{x \to 2^+} f(x) = 2^2 - 1 = 3$

Como $5 \neq 3$, **el límite no existe**.

---

**3.2.2** $\lim_{x \to -2^-} h(x) = (-2)^2 - 4 = 0$

$\lim_{x \to -2^+} h(x) = 4 - (-2)^2 = 0$

$\lim_{x \to -2} h(x) = 0$

---

**3.2.3** $\lim_{x \to 1^-} f(x) = 3(1) + a = 3 + a$

$\lim_{x \to 1^+} f(x) = 2(1)^2 + 1 = 3$

Para que exista el límite: $3 + a = 3 \Rightarrow a = 0$

---

**3.2.4** $\lim_{x \to 3} \frac{x^2 - 9}{x - 3} = \lim_{x \to 3} (x + 3) = 6$

Para continuidad: $k = 6$

---

**3.2.5** $\lim_{x \to 0^-} f(x) = \lim_{x \to 0^-} \frac{\sin x}{x} = 1$

$\lim_{x \to 0^+} f(x) = 1$

$\lim_{x \to 0} f(x) = 1$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 4.1 (Límites infinitos básicos)</b></summary>

### Soluciones Ejercicio 4.1

**4.1.1** $\lim_{x \to 0^+} \frac{1}{x} = +\infty$

$\lim_{x \to 0^-} \frac{1}{x} = -\infty$

---

**4.1.2** $\lim_{x \to 0} \frac{1}{x^2} = +\infty$ (desde ambos lados)

---

**4.1.3** $\lim_{x \to 3^+} \frac{1}{x - 3} = +\infty$

$\lim_{x \to 3^-} \frac{1}{x - 3} = -\infty$

---

**4.1.4** $\lim_{x \to 2} \frac{x + 1}{(x - 2)^2} = +\infty$ (desde ambos lados)

---

**4.1.5** $\lim_{x \to -1^+} \frac{x}{x + 1} = \frac{-1}{0^+} = -\infty$

$\lim_{x \to -1^-} \frac{x}{x + 1} = \frac{-1}{0^-} = +\infty$

---

**4.1.6** $\lim_{x \to 4} \frac{x - 1}{x^2 - 16} = \lim_{x \to 4} \frac{x - 1}{(x-4)(x+4)}$

No existe (depende del lado)

</details>

---

<details>
<summary><b>Ver soluciones - Sección 4.2 (Asíntotas verticales)</b></summary>

### Soluciones Ejercicio 4.2

**4.2.1** $f(x) = \frac{x}{x^2 - 9} = \frac{x}{(x-3)(x+3)}$

**Asíntotas verticales:** $x = 3$ y $x = -3$

---

**4.2.2** $f(x) = \frac{2x}{x^2 - 4}$

**Asíntotas verticales:** $x = 2$ y $x = -2$

---

**4.2.3** $f(x) = \frac{x^2 + 1}{x^2 - 5x + 6} = \frac{x^2 + 1}{(x-2)(x-3)}$

**Asíntotas verticales:** $x = 2$ y $x = 3$

---

**4.2.4** $f(x) = \frac{1}{x^2 + x - 6} = \frac{1}{(x+3)(x-2)}$

**Asíntotas verticales:** $x = -3$ y $x = 2$

---

**4.2.5** $f(x) = \frac{x - 1}{x^3 - x} = \frac{x - 1}{x(x-1)(x+1)}$

Para $x \neq 1$: $f(x) = \frac{1}{x(x+1)}$

**Asíntotas verticales:** $x = 0$ y $x = -1$ (discontinuidad evitable en $x = 1$)

</details>

---

<details>
<summary><b>Ver soluciones - Sección 5.1 (Límites al infinito de funciones racionales)</b></summary>

### Soluciones Ejercicio 5.1

**5.1.1** $\lim_{x \to \infty} \frac{3x + 2}{x - 1} = \lim_{x \to \infty} \frac{3 + \frac{2}{x}}{1 - \frac{1}{x}} = \frac{3}{1} = 3$

---

**5.1.2** $\lim_{x \to \infty} \frac{x^2 - 1}{2x^2 + 3} = \lim_{x \to \infty} \frac{1 - \frac{1}{x^2}}{2 + \frac{3}{x^2}} = \frac{1}{2}$

---

**5.1.3** $\lim_{x \to \infty} \frac{5x^3 + 2x}{x^3 - x + 1} = \lim_{x \to \infty} \frac{5 + \frac{2}{x^2}}{1 - \frac{1}{x^2} + \frac{1}{x^3}} = 5$

---

**5.1.4** $\lim_{x \to \infty} \frac{2x}{x^2 + 1} = \lim_{x \to \infty} \frac{\frac{2}{x}}{1 + \frac{1}{x^2}} = 0$

---

**5.1.5** $\lim_{x \to \infty} \frac{4x^2 - x + 3}{2x - 5} = \infty$ (grado numerador > grado denominador)

---

**5.1.6** $\lim_{x \to -\infty} \frac{x^3 + 2x^2}{x^2 - 1} = \lim_{x \to -\infty} x \cdot \frac{1 + \frac{2}{x}}{1 - \frac{1}{x^2}} = -\infty$

---

**5.1.7** $\lim_{x \to \infty} \frac{\sqrt{x^2 + 1}}{x} = \lim_{x \to \infty} \frac{x\sqrt{1 + \frac{1}{x^2}}}{x} = 1$

---

**5.1.8** $\lim_{x \to \infty} \frac{3x - 1}{7x + 2} = \frac{3}{7}$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 5.2 (Límites con radicales)</b></summary>

### Soluciones Ejercicio 5.2

**5.2.1** $\lim_{x \to \infty} \left(\sqrt{x + 1} - \sqrt{x}\right) = \lim_{x \to \infty} \frac{(\sqrt{x + 1} - \sqrt{x})(\sqrt{x + 1} + \sqrt{x})}{\sqrt{x + 1} + \sqrt{x}}$

$= \lim_{x \to \infty} \frac{1}{\sqrt{x + 1} + \sqrt{x}} = 0$

---

**5.2.2** $\lim_{x \to \infty} \frac{\sqrt{x^2 + x}}{x + 1} = \lim_{x \to \infty} \frac{x\sqrt{1 + \frac{1}{x}}}{x + 1} = \lim_{x \to \infty} \frac{\sqrt{1 + \frac{1}{x}}}{1 + \frac{1}{x}} = 1$

---

**5.2.3** $\lim_{x \to \infty} \left(\sqrt{x^2 + 2x} - x\right) = \lim_{x \to \infty} \frac{2x}{\sqrt{x^2 + 2x} + x} = \lim_{x \to \infty} \frac{2}{\sqrt{1 + \frac{2}{x}} + 1} = 1$

---

**5.2.4** $\lim_{x \to \infty} \frac{x}{\sqrt{4x^2 + 1}} = \lim_{x \to \infty} \frac{x}{2x\sqrt{1 + \frac{1}{4x^2}}} = \frac{1}{2}$

---

**5.2.5** Para $x < 0$: $\sqrt{x^2} = -x$

$\lim_{x \to -\infty} \frac{x}{\sqrt{x^2 + 1}} = \lim_{x \to -\infty} \frac{x}{-x\sqrt{1 + \frac{1}{x^2}}} = -1$

---

**5.2.6** $\lim_{x \to \infty} \sqrt{x}\left(\sqrt{x + 1} - \sqrt{x}\right) = \lim_{x \to \infty} \frac{\sqrt{x}}{\sqrt{x + 1} + \sqrt{x}} = \lim_{x \to \infty} \frac{1}{\sqrt{1 + \frac{1}{x}} + 1} = \frac{1}{2}$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 5.3 (Asíntotas horizontales)</b></summary>

### Soluciones Ejercicio 5.3

**5.3.1** $\lim_{x \to \pm\infty} \frac{2x^2 + 3}{x^2 - 1} = 2$

**Asíntota horizontal:** $y = 2$

---

**5.3.2** $\lim_{x \to \pm\infty} \frac{5x - 3}{x + 2} = 5$

**Asíntota horizontal:** $y = 5$

---

**5.3.3** $\lim_{x \to \pm\infty} \frac{x^3 + 1}{x^2 + 4} = \pm\infty$

**No hay asíntota horizontal**

---

**5.3.4** $\lim_{x \to \infty} \frac{\sqrt{9x^2 + 1}}{3x - 2} = 1$

$\lim_{x \to -\infty} \frac{\sqrt{9x^2 + 1}}{3x - 2} = -1$

**Asíntotas horizontales:** $y = 1$ y $y = -1$

---

**5.3.5** $\lim_{x \to \infty} \frac{e^x}{e^x + 1} = 1$

$\lim_{x \to -\infty} \frac{e^x}{e^x + 1} = 0$

**Asíntotas horizontales:** $y = 1$ (derecha) y $y = 0$ (izquierda)

</details>

---

<details>
<summary><b>Ver soluciones - Sección 6.1 (Indeterminación 0/0)</b></summary>

### Soluciones Ejercicio 6.1

**6.1.1** $\lim_{x \to 1} \frac{x^2 - 1}{x - 1} = \lim_{x \to 1} (x + 1) = 2$

---

**6.1.2** $\lim_{x \to 0} \frac{\sin(3x)}{x} = 3 \lim_{x \to 0} \frac{\sin(3x)}{3x} = 3(1) = 3$

---

**6.1.3** $\lim_{x \to 0} \frac{1 - \cos x}{x^2} = \frac{1}{2}$ (límite fundamental)

---

**6.1.4** $\lim_{x \to 2} \frac{x^3 - 8}{x^2 - 4} = \lim_{x \to 2} \frac{(x-2)(x^2+2x+4)}{(x-2)(x+2)} = \lim_{x \to 2} \frac{x^2+2x+4}{x+2} = \frac{12}{4} = 3$

---

**6.1.5** $\lim_{x \to 0} \frac{\sqrt{1 + x} - 1}{x} = \frac{1}{2}$ (de ejercicio 2.2.3)

</details>

---

<details>
<summary><b>Ver soluciones - Sección 6.2 (Indeterminación ∞/∞)</b></summary>

### Soluciones Ejercicio 6.2

**6.2.1** $\lim_{x \to \infty} \frac{5x^2 + 3x}{2x^2 - x + 1} = \frac{5}{2}$

---

**6.2.2** $\lim_{x \to \infty} \frac{x^3 + 2x^2 - 1}{4x^3 - 5} = \frac{1}{4}$

---

**6.2.3** $\lim_{x \to \infty} \frac{\sqrt{x^2 + x}}{2x + 1} = \lim_{x \to \infty} \frac{x\sqrt{1 + \frac{1}{x}}}{2x + 1} = \frac{1}{2}$

---

**6.2.4** $\lim_{x \to \infty} \frac{e^x}{x^2} = \infty$ (exponencial crece más rápido)

---

**6.2.5** $\lim_{x \to \infty} \frac{\ln x}{x} = 0$ (logaritmo crece más lento)

</details>

---

<details>
<summary><b>Ver soluciones - Sección 6.3 (Indeterminación ∞ - ∞)</b></summary>

### Soluciones Ejercicio 6.3

**6.3.1** $\lim_{x \to \infty} \left(\sqrt{x^2 + x} - x\right) = \lim_{x \to \infty} \frac{x}{\sqrt{x^2 + x} + x} = \frac{1}{2}$

---

**6.3.2** $\lim_{x \to \infty} \left(\sqrt{x^2 + 4x} - \sqrt{x^2 + x}\right) = \lim_{x \to \infty} \frac{3x}{\sqrt{x^2 + 4x} + \sqrt{x^2 + x}} = \frac{3}{2}$

---

**6.3.3** $\lim_{x \to \infty} \left(x - \sqrt{x^2 - 1}\right) = \lim_{x \to \infty} \frac{1}{x + \sqrt{x^2 - 1}} = 0$

---

**6.3.4** $\lim_{x \to \infty} \left(\sqrt{4x^2 + 1} - 2x\right) = \lim_{x \to \infty} \frac{1}{\sqrt{4x^2 + 1} + 2x} = 0$

---

**6.3.5** $\lim_{x \to 0^+} \left(\frac{1}{x} - \frac{1}{\sin x}\right) = \lim_{x \to 0^+} \frac{\sin x - x}{x \sin x} = 0$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 7.1 (Límites trigonométricos básicos)</b></summary>

### Soluciones Ejercicio 7.1

**7.1.1** $\lim_{x \to 0} \frac{\sin(2x)}{x} = 2 \lim_{x \to 0} \frac{\sin(2x)}{2x} = 2$

---

**7.1.2** $\lim_{x \to 0} \frac{\sin(5x)}{\sin(3x)} = \lim_{x \to 0} \frac{\frac{\sin(5x)}{x}}{\frac{\sin(3x)}{x}} = \frac{5}{3}$

---

**7.1.3** $\lim_{x \to 0} \frac{\tan x}{x} = \lim_{x \to 0} \frac{\sin x}{x \cos x} = 1$

---

**7.1.4** $\lim_{x \to 0} \frac{1 - \cos x}{x} = 0$

---

**7.1.5** $\lim_{x \to 0} \frac{\sin^2 x}{x} = \lim_{x \to 0} \sin x \cdot \frac{\sin x}{x} = 0 \cdot 1 = 0$

---

**7.1.6** $\lim_{x \to 0} \frac{x}{\sin(3x)} = \frac{1}{3}$

---

**7.1.7** $\lim_{x \to 0} \frac{\sin x \cos x}{x} = \lim_{x \to 0} \cos x \cdot \frac{\sin x}{x} = 1 \cdot 1 = 1$

---

**7.1.8** $\lim_{x \to 0} \frac{1 - \cos(2x)}{x^2} = \lim_{x \to 0} \frac{1 - \cos(2x)}{(2x)^2} \cdot 4 = \frac{1}{2} \cdot 4 = 2$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 7.2 (Límites trigonométricos complejos)</b></summary>

### Soluciones Ejercicio 7.2

**7.2.1** Usando serie de Taylor: $\sin x \approx x - \frac{x^3}{6}$

$\lim_{x \to 0} \frac{x - \frac{x^3}{6} - x}{x^3} = -\frac{1}{6}$

---

**7.2.2** $\tan x - \sin x = \sin x\left(\frac{1}{\cos x} - 1\right) = \sin x \cdot \frac{1 - \cos x}{\cos x}$

$\lim_{x \to 0} \frac{\sin x \cdot \frac{1 - \cos x}{\cos x}}{x^3} = \frac{1}{2}$

---

**7.2.3** $\lim_{x \to 0} \frac{\sin(ax)}{\sin(bx)} = \frac{a}{b}$

---

**7.2.4** $\lim_{x \to 0} \frac{x - \sin x}{x^3} = \frac{1}{6}$

---

**7.2.5** $\lim_{x \to 0} \frac{\sin x - \tan x}{x^3} = -\frac{1}{2}$

---

**7.2.6** Sea $u = x - \pi$:

$\lim_{x \to \pi} \frac{\sin x}{x - \pi} = \lim_{u \to 0} \frac{\sin(u + \pi)}{u} = \lim_{u \to 0} \frac{-\sin u}{u} = -1$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 8.1 (Verificar continuidad)</b></summary>

### Soluciones Ejercicio 8.1

**8.1.1** $f(2)$ no está definida → **No es continua** en $x = 2$

---

**8.1.2** $\lim_{x \to 1} g(x) = 1$, pero $g(1) = 2$ → **No es continua**

---

**8.1.3** Si definimos $h(0) = 1$, entonces $\lim_{x \to 0} h(x) = 1 = h(0)$ → **Es continua**

---

**8.1.4** $\lim_{x \to 0} |x| = 0 = f(0)$ → **Es continua**

---

**8.1.5** $g(0)$ no está definida → **No es continua**

---

**8.1.6** $\lim_{x \to 0^+} \sqrt{x} = 0 = f(0)$ → **Es continua por la derecha**

</details>

---

<details>
<summary><b>Ver soluciones - Sección 8.2 (Clasificar discontinuidades)</b></summary>

### Soluciones Ejercicio 8.2

**8.2.1** $\lim_{x \to 1} f(x) = 2$ existe pero $f(1)$ no está definida → **Discontinuidad evitable**

---

**8.2.2** Límites laterales diferentes → **Discontinuidad de salto**

---

**8.2.3** $\lim_{x \to 3} f(x) = \pm\infty$ → **Discontinuidad infinita**

---

**8.2.4** Función parte entera tiene saltos en enteros → **Discontinuidad de salto**

---

**8.2.5** $\lim_{x \to 0} \frac{\sin x}{x} = 1$ existe pero $f(0)$ no definida → **Discontinuidad evitable**

---

**8.2.6** $\lim_{x \to 3} f(x) = 6 \neq f(3) = 5$ → **Discontinuidad evitable**

</details>

---

<details>
<summary><b>Ver soluciones - Sección 8.3 (Hacer continua una función)</b></summary>

### Soluciones Ejercicio 8.3

**8.3.1** $\lim_{x \to 2} \frac{x^2 - 4}{x - 2} = 4$

Para continuidad: $k = 4$

---

**8.3.2** $\lim_{x \to 1^-} g(x) = 3 + a$

$\lim_{x \to 1^+} g(x) = 3$

$3 + a = 3 \Rightarrow a = 0$

---

**8.3.3** $\lim_{x \to 0} \frac{\sin(ax)}{x} = a$

Para continuidad: $a = 5$

---

**8.3.4** $\lim_{x \to 2^-} f(x) = 4 - 2b$

$\lim_{x \to 2^+} f(x) = 6 - b$

$4 - 2b = 4 = 6 - b \Rightarrow b = 2$

---

**8.3.5** $\lim_{x \to 1} \frac{\sqrt{x + c} - 2}{x - 1} = \frac{1}{2\sqrt{1 + c}} = \frac{1}{4}$

$\sqrt{1 + c} = 2 \Rightarrow c = 3$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 8.4 (Continuidad en intervalos)</b></summary>

### Soluciones Ejercicio 8.4

**8.4.1** Continua en $\mathbb{R} \setminus \{-2, 2\}$ → $(-\infty, -2) \cup (-2, 2) \cup (2, \infty)$

---

**8.4.2** Dominio: $4 - x^2 \geq 0$ → $[-2, 2]$

Continua en $[-2, 2]$

---

**8.4.3** Dominio: $x - 1 > 0$ → $(1, \infty)$

Continua en $(1, \infty)$

---

**8.4.4** Continua en $\mathbb{R} \setminus \{0\}$ → $(-\infty, 0) \cup (0, \infty)$

---

**8.4.5** Dominio: $x^2 - 1 > 0$ → $(-\infty, -1) \cup (1, \infty)$

---

**8.4.6** Continua en $\mathbb{R} \setminus \{\frac{\pi}{2} + n\pi : n \in \mathbb{Z}\}$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 9.1 (Teorema del Valor Intermedio)</b></summary>

### Soluciones Ejercicio 9.1

**9.1.1** $f(2) = 8 - 4 - 5 = -1 < 0$

$f(3) = 27 - 6 - 5 = 16 > 0$

Por TVI, existe $c \in (2, 3)$ con $f(c) = 0$

---

**9.1.2** $g(0) = 1 > 0$

$g(\frac{\pi}{2}) = 0 - \frac{\pi}{2} < 0$

Por TVI, existe raíz en $(0, \frac{\pi}{2})$

---

**9.1.3** $f(0) = -1 < 0$, $f(1) = 1 > 0$

Existe solución en $[0, 1]$

---

**9.1.4** $h(1) = 1 - 1 = 0$ → Raíz en $x = 1$ ✓

---

**9.1.5** Sea $f(c) = c^3 + c - 1$

$f(0) = -1$, $f(1) = 1$

Existe $c \in (0, 1)$ tal que $f(c) = 0$, es decir, $c^3 + c = 1$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 9.2 (Aplicaciones del TVI)</b></summary>

### Soluciones Ejercicio 9.2

**9.2.1** $h(0) = 100$, $h(5) = -25$

Como $50$ está entre $-25$ y $100$, por TVI existe $t$ tal que $h(t) = 50$

---

**9.2.2** $T(0) = 20$, $T(6) = 30$

$25$ está entre $20$ y $30$, por TVI existe momento con $T = 25°C$

---

**9.2.3** Sea $f(x) = x^3 - 2^x$

$f(1) = -1 < 0$, $f(2) = 4 > 0$

Por TVI, se intersectan en $(1, 2)$

---

**9.2.4** Sea $f(\theta) = \sin\theta - \cos\theta$

$f(0) = -1 < 0$, $f(\frac{\pi}{2}) = 1 > 0$

Existe $\theta$ con $\sin\theta = \cos\theta$ (es $\theta = \frac{\pi}{4}$)

---

**9.2.5** $f(0) = -3$, $f(1) = -3$, $f(2) = 11$

Hay raíz en $(1, 2)$. Para la segunda, $f(-2) = 11 > 0$, hay otra raíz en $(-2, 0)$

</details>

---

<details>
<summary><b>Ver soluciones - Sección 9.3 (Análisis de funciones continuas)</b></summary>

### Soluciones Ejercicio 9.3

**9.3.1** Sea $h(x) = f(x) - g(x)$

$h(a) = f(a) - g(a) < 0$

$h(b) = f(b) - g(b) > 0$

Por TVI, existe $c$ con $h(c) = 0$, es decir, $f(c) = g(c)$

---

**9.3.2** Sea $h(x) = f(x) - f(x + \frac{1}{2})$

$h(0) = f(0) - f(\frac{1}{2})$

$h(\frac{1}{2}) = f(\frac{1}{2}) - f(1) = f(\frac{1}{2}) - f(0)$

$h(0) + h(\frac{1}{2}) = 0$, por lo que al menos uno es cero o tienen signos opuestos → existe $c$

---

**9.3.3** Como los límites al infinito son $0$, para $M$ grande, $|f(x)| < 1$ fuera de $[-M, M]$.

En $[-M, M]$ (compacto), $f$ alcanza su máximo por teorema del valor extremo.

---

**9.3.4** Es consecuencia del **Teorema del Valor Extremo**.

---

**9.3.5** Por el teorema del valor extremo, $f$ alcanza su mínimo $m$ en $[a, b]$.

Como $f(x) > 0$, entonces $m > 0$.

</details>

---

## Notas importantes

1. **Límites:** Describen el comportamiento de una función cerca de un punto, no necesariamente en el punto.

2. **Continuidad:** Requiere que la función esté definida, el límite exista, y ambos coincidan.

3. **Límites laterales:** Cuando son diferentes, el límite no existe.

4. **Indeterminaciones:** Requieren técnicas algebraicas para resolverlas.

5. **Asíntotas:**
   - **Verticales:** Límites infinitos ($x \to a$)
   - **Horizontales:** Límites al infinito ($x \to \pm\infty$)

6. **Límites trigonométricos:** Use los límites fundamentales y propiedades trigonométricas.

7. **TVI:** Herramienta poderosa para demostrar existencia de raíces sin calcularlas explícitamente.

8. **Tipos de discontinuidad:**
   - **Evitable:** Redefiniendo el valor
   - **Salto:** Límites laterales diferentes
   - **Infinita:** Asíntota vertical
   - **Esencial:** Límite no existe de otra forma

9. **Funciones continuas comunes:** Polinomios, funciones trigonométricas, exponenciales, logarítmicas (en su dominio).

10. **Álgebra de límites:** La suma, producto, cociente (si denominador ≠ 0) de límites es el límite de la suma, producto, cociente.

---

**Fecha de entrega:** Por definir  
**Consultas:** Disponibles durante horas de oficina

---

*Desarrollado para el curso de Cálculo 1 - 2026*
