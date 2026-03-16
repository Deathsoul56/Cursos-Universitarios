# Estadísticos Descriptivos

## 1. Introducción y topología empírica de los datos

### 1.1 Motivación y marco conceptual

El Análisis Exploratorio de Datos (EDA) depende fuertemente de representaciones gráficas, pero la intuición visual carece del rigor algebraico absoluto necesario para la inferencia estadística, la demostración de teoremas y el modelaje automatizado. Aquí es donde intervienen los **estadísticos descriptivos**, métricas formales que comprimen (proyectan) la alta dimensionalidad de una muestra estocástica en escalares de alta densidad de información. 

Para estudiantes de ciencias e ingeniería superior, ya no basta con referirse a una media como un simple "promedio escolar". Es imperativo comprender a estos estadísticos paramétricos como **funcionales matemáticos**, operadores algebraicos y estimadores empíricos que minimizan de funciones de pérdida (*Loss Functions*) específicas en espacios métricos.

### 1.2 Nomenclatura axiomática y definiciones basales

Antes de explorar los estimadores, es obligatorio establecer una notación rigurosa:
Sea un espacio muestral del cual extraemos una muestra aleatoria de tamaño $n$. Definimos el vector muestral columna $\mathbf{x} = (x_1, x_2, ..., x_n)^T \in \mathbb{R}^n$, donde cada $x_i$ representa la $i$-ésima realización experimental de una variable aleatoria $X$.

- **Vector muestral original:** $\mathbf{x} = (x_1, x_2, ..., x_n)^T$
- **Estadísticos de orden (Vector ordenado):** $\mathbf{x}_{()} = (x_{(1)}, x_{(2)}, ..., x_{(n)})^T$ donde rige la desigualdad monotónica estricta $x_{(1)} \leq x_{(2)} \leq ... \leq x_{(n)}$. El valor $x_{(1)}$ es el límite inferior muestral y $x_{(n)}$ la cota empírica superior.
- **Datos agrupados (Partición del espacio):** Si el dominio continuo se discretiza en $k$ clases finitas, denotamos $m_i$ como la marca de clase (el centroide geométrico de un intervalo), $n_i$ como la frecuencia absoluta intra-clase y $f_i = n_i/n$ como la frecuencia marginal relativa (que integra a unidad $\sum f_i = 1$).

**Definición 1.1 (Estadístico muestral):**
Un **estadístico** es, analíticamente, cualquier transformación medible $T$ que mapea el espacio muestral multidimensional hacia la recta real, $T: \mathbb{R}^n \to \mathbb{R}$ (o a un vector $\mathbb{R}^k$), y cuya definición algebraica explícita **no depende de ningún parámetro poblacional teórico desconocido**. Actúa como estimador observable del parámetro poblacional abstracto $\theta$.

Se clasifican taxonómicamente en cuatro grandes familias topológicas:
1. **Medidas de Tendencia Central (Operadores de Localización):** Buscan parametrizar el "centro de masa" geométrico de la distribución de densidad probabilística (Media, Mediana, Moda).
2. **Medidas de Dispersión (Operadores de Escala):** Cuantifican normativamente el esparcimiento, entropía u homogeneidad del vector dimensional respecto a su centroide (Varianza, Desviación Estándar, RIC).
3. **Medidas de Posición (Cuantiles):** Estratifican el espacio muestral o función de distribución acumulada (FDA) en proporciones probabilísticas equiprobables (Cuartiles, Deciles).
4. **Medidas de Forma (Momentos de Orden Superior):** Evalúan deformaciones geométricas de las colas y la agudeza unimodal abstrayéndose de su escala o traslación posicional (Sesgo, Curtosis).

---

## 2. Operadores de Tendencia Central y de Localización

### 2.1 La Media Aritmética (Centro de Masa Geométrico)

**Contexto Histórico:** Sus primeros indicios algorítmicos recalan en la civilización babilónica. Sin embargo, su consolidación moderna y justificación paramétrica le debe su existencia a gigantes como **Carl Friedrich Gauss** y **Adrien-Marie Legendre**. En el siglo XIX, mientras calculaban las órbitas de asteroides elípticos, ambos genios demostraron independientemente que la media aritmética es precisamente el único operador empírico que acota los ruidos astronómicos gaussianos.

**Definición casual:** 
Es la variable de "equilibrio estático" equitativo del sistema cerrado muestral. Si las observaciones fuesen masas discretas amarradas a una palanca rígida horizontal sin peso (el eje Numérico), la media matemática es la coordenada puntual $X$ exacta donde debes colocar un pivote de soporte para anular todos los momentos de torsión, evitando que el sistema colapse.

**Definición 2.1 (Media aritmética muestral):**
Dado un vector de observaciones reales $\mathbf{x} \in \mathbb{R}^n$, definimos el **operador de media aritmética** $\bar{x}$ (siendo este el un estimador insesgado de la esperanza matemática estocástica poblacional $\mu = \mathbb{E}[X]$) estrictamente como la proyección de suma escalar equitativa:
$$\bar{x} = \frac{1}{n} \sum_{i=1}^{n} x_i$$
Para vectores tabulados y factorizados en $k$ clases con frecuencias $n_i$ y centroides $m_i$, el operador es idéntico al producto punto de los vectores de clase y densidad probabilística:
$$\bar{x} = \frac{1}{n} \sum_{i=1}^{k} m_i \cdot n_i = \sum_{i=1}^{k} m_i \cdot f_i$$

