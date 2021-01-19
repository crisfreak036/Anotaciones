
# Anotaciones del curso Conviértete en desarrollador web full-stack de LinkedIn

## Aprende Visual Studio Code

### Diferencias entre un editor de texto y un IDE

- Los editores de textos contienen herramientas como un bloc de notas con estaminas.
- Los IDE son entornos integrados de desarrollo.

La diferencia más grande entre ambos radica en la cantidad de herramientas con las cuales se va a desarrollar. Los IDE vienen con todas las herramientas precargadas en cambio los editores de texto no vienen con todas las herramientas, hay que ir instalándolas según se vayan necesitando.

### Componente comunes adicionales de Visual Studio Code 

Los siguientes son programas a instalar necesarios para un mejor trabajo con VSC. Se recomienda ie a los sitios específicos de cada software para su correcta instalación.

- Git
- Node.js
- Typescript
- Typings

### Extensiones en VSC

Las siguientes son extensiones recomendadas para VSC.

- vscode-icons
- ESLint
- HTML Snippets
- Beautify

### Autoguardado en VSC

Se debe ir a archivo y presionar en *Autoguardado*.
También se puede ir a preferencias, configuración, buscar *files.autosave* y configurar el delay con el que se quiere que se autoguarde el archivo.
En las opciones de autoguardado desde preferencias existen los siguiente tipos:

- **afterDelay:** Se guarda luego de un intervalo de tiempo previamente establecido.
- **off:** El autoguardado está desactivado. 
- **onFocusChange:** Se guarda luego de que cambiamos de pestaña.
- **omWindowChange:** ¿Se guarda al cambiar de ventana?

Cabe mencionar que para que beautify permite una opción que formatea el código cada vez que guardemos el mismo.

### Zoom en VSC (Atajos en VSC)

Se recomienda ir a Archivo, Preferencias, *Métodos abreviados de teclado* con el fin de saber los atajos de teclado configurados ene l dispositivo, esto se recomienda debido a que no en todos los dispositivos tienen los mismos comandos.

### Búsqueda y reemplazo de código en VSC

Para iniciar la búsqueda de código se puede utilizar el comando *CTRL + F* en windows (*CMD + F* en MAC) o bien ir a Editar y presionar en *Buscar*.
Ya hecho lo anterior, en la barra de búsqueda existe la opción de que el buscador considere las mayúsculas o no lo haga. Sumado a lo anterior existe la búsqueda a través de **expresiones regulares**, ejemplo: buscar *view[]* que sirve para ver todos los view con números que hayan en el código. En la misma barra de búsqueda en el lado izquierdo existe una punta de flecha que al presionarla da la opción de reemplazar por algo los resultados de la búsqueda que se hizo previamente, ya sea uno por uno o todos a la vez.

También se pueden hacer búsquedas en una selección de texto, seleccionamos el texto, presionamos *CTRL + F*, presionamos la opción de *Buscar en selección o ocupamos el comando ALT + L* y procedemos a escribir lo que queremos buscar en la barra de búsqueda. Luego de esto se puede hacer todo lo que se describió para la búsqueda global anteriormente.

Al igual que se pueden realizar búsquedas por archivos, también se pueden hacer en una carpeta, para hacer esto hay que presionar click derecho en la carpeta y presionar la opción *Buscar en carpeta*, luego aparecerán opciones como las que nos da la barra de búsqueda.

### Pistas y atajos rápidos en VSC

Permite buscar código y editarlo sin necesidad de desplazarse al bloque de código en cuestión.

Se de poner el cursos sobre lo deseado y presionar la combinación de teclas *Shift + F12 o ALT + F12* lo que mostrará una ventana que muestra todas las referencias que se hacen a lo deseado (por ejemplo una función). Lo que se abre es como un espacio virtual que permite la edición de lo que aparecé dentro de ella. Para cerrar la ventana hay que presionar la x.

### Paleta de comandos

*CTRL + P* abre la barra de comandos, poniendo un *?* mostrará las opciones que se pueden utilizar.
Poniendo un *@* aparecerán todas las funciones que existan en el código.
Poniendo *#* y algo más, mostrará lo que se puede buscar.

### Errores y warnings en VSC

AL presionar el juego de teclas *CTRL + SHIFT + M* mostrará una ventana con los errores que existan en el archivo.
Otra manera que hay para trabajar con los errores es presionar la tecla *F8* y mostrará una ayuda visual que dice cual es el error que hay en la línea que presenta el error. *F8* recorrerá el archivos buscando error por error y mostrando la ayuda visual error por error.

### Refactoring de código con VSC

- **Mover una línea:** Para mover una línea, se debe poner el cursor en la línea deseada, luego presionar la tecla *ALT* y con lasa flechas mover la línea hacía arriba o hacía abajo.

- **Encontrar una función:** Una función se puede encontrar desde su llamado dejando el cursor en su llamado y luego la tecla *F12*. También se puede presionar la tecla *CTRL* mientras se pasa el cursos sobre el llamado de la función lo que hará que se vuelva como un hipervínculo que direcciona a la función en cuestión, al momento de pasar el cursor sobre el llamado de la función se mostrará su estructura.

- **Seleccionar un trozo de texto en todos los lugares del código:** Por ejemplo, se selecciona una variable y luego se presiona *CTRL + D*, se seleccionará la variable en todos los lugares del código donde aparece, luego de esto se puede cambiar donde se seleccionó y el cambio se hará en todo el código. Cabe mencionar que los cambios se pueden hacer en cualquier lugar de lo seleccionado gracias a un multicursor que se posiciona en todas las selecciones.

### Debbuging: ELiminar errores en VSC

Lo primero que se debe hacer es ir al menú de deugging, luego levantar la configuración (tipo de tuerca con punto rojo en la parte superior) con el entorno que se desea, lo anterior creará un archivo y una carpeta en el directorio donde se encuentre el código. Luego de hay que volver a la ventana de depuración y presionar el ícono de play. Se abre (o hay que abrir) una consola que mostrará si hay algún error o cosas por el estilo. Se pueden agregar breakpoints que permite ejecutar ciertas secciones de código.

### Uso de Git en el editor de código de VSC

En la barra lateral izquierda hay un icono que hace alusión a Git. Dentro de ella hay una paleta de comandos que se utilizan con Git. También, si se presiona sobre algún archivo se puede ver los cambios que se han hecho. Instalando la extensión *Git History*, al presionar botón derecho en el archivo se pueden ver los commit que se han hecho y el estado del archivo en aquel commit con el objetivo de comparar la versión actual con la versión del archivo en aquel commit.

### Personalizar el teclado y el editor de VSC

Para personalizar los atajos, hay que ir a archivos, luego preferencias y después a *Métodos abreviados de teclado*, se abrirá una pestaña con todos los comandos que hay, se pueden editar todos.

## JavaScript Esencial

La primera capa **(Marcado HTML: capa de contenido)** de una página web es HTML el cual sólo da estructura.
La segunda capa **(Reglas CSS: Capa de presentación)** de una página web es CSS y se enfoca en como se verá el contenido.
La tercera capa **(Javascript: Capa de presentación)** de una página web es Javascript, el cual es un lenguaje interpretado que se ejecuta en el navegador e interactúa con las capas de HTML y CSS, manipulando e interactuando con el contenido.

### Conociendo JavaScript

#### Strict Mode (Modo estricto)

Sirve para asegurar que el código de JS que se está escribiendo, está siendo correcto y no se están cometiendo errores como la utilización de palabras reservadas o la no declaración de una variable, etc.

Para activarlo hay que dirigirse al archivo JS y poner lo siguiente:

```js
"use strict" // Activa el modo de estricto, debe estar al inicio del código
```

### Variables

#### Trabajando con variables en JS

Es una manera con la cual se almacenarán datos dentro de la aplicación.

```js
// Ejemplo 1
var nombre = 'Algo'; // Variable de tipo Global
console.log(nombre); //Muestra el contenido de la variable nombre
var nombre = 'Algo2'; // Cambia el contenido de la variable nombre declarada de manera global
console.log(nombre); // Muestra el nuevo contenido de la variable nombre 
```

Se recomienda el uso del contenedor VAR en variables globales

