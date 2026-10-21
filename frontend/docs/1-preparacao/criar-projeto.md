# Criar o projeto

## Pelo template (recomendado)

No Backstage, **Create** → template *Frontend estático*. Ele entrega:

- Projeto Vite + React + TypeScript.
- `catalog-info.yaml` com `spec.type: website`.
- Pipeline de CI/CD com publicação na CDN.
- `docs/` para o TechDocs.

## Manualmente

```bash
npm create vite@latest meu-frontend -- --template react-ts
cd meu-frontend
npm install
npm run dev
```