**Propiedades Algebraicas y de Espacios Topológicos:**
La media aritmética dista abismalmente de ser un mero "promedio sumatoria"; las siguientes características aseguran su hegemonía paramétrica:
1. **El Teorema Fundamental de la Desviación Nula (Centroide):** El valor esperado empírico de los vectores residuales referenciados a la media es indudablemente cero, es decir: $\sum_{i=1}^n (x_i - \bar{x}) = 0$.
2. **Isomorfismo Afín (Propiedad de Linealidad):** Si sometemos el sistema a un mapeo afín de escalado y traslación $Y_i = a X_i + b$ (por ejemplo, cambio de termodinámica C° a F°, o moneda), el operador de la media experimenta un traslape analógico total y directo: $\bar{y} = a\bar{x} + b$.
3. **El Teorema de Optimización de Mínimos Cuadrados L2 (Gauss):** Analíticamente, la media aritmética es la constante $c$ real que minimiza global y estrictamente la Función de Coste Cuadrática Media (MSE) sin utilizar el cálculo diferencial local. Es decir: $\arg\min_{c \in \mathbb{R}} \sum_{i=1}^n (x_i - c)^2 = \bar{x}$.
4. **Cierre de continuidad real:** $\bar{x} \in \mathbb{R}$, pudiendo ostentar sin conflicto una magnitud fraccionaria infinita aunque su dominio de origen sea en enteros estrictamente acotados (ej: $\mathbb{Z}$), no existiendo atadura a valores propios observados $\bar{x} \notin \mathbf{x}$.

**Axiomas de Limitaciones Críticas Dogmáticas:**
- **Inestabilidad robusta catastrófica (Sensibilidad severa):** La media usa algebraicamente cada átomo de la sumatoria en un numerador. Por esto falla ante distribuciones con "colas pesadas". Su **Punto de Ruptura (*Breakdown Point* estadístico)** es de valor nulo $\rightarrow 0$. Es decir, introducir teóricamente un solo dato infinito (un anomalía extrema u outlier, e.g. el capital de Elon Musk entra en un salón escolar pautando $N+1$) corrompe instantáneamente todo el centro de gravedad llevándose a $\bar{x} \to \infty$ y destrozando cualquier inferencia representativa de la sub-población regular subyacente.
### 2.2 Media Ponderada (Espacios con métricas heterogéneas)

En sistemas físicos y estadísticos complejos, no todas las observaciones $\mathbf{x}$ poseen la misma confiabilidad analítica o importancia paramétrica. 
Dado el vector de observaciones $\mathbf{x} \in \mathbb{R}^n$ y su correspondiente vector canónico de "pesos" o masas $\mathbf{w} \in \mathbb{R}^n_{\geq 0}$ (donde $\sum w_i > 0$), la **media ponderada** proyecta un centroide donde la fuerza gravitacional de cada elemento es alterada por su escalar $w_i$.

Se define como el producto interno vectorial normalizado por la traza (suma) de pesos:
$$\bar{x}_w = \frac{\mathbf{w} \cdot \mathbf{x}}{\|\mathbf{w}\|_1} = \frac{\sum_{i=1}^{n} w_i x_i}{\sum_{i=1}^{n} w_i}$$

*Aplicabilidad empírica:* Asignación de Calificaciones Universitarias por Créditos ECTS, cálculo de retornos financieros en carteras de inversión diversificadas.

### 2.3 Media Geométrica (Operador Log-Lineal o Multiplicativo)

**Definición 2.3:** Sea $\mathbf{x} \in \mathbb{R}^n_{> 0}$ un vector de observaciones estrictamente positivas. La **Media Geométrica** ($G$ o $MG$) se define matemáticamente como la raíz enésima de la productoria total de la muestra:
$$G = \left( \prod_{i=1}^{n} x_i \right)^{\frac{1}{n}} = \sqrt[n]{x_1 \cdot x_2 \cdots x_n}$$

**Isomorfismo Aditivo-Multiplicativo:** Transformando la métrica al espacio lagrangiano o logarítmico, el operador multiplicativo $G$  actúa isométricamente como la media aritmética simple de los logaritmos empíricos:
$$\ln(G) = \frac{1}{n} \sum_{i=1}^{n} \ln(x_i)$$
*Aplicabilidad empírica:* Capitalización continua compuesta (Interés compuesto), dinámicas poblacionales en biología (donde la variabilidad escala logarítmicamente) y promedios de ratios, tasas de crecimiento y factores paramétricos adyacentes.

### 2.4 Media Armónica (Tarifas y Razones de Cambio)

**Definición 2.4:** Sea $\mathbf{x} \in \mathbb{R}^n_{> 0}$. La **Media Armónica** ($H$ o $MH$) es analíticamente el inverso multiplicativo de la media aritmética de los recíprocos de las variables crudas:
$$H = \left( \frac{1}{n} \sum_{i=1}^{n} \frac{1}{x_i} \right)^{-1} = \frac{n}{\frac{1}{x_1} + \frac{1}{x_2} + ... + \frac{1}{x_n}}$$

