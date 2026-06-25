# Los Números: Fundamentos y Construcción

En esta clase se construyen los sistemas numéricos fundamentales —naturales, enteros, racionales, irracionales y reales— a partir de la teoría de conjuntos, y se establecen los axiomas que caracterizan a los números reales como cuerpo ordenado completo.

## 1. Teoría de conjuntos: Lenguaje fundamental de las matemáticas

### 1.1 Concepto intuitivo de conjunto

Pensemos en una colección de objetos bien definidos: los colores primarios, los números pares, o los puntos de una recta. En matemáticas, a esas colecciones se las llama **conjuntos**, y a cada objeto individual se lo llama **elemento**. Esta noción, propuesta por Georg Cantor en 1874, es la base de toda la matemática moderna.

**Definición 1.1 (Conjunto y elemento):**
Un **conjunto** es una colección bien definida de objetos, llamados **elementos**. Si $x$ es un elemento del conjunto $A$, se escribe $x \in A$ (se lee "$x$ pertenece a $A$"); en caso contrario, se escribe $x \notin A$.

> **Nota:** En este curso trabajaremos con conjuntos "concretos" (números, puntos, funciones). La definición formal y axiomática de conjunto se desarrolla en la teoría de conjuntos de Zermelo-Fraenkel (ZFC) y se estudia en cursos avanzados de lógica.

**Ejemplo 1.1:**
Sea $A = \{1, 2, 3, 4, 5\}$ el conjunto de los primeros cinco números naturales. Entonces $3 \in A$ pero $7 \notin A$. Sea $B = \{a, e, i, o, u\}$ el conjunto de las vocales; entonces $a \in B$ pero $b \notin B$.

> **Observación:** Los elementos de un conjunto no se repiten ni tienen orden prefijado. Por ejemplo, $\{2, 2, 3\} = \{2, 3\}$ y $\{1, 2, 3\} = \{3, 2, 1\}$.
### 1.2 Formas de especificar un conjunto

A menudo necesitamos describir conjuntos que tienen muchos elementos o incluso infinitos. Listar uno por uno no siempre es práctico, así que disponemos de distintas formas de especificar qué elementos pertenecen a un conjunto.

**Definición 1.2 (Notación por extensión):**
Un conjunto está dado **por extensión** cuando se enumeran todos sus elementos entre llaves:
$$A = \{2, 4, 6, 8\}.$$

**Definición 1.3 (Notación por comprensión):**
Un conjunto está dado **por comprensión** cuando se indica una propiedad $P(x)$ que caracteriza a sus elementos dentro de un universo $U$:
$$A = \{x \in U : P(x)\}.$$
Se lee: "$A$ es el conjunto de todos los $x$ en $U$ tales que $P(x)$ se cumple".

**Ejemplo 1.2:**
- Por extensión: $V = \{a, e, i, o, u\}$.
- Por comprensión: $P = \{x \in \mathbb{N} : x \text{ es par y } x \leq 8\} = \{2, 4, 6, 8\}$.

**Representación gráfica: diagramas de Venn**
Además de las notaciones algebraicas, los conjuntos pueden representarse gráficamente mediante **diagramas de Venn**. En estos diagramas cada conjunto se dibuja como una curva cerrada y los elementos como puntos en su interior. La intersección aparece como la región común y la inclusión como una curva dentro de otra.

![[diagrama_venn_A.png]]
*Figura 1.2.1: Diagrama de Venn del conjunto $A = \{2, 4, 6, 8\}$ dentro del universo $U = \{1, 2, 3, 4, 5, 6, 7, 8, 9, 10\}$. Los elementos dentro de la elipse magenta pertenecen a $A$; los elementos fuera de la elipse pero dentro del rectángulo pertenecen a $U$ pero no a $A$.*

**Aplicaciones:**
La notación por comprensión es la base de los lenguajes de consulta en bases de datos (como SQL) y de la especificación de propiedades en lógica y programación. Los diagramas de Venn se usan en probabilidad para visualizar eventos y sus intersecciones.

> **Observación:** La notación por comprensión tiene la forma general $\{x \in U : P(x)\}$, donde $U$ es un "universo" de referencia y $P(x)$ es un predicado. Siempre debe quedar claro cuál es el universo; de lo contrario la descripción puede ser ambigua.

### 1.3 Operaciones entre conjuntos

Dados dos conjuntos, es natural combinarlos o compararlos: reunir todos sus elementos, quedarnos solo con los comunes, o eliminar los elementos de uno que aparecen en otro. Estas operaciones son el lenguaje con el que se expresan relaciones entre colecciones.

**Definición 1.4 (Unión):**
La **unión** de $A$ y $B$ es el conjunto de elementos que pertenecen a $A$ **o** a $B$ (o a ambos):
$$A \cup B = \{x : x \in A \text{ o } x \in B\}.$$
*Se lee "$A$ unión $B$".*

**Definición 1.5 (Intersección):**
La **intersección** de $A$ y $B$ es el conjunto de elementos que pertenecen a $A$ **y** a $B$ simultáneamente:
$$A \cap B = \{x : x \in A \text{ y } x \in B\}.$$
*Se lee "$A$ intersección $B$".*

**Definición 1.6 (Diferencia):**
La **diferencia** $A \setminus B$ es el conjunto de elementos de $A$ que **no** están en $B$:
$$A \setminus B = \{x : x \in A \text{ y } x \notin B\}.$$
*Se lee "$A$ menos $B$".*

**Ejemplo 1.3:**
Sean $A = \{1, 2, 3, 4\}$ y $B = \{3, 4, 5, 6\}$. Entonces:
- $A \cup B = \{1, 2, 3, 4, 5, 6\}$,
- $A \cap B = \{3, 4\}$,
- $A \setminus B = \{1, 2\}$,
- $B \setminus A = \{5, 6\}$.

**Aplicaciones:**
Las operaciones entre conjuntos modelan situaciones cotidianas y técnicas: la unión describe la combinación de listas de clientes o genes; la intersección identifica características compartidas entre grupos; la diferencia filtra elementos excluyendo ciertos criterios. En probabilidad, estas operaciones corresponden a eventos "o", "y" y "no".

> **Observación:** Dos conjuntos $A$ y $B$ se dicen **disjuntos** cuando $A \cap B = \emptyset$, es decir, cuando no tienen elementos en común.

### 1.4 La paradoja de Russell y los límites de la intuición

La noción intuitiva de conjunto parece suficiente para trabajar con colecciones de números o puntos, pero permite formar expresiones como "el conjunto de todos los conjuntos". A principios del siglo XX, Bertrand Russell descubrió que esta libertad conduce a contradicciones lógicas. Comprender este límite justifica por qué la matemática moderna requiere axiomas precisos para hablar de conjuntos.

**La paradoja de Russell:**
Consideremos el conjunto $R$ definido como:
$$R = \{x : x \text{ es un conjunto y } x \notin x\}.$$
Es decir, $R$ es el conjunto de todos los conjuntos que **no se contienen a sí mismos**.

Ahora preguntamos: ¿Es $R \in R$?
- Si $R \in R$, entonces por definición de $R$, debe cumplirse $R \notin R$. **Contradicción**.
- Si $R \notin R$, entonces cumple la condición para estar en $R$, luego $R \in R$. **Contradicción**.

**Conclusión:** La noción "ingenua" de conjunto conduce a contradicciones lógicas. Por ello, en el siglo XX se desarrolló la **Teoría Axiomática de Conjuntos** (Zermelo-Fraenkel, ZFC), que establece reglas precisas sobre qué colecciones son conjuntos válidos.

> **Nota:** Para este curso trabajaremos con conjuntos "naturales" (números, funciones, puntos geométricos) que no presentan estas paradojas. Las sutilezas formales se estudiarán en cursos avanzados de Lógica Matemática o Teoría de Conjuntos.

### 1.5 El conjunto vacío

Entre todas las colecciones posibles, hay una que resulta especial: la colección que no contiene ningún elemento. Aunque pueda parecer anodina a primera vista, el conjunto vacío es indispensable: actúa como elemento neutro para la unión y como punto de partida para construir los números naturales.

**Definición 1.7 (Conjunto vacío):**
El **conjunto vacío**, denotado por $\emptyset$ o $\{\}$, es el único conjunto que no contiene elementos. Formalmente:
$$\emptyset = \{\} \quad \text{tal que} \quad \forall x, \, x \notin \emptyset.$$

> **Nota:** El símbolo $\forall$ se lee "para todo". La condición anterior afirma que ningún objeto $x$ pertenece a $\emptyset$.

**Propiedades fundamentales:**

1. **Unicidad.** Existe exactamente un conjunto vacío. Si $A$ y $B$ son dos conjuntos sin elementos, entonces $A = B = \emptyset$.

2. **Subconjunto universal.** El conjunto vacío es subconjunto de cualquier conjunto:
   $$\forall A, \quad \emptyset \subseteq A.$$
   *Se lee "el conjunto vacío es subconjunto de $A$".*
   
   **Justificación:** La implicación "$x \in \emptyset \Rightarrow x \in A$" es **vacuamente verdadera**, ya que no existe ningún $x \in \emptyset$ que pueda contradecirla.

3. **Unión e intersección:**
   - $A \cup \emptyset = A$ (el vacío es neutro para la unión),
   - $A \cap \emptyset = \emptyset$ (la intersección con el vacío es siempre vacía),
   - $A \setminus \emptyset = A$,
   - $\emptyset \setminus A = \emptyset$.

**Ejemplo 1.4:**
- $\mathcal{P}(\emptyset) = \{\emptyset\}$ (el conjunto potencia del vacío tiene un elemento).
- Si $A = \{1, 2, 3\}$, entonces $A \cap \emptyset = \emptyset$ y $A \cup \emptyset = \{1, 2, 3\}$.

> **Observación filosófica:** El conjunto vacío puede parecer abstracto o incluso paradójico ("¿cómo puede existir un conjunto de nada?"), pero es absolutamente fundamental en matemáticas. Es el "ladrillo" más básico desde el cual se construyen todos los números (ver Sección 4). Así como el cero es esencial en aritmética, el conjunto vacío es esencial en teoría de conjuntos.

> **Analogía:** El conjunto vacío puede imaginarse como una caja vacía: la caja existe aunque no contenga nada. El conjunto vacío es "algo" (un conjunto válido), pero ese algo no contiene elementos.

> **Notación importante:** No confundir:
> - $\emptyset$ (el conjunto vacío, que no tiene elementos),
> - $\{\emptyset\}$ (el conjunto que contiene al conjunto vacío como único elemento, por lo tanto tiene 1 elemento),
> - $\{\{\emptyset\}\}$ (el conjunto que contiene al conjunto $\{\emptyset\}$, tiene 1 elemento).
>
> Estas distinciones serán cruciales en la construcción de von Neumann de los números naturales.

### 1.6 Cardinalidad

Una de las primeras preguntas que surge ante un conjunto es "¿cuántos elementos tiene?". La cardinalidad responde esa pregunta de manera precisa y permite comparar tamaños incluso cuando los conjuntos son infinitos.

**Definición 1.8 (Cardinalidad):**
La **cardinalidad** de un conjunto finito $A$, denotada $|A|$, $\#A$ o $\operatorname{card}(A)$, es el **número de elementos** que contiene.

**Ejemplo 1.5:**
- $|\{2, 4, 6\}| = 3$.
- $|\{a, b, c, d, e\}| = 5$.
- $|\emptyset| = 0$ (el conjunto vacío no tiene elementos).

> **Observación:** Para conjuntos infinitos, la noción de cardinalidad es más sutil y se basa en la idea de **biyecciones** entre conjuntos (ver Sección 8).

### 1.7 Conjunto potencia

Dado un conjunto, a menudo interesa estudiar todas las subcolecciones que se pueden formar con sus elementos. El conjunto de todos esos subconjuntos recibe el nombre de **conjunto potencia** y aparece de manera natural en combinatoria, lógica y teoría de la computación.

**Definición 1.9 (Conjunto potencia):**
Dado un conjunto $A$, el **conjunto potencia** de $A$, denotado $\mathcal{P}(A)$ o $2^A$, es el conjunto de **todos los subconjuntos** de $A$:
$$\mathcal{P}(A) = \{B : B \subseteq A\}.$$

**Ejemplo 1.6:**
Si $A = \{1, 2\}$, entonces:
$$\mathcal{P}(A) = \{\emptyset, \{1\}, \{2\}, \{1,2\}\}.$$
Se observa que $|\mathcal{P}(A)| = 4$.

**Ejemplo 1.7:**
Si $A = \{a, b, c\}$, entonces:
$$\mathcal{P}(A) = \{\emptyset, \{a\}, \{b\}, \{c\}, \{a,b\}, \{a,c\}, \{b,c\}, \{a,b,c\}\},$$
y $|\mathcal{P}(A)| = 8$.

**Caso especial - El conjunto vacío:**
$$\mathcal{P}(\emptyset) = \{\emptyset\}.$$
El conjunto potencia del vacío **no es vacío**: contiene un elemento (el conjunto vacío mismo).

**Teorema 1.1 (Cardinalidad del conjunto potencia):**
Si $A$ es un conjunto finito con $|A| = n$, entonces:
$$|\mathcal{P}(A)| = 2^n.$$

**Demostración (idea intuitiva):**
Para construir un subconjunto de $A$, debemos decidir, para cada elemento de $A$, si lo incluimos o no. Son 2 opciones por cada uno de los $n$ elementos, lo que da $2 \times 2 \times \cdots \times 2 = 2^n$ posibilidades. $\square$

**Ejemplo 1.8 (Crecimiento exponencial):**
- $|\emptyset| = 0$, $|\mathcal{P}(\emptyset)| = 2^0 = 1$.
- $|\{a\}| = 1$, $|\mathcal{P}(\{a\})| = 2^1 = 2$.
- $|\{a,b\}| = 2$, $|\mathcal{P}(\{a,b\})| = 2^2 = 4$.
- $|\{a,b,c\}| = 3$, $|\mathcal{P}(\{a,b,c\})| = 2^3 = 8$.
- $|\{a,b,c,d\}| = 4$, $|\mathcal{P}(\{a,b,c,d\})| = 2^4 = 16$.

**Aplicaciones:**
El conjunto potencia es central en combinatoria (contar subconjuntos), en lógica proposicional (cada subconjunto de variables puede interpretarse como una asignación de valores de verdad) y en teoría de la computación (autómatas y lenguajes formales).

**Teorema de Cantor (1891):**
Para **cualquier** conjunto $A$ (finito o infinito), no existe ninguna función sobreyectiva de $A$ a $\mathcal{P}(A)$. En particular:
$$|A| < |\mathcal{P}(A)|.$$

Este resultado implica que existe una **jerarquía infinita de infinitos**:
$$|\mathbb{N}| < |\mathcal{P}(\mathbb{N})| < |\mathcal{P}(\mathcal{P}(\mathbb{N}))| < \cdots$$

> **Observación profunda:** El teorema de Cantor muestra que, dado cualquier conjunto infinito, siempre se puede construir uno de cardinalidad estrictamente mayor (su conjunto potencia). Esta idea es una de las más importantes de las matemáticas modernas.

> **Observación:** La notación $2^A$ proviene de que $|2^A| = 2^{|A|}$ cuando $A$ es finito. Además, se tiene siempre $|A| < |\mathcal{P}(A)|$, de modo que $n < 2^n$ para todo $n \geq 0$.

---

## 2. Símbolos lógicos y lenguaje matemático

Las matemáticas usan un lenguaje simbólico para expresar ideas con precisión, brevedad y universalidad. Aprender a leer estos símbolos es tan importante como aprender a leer ecuaciones: permite traducir definiciones, teoremas y demostraciones de manera inequívoca.

### 2.1 Símbolos lógicos y de conjuntos

Los símbolos lógicos y de pertenencia aparecen en casi toda definición y teorema. La siguiente tabla resume los más frecuentes.

|      Símbolo      | Significado                   | Ejemplo                              | Lectura                                                       |
| :---------------: | :---------------------------- | :----------------------------------- | :------------------------------------------------------------ |
|     $\forall$     | Para todo, para cada          | $\forall x \in \mathbb{N}, x \geq 0$ | "Para todo x natural, x es mayor o igual a 0"                 |
|     $\exists$     | Existe (al menos uno)         | $\exists x \in \mathbb{R}: x^2 = 2$  | "Existe un real x tal que x² = 2"                             |
|   $\exists!$      | Existe único                  | $\exists! x \in \mathbb{R}: x^2 = 4 \land x > 0$ | "Existe un único real positivo x tal que x² = 4" |
|    $\nexists$     | No existe                     | $\nexists x \in \mathbb{Q}: x^2 = 2$ | "No existe un racional x tal que x² = 2"                      |
|   $\therefore$    | Por lo tanto, entonces        | $x=2 \therefore x^2=4$               | "x igual 2, por lo tanto x² igual 4"                          |
|      $\land$      | Y (conjunción lógica)         | $x > 0 \land x < 5$                  | "x mayor que 0 y x menor que 5"                               |
|      $\lor$       | O (disyunción lógica)         | $x < 0 \lor x > 10$                  | "x menor que 0 o x mayor que 10"                              |
|      $\neg$       | Negación (no)                 | $\neg(x > 0)$                        | "no (x mayor que 0)" o "x no es mayor que 0"                  |
|   $\Rightarrow$   | Implica                       | $x = 2 \Rightarrow x^2 = 4$          | "x igual 2 implica x² igual 4"                                |
| $\Leftrightarrow$ | Si y solo si (sii)            | $x^2 = 4 \Leftrightarrow x = \pm 2$  | "x² igual 4 si y solo si x es ±2"                             |
|       $\in$       | Pertenece a                   | $3 \in \mathbb{N}$                   | "3 pertenece a los naturales"                                 |
|     $\notin$      | No pertenece a                | $-1 \notin \mathbb{N}$               | "-1 no pertenece a los naturales"                             |
|     $\subset$     | Subconjunto propio            | $\mathbb{N} \subset \mathbb{Z}$      | "Los naturales están contenidos (propiamente) en los enteros" |
|    $\subseteq$    | Subconjunto (puede ser igual) | $A \subseteq B$                      | "A está contenido en B (posiblemente A = B)"                  |
|    $\supset$      | Superconjunto propio          | $\mathbb{Z} \supset \mathbb{N}$      | "Los enteros contienen propiamente a los naturales"           |
|    $\supseteq$    | Superconjunto (puede ser igual) | $B \supseteq A$                    | "B contiene a A (posiblemente B = A)"                         |

### 2.2 Símbolos de orden y comparación

Para comparar cantidades y expresar relaciones de igualdad o desigualdad se usan los siguientes símbolos.

