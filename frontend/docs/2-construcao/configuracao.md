# Configuração por ambiente

Um build estático não lê variáveis de ambiente em tempo de execução. Para manter **um único
artefato** promovido entre ambientes, carregue a configuração de um arquivo publicado junto:

```json
// /config.json (diferente por ambiente, publicado pelo pipeline)
{ "apiBaseUrl": "https://api.staging.exemplo.com" }
```

```ts
export async function loadConfig() {
  const res = await fetch('/config.json', { cache: 'no-store' });
  return (await res.json()) as { apiBaseUrl: string };
}
```

!!! warning "Nada sensível no frontend"
    Tudo que vai para o navegador é público. Chaves e segredos ficam no backend.
