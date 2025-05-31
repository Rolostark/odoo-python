# Curso Python + Odoo: Personalización de Facturas/Contratos

## 1. Heredar y modificar el template de factura

```xml
<template id="report_invoice_document_inherit" inherit_id="account.report_invoice_document">
  <xpath expr="//h2" position="before">
    <p>¡Gracias por tu compra!</p>
  </xpath>
</template>
```

---

## Resumen

- Puedes personalizar los PDF heredando y modificando los QWeb templates estándar.