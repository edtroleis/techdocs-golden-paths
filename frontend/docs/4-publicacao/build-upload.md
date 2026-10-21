# Build e upload

```text
merge na main ─▶ npm ci ─▶ npm run build ─▶ upload dist/ ─▶ config.json do ambiente ─▶ invalidação
```

```bash
npm ci
npm run build
# exemplo genérico de upload para storage de objetos
storage-cli sync dist/ s3://meu-frontend-prod/ --delete
```

- Arquivos com hash no nome (`assets/index-3f2a.js`) são imutáveis.
- `index.html` e `config.json` não têm hash e são sempre revalidados.
