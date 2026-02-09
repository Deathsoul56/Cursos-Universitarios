# Lógica Matemática y Proposiciones

## 1. Introducción a la lógica matemática

### 1.1 ¿Qué es la lógica?

**Definición 1.1 (Lógica):**
La **lógica** es la ciencia que estudia los principios del razonamiento válido y la inferencia correcta. En matemáticas, la lógica proporciona el fundamento para construir argumentos rigurosos y demostraciones.

**Objetivo de la lógica matemática:**
- Formalizar el razonamiento matemático
- Distinguir argumentos válidos de inválidos
- Establecer métodos sistemáticos para demostrar teoremas
- Crear un lenguaje preciso y sin ambigüedades

**Áreas de aplicación:**
- Fundamentos de las matemáticas
- Ciencias de la computación (algoritmos, programación)
- Inteligencia artificial
- Diseño de circuitos digitales
- Bases de datos

### 1.2 Breve historia del álgebra booleana

**Álgebra booleana** (o álgebra de Boole) es el sistema algebraico que formaliza las operaciones lógicas.

**Cronología histórica:**

**Aristóteles (384-322 a.C.):**
- Estableció los fundamentos de la lógica formal
- Desarrolló el sistema de silogismos
- Formuló el principio de no contradicción

**Gottfried Leibniz (1646-1716):**
- Propuso la idea de un "cálculo lógico"
- Visionó un lenguaje universal para el razonamiento

**George Boole (1815-1864):**
- **1854:** Publicó "An Investigation of the Laws of Thought"
- Creó el **álgebra booleana**, un sistema algebraico para la lógica
- Representó operaciones lógicas mediante ecuaciones algebraicas
- Usó los valores 0 (falso) y 1 (verdadero)

**Augustus De Morgan (1806-1871):**
- Formuló las **Leyes de De Morgan** (1847)
- Estableció relaciones entre conjunción, disyunción y negación

**Gottlob Frege (1848-1925):**
- Desarrolló la lógica de predicados
- Introdujo cuantificadores universales y existenciales

**Bertrand Russell y Alfred Whitehead (1910-1913):**
- *Principia Mathematica*: intento de fundamentar toda la matemática en la lógica

**Claude Shannon (1916-2001):**
- **1937:** Tesis de maestría revolucionaria
- Aplicó el álgebra booleana al diseño de **circuitos eléctricos**
- Fundó la teoría de la información
- Sus ideas son la base de todos los circuitos digitales modernos

**Impacto moderno:**
El álgebra booleana es fundamental para:
- Procesadores y computadoras
- Lenguajes de programación
- Sistemas digitales
- Búsqueda en bases de datos (operadores AND, OR, NOT)

---
## 2. Preposiciones

### 2.1 Definición de preposición

**Definición 2.1 (Preposición):**
Una **preposición** (o enunciado) es una oración declarativa que puede ser **verdadera** o **falsa**, pero no ambas simultáneamente.

**Características de una proposición:**
1. Es una afirmación declarativa (no pregunta, orden o exclamación)
2. Tiene un valor de verdad definido: **verdadero (V)** o **falso (F)**
3. No puede ser verdadera y falsa al mismo tiempo (principio de no contradicción)
4. Debe ser verdadera o falsa (principio del tercero excluido)

**Ejemplo 2.1 (Proposiciones válidas):**

a) "$2 + 2 = 4$" → **Proposición verdadera**

b) "$\pi > 3$" → **Proposición verdadera**

c) "Lima es la capital de Chile" → **Proposición falsa**

d) "$5$ es un número par" → **Proposición falsa**

e) "Para todo $x \in \mathbb{R}$, $x^2 \geq 0$" → **Proposición verdadera**

**Ejemplo 2.2 (NO son proposiciones):**

a) "¿Qué hora es?" → **Pregunta** (no tiene valor de verdad)

b) "¡Estudia más!" → **Orden/Imperativo** (no tiene valor de verdad)

c) "Este enunciado es falso" → **Paradoja** (autorreferencial contradictorio)

d) "$x + 5 = 10$" → **Ecuación abierta** (depende del valor de $x$)

e) "Ella es alta" → **Subjetivo/Ambiguo** (no hay criterio claro de verdad)

**Observación:** Las proposiciones matemáticas son especialmente importantes porque tienen valores de verdad objetivos y universales.

### 2.2 Notación y valores de verdad

**Notación:**
- Las proposiciones se denotan con letras minúsculas: $p$, $q$, $r$, $s$, etc.
- Los valores de verdad se representan:
  - **V** (verdadero) o **T** (true) o **1**
  - **F** (falso) o **⊥** (bottom) o **0**

**Ejemplo 2.3:**
- $p$: "El agua hierve a 100°C al nivel del mar" → $p$ es **V**
- $q$: "$3 + 5 = 7$" → $q$ es **F**
- $r$: "Los ángulos de un triángulo suman 180°" → $r$ es **V**

### 2.3 Preposiciones simples y compuestas

