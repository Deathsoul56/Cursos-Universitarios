# PROBABILIDAD Y ESTADÍSTICA: ANÁLISIS DE DATOS E INFERENCIA

## **DESCRIPCIÓN DEL CURSO**

Este curso desarrolla una comprensión profunda y rigurosa de la teoría de probabilidades y la estadística matemática, comenzando desde los fundamentos axiomáticos hasta las técnicas avanzadas de inferencia estadística y modelado. Se enfatiza tanto el rigor matemático como las aplicaciones computacionales, desarrollando habilidades esenciales para el análisis cuantitativo en ciencias, ingeniería y tecnología.

---
## **OBJETIVOS DE APRENDIZAJE**

Al finalizar el curso, los estudiantes serán capaces de:

1. **Aplicar** técnicas de estadística descriptiva para resumir y visualizar datos univariados y multivariados
2. **Comprender** los fundamentos axiomáticos de la teoría de probabilidades
3. **Calcular** probabilidades utilizando técnicas de conteo, probabilidad condicional y teoremas fundamentales
4. **Analizar** variables aleatorias discretas y continuas y sus distribuciones
5. **Aplicar** el Teorema Central del Límite y la Ley de los Grandes Números
6. **Realizar** estimación puntual y por intervalos con rigor estadístico
7. **Diseñar** y ejecutar pruebas de hipótesis apropiadas para diversos contextos
8. **Construir** modelos de regresión lineal y evaluar su validez
9. **Interpretar** resultados estadísticos en contextos científicos y de ingeniería
10. **Utilizar** software estadístico (R/Python) para análisis de datos reales

---

## **PROGRAMA DETALLADO**

### **MÓDULO I: ESTADÍSTICA DESCRIPTIVA UNIVARIADA** _(Semanas 1-3)_

#### Semana 1: Fundamentos y Recolección de Datos

- Población y muestra: definiciones formales
- Variables: cualitativas (nominales, ordinales) y cuantitativas (discretas, continuas)
- Escalas de medición: nominal, ordinal, intervalo, razón
- Tipos de estudios: observacionales vs. experimentales
- Diseño de experimentos: aleatorización, control, replicación
- Muestreo aleatorio simple, estratificado, por conglomerados, sistemático
- Sesgo de selección y sesgo de respuesta
- Organización de datos: tablas de frecuencias
- Frecuencias absolutas, relativas y acumuladas
- Representación gráfica: histogramas, polígonos de frecuencia, ojivas
- Gráficos de barras, gráficos circulares, diagramas de tallo y hoja

#### Semana 2: Medidas de Tendencia Central y Posición

- Media aritmética: propiedades y sensibilidad a valores extremos
- Mediana: definición y cálculo para datos agrupados y no agrupados
- Moda: unimodal, bimodal, multimodal
- Media geométrica y media armónica: definiciones y aplicaciones
- Relación entre media, mediana y moda en distribuciones simétricas y asimétricas
- Cuantiles, cuartiles, deciles y percentiles
- Construcción e interpretación de diagramas de caja (boxplots)
- Detección de valores atípicos (outliers) mediante el criterio IQR
- Datos agrupados: cálculo de medidas usando marcas de clase
- Propiedades de las medidas de tendencia central

#### Semana 3: Medidas de Dispersión y Forma

- Rango y rango intercuartílico (IQR)
- Desviación media, varianza y desviación estándar
- Varianza poblacional (σ²) vs. varianza muestral (s²)
- Propiedades de la varianza: linealidad y transformaciones
- Coeficiente de variación: comparación de dispersión relativa
- Puntuaciones estandarizadas (z-scores)
- Desigualdad de Chebyshev: cota para probabilidades
- Momentos de una distribución
- Asimetría (skewness): coeficiente de asimetría de Pearson y Fisher
- Curtosis: distribuciones leptocúrticas, mesocúrticas y platicúrticas
- Interpretación de la forma de distribuciones empíricas

**Taller 1:** Análisis descriptivo completo de conjuntos de datos  
**Evaluación 1:** Quiz sobre estadística descriptiva univariada

