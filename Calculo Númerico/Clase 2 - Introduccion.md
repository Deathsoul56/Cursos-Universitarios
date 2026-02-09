# Introducción a los Métodos Numéricos

## ¿Qué son los métodos numéricos?

Los métodos numéricos constituyen técnicas mediante las cuales es posible formular problemas matemáticos de tal forma que puedan resolverse utilizando operaciones aritméticas. En otras palabras, son el puente entre las matemáticas teóricas y su aplicación práctica apoyandonos en las computadoras para los calculos repetitivos, permitiéndonos obtener soluciones aproximadas a problemas que de otra manera serían intratables.

## ¿Por qué son necesarios los métodos numéricos?

### 1. Inexistencia de soluciones analíticas cerradas

Existen numerosos problemas cuya solución analítica es muy difícil de obtener o incluso imposible de expresar en términos de funciones elementales. Por ejemplo:

$$\ln(x) = \sin(x)$$
![[ln_sin_neon.png]]
Esta ecuación trascendente no tiene solución algebraica cerrada pero sabemos por la continuidad de ambas funciones que existe una solución. No podemos despejar $x$ usando operaciones algebraicas convencionales, pero mediante métodos numéricos (como el método de Newton-Raphson o bisección) podemos aproximar sus raíces con la precisión deseada.

### 2. Soluciones en rangos específicos

No siempre es necesario conocer la solución analítica completa de un problema. En muchos casos prácticos solo requerimos valores numéricos en ciertos puntos o intervalos de tiempo. Por ejemplo, las ecuaciones de Lotka-Volterra que modelan la dinámica depredador-presa:

$$
\begin{cases}
\dfrac{dx}{dt} = \alpha \cdot x - \beta \cdot x \cdot y \\[10pt]
\dfrac{dy}{dt} = \delta \cdot x \cdot y - \gamma \cdot y
\end{cases}
$$

donde $x(t)$ representa la población de presas, $y(t)$ la de depredadores, y $\alpha, \beta, \delta, \gamma$ son parámetros del modelo. Estas ecuaciones diferenciales ordinarias no lineales rara vez tienen solución analítica, pero métodos como Runge-Kutta nos permiten simular la evolución del sistema en el tiempo.

### 3. Limitaciones de precisión computacional

Los computadores tienen memoria limitada y representan números con precisión finita, por lo que debemos trabajar con aproximaciones. Esto significa que nunca obtendremos resultados totalmente exactos:

$$\pi = 3.141592653589793...$$

En la práctica, usamos representaciones de punto flotante (como IEEE 754) que truncan o redondean los valores. Esto introduce errores de redondeo que deben ser cuidadosamente manejados en el diseño de algoritmos numéricos.

**Ejemplo de error de precisión:**

Consideremos una suma simple trabajando con precisión de 4 dígitos significativos:

$$
\begin{align*}
\text{Exacto: } &\quad 1.000 + 0.0001234 = 1.0001234 \\
\text{Con 4 dígitos: } &\quad 1.000 + 0.0001234 \approx 1.000
\end{align*}
$$

El número pequeño simplemente "desaparece" debido al redondeo. Este fenómeno es especialmente problemático en sumas con muchos términos.

Otro ejemplo ilustrativo es la cancelación catastrófica al restar números muy cercanos:

$$
\begin{align*}
a &= 3.141592653 \\
b &= 3.141591829 \\
a - b &= 0.000000824 \quad \text{(perdemos dígitos significativos)}
\end{align*}
$$

Si originalmente teníamos 10 dígitos de precisión, después de la resta solo tenemos 3 dígitos confiables. Este tipo de problemas puede acumularse y propagarse en algoritmos complejos, afectando significativamente la calidad del resultado final.

### 4. Complejidad computacional prohibitiva

Algunos problemas tienen solución analítica conocida, pero su cálculo directo requiere una cantidad de tiempo o recursos computacionales enorme. Por ejemplo, resolver un sistema lineal grande:

$$A \cdot \vec{x} = \vec{b} \qquad \text{donde } A \in \mathbb{R}^{1000 \times 1000}$$

Usar eliminación gaussiana directamente requiere $\mathcal{O}(n^3)$ operaciones, lo que para $n=1000$ significa aproximadamente mil millones de operaciones. Métodos numéricos iterativos (como Jacobi, Gauss-Seidel o gradiente conjugado) pueden ser mucho más eficientes, especialmente cuando $A$ es dispersa (tiene muchos ceros).