**Definición 2.2 (Proposición simple):**
Una **proposición simple** (o atómica) es aquella que no puede descomponerse en proposiciones más simples.

**Definición 2.3 (Proposición compuesta):**
Una **proposición compuesta** (o molecular) es aquella formada por dos o más proposiciones simples conectadas mediante **conectivos lógicos**.

**Ejemplo 2.4:**

**Proposiciones simples:**
- $p$: "Llueve"
- $q$: "Hace frío"

**Proposiciones compuestas:**
- "Llueve **y** hace frío" → $p \land q$
- "Llueve **o** hace frío" → $p \lor q$
- "**No** llueve" → $\neg p$
- "**Si** llueve, **entonces** hace frío" → $p \to q$

---
## 3. Conectivos lógicos fundamentales

### 3.1 Negación

**Definición 3.1 (Negación):**
La **negación** de una proposición $p$, denotada $\neg p$ (o $\sim p$), es la proposición que es **verdadera cuando $p$ es falsa** y **falsa cuando $p$ es verdadera**.

**Símbolos:** $\neg p$, $\sim p$, $\bar{p}$, NOT $p$

**Tabla de verdad:**

| $p$ | $\neg p$ |
| :-: | :------: |
|  V  |    F     |
|  F  |    V     |

**Ejemplo 3.1:**
- $p$: "5 es primo" (V)
- $\neg p$: "5 **no** es primo" (F)

**Ejemplo 3.2:**
- $q$: "$2 + 2 = 5$" (F)
- $\neg q$: "$2 + 2 \neq 5$" o "**No** es cierto que $2 + 2 = 5$" (V)

**Propiedad fundamental:**
$$\neg(\neg p) = p \quad \text{(Doble negación)}$$

### 3.2 Conjunción

**Definición 3.2 (Conjunción):**
La **conjunción** de dos proposiciones $p$ y $q$, denotada $p \land q$ (se lee "$p$ **y** $q$"), es la proposición que es **verdadera solo cuando ambas $p$ y $q$ son verdaderas**.

**Símbolos:** $p \land q$, $p \wedge q$, $p \cdot q$, $p$ AND $q$

**Tabla de verdad:**

| $p$ | $q$ | $p \land q$ |
| :-: | :-: | :---------: |
|  V  |  V  |      V      |
|  V  |  F  |      F      |
|  F  |  V  |      F      |
|  F  |  F  |      F      |

**Regla mnemotécnica:** La conjunción es verdadera **solo en la primera fila** (cuando todo es verdadero).

**Ejemplo 3.3:**
- $p$: "10 es par" (V)
- $q$: "10 es divisible por 5" (V)
- $p \land q$: "10 es par **y** divisible por 5" (V)

**Ejemplo 3.4:**
- $p$: "París está en Francia" (V)
- $q$: "2 + 2 = 5" (F)
- $p \land q$: "París está en Francia **y** $2 + 2 = 5$" (F)

### 3.3 Disyunción (inclusiva)

**Definición 3.3 (Disyunción):**
La **disyunción** de dos proposiciones $p$ y $q$, denotada $p \lor q$ (se lee "$p$ **o** $q$"), es la proposición que es **falsa solo cuando ambas $p$ y $q$ son falsas**.

**Símbolos:** $p \lor q$, $p \vee q$, $p + q$, $p$ OR $q$

**Tabla de verdad:**

| $p$ | $q$ | $p \lor q$ |
| :-: | :-: | :--------: |
|  V  |  V  |     V      |
|  V  |  F  |     V      |
|  F  |  V  |     V      |
|  F  |  F  |     F      |

**Regla mnemotécnica:** La disyunción es falsa **solo en la última fila** (cuando todo es falso).

**Observación:** En lógica matemática, el "o" es **inclusivo**: "$p$ o $q$" significa "al menos uno de los dos" (pueden ser ambos).

**Ejemplo 3.5:**
- $p$: "Estudio matemáticas" (V)
- $q$: "Estudio física" (V)
- $p \lor q$: "Estudio matemáticas **o** física" (V) → Estudio ambas

**Ejemplo 3.6:**
- $p$: "$7 < 5$" (F)
- $q$: "$7 = 5$" (F)
- $p \lor q$: "$7 < 5$ **o** $7 = 5$" (F)

### 3.4 Disyunción exclusiva (XOR)

**Definición 3.4 (Disyunción exclusiva):**
La **disyunción exclusiva** de $p$ y $q$, denotada $p \oplus q$, es verdadera cuando **exactamente una** de las proposiciones es verdadera.

**Símbolos:** $p \oplus q$, $p$ XOR $q$

**Tabla de verdad:**

| $p$ | $q$ | $p \oplus q$ |
| :-: | :-: | :----------: |
|  V  |  V  |      F       |
|  V  |  F  |      V       |
|  F  |  V  |      V       |
|  F  |  F  |      F       |

**Ejemplo 3.7:**
- $p$: "Nací en enero"
- $q$: "Nací en febrero"
- $p \oplus q$: "Nací en enero **o** en febrero" (solo uno es posible)

