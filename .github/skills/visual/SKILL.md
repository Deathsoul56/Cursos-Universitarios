---
description: >
  Estilo gráfico oscuro con acentos neon para ilustraciones, diagramas,
  gráficos de datos y animaciones generados con Python en el proyecto
  Cursos-Universitarios. Aplica SIEMPRE cuando se cree o modifique un script
  Python que produzca imágenes o GIFs para las notas: mantener fondo negro,
  colores neon de alto contraste, glow sutil y coherencia visual con las
  ilustraciones existentes.
---

# SKILL: Estilo visual oscuro / neon para ilustraciones Python

## Objetivo

Producir figuras, diagramas y animaciones con una estética unificada:
**fondo negro, colores neon saturados, bordes brillantes y glow sutil**. El
estilo debe ser legible en Obsidian con temas oscuros y mantenerse coherente
tanto en diagramas ilustrativos hechos con PIL como en gráficos de datos hechos
con matplotlib.

---

## Principios generales

1. **Fondo siempre oscuro.** Negro puro (`#000000`) o negro azulado muy oscuro
   (`#050510`). No usar fondos claros ni gradientes.
2. **Colores neon de alto contraste.** Magenta, cyan, amarillo, púrpura, verde
   y naranja como acentos principales.
3. **Textos con color semántico.** Títulos, etiquetas y leyendas de un panel
   deben usar el mismo color del elemento al que hacen referencia (por ejemplo,
   púrpura para la curva del panel izquierdo, cyan para la del derecho).
4. **Líneas y curvas con grosor suficiente.** Curvas principales y rectas de
   intersección deben tener entre 4 px y 6 px para destacar sobre el fondo y el
   grid. Líneas auxiliares pueden ser más delgadas (1–2 px).
5. **No mezclar gráficas con textos.** Reservar márgenes claros alrededor de
   títulos, leyendas y pies. Si una curva tiende a salirse, recortarla al área
   de dibujo; nunca dejar que cruce sobre el texto.
6. **Grid sutil.** Líneas tenues que ayuden a leer posiciones sin competir con
   el contenido.
7. **Cajas para fórmulas.** Cuando se muestre una fórmula o resultado clave,
   usar una caja con borde redondeado del color del acento.
8. **Claridad sobre decoración.** Cada color debe tener un significado
   consistente dentro de la figura.

---

## Paleta de colores

### Colores base

| Rol | HEX | Uso |
|-----|-----|-----|
| Fondo | `#000000` o `#050510` | Fondo de toda la imagen |
| Texto principal | `#ffffff` | Etiquetas, títulos, valores |
| Grid | `#1a1a2e` / `#222222` | Cuadrícula de fondo |
| Ejes | `#33334d` / `#666666` | Ejes coordenados |
| Líneas guía | `#444444` | Líneas auxiliares proyectadas |

### Colores de acento neon

| Nombre | HEX | Uso típico |
|--------|-----|------------|
| Púrpura | `#9900ff`, `#bf00ff` | **Color por defecto para curvas y figuras solitarias**. También fórmulas, distancias, semirrectas |
| Magenta / Rosa | `#ff007f`, `#ff00ff`, `#ff1493` | Figuras principales, conjuntos dominio, componentes X |
| Cyan | `#00ffff`, `#00ffcc` | Segunda curva en comparaciones, codominio, componentes Y |
| Amarillo | `#ffff00`, `#ffd700` | Vectores, flechas, hipotenusas, rectas de intersección, resultados destacados |
| Verde | `#00ff00`, `#00ff7f` | Tercera serie, confirmaciones, áreas |
| Naranja / Rojo | `#ff4500`, `#ff3333` | Cuarta serie, advertencias, barras adicionales |
| Blanco | `#ffffff` | Puntos de intersección, etiquetas numéricas, contornos |

### Reglas de uso del color

- **Color principal: púrpura (`#9900ff`).** Es el color por defecto para
  curvas y figuras solitarias, y también para sus títulos, leyendas y
  elementos asociados. **Nunca usar cian como primera opción** si no hay una
  segunda curva o una comparación explícita que lo justifique.
