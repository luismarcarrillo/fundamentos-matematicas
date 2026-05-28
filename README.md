# Fundamentos de las Matemáticas · 2026-I

Portafolio académico de los 8 talleres del curso, publicado con **Quarto** en **GitHub Pages**.

---

## Estructura del repositorio

```
fundamentos-matematicas/
│
├── _quarto.yml              ← configuración del sitio Quarto
├── index.qmd                ← página de inicio (o index.html si no usas Quarto)
│
├── talleres/
│   ├── taller-01.qmd        ← Lógica proposicional
│   ├── taller-02.qmd        ← Tablas de verdad
│   ├── taller-03.qmd        ← Teoría de conjuntos
│   ├── taller-04.qmd        ← Relaciones
│   ├── taller-05.qmd        ← Funciones
│   ├── taller-06.qmd        ← Inducción matemática
│   ├── taller-07.qmd        ← Números naturales
│   └── taller-08.qmd        ← Análisis real
│
├── assets/
│   ├── custom.scss          ← estilos personalizados
│   └── logo-universidad.png ← reemplaza con tu logo real
│
└── docs/                    ← (generado por Quarto) GitHub Pages sirve desde aquí
```

---

## Cómo publicar en GitHub Pages

### Opción A — Solo HTML (sin Quarto instalado localmente)

1. Sube `index.html` a la raíz del repositorio.
2. Para cada taller: crea la carpeta `talleres/` y sube los archivos `.html`
   que exportes desde tu entorno (Jupyter → Export as HTML, etc.).
3. En **Settings → Pages**, selecciona rama `main` y carpeta `/root`.
4. Tu sitio queda en `https://tu-usuario.github.io/fundamentos-matematicas/`.

---

### Opción B — Quarto completo (recomendada)

#### 1. Instalar Quarto

Descarga el instalador en [quarto.org/docs/get-started](https://quarto.org/docs/get-started/).

#### 2. Renderizar el sitio localmente

```bash
# Desde la raíz del repositorio:
quarto render

# O con vista en vivo:
quarto preview
```

Los archivos HTML quedan en `docs/`.

#### 3. Subir a GitHub

```bash
git add .
git commit -m "Agrego taller X renderizado"
git push
```

#### 4. Activar GitHub Pages

- Ve a **Settings → Pages** en tu repositorio.
- En *Source* selecciona rama `main` y carpeta `/docs`.
- Guarda. En ~2 minutos tu sitio estará en vivo.

---

## Cómo agregar un taller nuevo

1. Abre `talleres/taller-0X.qmd` en tu editor (VS Code + extensión Quarto, RStudio, o cualquier editor de texto).
2. Escribe tu desarrollo: texto en Markdown, matemáticas en LaTeX, código en bloques.
3. Ejecuta `quarto render talleres/taller-0X.qmd` para previsualizar.
4. Cuando esté listo, `quarto render` para compilar todo el sitio.
5. Haz `git push` — GitHub Pages se actualiza automáticamente.

---

## Agregar el logo de la universidad

1. Guarda el logo como `assets/logo-universidad.png`.
2. En `index.html` (o `index.qmd`), reemplaza el div `.univ-logo-placeholder` por:

```html
<img src="assets/logo-universidad.png" alt="Logo universidad"/>
```

---

## Cambiar los datos personales

Edita en `index.html` (sección `<script>`) o en `index.qmd`:

- `Tu Nombre Aquí` → tu nombre completo
- `000000000` → tu código estudiantil
- `Nombre del Profesor` → nombre del docente
- Los temas de cada taller en el arreglo `talleres`

---

## Recursos útiles

- [Quarto — Documentación oficial](https://quarto.org/docs/)
- [Quarto + GitHub Pages](https://quarto.org/docs/publishing/github-pages.html)
- [MathJax — LaTeX en web](https://www.mathjax.org/)