|  Símbolo   | Significado                      | Ejemplo                  | Lectura                               |
| :--------: | :------------------------------- | :----------------------- | :------------------------------------ |
|    $=$     | Igual a                          | $2 + 2 = 4$              | "2 más 2 igual a 4"                   |
|   $\neq$   | Distinto de, diferente de        | $3 \neq 5$               | "3 distinto de 5"                     |
|    $<$     | Menor que (estrictamente)        | $2 < 5$                  | "2 menor que 5"                       |
|    $>$     | Mayor que (estrictamente)        | $7 > 3$                  | "7 mayor que 3"                       |
|   $\leq$   | Menor o igual que                | $x \leq 10$              | "x menor o igual que 10"              |
|   $\geq$   | Mayor o igual que                | $y \geq 0$               | "y mayor o igual que 0"               |
|   $\ll$    | Mucho menor que                  | $0.001 \ll 1000$         | "0.001 mucho menor que 1000"          |
|   $\gg$    | Mucho mayor que                  | $10^6 \gg 10$            | "un millón mucho mayor que 10"        |
|  $\approx$ | Aproximadamente igual            | $\pi \approx 3.14$       | "pi aproximadamente 3.14"             |
|  $\equiv$  | Idénticamente igual, congruente  | $x^2 - 1 \equiv (x-1)(x+1)$ | "x² - 1 idénticamente igual a (x-1)(x+1)" |

> **Observación sobre $\Rightarrow$ vs $\geq$:**
> - $\Rightarrow$ (flecha simple) denota **implicación lógica** entre proposiciones
> - $\geq$ denota **relación de orden** entre números
> - No confundir: "$x > 0 \Rightarrow x^2 > 0$" (implicación) vs "$x \geq 0$" (comparación)

### 2.3 Terminología matemática fundamental

En matemáticas se clasifican las afirmaciones según su papel y su importancia relativa. Conocer esta terminología ayuda a entender qué se está afirmando y qué tipo de justificación se espera.

**Definición 2.1 (Axioma):**
Un **axioma** (o **postulado**) es una proposición que se acepta como verdadera sin demostración y que sirve de fundamento para una teoría matemática.

**Ejemplo 2.1:**
- "Dos puntos determinan una única recta" (axioma de geometría euclidiana).
- Los axiomas de Peano para los números naturales.
- Los axiomas de cuerpo para $\mathbb{R}$ (ver Sección 9).

**Definición 2.2 (Teorema):**
Un **teorema** es una proposición matemática importante que ha sido demostrada a partir de axiomas y resultados previos.

**Ejemplo 2.2:**
- Teorema 5.1: Caracterización decimal de racionales.
- Teorema 7.1: $|\mathbb{Z}| = |\mathbb{N}|$.
- Teorema 8.1: Los reales no son numerables (Teorema de Cantor).

**Definición 2.3 (Lema):**
Un **lema** es una proposición auxiliar que se demuestra para facilitar la demostración de un teorema más importante.

**Ejemplo 2.3:**
- Lema de Euclides: si un primo divide un producto, divide algún factor.
- Lema de Zorn (teoría de conjuntos).

**Definición 2.4 (Corolario):**
Un **corolario** es una proposición que se deduce de manera directa de un teorema o proposición anterior.

**Ejemplo 2.4:**
- Corolario del Teorema 5.1: Los números con expansión decimal infinita no periódica son irracionales.

**Definición 2.5 (Proposición):**
Una **proposición** es un resultado matemático demostrado, pero de menor importancia o generalidad que un teorema.

**Ejemplo 2.5:**
- Proposición 3.1: Propiedades de la suma en $\mathbb{N}$.
- Proposición 10.1: $1 + 0 = 1$.

**Jerarquía conceptual:**
```
Axioma (sin demostración, fundamento)
   ↓
Lema (auxiliar) → Teorema (resultado principal) → Corolario (consecuencia)
   ↓                      ↓
Proposición (resultado menor)
```

> **Observación:** En la práctica, la distinción entre teorema, proposición y lema no siempre es estricta. Lo que un autor llama "proposición" otro podría llamar "teorema" si lo considera suficientemente importante. Sin embargo, los axiomas y corolarios tienen roles más precisamente definidos.

### 2.4 El alfabeto griego

El alfabeto latino solo ofrece 26 letras, una cantidad insuficiente para nombrar la diversidad de variables, parámetros, funciones y constantes que aparecen en matemáticas. El alfabeto griego aporta 24 símbolos más, muchos de los cuales adquirieron significados casi universales gracias al trabajo de Leonhard Euler en el siglo XVIII. Por esta razón, resulta indispensable reconocer su pronunciación y sus usos más frecuentes.

**Distinción conceptual:**
- Letras latinas ($x, y, z$): típicamente variables o coordenadas.
- Letras griegas ($\alpha, \beta, \theta$): ángulos, parámetros, funciones especiales.

**Convenciones universales:**
- $\pi$: razón entre la circunferencia y el diámetro, $\pi\approx 3{,}14159\ldots$
- $\Sigma$ (sigma mayúscula): suma de una serie.
- $\Delta$ (delta mayúscula): diferencia o cambio.
- $\epsilon$ (épsilon): cantidad arbitrariamente pequeña, típica en límites.
- $\theta, \phi$: ángulos en trigonometría.
- $\lambda$: valores propios, longitud de onda.
- $\mu$: media de una distribución, coeficiente de fricción.
- $\sigma$: desviación estándar.

> **Nota histórica:** Leonhard Euler popularizó muchas de estas convenciones en el siglo XVIII, como $\pi$ para la constante circular (1737) y $\Sigma$ para sumatorias. Durante los siglos XIX y XX la notación griega se estandarizó en el análisis matemático, la física teórica, la estadística y la probabilidad.

**El alfabeto griego completo:**

| Mayúscula  |        Minúscula        | Nombre  | Pronunciación | Uso común en matemáticas                        |
| :--------: | :---------------------: | :------ | :------------ | :---------------------------------------------- |
|  $\Alpha$  |        $\alpha$         | Alfa    | alfa          | Ángulos, coeficientes                           |
|  $\Beta$   |         $\beta$         | Beta    | beta          | Ángulos, coeficientes                           |
|  $\Gamma$  |        $\gamma$         | Gamma   | gama          | Función Gamma, ángulos                          |
|  $\Delta$  |        $\delta$         | Delta   | delta         | Diferencia, incremento, discriminante           |
| $\Epsilon$ | $\epsilon, \varepsilon$ | Épsilon | épsilon       | Número pequeño, límites                         |
|  $\Zeta$   |         $\zeta$         | Zeta    | dseta         | Función zeta de Riemann                         |
|   $\Eta$   |         $\eta$          | Eta     | eta           | Eficiencia, coordenadas                         |
|  $\Theta$  |   $\theta, \vartheta$   | Theta   | theta         | Ángulos, temperatura                            |
|  $\Iota$   |         $\iota$         | Iota    | iota          | Índices                                         |
|  $\Kappa$  |        $\kappa$         | Kappa   | kapa          | Curvatura, constante dieléctrica                |
| $\Lambda$  |        $\lambda$        | Lambda  | lambda        | Valores propios, longitud de onda               |
|   $\Mu$    |          $\mu$          | Mu      | mu            | Media, coeficiente de fricción, micro-          |
|   $\Nu$    |          $\nu$          | Nu      | nu            | Frecuencia, grados de libertad                  |
|   $\Xi$    |          $\xi$          | Xi      | ksi           | Variable aleatoria, coordenadas                 |
| $\Omicron$ |           $o$           | Ómicron | ómicron       | Raramente usado (se confunde con O latina)      |
|   $\Pi$    |      $\pi, \varpi$      | Pi      | pi            | Constante π ≈ 3.14159..., producto              |
|   $\Rho$   |     $\rho, \varrho$     | Rho     | ro            | Densidad, radio polar, correlación              |
|  $\Sigma$  |   $\sigma, \varsigma$   | Sigma   | sigma         | Suma ($\Sigma$), desviación estándar ($\sigma$) |
|   $\Tau$   |         $\tau$          | Tau     | tau           | Constante de tiempo, torque, τ = 2π             |
| $\Upsilon$ |       $\upsilon$        | Ípsilon | ípsilon       | Raramente usado                                 |
|   $\Phi$   |     $\phi, \varphi$     | Fi      | fi            | Función, ángulo, razón áurea                    |
|   $\Chi$   |         $\chi$          | Ji      | ji            | Distribución chi-cuadrado                       |
|   $\Psi$   |         $\psi$          | Psi     | psi           | Función de onda (mecánica cuántica)             |
|  $\Omega$  |        $\omega$         | Omega   | omega         | Frecuencia angular, resistencia eléctrica (Ω)   |

> **Observaciones importantes:**
>
> 1. **Variantes tipográficas:** Algunas letras tienen variantes estilísticas:
>    - Épsilon: $\epsilon$ (lunate) vs $\varepsilon$ (curvilínea)
>    - Theta: $\theta$ (con línea) vs $\vartheta$ (script theta)
>    - Pi: $\pi$ (normal) vs $\varpi$ (variante pomega)
>    - Rho: $\rho$ (normal) vs $\varrho$ (con cola)
>    - Phi: $\phi$ (cerrada) vs $\varphi$ (abierta)
>
> 2. **Letras griegas en mayúscula que se parecen a las latinas:**
>    - $\Alpha$ (A), $\Beta$ (B), $\Epsilon$ (E), $\Zeta$ (Z), $\Eta$ (H), $\Iota$ (I), $\Kappa$ (K), $\Mu$ (M), $\Nu$ (N), $\Omicron$ (O), $\Rho$ (P), $\Tau$ (T), $\Chi$ (X)
>    - Por esta similitud, raramente se usan las mayúsculas de estas letras en notación matemática
>
> 3. **Letras distintivas más usadas:**
>    - Mayúsculas: $\Gamma, \Delta, \Theta, \Lambda, \Xi, \Pi, \Sigma, \Phi, \Psi, \Omega$
>    - Minúsculas: $\alpha, \beta, \gamma, \delta, \epsilon, \zeta, \theta, \lambda, \mu, \pi, \rho, \sigma, \tau, \phi, \omega$

> **Recomendación práctica:** Es recomendable familiarizarse con la pronunciación y escritura de las letras griegas, ya que resultan imprescindibles para la lectura y la comunicación matemática efectivas.

---

## 3. Construcción de los números naturales

Después de establecer el lenguaje de conjuntos, podemos construir los números naturales sin apelar a la intuición de "contar". La idea es partir de un objeto básico —el conjunto vacío— y definir cada número como el conjunto de todos los anteriores. Este proceso, desarrollado por John von Neumann en 1923, muestra que la aritmética puede fundarse únicamente en teoría de conjuntos.

### 3.1 El conjunto vacío y la construcción de von Neumann

**Definición 3.1 (Números naturales según von Neumann):**
Partiendo del conjunto vacío $\emptyset$, se define recursivamente:
$$0 := \emptyset = \{\},$$
$$1 := \{0\} = \{\emptyset\},$$
$$2 := \{0, 1\} = \{\emptyset, \{\emptyset\}\},$$
$$3 := \{0, 1, 2\},$$
y en general:
$$n := \{0, 1, 2, \dots, n-1\}.$$

En esta construcción, cada número natural $n$ es el conjunto de todos los números naturales menores que $n$. Notamos que $|n| = n$; es decir, la cardinalidad del conjunto coincide con el número mismo.

**Definición 3.2 (Función sucesor):**
La función sucesor $S$ se define como:
$$S(n) = n \cup \{n\}.$$
De esta manera, $S(n)$ representa al siguiente número natural, es decir, $n + 1$.

**Ejemplo 3.1:**
$$S(2) = 2 \cup \{2\} = \{0, 1\} \cup \{2\} = \{0, 1, 2\} = 3.$$

**Definición 3.3 (Conjunto de los números naturales):**
$$\mathbb{N} = \{0, 1, 2, 3, 4, \dots\}.$$

> **Convención para este curso:**
> - $\mathbb{N}^{*} = \{1, 2, 3, 4, \dots\}$ (naturales **sin** cero, también denotado $\mathbb{N}^{+}$).
> - $\mathbb{N} = \{0, 1, 2, 3, \dots\}$ (naturales **con** cero, también denotado $\mathbb{N}_0$).
>
> Diferentes textos usan convenciones distintas; lo esencial es declarar la convención al inicio de cada desarrollo.

### 3.2 La recta numérica de los naturales

La recta numérica permite visualizar $\mathbb{N}$ como puntos discretos sobre una línea. Esta representación es útil para entender el orden y la noción de "siguiente".

![[recta_numeros_naturales.png]]

**Características:**
- $\mathbb{N}$ tiene un primer elemento, el $0$.
- No tiene último elemento: es infinito.
- Está bien ordenado: entre dos naturales consecutivos no hay otro natural.
- Es discreto: no hay continuidad entre sus elementos.
- Existe un orden natural; por ejemplo, $5 > 3$, por lo que $\mathbb{N}$ es un conjunto ordenado.

### 3.3 La suma en $\mathbb{N}$

Una vez construidos los números, definimos la suma de manera recursiva a partir de la función sucesor. Esta definición captura la idea intuitiva de "seguir contando".

**Definición 3.4 (Suma de números naturales):**
Para cualesquiera $m, n \in \mathbb{N}$:
1. **Caso base:** $m + 0 = m$.
2. **Caso recursivo:** $m + S(n) = S(m + n)$.

> **Nota:** La definición anterior afirma que sumar $m + n$ equivale a aplicar la función sucesor $n$ veces al número $m$.

**Ejemplo 3.2 (Calculando $2 + 3$):**
$$\begin{align}
2 + 3 &= 2 + S(2) \\
&= S(2 + 2) \\
&= S(2 + S(1)) \\
&= S(S(2 + 1)) \\
&= S(S(2 + S(0))) \\
&= S(S(S(2 + 0))) \\
&= S(S(S(2))) \\
&= S(S(3)) \\
&= S(4) \\
&= 5.
\end{align}$$

**Proposición 3.1 (Propiedades de la suma):**
La suma en $\mathbb{N}$ satisface:
1. **Cerradura:** $\forall m, n \in \mathbb{N},\; m + n \in \mathbb{N}$.
2. **Asociatividad:** $\forall m, n, p \in \mathbb{N},\; (m + n) + p = m + (n + p)$.
3. **Conmutatividad:** $\forall m, n \in \mathbb{N},\; m + n = n + m$.
4. **Elemento neutro:** $\forall m \in \mathbb{N},\; m + 0 = 0 + m = m$.
5. **Ley de cancelación:** $\forall m, n, p \in \mathbb{N},\; m + p = n + p \Rightarrow m = n$.

> **Nota:** Estas propiedades se demuestran por inducción matemática, técnica que se estudia en detalle en el curso de Álgebra I.

### 3.4 La resta en $\mathbb{N}$: una operación parcial

En los naturales no siempre es posible restar: no existe un natural $k$ tal que $5 + k = 3$. Esta limitación es importante porque motiva la ampliación a los enteros.

**Definición 3.5 (Resta en $\mathbb{N}$):**
Dados $m, n \in \mathbb{N}$, decimos que $m - n$ existe en $\mathbb{N}$ si y solo si existe $k \in \mathbb{N}$ tal que:
$$n + k = m.$$
En ese caso, escribimos $k = m - n$.

**Ejemplo 3.3:**
- $12 - 2 = 10$ está definida en $\mathbb{N}$, porque $2 + 10 = 12$.
- $7 - 4 = 3$ está definida en $\mathbb{N}$, porque $4 + 3 = 7$.
- $3 - 5$ no está definida en $\mathbb{N}$, porque no existe $k \in \mathbb{N}$ tal que $5 + k = 3$.

**Condición necesaria y suficiente:**
$$m - n \in \mathbb{N} \quad \Longleftrightarrow \quad m \geq n.$$

> **Observación:** Cuando escribimos $m - n$ en $\mathbb{N}$, asumimos implícitamente que $m \geq n$. Ecuaciones como $5 + x = 3$ no tienen solución en $\mathbb{N}$; se resolverán al ampliar a $\mathbb{Z}$.

### 3.5 La multiplicación en $\mathbb{N}$

La multiplicación se introduce como suma repetida, lo que permite definirla recursivamente a partir de la suma.

**Definición 3.6 (Multiplicación de números naturales):**
Para cualesquiera $m, n \in \mathbb{N}$:
1. **Caso base:** $m \cdot 0 = 0$.
2. **Caso recursivo:** $m \cdot S(n) = m \cdot n + m$.

Equivalentemente, $m \cdot n = \underbrace{m + m + \cdots + m}_{n \text{ veces}}$.

**Ejemplo 3.4 (Calculando $3 \times 4$):**
$$\begin{align}
3 \cdot 4 &= 3 \cdot S(3) \\
&= 3 \cdot 3 + 3 \\
&= (3 \cdot S(2)) + 3 \\
&= (3 \cdot 2 + 3) + 3 \\
&= \cdots \\
&= 12.
\end{align}$$

**Proposición 3.2 (Propiedades de la multiplicación):**
La multiplicación en $\mathbb{N}$ satisface:
1. **Cerradura:** $\forall m, n \in \mathbb{N},\; m \cdot n \in \mathbb{N}$.
2. **Asociatividad:** $\forall m, n, p \in \mathbb{N},\; (m \cdot n) \cdot p = m \cdot (n \cdot p)$.
3. **Conmutatividad:** $\forall m, n \in \mathbb{N},\; m \cdot n = n \cdot m$.
4. **Elemento neutro:** $\forall m \in \mathbb{N},\; m \cdot 1 = 1 \cdot m = m$.
5. **Distributividad:** $\forall m, n, p \in \mathbb{N},\; m \cdot (n + p) = m \cdot n + m \cdot p$.
6. **Ley de cancelación:** $\forall m, n, p \in \mathbb{N},\; m \cdot p = n \cdot p \land p \neq 0 \Rightarrow m = n$.
7. **Absorción del cero:** $\forall m \in \mathbb{N},\; m \cdot 0 = 0 \cdot m = 0$.

> **Nota:** Estas propiedades se demuestran por inducción. La distributividad conecta suma y multiplicación y es fundamental para todo el álgebra posterior.

### 3.6 Múltiplos en $\mathbb{N}$

La noción de múltiplo surge directamente de la multiplicación y será esencial para estudiar divisibilidad, MCD y MCM.

**Definición 3.7 (Múltiplo):**
Dados $a, b \in \mathbb{N}$, decimos que $b$ es un **múltiplo** de $a$ si existe $k \in \mathbb{N}$ tal que:
$$b = a \cdot k.$$
También se dice que $a$ es un **factor** de $b$ o que $b$ es divisible por $a$.

**Ejemplo 3.5:**
- $12$ es múltiplo de $3$, pues $12 = 3 \cdot 4$.
- $20$ es múltiplo de $5$, pues $20 = 5 \cdot 4$.
- $0$ es múltiplo de cualquier $a$, pues $0 = a \cdot 0$.