---

### **MÓDULO II: TEORÍA DE PROBABILIDADES** _(Semanas 4-9)_

#### Semana 4: Fundamentos de Probabilidad

- Experimentos aleatorios y espacio muestral
- Eventos: simples, compuestos, mutuamente excluyentes
- Álgebra de eventos: unión, intersección, complemento
- Leyes de De Morgan
- Definiciones de probabilidad:
  - Clásica (Laplace): casos favorables/casos posibles
  - Frecuentista (von Mises): límite de frecuencias relativas
  - Axiomática (Kolmogorov): axiomas fundamentales
- Axiomas de Kolmogorov y consecuencias
- Propiedades básicas de la probabilidad
- Probabilidad de eventos complementarios
- Principio de inclusión-exclusión

#### Semana 5: Técnicas de Conteo

- Principio de multiplicación y adición
- Permutaciones: con y sin repetición
- Permutaciones de n elementos tomados de r en r
- Permutaciones circulares
- Combinaciones: definición y propiedades
- Números combinatorios y triángulo de Pascal
- Identidades combinatorias fundamentales
- Teorema del binomio
- Aplicaciones a cálculo de probabilidades
- Particiones y distribuciones de objetos
- Principio del palomar (pigeonhole principle)

#### Semana 6: Probabilidad Condicional e Independencia

- Probabilidad condicional: definición y propiedades
- Regla de la multiplicación
- Independencia de eventos: definición formal
- Independencia mutua vs. independencia por pares
- Teorema de la probabilidad total (ley de probabilidad total)
- Teorema de Bayes: derivación y aplicaciones
- Interpretación bayesiana: probabilidades a priori y a posteriori
- Aplicaciones del Teorema de Bayes en diagnóstico y clasificación
- Tablas de contingencia y probabilidades conjuntas
- Árboles de probabilidad

#### Semana 7: Variables Aleatorias Discretas

- Definición formal de variable aleatoria
- Variables aleatorias discretas: función de masa de probabilidad (PMF)
- Función de distribución acumulada (CDF): propiedades
- Valor esperado (esperanza matemática): definición y propiedades
- Linealidad de la esperanza
- Varianza y desviación estándar de variables aleatorias
- Momentos de variables aleatorias
- Distribución de Bernoulli: parámetros y propiedades
- Distribución Binomial: derivación, PMF, media y varianza
- Distribución Geométrica: tiempo hasta el primer éxito
- Distribución Binomial Negativa (Pascal)
- Distribución de Poisson: derivación como límite binomial
- Proceso de Poisson y aplicaciones

#### Semana 8: Variables Aleatorias Continuas

- Variables aleatorias continuas: función de densidad de probabilidad (PDF)
- Propiedades de la PDF: no negatividad e integral unitaria
- Función de distribución acumulada para variables continuas
- Relación entre PDF y CDF: derivación e integración
- Cálculo de probabilidades mediante integración
- Valor esperado y varianza para variables continuas
- Distribución Uniforme continua: U(a,b)
- Distribución Exponencial: λ, propiedad de pérdida de memoria
- Relación entre Poisson y Exponencial
- Distribución Gamma: función Gamma y aplicaciones
- Distribución Beta: parámetros α y β
- Introducción a la Distribución Normal: μ y σ²

#### Semana 9: Distribución Normal y Teoremas Límite

- Distribución Normal: N(μ, σ²)
- Función de densidad y propiedades
- Distribución Normal Estándar: Z ~ N(0,1)
- Estandarización: transformación Z
- Uso de tablas de la distribución normal
- Cálculo de probabilidades y percentiles
- Aproximación normal a la Binomial: continuidad correcta
- Teorema de De Moivre-Laplace
- Aproximación normal a la Poisson
- Ley de los Grandes Números (Débil y Fuerte)
- Teorema Central del Límite: enunciado formal y demostración (esquema)
- Distribución de la media muestral
- Aplicaciones del TCL en la práctica
- Consecuencias del TCL para inferencia estadística

