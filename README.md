# Modo Ya · Landing

Landing page de **Modo Ya**, delivery local de Malargüe, Mendoza.
Objetivos: que la gente descargue la app y que los locales gastronómicos se pre-inscriban.

## Archivos

- `index.html` — la página completa (HTML, CSS y JavaScript en un solo archivo).
- `img/` — fotos de comida recortadas sin fondo (Unsplash, licencia libre). Para cambiarlas, reemplazá los archivos manteniendo el mismo nombre.

## Lanzamiento

Mientras la app no esté en las tiendas, la página muestra avisos de "Próximamente" (barra de arriba, etiquetas "Pronto" en las tiendas, etc.).
El día del lanzamiento, en `index.html` cambiá:

```js
const PROXIMAMENTE = true;
```

por `false` y todos los avisos desaparecen.

## Pendiente antes de publicar

Buscá estas marcas en `index.html` y reemplazalas por los datos reales:

- `549XXXXXXXXXX` → número de WhatsApp.
- `Email: próximamente` → email de contacto.
- `[LINKS]` → links de Google Play, App Store, Instagram y TikTok.
- `[QR]` → QR real de descarga (el actual es decorativo).
- `PREINSCRIPTOS_INICIAL` → cantidad real de locales pre-inscriptos.
- Cupón `MODOYA` → sacarlo si la promo no va a existir.

## Formulario de pre-inscripción

Hoy está en modo prueba (no envía datos). Para conectarlo, cambiá en `index.html`:

```js
const FORM_CONFIG = { mode: "demo", endpoint: "" };
```

por, por ejemplo con Formspree:

```js
const FORM_CONFIG = { mode: "formspree", endpoint: "https://formspree.io/f/TU_ID" };
```

También acepta `"sheets"` (Google Apps Script) o `"custom"` (backend propio).

## Publicar

Arrastrar esta carpeta a https://app.netlify.com/drop, o activar GitHub Pages si el repositorio pasa a ser público.
