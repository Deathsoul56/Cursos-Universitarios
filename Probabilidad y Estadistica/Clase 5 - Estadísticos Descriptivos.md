# Estadísticos Descriptivos

En esta clase se estudian los estadísticos descriptivos que resumen un conjunto de datos en pocas cifras: las medidas de tendencia central (la media y sus variantes, la mediana y la moda), las medidas de posición (los cuantiles), las medidas de dispersión, los momentos, las medidas de forma (asimetría y curtosis) y las medidas de concentración (curva de Lorenz e índice de Gini, con los índices de Theil y de Atkinson como complemento opcional). Una sección opcional extiende la media y la varianza a datos complejos y angulares. Se demuestran las propiedades de cada medida y se discuten sus criterios de elección según la escala de medición, la forma de la distribución y la presencia de valores atípicos.

---

## 1. Introducción y notación

Las tablas de frecuencias y los gráficos de las clases anteriores muestran la forma de un conjunto de datos, pero no permiten compararlo con otro con precisión ni tomar decisiones a partir de él. Para eso se necesitan números: valores que resuman, cada uno, una característica específica de los datos. ¿Alrededor de qué valor se agrupan? ¿Cuánto se alejan entre sí? ¿Qué tan simétricos son? A esos resúmenes numéricos se les denomina **estadísticos descriptivos**, y son el objeto de esta clase.

### 1.1 Notación

Se denomina **población** al conjunto total de unidades de estudio, de tamaño $N$, y **muestra** a un subconjunto de ella, de tamaño $n$. En esta clase se utilizan las siguientes convenciones:

- $N$ denota el tamaño de la población y $n$ el tamaño de la muestra.
- Los **parámetros** poblacionales se denotan con letras griegas ($\mu$, $\sigma^2$) y sus análogos calculados a partir de una muestra, con letras latinas ($\bar{x}$, $S^2$).
- **Datos a granel:** $\mathbf{x} = (x_1, x_2, \ldots, x_n) \in \mathbb{R}^n$.
- **Estadísticos de orden:** al ordenar los datos de menor a mayor se obtiene $x_{(1)} \leq x_{(2)} \leq \cdots \leq x_{(n)}$, como en la Clase 3.
- **Datos agrupados:** si los datos se agrupan en $k$ clases, $m_i$ es la marca de la clase $i$, $n_i$ su frecuencia absoluta, con $\sum_{i=1}^{k} n_i = n$, y $f_i = n_i/n$ su frecuencia relativa.

### 1.2 Estadístico y familias de estadísticos

Antes de estudiar cada medida conviene precisar de qué clase de objeto se trata. Un promedio, una proporción o una desviación son resultados de operar con los datos observados, y se distinguen de las constantes de la población que se desea conocer. Esa diferencia, entre lo que se calcula y lo que se quiere estimar, organiza todo el resto del curso.
**Definición 1.1 (Estadístico):**
Un **estadístico** es una función $T: \mathbb{R}^n \to \mathbb{R}$ (o $T: \mathbb{R}^n \to \mathbb{R}^k$) que se calcula a partir de los datos de una muestra y cuya expresión no depende de ningún parámetro poblacional desconocido.

> **Observación:** un estadístico se calcula a partir de la muestra; un parámetro es una constante de la población, usualmente desconocida. Los estadísticos sirven para describir la muestra y, más adelante en el curso, para estimar los parámetros.

**Ejemplo 1.1 (Estadístico y parámetro):**
Se miden los tiempos de espera, en minutos, de $n = 4$ clientes elegidos entre todos los de una tienda: $(4, 7, 9, 12)$. La media $\bar{x} = 8$ y el máximo $x_{(4)} = 12$ son estadísticos, pues se calculan únicamente con los datos. La media $\mu$ de los tiempos de espera de todos los clientes de la tienda es un parámetro: no se conoce, y $\bar{x}$ sirve para estimarla. En cambio, la expresión $\sum_{i=1}^{4} (x_i - \mu)^2$ no es un estadístico, porque depende del parámetro desconocido $\mu$.

Los estadísticos descriptivos se organizan en familias, según la pregunta que responden:

| Familia | Pregunta que responde | Ejemplos | Sección |
|:--------|:----------------------|:---------|:-------:|
| Tendencia central | ¿Alrededor de qué valor se agrupan los datos? | Media, mediana, moda | 2 |
| Posición | ¿Qué valor deja por debajo una proporción dada de los datos? | Cuartiles, deciles, percentiles | 3 |
| Dispersión | ¿Cuánto se alejan los datos entre sí o respecto del centro? | Varianza, desviación estándar, rango intercuartílico | 4 |
| Forma | ¿Qué tan simétrica es la distribución y qué tan pesadas son sus colas? | Sesgo, curtosis | 5 y 6 |
| Concentración | ¿Qué tan acaparado está un total por pocas unidades? | Curva de Lorenz, índice de Gini | 7 |

---

## 2. Medidas de tendencia central

Resumir un conjunto de datos con un único valor típico es la forma más elemental de descripción. No existe una única manera de hacerlo: cada medida responde a un criterio distinto (equilibrio, error mínimo, posición, frecuencia) y, por ello, se comporta de manera distinta frente a valores extremos o frente a distintas escalas de medición. En esta sección se estudian las principales.

### 2.1 Media aritmética

Pensemos en una regla rígida y sin peso sobre la cual se colocan masas iguales en las posiciones $x_1, x_2, \ldots, x_n$. ¿En qué punto hay que apoyar el pivote para que la regla quede en equilibrio? Ese punto es la media aritmética: el valor que anula la suma de los momentos de torsión que ejerce cada masa. La idea es antigua y cotidiana (el "promedio"), pero su justificación matemática es más profunda de lo que parece.

> **Nota histórica:** en 1805 Adrien-Marie Legendre publicó el método de mínimos cuadrados para ajustar las órbitas de cometas. En 1809, Carl Friedrich Gauss mostró que si se exige que la media aritmética sea el valor más probable de una magnitud medida repetidas veces, entonces los errores de medición deben seguir la distribución que hoy lleva su nombre: la normal. Esta conexión entre la media, los mínimos cuadrados y la distribución normal es una de las ideas centrales de la estadística.

**Definición 2.1 (Media aritmética):**
Dada una muestra $\mathbf{x} = (x_1, \ldots, x_n) \in \mathbb{R}^n$ con $n \geq 1$, la **media aritmética** es:

$$
\bar{x} = \dfrac{1}{n} \sum_{i=1}^{n} x_i
$$

Cuando se conoce toda la población, la misma expresión con $N$ datos define la media poblacional $\mu$.

**Ejemplo 2.1 (Salarios de una pequeña empresa):**
Una empresa de software tiene $15$ empleados. Sus salarios mensuales, en miles de dólares y ordenados de menor a mayor, son:

$$
\mathbf{x} = (1.2,\ 1.2,\ 1.5,\ 1.5,\ 1.5,\ 1.8,\ 2.0,\ 2.2,\ 2.5,\ 2.5,\ 3.0,\ 3.5,\ 4.0,\ 6.0,\ 15.0)
$$

El último valor corresponde al director de la empresa. La media aritmética es:

$$
\begin{align}
\bar{x} &= \dfrac{1.2 + 1.2 + 1.5 + 1.5 + 1.5 + 1.8 + 2.0 + 2.2 + 2.5 + 2.5 + 3.0 + 3.5 + 4.0 + 6.0 + 15.0}{15} \\
&= \dfrac{49.4}{15} \approx 3.29
\end{align}
$$

El salario medio es de unos $3\,290$ dólares. Sin embargo, solo $4$ de los $15$ empleados ganan más que ese valor, y $11$ ganan menos. El único salario de $15\,000$ dólares eleva la media por encima de lo que gana la mayoría. Este conjunto de datos se utilizará como ejemplo de referencia en el resto de la clase.

Con frecuencia los datos se transforman mediante un cambio de unidades o de origen: de grados Celsius a Fahrenheit, de metros a centímetros, de dólares a miles de dólares. Si ya se conoce la media de los datos originales, ¿es necesario recalcularla con los datos transformados? El siguiente teorema muestra que no: la media se transforma igual que cada dato.

**Teorema 2.1 (Efecto de una transformación afín):**
Si $y_i = a x_i + b$ para $i = 1, \ldots, n$, con $a, b \in \mathbb{R}$, entonces:

$$
\bar{y} = a\bar{x} + b
$$

Por ejemplo, la conversión de grados Celsius a Fahrenheit es $y = 1.8x + 32$: si la temperatura media de una semana fue de $25\,^\circ\text{C}$, su media en grados Fahrenheit es $1.8 \cdot 25 + 32 = 77\,^\circ\text{F}$, sin necesidad de convertir cada medición.

**Demostración:**

$$
\begin{align}
\bar{y} &= \dfrac{1}{n} \sum_{i=1}^{n} (a x_i + b) \\
&= a \cdot \dfrac{1}{n} \sum_{i=1}^{n} x_i + \dfrac{1}{n} \cdot nb \\
&= a\bar{x} + b
\end{align}
$$

$\blacksquare$

**Teorema 2.2 (Suma de desviaciones nula):**
La suma de las desviaciones de los datos respecto de su media es cero:

$$
\sum_{i=1}^{n} (x_i - \bar{x}) = 0
$$

**Demostración:**
Como $\bar{x}$ no depende de $i$, la suma de $n$ copias de $\bar{x}$ es $n\bar{x}$. Entonces:

$$
\begin{align}
\sum_{i=1}^{n} (x_i - \bar{x}) &= \sum_{i=1}^{n} x_i - n\bar{x} \\
&= \sum_{i=1}^{n} x_i - n \cdot \dfrac{1}{n} \sum_{i=1}^{n} x_i \\
&= 0
\end{align}
$$

$\blacksquare$

El Teorema 2.2 es la expresión matemática del equilibrio de la regla: la media es el único punto $p$ que cumple $\sum_{i=1}^{n} (x_i - p) = 0$.

**Teorema 2.3 (La media minimiza el error cuadrático):**
Para todo $c \in \mathbb{R}$ se cumple:

$$
\sum_{i=1}^{n} (x_i - c)^2 = \sum_{i=1}^{n} (x_i - \bar{x})^2 + n(\bar{x} - c)^2
$$

En consecuencia, la media es el único valor $c$ que minimiza $\sum_{i=1}^{n} (x_i - c)^2$, es decir:

$$
\arg\min_{c \in \mathbb{R}} \sum_{i=1}^{n} (x_i - c)^2 = \bar{x}
$$

> **Nota:** $\arg\min$ no devuelve el valor mínimo de la función, sino el valor del argumento (aquí, la constante $c$) con el que se alcanza ese mínimo.

**Demostración:**
Se suma y se resta $\bar{x}$ dentro de cada término y se desarrolla el cuadrado:

$$
\begin{align}
\sum_{i=1}^{n} (x_i - c)^2 &= \sum_{i=1}^{n} \left[ (x_i - \bar{x}) + (\bar{x} - c) \right]^2 \\
&= \sum_{i=1}^{n} (x_i - \bar{x})^2 + 2(\bar{x} - c) \sum_{i=1}^{n} (x_i - \bar{x}) + n(\bar{x} - c)^2 \\
&= \sum_{i=1}^{n} (x_i - \bar{x})^2 + n(\bar{x} - c)^2
\end{align}
$$

donde en la última igualdad se usó el Teorema 2.2. El primer sumando no depende de $c$, y el segundo es no negativo y se anula si y solo si $c = \bar{x}$. Por tanto, el mínimo se alcanza únicamente en $c = \bar{x}$.
$\blacksquare$

**Ejemplo 2.2 (Aumento salarial):**
La empresa del Ejemplo 2.1 otorga a todos sus empleados un aumento del $5\%$ y una bonificación fija de $300$ dólares, es decir, $0.3$ en miles de dólares. El nuevo salario es la transformación afín $y_i = 1.05\,x_i + 0.3$. Por el Teorema 2.1, no es necesario recalcular la media con los $15$ salarios nuevos:

$$
\bar{y} = 1.05 \cdot 3.2933 + 0.3 \approx 3.758
$$

El salario medio pasa de unos $3\,293$ a $3\,758$ dólares. El factor $a = 1.05$ afecta al salario medio como a cada salario, y la constante $b = 0.3$ lo desplaza en la misma cantidad.

**Datos agrupados:**
Cuando solo se dispone de la tabla de frecuencias, la media se aproxima usando las marcas de clase en lugar de los datos originales.

**Definición 2.2 (Media para datos agrupados):**
Para datos agrupados en $k$ clases con marcas $m_i$ y frecuencias absolutas $n_i$, la media se aproxima por:

$$
\bar{x} \approx \dfrac{1}{n} \sum_{i=1}^{k} m_i n_i = \sum_{i=1}^{k} m_i f_i
$$

La igualdad exacta solo se cumple si todos los datos de cada clase coinciden con su marca; en general es una aproximación, porque dentro de cada intervalo se pierde la información individual (véase la Clase 3).

**Ejemplo 2.3 (Datos de la Clase 3):**
Con la tabla de las 50 mediciones de la Clase 3 (Ejemplo 3.4), las marcas y frecuencias son:

| Marca $m_i$ | 0.28 | 0.78 | 1.28 | 1.78 | 2.28 | 2.78 | 3.28 |
|:-----------:|:----:|:----:|:----:|:----:|:----:|:----:|:----:|
| $n_i$ | 19 | 9 | 9 | 6 | 2 | 3 | 2 |

$$
\begin{align}
\bar{x} &\approx \dfrac{0.28(19) + 0.78(9) + 1.28(9) + 1.78(6) + 2.28(2) + 2.78(3) + 3.28(2)}{50} \\
&= \dfrac{54.00}{50} = 1.08
\end{align}
$$

La media calculada con los 50 datos originales es $\bar{x} = 53.08/50 = 1.0616$. La diferencia entre ambos valores es el costo de haber agrupado los datos.

**Propiedades de la media aritmética:**

1. **Transformaciones afines:** si $y_i = a x_i + b$, entonces $\bar{y} = a\bar{x} + b$ (Teorema 2.1).
2. **Suma de desviaciones nula:** $\sum_{i=1}^{n} (x_i - \bar{x}) = 0$; la media es el punto de equilibrio de los datos (Teorema 2.2).
3. **Minimiza el error cuadrático:** $\bar{x}$ es el único valor $c$ que minimiza $\sum_{i=1}^{n} (x_i - c)^2$ (Teorema 2.3).
4. **Internalidad:** $x_{(1)} \leq \bar{x} \leq x_{(n)}$, y cualquiera de las dos igualdades se da si y solo si todos los datos son iguales.
5. **No pertenece necesariamente a los datos:** una media de $2.5$ hijos por familia no corresponde a ninguna familia real y sigue siendo un resumen válido. Tampoco tiene por qué respetar la naturaleza de la variable: es un valor de $\mathbb{R}$ aun cuando los datos sean enteros.
6. **Sensibilidad a valores atípicos:** un solo dato puede desplazar la media tanto como se quiera.

**Demostración de las propiedades 4 y 6:**
*Propiedad 4.* Como $x_{(1)} \leq x_i \leq x_{(n)}$ para todo $i$, promediando se obtiene $x_{(1)} \leq \bar{x} \leq x_{(n)}$. Si $\bar{x} = x_{(1)}$, entonces $\sum_i (x_i - x_{(1)}) = 0$ y, como todos los sumandos son no negativos, cada uno es cero, es decir, todos los datos son iguales a $x_{(1)}$. El caso $\bar{x} = x_{(n)}$ es análogo, y el recíproco es inmediato.

*Propiedad 6.* Sea $\mathbf{y}$ la muestra que resulta de reemplazar el dato $x_j$ por un valor $y_j$, sin modificar los demás. Entonces:

$$
\bar{y} - \bar{x} = \dfrac{y_j - x_j}{n}
$$

Para cualquier cota $K > 0$, si se elige $y_j$ con $|y_j - x_j| > nK$, se tiene $|\bar{y} - \bar{x}| > K$. Es decir, alterando un único dato, la media puede alejarse de su valor original tanto como se desee. Esta falta de resistencia se mide con el punto de ruptura de la Definición 2.10, que para la media vale $1/n$ (Proposición 2.5) y tiende a $0$ cuando $n$ crece.
$\blacksquare$

**Ejemplo 2.4 (Un dato erróneo):**
Si en el Ejemplo 2.1 el salario del director, $15.0$, se registrara por error como $150.0$, la media pasaría a:

$$
\bar{y} = 3.293 + \dfrac{150.0 - 15.0}{15} = 3.293 + 9 = 12.293
$$

Un solo dato erróneo casi cuadruplicaría el salario medio, a pesar de que los otros $14$ salarios no cambiaron. En la Sección 2.7 se verá que la mediana, en cambio, permanecería igual a $2.2$.

**Aplicaciones:**

- **Educación:** el promedio de calificaciones de un curso.
- **Física y ingeniería:** el valor medio de repetidas mediciones de una misma magnitud, que reduce el efecto del error aleatorio.
- **Aprendizaje automático:** el error cuadrático medio, la función de pérdida más usada en regresión, es una media aritmética de errores al cuadrado, y el Teorema 2.3 explica por qué la media es su minimizador.

### 2.2 Media ponderada

No todas las observaciones tienen siempre la misma importancia. En un curso, el examen final no debería pesar lo mismo que un cuestionario semanal; en una cartera de inversión, un activo en el que se invirtió el 70% del capital no debería contar igual que uno en el que se invirtió el 5%. La media ponderada resuelve esta situación asignando a cada dato un peso que refleja su importancia relativa.

**Definición 2.3 (Media ponderada):**
Dados los datos $\mathbf{x} \in \mathbb{R}^n$ y los pesos $\mathbf{w} = (w_1, \ldots, w_n)$ con $w_i \geq 0$ y $\sum_{i=1}^{n} w_i > 0$, la **media ponderada** es:

$$
\bar{x}_w = \dfrac{\sum_{i=1}^{n} w_i x_i}{\sum_{i=1}^{n} w_i}
$$

Si los pesos están normalizados, es decir $\sum_{i=1}^{n} w_i = 1$, el denominador es $1$ y $\bar{x}_w = \sum_{i=1}^{n} w_i x_i$.

**Ejemplo 2.5 (Salarios ponderados por antigüedad):**
Se retoman los salarios del Ejemplo 2.1 y se añade, para cada empleado, su antigüedad en la empresa en años, que se usará como peso $w_i$:

| Empleado | Salario $x_i$ (miles de USD) | Antigüedad $w_i$ (años) | $w_i x_i$ |
|:--------:|:----------------------------:|:-----------------------:|:---------:|
| 1 | 1.2 | 1 | 1.2 |
| 2 | 1.2 | 2 | 2.4 |
| 3 | 1.5 | 1 | 1.5 |
| 4 | 1.5 | 2 | 3.0 |
| 5 | 1.5 | 3 | 4.5 |
| 6 | 1.8 | 2 | 3.6 |
| 7 | 2.0 | 4 | 8.0 |
| 8 | 2.2 | 3 | 6.6 |
| 9 | 2.5 | 5 | 12.5 |
| 10 | 2.5 | 4 | 10.0 |
| 11 | 3.0 | 6 | 18.0 |
| 12 | 3.5 | 8 | 28.0 |
| 13 | 4.0 | 10 | 40.0 |
| 14 | 6.0 | 7 | 42.0 |
| 15 | 15.0 | 12 | 180.0 |
| **Total** | — | **70** | **361.3** |

$$
\bar{x}_w = \dfrac{\sum_{i=1}^{15} w_i x_i}{\sum_{i=1}^{15} w_i} = \dfrac{361.3}{70} \approx 5.16
$$

El salario medio ponderado por antigüedad es de unos $5\,160$ dólares, frente a los $3\,290$ de la media aritmética. La diferencia se debe a que los empleados más antiguos tienden a ganar más y, al ponderar, su salario cuenta tantas veces como años acumulados: el director, por ejemplo, aporta el $12/70 \approx 17\%$ del peso total y no el $1/15 \approx 7\%$. Esta media responde a una pregunta distinta de la anterior: no es el salario de un empleado típico, sino el salario promedio asociado a un año de trabajo acumulado en la empresa.

**Teorema 2.4 (Pesos iguales):**
Si todos los pesos son iguales, $w_1 = \cdots = w_n = w > 0$, entonces $\bar{x}_w = \bar{x}$.

**Demostración:**

$$
\bar{x}_w = \dfrac{\sum_{i=1}^{n} w x_i}{\sum_{i=1}^{n} w} = \dfrac{w \sum_{i=1}^{n} x_i}{nw} = \dfrac{1}{n} \sum_{i=1}^{n} x_i = \bar{x}
$$

$\blacksquare$

La media aritmética es, por tanto, un caso particular de media ponderada. Del mismo modo, la media de datos agrupados de la Definición 2.2 es la media ponderada de las marcas $m_i$ con pesos $w_i = n_i$.

**Ejemplo 2.6 (Calificación ponderada por créditos):**
Un estudiante obtiene las siguientes calificaciones, cada una ponderada por el número de créditos de la asignatura:

| Asignatura | Calificación $x_i$ | Créditos $w_i$ |
|:-----------|:------------------:|:--------------:|
| Bioquímica | 8.0 | 6 |
| Física II | 6.5 | 5 |
| Taller de Comunicación | 10.0 | 2 |

$$
\begin{align}
\bar{x}_w &= \dfrac{6(8.0) + 5(6.5) + 2(10.0)}{6 + 5 + 2} \\
&= \dfrac{100.5}{13} \approx 7.73
\end{align}
$$

La media aritmética de las tres calificaciones sería $8.17$. Aunque la nota más alta (10.0) corresponde al taller, su peso es el menor, por lo que influye poco en el resultado.

> **Observación:** la media ponderada con pesos no negativos siempre queda entre el mínimo y el máximo de los datos, pues es una combinación de ellos con coeficientes $w_i/\sum_j w_j \geq 0$ que suman $1$.

**Aplicaciones:**

- **Educación:** el promedio ponderado por créditos y la nota final de un curso.
- **Finanzas:** la rentabilidad de una cartera, ponderando cada activo por la fracción del capital invertido, y los índices bursátiles ponderados por capitalización de mercado.

### 2.3 Media geométrica

Cuando una magnitud evoluciona por cambios proporcionales y no por cambios aditivos, la media aritmética deja de representar bien el comportamiento típico. Pensemos en una población de bacterias que se multiplica cada hora, o en un capital cuyo crecimiento anual se aplica sobre lo acumulado el año anterior: el efecto total es el producto de los factores de crecimiento, no su suma. La media geométrica es el factor constante que, repetido en todos los períodos, produce el mismo efecto total.

**Definición 2.4 (Media geométrica):**
Dada una muestra de valores estrictamente positivos $\mathbf{x} \in \mathbb{R}^n_{>0}$, la **media geométrica** es:

$$
G = \left( \prod_{i=1}^{n} x_i \right)^{1/n} = \sqrt[n]{x_1 x_2 \cdots x_n}
$$

La restricción $x_i > 0$ evita raíces de índice par de números negativos.

**Teorema 2.5 (Media geométrica y media aritmética de logaritmos):**
El logaritmo de la media geométrica es la media aritmética de los logaritmos de los datos:

$$
\ln G = \dfrac{1}{n} \sum_{i=1}^{n} \ln x_i
$$

**Demostración:**
Aplicando $\ln$ a la definición y usando $\ln(a^r) = r \ln a$ y $\ln(ab) = \ln a + \ln b$:

$$
\begin{align}
\ln G &= \ln \left[ \left( \prod_{i=1}^{n} x_i \right)^{1/n} \right] \\
&= \dfrac{1}{n} \ln \left( \prod_{i=1}^{n} x_i \right) \\
&= \dfrac{1}{n} \sum_{i=1}^{n} \ln x_i
\end{align}
$$

$\blacksquare$

**Ejemplo 2.7 (Factores de crecimiento):**
Una empresa multiplica su valor por $5$ en el primer año y por $20$ en el segundo. El factor constante anual que produce el mismo resultado final es:

$$
G = \sqrt{5 \cdot 20} = \sqrt{100} = 10
$$

En cambio, la media aritmética daría $(5 + 20)/2 = 12.5$, y al aplicarla dos veces se obtendría $12.5^2 = 156.25$, que no coincide con el factor total real de $100$.

**Ejemplo 2.8 (Tasas de crecimiento):**
Cuando los datos son tasas de crecimiento $r_i$, la media geométrica se aplica a los factores $1 + r_i$. Un capital crece $10\%$, $20\%$ y luego decrece $5\%$ en tres años consecutivos. Los factores son $1.10$, $1.20$ y $0.95$, con producto $1.254$:

$$
G = \sqrt[3]{1.254} \approx 1.0784
$$

La tasa media anual es, por tanto, aproximadamente $7.84\%$. La media aritmética de las tasas, $(10 + 20 - 5)/3 = 8.33\%$, sobreestima el crecimiento: $1.0833^3 \approx 1.271 > 1.254$.

**Aplicaciones:**

- **Finanzas:** la tasa de rendimiento anual compuesta de una inversión.
- **Biología:** el crecimiento medio de poblaciones que se multiplican en cada período.
- **Índices y normalización:** la combinación de indicadores medidos en escalas muy distintas, como en el cálculo de índices compuestos, donde la media geométrica evita que una escala domine a las demás.

### 2.4 Media armónica

Un automóvil recorre un tramo a $60\ \text{km/h}$ y regresa por el mismo camino a $40\ \text{km/h}$. ¿Cuál es su velocidad media en todo el viaje? La respuesta intuitiva, $50\ \text{km/h}$, es incorrecta, porque el vehículo pasa más tiempo viajando a la velocidad menor. La media armónica es la media adecuada cuando los datos son razones (como velocidades) y la cantidad que se mantiene fija es el numerador de esa razón (aquí, la distancia).

**Definición 2.5 (Media armónica):**
Dada una muestra $\mathbf{x} \in \mathbb{R}^n_{>0}$, la **media armónica** es el inverso de la media aritmética de los inversos:

$$
H = \left( \dfrac{1}{n} \sum_{i=1}^{n} \dfrac{1}{x_i} \right)^{-1} = \dfrac{n}{\dfrac{1}{x_1} + \dfrac{1}{x_2} + \cdots + \dfrac{1}{x_n}}
$$

**Proposición 2.1 (Velocidad media):**
Si un móvil recorre $n$ tramos de igual longitud $d$ a velocidades constantes $v_1, \ldots, v_n > 0$, su velocidad media en el recorrido total es la media armónica de las velocidades.

**Demostración:**
La velocidad media es la distancia total dividida entre el tiempo total. El tiempo en el tramo $i$ es $d/v_i$, de modo que:

$$
\bar{v} = \dfrac{nd}{\sum_{i=1}^{n} \dfrac{d}{v_i}} = \dfrac{n}{\sum_{i=1}^{n} \dfrac{1}{v_i}} = H
$$

$\blacksquare$

**Ejemplo 2.9 (Ida y vuelta):**
Con $v_1 = 60$ y $v_2 = 40$ km/h:

$$
H = \dfrac{2}{\dfrac{1}{60} + \dfrac{1}{40}} = \dfrac{2}{\dfrac{5}{120}} = 48\ \text{km/h}
$$

Se verifica: para una distancia de $120\ \text{km}$ por tramo, el tiempo total es $2 + 3 = 5$ horas y la distancia total es $240\ \text{km}$, es decir, $240/5 = 48\ \text{km/h}$.

**Aplicaciones:**

- **Física:** la velocidad media en recorridos de tramos iguales y la resistencia equivalente de resistencias en paralelo, que es $H/n$.
- **Finanzas:** el promedio de razones como el precio sobre ganancias de varios activos.
- **Ciencias de la computación:** la medida $F_1$ de un clasificador es la media armónica de precisión y exhaustividad.

### 2.5 Medias geométrica y armónica ponderadas

Las medias geométrica y armónica de las secciones anteriores asignan a todos los datos la misma importancia. Esa hipótesis falla con frecuencia: un período de inversión de cinco años no debería pesar lo mismo que uno de un año, y un tramo de $120\ \text{km}$ no debería pesar lo mismo que uno de $80\ \text{km}$. Igual que con la media aritmética, la solución es asignar a cada dato un peso.

**Definición 2.6 (Media geométrica ponderada):**
Dados $\mathbf{x} \in \mathbb{R}^n_{>0}$ y pesos $w_i \geq 0$ con $\sum_{i=1}^{n} w_i > 0$, la **media geométrica ponderada** es:

$$
G_w = \left( \prod_{i=1}^{n} x_i^{w_i} \right)^{1/\sum_{i} w_i}
$$

**Definición 2.7 (Media armónica ponderada):**
Con los mismos datos y pesos, la **media armónica ponderada** es:

$$
H_w = \dfrac{\sum_{i=1}^{n} w_i}{\sum_{i=1}^{n} \dfrac{w_i}{x_i}}
$$

**Proposición 2.2 (Caracterización de las medias ponderadas):**
Se cumple:

$$
\ln G_w = \dfrac{\sum_{i=1}^{n} w_i \ln x_i}{\sum_{i=1}^{n} w_i}, \qquad \dfrac{1}{H_w} = \dfrac{\sum_{i=1}^{n} w_i \cdot \dfrac{1}{x_i}}{\sum_{i=1}^{n} w_i}
$$

Es decir, $\ln G_w$ es la media aritmética ponderada de los logaritmos y $1/H_w$ es la media aritmética ponderada de los inversos. Con pesos iguales, $G_w = G$ y $H_w = H$.

**Demostración:**
Aplicando $\ln$ a la Definición 2.6 y usando $\ln(ab) = \ln a + \ln b$ y $\ln(a^r) = r \ln a$:

$$
\ln G_w = \dfrac{1}{\sum_i w_i} \ln \left( \prod_{i=1}^{n} x_i^{w_i} \right) = \dfrac{\sum_{i=1}^{n} w_i \ln x_i}{\sum_{i=1}^{n} w_i}
$$

La segunda igualdad se obtiene invirtiendo la Definición 2.7. Si todos los pesos valen $w$, la primera expresión es $\tfrac{1}{n} \sum_i \ln x_i = \ln G$ (Teorema 2.5) y la segunda es $\tfrac{1}{n} \sum_i 1/x_i = 1/H$.
$\blacksquare$

**Proposición 2.3 (Desigualdad ponderada):**
Se cumple $H_w \leq G_w \leq \bar{x}_w$, con igualdad si y solo si todos los datos con peso positivo son iguales.

**Demostración:**
Se usa $\ln t \leq t - 1$ para $t > 0$, con igualdad si y solo si $t = 1$. Con $t = x_i/\bar{x}_w$, multiplicando por $w_i \geq 0$ y sumando:

$$
\begin{align}
\sum_{i=1}^{n} w_i \ln \dfrac{x_i}{\bar{x}_w} &\leq \sum_{i=1}^{n} w_i \left( \dfrac{x_i}{\bar{x}_w} - 1 \right) \\
&= \dfrac{\sum_i w_i x_i}{\bar{x}_w} - \sum_{i=1}^{n} w_i \\
&= 0
\end{align}
$$

