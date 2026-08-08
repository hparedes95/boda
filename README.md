# Nos casamos — Sara & Hector · 23 de octubre de 2027

Invitación de boda en formato arcade retro. Una sola página, sin dependencias:
todo (gráficos pixel art, música chiptune y efectos de sonido) se genera en el
navegador con Canvas y Web Audio.

## Ver la web

https://hparedes95.github.io/boda/

## Archivos

- `index.html` — la invitación completa (HTML + CSS + JS en un único archivo).
- `preview.png` — imagen de previsualización para WhatsApp y redes (1200×630).
- `.nojekyll` — evita que GitHub Pages procese el sitio con Jekyll.

## Activar GitHub Pages

En el repositorio: **Settings → Pages → Build and deployment**, elegir
*Deploy from a branch*, seleccionar la rama que contiene estos archivos y la
carpeta `/ (root)`. En un par de minutos la web queda publicada en la URL de
arriba.

## Personalizar

Casi todo el texto está en el bloque `CONFIG` al principio del `<script>` de
`index.html`:

```js
const CONFIG = {
  p1:     "HECTOR",
  p2:     "SARA",
  p3:     "ELIAS",
  titulo: "MISIÓN: BODA",
  anio:   "2020",
  ano:    "2027",
  dia:    "23",
  mes:    "OCTUBRE",
  web:    ""        // URL de la web con toda la info; vacío = "WEB PROXIMAMENTE"
};
```

Los textos que aparecen abajo durante cada nivel están en `CAP1`, `CAP2` y
`CAP3`, y la duración de cada escena en el array `SCENES`.

Si cambias de usuario o de repositorio, actualiza también las URLs absolutas de
las etiquetas `og:` y `canonical` en el `<head>`: las relativas no funcionan
para la previsualización en WhatsApp.
