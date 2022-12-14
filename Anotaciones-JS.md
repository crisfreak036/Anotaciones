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
var variable = 0, variable2 = 1, variable3 = 2; //Se definieron tres variables en una sola línea.
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

### Strings o Cadenas de Texto y sus métodos

#### Creación de un string

Los *strings* representan un texto que se le puede asignar a una variable.

Existen dos formas de crear una cadena de texto:

1. Creación del *string* mediante el uso de comillas dobles en el valor de la variable.

```js
//Creación de la variable producto
//Prima forma de crear un string
const producto = "Monitor de 20 pulgadas"; //La variable ya es un string al momento de ponerle las comillas en su definición
```
En este caso se **debe usar comillas dobles** al momento de darle valor a la variable.

2. Creación del *string* mediante el uso del objeto (quizás función, investigar más eso) `String()`.

```js
//Creación de la variable producto2
//Segunda forma de crear un string
const producto2 = String('Monitor 24 Pulgadas'); //El valor de la variable es dado en base al objeto String() que recibe la cadena de caracteres que nosotros enviemos entre comillas simples.
```
3. Creación de un nuevo objeto *string*.

```js
//Creación de la variable producto3
//Tercera forma de crear un string (es poco común)
const producto3 = new String('Monitor de 27 pulgadas'); // Aquí el String está siendo creado como si fuera un objeto nuevo
```
**Nota: En el caso de que se quiera poner comillas dobles o simples dentro de un string que comience y finalice con comillas dobles simples respectivamente, se debe ¿escapar? las comillas que no hagan referencia al final del string. Lo anterior se hace utilizando un backslash** 
```js
const producto = "Monitor de 20\" "
```

#### Métodos de un String

Debido a que los *strings* son una clase, estos cuentan con métodos que sirven para realizar distintas tareas de forma fácil y sencilla.

##### indexOf

Entrega en que posición del *string* se encuentran una palabra buscada. Entrega la posición dentro de la cadena de caracteres (el inicio de la palabra buscada) y si no se encuentra entrega un *-1*.

```js
/*variable.indexOf('palabra')*/

//Creación de la variable producto
const producto = "Tablet 7\" 8 Gb y 1 Gb Ram";

//Muestra por consola la variable producto
console.log(producto);

//Muestra la posición dentro del producto (que es un string) donde inicia la palabra Tablet
console.log(producto.indexOf('Tablet'));

//Cabe mencionar que el método diferencia entre minúsculas y mayúsculas
console.log(producto.indexOf('tablet')); //Muestra un -1 por consola

console.log(producto.indexOf('Monitor')); //Muestra -1 en la consola debido a que Monitor no se encuentra en la variable producto
```

##### Includes

Sirve para saber si dentro de una string se encuentra una palabra especifica. Este método **recibe** la palabra a buscar entre comillas simples y distingue entre minúsculas y mayúsculas, y **entrega** un valor booleano (true o false).

```js
/*variable.includes('palabra')*/

//Creación de la variable producto
const producto = 'Monitor de 32 pulgadas';

//Muestra por consola la variable producto
console.log(producto);

//Muestra true o false dependiendo de si la palabra Monitor se encuentra en el string producto
console.log(producto.includes('Monitor')); //Entrega True por consola

//Cabe mencionar que el método includes distingue entre minúsculas y mayúsculas
console.log(producto.includes('monitor')); //Entrega False por consola

console.log(producto.includes('Tablet')); //Entrega False por consola debido a que no se encuentra la palabra Tablet dentro del string producto
```

##### Length

Sirve para conocer la cantidad de caracteres que componen a un string. 

```js
/*variable.length()*/

//Creación de la variable producto2
const producto2 = 'Monitor 20 pulgadas';

//Creación de la variable cantidadCaracteres la cual contiene la cantidad de caracteres del string producto2
const cantidadCaracteres = producto2.length;

//Muestra por consola el valor de la variable producto2
console.log(producto2);

//Muestra por consola la cantidad de caracteres que componen a la variable producto
console.log(cantidadCaracteres);

/*No es necesario crear una nueva variable para la cantidad de caracteres del string*/
```

##### Concatenar un String (Unir Strings)

Sirve para unir strings. Existe tres formas para concatenar strings (la mejor es la tercera).

- **Forma 1:** Utilizando el método concat. El método concat une dos strings.

```js
//Se define la variable producto
const producto = 'Monitor 20 Pulgadas';

//Se define la variable precio
const precio = '30 USD';

//Se concatena la precio a la variable producto y se muestra por consola el resultado
console.log(producto.concat(precio)); //En la consola se muestra Monitor 20 Pulgadas30 USD

//Se concatena al producto la cadena de caracteres En Descuento
console.log(producto.concat(' En Descuento'));
```

- **Forma 2:** Utilizando el signo +. Es una sintaxis muy sencilla pero puede llegar a traer problemas cuando el output es muy grande.

```js
console.log( producto + precio ); //El signo + sirve para concatenar uno o más strings

console.log( producto + "Con un precio de: " + precio ); //Además se le pueden concatenar cadenas de caracteres que no necesariamente son variables previamente definidas 
```
- **Forma3:** Template Strings o Template Literal.

##### Template Strings (concatenación ECMAScript)

Con la llegada de ECMAScript 6, se introdujo un cambió a la concatenación de strings la cual se basa en la utilización del Backtick *`* en vez de comillas dobles o triples, además se elimina el uso del signo *+* y ahora para agregar una variable a lo que se quiere mostrar se utiliza la siguiente sintaxis ${variable}.

```js
console.log(`El producto ${producto} tiene un precio de ${precio}`); //Esta sintaxis es cómoda cuando se tiene un output muy grande.
```

##### Cortar espacios en blanco de un String

Para eliminar los espacios en blanco que vengan en una variable, se pueden utilizar los métodos trim(), trimStart() y trimEnd(), los cuales permiten eliminar los espacios en blanco tanto al inicio como al final, sólo los del inicio y sólo los del final respectivamente. Cabe mencionar que el método trim() es el más antiguo de los tres, ya que tanto trimStart() como trimEnd() son mucho más nuevos.

```js
// Definición de la variable producto con un valor tipo string que tiene muchos espacios
const producto = '     Monitor 20 Pulgadas     ';

// Se muestra por consola la variable producto
console.log(producto);

// Se muestra por consola el largo de la variable producto
console.log(producto.length); // El método length considera los espacios en blanco que contiene la variable

// Eliminación los espacios en blanco tanto al inicio como al final
console.log(producto.trim()); 

// Eliminación de espacios en blanco del inicio
console.log(producto.trimStart()); //trimStart se encarga de eliminar los espacios en blanco que se encuentran al inicio (no los del final) de la variable producto

// Eliminación de espacios en blanco del final
console.log(producto.trimEnd()); //trimEnd elimina los espacios en blanco que se encuentran al final de la variable producto (no los del inicio)

/* En JavaScript se pueden utilizar los métodos de forma encadenada, lo cual se llama Chaining o sea que se puede utilizar un método seguido de otro método */

console.log(producto.trimStart().trimEnd()); //La encadenación de trimStart().trimEnd() elimina los espacios en blanco tanto del inicio como del final de la variable producto
```
##### Replace

Sirve para reemplazar un palabra dentro de un *string* por otra como también se puede reemplazar el valor de un string por el de otro.

```js
// Definición de la variable producto
const producto = 'Monitor 20 Pulgadas';

// Se muestra por consola la variable producto
console.log(producto);

// Se reemplaza Pulgadas por comillas dobles "
console.log(producto.replace('Pulgadas', '"'));

// Se reemplaza Monitor por Monitor Curvo
console.log(producto.replace('Monitor','Monitor Curvo'));

/* Lo anterior sumamente util cuando se requiere reemplazar palabras de muchas variables */
```

##### Slice

Sirve para cortar un trozo del string indicando la posición del inicio del corte y el posición dle final del corte.

```js
console.log(producto.slice(0 , 10)); //Corta la variable producto desde la posición 0 hasta la posición 10 mostrando por consola Monitor 20

console.log(producto.slice(8)); //Corta la variable producto desde la posición 8 hasta el final del string. Lo anterior se debe a que no se le paso una posición de termino

console.log|(producto.slice(2 , 1)); //No muestra nada. Si el primer número es mayor que el segundo, JS no hará nada
```

##### Substring

Al igual que *variable.slice()* sirve para cortar un trozo del string pero con la gran diferencia que el utilizar *variable.substring()* permite que cuando el indice de inicio sea mayor que el indice de termino (*slice* en este caso no hace nada), *substring* interpreta que el indice menor es el de inicio y el indice mayor es el de termino.

```js
console.log(producto.substring(0 , 10)); //Corta la variable producto desde la posición 0 hasta la posición 10 mostrando por consola Monitor 20

console.log(producto.substring(10 , 0)); // Hace lo mismo que la línea de código anterior a pesar de que están mal ingresados los valores
```

##### Repeat

Sirve para repetir n cantidad de veces un *string*. Da igual que valor se le entregue al método, siempre se aproximará al entero más cercano.

```js
// Se define la variable texto la cual es la repetición triple de la cadena ' en Promoción'
const texto = ' en Promoción'.repeat(3);

//Se muestra en la consola el contenido de la variable texto
console.log(texto);
```

##### Split

Sirve para dividir una cadena de texto en base a un carácter o palabra que uno le entregue al método.

```js
// Se crea la variable hobbies que contiene una cadena compuesta por diferentes actividades
const hobbies = 'Leer, caminar, escuchar música, escribir, aprender a programar';

// Se divide la cadena contenida en la variable hobbies por el carácter "," y muestra en modo de tabla en la consola una tabla con las actividades ya separadas una de otras
console.table(hobbies.split(","));
```

##### Convertir en Mayúsculas

El método *toUpperCase()* sirve para transformar en mayúscula todos los caracteres de una cadena de texto contenida en una variable.

##### Convertir en minúsculas

El método *toLowerCase()* sirve para transformar en minúscula todos los caracteres de una cadena de texto contenida en una variable.

Lo anterior es muy util cuando existen datos que da igual si están en mayúsculas o minúsculas por lo cual se transforman todos a minúsculas y se trabajan de esa manera. Un ejemplo de lo anterior son los e-mails.

##### Convertir un número en string

El método *toString()* sirve para transformar un número en un string. Cabe mencionar que un número en string y un número normal tienen diferentes colores al ser mostrados en la consola del navegador y en JS no son lo mismo.

```js
// Se crea la variable precio que contiene un número
const precio = 300;

// Se muestra la variable precio por consola
console.log(precio);

// Se crea la variable precioString la cual contendrá una versión en string del precio (este paso no es necesario)
const precioString = precio.toString();

// Se muestra por consola la variable precioString (el uso de .toString() puede ser dentro de console.log())
console.log(precioString);
```
### Números en JavaScript

#### Creación de números en JavaScript

A diferencia de los otros lenguajes, en JavaScript todo los números se crean de la misma forma (ya sea un entero, un flotante o un double). Sumado a lo anterior hay que aclarar que un número de tipo *string* es distinto a un número como tal.

```js
/* Tipos de números que se pueden crear en JS*/

// Se crea la variable numero1 que es un número entero
const numero1 = 30;

// Se crea la variable numero2 que es un número entero
const numero2 = 20;

// Se crea la variable numero3 que es un flotante
const numero3 = 20.20;

// Se crea la variable numero4 que es un flotante
const numero4 = .102030;

// Se crea la variable numero5 que es un flotante
const numero5 = -20;
```

#### Operaciones en JavaScript

Existiendo números, existen operaciones matemáticas que se pueden realizar con ellos.

##### Suma 

Para la suma, se utiliza el operador *+*. Ya que las variables son números, no hay conflicto con respecto a la concatenación de *strings*.

```js
// Se crea la variable numero1 que es un número entero
const numero1 = 30;

// Se crea la variable numero2 que es un número entero
const numero2 = 20;

// Se crea la variable resultadoSuma que guardará el resultado de la Suma (este paso no es necesario)
let resultadoSuma;

// Suma 
resultadoSuma = numero1 + numero2;
```

##### Resta 

Para la resta se utiliza el operador *-*.

```js
// Se crea la variable resultadoResta que guardará el resultado de la Resta
let resultadoResta;

// Resta 
resultadoResta = numero1 - numero2;
```

##### Multiplicación

Para la multiplicación se utiliza el operador *\**.

```js
// Se crea la variable resultadoMulti que guardará el resultado de la Multiplicación
let resultadoMulti;

// Multiplicación
resultadoMulti = numero1 * numero2;
```

##### División 

Para la división se utiliza el operador */*.

```js
// Se crea la variable resultadoDivision que guardará el resultado de la División
let resultadoDivision;

// División
resultadoDivision = numero1 / numero2;
```
##### Modulo

El modulo de una división es el residuo que queda de la división entera ente el dividendo y el divisor. En el caso del modulo, el operador a utilizar es el *%*.

```js
// Se crea la variable resultadoModulo que guardará el resultado del Modulo
let resultadoModulo;

// Modulo
resultadoModulo = numero1 % numero2; 
```

#### El Objeto Math

En la consola del navegador se puede ingresar el código `Math` y presionar *enter* (existe en la ventana global de JS), de esta forma se pueden ver todos los métodos y funciones que contiene el objeto Math.

![Algunos métodos del objeto Math](archivos/images/objeto-math-algunas-funciones.png)

Se podría decir que es objeto hace lo que hacía la librería math en c o c++.

```js
/*Ejemplos de uso del objeto Math*/

// Creación de variable numeroPI que contiene el valor del número PI
const numeroPi = Math.PI;

// Muestra por consola el valor de la variable numeroPi
console.log(numeroPi);

// Redondea el valor de número Pi 
console.log(Math.round(numeroPi));

// Redondea 3.5 a 4
console.log(Math.round(3.5));

// Redondear al extremo superior siempre
console.log(Math.ceil(0.1));

// Redondear al extremo inferior siempre
console.log(Math.floor(0.9));

// Raíz cuadrada
console.log(Math.sqrt(4));

// Valor absoluto
console.log(Math.abs(-100));

// Potencia
console.log(Math.pow(2,2));

// Saber cual es el mínimo de una serie de números
console.log(Math.min(10,56,23,2,1));

// Saber cual es el máximo de una serie de números
console.log(Math.max(10,56,23,2,1));

// Aleatorio: Entrega un número aleatorio que pocas veces es entero
console.log(Math.random());

// Ejemplo número aleatorio del 0 al 30
const aleatorio = Math.floor(Math.random() * 30);
console.log(aleatorio);
```

#### El Orden de las Operaciones en JS

En JS existe un orden en el que se ejecutan las operaciones que al igual que en las matemáticas convencionales se rigen por PAPOMUDA (Paréntesis, potencias, multiplicación, división, adición y sustracción de izquierda a derecha)

#### Incrementos y Decrementos

Es importante saber como subir o bajar un valor en n unidades.

![Incremento por consola](archivos/images/Incremento-consola.png)

En la Ilustración anterior se puede observar el incremento de la variable puntaje dentro de la consola del navegador.

Al igual que el incremento, existe el decremento el cual se comporta como el incremento.

![Decremento por consola](archivos/images/Decremento-consola.png)

Los ejemplos anterior son para incrementar o disminuir en una unidad el valor de la variable pero, ¿Qué se hace si quiero aumentar o disminuir la variable en más de una unidad?. En la siguiente Ilustración se podrá observar que se hace para responder la pregunta antes planteada.

![Incremento y Decremento más de una unidad](archivos/images/Incremento-Decremento-sobre-una-unidad.png)

#### Convertir Strings a Números

Existen métodos que sirven para transformar  valores *strings* que representan un número. Para esto se ocupa el objeto *Number* y sus métodos.

```js
const numero1= "20"; // Tiene la representación de número pero es un string

// Muestra por consola la versión numérica entera del valor string de la variable numero1
console.log(Number.parseInt(numero1));
```

El ejemplo anterior transforma a entero la representación en *string* de la variable numero1.

Al igual que las representaciones enteras, existen las representaciones de tipo flotante que si se transforman con `Number.parseInt()`, se transformaran a entero perdiendo sus decimales. Para evitar lo anterior existe `Number.parseFloat()` el cual transforma las representaciones flotantes a números flotantes.

```js
const numero2= "20.2"; // Tiene la representación de un flotante pero es un string

// Muestra por consola la versión numérica entera del valor string de la variable numero2
console.log(Number.parseInt(numero2));

// Muestra por consola la versión numérica flotante del valor string de la variable numero2
console.log(Number.parseFloat(numero2));
```

Cabe mencionar que existe un método el cual permite saber si el valor de una variable es por ejemplo, un entero. Ese método es `Number.isInteger()`.

```js
const numero4= 20; // Es un número

let numero5; // Se crea la variable numero 5 vacía

// Muestra por consola un true debido a que numero4 es efectivamente un entero
console.log(Number.isInteger(numero4));

// Muestra por consola un false debido a que numero1 es un string
console.log(Number.isInteger(numero1));

// numero5 toma el valor numérico flotante de numero2
numero5 = Number.parseFloat(numero2);

// Muestra por consola una false debido a que numero5 es flotante y no un entero
console.log(Number.isInteger(numero5));
```

Por último, cabe mencionar que JS nos permite saber el tipo del valor de una variable con la función `typeof()`.

```js
console.log(typeof(numero1)); // Muestra el tipo de dato que tiene la variable numero1

console.log(typeof(numero2)); // Muestra el tipo de dato que tiene la variable numero2
```
### Operadores en JavaScript

En JS existen operadores que permiten la comparación de valores. Eso operadores son:

#### Operador Mayor que o Menor que

Permite comparar si un numero es mayor que otro. Retorna un true o un false al hacer la comparación.

```js
const numero1 = 20;
const numero2 = "20";
const numero3 = 30;

// Operador mayor a...
console.log(numero1 > numero3); // false
console.log(numero3 > numero1); // true

// Operador menor a...
console.log(numero1 < numero3); // true
```

#### Comparar 2 valores

Para comparar si un valor es igual a otro se recomienda el uso del *triple igual* `===`, ya que, el usar el *doble igual* (como en otros lenguajes) **no es una comparación estricta** debido a que en JS el doble igual lleva al mismo tipo de dato los valores, en cambio el *triple igual* no hace lo anterior.

```js
const numero1 = 20;
const numero2 = "20";
const numero3 = 30;

// Doble igual
console.log(numero1 == numero3); // false
console.log(numero1 > numero2); // true
/*Lo anterior se debe a que numero2 es un string que tiene formato de numero por lo cual cuando el doble igual lleva al mismo tipo de dato ambos números, estos serán iguales*/

// Triple igual o Comparador estricto
console.log(numero1 === numero2); // false
/*El comparador estricto se fija tanto en el valor como en el tipo de dato*/
```
Al igual que existe un comparador para saber si dos valores son iguales, existe un comparador con el cual se puede saber si dos valores son distintos, este comparador es `!=`.

```js
const numero1 = 20;
const numero2 = "20";
const numero3 = 30;

console.log(numero1 != numero3); // true
console.log(numero1 != numero2); // false
/*Lo anterior sucede debido a que este comparador solo compara los valores y no los tipos de datos*/

// Comparador distinto a... (estricto)
console.log(numero1 !== numero2); // true
/*numero1 y numero2 tienen el mismo valor pero son de distinto tipo de dato por lo cual para no tener problemas se recomienda transformar todo al mismo tipo de dato antes de comparar*/
```
#### Comparar Null y undefined en JavaScript

*Undefined* aparece cuando el valor de una variable no se encuentra definido a diferencia de *null* que debe ser asignado. Tanto *undefined* como *null*, JavaScript los interpreta como que tienen el mismo valor pero no tienen el mismo tipo de dato, ya que, el tipo de dato de *undefined* es undefined y el tipo de dato de *null* es object, debido a lo anterior se recomienda el uso del comparador estricto `===` cuando se comparen variables que contengan *undefined* o *null*.

```js
// Undefined
let numero;
console.log(numero); // undefined
/*Lo anterior se debe a que la variable esta definida pero su valor no*/
console.log(typeof numero); // undefined

// Null
let numero2 = null;
console.log(numero2); // null
console.log(typeof numero2); // object

// Comparación
console.log(numero == numero2); // true
/*JavaScript que el valor undefined y el valor null son iguales*/

// Comparación estricta
console.log(numero === numero2); // false
/*Se recomienda el uso de la comparación estricta en estos casos ya que a pesar de que JS interpreta que tanto null como undefined son el mismo valor, no tienen el mismo tipo de dato*/
```

### Booleans en JavaScript

#### Crear y Comparar Booleans
```js
const boolean1 = true; //Valor primitivo true
const boolean2 = false; //Valor primitivo false
const boolean3 = "true"; //String true, no booleano

//console.log(boolean1);
//console.log(boolean2);
//console.log(boolean1==boolean3); //Muestra un false

//const boolean4 = new Boolean(true); //Objeto no valor primitivo
//console.log(typeof(boolean4));
```

#### Más sobre Comparar Booleans
```js
const boolean1 = true; //Valor primitivo true
const boolean2 = false; //Valor primitivo false

console.log(boolean1 == boolean2); //false
console.log(boolean1 === boolean2); //false
console.log(boolean1 === true); //true
console.log(boolean1 === "true"); //false
```

#### Buenas practicas a la hora de evaluar un Boolean

Ahora se muestraq un código en donde dependiendo del varlo de _autenticado_, se muestra algo por conosola.

```js
const autenticado = true;

if(autenticado === true) {
    console.log('Si puedes ver Netflix')
} else {
    console.log('No, no puedes verlo')
}
```

El problema con el código el anterior es que la variable _autenticado_ de por si ya viene con el valor `true` por lo cual es innecesario realizar la comparación inicial, por lo cual se recomienda no hacerla, quedando de la siguiente manera el código:

```js
const autenticado = true;

if(autenticado) {
    console.log('Si puedes ver Netflix')
} else {
    console.log('No, no puedes verlo')
}
```

Otra forma en la que se puede escribir el código anterior es utilizando el **Operador Ternario**, en donde en una sola línea se puede escribir el código anterior.

```js
const autenticado = true;
console.log( autenticado ? 'Si está autenticado' : 'No está autenticado');
```

### Objetos en JavaScript

#### Crear Objetos en JavaScript

Los objetos permiten la agrupación de propiedades en una sola entidad, como se puede observar en el siguiente ejemplo donde se agruparon las variables _nombre_, _precio_ y _disponible_ en un sólo objeto llamado _producto_.

```js
const nombre = "Monitor 20 Pulgadas";
const precio = 300;
const disponible = true;

// Un objeto agrupa todo en una sola variable..

// Object Literal o Objeto Literal
const producto = {
    nombre: "Monitor 20 Pulgadas", // Propiedad o Llave del objeto
    precio: 300,
    disponible: true
}

console.log(producto);
```

#### Como acceder a los valores de un objeto

Los obejtos tienen algo llamado la _sintaxis de punto_, en la cual al escribir el nombre del objeto y un punto, se puede acceder a sus propiedades. Lo anterior se pude probar con el siguiente código.

```js
// Object Literal o Objeto Literal
const producto = {
    nombre: "Monitor 20 Pulgadas", // Propiedad o Llave del objeto
    precio: 300,
    disponible: true
}

// Acceder a las propiedades de un objeto mediante el uso de la sintaxis de punto

console.log(producto.nombre); // Muestra el contenido de la propiedad nombre
console.log(producto.precio); // Muestra el contenido de la propiedad precio
console.log(producto.disponible); // Muestra el contenido de la propiedad disponible

```

Existe una forma poco común con la cual se puede acceder a las propiedades de un objeto que se muestra en el siguiente código:

```js
// Object Literal o Objeto Literal
const producto = {
    nombre: "Monitor 20 Pulgadas", // Propiedad o Llave del objeto
    precio: 300,
    disponible: true
}

// Otra forma poco común de acceder a las propiedades de un objeto

console.log(producto['nombre']); // Muestra el contenido de la propiedad nombre
```

#### Agregar o eliminar Propiedades de un objeto

Una forma de agregar nuevas propiedades a un objeto es directamente en el código fuente del objeto.

Si se quiere **agregar** las propiedades luego de haber escrito el código y sin modificar el códgio fuente del objeto, hay que utilizar la _sintaxis de punto_ con un nombre de propiedad que no exista en el objeto (si la propiedad existe, esto la reescribirá), como si estuvieramos creando una nueva variable con su respectivo valor.

```js
producto.imagen = 'imagen.jpg'; // Agrega la propiedad imagen al objeto producto
```

Si se quiere **eliminar** una propiedad de un objeto sin modificar directamente el código fuente, hay que utilizar la palabra `delete` antes de la propiedad que se quiere eliminar la cual se debe escribir con su _sintaxis de punto_ correspondiente.

```js
delete producto.disponible // Elimina la propiedad disponible del objeto producto
```

#### Destructuring de Objetos

_Destructuring_ hace referencia a la asginación de los valores de de las propiedades de un objeto a variables comunes y corrientes en un sólo paso. Antes de ES6, se debeía crear una variable y asignarle el valor de la propiedad mediante la _sintaxis de punto_, esto se muestra en el siguiente código:

```js
// Object Literal o Objeto Literal
const producto = {
    nombre: "Monitor 20 Pulgadas", // Propiedad o Llave del objeto
    precio: 300,
    disponible: true
}

const nombre = producto.nombre; // Forma antigua de asignación
console.log(nombre);
```

Ahora mediante el _Object Destructuring_ se puede crear y asignar el valor a la variable en una sólo línea de la siguiente forma:

```js
// Object Literal o Objeto Literal
const producto = {
    nombre: "Monitor 20 Pulgadas", // Propiedad o Llave del objeto
    precio: 300,
    disponible: true
}

// Object Destructuring

const { nombre } = producto;
console.log(nombre);
```

Lo anterior se puede repetir cuantas propiedades se quieran extraer pero si todas las porpiedades pertenecen al mismo objeto, se puede extraer todas de una sola vez de la siguiente manera: 

```js
// Object Literal o Objeto Literal
const producto = {
    nombre: "Monitor 20 Pulgadas", // Propiedad o Llave del objeto
    precio: 300,
    disponible: true
}

// Object Destructuring

const { nombre, precio, disponible } = producto;
console.log(nombre);
console.log(precio);
console.log(disponible);
```

#### Objetos dentro de objetos

Los objetos pueden contener propiedades que son objetos, y estas propiedades objeto pueden tener propiedades objetos y así sucesivamente. Para acceder a las propiedades de estas propiedades objetos, se sigue utilizando la _sintaxis de punto_. Lo anterior se puede observar en el siguiente código:

```js
// Objetos dentro de Objetos

const producto = {
    nombre: "Monitor 20 Pulgadas",
    precio: 300,
    disponibilidad: true,
    /*informacion es un objeto que contiene objetos*/
    informacion: {
        medidas: {
            peso: '1kg',
            medida: '1m'
        },
        fabricacion: {
            pais: 'China'
        }
    }
}

console.log(producto);
console.log(producto.informacion.medidas.peso); // Muestra en consola el peso del producto
console.log(producto.informacion.fabricacion.pais); // Muestra en consola el país donde fue fabricado
```

#### Destructuring de Objetos Anidados

Al igual que con las propiedades normales, se puede realizar _Destructuring_ de propiedades objetos. Para esto, hay que añadir `:` al nombre de la propiedad objeto, seguido de un par de llaves en las que se indicará las propiedades que se quieren extraer.

```js
// Objetos dentro de Objetos

const producto = {
    nombre: "Monitor 20 Pulgadas",
    precio: 300,
    disponibilidad: true,
    informacion: {
        medidas: {
            peso: '1kg',
            medida: '1m'
        },
        fabricacion: {
            pais: 'China'
        }
    }
}

/*En este ejemplo, se crean las variables peso y medida, pero no las variables informacion y medidas*/
const { informacion: { medidas: { peso, medida } } } = producto;
console.log(peso);
console.log(medida);
```

Cabe mencionar que en la extracción anterior no se crean las variables `informacion` y `medidas`, para crearlas habría que agregarlas separadas por coma.

```js
/*En este ejemplo se crean variables tanto para informacion como para medidas*/
const { informacion, informacion: { medidas }, informacion: { medidas: { peso, medida } } } = producto;
console.log(informacion);
console.log(medidas);
console.log(peso);
console.log(medida);
```

#### Congelar un Objeto para no poder modificarlo

Aunque un objeto sea definido como una constante que no se puede modificar, sus propiedades si pueden modificarse.

```js
// Object Literal o Objeto Literal
const producto = {
    nombre: "Monitor 20 Pulgadas", // Propiedad o Llave del objeto
    precio: 300,
    disponible: true
}

producto.disponible = false; // Cambia el valor de la propiedad disponible a false

delete producto.precio; // Elimina la propiedad precio del objeto producto

producto.imagen = "imagen.jpg"; // Crea la propiedad imagen con un valor asignado

console.log(producto);
```

Si es que se quiere evitar que lo anterior suceda, hay que activiar el _modo estricto_, el cual se podría decir que ayuda a evitar malas practicas al momento de escribir código en JS. Para activarlo sólo hay que poner en la primera línea del archivo el lo siguiente `"use strict";`.

Con el modo estricto activo, se puede acceder a una serie de _Object Methods_ que permitirán evitar la modificación de los objetos, por ejemplo el método `Object.freeze()` "congela" el objeto, evitando que se le puedan aplicar modificaciones.

```js
const producto = {
    nombre: "Monitor 20 Pulgadas",
    precio: 300,
    disponibilidad: true,
    informacion: {
        medidas: {
            peso: '1kg',
            medida: '1m'
        },
        fabricacion: {
            pais: 'China'
        }
    }
}

Object.freeze( producto ); // No permite que el producto sea modificado
```

Cabe mencionar que si no se sabe el estado de "congelamiento" de un objeto, existe el método `Object.isFrozen()` el cual evalua si un objeto se encuentra "congelado".

```js
/*Muestra en consola un true o false dependinedo de si el objeto está congelado o no*/
console.log(Object.isFrozen(producto));
```

#### Sellar un Objeto

El sellado de un obejto, a diferencia del congelamiento de un objeto, evita que se añadan o eliminen propiedades pero si **permite que se modifiquen las existentes**. Para sellar un objeto se utiliza el método `Object.seal()` y para saber si un objeto se encuentra sellado, se utiliza el método `Object.isSealed()`.

```js
"use strict";

// Object Literal o Objeto Literal
const producto = {
    nombre: "Monitor 20 Pulgadas", // Propiedad o Llave del objeto
    precio: 300,
    disponible: true
}

Object.seal( producto ); // No permite que el producto sea modificado

producto.disponible = false;
console.log(producto);
//delete producto.disponible; // Muestra error en la consola

/*Muestra en consola un true o false dependinedo de si el objeto está sellado o no*/
console.log(Object.isSealed(producto));
```

#### Copiar 2 Objetos

Aquí se verá como unir dos objetos.
Existen dos formas de hacerlo.
_
1. **Método Assign:** El método assign copiar las propiedades del los objetos de derecha a izquierda, o sea, asigna las propiedades del _objeto2_ a _objeto1_ modificando el _objeto1_. Para utilizarlo hay que escirbir lo siguiente: `Objeto.assign(objeto1, objeto2)`

```js
/*Ejemplo uso del método assign*/
const producto = {
    nombre: "Monitor 20 Pulgadas", // Propiedad o Llave del objeto
    precio: 300,
    disponible: true
}

const medidas = {
    peso:'1kg',
    medida: '1m'
}

console.log(producto);
console.log(medidas);

/*Assign, asigna las propiedades del segundo objeto al primer objeto
provocando que el primer objeto sea modificado*/
const resultado = Object.assign(producto, medidas);
console.log(resultado);
//console.log(producto); // Para utilizar este console.log, hay que comentar el que sale más arriba
```

2. **Spread Operator o Rest Operator:** Lo que hace esto es copiar las propiedades de los obejtos que se quieran unir a la variable objeto en la cual se utilice el operador. En el siguiente código se muestra el uso de este operador.

```js
/*Ejemplo Spread Operator o Rest Operator*/
const producto = {
    nombre: "Monitor 20 Pulgadas", // Propiedad o Llave del objeto
    precio: 300,
    disponible: true
}

const medidas = {
    peso:'1kg',
    medida: '1m'
}

console.log(producto);
console.log(medidas);

/*A diferencia del método Assign, el Spread Operator no modifica el valor
del primer objeto*/
const resultado2 = { ...producto, ...medidas};
console.log(resultado2);
//console.log(producto); // Para utilizar este console.log, hay que comentar el que sale más arriba
```

#### Funciones en Objetos y acceder a sus valores

Utilización de la palraba reservada `this.`, el cual sirve para referencias a las propiedades del objeto, en espñol _this_ significa _esta_, es por eso que al utilizarlo con una propiedad es como decir _"esta.propiedad"_.

```js
const producto = {
    nombre: "Monitor 20 Pulgadas", // Propiedad o Llave del objeto
    precio: 300,
    disponible: true,
    mostrarInfo: function() {
        console.log(`El producto: ${this.nombre}, tiene un precio de: ${this.precio}`)
    }
}

producto.mostrarInfo(); // Forma de llamar a la función mostrarInfo perteneciente al objeto producto
```

#### Object Constructor

Es una forma de automatizar la creación de objetos cuando estos son muchos. Es una menra distinta de definición de objetos en comparación a la hasta ahora utilizada _Object Literal_. Este es más dinámico que _Object Literal_.

Esta forma conssite en la creación de una función que recibe los valores de las propiedades que se definen en la función. 

En el siguiente bloque de código se puede observar la sintaxis para la utilización del _Object Constructor_. 

```js
// Object Literal
const producto = {
    nombre: "Monitor 20 Pulgadas",
    precio: 300,
    disponible: true,
}
console.log(producto);

// Object Constructor
function Producto(nombre,precio) {
    /*El uso de this permite el almacenamiento de 
    los valores entregados dentro del objeto*/
    this.nombre = nombre;
    this.precio = precio;
    this.disponible = true;
}

const producto2 = new Producto("Monitor 24 Pulgadas",500);
console.log(producto2);
```

Esta forma de construir objetos era la que antiguamente soportaba JavaScript, ya que antes no aceptaba clases.

#### Object .keys .values y .entries

##### Método .keys

`Object.keys(<nombre-objeto>)` retorna un arreglo con las _keys_ o _propiedades_ del objeto.

```js
const producto = {
    nombre: "Monitor 20 Pulgadas",
    precio: 300,
    disponible: true,
}

console.log(Object.keys(producto));
```

##### Método .values
`Object.velues(<nombre-objeto>)` retorna un arreglo con las _values_ o _valores_ de las propiedades dle objeto.

```js
const producto = {
    nombre: "Monitor 20 Pulgadas",
    precio: 300,
    disponible: true,
}

