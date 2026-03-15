# Representaciones Gráficas en Estadística Descriptiva

## 1. Introducción y fundamentos de la visualización estadística

### 1.1 Motivación

La **visualización estadística** constituye una herramienta fundamental en el análisis exploratorio de datos (EDA). Mientras que las tablas de frecuencias proporcionan un resumen numérico, los **gráficos estadísticos** permiten:

1. **Identificación rápida de patrones**: Tendencias, agrupaciones, outliers
2. **Comunicación efectiva**: Transmitir información compleja de forma intuitiva
3. **Análisis de la forma de distribución**: Simetría, sesgo, multimodalidad
4. **Comparación entre grupos**: Visualizar diferencias y similitudes

**Principio fundamental de Tukey (1977):**
> "El análisis de datos gráfico es superior al numérico en la revelación de la estructura de los datos, particularmente de características inesperadas."

### 1.2 Marco conceptual

**Definición 1.1 (Representación gráfica estadística):**
Una **representación gráfica** de una variable estadística $X$ es una función biyectiva:
$$\varphi: (\text{Datos}, \text{Frecuencias}) \to \mathbb{R}^2$$
que mapea información estadística (clases y sus frecuencias) a coordenadas en el plano cartesiano, satisfaciendo criterios de **proporcionalidad visual** y **legibilidad**.

**Propiedades deseables:**
1. **Proporcionalidad**: El área o altura debe ser proporcional a la frecuencia representada
2. **Claridad**: La interpretación debe ser inmediata y no ambigua
3. **Completitud**: Debe representar toda la información relevante
4. **Honestidad**: No debe distorsionar ni exagerar patrones

---

## 2. Gráfico de barras

### 2.1 Definición y características

**Definición 2.1 (Gráfico de barras):**
Sea $X$ una **variable discreta** (cualitativa o cuantitativa no agrupada) con $k$ clases: $X_1, X_2, ..., X_k$ y frecuencias asociadas $n_1, n_2, ..., n_k$ (o $f_1, f_2, ..., f_k$). Un **gráfico de barras** es una representación gráfica donde:
- Cada clase $X_i$ se representa por una **barra rectangular** de base uniforme $b$
- La **altura** $h_i$ de la barra es proporcional a su frecuencia: $h_i \propto n_i$ (o $h_i \propto f_i$)
- Las barras están **espacialmente separadas** para enfatizar la naturaleza discreta de la variable
![[grafico-barras.png]]
**Especificaciones técnicas:**

| Característica | Requisito | Justificación |
|:---------------|:----------|:--------------|
| **Orientación** | Horizontal o vertical | Ambas son válidas; vertical es más común |
| **Separación** | Las barras **deben** estar separadas | Indica naturaleza discreta de $X$ |
| **Base** | Todas las barras con base uniforme $b$ | Asegura comparabilidad |
| **Altura** | $h_i = c \cdot n_i$ (o $h_i = c \cdot f_i$), con $c>0$ constante | Proporcionalidad visual |
| **Número de barras** | Igual a $k$ (número de clases) | Exhaustividad |
| **Escala del eje** | Debe iniciar en cero | Honestidad en la representación |
### 2.2 Construcción formal

**Algoritmo de construcción:**

1. **Eje horizontal (abscisas)**: Representar las $k$ clases $X_1, ..., X_k$
2. **Eje vertical (ordenadas)**: Escala para frecuencias (absoluta $n_i$ o relativa $f_i$)
3. **Dibujar barras**: Para cada $i \in \{1,...,k\}$:
   - Centrar barra sobre $X_i$
   - Altura $h_i = n_i$ (o $h_i = f_i$)
   - Ancho uniforme $b$ (arbitrario pero constante)
4. **Etiquetado**: Título, etiquetas de ejes, leyenda si aplica
### 2.3 Aplicabilidad

**Criterio de uso:**
El gráfico de barras es apropiado para:
- Variables **cualitativas** (nominales u ordinales)
- Variables **cuantitativas discretas** sin agrupar (cuando $k$ es razonablemente pequeño, típicamente $k \leq 20$)

**Ejemplos de uso adecuado:**
- Frecuencia de tipos de sangre: $\{A^+, A^-, B^+, B^-, AB^+, AB^-, O^+, O^-\}$
- Número de hijos por familia: $\{0, 1, 2, 3, 4, 5+\}$
- Categoría de producto más vendido
- Nivel educativo: $\{\text{Primaria}, \text{Secundaria}, \text{Universitaria}, \text{Posgrado}\}$

### 2.4 Variantes

**a) Gráfico de barras agrupadas:**
Para comparar múltiples variables categóricas simultáneamente.
![[barras-agrupadas.png]]
**b) Gráfico de barras apiladas:**
Muestra composición relativa de subcategorías dentro de cada clase.
![[barras-apiladas.png]]
Es muy útil para desglosar una variable en el porcentaje en sus contribuciones, o en su defecto cuando todos los grupos tienen el mismo total.
![[barras-apiladas-100.png]]

**c) Gráfico de barras horizontales:**
Preferible cuando las etiquetas de clase son largas o cuando se desea enfatizar comparaciones de magnitud.
![[barras-horizontal.png]]

---
## 3. Histograma

### 3.1 Definición y fundamentación

**Definición 3.1 (Histograma):**
Sea $X$ una **variable continua** o discreta con muchos valores agrupada en $k$ intervalos de clase $I_i = [c_i, c_{i+1})$ para $i=1,...,k$, con frecuencias $n_1, ..., n_k$ (o $f_1, ..., f_k$). Un **histograma** es una representación gráfica donde:
- Cada intervalo $I_i$ se representa por un **rectángulo**
- La base del rectángulo es el intervalo $[c_i, c_{i+1}]$ sobre el eje horizontal
- El **área** del rectángulo es proporcional a la frecuencia $n_i$ (o $f_i$)
- Los rectángulos son **adyacentes** (sin separación) para enfatizar la naturaleza continua de $X$

**Altura de las barras:**

Si los intervalos tienen **amplitud constante** $a = c_{i+1} - c_i$, entonces:
$$h_i = \frac{n_i}{a} \quad \text{o} \quad h_i = \frac{f_i}{a}$$

Si los intervalos tienen **amplitud variable** $a_i = c_{i+1} - c_i$, entonces:
$$h_i = \frac{n_i}{a_i} \quad \text{o} \quad h_i = \frac{f_i}{a_i}$$

**Justificación:** El área del rectángulo es $\text{base} \times \text{altura} = a_i \times h_i = a_i \times \frac{n_i}{a_i} = n_i$ (o $f_i$), cumpliendo el principio de proporcionalidad.
![[histograma.png]]
### 3.2 Propiedades matemáticas