**Relación con otros conectivos:**
$$p \oplus q \equiv (p \lor q) \land \neg(p \land q)$$
$$p \oplus q \equiv (p \land \neg q) \lor (\neg p \land q)$$

---

## 4. Tablas de verdad

### 4.1 Construcción de tablas de verdad

**Definición 4.1 (Tabla de verdad):**
Una **tabla de verdad** es una herramienta que muestra todas las posibles combinaciones de valores de verdad de las proposiciones simples y el valor resultante de una proposición compuesta.

**Procedimiento:**
1. Identificar las proposiciones simples ($p$, $q$, $r$, etc.)
2. Determinar el número de filas: $2^n$ donde $n$ es el número de proposiciones
3. Listar todas las combinaciones posibles de valores de verdad
4. Evaluar la proposición compuesta para cada combinación

**Ejemplo 4.1:**
Construya la tabla de verdad para $\neg p \land q$:

| $p$ | $q$ | $\neg p$ | $\neg p \land q$ |
| :-: | :-: | :------: | :--------------: |
|  V  |  V  |    F     |        F         |
|  V  |  F  |    F     |        F         |
|  F  |  V  |    V     |        V         |
|  F  |  F  |    V     |        F         |

**Ejemplo 4.2:**
Tabla de verdad para $(p \lor q) \land \neg q$:

| $p$ | $q$ | $p \lor q$ | $\neg q$ | $(p \lor q) \land \neg q$ |
| :-: | :-: | :--------: | :------: | :-----------------------: |
|  V  |  V  |     V      |    F     |             F             |
|  V  |  F  |     V      |    V     |             V             |
|  F  |  V  |     V      |    F     |             F             |
|  F  |  F  |     F      |    V     |             F             |

### 4.2 Tablas con tres proposiciones

**Ejemplo 4.3:**
Tabla de verdad para $p \land (q \lor r)$:

| $p$ | $q$ | $r$ | $q \lor r$ | $p \land (q \lor r)$ |
| :-: | :-: | :-: | :--------: | :------------------: |
|  V  |  V  |  V  |     V      |          V           |
|  V  |  V  |  F  |     V      |          V           |
|  V  |  F  |  V  |     V      |          V           |
|  V  |  F  |  F  |     F      |          F           |
|  F  |  V  |  V  |     V      |          F           |
|  F  |  V  |  F  |     V      |          F           |
|  F  |  F  |  V  |     V      |          F           |
|  F  |  F  |  F  |     F      |          F           |

**Observación:** Con 3 proposiciones hay $2^3 = 8$ filas.

---

## 5. Leyes de De Morgan

### 5.1 Enunciado de las leyes

**Teorema 5.1 (Leyes de De Morgan):**
Para cualesquiera proposiciones $p$ y $q$:

**Primera Ley:**
$$\neg(p \land q) \equiv \neg p \lor \neg q$$

"La negación de una conjunción es la disyunción de las negaciones"

**Segunda Ley:**
$$\neg(p \lor q) \equiv \neg p \land \neg q$$

"La negación de una disyunción es la conjunción de las negaciones"

### 5.2 Demostración mediante tablas de verdad

**Demostración de la Primera Ley:**

| $p$ | $q$ | $p \land q$ | $\neg(p \land q)$ | $\neg p$ | $\neg q$ | $\neg p \lor \neg q$ |
| :-: | :-: | :---------: | :---------------: | :------: | :------: | :------------------: |
|  V  |  V  |      V      |         F         |    F     |    F     |          F           |
|  V  |  F  |      F      |         V         |    F     |    V     |          V           |
|  F  |  V  |      F      |         V         |    V     |    F     |          V           |
|  F  |  F  |      F      |         V         |    V     |    V     |          V           |

Las columnas $\neg(p \land q)$ y $\neg p \lor \neg q$ son idénticas. ✓

**Demostración de la Segunda Ley:**

| $p$ | $q$ | $p \lor q$ | $\neg(p \lor q)$ | $\neg p$ | $\neg q$ | $\neg p \land \neg q$ |
| :-: | :-: | :--------: | :--------------: | :------: | :------: | :-------------------: |
|  V  |  V  |     V      |        F         |    F     |    F     |           F           |
|  V  |  F  |     V      |        F         |    F     |    V     |           F           |
|  F  |  V  |     V      |        F         |    V     |    F     |           F           |
|  F  |  F  |     F      |        V         |    V     |    V     |           V           |

Las columnas $\neg(p \lor q)$ y $\neg p \land \neg q$ son idénticas. ✓

### 5.3 Interpretación y ejemplos

**Ejemplo 5.1:**
Niegue: "Llueve y hace frío"

**Solución:**
- $p$: "Llueve"
- $q$: "Hace frío"
- Original: $p \land q$

Aplicando De Morgan:
$$\neg(p \land q) \equiv \neg p \lor \neg q$$

**Negación:** "**No** llueve **o no** hace frío"

**Ejemplo 5.2:**
Niegue: "Estudio matemáticas o física"