**Taller 2:** Problemas de probabilidad y distribuciones  
**Taller 3:** Simulación de distribuciones y TCL  
**Examen Parcial 1:** Estadística descriptiva y teoría de probabilidades

---

### **MÓDULO III: INFERENCIA ESTADÍSTICA** _(Semanas 10-15)_

#### Semana 10: Distribuciones Muestrales

- Muestreo aleatorio y estadísticos
- Parámetros vs. estadísticos: notación griega y latina
- Distribución muestral de un estadístico
- Distribución de la media muestral: E(X̄), Var(X̄)
- Error estándar de la media
- Distribución Chi-cuadrado (χ²): definición y propiedades
- Grados de libertad y aditividad
- Distribución de la varianza muestral
- Distribución t de Student: derivación y propiedades
- Comparación entre t y Normal estándar
- Distribución F de Fisher-Snedecor: razón de varianzas
- Relaciones entre distribuciones (Normal, χ², t, F)

#### Semana 11: Estimación Puntual

- Conceptos fundamentales: estimador vs. estimado
- Propiedades deseables de estimadores:
  - Insesgamiento (unbiasedness): E(θ̂) = θ
  - Eficiencia: mínima varianza
  - Consistencia: convergencia en probabilidad
  - Suficiencia: información completa sobre el parámetro
- Error cuadrático medio (MSE): sesgo-varianza tradeoff
- Métodos de estimación:
  - Método de momentos: igualación de momentos poblacionales y muestrales
  - Método de máxima verosimilitud (MLE)
  - Función de verosimilitud: construcción y maximización
- Propiedades asintóticas de los MLE
- Estimadores para media, varianza y proporción
- Estimadores robustos

#### Semana 12: Estimación por Intervalos I

- Concepto de intervalo de confianza
- Nivel de confianza e interpretación correcta
- Construcción de intervalos de confianza:
  - Método del pivote
  - Método general basado en distribuciones muestrales
- Intervalo de confianza para la media (μ):
  - Caso σ² conocida (distribución Normal)
  - Caso σ² desconocida (distribución t)
- Determinación del tamaño de muestra para precisión deseada
- Intervalo de confianza para la varianza (σ²) usando χ²
- Intervalo de confianza para una proporción (p):
  - Método de Wald
  - Método de Wilson (score interval)
  - Método de Agresti-Coull
- Corrección de continuidad

#### Semana 13: Estimación por Intervalos II

- Intervalos de confianza para diferencia de medias:
  - Muestras independientes con varianzas conocidas
  - Muestras independientes con varianzas iguales (pooled variance)
  - Muestras independientes con varianzas desiguales (Welch-Satterthwaite)
  - Muestras pareadas (datos dependientes)
- Intervalo de confianza para razón de varianzas (σ₁²/σ₂²) usando F
- Intervalo de confianza para diferencia de proporciones
- Interpretación de intervalos en contexto científico
- Intervalos de predicción vs. intervalos de confianza
- Introducción a métodos bootstrap para construcción de intervalos

#### Semana 14: Pruebas de Hipótesis I

- Conceptos fundamentales:
  - Hipótesis nula (H₀) e hipótesis alternativa (H₁ o Hₐ)
  - Estadístico de prueba
  - Región crítica y región de aceptación
- Tipos de error:
  - Error Tipo I (α): rechazar H₀ siendo verdadera
  - Error Tipo II (β): no rechazar H₀ siendo falsa
- Potencia de la prueba: 1 - β
- Nivel de significancia (α): valores típicos (0.05, 0.01, 0.10)
- Valor p (p-value): definición e interpretación correcta
- Metodología general para pruebas de hipótesis
- Pruebas unilaterales (cola derecha/izquierda) vs. bilaterales (dos colas)
- Prueba Z para la media (σ² conocida)
- Prueba t para la media (σ² desconocida)
- Relación entre intervalos de confianza y pruebas de hipótesis
- Prueba para la varianza usando χ²
- Prueba Z para una proporción

#### Semana 15: Pruebas de Hipótesis II

- Prueba t para comparación de dos medias:
  - Muestras independientes (pooled y Welch)
  - Muestras pareadas