**Propiedad 3.1 (Conservación de frecuencias):**
El área total del histograma con frecuencias relativas es:
$$\sum_{i=1}^{k} \text{Área}_i = \sum_{i=1}^{k} a_i \cdot h_i = \sum_{i=1}^{k} a_i \cdot \frac{f_i}{a_i} = \sum_{i=1}^{k} f_i = 1$$
con frecuencias absoluta:
$$\sum_{i=1}^{k} \text{Área}_i = \sum_{i=1}^{k} a_i \cdot h_i = \sum_{i=1}^{k} a_i \cdot \frac{n_i}{a_i} = \sum_{i=1}^{k} n_i = N$$

Esto significa que el histograma de frecuencias relativas puede interpretarse como una **aproximación discreta de una función de densidad de probabilidad**.

**Propiedad 3.2 (Convergencia asintótica):**
Bajo ciertas condiciones de regularidad, cuando $N \to \infty$ y $a \to 0$ (pero $Na \to \infty$), el histograma converge a la **función de densidad verdadera** $f(x)$ de la población:
$$h(x) \xrightarrow{N \to \infty} f(x)$$
Este resultado justifica el uso del histograma como **estimador no paramétrico de la densidad**.
### 3.3 Diferencias clave con el gráfico de barras

| Característica | Gráfico de Barras | Histograma |
|:---------------|:------------------|:-----------|
| **Tipo de variable** | Discreta (cualitativa o cuantitativa) | Continua (o discreta agrupada) |
| **Separación** | Barras separadas | Rectángulos adyacentes |
| **Base de barras** | Uniforme (arbitraria) | Amplitud del intervalo $a_i$ |
| **Interpretación de altura** | Directamente la frecuencia | Densidad de frecuencia $f_i/a_i$ |
| **Interpretación de área** | No relevante | Proporcional a la frecuencia |
| **Objetivo** | Comparar categorías | Mostrar forma de distribución |
### 3.4 Construcción paso a paso

1. **Agrupar datos**: Usar regla de Sturges o $\sqrt{N}$ para determinar $k$
2. **Calcular límites**: Definir $c_1, c_2, ..., c_{k+1}$
3. **Eje horizontal**: Marcar los límites de clase $c_i$
4. **Eje vertical**: 
   - Si $a$ constante: frecuencia $n_i$ o $f_i$
   - Si $a_i$ variable: densidad $n_i/a_i$ o $f_i/a_i$
5. **Dibujar rectángulos**: Sin espacios, altura según paso 4
6. **Etiquetado**: Título, ejes, interpretación

---
## 4. Polígono de frecuencias

### 4.1 Definición

**Definición 4.1 (Polígono de frecuencias):**
Sea un histograma con marcas de clase $m_1, ..., m_k$ y frecuencias $n_1, ..., n_k$ (o densidades $h_1, ..., h_k$). El **polígono de frecuencias** es una representación gráfica que:
1. Conecta los puntos $(m_i, h_i)$ mediante segmentos de recta para $i=1,...,k$
2. Extiende el polígono hasta el eje horizontal en los extremos: añade puntos $(m_0, 0)$ y $(m_{k+1}, 0)$ donde $m_0 = c_1 - a/2$ y $m_{k+1} = c_{k+1} + a/2$

**Representación matemática:**
El polígono de frecuencias es una **función lineal a trozos** $g: [c_1 - a/2, c_{k+1} + a/2] \to \mathbb{R}_{\geq 0}$ definida por interpolación lineal entre los puntos $(m_i, h_i)$.
![[poligono-frecuencia.png]]
### 4.2 Propiedades

**Propiedad 4.1 (Equivalencia de área):**
Si el histograma tiene intervalos de amplitud constante $a$, el área bajo el polígono de frecuencias es **igual** al área del histograma:
$$\int_{c_1-a/2}^{c_{k+1}+a/2} g(x) dx = \sum_{i=1}^{k} a_i \cdot h_i = \sum_{i=1}^{k} n_i = N \quad \text{(o 1 si son frecuencias relativas)}$$
### 4.3 Ventajas

1. **Suavizado visual**: Proporciona una representación más continua que el histograma
2. **Comparación múltiple**: Permite superponer polígonos de diferentes grupos para comparación
3. **Tendencia central**: Facilita identificar la forma general de la distribución
4. **Transición conceptual**: Sirve como puente visual entre el histograma discreto y la **curva de densidad continua**

---
## 5. Curva de densidad y aproximación de la distribución (Opcional)

### 5.1 Concepto de curva de densidad

**Definición 5.1 (Curva de densidad empírica):**
Una **curva de densidad** es una función suave $f: \mathbb{R} \to \mathbb{R}_{\geq 0}$ que aproxima la distribución de los datos, obtenida mediante técnicas de **suavizado** del histograma o polígono de frecuencias.
![[dist-aprox.png]]
**Métodos de construcción:**
1. **Estimación por kernel (KDE)**: 
   $$\hat{f}(x) = \frac{1}{Nh} \sum_{i=1}^{N} K\left(\frac{x-x_i}{h}\right)$$
   donde $K$ es una función kernel (ej: gaussiano) y $h$ es el ancho de banda
   
2. **Ajuste paramétrico**: Ajustar una distribución teórica (normal, exponencial, etc.)
3. **Suavizado de splines**: Interpolación mediante funciones polinómicas a trozos
### 5.2 Interpretación visual

La curva de densidad permite visualizar:
- **Forma general** de la distribución
- **Tendencias** y patrones que podrían ser ocultados por el ruido del histograma
- **Aproximación a la distribución poblacional** subyacente

**Conexión con la teoría:**
En el límite cuando $N \to \infty$, bajo condiciones de regularidad:
$$\hat{f}(x) \xrightarrow{P} f(x)$$
donde $f(x)$ es la verdadera función de densidad de probabilidad de la población.

### 5.3 Forma de las distribuciones

Podemos hacernos de una idea de la forma de la distribucion de los datos mediante su histograma

#### 5.3.1 Simetría y asimetría

**Definición 6.1 (Distribución simétrica):**
Una distribución es **simétrica** respecto a un valor central $c$ si su función de densidad satisface:
$$f(c-x) = f(c+x) \quad \forall x \in \mathbb{R}$$

Visualmente, el histograma o curva se puede "doblar" por la mitad en $x=c$ y ambas partes coinciden.

**Característica estadística:** Para distribuciones simétricas unimodales:
$$\text{Media} = \text{Mediana} = \text{Moda} = c$$

**Ejemplos:** Distribución normal (gaussiana), distribución uniforme, distribución $t$ de Student.
![[dist-simetrica.png]]
**Definición 6.2 (Distribución asimétrica o sesgada):**
Una distribución es **asimétrica** si no cumple la propiedad de simetría. El **sesgo** cuantifica la dirección y magnitud de la asimetría.
#### 5.3.2 Sesgo positivo (sesgado a la derecha)

**Características:**
- La **cola derecha** es más larga que la izquierda
- La mayoría de los datos se concentran en valores **bajos**
- Media > Mediana > Moda (típicamente)

