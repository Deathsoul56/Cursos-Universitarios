# Inecuaciones: Fundamentos Algebraicos

## 1. Desigualdades e Inecuaciones: Conceptos Básicos

### 1.1 Desigualdades: Definición y Tipos

A diferencia de las ecuaciones, que establecen una igualdad estricta entre dos cantidades, gran parte de la matemática se basa en comparar tamaños o magnitudes que no son iguales. Piensa en situaciones cotidianas: "la velocidad máxima es 120 km/h", "el presupuesto debe ser menor a 500 dólares". Las desigualdades nos permiten modelar matemáticamente estas restricciones y acotar valores.

**Definición 1.1 (Desigualdad):**
Una desigualdad es una relación matemática de orden que compara dos expresiones usando los símbolos:
- $<$ (menor que)
- $>$ (mayor que)
- $\leq$ (menor o igual que)
- $\geq$ (mayor o igual que)

En su forma más fundamental, las desigualdades se trabajan puramente con **números reales** para establecer una relación de tamaño.

**Ejemplo 1.1 (Desigualdades numéricas):**
Cuando operamos únicamente con números, una desigualdad puede evaluarse directamente como un enunciado verdadero o falso:
- $5 > 3$ (Verdadero: 5 está a la derecha de 3 en la recta numérica).
- $-2 > -9$ (Verdadero: -2 es mayor porque está menos a la izquierda que -9).
- $6 < 2$ (Falso: 6 es estrictamente mayor que 2).
- $4 \leq 4$ (Verdadero: cumple la condición de "igual").

Sin embargo, las desigualdades también se pueden usar con **incógnitas** o variables. Cuando introducimos incógnitas, surgen dos grandes familias de desigualdades:
1. **Desigualdades absolutas:** Son ciertas para cualquier valor numérico real. Por ejemplo, $x^2 \geq 0$ es una verdad absoluta en $\mathbb{R}$.
2. **Desigualdades condicionales (Inecuaciones):** Su veracidad depende del valor que tomen sus variables. Por ejemplo, $x + 2 > 5$ solo es cierto si $x > 3$.

**Proposición 1.1 (Propiedades del orden en $\mathbb{R}$):**

Para cualesquiera $a, b, c \in \mathbb{R}$:
1. **Tricotomía:** Exactamente una de estas se cumple: $a < b$, $a = b$, o $a > b$.
2. **Transitividad:** Si $a < b$ y $b < c$, entonces $a < c$. (Esta propiedad también es válida para $>$, $\leq$ y $\geq$).
3. **Adición:** Si $a < b$, entonces $a + c < b + c$.
4. **Multiplicación por positivo:** Si $a < b$ y $c > 0$, entonces $ac < bc$.
5. **Multiplicación por negativo:** Si $a < b$ y $c < 0$, entonces $ac > bc$.

> **Advertencia:** ¡La última propiedad es la causa número uno de errores en cálculo! Al multiplicar o dividir una desigualdad por un número **negativo**, el símbolo de orden se **invierte**.

### 1.2 Inecuaciones: Estructura y Solución

Ahora nos enfocaremos exclusivamente en las desigualdades condicionales.

**Definición 1.2 (Inecuación):**
Una **inecuación** es una desigualdad algebraica en la que aparecen uno o más valores desconocidos (variables o incógnitas), y resolverla consiste en encontrar todos los valores que hacen que dicha desigualdad sea verdadera.

En su forma más general, cualquier inecuación de una variable puede escribirse matemáticamente llevando todos sus términos a un lado, adoptando alguna de las siguientes formas:
$$f(x) \geq 0, \quad f(x) \leq 0, \quad f(x) > 0, \quad f(x) < 0$$
donde $x \in \text{Dom}(f)$.

Al igual que en las ecuaciones, una inecuación consta de dos **miembros** separados por el signo de desigualdad. Los elementos sumados o restados dentro de cada miembro son los **términos**.

**Ejemplo 1.2 (Variedad de inecuaciones):**
Las inecuaciones pueden involucrar diversos tipos de funciones. A continuación, presentamos algunos ejemplos puramente demostrativos con distintos símbolos de orden:
- **Lineal (menor estricto):** $3x - 5 < 10$
- **Cuadrática (mayor o igual):** $x^2 - 4x + 3 \geq 0$
- **Racional (menor o igual):** $\dfrac{2x + 1}{x - 3} \leq 4$
- **Valor absoluto (mayor estricto):** $|2x - 7| > 5$
- **Logarítmica:** $\ln(x - 2) \leq 1$

