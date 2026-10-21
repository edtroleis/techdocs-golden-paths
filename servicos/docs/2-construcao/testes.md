# Testes

## Pirâmide

| Nível | Quantidade | Executa em |
|-------|-----------|------------|
| Unitários | Muitos | Todo push |
| Integração (banco/fila em container) | Alguns | Todo PR |
| Contrato (API) | Por endpoint público | Todo PR |
| End-to-end | Poucos, fluxos críticos | Antes de produção |

## Regras

- Todo bug corrigido ganha um teste que o reproduz.
- Testes determinísticos: sem depender de horário, rede externa ou ordem de execução.
- Dependências externas em container durante o teste (Podman/Testcontainers).

```python
def test_health_returns_ok(client):
    response = client.get("/health")
    assert response.status_code == 200
    assert response.json() == {"status": "ok"}
```