console.log(Object.keys(producto));
```

##### Método .entries
`Object.entries(<nombre-objeto>)` retorna arreglos compuestos por el par _[key, value]_ que tenga el objeto.

```js
const producto = {
    nombre: "Monitor 20 Pulgadas",
    precio: 300,
    disponible: true,
}

console.log(Object.entries(producto));
```

### Arrays o Arreglos en JS
Permiten agrupar elementos del mismo tipo.

#### Crear Arrays en JS
Los arreglos se crean con corchetes `[]`, siemrpe que se vea algo en JS encapsulado en corchetes, es porque es un _arreglo_. Estos contienen solo valores a diferencia de los objetos que contienen llave y valor. Lo que se podría considerar un simil a la llave en los objetos, en los arreglos sería el _indice_ o _posición_ la cual parte desde el 0 en JS.

```js
// Creación más común
const numeros = [10,20,30];
console.log(numeros);

// Creación con constructor Array (menos común)
const meses = new Array('Enero','Febrero','Marzo');
console.log(meses);
```

Se pueden crear arreglos que contengan distintos tipos de elementos y también se pueden tener arreglos dentro de arreglos.

```js
// Un que contiene datos de todo tipo

const deTodo = ["Hola", 10, true, "si", null, { nombre: 'Nombre', algo: 'Algo'}, [1,2,3]];
console.log(deTodo);
```

#### Acceder a los valores de un Array

Para acceder a los valores, hay que utilizar el indice como se muestra en el siguiente ejemplo.

```js
const numeros = [10,20,30,40,50];
console.log(numeros);
console.table(numeros); // Permite mostrar en consola en formato de tabla el indice y el valor del contenido del arreglo

// Acceder al arreglo
console.log(numeros[0]);
```
En el caso de que se quiera acceder a un valor que de un arreglo que se encuentra dentro de un arreglo, hay que agregar otra dimensión de corchetes como muestra el siguiente ejemplo

```js
const numeros = [10,20,30,40,50,[1,2,3]];
console.log(numeros);
console.table(numeros); // Permite mostrar en consola en formato de tabla el indice y el valor del contenido del arreglo

// Acceder al arreglo
console.log(numeros[5][0]); // Se muestra el primer valor del arreglo contenido por el primer arreglo
``` 

#### Recorrer un Array

Para recorrer un arreglo se puede utilizar el iterador _for()_, el cual permitirá recorrer el arreglo desde un punto que nosotros indiquemos hasta un punto final que nosotros indiquemos. Para recorrer un arreglo desde su indice 0 hasta su último indice, hay que inicializar el iterador en 0 y determinar que el ciclo se repita mientras i sea menor al largo del arreglo, o sea, `i<arreglo.lenght`. En el siguiente código se puede observar lo antes mencionado.

```js
const meses = ['Enero','Febrero','Marzo','Abril','Mayo','Junio'];
console.table(meses);

// Obtener el tamaño de un arreglo
console.log(meses.length);

/*Recorre el arreglo mientras que el iterador sea menor al largo del arreglo*/
for(let i = 0;i<meses.length;i++){
    console.log(meses[i]);
}
```

#### Agregar nuevos valores a un arreglo

Los arreglos, sin importar que sean declarados como un _const_ pueden seguir siendo modificados.

```js
const meses = ['Enero','Febrero','Marzo','Abril','Mayo','Junio','Julio'];
console.table(meses);
meses[0] = 'Nuevo mes'; // Cambia el primer valor del arreglo por otro valor
console.table(meses);
```

La primera forma en la cual se puede agregar un nuevo elemento a un arreglo es asignando un valor a un indice que no tiene valor asignado.

```js
const meses = ['Enero','Febrero','Marzo','Abril','Mayo','Junio','Julio'];
console.table(meses); // Tiene ocupados los indices del 0 al 6

// Primer forma de añadir elementos a un arreglo

meses[7] = 'Último mes'; // Al no existir valor en ese indice, se asigna el nuevo valor a ese indice
console.table(meses);
```

**Nota: En el caso de que el indice elegido no sea consecutivo, como por ejemplo el indice 31 del ejemplo anterior, JS asigna valor al indice indicado sin asignarle valor a los indices anteriores a este**

#### Añadir nuevos elementos al fin o inicio de un arreglo

La forma más común para añadir elementos a un arreglo no es la que se mencionó anteriormente, sino que es es utilizando el método _push()_, el cual agrega un elemento al final del arreglo, asignandole el último indice consecutivo sin utilizar.

```js
const carrito = []; // Se inicializa vacío debido a que aún no se realizan compras
console.log(carrito);

// Definir producto
const producto = {
    nombre: "Monitor 32 pulgadas",
    precio: 400
}

// Se agrega un producto al final del arreglo carrito
carrito.push(producto);
console.table(carrito);
```

Tal como se puede agregar al final, un elemento se puede agregar al principio del arreglo utilizando el método _unshift()_.

```js
const carrito = []; // Se inicializa vacío debido a que aún no se realizan compras
console.log(carrito);

// Definir producto y agregarlo al principio con .push()
const producto2 = {
    nombre: "Celular",
    precio: 800
}

carrito.push(producto2);
console.table(carrito);

// Agregar un elemento al principio del arreglo con .unshift()
const producto3 = {
    nombre:"Teclado",
    precio: 50
}

carrito.unshift(producto3);
console.table(carrito);
```

#### Crear nuevo arreglo con el spread operator

En las nuevas versiones de JS existen diferenes funciones que hacen lo mismo. Se pueden clasificar entre _Declarativa_ e _Imperativa_.

- **Imperativa:** Se trata de la forma en la cual se modifica una variable inicial, se trabaja sobre ella. Los métodos _Imperativos_ son muy claros, o sea, sólo con leerlos se entiende que es lo que hacen.

- **Declarativa:** Es una paradijma que expresa la logica, sin describir tanto el flujo de control. No modifica una variable inicial, crea una nueva.

En este caso, el modo de agregar elementos utilizando el _Spread Operator_ es de forma **declarativa**.

```js
const carrito = []; // Se inicializa vacío debido a que aún no se realizan compras

// Definir producto
const producto = {
    nombre: "Monitor 32 pulgadas",
    precio: 400
}


const producto2 = {
    nombre: "Celular",
    precio: 800
}


// Agregar un elemento al principio del arreglo con .unshift()
const producto3 = {
    nombre:"Teclado",
    precio: 50
}

let resultado;

resultado = [...carrito,producto]; // Toma una copia del contenido de carrito y le añade el contenido de producto
resultado = [...resultado, producto2]; // Toma una copia de resultado y le añade producto2

/*El orden en el que se añaden los elementos depende de como se declare*/
resultado = [producto3, ...resultado]; // Añade producto3 antes que la copia de resultado

console.table(resultado);
console.log(carrito); // El contenido de carrito sigue siendo el mismo que al inicio
```

#### Elimianr elementos con Splice

Es la forma _Imperativa_ de eliminar elementos de un arreglo. Se hace utlizando el método _.pop()_ en el arreglo al cual se le quiere eliminar un elemento. El método _.pop()_ elimina el úlitmo elemeto del arreglo.

```js
const carrito = []; // Se inicializa vacío debido a que aún no se realizan compras
console.log(carrito);

// Definir producto
const producto = {
    nombre: "Monitor 32 pulgadas",
    precio: 400
}

// Se agrega un producto al final del arreglo carrito
carrito.push(producto);
console.table(carrito);

const producto2 = {
    nombre: "Celular",
    precio: 800
}

carrito.push(producto2);
console.table(carrito);

const producto3 = {
    nombre:"Teclado",
    precio: 50
}

carrito.push(producto3);
console.table(carrito);

const producto4 = {
    nombre: "Celular2",
    precio: 800
}

carrito.push(producto4);
console.table(carrito);

// Eliminar ultimo elemento de un arreglo

carrito.pop(); // Elimina el último elemento
console.table(carrito);
```

Para eliminar el primer elemento del arreglo, se debe utilizar el método _.shift()_.

```js
const carrito = []; // Se inicializa vacío debido a que aún no se realizan compras
console.log(carrito);

// Definir producto
const producto = {
    nombre: "Monitor 32 pulgadas",
    precio: 400
}

// Se agrega un producto al final del arreglo carrito
carrito.push(producto);
console.table(carrito);

const producto2 = {
    nombre: "Celular",
    precio: 800
}

carrito.push(producto2);
console.table(carrito);

const producto3 = {
    nombre:"Teclado",
    precio: 50
}

carrito.push(producto3);
console.table(carrito);

const producto4 = {
    nombre: "Celular2",
    precio: 800
}

carrito.push(producto4);
console.table(carrito);

// Eliminar del inicio del arreglo

carrito.shift();
console.table(carrito);
```

Para eliminar un elemento sin importar el lugar del arreglo, se puede utilizar el método _.splice(inicio,cant.eliminar)_, el cual recibe la posición del elemento a eliminar y la cantidad de elementos desde esa posición que se quieren eliminar, por ejemplo, `arreglo.splice(2,1)` elimina un elemento desde el indice 2, o sea, elimina el elemento que se encuentra en el indice 2, en cambio, `arreglo.splice(2,3)`, elimina 3 elementos desde el indice 2, o sea, elimina los elementos de los indices 2,3 y 4.

```js
const carrito = []; // Se inicializa vacío debido a que aún no se realizan compras
console.log(carrito);

// Definir producto
const producto = {
    nombre: "Monitor 32 pulgadas",
    precio: 400
}

// Se agrega un producto al final del arreglo carrito
carrito.push(producto);
console.table(carrito);

const producto2 = {
    nombre: "Celular",
    precio: 800
}

carrito.push(producto2);
console.table(carrito);

const producto3 = {
    nombre:"Teclado",
    precio: 50
}

carrito.push(producto3);
console.table(carrito);

const producto4 = {
    nombre: "Celular2",
    precio: 800
}

carrito.push(producto4);
console.table(carrito);

// Eliminar un elemento en cualquier posición del arreglo
carrito.splice(1,1); // Elimina el elemento que se encuentra en el indice 1
console.table(carrito);

carrito.splice(1,2); // Elimina los elementos que se encuentran en al posición 1 y 2
console.table(carrito);
```

#### Destructuring de Arrays

Sirve para extraer el valor y la variable en un mismo paso. Se puede ocupar de varias formas, alguna de ellas son las siguientes:

- Extraer el primer valor del arreglo.

```js
const numeros = [10,20,30,40,50];

const [indiceCero] = numeros; // Crea una variable con el primer valor del arreglo
console.log(indiceCero);
```

- Extraer el último valor del arreglo

```js
const numeros = [10,20,30,40,50];

const [ , , , ,ultimo] = numeros; // Crea una variable con el úlitmo valor del arreglo
console.log(ultimo);
```

- Extraer más de un valor del arreglo en variables diferentes.

```js
const numeros = [10,20,30,40,50];

const [indiceCero2, indiceUno] = numeros; // Crea 2 variables con el primer y segundo valor respectivamente
console.log(indiceCero2);
console.log(indiceUno);
```

- Extraer un elemento de cualquier posición, en el ejemplo se extrae el valor del indice 2, o sea, el tercer valor del arreglo.

```js
const numeros = [10,20,30,40,50];

const [,,indiceTres] = numeros; // Crea una variable con el tercer valor del arreglo
console.log(indiceTres);
```

- Extraer los valores que uno necesite y guardar el resto en un nuevo arreglo (usando el _Spread Operator_)

```js
const numeros = [10,20,30,40,50];

const [primero, segundo, ...tercero] = numeros; // Crea 2 variables con el primer y segundo valor y un arreglo con el resto de los valores
console.log(primero);
console.log(segundo);
console.table(tercero);
```

#### .forEach para iterar un Arreglo

Es una forma de iterar accediendo directamente sobre los valores del arreglo, sin la necesidad de tener que trabajar con los indices y el nombre del arreglo.

```js
const carrito = [
    { nombre: 'Monitor 27 pulgadas', precio: 500},
    { nombre: 'Televisión', precio: 100},
    { nombre: 'Tablet', precio: 200},
    { nombre: 'Audifonos', precio: 300},
    { nombre: 'Teclado', precio: 400},
    { nombre: 'Celular', precio: 700},
]

/*.forEach() itera sobre cada valor del arreglo, en este caso, cada valor del arreglo es un producto*/
carrito.forEach( function(producto){
    console.log(`${producto.nombre} - Precio: ${producto.precio}`);
} )
```

#### .map para iterar un Arreglo y sus diferencias con .forEach

Hace lo mismo que _.forEach()_ pero **crea un arreglo nuevo**, o sea, que si se utilizará _.forEach()_ dentro de una variable, la variable no guardaría nada.

Un ejemplo de uso donde viene bien la creación de un nuevo arreglo, sería si se necesitará traer todos los productos en base a un precio, ahí la creación de un nuevo arreglo con los elementos que cumplan con el requisito vendría de maravilla.

```js
const carrito = [
    { nombre: 'Monitor 27 pulgadas', precio: 500},
    { nombre: 'Televisión', precio: 100},
    { nombre: 'Tablet', precio: 200},
    { nombre: 'Audifonos', precio: 300},
    { nombre: 'Teclado', precio: 400},
    { nombre: 'Celular', precio: 700},
]

const nuevoArreglo = carrito.map(function(producto){
    return `${producto.nombre} - Precio: ${producto.precio}`;
})

console.log(nuevoArreglo); // Muestra un nuevo arreglo con todos los elementos

const nuevoArreglo2 = carrito.forEach(function(producto){
    return `${producto.nombre} - Precio: ${producto.precio}`;
})

console.log(nuevoArreglo2); // Muestra un undefined
```

### Funciones en JS

#### Crear funciones en JS

Existen dos formas de crear una función, una es de forma _Declarativa_ y la otra de forma _Expresiva_, amabas se mandan a llamar de la misma forma, pero la diferencia es que la segunda se "guarda" en una variable. Cabe mencionar que en cuento a performance, no se observan diferencias entre ambas.

- **Declaración de función (Function Declaration)**

```js
/*
function nombreFuncion(parametro1, parametro2, parametroN){
    // Cuerpo de la función, codigo que se ejecuta
}

nombreFuncion(valor1, valor2, valorn); // Llamado función
*/

function sumar(){
    console.log(2+2);
}

// Llamado de la función
sumar();
```

- **Expresión de función (function Expression)**

```js
/*
Estructura
const nombreFuncion = function(parametro1, parametro2, parametroN){
    // Cuerpo de la función, codigo que se ejecuta
}

Llmado
nombreFuncion(valor1,valor2,valorN);
*/

const sumar2 = function(){
    console.log(3+3);
}

sumar2(); // Llamado función
```

#### Diferencias entre function expression y declaration

Las funciones creadas de forma _Declarativa_ **pueden llamarse antes de crear la función**, o sea, no importa el orden donde se escriba lo que hace la función, puede invocarse antes. Lo anterior es algo que las _Expresiones de Funciones_ no pueden, esto ha de deberse a que tal como las variables, estas no pueden utilizarse antes de declararse.

#### Algunas funciones nativas en JS

JS cuenta con más de 4000 funciones las cuales forman la "librería estandar" (en realidad JS no tiene una librería estandar como otros lenguajes) del lenguaje.

```js
/*Funciones nativas de JS*/

alert('hubo un erro...'); // Despliega una ventana de error

prompt('¿Cual es tu edad?'); // Depsliega una ventana para ingresar datos

console.log( parseInt('20')); // parseInt() es una función que tranfroma un string con formato de entero a entero
```

#### Parametros y Argumentos en Funciones

Los _parametros_, son como variables generales que se utilizan dentro de las funciones y reciben el valor que se pasa como _argumentos_ al momento de ser llamada la función.

```js
function sumar(a, b){
    /*a y b son parametros*/    
    console.log(a+b);
}

sumar(2, 3); // 2 y 3 son argumentos

function saludar(nombre, apellido){
    console.log(`Hola ${nombre} ${apellido}`);
}

saludar('Juan','Pérez');
```

#### Parametros por default

Se utilizan para evitar que cuando se llame la función y no se le entreguen argumentos, no queden los parametros como _undefined_ en la función. Para esto, en la declaración de la función hay que darle el valor por default a los parametros.

```js
function saludar(nombre = 'Desconocido', apellido = ''){
    console.log(`Hola ${nombre} ${apellido}`);
}

saludar(); // En este caso se muestra un Hola Desconocido
saludar('Juan'); // En este caso se muestra un Hola Juan
saludar('Juan','Pérez'); // En este caso se muestra Hola Juan Pérez
```

#### Como se comunican las funciones entre si

Las funciones se pueden ir llamando dentro de otras funciones como se muestra en el siguiente ejemplo.

```js
iniciarApp(); // Función que inicia todo, siempre debe estar

function iniciarApp(){
    console.log('Iniciando App...') // Finalizando esto
    segundaFuncion(); // Se llama a la segunda función
}

function segundaFuncion(){
    console.log('Hola desde la segunda función'); // Cuando se ejecute esto
    usuarioAutenticado('Pablo'); // Se llama la función
}

function usuarioAutenticado(usuario){
    console.log('Autenticando usuario... espere...');
    console.log(`Usuario autenticado exitosamente: ${usuario}`);
}
```

#### Funciones que retornan valores

Hasta ahora se han visto funciones que sólo muestran por consola cosas, sin embargo, no siempre será así, existen funciones que permiten retornar valores los cuales serán asignados a una variables. Para esto, luego de ejecutar el código de la función, dentro del cuerpo de la función, hay que utilizar la palabra `return` seguida de lo que se quiere retornar. Luego se define una variable la cual su valor será igual al llamado de la función que retorna algo, lo que permite que ahora se pueda trabajar con esa variable y su valor que proviene del uso de la función.

```js
/*Ejemplo sencillo*/

function sumar(a,b){
    return a+b; // Retorna la suma de a y b
}

const resultado = sumar(2,3); // Se guarda lo que retorna la función en la variable resultado
console.log(resultado); // Se muestra por consola el contenido de la variable resultado
```

```js
// Ejemplo más avanzado

let total = 0;

// Agrega cierta cantidad a la variable total
function agregarCarrito(precio) {
    return total += precio;
}

// En base a la variable total se le suma un impuesto del 15%
function calcularImpuesto(total){
    return total * 1.15;
}

total = agregarCarrito(100); // Agrega 100 a la variable total
total = agregarCarrito(300); // Agrega 300 a la variable total
total = agregarCarrito(500); // Agrega 500 a la variable total
total = agregarCarrito(200); // Agrega 200 a la variable total

totalPagar = calcularImpuesto(total); // Agrega el 15% al total
console.log(`Total a pagar es de ${totalPagar}`); // Muestra en consola el total a pagar
console.log(total); // Muestra en consola el total sin impuesto
```

#### Añadir funciones en un Objeto

Estos son los _métodos de propiedad_, son funciones con sintaxis similar a las de un método. Una de las ventajas que tiene la creación de _métodos de propiedad_ es que al estar dentro de un objeto, en la consola se puede llamar el objeto y eso entregará el listado con todas las funciones que se encuentren contenidas en aquel objeto.

Para crear los _métodos de propiedad_, hay que hacer lo mismo que se hacía cuando se creaban propiedades, pero está vez el valor que contendrá es una función.

```js
const reproductor = {
    reproducir: function(id = 'Desconocido'){
        console.log(`Reproduciendo canción con el id ${id}`);
    },
    pausar: function(){
        console.log('Reproducción pausada');
    },
    borrar: function(id = 'Desconocido'){
        console.log(`Borrando canción con el id ${id}`);
    },
    crearPlaylist: function(nombrePlaylist){
        console.log(`Playlist ${nombrePlaylist} creada`);
    },
    reproducirPlaylist: function(nombrePlaylist){
        console.log(`Reproduciendo Playlist ${nombrePlaylist}`);
    }
}

reproductor.reproducir(20);
reproductor.pausar();
reproductor.borrar(20);
reproductor.crearPlaylist('Random');
reproductor.reproducirPlaylist('Random');
```

Para finalizar, hay que mencionar la creación de funciones set y get, las cuales permiten establecer un valor y obtener un valor de un obejto respectivamente. En el siguiente código se encuentra el objeto reproductor con sus funciones set y get para una canción, además de sus respectivas llamadas en el código.

```js
const reproductor = {
    reproducir: function(id = 'Desconocido'){
        console.log(`Reproduciendo canción con el id ${id}`);
    },
    pausar: function(){
        console.log('Reproducción pausada');
    },
    borrar: function(id = 'Desconocido'){
        console.log(`Borrando canción con el id ${id}`);
    },
    crearPlaylist: function(nombrePlaylist){
        console.log(`Playlist ${nombrePlaylist} creada`);
    },
    reproducirPlaylist: function(nombrePlaylist){
        console.log(`Reproduciendo Playlist ${nombrePlaylist}`);
    },

        /*Tanto set como get luego se utilizan como si se estuvieran manejando propiedades del objeto*/
    set nuevaCancion(cancion){
        this.cancion = cancion;
        console.log(`Añadiendo ${cancion}`);
    },

    get obtenerCancion(){
        console.log(`${this.cancion}`);
    }
}

reproductor.reproducir(20);
reproductor.pausar();
reproductor.borrar(20);
reproductor.crearPlaylist('Random');
reproductor.reproducirPlaylist('Random');

reproductor.nuevaCancion = 'Low'; // Utilización del set
reproductor.obtenerCancion; // Llamado del get
```

#### Arrow Functions

Es una sintaxis mucho más corta para crear funciones. En esta se utiliza _Function Expresion_, en comparación a la declaración normal de funciones, se cambia la palabra _function_ por una flecha `=>` al lado derecho de los parentesis y si la función tiene una sóla línea, no es necesario utilizar las _llaves_ de la función y el `return` es implicito, por lo cual no hay que escribirlo. En el siguiente ejemplo se muestra una función declarada de forma normal y su versión en _arrow function_.

```js
// Function Expression normal
const aprendiendo = function(){
    return 'Aprendiendo JavaScript';
}
console.log(aprendiendo());

// Arrow Function
const aprendiendo2 = () => 'Aprendiendo JavaScript';
console.log(aprendiendo2());
```

#### Parametros en Arrow Function

Al igual que en las funciones delcaradas de forma normal, en los parentesis es donde se declaran los parametros de la función pero en _Arrow Functions_ si se utilizará un sólo parametro, los parentesis pasan a ser opcionales.

```js
// Ejemplo de un parámetro
const aprendiendo = function(tecnologia = 'Algo'){
    return `Aprendiendo ${tecnologia}`;
}
console.log(aprendiendo('JavaScript'));

const aprendiendo2 = tecnologia => `Aprendiendo ${tecnologia}`; // Sin los paréntesis no se puede utilizar un parámetro por default
console.log(aprendiendo2('Javascript'));
```

Hay que recalcar que lo anterior es sólo en el caso de utilizar un sólo parámatro, cuando exista más de uno o se quiera utilizar los _parámetros por default_, hay que utilizar parentesis.

```js
// Ejemplo con dos parámetros
const aprendiendo3 = function(tecnologia, tecnologia2){
    return `Aprendiendo ${tecnologia} y ${tecnologia2}`;
}
console.log(aprendiendo3('JavaScript','Node.js'));

const aprendiendo4 = (tecnologia, tecnologia2) => `Aprendiendo ${tecnologia} y ${tecnologia2}`;
console.log(aprendiendo4('Javascript','Node.js'));
```

#### Arrow Function en .forEach y .map

Las _Arrow Function_ son muy bien utilizadas en los métodos `Arreglo.forEach()` y `Arreglo.map()`. Los siguiente bloques de código muestran la sintaxis sin y con _Arrow Function_.

```js
/*Ejemplo sin Arrow Function*/
const carrito = [
    { nombre: 'Monitor 27 pulgadas', precio: 500},
    { nombre: 'Televisión', precio: 100},
    { nombre: 'Tablet', precio: 200},
    { nombre: 'Audifonos', precio: 300},
    { nombre: 'Teclado', precio: 400},
    { nombre: 'Celular', precio: 700},
]

const nuevoArreglo = carrito.map(function(producto){
    return `${producto.nombre} - Precio: ${producto.precio}`;
})
console.log(nuevoArreglo); // Muestra un nuevo arreglo con todos los elementos

carrito.forEach(function(producto){
    console.log(`${producto.nombre} - Precio: ${producto.precio}`);
})
```

```js
/*Ejemplo con Arrow Function*/
const carrito = [
    { nombre: 'Monitor 27 pulgadas', precio: 500},
    { nombre: 'Televisión', precio: 100},
    { nombre: 'Tablet', precio: 200},
    { nombre: 'Audifonos', precio: 300},
    { nombre: 'Teclado', precio: 400},
    { nombre: 'Celular', precio: 700},
]

const nuevoArreglo = carrito.map((producto) => `${producto.nombre} - Precio: ${producto.precio}`);
console.log(nuevoArreglo); // Muestra un nuevo arreglo con todos los elementos

carrito.forEach((producto) => console.log(`${producto.nombre} - Precio: ${producto.precio}`));
```

#### Arrow Functions en métodos de propiedad

Las _Arrow Functions_ también son una buena opción cuando se escriben _métodos de propiedad_, ya que, permiten la reducción de línea de código en comparación a la declaración normal de funciones.

```js
/*Ejemplo sin Arrow Function*/
const reproductor = {
    reproducir: function(id = 'Desconocido'){
        console.log(`Reproduciendo canción con el id ${id}`);
    },
    pausar: function(){
        console.log('Reproducción pausada');
    },
    borrar: function(id = 'Desconocido'){
        console.log(`Borrando canción con el id ${id}`);
    },
    crearPlaylist: function(nombrePlaylist){
        console.log(`Playlist ${nombrePlaylist} creada`);
    },
    reproducirPlaylist: function(nombrePlaylist){
        console.log(`Reproduciendo Playlist ${nombrePlaylist}`);
    }
}

reproductor.reproducir(20);
reproductor.pausar();
reproductor.borrar(20);
reproductor.crearPlaylist('Random');
reproductor.reproducirPlaylist('Random');
```

```js
/*Ejemplo con Arrow Function*/
const reproductor = {
    reproducir: (id = 'Desconocido') => console.log(`Reproduciendo canción con el id ${id}`),
    pausar: () => console.log('Reproducción pausada'),
    borrar: (id = 'Desconocido') => console.log(`Borrando canción con el id ${id}`),
    crearPlaylist: (nombrePlaylist) => console.log(`Playlist ${nombrePlaylist} creada`),
    reproducirPlaylist: (nombrePlaylist) => console.log(`Reproduciendo Playlist ${nombrePlaylist}`)
}

reproductor.reproducir(20);
reproductor.pausar();
reproductor.borrar(20);
reproductor.crearPlaylist('Random');
reproductor.reproducirPlaylist('Random');
```

### Estructuras de control

#### Creando un if

Permite comprobar condiciones y en base a eso ejecutar cierto código. Especificamente el condicional _if_ hace referencia a que **si se cumple una condición** se haga algo.

```js
const puntaje = 1000;

if(puntaje === 1000){
    console.log('si es igual...')
}
```

#### Comparador estricto

El comparador estricto es utilizar tres iguales seguidos `===`, a diferencia del comprador normal `==`, el estricto compara el contenido y el tipo de los elementos a comparar. Por ejemplo, el comparador normal dice que el número 1000 y el string '1000' son iguales, esto se debe a que ambos parecen ser iguales pero su tipo es distinto. Por otro lado, el comparador estricto al compararlos entrega un false, porque efectivamente no son iguales.

```js
/*Ejemplo comparador normal*/
const puntaje = 1000;

if(puntaje == '1000'){
    console.log('si es igual...') // Muestra esto por consola
} else {
    console.log('no es igual...');
}
```

```js
/*Ejemplo comparador estricto*/
const puntaje = 1000;

if(puntaje === '1000'){
    console.log('si es igual...') 
    } else {
    console.log('no es igual...'); // Muestra esto por consola
}
```

En el caso de la diferencia, también existe un operador estricto para esto, el normal es `!=` y el estricto es `!==`, ambos se comportan de la misma manera que los de igualdad.

#### Comparador Mayor que y Menor que

Para saber si algo es mayor o menor que algo se deben utilizar los siguiente comparadores `>` y `<` respectivamente. De igual forma si la condición implica ver si algo es mayor o igual, o menos o igual, se deben utilizar los siguientes operadores `<=` y `<=`.

#### else-if

Sirve para evaluar una condición intermedia entre el if y else. Para utilizarlo, sólo hay que agregar un if luego del else separado por un espacio.

```js
const dinero = 500;
const totalPagar = 300;
const tarjeta = true;

if(dinero>=totalPagar){
    console.log('Se puede pagar');
/*No se hace una comparación de tarjeta === true porque tarjeta es booleano y el if sólo necesita un true o un false*/
} else if(tarjeta){
    console.log('Se puede pagar con la tarjeta')
} else{
    console.log('Fondos Insuficientes');
}
```

Cabe mencionar que se pueden utilizar cuantos else-if uno quiera, teniendo siempre en cuenta no perder la trazabilidad del código.

#### Switch para evaluar multiples condiciones

Es una estructura similar a lo que sería muchos if,else-if y else juntos pero de una manera más sencilla de leer y entender. Basciamente, dependiendo del valor que tenga una variable, se ejecuta cierto código.

```js
// Switch case
// Dependiendo de el valor de metodoPago, se ejecuta algo
const metodoPago = 'efectivo';

/*En el parentesis va lo que se quiere comparar*/
switch(metodoPago){
    /*case son como los if*/
    case 'efectivo':
        console.log(`Pagaste con ${metodoPago}`);
        break;
    case 'cheque':
        console.log(`Pagaste con ${metodoPago}`);
        break;
    case 'tarjeta':
        console.log(`Pagaste con ${metodoPago}`);
        break;
    /*default es similar a un else*/
    default:
        console.log('Aún no has seleccionado un método de pago o método de pago no soportado');
        break;
}
```

Que no se olvide que no es necesario mostras algo por consola, se puede reemplazar por la cantidad de código que uno necesite y por otras cosas como funciones por ejemplo.

#### Operador &&

Este operador se utiliza para comprobar más de una condición en el mismo if. Amabas condiciones deben cumplirse para que se ejecute el código asociado a la condición.

```js
const usuario = false;
const puedePagar = true;

if(usuario && puedePagar){
    console.log('Si puedes comprar');
} else if(!usuario && !puedePagar){
    console.log('No puedes comprar');
} else if(!usuario){
    console.log('Debes registrarte');
} else{
    console.log('Saldo insuficiente');
}
```

#### Operador ||

Este operador se utiliza para saber si una de dos o más condiciones en un mismo if se cumplen. A diferencia del operador &&, el operador || sólo necesita que una condición se cumpla para ejecutar el código asociado.

```js
const efectivo = 300;
const credito = 400;
const disponible = efectivo + credito;
const totalPagar = 600;

if(efectivo>=totalPagar || credito>=totalPagar || disponible>=totalPagar){
    console.log('Se puede pagar')
} else{
    console.log('Fondos insuficientes');
}
```

#### Detener la ejecución de un if con una función

Se puede crear una función que compruebe algo y que en ella sólo hayan if, para evitar que se comprueben más de uno luego de que se haya encontrado una coincidencia, hay que colocar un return luego del código a ejecutar dentro del if.

```js
const puntaje = 500;

// Función que según el puntaje entrega un mensaje
function revisarPuntaje(puntaje = 300){
    if(puntaje = 500){
        console.log('Excelente puntaje, felicitaciones');
        return;
    }

    if(puntaje = 300){
        console.log('Buen puntaje');
        return;
    }
}

revisarPuntaje(puntaje); // Llamado de la función
```

#### Operador ternario

Al igual que las _Arrow Functions_, el _operador ternario_ reduce la cantidad de código, este caso, la cantidad de código de una estructura if else. La reducción se produce porque se eliminan las palabras reservadas _if_ y _else_, al igual que las llaves.

```js
const autenticado = true;

// Sin operador ternario
if(autenticado){
    console.log('Si está autenticado');
} else{
    console.log('No está autenticado');
}

// Con operador ternario
/*Si se cumple la condición antes del ? se ejecuta lo primero antes del : de lo contrario se ejecuta lo otro*/
console.log(autenticado ? 'Si está autenticado':'No está autenticado');
```

Al igual que con la estructura normal, aquí se pueden comprar más de una condición añadiendo los operadores && y ||, además se pueden anidad operadores ternarios como si se estuvieran anidando if pero eso es poco común y no se suele utilizar.

### Iteradores en JS

El código se ejecuta hasta que una condición se cumpla o se deje de cumplir.

#### For Loop

Se ejecuta hasta que una condición se deja de cumplir. Se compone de la palabra reservada _for_, un parentesis que contiene al iterador, la condición de finalización y el incremento, separados por punto y coma, y las llaves en donde irá el bloque de código que se quiere repetir.

```js
/*Ejemplo for loop*/
for(let i=0; i<=10; i++){
    console.log(`Número ${i}`)
}
```

```js
/*Ejemplo de prueba téecnica*/
for(let i=1; i<=20; i++){
    console.log( i%2 ? `El numero ${i} es PAR` : `El numero ${i} es IMPAR`);
}
```

#### break y continue en un for loop

_break_ rompe la ejecución del loop, mientras que _continue_ permite interceptar un elemento, identificarlo y continuar con la ejecución.

```js
/*Ejemplo break*/

for(let i = 0; i<= 10; i++){
    if(i===5){
        console.log('Este es el 5');
        break; // Al encontrar la coincidencia, deja de ejecutarse el loop
    }
    console.log(`Numero: ${i}`);
}
```

```js
/*Ejemplo continue*/

for(let i = 0; i<= 10; i++){
    if(i===5){
        console.log('Este es el 5');
        continue; // Luego de encontrar la coincidencia, continua con la siguiente iteración
    }
    console.log(`Numero: ${i}`);
}
```

#### While loop

Se ejecuta mientras una condición sea verdadera. Lo que se puede hacer con un for, también se puede hacer con un while. La estructura del while se puede observar en el siguiente ejemplo.

```js
let i = 0; // Inicializador

// Entre parentesis se encuentra la condición de iteración
while(i<10){
    console.log(`Numero ${i}`); // Bloque de código
    i++; // Incremento
}
```

#### Do While Loop

Es una variación del While en la cual el código se ejecuta al menos una vez antes de verificar la condición.

```js
let i = 0;

