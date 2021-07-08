
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

- **Mover una línea:** Para mover una línea, se debe poner el cursor en la línea deseada, luego presionar la tecla *ALT* y con las flechas mover la línea hacía arriba o hacía abajo.

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

Para definir una cadena de texto, se el contenido se puede poner entre comillas simples o comillas simples pero **no las dos combinadas alternándose entre simples al inicio y dobles al final o viceversa**.

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
let personaJSON = JSON.stringify(persona) //Transforma el JSON persona a una cadena de texto (ya no es un objeto con método GET)
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

#### Operadores Relacionales

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

var activo = true // Booleano

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
### Trabajando con cadenas de texto

En JS existen las cadenas de texto las cuales tienen métodos los cuales hacen más el trabajo con ellas.

#### Creación de cadenas de texto

Se pueden crear dejando entre comillas el valor texto de la variable (más común) o mediante el uso del objeto `String` el que dejara el texto como una cadena de las letras quer lo componen.

```js
/*Creación mediante la utilización de comillas (Pueden ser dobles o simples pero no combinadas)*/
var pais = 'México';

/*Creación mediante el uso del objeto String*/
var comida = new String("Ceviche");
```

#### Medir una cadena de texto 

Para medir el largo de la cadena de texto se utiliza el metodo `.lenght` el cual retorna el largo de la cadena de texto que se encuentra guardada en la variable. Cabe mencionar que las tabulaciones (se pueden encontrar antes, entre o después del texto) son contadas como si fueran letras por lo cual si solo se ingresan tabulaciones, el metodo entregará un largo de todas formas.

```js
var mensaje = "Estoy aprendiendo JavaScript";

console.log("La cadena de texto tiene: " + mensaje.length + " letras");
/* El resultado de lo anterior es: La cadena de texto tiene: 28 letras*/
```

#### Búsqueda de texto por ínidces y por expresiones regulares

```js
/*Primero se define una variable con la que se utilizaran los métodos, que contenga la cadena de texto*/
var mensaje = 'Estoy aprendiendo JavaScript y estoy aprendiendo mucho';

/*Luego se define una variable que guardara el resultado de la búsqueda*/
var resultado;
```

- **indexOf:** Busca la primera aparición de lo que se le entrega y regresa la posición de esta.

```js
resultado = mensaje.indexOf("aprendiendo");
console.log(resultado); // 6
```

- **lastIndexOf:** Busca la ultima aparición de lo que se le entrega y regresa la posición de esta.

```js
resultado = mensaje.lastIndexOf("aprendiendo");
console.log(resultado); // 37
```

- **search:** Es similar a indexOf, en si retorna lo mismo, o sea, la posición de la primera concidencia dentro de la cadena de caracteres.

```js
resultado = mensaje.search("aprendiendo");
console.log(resultado); // 6
```

- **search | expresión regular:** En este caso al search se le entrega la expresión regular que estamos buscando ( se pone entre slashs `variable.search(/ja/)`), en el caso de que ae quiera buscar sin considerar mayusculas y minusculas (in case sensitive) luego del segundo slash se debe agregar una *i* quedando todo de la siguiente manera `variable.search(/ja/i)`.

```js
resultado = mensaje.search(/ja/i); /*Entre slashs va la expresión que se quiere buscar, el i es para que no distinga entre mayusuclas y minisculas*/
console.log(resultado); // 18
```

Cabe menscionar que si cualquiera de los metodos entrega como valor *-1* significa que se buscaba en la cadena de caracteres no se encontró.

#### Búsqueda de caractares en cadenas

```js
/*Primero se define una variable con la que se utilizaran los métodos, que contenga la cadena de texto*/
var mensaje = 'Estoy aprendiendo JavaScript y estoy aprendiendo mucho';

/*Luego se define una variable que guardara el resultado de la búsqueda*/
var resultado;
```

- **match:** Trabaja con expresiones regulares (lo que se busca debe ir entre slash `/buscado/`). si se utiliza `variable.match(/buscado/)`, retorna un arreglo con lo que se buscaba (la primira concidencia que encuentra), su posición (donde inicia lo buscado), la entreda en la cual buscó lo solicitado. En cambio si se utiliza `variable.match(/buscado/gi)` **(g es de global e i es de in case sensitive)**, retornara un arreglo con todas las coincidencias pero sin la otra información.

```js
//resultado = mensaje.match(/aprendiendo/); // ["aprendiendo", index: 6, input: "Estoy aprendiendo JavaScript y estoy Aprendiendo mucho", groups: undefined]
//resultado = mensaje.match(/aprendiendo/gi); // ["aprendiendo", "Aprendiendo"]
console.log(resultado); 
```

- **substr:** Este metodo recibe de parametro la primera posición de donde comenzar a buscar y la cantidad de caracteres a considerar desde la posición inicial. Ingresando lo anterior, se retorna todo lo que se encuentre entre las posiciones indicadas. (`variable.substr(inicio,cant-caracteres)`).

```js
resultado = mensaje.substr(6,11); // Desde el caracter en la posición 6 considera 11 caracteres
console.log(resultado); // aprendiendo
```

- **substring:** Es una opción a `substr` que a diferencia de esta, considera las posiciones de inicio y fin del arreglo de caracteres, o sea, que su segundo parametro debe ser la posición en la que se quiere finalizar la "busqueda" dentro de la cadena de caracteres original. (`variable.substring(inicio,fin)`)

```js
resultado = mensaje.substring(6,17); // Desde el caracter en la posición 6 retornara todo lo que encuentre hasta la posición 17
console.log(resultado); // aprendiendo
```

- **charAt:** Este metodo recibe la posición del caracter que se está buscando.

```js
resultado = mensaje.charAt(0); // Busca el caracter que se encuentra en la posición 0 de la cadena
console.log(resultado); // E
```

#### Búsqueda de cadenas de texto especificas

```js
/*Primero se define una variable con la que se utilizaran los métodos, que contenga la cadena de texto*/
var mensaje = 'Estoy aprendiendo JavaScript y estoy aprendiendo mucho';

/*Luego se define una variable que guardara el resultado de la búsqueda*/
var resultado;
```

Los siguientes son los nuevos metodos de busqueda (2017 vibes). Cabe mencionar que todos estos metodos **son sensibles a mayusculas y minusculas**.

- **startsWith:** Sirve para saber si alguna cadena de texto comienza con cierta palabra o caracter.

```js
resultado = mensaje.startsWith("es");
console.log(resultado); // false debido a que mensaje comienza con Es y no con es.
```

Existe una variante que combina un metodo visto anteriormente. En esta variante, no solo se recibe lo que se quiere buscar sino que también se recibe una posición en la cual buscar si esta inicia con la palabra o caracter deseado. Lo anterior se puede gracias a la utilización del metodo `indexOf`.

```js
var textoEn =  mensaje.indexOf("JavaScript"): // Obtiene la posición de inicio de la palabra JavaScript dentro de la cadena
resultado = mensaje.startsWith("Ja", textoEn); // Desde la posición que guarda textoEn busca si comienza con Ja lo cual resulta en un true
```

- **endsWith:** Sirve para saber si alguna cadena de texto termina con cierta palabra o caracter.

```js
resultado = mensaje.endsWith("JavaScript");
console.log(resultado); // true
```

- **includes:** Sirve para saber si alguna cadena de texto incluye cierta palabra o caracter.

```js
resultado = mensaje.includes("JavaScript";
console.log(resultado); // true
```

Tambien se le puede entregar una posición desde la cual comenzar a buscar el termino de la cadena.

```js
resultado = mensaje.includes("Estoy", 6); // comienza la busqueda desde la posición 6 de la cadena
console.log(resultado); // false
```

#### Métodos de generación, reemplazo y separación

Las situaciones que se nos pueden presentar cuando estamos trabajando con cadenas de texto pueden ser muy variadas, es por eso que también tenemos algunos métodos para generar texto, para reemplazar o para separar.

```js
/*Primero se define una variable con la que se utilizaran los métodos, que contenga la cadena de texto*/
var mensaje = 'Estoy aprendiendo JavaScript';

/*Luego se define una variable que guardara el resultado de la búsqueda*/
var resultado;
```

- **repeat:** Al tulizar *repeat* se repetira n cantidad de veces (la que nosotros establezcamos) el contenido de la variable en la misma línea y cada repetición se encontrara unida al final de la cadena anterior.

```js
resultado = mensaje.repeat(2)
console.log(resultado); // Estoy aprendiendo JavaScriptEstoy aprendiendo JavaScript
```

- **replace:** Se encarga de buscar un caracter, palabra o frase dentro de la cadena de texto con el fin de reemplazarla por otro caracter, palabra o frase **sin afectar la cadena de texto original**. Lo anterior lo hace con la primera coincidencia que encuentra por lo cual en el caso de haber otra más adelante, no será reemplazada.

```js
resultado = mensaje.replace("JavaScript","a programar")
console.log(resultado); // Estoy aprendiendo a programar
```

- **slice:** Se encarga de mover el cursor de inicio de la cadena a la posición que uno indique y desede ahí se puede elegir hasta donde se quiere considerar la cadena texto, o sea, permite obtener un pedazo de la cadena de texto sin afectar a la cadena de texto original.

```js
/*Se le entrega solo el inicio*/
resultado = mensaje.slice(6)
console.log(resultado); // aprendiendo JavaScript

/*Se leentrega inicio y fin*/
var resultado2;
resultado2 = mensaje.slice(6, 17)
console.log(resultado2); // aprendiendo
//resultado2 = mensaje.slice(6,mensaje.length-6);
//console.log(resultado2); //aprendiendo Java
```

- **split:** Separa toda la cadena de texto en base a una caracter o palabra que se le entrega retornando un arreglo.

```js
resultado = mensaje.split(" "); // Se separan las palabras por espacios (se puede poner otro tipo de separador)
console.log(resultado); // ["Estoy","aprendiendo","JavaScript"]
```

- **trim:** Quita los espacios en blanco tanto del inicio como del final de la cadena de texto.

```js
var mensaje2 = "     Estoy aprendiendo JavaScript     ";
resultado = mensaje2.trim();
console.log(resultado); // Estoy aprendiendo JavaScript
```