**Solución:**
- $p$: "Estudio matemáticas"
- $q$: "Estudio física"
- Original: $p \lor q$

Aplicando De Morgan:
$$\neg(p \lor q) \equiv \neg p \land \neg q$$

**Negación:** "**No** estudio matemáticas **y no** estudio física"

### 5.4 Generalización

**Teorema 5.2 (Leyes de De Morgan generalizadas):**
Para $n$ proposiciones:

$$\neg(p_1 \land p_2 \land \cdots \land p_n) \equiv \neg p_1 \lor \neg p_2 \lor \cdots \lor \neg p_n$$

$$\neg(p_1 \lor p_2 \lor \cdots \lor p_n) \equiv \neg p_1 \land \neg p_2 \land \cdots \land \neg p_n$$

**Ejemplo 5.3:**
Niegue: "$x > 0$ y $x < 10$ y $x$ es par"

Aplicando De Morgan:
"$x \leq 0$ **o** $x \geq 10$ **o** $x$ es impar"

---

## 6. Propiedades de los conectivos lógicos

### 6.1 Propiedades algebraicas

**Teorema 6.1 (Propiedades de la conjunción y disyunción):**

**1. Conmutatividad:**
$$p \land q \equiv q \land p$$
$$p \lor q \equiv q \lor p$$

**2. Asociatividad:**
$$(p \land q) \land r \equiv p \land (q \land r)$$
$$(p \lor q) \lor r \equiv p \lor (q \lor r)$$

**3. Distributividad:**
$$p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$$
$$p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)$$

**4. Identidad:**
$$p \land V \equiv p \quad \text{(V es el elemento neutro de } \land \text{)}$$
$$p \lor F \equiv p \quad \text{(F es el elemento neutro de } \lor \text{)}$$

**5. Dominación:**
$$p \land F \equiv F$$
$$p \lor V \equiv V$$

**6. Idempotencia:**
$$p \land p \equiv p$$
$$p \lor p \equiv p$$

**7. Absorción:**
$$p \land (p \lor q) \equiv p$$
$$p \lor (p \land q) \equiv p$$

**8. Leyes de De Morgan:**
$$\neg(p \land q) \equiv \neg p \lor \neg q$$
$$\neg(p \lor q) \equiv \neg p \land \neg q$$

**9. Doble negación:**
$$\neg(\neg p) \equiv p$$

**10. Complemento:**
$$p \land \neg p \equiv F \quad \text{(Contradicción)}$$
$$p \lor \neg p \equiv V \quad \text{(Tercero excluido)}$$

### 6.2 Demostración de propiedades

**Ejemplo 6.1:** Demuestre la propiedad distributiva $p \land (q \lor r) \equiv (p \land q) \lor (p \land r)$

| $p$ | $q$ | $r$ | $q \lor r$ | $p \land (q \lor r)$ | $p \land q$ | $p \land r$ | $(p \land q) \lor (p \land r)$ |
| :-: | :-: | :-: | :--------: | :------------------: | :---------: | :---------: | :----------------------------: |
|  V  |  V  |  V  |     V      |          V           |      V      |      V      |               V                |
|  V  |  V  |  F  |     V      |          V           |      V      |      F      |               V                |
|  V  |  F  |  V  |     V      |          V           |      F      |      V      |               V                |
|  V  |  F  |  F  |     F      |          F           |      F      |      F      |               F                |
|  F  |  V  |  V  |     V      |          F           |      F      |      F      |               F                |
|  F  |  V  |  F  |     V      |          F           |      F      |      F      |               F                |
|  F  |  F  |  V  |     V      |          F           |      F      |      F      |               F                |
|  F  |  F  |  F  |     F      |          F           |      F      |      F      |               F                |

Las columnas son idénticas. ✓

### 6.3 Simplificación de expresiones

**Ejemplo 6.2:**
Simplifique: $(p \land q) \lor (p \land \neg q)$

**Solución:**
$$\begin{align}
(p \land q) \lor (p \land \neg q) &\equiv p \land (q \lor \neg q) \quad \text{(Distributividad)} \\
&\equiv p \land V \quad \text{(Complemento)} \\
&\equiv p \quad \text{(Identidad)}
\end{align}$$

**Ejemplo 6.3:**
Simplifique: $\neg(p \lor \neg q) \lor (\neg p \land \neg q)$

**Solución:**
$$\begin{align}
\neg(p \lor \neg q) \lor (\neg p \land \neg q) &\equiv (\neg p \land \neg(\neg q)) \lor (\neg p \land \neg q) \quad \text{(De Morgan)} \\
&\equiv (\neg p \land q) \lor (\neg p \land \neg q) \\
&\equiv \neg p \land (q \lor \neg q) \quad \text{(Distributividad)} \\
&\equiv \neg p \land V \\
&\equiv \neg p
\end{align}$$

---

## 7. Tautologías y contradicciones

### 7.1 Tautologías

**Definición 7.1 (Tautología):**
Una **tautología** es una proposición compuesta que es **siempre verdadera**, independientemente de los valores de verdad de sus proposiciones componentes.