```js
// Ejemplo 2
var nombre = 'Algo'; // Variable nombre declarada de forma global
console.log(nombre); // Muestra el contenido de nombre por consola
function saludo() {
    var nombre = 'Algo 2'; // Variable nombre declarada de forma local
    console.log(nombre); // Muestra el contenido de nombre por consola
}
saludo(); // Llama a la función saludo()
console.log(nombre); // Muestra el contenido final que tiene la variable nombre. En este caso no se ve afectada la variable nombre global por la función saludo().
```

#### Contenedores Let

Se recomienda su uso dentro de funciones para variable locales.

```js
var nombre = 'Pedro';
function saludo() {
    let nombre = 'Algo 2'; // Variable nombre declarada de forma local
    console.log(nombre); // Muestra el contenido de nombre por consola
}
saludo(); // Llama a la función saludo()
console.log(nombre);
```

#### Contenedores Const

Este contenedor es para las variables que se mantendrán constantes y nunca cambiarán,por lo cual cualquier variable que sea declarada con este tipo de contenedor, su valor no podrá ser modificado de ninguna forma mientras la aplicación se esté ejecutando.

```js
const constante1 = 34;
console.log(constante1);
const constante1 = 35; // Lanzará un error porque no se puede cambiar el valor de la variable constante1
console.log(constante1); 
```

### Tipos de Datos 

#### Trabajar con números en JavaScript

No se escriben con comillas a diferencia de los strings. Pueden ser flotantes (decimales) y con negativos al igual que con positivos.
En el caso de que se tenga un número escrito como cadena de caracteres, existe una función que convierte los números de tipo string a número matemáticamente trabajable, la función es ***Number()***.

```js
let valor1 = 34; // La variable valor1 contiene un entero
console.log(valor1);
let valor2 = '100' // La variable valor2 contiene un número que está como cadena de caracteres
console.log(valor2);
let nuevoValor2 = Number(valor2); // nuevoValor2 contiene la versión numérica de valor2
console.log(nuevoValor2);
```

A su vez existen dos funciones que sirven para transformar un número escrito en cadena de carácteres en número trabajable, ya sea, entero (*parseInt()*)o flotante (*parseFloat()*).

```js
let valor1 = '100';
let valor2 = '12.5';
let nuevoValor1 = parseInt(valor1); //Transforma a entero el contenido de valor1
let nuevoValor2 = parseFloat(valor2); //Transforma en flotante el contenido de valor2
```

#### Trabajar con cadenas de texto o String 

Para definir una cadena de texto, se el contenido se puede poner entre comillas simples o comillas simples pero **no las dos combinadas alternandose entre simples al inicio y dobles al final o viceversa**.

```js
let variable1 = "texto1";
let variable2 = 'texto2';
let variable3 = 'Pedro tenía un "pequeño" problema'; //Se pueden utilizar dentro del contenido las comillas contrarias de las cuales se utilizan para declarar
```

Al igual que los números de tipo String se pueden transformar a valor numérico, existe una función que transforma los valores numéricos a strings y es *String()*.

```js
let numero1 = 45;
let texto1 = String(numero1); //Transforma el valor numérico de numero1 en un string
```

#### Uso de los datos booleanos

Los datos Booleanos aceptan sólo dos valores *true* o *false*.

```js
let verdadero = true;
let falso = false;
```

Para obtener el booleano de algo se puede utilizar la función *Boolean()* la cual arrojará el true o false correspondiente a lo que se le entregue.

```js
let estado = Boolean(14 > 9);
console.log(estado);
```

#### Trabajar con fechas en JavaScript

En JS se puede trabajar con fechas, lo anterior es posible gracias al objeto *Date()*. El objeto en cuestión se crea de la siguiente forma: 

```js
let fecha = new Date(); //Al declararla de esta forma, fecha guardará los valores de la fecha de creación de la variable 
console.log(fecha);
```

La manera anterior lo que hace es crear un objeto del tipo *Date()* que guarda los parámetros de la fecha al momento de ser creado.

Los objetos del tipo *Date()* cuentan con una serie de métodos los cuales son:

```js
let fecha = new Date()

fecha.getDay() //Entrega el día de la semana en la que se encuentra la fecha actualmente
fecha.getDate() //Entrega el día del mes en el cual uno se encuentra actualmente
```

Lo anterior son ejemplos de los tipos de método *get* que tiene la clase *Date()*.

Para poder establecer valores a la variable fecha se debe setear la información con los métodos *set()*. Ejemplo de lo anterior son los siguientes:

```js
fecha.setDate() //Hace que la fecha apunte a un día en especifico 
fecha.setMonth() //Hace que el mes apunte a un día en especifico
```

Lo anterior son ejemplos de los tipos *set* que tiene la clase *Date()*.

#### Uso de símbolos en JavaScript 

Son un tipo de dato que sus valores son únicos e inmutables por lo cual no cambiarán a lo largo del programa. Estos valores puede ser utilizados ya sea con identificadores clave, como si fuera una propiedad del objeto, es decir, cuando creemos un símbolo podemos asignarle un nombre o podemos asignarlo a una variable. Así, entonces, cada uno de estos tendrá un valor de tipo *symbol* o símbolo, por lo cual este dato va a ser único completamente a lo largo de todo el programa.

```js
let simbolo1 = Symbol(); //No es un constructor de objeto
// new Symbol() tira error
```

Cada vez que se crea un símbolo se crea una nueva variable única y diferente a otra, da igual que 2 variables de tipo *symbol* sean declaradas de la misma forma ya que serán distintas.

```js
let simbolo = Symbol();
let simbolo1 = Symbol();
console.log(Boolean(simbolo1 == simbolo2)); //Arroja un false
```

#### Estructurando datos con JSON

En JS se puede trabajar con objetos que permiten estructurar de mejor manera los datos con los cuales se estarán trabajando a lo largo de una aplicación. JSON en sus iniciales significa *JavaScript Object Notation*, el cual es un formato de intercambio de datos bastante ligero y es bastante descriptivo, esto se debe a que utiliza la estructura de un objeto. Con un JSON establecido, aunque directamente no se reciba un JSON, el dato se puede convertir a uno.

```js
//Declaración de una estructura JSON con datos
let persona = {nombre: 'Juan', twitter: '@juan'};
console.log(persona.nombre); //Muestra el nombre de la variable persona
console.log(persona.twitter); //Muestra el twitter de la variable persona

//Declaración de un arreglo de estructuras JSON con datos
let personas = [
    {nombre: 'Juan', twitter: '@juan'},
    {nombre: 'Pedro', twitter: '@pedro'},
    {nombre: 'Simón', twitter: '@simon'}
];

console.log(personas[0]); //Muestra la información del lugar 0 del arreglo personas
console.log(personas[2].nombre); //Muestra el contenido del nombre de lo que se aloja en el lugar 2 del arreglo
```

Para utilizar los datos y enviarlos a un servidor o almacenarlos localmente, se debe convertir los datos  utilizando métodos del objeto *JSON*.

```js
//Convertir un objeto JSON a cadena de caracteres 
let persona = {nombre: 'Juan', twitter: '@juan'};
let personaJSON = JSON.stringify(persona) //Transforma el JSON persona a una cadena de texto (ya no es un objeto con metodo GET)
```

Al igual que se puede transformar un JSON en cadena de texto, las cadenas de texto se (con estructura de JSON) se pueden transformar en un objeto JSON.

```js
//Convertir una cadena de texto a objeto JSON
let personaJSON = '{"nombre":"Juan","twitter":"@juan"}';
let nuevaPersona = JSON.parse(personaJSON); //Convierte la cadena texto en un objeto JSON
```

JSON es la manera ideal para que podamos intercambiar datos, ya sea en nuestra aplicación o con servicios externos.

### Operadores

Los operadores son aquellos recursos de JS que permitiran la realización de distintas operaciones

#### Operadores aritméticos

Existen de Suma *(+)*, Resta *(-)*, Multiplicación *(\*)*, División *(/)*, Modulo o Residuo *(%)*, Incremento *(++)* y Decremento *(--)*.

