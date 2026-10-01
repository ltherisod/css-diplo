# POWER GYM — CSS Grid y Media Queries

La web está completa en contenido y estilos visuales.

Durante las clases se trabaja sobre este mismo proyecto para practicar **CSS Grid**, **Grid Areas**, **Flexbox** y **Media Queries**.

## Estructura

```text
/
├── index.html
├── pages/
│   ├── actividades.html
│   ├── planes.html
│   ├── nosotros.html
│   └── contacto.html
└── styles/
    └── styles.css
```

## En clase

- Navbar: usa Flexbox.
- Footer: usa Flexbox.
- `.cards-grid`: usa CSS Grid.
- `.card-destacada`: modifica el espacio que ocupa una tarjeta dentro de la grilla.
- `.layout-areas`: usa Grid y `grid-template-areas`.
- `.area-texto` y `.area-imagen`: identifican las áreas dentro del layout.
- `.hero h1`: se adapta usando `clamp()`.

## Responsive y Media Queries

El proyecto trabaja con una estrategia **Mobile First**.

Esto significa que primero se escriben los estilos para pantallas pequeñas y luego se agregan cambios cuando aumenta el ancho disponible.

### Mobile

Los estilos base funcionan sin Media Query.

Ejemplo:

```css
.cards-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 24px;
}
```

Las tarjetas se muestran en una sola columna.

### Tablet

Desde `768px` se puede modificar la distribución:

```css
@media (min-width: 768px) {
  .cards-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}
```

### Desktop

Desde `1024px` se realizan cambios más importantes en el layout:

```css
@media (min-width: 1024px) {
  .cards-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}
```

También se adapta la sección de Grid Areas.

En mobile:

```css
grid-template-areas:
  "texto"
  "imagen";
```

En desktop:

```css
grid-template-areas:
  "texto imagen";
```

De esta manera, el contenido puede pasar de estar apilado a mostrarse en dos columnas sin modificar el HTML.

El navbar también puede cambiar su distribución utilizando Flexbox:

```css
flex-direction: column;
```

en mobile y:

```css
flex-direction: row;
```

en desktop.

## Paleta

- Negro: `#0B0B0B`
- Negro secundario: `#171717`
- Verde lima: `#C7FF3D`
- Blanco: `#FFFFFF`
- Gris: `#C8C8C8`

## Buenas prácticas aplicadas

- HTML semántico: `header`, `nav`, `main`, `section`, `article`, `footer`.
- Un único archivo CSS compartido por las 5 páginas.
- Clases descriptivas y reutilizables.
- Imágenes con atributo `alt`.
- `meta viewport` en todas las páginas.
- Contenedor con `max-width` para evitar textos demasiado anchos.
- `object-fit` para mantener proporción de imágenes.
- Uso de `fr` para crear columnas flexibles.
- Uso de `gap` para separar elementos de Grid y Flexbox.
- Mobile First como estrategia responsive.
- Media Queries con `min-width`.
- Breakpoints de referencia en `768px` y `1024px`.
- Separación clara del CSS por secciones y comentarios.
- El HTML se mantiene y CSS se encarga de reorganizar el contenido según el tamaño de pantalla.

> Las imágenes se cargan desde Unsplash y necesitan conexión a Internet.