Por tanto $\sum_i w_i \ln x_i \leq \left( \sum_i w_i \right) \ln \bar{x}_w$, es decir, $\ln G_w \leq \ln \bar{x}_w$. La igualdad exige $x_i = \bar{x}_w$ para todo $i$ con $w_i > 0$. Para $H_w \leq G_w$ se aplica lo anterior a los datos $y_i = 1/x_i$ con los mismos pesos: por la Proposición 2.2, la media geométrica ponderada de los $y_i$ es $1/G_w$ y su media aritmética ponderada es $1/H_w$, de modo que $1/G_w \leq 1/H_w$.
$\blacksquare$

**Ejemplo 2.10 (Crecimiento con períodos de distinta duración):**
Un capital crece con un factor anual de $1.10$ durante $2$ años y luego con un factor anual de $1.05$ durante $3$ años. Los pesos son las duraciones, $w_1 = 2$ y $w_2 = 3$:

$$
G_w = \left( 1.10^2 \cdot 1.05^3 \right)^{1/5} = 1.4007^{1/5} \approx 1.0697
$$

El crecimiento anual medio es, por tanto, aproximadamente $6.97\%$. La media aritmética ponderada de las tasas, $(2 \cdot 10 + 3 \cdot 5)/5 = 7\%$, lo sobreestima.

**Ejemplo 2.11 (Velocidad media con tramos de distinta longitud):**
Un vehículo recorre $120\ \text{km}$ a $60\ \text{km/h}$ y luego $80\ \text{km}$ a $40\ \text{km/h}$. Como la velocidad media es la distancia total entre el tiempo total, y el tiempo en el tramo $i$ es $d_i/v_i$, se trata de la media armónica de las velocidades ponderada por las distancias $d_i$:

$$
H_w = \dfrac{d_1 + d_2}{\dfrac{d_1}{v_1} + \dfrac{d_2}{v_2}} = \dfrac{200}{2 + 2} = 50\ \text{km/h}
$$

**Aplicaciones:**

- **Finanzas:** el rendimiento anual medio de una inversión con períodos de distinta duración.
- **Física y transporte:** la velocidad media y el rendimiento medio de combustible (kilómetros por litro) en recorridos con tramos de distinta longitud.

### 2.6 Media cuadrática (RMS)

En muchos fenómenos el signo de una cantidad no importa, solo su magnitud: la tensión de una corriente alterna oscila entre valores positivos y negativos y su media aritmética es cero, aunque la corriente transporte energía. La **media cuadrática** (en inglés, *root mean square*, RMS) resume la magnitud típica de los datos sin que los signos se cancelen.

**Definición 2.8 (Media cuadrática):**
Dada una muestra $\mathbf{x} \in \mathbb{R}^n$, la **media cuadrática** es:

$$
\text{RMS} = \sqrt{\dfrac{1}{n} \sum_{i=1}^{n} x_i^2}
$$

**Proposición 2.4 (Relación con la media y la dispersión):**
Se cumple:

$$
\text{RMS}^2 = \bar{x}^2 + \dfrac{1}{n} \sum_{i=1}^{n} (x_i - \bar{x})^2
$$

En particular, $\text{RMS} \geq |\bar{x}|$, con igualdad si y solo si todos los datos son iguales.

**Demostración:**
Se aplica el Teorema 2.3 con $c = 0$:

$$
\sum_{i=1}^{n} x_i^2 = \sum_{i=1}^{n} (x_i - \bar{x})^2 + n\bar{x}^2
$$

Dividiendo entre $n$ se obtiene la igualdad. El segundo sumando de la derecha es no negativo y se anula si y solo si $x_i = \bar{x}$ para todo $i$.
$\blacksquare$

**Ejemplo 2.12 (Errores de medición):**
Los errores de un instrumento en cinco mediciones son $(-2, -1, 0, 1, 2)$. Su media es $\bar{x} = 0$, lo que oculta que el instrumento se equivoca, mientras que:

$$
\text{RMS} = \sqrt{\dfrac{4 + 1 + 0 + 1 + 4}{5}} = \sqrt{2} \approx 1.41
$$

**Aplicaciones:**

- **Ingeniería eléctrica:** la tensión eficaz de una corriente alterna es el valor RMS de la tensión; para una señal sinusoidal de amplitud $V_0$, equivale a $V_0/\sqrt{2}$.
- **Aprendizaje automático y estadística:** la raíz del error cuadrático medio (RMSE) mide el error típico de las predicciones de un modelo.

### 2.7 Mediana

La media es sensible a valores extremos porque cada dato influye en ella con el mismo peso. La **mediana** adopta otro criterio: es el valor que deja la mitad de los datos por debajo y la mitad por encima. Para hallarla no se suman los datos, solo se ordenan, y por eso un valor extremo no la desplaza más allá de su posición en el orden.

**Definición 2.9 (Mediana):**
Dada una muestra con estadísticos de orden $x_{(1)} \leq \cdots \leq x_{(n)}$, la **mediana** $Me$ es:

$$
Me = \begin{cases} x_{((n+1)/2)} & \text{si } n \text{ es impar,} \\[1ex] \dfrac{1}{2} \left[ x_{(n/2)} + x_{(n/2 + 1)} \right] & \text{si } n \text{ es par.} \end{cases}
$$

**Teorema 2.6 (La mediana minimiza el error absoluto):**
La función $c \mapsto \sum_{i=1}^{n} |x_i - c|$ alcanza su mínimo en $c = Me$. Más precisamente:

- si $n$ es impar, el mínimo se alcanza únicamente en $c = x_{((n+1)/2)}$;
- si $n$ es par, el mínimo se alcanza en todo $c \in [x_{(n/2)}, x_{(n/2+1)}]$, y la mediana es el punto medio de ese intervalo.

**Demostración:**
Sea $s = \lfloor n/2 \rfloor$. Para cada $i \in \{1, \ldots, s\}$ se agrupan los datos $x_{(i)}$ y $x_{(n+1-i)}$. Por la desigualdad triangular:

$$
\lvert x_{(i)} - c \rvert + \lvert x_{(n+1-i)} - c \rvert \geq (x_{(n+1-i)} - c) + (c - x_{(i)}) = x_{(n+1-i)} - x_{(i)}
$$

con igualdad si y solo si $x_{(i)} \leq c \leq x_{(n+1-i)}$. Sumando sobre $i = 1, \ldots, s$, y añadiendo el término central $|x_{((n+1)/2)} - c|$ cuando $n$ es impar, se obtiene:

$$
\sum_{i=1}^{n} |x_i - c| \geq C + \mathbb{1}_{\{n \text{ impar}\}} \cdot |x_{((n+1)/2)} - c|, \qquad C = \sum_{i=1}^{s} (x_{(n+1-i)} - x_{(i)})
$$

La constante $C$ no depende de $c$. Los intervalos $[x_{(i)}, x_{(n+1-i)}]$ están anidados, y el más pequeño es el correspondiente a $i = s$. La igualdad en la cota anterior se da si y solo si $c$ pertenece a ese intervalo más pequeño.

- Si $n$ es par, el lado derecho es la constante $C$, y el mínimo $C$ se alcanza exactamente cuando $c \in [x_{(n/2)}, x_{(n/2+1)}]$.
- Si $n$ es impar, el lado derecho es mínimo (igual a $C$) solo en $c = x_{((n+1)/2)}$, y ese valor pertenece al intervalo más pequeño, por lo que allí se alcanza la igualdad. Para cualquier otro $c$, la suma es al menos $C + |x_{((n+1)/2)} - c| > C$.

En ambos casos, $Me$ es un punto donde se alcanza el mínimo.
$\blacksquare$

> **Observación:** los Teoremas 2.3 y 2.6 muestran una correspondencia: la media minimiza $\sum_i (x_i - c)^2$ y la mediana minimiza $\sum_i |x_i - c|$. Los valores mínimos que se alcanzan, $\tfrac{1}{n}\sum_i (x_i - \bar{x})^2$ y $\tfrac{1}{n}\sum_i |x_i - Me|$, no son medidas de tendencia central sino de dispersión (la varianza y la desviación absoluta respecto de la mediana), que se estudian en la Sección 4.

Para medir cuánto soporta un estadístico la presencia de datos erróneos se introduce el siguiente concepto.

**Definición 2.10 (Punto de ruptura muestral):**
Sea $T$ un estadístico y $\mathbf{x}$ una muestra de tamaño $n$. El **punto de ruptura** de $T$ en $\mathbf{x}$ es la menor proporción $m/n$ tal que, reemplazando $m$ datos de $\mathbf{x}$ por valores arbitrarios, el valor de $T$ puede hacerse arbitrariamente grande en valor absoluto.

**Proposición 2.5 (Puntos de ruptura de la media y la mediana):**
Para una muestra de tamaño $n$:

$$
\varepsilon^*(\bar{x}) = \dfrac{1}{n}, \qquad \varepsilon^*(Me) = \dfrac{\lceil n/2 \rceil}{n}
$$

Cuando $n \to \infty$, el punto de ruptura de la media tiende a $0$ y el de la mediana a $\tfrac{1}{2}$.

