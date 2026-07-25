# Sitio web — NodoSec Instalaciones

Sitio estático (HTML/CSS/JS puro, sin frameworks ni build step). Funciona directo en GitHub Pages, Netlify, Vercel o cualquier hosting estático.

## Antes de publicar — reemplaza estos placeholders

Busca estos textos en `index.html` y cámbialos por tus datos reales:

| Placeholder | Dónde aparece | Reemplazar por |
|---|---|---|
| `+52 55 0000 0000` | Botón WhatsApp (2 lugares) y teléfono de contacto | Tu número real, formato `52<lada><número>` para el link de WhatsApp (`wa.me/...`) |
| `contacto@nodosec.mx` | Sección de contacto | Tu correo real |
| `href="#"` en Facebook/Instagram (footer) | Pie de página | Links reales a tus redes, una vez creadas |
| Lista de municipios en "Cobertura" | Sección `#cobertura` | Ajusta a tu zona real de servicio |

También revisa `<meta name="description">` y las etiquetas Open Graph en el `<head>` si cambias el dominio.

## Publicar en GitHub Pages (gratis)

1. Crea un repositorio nuevo en GitHub (público, para usar Pages gratis) — por ejemplo `nodosec-web`.
2. Sube el contenido de esta carpeta a la raíz del repositorio:
   ```bash
   cd nodosec-site
   git init
   git add .
   git commit -m "Sitio inicial NodoSec"
   git branch -M main
   git remote add origin https://github.com/TU-USUARIO/nodosec-web.git
   git push -u origin main
   ```
3. En GitHub: **Settings → Pages → Source → Deploy from a branch → main / (root)**.
4. En unos minutos el sitio queda publicado en `https://TU-USUARIO.github.io/nodosec-web/`.
5. Si compras un dominio propio (ej. `nodosec.mx`), en el mismo menú de Pages agrega el dominio en "Custom domain" y configura el DNS del dominio (registro CNAME apuntando a `TU-USUARIO.github.io`).

## Estructura de archivos

```
index.html
assets/
  css/style.css
  js/script.js
  img/
    favicon.png              ← ícono para pestaña del navegador
    logo-horizontal.png       ← logo fondo claro
    logo-horizontal-dark.png  ← logo fondo oscuro (usado en el header)
    logo-icon.png             ← ícono solo (footer, redes)
    producto-*.png            ← imágenes de producto
```

## Notas

- Las imágenes de producto son las capturas que compartiste (kits HiLook y ZKTeco). Para verse más profesional y generar más confianza, lo ideal a mediano plazo es reemplazarlas por fotos reales de tus propias instalaciones.
- Los precios de la sección "Precios de referencia" están tomados del Excel `NodoSec_Cotizador.xlsx` — si cambias el tarifario ahí, actualiza también la tabla en `index.html` (sección `#precios`).
- El sitio usa Google Fonts (Space Grotesk, Inter, JetBrains Mono) vía CDN — necesita conexión a internet para verse con la tipografía completa; si no carga, cae automáticamente en una fuente del sistema.
