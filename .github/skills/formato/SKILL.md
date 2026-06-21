---
description: >
  Formato y estilo para cursos universitarios STEM de alto rigor académico.
  Aplica SIEMPRE cuando el usuario trabaja en este proyecto de Cursos-Universitarios:
  redactar definiciones, explicar conceptos, crear apuntes, estructurar secciones,
  agregar ejemplos, demostraciones o contexto histórico en cursos de matemáticas,
  física, ingeniería o ciencias formales. WHEN: crear apuntes universitarios,
  redactar definición matemática, agregar contexto histórico, estructurar clase
  STEM, curso universitario, Calculo, Algebra, escribir nueva sección, nuevo concepto,
  nueva definición, nuevo teorema, nuevo ejemplo, Calculo 1, Calculo II, Álgebra,
  Probabilidad, Estadística, Ciencia de los Materiales, Cálculo Numérico.
---
# SKILL: Cursos Universitarios STEM — Formato Estándar

## Objetivo

Producir material académico universitario de alta calidad siguiendo el formato
ya establecido en el proyecto. El contenido debe ser **formalmente correcto**,
**pedagógicamente sólido** y **accesible sin sacrificar rigor**.

**Espíritu del proyecto:** Estos apuntes no son un libro de texto. Son los apuntes
de un estudiante brillante que entiende el material en profundidad y sabe explicarlo.
El lector debe poder seguir la idea antes de ver la definición, y debe saber para qué
sirve el objeto antes de olvidarlo. El pipeline canónico es:

```
motivación casual → definición formal → ejemplos → aplicaciones
```

Las primeras cinco capas son el núcleo del pipeline. La sección de aplicaciones es
opcional: se incluye cuando enriquece la comprensión; se omite cuando no aporta
valor adicional o cuando sobrecargaría la sección.

---

## Estructura de una clase completa

Una vez que la clase está **completamente redactada**, debe incluirse un **resumen ejecutivo**
breve justo debajo del título principal `# Título de la clase`. Este párrafo describe en
una o dos oraciones qué se estudiará en la clase y cuáles son los objetivos centrales.

**Reglas:**

- El resumen ejecutivo se escribe **al final**, cuando toda la clase está lista.
- No debe anticipar secciones que aún no existen ni prometer contenido que no se cubrirá.
- Debe ser conciso y servir como guía de lectura.

**Ejemplo:**

```markdown
# Funciones Parte 2

En esta clase profundizaremos en el análisis de funciones, estableciendo definiciones
formales para las transformaciones geométricas, la clasificación según simetría (paridad),
la composición de funciones, y el estudio riguroso de la inyectividad, sobreyectividad
y funciones inversas.
```

---

## Estructura de una sección

Cada sección principal usa el encabezado `## N. Título` y sus subsecciones
`### N.M Nombre del concepto`. Dentro de cada subsección el orden es:

```
1. Motivación casual                     ← OBLIGATORIO
2. Contexto histórico                    ← RECOMENDADO
3. Definición(es) formal(es)             ← OBLIGATORIO si hay objeto nuevo
4. Teoremas / Proposiciones              ← según corresponda
5. Ejemplos                              ← OBLIGATORIO al menos uno
6. Aplicaciones                          ← OPCIONAL
7. Observaciones / Notas                 ← según corresponda
```

---

## 1. Introducción casual (motivación)

**Propósito:** Que el estudiante entienda *qué* es el objeto y *para qué sirve*
antes de ver la definición formal.

**Formato:** Párrafo(s) de texto libre, sin etiqueta especial. Máximo 2–3 párrafos.

**Patrones de escritura usados en el proyecto:**

- "Pensemos en un/una..."
- "Imaginemos..."
- "La idea principal es..."
- Descripción directa de la motivación geométrica o física

**Ejemplo real del proyecto:**

```markdown
Pensemos en un cuadrado de lados iguales a 1 unidad: si trazamos una diagonal
obtendremos un triángulo rectángulo con ambos catetos iguales a 1...
```

**Reglas:**

- No usar jerga técnica que aún no haya sido definida en el texto
- No escribir "es obvio que", "claramente", "trivialmente"
- No poner etiqueta `**Idea intuitiva:**` — el párrafo habla por sí solo

