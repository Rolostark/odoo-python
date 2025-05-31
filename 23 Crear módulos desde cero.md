# Curso Python + Odoo: Crear módulos desde cero

## 1. Estructura básica

```
mi_modulo/
|-- __manifest__.py
|-- __init__.py
|-- models/
|   |-- __init__.py
|   |-- modelo.py
|-- views/
|   |-- modelo_views.xml
```

## 2. Manifest

```python
# __manifest__.py
{
    'name': "Mi Módulo",
    'version': '16.0.1.0.0',
    'depends': ['base'],
    'data': ['views/modelo_views.xml'],
}
```

---

## Resumen

- Un módulo es un conjunto de modelos, vistas y lógica agrupada.