**Demostración:**
*Media.* Si se reemplaza un solo dato por un valor $M$, la media vale $\bar{y} = \tfrac{1}{n}(M + S')$, donde $S'$ es la suma de los $n-1$ datos restantes. Al hacer $M \to \infty$, $|\bar{y}| \to \infty$. Por tanto, basta un dato: $\varepsilon^*(\bar{x}) = 1/n$.

*Mediana.* Sean $a = \lfloor (n+1)/2 \rfloor$ y $b = \lceil (n+1)/2 \rceil$, de modo que $Me = \tfrac{1}{2}(y_{(a)} + y_{(b)})$ para la muestra modificada $\mathbf{y}$. Se observa que $n - b + 1 = a = \lceil n/2 \rceil$. Para que $y_{(b)}$ supere $\max \mathbf{x}$ deben existir al menos $n - b + 1 = \lceil n/2 \rceil$ valores de $\mathbf{y}$ mayores que $\max \mathbf{x}$, y estos solo pueden provenir de datos reemplazados. De forma análoga, para que $y_{(a)}$ sea menor que $\min \mathbf{x}$ se necesitan al menos $a = \lceil n/2 \rceil$ datos reemplazados. Por tanto, si se reemplazan menos de $\lceil n/2 \rceil$ datos, $Me$ permanece en $[\min \mathbf{x}, \max \mathbf{x}]$ y no puede hacerse arbitrariamente grande. Con exactamente $\lceil n/2 \rceil$ datos reemplazados por $M \to \infty$, $y_{(b)} = M$ y $Me \to \infty$.
$\blacksquare$

**Ejemplo 2.13 (Efecto de un valor atípico):**
Sea $\mathbf{x} = (1, 3, 4, 5, 7)$, con $\bar{x} = 4$ y $Me = 4$. Si el último dato se reemplaza por $700$ (por ejemplo, por un error de digitación), se obtiene $\mathbf{y} = (1, 3, 4, 5, 700)$ y:

$$
\bar{y} = \dfrac{713}{5} = 142.6, \qquad Me = 4
$$

La media pasó de $4$ a $142.6$, mientras que la mediana no cambió.

> **Observación:** la mediana solo requiere ordenar los datos, no operar con ellos, por lo que está definida para variables ordinales (por ejemplo, un nivel de satisfacción con categorías ordenadas: "Malo", "Regular", "Bueno"), para las cuales la media no tiene sentido. Para datos agrupados, la mediana se calcula por interpolación y se trata junto con los cuantiles en la Sección 3.

**Aplicaciones:**

- **Economía:** el ingreso mediano describe mejor al hogar típico que el ingreso medio, que es arrastrado por los ingresos muy altos.
- **Salud y ciencias sociales:** el tiempo mediano de supervivencia y la edad mediana de una población.
- **Estadística robusta:** la mediana es el estimador de localización resistente por excelencia.

### 2.8 Moda

A diferencia de la media y la mediana, que buscan un centro, la **moda** busca el valor más común: aquel en torno al cual los datos se repiten más. Es la única medida de tendencia central que tiene sentido para variables cualitativas nominales, como el tipo sanguíneo más frecuente en un banco de sangre.

En la Clase 4 la moda se definió para una distribución como un máximo local estricto de su densidad. Aquí se define para una muestra, distinguiendo dos casos.

**Definición 2.11 (Moda de datos a granel):**
Sea $\mathbf{x}$ una muestra y, para cada valor distinto $v$ que aparece en ella, sea $n(v) = \#\{ i : x_i = v \}$ su frecuencia absoluta. Una **moda** de la muestra es todo valor $v$ que maximiza $n(v)$:

$$
Mo \in \arg\max_{v \in \text{Rec}(X)} n(v)
$$

El conjunto de modas puede tener más de un elemento; si todos los valores tienen la misma frecuencia, la muestra no tiene moda en sentido práctico.

**Ejemplo 2.14 (Datos de la Clase 3):**
Para $\mathbf{x} = (2, 2, 2, 5, 5, 5, 5, 5, 5, 5, 7, 7, 7, 7)$ se tiene $n(2) = 3$, $n(5) = 7$ y $n(7) = 4$, de modo que $Mo = 5$.

En variables continuas medidas con precisión, es poco probable que dos observaciones coincidan exactamente, y la moda de datos a granel pierde significado. En las 50 mediciones de la Clase 3, por ejemplo, los valores $0.03$, $0.22$, $0.29$ y $0.86$ aparecen cada uno dos veces, y esas coincidencias son accidentales. Para esos casos se recurre a los datos agrupados.

**Definición 2.12 (Clase modal y moda de datos agrupados):**
Para datos agrupados en intervalos de amplitud constante $a$, la **clase modal** $I_j = [L_j, L_j + a)$ es la de mayor frecuencia $n_j$. Se definen:

$$
\Delta_1 = n_j - n_{j-1}, \qquad \Delta_2 = n_j - n_{j+1}
$$

donde $n_{j-1}$ y $n_{j+1}$ son las frecuencias de las clases vecinas (con frecuencia $0$ si la clase modal es la primera o la última). Si $\Delta_1 + \Delta_2 > 0$, la **moda de los datos agrupados** es:

$$
Mo = L_j + \dfrac{\Delta_1}{\Delta_1 + \Delta_2} \cdot a
$$

**Proposición 2.6 (Deducción de la fórmula de la moda agrupada):**
La moda de la Definición 2.12 es la abscisa del punto de intersección de dos segmentos del histograma: el que une el extremo superior izquierdo de la barra anterior con el de la barra modal, y el que une el extremo superior izquierdo de la barra modal con el de la barra siguiente.

**Demostración:**
Sea $t = (x - L_j)/a \in [0, 1]$ la posición relativa dentro de la clase modal. El primer segmento va de $(L_j, n_{j-1})$ a $(L_j + a, n_j)$, y el segundo, de $(L_j, n_j)$ a $(L_j + a, n_{j+1})$. Sus alturas son, respectivamente:

$$
y_1(t) = n_{j-1} + \Delta_1 t, \qquad y_2(t) = n_j - \Delta_2 t
$$

Igualando $y_1(t) = y_2(t)$:

$$
\begin{align}
n_{j-1} + \Delta_1 t &= n_j - \Delta_2 t \\
(\Delta_1 + \Delta_2)\, t &= n_j - n_{j-1} = \Delta_1 \\
t &= \dfrac{\Delta_1}{\Delta_1 + \Delta_2}
\end{align}
$$

Por tanto, $x = L_j + t\,a = L_j + \dfrac{\Delta_1}{\Delta_1 + \Delta_2}\, a$.
$\blacksquare$

> **Nota:** si los intervalos tienen amplitudes distintas, las frecuencias $n_i$ deben sustituirse por las densidades $n_i/a_i$ al determinar la clase modal y al calcular $\Delta_1$ y $\Delta_2$.

**Ejemplo 2.15 (Moda agrupada):**
En la tabla de las 50 mediciones, la clase modal es $[0.03, 0.53)$, con $n_1 = 19$ y amplitud $a = 0.50$. Al ser la primera clase, se toma $n_0 = 0$. Entonces $\Delta_1 = 19 - 0 = 19$ y $\Delta_2 = 19 - 9 = 10$:

$$
Mo = 0.03 + \dfrac{19}{19 + 10} \cdot 0.50 \approx 0.03 + 0.328 = 0.358
$$

**Aplicaciones:**

- **Mercadotecnia y operaciones:** la talla o el producto más vendido.
- **Ciencias sociales:** la categoría más frecuente en variables nominales, para las cuales no existe ni media ni mediana.
- **Análisis de distribuciones:** la presencia de varias modas sugiere la mezcla de subpoblaciones, como se vio en la Clase 4.

### 2.9 Media recortada y media winsorizada

La media usa todos los datos, y por eso un solo valor atípico la desplaza; la mediana ignora casi todos los datos, y por eso se mantiene estable pero desperdicia información. Entre ambos extremos existe una solución intermedia: descartar una proporción fija de los datos más pequeños y de los más grandes, y promediar el resto. Es lo que se hace en las competencias deportivas con jurado, donde se elimina la puntuación más alta y la más baja antes de promediar las demás.

**Definición 2.13 (Media recortada):**
Sea $\alpha \in [0, \tfrac{1}{2})$ y $g = \lfloor \alpha n \rfloor$. La **media recortada al $100\alpha\%$** es el promedio de los datos ordenados una vez descartados los $g$ menores y los $g$ mayores:

$$
\bar{x}_\alpha = \dfrac{1}{n - 2g} \sum_{i=g+1}^{n-g} x_{(i)}
$$

Como $2g \leq 2\alpha n < n$, siempre quedan al menos $n - 2g \geq 1$ datos. Los valores usuales son $\alpha = 0.05$, $0.10$ y $0.20$.

**Definición 2.14 (Media winsorizada):**
En lugar de descartar los $g$ menores y los $g$ mayores, se los reemplaza por el dato más cercano que se conserva, y se promedian los $n$ datos resultantes:

$$
\bar{x}_\alpha^{W} = \dfrac{1}{n} \left[ g\,x_{(g+1)} + \sum_{i=g+1}^{n-g} x_{(i)} + g\,x_{(n-g)} \right]
$$

**Proposición 2.7 (Propiedades de la media recortada):**

1. Para $\alpha = 0$, $\bar{x}_\alpha = \bar{x}$.
2. Para el recorte máximo, $g = \lfloor (n-1)/2 \rfloor$, $\bar{x}_\alpha = Me$.
3. $x_{(g+1)} \leq \bar{x}_\alpha \leq x_{(n-g)}$.
4. El punto de ruptura (Definición 2.10) de $\bar{x}_\alpha$ es $(g+1)/n$, que tiende a $\alpha$ cuando $n \to \infty$.

**Demostración:**
1. Si $\alpha = 0$, entonces $g = 0$ y la suma recorre todos los datos.

2. Si $n$ es impar, $g = (n-1)/2$ y solo queda $x_{((n+1)/2)}$; si $n$ es par, $g = (n-2)/2$ y quedan $x_{(n/2)}$ y $x_{(n/2+1)}$, cuyo promedio es $Me$.

3. Es un promedio de números que están entre $x_{(g+1)}$ y $x_{(n-g)}$.

4. Sea $\mathbf{y}$ la muestra obtenida al reemplazar $m$ datos por valores arbitrarios. Si $m \leq g$, el valor $y_{(g+1)}$ no puede ser menor que $x_{(1)}$, pues para ello harían falta al menos $g+1$ valores menores que $x_{(1)}$, y solo los datos reemplazados podrían serlo. Análogamente, $y_{(n-g)} \leq x_{(n)}$. Por tanto, todos los términos de la suma recortada están en $[x_{(1)}, x_{(n)}]$ y $\bar{x}_\alpha$ permanece acotada. Si $m = g+1$ y esos datos se reemplazan por un valor $M \to \infty$, los $g+1$ valores mayores de $\mathbf{y}$ son iguales a $M$, de modo que $y_{(n-g)} = M$ pertenece a la suma y $\bar{x}_\alpha \to \infty$.
$\blacksquare$

**Ejemplo 2.16 (Un valor atípico):**
Sea $\mathbf{x} = (2, 3, 3, 4, 5, 5, 6, 7, 8, 90)$, con $n = 10$ y $\alpha = 0.10$, de modo que $g = 1$. Se descartan $2$ y $90$:

$$
\bar{x} = \dfrac{133}{10} = 13.3, \qquad \bar{x}_{0.10} = \dfrac{3 + 3 + 4 + 5 + 5 + 6 + 7 + 8}{8} = \dfrac{41}{8} = 5.125, \qquad Me = 5
$$

La media winsorizada reemplaza $2$ por $3$ y $90$ por $8$, y da $\bar{x}_{0.10}^{W} = 52/10 = 5.2$. La media aritmética es arrastrada por el valor $90$, mientras que las otras tres medidas permanecen cerca del centro de los datos.

> **Observación:** el recorte $\alpha$ es un compromiso. Un valor mayor aumenta la resistencia a valores atípicos (por la Proposición 2.7, el punto de ruptura tiende a $\alpha$) pero descarta más información. Con $\alpha = 0.25$ se obtiene la media intercuartílica, que promedia solo la mitad central de los datos.

**Aplicaciones:**

- **Deportes y concursos con jurado:** la puntuación final descarta los valores extremos de los jueces para reducir el efecto de un juicio sesgado.
- **Estadística robusta:** es una alternativa que conserva más información que la mediana y es mucho menos sensible que la media a datos erróneos.

### 2.10 Medias de potencias (Opcional)

Las medias armónica, geométrica, aritmética y cuadrática no son medidas independientes: forman una familia que se obtiene variando un único parámetro. Reconocerlo permite ordenarlas y compararlas.

**Definición 2.15 (Media de potencias de orden $p$):**
Para $\mathbf{x} \in \mathbb{R}^n_{>0}$ y $p \in \mathbb{R}$, la **media de potencias de orden $p$** es:

$$
M_p = \left( \dfrac{1}{n} \sum_{i=1}^{n} x_i^p \right)^{1/p} \quad (p \neq 0), \qquad M_0 = G
$$

**Proposición 2.8 (Casos particulares):**
$M_{-1} = H$, $M_1 = \bar{x}$, $M_2 = \text{RMS}$, y además:

$$
\lim_{p \to 0} M_p = G, \qquad \lim_{p \to \infty} M_p = \max_i x_i, \qquad \lim_{p \to -\infty} M_p = \min_i x_i
$$

**Demostración:**
Los casos $p = -1, 1, 2$ se obtienen directamente de las definiciones.

*Límite en $p \to 0$.* Sea $\varphi(p) = \ln\left( \tfrac{1}{n} \sum x_i^p \right)$. Entonces $\varphi(0) = 0$ y $\ln M_p = \varphi(p)/p$. Por definición de derivada, $\lim_{p \to 0} \varphi(p)/p = \varphi'(0)$, y:

$$
\varphi'(0) = \left. \dfrac{\sum x_i^p \ln x_i}{\sum x_i^p} \right|_{p=0} = \dfrac{1}{n} \sum_{i=1}^{n} \ln x_i = \ln G
$$

*Límite en $p \to \infty$.* Sea $x_{\max} = \max_i x_i$. Entonces $M_p = x_{\max} \left( \tfrac{1}{n} \sum (x_i/x_{\max})^p \right)^{1/p}$. La suma interior está entre $1/n$ (en el término $1$ que no se anula) y $1$, así que el factor está entre $(1/n)^{1/p}$ y $1$, y ambos extremos tienden a $1$.

*Límite en $p \to -\infty$.* Es análogo, factorizando $x_{\min} = \min_i x_i$: ahora $(x_i/x_{\min})^p \leq 1$ para $p < 0$ y se obtiene el mismo argumento.
$\blacksquare$

**Teorema 2.7 (Desigualdad entre medias):**
Para datos positivos:

$$
H \leq G \leq \bar{x} \leq \text{RMS}
$$

y cada desigualdad es una igualdad si y solo si todos los datos son iguales.

**Demostración:**
*$\bar{x} \leq \text{RMS}$:* es la Proposición 2.4.

*$G \leq \bar{x}$:* se usa la desigualdad $\ln t \leq t - 1$ para $t > 0$, con igualdad si y solo si $t = 1$. Aplicada con $t = x_i/\bar{x}$ y sumando:

$$
\begin{align}
\sum_{i=1}^{n} \ln \dfrac{x_i}{\bar{x}} &\leq \sum_{i=1}^{n} \left( \dfrac{x_i}{\bar{x}} - 1 \right) = \dfrac{n\bar{x}}{\bar{x}} - n = 0 \\
\sum_{i=1}^{n} \ln x_i - n \ln \bar{x} &\leq 0 \\
\ln G &\leq \ln \bar{x}
\end{align}
$$

con igualdad si y solo si $x_i = \bar{x}$ para todo $i$.

*$H \leq G$:* se aplica la desigualdad anterior a los datos $y_i = 1/x_i$. La media geométrica de los $y_i$ es $1/G$ y su media aritmética es $1/H$, de modo que $1/G \leq 1/H$, es decir, $H \leq G$.
$\blacksquare$

> **Observación:** en general, $M_p$ es una función creciente de $p$. Esa propiedad se demuestra con la desigualdad de Jensen, que se verá en el curso de probabilidad, y contiene al Teorema 2.7 como caso particular.

**Ejemplo 2.17 (Medias de potencias de 1 y 4):**
Para $\mathbf{x} = (1, 4)$: $H = 2/(1 + 1/4) = 1.6$, $G = \sqrt{4} = 2$, $\bar{x} = 2.5$ y $\text{RMS} = \sqrt{(1 + 16)/2} \approx 2.92$. Se verifica $1.6 \leq 2 \leq 2.5 \leq 2.92$.

### 2.11 Qué es un promedio (Opcional)

Hasta aquí se han llamado "medias" a varias funciones de los datos, pero conviene precisar qué propiedades mínimas se espera de cualquier medida de tendencia central. Una exigencia natural es que el valor reportado no pueda quedar fuera del rango de los datos, y que no dependa del orden en que se registraron.

**Definición 2.16 (Promedio):**
Una función $f: \mathbb{R}^n \to \mathbb{R}$ es un **promedio** si cumple:

1. **Internalidad:** $\min_i x_i \leq f(\mathbf{x}) \leq \max_i x_i$ para todo $\mathbf{x}$.
2. **Simetría:** $f(x_{\sigma(1)}, \ldots, x_{\sigma(n)}) = f(x_1, \ldots, x_n)$ para toda permutación $\sigma$ de $\{1, \ldots, n\}$.

**Proposición 2.9 (Idempotencia):**
Todo promedio cumple $f(k, k, \ldots, k) = k$.

**Demostración:**
Si $x_1 = \cdots = x_n = k$, entonces $\min_i x_i = \max_i x_i = k$ y, por internalidad, $k \leq f(k, \ldots, k) \leq k$.
$\blacksquare$

La media aritmética, la mediana, la media geométrica y la media armónica son promedios, esta última y la geométrica sobre datos positivos. La media cuadrática, en cambio, no lo es en general: para $\mathbf{x} = (-1, -1)$ se tiene $\text{RMS} = 1 > \max_i x_i = -1$. Esto es coherente con su propósito, ya que el RMS mide magnitud y no ubicación.

**Ejemplo 2.18 (Funciones que no son promedios):**
Las dos condiciones de la Definición 2.16 son independientes. La función $f(\mathbf{x}) = x_1$ (el primer dato registrado) cumple la internalidad, pues $x_1$ está entre el mínimo y el máximo, pero no la simetría: $f(2, 3) = 2$ y $f(3, 2) = 3$, de modo que el resultado depende del orden en que se registraron los datos. La función $g(\mathbf{x}) = \max_i x_i + 1$ cumple la simetría, pues no depende del orden, pero no la internalidad: $g(2, 3) = 4 > 3$. Ninguna de las dos es un promedio. En cambio, el punto medio del rango, $\tfrac{1}{2}\left( x_{(1)} + x_{(n)} \right)$, sí lo es: queda entre el mínimo y el máximo y no depende del orden.

### 2.12 Media aritmético-geométrica (Opcional)

Se ha visto que $G \leq \bar{x}$ para cualesquiera datos positivos. ¿Qué ocurre al aplicar ambas medias de forma alternada? Dados dos números positivos, se reemplaza el par por su media aritmética y su media geométrica, y se repite el proceso. Ambos valores se acercan entre sí con una rapidez extraordinaria y convergen a un mismo número, la **media aritmético-geométrica**. El primer algoritmo con este par de sucesiones aparece en la obra de Joseph-Louis Lagrange, y fue Carl Friedrich Gauss quien analizó sus propiedades y, en 1799, la relacionó con las integrales elípticas. Es más una curiosidad matemática que una herramienta descriptiva, pero está en el corazón del cálculo de integrales elípticas.

**Definición 2.17 (Media aritmético-geométrica):**
Dados $a_0 \geq b_0 > 0$, se define recursivamente:

$$
a_{k+1} = \dfrac{a_k + b_k}{2}, \qquad b_{k+1} = \sqrt{a_k b_k}
$$

El límite común de ambas sucesiones, que existe por la Proposición 2.10, se denomina **media aritmético-geométrica** de $a_0$ y $b_0$ y se denota $M(a_0, b_0)$.

**Proposición 2.10 (Convergencia y cotas):**
Las sucesiones $(a_k)$ y $(b_k)$ convergen a un límite común $M(a_0, b_0)$ y se cumple:

$$
\sqrt{a_0 b_0} \leq M(a_0, b_0) \leq \dfrac{a_0 + b_0}{2}
$$

con igualdad si y solo si $a_0 = b_0$.

**Demostración:**
Si $a_0 = b_0$, todos los términos de ambas sucesiones son iguales a $a_0$, y las cotas son igualdades. Para el caso general, por la desigualdad entre medias aritmética y geométrica (Teorema 2.7 con $n = 2$), $b_{k} \leq a_{k}$ para todo $k$. Entonces $a_{k+1} = (a_k + b_k)/2 \leq a_k$ y $b_{k+1} = \sqrt{a_k b_k} \geq \sqrt{b_k b_k} = b_k$. Así, $(a_k)$ es decreciente y acotada inferiormente por $b_0 > 0$, y $(b_k)$ es creciente y acotada superiormente por $a_0$; ambas convergen. Además, como $b_{k+1} \geq b_k$:

$$
a_{k+1} - b_{k+1} \leq a_{k+1} - b_k = \dfrac{a_k - b_k}{2}
$$

de modo que $a_k - b_k \to 0$ y los dos límites coinciden. Por la monotonía, para $k \geq 1$ se tiene $b_1 \leq b_k \leq M \leq a_k \leq a_1$, y $b_1 = \sqrt{a_0 b_0}$, $a_1 = (a_0 + b_0)/2$. Si $a_0 > b_0$, entonces $b_1 < a_1$ y, de $a_2 < a_1$ y $b_2 > b_1$, ambas desigualdades son estrictas.
$\blacksquare$

**Ejemplo 2.19 (Media aritmético-geométrica de 1 y 4):**
Con $a_0 = 4$ y $b_0 = 1$, se obtiene:

| $k$ | $a_k$ | $b_k$ |
|:---:|:-----:|:-----:|
| 0 | $4$ | $1$ |
| 1 | $2.5$ | $2$ |
| 2 | $2.25$ | $2.2360680$ |
| 3 | $2.2430340$ | $2.2430232$ |
| 4 | $2.2430286$ | $2.2430286$ |

De modo que $M(1, 4) \approx 2.24303$. Esto es consistente con el Ejemplo 2.17, donde para los mismos datos $G = 2$ y $\bar{x} = 2.5$. Cada paso duplica aproximadamente el número de cifras decimales correctas, de ahí su utilidad en el cálculo numérico.

> **Observación:** la media aritmético-geométrica se relaciona con una integral elíptica completa de primera especie:
>
> $$
> \dfrac{1}{M(a, b)} = \dfrac{2}{\pi} \int_0^{\pi/2} \dfrac{d\theta}{\sqrt{a^2 \cos^2 \theta + b^2 \sin^2 \theta}}
> $$
>
> Con $a = 4$ y $b = 1$, la integral da $0.44583$, que coincide con $1/M(1, 4)$. La demostración de esta identidad requiere un cambio de variable en integrales y se difiere al curso de cálculo. Gracias a ella, esa integral se calcula con unas pocas iteraciones. Aparece, por ejemplo, en el período de un péndulo de amplitud arbitraria $\theta_0$, que resulta ser $T = \dfrac{2\pi}{M\left(1, \cos\frac{\theta_0}{2}\right)} \sqrt{\dfrac{\ell}{g}}$. El perímetro de una elipse, en cambio, requiere la integral completa de segunda especie, que también puede calcularse con la media aritmético-geométrica, aunque mediante otra fórmula.

### 2.13 Mediana geométrica (Opcional)

La mediana está definida para datos de una sola dimensión, pues necesita ordenarlos. Cuando cada observación es un punto $\mathbf{p}_i \in \mathbb{R}^k$ (por ejemplo, las ubicaciones de $n$ clientes sobre un mapa), no existe un orden natural. La generalización se apoya en el Teorema 2.6: en una dimensión, la mediana es el punto que minimiza la suma de las distancias a los datos.

**Definición 2.18 (Mediana geométrica):**
Dados los puntos $\mathbf{p}_1, \ldots, \mathbf{p}_n \in \mathbb{R}^k$, la **mediana geométrica** (o mediana espacial) es un punto $\mathbf{m} \in \mathbb{R}^k$ que minimiza la suma de las distancias euclidianas:

$$
\mathbf{m} \in \arg\min_{\mathbf{m} \in \mathbb{R}^k} \sum_{i=1}^{n} \| \mathbf{p}_i - \mathbf{m} \|_2
$$

Para $k = 1$, la Definición 2.18 se reduce a la mediana usual, por el Teorema 2.6. Para $k \geq 2$ en general no existe una fórmula cerrada, y se calcula con métodos iterativos como el algoritmo de Weiszfeld (1937).

**Ejemplo 2.20 (Mediana geométrica en el plano):**
Se consideran los vértices de un rectángulo, $(0, 0)$, $(4, 0)$, $(4, 3)$ y $(0, 3)$. Para un punto $\mathbf{m}$ cualquiera, la desigualdad triangular da $\|\mathbf{p}_1 - \mathbf{m}\| + \|\mathbf{p}_3 - \mathbf{m}\| \geq \|\mathbf{p}_1 - \mathbf{p}_3\| = 5$, con igualdad si y solo si $\mathbf{m}$ está sobre la diagonal que une $\mathbf{p}_1$ y $\mathbf{p}_3$; lo mismo vale para la otra diagonal. La suma total es, por tanto, al menos $10$, y se alcanza únicamente en el punto donde se cortan ambas diagonales, $\mathbf{m} = (2,\ 1.5)$, que es la mediana geométrica.

Con los puntos $(0, 0)$, $(1, 0)$ y $(10, 0)$, situados sobre una recta, la mediana geométrica es $(1, 0)$, la mediana de las abscisas, mientras que el centroide, $(3.67,\ 0)$, es arrastrado por el punto lejano.

**Aplicaciones:**

- **Logística:** la ubicación de un centro de distribución que minimiza la distancia total a los clientes (problema de Fermat-Weber).
- **Estadística robusta multivariada:** un estimador del centro de una nube de puntos, resistente a valores atípicos.

### 2.14 Qué medida usar: las más importantes

En esta sección aparecieron muchas medias, pero en la práctica unas pocas concentran casi todo el uso. La elección depende de tres factores: la escala de medición de la variable, la forma de la distribución y la presencia de valores atípicos.

| Medida | Cuándo se usa | Nivel de importancia |
|:-------|:--------------|:---------------------|
| Media aritmética | Datos numéricos con distribución aproximadamente simétrica y sin valores atípicos relevantes. Es la base de la varianza y de la mayor parte de la inferencia estadística. | Fundamental |
| Mediana | Datos ordinales, distribuciones asimétricas o con valores atípicos. | Fundamental |
| Moda | Variables cualitativas nominales; valor más frecuente. | Fundamental |
| Media ponderada | Observaciones de importancia desigual y datos agrupados. | Frecuente |
| Media recortada | Compromiso entre la media y la mediana cuando pueden existir datos erróneos. | Frecuente en análisis robusto |
| Media geométrica (y ponderada) | Factores de crecimiento, tasas e índices, con datos positivos. | Según el contexto |
| Media armónica (y ponderada) | Razones con numerador fijo: velocidades con distancias dadas, rendimientos. | Según el contexto |
| Media cuadrática (RMS) | Magnitud de cantidades con signo; error típico de un modelo. | Según el contexto |
| Medias de potencias, media aritmético-geométrica, mediana geométrica, definición de promedio | Marco teórico y curiosidades matemáticas. | Opcional |

La escala de medición restringe las medidas admisibles:

| Escala | Medidas admisibles |
|:-------|:-------------------|
| Nominal | Moda |
| Ordinal | Moda y mediana (y los cuantiles) |
| De intervalo | Además, la media aritmética y la media recortada |
| De razón | Todas, incluidas las medias geométrica y armónica, que dependen de un cero absoluto |

Como regla práctica, conviene calcular siempre la media y la mediana. Si son similares, los datos son aproximadamente simétricos y sin valores atípicos influyentes, y cualquiera de las dos resume bien el centro. Si difieren mucho, la distribución es asimétrica o contiene valores extremos. En una distribución con sesgo positivo, la media es mayor que la mediana, y en una con sesgo negativo, es menor (Clase 4, Sección 5.2); en esos casos la mediana (o una media recortada) describe mejor el valor típico.

---

## 3. Medidas de posición: cuantiles

La mediana divide los datos en dos mitades iguales. Con la misma idea se puede preguntar por otras proporciones: ¿qué valor deja por debajo al 25% de los datos?, ¿y al 90%? Un estudiante que obtiene el percentil 85 en un examen sabe que superó a aproximadamente el 85% de sus compañeros, sin necesidad de conocer su nota exacta ni la del resto. Los **cuantiles** generalizan la mediana a cualquier proporción y son la herramienta básica para describir la posición de un dato dentro de un conjunto.

> **Nota histórica:** en el siglo XIX, Francis Galton popularizó el uso de la mediana y los cuartiles para describir distribuciones empíricas, en el contexto de sus estudios sobre la herencia de características físicas. Hoy los cuantiles aparecen en programas como Excel y Python, pero cada uno los calcula con una convención ligeramente distinta, como se verá en esta sección.

### 3.1 Definición de cuantil y no unicidad

Sea $F_n(x) = \tfrac{1}{n} \#\{ i : x_i \leq x \}$ la función de distribución empírica de la muestra (Clase 3, Sección 4). Un cuantil de orden $p$ es un valor que deja, a lo sumo, una proporción $p$ de datos estrictamente por debajo y, al menos, una proporción $p$ por debajo o iguales a él.

**Definición 3.1 (Cuantil muestral de orden $p$):**
Sea $\mathbf{x} = (x_1, \ldots, x_n)$ una muestra y $p \in (0, 1)$. Un número $q \in \mathbb{R}$ es un **cuantil de orden $p$** de la muestra si:

$$
\#\{ i : x_i \leq q \} \geq np \quad \text{y} \quad \#\{ i : x_i \geq q \} \geq n(1 - p)
$$

> **Observación:** la segunda condición equivale a $\#\{ i : x_i < q \} \leq np$. Por tanto, $q$ es un cuantil de orden $p$ si y solo si $F_n(q^-) \leq p \leq F_n(q)$, donde $F_n(q^-)$ es el límite de $F_n$ por la izquierda. En palabras: el cuantil es una inversa generalizada de la función de distribución empírica.

**Proposición 3.1 (Caracterización del cuantil muestral):**
Sea $p \in (0, 1)$.

1. Si $np$ no es entero, existe un único cuantil de orden $p$: $q = x_{(\lceil np \rceil)}$.
2. Si $np$ es entero, el conjunto de cuantiles de orden $p$ es el intervalo $[x_{(np)}, x_{(np+1)}]$.

**Demostración:**
Sea $j$ un entero con $1 \leq j \leq n$. Se tienen las equivalencias:

- $\#\{ i : x_i \leq q \} \geq j$ si y solo si $q \geq x_{(j)}$, pues los $j$ menores datos son $x_{(1)}, \ldots, x_{(j)}$.
- $\#\{ i : x_i \geq q \} \geq n - j + 1$ si y solo si $q \leq x_{(j)}$, pues los $n - j + 1$ mayores datos son $x_{(j)}, \ldots, x_{(n)}$.

*Caso 1.* Si $np$ no es entero, sea $j = \lceil np \rceil$. Como los conteos son enteros, $\#\{ x_i \leq q \} \geq np$ equivale a $\#\{ x_i \leq q \} \geq j$, y $\#\{ x_i \geq q \} \geq n - np$ equivale a $\#\{ x_i \geq q \} \geq \lceil n - np \rceil = n - j + 1$. Por las equivalencias anteriores, las dos condiciones se cumplen si y solo si $x_{(j)} \leq q \leq x_{(j)}$, es decir, $q = x_{(j)}$.

*Caso 2.* Si $np = k$ es entero, con $1 \leq k \leq n-1$, la primera condición es $\#\{ x_i \leq q \} \geq k$, equivalente a $q \geq x_{(k)}$, y la segunda es $\#\{ x_i \geq q \} \geq n - k$, equivalente a $q \leq x_{(k+1)}$. Por tanto, $q \in [x_{(k)}, x_{(k+1)}]$.
$\blacksquare$

Para $p = \tfrac{1}{2}$ se recupera la mediana: si $n$ es impar, $np$ no es entero y el cuantil es $x_{((n+1)/2)}$; si $n$ es par, el conjunto de cuantiles es $[x_{(n/2)}, x_{(n/2+1)}]$, que es el conjunto de minimizadores del Teorema 2.6.

**Definición 3.2 (Cuartiles, deciles y percentiles):**
Se utilizan nombres especiales para órdenes particulares:

- **Cuartiles** $Q_1, Q_2, Q_3$: cuantiles de orden $0.25$, $0.50$ y $0.75$. Dividen los datos en cuatro partes de igual proporción. $Q_2$ es la mediana.
- **Deciles** $D_1, \ldots, D_9$: cuantiles de orden $0.1, 0.2, \ldots, 0.9$.
- **Percentiles** $P_1, \ldots, P_{99}$: cuantiles de orden $0.01, 0.02, \ldots, 0.99$.

La Proposición 3.1 muestra que, cuando $np$ es entero, hay infinitos números que cumplen la definición de cuantil. En muestras con valores muy dispersos, ese intervalo puede ser enorme.

**Ejemplo 3.1 (Una muestra muy dispareja):**
Sea $\mathbf{x} = (1, 1, 1, 200)$, con $n = 4$. Para el tercer cuartil, $p = 0.75$ y $np = 3$ es entero. Por la Proposición 3.1:

$$
Q_3 \in [x_{(3)}, x_{(4)}] = [1, 200]
$$

Cualquier número entre $1$ y $200$ deja al menos el 75% de los datos por debajo o iguales a él y al menos el 25% por encima o iguales a él. En cambio, para el primer cuartil, $np = 1$ y el conjunto es $[x_{(1)}, x_{(2)}] = [1, 1]$, de modo que $Q_1 = 1$ es único aunque $np$ sea entero, porque los dos datos involucrados coinciden.

**Ejemplo 3.2 (Deciles):**
Sea $\mathbf{x} = (1, 1, 1, 1, 1, 1, 1, 1, 1, 200)$, con $n = 10$. Para el noveno decil, $p = 0.9$ y $np = 9$ es entero:

$$
D_9 \in [x_{(9)}, x_{(10)}] = [1, 200]
$$

Es decir, cualquier valor de ese intervalo es un noveno decil legítimo de la muestra.

> **Observación:** que la definición admita varios valores no es una patología de ejemplos artificiales: ocurre siempre que $np$ es entero y los dos datos consecutivos $x_{(np)}$ y $x_{(np+1)}$ son distintos. Como un programa, como Excel o Python, debe devolver un solo número, cada uno adopta una convención para elegirlo.

### 3.2 Cinco formas de calcular cuantiles

Hyndman y Fan (1996) catalogaron nueve métodos de cálculo de cuantiles muestrales usados en la práctica, numerados del 1 al 9. A continuación se presentan cinco de ellos.

Para $h \in [1, n]$ se define el **valor interpolado** de los datos ordenados:

$$
x_{(h)} = x_{(\lfloor h \rfloor)} + (h - \lfloor h \rfloor) \left( x_{(\lfloor h \rfloor + 1)} - x_{(\lfloor h \rfloor)} \right)
$$

que coincide con $x_{(h)}$ cuando $h$ es entero. Si el valor de $h$ que arroja un método cae fuera de $[1, n]$, se toma el extremo más cercano.

**Definición 3.3 (Cinco métodos de cálculo):**
Sea $p \in (0, 1)$.

| Método | Fórmula | Usado por |
|:-------|:--------|:----------|
| **A. Mediana de las mitades** | Solo para cuartiles: $Q_2 = Me$; $Q_1$ y $Q_3$ son las medianas de la mitad inferior y de la mitad superior de los datos ordenados. Si $n$ es impar, la mediana se excluye de ambas mitades. | Textos clásicos; cálculo manual |
| **B. Tipo 1** | $x_{(\lceil np \rceil)}$ | Definición de $Q(p) = \inf\{ x : F_n(x) \geq p \}$ |
| **C. Tipo 6** | $x_{(h)}$ con $h = (n+1)p$ | Excel `.EXC` |
| **D. Tipo 7** | $x_{(h)}$ con $h = 1 + (n-1)p$ | Python (NumPy, pandas), Excel `.INC` |
| **E. Tipo 8** | $x_{(h)}$ con $h = (n + \tfrac{1}{3})p + \tfrac{1}{3}$ | Recomendado por Hyndman y Fan |

> **Nota:** el método B es el único de la lista que devuelve siempre uno de los datos y que, además, coincide con el extremo inferior del conjunto de cuantiles de la Proposición 3.1. Los métodos con interpolación (C, D y E) devuelven valores intermedios entre dos datos consecutivos y, cuando $np$ no es entero, en general no cumplen en sentido estricto la Definición 3.1. Son convenciones que buscan comportarse bien al estimar los cuantiles de la población.

**Ejemplo 3.3 (Los cinco métodos sobre las mismas muestras):**
Se aplican los métodos a la muestra $(1, 1, 1, 200)$ y a las 18 calificaciones de la Clase 4:

$$
5.5, 6.0, 6.5, 7.0, 7.0, 7.5, 7.5, 7.5, 8.0, 8.0, 8.5, 8.5, 8.5, 8.5, 9.0, 9.0, 9.5, 10.0
$$

| Método | $Q_3$ de $(1, 1, 1, 200)$ | $Q_1$ de las calificaciones | $Q_3$ de las calificaciones |
|:-------|:-------------------------:|:---------------------------:|:---------------------------:|
| A. Mediana de las mitades | $100.5$ | $7.0$ | $8.5$ |
| B. Tipo 1 | $1$ | $7.0$ | $8.5$ |
| C. Tipo 6 | $150.25$ | $7.0$ | $8.625$ |
| D. Tipo 7 | $50.75$ | $7.125$ | $8.5$ |
| E. Tipo 8 | $\approx 117.08$ | $7.0$ | $\approx 8.54$ |

Para $(1,1,1,200)$, los cinco valores de $Q_3$ pertenecen al conjunto $[1, 200]$ del Ejemplo 3.1, pero difieren enormemente entre sí. Para las calificaciones, donde los datos están poco dispersos, los métodos difieren entre sí en menos de $0.13$. Como ejemplo del cálculo, para $Q_3$ de las calificaciones con $n = 18$ por el método C: $h = 19 \cdot 0.75 = 14.25$, $x_{(14)} = 8.5$, $x_{(15)} = 9.0$, y por tanto $Q_3 = 8.5 + 0.25(9.0 - 8.5) = 8.625$.

### 3.3 Convención del curso: el método D (Tipo 7)

Como el cuantil admite varios valores y los métodos de cálculo difieren, es necesario fijar una convención. En este curso se adopta el **método D (Tipo 7)**, porque es el que utilizan por defecto Python (NumPy y pandas) y la función de Excel `PERCENTILE.INC` / `QUARTILE.INC`, de modo que los resultados calculados a mano pueden verificarse directamente con un programa. Además, es válido para cualquier decil o percentil, a diferencia del método A.

**Definición 3.4 (Cuantil Tipo 7):**
Para $p \in [0, 1]$, el **cuantil Tipo 7** de orden $p$ es:

$$
Q_p = x_{(h)}, \quad h = 1 + (n-1)p
$$

donde $x_{(h)}$ es el valor interpolado definido en la Sección 3.2. A partir de aquí, $Q_1$, $Q_3$, $D_k$ y $P_k$ se calculan con esta definición, salvo indicación contraria.

**Proposición 3.2 (Propiedades del cuantil Tipo 7):**

1. $Q_{1/2} = Me$ (la mediana de la Definición 2.9).
2. $Q_0 = x_{(1)}$ y $Q_1 = x_{(n)}$.
3. Si $y_i = a x_i + b$ con $a > 0$, entonces $Q_p(\mathbf{y}) = a\,Q_p(\mathbf{x}) + b$.

**Demostración:**
1. Para $p = \tfrac{1}{2}$, $h = 1 + \tfrac{n-1}{2} = \tfrac{n+1}{2}$. Si $n$ es impar, $h$ es entero y $Q_{1/2} = x_{((n+1)/2)}$. Si $n$ es par, $\lfloor h \rfloor = n/2$ y la parte fraccionaria es $\tfrac{1}{2}$, de modo que $Q_{1/2} = x_{(n/2)} + \tfrac{1}{2}(x_{(n/2+1)} - x_{(n/2)})$, el punto medio de los dos valores centrales.
2. Para $p = 0$, $h = 1$; para $p = 1$, $h = n$.
3. Como $a > 0$, el orden se conserva: $y_{(i)} = a x_{(i)} + b$. Con $f = \lfloor h \rfloor$ y $g = h - f$:

$$
\begin{align}
Q_p(\mathbf{y}) &= (1 - g)\,y_{(f)} + g\,y_{(f+1)} \\
&= (1 - g)(a x_{(f)} + b) + g(a x_{(f+1)} + b) \\
&= a\left[ (1 - g)\,x_{(f)} + g\,x_{(f+1)} \right] + b \\
&= a\,Q_p(\mathbf{x}) + b
\end{align}
$$

$\blacksquare$

La propiedad 3 es análoga al Teorema 2.1 para la media: los cuantiles se comportan bien ante cambios de unidad.

**Ejemplo 3.4 (Cuantiles de las 50 mediciones):**
Con los 50 datos de la Clase 3 ordenados, $n = 50$ y los datos relevantes son $x_{(13)} = x_{(14)} = 0.29$, $x_{(25)} = 0.86$, $x_{(26)} = 0.93$, $x_{(37)} = 1.44$, $x_{(38)} = 1.71$, $x_{(45)} = 2.34$ y $x_{(46)} = 2.63$.

$$
\begin{align}
Q_1 &: h = 1 + 49(0.25) = 13.25 \Rightarrow Q_1 = 0.29 + 0.25(0.29 - 0.29) = 0.29 \\
Q_2 &: h = 1 + 49(0.50) = 25.50 \Rightarrow Q_2 = 0.86 + 0.50(0.93 - 0.86) = 0.895 \\
Q_3 &: h = 1 + 49(0.75) = 37.75 \Rightarrow Q_3 = 1.44 + 0.75(1.71 - 1.44) = 1.6425 \\
P_{90} &: h = 1 + 49(0.90) = 45.10 \Rightarrow P_{90} = 2.34 + 0.10(2.63 - 2.34) = 2.369
\end{align}
$$

Esto significa que, aproximadamente, la mitad de las mediciones es menor que $0.895$ y el 90% es menor que $2.369$.

**Aplicaciones:**

- **Salud:** las curvas de crecimiento pediátricas se expresan en percentiles de peso y talla.
- **Educación:** los puntajes de pruebas estandarizadas se informan como percentiles.
- **Finanzas:** el valor en riesgo (VaR) de una cartera es un cuantil de la distribución de pérdidas.
- **Computación:** en el monitoreo de servicios, las latencias se reportan como $P_{95}$ y $P_{99}$, porque la media oculta las demoras extremas.

### 3.4 Cuantiles para datos agrupados

Cuando solo se dispone de la tabla de frecuencias agrupadas, no se conocen los datos ordenados, y los métodos anteriores no pueden aplicarse. Se recurre a la ojiva de la Clase 4, que une con segmentos de recta los puntos $(c_{i+1}, N_i)$. Esto equivale a suponer que los datos se reparten de forma uniforme dentro de cada intervalo. El cuantil se obtiene invirtiendo esa función lineal a trozos.

**Definición 3.5 (Cuantil para datos agrupados):**
Sean los intervalos $I_i = [c_i, c_{i+1})$ de amplitud $a_i = c_{i+1} - c_i$, con frecuencias absolutas $n_i$ y frecuencias absolutas acumuladas $N_i$, y $N_0 = 0$. Para $p \in (0, 1)$, sea $I_j$ la clase que cumple $N_{j-1} < np \leq N_j$. El cuantil de orden $p$ es:

$$
Q_p = c_j + a_j \cdot \dfrac{np - N_{j-1}}{n_j}
$$

**Proposición 3.3 (Interpretación como inversa de la ojiva):**
La fórmula de la Definición 3.5 es la abscisa del punto de la ojiva cuya ordenada (en frecuencias absolutas acumuladas) es $np$.

**Demostración:**
En el intervalo $I_j$, la ojiva es el segmento que une $(c_j, N_{j-1})$ con $(c_{j+1}, N_j)$. Su pendiente es $(N_j - N_{j-1})/a_j = n_j/a_j$, y su ecuación es:

$$
N(x) = N_{j-1} + \dfrac{n_j}{a_j}(x - c_j)
$$

Igualando $N(x) = np$ y despejando $x$ se obtiene $x = c_j + a_j (np - N_{j-1})/n_j$. La condición $N_{j-1} < np \leq N_j$ garantiza que $x \in (c_j, c_{j+1}]$ y que $n_j > 0$.
$\blacksquare$

**Ejemplo 3.5 (Cuartiles de datos agrupados):**
Con la tabla de las 50 mediciones, $n = 50$ y las frecuencias acumuladas son $N_1 = 19$, $N_2 = 28$, $N_3 = 37$, $N_4 = 43$. Para $Q_2$, $np = 25$ y $N_1 = 19 < 25 \leq 28 = N_2$, de modo que $j = 2$:

$$
Q_2 = 0.53 + 0.50 \cdot \dfrac{25 - 19}{9} \approx 0.863
$$

De manera análoga, $Q_1$ ($np = 12.5$, clase $1$) y $Q_3$ ($np = 37.5$, clase $4$):

$$
Q_1 = 0.03 + 0.50 \cdot \dfrac{12.5 - 0}{19} \approx 0.359, \qquad Q_3 = 1.53 + 0.50 \cdot \dfrac{37.5 - 37}{6} \approx 1.572
$$

Comparados con los valores calculados con los datos originales en el Ejemplo 3.4 ($0.29$, $0.895$ y $1.6425$), se aprecia la pérdida de información por agrupar.

### 3.5 Resumen de cinco números

Cinco valores bastan para dar una idea de la posición y de la amplitud de unos datos: los dos extremos, el centro y los límites de la mitad central. Es la información que ya se utilizó para construir el diagrama de caja de la Clase 4.
**Definición 3.6 (Resumen de cinco números):**
El **resumen de cinco números** de una muestra es la lista:

$$
\left( x_{(1)},\ Q_1,\ Q_2,\ Q_3,\ x_{(n)} \right)
$$

formada por el mínimo, el primer cuartil, la mediana, el tercer cuartil y el máximo. Es el resumen que representa el diagrama de caja y bigotes de la Clase 4.

**Ejemplo 3.6 (Calificaciones):**
Para las 18 calificaciones, con la convención del Tipo 7: $x_{(1)} = 5.5$, $Q_1 = 7.125$, $Q_2 = 8.0$, $Q_3 = 8.5$ y $x_{(18)} = 10.0$. El resumen de cinco números es $(5.5, 7.125, 8.0, 8.5, 10.0)$.

---

## 4. Medidas de dispersión

Dos conjuntos de datos pueden tener la misma media y, sin embargo, ser muy distintos. Una empresa donde los 15 empleados ganan aproximadamente $3\,290$ dólares cada uno tiene el mismo salario medio que la del Ejemplo 2.1, pero en ella nadie gana mucho más ni mucho menos que los demás. La media dice dónde está el centro de los datos; no dice nada sobre cuánto se alejan de él. Las **medidas de dispersión** cuantifican esa variabilidad y completan la descripción de un conjunto de datos.

### 4.1 Rango y rango intercuartílico

La forma más inmediata de medir la dispersión es mirar cuánto separa a los datos extremos entre sí. Una versión más resistente descarta las colas y mira solo la parte central.

**Definición 4.1 (Rango):**
El **rango** de una muestra es:

$$
R = x_{(n)} - x_{(1)}
$$

**Definición 4.2 (Rango intercuartílico):**
El **rango intercuartílico** (RIC) es la diferencia entre el tercer y el primer cuartil:

$$
\text{RIC} = Q_3 - Q_1
$$

calculados con la convención de la Sección 3.3. El RIC mide la amplitud del intervalo que contiene aproximadamente el 50% central de los datos, y es la longitud de la caja del diagrama de caja de la Clase 4.

**Ejemplo 4.1 (Salarios):**
Para los salarios del Ejemplo 2.1, $x_{(1)} = 1.2$, $x_{(15)} = 15.0$, $Q_1 = 1.5$ y $Q_3 = 3.25$:

$$
R = 15.0 - 1.2 = 13.8, \qquad \text{RIC} = 3.25 - 1.5 = 1.75
$$

El rango depende únicamente de los dos datos extremos. Si el salario del director fuera $150$ en lugar de $15$, el rango pasaría a $148.8$, mientras que el RIC seguiría siendo $1.75$, pues $Q_1$ y $Q_3$ no dependen del valor del dato máximo.

> **Observación:** el rango es el estadístico de dispersión más sensible a valores atípicos. El RIC es resistente a ellos, por lo que es la medida de dispersión que acompaña de forma natural a la mediana.

### 4.2 Varianza y desviación estándar

Una primera idea para medir la dispersión es promediar las desviaciones $x_i - \bar{x}$ de cada dato respecto de la media. Pero por el Teorema 2.2 su suma es siempre cero, y las desviaciones positivas y negativas se cancelan. Hay dos maneras naturales de evitarlo: elevarlas al cuadrado (varianza) o tomar su valor absoluto (Sección 4.4). La varianza es la más usada porque, como muestra el Teorema 2.3, está ligada a la media: la media es el punto respecto del cual la suma de cuadrados es mínima.

> **Nota histórica:** el término *desviación estándar* fue introducido por Karl Pearson en 1893, y el término *varianza* por Ronald Fisher en 1918. La idea de medir la dispersión mediante cuadrados de desviaciones es, sin embargo, anterior, y está ligada al método de mínimos cuadrados.

**Definición 4.3 (Varianza poblacional):**
Para una población de tamaño $N$ con media $\mu$, la **varianza poblacional** es:

$$
\sigma^2 = \dfrac{1}{N} \sum_{i=1}^{N} (x_i - \mu)^2
$$

**Definición 4.4 (Varianza muestral):**
Para una muestra de tamaño $n \geq 2$, la **varianza muestral** es:

$$
S^2 = \dfrac{1}{n-1} \sum_{i=1}^{n} (x_i - \bar{x})^2
$$

**Definición 4.5 (Desviación estándar):**
La **desviación estándar** es la raíz cuadrada de la varianza: $\sigma = \sqrt{\sigma^2}$ en la población y $S = \sqrt{S^2}$ en la muestra.

La varianza se expresa en el cuadrado de las unidades de los datos (por ejemplo, dólares al cuadrado). La desviación estándar vuelve a las unidades originales, y por eso es la que se interpreta.

**¿Por qué se divide entre $n-1$?** Si se conociera la media poblacional $\mu$, el promedio natural sería $\tfrac{1}{n}\sum (x_i - \mu)^2$. Pero $\mu$ no se conoce y se sustituye por $\bar{x}$, lo cual subestima la dispersión:

**Proposición 4.1 (Subestimación al usar $\bar{x}$):**
Para todo $\mu \in \mathbb{R}$:

$$
\dfrac{1}{n} \sum_{i=1}^{n} (x_i - \mu)^2 = \dfrac{1}{n} \sum_{i=1}^{n} (x_i - \bar{x})^2 + (\bar{x} - \mu)^2
$$

En particular, $\tfrac{1}{n}\sum (x_i - \bar{x})^2 \leq \tfrac{1}{n}\sum (x_i - \mu)^2$, con igualdad si y solo si $\bar{x} = \mu$.

**Demostración:**
Es el Teorema 2.3 con $c = \mu$, dividido entre $n$. La desigualdad se sigue de que $(\bar{x} - \mu)^2 \geq 0$.
$\blacksquare$

Es decir, el promedio de los cuadrados de las desviaciones respecto de $\bar{x}$ es sistemáticamente menor que el que se obtendría respecto del verdadero centro $\mu$. Para compensar, se divide entre $n-1$ en lugar de $n$. Que esta corrección hace exactamente que $S^2$ sea un estimador insesgado de $\sigma^2$ se demostrará en el estudio de la estimación puntual, cuando se introduzca la esperanza matemática de una variable aleatoria.

> **Observación:** el divisor $n-1$ se interpreta como el número de **grados de libertad**. Por el Teorema 2.2, las $n$ desviaciones $x_i - \bar{x}$ deben sumar cero, de modo que solo $n-1$ de ellas pueden variar libremente. Los programas no coinciden en el divisor por defecto: en Python, `pandas.Series.var` divide entre $n-1$ y `numpy.var` entre $n$; en Excel, `VAR.S` divide entre $n-1$ y `VAR.P` entre $N$. Conviene verificarlo siempre.

**Proposición 4.2 (Fórmula de cálculo):**
Se cumple:

$$
\sum_{i=1}^{n} (x_i - \bar{x})^2 = \sum_{i=1}^{n} x_i^2 - n\bar{x}^2
$$

y, por tanto, $S^2 = \dfrac{\sum x_i^2 - n\bar{x}^2}{n-1}$.

**Demostración:**

$$
\begin{align}
\sum_{i=1}^{n} (x_i - \bar{x})^2 &= \sum_{i=1}^{n} x_i^2 - 2\bar{x} \sum_{i=1}^{n} x_i + n\bar{x}^2 \\
&= \sum_{i=1}^{n} x_i^2 - 2n\bar{x}^2 + n\bar{x}^2 \\
&= \sum_{i=1}^{n} x_i^2 - n\bar{x}^2
\end{align}
$$

$\blacksquare$

> **Nota:** esta fórmula facilita el cálculo manual, pero en computadora puede perder precisión cuando $\sum x_i^2$ y $n\bar{x}^2$ son muy grandes y casi iguales. Para ese caso existe el algoritmo de actualización de Welford (1962), que calcula la varianza en una sola pasada de forma numéricamente estable.

**Proposición 4.3 (Efecto de una transformación afín):**
Si $y_i = a x_i + b$ con $a, b \in \mathbb{R}$, entonces:

$$
S_y^2 = a^2 S_x^2, \qquad S_y = |a|\, S_x
$$

**Demostración:**
Por el Teorema 2.1, $\bar{y} = a\bar{x} + b$, de modo que $y_i - \bar{y} = a(x_i - \bar{x})$. Entonces:

$$
S_y^2 = \dfrac{1}{n-1} \sum_{i=1}^{n} a^2 (x_i - \bar{x})^2 = a^2 S_x^2
$$

$\blacksquare$

La varianza no cambia al sumar una constante (trasladar los datos) y se multiplica por $a^2$ al cambiar la escala.

**Ejemplo 4.2 (Salarios):**
Con los salarios del Ejemplo 2.1, $\sum x_i^2 = 332.46$ y $n\bar{x}^2 = 49.4^2/15 \approx 162.69$. Por la Proposición 4.2:

$$
\begin{align}
S^2 &= \dfrac{332.46 - 162.69}{14} = \dfrac{169.77}{14} \approx 12.13 \\
S &= \sqrt{12.13} \approx 3.48
\end{align}
$$

La desviación estándar es de unos $3\,480$ dólares, más grande que la propia media ($3\,290$). Esto refleja la fuerte dispersión generada por el salario del director: sin él, los otros $14$ salarios tienen una desviación estándar de apenas $1.33$ (miles de dólares).

**Datos agrupados:**
Cuando solo se dispone de la tabla de frecuencias, se usan las marcas de clase, igual que para la media (Definición 2.2).

**Definición 4.6 (Varianza para datos agrupados):**
Para datos agrupados en $k$ clases con marcas $m_i$ y frecuencias absolutas $n_i$, y con $\bar{x}$ la media agrupada, la varianza se aproxima por:

$$
S^2 \approx \dfrac{1}{n-1} \sum_{i=1}^{k} n_i (m_i - \bar{x})^2
$$

**Ejemplo 4.3 (Datos de la Clase 3):**
Con la tabla de las 50 mediciones y $\bar{x} = 1.08$ (Ejemplo 2.3):

$$
\begin{align}
\sum_{i=1}^{7} n_i (m_i - \bar{x})^2 &= 19(0.8)^2 + 9(0.3)^2 + 9(0.2)^2 + 6(0.7)^2 + 2(1.2)^2 + 3(1.7)^2 + 2(2.2)^2 \\
&= 37.50 \\
S^2 &\approx \dfrac{37.50}{49} \approx 0.765, \qquad S \approx 0.875
\end{align}
$$

Con los 50 datos originales se obtiene $S^2 \approx 0.840$ y $S \approx 0.916$. Como ocurre con la media, agrupar los datos introduce una pérdida de precisión.

### 4.3 Coeficiente de variación

Una desviación estándar de $10$ metros es enorme al medir una vereda de $50$ metros, pero insignificante al medir la distancia a la Luna. La desviación estándar depende de las unidades y de la magnitud de los datos, por lo que no sirve para comparar la dispersión de conjuntos medidos en escalas distintas. El **coeficiente de variación** mide la dispersión en relación con el tamaño de la media.

**Definición 4.7 (Coeficiente de variación):**
Para una muestra con media $\bar{x} \neq 0$, el **coeficiente de variación** es:

$$
CV = \dfrac{S}{|\bar{x}|}
$$

que suele expresarse como porcentaje, $100 \cdot CV\,\%$.

**Proposición 4.4 (Invarianza ante cambios de escala):**
Si $y_i = a x_i$ con $a \neq 0$, entonces $CV_y = CV_x$.

**Demostración:**
Por el Teorema 2.1, $\bar{y} = a\bar{x}$, y por la Proposición 4.3, $S_y = |a| S_x$. Entonces:

$$
CV_y = \dfrac{|a|\, S_x}{|a|\,|\bar{x}|} = CV_x
$$

$\blacksquare$

El coeficiente de variación no depende de las unidades, pero sí del punto de origen: si se suma una constante a los datos, $S$ no cambia y $\bar{x}$ sí. Por eso solo tiene sentido para variables en escala de razón, con un cero absoluto.

**Ejemplo 4.4 (Comparación de conjuntos en escalas distintas):**
Los salarios del Ejemplo 2.1 tienen $\bar{x} = 3.29$ y $S = 3.48$ (miles de dólares), y las 18 calificaciones de la Clase 4 tienen $\bar{x} \approx 7.89$ y $S \approx 1.20$ puntos:

$$
CV_{\text{salarios}} = \dfrac{3.48}{3.29} \approx 1.06 \;(106\%), \qquad CV_{\text{calificaciones}} = \dfrac{1.20}{7.89} \approx 0.15 \;(15\%)
$$

Aunque una desviación está en dólares y la otra en puntos, el coeficiente de variación permite concluir que los salarios varían proporcionalmente mucho más que las calificaciones.

> **Nota:** el coeficiente de variación es inestable cuando $\bar{x}$ es cercano a cero. Algunos textos consideran "homogéneo" un conjunto con $CV$ menor a aproximadamente $30\%$, pero se trata de una regla orientativa, sin fundamento teórico universal.

### 4.4 Desviaciones absolutas

La varianza eleva las desviaciones al cuadrado, lo que da un peso muy grande a los datos lejanos. Una alternativa es promediar los valores absolutos de las desviaciones. Aparecen dos versiones, según el centro respecto del cual se miden.

**Definición 4.8 (Desviación absoluta media):**
La **desviación absoluta media** respecto de la media es:

$$
D = \dfrac{1}{n} \sum_{i=1}^{n} |x_i - \bar{x}|
$$

**Definición 4.9 (Desviación absoluta mediana, MAD):**
La **desviación absoluta mediana** (en inglés, *median absolute deviation*, MAD) es la mediana de los valores absolutos de las desviaciones respecto de la mediana:

$$
\text{MAD} = \text{Mediana}\left( |x_1 - Me|,\ \ldots,\ |x_n - Me| \right)
$$

**Proposición 4.5 (Comparación con la desviación respecto de la media):**
Se cumple:

$$
\dfrac{1}{n} \sum_{i=1}^{n} |x_i - Me| \leq \dfrac{1}{n} \sum_{i=1}^{n} |x_i - \bar{x}|
$$

**Demostración:**
Por el Teorema 2.6, la función $c \mapsto \sum_i |x_i - c|$ alcanza su mínimo en $c = Me$, de modo que su valor en $c = Me$ no puede superar su valor en $c = \bar{x}$.
$\blacksquare$

**Ejemplo 4.5 (Salarios):**
Para los salarios del Ejemplo 2.1, $\sum |x_i - \bar{x}| \approx 30.65$ y, por tanto, $D \approx 2.04$. Respecto de la mediana $Me = 2.2$, las desviaciones absolutas ordenadas son:

$$
(0.0,\ 0.2,\ 0.3,\ 0.3,\ 0.4,\ 0.7,\ 0.7,\ 0.7,\ 0.8,\ 1.0,\ 1.0,\ 1.3,\ 1.8,\ 3.8,\ 12.8)
$$

y su mediana, el octavo valor, es $\text{MAD} = 0.7$. Si el salario del director fuera $150$ en lugar de $15$, la mediana de los datos y las desviaciones de los demás empleados no cambiarían, por lo que $\text{MAD}$ seguiría valiendo $0.7$; en cambio, la desviación estándar pasaría de $3.48$ a $38.12$.

> **Observación:** para datos normales, la MAD multiplicada por la constante $1.4826$ es comparable con la desviación estándar, lo que permite usarla como una versión resistente de $S$. La justificación de esa constante requiere la distribución normal y se verá en el curso de probabilidad. Para los salarios, $1.4826 \cdot 0.7 \approx 1.04$, muy inferior a $S = 3.48$, lo que revela que la desviación estándar está inflada por el valor extremo.

### 4.5 Puntaje estandarizado

Un estudiante obtiene $15$ puntos en un examen y otro obtiene $80$ en un examen distinto. ¿Cuál tuvo mejor desempeño relativo? Para comparar, hay que expresar cada valor en una escala común: cuántas desviaciones estándar se aleja de la media de su grupo.

**Definición 4.10 (Puntaje estandarizado o puntaje $z$):**
Dada una muestra con media $\bar{x}$ y desviación estándar $S > 0$, el **puntaje $z$** del dato $x_i$ es:

$$
z_i = \dfrac{x_i - \bar{x}}{S}
$$

**Proposición 4.6 (Propiedades de los puntajes $z$):**
Los puntajes estandarizados tienen media $0$ y desviación estándar $1$.

**Demostración:**
Por el Teorema 2.2, $\bar{z} = \tfrac{1}{nS} \sum (x_i - \bar{x}) = 0$. Entonces:

$$
S_z^2 = \dfrac{1}{n-1} \sum_{i=1}^{n} \dfrac{(x_i - \bar{x})^2}{S^2} = \dfrac{1}{S^2} \cdot \dfrac{\sum (x_i - \bar{x})^2}{n-1} = 1
$$

$\blacksquare$

**Ejemplo 4.6 (Salarios):**
Con $\bar{x} = 3.29$ y $S = 3.48$:

$$
z_{15.0} = \dfrac{15.0 - 3.29}{3.48} \approx 3.36, \qquad z_{6.0} \approx 0.78, \qquad z_{1.2} \approx -0.60
$$

El salario del director está a $3.36$ desviaciones estándar por encima de la media, mientras que el salario mínimo está a solo $0.60$ por debajo. Esta asimetría ya sugiere que la distribución tiene una cola derecha larga.

### 4.6 Desigualdad de Chebyshev

Conocidas la media y la desviación estándar, ¿qué proporción de los datos puede alejarse mucho de la media? Aunque no se conozca nada más sobre la forma de la distribución, la desviación estándar impone una cota.

> **Nota histórica:** la desigualdad lleva el nombre de Pafnuti Chebyshev, quien la publicó en 1867, aunque Irénée-Jules Bienaymé la había obtenido antes. Es uno de los primeros resultados generales que relacionan la dispersión con la proporción de datos extremos.

**Teorema 4.1 (Desigualdad de Chebyshev muestral):**
Sea una muestra con desviación estándar $S > 0$ y sea $k > 0$. La proporción de datos que se alejan de la media $k$ desviaciones estándar o más cumple:

$$
\dfrac{\#\{ i : |x_i - \bar{x}| \geq kS \}}{n} \leq \dfrac{n-1}{n\,k^2} < \dfrac{1}{k^2}
$$

En consecuencia, al menos una proporción $1 - 1/k^2$ de los datos está a menos de $kS$ de la media.

**Demostración:**
Sea $m$ el número de datos con $|x_i - \bar{x}| \geq kS$. Todos los términos de la suma son no negativos, y los $m$ términos seleccionados valen al menos $k^2 S^2$:

$$
\begin{align}
(n-1)S^2 &= \sum_{i=1}^{n} (x_i - \bar{x})^2 \\
&\geq \sum_{|x_i - \bar{x}| \geq kS} (x_i - \bar{x})^2 \\
&\geq m\, k^2 S^2
\end{align}
$$

Dividiendo entre $k^2 S^2 > 0$ se obtiene $m \leq (n-1)/k^2$, y dividiendo entre $n$, $m/n \leq (n-1)/(nk^2) < 1/k^2$.
$\blacksquare$

**Ejemplo 4.7 (Salarios):**
Para $k = 2$, la desigualdad garantiza que al menos el $1 - 1/4 = 75\%$ de los datos está en $\bar{x} \pm 2S = [-3.67,\ 10.26]$, y para $k = 3$, al menos el $1 - 1/9 \approx 88.9\%$ en $[-7.15,\ 13.74]$. En los datos, $14$ de los $15$ salarios ($93.3\%$) están dentro de ambos intervalos; solo queda fuera el del director, cuyo puntaje $z = 3.36$ supera $3$. Las cotas se cumplen, aunque son conservadoras.

> **Observación:** la desigualdad vale para cualquier conjunto de datos, por lo que su cota es necesariamente conservadora. Para datos con forma de campana, las proporciones reales son mucho mayores (aproximadamente $95\%$ dentro de $2$ desviaciones estándar en una distribución normal), un resultado que se estudiará en la distribución normal.

### 4.7 Combinación de grupos (Opcional)

Los datos suelen llegar en partes: los salarios de cada departamento de una empresa, las mediciones de cada turno de una fábrica, los registros que procesa cada servidor de un sistema. Si de cada parte se conservan solo el tamaño, la media y la varianza, ¿es posible obtener la media y la varianza de todos los datos juntos, sin volver a los datos originales? La media sí se obtiene de inmediato. La varianza, en cambio, no es el promedio de las varianzas de los grupos: hay que añadir un término que mide cuánto se separan los grupos entre sí.

Sean $k$ grupos de tamaños $n_1, \ldots, n_k$, con $n = \sum_{j=1}^{k} n_j$. El dato $i$-ésimo del grupo $j$ se denota $x_{ji}$, y $\bar{x}_j$ y $S_j^2$ son la media y la varianza muestral del grupo $j$ (con $n_j \geq 2$).

**Proposición 4.7 (Media combinada):**
La media de todos los datos es la media ponderada de las medias de los grupos, con pesos iguales a los tamaños:

$$
\bar{x} = \dfrac{1}{n} \sum_{j=1}^{k} n_j \bar{x}_j
$$

**Demostración:**
La suma de todos los datos es la suma de las sumas de cada grupo, y la suma del grupo $j$ es $n_j \bar{x}_j$:

$$
\bar{x} = \dfrac{1}{n} \sum_{j=1}^{k} \sum_{i=1}^{n_j} x_{ji} = \dfrac{1}{n} \sum_{j=1}^{k} n_j \bar{x}_j
$$

$\blacksquare$

**Teorema 4.2 (Descomposición de la varianza):**
La varianza muestral de todos los datos satisface:

$$
(n-1)\,S^2 = \underbrace{\sum_{j=1}^{k} (n_j - 1)\, S_j^2}_{\text{variación dentro de los grupos}} + \underbrace{\sum_{j=1}^{k} n_j \left( \bar{x}_j - \bar{x} \right)^2}_{\text{variación entre los grupos}}
$$

**Demostración:**
Se aplica el Teorema 2.3 al grupo $j$, con $c = \bar{x}$:

$$
\sum_{i=1}^{n_j} (x_{ji} - \bar{x})^2 = \sum_{i=1}^{n_j} (x_{ji} - \bar{x}_j)^2 + n_j (\bar{x}_j - \bar{x})^2 = (n_j - 1)\, S_j^2 + n_j (\bar{x}_j - \bar{x})^2
$$

Sumando sobre $j = 1, \ldots, k$, el lado izquierdo es $\sum_{j} \sum_{i} (x_{ji} - \bar{x})^2 = (n-1)S^2$, y se obtiene la igualdad.
$\blacksquare$

La varianza total no es, por tanto, el promedio ponderado de las varianzas de los grupos: a la variación dentro de cada grupo se suma la variación entre los grupos, que mide cuánto se alejan las medias de los grupos de la media global. Si todos los grupos tienen la misma media, el segundo término se anula. Para una población dividida en subpoblaciones de tamaños $N_j$, con medias $\mu_j$ y varianzas $\sigma_j^2$, la misma demostración da $\sigma^2 = \sum_j \tfrac{N_j}{N}\, \sigma_j^2 + \sum_j \tfrac{N_j}{N}\, (\mu_j - \mu)^2$.

**Ejemplo 4.8 (Salarios por grupos):**
Los $15$ empleados del Ejemplo 2.1 se dividen en dos grupos: el grupo $A$, con los $8$ salarios menores o iguales a $2.2$, y el grupo $B$, con los $7$ restantes:

| Grupo | Salarios | $n_j$ | $\bar{x}_j$ | $S_j^2$ |
|:-----:|:---------|:-----:|:-----------:|:-------:|
| $A$ | $1.2,\ 1.2,\ 1.5,\ 1.5,\ 1.5,\ 1.8,\ 2.0,\ 2.2$ | 8 | $1.6125$ | $0.1298$ |
| $B$ | $2.5,\ 2.5,\ 3.0,\ 3.5,\ 4.0,\ 6.0,\ 15.0$ | 7 | $5.2143$ | $20.0714$ |

Con solo esta tabla, la media y la varianza de los $15$ salarios son:

$$
\begin{align}
\bar{x} &= \dfrac{8(1.6125) + 7(5.2143)}{15} = \dfrac{12.9 + 36.5}{15} \approx 3.2933 \\
(n-1)S^2 &= \underbrace{7(0.1298) + 6(20.0714)}_{\text{dentro} \,\approx\, 121.34} + \underbrace{8(1.6125 - 3.2933)^2 + 7(5.2143 - 3.2933)^2}_{\text{entre} \,\approx\, 48.43} \\
&\approx 169.77 \\
S^2 &= \dfrac{169.77}{14} \approx 12.13
\end{align}
$$

Estos valores coinciden con los obtenidos en el Ejemplo 4.2 a partir de los $15$ datos. Además, el desglose revela que aproximadamente el $71\%$ de la variación total ocurre dentro de los grupos (casi toda en el grupo $B$, por el salario del director) y el $29\%$ restante se debe a la diferencia entre los salarios medios de ambos grupos.

**Aplicaciones:**

- **Cómputo en paralelo y en flujo continuo:** los datos se procesan por bloques, y cada bloque entrega solo $(n_j, \bar{x}_j, S_j^2)$, que luego se combinan con la Proposición 4.7 y el Teorema 4.2.
- **Muestreo estratificado:** la varianza total de una población se separa en la variación dentro de los estratos y entre los estratos.
- **Análisis de varianza:** el Teorema 4.2 es el punto de partida de esta técnica, que compara las medias de varios grupos a partir de la variación entre ellos frente a la variación dentro de ellos (en cursos posteriores).

### 4.8 Corrección de Sheppard (Opcional)

Al agrupar los datos en intervalos, la varianza se aproxima usando las marcas de clase (Definición 4.6). Esa aproximación comete un error sistemático, porque se sustituye cada dato por el centro de su intervalo. A fines del siglo XIX, William F. Sheppard (1897) propuso una corrección sencilla para estimar la varianza de los datos originales a partir de la tabla agrupada. En esta sección se deduce de dónde sale esa corrección y bajo qué condiciones es razonable.

Se consideran intervalos de amplitud constante $c$. Para cada dato $x_i$, sea $g_i$ la marca de la clase a la que pertenece y $e_i = g_i - x_i$ el **error de agrupación**, que cumple $|e_i| \leq c/2$. En esta sección, $m_2(\cdot)$ denota el promedio de los cuadrados de las desviaciones respecto de la media (con divisor $n$) y $\operatorname{cov}(u, v) = \tfrac{1}{n} \sum_i (u_i - \bar{u})(v_i - \bar{v})$ la covarianza con el mismo divisor.

**Proposición 4.8 (Efecto de agrupar sobre la varianza):**
Con la notación anterior se cumple, para cualquier conjunto de datos:

$$
\begin{align}
m_2(g) &= m_2(x) + m_2(e) + 2\operatorname{cov}(x, e) \\
m_2(x) &= m_2(g) + m_2(e) - 2\operatorname{cov}(g, e)
\end{align}
$$

**Demostración:**
Como $g_i = x_i + e_i$, se tiene $g_i - \bar{g} = (x_i - \bar{x}) + (e_i - \bar{e})$. Elevando al cuadrado, promediando sobre $i$ y desarrollando el binomio se obtiene la primera igualdad. La segunda se obtiene de la misma manera a partir de $x_i = g_i - e_i$:

$$
(x_i - \bar{x})^2 = (g_i - \bar{g})^2 + (e_i - \bar{e})^2 - 2 (g_i - \bar{g})(e_i - \bar{e})
$$

$\blacksquare$

Las igualdades son exactas, pero dependen de las covarianzas de los datos, que son desconocidas cuando solo se dispone de la tabla agrupada. Hay que añadir hipótesis sobre cómo se distribuye el error. Si los errores se reparten de forma uniforme en $(-c/2,\ c/2)$, su varianza es:

$$
m_2(e) \approx \int_{-c/2}^{c/2} \dfrac{t^2}{c}\, dt = \dfrac{1}{c} \cdot \dfrac{2}{3} \left( \dfrac{c}{2} \right)^3 = \dfrac{c^2}{12}
$$

Según cómo se comporte la covarianza se obtienen dos correcciones opuestas:

- **Hipótesis de Sheppard:** el error no está correlacionado con el dato, $\operatorname{cov}(x, e) \approx 0$. Por la primera igualdad, $m_2(x) \approx m_2(g) - c^2/12$. La varianza calculada con las marcas de clase sobreestima la verdadera, y la corrección es **negativa**.
- **Hipótesis de uniformidad dentro de cada clase:** el error no está correlacionado con la marca, $\operatorname{cov}(g, e) \approx 0$. Por la segunda igualdad, $m_2(x) \approx m_2(g) + c^2/12$. La varianza agrupada subestima la verdadera, y la corrección es **positiva**.

La corrección de Sheppard, $m_2(x) \approx m_2(g) - c^2/12$, se justifica en distribuciones suaves cuya densidad se anula en los extremos, como la normal; la segunda hipótesis describe mejor distribuciones aproximadamente uniformes en cada clase. Para la media no se aplica corrección, y el tercer momento central tampoco cambia. Para el cuarto momento central, Sheppard obtuvo $m_4(x) \approx m_4(g) - \tfrac{1}{2}\, m_2(g)\, c^2 + \tfrac{7}{240}\, c^4$, resultado que se deduce con herramientas de probabilidad y que se menciona aquí sin demostración.

**Ejemplo 4.9 (Datos de la Clase 3):**
Con las $50$ mediciones agrupadas en clases de amplitud $c = 0.50$ (Ejemplo 3.4), se calculan las cantidades de la Proposición 4.8 usando los datos originales y su marca de clase:

| Cantidad | Valor |
|:---------|:-----:|
| $m_2(x)$, con los datos originales | $0.8227$ |
| $m_2(g)$, con las marcas de clase | $0.7500$ |
| $m_2(e)$ | $0.0213$ |
| $c^2/12$ | $0.0208$ |
| $\operatorname{cov}(x, e)$ | $-0.0470$ |
| $\operatorname{cov}(g, e)$ | $-0.0257$ |

Se verifica la Proposición 4.8: $0.8227 + 0.0213 + 2(-0.0470) = 0.7500$. El error de agrupación tiene una varianza casi igual a $c^2/12$, tal como se supuso. En cambio, ninguna de las dos covarianzas es cercana a cero. Las correcciones resultan:

$$
m_2(g) - \dfrac{c^2}{12} = 0.7292 \quad \text{(Sheppard)}, \qquad m_2(g) + \dfrac{c^2}{12} = 0.7708 \quad \text{(uniformidad)}
$$

frente al valor verdadero $0.8227$. En este caso la corrección de Sheppard empeora la aproximación: el error pasa de $0.0727$ a $0.0935$. El motivo es que la distribución es asimétrica, con su mayor densidad en el primer intervalo, de modo que su densidad no se anula en el extremo izquierdo y las hipótesis de Sheppard no se cumplen.

> **Observación:** la corrección de Sheppard es una aproximación que depende de la forma de la distribución. Es razonable con muchos datos, clases angostas y distribuciones suaves y con forma de campana; con distribuciones como la del Ejemplo 4.9 no debe aplicarse sin cautela.

### 4.9 Estimadores robustos adicionales (Opcional)

La desviación estándar es sensible a valores atípicos, mientras que el RIC y la MAD son resistentes (Sección 4.4). Sin embargo, estos últimos están en una escala distinta de la de $S$: para los salarios, $\text{MAD} = 0.7$ y $\text{RIC} = 1.75$, frente a $S = 3.48$, de modo que no pueden compararse directamente. Esta sección presenta versiones resistentes ajustadas a la escala de $S$ y una medida de dispersión distinta, que no se basa en desviaciones respecto de un centro.

**Proposición 4.9 (Punto de ruptura de la desviación estándar):**
El punto de ruptura (Definición 2.10) de la desviación estándar muestral es $1/n$, para $n \geq 2$.

**Demostración:**
Sea $\mathbf{y}$ la muestra que resulta de reemplazar el dato $x_j$ por un valor $M$, y sea $k \neq j$ otro índice. Por la desigualdad $(a - b)^2 \leq 2(a - c)^2 + 2(b - c)^2$ con $c = \bar{y}$, y descartando los demás sumandos, que son no negativos:

$$
(n-1)\, S_y^2 \geq (M - \bar{y})^2 + (x_k - \bar{y})^2 \geq \dfrac{(M - x_k)^2}{2}
$$

Cuando $M \to \infty$, el lado derecho tiende a infinito y, por tanto, $S_y \to \infty$. Con un solo dato modificado basta, de modo que el punto de ruptura es $1/n$.
$\blacksquare$

**Definición 4.11 (Escalas robustas):**
Las **escalas robustas** basadas en la MAD y en el RIC son:

$$
\hat{\sigma}_{\text{MAD}} = 1.4826 \cdot \text{MAD}, \qquad \hat{\sigma}_{\text{RIC}} = \dfrac{\text{RIC}}{1.349}
$$

Las constantes están elegidas para que, en datos con distribución normal, ambos estimadores sean comparables con la desviación estándar. Su justificación se basa en los cuantiles de la distribución normal y se estudia en el curso de probabilidad. Los puntos de ruptura de la MAD y del RIC son, aproximadamente, $50\%$ y $25\%$, respectivamente, un resultado que se demuestra en el estudio de la estadística robusta.

**Ejemplo 4.10 (Salarios):**
Para los salarios del Ejemplo 2.1:

$$
\hat{\sigma}_{\text{MAD}} = 1.4826 \cdot 0.7 \approx 1.04, \qquad \hat{\sigma}_{\text{RIC}} = \dfrac{1.75}{1.349} \approx 1.30, \qquad S \approx 3.48
$$

Las dos escalas robustas indican que el salario típico varía alrededor de $1\,000$ a $1\,300$ dólares, valor mucho menor que el de $S$, inflada por el salario del director. Si ese salario se registrara por error como $150$, $S$ pasaría a $38.12$ mientras que $\text{MAD}$ y $\text{RIC}$ seguirían siendo $0.7$ y $1.75$.

**Definición 4.12 (Diferencia media de Gini):**
La **diferencia media de Gini** es el promedio de las diferencias absolutas entre todos los pares de datos:

$$
\text{GMD} = \dfrac{1}{n(n-1)} \sum_{i=1}^{n} \sum_{j=1}^{n} |x_i - x_j|
$$

A diferencia de la varianza, no usa la media ni eleva al cuadrado. Mide cuán distintos son, en promedio, dos datos elegidos al azar.

**Proposición 4.10 (Cálculo de la diferencia media):**
Se cumple:

$$
\sum_{i=1}^{n} \sum_{j=1}^{n} |x_i - x_j| = 2 \sum_{k=1}^{n} (2k - n - 1)\, x_{(k)}
$$

**Demostración:**
La suma sobre los pares ordenados no cambia si se recorren los datos en el orden de los estadísticos de orden. Para $i < j$, $|x_{(i)} - x_{(j)}| = x_{(j)} - x_{(i)}$, y cada par no ordenado aparece dos veces. Fijado $k$, el dato $x_{(k)}$ interviene con signo positivo cuando es el mayor del par, es decir, con los $k - 1$ datos menores, y con signo negativo cuando es el menor del par, es decir, con los $n - k$ datos mayores. Su coeficiente en la suma es, por tanto, $2\left[(k-1) - (n-k)\right] = 2(2k - n - 1)$.
$\blacksquare$

**Ejemplo 4.11 (Salarios):**
Para los salarios ordenados del Ejemplo 2.1, $\sum_{k=1}^{15} (2k - 16)\, x_{(k)} = 304.6$, de modo que:

$$
\text{GMD} = \dfrac{2 \cdot 304.6}{15 \cdot 14} \approx 2.90
$$

Es decir, dos empleados elegidos al azar difieren en promedio en unos $2\,900$ dólares. La diferencia media de Gini no es resistente: si un dato crece sin límite, la suma incluye diferencias $|M - x_i|$ que crecen con él. Sí es menos sensible que $S$, pues crece linealmente con el dato extremo y no cuadráticamente. Se relaciona con el índice de Gini de la Sección 7, que para estos datos vale $\dfrac{1}{2n^2\bar{x}} \sum_{i,j} |x_i - x_j| \approx 0.411$.

### 4.10 Qué medida de dispersión usar

Las medidas de dispersión se agrupan de forma natural con las de tendencia central: la media se acompaña de la desviación estándar, y la mediana del RIC o de la MAD.

| Medida | Unidades | Sensibilidad a atípicos | Cuándo se usa |
|:-------|:--------:|:-----------------------:|:--------------|
| Rango $R$ | Las de los datos | Muy alta | Descripción rápida de la amplitud total |
| RIC | Las de los datos | Resistente | Acompaña a la mediana; base del diagrama de caja |
| Varianza $S^2$ | Cuadrado de las de los datos | Muy alta | Base de la teoría estadística y de la inferencia |
| Desviación estándar $S$ | Las de los datos | Muy alta | Acompaña a la media; la medida más usada |
| Desviación absoluta media $D$ | Las de los datos | Moderada | Alternativa a $S$ menos influida por valores lejanos |
| MAD | Las de los datos | Resistente | Versión robusta de $S$; detección de atípicos |
| $\hat{\sigma}_{\text{MAD}}$, $\hat{\sigma}_{\text{RIC}}$ | Las de los datos | Resistente | Versiones robustas en la escala de $S$ (opcional) |
| Diferencia media de Gini | Las de los datos | Moderada | Alternativa que no usa un centro; conecta con el índice de Gini (opcional) |
| Coeficiente de variación | Sin unidades | Alta (usa $\bar{x}$ y $S$) | Comparar la variabilidad de conjuntos en escalas distintas |

Como regla práctica, cuando la distribución es aproximadamente simétrica y sin valores atípicos relevantes, se reporta el par $(\bar{x}, S)$. Cuando es asimétrica o contiene valores extremos, el par $(Me, \text{RIC})$ o $(Me, \text{MAD})$ describe mejor el conjunto. Los salarios del Ejemplo 2.1 son un caso claro de este segundo tipo.

---

## 5. Momentos

La media y la varianza no son hallazgos aislados. La media es el promedio de los datos; la varianza es el promedio de los cuadrados de sus desviaciones. Ambos son casos de una misma construcción: promediar una potencia de los datos o de sus desviaciones. Variar el exponente da lugar a una familia de resúmenes llamados **momentos**, cuyo nombre proviene de la mecánica. Si cada dato es una masa unitaria colocada sobre una recta, el primer momento es el centro de masa (la media, como en la imagen de la regla de la Sección 2.1) y el segundo momento respecto del centro es el momento de inercia, que mide cuán dispersa está la masa (la varianza). Los momentos de orden tres y cuatro miden la asimetría y el peso de las colas, y se usarán en la Sección 6.

> **Nota histórica:** Karl Pearson usó los momentos de una muestra a partir de 1894 para ajustar curvas a datos, en lo que se conoce como el método de los momentos. En él, se eligen los parámetros de una distribución teórica de modo que sus momentos coincidan con los de la muestra.

### 5.1 Momentos respecto del origen y centrales

Los momentos se agrupan en dos familias. Los momentos respecto del origen promedian potencias de los propios datos y generalizan a la media; los momentos centrales promedian potencias de las desviaciones respecto de la media y describen cómo se distribuyen los datos alrededor de ella.
**Definición 5.1 (Momento respecto del origen):**
El **momento de orden $r$ respecto del origen** de una muestra $\mathbf{x}$ es:

$$
a_r = \dfrac{1}{n} \sum_{i=1}^{n} x_i^r, \qquad r = 1, 2, 3, \ldots
$$

**Definición 5.2 (Momento central):**
El **momento central de orden $r$** es:

$$
m_r = \dfrac{1}{n} \sum_{i=1}^{n} (x_i - \bar{x})^r, \qquad r = 1, 2, 3, \ldots
$$

> **Observación:** los momentos se definen con divisor $n$, no $n-1$. Por eso el segundo momento central $m_2$ no coincide con la varianza muestral $S^2$ de la Definición 4.4, sino que $S^2 = \tfrac{n}{n-1}\, m_2$.

**Proposición 5.1 (Casos particulares):**

1. $a_1 = \bar{x}$.
2. $m_1 = 0$.
3. $m_2 = a_2 - a_1^2$.
4. $a_2 = \text{RMS}^2$.
5. $S^2 = \dfrac{n}{n-1}\, m_2$.

**Demostración:**
1. y 4. Son las Definiciones 2.1 y 2.8.
2. Por el Teorema 2.2, $\sum (x_i - \bar{x}) = 0$.
3. Dividiendo entre $n$ la fórmula de cálculo de la Proposición 4.2, $\sum (x_i - \bar{x})^2 = \sum x_i^2 - n\bar{x}^2$, se obtiene $m_2 = a_2 - a_1^2$.
5. Es la Definición 4.4 escrita con $m_2$.
$\blacksquare$

Los momentos centrales pueden calcularse a partir de los momentos respecto del origen, sin necesidad de restar la media dato por dato.

**Proposición 5.2 (Momentos centrales en términos de los momentos respecto del origen):**
Con la convención $a_0 = 1$, para todo $r \geq 1$:

$$
m_r = \sum_{j=0}^{r} \binom{r}{j} (-a_1)^{r-j}\, a_j
$$

En particular:

$$
\begin{align}
m_3 &= a_3 - 3a_1 a_2 + 2a_1^3 \\
m_4 &= a_4 - 4a_1 a_3 + 6a_1^2 a_2 - 3a_1^4
\end{align}
$$

**Demostración:**
Por el teorema del binomio, $(x_i - a_1)^r = \sum_{j=0}^{r} \binom{r}{j} x_i^j (-a_1)^{r-j}$. Promediando sobre $i$ y usando que $a_1 = \bar{x}$:

$$
m_r = \dfrac{1}{n} \sum_{i=1}^{n} \sum_{j=0}^{r} \binom{r}{j} x_i^j (-a_1)^{r-j} = \sum_{j=0}^{r} \binom{r}{j} (-a_1)^{r-j}\, a_j
$$

Para $r = 3$, se tiene $a_3 - 3a_1 a_2 + 3a_1^2 a_1 - a_1^3 = a_3 - 3a_1a_2 + 2a_1^3$. Para $r = 4$, $a_4 - 4a_1a_3 + 6a_1^2a_2 - 4a_1^3 a_1 + a_1^4 = a_4 - 4a_1a_3 + 6a_1^2a_2 - 3a_1^4$.
$\blacksquare$

**Ejemplo 5.1 (Salarios):**
Con los salarios del Ejemplo 2.1 ($n = 15$), los momentos respecto del origen son:

$$
a_1 \approx 3.2933, \qquad a_2 = 22.164, \qquad a_3 \approx 252.946, \qquad a_4 \approx 3503.696
$$

Por la Proposición 5.2, los momentos centrales son:

$$
\begin{align}
m_2 &= 22.164 - 3.2933^2 \approx 11.318 \\
m_3 &= 252.946 - 3(3.2933)(22.164) + 2(3.2933)^3 \approx 105.405 \\
m_4 &\approx 1261.0
\end{align}
$$

Se verifica que $S^2 = \tfrac{15}{14}\, m_2 \approx 12.13$, el valor del Ejemplo 4.2.

### 5.2 Momentos estandarizados y simetría

Los momentos centrales dependen de las unidades de los datos: $m_3$ se expresa en unidades al cubo y $m_4$ en unidades a la cuarta. Para obtener resúmenes de la forma de la distribución que no dependan de la escala, se dividen entre una potencia de la desviación estándar.

**Proposición 5.3 (Efecto de una transformación afín en los momentos centrales):**
Si $y_i = a x_i + b$ con $a, b \in \mathbb{R}$, entonces $m_r(\mathbf{y}) = a^r\, m_r(\mathbf{x})$ para todo $r \geq 1$.

**Demostración:**
Por el Teorema 2.1, $y_i - \bar{y} = a(x_i - \bar{x})$, de modo que:

$$
m_r(\mathbf{y}) = \dfrac{1}{n} \sum_{i=1}^{n} a^r (x_i - \bar{x})^r = a^r\, m_r(\mathbf{x})
$$

$\blacksquare$

**Definición 5.3 (Momento estandarizado):**
Si $m_2 > 0$, el **momento estandarizado de orden $r$** es:

$$
\tilde{m}_r = \dfrac{m_r}{m_2^{r/2}}
$$

Es decir, el momento central de orden $r$ medido en unidades de la desviación estándar $\sqrt{m_2}$ elevada a $r$. Siempre se tiene $\tilde{m}_1 = 0$ y $\tilde{m}_2 = 1$.

**Proposición 5.4 (Invariancia de los momentos estandarizados):**
Si $y_i = a x_i + b$ con $a \neq 0$, entonces $\tilde{m}_r(\mathbf{y}) = (\operatorname{sgn} a)^r\, \tilde{m}_r(\mathbf{x})$. En particular, si $a > 0$, los momentos estandarizados no cambian.

**Demostración:**
Por la Proposición 5.3, $m_r(\mathbf{y}) = a^r m_r(\mathbf{x})$ y $m_2(\mathbf{y}) = a^2 m_2(\mathbf{x})$. Entonces:

$$
\tilde{m}_r(\mathbf{y}) = \dfrac{a^r\, m_r(\mathbf{x})}{(a^2\, m_2(\mathbf{x}))^{r/2}} = \dfrac{a^r}{|a|^r} \cdot \dfrac{m_r(\mathbf{x})}{m_2(\mathbf{x})^{r/2}} = (\operatorname{sgn} a)^r\, \tilde{m}_r(\mathbf{x})
$$

$\blacksquare$

Esta propiedad justifica que $\tilde{m}_3$ y $\tilde{m}_4$ describan la forma de los datos y no su escala ni su posición: cambiar de unidades (por ejemplo, de dólares a miles de dólares) o trasladar los datos no los modifica.

Los momentos centrales de orden impar capturan la asimetría. Si los datos están repartidos de forma simétrica alrededor de un centro, las desviaciones positivas y negativas se compensan potencia a potencia.

**Proposición 5.5 (Datos simétricos):**
Se dice que una muestra es **simétrica respecto de $c$** si el conjunto de sus valores (con repeticiones) no cambia al reflejarlo respecto de $c$, es decir, si los datos $\{ x_i \}$ y $\{ 2c - x_i \}$ coinciden. En ese caso, $\bar{x} = c$ y $m_r = 0$ para todo $r$ impar.

**Demostración:**
Como ambos conjuntos coinciden, $\bar{x} = \tfrac{1}{n} \sum x_i = \tfrac{1}{n} \sum (2c - x_i) = 2c - \bar{x}$, de donde $\bar{x} = c$. Para $r$ impar:

$$
\sum_{i=1}^{n} (x_i - c)^r = \sum_{i=1}^{n} \left( (2c - x_i) - c \right)^r = \sum_{i=1}^{n} (c - x_i)^r = -\sum_{i=1}^{n} (x_i - c)^r
$$

Por tanto, la suma es igual a su opuesta, y vale cero.
$\blacksquare$

La recíproca es falsa: que un momento central de orden impar sea cero no implica que la muestra sea simétrica.

**Ejemplo 5.2 (Un contraejemplo):**
Sea $\mathbf{x} = (0, 6, 8, 17, 19)$, con $\bar{x} = 10$ y desviaciones $(-10, -4, -2, 7, 9)$. Se tiene:

$$
m_3 = \dfrac{(-10)^3 + (-4)^3 + (-2)^3 + 7^3 + 9^3}{5} = \dfrac{-1072 + 1072}{5} = 0
$$

pero la muestra no es simétrica respecto de $10$: para serlo, el valor $0$ debería tener como reflejo a $20$, que no pertenece a los datos.

### 5.3 Momentos para datos agrupados

Igual que con la media y la varianza, cuando solo se dispone de la tabla de frecuencias se usan las marcas de clase.

**Definición 5.4 (Momentos para datos agrupados):**
Para datos agrupados en $k$ clases con marcas $m_i$ y frecuencias absolutas $n_i$, con $\bar{x}$ la media agrupada, los momentos se aproximan por:

$$
a_r \approx \dfrac{1}{n} \sum_{i=1}^{k} n_i\, m_i^r, \qquad m_r \approx \dfrac{1}{n} \sum_{i=1}^{k} n_i\, (m_i - \bar{x})^r
$$

**Ejemplo 5.3 (Datos de la Clase 3):**
Con la tabla de las 50 mediciones y $\bar{x} = 1.08$, las marcas de clase producen los momentos centrales aproximados que se comparan a continuación con los calculados con los 50 datos originales:

| Momento central | Datos agrupados | Datos originales |
|:---------------:|:---------------:|:----------------:|
| $m_2$ | $0.750$ | $0.823$ |
| $m_3$ | $0.633$ | $0.668$ |
| $m_4$ | $1.707$ | $2.028$ |

Como ocurre con la media y la varianza, agrupar los datos introduce una pérdida de precisión, que en este caso es mayor para el momento de orden cuatro. La Sección 4.8 (opcional) estudia las correcciones de Sheppard, que intentan compensar parte de este error y que, como allí se muestra, solo son confiables bajo ciertas condiciones.

**Aplicaciones:**

- **Mecánica:** el centro de masa y el momento de inercia de un cuerpo son momentos de primer y segundo orden de su distribución de masa.
- **Estadística teórica:** el método de los momentos de Pearson para estimar parámetros de una distribución.
- **Finanzas:** la asimetría y la curtosis de los rendimientos de un activo (momentos estandarizados de orden 3 y 4) describen la probabilidad de pérdidas o ganancias extremas.
- **Aprendizaje automático:** la normalización de variables resta la media y divide por la desviación estándar, usando momentos de primer y segundo orden.

---

## 6. Medidas de forma: asimetría y curtosis

La media y la desviación estándar no determinan la forma de un conjunto de datos. Dos conjuntos pueden tener la misma media y la misma varianza y, sin embargo, ser muy distintos: uno puede repartirse de manera simétrica alrededor de su centro y el otro acumular casi todos los datos en un lado con una cola larga hacia el otro; uno puede tener todas sus desviaciones moderadas y el otro tener muchas desviaciones pequeñas y unas pocas gigantescas. En la Clase 4 estas diferencias se describieron con histogramas (Sección 5.2). Aquí se cuantifican mediante los momentos estandarizados de orden tres y cuatro (Definición 5.3): la **asimetría** y la **curtosis**.

### 6.1 Asimetría: coeficiente de Fisher

Las desviaciones respecto de la media tienen suma cero (Teorema 2.2), de modo que las que quedan por encima y por debajo de ella se compensan en promedio. Elevadas al cuadrado, pierden el signo. Pero elevadas al cubo conservan el signo y amplifican las desviaciones grandes: si los valores extremos se encuentran sobre todo a la derecha de la media, el promedio de los cubos es positivo, y si se encuentran a la izquierda, es negativo. Ese promedio, estandarizado para que no dependa de la escala, es el coeficiente de asimetría.

> **Nota histórica:** Karl Pearson estudió la asimetría de las distribuciones de frecuencias en trabajos como *Skew Variation in Homogeneous Material* (1895), y dos de los coeficientes de la Sección 6.2 llevan su nombre. El coeficiente basado en el tercer momento se asocia con el nombre de Ronald Fisher.

**Definición 6.1 (Coeficiente de asimetría de Fisher):**
Dada una muestra con $m_2 > 0$, el **coeficiente de asimetría** es el momento estandarizado de orden $3$:

$$
g_1 = \tilde{m}_3 = \dfrac{m_3}{m_2^{3/2}} = \dfrac{\dfrac{1}{n} \sum_{i=1}^{n} (x_i - \bar{x})^3}{\left[ \dfrac{1}{n} \sum_{i=1}^{n} (x_i - \bar{x})^2 \right]^{3/2}}
$$

**Proposición 6.1 (Propiedades de $g_1$):**

1. Si $y_i = a x_i + b$ con $a > 0$, entonces $g_1(\mathbf{y}) = g_1(\mathbf{x})$; si $a < 0$, entonces $g_1(\mathbf{y}) = -g_1(\mathbf{x})$.
2. Si la muestra es simétrica respecto de un valor $c$ (Proposición 5.5), entonces $g_1 = 0$.
3. El signo de $g_1$ es el de $m_3$.

**Demostración:**
1. Es la Proposición 5.4 con $r = 3$, pues $(\operatorname{sgn} a)^3 = \operatorname{sgn} a$.
2. Es la Proposición 5.5: los momentos centrales de orden impar de una muestra simétrica son nulos.
3. Se sigue de que $m_2^{3/2} > 0$.
$\blacksquare$

La propiedad 1 muestra que $g_1$ es independiente de las unidades. Cambiar el signo de los datos ($a = -1$) refleja la distribución y, con ella, el signo de la asimetría. La recíproca de la propiedad 2 es falsa: el Ejemplo 5.2 muestra una muestra no simétrica con $m_3 = 0$.

**Interpretación de $g_1$:**

- $g_1 > 0$: asimetría positiva (sesgo a la derecha); los valores extremos se encuentran sobre todo por encima de la media, y la cola derecha es más larga.
- $g_1 < 0$: asimetría negativa (sesgo a la izquierda); la cola izquierda es más larga.
- $g_1 \approx 0$: no hay una asimetría marcada, aunque la distribución no necesariamente es simétrica.

**Ejemplo 6.1 (Salarios):**
Para los salarios del Ejemplo 2.1, $m_3 \approx 105.405$ y $m_2 \approx 11.318$ (Ejemplo 5.1):

$$
g_1 = \dfrac{105.405}{11.318^{3/2}} = \dfrac{105.405}{38.08} \approx 2.77
$$

La asimetría positiva es muy marcada, como ya anticipaban la diferencia entre la media ($3.29$) y la mediana ($2.2$) y el puntaje $z = 3.36$ del director (Ejemplo 4.6).

**Ejemplo 6.2 (Datos de la Clase 3):**
Con los $50$ datos originales, $g_1 \approx 0.896$. Con los datos agrupados (Ejemplo 5.3), $m_3 = 0.633$ y $m_2 = 0.750$, de modo que $g_1 \approx 0.975$. Ambos valores son positivos y de magnitud similar, lo que confirma la asimetría positiva de esta distribución, observada en el histograma de la Clase 4.

**Ejemplo 6.3 (Efecto de una transformación no lineal):**
Las propiedades de la Proposición 6.1 valen para transformaciones afines. Con transformaciones no lineales, la asimetría sí puede cambiar. Los logaritmos de los salarios del Ejemplo 2.1 tienen $g_1 \approx 1.29$, bastante menor que $2.77$: el logaritmo comprime los valores grandes y atenúa la cola derecha (recuérdese que la media geométrica es la media de los logaritmos, Teorema 2.5).

**Aplicaciones:**

- **Finanzas:** la asimetría de los rendimientos de un activo indica si las grandes ganancias o las grandes pérdidas son más probables.
- **Aprendizaje automático:** las variables con asimetría positiva marcada, como ingresos o precios, suelen transformarse con logaritmo o raíz cuadrada antes de ajustar modelos.
- **Control de calidad:** una distribución asimétrica de las dimensiones de una pieza sugiere un proceso con un límite natural, como el tamaño mínimo de un material.

### 6.2 Otras medidas de asimetría

El coeficiente de Fisher depende de los terceros momentos y, por tanto, de los datos más alejados. Existen alternativas más sencillas de calcular y, en un caso, resistentes a valores atípicos.

**Definición 6.2 (Coeficientes de asimetría de Pearson):**
Con $S > 0$, los dos **coeficientes de asimetría de Pearson** son:

$$
\text{Sk}_1 = \dfrac{\bar{x} - Mo}{S}, \qquad \text{Sk}_2 = \dfrac{3\,(\bar{x} - Me)}{S}
$$

El primero usa la moda y el segundo la mediana. Se basan en que, en una distribución con cola larga a la derecha, la media se desplaza hacia ella más que la mediana o la moda.

**Definición 6.3 (Coeficiente de asimetría de Bowley):**
Con $Q_3 > Q_1$, el **coeficiente de asimetría de Bowley** (también llamado de Yule) es:

$$
A_Q = \dfrac{(Q_3 - Me) - (Me - Q_1)}{Q_3 - Q_1} = \dfrac{Q_1 + Q_3 - 2\,Me}{Q_3 - Q_1}
$$

Compara las distancias de la mediana a cada cuartil, dividida entre el RIC. $A_Q > 0$ si y solo si la mediana está más cerca de $Q_1$ que de $Q_3$, que es el criterio visual del diagrama de caja de la Clase 4.

> **Nota histórica:** el coeficiente basado en cuartiles aparece en los *Elements of Statistics* de Arthur Bowley (1901), y George Udny Yule lo retomó en 1912.

**Proposición 6.2 (Acotación y simetría):**

1. $-1 \leq A_Q \leq 1$.
2. $|\text{Sk}_2| \leq 3$.
3. Si la muestra es simétrica respecto de $c$, entonces $\text{Sk}_2 = 0$ y $A_Q = 0$.

**Demostración:**
1. Como los cuartiles están ordenados, $Q_1 \leq Me \leq Q_3$, de modo que $0 \leq Q_3 - Me \leq Q_3 - Q_1$ y $0 \leq Me - Q_1 \leq Q_3 - Q_1$. Su diferencia está entre $-(Q_3 - Q_1)$ y $Q_3 - Q_1$, y dividiendo entre el RIC se obtiene la acotación.

2. Se encadenan cuatro desigualdades. Primero, $|\bar{x} - Me| = \left| \tfrac{1}{n} \sum_i (x_i - Me) \right| \leq \tfrac{1}{n} \sum_i |x_i - Me|$. Segundo, por la Proposición 4.5, $\tfrac{1}{n} \sum_i |x_i - Me| \leq \tfrac{1}{n} \sum_i |x_i - \bar{x}|$. Tercero, con $d_i = |x_i - \bar{x}|$ y $\bar{d} = \tfrac{1}{n} \sum_i d_i$:

$$
\dfrac{1}{n} \sum_{i=1}^{n} d_i^2 - \bar{d}^{\,2} = \dfrac{1}{n} \sum_{i=1}^{n} (d_i - \bar{d})^2 \geq 0
$$

lo que implica $\bar{d} \leq \sqrt{m_2}$. Cuarto, $m_2 = \tfrac{n-1}{n} S^2 \leq S^2$. Por tanto, $|\bar{x} - Me| \leq S$ y $|\text{Sk}_2| \leq 3$.

3. Si la muestra es simétrica respecto de $c$, entonces $x_{(k)} + x_{(n+1-k)} = 2c$ para todo $k$. Con la convención de la Sección 3.3, $Q_p = x_{(h)}$ con $h = 1 + (n-1)p$, y el índice correspondiente a $1 - p$ es $h' = n + 1 - h$. Sean $f = \lfloor h \rfloor$ y $g = h - f$. Interpolando:

$$
\begin{align}
Q_{1-p} &= g\,x_{(n-f)} + (1-g)\,x_{(n-f+1)} \\
&= g\,(2c - x_{(f+1)}) + (1-g)\,(2c - x_{(f)}) \\
&= 2c - Q_p
\end{align}
$$

En particular, $Me = c$ y $Q_1 + Q_3 = 2c$. Además, $\bar{x} = c$ por la Proposición 5.5. Por tanto, $\text{Sk}_2 = 0$ y $A_Q = 0$.
$\blacksquare$

**Ejemplo 6.4 (Comparación de medidas de asimetría):**
Para los salarios del Ejemplo 2.1 ($\bar{x} = 3.29$, $Me = 2.2$, $Mo = 1.5$, $S = 3.48$, $Q_1 = 1.5$, $Q_3 = 3.25$) y para las $50$ mediciones de la Clase 3 ($\bar{x} = 1.06$, $Me = 0.895$, $S = 0.916$, $Q_1 = 0.29$, $Q_3 = 1.6425$):

| Datos | $g_1$ | $\text{Sk}_1$ | $\text{Sk}_2$ | $A_Q$ |
|:------|:-----:|:-------------:|:-------------:|:-----:|
| Salarios | $2.77$ | $0.52$ | $0.94$ | $0.20$ |
| $50$ mediciones | $0.90$ | — | $0.55$ | $0.11$ |

Los cuatro coeficientes son positivos y coinciden en la dirección de la asimetría. Difieren en la magnitud: $g_1$ y $\text{Sk}_2$ usan la media y la desviación estándar, que reaccionan ante el salario del director, mientras que $A_Q$ solo usa cuartiles y la mediana, que no reaccionan. Si el salario del director fuera $150$ en lugar de $15$, $g_1$ pasaría a $3.47$, mientras que $A_Q$ seguiría valiendo exactamente $0.20$, porque $Q_1$, $Me$ y $Q_3$ no cambian.

**Ejemplo 6.5 (Un contraejemplo a la regla "la media supera a la mediana"):**
La relación entre el signo de la asimetría y el orden de la media y la mediana no es tan rígida como suele enseñarse. Sea $\mathbf{x} = (0, 0, 2, 2, 5)$. Su media es $\bar{x} = 1.8$ y su mediana es $Me = 2$. Las desviaciones respecto de la media son $(-1.8, -1.8, 0.2, 0.2, 3.2)$, con $m_3 = 4.224$ y $m_2 = 3.36$, de modo que $g_1 \approx 0.69 > 0$. La asimetría de Fisher es positiva, pero la media es menor que la mediana y, por tanto, $\text{Sk}_2 < 0$.

> **Observación importante:** los coeficientes de Fisher y de Pearson no siempre tienen el mismo signo. La regla "con asimetría positiva, media mayor que mediana" es una tendencia, no una ley. Es más probable que falle en distribuciones discretas, multimodales o con una cola larga y la otra pesada (von Hippel, 2005).

### 6.3 Curtosis

Además del lado hacia el que se estiran los datos, importa cuánto se estiran. Dos conjuntos con la misma media y la misma varianza pueden diferir en la manera como reparten esa varianza: en uno, todas las desviaciones son moderadas; en el otro, casi todas son pequeñas, pero unas pocas son enormes. La elevación a la cuarta potencia amplifica las desviaciones grandes mucho más que la elevación al cuadrado. El promedio de las cuartas potencias de las desviaciones, estandarizado, es sensible a la presencia de esos valores extremos. Es la curtosis.

> **Nota histórica:** el término *curtosis* proviene del griego κυρτός ('curvado, arqueado'). La medida estándar se debe a Karl Pearson, quien la describió como el grado de achatamiento de una distribución respecto de la curva normal. Durante décadas se la interpretó como una medida de la "punta" de la distribución. Westfall (2014) mostró que lo que mide, sin ambigüedad, es el peso de las colas.

**Definición 6.4 (Curtosis y exceso de curtosis):**
Dada una muestra con $m_2 > 0$, la **curtosis** es el momento estandarizado de orden $4$:

$$
\beta_2 = \tilde{m}_4 = \dfrac{m_4}{m_2^{2}}
$$

y el **exceso de curtosis** es $g_2 = \beta_2 - 3$. Se sustrae $3$ porque ese es el valor de la curtosis de una distribución normal, de modo que $g_2$ compara la forma de los datos con la de una campana normal. Este resultado sobre la distribución normal se demuestra en el curso de probabilidad.

Se introducen las desviaciones estandarizadas con divisor $n$, $u_i = (x_i - \bar{x})/\sqrt{m_2}$, que cumplen $\tfrac{1}{n} \sum_i u_i = 0$ y $\tfrac{1}{n} \sum_i u_i^2 = 1$. No deben confundirse con los puntajes $z$ de la Definición 4.10, que dividen entre $S$. En términos de ellas, $g_1 = \tfrac{1}{n} \sum u_i^3$ y $\beta_2 = \tfrac{1}{n} \sum u_i^4$.

**Proposición 6.3 (Cota inferior de la curtosis):**
Para toda muestra con $m_2 > 0$:

$$
\beta_2 \geq 1 + g_1^2
$$

es decir, $g_2 \geq g_1^2 - 2$. La igualdad se da si y solo si los datos toman a lo sumo dos valores distintos. En particular, $\beta_2 \geq 1$.

**Demostración:**
Para todo $t \in \mathbb{R}$, el promedio de $(u_i^2 - 1 - t\,u_i)^2$ es no negativo. Desarrollando el cuadrado y usando $\tfrac{1}{n} \sum u_i = 0$, $\tfrac{1}{n} \sum u_i^2 = 1$, $\tfrac{1}{n} \sum u_i^3 = g_1$ y $\tfrac{1}{n} \sum u_i^4 = \beta_2$:

$$
\begin{align}
0 &\leq \dfrac{1}{n} \sum_{i=1}^{n} \left( u_i^2 - 1 - t\,u_i \right)^2 \\
&= \dfrac{1}{n} \sum_{i=1}^{n} \left[ (u_i^2 - 1)^2 - 2t\,u_i (u_i^2 - 1) + t^2 u_i^2 \right] \\
&= (\beta_2 - 1) - 2t\,g_1 + t^2
\end{align}
$$

Un polinomio de segundo grado en $t$ que es no negativo para todo $t$ tiene discriminante no positivo: $4g_1^2 - 4(\beta_2 - 1) \leq 0$, es decir, $\beta_2 \geq 1 + g_1^2$.

*Igualdad.* Se da si y solo si existe $t$ con $u_i^2 - 1 - t\,u_i = 0$ para todo $i$, es decir, si todos los $u_i$ son raíces de una misma ecuación cuadrática, lo cual ocurre únicamente si los datos toman a lo sumo dos valores. Recíprocamente, si los datos toman dos valores, cuyas desviaciones estandarizadas son $u'$ y $u''$, las condiciones de media $0$ y varianza $1$ implican $u' u'' = -1$, y con $t = u' + u''$ se tiene $u^2 - 1 - t\,u = (u - u')(u - u'') = 0$ para todos los datos. Entonces el polinomio $(\beta_2 - 1) - 2t\,g_1 + t^2$ se anula en ese $t$ y, al ser no negativo, su discriminante es nulo, es decir, $\beta_2 = 1 + g_1^2$.
$\blacksquare$

La cota $\beta_2 \geq 1$ muestra que el exceso de curtosis nunca es menor que $-2$.

**Proposición 6.4 (La curtosis mide el peso de las colas):**
Sea $T = \dfrac{1}{n} \sum_{|u_i| > 1} u_i^2 (u_i^2 - 1)$ la contribución de los datos que distan más de una desviación estándar de la media. Entonces:

$$
T - \dfrac{1}{4} \leq \beta_2 - 1 \leq T
$$

**Demostración:**
Como $\tfrac{1}{n} \sum u_i^2 = 1$, se tiene $\beta_2 - 1 = \tfrac{1}{n} \sum (u_i^4 - u_i^2)$. Separando los datos con $|u_i| > 1$ de los que cumplen $|u_i| \leq 1$:

$$
\beta_2 - 1 = T - C, \qquad C = \dfrac{1}{n} \sum_{|u_i| \leq 1} u_i^2 (1 - u_i^2)
$$

Para $|u_i| \leq 1$, el producto $s(1 - s)$ con $s = u_i^2 \in [0, 1]$ está entre $0$ y $\tfrac{1}{4}$ (su máximo se alcanza en $s = \tfrac{1}{2}$). Por tanto $0 \leq C \leq \tfrac{1}{4}$, y de $\beta_2 - 1 = T - C$ se sigue la acotación.
$\blacksquare$

La Proposición 6.4 formaliza la interpretación correcta de la curtosis: la parte central de los datos, los que están a menos de una desviación estándar de la media, afecta a $\beta_2$ en a lo sumo $\tfrac{1}{4}$, y el resto de $\beta_2$ proviene de los datos más alejados. Una curtosis alta indica la presencia de valores extremos, y no una distribución "puntiaguda". Por eso un exceso de curtosis positivo se llama **leptocúrtico** y uno negativo, **platicúrtico**.

**Definición 6.5 (Tipos de curtosis):**
Según el signo del exceso de curtosis, una distribución es:

- **Mesocúrtica** si $g_2 \approx 0$, con colas comparables a las de la distribución normal.
- **Leptocúrtica** si $g_2 > 0$: colas más pesadas que la normal, es decir, más datos extremos.
- **Platicúrtica** si $g_2 < 0$: colas más livianas que la normal, es decir, menos datos extremos.

**Ejemplo 6.6 (Salarios):**
Para los salarios del Ejemplo 2.1, $m_4 \approx 1261.0$ y $m_2 \approx 11.318$ (Ejemplo 5.1):

$$
\beta_2 = \dfrac{1261.0}{11.318^2} \approx 9.84, \qquad g_2 \approx 6.84
$$

La distribución es fuertemente leptocúrtica. Solo un dato, el del director, dista más de una desviación estándar de la media, con $u = 3.48$. Su contribución es $T = 8.97$, frente a $\beta_2 - 1 = 8.84$: prácticamente toda la curtosis proviene de un único valor extremo, y los otros $14$ datos casi no influyen. También se verifica la Proposición 6.3: $\beta_2 = 9.84 \geq 1 + g_1^2 = 1 + 7.66 = 8.66$.

**Ejemplo 6.7 (Distribución uniforme):**
Una distribución uniforme en $[-\tfrac{1}{2}, \tfrac{1}{2}]$ (densidad constante igual a $1$) tiene, por integración, momentos $\int_{-1/2}^{1/2} t^2\, dt = \tfrac{1}{12}$ y $\int_{-1/2}^{1/2} t^4\, dt = \tfrac{1}{80}$:

$$
\beta_2 = \dfrac{1/80}{(1/12)^2} = \dfrac{144}{80} = 1.8, \qquad g_2 = -1.2
$$

Es platicúrtica porque su soporte es acotado y, por tanto, no puede producir valores extremos. El nombre no implica que su cima sea plana: lo relevante es la ausencia de colas. Entre las distribuciones continuas habituales, la de Laplace y la exponencial tienen exceso de curtosis positivo, $3$ y $6$ respectivamente, un cálculo que se hace en el curso de probabilidad.

**Ejemplo 6.8 (Datos de la Clase 3):**
Con los $50$ datos originales, $g_2 \approx -0.004$, y con los datos agrupados (Ejemplo 5.3), $g_2 \approx 0.035$. Ambos valores son casi nulos, de modo que las colas tienen un peso similar al de una campana normal. Esa cercanía no implica normalidad: los mismos datos tienen una asimetría marcada ($g_1 \approx 0.90$, Ejemplo 6.2), de modo que su forma es muy distinta de la de una campana simétrica. La asimetría y la curtosis describen aspectos distintos y deben informarse juntas.

**Aplicaciones:**

- **Finanzas:** los rendimientos de los activos suelen tener un exceso de curtosis positivo, de modo que los movimientos extremos son más frecuentes de lo que predice un modelo con colas normales. Subestimar las colas conduce a subestimar el riesgo.
- **Pruebas de normalidad:** estadísticos como el de Jarque-Bera combinan $g_1$ y $g_2$ para contrastar si unos datos pueden provenir de una distribución normal.
- **Análisis de señales:** la curtosis de una señal, por ejemplo sísmica, se usa para detectar la presencia de impulsos y valores atípicos.

### 6.4 Estimadores muestrales corregidos

Los coeficientes $g_1$ y $g_2$ se calculan con momentos de divisor $n$. Los programas, como Excel y Python, no siempre devuelven esas cantidades: varios aplican correcciones que dependen de $n$, diseñadas para que el estimador no tenga sesgo cuando los datos provienen de una distribución normal. Conocer cuál se calcula es necesario para reproducir resultados.

**Definición 6.6 (Versiones con corrección por tamaño de muestra):**
Para una muestra de tamaño $n \geq 3$ (para $G_1$) y $n \geq 4$ (para $G_2$), se definen:

$$
G_1 = \dfrac{\sqrt{n(n-1)}}{n-2}\, g_1, \qquad G_2 = \dfrac{n-1}{(n-2)(n-3)} \left[ (n+1)\, g_2 + 6 \right]
$$

$G_1$ y $G_2$ se construyen a partir de estimadores insesgados de los cumulantes tercero y cuarto, un concepto que se estudia en probabilidad. Son insesgados cuando los datos provienen de una distribución normal.

**Proposición 6.5 (Propiedades de $G_1$ y $G_2$):**

1. $G_1$ y $g_1$ tienen el mismo signo, y $|G_1| > |g_1|$ si $g_1 \neq 0$.
2. $G_1 = \dfrac{n}{(n-1)(n-2)} \sum_{i=1}^{n} \left( \dfrac{x_i - \bar{x}}{S} \right)^3$.
3. Cuando $n \to \infty$, $G_1 / g_1 \to 1$ y $G_2 - g_2 \to 0$ (con $g_2$ fijo).

**Demostración:**
1. El factor $\dfrac{\sqrt{n(n-1)}}{n-2}$ es positivo y mayor que $1$, pues $n(n-1) > (n-2)^2$ equivale a $3n > 4$.

2. Como $S^2 = \tfrac{n}{n-1}\, m_2$, se tiene $S^3 = \left( \tfrac{n}{n-1} \right)^{3/2} m_2^{3/2}$ y:

$$
\begin{align}
\sum_{i=1}^{n} \left( \dfrac{x_i - \bar{x}}{S} \right)^3 &= \dfrac{n\, m_3}{S^3} \\
&= n\, g_1 \left( \dfrac{n-1}{n} \right)^{3/2}
\end{align}
$$

Multiplicando por $\dfrac{n}{(n-1)(n-2)}$ se obtiene $g_1 \dfrac{n^{2} (n-1)^{3/2}}{n^{3/2}(n-1)(n-2)} = \dfrac{\sqrt{n(n-1)}}{n-2}\, g_1 = G_1$.

3. $\dfrac{\sqrt{n(n-1)}}{n-2} \to 1$. Además, $\dfrac{(n-1)(n+1)}{(n-2)(n-3)} \to 1$ y $\dfrac{6(n-1)}{(n-2)(n-3)} \to 0$, de modo que $G_2 - g_2 \to 0$.
$\blacksquare$

Para tamaños muestrales pequeños las diferencias son considerables.

**Ejemplo 6.9 (Efecto de la corrección):**
Para los salarios ($n = 15$) y las $50$ mediciones ($n = 50$):

| Datos | $g_1$ | $G_1$ | $g_2$ | $G_2$ |
|:------|:-----:|:-----:|:-----:|:-----:|
| Salarios ($n = 15$) | $2.768$ | $3.086$ | $6.844$ | $10.366$ |
| $50$ mediciones ($n = 50$) | $0.896$ | $0.924$ | $-0.004$ | $0.126$ |

Con $n = 15$, la corrección aumenta $g_1$ en aproximadamente un $11\%$ y $g_2$ en más de un $50\%$; con $n = 50$ los cambios son menores, aunque todavía visibles.

**Qué calculan por defecto Python y Excel:**

| Programa | Asimetría | Curtosis |
|:---------|:---------:|:--------:|
| Python, `scipy.stats.skew` y `scipy.stats.kurtosis` (`bias=True`, por defecto) | $g_1$ | $g_2$ (exceso) |
| Python, las mismas funciones con `bias=False` | $G_1$ | $G_2$ (exceso) |
| Python, `pandas`: `Series.skew()` y `Series.kurt()` | $G_1$ | $G_2$ (exceso) |
| Excel: `SKEW` y `KURT` | $G_1$ | $G_2$ (exceso) |

En este curso, salvo indicación contraria, $g_1$ y $g_2$ se calculan con la Definición 6.1 y la Definición 6.4, es decir, con momentos de divisor $n$.

### 6.5 Qué medida de forma usar

Las medidas de forma se interpretan junto con las de tendencia central y dispersión. Ninguna de ellas determina por sí sola la forma de la distribución.

| Medida | Qué mide | Sensibilidad a valores atípicos | Observaciones |
|:-------|:---------|:-------------------------------:|:--------------|
| $g_1$ (Fisher) | Asimetría, basada en terceros momentos | Muy alta | La más usada; unos pocos datos extremos pueden hacerla muy grande; invariante ante transformaciones afines con $a > 0$ |
| $\text{Sk}_1$, $\text{Sk}_2$ (Pearson) | Asimetría, a partir de la diferencia entre media y moda o mediana | Alta (usan $\bar{x}$ y $S$) | Fáciles de calcular; $\lvert \text{Sk}_2 \rvert \leq 3$ |
| $A_Q$ (Bowley) | Asimetría, a partir de cuartiles | Resistente | Acotado en $[-1, 1]$; ignora las colas más allá de los cuartiles |
| $g_2$ (exceso de curtosis) | Peso de las colas | Muy alta | No mide la "punta"; $g_2 \geq g_1^2 - 2$ |

Como regla práctica, para describir la forma de unos datos conviene informar $g_1$ y $g_2$ junto con una medida resistente como $A_Q$: si coinciden en el signo y en la intensidad, la asimetría es una característica de la distribución; si $g_1$ es grande y $A_Q$ es pequeño, como en los salarios, la asimetría se debe en gran medida a unos pocos valores extremos.

---

## 7. Medidas de concentración y desigualdad

Algunas variables representan un total que se reparte entre las unidades de una población: la masa salarial de una empresa, la riqueza de un país, el ancho de banda de una red, las ventas de una cadena de tiendas. Para ellas, además de preguntar cuánto varían los datos, interesa saber **cómo se reparte el total**: ¿qué fracción del total posee la mitad más pobre?, ¿cuánto acaparan las unidades más grandes? La desviación estándar depende de la escala y del tamaño de los datos, y el coeficiente de variación (Sección 4.3) se apoya en los cuadrados de las desviaciones. Las medidas de concentración se construyen, en cambio, con las **participaciones** $p_i = x_i / \sum_j x_j$ de cada unidad en el total.

En toda esta sección se supone que los datos son no negativos, $x_i \geq 0$, con total positivo $X = \sum_{i=1}^{n} x_i > 0$ (escala de razón), y se ordenan $x_{(1)} \leq x_{(2)} \leq \cdots \leq x_{(n)}$. La Clase 4 mostró una primera aproximación a esta idea con el diagrama de Pareto y la regla 80/20 (Sección 9.3), en la que se ordenan categorías de mayor a menor y se acumula su contribución. Aquí se ordenan las unidades de menor a mayor y se acumulan, en proporciones, tanto las unidades como el total.

> **Nota histórica:** el estadístico estadounidense Max O. Lorenz propuso en 1905 la curva que lleva su nombre. En 1912, Corrado Gini publicó *Variabilità e mutabilità*, donde introdujo la diferencia media como medida de variabilidad y, apoyándose en el trabajo de Lorenz, desarrolló el índice que lleva su nombre. Henri Theil propuso en 1967 un índice inspirado en la entropía de Shannon, y Anthony Atkinson, en 1970, un índice que incorpora explícitamente un criterio de aversión a la desigualdad.

### 7.1 Curva de Lorenz

Si se ordenan los individuos del más pobre al más rico y se grafica, para cada fracción $i/n$ de la población, la fracción del total que acumula, se obtiene una curva que resume el reparto. En un reparto perfectamente igualitario, el $10\%$ más pobre posee el $10\%$ del total y la curva coincide con la diagonal; cuanto más se concentra el total en pocas unidades, más se curva hacia abajo.

**Definición 7.1 (Curva de Lorenz muestral):**
Sean $S_i = \sum_{j=1}^{i} x_{(j)}$ las sumas acumuladas de los datos ordenados y $L_i = S_i / X$, con $L_0 = 0$. La **curva de Lorenz** es la poligonal que une los puntos $\left( \dfrac{i}{n},\ L_i \right)$, para $i = 0, 1, \ldots, n$.

Es decir, $L_i$ es la fracción del total que poseen las $i$ unidades más pequeñas, que representan la fracción $i/n$ de la población.

**Proposición 7.1 (Propiedades de la curva de Lorenz):**

1. $L_i \leq \dfrac{i}{n}$ para todo $i$: la curva nunca pasa por encima de la diagonal.
2. La poligonal es convexa: la pendiente del segmento $i$ es $x_{(i)}/\bar{x}$, y no decrece con $i$.
3. $L_i = i/n$ para todo $i$ si y solo si todos los datos son iguales.

**Demostración:**
1. Para $i = n$, $L_n = 1$. Sea $i < n$ y sean $a$ la media de los $i$ datos menores y $b$ la media de los $n - i$ datos mayores. Cada uno de los primeros es menor o igual que cada uno de los segundos, de modo que $a \leq b$. La media global es una combinación convexa de ambos, $\bar{x} = \dfrac{i\,a + (n-i)\,b}{n} \geq a$. Entonces $S_i = i\,a \leq i\,\bar{x}$ y:

$$
L_i = \dfrac{S_i}{X} \leq \dfrac{i\,\bar{x}}{n\,\bar{x}} = \dfrac{i}{n}
$$

2. La pendiente del segmento que une $\left( \tfrac{i-1}{n}, L_{i-1} \right)$ con $\left( \tfrac{i}{n}, L_i \right)$ es $\dfrac{L_i - L_{i-1}}{1/n} = \dfrac{n\,x_{(i)}}{X} = \dfrac{x_{(i)}}{\bar{x}}$, que no decrece porque $x_{(i)}$ no decrece.

3. Si todos los datos son iguales a $c$, entonces $S_i = ic$ y $X = nc$, de modo que $L_i = i/n$. Recíprocamente, si $L_i = i/n$ para todo $i$, todos los segmentos tienen pendiente $1$, es decir, $x_{(i)} = \bar{x}$ para todo $i$.
$\blacksquare$

**Ejemplo 7.1 (Salarios):**
Para los $15$ salarios del Ejemplo 2.1, con $X = 49.4$:

| $i$ | $i/n$ | $x_{(i)}$ | $S_i$ | $L_i$ |
|:---:|:-----:|:---------:|:-----:|:-----:|
| 1 | 0.067 | 1.2 | 1.2 | 0.024 |
| 2 | 0.133 | 1.2 | 2.4 | 0.049 |
| 3 | 0.200 | 1.5 | 3.9 | 0.079 |
| 4 | 0.267 | 1.5 | 5.4 | 0.109 |
| 5 | 0.333 | 1.5 | 6.9 | 0.140 |
| 6 | 0.400 | 1.8 | 8.7 | 0.176 |
| 7 | 0.467 | 2.0 | 10.7 | 0.217 |
| 8 | 0.533 | 2.2 | 12.9 | 0.261 |
| 9 | 0.600 | 2.5 | 15.4 | 0.312 |
| 10 | 0.667 | 2.5 | 17.9 | 0.362 |
| 11 | 0.733 | 3.0 | 20.9 | 0.423 |
| 12 | 0.800 | 3.5 | 24.4 | 0.494 |
| 13 | 0.867 | 4.0 | 28.4 | 0.575 |
| 14 | 0.933 | 6.0 | 34.4 | 0.696 |
| 15 | 1.000 | 15.0 | 49.4 | 1.000 |

Se lee, por ejemplo, que los $7$ empleados peor pagados ($46.7\%$ de la plantilla) reciben el $21.7\%$ de la masa salarial. Los $12$ peor pagados ($80\%$) reciben el $49.4\%$, de modo que los $3$ mejor pagados ($20\%$) reciben el $50.6\%$. El director solo, que es el $6.7\%$ de la plantilla, recibe el $30.4\%$ de la masa salarial. Es una concentración marcada, aunque menor que la que describe la regla 80/20 de la Clase 4, según la cual el $20\%$ superior recibiría el $80\%$.

### 7.2 Índice de Gini

La curva de Lorenz describe todo el reparto, pero comparar dos curvas que se cruzan, o resumir una en una sola cifra, requiere un número. Corrado Gini propuso medir cuánto se aleja la curva de la diagonal por medio del área que las separa.

**Definición 7.2 (Índice de Gini):**
El **índice de Gini** es el cociente entre el área que queda entre la diagonal y la curva de Lorenz y el área total que queda bajo la diagonal, que es $\tfrac{1}{2}$. Si $B$ es el área bajo la curva de Lorenz:

$$
I_G = \dfrac{\dfrac{1}{2} - B}{\dfrac{1}{2}} = 1 - 2B
$$

> **Nota:** se usa el símbolo $I_G$ para no confundirlo con la media geométrica $G$ de la Sección 2.3.

**Proposición 7.2 (Fórmulas para el índice de Gini):**
Para datos $x_i \geq 0$ con total $X > 0$:

$$
\begin{align}
I_G &= 1 - \dfrac{1}{n} \sum_{i=1}^{n} (L_{i-1} + L_i) \tag{a} \\
I_G &= \dfrac{\sum_{k=1}^{n} (2k - n - 1)\, x_{(k)}}{n\,X} \tag{b} \\
I_G &= \dfrac{\sum_{i=1}^{n} \sum_{j=1}^{n} |x_i - x_j|}{2\,n\,X} = \dfrac{n-1}{2n} \cdot \dfrac{\text{GMD}}{\bar{x}} \tag{c}
\end{align}
$$

donde GMD es la diferencia media de Gini de la Definición 4.12. La fórmula (c) muestra que $I_G$ es la mitad de la diferencia media relativa, ajustada por el factor $\tfrac{n-1}{n}$.

**Demostración:**
(a) El área bajo la poligonal es la suma de $n$ trapecios de ancho $1/n$ y alturas $L_{i-1}$ y $L_i$, es decir, $B = \tfrac{1}{n} \sum_i \tfrac{L_{i-1} + L_i}{2}$. Se sustituye en $I_G = 1 - 2B$.

(b) Como $L_0 = 0$ y $L_n = 1$, se tiene $\sum_{i=1}^{n} (L_{i-1} + L_i) = 2 \sum_{i=1}^{n} L_i - 1$. Además, $\sum_{i=1}^{n} S_i = \sum_{i=1}^{n} \sum_{j \leq i} x_{(j)} = \sum_{j=1}^{n} (n + 1 - j)\, x_{(j)}$, pues $x_{(j)}$ aparece en $S_i$ para $i = j, \ldots, n$. Entonces:

$$
\begin{align}
I_G &= 1 - \dfrac{1}{n} \left( \dfrac{2}{X} \sum_{j=1}^{n} (n + 1 - j)\, x_{(j)} - 1 \right) \\
&= \dfrac{(n+1)\,X - 2 \sum_{j} (n + 1 - j)\, x_{(j)}}{n\,X} \\
&= \dfrac{\sum_{j} \left[ (n+1) - 2(n+1) + 2j \right] x_{(j)}}{n\,X} \\
&= \dfrac{\sum_{j} (2j - n - 1)\, x_{(j)}}{n\,X}
\end{align}
$$

(c) Por la Proposición 4.10, $\sum_{i,j} |x_i - x_j| = 2 \sum_k (2k - n - 1)\, x_{(k)}$; dividiendo entre $2nX$ se obtiene (b). Por la Definición 4.12, $\sum_{i,j} |x_i - x_j| = n(n-1)\,\text{GMD}$ y $X = n\bar{x}$, de donde $I_G = \dfrac{n(n-1)\,\text{GMD}}{2n^2 \bar{x}} = \dfrac{n-1}{2n} \cdot \dfrac{\text{GMD}}{\bar{x}}$.
$\blacksquare$

**Proposición 7.3 (Cotas e invariancia del índice de Gini):**

1. $0 \leq I_G \leq \dfrac{n-1}{n}$.
2. $I_G = 0$ si y solo si todos los datos son iguales, e $I_G = \dfrac{n-1}{n}$ si y solo si una sola unidad posee todo el total.
3. Si $a > 0$, $I_G(a\mathbf{x}) = I_G(\mathbf{x})$. Si $b > 0$ y los datos no son todos iguales, $I_G(\mathbf{x} + b) < I_G(\mathbf{x})$.

**Demostración:**
1. y 2. Por la Proposición 7.1, $L_i \leq i/n$, de modo que $\sum_{i=1}^{n} L_i \leq \tfrac{n+1}{2}$ y, por (a), $I_G = 1 - \tfrac{1}{n}\left( 2\sum_i L_i - 1 \right) \geq 1 - \tfrac{1}{n} \cdot n = 0$, con igualdad si y solo si $L_i = i/n$ para todo $i$, es decir, si los datos son iguales. Para la cota superior, como $L_i \geq 0$ y $L_n = 1$, se tiene $\sum_{i=1}^{n} L_i \geq 1$, y entonces $I_G \leq 1 - \tfrac{1}{n}(2 - 1) = \tfrac{n-1}{n}$, con igualdad si y solo si $L_1 = \cdots = L_{n-1} = 0$, es decir, $x_{(1)} = \cdots = x_{(n-1)} = 0$.

3. Con $y_i = a x_i$, el numerador y el denominador de (b) se multiplican por $a$. Con $y_i = x_i + b$, como $\sum_{k=1}^{n} (2k - n - 1) = 0$, el numerador de (b) no cambia, mientras que el denominador pasa de $nX$ a $n(X + nb) > nX$. Si los datos no son todos iguales, el numerador es positivo y el cociente disminuye.
$\blacksquare$

El índice de Gini muestral alcanza su máximo $\tfrac{n-1}{n}$, no $1$; por eso algunos autores usan el **índice de Gini normalizado** $\tfrac{n}{n-1}\, I_G \in [0, 1]$. Para poblaciones grandes la diferencia es despreciable.

**Ejemplo 7.2 (Salarios):**
Para los salarios, $\sum_k (2k - 16)\, x_{(k)} = 304.6$ y $nX = 15 \cdot 49.4 = 741$:

$$
I_G = \dfrac{304.6}{741} \approx 0.411
$$

El máximo posible con $n = 15$ es $14/15 \approx 0.933$, y el índice normalizado vale $0.411 \cdot \tfrac{15}{14} \approx 0.440$. Con la fórmula (a), el área bajo la poligonal es $B \approx 0.2945$ y $1 - 2B \approx 0.411$, lo que confirma la equivalencia de las fórmulas. También coincide con la fórmula (c): con $\text{GMD} \approx 2.901$ (Ejemplo 4.11), $\dfrac{14}{30} \cdot \dfrac{2.901}{3.293} \approx 0.411$.

**Ejemplo 7.3 (Un aumento proporcional y una bonificación fija):**
Al otorgar a todos los empleados el aumento del $5\%$ y la bonificación fija de $0.3$ del Ejemplo 2.2, los nuevos salarios son $y_i = 1.05\,x_i + 0.3 = 1.05\,(x_i + 0.286)$. El factor multiplicativo no modifica el índice y la constante lo reduce, por la Proposición 7.3:

$$
I_G(\mathbf{y}) = I_G(\mathbf{x} + 0.286) = \dfrac{304.6}{15\,(49.4 + 15 \cdot 0.286)} \approx 0.378
$$

Una suma fija a todos los salarios reduce la concentración relativa, aunque no modifique las diferencias absolutas entre ellos. Por eso el índice de Gini es una medida de desigualdad relativa, y no de dispersión absoluta como la desviación estándar.

**Proposición 7.4 (Cota del índice de Gini a partir de un punto de la curva de Lorenz):**
Si el $100u\%$ más rico de la muestra ($u = m/n$ con $m$ entero) posee una fracción $f$ del total, entonces:

$$
I_G \geq f - u
$$

**Demostración:**
El punto $(1 - u,\ 1 - f)$ es un vértice de la poligonal de Lorenz, pues las $n - m$ unidades menores poseen la fracción $1 - f$ del total. Por la Proposición 7.1, la poligonal es convexa, de modo que queda por debajo de los segmentos que unen $(0, 0)$ con $(1-u, 1-f)$ y este con $(1, 1)$. El área bajo esa poligonal de dos tramos es la suma de dos trapecios:

$$
\dfrac{1}{2}(1-u)(1-f) + \dfrac{1}{2}\, u\,\left[ (1-f) + 1 \right] = \dfrac{1}{2}\left( 1 - f + u \right)
$$

Como el área $B$ bajo la curva de Lorenz no supera ese valor, $I_G = 1 - 2B \geq 1 - (1 - f + u) = f - u$.
$\blacksquare$

**Ejemplo 7.4 (La regla 80/20 y los salarios):**
Si el $20\%$ más rico recibe el $80\%$ del total, como sostiene la regla 80/20 de Pareto, entonces $I_G \geq 0.8 - 0.2 = 0.6$. Para los salarios, el $20\%$ más rico ($3$ empleados) recibe $f = 0.506$ del total, y la proposición garantiza $I_G \geq 0.506 - 0.2 = 0.306$, cota que se cumple con holgura, pues $I_G = 0.411$.

> **Observación:** el índice de Gini resume una curva en un número, por lo que curvas de Lorenz distintas pueden tener el mismo índice. Si el índice no se acompaña de la curva, no revela en qué parte de la distribución se produce la desigualdad. Además, los resultados de esta sección suponen $x_i \geq 0$; con valores negativos, como las deudas, el índice puede superar $1$.

**Aplicaciones:**

- **Economía y política pública:** la desigualdad de ingresos, riqueza o consumo de un país se reporta habitualmente con el índice de Gini.
- **Computación y redes:** la concentración de la carga entre servidores, o del tráfico entre usuarios, puede medirse con la curva de Lorenz y el índice de Gini.
- **Control de calidad:** la regla 80/20 de la Clase 4 equivale a un punto de la curva de Lorenz, y la Proposición 7.4 permite acotar el índice a partir de él.

El índice de Gini de esta sección no debe confundirse con la *impureza de Gini* usada en los árboles de decisión de aprendizaje automático, que es una cantidad distinta.

### 7.3 Índices de Theil y de Atkinson (Opcional)

El índice de Gini no admite, en general, una descomposición aditiva en una parte *dentro* de los grupos y otra *entre* los grupos, como la del Teorema 4.2 para la varianza (Shorrocks, 1980). Las dos medidas de esta sección sí permiten estudiar subgrupos: la primera, el índice de Theil, de forma aditiva; la segunda, el índice de Atkinson, incorpora de manera explícita cuánto importa la desigualdad que afecta a los más pobres.

**Definición 7.3 (Índice de Theil):**
Con participaciones $p_i = x_i / X$ y la convención $0 \ln 0 = 0$, el **índice de Theil** es:

$$
\text{Th} = \dfrac{1}{n} \sum_{i=1}^{n} \dfrac{x_i}{\bar{x}} \ln \dfrac{x_i}{\bar{x}} = \sum_{i=1}^{n} p_i \ln (n\, p_i)
$$

**Proposición 7.5 (Índice de Theil y entropía):**
Sea $H = -\sum_{i=1}^{n} p_i \ln p_i$ la entropía de Shannon de las participaciones. Entonces:

$$
\text{Th} = \ln n - H, \qquad 0 \leq \text{Th} \leq \ln n
$$

con $\text{Th} = 0$ si y solo si todos los datos son iguales, y $\text{Th} = \ln n$ si y solo si una sola unidad posee todo el total.

**Demostración:**
La igualdad entre las dos expresiones de la Definición 7.3 se debe a que $\tfrac{x_i}{\bar{x}} = n\,p_i$. Desarrollando el logaritmo y usando $\sum p_i = 1$:

$$
\text{Th} = \sum_{i=1}^{n} p_i \ln n + \sum_{i=1}^{n} p_i \ln p_i = \ln n - H
$$

*Cota inferior.* Sea $m$ el número de unidades con $p_i > 0$. Con $\ln t \leq t - 1$ aplicada a $t = \tfrac{1}{n p_i}$:

$$
-\text{Th} = \sum_{p_i > 0} p_i \ln \dfrac{1}{n\,p_i} \leq \sum_{p_i > 0} p_i \left( \dfrac{1}{n\,p_i} - 1 \right) = \dfrac{m}{n} - 1 \leq 0
$$

de modo que $\text{Th} \geq 0$. La igualdad exige $m = n$ y $n\,p_i = 1$ para todo $i$, es decir, que todos los datos sean iguales.

*Cota superior.* Como $H \geq 0$ (cada término $-p_i \ln p_i$ es no negativo), $\text{Th} \leq \ln n$. Se tiene $H = 0$ si y solo si cada $p_i \in \{0, 1\}$, es decir, si una sola unidad posee todo el total.
$\blacksquare$

El índice de Theil es, por tanto, la "distancia" entre la entropía máxima $\ln n$, que corresponde al reparto igualitario, y la entropía observada $H$. Cuanto más concentrado está el total, menor es la entropía y mayor el índice.

**Proposición 7.6 (Descomposición del índice de Theil):**
Se divide la muestra en grupos $g = 1, \ldots, k$, de tamaños $n_g$ y totales $X_g$. Sean $s_g = X_g / X$ la participación del grupo en el total, $\nu_g = n_g / n$ su participación en la población y $\text{Th}_g$ el índice de Theil calculado solo con los datos del grupo. Entonces:

$$
\text{Th} = \underbrace{\sum_{g=1}^{k} s_g\, \text{Th}_g}_{\text{dentro de los grupos}} + \underbrace{\sum_{g=1}^{k} s_g \ln \dfrac{s_g}{\nu_g}}_{\text{entre los grupos}}
$$

**Demostración:**
Para una unidad $i$ del grupo $g$, su participación en el total es $p_i = s_g\, q_i$, donde $q_i = x_i / X_g$ es su participación dentro del grupo y $\sum_{i \in g} q_i = 1$. Se tiene $n\,p_i = \dfrac{s_g}{\nu_g} \cdot n_g\, q_i$, de modo que $\ln(n\,p_i) = \ln \dfrac{s_g}{\nu_g} + \ln(n_g\, q_i)$. Sumando sobre las unidades del grupo:

$$
\begin{align}
\sum_{i \in g} p_i \ln (n\,p_i) &= s_g \ln \dfrac{s_g}{\nu_g} \sum_{i \in g} q_i + s_g \sum_{i \in g} q_i \ln (n_g\, q_i) \\
&= s_g \ln \dfrac{s_g}{\nu_g} + s_g\, \text{Th}_g
\end{align}
$$

Sumando sobre los grupos se obtiene la igualdad.
$\blacksquare$

Como $\dfrac{s_g}{\nu_g} = \dfrac{\bar{x}_g}{\bar{x}}$, el término entre grupos es $\sum_g \nu_g \dfrac{\bar{x}_g}{\bar{x}} \ln \dfrac{\bar{x}_g}{\bar{x}}$: el índice de Theil de la población en la que cada unidad recibe la media de su grupo.

**Ejemplo 7.5 (Salarios por grupos):**
Con los grupos $A$ (los $8$ salarios menores o iguales a $2.2$) y $B$ (los $7$ restantes) del Ejemplo 4.8: $s_A = 12.9/49.4 = 0.261$, $s_B = 0.739$, $\nu_A = 8/15 = 0.533$ y $\nu_B = 0.467$. Los índices dentro de cada grupo son $\text{Th}_A \approx 0.0215$ y $\text{Th}_B \approx 0.2439$:

$$
\begin{align}
\text{dentro} &= 0.261(0.0215) + 0.739(0.2439) \approx 0.1858 \\
\text{entre} &= 0.261 \ln \dfrac{0.261}{0.533} + 0.739 \ln \dfrac{0.739}{0.467} \approx 0.1530 \\
\text{Th} &\approx 0.1858 + 0.1530 = 0.3389
\end{align}
$$

que coincide con el índice calculado con los $15$ datos, $\text{Th} = \ln 15 - H = 2.7081 - 2.3692 = 0.3389$. Aproximadamente el $55\%$ de la desigualdad medida por el índice de Theil se encuentra dentro de los grupos y el $45\%$ entre ellos. Estos porcentajes difieren de los de la descomposición de la varianza del Ejemplo 4.8 ($71\%$ y $29\%$), pues cada medida pondera las diferencias de manera distinta.

**Definición 7.4 (Índice de Atkinson):**
Para datos estrictamente positivos $x_i > 0$ y un parámetro $\varepsilon \geq 0$, el **índice de Atkinson** es:

$$
A_\varepsilon = 1 - \dfrac{M_{1-\varepsilon}(\mathbf{x})}{\bar{x}}
$$

donde $M_p$ es la media de potencias de la Definición 2.15, con $M_0 = G$ (media geométrica). Es decir, para $\varepsilon \neq 1$, $A_\varepsilon = 1 - \dfrac{1}{\bar{x}} \left( \dfrac{1}{n} \sum_i x_i^{1-\varepsilon} \right)^{1/(1-\varepsilon)}$, y para $\varepsilon = 1$, $A_1 = 1 - G/\bar{x}$.

El parámetro $\varepsilon$ expresa la **aversión a la desigualdad**: cuanto mayor es, más peso se da a lo que ocurre entre los menores ingresos. Para entender su significado se considera una función de bienestar social que depende de los ingresos.

**Proposición 7.7 (Ingreso igualmente distribuido equivalente):**
Sea el bienestar social $W_\varepsilon(\mathbf{x}) = \dfrac{1}{n} \sum_{i=1}^{n} \dfrac{x_i^{1-\varepsilon}}{1-\varepsilon}$ si $\varepsilon \neq 1$, y $W_1(\mathbf{x}) = \dfrac{1}{n} \sum_{i=1}^{n} \ln x_i$. El único ingreso $\xi > 0$ tal que un reparto en el que todos reciben $\xi$ tiene el mismo bienestar que $\mathbf{x}$ es $\xi = M_{1-\varepsilon}(\mathbf{x})$. En consecuencia, $A_\varepsilon = 1 - \xi / \bar{x}$.

**Demostración:**
Para $\varepsilon \neq 1$, el bienestar de un reparto igualitario con ingreso $\xi$ es $\dfrac{\xi^{1-\varepsilon}}{1-\varepsilon}$. Igualándolo a $W_\varepsilon(\mathbf{x})$ y multiplicando por $1-\varepsilon$ se obtiene $\xi^{1-\varepsilon} = \dfrac{1}{n} \sum_i x_i^{1-\varepsilon}$, de donde $\xi = M_{1-\varepsilon}(\mathbf{x})$. Para $\varepsilon = 1$, $\ln \xi = \dfrac{1}{n} \sum_i \ln x_i$, de modo que $\xi = G$ por el Teorema 2.5. La unicidad se debe a que $t \mapsto \tfrac{t^{1-\varepsilon}}{1-\varepsilon}$ y $t \mapsto \ln t$ son estrictamente crecientes.
$\blacksquare$

Por tanto, $A_\varepsilon$ es la fracción del ingreso medio que podría sacrificarse, repartiendo el total por igual, sin disminuir el bienestar social. Para $\varepsilon = 0$, el bienestar es la suma de los ingresos, que no depende del reparto, y $A_0 = 0$.

**Proposición 7.8 (Propiedades del índice de Atkinson):**

1. $A_\varepsilon < 1$ y $A_\varepsilon \geq 0$. Para $\varepsilon > 0$, $A_\varepsilon = 0$ si y solo si todos los datos son iguales; para $\varepsilon = 0$, $A_0 = 0$ siempre.
2. $A_\varepsilon(a\mathbf{x}) = A_\varepsilon(\mathbf{x})$ para $a > 0$.
3. $A_1 = 1 - e^{-L}$, con $L = \dfrac{1}{n} \sum_{i=1}^{n} \ln \dfrac{\bar{x}}{x_i}$.
4. Cuando $\varepsilon \to \infty$, $A_\varepsilon \to 1 - \dfrac{x_{(1)}}{\bar{x}}$.

**Demostración:**
1. Como $x_i > 0$, $M_{1-\varepsilon} > 0$ y $A_\varepsilon < 1$. La desigualdad $M_{1-\varepsilon} \leq \bar{x}$, equivalente a $A_\varepsilon \geq 0$, se demostró para $\varepsilon = 1$ ($G \leq \bar{x}$) y para $\varepsilon = 2$ ($H \leq G \leq \bar{x}$) en el Teorema 2.7. Para $\varepsilon$ arbitrario, tanto la desigualdad como su caso de igualdad se deducen de que $M_p$ es estrictamente creciente en $p$ cuando los datos no son todos iguales, resultado que se difiere a la desigualdad de Jensen del curso de probabilidad (Sección 2.10).
2. Por homogeneidad, $M_p(a\mathbf{x}) = a\,M_p(\mathbf{x})$, y $\overline{a\mathbf{x}} = a\bar{x}$.
3. Por el Teorema 2.5, $\ln G = \tfrac{1}{n}\sum \ln x_i$, de modo que $L = \ln \bar{x} - \ln G$ y $e^{-L} = G/\bar{x}$.
4. Por la Proposición 2.8, $M_p \to x_{(1)}$ cuando $p \to -\infty$.
$\blacksquare$

La cantidad $L$ de la propiedad 3 se denomina *desviación logarítmica media* o índice de Theil $L$. De la propiedad 4 se deduce que, para una aversión muy grande, el bienestar depende únicamente del menor ingreso (criterio *maximin*, asociado a John Rawls), y que el índice resulta cercano a $1 - x_{(1)}/\bar{x}$.

**Ejemplo 7.6 (Salarios):**
Para los salarios, con $\bar{x} = 3.293$, las medias de potencias $M_{1-\varepsilon}$ y los índices de Atkinson son:

| $\varepsilon$ | $M_{1-\varepsilon}$ | $A_\varepsilon$ |
|:-------------:|:-------------------:|:---------------:|
| $0$ | $3.293$ | $0$ |
| $0.5$ | $2.821$ | $0.144$ |
| $1$ | $2.496$ | $0.242$ |
| $2$ | $2.119$ | $0.357$ |
| $5$ | $1.692$ | $0.486$ |
| $\to \infty$ | $1.2$ | $0.636$ |

Con $\varepsilon = 1$, $A_1 = 0.242$: un reparto en el que todos ganan $2\,496$ dólares produce el mismo bienestar que el reparto actual, cuyo salario medio es de $3\,293$. Es decir, desde ese criterio, la desigualdad "cuesta" el $24.2\%$ del salario medio. El índice crece con $\varepsilon$ porque los salarios más bajos, que son los menores de la muestra, pesan cada vez más.

**Aplicaciones:**

- **Economía:** el índice de Theil se usa para descomponer la desigualdad de una región en la que existe entre países y la que existe dentro de ellos; el de Atkinson, para comparar cómo cambia la desigualdad según cuánto se pondere a los más pobres.
- **Teoría de la información:** el índice de Theil es la redundancia de un conjunto de participaciones, es decir, la diferencia entre la entropía máxima y la observada.
- **Segregación y diversidad:** el índice de Theil se utiliza también para medir cuánto se concentra una población en ciertos grupos.

### 7.4 Qué medida de concentración usar

Todas las medidas de esta sección son invariantes ante cambios de escala (Proposiciones 7.3 y 7.8) y requieren datos no negativos. Difieren en lo que informan:

| Medida | Qué resume | Propiedad destacada |
|:-------|:-----------|:--------------------|
| Curva de Lorenz | Todo el reparto, gráficamente | Muestra en qué tramo de la población se acumula el total |
| Índice de Gini | El área entre la curva y la diagonal | Un solo número; no es descomponible de forma aditiva; curvas distintas pueden dar el mismo valor |
| Índice de Theil (opcional) | La distancia entre la entropía máxima y la observada | Descomponible en una parte dentro y otra entre grupos |
| Índice de Atkinson (opcional) | El bienestar perdido por la desigualdad, con aversión $\varepsilon$ | Explicita el criterio: más $\varepsilon$ pesa más lo que ocurre entre los menores ingresos |

Como regla práctica, el par curva de Lorenz e índice de Gini es el punto de partida para describir un reparto. Si interesa distinguir cuánta desigualdad hay entre grupos y cuánta dentro de ellos, se usa el índice de Theil; si se desea hacer explícito cuánto se pondera a los más desfavorecidos, el de Atkinson.

---

## 8. Datos complejos y datos angulares (Opcional)

No todos los datos son números reales sueltos. Una señal de radio se describe mediante dos mediciones simultáneas, su componente en fase y su componente en cuadratura, que solo tienen sentido juntas. Una dirección de viento, la hora del día en que llega un cliente o el ángulo de un enlace molecular no se sitúan sobre una recta, sino sobre un círculo. En ambos casos conviene representar cada observación como un **número complejo** $z = x + iy$, es decir, como un punto del plano, y preguntarse qué significan allí la media y la dispersión. Esta sección es opcional y presupone la aritmética de los números complejos: módulo $|z| = \sqrt{x^2 + y^2}$, conjugado y forma polar $z = |z|\,e^{i\theta}$.

> **Nota histórica:** el plano complejo recibe el nombre de plano de Argand o de Gauss. Aunque los diagramas llevan el nombre de Jean-Robert Argand (1768-1822), fueron descritos por primera vez por el agrimensor y matemático noruego-danés Caspar Wessel (1745-1818).

### 8.1 Media y varianza de datos complejos

Sean $z_k = x_k + i y_k$, con $k = 1, \ldots, n$, observaciones complejas. Se denotan $S_x^2$ y $S_y^2$ las varianzas muestrales de las partes real e imaginaria, y $C_{xy} = \dfrac{1}{n-1} \sum_k (x_k - \bar{x})(y_k - \bar{y})$ su covarianza muestral.

**Definición 8.1 (Media de datos complejos):**
La **media** de $z_1, \ldots, z_n$ es:

$$
\bar{z} = \dfrac{1}{n} \sum_{k=1}^{n} z_k = \bar{x} + i\,\bar{y}
$$

Es el centroide de la nube de puntos en el plano complejo.

**Proposición 8.1 (Propiedades de la media compleja):**

1. Si $w_k = \alpha z_k + \beta$ con $\alpha, \beta \in \mathbb{C}$, entonces $\bar{w} = \alpha \bar{z} + \beta$.
2. $\sum_{k=1}^{n} (z_k - \bar{z}) = 0$.
3. Para todo $c \in \mathbb{C}$, $\displaystyle \sum_{k=1}^{n} |z_k - c|^2 = \sum_{k=1}^{n} |z_k - \bar{z}|^2 + n\,|\bar{z} - c|^2$. En consecuencia, $\bar{z}$ es el único punto del plano que minimiza la suma de los cuadrados de las distancias a los datos.

**Demostración:**
1. y 2. Se demuestran como los Teoremas 2.1 y 2.2, pues solo usan la linealidad de la suma, que es válida para coeficientes complejos.

3. Se usa la identidad $|a + b|^2 = |a|^2 + |b|^2 + 2\,\text{Re}(a\,\bar{b})$ con $a = z_k - \bar{z}$ y $b = \bar{z} - c$:

$$
\begin{align}
\sum_{k=1}^{n} |z_k - c|^2 &= \sum_{k=1}^{n} |z_k - \bar{z}|^2 + n\,|\bar{z} - c|^2 + 2\,\text{Re}\left( \sum_{k=1}^{n} (z_k - \bar{z})\, \overline{(\bar{z} - c)} \right) \\
&= \sum_{k=1}^{n} |z_k - \bar{z}|^2 + n\,|\bar{z} - c|^2
\end{align}
$$

donde el último sumando se anula por la propiedad 2. El segundo término es no negativo y se anula si y solo si $c = \bar{z}$.
$\blacksquare$

La propiedad 1 incluye como casos particulares las traslaciones ($\alpha = 1$), los cambios de escala ($\alpha > 0$ real) y las rotaciones alrededor del origen ($|\alpha| = 1$). La propiedad 3 es el análogo del Teorema 2.3.

Para medir la dispersión no basta con copiar la varianza real. Si se elevara al cuadrado una desviación puramente imaginaria, por ejemplo $i$, se obtendría $i^2 = -1$, y desviaciones de distinta dirección podrían compensarse entre sí. Lo natural es medir cada desviación por su distancia al centroide, que es su módulo.

**Definición 8.2 (Varianza de datos complejos):**
La **varianza** es:

$$
S_z^2 = \dfrac{1}{n-1} \sum_{k=1}^{n} |z_k - \bar{z}|^2
$$

**Proposición 8.2 (Varianza compleja y varianzas de las partes):**

1. $S_z^2 = S_x^2 + S_y^2$.
2. Si $w_k = \alpha z_k + \beta$, entonces $S_w^2 = |\alpha|^2\, S_z^2$. En particular, no cambia con traslaciones ni rotaciones.

**Demostración:**
1. Como $|z_k - \bar{z}|^2 = (x_k - \bar{x})^2 + (y_k - \bar{y})^2$, se suma sobre $k$ y se divide entre $n - 1$.
2. Por la Proposición 8.1, $w_k - \bar{w} = \alpha (z_k - \bar{z})$, de modo que $|w_k - \bar{w}|^2 = |\alpha|^2\, |z_k - \bar{z}|^2$.
$\blacksquare$

La varianza compleja es un número real no negativo que mide el tamaño total de la nube, pero no distingue una nube circular de una alargada. Para capturar su forma se define una segunda cantidad que sí usa el cuadrado ordinario.

**Definición 8.3 (Pseudo-varianza):**
La **pseudo-varianza** (o varianza de relación) es:

$$
\tau = \dfrac{1}{n-1} \sum_{k=1}^{n} (z_k - \bar{z})^2
$$

En general, $\tau$ es un número complejo.

**Proposición 8.3 (Propiedades de la pseudo-varianza):**

1. $\tau = (S_x^2 - S_y^2) + 2i\,C_{xy}$.
2. $|\tau| \leq S_z^2$, con igualdad si y solo si los puntos están alineados sobre una recta que pasa por $\bar{z}$.
3. Si $w_k = e^{i\theta} z_k$ (rotación de ángulo $\theta$), entonces $S_w^2 = S_z^2$ y $\tau_w = e^{2i\theta}\,\tau$.
4. $\tau = 0$ si y solo si $S_x^2 = S_y^2$ y $C_{xy} = 0$.

**Demostración:**
1. Como $(a + ib)^2 = a^2 - b^2 + 2iab$ con $a = x_k - \bar{x}$ y $b = y_k - \bar{y}$, se suma sobre $k$ y se divide entre $n - 1$.
2. Con $d_k = z_k - \bar{z}$, por la desigualdad triangular, $\left| \sum_k d_k^2 \right| \leq \sum_k |d_k|^2$. La igualdad se da si y solo si todos los $d_k^2$ no nulos tienen el mismo argumento, es decir, si todos los $d_k$ son múltiplos reales, positivos o negativos, de un mismo número complejo unitario, lo cual equivale a que los puntos estén alineados sobre una recta por $\bar{z}$.
3. Por la Proposición 8.1, $w_k - \bar{w} = e^{i\theta}(z_k - \bar{z})$, de modo que $(w_k - \bar{w})^2 = e^{2i\theta}(z_k - \bar{z})^2$. El valor de $S_w^2$ se sigue de la Proposición 8.2.
4. Es consecuencia de la propiedad 1: un número complejo es nulo si y solo si lo son sus partes real e imaginaria.
$\blacksquare$

La pseudo-varianza tiene un significado geométrico preciso. Para una dirección fijada por el ángulo $\varphi$, el valor $\text{Re}\left( e^{-i\varphi} z_k \right) = x_k \cos\varphi + y_k \sin\varphi$ es la proyección del dato sobre esa dirección.

**Proposición 8.4 (Varianza en una dirección):**
La varianza muestral de las proyecciones de los datos sobre la dirección $\varphi$ es:

$$
\dfrac{S_z^2 + \text{Re}\left( \tau\, e^{-2i\varphi} \right)}{2}
$$

En consecuencia, la mayor y la menor varianza posibles en una dirección son $\dfrac{S_z^2 + |\tau|}{2}$ y $\dfrac{S_z^2 - |\tau|}{2}$; la primera se alcanza en la dirección $\varphi = \tfrac{1}{2} \arg \tau$ y la segunda en la dirección perpendicular.

**Demostración:**
La varianza de las proyecciones es $S_x^2 \cos^2\varphi + 2C_{xy} \sin\varphi \cos\varphi + S_y^2 \sin^2\varphi$. Con $\cos^2\varphi = \tfrac{1 + \cos 2\varphi}{2}$, $\sin^2\varphi = \tfrac{1 - \cos 2\varphi}{2}$ y $2\sin\varphi\cos\varphi = \sin 2\varphi$:

$$
\begin{align}
&= \dfrac{S_x^2 + S_y^2}{2} + \dfrac{S_x^2 - S_y^2}{2} \cos 2\varphi + C_{xy} \sin 2\varphi \\
&= \dfrac{1}{2} \left[ S_z^2 + (S_x^2 - S_y^2) \cos 2\varphi + 2C_{xy} \sin 2\varphi \right] \\
&= \dfrac{1}{2} \left[ S_z^2 + \text{Re}\left( \tau\, e^{-2i\varphi} \right) \right]
\end{align}
$$

pues, por la Proposición 8.3, $\text{Re}\left( \tau\, e^{-2i\varphi} \right) = \text{Re}\left[ \left( (S_x^2 - S_y^2) + 2iC_{xy} \right) (\cos 2\varphi - i \sin 2\varphi) \right] = (S_x^2 - S_y^2)\cos 2\varphi + 2C_{xy} \sin 2\varphi$. Finalmente, $\text{Re}\left( \tau\, e^{-2i\varphi} \right) = |\tau| \cos(2\varphi - \arg\tau)$, que varía entre $-|\tau|$ y $|\tau|$, y alcanza el máximo cuando $2\varphi = \arg\tau$ y el mínimo cuando $2\varphi = \arg\tau + \pi$.
$\blacksquare$

La varianza compleja $S_z^2$ da, entonces, el tamaño total de la nube, y la pseudo-varianza da su forma: $|\tau|/S_z^2 \in [0, 1]$ es $0$ para una nube con la misma varianza en todas las direcciones y $1$ para una nube degenerada en una recta, y $\tfrac{1}{2}\arg\tau$ es la dirección en la que la nube se extiende más. Cuando $\tau = 0$, los datos centrados se denominan **propios** (en inglés, *proper*) en el procesamiento de señales.

**Ejemplo 8.1 (Una nube alargada):**
Sean los cinco datos $z = (1 + i,\ 2 + 3i,\ 3 + 2i,\ 4 + 5i,\ 5 + 4i)$. Su media es $\bar{z} = 3 + 3i$, y las desviaciones son $(-2 - 2i,\ -1,\ -i,\ 1 + 2i,\ 2 + i)$. Las varianzas y la covarianza de las partes son $S_x^2 = S_y^2 = 2.5$ y $C_{xy} = 2$, de modo que:

$$
S_z^2 = 2.5 + 2.5 = 5, \qquad \tau = (2.5 - 2.5) + 2i\,(2) = 4i
$$

Entonces $|\tau| = 4$, $\arg\tau = 90^\circ$ y $|\tau|/S_z^2 = 0.8$: la nube es fuertemente alargada. Por la Proposición 8.4, la varianza máxima es $\tfrac{5 + 4}{2} = 4.5$, y se alcanza en la dirección $\varphi = 45^\circ$; la mínima es $\tfrac{5 - 4}{2} = 0.5$, en la dirección $135^\circ$. Las partes real e imaginaria, por separado, tienen la misma varianza ($2.5$ en las direcciones de $0^\circ$ y $90^\circ$), de modo que, observadas solo por sus componentes, no revelan que los datos se concentran sobre la diagonal.

Si la nube se gira $90^\circ$, $w_k = i z_k$, se tiene $S_w^2 = 5$ y $\tau_w = i^2 \tau = -4i$, con el mismo módulo $4$ y la dirección principal en $\tfrac{1}{2} \arg(-4i) = -45^\circ$, equivalente a $135^\circ$, que es la dirección principal original ($45^\circ$) girada $90^\circ$.

**Aplicaciones:**

- **Telecomunicaciones y procesamiento de señales:** las señales con amplitud y fase, como los símbolos de las modulaciones de amplitud en cuadratura (QAM), se describen con números complejos. La media, la varianza y la pseudo-varianza del ruido recibido caracterizan su comportamiento, y la hipótesis de que $\tau = 0$ es una suposición habitual en comunicaciones inalámbricas.

### 8.2 Datos angulares: media circular

La hora del día es un dato cíclico: las $23{:}00$ y la $1{:}00$ de la mañana distan dos horas, y no veintidós. Si tres clientes llegan a las $23$, $1$ y $2$ horas, la media aritmética, $8.7$ horas, es decir, las $8{:}40$ de la mañana, no describe a ninguno de ellos. De igual modo, $180^\circ$ no es una media razonable de $2^\circ$ y $358^\circ$. La media aritmética supone que los datos viven sobre una recta, y los ángulos viven sobre un círculo.

La solución consiste en representar cada ángulo $\theta_k$ como el punto $w_k = e^{i\theta_k}$ de la circunferencia unitaria, promediar esos puntos y tomar el argumento del resultado.

**Definición 8.4 (Media circular y longitud resultante):**
Dados los ángulos $\theta_1, \ldots, \theta_n$ (en radianes), sea

$$
\bar{w} = \dfrac{1}{n} \sum_{k=1}^{n} e^{i\theta_k} = \bar{C} + i\,\bar{S}, \qquad \bar{C} = \dfrac{1}{n} \sum_{k=1}^{n} \cos\theta_k, \quad \bar{S} = \dfrac{1}{n} \sum_{k=1}^{n} \sin\theta_k
$$

La **longitud resultante** es $R = |\bar{w}| = \sqrt{\bar{C}^2 + \bar{S}^2}$. Si $R > 0$, la **media circular** es $\bar{\theta} = \arg \bar{w}$ (módulo $2\pi$), de modo que $\bar{w} = R\,e^{i\bar{\theta}}$. La **varianza circular** es $V = 1 - R$.

**Proposición 8.5 (Propiedades de la media circular):**

1. $0 \leq R \leq 1$, y $R = 1$ si y solo si todos los ángulos son iguales (módulo $2\pi$). Por tanto, $0 \leq V \leq 1$.
2. Si todos los ángulos se aumentan en $\varphi$, la media circular aumenta en $\varphi$ y $R$ no cambia.
3. Para todo $\varphi \in \mathbb{R}$, $\displaystyle \sum_{k=1}^{n} \left| e^{i\theta_k} - e^{i\varphi} \right|^2 = 2n \left[ 1 - R \cos(\varphi - \bar{\theta}) \right]$. Si $R > 0$, la media circular es el único ángulo (módulo $2\pi$) que minimiza esta suma.
4. $\dfrac{1}{n} \displaystyle \sum_{k=1}^{n} |w_k - \bar{w}|^2 = 1 - R^2$, de modo que $V \leq 1 - R^2 \leq 2V$.

**Demostración:**
1. Por la desigualdad triangular, $|\bar{w}| \leq \tfrac{1}{n} \sum_k |e^{i\theta_k}| = 1$, con igualdad si y solo si todos los números complejos unitarios tienen el mismo argumento.
2. $\tfrac{1}{n} \sum_k e^{i(\theta_k + \varphi)} = e^{i\varphi}\,\bar{w}$, cuyo módulo es $R$ y cuyo argumento es $\bar{\theta} + \varphi$.
3. Como $|e^{i\theta_k}| = |e^{i\varphi}| = 1$, se tiene $\left| e^{i\theta_k} - e^{i\varphi} \right|^2 = 2 - 2\cos(\theta_k - \varphi)$. Además, $\sum_k \cos(\theta_k - \varphi) = \text{Re}\left( e^{-i\varphi} \sum_k e^{i\theta_k} \right) = n\,\text{Re}\left( R\,e^{i(\bar{\theta} - \varphi)} \right) = nR \cos(\varphi - \bar{\theta})$. La suma es mínima cuando $\cos(\varphi - \bar{\theta}) = 1$, es decir, $\varphi = \bar{\theta}$ módulo $2\pi$.
4. Es la Proposición 8.1 (propiedad 3) con $c = 0$, dividida entre $n$: $\tfrac{1}{n} \sum_k |w_k - \bar{w}|^2 = \tfrac{1}{n} \sum_k |w_k|^2 - |\bar{w}|^2 = 1 - R^2$. Como $1 - R^2 = (1 - R)(1 + R)$ y $1 \leq 1 + R \leq 2$, se obtiene la acotación.
$\blacksquare$

La propiedad 3 es el análogo del Teorema 2.3: la media circular es el ángulo cuya dirección minimiza la suma de los cuadrados de las distancias a los datos. Cuando $R = 0$, los datos se reparten de manera equilibrada alrededor del círculo y la media circular no está definida.

**Ejemplo 8.2 (Ángulos):**
Para los ángulos $350^\circ$, $10^\circ$ y $20^\circ$, la media aritmética es $126.7^\circ$. En cambio:

$$
\bar{C} = \dfrac{0.9848 + 0.9848 + 0.9397}{3} \approx 0.9698, \qquad \bar{S} = \dfrac{-0.1736 + 0.1736 + 0.3420}{3} \approx 0.1140
$$

de modo que $R = \sqrt{0.9698^2 + 0.1140^2} \approx 0.976$, $\bar{\theta} = \arctan\dfrac{0.1140}{0.9698} \approx 6.7^\circ$ y $V \approx 0.024$. La media circular, $6.7^\circ$, se sitúa en el centro del grupo, y la longitud resultante, cercana a $1$, indica que los ángulos están muy concentrados. Para los ángulos $0^\circ$, $90^\circ$, $180^\circ$ y $270^\circ$, en cambio, $\bar{w} = 0$: $R = 0$, $V = 1$ y la media circular no está definida.

**Ejemplo 8.3 (Hora de llegada):**
Para convertir horas en ángulos se usa que $24$ horas equivalen a $360^\circ$, es decir, $15^\circ$ por hora. Las llegadas a las $23$, $1$ y $2$ horas corresponden a $345^\circ$, $15^\circ$ y $30^\circ$. Se obtiene $R \approx 0.947$ y $\bar{\theta} \approx 10.1^\circ$, es decir, $10.1/15 \approx 0.68$ horas: la hora media de llegada es aproximadamente las $0{:}41$, frente a las $8{:}40$ de la media aritmética.

> **Observación:** la media circular y la varianza $V = 1 - R$ son los análogos de $\bar{x}$ y $S^2$ para datos angulares, pero no heredan todas sus propiedades: por ejemplo, $V$ está acotada en $[0, 1]$ y no se mide en el cuadrado de las unidades del ángulo. La estadística de datos direccionales (circulares y esféricos) es una rama propia de la estadística.

**Aplicaciones:**

- **Meteorología y navegación:** direcciones del viento, rumbos y orientaciones.
- **Datos temporales cíclicos:** hora del día, día de la semana, mes del año.
- **Química y biología estructural:** ángulos diedros en moléculas y orientaciones de proteínas.

---

## 9. Resumen conceptual

Esta clase presentó cinco familias de estadísticos: de tendencia central, de posición, de dispersión, de forma y de concentración, además de la extensión opcional a datos complejos y angulares. Cada una responde una pregunta distinta sobre los datos. En este resumen se reúnen sus definiciones, sus propiedades principales y las decisiones de convención que se tomaron.

### 9.1 Tabla de síntesis

Las siguientes tablas reúnen, por familia, las medidas estudiadas con su definición y su propiedad principal.
**Medidas de tendencia central** (Sección 2). Las medias geométrica, armónica y cuadrática se definen para datos positivos (la cuadrática, para cualquier dato real).

| Medida | Definición | Propiedad clave | Resistente a atípicos |
|:-------|:-----------|:----------------|:---------------------:|
| Media aritmética $\bar{x}$ | $\tfrac{1}{n}\sum x_i$ | Punto de equilibrio; minimiza $\sum (x_i - c)^2$ | No |
| Media ponderada $\bar{x}_w$ | $\sum w_i x_i / \sum w_i$ | Incluye a la media y a los datos agrupados como casos particulares | No |
| Media geométrica $G$ | $\left( \prod x_i \right)^{1/n}$ | $\ln G$ es la media de los $\ln x_i$; factores de crecimiento | No |
| Media armónica $H$ | $n / \sum (1/x_i)$ | Velocidad media con tramos de igual longitud | No |
| Media cuadrática (RMS) | $\sqrt{\tfrac{1}{n}\sum x_i^2}$ | $\text{RMS}^2 = \bar{x}^2 + m_2$ | No |
| Mediana $Me$ | Valor central de los datos ordenados | Minimiza $\sum \lvert x_i - c \rvert$ | Sí (punto de ruptura $\lceil n/2 \rceil / n$) |
| Moda $Mo$ | Valor de mayor frecuencia | Única medida para variables nominales | Sí |
| Media recortada $\bar{x}_\alpha$ | Media sin los $g$ menores y los $g$ mayores | Compromiso entre la media y la mediana | Sí (punto de ruptura $(g+1)/n$) |

**Medidas de posición** (Sección 3).

| Medida | Definición | Propiedad clave |
|:-------|:-----------|:----------------|
| Cuantil de orden $p$ | Valor $q$ con $\#\{x_i \leq q\} \geq np$ y $\#\{x_i \geq q\} \geq n(1-p)$ | No es único cuando $np$ es entero |
| Cuantil Tipo 7 (convención del curso) | $x_{(h)}$ con $h = 1 + (n-1)p$ | Es el que calculan Python y Excel; equivariante ante $y = ax + b$ con $a > 0$ |
| Cuartiles, deciles, percentiles | Cuantiles de orden $k/4$, $k/10$, $k/100$ | $Q_2 = Me$ |
| Resumen de cinco números | $\left( x_{(1)}, Q_1, Q_2, Q_3, x_{(n)} \right)$ | Es lo que representa el diagrama de caja |

**Medidas de dispersión** (Sección 4).

| Medida | Definición | Propiedad clave | Resistente a atípicos |
|:-------|:-----------|:----------------|:---------------------:|
| Rango $R$ | $x_{(n)} - x_{(1)}$ | Solo usa los extremos | No |
| RIC | $Q_3 - Q_1$ | Amplitud del $50\%$ central | Sí |
| Varianza $S^2$ | $\tfrac{1}{n-1}\sum (x_i - \bar{x})^2$ | $(n-1)S^2 = $ variación dentro $+$ entre grupos | No |
| Desviación estándar $S$ | $\sqrt{S^2}$ | Mismas unidades que los datos; cota de Chebyshev | No |
| Coeficiente de variación | $S / \lvert \bar{x} \rvert$ | No depende de la escala; solo para escala de razón | No |
| Desviación absoluta media $D$ | $\tfrac{1}{n}\sum \lvert x_i - \bar{x} \rvert$ | $\tfrac{1}{n}\sum \lvert x_i - Me \rvert \leq D$ | Moderada |
| MAD | Mediana de $\lvert x_i - Me \rvert$ | $1.4826\,\text{MAD}$ es comparable con $S$ en datos normales | Sí |
| Puntaje $z$ | $(x_i - \bar{x})/S$ | Media $0$ y desviación estándar $1$ | No |

**Momentos y medidas de forma** (Secciones 5 y 6).

| Medida | Definición | Propiedad clave |
|:-------|:-----------|:----------------|
| Momentos $a_r$ y $m_r$ | $\tfrac{1}{n}\sum x_i^r$ y $\tfrac{1}{n}\sum (x_i - \bar{x})^r$ | $m_2 = a_2 - a_1^2$ y $S^2 = \tfrac{n}{n-1}\, m_2$ |
| Asimetría de Fisher $g_1$ | $m_3 / m_2^{3/2}$ | Su signo indica el lado de la cola larga; invariante con $a > 0$ |
| Asimetría de Pearson $\text{Sk}_1$, $\text{Sk}_2$ | $(\bar{x} - Mo)/S$ y $3(\bar{x} - Me)/S$ | $\lvert \text{Sk}_2 \rvert \leq 3$ |
| Asimetría de Bowley $A_Q$ | $\dfrac{(Q_3 - Me) - (Me - Q_1)}{Q_3 - Q_1}$ | Está en $[-1, 1]$ y es resistente |
| Curtosis $\beta_2$ y exceso $g_2$ | $m_4/m_2^2$ y $\beta_2 - 3$ | Mide el peso de las colas, no la "punta"; $\beta_2 \geq 1 + g_1^2$ |
| $G_1$ y $G_2$ | $\tfrac{\sqrt{n(n-1)}}{n-2}\, g_1$ y $\tfrac{n-1}{(n-2)(n-3)}\left[(n+1)g_2 + 6\right]$ | Son las versiones que calculan Excel y `pandas` |

**Medidas de concentración** (Sección 7).

| Medida | Definición | Propiedad clave |
|:-------|:-----------|:----------------|
| Curva de Lorenz | Poligonal por $\left( \tfrac{i}{n}, L_i \right)$, con $L_i$ la fracción del total de los $i$ menores | Está bajo la diagonal y es convexa |
| Índice de Gini $I_G$ | $1 - 2B = \dfrac{\sum (2k - n - 1)\, x_{(k)}}{nX}$ | $0 \leq I_G \leq \tfrac{n-1}{n}$; no cambia con la escala |
| Índice de Theil (opcional) | $\ln n - H$, con $H$ la entropía de las participaciones | $0 \leq \text{Th} \leq \ln n$; descomponible en dentro y entre grupos |
| Índice de Atkinson (opcional) | $1 - M_{1-\varepsilon}/\bar{x}$ | El parámetro $\varepsilon$ expresa la aversión a la desigualdad |

**Datos complejos y angulares** (Sección 8, opcional).

| Medida | Definición | Propiedad clave |
|:-------|:-----------|:----------------|
| Media compleja $\bar{z}$ | $\tfrac{1}{n}\sum z_k$ | Centroide; minimiza $\sum \lvert z_k - c \rvert^2$ |
| Varianza compleja $S_z^2$ | $\tfrac{1}{n-1}\sum \lvert z_k - \bar{z} \rvert^2$ | $S_x^2 + S_y^2$; no cambia con rotaciones |
| Pseudo-varianza $\tau$ | $\tfrac{1}{n-1}\sum (z_k - \bar{z})^2$ | La varianza en la dirección $\varphi$ es $\tfrac{1}{2}\left[ S_z^2 + \text{Re}(\tau e^{-2i\varphi}) \right]$ |
| Media circular $\bar{\theta}$ y longitud resultante $R$ | $\arg \bar{w}$ y $\lvert \bar{w} \rvert$, con $\bar{w} = \tfrac{1}{n}\sum e^{i\theta_k}$ | $0 \leq R \leq 1$; la varianza circular es $1 - R$ |

### 9.2 El centro y la dispersión como pareja

Varias medidas de esta clase no son hallazgos aislados. Cada medida de tendencia central es el valor $c$ que minimiza una medida de error entre los datos y $c$, y el valor mínimo de ese error, promediado sobre los datos, es una medida de dispersión.

| Error que se minimiza | Centro | Dispersión asociada |
|:----------------------|:-------|:--------------------|
| $\sum (x_i - c)^2$ | Media $\bar{x}$ (Teorema 2.3) | Varianza (con divisor $n$, $m_2$) |
| $\sum \lvert x_i - c \rvert$ | Mediana $Me$ (Teorema 2.6) | Desviación absoluta respecto de la mediana (Proposición 4.5) |
| $\#\{ i : x_i \neq c \}$ | Moda $Mo$ | Proporción de datos distintos de la moda |
| $\max_i \lvert x_i - c \rvert$ | Punto medio $\tfrac{1}{2}\left( x_{(1)} + x_{(n)} \right)$ | Semirrango $R/2$ |

Los dos últimos casos se justifican con un argumento breve. El número de datos distintos de $c$ es $n - \#\{ i : x_i = c \}$, que es mínimo cuando $c$ es un valor de mayor frecuencia. Además, $\max_i \lvert x_i - c \rvert = \max\left( c - x_{(1)},\ x_{(n)} - c \right)$ y la suma de ambos términos es constante e igual a $R$, de modo que el máximo es al menos $R/2$, con igualdad si y solo si $c = \tfrac{1}{2}(x_{(1)} + x_{(n)})$.

Esta correspondencia explica el comportamiento de cada medida. Los errores que dan más peso a los datos lejanos (el cuadrado y el máximo) conducen a medidas sensibles a valores atípicos; los que no lo hacen (el valor absoluto y el conteo) conducen a medidas resistentes.

### 9.3 Convenciones del curso

Como varias medidas admiten más de una definición, se fijaron las siguientes convenciones, que deben tenerse presentes al comparar resultados con los de un programa (como Excel o Python) o de un texto.
| Tema | Convención |
|:-----|:-----------|
| Tamaños | $N$ es el tamaño de la población y $n$ el de la muestra |
| Varianza y desviación estándar muestrales | Divisor $n-1$ ($S^2$, $S$) |
| Momentos | Divisor $n$ ($a_r$, $m_r$); por tanto, $m_2 \neq S^2$ |
| Cuantiles | Tipo 7: $x_{(h)}$ con $h = 1 + (n-1)p$ |
| Asimetría y curtosis | $g_1$ y $g_2$ con divisor $n$; el exceso de curtosis resta $3$ |
| Índice de Gini | Se denota $I_G$ para no confundirlo con la media geométrica $G$ |
| Datos agrupados | Se usan marcas de clase; los resultados son aproximados |

Al comparar con un programa, conviene verificar qué convención usa: `scipy.stats.skew` calcula $g_1$, mientras que `pandas.Series.skew` calcula $G_1$; `numpy.var` divide entre $n$ por defecto y `pandas.Series.var` entre $n-1$.

### 9.4 Guía de elección

La elección del resumen depende de la escala de la variable, de la forma de la distribución y de la presencia de valores atípicos.
| Situación | Resumen recomendado |
|:----------|:--------------------|
| Variable cualitativa nominal | Moda |
| Variable ordinal | Mediana, cuantiles, RIC |
| Datos numéricos, simétricos y sin atípicos relevantes | $\bar{x}$ y $S$; $g_1$ y $g_2$ para la forma |
| Datos asimétricos o con atípicos | $Me$ y RIC o MAD; $A_Q$; media recortada como alternativa |
| Factores de crecimiento, tasas o índices | Media geométrica |
| Razones con numerador fijo (por ejemplo, velocidades) | Media armónica |
| Magnitud de cantidades con signo | RMS |
| Observaciones de importancia desigual | Media ponderada |
| Comparar la variabilidad de conjuntos en escalas distintas | Coeficiente de variación (escala de razón) |
| Describir cómo se reparte un total | Curva de Lorenz e índice de Gini; Theil si se necesita separar grupos |
| Datos complejos | $\bar{z}$, $S_z^2$ y $\tau$ |
| Datos angulares o cíclicos | Media circular y longitud resultante $R$ |

Como regla práctica, conviene calcular siempre la media y la mediana: si son similares, los datos son aproximadamente simétricos y cualquiera de las dos resume bien su centro; si difieren mucho, hay asimetría o valores extremos.

### 9.5 Resultados principales

La siguiente tabla lista los resultados demostrados que sostienen el resto de la clase.
| Resultado | Enunciado | Sección |
|:----------|:----------|:-------:|
| Teorema 2.2 | $\sum (x_i - \bar{x}) = 0$ | 2.1 |
| Teorema 2.3 | $\sum (x_i - c)^2 = \sum (x_i - \bar{x})^2 + n(\bar{x} - c)^2$; la media minimiza el error cuadrático | 2.1 |
| Teorema 2.6 | La mediana minimiza el error absoluto | 2.7 |
| Proposición 2.5 | Puntos de ruptura: $1/n$ para la media y $\lceil n/2 \rceil / n$ para la mediana | 2.7 |
| Teorema 2.7 | $H \leq G \leq \bar{x} \leq \text{RMS}$ | 2.10 |
| Proposición 3.1 | El cuantil es único si $np$ no es entero; si lo es, es todo el intervalo $[x_{(np)}, x_{(np+1)}]$ | 3.1 |
| Teorema 4.1 | Desigualdad de Chebyshev: la proporción de datos a $kS$ o más de la media es menor que $1/k^2$ | 4.6 |
| Teorema 4.2 | $(n-1)S^2 = \sum_j (n_j - 1)S_j^2 + \sum_j n_j (\bar{x}_j - \bar{x})^2$ | 4.7 |
| Proposición 5.2 | Momentos centrales a partir de los momentos respecto del origen | 5.1 |
| Proposición 6.3 | $\beta_2 \geq 1 + g_1^2$ | 6.3 |
| Proposición 6.4 | La curtosis proviene de los datos a más de una desviación estándar de la media, salvo una contribución de a lo sumo $\tfrac{1}{4}$ | 6.3 |
| Proposición 7.3 | $0 \leq I_G \leq \tfrac{n-1}{n}$ | 7.2 |
| Proposición 7.6 | $\text{Th} = $ dentro de los grupos $+$ entre los grupos | 7.3 |
| Proposición 8.4 | La varianza en la dirección $\varphi$ es $\tfrac{1}{2}\left[ S_z^2 + \text{Re}(\tau e^{-2i\varphi}) \right]$ | 8.1 |

---

## 10. Ejercicios resueltos

### Ejercicio 10.1

Los tiempos de respuesta, en milisegundos, de $11$ solicitudes a un servidor son:

$$
12,\ 15,\ 15,\ 16,\ 18,\ 20,\ 21,\ 22,\ 25,\ 30,\ 95
$$

a) Calcular la media, la mediana y la moda.
b) Calcular la media recortada al $10\%$.
c) Si el último valor fuera $950$ en lugar de $95$, recalcular las tres medidas anteriores.
d) Decidir qué medida resume mejor los tiempos y justificar la elección.

