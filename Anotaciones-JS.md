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

### Tiempo de Ejecución

Para ver el tiempo de ejecución de nuestro código en JS existe las funciones `console.time();` y `console.timeEND();` las cuales marcan el inicio y el fin (respectivamente) del código que queremos ejecutar. Ambos reciben variables que pueden ser desde cadenas de caracteres puestas directamente o variables previamente definidas.

![Ejemplo console.time() y console.timeEND()](archivos/images/console.time()-y-console.timeEND().png)