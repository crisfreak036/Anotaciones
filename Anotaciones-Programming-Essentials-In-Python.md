# Anotaciones Curso PCAP

## ¿Cómo funciona un programa de computadora?

Un programa hace que una computadora sea utilizable. Sin un programa, una computadora, incluso la más poderosa, no es más que un objeto. Del mismo modo, sin un pianista, un piano no es más que una caja de madera.

Una computadora puede ejecutar solo operaciones extremadamente simples, por ejemplo, una computadora no puede evaluar el valor de una función matemática complicada por sí misma, aunque esto no está más allá de los límites posibles en un futuro próximo.

Imagina que quieres saber la velocidad promedio que has alcanzado durante un largo viaje. Sabes la distancia, sabes el tiempo, necesitas la velocidad.

Naturalmente, la computadora podrá calcular esto, pero la computadora no es consciente de cosas como la distancia, la velocidad o el tiempo. Por lo tanto, es necesario instruir a la computadora para que:

- Acepte un número que represente la distancia.
- Acepte un número que represente el tiempo de viaje.
- Divida el valor anterior por el segundo y almacene el resultado en la memoria.
- Muestre el resultado (representando la velocidad promedio) en un formato legible.

Estas cuatro acciones simples forman un **programa**. Por supuesto, estos ejemplos no están formalizados, y están muy lejos de lo que la computadora puede entender, pero son lo suficientemente buenos como para traducirlos a un idioma que la computadora pueda aceptar.

La palabra clave es el **lenguaje**.

## Lenguajes naturales vs. Lenguajes de programación

Un lenguaje es un medio (y una herramienta) para expresar y registrar pensamientos. Hay muchos lenguajes a nuestro alrededor. Algunos de ellos no requieren hablar ni escribir, como el lenguaje corporal. Es posible expresar tus sentimientos más profundos de manera muy precisa sin decir una palabra.

Otro lenguaje que empleas cada día es tu lengua materna, que utilizas para manifestar tu voluntad y para pensar en la realidad. Las computadoras también tienen su propio lenguaje, llamado **lenguaje máquina**, el cual es muy rudimentario.

Una computadora, incluso la más técnicamente sofisticada, carece incluso de un rastro de inteligencia. Se podría decir que es como un perro bien entrenado, responde solo a un conjunto predeterminado de comandos conocidos.

Los comandos que reconoce son muy simples. Podemos imaginar que la computadora responde a órdenes como "Toma ese número, divídelo por otro y guarda el resultado".

Un conjunto completo de comandos conocidos se llama **lista de instrucciones**, a veces abreviada **IL** (por sus siglas en inglés de *Instruction List*). Los diferentes tipos de computadoras pueden variar según el tamaño de sus IL y las instrucciones pueden ser completamente diferentes en diferentes modelos.

**Nota: los lenguajes máquina son desarrollados por humanos**.

Ninguna computadora es actualmente capaz de crear un nuevo idioma. Sin embargo, eso puede cambiar pronto. Por otro lado, las personas también usan varios idiomas muy diferentes, pero estos idiomas se crearon ellos mismos. Además, todavía están evolucionando.

Cada día se crean nuevas palabras y desaparecen las viejas. Estos lenguajes se llaman **lenguajes naturales**.

## ¿Qué hace un lenguaje?

Podemos decir que cada idioma (máquina o natural, no importa) consta de los siguientes elementos:

- Alfabeto: Un conjunto de símbolos utilizados para formar palabras de un determinado idioma.

- Léxico (Diccionario): Un conjunto de palabras que el idioma ofrece a sus usuarios.

- Sintaxis: Un conjunto de reglas (formales o informales, escritas o interpretadas intuitivamente) utilizadas para precisar si una determinada cadena de palabras forma una oración válida.

- Semántica: Un conjunto de reglas que determinan si una frase tiene sentido.

**La IL es, de hecho, el alfabeto de un lenguaje máquina. Este es el conjunto de símbolos más simple y principal que podemos usar para dar comandos a una computadora. Es la lengua materna de la computadora.**

Desafortunadamente, esta lengua está muy lejos de ser una lengua materna humana. Todos (tanto las computadoras como los humanos) necesitamos algo más, un lenguaje común para las computadoras y los seres humanos, o un puente entre los dos mundos diferentes.

Tales lenguajes son a menudo llamados **lenguajes de programación de alto nivel**. Son algo similares a los naturales en que usan símbolos, palabras y convenciones legibles para los humanos. Estos lenguajes permiten a los humanos expresar comandos a computadoras que son mucho más complejas que las ofrecidas por las IL.

Un programa escrito en un lenguaje de programación de alto nivel se llama **código fuente** (en contraste con el código de máquina ejecutado por las computadoras). Del mismo modo, el archivo que contiene el código fuente se llama archivo fuente.

## Compilación vs. Interpretación

La programación de computadora es el acto de establecer una secuencia de instrucciones con la cual se causará el efecto deseado.

Por supuesto, tal composición tiene que ser correcta en muchos sentidos, tales como:

