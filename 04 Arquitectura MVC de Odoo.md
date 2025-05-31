# Curso Python + Odoo: Arquitectura MVC en Odoo

## Introducción

Odoo utiliza la arquitectura Modelo-Vista-Controlador (MVC).

---

## 1. Modelo

Define la estructura de los datos.

```python
from odoo import models, fields

class Libro(models.Model):
    _name = 'biblioteca.libro'
    titulo = fields.Char("Título")
    autor = fields.Char("Autor")
```

---

## 2. Vista

Define cómo se muestran los datos al usuario (XML):

```xml
<record id="view_form_libro" model="ir.ui.view">
  <field name="name">biblioteca.libro.form</field>
  <field name="model">biblioteca.libro</field>
  <field name="arch" type="xml">
    <form>
      <field name="titulo"/>
      <field name="autor"/>
    </form>
  </field>
</record>
```

---

## 3. Controlador

Gestiona la lógica y las peticiones web (opcional):

```python
from odoo import http

class BibliotecaController(http.Controller):
    @http.route('/biblioteca/libros', auth='public')
    def lista_libros(self, **kw):
        return "Listado de libros"
```

---

## Resumen

- Modelo: estructura de datos.
- Vista: interfaz de usuario.
- Controlador: lógica y rutas.