---

## 2. Contexto histórico (RECOMENDADO)

La ciencia se entiende mejor en su contexto. El contexto histórico no es ornamento:
revela por qué el concepto existe, qué problema urgía resolver, y por qué la definición
tiene la forma que tiene. Se incluye por defecto; se omite solo cuando no hay nada
relevante que decir.

**Formato — dos variantes según la relevancia:**

**Variante A — integrado en la introducción** (cuando es breve y natural):

```markdown
Esta noción, propuesta por Georg Cantor en 1874, es la base de toda la
matemática moderna.
```

**Variante B — bloque separado** (cuando merece atención propia):

```markdown
> **Nota histórica:** En los *Elementos* (c. 300 a.C.), Euclides estableció
> los fundamentos de la geometría mediante cinco postulados básicos.
```

**Cuándo omitirlo:**

- El concepto es puramente notacional o auxiliar (un símbolo de conveniencia, un lema interno)
- La historia no aporta comprensión adicional al concepto en cuestión
- El origen es contemporáneo y no hay controversia ni desarrollo significativo que contar

---

## 3. Definiciones

**Formato estándar:**

```markdown
**Definición N.M (Nombre del concepto):**
$$\text{expresión formal}$$
donde $a$ es [descripción] y $b$ es [descripción], con $a \in \text{dominio}$.
```

**Reglas:**

- Numeración correlativa dentro de la sección: `Definición 1.1`, `Definición 1.2`, etc.
- Siempre especificar el dominio y condiciones de validez
- Si la definición es corta, puede ir inline (sin bloque `$$`):
  `**Definición 1.1 (Conjunto vacío):** El conjunto vacío, denotado $\emptyset$, es...`
- Usar `$\forall$`, `$\exists$`, `$\in$`, `$\notin$` para cuantificadores
- Usar `\text{}` para palabras dentro de expresiones matemáticas

**Variantes de objetos matemáticos y su formato:**

| Objeto       | Etiqueta                           |
| ------------ | ---------------------------------- |
| Definición  | `**Definición N.M (Nombre):**`  |
| Teorema      | `**Teorema N.M (Nombre):**`      |
| Proposición | `**Proposición N.M (Nombre):**` |
| Lema         | `**Lema N.M (Nombre):**`         |
| Corolario    | `**Corolario N.M (Nombre):**`    |
| Postulado    | `**Postulado N:** texto`         |

---

## 4. Demostraciones

**Formato:**

```markdown
**Demostración:**
[texto explicativo del enfoque]
$$\text{paso algebraico}$$
[texto]
$$\text{paso siguiente}$$
[conclusión]
$\blacksquare$
```

**Reglas:**

- Toda demostración termina con `$\blacksquare$`
- Si la demostración es larga o requiere herramientas no vistas aún, indicarlo:
  ```markdown
  **Demostración:** Se demostrará en la Sección N.M cuando se introduzca [concepto].
  ```
- **NO omitir una demostración alegando que es "trivial" o "se deja como ejercicio para el lector".** Si un resultado no se prueba en la clase actual, debe diferirse con referencia explícita a la sección o curso donde se demostrará.
- Si la demostración es una "idea intuitiva" (no totalmente rigurosa), indicarlo:
  ```markdown
  **Demostración (idea intuitiva):**
  ...
  $\square$
  ```

  Usar `$\square$` (cuadrado vacío) para demos no totalmente rigurosas,
  `$\blacksquare$` para demos completas y rigurosas.

---

## 5. Ejemplos

**Formato:**

```markdown
**Ejemplo N.M:**
[enunciado del ejemplo]
$$\text{desarrollo}$$
[interpretación o resultado]
```

**Reglas:**

- Al menos un ejemplo por definición o teorema importante
- Numeración correlativa: `Ejemplo 1.1`, `Ejemplo 1.2`, etc.
- Preferir ejemplos que muestren el caso general **y** los casos límite
- Para soluciones multi-paso usar alineación:
  ```markdown
  $$\begin{align}
  f(x) &= \text{paso 1} \\
       &= \text{paso 2} \\
       &= \text{resultado}
  \end{align}$$
  ```

