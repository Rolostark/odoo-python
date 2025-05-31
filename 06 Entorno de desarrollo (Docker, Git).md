# Curso Python + Odoo: Entorno de Desarrollo (Docker, Git)

## 1. Preparar el entorno con Docker

```bash
# Ejemplo básico de docker-compose.yml para Odoo + PostgreSQL
version: '3'
services:
  db:
    image: postgres:13
    environment:
      - POSTGRES_DB=postgres
      - POSTGRES_USER=odoo
      - POSTGRES_PASSWORD=odoo
    ports:
      - "5432:5432"
  odoo:
    image: odoo:16
    depends_on:
      - db
    ports:
      - "8069:8069"
    environment:
      - HOST=db
      - USER=odoo
      - PASSWORD=odoo
    volumes:
      - ./addons:/mnt/extra-addons
      - ./odoo.conf:/etc/odoo/odoo.conf
```

## 2. Uso básico de Git

```bash
git clone https://github.com/tu_usuario/tu_repo_odoo.git
cd tu_repo_odoo
git checkout -b mi_rama
# Realiza cambios...
git add .
git commit -m "Mi primer commit"
git push origin mi_rama
```

---

## Resumen

- Docker facilita el despliegue y aislamiento.
- Git permite el control de versiones y colaboración.