### 5. Problemas altamente complejos

Muchos problemas de la física e ingeniería involucran ecuaciones en derivadas parciales no lineales que describen fenómenos complejos. Por ejemplo, las ecuaciones de Navier-Stokes para fluidos incompresibles:

$$
\rho \left(\dfrac{\partial\vec{v}}{\partial t} + \vec{v} \cdot \nabla \vec{v}\right) = -\nabla P + \mu \cdot \nabla^2 \vec{v} + \vec{f}
$$

donde $\vec{v}$ es el campo de velocidad, $P$ la presión, $\rho$ la densidad, $\mu$ la viscosidad dinámica y $\vec{f}$ las fuerzas externas. Estas ecuaciones no tienen solución analítica general, y su resolución numérica (mediante elementos finitos, volúmenes finitos o diferencias finitas) es fundamental en aerodinámica, meteorología y muchas otras áreas.

### 6. Sensibilidad a condiciones iniciales (Sistemas caóticos)

Algunos sistemas presentan dependencia sensible de las condiciones iniciales, donde pequeñísimas variaciones producen resultados completamente diferentes. Este comportamiento caótico es imposible de analizar analíticamente más allá de cortos períodos de tiempo. Por ejemplo, el problema de los tres cuerpos en mecánica celeste:

$$ m_i \dfrac{d^2\vec{r}_i}{dt^2} = \sum_{j \neq i} G \dfrac{m_i m_j (\vec{r}_j - \vec{r}_i)}{|\vec{r}_j - \vec{r}_i|^3}, \quad i = 1,2,3$$

Este sistema no tiene solución analítica general (excepto casos muy especiales) y debe resolverse numéricamente. Otro ejemplo clásico es el péndulo doble, donde la ecuación de movimiento es:

$$
\begin{cases}
(m_1 + m_2)L_1\ddot{\theta}_1 + m_2L_2\ddot{\theta}_2\cos(\theta_1-\theta_2) + m_2L_2\dot{\theta}_2^2\sin(\theta_1-\theta_2) + (m_1+m_2)g\sin\theta_1 = 0 \\[8pt]
m_2L_2\ddot{\theta}_2 + m_2L_1\ddot{\theta}_1\cos(\theta_1-\theta_2) - m_2L_1\dot{\theta}_1^2\sin(\theta_1-\theta_2) + m_2g\sin\theta_2 = 0
\end{cases}
$$

Aunque las ecuaciones son deterministas, su naturaleza caótica hace que la simulación numérica sea la única herramienta práctica para estudiar su comportamiento a largo plazo.

### 7. Dominios geométricos irregulares

Cuando necesitamos resolver ecuaciones en regiones con formas complicadas o geometrías irregulares, los métodos analíticos se vuelven intratables. Por ejemplo, calcular el flujo de calor en una pieza mecánica con forma arbitraria:

$$\nabla^2 T = 0 \quad \text{en } \Omega$$

donde $\Omega$ es el dominio con geometría compleja (como el perfil de un álabe de turbina o el fuselaje de un avión). Los métodos numéricos discretizan el dominio mediante:

- **Diferencias finitas**: Requieren mallas estructuradas (rectangulares)
- **Elementos finitos**: Permiten mallas no estructuradas que se adaptan a geometrías complejas
- **Volúmenes finitos**: Útiles en problemas de conservación con geometrías arbitrarias

Esta discretización del espacio permite transformar el problema continuo en un sistema algebraico resoluble.

### 8. Optimización con múltiples variables

En problemas de optimización con muchas variables, encontrar analíticamente el máximo o mínimo mediante cálculo diferencial se vuelve impracticable. Por ejemplo, en el entrenamiento de una red neuronal con función de pérdida:

$$
\min_{\vec{w}} \mathcal{L}(\vec{w}) = \min_{\vec{w}} \sum_{i=1}^{N} \left( y_i - f(\vec{x}_i; \vec{w}) \right)^2
$$

donde $\vec{w} \in \mathbb{R}^n$ puede tener millones de parámetros. Resolver $\nabla \mathcal{L}(\vec{w}) = 0$ analíticamente es imposible, por lo que usamos métodos iterativos como:

