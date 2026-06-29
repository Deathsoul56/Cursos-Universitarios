# Probabilidad y Estadística: Análisis de Datos e Inferencia

Este curso introduce los fundamentos de la probabilidad y la estadística matemática desde una perspectiva rigurosa, comenzando por la descripción de datos y llegando hasta la inferencia estadística y la regresión. El objetivo es construir una comprensión sólida tanto de la teoría como de su uso en contextos científicos e ingenieriles.

---
## 1. Descripción del curso

La probabilidad y la estadística proporcionan el lenguaje matemático para modelar la incertidumbre y tomar decisiones con datos. A diferencia de otras ramas de las matemáticas que parten de situaciones deterministas, aquí se estudia cómo extraer conclusiones válidas bajo variabilidad e información incompleta.

El curso se organiza en cuatro grandes bloques. Primero, se desarrollan las herramientas de la **estadística descriptiva** para resumir y visualizar datos. Luego se construye la **teoría de probabilidades** sobre bases axiomáticas, incluyendo técnicas de conteo, probabilidad condicional, variables aleatorias y distribuciones. El tercer bloque introduce la **inferencia estadística**: estimación, intervalos de confianza y pruebas de hipótesis. Finalmente, se abordan los conceptos básicos de la **estadística multivariada** y la **regresión lineal**.

A lo largo del curso se enfatiza el rigor matemático, pero también la interpretación de los resultados. Se busca que cada definición y cada teorema estén acompañados de ejemplos concretos que muestren su utilidad en situaciones reales.

---
## 2. Objetivos de aprendizaje

Al finalizar el curso, se espera que el estudiante sea capaz de:

1. Describir, resumir y visualizar conjuntos de datos univariados y bivariados.
2. Enunciar los axiomas de Kolmogorov y derivar propiedades básicas de la probabilidad.
3. Calcular probabilidades utilizando técnicas de conteo, probabilidad condicional y los teoremas de Bayes y de la probabilidad total.
4. Analizar variables aleatorias discretas y continuas, incluyendo sus distribuciones más importantes.
5. Aplicar el Teorema Central del Límite para aproximar distribuciones muestrales y enunciar la Ley de los Grandes Números.
6. Construir estimadores puntuales e intervalos de confianza para parámetros poblacionales.
7. Diseñar e interpretar pruebas de hipótesis en contextos de ingeniería y ciencias.
8. Construir y evaluar modelos de regresión lineal simple y múltiple.
9. Interpretar resultados estadísticos con precisión y criterio.
10. Utilizar software estadístico (R o Python) para analizar datos reales.

---
## 3. Prerrequisitos

### Conocimientos matemáticos

- Cálculo diferencial e integral: derivadas, integrales definidas e indefinidas, series.
- Álgebra lineal: matrices, sistemas de ecuaciones lineales, vectores.
- Lógica proposicional: conectivos lógicos, tablas de verdad, cuantificadores e implicaciones.

### Competencias computacionales

- Programación básica en Python o R.
- Manejo de archivos de datos y uso de bibliotecas científicas básicas.

### Herramientas recomendadas

- **Python:** NumPy, Pandas, Matplotlib, Seaborn, SciPy, statsmodels.
- **R:** tidyverse, ggplot2, dplyr, stats.
- **Recursos auxiliares:** GeoGebra, Jupyter Notebooks, RStudio.

---
## 4. Programa

### Módulo I. Estadística descriptiva univariada (Semanas 1–3)

- Población y muestra: definiciones formales.
- Variables cualitativas y cuantitativas; escalas de medición.
- Tipos de muestreo: aleatorio simple, estratificado, por conglomerados y sistemático.
- Tablas de frecuencias: absolutas, relativas y acumuladas.
- Representaciones gráficas: histogramas, polígonos de frecuencia, ojivas, boxplots.
- Medidas de tendencia central: media, mediana, moda.
- Medidas de posición: cuartiles, percentiles.
- Medidas de dispersión: varianza, desviación estándar, rango intercuartílico.
- Asimetría y curtosis.

### Módulo II. Teoría de probabilidades (Semanas 4–9)

- Experimentos aleatorios, espacio muestral y eventos.
- Álgebra de eventos: unión, intersección, complemento.
- Definiciones de probabilidad: clásica, frecuentista y axiomática.
- Axiomas de Kolmogorov y propiedades derivadas.
- Técnicas de conteo: permutaciones, combinaciones y principio de multiplicación.
- Probabilidad condicional e independencia de eventos.
- Teorema de la probabilidad total y teorema de Bayes.
- Variables aleatorias discretas: función de masa, valor esperado y varianza.
- Distribuciones discretas: Bernoulli, binomial, geométrica, Poisson.
- Variables aleatorias continuas: función de densidad y función de distribución.
- Distribuciones continuas: uniforme, exponencial, gamma, normal.
- Teorema Central del Límite y Ley de los Grandes Números.

### Módulo III. Inferencia estadística (Semanas 10–15)

- Estadísticos y distribuciones muestrales.
- Distribuciones $\chi^2$, $t$ de Student y $F$.
- Estimación puntual: insesgamiento, eficiencia, consistencia.
- Métodos de momentos y máxima verosimilitud.
- Estimación por intervalos: media, varianza y proporción.
- Pruebas de hipótesis: conceptos fundamentales, errores tipo I y II, valor $p$.
- Pruebas para la media, varianza y proporción.
- Comparación de dos poblaciones.
- Pruebas de bondad de ajuste e independencia.

### Módulo IV. Estadística multivariada y regresión (Semanas 16–18)

