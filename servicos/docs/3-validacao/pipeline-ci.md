# Pipeline de CI

```text
push/PR ─▶ lint ─▶ testes ─▶ build da imagem ─▶ scans ─▶ build do TechDocs
```

| Etapa | Ferramenta sugerida | Bloqueia o merge? |
|-------|---------------------|-------------------|
| Lint e formatação | ruff / eslint | Sim |
| Testes + cobertura | pytest / jest | Sim |
| Build da imagem | podman / buildah | Sim |
| Scan de dependências e imagem | Trivy | Sim, para CVEs críticas |
| Scan de segredos | gitleaks | Sim |
| TechDocs | `techdocs-cli generate` | Sim |

!!! note "Documentação também é validada"
    Doc quebrada é build quebrado: o `mkdocs.yml` usa `strict: true`.
