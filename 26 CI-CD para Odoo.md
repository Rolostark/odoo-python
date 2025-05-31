# Curso Python + Odoo: CI/CD para Odoo

## 1. Ejemplo con GitHub Actions

```yaml
name: Odoo CI
on: [push]
jobs:
  test:
    runs-on: ubuntu-latest
    services:
      postgres:
        image: postgres:13
        env:
          POSTGRES_USER: odoo
          POSTGRES_PASSWORD: odoo
          POSTGRES_DB: odoo
        ports:
          - 5432:5432
    steps:
      - uses: actions/checkout@v2
      - name: Configurar entorno Python
        run: |
          python -m pip install --upgrade pip
          pip install -r requirements.txt
      - name: Ejecutar tests
        run: |
          # Comando para ejecutar tests Odoo
```

---

## Resumen

- CI/CD automatiza pruebas y despliegues de Odoo.