- Descripción de datos bivariados: covarianza y correlación.
- Coeficiente de correlación de Pearson y su interpretación.
- Modelo de regresión lineal simple: mínimos cuadrados ordinarios.
- Propiedades de los estimadores e inferencia sobre los coeficientes.
- Coeficiente de determinación $R^2$ y análisis de residuos.
- Introducción a la regresión lineal múltiple.

---
## 5. Bibliografía

### Textos principales

1. **Devore, J. L. & Berk, K. N.** (2012). *Modern Mathematical Statistics with Applications* (2nd ed.). Springer. [Texto guía principal: riguroso, completo y con fuerte enfoque en aplicaciones.]

2. **Devore, J. L.** (2008). *Probabilidad y Estadística para Ingeniería y Ciencias* (7th ed.). Cengage Learning. [Versión más accesible para lectura complementaria y ejemplos introductorios.]

3. **Wackerly, D. D., Mendenhall, W. & Scheaffer, R. L.** (2014). *Mathematical Statistics with Applications* (7th ed.). Cengage Learning. [Riguroso, énfasis teórico.]

4. **Ross, S. M.** (2017). *Introduction to Probability and Statistics for Engineers and Scientists* (6th ed.). Academic Press. [Enfoque en STEM.]

### Teoría de probabilidad

5. **Ross, S. M.** (2019). *A First Course in Probability* (10th ed.). Pearson. [Excelente para fundamentos.]

6. **Bertsekas, D. P. & Tsitsiklis, J. N.** (2008). *Introduction to Probability* (2nd ed.). Athena Scientific. [Riguroso con aplicaciones modernas.]

7. **Grimmett, G. & Stirzaker, D.** (2020). *Probability and Random Processes* (4th ed.). Oxford University Press. [Avanzado.]

### Inferencia estadística

8. **Casella, G. & Berger, R. L.** (2021). *Statistical Inference* (3rd ed.). Cengage Learning. [Texto estándar para teoría.]

9. **Hogg, R. V., McKean, J. W. & Craig, A. T.** (2019). *Introduction to Mathematical Statistics* (8th ed.). Pearson. [Riguroso.]

### Estadística aplicada y regresión

10. **Montgomery, D. C. & Runger, G. C.** (2018). *Applied Statistics and Probability for Engineers* (7th ed.). Wiley. [Excelente para ingeniería.]

11. **Kutner, M. H., Nachtsheim, C. J., Neter, J. & Li, W.** (2004). *Applied Linear Statistical Models* (5th ed.). McGraw-Hill. [Referencia para regresión.]

12. **James, G., Witten, D., Hastie, T. & Tibshirani, R.** (2021). *An Introduction to Statistical Learning with Applications in R* (2nd ed.). Springer. [Moderno, con R.]

### Computación estadística

13. **Verzani, J.** (2014). *Using R for Introductory Statistics* (2nd ed.). CRC Press.

14. **McKinney, W.** (2022). *Python for Data Analysis* (3rd ed.). O'Reilly. [Pandas y análisis de datos.]

15. **Bruce, P., Bruce, A. & Gedeck, P.** (2020). *Practical Statistics for Data Scientists* (2nd ed.). O'Reilly. [Moderno, R y Python.]

### Referencias avanzadas

16. **Lehmann, E. L. & Romano, J. P.** (2005). *Testing Statistical Hypotheses* (3rd ed.). Springer. [Teoría avanzada de pruebas.]

17. **Wasserman, L.** (2004). *All of Statistics: A Concise Course in Statistical Inference*. Springer. [Compacto y moderno.]

### Recursos en línea

- Khan Academy: Estadística y probabilidad.
- MIT OpenCourseWare: 18.05 Introduction to Probability and Statistics.
- StatQuest (YouTube): explicaciones visuales.
- Seeing Theory (Brown University): visualizaciones interactivas.
- OpenIntro Statistics: libro gratuito de alta calidad.

---
## 6. Conocimientos al finalizar el curso

Al terminar el curso, el estudiante habrá desarrollado las siguientes competencias centrales:

- **Estadística descriptiva:** resumir, visualizar e interpretar datos usando tablas, gráficas y medidas numéricas.
- **Fundamentos de probabilidad:** aplicar los axiomas de Kolmogorov, técnicas de conteo, probabilidad condicional y el teorema de Bayes.
- **Modelado con variables aleatorias:** calcular probabilidades, esperanzas y varianzas para distribuciones discretas y continuas.
- **Teoremas límite:** aplicar el Teorema Central del Límite para aproximar distribuciones muestrales.
- **Inferencia estadística:** construir estimadores, intervalos de confianza y pruebas de hipótesis con interpretación correcta.
- **Regresión lineal:** ajustar y evaluar modelos de regresión simple y múltiple.
- **Pensamiento estadístico crítico:** cuestionar supuestos, identificar errores comunes y comunicar resultados con rigor.

---
## 7. Conexiones interdisciplinarias

- **Ingeniería:** control de calidad, confiabilidad, diseño de experimentos y procesamiento de señales.
- **Ciencias de la computación:** machine learning, análisis de algoritmos, redes y seguridad informática.
- **Física:** mecánica estadística, física de partículas, termodinámica y óptica.
- **Biología y ciencias de la salud:** epidemiología, genética, ensayos clínicos y bioinformática.
- **Economía y finanzas:** econometría, finanzas cuantitativas, análisis de riesgo y series temporales.
- **Ciencias sociales:** diseño de encuestas, análisis electoral y psicometría.

---

**Fin de la Clase 1: Presentación del Curso**
