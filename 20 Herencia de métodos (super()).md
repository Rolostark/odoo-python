# Curso Python + Odoo: Herencia de Métodos (super())

## 1. Sobrescribir un método y llamar a super()

```python
from odoo import models

class ResPartner(models.Model):
    _inherit = 'res.partner'

    def write(self, vals):
        # Acción antes de la llamada al método original
        print("Actualizando partner")
        resultado = super().write(vals)
        # Acción después
        return resultado
```

---

## Resumen

- Usa `super()` para extender la lógica de métodos existentes.