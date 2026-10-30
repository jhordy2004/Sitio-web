# MANGA VOID — Tienda Oficial de Manga y Ediciones de Colección

**Asignatura:** Desarrollo de Aplicaciones Web  
**Carrera:** Ingeniería en Software  
**Institución:** Universidad de Guayaquil  
**Semestre:** 6to Semestre  
**Docente:** Mgtr. Karla Yadira Abad Sacoto  
**Estudiante:** Marco Córdova Rivera  

---

## 1. Descripción de la Temática

**MANGA VOID** es un sitio web estático de comercio electrónico y archivo cultural dedicado al manga físico japonés, ediciones de lujo (*Kanzenban*), formatos integrales (*Ómnibus*) y piezas de colección.

El proyecto está diseñado bajo una dirección estética **"Manga-Industrial"** de alto contraste:
- Paleta cromática inspirada en la tinta china y el rojo carmesí (*Crimson Ink*): `#b7102a` (rojo primario), `#161d16` (negro tinta profunda), `#f3fcf0` (blanco papel ahuesado) y acentos secundarios en azul acero y azul petróleo.
- Tipografías oficiales desde **Google Fonts**: **Anton** (titulares de impacto cinético), **Hanken Grotesk** (lectura contemporánea y cómoda) y **JetBrains Mono** (metadatos, ISBN, precios y etiquetas de archivo).
- Bordes sólidos de 2px, sombras duras sin desenfoque (`box-shadow: 4px 4px 0 var(--color-tinta)`), esquinas a 0px en paneles e inputs, esquinas a 4px en botones táctiles y tramas de fondo *screentone* generadas mediante degradados radiales repetitivos.
- **Contenido 100% original y coherente en español**: sin textos de relleno ni *lorem ipsum*. Títulos y autores de ficción ("Cyberpunk Edge", "Blade Soul", "Neo Tokyo Ghost", "Blood & Steel", etc.) con precios en formato USD `$14.99`.

---

## 2. Estructura de Archivos del Proyecto

```text
sitio-web/
│
├── index.html          # Página 1: Inicio (Hero destacado, 5 compromisos, 4 lanzamientos, editoriales, suscripción)
├── catalogo.html       # Página 2: Catálogo general (Mínimo 12 tarjetas en <article>, filtros visuales y CSS interno)
├── pagina3.html        # Página 3: Guía del Coleccionista (Demografías en <dl>, tabla comparativa, guía de lectura <ol>, FAQ en <details> y contacto)
│
├── css/
│   └── styles.css      # Hoja de estilos externa principal con variables, selectores comentados, Flexbox, Grid y Responsive
│
├── img/                # Directorio de recursos gráficos vectoriales SVG con licencia libre y sin derechos de autor
│   ├── logo.svg
│   ├── portada-hero.svg
│   ├── manga-01.svg a manga-12.svg
│   └── guia-lectura.svg
│
├── DESIGN.md           # Sistema de diseño con tokens de color, espaciado y tipografía
├── screen.png          # Maqueta gráfica de referencia
├── CAPTURAS.md         # Guía de archivos y líneas de código para capturas del PDF académico
└── README.md           # Documentación general y guía de despliegue
```

Todos los enlaces internos son **relativos** (`index.html`, `catalogo.html`, `pagina3.html`, `css/styles.css`, `img/...`) para garantizar funcionamiento inmediato tanto en local como en GitHub Pages bajo cualquier subdirectorio.

---

## 3. Páginas y Arquitectura Semántica HTML5

Las 3 páginas implementan un menú de navegación funcional común con el enlace activo resaltado (`class="enlace-activo" aria-current="page"`), jerarquía estricta de encabezados (`<h1>` único, `<h2>`, `<h3>`), y todas las etiquetas semánticas obligatorias:
- `<header>`: Logotipo, navegación y buscador funcional sin JS.
- `<nav>`: Enlaces entre las 3 páginas.
- `<main>`: Contenedor estructural del contenido propio de cada página.
- `<section>`: Divisiones temáticas principales con encabezados descriptivos.
- `<article>`: Tarjetas independientes de contenido y mangas.
- `<aside>`: Franja de editoriales asociadas (enlaces externos seguros con `rel="noopener noreferrer"`) y paneles laterales de filtro y notas técnicas.
- `<footer>`: Mapa del sitio, créditos institucionales, enlaces de recursos y derechos reservados.
- `<figure>` y `<figcaption>`: Para cada portada y para la infografía didáctica de lectura oriental.

---

## 4. Requisitos CSS Implementados

### 4.1 Los Tres Tipos de Hojas de Estilo
1. **CSS Externo:** Archivo `css/styles.css` vinculado mediante `<link rel="stylesheet" href="css/styles.css">` en las tres páginas.
2. **CSS Interno:** Bloque `<style>` dentro del `<head>` de `catalogo.html` con estilos exclusivos de las etiquetas (*HOT*, *SALE*, *NUEVO*, *OMNIBUS*) y del panel de filtrado.
3. **CSS En Línea:** Atributos `style=""` comentados individualmente con `<!-- CSS EN LÍNEA: ... -->` en `index.html` y `pagina3.html`.

