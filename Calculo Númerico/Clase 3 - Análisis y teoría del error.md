La teoría del error es el análisis de los errores causados por las mediciones, podemos definir Error como **la diferencia entre el valor medido y el "valor verdadero"**. 
En la naturaleza obtener el valor verdadero al realizar una medición es prácticamente imposible, todos los aparatos de medición tienen un resolución que nos informa sobre el nivel de precisión que podemos tener al momento de medir.
Ejemplo, si medimos el tamaño de una hoja de papel con una regla podemos obtener 15.41cm pero con otra regla podemos obtener 15.37cm y con una tercera regla podemos tener 15.43cm, entonces ¿Cuál es el valor real?. 
Pese a que el concepto de teoría del error es algo aplicado mas a las mediciones experimentales y de laboratorio, sus herramientas y conceptos también aplicaran en las solución de métodos numéricos

error de medición
error sistemático

Precisión vs Exactitud




Cálculos analíticos
$\frac{10}{2}=5$
$x^2-6x+8=0$
$x=\frac{6 \pm \sqrt{(-6)^2-4\cdot 8} }{2}=\frac{6 \pm \sqrt{36-32}}{2}=\frac{6 \pm \sqrt{4}}{2}=\frac{6 \pm 2}{2}$
$x=4 \wedge x=2$






## Notación Científica
 


## Aritmética computacional
En 1985, el Instituto para Ingenieros Eléctricos y Electrónicos (IEEE; Institute for Electrical and electronic Engineers) publicó un reporte llamado Binary Point Arithmetic Stander 754-1985 (Estándar para la aritmética binaria de punto flotante). En 2008 se publicó una versión actualizada con el nombre de _IEEE 754-2008_; la cual proporciona estándares para n+umeros de punto flotante decimales y binarios, formatos para intercambio de datos, algoritmos para redondear operaciones aritméticas y manejo de excepciones.
Los números de punto flotante siguen el siguiente estándar. Una representación de 64 bits (dígito binario) se usa para un número real. El primer bit es un indicador de signo, denominado **s**. A éste le sigue un exponente de 11 bits, **c**, llamado **característica**, y una fracción binaria de 52 bits, **f**, llamada **mantisa**. La base para el exponente es 2.



la mantisa como posee 52 bits su máximo será $2^{52}-1=4,503,599,627,370,495$ por lo que tenemos 16 dígitos de precisión
El exponente tiene 11 bits así que nos da un rango de $2^{52}-1=2047$. Sin embargo, usar sólo enteros positivos para el exponente no permitiría una representación adecuada de los números con magnitud pequeña. Para garantizar que estos números son igualmente representables tomaremos el rango $(-1023,1024)$ 
Para ahorrar almacenamiento y proporcionar una representación única para cada número de punto flotante, se impone una normalización. Por medio de este sistema obtenemos un número de punto flotante de la forma:
$$(-1)^{s} \cdot 2^{c-1023} \cdot (1+f)$$

Considere el número de máquina
0  10000000011  1011100100010000000000000000000000000000000000000000
El bit mas a la izquierda es $S=0$, lo cual significa que es un número positivo
Los siguientes 11 bits $(10000000011)_{2} = (1027)_{10}$, proveen la característica
La parte exponencial del número es, por lo tanto $2^{1027-1023}=2^{4}$
Los 52 bits finales especifican que la mantisa es 
$f = (0.101110010001)_{2} \longrightarrow (1+f) = (1.101110010001)_{2}$
$$f =1 \cdot \frac{1}{2}^{1} + 0 \cdot \frac{1}{2}^{2} + 1 \cdot \frac{1}{2}^{3} + 1 \cdot \frac{1}{2}^{4} + 1 \cdot \frac{1}{2}^{5} + 0 \cdot \frac{1}{2}^{6} + 0 \cdot \frac{1}{2}^{7} + 1 \cdot \frac{1}{2}^{8} + 0 \cdot \frac{1}{2}^{9} + 0 \cdot \frac{1}{2}^{10} + 0 \cdot \frac{1}{2}^{11} + 1 \cdot \frac{1}{2}^{12}$$ 
$$f =1 \cdot \frac{1}{2}^{1} + 1 \cdot \frac{1}{2}^{3} + 1 \cdot \frac{1}{2}^{4} + 1 \cdot \frac{1}{2}^{5} + 1 \cdot \frac{1}{2}^{8}+ 1 \cdot \frac{1}{2}^{12}$$
Como consecuencia, este número de máquina representa precisamente el número decimal
$$(-1)^{s} \cdot 2^{c} \cdot (1+f)=(-1)^{0} \cdot 2^{1027-1023} \cdot [1+(\frac{1}{2}^{}+\frac{1}{8}+\frac{1}{16}+\frac{1}{32}+\frac{1}{256}+\frac{1}{4096})]=27.56640625$$

