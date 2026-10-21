# Testes

| Tipo | Ferramenta | Executa em |
|------|------------|------------|
| Unitário/componente | Vitest + Testing Library | Todo push |
| End-to-end | Playwright | Todo PR (contra preview) |

```ts
import { render, screen } from '@testing-library/react';
import { App } from '../src/App';

test('mostra o título', () => {
  render(<App />);
  expect(screen.getByRole('heading', { level: 1 })).toBeInTheDocument();
});
```
