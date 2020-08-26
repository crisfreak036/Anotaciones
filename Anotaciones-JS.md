# Anotaciones Curso de JavaScript

## Definiciones Generales

- **ECMAScript:** Es la especificación para crear un lenguaje de scripting.
Los navegadores utilizan ECMAScript para interpretar el código JavaScript.
Dicta la reglas, detalles y lineamientos que un lenguaje de scripting debe seguir para ser considerado por ECMAScript.

- **JavaScript:** Es un lenguaje de Scripting que sigue la especificación de ECMAScript.
Es un dialecto del lenguaje de ECMAScript.

- **Frameworks JavaScript:** Angular, React y VueJS (entre otros) son frameworks front-end para aplicaciones utilizados para simplificar la construcción de aplicaciones avanzadas e interactivas. Estas librerías tienen la ventaja de que tienen varias funciones ya hechas que se encuentran disponibles para facilitar el desarrollo de aplicaciones.

- **NodeJS:** Plataforma hecha en JavaScript que se utiliza para realizar operaciones avanzadas y aplicaciones en servidores y computadoras con JavaScript. NodeJS permite la utilización de **NPM** que son una gran cantidad de librerías que se pueden utilizar con esta plataforma.

## Herramientas necesarias

Se recomienda instalar Visual Studio Code ya que tiene herramientas que funcionan perfectamente con JavaScript. En Visual Studio Code se recomienda instalar los siguientes paquetes:

- **Live Server:** Es de Ritwick Dey. Permite crear un servidor local. Gracias a Live Server se abrirá el navegador con el server local de nuestro archivo, en el navegador hay que tener la consola abierta.
- **Bracket Pair Colorizer:** Es de CoenraadS. Permite que los distintos paréntesis tenga colores diferentes según nivel al que se encuentren.
- **editor.wordWarp:** Al estar encendido permite que cuando se escriba mucho código, el código siempre se mantenga en pantalla (no se vaya para al lado).
- Se recomienda utilizar **emmet**. 

## Fundamentos de JavaScript 

### Primeros pasos con JavaScript

- Primero se debe crear un archivo con extensión *.js* con cualquier nombre (que no tenga caracteres raros) por ejemplo *app.js*.

- Luego se debe crear un archivo *index.html*. Dentro del archivo tecleando un signo de exclamación *!* y luego *TAB*, se crea la plantilla del HTML gracias a emmet.

- Para crear el primer programa en JS (Hola Mundo), dentro del index.html se debe agregar un `<div id="app"></div>` (donde el id será app, aunque puede ser el que uno deseé) la cual se irá llenando con JavaScript posteriormente.

- Luego hay que crear un etiqueta `<script></script>` la cual el navegador interpretará como que es JS y no otra cosa como HTML o CSS (cabe mencionar que para este último existe la etiqueta `<style></style>`).

- JavaScript permite hacer cosas como que el *div* vacío que creamos anteriormente haga algo. Por ejemplo un *Hola Mundo* sería de la siguiente manera: 

```html
<script>
    document.getElementById('app').innerHTML = 'Hola Mundo';
</script>
```
Lo anterior es en el caso de que no exista un archivo con extensión *.js* (en este caso existe el archivo y el ide del *div* vacío lleva en su id el nombre de ese archivo)

- Existiendo un archivo *.js* al cual hacer referencia, el bloque de código *html* queda de la siguiente manera:

```html
<script src=app.js></script> <!--Es similar a como se ponen imágenes en HTML, se pone sólo app.js porque ambos archivos se encuentran en el mismo directorio y al mismo nivel de lo contrario se coloca el directorio primero. Ejemplo JavaScript/app.js-->
```
- Se recomienda que la etiqueta *script* se encuentre antes del final de la etiqueta *body*. Esto se debe a que HTML carga desde arriba hacía abajo el código por lo cual poner código pesado de JS haría que se demorará más en cargar el página.

### Primer programa en JavaScript

El siguiente bloque de código pide mediante un prompt (una especie de cuadro de dialogo) un nombre y edad para luego mostrarlos en la página (el index.html básicamente). Lo anterior es posible debido a las etiquetas *div* y *script* que previamente pusimos en el *index.html*.

```js 
let nombre = prompt('¿Cual es tu nombre?'); /*Mediante un cuadro de dialogo pide el nombre. Cabe mencionar que el nombre no está siendo definido como un string o algo por el estilo, por lo cual se puede llenar con cualquier tipo de carácter*/

let edad = prompt('¿Cual es tu edad?'); /*Mediante un cuadro de dialogo pide la edad. Cabe mencionar que la edad no está siendo definida como un entero o algo por el estilo, por lo cual se puede llenar con cualquier tipo de carácter*/
/*Ambos cuadros de dialogo aparecen antes de que se termine de cargar la página*/

document.getElementById('app').innerHTML = `Bienvenido ${nombre} de ${edad} años`; /*Muestra el mensaje de Bienvenido {nombre} de {edad} años en el index.html debido a la sección asignada con las etiquetas scripts. Si no se llenan los cuadros de dialogo, el mensaje mostrará null en ambos "valores".*/
```
### La consola de Chrome

Cada navegador tiene su propia consola pero la de Chrome suele ser la mejor para trabajar con JS.

La consola es excelente al momento de probar el código de JS y ver errores en él.

La consola del navegador devuelve de un color los número y de otro color las cadenas de caracteres.

Existe algo que se llama la **Ventana Global** `document` que devuelve todo lo que tiene que ver con el HTML.