## Propagación del error



$100 \cdot \sqrt{2} \cdot \sqrt{3} = 100 \cdot 1.41 \cdot 1.73 =243.93$ (aproximando con 2 decimales)
$100 \cdot \sqrt{2} \cdot \sqrt{3} = 244.98$ (por calculadora)

$\sqrt{2} = 1.14 \pm 0.005$
$\sqrt{3} = 1.73 \pm 0.005$
$100 \cdot \sqrt{2} \cdot \sqrt{3} = 100 \cdot (\sqrt{2} \pm 0.005) \cdot (\sqrt{3} \pm 0.005)$ 


# Análisis y Teoría del Error

## 1. Introducción a la teoría del error

### 1.1 Concepto fundamental

**Definición 1.1 (Teoría del error):**
La **teoría del error** es el análisis matemático de los errores causados por las mediciones, aproximaciones y representaciones numéricas en el cálculo científico y computacional.

**Motivación:**
En la práctica científica y computacional, enfrentamos dos realidades fundamentales:
1. En la naturaleza, obtener el **valor verdadero** de una medición es prácticamente imposible
2. Las computadoras tienen **limitaciones de precisión** en la representación de números

**Contexto histórico:**
La teoría del error se originó en astronomía y geodesia en los siglos XVIII y XIX, con contribuciones de Carl Friedrich Gauss, Pierre-Simon Laplace y Adrien-Marie Legendre. Con el advenimiento de las computadoras digitales, esta teoría se expandió al análisis numérico moderno.

### 1.2 Importancia en métodos numéricos

**Áreas de aplicación:**
- Mediciones experimentales y de laboratorio
- Cálculos científicos y de ingeniería
- Simulaciones numéricas
- Procesamiento de señales
- Computación científica
- Optimización numérica

**Observación:** Aunque el concepto de teoría del error se asocia tradicionalmente con mediciones experimentales, sus herramientas y conceptos son fundamentales para la solución de métodos numéricos.

---

## 2. Tipos de errores

### 2.1 Error absoluto y error relativo

**Definición 2.1 (Valor verdadero y valor aproximado):**
- $x$: **valor verdadero** (valor exacto que buscamos)
- $\tilde{x}$: **valor aproximado** (valor medido o calculado)

**Definición 2.2 (Error absoluto):**
El **error absoluto** es la diferencia entre el valor verdadero y el valor aproximado:
$$E_a = |x - \tilde{x}|$$

**Definición 2.3 (Error relativo):**
El **error relativo** es la razón entre el error absoluto y el valor verdadero:
$$E_r = \frac{|x - \tilde{x}|}{|x|}, \quad x \neq 0$$

**Error relativo porcentual:**
$$E_r\% = \frac{|x - \tilde{x}|}{|x|} \times 100\%$$

**Ejemplo 2.1:**
Si medimos la longitud de una hoja de papel:
- Valor verdadero (supuesto): $x = 15.40$ cm
- Valor medido: $\tilde{x} = 15.37$ cm

**Error absoluto:**
$$E_a = |15.40 - 15.37| = 0.03 \text{ cm}$$

**Error relativo:**
$$E_r = \frac{0.03}{15.40} \approx 0.001948 \approx 0.19\%$$

**Ejemplo 2.2 (Importancia del error relativo):**

**Caso 1:**
- Medición de distancia entre ciudades: $x = 100$ km, $\tilde{x} = 100.03$ km
- $E_a = 0.03$ km (30 metros)
- $E_r = 0.03\%$

**Caso 2:**
- Medición de un transistor: $x = 1$ mm, $\tilde{x} = 1.03$ mm
- $E_a = 0.03$ mm
- $E_r = 3\%$

**Conclusión:** Aunque el error absoluto es el mismo, el error relativo revela que la segunda medición es mucho menos precisa.

### 2.2 Error de medición

**Definición 2.4 (Error de medición):**
El **error de medición** es la incertidumbre asociada con la limitación física de los instrumentos de medición.

**Características:**
1. **Resolución del instrumento:** Mínima división de escala
2. **Incertidumbre instrumental:** Típicamente $\pm$ la mitad de la división más pequeña
3. **Condiciones ambientales:** Temperatura, presión, humedad
4. **Error humano:** Lectura e interpretación