```js
"use strict"
var datoA = 10;
var datoB = 20;

// SUMA +
var suma = datoA + datoB;
console.log('La suma de '+ datoA +' + '+ datoB +' es igual a: ', suma); //Cuando + se ocupa fuera de una operación matemática, el + sirve para concatenar

// RESTA -
var resta = datoA - datoB;
console.log('La resta de '+ datoA +' - '+ datoB +' es igual a: ', resta);

// MULTIPLICACIÓN *
var multiplicacion = datoA * datoB;
console.log('La multiplicación de '+ datoA +' * '+ datoB +' es igual a: ', multiplicacion);

// DIVISIÓN /
var division = datoA / datoB;
console.log('La división de '+ datoA +' / '+ datoB +' es igual a: ', division);

// MODULO O RESIDUO % (Lo que sobra de realizar la división)
var modulo = datoA % datoB;
console.log('El módulo o residuo de '+ datoA +' % '+ datoB +' es igual a: ', modulo);

// INCREMENTO ++
var incremento = datoA; //incremento = incremento+1
console.log('El incremento ++ de '+ datoA +' es igual a: ', incremento);


// DECREMENTO --
var decremento = datoA;
decremento--; //decremento = decremento -1
console.log('El decremento -- de '+ datoA +' es igual a: ', decremento);
```

#### Operadores Ralacionales

Permiten la validación o la definición de relaciones entre dos entidades. El uso de estos operadores implica que lo que retornen sea un *true* o un *false*.

```js
"use strict"
var datoA = 10;
var datoB = 20;

// MAYOR QUE >
var mayorQue = datoA > datoB;
console.log("Es "+ datoA + " mayor que " + datoB + ": " + mayorQue);

// MENOR QUE <
var menorQue =  datoA < datoB;
console.log("Es "+ datoA + " menor que " + datoB + ": " + menorQue);

// MAYOR O IGUAL QUE >=
var mayorOIgualQue =  datoA >= datoB;
console.log("Es "+ datoA + " mayor o igual que " + datoB + ": " + mayorOIgualQue);

// MENOR O IGUAL QUE <=
var menorOIgualQue =  datoA <= datoB;
console.log("Es "+ datoA + " menor o igual que " + datoB + ": " + menorOIgualQue);

// IGUAL QUE ==
var igualQue =  datoA == datoB;
console.log("Es "+ datoA + " igual que " + datoB + ": " + igualQue);

// NO ES IGUAL QUE O ES DIFERENTE QUE !=
var noEsIgualQue =  datoA != datoB;
console.log("Es "+ datoA + " no es igual o es diferente que " + datoB + ": " + noEsIgualQue);
```

#### Operadores Lógicos

Sirven para combinar la evaluación de dos o más condiciones y ,de hecho, también se utilizarán aquí los operadores relacionales. Este tipo de operadores lógicos, una vez que son evaluados, regresan un valor *booleano*, es decir, *true* o un *false*. Los operadores que existen son: AND *(&&)* el cual implica que se cumplan todas las condiciones anidadas para que arroje un *true*, OR *(||)* implica que se cumpla al menos una condición para que sea *true* y NOT *(!)* el que implica que se niega lo que lo acompaña.

```js
var datoA = 10;
var datoB = 20;

// OPERADOR Y o AND - && 
var and = (datoA > 10 && datoB > 10) //Arroja true sólo si se cumplen ambas condiciones
console.log('El resultado de la evaluación AND es: ' + and);

// OPERADOR O u OR - ||
var or = (datoA > 10 || datoB > 10); //Arroja true si una de las dos condiciones se cumple
console.log('El resultado de la evaluación OR es: ' + or);

// OPERADOR DE NEGACIÓN o NOT - !
var not = !(datoA > 10) //Arroja lo contrario a lo que retorna la operación racional entre paréntesis
console.log('El resultado de la evaluación NOT es: ' + not);
```

#### Operadores de Asignación

Son aquellos operadores que permiten guardar resultados de una evaluación, de una operación o, incluso, solamente un valor dentro de una variable. Existen 5 tipos de asignación los cuales son: 

- **Asignación Simple:** Donde se utiliza sólo el igual *"="*.
```js
let variable = 10;
``` 
- **Sumar y Asignar:** Se utiliza un *"+="*.
```js
let variable = 5;
let masIgual = 10;
masIgual += variable; //A masigual se le suma el valor de la variable y luego se le asigna ese nuevo valor

/*Lo anterior es equivalente a hacer 
masIgual = masIgual + variable 
pero de manera más acotada*/
```

- **Restar y Asignar:** Se utiliza el *"-="*.

```js
let variable = 5;
let menosIgual = 10;
menosIgual -= variable; //A menosIgual se le resta el valor de la variable y luego el resultado se asigna a menosIgual
```

- **Multiplicar y asignar:** Se utiliza el *"\*="*.

```js
let variable = 5;
let porIgual = 10;
porIgual *= variable; //El valor de porIgual se multiplica por el valor de la variable y luego el resultado se asigna a porIgual
```

- **Dividir y Asignar:** Se utiliza el *"/="*.

```js
let variable = 5;
let entreIgual = 10;
entreIgual /= variable; //El valor de entreIgual se divide por el valor de la variable y luego el resultado se asigna a entreIgual
```

De esta manera, se pueden hacer operaciones aritméticas de una manera simplificada y, a la vez, estar asignando los valores en las variables que corresponden.

#### Operador negativo

Este operador lo que hace es volver negativo el valor positivo de una variable, o sea, pasar de los reales positivos a los reales negativos.

```js
let valor1 = 10;
console.log(valor1);
let valor2 = -valor1; //El valor positivo de valor1 lo vuelve negativo y lo guarda en valor 2
console.log(valor2);
```

#### Operador de Concatenación

El operador de concatenación nos va a servir para poder unir dos textos o unir dos valores. No va a realizar ninguna operación aritmética, a menos que los datos que nosotros estemos uniendo sean números.

- **Concatenación Numérica**
```js
//Concatenación de números (suma)
let datoA = 10;
let datoB = 20;
let concatNumeros = datoA + datoB;
console.log(concatNumeros); //lo que resulta de lo anterior sigue siendo un valor numérico
```

- **Concatenación de Cadenas de texto**
```js
let nombre = 'Sergio';
let apellido = 'Brito';
let concatTexto = nombre + apellido; //Los concatena sin ningún espacio entre medio
console.log(concatTexto);
let concatTexto2 = nombre + ' ' + apellido; //Se agrega un espacio entre ambas cadenas de texto
console.log(concatTexto2); 
```

- **Concatenación de números como texto**
```js
let datoC = '10';
let datoD = '20';
let concatNumComoTxt = datoC + datoD;
console.log(concatNumComoTxt); //lo que resulta de lo anterior es la concatenación de los textos en formato numérico, o sea, 1020. En resumen, no es una operación aritmética. 
```

- **Concatenación de texto y número**
```js
//Si se concatena un número y un texto, el resultado se vuelve un texto.

let datoA = 10; //valor numérico
let datoC = '10'; //cadena de texto
let concatTxtNum = datoA + datoC; //Concatenación
console.log(concatTxtNum);
```

#### Operador Ternario o Condicional

El operador ternario o condicional es un operador compuesto que me va a permitir hacer dos operaciones en una sola. Una de ellas es hacer una evaluación de los datos y, dependiendo de este resultado, hacer la asignación de un valor.

La sintaxis de un operador ternario conociste en una condición *" algo >, = ó < algo2 "*, seguido del símbolo de interrogación *" ? "* . Si esta condición se llega a cumplir, entonces el resultado de si la condición se cumple, iría justo justo después de el signo de interrogación, el cual separaremos del resultado contrario o del resultado utilizando el símbolo de dos puntos *" : "* .

```js
//Ejemplo de un operador ternario

let datoA = 10;
let datoB = 20; 

// let variable = Condición ? TRUE : FALSE 
let resultado = datoA > datoB ? 'Si es mayor' : 'No es mayor';
console.log(resultado);
```
Hay que tener cuidado con el uso de los operadores ternarios, esto es porque si se requiere tomar muchas decisiones, este no será muy útil.

#### Operador de tipo de dato

Bajo ciertas circunstancias necesitarás evaluar el tipo de dato con el cual estás trabajando, porque a veces necesitamos que el dato que estemos almacenando sea un número o una cadena de texto o un valor "booleano". Para esto, nosotros tenemos un operador de tipo de datos. Este operador de tipo de datos se llama `typeof`.

```js
var datoA = 10; // Número

var nombre = "Playa"; // Cadena de texto

var activo = true // Boleano

var persona = {
	edad: 34, // Número
	deporte: 'Correr' // Cadena de texto
} // Objeto

console.log(typeof datoA); //Arroja que es number
console.log(typeof nombre); //Arroja que es string
console.log(typeof activo); //Arroja que es bool

// Muestra el tipo de dato de la variable persona 
console.log(typeof persona); //Arroja que es object

// Muestra los tipos de datos de las propiedades del objeto persona 

console.log(typeof persona.edad); //Arroja que es number 
console.log(typeof persona.deporte); //Arroja que es string
```

