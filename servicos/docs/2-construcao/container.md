# Container

## Containerfile de referência

```dockerfile
FROM registry.access.redhat.com/ubi9/python-312 AS build
WORKDIR /app
COPY requirements.txt .
RUN pip install --no-cache-dir --target /app/deps -r requirements.txt
COPY src/ src/

FROM registry.access.redhat.com/ubi9/python-312-minimal
WORKDIR /app
COPY --from=build /app /app
ENV PYTHONPATH=/app/deps
USER 1001
EXPOSE 8080
CMD ["python", "-m", "uvicorn", "src.main:app", "--host", "0.0.0.0", "--port", "8080"]
```

## Regras

- Imagem base aprovada e mínima.
- Usuário **não-root**.
- Uma imagem por versão, promovida entre ambientes (não rebuildar por ambiente).
- Tag imutável (SHA do commit), nunca só `latest`.

```bash
podman build -t meu-servico:dev .
podman run --rm -p 8080:8080 meu-servico:dev
```