#### Métodos de transformación de texto en JS

Existen metodos que permiten la tranformación de caracteres en cadenas te texto, de algo a cadena de texto o cubren la necesidad de combinar cadenas de texto.
```js
/*Se definen ciertas variables que ayudaran al entendimiento de los metodos de la sección*/
var mensaje = "Estoy aprendiendo JavaScript";
var mensaje2 = " y programación";
var total = 123456;
var resultado;
```

- **toString:** Sirve para tanformar, pñor ejemplo, un numero a cadena de texto.

```js
console.log(total); // 123456 
resultado = total.toString(); // Tranforma el numero 123456 a cadena de texto
console.log(resultado); // "123456"
```

- **toLowerCase:** Tranforma todos los caracteres de la cadena de texto a minusculas.

```js
console.log(mensaje); // Estoy aprendiendo JavaScript
resultado = mensaje.toLowerCase(); // Transforma los caracteres del contenido de mensaje en minusculas 
console.log(resultado); // estoy aprendiendo javascript
```

- **toUpperCase:** Tranforma todos los caracteres de la cadena de texto a mayusculas.

```js
console.log(mensaje2); // y programación
resultado = mensaje2.toUpperCase(); // Transforma los caracteres del contenido de mensaje2 en MAYUSCULAS 
console.log(resultado); // Y PROGRAMACIÓN
```

- **concat:** Permite unir dos o más cadenas de texto.

```js
var mensaje3 = ", cada vez aprendo más.";
resultado = mensaje.concat(mensaje2, mensaje3," Espero seguir aprendiendo mucho más.");
console.log(resultado); // Estoy aprendiendo JavaScript y programación, cada vez aprendo más. Espero seguir aprendiendo mucho más.
```

#### Funcionamiento de las plantillas y literales en JS

Una de las cosas verdaderamente funcionales cuando trabajamos con cadenas de texto que posee JavaScript es el uso de plantillas y literales. Para poder escribir plantillas se utilizan backtiicks o comillas especiales las cuales ayudaran a definir la plantillas y dentro de estas se deja el uso del simbolo *+* para concatenar cadenas de texto y se cambiar por el uso de literales los cuales son definidos por un signo de peso *$* seguidos de llaves que contendrán a la variable que se quiere agregar a la plantilla.

```js
var lenguaje = 'JavaScript';
var lenguaje2 = 'HTML';
var mensaje, mensaje2;

/*Mensaje Simple*/
mensaje = `Me gusta aprender ${lenguaje} y su integración con ${lenguaje2}`;
console.log(mensaje);

/*Mensaje multilinea*/
mensaje2 = `
    Hola Mundo,
    estoy aprendiendo
    ${lenguaje} y me gusta
    como se integra con ${lenguaje2} y CSS`;

console.log(mensaje2);
```

### Trabajar con arreglos en JS

Los arreglos son estructuras de datos que nos permitirán almacenar más de un tipo de dato dentro de una misma variable. ¿Qué significa esto? Que si yo tengo información de distinta índole y quiero almacenarla en un solo lugar, lo voy a poder hacer con estos arreglos.

#### Creación de arreglos

Los arreglos tienen una sintaxis en específico, es decir, una manera exclusiva de escribirlos. Para que nosotros podamos identificar un arreglo necesitaremos utilizar los caracteres de los corchetes. Al usar estos caracteres podrás identificar un arreglo, así cuando estés trabajando en cualquier lugar y veas que hay corchetes de por medio significa que todo lo que está dentro de ese lugar son elementos de un arreglo. Los arreglos se componen de casillas que parten en 0, las cuales equivalen a las posiciones que tendrán los elementos dentro del arreglo.

```js
var platillos = ['ceviche','tacos','pasta']; // Creación mediante corchetes
var bebidas = new Array('Jamaica', 'Chicha Morada', 'Pozol'); // Creación mendiante objeto Array

/*Para comprabar que una variable es un arreglo se debe utilizar el metodo isArray()*/
var esArreglo = Array.isArray(platillos);
console.log(esArreglo); // true porque es un arreglo
```

#### Medir y acceder en JS a un arreglo

Cuando trabajamos con arreglos, va a haber dos cosas que vamos a necesitar saber indudablemente ante cualquier operación. La primera de ellas es cuánto mide nuestro arreglo, y la segunda de ellas es cuál es la información (acceder a la información) que se encuentra en determinada posición de nuestro arreglo.

```js
/*Se define un arreeglo de platillos*/
var platillos = ['ceviche','tacos','pasta'];
```

- **Tamaño de un arreglo:** Para medir el tamaño de un arreglo se debe utilizar el metodo `lenght`.

```js
var largoArreglo = platillos.length; //Se guarda el largo del arreglo en la variable largoArreglo
console.log(`Hay ${largoArreglo} platillos en el menú`);
```

- **Acceder al contenido de un arreglo:** Como se dijo con anterioridad, existen posiciones dentro de los arreglos las cuales comienzan en el 0, estas posiciones son llamadas **indices** y estos nos permitaran acceder al contenido que se encuentra en el indice determinado.

```js
var platillo1 = platillos[0]; //Contiene el valor que se encuentra en la posición 0, o sea, ceviche.
var platillo2 = platillos[1]; //Contiene el valor que se encuentra en la posición 1, o sea, tacos.
var platillo3 = platillos[2]; //Contiene el valor que se encuentra en la posición 2, o sea, pasta.

var menu = `El menú de hoy esta compuesto por:
- ${platillo1}
- ${platillo2}
- ${platillo3}`;

console.log(menu)
```

#### Arreglos Multidimensionales

En un arreglo podemos almacenar distintos tipos de datos: datos numéricos, cadenas de texto, "booleanos", incluso otros arreglos. Cuando trabajamos con arreglos dentro de otros arreglos, es decir, cuando almacenamos un arreglo dentro de otro arreglo, estos se conocen como **arreglos multidimensionales**.

```js
/*Un arreglo multidimensional (matriz) se define como un arreglo que contiene arreglos*/

// Ejemplo
var matriz = [[1,2],[3,4]]; // Arreglo Multidimensional de 2 x 2

/*Para ingresar al contenido del arreglo es necesario indicar dos parametros (en los arreglos es una sola posición el parametro) la posición del arreglo dentro del arreglo más grande y la posición del contenido dentro del arreglo al cual se accede con la primera posición indicada*/

console.log(matriz[0][0]); // 1
console.log(matriz[0][1]); // 2
console.log(matriz[1][0]); // 3
console.log(matriz[1][1]); // 4
```

Lo siguiente es un ejemplo de como iterar un arreglo multidimensional.

```js
/*En este ejmplo se muestran por consola el contenido de los arreglos*/

var platillos = ["ceviche", "tacos", "pasta"];
var paises = ["Perú", "México", "Italia"];
//Se puede agregar al arreglo de arreglos menu
//var mascotas = ["Perro", "Gato", "Hamster"];

var menu = [ platillos, paises];

// Algoritmo para recorrer una matriz con dimensiones desonocidas
for(var i=0;i<menu.length;i++){
  // Primer for para recorrer las filas
  for(var j=0;j<menu[i].length;j++){
    // Segundo for para recorrer las columnas
    console.log(menu[i][j]);
  }
  console.log('\n'); // Salto de línea para separa el contenido de los arreglos
};

console.table(menu); // Se despliega como tabla en la consola
```

#### Operaciones básicas de un arreglo

En un arreglo puedo tener ciertas operaciones básicas que me ayudarán a procesar mejor los datos cuando estoy integrándolos o trabajándolos dentro o fuera de un arreglo. Estas operaciones básicas o métodos son los siguientes:

- **push():** Permite agregar al final del arreglo uno o más elementos sin la necesidad de uno tener que agregar de forma manual un elemento al arreglo ya defenido.

```js
var lenguajesProgramacion = ["Python"]; // Se crea un arreglo que contiene un elemento

lenguajesProgramacion.push("C"); // Al final del arreglo se agrega el elemento "C"
lenguajesProgramacion.push("C++"); // Al final del arreglo se agrega el elemento "C++"

// Lo anterior se podría haber hecho en una sola línea entregando los dos elementos separados por una coma
//lenguajesProgramacion.push("C", "C++");

console.log(lenguajesProgramacion); // ["Python","C","C++"]
```

- **pop():** Este metodo extrae el úlitmo elemnto del arreglo, no recibe ningún parametro. Al utilizar este metodo, el arreglo se modifica por lo cual el último elemento ya no se encontrará en el arreglo (se recomienda guardarlo en una variable o algo por el estilo en el caso de necesitarlo a futuro)

```js
/*En el este ejemplo se utilizaq el arreglo final del ejemplo de uso de push()*/

//var lenguajesProgramacion = ["Python","C","C++"];

var ultimoElemento = lenguajesProgramacion.pop(); // Se define una variable que contendrá lo que se obtiene de usar pop() sobre un arreglo

console.log(ultimoElemento); // C++
console.log(lenguajesProgramacion); // ["Python","C"]
```

- **join():** Se encarga de transformar todos los elementos del arreglo en una sola cadena de texto.

```js
/*En el este ejemplo se utilizaq el arreglo final del ejemplo de uso de pop()*/

//var lenguajesProgramacion = ["Python","C"];
var arregloTexto = lenguajesProgramacion.join();
console.log(arregloTexto); // Python,C
```

#### Generación de arreglos con split(), from() y of()

La generación de arreglos no está ligada exclusivamente a tener una variable seguida de los corchetes y están ingresando los datos en ese momento. De hecho, tenemos algunos métodos que nos pueden servir para poder crear un arreglo desde 0.

- **split():** Permite tranformar en arreglo una cadena de texto que tenga elementos separados por algun delimitador, por ejemplo, comas.

```js
var mensaje = "ceviche, tacos, pasta";
var platillos = mensaje.split(', '); // Se separan los elementos que están separados por una comay un espacio
console.log(platillos); // ["ceviche","tacos","pasta"]
```

- **Array.from():** 

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title></title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>