**Ejemplo 2.3:**
Medimos el tamaño de una hoja con tres reglas diferentes:
- Regla 1: $15.41$ cm
- Regla 2: $15.37$ cm
- Regla 3: $15.43$ cm

**Pregunta:** ¿Cuál es el valor real?

**Análisis estadístico:**
- **Media:** $\bar{x} = \frac{15.41 + 15.37 + 15.43}{3} = 15.40$ cm
- **Desviación estándar:** $s = \sqrt{\frac{\sum(x_i - \bar{x})^2}{n-1}} \approx 0.03$ cm
- **Valor reportado:** $x = 15.40 \pm 0.03$ cm

### 2.3 Errores sistemáticos y aleatorios

**Definición 2.5 (Error sistemático):**
Un **error sistemático** es un error que se repite consistentemente en la misma dirección debido a:
- Calibración incorrecta del instrumento
- Condiciones experimentales sesgadas
- Método defectuoso
- Limitaciones del modelo matemático

**Características:**
- Predecible y reproducible
- Puede ser corregido si se identifica
- Afecta la **exactitud**

**Ejemplo 2.4:**
Una balanza descalibrada que siempre suma 5 gramos produce un error sistemático de $+5$ g.

**Definición 2.6 (Error aleatorio):**
Un **error aleatorio** es una fluctuación impredecible causada por:
- Variaciones ambientales
- Limitaciones en la lectura
- Ruido en la medición

**Características:**
- Impredecible e irregular
- Se distribuye aleatoriamente alrededor del valor verdadero
- Afecta la **precisión**
- Se puede reducir mediante promedios

**Ejemplo 2.5:**
Variaciones en la temperatura ambiente que afectan ligeramente cada medición de manera diferente.

### 2.4 Precisión vs Exactitud

**Definición 2.7 (Exactitud - Accuracy):**
La **exactitud** es la cercanía de un valor medido al valor verdadero. Mide qué tan correcto es el resultado.

**Definición 2.8 (Precisión - Precision):**
La **precisión** es la cercanía entre múltiples mediciones del mismo valor. Mide la reproducibilidad.

**Representación gráfica:**

```
  ALTA EXACTITUD         BAJA EXACTITUD
  ALTA PRECISIÓN         ALTA PRECISIÓN
       •••                    •••
       •○•                     •••
       •••                      •
  (agrupado en             (agrupado lejos
   el centro)               del centro)

  ALTA EXACTITUD         BAJA EXACTITUD
  BAJA PRECISIÓN         BAJA PRECISIÓN
    • • •                  •   •
      •○•                    •  ○
    •   •                •     •
  (disperso cerca        (disperso lejos
   del centro)            del centro)

  ○ = valor verdadero
  • = mediciones
```

**Ejemplo 2.6:**
Un tirador realiza 5 disparos:

**Caso A (Alta precisión, alta exactitud):**
Todos los disparos están agrupados en el centro → **IDEAL**

**Caso B (Alta precisión, baja exactitud):**
Todos los disparos están agrupados pero lejos del centro → Error sistemático

**Caso C (Baja precisión, alta exactitud):**
Los disparos están dispersos pero centrados alrededor del objetivo → Errores aleatorios

**Caso D (Baja precisión, baja exactitud):**
Los disparos están dispersos y lejos del centro → **PEOR CASO**

**Relación con errores:**
- **Exactitud** está afectada por **errores sistemáticos**
- **Precisión** está afectada por **errores aleatorios**

---

## 3. Cálculos analíticos vs numéricos

### 3.1 Soluciones analíticas exactas

**Definición 3.1 (Solución analítica):**
Una **solución analítica** (o exacta) es una expresión matemática cerrada que proporciona el valor exacto sin aproximaciones.

**Ejemplo 3.1 (Operaciones aritméticas exactas):**
$$\frac{10}{2} = 5$$

El resultado es **exacto**, sin error.

**Ejemplo 3.2 (Ecuación cuadrática):**
Resolver $x^2 - 6x + 8 = 0$:

$$\begin{align}
x &= \frac{6 \pm \sqrt{(-6)^2 - 4 \cdot 1 \cdot 8}}{2 \cdot 1} \\
&= \frac{6 \pm \sqrt{36 - 32}}{2} \\
&= \frac{6 \pm \sqrt{4}}{2} \\
&= \frac{6 \pm 2}{2}
\end{align}$$