*Aplicabilidad empírica:* Operaciones en física elemental con magnitudes combinadas. Si un objeto viaja una distancia constante a través de fluidos iterativos a velocidades de $k$ kilómetros o resistencias, la media armónica computa estocásticamente la velocidad base empírica total sin distorsiones temporales.

### 2.5 Media Cuadrática o RMS (Raíz Media Cuadrática)

Este estadístico evalúa la "magnitud escalar agregada", siendo puramente independiente del signo estricto de las variables observadas (siendo impermune a diferencias de fase, de ahí su suprema utilización en funciones de onda y cinemática).
$$\text{RMS} = \sqrt{\frac{1}{n}\sum_{i=1}^{n} x_i^2}$$
*Aplicabilidad empírica:* Tensión eficaz en circuitos de corriente alterna, desvío o ruido intrínseco de Root-Mean-Square (RMS) y dispersión de gases (físico-química de perfiles de velocidad de Boltzmann).

### 2.6 La Media Generalizada (Teorema de la Norma de Hölder)

El genio axiomático de la matemática permite englobar a todas las medias anteriores en un metaparámetro topológico solitario conocido como **Media de Potencias** o la variante estadística de la **Norma-$L_p$** de Lebesgue y de Hölder.
Sea el vector $\mathbf{x} \in \mathbb{R}^n_{> 0}$ y $p \in \mathbb{R} \setminus \{0\}$, se define el operador general paramétrico como:
$$M_p(\mathbf{x}) = \left( \frac{1}{n} \sum_{i=1}^{n} x_i^p \right)^{1/p}$$

