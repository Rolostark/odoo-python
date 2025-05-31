# Curso Python + Odoo: Herencia de Vistas (xpath)

## 1. Modificar una vista existente usando xpath

```xml
<record id="view_form_partner_inherit" model="ir.ui.view">
  <field name="name">res.partner.form.inherit</field>
  <field name="model">res.partner</field>
  <field name="inherit_id" ref="base.view_partner_form"/>
  <field name="arch" type="xml">
    <xpath expr="//field[@name='name']" position="after">
      <field name="twitter_user"/>
    </xpath>
  </field>
</record>
```

---

## Resumen

- Usa `xpath` para insertar, modificar o eliminar elementos en vistas heredadas.