**Soluciones exactas:**
$$x_1 = \frac{6 + 2}{2} = 4, \quad x_2 = \frac{6 - 2}{2} = 2$$

### 3.2 Limitaciones de las soluciones analíticas

**Problemas sin solución analítica:**
1. Ecuaciones trascendentales: $e^x = x^2$
2. Integrales no elementales: $\int e^{-x^2} dx$
3. Sistemas no lineales complejos
4. Ecuaciones diferenciales no lineales

**Necesidad de métodos numéricos:**
Cuando no existe solución analítica o es impráctica de obtener, recurrimos a métodos numéricos que proporcionan **aproximaciones**.

**Ejemplo 3.3:**
La ecuación $\cos(x) = x$ no tiene solución analítica. Un método numérico (como Newton-Raphson) proporciona:
$$x \approx 0.739085133215$$

---

## 4. Notación científica

### 4.1 Definición y formato

**Definición 4.1 (Notación científica):**
La **notación científica** (o notación exponencial) expresa un número en la forma:
$$x = \pm m \times 10^e$$

donde:
- $m$ es la **mantisa** (o significando): $1 \leq |m| < 10$
- $e$ es el **exponente** (un entero)
- $\pm$ es el signo

**Formato normalizado:**
$$x = \pm d_0.d_1d_2d_3\ldots d_n \times 10^e$$

donde $d_0 \neq 0$ (excepto para el número cero).

### 4.2 Ventajas de la notación científica

**Ventajas:**
1. **Compacidad:** Representa números muy grandes o muy pequeños
2. **Claridad:** Muestra explícitamente la magnitud
3. **Precisión:** Indica claramente los dígitos significativos
4. **Operaciones:** Facilita multiplicación y división

**Ejemplo 4.1 (Números muy grandes):**
- Velocidad de la luz: $299,792,458$ m/s = $2.99792458 \times 10^8$ m/s
- Número de Avogadro: $6.022 \times 10^{23}$ moléculas/mol
- Distancia Tierra-Sol: $1.496 \times 10^{11}$ m

**Ejemplo 4.2 (Números muy pequeños):**
- Masa del electrón: $9.109 \times 10^{-31}$ kg
- Carga del electrón: $1.602 \times 10^{-19}$ C
- Constante de Planck: $6.626 \times 10^{-34}$ J·s

### 4.3 Operaciones en notación científica

**Multiplicación:**
$$(m_1 \times 10^{e_1}) \times (m_2 \times 10^{e_2}) = (m_1 \times m_2) \times 10^{e_1 + e_2}$$

**División:**
$$\frac{m_1 \times 10^{e_1}}{m_2 \times 10^{e_2}} = \frac{m_1}{m_2} \times 10^{e_1 - e_2}$$

**Ejemplo 4.3:**
$$(3.0 \times 10^8) \times (2.0 \times 10^{-3}) = (3.0 \times 2.0) \times 10^{8 + (-3)} = 6.0 \times 10^5$$

**Ejemplo 4.4:**
$$\frac{6.0 \times 10^{12}}{2.0 \times 10^4} = \frac{6.0}{2.0} \times 10^{12 - 4} = 3.0 \times 10^8$$

### 4.4 Dígitos significativos

**Definición 4.2 (Dígitos significativos):**
Los **dígitos significativos** de un número son todos los dígitos que aportan información sobre su precisión, excluyendo ceros que solo indican la posición del punto decimal.

**Reglas:**
1. Todos los dígitos no ceros son significativos
2. Ceros entre dígitos no ceros son significativos
3. Ceros a la izquierda NO son significativos
4. Ceros a la derecha SÍ son significativos si hay punto decimal

**Ejemplo 4.5:**
- $123.45$ → 5 dígitos significativos
- $0.00456$ → 3 dígitos significativos (los ceros iniciales no cuentan)
- $1.2300$ → 5 dígitos significativos (los ceros finales cuentan)
- $1200$ → ambiguo (2, 3 o 4 dígitos significativos)
- $1.200 \times 10^3$ → claramente 4 dígitos significativos

**Observación:** La notación científica elimina la ambigüedad sobre dígitos significativos.

---

## 5. Aritmética computacional

### 5.1 Representación de números en computadoras

