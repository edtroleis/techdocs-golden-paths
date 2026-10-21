# Pré-requisitos

## Antes de escrever código

- [ ] O problema e o usuário do serviço estão descritos (uma página basta).
- [ ] Existe um **time dono** (Group no catálogo) que vai operar o serviço.
- [ ] O serviço tem um **System** de destino no catálogo.
- [ ] As decisões de arquitetura relevantes foram discutidas (veja a
      [Wiki de Arquitetura](http://localhost:3000/docs/default/component/wiki-arquitetura)).
- [ ] Os dados tratados foram classificados (veja a
      [Wiki de Compliance](http://localhost:3000/docs/default/component/wiki-compliance)).

## Ambiente local

| Ferramenta | Versão | Manual |
|------------|--------|--------|
| OpenShift Dev Spaces | workspace do repositório | [Manual de OpenShift Dev Spaces](http://localhost:3000/docs/default/component/manual-dev-spaces) |
| Podman | 5.x | [Manual de Podman Desktop](http://localhost:3000/docs/default/component/manual-podman-desktop) |
| Git + GitHub CLI | recente | — |
| Runtime da linguagem | versão LTS aprovada | — |

!!! tip "Sem instalar nada"
    No Dev Spaces, Git, Podman e o runtime já vêm no workspace definido pelo `devfile.yaml`.
    O [WSL](http://localhost:3000/docs/default/component/manual-wsl) está descontinuado como ambiente local.