**Conjunto de múltiplos:**
El conjunto de todos los múltiplos de $a \in \mathbb{N}$ se denota:
$$M(a) = \{a \cdot k : k \in \mathbb{N}\} = \{0, a, 2a, 3a, \dots\}.$$

**Ejemplo 3.6:**
- $M(2) = \{0, 2, 4, 6, 8, \dots\}$ (números pares).
- $M(3) = \{0, 3, 6, 9, 12, \dots\}$.
- $M(1) = \mathbb{N}$.

> **Observación:** El estudio de múltiplos y divisores se extiende en la Sección 4 al conjunto de los números enteros, donde la divisibilidad adquiere mayor simetría.

**Aplicaciones:**
La construcción recursiva de los naturales y sus operaciones es la base de la aritmética computacional: los procesadores implementan suma y multiplicación mediante operaciones iteradas sobre representaciones binarias. Los múltiplos y la divisibilidad aparecen en criptografía (RSA), teoría de números y algoritmos de sincronización.


## 4. Los números enteros: $\mathbb{Z}$

### 4.1 Motivación: la resta en los naturales

Pensemos en la ecuación $5 + x = 3$. En $\mathbb{N}$, dicha ecuación no tiene solución, pues la resta $3 - 5$ no está definida. Los números naturales permiten contar y sumar libremente, pero no restar en todas las situaciones. Para que toda ecuación de la forma $a + x = b$ posea una solución, se extiende $\mathbb{N}$ a un conjunto que incluya los números negativos.

> **Nota histórica:** Los números negativos fueron rechazados durante siglos en Europa, mientras que en la India Brahmagupta ya los manipulaba sistemáticamente en el siglo VII. No se aceptaron plenamente en Occidente hasta el Renacimiento, con trabajos de Cardano y Descartes.

**Definición 4.1 (Conjunto de los números enteros):**
El conjunto de los **números enteros** es
$$\mathbb{Z} = \{ \dots, -3, -2, -1, 0, 1, 2, 3, \dots \}.$$
El símbolo $\mathbb{Z}$ proviene del alemán *Zahlen* (números).

Se distinguen los siguientes subconjuntos:
- **Enteros positivos:** $\mathbb{Z}^+ = \{1, 2, 3, \dots\} = \mathbb{N}^*$.
- **Enteros negativos:** $\mathbb{Z}^- = \{\dots, -3, -2, -1\}$.
- **Enteros no negativos:** $\mathbb{Z}_{\geq 0} = \{0, 1, 2, 3, \dots\} = \mathbb{N}$.

> **Observación:** En este proyecto se utiliza $\mathbb{N} = \{0, 1, 2, \dots\}$. Por tanto, $\mathbb{Z}^+ = \mathbb{N} \setminus \{0\} = \mathbb{N}^*$, y $\mathbb{Z} = \mathbb{Z}^- \cup \{0\} \cup \mathbb{Z}^+$ es una unión disjunta.

**Ejemplo 4.1:**
Se tiene que $-7 \in \mathbb{Z}$ pero $-7 \notin \mathbb{N}$; $0 \in \mathbb{Z} \cap \mathbb{N}$; y $\dfrac{1}{2} \notin \mathbb{Z}$.

**Aplicaciones:**
Los enteros modelan situaciones con dos direcciones opuestas: temperaturas bajo cero, saldos deudores, desplazamientos hacia la izquierda en la recta numérica y diferencias de tiempo. Sin ellos, la resta general no estaría definida.

### 4.2 Construcción formal por clases de equivalencia (opcional)

La descripción $\mathbb{Z} = \{\dots, -2, -1, 0, 1, 2, \dots\}$ es intuitiva, pero no explica por qué $-3$ es un objeto matemático legítimo ni cómo se suman los negativos. Una construcción rigurosa parte exclusivamente de los números naturales.

**Definición 4.2 (Construcción de los enteros):**
Se define $\mathbb{Z}$ como el conjunto de clases de equivalencia del producto cartesiano $\mathbb{N} \times \mathbb{N}$ bajo la relación
$$(a,b) \sim (c,d) \quad \Longleftrightarrow \quad a + d = b + c,$$
donde el par $(a,b)$ representa intuitivamente la diferencia $a - b$.

La suma y el producto se definen sobre las clases mediante representantes:
$$[(a,b)] + [(c,d)] = [(a+c, b+d)],$$
$$[(a,b)] \cdot [(c,d)] = [(ac + bd, ad + bc)].$$

Se verifica que estas operaciones no dependen de los representantes elegidos. La clase $[(0,0)]$ actúa como cero, y $[(b,a)]$ es el inverso aditivo de $[(a,b)]$.

> **Nota:** Esta construcción muestra que los enteros negativos no son símbolos arbitrarios, sino pares ordenados de naturales identificados mediante una relación de equivalencia. Puede omitirse en una primera lectura sin pérdida de continuidad.

### 4.3 Operaciones en $\mathbb{Z}$

Una vez construido $\mathbb{Z}$, las operaciones se extienden de $\mathbb{N}$ conservando las propiedades algebraicas deseables: asociatividad, conmutatividad y distributividad.

**Definición 4.3 (Suma y resta en $\mathbb{Z}$):**
Dados $m, n \in \mathbb{Z}$, la **suma** $m + n$ extiende la suma en $\mathbb{N}$ y satisface $m + (-m) = 0$ para todo $m \in \mathbb{Z}$. La **resta** se define como
$$m - n := m + (-n),$$
donde $-n$ es el **inverso aditivo** de $n$, es decir, el único entero tal que $n + (-n) = 0$.

**Definición 4.4 (Multiplicación en $\mathbb{Z}$):**
Dados $m, n \in \mathbb{Z}$, el producto $m \cdot n$ se define de modo que:
- si $n > 0$, entonces $m \cdot n = \underbrace{m + m + \dots + m}_{n \text{ veces}}$;
- $m \cdot 0 = 0$;
- si $n < 0$, entonces $m \cdot n = -(m \cdot |n|)$.

**Proposición 4.1 (Propiedades algebraicas de $\mathbb{Z}$):**
Para cualesquiera $a, b, c \in \mathbb{Z}$ se cumple:
1. **Cerradura:** $a + b \in \mathbb{Z}$ y $a \cdot b \in \mathbb{Z}$.
2. **Asociatividad:** $(a + b) + c = a + (b + c)$ y $(a \cdot b) \cdot c = a \cdot (b \cdot c)$.
3. **Conmutatividad:** $a + b = b + a$ y $a \cdot b = b \cdot a$.
4. **Elementos neutros:** $a + 0 = a$ y $a \cdot 1 = a$.
5. **Inverso aditivo:** existe $-a \in \mathbb{Z}$ tal que $a + (-a) = 0$.
6. **Distributividad:** $a \cdot (b + c) = a \cdot b + a \cdot c$.
7. **Producto nulo:** $a \cdot b = 0 \Longleftrightarrow a = 0$ o $b = 0$.

> **Observación:** $(\mathbb{Z}, +, \cdot)$ es un **anillo conmutativo con unidad**. No es un cuerpo, porque la mayoría de los enteros no tienen inverso multiplicativo en $\mathbb{Z}$; por ejemplo, no existe $x \in \mathbb{Z}$ tal que $2x = 1$.

> **Nota:** Las demostraciones de estas propiedades a partir de la construcción por clases de equivalencia de la Definición 4.2 se desarrollan en cursos de álgebra abstracta. Aquí se aceptan como consecuencia de dicha construcción y de la extensión natural de las operaciones en $\mathbb{N}$.

**Ejemplo 4.2:**
Calcular $(-3) \cdot (-5)$ y $4 \cdot (-2)$:
$$(-3) \cdot (-5) = -(3 \cdot (-5)) = -(-(3 \cdot 5)) = 15,$$
$$4 \cdot (-2) = -(4 \cdot 2) = -8.$$

La regla de los signos se resume en la siguiente tabla:

| $a$ | $b$ | $a \cdot b$ |
|:---:|:---:|:-----------:|
| $+$ | $+$ | $+$ |
| $+$ | $-$ | $-$ |
| $-$ | $+$ | $-$ |
| $-$ | $-$ | $+$ |

### 4.4 Divisibilidad y conjunto de divisores

En $\mathbb{Z}$ no siempre es posible dividir: $7 \div 2$ no produce un entero. La divisibilidad captura exactamente cuándo sí es posible efectuar la división dentro de $\mathbb{Z}$.

**Definición 4.5 (Divisibilidad):**
Sean $a, b \in \mathbb{Z}$ con $b \neq 0$. Se dice que $b$ **divide** a $a$, y se escribe $b \mid a$, si existe $c \in \mathbb{Z}$ tal que
$$a = b \cdot c.$$
En tal caso, $b$ es un **divisor** de $a$, y $a$ es un **múltiplo** de $b$. Si $b$ no divide a $a$, se escribe $b \nmid a$.

**Proposición 4.2 (Propiedades de la divisibilidad):**
Para cualesquiera $a, b, c \in \mathbb{Z}$ (con los divisores no nulos cuando se requiera):
1. $a \mid a$ para todo $a \in \mathbb{Z} \setminus \{0\}$.
2. Si $a \mid b$ y $b \mid c$, entonces $a \mid c$.
3. $1 \mid a$ y $a \mid 0$ para todo $a \in \mathbb{Z} \setminus \{0\}$.
4. Si $a \mid b$ y $a \mid c$, entonces $a \mid (b + c)$ y $a \mid (b - c)$.

**Demostración:**
Se prueba la propiedad 4 como ejemplo. Si $a \mid b$ y $a \mid c$, existen $k, \ell \in \mathbb{Z}$ tales que $b = ak$ y $c = a\ell$. Entonces
$$b + c = ak + a\ell = a(k + \ell),$$
y $k + \ell \in \mathbb{Z}$, luego $a \mid (b + c)$. Análogamente, $b - c = a(k - \ell)$, por lo que $a \mid (b - c)$. $\blacksquare$

**Definición 4.6 (Conjunto de divisores positivos):**
Dado $n \in \mathbb{Z} \setminus \{0\}$, su conjunto de divisores positivos es
$$D(n) = \{ d \in \mathbb{N}^* : d \mid n \}.$$

**Definición 4.7 (Número primo):**
Un entero $p > 1$ es **primo** si sus únicos divisores positivos son $1$ y $p$, es decir, $D(p) = \{1, p\}$. Un entero mayor que $1$ que no es primo se llama **compuesto**.

> **Observación:** El número $1$ no es primo ni compuesto. Todo entero no nulo divide a $0$, pues $0 = a \cdot 0$.

**Ejemplo 4.3:**
- $3 \mid 12$ porque $12 = 3 \cdot 4$.
- $6 \nmid 15$ pues no existe $c \in \mathbb{Z}$ tal que $15 = 6c$.
- $D(12) = \{1, 2, 3, 4, 6, 12\}$.
- $D(7) = \{1, 7\}$, por lo que $7$ es primo.

### 4.5 División euclidiana

Aunque la división exacta no siempre es posible, sí se puede dividir con resto. Este resultado es la base del algoritmo de Euclides y de la aritmética modular.

> **Nota histórica:** La división con resto aparece ya en los *Elementos* de Euclides (c. 300 a.C.), donde se utiliza como herramienta fundamental para estudiar la divisibilidad.

**Teorema 4.1 (División euclidiana):**
Dados $a, b \in \mathbb{Z}$ con $b > 0$, existen únicos enteros $q$ (cociente) y $r$ (resto) tales que
$$a = b \cdot q + r \quad \text{con} \quad 0 \leq r < b.$$

**Demostración:**

*Existencia.* Sea $S = \{ a - bq : q \in \mathbb{Z} \} \cap \mathbb{N}$. Como $b > 0$, eligiendo $q$ suficientemente negativo se tiene $a - bq \geq 0$, así que $S$ es no vacío. Por el principio del buen orden, $S$ posee un mínimo $r = a - bq_0$ para algún $q_0 \in \mathbb{Z}$. Entonces $r \geq 0$. Si $r \geq b$, se tendría
$$a - b(q_0 + 1) = r - b \geq 0,$$
lo cual contradice la minimalidad de $r$. Por tanto $r < b$.

