# Extracto Importado · Manual de marca interactivo

Es una landing de una sola página que presenta la identidad, la voz y la forma de trabajo de **Extracto Importado**. Es un sitio estático (HTML, CSS y JavaScript) listo para GitHub Pages: no necesita backend ni claves de API.

Usa el mismo motor que el manual de Crisger: el contenido está en `data.json` y tiene editor local, modo presentación, editor de piezas, firma de correo y kit de descargas. Suma buscador, textos para copiar con filtros, glosario, descargas, plantillas de flyers y un generador de brief.

La estética es la de la marca: base blanca, títulos en mayúsculas espaciadas en Gotham Light y oro solo para acentos.

## Estructura

```
index.html      Estructura base, buscador, visor de imágenes y editor
fonts/          Gotham (licencia comercial, ver más abajo)
style.css       Diseño, colores de marca y responsive
app.js          Render desde data.json, interacciones, herramientas y editor
data.json       Todo el contenido editable del manual
media/          Logos en SVG, fotos de producto (fotos/), miniaturas de plantillas (plantillas/) e imagen para compartir
  descargas/    PNG de logos, ZIP de logos, ZIP de fotos, hoja membretada (Word y PDF), manual en PDF y catálogo
README.md
```

## Secciones

El manual está ordenado como lo recorre alguien que se suma al equipo o empieza a revender: primero la marca y el producto, después cómo se ve y cómo habla, y al final las herramientas.

1. **Marca**: qué es Extracto, conceptos, cifras, por qué nos eligen y públicos.
2. **Productos**: líneas (Parfum, Body Mist, Discovery set), descripción de cada formato, nomenclatura por código, packaging, cómo usarlo y cuidarlo, y descargas del catálogo y las fotos.
3. **Identidad**: logo con selector de versiones y fondos, espacio de protección, usos incorrectos, paleta, proporción de color, tonos, contraste, tipografía Gotham, jerarquía y tramas con el monograma.
4. **Fotografía**: criterios para fotografiar el producto y galería con las 12 fotos oficiales, filtrable por categoría.
5. **Voz**: principios, personalidad, cómo describir una fragancia, así sí / así no, palabras que usamos, familias olfativas, glosario con buscador y reglas de formato.
6. **Textos**: 36 textos listos para copiar, con buscador y filtros por etapa de la venta y por canal (primer contacto, consultas, objeciones, cierre, posventa, revendedores, redes, estados de WhatsApp y perfiles). Lo que va entre [corchetes] se resalta para completar.
7. **Ventas**: recorrido de la consulta a la posventa, canales copiables, envíos y pagos.
8. **Revendedores**: cómo empezar, qué ofrecemos y buenas prácticas.
9. **Pedidos**: plazos por tipo de pieza y un generador de brief completo. El brief chequea la fecha contra el plazo, avisa qué falta, se copia, se descarga en .txt o se envía por WhatsApp, y queda guardado como borrador en el navegador.
10. **Kit de marca**: logos en SVG y PNG, paleta, tipografía, **14 plantillas de flyers**, editor de piezas, firma de correo, hoja membretada, fotos, catálogo y manual en PDF.

El botón **Buscar** de la cabecera (o la tecla `/`) busca en todo el manual.

## Plantillas de flyers

Hay 14 plantillas listas: lanzamiento, best seller, promo por cantidad, fecha especial, Body Mist, banner web, envíos, cuotas sin interés, sumate a Vende Extracto, llegó stock, cultura olfativa, reseña de cliente, aviso y sorteo.

- **Cómo se usan:** al tocar una plantilla se carga en el editor con su formato, estructura, color, textos y foto de fondo. Desde ahí se cambian los textos, la foto (subiendo una propia o eligiendo una de las oficiales) y el encuadre, y se descarga en PNG.
- **Formatos:** publicación 1080 × 1350, cuadrado 1080 × 1080, historia 1080 × 1920 y banner web 1440 × 360.
- **Estructuras:** Etiqueta (una tarjeta con marco fino, como la del frasco), Marco, Clásica, Centrada y Panel.
- **Colores:** Blanco, Niebla y Negro. Los títulos van siempre en mayúsculas espaciadas, con un filete dorado.
- **Miniaturas:** están en `media/plantillas/`. Si cambiás una plantilla en `app.js` (constante `TPL_PRESETS`), la miniatura vieja sigue ahí hasta que la reemplaces.

## Catálogo