<body>
    <!--En el cuerpo se encuentra una divisón que contiene a la clase platillos, la cual contiene 3 parrafos que tienen un nombre de platillo cada uno-->
    <div class="platillos">
        <p>Ceviche</p>
        <p>Tacos</p>
        <p>Pasta</p>
    </div>
    <script src="js/app.js"></script>
</body>

</html>
```

```js
/*Creación de un arreglo desde la información que se encuentra en el HTML*/

var platillosHTML = Array.from(document.querySelectorAll('.platillos p')) /*Trae la información desde el HTML. Al querySlectorAll se le entrega el nombre de la clase y etiqueta p. Al hacer esto, se genera un arreglo formal que tiene toda la información de la etiqueta por lo cual hay información que no es necesaria pero al ser un arreglo como tal, tiene métodos que ayudarán a aislar solamente el contenido de la propiedad textContent, la cual contiene el texto del parrafo, o sea, los platillos*/

/*El arreglo que se busca generar necesita solamente lo que se encuentra en la propiedad textContent por lo cual se utilizara el método .map() el cual permitará realizar el mapeo de los elementos que se necesiten para trabajar (mediante una iteración continua que no requiere algún iterador para usarse), o sea, los platillos contenidos en cada parrafo*/

var platillos = platillosHTML.map( platillo => platillo.textContent) // El método recibe un parametro (no importa el nombre), una flecha => y la propiedad que se necesita.

console.log(platillos); // ["Ceviche","Taco","Pasta"]
```

- **Array.of():** Todo lo que se le entregue como parametro, se convertirá en un arreglo.

```js
var platillos = Array.of("ceviche", "tacos", "pasta");

console.log(platillos) // ["ceviche","tacos","pasta"]
```

#### Ordenando un arreglo

En los arreglos, generalmente, vamos a guardar colecciones grandes de datos. Estos datos, muchas veces, los vamos a presentar en una tabla o en pantalla de manera ordenada o de manera desordenada, lo cual es una actividad que debe ir por usabilidad en casi todas las páginas web o aplicaciones que estén presentando datos. Para los arreglos existen unos métodos que ayudaran a darle algún tipo de orden a estos, estos métodos son:

```js
/*Se definiran dos arreglos que se utilizaran como ejemplo para los métodos*/
var platillos = ["Ceviche", "Tacos", "Pasta"]; // Arrglo que contiene strings
console.log('Antes: ', platillos); // Se muestra el contenido antes de aplicar los metodos

var numeros = [4,5,1,3,9,8,7,3]; // Arreglo que contiene numeros
console.log(`Arreglo antes del orden: ${numeros}`); // Se muestra el arreglo antes de aplicar los metodos
```

- **.sort():** Ordena el arreglo de una forma logica, por ejemplo, alfabeticamente, de mayor a menor, etc, si fuera un arreglo con numeros y letras, se separan los numeros de las letras, etc.

```js

// Ordenamiento del arreglo de Strings
platillos.sort(); 
console.log('Ordenado: ', platillos); 

// Ordenamiento del arreglo de numeros
numeros.sort();
console.log(`Arreglo después de ordenar (uso de .sort()): ${numeros}`);
```

- **.reverse():** Cambia el orden del arreglo desde atrás hacia delando, lo que significa que ahora el último se encuentra en la posición inicial y el elemento de la posición inicial se encuentra en el final del arreglo.

```js
// El arreglo de strings ordenado, se le revierte el orden
platillos.reverse(); 
console.log('Al reves: ', platillos);

// El arreeglo de numeros ordenado, se le revierte el orden
numeros.reverse();
console.log(`Arreglo después de revertir el orden (uso de .reverse()): ${numeros}`);
```

Hay que siempre recordar que los metodos anteriores trabajan sobre el mismo arreglo, por lo cual se recomienda hacer un backup del estado inicial del arreglo.

#### Desestructuración de arreglos

Con los arreglos en JavaScript, también podemos trabajar con algo llamado desestructura o desestructuración de arreglos. ¿Esto qué es? Es como una asignación a la inversa. El fin de esto es guardar en variables por separado cada uno de los elementos del arreglo.

```js
// Se define un arreglo de Strings que se utilizará como ejemplo
var platillos = ["ceviche", "tacos", "pasta", "tostadas"];

// Recordar descomentar los bloques de código para probarlos y comentar los que ya se probaron

// Se pueden dejar cada uno de los elementos de la siguiente manera
/*
var platillo1 = platillo[0];
var platillo2 = platillo[1];
var platillo3 = platillo[2];
var platillo4 = platillo[3];
console.log(platillo1, platillo2, platillo3, platillo4);
*/

// Se puede desestructurar definiendo variables con valor nulo y asiendo una asginación multiple
/*
var platillo1 = null;
var platillo2 = null;
var platillo3 = null;
var platillo4 = null;

[platillo1, platillo2, platillo3, platillo4] = platillos; // Cada elemento del arreglo queda guardado en una de las variables definidas

console.log(platillo1, platillo2, platillo3, platillo4);
*/

// Se puede hacer lo anterior pero saltandose el paso de tener que definir la variables con null

var [platillo1, platillo2, platillo3, platillo4] = platillos; // En la misma línea se definen las variables que contendran por separado los elementos del arreglo

console.log(platillo1, platillo2, platillo3, platillo4);
```

### Búsquedas en Arreglos

#### Iterando arreglos con for... in

Además de tener el ciclo *for* o alguna estructura de control como el *while* o el *do while*, también contamos con una variante del ciclo *for* para poder iterar dentro de un arreglo. En este caso, este "loop" que vamos a utilizar se llama *for in*. A diferencia del *for* ya conocido, el *for...in* solo requiere de la definición del iterador y que se le indique el arreglo en el cual iterará. Sabiendo lo anterior. lo que hará *for...in* será iterar tantas veces como el largo del arreglo, o sea, sería como un cilo for normal que inicia en 0 y va iterando uno en uno las pocisiones hasta el final del arreglo. Cabe mencionar que al igual que en el ciclo for normal, el iterador va dando la posición del elemento y no el elemento en si.

```js
var platillos = ["ceviche", "tacos", "pasta"];

// i es el iterador el cual iterará in el arreglo platillos
for ( let i in platillos) {
    console.log(platillos[i])
}

/*Siempre hay qu erecordar que el contexto es necesario para luego entender de mejor manera el código por lo cual se recomienda que el iterador sea lo más explicito y acorde al contexto de lo que se está obteniendo del arreglo. En el ejemplo en vez de llamar i al iterador, se le puede poner platillo denido a que el arreglo está lleno de platillos*/
```

#### Iteración de arreglos con forEach()

Otra manera que tenemos de iterar directamente sobre un arreglo es utilizando el método *forEach()*, que está ligado directamente a los arreglos. Este tipo de métodos lo que va a recibir es una función y podemos utilizar una función anónima o un *arrow function*, **se recomienda más el uso de arrow function**. La función que recibe este metodo está compuesta por el parametro que fungirá de iterador, la flecha que indica que es lo que se hará con el elemento que se guarda en el parametro/iterador (este metodo extrae directamente el elemento, a diferencia del for normal o el for... in que trabajan con la posiciones de los elementos en el arreglo) y por último lo que se hará con el elemento, en el caso de que esto último sea más de una acción sólo se debe poner llaves que delimiten el bloque de código que se ejecutará y un return que devolverá el dato que se quiere reotrnar.

```js
// Ejemeplo en donde se mostrará por consola todos los elementos del arreglo
var platillos = ["ceviche", "tacos", "pasta"];
platillos.forEach( platillo => console.log(platillo) ) // Cada elemento del arreglo se mostrará por consola
```

Cabe mencionar que de todas formas se puede obtener el indice del elemento dentro del arreglo, lo anterior se logra de la siguiente manera:

```js
var platillos = ["ceviche", "tacos", "pasta"];
platillos.forEach( (platillo, index) => console.log(index, platillo) ) // Cada elemento junto con su posición se mostrarán por consola
```

#### Buscar en arreglo con JS

Una de las operaciones más buscadas por todo programador es la operación de la búsqueda. Sí, cuando trabajamos con un arreglo, a veces necesitamos buscar determinado dato dentro del arreglo. Y muy probablemente tu arreglo sea muy grande o contenga muchísima información, para lo cual va a ser muy importante que podamos tener un método óptimo para esto. Con la evolución de JavaScript, se han presentado nuevos métodos y uno de estos métodos es el método llamado *find*, que me va a permitir a mí iterar sobre un arreglo sin necesidad de utilizar un ciclo y, a partir de esto, recuperar la información que yo quiero. Para utilizar este metodo será necesaria una *arrow function* y una variable que guarde el elemento encontrado. El metodos deja de buscar en la primera coincidencia que encuentra y en el caso de no enconrar ninguna, la variable contendrá el valor *undefined*.

```js
// Ejemplo arreglo simple
var platillos = ["ceviche", "tacos", "pasta"];

var pElegido = platillos.find( platillo => platillo === "tacos");
/*En pElegido se guarda la coincidencia*/

console.log(pElegido)
```

```js
// Ejemeplo arreglo de objetos

var menu = [
	{nombre: 'Ceviche', precio: 20, pais: 'Perú'},
	{nombre: 'Tacos', precio: 10 , pais: 'México'},
	{nombre: 'Pasta', precio: 50, pais: 'Italia'},
  {nombre: 'Tacos', precio: 60, pais: 'USA'}
];

var pElegido = menu.find( platillo => platillo.nombre === 'Tacos');
/*En este caso en la variable pElegido quedará guardada toda la información perteneciente a la coincidencia encontrada, no sólo el nombre de la coincidencia*/

console.log(pElegido)
```

#### Búsqueda de índice de elementos

En algunas circunstancias no vamos a necesitar acceder al objeto que hayamos encontrado en el arreglo. Al contrario, necesitamos encontrar el índice donde se encuentra nuestro dato, lo anterior se lográ gracias al metodo *.findIndex()*. Este metodo al igual que el metodo *.find()*, recibe una *arrow function* que se encargará de indicar la coincidencia que se quiere encontrar y el indice de la coincidencia quedará almacenado en la variable en la cual se guarda todo el codigo anterior. Cabe mencionar que si no se encuentre ninguna coincidencia, se almacena el valor *-1* y que tanto este metodo como el metodo *.find()* son sensibles a las mayusucalas y minusculas.

```js
// Ejemplo con arreglo de Strings