**Interpretación:** Hay algunos valores **extremadamente grandes** que "arrastran" la distribución hacia la derecha.

**Ejemplos:** Ingresos salariales, tiempos de espera, precios de viviendas, concentraciones químicas con límite inferior.

**Medida formal:** Coeficiente de asimetría de Fisher $g_1 > 0$

![[sesgada-der.png]]
#### 5.3.3 Sesgo negativo (sesgado a la izquierda)

**Características:**
- La **cola izquierda** es más larga que la derecha
- La mayoría de los datos se concentran en valores **altos**
- Media < Mediana < Moda (típicamente)

**Interpretación:** Hay algunos valores **extremadamente pequeños** que "arrastran" la distribución hacia la izquierda.

**Ejemplos:** Edad de fallecimiento en países desarrollados, calificaciones en exámenes fáciles, vida útil de productos con límite superior natural.

**Medida formal:** Coeficiente de asimetría de Fisher $g_1 < 0$

![[sesgada-izq.png]]
### 5.3.4 Modalidad

**Definición 6.3 (Moda de una distribución):**
Una **moda** es un valor (o intervalo) donde la distribución alcanza un **máximo local** de frecuencia. Formalmente, $x_0$ es una moda si:
$$f(x_0) \geq f(x) \quad \forall x \in (x_0-\epsilon, x_0+\epsilon)$$
para algún $\epsilon > 0$.

**Clasificación por modalidad:**
**Distribución unimodal**
- **Una sola moda** (un único pico)
- La más común en fenómenos naturales
- Ejemplos: Distribución normal, exponencial, chi-cuadrado
**Distribución bimodal**
- **Dos modas** distintas (dos picos)
- Sugiere la presencia de **dos subpoblaciones** o **dos procesos generadores** mezclados
- Ejemplo: Alturas en una población mixta (hombres y mujeres), tiempos de reacción en dos grupos experimentales

**Interpretación crítica:** Una distribución bimodal puede indicar que el análisis debe hacerse **por separado** para cada grupo.

![[bimodal.png]]
**Distribución multimodal**
- **Tres o más modas**
- Menos común, indica estructura compleja
- Puede sugerir necesidad de estratificación del análisis
**Distribución uniforme**
- **Sin moda** (todas las frecuencias son aproximadamente iguales)
- Rara en datos naturales, común en datos generados artificialmente
![[uniforme_histograma.png]]

*Esta solo son algunas de las formas que pueden tomar la distribución aproximada*

---
## Ejercicio
Hacer el histograma con su respectivo polígono de frecuencia y un bosquejo de la curva de distribución usando la tabla de frecuencias que completamos en la clase anterior

| Intervalo $I_i$ | Marca $m_i$ | $n_i$  | $N_i$ |  $f_i$   | $F_i$ (%) |
| :-------------: | :---------: | :----: | :---: | :------: | :-------: |
|  $[0.03,0.53)$  |    0.28     |   19   |  19   |   38%    |    38%    |
|  $[0.53,1.03)$  |    0.78     |   9    |  28   |   18%    |    56%    |
|  $[1.03,1.53)$  |    1.28     |   9    |  37   |   18%    |    74%    |
|  $[1.53,2.03)$  |    1.78     |   6    |  43   |   12%    |    86%    |
|  $[2.03,2.53)$  |    2.28     |   2    |  45   |    4%    |    90%    |
|  $[2.53,3.03)$  |    2.78     |   3    |  48   |    6%    |    96%    |
|  $[3.03,3.53]$  |    3.28     |   2    |  50   |    4%    |   100%    |
|    **Total**    |      —      | **50** |   —   | **100%** |     —     |
![[clase4-ejercicio1.png]]
![[clase-ejercicio1.2.png]]

---
## 6. Histograma de frecuencias absolutas vs. relativas

### 6.1 Comparación formal

| Aspecto | Frecuencias Absolutas $(n_i)$ | Frecuencias Relativas $(f_i)$ |
|:--------|:-----------------------------|:-----------------------------|
| **Rango del eje Y** | $[0, n_{\max}]$ donde $n_{\max} = \max_i n_i$ | $[0, f_{\max}]$ donde $f_{\max} = \max_i f_i \leq 1$ |
| **Interpretación de área** | Número total de observaciones: $\sum n_i = N$ | Proporción total: $\sum f_i = 1$ |
| **Comparabilidad** | Solo para muestras del mismo tamaño | Para muestras de **cualquier tamaño** |
| **Uso típico** | Análisis exploratorio único | Comparación entre grupos |
### 6.2 Ventaja fundamental del histograma de frecuencias relativas

**Teorema 6.1 (Invarianza por tamaño muestral):**
Sean $\mathbf{x}^{(1)} = (x_1^{(1)}, ..., x_{N_1}^{(1)})$ y $\mathbf{x}^{(2)} = (x_1^{(2)}, ..., x_{N_2}^{(2)})$ dos muestras de tamaños $N_1 \neq N_2$ provenientes de la misma población con distribución $F$. Si ambas muestras son suficientemente grandes y representativas, sus histogramas de **frecuencias relativas** convergirán a la misma forma, independientemente de $N_1$ y $N_2$:
$$\hat{f}_1(x) \approx \hat{f}_2(x) \approx f(x)$$
donde $f(x)$ es la verdadera densidad poblacional.

**Implicación práctica:** El histograma de frecuencias relativas permite:
1. **Comparar** distribuciones de grupos con diferentes tamaños muestrales
2. **Estandarizar** visualizaciones para presentaciones
3. **Interpretar** el histograma como aproximación de la **distribución de probabilidad**

**Ejemplo:** Comparar ingresos de dos ciudades con poblaciones muy diferentes ($N_1=500$ vs. $N_2=5000$). Con frecuencias absolutas, la comparación visual es engañosa; con frecuencias relativas, las formas se pueden comparar directamente.

## 7. Gráfico de sectores (Gráfico de torta)

### 7.1 Contexto histórico y definición intuitiva

Un gráfico de sectores es una representación circular que se divide en porciones (sectores), donde cada porción ilustra la proporción o porcentaje que una categoría representa sobre el total. Es la analogía visual clásica de "cómo se reparte un pastel" entre varias partes.

**Contexto Histórico:** El gráfico de sectores, ampliamente conocido como "gráfico de torta", fue introducido por primera vez por el ingeniero y economista escocés **William Playfair** en su obra *Statistical Breviary* (1801). Playfair, considerado el principal inventor de los gráficos estadísticos modernos, lo diseñó para mostrar las proporciones del Imperio Turco ubicado en Asia, Europa y África. Aunque en la actualidad existe un fuerte debate estadístico sobre su eficiencia visual frente al gráfico de barras, sigue siendo una de las representaciones más reconocidas globalmente.

### 7.2 Definición formal 