- Alfabéticamente: Un programa debe escribirse en una secuencia de comandos reconocible, por ejemplo, el Romano, Cirílico, etc.- 
- Léxicamente: Cada lenguaje de programación tiene su diccionario y necesitas dominarlo; afortunadamente, es mucho más simple y más pequeño que el - diccionario de cualquier lenguaje natural.
- Sintácticamente: Cada idioma tiene sus reglas y deben ser obedecidas.
- Semánticamente: El programa tiene que tener sentido.

Hay dos formas diferentes de **transformar un programa de un lenguaje de programación de alto nivel a un lenguaje de máquina**:

- Compilación: **El programa fuente se traduce una vez (sin embargo, esta ley debe repetirse cada vez que se modifique el código fuente)** obteniendo un archivo (por ejemplo, un archivo .exe si el código está diseñado para ejecutarse en MS Windows) que contiene el código de la máquina; ahora puedes distribuir el archivo en todo el mundo; el programa que realiza esta traducción se llama compilador o traductor.

- Interpretación: Tú (o cualquier usuario del código) puedes traducir el programa fuente cada vez que se ejecute; el programa que realiza este tipo de transformación se denomina intérprete, ya que interpreta el código cada vez que está destinado a ejecutarse; también significa que no puede distribuir el código fuente tal como está, porque el usuario final también necesita que el intérprete lo ejecute.

**Nota: La diferencia radica en que la compilación se hace una vez hasta que se modifica el código donde se debe volver a compilar. Por otro lado está la interpretación que hace que el código se interprete cada vez que se ejecute existan o no cambios en el código fuente.**

Debido a algunas razones muy fundamentales, un lenguaje de programación de alto nivel particular está diseñado para caer en una de estas dos categorías.

Hay muy pocos idiomas que se pueden compilar e interpretar. Por lo general, un lenguaje de programación se proyecta con este factor en la mente de sus constructores: ¿Se compilará o interpretará?

## ¿Qué hace realmente el intérprete?

Supongamos una vez más que has escrito un programa. Ahora, existe como un archivo de computadora: un programa de computadora es en realidad una pieza de texto, por lo que el código fuente generalmente se coloca en archivos de texto. Nota: debe ser texto puro, sin ninguna decoración, como diferentes fuentes, colores, imágenes incrustadas u otros medios. Ahora tienes que invocar al intérprete y dejar que lea el archivo fuente.

El intérprete lee el código fuente de una manera que es común en la cultura occidental: de arriba hacía abajo y de izquierda a derecha. Hay algunas excepciones: se cubrirán más adelante en el curso.

En primer lugar, el intérprete verifica si todas las líneas subsiguientes son correctas (utilizando los cuatro aspectos tratados anteriormente).

Si el compilador encuentra un error, termina su trabajo inmediatamente. El único resultado en este caso es un mensaje de error. El intérprete le informará dónde se encuentra el error y qué lo causó. Sin embargo, estos mensajes pueden ser engañosos, ya que el intérprete no puede seguir tus intenciones exactas y puede detectar errores a cierta distancia de tus causas reales.

Por ejemplo, si intentas usar una entidad de un nombre desconocido, causará un error, pero el error se descubrirá en el lugar donde se intenta usar la entidad, no donde se introdujo el nombre de la nueva entidad.

En otras palabras, la razón real generalmente se ubica un poco antes en el código, por ejemplo, en el lugar donde se tuvo que informar al intérprete de que usaría la entidad del nombre.

Si la línea se ve bien, el intérprete intenta ejecutarla (nota: cada línea generalmente se ejecuta por separado, por lo que el trío "Lectura - Verificación - Ejecución", pueden repetirse muchas veces, más veces que el número real de líneas en el archivo fuente, como algunas partes del código pueden ejecutarse más de una vez).

También es posible que una parte significativa del código se ejecute con éxito antes de que el intérprete encuentre un error. Este es el comportamiento normal en este modelo de ejecución.

Puedes preguntar ahora: ¿Cuál es mejor? ¿El modelo de "compilación" o el modelo de "interpretación"? No hay una respuesta obvia. Si hubiera habido, uno de estos modelos habría dejado de existir hace mucho tiempo. Ambos tienen sus ventajas y sus desventajas.

## Compilación vs. Interpretación - Ventajas y Desventajas

![Tabla Comparativa](/archivos/images/imagenes-anotaciones-PCAP/Compilacion-vs-Interpretacion-Ventajas-Desventajas.png)

**¿Qué significa todo esto para ti?**

- Python es un lenguaje interpretado. Esto significa que hereda todas las ventajas y desventajas descritas. Por supuesto, agrega algunas de sus características únicas a ambos conjuntos.
- Si deseas programar en Python, necesitarás el intérprete de Python. No podrás ejecutar tu código sin él. Afortunadamente, Python es gratis. Esta es una de sus ventajas más importantes.

Debido a razones históricas, los lenguajes diseñados para ser utilizados en la manera de interpretación a menudo se llaman lenguajes de programación, mientras que los programas fuente codificados que los usan se llaman scripts.
