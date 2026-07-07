# Renata Dantas — tour 3D (Apto 117)

Experiência web em 3D com Three.js — site **estático**, sem build step.

## Rodar local

O `.glb` é carregado por `fetch`, então precisa ser servido via HTTP (não abrir com `file://`):

```bash
python3 -m http.server 8080
# abra http://localhost:8080
```

## Deploy na Vercel

Site estático, sem framework. Nas configurações do projeto:

- **Framework Preset:** Other
- **Build Command:** _(vazio)_
- **Output Directory:** `.` _(raiz)_

O `index.html` já está na raiz do repositório, então funciona sem configuração adicional.

## Estrutura

- `index.html` — página + toda a lógica (câmera guiada por scroll, hotspots, overlays)
- `apto-117.opt.glb` — modelo 3D otimizado (~29 MB)
- `public/fotos/` — imagens dos hotspots

## Atalhos de dev (no navegador)

- Tecla **D** — editor do trilho de câmera (keyframes)
- Tecla **H** — editor de hotspots (clique na cena pra soltar um pin)
