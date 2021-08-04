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

ambos métodos sirven para encontrar una valor en un arreglo. Sin embargo, _.includes()_ sirve sólo para arreglos de indices, en cambio, _.some()_ es tanto para arreglos de indices como para arreglos de objetos. Por otro lado, ambos métodos se diferencian con respecto al parámetro que reciben, por un lado _.includes()_ recibe el valor que se está buscando en el arreglo, mientras que _.some()_ recibe una _Arrow Function_ la cual se encarga de recorrer el arreglo (de indice u objetos) y buscar un valor, la estructura de la _Arrow Function_ es similar a la de un _.forEach_ o un _.map_, en donde el cuerpo de la función se compone de un _return_ seguido por lo que se está buscando.

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

#### .findInde para encontrar la posición en un array

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