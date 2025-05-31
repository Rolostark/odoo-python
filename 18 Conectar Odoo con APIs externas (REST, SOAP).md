# Curso Python + Odoo: Conectar Odoo con APIs externas (REST, SOAP)

## 1. Consumir API REST

```python
import requests

class ApiService(models.Model):
    _name = 'api.service'

    def obtener_datos(self):
        response = requests.get('https://api.externa.com/data')
        if response.status_code == 200:
            return response.json()
```

## 2. Consumir API SOAP

```python
from zeep import Client

client = Client('http://api.externa.com/servicio?wsdl')
result = client.service.Metodo()
```

---

## Resumen

- Usa librerías externas (`requests`, `zeep`) para consumir APIs desde Odoo.