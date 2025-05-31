# Curso Python + Odoo: Manejo de Listas y Diccionarios

## Introducción

Las listas y diccionarios son estructuras fundamentales en Python y Odoo.

---

## 1. Listas

```python
colores = ['rojo', 'verde', 'azul']
print(colores[0])  # rojo

for color in colores:
    print(color)
```

---

## 2. Diccionarios

```python
persona = {'nombre': 'Ana', 'edad': 30}
print(persona['nombre'])  # Ana

for clave, valor in persona.items():
    print(f"{clave}: {valor}")
```

---

## 3. Ejemplo en Odoo

```python
from odoo import models, fields

class ListaEjemplo(models.Model):
    _name = 'lista.ejemplo'
    name = fields.Char("Nombre")
    
    def lista_colores(self):
        colores = ['rojo', 'verde', 'azul']
        for color in colores:
            print(color)
    
    def diccionario_persona(self):
        persona = {'nombre': self.name, 'edad': 25}
        print(persona)
```

---

## Resumen

- Las listas almacenan elementos ordenados.
- Los diccionarios almacenan pares clave-valor.
- Útil para manejar datos dinámicos en métodos Odoo.