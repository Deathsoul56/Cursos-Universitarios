---
description: >
  Formato estándar para syllabus de cursos universitarios STEM en este proyecto.
  Aplica SIEMPRE al crear o editar la presentación de un curso, programa,
  descripción, objetivos, prerrequisitos o bibliografía de Cálculo, Álgebra,
  Probabilidad, Estadística, Ciencia de los Materiales o Cálculo Numérico.
  WHEN: syllabus, presentación del curso, programa del curso, descripción
  del curso, objetivos de aprendizaje, bibliografía.
---
# SKILL: Syllabus estándar — Cursos Universitarios STEM

## Objetivo

Definir una estructura común, concisa y formal para los documentos de presentación de curso (syllabus) del proyecto. Un syllabus no es un plan de clases detallado ni un manual del docente: es la carta de presentación de un curso para un estudiante que decide qué estudiar, qué esperar y qué herramientas necesita.

## Espíritu

- Rigor sin pedantería.
- Enfoque en el estudiante, no en la administración académica.
- Contenido replicable entre cursos del repositorio.

## Secciones obligatorias

1. **Título del curso** (`# Nombre del curso`).
2. **Resumen ejecutivo** (1–2 oraciones justo debajo del título).
3. **Descripción del curso** (motivación + alcance formal).
4. **Objetivos de aprendizaje** (numerados, observables).
5. **Prerrequisitos** (conocimientos concretos previos).
6. **Programa / contenido por módulos**.
7. **Bibliografía** (principales y complementarios, con anotaciones).

## Secciones opcionales

- Metodología y notas de estudio.
- Conocimientos o competencias al finalizar el curso.
- Conexiones interdisciplinarias.

## Reglas de contenido

- **NO incluir**: horarios de examen, políticas de evaluación, porcentajes de calificación, normas de asistencia, fechas de entrega ni información de matrícula.
- **NO usar verbos vagos** en objetivos como "comprender", "dominar", "saber" o "conocer". Preferir: "demostrar", "calcular", "resolver", "formular", "analizar", "construir", "aplicar", "clasificar", "verificar".
- La descripción debe comenzar con una **motivación casual** (para qué sirve el curso) antes de la declaración formal de su alcance.
- Los objetivos deben ser **observables**: una tercera persona debe poder verificar si el estudiante los cumple.
- Los prerrequisitos deben ser **conocimientos concretos**, no cursos genéricos.
- El programa debe organizarse por **módulos numerados** (`## N. Módulo ...` o `### Módulo N...`) con subtemas concisos. Puede incluir una indicación temporal aproximada (semanas) si es útil para autoestudio.
- La bibliografía separa **textos principales** de **complementarios**; se añade una breve nota cuando el texto tiene un enfoque especial (rigor, aplicaciones, nivel avanzado).

## Convenciones de formato

- Encabezados: `# Título del curso`, `## N. Nombre de sección`, `### N.M Subsección` solo si es estrictamente necesario.
- No usar texto en mayúsculas para encabezados.
- Matemáticas en `$...$` o `$$...$$`.
- Listas numeradas para objetivos y bibliografía.
- Tablas permitidas para resumen de módulos o carga horaria.
- Separadores `---` solo entre secciones principales.

## Ejemplo de estructura

```markdown
# Cálculo 1: Análisis Real y Cálculo Diferencial

En este curso se construyen los fundamentos del análisis real de una variable y se desarrolla el cálculo diferencial, desde la axiomática de los números reales hasta las aplicaciones de la derivada en contextos STEM.

## 1. Descripción del curso

El cálculo diferencial nace de la necesidad de cuantificar el cambio instantáneo... En este curso se estudian ...

## 2. Objetivos de aprendizaje

Al finalizar el curso, el estudiante será capaz de:

1. Demostrar propiedades básicas de los números reales a partir del axioma del supremo.
2. Calcular límites de funciones algebraicas y trascendentes usando definiciones y técnicas estándar.
3. Resolver problemas de optimización y razones de cambio relacionadas mediante derivadas.
4. Analizar el comportamiento global de una función usando derivadas de primer y segundo orden.
5. Aplicar el cálculo diferencial en modelos de física, ingeniería y economía.

## 3. Prerrequisitos

- Aritmética y álgebra básica: factorización, fracciones, potencias, raíces.
- Funciones elementales: polinomios, racionales, exponenciales, logaritmos y trigonométricas.
- Geometría analítica: rectas, circunferencias y cónicas.
- Nociones de lógica proposicional y cuantificadores.

## 4. Programa

### Módulo 0. Fundamentos matemáticos
Construcción axiomática de los números reales, valor absoluto, ecuaciones e inecuaciones.

### Módulo 1. Geometría analítica y cónicas
Ecuación general de segundo grado, clasificación, traslación y rotación.

...

## 5. Bibliografía

### Textos principales
1. Stewart, J., Clegg, D. & Watson, S. (2020). *Calculus: Early Transcendentals* (9th ed.). Cengage Learning.

### Textos complementarios
2. Spivak, M. (2008). *Calculus* (4th ed.). Publish or Perish. [Énfasis en rigor y demostración.]
```

## Lo que NO hacer

- No incluir secciones de evaluación, exámenes, calificaciones ni políticas administrativas.
- No escribir objetivos con verbos no observables.
- No usar mayúsculas en encabezados.
- No incluir marcadores TODO ni secciones vacías.
