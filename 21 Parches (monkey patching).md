# Curso Python + Odoo: Parches (Monkey Patching)

## 1. Sobrescribir un método en tiempo de ejecución

```python
from odoo.addons.base.models.res_partner import ResPartner

def nuevo_metodo(self):
    print("Método modificado dinámicamente")

ResPartner.nuevo_metodo = nuevo_metodo
```

---

## Resumen

- Monkey patching permite modificar funciones o métodos en tiempo de ejecución (usarlo con precaución).