**Contexto histórico:**
En 1985, el **Instituto de Ingenieros Eléctricos y Electrónicos (IEEE)** publicó el estándar **IEEE 754-1985** para aritmética binaria de punto flotante. En 2008 se publicó una versión actualizada: **IEEE 754-2008**, que proporciona:
- Estándares para números de punto flotante (decimales y binarios)
- Formatos para intercambio de datos
- Algoritmos para redondeo de operaciones aritméticas
- Manejo de excepciones (overflow, underflow, NaN, infinito)

**Importancia:** Este estándar es usado por prácticamente todas las computadoras modernas.

### 5.2 Formato de punto flotante de doble precisión (64 bits)

**Definición 5.1 (Número de punto flotante IEEE 754):**
Un número real se representa usando **64 bits** (8 bytes) divididos en tres campos:

![[Representacion de punto flotante.png]]

**Componentes:**

1. **S (Signo):** 1 bit
   - $S = 0$: número positivo
   - $S = 1$: número negativo

2. **C (Característica o exponente sesgado):** 11 bits
   - Rango: $0$ a $2^{11} - 1 = 2047$
   - Valores especiales: $0$ y $2047$ reservados
   - Exponente real: $e = C - 1023$ (sesgo de 1023)
   - Rango del exponente: $-1023$ a $+1024$

3. **F (Fracción o mantisa):** 52 bits
   - Representa la parte fraccionaria
   - Bit implícito: siempre hay un "1" antes del punto binario (normalización)
   - Mantisa completa: $1.f = 1 + F$

**Fórmula de representación:**
$$x = (-1)^S \times 2^{C - 1023} \times (1 + F)$$

donde:
$$F = \sum_{i=1}^{52} b_i \times 2^{-i}$$

y $b_i \in \{0, 1\}$ son los bits de la fracción.

### 5.3 Precisión y rango

**Proposición 5.1 (Precisión):**
La mantisa de 52 bits proporciona:
- Máximo valor de la fracción: $2^{52} - 1 = 4,503,599,627,370,495$
- Aproximadamente **16 dígitos decimales de precisión**

**Demostración:**
$$\log_{10}(2^{52}) \approx 52 \times 0.30103 \approx 15.65 \text{ dígitos decimales}$$

**Proposición 5.2 (Rango):**
El exponente de 11 bits proporciona:
- Rango del exponente: $-1023$ a $+1024$
- Número más pequeño (normalizado): $\approx 2.23 \times 10^{-308}$
- Número más grande: $\approx 1.80 \times 10^{308}$

**Valores especiales:**

| Caso | S | C | F | Significado |
|------|---|---|---|-------------|
| Cero | 0/1 | 0 | 0 | $+0$ o $-0$ |
| Infinito | 0/1 | 2047 | 0 | $+\infty$ o $-\infty$ |
| NaN | 0/1 | 2047 | ≠0 | Not a Number |
| Subnormal | 0/1 | 0 | ≠0 | $(-1)^S \times 2^{-1022} \times (0 + F)$ |

### 5.4 Ejemplo detallado

**Ejemplo 5.1:**
Considere el número de máquina representado en 64 bits:

```
0  10000000011  1011100100010000000000000000000000000000000000000000
```

**Análisis paso a paso:**

**1. Signo (S):**
$$S = 0 \Rightarrow \text{número positivo}$$

**2. Característica (C):**
$$(10000000011)_2 = 1 \times 2^{10} + 0 \times 2^9 + \cdots + 1 \times 2^1 + 1 \times 2^0 = 1024 + 2 + 1 = 1027$$

**Exponente:**
$$e = C - 1023 = 1027 - 1023 = 4$$
$$2^e = 2^4 = 16$$

**3. Mantisa (F):**
Bits de la fracción: $(1011100100010)_2$ (primeros 12 bits no ceros, resto ceros)

$$\begin{align}
F &= 1 \times 2^{-1} + 0 \times 2^{-2} + 1 \times 2^{-3} + 1 \times 2^{-4} + 1 \times 2^{-5} \\
  &\quad + 0 \times 2^{-6} + 0 \times 2^{-7} + 1 \times 2^{-8} + 0 \times 2^{-9} \\
  &\quad + 0 \times 2^{-10} + 0 \times 2^{-11} + 1 \times 2^{-12} \\
  &= \frac{1}{2} + \frac{1}{8} + \frac{1}{16} + \frac{1}{32} + \frac{1}{256} + \frac{1}{4096} \\
  &= 0.5 + 0.125 + 0.0625 + 0.03125 + 0.00390625 + 0.000244140625 \\
  &= 0.72290039063
\end{align}$$

**Mantisa completa:**
$$1 + F = 1.72290039063$$

