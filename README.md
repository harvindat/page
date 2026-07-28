# Balatas y Refacciones Rodríguez — Landing Page

Landing page premium, responsiva y de una sola página para la refaccionaria
**Balatas y Refacciones Rodríguez** (Durango). HTML, CSS y JavaScript puros,
sin frameworks ni pasos de build.

## Dos versiones (elige una)

El proyecto incluye **dos temas** con el mismo contenido y comportamiento, para que
compares y decidas cuál publicar:

- **`index.html`** — versión clara (azul marino + rojo sobre fondo claro).
- **`index-carbon.html`** — versión carbon: negro elegante con acentos de **azul neón**
  y **rojo** de la marca, glass oscuro, hairlines neón, glows y mapa en modo oscuro.

Cada versión tiene abajo a la izquierda un botón para saltar a la otra ("Versión carbon" /
"Versión clara"), así comparas al instante. Cuando decidas, publica solo el archivo que
prefieras (renómbralo a `index.html` si eliges la carbon).

## Qué incluye

- Diseño minimalista y sofisticado con la paleta de la marca (azul marino `#0A1F4D`
  + rojo `#DA1F26`) como único color de acento. Tipografía Saira (títulos) + Manrope (texto).
- Superficies de vidrio ligero (glassmorphism), bordes finos, sombras tintadas en azul
  y microinteracciones con transiciones spring.
- Logo vectorial (SVG) embebido en encabezado y pie.
- Hero con disco de freno animado dentro de un marco de doble bisel.
- Seccion de **Marcas** con un muro animado (marquesina infinita de 3 filas, con
  pausa al pasar el cursor) que muestra el catalogo completo de logos de
  distribuidores; funciona igual en la version clara y en la carbon.
- Secciones: Nosotros (Mision/Vision), Valores (bento), Servicios, Opiniones y Contacto.
- Seccion de **Opiniones** de clientes (testimonios).
- **Soso**, la mascota bujia interactiva: sigue el cursor, se puede arrastrar entre
  esquinas y rota consejos. En este rediseno se redujo un 15% de tamano.
- Boton de WhatsApp, mapa de ubicacion embebido y enlace a Facebook.
- SEO: metadatos, Open Graph, JSON-LD `AutoPartsStore`, favicon SVG.
- Accesible: navegacion por teclado, `aria-*`, scroll-spy y respeto a
  `prefers-reduced-motion`.

## Estructura

```
.
├── index.html            (versión clara: logo SVG, secciones, mascota y scripts embebidos)
├── index-carbon.html     (versión carbon/negra: mismo contenido, tema oscuro neón + rojo)
└── assets/
    ├── brands/           (chips normalizados del muro de marcas)
    │   ├── brand00.png ... brand45.png   (catálogo de logos de distribuidores)
    ├── gonher.jpeg        (logos originales / fuentes)
    ├── ciosa.jpeg
    ├── vazquez.jpeg
    ├── energy-parts.jpeg
    ├── spr.jpeg
    └── logo.jpeg
```

El muro de marcas usa los chips normalizados en `assets/brands/` (`brand00.png` …
`brand45.png`): cada logo recortado y centrado en un chip uniforme de 320x180,
respetando su color de fondo nativo para que los de fondo oscuro sigan legibles.
Los `.jpeg` en `assets/` se conservan como fuentes originales.

## Probar localmente

Para que el mapa cargue, sirvelo por HTTP local:

```bash
python3 -m http.server 8080   # http://localhost:8080
```

## Publicar en GitHub Pages

1. Sube estos archivos a un repo nuevo (incluida la carpeta `assets/`):

   ```bash
   git init
   git add .
   git commit -m "Rediseno premium landing Balatas y Refacciones Rodriguez"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
   git push -u origin main
   ```

2. En GitHub: **Settings -> Pages**.
3. En **Source** elige "Deploy from a branch", rama `main`, carpeta `/ (root)`. Guarda.
4. En 1 o 2 minutos: `https://TU_USUARIO.github.io/TU_REPO/`.

Si usas un workflow de GitHub Actions en lugar de "Deploy from branch", incluye
control de concurrencia para evitar conflictos entre ejecuciones:

```yaml
concurrency:
  group: pages
  cancel-in-progress: true
```

## Pendiente antes de publicar

- Reemplazar el dominio de ejemplo `https://balatasrodriguez.com/` por el dominio real
  en las etiquetas `<link rel="canonical">` y `og:url` (marcadas con `TODO` en `index.html`).
- Confirmar o ajustar la linea/descripcion de cada marca en la seccion "Marcas"
  (por ejemplo Gonher, Energy Parts). Estan como texto editable dentro de cada
  `.brand-meta` en `index.html`.

## Personalizar

- **Logo:** es un `<svg class="logo-mark">` en encabezado y pie; texto y colores en
  las clases `.logo-word .l1` / `.l2` del CSS.
- **WhatsApp:** busca `5216751052695` en `index.html`.
- **Facebook:** busca `facebook.com/search` y pon la URL real de la pagina.
- **Consejos de Soso:** edita el arreglo `TIPS` dentro del `<script>`.
- **Tamano de Soso:** variable `--soso-size` (117px escritorio; 92px y 75px en movil).
- **Colores:** variables CSS en `:root` al inicio del `<style>`.

## Notas del rediseno

- Se conservo la colorimetria de la marca (azul marino + rojo) como pedia el encargo,
  en lugar de los acentos genericos del prompt base.
- Se mantuvo la mascota Soso intacta en comportamiento, solo 15% mas pequena.
- Se anadieron dos secciones nuevas: tarjetas de marca ("lineas") y opiniones.
- Se mantiene sin frameworks ni build para desplegar directo en GitHub Pages y
  conservar la mascota y sus interacciones ya probadas.
