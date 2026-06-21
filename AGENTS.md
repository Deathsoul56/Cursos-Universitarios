# AGENTS.md — Cursos Universitarios

## Tipo de proyecto

Repositorio de notas académicas universitarias para STEM, diseñadas para visualizarse en
Obsidian. Archivos en Markdown con soporte para KaTeX (matemáticas).

## Filosofía del proyecto

Estos apuntes tienen un objetivo preciso: **rigor formal sin pedantería**. No son un libro
de texto ni un manual de referencia — son los apuntes de un estudiante brillante que
entiende profundamente el material y sabe explicarlo.

El tono ideal es el de un alumno de alto rendimiento en una universidad de primer nivel:
conoce la definición épsilon-delta, pero primero dibuja la idea con palabras. Puede
demostrar el teorema, pero antes explica por qué alguien querría demostrarlo.

**El contenido tiene cuatro capas, en orden:**

1. **Motivación casual** — qué problema resuelve este concepto, por qué existe
2. **Definición formal** — con rigor, numeración y dominio explícito
3. **Ejemplos** — al menos uno por objeto importante, preferiblemente varios
4. **Aplicaciones** *(opcional)* — dónde aparece en matemáticas, física, ingeniería u otras áreas

Este pipeline es la identidad del proyecto. Diferencia estos apuntes de un libro (que va
directo a la definición) y de apuntes informales (que nunca llegan al rigor formal).

## Estructura del repositorio

```
/Calculo 1/                    ← Clases 1-10, Guías 1-5
/Algebra/                      ← Clases de lógica y proposiciones
/Algebra Lineal/               ← (en desarrollo)
/Calculo Numérico/             ← Clases de análisis de errores
/Ciencia de los Materiales/
/Probabilidad y Estadistica/
/Recursos/
/.github/skills/formato/SKILL.md   ← Formato académico obligatorio
/.github/skills/visual/SKILL.md    ← Estilo visual oscuro/neon para ilustraciones Python
```

### Tipos de archivo

| Tipo | Descripción | Estructura |
|------|-------------|------------|
| **Clase** | Notas de contenido teórico | Pipeline completo: motivación → definición → ejemplos → aplicaciones *(opcional)* |
| **Guía** | Serie de ejercicios resueltos | Teoría breve de referencia + ejercicios con dificultad por estrellas |

## Pipeline estándar de cada subsección (Clases)

Cada concepto nuevo sigue este orden dentro de su `### N.M` subsección:

```
1. Motivación casual           ← OBLIGATORIO
   Párrafo(s) libres. Qué problema resuelve. Sin etiqueta especial.

2. Contexto histórico          ← RECOMENDADO
   La ciencia se entiende mejor en su contexto. Omitir solo si el concepto
   no tiene historia relevante o si el origen es puramente formal/notacional.

3. Definición(es) formal(es)   ← OBLIGATORIO si hay objeto nuevo
   Con numeración, dominio y condiciones de validez.

4. Teoremas / Proposiciones    ← según corresponda
   Con demostración (o referencia a sección donde se demostrará).

5. Ejemplos                    ← OBLIGATORIO al menos uno
   Caso general + casos límite cuando sea relevante.

6. Aplicaciones                ← OPCIONAL
   Dónde aparece en matemáticas, física, ingeniería u otras disciplinas.

7. Observaciones / Notas       ← según corresponda
   Extensiones técnicas, errores comunes, conexiones con otros temas.
```

La sección de **Aplicaciones** es opcional. Se incluye cuando el concepto tiene conexiones
relevantes con otras áreas y enriquece la comprensión; se omite cuando el contexto no lo
justifica o cuando agregar aplicaciones sobrecarga la sección.

## Reglas de formato obligatorias

**ANTES de redactar, ampliar o editar cualquier contenido, cargar y aplicar:**

`.github/skills/formato/SKILL.md`

Esa skill define en detalle:
- Encabezados: `## N. Título` y `### N.M Concepto`
- Definiciones: `**Definición N.M (Nombre):**` + expresión matemática + dominio
- Teoremas: `**Teorema N.M (Nombre):**` + enunciado formal + demostración
- Demostraciones: `$\blacksquare$` (rigurosa) o `$\square$` (intuitiva)
- Ejemplos: numeración correlativa, al menos uno por objeto importante
- Aplicaciones: párrafo(s) o lista conectando el concepto con contextos reales
- Ejercicios (Guías): encabezado `### Ejercicio N.M`, `**Solución:**`, desarrollo paso a paso

## Convenciones de lenguaje

- Español formal académico
- Verbos preferidos: "se define", "se cumple", "se demuestra", "se verifica", "se tiene que"
- **PROHIBIDO:** "es obvio que", "claramente", "trivialmente", "es fácil ver", "simplemente"
- **PROHIBIDO:** etiquetas como `**Idea intuitiva:**` — el párrafo motivacional habla por sí solo
- **PROHIBIDO:** hablar al lector en segunda persona informal ("haz esto", "fíjate que")
- **PROHIBIDO:** omitir una demostración alegando que es "trivial" o "se deja como ejercicio para el lector". Toda afirmación demostrable debe demostrarse aquí o, si corresponde a otro curso, diferirse con referencia explícita a la sección o curso donde se demostrará.

## Matemáticas

- Inline: `$expresión$`
- Display (1-2 líneas): `$$ecuación$$`
- Desarrollos de 3+ líneas: `\begin{align}...\end{align}` obligatorio en un único bloque
- Usar `\dfrac` sobre `\frac` en expresiones display
- Usar `\text{}` para texto dentro de expresiones matemáticas
- Notación consistente: no cambiar $\theta$ por $\alpha$ a mitad de una sección

## Cómo editar este proyecto

1. Antes de crear o editar cualquier nota de curso → cargar `.github/skills/formato/SKILL.md` con la skill tool
2. Antes de crear o editar cualquier script Python que genere imágenes o GIFs → cargar `.github/skills/visual/SKILL.md` con la skill tool
3. Seguir el pipeline: motivación → definición → teoremas → ejemplos → aplicaciones → observaciones
4. Mantener numeración correlativa dentro de cada sección
5. No dejar secciones vacías ni marcadores "TODO"
6. En Guías: `### N.M Título ⭐/⭐⭐/⭐⭐⭐` para bloques de ejercicios; `### Ejercicio N.M` para cada uno

## Tareas pendientes (BackLog.md)

Ver `BackLog.md` para tareas pendientes de desarrollo.
