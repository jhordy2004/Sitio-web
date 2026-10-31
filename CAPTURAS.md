# GUÍA OFICIAL DE CAPTURAS PARA EL INFORME EN PDF
**Universidad de Guayaquil — Desarrollo de Aplicaciones Web**  
**Docente:** Mgtr. Karla Yadira Abad Sacoto  
**Estudiante:** Marco Córdova Rivera  

Este documento lista la ubicación exacta (archivo y número de línea) de cada elemento evaluado en la rúbrica docente para que tomes las capturas de pantalla de tu editor de código y del navegador web para el informe final en formato PDF.

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
| **4** | **Id** | Línea 203 | `#encabezado-principal` | Fija el header superior con position sticky, z-index 100 y borde inferior sólido de 4px color tinta. |
| **4b** | **Id** | Línea 215 | `#bloque-suscripcion` | Bloque oscuro inverso con borde superior rojo. |
| **5** | **Elemento + Clase** | Línea 225 | `article.tarjeta-manga` | Especificidad alta para tarjetas artículo. |
| **5b** | **Elemento + Clase** | Línea 230 | `p.descripcion-manga` | Formato al párrafo de sinopsis del manga. |
| **5c** | **Elemento + Clase** | Línea 239 | `a.boton-accion` | Enlace con apariencia de botón secundario. |
| **6** | **Agrupación (coma)** | Línea 111 | `h1, h2, h3, h4` | Unifica la fuente Anton en titulares. |
| **7** | **Combinador Descendiente** | Línea 253 | `nav a` | Enlaces contenidos dentro del nav. |
| **7b** | **Combinador Hijo Directo (header)** | Línea 1144 | `.menu > ul` | Aplica orientación en columna y espaciado vertical en el menú móvil. |
| **7c** | **Combinador Hijo Directo (lista)** | Línea 251 | `ul.lista-beneficios > li` | Elementos `li` hijos directos de la lista. |
| **7d** | **Combinador Hermano Adyacente (foco)**| Línea 1032 | `.menu-toggle:focus-visible + .menu-boton` | Indicador de foco accesible al botón hamburguesa con teclado. |
| **7e** | **Combinador Hermano Adyacente (texto)**| Línea 259 | `h2 + p.subtitulo-seccion` | Párrafo inmediatamente posterior a un h2. |
| **7f** | **Combinador Hermano General (menú)** | Línea 1078 | `.menu-toggle:checked ~ .encabezado__panel` | Despliega el panel del encabezado (buscador y menú) al marcarse el checkbox ☰ sin JS. |
| **7g** | **Combinador Hermano General (texto)**| Línea 267 | `.contenido-articulo h2 ~ p` | Párrafos subsiguientes a un h2. |
| **8** | **Pseudoclase :hover** | Líneas 1056, 1128, 1172 | `.menu a:hover`, `.menu-boton:hover`, `.buscador button:hover` | Efectos hover destacados en menú, botón hamburguesa y búsqueda. |
| **8b** | **Pseudoclase :focus** | Línea 1106 | `.buscador input[type="search"]:focus` | Ilumina el borde del input a rojo primario sin variar los 44px de altura. |
| **8c** | **Pseudoclase :focus-visible** | Línea 1027 | `.menu-toggle:focus-visible` | Mantiene accesible por teclado el interruptor oculto del menú. |
| **8d** | **Pseudoclase :checked** | Línea 1062 | `.menu-toggle:checked + .menu-boton` | Activa fondo rojo en botón hamburguesa cuando el menú está abierto. |
| **8e** | **Pseudoclase :active** | Línea 299 | `.boton-primario:active` | Efecto de botón presionado al hacer clic. |
| **8f** | **Pseudoclase :link** | Línea 306 | `.enlace-destacado:link` | Enlaces aún no visitados. |
| **8g** | **Pseudoclase :visited** | Línea 312 | `.enlace-destacado:visited` | Enlaces ya visitados. |
| **8h** | **Pseudoclase :first-child** | Línea 317 | `ul.lista-beneficios > li:first-child` | Resalta el primer beneficio en negrita. |
| **8i** | **Pseudoclase :last-child** | Línea 322 | `.columna-informacion > p:last-child` | Quita el margen al último elemento. |
| **8j** | **Pseudoclase :nth-child** | Línea 327 | `table tbody tr:nth-child(2n)` | Filas alternadas cebra en la tabla. |
| **9** | **Pseudoelemento ::before** | Línea 332 | `ul.lista-beneficios > li::before` | Inserta viñeta de cuadrado rojo manga (■). |
| **9b** | **Pseudoelemento ::after** | Línea 342 | `a.enlace-con-flecha::after` | Inserta flecha dinámica (→) que se desplaza. |
| **9c** | **Pseudoelemento ::first-letter** | Línea 353 | `p.parrafo-capitular::first-letter` | Letra capital de 3.2rem al inicio de la guía. |
| **9d** | **Pseudoelemento ::first-line** | Línea 363 | `p.parrafo-destacado::first-line` | Primera línea estilizada en mayúsculas. |
| **9e** | **Pseudoelemento ::marker** | Línea 370 | `ol.lista-pasos-lectura li::marker` | Números rojos estilizados en la lista de lectura. |
| **9f** | **Pseudoelemento ::selection** | Línea 377 | `::selection` | Fondo carmesí al seleccionar texto. |
| **10** | **Atributo [aria-current]** | Línea 1180 | `a[aria-current="page"]` | Resalta el enlace activo en rojo con borde inferior de 3px. |
| **10b** | **Atributo [type="search"]** | Línea 1091 | `.buscador input[type="search"]` | Altura exacta de 44px, borde sólido y min-width: 0 anti-desbordamiento. |
| **10c** | **Atributo [target]** | Línea 383 | `a[target="_blank"]` | Cursor alias en enlaces externos. |
| **10d** | **Atributo [type="text"]** | Línea 388 | `input[type="text"]` | Estilo uniforme para campos de texto. |
| **10e** | **Atributo [type="email"]** | Línea 399 | `input[type="email"]` | Campo de correo con tipografía monoespaciada. |
| **10f** | **Atributo [href^="https"]** | Línea 409 | `a[href^="https"]` | Detecta enlaces externos seguros. |
| **10g** | **Atributo [href$=".html"]** | Línea 414 | `a[href$=".html"]` | Identifica enlaces a páginas HTML internas. |
| **10h** | **Atributo [href*="manga"]** | Línea 419 | `a[href*="manga"]` | Enlaces que contienen la palabra manga. |
| **10i** | **Atributo [class*="etiqueta"]**| Línea 424 | `[class*="etiqueta"]` | Formato tipográfico a todas las etiquetas. |
| **10j** | **Atributo [class="..."]** | Línea 433 | `[class="boton-primario"]` | Coincidencia exacta por atributo de clase. |

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