**Definición 1.3 (Conjunto Solución):**
El **conjunto solución** de una inecuación es el conjunto de todos los valores reales que satisfacen la desigualdad. Dos inecuaciones se denominan **equivalentes** si tienen exactamente el mismo conjunto solución.

> **Observación importante:** A diferencia de las ecuaciones lineales o cuadráticas, donde la solución suele ser un conjunto discreto de números (uno, dos o tres valores específicos), en las inecuaciones el conjunto solución es casi siempre **infinito**, abarcando todo un continuo en la recta numérica.

**Ejemplo 1.3 (Conjuntos solución simples):**
Para comprender la naturaleza de estos conjuntos, veamos algunas inecuaciones elementales:
- $x > 0 \implies$ El conjunto solución son todos los números reales estrictamente positivos ($\mathbb{R}^+$).
- $x \leq 0 \implies$ El conjunto solución son todos los reales negativos incluyendo al cero ($\mathbb{R}^- \cup \{0\}$).
- $x^2 < 0 \implies$ El conjunto solución es vacío ($\emptyset$), ya que ningún número real al cuadrado arroja un resultado negativo.
- $|x| \geq 0 \implies$ El conjunto solución son todos los números reales ($\mathbb{R}$), pues el valor absoluto de cualquier número siempre es no negativo.

### 1.3 Intervalos como Conjuntos Solución

Para representar estos infinitos valores, empleamos la notación de intervalos. Un intervalo es un subconjunto conexo de la recta real $\mathbb{R}$.

**Definición 1.4 (Intervalos):**
Sean $a, b \in \mathbb{R}$ con $a < b$. Definimos los siguientes tipos de intervalos y sus representaciones:

