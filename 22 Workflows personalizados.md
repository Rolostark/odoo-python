# Curso Python + Odoo: Workflows personalizados

## 1. Usar estados (state) y botones

```python
from odoo import models, fields

class Proyecto(models.Model):
    _name = 'mi_modulo.proyecto'
    state = fields.Selection([
        ('borrador', 'Borrador'),
        ('progreso', 'En Progreso'),
        ('finalizado', 'Finalizado')
    ], default='borrador')

    def action_iniciar(self):
        self.state = 'progreso'
```

## 2. Botón en vista XML

```xml
<button name="action_iniciar" type="object" string="Iniciar"/>
```

---

## Resumen

- Los workflows se implementan con campos `state` y métodos asociados a botones.