# GUÍA OFICIAL DE CAPTURAS PARA EL INFORME EN PDF
**Universidad de Guayaquil — Desarrollo de Aplicaciones Web**  
**Docente:** Mgtr. Karla Yadira Abad Sacoto  
**Estudiante:** Marco Córdova Rivera  

Este documento lista la ubicación exacta (archivo y número de línea) de cada elemento evaluado en la rúbrica docente para que tomes las capturas de pantalla de tu editor de código y de la web para el informe final en formato PDF.

---

## 1. Capturas de los Tres Tipos de Hojas de Estilo

| Tipo de CSS | Archivo | Líneas aprox. | Comentario / Código para capturar |
| :--- | :--- | :--- | :--- |
| **CSS EXTERNO** | `css/styles.css` | Línea 8 | `/* ===== CSS EXTERNO: Vinculado mediante <link rel="stylesheet" href="css/styles.css"> ===== */` |
| **Enlace Externo** | `index.html` | Línea 8-10 | `<!-- CSS EXTERNO: Hoja de estilos principal del proyecto -->`<br>`<link rel="stylesheet" href="css/styles.css">` |
| **CSS INTERNO** | `catalogo.html` | Líneas 16-95 | `<!-- CSS INTERNO: Estilos específicos para catálogo, filtros y etiquetas -->`<br>Bloque `<style> ... </style>` dentro del `<head>` |
| **CSS EN LÍNEA 1** | `index.html` | Línea 57-59 | `<!-- CSS EN LÍNEA: Destaca el fondo carmesí y bordes de la etiqueta de edición especial -->`<br>`style="background-color: #b7102a; color: #ffffff; ..."` |
| **CSS EN LÍNEA 2** | `index.html` | Línea 70-71 | `<!-- CSS EN LÍNEA: Establece un espaciado entre letras distintivo y borde reforzado en el botón de vista previa -->`<br>`style="letter-spacing: 1.5px; border-width: 2px;"` |
| **CSS EN LÍNEA 3** | `pagina3.html` | Línea 110-112 | `<!-- CSS EN LÍNEA: Fija el ancho exacto y estilo destacado para la columna de tipo de edición -->`<br>`style="width: 24%; background-color: #dce5d9; text-transform: uppercase;"` |
| **CSS EN LÍNEA 4** | `pagina3.html` | Línea 215-217 | `<!-- CSS EN LÍNEA: Aplica un borde lateral carmesí de 6px y fondo verde tenue para enfatizar la advertencia -->`<br>`style="border-left: 6px solid #b7102a; ..."` |

---

## 2. Capturas de Selectores CSS (Archivo `css/styles.css`)

Todos los selectores tienen el encabezado destacado obligatorio:  
`/* ========== SELECTOR: <nombre> | Ejemplo: <regla> | Qué hace: <explicación breve> ========== */`

