# vacantica-media

Repo **público**, solo para servir archivos de media ya aprobados (memes, reels) vía jsDelivr, para que herramientas externas como Metricool puedan leerlos por URL pública al programar publicaciones.

## Qué va aquí

Únicamente el archivo final de una pieza que ya pasó revisión en [vacantica-social](https://github.com/arcaxus/vacantica-social) (el repo privado, fuente de verdad de guiones, escenas y trabajo en progreso). Nada de contenido sin aprobar, guiones, código ni material de trabajo.

Estructura, calcada de `output/` en vacantica-social:

```
memes/<slug>/meme.png
reels/<slug>/video-final-PUBLICABLE.mp4
```

## Cómo se usa

Cada archivo aquí es accesible vía jsDelivr sin build ni configuración:

```
https://cdn.jsdelivr.net/gh/arcaxus/vacantica-media@main/<ruta-del-archivo>
```

Ejemplo: `memes/vacante-perfecta/meme.png` →
`https://cdn.jsdelivr.net/gh/arcaxus/vacantica-media@main/memes/vacante-perfecta/meme.png`

Esa URL se usa como `media` al programar el post en Metricool.

## Nota sobre caché

jsDelivr cachea agresivamente. Si un archivo se **reemplaza** con el mismo nombre, puede tardar en reflejar el cambio (usar `@<hash-de-commit>` en vez de `@main` fuerza la versión exacta si hace falta evitar la caché). En el flujo normal cada pieza es nueva, así que esto rara vez importa.
