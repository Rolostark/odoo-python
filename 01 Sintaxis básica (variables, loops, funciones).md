# Curso Python + Odoo: Sintaxis Básica

## Introducción

Este módulo cubre la sintaxis básica de Python, necesaria para trabajar con Odoo.

---

## 1. Variables

```python
# En Python no necesitas declarar el tipo de variable
numero = 10
texto = "Hola Odoo"
flotante = 3.14
```

---

## 2. Bucles (Loops)

```python
# Bucle for
for i in range(5):
    print("Iteración:", i)

# Bucle while
contador = 0
while contador < 5:
    print("Contador:", contador)
    contador += 1
```

---

## 3. Funciones

```python
def saludar(nombre):
    return f"Hola, {nombre}"

print(saludar("Odoo"))
```

---

## 4. Ejemplo en Odoo: Uso de Sintaxis Básica

```python
from odoo import models, fields

class DemoModelo(models.Model):
    _name = 'demo.modelo'
    name = fields.Char("Nombre")
    
    def imprimir_nombres(self):
        for registro in self:
            print(f"Nombre del registro: {registro.name}")
```

## 4. Ejemplo en Odoo: Uso de Sintaxis Básica explicacion

```python
# Importar las clases necesarias de Odoo:
# - models: Para crear nuevos modelos/tablas de base de datos
# - fields: Para definir los campos/columnas del modelo
from odoo import models, fields

# Definición de un nuevo modelo (tabla en la base de datos)
class DemoModelo(models.Model):
    # Nombre técnico del modelo que usará Odoo (debe ser único en el sistema)
    # Convención: 'nombre.modulo' en minúsculas y con puntos
    _name = 'demo.modelo'
    
    # Campo de tipo Char (texto corto) llamado 'name'
    # Por convención, Odoo usa 'name' como campo descriptor por defecto
    # El parámetro "Nombre" es el label que se mostrará en las vistas
    name = fields.Char("Nombre")
    
    # Método personalizado que imprime los nombres de los registros
    # 'self' puede contener uno o múltiples registros (recordset)
    def imprimir_nombres(self):
        # Iterar sobre todos los registros en el recordset (self)
        for registro in self:
            # Imprimir en consola el nombre de cada registro
            # f-string (formatted string) para interpolación de variables
            print(f"Nombre del registro: {registro.name}")
```

---

## Resumen

- Declarar variables en Python es sencillo.
- Los bucles ayudan a iterar sobre elementos.
- Las funciones encapsulan lógica reutilizable.
- Estos conceptos se usan en métodos de modelos Odoo.
