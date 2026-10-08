# Semana N°4
## Clase 7 - Pseudoclases y Pseudoelementos

---

### Pseudoclases

Las Pseudoclases son *estados* de los elementos html que podemos estilizar con css.
Se utilizan indicando primero el elemento html, class o id y luego se llama al estado con :estado.
Ejemplo:
```img:hover{}```
Contamos con multiples pseudoclases para utilizar.
Algunas de ellas son:
1. :hover. Sirve para indicar el estado de cuando se pasa el cursor por encima del elemento
2. :active. Indica el estado del elemento cuando es clickeado o se mantiene clickeado
3. :focus. Se usa en *input* y sirve para indicar cuando el usuario está "posado" en ese recuadro de escritura
4. :visited. Se utiliza para indicar que un enlace ya ha sido visitado.
5. :first-child y :last-child. Son estados en los que podemos dar un estilo personalizado al primer o ultimo hijo de un bloque para resaltarlo.
6. :nth-child. Este cuenta con multiples opciones en las que podemos seleccionar un hijo o varios hijos en especifico y luego darles estilos personalizados o variados.
7. Hay muchas más, por eso podemos visitar [Mozilla Developer](https://developer.mozilla.org/es/docs/Learn_web_development/Core/Styling_basics/Pseudo_classes_and_elements) para buscar alguna otra en particular.

---

### Pseudoelementos

Los pseudoelementos son elementos "ficticios" que vamos a crear para resaltar otros.
Se utilizan indicando primero el elemento html, class o id y luego se llama al elemento con ::elemento. Lo importante es que nunca nos debe faltar en el bloque la propiedad **content** y su valor con **""**
Ejemplo:
```h3.price::before```

Contamos con multiples pseudoelementos.
Algunos de ellos son:
1. ::before y ::after. Estos nos permiten indicar algún elemento o contenido antes o después del contenido.
2. ::placeholder. Nos permite darle estilo al placeholder del *input*.
3. ::selection. Nos permite darle estilo al contenido seleccionado (texto) al clickear y arrastrar el mouse.
4. ::first-letter y ::first-line. Nos ayudan a darle estilo personalizado a la primer letra de un texto o a la primera línea de un párrafo.
7. Hay muchos más, por eso podemos visitar [Mozilla Developer](https://developer.mozilla.org/es/docs/Learn_web_development/Core/Styling_basics/Pseudo_classes_and_elements) para buscar algún otro en particular.

---

## Clase 8 - Bootstrap

Bootstrap es una herramienta que nos brinda componentes preestilizados y responsivos para usar en nuestro proyecto

Para empezar a trabajar con Bootstrap, primero tenemos que ir a la [página oficial](https://getbootstrap.com/) y, en la sección *"include via CDN"*, copiar el ```link``` en el head y también el ```script``` al final del body, antes del cierre del mismo y luego del cierre del footer.

**Bootstrap** trabaja exclusivamente con las clases aplicadas en el archivo html.

Contenido que vimos:
### Grid System

El grid system es un sistema de grillas que se arma por medio de clases.
Pasos para *Grid System*
1. .container. El contenedor principal del todo el sistema.
2. .row. Contenedor que hace referencia a las filas
3. .col. Contenedor que hace referencia a las columnas
*Grid System* cuenta con un sistema de 12 columnas por fila. Cada fila debe lograr llegar a la cantidad de 12 columnas.
Hay varias maneras de trabajar las filas
Podemos indicar simplemente ```.row``` o bien podemos indicar cuantas columnas queremos que haya por fila con ```.row-cols-#```. El número indica cuantos elementos habrá dentro de cada fila.
Otra forma es indicar cuanto vale cada columna. ```.col``` le dara el valor en base a la cantidad de elementos .col haya en la .row. Sino podemos indicar cuanto vale cada .col con ```.col-#```.
También podemos armar las columnas y las filas en base a la medida responsive que deseemos.
Las medidas son:
1. xsm = <576px
2. sm = ≥576px
3. md = ≥768px
4. lg = ≥992px
5. xl = ≥1200px
6. xxl = ≥1400px
Para indicar cuando debe aplicar la columna debemos indicarselo antes del valor de .col. Ejemplo ```.col-lg-#```. El valor por defecto de ```.col-#``` se aplica desde xsm en adelante.
Usando *grid system* podemos ordenar otros elementos de Bootstrap.

---

### NavBar

Cuando vimos *NavBar* vimos la importancia de ir acomodando cada una de las propiedades y de los valores *aria* de la misma.
Si queremos que la barra permanezca cerrada, en la nav con class "navbar", debemos eliminar la class "navbar-expand-lg" para poder utilizar la nav.
Además, debemos tener cuidado con los estilos predefinidos de la barra y aplicarle nuestros estilos personalizados.

---

### Carousel

El carrusel es un elemento muy poderoso de Bootstrap pero debemos ser muy cuidadosos al armarlo.
Cuando le indiquemos las rutas de las imágenes, no debemos asignarle tamaño a las imágenes, sino dejar que tomen su tamaño original. Esto logrará *"romper"* el layout de la página, pero para darle un tamaño bien armado debemos utilizar *Grid System*.
También debemos ser precavidos con el **ID** que viene precargado en el carousel. Cuando terminemos de armarlo, utilizamos la lupa del menú de VSCode y cambiamos el valor de ese **ID** en todos los lugares donde se repite.
Si utilizamos más de 3 slides, debemos agregar el valor de estas slides en la sección de *"carousel-indicators"* para ir agregando los diferentes *#* de cada slide.
**-Recordatorio:** como Bootstrap trabaja con JS, debemos entender que JS empieza a indexar desde el 0 y no el 1. Por eso el 0 es la primer img, el 1 es la segunda...

---

Además, tenemos muchos otros componentes que podemos utilizar de Bootstrap. Se puede utilizar a Gusto. Pero es importante **recordar**
## Tengo que usar Bootstrap, pero también tengo que utilizar html y css.
Usarlo no es Abusarse de su uso. En el proyecto es requisito ver que saben trabajar con css nativo o vanilla
Por eso, la recomendación siempre es usar la NavBar en **TODOS** los *html* y el *carousel* o algún otro componente en otras páginas. Pero luego, hacer el resto con html y css

---

# Muchos éxitos en sus proyectos