- **Cian es un color secundario.** Solo se utiliza cuando hay una segunda
  curva o serie que se contrasta con la principal (por ejemplo, comparar
  dominio y codominio, o dos funciones en el mismo gráfico).
- No usar más de 4–5 colores de acento en una misma figura.
- Mantener un color por categoría semántica (por ejemplo, púrpura para la
  curva principal, magenta para el dominio, cyan para el codominio, amarillo
  para las flechas).
- Para series de datos (barras, líneas), usar la lista: púrpura → magenta →
  cyan → amarillo → verde → naranja.
- Los textos asociados a un objeto deben usar el color de ese objeto: título y
  leyenda en púrpura si la curva es púrpura; título y leyenda en cyan si la
  curva es cyan.
- Los textos en color neon deben llevar un contorno oscuro o un glow para
  mejorar la legibilidad sobre fondo negro.
- **El título de la figura siempre va centrado horizontalmente** en la parte
  superior. Su color sigue la regla principal: púrpura por defecto.

---

## Dos familias de visualización

### Familia A: Diagramas ilustrativos (PIL / Pillow)

Usar cuando la figura es un diagrama geométrico, una demostración visual, un
mapeo entre conjuntos o una animación.

#### Elementos típicos

- **Título** en la parte superior, centrado, en mayúsculas o con inicial
  mayúscula, color de acento con glow.
- **Área de dibujo** claramente delimitada, con márgenes de al menos 30–40 px
  respecto a los bordes del panel y respecto a títulos, leyendas y pies.
- **Figura central** con borde neon y relleno semitransparente del mismo color.
- **Puntos** como círculos con relleno blanco y contorno del color de su
  conjunto.
- **Líneas y flechas** gruesas (4–6 px para elementos principales, 2–3 px para
  secundarios) en amarillo o en el color de su elemento.
- **Etiquetas** cerca de cada objeto, en el mismo color que el objeto.
- **Fórmula o resultado** al pie o junto a la figura, dentro de una caja con
  borde redondeado.

#### Layout y márgenes

```
+-------------------------------+
|         Título principal      |
|   Título panel    Título panel|
|  +--------------+ +----------+|
|  |              | |          ||
|  | Área de      | | Área de  ||
|  | dibujo       | | dibujo   ||
|  |              | |          ||
|  +--------------+ +----------+|
|   Leyenda panel   Leyenda panel|
|         Pie de imagen         |
+-------------------------------+
```

- Dejar al menos 30 px entre el área de dibujo y cualquier texto.
- Si una curva se sale del área de dibujo, recortarla; nunca extenderla sobre
  títulos o leyendas.
- Las leyendas inferiores deben quedar completamente por debajo del área de
  dibujo.

#### Cajas de fórmulas

```python
# Ejemplo conceptual
bbox = [x0, y0, x1, y1]
draw.rounded_rectangle(bbox, radius=20, outline=accent_color, width=3)
# Glow exterior
draw.rounded_rectangle([x0-2, y0-2, x1+2, y1+2], radius=22,
                       outline=glow_color, width=1)
```

- Borde: 2–3 px del color del acento.
- Esquinas redondeadas: 15–25 px de radio.
- Opcional: glow exterior de 1 px con una versión más oscura o más clara del
  color.

#### Glow en textos

Dibujar el texto 1–2 px desplazado en cada dirección con el color del acento
antes de dibujar el texto blanco central:

```python
for dx, dy in [(-1,-1), (-1,1), (1,-1), (1,1), (0,0)]:
    color = glow_color if (dx, dy) != (0,0) else text_color
    draw.text((x+dx, y+dy), text, fill=color, font=font)
```

---

### Familia B: Gráficos de datos (matplotlib)

Usar para barras, histogramas, líneas, dispersión, etc.

#### Configuración base de matplotlib

```python
import matplotlib.pyplot as plt

plt.style.use('dark_background')
plt.rcParams.update({
    "figure.facecolor": "#000000",
    "axes.facecolor": "#000000",
    "axes.edgecolor": "#ffffff",
    "axes.labelcolor": "#ffffff",
    "text.color": "#ffffff",
    "xtick.color": "#ffffff",
    "ytick.color": "#ffffff",
    "grid.color": "#222222",
    "grid.linestyle": "--",
    "grid.linewidth": 0.5,
})
```

