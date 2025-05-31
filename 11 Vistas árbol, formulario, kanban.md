# Curso Python + Odoo: Vistas Árbol, Formulario y Kanban

## 1. Vista árbol (list)

```xml
<record id="view_tree_curso" model="ir.ui.view">
  <field name="name">academia.curso.tree</field>
  <field name="model">academia.curso</field>
  <field name="arch" type="xml">
    <tree>
      <field name="name"/>
      <field name="fecha_inicio"/>
    </tree>
  </field>
</record>
```

## 2. Vista formulario

```xml
<record id="view_form_curso" model="ir.ui.view">
  <field name="name">academia.curso.form</field>
  <field name="model">academia.curso</field>
  <field name="arch" type="xml">
    <form>
      <field name="name"/>
      <field name="descripcion"/>
    </form>
  </field>
</record>
```

## 3. Vista Kanban

```xml
<record id="view_kanban_curso" model="ir.ui.view">
  <field name="name">academia.curso.kanban</field>
  <field name="model">academia.curso</field>
  <field name="arch" type="xml">
    <kanban>
      <field name="name"/>
      <templates>
        <t t-name="kanban-box">
          <div>
            <strong><field name="name"/></strong>
          </div>
        </t>
      </templates>
    </kanban>
  </field>
</record>
```

---

## Resumen

- Árbol: tabla de registros.
- Formulario: detalles de un registro.
- Kanban: tarjetas visuales.