**4. Valor decimal:**
$$\begin{align}
x &= (-1)^0 \times 2^4 \times 1.72290039063 \\
  &= 1 \times 16 \times 1.72290039063 \\
  &= 27.56640625
\end{align}$$

**Resultado:** El número de máquina representa exactamente $27.56640625$.

### 5.5 Errores de redondeo y truncamiento

**Definición 5.2 (Error de redondeo):**
El **error de redondeo** ocurre cuando un número real no puede representarse exactamente con un número finito de bits y debe aproximarse al número de punto flotante más cercano.

**Ejemplo 5.2:**
El número $0.1$ (decimal) no tiene representación exacta en binario:
$$(0.1)_{10} = (0.0001100110011001100110011\ldots)_2 \text{ (periódico)}$$

La computadora lo trunca o redondea, causando un error.

**Demostración numérica:**
```python
>>> 0.1 + 0.1 + 0.1 == 0.3
False
>>> 0.1 + 0.1 + 0.1
0.30000000000000004
```

**Definición 5.3 (Epsilon de máquina):**
El **epsilon de máquina** ($\epsilon_m$) es el número positivo más pequeño tal que:
$$1 + \epsilon_m \neq 1$$

en aritmética de punto flotante.

Para IEEE 754 doble precisión:
$$\epsilon_m = 2^{-52} \approx 2.22 \times 10^{-16}$$

**Implicación:** No podemos distinguir números que difieren en menos de $\epsilon_m$ del número base.

---

## 6. Propagación del error

### 6.1 Concepto de propagación

**Definición 6.1 (Propagación del error):**
La **propagación del error** es el proceso por el cual los errores en las variables de entrada se transmiten y amplifican en el resultado de una operación o función.

**Observación crítica:** En cálculos numéricos largos, los errores pequeños pueden acumularse y producir resultados significativamente inexactos.

### 6.2 Propagación en operaciones aritméticas

**Teorema 6.1 (Propagación en suma y resta):**
Si $x = a \pm b$ donde $a$ y $b$ tienen errores $\delta a$ y $\delta b$:

**Error absoluto:**
$$\delta x \approx |\delta a| + |\delta b|$$

**Interpretación:** Los errores absolutos se **suman** en adición y sustracción.

**Teorema 6.2 (Propagación en multiplicación y división):**
Si $x = a \times b$ o $x = a / b$ donde $a$ y $b$ tienen errores relativos $\epsilon_a$ y $\epsilon_b$:

**Error relativo:**
$$\epsilon_x \approx |\epsilon_a| + |\epsilon_b|$$

**Interpretación:** Los errores relativos se **suman** en multiplicación y división.

### 6.3 Ejemplo de propagación de error

**Ejemplo 6.1:**
Calcular $100 \times \sqrt{2} \times \sqrt{3}$ usando aproximaciones con 2 decimales.

**Valores aproximados:**
$$\sqrt{2} \approx 1.41 \pm 0.005 \quad \text{(precisión de 2 decimales)}$$
$$\sqrt{3} \approx 1.73 \pm 0.005$$

**Método 1 (Con aproximaciones):**
$$100 \times 1.41 \times 1.73 = 243.93$$

**Método 2 (Calculadora con mayor precisión):**
$$100 \times \sqrt{2} \times \sqrt{3} = 100 \times \sqrt{6} \approx 244.9489742783$$

**Error:**
$$E_a = |244.9489742783 - 243.93| = 1.0190 \text{ (aproximadamente)}$$

$$E_r = \frac{1.0190}{244.9489742783} \approx 0.416\%$$

**Análisis de propagación:**

Si escribimos:
$$\sqrt{2} = 1.41 \pm 0.005, \quad \sqrt{3} = 1.73 \pm 0.005$$

El producto puede estar en el rango:
$$\begin{align}
\text{Mínimo:} &\quad 100 \times (1.41 - 0.005) \times (1.73 - 0.005) = 242.762 \\
\text{Máximo:} &\quad 100 \times (1.41 + 0.005) \times (1.73 + 0.005) = 245.105
\end{align}$$

**Incertidumbre propagada:**
$$100 \times \sqrt{2} \times \sqrt{3} = 243.93 \pm 1.17$$

### 6.4 Fórmulas generales de propagación

**Teorema 6.3 (Propagación general):**
Para una función $f(x_1, x_2, \ldots, x_n)$ con errores $\delta x_i$ en las variables:

