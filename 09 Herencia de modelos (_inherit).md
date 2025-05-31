# Curso Python + Odoo: Herencia de Modelos (`_inherit`)

## 1. Heredar y extender un modelo existente

```python
from odoo import models, fields

class ResPartner(models.Model):
    _inherit = 'res.partner'
    twitter_user = fields.Char("Usuario de Twitter")
```

---

## Resumen

- Usa `_inherit` para añadir campos o lógica a modelos existentes de Odoo.