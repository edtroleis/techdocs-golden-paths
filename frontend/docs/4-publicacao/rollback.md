# Rollback

Mantenha as últimas versões publicadas em prefixos versionados:

```text
releases/2026-10-20-a1b2c3/
releases/2026-10-21-d4e5f6/   ◀── atual
```

Rollback = apontar a origem da CDN (ou copiar `index.html`) para a versão anterior e invalidar
`index.html`. Leva segundos e não exige novo build.
