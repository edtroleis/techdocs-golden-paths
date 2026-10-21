# Operação

## Runbook

Todo serviço mantém em `docs/runbook.md`:

- Como fazer deploy e rollback.
- O que cada alerta significa e o primeiro passo de resposta.
- Dependências e como verificar cada uma.
- Contatos de escalonamento.

## Incidentes

1. Reconheça o alerta e abra o canal do incidente.
2. Mitigue primeiro (rollback, feature flag), investigue depois.
3. Comunique o status em intervalos regulares.
4. Faça o pós-incidente sem culpados, com ações registradas.

## SLOs

| SLO | Meta sugerida |
|-----|---------------|
| Disponibilidade | 99,9% / 30 dias |
| Latência p95 | < 300 ms |