**Solución:**
a) La suma de los datos es $289$, de modo que $\bar{x} = 289/11 \approx 26.27$. Como $n = 11$ es impar, la mediana es el dato central, $x_{(6)} = 20$. El valor que más se repite es $15$ (aparece dos veces), de modo que $Mo = 15$.

b) Con $\alpha = 0.10$, $g = \lfloor 0.10 \cdot 11 \rfloor = 1$. Se descartan el menor ($12$) y el mayor ($95$):

$$
\bar{x}_{0.10} = \dfrac{289 - 12 - 95}{9} = \dfrac{182}{9} \approx 20.22
$$

c) Con $950$ en lugar de $95$, la suma es $1144$:

$$
\begin{align}
\bar{x} &= \dfrac{1144}{11} = 104 \\
Me &= x_{(6)} = 20 \\
\bar{x}_{0.10} &= \dfrac{1144 - 12 - 950}{9} = \dfrac{182}{9} \approx 20.22
\end{align}
$$

La media pasó de $26.27$ a $104$, mientras que la mediana y la media recortada no cambiaron.

d) Un único valor atípico desplaza la media, cuyo punto de ruptura es $1/11$ (Proposición 2.5). La mediana, con punto de ruptura $\lceil 11/2 \rceil / 11 = 6/11$, y la media recortada, con $(g+1)/n = 2/11$ (Proposición 2.7), resisten ese valor. Por tanto, para describir el tiempo típico de respuesta conviene la mediana ($20$ ms) o la media recortada ($20.2$ ms). La media sería engañosa.