#### Enviar valores a la consola

Para enviar valores a la consola desde un archivo *JS* se debe ocupar el siguiente comando `console.log();`. Utilizar `console.log();` es muy útil debido a que permite comprobar las cosas que uno hace en *JS*.

```js
console.log("Enviando a la consola");
console.log('hasta aquí todo bien');
console.log(2+2); 
console.log(true); 
console.log('ID:'+ 20); /*Con console.log() se puede enviar todo tipo de valores a la consola.*/
```

Desde la consola del navegador se puede utilizar `console.log()`. Cabe mencionar que puede llegar a salir *undefined* debido a que la función no retorna un valor.

![Ejemplo Hola Mundo Consola Navegador](archivos/images/Hola-mundo-consola-navegador.png)

Dentro de la misma consola se pueden definir variables, las cuales se pueden enviar para que sean mostradas (muy parecido a como cuando se trabajaba en el IDE de python). Cabe mencionar que cuando se manda una variable por consola, se pone sólo el nombre de la variable y no entre comillas como cuando se manda una cadena de caracteres y cosas por el estilo.

![Ejemplo variable hola en Consola Navegador](archivos/images/variable-hola-por-consola-navegador.png)

Como se dijo anteriormente se puede enviar de todo por `console.log()` como por ejemplo arreglos.

La función anterior no es la única que existe para mostrar valores en la consola, también existe `console.table()` que muestra los valores en forma de una tabla. Ejemplo de lo anterior sería `console.table([1,2,3]);`

![Ejemplo console.table()](archivos/images/console.table().png)

Los anteriores son ejemplos de las funciones tipo console que tiene JS.

#### Tiempo de Ejecución

Para ver el tiempo de ejecución de nuestro código en JS existe las funciones `console.time();` y `console.timeEND();` las cuales marcan el inicio y el fin (respectivamente) del código que queremos ejecutar. Ambos reciben variables que pueden ser desde cadenas de caracteres puestas directamente o variables previamente definidas.

![Ejemplo console.time() y console.timeEND()](archivos/images/console.time()-y-console.timeEND().png)

### Consideraciones con el punto y coma

En JavaScript el *;* no es obligatorio pero por buena práctica se debe utilizar como si este fuera obligatorio. El punto y coma sirve para indicar cuando finaliza una línea de código.

### ESLint para solucionar errores de código

Revisa el código que se escribe para corregir el estilo en el cual se escribe el código de JS. Se debe configurar manualmente. ESLint puede corregir errores en base a lo que se configuró previamente.

### Variables en JavaScripts

Existen formas de darle nombre a una variable creada que aparte de ser una buena práctica, también ayudan a entender mejor el código. Estas formas son: 

- Camelcase: Es donde el segundo nombre de la variable lleva mayúscula. 

```js
var nombreVariable = 'Algo'; //Ejemplo de camelcase
```

- Underscore: Es donde los nombres de la variable se separan por un guión bajo.

```js
var nombre_variable = 'Algo'; //Ejemplo de underscore
```

- Pascalcase: Es donde todos los nombres de la variable llevan mayúscula.

```js
var NombreVariable = 'Algo'; //Ejemplo de pascalcase
```

Los siguientes tipos de variables son soportados por todos los navegadores.

#### Var

**Ya no se recomienda la variable de tipo VAR**

Para crear una variable de tipo *VAR* se debe hacer lo siguiente: 

```js
var nombre = 'Juan'; //Puede ser con comillas simples o dobles.

nombre = 'John'; //Sin necesidad de anteponer VAR se puede cambiar el contenido de la variable de tipo VAR, debido a que esta ya fue definida con anterioridad.

var nombre = 'Pedro'; //En este caso se vuelve a declarar la variable nombre y ya que es VAR no hay problema en hacerlo.

```

Primero se pone el tipo de la variable (*VAR* en este caso), luego un nombre para la variable **(los nombres de variables deben ser con letras primero y después números. Tampoco deben tener caracteres especiales al inicio)** y después lo que contendrá la variable.

De igual forma **se pueden inicializar variables sin valor**.

```js
var nombre; //La variable nombre de tipo VAR no tiene valor previamente definido
```
Además se pueden inicializar más de un mismo tipo de variable en una misma línea, sólo se tienen que separar por una coma.

```js
var variable = 0, variable2 = 1, variable3 = 2; //Se definieron tres variables en una sóla línea.
```

#### Let

**Se recomienda el uso de *let* cuando el valor será sobrescrito y no se volverá a definir**

A diferencia de *VAR*, no se pueden volver a declarar. Sólo se puede volver a dar valor.

```js
let variable1 = 'Libro'; //Se crea la variable1 de tipo let que contiene a Libro

variable1 = 'Libro 1'; //Se cambia el valor de la variable1 a Libro 1

let variable1 = 'Libro 2' //Tira error debido a que al ser de tipo let no se puede volver a declarar
```

#### Const

**Se recomienda su uso cuando se sabe que el valor asignado se mantendrá constante siempre**.

Las variables de tipo *const* deben inicializarse siempre, no pueden ir vacías desde su creación. Tampoco se le pueden reasignar un valor a este tipo de variable. 

```js
const producto = 'Libro'; //Se define una variable producto de tipo const

console.log(producto); // Se muestra por consola del navegador la variable producto

producto = 'Libro2' // La consola tira muestra el siguiente error: Uncaught TypeError: Assignment to constant variable.
```

