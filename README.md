# KRYM Symbol (CC0)

Símbolo abierto de KRYM para uso libre en web y diseño. Incluye **SVG**, **sprite** (`<use>`), **PNG** e **iconfont**. Licencia: **CC0 1.0 (dominio público)**.

## CDN
- Sprite (`<use>`): `https://cdn.jsdelivr.net/gh/ceokrym/krym-symbol/sprites/symbols.svg#simbolo`
- SVG (currentColor): `https://cdn.jsdelivr.net/gh/ceokrym/krym-symbol/svg/simbolo.svg`
- PNG negro 512: `https://cdn.jsdelivr.net/gh/ceokrym/krym-symbol/png/simbolo-black-512.png`
- PNG blanco 512: `https://cdn.jsdelivr.net/gh/ceokrym/krym-symbol/png/simbolo-white-512.png`
- Iconfont (CSS): `https://cdn.jsdelivr.net/gh/ceokrym/krym-symbol/iconfont/style.css`
- Figma (.fig): `https://cdn.jsdelivr.net/gh/ceokrym/krym-symbol/figma/simbolo.fig`

> Tip: si el CDN no refresca tras un commit, agrega `?v=1` al final de la URL.

## Uso rápido
**Sprite**
```html
<svg width="64" height="64" aria-label="KRYM symbol" style="color:#111">
  <use href="https://cdn.jsdelivr.net/gh/ceokrym/krym-symbol/sprites/symbols.svg#simbolo?v=1"></use>
</svg>

### SVG Directo
<img alt="KRYM symbol"
     src="https://cdn.jsdelivr.net/gh/ceokrym/krym-symbol/svg/simbolo.svg"
     width="128" height="128">

### PNG
<!-- Negro sobre fondo claro -->
<img src="https://cdn.jsdelivr.net/gh/ceokrym/krym-symbol/png/simbolo-black-256.png"
     alt="KRYM symbol" width="128" height="128">

<!-- Blanco sobre fondo oscuro -->
<div style="background:#111;padding:12px;display:inline-block">
  <img src="https://cdn.jsdelivr.net/gh/ceokrym/krym-symbol/png/simbolo-white-256.png"
       alt="KRYM symbol" width="128" height="128">
</div>

### Incofont
<link rel="stylesheet" href="https://cdn.jsdelivr.net/gh/ceokrym/krym-symbol/iconfont/style.css">
<i class="icon-krym" aria-hidden="true"></i>
<style>
  .icon-krym{font-size:64px;color:#111}
  @media (prefers-color-scheme:dark){.icon-krym{color:#fff}}
</style>

## PNGs publicados
Rutas esperadas (fondo transparente):
png/simbolo-black-32|64|128|256|512.png
png/simbolo-white-32|64|128|256|512.png

Recomendación: ~8–12% de margen interno y arte centrado.

## Estructura del repo
krym-symbol/
├─ LICENSE
├─ README.md
├─ svg/
│  ├─ simbolo.svg                 # SVG maestro (fill="currentColor")
│  └─ simbolo-monocromo.svg       # variante 1 color (negro/blanco)
├─ png/
│  ├─ simbolo-black-32.png
│  ├─ simbolo-black-64.png
│  ├─ simbolo-black-128.png
│  ├─ simbolo-black-256.png
│  ├─ simbolo-black-512.png
│  ├─ simbolo-white-32.png
│  ├─ simbolo-white-64.png
│  ├─ simbolo-white-128.png
│  ├─ simbolo-white-256.png
│  └─ simbolo-white-512.png
├─ sprites/
│  └─ symbols.svg                 # <symbol id="simbolo">…</symbol>
├─ iconfont/
│  ├─ demo.html
│  ├─ krym.ttf
│  ├─ krym.woff
│  ├─ selection.json
│  └─ style.css                   # define .icon-krym (content: "\e900")
└─ figma/
   └─ simbolo.fig

## Accesibilidad
Con significado: aria-label="KRYM symbol" o <title>…</title>.

Decorativo: aria-hidden="true".

## Notas & Troubleshooting
Color: el sprite/SVG hereda currentColor → controla con CSS (color:).

Blanco “invisible”: prueba sobre fondo oscuro o pon style="color:#111".

<use> no muestra: confirma id="simbolo" y usa #simbolo en la URL; añade ?v=1.

Iconfont sin ícono: verifica .icon-krym:before { content:"\e900"; } en iconfont/style.css y que la fuente cargó.

## Licencia
CC0 1.0 Universal — Dominio público. Puedes usar, modificar y distribuir sin atribución. Consulta el archivo LICENSE.
