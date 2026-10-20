# Semana N°6
## Clase 9 - Instalación de SASS y Conocimientos básicos

### Instalación

1. Debemos instalar [NODEJS](https://nodejs.org/es) de su página oficial. Clickeamos en "obtener Node" y descargamos el instalador .msi para Windows o .pkg para MacOs.

2. Verificamos la versión abriendo cmd o powershell y ejecutamos el comando ```node --version```.

3. En nuestro **VSCode** con el proyecto abierto, abrimos una terminal ```ctrl + j``` y ejecutamos ```npm i -g sass```.

4. Verificamos la versión de sass con el comando ```sass --v```.

Nota: Si les surge el error de *"No pudimos avanzar porque la ejecución de Scripts está deshabilitada"* debemos hacer lo siguiente:

1. Abrimos **Powershell** como administrador.

2. Ejecutamos el siguiente comando: ```Set-ExecutionPolicy RemoteSigned -Scope CurrentUser```

3. Cuando nos pida confirmar, escribimos **O** y le damos *Enter*

4. Listo. Scripts activos.

5. Reintentamos los pasos que se nos hayan bloqueado en la instalación anterior.

---

### Configurando SASS

1. Lo primero que debemos hacer es una copia (backUp) de mi archivo .css

2. Luego empiezo con la creación de la estructura de SASS
    1. Creo la carpeta *sass*.
    2. Creo el archivo *main.scss*.
    3. Dentro de *sass* creo las carpetas:
        1. layout.
        2. utilities.
        3. components.
    4. Dentro de *layout* creo los archivos basados en los archivos .html
    5. Dentro de *utilities* creo los archivos:
        1. _reset.scss
        2. _variables.scss
        3. _animations.scss
        4. _mixins.scss
    6. Dentro de *components* creo los archivos:
        1. _header.scss
        2. _footer.scss

Nota: recordar que los partials (los archivos que son dependencia de main.scss) se deben llamar utilizando primero _ y luego el nombre. Pero al llamarlos con la regla **@use** los llamo sin el _

---

### Variables

Dentro del archivo *_variables.scss* debo crear las variables necesarias para reutilizar en el proyecto.
Si no tengo variables, puedo pedirle a la IA que me genere algunos colores para mi proyecto y que me recomiende algunas fuentes. Tomo 2 fuentes y 4/5 colores y los armo cómo variables

Las variables se definen con el selector *$* y luego el nombre.

Ejemplo:

```$bg-ppal: #aabbcc;```

Luego para utilizarla en los archivos, tengo que llamar a la regla **@use** y llamar al archivo *variables*, luego definir el archivo como *v* y llamar a la variable donde la necesite.

Ejemplo:

    @use "variables" as v;

    header{
        background-color: v.$bg-ppal;
        }

---

### Nesting/Anidamiento

El nesting es la posibilidad de anidar selectores css para darle especificidad a mi codigo.

Por ejemplo, quiero llegar al *logo* que está dentro de la etiqueta *a* que está dentro de *nav* que está dentro de *header*

Entonces, el nesting correcto sería:

    header{
        nav{
            a{
                .logo{
                    height: 5vh;
                    width: auto;
                }
            }
        }
    }

---

## Clase 10 - SASS Avanzado



---

# Muchos éxitos en sus proyectos