### Ejercicio 10.2

a) Un estudiante obtiene calificaciones de $8.5$, $7.0$ y $9.0$ en asignaturas de $4$, $3$ y $2$ créditos. Calcular su promedio ponderado.
b) Una inversión rinde $+20\%$, $-10\%$ y $+50\%$ en tres años consecutivos. Calcular el rendimiento anual medio.
c) Un vehículo recorre $100$ km a $80$ km/h y luego $150$ km a $100$ km/h. Calcular su velocidad media.

**Solución:**
a) Es una media ponderada con pesos iguales a los créditos:

$$
\bar{x}_w = \dfrac{4(8.5) + 3(7.0) + 2(9.0)}{4 + 3 + 2} = \dfrac{73}{9} \approx 8.11
$$

La media aritmética simple, $8.17$, sobreestima el promedio porque otorga el mismo peso a la asignatura de menor peso, que fue la de mejor nota.

b) Los factores de crecimiento son $1.2$, $0.9$ y $1.5$, con producto $1.62$. El factor anual medio es la media geométrica:

$$
G = \sqrt[3]{1.62} \approx 1.1745
$$

El rendimiento anual medio es, por tanto, de aproximadamente $17.4\%$. La media aritmética de los rendimientos, $20\%$, lo sobreestima: con un factor constante de $1.2$ se obtendría $1.2^3 = 1.728 \neq 1.62$.

