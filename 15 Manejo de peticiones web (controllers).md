# Curso Python + Odoo: Manejo de Peticiones Web (Controllers)

## 1. Crear un controlador HTTP

```python
from odoo import http

class WebController(http.Controller):
    @http.route('/web_demo', auth='public', website=True)
    def web_demo(self, **kw):
        return "<h1>¡Hola desde Odoo Controller!</h1>"
```

---

## Resumen

- Los controllers manejan rutas y peticiones HTTP personalizadas.