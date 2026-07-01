# Publicar el sitio (una sola vez, gratis)

Este motor genera HTML estático en esta carpeta. Para que Google lo indexe:

## Opción A — GitHub Pages (gratis)
1. Creá un repo público (ej. `zorin-site`) y subí el contenido de esta carpeta.
2. Settings -> Pages -> Deploy from branch -> main -> / (root).
3. Te da una URL `https://<user>.github.io/zorin-site`.
4. Cambiá `BASE_URL` en seo/generate_site.py por esa URL y volvé a correr (regenera canonical/sitemap).
5. Registrá el sitio en Google Search Console y subí el sitemap.xml.

## Opción B — Cloudflare Pages / Netlify (gratis, dominio propio)
Igual, pero podés conectar un dominio propio (ej. zorinapp.com/blog).

## Automatización
El Task Scheduler ya corre esto 1x/día (tarea Zorin-SEO-Daily): genera un artículo nuevo,
actualiza index + sitemap. Vos solo hacés `git push` (o conectás el deploy automático del repo).