---

## 6. Aplicaciones

**Propósito:** Conectar el objeto formal recién definido con contextos donde aparece
de manera concreta: otras ramas de la matemática, física, ingeniería, computación, economía, etc.
Esta sección responde la pregunta implícita del estudiante: *¿y esto para qué sirve?*

**Cuándo incluirla:**

Se incluye cuando el concepto tiene conexiones relevantes con otras áreas y la sección
se beneficia de ese contexto. Se omite cuando no aporta comprensión adicional, cuando
agregar aplicaciones sobrecargaría el tema, o cuando el objeto es puramente auxiliar
(una notación interna, un lema que solo sirve para probar otro resultado).

**Formato:**

Párrafo(s) de texto, o lista cuando hay múltiples aplicaciones independientes.
No es necesario desarrollar en profundidad cada aplicación — basta con indicar
el contexto y por qué el objeto es útil allí.

```markdown
**Aplicaciones:**

Este concepto aparece de forma central en [área 1]: [descripción breve].
En [área 2], se utiliza para [descripción breve].

- **[Área 1]:** descripción concisa del uso.
- **[Área 2]:** descripción concisa del uso.
- **[Área 3]:** descripción concisa del uso.
```

**Ejemplos de aplicaciones bien escritas:**

```markdown
**Aplicaciones:**

La fórmula de la distancia euclidiana es la base del análisis de datos y aprendizaje
automático: la mayoría de los algoritmos de clasificación y agrupamiento miden
"similitud" precisamente como distancia en $\mathbb{R}^n$. En física, describe la
separación real entre dos puntos en el espacio tridimensional y es el punto de partida
para definir trabajo, campo eléctrico y potencial gravitacional.
```

```markdown
**Aplicaciones:**

- **Cálculo diferencial:** la continuidad es condición necesaria para la
  diferenciabilidad; toda función derivable es continua.
- **Análisis numérico:** los métodos de aproximación (bisección, Newton-Raphson)
  exigen continuidad para garantizar la existencia de raíces.
- **Ingeniería de control:** la respuesta de un sistema físico modelada por una
  función continua garantiza ausencia de saltos bruscos en la señal de salida.
```

---

## 7. Observaciones y Notas

**Observación** — para aclaraciones técnicas, extensiones o conexiones con otros temas:

```markdown
> **Observación:** texto de la observación.
```

**Observación importante** — cuando la distinción es crítica para no cometer errores:

```markdown
> **Observación importante:** texto.
```

**Nota** — para aclaraciones metodológicas, de notación o advertencias:

```markdown
> **Nota:** texto de la nota.
```

**Advertencia** — cuando hay un error común que el estudiante debe evitar:

```markdown
> **Advertencia:** No confundir $\emptyset$ con $\{\emptyset\}$...
```

---

## Convenciones de formato general

### Encabezados

```markdown
## N. Título de sección principal
### N.M Nombre del concepto
#### N.M.K Subcategoría (usar con moderación)
```

### Separadores

- Usar `---` **solo** cuando se cambia de sección grande o principal (encabezados `## N.`, por ejemplo, al pasar de la sección 4 a la 5).
- Cuando se cambia entre subsecciones de la misma sección padre (por ejemplo, de `### 5.2` a `### 5.3`), **NO usar `---`**. El salto se indica únicamente con el nuevo título.

### Matemáticas

- **Inline:** `$expresión$` para símbolos dentro del texto
- **Display simple:** `$$ecuación$$` para ecuaciones importantes de 1 o 2 líneas.
- **Desarrollos matemáticos:** Si un bloque de ecuaciones (desarrollo o demostración) tiene **3 o más líneas**, es OBLIGATORIO agrupar todo en un único bloque usando el entorno `\begin{align} ... \end{align}` en lugar de múltiples bloques `$$` independientes.
- Notación consistente: si se define $\theta$ para el ángulo, no cambiar a $\alpha$
- Fracciones en display: preferir `\dfrac` sobre `\frac` para mayor legibilidad

### Imágenes (formato Obsidian)

```markdown
![[nombre_archivo.png]]
![[nombre_archivo.png|ancho]]    ← con ancho en píxeles
```