- Supuestos de las pruebas paramétricas: normalidad, homocedasticidad
- Prueba F para igualdad de varianzas (Levene test como alternativa)
- Prueba Z para diferencia de proporciones
- Introducción a pruebas no paramétricas:
  - Prueba de Wilcoxon de rangos con signo
  - Prueba U de Mann-Whitney
  - Prueba de Kruskal-Wallis
  - Prueba de signos
- Pruebas de bondad de ajuste:
  - Prueba Chi-cuadrado para bondad de ajuste
  - Prueba de Kolmogorov-Smirnov
- Prueba Chi-cuadrado de independencia en tablas de contingencia
- Consideraciones sobre múltiples comparaciones (Bonferroni, FDR)
- Tamaño del efecto: d de Cohen, r de Pearson

**Taller 4:** Estimación puntual y por intervalos  
**Taller 5:** Diseño y ejecución de pruebas de hipótesis  
**Examen Parcial 2:** Inferencia estadística

---

### **MÓDULO IV: ESTADÍSTICA MULTIVARIADA Y REGRESIÓN** _(Semanas 16-18)_

#### Semana 16: Estadística Descriptiva Bivariada

- Datos bivariados: pares (x, y)
- Diagramas de dispersión (scatter plots)
- Covarianza: definición y propiedades
- Cov(X,Y) = E[(X - μₓ)(Y - μᵧ)]
- Covarianza muestral
- Interpretación: asociación lineal entre variables
- Coeficiente de correlación lineal de Pearson:
  - Definición: ρ = Cov(X,Y)/(σₓσᵧ)
  - Propiedades: -1 ≤ ρ ≤ 1
  - Correlación vs. causalidad
- Coeficiente de correlación muestral (r)
- Prueba de significancia para correlación
- Correlación espuria y variables confusoras
- Transformaciones para linealizar relaciones
- Coeficientes de correlación no paramétricos:
  - Correlación de Spearman (rangos)
  - Tau de Kendall
- Correlaciones parciales
- Matrices de correlación para múltiples variables

#### Semana 17: Regresión Lineal Simple

- Modelo de regresión lineal simple: Y = β₀ + β₁X + ε
- Supuestos del modelo:
  - Linealidad
  - Independencia de errores
  - Homocedasticidad: Var(ε) = σ² constante
  - Normalidad de errores: ε ~ N(0, σ²)
- Método de mínimos cuadrados ordinarios (OLS)
- Derivación de estimadores β̂₀ y β̂₁
- Propiedades de los estimadores: insesgamiento, normalidad
- Recta de regresión: ŷ = β̂₀ + β̂₁x
- Interpretación de parámetros: pendiente e intercepto
- Residuos: e = y - ŷ
- Suma de cuadrados: SST, SSR, SSE
- Descomposición de la variabilidad: SST = SSR + SSE
- Coeficiente de determinación: R² = SSR/SST
- R² ajustado
- Error estándar de la regresión (s)
- Inferencia sobre los coeficientes:
  - Intervalos de confianza para β₀ y β₁
  - Prueba t para significancia de β₁
- Análisis de varianza (ANOVA) para regresión
- Prueba F global del modelo
- Intervalos de confianza para la respuesta media
- Intervalos de predicción para valores individuales

#### Semana 18: Diagnóstico de Regresión y Regresión Múltiple

**Diagnóstico del Modelo de Regresión:**
- Análisis de residuos:
  - Gráficos de residuos vs. valores ajustados
  - Gráfico Q-Q (quantile-quantile) para normalidad
  - Gráfico de residuos vs. orden temporal (autocorrelación)
- Detección de valores influyentes:
  - Leverage (apalancamiento)
  - Distancia de Cook
  - DFFITs y DFBETAs
- Pruebas formales de supuestos:
  - Prueba de Shapiro-Wilk para normalidad
  - Prueba de Breusch-Pagan para homocedasticidad
  - Prueba de Durbin-Watson para autocorrelación
- Transformaciones para corregir violaciones de supuestos
- Multicolinealidad: detección y tratamiento