**Error absoluto (aproximación lineal):**
$$\delta f \approx \sum_{i=1}^{n} \left| \frac{\partial f}{\partial x_i} \right| \delta x_i$$

**Error relativo:**
$$\epsilon_f \approx \sum_{i=1}^{n} \left| \frac{\partial \ln f}{\partial \ln x_i} \right| \epsilon_{x_i}$$

**Ejemplo 6.2:**
Para $f(x, y) = x^2 y$:

$$\frac{\partial f}{\partial x} = 2xy, \quad \frac{\partial f}{\partial y} = x^2$$

$$\delta f \approx |2xy| \delta x + |x^2| \delta y$$

**Ejemplo 6.3:**
Para $f(x) = x^n$:

$$\epsilon_f \approx n \epsilon_x$$

**Conclusión:** Las potencias **amplifican** el error relativo por un factor de $n$.

### 6.5 Cancelación catastrófica

**Definición 6.2 (Cancelación catastrófica):**
La **cancelación catastrófica** (o pérdida de significancia) ocurre cuando se restan dos números casi iguales, causando una pérdida significativa de dígitos significativos.

**Ejemplo 6.4:**
Calcular $x - y$ donde:
$$x = 1.234567, \quad y = 1.234560$$

Resultado: $x - y = 0.000007$

**Problema:** Si ambos números tienen error en el 6to decimal, el resultado tiene error del 100%.

**Ejemplo 6.5 (Fórmula cuadrática):**
Para resolver $ax^2 + bx + c = 0$, la fórmula:
$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

puede sufrir cancelación cuando $b^2 \gg 4ac$ y usamos el signo que hace que el numerador sea la resta de números casi iguales.

**Solución alternativa:**
$$x_1 = \frac{-b - \text{sgn}(b)\sqrt{b^2 - 4ac}}{2a}, \quad x_2 = \frac{c}{ax_1}$$

---

## 7. Tipos de errores en métodos numéricos

### 7.1 Clasificación de errores

**1. Error de modelado:**
- Simplificaciones en el modelo matemático
- Suposiciones sobre el sistema físico

**2. Error de datos:**
- Incertidumbre en los parámetros de entrada
- Errores de medición

**3. Error de truncamiento:**
- Aproximación de procesos infinitos con procesos finitos
- Series de Taylor truncadas
- Número finito de iteraciones

**4. Error de redondeo:**
- Limitaciones de la aritmética de punto flotante
- Acumulación en cálculos largos

### 7.2 Error de truncamiento

**Definición 7.1 (Error de truncamiento):**
El **error de truncamiento** es el error introducido al aproximar un proceso matemático infinito con uno finito.

**Ejemplo 7.1 (Serie de Taylor):**
$$e^x = 1 + x + \frac{x^2}{2!} + \frac{x^3}{3!} + \cdots$$

Si truncamos después de $n$ términos:
$$e^x \approx \sum_{k=0}^{n} \frac{x^k}{k!}$$

**Error de truncamiento:**
$$E_T = e^x - \sum_{k=0}^{n} \frac{x^k}{k!} = \sum_{k=n+1}^{\infty} \frac{x^k}{k!}$$

**Ejemplo 7.2 (Diferencias finitas):**
La derivada $f'(x)$ puede aproximarse:
$$f'(x) \approx \frac{f(x+h) - f(x)}{h}$$

**Error de truncamiento:** $O(h)$ (orden de $h$)

### 7.3 Orden de convergencia

**Definición 7.2 (Orden de convergencia):**
Decimos que una aproximación tiene **orden** $p$ si:
$$E(h) = O(h^p)$$

es decir, existe una constante $C$ tal que:
$$|E(h)| \leq C h^p$$

para $h$ suficientemente pequeño.

**Interpretación:**
- Mayor $p$ → convergencia más rápida
- Si $p = 1$: convergencia lineal
- Si $p = 2$: convergencia cuadrática

---

## 8. Estrategias para minimizar errores

### 8.1 Buenas prácticas

**1. Evitar cancelación catastrófica:**
- Reformular expresiones algebraicamente
- Usar identidades trigonométricas

**2. Ordenar operaciones:**
- Sumar números del más pequeño al más grande
- Evitar sumar cantidades de magnitudes muy diferentes

**3. Usar mayor precisión:**
- Cálculos intermedios con doble precisión
- Acumuladores de alta precisión

**4. Algoritmos estables:**
- Preferir métodos numéricamente estables
- Evitar divisiones por números muy pequeños