**Definición 7.1 (Gráfico de sectores o circular):**
Sea $X$ una **variable cualitativa** o **cuantitativa discreta** con $k$ clases: $X_1, X_2, ..., X_k$ y frecuencias absolutas $n_1, n_2, ..., n_k$ (o relativas $f_i$) tal que $\sum_{i=1}^{k} n_i = N$. Un **gráfico de sectores** es una partición de un disco bidimensional (círculo) en $k$ sectores circulares disjuntos, donde:
- Existe una biyección entre cada clase $X_i$ y un sector circular $S_i$.
- El **ángulo central** $\alpha_i$ (y bidimensionalmente el área) del sector $S_i$ es estrictamente proporcional a la frecuencia relativa $f_i$ de la clase representada.

**Propiedad 7.1 (Condición de proporcionalidad circular):**
Dado que el círculo completo abarca un ángulo de $360^\circ$ (o $2\pi$ radianes) representando el total poblacional (100%), el ángulo central proyectado para la clase $X_i$ se define rigurosamente como:
$$\alpha_i = f_i \cdot 360^\circ \quad \iff \quad \alpha_i = \left(\frac{n_i}{N}\right) \cdot 360^\circ$$

![[grafico-torta.png]]

### 7.3 Construcción formal

**Algoritmo de construcción:**

1. **Cálculo de frecuencias relativas:** Para cada clase $X_i$, calcular $f_i = \frac{n_i}{N}$.
2. **Determinación angular:** Para cada clase, computar $\alpha_i = f_i \cdot 360^\circ$. Validar siempre que $\sum_{i=1}^{k} \alpha_i = 360^\circ$ (salvo errores mínimos de redondeo).
3. **Trazado geométrico:** 
   - Dibujar un círculo de radio arbitrario $R$.
   - Trazar los $k$ sectores utilizando un transportador (o software), acumulando los ángulos $\alpha_1, \alpha_1+\alpha_2, ...$ de forma adyacente.
4. **Etiquetado riguroso:** Asociar cada sector a su categoría (mediante leyendas o colores puros) y plasmar el **porcentaje explícito** sobre el sector para evitar malinterpretaciones del observador.

### 7.4 Aplicabilidad, ventajas y limitaciones críticas

**Criterio de uso apropiado:**
El uso de gráficos de pastel está acotado preferentemente a:
- Variables **cualitativas** (nominales u ordinales).
- Ilustrar la **composición de un total cerrado** donde la suma es unívocamente el 100%.
- Escenarios de dimensionalidad reducida (por convención general, $\mathbf{k \leq 5}$).

**Limitaciones y problemas perceptivos (Cleveland y McGill, 1984):**
La investigación formal en cognición visual ha demostrado sistemáticamente que **el cerebro humano es muy ineficiente decodificando ángulos y áreas** en comparación con las longitudes unidimensionales (como en un diagrama de barras). 

- **Dimensionalidad excesiva:** Para muchas clases ($k > 5$), el gráfico se satura en "rebanadas" minúsculas, generando ruido cognitivo perceptible.
- **Dificultad de contraste analítico:** Discernir perceptualmente entre una proporción del $18\%$ (aprox $65^\circ$) y una de $19\%$ (aprox $68^\circ$) sin etiquetas numéricas es un esfuerzo imposible para la percepción.
- **Falacia del 3D:** Renderizar un gráfico de torta en 3D introduce una inclinación y altera la perspectiva aparente de los sectores fronterizos al observador, una grave violación a los principios éticos de la **proporcionalidad verdadera de Tufte**.

## 8. Ojiva o polígono de frecuencias acumuladas

### 8.1 Contexto histórico y etimología

**Contexto Histórico:** El término "ojiva" aplicado a la estadística fue introducido por vez primera en 1901 por el eminente estadístico y economista británico **Arthur Lyon Bowley**. Bowley advirtió en sus publicaciones que la forma geométrica asintótica que adquiere una distribución de frecuencias acumuladas (particularmente la integral de la famosa Campana de Gauss) se asemejaba asombrosamente a la "ojiva" o arco apuntado clásico de la arquitectura gótica medieval y la forma balística. Esta dualidad analítico-geométrica fue tan elocuente que el término bautizó al gráfico de forma universal.

**Definición casual:**
Una ojiva es un gráfico de línea continuo que nos exhibe el recuento acumulado ("running total") de los datos a medida que avanzamos a lo largo de las clases de una variable. En lugar de responder "¿cuántas personas miden exactamente 1.70 m?" (como lo haría un histograma o curva de densidad en una clase), la ojiva responde inquisitivamente: "¿qué porcentaje o volumen de personas miden 1.70 m **o menos**?".

### 8.2 Definición formal matemática

**Definición 8.1 (Ojiva o Polígono de Frecuencias Acumuladas):**
Sea $X$ una variable cuantitativa (continua o discreta) agrupada secuencialmente en $k$ clases finitas de la forma $I_i = [c_i, c_{i+1})$, donde $c_{i+1}$ representa abstractamente el límite superior estricto del intervalo. Sea $F_i$ la **frecuencia absoluta acumulada** (o $F_{R,i}$ como frecuencia relativa acumulada) definida de forma recursiva como la sumatoria integral $F_i = \sum_{m=1}^{i} f_m$.
La **ojiva** es una representación paramétrica escalar consistente en la unión lineal de puntos cartesianos evaluados **exclusivamente sobre el límite superior** de cada clase. Topológicamente, es la traza vectorial unívoca dictada por los pares ordenados:
$$P_i = (c_{i+1}, F_i), \quad \forall i \in \{1, 2, ..., k\}$$

**Teorema 8.1 (Propiedad de isomorfismo continuo empírico):**
En el modelado inferencial, la ojiva de frecuencias relativas porcentuales actúa directamente como el principal **Estimador Empírico Computacional** de la verdadera **Función de Distribución Acumulada** (FDA, o CDF por sus siglas en inglés) del marco axiomático de probabilidad, delimitada canónicamente por:
$$F_X(x) = P(X \leq x)$$
**Axioma de Convergencia asintótica:** Según los teoremas del límite de Glivenko-Cantelli, conforme el tamaño muestral $N \to \infty$ y el ancho de clase $\Delta c \to 0$, la curva discreta quebrada de la ojiva converge estructural y uniformemente en su probabilidad hacia la forma suave continua de su variable generatriz teórica.

### 8.3 Algoritmo metodológico de construcción

