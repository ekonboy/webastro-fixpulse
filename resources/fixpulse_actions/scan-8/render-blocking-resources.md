# FixPulse Patch Proposal

- Scan ID: `8`
- Issue Key: `render-blocking-resources`
- Severity: `critical`
- Impact: `100`
- Effort: `55`

## Summary (ES)

Reduce resources that block first paint.

## Suggested Paths

- `resources/**`
- `assets/**`
- `vite.config.*`
- `package.json`

## Steps (EN)

- Inline only critical CSS required for the first viewport.
- Move non-critical CSS/JS to deferred loading.
- Add preconnect/preload for critical fonts and key stylesheets.

## Evidence

- [other] https://fonts.bunny.net/css?family=outfit:400,500,600,700,800&display=swap (1 KB)

_Generated at 2026-02-17T13:15:16+00:00_