**Introducción a Regresión Lineal Múltiple:**
- Modelo: Y = β₀ + β₁X₁ + β₂X₂ + ... + βₖXₖ + ε
- Notación matricial: Y = Xβ + ε
- Estimación por mínimos cuadrados: β̂ = (X'X)⁻¹X'Y
- Interpretación de coeficientes: efectos parciales
- R² y R² ajustado en regresión múltiple
- Prueba F global y pruebas t individuales
- Selección de variables:
  - Backward elimination
  - Forward selection
  - Stepwise regression
- Criterios de información: AIC, BIC
- Variables indicadoras (dummies) para variables categóricas
- Términos de interacción

**Taller 6:** Análisis de regresión y diagnóstico completo  
**Evaluación 3:** Proyecto final de análisis de datos

---

## **HERRAMIENTAS COMPUTACIONALES**

### **Software Estadístico (Obligatorio)**

El curso requiere el uso de **R** o **Python** para todos los análisis:

#### **R / RStudio**
- Instalación de R (CRAN) y RStudio
- Paquetes esenciales: `tidyverse`, `ggplot2`, `dplyr`, `readr`
- Paquetes estadísticos: `stats`, `MASS`, `car`, `lmtest`
- Generación de reportes con R Markdown

#### **Python**
- Distribución Anaconda recomendada
- Librerías esenciales:
  - `NumPy`: operaciones numéricas
  - `Pandas`: manipulación de datos
  - `Matplotlib` / `Seaborn`: visualización
  - `SciPy`: funciones estadísticas
  - `statsmodels`: modelos estadísticos y regresión
  - `scikit-learn`: machine learning y análisis
- Jupyter Notebooks para análisis interactivo

### **Recursos Adicionales**

- **Excel/Google Sheets:** para cálculos básicos y enseñanza de conceptos
- **GeoGebra:** visualización de distribuciones de probabilidad
- **StatKey / Rossman-Chance Applets:** simulaciones interactivas
- **Online calculators:** VassarStats, GraphPad

---

## **BIBLIOGRAFÍA**

### **Textos Principales**

1. **Wackerly, D.D., Mendenhall, W. & Scheaffer, R.L.** (2014). _Mathematical Statistics with Applications_ (7th ed.). Cengage Learning. [Riguroso, énfasis teórico]

2. **Devore, J.L.** (2015). _Probability and Statistics for Engineering and the Sciences_ (9th ed.). Cengage Learning. [Balance teoría-aplicaciones]

3. **Ross, S.M.** (2017). _Introduction to Probability and Statistics for Engineers and Scientists_ (6th ed.). Academic Press. [Enfoque en STEM]

### **Teoría de Probabilidad**

4. **Ross, S.M.** (2019). _A First Course in Probability_ (10th ed.). Pearson. [Excelente para fundamentos]

5. **Bertsekas, D.P. & Tsitsiklis, J.N.** (2008). _Introduction to Probability_ (2nd ed.). Athena Scientific. [Riguroso con aplicaciones modernas]

6. **Grimmett, G. & Stirzaker, D.** (2020). _Probability and Random Processes_ (4th ed.). Oxford University Press. [Avanzado]

### **Inferencia Estadística**

7. **Casella, G. & Berger, R.L.** (2021). _Statistical Inference_ (3rd ed.). Cengage Learning. [Texto estándar para teoría]

8. **Hogg, R.V., McKean, J.W. & Craig, A.T.** (2019). _Introduction to Mathematical Statistics_ (8th ed.). Pearson. [Riguroso]

### **Estadística Aplicada y Regresión**

9. **Montgomery, D.C. & Runger, G.C.** (2018). _Applied Statistics and Probability for Engineers_ (7th ed.). Wiley. [Excelente para ingeniería]

10. **Kutner, M.H., Nachtsheim, C.J., Neter, J. & Li, W.** (2004). _Applied Linear Statistical Models_ (5th ed.). McGraw-Hill. [Referencia para regresión]

11. **James, G., Witten, D., Hastie, T. & Tibshirani, R.** (2021). _An Introduction to Statistical Learning with Applications in R_ (2nd ed.). Springer. [Moderno, con R]

### **Computación Estadística**

12. **Verzani, J.** (2014). _Using R for Introductory Statistics_ (2nd ed.). CRC Press.

13. **McKinney, W.** (2022). _Python for Data Analysis_ (3rd ed.). O'Reilly. [Pandas y análisis de datos]

14. **Bruce, P., Bruce, A. & Gedeck, P.** (2020). _Practical Statistics for Data Scientists_ (2nd ed.). O'Reilly. [Moderno, R y Python]

### **Referencias Avanzadas**

15. **Lehmann, E.L. & Romano, J.P.** (2005). _Testing Statistical Hypotheses_ (3rd ed.). Springer. [Teoría avanzada de pruebas]

16. **Wasserman, L.** (2004). _All of Statistics: A Concise Course in Statistical Inference_. Springer. [Compacto y moderno]

### **Recursos en Línea**

- **Khan Academy:** Estadística y probabilidad
- **MIT OpenCourseWare:** 18.05 Introduction to Probability and Statistics
- **Coursera:** Cursos de estadística de Duke, Stanford
- **StatQuest (YouTube):** Explicaciones visuales excelentes
- **Seeing Theory (Brown University):** Visualizaciones interactivas
- **OpenIntro Statistics:** Libro gratuito de alta calidad

---

## **EVALUACIÓN**

### **Distribución de Calificaciones**

| Componente | Porcentaje |
|------------|-----------|
| Examen Parcial 1 (Módulos I-II) | 25% |
| Examen Parcial 2 (Módulo III) | 25% |
| Proyecto Final (Módulo IV) | 20% |
| Talleres (6 talleres) | 15% |
| Quizzes (3 quizzes) | 10% |
| Tareas computacionales | 5% |
| **TOTAL** | **100%** |

### **Descripción de Evaluaciones**

**Exámenes Parciales:**
- Problemas teóricos que requieren demostraciones
- Ejercicios de aplicación y cálculo
- Interpretación de resultados
- Tiempo: 2 horas

**Proyecto Final:**
- Análisis completo de un conjunto de datos real
- Estadística descriptiva, inferencia y regresión
- Reporte técnico escrito (formato científico)
- Código documentado (R o Python)
- Presentación oral (10-15 minutos)

**Talleres:**
- Problemas prácticos para resolver en grupos pequeños
- Énfasis en aplicaciones computacionales
- Entrega semanal

**Quizzes:**
- Evaluaciones cortas (30 minutos)
- Conceptos fundamentales y definiciones
- Sin previo aviso (posiblemente)

---

## **APLICACIONES INTERDISCIPLINARIAS**

### **Ingeniería**

- **Control de Calidad:** gráficos de control, Six Sigma
- **Confiabilidad:** análisis de fallas y tiempos de vida
- **Diseño de Experimentos:** factorial designs, optimización
- **Procesamiento de Señales:** análisis espectral, filtrado
- **Ingeniería de Software:** testing, análisis de bugs

### **Ciencias de la Computación**

- **Machine Learning:** fundamentos probabilísticos
- **Análisis de Algoritmos:** complejidad esperada
- **Redes y Comunicaciones:** teoría de colas, throughput
- **Seguridad:** criptografía, análisis de riesgos
- **Big Data:** muestreo, estimación en datasets masivos

### **Física**

- **Mecánica Estadística:** distribuciones de Maxwell-Boltzmann
- **Física de Partículas:** análisis de experimentos, detección de señales
- **Termodinámica:** entropía e incertidumbre
- **Óptica:** ruido en mediciones
- **Física Experimental:** propagación de errores, ajuste de curvas

### **Biología y Ciencias de la Salud**

- **Epidemiología:** tasas, riesgos relativos, odds ratios
- **Genética:** análisis de ligamiento, GWAS
- **Ensayos Clínicos:** diseño, análisis de eficacia y seguridad
- **Ecología:** modelos poblacionales, biodiversidad
- **Bioinformática:** análisis de secuencias, expresión génica

### **Economía y Finanzas**

- **Econometría:** modelos de regresión para datos económicos
- **Finanzas Cuantitativas:** modelos de riesgo, teoría de portafolio
- **Análisis de Series Temporales:** predicción económica
- **Ciencias Actuariales:** seguros, pensiones, cálculo de primas
- **Análisis de Mercado:** A/B testing, segmentación

### **Ciencias Sociales**

- **Psicología:** diseño de experimentos, análisis de encuestas
- **Sociología:** muestreo de poblaciones, análisis de surveys
- **Educación:** análisis de resultados de aprendizaje
- **Ciencias Políticas:** encuestas de opinión, análisis electoral

---

## **PROBLEMAS TIPO Y EJEMPLOS**

### **Estadística Descriptiva**

**Problema 1:** Dada la siguiente muestra de tiempos de vida (en horas) de 15 componentes electrónicos: 1250, 1340, 1420, 1150, 1380, 1290, 1500, 1100, 1360, 1410, 1320, 1280, 1450, 1390, 1180

a) Calcular media, mediana, desviación estándar y coeficiente de variación  
b) Determinar cuartiles y construir boxplot  
c) Identificar valores atípicos usando el criterio IQR  
d) Calcular e interpretar el coeficiente de asimetría

