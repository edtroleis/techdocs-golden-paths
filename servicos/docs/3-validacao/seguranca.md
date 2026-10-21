# Segurança

## Controles automatizados

| Controle | Quando | Evidência |
|----------|--------|-----------|
| Scan de segredos | Todo push | Relatório do CI |
| SCA (dependências) | Todo PR e diário | Relatório do CI / alertas |
| Scan de imagem | Todo build | Relatório do CI |
| SAST | Todo PR | Relatório do CI |

## Segredos

- Guardados no cofre de segredos; injetados em tempo de execução.
- Nunca em variáveis do repositório em texto claro, nem em logs.
- Rotação periódica e imediata em caso de vazamento.

Controles de compliance e evidências: veja a
[Wiki de Compliance](http://localhost:3000/docs/default/component/wiki-compliance).