c) La velocidad media es la distancia total entre el tiempo total. Los tiempos son $100/80 = 1.25$ h y $150/100 = 1.5$ h:

$$
\bar{v} = \dfrac{100 + 150}{1.25 + 1.5} = \dfrac{250}{2.75} \approx 90.9 \text{ km/h}
$$

Es la media armónica de las velocidades ponderada por las distancias (Definición 2.7). La media aritmética simple de las velocidades, $90$, y la ponderada por las distancias, $92$, no corresponden a la velocidad real.

### Ejercicio 10.3

Demostrar que, para dos datos positivos $x_1, x_2$, se cumple $G^2 = \bar{x}\, H$, y deducir de ello que $H \leq G \leq \bar{x}$ sin usar logaritmos.

**Solución:**
Para $n = 2$:

$$
\bar{x} = \dfrac{x_1 + x_2}{2}, \qquad G^2 = x_1 x_2, \qquad H = \dfrac{2}{\dfrac{1}{x_1} + \dfrac{1}{x_2}} = \dfrac{2\,x_1 x_2}{x_1 + x_2}
$$

Entonces:

$$
\bar{x}\, H = \dfrac{x_1 + x_2}{2} \cdot \dfrac{2\,x_1 x_2}{x_1 + x_2} = x_1 x_2 = G^2
$$

