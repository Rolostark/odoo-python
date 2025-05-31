# Curso Python + Odoo: Webhooks

## 1. Crear endpoint para recibir webhooks

```python
from odoo import http

class WebhookController(http.Controller):
    @http.route('/webhook/recibir', type='json', auth='public')
    def recibir_webhook(self, **kwargs):
        # Procesar los datos recibidos
        datos = kwargs
        # Lógica personalizada...
        return {'status': 'ok'}
```

---

## Resumen

- Los webhooks son endpoints para recibir notificaciones de sistemas externos.