do {
    console.log(`Numero ${i}`); // Bloque de código a ejecutar
    i++; // Incremento
} while (i<10); // Condición
```

#### .forEach y .map

##### .forEach

Es ideal para rcorrer arregles, se ejcuta al menos una vez por cada vez que hayan elementos en el arreglo, o sea, se ejecuta tanta veces como elementos hayan en el arreglo.
Itera sobre los elementos del arreglo, por lo cual el iterador obtiene el elemeto del arreglo, a diferencia del for normal que itera en base al indice.

```js
const pendientes = ['Tarea','Comer','Proyecto','Estudiar JS'];

pendientes.forEach(
    /*forEach itera sobre los elementos, por eso es que iterador equivale al elemento del arreglo.
    De todas formas permite obtener el indice en el arreglo, agregando otro elemento separado por
    una coma al lado derecho del iterador*/
    (iterador, indice) => {
        console.log(`Elemento ${iterador} en el indice ${indice}`);
    }
)
```

##### .map

Su estructura es igual a la del _.forEach()_ y hace lo mismo pero a diferencia del _.forEach()_, _.map()_ crea un nuevo elemento con el resultado de haber recorrido el arreglo.

```js
// map

const baratos = carrito.map(producto => producto)
console.log(baratos);
```

**Nota:** Recordar siempre retornar los elementos de vuelta para que no sean reemplazados por un _undefined_.

```js
let arreglo = [{id: 0, cantidad: 1}, {id: 1, cantidad: 1}, {id: 2, cantidad: 1}, {id: 3, cantidad: 1}];
console.log(arreglo);

// El siguiente código devuelve un arreglo donde todos los elementos son undefined
// const arregloNuevo = arreglo.map( elemento => {
//     if(elemento.id === 2){
//         elemento.cantidad +=1; // Esta asginacion afecta al valor del antiguo arreglo
//     }
//     //El return elemento, debería estar aquí
// });

// El siguiente código devuelve un arreglo donde todos los elementos menos uno son udefined
// const arregloNuevo = arreglo.map( elemento => {
//     if(elemento.id === 2){
//         elemento.cantidad +=1; // Esta asginacion afecta al valor del antiguo arreglo
//         return elemento;
//     }
//     //El return elemento, debería estar aquí
// });

// Busca el elemento con el id igual a 2 y retorna un arreglo nuevo
const arregloNuevo = arreglo.map( elemento => {
    if(elemento.id === 2){
        elemento.cantidad +=1; // Esta asginacion afecta al valor del antiguo arreglo
    }
    return elemento;
});

// El contenido del nuevo arreglo es asignado al antiguo arreglo
arreglo = [...arreloNuevo];
console.log(arreglo);
```

#### for ...of

Itera sobre el arreglo original y el iterador toma el valor de cada elemento del arreglo. Su estructura se basa en la del _for_ pero la condición y el incremento se reemplazan por un `of nombre.arreglo` quedando la declaración de la siguiente manera `for (iterador of nombreArreglo){}`.

```js
const carrito = [
    { nombre: 'Monitor 27 pulgadas', precio: 500},
    { nombre: 'Televisión', precio: 100},
    { nombre: 'Tablet', precio: 200},
    { nombre: 'Audifonos', precio: 300},
    { nombre: 'Teclado', precio: 400},
    { nombre: 'Celular', precio: 700},
]

for( pendientes of carrito){
    console.log(pendientes);
}
```

Cabe mencionar que desde ECMAScript 7, se puede iterar sobre un objeto utilizando _for of_ y `Object.entries(objetoAIterar)`. Para hacerlo, hay que definir dos iteradores, el primero que entregará el nombre de la propiedad y el segundo que entregará los valores `let[llave,valor]`.

```js
const automovil = {
    modelo: 'Camaro',
    year: 1969,
    motor: '6.0'
}

//ECMAScript 7 introdujeron el siguiente iterador para objetos
for( let [llave,valor] of Object.entries(automovil)){
    console.log(llave); // Muestra la propiedad
    console.log(valor); // Muestra el valor de la propiedad
}
```

#### for ...in

Esta variación del _for_ está hecha para iterar sobre **objetos**, itera sobre arreglos pero entrega el indice, en cambio, en los objetos entrega las propiedades de este. Su estructura es como la de _for...of_ pero se cambia el _of_ por un _in_ quedando de la siguiente forma `for (iterador in Objeto){}`. El iterador definido mostrará el nombre de las propiedades, para mostrar el valor de las propiedades hay que escribir el nombre del objeto seguido de una par de corechetes y dentro escribie el nombre del iterador `Objeto[iterador]`.

```js
const pendientes = ['Tarea', 'Comer', 'Proyecto', 'Estudiar JS']; // Arreglo

for( let pendiente in pendientes){
    console.log(pendiente); //Muestra los indices de cada elemento 
}

// Objeto
const automovil = {
    modelo: 'Camaro',
    year: 1969,
    motor: '6.0'
}

//for in para objeto
for( let propiedad in automovil){
    console.log(propiedad); // Muestra la llave del objeto
    console.log(automovil[propiedad]); // Muestra el valor de la propiedad
}
```

### Array Methods

#### .includes y .some

Ambos métodos sirven para encontrar una valor en un arreglo. Sin embargo, _.includes()_ sirve sólo para arreglos de indices, en cambio, _.some()_ es tanto para arreglos de indices como para arreglos de objetos. Por otro lado, ambos métodos se diferencian con respecto al parámetro que reciben, por un lado _.includes()_ recibe el valor que se está buscando en el arreglo, mientras que _.some()_ recibe una _Arrow Function_ la cual se encarga de recorrer el arreglo (de indice u objetos) y buscar un valor, la estructura de la _Arrow Function_ es similar a la de un _.forEach_ o un _.map_, en donde el cuerpo de la función se compone de un _return_ seguido por lo que se está buscando.

```js
// Ejemplo .includes()
const meses = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio', 'Julio']; // Arreglo con indices

// Comprobar si un valor existe de forma manual en un arreglo

meses.forEach( (mes) => {
    if(mes === 'Enero'){
        console.log('Enero existe');
    }
});

// Comprobar si un valor existe en un arreglo de indices con .includes

/*.includes entrega un true en la primera coincidencia que 
encuentra en el arreglo. Es sólo para arreglos con indices*/
const resultado = meses.includes('Enero');
console.log(resultado);
```
Cabe mencionar que tanto _.includes()_ como _.some()_ hay que utilizarlos de forma _Expresiva_, o sea, hay que utilzarlas dentro de una variable la cual contendrá el resultado booleano de si se encontró coincidencia o no.

```js
// Ejemplo .some()

const meses = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio', 'Julio']; // Arreglo con indices

// Arreglo con Objetos
const carrito = [
    { nombre: 'Monitor 27 Pulgadas', precio: 500 },
    { nombre: 'Televisión', precio: 100 },
    { nombre: 'Tablet', precio: 200 },
    { nombre: 'Audifonos', precio: 300 },
    { nombre: 'Teclado', precio: 400 },
    { nombre: 'Celular', precio: 700 },
]

// Comprobar si un valor existe en un arreglo de objetos con .some
/*.some similar a un forEach ocupa un arrow function compuesto por 
el iterador*/

const existe = carrito.some( producto => {
    return producto.nombre === 'Teclado' // Se encarga de encontrar la coincidencia y retornar el booleano correspondiente
});
console.log(existe);

// Comprobación en un arreglo tradicional con .some y arrow function full

const existe2 = meses.some( mes => mes === 'Marzo');
console.log(existe2);
```

#### .findIndex para encontrar la posición en un array

Este método sirve para encontrar el índice de un elemento. Entrega el índice de la primera coincidencia que encuentra. Sirve tanto para arreglos con indices como  con objetos, añadiendo la sintaxis de punto al momento de hacer la compración. Cabe mencionar que si no se encuentra el elemento indicado, este método retorna un _-1_.

```js
const meses = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio', 'Julio']; // Arreglo con indices

// Arreglo con Objetos
const carrito = [
    { nombre: 'Monitor 27 Pulgadas', precio: 500 },
    { nombre: 'Televisión', precio: 100 },
    { nombre: 'Tablet', precio: 200 },
    { nombre: 'Audifonos', precio: 300 },
    { nombre: 'Teclado', precio: 400 },
    { nombre: 'Celular', precio: 700 },
]

// Encontrar indice de un elemento de forma manual

meses.forEach( (mes, indice) => {
    if(mes === 'Marzo'){
        console.log(`El indice del mes ${mes} es ${indice}`);
    }
})

// Encontrar indice de un elemento con .findIndex

const indiceAbril = meses.findIndex( mes => mes === 'Abril');
console.log(indiceAbril); // Si no encuentra el elemento, da retorna un -1

const indiceTablet = carrito.findIndex( producto => producto.nombre === 'Tablet');
console.log(indiceTablet);
```

#### .reduce

Es una función reducer, o sea, una función reductora la cual toma una gran cantidad de datos, los cuales une y entrega una gran cantdiad de resultados.

El método .reduce() utiliza una arrow function el cual recibe dos valores, el valor previo y el actual, en el ejemplo, el valor previo sería
el total al cual se le sumará el valor actual, o sea, producto.precio, durante la iteración .reduce() hará como si se hiciera un +=
por lo cual en el cuerpo de la función hay que poner sólo un +.


```js
// Arreglo con Objetos
const carrito = [
    { nombre: 'Monitor 27 Pulgadas', precio: 500 },
    { nombre: 'Televisión', precio: 100 },
    { nombre: 'Tablet', precio: 200 },
    { nombre: 'Audifonos', precio: 300 },
    { nombre: 'Teclado', precio: 400 },
    { nombre: 'Celular', precio: 700 },
]

// Con un forEach

let total = 0;
carrito.forEach( producto => total += producto.precio); // Suma todos los precios de los productos dentro del carrito
console.log(total);

// Con un  .reduce
let resultado = carrito.reduce( (total2, producto) => total2 + producto.precio, 0 ); // El 0 es el valor con el que inicia total2
console.log(resultado);
```

Cabe mencionar que al utilizar .reduce no es necesario crear una variable fuera de la arrow function, ya que dentro de ella es donde se define e inicializa.

#### .filter

Crea un nuevo arreglo basado en el parametro que es evaluado, osea, crea un nuevo arreglo en base a una condición que uno entregue. Al igual que los otros métodos, _.filter_ utiliza un _arrow function_ que itera sobre el arreglo, y en su return, se pone la condición.

Se puede utilizar para filtrar elementos.

```js
// Arreglo con Objetos
const carrito = [
    { nombre: 'Monitor 27 Pulgadas', precio: 500 },
    { nombre: 'Televisión', precio: 100 },
    { nombre: 'Tablet', precio: 200 },
    { nombre: 'Audifonos', precio: 300 },
    { nombre: 'Teclado', precio: 400 },
    { nombre: 'Celular', precio: 700 },
]

let resultado = carrito.filter( producto => producto.precio >= 400); // Crea un arreglo con los productos con precios mayores o iguales a 400
console.table(resultado);
```

Al igual que se puede utilizar para quitar elementos

```js
// Arreglo con Objetos
const carrito = [
    { nombre: 'Monitor 27 Pulgadas', precio: 500 },
    { nombre: 'Televisión', precio: 100 },
    { nombre: 'Tablet', precio: 200 },
    { nombre: 'Audifonos', precio: 300 },
    { nombre: 'Teclado', precio: 400 },
    { nombre: 'Celular', precio: 700 },
]

// filter se puede utilizar para quitar un elemento de un arreglo
let resultado3 = carrito.filter( producto => producto.nombre != 'Tablet'); // Trae todos los productos menos la Tablet
console.table(resultado3);
```

#### .find

Crea un nuevo arreglo en base a la condición que uno está entregando en el _arrow function_. Devuelve el primer elemento que cumpla con la condición, si no encuentra coincidencia, devuelve un undefined.

```js
// Arreglo con Objetos
const carrito = [
    { nombre: 'Monitor 27 Pulgadas', precio: 500 },
    { nombre: 'Televisión', precio: 100 },
    { nombre: 'Tablet', precio: 200 },
    { nombre: 'Audifonos', precio: 300 },
    { nombre: 'Teclado', precio: 400 },
    { nombre: 'Celular', precio: 700 },
]

// con un forEach
let resultado = '';
carrito.forEach( (producto, index) => {
    if(producto.nombre == 'Tablet'){
        resultado = carrito[index];
    }
} );
console.log(resultado);

// CON EL MÉTODO .find
const resultado2 = carrito.find( producto => producto.nombre === 'Tablet');
console.log(resultado2);
```

#### .every

Es un método que sirve para comprobar que todos los elementos de una arreglo cumplen con una misma condición, retorna un booleano y sólo retorna un true si todos los elementos del arreglo cumplen con cierta condición. Si se quiere comprobar que al menos un elemento del arreglo cumpla con la condición, existe el método _.some()_ que se vió anteriormente.

```js
// Arreglo con Objetos
const carrito = [
    { nombre: 'Monitor 27 Pulgadas', precio: 500 },
    { nombre: 'Televisión', precio: 100 },
    { nombre: 'Tablet', precio: 200 },
    { nombre: 'Audifonos', precio: 300 },
    { nombre: 'Teclado', precio: 400 },
    { nombre: 'Celular', precio: 700 },
]

const resultado = carrito.every( producto => producto.precio < 1000);
console.log(resultado); //true, todos los elementos cumplen con la condición

const resultado2 = carrito.every( producto => producto.precio < 500);
console.log(resultado2); //false, no todos los elementos cumplen con la condición

const resultado3 = carrito.some( producto => producto.precio < 500);
console.log(resultado3); //true, al menos un elemento cumple con la condición
```

#### Unir arrglos con .concat o Spread Operator

##### .concat

Es un método que sirve para unir dos o más arreglos. Se utiliza en el arreglo al que se le quiere unir elementos. A diferencia de los otros métodos, _.concat()_ no utiliza _aroow function_. Además de arreglos, puede recibir otro tipo de variables, como lo serían enteros y strings. Hay que tener en cuenta que dependiendo de el orden con el que se pasen los elementos al método, es el orden con el que se encontrarán en el nuevo arreglo.

```js
const meses = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio']; // Arreglo con indices
const meses2 = ['Julio','Agosto','Septiembre','Octubre','Noviembre','Diciembre'];
const mesesUpper1 = ['ENERO', 'FEBRERO'];
const mesesUpper2 = ['MARZO', 'ABRIL'];
const numero = 10;
const palabra = 'String';

// con .concat()
const anio = meses.concat(meses2); // Es recomendable guardar en una nueva variable el resultado de .concat()
console.table(anio);
console.table(meses); // .concat no afecta a ninguno de los arreglos
console.table(meses2); // .concat no afecta a ninguno de los arreglos

const anio2 = anio.concat(mesesUpper1, mesesUpper2); // .concat() puede recibir más de un arreglo
console.table(anio2);

// Se pueden concatenar otros tipos de variables, como lo serían números y palabras
const arreglo1 = mesesUpper1.concat(mesesUpper2, numero, palabra);
console.table(arreglo1);
```

##### Con Spread Operator

Además de arreglos, puede unir otro tipo de variables, como lo serían enteros y strings. Hay que tener en cuenta que dependiendo de el orden con el que se pasen los elementos al método, es el orden con el que se encontrarán en el nuevo arreglo, además en el caso de los _Strings_ hay que tener cuidado con no anteponer _..._ antes del nombre de la variable, ya que el _spread operator_ lo que hará será añadir cada uno de los caracteres de la palabra por separado al arreglo.

```js
const meses = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio']; // Arreglo con indices
const meses2 = ['Julio','Agosto','Septiembre','Octubre','Noviembre','Diciembre'];
const mesesUpper1 = ['ENERO', 'FEBRERO'];
const mesesUpper2 = ['MARZO', 'ABRIL'];
const numero = 10;
const palabra = 'String';

// con Spread operator
const nuevoAnio = [...meses,...meses2]; // Se toma una copia de cada arreglo indicado y se crea un nuevo arreglo que los tenga a ambos concatenados
console.table(nuevoAnio);

/* Al igual que con .concat(), se pueden concatenar otros elementos no arreglos con el spread operator pero hay que tener cuidado con no anteponer los ...
de lo contrario, en el caso de un string, añadirá cada carácter que componga a la palabra*/
const arreglo2 = [...mesesUpper1, ...mesesUpper2, numero, palabra];
console.table(arreglo2);

const arreglo3 = [...mesesUpper1, ...mesesUpper2, numero, ...palabra]; // Los números no pueden separarse con el spread operator, a diferencia de las palabras que se separan en caracteres
console.table(arreglo3);
```

#### Spread Operator

Entre uno de los beneficios que tiene el uso del _spread operator_, se encuentra el no modificar la variable original, ya que crea una copia la cual se termina alamcenando en una nueva variable.

```js
// Rest o Spread Operator

const meses = ['Enero', 'Febrero', 'Marzo', 'Abril', 'Mayo', 'Junio', 'Julio']; // Arreglo con indices

// Arreglo con Objetos
const carrito = [
    { nombre: 'Monitor 27 Pulgadas', precio: 500 },
    { nombre: 'Televisión', precio: 100 },
    { nombre: 'Tablet', precio: 200 },
    { nombre: 'Audifonos', precio: 300 },
    { nombre: 'Teclado', precio: 400 },
    { nombre: 'Celular', precio: 700 },
]

// Agregar un elemento al final de un arreglo con indices
meses2 = [...meses, 'Agosto'];
console.log(meses2);

// Agregar un elemento al final de un arreglo de objetos
const producto = {nombre: 'Disco Duro', precio: 300};
const carrito2 = [...carrito, producto];
console.table(carrito2);
```

### El Objeto Date()

Es el objeto en el cual residen las fechas, las cuales al pertenecer a Date(), su tipo es de objeto. **Se recomienda que si se necesita validar una fecha, se haga con la hora del servidor en donde se encuentré el sitio y no con JavaScript.**

- **Inicializar una variable de tipo Date():** Para hacar que una variable sea una fecha, hay que crear un nuevo obejto Date(), el cual si se crea sin valor alguno, alamacena la fecha y la hora en la cual se instanció la variable.

```js
const diaHoy = new Date(); // Inicializar una variable de tipo Date()
console.log(diaHoy); // Muestra lo que tiene diaHoy
```

En el caso de que se le quiera dar un valor, se puede incluir alguna fecha dentro de los parentesis del constructor del objeto, como muestra el siguiente ejemplo.

```js
const algunDia = new Date('1-5-2000'); // otra opción de valor es ¿January 5 2000'
console.log(algunDia); // Muestra información acorde a la fecha indicada
```

- **Obtener una parte de la fecha:** Desde una fecha, se pueden obtener distintos valores, como lo serían el año, día, mes u hora de la fecha en cuestión.

```js
const diaHoy = new Date(); // Inicializar una variable de tipo Date()
let valor; // Variable auxiliar

// Hay que ir comentando y descomentando las líneas de código para ejecutarlas
// valor = diaHoy.getFullYear(); // Se obtiene el año de la fecha
// valor = diaHoy.getMonth(); // Se obtiene el mes de la fecha (Enero es 0, Febrero es 1, Marzo es 2, etc)
// valor = diaHoy.getMinutes(); // Se obtiene los minutos de la fecha
// valor = diaHoy.getHours(); // Se obtiene la hora de la fecha
valor = diaHoy.getTime(); // Se obtiene el tiempo que ha transcurrido desde el primero de enero de 1970 hasta la fecha en milisegundos

console.log(valor); // Muestra lo que tiene diaHoy
```
- **Cambiar una fecha:** Para cambiar algún valor de una fecha, existen los métodos _.set...()_, los cuales permiten establecer valor especificos para el año, mes, día, etc.

```js
const diaHoy = new Date(); // Inicializar una variable de tipo Date()
let valor; // Variable auxiliar

valor = diaHoy.setFullYear('2010'); // Se establece que el año de diaHoy será 2010
valor = diaHoy.getFullYear(); // Se obtiene el año de la fecha

console.log(valor); // Muestra lo que tiene diaHoy
```

- Sin instanciar, se puede utilizar el objeto `Date()` directamente, el cual entregará información del día y momento en el que se instanción y también se puede utilizar `Date.now()` el cuál entragará los milisegundos que han pasado desde el 1 de enero de 1970 hasta la fecha en la cual se utiliza el método.

#### MomentJS tu aliado para formatear Fechas

Permite dar el formato que uno estime conveniente a la fecha. Hay que importar momentJS.
De igual forma existe locale, el cual debe importarse y también sirve para cambiar el formato de la fecha dependiendo de la locación que indique la computadora.

```js
const diaHoy = new Date();

moment.locale('es'); // Trata las fechas como se tratan en español

console.log(moment().format('MMMM')); // Trae el nombre del mes actual
console.log(moment().format('MMMM D')); // Trae el nombre del mes actual y el día
console.log(moment().format('MMMM D')); // Trae el nombre del mes actual y el día
console.log(moment().format('MMMM D YYYY')); // Trae el nombre del mes actual, el día y el año
console.log(moment().format('MMMM D YYYY h:mm:ss')); // Trae el nombre del mes actual, el día, el año y la hora
console.log(moment().format('MMMM D YYYY h:mm:ss a')); // Trae el nombre del mes actual, el día, el año, la hora y si es am o pm 

console.log(moment().format('LLLL', diaHoy)); // Formato amigable especial
```

Se pueden hacer _"operaciones"_ con las fechas.

```js
console.log(moment().add(3, 'days').calendar()); // Añade 3 días a la fecha actual,ideal para cupones con fecha de expiración
```

## JavaScript para la web

### JavaScript DOM (Document Object Model)

#### ¿Qué es el DOM?

Document Object Model, es el objeto modelo del documento HTML con el cual JS puede interactuar. El siguiente es un diagrama de lo que sería el DOM.

![Diagrama-DOM](archivos\images\Diagrama-DOM.png)

#### Código HTML a utilizar

Este código se utilizará tanto en esta sección como en la sección de [eventos](#eventos).

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>MiViaje.com</title>
    <link rel="stylesheet" href="https://necolas.github.io/normalize.css/8.0.0/normalize.css">
    <link href="https://fonts.googleapis.com/css?family=Lato:400,700,900" rel="stylesheet">
    <link rel="stylesheet" href="css/fontawesome-all.min.css">
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>

    <div class="hero">
        <header class="header contenedor">
            <div class="logo">
                <img src="img/logo.png">
            </div>
            <nav class="navegacion">
                <a href="#">Vender</a>
                <a href="#">Ayuda</a>
                <a href="#">Registro</a>
                <a href="#">Iniciar Sesión</a>
            </nav>
        </header>

        <div class="contenido-hero contenedor">
            <h1>Encuentra <span> hospedaje  </span>para tus próximas vacaciones</h1>

            <form action="/buscador" method="POST" class="formulario formulario-buscar" id="formulario" >
                <input type="text" name="busqueda" class="busqueda" placeholder="New York, Londres, Roma, Guadalajara">
                <input type="submit" value="Buscar" id="btn-submit">
            </form>
        </div>
    </div> <!--.hero-->

    <main class="contenido contenedor">
        <section class="hacer">
            <h2>Que Hacer</h2>
            <div class="contenedor-cards">
                    <div class="card">
                        <img src="img/hacer1.jpg">
                        <div class="info">
                            <p class="categoria concierto">concierto</p>
                            <p class="titulo">Música electrónica 2021</p>
                            <p class="precio">$1,200 por persona</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/hacer2.jpg">
                        <div class="info">
                            <p class="categoria concierto">concierto</p>
                            <p class="titulo">Rock en Los Ángeles</p>
                            <p class="precio">$300 por persona</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/hacer3.jpg">
                        <div class="info">
                            <p class="categoria clase">Clase Cocina</p>
                            <p class="titulo">Comida Española para Principiantes</p>
                            <p class="precio">$400 por persona</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/hacer4.jpg">
                        <div class="info">
                            <p class="categoria paseo">Paseo en Bici</p>
                            <p class="titulo">Paseo en las Montañas</p>
                            <p class="precio">$200 por persona</p>
                        </div>
                    </div> <!--.card-->
            </div> <!--.columnas4 cuadros-->
        </section>


        <section class="hacer">
            <h2 class="mi-viaje-plus">Presentamos Miviaje.com Plus</h2>
            <div class="contenedor-cards premium">
                <div class="info">
                    <h3>Una nueva sección de alojamientos de lujo</h3>
                    <a href="#" class="boton btn-mi-viaje">Explorar alojamientos </a>
                </div>
            </div> <!--.columnas4 cuadros-->
        </section>

        <section class="hospedaje">
            <h2>Hospedaje</h2>
            <div class="contenedor-cards">
                    <div class="card">
                        <img src="img/hospedaje1.jpg">
                        <div class="info">
                            <p class="categoria hospedaje">Casa completa - 2 camas</p>
                            <p class="titulo">Casa completa con todos los servicios y 2 recamaras</p>
                            <p class="precio">$3,200 por noche</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/hospedaje2.jpg">
                        <div class="info">
                            <p class="categoria hospedaje">1 Cuarto con 2 camas</p>
                            <p class="titulo">1 Cuarto con 2 camas y alberca </p>
                            <p class="precio">$2,200 por noche</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/hospedaje3.jpg">
                        <div class="info">
                            <p class="categoria hospedaje">Cabaña completa - 4 Camas</p>
                            <p class="titulo">Cabaña en Bosque para 6 personas</p>
                            <p class="precio">$2,500 por noche</p>
                        </div>
                    </div> <!--.card-->
            </div> <!--.columnas4 cuadros-->
        </section>

        <section class="destinos">
            <h2>Destinos Populares</h2>
            <div class="contenedor-cards">
                    <div class="card">
                        <img src="img/populares1.jpg">
                        <div class="info">
                            <p class="titulo">Austria</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/populares2.jpg">
                        <div class="info">
                            <p class="titulo">Francia</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/populares3.jpg">
                        <div class="info">
                            <p class="titulo">Grecia</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/populares4.jpg">
                        <div class="info">
                            <p class="titulo">Inglaterra</p>
                        </div>
                    </div> <!--.card-->
            </div> <!--.columnas4 cuadros-->
        </section>

        <section class="hacer">
                <h2>Que Hacer en New York</h2>
                <div class="contenedor-cards">
                        <div class="card">
                            <img src="img/newyork1.jpg">
                            <div class="info">
                                <p class="categoria clase">Clase</p>
                                <p class="titulo">Comida Japonesa para Principiantes</p>
                                <p class="precio">$300 por persona</p>
                            </div>
                        </div> <!--.card-->
                        <div class="card">
                            <img src="img/newyork2.jpg">
                            <div class="info">
                                <p class="categoria concierto">concierto</p>
                                <p class="titulo">Festival EDM 2021</p>
                                <p class="precio">$1,200 por persona</p>
                            </div>
                        </div> <!--.card-->
                        <div class="card">
                            <img src="img/newyork3.jpg">
                            <div class="info">
                                <p class="categoria clase">Clase de Cocina</p>
                                <p class="titulo">Paella Dominicana</p>
                                <p class="precio">$200 por persona</p>
                            </div>
                        </div> <!--.card-->
                        <div class="card">
                            <img src="img/newyork4.jpg">
                            <div class="info">
                                <p class="categoria paseo">Paseos</p>
                                <p class="titulo">Paseo a Caballo</p>
                                <p class="precio">$100 por persona</p>
                            </div>
                        </div> <!--.card-->
                </div> <!--.columnas4 cuadros-->
            </section>

    </main>
    
   

    <footer id="footer" class="footer">
        <div class="contenedor">
                <div class="nav-footer">
                    <h3 class="titulo-footer">MiViaje.com</h3>
                    <nav class="menu">
                        <a href="#">Empleo</a>
                        <a href="#">Prensa</a>
                        <a href="#">Politicas</a>
                        <a href="#">Ayuda</a>
                    </nav>
                </div>

                <div class="nav-footer">
                    <h3 class="titulo-footer">Descubre MiViaje.com</h3>
                    <nav class="menu">
                        <a href="#">Confianza y Seguridad</a>
                        <a href="#">Crédito de Viajero</a>
                        <a href="#">AirBNB Citizen</a>
                        <a href="#">Viaje de negocios</a>
                    </nav>
                </div>

                <div class="nav-footer">
                    <h3 class="titulo-footer">Hospedaje</h3>
                    <nav class="menu">
                        <a href="#">Razones para Hospedar</a>
                        <a href="#">Hospitalidad</a>
                        <a href="#">Ser un anfitrión responsable</a>
                        <a href="#">Centro de la Comunidad</a>
                    </nav>
                </div>

                <div class="nav-footer">
                    <nav class="sociales">
                        <ul>
                            <li><a href="http://facebook.com" target="_blank"><span>Facebook</span></a></li>
                            <li><a href="http://twitter.com" target="_blank"><span>Twitter</span></a></li>
                            <li><a href="http://instagram.com" target="_blank"><span>Instagram</span></a></li>
                        </ul>
                    </nav>
                    <nav class="menu">
                        <a href="#">Razones para Hospedar</a>
                        <a href="#">Hospitalidad</a>
                        <a href="#">Ser un anfitrión responsable</a>
                        <a href="#">Centro de la Comunidad</a>
                    </nav>
                </div>
        </div>
    </footer>
    <a href="#footer" class="btn-flotante">Idioma y Moneda</a>
    <!--En la etiqueta script se debe colocar la ruta del archivo .js con el que hacer pruebas en la página-->
    <!--<script src=""></script>-->
</body>
</html>
```

#### Acceder a elementos HTML con document

document es el objeto que hace referencia a todo el HTML.

```js
let elemento;

elemento = document;
elemento = document.all; // Selecciona todos los elementos que conforman el HTML
elemento = document.head; // Selecciona la cabecera del HTML
elemento = document.body; // Selecciona el cuerpo del HTML
elemento = document.domain; // Muestra el dominio donde se carga la página

elemento = document.forms; // Muestra los forms que se encuentren en la página. Los entrega como un HTMLCollection
elemento = document.forms[0]; // Muestra el primer elemento del HTMLCollection
elemento = document.forms[0].id; // Muestra el id del primer elemento del HTMLCollection
elemento = document.forms[0].method; // Muestra el método del primer elemento del HTMLCollection
elemento = document.forms[0].classList; // Muestra las clases del primer elemento del HTMLCollection
elemento = document.forms[0].action; // Muestra la ruta del primer elemento del HTMLCollection

elemento = document.links; // Muestra todos los enlaces que contienen el HTML
elemento = document.links[4]; // Muestra información del cuarto elemento (quinto enlace) del HTMLCollection creado por document.links
elemento = document.links[4].classList; // Muestra las clases del cuarto elemento (quinto enlace) del HTMLCollection creado por document.links
elemento = document.links[4].className; // // Muestra las clases del cuarto elemento (quinto enlace) del HTMLCollection creado por document.links como un string

elemento = document.images; // Muestra todas las imágenes que se encuentran en la página
elemento = document.scripts; // Muestra todas los Scripts que se encuentran en la página

console.log(elemento);
```

#### getElementsByClassName

Cada vez es menos popular, sin embargo, es necesario conocerla. Sirve para seleccionar elementos por su clase, los cuales son retornados como un _HTMLCollection_ los cuales son similares a los arreglos.

```js
// Seleccionar elementos por su clase

// Las clases se pueden repetir a lo largo del código

// Esto permite almacenar el header en la variable header lo cual permitirá que se puede interactuar con su código
const header = document.getElementsByClassName('header');
console.log(header);

const hero = document.getElementsByClassName('hero');
console.log(hero);

const contenedor = document.getElementsByClassName('contenedor');
console.log(contenedor);

// Si una clase no existe
const noExiste = document.getElementsByClassName('no-existe');
console.log(noExiste); // Entrega un HTMLCollection vacío
```

#### getElementsById

Sirve para seleccionar elementos por su id, los cuales son únicos, o sea, no puede asiganrse el mismo a id a más de un elemento. Si por algún motivo **existierán 2 id iguales**, _getElementById_ seleccionará el primero. Si no encuentra el _id_, retorna un _null_.

```js
// Seleccionar por id
const formulario = document.getElementById('formulario');
console.log(formulario);

// Seleccionar algo que no existe
const noExiste = document.getElementById('no-existe');
console.log(noExiste); // noExiste guarda un null como valor
```

#### querySelector

Retorna como máximo un elemento, pero tiene la caracteristica que permite seleccionar hasta clases, se asimila a cuando se escriben selectores en una hoja de estilos CSS. Permite seleccionar un elemento (el primero que coincida) meidante el uso de selectores de CSS (en el caso de las clases), id o etiqueta html.

```js
// Seleccionar un elemento por su clase (con la sintaxis de CSS)
const card = document.querySelector('.card');
console.log(card); // Retorna el primer elemento que ocupe la clase mencionada

// Se pueden utilizar selectores específicos como los de CSS
const info = document.querySelector('.premium .info');
console.log(info);

// Seleccionar un elemento que comparte clase con otro que está primero (con la sintaxis de CSS)
const segundoCard = document.querySelector('section.hospedaje .card:nth-child(2)');
console.log(segundoCard);

// Seleccionar elemento por el id (con la sintaxis de CSS)
const formulario = document.querySelector('#formulario');
console.log(formulario);

// Seleccionar elementos por su etiqueta HTML
const navegacion = document.querySelector('nav');
console.log(navegacion);
```

#### querySelectorAll

A diferencia de _querySelector_, **_querySelectorAll_** retorna todos los elementos que coincidan con el selector que se le entrega, como por ejemplo, todos los elementos que compartan una misma clase. Tanto _querySelector_ como _ querySelectorAll_ comparten sintáxis. Retorna un NodeList, similar a un arreglo, el cual contienen todo los nodos (etiquetas del HTML, <div\>, <a\>, <p\>, etc).

```js
// Seleccionar todos los elementos de una misma clase
const card = document.querySelectorAll('.card');
console.log(card); // Retorna un NodeList, similar a un arreglo

// Si no se encuentra coincidencia con el selector
const noExiste = document.querySelectorAll('.no-existe');
console.log(noExiste); // NodeList vacía
```

#### Modificar Textos o Imagenes con JS

##### Modificar Textos

Hasta ahora sólo se ha visto como seleccionar elementos de la página pero no se ha visto de que sirve hacerlo. La idea es seleccionar elementos y modificarlos para hacerlos más dinámicos meidante el uso de JS.

En el ejemplo de la sección, se debe seleccionar el _<h1\>_ el cual será útil para practicar con el texto que contiene.

```js
const encabezado = document.querySelector('.contenido-hero h1');
console.log(encabezado);
```

1. **Mostrar texto con JS:** Para seleccionar texto con JS exiten 3 formas:

- Utilizar _elemento.innerText_ para traer el texto, hay que tener en consideración que si en el CSS se encuentra la propiedad **_visibility: hidden;_**, no retornará nada.

```js
console.log(encabezado.innerText);
```

- Utilizar _elemento.textContent_ para traer el texto, sin importar las propiedades en el CSS.

