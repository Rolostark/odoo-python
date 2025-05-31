# Curso Python + Odoo: Personalización de UI

## 1. Cambiar etiquetas y estilos (XML + CSS)

```xml
<field name="name" string="Nombre del Curso"/>
```

```css
.o_form_view .o_form_label {
  color: #2E86C1;
}
```

## 2. Añadir widgets

```xml
<field name="fecha_inicio" widget="date"/>
```

---

## Resumen

- Personaliza la UI cambiando etiquetas, estilos y widgets en las vistas.