### Uso de condicionales o decisiones

Las condiciones o decisiones son mecanismos que ofrece JavaScript para poder tomar –valga la redundancia– una decisión sobre qué flujo se lleva en el programa. Por ejemplo, si tenemos un dato que es válido, entonces podemos hacer determinada cantidad de acciones o determinadas acciones. Al contrario, si este no es válido, entonces se ejecutará o no otro cierto paquete de acciones. Este tipo de estructuras de control te ayudan a organizar el flujo de datos a través de tu aplicación, y esto te va a facilitar mucho más el proceso de desarrollo de una aplicación.

#### Condición if

Para esta estructura se debe escribir la palabra reservada `if` seguida de la condición (que involucrá operadores racionales) entre paréntesis `if(datoA > datoB)`, po último todas las acciones que se quieren ejecutar cuando se cumpla la condición van delimitadas por llaves, pueden ser más de una. Todo lo anterior junto quedará de la siguiente manera:

```js
/*Ejemplo uso del if*/
var datoA = 110;
var datoB = 20;
var resultado = "Sin datos";

if( datoA > datoB ){
    resultado = "La condición se cumplió"; //Si se cumple la condición, resultado se actualizará
} //En el caso que la condición no se cumpla, resultado no se actualizará

console.log("El resultado de la evaluación if es: ", resultado);
```

#### Condición if-else

Es la combinación de la estructura `ìf` sumándole la palabra reservada `else` que establecería que se debe ejecutar en caso de que no se cumpla la condición. Hay que tener claro que `else` no lleva una condición o algo por el estilo ya que en si `else` ya hace referencia a que la condición del `ìf` no se cumplió, o sea, esa es la condición implícita del `else`.

```js
/*Ejemplo uso de if-else*/
var datoA = 10;
var datoB = 20;
var resultado = "Sin datos";

if (datoA > datoB){
	resultado = "La condición se cumplió";
} else {
    resultado = "La condición no se cumplió";
} //A diferencia de el Ejemplo uso del if, este ejemplo establece código a ejecutar en caso de que una condición no se cumpla 

console.log("El resultado de la evaluación if-else es: ", resultado);
```

#### Condición if-else-if

Cuando en un else se quiere poner una condición, se debe poner un `if` seguido del `else` correspondiente al primer `if`. Lo anterior queda de la siguiente manera: 

```js
/*Ejemplo uso de if-else-if*/
let datoA = 30;
let datoB = 20;
let resultado = 'Sin datos';

if (datoA > datoB){
  resultado = 'La primera condición se cumplió';
} else if (datoB == datoA){
  resultado = 'Se cumplió la segunda condición';
} else{
  resultado = 'No se cumplió ninguna condición';
}

console.log('El resultado de la evaluación if-else-if es que:', resultado);
```

Una ventaja de la estructura anterior es que se pueden agregar tantas condiciones como se necesiten pero hay que tener cuidado debido a que la estructura se puede volver muy compleja y extensa por lo cual se recomienda tener bien establecido el flujo de la aplicación.

#### Condiciones anidadas

JS permite estructuras de controla anidadas (al igual que la mayoría de los lenguajes), por lo cual hay que tener bien establecido el flujo de la aplicación para evitar la creación de anidaciones innecesarias.

```js
/*Ejemplo uso de condiciones anidadas*/
var datoA = 110;
var datoB = 20;
var datoC = 5;
var resultado = "Sin datos";

if (datoA > datoB){
  resultado = 'La condición se cumplió';
  /*El if-else que se encuentra aquí está anidado al if inicial*/
  if (datoC < datoB){
    resultado = 'Evaluación anidada se cumplió';
  } else {
    resultado = 'Evaluación anidada no se cumplió';
  }
} else {
  resultado = 'No se cumplió la evaluación';
} //Este es el else del if inicial

console.log("El resultado de la evaluación anidada es: ", resultado);
```

#### JavaScript y la estructura Switch

Cuando las estructuras anteriores se vuelven muy complejas y comienza a existir la necesidad de crear enormes anidaciones, JS entrega la estructura de control `switch (variable a evaluar)` el cual se compone de distintas condiciones los cuales se establecen como casos (`case 10` ó `case 'palabra'`), además esos casos terminan con un `break` que rompé la ejecución del `switch` cuando se cumple una condición y un caso base o default (`default`) el cual contiene la situación de que no se haya cumplido ninguno de los casos establecidos anteriormente. Recordar que toda esta estructura va encerrada entre llaves. Todo lo anterior en estructura de código queda de la siguiente manera:

- **Ejemplo de Evaluación con números**

```js
/*Ejemplo de Evaluación con números*/
// Evaluación con números
var edad = 40;
var resultado = ""; //Es una cadena texto vacía

switch (edad) {
    case 10:
        resultado = "La edad es 10 años";
        /*Dentro de los bloques de código de los casos se pueden agregar más estructuras de control*/
	break;
	case 20:
		resultado = "La edad es 20 años";
	break;
    case 30:
		resultado = "La edad es 30 años";
    break;
    case 40:
		resultado = "La edad es 40 años";
	break;
    default:
    	resultado = "Ningún caso coincide";
    break;
}

console.log("El resultado de la evaluación con números es: "+ resultado);
```

- **Ejemplo de Evaluación con cadena de texto**

```js
var producto = "Radio"; //Si por algún motivo se pone la palabra radio, el swtich arrojará el caso default debido a que se distingue entre mayúsculas y minúsculas

switch (producto) {
    case "TV":
		resultado = "Se eligió la TV";
	break;
	case "Radio":
		resultado = "Se eligió el Radio ";
	break;
    case "Teléfono":
		resultado = "Se eligió el teléfono ";
	break;
    default:
    	resultado = "No se eligió ningún producto";
    break;
}

console.log("El resultado de la evaluación con texto es: "+ resultado)
```

### Ciclos o loops en JS

Los ciclos son estructuras de control bastante sofisticadas, de hecho, nos sirven para estar repitiendo acciones. Nosotros podemos tener distintos tipos de ciclos, pero también a lo largo de todos los lenguajes de programación los podrás encontrar con distintos nombres como ciclos, "loops" o iteradores. De hecho, los ciclos son la manera ideal de estar repitiendo un conjunto de acciones. En este contexto, cada vez que tú tienes una repetición lo podemos conocer como una iteración. Así, nosotros podemos tener identificados dos tipos de ciclos: los ciclos definidos y los ciclos indefinidos. Donde con los ciclos definidos sabemos cuántas veces se va a ejecutar, al contrario, con los ciclos indefinidos no sabemos cuántas veces se va a ejecutar.

Cosas a considerar con respecto a los ciclo: 

- 2 tipos: Definidos e indefinidos
- Definidos: Ciclo FOR
- Indefinidos: Ciclo WHILE y Ciclo DO...WHILE

#### Ciclo for

Es un ciclo definido, para utilizarlo se utiliza la palabra reservada `for` seguida de un par de paréntesis que contendrán un contador (se puede definir y asignar un valor inicial ahí mismo), la condición o evaluación para que se repita y el paso que sería un incrementador o un decrementador, todo lo anterior se separa por punto y coma quedando de la siguiente manera: `for (contador; condición; incremento o decremento)`.

```js
/*Ejemplo ciclo for*/
var productos = 5;

/*Es ciclo for hace las repeticiones mientras que contador sea menor a productos partiendo desde el contador igual 0*/
for (let contador = 0; contador < productos; contador++) {
    console.log("Producto #"+ contador);
    debugger;
}
```

#### Ciclo while 

La estructura de control `while` es un ciclo que me permitirá ejecutar un "set" de instrucciones siempre y cuando una condición en específico se logre cumplir. Este ciclo evalúa antes de ejecutar el bloque de código asignado. La estructura del `while` es la siguiente:

```js
//Ciclo WHILE | Ciclo Indefinido
// Iteración indeterminada o desconocida

var productos = 5; 

while(productos > 0) { 
   	console.log( 'Producto vendido');
   	productos--;
   debugger;
}
```

#### Ciclo do while