Por otra parte, $\bar{x} \geq H$ equivale a $\dfrac{x_1 + x_2}{2} \geq \dfrac{2\,x_1 x_2}{x_1 + x_2}$, es decir, a $(x_1 + x_2)^2 \geq 4\,x_1 x_2$, que es $(x_1 - x_2)^2 \geq 0$. Como $G = \sqrt{\bar{x}\, H}$ es la media geométrica de los números $H \leq \bar{x}$, queda comprendida entre ambos: $H \leq G \leq \bar{x}$. La igualdad se da si y solo si $x_1 = x_2$.
$\blacksquare$

### Ejercicio 10.4

Los siguientes $12$ datos están ordenados:

$$
3,\ 5,\ 6,\ 8,\ 9,\ 10,\ 12,\ 13,\ 15,\ 16,\ 18,\ 41
$$

a) Calcular $Q_1$, $Q_2$, $Q_3$ y $P_{90}$ con la convención del curso (Tipo 7).
b) Calcular el RIC y las barreras interiores y exteriores, y clasificar el dato $41$.
c) Verificar que los resultados son compatibles con la definición de cuantil (Definición 3.1).

**Solución:**
a) Con $n = 12$ y $h = 1 + 11p$:

$$
\begin{align}
Q_1 &: h = 3.75 \Rightarrow x_{(3)} + 0.75\,(x_{(4)} - x_{(3)}) = 6 + 0.75(2) = 7.5 \\
Q_2 &: h = 6.5 \Rightarrow 10 + 0.5(12 - 10) = 11 \\
Q_3 &: h = 9.25 \Rightarrow 15 + 0.25(16 - 15) = 15.25 \\
P_{90} &: h = 10.9 \Rightarrow 16 + 0.9(18 - 16) = 17.8
\end{align}
$$