### **Probabilidad**

**Problema 2:** En un lote de 20 circuitos integrados, 5 son defectuosos. Se seleccionan 4 circuitos al azar sin reemplazo.

a) ¿Cuál es la probabilidad de que exactamente 2 sean defectuosos?  
b) ¿Cuál es la probabilidad de que al menos uno sea defectuoso?  
c) Si el primer circuito seleccionado es defectuoso, ¿cuál es la probabilidad de que el segundo también lo sea?

**Problema 3:** El tiempo entre llegadas de paquetes a un router sigue una distribución exponencial con media de 0.5 segundos.

a) ¿Cuál es la probabilidad de que transcurran más de 1 segundo entre dos llegadas consecutivas?  
b) Si ya han pasado 0.8 segundos desde la última llegada, ¿cuál es la probabilidad de que pasen al menos 0.3 segundos más? (propiedad de pérdida de memoria)

**Problema 4:** Demuestre que si X ~ Poisson(λ), entonces E(X) = Var(X) = λ.

### **Distribuciones y TCL**

**Problema 5:** Los puntajes en un examen tienen distribución N(75, 100). 

a) ¿Qué porcentaje de estudiantes obtienen puntajes entre 65 y 85?  
b) ¿Cuál debe ser el puntaje mínimo para estar en el 10% superior?  
c) Si se seleccionan 25 estudiantes al azar, ¿cuál es la probabilidad de que su promedio exceda 78?