var platillos = ["ceviche", "tacos", "pasta"];

var numPlatillo = platillos.findIndex( platillo => platillo == 'tacos' ); // El indice de la coincidencia se guarda en la variable numPlatillo

console.log("Platillo número: ", numPlatillo); // Se muestra por consola el indice de la coincidencia
```

```js
// Ejemplo con arreglo de Onjetos

var menu = [{
        nombre: 'Ceviche',
        precio: 20,
        pais: 'Perú'
    },
    {
        nombre: 'Tacos',
        precio: 10,
        pais: 'México'
    },
    {
        nombre: 'Pasta',
        precio: 50,
        pais: 'Italia'
    }
]

var numPlatillo = menu.findIndex( platillo => platillo.nombre == 'Pasta' );

console.log("Platillo número: ", numPlatillo);
```

#### Filtrar arreglos usando JS

Este metodo se recibe los mismos parametros que el metodo *.find()* pero a diferencia de este que detiene la busqueda en el momento que encuentra la primera coincidencia, *.filter()* retorna un arreglo con todas las coincidencias que encuentra.

```js
var menu = [{
        nombre: 'Ceviche',
        precio: 20,
        pais: 'Perú'
    },
    {
        nombre: 'Tacos',
        precio: 10,
        pais: 'México'
    },
    {
        nombre: 'Pasta',
        precio: 50,
        pais: 'Italia'
    },
    {
        nombre: 'Quesadillas',
        precio: 15,
        pais: 'México'
    }
];

var resultado = null;


//resultado =  menu.find(platillo => platillo.pais === 'México'); // Solo entrega la primera coincidencia


resultado =  menu.filter(platillo => platillo.pais === 'México'); // Entrega un arreglo con todas las coincidencias donde el pais del platillo sea México

console.log(resultado);
```

#### Validación de elementos de un Arreglo

Existen metodos que sirven para validar si existen o no elementos dentro del areglo que cumplan con condiciones que establecidad. Estos metodos son *.some()* y *.every()* los cuales entregan un booleano, en el caso de *.some()* retorna un *true* siemrpe y cuando al menos uno de los elementos cumplan con la condición establecida, en cambio, *.every()* entrega un *true* solamente si todos los elementos del arreglo cumplen con la condición preestablecida.

```js
var resultado = null;
var resultado2 = null;

var menu = [{
        nombre: 'Ceviche',
        precio: 20,
        pais: 'Perú'
    },
    {
        nombre: 'Tacos',
        precio: 10,
        pais: 'México'
    },
    {
        nombre: 'Pasta',
        precio: 50,
        pais: 'Italia'
    },
    {
        nombre: 'Quesadillas',
        precio: 15,
        pais: 'México'
    }
]


resultado = menu.some( platillo => platillo.precio <= 10);
console.log('¿Hay platillos abajo de 20? ', resultado); // true

resultado2 = menu.every( platillo => platillo.precio <= 60); 
console.log('¿Todos los platillos cuestan menos de 10? ', resultado2); // true
```

### Conociendo el DOM y el BOM

#### Entender el DOM y el BOM

Para entender el DOM y el BOM se usará el siguiente ejemplo en HTML, en el cual tendremos un etiqueta script para el código de JavaScript que se relaciona tanto con el DOM como con el BOM.

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title></title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>

<body>
    <h1 class="title">Lorem ipsum</h1>
    <button id="boton">¡Púlsame!</button>
    <div id="container">
        <p class="principal">
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus sapien nulla, tincidunt nec ante ut, porta tempus dui. Integer
            consequat rhoncus tempus. Etiam nulla nisl, mattis a nisl pulvinar, tempor elementum lectus. Morbi sed tortor
            luctus, faucibus dolor eu, ullamcorper arcu. Aenean condimentum quis nisi et malesuada. Morbi nec mi et turpis
            condimentum suscipit quis vel arcu. Vestibulum at mi vitae urna gravida consectetur. Nam suscipit ac purus a
            bibendum.
        </p>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus sapien nulla, tincidunt nec ante ut, porta tempus dui. Integer
            consequat rhoncus tempus. Etiam nulla nisl, mattis a nisl pulvinar, tempor elementum lectus. Morbi sed tortor
            luctus, faucibus dolor eu, ullamcorper arcu. Aenean condimentum quis nisi et malesuada. Morbi nec mi et turpis
            condimentum suscipit quis vel arcu. Vestibulum at mi vitae urna gravida consectetur. Nam suscipit ac purus a
            bibendum.
        </p>
        <p>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus sapien nulla, tincidunt nec ante ut, porta tempus dui. Integer
            consequat rhoncus tempus. Etiam nulla nisl, mattis a nisl pulvinar, tempor elementum lectus. Morbi sed tortor
            luctus, faucibus dolor eu, ullamcorper arcu. Aenean condimentum quis nisi et malesuada. Morbi nec mi et turpis
            condimentum suscipit quis vel arcu. Vestibulum at mi vitae urna gravida consectetur. Nam suscipit ac purus a
            bibendum.
        </p>
    </div>

    <script>
        //********************************
        //*** Entendiendo el DOM y el BOM

        var boton = document.getElementById("boton"); // Ejemplo 1 DOM

        boton.addEventListener('click', function () {
           console.log(window.location.href);

            window.location.href = 'http://github.com/yacafx'; // Ejemplo 2 BOM
        })

    </script>

</body>

</html>
```

##### DOM (Document Object Model

Para que JavaScript pueda liberar todo su poder es necesario de un mecanismo que me permita interactuar con HTML e incluso con CSS. Este mecanismo se llama **Document Object Model** (Modelo Objeto del Documento en español) o lo podemos conocer también como DOM. La principal característica del DOM es que nos permite usar los elementos o etiquetas que componen una página web como objetos y así poder manipularlos con JavaScript. De una manera resumida, el DOM es el puente entre HTML y JavaScript, pues al poder usar o referirnos a los elementos que componen nuestro sitio o aplicación, podremos manipular a nuestro gusto y necesidad todo lo que hayamos creado.

```js
/*Ejemplo 1 DOM, extraido del Ejemplo de HTML anterior*/

var boton = doucment.getElemntById("boton"); // En el código HTML existe un id boton el cual sirve para que .getElementById obtenga todo lo relacionado al id y lo guarde en la variable boton

/*Al elemento botón se le agrega un addEventListener, o sea, un escucha que se encargue de hacer algo cuando se lleve a cabo cierta acción sobre el boton que se encuentra en el código HTML*/
boton.addEventListener('click', function(){
  console.log("Presionaste el botón"); // Esto es un ejemplo de una acción que se puede realizar al presionar el botón
})
```
Hay que recordar que si se tiene el código de JS en un archivo aparte, hay que importarlo a HTML con la siguiente línea de código:

```html
<!--Recordar que la siguiente etiqueta va dentro del body-->
  <script src="ubicacion/archivo.js"></script>
```
##### BOM (Browser Object Model)

El BOM significa **Browser Object Model**, y también, al igual que el DOM, están definidos por la W3C, que es la organización que se encarga de dictar los estándares web a nivel mundial. Para evitar confusiones, existen algunos objetos independientes que hacen referencia tanto al BOM como al DOM. Y si lo vemos en perspectiva, el BOM es el contenedor o padre principal, y dentro vive el DOM. Para el DOM ya tenemos el objeto *document* que habíamos visto, pero para el caso del BOM tenemos otro objeto. Este objeto se llama *window* y también tiene sus propios métodos y sus propiedades, así que pueden actuar de manera independiente pero podemos coordinar su operación.

```js

// Se utilizó de base el Ejemplo 1
var boton = doucment.getElemntById("boton"); // En el código HTML existe un id boton el cual sirve para que .getElementById obtenga todo lo relacionado al id y lo guarde en la variable boton

/*Al elemento botón se le agrega un addEventListener, o sea, un escucha que se encargue de hacer algo cuando se lleve a cabo cierta acción sobre el boton que se encuentra en el código HTML*/
boton.addEventListener('click', function(){
  console.log(window.location.href); // window.location.href muestra la dirección donde se encunetra alojado el código
  window.location.href = 'http://github.com/yacafx'; // al presionar el botón se redireccionara al link
  /*Ambas línea de código anteriores utilizan el elemento window del BOM*/
})
```

#### Propiedades y métodos del DOM

- **.getElementsById():** Este metodos hace referencia a el elemento por su id. Recibe como parametro el id del elemento que se quieren obtener.

```js
var boton = document.getElementById("id");
```

- **.getElementsByTagName():** Este metodos hace referencia a todos los elementos que tengan la misma etiqueta. Recibe como parametro la etiqueta de los elementos que se quieren obtener.

```js
var todosLosParrafos = document.getElementsByTagName('etiqueta');
```

- **.getElementsByClassName():** Este metodos hace referencia a todos los elementos que tengan la misma clase. Recibe como parametro la clase de los elementos que se quieren obtener. Este método captura todo los elementos que tengan la clase y los guarda en un arreglo por lo cual para acceder a uno en especifico se debe manejar como un areglo.

```js
var parrafoPorClase = document.getElementsByClassName('nombreClase')[0].textContent;
```

**Para obtener solamente el texto del id, clase o etiqueta, se debe anexar un *.textContent* luego de los parenesis que reciben el parametro**

En JS también se puede manejar las propiedades de los objetos del HTML, como por ejemplo, el color, forma o tamaño de un botón.

- **.createElement():** Este método permite crear etiquetas para HTML de forma dinamica. Para insetar el elemento en el `<body></body>` se debe utilizar `document.body.appendChild(elementoAInsertar);` en el código de JS.

```js
var foto = document.createElement('img'); // Secreará una etiqueta imagen
foto.src = "foto1.jpg"; // ubicación de la foto
foto.name = "foto1"; // Nombre de la foto
foto.width = 400; // Tamaño de a foto
document.body.appendChild(foto); // Donde se insertará la foto
```

