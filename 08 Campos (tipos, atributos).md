# Curso Python + Odoo: Campos (Tipos, Atributos)

## 1. Ejemplo de varios tipos de campos

```python
from odoo import models, fields

class Empleado(models.Model):
    _name = 'empresa.empleado'
    name = fields.Char("Nombre")
    edad = fields.Integer("Edad")
    salario = fields.Float("Salario")
    fecha_nacimiento = fields.Date("Fecha de Nacimiento")
    es_activo = fields.Boolean("Activo", default=True)
    departamento_id = fields.Many2one('empresa.departamento', string="Departamento")
```

---

## 2. Atributos útiles

- `required=True`: Campo obligatorio.
- `default=valor`: Valor por defecto.
- `readonly=True`: Solo lectura.

---

## Resumen

- Usa diferentes tipos de campos según la información a almacenar.