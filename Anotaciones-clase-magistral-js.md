# Recomendaciones
- Tener una carpeta para los JS

- Hay que importar las librerias en el orden correcto para evitar problemas

- No es recomendable trabajar todo en un sólo archivo 

- Dividir toma más tiempo, si uno caga el siguiente igual ya que hay dependencia, es como que fuera una conexión en serie

- Los id son para cosas unicas (en CSS no se utilizan mucho porque no son reutilizables)

- Una funcion anonoima es aquella sin nombre

# Anotaciones 
- Funciona en el navegador

- También funciona en el navegar con Node.js

- Las APIS con bloques de códigos de otra persona que nos dejan ocupar, de HTML sería todo lo que se puede ocupar con documents."submetodo"

- Un problema con JS es su alcance

## //Output
- console (es una clase que prmite interactuar con la consola del enterno en el que se ejecuta el script)

- console.log() permite que se le ingrese cualqueir tipo de dato "hola", 12, hasta objetos y los imprime bonitos 

## //Comments
- Es con doble slash es para una línea y es más recomendable, para un parrafo// <--- o /* */

## //Variable declaration
- JS no es un lenguaje fuertemente tipido por lo cual se puede cambiar el tipo de varible cuando uno quiera 
- Poner el punto y coma al final de cada línea no es necesario pero es una buena práctica 

- Formas de declarar la variable
     ```js
        var a = "Variable"; //Soportada por todos los navegadores, siempre tiene alcance global 
    ```
     ```js
        const b = "Const"; //Puede no ser reconocida, su valor no puede ser alterado y el alcance es en funcion de su bloque de declaración                  
    ```
    ```js
         let c = "JS may you let to do this"; // El alcance es lo mismo que el anterior 
    ```
## //FlowControl

- Los de toda la vida (usar goto no es recomendable)

## //Scope (Alcance)

- Las variables globales son peligrosas

- No declar el tipo es equivalente a declarar un VAR

## //Operators

## //Comparators - Coertion

- Tengo que tener cuidado con esto, poniendo un === (estricatamente igual) en cambio el == es un quizás se parece

## //Data types
 - Son clases por lo cual tiene distintos metodos

 - Declarar un numero (let n=0) tiene metodos pero no serán los mismos de Number.

 - undefined (la variable no tiene valor o sea que no está definida) y null (la variable vale null) no son iguales

     ### For
     - No hay que definir el int como en C

     ### Array

    ```js
        let list = ['asd', 123]; //Definiendo uno
    ```
    - Son los de toda la vida, tienen metodos como concat, entries (mostrar entradas) 
    
     ### Functions

     ```js
        function greet (name)
            console.log("hola " + name)
     ```
     - greet es un tipo de variable exclusivo de las funciones o sea que es equivalente a un int pero de funciones se pueden definir cosas del tipo greet y todo

     ```js
        const g = greet;
        g(crus);
        console.log(greet);
     ```

     - En JS casi todo son funcions u objetos 

     - Se pueden declarar sin poner el function (ver lo que mande el jacob)

     - Las funciones siempre devuelven una sola cosa

     ### Objects (antes de ES6 se usaban para todo)
     
     - this.lo que sea: es un puntero que hace referencia a lo que se le ponga después del punto 

     - Se pueden poner objetos dentro de los objetos

     ### Clases

     - Se parecen más a python que a C

     - Se pone class el nombre de la clase y se ocupan llaves de toda la vida 

     - Es una forma más sofisticada de utilizar clases  funciones

     - Por cosas de buena cosa hay que declarar afuera del contructor una variable vacia la cual se rellenará 

     - Se recomienda tener algo ya definido en la clase para que en el caso de que no entreguen nada exista algún resultado por defecto 