```js
console.log(encabezado.textContent); // Lo retorna tal cual está en el HTML
```

- Utilizar _elemento.innerHTML_ para traer el HTML, o sea, si hay código HTML dentro del texto, aparecerá igual.

```js
console.log(encabezado.innerHTML); // Retorna tanto el texto como el código HTML que haya entre medio
```

2. **Seleccionar el texto con JS:** Se puede aplicar encadenamiento para seleccionar directamente el texto, sin la necesidad de seleccionar primero la etiqueta HTML por ejemplo.

```js
// Encadenamiento para seleccionar un elemento directamente
const encabezado = document.querySelector('.contenido-hero h1').textContent;
console.log(encabezado);
```

3. **Modificar el texto con JS:** Con el texto seleccionado, como si de una variable se tratase, se puede cambiar su valor.

```js
// Cambiar el texto con JS
document.querySelector('.contenido-hero h1').textContent = 'Nuevo Encabezado';
```

##### Modificar imágenes

Para la modificación de imágnes, lo que se puede hacer es modificar su fuente, o sea, su _src_.

En este caso de ejemplo, se seleccionará la prmera imagen que se encuentra en el div con la clase _contenedor-cards_.

```js
// Seleccionar imágen
const imagen = document.querySelector('.contenedor-cards .card img');
// Se comprueba que está seleccionado
console.log(imagen);
```

Exisistirá un gran número de propiedades que se pueden modificar de esa imagen, las cuales en navegadores como _Firefox Developer Edition_ se pueden ver todas,sin embargo, en este caso lo que importa es modificar el _src_ de la imágen por el de otra imágen.

```js
// Se cambiar el src de esa imagen por el de otra
imagen.src = 'https://n9.cl/1nznq'
```

#### Cambiando el CSS con JS

Con JS se pueden cambiar las propiedades CSS asociadas a un elemento, utilizando la propiedad _.style_ seguida por la propiedad de CSS las cuales siguen la escritura de variables en JS, ejemplo _backgroud-color_ se escribe _.backgroundColor_. La otra forma es añadiendo o eliminando clases a un elemento con los métodos _elemento.classList.add('nombre-clase')_ o _elemento.classList.remove('nombre-clase')_ respectivamente.

```js
const encabezado = document.querySelector('.contenido-hero h1');
console.log(encabezado);

// Acceder a la propiedad Style del h1
console.log(encabezado.style); // Permite ver todas las propiedades que tiene el elemento

// FORMA SENCILLA DE CAMBIAR PROPIEDADES UNA A UNA
// Cambiar el color del fondo del h1
encabezado.style.backgroundColor = 'red';
// Las mismas propiedades de CSS se pueden encontrar en JS con una sintaxis similar pero no igual en el nombre de las propiedades

// Cambiar la fuente del h1
encabezado.style.fontFamily = 'Arial';

// Transformarlo a mayúsculas
encabezado.style.textTransform = 'uppercase';

// AGREGANDO O ELIMINANDO CLASS-NAMES
/*Es más recomendable establecer un estilo para una clase, la se puede añadir o eliminar
con código JS*/

// Seleccionar el primer elemento de la clase card
const card = document.querySelector('.contenedor-cards .card');
card.classList.add('nueva-clase','segunda-clase'); // Añade 2 nuevas clases 
console.log(card.classList); // Muestra el arreglo con todas las clases del contenedor card
console.log(card);
card.classList.remove('segunda-clase'); // Elimina la clase segunda-clase
console.log(card.classList); // Muestra el arreglo con todas las clases del contenedor card
console.log(card);
```

#### Traversing the DOM

Traversing the DOM hace referencia a recorrer el DOM como si de una mapa se tratase.

```js
/*Recorrer desde el elemento padre hacía los hijos*/
// Seleccionar el elemento <nav>
const navegacion = document.querySelector('.navegacion');
console.log(navegacion);
console.log(navegacion.childNodes); // Cuenta como elemento los espacios en blanco (saltos de línea)
console.log(navegacion.children); // Cuanta sólo elementos reales del HTML. Retorna un HTMLCollection
console.log(navegacion.children[2]); // Muestra el tercer elemento

/*Acceder al primer y ultimo elemento*/
console.log(navegacion.firstElementChild); // Primer elemento hijo de la navegación
console.log(navegacion.lastElementChild); // Último elemento hijo de la navegación
```
```js
// Seleccionar un elemento del contendedor clase .card
const card = document.querySelector('.card');
console.log(card);
console.log(card.children);

// Acceder al título
console.log(card.children[1].children[1].textContent);
/*el primer acceso es al contendedor de la información y
el segundo es para acceder al párrafo <P>, finalmente .textContent
es para acceder al texto del párrafo*/

// Cambiar imagen del elemento del contendedor clase .card con traversing
const imagen = card.children[0];
console.log(imagen);
//imagen.src = 'https://n9.cl/1nznq';

/*Recorrer desde los elementos hijos hacía el padre*/
// Acceder al nodo padre del elemento seleccionado
console.log(card.parentNode); // Las propiedades que se refieran a los Node incluyen saltos de línea
console.log(card.parentElement); // PErmite ver el elemento padre sin contar los saltos de línea
console.log(card.parentElement.parentElement); // Accede al elemento padre del elemento padre
/*Se pueden utilizar tanto parentElement como sea necesario*/

/*Acceder a los elementos hermanos (los que comparten un mismo elemento padre) de un elemento*/
console.log(card.nextElementSibling); // Segundo elemento card
console.log(card.nextElementSibling.nextElementSibling); // Tercer elemento card
console.log(card.nextElementSibling.nextElementSibling.nextElementSibling); // Cuarto elemento card
//console.log(card.nextElementSibling.nextElementSibling.nextElementSibling.nextElementSibling); // No hay un quinto elemento, muestra un null

/*Seleccionar un elemento que comparte clase con otros*/
const ulitmoCard = document.querySelector('.card:nth-child(4)');
console.log(ulitmoCard);
/*Seleccionar los elementos hermanos anteriores a los de un elemento*/
console.log(ulitmoCard.previousElementSibling);
```

#### Eliminar elementos del DOM

Existen 2 formas de hacerlo, eliminando un elemento por si mismo y la otra es eliinarlo desde el padre.

```js
const primerEnlace = document.querySelector('a'); // Selecciona el primer enlace en el HTML
console.log(primerEnlace);

// Eliminar un elemento directamente con el método .remove()
primerEnlace.remove(); // Ya no se encuentra en el DOM

// Eliminar desde el padre
// Lo primero es seleccionar el element padre
const navegacion = document.querySelector('.navegacion');
console.log(navegacion);

// Lo segundo es identificar el elemento a eliminar
console.log(navegacion.children); // Aparte de mostrar los elemento, da la posición de los mismos
navegacion.removeChild(navegacion.children[1]); // Recibe la posición del elemento hijo a eliminar
```

#### Creación de HTML con JS

A grandes rasgos, son 3 los pasos a seguir para crear HTML con JS, **crear elemento, seleccionar donde añadirlo, elegir la forma de añadirlo**.

1. **Crear el elemento:** Para crear el elemento de puede utilizar el método _.createElement()_ perteneciente el DOM `document.createElement()`, el cual recibe la etiqueta HTML con la que se quiere crear elemento, tanto en miniscula como en mayuscula (a, img, h1, div, etc).

```js
// .createElement() recibe la etiqueta del elemento a crear div, h1, img, a, etc
const enlace = document.createElement('a'); // Crea un enlace
```

Luego hay que dotar con atributos al elemento, se pueden añadir cuantas uno quiera.

```js
/*Ejemplos de atributos que se pueden agregar*/
// Se pueden agregar cuantos atributos sean necesarios
// Agregando texto al enlace
enlace.textContent = 'Nuevo Enlace';
// Agregando href
enlace.href = '/nuevo-enlace';
console.log(enlace);
// Agregando una clase
enlace.classList.add('nueva-clase');
// Agregar atributo personalizado
enlace.setAttribute('data-enlace','nuevo-enlace');
```

2. **Elegir donde irá el elemento:** Con elemento creado como uno quiere, es necesario seleccionar el lugar donde irá, o sea, el elemento padre que lo contendrá.

En el siguiente ejemplo se seleccionará la navegación como el elemento padre que contendrá el elemento enlace anteriormente creado.

```js
// Seleccionar donde insertar el nuevo elemento
const navegacion = document.querySelector('.navegacion'); // Se selecciona la etiqueta nav con su clase nevgacion
console.log(navegacion); // Se muestra por consola que la selección se haya realizado correctamente
```

3. **Elegir la forma de añadirlo:** Existen dos formas para añadir un nuevo elemento, puede ser directamente como último elemento hijo (_.appendChild()_) o antes de otro elemento (_.insertBefore()_).

- **Agregar elemento al final:** Esto se hace utilizando el método _.appendChild()_ en el elemento padre. Este método recibe como parámetro el elemento que se agregará como hijo.

```js
navegacion.appendChild(enlace); // Añade como último elemento el elemento que se le entrega
console.log(navegacion);
```

- **Agregar elemento antes de otro elemento:** Esto se hace utilizando el método _.insertBefore()_ en el elemento padre. Este método recibe como parámetros el elemento que se quiere agregar y el elemento que servirá como referencia para saber antes de que elemento se agregará el nuevo hijo. Para dar esa referencia, se puede utilizar el método _.childre()_ en el padre para saber la posición de el elemnto de referencia y luego utilizarlo de nuevo como parametro, indicando su indice correspondiente.

```js
console.log(navegacion.children); // Muestra un HTMLCollection con la posición de todos los elementos hijos desde el 0 en adelante similar a un arreglo
navegacion.insertBefore(enlace, navegacion.children[1]); // Recibe el elemento a agregar y el elemento de referencia para insertar antes de ese elemento
```

El siguiente es un ejemplo en el cual se crear una nueva tarjeta para el primer contendor-cards, en el cual se utiliza todo lo anterior, junto a el método _.append()_ el cual a diferencia de _.appendChild()_, permite añadir más de un elemento a la vez, siempre teniendo en consideración que el orden en el que se pasen como parametros lo elementos será el orden con el que se añadirán al padre.

```js
/* Crear un card */

// Crear el elemento contenedor de clase card
const newCard = document.createElement('div');
newCard.classList.add('card');
//console.log(newCard);

// Crear el elemento img
const imagen = document.createElement('img');
imagen.src = 'img/hacer1.jpg'
//console.log(imagen);

// Crear contenedor de clase info
const info = document.createElement('div');
info.classList.add('info');
//console.log(info);

// Crear elementos p
// Elemento Categoria
const parrafoCategoria = document.createElement('p');
parrafoCategoria.classList.add('categoria','clase');
parrafoCategoria.textContent = 'Clase DJ';
//console.log(parrafoCategoria);

// Elemento Título
const parrafoTitulo = document.createElement('p');
parrafoTitulo.classList.add('titulo');
parrafoTitulo.textContent = 'Fundamentos de la mezcla musical para fiestas';
//console.log(parrafoTitulo);

// Elemento Precio
const parrafoPrecio = document.createElement('p');
parrafoPrecio.classList.add('precio');
parrafoPrecio.textContent = '$350 por persona';
//console.log(parrafoPrecio);

// Añadir parrafos al contenedor info usando .append() que permite añadir más de un elemento a la vez
info.append(parrafoCategoria,parrafoTitulo,parrafoPrecio);
//console.log(info);

// Añadir imagen e info a newCard
newCard.append(imagen,info);
//console.log(newCard);

// Seleccionar el elemento padre donde se añadirá la nueva card. Tener cuidado con los selectores a utilizar
const contenedorCards = document.querySelector('.hacer .contenedor-cards');
//console.log(contenedorCards);

// Añadir al final el elemento completo al elemento padre
contenedorCards.appendChild(newCard);
console.log(contenedorCards);

// Si se quiere añadir el elemento en otra posición se puede hacer lo siguiente
// Antes de descomentar el siguiente código, se recomienda comentar el anterior en donde se añade al final
/*
console.log(contenedorCards.children);
contenedorCards.insertBefore(newCard, contenedorCards.children[2]); // Se añade en la tercera posición
console.log(contenedorCards);
*/
```

En el ejemplo anterior, se fueron creando elementos desde el más general que los contiene a todos (newCard) hasta el más especificos (los parrafos) y luego se fueron agregando desde los más especificos al más general.

#### Ejemplo Avanzado de manipulación del HTML con JS (botón interactivo)

El siguiente es un ejemplo de como se puede hacer que un botón sea interactivo mediante la manipulación de las clases CSS asociadas a elementos del HTML. En este caso se modifican las clases del footer y de un botón el cual mediante la utilización de un _.addEventListener()_ mostrará el footer cuando se haga click en él.

Para hacer lo anterior,  _.addEventListener()_ recibe el tipo de evento que lo activará y una función que tendrá el código a ejecutar cuando se haga click sobre el botón. Cabe mencionar que la función que recibe el método puede ser tanto una definida con anterioridad o una función anonima.

```js
// Selección de los elementos con los que se trabajará
const btnFlotante = document.querySelector('.btn-flotante');
console.log(btnFlotante);
const footer = document.querySelector('.footer');
console.log(footer);
```

```js
// Con función anónima
btnFlotante.addEventListener('click', () => {
    /*.classList.contains() permite saber si el elemento tiene
    la clase que se entrega como parámetro al método*/

    // Si el footer contiene la clase activo, se remueve
    if(footer.classList.contains('activo')){
        footer.classList.remove('activo');
        btnFlotante.classList.remove('activo');
        btnFlotante.textContent = 'Idioma y Moneda';
    } else{
        // De lo contrario, se añade
        footer.classList.add('activo');
        btnFlotante.classList.add('activo');
        btnFlotante.textContent = 'Cerrar';
    }
})
```

```js
// Con función normal
// Función para mostrar y ocultar el footer con un botón
function mostrarOcultarFooter(){
    if(this.classList.contains('activo')){
        footer.classList.remove('activo');
        this.classList.remove('activo'); // Los this hacen referencia btnFlotante al que se le agregó el EventLitstener
        this.textContent = 'Idioma y Moneda';
    } else{
        footer.classList.add('activo');
        this.classList.add('activo');
        this.textContent = 'Cerrar';
    }
}

// Se le añade un EventListener que reacciona los clicks
btnFlotante.addEventListener('click', mostrarOcultarFooter);
```

### Eventos

**Nota: Se seguirá utilizando el mismo código HTML de la sección anterior [DOM](#código-html-a-utilizar).**

Para el  _.addEventListener()_, existe una gran cantidad de eventos, los cuales algunos se irán viendo a lo largo de esta sección.

#### Detectar cuando el HTML ha cargado por completo

Entre los tipos de eventos que recibe _.addEventListener()_ se encuentra _DOMContentLoaded_ el cual sirve para saber cuando cargó por completo el HTML de la página.

```js
document.addEventListener('DOMContentLoaded', () => {
    console.log('Documento Listo');
});
```

#### Eventos con el mouse

Existe una gran variedad de eventos que suceden con el mouse, en los siguiente bloques de código se pondrán algunos.

Se selecciona la navegación como el elemento en el cual se probarán los eventos con el mouse.

```js
const navegacion = document.querySelector('nav');
console.log(navegacion);
```

##### Click

Se activa cuando se realiza cualquier tipo de click sobre el elemento.

```js
// Evento click
// click con el mouse
navegacion.addEventListener('click', () => {
    console.log('click en nav');
});
```

##### Mouseenter

Se activa cuando el cursor entra a la zona del elemento.

```js
// Evento mouseenter
// Pasar el cursor sobre el elemento, entrar a la zona del elemento
navegacion.addEventListener('mouseenter', () => {
    console.log('cursor sobre la nevegacion');
});
```

##### Mouseout

Se activa cuando el cursor sale de la zona del elemento.

```js
// Evento mouseout
// Sacar el cursor de la zona del elemento
navegacion.addEventListener('mouseout', () => {
    console.log('cursor sale de la nevegacion');
});
```

##### Mousedown

Se activa cuando se hace click en el elemento.

```js
// Evento mousedown
// Similar al click
navegacion.addEventListener('mousedown', () => {
    console.log('click con el mouse');
});
```

##### Mouseup

Se activa cuando se hace click y se suelta el click.

```js
// Evento mouseup
// Hace click y luego suelta
navegacion.addEventListener('mouseup', () => {
    console.log('se dejo de presionar');
});
```

##### Dbclick

Se activa cuando se hace doble click en el elemento.

```js
// Evento dblclick
// Detecta el doble click
navegacion.addEventListener('dblclick', () => {
    console.log('doble click detectado');
});
```

#### Eventos sobre los inputs

Son los eventos que suceden en el teclado.
Para los siguientes eventos, hay que ubicarse en la barra de búsqueda.

```js
const busqueda = document.querySelector('.busqueda');
console.log(busqueda);
```

##### Keydown

Es un evento que registra cuando se escribe algo, reacciona a cualquier tipo de tecla, no necesariamente a las letras.

```js
// Se activa cuando se presiona cualquier tecla. Mantener presionado es como presionar muchas veces 
busqueda.addEventListener('keydown', () => {
    console.log('Se presionó una tecla');
});
```

##### Keyup

Es un evento que registra cuando se deja de presionar una tecla.

```js
// Evento keyup
// Se activa cuando se deja de presionar una tecla 
busqueda.addEventListener('keyup', () => {
    console.log('Se soltó una tecla');
});
```
##### Blur

Es un evento que se activa al presionar fuera del input.

```js
// Evento blur
// Se activa cuando se presiona el input (entra) y luego se presiona fuera de él 
busqueda.addEventListener('blur', () => {
    console.log('salió del input');
});
```

##### Copy

Es un evento que se activa cuando se copia algo en el input, ya sea utilizando el comando o la opción después de presionar el botón derecho.

```js
// Evento copy
// Se activa cuando se copia (de cualquier forma) algo escrito en el input 
busqueda.addEventListener('copy', () => {
    console.log('Copiado');
});
```

##### Paste

Es un evento que se activa cuando se pega algo en el input, ya sea utilizando el comando o la opción después de presionar el botón derecho.

```js
// Evento paste
// Se activa cuando se pega (de cualquier forma) algo en el input 
busqueda.addEventListener('paste', () => {
    console.log('Pegado');
});
```

##### Cut

Es un evento que se activa cuando se corta algo en el input, ya sea utilizando el comando o la opción después de presionar el botón derecho.

```js
// Evento cut
// Se activa cuando se corta (de cualquier forma) algo en el input 
busqueda.addEventListener('cut', () => {
    console.log('cortado');
});
```

##### Input

Es un evento que se activa con cualquiera de los eventos antes vistos, exceptuando el evento _blur_.

```js
// Evento input
// Se activa con cualquiera de las acciones anteriores (excepto blur), 
// ya que hace referencia al input de algo 
busqueda.addEventListener('input', () => {
    console.log('Ingresando...');
});
```

##### Información de un evento

Para saber que ocurre durante el evento, se puede agregar un parámetro a la función anónima con el nombre de evento, e o evt.

Lo siguiente es el tipo de información que se tiene del evento, en este caso, del evento input.

```js
busqueda.addEventListener('input', (e) => {
    console.log(e);
});
```

![Tipo-de-informacion](\archivos\images\info-evento.png)

Un ejemplo de lo que se puede hacer con la información del evento, es la validación de si existe texto o no, utilizando la propiedad _e.target.value_ la cual entrega lo que se está escribiendo en el input.

```js
busqueda.addEventListener('input', (e) => {
    // e.target.value permite saber lo que se escribió en el input
    if(e.target.value == ''){
        console.log('No hay texto');
    } else{
        console.log('Hay texto');
    }
});
```

#### Evento Submit a un formulario

El evento _submit_ es aquel que se acciona cuando el usuario envia un fomrulario, esto puede ser es un buscados, cuando se presiona enter o el botón de buscar.

Entre lo que el evento registra, se encuentra el método _.preventDefault()_ el cuál permite evitar cualquier acción por default que tenga el elemento seleccionado.

```js
const formulario = document.querySelector('#formulario'); // Seleccionar formulario por su id
//console.log(formulario);

// Evento submit
// Es aquel evento que se acciona cuando el usuario presiona el botón submit (enter, ingresar, buscar, etc)
formulario.addEventListener('submit', (e) => {
    e.preventDefault(); // Evita que se ejecute la acción predeterminada al presionar el botón de submit
    console.log(e); // Se muestra por consola todo lo que trae el evento
    console.log(e.target.method); // Tipo de método por default   
    console.log(e.target.action); // Enlace de destino del formulario cuando se mande
});
```

#### Eventos al dar scroll con el mouse

A diferencia de los otros eventos, estos eventos ocurren en la ventana global, poe lo cual se utiliza el objeto _window_

##### Scroll

Detecta el Scroll, ya sea hacía arriba o hacía abajo.

```js
window.addEventListener('scroll', () => {
    console.log('Se hace scroll');
});
```

Se puede utilizar la propiedad _window.scrollY_ para saber la cantidad de pixeles a los que equivale el scroll, cuando se hace scroll hacía abajo suma los pixeles mientras que cuando se hace scroll hacía arriba va restando los pixeles.

```js
window.addEventListener('scroll', () => {
    const scrollPx = window.scrollY; // Cantidad de pixeles que se hace scroll
    console.log(scrollPx);
});
```

Saber la posición de de algún elemento, puede servir para ejecutar alguna acción cuando se alcane el mismo. En el siguiente ejemplo se ejecuta algo al quedar visible un elmento especifico.

```js
window.addEventListener('scroll', () => {
    const premium = document.querySelector('.contenedor-cards.premium');
    const ubicacion = premium.getBoundingClientRect(); // Entre lo que contiene, se encuentra la distancia que hay entre el elemento y donde uno se encuentra en la página
    if(ubicacion.top < 100){
        console.log('El elemento ya es visible');
    } else{
        console.log('Aún no, da más scroll');        
    }
});
```

#### Event Bubbling y como evitarlo

El _Event Bubbling_ es cuando los eventos se esparcen como una burbuja, esto ocurre cuando hay eventos asigandos tanto a hijos como a padres, lo que provoca que el evento del hijo active el evento del padre.

```js
const card = document.querySelector('.contenedor-cards .card:nth-child(1)');
const informacion = document.querySelector('.contenedor-cards .card:nth-child(1) .info');
const titulo = document.querySelector('.contenedor-cards .card:nth-child(1) .info .titulo');
// console.log(card);
// console.log(informacion);
// console.log(titulo);

card.addEventListener('click', () => {
    console.log('click en tarjeta');
});

informacion.addEventListener('click', () => {
    console.log('click en informacion');
});

titulo.addEventListener('click', () => {
    console.log('click en titulo');
});
```

En el ejemplo anterior, presionar sobre la primera card, sólo muestra el "click en tarjeta", en cambio, dar click en la info muestra tanto "click en tarjeta" como "click en informacion" y presionar en el título, provocará que se muestren los 3 clicks en consola.

Para evitar el _Event Bubbling_ existen 3 formas, utilizar el método _e.stopPrpagation()_, prevenir con _Delegation_ y prevenir utilizando un método.

##### e.stopPropagation()

_.stopPropagation()_ evita la propagación de eventos. El método se asocia a la variable evento que se le asigne a la función anonima.

```js
card.addEventListener('click', (e) => {
    e.stopPropagation();
    console.log('click en tarjeta');
});

informacion.addEventListener('click', (e) => {
    e.stopPropagation();
    console.log('click en informacion');
});

titulo.addEventListener('click', (e) => {
    e.stopPropagation(); // Detiene la propagación de eventos
    console.log('click en titulo');
});
```

##### Delegation

Es cuando se tiene un selector principal (el padre de ciertos elementos) que se utiliza para realizar acciones con un evento en otroa elementos contenidos por este mismo.

En el siguiente ejemplo se selecciona una tajeta y se la añade un _Event Listener_ y dependiendo de la clase que contenga el elemento que uno clickea, muestra por consola algo distinto.

```js
const card = document.querySelector('.contenedor-cards .card:nth-child(1)');
console.log(card);


card.addEventListener('click', (e) => {

    // Sirve para saber el tipo de etiqueta
    if(e.target.localName == 'img'){
        console.log('Diste click en la imagen');
    }

    // Dependiendo de la clase que contenga se hace algo
    if(e.target.classList.contains('titulo')){
        console.log('Diste click en el título');
    }

    if(e.target.classList.contains('categoria')){
        console.log('Diste click en la categoría');
    }


    if(e.target.classList.contains('precio')){
        console.log('Diste click en el precio');
    }
});
```

#### .onclick

Sirve para mandar a llamar una función al momento de presionar sobre un elemento. Se suele utilizar cuando se crea contenido HTML. Se implementa como una propiedad, la que tendrá como valor una función anonima que en su cuerpo tendrá el código a ejecutar o se mandará a llamar la función que se  quiere ejecutar. Es practicamente como añadir un _.addEventListener()_ al momento de generar un elemento de HTML con JS.

```js
// Evitar la propagación con contenido creado...
const parrafo1 = document.createElement('P');
parrafo1.textContent = 'Concierto';
parrafo1.classList.add('categoria');
parrafo1.classList.add('concierto');
// .onclick
parrafo1.onclick = function(){
    console.log('Este es el primer parrafo desde la función anónima más común');
};

// Segundo parrafo
const parrafo2 = document.createElement('P');
parrafo2.textContent = 'Concierto de Rock';
parrafo2.classList.add('titulo');
// .onclick
parrafo2.onclick = () => {
    console.log('Este es el segundo parrafo desde función anónima tipo arrow function');
};

// 3er parrafo...
const parrafo3 = document.createElement('p');
parrafo3.textContent = '$800 por persona';
parrafo3.classList.add('precio');
// .onclick
parrafo3.onclick = function(){
    nombreFuncion('nombreFuncion'); // Llamado de la función definida fuera de esta función
};

// Función que da el nombre de una función
function nombreFuncion(nombreF){
    console.log(`Este es el tercer parrafo desde la función ${nombreF}`);
}

// crear el div...
const info = document.createElement('div');
info.classList.add('info');
info.appendChild(parrafo1)
info.appendChild(parrafo2)
info.appendChild(parrafo3);

// Vamos a crear la imagen
const imagen = document.createElement('img');
imagen.src = 'img/hacer2.jpg';
// .onclick
imagen.onclick = function(){
    console.log('Esto es una imagen');
}

// Crear el Card..
const contenedorCard = document.createElement('div');
contenedorCard.classList.add('contenedorCard');

// Vamos a asignar la imagen al card...
contenedorCard.appendChild(imagen);

// y el info
contenedorCard.appendChild(info);

// Insertarlo en el HTML...
const contenedor = document.querySelector('.hacer .contenedor-cards');
contenedor.appendChild(contenedorCard); // al inicio info
```

### LocalStorage

Pertenece a la API de Js, o sea, utiliza el objeto _window_. El cual no es necesario color cada vez que se utiliza alguna de sus propiedades o métodos.

Local Storage permite almacenar cierta información en el navegador sin perderla cuando la computadora se apaga.

También existe algo llamado Session Storage que sirve para almacenar información durante la sesión, o sea, mientras uno se encuentre en la página web.

#### Agregar elementos a localStorage

Para agregar elementos hay que utilizar el método `localStorage.setItem(llave, valor)`, el cual recibe una llave, o nombre de lo que se guardará, que además sirve para luego buscarlo y su valor el cual puede ir variando. 

```js
localStorage.setItem('curso', 'JavaScript');
```

**Es importante aclarar que Local Storage sólo puede guardar Strings**, no puede guardar enteros, arreglos, objetos, sin embargo se pueden guardar los objetos y los arreglos utilizando el método `JSON.stringify()`,el cual recibe un arreglo u objeto para ser trandformado en un string que si podrá ser almacenado en Local Storage.

```js
const producto = {
    nombre: "Monitor 24 Pulgadas",
    precio: 300
}

const productoString = JSON.stringify( producto );
localStorage.setItem('producto', productoString);

const meses = ['Enero', 'Febrero', 'Marzo'];
const mesesString = JSON.stringify( meses );
localStorage.setItem('meses', mesesString);

// Versión alternativa sin crear una variable extra
// localStorage.setItem('meses', JSON.stringify( meses ));
```

#### Obtener elementos de Local Storage

Para obtener elementos de Local Storage, se utiliza el método `localStorage.getItem(llave)`, el cuál recibe la llave o nombre que se le dio al ser alamcenado en el Local Storage.

Hay que tener en cuenta que lo que se obtiene desde Local Storage es un string, ya que, eso es lo único que puede almacenar, es por esto que al momento de alamcenar un objeto o un arreglo, se utiliza `JSON.stringify()`, tal como existe el método anterior para transformar objetos y arreglos en string, existe el método `JSON.parse()` el cuál transforma los strings con estructura de objeto o arreglo en objetos y arreglos.

```js
const curso = localStorage.getItem('curso');
console.log(curso);

const producto = JSON.parse(localStorage.getItem('producto')); // JSON.parse(), transforma un string en el tipo al que corresponde su estructura
console.log(producto);

const meses = JSON.parse(localStorage.getItem('meses'));
console.log(meses);
```

#### Eliminar y actualizar elementos de Local Storage

##### Quitar elementos de Local Storage

Para quitar un elemento de Local Storage existe el método `localStorage.removeItem(llave)`, el cual recibe la llave o nombre que se le dio al elemento cuando se alamcenó en Local Storage.

Si lo que se quiere es eliminar todo lo que haya en Local Storage, se debe utilizar el método `localStorage.clear()`.

```js
// Quitar elemento
localStorage.removeItem('producto'); // Elimina el elemento producto

// Quitar todo lo que haya en Local Storage
//localStorage.clear();
```

##### Actualizar elementos en Local Storage

No existe como tal un método para la actualización, pero se pueden sobreescribir los elementos mediante la utilización del método `localStorage.setItem(llave, nuevoValor)`, el cual recibe la llave del elemento que se quiere actualizar y el nuevo valor que se le quiere dar.

```js
// En el caso de Local Storage no existe un método para actualizar
// La actualización de un elemento se basa en sobreescribirlo (obtención -> modificación -> volver a almacenar con la misma llave)

// Actualizar arreglo de meses
const mesesArreglo = JSON.parse(localStorage.getItem('meses')); // Se obtiene el arreglo almacenado en Local Storage
console.log(mesesArreglo); // Se muestra el arreglo obtenido
const mesesArregloActualizado = [...mesesArreglo, 'Abril', 'Mayo', 'Junio']; // Se crea un nuevo arreglo (se puede utilizar .push() para evitar crear otro arreglo) con los meses antiguos y nuevos
console.log(mesesArregloActualizado); // Se muestra el nuevo arreglo
localStorage.setItem('meses', JSON.stringify(mesesArregloActualizado)); // Se almacena el nuevo arreglo en formato de String con la misma llave
```

## JavaScript Intermedio/Avanzado

### Prototypes en JavaScript

#### ¿Qué es el Proto? y crear un tipo de objeto nuevo

Hasta ahora se conocía la sitaxis de _Object Literal_, la cual es la que más se utiliza pero a es menos dinámica.

```js
// Object Literal
// Menos dinámico
const cliente = {
    nombre: 'Juan',
    saldo: 500
}

console.log(cliente);
console.log(typeof(cliente)); // object
```

Es aquí donde la _Programación orientada a objetos_ o _POO_ entra en acción. La idea de este tipo de programación es la de poder hacer más dinámica la creación de objetos. Existen los constructores de objetos, los cuales mediante la entrega de argumentos, instancias valores para un nuevo obejto.

```js
// Object Constructor
// Permite crear multiples instancias del mismo objeto

function Cliente(nombre, saldo){
    this.nombre = nombre;
    this.saldo = saldo;
}

const pedro = new Cliente('Pedro', 500);
console.log(pedro);
console.log(typeof(pedro));
```

#### El problema de no usar prototypes

Lo malo de programar sin prototypes es que si muchas personas trabajan sobre el mismo código, no saben que funciones ocupar o que hace cada función.

En el siguiente ejemplo, es un poco más complicado entender cual función pertenece a cada objeto, es ahí donde prototype ayuda a la comprensión y estructura.

```js
function Cliente(nombre, saldo){
    this.nombre = nombre;
    this.saldo = saldo;
}

const pedro = new Cliente('Pedro', 500);
console.log(pedro);
console.log(typeof(pedro));

// Muestra por consola el nombre y saldo de un cliente
function formatearCliente(cliente){
    const { nombre, saldo } = cliente;
    console.log(`El Cliente ${nombre} tiene un saldo de ${saldo}`);
}

formatearCliente(pedro);


function Empresa(nombre, saldo, categoria){
    this.nombre = nombre;
    this.saldo = saldo;
    this.categoria = categoria;
}

const pepsi = new Empresa('Pepsi', 500000000, 'alimentos');
console.log(pepsi)

formatearCliente(pepsi); // Muestra el nombre y el saldo pero no la categoría

// Para mostrar toda la información es necesario crear otra función
function formatearEmpresa(empresa){
    const { nombre, saldo, categoria } = empresa;
    console.log(`La Empresa ${nombre} tiene un saldo de ${saldo} y su categoría es ${categoria}`);
}

formatearEmpresa(pepsi);
```

#### Creación de un prototype

Los prototypes mantienen la referencia al objeto y se vuelven único para ese objeto.

Los prototypes también se pueden llamar desde dentro de otros prototypes, utilizando this. en vez del nombre del objeto.

Se utilizan funciones anónimas con la sintaxis de function() y no de Arrow Function para crearlos. Lo anterior se debe a que las Arrow Function buscan en la ventana global las variables que utilizan el this., en cambio, function() busca en el objeto al que hace referencia su declaración.

```js
// Declaración del constructor 
function Cliente(nombre, saldo){
    this.nombre = nombre;
    this.saldo = saldo;
}

// Instanciar nuevo cliente
const pedro = new Cliente('Pedro', 6000);
console.log(pedro);

// Funciones exclusivas para un nuevo cliente
Cliente.prototype.tipoCliente = function(){
    let tipo;
    if(this.saldo > 10000){
        tipo = 'GOLD';
    } else if( this.saldo > 5000){
        tipo = 'PLATINUM';
    } else{
        tipo = 'Normal';
    }

    return tipo;
}

Cliente.prototype.nombreClienteSaldo = function(){
    return `Nombre: ${this.nombre} \nSaldo: ${this.saldo} \nTipo Cliente: ${this.tipoCliente()}`
}

Cliente.prototype.retiraSaldo = function(retira){
    if(this.saldo >= retira){
        this.saldo -= retira;
    }
}

// Llamado funciones (métodos) de un objeto
console.log(pedro.tipoCliente()); // Obtiene el tipo de cliente
console.log(pedro.nombreClienteSaldo()); // Muestra los datos del cliente 
pedro.retiraSaldo(5000); // El cliente retira 5000
console.log(pedro.nombreClienteSaldo()); // Muestra los nuevos datos del cliente
```

#### Heredar un Prototype

Existe algo llamado _God Object_ el cual es el objeto principal desde el cual otros objetos van heredando propiedades y funciones. Lo anterior es posible gracias a la existencia de la herencia entre los objetos. Para heredar propiedades se debe utilizar el método `ObjetoPadre.call(this, propiedad1, propiedad2,..., propiedadn)` en el constructor del objeto al cual se le quiere heredad propiedades y para heredar las funciones, se debe asignar el prototype del objeto hijo el prototype del objeto padre con el método `Object.create( ObjetoPadre.prototype )`. Lo anterior hará que el constructor no se encuentre si se expande el objeto en la consola, por lo cual se debe asignar el objeto padre al constructor del objeto hijo `ObjetoHijo.prototype.constructor = ObjetoPadre;`

```js
// Heredar un Prototype

function Cliente(nombre, saldo){
    this.nombre = nombre;
    this.saldo = saldo;
}

// Instanciar nuevo cliente
const pedro = new Cliente('Pedro', 6000);
console.log(pedro);

// Funciones exclusivas para un nuevo cliente
Cliente.prototype.tipoCliente = function(){
    let tipo;
    if(this.saldo > 10000){
        tipo = 'GOLD';
    } else if( this.saldo > 5000){
        tipo = 'PLATINUM';
    } else{
        tipo = 'Normal';
    }

    return tipo;
}


Cliente.prototype.nombreClienteSaldo = function(){
    return `Nombre: ${this.nombre} \nSaldo: ${this.saldo} \nTipo Cliente: ${this.tipoCliente()}`
}

Cliente.prototype.retiraSaldo = function(retira){
    if(this.saldo >= retira){
        this.saldo -= retira;
    }
}

// Constructor objeto persona

function Persona(nombre, saldo, telefono){
    /* Forma normal sin herencia de almacenar la información */
    // this.nombre = nombre;
    // this.saldo = saldo;

    /* Forma con Herencia de almacenar las propiedades que comparten ambos objetos */
    Cliente.call(this, nombre, saldo); // Se heredan this.nombre y this.saldo provenientes de Cliente (Heredando constructor cliente básicamente)
    

    this.telefono = telefono; // Propiedad única del objeto Persona    
}

/* Si se quiere heredar las funciones asociadas al objeto Cliente, se debe escribir el siguiente código antes de instanciar un una variable asociada al objeto persona */

// Funciones exclusivas heredadas de Cliente a Persona
Persona.prototype = Object.create( Cliente.prototype ); // Object.create() copia el prototype de un objeto a otro
Persona.prototype.constructor = Cliente; // Se vuelve a definir el constructor porque se pierde al copiar el prototype del otro objeto

Persona.prototype.mostrarTelefono = function(){
    return `El telefono de ${this.nombre} es ${this.telefono}`
}

// Instanciar personas

const pedrito = new Persona('Pedro Augusto', 5000, 9986532);
console.log(pedrito);

// Llamado de las funciones
console.log(pedrito.nombreClienteSaldo());
console.log(pedrito.mostrarTelefono());
// console.log(pedro.mostrarTelefono()); // Las funciones de Persona no se heredan a Cliente
```

### Programación Orientada a Objetos en JS

#### Definiendo e Instanciando una clase

Para definir una clase, se puede hacer mediante declaración o expresión, siendo la primera la más popular.

```js
// Class Declaration
class Cliente{
    // cuerpo de la clase...
}

// Class Expression
const Cliente2 = class{
    // cuerpo de la clase...
}
```

Para instanciar una clase, hay que definir una variable y asiganarle la nueva clase de la siguiente manera.

```js
// Instanciar la clase 
const pedro = new Cliente(  ); // Objeto vacío
console.log(pedro);
```

Para que el objeto deje de ser vacío, hay que definir el constructor en la clase utilizando la palabra reservada `constructor` y definiendo los valores que se utilizarán para instanciar la clase.

```js
class Cliente{
    constructor( nombre, saldo ){
        this.nombre = nombre;
        this.saldo = saldo;
    }
}
```

Con lo anteior, al momento de instanciar, se entregan los valores requeridos por el constructor.

```js
const pedro = new Cliente('Pedro', 500);
console.log(pedro);
```

#### Métodos y Métodos estaticos en las clases

Al igual que antes se utilizaban los _protoypes_ para asiganr funciones exclusivas a un objeto, en las clases también se puede hacer lo mismo definiendo funciones dentro de la clase, las cuales toman el nombre de _métodos_.

```js
class Cliente{
    constructor( nombre, saldo ){
        this.nombre = nombre;
        this.saldo = saldo;
    }

    // Definición de un método
    mostrarInformacion(){
        return `El cliente ${this.nombre} tiene un saldo de ${this.saldo}`;
    }
}
```

Los métodos se utilizan luego de instanciar la clase, como se muestra en el siguiente ejemplo.

```js
// Instanciar la clase 
const pedro = new Cliente('Pedro', 500);

// Llamado de un método de la clase Cliente
console.log(pedro.mostrarInformacion());
```

Cabe mencionar que existen los métodos estaticos, los cuales no necesitan de instanciar la clase para ser utilizado.

```js
class Cliente{
    constructor( nombre, saldo ){
        this.nombre = nombre;
        this.saldo = saldo;
    }

    // Propiedad estatica (no requiere una instancia para utilizarla)
    // Es una propiedad que pertenece más a la clase que a un objeto
    static bienvenida(){
        return `No necesita instancia para ser utilizada`;
    }
}
```

Este tipo de métodos no pueden ser utilizados con un objeto instanciado.

```js
// console.log(pedro.bienvenida()); // Da un error
console.log(Cliente.bienvenida());
```

#### Heredar una clase

Para que un objeto **herede** los atributos y métodos de otro objeto, en su declaración, luego del nombre, hay que agregar la palabra _extends_ seguida de la clase desde la cual se heredarán los atributos y los métodos.

```js
class Empresa extends Cliente{} // Hereda todas las propiedades y métodos de la clase padre Cliente
```

Si en la clase hijo (clase Empresa en el ejemplo anteiror) se quieren asignar nuevos atributos, hay que reescribir el constructor de la clase, teniendo en cuenta que los atributos de la clase padre no se definirán con el clásico `this.atributo = nombreAtributo`, sino que se utilizará la función `super()`, la cual recibirá como parámetros los atributos heredados desde el padre.

```js
class Empresa extends Cliente{
    constructor(nombre, saldo, telefono, categoria){
        super( nombre, saldo ); // Equivale al this.nombre y this.saldo definidos en la clase Padre
        this.telefono = telefono;
        this.categoria = categoria;
    }
}
```

Por último, si se quiere reescribir un método en la clase hijo, hay que vovler a utilizar el mismo nombre que tiene en la clase padre.

```js
class Empresa extends Cliente{
    constructor(nombre, saldo, telefono, categoria){
        super( nombre, saldo ); // Equivale al this.nombre y this.saldo definidos en la clase Padre
        this.telefono = telefono;
        this.categoria = categoria;
    }

    // Si se define un método con el mismo nombre que uno en la clase padre, este se reescribe en el hijo
    static bienvenida(){
        return `No necesita instancia de la clase Empresa para ser utilizada`;
    }
}
```

#### Propiedades Privadas en JS

Es una característica muy reciente, que no es soportada en todos los navegadores para la fecha de estas anotaciones (2020-2021).
Las propiedades privadas son aquellas que sólo pueden ser manejadas dentro de la clase, ya sea utilizando un _set_ o un _get_, desde un constructor o desde algún otro método que se encuentre dentro de la clase. Para definir un atributo privado, se debe utilizar un numeral seguido del nombre de la variable `#atributoPrivado`, lo anterior se posiciona antes del constructor y para utilizarlo en la clase, hay que poner el signo de gato junto con el nombre de la propiedad `this.#atributoPrivado`.

```js
class Cliente{
    #nombre;

    constructor( nombre, saldo ){
        this.#nombre = nombre;
        this.saldo = saldo;
    }

    // Cambiar el nombre de la persona
    set nuevoNombre(nombre){
        this.#nombre = nombre;
    }

    // Retorna el nombre de la persona
    get obtenerNombre(){
        return this.#nombre;
    }

    // Definición de un método
    mostrarInformacion(){
        return `El cliente ${this.#nombre} tiene un saldo de ${this.saldo}`;
    }

    // Propiedad estatica (no requiere una instancia para utilizarla)
    // Es una propiedad que pertenece más a la clase que a un objeto
    static bienvenida(){
        return `No necesita instancia para ser utilizada`;
    }
}