1. **Intervalo abierto** $(a, b)$: 
   - **Conjunto:** $\{x \in \mathbb{R} : a < x < b\}$
   - **Gráficamente:** Los extremos no están incluidos, se denotan con un círculo vacío ($\circ$).
   > **Nota de notación:** En muchos textos formales, el intervalo abierto también se denota usando corchetes invertidos (apuntando hacia afuera): $]a, b[$. Del mismo modo, un semiabierto puede escribirse como $[a, b[$ o $]a, b]$. Ambas convenciones son válidas y significan exactamente lo mismo.

2. **Intervalo cerrado** $[a, b]$:
   - **Conjunto:** $\{x \in \mathbb{R} : a \leq x \leq b\}$
   - **Gráficamente:** Los extremos están incluidos, se denotan con un círculo relleno ($\bullet$).

3. **Intervalos semiabiertos** $[a, b)$ o $(a, b]$:
   - **Conjunto:** $\{x \in \mathbb{R} : a \leq x < b\}$ o $\{x \in \mathbb{R} : a < x \leq b\}$
   - **Gráficamente:** Un extremo cerrado ($\bullet$) y el otro abierto ($\circ$).

4. **Intervalos infinitos** $(a, \infty)$, $[a, \infty)$, $(-\infty, b)$, $(-\infty, b]$:
   - **Conjunto:** $\{x \in \mathbb{R} : x > a\}$, $\{x \in \mathbb{R} : x \leq b\}$, etc.
   - Representan rayos infinitos en la recta real.

> **Nota:** El símbolo $\infty$ (infinito) no es un número real, sino un concepto que indica un crecimiento sin cota. Por ello, los extremos infinitos **siempre** deben ir con paréntesis abierto, indicando que jamás se alcanzan.

**Ejemplo 1.4:**
Si la solución a una inecuación nos dicta que $x$ debe ser "mayor o igual a -2 y estrictamente menor que 5", se puede representar de tres formas equivalentes y formalmente válidas:
- **Inecuación:** $-2 \leq x < 5$
- **Conjunto:** $\{x \in \mathbb{R} : -2 \leq x < 5\}$
- **Intervalo:** $[-2, 5)$

---

## 2. Tipos de Inecuaciones y Resolución

### 2.1 Inecuaciones lineales

**Ejemplo 2.1:**
$$3x - 5 < 7$$
$$3x < 12$$
$$x < 4$$

**Solución:** $(-\infty, 4)$

**Ejemplo 2.2 (Con inversión):**
$$-2x + 3 \geq 11$$
$$-2x \geq 8$$
$$x \leq -4 \quad \text{(dividimos por -2, invertimos)}$$

**Solución:** $(-\infty, -4]$

### 2.2 Inecuaciones cuadráticas

**Método de resolución:**

1. Llevar todo a un lado: $ax^2 + bx + c \lessgtr 0$
2. Encontrar las raíces (si existen)
3. Analizar el signo de la parábola en cada intervalo
4. Seleccionar los intervalos que satisfacen la desigualdad

**Ejemplo 2.3:**
$$x^2 - 5x + 6 < 0$$

Factorizamos:
$$(x - 2)(x - 3) < 0$$

Raíces: $x = 2$ y $x = 3$

**Tabla de signos:**

| Intervalo       | $(-\infty, 2)$ | $(2, 3)$ | $(3, \infty)$ |
| --------------- | -------------- | -------- | ------------- |
| $(x - 2)$       | $-$            | $+$      | $+$           |
| $(x - 3)$       | $-$            | $-$      | $+$           |
| $(x-2)(x-3)$    | $+$            | $-$      | $+$           |

La desigualdad $(x-2)(x-3) < 0$ se cumple en $(2, 3)$.

**Solución:** $(2, 3)$

**Representación gráfica:**
```text
      +           -           +
  -------○=================○-------
         2                 3
```

### 2.3 Inecuaciones racionales

**Método de resolución:**

1. Llevar todo a un lado: $\frac{P(x)}{Q(x)} \lessgtr 0$
2. Encontrar raíces de $P(x)$ (numerador) y $Q(x)$ (denominador)
3. Construir tabla de signos
4. Seleccionar intervalos según la desigualdad

**¡IMPORTANTE!** Los valores que anulan el denominador **nunca** están en la solución (ni siquiera con $\leq$ o $\geq$).

**Ejemplo 2.4:**
$$\frac{x + 1}{x - 2} \geq 0$$

**Puntos críticos:**
- Raíz del numerador: $x = -1$
- Raíz del denominador: $x = 2$ (excluido siempre)

**Tabla de signos:**

| Intervalo           | $(-\infty, -1)$ | $(-1, 2)$ | $(2, \infty)$ |
| ------------------- | --------------- | --------- | ------------- |
| $(x + 1)$           | $-$             | $+$       | $+$           |
| $(x - 2)$           | $-$             | $-$       | $+$           |
| $\frac{x+1}{x-2}$   | $+$             | $-$       | $+$           |

La desigualdad $\geq 0$ se cumple donde el cociente es positivo o cero:
- En $(-\infty, -1)$: positivo ✓
- En $x = -1$: cero (anula numerador) ✓
- En $(2, \infty)$: positivo ✓

**Solución:** $(-\infty, -1] \cup (2, \infty)$

**Nota:** $x = 2$ no está incluido porque anula el denominador.

### 2.4 Inecuaciones con valor absoluto

Las inecuaciones con valor absoluto se resuelven utilizando las propiedades de la distancia.

**Propiedades fundamentales:**
Para cualquier número real $a > 0$:

1. **Caso menor que:** $|x| < a \iff -a < x < a$
   - Interpretación: La distancia de $x$ al origen es menor que $a$.
   - Solución: Intervalo $(-a, a)$.
   - Análogamente para $\leq$: $|x| \leq a \iff -a \leq x \leq a$.

2. **Caso mayor que:** $|x| > a \iff x > a \lor x < -a$
   - Interpretación: La distancia de $x$ al origen es mayor que $a$.
   - Solución: Unión $(-\infty, -a) \cup (a, \infty)$.
   - Análogamente para $\geq$: $|x| \geq a \iff x \geq a \lor x \leq -a$.

**Ejemplo 2.5 (Caso menor):**
Resolver $|2x - 3| \leq 5$

Aplicamos la propiedad 1:
$$-5 \leq 2x - 3 \leq 5$$
$$-2 \leq 2x \leq 8$$
$$-1 \leq x \leq 4$$

**Solución:** $[-1, 4]$

**Ejemplo 2.6 (Caso mayor):**
Resolver $|3x + 1| > 7$

Aplicamos la propiedad 2:
$$3x + 1 > 7 \quad \lor \quad 3x + 1 < -7$$
$$3x > 6 \quad \lor \quad 3x < -8$$
$$x > 2 \quad \lor \quad x < -8/3$$

**Solución:** $(-\infty, -8/3) \cup (2, \infty)$

---

## 3. Ejercicios propuestos

1. Resuelva: $5x - 7 \leq 3x + 9$
2. Resuelva: $x^2 + x - 6 > 0$
3. Resuelva: $\frac{x - 3}{x + 1} < 2$
4. Resuelva: $|2x - 1| \leq 5$

---

## Referencias y lectura adicional

- **Stewart, J.** *Precálculo: Matemáticas para el Cálculo*, 7ª edición (2017)
- **Larson, R. & Edwards, B.** *Cálculo con Geometría Analítica*, 9ª edición (2010)

---

*Fin de Clase 4 - Inecuaciones*
