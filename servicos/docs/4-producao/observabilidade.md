# Observabilidade

| Sinal | Padrão | Exemplo |
|-------|--------|---------|
| Logs | JSON em stdout com `trace_id` | `{"level":"info","msg":"pedido criado","trace_id":"abc"}` |
| Métricas | RED: rate, errors, duration | `http_requests_total`, `http_request_duration_seconds` |
| Traces | OpenTelemetry | Propagação de contexto entre serviços |

## Alertas mínimos

| Alerta | Condição | Link |
|--------|----------|------|
| Indisponível | `/health` falhando por 2 min | Runbook |
| Erros | 5xx acima do SLO por 5 min | Runbook |
| Latência | p95 acima do SLO por 10 min | Runbook |

Todo alerta aponta para o **runbook** do serviço no TechDocs.