// Instanciar la clase 
const pedro = new Cliente('Pedro', 500);
console.log(pedro);
// console.log(pedro.#nombre); // No se puede acceder a la propiedad desde fuera de la clase
console.log(pedro.mostrarInformacion()); // El método si puede utilizar el atributo
pedro.nuevoNombre = "Pedrito"; // Cambia el valor del nombre
console.log(pedro.obtenerNombre); // Muestra el valor del nombre
```

### Sets, Maps y Symbols

#### Sets y sus Caracteristicas

Permite la creación de una lista sin duplicados, además que cuando manejan un gran numero de datos, tienede a ser manejado más rápido que un arreglo.

Algunos métodos pertenecientes a los arreglos también se pueden utilizar en los _sets_ pero no todos.

Los sets son sólo valores, no llave-valores como los objetos.

Diferencian entre mayusuculas y minusculas.

- Forma de inicializar un _Set_ y agregar elementos.
```js
// Declarar un Set
const carrito = new Set();

// Agregar elementos al Set con el set method .add()
carrito.add('Camisa');
carrito.add('Disco #1');
carrito.add('Disco #2');
carrito.add('Disco #3');

// Intentar agregar un elemento que ya existe
// carrito.add('Camisa'); // No lo agrega

// camisa es distinto de Camisa
carrito.add('camisa'); // Lo agrega
console.log(carrito);
//console.log(carrito.add('camisa')); // No retorna nada
```

- Eliminar un elemento del _Set_ o todos los elementos.

```js
// Eliminar un elemento con .delete()
//carrito.delete('camisa');
console.log(carrito);
console.log(carrito.delete('camisa')); // retorna true
console.log(carrito.delete('camisa')); // retorna false porque ya fue eliminado

// Eliminar todos los elementos del Set
// carrito.clear();
// console.log(carrito);
```

- Forma de saber el largo de un _Set_ y si contiene un elemento en especifico.

```js
// Largo de un set utilizando el set method .size
console.log(carrito.size);

// Saber si un elemento se encuentra dentro del Set con .has()
console.log(carrito.has('Camisa')); // true
```

- Iteración de un _Set_ con el método `.forEach()`. Los

```js
// Iteración en los Sets
carrito.forEach( (producto, index, pertenece) => {
    console.log(producto);
    console.log(index); // Mismo elemento que producto ya que los sets sólo almacenan valores sin llave
    console.log(pertenece); // Muestra el set completo al que el elemento pertenece
});
```

- Ejemplo de uso de un _Set_

```js
// Del siguiente arreglo, eliminar los duplicados
const numeros = [10,20,30,40,50,10,20];
console.log(numeros);
const numerosNoDuplicados = new Set(numeros);
console.log(numerosNoDuplicados);
```

#### Qué es un WeakSet y en que se diferencia de una Set

A diferencia del _Set_ el cual permite almacenar todo tipo de variables, los _WeakSet_ **sólo permiten el almacenamiento de objetos**.

A diferencia de los _Set_, un _WeakSet_ no tiene la propiedad _.size_, por lo cual no se puede conocer la extensión del _WeakSet_.

La última diferencia es que los _WeakSet_ no son iterables como si lo son los _Set_.

```js
// WeakSet

const weakSet = new WeakSet();

const cliente = {
    nombre: 'Pedro',
    saldo: 100
};

// Agrega objeto al weakSet con el método .add()
weakSet.add(cliente); 

// const nombre = 'Juan';
// weakSet.add(nombre); // Marca un error al no ser un objeto lo que se quiere agregar

console.log(weakSet);

// Saber si contiene un objeto con el método .has()
console.log(weakSet.has(cliente)); // Retorna un true

// Eliminar un objeto con el método .delete()
console.log(weakSet.delete(cliente)); // Retorna true
console.log(weakSet);
```

#### Maps y sus caracteristicas

Son listas ordenadas en llave y valor, los cuales pueden ser cualquier tipo de dato.
Tienen mejor perfomance que un obejto (en especial cuando son más grandes) y son especialmente diseñados para agregar o quitar elementos, o también para recorrelos.

En el siguiente bloque de código se puede observar todo lo que se peude hacer con los _Maps_

```js
// Inicializar Map vacío
const cliente = new Map();

// Inicializar Map con elementos
// Se puede seguir utilizando el método set para agregar valores
const paciente = new Map([['nombre','Paciente'],['cuarto','no definido']]);
console.log(paciente);

// Agregar un elemento utilizando el método .set(llave, valor)

cliente.set('nombre','Karen');
cliente.set('tipo','Premium');
cliente.set('saldo', 3000);
cliente.set(true, true);
cliente.set([0], false);

console.log(cliente);

// Reescribir un valor utilzando su llave y el método set(llave,nuevoValor)
cliente.set('tipo','Gold');

// Obtener el tamaño del Map con la propiedad .size
console.log(cliente.size);

// Saber si una llave se encuentra en el Map
console.log(cliente.has('tipo'));

// Obtener un valor mediante su llave con el método .get(llave)
console.log(cliente.get('tipo'));

// Eliminar elementos usando su llave con el método .delete(llave)
console.log(cliente.delete('tipo')); // Retorna true
console.log(cliente.has('tipo')); // false
console.log(cliente); // Ya no se encuentra el elemento

// Limpiar el Map con el método clear()
cliente.clear();
console.log(cliente);

// Iteración en los Maps
paciente.forEach(( dato, index ) => {
    console.log(`La llave es: ${index} y el valor es ${dato}`);
});
```

#### ¿Qué son los WeakMaps?

Sirve para ocultar cierta información no tan sensible.
No son iterables.
No tienen la porpiedad _.size_, por lo cual no se puede saber su extensión.
Sólo aceptan obejetos como llave.

En el siguiente bloque de código se puede observar todo lo que se peude hacer con los _WeakMaps_

```js
// WeakMaps

const producto = {
    idPRoducto : 10
}

// Inicializar un WeakMap
const weakMap = new WeakMap();

// Agregar elemento a un WeakMap utilizando el método .set()
weakMap.set(producto, 'Monitor');
// weakMap.set('Producto', 'Televisión'); // Sólo acepta objetos en su llave, de lo contrario retorna un error en consola
console.log(weakMap); // El objeto producto queda como la llave de Monitor, y las propiedades del objeto quedan inaccesibles mediante el uso del método .get()

// .has() para saber si contiene un elemento
console.log(weakMap.has(producto));
// Obtener un elemento utilizando el método .get()
console.log(weakMap.get(producto));

// Eliminar un elemento utilizando el método .delete()
// console.log(weakMap.delete(producto));
```

#### Symbols y sus Caracteristicas

- Permite la creación de propiedades únicas e irrepetibles. A diferencia de _Set_ o _Map_, los _Symbols_ no requieren la palabra reservada `new` para ser creados.

```js
// Inicializar un Symbol
const sym = Symbol('1');
const sym2 = Symbol('1');
```

- **Ningún Symbol es igual a otro Symbol**

```js
// En teoría deberían ser iguales, ya que su valor y tipo de dato son "iguales"
if(sym === sym2) {
    console.log(`Son iguales`);
} else {
    console.log(`No son iguales`); // Retorna esto
}
```

- Pueden ser utilizados como propiedades de un objeto mediante la sitaxis de corchetes.

```js
const nombre = Symbol();
const apellido = Symbol();

const persona = {};

// Agregar nombre y apellido como llaves del objeto
// Las propiedad que utilizan Symbol no son iterables
persona[nombre] = 'Pedro';
persona[apellido] = 'Piedra';
persona.tipoCliente = 'Premium';
persona.saldo = 500;

/* En la consola saldrá que tanto el valor asignado al nombre y el valor asignado
al apellido son Symbol() */
console.log(persona);

// Para acceder al nombre y al apellido del objeto hay que ocupar la sintaxis de corchete, no la de puntos.
console.log(`La persona se llama ${persona[nombre]} ${persona[apellido]} y su saldo es de ${persona.saldo}`);
```

- **Los Symbol no son iterables**

```js
// Al iterar el objeto, las propiedades del tipo Symbol quedan privadas y no accesibles
for( propiedad in persona){
    console.log(propiedad); // tipoCliente, saldo
}
```

- Al crear un _Symbol_, se puede agregar una descripción de él, la cual se entrega como _String_ sus parentesis del constructor.

```js
// Definir una descripción del Symbol
const cliente = {};
const nombreCliente = Symbol('Nombre del Cliente');

cliente[nombreCliente] = 'Paquito';
console.log(cliente); // En la consola se podrá observar una descripción perteneciente a la propiedad Symbol del objeto
console.log(cliente[nombreCliente]); // Acceder al valor de la propiedad
console.log(nombreCliente); // Muestra solamente la descripción del Symbol
```

#### Crear un iterador porpio

```js
function crearIterador(arreglo){
    let i = 0 // Contador

    return {
        siguiente: () => {
            const fin = (i >= arreglo.length); // Establece el fin del arreglo
            const valor = !fin ? arreglo[i++] : undefined ; // Almacena el valor iterado si se cumple una condición

            return {
                fin,
                valor
            }
        }
    }
}

const carrito = ['Producto1','Producto2','Producto3'];

// Utilizar el iterador
const recorrerArreglo = crearIterador(carrito);

// Descomentar uno a uno para ir viendo la iteración
// console.log(recorrerArreglo.siguiente()); // Muestra un elemento iterado [0] 
// console.log(recorrerArreglo.siguiente()); // Muestra un elemento iterado [1] 
// console.log(recorrerArreglo.siguiente()); // Muestra un elemento iterado [2]
// console.log(recorrerArreglo.siguiente()); // Muestra undefined
```

#### Generadores en JS

Un generador es una función que retorna un iterador. Como peculiaridad tiene que antes del nombre de la función hay que agregar un asterisco para que JS lo reconozca como un _Generador_, a lo anterior se le suma el uso de la palabra reservada `yield` que hace alusión a los valores a iterar. 

```js
function *crearGenerador(){
    // Valores a iterar
    yield 1;
    yield 'Pedro';
    yield 3+3;
    yield true;
}

// Acceder a los valores yield
const iterador = crearGenerador();

// El iterador se encuentra suspended hasta que se utiliza el método next() y luego vuelve a suspended
console.log(iterador); // crearGenerador {<suspended>}
console.log(iterador.next()); // 1 (Primer valor)
console.log(iterador); // Vuelve a crearGenerador {<suspended>}
console.log(iterador.next()); // Pedro (Segundo valor)
console.log(iterador.next().value); // Valor de la suma de 3+3 (Tercer valor)
console.log(iterador.next().done); // false debido a que aún no alcanza no llega al final (Cuarto valor)
console.log(iterador.next()); // { value: undefined, done: true }
console.log(iterador); // crearGenerador {<closed>} Termino de iterar
```

El siguiente bloque de código muestra un ejemplo un poco más complejo del uso de _Generador_

```js
// Generador para un carrito de compras (Elementos dinamicos)

function *generarCarrito( carrito ){
    for(let i = 0; i < carrito.length; i++){
        yield carrito[i];
    }
}

const carrito = ['Producto 1', 'Producto 2', 'Producto 3'];
const iterador = generarCarrito(carrito);
console.log(iterador.next()); // Primer elemento
```

#### Otros Iteradores en JS

```js
// Variables iterables
const ciudades = ['Londres', 'New York', 'Madrid', 'Paris'];
const ordenes = new Set([123, 231, 131, 102]);
const datos = new Map();

datos.set('nombre', 'Pedro');
datos.set('profesion', 'Desarrollador Web');
```

##### Values Iterator

Entrega sólo los valores al momento de iterar.

```js
// Obtener el valor iterando sobre .values() 

for( let value of ciudades.values()){
    console.log(value); 
}


for( let value of ordenes.values()){
    console.log(value); 
}

for( let value of datos.values()){
    console.log(value); 
}

```

#### Keys Iterator

Entrega sólo las llaves de los elementos, o sea, indices en arreglos, la llave en los _Map_ y el mismo valor en un _Set_.

```js
// Obtener la llave iterando sobre .keys() 

for( let key of ciudades.keys()){
    console.log(key); // indices
}


for( let key of ordenes.keys()){
    console.log(key); // el mismo valor
}

for( let key of datos.keys()){
    console.log(key); // las llaves
}
```


##### Entries Iterator

Entrega tanto como llave y valor al momento de iterar.

```js
// Obtener llave y valor iterando sobre .entries() 

for( let entry of ciudades.entries()){
    console.log(entry); // Muestra su posición y valor
}


for( let entry of ordenes.entries()){
    console.log(entry); // Llave y valor son el mismo resultado
}

for( let entry of datos.entries()){
    console.log(entry); // Muestra llave y valor
}
```

##### Default

Cada uno de los elementos iterables (arreglo, set, map) tiene un iterador por default y dependiendo del tipo de dato, el resultado será distinto.

```js
// Default

for( let ciudad of ciudades ){
    console.log(ciudad); // los valores
}

for(let orden of ordenes){
    console.log(orden); // los valores
}

for(let dato of datos){
    console.log(dato); // arreglo de llave valor
}
```

### Módulos en Javascript

#### Básicos de los módulos en ES6

Una primera opción para modularizar un código, es utilizar los _IIFE_, los cuales nos permiterá evitar que otros archivos de js utilicen por accidente elementos definidos en los otros archivos, dando prioridad a la función _IIFE_ definida en un archivo.

```js
( function(){
    console.log('Desde un IIFE');
    const nombreCliente = 'Pedro'; // No puede ser accedida fuera de la función 
})();
```

Lo anterior puede ser una solución inicial a la modularización dle código, sin embargo existe una mejor opción que es la _Importación y Exportación_ de código entre archivos.

##### Export

`export` es una palabra reservada que sirve para indicar código que se quiere exportar desde el archivo en donde está escirto para ser utilizado en otros archivos.

```js
// En cliente.js
export const nombreCliente = 'Juan';
```

A veces, se puede requerir la utilización del tipo _module_ en la etiqueta script del HTML en donde se invoca al archivo .js con el código a exportar.

```html
<script src="js/cliente.js" type="module"></script>
```

Sin embargo, si existen muchos archivos, no es necesario llamarlos al HTML, sólo hay que identificar con el `type="module"` al archivo donde se importarán los códigos de otros archivos.

##### Import

`import` es una palabra reservada que se utiliza para indicar la importación de código desde otro archivo.

Es necesario indicar en el HTML que el archivo al cual se le importará código es un modulo utilizando la etiqueta `type="module"`.

```html
<script src="js/app.js" type='module'></script>
```

```js
// En app.js
import {nombreCliente} from './cliente.js' 

console.log(nombreCliente);
```

#### Exportar e Importar funciones

Al igual que con las variables, se pueden exportar e importar funciones creadas en otro archivo para ser utilizadas en otros archivos.

```js
// En cliente.js
export const nombreCliente = 'Juan';
export const ahorro = 200;

export function mostrarInformacionCliente(nombreCliente, ahorro) {
    return `El nombre del cliente es ${nombreCliente} y su ahorro es de ${ahorro}`;
}

export function tieneSaldo(ahorro){
    if(ahorro > 0){
        return `Tiene saldo y es de ${ahorro}`
    }

    return `No tiene saldo`
}
```

```js
// En app.js
import { nombreCliente, ahorro, mostrarInformacionCliente, tieneSaldo } from './cliente.js' 

console.log(mostrarInformacionCliente(nombreCliente, ahorro));

console.log(tieneSaldo(ahorro));
```

#### Exportar e Importar clases

Similar a las funciones, las clases se exportan de la misma forma. Se definen en un archivo y antes de su definición se utiliza la palabra reservada `export`, luego en el archivo que se quiera utilizar se utiliza `import`, seguido de unas llaves que contendrán los nombres de las clases a importar, seguido de un from con la ruta del arhcivo desde donde se están importando las clases.

```js
// En cliente.js

export class Cliente{
    constructor(nombreCliente, ahorro){
        this.nombreCliente = nombreCliente;
        this.ahorro = ahorro;
    }

    mostrarInformacion(){
        console.log(`El nombre del cliente es ${this.nombreCliente} y su ahorro es de ${this.ahorro}`);
    }
}
```

```js
// En app.js
import { nombreCliente, ahorro, Cliente } from './cliente.js' 

const cliente = new Cliente(nombreCliente, ahorro);
console.log(cliente);

cliente.mostrarInformacion();
```

#### Heredar una clase que está siendo importada

Al igual que con la herencia que se ha visto con anterioridad, se pueden importar clases a un archivo y en ese archivo se pueden heredar las propiedades y métodos de la clase importada a una nueva clase que se está escribiendo en aquel archivo y a su vez, se puede exportar esa nueva clase heredada para ser utilizada en otro archivo.

```js
// En cliente.js
export class Cliente{
    constructor(nombreCliente, ahorro){
        this.nombreCliente = nombreCliente;
        this.ahorro = ahorro;
    }

    mostrarInformacion(){
        console.log(`El nombre del cliente es ${this.nombreCliente} y su ahorro es de ${this.ahorro}`);
    }
}
```

```js
// En empresa.js
import { Cliente } from './cliente.js'

export class Empresa extends Cliente {
    constructor(nombre, ahorro, categoria){
        super(nombre, ahorro);
        this.categoria = categoria;
    }

    mostrarInformacion(){
        console.log(`El nombre del cliente es ${this.nombreCliente} tiene un ahorro de ${this.ahorro} y su categoría es de ${this.categoria}`);
    }
}
```

```js
// En app.js
import { Empresa } from './empresa.js' // Se recomienda siempre dejar los imports en la parte superior

const empresa = new Empresa('Pepsi', 5000, 'Alimentos');
console.log(empresa);
empresa.mostrarInformacion();
```

#### Export Default y alias a los imports

Hasta ahora todos los imports que se han hecho, han sido delimitados por un par de _llaves_, lo anterior se debe a que ninguno de los exports realizados llevaba la palabra reservada `default` entre la palabra `export` y el nombre de la función, clase o variable. Los elementos exportados con la palabra `default`, **deben ser importados fuera de las llaves**. Además es muy importante recalcar que **no se pueden tener más de un export default por archivo**

```js
// En cliente.js
export default function nuevaFuncion(){
    console.log('Este es el export default');
}
```

```js
// En app.js
import nuevaFuncion, { nombreCliente, ahorro, mostrarInformacionCliente, tieneSaldo, Cliente } from './cliente.js'

nuevaFuncion();
```

También, se pueden importar los códigos con un alias. En el caso de los `export default` al existir sólo uno, se puede importar con cualquier nombre que uno quiera (no es recomendable), para los demás import, luego de su nombre se pone la palabra reservada `as` y seguido se pone el alias con el que se quiere llamar a ese import, de esta forma a lo largo del código escrito en aquel archivo, se utilizará el alias cada vez que se quiera utilizar el import.

```js
// En cliente.js
export const nombreCliente = 'Juan';
export const ahorro = 200;
```

```js
// En app.js
import { nombreCliente as nombre, ahorro as saldo } from './cliente.js'
console.log(nombre);
console.log(saldo);
```

### IndexedDB - Una base de datos real en JavaScript

#### Introducción a IndexedDB

- Es una API de JS que se utiliza para almacenar grandes cantidades de datos estructurados. 
- Puede almacenar strings, booleans, algunso archivos y cualquier tipo de dato soportado por Javascript. 
- No tiene "limites" conocidos, sin embargo, cuando se quiere almacenar algo de más de 50 mb, preguntará por permisos.
- Es soportada por todas las últimas versiones de los navegadores.

_IndexedDB_ es diferente a _LocalStorage_, esta última es una buena solución para almacenar poca informcación (como un carrito de compras abandonado o un JSON Wen Token). En cambio, _IndexedDB_ es una base de datos completa, sin embargo, hay que tener en cuenta que **estos datos siguen siendo visibles para cualquiera** (ya que se ejecuta en el navegador) por lo que no es recomendable almacenar passwords o tarjetas de crédito.

#### Creando la base de datos

- Para crear la base de datos, se utiliza el método `window.indexedDB.open('nombre', version)`.

- Sumado a la creación existen algunos métodos que permiten saber si hubo un error al crearla, si se creo correctamente y otro que sirve al momento de generar las columnas de la base de datos. Todo lo anterior, sumado a la creación de la base de datos se puede observar en el siguiente bloque de código.

```js
document.addEventListener('DOMContentLoaded', () => {
    crmDB();
});

function crmDB() {
    // Crear base de datos v1.0
    let crmDB = window.indexedDB.open('crm', 1);

    // Si hay un error
    crmDB.onerror = function () {
        console.log('Hubo un error a la hora de crear la BDD')
    }

    // Si se creo bien
    crmDB.onsuccess = function () {
        console.log('Bases de datos creada exitosamente');
    }
    // Configuración de la bdd
    crmDB.onupgradeneeded = function () {
        console.log('Este método se ejecuta una sola vez'); // Al ser creada la base de datos
    }
}
```

#### Creando tablas

Antes que nada, la creación de las columnas y tablas, hay que dejar en claro que todo el código a utilizar debe colocarse en el método `.onupgradeneeded`, en la función anonima que se le asigna, como paramatro se le asigna un evento (`e`), del cual la propiedad `e.target.result` será la base de datos.

```js
crmDB.onupgradeneeded = function (e) {
        const db = e.target.result;
    }
```

Con lo anterior realizado, hay que definir el `objectStore`, que será igual al método `db.createObjectStore('nombre-bdd', { objeto de configuración });`.

```js
crmDB.onupgradeneeded = function (e) {

        // Configuración inicial
        const db = e.target.result;

        const objectStore = db.createObjectStore('crm', {
            keyPath: 'crm', // Referencia con la cual consultar el elemento
            autoIncrement: true // Incrementa automaticamente el id de los registros
        });

    }
```

Finalmente, con lo anterior definido, ya se puede comenzar con la creación de columnas para la base de datos utilizando el método `objectStore.createIndex( 'nombre-columna', 'keypath', { objeto de configuración } )`

```js
    // Configuración de la bdd
    crmDB.onupgradeneeded = function (e) {
        
        // Configuración inicial
        const db = e.target.result;

        const objectStore = db.createObjectStore('crm', {
            keyPath: 'crm',
            autoIncrement: true // Incrementa automaticamente el id de los registros
        });

        // Definir las columnas
        objectStore.createIndex('nombre', 'nombre', {unique: false}); // Columna de nombres que pueden repetirse
        objectStore.createIndex('email', 'email', {unique: true}); // Columna de emails que no pueden repetirse
        objectStore.createIndex('telefono', 'telefono', {unique: false}); // Columna de telefonos que pueden repetirse

        console.log('Columnas creadas correctamente');
    }
```

Hay que recordar que si con anterioridad creaste la base de datos sin la configuración inicial, puede eliminarla y volver a correr el código para que el método con las funciones se ejecute correspondiente.

#### Insertando registros a las BDD

El manejo de la información en la base de datos, se maneja en base a transacciones, como las que se hacen en un cajero en el cual antes de poder sacar cieta cantidad de dinero, se debe comprobar si el cliente tiene un saldo igual o superior al monto que quiere retirar.

El código final que incluye el setup inicial más el insertado de registros es el siguiente:

```js
let DB; // Es equivalente a e.target.result pero de forma global

document.addEventListener('DOMContentLoaded', () => {
    crmDB();

    // Luego de 5 segundos llama a la función crearCliente()
    setTimeout(() => {
        crearCliente(); // Inserta un registro en la base de datos
    }, 5000);
});

function crmDB() {
    // Crear base de datos v1.0
    let crmDB = window.indexedDB.open('crm', 1);

    // Si hay un error
    crmDB.onerror = function () {
        console.log('Hubo un error a la hora de crear la BDD')
    }

    // Si se creo bien
    crmDB.onsuccess = function () {
        console.log('Bases de datos creada exitosamente');

        DB = crmDB.result; // Asigna la base de datos creada a DB
    }
    // Configuración de la bdd
    crmDB.onupgradeneeded = function (e) {
        
        // Configuración inicial
        const db = e.target.result;

        const objectStore = db.createObjectStore('crm', {
            keyPath: 'crm',
            autoIncrement: true // Incrementa automaticamente el id de los registros
        });

        // Definir las columnas
        objectStore.createIndex('nombre', 'nombre', {unique: false}); // Columna de nombres que pueden repetirse
        objectStore.createIndex('email', 'email', {unique: true}); // Columna de emails que no pueden repetirse
        objectStore.createIndex('telefono', 'telefono', {unique: false}); // Columna de telefonos que pueden repetirse

        console.log('Columnas creadas correctamente');
    }
}

function crearCliente(){
    let transaction = DB.transaction(['crm'], 'readwrite'); // Donde se hará la transacción y de que tipo será (en este caso es lectura/escritura)

    // Muestra un mensaje si la transacción fue realizada existosamente
    transaction.oncomplete = function(){
        console.log('Transacción completada');
    }
    // Muestra un mensaje si la transacción no fue realizada    
    transaction.onerror = function(){
        console.log('Transacción erronea')
    }

    const objectStore = transaction.objectStore('crm'); // El objeto a almacenar 

    // El registro que se almacenará
    const nuevoCliente = {
        telefono: 789654321,
        nombre: 'Pedro',
        email: 'correo@correo.com'
    };

    const peticion = objectStore.add(nuevoCliente);  // Petición de almacenamiento en el objectStore
    console.log(peticion); // Se comprueba en consola lo realizado
}
```

### Promises, Callbacks y Programación Asincrona en JS

#### Ejemplo de Callbacks

_Callbacks_ hace referencia a la ejecución de una función luego de que se mande a llamar otra función.

```js
const paises = ['Francia', 'España', 'Portugal', 'Australia', 'Inglaterra'];

function nuevoPais(pais, callback) {
    setTimeout(() => {
        paises.push(pais);
        callback(); // Hace referencia a una función que se entrega como argumento
    }, 2000);
}

function mostrarPaises(){
    setTimeout(() => {
        paises.forEach( pais => {
            console.log(pais);
        });
    }, 2000);
}

nuevoPais('Alemania', mostrarPaises); // Añade el país y luego llama a mostrarPaises
```

El uso de muchos _callback_ puede provocar lo que se conoce como _Callback Hell_.

#### El muy exagerado Callback Hell

Se conoce como _Callback Hell_ al constante llamado de callbacks dentro de una función, lo que hace que esta sea más dificil de leer, de mantener y de mejorar.

```js
const paises = [];