| # | Categoría de Selector | Línea aprox. | Ejemplo de Regla | Qué hace (resumen) |
| :---: | :--- | :--- | :--- | :--- |
| **1** | **Universal** | Línea 85 | `*`, `*::before`, `*::after` | Reset general y `box-sizing: border-box`. |
| **2** | **Elemento** | Línea 94 | `body` | Configura tipografía base, color y screentone. |
| **2b** | **Elemento** | Líneas 120-165 | `h1`, `h2`, `h3`, `p`, `a`, `img`, `ul`, `table` | Estilos base para elementos de texto y tablas. |
| **3** | **Clase** | Línea 173 | `.tarjeta-manga` | Borde de 2px, esquinas a 0px y sombra dura. |
| **3b** | **Clase** | Línea 186 | `.boton-primario` | Botón carmesí con esquinas a 4px y sombra dura. |
| **4** | **Id** | Línea 203 | `#encabezado-sitio` | Fija el header superior con sombra sólida. |
| **4b** | **Id** | Línea 214 | `#bloque-suscripcion` | Bloque oscuro inverso con borde superior rojo. |
| **5** | **Elemento + Clase** | Línea 224 | `article.tarjeta-manga` | Especificidad alta para tarjetas artículo. |
| **5b** | **Elemento + Clase** | Línea 229 | `p.descripcion-manga` | Formato al párrafo de sinopsis del manga. |
| **5c** | **Elemento + Clase** | Línea 238 | `a.boton-accion` | Enlace con apariencia de botón secundario. |
| **6** | **Agrupación (coma)** | Línea 111 | `h1, h2, h3, h4` | Unifica la fuente Anton en titulares. |
| **7** | **Combinador Descendiente** | Línea 252 | `nav a` | Enlaces contenidos dentro del nav. |
| **7b** | **Combinador Hijo Directo** | Línea 261 | `ul.lista-beneficios > li` | Elementos `li` hijos directos de la lista. |
| **7c** | **Combinador Hermano Adyacente** | Línea 269 | `h2 + p.subtitulo-seccion` | Párrafo inmediatamente posterior a un h2. |
| **7d** | **Combinador Hermano General** | Línea 277 | `.contenido-articulo h2 ~ p` | Párrafos subsiguientes a un h2. |
| **8** | **Pseudoclase :hover** | Línea 283 | `.tarjeta-manga:hover` | Efecto pop desplazando 4px arriba-izquierda. |
| **8b** | **Pseudoclase :focus** | Línea 289 | `input:focus`, `textarea:focus` | Borde rojo primario y halo accesible. |
| **8c** | **Pseudoclase :active** | Línea 298 | `.boton-primario:active` | Efecto de botón presionado al hacer clic. |
| **8d** | **Pseudoclase :link** | Línea 305 | `.enlace-destacado:link` | Enlaces aún no visitados. |
| **8e** | **Pseudoclase :visited** | Línea 311 | `.enlace-destacado:visited` | Enlaces ya visitados. |
| **8f** | **Pseudoclase :first-child** | Línea 316 | `ul.lista-beneficios > li:first-child` | Resalta el primer beneficio en negrita. |
| **8g** | **Pseudoclase :last-child** | Línea 321 | `.columna-informacion > p:last-child` | Quita el margen al último elemento. |
| **8h** | **Pseudoclase :nth-child** | Línea 326 | `table tbody tr:nth-child(2n)` | Filas alternadas cebra en la tabla. |
| **9** | **Pseudoelemento ::before** | Línea 331 | `ul.lista-beneficios > li::before` | Inserta viñeta de cuadrado rojo manga (■). |
| **9b** | **Pseudoelemento ::after** | Línea 341 | `a.enlace-con-flecha::after` | Inserta flecha dinámica (→) que se desplaza. |
| **9c** | **Pseudoelemento ::first-letter** | Línea 352 | `p.parrafo-capitular::first-letter` | Letra capital de 3.2rem al inicio de la guía. |
| **9d** | **Pseudoelemento ::first-line** | Línea 362 | `p.parrafo-destacado::first-line` | Primera línea estilizada en mayúsculas. |
| **9e** | **Pseudoelemento ::marker** | Línea 369 | `ol.lista-pasos-lectura li::marker` | Números rojos estilizados en la lista de lectura. |
| **9f** | **Pseudoelemento ::selection** | Línea 376 | `::selection` | Fondo carmesí al seleccionar texto. |
| **10** | **Atributo [target]** | Línea 382 | `a[target="_blank"]` | Cursor alias en enlaces externos. |
| **10b** | **Atributo [type="text"]** | Línea 387 | `input[type="text"]`, `input[type="search"]` | Estilo uniforme para campos de texto. |
| **10c** | **Atributo [type="email"]** | Línea 398 | `input[type="email"]` | Campo de correo con tipografía monoespaciada. |
| **10d** | **Atributo [href^="https"]** | Línea 408 | `a[href^="https"]` | Detecta enlaces externos seguros. |
| **10e** | **Atributo [href$=".html"]** | Línea 413 | `a[href$=".html"]` | Identifica enlaces a páginas HTML internas. |
| **10f** | **Atributo [href*="manga"]** | Línea 418 | `a[href*="manga"]` | Enlaces que contienen la palabra manga. |
| **10g** | **Atributo [class*="etiqueta"]**| Línea 423 | `[class*="etiqueta"]` | Formato tipográfico a todas las etiquetas. |
| **10h** | **Atributo [class="..."]** | Línea 432 | `[class="boton-primario"]` | Coincidencia exacta por atributo de clase. |

---

## 3. Capturas de Especificidad, Modelo de Caja y Display

- **Especificidad y Conflicto Resuelto:**
  - Archivo: `css/styles.css`
  - Líneas: 69-80
  - Ejemplo comentado: `article.tarjeta-manga p.descripcion-manga` (0-0-2-2) vs `.tarjeta-manga p` (0-0-1-1). Explica por qué no se requiere `!important`.
- **Modelo de Caja y Propiedades Display:**
  - Archivo: `css/styles.css`
  - Líneas: 438-478
  - Comenta `margin`, `border`, `padding`, `width`, `height`, y el uso de `display: block`, `display: inline-block` (en etiquetas y chips) y `display: inline`.

---

## 4. Capturas de las Dos Técnicas de Maquetación

### Técnica 1: Flexbox
- **Archivo:** `css/styles.css`
- **Líneas:** 480-705
- **Sección:** `/* ===== TÉCNICA DE MAQUETACIÓN 1: FLEXBOX ===== */`
- **Elementos donde se aplica:**
  1. Barra de navegación y header (`.barra-navegacion`, `.menu-principal`).
  2. Hero layout (`.bloque-hero`, `.botones-hero`).
  3. Barra de precio y botón de compra de cada tarjeta (`.pie-tarjeta-manga`).
  4. Franja de editoriales y aliados internacionales (`.editoriales-lista`).
  5. Formulario del boletín de suscripción (`.formulario-suscripcion`).
  6. Columnas del pie de página (`.pie-de-pagina`, `.footer-columnas`).