El bloque de descargas de Productos y el kit apuntan a `media/descargas/extracto-catalogo.pdf`. Cuando subas el catálogo con ese nombre, el botón se activa solo; mientras no esté, muestra «Pendiente de carga».

## Logo

El logo principal sale del archivo oficial: se vectorizó en SVG en color, en blanco y en versión monocromática. El original en PNG está en `media/descargas/png/logo-extracto-original.png`.

El **monograma** (una E espejada junto a una E) se reconstruyó a partir del que aparece en el Body Mist, con la E del logo. Las versiones **vertical** y **compacta** combinan el monograma con el logo. Validalas con la diseñadora antes de producir. Para reemplazar cualquier versión, cambiá el archivo en `media/` (mismo nombre) o usá la pestaña **Logos** del editor.

## Fotos

Las fotos para la web están en `media/fotos/` (WebP, 1600 px). Las versiones en alta para descargar están en `media/descargas/extracto-fotos-producto.zip`.

## Tipografía: Gotham

El sitio usa **Gotham** (Thin a Ultra) desde la carpeta `fonts/`: Light para titulares, Book para textos y Medium para etiquetas. Si falta, usa Montserrat o Helvetica como reemplazo.

**Importante sobre la licencia:** Gotham es una tipografía comercial (Hoefler&Co). Si el repositorio es **público**, los archivos de `fonts/` quedan descargables por cualquiera, y eso requiere una licencia web de Gotham. Si la empresa no la tiene, conviene alguna de estas opciones:

- Publicar desde un repositorio **privado**. GitHub Pages desde repositorios privados requiere un plan pago.
- Borrar la carpeta `fonts/` antes de subir el sitio. En ese caso se verá con Montserrat o Helvetica.
- Comprar la licencia web.

El kit de descargas **no** ofrece los archivos de Gotham: indica que se piden al equipo de diseño.

## Publicar en GitHub Pages

1. Creá un repositorio en GitHub (por ejemplo, `extracto-manual`).
2. Descomprimí el ZIP y subí **el contenido** de la carpeta a la raíz del repositorio. `index.html` tiene que quedar en la raíz, no dentro de otra carpeta.
   - **En la web de GitHub:** usá **Add file → Upload files**, arrastrá `index.html`, `style.css`, `app.js`, `data.json`, `README.md` y las carpetas `media` y `fonts`, y confirmá con **Commit changes**.
   - **Por terminal:**
     ```bash
     git init
     git add .
     git commit -m "Manual de marca Extracto Importado"
     git branch -M main
     git remote add origin https://github.com/USUARIO/extracto-manual.git
     git push -u origin main
     ```
3. En el repositorio, abrí **Settings → Pages**.
4. En **Build and deployment → Source**, elegí **Deploy from a branch**.
5. En **Branch**, seleccioná `main` y la carpeta `/ (root)`, y guardá con **Save**.
6. Esperá uno o dos minutos. La dirección aparece arriba en esa misma pantalla (`https://USUARIO.github.io/extracto-manual/`).

Todas las rutas son relativas, así que el sitio funciona tanto en GitHub Pages como en un dominio propio.

### Revisión local

Los navegadores bloquean la lectura de `data.json` cuando se abre `index.html` con doble clic. Para probarlo en tu computadora, ejecutá esto dentro de la carpeta:

```bash
python -m http.server 8000
```

Después abrí `http://localhost:8000`.

## Editar el contenido

El botón **Editar contenido** está oculto para los visitantes. Para verlo, abrí el sitio con `?editar` al final de la dirección, por ejemplo `https://USUARIO.github.io/extracto-manual/?editar`. El botón aparece en el pie y queda recordado en ese navegador. Para ocultarlo, abrí la dirección con `?editar=0`.

El editor tiene cinco pestañas:

- **Portada:** textos generales y del kit.
- **Secciones.**
- **Bloques.**
- **Colores:** el primer color define el acento de toda la interfaz.
- **Logos.**

En **Bloques**, el campo **Lista** controla el contenido de las herramientas:

