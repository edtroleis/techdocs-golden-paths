# Golden Path para Frontend

!!! note "Conteúdo demonstrativo"
    Exemplo de jornada para criar e publicar uma aplicação frontend estática em CDN. Adapte
    ferramentas e controles aos padrões aprovados pela organização.

Objetivo: sair do zero e ter um frontend publicado em CDN, com pipeline, testes e rollback,
**em menos de 1 dia**.

## Jornada

| Etapa | Tempo estimado | Resultado |
|-------|----------------|-----------|
| [1. Preparação](1-preparacao/pre-requisitos.md) | 30 min | Repositório criado a partir do template |
| [2. Construção](2-construcao/stack-e-estrutura.md) | 3–4 h | Aplicação funcionando localmente |
| [3. Validação](3-validacao/testes.md) | 1–2 h | Testes, performance e acessibilidade no CI |
| [4. Publicação](4-publicacao/build-upload.md) | 1 h | Site na CDN, com cache e rollback |

## Arquitetura de referência

```text
Navegador ─▶ CDN (cache na borda) ─▶ Storage de objetos (arquivos estáticos)
     │
     └──▶ APIs de backend (domínio próprio, CORS restrito)
```

APIs consumidas pelo frontend seguem o
[Golden Path para Serviços](http://localhost:3000/docs/default/component/golden-path-servicos).