A este nuevo elemento se le puede agregar un *.addEventListener()* con el cual poder ejecutar algún tipo de instrucción cuando se interactué con él. Un ejemplo de lo anterior es el siguiente código que hace que cambie la imagen cada vez que se hace click sobre ella (hay que establecer la direción de las imagenes antes de correr el código).

```js
foto.addEventListener('click', function () {
  if (this.name === 'foto1') {
    this.src = 'foto2.jpg'; // Cambiar ubicación por la de donde se encuentren las imagenes que uno quiere poner
    this.name = 'foto2';
    } else {
      this.src = 'foto1.jpg'; // Cambiar ubicación por la de donde se encuentren las imagenes que uno quiere poner
      this.name = 'foto1';
      }
})
```

#### Propiedades y métodos del BOM

Ya trabajamos con el DOM, es decir, con el objeto del documento. Ahora vamos a trabajar con el navegador, y para esto ahora utilizaremos el objeto *window*. En este caso, el objeto *window* tiene muchas propiedades entre las que podemos encontrar:

- **window.innerHeight y window.innerWidth:** Permiten obtener el alto y ancho del área de contenido de la ventana. Cabe mencionar que no es necesario escribir window. antes de los métodos, se pueden escribir directamente, pero de otdas formas se recomienda utilizar el objeto window con el fin de que el método o propiedad funcione correctamente.

```js
console.log('innerHeight: ', window.innerHeight);
console.log('innerWidth: ', window.innerWidth);
```

- **localStorage:** Este objeto es *window.localStorage* (pertenece al objeto *window*) el cual permite hacer cosas con respecto al almacenamiento local del navegador, lo almacenado se encuentra en la sección *Application* que se encuentra al inspeccionar elementos de la página web. Entre las cosas que se pueden hacer con este objeto se encuentra lo siguiente:

  - **localStorage.setItem:** El utilizar este tipo de método sirve para guardar algunos datos como, por ejemplo, algun "token", algún nombre usuario, algún texto que no necesitemos que vaya al servidor, etc. Este método recibe un par de datos los cuales son *el campo del contenido* y *el contenido*. Para recuperar el contenido se debe utilizar el método *.getItem(campoDelContenido)*.

  ```js
  localStorage.setItem('contenido','Código y café es una gran combinación'); // En el localStorage se guarda los parametros
  var contenido = localStorage.getItem('contenido'); // Se obtine y guarda en una variable el texto que se guardó en localStorage bajo el campo "contenido"
  console.log(contenido); // Se muestra por consola "Código y café es una gran combinación"
  ```

Ahora que tenemos nociones tanto del DOM como del BOM, se mostrará un ejemplo que combina métodos de ambos para cambiar un parafo al parecionar un botón que s eencunetra en la página.

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title></title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
</head>

<body>
    <h1 class="title">Lorem ipsum</h1>
    <button id="boton">¡Púlsame!</button>
    <div id="container">
        <p class="principal">
            Parrafo 1 <br> Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus sapien nulla, tincidunt nec ante
            ut, porta tempus dui. Integer consequat rhoncus tempus. Etiam nulla nisl, mattis a nisl pulvinar, tempor elementum
            lectus. Morbi sed tortor luctus, faucibus dolor eu, ullamcorper arcu. Aenean condimentum quis nisi et malesuada.
            Morbi nec mi et turpis condimentum suscipit quis vel arcu. Vestibulum at mi vitae urna gravida consectetur. Nam
            suscipit ac purus a bibendum.
        </p>

    </div>

    <script src="app.js"></script>

</body>

</html>
```
```js
/*Esto sería el código que iría en el archivo app.js al que se hace referencia en el código HTML anterior*/
var boton = document.getElementById('boton');
var principal = document.getElementsByClassName('principal')[0];

console.log('innerHeight: ', window.innerHeight);
console.log('innerWidth: ', window.innerWidth);

localStorage.setItem('contenido', 'Código y café es una gran combinación') // Se gurda en localStorage del navegador una frase


boton.addEventListener('click', function () {
  var contenido = localStorage.getItem('contenido'); // Desde localStorage se obtiene la frase asociada a el campo "contenido" y se almacena en la variable contenido
  principal.innerHTML = contenido; // principal.innerHTML lo que hará es reemplazar todo el contenido almacenado orginalmente por lo que almacena contenido
  /*Los siguientes son métodos utiles para manipular la navegación de la página*/
  window.history.forward(); // Avanzar en el historico 
  window.history.back(); // Retorceder en el historico del navegador
  window.history.go(3); // mover a través del historico del navegador
})
```

**Para saber más métodos tanto del DOM como del BOM se peude acudir a la documentación que existe tanto por parte de Mozilla como del sitio w3schools**

### Trabajar con datos remotos o externos

#### Obtener datos con fetch

Con JavaScript podemos conectarnos a datos remotos o a archivos con datos que tengamos almacenados localmente. De hecho, esta es una característica muy recurrente en casi todos los sistemas, aplicaciones o páginas web que vayas a desarrollar. Probablemente hayas escuchado que hay muchos servicios en Internet que te ofrecen algo llamado API, esto es un mecanismo para que puedas consumir sus datos. Por ejemplo, servicios como Spotify, YouTube, Flickr, etc., tienen disponible ese tipo de API y, de hecho, muchos sistemas también que no son tan públicos tendrán disponible este tipo de sistemas, para lo cual será necesario que tengas un mecanismo para conectarte.

Lo siguiente es un ejemplo compuesto por un HTML que tiene una sección llamada contenerdo y un botón, y código de JS con el cual se interactuara con los elementos del HTML.

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title></title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        h1 {
            border-top: 2px solid #ccc;
            text-transform: uppercase;
            font-size: 18px;
        }

        p {
            font-family: Verdana, Geneva, Tahoma, sans-serif;
            box-shadow: 5px 5px 5px #ccc;
            padding: 10px;
        }

        button {
            width: 100%;
            height: 50px;
            font-size: 16px;
            border-radius: 5px;
            outline: none;
            color: white;
            font-weight: bold;
            background-color: steelblue;
        }
    </style>
</head>
<!--El cuerpo contiene el botón al que se le aplica el estilo anterior-->
<body>
    <button id="boton">Traer datos</button>
    <div id="contenedor">

    </div>

    <script src="app.js"></script>
</body>

</html>
```

```js
var boton = document.getElementById('boton');
var contenedor = document.getElementById('contenedor');
var posts = null;
/*Al presionar sobre el botón, */
boton.addEventListener('click', function () {

    /*fetch es un método que recibe la URL o link donde se encuentren los datos que se quieren consumir. Este método trabaja en base a promesas, pero ¿qué es una promesa? Todos hemos hecho una promesa alguna vez donde a quien le hacemos la promesa se queda esperando hasta que nosotros la hagamos porque confía que en algún momento nosotros la cumplamos. Lo mismo va a suceder con los datos, los datos van a trabajar con promesas, dado que van a solicitar la información a algún servicio remoto y van a quedar a la espera de esos datos.*/

    fetch('http://jsonplaceholder.typicode.com/posts') // Desde la URL se extrae un JSON que contiene los parametros a utilizar (userId, id, title y body)

    /*Lo que sigue es un preformateo de los datos, lo cual es algo que siempre hay que hacer cuando se trabaja con el método fetch*/
    
    .then(data => data.json()) /*.then es un método que hace referencia a "Luego de que...", en este caso luego de que se obtengan los datos, se ejecuta cierta acción. La arrow function anterior lo que hace es transformar la data recibida en un archivo .json. Cada nuevo .then es una nueva promesa.*/

    .then(data => {
        posts = data;  // Se asigna el contenido de data a la variable posts
        mostrarDatos(posts)  // Se pasa el contenido de post a la función mostrarDatos
    })

});

/*Función que genera de forma dinámica los elementos que irán en el cuerpo del HTML*/
function mostrarDatos(posts) {
    posts.map((post, i) => {
        /*Se almacena la creación de una título h1 y un parrafo p en variables titulo y contenido*/
        let titulo = document.createElement('h1');
        let contenido = document.createElement('p');

        /*Se crea un titulo de forma dinamica conteniendo el indice (i + 1), un guión y el título (post.title) que trae el objeto correspondiente al indice de la iteración*/        
        titulo.innerHTML = (i + 1) + " - " + post.title;

        /*Se crea un parrafo con el atributo body proveniente del JSON*/
        contenido.innerHTML = post.body;

        /*Se agrega tanto el título como el contenido a la sección <div id="contenedor"> </div> del HTML*/
        contenedor.appendChild(titulo);
        contenedor.appendChild(contenido);
    })
}
```

#### Trabajar con promesas en JavaScript

Los siguiente bloques de código son el código HTML y CSS necesario para que en el navegador un botón al ser presionado, traiga todos el texto y las imagenes de banderas desde dos url distintos, todo esto gracias a la implementación de JS en el botón.

```html
<!--Código HTML para practicar promesas-->
<!DOCTYPE html>
<html lang="en">

<head>
    <title></title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        h1 {
            border-top: 2px solid #ccc;
            text-transform: uppercase;
            font-size: 18px;
        }

        p {
            font-family: Verdana, Geneva, Tahoma, sans-serif;
            box-shadow: 5px 5px 5px #ccc;
            padding: 10px;
        }

        button {
            width: 100%;
            height: 50px;
            font-size: 16px;
            border-radius: 5px;
            outline: none;
            color: white;
            font-weight: bold;
            background-color: steelblue;
        }

        img {
            border: 1px solid gray;
            margin: 5px;
            background-color: #ccc;
        }
    </style>
</head>

<body>
    <button id="boton">Traer datos</button>
    <h1>Banderas</h1>
    <div id="banderas">

    </div>
    <hr>
    <h1>POSTS</h1>
    <div id="contenedor">

    </div>

    <script src="app.js"></script>
</body>

</html>
```

