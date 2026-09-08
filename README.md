# Ximena Hincapié — portafolio y hoja de vida

Sitio de una sola página: motion design y desarrollo web. Estático, sin dependencias ni proceso de build.

## Archivos

- `index.html` — el sitio.
- `support.js` — runtime que necesita `index.html`. Debe quedar junto a él.
- `Ximena Hincapie.dc.html` — archivo de trabajo (fuente editable). `index.html` es su copia publicable.
- `proyectos/` — miniaturas de los sitios web.
- `robots.txt`, `sitemap.xml` — indexación en buscadores.
- `render.yaml` — configuración de despliegue.

## Publicar en Render

1. Sube el repositorio a GitHub.
2. En Render: **New → Static Site** y conecta el repositorio.
3. Deja el build command vacío y el publish directory en `.` (o deja que Render lea `render.yaml`).
4. Deploy.

Cada push a la rama principal vuelve a desplegar.

## Antes de publicar

Reemplaza el dominio provisional `https://ximenahincapie.com/` por la URL real en:

- `index.html` — etiquetas `canonical`, `og:url` y el bloque JSON-LD.
- `robots.txt` — línea `Sitemap:`.
- `sitemap.xml` — etiqueta `<loc>`.

También falta la URL de LinkedIn: en `index.html` apunta a `https://www.linkedin.com/`.

## Editar contenido

Los textos viven en el objeto `DICT` dentro de `index.html`, con una versión en español (`es`) y una en inglés (`en`). Al cambiar una frase hay que cambiarla en las dos. Después de editar el archivo de trabajo, vuelve a copiarlo sobre `index.html`.
