# Balatas y Refacciones Rodríguez — Landing Page

Landing page premium, responsiva y de una sola página para la refaccionaria
**Balatas y Refacciones Rodríguez** (Durango). Hecha con HTML, CSS y JavaScript
puros (sin frameworks ni dependencias de build).

## ✨ Incluye
- Diseño moderno y minimalista con paleta tomada del logo (azul marino + rojo).
- Hero con disco de freno animado y caliper.
- Secciones: Nosotros (Misión/Visión), Valores, Servicios, Marcas y Contacto.
- Marquesina con marcas: Gonher, Ciosa, Vázquez, Energy Parts, SPR Automotive.
- **Chispas**, la mascota bujía: da consejos cada 6 s y cambia de esquina cada 2 consejos.
- Botón de WhatsApp, mapa de ubicación y enlace a Facebook.
- Accesible y respeta `prefers-reduced-motion`.

## 📁 Estructura
```
.
├── index.html
└── assets/
    ├── logo.jpeg
    ├── gonher.jpeg
    ├── ciosa.jpeg
    ├── vazquez.jpeg
    ├── energy-parts.jpeg
    └── spr.jpeg
```

## 🚀 Probar localmente
Solo abre `index.html` en tu navegador. Para que el mapa cargue bien, sírvelo
con un servidor local:
```bash
python3 -m http.server 8080
# luego abre http://localhost:8080
```

## 🌐 Publicar en GitHub Pages
1. Crea un repositorio nuevo y sube estos archivos (incluida la carpeta `assets/`).
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
4. En 1–2 minutos tu sitio estará en
   `https://TU_USUARIO.github.io/TU_REPO/`.

## ✏️ Personalizar
- **Datos de contacto / WhatsApp:** busca `5216751052695` en `index.html`.
- **Enlace de Facebook:** busca `facebook.com/search` y reemplázalo por la URL real de la página.
- **Consejos de Chispas:** edita el arreglo `TIPS` dentro del `<script>`.
- **Colores:** edita las variables CSS en `:root` (al inicio del `<style>`).
