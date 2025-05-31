# Curso Python + Odoo: Crear Modelos (models.Model)

## 1. Crear un modelo básico

```python
from odoo import models, fields

class AcademiaCurso(models.Model):
    _name = 'academia.curso'
    name = fields.Char("Nombre del Curso", required=True)
    descripcion = fields.Text("Descripción")
    fecha_inicio = fields.Date("Fecha de Inicio")
```

---

## Resumen

- Crea una clase que herede de `models.Model`.
- Define el nombre técnico con `_name`.
- Agrega campos usando `fields`.