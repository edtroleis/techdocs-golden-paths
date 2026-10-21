# Stack e estrutura

| Camada | Escolha padrão |
|--------|----------------|
| Build | Vite |
| UI | React + TypeScript |
| Estilo | CSS Modules ou biblioteca de design system aprovada |
| Testes | Vitest + Testing Library; Playwright para e2e |
| Lint | ESLint + Prettier |

```text
meu-frontend/
├── catalog-info.yaml
├── docs/ + mkdocs.yml
├── public/
├── src/
│   ├── components/
│   ├── pages/
│   ├── services/        # chamadas às APIs
│   └── main.tsx
├── tests/
└── .github/workflows/
```
