# Cache e invalidação

| Arquivo | `Cache-Control` |
|---------|-----------------|
| `assets/*` (com hash) | `public, max-age=31536000, immutable` |
| `index.html` | `no-cache` |
| `config.json` | `no-store` |

Com essa política, um deploy só precisa invalidar `index.html` e `config.json` na CDN.
