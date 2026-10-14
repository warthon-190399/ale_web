# Portafolio — Esther Fernández

Sitio estático (HTML + CSS + JS puro, sin dependencias ni build step).

## Estructura

```
index.html               → página principal del portafolio
caso-active-park.html    → caso de estudio "Estrategia de precios — Active Park"
voz-del-shopper/         → dashboard "La voz del shopper" (supermercados de Lima)
  index.html
  assets/d3.v7.8.5.min.js
  data/dash_data.json     → indicadores agregados (para actualizar, reemplazar este archivo)
  data/dash_geo.json      → mapa de distritos de Lima y Callao
assets/
  images/
    foto-perfil.png
    icons/                → íconos de herramientas (Excel, Power BI, SQL, etc.)
    trabajos/              → imágenes del carrusel "Mi trabajo en acción"
  cv/
    CV-Esther-Fernandez.pdf
README.md
```

## Cómo subirlo a GitHub

1. Crea un repositorio nuevo en GitHub. Si quieres que quede en `tuusuario.github.io`
   (dominio raíz), el repo debe llamarse exactamente `tuusuario.github.io`.
   Si prefieres un repo con otro nombre (ej. `portafolio`), el sitio quedará en
   `tuusuario.github.io/portafolio/`.

2. Desde esta carpeta, en tu terminal:

   ```bash
   git init
   git add .
   git commit -m "Primera versión del portafolio"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/TU-REPO.git
   git push -u origin main
   ```

## Cómo activar GitHub Pages

1. En GitHub, entra al repositorio → **Settings** → **Pages**.
2. En "Build and deployment" → **Source**, elige **Deploy from a branch**.
3. En **Branch**, selecciona `main` y la carpeta `/ (root)`.
4. Guarda. En un par de minutos tu sitio estará disponible en la URL que
   GitHub te muestra ahí mismo (normalmente `https://TU-USUARIO.github.io/TU-REPO/`).

## Notas

- Todas las imágenes y el PDF del CV ya están incluidos como archivos locales
  dentro de `assets/` — no dependen de ningún servicio externo, así que
  funcionan igual en GitHub Pages que en tu computadora.
- El carrusel de "Mi trabajo en acción" y el color de acento están
  resueltos con JavaScript plano (sin frameworks) al final de `index.html`.
- Para cambiar el color de acento del sitio, busca `ACCENT` en el `<script>`
  al final de `index.html` y los valores `#5C6B2E` a lo largo del archivo
  (ese es el verde oliva usado como color de marca).
- El dashboard `voz-del-shopper/` carga sus datos desde `data/` con `fetch`, así que en local
  hay que abrirlo con un servidor (`python -m http.server 8000` en la raíz del sitio);
  en GitHub Pages funciona directo. Solo contiene datos agregados: no subir reseñas crudas.
