# Guia de Plantas (MVP)

Guia de plantas de interior agrupadas por cuidados, com diagnóstico de problemas por sintomas.
Site estático (HTML + JS puro), sem backend. Funciona como PWA: pode ser instalado na tela inicial e funciona offline.

## Estrutura
- `index.html` — o app inteiro (dados, ilustrações e interface)
- `manifest.webmanifest` — nome, cores e ícones para instalação
- `sw.js` — service worker (cache offline)
- `icons/` — ícones do app
- `.nojekyll` — faz o GitHub Pages servir os arquivos como estão

## Rodar localmente
O service worker só funciona via http(s), não abrindo o arquivo direto:

    python3 -m http.server 8000

Abra http://localhost:8000

## Publicar uma atualização
1. Edite os arquivos
2. Aumente `VERSION` em `sw.js` (ex.: "v1" → "v2")
3. `git commit` e `git push` — o GitHub Pages publica sozinho