```js
/*Código JS para practicar el uso de promesas*/
var boton = document.getElementById('boton');
var contenedor = document.getElementById('contenedor');
var contBanderas = document.getElementById('banderas');

// Al clickear el botón del códgio HTML se ejcuta el código
boton.addEventListener('click', function () {
    
    getPosts() // Trae todos los post y gracias a que getPosts() retorna una promesa da la posibilidad de utilizar una promesa
        .then(data => data.json()) // Se formatea la información para que quede en formato JSON
         // Luego del formateo, se reciben los datos
        .then(posts => {
            mostrarDatos(posts);
            //Una promesa puede retornar un promesa y así sucesivamente
            return getCountries(); // Esto genera una nueva promesa
        })
        .then(data => data.json()) // Se formatea la información para que tenga formato JSON
        .then(countries => {
            mostrarBanderas(countries); // Muestra la información de las countries
        });

});

// Función que obtiene datos desde la url indicada, retorna una promesa
function getPosts() {
    return fetch('http://jsonplaceholder.typicode.com/posts');
}

// Se importan los datos de los paises desde la URL indicada, retorna una promesa 
function getCountries() {
    return fetch('https://restcountries.eu/rest/v2/all');
}

// Muestra todo lo relacionado a Countries en modo de imagen en el HTML. Lee donbde se encuentra una bandera y genera una imagen
function mostrarBanderas(countries) {
    contBanderas.innerHTML = '';
    countries.map((country, i) => {
        let bandera = document.createElement('img');
        bandera.src = country.flag;
        bandera.width = '20';
        bandera.height = '20';
        contBanderas.appendChild(bandera);
    })
}

// Muestra todo el contenido de los POST
function mostrarDatos(posts) {
    contBanderas.innerHTML = '';
    posts.map((post, i) => {
        let titulo = document.createElement('h1');
        let contenido = document.createElement('p');

        titulo.innerHTML = (i + 1) + " - " + post.title;
        contenido.innerHTML = post.body;

        contenedor.appendChild(titulo);
        contenedor.appendChild(contenido);
    })
}
```
#### Manejo de los errores en Javascript

Muchas veces nos vamos a enfrentar a errores y errores que no van a depender de nosotros. Por ejemplo, ¿qué sucede si los servicios que estamos consumiendo no están disponibles o los datos en algún momento se malformaron y no llegó bien la información? ¿O simplemente no tenemos acceso a Internet y, por tanto, no podemos consumir datos? Bueno, también es muy importante que podamos manejar los errores y reaccionar ante ellos.

Para capturar errores al momento de utilizar fetch y promesas se utiliza el método `.catch()`, el cual recibe una *arrow function*

```html
<!DOCTYPE html>
<html lang="en">

<head>
    <title></title>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1">
    <style>
        h1 {
            border-top: 2px solid #ccc;
            text-transform: uppercase;
            font-size: 18px;
        }

        p {
            font-family: Verdana, Geneva, Tahoma, sans-serif;
            box-shadow: 5px 5px 5px #ccc;
            padding: 10px;
        }

        button {
            width: 100%;
            height: 50px;
            font-size: 16px;
            border-radius: 5px;
            outline: none;
            color: white;
            font-weight: bold;
            background-color: steelblue;
        }

        img {
            border: 1px solid gray;
            margin: 5px;
            background-color: #ccc;
        }
        
        /*Regla para la etiqueta que tiene como id="mensaje"*/
        #mensajes {
            width: 90%;
            height: 50px;
            margin: 0 auto;
            background-color: lightcoral;
            margin-top: 10px;
            padding: 10px;
            border-radius: 5px;
            color: white;
            text-align: center;
        }
        /*La clase hide hace que cualquier elemento HTML con esta clase, se oculte cuando carga la página */
        .hide {
            display: none;
        }
    </style>
</head>

<body>
    <button id="boton">Traer datos</button>
    <!--En el caso de exista un error, la información del error se irá a la división div-->
    <div id="mensajes" class="hide"></div>
    <h1>Banderas</h1>
    <div id="banderas">

    </div>
    <hr>
    <h1>POSTS</h1>
    <div id="contenedor">

    </div>

    <script src="app.js"></script>
</body>

</html>
```

```js
var boton = document.getElementById('boton');
var mensajes = document.getElementById('mensajes');
var contenedor = document.getElementById('contenedor');
var contBanderas = document.getElementById('banderas');

boton.addEventListener('click', function () {
    getPosts()
        .then(data => data.json())
        .then(posts => {
            mostrarDatos(posts);
            return getCountries();
        })
        .then(data => data.json())
        .then(countries => {
            mostrarBanderas(countries);
        })
        // El método catch captura todos los errores que suscedan
        .catch(error => {
             mensajes.classList.toggle('hide'); // .toggle remueve o agrega algo según se requiera. En este caso remueve la clase hide
             mensajes.innerHTML = error; // En el div antes definido en el HTML se mostrará el error que haya ocurrido
             setTimeout(() => mensajes.classList.toggle('hide'), 6000); /*Luego de 6 segundos, el mensaje desaparece porque se agrega la clase hide otra vez con .toggle()*/
        })
});

function getPosts() {
    return fetch('http://jsonplaceholder.typicode.com/posts');
}

function getCountries() {
    return fetch('https://restcountries.eu/rest/v2/allm'); //Se le agrego una m al final para provocar un error que mostrar
}

function mostrarBanderas(countries) {
    contBanderas.innerHTML = '';
    countries.map((country, i) => {
        let bandera = document.createElement('img');
        bandera.src = country.flag;
        bandera.width = '20';
        bandera.height = '20';
        contBanderas.appendChild(bandera);
    })
}

function mostrarDatos(posts) {
    contBanderas.innerHTML = '';
    posts.map((post, i) => {
        let titulo = document.createElement('h1');
        let contenido = document.createElement('p');

        titulo.innerHTML = (i + 1) + " - " + post.title;
        contenido.innerHTML = post.body;

        contenedor.appendChild(titulo);
        contenedor.appendChild(contenido);
    })
```

### Programación orientada a objetos

La programación orientada a objetos es un tema fascinante, porque nos facilitará mucho del trabajo que tenemos que hacer cuando estemos programando.

#### Trabajar con clases en laprogramación orientada a objetos

Los siguiente es la sintaxis más común con la que se trabajan las clases.

```js

/*Esta es la sintaxis con la que se define una clase*/
class Pantalla {
    constructor() {

    }
}

/*Tanto tvSala como tvHabitacion son objetos del tipo Pantalla
Para generar una nuevo objeto del tipo Pantalla, se debe utilizar 
la palabra new seguida de la clase a la que pertenecerá el objeto*/
const tvSala = new Pantalla(); // Declaración objeto
const tvHabitacion = new Pantalla();
```

#### Objetos: sus métodos y sus propiedades

En la programación orientada a objetos, las clases son el elemento base que se necesita para poder comenzar con este paradigma. Ahora, también se requieren de otros elementos, como son las propiedades y como son los métodos. Las propiedades van a describir al objeto que estamos creando y los métodos le van a dar vida. Es como si fuera una persona. Las propiedades son su color de piel, su color de cabello, su estatura, su peso. Y los métodos son las cosas que puede hacer, por ejemplo, puede caminar, puede brincar, puede correr, puede sentarse, etc. Entonces, lo que estamos haciendo con la programación orientada a objetos es hacer una analogía o una metáfora de la vida real pero en un código, es decir, en la computadora.

```js

class Pantalla {
    /*En el constructor se colocan las propiedades necesarias para que el objeto se inicialice*/
    constructor(marca, modelo, pulgadas) {
        /*El dato entregado en la declaración de un obejto se asignan al objeto utiilizando el obejeto this. (hace referencia a la instancia que se está trabajando)*/
        this.marca = marca; // Propiedad
        this.modelo = modelo; // Propiedad
        this.pulgadas = pulgadas; // Propiedad
    }
    /*Método*/
    encendido() {
        console.log(`La pantalla ${this.marca} se ha encendido`);
    }

    /*Los métodos de un obejto no necesitan la palabra reservada function para declararlos. Para utilizar los métodos, se debe escribir lo siguiente:
    objeto.metodo()*/
    /*Método*/
    volumen() {
        console.log(`El volumen se ha modificado`); // Acciones que realizará el método del objeto
    }
    /*Método*/
    info() {
        console.log(`La pantalla ${this.marca} de modelo ${this.modelo} es de ${this.pulgadas} pulgadas`);
    }
    /*En el caso que se quiera asignar nuevas propiedades al objeto sin estos estar declarados en el constructor, se debe hacer un método set propiedad(valor){} y si se quiere poder acceder a ese dato, se debe crear un método get propiedad(){return this.propiedad}
    
    Para poder setear la nueva propiedad, se debe escribir lo siguiente: objeto.nuevaPropiedad = valor;
    Para obtener el valor de la nueva propiedad, se debe escribir lo siguiente: objeto.nuevaPropiedad;
     */

    set peso(value) {
        this.kgs = value.trim();
    }

    get peso() {
        return this.kgs;
    }
}

const tvSala = new Pantalla('Master', 'Oasis', 55); // Declaración del obejto pantalla con sus propiedades 
const tvHabitacion = new Pantalla('Origin', 'Artemis', 80);
```

#### Herencia de métodos y propiedades

Cuando trabajamos con programación orientada a objetos, muchas veces creamos plantillas o clases muy genéricas. Y este tipo de clases nos van a servir porque a partir de estas se van a derivar otras clases, es decir, vamos a tener clases padre y vamos a tener clases hijo.

Teniendo dos clases, estás pueden ser independiente una de la otra pero, si se quiere que la segunda clase **extienda** de la primera, o sea, que herede tanto sus métodos como sus propiedades, se debe utilizar la palabra reservada `exteds` seguida de la clase desde la cual se heredan los métodos y propiedades. Ejemplo de lo anterior sería:

```js
class claseHija extends clasePadre{
    constructor(propiedadConstructoraPadre,propiedadUno, propiedadN){
        super(propiedadConstructuraPadre)
        this.propiedadUno = propiedadUno;
        this.propiedadN = propiedadN;
    }

    metodoUno(){
        // código
    }

    metodoDos(){
        // código
    }

    get propiedadUno(){
        return this.propiedadUno
    }
}
```

Cabe destacar que existe una palabra reservada llamada `static` la cual permite que un método (investigar que más) sea accesible sin la necesidad de crear una instancia de la clase, lo cual permite que se pueda llamar sólo con el nombre dado a la plantilla de la clase. 