## 4. Capturas de las Técnicas de Maquetación

### Técnica 1: Flexbox
- **Archivo:** `css/styles.css`
- **Secciones comentadas:**
  - `/* ===== TÉCNICA DE MAQUETACIÓN 1: FLEXBOX ===== */` (Línea 472)
  - `/* ===== TÉCNICA DE MAQUETACIÓN: FLEXBOX (header) ===== */` (Línea 982)
- **Elementos donde se aplica:**
  1. Header y navegación (.encabezado__contenido, .encabezado__panel, .menu, .buscador, .logo).
  2. Hero layout (`.bloque-hero`, `.botones-hero`).
  3. Barra de precio y botón de compra de cada tarjeta (`.pie-tarjeta-manga`).
  4. Franja de editoriales y aliados internacionales (`.editoriales-lista`).
  5. Formulario del boletín de suscripción (`.formulario-suscripcion`).
  6. Columnas del pie de página (`.pie-de-pagina`, `.footer-columnas`).

### Técnica 2: CSS Grid
- **Archivo:** `css/styles.css`
- **Sección comentada:** `/* ===== TÉCNICA DE MAQUETACIÓN 2: CSS GRID ===== */` (Línea 654)
- **Elementos donde se aplica:**
  1. Cuadrícula de 12 tarjetas en el catálogo (`.cuadricula-catalogo`).
  2. Cuadrícula de 4 tarjetas en inicio (`.cuadricula-lanzamientos`).
  3. Layout principal de dos columnas en catálogo (`.layout-catalogo`: Aside lateral + Cuadrícula de productos).

---

## 5. Capturas de Diseño Responsivo y Media Queries

- **Variables CSS (:root):**
  - Archivo: `css/styles.css` | Líneas: 22-65
  - Define más de 15 variables: colores carmesí, tinta, papel, fuentes Anton, Hanken Grotesk, JetBrains Mono, espaciado base 8px, sombras duras y radios.
- **Media Queries para el Encabezado y Catálogo:**
  - **Móvil (< 900px):** Reglas base por defecto (Líneas 982-1199). Barra superior con Logo a la izquierda y botón ☰ a la derecha (`justify-content: space-between`). Panel oculto por defecto que se despliega verticalmente al marcar el checkbox ☰ sin JS: buscador arriba (order 1) y enlaces abajo (order 2).
  - **Catálogo Tableta (`@media (min-width: 600px)`):**
    - Archivo: `css/styles.css` | Línea 892
    - Cuadrícula del catálogo a 2 columnas.
  - **Catálogo y Layout Escritorio (`@media (min-width: 1024px)`):**
    - Archivo: `css/styles.css` | Línea 928
    - Cuadrícula del catálogo a 3 columnas y layout en 2 columnas con aside lateral.
  - **Encabezado Escritorio (`/* ===== MEDIA QUERY ESCRITORIO (≥ 900px) ===== */`):**
    - Archivo: `css/styles.css` | Línea 1201
    - UNA sola fila horizontal: Logo a la izquierda, menú centrado (`Inicio`, `Catálogo`, `Guía del Coleccionista`) y buscador a la derecha (ancho 300px), todo alineado verticalmente al centro. Botón ☰ oculto (`display: none`).

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
1. **Página de Inicio (`index.html`) en Escritorio (≥1024px / 1440px):**
   - Header en UNA sola fila (logo izquierda, menú centrado, buscador 300px derecha con input y botón perfectamente alineados a 44px).
   - Hero con edición de colección.
   - Sección de 5 compromisos.
   - Sección de lanzamientos + franja de editoriales + newsletter + footer.
2. **Página en Tableta (768px–1023px):**
   - Fila 1: Logo + Menú horizontal.
   - Fila 2: Buscador a ancho completo.
3. **Página en Móvil (<768px):**
   - Fila 1: Logo + Botón hamburguesa (☰).
   - Menú desplegado en vertical al tocar el botón ☰.
   - Buscador a todo el ancho debajo.
4. **Página de Catálogo (`catalogo.html`):**
   - Aside lateral de filtros + cuadrícula de 12 tarjetas en `<article>`.
5. **Página de Guía del Coleccionista (`pagina3.html`):**
   - Glosario de demografías (`<dl>`), tabla comparativa, infografía de lectura (`<ol>` + `<figure>`), acordeón FAQ (`<details>`) y formulario de contacto.
