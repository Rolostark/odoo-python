# Curso Python + Odoo: Reportes PDF (QWeb templates)

## 1. Definir template QWeb para PDF

```xml
<template id="reporte_curso">
  <t t-call="web.html_container">
    <t t-foreach="docs" t-as="curso">
      <h2><t t-esc="curso.name"/></h2>
      <p><t t-esc="curso.descripcion"/></p>
    </t>
  </t>
</template>
```

## 2. Acción para reporte

```xml
<report
    id="action_reporte_curso"
    model="academia.curso"
    string="Imprimir Curso"
    report_type="qweb-pdf"
    name="mi_modulo.reporte_curso"
    file="mi_modulo.reporte_curso"/>
```

---

## Resumen

- Usa QWeb para crear reportes PDF personalizados.