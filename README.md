# PulseSite Astro Demo

Landing demo en Astro para validar flujo completo de FixPulse (scan -> generate patch -> create PR -> revert PR).

## Requisitos
- Node 20+
- npm

## Desarrollo local
```powershell
cd m:\NODE\fixpulse\web-astro
npm install
npm run dev
```

Abre: `http://localhost:4321`

## Build
```powershell
npm run build
npm run preview
```

## Subir a GitHub
1. Crea un repo nuevo en GitHub (ej: `astro-fixpulse-demo`).
2. En esta carpeta:
```powershell
git add .
git commit -m "feat: initial astro demo for fixpulse phase2"
git branch -M main
git remote add origin https://github.com/<tu_usuario>/astro-fixpulse-demo.git
git push -u origin main
```

## Conectar con FixPulse (Create PR/Revert PR)
Configura en `apps/web/.env` del panel FixPulse:
```env
GITHUB_TOKEN=<token_con_repo_scope>
GITHUB_REPO=<tu_usuario>/astro-fixpulse-demo
FIXPULSE_REPO_PATH=m:\NODE\fixpulse\web-astro
FIXPULSE_REPO_DEFAULT_BRANCH=main
```

Luego:
- Ejecuta scan contra `http://localhost:4321` (o URL desplegada).
- En detalle técnico usa:
  - `Generate Patch`
  - `Create PR`
  - `Revert PR`
