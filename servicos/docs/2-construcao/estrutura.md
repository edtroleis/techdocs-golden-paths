# Estrutura do serviço

```text
meu-servico/
├── catalog-info.yaml      # registro no Backstage
├── mkdocs.yml + docs/     # TechDocs
├── openapi.yaml           # contrato da API
├── src/                   # código
├── tests/                 # testes
├── Containerfile          # imagem
└── .github/workflows/     # CI/CD
```

## Princípios

| Princípio | Na prática |
|-----------|------------|
| Configuração por ambiente | Variáveis de ambiente; nada de config por ambiente no código |
| Stateless | Estado em banco/fila gerenciados |
| Contrato primeiro | `openapi.yaml` revisado antes da implementação |
| Logs em stdout | JSON estruturado, com `trace_id` |

## Endpoints obrigatórios

| Endpoint | Uso |
|----------|-----|
| `/health` | Liveness: o processo está vivo |
| `/ready` | Readiness: dependências acessíveis |
| `/metrics` | Métricas no formato Prometheus |
