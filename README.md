# Semana 2

## Clase 3: Box-Modeling, Display & Position

### Box Modeling:

Propiedades vistas:
- `margin`: Permite agregar espacio **por fuera** de elemento.

- `padding`: Permite agregar espacio **por dentro** del elemento.

- `box-sizing: border-box;`: Indica que el tamaño (height y width) del elemento se calcula con el padding y el border asignado.

- `Border`: Recibe 3 parametros cómo mínimo: *tamaño en px*, *tipo de borde* y *color*. Ej: `border: 1px solid blue;`. Dibuja un borde del elemento

- `border-radius`: Recibe valor en px e indica cuanto se deben redondearlas esquinas del borde.

Para más lectura sobre el border, acceder a [W3School Border](https://www.w3schools.com/css/css_border.asp)

---

### Display:

1. `none`. Simplemente desaparece el elemento, deja de ocupar su espacio en la visual.

2. `block`. El display por defecto de la mayoría de los elementos. Significa que el elemento va a ocupar el total del ancho de pantalla y siempre va a ir hacia abajo un salto de linea.

3. `inline`. Display que permite que cada elemento ocupe el alto y ancho de su **CONTENIDO** y, si hubiera lugar, permite que se posicione otro elemento *inline* a su lado. **NO** se puede asignarle width ni height.

4. `inline-block`. Display que permite que cada elemento pueda disponer del espacio de su contenido y a su vez que se forme uno del lado de otro siempre que el ancho de lugar. **SÍ** se le puede asignar width y height.

---

### Position:

1. `static`. Posición estatica que traen por defecto **TODOS** los elementos. No cambia el flujo de lectura y construcción del **HTML**.

2. `relative`. Posición que permite mover un elemento hacia la dirección indicada con: `top`, `right`, `bottom` & `left`. **NO** lo elimina del flujo de lectura y construcción del archivo **HTML**

3. `absolute`. Posición que permite mover un elemento hacia la dirección indicada con: `top`, `right`, `bottom` & `left`. ***SÍ*** lo elimina del flujo de lectura y construcción del archivo por lo que hay que tener en cuenta que el siguiente elemento va a ocupar su lugar en la lectura y construcción del archivo. El elemento con positión `absolute` se va a superponer a cualquier otro elemento.

4. `fixed`: Posición que me permite indicar donde quiero que un elemento "viva" constantemente y me acompañe cuando hago scroll. ***SÍ*** lo elimina del flujo de lectura y construcción del archivo por lo que hay que tener en cuenta que el siguiente elemento va a ocupar su lugar en la lectura y construcción del archivo. El elemento con positión `fixed` se va a superponer a cualquier otro. Esta position convierte al elemento a `inline`, por lo tanto su tamaño será su contenido.

5. `sticky`: Posición que me permite indicar a partir de que medida quiero que mi elemento me acompañe cuando hago scroll. ***NO*** elimina al elemento del flujo de lectura y construcción.
 
---

## Clase 4: Flexbox

### Flexbox o modelo de cajas flexibles

Me permite trabajar desde el contenedor padre para ordenar a sus hijos

Propiedades con las que debo trabajar:

1. `display: flex;` --> Indica que el contenedor el flex (no confundir con el valor `flexbox`)

2. `flex-directión` --> Indica la dirección del contenedor flexible. Por defecto, su valor es `row` pero podemos utilizar los valores `column`, `row-reverse` & `column-reverse`.

3. `flex-wrap` --> Indica el agrupamiento del contenedor. Por defecto, su valor es `nowrap`, pero podemos utilizar los valores `wrap` & `wrap-reverse`.

4. `flex-flow` --> Es una combinación de `flex-direction` y `flex-wrap`. Se debe poner en el orden mencionado arriba.

5. `justify-content` --> Justificar el contenido en el **EJE PRINCIPAL** del elemento flexible. Por ejemplo, si el elemento es `row` el **EJE PRINCIPAL** es el ***horizontal***. Recibe los valores: `start`, `center`, `end`, `space-around`, `space-between` & `space-evenly`.

6. `align-items` o `align-content` --> Primero tengo que entender cuando usar cada uno. `items` lo utilizamos cuando es ***unilinear*** mientras que `content` lo utilizo cuando es ***multilinear***. `items` puede recibir los valores: `start`, `center` & `end`, mientras que `content` puede recibir los valores: `start`, `center`, `end`, `space-around`, `space-between` & `space-evenly`.

7. `gap` --> Indica cuanto se separarán los elementos hijos entre sí.

8. `align-self` y `justify-self` --> se aplica directamente a los hijos y cumple la misma función que `align-items` y `justify-content`.

9. `flex-basis` --> Indica el tamaño "ideal" del elemento hijo.

10. `flex-grow` & `flex-shrink` --> Indica el tamaño que debe crecer (`grow`) o reducirse (`shrink`) el elemento hijo con respecto a sus hermanos. Sus valores son: `0` para no modificarse, `1` para que su modificación sea menor a sus hermanos & `2` para que su modificación sea mayor a sus hermanos.

11. `flex` --> Funciona cómo `flex-flow` al reducir en este caso a `flex-grow`, `flex-shrink` & `flex-basis` respectivamente
 
#### Enlaces alternativos

[Documentación de Flexbox](developer.mozilla.org/es/docs/Web/CSS/Guides/Flexible_box_layout/Basic_concepts)

[Machete / guía visual de Flexbox](stackblitz.com/edit/stackblitz-starters-xcpnm3an?file=index.html)

[Ejemplo de un sitio con 5 archivos HTML conectados a un mismo CSS](stackblitz.com/edit/stackblitz-starters-dojwviav?file=index.html)