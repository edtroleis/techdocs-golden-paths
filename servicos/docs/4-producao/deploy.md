# Deploy

## Ambientes

| Ambiente | Gatilho | Aprovação |
|----------|---------|-----------|
| dev | Merge na `main` | Automática |
| staging | dev verde | Automática |
| produção | staging verde | Manual, dentro da janela |

## Estratégia

- **Progressivo**: canary ou rolling, com verificação automática de métricas.
- **Rollback** em um comando, testado antes do primeiro deploy.
- **Migrações de banco** compatíveis com a versão anterior (expand/contract).

```text
v1 ──▶ canary 10% v2 ──(métricas ok)──▶ 50% ──▶ 100%
                     └─(erro)──▶ rollback para v1
```