### Listas de propiedades numeradas

```markdown
1. **Nombre de la propiedad:** descripción
2. **Nombre de la propiedad:** descripción
```

### Tablas

- Usar para comparaciones, clasificaciones y tablas de valores
- Centrar columnas numéricas con `:---:`
- Alinear texto a la izquierda con `:---`

### Lenguaje académico

- Español formal y técnico
- Verbos preferidos: "se define", "se cumple", "se demuestra", "se tiene que", "se verifica"
- **Prohibido:** "es obvio que", "claramente", "trivialmente", "es fácil ver"

---

## Plantilla completa de subsección

```markdown
### N.M Nombre del concepto

Párrafo introductorio casual. Aquí se establece la motivación: qué problema
resuelve este concepto, por qué es útil, qué imagen mental debe construir
el estudiante. Puede usarse "Pensemos en...", analogías o preguntas retóricas.
Máximo 2–3 párrafos.

> **Nota histórica:** [Solo si aporta comprensión — OMITIR si no aplica]

**Definición N.M (Nombre):**
$$\text{expresión matemática formal}$$
donde $a$ es [descripción] y $b$ es [descripción], con $a \in \text{dominio}$.

**Teorema N.M (Nombre del teorema):**
$$\text{enunciado formal}$$

**Demostración:**
[texto explicativo]
$$\text{paso algebraico}$$
[conclusión]
$\blacksquare$

**Ejemplo N.M:**
[enunciado concreto]
$$\text{desarrollo}$$

**Aplicaciones:**
[Párrafo o lista indicando en qué contextos aparece este concepto y por qué es útil.
OMITIR solo si el objeto es puramente auxiliar.]

> **Observación:** [aclaración técnica o extensión del concepto — OMITIR si no aplica]
```

---

## 8. Ejercicios resueltos

**Propósito:** Sección dedicada a problemas resueltos paso a paso. Cada ejercicio debe ser un título independiente para facilitar la navegación y referencia.

**Formato estándar:**

```markdown
### Ejercicio N.M

[Enunciado del ejercicio]

**Solución:**
[Desarrollo paso a paso]
[Expresiones matemáticas]
[Conclusión o respuesta final]
```

**Reglas:**

- Cada ejercicio es un encabezado `###` (no `####`)
- Numeración correlativa dentro de la sección: `Ejercicio 1:`, `Ejercicio 2:`, etc.
- Siempre incluir **Solución:** como encabezado antes del desarrollo
- Usar alineación (`\begin{align}`) para pasos algebraicos múltiples
- Terminar con la respuesta final clara (destacarla si es relevante)

**Ejemplo real del proyecto:**

```markdown
### Ejercicio 1:
Encuentre el centro y radio de la circunferencia $x^2 + y^2 - 8x + 6y + 9 = 0$.

**Solución:**
Completamos cuadrados para $x$ e $y$:

$$x^2 - 8x + y^2 + 6y = -9$$
$$(x^2 - 8x + 16) + (y^2 + 6y + 9) = -9 + 16 + 9$$
$$(x - 4)^2 + (y + 3)^2 = 16$$

- **Centro:** $(4, -3)$
- **Radio:** $r = \sqrt{16} = 4$
```

---

## Lo que NO hacer

- No añadir la etiqueta `**Idea intuitiva:**` — escribir directo el párrafo introductorio
- No omitir condiciones de dominio en definiciones
- No mezclar notaciones distintas para el mismo objeto
- No añadir contexto histórico que no aporte comprensión
- No presentar demostraciones informales como si fueran formales
  (usar `$\square$` si es informal, `$\blacksquare$` si es rigurosa)
- No omitir demostraciones alegando que son "triviales" o "ejercicio para el lector"
- No usar conceptos sin haberlos definido previamente (o sin indicar el prerequisito)
- No incluir secciones vacías ni marcadores de posición como "TODO"
- No escribir encabezados `#### N.M.K` a menos que sea estrictamente necesario
- No escribir "es obvio que", "claramente", "trivialmente", "simplemente" o "es fácil ver"
- No dirigirse al lector en segunda persona informal ("haz esto", "fíjate que")
