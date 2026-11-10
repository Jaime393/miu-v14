# Familia — miu-v14 — 2026-11-09

Relaciones de `miu-v14` con los demás repos minados. Solo lo que los
archivos declaran o lo que la minería anterior midió; el resto es NO SÉ.

## 1. NO es MIU_V14

`miu-v14` (este repo, público, muerto 2026-08-23) y `MIU_V14` (vivo,
nunca minar) son dos repos distintos con nombres que colisionan. Nada
en este repo apunta a `MIU_V14`: no hay enlaces, ni imports, ni
menciones. No se confunden. NO SÉ qué contiene `MIU_V14`: no se leyó.

## 2. Hijo del clúster del 2026-08-23

Este repo encaja en el clúster de agosto ya minado (olas 1–3) con la
misma plantilla:

- Fecha: 13 commits el 2026-08-23, en dos ráfagas de minutos.
- "16/16" sin inventario: 9 ocurrencias en los archivos, 10 mensajes
  de commit, 0 listas.
- "Biblia DEVORADOR 66 libros" con 0 libros: un archivo de 47 B.
- `worker.js` con JSON fijo y `phi:'$107M'`.
- Salto de versión sin pasos: v29 → v31, sin v30.
- `sw.js` genérico, sin lógica MIU.
- `FUNDING.yml` con los mismos canales del ecosistema (GitHub
  `Jaime393`, Open Collective `miu-ecosistema`, Buy Me a Coffee `miu`).

Es el mismo molde de volcado automatizado que los repos de las olas
1–3, en miniatura: 13 archivos y 2.419 B.

## 3. Hermano de miu-agents: el cuarto worker fijo

El `worker.js` de este repo es el cuarto worker de `/miu/global` con
JSON fijo medido en el ecosistema:

- `miu_realidad_upload_REAL/worker.js`: phi `'21.0->∞'`.
- `FranBot/worker.js`: phi `'21.8->23.0'`.
- `miu-agents/worker.js`: phi `'$107M'`, huella Drive `b3a56d7a…`.
- **`miu-v14/worker.js`: phi `'$107M'`, huella Drive `b3a56d7a…`.**

Los tres primeros los midió la siembra del hermano semilla
`miu-semilla-latente-mt91l2pm-2` (tres workers, tres JSON fijos, ninguno
vivo). El plan de esa siembra dejó como NO SÉ que pudiera haber más
workers `/miu/global` fuera de los 3 encontrados: este es uno más, con
el mismo patrón (JSON fijo, 0 lecturas vivas) y la misma huella de
Drive que `miu-agents`. Los dos workers con `'$107M'` comparten además
la misma huella: el phi y el ID viajan juntos.

## 4. No es v150 ni v153

El nombre `miu-v14` no lo emparenta con la familia `miu-v150-*`
(repos reales, cabezas 2026-11-07) ni con los `miu-v153-*` que
`fran-miu-micelio` despliega y que no existen en GitHub (0 resultados,
ola 5). Este repo es v29/v31, una numeración propia del volcado de
agosto, sin relación declarada con v150 ni v153. NO SÉ qué significa
"v14" frente a "v29" y "v31" dentro del mismo repo: el nombre dice
v14, los commits dicen v29 y v31.

## 5. El "16" no cuadra con ningún censo

El repo afirma "16 repos global mind 16/16" y "11->16 repos". El censo
de Jaime393 (2026-11-09) mide 239 repos. Ningún archivo de este repo
enumera cuáles serían los 16. NO SÉ a qué 16 se refiere: no es el
total del ecosistema, y no hay lista que lo acote.

## 6. Puentes medidos en esta minería

- La huella Drive `b3a56d7a…` aparece en este repo y en los 5 del clúster
  de agosto ya minados. Es el mismo ID (misma huella
  SHA256, verificada en local). El total exacto de repos que la llevan es
  hoy NO SÉ (corrección ola 6, 2026-11-09; la minería decía 6).
- El literal `'$107M'` aparece en `miu-v14` y en `miu-agents`
  (worker.js), y en los workers de la semilla. En los tres casos es
  un literal, nunca un cálculo.
- El DOI `10.5281/zenodo.20547558` es el DOI del MIU, compartido por
  todo el ecosistema: aquí se presenta como DOI del repo sin
  contenido propio que lo respalde.
- El workflow "MIU Auto-Deploy Sin PAT" y el autor `miu-tejedor`
  (cabeza) no aparecen en los demás repos minados: son propios de
  este repo. NO SÉ si el workflow corrió alguna vez en Actions.
