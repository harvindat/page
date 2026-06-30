# Balatas y Refacciones Rodríguez — Landing Page

Landing page premium, responsiva y de una sola página para la refaccionaria
**Balatas y Refacciones Rodríguez** (Durango). HTML, CSS y JavaScript puros,
sin frameworks ni pasos de build.

## ✨ Incluye
- Diseño moderno y minimalista con paleta tomada del logo (azul marino + rojo).
- **Logo vectorial (SVG)** rediseñado en la tipografía y colores de la página.
- Hero con disco de freno animado y caliper.
- Secciones: Nosotros (Misión/Visión), Valores, Servicios, Marcas y Contacto.
- Marquesina de marcas: Gonher, Ciosa, Vázquez, Energy Parts, SPR Automotive.
- **Soso**, la mascota bujía: da consejos cada 6 s y cambia de esquina cada 2 consejos.
- Botón de WhatsApp, mapa de ubicación y enlace a Facebook.
- Accesible y respeta `prefers-reduced-motion`.

## 📁 Estructura
```
.
├── index.html          (incluye el logo como SVG embebido)
└── assets/
    ├── gonher.jpeg
    ├── ciosa.jpeg
    ├── vazquez.jpeg
    ├── energy-parts.jpeg
    └── spr.jpeg
```

## 🚀 Probar localmente
Abre `index.html` en tu navegador. Para que el mapa cargue, sírvelo en local:
```bash
python3 -m http.server 8080   # http://localhost:8080
```

## 🌐 Publicar en GitHub Pages
1. Sube estos archivos a un repo nuevo (incluida la carpeta `assets/`):
   ```bash
   git init
   git add .
   git commit -m "Landing page Balatas y Refacciones Rodríguez"
   git branch -M main
   git remote add origin https://github.com/TU_USUARIO/TU_REPO.git
   git push -u origin main
   ```
2. En GitHub: **Settings → Pages**.
3. En **Source** elige la rama `main` y la carpeta `/ (root)`. Guarda.
4. En 1–2 min: `https://TU_USUARIO.github.io/TU_REPO/`.

## ✏️ Personalizar
- **Logo:** es un `<svg class="logo-mark">` dentro de `index.html` (header y footer);
  el texto y colores se controlan con las clases `.logo-word .l1` / `.l2` en el CSS.
- **WhatsApp:** busca `5216751052695` en `index.html`.
- **Facebook:** busca `facebook.com/search` y pon la URL real de la página.
- **Consejos de Soso:** edita el arreglo `TIPS` dentro del `<script>`.
- **Colores:** variables CSS en `:root` (inicio del `<style>`).