*Unicidad.* Supongamos que $a = bq + r = bq' + r'$ con $0 \leq r, r' < b$. Restando,
$$b(q - q') = r' - r.$$
Como $-b < r' - r < b$, el único múltiplo de $b$ en ese intervalo es $0$. Luego $r' = r$ y, puesto que $b \neq 0$, se deduce $q' = q$. $\blacksquare$

**Ejemplo 4.4:**
- $17 = 5 \cdot 3 + 2$, de modo que $q = 3$ y $r = 2$.
- $-17 = 5 \cdot (-4) + 3$, pues se exige $0 \leq r < 5$; no se admite $-17 = 5 \cdot (-3) + (-2)$.

### 4.6 Aritmética modular

La división euclidiana asigna a cada entero un resto respecto de un divisor fijo. Ese resto es la piedra angular de la aritmética modular.

**Definición 4.8 (Operación módulo):**
Dados $a, b \in \mathbb{Z}$ con $b > 0$, el **módulo** de $a$ respecto de $b$, denotado $a \bmod b$, es el único resto $r$ de la división euclidiana de $a$ entre $b$:
$$a \bmod b = r \quad \text{donde} \quad a = bq + r, \quad 0 \leq r < b.$$
La notación $a \equiv c \pmod{b}$ indica que $a \bmod b = c \bmod b$.

**Proposición 4.3 (Propiedades del módulo):**
Para cualesquiera $a, c \in \mathbb{Z}$ y $b > 0$ se cumple:
1. $0 \leq a \bmod b < b$.
2. $a \bmod b = 0 \Longleftrightarrow b \mid a$.
3. $(a + c) \bmod b = \bigl((a \bmod b) + (c \bmod b)\bigr) \bmod b$.
4. $(a \cdot c) \bmod b = \bigl((a \bmod b) \cdot (c \bmod b)\bigr) \bmod b$.

**Demostración:**
Las dos primeras propiedades se siguen directamente de la Definición 4.8 y del Teorema 4.1. Para la tercera, escribamos $a = bq_1 + r_1$ y $c = bq_2 + r_2$ con $0 \leq r_1, r_2 < b$. Entonces
$$a + c = b(q_1 + q_2) + (r_1 + r_2).$$
Si $r_1 + r_2 < b$, el resto de $a + c$ al dividir por $b$ es $r_1 + r_2$; si $r_1 + r_2 \geq b$, se le resta $b$ el número necesario de veces. En ambos casos el resultado coincide con $(r_1 + r_2) \bmod b$, que es la propiedad enunciada. La demostración para el producto es análoga, pues
$$a \cdot c = b^2 q_1 q_2 + b(q_1 r_2 + q_2 r_1) + r_1 r_2,$$
y el resto de $a \cdot c$ respecto de $b$ es el mismo que el de $r_1 r_2$. $\blacksquare$

**Ejemplo 4.5:**
- $23 \bmod 7 = 2$ porque $23 = 7 \cdot 3 + 2$.
- $101 \bmod 7 = 3$ porque $101 = 7 \cdot 14 + 3$.
- $(17 + 8) \bmod 5 = 25 \bmod 5 = 0$, y también $(2 + 3) \bmod 5 = 0$.

**Aplicaciones:**
La aritmética modular aparece en criptografía (RSA, curvas elípticas), en el diseño de funciones hash, en la generación de números pseudoaleatorios, en la corrección de errores y en la programación de calendarios y relojes. Por ejemplo, las $15:00$ horas equivalen a las $3:00$ PM porque $15 \bmod 12 = 3$.

### 4.7 Máximo común divisor y mínimo común múltiplo

El divisor común más grande de dos enteros y el múltiplo común más pequeño son dos cantidades fundamentales en la teoría de números.

> **Nota histórica:** El algoritmo de Euclides para calcular el máximo común divisor es uno de los algoritmos más antiguos conocidos y aparece en el Libro VII de los *Elementos* de Euclides.

**Definición 4.9 (Máximo común divisor):**
Dados $a, b \in \mathbb{Z}$ no ambos nulos, el **máximo común divisor** de $a$ y $b$ es
$$\gcd(a,b) = \max\{ d \in \mathbb{N}^* : d \mid a \text{ y } d \mid b \}.$$
Equivalentemente, $\gcd(a,b) = \max\bigl(D(a) \cap D(b)\bigr)$.

**Definición 4.10 (Números coprimos):**
Dos enteros $a$ y $b$ son **coprimos** (o primos relativos) si $\gcd(a,b) = 1$.

**Ejemplo 4.6:**
- $\gcd(12, 18) = 6$ pues $D(12) \cap D(18) = \{1, 2, 3, 6\}$.
- $\gcd(7, 11) = 1$, por lo que $7$ y $11$ son coprimos.
- $\gcd(0, 5) = 5$ porque todo entero positivo divide a $0$.

**Teorema 4.2 (Algoritmo de Euclides):**
Sean $a, b \in \mathbb{Z}$ con $b > 0$. Si $a = bq + r$ con $0 \leq r < b$, entonces
$$\gcd(a,b) = \gcd(b,r).$$

**Demostración:**
Sea $d = \gcd(a,b)$. Entonces $d \mid a$ y $d \mid b$, de modo que $d \mid (a - bq) = r$. Así $d$ es divisor común de $b$ y $r$, luego $d \leq \gcd(b,r)$.

Recíprocamente, sea $d' = \gcd(b,r)$. Entonces $d' \mid b$ y $d' \mid r$, por lo que $d' \mid (bq + r) = a$. Luego $d'$ es divisor común de $a$ y $b$, de donde $d' \leq \gcd(a,b)$.

De ambas desigualdades se concluye que $\gcd(a,b) = \gcd(b,r)$. $\blacksquare$

**Ejemplo 4.7 (Cálculo de $\gcd(48, 18)$):**
Aplicando divisiones sucesivas:
$$\begin{align}
48 &= 18 \cdot 2 + 12, \\
18 &= 12 \cdot 1 + 6, \\
12 &= 6 \cdot 2 + 0.
\end{align}$$
El último resto no nulo es $6$, por lo que $\gcd(48, 18) = 6$.

**Definición 4.11 (Mínimo común múltiplo):**
Dados $a, b \in \mathbb{Z} \setminus \{0\}$, el **mínimo común múltiplo** de $a$ y $b$ es
$$\operatorname{lcm}(a,b) = \min\{ m \in \mathbb{N}^* : a \mid m \text{ y } b \mid m \}.$$

**Teorema 4.3 (Relación entre MCD y MCM):**
Para cualesquiera $a, b \in \mathbb{Z}^+$ se cumple
$$\gcd(a,b) \cdot \operatorname{lcm}(a,b) = a \cdot b.$$

**Demostración:**
Sea $d = \gcd(a,b)$. Entonces $a = d a_1$ y $b = d b_1$ con $\gcd(a_1, b_1) = 1$. Sea $m = d a_1 b_1$. Se verifica que $a \mid m$ y $b \mid m$, así que $\operatorname{lcm}(a,b) \leq m$.

Recíprocamente, sea $M$ un múltiplo común positivo de $a$ y $b$. Entonces $M = a k = b \ell$ para algunos $k, \ell \in \mathbb{Z}^+$. Sustituyendo,
$$d a_1 k = d b_1 \ell \quad \Longrightarrow \quad a_1 k = b_1 \ell.$$
Como $\gcd(a_1, b_1) = 1$, se tiene $a_1 \mid \ell$, luego $\ell = a_1 t$ para algún $t \in \mathbb{Z}^+$. Por tanto
$$M = b \ell = d b_1 a_1 t = m \cdot t \geq m.$$
Así, $m$ es el menor múltiplo común positivo, es decir, $\operatorname{lcm}(a,b) = d a_1 b_1$. Finalmente,
$$\gcd(a,b) \cdot \operatorname{lcm}(a,b) = d \cdot (d a_1 b_1) = (d a_1)(d b_1) = a \cdot b. \quad \blacksquare$$

**Ejemplo 4.8:**
Como $\gcd(48, 18) = 6$, se tiene
$$\operatorname{lcm}(48, 18) = \frac{48 \cdot 18}{6} = 144.$$
En efecto, $144 = 48 \cdot 3 = 18 \cdot 8$.

> **Observación:** Para calcular el mínimo común múltiplo de más de dos enteros se aplica la propiedad asociativa: $\operatorname{lcm}(a,b,c) = \operatorname{lcm}(\operatorname{lcm}(a,b),c)$, y análogamente para el máximo común divisor.

### 4.8 Valor absoluto

El valor absoluto mide la distancia de un entero al origen, independientemente de su signo. Es una herramienta central para definir distancia y convergencia.

**Definición 4.12 (Valor absoluto):**
El **valor absoluto** de $a \in \mathbb{Z}$ se define como
$$|a| = \begin{cases}
a & \text{si } a \geq 0, \\
-a & \text{si } a < 0.
\end{cases}$$

**Ejemplo 4.9:**
$|5| = 5$, $|-5| = 5$, $|0| = 0$ y $|-12| = 12$.

**Proposición 4.4 (Propiedades del valor absoluto):**
Para cualesquiera $a, b \in \mathbb{Z}$ se cumple:
1. $|a| \geq 0$, y $|a| = 0 \Longleftrightarrow a = 0$.
2. $|-a| = |a|$.
3. $|a \cdot b| = |a| \cdot |b|$.
4. $|a + b| \leq |a| + |b|$ (desigualdad triangular).

> **Nota:** Las tres primeras propiedades se verifican directamente separando los casos $a \geq 0$ y $a < 0$ en la definición de valor absoluto.

**Demostración (desigualdad triangular):
Se analizan los signos de $a$ y $b$. Si ambos tienen el mismo signo o alguno es cero, entonces $|a+b| = |a| + |b|$. Si tienen signos opuestos, la suma se cancela parcialmente y $|a+b| < |a| + |b|$. En todos los casos se cumple $|a+b| \leq |a| + |b|$. $\blacksquare$

### 4.9 De enteros a fracciones

Los enteros permiten contar objetos enteros, pero no expresar partes de un todo. Una **fracción** es la representación natural de una cantidad que resulta de dividir una unidad en partes iguales.

**Definición 4.13 (Fracción):**
Una **fracción** es una expresión de la forma
$$\frac{a}{b},$$
donde $a \in \mathbb{Z}$ es el **numerador**, $b \in \mathbb{Z} \setminus \{0\}$ es el **denominador**, y $b$ indica en cuántas partes iguales se divide la unidad.

**Definición 4.14 (Fracciones equivalentes):**
Dos fracciones $\frac{a}{b}$ y $\frac{c}{d}$ son **equivalentes** si
$$\frac{a}{b} = \frac{c}{d} \quad \Longleftrightarrow \quad a \cdot d = b \cdot c.$$
Equivalentemente, $\frac{a}{b} = \frac{a \cdot k}{b \cdot k}$ para todo $k \in \mathbb{Z} \setminus \{0\}$.

**Definición 4.15 (Fracción irreducible):**
Una fracción $\frac{a}{b}$ está en **forma irreducible** si $\gcd(a,b) = 1$.

**Ejemplo 4.10:**
La fracción $\frac{48}{60}$ se simplifica dividiendo numerador y denominador por $\gcd(48, 60) = 12$:
$$\frac{48}{60} = \frac{48 \div 12}{60 \div 12} = \frac{4}{5}.$$
Como $\gcd(4,5) = 1$, la fracción $\frac{4}{5}$ es irreducible.

> **Nota:** El estudio completo de las fracciones —suma, resta, multiplicación, división, comparación y representación decimal— se desarrolla en la Sección 5, dedicada a los números racionales $\mathbb{Q}$.

---

## 5. Los números racionales: $\mathbb{Q}$

### 5.1 Motivación: El problema de la división

**Definición 5.1 (División):**
Decimos que $a$ es divisible por $b$ (con $b \neq 0$) si:
$$\exists c \in \mathbb{Z} : a = b \cdot c$$
Y escribimos $c = a \div b$ o $c = \frac{a}{b}$.

por ejemplo
$$12=3\cdot4 \Rightarrow 12\div4=3$$

**El problema:** La ecuación $2 \cdot x = 3$ **no tiene solución** en $\mathbb{Z}$, porque $\frac{3}{2} \notin \mathbb{Z}$.

**Problema general:** La división no siempre está definida en $\mathbb{Z}$:
$$\frac{a}{b} \in \mathbb{Z} \quad \text{solo si } b \mid a \quad \text{($b$ divide a $a$)}$$

Para resolver este problema, **ampliamos** $\mathbb{Z}$ a $\mathbb{Q}$.
### 5.2 Definición y propiedades

**Definición 5.2 (Números racionales):**
$$\mathbb{Q} = \left\{\frac{p}{q} : p,q \in \mathbb{Z}, q \neq 0\right\}$$
El símbolo $\mathbb{Q}$ proviene del inglés *quotient* (cociente).

> **Interpretación:** Un número racional es una **fracción** $\frac{p}{q}$ donde $p$ es un entero (numerador) y $q$ es un natural (denominador).
> Cuando tenemos el caso donde $\gcd(p,q)=1$ decimos que el numero ${p}/{q}$ es una fracción irreducible.

Si tenemos la fracción ${p'}/{q'}$ y además $\gcd(p',q')=k$ podemos reducir esta fracción a otra fracción irreducible de la siguiente manera:
$$\frac{p'}{q'} \cdot 1 = \frac{p'}{q'} \cdot \frac{k}{k}=\frac{p}{q} \quad \text{con} \quad p = \frac{p'}{k} ,\quad q=\frac{q'}{k}$$
Decimos que $p/q$ es la forma canónica o irreducible de $p'/q'$

expresada en **forma irreducible** (simplificada).

**Ejemplos:**
- $\frac{1}{2}, \frac{-3}{4}, \frac{7}{5}, \frac{0}{1} = 0, \frac{5}{1} = 5$
- $\frac{2}{4}$ no está en forma estándar; se simplifica a $\frac{1}{2}$

**Propiedad fundamental:** En $\mathbb{Q}$, la división **siempre** está definida (excepto por cero):
$$\forall a \in \mathbb{Q}, \forall b \in \mathbb{Q} \setminus \{0\}, \quad \exists! \, c \in \mathbb{Q} : a \div b = c$$

### 5.3 Representación decimal de números racionales

Todo número racional puede expresarse como una **expansión decimal** mediante la división del numerador entre el denominador. Existen tres tipos de representaciones:

#### 5.3.1 Decimal exacto (o finito)

**Definición 5.3 (Decimal exacto):**
Un número racional tiene **representación decimal exacta** si al dividir el numerador entre el denominador, el proceso termina (resto cero) después de un número finito de dígitos.

**Caracterización:** Un número racional $\frac{p}{q}$ (en forma irreducible) tiene representación decimal exacta **si y solo si** el denominador $q$ tiene únicamente factores primos 2 y/o 5.

**Formalmente:** $\frac{p}{q}$ es decimal exacto $\Leftrightarrow q = 2^a \cdot 5^b$ para algunos $a, b \in \mathbb{N}_0$

**Ejemplos 5.1:**
- $\frac{1}{2} = 0.5$ (denominador: $2^1$)
- $\frac{3}{4} = 0.75$ (denominador: $2^2 = 4$)
- $\frac{7}{8} = 0.875$ (denominador: $2^3 = 8$)
- $\frac{13}{20} = 0.65$ (denominador: $2^2 \cdot 5 = 20$)
- $\frac{3}{5} = 0.6$ (denominador: $5^1$)
- $\frac{17}{25} = 0.68$ (denominador: $5^2 = 25$)
- $\frac{23}{40} = 0.575$ (denominador: $2^3 \cdot 5 = 40$)

#### 5.3.2 Decimal periódico puro

**Definición 5.4 (Decimal periódico puro):**
Un número racional tiene **representación decimal periódica pura** si, después del punto decimal, existe un bloque de dígitos que se repite indefinidamente, **sin ningún dígito no periódico** antes del período.

**Notación:** La parte que se repite (período) se indica con una barra superior:
$$\frac{1}{3} = 0.\overline{3} = 0.333...$$
$$\frac{2}{11} = 0.\overline{18} = 0.181818...$$

**Caracterización:** Un número racional $\frac{p}{q}$ (en forma irreducible) es periódico puro **si y solo si** el denominador $q$ **no contiene** los factores primos 2 ni 5.

**Formalmente:** $\frac{p}{q}$ es periódico puro $\Leftrightarrow \gcd(q, 10) = 1$

**Ejemplos 5.2:**
- $\frac{1}{3} = 0.\overline{3}$ (período: 3)
- $\frac{2}{3} = 0.\overline{6}$ (período: 6)
- $\frac{1}{9} = 0.\overline{1}$ (período: 1)
- $\frac{5}{9} = 0.\overline{5}$ (período: 5)
- $\frac{2}{11} = 0.\overline{18}$ (período: 18)
- $\frac{1}{7} = 0.\overline{142857}$ (período: 142857, longitud 6)
- $\frac{5}{11} = 0.\overline{45}$ (período: 45)
- $\frac{4}{9} = 0.\overline{4}$ (período: 4)

> **Observación:** La longitud del período puede variar. Por ejemplo, $\frac{1}{7}$ tiene período de longitud 6, mientras que $\frac{1}{3}$ tiene período de longitud 1.

#### 5.3.3 Decimal semiperiódico (o periódico mixto)

**Definición 5.5 (Decimal semiperiódico):**
Un número racional tiene **representación decimal semiperiódica** (o **periódica mixta**) si tiene una parte no periódica (antiperíodo) seguida de una parte periódica.

**Notación:** Se indica la parte no periódica seguida de la parte periódica con barra:
$$\frac{5}{6} = 0.8\overline{3} = 0.8333...$$
$$\frac{7}{12} = 0.58\overline{3} = 0.58333...$$

**Caracterización:** Un número racional $\frac{p}{q}$ (en forma irreducible) es semiperiódico **si y solo si** el denominador $q$ contiene factores primos 2 y/o 5, **y además** otros factores primos distintos.

**Formalmente:** $\frac{p}{q}$ es semiperiódico $\Leftrightarrow 1 < \gcd(q, 10) < q$

**Ejemplos 5.3:**
- $\frac{1}{6} = 0.1\overline{6}$ (antiperíodo: 1, período: 6) — denominador: $2 \cdot 3 = 6$
- $\frac{5}{6} = 0.8\overline{3}$ (antiperíodo: 8, período: 3) — denominador: $2 \cdot 3 = 6$
- $\frac{7}{12} = 0.58\overline{3}$ (antiperíodo: 58, período: 3) — denominador: $2^2 \cdot 3 = 12$
- $\frac{11}{30} = 0.3\overline{6}$ (antiperíodo: 3, período: 6) — denominador: $2 \cdot 3 \cdot 5 = 30$
- $\frac{13}{60} = 0.21\overline{6}$ (antiperíodo: 21, período: 6) — denominador: $2^2 \cdot 3 \cdot 5 = 60$

> **Observación:** La longitud del antiperíodo está determinada por las potencias de 2 y 5 en el denominador.
#### 5.3.4 Teorema de caracterización

**Teorema 5.1 (Caracterización decimal de racionales):**
Un número real tiene expansión decimal **exacta, periódica pura o semiperiódica** si y solo si es un **número racional**.

**Demostración:**

*($\Rightarrow$) Toda expansión decimal exacta, periódica pura o semiperiódica es un número racional.*

Sea $x$ un número real con una de estas expansiones. Separamos la parte entera, que es un entero, y analizamos la parte fraccionaria.

1. **Decimal exacta:** Si la parte decimal termina después de $m$ cifras, digamos $0.a_1 a_2 \dots a_m$, entonces:
$$x = N + \frac{A}{10^m},$$
donde $N$ es la parte entera y $A = a_1 a_2 \dots a_m$ es el entero formado por las cifras decimales. Como $N$ y $A$ son enteros, $x$ es racional.

2. **Decimal periódico puro:** Si $x = N + 0.\overline{b_1 b_2 \dots b_k}$, sea $B$ el entero formado por el período $b_1 b_2 \dots b_k$. Multiplicando por $10^k$ se obtiene:
$$10^k(x - N) = B + 0.\overline{b_1 b_2 \dots b_k} = B + (x - N).$$
Por tanto $(10^k - 1)(x - N) = B$, de donde:
$$x = N + \frac{B}{10^k - 1},$$
que es racional.

3. **Decimal semiperiódico:** Si $x = N.a_1 a_2 \dots a_m \overline{b_1 b_2 \dots b_k}$, multiplicamos por $10^m$ para dejar el período justo después del punto decimal:
$$10^m(x - N) = A + 0.\overline{b_1 b_2 \dots b_k},$$
donde $A$ es el entero formado por $a_1 a_2 \dots a_m$. La parte periódica es racional por el caso anterior, luego $x$ es racional.

*($\Leftarrow$) Todo número racional tiene expansión decimal exacta, periódica pura o semiperiódica.*

Sea $x = \dfrac{p}{q}$ con $p \in \mathbb{Z}$, $q \in \mathbb{Z}^+$ y la fracción reducida. Al efectuar la división de $p$ entre $q$, en cada paso se obtiene un resto $r_i$ que cumple $0 \leq r_i < q$. Como solo existen $q$ restos posibles, después de a lo más $q$ pasos algún resto debe repetirse (principio del palomar). Una vez que un resto se repite, el proceso de división reproduce las mismas cifras, por lo que la expansión decimal se vuelve periódica a partir de ese momento.

Más aún, escribiendo $q = 2^a \cdot 5^b \cdot q'$ con $\gcd(q', 10) = 1$:
- si $q' = 1$, el decimal es exacto;
- si $a = b = 0$, el decimal es periódico puro;
- en cualquier otro caso, el decimal es semiperiódico.

En todos los casos la expansión decimal es de uno de los tres tipos permitidos. $\blacksquare$

**Corolario:** Los números con expansión decimal **infinita no periódica** son **irracionales** (como $\pi$, $e$, $\sqrt{2}$).
#### 5.3.5 Conversión de decimal periódico a fracción

**Método general:** Para convertir un decimal periódico o semiperiódico a fracción:

**Ejemplo 5.4 (Periódico puro):**
Convertir $0.\overline{36}$ a fracción:

Sea $x = 0.\overline{36} = 0.363636...$

Multiplicamos por $10^2 = 100$ (potencia igual a la longitud del período):
$$100x = 36.363636...$$

Restamos:
$$100x - x = 36.363636... - 0.363636...$$
$$99x = 36$$
$$x = \frac{36}{99} = \frac{4}{11}$$

**Ejemplo 5.5 (Semiperiódico):**
Convertir $0.58\overline{3}$ a fracción:

Sea $x = 0.58\overline{3} = 0.58333...$

Multiplicamos por $10^1 = 10$ (potencia igual a la longitud del antiperíodo):
$$10x = 5.8333...$$

Multiplicamos por $10^2 = 100$ (potencia igual a longitud antiperíodo + período):
$$100x = 58.333...$$

Restamos:
$$100x - 10x = 58.333... - 5.833...$$
$$90x = 52.5$$
$$x = \frac{52.5}{90} = \frac{525}{900} = \frac{7}{12}$$

**Fórmula directa para decimales periódicos:**

Para $0.\overline{a_1a_2...a_n}$ (periódico puro con período de longitud $n$):
$$0.\overline{a_1a_2...a_n} = \frac{a_1a_2...a_n}{\underbrace{99...9}_{n \text{ nueves}}}$$

Para $0.b_1b_2...\overline{a_1a_2...a_n}$ (semiperiódico):
$$0.b_1b_2...\overline{a_1a_2...a_n} = \frac{b_1b_2...a_1a_2...a_n - b_1b_2...}{\underbrace{99...9}_{n \text{ nueves}}\underbrace{00...0}_{m \text{ ceros}}}$$
donde $m$ es la longitud del antiperíodo.

**Ejemplos usando fórmulas:**
- $0.\overline{7} = \frac{7}{9}$
- $0.\overline{15} = \frac{15}{99} = \frac{5}{33}$
- $0.2\overline{4} = \frac{24-2}{90} = \frac{22}{90} = \frac{11}{45}$

### 5.4 Densidad de los racionales

**Teorema 5.2 (Densidad de $\mathbb{Q}$):**
Entre cualesquiera dos números racionales distintos, existe otro número racional:
$$\forall a, b \in \mathbb{Q}, \, a < b \quad \Rightarrow \quad \exists r \in \mathbb{Q} : a < r < b$$

**Demostración:** Basta tomar $r = \frac{a+b}{2}$ (el promedio).

**Consecuencia:** Entre dos racionales hay **infinitos** racionales. Esto contrasta radicalmente con los naturales o enteros.

**Visualización en la recta:**
```
  ●  ●●  ●  ●●●  ●  ●●  ●●●  ●  ●●  ●●●●  ●  ●●  ●●●  ●  ●●  ●  
  ← -------------------------------------------------------  →
          -1              0              1              2
```

Los racionales son **densos**: aparentemente "llenan" la recta. Pero, sorprendentemente, aún dejan "huecos" (ver siguiente sección).

---

## 6. Los números irracionales y reales

### 6.1 Otras operaciones: Potencias, raíces y logaritmos

Antes de continuar, definimos operaciones adicionales:

