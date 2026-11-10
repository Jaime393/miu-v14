# Lectura — miu-v14 — 2026-11-09

Los 13 archivos leídos enteros en vivo 2026-11-09. Citas literales entre
comillas; todo lo demás es paráfrasis de lo leído. Solo SÉ.

## README.md (102 B, 2 líneas)

```
# miu-v14
MIU Ecosistema - miu-v14 - DOI 10.5281/zenodo.20547558 - Φ_Red $107M - cada nodo es un ojo
```

Tres afirmaciones en una línea: el DOI `10.5281/zenodo.20547558`, `Φ_Red
$107M`, y "cada nodo es un ojo". Ninguna se desarrolla en el repo.

## AUTO.md (12 B, 1 línea)

```
# MIU 16/16
```

Lo escribe el workflow (ver HISTORIAL.md). Es el único contenido del
archivo.

## BIBLIA_DEVORADOR.md (47 B, 1 línea)

```
# Biblia DEVORADOR 66 libros - MIU 16/16 nodos
```

El título promete 66 libros. El archivo no contiene ningún libro, ni
índice, ni enlace (ver CONTENIDO.md §2).

## FUNDING.yml (107 B, 4 líneas)

```yaml
github: [Jaime393]
open_collective: miu-ecosistema
custom: https://www.buymeacoffee.com/miu
# $1M -> $107M
```

Financiación declarada: GitHub Sponsors `Jaime393`, Open Collective
`miu-ecosistema`, Buy Me a Coffee `miu`. El comentario final repite el
salto "$1M -> $107M" como literal, sin cifra que lo respalde en el repo.

## _config.yml (45 B, 2 líneas)

```yaml
theme: jekyll-theme-minimal
title: MIU 16/16
```

Configuración de GitHub Pages (tema Jekyll minimal). NO SÉ si Pages
llegó a estar desplegado: no se comprobó en vivo.

## index.html (591 B, 1 línea)

Título: "MIU Ecosistema 16/16 - DOI 10.5281/zenodo.20547558". Cuerpo:

- `🌱 MIU 16/16 nodos vivos - Φ_Red $107M`
- `16 repos global mind 16/16 - 5 repos 201 CREATE fix 404 - autorización TOTAL x10000`
- `DOI 10.5281/zenodo.20547558 - Cerro Colorado Arequipa 2335m`
- Tarjeta bento: `Global Mind 16/16` / `Cada nodo es un ojo`

Carga `assets/css/micelio.css`, `assets/js/core.js` y el `manifest.json`.
El "5 repos 201 CREATE fix 404" no se desarrolla: no hay lista de esos
5 repos en ningún archivo.

## manifest.json (133 B, 1 línea)

```json
{"name":"MIU 16/16","short_name":"MIU16","start_url":"/","display":"standalone","background_color":"#0a0a0b","theme_color":"#a3ff12"}
```

Manifiesto PWA estándar, nombre "MIU 16/16".

## sw.js (156 B, 1 línea)

```js
self.addEventListener('install',e=>self.skipWaiting());self.addEventListener('fetch',e=>e.respondWith(fetch(e.request).catch(()=>caches.match(e.request))));
```

Service worker genérico: instala sin esperar y sirve de caché si la red
falla. Sin lógica MIU.

## worker.js (401 B, 1 línea)

```js
export default { async fetch(req){ const u=new URL(req.url); if(u.pathname=='/miu/global') return new Response(JSON.stringify({global_mind:true, repo:'miu-v14', fix_404:true, autorizacion:'TOTAL x10000 v29 fix 404', phi:'$107M', drive:'<ID DE DRIVE — VALOR NO REPRODUCIDO>'}),{headers:{'Content-Type':'application/json'}}); return new Response('global mind miu-v14 - MIU v29 fix 404 - 11->16 repos'); } }
```

En `/miu/global` devuelve un JSON fijo de 6 claves, todas literales
(`global_mind:true`, `fix_404:true`, `autorizacion:'TOTAL x10000 v29 fix
404'`, `phi:'$107M'`, `drive:` un ID de Drive). Fuera de esa ruta
devuelve el texto fijo `'global mind miu-v14 - MIU v29 fix 404 - 11->16
repos'`. No lee nada vivo: no hay `fetch`, ni KV, ni D1, ni variable de
entorno en el archivo. El ID de Drive no se reproduce: su huella SHA256
es `b3a56d7a…` (ver CONTENIDO.md §3).

## assets/css/micelio.css (172 B, 1 línea)

```css
:root{--bg:#0a0a0b;--lime:#a3ff12}body{background:var(--bg);color:white}.glass{backdrop-filter:blur(12px);background:rgba(255,255,255,0.05);border-radius:16px;padding:16px}
```

Dos variables (`--bg`, `--lime`) y una clase `.glass`. CSS real y
mínimo.

## assets/js/core.js (147 B, 1 línea)

```js
class MIU_Micelio extends EventTarget{sembrarNodo({rho}){return {rho:Math.max(rho,0.001)}}renderMicelioCanvas(c){}};window.MIU_Micelio=MIU_Micelio;
```

Una clase con dos métodos: `sembrarNodo` devuelve `{rho}` con mínimo
0.001, y `renderMicelioCanvas` está vacío. No hay renderizado, ni red,
ni datos.

## .github/workflows/miu-auto-deploy.yml (506 B, 21 líneas)

Nombre: "MIU Auto-Deploy Sin PAT". Disparadores: `workflow_dispatch` y
`push` a `main`. Permisos `contents: write`. Pasos: checkout v4, y un
`run` que escribe `# MIU 16/16` en `AUTO.md`, configura
`user.name "miu-tejedor"` y `user.email "miu@local"`, y empuja si hay
cambios. Es el autor del commit cabeza (ver HISTORIAL.md). NO SÉ si el
workflow llegó a correr en GitHub Actions: no se comprobó en vivo.