**Símbolo:** Se denota con $\top$ o simplemente $V$.

**Ejemplo 7.1 (Tautologías básicas):**

a) $p \lor \neg p$ (Ley del tercero excluido)

| $p$ | $\neg p$ | $p \lor \neg p$ |
| :-: | :------: | :-------------: |
|  V  |    F     |        V        |
|  F  |    V     |        V        |

**Siempre verdadera** ✓

b) $\neg(p \land \neg p)$ (Ley de no contradicción)

| $p$ | $\neg p$ | $p \land \neg p$ | $\neg(p \land \neg p)$ |
| :-: | :------: | :--------------: | :--------------------: |
|  V  |    F     |        F         |           V            |
|  F  |    V     |        F         |           V            |

**Siempre verdadera** ✓

**Ejemplo 7.2:**
Verifique que $(p \to q) \equiv (\neg p \lor q)$ es una tautología (equivalencia lógica).

Demostración: Más adelante con implicación.

**Ejemplo 7.3 (Tautologías importantes):**

- $(p \land q) \to p$ (Simplificación)
- $p \to (p \lor q)$ (Adición)
- $[(p \to q) \land p] \to q$ (Modus ponens)
- $[(p \to q) \land \neg q] \to \neg p$ (Modus tollens)

### 7.2 Contradicciones (Absurdos)

**Definición 7.2 (Contradicción):**
Una **contradicción** (o **absurdo**) es una proposición compuesta que es **siempre falsa**, independientemente de los valores de verdad de sus proposiciones componentes.

**Símbolo:** Se denota con $\bot$ o $F$.

**Ejemplo 7.4 (Contradicciones básicas):**

a) $p \land \neg p$

| $p$ | $\neg p$ | $p \land \neg p$ |
| :-: | :------: | :--------------: |
|  V  |    F     |        F         |
|  F  |    V     |        F         |

**Siempre falsa** ✓

b) $(p \lor q) \land \neg p \land \neg q$

| $p$ | $q$ | $p \lor q$ | $\neg p$ | $\neg q$ | $(p \lor q) \land \neg p \land \neg q$ |
| :-: | :-: | :--------: | :------: | :------: | :------------------------------------: |
|  V  |  V  |     V      |    F     |    F     |                   F                    |
|  V  |  F  |     V      |    F     |    V     |                   F                    |
|  F  |  V  |     V      |    V     |    F     |                   F                    |
|  F  |  F  |     F      |    V     |    V     |                   F                    |

**Siempre falsa** ✓

### 7.3 Contingencias

**Definición 7.3 (Contingencia):**
Una **contingencia** es una proposición que no es ni tautología ni contradicción. Es decir, puede ser verdadera o falsa dependiendo de los valores de sus componentes.

**Ejemplo 7.5:**
- $p \land q$ es una contingencia
- $p \to q$ es una contingencia (según valores de $p$ y $q$)
- $p \oplus q$ es una contingencia

---

## 8. Implicación (Condicional)

### 8.1 Definición de implicación

**Definición 8.1 (Implicación o Condicional):**
La **implicación** $p \to q$ (se lee "**si** $p$ **entonces** $q$" o "$p$ **implica** $q$") es la proposición que es **falsa solo cuando $p$ es verdadera y $q$ es falsa**.

**Símbolos:** $p \to q$, $p \Rightarrow q$, $p \supset q$

**Componentes:**
- $p$: **hipótesis**, **antecedente** o **premisa**
- $q$: **conclusión**, **consecuente** o **tesis**

**Tabla de verdad:**

| $p$ | $q$ | $p \to q$ |
| :-: | :-: | :-------: |
|  V  |  V  |     V     |
|  V  |  F  |     F     |
|  F  |  V  |     V     |
|  F  |  F  |     V     |

**Regla mnemotécnica:** La implicación es falsa **solo en la segunda fila** (hipótesis verdadera, conclusión falsa).

**Observación importante:** 
- Cuando la hipótesis es **falsa**, la implicación es **vacuamente verdadera** (verdadera "por vacuidad")
- "$p \to q$" no afirma que $p$ causa $q$, solo que no se da el caso "$p$ verdadero y $q$ falso"

**Ejemplo 8.1:**
- $p$: "$x = 2$"
- $q$: "$x^2 = 4$"
- $p \to q$: "Si $x = 2$, entonces $x^2 = 4$" (V)

**Ejemplo 8.2:**
- $p$: "$n$ es divisible por 4"
- $q$: "$n$ es par"
- $p \to q$: "Si $n$ es divisible por 4, entonces $n$ es par" (V, siempre)

**Ejemplo 8.3 (Implicación vacua):**
- $p$: "$2 + 2 = 5$" (F)
- $q$: "La luna está hecha de queso" (F)
- $p \to q$: "Si $2 + 2 = 5$, entonces la luna está hecha de queso" (V)

Como la hipótesis es falsa, la implicación es verdadera independientemente de $q$.

### 8.2 Equivalencia con disyunción

**Teorema 8.1:**
$$p \to q \equiv \neg p \lor q$$