**Definición 6.1 (Potenciación):**
$$a^n = \underbrace{a \cdot a \cdot ... \cdot a}_{n \text{ veces}}, \quad n \in \mathbb{N}$$
Con las extensiones:
- $a^0 = 1$ para $a \neq 0$
- $a^{-n} = \frac{1}{a^n}$ para $a \neq 0$
- $a^{m/n} = \sqrt[n]{a^m} = (\sqrt[n]{a})^m$ para $a > 0$

**Propiedades de la potenciación:**

Para cualesquiera $a, b > 0$ y $m, n \in \mathbb{R}$:

1. **Producto de potencias de igual base:** $a^m \cdot a^n = a^{m+n}$
2. **Cociente de potencias de igual base:** $\frac{a^m}{a^n} = a^{m-n}$
3. **Potencia de una potencia:** $(a^m)^n = a^{m \cdot n}$
4. **Potencia de un producto:** $(a \cdot b)^n = a^n \cdot b^n$
5. **Potencia de un cociente:** $\left(\frac{a}{b}\right)^n = \frac{a^n}{b^n}$
6. **Identidad:** $a^1 = a$

**Ejemplos:**
- $2^3 \cdot 2^4 = 2^{3+4} = 2^7 = 128$
- $\frac{5^6}{5^2} = 5^{6-2} = 5^4 = 625$
- $(3^2)^3 = 3^{2 \cdot 3} = 3^6 = 729$
- $(2 \cdot 3)^2 = 2^2 \cdot 3^2 = 4 \cdot 9 = 36$

**Definición 6.2 (Raíz n-ésima):**
La **raíz n-ésima** de $a$ (con $n \in \mathbb{N}$, $n \geq 2$) es el número $x$ tal que:
$$x^n = a$$
Se denota $x = \sqrt[n]{a}$ o $x = a^{1/n}$.

**Casos particulares:**
- $n = 2$: **raíz cuadrada** $\sqrt{a} = \sqrt[2]{a}$
- $n = 3$: **raíz cúbica** $\sqrt[3]{a}$

> **Observaciones importantes:**
>
> 1. Para $n$ **par** y $a \geq 0$: existe una única raíz **no negativa** (raíz principal)
>    - $\sqrt{16} = 4$ (tomamos la raíz positiva)
>    - $\sqrt{9} = 3$
>
> 2. Para $n$ **impar**: existe una única raíz real para todo $a \in \mathbb{R}$
>    - $\sqrt[3]{-8} = -2$ (las raíces impares pueden ser negativas)
>    - $\sqrt[3]{27} = 3$
>
> 3. Para $n$ par y $a < 0$: **no existe raíz real** (se necesitan números complejos)
>    - $\sqrt{-4} \notin \mathbb{R}$ (no existe raíz cuadrada real de un número negativo)

**Propiedades de las raíces:**

Para $a, b \geq 0$ y $m, n \in \mathbb{N}$ con $n, m \geq 2$:

1. **Producto de raíces:** $\sqrt[n]{a} \cdot \sqrt[n]{b} = \sqrt[n]{a \cdot b}$
2. **Cociente de raíces:** $\frac{\sqrt[n]{a}}{\sqrt[n]{b}} = \sqrt[n]{\frac{a}{b}}$ (con $b \neq 0$)
3. **Raíz de una raíz:** $\sqrt[m]{\sqrt[n]{a}} = \sqrt[m \cdot n]{a}$
4. **Raíz de una potencia:** $\sqrt[n]{a^m} = (\sqrt[n]{a})^m = a^{m/n}$
5. **Identidad:** $\sqrt[n]{a^n} = a$ (para $a \geq 0$ cuando $n$ es par)

**Ejemplos:**
- $\sqrt{4} \cdot \sqrt{9} = \sqrt{4 \cdot 9} = \sqrt{36} = 6$
- $\frac{\sqrt{50}}{\sqrt{2}} = \sqrt{\frac{50}{2}} = \sqrt{25} = 5$
- $\sqrt{\sqrt{16}} = \sqrt[4]{16} = 2$
- $\sqrt[3]{8^2} = (\sqrt[3]{8})^2 = 2^2 = 4$

**Definición 6.3 (Logaritmo):**
El **logaritmo en base $b$** de $a$ (con $b > 0$, $b \neq 1$, $a > 0$) es el número $x$ tal que:
$$x = \log_b(a) \iff b^x = a$$
Se denota $x = \log_b(a)$ a la operación de logaritmo.

> **Interpretación:** El logaritmo responde a la pregunta: "¿A qué potencia debo elevar $b$ para obtener $a$?"

**Bases especiales y notación:**

1. **Logaritmo decimal (base 10):**
   $$\log_{10}(a) = \log(a)$$
   Cuando no se indica la base, se asume base 10. Usado en ciencias e ingeniería.

2. **Logaritmo natural (base $e$):**
   $$\log_e(a) = \ln(a)$$
   Donde $e = 2.71828...$ (número de Euler). Es el logaritmo más importante en matemáticas y cálculo.

3. **Logaritmo binario (base 2):**
   $$\log_2(a)$$
   Usado en ciencias de la computación e informática.

**Ejemplos básicos:**
- $\log_{10}(100) = \log(100) = 2$ porque $10^2 = 100$
- $\log_{10}(1000) = 3$ porque $10^3 = 1000$
- $\log_2(8) = 3$ porque $2^3 = 8$
- $\log_2(16) = 4$ porque $2^4 = 16$
- $\ln(e) = 1$ porque $e^1 = e$
- $\ln(e^3) = 3$ porque $e^3 = e^3$
- $\ln(1) = 0$ porque $e^0 = 1$
- $\log(1) = 0$ porque $10^0 = 1$

**Propiedades fundamentales de los logaritmos:**

Para cualesquiera $a, b > 0$ y $c \in \mathbb{R}$ (en cualquier base):

1. **Logaritmo de un producto:** $\log_b(a \cdot c) = \log_b(a) + \log_b(c)$   
2. **Logaritmo de un cociente:** $\log_b\left(\frac{a}{c}\right) = \log_b(a) - \log_b(c)$   
3. **Logaritmo de una potencia:** $\log_b(a^c) = c \cdot \log_b(a)$   
4. **Identidad:** $\log_b(b) = 1$ y $\log_b(1) = 0$   
5. **Cambio de base:** $\log_b(a) = \frac{\log_c(a)}{\log_c(b)}$ (para cualquier base $c > 0$, $c \neq 1$)   
6. **Inversa de la exponencial:** $b^{\log_b(a)} = a$ y $\log_b(b^a) = a$

**Casos particulares importantes:**
$$\log_b(a) = \frac{\ln(a)}{\ln(b)} = \frac{\log(a)}{\log(b)}$$

Esta fórmula permite convertir logaritmos de una base a otra.

**Ejemplos de aplicación de propiedades:**

- $\log(100 \cdot 10) = \log(100) + \log(10) = 2 + 1 = 3$
- $\log\left(\frac{1000}{10}\right) = \log(1000) - \log(10) = 3 - 1 = 2$
- $\log(10^5) = 5 \cdot \log(10) = 5 \cdot 1 = 5$
- $\ln(e^7) = 7 \cdot \ln(e) = 7 \cdot 1 = 7$
- $\log_2(32) = \log_2(2^5) = 5$

**Cambio de base (ejemplo):**
$$\log_2(10) = \frac{\log_{10}(10)}{\log_{10}(2)} = \frac{1}{\log_{10}(2)} \approx \frac{1}{0.301} \approx 3.32$$

O usando logaritmo natural:
$$\log_2(10) = \frac{\ln(10)}{\ln(2)} \approx \frac{2.303}{0.693} \approx 3.32$$

**Relación entre las tres operaciones:**

Las operaciones de potenciación, radicación y logaritmos están íntimamente relacionadas:

$$a^n = b \quad \Leftrightarrow \quad a = \sqrt[n]{b} \quad \Leftrightarrow \quad n = \log_a(b)$$

**Aplicaciones:**
- **Potencias**: crecimiento exponencial, interés compuesto, desintegración radiactiva
- **Raíces**: ecuaciones algebraicas, geometría (cálculo de lados)
- **Logaritmos**: escalas (pH, decibeles, Richter), cálculo de tiempos de duplicación, complejidad algorítmica

### 6.2 El problema con la raíz: Números irracionales

**Problema fundamental:** La ecuación $x^2 = 2$ **no tiene solución** en $\mathbb{Q}$.

**Teorema 6.1 ($\sqrt{2}$ es irracional):**
No existe ningún número racional $r \in \mathbb{Q}$ tal que $r^2 = 2$.

**Demostración (por contradicción):**
Supongamos que existe $r = \frac{p}{q} \in \mathbb{Q}$ con $\gcd(p,q) = 1$ tal que $r^2 = 2$.

Entonces:
$$\left(\frac{p}{q}\right)^2 = 2 \quad \Rightarrow \quad p^2 = 2q^2$$

Esto implica que $p^2$ es par, luego $p$ es par (si $p$ fuera impar, $p^2$ sería impar). Escribamos $p = 2k$ para algún $k \in \mathbb{Z}$.

Sustituyendo:
$$(2k)^2 = 2q^2 \quad \Rightarrow \quad 4k^2 = 2q^2 \quad \Rightarrow \quad 2k^2 = q^2$$

Luego $q^2$ es par, por lo tanto $q$ es par.

Pero si $p$ y $q$ son ambos pares, entonces $\gcd(p,q) \geq 2$, lo cual **contradice** nuestra suposición de que $\gcd(p,q) = 1$.

Por lo tanto, $\sqrt{2} \notin \mathbb{Q}$. $\square$

**Definición 6.4 (Números irracionales):**
$$\mathbb{I} = \{x \in \mathbb{R} : x \notin \mathbb{Q}\}$$

**Nota**: esta definición requiere del conjunto de los números reales que serán definidos en la siguiente sección. La definición formal del conjunto de los números irracionales $\mathbb{I}$ como la de los números reales $\mathbb{R}$ son bastante complejas y se verán con mayor profundidad en el curso de **Análisis Real**

Otra definición es **Por oposición a ℚ** :
$$\mathbb{I} = \{x : x \quad es\quad una\quad expresión\quad decimal\quad infinita\quad no\quad periódica\}$$
o también
$$\mathbb{I} = \{x : x \quad \text{todo número que no se puede expresar de la forma:} \quad P/Q \}$$
Es decir, los números irracionales son aquellos que **no pueden expresarse como fracción** de dos enteros. 
Ambas definiciones son un tanto vagas, pero para definir correctamente a los números irracionales necesitaremos herramientas mas avanzadas, por lo cual quedara para un curso de Análisis Real la definición totalmente formal

**Ejemplos de irracionales:**
- $\sqrt{2}, \sqrt{3}, \sqrt{5}, ..., \sqrt{n}$ (para $n$ no cuadrado perfecto)
- $\pi = 3.14159...$
- $e = 2.71828...$
- $\phi = \frac{1+\sqrt{5}}{2} = 1.618...$ (razón áurea)

### 6.3 Los números reales: $\mathbb{R}$

**Definición intuitiva 6.5:**
Los **números reales** $\mathbb{R}$ son la unión de los racionales y los irracionales:
$$\mathbb{R} = \mathbb{Q} \cup \mathbb{I}$$

Geométricamente, $\mathbb{R}$ corresponde a **todos los puntos** de la recta numérica, sin dejar ningún "hueco".

> **Nota sobre la formalidad:**
> La construcción rigurosa de $\mathbb{R}$ es técnicamente compleja y se realiza mediante:
> 1. **Cortaduras de Dedekind** (Richard Dedekind, 1872)
> 2. **Sucesiones de Cauchy** (Georg Cantor, 1872)

Estas construcciones garantizan que $\mathbb{R}$ sea **completo**: toda sucesión de Cauchy converge a un elemento de $\mathbb{R}$. Los detalles se estudiarán en el curso de **Análisis Real**.

### 6.4 La recta real

```
  ← ━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━━  →
                      -π    -√2   -1    0    1   √2    e    π
```

**Características de $\mathbb{R}$:**
- Es **continuo**: no tiene "huecos"
- Es **denso en sí mismo**: entre dos reales distintos hay infinitos reales
- Es **completo**: toda sucesión convergente de reales tiene límite en $\mathbb{R}$
- Es **no numerable**: tiene cardinalidad $\mathfrak{c} = 2^{\aleph_0} > \aleph_0$ (ver Sección 8)

---

## 7. Conjuntos infinitos y cardinalidades infinitas [Opcional]

### 7.1 Concepto de infinito

**Definición intuitiva:** Un conjunto es **infinito** si no es finito, es decir, si no podemos asignarle un número natural como cardinalidad.

**Ejemplos de conjuntos infinitos:**
- $\mathbb{N} = \{0, 1, 2, 3, 4, ...\}$ (números naturales)
- $\mathbb{N}^{*} = \{1, 2, 3, 4, ...\}$ (números naturales sin el cero)
- $\mathbb{Z} = \{..., -2, -1, 0, 1, 2, ...\}$ (números enteros)
- $\mathbb{Q}$ (números racionales)
- $\mathbb{R}$ (números reales)

### 7.2 Cardinalidad numerable: $\aleph_0$ (Aleph cero)

**Definición 7.1 (Conjunto numerable):**
Un conjunto infinito $A$ es **numerable** (o **contable**) si existe una biyección entre $A$ y $\mathbb{N}$. En otras palabras, si podemos "listar" sus elementos en una secuencia:
$$A = \{a_1, a_2, a_3, ...\}$$
La **cardinalidad** de un conjunto numerable se denota $\aleph_0$ (aleph cero, primera letra del alfabeto hebreo).

> **Observación:** El concepto de **biyecciones** se estudiaría mas en profundidad en la [[Clase 9 - Funciones Parte 2]].

**Propiedad fundamental:** $|\mathbb{N}| = |\mathbb{Z}| = |\mathbb{Q}| = \aleph_0$

#### 7.2.1 El Hotel de Hilbert: El infinito materializado

El matemático alemán David Hilbert (1862-1943) propuso una paradoja que ilustra las propiedades contraintuitivas de los conjuntos infinitos:

**La paradoja del Hotel de Hilbert:**

Imaginemos un hotel con **infinitas habitaciones** numeradas: 1, 2, 3, 4, 5, ... hasta el infinito.

**Escenario 1: Llega un nuevo huésped, pero el hotel está lleno**

- **Situación:** Todas las infinitas habitaciones están ocupadas
- **Problema:** Llega un nuevo huésped y pide una habitación
- **Solución:** El recepcionista pide a cada huésped que se mueva a la habitación siguiente:
  - Huésped de habitación 1 → habitación 2
  - Huésped de habitación 2 → habitación 3
  - Huésped de habitación $n$ → habitación $n+1$
- **Resultado:** ¡La habitación 1 queda libre para el nuevo huésped!

> **Interpretación matemática:** Esto demuestra que $\aleph_0 + 1 = \aleph_0$

**Escenario 2: Llegan infinitos nuevos huéspedes**

- **Situación:** El hotel está lleno (infinitas habitaciones ocupadas)
- **Problema:** Llega un autobús con **infinitos** nuevos huéspedes
- **Solución:** El recepcionista pide a cada huésped actual que se mueva al **doble** de su número de habitación:
  - Huésped de habitación 1 → habitación 2
  - Huésped de habitación 2 → habitación 4
  - Huésped de habitación 3 → habitación 6
  - Huésped de habitación $n$ → habitación $2n$
- **Resultado:** ¡Todas las habitaciones **impares** quedan libres! (1, 3, 5, 7, ...)
- Los infinitos nuevos huéspedes ocupan las habitaciones 1, 3, 5, 7, ...

> **Interpretación matemática:** Esto demuestra que $\aleph_0 + \aleph_0 = \aleph_0$ y $2 \cdot \aleph_0 = \aleph_0$

**Escenario 3: Llegan infinitos autobuses con infinitos huéspedes cada uno**

- **Situación:** El hotel está lleno
- **Problema:** Llegan **infinitos** autobuses, cada uno con **infinitos** huéspedes
- **Solución:** Usar la enumeración de Cantor (ver subsección sobre $\mathbb{Q}$)
- **Resultado:** ¡Todos pueden ser acomodados!

> **Interpretación matemática:** Esto demuestra que $\aleph_0 \cdot \aleph_0 = \aleph_0$

#### 7.2.2 Paradojas del infinito: Aritmética de $\aleph_0$

El infinito no se comporta como los números finitos. Las siguientes ecuaciones son **verdaderas**:

1. **Suma con constante:** $\aleph_0 + 1 = \aleph_0$
   - Agregar un elemento a un conjunto infinito no cambia su cardinalidad
1. **Suma con finitos:** $\aleph_0 + n = \aleph_0$ para cualquier $n \in \mathbb{N}$
   - Agregar un número finito de elementos no cambia la cardinalidad
1. **Suma de infinitos:** $\aleph_0 + \aleph_0 = \aleph_0$
   - La unión de dos conjuntos numerables es numerable
1. **Producto por constante:** $2 \cdot \aleph_0 = \aleph_0$
   - "El doble del infinito es infinito"
1. **Producto de infinitos:** $\aleph_0 \cdot \aleph_0 = \aleph_0$
   - El producto cartesiano de dos conjuntos numerables es numerable
1. **Potencia finita:** $\aleph_0^n = \aleph_0$ para $n \in \mathbb{N}$ finito
   - $\mathbb{N}^2$, $\mathbb{N}^3$, etc., son numerables

> **Advertencia:** Estas propiedades **NO** se cumplen para operaciones como $2^{\aleph_0}$, que es **estrictamente mayor** que $\aleph_0$ (ver Teorema de Cantor sobre el conjunto potencia).

#### 7.2.3 Demostración: $|\mathbb{Z}| = |\mathbb{N}|$

Demostraremos que el conjunto de los enteros tiene la misma cardinalidad que los naturales construyendo una **biyección explícita**.

**Teorema 7.1:** $|\mathbb{Z}| = |\mathbb{N}| = \aleph_0$

**Demostración:**

Debemos construir una función $f: \mathbb{N} \to \mathbb{Z}$ que sea **biyectiva** (inyectiva y sobreyectiva).

**Idea:** Alternamos entre números positivos y negativos, "emparejando" cada entero con un natural único.

**Definición de la biyección:**
$$f(n) = \begin{cases}
0 & \text{si } n = 0 \\
\frac{n}{2} & \text{si } n > 0 \text{ y } n \text{ es par} \\
-\frac{n+1}{2} & \text{si } n > 0 \text{ y } n \text{ es impar}
\end{cases}$$

O de manera más compacta:
$$f(n) = \begin{cases}
\frac{n}{2} & \text{si } n \text{ es par} \\
-\frac{n+1}{2} & \text{si } n \text{ es impar}
\end{cases}$$