**Problema 6:** Una máquina produce componentes con probabilidad de defecto p = 0.02. En una muestra de n = 200 componentes:

a) Usando la aproximación normal, calcule P(X ≤ 5) donde X es el número de defectuosos  
b) Justifique la validez de la aproximación normal  
c) Compare con el resultado exacto usando la distribución binomial

### **Inferencia**

**Problema 7:** Se desea estimar la resistencia promedio de un nuevo material. Una muestra de n = 16 especímenes da x̄ = 520 MPa y s = 25 MPa. Asumiendo normalidad:

a) Construya un intervalo de confianza del 95% para μ  
b) ¿Qué tamaño de muestra se necesita para un margen de error de 5 MPa con 99% de confianza?  
c) Pruebe H₀: μ = 500 vs. H₁: μ > 500 con α = 0.05. Interprete el resultado.

**Problema 8:** Dos métodos de manufactura (A y B) se comparan. Método A: n₁ = 20, x̄₁ = 42.5, s₁ = 3.2. Método B: n₂ = 25, x̄₂ = 45.1, s₂ = 2.8.

a) Pruebe si las varianzas son iguales (α = 0.10)  
b) Construya un IC del 95% para μ₁ - μ₂  
c) ¿Hay evidencia de diferencia entre los métodos? (α = 0.05)

### **Regresión**