1. **Tabulación exhaustiva escalar:** Generar las columnas obligatorias de "Límites Superiores de Clase" ($c_{i+1}$) y la columna dependiente ligada a la secuencia de frecuencias acumuladas $F_i$ (absolutas numéricas) o $F_{R,i}$ (relativas porcentuales normalizadas a base 1).
2. **Anclaje nulo topológico:** Para asegurar la validez física inquebrantable que un área probabilística vacía genera probabilidad $0$, se **debe anclar por obligación un nodo cero** artificial inferior coincidente con límite métrico primario ($c_1$) con una coordenada en el piso horizontal, formando la dupla $(c_1, 0)$.
3. **Mapeo vectorial cartesiano escalonado:** Trazar posicionalmente el resto de la bóveda de la data trazando todos los $k$ pares empíricos calculados $(c_{i+1}, F_i)$ en el espacio métrico plano $\mathbb{R}^2$.
4. **Interpolación segmentada directa:** Unir cronológicamente (con sentido absoluto de izquierda a derecha sin nunca retroceder) los nodos vectoriales contiguos valiéndose de segmentos puros de recta matemática en una sola dimensión.
5. **Tope integral estructural:** El punto algorítmico terminal $(c_{k+1}, F_k)$ tiene que ascender irrevocablemente hasta alcanzar o emparejarse con el coloso final numérico poblacional analizado completo $N$ (para medidas absolutas) o su análogo escalado a cota absoluta $100\%$ ($1.0$). Un déficit aquí expone error humano en suma.

![[ojiva-acumulada.png]]

### 8.4 Utilidad paramétrica heurística e interpolación de posición

**Relevancia funcional insuperable y utilidades analíticas profundas:**
- **Localización microscópica y resolución inversa de Quantiles:** La curva de ojiva permite calcular interpolaciones algebraicas por inversión funcional. En ciencias sociales y ciencias de la salud, si deseamos estimar el **Decil 8** o **Percentil 85** poblacional, únicamente hace falta lanzar un rayo vector topológico horizontal trazado del eje $Y$ dependiente (en altura 80% u 85%) hacia adelante, impactar la ojiva en el plano de dispersión, y acto seguido dictaminar una transversal vertical plomada directo hasta el eje de piso estático $X$ para revelar en qué estrato crudo puntual ocurrió dicho percentil anatómico. Sirve como regla general para cualquier Cuartil $Q_1$, Mediana $Q_2$, etc.
- **Auditoría de densidad y aglomeración poblacional de la pendiente:** En las gráficas de ojiva, rastrear su derivada matemática visual o inclinación (pendiente de secante), informa directamente la densidad subyacente de la data real. Zonas verticales escarpadas implican una altísima condensación estadística extrema de la moda de variados datos saturados en un corto trecho geométrico de longitud. Como es de esperarse, dominios con pendiente larga mesetaria avisan enormes fosos empíricos despoblados. El viraje global y gradual de todo el sistema hacia cóncavo o hacia convexo informa de a qué extremo se localiza el sesgo direccional macro (asimetría global), sin necesidad a calcular de forma teórica un parámetro explícito por de $g_1$ del coeficiente asimétrico cúbico de Fisher a mano alzada.

## 9. Diagrama de Pareto

### 9.1 Contexto histórico y definición intuitiva

Un diagrama de Pareto es una poderosa combinación analítica que funde un gráfico de barras organizado de mayor a menor con un polígono de frecuencias acumuladas superpuesto. Su propósito principal en gestión y ciencia es ayudar a identificar rápidamente los problemas y causas más influyentes de un sistema, mostrando de forma muy elocuente cuáles variables se llevan el "león de la contribución" a un efecto global.

**Contexto Histórico:** El principio subyacente fue introducido a finales del siglo XIX por el economista y sociólogo italiano **Vilfredo Pareto**, quien observó empíricamente que aproximadamente el 80% de la riqueza o propiedad de tierras en Italia estaba en manos de apenas el 20% de la población. Más tarde, en la década de 1940, el ingeniero de calidad **Joseph Juran** universalizó y formalizó este concepto estadístico bajo el nombre "Principio de Pareto" y lo adaptó al control de calidad, acuñando la famosa frase que distingue contundentemente entre los "pocos vitales y los muchos triviales".

### 9.2 Definición formal y fundamentación empírica

**Definición 8.1 (Diagrama de Pareto):**
Sea $X$ una **variable cualitativa o nominal** que parametriza fallos, causas o eventos discretos con $k$ clases finitas: $X_1, X_2, ..., X_k$. Sean $n_1, n_2, ..., n_k$ sus respectivas frecuencias absolutas, las cuales reciben un reordenamiento artificial estricto en forma **monótonamente decreciente**, tal que $n_1 \geq n_2 \geq ... \geq n_k$.
Un **diagrama de Pareto** es un constructo visual híbrido compuesto por:
1. Un **gráfico de barras vertical**, donde la ordenada máxima de cada base rectangular es proporcional a su frecuencia respectiva $n_i$. Estas barras se adhieren sin separación espacial para ilustrar continuidad analítica.
2. Una **ojiva porcentual** adjunta (un polígono de las frecuencias relativas acumuladas $F_i$), escalada sistemáticamente contra un eje secundario de ordenadas (Y-derecho) mapeado bajo el intervalo $[0\%, 100\%]$.

**Teorema 8.1 (Principio de escasez o de eficacia marginal de Pareto - Regla 80/20):**
Aunque no es una ley puramente axiomática, el postulado se revela como un isomorfismo empírico irrefutable en distribuciones de asimetría radical (colas pesadas). Establece que, usualmente, un pequeño clúster de causas (normalmente alrededor de $j/k \approx 0.20$) engendra la arrolladora mayoría del impacto total acumulado en el sistema; es decir:
$$\sum_{i=1}^{j} f_i \approx 0.80$$

![[diagrama-pareto.png]]

### 9.3 Rigor metodológico en su algoritmo de construcción

Construir un Pareto libre de sesgos exige acatar un algoritmo normalizado de doble escala:

1. **Recolección y taxonometría categórica:** Cuantificar el vector de incidencias de un sistema de acuerdo a tipología bajo una ventana del tiempo controlada $T$.
2. **Re-ordenación paramétrica:** Ordenar las categorías en el eje de las abscisas (X) estrictamente mediante su frecuencia $n_i$, de forma decreciente. *(Axioma de la miscelánea: Si existe un bloque heterogéneo condensado de eventos menores bajo el nombre "Otros", matemáticamente debe posicionarse al extremo final del eje $\mathbf{X_k}$, subvirtiendo la regla de decrecimiento para descartarlo como ruido visual)*.
3. **Mapeo matemático acumulativo:** Computar para cada categoría reclasificada $i$, la frecuencia local relativa $f_i$ y su sumatoria integral $F_i = \sum_{m=1}^{i} f_m$.
4. **Acoplamiento de proyección topológica:** 
   - **Eje Y izquierdo (Primario):** Escalar sobre la suma discreta agregada ($0 \to \sum_{i=1}^k n_i$).
   - **Eje Y derecho (Secundario):** Escalar paramétricamente ($0\% \to 100\%$).
   - **Anclaje de la ojiva:** Anclar los nodos del polígono acumulativo asegurando que el nodo terminal converja exactamente con el techo absoluto (100%) en el límite derecho.