#### Paleta recomendada para series

```python
NEON_COLORS = ["#9900ff", "#ff00ff", "#00ffff", "#ffff00",
               "#00ff00", "#ff4500", "#ff1493"]
```

#### Reglas

- Usar `edgecolor="white"` y `linewidth=1.5` en barras para que resalten.
- Mostrar valores sobre las barras en blanco con `fontweight="bold"`.
- Líneas gruesas (`linewidth=2.5` o más) con glow simulado dibujando la misma
  línea 2–3 veces con transparencia y grosor creciente.
- Leyenda con fondo oscuro y borde blanco.

---

## Tipografía

- **Fuente preferida para PIL:** `Consolas` bold/regular (`consolab.ttf` /
  `consola.ttf`).
- **Fallback PIL:** `Arial`, luego `ImageFont.load_default()`.
- **Fuente matplotlib:** `Consolas` si está disponible; de lo contrario dejar
  la fuente por defecto.

### Jerarquía de tamaños (PIL)

| Uso | Tamaño | Peso |
|-----|--------|------|
| Título principal | 32–48 | Bold |
| Números grandes / destaque | 48–72 | Bold |
| Subtítulos / etiquetas de sección | 20–28 | Bold |
| Etiquetas de objetos | 16–20 | Bold |
| Valores numéricos y cuerpo | 14–18 | Regular |
| Notas pequeñas | 12–14 | Regular |

---

## Convenciones por tipo de figura

### Diagramas de conjuntos (funciones, relaciones)

- Conjunto de partida (dominio): elipse magenta con puntos magenta/rosa.
- Conjunto de llegada (codominio): elipse cyan con puntos cyan.
- Flechas de mapeo: amarillas, con punta de flecha.
- Título del mapeo: centrado arriba, **púrpura** con glow.
- Leyenda al pie: color del acente correspondiente.

### Plano cartesiano

- Fondo negro, grid gris oscuro punteado o continuo.
- Ejes X e Y en color cyan claro o blanco; flechas opcionales en los extremos.
- Cuadrantes con tintes sutilmente coloreados (muy transparentes) para
  diferenciarlos visualmente.
- **Curvas principales:** grosor 4–6 px, con glow sutil o sin glow según el
  estilo deseado. Recortarlas al área de dibujo para que no choquen con textos.
- **Rectas de intersección / verificación:** usar un color de alto contraste
  como el amarillo `#ffff00`, grosor 4–6 px, para que destaquen sobre las
  curvas y el grid.
- **Puntos importantes:** círculos con relleno blanco y contorno del color de
  la curva; radio 6–8 px.
- Mantener márgenes claros entre el área de dibujo y los títulos o leyendas.

### Gráficos de barras / histogramas

- Fondo negro, ejes blancos, grid horizontal sutil.
- Barras con bordes blancos y relleno neon.
- Valores sobre cada barra en blanco bold.
- Etiquetas de ejes en blanco, tamaño grande.
- Para histogramas: usar colores diferentes por intervalo solo cuando el
  intervalo tenga significado; de lo contrario, un solo color.

### Demostraciones geométricas

- Figuras con relleno semitransparente (alpha ~0.3–0.5) y borde sólido neon.
- Lados importantes resaltados en amarillo o cyan.
- Ángulos rectos marcados con un pequeño cuadrado blanco.
- Fórmula final en una caja con borde redondeado al pie.

---

## Plantilla base para PIL

