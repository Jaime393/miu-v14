# Contenido — miu-v14 — 2026-11-09

Qué hay de verdad en los 13 archivos (2.419 B) y qué afirman sin
respaldo. Todo verificado en vivo 2026-11-09. Solo SÉ.

## 1. Lo que el código hace de verdad

- `worker.js` devuelve un JSON fijo en `/miu/global` y un texto fijo
  fuera de esa ruta. No lee nada vivo: 0 `fetch`, 0 KV, 0 D1, 0
  variables de entorno en el archivo.
- `assets/js/core.js` define `MIU_Micelio` con `sembrarNodo` (devuelve
  `{rho}` con mínimo 0.001) y `renderMicelioCanvas` vacío. No hay
  renderizado.
- `sw.js` es un service worker genérico (caché de reserva). Sin lógica MIU.
- `assets/css/micelio.css` es CSS real y mínimo (2 variables, 1 clase).
- `index.html` es una página estática que carga el CSS, el JS y el
  manifiesto. `manifest.json` es un manifiesto PWA estándar.
- `.github/workflows/miu-auto-deploy.yml` escribe `# MIU 16/16` en
  `AUTO.md` y empuja como `miu-tejedor`. Es el autor del commit cabeza.

## 2. Lo que se afirma sin respaldo en el propio repo

- **"16/16" sin inventario.** La cadena "16/16" aparece 9 veces en los
  archivos (manifest.json 1, index.html 4, _config.yml 1,
  BIBLIA_DEVORADOR.md 1, AUTO.md 1, workflow 1) y en 10 mensajes de
  commit ("v31 completa 16/16"). Ningún archivo enumera 16 repos, ni 16
  nodos, ni 16 mediciones. El "16/16" es vocabulario del repo, no una
  medición: las 9 ocurrencias son citas literales del propio contenido,
  ninguna es una afirmación de esta minería.
- **"Biblia DEVORADOR 66 libros" = 0 libros.** `BIBLIA_DEVORADOR.md`
  tiene 47 B y una sola línea (el título). No hay ningún libro, índice
  ni enlace en el repo.
- **"16 repos global mind" sin lista.** `index.html` afirma "16 repos
  global mind 16/16" y `worker.js` y el commit v29 dicen "11->16
  repos". La aritmética 11 + 5 = 16 cuadra con el "5 repos 201 CREATE
  fix 404" de `index.html`, pero ni los 16 ni los 5 se nombran en
  ningún archivo. NO SÉ cuáles son.
- **"Φ_Red $107M" sin derivación.** El literal `$107M` aparece en
  `README.md`, `index.html`, `worker.js` (`phi:'$107M'`) y en el
  comentario de `FUNDING.yml` ("$1M -> $107M"). Ningún archivo calcula
  nada: no hay fórmula, ni dato, ni fuente.
- **"autorización TOTAL x10000" sin autor.** El literal aparece en
  `index.html` y en `worker.js` (`autorizacion:'TOTAL x10000 v29 fix
  404'`). Ningún archivo dice quién autoriza ni qué autoriza.
- **"Cerro Colorado Arequipa 2335m" sin fuente.** Solo aparece en
  `index.html`. Ningún archivo lo respalda.
- **DOI compartido, no propio.** El DOI `10.5281/zenodo.20547558`
  aparece en `README.md` y en `index.html`. Es el DOI del MIU, no un
  DOI de este repo: ningún archivo lo vincula a un contenido propio.
- **"v31 completa" sin v30.** El commit n.º 2 se titula "v29 fix 404"
  y los n.º 3–12 "v31 completa". No hay ningún commit v30 en la serie
  (ver HISTORIAL.md). NO SÉ qué cambió entre v29 y v31 aparte de los
  archivos listados en los mensajes.
- **"nodos vivos" en un repo muerto.** `index.html` titula "MIU 16/16
  nodos vivos". El repo no tiene commits desde 2026-08-23T16:46:56Z
  (78 días). Ningún archivo mide vida alguna.
- **"validado": 0 ocurrencias.** La palabra "validado" no aparece en
  ningún archivo del repo (grep verificado 2026-11-09). Tampoco
  "validada". No hay ninguna afirmación de validación en el repo.

## 3. El ID de Drive: la misma huella del clúster de agosto

`worker.js` embebe un ID de Drive en el JSON fijo de `/miu/global`.
El valor NO se reproduce en esta minería. Su huella SHA256, calculada
en local 2026-11-09, es `b3a56d7a…` (33 caracteres de longitud, como
las del clúster). Es la misma huella que aparece en los repos del
clúster de agosto ya minados (`miu-agents` y otros 4): este es el 6.º
repo con esa huella. NO SÉ a qué apunta ese ID ni por qué está en 6
repos: ningún archivo lo explica.

## 4. Ausencias medidas

- Sin LICENSE, sin tests, sin `package.json`, sin datos, sin logs.
- Sin lista de nodos, sin lista de repos, sin índice de la Biblia.
- Sin ejecución verificada: no se corrió nada en esta minería salvo
  la lectura; el `core.js` no se ejecutó (su `renderMicelioCanvas`
  está vacío y `sembrarNodo` es una función pura de una línea).
- Sin ramas verificadas: solo se leyó `main`. NO SÉ si hay otras ramas
  ni si Pages llegó a desplegarse.