El ciclo `do while` no es más que una variante del ciclo `while`, solamente hay una diferencia: dónde nosotros vamos a evaluar la condición. En el caso de `while`, lo primero que hacíamos era preguntar si podíamos ejecutar el conjunto de acciones. Si la decisión era válida, entonces ejecutábamos. En este caso, con `do while` lo primero que hacemos es ejecutar las acciones y después preguntar si podemos continuar ejecutando las acciones. Así que debes tener mucho cuidado con cuál de los dos ciclos vas a ocupar dependiendo del objetivo que busques lograr en el flujo de tu aplicación. La estructura del `do while` es la siguiente:

```js
//Ciclo DO..WHILE | Ciclo Indefinido
//Iteración indeterminada o desconocida

var productos = 5; 

do { 
   	console.log( 'Producto vendido');
   	productos--;
   debugger;
}  while(productos>=1)
```

#### Controlar ciclos en JS (break y continuo)

Los ciclos son tan sofisticados que también nos permiten controlar el flujo que van a tener. Es decir, si yo decido continuar e ignorar cierta cantidad de instrucciones lo puedo hacer. O si simplemente yo decido romper el ciclo y continuar, también lo puedo hacer. En este caso, para realizar este par de operaciones, utilizaremos las instrucciones `continue` y las instrucciones `break`.

- **Ejemplo del uso de continue**

Lo que hace `conitnue` es que cuando se lee uno en el código, lo que le sigue no se lee, se ignora, es como tomar un atajo al siguiente paso. Mantiene el flujo y no rompe la estructura de control.

```js
/*Ejemplo del uso de continue en una iteración que cuenta los números impares entre el 0 y el 20*/
let contador = 0;
let cuenta = 0;

for (contador = 0; contador <= 20; contador++){
  if (contador % 2 == 0){
    continue;
  }
  cuenta ++;
  console.log(contador);
}
console.log('Existen', cuenta, 'números impares');
```

- **Ejemplo uso del break**

A diferencia de `continue`, `break` rompe el flujo, o sea, rompe la estructura de control y evita que se siga ejecutando.

```js
var contador = 0 
var cuenta = 0;

for(contador = 0;contador<= 20;contador++) { 
    if(contador == 5){
        break; //Cuando contador sea 5, la iteración se detendrá y se detendrá su ejecución.
    }
   if (contador % 2 == 0) { 
      continue; //Si se cumple la condición anterior, se ignora todo lo que sigue después del continue.
   } 
   cuenta++;
   debugger;
} 

console.log("Hay",cuenta, "números impares antes de llegar a", contador);
```

### Funciones o métodos

Una función es un conjunto de instrucciones que podremos invocar a través de un nombre clave. Por ejemplo, en un ser humano, la actividad de caminar es un conjunto de instrucciones que combina distintas partes del cuerpo. Así, cuando nosotros escuchamos la palabra caminar o pensamos en el término caminar, todo nuestro cuerpo comienza a moverse. Es decir, hay muchas instrucciones en nuestro cuerpo que están ligadas a la palabra caminar. En el desarrollo de una aplicación web o una aplicación móvil trabajada con JavaScript, nosotros podremos agrupar un conjunto de instrucciones y después invocarlas a través de una palabra clave, esto es una función. También es posible que a una función puedas escucharla con el nombre de método, cualquiera de los dos nombres son adecuados.

#### Estructura básica de una función

La estructura de una función, consiste en la palabra reservada `function`, seguida de el nombre de la función con un par de paréntesis al final (los cuales contendrá los parámetros que la función puede recibir) y de un conjunto de llaves en donde dentro de ellas se indicarán las instrucciones que se quieren ejecutar cuando se llame la función.
Para invocar a la función, se debe poner su nombre junto con unos paréntesis que contendrán los valores que se le entregarán a la función. Todo lo anterior quedaría de la siguiente manera: 

```js
function saludar() {
    var saludo = "Hola Mundo";
    //console.log(saludo);
    return saludo;
}

saludar();
```
#### Parámetros de una función

Una función, además de procesar información y ejecutar instrucciones, también puede recibir elementos con los cuales pueda trabajar. Puedes verlo como si fuera una fábrica. Una fábrica para poder producir sus productos necesita de ingredientes o implementos para poder trabajar. Estos vienen de fuera y se procesan dentro de la fábrica. Así, una vez que termina todo este proceso, al final tienes un producto ya formado. De la misma manera, las funciones pueden recibir este tipo de implementos, que para este tipo de instrucciones le llamaremos parámetros. Lo anterior se mostrará con el siguiente ejemplo:

```js
/*Ejemplo 1*/
function saludar(nombre, edad) {
	console.log('Hola: ', nombre);
	console.log('Edad: ', edad);
	var resultado = nombre + " tiene " + edad + " años";
	return resultado;
}

var mensaje = saludar("yacaFx", 34);

console.log(mensaje)
```

```js
/*Ejemplo 2*/
function saludar(nombre,edad) {
    var nombreLocal = nombre; //Se puede trabajar directamente con los parámetros que recibe la función sin tener que guardarla de forma local
    var edadLocal = edad; //Se puede trabajar directamente con los parámetros que recibe la función sin tener que guardarla de forma local
    var saludo = 'Hola' + ' ' + nombre + ' ' + 'tu edad es' + ' ' + edad;
    return saludo;
}

var mensaje = saludar('Juan', 23);

console.log(mensaje);
```

#### Inicialización de parámetros

Muchas veces nos encontraremos en la situación en que al momento de utilizar una función no necesitemos enviar valores de un parámetro aunque la función tenga declarado que va a recibir un parámetro. Es decir, existirán ciertas circunstancias donde el mismo algoritmo que nosotros hayamos armado pueda o no recibir un valor. Existe lo que es preinicializar un parámetro, se hace dentro de los paréntesis de la función, se pone un igual como si estuviéramos definiendo cualquier variable, lo anterior hará que si no recibe valor, se utilizará el valor preinicializado, pero si recibe valor, se utilizará ese valor

```js
/*La función contar debería recibir un parámetro pero en el caso de que no se reciba, cantidad está preinicializado como 20*/
function contar(cantidad = 20) {
	console.log('Total: ', cantidad);
}

contar(100);
```
#### Parámetros de tipo REST

Muchas veces, los algoritmos que estamos haciendo nos presentan bastantes retos a resolver. Por fortuna, la gran mayoría de los lenguajes de programación son muy versátiles y flexibles y nos ofrecen los medios necesarios para poder dar solución a los casos que se nos lleguen a presentar. En este caso vamos a presentar una situación. La siguiente función recibe dos ingredientes que muestra por consola.

```js
function cocinar(ingrediente1, ingrediente2){
  console.log('El ingrediente 1 es:', ingrediente1);
  console.log('El ingrediente 2 es:', ingrediente2);
}

cocinar('Pollo','Tomate');
```

Pero, **¿Qué sucede si no se sabe cuántos parámetros más voy a enviar, es decir, cuántos ingredientes más pueda yo llegar a necesitar: uno, dos, tres, cinco?**.  Lo que tendremos que hacer es utilizar un parámetro de tipo *rest*, esto viene de la expresión: *el resto de...* Entonces, nosotros aquí utilizaremos un operador muy importante, escribiremos tres puntos y le daremos nombre al parámetro. Este nombre que nosotros pondremos será *masIngredientes*, así si yo escribo `console.log(masIngredientes)` e invoco a los demás ingredientes en forma de un *arreglo de tipo objeto* por lo cual se puede trabajar como tal.

```js
/*Ejemplo de uso de parámetros de tipo REST*/
/*masIngredientes es el parámetro de tipo REST que se puede trabajar como un arreglo de objetos*/
function cocinar(ingrediente1, ingrediente2, ...masIngredientes){
  console.log('El ingrediente 1 es:', ingrediente1); //Muestra el primer ingrediente
  console.log('El ingrediente 2 es:', ingrediente2); //Muestra el segundo ingrediente
  console.log('Los demás ingredientes son:', masIngredientes); //Muestra el arreglo compuesto por el resto de los valores entregados a la función
  /*El siguiente bloque de código se encarga de mostrar el resto de los ingredientes que contiene masIngredientes como se mostrarón los ingredientes 1 y 2*/
  if (masIngredientes.length != 0){
    var contador = 0;
    while(contador < masIngredientes.length){
      var ingrediIndice = contador + 3
      console.log('El ingrediente', ingrediIndice, 'es:', masIngredientes[contador]); 
      contador++;
    }
  }
}
cocinar('Pollo','Tomate','Arroz','Frijoles', 'Pescado', 'Papa');
```
```js
/*El mismo ejemplo anterior pero con un for*/
function cocinar(ingrediente1, ingrediente2, ...masIngredientes){
  console.log('El ingrediente 1 es:', ingrediente1);
  console.log('El ingrediente 2 es:', ingrediente2);
  console.log('Los demás ingredientes son:', masIngredientes); //Muestra el arreglo compuesto por el resto de los valores entregados a la función
  if (masIngredientes.length != 0){
    for(let contador = 0; contador < masIngredientes.length; contador++){
      var ingrediIndice = contador + 3
      console.log('El ingrediente', ingrediIndice, 'es:', masIngredientes[contador]); 
    }
  }
}

cocinar('Pollo','Tomate','Arroz','Frijoles','Pescado', 'Papa');
```