### Técnica 2: CSS Grid
- **Archivo:** `css/styles.css`
- **Líneas:** 707-775
- **Sección:** `/* ===== TÉCNICA DE MAQUETACIÓN 2: CSS GRID ===== */`
- **Elementos donde se aplica:**
  1. Cuadrícula de 12 tarjetas en el catálogo (`.cuadricula-catalogo`).
  2. Cuadrícula de 4 tarjetas en inicio (`.cuadricula-lanzamientos`).
  3. Layout principal de dos columnas en catálogo (`.layout-catalogo`: Aside lateral + Cuadrícula de productos).

---

## 5. Capturas de Variables CSS y Diseño Responsivo (Mobile-First)

- **Variables CSS (:root):**
  - Archivo: `css/styles.css`
  - Líneas: 22-65
  - Define más de 15 variables: colores carmesí, tinta, papel, fuentes Anton, Hanken Grotesk, JetBrains Mono, espaciado base 8px, sombras duras y radios.
- **Diseño Responsivo con Media Queries:**
  - Archivo: `css/styles.css`
  - Líneas: 875-965
  - **Móvil (< 600px):** 1 columna (regla base sin media query).
  - **Tableta (`@media (min-width: 600px)`):** 2 columnas (`.cuadricula-catalogo { grid-template-columns: repeat(2, 1fr); }`).
  - **Escritorio (`@media (min-width: 1024px)`):** 3 columnas cumpliendo la rúbrica docente (`.cuadricula-catalogo { grid-template-columns: repeat(3, 1fr); }`).

---

## 6. Capturas de Validación W3C (HTML5 y CSS3)

La profesora evalúa que el sitio esté validado formalmente en el Consorcio W3C:

1. Ingresa a: [https://validator.w3.org/#validate_by_input](https://validator.w3.org/#validate_by_input)
2. Pega el código completo o sube los archivos uno por uno:
   - `index.html` -> Resultado esperado: **"Document checking completed. No errors or warnings to show."** (Verde).
   - `catalogo.html` -> Resultado esperado: **"Document checking completed. No errors or warnings to show."** (Verde).
   - `pagina3.html` -> Resultado esperado: **"Document checking completed. No errors or warnings to show."** (Verde).
3. Ingresa al validador de CSS: [https://jigsaw.w3.org/css-validator/#validate_by_input](https://jigsaw.w3.org/css-validator/#validate_by_input)
   - Valida `css/styles.css` -> Resultado esperado: **"Felicidades! No se han encontrado errores."** (Verde).
4. Toma captura completa de cada pantalla donde se vea el mensaje verde de éxito y la URL del validador.

---

## 7. Capturas de Vistas Web (Navegador)

Para armar el PDF, toma capturas de:
1. **Página de Inicio (`index.html`) en Escritorio (1440px):**
   - Header + Hero con edición de colección.
   - Sección de 5 compromisos.
   - Sección de 4 últimos lanzamientos + franja de editoriales + newsletter + footer.
2. **Página de Catálogo (`catalogo.html`) en Escritorio (1440px):**
   - Aside lateral de filtros + 3 columnas de tarjetas (12 tomos).
3. **Página de Guía del Coleccionista (`pagina3.html`) en Escritorio (1440px):**
   - Glosario de demografías (`<dl>`).
   - Tabla comparativa de formatos.
   - Infografía didáctica de lectura oriental (`<ol>` + `<figure>`).
   - Acordeón de preguntas frecuentes (`<details>`) y formulario de contacto.
4. **Vistas Móviles (360px - 400px):**
   - Abre la herramienta de desarrollador (`F12` en Chrome/Edge o `Ctrl+Shift+M` para modo responsive).
   - Captura el menú reorganizado, el catálogo en 1 sola columna y el formulario de suscripción.

---

## 8. Checklist Final para Entrega del PDF

- [x] Repositorio de GitHub creado y código subido.
- [x] GitHub Pages activo con enlace público funcional.
- [x] URL del repositorio y URL de GitHub Pages colocadas en la carátula del informe.
- [x] Capturas de los 3 tipos de CSS (Externo, Interno, En línea).
- [x] Capturas de los selectores clasificados por categoría con sus comentarios.
- [x] Capturas de Flexbox y CSS Grid.
- [x] Capturas de las 3 páginas en versión Escritorio y Móvil.
- [x] Capturas de las validaciones W3C en verde para los 3 archivos HTML y el archivo CSS.
- [x] Fecha de entrega: Hasta el **8 de noviembre de 2026**.
