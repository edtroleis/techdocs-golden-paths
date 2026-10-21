# Criar o repositório

## Pelo template (recomendado)

1. No Backstage, clique em **Create**.
2. Escolha o template de serviço da sua linguagem.
3. Informe nome, descrição, owner e system.
4. O template cria o repositório com estrutura, pipeline, `catalog-info.yaml` e `docs/` prontos.

## Manualmente

```bash
gh repo create minha-org/meu-servico --private --clone
cd meu-servico
```

Adicione no mínimo:

```yaml
# catalog-info.yaml
apiVersion: backstage.io/v1alpha1
kind: Component
metadata:
  name: meu-servico
  annotations:
    backstage.io/techdocs-ref: dir:.
spec:
  type: service
  lifecycle: experimental
  owner: meu-time
  system: meu-sistema
```

## Proteções do repositório

- Branch `main` protegida: merge só por PR, com CI verde e 1 aprovação.
- `CODEOWNERS` apontando para o time dono.
- Dependabot/Renovate habilitado.
