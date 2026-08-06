# Lexus NX 300 2019 — landing de venta

Sitio estático de una página (`index.html`) para la venta particular de un Lexus NX 300 2019.
Publicado en: https://lexus-nx300.netlify.app/

## Qué se corrigió respecto a la versión anterior (drag & drop a Netlify)

- `canonical` apuntaba a un placeholder (`TU-SITIO.netlify.app`) — corregido al dominio real.
- `og:image` / `twitter:image` referenciaban `og-image.jpg`, un archivo que nunca se subió — se extrajo una foto real del auto y se agregó al repo.
- Precio desalineado con el aviso de ChileAutos ($24.870.000 vs $23.770.000) — unificado a $23.770.000 en todo el sitio (meta tags, JSON-LD, precio visible, tabla de mercado).
- Se agregó sección de FAQ visible + schema `FAQPage` (formato que citan los motores de IA generativa).
- Se agregó `robots.txt` y `sitemap.xml` en la raíz.
- Se agregó `sameAs` en el JSON-LD apuntando al aviso de ChileAutos, y un link cruzado visible en la landing — señal de que ambos avisos son la misma entidad/vehículo.
- Se agregó `llms.txt` (estándar emergente, bajo costo).

## Cómo desplegar cambios

Este repo está pensado para conectarse a Netlify vía Git (Site settings → Build & deploy → Link repository).
Una vez conectado, cualquier `git push` a `main` dispara un deploy automático — no hace falta volver a arrastrar el HTML manualmente.

No hay build step: `netlify.toml` publica la raíz del repo tal cual (sitio estático).

## Pendiente (acción manual del dueño, fuera de este repo)

- Conectar este repo a Netlify (o a Vercel/Cloudflare Pages) para que el deploy sea automático vía git push.
- Dar de alta el sitio en Google Search Console y Bing Webmaster Tools, y enviar `sitemap.xml`.
- Actualizar el precio en el aviso de ChileAutos a $23.770.000 para que coincida (ese aviso vive en la plataforma de ChileAutos, no en este repo).