- **Descenso del gradiente**: $\vec{w}_{k+1} = \vec{w}_k - \alpha \nabla \mathcal{L}(\vec{w}_k)$
- **Método de Newton**: Usa información de segunda derivada (Hessiana)
- **Algoritmos genéticos**: Para espacios de búsqueda discretos o no diferenciables

Otro ejemplo es la optimización de diseño en ingeniería, donde queremos minimizar el peso de una estructura sujeta a restricciones de resistencia.

### 9. Problemas inversos

En los problemas inversos conocemos el efecto y queremos determinar la causa o los parámetros del sistema. Estos problemas son típicamente mal condicionados (pequeños errores en los datos producen grandes errores en la solución) y requieren técnicas de regularización. Ejemplos importantes:

**Tomografía computarizada**: A partir de proyecciones de rayos X desde múltiples ángulos, reconstruir la imagen interna del cuerpo. Matemáticamente, esto involucra invertir la transformada de Radon:

$$g(\theta, s) = \int_{-\infty}^{\infty} f(x,y) \, dl$$

donde $g$ son las mediciones y $f$ es la densidad interna que queremos reconstruir.

**Identificación de parámetros**: En sistemas dinámicos, determinar parámetros desconocidos a partir de mediciones. Por ejemplo, estimar la permeabilidad de un yacimiento petrolero a partir de datos de presión en pozos.

Estos problemas requieren métodos numéricos especializados como mínimos cuadrados regularizados o métodos bayesianos.

### 10. Integrales sin forma cerrada

Muchas integrales fundamentales en ciencia e ingeniería no tienen antiderivada expresable mediante funciones elementales. Por ejemplo:

$$\int e^{-x^2} \, dx$$

Esta integral (relacionada con la distribución normal en estadística) no tiene forma cerrada, pero es fundamental para calcular probabilidades. Otros ejemplos importantes:

**Integral elíptica completa de primera clase**:
$$K(k) = \int_0^{\pi/2} \dfrac{d\theta}{\sqrt{1 - k^2\sin^2\theta}}$$

Aparece en el período de un péndulo simple con amplitud grande, longitud de arco de elipse, y muchos otros problemas físicos.

**Función error**:
$$\text{erf}(x) = \dfrac{2}{\sqrt{\pi}} \int_0^x e^{-t^2} \, dt$$

Esencial en teoría de probabilidad, difusión y propagación de calor.

Para evaluar estas integrales en puntos específicos, usamos métodos de integración numérica como:
- Regla del trapecio
- Regla de Simpson
- Cuadratura de Gauss

Estos métodos aproximan la integral mediante sumas ponderadas de valores de la función en puntos específicos.

## Aplicaciones de los métodos numéricos

Los métodos numéricos son ubicuos en la ciencia y la ingeniería modernas:

- **Meteorología y climatología**: Predicción del tiempo mediante modelos atmosféricos
- **Ingeniería estructural**: Análisis de tensiones y deformaciones en edificios y puentes
- **Gráficos computacionales**: Renderizado 3D, animaciones y simulaciones físicas
- **Finanzas**: Valoración de derivados financieros y análisis de riesgo
- **Medicina**: Procesamiento de imágenes médicas y simulación de sistemas biológicos
- **Inteligencia artificial**: Entrenamiento de redes neuronales mediante optimización numérica
- **Industria automotriz**: Simulación de colisiones y dinámica de vehículos
- **Exploración espacial**: Cálculo de trayectorias y optimización de misiones

## Consideraciones importantes

Al trabajar con métodos numéricos debemos tener presente:

1. **Error de truncamiento**: Error introducido al aproximar procesos infinitos (series, derivadas) por procesos finitos
2. **Error de redondeo**: Error debido a la representación finita de números en computadora
3. **Estabilidad**: Un algoritmo es estable si pequeños errores no crecen descontroladamente
4. **Convergencia**: La solución aproximada debe acercarse a la solución exacta conforme refinamos el método
5. **Eficiencia**: El balance entre precisión y costo computacional es crucial

En este curso estudiaremos diversos métodos numéricos para resolver problemas de: solución de ecuaciones no lineales, sistemas de ecuaciones lineales, interpolación y aproximación, diferenciación e integración numérica, y ecuaciones diferenciales.