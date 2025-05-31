# Curso Python + Odoo: Clases y Objetos (POO)

## Introducción

Odoo está basado en la Programación Orientada a Objetos (POO) de Python.

---

## 1. Definir una clase en Python

```python
class Vehiculo:
    def __init__(self, marca, modelo):
        self.marca = marca
        self.modelo = modelo
    
    def descripcion(self):
        return f"{self.marca} {self.modelo}"
```

---

## 2. Crear un objeto

```python
coche = Vehiculo("Toyota", "Corolla")
print(coche.descripcion())
```

---

## 3. Ejemplo en Odoo: Modelo como clase

```python
from odoo import models, fields

class BibliotecaLibro(models.Model):
    _name = 'biblioteca.libro'
    titulo = fields.Char("Título")
    autor = fields.Char("Autor")
    
    def mostrar_descripcion(self):
        for libro in self:
            print(f"{libro.titulo} por {libro.autor}")
```

---

## Resumen

- Las clases encapsulan datos y lógica.
- Los modelos en Odoo heredan de `models.Model` y funcionan como clases.