**Tabla de correspondencia:**

| $n$ (natural) | $f(n)$ (entero) | Visualización |
|:-------------:|:---------------:|:-------------:|
| 0 | 0 | $0 \leftrightarrow 0$ |
| 1 | -1 | $1 \leftrightarrow -1$ |
| 2 | 1 | $2 \leftrightarrow 1$ |
| 3 | -2 | $3 \leftrightarrow -2$ |
| 4 | 2 | $4 \leftrightarrow 2$ |
| 5 | -3 | $5 \leftrightarrow -3$ |
| 6 | 3 | $6 \leftrightarrow 3$ |
| 7 | -4 | $7 \leftrightarrow -4$ |
| 8 | 4 | $8 \leftrightarrow 4$ |
| ... | ... | ... |

**Representación en la recta:**
```
Naturales:     0   1   2   3   4   5   6   7   8   9  ...
               ↓   ↓   ↓   ↓   ↓   ↓   ↓   ↓   ↓   ↓
Enteros:       0  -1   1  -2   2  -3   3  -4   4  -5  ...
```

**Verificación:**

1. **Inyectividad:** Si $f(n_1) = f(n_2)$, entonces $n_1 = n_2$.
   - Números pares mapean a positivos, impares a negativos
   - Dentro de cada caso, la correspondencia es única

2. **Sobreyectividad:** Para cada $z \in \mathbb{Z}$, existe $n \in \mathbb{N}$ tal que $f(n) = z$.
   - Si $z = 0$, entonces $n = 0$
   - Si $z > 0$, entonces $n = 2z$ (par)
   - Si $z < 0$, entonces $n = -2z - 1$ (impar)

Por lo tanto, $f$ es biyectiva, y $|\mathbb{Z}| = |\mathbb{N}| = \aleph_0$. $\square$

> **Observación profunda:** Aunque $\mathbb{Z}$ parece "dos veces más grande" que $\mathbb{N}$ (tiene negativos y positivos), podemos **emparejar** perfectamente cada entero con un natural único. Esto es la esencia de la equipotencia: dos conjuntos tienen la misma cardinalidad si sus elementos pueden ponerse en correspondencia uno a uno.
#### 7.2.4 Los racionales son numerables: El método diagonal de Cantor

**Teorema 7.2:** $|\mathbb{Q}| = |\mathbb{N}| = \aleph_0$

**Demostración (Enumeración diagonal de Cantor):**

Georg Cantor demostró que los racionales positivos pueden "listarse" usando un método ingenioso.

**Paso 1:** Organizamos los racionales positivos en una **tabla infinita** donde:
- La fila $n$ tiene denominador $n$
- La columna $m$ tiene numerador $m$

```
      1      2      3      4      5      6     ...
    ┌────────────────────────────────────────────
 1  │ 1/1    2/1    3/1    4/1    5/1    6/1   ...
    │
 2  │ 1/2    2/2    3/2    4/2    5/2    6/2   ...
    │
 3  │ 1/3    2/3    3/3    4/3    5/3    6/3   ...
    │
 4  │ 1/4    2/4    3/4    4/4    5/4    6/4   ...
    │
 5  │ 1/5    2/5    3/5    4/5    5/5    6/5   ...
    │
...  ...    ...    ...    ...    ...    ...
```

> **Observación:** Cada racional positivo $\frac{p}{q}$ aparece en la posición (fila $q$, columna $p$).

**Paso 2:** Recorremos la tabla en **diagonal**, siguiendo este patrón en zigzag:

```
      1      2      3      4      5      6
    ┌────────────────────────────────────
 1  │ 1/1 →  2/1    3/1 →  4/1    5/1 → ...
    │  ↓      ↗      ↓      ↗      ↓
 2  │ 1/2    2/2 →  3/2    4/2 →  5/2  ...
    │  ↓      ↗      ↓      ↗
 3  │ 1/3    2/3    3/3 →  4/3    5/3  ...
    │  ↓      ↗      ↓
 4  │ 1/4    2/4    3/4    4/4    5/4  ...
    │  ↓      ↗
 5  │ 1/5    2/5    3/5    4/5    5/5  ...
```

**Paso 3:** Enumeración resultante (omitiendo repetidos como $\frac{2}{2} = \frac{1}{1}$):
$$\mathbb{Q}^+ = \left\{\frac{1}{1}, \frac{2}{1}, \frac{1}{2}, \frac{1}{3}, \frac{3}{1}, \frac{4}{1}, \frac{3}{2}, \frac{2}{3}, \frac{1}{4}, \frac{1}{5}, ...\right\}$$

**Paso 4:** Para incluir racionales negativos y cero, intercalamos:
$$\mathbb{Q} = \left\{0, \frac{1}{1}, -\frac{1}{1}, \frac{2}{1}, -\frac{2}{1}, \frac{1}{2}, -\frac{1}{2}, \frac{1}{3}, -\frac{1}{3}, ...\right\}$$

Por lo tanto, $\mathbb{Q}$ puede ser listado en una secuencia, lo que significa que $|\mathbb{Q}| = \aleph_0$. $\square$

> **Observación crucial:** Este método **diagonal** permite convertir una tabla bidimensional (infinita × infinita) en una lista unidimensional (secuencia). Es uno de los resultados más sorprendentes de Cantor: aunque hay "infinitos infinitos" de racionales, podemos contarlos uno por uno.

> **Nota histórica:** Cantor usó una técnica similar (el **argumento diagonal**) para demostrar lo contrario sobre $\mathbb{R}$: que los reales **no** son numerables (ver Sección 8.1). Ambos métodos diagonales son fundamentales en teoría de conjuntos.

---

## 8. Cardinalidades infinitas: $\aleph_0$ y $\aleph_1$ (Opcional)

### 8.1 Cardinalidad de los reales

**Teorema 8.1 (Teorema de Cantor, 1874):**
El conjunto $\mathbb{R}$ **no es numerable**: no existe ninguna biyección entre $\mathbb{N}$ y $\mathbb{R}$.

**Idea de la demostración (Argumento diagonal de Cantor):**
Supongamos que $\mathbb{R}$ es numerable. Entonces podemos listar todos los reales en $[0,1]$ como una secuencia infinita:
$$r_1 = 0.a_{11}a_{12}a_{13}...$$
$$r_2 = 0.a_{21}a_{22}a_{23}...$$
$$r_3 = 0.a_{31}a_{32}a_{33}...$$
$$...$$

Construimos un nuevo número $r = 0.b_1b_2b_3...$ donde cada dígito $b_i$ es diferente de $a_{ii}$ (el i-ésimo dígito de $r_i$). Por ejemplo, si $a_{ii} = 5$, tomamos $b_i = 6$.

Entonces $r$ es distinto de **todos** los números en la lista (difiere de $r_i$ en el i-ésimo dígito), lo cual contradice que la lista contenía todos los reales. $\square$

**Definición 8.1 (Cardinalidad del continuo):**
La cardinalidad de $\mathbb{R}$ se denota $\mathfrak{c}$ (letra gótica "c" de *continuo*) y se cumple $\mathfrak{c} = 2^{\aleph_0}$. La notación $\aleph_1$ se reserva para el siguiente cardinal infinito después de $\aleph_0$; la igualdad $\mathfrak{c} = \aleph_1$ es la **Hipótesis del Continuo**, independiente de ZFC.

**Jerarquía de infinitos:**
$$|\mathbb{N}| = \aleph_0 < |\mathbb{R}| = \mathfrak{c} = 2^{\aleph_0}$$

> **Observación profunda:** Existen "tamaños" de infinito. El infinito de los reales es **estrictamente mayor** que el infinito de los naturales. Cantor demostró que existe una jerarquía infinita de cardinalidades:
> $$\aleph_0 < \aleph_1 < \aleph_2 < \aleph_3 < ...$$

### 8.2 Paradojas de conjuntos infinitos

**Propiedad sorprendente:** Los conjuntos infinitos pueden tener la **misma cardinalidad** que algunos de sus subconjuntos propios. Por ejemplo:
$$|\mathbb{N}| = |\{2, 4, 6, 8, ...\}| = \aleph_0$$
(los números pares tienen "la misma cantidad" de elementos que todos los naturales)

De hecho:
$$|\mathbb{N}| = |\mathbb{Z}| = |\mathbb{Q}| = \aleph_0$$

Pero:
$$|\mathbb{R}| = \mathfrak{c} > \aleph_0$$

**Mención al problema del continuo:** La **Hipótesis del Continuo** de Cantor afirma que no existe ningún conjunto cuya cardinalidad esté **estrictamente entre** $\aleph_0$ y $2^{\aleph_0}$, o equivalentemente, que $\mathfrak{c} = \aleph_1$. Kurt Gödel (1940) y Paul Cohen (1963) demostraron que esta hipótesis es **independiente** de los axiomas de la teoría de conjuntos (ZFC): no se puede demostrar ni refutar dentro del sistema axiomático estándar.

### 8.3 Biyecciones sorprendentes

**Propiedad 8.1:** El intervalo $[0, 1]$ tiene la **misma cardinalidad** que toda la recta real $(-\infty, \infty)$.

**Demostración (construcción de biyección):**
Consideremos la función:
$$f: (0,1) \to \mathbb{R}, \quad f(x) = \tan\left(\pi\left(x - \frac{1}{2}\right)\right)$$

Esta función es una biyección (se puede verificar que es inyectiva y sobreyectiva). Por lo tanto:
$$|(0,1)| = |\mathbb{R}| = \mathfrak{c}$$

> **Interpretación:** En un segmento de longitud 1 hay "tantos puntos" como en toda la recta infinita. ¡El infinito tiene propiedades contraintuitivas!

**Propiedad 8.2:** El círculo unitario tiene la misma cardinalidad que la recta real.

**Idea:** Podemos proyectar estereográficamente el círculo sobre la recta, estableciendo una biyección.

---

## 9. Axiomas de los números reales

Los números reales no solo son un conjunto, sino una **estructura algebraica** con operaciones (suma y multiplicación) y una relación de orden ($\leq$). Estas propiedades se formalizan mediante **axiomas**.

**Contexto histórico:** Antes de estudiar los axiomas de $\mathbb{R}$, es importante reconocer que cada sistema numérico tiene sus propios axiomas fundacionales. Los **Axiomas de Peano** (formulados por Giuseppe Peano en 1889) son los axiomas que definen rigurosamente los números naturales $\mathbb{N}$, y son la base sobre la cual se construyen todos los demás sistemas numéricos.

**Los cinco Axiomas de Peano para $\mathbb{N}$:**

1. $0 \in \mathbb{N}$ (existe un primer número natural)
2. Todo número natural $n$ tiene un **sucesor** $S(n) \in \mathbb{N}$
3. $0$ no es sucesor de ningún número natural ($\forall n \in \mathbb{N}, \, S(n) \neq 0$)
4. La función sucesor es **inyectiva**: $S(n) = S(m) \Rightarrow n = m$
5. **Principio de inducción**: Si $P(0)$ es verdadero, y $P(n) \Rightarrow P(S(n))$ para todo $n$, entonces $P(n)$ es verdadero para todo $n \in \mathbb{N}$

**Jerarquía de construcción:**
```
Axiomas de Peano → ℕ (naturales)
      ↓
   ℕ → ℤ (enteros, como pares de naturales)
      ↓
   ℤ → ℚ (racionales, como cocientes de enteros)
      ↓
   ℚ → ℝ (reales, mediante completitud)
```

Cada sistema se construye formalmente a partir del anterior. Los axiomas que veremos a continuación caracterizan a $\mathbb{R}$ como un **cuerpo ordenado completo**.

### 9.1 Axiomas de cuerpo

**Definición 9.1 (Cuerpo):**
Un **cuerpo** es un conjunto $F$ con dos operaciones binarias $+$ (suma) y $\cdot$ (multiplicación) que satisfacen:

**Axiomas de la suma:**
1. **Cerradura**: $\forall a, b \in F, \quad a + b \in F$
2. **Asociatividad**: $\forall a, b, c \in F, \quad (a + b) + c = a + (b + c)$
3. **Elemento neutro**: $\exists \, 0 \in F : \forall a \in F, \quad a + 0 = a$
4. **Elemento inverso**: $\forall a \in F, \, \exists \, (-a) \in F : a + (-a) = 0$
5. **Conmutatividad**: $\forall a, b \in F, \quad a + b = b + a$

**Axiomas de la multiplicación:**
6. **Cerradura**: $\forall a, b \in F, \quad a \cdot b \in F$
7. **Asociatividad**: $\forall a, b, c \in F, \quad (a \cdot b) \cdot c = a \cdot (b \cdot c)$
8. **Elemento neutro**: $\exists \, 1 \in F : \forall a \in F, \quad a \cdot 1 = a$ (con $1 \neq 0$)
9. **Elemento inverso**: $\forall a \in F \setminus \{0\}, \, \exists \, a^{-1} \in F : a \cdot a^{-1} = 1$
10. **Conmutatividad**: $\forall a, b \in F, \quad a \cdot b = b \cdot a$

**Axioma distributivo:**
11. **Distributividad**: $\forall a, b, c \in F, \quad a \cdot (b + c) = (a \cdot b) + (a \cdot c)$

**Ejemplo:** $\mathbb{Q}$ y $\mathbb{R}$ son cuerpos. $\mathbb{Z}$ **no** es cuerpo (no todo entero no nulo tiene inverso multiplicativo en $\mathbb{Z}$).

### 9.2 Axiomas de orden

**Definición 9.2 (Cuerpo ordenado):**
Un cuerpo $F$ es **ordenado** si existe una relación $\leq$ que satisface:

**Axiomas del orden:**
12. **Tricotomía**: $\forall a, b \in F$, exactamente una de las siguientes es verdadera: $a < b$, $a = b$, o $a > b$
13. **Transitividad**: $\forall a, b, c \in F, \quad a \leq b \land b \leq c \Rightarrow a \leq c$
14. **Compatibilidad con la suma**: $\forall a, b, c \in F, \quad a \leq b \Rightarrow a + c \leq b + c$
15. **Compatibilidad con la multiplicación**: $\forall a, b, c \in F, \quad a \leq b \land c \geq 0 \Rightarrow a \cdot c \leq b \cdot c$

### 9.3 Axioma de completitud

El axioma que distingue $\mathbb{R}$ de $\mathbb{Q}$:

**Axioma 16 (Completitud o del supremo):**
Todo subconjunto no vacío de $\mathbb{R}$ que está **acotado superiormente** tiene un **supremo** (mínima cota superior) en $\mathbb{R}$.

> **Interpretación:** Este axioma garantiza que $\mathbb{R}$ "no tiene huecos". Es el axioma que falta en $\mathbb{Q}$ y que se necesita para hacer Cálculo (límites, continuidad, convergencia).

---

## 10. Demostraciones elementales con los axiomas

### 10.1 Demostración: $1 + 0 = 1$

**Proposición 10.1:** $\forall a \in \mathbb{R}, \quad a + 0 = a$

**Demostración:**
Por el **Axioma 3** (elemento neutro de la suma), sabemos que existe un elemento $0 \in \mathbb{R}$ tal que:
$$\forall a \in \mathbb{R}, \quad a + 0 = a$$

En particular, para $a = 1$:
$$1 + 0 = 1$$

Esto es **inmediato del axioma**. $\square$

> **Nota:** Esta es una aplicación directa del axioma, no requiere deducción adicional.

### 10.2 Demostración: $1 + 1 = 2$

**Proposición 10.2:** $1 + 1 = 2$

**Demostración:**
En la construcción de von Neumann (Sección 4), definimos:
$$2 := S(1) = 1 \cup \{1\}$$

En términos aritméticos, el **sucesor** de 1 es precisamente lo que llamamos 2. Y por la definición de suma en $\mathbb{N}$:
$$1 + 1 := S(1) = 2$$

Por lo tanto, $1 + 1 = 2$ por **definición**. $\square$

> **Observación filosófica:** Esta "demostración" puede parecer inmediata, pero formaliza precisamente qué significa "2". Bertrand Russell y Alfred North Whitehead dedicaron cientos de páginas en *Principia Mathematica* (1910-1913) para probar rigurosamente que $1 + 1 = 2$ desde los fundamentos de la lógica.

### 10.3 Demostración: Ley de cancelación de la suma

**Proposición 10.3 (Ley de cancelación):** Si $a + b = a + c$, entonces $b = c$.

**Demostración:**
Supongamos que $a + b = a + c$, donde $a, b, c \in \mathbb{R}$.

Por el **Axioma 4** (existencia del inverso aditivo), existe $(-a) \in \mathbb{R}$ tal que:
$$a + (-a) = 0$$

Sumamos $(-a)$ a ambos lados de la ecuación $a + b = a + c$:
$$(-a) + (a + b) = (-a) + (a + c)$$

Por el **Axioma 2** (asociatividad de la suma), podemos reagrupar:
$$\big((-a) + a\big) + b = \big((-a) + a\big) + c$$

Por el **Axioma 5** (conmutatividad de la suma), $(-a) + a = a + (-a) = 0$:
$$0 + b = 0 + c$$

Por el **Axioma 3** (elemento neutro de la suma), $0 + b = b$ y $0 + c = c$:
$$b = c$$

Por lo tanto, hemos demostrado que $a + b = a + c \Rightarrow b = c$. $\square$

**Importancia:** Esta propiedad nos permite "cancelar" términos iguales en ambos lados de una ecuación, una técnica fundamental en la resolución de ecuaciones algebraicas.

**Ejemplo de aplicación:**
Si $5 + x = 5 + 3$, entonces por la ley de cancelación, $x = 3$.

### 10.4 Demostración: $\sqrt{2} \in \mathbb{I}$

Ya demostramos en el **Teorema 6.1** que $\sqrt{2} \notin \mathbb{Q}$.

**Proposición 10.4:** $\sqrt{2} \in \mathbb{I}$

**Demostración:**
Por definición (Def. 6.4):
$$\mathbb{I} = \mathbb{R} \setminus \mathbb{Q}$$

Sabemos que:
1. Existe $x \in \mathbb{R}$ tal que $x^2 = 2$ (por el axioma de completitud de $\mathbb{R}$)
2. $x \notin \mathbb{Q}$ (por el Teorema 6.1)

Por lo tanto, $x = \sqrt{2} \in \mathbb{R} \setminus \mathbb{Q} = \mathbb{I}$. $\square$

## 11. Temas Varios de Números Reales

Además de las operaciones fundamentales de suma, multiplicación, resta, división y potenciación, existen otras operaciones y funciones importantes definidas sobre los números reales.

### 11.1 Función Sucesor y Antecesor

**Definición 11.1 (Función Sucesor):**
La función sucesor $S: \mathbb{R} \to \mathbb{R}$ se define como:
$$S(n) = n + 1$$