De esta forma las funciones puede recibir N cantidad de parámetros sin tener conocimiento de la cantidad real que recibirán.

#### Parámetros de tipo SPREAD

Si ya contamos con una opción para poder recibir N cantidad de parámetros *(REST)*, también deberíamos contar con una opción para poder enviar N cantidad de parámetros y que no estén declarados todos estos parámetros directamente. Veamos los siguientes parámetros llamados *SPREAD*, es decir, parámetros que se pueden esparcir. A diferencia de los parámetros *REST*, los parámetros *SPREAD* no es necesario que sean declarados en la estuctura original de la fumción, **sino en la invocación** (`función(...parámetroSpread, parámetroNormal,...);`). Lo que pasará es que el parámetro *spread* se esparcirá entre los parámetros que recibe la función, o sea, que si en la función se declara que recibirá 3 parámetro, el parámetro *spread* se esparcirá (distribuirá) entre ese 3 parámetros que recibe (son un arreglo que cada casilla se guarda en uno de los parámetros que recibe la función).

```js
/*Ejemplo del uso de SPREAD*/
function cocinar(ingrediente1, ingrediente2, ingrediente3){
  console.log('El Ingrediente 1 es:', ingrediente1);
  console.log('El Ingrediente 2 es:', ingrediente2);
  console.log('El Ingrediente 3 es:', ingrediente3);
}

let ingredientes = ['Tomate','Papa','Arroz','Sal'];
cocinar('Pollo','Lechuga', ...ingredientes); //En este caso solo Tomate queda guardado como ingrediente3 en la función (...ingredientes es el parámetro SPREAD)
```

```js
/*Ejemplo del uso de parámetros REST y SPREAD*/
function cocinar (ingrediente1, ingrediente2, ingrediente3, ...otrosIngredientes){
  console.log('El Ingrediente 1 es:', ingrediente1);
  console.log('El Ingrediente 2 es:', ingrediente2);
  console.log('El Ingrediente 3 es:', ingrediente3);
  console.log('Los otros ingredientes son:', otrosIngredientes);
}

let ingredientes = ['Tomate','Papa','Arroz','Sal'];

/*En este llamado, al estar el parámetro SPREAD al final, el resto de los valores que guardaquedan en el parámetro REST de la función*/
//cocinar('Pollo','Lechuga', ...ingredientes);

/*En este llamado, al estar el parámetro SPREAD al principio, los lugares de los parámetros de la función son ocupados por los valores del parámetro SPREAD y el resto de parámetros quedan en el parámetro REST de la fumción*/
//cocinar(...ingredientes, "Arroz", "Pescado", "Chile");
```

#### Funciones anónimas en JS

Las funciones anónimas son un recurso ampliamente utilizado por los programadores de JavaScript. Esto nos permite no asignarle a un nombre a un conjunto de instrucciones que deseemos ejecutarlo sin necesidad de asociarlo. Esto lo podemos utilizar comúnmente cuando tenemos un *callback* o cuando queremos nosotros aislar una función de algún otro elemento. Por ejemplo, si nosotros quisiéramos ahorita ejecutar una función o un conjunto de instrucciones al inicio de nuestra aplicación, en lugar de tener que crear una función nueva y ponerle un nombre e invocar la función, podemos hacerlo de manera aislada. ¿Esto cómo es? Vamos a escribir la sintaxis de dos paréntesis seguidos, esto nos permite aislar nuestra función, y en este caso estamos poniendo aquí adentro las instrucciones que nosotros queremos generar, pero para escribir estas instrucciones simplemente vamos a ocupar la siguiente sintaxis: `function`, paréntesis y llaves. Si te das cuenta, esto cambia de una función normal, puesto que la función normal antes del paréntesis y después de la palabra clave `function` lleva un nombre; en este caso no lo lleva.

```js
/*Ejemplo 1: Forma aislada de escribir una función anónima*/
(
  function(){
    var mensaje = 'Hola de nuevo';
    console.log(mensaje);
  }
)()
```
**La siguiente forma es la más común para escribir funciones anónimas**, puedes recibir parámatros y se llaman con el nombre de la variable a la que se le asignó la función.

```js
/*Ejemplo 2: Forma más común de escribir fumciones anónimas*/

let saludar = function(nombre){
    var mensaje = 'Hola de nuevo' + ' '+ nombre;
    console.log(mensaje);
}

saludar('Juan');
```

#### Entendiendo los callbacks

Hemos aprendido que una función puede recibir parámetros de distintos tipos: objetos, arreglos, cadenas de texto, números, valores "booleanos". Pero ¿qué crees? También puede recibir funciones como parámetros. Espera, todavía no enloquezcas. De hecho, recibir funciones como parámetros es algo muy común y de pronto lo vas a estar utilizando y ni cuenta te vas a dar, puesto que los "callbacks" hacen mucho juego con las funciones anónimas.

```js
/*Ejemplo de callbacks(CB)*/

/*Tanto sumarCB como restarCB con callbacks*/
function calcular(datoA, datoB, sumarCB, restarCB){
  let suma = datoA + datoB;
  let resta = datoA - datoB;
  /*Deben llamarse dentro de la función para que las estructura que reciben, reciban los respectivos parámetros que se les quiere entregar*/
  sumarCB(suma);
  restarCB(resta);
}

/*Cuando se llamar la función calcular, se le entrega los valores 2 y 3 para las operaciones suma y resta de la función y además se le entrega tantas funciones anónimas como callbacks se hayan definido*/
calcular(2,3, function(resultadoSuma){
  console.log('Suma igual a', resultadoSuma);
}, function(resultadoResta){
  console.log('Resta igual a', resultadoResta);
});
```
Un punto muy importante: los *callbacks* generalmente me ayudan a controlar procesos asíncronos, es decir, en una función yo puedo hacer la invocación de muchos procesos y en otra función puedo hacer otra invocación, ya sea de otros tantos u otros pocos procesos. Así, entonces, se ejecuta una función y la otra función también se puede ejecutar y no importa cuál vaya terminando porque de cualquier forma podemos estar recuperando la información. La estructura al final es la siguiente:  `nombreFunción(valor1, valor2, ..., valorN, func, func, ..., funcN)`

#### Funciones arrow

Otra manera que tenemos de escribir funciones anónimas es a través de las llamadas funciones de tipo *arrow* o función *flecha*, que también son conocidas con el nombre de *Fat arrow* o *lambda functions* o funciones *lambda*. Puedes llamarla con cualquiera de estos nombres. La idea es simplificar un poco el uso de la sintaxis para esta función, veamos cómo escribir una función con este tipo de sintaxis. Para esto, vamos a crear una variable nueva llamada `saludar` donde almacenaremos el resultado de nuestra función. En este caso vamos a escribir primero `let saludar = nombre`, después el símbolo de igual seguido del símbolo mayor que, pero lo dejamos pegado (`let saludar = nombre =>`). Después de esto, entre comillas vamos a escribir la palabra (`let saludar = nombre => 'Hola'`), dejamos un espacio y concatenamos con la palabra (`let saludar = nombre => 'Hola' + nombre`). El llamado de este tipo de funciones es el mismo de una función común y corriente. Lo anterior junto queda de la siguiente forma:

```js
let saludar = nombre => 'Hola' + ' ' + nombre; //nombre es el parámetro que recibe la función y lo que sigue d ela flecha es lo que retorna 
console.log(saludad('Susana'));
```