```python
from PIL import Image, ImageDraw, ImageFont

# --- Configuración ---
WIDTH, HEIGHT = 1000, 700
BG = "#000000"

COLORS = {
    "purple": "#9900ff",   # color por defecto para curvas solitarias
    "magenta": "#ff007f",
    "cyan": "#00ffff",
    "yellow": "#ffff00",
    "green": "#00ff00",
    "orange": "#ff4500",
    "white": "#ffffff",
    "grid": "#1a1a2e",
    "axis": "#33334d",
}

def get_font(size, bold=False):
    try:
        name = "consolab.ttf" if bold else "consola.ttf"
        return ImageFont.truetype(f"C:/Windows/Fonts/{name}", size)
    except:
        try:
            return ImageFont.truetype("arial.ttf", size)
        except:
            return ImageFont.load_default()

font_title = get_font(36, bold=True)
font_label = get_font(18, bold=True)
font_text = get_font(16)

# --- Crear imagen ---
img = Image.new('RGB', (WIDTH, HEIGHT), BG)
draw = ImageDraw.Draw(img)

# Grid opcional
for i in range(0, WIDTH, 50):
    draw.line([(i, 0), (i, HEIGHT)], fill=COLORS["grid"])
for i in range(0, HEIGHT, 50):
    draw.line([(0, i), (WIDTH, i)], fill=COLORS["grid"])

# Título con glow
def draw_glow_text(draw, pos, text, font, glow, text_color, offset=2):
    x, y = pos
    for dx in range(-offset, offset+1):
        for dy in range(-offset, offset+1):
            if dx != 0 or dy != 0:
                draw.text((x+dx, y+dy), text, fill=glow, font=font)
    draw.text((x, y), text, fill=text_color, font=font)

draw_glow_text(draw, (WIDTH//2, 30), "Título de la figura",
               font_title, COLORS["purple"], COLORS["white"])

# Guardar
img.save("figura.png")
```

---

## Plantilla base para matplotlib

```python
import matplotlib.pyplot as plt
import numpy as np

NEON = ["#9900ff", "#ff00ff", "#00ffff", "#ffff00",
        "#00ff00", "#ff4500", "#ff1493"]

plt.style.use('dark_background')
plt.rcParams.update({
    "figure.facecolor": "#000000",
    "axes.facecolor": "#000000",
    "axes.edgecolor": "#ffffff",
    "axes.labelcolor": "#ffffff",
    "text.color": "#ffffff",
    "xtick.color": "#ffffff",
    "ytick.color": "#ffffff",
    "grid.color": "#222222",
    "grid.linestyle": "--",
    "grid.linewidth": 0.5,
})

fig, ax = plt.subplots(figsize=(10, 6))

# Ejemplo: línea con glow
x = np.linspace(-2, 5, 300)
y = np.sin(x)
for w, alpha in [(6, 0.15), (4, 0.3), (2, 1.0)]:
    ax.plot(x, y, color=NEON[0], linewidth=w, alpha=alpha)

ax.set_xlabel("x", fontsize=14)
ax.set_ylabel("y", fontsize=14)
ax.set_title("Título", fontsize=18, color=NEON[0])
ax.grid(True)
plt.tight_layout()
plt.savefig("grafico.png", dpi=150, facecolor="#000000")
```

---

## Reglas de exportación

- **Formato:** PNG para imágenes estáticas, GIF para animaciones.
- **Resolución:** 150 DPI para notas; 300 DPI si se usará en presentaciones.
- **Dimensiones:** preferir proporciones 16:9, 4:3 o 1:1 según el contenido.
- **Ubicación de salida de los scripts:** guardar SIEMPRE en la **raíz del
  proyecto**. El usuario revisará la imagen y, una vez aprobada, la moverá a
  `Recursos/`. Esto facilita la iteración y evita perder imágenes entre muchos
  archivos.
- **Referencia en Obsidian:** usar `![[Recursos/nombre_archivo.png]]` o
  `![[Recursos/nombre_archivo.gif]]`, ya que la ubicación final de las
  ilustraciones aprobadas es `Recursos/`.

---

## Lo que NO hacer

- No usar fondos claros ni degradados.
- No usar colores pastel o apagados.
- No usar más de 5 colores de acento en una sola figura.
- No dejar textos sin contorno o glow si son de color neon sobre negro.
- No usar tipografías decorativas o serif.
- No omitir el grid en planos cartesianos ni los bordes en barras.
- **No mezclar funciones, curvas o figuras sobre el texto.** Siempre respetar
  los márgenes entre el área de dibujo y los títulos, leyendas y pies.
- No usar líneas o curvas demasiado delgadas; los elementos principales deben
  tener al menos 3 px, preferiblemente 4–6 px.
- No desvincular el color de los textos del elemento al que se refieren; los
  títulos y leyendas deben compartir color con su curva o figura asociada.
- No generar figuras con dimensiones arbitrarias que no encajen en el estilo
  del proyecto.