### 9.4 Usabilidad analítica y restricciones de validación

**Valoración funcional en la praxis heurística:**
Su aplicación trasciende la estadística exploratoria simple y fundamenta la toma de decisiones gerencial en las ramas más técnicas *(e.g. Lean Six-Sigma, Desarrollo de Software)*. Ataca el dilema paramétrico de forma pragmática: **¿Hacia qué clúster apunto mis recursos logísticos para optimizar drásticamente la esperanza del ROI correctivo?** No hay alternativa contemporánea más elegante ni intuitiva para segmentar la "cabeza" que acapara la varianza poblacional general.

**Limitaciones y advertencias del algoritmo:**
- **La ceguera ante el "peso o gravedad costosa" (Severity Bias):** Mide el volumen pero no calibra el daño. Un defecto logístico rarísimo (ej. explosión termodinámica eventual) representará un $n_i$ bajísimo confundiéndose como "trivial" según la ojiva, pese a ser fatal. Solución: la mutación por *Pareto Multiplicativo Ponderado* (Costos $\propto n_i \cdot \text{Impacto}_i$).
- **No escarba la relación causal basal funcional:** Revelará sin lugar a dudas *qué y cuánto* es lo que más falla en superficie, pero nunca proporcionará una epifanía empírica sobre *por qué* suceden esas fallas ni si exhiben colinealidad fuerte entre ellas.---


## 10. Diagrama de tallo y hoja (Stem-and-Leaf Plot)

### 10.1 Contexto histórico y definición intuitiva

Es una técnica de representación semi-gráfica que desintegra "quirúrgicamente" cada número de una muestra cuantitativa en dos partes emparejadas: un "tallo" (los primeros dígitos posicionales) y una "hoja" (el último dígito residual). Visualmente, exhibe la silueta de un histograma horizontal, pero construido enteramente por el texto de los números crudos, impidiendo la pérdida tradicional de información numédica que ocurre al hacer agrupamientos ciegos.

**Contexto Histórico:** El diagrama de tallo y hoja fue formalizado en la década de 1960 por el eminente matemático de Princeton **John W. Tukey**, pionero indiscutible del Análisis Exploratorio de Datos (EDA). Tukey buscaba desarrollar heurísticas visuales "rápidas y sucias" (quick-and-dirty) que los estadísticos pudieran trazar analógicamente en una época donde las computadoras interactuaban solo con tarjetas perforadas y carecían del renderizado visual moderno. Su filosofía no concebía este gráfico para reemplazar al robusto histograma, sino complementarlo para el modelado instantáneo y el respeto a la cifra atómica real.

### 10.2 Definición formal y fundamentación topológica

**Definición 9.1 (Diagrama de tallo y hojas):**
Sea un conjunto de datos poblacionales (o muestrales) ordenado localmente $X = \{x_1, x_2, ..., x_N\}$ donde cada variable empírica $x_i$ está codificada en un sistema posicional de numeración abstracta (típicamente base 10). Se estipula un **operador de partición ortogonal** $\pi(x_i) = (T_i, H_i)$ donde:
- **Tallo ($T_i$):** Componente algebraico de mayor magnitud jerárquica (decenas, centenas o millares).
- **Hoja ($H_i$):** El remanente truncado unitario de menor sensibilidad jerárquica métrica, usualmente acotado al rango $H_i \in \{0, 1, ..., 9\}$.

Consecuentemente, se aglomeran todos los submúltiplos $H_i$ co-relacionados a un mismo operador origen $T$ en una matriz indexada bidimensional. Al graficarlo, la cardinalidad de hojas subyacente a un tallo emula estructuralmente la frecuencia absoluta $n_i$ de un intervalo modular del histograma clásico.

![[diagrama-tallo-hoja.png]]

### 10.3 Algoritmo logístico de construcción sistemática

La sintaxis constructiva requiere una estricta segregación numérica y canónica lineal:

1. **Anclaje de la granularidad posicional:** Aislar el dígito dominante como núcleo del "tallo". Evaluando el dato experimental $x_k = 72$, el multiplicador decenal equivale al $7$ (escala estructural matriz) y remite como hoja unitaria expansiva al $2$.
2. **Bisección vertical cartesiana:** Perpendicular a las ordenadas, trazar transversalmente un segmento interceptor vertical. En la región izquierda (abscisas categóricas), enumerar de forma asintóticamente estricta todo el intervalo métrico desde $T_{\min}$ a $T_{\max}$. ¡Advertencia estadística severa! Omitir visualmente un tallo inactivo (tallo donde ninguna hoja aterrizó y su frecuencia es $0$) vulnera y distorsiona la forma de densidad de la distribución empírica. 
3. **Plasmado de la ramificación perimetrante:** Consignar para cada evento experimental crudo su respectivo $H_i$, indexándolo de forma paralela u horizontal al elemento $T_i$ de su tallo creador.
4. **Ordenamiento canónico (post-tabulación EDA):** Ordenar estocásticamente las hojas de izquierda a derecha ascendentemente por orden de magnitud. Un tallo de muestra quedará codificado descriptivamente así: $5 \mid 1 \ 1 \ 2 \ 4 \ 6 \ 9$.

### 10.4 Usabilidad analítica, pros y restricciones lógicas

**Aciertos paramétricos insuperables:**
- **Inmutabilidad intrínseca del dato (Data Intactness):** En la ontología del histograma estándar un intervalo "desvanece" la variable experimental tragándose el valor microscópico original (sabemos que hay 5 datos entre 10 y 20, pero no sus cifras). El diagrama de ramificación preserva la identidad atómica exacta y total sin alterar ni una cifra.
- **Rastreo forense subatómico:** Su fisonomía devela imperfecciones sub-paramétricas ocultas, logrando identificar modas localizadas o anomalías psicológicas severas como el sesgo del redondeo algorítmico humano (un fenómeno en toma de inventarios donde por economía cerebral, el personal tabula un exceso brutal de valores terminados preferentemente en digitación de los rangos $\mathbf{0}$ o $\mathbf{5}$).

**Limitantes estadísticas dogmáticas:**
- **Barrera de fatiga dimensional (Hipótesis del N-Grande):** Resulta analíticamente asfixiante e ilegible bajo muestreos poblacionales densos ($N > 100$). Acentuadas aglomeraciones ahogan diametralmente la horizontalidad del papel, destrozando la percepción cognitiva de heurística rápida ideada por Tukey.
- **Abstracción decimal anidada:** Tratándose de conjuntos experimentales de crudo control analítico con una altísima precisión y varianza marginal microscópica (por ejemplo, mediciones farmacológicas del orden $\{0.012, 0.015, 0.018\}$), el tallo natural deviene disfuncional. Dibujarlo forzaría re-escalamiento cognitivamente agobiante (factores multiplicativos $\lambda$-shift de $\times 1000$ previo al particionado) lo cual somete al interpretador posterior del gráfico a una fuerte probabilidad de equivocación y sesgo de lectura.