**Demostración:**

| $p$ | $q$ | $p \to q$ | $\neg p$ | $\neg p \lor q$ |
| :-: | :-: | :-------: | :------: | :-------------: |
|  V  |  V  |     V     |    F     |        V        |
|  V  |  F  |     F     |    F     |        F        |
|  F  |  V  |     V     |    V     |        V        |
|  F  |  F  |     V     |    V     |        V        |

Las columnas son idénticas. ✓

**Uso:** Esta equivalencia permite expresar implicaciones usando solo negación y disyunción.

### 8.3 Formas relacionadas

**Definición 8.2 (Formas de una implicación):**

Dada la implicación $p \to q$:

1. **Recíproca:** $q \to p$
2. **Inversa:** $\neg p \to \neg q$
3. **Contrapositiva:** $\neg q \to \neg p$

**Teorema 8.2:**
Una implicación y su contrapositiva son **lógicamente equivalentes**:
$$p \to q \equiv \neg q \to \neg p$$

**Demostración:**

| $p$ | $q$ | $p \to q$ | $\neg q$ | $\neg p$ | $\neg q \to \neg p$ |
| :-: | :-: | :-------: | :------: | :------: | :-----------------: |
|  V  |  V  |     V     |    F     |    F     |          V          |
|  V  |  F  |     F     |    V     |    F     |          F          |
|  F  |  V  |     V     |    F     |    V     |          V          |
|  F  |  F  |     V     |    V     |    V     |          V          |

Las columnas son idénticas. ✓

**Observación:** La **recíproca** y la **inversa** NO son equivalentes a la implicación original.

**Ejemplo 8.4:**
- **Original:** "Si llueve, entonces la calle está mojada" ($p \to q$)
- **Recíproca:** "Si la calle está mojada, entonces llueve" ($q \to p$) → No necesariamente verdadera
- **Inversa:** "Si no llueve, entonces la calle no está mojada" ($\neg p \to \neg q$) → No necesariamente verdadera
- **Contrapositiva:** "Si la calle no está mojada, entonces no llueve" ($\neg q \to \neg p$) → Equivalente a la original

### 8.4 Propiedades de la implicación

**Proposición 8.1 (Propiedades):**

1. **No conmutativa:** $p \to q \not\equiv q \to p$ (en general)

2. **Transitividad:**
   $$[(p \to q) \land (q \to r)] \to (p \to r)$$

3. **Modus ponens:**
   $$[(p \to q) \land p] \to q \quad \text{(Tautología)}$$

4. **Modus tollens:**
   $$[(p \to q) \land \neg q] \to \neg p \quad \text{(Tautología)}$$

5. **Silogismo hipotético:**
   $$[(p \to q) \land (q \to r)] \to (p \to r)$$

**Ejemplo 8.5 (Modus ponens):**
- Premisa 1: "Si estudio, entonces aprobaré" ($p \to q$)
- Premisa 2: "Estudio" ($p$)
- Conclusión: "Aprobaré" ($q$)

**Ejemplo 8.6 (Modus tollens):**
- Premisa 1: "Si es un mamífero, entonces respira aire" ($p \to q$)
- Premisa 2: "No respira aire" ($\neg q$)
- Conclusión: "No es un mamífero" ($\neg p$)

---

## 9. Bicondicional (Si y solo si)

### 9.1 Definición de bicondicional

**Definición 9.1 (Bicondicional):**
El **bicondicional** $p \leftrightarrow q$ (se lee "$p$ **si y solo si** $q$") es la proposición que es **verdadera cuando $p$ y $q$ tienen el mismo valor de verdad**.

**Símbolos:** $p \leftrightarrow q$, $p \Leftrightarrow q$, $p \equiv q$, $p$ IFF $q$

**Tabla de verdad:**

| $p$ | $q$ | $p \leftrightarrow q$ |
| :-: | :-: | :-------------------: |
|  V  |  V  |           V           |
|  V  |  F  |           F           |
|  F  |  V  |           F           |
|  F  |  F  |           V           |

**Regla mnemotécnica:** El bicondicional es verdadero en las **filas 1 y 4** (cuando ambos tienen el mismo valor).

**Interpretación:** "$p$ si y solo si $q$" significa:
- **Si $p$ entonces $q$** ($p \to q$), **Y**
- **Si $q$ entonces $p$** ($q \to p$)

### 9.2 Equivalencias del bicondicional

**Teorema 9.1:**
$$p \leftrightarrow q \equiv (p \to q) \land (q \to p)$$

**Demostración:**

| $p$ | $q$ | $p \to q$ | $q \to p$ | $(p \to q) \land (q \to p)$ | $p \leftrightarrow q$ |
|-----|-----|-----------|-----------|-----------------------------|-----------------------|
| V   | V   | V         | V         | V                           | V                     |
| V   | F   | F         | V         | F                           | F                     |
| F   | V   | V         | F         | F                           | F                     |
| F   | F   | V         | V         | V                           | V                     |

Las columnas son idénticas. ✓

