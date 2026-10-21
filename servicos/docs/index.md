# Golden Path para Serviços

!!! note "Conteúdo demonstrativo"
    Exemplo de uma jornada para criar, validar e operar um serviço. Os nomes de ferramentas,
    controles e etapas devem ser adaptados aos padrões aprovados pela organização.

Este guia acompanha uma equipe desde a ideia inicial até a operação em produção. O caminho
prioriza ownership claro, mudanças pequenas, controles automatizados e evidências que possam
ser consultadas depois.

## Jornada

1. **[Preparação](1-preparacao/pre-requisitos.md)**: confirme os pré-requisitos e crie o repositório.
2. **[Construção](2-construcao/estrutura.md)**: estruture o código, escreva testes e empacote em container.
3. **[Validação](3-validacao/pipeline-ci.md)**: pipeline de CI com qualidade e segurança como barreiras.
4. **[Produção](4-producao/deploy.md)**: deploy progressivo, observabilidade e operação.

## Resultado esperado

Ao final da jornada, o serviço:

| Aspecto | Resultado |
|---------|-----------|
| Catálogo | Registrado no Backstage com owner, system e lifecycle |
| Documentação | TechDocs com visão geral, arquitetura e runbook |
| Qualidade | Testes automatizados no CI, cobertura acompanhada |
| Segurança | Sem segredos no repo; dependências e imagem escaneadas |
| Operação | Health checks, métricas, logs, alertas e rollback testado |

Exemplo de serviço que segue este caminho:
[demo-service](http://localhost:3000/catalog/default/component/demo-service).