## 11. Diagrama de caja y bigotes (Box Plot)

### 11.1 Contexto histórico y definición intuitiva

Un diagrama de caja es una estandarización visual que destila cualquier conjunto de datos masivo en un simple rectángulo (la caja) con dos líneas extendidas (los bigotes). Nos muestra de inmediato dónde está concentrada la "mitad" de la población, dónde está el equilibrio central, y detecta automáticamente aquellos valores que son tan extremos que deben considerarse anomalías o "bichos raros" dentro de la muestra.

**Contexto Histórico:** El diagrama de caja, o _boxplot_, es otra joya magistral introducida en 1970 por el matemático **John W. Tukey** (y diseminada en su influyente libro de 1977, *Exploratory Data Analysis*). Mientras el histograma intentaba modelar toda la curva de densidad y el diagrama de tallo y hoja buscaba preservar toda la cifra atómica, Tukey diseñó el _boxplot_ con una filosofía contraria pero igualmente brillante: **la abstracción y la robustez**. Su objetivo era comprimir la "columna vertebral" de una distribución en una representación mínima e hipereficiente que fuera resistente a anomalías.

### 11.2 Arquitectura formal y el Resumen de los 5 Números

**Definición 10.1 (Diagrama de Caja de Tukey):**
Sea una variable aleatoria cuantitativa con una muestra ordenada $X = (x_{(1)}, x_{(2)}, ..., x_{(N)})$. El diagrama de caja es la representación geométrica bidimensional fundamentada estrictamente en el **Resumen de los 5 números estadísticos de posición no paramétricos**:
1. El valor Mínimo empírico (excluyendo atípicos).
2. El Primer Cuartil ($Q_1$ o percentil 25).
3. La Mediana ($Q_2$ o percentil 50).
4. El Tercer Cuartil ($Q_3$ o percentil 75).
5. El valor Máximo empírico (excluyendo atípicos).

**Axiomas de diseño estructural:**
- **La Caja central (El "Core"):** Se traza un rectángulo delimitado por los valores ordinales de $Q_1$ (base) y $Q_3$ (techo). Por definición matemática inquebrantable, exactamente **el 50% central de la dispersión de datos de toda la muestra habita dentro de esta caja**.
- **La Dispersión Robusta (RIC):** La altura teórica de la caja se define como el Rango Intercuartílico: $\text{RIC} = Q_3 - Q_1$. Esta métrica mide la dispersión y es completamente inmune y ortogonal a la influencia de valores extremos.
- **La Cicatriz de la Mediana:** Se segmenta la caja con una línea transversal ubicada exactamente en el valor de la Mediana ($Q_2$). Su asimetría respecto al centro de la caja revela de inmediato el sesgo natural (positivo o negativo) de la distribución focal.

![[diagrama-caja.png]]

### 11.3 Algoritmo heurístico de construcción y detección de anomalías

El genio de este gráfico radica en su rigor para definir y marginar matemáticamente qué es un "Outlier" (valor atípico), negándose a dejarlo a la subjetividad humana.

1. **Tabulación posicional:** Calcular rigurosamente los estadísticos de orden $Q_1$, $Mediana$ y $Q_3$. Trazar la caja transversal y su línea de segmentación mediana.
2. **Cálculo de las Barreras Teóricas Inobservables (Fences):** Se computan los límites teóricos del sistema usando un factor de escala canónico propuesto por Tukey (1.5):
   - **Barrera Interior Inferior:** $\text{LII} = Q_1 - 1.5 \cdot \text{RIC}$
   - **Barrera Interior Superior:** $\text{LIS} = Q_3 + 1.5 \cdot \text{RIC}$
   *(Nota: Valores que excedan $3.0 \cdot \text{RIC}$ se denominan "Atípicos Extremos" o "Far Outliers").*
3. **Expansión de los Bigotes (Whiskers):** Los segmentos (bigotes) no viajan al infinito ni hasta los límites teóricos. Un bigote se arrastra hacia afuera solo hasta hacer contacto con **el último dato experimental real** que orbite dentro del límite de las barreras (es decir, el dato más extremo que aún cumple $x_i \geq \text{LII}$ y $x_i \leq \text{LIS}$).
4. **Graficado individual del atípico:** Todo $x_i$ muestral que perfore y sobreviva fuera de estas barreras teóricas se considera una desviación, y es penalizado. Pierde el "anonimato" del bloque y es graficado individualmente flotando como un punto explícito, asterisco o cruz.

### 11.4 Relevancia analítica de alto nivel y restricciones

**¿Por qué es uno de los gráficos más importantes de la estadística contemporánea?**
- **El Rey de la Comparatividad Estratificada:** Poner dos histogramas superpuestos es visualmente ruidoso. Poner 10 es ininteligible. Sin embargo, colocar 10 diagramas de caja en paralelo compartiendo el mismo eje (Boxplots paralelos) produce un despliegue paramétrico magnífico donde el cerebro humano compara instantáneamente el cambio de medias, empujes y varianzas de 10 estratos distintos de una pasada.
- **Robustez y blindaje analítico:** Al ignorar la Media $(\mu)$ y la Varianza $(\sigma^2)$ (las cuales nacen sesgadas ante el menor defecto extremo), el gráfico de caja usa métricas no paramétricas ordinales ($Q_1, Q_2, Q_3$). Esto lo vuelve indestructible y ciego a perturbaciones extremas que destruirían otros modelos matemáticos.

**Limitantes estadísticas dogmáticas:**
- **Encubridor de las formas multi-modales:** La abstracción de Tukey tiene un costo gravísimo. Diferentes distribuciones empíricas completamente opuestas (una masa uniforme, y un fenómeno estrictamente bimodal de dos picos) **pueden generar algebraica e idénticamente el mismo diagrama de caja**. El boxplot asume unimodalidad tácita; es por ello que hoy en día, las variables críticas bivariadas en _Machine Learning_ o ciencia de datos exigen graficar encima el diagrama de caja sobre un *Violin Plot* (que incorpora la curva real de la densidad empírica lateralmente).


---

## 11. Principios de buena práctica en visualización

### 11.1 Los principios de Tufte (1983)

Edward Tufte estableció principios fundamentales para gráficos estadísticos efectivos:

1. **Integridad gráfica**: Evitar distorsiones. El tamaño visual debe ser proporcional a las cantidades representadas.
2. **Maximizar la razón datos-tinta**: Eliminar elementos decorativos innecesarios (chartjunk).
3. **Claridad**: Cada elemento debe tener un propósito comunicativo claro.
4. **Densidad de datos**: Mostrar la mayor cantidad de información en el menor espacio posible sin sacrificar claridad.

### 11.2 Errores comunes a evitar