Las medias estandarizadas previas emergen únicamente como casos particulares del parámetro $p$ bajo el Teorema Analítico de Límites:
- Si $p \to -\infty$, entonces $M_{-\infty} = \min(\mathbf{x})$
- Si $p = -1$, entonces $M_{-1} = H$ (Media Armónica)
- Si $p \to 0$, entonces $\lim_{p \to 0} M_p = G$ (Media Geométrica derivado de la Regla de L'Hôpital)
- Si $p = 1$, entonces $M_{1} = \bar{x}$ (Media Aritmética L1)
- Si $p = 2$, entonces $M_{2} = \text{RMS}$ (Media Cuadrática)
- Si $p \to \infty$, entonces $M_{\infty} = \max(\mathbf{x})$ (Norma Suprema)

**Desigualdad Fundamental Macroscópica M-G-H (Cauchy - Hölder):** 
$$H \leq G \leq \bar{x} \leq \text{RMS}$$
*Nota:* La igualdad entre estos estadísticos ocurre sí y solo si (S.S.S) la varianza empírica muestral colapsa a $0$, implicando que obligatoriamente $x_1 = x_2 = ... = x_n$ (Muestra trivial).

### 2.7 Axiomatización: Condiciones de Cauchy para un "Promedio"

No todo operador algebraico puede autodenominarse "promedio". Para que un funcional matemático adquiera la noble conmutatividad y se defina formalmente como medida paramétrica central en $\mathbb{R}^n$, debe cumplir irrefutablemente la **Propiedad Topológica de Entrelazado de Cauchy**:
Sea $f$ un operador empírico y $x_{(1)}, x_{(n)}$ las cotas inferior y superior respectivamente, $f$ debe satisfacer:
1. **Acotamiento intrínseco estricto:** $\min(\mathbf{x}) \leq f(\mathbf{x}) \leq \max(\mathbf{x})$ (Su proyección nunca puede escapar paramétricamente de los límites tangibles muestrales).
2. **Propiedad de Identidad Absoluta (Homogeneidad central):** Si toda la matriz colapsa en la misma magnitud, i.e., $x_1 = ... = x_n = k$, entonces $f(k,k, ..., k) = k$.
3. **Equivarianza permutativa (Simetría abeliana):** Cambiar el orden de llegada en la captura del dato paramétrico es irrelevante matemáticamente $\Rightarrow f(x_1, x_2) = f(x_2, x_1)$.

### 2.8 La Mediana (Operador de Posición y Minimización $L_1$)

Mientras la media minimiza la suma de errores al cuadrado ($L_2$), el espacio topológico ofrece un funcional estadístico distinto diseñado exclusivamente para repeler valores erráticos extremos que corromperían al primero.

**Definición 2.8.1 (Mediana Empírica Muestral):**
Sea el vector estadístico de orden $\mathbf{x}_{()} = (x_{(1)}, x_{(2)}, ..., x_{(n)})^T$. La **Mediana** (Notada $Me$, $M_d$ o $\tilde{x}$) es paramétricamente el valor percentil cincuenta ($P_{50}$) que disecta al espacio muestral en dos subconjuntos de estricta igualdad cardinal. Funcionalmente se define iterando:
- Si $n$ es impar: $Me = x_{((n+1)/2)}$
- Si $n$ es par: $Me = \frac{1}{2} \left[ x_{(n/2)} + x_{(n/2 + 1)} \right]$

**Teorema de Centralidad Robusta (Optimización Absoluta de Laplace):**
La mediana se eleva como el supremo estimador robusto porque es la solución algebraica exacta y única que **minimiza la función de Desviación Absoluta Media (MAE / Norma de Manhattan o $L_1$)**:
$$\arg\min_{c \in \mathbb{R}} \sum_{i=1}^n |x_i - c| = Me$$

**Axiomas Estructurales:**
- **Inmunidad Topológica (Robustez Extrema):** Contrario a la media aritmética, la Mediana ostenta el máximo **Punto de Ruptura (*Breakdown Point*) del 50%**. Esto significa que puedes alterar maliciosamente hasta el 49.9% de los datos muestrales hacia el infinito analítico sin lograr desplazar o corromper severamente la lectura de la mediana.
- Es una medida **ordinal y posicional**, no escalar, lo que la hace matemáticamente admisible para estudiar variables con escalas Ordinales estipuladas arbitrariamente (ej. medir satisfacción: "Malo, Regular, Bueno").

### 2.9 La Mediana Geométrica (Mediana Espacial o de Fréchet)

Cuando superamos el mundo unidimensional y el dato crudo pasa a ser un punto topográfico o un vector físico $\mathbf{p}_i \in \mathbb{R}^k$ en el plano multivariado (ej: ubicaciones GPS de clientes, radares), el cálculo clásico es paralizado (dado que los vectores multidimensionales no tienen "orden" ordinal ascendente natural). Para este dominio, se define la **Mediana Geométrica o Mediana Espacial de Fréchet**.

Se parametriza rigurosamente como el vector $\mathbf{m} \in \mathbb{R}^k$ que minimiza globalmente la somatoria euclidiana completa de todas las distancias no cuadradas hacia todos los puntos muestrales $P_i$:
$$\arg\min_{\mathbf{m} \in \mathbb{R}^k} \sum_{i=1}^n \left\| \mathbf{p}_i - \mathbf{m} \right\|_2$$
*Nota de cálculo analítico:* Carece de una fórmula cerrada despejable a mano. Se aproxima típicamente por computadora mediante complejos algoritmos iterativos no lineales como el algoritmo iterativo recursivo de **Weiszfeld**.

### 2.10 La Moda (Densidad de Máxima Verosimilitud)

**Definición 2.10.1:**
A diferencia de sus homólogos que buscan un "centro de equilibrio" físico, la **Moda** ($Mo$) es el estimador diseñado para ubicar **el pico global local del espacio de probabilidad o frecuencia**.
En variables aleatorias discretas puras finitas, se define formalmente como el suceso algebraico que ostenta la cardinalidad (probabilidad) suprema dentro del muestreo:
$$Mo = \arg\max_{x \in \{x_1, ..., x_n\}} f(x)$$

**Problemática y Formalismo en Series Continuas (Datos Agrupados):**
Cuando las observaciones aleatorias son reales ($\mathbb{R}$), la probabilidad de repetir dos números con precisión nuclear infinita (ej: que dos cilindros pesen exactamente $135.0021319$ gramos) es algebraicamente nula ($P = 0$). Hablar de moda no agrupada en espectros continuos carece de rigor y sentido estocástico.
Para estos casos continuos particionados en intervalos $[c_i, c_{i+1})$, la ciencia recurre a identificar primero el intervalo o "clase modal" (el dominio $k$ con la densidad superior $f_k / a_k$). Luego computa un refinamiento geométrico linear paramétrico de intercepctos utilizando el principio de Thales (asumiendo pendiente equitativa entre barras vecinas) para ubicar matemáticamente una moda continua teórica:
$$Mo = L_i + \left( \frac{\Delta_1}{\Delta_1 + \Delta_2} \right) \cdot a_i$$
Donde $L_i$ es el cimiento de la clase modal, $a_i$ la amplitud de paso métrico del segmento, $\Delta_1$ y $\Delta_2$ son los deltas de frecuencias absolutas que separan la "barrera modal" actual respecto a su precedente ($\Delta_1 = n_i - n_{i-1}$) y subsecuente clase ($\Delta_2 = n_i - n_{i+1}$).
## 3. Operadores de Dispersión y Variabilidad (Estadísticos de Escala)

Si los operadores de Tendencia Central intentan focalizar el espacio muestral colapsándolo a un solo punto (el escalar paramétrico cero-dimensional), los **Operadores de Dispersión** capturan el nivel de *entropía o ruido* que la variable acarrea a su alrededor. Matemáticamente dimensionan cuán "alejado" está el vector real con respecto a encontrarse totalmente estático sin variación.

### 3.1 Varianza Numérica (Momento de Inercia Estadístico)

**Definición 3.1.1:** Inspirada profundamente en la Mecánica Clásica, la Varianza Poblacional ($\sigma^2$) es análoga al *Momento de Inercia Físico* de un sólido rígido. Mide el grado de dispersión térmica cuadrática promedio respecto al centroide de equilibrio ($\mu$).
$$\sigma^2 = \frac{1}{N} \sum_{i=1}^N (x_i - \mu)^2 = \mathbb{E}[(X - \mu)^2]$$

**Corrección Lineal de Bessel para Inferencias Muestrales:**
A nivel analítico, calcular la varianza de una muestra (para estimar pasivamente a la inobservable $\sigma^2$ entera) genera un **estimador estrictamente sesgado**. La muestra tiende matemáticamente a aglomerarse un poco más cerca de su propia media dictatorial $\bar{x}$ que de la lejana e invisible media poblacional real $\mu$. Por ende, la suma de los residuos al cuadrado en una muestra sufre de *sobre-optimismo en la concentración*. 
Para anular este déficit y obtener un estimador insesgado genuino, el denominador pierde un Grado de Libertad Topológico ($n-1$) conocido como la **Corrección paramétrica de Friedrich Bessel**:
$$S^2 = \frac{1}{(n - 1)} \sum_{i=1}^{n} (x_i - \bar{x})^2$$
*Teorema Paralelo de Despliegue Computacional:* Algebraicamente, se expande el binomio al cuadrado para facilitar programaciones e iteraciones asintóticas minimizando sobrecarga de CPU (Algoritmo de Welford): $S^2 = \frac{\sum x_i^2 - n\bar{x}^2}{n-1}$.

### 3.2 Desviación Estándar (o Típica)

Dado que la varianza computa medidas cuadradas (e.g. Dólares al cuadrado o Metros al cuadrado), sus unidades físicas se tornan hermenéuticamente irreales. La desviación estándar aterriza dimensionalmente y extrae la raíz resolviendo esto para devolvernos al espacio y unidad paramétrica original unidimensional:
- Muestral: $S = \sqrt{S^2}$
- Poblacional: $\sigma = \sqrt{\sigma^2}$

### 3.3 Coeficiente de Variación de Pearson (CV)

**Definición 3.3.1:** Las dispersiones absolutas ($\sigma$) están dogmáticamente atadas a la escala escalar de su variable. Ej: Una dispersión de error de $10\text{m}$ es colosal al pavimentar una vereda de $50\text{m}$, pero imperceptible midiendo distancias lunares de $384,000 \text{km}$.
El **CV** se postula como un estimador escalar puro adimensional que permite homogeneizar dos varianzas dispares frente a frente, actuando como coeficiente de ruido relativo respecto a su señal de fondo:
$$CV = \left( \frac{S}{|\bar{x}|} \right) \cdot 100\%$$
*Axioma de Homogeneidad Relativa:* Si $CV \leq 33\%$, la muestra se aprueba típicamente como métricamente "homogénea", acreditando que la $\bar{x}$ sí ostenta suficiente nivel de representación frente al ruido. 

### 3.4 Desviación Absoluta Media (MAD) y Desviación Mediana (MAD-Med)

Como las varianzas ($L_2$) y la desviación estándar amplifican cuadráticamente las distancias lejanas (penalizando los Outliers drásticamente y sesgando la balanza), surgen las formas Robustas ($L_1$), que penalizan topológicamente solo en valor absoluto perimetral puro (Norma del Taxista):
- Desviación Absoluta Media de Media: $D_{\bar{x}} = \frac{1}{n}\sum |x_i - \bar{x}|$ (Muy susceptible al sesgo de la media paramétrica subyacente).
- **Desviación Absoluta Mediana (MAD Robusta Superior):** Computa la mediana del vector residual perimetral frente a otra mediana: $MAD = \operatorname{Mediana} \left( | \mathbf{x} - \tilde{x} | \right)$. Extremadamente robusta frente a ruidos infinitos.

### 3.5 Amplitud y Pseudo-Saturaciones (Ric)

- **Amplitud Espacial Total (Rango):** Operador elemental que sustrae las fronteras tangibles: $R = \max(\mathbf{x}) - \min(\mathbf{x}) = x_{(n)} - x_{(1)}$. Total y absurdamente lábil a cualquier anomalía solitaria.
- **Rango Intercuartílico (RIC):** Al extirpar sistemáticamente el $25\%$ de colas inferiores y el $25\%$ de crestas superiores del dominio, retiene numéricamente exclusivamente la coraza y estabilidad central real:
$$RIC = Q_3 - Q_1$$

---

## 4. Aglomerantes de Posición: Cuantiles Fraccionarios 

La familia paramétrica de los **Cuantiles** son funcionales estadísticos inversos. En lugar de interrogar *¿cuál es la probabilidad inferior?*, interrogan al reverso analítico *¿qué coordenada escalar en el plano físico (X) garantiza atrapar detrás a una trinchera probabilística específica y deseada (ej. $p = 0.85$)?*

Formalmente, el cuantil de orden $p \in (0, 1)$ se define como la evaluación generalizada inversa empírica de una Función Distribución FDA:
$$Q(p) = \inf \left\{ x \in \mathbb{R} : F(x) \geq p \right\}$$
Clasificaciones Topológicas:
- **Cuartiles ($Q_k$):** Fracturan al tejido del dominio poblacional en la constante $q = 4$ fragmentos de igualdad perimetral estocástica de $25\%$ cada uno. Existen 3 funcionales intercesores: $Q_1$, $Q_2$ (Mediana) y $Q_3$.
- **Deciles ($D_k$):** Segmentan modularmente el espacio en salto constante base $10$.
- **Percentiles ($P_k$ o Céntilos):** Subdivisión atómica al $1\%$ constante, generando los $99$ interceptos de corte numérico más potentes y solicitados de toda la analítica paramétrica transversal y longitudinal de la ciencia de las mediciones biomédicas y de calidad de diseño.

*Algoritmo Discreto para datos no agrupados:* Al requerir aislar un Percentil $k-$ésimo, se acata un puntero espacial $Pos_{Pk} = \frac{k(n+1)}{100}$. Si arroja dominio fraccionario $i.d$, el estadístico asimila paramétricamente la interpolación rectilínea estricta: $P_k = x_{(i)} + d \cdot (x_{(i+1)} - x_{(i)})$.

---

## 5. Estadísticos de Forma Geométrica (Tensor Topológico de Curvatura)

### 5.1 El Vector Transversal Analítico de la Asimetría (Sesgo)

- **Asimetría Cúbica de Fisher (Momentos):** Utiliza las palancas del cálculo de momento central paramétrico del hipercubo ($M_3$):
  $$g_1 = \frac{m_3}{S^3} = \frac{\frac{1}{n}\sum (x_i - \bar{x})^3}{ \left[ \frac{1}{n} \sum (x_i - \bar{x})^2 \right]^{3/2}}$$
  Dado que los volúmenes residuales son cúbicos, **el rastro conservará algebraicamente su signo** $(+, -)$ dictando dictatoriamente hacia dónde recae la cola de estallido mayor de la distribución probabilística empírica.
- **Asimetría Empírica de Pearson (Basado en Centroides):** Demostró la heurística analítica de que, en asimetría leve a nula, el diferencial escalar de Media-Moda actúa como proxy topológico asintótico del sesgo original estocástico: $\text{As}_{\text{Pear}} \approx \frac{3(\bar{x} - Me)}{S}$ (Versión modificada).
- **Asimetría Cuartílica de Bowley (Blindaje Robusto Absoluto L1):** Descansa en cuán ladeada está la simetría paramétrica interior pura de la caja fundamental de Tukey entre cuartiles: $A_Q = \frac{(Q_3 - Me) - (Me - Q_1)}{Q_3 - Q_1}$. Métrica insensible a ruido marginal y de las más estelares en ciencia de datos moderna paramédica.

### 5.2 Topología de Apuntamiento Curtósico (Curtosis de Karl Pearson)

La curtosis paramétrica decodifica exclusivamente dos atributos estocásticos inter-amarrados: La punta piramidal atómica en torno a la media y el lastre masivo denso en la prolongación lejana infinita de las **Colas**. Se ancla usando los Momentos del hipercubo tesseract de cuarta fase ($M_4$):
$$g_2 = \left[ \frac{\frac{1}{n}\sum (x_i - \bar{x})^4}{ \left[ \frac{1}{n}\sum (x_i - \bar{x})^2 \right]^2 } \right] - 3$$
El $-3$ opera como restador central estandarizado en la ciencia (Exceso de Curtosis), diseñado para acortar como axioma de validación que una distribución Normal perfecta (Campana Gaussiana) compute exactamente al grado asintótico $g_2 = 0$ (Platillo **Mesocúrtico**).
- $g_2 > 0$: **Leptocúrtica:** Cumbre puntiaguda ultra afilada con colas gruesas monstruosas. Altísima volatilidad impredecible.
- $g_2 < 0$: **Platicúrtica:** Cumbre llana tabular y achatada, con colas finas ligeras. Alta pasividad sistémica y baja sorpresa de outliers.


## 6. Dinámica de Momentos Estadísticos (Mecánica Funcional)

En analogía directa con la física teórica y el centro de masa puntual multivariado, la estadística engloba todas las características de una distribución a través de un tensor unidimensional unificado conocido como la **Familia de Momentos**.

**Definición 6.1 (Momento empírico No Centrado o respecto al origen):**
El momento muestral de orden $r$ respecto al origen $0$ se enuncia algebraicamente como:
$$a_r = \frac{1}{n} \sum_{i=1}^n x_i^r$$
- *Propiedad:* El Momento primario ($r=1$) colapsa universalmente en la Media Aritmética L1, $a_1 = \bar{x}$. Es el centro de masa espacial del sistema.

**Definición 6.2 (Momento empírico Centrado):**
El momento de orden $r$ centralizado respecto al promedio real del balance de la distribución ($\bar{x}$) se define computando:
$$m_r = \frac{1}{n} \sum_{i=1}^n (x_i - \bar{x})^r$$
- *Propiedad:* El Momento central estático ($r=1$) da como corolario cero forzoso ($m_1 = 0$) por el Teorema del Residual de la Media.
- *Propiedad:* El Segundo Momento central ($r=2$) desemboca por definición en la **Varianza** poblacional o inercial, $m_2 = \sigma^2$.
- *Propiedad:* El Tercero ($m_3$) y Cuarto ($m_4$) erigen las formulaciones de Sesgo Cortante y Curtosis relativas abordadas en la Sec 5.

**Optimización Matemática bajo Derivadas Espaciales del Funcional de Pérdidas:**
Consideremos el operador general de sumatoria de distancias $M_2(c) = \sum_{i=1}^n (x_i - c)^2$. Al derivar infinitesimalmente dicho funcional e igualar a $0$ para buscar el hoyo de óptimo de pozo potencial global, $\frac{d M_2(c)}{dc} = -2\sum(x_i - c) = 0$, comprobaremos algebraicamente que el funcional minimizado subyacente obliga inequívocamente a que $c = \bar{x}$.
Análogamente, se demuestra vía series condicionales de sub-gradientes que el funcional de métrica absoluta (Norma $L_1$) $M_1(c) = \sum |x_i - c|$, minimiza su pozo direccional exótico exclusivamente al golpear contra la pared paramétrica central $c = \text{Me}$ (La Mediana posicional).


## 7. Estadísticos de Concentración y Entropía (Análisis de Desigualdad)

Estos algoritmos robustos nacieron en la econometría, ciencia de redes y termodinámica pura. Mientras un operador de "dispersión" clama si los datos numéricos oscilan mucho, los estimadores de **concentración** miden en qué grado una variable "masiva y limitante" (e.g. Total Mundial de Riqueza, Ancho de Banda Server, Biomasa Estocástica oceánica) es acaparada tiranamente por una minúscula élite marginal del espectro poblacional, versus estar uniforme y estocásticamente democratizada.

### 7.1 Curva Topológica de Lorenz (Mapeo Ecuánime)

Es un constructo paramétrico integral bidimensional. Si indexáramos a todos los portadores del recurso material desde el de menor valía al de mayor valía sobre el Eje de las Abscisas ($x \in [0\%, 100\%]$), y sobre el eje de las Ordenadas proyectamos la fracción matemática exacta de torta acumulada que aquellos estratos sostienen ($y \in [0\%, 100\%]$).
- **Línea de la Condición Ecuánime (Axioma de Equidad Pura $45^\circ$):** Analíticamente graficada como $y = x$. Significa que la porción inferior del $10\%$ basal de la red es textualmente dueño del $10\%$ milimétrico de los recursos circulantes disponibles.
- **Curva Sagital Empírica de Lorenz ($L$):** Función polinómica o spline convexa continua. Qué tan combada, deflactada o "aboyada hacia abajo" se rastree en la topología paramétrica frente al resguardo estricto equitativo de $y=x$, denuncia la dureza absoluta de la concentración del sistema.

### 7.2 Índice Algébrico de Corrado Gini

Es un escalar integrador: representa cristalizada y paramétricamente la métrica del área diferencial contenida entre la curva empírica local y la utopía de la recta pura. Se procesa sobre una integral de base estandarizada acotada irrefutablemente entre $[0, 1]$:
$$G = \frac{\text{Área acaparada entre la utopía Ecuánime y la Curva Lorenz } L(x)}{\text{Área Triangular Isósceles Total subyacente de la Equidad}}$$
- **Gini = 0 $\rightarrow$ Estado Entrópico Total:** Red sin energía potencial concentrada, donde cada nodo topológico del hiper-espacio matricial carga precisamente la misma constante paramétrica de peso ($S = 0$).
- **Gini = 1 $\rightarrow$ Dominancia Súbita Monopolística Singular:** Agujero negro económico. Toda absoluta e íntegra tajada matemática del bien referenciado ha sido absorbida exclusivamente por un y solo un vector hiper-dominante, dejando aridez de vector cero estricto $\to 0$ para todos los otros $N-1$ perfiles.

### 7.3 Índice Termodinámico de Henri Theil (Entropía Paramétrica)

Nació inspirado directamente e intactamente sobre la revolucionaria *Ecuación General de la Teoría de la Información* del maestro de AT&T y MIT, **Claude E. Shannon**. A diferencia de los modelos geométricos, se vale únicamente de Operadores Analíticos Logarítmicos Naturales. 
El sublime portento de los logaritmos no es baladí: ostenta la propiedad celestial del cálculo de que Theil es un parámetro estadístico **totalmente aditivo y axiomáticamente descomponible infinitas veces**. (e.g., Logramos diseccionar en paralelos independientes la entropía diferencial global Inter-Naciones, de la sumatoria de desigualdades encriptadas locales Intra-Nación sin chocar con errores algebraicos de frontera).

$$T_T = \frac{1}{n} \sum_{i=1}^n \left( \frac{x_i}{\bar{x}} \cdot \ln \left[ \frac{x_i}{\bar{x}} \right] \right) \quad \text{(Entropía Redundante Estricta Theil-T)}$$

### 7.4 Tensor Axiomático de Anthony Atkinson ($A_\epsilon$)

Atkinson interviene la neutralidad absoluta con el factor humano. Postula introducir un Tensor paramétrico externo estipulado y variable $\epsilon$ (Coeficiente normativo de **"aversión al riesgo / aversión a la hambruna material"** dictado por la ideología empírica del diseñador estadístico sociólogo o el comité bioético).

$$A_\epsilon = 1 - \left[ \frac{1}{n} \sum_{i=1}^n \left( \frac{x_i}{\bar{x}} \right)^{1-\epsilon} \right]^{\frac{1}{1-\epsilon}}$$
Donde siempre rige inexorablemente $\epsilon \in (0, \infty)$.
Conforme forzamos teóricamente el tensor a la escala del infinito $\epsilon \to \infty$, el algoritmo de Atkinson acopla un isomorfismo analítico hacia la famosa moralidad utópica del filósofo **John Rawls**: Sentencia el estatus estadístico superior de todo el sistema valorando tajante e inflexiblemente nada más a las ruinas o paupérrimas condiciones en el que vive de hecho, su nodo más atómicamente destruido, marginado, microscópico y olvidado del vector numérico general $\to \{ \mathbf{x} : \sim x_{(1)} \}$.

## 8. Extensión Analítica a Variables Complejas (Espacio $\mathbb{C}^n$) [Opcional]

### 8.1 Motivación y métrica en dominios bidimensionales
En los cimientos de la física moderna y el procesamiento de señales (eléctricas, telecomunicaciones, radar), el dato empírico no habita en la recta analítica real $\mathbb{R}$, sino que emerge intrínsecamente como una magnitud bidimensional provista de fase estocástica y asimetría acoplada. 

**Definición casual poco rigurosa:** 
Imagina que en lugar de buscar "cuál es el promedio" de estaturas (puntos amarrados en una recta numérica), intentas promediar flechas giratorias dibujadas en un mapa estelar de fuerzas vectoriales. Calcular una media estocástica compleja es equilibrar simultáneamente cientos de esas flechas para hallar el "viento vector de consenso", mientras que la dispersión (varianza) dimensiona qué tan caóticamente se disparan lejos de ese eje.

### 8.2 Formalismo Paramétrico Complejo

**Definición formal:**
Sea un vector muestral estocástico encajado $\mathbf{z} \in \mathbb{C}^n$, donde cada realización experimental adopta la forma $z_k = x_k + iy_k = r_k e^{i\theta_k}$ (donde $x_k, y_k \in \mathbb{R}$ e $i^2 = -1$).
Los operadores descriptivos experimentan la siguiente metamorfosis tensorial:

1. **La Media Aritmética Compleja (Centroide del diagrama de Argand):**
Conserva isomorfismo de operador afín lineal y se postula aditivamente en componentes ortogonales algebraicas triviales.
$$ \bar{z} = \frac{1}{n} \sum_{k=1}^n z_k = \bar{x} + i\bar{y} $$

2. **Varianza Compleja Normada (Métrica Cuadrática de Hermite):**
Advertencia axiomática: los números imaginarios crudos no pueden ser elevados al cuadrado rudimentariamente en $\mathbb{R}$ bajo la Función de Pérdida clásica (es decir, una desviación "i" al cuadrado rinde $-1$, distorsionando métricamente la matriz de covarianza real y L2). El operador analítico de dispersión se funda entonces obligatoriamente sobre el **Cuadrado Conjugado Hermítico**:
$$ S_z^2 = \frac{1}{n-1} \sum_{k=1}^{n} |z_k - \bar{z}|^2 = \frac{1}{n-1} \sum_{k=1}^{n} (z_k - \bar{z}) \overline{(z_k - \bar{z})} $$

3. **La Pseudo-Covarianza ($\tau$):**
Evalúa el remanente cuadrado sin transposición recíproca (producto no conjugado) dictando la "circularidad paramétrica ideal" posicional.
$$ \tau = \frac{1}{n-1} \sum_{k=1}^n (z_k - \bar{z})^2 $$

### 8.3 Estructuras y Ejemplos de aplicación 
- **Procesamiento de Señales Radiodifusivas (Telecomunicaciones 5G y Radares M-QAM):** Las portadoras viajan como analíticas de fasores electromagnéticos descritas estocásticamente en $\mathbb{C}$. Entender las colas de las varianzas en las constelaciones de recepción decodifica los ruidos o rebotes atmosféricos antes de aplicar Fourier.
- **Teoría Tensorial Cuántica:** Los estados vectorizados de un sistema, definen funciones de onda hermíticas multidimensionales complejas, cuya matriz varianza se traduce literalmente en la muralla limitante analítica del **Principio de Incertidumbre Limitrofe de Heisenberg** ($\sigma_{x}\sigma_{p} \ge \hbar/2$).

### 8.4 Datos Históricos Analíticos (Cronología Intelectual)
La validación axiomática de estos entes fue titánica e insultantemente ignorada por muchas potencias (siendo vilipendiados como números "Imaginarios" o invenciones desprovistas de rigor).
Fue el gran príncipe genio **Carl Friedrich Gauss**, de la mano intelectual y casi silenciada de **Caspar Wessel** a fines del siglo XVIII, quien legitimó y atornilló inquebrantablemente su uso en redes reticulares algebraicas para diagramas polares completos.
Lo maravillosamente enigmático de sus investigaciones y de la historia matemática en variables complejas es su tardía ironía: Gauss elaboró en su estudio privado estas expansiones estocásticas vectorales planas para disfrutar sus capacidades sin proveerles de materialización en este universo de la recta 1D y de forma utópica; sin atisbar que el destino de las naciones mundiales en pleno frente marítimo del Pacífico en la Segunda Guerra Mundial, terminaría siendo definido por cientos de operadores paramédicos y analistas militares programando frenéticamente y con vida dependiente las primeras computadoras mecánicas con **varianzas aleatorias espaciales bidimensionales y estocástica de espectro radar imaginario**, demostrando que ninguna matemática era más inquebrantable que aquella extraída de planos abstractos y sueños numéricos.