**Teorema 9.2 (Otras equivalencias):**
$$p \leftrightarrow q \equiv (p \land q) \lor (\neg p \land \neg q)$$
$$p \leftrightarrow q \equiv \neg(p \oplus q)$$

**Ejemplo 9.1:**
- $p$: "$n$ es par"
- $q$: "$n$ es divisible por 2"
- $p \leftrightarrow q$: "$n$ es par **si y solo si** $n$ es divisible por 2" (V, definición)

**Ejemplo 9.2:**
En matemáticas:
- "Un triángulo es equilátero **si y solo si** sus tres lados son iguales"
- "$x^2 = 4$ **si y solo si** $x = 2$ o $x = -2$"

### 9.3 Propiedades del bicondicional

**Proposición 9.1 (Propiedades):**

1. **Conmutatividad:**
   $$p \leftrightarrow q \equiv q \leftrightarrow p$$

2. **Asociatividad:**
   $$(p \leftrightarrow q) \leftrightarrow r \equiv p \leftrightarrow (q \leftrightarrow r)$$

3. **Transitividad:**
   $$[(p \leftrightarrow q) \land (q \leftrightarrow r)] \to (p \leftrightarrow r)$$

4. **Reflexividad:**
   $$p \leftrightarrow p \quad \text{(Tautología)}$$

**Observación:** El bicondicional establece una **equivalencia lógica** entre proposiciones.

---

## 10. Jerarquía de conectivos y paréntesis

### 10.1 Orden de precedencia

**Orden de evaluación (de mayor a menor prioridad):**

1. $\neg$ (Negación)
2. $\land$ (Conjunción)
3. $\lor$ (Disyunción)
4. $\to$ (Implicación)
5. $\leftrightarrow$ (Bicondicional)

**Ejemplo 10.1:**
La expresión $\neg p \land q \to r$ se interpreta como:
$$[(\neg p) \land q] \to r$$

**Ejemplo 10.2:**
La expresión $p \lor q \land r$ se interpreta como:
$$p \lor (q \land r)$$

**Recomendación:** Usar paréntesis para mayor claridad, especialmente en expresiones complejas.

---

## 11. Argumentos y razonamiento lógico

### 11.1 Argumentos válidos

**Definición 11.1 (Argumento):**
Un **argumento** es una secuencia de proposiciones donde:
- Las proposiciones iniciales se llaman **premisas**
- La proposición final se llama **conclusión**

**Definición 11.2 (Argumento válido):**
Un argumento es **válido** si: siempre que todas las premisas sean verdaderas, la conclusión también es verdadera.

**Notación:**
$$\frac{p_1, p_2, \ldots, p_n}{\therefore q}$$

Significa: "De las premisas $p_1, p_2, \ldots, p_n$ se concluye $q$"

**Observación:** Un argumento válido tiene la forma de una tautología:
$$(p_1 \land p_2 \land \cdots \land p_n) \to q$$

### 11.2 Reglas de inferencia básicas

**1. Modus ponens:**
$$\frac{p \to q, \quad p}{\therefore q}$$

**2. Modus tollens:**
$$\frac{p \to q, \quad \neg q}{\therefore \neg p}$$

**3. Silogismo hipotético:**
$$\frac{p \to q, \quad q \to r}{\therefore p \to r}$$

**4. Silogismo disyuntivo:**
$$\frac{p \lor q, \quad \neg p}{\therefore q}$$

**5. Adición:**
$$\frac{p}{\therefore p \lor q}$$

**6. Simplificación:**
$$\frac{p \land q}{\therefore p}$$

**7. Conjunción:**
$$\frac{p, \quad q}{\therefore p \land q}$$

**Ejemplo 11.1:**
Verifique el argumento:
- Premisa 1: "Si llueve, entonces la calle está mojada"
- Premisa 2: "Llueve"
- Conclusión: "La calle está mojada"

**Solución:** Aplicando **modus ponens**, el argumento es válido.

**Ejemplo 11.2:**
- Premisa 1: "Si estudio, aprobaré" ($p \to q$)
- Premisa 2: "No aprobé" ($\neg q$)
- Conclusión: "No estudié" ($\neg p$)

**Solución:** Aplicando **modus tollens**, el argumento es válido.

---

## 12. Aplicaciones en matemáticas y computación

### 12.1 Demostraciones matemáticas

La lógica es fundamental para:
- **Demostración directa:** Usar $p \to q$ directamente
- **Demostración por contradicción:** Asumir $\neg q$ y derivar una contradicción
- **Demostración por contrapositiva:** Demostrar $\neg q \to \neg p$

### 12.2 Álgebra booleana en computación

**Operaciones en bits:**
- AND ($\land$): $1 \land 1 = 1$, resto $= 0$
- OR ($\lor$): $0 \lor 0 = 0$, resto $= 1$
- NOT ($\neg$): $\neg 0 = 1$, $\neg 1 = 0$
- XOR ($\oplus$): $0 \oplus 0 = 0$, $1 \oplus 1 = 0$, resto $= 1$

