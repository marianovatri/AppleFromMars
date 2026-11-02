# Apple From Mars

Proyecto para el NASA International Space Apps Challenge 2022: *Outfitting a Mars Habitat: A 3D Print Challenge*.

Sitio: https://marsproyect.netlify.app/

## Sitio actual (`site/`)

Página estática, sin compilación: visor 3D de las piezas imprimibles (Three.js + STLLoader), láminas, planos en PDF y hora marciana en vivo.

Para verlo en local hace falta un servidor (el visor carga los `.stl` por HTTP):

```
cd site
python -m http.server 8000
```

Netlify publica `site/` según `netlify.toml`.

## Versión original (2022)

La versión hecha durante la competencia sigue en `src/` (Vue 3). Los archivos fuente originales (STL, SketchUp y PDF) están en `AppleFromMars/`.
