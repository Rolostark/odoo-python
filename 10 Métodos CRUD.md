# Curso Python + Odoo: Métodos CRUD

## 1. Crear (Create)

```python
nuevo = self.env['academia.curso'].create({'name': 'Curso Python', 'descripcion': 'Aprende Python'})
```

## 2. Leer (Read)

```python
cursos = self.env['academia.curso'].search([('name', '=', 'Curso Python')])
```

## 3. Actualizar (Write)

```python
cursos.write({'descripcion': 'Curso actualizado'})
```

## 4. Eliminar (Unlink)

```python
cursos.unlink()
```

---

## Resumen

- CRUD: Crear, Leer, Actualizar, Eliminar registros de modelos.