```js
/*Clase padre llamada Producto*/
class Producto {
    constructor(numSerie) {
        this.numSerie = numSerie;
        this.tiempoGarantia = 100;
    }

    /*La palabra reservada static hace que el metodo infoTienda() este disponible aunque no se genere una nueva clase*/
    static get infoTienda() {
        console.log(`Productos de la tienda Patito Inc`);
    }

    set garantia(value) {
        this.tiempoGarantia -= value;
    }

    get garantia() {
        return this.tiempoGarantia;
    }
}

/*Clase hija proveniente de la clase padre Producto*/
class Pantalla extends Producto  {
    constructor(numSerie, marca, modelo, pulgadas) {
        super(numSerie) // Super constructor que hace referencia al constructor de la clase padre, lo que implica que es necesario que la clase hijo, reciba las propiedades necesarias establecidas por el constructor del padre.
        this.marca = marca;
        this.modelo = modelo;
        this.pulgadas = pulgadas;
    }

    encendido() {
        this.garantia = 1;
        console.log(`La pantalla ${this.marca} se ha encendido`);
    }

    volumen() {
        console.log(`El volumen se ha modificado`);
    }

    info() {
        console.log(`La pantalla ${this.marca} de modelo ${this.modelo} es de ${this.pulgadas} pulgadas`);
    }

    set peso(value) {
        this.kgs = value.trim();
    }

    get peso() {
        return this.kgs;
    }
}

const tvSala = new Pantalla('13579','Master', 'Oasis', 55);
const tvHabitacion = new Pantalla('24680','Origin', 'Artemis', 80);
```

### Solución y manejo de errores en JS

#### Manejo de errores en JS

Para manejar los errores en JS, existe una estructura llamada *try and catch* (se escribe como un if/else anidado) la cual se compone por un bloque *try* en el cual se escribirá todo el código que quiera ser probado, y un bloque *catch*, en el cual se pondrá el código que ayudará a mostrar e identificar el error que exista en el código del bloque *try*

```js
/*Ejemplo sencillo de la estructura try and catch*/
try {
    var array = new Array(10000000000); // Error de largo del arreglo
} catch (error) {
    console.log(error) // Muestra el error en consola
}
```

```js
/*Ejemplo sencillo dos de la estructura try and catch*/
try {
    var x=y; // Variable y no se encuentra definida
} catch (error) {
    console.log(error) // Muestra el error en consola
}
```

Los errores (el `error` del bloque *catch*) se componen por un `error.message` y `error.name` los cuales también pueden ser utilizados por separados.

```js
try {
    decodeURIComponent("http://%ominio.com");
} catch (error) {
    console.log(error.message) // Muestra por consola el mensaje del error
    console.log(error.name) // Muestra por consola el nombre del error
}
```

#### Generación de errores personalizados con JS

Cuando nos enfrentamos a una nueva aplicación o un nuevo proyecto, lo que tenemos que hacer primero generalmente es planear cuáles van a ser todos los flujos de datos que se van a seguir en nuestra aplicación. Pero algo que olvidamos generalmente hacer es planear también los errores. ¿Por qué planear los errores? Porque también es muy importante que le puedas decir tú al usuario en que está mal y así el usuario tenga la facilidad de resolver o corregir sus datos de entrada ante el sistema que tú hayas hecho. Para esto, nosotros podemos trabajar con errores personalizados. Así, una vez que tú tengas identificados todos los posibles errores que lleguen a suceder puedas lanzar mensajes adecuados ante cada situación. 

Para generar un error personalizado se utiliza la palabra reservada `throw` (la cual hace referencia a la detonación de algo) y el objeto *Error* que se define como `new Error("Aquí va el mensaje de error")`. En el siguiente bloque de código se muestra como quedría en JS la implementación de lo que se explicó anteriormente.

```js
throw new Error("Aquí ve el mensaje del error personalizado")
```

La creación de errores personalizados permite que los bloques de código *catch* puedan obtener el error relacionados al código que se está probando.

