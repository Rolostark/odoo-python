# Curso Python + Odoo: Crear rutas API (JsonRPC)

## 1. Crear endpoint usando JsonRPC

```python
from odoo import http

class MiApiController(http.Controller):
    @http.route('/miapi/curso', type='json', auth='public')
    def obtener_cursos(self):
        cursos = http.request.env['academia.curso'].search([])
        return [{'id': c.id, 'name': c.name} for c in cursos]
```

---

## Resumen

- Usa `@http.route` con `type='json'` para exponer rutas tipo API en Odoo.