Esta función asigna a cada número su siguiente número sumándole la unidad. Es fundamental en la construcción axiomática de los números naturales (Axiomas de Peano).

**Ejemplos:**
- $S(5) = 6$
- $S(-3) = -2$
- $S(0) = 1$

**Definición 11.2 (Función Antecesor):**
La función antecesor $A: \mathbb{R} \to \mathbb{R}$ se define como:
$$A(n) = n - 1$$
Esta función asigna a cada número su antecesor restándole la unidad. Es la operación inversa del sucesor.

**Ejemplos:**
- $A(5) = 4$
- $A(0) = -1$
- $A(-3) = -4$

**Propiedad:**
Para todo $n \in \mathbb{R}$: $A(S(n)) = S(A(n)) = n$

### 11.2 Factorial

**Definición 11.3 (Factorial):**
El factorial de un número natural $n$, denotado $n!$, se define recursivamente como:
$$n! = \begin{cases}
1 & \text{si } n = 0 \\
n \cdot (n-1)! & \text{si } n \in \mathbb{N}
\end{cases}$$

Equivalentemente, de forma explícita:
$$n! = n \times (n-1) \times (n-2) \times \dots \times 2 \times 1$$

**Ejemplos:**
- $0! = 1$ (por definición)
- $1! = 1$
- $2! = 2 \times 1 = 2$
- $3! = 3 \times 2 \times 1 = 6$
- $4! = 4 \times 3 \times 2 \times 1 = 24$
- $5! = 5 \times 4 \times 3 \times 2 \times 1 = 120$
- $10! = 3,628,800$

**Propiedades:**
1. $n! = n \cdot (n-1)!$ (recursividad)
2. $\frac{n!}{(n-1)!} = n$
3. El factorial crece extremadamente rápido (más rápido que cualquier polinomio o exponencial simple)

**Aplicaciones:**
- Conteo de permutaciones: El número de formas de ordenar $n$ objetos distintos es $n!$
- Combinatoria y teoría de probabilidades
- Desarrollo en series de Taylor
- Coeficientes binomiales: $\binom{n}{k} = \frac{n!}{k!(n-k)!}$

> **Observación:**
> Aunque el factorial se define originalmente sobre los naturales, puede extenderse a los números reales positivos mediante la **función Gamma**: $\Gamma(n+1) = n!$ para $n \in \mathbb{N}_0$.

### 11.3 Números pares e impares

**Definición 11.4 (Número par):**
Un número entero $n$ es **par** si es divisible por $2$, es decir:
$$n \text{ es par} \quad \Leftrightarrow \quad \exists k \in \mathbb{Z}, \, n = 2k$$

**Equivalentemente:** $n$ es par si y solo si $2 \mid n$ (o $n \bmod 2 = 0$).

**Ejemplos de números pares:**
$$..., -6, -4, -2, 0, 2, 4, 6, 8, 10, ...$$

**Definición 11.5 (Número impar):**
Un número entero $n$ es **impar** si **no** es divisible por $2$, es decir:
$$n \text{ es impar} \quad \Leftrightarrow \quad \exists k \in \mathbb{Z}, \, n = 2k + 1$$

**Equivalentemente:** $n$ es impar si y solo si $2 \nmid n$ (o $n \bmod 2 = 1$).

**Ejemplos de números impares:**
$$..., -5, -3, -1, 1, 3, 5, 7, 9, 11, ...$$

**Proposición 11.1 (Partición de $\mathbb{Z}$):**
Todo número entero es **par o impar**, pero no ambos. Formalmente:
$$\mathbb{Z} = \{\text{pares}\} \cup \{\text{impares}\} \quad \text{y} \quad \{\text{pares}\} \cap \{\text{impares}\} = \emptyset$$

**Propiedades de paridad:**

1. **Suma de pares:** par + par = par
   - **Demostración:** Sean $n = 2a$ y $m = 2b$ con $a, b \in \mathbb{Z}$. Entonces $n + m = 2(a + b)$, que es de la forma $2k$ con $k \in \mathbb{Z}$. Por tanto, $n + m$ es par. $\square$

2. **Suma de impares:** impar + impar = par
   - **Demostración:** Sean $n = 2a + 1$ y $m = 2b + 1$ con $a, b \in \mathbb{Z}$. Entonces $n + m = 2(a + b + 1)$, que es de la forma $2k$ con $k \in \mathbb{Z}$. Por tanto, $n + m$ es par. $\square$

3. **Suma de par e impar:** par + impar = impar
   - **Demostración:** Sean $n = 2a$ par y $m = 2b + 1$ impar con $a, b \in \mathbb{Z}$. Entonces $n + m = 2(a + b) + 1$, que es de la forma $2k + 1$ con $k \in \mathbb{Z}$. Por tanto, $n + m$ es impar. $\square$

4. **Producto de pares:** par × par = par
   - **Demostración:** Sean $n = 2a$ y $m = 2b$ con $a, b \in \mathbb{Z}$. Entonces $n \cdot m = 2(2ab)$, que es de la forma $2k$ con $k \in \mathbb{Z}$. Por tanto, $n \cdot m$ es par. $\square$

5. **Producto de impares:** impar × impar = impar
   - **Demostración:** Sean $n = 2a + 1$ y $m = 2b + 1$ con $a, b \in \mathbb{Z}$. Entonces $n \cdot m = 4ab + 2a + 2b + 1 = 2(2ab + a + b) + 1$, que es de la forma $2k + 1$ con $k \in \mathbb{Z}$. Por tanto, $n \cdot m$ es impar. $\square$

6. **Producto de par e impar:** par × impar = par
   - **Demostración:** Sean $n = 2a$ par y $m = 2b + 1$ impar con $a, b \in \mathbb{Z}$. Entonces $n \cdot m = 2\bigl(a(2b + 1)\bigr)$, que es de la forma $2k$ con $k \in \mathbb{Z}$. Por tanto, $n \cdot m$ es par. $\square$

**Tabla de paridad:**

| Operación | Resultado |
|:----------|:----------|
| par + par | par |
| par + impar | impar |
| impar + impar | par |
| par × par | par |
| par × impar | par |
| impar × impar | impar |

### 11.4 Criterios de divisibilidad

Los **criterios de divisibilidad** son reglas que permiten determinar si un número es divisible por otro sin necesidad de realizar la división completa. Son especialmente útiles con números grandes.

**Criterio de divisibilidad por 2:**

**Proposición 11.2:** Un número entero es divisible por $2$ si y solo si su última cifra es par; es decir, termina en $0, 2, 4, 6$ u $8$.

**Demostración:** Todo número puede escribirse como:
$$n = 10a + b$$
donde $a$ representa las cifras excepto la última, y $b$ es la última cifra.

Como $10 = 2 \times 5$, tenemos $10a = 2(5a)$, que es siempre par. Por lo tanto:
$$n = 10a + b = 2(5a) + b$$
$n$ es par si y solo si $b$ es par, es decir, $b \in \{0, 2, 4, 6, 8\}$. $\square$

**Ejemplos:**
- $3458$ es divisible por $2$ porque termina en $8$ ✓
- $1237$ no es divisible por $2$ porque termina en $7$ ✗

**Criterio de divisibilidad por 3:**

**Proposición 11.3:** Un número es divisible por $3$ si y solo si la **suma de sus cifras** es divisible por $3$.

**Demostración:** Consideremos el número en notación decimal:
$$n = a_k \cdot 10^k + a_{k-1} \cdot 10^{k-1} + \cdots + a_1 \cdot 10 + a_0$$

Observemos que $10 \equiv 1 \pmod{3}$ (porque $10 = 3 \times 3 + 1$).

Por lo tanto:
$$10^j \equiv 1^j \equiv 1 \pmod{3} \quad \text{para todo } j$$

Entonces:
$$n \equiv a_k \cdot 1 + a_{k-1} \cdot 1 + \cdots + a_1 \cdot 1 + a_0 \pmod{3}$$
$$n \equiv a_k + a_{k-1} + \cdots + a_1 + a_0 \pmod{3}$$

Por lo tanto, $3 \mid n$ si y solo si $3 \mid (a_k + a_{k-1} + \cdots + a_1 + a_0)$. $\square$

**Ejemplos:**
- $12345$: suma de cifras = $1+2+3+4+5 = 15$, y $3 \mid 15$ ✓ → $3 \mid 12345$
- $7891$: suma de cifras = $7+8+9+1 = 25$, y $3 \nmid 25$ ✗ → $3 \nmid 7891$

**Criterio de divisibilidad por 4:**

**Proposición 11.4:** Un número es divisible por $4$ si y solo si sus **dos últimas cifras** forman un número divisible por $4$.

**Demostración:** Todo número puede escribirse como:
$$n = 100a + b$$
donde $b$ representa las dos últimas cifras ($0 \leq b < 100$).

Como $100 = 4 \times 25$, tenemos:
$$n = 4(25a) + b$$
Por lo tanto, $4 \mid n$ si y solo si $4 \mid b$. $\square$

**Ejemplos:**
- $3528$: las dos últimas cifras son $28$, y $28 = 4 \times 7$ ✓ → $4 \mid 3528$
- $4567$: las dos últimas cifras son $67$, y $4 \nmid 67$ ✗ → $4 \nmid 4567$

**Criterio de divisibilidad por 5:**

**Proposición 11.5:** Un número es divisible por $5$ si y solo si su última cifra es $0$ o $5$.

**Demostración:** Análoga al caso de divisibilidad por $2$:
$$n = 10a + b$$
Como $10 = 5 \times 2$, tenemos $10a = 5(2a)$, siempre divisible por $5$. Por lo tanto:
$$5 \mid n \quad \Leftrightarrow \quad 5 \mid b \quad \Leftrightarrow \quad b \in \{0, 5\}$$
$\square$

**Ejemplos:**
- $2345$ termina en $5$ ✓ → $5 \mid 2345$
- $8932$ termina en $2$ ✗ → $5 \nmid 8932$

**Criterio de divisibilidad por 6:**

**Proposición 11.6:** Un número es divisible por $6$ si y solo si es divisible por $2$ **y** por $3$.

**Demostración:** Como $6 = 2 \times 3$ y $\gcd(2, 3) = 1$, por el teorema fundamental de la aritmética:
$$6 \mid n \quad \Leftrightarrow \quad (2 \mid n) \land (3 \mid n)$$
$\square$

**Ejemplo:**
- $1236$: termina en $6$ (divisible por $2$) ✓, suma de cifras = $12$ (divisible por $3$) ✓ → $6 \mid 1236$

**Criterio de divisibilidad por 8:**

**Proposición 11.7:** Un número es divisible por $8$ si y solo si sus **tres últimas cifras** forman un número divisible por $8$.

**Demostración:** 
$$n = 1000a + b$$

Como $1000 = 8 \times 125$:
$$n = 8(125a) + b$$

Por lo tanto, $8 \mid n \Leftrightarrow 8 \mid b$. $\square$

**Ejemplos:**
- $45216$: las tres últimas cifras son $216 = 8 \times 27$ ✓ → $8 \mid 45216$
- $12345$: las tres últimas cifras son $345$, y $8 \nmid 345$ ✗ → $8 \nmid 12345$

**Criterio de divisibilidad por 9:**

**Proposición 11.8:** Un número es divisible por $9$ si y solo si la **suma de sus cifras** es divisible por $9$.

**Demostración:** Análoga al criterio de divisibilidad por $3$, pero usando $10 \equiv 1 \pmod{9}$. $\square$

**Ejemplo:**
- $7281$: suma = $7+2+8+1 = 18$, y $9 \mid 18$ ✓ → $9 \mid 7281$

**Criterio de divisibilidad por 10:**

**Proposición 11.9:** Un número es divisible por $10$ si y solo si su última cifra es $0$.

**Demostración:** Escribamos $n = 10a + b$ con $0 \leq b \leq 9$. Como $10 \equiv 0 \pmod{10}$, se tiene $n \equiv b \pmod{10}$. Por tanto $10 \mid n$ si y solo si $10 \mid b$. Pero el único dígito divisible por $10$ es $b = 0$. $\square$

**Criterio de divisibilidad por 11:**

**Proposición 11.10:** Un número es divisible por $11$ si y solo si la **suma alternada de sus cifras** (empezando por la derecha) es divisible por $11$.

**Demostración:** Como $10 \equiv -1 \pmod{11}$, tenemos:
$$10^j \equiv (-1)^j \pmod{11}$$

Por lo tanto, si $n = a_k \cdot 10^k + \cdots + a_1 \cdot 10 + a_0$:
$$n \equiv a_k(-1)^k + \cdots + a_1(-1) + a_0 \pmod{11}$$

Es decir, $11 \mid n$ si y solo si $11$ divide la suma alternada $a_0 - a_1 + a_2 - a_3 + \cdots$. $\square$

**Ejemplo:**
- $1331$: suma alternada = $1 - 3 + 3 - 1 = 0$, y $11 \mid 0$ ✓ → $11 \mid 1331$ (de hecho, $1331 = 11^3$)
- $4576$: suma alternada = $6 - 7 + 5 - 4 = 0$, y $11 \mid 0$ ✓ → $11 \mid 4576$

**Criterio de divisibilidad por 7:**

**Proposición 11.11:** Un número es divisible por $7$ si y solo si la diferencia entre el número sin la última cifra y el doble de la última cifra es divisible por $7$.

**Demostración:** Sea $n = 10a + b$, donde $b$ es la última cifra. Multiplicando por $2$:
$$2n = 20a + 2b.$$
Como $20 \equiv -1 \pmod{7}$, se tiene:
$$2n \equiv -a + 2b \pmod{7}.$$
Puesto que $\gcd(2, 7) = 1$, la congruencia $7 \mid n$ equivale a $7 \mid 2n$, es decir:
$$-a + 2b \equiv 0 \pmod{7} \quad \Longleftrightarrow \quad a - 2b \equiv 0 \pmod{7}.$$
Por lo tanto, $7 \mid n \Leftrightarrow 7 \mid (a - 2b)$. $\square$

**Procedimiento alternativo (iterativo):**
1. Separar la última cifra
2. Restar el doble de la última cifra del número restante
3. Repetir hasta obtener un número pequeño
4. Verificar si el resultado es divisible por $7$

**Ejemplo:**
- $343$: $34 - 2(3) = 34 - 6 = 28$, y $7 \mid 28$ ✓ → $7 \mid 343$ (de hecho, $343 = 7^3$)
- $1001$: $100 - 2(1) = 98$, luego $9 - 2(8) = 9 - 16 = -7$, y $7 \mid (-7)$ ✓ → $7 \mid 1001$
- $1234$: $123 - 2(4) = 115$, luego $11 - 2(5) = 1$, y $7 \nmid 1$ ✗ → $7 \nmid 1234$

> **Observación sobre criterios compuestos:**

Para algunos números que son **productos de factores coprimos**, el criterio de divisibilidad se reduce a la **conjunción** de los criterios de sus factores.

**Proposición 11.12 (Criterios compuestos):** Si $n = p \cdot q$ con $\gcd(p, q) = 1$, entonces para todo $m \in \mathbb{Z}$:
$$n \mid m \quad \Leftrightarrow \quad (p \mid m) \land (q \mid m)$$

**Ejemplos:**

1. **Divisibilidad por 15:**
   - Como $15 = 3 \times 5$ y $\gcd(3, 5) = 1$:
   - $15 \mid n \Leftrightarrow (3 \mid n) \land (5 \mid n)$
   - **Criterio:** Un número es divisible por $15$ si termina en $0$ o $5$ (criterio de $5$) **y** la suma de sus cifras es divisible por $3$ (criterio de $3$).
   - **Ejemplo:** $1275$ → termina en $5$ ✓, suma = $1+2+7+5 = 15$, y $3 \mid 15$ ✓ → $15 \mid 1275$

2. **Divisibilidad por 12:**
   - Como $12 = 3 \times 4$ y $\gcd(3, 4) = 1$:
   - $12 \mid n \Leftrightarrow (3 \mid n) \land (4 \mid n)$
   - **Criterio:** Divisible por $3$ (suma de cifras) **y** por $4$ (últimas dos cifras).

3. **Divisibilidad por 18:**
   - Como $18 = 2 \times 9$ y $\gcd(2, 9) = 1$:
   - $18 \mid n \Leftrightarrow (2 \mid n) \land (9 \mid n)$
   - **Criterio:** Divisible por $2$ (última cifra par) **y** por $9$ (suma de cifras divisible por $9$).

**Tabla resumen de criterios:**

| Divisor | Criterio |
|:--------|:---------|
| $2$ | Última cifra es par ($0, 2, 4, 6, 8$) |
| $3$ | Suma de cifras es divisible por $3$ |
| $4$ | Últimas dos cifras divisibles por $4$ |
| $5$ | Última cifra es $0$ o $5$ |
| $6$ | Divisible por $2$ y por $3$ |
| $7$ | Restar el doble de la última cifra del resto |
| $8$ | Últimas tres cifras divisibles por $8$ |
| $9$ | Suma de cifras es divisible por $9$ |
| $10$ | Última cifra es $0$ |
| $11$ | Suma alternada de cifras divisible por $11$ |
| $12$ | Divisible por $3$ y por $4$ |
| $15$ | Divisible por $3$ y por $5$ |
| $18$ | Divisible por $2$ y por $9$ |

### 11.5 Hiperoperaciones (Curiosidad)

Más allá de la potenciación, existe una jerarquía infinita de operaciones matemáticas conocida como **hiperoperaciones**. Así como la multiplicación es una suma iterada y la potenciación es una multiplicación iterada, podemos continuar esta secuencia indefinidamente.

#### 11.5.1 La Secuencia de Operaciones

Las primeras operaciones básicas pueden verse como casos particulares de una jerarquía:

1. **Sucesor ($H_0$):** $S(n) = n + 1$ (operación primitiva)
2. **Suma ($H_1$):** $a + b$ (aplicar el sucesor $b$ veces a partir de $a$)
3. **Multiplicación ($H_2$):** $a \times b$ (sumar $a$ consigo mismo $b$ veces)
4. **Potenciación ($H_3$):** $a^b$ (multiplicar $a$ consigo mismo $b$ veces)

¿Qué sigue?

#### 11.5.2 Tetración ($H_4$)

La **tetración** es la operación que sigue a la potenciación. Se define como una "potenciación iterada".

**Notación:**
La notación estándar inventada por Rudy Rucker es colocar el exponente a la izquierda y arriba:
$${^{b}a}$$
Léase "a tetrado a la b" o "torre de potencias de orden b para a".

**Definición:**
$${^{b}a} = \underbrace{a^{a^{\cdot^{\cdot^{a}}}}}_{b \text{ veces}}$$
**Ejemplos:**
- ${^{2}3} = 3^3 = 27$
- ${^{3}2} = 2^{2^2} = 2^4 = 16$
- ${^{3}3} = 3^{3^3} = 3^{27} \approx 7.6 \times 10^{12}$
- ${^{4}2} = 2^{2^{2^2}} = 2^{16} = 65,536$