Esto quiere decir que con esto tenemos un tipo de función más sencillo y claro, es muchísimo más fácil que escribir una función anónima con la sintaxis de'function'. Pero este tipo de funciones también tiene ciertas variantes. 

- **Ejemplo Aritemetico**

```js
/*sumarDiez se encarga de sumarle 10 a lo que reciba al ser llamada*/
let sumarDiez = a => a+10;
console.log('El resultado al sumar 10 es:', sumarDiez(10));
```

- **Enviar más de un parámetro**

```js
/*Sumar se encarga de sumar los dos parámetros que recibe al momento de ser invocada*/
let sumar = (a,b) => a+b;
console.log('El resultado de la suma es:', sumar(1,2));
```

- **Más de una instrucción**

```js
/*sumaTriple se encarga de sumarle 5 a la suma de los parámetros que se pasen al momento de llamar a la función*/
let sumaTriple = (a,b) => {
  let c = 5;
  return a + b + c;
}
console.log('El resultado de sumarle 5 a los parámetros es:', sumaTriple(1,2)); //Muestra por consola la suma de a, b y la variable local de sumaTriple, c.
```
- **No enviar ningún parámetro**

```js
/*Validar no recibe ningún parámetro por lo cual al ser llamada sólo muestra el mensaje que retorna*/
let validar = () => {
  return 'Validación correcta';
}
console.log(validar());
```

Este tipo de funciones se vuelven bastante importantes y muy usables cuando quiero integrarlas en "callbacks" o incluso cuando yo quiero utilizarlas dentro de otras funciones como, por ejemplo, funciones de búsqueda en un arreglo o funciones que me permiten estar iterando en colecciones de datos.

#### Uso del operador this

Es un objeto de referencia u operador. Cuando se usa en una función anónima normal, por ejemplo puede traer cierta cosa de el HTML (`this.innerHTML`) o una clase entera (`this`) pero si se usa en una función anónima de tipo *arrow*, trae absolutamente todo (`this`), aunque eso se puede eaprovechar para hacer que al momento de interectatuar con el elemnto que en su código tiene un `this.section`, este redireccione a otra cosa.

### Eventos en JavaScript

JS permite la lecutra de distintos tipos eventos los cuales son:

#### Eventos del mouse

En JavaScript, es posible interactuar con casi todos los elementos que van a componer una página web o nuestra aplicación, desde HTML, CSS o el mismo JavaScript. Para esto necesitamos agregar elementos de escucha, es decir, agregar un elemento que me permita a mí estar escuchando cuando algo sucede. Uno puede agregar este tipo de elementos ya sea directamente en las etiquetas de HTML o trabajándolas directamente en JavaScript. Mi recomendación es: tráete todo este tipo de interacciones hacia JavaScript. Para esto, lo primero que tenemos que hacer es hacer una asociación entre HTML y JavaScript. Lo anterior se logra de la siguiente manera:

```html
<!--HTML de un botón-->
<!DOCTYPE html>
<html lang="en">

<head>
    <title></title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <!--Etiqueta dedicada al css del botón-->
    <style> 
        div {
            width: 200px;
            height: 50px;
            background-color: chocolate;
            text-align: center;
            padding: 2%;
            margin: 0 auto;
            color: white;
            border-radius: 10px;
            box-shadow: 5px 5px 5px gray;
            cursor: pointer;
        }
    </style>
</head>

<body>
    <!--Esta clase es referenciada en el archivo app.js-->
    <div class="boton">
        Da click en este botón
    </div>
    <!--Se llama al código del archivo app.js ubicado en la carpeta js-->
    <script src="js/app.js"></script>
</body>

</html>
```
```js
/*app.js*/

/*Para realizar la aosición entre las acciones del mouse en el botón, se utiliza lo que tiene como contenido la constante botón*/
const boton = document.querySelector('.boton');

/*El método addEvenListener sirve para poner una escucha de eventos*/
boton.addEventListener('click', function () {
    console.log("El boton se ha pulsado");
})//Evento Click sobre el botón

boton.addEventListener('mouseover', function () {
    console.log("El mouse esta sobre el botón");
})//Evento de poner el cursor sobre el botón (detecta si el mouse está sobre el botón)

boton.addEventListener('mouseout', function () {
    console.log("El mouse esta fuera del botón");
})//Evento de sacar el cursor del botón

/*Existen más evenetos que s epueden utilizar, se pueden encontrar en w3schools o en Mozilla Developer Network*/
```

#### Eventos del teclado

Así como podemos escuchar eventos del mouse, también podemos escuchar eventos del teclado. Y para esto tenemos tres tipos de eventos: los eventos que podemos escuchar del teclado son **keydown**, **keypress** y**keyup** y podemos escucharlos directamente cuando se están aplicando a determinada etiqueta o elemento de HTML de nuestra página o aplicación o cuando lo estamos aplicando a cualquier parte de nuestra página. Cuando queremos aplicarlo a cualquier parte de nuestra página, solamente debemos dirigir nuestro `addEventListener` al objeto `window` y con esto podemos escuchar.

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title></title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <!--Se llama al código alojado en app.js-->
        <script src="js/app.js"></script>
    </head>
    <body>
    
    </body>
</html>
```
```js
/*app.js*/

window.addEventListener("keydown", function (event) {
  console.log('Pulsando tecla');
  /*Con el código que se encuentra dentro del console.log(), se puede saber cual es la tecla que se está presionando y transforma el código arrojado por event.keyCode en la letra que se pulsó*/
	console.log(String.fromCharCode(event.keyCode))
})//keydown es para cuando el evneto es el pulsar una tecla


window.addEventListener("keypress", function (event) {
	console.log('Tecla pulsada')
})//keypress es para cuando el evento es mantener una tecla pulsada


window.addEventListener("keyup", function (event) {
	console.log('Tecla liberada')
})//keyup es para cuando una tecla se deja de presionar
```

#### Evento de carga de documento

Como hemos venido realizando, podemos escuchar eventos que sucedan en cualquier parte de nuestra aplicación web. Ahora nos toca escuchar un evento principal y es el evento de cuando el documento ha terminado de cargarse. ¿Para qué? Para poder contar con estos elementos ya listos en pantalla y poder comenzar a interactuar con algo. Se te puede presentar una situación similar cuando tú tengas un espacio donde necesites cargar datos remotos o datos que se encuentren en otro lado y no precisamente en tu misma página. Para este tipo de situaciones, lo que nosotros hacemos primero es escuchar cuando la carga del documento o de la ventana ha terminado y, una vez que ha terminado esta carga, entonces nosotros ya podemos trabajar.

```html
<!DOCTYPE html>
<html lang="en">
    <head>
        <title></title>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1">
        <!--Se llama al código de JS desde app.js-->
        <script src="js/app.js"></script>
    </head>
    <body>
    
    </body>
</html>
```
```js
/*app.js*/

/*El evento load permite permite estar a la escucha de que todo los elementos HTML, JS, CSS, imágenes, etc se hayan "parseado", o sea, se hayan cargado*/
window.addEventListener('load', function() {
  console.log('El contenido de la ventana se ha cargado');  
});
```

Un ejemplo de uso de lo anterior es que al temrinar de cargar todo, entonces ahora si puedo ir y conectarme a un dato remoto. En el ejmplo de código anterior, luego de saber que todo se cargó, se puede hacer todas las invocaciones de otras funciones o de datos que se necesiten. De esta forma, ya puedes interactuar y comenzar a trabajar con el evento `load` cada que tu documento ha sido cargado satisfactoriamente dentro de una ventana web.

#### Eventos multimedia en JS

También se puede escuchar las acciones que se realizan sobre un vídeo con los eventos `play`, `seeking` y `ended` los cuales hacen referencia al momento en el que se inició el vídeo, se está buscando en el vídeo (barrido de tiempo, tiene métodos para obtener cosas como el tiempo en el cual se detuvo la busqueda) y al momento en el que el vídeo terminó.

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title></title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">

</head>

<body>
  <!--Se inserta un vídeo-->
    <video class="bostonVideo" width="500" controls>
        <source src="boston.mp4" type="video/mp4">
    </video>
    <script src="js/app.js"></script>
</body>

</html>
```