function nuevoPais(pais, callback){
    paises.push(pais);
    console.log(`Pais ${pais} agregado correctamente`);
    callback();
}

function mostrarPaises(){
    console.log(paises);
}

function iniciarCallbackHell(){
    setTimeout(() => {
        nuevoPais('Alemania', mostrarPaises);

        setTimeout(() => {
            nuevoPais('Francia', mostrarPaises);
            
            setTimeout(() => {
                nuevoPais('Inglaterra', mostrarPaises);
            }, 3000);

        }, 3000);

    }, 3000);
}

iniciarCallbackHell();
```

#### Creando un Promise y .then y .catch

```js
/* resolve es cuando se ejecuta el promise de manera correcta, mientras que reject es
cuando existe un problema */
const aplicarDescuento = new Promise( (resolve, reject) => {
    const descuento = false;

    if(descuento) {
        resolve('Descuento aplicado');
    } else{
        reject('No se pudo aplicar el descuento');
    }
} );

// Utilización del Promise

/* Tienen 3 posibles valores los Promises 
fulfilled - El promise se cumplió 
rejected - El promise no se cumplió
pending - No se ha cumplido y tampoco ha sido rechazado
*/

/* Se lee como "Vamos a utilizar aplicar descuento entonces (.then) se ejecuta algo,
si falla, se atrapa (.catch) el error" */
aplicarDescuento
    .then( resultado => {
        console.log(resultado);
    })
    .catch( error => {
        console.log(error);
    })
```

#### De Callback Hell a Promises

```js
const paises = [];

const nuevoPais = pais =>  new Promise((resolve) => {
    setTimeout(() => {
        paises.push(pais);
        resolve(`Pais ${pais} agregado correctamente`);
    }, 3000);
})

// El "resultado" que se imprime hace referencia lo que entrega en resolve de la promesa
nuevoPais('Alemania').then( resultado => {
        console.log(resultado);
        console.log(paises);
        return nuevoPais('Francia') // Al terminar la función llama de nuevo a la función
    })
    .then( resultado => {
        console.log(resultado);
        console.log(paises);
        return nuevoPais('Inglaterra')
    })
    .then( resultado => {
        console.log(resultado);
        console.log(paises);
    })
```

### API's en JS

```html
<!-- index.html -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
    <button type="button" id="notificar">
        Notificarme!!
    </button>

    <button type="button" id="verNotificacion">
        Ver Notificación
    </button>

    <br><br><br>

    <button type="button" id="abrir-pantalla-completa">
        Full Screen
    </button>

    <button type="button" id="salir-pantalla-completa">
        Salir de Full Screen
    </button>

    <br><br><br>

    <button type="button" id="microfono">
        Speech Recognition API
    </button>

    <div id="salida" class="ocultar"></div>

    <script src="js/01-app.js"></script>
    <script src="js/03-app.js"></script>
    <script src="js/04-app.js"></script>
    <script src="js/05-app.js"></script>
    <script src="js/06-app.js"></script>

</body>
</html>
```

```html
<!-- viaje.html utilizado para el ejemplo de 02-app.js Intersection Observer -->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <meta http-equiv="X-UA-Compatible" content="ie=edge">
    <title>MiViaje.com</title>
    <link rel="stylesheet" href="https://necolas.github.io/normalize.css/8.0.0/normalize.css">
    <link href="https://fonts.googleapis.com/css?family=Lato:400,700,900" rel="stylesheet">
    <link rel="stylesheet" href="css/fontawesome-all.min.css">
    <link rel="stylesheet" href="css/styles.css">
</head>
<body>

    <div class="hero">
        <header class="header contenedor">
            <div class="logo">
                <img src="img/logo.png">
            </div>
            <nav class="navegacion">
                <a href="#">Vender</a>
                <a href="#">Ayuda</a>
                <a href="#">Registro</a>
                <a href="#">Iniciar Sesión</a>
            </nav>
        </header>

        <div class="contenido-hero contenedor">
            <h1 id="formulario">Encuentra <span> hospedaje  </span>para tus próximas vacaciones</h1>

            <form action="/buscador" method="POST" class="formulario formulario-buscar" id="formulario" >
                <input type="text" name="busqueda" class="busqueda" placeholder="New York, Londres, Roma, Guadalajara">
                <input type="submit" value="Buscar" id="btn-submit">
            </form>
        </div>
    </div> <!--.hero-->

    <main class="contenido contenedor">
        <section class="hacer">
            <h2>Que Hacer</h2>
            <div class="contenedor-cards">
                    <div class="card">
                        <img src="img/hacer1.jpg">
                        <div class="info">
                            <p class="categoria concierto">concierto</p>
                            <p class="titulo">Música electrónica 2021</p>
                            <p class="precio">$1,200 por persona</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/hacer2.jpg">
                        <div class="info">
                            <p class="categoria concierto">concierto</p>
                            <p class="titulo">Rock en Los Ángeles</p>
                            <p class="precio">$300 por persona</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/hacer3.jpg">
                        <div class="info">
                            <p class="categoria clase">Clase Cocina</p>
                            <p class="titulo">Comida Española para Principiantes</p>
                            <p class="precio">$400 por persona</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/hacer4.jpg">
                        <div class="info">
                            <p class="categoria paseo">Paseo en Bici</p>
                            <p class="titulo">Paseo en las Montañas</p>
                            <p class="precio">$200 por persona</p>
                        </div>
                    </div> <!--.card-->
            </div> <!--.columnas4 cuadros-->
        </section>


        <section class="hacer">
            <h2 class="mi-viaje-plus">Presentamos Miviaje.com Plus</h2>
            <div class="contenedor-cards premium">
                <div class="info">
                    <h3>Una nueva sección de alojamientos de lujo</h3>
                    <a href="#" class="boton btn-mi-viaje">Explorar alojamientos </a>
                </div>
            </div> <!--.columnas4 cuadros-->
        </section>

        <section class="hospedaje">
            <h2>Hospedaje</h2>
            <div class="contenedor-cards">
                    <div class="card">
                        <img src="img/hospedaje1.jpg">
                        <div class="info">
                            <p class="categoria hospedaje">Casa completa - 2 camas</p>
                            <p class="titulo">Casa completa con todos los servicios y 2 recamaras</p>
                            <p class="precio">$3,200 por noche</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/hospedaje2.jpg">
                        <div class="info">
                            <p class="categoria hospedaje">1 Cuarto con 2 camas</p>
                            <p class="titulo">1 Cuarto con 2 camas y alberca </p>
                            <p class="precio">$2,200 por noche</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/hospedaje3.jpg">
                        <div class="info">
                            <p class="categoria hospedaje">Cabaña completa - 4 Camas</p>
                            <p class="titulo">Cabaña en Bosque para 6 personas</p>
                            <p class="precio">$2,500 por noche</p>
                        </div>
                    </div> <!--.card-->
            </div> <!--.columnas4 cuadros-->
        </section>

        <section class="destinos">
            <h2>Destinos Populares</h2>
            <div class="contenedor-cards">
                    <div class="card">
                        <img src="img/populares1.jpg">
                        <div class="info">
                            <p class="titulo">Austria</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/populares2.jpg">
                        <div class="info">
                            <p class="titulo">Francia</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/populares3.jpg">
                        <div class="info">
                            <p class="titulo">Grecia</p>
                        </div>
                    </div> <!--.card-->
                    <div class="card">
                        <img src="img/populares4.jpg">
                        <div class="info">
                            <p class="titulo">Inglaterra</p>
                        </div>
                    </div> <!--.card-->
            </div> <!--.columnas4 cuadros-->
        </section>

        <section class="hacer">
                <h2>Que Hacer en New York</h2>
                <div class="contenedor-cards">
                        <div class="card">
                            <img src="img/newyork1.jpg">
                            <div class="info">
                                <p class="categoria clase">Clase</p>
                                <p class="titulo">Comida Japonesa para Principiantes</p>
                                <p class="precio">$300 por persona</p>
                            </div>
                        </div> <!--.card-->
                        <div class="card">
                            <img src="img/newyork2.jpg">
                            <div class="info">
                                <p class="categoria concierto">concierto</p>
                                <p class="titulo">Festival EDM 2021</p>
                                <p class="precio">$1,200 por persona</p>
                            </div>
                        </div> <!--.card-->
                        <div class="card">
                            <img src="img/newyork3.jpg">
                            <div class="info">
                                <p class="categoria clase">Clase de Cocina</p>
                                <p class="titulo">Paella Dominicana</p>
                                <p class="precio">$200 por persona</p>
                            </div>
                        </div> <!--.card-->
                        <div class="card">
                            <img src="img/newyork4.jpg">
                            <div class="info">
                                <p class="categoria paseo">Paseos</p>
                                <p class="titulo">Paseo a Caballo</p>
                                <p class="precio">$100 por persona</p>
                            </div>
                        </div> <!--.card-->
                </div> <!--.columnas4 cuadros-->
            </section>

    </main>
    
   

    <footer id="footer" class="footer">
        <div class="contenedor">
                <div class="nav-footer">
                    <h3 class="titulo-footer">MiViaje.com</h3>
                    <nav class="menu">
                        <a href="#">Empleo</a>
                        <a href="#">Prensa</a>
                        <a href="#">Politicas</a>
                        <a href="#">Ayuda</a>
                    </nav>
                </div>

                <div class="nav-footer">
                    <h3 class="titulo-footer">Descubre MiViaje.com</h3>
                    <nav class="menu">
                        <a href="#">Confianza y Seguridad</a>
                        <a href="#">Crédito de Viajero</a>
                        <a href="#">AirBNB Citizen</a>
                        <a href="#">Viaje de negocios</a>
                    </nav>
                </div>

                <div class="nav-footer">
                    <h3 class="titulo-footer">Hospedaje</h3>
                    <nav class="menu">
                        <a href="#">Razones para Hospedar</a>
                        <a href="#">Hospitalidad</a>
                        <a href="#">Ser un anfitrión responsable</a>
                        <a href="#">Centro de la Comunidad</a>
                    </nav>
                </div>

                <div class="nav-footer">
                    <nav class="sociales">
                        <ul>
                            <li><a href="http://facebook.com" target="_blank"><span>Facebook</span></a></li>
                            <li><a href="http://twitter.com" target="_blank"><span>Twitter</span></a></li>
                            <li><a href="http://instagram.com" target="_blank"><span>Instagram</span></a></li>
                        </ul>
                    </nav>
                    <nav class="menu">
                        <a href="#">Razones para Hospedar</a>
                        <a href="#">Hospitalidad</a>
                        <a href="#">Ser un anfitrión responsable</a>
                        <a href="#">Centro de la Comunidad</a>
                    </nav>
                </div>
        </div>
    </footer>
    <a href="#footer" class="btn-flotante">Idioma y Moneda</a>

    <script src="js/02-app.js"></script>
</body>
</html>
```

#### Notification API

Para que JS entregue notificaciones al usuario, este último **debe aceptar recibir notificaciones**.
Todo lo de la snotificaciones es manejado por la _Notification API_, la cual al igual que muchas APIs actuales, funciona con promesas (_Promises_).

```js
/* 01-app.js */

const btnNotificar = document.querySelector('#notificar');

btnNotificar.addEventListener('click', () => {
    // Solicitar al usuario permiso para enviar notificaciones
    // Notification hace referencia a la API
    Notification
        .requestPermission() // Método que se encarga de desplegar la solicitud de permiso al usuario
        .then( respuesta => {
            // Una vez solicitado el permiso, se muestra en consola la respuesta a la solicitud
            console.log('La respuesta es:', respuesta); // granted = permiso otorgado
        })
});

const btnVerNotificacion = document.querySelector('#verNotificacion');

btnVerNotificacion.addEventListener('click', () => {
    // Se verifica si el permiso fue dado
    if(Notification.permission == 'granted'){
        // La notificación puede mostrar más información aparte del texto
        const notificacion = new Notification('Esta es la notificación', {
            icon: 'https://upload.wikimedia.org/wikipedia/commons/thumb/9/99/Unofficial_JavaScript_logo_2.svg/480px-Unofficial_JavaScript_logo_2.svg.png',
            body: 'Aprendiendo Notification API'
        }); // Crea una notificación que el navegador muestra al usuario

        // Al presionar en la notificacion (o en ver), redirige a un enlace
        notificacion.onclick = function(){
            // Forma de abrir una URL
            window.open('https://developer.mozilla.org/es/docs/Web/API/notification');
        }
    }
})
```

#### Intersectation Observer

Se utiliza para identificar cuando un elemento esta visible.
Se suele utilizar para dar el efecto de scroll infinito o de _lazy loading_ en alguna imagenes.
El Intersection Observer hay que utilizarlo como una clase, en la cual su constructor recibe una _Arrow Function_ que como parametro se le define un _entries_.

```js
// 02-app.js
document.addEventListener('DOMContentLoaded', () => {

    // Habilita IntersectionObserver
    const observer = new IntersectionObserver( (entries) => {
        // console.log(entries[0]); // El primer elemento es el más importante. Comenzará a tener valores cuando se defina que elemento se observará
        // Notifica siempre que se intersecte el elemento y se encuentre visible (lo importante es isIntersecting)

        if(entries[0].isIntersecting){
            console.log('El elemento se encuentra visible');
        }
    });

    // Se le indica que elemento va a observar
    observer.observe(document.querySelector('.premium'));
});
```

#### Detectar si existe conexión a internet

Se puede detectar si existe conexión mediante la utilización de objeto _window_ que tiene los Listeners de online y offline que indican si hay o no internet.

```js
// 03-app.js
// Detectar conexión de internet

window.addEventListener('online', actualizarEstado);
window.addEventListener('offline', actualizarEstado);

function actualizarEstado() {
    if(navigator.onLine){
        console.log('Estas conectado');
    } else{
        console.log('No estas conectado');
    }
}
```

#### Ejecutar pantalla completa con JS

Con Javascript se puede entrar o salir del modo pantalla completa, utilizando los métodos de `.requestFullScreen()` y `.exitFullscreen()` en el elemento que se quiere dejar en pantalla completa (el sitio, el vídeo o una imagen).

```js
// 04-app.js
// Selectores de botones
const btnFullScreen = document.querySelector('#abrir-pantalla-completa');
const btnSalirFullScreen = document.querySelector('#salir-pantalla-completa');

btnFullScreen.addEventListener('click', pantallaCompleta);
btnSalirFullScreen.addEventListener('click', salirPantallaCompleta);

function pantallaCompleta(){
    // Se quiere que todo el sitio esté en pantalla completa
    document.documentElement.requestFullscreen(); // Solicita el modo pantalla completa
    // Lo anterior sirve para otros elementos como una imagen o vídeo
}

function salirPantallaCompleta(){
    // Se selecciona el elemento que está en pantalla completa
    document.exitFullscreen(); // El elemento se saca del modo pantalla completa
}
```

#### Detectar si el usuario se encuentra viendo la página

El listener que sirve para saber si el usuario está viendo la página o no es `'visibilitychange'`.

```js
// 05-app.js
document.addEventListener('visibilitychange', () => {
    // console.log(document.visibilityState); // hidden - visible
    if(document.visibilityState === 'visible'){
        console.log('Ejecutar código para reproducir el vídeo');
    }else{
        console.log('Ejecutar código para pausar el vídeo');
    }
});
```

#### Speech API

Es una API que permite la utilización de la voz dentro de la página para transcribirlo a texto, requiere de que el usuario ceda permisos de uso del microfono.
Es una API muy nueva por lo cual a la fecha de hoy no muchos navegadores la soportan (Navegadores de Android, Chrome y Edge).

```js
// 06-app.js
const salida = document.querySelector('#salida');
const btnSpeechRecognition = document.querySelector('#microfono');

btnSpeechRecognition.addEventListener('click', ejecutarSpeechAPI);

function ejecutarSpeechAPI(){
    const SpeechRecognition = webkitSpeechRecognition;
    const recognition = new SpeechRecognition();

    // Inicia el reconocimiento
    recognition.start();

    // Cuando se ejecute recognition se ejecuta la siguiente función
    recognition.onstart = function(){
        salida.classList.remove('ocultar');
        salida.classList.add('mostrar');
        salida.textContent = 'Escuchando...';
    };

    // Cuando el usuario haya terminado de hablar
    recognition.onspeechend = function(){
        salida.textContent = 'Se detuvo la escucha...';
        recognition.stop(); // Se detiene el reconocimiento
    }

    // Lo hablado se traduce a texto
    recognition.onresult = function(e){
        // console.log(e.results[0][0]); // Confidence es que tan seguro esta la API de lo que se dijo y transcript es lo que se tradujo a texto
        const { confidence, transcript } = e.results[0][0];

        const speech = document.createElement('p');
        speech.innerHTML = `Grabado: ${transcript}`;

        const seguridad = document.createElement('p');
        seguridad.innerHTML = `Seguridad ${ parseInt( confidence * 100 )}%`
        
        salida.append(speech, seguridad);
    }
}
```

### Fetch API - Para obtener datos de otros servidores o APIs

```html
<!--index.html-->
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
    <link href="https://fonts.googleapis.com/css2?family=Carrois+Gothic+SC&display=swap" rel="stylesheet"> 
    <link rel="stylesheet" href="../assets/css/style.css">
</head>
<body>

    <div class="contenido">
        <h1>JavaScript Moderno</h1>
        <a href="http://www.codigoconjuan.com" target="_blank">codigoconjuan.com</a>
        <p>Fetch API</p>
        <p class="hashtag">#JSModernoConJuan</p>

        <div id="contenido"></div>

        <button type="button" id="cargarTxt">
            Obtener desde TXT
        </button>
        <button type="button" id="cargarJSON">
           Cargar JSON - Objeto
        </button>
        <button type="button" id="cargarJSONArray">
            Cargar JSON - Array
        </button>
        <button type="button" id="cargarAPI">
            Cargar API
        </button>
    </div>

    <script src="js/01-app.js"></script> 
    <script src="js/02-app.js"></script> 
    <script src="js/03-app.js"></script> 
    <script src="js/04-app.js"></script> 
    
</body>
</html>
```
- Información para un archivo txt

```
Informacion desde un archivo .txt
```

- Información de empleado.json

```json
{
     "id" : 1,
     "nombre" : "Juan",
     "empresa" : "Código Con Juan",
     "trabajo" : "Desarrollador Web"
}
```

- Información de empleados.json

```json
[
     {
          "id" : 1,
          "nombre" : "Juan",
          "empresa" : "Código con Juan",
          "trabajo" : "Desarrollador Web"
     },
     {
          "id" : 2,
          "nombre" : "Alejandra",
          "empresa" : "Código con Juan",
          "trabajo" : "Diseñadora"
     },
     {
          "id" : 3,
          "nombre" : "Pedro",
          "empresa" : "Código con Juan",
          "trabajo" : "Aplicaciones Móviles"
     }
]
```

#### Como utilizar FECTH API

- Fetch API sólo puede leer textos planos, no soporta _XML_.
- Fetch API es nativo de JavaScript, antes se utilizaba AJAX pero ahora es más recomendable utilizar Fetch. Al ser nativo, tanto el _resolve_ como el _rejected_ de la promesa, ya estan definidos.
- Al igual que otras API actuales, FETCH API utiliza _Promises_.
- **FETCH API sirve tanto como para obtener datos como para enviar datos**

Hay diferentes forma de utilizar Fetch API:

1. Utilizando `fetch()` y entregando como parametro la URL desde donde vendrán los datos que se quieren obtener o hacía donde se quieren enviar.

```js
fetch('url/datos.txt')
```

2. Otra forma es haciendo lo mismo que en la forma anterior pero guardando la URL en una variable la cual será entegada como parametro a `fetch()`.

```js
const url = 'url/datos.tx';
fetch(url)
```

Sin importar cual se utilice, al funcionar con _Promises_, se utiliza `.then( response => {})`, la respuesta que entrega tiene vairada información como el `status` que permite saber si la petición fue correcta. La repsuesta de la promesa de FETCH API, suele ser acompañada por los métodos `.txt()` o `.json()` que entregan en formato de texto o json la información de la respuesta. Finalmente esa respuesta con su corresondiente método transformados, se retorna para que otra promesa (`.then( datos => {...})`) maneje los datos ya en el formato deseado.

```js
// 01-app.js

const btnObtenerDesdeTXT = document.querySelector('#cargarTxt');
btnObtenerDesdeTXT.addEventListener('click', obtenerDatos);

function obtenerDatos() {
    // Una forma
    // fetch('data/datos.txt')
    
    // Segunda forma
    const url =  'data/datos.txt';
    fetch(url)
        .then( respuesta => {
            // console.log(respuesta);
            // console.log(respuesta.status); // Entrega el HTTP Response
            // console.log(respuesta.url); // Entrega la URL de respuesta
            // console.log(respuesta.type); // Entrega el tipo de consulta que se está realizando

            return respuesta.text(); // Junto a .text(), .json() son los más utilizados
        })
        .then( datos => {
            // Obtenida la información, entonces se muestran los datos
            console.log(datos);
        })
        .catch( error => console.log(error))
}
```

#### Consultar un JSON

JSON es conocido como una tecnologia de transporte, la cual tiene alta compatibilidad con JS.
Al consultar JSON y ser recibido en JS, es transformado a un objeto para su manejo en JS.

```js
// 02-app.js

// Dar click en Cargar JSON - Objeto debe descargar el contenido
// Almacenado en el archivo JSON

const btnCargarJsonObj = document.querySelector('#cargarJSON');
btnCargarJsonObj.addEventListener('click', obtenerDatos);

function obtenerDatos() {

    const url =  'data/empleado.json';
    fetch(url)
        .then( respuesta => {

            return respuesta.json();
        })
        .then( dato => {
            mostrarDatos(dato); // El console.log puede ser reemplazado por una función que muestre de otra forma la información entregada
        })
        .catch( error => console.log(error))
}

// Scripting que muestra en el HTML la información obtenida del JSON
function mostrarDatos({ empresa, id, nombre, trabajo }) {
    const contenido = document.querySelector('.contenido');
    
    const empleado = document.createElement('div');
    empleado.innerHTML = `
    <p> ID: ${id}</p>
    <p> Empleado: ${nombre}</p>
    <p> Empresa: ${empresa}</p>
    <p> Trabajo: ${trabajo}</p>
    `
    contenido.appendChild(empleado);
}
```

#### Consultar e imprimir los resultados de un Fecth (Arreglo de JSON)

Cuando se trata de un arreglo que contiene muchos objetos, se obtienen de la misma forma como si fuera uno sólo pero la respuesta ahora viene en forma de arreglo y el método `.json()` entrega un arreglo de objetos que debe ser iterado para acceder a cada uno de los elementos que trae.

```js
// 03-app.js
const btnCargarJsonArr = document.querySelector('#cargarJSONArray');
btnCargarJsonArr.addEventListener('click', obtenerDatos);

function obtenerDatos() {

    const url =  'data/empleados.json';
    fetch(url)
        .then( respuesta => respuesta.json())
        .then( datos => {
            mostrarDatos(datos);
        })
        .catch( error => console.log(error))
}

// Scripting que muestra en el HTML la información obtenida del JSON
function mostrarDatos(datos) {
    const contenido = document.querySelector('.contenido');
    datos.forEach( empleado => {
        const { id, nombre, empresa, trabajo } = empleado;
        const contenedorEmpleado = document.createElement('div');
        contenedorEmpleado.innerHTML = `
        <p> ID: ${id}</p>
        <p> Empleado: ${nombre}</p>
        <p> Empresa: ${empresa}</p>
        <p> Trabajo: ${trabajo}</p>
        `
        contenido.appendChild(contenedorEmpleado);
    });
}
```

#### Consultar e imprimir los rsultados de una API (consumir una API)

Consultar una API es igual a consultar un archivo JSON almacenado de manera local pero puede tomar un poco más de tiempo debido a que ahora lo que se consulta no se encuentra almacenado de manera local.

```js
// 04-app.js

const btnCargarAPI = document.querySelector('#cargarAPI');
btnCargarAPI.addEventListener('click', obtenerDatos);

function obtenerDatos() {

    const url = 'https://picsum.photos/list';
    fetch(url)
        .then( respuesta => respuesta.json())
        .then( datos => {
            mostrarContenido(datos);
        })
        .catch( error => console.log(error))
}

function mostrarContenido(datos) {
    const contenido = document.querySelector('.contenido');
    datos.forEach( perfil => {
        const { author, post_url } = perfil;

        const contenedorPerfil = document.createElement('div');
        contenedorPerfil.innerHTML = `
        <p> Autor: ${author}</p>
        <a href=${post_url}> Ver Imagen </a>
        `
        contenido.appendChild(contenedorPerfil);
    })
}
```

#### Extra: Crear paginación desde 0

Para crear una paginación con la información entregada desde una API, antes que nada es necesario saber:

- La **cantidad de resultados totales** que vienen en la respuesta de la API.
- Definir los elementos que se van a mostrar por cada página.

Con la información anterior ya se puede calcular la cantdiad de páginas de manera dinamica.

```js
// Ejemplo de función de soporte que calcula la cantidad de páginas de forma dinamica
function calcularPaginas( total, registrosPorPagina ){
    return parseInt( Math.ceil( total / registrosPorPagina ))
}
```

**Nota: La paginación es posible sólo si la API desde donde se consulta la información presenta la opción de paginación.**

Sabiendo los datos anterior, hay que crear el _Generador_ que será el encargado de generar los números de páginas en base los datos anteriores.

```js
// Generador que va a registrar la cantidad de elementos de acuerdo a las páginas
export function *crearPaginador(totalPaginas){
    for(let i = 1; i <= totalPaginas; i++){
        yield i;
    }
}
```

El generador anterior será el iterador que ayudará a generar tanto los números como el scripting para los botones que servirán para moverse entre páginas.

```js
function mostrarPaginador(totalPaginas) {
    
    // Limpiar la paginacion anterior
    limpiarResultadosPrevios(paginacion);

    iterador = func.crearPaginador(totalPaginas); // Uso del Generador

    // Loop infinito que se termina cuando la propiedad done es true
    while(true){
        // Destructuring del iterador.next()
        const { value, done } = iterador.next(); // Uso de los valores que entrega el iterador
        if(done) return;


        // Genera un botón por cada elemento en el generador
        const boton = document.createElement('a');
        boton.href = '#';
        boton.dataset.pagina = value;
        boton.textContent = value;
        boton.classList.add('siguiente', 'bg-yellow-400', 'px-4', 'py-1', 'mr-2', 'font-bold', 'mb-4', 'rounded');

        // Al hacer click vuelve a pedir a la API que entrega la nueva pagina con imagenes
        boton.onclick = function(){
            paginaActual = value;
            func.buscaImagenes();
        }
        
        // Añade el boton al DOM
        paginacion.appendChild(boton);
    }
}
```

Para más infomración sobre el código de la páginación, se puede visitar el siguiente repositorio de GitHub [Buscador de Imagenes con Pixebay API](https://github.com/crisfreak036/buscador-imagenes).

### Fetch API - Con otros HTTP Methods

Por default, `.fetch()` viene configurado con el método _GET_, debido a eso es se puede obtener información desde la APIs, sin embargo, `.fetch()` permite utilizar otro métodos de HTTP como lo serían _POST, PUT, PATCH, DELETE, etc_. Para realizar lo anterior, además del _endpoint_ hay que entregarle un objeto con la configuración de que es lo que se quiere hacer con `.fetch()`.

```js
// Ejemplo de Post
const url = 'endpoint de json-server por ejemplo';

const cliente = {
    nombre = 'Juan Carlos',
    email = 'correo@correo.cl',
    telefono = '985623589',
    empresa = 'Miksa'
};

fetch(  url, {
            method: 'POST', // Método a utilizar
            body: JSON.stringify( cliente ), // Lo que se quiere alamcenar en la API
            // El tipo de contenido que se manda a la API
            headers: {
                'Content-Type': 'application/json'
            }
        } );
```

```js
// Ejemplo de delete
const url = 'endpoint de json-server por ejemplo';

export const eliminarClienteAPI = ( id ) => {
    try {
        fetch( `${url}/${id}`, {
            method: 'DELETE'
        });
    } catch (error) {
        console.log(error);
    }
}
```

```js
// Ejemplo de put
const url = 'endpoint de json-server por ejemplo';
export const editarClienteAPI = async ( cliente, id ) => {
    try {
        await fetch(  `${url}/${id}`, {
            method: 'PUT',
            body: JSON.stringify( cliente ),
            headers: {
                'Content-Type': 'application/json'
            }
        } );

        window.location.href = 'index.html' // Redirige al index.html
    } catch (error) {
        console.log(error);
    }
}

/*
Cabe mencionar que se puede utilizar PATCH para modificar de forma parcial el objeto. PUT es el más popular y se encarga de modificar todo el objeto.
*/
```

### Async Await en JavaScript

#### ¿Qué es Try Catch?

En los lenguajes de programación, cuando existe un error en el código, se muestra por consola y se detiene la ejecución de lo que sigue después de la línea de código que presenta el error. Usando el bloque _Try-Catch_, se puede mostrar el error por consola y se puede ejecutar el código que sigue después del error.

```js
// Sin Try-Catch
console.log('Antes del error'); // Se ejecuta

hola(); // Arroja un error

console.log('Después del error'); // No se ejecuta
```

```js
// Con Try-Catch
console.log('Antes del bloque try-catch'); // Se ejecuta

try {
    hola(); // Da un error
} catch (error) {
    // Se puede demoniar esta parte como "Administración del error"
    console.log(error); // Se muestra el error en la consola
}

console.log('Después del bloque try-catch'); // Se ejecuta
```

Se le puede denominar _Administración del error_ a la sección catch del bloque, ya que permite observar de mejor manera que sucede en la linea de código conflictiva de la aplicación.

Esta demás decir que no se debe encerrar todo el código en un bloque  _Try-Catch_, sólo se debe utilizar en partes criticas del código como lo serían la conexión a una base de datos, consultar una API, autenticar un usuario o acciones que nos permitan que en caso de que falle, nuestra aplicación continue funcionando.

Algo que cabe mencionar es que si en el _try_ se encuentra un error, se detiene la ejecución del código que prosiga después del error y _catch_ captura ese error y ejecuta el bloque de código asignado al caso de que existiera un error.

#### Async-Await: ¿Qué es lo que hace? y primer ejemplo

Son una alternativa a los _Promises_ pero funcionan sobre ellos.

La palabra reservada _async_ va en la función padre que llama a las otras funciones, mientras que _await_ se utiliza en la parte del código que va a esperar a que se ejecute el _promise_. En palabras simples, lo que hace _await_ es darle entender a JS que debe esperar (detiene la ejecución del código hasta que se resuelva el _promise_) a que el fragmento con _await_ entregue una respuesta antes de seguir ejecutando el código.

El siguiente es un ejemplo de _async-await_ con _function delcaration_.

```js
function descargarClientes(){

    return new Promise( (resolve, reject) => {
        const error = false; // Si el valor es true...

        setTimeout( () => {
            if(!error){
                resolve('Listado de clientes descargado exitosamente');
            } else{
                reject('Error en la conexión');
            }
        }, 3000);
    })
}

// Async-Await
async function ejecutar(){
    try {
        console.log('Antes del await');
        const respuesta = await descargarClientes();
        console.log('Después del await'); // ... esta línea y la siguiente no se ejecutaría...
        console.log(respuesta);
    } catch (error) {
        console.log(error); // ... pasaría directamente al catch
    }
}

ejecutar();
```

#### Async-Await en _function expresion_

En el caso de utilizar _function expresion_, la palabra reservada _async_ se posiciona antes de la función anonima. Esa es la diferencia entre _function expresion_ y _function declaration_.

```js
function descargarClientes(){

    return new Promise( (resolve, reject) => {
        const error = false;

        setTimeout( () => {
            if(!error){
                resolve('Listado de clientes descargado exitosamente');
            } else{
                reject('Error en la conexión');
            }
        }, 3000);
    })
}

// Async-Await
const ejecutar = async () => {
    try {
        console.log('Antes del await');
        const respuesta = await descargarClientes();
        console.log('Después del await');
        console.log(respuesta);
    } catch (error) {
        console.log(error);
    }
}

ejecutar();
```

#### ¿Cómo manejar multiples _await_?

El uso de multiples _await_ es util en casos como el consumo de más de una API de manera muy eficiente.

```js
// Promesas que se utilizaran de ejemplo
function descargarNuevosClientes(){
    return new Promise( resolve => {
        console.log('Descargando Clientes...');

        setTimeout(() => {
            resolve('Los clientes han sido descargados')
        }, 5000);
    } )
}

function descargarNuevosPedidos(){
    return new Promise( resolve => {
        console.log('Descargando Pedidos...');

        setTimeout(() => {
            resolve('Los pedidos han sido descargados')
        }, 3000);
    } )
}
```

El siguiente bloque de código contiene lo que sería el llamado de 2 promesas utilizando _async-await_. Primero se resolvera una promesa y luego la otra, lo cual en algunos casos está bien, sin embargo, esto puede llegar a afectar la performance de la aplicación.

```js
const app = async () => {
    try {
        const clientes = await descargarNuevosClientes();
        console.log(clientes);
        
        const pedidos = await descargarNuevosPedidos();
        console.log(pedidos);
    } catch (error) {
        console.log(error);
    }
}

app(); // Tiempo de ejecución 8 segundos
```

Si nos encontramos en el caso de que ambas promesas que queremos ejecutar no tienen implicancia una sobre la otra, se puede utilizar el método de las promesas `Promise.all([arreglo-de-promesas])` que recibe un arreglo con las promesas que se quieren utilizar y retorna una arreglo con sus respectivas respuestas. Lo que hace el método anterior es que ejecuta ambas promesas al mismo tiempo, lo cual dismimiye el tiempo de espera entre el request y la respuesta.

```js
const app = async () => {
    try {
        const respuesta = await Promise.all([ descargarNuevosClientes(), descargarNuevosPedidos() ]);
        console.log(respuesta);
    } catch (error) {
        console.log(error);
    }
}

app(); // Tiempo de ejecución 5 segundos
```

#### Async-Await hacia una API con Fetch

Con la combinación de la estructura _try-catch_ y las palabras _async-await_, se pueden consumir APIs de la misma forma que se hacía con _fetch-then-catch_ pero de una manera en la cual el código queda más legible. Esta nueva forma de consumo a APIs suele ser utilizada con los frameworks de JS y con Node.js

```js
const url = 'https://picsum.photos/list';

document.addEventListener('DOMContentLoaded', obtenerDatos);

