# CSS · Clase 1

Proyecto preparado para la primera clase de la Diplomatura de CSS.

## Estructura

```text
css-clase-1/
├── index.html
├── styles/
│   └── styles.css
└── ejemplos/
    ├── 01-link-roto/
    ├── 02-selector-no-coincide/
    ├── 03-especificidad/
    └── 04-error-sintaxis/
```

## Proyecto principal

Abrí `index.html`.

Está preparado para explicar:

- Vinculación de CSS externo.
- Anatomía de una regla.
- Selector, propiedad y valor.
- Selectores de etiqueta.
- Selectores de clase.
- Selector de ID.
- Agrupación de selectores.
- Comentarios en CSS.

No utiliza todavía:

- margin
- padding
- border
- Flexbox
- Grid
- pseudoclases como `:hover`

Esos contenidos aparecen más adelante en el curso.

---

# PPT 10 · “Mi CSS no aplica”

Dentro de `ejemplos/` hay cuatro errores preparados.

## 01 · Link roto

El HTML apunta a una ruta de CSS que no existe.

Objetivo de la demo:

1. Abrir la página.
2. Mostrar que no tiene estilos.
3. Inspeccionar con DevTools.
4. Revisar el `<link>`.
5. Cambiar:

```html
<link rel="stylesheet" href="css/styles.css">
```

por:

```html
<link rel="stylesheet" href="styles/styles.css">
```

Idea clave: si la hoja no está vinculada, ninguna regla puede aplicarse.

---

## 02 · Selector no coincide

La hoja está correctamente vinculada, pero el HTML usa:

```html
class="mensaje"
```

y el CSS intenta seleccionar:

```css
.mensage
```

Objetivo:

- Mostrar que la regla no aparece en el panel Styles.
- Corregir el nombre del selector.

Idea clave: si la regla no aparece en DevTools, primero revisamos si el selector realmente coincide con el elemento.

---

## 03 · Especificidad

Dos reglas intentan cambiar el mismo elemento:

```css
.mensaje {
  color: blue;
}

#mensaje-principal {
  color: red;
}
```

El elemento tiene clase e ID.

Objetivo:

- Inspeccionar el elemento.
- Ver una propiedad tachada.
- Explicar que la regla existe, pero perdió frente a otra con mayor especificidad.

Idea clave:

> ¿La regla aparece?
> - No → selector o vínculo.
> - Sí, pero tachada → perdió por cascada/especificidad.

---

## 04 · Error de sintaxis

Hay una declaración escrita con `=` en lugar de `:`.

Objetivo:

- Detectar que una declaración inválida es ignorada por el navegador.
- Corregir la sintaxis.

Idea clave: CSS intenta seguir funcionando aunque encuentre una declaración inválida; por eso a veces “solo una cosa” parece no funcionar.