El crecimiento de la tetración es increíblemente rápido, mucho más explosivo que la función exponencial.
#### 11.5.3 Notación de Flecha de Knuth

Para manejar estas operaciones gigantescas, Donald Knuth introdujo en 1976 una notación basada en flechas hacia arriba ($\uparrow$).

- **Multiplicación:** $a \times b = a + a + \dots + a$
- **Potenciación:** $a \uparrow b = a^b = a \times a \times \dots \times a$
- **Tetración:** $a \uparrow\uparrow b = {^{b}a} = a \uparrow (a \uparrow (\dots \uparrow a))$ ($b$ veces)

**Ejemplos:**
- $3 \uparrow\uparrow 2 = 3^3 = 27$
- $3 \uparrow\uparrow 3 = 3^{3^3} = 3^{27} = 7\,625\,597\,282\,987$ 
#### 11.5.4 Pentación, Hexación y N-ación

La secuencia continúa indefinidamente añadiendo más flechas.

**Pentación ($H_5$):** $a \uparrow\uparrow\uparrow b$
Es una "tetración iterada".
$$a \uparrow\uparrow\uparrow b = \underbrace{a \uparrow\uparrow (a \uparrow\uparrow (\dots \uparrow\uparrow a))}_{b \text{ veces}}$$
por ejemplo:
$$3 \uparrow \uparrow \uparrow 4 = 3 \uparrow \uparrow 3 \uparrow \uparrow 3 \uparrow \uparrow 3$$
Las operaciones se resuelven de derecha a izquierda
$$3 \uparrow \uparrow \uparrow 4 = 3 \uparrow \uparrow 3 \uparrow \uparrow \underbrace{ (3 \uparrow \uparrow 3)}_{\text{primera}} = 3 \uparrow \uparrow (3 \uparrow \uparrow 7\,625\,597\,282\,987)$$
**Hexación ($H_6$):** $a \uparrow\uparrow\uparrow\uparrow b$
Es una "pentación iterada".

**N-ación ($H_n$):**
En general, la $n$-ésima hiperoperación para $n \geq 4$ se puede expresar con $n-2$ flechas de Knuth.

Estas operaciones generan números inimaginablemente grandes, como el **Número de Graham**, que es tan inmenso que el universo observable es demasiado pequeño para contener su representación decimal escrita dígito por dígito, incluso si cada dígito ocupara un volumen de Planck.

### 11.6 El Teorema Fundamental de la Aritmética (Opcional)

El **Teorema Fundamental de la Aritmética** es uno de los resultados más importantes de la teoría de números y establece una propiedad única de los números naturales: la **factorización única en números primos**.

**Definición previa (Número primo):**
Un número natural $p > 1$ es **primo** si sus únicos divisores positivos son $1$ y $p$ mismo. Es decir:
$$p \text{ es primo} \quad \Leftrightarrow \quad \forall d \in \mathbb{N}, \, d \mid p \Rightarrow d = 1 \text{ o } d = p$$

**Ejemplos de números primos:** $2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, ...$

**Definición (Número compuesto):**
Un número natural $n > 1$ es **compuesto** si **no** es primo, es decir, si tiene al menos un divisor distinto de $1$ y de sí mismo.

**Ejemplos de números compuestos:** $4, 6, 8, 9, 10, 12, 14, 15, 16, 18, 20, ...$

**Teorema 11.1 (Teorema Fundamental de la Aritmética):**
Todo número natural $n > 1$ puede expresarse como **producto de números primos** de forma **única** (salvo el orden de los factores).

**Formalmente:** Para todo $n \in \mathbb{N}$ con $n > 1$, existen primos únicos $p_1, p_2, \dots, p_k$ y exponentes únicos $e_1, e_2, \dots, e_k \in \mathbb{N}$ tales que:
$$n = p_1^{e_1} \cdot p_2^{e_2} \cdot \ldots \cdot p_k^{e_k}$$
donde $p_1 < p_2 < \cdots < p_k$ (ordenados de menor a mayor).

**Ejemplos:**

1. $60 = 2^2 \cdot 3 \cdot 5$ (factorización única)
2. $100 = 2^2 \cdot 5^2$
3. $1001 = 7 \cdot 11 \cdot 13$
4. $2024 = 2^3 \cdot 11 \cdot 23$
5. $17$ es primo, por lo tanto $17 = 17^1$ (ya está en su forma prima)

**Demostración (idea intuitiva):**

La demostración del teorema consta de dos partes:

1. **Existencia (todo número se puede factorizar):**
   - Si $n$ es primo, ya está factorizado
   - Si $n$ es compuesto, entonces $n = a \cdot b$ con $1 < a, b < n$
   - Aplicamos el mismo proceso recursivamente a $a$ y $b$
   - Como los factores son cada vez más pequeños, el proceso **termina** (descenso infinito imposible)
   - Eventualmente todos los factores son primos

2. **Unicidad (la factorización es única):**
   - Supongamos que existe $n$ con dos factorizaciones distintas:
     $$n = p_1 \cdot p_2 \cdots p_r = q_1 \cdot q_2 \cdots q_s$$
   - Dado que $p_1 \mid n$, entonces $p_1$ divide al producto $q_1 \cdot q_2 \cdots q_s$
   - Por el **Lema de Euclides** (si un primo divide un producto, divide al menos uno de los factores), $p_1$ debe dividir a algún $q_i$
   - Como $q_i$ es primo, esto implica $p_1 = q_i$
   - Cancelamos $p_1 = q_i$ y aplicamos el mismo argumento al número resultante
   - Por inducción, todas las factorizaciones son idénticas (salvo el orden)

> **Nota:** La demostración formal completa del Teorema Fundamental de la Aritmética se desarrollará en el curso de **Teoría de Números**, donde se establecerán rigurosamente el Lema de Euclides y las técnicas de inducción necesarias.

**Consecuencias importantes:**

1. **Los primos son los "átomos" de los números:** Así como la materia se compone de átomos, los números naturales se componen de primos.

2. **Algoritmos de factorización:** Este teorema garantiza que siempre podemos descomponer un número en factores primos únicos, lo cual es fundamental en:
   - Criptografía (RSA, cifrado de clave pública)
   - Cálculo de MCD y MCM mediante factorización prima
   - Teoría de números computacional

3. **Infinitud de los primos:** Existen infinitos números primos (demostrado por Euclides hace más de 2000 años).

4. **Base para estructuras algebraicas:** La factorización única es una propiedad que se generaliza a otras estructuras algebraicas (dominios de factorización única, anillos).

> **Observación histórica:**
> Aunque el teorema parece "obvio" intuitivamente, su demostración rigurosa requiere el **Lema de Euclides** y técnicas de inducción. Fue formulado explícitamente por Carl Friedrich Gauss en su obra *Disquisitiones Arithmeticae* (1801), aunque sus principios eran conocidos desde la antigüedad griega.

**Ejemplo de aplicación (simplificación de radicales):**
$$\sqrt{180} = \sqrt{2^2 \cdot 3^2 \cdot 5} = \sqrt{2^2} \cdot \sqrt{3^2} \cdot \sqrt{5} = 2 \cdot 3 \cdot \sqrt{5} = 6\sqrt{5}$$

La factorización única nos permite identificar exactamente qué factores pueden "salir" de la raíz.

---

## 12. Jerarquía de los sistemas numéricos

### 12.1 Diagrama de inclusión

```mermaid
graph TD
    N[ℕ: Naturales<br/>1, 2, 3, ...]
    Z[ℤ: Enteros<br/>..., -2, -1, 0, 1, 2, ...]
    Q[ℚ: Racionales<br/>p/q con p∈ℤ, q∈ℕ]
    I[𝕀: Irracionales<br/>√2, π, e, ...]
    R[ℝ: Reales<br/>Todos los puntos de la recta]
    
    N -->|Agregar negativos| Z
    Z -->|Agregar fracciones| Q
    Q -->|Agregar irracionales| R
    I -->|Unión con ℚ| R
    
    style N fill:#e1f5ff,stroke:#333,stroke-width:2px
    style Z fill:#fff4e1,stroke:#333,stroke-width:2px
    style Q fill:#e1ffe1,stroke:#333,stroke-width:2px
    style I fill:#ffe1f5,stroke:#333,stroke-width:2px
    style R fill:#f5e1ff,stroke:#333,stroke-width:3px
```

### 12.2 Tabla comparativa

| Conjunto | Notación | Problema que resuelve | Cardinalidad | Ejemplo |
|:---------|:---------|:---------------------|:-------------|:--------|
| Naturales | $\mathbb{N}$ | Contar objetos | $\aleph_0$ | 1, 2, 3, 42 |
| Enteros | $\mathbb{Z}$ | Resta siempre definida | $\aleph_0$ | -5, 0, 17 |
| Racionales | $\mathbb{Q}$ | División siempre definida (excepto por 0) | $\aleph_0$ | $\frac{3}{4}$, $-\frac{7}{2}$, $0.25$ |
| Irracionales | $\mathbb{I}$ | Raíces, π, e | $\mathfrak{c}$ | $\sqrt{2}$, $\pi$, $e$ |
| Reales | $\mathbb{R}$ | Completitud (límites existen) | $\mathfrak{c}$ | Todos los anteriores |

### 12.3 Propiedades fundamentales

| Propiedad | $\mathbb{N}$ | $\mathbb{Z}$ | $\mathbb{Q}$ | $\mathbb{R}$ |
|:----------|:------------:|:------------:|:------------:|:------------:|
| Cerrado bajo suma | ✓ | ✓ | ✓ | ✓ |
| Cerrado bajo resta | ✗ | ✓ | ✓ | ✓ |
| Cerrado bajo multiplicación | ✓ | ✓ | ✓ | ✓ |
| Cerrado bajo división (excepto por 0) | ✗ | ✗ | ✓ | ✓ |
| Es un cuerpo | ✗ | ✗ | ✓ | ✓ |
| Es ordenado | ✓ | ✓ | ✓ | ✓ |
| Es completo | ✗ | ✗ | ✗ | ✓ |
| Es discreto | ✓ | ✓ | ✗ | ✗ |
| Es denso | ✗ | ✗ | ✓ | ✓ |

---

## 13. Reflexiones finales y conexión con el Cálculo

### 13.1 ¿Por qué necesitamos $\mathbb{R}$ para el Cálculo?

El Cálculo se fundamenta en conceptos como:
- **Límites**: $\lim_{x \to a} f(x)$
- **Continuidad**: funciones sin "saltos"
- **Derivadas**: tasas de cambio instantáneas
- **Integrales**: áreas bajo curvas

Todos estos conceptos requieren la **completitud** de $\mathbb{R}$. En $\mathbb{Q}$, muchas sucesiones "deberían" converger pero no lo hacen (porque su límite es irracional).

**Ejemplo:** La sucesión en $\mathbb{Q}$:
$$1, \quad 1.4, \quad 1.41, \quad 1.414, \quad 1.4142, \quad ...$$
(aproximaciones decimales de $\sqrt{2}$) "debería" converger, pero no tiene límite en $\mathbb{Q}$. En $\mathbb{R}$, converge a $\sqrt{2}$.

### 13.2 La belleza de la estructura matemática

La construcción de los números desde $\mathbb{N}$ hasta $\mathbb{R}$ es uno de los logros más elegantes de las matemáticas. Muestra cómo:
1. Partimos de una idea simple (conjunto vacío)
2. Construimos estructuras cada vez más ricas
3. Cada extensión resuelve un problema del sistema anterior
4. Llegamos a una estructura completa y coherente ($\mathbb{R}$) que modela el continuo

Esta "escalera" de conjuntos numéricos es el **fundamento** sobre el cual se construye todo el Cálculo y el Análisis Matemático.

---

## 14. Resumen de conceptos clave

**Teoría de conjuntos:**
- Conjuntos, elementos, pertenencia
- Operaciones: $\cup$, $\cap$, $\setminus$
- Paradoja de Russell: límites de la intuición
- Cardinalidad finita e infinita

**Los sistemas numéricos:**
- $\mathbb{N}$: naturales (contar)
- $\mathbb{Z}$: enteros (resta)
- $\mathbb{Q}$: racionales (división)
- $\mathbb{I}$: irracionales ($\sqrt{2}, \pi, e$)
- $\mathbb{R}$: reales (completitud)

**Cardinalidades infinitas:**
- $|\mathbb{N}| = |\mathbb{Z}| = |\mathbb{Q}| = \aleph_0$ (numerable)
- $|\mathbb{R}| = \mathfrak{c} > \aleph_0$ (no numerable)

**Axiomas de $\mathbb{R}$:**
- Axiomas de cuerpo (suma, multiplicación)
- Axiomas de orden ($\leq$)
- Axioma de completitud (supremo)

---
## 15. Ejercicios resueltos

### Ejercicio 1:
Demostrar formalmente que la suma de dos números racionales es siempre un número racional.

**Solución:**
Para que un número sea racional ($\mathbb{Q}$), debe poder expresarse como el cociente de dos enteros donde el denominador es distinto de cero.

Sean $x$ e $y$ dos números racionales cualesquiera. Por definición, existen enteros $a, b, c, d$ con $b \neq 0$ y $d \neq 0$ tales que:
$$x = \frac{a}{b} \quad \text{y} \quad y = \frac{c}{d}$$

Realizamos la suma de ambos números:
$$x + y = \frac{a}{b} + \frac{c}{d}$$

Buscando un denominador común, se cumple que:
$$x + y = \frac{ad + bc}{bd}$$

Como el conjunto de los enteros ($\mathbb{Z}$) es cerrado bajo la multiplicación y la suma:
1. El numerador $(ad + bc)$ es un número entero.
2. El denominador $(bd)$ es un número entero.

Además, como $b \neq 0$ y $d \neq 0$, su producto se verifica no nulo: $bd \neq 0$.
Por lo tanto, la expresión final es el cociente de dos enteros con denominador no nulo, lo cual cumple exactamente la definición de un número racional.

**Respuesta final:** Se demuestra que la suma de dos racionales pertenece siempre a $\mathbb{Q}$. $\blacksquare$

### Ejercicio 2:
Determinar si el número $45,312$ es divisible por $3$, $4$ y $9$, aplicando los criterios de divisibilidad estudiados.

**Solución:**
Se analiza cada caso aplicando su criterio correspondiente paso a paso:

**Paso 1: Divisibilidad por 3**
El criterio establece que la suma de las cifras debe ser múltiplo de $3$.
$$4 + 5 + 3 + 1 + 2 = 15$$
Dado que $15$ es divisible por $3$ ($15 = 3 \times 5$), se verifica que el número $45,312$ es divisible por $3$.

**Paso 2: Divisibilidad por 4**
El criterio establece que las dos últimas cifras deben formar un número múltiplo de $4$.
Las dos últimas cifras son $12$.
Dado que $12$ es divisible por $4$ ($12 = 4 \times 3$), se verifica que el número $45,312$ es divisible por $4$.

**Paso 3: Divisibilidad por 9**
El criterio establece que la suma de las cifras debe ser múltiplo de $9$.
Tomamos la suma ya calculada en el paso uno: $15$.
Dado que $15$ no es divisible por $9$, el número $45,312$ no es divisible por $9$.

**Respuesta final:** El número $45,312$ es divisible por $3$ y por $4$, pero no es divisible por $9$.

### Ejercicio 3:
Demostrar que para dos cualesquiera números reales $a$ y $b$ se cumple que $a \cdot (-b) = -(ab)$.

**Solución:**
Queremos demostrar que la expresión $a \cdot (-b)$ actúa como el inverso aditivo de $ab$. Según el **Axioma 4** (elemento inverso de la suma), para probar que un elemento es el inverso de otro, basta con verificar que al sumarlos el resultado sea el elemento neutro ($0$):
$$(ab) + (a \cdot (-b)) = 0$$

**Paso 1: Aplicar distributividad**
Partimos de la expresión original y aplicamos el **Axioma 11** (Distributividad) para factorizar la variable $a$:
$$(ab) + (a \cdot (-b)) = a \cdot (b + (-b))$$

**Paso 2: Elemento inverso de la suma**
Por el **Axioma 4**, la suma de un número con su inverso aditivo siempre resulta en $0$. Por ende, reemplazamos $b + (-b)$ por $0$:
$$a \cdot (b + (-b)) = a \cdot 0$$

**Paso 3: Multiplicación por el neutro aditivo**
Por las propiedades deducidas de los axiomas de cuerpo, sabemos que todo número real multiplicado por cero da cero ($a \cdot 0 = 0$).
*(Nota: Esto se deduce de $a \cdot 0 = a \cdot (0 + 0) = a \cdot 0 + a \cdot 0$, lo que al restar $a \cdot 0$ a ambos lados demuestra que $0 = a \cdot 0$).*
Por lo tanto:
$$a \cdot 0 = 0$$

**Conclusión:**
Al encadenar todos los pasos, hemos comprobado que:
$$(ab) + (a \cdot (-b)) = 0$$
Dado que sumarle $a \cdot (-b)$ a $ab$ da como resultado $0$, queda certificado que $a \cdot (-b)$ es exactamente el inverso aditivo de $ab$.

**Respuesta final:** Por unicidad del inverso aditivo en $\mathbb{R}$, se demuestra que $a \cdot (-b) = -(ab)$. $\blacksquare$

---
## 16. Ejercicios propuestos

**Ejercicio 1:** Demuestra que $\mathbb{Z}$ tiene la misma cardinalidad que $\mathbb{N}$ construyendo explícitamente una biyección entre ellos.

**Ejercicio 2:** Prueba que $\sqrt{3} \notin \mathbb{Q}$ usando un argumento similar al del Teorema 7.1.

**Ejercicio 3:** Usando los axiomas de cuerpo, demuestra que:
a) $\forall a \in \mathbb{R}, \quad a \cdot 0 = 0$  
b) $\forall a \in \mathbb{R}, \quad (-1) \cdot a = -a$

**Ejercicio 4:** Explica con tus palabras por qué $\mathbb{Q}$ es denso pero no completo.

**Ejercicio 5 (Desafío):** Investiga la **construcción por cortaduras de Dedekind** de $\mathbb{R}$ y explica la idea central en un párrafo.

---

**Referencias recomendadas:**
- Rudin, W. (1976). *Principles of Mathematical Analysis* (3rd ed.). McGraw-Hill.
- Spivak, M. (2008). *Calculus* (4th ed.). Publish or Perish.
- Apostol, T. M. (1967). *Calculus, Volume I* (2nd ed.). Wiley.
- Stewart, J. (2015). *Calculus: Early Transcendentals* (8th ed.). Cengage Learning.
