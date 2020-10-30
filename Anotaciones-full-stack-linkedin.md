
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






