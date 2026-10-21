# Checklist de produção

- [ ] `catalog-info.yaml` com owner, system e lifecycle
- [ ] TechDocs com visão geral, arquitetura e runbook
- [ ] API registrada no catálogo (OpenAPI)
- [ ] `/health`, `/ready` e `/metrics`
- [ ] Logs estruturados com `trace_id`
- [ ] Alertas de disponibilidade, erro e latência
- [ ] Segredos no cofre, nenhum no repositório
- [ ] Imagem não-root, escaneada, com tag imutável
- [ ] Pipeline com testes, scans e build de docs
- [ ] Rollback testado
- [ ] SLOs definidos e publicados