| Error | Problema | Solución |
|:------|:---------|:---------|
| **Eje Y truncado** | Exagera diferencias pequeñas | Iniciar eje en cero |
| **3D innecesario** | Distorsiona proporciones astronómicamente | Usar 2D siempre que sea posible, estricto en gráficos de torta |
| **Demasiados colores** | Confunde, no aporta información | Usar color con propósito específico o paleta monocromática |
| **Escalas inconsistentes** | Impide comparación | Estandarizar escalas al comparar (e.g. ojivas normalizadas al 100%) |
| **Falta de etiquetas** | Información incompleta | Título, ejes, leyenda, unidades numéricas claras |

---

## 12. Resumen conceptual

### 12.1 Tabla de decisión para elegir gráfico

```mermaid
graph TD
    A[¿Qué gráfico usar?] --> B{Naturaleza de la Variable}
    
    B -->|Cualitativa / Nominal| C{¿Objetivo Analítico?}
    C -->|Comparar conteos| C1[Gráfico de barras]
    C -->|Composición Total 100%| C2[Gráfico de sectores<br/>(si k ≤ 5)]
    C -->|Identificar "Pocos Vitales"| C3[Diagrama de Pareto]
    
    B -->|Cuantitativa Continua /<br/>Discreta Agrupada| D{¿Objetivo Analítico?}
    D -->|Densidad General| D1[Histograma + Curva]
    D -->|Preservar Cifra Atómica| D2[Tallo y Hoja<br/>(si N < 100)]
    D -->|Cuantiles y Percentiles| D3[Ojiva de Frecuencias<br/>Acumuladas]
    D -->|Comparabilidad Estratificada| D4[Diagrama de Caja<br/>(Box Plot)]
    D -->|Comparar Densidades| D5[Polígonos Superpuestos]
    
    style A fill:#e1f5ff,stroke:#333,stroke-width:2px
    style B fill:#fff4e1,stroke:#333,stroke-width:2px
    style C fill:#f9e1ff,stroke:#333,stroke-width:1px
    style D fill:#e1ffe5,stroke:#333,stroke-width:1px
```

### 12.2 Conceptos clave añadidos y consolidados

| Concepto | Definición sintética / Topológica | Aplicación Estadística |
|:---------|:--------------------------------|:-----------------------|
| **Gráfico de barras** | Rectángulos separados, altura proporcional | Nominales / Discretas simples |
| **Sectores (Torta)** | Biyección ángulo-frecuencia $\alpha_i = f_i 360^\circ$ | Composición de totales ($k \leq 5$) |
| **Ojiva (FDA)** | Vector escalonado asintótico $(c_{i+1}, F_i)$ | Extracción inversa de Percentiles |
| **Diagrama de Pareto** | Barras decrecientes + Ojiva acumulada acoplada | Regla técnica 80/20, Six-Sigma|
| **Tallo y Hoja (EDA)** | Partición posicional ortogonal $\pi(x) = (T, H)$ | Auditoría subatómica, $N < 100$ |
| **Boxplot (Caja)** | Abstracción de Tukey basada en $Q_1, Q_2, Q_3$ | Análisis de atípicos, Robustez |
| **Histograma** | Rectángulos adyacentes, área total conservada | Función de Densidad (Continuas) |
| **Simetría y Sesgo** | Relación de colas y deltas de Media-Mediana | Diagnóstico direccional previo |

---

## 13. Ejemplo integrador

**Problema:** Analizar la distribución de alturas (en cm) de 100 estudiantes universitarios.

**Datos resumidos:**

| Intervalo | $n_i$ | $f_i$ | $N_i$ | $F_i$ |
|:---------:|:-----:|:-----:|:-----:|:-----:|
| [150,155) | 5 | 0.05 | 5 | 0.05 |
| [155,160) | 12 | 0.12 | 17 | 0.17 |
| [160,165) | 23 | 0.23 | 40 | 0.40 |
| [165,170) | 28 | 0.28 | 68 | 0.68 |
| [170,175) | 18 | 0.18 | 86 | 0.86 |
| [175,180) | 10 | 0.10 | 96 | 0.96 |
| [180,185] | 4 | 0.04 | 100 | 1.00 |

**Análisis gráfico:**

1. **Histograma**: Muestra distribución **unimodal** con moda en $[165,170)$
2. **Ojiva Cuantílica**: El $F_i=0.40$ en el límite $165$, indica que el primer cuartil y casi el percentil 40 se posiciona justo debajo de $165\text{cm}$.
3. **Forma**: Aproximadamente **simétrica**, aunque con ligero **sesgo positivo** (cola derecha ligeramente más larga)
4. **Comparación Estratificada**: Si queremos comparar con otra universidad, usamos múltiples **Boxplots paralelos** con el mismo eje métrico.

---

## 14. Ejercicios propuestos

**Ejercicio 1 (Visualización Avanzada):** Explica rigurosamente desde el paradigma del Análisis Exploratorio de Datos (EDA) de John Tukey, qué ventajas empíricas tiene el "tallo y hoja" sobre el histograma clásico si el tamaño de muestra poblacional es $N=42$.

**Ejercicio 2:** Dada la siguiente distribución de calificaciones (0-10):
```
5.5, 6.0, 6.5, 7.0, 7.0, 7.5, 7.5, 7.5, 8.0, 8.0,
8.5, 8.5, 8.5, 8.5, 9.0, 9.0, 9.5, 10.0
```
a) Construye un diagrama de caja calculando a mano sus $5$ estadísticos.
b) Proyecta una Ojiva y evalúa a ojo desnudo dónde cruza la línea del Decil 8 ($80\%$). 
c) Clasifica la asimetría local.

**Ejercicio 3:** ¿Bajo qué escenario algorítmico el Teorema o Diagrama de Pareto perdería su fundamentabilidad analítica a nivel de gestión de calidad? (Pista: analizar una distribución estrictamente uniforme de errores).

**Ejercicio 4 (Cálculo Paramétrico):** Demuestra formalmente que una muestra empírica donde el límite empírico inferior coincide absolutamente con $Q_1$ carecerá visiblemente de un "bigote estructural izquierdo" en el Boxplot de Tukey.

---

## 15. Conexión con temas futuros

Los gráficos estudiados en esta clase son fundamentales para:
- **Estadística Inferencial**: Visualizar supuestos de normalidad antes de pruebas paramétricas
- **Análisis de Regresión**: Gráficos de dispersión para identificar relaciones
- **Control de Calidad**: Histogramas para monitorear procesos
- **Machine Learning**: Análisis exploratorio de datos (EDA) antes de modelado

---

**Referencias bibliográficas:**
- Tufte, E. R. (1983). *The Visual Display of Quantitative Information*. Graphics Press.
- Cleveland, W. S. (1993). *Visualizing Data*. Hobart Press.
- Tukey, J. W. (1977). *Exploratory Data Analysis*. Addison-Wesley.
- Wilkinson, L. (2005). *The Grammar of Graphics* (2nd ed.). Springer.