```js
/*Eventos Multimedia en vídeos*/
const video = document.querySelector('.bostonVideo');

/*Cuando se inicia el vídeo se muetra por consola el mensaje 'El video ha iniciado'*/
video.addEventListener("play", function () {
    console.log('El video ha iniciado');
});

/*Cuando hace un barrido en la línea de tiempo del vídeo se muetra por consola el mensaje 'Se esta buscando en el video' 
y además se devuelve el tiempo del barrido/busqueda */
video.addEventListener("seeking", function () {
    console.log('Se esta buscando en el video', this.currentTime);
});

/*Cuando el vídeo termina su reproduccion se muestra por consola el mensaje 'El video ha terminado'*/
video.addEventListener("ended", function () {
    console.log('El video ha terminado');
});
```

#### Uso de temporizadores o timers

Bajo ciertas circunstancias, el uso de temporizadores dentro de una aplicación va a ser muy importante ya que estos sirven para poder ejecutar determinadas acciones dependiendo de un cierto lapso de tiempo. Existen dos tipos de temporizadores llamados `setInterval` (ejecución infinita de un elemento cada determinado tiempo) y `setTimeout` (ejecuta una acción después del tiempo que se indica, se hace sólo una vez).

```js
/*setColor es la función que se ejecutará con los temporizadores*/
function setColor() {
    var pagina = document.body;
    pagina.style.backgroundColor = pagina.style.backgroundColor == "blue" ? "green" : "blue";
}
```

```js
/*Ejecución infinita de setColor cada 2000 milisegundos (2 segundos)*/
var temporizador = setInterval(function () {
      setColor();
  }, 2000);

/*Lo anterior se ejecuta de manera infinita por lo cual se crea la función stopChangeColor la cual se encarga de limpiar el temporizador y detener las ejecuciones de setInterval*/
function stopChangeColor() {
    clearInterval(temporizador) //Metodo que limpia el intervalo de tiempo de temporizador
}
```

```js
/*Luego de 3000 milisegundos (3 segundos) se ejecuta una vezla función setColor*/
 setTimeout(function () {
     setColor();
 }, 3000);
```

### Ventanas Emergentes o Cuadros de diálogo en JS
JavaScript cuenta con mecanismos suficientes para poder alertar o notificar al usuario de que algo ha sucedido en el sistema.

#### Ventanas de Alerta en JS

Para generar una ventana de alerta de utiliza la palabra reservada `alert` la cual cumple la función de mostrar una alerta por pantalla que notifica de algo al usuario. Este tipo de alertas no escucha alguna acción realizada sobre ella misma como por ejemplo que el usuario presionó en el botón de Aceptar que esta misma contiene. Lo anterior se debe a que este tipo de alertas tiene el unico objetivo de avisar algo sin esperar respuesta a ello.

**CUIDADO CON EL USO DE ESTE TIPO DE ALERTAS YA QUE ESTE TIPO DE ALERTAS TIENEN EL OBJETIVO DE AVISAR AL USUARIO DE EVENTOS IMPORTANTES DE ALTA ESCALA**

```js
/*Se hace uso del mismo vídeo de la sección Eventos multimedia*/
const video = document.querySelector('.bostonVideo');

/*Al terminar el vídeo se genera una alerta por pantalla que hace alusión a eso*/
video.addEventListener("ended", function () {
  //alert("El vídeo ha terminado"); //Alerta sin salto de línea
  alert("MENSAJE \n\n El video ha terminado"); //Alerta con salto de línea (\n)
});
```

#### Generar en JS una ventana de confirmación

Existirán ocasiones en las cuales se hará necesario ejecutar una acción de acuerdo a la respuesta que proporcione el usuario a una ventana emergente. En estos casos existe el método `confirm` el cual notificará algo directamente por pantalla dandonos la opción de elegir que acción queremos ejecutar dependiendo de la respuesta del usuario a esta notificación. Esta ventana emergente tiene los botonoes aceptar (retorna un True) y cancelar (retorna un False).

```js
/*Se utiliza el mismo vídeo de Eventos Multimedia*/
const video = document.querySelector('.bostonVideo');

/*Cuando el vídeo termina se genera una ventana de notificación que pregunta al usuario si quiere repetir el vídeo*/
video.addEventListener("ended", function () {
    let resultado = confirm("¿Deseas ver el video nuevamente?");
    console.log(resultado); //Muestra por consola lo que contiene la variable resultado 
    if (resultado) {
        video.play();
    }else {
        window.location = "http://www.google.com";
    }
/*En este caso, no es necesario colocar en la condición resultado == true ya que al ser un valor booleano la estructura de control por si sola entenderá que cuando resultado es true se ejecuta cierto codigo, de lo contrario (cuando es false) se ejecuta otra cosa*/
});
```

#### Ventana de ingreso de datos

JS permite la creación de ventanas emergentes en las cuales el usuario puede colocar cierta información la cual se puede almacenar en una variable, base de datos o el medio de almacenamiento que se estime conveniente. Para lo anterior existe `prompt()`.

```js
/*Se ocupa el vídeo de la sección eventos multimedia*/
const video = document.querySelector('.bostonVideo');

video.addEventListener("ended", function () {
  /*email guarda el email que ingresa el usuario en la ventana emergente, por default tiene data@info.com*/
   let email = prompt("Escribe tu correo para ver mas videos",  "data@info.com");
   /*Estructura de control que permite ejecutar codigo en caso de que el usuario presione en cancelar y en el caso de que deje el email vacio*/  
   if (email == null || email == "") {
        console.log("Sin datos");
    } else {
        console.log(email);
    }
});
```

### Trabajando con números en JS

Al igual que muchos lenguajes de programación, Javascript dispone de muchas propiedades métodos y mecanismos para facilitar nuestras tareas como programador.

#### Propiedades numéricas

Para utilizar las propiedades numéricas es se debe invocar a `Number`. Entre las propiedades se encuentran las siguientes:

- **MAX_VALUE:** Entrega el número más grande con el que puede trabajar JS.

```js
console.log("MAX_VALUE: ", Number.MAX_VALUE);
```

- **MIN_VALUE:** Entrega el valor minimo con el que trabaja JS.

```js
console.log("MIN_VALUE: ", Number.MIN_VALUE);
```

- **NEGATIVE_INFINITY:** Es el objeto Infinity (si se ocupa en un for, el for será infinito) negativo.

```js
console.log("NEGATIVE_INFINITY: ", Number.NEGATIVE_INFINITY);
```

- **POSITIVE_INFINITY:** Es el objeto Inifinity positivo.

```js
console.log("POSITIVE_INFINITY: ", Number.POSITIVE_INFINITY);
```

- **NaN:** "Not a Number", hace referencia a si el valor es o no un número.   

```js
console.log("NaN: ", Number.NaN);
```

#### Métodos numéricos

En JS existen métodos para trabajr con números los cuales principalmente ayudaran a convertir numeros por ejemplo de string con formato numero a numero entero o float.

```js
var numero = "10.5";

/*typeof entrega el tipo de la variable*/
console.log('Number: ', typeof numero, typeof Number(numero)); //numero es un string, al utilizar Number() numero se vuelve un objeto del tipo Number

/*Tranforma el contenido del string numero a entero matematicamente utilizable*/
console.log('parseInt: ',  parseInt(numero));

/*Tranforma el contenido del string numero a flotante matematicamente utilizable*/
console.log('parseFloat: ', Number.parseFloat(numero));

/*Entrega un true o false dependiendo de si el valor de la variable tiene formato de numero o no (una letra arroja true)*/
console.log('isNaN: ', isNaN(numero));

/*Entrega true o false dependiendo de si el valor de la variable es un entero o no*/
console.log('isInteger: ', Number.isInteger(numero));
```

#### Métodos numéricos en instancias

En JavaScript, cuando tenemos una variable que está almacenando un número directamente, automáticamente estamos contando con ciertos métodos que podemos utilizar. 

```js
var numero = 2.5;

/*Transfroma el numero a notación cientifica, recibiendo la cantdias de decimales que tendrá la parte entera. Se aplica directamente al numero que se encuentra almacenado en la variable*/
console.log("toExponential: ", numero.toExponential(4));

/*Ajusta el numero para manejar los x decimales que se indican. Si se utiliza el valor 0, se hace un redondeo. El valor resultante es un String*/
console.log("toFixed: ", numero.toFixed(2));

/*Da una precisión del digito hasta los x decimales que se indican. El valor resultante es de tipo String*/
console.log("toPrecision: ", numero.toPrecision(6));

/*Transforma a string (cadena de texto) el valor del numero*/
console.log("toString: ", typeof numero.toString());
```