**Compuertas lógicas:**
Los circuitos digitales implementan operaciones lógicas mediante compuertas (AND, OR, NOT, NAND, NOR, XOR).

**Búsquedas en bases de datos:**
- "Buscar libros de matemáticas **AND** álgebra"
- "Buscar artículos de física **OR** química"
- "Buscar documentos **NOT** confidenciales"

---

## 13. Resumen de conectivos lógicos

| Conectivo | Símbolo | Nombre | Se lee | Verdadero cuando... |
|-----------|---------|--------|--------|---------------------|
| Negación | $\neg p$ | NOT | "no $p$" | $p$ es falso |
| Conjunción | $p \land q$ | AND | "$p$ y $q$" | Ambos son verdaderos |
| Disyunción | $p \lor q$ | OR | "$p$ o $q$" | Al menos uno es verdadero |
| XOR | $p \oplus q$ | XOR | "$p$ o $q$ (exclusivo)" | Exactamente uno es verdadero |
| Implicación | $p \to q$ | IF-THEN | "si $p$ entonces $q$" | $p$ es falso o $q$ es verdadero |
| Bicondicional | $p \leftrightarrow q$ | IFF | "$p$ si y solo si $q$" | Ambos tienen el mismo valor |

---

## 14. Ejercicios propuestos

### 14.1 Proposiciones y valores de verdad

1. Determine cuáles son proposiciones y evalúe su valor de verdad:
   a) "$\pi$ es irracional"
   b) "¿Cuántos lados tiene un hexágono?"
   c) "$2^3 = 8$"
   d) "¡Qué día tan hermoso!"
   e) "$x + 5 = 10$"

2. Sea $p$: "$5 > 3$", $q$: "$2$ es impar". Evalúe:
   a) $p \land q$
   b) $p \lor q$
   c) $\neg p$
   d) $p \to q$

### 14.2 Tablas de verdad

3. Construya tablas de verdad para:
   a) $(p \land q) \lor \neg p$
   b) $\neg(p \lor q) \land r$
   c) $(p \to q) \land (q \to p)$

4. Verifique mediante tabla de verdad que $p \to q \equiv \neg p \lor q$

### 14.3 Leyes de De Morgan

5. Niegue las siguientes proposiciones:
   a) "Hace sol y hace calor"
   b) "Estudio matemáticas o física"
   c) "$x > 0$ y $x < 10$"

6. Simplifique usando las leyes de De Morgan:
   a) $\neg(p \land \neg q)$
   b) $\neg(\neg p \lor q)$

### 14.4 Simplificación

7. Simplifique usando propiedades:
   a) $(p \lor q) \land (p \lor \neg q)$
   b) $\neg(p \land q) \lor (p \land q)$
   c) $(p \to q) \land p$

8. Demuestre que $(p \land q) \to p$ es una tautología

### 14.5 Tautologías y contradicciones

9. Determine si son tautologías, contradicciones o contingencias:
   a) $p \lor \neg p$
   b) $p \land \neg p$
   c) $(p \to q) \lor (q \to p)$
   d) $(p \land q) \land \neg p$

### 14.6 Implicación y bicondicional

10. Para $p$: "$n$ es par", $q$: "$n$ es divisible por 2", escriba en palabras:
    a) $p \to q$
    b) $q \to p$
    c) $\neg q \to \neg p$
    d) $p \leftrightarrow q$

11. Determine la contrapositiva, recíproca e inversa de:
    "Si un número es divisible por 4, entonces es par"

12. Evalúe la validez de los siguientes argumentos:
    a) Premisas: $p \to q$, $p$; Conclusión: $q$
    b) Premisas: $p \to q$, $q$; Conclusión: $p$
    c) Premisas: $p \to q$, $\neg q$; Conclusión: $\neg p$

### 14.7 Aplicaciones

13. Un sistema de seguridad activa una alarma si:
    - La puerta está abierta Y es de noche, O
    - Hay movimiento Y no está desactivado
    
    Escriba la expresión lógica y construya su tabla de verdad.

14. Exprese en lógica proposicional:
    "Un triángulo es equilátero si y solo si todos sus lados son iguales y todos sus ángulos son iguales"

15. Niegue y simplifique:
    "Si estudio y hago ejercicios, entonces aprobaré el examen"

### 14.8 Demostración

16. Demuestre que $(p \to q) \land (p \to \neg q) \equiv \neg p$ es una tautología

17. Demuestre la ley distributiva: $p \lor (q \land r) \equiv (p \lor q) \land (p \lor r)$

18. Verifique que el silogismo hipotético es válido:
    $[(p \to q) \land (q \to r)] \to (p \to r)$

### 14.9 Razonamiento

19. Complete la conclusión válida:
    - Si hace frío, entonces uso abrigo
    - No uso abrigo
    - Por lo tanto, ...

20. Analice el siguiente argumento:
    - Si llueve, la calle está mojada
    - La calle está mojada
    - Por lo tanto, llueve
    
    ¿Es válido? Justifique.

---

**Fin de la Clase 2**
