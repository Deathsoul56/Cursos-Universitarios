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

---

## Estructura de una sección

Cada sección principal usa el encabezado `## N. Título` y sus subsecciones
`### N.M Nombre del concepto`. Dentro de cada subsección el orden es:

```
1. Introducción/motivación casual        ← OBLIGATORIO
2. Contexto histórico                    ← OPCIONAL
3. Definición(es) formal(es)             ← OBLIGATORIO si hay objeto nuevo
4. Teoremas / Proposiciones              ← según corresponda
5. Ejemplos                              ← OBLIGATORIO al menos uno
6. Observaciones / Notas                 ← según corresponda
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

## 2. Contexto histórico (OPCIONAL)

Solo incluir si **aporta motivación o comprensión**. Nunca como relleno.

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

**Cuándo incluirlo:**
- El nombre del objeto tiene un origen no obvio (e.g., "seno" viene del latín *sinus*)
- El concepto tardó siglos en formalizarse (e.g., el límite en el Cálculo)
- Existe una paradoja o controversia histórica relevante (e.g., paradoja de Russell)
- El autor o época es relevante para entender el concepto

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

| Objeto | Etiqueta |
|---|---|
| Definición | `**Definición N.M (Nombre):**` |
| Teorema | `**Teorema N.M (Nombre):**` |
| Proposición | `**Proposición N.M (Nombre):**` |
| Lema | `**Lema N.M (Nombre):**` |
| Corolario | `**Corolario N.M (Nombre):**` |
| Postulado | `**Postulado N:** texto` |

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

## 6. Observaciones y Notas

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
- Usar `---` entre secciones principales (`## N.`)
- No usar `---` entre subsecciones (`### N.M`)

### Matemáticas
- **Inline:** `$expresión$` para símbolos dentro del texto
- **Display:** `$$ecuación$$` para ecuaciones importantes o multi-línea
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

> **Observación:** [aclaración técnica o extensión del concepto — OMITIR si no aplica]
```

---

## Lo que NO hacer

- No añadir la etiqueta `**Idea intuitiva:**` — escribir directo el párrafo introductorio
- No omitir condiciones de dominio en definiciones
- No mezclar notaciones distintas para el mismo objeto
- No añadir contexto histórico que no aporte comprensión
- No presentar demostraciones informales como si fueran formales
  (usar `$\square$` si es informal, `$\blacksquare$` si es rigurosa)
- No usar conceptos sin haberlos definido previamente (o sin indicar el prerequisito)
- No incluir secciones vacías ni marcadores de posición como "TODO"
- No escribir encabezados `#### N.M.K` a menos que sea estrictamente necesario
