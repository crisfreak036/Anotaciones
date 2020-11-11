
# Anotaciones del curso Conviértete en desarrollador web full-stack de LinkedIn

## Aprende Visual Studio Code

### Diferencias entre un editor de texto y un IDE

- Los editores de textos contienen herramientas como un bloc de notas con estaminas.
- Los IDE son entornos integrados de desarrollo.

La diferencia más grande entre ambos radica enla cantidad de herramientas con las cuales se va a desarrollar. Los IDE vienen con todas las herramientas precargadas en cambio los editores de texto no vienen con todas las herramientas, hay que ir instalándolas según se vayan necesitando.

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

- **Seleccionar un trozo de texto en todos los lugares del código:** Por ejemplo, se selecciona una variable y luego se presiona *CTRL + D*, se seleccionará la variable en todos los lugares del código donde aparece, luego de esto se puede cambiar donde se seleccionó y el cambio se hará en todo el código. Cabe mencionar que los cambios se pueden hacer en cualquier lugar de lo seleccionado gracias a un multicursos que se posiciona en todas las selecciones.

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

### Strict Mode (Modo estricto)

Sirve para asegurar que el código de JS que se está escribiendo, está siendo correcto y no se están cometiendo errores como la utilización de palabras reservadas o la no declaración de una variable, etc.

Para activarlo hay que dirigirse al archivo JS y poner lo siguiente:

```js
"use strict" // Activa el modo de estricto, debe estar al inicio del código
```

### Trabajando con variables en JS

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

### Contenedores Let

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

### Contenedores Const

Este contenedor es para las variables que se mantendrán constantes y nunca cambiarán,por lo cual cualquier variable que sea declarada con este tipo de contenedor, su valor no podrá ser modificado de ninguna forma mientras la aplicación se esté ejecutando.

```js
const constante1 = 34;
console.log(constante1);
const constante1 = 35; // Lanzará un error porque no se puede cambiar el valor de la variable constante1
console.log(constante1); 
```

### Trabajar con números en JavaScript

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

### Trabajar con cadenas de texto o String 

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

### Uso de los datos booleanos

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

### Trabajar con fechas en JavaScript

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

### Uso de símbolos en JavaScript 

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

### Estructurando datos con JSON

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