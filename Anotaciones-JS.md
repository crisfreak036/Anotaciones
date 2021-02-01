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

Sirve para conocer la cantidad de carácteres que componen a un string. 

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

El método *toUpperCase()* sirve para transformar en mayúscula todos los carácteres de una cadena de texto contenida en una variable.

##### Convertir en minúsculas

El método *toLowerCase()* sirve para transformar en minúscula todos los carácteres de una cadena de texto contenida en una variable.

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