**Problema 9:** Se estudia la relación entre temperatura (X, °C) y consumo eléctrico (Y, kWh). Datos de 12 días dan:
- Σx = 300, Σy = 480, Σx² = 7800, Σy² = 19600, Σxy = 12500

a) Calcular el coeficiente de correlación r  
b) Obtener la ecuación de regresión ŷ = β̂₀ + β̂₁x  
c) Interpretar β̂₁ en contexto  
d) Calcular R² e interpretar  
e) Predecir el consumo cuando la temperatura es 28°C  
f) Realizar la prueba H₀: β₁ = 0 vs. H₁: β₁ ≠ 0 con α = 0.05

**Problema 10:** En un análisis de regresión con n = 50, se obtiene R² = 0.76, SSE = 1200.

a) Calcule SST y SSR  
b) Pruebe la significancia global del modelo con α = 0.01  
c) Calcule e interprete el error estándar de la regresión

---

## **ESTRUCTURA DE CLASES**

Cada sesión de clase (semana) incluirá:

1. **Teoría (60 min):** 
   - Derivaciones formales y demostraciones
   - Teoremas fundamentales con pruebas
   - Conceptos y definiciones rigurosas

2. **Ejemplos (30 min):**
   - Aplicación de conceptos a problemas concretos
   - Cálculos detallados paso a paso
   - Interpretación de resultados

3. **Computación (30 min):**
   - Implementación en R o Python
   - Simulaciones y visualizaciones
   - Análisis de datos reales

4. **Discusión (15 min):**
   - Conexiones interdisciplinarias
   - Intuición estadística
   - Errores comunes y cuidados

---

## **PRERREQUISITOS**

### **Conocimientos Matemáticos**

- **Cálculo Diferencial e Integral:** derivadas, integrales, series
- **Álgebra Lineal:** matrices, sistemas lineales, valores propios
- **Fundamentos de Lógica:** demostraciones matemáticas

### **Competencias Computacionales**

- Programación básica (preferiblemente Python o R)
- Manipulación de archivos de datos
- Uso de software científico/estadístico

### **Habilidades Deseables**

- Pensamiento analítico y abstracción
- Capacidad para interpretar resultados cuantitativos
- Curiosidad científica y rigor metodológico

---

## **CONSEJOS PARA EL ÉXITO**

1. **Práctica constante:** La estadística se aprende haciendo problemas, no solo leyendo
2. **No memorice fórmulas sin entender:** Comprenda de dónde vienen
3. **Use software desde el inicio:** Familiarícese con R o Python temprano
4. **Interprete siempre:** Los números sin contexto no tienen significado
5. **Trabaje en grupo:** Discutir problemas mejora la comprensión
6. **Consulte múltiples fuentes:** Diferentes autores dan diferentes perspectivas
7. **Verifique supuestos:** Las técnicas estadísticas tienen condiciones de validez
8. **Visualice los datos:** Los gráficos revelan patrones que los números ocultan
9. **Lea artículos científicos:** Vea cómo se usa estadística en su disciplina
10. **Cuestione resultados:** Desarrolle pensamiento crítico sobre análisis estadísticos

---

## **INTEGRIDAD ACADÉMICA**

- Se espera trabajo original en todas las evaluaciones individuales
- La colaboración en talleres es permitida y fomentada
- El plagio y la copia serán sancionados según reglamento universitario
- Cite apropiadamente fuentes externas en el proyecto final
- El uso de IA (ChatGPT, etc.) debe ser declarado y supervisado

---

## **RECURSOS DE APOYO**

- **Horas de oficina:** [Por definir según horario del profesor]
- **Tutorías:** [Disponibilidad de tutores o ayudantes]
- **Foro en línea:** Para discusión de problemas y dudas
- **Repositorio de código:** Ejemplos y plantillas en GitHub
- **Videos complementarios:** Enlaces a material audiovisual

---

**¡Bienvenidos al fascinante mundo de la probabilidad y la estadística!**

_Este curso te proporcionará las herramientas matemáticas y computacionales para tomar decisiones bajo incertidumbre, analizar datos científicos y contribuir al avance del conocimiento en tu área STEM._