```js
var valor1 = 10;
var valor2 = 20;

try {
    /*Si la condición se cumple entrega un mensaje. Cualquier otro resultados falso se considera un error*/
    if (valor1 > valor2) {
        console.log(`Mensaje de validación: ${valor1} si es mayor que ${valor2}`); 
    } else {
        throw new Error(`${valor1} no es mayor que ${valor2} :(`)
    }

} catch (error) {
    console.log(error);
}
```

De esta manera, se pueden detonar cuantos errores se necesiten, no hay un delimitante, aunque se recomienda que se planeen adecuadamente para no saturar de mensajes innecesarios al usuario.

#### Depurar código en JS

La base de toda aplicación o de todo desarrollo en el cual estaremos trabajando siempre es la correcta planeación. Es decir, nosotros debemos planear, previamente a escribir el código, cuál va a ser el algoritmo que vamos a estar utilizando. Para esto, puedes utilizar una hoja de papel e ir escribiendo todos los pasos que se van a ir detonando en tu aplicación. Una vez que nosotros tenemos estos pasos bien definidos, entonces ya pasamos a la parte de escribir código. La parte más difícil de la programación no es escribir el código o aprender un nuevo lenguaje. De hecho, es la generación de ese algoritmo que te va a permitir solucionar un problema. Cuando tú ya estás trabajando en el código y terminaste tu algoritmo correctamente, entonces viene la etapa de pruebas y comienzas a tratar de ejecutar tu aplicación. Muchas veces, puedes encontrarte con problemas. Tal vez lo hayas planeado correctamente en el papel, pero algo en la escritura salió mal, entonces es cuando nosotros necesitamos depurar nuestra aplicación o "debuggear" nuestra aplicación, es decir, encontrar errores que muy probablemente hayamos dejado pasar por alto. Para lo anterior, existe el navegador, en el caso de google chrome (navegadores basados en chromium), existe una pestalla llamada *Sources*, en donde se puede ejecutar y probar todo el código de la aplicación. 

Para saber si algo sucede dentro del código, el navegador entrega lo que se denomina *breakpoint*, los cuales son puntos en tu programa que te van a permitir detener la ejecución en ese momento para que tú puedas hacer pruebas. Para generar un breakpoint, se debe presionar sobre el numero de la línea de código en la cual se quiere establecer el breakpoint. Con la tecla *Esc* se puede abrir la consola, con la cual se trabajará para hacer cosas con el programa. Cuando se ejecuta el programa, en el debugger se observará la pausa en el breakpoint y en los costados se podrá ver información relacionada a la línea de código en la cual se estableció el breakpoint.

**Seguir desarrollando**

#### Uso del debugger

A veces, nuestro código va a ser muy grande, es decir, vamos a tener demasiadas líneas de código que hacen que si utilizamos esta opción que tenemos en pantalla para utilizar el "debugger" hagan el proceso demasiado complicado. Por lo cual, nosotros tenemos una palabra reservada llamada'debugger' que podemos utilizar con Google Chrome, y esto es que nosotros, en el momento que deseemos, en nuestro programa podemos utilizarla para que se detenga en la ejecución, esto sin necesidad de tener escrito un "breakpoint", el cual, nosotros, como habíamos visto, podemos agregar en cualquier momento y si lo queremos quitar, bueno, damos también un clic sobre este "breakpoint" y se elimina.

```js
var boton = document.getElementById('boton');
var contenedor = document.getElementById('contenedor');
var contBanderas = document.getElementById('banderas');

boton.addEventListener('click', function () {
    getPosts()
        .then(data => data.json())
        .then(posts => {
            mostrarDatos(posts);
            return getCountries();
        })
        .then(data => data.json())
        .then(countries => {
            mostrarBanderas(countries);
        });
});

function getPosts() {
    return fetch('http://jsonplaceholder.typicode.com/posts');
}

function getCountries() {
    return fetch('https://restcountries.eu/rest/v2/all');
}

function mostrarBanderas(countries) {
    contBanderas.innerHTML = '';
    countries.map((country, i) => {
        let bandera = document.createElement('img');
        bandera.src = country.flag;
        bandera.width = '20';
        bandera.height = '20';
        contBanderas.appendChild(bandera);
    })
}

function mostrarDatos(posts) {
    contBanderas.innerHTML = '';
    posts.map((post, i) => {
        
        debugger; // El debugger del navegador se detiene para saber que sucede con los posts
        
        let titulo = document.createElement('h1'); // Cada stepover que se haga en el navegador, mnostrará lo que sucede al ejecutarse la siguiente línea de código.
        let contenido = document.createElement('p');

        titulo.innerHTML = (i + 1) + " - " + post.title;
        contenido.innerHTML = post.body;

        contenedor.appendChild(titulo);
        contenedor.appendChild(contenido);
        /*En el caso de que se quiera continuar la ejecución de todo el código, hay que presionar de forma prolongada el botón play "Resume script execution" para presionar en en el otro botón play que permite continuar la ejecución sin pausas*/
    })
}
```

### Despedida del curso JS esencial

El alcance que tiene JavaScript en la actualidad es bastante grande, y todo lo que has aprendido a lo largo de este curso te servirá para que puedas comenzar y puedas trabajar con este lenguaje. Pero es muy importante que conozcas algunas de las herramientas más importantes y conocidas que te pueden servir o con las cuales te encontrarás en el camino.

#### Consideraciones generales con JS

- **Node.js:** Node es un entorno para poder trabajar en servidor pero con JavaScript, así entonces podemos ejecutar código de JavaScript como si ejecutaras código de Java o código de PHP o código de algún otro tipo de lenguaje.

- **Webpack:** Actualmente tenemos muchos archivos con los cuales vamos a trabajar y Webpack nos permite empaquetar todo en muy pocos archivos o incluso, en ciertas circunstancias, en un solo archivo. Entonces, las recomendación es: aprende y conoce sobre este empaquetador para que puedas agilizar tu trabajo. 

- **ESLint:** Si estás escribiendo mal una sintaxis o tienes algún error que desees solucionar, esta herramienta te dará las claves para que puedas agilizar ese proceso.

- **TypeScript:** TypeScript es un transpilador. ¿Qué es eso? Hay muchas características que existen y que se van agregando a JavaScript pero que no todos los navegadores soportan. La labor de TypeScript es hacer un transpilado, es decir, convertir este código, con todas las cosas nuevas que casi todos los navegadores no soportan, a un código que realmente pueda soportarlo. Esto es posible gracias a TypeScript. 

- **Frameworks:** AngularJS, React o Vue, que te van a permitir a ti trabajar de una manera más ágil con el lenguaje. Estos no son más que "frameworks" que te van a facilitar tu labor como programador.

- **Desarrollo de aplicaciones nativas:** Si te animas a trabajar con algunas aplicaciones nativas tendrás algunas herramientas como NativeScript o como Ionic. 

El alcance de JavaScript es tan grande que también podemos **trabajar con bases de datos**, es decir, podemos integrar muchas cosas de JavaScript a bases de datos, como es el caso de **MongoDB cuando trabajamos en ella con archivos de tipo JSON**. Pero, bueno, como te das cuenta, el universo que maneja JavaScript es bastante amplio y hay muchas líneas de especialización. Mi recomendación es: trata de conocerlas todas y de utilizar siempre muy buenas prácticas para que puedas adaptar cualquiera de ellas sin ningún problema.

#### Conclusiones y despedida del curso JS esencial

Este curso llegó a su fin, pero no te preocupes, hay mucho JavaScript por delante. A lo largo de este curso, pudiste aprender muchas cosas. Por ejemplo, desde trabajar con estructuras de control y variables como, por ejemplo, en el ciclo'for' donde pudiste aprender cómo iterar sobre una colección de datos. También aprendiste sobre la manera tradicional de crear una función y también cómo crear funciones anónimas o las llamadas "arrow functions", que será un recurso muy necesario en todos tus desarrollos. Incluso llegamos a utilizar algunos métodos más simples, pero a la vez sofisticados, para buscar contenido dentro de un arreglo, como cuando trabajábamos con el método'find'. Y creo que uno de los ejercicios que más disfrutamos fue cuando nos conectamos a datos remotos. Sí, cuando pulsábamos un botón y nos traíamos una colección de "posts" y una colección de banderas de servicios que estaban en otro servidor. Creo que todos estos ejercicios y ejemplos que estuvimos viendo alrededor del curso te serán muy útiles en tu labor como programador. No olvides siempre consultar este contenido para que puedas tener a la mano toda la información que necesites cuando estás trabajando y, aun así, siempre aprender más sobre JavaScript y documentarte en Internet. Hay muchísima información ahí afuera que puede servir y muchas herramientas que se generan y actualizan día a día. JavaScript es un gran lenguaje, y si estás aquí tienes un gran futuro como programador. Muchas gracias.

**TODO LO QUE HAY EN ESTA SECCIÓN PROVIENE DE APUNTES PROPIOS DE CRISTOPHER SOTO Y LAS TRANSCRIPCIONES DEL CURSO JAVASCRIPT ESENCIAL IMPARTIDO POR SERGIO BRITO EN LINKEDIN LEARNING**

## JavaScript avanzado: Buenas prácticas

Día a día, todos los desarrolladores de "software", ya sea web o de escritorio, nos encontramos con prácticas comunes que siempre agregamos a nuestro proceso de desarrollo. Algunas, porque ya las conocemos y sabemos que funcionan bien. Otras, porque hemos visto y comprobado que a otros desarrolladores les funciona bien y lo usan como una práctica general. Soy Sergio Brito y en esta serie de vídeos conocerás las mejores prácticas para trabajar y desarrollar aplicaciones web con JavaScript. Conocerás y aprenderás cómo replicar estas prácticas comunes que otros desarrolladores han aplicado con resultados exitosos y que podrás aplicar a tu proyecto. Siempre es recomendado que, por cada lenguaje de programación nuevo que conozcamos, después de aprender los conceptos básicos, nos familiaricemos con las buenas prácticas de desarrollo del lenguaje en cuestión. Estas son las buenas prácticas. Aquellas que, por el uso común entre desarrolladores, indican un buen resultado si se aplica en un entorno adecuado. Aplicar las buenas prácticas a todo desarrollo que hagas es un buen hábito que todo desarrollador de "software" debe hacer con cada nuevo proyecto que realice para así tener una base sólida de código, con el cual lograr una aplicación exitosa y, sobre todo, muy profesional.

### Introducción a las buenas prácticas con JS

#### Objetivos de buenas práctivas con JS

El objetivo de este curso es que puedas conocer las mejores prácticas de trabajo con JavaScript. Prácticas que van a ir desde la integración con variables, algunas estructuras y objetos, algunos cálculos que podemos llegar a evitar, el trabajo con Estilo, formas de declarar un variable, para qué me sirve la "indentación", cómo trabajar con un punto y coma, cómo puedo trabajar con comentarios y también generar documentación de mi aplicación con solo escribir el comentario, así como también estaremos repasando algunos puntos sobre organización de código. Organización de código que me va a permitir optimizar mis consultas y mis cálculos, así como también evitarme la duplicidad o establecer bloques bastante bien definidos sobre el uso de funciones. Y del mismo modo, algunas cuestiones sobre "performance" como el uso de alguna notación de objetos, como es JSON, para la manipulación de datos, o cómo poder estar nosotros realizando pruebas de rendimiento directamente en nuestro código, trabajando con JavaScript y la consola de nuestro "browser". Del mismo modo, podrás aprender cómo podemos "minificar" y ofuscar código para que nuestro trabajo sea muchísimo más sencillo. Y el uso de algunas herramientas como puede ser JSHint o JSLink para poder encontrar errores y tener un código bastante limpio y sofisticado en nuestro proyecto de desarrollo web.

#### Requesitos antes de comenzar el curso

Es muy importante que, antes de comenzar, sepas que debes de contar con los conocimientos básicos de programación y haber trabajado ya un poco, al menos, con JavaScript. Esto dado que estaremos nosotros revisando las buenas prácticas de trabajo con esta herramienta, por lo cual es muy recomendable que ya hayas tenido un acercamiento previo con este. Así, entenderás cuál es la razón de que esta buena práctica se esté aplicando. No es importante que tengas un conocimiento sobre CSS o sobre HTML profundo, pero sí que tengas las bases también de HTML. Entonces, en resumen, debes contar con el conocimiento básico de HTML, haber trabajado ya, aunque sea un poco, o interactuado en los conceptos más básicos, con JavaScript y contar con un editor de texto. Con estos tres elementos, en conjunto, podrás sacar mayor provecho de este curso sobre las buenas prácticas de trabajo con JavaScript.

### Prácticas generales en JS

#### Aprende HTML y CSS

La potencia que tiene JavaScript está dada principalmente por la relación que tiene con otros lenguajes, como lo es HTML y las Cascadas de Estilo. Por tanto, es muy importante tener al menos el conocimiento básico sobre cómo funciona cada uno de estos lenguajes y la relación que tiene con JavaScript, pues es precisamente la relación entre estos lenguajes lo que provoca que tengamos aplicaciones web bastante robustas y bastante llamativas, dado que esto funciona de una manera muy ligada. Por ejemplo, HTML da toda la estructura que va a tener una página o una aplicación web. CSS 3, en este caso, provee toda la vista que el usuario va a poder estar contemplando al momento de acceder a una página o algún sitio web. Y JavaScript, obviamente, va a proveer toda la interacción en la cual el usuario va a poder sacar provecho de la información contenida en el sitio. Como ves, entonces, la combinación de estas tres herramientas es muy importante. Por lo cual, si tú tienes un conocimiento bastante robusto sobre CSS3 y HTML, es por seguro que podrás sacar gran provecho de JavaScript y llevar tus aplicaciones web al máximo.

#### Primero JS

Uno de los errores más comunes de muchos desarrolladores y diseñadores web de la actualidad es que buscan primero comenzar a trabajar con JavaScript desde un "framework". Es decir, buscan primero aprender el uso de herramientas como jQuery, AngularJS o React, por ejemplo, para poder trabajar directamente con JavaScript. Cuando la realidad es que primero hay que aprender JavaScript, puesto que este es el lenguaje que da pie a "frameworks" de esta talla y a herramientas tan poderosas como puede ser Cordova, PhoneGap o Ionic. La idea es que primero trabajes y entiendas cómo funciona JavaScript antes de aventurarte a trabajar con otros "frameworks" que, si bien te van a facilitar la vida, es necesario que tengas unas bases sólidas sobre el uso de JavaScript. Si logras tener una base sólida utilizando JavaScript, desde la resolución de problemas hasta la implementación de estos u otros "frameworks", te van a hacer muchísimo más sencilla la labor de estar desarrollando una aplicación o un sitio web.

#### Especificación y documentación de JS

Siempre una buena práctica va a ser poder consultar la especificación, documentación o referencias del lenguaje en el que estemos trabajando. Y tal es el caso con JavaScript. Es muy recomendable que puedas entrar directamente al [documento de especificación (ECMAScript 2022)](https://tc39.es/ecma262/) y consultar todas las características que tiene. Muy probablemente aquí puedes resolver muchos problemas que se te presentan día a día. Aunque haya libros bastante especializados sobre algún tema en específico o sobre temas en general de JavaScript, nada se compara a la especificación original del lenguaje. O, por ejemplo, consultar alguna referencia que existe en la web, donde podrás encontrar cuestiones desde cómo se aplican determinadas características de la herramienta, hasta detalles de la librería y estos cómo te van a poder ayudar. La documentación es pieza clave en todo desarrollo web. Por tanto, no le tengas miedo y comienza a ocuparlo, para que puedas conseguir el mayor provecho de todo desarrollo que vayas a trabajar.

### Variables, estructuras y objetos en JS

#### Uso de variables en JS

#### Variables globales en JS

#### Palabras reservadas en JS

#### Cálculos innecesarios con JS

#### Objetos y funciones anónimas en JS

#### For in en JS

#### Validad objetos en JS

#### Expresiones booleanas en JS

#### Operador ternario en JS

#### Igualdad con JS

#### Constructores de obejtos en JS

#### Try and catch en JS

#### Literales en JS