### 4.2 Selectores Revisados en Clase (con comentarios destacados)
Cada selector cuenta con el formato exigido:
`/* ========== SELECTOR: <nombre> | Ejemplo: <regla> | Qué hace: <explicación breve> ========== */`
- **Universal:** `*` (reset, box-sizing: border-box)
- **Elemento:** `body`, `h1`, `h2`, `p`, `a`, `img`, `ul`, `table`
- **Clase:** `.tarjeta-manga`, `.boton-primario`, etc.
- **Id:** `#encabezado-sitio`, `#bloque-suscripcion`
- **Elemento + Clase:** `article.tarjeta-manga`, `p.descripcion-manga`, `a.boton-accion`
- **Agrupación (coma):** `h1, h2, h3, h4`
- **Combinadores:** Descendiente (`nav a`), Hijo directo (`ul > li`), Hermano adyacente (`h2 + p`), Hermano general (`h2 ~ p`)
- **Pseudoclases:** `:hover`, `:focus`, `:active`, `:link`, `:visited`, `:first-child`, `:last-child`, `:nth-child(2n)`
- **Pseudoelementos:** `::before`, `::after`, `::first-letter`, `::first-line`, `::marker`, `::selection`
- **Atributos:** `a[target]`, `input[type="text"]`, `input[type="email"]`, `a[href^="https"]`, `a[href$=".html"]`, `a[href*="manga"]`, `[class*="etiqueta"]`, `[class="boton-primario"]`
- **Especificidad:** Conflicto de especificidad resuelto y documentado sin uso de `!important`.
- **Modelo de Caja:** `margin`, `border`, `padding`, `width`, `height`.
- **Display:** `block`, `inline`, e `inline-block` comentados y aplicados.

### 4.3 Dos Técnicas de Maquetación
- **FLEXBOX (`/* ===== TÉCNICA DE MAQUETACIÓN 1: FLEXBOX ===== */`):** Header, navegación, botones del Hero, barra de precio/acción de las tarjetas, alineación de editoriales y pie de página.
- **CSS GRID (`/* ===== TÉCNICA DE MAQUETACIÓN 2: CSS GRID ===== */`):** Cuadrícula responsiva de 12 tarjetas en catálogo, layout del catálogo con aside lateral y cuadrícula de lanzamientos en inicio.

### 4.4 Variables CSS (:root)
Más de 15 variables en español para colores, fuentes, espaciado atómico (base 8px), sombras duras y radios de borde.

### 4.5 Diseño Responsivo (Mobile-First)
- **Móvil (< 600px):** Catálogo en 1 columna, navegación adaptable con `flex-wrap` sin JavaScript.
- **Tableta (>= 600px):** Catálogo en 2 columnas mediante `@media (min-width: 600px)`.
- **Escritorio (>= 1024px):** Catálogo en 3 columnas cumpliendo la rúbrica docente mediante `@media (min-width: 1024px)`.
- Sin desbordamiento horizontal garantizado en 360px, 768px y 1440px.

---

## 5. Cómo Ver el Sitio Localmente

### Opción 1: Abrir directamente en el navegador
1. Descarga o clona la carpeta `sitio-web`.
2. Haz doble clic en `index.html` para abrirlo en cualquier navegador web moderno (Google Chrome, Firefox, Edge, Safari).

### Opción 2: Usar un servidor local con Python
Si tienes Python instalado:
```bash
cd sitio-web
python -m http.server 8000
```
Luego abre tu navegador en: [http://localhost:8000](http://localhost:8000)

### Opción 3: Extensión Live Server de VS Code
1. Abre la carpeta `sitio-web` en Visual Studio Code.
2. Haz clic derecho sobre `index.html` y selecciona **"Open with Live Server"**.

---

## 6. Pasos para Publicar en GitHub Pages

1. **Crear repositorio en GitHub:**
   - Ingresa a [github.com](https://github.com) y crea un nuevo repositorio público (ejemplo: `sitio-web-manga-void`).

2. **Subir los archivos mediante Git:**
   Abre una terminal en la carpeta `sitio-web` y ejecuta:
   ```bash
   git init
   git add .
   git commit -m "Entrega: Sitio web Manga Void con HTML5 semántico y CSS3"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/sitio-web-manga-void.git
   git push -u origin main
   ```

3. **Activar GitHub Pages:**
   - En tu repositorio de GitHub, haz clic en la pestaña **Settings** (Configuración).
   - En el menú lateral izquierdo, haz clic en **Pages**.
   - En la sección **Build and deployment**:
     - **Source:** Selecciona `Deploy from a branch`.
     - **Branch:** Selecciona la rama `main` y en la carpeta mantén `/ (root)`.
     - Haz clic en **Save** (Guardar).

4. **Obtener la URL pública:**
   - Espera entre 1 y 2 minutos mientras se procesa la GitHub Action.
   - Recarga la página de Pages y verás un mensaje verde:
     `Your site is live at https://TU-USUARIO.github.io/sitio-web-manga-void/`
   - Copia esa URL para incluirla en la portada de tu informe PDF de la tarea.

---

## 7. Créditos y Licencias

- **Imágenes:** Ilustraciones vectoriales originales SVG desarrolladas para el proyecto con licencia abierta sin restricciones de autor.
- **Tipografías:** Anton (Vernon Adams, SIL Open Font License), Hanken Grotesk (Hanken Design Co., SIL Open Font License) y JetBrains Mono (JetBrains, Apache License 2.0) a través de Google Fonts.
- **Validación:** Código estructurado conforme a los estándares oficiales de la W3C (HTML5 y CSS3).