// Consumo de API con fetch-then-catch
// function obtenerDatos() {
//     fetch(url)
//         .then( respuesta => respuesta.json())
//         .then( datos => console.log(datos))
//         .catch( error => console.log(error));
// }

// Consumo de API con async-await
async function obtenerDatos() {
    try {
        const respuesta = await fetch(url); // Es línea bloquea a la siguiente línea hasta que termine de ejecutarse
        const datos = await respuesta.json(); // Se hacen por separado debido a que esta depende de la respuesta de la llamada anterior
        console.log(datos);
    } catch (error) {
        console.log(error);
    }
}
```

### Functional JavaScript

#### ¿Qué es Functional JS?

- En palabras simples es crear tu código utilizando funciones.
- Existe reglas para la programación funcional, como las que serían que las **funciones deben tomar una entrada y tener una salida de datos**.
- **NO SE PERMITE LA MODIFICACIÓN DE LOS DATOS**.
- Se podría decir que tiene una sintaxix más orientadas a las matemáticas.

Los conceptos claves de la programación funcional son los siguientes:

- **Inmutabilidad** - Los datos no deben modificarse (se suele utilizar casi siempre _const_)
- Se separan las Funciones de datos - Se utilizan mucho funciones que retornan un nuevo dato o _Array Methods_, de esa forma tendremos funciones que entregan un resultado nuevo pero nunca modifica los datos de entrada.
- First-class functions - Es poder crear funciones que parezcan cualquier variable como lo es _function expression_

#### First Class Functions

Se trata de poder asignar una función a una variable como si fuera un valor (string, boleano, etc), haciendo que se pueda utilizar la variable como un _"alias"_ de la función.

```js
const suma = function( a,b ) {
    return a + b;
}

const resultado = suma;

console.log(resultado( 10,20 ));
```

#### Funciones como argumento

Es cuando se establece lo que se podría llamar una _plantilla de función_, la cual tiene ciertos paramatros que dependiendo de la función que se le entregue como parametro a la plantilla, hará cierta cosa.

```js
const suma = ( a,b ) => a + b; // Función que suma 2 números
const multiplicar = ( a,b ) => a * b; // Función que multiplica 2 números

const sumarOMultiplicar = fn => fn( 10,20 ); // fn será la suma o la multiplicación dependiendo de la función que se le entregue como argumento

console.log( sumarOMultiplicar( suma ) ); // Suma 10 y 20
console.log( sumarOMultiplicar( multiplicar ) ); // Multiplica 10 y 20
```

#### Separar los Datos de las funciones (Higher order functions)

Son funciones que toman o retornan una función como argumento, básicamente la mayoría de los _Array Methods_ son _Higher order functions_.

```js
const carrito = [
    { nombre: 'Monitor 20 Pulgadas', precio: 500},
    { nombre: 'Televisión 50 Pulgadas', precio: 700},
    { nombre: 'Tablet', precio: 300},
    { nombre: 'Audifonos', precio: 200},
    { nombre: 'Teclado', precio: 50},
    { nombre: 'Celular', precio: 500},
    { nombre: 'Bocinas', precio: 300},
    { nombre: 'Laptop', precio: 800},
];

// Modo normal
const resultado = carrito.filter( producto => producto.precio > 400 );
console.log( resultado );

// Modo Higher order function
const mayor400 = producto => {
    return producto.precio > 400
}

const resultado2 = carrito.filter( mayor400 );
console.log( resultado2 );
```

#### .map es muy utilizado en Functional JS

A diferencia de _.forEach()_, `.map()` itera sobre un arreglo y a su vez crea un nuevo arreglo con el resultado de la iteración. Lo anterior permite que cualquier operación que se aplique a un arreglo existente, no modifique ese arreglo.

```js
const carrito = [
    { nombre: 'Monitor 20 Pulgadas', precio: 500},
    { nombre: 'Televisión 50 Pulgadas', precio: 700},
    { nombre: 'Tablet', precio: 300},
    { nombre: 'Audifonos', precio: 200},
    { nombre: 'Teclado', precio: 50},
    { nombre: 'Celular', precio: 500},
    { nombre: 'Bocinas', precio: 300},
    { nombre: 'Laptop', precio: 800},
];

const obtenerNombresProductos = producto => producto.nombre;

const nombresProductos = carrito.map( obtenerNombresProductos );
console.log( nombresProductos );
```

#### Menos cantidad de código en las funciones

Con la idea de minimizar la cantidad de código que se utiliza, se puede utilizar la forma mád corta de las _arrow functions_ en la cual, si es sólo una línea, se da or implicito el return y no es necesario utilizar llaves. Sumado a lo anterior, las variables tipo alias que se le da al elemento iterador, puede ser una sola letra.

```js
const carrito = [
    { nombre: 'Monitor 20 Pulgadas', precio: 500},
    { nombre: 'Televisión 50 Pulgadas', precio: 700},
    { nombre: 'Tablet', precio: 300},
    { nombre: 'Audifonos', precio: 200},
    { nombre: 'Teclado', precio: 50},
    { nombre: 'Celular', precio: 500},
    { nombre: 'Bocinas', precio: 300},
    { nombre: 'Laptop', precio: 800},
];

const obtenerNombresProductos = p => p.nombre;

const nombresProductos = carrito.map( obtenerNombresProductos );
console.log( nombresProductos );

const mayor400 = p => p.precio > 400
const resultado2 = carrito.filter( mayor400 );
console.log( resultado2 );
```

#### Pure Functions

Mayomente utilizadas en _react.js_, son funciones que retornan un dato sin modificar los valores de las variables globales, o sea, retornan un nuevo dato. Además de lo anterior, las _funciones puras_ tienen la caracteristica de reotrnar tanto datos como reciben.

```js
// Funciones puras o Pure Functions

const duplicar = numero => numero * 2; // Recibe un parametro y retorna un nuevo parametro

const numero1 = 20; // Variable global

const numero2 = duplicar(20); // El uso de la variable global en la función no modifica a la variable global

console.log(`La variable global es ${numero1} y la nueva variable es ${numero2}`);
```

#### Funciones que retornan una función

Son funciones que se estructuran como una _arrow function_ pero que dentor de la _arrow function_ hay otra _arrow function_ .

```js
const obtenerCliente = () => () => console.log('Retornando una función');

const fn = obtenerCliente();
console.log( fn ); // Muestra la función anonima

fn(); // La variable se puede utilizar como función
```

#### Closures

Los closures van de la mano con los scope (alcances) que existe entre las variables de los distintos bloques de código. Los closures se crean cada vez que se crea una función, son la forma de accder a una función o valor desde el exterior de la función.

```js
const obtenerCliente = () => {
    const nombre = 'Pedro';

    function muestraNombre() {
        console.log(nombre);
    }

    return muestraNombre;
}

const cliente = obtenerCliente(); // obtenerCliente retorna la función muestraNombre

cliente(); // Debido a lo anterior es que al invocar cliente, se muestra el nombre definido dentro de la función
```

#### Partials y Currying

_Currying_ es dividir una función que toma más de un parametro en argumentos de forma parcial. Lo anterior se hace utilizando _arrow functions_ y similar a _First Class Functions_, lo que hace es que por cada división de parametros se crea una función parcial que recibirá el o los siguiente parametros.

```js
// Ejemplo al divir en dos partials
const suma = ( a, b, c ) => a + b + c;

// Hacer uso de Currying y partials
const parcial = (a) => (b, c) => suma( a,b,c );

const primerNumero = parcial(5); // primerNumero es una función que ya tiene el valor de a pero que si se invoca, debe recibir dos parametros más
console.log(primerNumero);

const resultadoSUma = primerNumero(5,5);
console.log(resultadoSUma); // 15
```

```js
// Ejemplo al dividir en 3 partials
const partial = a => b => c => suma( a, b, c );

const primerArgumento = partial( 5 ); // Se entrega a
console.log(primerArgumento);

const segundoArgumento = primerArgumento( 5 ); // Se entrega b
console.log(segundoArgumento);

const tercerArgumento = segundoArgumento( 5 ); // Se entrega c
console.log(tercerArgumento);
```

Lo anterior puede parecer mucho trabajo y mucho código, lo cual es cierto, es por esto que existe una sitaxis mucho más sencilla para utilizar los parciales y es la siguiente:

```js
const suma = ( a, b, c ) => a + b + c;

const partial = a => b => c => suma( a, b, c );

const resultado = partial(5)(5)(5);
console.log(resultado);
```

#### Composition

Se podría decir que viene a ser como una alternativa a las clases. Se utiliza cuando existen funciones que se pueden compartir entre objetos, o sea, se escribe una función que puede ser utilizada en diferentes objetos y se las vas asignando para que puedas utilizarla en vez de utilizar la herencia entre clases.

Hay que tener en consideración, que con _Composition_, el constructor del objeto es distinto, se utiliza la forma antigua de construir clases y se establece un objeto que almacenará sus atributos. Teniendo claro lo anterior, se asignarán los métodos meidante composition, en la cual se definirá una función que recibirá el objeto con los atributos y reotrnará el método que se utilizará en los objetos pertenecientes a la clase que hayamos definidos. Por último, para asignar estas funciones, se debe utilizar un return dentro de la clase, seguido de `Object.assign()`, el cuál recibirá como parámetro el objeto de los atributos y el nombre de la función que contiene el método que se quiere asignar.

El acceso a los atributos y métodos en estas clases, es mediante la sintaxis de punto pero en el caso de los métodos, hay que llamar el nombre del método que reotrnaba la función que se le entrego a `Object.assign()`.

```js
// Composition function
// La función obtenerNombre sirve para asignar mostrarNombre a los objetos al usar Object.assign()
const obtenerNombre = info => ({
    // Toma el objeto que almacena los parametros que se entregan al constructor del objeto
    mostrarNombre() {
        console.log(`Nombre: ${info.nombre}`);
    }
})


function Cliente( nombre, email, empresa ) {
    let info = {
        nombre,
        email,
        empresa
    };

    return Object.assign(
        info,
        obtenerNombre(info)
    )
}

function Empleado( nombre, email, puesto ) {
    let info = {
        nombre,
        email,
        puesto
    };

    return Object.assign(
        info,
        obtenerNombre(info)
    )
    
}

const cliente = Cliente( 'Pedrito', 'pedrito@pedro.com', 'P.E.D.R.O dot COM' );
cliente.mostrarNombre();

const empleado = Empleado( 'Pedrote', 'pedrote@pedrote.com', 'Programador' );
empleado.mostrarNombre();
```

El siguiente es un ejemplo en el cual se creará una función para entregar datos a un atibuto del objeto.

```js

const guardarEmail = info => ({
    agregarEmail( email ) {
        info.email = email;
        console.log( `${email} guardado para el cliente ${ info.cliente }` );
    }
})

function Cliente( nombre, email, empresa ) {
    let info = {
        nombre,
        email,
        empresa
    };

    return Object.assign(
        info,
        guardarEmail(info)
    )
}

function Empleado( nombre, email, puesto ) {
    let info = {
        nombre,
        email,
        puesto
    };

    return Object.assign(
        info,
        guardarEmail(info)
    )
    
}

const cliente = Cliente( 'Pedrito', null, 'P.E.D.R.O dot COM' );
console.log('--------------------------------');
console.log(cliente);
console.log('--------------------------------');
cliente.agregarEmail('pedrito@pedro.com');
console.log('--------------------------------');
console.log(cliente);


const empleado = Empleado( 'Pedrote', null, 'Programador' );
console.log('--------------------------------');
console.log(empleado);
console.log('--------------------------------');
empleado.agregarEmail('pedrote@pedrote.com');
console.log('--------------------------------');
console.log(empleado);
```

### Dominando JS

#### Scope

Es el alcance que tiene una variable dentro de un bloque de código.
Existen 2 tipo de _scope_, uno es el _scope global_ y el otro es el _scope de una función o un bloque de código_.

```js
// Ejemplo 1
const cliente = 'Juan';

function mostrarCliente() {
    console.log(cliente);
}

mostrarCliente();
```

En el ejemplo anterior (Ejemplo 1), la función _mostrarCliente()_ muestra el valor de la variable cliente. Al no haber ninguna variable con ese nombre dentro de la función, busca en el scope global una variable con ese nombre, es debido a lo anterior que la función muestra el contenido de la variable global cliente.

```js
// Ejemplo 2
function mostrarCliente() {
    const cliente = 'Juan';
}
console.log(cliente);

mostrarCliente();
```

En el ejemplo 2, se define dentro de la función una variable cliente, su scope es sólo el de la función, debido al scope es que al momento de intentar mostrar por consola la variable cliente, muestra un error `Uncaught ReferenceError: cliente is not defined` debido a que en el scope global no hay ninguna variable llamada cliente definida.

En JS el scrope lo delimitan las llaves, por lo cual si hay código entre llaves, hay un nuevo scope.

#### Hoisting

Es un termino que se utiliza para referirse a como funcionan los contextos de ejecución en el lenguaje. JavaScript se ejecuta en dos partes, primero se recorre el código creando (registrandolas) las variables y en la segunda parte se ejecutan. Debido a lo anterior, existen diferencias entre _function expression_ y _function declaration_, sin importar donde se mande a llamar una función del tipo _function declaration_, no existirán errores al momento de ejecutar el código, en cambio, no se puede llamar una función del tipo _function expression_ antes de ser declarada porque arroja error al ejecutarse. Lo anterior se debe a que en la primera parte de la ejecución, las funciones del tipo _function expression_ son registradas como variables con valor _undefined_, lo cual provoca que en la segunda parte de la ejecución exista un error al llamar la función antes de declararla (en la declaración es donde se cambia el undefined por la función que registrará a la variable como una función).

```js
// Function declaration
obtenerCliente('Pedro'); // Da igual si se encuentra el llamado antes o después de la función
function obtenerCliente( nombre ) {
    console.log(`El nombre del cliente es ${nombre}`);
}


// Function expression
// obtenerCliente2('Pedro'); // No funciona estando acá
const obtenerCliente2 = ( nombre ) => {
    console.log(`El nombre del cliente es ${nombre}`);
}
obtenerCliente2('Pedro'); // Funciona
```

#### Coercion

Hace referencia a la conversión automatica (implicita) o explicita de valores de un tipo dado a otro.

```js
// Coerción implicita
const numero1 = 20;
const numero2 = "40";

// Se fuerza a JS maneje la diferencia de los tipos de datos (transforma el 20 de numero a string) 
console.log( numero1 + numero2 );

// Coerción explicita
console.log(Number(numero2)); // Explicitamente se cambia el tipo del valor de la variable
console.log(numero1.toString());

const pedido = [1,2,3,4];
console.log(pedido.toString());
console.log(JSON.stringify(pedido));
```

#### Implicit Binding

Se da por implicito donde encontrar el valor mediante el uso de `this.`. 

```js
// Implicit Binding

const usuario = {
    nombre: 'Pedro',
    edad: 20,

    informacion() {
        /* .this hace referencia a que las variables se encuentran
        en "este" objeto, dentro de su scope */
        console.log(`${this.nombre} tiene ${this.edad} años`);
    },

    mascota: {
        nombre: 'Puerco-Araña',
        edad: '5',

        informacion() {
            /* .this hace referencia a los atributos que se encuentran
            en el scope más cercano al método */
            console.log(`${this.nombre} tiene ${this.edad} años`);
        }
    }
}

usuario.informacion();
usuario.mascota.informacion();
```

#### Explicit Binding

Es similar al _Implicit Binding_ pero en este caso se ocupa una de estas 3 funciones :

- **.call()**: Es una función que existe en todas las funciones de JS, inclusive en las que uno crea. Recibe cualquier tipo de variable y sirve para especificarle a una función que elementos debe utilizar.

```js
// Explicit Binding

function persona( elemento1, elemento2 ) {
    console.log(`Mi nombre es ${this.nombre} y escucho ${elemento1} y ${elemento2}`);
}

const informacion = {
    nombre: 'Juan'
}

const musicaFavorita = ['Heavy Metal', 'Rock'];

/* .call() requiere que en el caso de los arreglos, se entreguen
los elementos uno a uno */
persona.call( informacion, musicaFavorita[0], musicaFavorita[1] );
```

- **.apply():** Es una función que existe en todas las funciones de JS, inclusive en las que uno crea. Recibe cualquier tipo de variable y a diferencia de `.call()`, puede recibir un arreglo, no es necesario especificar cada uno de los elementos de este.

```js
// Explicit Binding

function persona( elemento1, elemento2 ) {
    console.log(`Mi nombre es ${this.nombre} y escucho ${elemento1} y ${elemento2}`);
}

const informacion = {
    nombre: 'Juan'
}

const musicaFavorita = ['Heavy Metal', 'Rock'];

/* Funciona igual que .call() pero no es necesario especificar
uno a uno los elementos del arreglo */
persona.apply( informacion, musicaFavorita );
```

- **.bind():** Funciona igual que `.call()` pero crea una nueva función.

```js
// Explicit Binding

function persona( elemento1, elemento2 ) {
    console.log(`Mi nombre es ${this.nombre} y escucho ${elemento1} y ${elemento2}`);
}

const informacion = {
    nombre: 'Juan'
}

const musicaFavorita = ['Heavy Metal', 'Rock'];

/* Funciona igual que .call(), también se debe especificar cada uno
de los elementos del arreglo, la diferencia es que crea una nueva función */
const nuevaFuncion = persona.bind(informacion, musicaFavorita[0], musicaFavorita[1]);
nuevaFuncion();
```

#### new Binding

Cada vez que se crea un nuevo objeto con la palabra reservada `new`, se crea un _new binding_, que hace referencia al uso de _.this_ para el nuvo objeto creado.

```js
function Auto( modelo, color ) {
    this.modelo = modelo;
    this.color = color;
}

const auto = new Auto( 'Camaro', 'Negro' );
console.log(auto);
```

#### Window Binding

Es cuando se almacenan valores en al ventana global. Cuando JS no encuetra la definición de una variable, la busca en la ventana global (`window`), si no la encuentra ahí muestra un error de que la variable no está definida.

```js
// Window Binding

window.color = 'negro';
function obtenerColor() {
    console.log(color);
}
obtenerColor();
```

#### Event Loop o Loop de Eventos

Es como se va ejecutando el código en JS, es decir, que tiene mayor prioridad de ejecución.

**Nota:** En la pagina de [MDN Web Docs](https://developer.mozilla.org/es/docs/Web/JavaScript/EventLoop) y en el vídeo de la presentación de [Philip Roberts en la JSConf EU 2014](https://www.youtube.com/watch?v=8aGhZQkoFbQ&t=119s), se explica muy bien lo que es el _Event Loop_.

```js
console.log('Primero');

setTimeout( () => {
    console.log('Segundo');
}, 0);

console.log('Tercero');

setTimeout( () => {
    console.log('Cuarto');
}, 0);

new Promise(function(resolve){
    resolve('Desconocido...');
}).then(console.log)

console.log('Ultimo');

function hola() {
    console.log('Hola');
}
hola();
```

En el ejemplo anterior, se puede observar que los console.log tienen mayor prioridad que lo demás, seguidos por la función, luego la promesa y finalmente los setTimeout que se puede decir que realmente no empiezan en 0 como se le indica en el código.

#### ¿Qué es self?

Básicamente, self hace referencia a la ventana global (windows) y es utilizada en _Service Workers_ (donde no se encuentra disponible la palabra window) y _Progressive web apps_.

```js
// window == self

// window.onload = () => {
//     console.log('Ventana lista');
// }

// self.onload = () => {
//     console.log('Ventana lista utilizando self');
// }

window.nombre = 'Pedro';

const persona = {
    trabajo: 'Programador',
    mostrarInfo() {
        console.log(`${self.nombre} es un ${this.trabajo}`);
        // self hace referencia a la ventana global mientras que this hace referencia al objeto
    }
}

persona.mostrarInfo()

const producto = {
    nombre: 'Monitor 20 Pulgadas',
    precio: 30,
    disponible: true,
    mostrarInfo: function() {
        const self = this; // Se puede dar como "seudonimo" a this la palabra self
        return `El producto: ${self.nombre} tiene un precio de ${self.precio}`
    }
}

console.log(producto.mostrarInfo());
```

### Service Workers y PRogressive web apps (PWA)

#### Caracteristicas de una PWA

- **Rapida** - Cargan toda la información en menos de 5 segundos.

- **Instalable** - Se pueden navegar o instalar en tu navegador o teléfono móvil como una aplicación nátiva.

- **Soporte Offline** - Pueden funcionar si una conexión a internet.


#### Service Workers

- **Es la base de una PWA**. Son scripts que están corriendo todo el tiempo detrás de escenas.

- Funcionan Offline.

- **No tienen acceso al DOM**.

- Cargan de forma instantanea.

- Pueden sincronizar datos detrás de escena o sin interferir en la navegación.

##### Funciones No Disponibles en Service Workers

- No utiliza la ventana global (window), utiliza _self_.

- No utiliza document, utiliza caches.

- No utiliza localStorage, utiliza fetch.

#### Generar reporte de Lighthouse

Lighthouse es una herramienta que permite generar reportes con información sobre una pagina web referente a Performance, Accesibilidad, SEO, Mejores Practicas, y PWA. Lo anterior para mobile y desktop.

Con esta herramienta se puede saber que es requerido para poder transformar una página web en una PWA, además de conocer las desvalencias que presenta en cada uno de los ambitos antes mencionados.

Uno de los elementos que harán falta al momento de realizar la transición hacía una PWA es el _manifest.json_, el cual es un archivo obligatorio al momento de crear una PWA.

Para agregar el _manifest.json_ al HTML hay que agregar como si fuera una hoja de estilo. 

```html
<link rel="manifest" href="manifest.json">
```

```json
{
    "name": "APV",
    "short_name": "APV",
    "start_url": "./index.html",
    "display": "standalone",
    "background_color": "#D41872",
    "theme_color": "#D41872",
    "orientation": "portrait",
    "icons": [
        {
          "src": "img/icons/Icon-72",
          "type": "image/png",
          "sizes": "72x72"
        },
        {
          "src": "img/icons/Icon-120.png",
          "type": "image/png",
          "sizes": "120x120"
        },
        {
          "src": "img/icons/Icon-128.png",
          "type": "image/png",
          "sizes": "128x128"
        },
        {
          "src": "img/icons/Icon-144.png",
          "type": "image/png",
          "sizes": "144x144"
        },
        {
          "src": "img/icons/Icon-152.png",
          "type": "image/png",
          "sizes": "152x152"
        },
        {
          "src": "img/icons/Icon-196.png",
          "type": "image/png",
          "sizes": "196x196"
        },
        {
          "src": "img/icons/Icon-256.png",
          "type": "image/png",
          "sizes": "256x256"
        },
        {
          "src": "img/icons/Icon-512.png",
          "type": "image/png",
          "sizes": "512x512"
        }
      ]
}
```

#### Detectar el soporte de Service Workers

Para detectar el sporte de Service Worker con el navegador utilizando JS, se debe hacer lo siguiente:

```js
if( 'serviceWorker' in navigator ) {
    // Se registra el service worker de la app
    navigator.serviceWorker.register('./sw.js')
    .then( registrado => console.log('Service worker fue registrado exitosamente...', registrado) )
    .catch( error => console.log('Fallo la instalación...', error) )

}else {
    console.log("Service Worker no soportado");
}
```

Dependiendo del contenido del service worker, existirá un tiempo de carga, por lo cual `navigator.serviceWorker.register('./sw.js')` retorna una promesa.

#### Instalar y Activar un Service Worker

La instalación del SW se hace una sola vez, por lo cual el evento que se le agregue a esa instalación se ejecutara una sola vez, por lo cual da igual cuantas veces se recargue la página, la instalación no se volverá a realizar.

```js
// sw.js
// Evento que sucede al instalarse el SW
self.addEventListener('install', e => {
    console.log('Instalado el Service Worker...');

    console.log(e)
});
```

Por otro lado existe el evento de activación, el cual se ejecuta cuando llamamos a activar el SW, por ende, no se activa automaticamente.

```js
// sw.js
// Evento para activar el SW
self.addEventListener('activate', e => {
    console.log('Service Worker Activado...');

    console.log(e)
});
```

La instalación del SW es un buen momento para añadir al caché ciertos archivos, mientras que la activación es un buen lugar para nuevas versiones de la PWA.

#### Hacer una PWA Instalable

Las PWA sepeuden instalar tanto en un navegado de escritorio como en dispositivos mobiles. Para poder hacerlo se requieren 3 cosas:

- Un manifest.json valido
- Tener un dominio https o un localhost
- Se debe tener registrado el eventlistener de fetch

En las secciones anteriores se han visto 2 de los 3 requisitos, quedando sólo el registro del evento fetch. El evento fetch se agrega al archivo sw.js d ela siguiente manera:

```js
// sw.js
// Evento fetch para descargar archivos estaticos
self.addEventListener('fetch', e => {
    console.log('Registrando fetch...', e)
})
```

#### Cachear Archivos

Se recomienda guardar caché al momento de la instalación del Service Worker.
El cachear archivos ayuda a que se pueda ver información de manera offline. Lo recomendable es que se descargué el caché de las páginas que el usuario visita, no de toda la app, de lo contrario la carga se haría muy lenta y la idea es que una PWA sea rápida.

Antes de poder cachear elemetos, es necesario darle un nombre.

```js
const nombreCache = 'apv-v1';
```

Luego hay que indicar los elementos que se quieren cachear, y ya que estos pueden pesar una gran cantidad de mb, el service worker tiene un método llamado `.waitUntil()` que se utiliza con el evento proveniente de, en este caso, install. Dentro del método anterior se agrega un `caches.open(nombre-cache)` el cual retorna una promesa en la cual se puede indicar que se está alamcenando archivos en el cache y hay que agregar el método `.addAll(archivos-cache)` al elemento cache de la función anonima de la promesa.

```js
//sw.js
// Nombre 
const nombreCache = 'apv-v1';

// Archivos para almacenar en el caché para utilizarlos de forma offline
const archivos = [
    "/",
    "index.html",
    "./css/bootstrap.css",
    "./css/styles.css",
    "./js/app.js",
    "./js/apv.js",
  ];

// Evento que sucede al instalarse el SW
self.addEventListener('install', e => {
    console.log('Instalado el Service Worker...',e)
    // El SW espera a que se guarden todos los archivos en el Cache
    e.waitUntil(
        caches.open(nombreCache)
            .then( cache => {
                console.log('Almacenando archivos en el cache...');
                cache.addAll(archivos) // .add() sería si fuera un sólo archivo
            } )
    )
});
```

#### Agregar soperte offline

Para mostrar los archivos almacenados en el caché, existe un método del evento fetch llamado `.respondWith( caches.match(e.request) )` el cual indentifica el request que se está haciendo y retorna una promesa, por lo cual se utiliza `.then()` para recibir la respuesta que sería lo almacenado en el cache.

#### Agregar un página de error cuando no hay conexión

Al momento de obtener lo almacenado en el caché, en el `.catch()` se pasa una arrow function que retorne `caches.match('/error.html')`, es necesario haber cacheado con anterioridad la página de error.

```js
// En sw.js en fetch
// Evento fetch para descargar archivos estaticos
self.addEventListener('fetch', e => {
    console.log('Registrando fetch...', e)

    e.respondWith(
        caches.match(e.request)
            .then( respuestaCache => {
                return respuestaCache
            })
            .catch( () => caches.match('/error.html'))
    )
})
```

```js
// opción alternativa
self.addEventListener('fetch', e => {
  console.log('Fetch', e)
 
  e.respondWith(
    caches
      .match(e.request)
      .then(cacheResponse => (cacheResponse ? cacheResponse : caches.match('error.html')))
    
  )
})
```

#### Como Realizar nuevas secciones del PWA

Al lanzar nuevas versiones de la app, es necesario eliminar el cache anterior e instalar el nuevo. Un buen lugar para hacerlo es el evento _activate_.

```js
// En sw.js
const nombreCache = 'apv-v3'; // new version of the cache for the new version of the app

// Evento para activar el SW
self.addEventListener('activate', e => {
    console.log('Service Worker Activado...')

    e.waitUntil(
        caches.keys()
            .then( keys => {
                // console.log(keys);

                return Promise.all(
                    keys.filter( key => key !== nombreCache )
                        .map( key => caches.delete(key) ) // Borra los caches no actuales
                )
            })
    )
});
```

### Design Patterns o Patrones de diseño en JavaScript

Los patrones de diseño son soluciones típicas a problemas comunes en Desarrollo de software, cada patrón es como unplano que e puede personalizar para resolver un problema de diseño en el código.

Entres los **beneficios** que presentan los patrones de diseño, se encuentran los siguientes:

- Son soluciones a problemas de diseño de código.
- Son soluciones probadas.
- Son soluciones posiblemente conocidad por todos por lo cual ayuda a mantener un patrón en el desarrollo de software.

Existen diferentes **categorías** de patrones de diseño entre las cuales se encuentran:

- **De Creación:** Permiten crear objetos y permiten la reutilización del código.

- **De Estructura:** Explican como deben comunicarse los objetos y clases en grndes proyectos.

- **De Comportamiento:** Se encargan de como se comportan y comunican los objetos.

#### Class Pattern (Creación)

Básicamente es la utilización de clases para la creación de los objetos. Define el como deben crearse los objetos y los patrones que estos deben tener.

```js
// Class Pattern ejemplo

class Persona {
    constructor(nombre, email){
        this.nombre = nombre;
        this.email = email;
    }
}

const persona = new Persona("Pedro", "pedro@pedro.pe");
console.log(persona);
```

#### Constructor Pattern (Creación)

En este patrón de diseño se utiliza una clase base como plano para que las demás clases hereden sobre esta, o sea, es como tener una clase principal que hereda sus caracteristicas a las demás. Lo anterior en otros lenguajes de programación se conocen como **_Clases Abstractas_** (JavaScript no acepta clases abstractas, pero otros lenguajes si las aceptan y esas clases no son intansiables).

```js
// Constructor Pattern

class Persona {
    constructor(nombre, email){
        this.nombre = nombre;
        this.email = email;
    }
}

class Cliente extends Persona {
    constructor(nombre, email, empresa, telefono) {
        super(nombre, email);
        this.empresa = empresa; // Nueva propiedad
        this.telefono = telefono; // Nueva propiedad
    }
}

const cliente = new Cliente("Pedro", "pedro@pedro.pe","Pedro Co.", "123456789");
console.log(cliente);
```

#### Singleton (Creación)

Secaracteriza por no permitir la creación de multiples instacias de una misma clase, en cambio, siempre retorna el objeto instanciado. Este patrón de diseño requiere el uso de una variable que represente a la instaciación de la clase la cual se inicializa vacía (_null_) y para modificarla, es necesaria agregarla en el constructor de la clase y su valor será el objeto, o sea, _this_. PAra prevenir que se instancia nuevamente el objeto, en el constructor se añade un condicional el cual permite instanciar el objeto solamene cuando la variable instancia se encuentre vacía. Usualmente se utiliza cuando se almacena toda la información general en un sólo objeto.

```js
// Singleton

let instancia = null; // Variable de instancia

class Persona {
    constructor(nombre, email) {
        // El objeto se instancia solamente si la variable instancia está vacía
        if(!instancia) {
            this.nombre = nombre;
            this.email = email;
            instancia = this;
        } else {
            return instancia;
        }
    }
}

const persona = new Persona("Pedro", "pedro@pedro.pe");
console.log(persona);

const persona2 = new Persona("Karen", "karen@pedro.pe");
console.log(persona2); // Muestra los valores de la primera instancia
```

#### Factory (Creación)

Es una forma de crear objetos en base a una cierta condición que provoca que algunos atributos sean comunes y otros diferentes. Este tipo de patrón de diseño es utilizable ne ciertos casos.

```js
// Factory - Crea objetos basados en ciertas condiciones

// Clase que crea inputs en base a un type y un name
class InputHTML {
    constructor(type, name) {
        this.type = type;
        this.name = name;
    }

    crearInput() {
        return `<input type="${this.type}" name="${this.name}" id="${this.name}">`
    }
}

// Clase que sirve para crear inputs dependiendo del tipo de elemento
class HTMLFactory {
    crearElemento(type, name) {
        switch(type) {
            case 'text':
                return new InputHTML('text', name);
            case 'tel':
                return new InputHTML('tel', name);
            case 'email':
                return new InputHTML('email', name);
            default:
                return;
        }
    }
}

const elemento = new HTMLFactory(); // Instancia de la clase condicional

const inputText = elemento.crearElemento("text", "nombre-cliente");
console.log(inputText.crearInput());

const inputTel = elemento.crearElemento("tel", "telefono-cliente");
console.log(inputTel.crearInput());

const inputEmail = elemento.crearElemento("email", "email-cliente");
console.log(inputEmail.crearInput());
```

#### Module (Estructura)

Es cuando un proyecto se estructura en diferentes archivos (modulos) los cuales exportan variables, clases y/o funciones a otros.

#### Mixin Pattern

Es uan forma de agregar funciones a una clase una vez que hayan sido creadas. En este patrón de diseño, las funciones se añaden utilizando `Object.assign( objeto.prototype, nuevasFunciones)`. Entre los benificiones que se encuentran al utilizar esta patrón de diseño es que las mismas funciones se pueden asignar a distintos objetos.

```js
// Mixin Pattern

class Persona {
    constructor(nombre, email){
        this.nombre = nombre;
        this.email = email;
    }

    get nombreCliente() {
        return this.nombre;
    }
}

class Cliente {
    constructor(nombre, email){
        this.nombre = nombre;
        this.email = email;
    }
}

const funcionesPersona = {
    mostrarInformacion() {
        console.log(`Nombre: ${this.nombre} - Email: ${this.email}`);
    },
    mostrarNombreCliente() {
        console.log(`El nombre del Cliente es ${this.nombre}`);
    }
}

// Añadir funcionesPersona a Persona
Object.assign(Persona.prototype, funcionesPersona);

// Añadir funcionesPersona a Cliente
Object.assign(Cliente.prototype, funcionesPersona);

const persona = new Persona("Pedro", "pedro@pedro.pe");
console.log(persona);
persona.mostrarInformacion();
console.log(persona.nombreCliente);
persona.mostrarNombreCliente();

const cliente = new Cliente("Pedroneitor", "pedro@pedro.pe");
console.log(cliente);
cliente.mostrarNombreCliente();
```

#### Namespace (Estructura)

Ayuda a evitar la colisión de nombres de vareiables o funciones de nuestro código con las del _scope global de JS_. La idea es crear un objeto global al rededor de la aplicación y agregar todas las funciones dentro del objeto en lugar de crear multiples funciones fuera del objeto. Es necesario deifnir un objeto global sobre el cual se irán colocando todos os datos, funciones y operaciones relacionadas a la aplicación. Los proyectos grandes suelen beneficiarse de este patrón de diseño ya que evita que funciones con el mismo nombre choquen entre si.

```js
// Namespace