| Bloque | Formato de cada línea |
| --- | --- |
| Cifras destacadas | `Valor — Etiqueta — Detalle` |
| Tarjetas | `Título — Texto` |
| Tabla | Columnas separadas con `|`. La primera línea es el encabezado. |
| Catálogo con vista de pauta | Como la tabla. La 3.ª columna (equivalencia) se oculta en la vista para anuncios pagos. |
| Así sí / así no | `Así sí || Así no`. Para cambiar los títulos, primera línea `# Somos || No somos` |
| Vocabulario | Una palabra o expresión por línea |
| Glosario con buscador | `Término — Definición` |
| Descargas | `Nombre | ruta del archivo | detalle` |
| Canales copiables | `Canal | Dato para copiar | Nota` |
| Pasos de un proceso | `Título — Texto` |
| Textos para copiar | `Categoría | Título — Texto` |
| Usos incorrectos | Un ejemplo por línea. Reconoce: color, contorno, forma, volumen, sombra, reflejar, comprimir, expandir y rotar. |
| Jerarquía tipográfica | `Referencia — Texto de ejemplo` |


### Cómo se guardan los cambios

- Los cambios del editor se guardan solo en **ese navegador**. El sitio publicado no cambia.
- **Exportar data.json** descarga el contenido actual.
- **Importar JSON** carga un archivo guardado antes.
- **Restaurar versión publicada** borra los cambios locales.
- El borrador del brief y la firma de correo también quedan guardados en el navegador de cada persona.

### Publicar una actualización

1. Editá el contenido desde el panel.
2. Pulsá **Exportar data.json**.
3. En GitHub, reemplazá `data.json` por el archivo exportado y confirmá con **Commit changes**.
4. Cuando termine la publicación, usá **Restaurar versión publicada** en tu navegador.

Las imágenes que se suben desde el editor quedan incrustadas en el JSON. Para imágenes definitivas conviene subirlas a `media/` y escribir su ruta.

## Carpeta de Google Drive (opcional)

El generador de piezas puede mostrar como fondos las imágenes y los videos de una carpeta de Google Drive compartida. Los pasos son:

1. Compartí la carpeta como **Cualquier persona con el enlace → Lector**.
2. Creá una clave de la **Google Drive API** en [console.cloud.google.com](https://console.cloud.google.com), restringida a tu sitio (`https://USUARIO.github.io/*`) y solo a esa API.
3. Pegá el enlace de la carpeta y la clave en el editor (pestaña **Portada → Google Drive**) y exportá `data.json`.

## Videos en el generador

Acepta videos MP4, WebM o MOV de hasta 50 MB y exporta un tramo de 3 a 15 segundos, sin sonido. Chrome, Edge y Safari exportan en MP4; otros navegadores, en WebM.

## Modo presentación

El botón **Presentar** pone el manual en pantalla completa y lo recorre bloque por bloque:

- **Avanzar:** flechas, barra espaciadora o deslizar en pantallas táctiles.
- **Salir:** Esc.

## Vista previa al compartir

Al compartir el enlace aparece una tarjeta con `media/og-extracto.jpg`. Para máxima compatibilidad, en `index.html` reemplazá `media/og-extracto.jpg` (dos veces) por la dirección completa publicada.

## Manual en PDF

`media/descargas/extracto-manual-de-marca.pdf` es una versión en A4 horizontal. Si cambiás el contenido, hay que generar una nueva:

1. Abrí el sitio en Chrome y elegí **Imprimir → Guardar como PDF**, con márgenes **Ninguno** y **Gráficos de fondo** activado.
2. Reemplazá el archivo en `media/descargas`.

## Si no ves los cambios

1. En la pestaña **Actions** del repositorio, esperá la tilde verde de «pages build and deployment».
2. Revisá que `index.html`, `app.js`, `style.css` y `data.json` estén en la raíz.
3. Forzá la recarga con `Ctrl + Shift + R` (Windows) o `Cmd + Shift + R` (Mac).
4. `index.html` carga `style.css` y `app.js` con un número de versión (`?v=...`). Si los modificás a mano, cambiá ese número.

## Criterios de marca

- **Colores:**
  - Blanco `#FFFFFF`: la base.
  - Blanco niebla `#F4F3F0`.
  - Gris piedra `#C9C7C2`.
  - Grafito `#3A3A38`.
  - Negro `#050505`.
  - Oro `#C89210`: solo para acentos, como filetes, etiquetas y detalles, nunca de fondo.
- **Tipografía:** Gotham. Light en mayúsculas espaciadas para títulos, Book para textos y Medium para etiquetas y botones.
- **Pauta:** en anuncios pagos no se nombran marcas originales; se comunica por código y notas.
- **Propuestas a validar:** los plazos de reel, campaña y producción de fotos, y las decisiones de operación.
