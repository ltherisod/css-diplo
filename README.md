# POWER GYM — Módulo 6: migración a SCSS

El sitio conserva las **cinco páginas**, la paleta negra y verde lima, Bootstrap, las animaciones y el responsive del proyecto anterior. No se cambiaron los HTML.

## Ver la página en tu computadora

Abrí `index.html` en el navegador (o con Live Server). El archivo `styles/styles.css` original está incluido para poder ver la página incluso antes de instalar Sass.

## Instalar y compilar Sass localmente

1. Abrí la carpeta del proyecto con VS Code.
2. En la terminal ejecutá `npm install` (Node y npm ya deben estar instalados).
3. Ejecutá `npm run sass` para compilar una vez.
4. Para trabajar en vivo usá `npm run sass:watch` y dejá la terminal abierta.
5. Modificá **solamente los archivos `.scss`**, no el CSS compilado.

El CSS compilado queda en `styles/styles.css`, que es el archivo enlazado en los 5 HTML. Sass también se puede ejecutar con `npx sass --watch scss/main.scss:styles/styles.css`.

## Arquitectura

- `scss/main.scss`: único punto de entrada; agrupa todo mediante `@use`.
- `scss/utilities/_variables.scss`: paleta original, medidas y tokens.
- `scss/utilities/_mixins.scss`: Flexbox, Grid, foco y media queries `mobile`, `tablet`, `desktop` con `@content`.
- `scss/utilities/_extends.scss`: placeholder `%flex-centrado` usado mediante `@extend`.
- `scss/base/`: reglas generales y tipografía.
- `scss/layout/`: header, navegación, hero, secciones, áreas y footer.
- `scss/components/`: botones, cards, carousel, formularios y demostraciones de animaciones.

**Responsive:** siguiendo el enfoque del profesor, los `@include m.mobile`, `@include m.tablet` y `@include m.desktop` están dentro del parcial correspondiente al elemento (no en un único `_responsive.scss`). Conservamos los cortes originales: 767, 768 y 1024 px. El diseño sigue siendo mobile-first.

## Respaldo del estilo anterior

`backup-style.css` es una copia íntegra del CSS anterior a la migración; **no se debe editar**. El archivo `styles/styles.css` es el CSS utilizado por las páginas y se reemplaza al compilar Sass. El respaldo sirve para comparar y recuperar los estilos si hiciera falta.

## Git y dependencias

`.gitignore` excluye `node_modules/` y los mapas `.css.map`. Se incluyen `package.json` (y `package-lock.json` cuando se genere con `npm install`), `scss/`, `styles/styles.css`, HTML e imágenes.

## Nota de verificación

El CSS que acompaña al ZIP reproduce exactamente el CSS original. Al instalar Sass ejecutá `npm run sass` para compilar el código SCSS refactorizado. Los HTML no necesitan vincular ningún archivo `.scss`.
