# Curso Python + Odoo: Módulos, Modelos y Vistas

## Introducción

Odoo agrupa funcionalidades en módulos, que contienen modelos y vistas.

---

## 1. ¿Qué es un módulo?

Conjunto de archivos que agregan una funcionalidad específica a Odoo.

```
mi_modulo/
|-- __manifest__.py
|-- models/
|-- views/
```

---

## 2. Modelos

Definen la estructura de los datos.

```python
from odoo import models, fields

class Cliente(models.Model):
    _name = 'mi_modulo.cliente'
    nombre = fields.Char("Nombre")
```

---

## 3. Vistas

Definen la interfaz gráfica (XML):

```xml
<record id="view_form_cliente" model="ir.ui.view">
  <field name="name">mi_modulo.cliente.form</field>
  <field name="model">mi_modulo.cliente</field>
  <field name="arch" type="xml">
    <form>
      <field name="nombre"/>
    </form>
  </field>
</record>
```

---

## Resumen

- Módulo: conjunto de funcionalidad.
- Modelo: estructura de datos.
- Vista: interfaz gráfica.