**5. Análisis de sensibilidad:**
- Estudiar cómo los errores de entrada afectan la salida
- Calcular números de condición

### 8.2 Condicionamiento

**Definición 8.1 (Número de condición):**
El **número de condición** de un problema mide su sensibilidad a perturbaciones en los datos de entrada.

Para una función $f$:
$$\kappa = \left| \frac{x f'(x)}{f(x)} \right|$$

**Interpretación:**
- $\kappa \approx 1$: problema **bien condicionado**
- $\kappa \gg 1$: problema **mal condicionado**

**Ejemplo 8.1:**
Para $f(x) = x^n$:
$$\kappa = n$$

Las potencias altas están mal condicionadas.

---

## 9. Resumen de conceptos clave

**Tipos de errores:**
- **Error absoluto:** $E_a = |x - \tilde{x}|$
- **Error relativo:** $E_r = \frac{|x - \tilde{x}|}{|x|}$

**Características:**
- **Precisión:** Reproducibilidad de mediciones
- **Exactitud:** Cercanía al valor verdadero

**Representación computacional:**
- **IEEE 754:** $(-1)^S \times 2^{C-1023} \times (1+F)$
- **Precisión:** ~16 dígitos decimales (doble precisión)
- **Epsilon de máquina:** $2^{-52} \approx 2.22 \times 10^{-16}$

**Propagación:**
- Suma/resta: errores absolutos se suman
- Multiplicación/división: errores relativos se suman
- Cancelación catastrófica: restar números similares

---

## 10. Ejercicios propuestos

### 10.1 Errores básicos

1. Calcule el error absoluto y relativo si el valor verdadero es $\pi = 3.141592654$ y la aproximación es $3.14$

2. Una medición de 1000 kg tiene un error de 1 kg. Otra de 10 kg tiene un error de 0.5 kg. ¿Cuál es más precisa en términos relativos?

3. Explique la diferencia entre precisión y exactitud usando un ejemplo concreto

### 10.2 Notación científica

4. Exprese en notación científica:
   a) $0.000000456$
   b) $123,000,000,000$
   c) Masa del protón: $0.000000000000000000000000001673$ kg

5. Calcule $(3.2 \times 10^{-5}) \times (2.5 \times 10^{8})$

6. ¿Cuántos dígitos significativos tiene $0.00304$?

### 10.3 Punto flotante

7. Convierta $(1.25)_{10}$ a representación IEEE 754 de 64 bits

8. ¿Cuál es el número decimal representado por:
   ```
   0  01111111110  1000000000000000000000000000000000000000000000000000
   ```

9. Explique por qué $0.1 + 0.2 \neq 0.3$ en aritmética de punto flotante

### 10.4 Propagación de errores

10. Si $x = 10.0 \pm 0.1$ y $y = 5.0 \pm 0.1$, encuentre el rango de valores para:
    a) $x + y$
    b) $x - y$
    c) $x \times y$
    d) $x / y$

11. Calcule $\sqrt{4.01} - \sqrt{4.00}$ de dos formas:
    a) Directamente
    b) Racionalizando
    ¿Cuál método es mejor numéricamente?

12. Para $f(x,y) = xy^2$, si $x = 2 \pm 0.01$ y $y = 3 \pm 0.02$, estime el error en $f$

### 10.5 Análisis de errores

13. Demuestre que el error relativo en $x^n$ es aproximadamente $n$ veces el error relativo en $x$

14. ¿Por qué es problemático calcular $(1 - \cos x)$ para $x$ pequeño? Proponga una alternativa

15. Analice la estabilidad de calcular las raíces de $x^2 - 2px + q = 0$ cuando $p^2 \gg q$

### 10.6 Aplicaciones

16. Un algoritmo calcula $\pi$ con error relativo $10^{-10}$. ¿Cuántos dígitos decimales son confiables?

17. En un experimento, medimos $t = 2.5 \pm 0.1$ s. La distancia es $d = v \times t$ donde $v = 10 \pm 0.2$ m/s. Calcule $d$ con su incertidumbre

18. Explique por qué sumar $1 + 10^{-20}$ mil millones de veces en una computadora puede dar resultado $1$

### 10.7 Problemas avanzados

19. Compare el error de truncamiento al aproximar $\sin(0.1)$ usando:
    a) $\sin(x) \approx x$
    b) $\sin(x) \approx x - \frac{x^3}{6}$

20. Investigue el número de condición de evaluar $f(x) = \frac{1}{1-x}$ cerca de $x = 1$

---

**Fin de la Clase 3**