const restaurantApp = {};

// Se añaden platillos a el objeto global
restaurantApp.platillos = [
    {
        platillo: 'Pizza',
        precio: 25
    },
    {
        platillo: 'Hamburguesa',
        precio: 20
    },
    {
        platillo: 'Hot Dog',
        precio: 18
    }
];

restaurantApp.funciones = {
    mostrarMenu: (platillos) => {
        platillos.forEach((platillo, index) => {
            console.log(`Platillo ${index}: ${platillo.platillo} - Precio: ${platillo.precio}`)
        });
    },
    ordenar: () => {
        idOrden = window.prompt(
            "Ingrese el número del platillo que quiere ordenar",
            -1
        );

        if(!idOrden || idOrden >= restaurantApp.platillos.length || idOrden < 0) {
            console.log(`Platillo no encontrado`)
            return;
        }
        const indice = parseInt(idOrden);
        const platilloOrdenado = restaurantApp.platillos[indice].platillo
        console.log(`Tu platillo: ${platilloOrdenado}, está en preparación`)
    },
    agregarPlatillos: (platillo, precio) => {
        const nuevoPlatillo = {
            platillo,
            precio
        };

        // restaurantApp.platillos.push(nuevoPlatillo);
        platillosActualizados = [...restaurantApp.platillos, nuevoPlatillo];
        restaurantApp.platillos = platillosActualizados;
        // restaurantApp.funciones.mostrarMenu(restaurantApp.platillos)
    }
}

restaurantApp.funciones.ordenar();

restaurantApp.funciones.agregarPlatillos("Fideos", 15);

const { platillos } = restaurantApp;
restaurantApp.funciones.mostrarMenu( platillos ); // Es difícil que choque con otro tipo de funciones
```

#### Mediator

Es un patrón de diseño que se comunica con diferentes objetos a la vez, el mediador define objetos ya localizados para objetivos especificos.

```js
// Mediator Pattern
// Creación de Clases
class Vendedor {
    constructor(nombre) {
        this.nombre = nombre;
        this.sala = null;
    }

    oferta( articulo, precio ) {
        console.log(`Tenemos un ${articulo} a un precio de ${precio}`);
    }

    vendido( comprador ) {
        console.log(`Vendido al ${comprador}`);
    }
}

class Comprador {
    constructor(nombre) {
        this.nombre = nombre;
        this.sala = null;
    }

    ofertar( cantidad ) {
        console.log(`${this.nombre} : ${cantidad}`)
    }
}

// Clase Mediadora
class Subasta {
    constructor() {
        this.compradores = {};
    }

    registrar( usuario ) {
        this.compradores[usuario.nombre] = usuario;
        usuario.sala = this; // Asigna la info de la Subasta al usuario
    }

    mostrarSala() {
        console.log(this.compradores);
    }
}

// Creación de objetos
const juan = new Comprador("Juan");
const pablo = new Comprador("Pablo");
const vendedor = new Vendedor("Vendedor de Autos");
const subasta = new Subasta();


// Registrar integrantes en la sala
subasta.registrar(juan);
subasta.registrar(pablo);
subasta.mostrarSala();

// Subasta
vendedor.oferta("Mustang 66", 3000);

juan.ofertar(3500);
pablo.ofertar(4000);

vendedor.vendido(pablo.nombre);
```

### Debug, Medir Performance y Seguridad

#### performance.now() para conocer cuanto tarda en ejecutarse el código

Se puede aplicar `performance.now()` al inicio y al fin de un bloque de código con el de medir el tiempo que le toma a ese bloque ser ejecutado. Para llevar a cabo lo anterior es necesario hacer la resta entre el tiempo final captado por un `performance.now()` y el tiempo de inicio que también fue capturado por otro `performance.now()`.

```js
// llena el select 
function selectCriptomonedas(criptomonedas) {

    // Conocer el tiempo de ejecución
    const inicioEjecucion = performance.now();

    // criptomonedas.forEach( cripto => {
    //     const { FullName, Name } = cripto.CoinInfo;
    //     const option = document.createElement('option');
    //     option.value = Name;
    //     option.textContent = FullName;
    //     // insertar el HTML
    //     criptomonedasSelect.appendChild(option);
    // });

    for( let i = 0; i < criptomonedas.length; i++ ) {
        const { FullName, Name } = criptomonedas[i].CoinInfo;
        const option = document.createElement('option');
        option.value = Name;
        option.textContent = FullName;
        // insertar el HTML
        criptomonedasSelect.appendChild(option);
    }

    const finEjecucion = performance.now()

    console.log( `El tiempo de ejecución fue de ${finEjecucion-inicioEjecucion}` );
}
```

#### async o defer? cual utilizar

async o defer son etiquetas de HTML que pueden ayudar a la carga de los scripts. En el caso de **async**, el script carga inmediatamente el código junto al HTML por lo cual no es recomendable cuando se tienen scripts que modifiquen el HTML. Por otro lado **defer**, no ejecuta el script hasta que el HTML esté completamente cargado pero si lo descarga inmediatamente.

#### Como utilizar Debugger (Chrome) (No parece funcionar en Brave)

Existe la palabra reservada `debugger` la cual detiene la ejecución del código y muestra en el navegador todas las variables que hay hasta el momento en que se pausó la ejecución. Para continuar con la ejecución se debe presionar en un botón de play que se encuentra sobre la página web.

#### Opciones para ofuscar el código y ocultarlo

La ofuscación de código se reocmienda ser utilizado en los casos que haya poco código. [JavaScript2img](https://javascript2img.com/) es una página que permite ofuscar cualquier códgio de JS que se pegue en ella.

#### Otras medidas de seguridad

- **No** almacenar contraseñas en LocalStorage o IndexedDB. Ninguno de los almacenamientos anteriores tienen como objetivo almecenar contenido sensible.

- El **DOM Scripting ya escapa los datos y evita riesgos de seguridad**, utiliza `texContent` la mayoría de las veces, evitando utilizar `innerHTML`.

- **`innerHTML`** puede ser utilizado solamente en los casos donde la fuente d elos datos sea segura.

Respecto a los **Formularios**:

- Se deben validar tanto en el cliente para entregar retroalimentación en tiempo real como en el servidor.

- Si deseas crear apps con Autenticación de usuarios se puede utilizar JWT (Json Web Token) y Auth0.

Consideraciones a tener en cuenta:

- Cuando trabajes con dependencias, utiliza una herramienta para verificar vulnerabilidades como [Snyk](https://snyk.io/).

- Ofuscar el código si lo consideras necesario.

- Siempre Hashear información sensible, lo anterior se puede hacer utilizando la librería **bcrypt**.

### Testing - Creando un Mini Framework

#### Introducción al Testing

##### Ventajas

- Mejorará la calidad detu Software evitando Bugs.

- Existen herramientas que automatizan las pruebas de los proyectos, por lo cual se hace menos complicado o tardado el probar todos los diferentes escenarios en nuestra aplicación.

##### Consideraciones

- ¿Cuántas veces has agregado nuevas funciones a un proyecto existente pero desconoces si funciona bien con lo existente?.

- Tener pruebas hará que una persona que no ha mantenido un proyecto conozca que es loque hace cada parte.

- No harás pruebas de todo, más bien de como seintegran diferentes partes de la aplicación.

##### Tipos de Testing

- **End to End**: Más interactivo, simula algunos clicks, llenar formularios y asegurarse de que se muestra en pantalla lo que se desea. La herramienta Cypress suele ser muy util para la realización de estas pruebas.

- **Integración**: Revisan que múltiples partes de nuestro proyecto funcionen bien.

- **Unit (Unitarias)**: Revisan que cada parte funcione de manera correcta por si sola.

- **Static (Estaticas)**: Revisan por errores en el código mientras vas escribiendo.

##### Herramientas para Testing

- Cada tecnología tiene sus herramientas para Testing, pero una muy popular es Jest, hay versiones para VueJS, Angular, TypeScript, Node, React, etc. Es necesario tener instalado Node.js.

- Otra opción es Cypress que es una herramienta para hacer testings End to End.

#### Creación de un Mini Framework para Testing

El testeo sin herramientas se basa en la creación de pruebas especificas que se pasan si se obtiene el valor esperado.

```js
// Probar 2 valores

function suma(a,b) {
    return a + b;
}

function restar(a,b) {
    return a - b;
}

// Función que compara el resultado con el valor esperado
function expected( esperado ) {
    return {
        toBe( resultado ) {
            if( resultado !== esperado ) {
                console.error(`El resultado de la prueba fue - ${resultado} - , el cual es distinto al valor esperado ${esperado}, por lo cual la prueba no fue superada ❌`);
            } else {
                console.log('Prueba superada correctamente ✔');
            }
        },
        toEqual( resultado ) {
            if( resultado !== esperado ) {
                console.error(`El resultado de la prueba fue - ${resultado} - , el cual no es igual al valor esperado ${esperado}, por lo cual la prueba no fue superada ❌`);
            } else {
                console.log('Prueba superada correctamente ✔');
            }
        }
    }
}

let resultadoPruebaSuma = suma(1,2);
let valorEsperadoSuma = 3;

expected(valorEsperadoSuma).toBe(resultadoPruebaSuma);

// if( valorEsperadoSuma !== resultadoPruebaSuma ) {
//     console.error(`El resultado de la prueba fue - ${resultadoPruebaSuma} - , el cual es distinto al valor esperado ${valorEsperadoSuma}, por lo cual la prueba no fue superada ❌`);
// } else {
//     console.log('Prueba superada correctamente ✔');
// }

let resultadoPruebaResta = restar(8,3);
let valorEsperadoResta = 5;

expected(valorEsperadoResta).toBe(resultadoPruebaResta);

// if( valorEsperadoResta !== resultadoPruebaResta ) {
//     console.error(`El resultado de la prueba fue - ${resultadoPruebaResta} - , el cual es distinto al valor esperado ${valorEsperadoResta}, por lo cual la prueba no fue superada ❌`);
// } else {
//     console.log('Prueba superada correctamente ✔');
// }
```

#### Probando código asincrono

Finalmente se puede probar el código de manera asincrona lo cual permite probar la correcta ejecución de una prueba como el resultado de la prueba.

```js
// Probar 2 valores

function suma(a,b) {
    // return a + b + 1;
    return a + b;
}

function restar(a,b) {
    return a - b;
}

const sumaAsync = async ( a, b ) => {
    return Promise.resolve( suma( a,b ) );
}

// Función que compara el resultado con el valor esperado
function expected( esperado ) {
    return {
        toBe( resultado ) {
            if( resultado !== esperado ) {
                console.error(`El resultado de la prueba fue - ${resultado} - , el cual es distinto al valor esperado ${esperado}, por lo cual la prueba no fue superada ✖`);
            } else {
                console.log('Prueba superada correctamente ✔');
            }
        },
        toEqual( resultado ) {
            if( resultado !== esperado ) {
                console.error(`El resultado de la prueba fue - ${resultado} - , el cual no es igual al valor esperado ${esperado}, por lo cual la prueba no fue superada ✖`);
            } else {
                console.log('Prueba superada correctamente ✔');
            }
        }
    }
}

const test = async ( mensaje, callback ) => {
    try {
        await callback();
        console.log(`La prueba: ${mensaje} se ejecutó correctamente ✔`);
    } catch (error) {
        console.error('Error! Prueba no ejecutada correctamente ✖');
        console.error(error);
    }
}

let resultadoPruebaSuma = suma(1,2);
let valorEsperadoSuma = 3;

expected(valorEsperadoSuma).toBe(resultadoPruebaSuma);

// if( valorEsperadoSuma !== resultadoPruebaSuma ) {
//     console.error(`El resultado de la prueba fue - ${resultadoPruebaSuma} - , el cual es distinto al valor esperado ${valorEsperadoSuma}, por lo cual la prueba no fue superada ❌`);
// } else {
//     console.log('Prueba superada correctamente ✔');
// }

let resultadoPruebaResta = restar(8,3);
let valorEsperadoResta = 5;

expected(valorEsperadoResta).toBe(resultadoPruebaResta);

// if( valorEsperadoResta !== resultadoPruebaResta ) {
//     console.error(`El resultado de la prueba fue - ${resultadoPruebaResta} - , el cual es distinto al valor esperado ${valorEsperadoResta}, por lo cual la prueba no fue superada ❌`);
// } else {
//     console.log('Prueba superada correctamente ✔');
// }

test('Suma 10 + 20 y el resultado debe ser 30', async () => {
    const resultado = await sumaAsync(10, 20);
    const esperado = 30;
    expected(esperado).toBe(resultado);
})
```

### Testing - JEST (Introducción al Testing en JS con JEST)

#### Primeros pasos con Jest

Lo primero es ingresar el comando `npm init` a la consola de comando, ingresar la información que creamos necesaria, lo anterior con el fin de generar un **_package-lock.json_** el cual permitará la instalación de diferentes paquetes ya sea como dependencia de desarrollo (desarrollo) o del proyecto (producción/app final).

Luego se instala JEST como una dependencia de desarrollo con el comando `npm i --save-dev jest`.

Una vez instalado, en el archivo _package.json_, en la propiedad _scripts_. en la propiedad _test_ se coloca `"jest"`. Lo anterior sirve para que cuando se ejecute el comando `npm run test`, `npm test` o `npm t` se ejecuten las pruebas programadas con jest.

**Para que se ejecuten las pruebas, hay que tener los script en una carpeta llama _\_\_test\_\__**, lo anterior se debe a que Jest entiende que esa carpeta es la que contiene los script de pruebas de la aplicación. También se recomienda que los scripts de test lleven como extensión `.test.js` para que sea reconocidos como archivos que contienen pruebas.

Dentro del script de pruebas, se utiliza la función `test()` o la función `it()`, las cuales son la misma y reciben un mensaje como primer argumento y un callback el cual es la prueba que se quiere realizar. También, no es necesario crear un archivo para cada prueba que se quiera realizar, Jest permite agrupar las pruebas de un mismo archivo utilizando la función `describe()`, la cual recibe una decripción de las pruebas a realizar y las pruebas que se quieren agrupar ahí, **agrupar pruebas del mismo tipo en un solo archivo se considera buena practica**.

```js
// Ejemplo de pruebas con jest
// archivo holamundo.test.js en la carpeta __test__

test('Hola testing desde Jest utilizando test', () => {
    // Cuerpo de la prueba
});

it('Hola testing desde Jest utilizando it', () => {
    // Cuerpo de la prueba
});

describe('Grupo de pruebas 1', () => {
    test('Prueba 1', () => {
        // Cuerpo de la prueba
    });
    it('Prueba 2', () => {
        // Cuerpo de la prueba
    });
});
```

### REACT: Aprende React Creando un Proyecto

#### ¿Qué es React?

- Es una librería JS para crear interfaces de usuario para aplicaicones Web.
- Desarollada por Facebook
- Se ejecuta en el cliente (no necesita una respuesta de un servidor).
- Permite ordenar un proyecto de mejor manera por medio de la creación de Componentes.
- Una gran ventaja es que cuenta con una gran cantidad de Herramientas y Librerías así como Soporte.

#### Herramientas para trabajar con React

1. Es necesario tener instalado node y npm. Para saber si ya están instalados, se pueden utilizar los siguientes comandos `node -v ` y `npm -v`.

2. En el directorio que contendrá el proyecto, se utiilza el comando `npx create react app nombre-proyecto` para crear un proyecto en React.js con todo lo necesario para desarrollar.

3. En el navegador (basado en chromium), se recomienda la instalación de [_React Developer Tools_](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=es). En el caso de mozilla existe igualmente un [_React Developer Tools_](https://addons.mozilla.org/es/firefox/addon/react-devtools/).

4. Dentro del directorio creado con los archivos del proyecto, se ejecuta el comando `npm start` para ejecutar la app en react.

5. Se recomienda instalar los complementos _Code ES7+ React/Redux/React-Native/JS snippets_ y _Simple React Snippets_ desde las extensiones de Visual Studio Code.

6. En la carpeta _public_ del proyecto, se encuentra los archivos básicos de una página, en el HTMl se pueden importar hojas de estilo o librerías que se quieran ocupar. En el caso de querer importar librerías, se puede buscar en [cdnjs](https://cdnjs.com/). Ejemplo de librerías que se pueden importar desde [cdnjs](https://cdnjs.com/) son _normalize_ y _skeleton_ (siempre en ese orden, ya que skeleton no funciona sin antes haber importado normalize), las cuales permite el uso de una versión más ligera de bootstrap.

7. Dentro del directorio _src_ se encuentran los archivos a modificar para crear desarrollar la aplicación que queramos. Entre los archivos se pueden encontrar:
    - **_index.js_:** Archivo que se encarga de llamar _App.js_.
    - **_App.js_:** Es el componente principal de la aplicaicón a desarrollar.

#### Estructura básica de un componente

- Los componentes en React pueden contener unas pocas líneas o cientos de línea.

- Se recomienda la creación de un directorio llamado _componments_ para contener los componentes que se desarrollen. Esta carpeta se debe crear dentro del directorio _src_.

- La nomenclatura de nombre de componentes dice que deben comenzar con mayúsuclas y no deben contener espacios.

- Teniendo instalada la extención _Simple React Snippets_, se puede utilizar el shortcut `imr` el cual escribe un `import React from 'react';` al script.

El siguiente es un componente de React que sirve para ver la estructura de los elementos.

```js
// import de React
import React from 'react';

// Función componente a exportar
function Header() {

    // Return de React que retorna un elemnto de HTML
    return(
        <h1>Hola Mundo</h1>
    )
}

// export que indica que se exporta el componente
export default Header;
```

Es importante destacar que estos componentes pueden ser utilizados multiples veces a lo largo de la aplicación y el return de los componentes siempre debe contener un contenedor el cual dentro de él contendrá los demás elmentos.

```js
// Ejemplo App.js que da error
import React from "react";
import Header from "./components/Header"

function App() {
  return (
      <Header />
      <Header />
      <Header />
      <Header />
      <Header />
  );
}

export default App;
```

```js
// Ejemplo App.js sin errores
import React from "react";
import Header from "./components/Header"

function App() {
  return (
    <div className="App">
      {/* Cada componente <Header /> es un elemento que se muestra en el HTML */}
      <Header />
      <Header />
      <Header />
      <Header />
      <Header />
    </div>
  );
}

export default App;
```

Si no se quiere escribir elemenmtos de HTML que contengan los demás elementos, se recomienda el uso de _Fragment_, el se importa desde React y se usa como un div pero no crea un elemento HTML nuevo.

```js
import React, { Fragment } from "react";
import Header from "./components/Header"

function App() {
  return (
    <Fragment>
      {/* Cada componente <Header /> es un elemento que se muestra en el HTML */}
      <Header />
      <Header />
      <Header />
      <Header />
      <Header />
    </Fragment>
  );
}

export default App;
```

#### Pasar datos entre componentes

En _React_, los datos fluyen desde el componente principal hacía los componentes hijos, lo anterior es posible gracias al uso de **_props_**. Los _props_ son similares a un atributo del HTML que se le asigna al componente. La extensión _React Developer Tools_ permite ver el árbol de componentes del proyecto, además de los props que se entregan de padre a hijo. React utiliza una sintaxis llamada JSX, lo cual es como una combinación de HTML y JS, donde todo lo que se encuentra entre `{}` es JavaScript mientras que lo demás es HTML. Cabe mencionar que es posible el destructuring de props en los argumentos de las funciones de los componentes, lo cual sirve para codificar de manera más semantica los componentes de la aplicación.

```js
// App.js
import React, { Fragment } from "react";
import Header from "./components/Header"

function App() {
  return (
    <Fragment>
      {/* Los props se pasan como atributosd de HTML al componente */}
      <Header
        titulo="Cotizador de Prestamos"
        descripcion="Utiliza el formulario y obtén una cotización"
      />
    </Fragment>
  );
}

export default App;

/*-------------------------------------------------------------------------*/

// Header.js
import React, { Fragment } from 'react';

function Header(props) {
// function Header({titulo, descripcion}) {

    /* Entre la declaración de la función y el return
     se puede colocar código standard de JS */

    console.log(props)

    return(
        <Fragment>
            {/* Dentro de las llaves, lo que hay
            es código JS */}

            {/*<h1>{ titulo }</h1>*/ }
            {/*<p>{ descripcion }</p>*/}
            <h1>{ props.titulo }</h1>
            <p>{ props.descripcion }</p>
        </Fragment>
    )
}

export default Header;
```

#### Segunda forma de escribir componentes funcionales

La primera opción de creación de componentes es mediante _Function Delcaration_, muientras que la segunda es con _Function Expresion_, lo cual permite crear componentes con menos líenas de código, sin embargo, al quitar el return, se pierde el espacio para escribir código JS dentro del componente.

```js
const Header = ({ titulo, descripcion }) => ( 
        <Fragment>
            <h1>{ titulo }</h1>
            <p>{ descripcion }</p>
        </Fragment>
     );

export default Header;
```

#### Class vs ClassName 

Es importante saber que en React, la asignación de clases se hace utilzando el atributo `className`, no `class` como se hace en HTML.

#### useState

Las aplicaciones de React suelen ser rápidas gracias al manejo del _state_, el cual se importa desde la librería de React utilizando añadiendo lo siguiente a la importación de React `{useState}`.

Usualmente, cada pieza interactiva de la aplicación tiene un state asociado.

Para usarlo, se debe definir un array destructurting de los valores que entrega useState, esos valores serían una variable que contiene el valor y una función que será utilzada para estar interactuando y guardando lo que es el state que se está creando.

Hay que mensionar que `useState()` permite el ingreso de un valor por default el cual se le asigna al estado inicial de la variable.

Es importante tener claro donde se definiran los estados, ya que si se quieren pasar los valores entre componentes, siempre hay que tener en cuenta que los props pasan de un padre a un hjio pero no pueden pasar de un hijo a un padre. Al parecer lo ideal es definir los estados en el padre (se podría decir que el mejor lugar es el componente principal o el componente que contenga todos los demás) con el fin de poder utilizarlos en sus distintos hijos.

#### Eventos en React

A diferenmcia de JS donde era necesario seleccionar el elemento antes de añadirle un evento, en React por defecto viene una gran cantdiad de eventos que se integran a los elementos como si de una atributo de HTML se tratase. Se recomienda no utilizar la función que entrega `useSatet()` dentro de otra función la cual sería llamada (sin sus parentesis) por el evento definido en el componente, de todas formas se puede ingresar la función directamente en el evento siempre y cuando la función sea corta, de una línea por ejemplo.

#### Carga condicional de componentes

La carga condicional de componentes hace referencia a que mediante el uso de condicionales en el área de código JS de los componentes, se puede utilizar una variable que almacenará cierto componente dependiendo de ciertas condiciones previamente establecidas, como por ejemplo, la carga condicional de componentes que dependa del tipo de usuario que ingresa a la página.

```js
// Carga condicional de componentes
    let variableComponent;

    if(totalPay === 0) {
        variableComponent = <Message/>;
    } else {
        variableComponent = <LoanInfo 
                                loan={loan}
                                deadLineValue={deadLineValue}
                                monthlyPay={monthlyPay}
                                totalPay={totalPay}
                            />
    }
```

Los componentes condicionales puede ir de la mano con los estados boleanos que se pueden crear utilizando `useState()`.

##### Ideas y Anotaciones

- Se puede agregar elementos condicionales al HTML utilizando estados booleanos, además se puede reducir código utilizando el operador ternario.

    ```js
    // Si errorState es true, se muestra un mensaje de error
    { (errorState) ? <p className="error">Todos los campos son obligatorios</p>: null }
    ```

- Hay que tener en consideración de que si un componente en React tiene más de 100 líneas, se puede considerar necesaria la división del mismo o ver que código puede ser refactorizado.

### VueJS: Aprende Creando un Proyecto

#### Introducción

Se recomienda instalar la extensión oficial de vue desarrollada por el Vue team.[Vue Language Features (Volar)](https://marketplace.visualstudio.com/items?itemName=Vue.volar)

Junto a la anterior se recomienda instalar [Vue de Rahul Kadyan](https://marketplace.visualstudio.com/items?itemName=znck.vue)

Para crear un proyecto, se recomienda utilizar vite con el comando `npm init vite@latest`, se eligen las configuraciones y después de instalan las dependencias con el comando `npm install`

Mayoritariamente el código se escribirá en la carpeta src (como en react). También tiene un archivo principal llamado `App.vue`, además de un archivo `main.js` que monta el componente app al DOMm de la aplicación.

#### Single File Components en Vue.js

Utiliza la convención SFC (Single File Components) en la cual cada componente tiene 3 partes: `<script>` `<style>` y `<template>`.

* **`<script>`:** Se coloca toda la lógica de JS del componente. 
* **`<style>`:** Se coloca todo el código CSS del componente. Estos estilos al llevar la palabra **scoped**, aplican solo al componente, si se quitá, aplica a otros componente.
* **`<template>`:** Se coloca todo el código HTML del componente.

No es obligatorio tener los 3 pero en generAL SFC es la convención para escribir componentes en Vue.

#### Instalación Tailwindcss

Para integrar tailwindcss con proyectos de Vue o React, se recomienda utilizar el siguiente comando `npm install -D tailwindcss postcss autoprefixer`.

Una vez instalados los paquetes anteriores, se deben realizar las siguientes pasos para configurar tailwind en el proyecto:

1. Ejecutar el comando `npx tailwindcss init -p` para generar 2 archivos de configuración **postcss.config.cjs** y **tailwind.config.cjs**

2. Dentro del archivo **tailwind.config.cjs** se debe realizar las siguientes configuraciones:
```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [
    "./index.html",
    "./src/**/*.{vue,js,ts,tsx}"
  ],
  theme: {
    extend: {},
  },
  plugins: [],
}
```

3. En el archivo css principal (**style.css**) se deben colocar las directivas de tailwind con el obejtivo de indicarle al proyecto que queremos utilizar tailwindcss:
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```

#### Componentes en Vue.js

* Al igual que en React, los componentes permiten dividir el código en partes reutilizables.

* Los componentes utilizan la extensión **.vue** y se importan con un import de JavaScript dentro de la etiqueta **`<script>`**.

* Con la etiqueta **`<script setup>`** cualquier componente que es importado se hace disponible en el template.

* Se puede pasar información de un componente a otro mediante el uso de Props.

#### API Styles en Vue - Options API y Composition API
En el caso de **Options API** se utiliza una sintaxis de tipo objeto, mientras que en **Composition API** se definen los componentes utilizando imports y escribiendo las funciones directamente en el componente (el utilizar la palabra setup en la etiqueta script, indica que se utiliza esta API).

El siguiente es un ejemplo de **Options API**:

```js
<script>
    import Component from './components/Component.vue'

    export default {
        components: {
            Component
        },
        data: {

        }
    }
</script>
```

Se recomienda utlizar **Options API** cuando se está comenzando a aprendar Vue, además es la opción recomendada para personas con más experiencia en lenguajes orientados a objetos. El mejor escenario para utilizar esta API es cuando el proyecto a realizar utilizará pequeñas piezas de Vue o escenarios no tan complejos.

En el caso de **Composition API**, es recomenddo su uso si todo el proyecto será hecho con Vue.js

#### Eventos en Vue

Los eventos en Vue.js se agregan con la directiva `v-on:evento` aunque usualemnte se recomienda la sintaxis corta de `@evento`.

Un ejemplo con la sitaxis completa sería el siguiente:
```js
<div class="my-5">
      <input 
        type="range" 
        name="" 
        id="" 
        className='w-full h-6 bg-gray-200 accent-lime-500 hover:accent-lime-600 mt-5'
        v-on:input="handleChange"
      />
</div>
```

En el ejemplo anterior, cada ingreso de data que recibe el input range es manejado por la función `handleChange` que por ahora hace lo siguiente:

```js
const handleChange = (e) => {
    console.log(e.target.value);
  }
```

Con la versión corta, el evento quedaría de la siguiente manera:

```js
<div class="my-5">
      <input 
        type="range" 
        name="" 
        id="" 
        className='w-full h-6 bg-gray-200 accent-lime-500 hover:accent-lime-600 mt-5'
        @input="handleChange"
      />
</div>
```

El resultado es el mismo en ambos casos, sin embargo, para los eventos, la sintaxis corta es la más recomendada.

#### Reactive y Ref

El state es la fuente de la verdad (source of truth) de la aplicación. Un ejemplo de state sería un carrito de compras, la autenticación de un usuario o un listado de clientes.

Vue.js maneja y actualiza el state en base a ciertas funciones o condiciones en el código.

En Vue existen dos formas sencillas de manejar un state, esto se hace con la función **`ref`** y **`reactive`**, ambos se importan desde vue. La diferencia entre ambas radica en que **`ref`** toma valores primitivos mientras que **`reactive`** toma objetos.

En un equipo de trabajo o un proyecto grande se recomienda administrar el state con una herramienta llamada Pinia (sutituto de VueX)

####  Modificación del state

##### Ref

Tal como los objetos en JS, en el caso de ref se reasigna el valor del **.value** con el valor de interés como se muestra en el siguiente código:

```js
const handleChange = (e) => {
    cantidad.value = +e.target.value;
    console.log(cantidad.value)
}
```

**Nota:** Para utilizar una variable dentro del template, se debe colocar dentro de dobles llaves **{{variable}}**

##### Reactive

Similar a ref, aquí se le asgina el valor directamente al atirbuto de interés.

```js
const handleChange = (e) => {
    state.cantidad = Number(e.target.value);
    console.log(state.cantidad)
}
```

#### Mostrar el state en pantalla

La forma más sencilla es la de utilizar la sintaxis de doble llave **{{variable}}**, sin embargo también se pueden utilizar las directivas de vue **v-text** o **v-html**. Nuestra atención se centra en **v-text** que se utiliza de la siguiente manera:

```js
<p
      class='text-center my-10 text-5xl font-extrabold text-indigo-600'
      v-text="cantidad"
    >
</p>
```

Hay que tener en consideración que si se quiere agregar otro tipo de texto como lo sería un signo de pesos, habría que hacer lo siguiente:

```js
<p
      class='text-center my-10 text-5xl font-extrabold text-indigo-600'
      v-text="`$ ${cantidad}`"
    >
</p>
```

#### Atributos dinámicos en Vue.js

Para indicar que un atirbuto es dinámico, se colocan dos puntos antes del atributo, lo cual indicará que se debe ir a buscar una variable o una función con el nombre que se dará como valor al atributo.

```js
<div class="my-5">
      <input 
        type="range" 
        name="" 
        id=""
        class='w-full h-6 bg-gray-200 accent-lime-500 hover:accent-lime-600 mt-5'
        :min="MIN"
        :max="MAX"
        :step="STEP"
        :value="cantidad"
        @input="handleChange"
      />
</div>
```

Es importante destacar que en el caso del valor, con el sólo hecho de colocar el state que se definió es suficiente para que se haga la conexión entre el valor el valor del input y el valor del state, por lo cual **NO** se debe poner **cantidad.value**, ya que, eso causa errores en la rendericación del componente.

#### La directiva v-model

Permite realizar la actualización de un estado desde un input y la asginación del state al value del input.

```js
<div class="my-5">
      <input 
        type="range" 
        name="" 
        id=""
        class='w-full h-6 bg-gray-200 accent-lime-500 hover:accent-lime-600 mt-5'
        :min="MIN"
        :max="MAX"
        :step="STEP"
        v-model="cantidad"
      />
</div>
```

El código anterior lo que hará será modificar el state cantidad cuando el input cambié, sin embargo, los valores que se asignarán serán en string,, debido a lo anterior es que existen los modificadores los cuales permitirán cambiar el tipo del valor que se le asignará al estado.

```js
<div class="my-5">
    <input 
    type="range" 
    name="" 
    id=""
    class='w-full h-6 bg-gray-200 accent-lime-500 hover:accent-lime-600 mt-5'
    :min="MIN"
    :max="MAX"
    :step="STEP"
    v-model.number="cantidad"
    />
</div>
```

#### Computed Properties en Vue.js

Es una función que está pendiente de los cambios de tu state y realiza los cambios necesarios cuando este cambia. La idea es utilizarlas con el fin de que el código sea ordenada y se sigan teniendo actualizaciones de código. Se considera buena práctica agregar la función al código de Vue.js con esta función.

Para hacer uso de estas propiedades, se debe importar desde vue la función **computed**.

```js
<script setup>
  import { computed } from 'vue';

  // Definición de state con ref
  const cantidad = ref(10000);

  const formatearDinero = computed( () => {
    const formatter = new Intl.NumberFormat('en-US', {
        style: 'currency',
        currency: 'USD'
    });
    return formatter.format(cantidad.value);
});
</script>
```

Esta opción es recomendada cuando se trata de funciones que muestran algo, en cambio, no se recomienda para las funciones encargadas del manejo de lógica como lo sería el manejo de un evento.

#### Pasando props a un componente

Para pasar props a un componente en Vue se utiliza la misma sintaxis que utilizan los atributos dinámicos y entre las comillas dobles se le proporciona JavaScript, esto último hay que tenerlo en consideración, ya que, en casos donde se quiera enviar elementos reservados en JavaScript como lo serían un signo más por ejemplo, hay que mandarselo en formato string **'+'**.

```js
<Button
    :tipoBoton="'button'"
    :contenidoTexto="'-'"
    :handle="handleDecremento"
/>
```

Desde el componente en la zona del script se importan las props de dos maneras, ambas utilizando `const props = defineProps()` pero se diferencian en lo que reciben:

1. **Arreglo con los nombres de los props:** Tal como lo dice el nombre, en estos casos `defineProps()` recibe un arreglo con los nombres de los props que recibe el componente, generando un objeto que como atributos tiene los props definidos.

```js
<script setup>
    const props = defineProps(['tipoBoton', 'contenidoTexto', 'handle'])
</script>
```

2. **Objeto con los nombres de los props:** En este caso se le pasa un objeto que como llaves tendrá los props que se le quieren pasar al componente y como valores los tipos que tendrán cada llave. En el caso de no entregar un elemento con el tipo definido, se muestra una advertencia en la consola de comandos.

```js
<script setup>
    const props = defineProps({
        tipoBoton: String, 
        contenidoTexto: String, 
        handle: Function
    })
</script>
```

Para hacer uso de los props dentro del componente, sólo se llaman por el nombre, como si ya se hubiera hecho el destructuring del objeto props.

```js
<template>
    <button
        :type="tipoBoton"
        className='h-10 w-10 flex items-center justify-center font-bold text-white text-2xl bg-lime-500 rounded-full hover:ring-2 hover:ring-offset-2 hover:ring-lime-500'
        @click="handle"
    >
    {{contenidoTexto}}
    </button>
</template>
```