b) $\text{RIC} = 15.25 - 7.5 = 7.75$. Las barreras son:

$$
\begin{align}
L_I &= 7.5 - 1.5(7.75) = -4.125, & L_S &= 15.25 + 1.5(7.75) = 26.875 \\
E_I &= 7.5 - 3(7.75) = -15.75, & E_S &= 15.25 + 3(7.75) = 38.5
\end{align}
$$

Como $41 > E_S = 38.5$, el dato $41$ es un valor **extremo** (Proposición 11.2 de la Clase 4).

c) Para $p = 0.25$, $np = 3$ es entero, de modo que los cuantiles son todos los valores del intervalo $[x_{(3)}, x_{(4)}] = [6, 8]$; $7.5$ pertenece a él. Para $p = 0.5$, $np = 6$ y el conjunto es $[10, 12]$, que contiene a $11$. Para $p = 0.75$, $np = 9$ y el conjunto es $[15, 16]$, que contiene a $15.25$. Para $p = 0.9$, $np = 10.8$ no es entero y la Proposición 3.1 da el único cuantil $x_{(11)} = 18$: el valor $17.8$ del Tipo 7 no cumple estrictamente la definición, pues es una convención de interpolación (Sección 3.2).

### Ejercicio 10.5

Dos secciones de un curso rindieron la misma prueba. La sección $A$ tiene $n_A = 10$ estudiantes, media $14$ y varianza $4$; la sección $B$ tiene $n_B = 15$, media $12$ y varianza $9$. Calcular la media y la varianza de los $25$ estudiantes juntos, y la fracción de la variación total que se debe a la diferencia entre las secciones.

**Solución:**
Por la Proposición 4.7, la media combinada es:

$$
\bar{x} = \dfrac{10(14) + 15(12)}{25} = \dfrac{320}{25} = 12.8
$$

Por el Teorema 4.2:

$$
\begin{align}
(n-1)S^2 &= \underbrace{9(4) + 14(9)}_{\text{dentro} \,=\, 162} + \underbrace{10(14 - 12.8)^2 + 15(12 - 12.8)^2}_{\text{entre} \,=\, 14.4 + 9.6 \,=\, 24} \\
&= 186
\end{align}
$$

Entonces $S^2 = 186/24 = 7.75$ y $S \approx 2.78$. La variación entre secciones es $24/186 \approx 12.9\%$ de la variación total. El resto se debe a la variación dentro de cada sección. Obsérvese que la varianza combinada, $7.75$, no es el promedio de $4$ y $9$.

### Ejercicio 10.6

En el examen $A$, la media es $70$ y la desviación estándar es $5$; en el examen $B$, son $55$ y $6$. Un estudiante obtuvo $78$ en $A$ y $64$ en $B$.

a) Determinar en cuál de los dos exámenes tuvo mejor desempeño relativo.
b) Según la desigualdad de Chebyshev, acotar la proporción de estudiantes del examen $A$ que obtuvieron entre $55$ y $85$.

**Solución:**
a) Se comparan los puntajes $z$:

$$
z_A = \dfrac{78 - 70}{5} = 1.6, \qquad z_B = \dfrac{64 - 55}{6} = 1.5
$$

En valores absolutos, el estudiante obtuvo $9$ puntos sobre la media en $B$ y $8$ en $A$, pero en términos de desviaciones estándar su desempeño fue ligeramente mejor en $A$ ($1.6$ frente a $1.5$).

b) El intervalo $[55, 85]$ es $\bar{x} \pm 3S$, pues $70 \pm 15$ y $S = 5$. Por el Teorema 4.1, la proporción de datos fuera del intervalo es menor que $1/3^2 = 1/9$, de modo que al menos $1 - 1/9 \approx 88.9\%$ de los estudiantes obtuvo entre $55$ y $85$ puntos.

### Ejercicio 10.7

Para los datos $1,\ 2,\ 3,\ 4,\ 10$:

a) Calcular $g_1$ y $g_2$, y verificar la cota de la Proposición 6.3.
b) Calcular $G_1$ y $G_2$.
c) Calcular el coeficiente de Bowley y compararlo con $g_1$.

**Solución:**
a) La media es $4$ y las desviaciones son $(-3, -2, -1, 0, 6)$:

$$
\begin{align}
m_2 &= \dfrac{9 + 4 + 1 + 0 + 36}{5} = 10 \\
m_3 &= \dfrac{-27 - 8 - 1 + 0 + 216}{5} = 36 \\
m_4 &= \dfrac{81 + 16 + 1 + 0 + 1296}{5} = 278.8
\end{align}
$$

Entonces:

$$
g_1 = \dfrac{36}{10^{3/2}} \approx 1.138, \qquad \beta_2 = \dfrac{278.8}{100} = 2.788, \qquad g_2 = -0.212
$$

La cota se cumple: $\beta_2 = 2.788 \geq 1 + g_1^2 = 1 + 1.296 = 2.296$.

b) Con $n = 5$:

$$
G_1 = \dfrac{\sqrt{5 \cdot 4}}{3}\, g_1 \approx 1.697, \qquad G_2 = \dfrac{4}{3 \cdot 2} \left[ 6(-0.212) + 6 \right] \approx 3.152
$$

Con una muestra tan pequeña, las correcciones son grandes: $G_1$ es un $49\%$ mayor que $g_1$, y $G_2$ cambia incluso el signo del exceso de curtosis.

c) Con el Tipo 7, $Q_1 = 2$, $Me = 3$ y $Q_3 = 4$, de modo que:

$$
A_Q = \dfrac{(4 - 3) - (3 - 2)}{4 - 2} = 0
$$

El coeficiente de Bowley indica ausencia de asimetría, mientras que $g_1 \approx 1.14$ indica una asimetría positiva marcada. La diferencia se debe a que $A_Q$ solo usa los cuartiles y la mediana, y no percibe el dato $10$, que es el que genera la asimetría de $g_1$.

### Ejercicio 10.8

Los ingresos mensuales, en miles de dólares, de cuatro hogares son $2$, $3$, $5$ y $10$.

a) Construir la curva de Lorenz y calcular el índice de Gini.
b) Comparar con el máximo posible para $n = 4$.
c) ¿Qué ocurre con el índice si a todos los hogares se les suman $3$ mil dólares?

**Solución:**
a) Con $X = 20$, las sumas acumuladas son $2, 5, 10, 20$, de modo que $L_1 = 0.10$, $L_2 = 0.25$, $L_3 = 0.50$ y $L_4 = 1$. Por la fórmula (b) de la Proposición 7.2:

$$
I_G = \dfrac{(-3)(2) + (-1)(3) + (1)(5) + (3)(10)}{4 \cdot 20} = \dfrac{26}{80} = 0.325
$$

Con la fórmula (a) se obtiene el mismo resultado: el área bajo la poligonal es $B = \tfrac{1}{4}\left( \tfrac{0.1}{2} + \tfrac{0.1 + 0.25}{2} + \tfrac{0.25 + 0.5}{2} + \tfrac{0.5 + 1}{2} \right) = 0.3375$ y $1 - 2B = 0.325$.

b) El máximo para $n = 4$ es $\tfrac{n-1}{n} = 0.75$, de modo que el índice normalizado es $0.325 \cdot \tfrac{4}{3} \approx 0.433$. Además, el hogar más rico ($u = 0.25$) recibe la mitad del total ($f = 0.5$), y la Proposición 7.4 garantiza $I_G \geq 0.5 - 0.25 = 0.25$, cota que se cumple.

c) Los ingresos pasan a ser $5, 6, 8, 13$ con $X = 32$. El numerador de la fórmula (b) no cambia ($26$), y el denominador pasa a $4 \cdot 32 = 128$:

$$
I_G = \dfrac{26}{128} \approx 0.203
$$

El índice disminuye (Proposición 7.3): sumar una cantidad fija a todos reduce la concentración relativa, aunque las diferencias absolutas no cambien. En cambio, multiplicar todos los ingresos por $10$ no modificaría el índice.

### Ejercicio 10.9 (Opcional)

Cuatro clientes llegan a una tienda a las $22$, $23$, $1$ y $2$ horas. Calcular la hora media de llegada.

**Solución:**
La media aritmética de las horas es $(22 + 23 + 1 + 2)/4 = 12$, es decir, el mediodía, que es la hora más alejada de todas las llegadas. Se convierten las horas en ángulos con $15^\circ$ por hora: $330^\circ$, $345^\circ$, $15^\circ$ y $30^\circ$. Entonces:

$$
\begin{align}
\bar{C} &= \dfrac{\cos 330^\circ + \cos 345^\circ + \cos 15^\circ + \cos 30^\circ}{4} = \dfrac{0.866 + 0.966 + 0.966 + 0.866}{4} \approx 0.916 \\
\bar{S} &= \dfrac{\sin 330^\circ + \sin 345^\circ + \sin 15^\circ + \sin 30^\circ}{4} = \dfrac{-0.5 - 0.259 + 0.259 + 0.5}{4} = 0
\end{align}
$$

Por tanto, $R \approx 0.916$ y $\bar{\theta} = 0^\circ$: la hora media de llegada es la medianoche, y la longitud resultante, cercana a $1$, indica que las llegadas están muy concentradas alrededor de esa hora.

---

## 11. Ejercicios propuestos

### Ejercicio 11.1

Demostrar que la mediana es equivariante ante transformaciones afines: si $y_i = a x_i + b$ con $a \neq 0$, entonces $Me(\mathbf{y}) = a\, Me(\mathbf{x}) + b$. (Pista: distinguir los casos $a > 0$ y $a < 0$, y examinar cómo cambia el orden de los datos.)

### Ejercicio 11.2

Demostrar que la media ponderada con pesos no negativos $w_i \geq 0$ y $\sum_i w_i > 0$ cumple $x_{(1)} \leq \bar{x}_w \leq x_{(n)}$, y determinar cuándo se alcanza cada igualdad.

### Ejercicio 11.3

Con los salarios del Ejemplo 2.1, calcular la media recortada al $20\%$ y compararla con la media y con la mediana. Explicar por qué se encuentra entre ellas.

### Ejercicio 11.4

Con la tabla de las $50$ mediciones agrupadas de la Clase 3 (Ejemplo 3.4), calcular el percentil $90$ con la Definición 3.5 y compararlo con el valor $2.369$ obtenido con los datos originales (Ejemplo 3.4). Explicar el origen de la diferencia.

### Ejercicio 11.5

Con los salarios del Ejemplo 2.1, verificar la desigualdad de Chebyshev para $k = 1.5$: calcular la cota que garantiza el Teorema 4.1, contar cuántos datos se encuentran a menos de $1.5\,S$ de la media y comparar ambas cantidades.

### Ejercicio 11.6

Calcular $g_1$, $g_2$, $G_1$ y $G_2$ para los datos $2,\ 4,\ 4,\ 4,\ 5,\ 5,\ 7,\ 9$ y verificar la cota $\beta_2 \geq 1 + g_1^2$.

### Ejercicio 11.7

Demostrar que, para dos datos $0 \leq a \leq b$ con $a + b > 0$, el índice de Gini es $I_G = \dfrac{b - a}{2(a + b)}$. Deducir su valor máximo y los casos en que se alcanza.

### Ejercicio 11.8

Para los datos $2$ y $8$, calcular el índice de Gini, el índice de Theil y el índice de Atkinson con $\varepsilon = 1$, y verificar que $\text{Th} = \ln 2 - H$, con $H$ la entropía de las participaciones.

### Ejercicio 11.9 (Opcional)

Para los datos complejos $z = (0,\ 1 + i,\ 2 + 2i,\ 3 + 3i)$, calcular $\bar{z}$, $S_z^2$, $\tau$ y el cociente $|\tau|/S_z^2$, y determinar la dirección de mayor varianza. Explicar el resultado mediante la Proposición 8.3.

### Ejercicio 11.10 (Opcional)

Calcular la media circular, la longitud resultante $R$ y la varianza circular de los ángulos $30^\circ$ y $330^\circ$. Explicar por qué la media aritmética de estos ángulos, $180^\circ$, no es una medida razonable de su posición.

### Ejercicio 11.11

Los tiempos de espera, en minutos, en una ventanilla son:

$$
4,\ 5,\ 5,\ 6,\ 7,\ 7,\ 7,\ 8,\ 9,\ 10,\ 12,\ 25
$$

a) Calcular la media, la mediana, la moda y la media recortada al $10\%$.
b) Calcular la desviación estándar y el coeficiente de variación.
c) Calcular $Q_1$ y $Q_3$ (Tipo 7), el RIC y las barreras de Tukey, y clasificar cada dato.
d) Calcular $g_1$ y el coeficiente de Bowley, y comparar ambos.
e) Decidir qué medidas de centro, dispersión y asimetría conviene informar, y justificar la elección.

### Ejercicio 11.12

Explicar, usando la Proposición 6.4, por qué un exceso de curtosis alto no implica que la distribución sea "puntiaguda". Construir un conjunto de datos, de cualquier tamaño, con exceso de curtosis positivo y cuyo histograma sea plano en su parte central, y calcular su exceso de curtosis.

### Ejercicio 11.13

Construir un conjunto de cinco datos con $g_1 > 0$ y media menor que la mediana, distinto del Ejemplo 6.5, y verificar los cálculos. Explicar qué indica este resultado sobre la regla "con asimetría positiva, la media es mayor que la mediana".

---

**Fin de la Clase 5: Estadísticos Descriptivos**
